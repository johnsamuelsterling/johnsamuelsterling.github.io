---
layout: page
title: "Home"
class: home
---

# Hi, I'm John Sterling

<div class="columns" markdown="1">

<div class="intro" markdown="1">
I am a second year graduate student at [Auburn University](https://www.auburn.edu/cosam/departments/math/) studying under Dr. Ziqin Feng. I earned a B.S. in Mathematics alonside a minor in Philosophy from the [University of Alabama in Huntsville](https://www.uah.edu/). Additionally, I have been a research associate at the [Rotorcraft Systems Engineering and Simulation Center](https://www.uah.edu/rsesc). Details are in my [CV]({{ "/cv/" | relative_url }}).

My research interests lie in topology, specifically algebraic and combinatorial topology. I am particularly interested in the study of Čech and Vietoris-Rips complexes as well as persistent homology. 

Find me on [GitHub](https://github.com/johnsamuelsterling) and [LinkedIn](https://www.linkedin.com/in/john-sterling-87712817a/).
</div>

<div class="me" markdown="1">
<picture>
  <source srcset='/images/JohnCoffeeAU.webp' type='image/webp' />
  <img
    src='/images/JohnCoffeeAU.png'
    alt='John Sterling'>
</picture>

{:.no-list}
* <a href="mailto:{{ site.email }}">{{ site.email }}</a>
* Parker Hall, Office 142
</div>
</div>

## Featured <a href="{{ "/publications/" | relative_url }}">Publications</a>

<div class="featured-publications">
  {% assign sorted_publications = site.publications | sort: 'year' | reverse %}
  {% for pub in sorted_publications %}
    {% if pub.highlight %}
      <a href="{{ pub.pdf }}" class="publication">
        <strong>{{ pub.title }}</strong>
        <span class="authors">{% for author in pub.authors %}{{ author }}{% unless forloop.last %}, {% endunless %}{% endfor %}</span>.
        <i>{% if pub.venue %}{{ pub.venue }}, {% endif %}{{ pub.year }}</i>.
        {% for award in pub.awards %}<br/><span class="award"><i class="fas fa-{% if award == "Best Paper Award" %}trophy{% else %}award{% endif %}" aria-hidden="true"></i> {{ award }}</span>{% endfor %}
      </a>
    {% endif %}
  {% endfor %}
</div>

<a href="{{ "/publications/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  Show All Publications
</a>

<div class="news" markdown="1">
## Latest News

<ul>
{% for news in site.data.news limit:5 %}
  {% include news.html news=news %}
{% endfor %}
</ul>
[(see all)]({{ absolute_url }}/news) 

</div>

<div class="travel" markdown="1">
