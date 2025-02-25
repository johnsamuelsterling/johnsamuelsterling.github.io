---
layout: page
title: "Home"
class: home
---

# Hi, I'm John Sterling

<div class="columns" markdown="1">

<div class="intro" markdown="1">
I am a second year graduate student at [Auburn University](https://www.auburn.edu/cosam/departments/math/) studying under Dr. Ziqin Feng. I earned a B.S. in Mathematics alonside a minor in Philosophy from the [University of Alabama in Huntsville](https://www.uah.edu/). Additionally, I have been a research associate at the [Rotorcraft Systems Engineering and Simulation Center](https://www.uah.edu/rsesc).

My research interests lie in topology, specifically algebraic and combinatorial topology. I am particularly interested in the study of Čech and Vietoris-Rips complexes as well as persistent homology. 

Find me on [GitHub](https://github.com/johnsamuelsterling) and [LinkedIn](https://www.linkedin.com/in/john-sterling-87712817a/).
</div>

<div class="me" markdown="1">
<picture>
  <source srcset='/images/JohnCoffeeAU.webp' type='image/webp' />
  <img
    src='/images/JohnCoffeeAU.jpg'
    alt='John Sterling'>
</picture>

{:.no-list}
* <a href="mailto:{{ site.email }}">{{ site.email }}</a>
* NSH 2504B
</div>

</div>

During my first year at UW, I received support from the [Fulbright program](https://en.wikipedia.org/wiki/Fulbright_Program). In 2013, I received my B.S. from [Hasso Plattner Institute](https://hpi.de/). I am a scholar of the [German National Academic Foundation](http://www.studienstiftung.de/). I have worked with the [Open Knowledge Foundation](http://www.okfn.org), [Google Research](https://ai.google/research/), [Microsoft Research](https://www.microsoft.com/en-us/research/group/vibe/), and others. Details are in my [CV]({{ "/cv/" | relative_url }}).

## Featured <a href="{{ "/projects/" | relative_url }}">Projects</a>

<div class="featured-projects">
  {% assign sorted_projects = site.data.projects | sort: 'highlight' %}
  {% for project in sorted_projects %}
    {% if project.highlight %}
      {% include project.html project=project %}
    {% endif %}
  {% endfor %}
</div>

<a href="{{ "/projects/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  Show More Projects
</a>

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
