---
layout: default
title: Course Schedules
---
{% if site.archived == true %}
Obviously this course isn't active and there aren't any discussion sections or office hours. But I left a bunch of sample data in the repo to show how the backend works when you need to display a weekly schedule (in this case OHs). It was tricky to get working at the time but I built everything so that you only need to set the time(s) in the people.yml file and everything is beautifully displayed on the schedule table. Super helpful since staff needs to change OH times frequently throughout the semester and all you need to do on your end is to change a few values in the .yml file instead of futzing with a bunch of HTML.   
{% endif %}


#### Lectures

<table id="customers">
  <tr>
    <th> Section </th>
    <th> Tuesdays and Thursdays at </th>
    <th> Who </th>
    <th> Location </th>
  </tr>
  <tr>
    <td> BL1 </td>
    <td> 12:30PM - 1:45PM </td>
    <td> Kani </td>
    <td> 0027/1025 CIF </td>
  </tr>
</table>
&nbsp;

#### Discussion Sections
<table id="customers">
  <tr>
    <th> Section </th>
    <th> Wednesdays and Fridays at </th>
    <th> Who </th>
    <th> Location </th>
  </tr>
  <tr>
    <td> BYA </td>
    <td> 09:00AM - 09:50AM </td>
    <td> Jack Chen, Yueyi Shen </td>
    <td> 2017 ECEB </td>
  </tr>
  <tr>
    <td> BYB </td>
    <td> 10:00AM - 10:50AM </td>
    <td> Haoyuan You </td>
    <td> 0216 Siebel </td>
  </tr>
  <tr>
    <td> BYC </td>
    <td> 11:00AM - 11:50AM </td>
    <td> Sindhu Vydana </td>
    <td> 4070 ECEB </td>
  </tr>
  <tr>
    <td> BYD </td>
    <td> 12:00PM - 12:50PM </td>
    <td> Sandhya Perumenki </td>
    <td> 4070 ECEB </td>
  </tr>
  <tr>
    <td> BYE </td>
    <td> 01:00PM - 01:50PM </td>
    <td> Weiyang Wang, Sumedh Vemuganti </td>
    <td> 4070 ECEB </td>
  </tr>
  <tr>
    <td> BYF </td>
    <td> 02:00PM - 02:50PM </td>
    <td> Sung Woo Jeon </td>
    <td> 4070 ECEB </td>
  </tr>
</table>
&nbsp;

#### Office hours
Office hours will be conducted by the instructor(s), TAs and CAs. Office hours are not a place to check if your homework solutions are correct (the CAs do not even have access to the homework solutions). Office hours are meant to help you master the course concepts and assist you in working through any assignments when you are stuck. 

{% include OHs_table.html %}


