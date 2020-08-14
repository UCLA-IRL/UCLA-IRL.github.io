---
layout: default
title: People
section_id: portfolio
categories:
  - internal: prof
    external: Professors
  - internal: phd-candidate
    external: Ph.D. Candidate
  - internal: phd-student
    external: Ph.D. Students
  - internal: masters
    external: Master's Students
  - internal: undergrad
    external: Undergraduate Students
  - internal: visitor
    external: Visiting Researchers
alumni_categories:
  - internal: alPHD
    external: Alumni (Ph.D. Students)
  - internal: alMasters
    external: Alumni (Master's Students)
  - internal: alVisitors
    external: Alumni (Visitors)
---


<div class='full parallax' style='background-image: url(images/banner/banner.jpg); color: #fff;'>
  <div class='row'>
    <div class='large-12 columns'>
      {% include section-header.html title="The team" tagline="The members of the IRL Group." color="#000000" class="big" %}
    </div>
  </div>
  <div class='four spacing'></div>
</div>


<div class='four spacing'></div>

<h1 style="text-align: center;">
  Current Members
</h1>

<div class='full'>
  <div class='row'>
    <div class='mod modGallery'>
      <div class='gallery-nav'>
        <ul>
          <li class='current'>
            <a data-cat='all' href='#'>All</a>
          </li>
          {% for category in page.categories %}
            <li>
              <a data-cat='{{ category.internal }}' href='#'>{{ category.external }}</a>
            </li>
          {% endfor %}
        </ul>
      </div>

      <ul class='gallery small-block-grid-5'>

        {% for category in page.categories %}
          {% for person in site.data.people %}
            {% if person.klass == category.internal %}
            <li class="{{ person.klass }}">
              <a href='{{ person.link_to }}'>
                <img alt="" src="{{ person.image }}" />
                <div class='overlay'>
                  <div class='thumb-info'>
                    <h3>{{ person.name }}</h3>
                    <p>{{ person.desc }}</p>
                  </div>
                </div>
              </a>
            </li>
            {% endif %}
          {% endfor %}
        {% endfor %}

      </ul>
    </div>
  </div>

  <div class='four spacing'></div>
</div>

<h1 style="text-align: center;">
  Alumni
</h1>

<div class='full'>
  <div class='row'>
    <div class='mod modGallery'>
      <div class='gallery-nav'>
        <ul>
          <li class='current'>
            <a data-cat='all' href='#'>All</a>
          </li>
          {% for category in page.alumni_categories %}
            <li>
              <a data-cat='{{ category.internal }}' href='#'>{{ category.external }}</a>
            </li>
          {% endfor %}
        </ul>
      </div>

      <ul class='gallery small-block-grid-5'>

        {% for category in page.alumni_categories %}
          {% for person in site.data.people %}
            {% if person.klass == category.internal %}
              <li class="{{ person.klass }}">
                <a href='{{ person.link_to }}'>
                  <img alt="" src="{{ person.image }}" />
                  <div class='overlay'>
                    <div class='thumb-info'>
                      <h3>{{ person.name }}</h3>
                      <p>{{ person.desc }}</p>
                    </div>
                  </div>
                </a>
              </li>
            {% endif %}
          {% endfor %}
        {% endfor %}

      </ul>

    </div>
  </div>

  <div class='four spacing'></div>
</div>