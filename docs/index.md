---
layout: post
image: /images/header.png
---


![A Wardley Map sketch that characterizes the main ideas about this audiobook version of Simon Wardley's book.](images/header.png)

Here you can download and listen to the (synthetically generated) audio version of [Simon Wardley](https://twitter.com/swardley)'s book ["Wardley Maps &ndash; Topographical intelligence in business"](https://medium.com/wardleymaps).

_If you want to find out more about this website (e. g. what headphones, housework and the constant desire to learn have to do with it), check out the [About](./about/) section. Plus: there is now also a [German version](https://feststelltaste.github.io/wardley-maps-hoerbuch/) of the book._

# Complete MP3 file

Here you can find one "big" MP3 file that contains the complete content of the book. 

**Female voice**  

* <b><a href="https://github.com/feststelltaste/wardley-maps-audiobook/releases/download/v1.1/Simon_Wardley_-_Wardley_Maps_-_Topographical_intelligence_in_business_v1.0-female.mp3">Simon Wardley: Wardley Maps - Topographical intelligence in business (301 MB)</a></b>

**Male voice** 

* <b><a href="https://github.com/feststelltaste/wardley-maps-audiobook/releases/download/v1.0/Simon_Wardley_-_Wardley_Maps_-_Topographical_intelligence_in_business_v1.0.mp3">Simon Wardley: Wardley Maps - Topographical intelligence in business (306 MB)</a></b>


# RSS feeds (beta)

There are two RSS feeds that you can manually import to your podcast app:

* <a href="rss_female.xml">Female version</a>
* <a href="rss.xml">Male version</a>

# Single MP3 files (1 file per section)

Here you can find one MP3 file for each section of the book for direct listening. You can download these files in one package:

**Female voice**  
* [**.tar.gz file (282 MB)**](https://github.com/feststelltaste/wardley-maps-audiobook/releases/download/v0.1-female/wardley-maps-audiobook-v0.1-female.tar.gz)
* [**.zip file (282 MB)**](https://github.com/feststelltaste/wardley-maps-audiobook/releases/download/v0.1-female/wardley-maps-audiobook-v0.1-female.zip)

**Male voice**  
* [**.tar.gz file (285 MB)**](https://github.com/feststelltaste/wardley-maps-audiobook/releases/download/v1.0/wardley-maps-audiobook-v1.0.tar.gz)
* [**.zip file (285 MB)**](https://github.com/feststelltaste/wardley-maps-audiobook/releases/download/v1.0/wardley-maps-audiobook-v1.0.zip)

I recommend to import those files into an audiobook app like [Voice (for Android)](https://play.google.com/store/apps/details?id=de.ph1b.audiobook&hl=de&gl=US). That's the way I'm listening to this audiobook.


Alternatively, you can directly listen to a section by clicking on a type of voice you prefer:

{% for txt in site.static_files %}
{% if txt.path contains 'texts' and txt.path contains '.txt' %}
{% assign filename = txt.path | split: "/" | last | replace: ".txt", ".mp3" | escape %}
{% assign title = txt.path | remove: "/texts/" | remove: ".txt" %}  
<div class="title" style="padding-bottom: 15px; line-height: 100%;">{{title}}<br/>
<small>
<a class="female" style="color:grey" href="https://wardley-maps-audiobook.s3.eu-central-1.amazonaws.com/mp3/amy/{{filename}}">female voice</a>
&nbsp;
<a class="male" style="color:grey"  href="https://wardley-maps-audiobook.s3.eu-central-1.amazonaws.com/mp3/brian/{{filename}}">male voice</a></small>

{% assign current_id = filename | slice: 0, 3 %}
{% for mp3_ben in site.static_files %}
{% if mp3_ben.path contains 'mp3/ben_mosior' and mp3_ben.path contains '.mp3' %}
{% if mp3_ben.path contains current_id  %}
{% assign ben_id = mp3_ben.path | slice: 0, 3 %}
&nbsp;
<small>
<a style="color:grey" href="{{ site.baseurl }}{{ mp3_ben.path | escape }}">Ben</a>
</small>
{% endif %}
{% endif %}
{% endfor %}

</div>
{% endif %}
{% endfor %}

# Human Narrators
In addition to the generated version of the audiobook by Amazon Polly, we're happy to have some voices from the Wardley Mapping community!


**Ben Mosior**  
Principal, <a href="https://hiredthought.com/">Hired Thought</a>

<table style="border:none;">
 <tr>
  <td style="border:none;" width="150px"><img src="mp3/ben_mosior/avatar.png" width="150" height="150"></td>
  <td style="border:none;" >
  Ben is your friendly methodology whisperer, developing innovative new methods into everyday tools and facilitating learning experiences for teams and communities. Through Hired Thought, Ben shares decision-making and sensemaking approaches oriented around collective knowledge creation. To democratize access to strategic thinking methods, he operates <a href="https://learnwardleymapping.com/">LearnWardleyMapping.com</a> and runs regular events to inform and uplift new practitioners. Ben's goal in work and life is to do his part to enable purposeful systems to flourish. He podcasts for joy and teaches for hope.
  </td>
 </tr>
</table>

# About the creator

**Markus Harrer**  
Senior Consultant, <a href="https://markusharrer.de/">INNOQ</a>

<table style="border:none;">
 <tr>
  <td style="border:none;" width="150px"><img src="images/markus_harrer.png" width="150" height="150"></td>
  <td style="border:none;" >
  Markus Harrer is a software engineer who’s passionate about improving the way we do software development. He specializes in the analysis of software data such as source code, application performance data or version control repositories to show the underlying problems of the symptoms we face on the surface. He is an active contributor in communities on the topics of Software Analytics, software architecture, software modernization and Wardley Maps. He is also an accredited trainer for the iSAQB Foundation Level and the Advanced Level Module IMPROVE.
  </td>
 </tr>
</table>

# More information

Here you can find some further awesome resources about Wardley Maps:
- <https://www.feststelltaste.de/top-5-learning-wardley-maps/> - Markus Harrer's recommendations for getting into the topic.
- <https://learnwardleymapping.com/> - An excellent introduction to Wardley Maps.
- <http://list.wardleymaps.com> - Useful Wardley mapping resources.


# Statistics
Here are some statistics from the underlying [GitHub repository](https://github.com/feststelltaste/wardley-maps-audiobook/):

[![Current Github Release](https://img.shields.io/github/v/release/feststelltaste/wardley-maps-audiobook)](https://github.com/feststelltaste/wardley-maps-audiobook/releases)
[![Github Release Downloads](https://img.shields.io/github/downloads/feststelltaste/wardley-maps-audiobook/total?label=downloads%20%28since%20Feb%2011%2C%202021%29)](https://tooomm.github.io/github-release-stats/?username=feststelltaste&repository=wardley-maps-audiobook)
[![GitHub Issues](https://img.shields.io/github/issues-raw/feststelltaste/wardley-maps-audiobook)](https://github.com/feststelltaste/wardley-maps-audiobook/issues)
[![Github Stars](https://img.shields.io/github/stars/feststelltaste/wardley-maps-audiobook?style=social)](https://github.com/feststelltaste/wardley-maps-audiobook/stargazers)

{% include open-embed.html %}
