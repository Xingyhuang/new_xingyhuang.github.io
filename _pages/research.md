---
layout: page
order: 1
title: RESEARCH
permalink: /research/
description: 
nav: true
---
<br>

{% for project in site.data.research %}
<hr style="border:none; background-color:#828282; height:3px">
<a name="{{project.title}}" style="padding-top: 45px; margin-top: -45px;"></a>
<p style="font-size:18pt">
{{project.title}}</p>

<div style="line-height:50%;"> <br></div>
<div class="row">
<div class="column" align="center">
 <br/>
   <figure>
  <img src="{{ project.figure }}" style="width:80%">
 </figure> 
  <p style="margin-left:0%; width:85%; font-size:10pt;">
  <i>{{project.caption}}</i>
  </p>
  </div>
  <div class="column">
  {% for question in project.questions%}
  <p style="margin-left:0%; width:100%;font-size:12pt; font-weight:bold">{{question.q}}</p>
  <p style="margin-left:0%; width:100%; font-size:12pt">
  {{question.description}}
  </p>
  {% endfor %}
  
  {% if project.pubs %}
  <p style="margin-left:0%; width:100%;font-size:11pt">
  <b>Related Publications:</b>
  {% for pub in project.pubs %}
  <a href="{{pub.link}}" target='_blank'>{{pub.name}}</a>
  {% endfor %}
  </p>
  {% endif %}
  {% if project.media %}
  <p style="margin-left:0%; width:100%;font-size:11pt">
  <b>Related Media Coverage:</b>
  {% for media in project.media %}
  <a href="{{media.link}}" target='_blank'>{{media.name}}</a>
  {% endfor %}
  </p>
  {% endif %}

  
  
  </div>
</div>
{% endfor %}

<br/>
<hr style="border:none; background-color:#828282; height:3px">
