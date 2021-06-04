---
layout: workshop      # DON'T CHANGE THIS.
# More detailed instructions (including how to fill these variables for an
# online workshop) are available at
# https://carpentries.github.io/workshop-template/customization/index.html
venue: "University of Manchester"        # brief name of the institution that hosts the workshop without address (e.g., "Euphoric State University")
address: "online"      # full street address of workshop (e.g., "Room A, 123 Forth Street, Blimingen, Euphoria"), videoconferencing URL, or 'online'
country: "gb"      # lowercase two-letter ISO country code such as "fr" (see https://en.wikipedia.org/wiki/ISO_3166-1#Current_codes) for the institution that hosts the workshop
language: "en"     # lowercase two-letter ISO language code such as "fr" (see https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) for the
latitude: "53.46674756854867"        # decimal latitude of workshop venue (use https://www.latlong.net/)
longitude: "-2.2337120440390756"       # decimal longitude of the workshop venue (use https://www.latlong.net)
humandate: "08 - 11 June 2021"    # human-readable dates for the workshop (e.g., "Feb 17-18, 2020")
humantime: "9:30 - 12:30"    # human-readable times for the workshop (e.g., "9:00 am - 4:30 pm")
timezone: "BST (UTC+1)"
startdate: 2021-06-08      # machine-readable start date for the workshop in YYYY-MM-DD format like 2015-01-01
enddate: 2021-06-11        # machine-readable end date for the workshop in YYYY-MM-DD format like 2015-01-02
instructor: ["Phil Reed, Nilani Ganeshwaran, Doug Lowe, Shashank Harivyasi"] # boxed, comma-separated list of instructors' names as strings, like ["Kay McNulty", "Betty Jennings", "Betty Snyder"]
helper: ["Aleksandra Nenadic", "Gina Pegu", "Peter Smyth", "Carlene Barton", "Rosalind Bell", "Chris Grave"]     # boxed, comma-separated list of helpers' names, like ["Marlyn Wescoff", "Fran Bilas", "Ruth Lichterman"]
email: ["a.nenadic@manchester.ac.uk"]    # boxed, comma-separated list of contact email addresses for the host, lead instructor, or whoever else is handling questions, like ["marlyn.wescoff@example.org", "fran.bilas@example.org", "ruth.lichterman@example.org"]
collaborative_notes:  "https://pad.carpentries.org/2021-06-08-manchester-online" # optional: URL for the workshop collaborative notes, e.g. an Etherpad or Google Docs document (e.g., https://pad.carpentries.org/2015-01-01-euphoria)
eventbrite: "153867398531"           # optional: alphanumeric key for Eventbrite registration, e.g., "1234567890AB" (if Eventbrite is being used)
---

{% comment %} See instructions in the comments below for how to edit specific sections of this workshop template. {% endcomment %}

{% comment %}
HEADER

Edit the values in the block above to be appropriate for your workshop.
If the value is not 'true', 'false', 'null', or a number, please use
double quotation marks around the value, unless specified otherwise.
And run 'make workshop-check' *before* committing to make sure that changes are good.
{% endcomment %}


{% comment %}
Check DC curriculum
{% endcomment %}

{% if site.carpentry == "dc" %}
{% unless site.curriculum == "dc-ecology" or site.curriculum == "dc-genomics" or site.curriculum == "dc-socsci" or site.curriculum == "dc-geospatial" %}
<div class="alert alert-warning">
It looks like you are setting up a website for a Data Carpentry curriculum but you haven't specified the curriculum type in the <code>_config.yml</code> file (current value in <code>_config.yml</code>: "<strong>{{ site.curriculum }}</strong>", possible values: <code>dc-ecology</code>, <code>dc-genomics</code>, <code>dc-socsci</code>, or <code>dc-geospatial</code>). After editing this file, you need to run <code>make serve</code> again to see the changes reflected.
</div>
{% endunless %}
{% endif %}

