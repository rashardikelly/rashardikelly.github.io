---
layout: post
mermaid: true
published: true
title: "Listing Posts in LiQUiD "
tags: computing jekyll programming webdesign blogging tips
catagories: computing jekyll programming webdesign blogging tips
image: post_computingq.PNG

---
[music](https://www.youtube.com/watch?v=stwV3Q2q2RY)
### Collections 
a great way to group related content [read](https://jekyllrb.com/docs/collections/) 
[LiquidBasics](https://shopify.dev/docs/api/liquid/basics) [LOOPiNG](https://shopify.github.io/liquid/tags/iteration/) ; [tutorial](https://www.shopifyacademy.com/getting-started-with-liquid-for-developers-new)

[Liquid reference](https://shopify.dev/docs/api/liquid) Liquid is a template language created by Shopify. It's available as [an open source project on GitHub](https://github.com/ThakaRashard/liquid), and is used by many different software projects and [companies](https://www.nasa.gov/international-space-station/).
[Comments in GitHub flavour of Markdown](https://gist.github.com/jonikarppinen/47dc8c1d7ab7e911f4c9)
>[TryingThis](https://gist.github.com/jonikarppinen/47dc8c1d7ab7e911f4c9?permalink_comment_id=3450152#gistcomment-3450152)
[//]: # (This is a comment.)
[//]: # (This is a comment on a new line.)
![image](https://github.com/user-attachments/assets/6433a024-6b1e-4c09-a48a-659f125729c9)
[Creating and highlighting code blocks - MARKDOWN @github](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks) [HiGHTLiGHTiNG](https://www.markdownguide.org/extended-syntax/#highlight) ![SHOPiFY](https://cdn.shopify.com/shopifycloud/web/assets/v1/vite/client/en/assets/shopify-wordmark-monochrome-CpVsfBAAmxEP.svg)
I need to highlight these ==very important words==.
```
I need to highlight these ==very important words==.
```
[https://admin.shopify.com/store/holetoanotheruniverse](https://admin.shopify.com/store/holetoanotheruniverse) 


[ASTRALWERKS CASSETTE SAMPLER SUMMER 1994](https://youtu.be/kypmFar9CRE?t=1248)
![BAKERSFiELD](https://eoimages.gsfc.nasa.gov/images/imagerecords/80000/80595/wasco_ast_2011191_lrg.jpg)
# Listing Tags 

<div class="tupperware" >
 
<tr>
{% for tag in page.tags %}
<td>{{ tag }}</td>
{% endfor %}
</tr>

</div>

<div class="tupperware" >
<tr>
{% for tag in page.tags %}
<td>{{ tag }}</td>
{% endfor %}
</tr>
</div>

{% raw %}

<div class="tupperware" >
 
<tr>
{% for tag in page.tags %}
<td>{{ tag }}</td>
{% endfor %}
</tr>

</div>

{% endraw %}






{% for tag in site.tags %}
  <h3>{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ site.github.url }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}



{% raw %}

{% for tag in site.tags %}
  <h3>{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ site.github.url }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}

{% endraw %}



# Listing Posts
<div class="tupperware" >
 {% for LA in site.categories %}

   
  <ul>
             {% for posts in category %}
               {% for post in posts %}
                 {% if post.url %}
         <li>
          <h2><a href="{{ post.url | prepend: site.baseurl | replace: '//', '/' }}">{{ post.title }}</a></h2>
          <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date_to_string }}</time>
          <p>{{ post.content | strip_html | truncatewords:50 }}</p>
      </li>
                {% endif %}
              {% endfor %}
            {% endfor %}
         </ul>
    
 {% endfor %}

 </div>

@jekyll @nasa-jpl @blackgirlscode test bed 



{% for LA in site.tags %}
  <h3>{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ site.github.url }}{{ post.url }}">{{ post.title }}</a></li>
      <article class="paginator">
  <a href="{{ site.github.url }}{{ post.url }}">
    <div class="featured-post" {% if post.image %}style="background-image:url({{ site.github.url }}/assets/img/{{ post.image }})"{% endif %}>
      <h2><span>{{ post.title }}</span></h2>
    </div>
  </a>
</article>
    {% endfor %}
  </ul>
{% endfor %}

{% raw %}

{% for LA in site.tags %}
  <h3>{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ site.github.url }}{{ post.url }}">{{ post.title }}</a></li>
      <article class="paginator">
  <a href="{{ site.github.url }}{{ post.url }}">
    <div class="featured-post" {% if post.image %}style="background-image:url({{ site.github.url }}/assets/img/{{ post.image }})"{% endif %}>
      <h2><span>{{ post.title }}</span></h2>
    </div>
  </a>
</article>
    {% endfor %}
  </ul>
{% endfor %}

{% endraw %}


<ul>
    {% for post in site.posts %}
      <li>
          <h2><a href="{{ post.url | prepend: site.baseurl | replace: '//', '/' }}">{{ post.title }}</a></h2>
          <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date_to_string }}</time>
          <p>{{ post.content | strip_html | truncatewords:50 }}</p>
      </li>
    {% endfor %}
</ul>

{% raw %}

<ul>
    {% for post in site.posts %}
      <li>
          <h2><a href="{{ post.url | prepend: site.baseurl | replace: '//', '/' }}">{{ post.title }}</a></h2>
          <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date_to_string }}</time>
          <p>{{ post.content | strip_html | truncatewords:50 }}</p>
      </li>
    {% endfor %}
</ul>

{% endraw %}


{% for mars in site.tags %}
  <h3>{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ site.github.url }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}

{% raw %}

{% for mars in site.tags %}
  <h3>{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ site.github.url }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}

{% endraw %}



  {% for post in site.posts %}
    
<article class="paginator">
  <a href="{{ site.github.url }}{{ post.url }}">
    <div class="featured-post" {% if post.image %}style="background-image:url({{ site.github.url }}/assets/img/{{ post.image }})"{% endif %}>
      <h2><span>{{ post.title }}</span></h2>
    </div>
  </a>
</article>

  {% endfor %}

{% raw %}

  {% for post in site.posts %}
    
<article class="paginator">
  <a href="{{ site.github.url }}{{ post.url }}">
    <div class="featured-post" {% if post.image %}style="background-image:url({{ site.github.url }}/assets/img/{{ post.image }})"{% endif %}>
      <h2><span>{{ post.title }}</span></h2>
    </div>
  </a>
</article>

  {% endfor %}

{% endraw %}



[markdouwn](https://humanwhocodes.com/blog/2019/04/jekyll-hooks-output-markdown/) 
@blackgirlscode 
