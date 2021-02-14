---
layout: post
image: /images/header.png
---


![A Wardley Map sketch that characterizes the main ideas about this audiobook version of Simon Wardley's book.](images/header.png)

Here you can download and listen to the (synthetically generated) audio version of [Simon Wardley](https://twitter.com/swardley)'s book ["Wardley Maps &ndash; Topographical intelligence in business"](https://medium.com/wardleymaps).

_If you want to find out more about this website (e. g. what headphones, housework and the constant desire to learn have to do with it), check out the [About](./about/) section._

# Complete MP3 file

Here you can find one "big" MP3 file that contains the complete content of the book. 

**Female voice**  

* <b><a href="https://github.com/feststelltaste/wardley-maps-audiobook/releases/download/v0.1-female/Simon_Wardley_-_Wardley_Maps_-_Topographical_intelligence_in_business_v0.1-female.mp3">Simon Wardley: Wardley Maps - Topographical intelligence in business (301 MB)</a></b>

**Male voice** 

* <b><a href="https://github.com/feststelltaste/wardley-maps-audiobook/releases/download/v1.0/Simon_Wardley_-_Wardley_Maps_-_Topographical_intelligence_in_business_v1.0.mp3">Simon Wardley: Wardley Maps - Topographical intelligence in business (306 MB)</a></b>


# Single MP3 files (1 file per section)

Here you can find one MP3 file for each section of the book for direct listening. You can download these files in one package:

**Female voice**  
* [**.tar.gz file (282 MB)**](https://github.com/feststelltaste/wardley-maps-audiobook/releases/download/v0.1-female/wardley-maps-audiobook-v0.1-female.tar.gz)
* [**.zip file (282 MB)**](https://github.com/feststelltaste/wardley-maps-audiobook/releases/download/v0.1-female/wardley-maps-audiobook-v0.1-female.zip)

**Male voice**  
* [**.tar.gz file (285 MB)**](https://github.com/feststelltaste/wardley-maps-audiobook/releases/download/v1.0/wardley-maps-audiobook-v1.0.tar.gz)
* [**.zip file (285 MB)**](https://github.com/feststelltaste/wardley-maps-audiobook/releases/download/v1.0/wardley-maps-audiobook-v1.0.zip)

Or you can directly listen to a section by clicking on a type of voice you prefer:


{% for mp3 in site.static_files %}
{% if mp3.path contains 'mp3/brian' %}
{% assign filename = mp3.path | remove: "/mp3/brian/" | remove: ".mp3" %}
{% assign id = filename | split: "- " | last | replace: " ", "-" | downcase %}

<div style="padding-bottom: 15px; line-height: 100%;">
{{filename}}<br/>
<small>{% assign female_path = mp3.path | replace: "brian/", "amy/" %}
<a style="color:grey" href="{{ site.baseurl }}{{ female_path | escape }}">female voice</a>
&nbsp;
<a style="color:grey" href="{{ site.baseurl }}{{ mp3.path | escape }}">male voice</a></small>
</div>
{% endif %}
{% endfor %}

# More information

Here you can find some further awesome resources about Wardley Maps:
- <http://list.wardleymaps.com> - Useful Wardley mapping resources.
- <https://learnwardleymapping.com/> - An excellent introduction to Wardley Maps.

# Statistics
Here are some statistics from the underlying [GitHub repository](https://github.com/feststelltaste/wardley-maps-audiobook/):

[![Current Github Release](https://img.shields.io/github/v/release/feststelltaste/wardley-maps-audiobook)](https://github.com/feststelltaste/wardley-maps-audiobook/releases)
[![Github Release Downloads](https://img.shields.io/github/downloads/feststelltaste/wardley-maps-audiobook/total?label=downloads%20%28since%20Feb%2011%2C%202021%29)](https://tooomm.github.io/github-release-stats/?username=feststelltaste&repository=wardley-maps-audiobook)
[![GitHub Issues](https://img.shields.io/github/issues-raw/feststelltaste/wardley-maps-audiobook)](https://github.com/feststelltaste/wardley-maps-audiobook/issues)
[![Github Stars](https://img.shields.io/github/stars/feststelltaste/wardley-maps-audiobook?style=social)](https://github.com/feststelltaste/wardley-maps-audiobook/stargazers)


{% include open-embed.html %}