{% comment %}
Check SWC curriculum
{% endcomment %}

{% if site.carpentry == "swc" %}
{% unless site.curriculum == "swc-inflammation" or site.curriculum == "swc-gapminder" %}
<div class="alert alert-warning">
It looks like you are setting up a website for a Software Carpentry curriculum but you haven't specified the curriculum type in the <code>_config.yml</code> file (current value in <code>_config.yml</code>: "<strong>{{ site.curriculum }}</strong>", possible values: <code>swc-inflammation</code>, or <code>swc-gapminder</code>). After editing this file, you need to run <code>make serve</code> again to see the changes reflected.
</div>
{% endunless %}
{% endif %}

<h2 id="general">General Information</h2>

{% if site.carpentry == "swc" %}
{% include swc/intro.html %}
{% elsif site.carpentry == "dc" %}
{% include dc/intro.html %}
{% elsif site.carpentry == "lc" %}
{% include lc/intro.html %}
{% endif %}

The workshop is organised jointly by colleagues from <a href="https://www.methods.manchester.ac.uk/" target="_blank">Methods@Manchester, <a href="https://www.library.manchester.ac.uk/" target="_blank">the University of Manchester Library</a>, <a href="https://www.itservices.manchester.ac.uk/research/" target="_blank">the University of Manchester Research IT</a>, and Manchester branch of <a href="https://software.ac.uk/" target="_blank">the Software Sustainability Institute</a>.

We are committed to providing a positive and accessible learning environment for all. Please
  notify the <a href="mailto:{{page.email}}">hosts</a> in advance of the workshop if you require any accommodations or if there is
  anything we can do to make this workshop more accessible to you.
  
<h3 id="audience">Audience</h3>
The workshop is aimed at the University of Manchester's postgraduate students and research and other staff who develop software or deal with or analyse data as part of their work. You don't need to have any previous knowledge of the tools that will be presented at the workshop - this is an introductory-level course.

<h3 id="where">When & Where</h3>
The workshop will be run online over 4 half-days, from {{page.humandate}}, {{page.humantime}} {{page.timezone}}. We will meet using the online videoconference software Zoom. You will need to <a href="https://zoom.us/download" target="_blank">download and install Zoom client</a> to connect with your instructors. The Zoom link to use for this event will be announced via email to registered participants.

<h3>Registration</h3>
Registration is free <a href="https://www.eventbrite.com/e/{{page.eventbrite}}" target="_blank">
via EventBrite</a>. You will need a special code to register - please get in touch with 
<a href='mailto:{{page.email}}'>Aleksandra Nenadic</a> using your Manchester email address.

<h3>Requirements</h3>
Participants must have a laptop/PC with a Mac, Linux, or Windows operating system (rather than a tablet, Chromebook, etc.) that they have administrative privileges on. They should have a few [specific software packages]({{site.baseurl}}/#setup) installed (listed below).

<h3>Code of Conduct</h3>

All participants (including instructors, helpers and observers) are required to abide by The Carpentries <a href="{{
site.swc_site }}/conduct/">Code of Conduct</a>.

<h3 id="contact">Contact</h3>
<p>
Please email
{% if page.email %}
  {% for contact in page.email %}
    {% if forloop.last and page.email.size > 1 %}
      or
    {% else %}
      {% unless forloop.first %}
      ,
      {% endunless %}
    {% endif %}
    <a href='mailto:{{contact}}'>{{contact}}</a>
  {% endfor %}
{% else %}
  to-be-announced
{% endif %}
for more information.
</p>

<hr/>

{% comment %}
Collaborative Notes

If you want to use an Etherpad, go to

https://pad.carpentries.org/YYYY-MM-DD-site

where 'YYYY-MM-DD-site' is the identifier for your workshop,
e.g., '2015-06-10-esu'.

Note we also have a CodiMD (the open-source version of HackMD)
available at https://codimd.carpentries.org
{% endcomment %}
{% if page.collaborative_notes %}
<h2 id="collaborative_notes">Collaborative Notes</h2>

