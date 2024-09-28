---
layout: default
permalink: /courses/
title: Courses
datatable: true
---
<p><H2 style="display: inline-block;" >"Without a certificate you do not exist."</H2>&nbsp;&nbsp;<h5  style="display: inline-block;" > (Old russian proverb)</h5></p>

<table id="retraining" class="display" style="width:100%">
  <thead>
    <tr>
      <th>Retraining Course</th>
      <th>Description</th>
      <th>Issuer</th>
      <th style="width:20%">Tags</th>
      <th style="width:20%">Year</th>
    </tr>
  </thead>
  <tbody>
  {% for retraining in site.retraining %}
    <tr>
      <td><a href="{{ retraining.url }}">{{ retraining.title }}</a></td>
      <td>{{retraining.description}}</td>
      <td>{{retraining.issuer}}</td>
      <td>
      <h6>
       {% for tag in retraining.tags %}
  <a class="post" href="/tag/{{tag}}">{{tag}}</a>{% unless forloop.last %}, {% endunless %}
  {% endfor %}</h6>
      </td>
      <td>{{retraining.year}}</td>
    </tr>
    {% endfor %}
  </tbody>
</table>




<table id="onlinecourses" class="display" style="width:100%">
  <thead>
    <tr>
      <th>Course Name</th>
      <th>Date</th>
      <th>Issuer</th>
      <th>Certificate</th>
    </tr>
  </thead>
  <tbody>
  {% for course in site.data.courses %}
    <tr>
      <td>{{course.Name}}</td>
      <td>{{course.Date}}</td>
      <td>{{course.Issuer}}</td>
      <td><a href="{{course.Link}}">Certificate</a></td>
    </tr>
    {% endfor %}
  </tbody>
</table>

<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
<script src="https://cdn.datatables.net/1.10.25/js/jquery.dataTables.js"></script>
<script>
  $(document).ready(function() {
    $('#onlinecourses').DataTable();
  });
</script>

