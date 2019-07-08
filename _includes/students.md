  <h2>Students</h2>
  <table>
  <!-- <thead>
  <tr><th>pic</th><th>name</th><th>year</th></tr>
  </thead> -->
<tbody>
{% for student in site.students %}
   <tr>

    <td class="pic">
      <img class="personimageSmall" src="{{ student.url }}/profile.jpg" alt="thumbnail" >
     </td>
     <td class="name"><a href="{{student.url}}">{{ student.name }}</a></td>
     </tr>
   {% endfor %}
</tbody>
  </table>