<p>
We will use this <a href="{{ page.collaborative_notes }}">collaborative document</a> for chatting, taking notes, and sharing URLs and bits of code during the workshop.
</p>
<hr/>
{% endif %}


{% comment %}
SURVEYS - DO NOT EDIT SURVEY LINKS
{% endcomment %}
<h2 id="surveys">Surveys</h2>
<p>Please be sure to complete these surveys before and after the workshop.</p>
<p><a href="{{ site.pre_survey }}{{ site.github.project_title }}">Pre-workshop survey</a></p>
<p><a href="{{ site.post_survey }}{{ site.github.project_title }}">Post-workshop survey</a></p>

<hr/>


{% comment %}
SCHEDULE

Show the workshop's schedule.  Edit the items and times in the table
to match your plans.  You may also want to change 'Day 1' and 'Day
2' to be actual dates or days of the week.
{% endcomment %}
<h2 id="schedule">Schedule</h2>

<div class="row">
<!--  <div style="padding-left: 15px;">Before the workshop: please fill in the <a href="{{ site.pre_survey }}{{ site.github.project_title }}">pre-workshop survey</a></div>-->
  {% assign startdate = {{page.startdate}} | date: '%s' %}
  {% assign day1 =  startdate | date_to_long_string %}
  {% assign day2 =  startdate | plus: 86400 | date_to_long_string %}
  {% assign day3 =  startdate | plus: 86400 | plus: 86400 | date_to_long_string %}
  {% assign day4 =  startdate | plus: 86400 | plus: 86400 | plus: 86400 | date_to_long_string %}

  <div class="col-md-6">
    <h3>Day 1, {{day1}}, {{page.humantime}} {{page.timezone}}</h3>
    <table class="table table-striped">
      <tr> <td><a href="https://librarycarpentry.org/lc-data-intro/">Introduction to Working with Data (Regular Expressions)</a></td> </tr>
    </table>
  </div>
  <div class="col-md-6">
    <h3>Day 2, {{day2}}, {{page.humantime}} {{page.timezone}}</h3>
    <table class="table table-striped">
      <tr> <td><a href="https://librarycarpentry.org/lc-shell/" target="_blank">Automating tasks with UNIX Shell</a></td> </tr>
    </table>
  </div>
</div>
<div class="row">
    <div class="col-md-6">
    <h3>Day 3, {{day3}}, {{page.humantime}} {{page.timezone}}</h3>
    <table class="table table-striped">
      <tr> <td><a href="https://librarycarpentry.org/lc-open-refine/" target="_blank">Data Cleaning with OpenRefine</a></td> </tr>
    </table>
  </div>
  <div class="col-md-6">
      <h3>Day 4, {{day4}}, {{page.humantime}} {{page.timezone}}</h3>
      <table class="table table-striped">
        <tr> <td><a href="https://librarycarpentry.org/lc-git/" target="_blank">Introduction to Git & GitHub</a></td> </tr>
      </table>
  </div>
</div>

<hr/>

{% comment %}
SYLLABUS

Show what topics will be covered.

1. If your workshop is R rather than Python, remove the comment
around that section and put a comment around the Python section.
2. Some workshops will delete SQL.
3. Please make sure the list of topics is synchronized with what you
intend to teach.
4. You may need to move the div's with class="col-md-6" around inside
the div's with class="row" to balance the multi-column layout.

This is one of the places where people frequently make mistakes, so
please preview your site before committing, and make sure to run
'tools/check' as well.
{% endcomment %}
{% comment %}
<h2 id="syllabus">Syllabus</h2>

{% if site.carpentry == "swc" %}
{% include swc/syllabus.html %}
{% elsif site.carpentry == "dc" %}
{% include dc/syllabus.html %}
{% elsif site.carpentry == "lc" %}
{% include lc/syllabus.html %}
{% endif %}

