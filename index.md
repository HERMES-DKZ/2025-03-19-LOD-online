---
layout: workshop      # DON'T CHANGE THIS.
# More detailed instructions (including how to fill these variables for an
# online workshop) are available at
# https://carpentries.github.io/workshop-template/customization/index.html
venue: "HERMES"        # brief name of the institution that hosts the workshop without address (e.g., "Euphoric State University")
address: "online"      # full street address of workshop (e.g., "Room A, 123 Forth Street, Blimingen, Euphoria"), videoconferencing URL, or 'online'
country: "de"      # lowercase two-letter ISO country code such as "fr" (see https://en.wikipedia.org/wiki/ISO_3166-1#Current_codes) for the institution that hosts the workshop
language: "de"     # lowercase two-letter ISO language code such as "fr" (see https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) for the workshop
latitude: "45"        # decimal latitude of workshop venue (use https://www.latlong.net/)
longitude: "-1"       # decimal longitude of the workshop venue (use https://www.latlong.net)
humandate: "19.3.2025"    # human-readable dates for the workshop (e.g., "Feb 17-18, 2020")
humantime: "9:00 - 17:00 Uhr"    # human-readable times for the workshop e.g., "9:00 am - 4:30 pm CEST (7:00 am - 2:30 pm UTC)"
startdate: 2025-03-19      # machine-readable start date for the workshop in YYYY-MM-DD format like 2015-01-01
enddate: 2025-03-19        # machine-readable end date for the workshop in YYYY-MM-DD format like 2015-01-02
instructor: ["Julia Tolksdorf", "Robert Zwick"] # boxed, comma-separated list of instructors' names as strings, like ["Kay McNulty", "Betty Jennings", "Betty Snyder"]
helper: ["Judit Garzón Rodríguez", "Marlon-Benedikt George"]     # boxed, comma-separated list of helpers' names, like ["Marlyn Wescoff", "Fran Bilas", "Ruth Lichterman"]
email: ["julia.tolksdorf@hs-mainz.de","robert.zwick@hs-mainz.de"]    # boxed, comma-separated list of contact email addresses for the host, lead instructor, or whoever else is handling questions, like ["marlyn.wescoff@example.org", "fran.bilas@example.org", "ruth.lichterman@example.org"]
collaborative_notes:  https://pad.carpentries.org/2025-03-19-LOD-online # optional: URL for the workshop collaborative notes, e.g. an Etherpad or Google Docs document (e.g., https://pad.carpentries.org/2015-01-01-euphoria)
eventbrite:           # optional: alphanumeric key for Eventbrite registration, e.g., "1234567890AB" (if Eventbrite is being used)
what3words:           # optional: what3words (https://what3words.com) address of the workshop venue, without leading slashes e.g. "globe.lessening.computers"
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
{% unless site.curriculum == "dc-astronomy" or site.curriculum == "dc-ecology" or site.curriculum == "dc-genomics" or site.curriculum == "dc-geospatial" or site.curriculum == "dc-image" or site.curriculum == "dc-socsci" %}
<div class="alert alert-warning">
It looks like you are setting up a website for a Data Carpentry curriculum but you haven't specified the curriculum type in the <code>_config.yml</code> file (current value in <code>_config.yml</code>: "<strong>{{ site.curriculum }}</strong>", possible values: <code>dc-image</code>, <code>dc-astronomy</code>, <code>dc-ecology</code>, <code>dc-genomics</code>, <code>dc-socsci</code>, or <code>dc-geospatial</code>). After editing this file, you need to run <code>make serve</code> again to see the changes reflected.
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

{% comment %}
EVENTBRITE

This block includes the Eventbrite registration widget if
'eventbrite' has been set in the header.  You can delete it if you
are not using Eventbrite, or leave it in, since it will not be
displayed if the 'eventbrite' field in the header is not set.
{% endcomment %}
{% if page.eventbrite %}
<strong>Some adblockers block the registration window. If you do not see the
  registration box below, please check your adblocker settings.</strong>
