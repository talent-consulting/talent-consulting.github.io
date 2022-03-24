---
category: SubIndex
type: Index 
---

{% assign pages = site.pages 
| where: "type", "Guides" 
| group_by: "category" %}


{% for page in pages %}

### {{page.name }}
<div class="grid is-fibonacci">
    {% for item in page.items %}

    <div class="grid-item">
        <div class="columns is-mobile is-gapless has-box-shadow-heavy has-border-radius-large has-overflow-hidden is-relative"
            data-bi-name="card">
            <div class="column is-4">
                <div class="is-flex has-flex-align-items-center has-flex-justify-content-center is-full-height"
                    style="background-color: #00518F;">
                    <span aria-hidden="true">
                        <i class="{{ item.icon }}"></i>
                    </span>
                </div>
            </div>
            <div class="column is-8 has-body-background">
                <div class="has-padding-medium">
                    <a href="{{ item.url | relative_url }}"  class="is-block stretched-link" data-linktype="absolute-path">
                        <h2 id="{{ item.title | remove: ' ' }}" class="is-size-large">{{ item.title }}</h2>
                    </a>
                </div>
            </div>
        </div>
    </div>
    {% endfor %}
</div>

{% endfor %}