<hr/>
{% endcomment %}

<h2 id="setup">Setup</h2>
<h3>Installation instructions</h3>
<p>
  To participate in this workshop,
  you will need to install <strong>all of the software described below before coming to the workshop</strong>. We will run a pre-workshop installation session to help everyone set up and make sure they have the required software installed.
</p>

{% if site.carpentry == "swc" %}
{% include swc/setup.html %}
{% elsif site.carpentry == "dc" %}
{% include dc/setup.html %}
{% elsif site.carpentry == "lc" %}
{% include lc/setup.html %}
{% endif %}

<p>
  We maintain a list of common issues that occur during installation as a reference for instructors
  that may be useful on the
  <a href = "{{site.swc_github}}/workshop-template/wiki/Configuration-Problems-and-Solutions">Configuration Problems and Solutions wiki page</a>.
</p>


{% comment %}
These are the installation instructions for the tools used
during the workshop.
{% endcomment %}

<h2 id="setup-uom">Setup instructions specific to University of Manchester staff</h2>
<p>Further to the above setup instructions, we would like to provide you with some extra suggestions, specific to University of Manchester managed-desktop machines (i.e. your Windows 10 work laptop).</p>

  <h3>OpenRefine</h3>
  <ol>
    <li>If you do not have administrator rights, you can still install OpenRefine to your local hard drive (<b>‘This PC’ &gt; ‘OS (C:)’ &gt; ‘Work’</b>).</li>
    <li>OpenRefine will not work if you install it to a network drive such as your P: drive.</li>
    <li>Download the <a href="https://github.com/OpenRefine/OpenRefine/releases/download/3.4.1/openrefine-win-3.4.1.zip" target="_blank">Windows kit</a>, a file called ‘<b>openrefine-win-3.4.1.zip</b>’.</li>
    <li>Move the file from ‘Downloads’ to your local hard drive (<b>‘This PC’ &gt; ‘OS (C:)’ &gt;> ‘Work’</b>).</li>
    <li>Unzip the file: Right-click on the file, choose ‘<b>7-Zip</b>’ then ‘<b>Extract Here</b>’. </li>
    <li>Open the new folder ‘<b>openrefine-win-3.4.1</b>’ then double-click ‘<b>openrefine</b>’ with the blue gem icon.</li>
    <li>OpenRefine will run in the background, you must leave it open. Wait for a new tab to open automatically in your browser at <a href="http://127.0.0.1:3333">http://127.0.0.1:3333/</a>.</li>
    <li>If for some reason your computer does not have Java JRE, you can install that from the Software Center, or replace the file in step 3 with the <a href="https://github.com/OpenRefine/OpenRefine/releases/download/3.5-beta1/openrefine-win-with-java-3.5-beta1.zip" target="_blank">Windows kit with embedded Java</a>.</li>
  </ol>

  <h3>Git and Shell</h3>
  <ol>
    <li>For the Git and Shell lessons, we suggest you install ‘<b>Git 2.22.0</b>’ from the Software Center. It includes a program called Git Bash.</li>
    <li>Click on the Windows Start button then ‘<b>Software Center</b>’ should appear on the right. (It may also be on the desktop.)</li>
    <li>In the ‘<b>Applications</b>’ tab, go to the search box on the right and type ‘<b>git</b>’ then press Enter.</li>
    <li>Click on the result ‘<b>Git 2.22.0</b>’.</li>
    <li>Click the ‘<b>Install</b>’ button.</li>
    <li>When it has installed, go back to the Start menu and scroll to the ‘G’ section. In the ‘<b>Git</b>’ folder, click ‘<b>Git Bash</b>’.</li>
    <li>This is our command shell where we can type commands to interact with the files on our computer and with the GitHub server.</li>
    <li>(TBC) we will not be using the alternative software ‘<b>GitHub Desktop 2.5.4</b>’ in this workshop though we may mention it for your future use.</li>
  </ol>