<div id="eventbrite-widget-container"></div>
<script src="https://www.eventbrite.com/static/widgets/eb_widgets.js"></script>
<script type="text/javascript">
    window.EBWidgets.createWidget({
        // Required
        widgetType: 'checkout',
        eventId: {{page.eventbrite}},
        iframeContainerId: 'eventbrite-widget-container',
    });
</script>
{% endif %}


<h2 id="general">Allgemeine Informationen</h2>

{% comment %}
INTRODUCTION

Edit the general explanatory paragraph below if you want to change
the pitch.
{% endcomment %}

<p>
<strong><a href="https://carpentries.org">Das Carpentries</a></strong>-Projekt umfasst die <a
href="{{site.swc_site}}">Software Carpentry</a>, <a href="{{site.dc_site}}">Data Carpentry</a>, und
<a href="{{site.lc_site}}">Library Carpentry</a> Communities von Instructorn, Trainern, Maintainern,
Helpern und Supportern, die sich zum Ziel gesetzt haben, Forschenden Grundkenntnisse in Informatik und Datenwissenschaft zu vermitteln.
<p align="center">
  <em>
  <strong>Möchtest Du mehr erfahren und mit The Carpentries verbunden bleiben?</strong> Carpentries Clippings ist der zweiwöchentlich erscheinende Newsletter von The Carpentries, in dem wir Neuigkeiten aus der Community, Stellenausschreibungen und vieles mehr mitteilen.
Melde Dich an, um künftige Ausgaben zu erhalten und unser vollständiges Archiv zu lesen: <a href="https://carpentries.org/newsletter/">https://carpentries.org/newsletter/</a>
  </em>
</p>
{% if site.carpentry == "swc" %}
{% include swc/intro.html %}
{% elsif site.carpentry == "dc" %}
{% include dc/intro.html %}
{% elsif site.carpentry == "lc" %}
{% include lc/intro.html %}
{% endif %}

{% if site.pilot %}


<p>Dies ist ein Pilot-Workshop, in dem eine Lektion getestet wird, die noch in der Entwicklung ist. Die Autoren der Lektion freuen sich über jedes Feedback zum Inhalt der Lektion und über Vorschläge, wie sie weiter verbessert werden kann.</p>

{% endif %}

{% comment %}
AUDIENCE

