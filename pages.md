---
layout: default
---

# Pages directory

Pages available on myfiles.ga-

{% for page in site.pages %}
  {% if page.categories contains 'pages' %}
  <li><a href="{{page.url}}" style="color:#b5e853;">{{page.title}}</a></li><br>
  {% endif %}
{% endfor %}

To learn how to create a page, go through this [example](https://drive.google.com/file/d/1zChg_4ftQVWqrdxO7uPYkQR6d5A5MwH9/view) page. Just type your content in a plain text file and mail it to [sam@orthosam.com](mailto:sam@orthosam.com) and watch it go live!
