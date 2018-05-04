---
layout: default
---

# Pages directory

{% for cat in site.category-list %}
### {{ cat }}
<ul>
  {% for page in site.pages %}
    {% if page.resource == true %}
      {% for pc in page.categories %}
        {% if pc == cat %}
          <li><a href="{{ page.url }}">{{ page.title }}</a></li>
        {% endif %}   <!-- cat-match-p -->
      {% endfor %}  <!-- page-category -->
    {% endif %}   <!-- resource-p -->
  {% endfor %}  <!-- page -->
</ul>
{% endfor %}  <!-- cat -->

To learn how to create a page, go through this [example](https://drive.google.com/file/d/1zChg_4ftQVWqrdxO7uPYkQR6d5A5MwH9/view) page. Just type your content in a plain text file and mail it to [sam@orthosam.com](mailto:sam@orthosam.com) and watch it go live!