Explain who your audience is.  (In particular, tell readers if the
workshop is only open to people from a particular institution.
{% endcomment %}
{% if site.carpentry == "swc" %}
{% include swc/who.html %}
{% elsif site.carpentry == "dc" %}
{% include dc/who.html %}
{% elsif site.carpentry == "lc" %}
{% include lc/who.html %}
{% endif %}

{% comment %}
LOCATION

This block displays the address and links to maps showing directions
if the latitude and longitude of the workshop have been set.  You
can use https://www.latlong.net/ to find the lat/long of an
address.
{% endcomment %}
{% assign begin_address = page.address | slice: 0, 4 | downcase  %}
{% if page.address == "online" %}
{% assign online = "true_private" %}
{% elsif begin_address contains "http" %}
{% assign online = "true_public" %}
{% else %}
{% assign online = "false" %}
{% endif %}
{% if page.latitude and page.longitude and online == "false" %}
<p id="where">
  <strong>Where:</strong>
  {{page.address}}.
  Get directions with
  <a href="//www.openstreetmap.org/?mlat={{page.latitude}}&mlon={{page.longitude}}&zoom=16">OpenStreetMap</a>
  or
  <a href="//maps.google.com/maps?q={{page.latitude}},{{page.longitude}}">Google Maps</a>.
  {% if page.what3words %}
    What3Words location:
    <a href="https://what3words.com/{{page.what3words}}">///{{page.what3words}}</a>.
  {%endif %}
</p>
{% elsif online == "true_public" %}
<p id="where">
  <strong>Where:</strong>
  online at <a href="{{page.address}}">{{page.address}}</a>.
  If you need a password or other information to access the training,
  the instructor will pass it on to you before the workshop.
</p>
{% elsif online == "true_private" %}
<p id="where">
  <strong>Wo:</strong> Dieser Workshop findet online statt.
  Die Workshop-Hosts werden Dir die Informationen geben, die du für die Teilnahme an diesem Treffen benötigst.
</p>
{% endif %}

{% comment %}
DATE

This block displays the date and links to Google Calendar.
{% endcomment %}
{% if page.humandate %}
<p id="when">
  <strong>Wann:</strong>
  {{page.humandate}}; {{page.humantime}}
  {% include workshop_calendar.html %}
</p>
{% endif %}

{% comment %}
SPECIAL REQUIREMENTS

Modify the block below if there are any special requirements.
{% endcomment %}
<p id="requirements">
  <strong>Anforderungen:</strong>
  {% if online == "false" %}
    Die Teilnehmer:innen müssen einen Laptop mit einem
    Mac-, Linux- oder Windows-Betriebssystem (kein Tablet, Chromebook usw.) mitbringen, auf dem sie über administrative Rechte verfügen.
  {% else %}
    Die Teilnehmer:innen müssen einen Laptop mit einem
    Mac-, Linux- oder Windows-Betriebssystem (kein Tablet, Chromebook usw.) mitbringen, auf dem sie über administrative Rechte verfügen.
  {% endif %}
   Sie sollten zudem einige spezielle Softwarepakete installiert haben (siehe <a href="#setup">unten</a>).
</p>

{% comment %}
ACCESSIBILITY

Modify the block below if there are any barriers to accessibility or
special instructions.
{% endcomment %}
<p id="accessibility">
  <strong>Zugänglichkeit:</strong>
  Wir sind bestrebt, diesen Workshop für alle zugänglich zu machen. 
{% if online == "false" %}
  The workshop organizers have checked that:
<p>
  <ul>
    <li>The room is wheelchair / scooter accessible.</li>
    <li>Accessible restrooms are available.</li>
  </ul>
{% endif %}
</p>
<p>Wir sind bestrebt, ein positives und zugängliches Lernumfeld für alle zu schaffen. 
  Wir verlangen von den Teilnehmer:innen keine Unterlagen über Behinderungen oder die Offenlegung unnötiger persönlicher Informationen. 
  Wir möchten jedoch dazu beitragen, dass alle Teilnehmer:innen ein integratives, zugängliches Erlebnis haben. 
  Wir ermutigen Dich, uns alle Informationen mitzuteilen, die hilfreich sind, um Deine Carpentries-Erfahrung zugänglich zu machen.
  Um eine Hilfsmittel für diesen Workshop zu beantragen, fülle bitte das  
  <a href="https://carpentries.typeform.com/to/B2OSYaD0"> Formular zur Beantragung</a> aus.
  Wenn Du Fragen hast oder Hilfe beim Ausfüllen des Formulars benötigst, schreibe uns bitte eine <a href="mailto:team@carpentries.org">E-Mail</a> 
  an uns.
</p>
<p>
  <a href="https://glosario.carpentries.org/">Glosario</a> ist ein mehrsprachiges Glossar für Begriffe aus dem Bereich Informatik und Datenwissenschaft. Das Glossar hilft Lernenden, die an Workshops teilnehmen und unsere Lektionen nutzen, den Sinn von Computer- und Programmierjargon in englischer Sprache zu verstehen, indem es in ihrer Muttersprache angeboten wird. Die Übersetzung von Begriffen aus der Datenwissenschaft ist auch ein Lehrmittel für Carpentries-Lehrer, um Barrieren für ihre Lernenden abzubauen.
</p>

{% comment %}
CONTACT EMAIL ADDRESS

Display the contact email address set in the configuration file.
{% endcomment %}
<p id="contact">
  <strong>Kontakt:</strong>
  Schreiben Sie an
  {% if page.email %}
  {% for email in page.email %}
  {% if forloop.last and page.email.size > 1 %}
  or
  {% else %}
  {% unless forloop.first %}
  ,
  {% endunless %}
  {% endif %}
  <a href='mailto:{{email}}'>{{email}}</a>
  {% endfor %}
  {% else %}
  to-be-announced
  {% endif %}
  für mehr Informationen.
</p>


<p id="roles">
  <strong>Rollen:</strong>
  Um mehr über die Rollen beim Workshop zu erfahren (wer was macht),
  lese <a href="https://carpentries.org/workshop_faq/#what-are-the-roles-of-everyone-participating-in-a-workshop">unsere Workshop-FAQs</a>.
</p>

{% comment %}
WHO CAN ATTEND?

If you would like to specify who can attend the workshop,
you can use the section below.

Move the 'endcomment' tag above the beginning of the following
<p> tag to make this section visible.

Edit the text to match who can attend the workshop. For instance:
- This workshop is open to affiliates to ABC university.
- This workshop is open to the public.
- If you are interested in attending this workshop, contact me@example.com
  for more information

<p id="who-can-attend">
    <strong>Who can attend?:</strong>
    This workshop is open to ....
</p>
{% endcomment %}

<hr/>

{% comment%}
CODE OF CONDUCT
{% endcomment %}
<h2 id="code-of-conduct">Code of Conduct</h2>

<p>
Jeder, der an den Aktivitäten von The Carpentries teilnimmt, ist verpflichtet, den <a href="https://docs.carpentries.org/topic_folders/policies/code-of-conduct.html">Verhaltenskodex</a> einzuhalten. In diesem Dokument wird auch beschrieben, wie ein Vorfall zu melden ist.
</p>

<p class="text-center">
  <a href="https://goo.gl/forms/KoUfO53Za3apOuOK2">
    <button type="button" class="btn btn-info">Einen Code of Conduct Vorfall melden</button>
  </a>
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
<h2 id="collaborative_notes">Kollaboratives Pad</h2>

<p>
Wir werden dieses <a href="{{ page.collaborative_notes }}">kollaborative Dokument</a> zum Chatten, für Notizen und zum Austausch von URLs und Codeblöcken verwenden.
</p>
<hr/>
{% endif %}


{% comment %}
SURVEYS - DO NOT EDIT SURVEY LINKS
{% endcomment %}
<h2 id="surveys">Umfragen</h2>
<p>Da wir in diesem Pilot-Workshop eine neue Lektion mit frischen Inhalten testen, sind wir auf Dein ausführliches Feedback angewiesen. Deine Rückmeldung hilft uns, die Lektion kontinuierlich zu verbessern. Bitte nimm Dir nach dem Workshop einen Moment Zeit, um die Umfrage auszufüllen.</p>
{% if site.carpentry == "incubator" %}
<p>Post-Workshop Umfrage (Link folgt)</p>
{% elsif site.incubator_pre_survey or site.incubator_post_survey %}
<div class="alert alert-danger">
WARNING: you have defined custom pre- and/or post-survey links for
a workshop not configured for The Carpentries Incubator
(the value of `curriculum` is not set to `incubator` in `_config.yml`).
Please comment out the `incubator_pre_survey` and `incubator_post_survey` fields
in `_config.yml` or, if this workshop is teaching a lesson in the Incubator,
change the value of `carpentry` to `incubator`.
</div>
{% else %}
<p><a href="{{ site.pre_survey }}{{ site.github.project_title }}">Pre-workshop Survey</a></p>
<p><a href="{{ site.post_survey }}{{ site.github.project_title }}">Post-workshop Survey</a></p>
{% endif %}

<hr/>


{% comment %}
SCHEDULE

Show the workshop's schedule.

Small changes to the schedule can be made by modifying the
`schedule.html` found in the `_includes` folder for your
workshop type (`swc`, `lc`, or `dc`). Edit the items and
times in the table to match your plans. You may also want to
change 'Day 1' and 'Day 2' to be actual dates or days of the
week.

For larger changes, a blank template for a 4-day workshop
(useful for online teaching for instance) can be found in
`_includes/custom-schedule.html`. Add the times, and what
you will be teaching to this file. You may also want to add
rows to the table if you wish to break down the schedule
further. To use this custom schedule here, replace the block
of code below the Schedule `<h2>` header below with
`{% include custom-schedule.html %}`.
{% endcomment %}

<h2 id="schedule">Zeitplan</h2>

{% if site.carpentry == "swc" %}
{% include swc/schedule.html %}
{% elsif site.carpentry == "dc" %}
{% include dc/schedule.html %}
{% elsif site.carpentry == "lc" %}
{% include lc/schedule.html %}
{% elsif site.carpentry == "incubator" %}

{% endif %}

{% comment %}
Edit/replace the text above if you want to include a schedule table.
See the contents of the _includes/custom-schedule.html file for an example of
how one of these schedule tables is constructed.
{% endcomment %}

{% if site.pilot %}
 <p>Dieser Workshop befindet sich in der Erprobungsphase und ein genauer Zeitplan muss noch festgelegt werden.
 Der Workshop wird regelmäßige Pausen beinhalten. <a href="mailto:{{page.email}}">Bitte wende Dich an die Organisatoren des Workshops</a>, wenn Du weitere Informationen über den geplanten Zeitplan wünschst.</p>

 <div class="row">        <!-- first two days -->
  <div class="col-md-6"> <!-- left column -->
    <table class="table table-striped">
      <tr>               <!-- row 1   -->
        <td>Bevor es los geht</td>
        <td><a href="{{ site.pre_survey }}{{ site.github.project_title }}" target="_blank">Pre-workshop survey</a></td>
      </tr>
      <tr>               <!-- row 2   -->
        <td>9:00</td>        <!-- time    -->
        <td>Vorstellung und Intro</td>        <!-- content -->
      </tr>
      <tr>               <!-- row 3   -->
        <td>9:30</td>        <!-- time    -->
        <td>Block 1</td>        <!-- content -->
      </tr>
            <tr>               <!-- row 2   -->
        <td>12:30</td>        <!-- time    -->
        <td>Mittagspause</td>        <!-- content -->
      </tr>
      <tr>               <!-- row 3   -->
        <td>13:30</td>        <!-- time    -->
        <td>Block 2</td>        <!-- content -->
      </tr>
            <tr>               <!-- row 3   -->
        <td>16:30</td>        <!-- time    -->
        <td>Recap & Feedback</td>        <!-- content -->
      </tr>
    </table>
  </div>
</div>

{% endif %}

<hr/>


{% comment %}
SETUP

Delete irrelevant sections from the setup instructions.  Each
section is inside a 'div' without any classes to make the beginning
and end easier to find.

This is the other place where people frequently make mistakes, so
please preview your site before committing, and make sure to run
'tools/check' as well.
{% endcomment %}

<h2 id="setup">Setup</h2>

<p>
  Zur Teilnahme am
  {% if site.carpentry == "swc" %}
  Software Carpentry
  {% elsif site.carpentry == "dc" %}
  Data Carpentry
  {% elsif site.carpentry == "lc" %}
  Library Carpentry
  {% endif %}
  Workshop,
  benötigst Du Zugang zu der unten beschriebenen Software.
  Darüber hinaus benötist Du einen aktuellen Webbrowser.
</p>
<p>
  Wir führen eine Liste mit häufigen Problemen, die während der Installation auftreten, als Referenz für Instructor
  die nützlich sein können auf der
  <a href = "{{site.swc_github}}/workshop-template/wiki/Configuration-Problems-and-Solutions">Konfigurationsprobleme und Lösungen Wiki-Seite</a>.
</p>

{% comment %}
For online workshops, the section below provides:
- installation instructions for the Zoom client
- recommendations for setting up Learners' workspace so they can follow along
  the instructions and the videoconferencing

If you do not use Zoom for your online workshop, edit the file
`_includes/install_instructions/videoconferencing.html`
to include the relevant installation instructions.
{% endcomment %}
{% if online != "false" %}
{% include install_instructions/videoconferencing.html %}
{% endif %}

{% comment %}
These are the installation instructions for the tools used
during the workshop.
{% endcomment %}

{% if site.carpentry == "swc" %}
{% include swc/setup.html %}
{% elsif site.carpentry == "dc" %}
{% include dc/setup.html %}
{% elsif site.carpentry == "lc" %}
{% include lc/setup.html %}
{% elsif site.carpentry == "incubator" %}
{% include install_instructions/openrefine.html %}

{% endif %}
