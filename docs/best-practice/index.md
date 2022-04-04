---
category: Guides
type: Best practice
pagetype: Index
icon: fas fa-ranking-star fa-2x
description: Best practices when developing 
order: 10000
---

# Best practices
 
> The documents in this section talk through the company and how we operate
 
{% assign pages = site.pages
  | where: "category", "Guides"
  | where: "subtype", "Devops"
  | group_by: "type" %}
 
{% for page in pages %}

### {{ page.name }}

<div class="grid is-fibonacci">
    {% for item in page.items %}
        {% if item.pagetype != "Index" %}
    <div class="grid-item">
        <div class="columns is-mobile is-gapless has-box-shadow-heavy has-border-radius-large has-overflow-hidden is-relative"
            data-bi-name="card">
            <div class="column is-4">
                <div class="is-flex has-flex-align-items-center has-flex-justify-content-center is-full-height"
                    style="background-color: #018EAC;">
                    <span aria-hidden="true">
                        <i class="{{ item.icon }}"></i>
                    </span>
                </div>
            </div>
            <div class="column is-8 has-body-background">
                <div class="has-padding-medium">
                    <a href="{{ item.url | relative_url }}"  class="is-block stretched-link" data-linktype="absolute-path">
                        <h2 id="{{ item.title | remove: ' ' }}" class="is-size-large">{{ item.title }}</h2>
                        <p class="subIndex">{{item.description}}</p>
                    </a>
                </div>
            </div>
        </div>
    </div>
        {% endif %}
    {% endfor %}
</div>
{% endfor %}
