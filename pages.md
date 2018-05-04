---
layout: default
---

# Pages directory

{% for page in site.pages %}
  {% if page.categories contains 'fruit' %}
    <div class="item">
      <h3>{{page.title}}</h3>
      <p>{{page.description}}</p>  
    </div>
  {% endif %}
{% endfor %}

To learn how to create a page, go through this [example](https://drive.google.com/file/d/1zChg_4ftQVWqrdxO7uPYkQR6d5A5MwH9/view) page. Just type your content in a plain text file and mail it to [sam@orthosam.com](mailto:sam@orthosam.com) and watch it go live!
