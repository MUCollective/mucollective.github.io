---
layout: default
title: "Publications"
---

<div class="main-section-wrap">
  <div class="search-wrap">
    <div class="form-row">
      <label for="paper-search">Search by title or author name</label>
      <input name="paper-search" id="paper-search" type="text" onkeyup=" search(event)" />
    </div>
    <div class="year-filters form-row">
      <label for="paper-year">Filter by year</label>
      <div id="year-buttons"></div>
    </div>
    <div class="category-filters form-row">
      <label for="paper-year">Filter by categories</label>
      <div id="category-buttons"></div>
    </div>
    <div class="form-row">
      <label><span id="n-papers"></span> paper(s)</label>
      <button id="clear-all" onclick="clear_all()">Clear all</button>
    </div>
  </div>
  {% for post in site.posts %}
    {% if post.category contains 'paper' %}
      {% assign currentdate = post.date | date: "%Y" %}
      {% if currentdate != date %}
        <h3 class="post-cat-title year" id="y{{currentdate}}">{{ currentdate }}</h3>
        {% assign date = currentdate %}
      {% endif %}
        {% include paper-list-item.html
          title=post.title
          thumb=post.thumb
          url=post.url
          authors=post.authors
          venue=post.venue
          bestPaper=post.bestPaper
          honorable=post.honorable
          pdf=post.pdf
          supplementary=post.supplementary
          github=post.github
          additionals=post.additionals
          category=post.category
          year=currentdate
        %}
    {% endif %}
  {% endfor %}
</div>

  <script>
    // filter
    let year_filter_items = [];
    let category_filter_items = [];
    let filter_status = {};
    function load_filters() {
      // year filter
      year_filter_items = Array.from(document.querySelectorAll(".post-cat-title.year")).map((yt) => {
        return {year: yt.innerText, selected: false};
      });
      category_filter_items = [
{% for topic in site.data.research_areas %}
        { name: '{{topic.name}}', key: '{{topic.category}}', selected: false },
{% endfor %}
{% for topic in site.data.minor_topics %}
        { name: '{{topic.name}}', key: '{{topic.category}}', selected: false },
{% endfor %}
      ];

      year_filter_items.forEach((y) => {
        let button = document.createElement("button");
        button.innerHTML = y.year;
        button.addEventListener ("click", () => {
          y.selected = !y.selected;
          if (y.selected) {
            filter_by("year", "on", y.year);
            button.classList.add("selected");
          } else {
            filter_by("year", "off", y.year);
            button.classList.remove("selected");
          }
        });
        document.querySelector("#year-buttons").append(button);
      });

      category_filter_items.forEach((y) => {
        let button = document.createElement("button");
        button.innerHTML = y.name;
        button.addEventListener ("click", () => {
          y.selected = !y.selected;
          if (y.selected) {
            filter_by("category", "on", y.key);
            button.classList.add("selected");
          } else {
            filter_by("category", "off", y.key);
            button.classList.remove("selected");
          }
        });
        document.querySelector("#category-buttons").append(button);
      });
    }

    function filter_by(by, onf, value) {
      if (!filter_status[by]) filter_status[by] = [];
      filter_status[by] = filter_status[by].filter(d => d !== value);
      if (onf === "on") {
        filter_status[by].push(value);
      }
      let year_check = [];
      article_data.forEach((art) => {
        let matches = Object.keys(filter_status).map((fby) =>  {
          if (fby === "category") {
            if (filter_status[fby]?.length == 0 || !filter_status[fby]) return 1;
            else if (art[fby].some(a => filter_status[fby].includes(a))) return 1;
            else return -1;
          } else {
            if (filter_status[fby]?.length == 0 || !filter_status[fby]) return 1;
            else if (filter_status[fby].includes(art[fby])) return 1;
            else return -1;
          }
        });
        if (!matches.every(d => d == 1)) {
          art.dom.classList.add("filter-hidden");
        } else {
          art.dom.classList.remove("filter-hidden");
          year_check.push(art.year);
        }
      });
      document.querySelectorAll(".post-cat-title.year").forEach((yt) => {
        if (!year_check.includes(yt.innerText)) yt.classList.add("filter-hidden");
        else  yt.classList.remove("filter-hidden");
      });
      update_paper_numbers();
    }

    // search
    let article_data = [];
    function parse_items() {
      article_data = Array.from(document.querySelectorAll('article.paper-list-item')).map((dom) => {return {
        dom,
        title: dom.getAttribute("data-title").toLowerCase(),
        authors: dom.getAttribute("data-authors").toLowerCase(),
        category: dom.getAttribute("data-category").split(/\s+/gi),
        year: dom.getAttribute("data-year")
        };
      });
    }

    function search(event) {
      let search_text = event?.target?.value || "";
      if (article_data.length == 0) {
        parse_items();
      }
      let year_check = [];
      if (search_text.length == 0) {
        clear_search();
      } else {
        let tokens = search_text.toLowerCase().split(/\s+/gi);
        article_data.forEach((art) => {
          let matches = tokens.map((d) => {
            if (art.title.includes(d)) return 1;
            else if (art.authors.includes(d)) return 1;
            return -1;
          });
          if (!matches.every(d => d == 1)) {
            art.dom.classList.add("hidden");
          } else {
            art.dom.classList.remove("hidden");
            year_check.push(art.year);
          }
        });
        document.querySelectorAll(".post-cat-title.year").forEach((yt) => {
          if (!year_check.includes(yt.innerText)) yt.classList.add("hidden");
        });
        update_paper_numbers();
      }
    }
    function clear_search() {
      article_data.forEach((art) => {
        art.dom.classList.remove("hidden");
      });
      document.querySelectorAll(".post-cat-title").forEach((yt) => {
        yt.classList.remove("hidden");
      });
      update_paper_numbers();
    }
    parse_items();
    load_filters();

    function clear_all() {
      document.querySelector("#paper-search").value = "";
      article_data.forEach((art) => {
        art.dom.classList.remove("hidden");
        art.dom.classList.remove("filter-hidden");
      });
      document.querySelectorAll(".post-cat-title").forEach((yt) => {
        yt.classList.remove("hidden");
        yt.classList.remove("filter-hidden");
      });
      filter_status = {};
      year_filter_items.forEach(y => y.selected = false);
      document.querySelectorAll("#year-buttons button").forEach((button) => button.classList.remove("selected"));
      category_filter_items.forEach(y => y.selected = false);
      document.querySelectorAll("#category-buttons button").forEach((button) => button.classList.remove("selected"));
      update_paper_numbers();
    }
    function update_paper_numbers() {
      document.querySelector("#n-papers").innerText = article_data.filter((art) => !art.dom.classList.contains("hidden") && !art.dom.classList.contains("filter-hidden")).length || 0;
    }
    update_paper_numbers();
  </script>
