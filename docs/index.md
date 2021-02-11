---
layout: post
image: /images/header.png
---


![A Wardley Map sketch that characterizes the main ideas about this audiobook version of Simon Wardley's book.](images/header.png)

Here you can download and listen to the (synthetically generated) audio version of [Simon Wardley](https://twitter.com/swardley)'s book ["Wardley Maps &ndash; Topographical intelligence in business"](https://medium.com/wardleymaps).

_If you want to find out more about this website (e. g. what headphones, housework and the constant desire to learn have to do with it), check out the [About](./about/) section._

# MP3 (full version)

This is one "big" MP3 file that contains the complete content of the book. 

<a href="https://github.com/feststelltaste/temp-release-test/releases/download/v1.0/Simon_Wardley_-_Wardley_Maps_-_Topographical_intelligence_in_business_v1.0.mp3">Simon Wardley: Wardley Maps - Topographical intelligence in business (complete audiobook, 305 MB)</a>

# MP3s (1 file per section)

Here you can find one MP3 file for each section of the book. You can also download these files in one package as [.tar.gz file](https://github.com/feststelltaste/temp-release-test/releases/download/v1.0/wardley-maps-audiobook-v1.0.tar.gz) or [.zip file](https://github.com/feststelltaste/temp-release-test/releases/download/v1.0/wardley-maps-audiobook-v1.0.zip).


{% for mp3 in site.static_files %}
{% if mp3.path contains 'mp3/' %}
{% assign filename = mp3.path | remove: "/mp3/" | remove: ".mp3" %}
{% assign id = filename | split: "- " | last | replace: " ", "-" | downcase %}
<div style="padding-bottom: 10px">
<a href="#{{id | escape}}" name="{{id | escape}}"><i class="fa fa-link"></i></a>&nbsp;&nbsp;<a href="{{ site.baseurl }}{{ mp3.path | escape }}">{{filename}}</a>
</div>
{% endif %}
{% endfor %}


# More information

Here you can find some further awesome resources about Wardley Maps:
- <http://list.wardleymaps.com> - Useful Wardley mapping resources.
- <https://learnwardleymapping.com/> - Ben Mosior website for beginners.


{% include open-embed.html %}
