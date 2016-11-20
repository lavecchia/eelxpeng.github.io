---
layout: page
permalink: /research/
title: Research
pubs:

    - title:   "Connection Discovery using Shared Images by Gaussian Relational Topic Model"
      author:  "X. Li, M. Cheung and J. She"
      journal: "IEEE International Conference on Big Data"
      note:    "(Accepted)"
      year:    "2016"
      url:     ""
      media:
        - name: "paper"
          url:  "http://cci.drexel.edu/bigdata/bigdata2016/"

    - title:   "Visual Background Recommendation for Dance Performances Using Dancer-Shared Images"
      author:  "J. Wen, X. Li, J. She, S. Park and M. Cheung"
      journal: "IEEE International Conference on Cyber Physical and Social Computing"
      note:    "(Accepted)"
      year:    "2016"
      url:     ""
      media:
        - name: "paper"
          url:  "http://umc.uestc.edu.cn/conference/cybermatics2016/CPSCom2016/accepted-list.php"

    - title:   "Non-user Generated Annotation on User Shared Images for Con- nection Discovery"
      author:  "M. Cheung, J. She and X. Li"
      journal: "IEEE International Conference on Cyber Physical and Social Computing"
      year:    "2015"
      url:     ""
      media:
        - name: "paper"
          url:  "http://ieeexplore.ieee.org/document/7396504/?arnumber=7396504&tag=1"

    
---

## Publications

{% assign thumbnail="left" %}

{% for pub in page.pubs %}
{% if pub.image %}
{% include image.html url=pub.image caption="" height="100px" align=thumbnail %}
{% endif %}
[**{{pub.title}}**]({% if pub.internal %}{{pub.url | prepend: site.baseurl}}{% else %}{{pub.url}}{% endif %})<br />
{{pub.author}}<br />
*{{pub.journal}}*
{% if pub.note %} *({{pub.note}})*
{% endif %} *{{pub.year}}* {% if pub.doi %}[[doi]({{pub.doi}})]{% endif %}
{% if pub.media %}<br />Media: {% for article in pub.media %}[[{{article.name}}]({{article.url}})]{% endfor %}{% endif %}

{% endfor %}