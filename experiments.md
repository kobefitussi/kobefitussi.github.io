---
layout: default
permalink: /experiments/
title: Experiments
---
<p>
Experiments with code and hardware I enjoy to create, send me if you like it too</p>
<!--
<ul>
{% for experiment in site.experiments %}
 <li><a href="{{ experiment.url }}">{{ experiment.title }}</a>-{{ experiment.description }}<div style="text-color=gray">{{ experiment.tags }}</div></li>
{% endfor %}
</ul> -->

<table id="experiments" class="display" style="width:100%">
  <thead>
    <tr>
      <th >Experiment</th>
      <th>Description</th>
      <th style="width:20%">Tags</th>
    </tr>
  </thead>
  <tbody>
  {% for experiment in site.experiments %}
    <tr>
      <td><a href="{{ experiment.url }}">{{ experiment.title }}</a></td>
      <td>{{experiment.description}}</td>
      <td>
      <h6>
       {% for tag in experiment.tags %}
  <a class="post" href="/tag/{{tag}}">{{tag}}</a>{% unless forloop.last %}, {% endunless %}
  {% endfor %}</h6>
      </td>
    </tr>
    {% endfor %}
  </tbody>
</table>

<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
<script src="https://cdn.datatables.net/1.10.25/js/jquery.dataTables.js"></script>
<script>
  $(document).ready(function() {
    $('#experiments').DataTable({    scrollCollapse: true,
    scroller: true,
    scrollY: 500});
  });
</script>
