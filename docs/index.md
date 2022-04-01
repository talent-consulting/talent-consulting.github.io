# Talent Consulting hand book

## General

The following sections contains information for the public audience on Talent Consulting and information about how we work and the process, governance and standards we follow.

---

<div>
{% assign pages = site.pages
    | where: "pagetype", "Index" 
    | group_by: "category" %}

    {% for page in pages %}
        {% assign items = page.items | sort: "order" %}

    <h1 id="{{page.name}}">{{page.name}}</h1>
    
    <div class="grid is-fibonacci">
    
    {% for item in items %}
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
                        <a href="{{ item.dir | relative_url }}"  class="is-block stretched-link" data-linktype="absolute-path">
                            <h2 id="{{ page.title | remove: ' ' }}" class="is-size-large">{{ item.title }}</h2>
                        </a>
                        <p class="subIndex">{{item.description}}</p>
                    </div>
                </div>
            </div>
        </div>
    {% endfor %}

    </div>
    <hr/>
    {% endfor %}
</div>
