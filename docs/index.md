---
layout: post
image: /images/header.png
---


![A Wardley Map sketch that characterizes the main ideas about this audiobook version of Simon Wardley's book.](images/header.png)

Here you can download and listen to the (synthetic generated) audio version of [Simon Wardley](https://twitter.com/swardley)'s book ["Wardley Maps &ndash; Topographical intelligence in business"](https://medium.com/wardleymaps).


# MP3 (full version)

<a href="https://www.feststelltaste.de/wp-content/uploads/share/Simon%20Wardley%20-%20Wardley%20Maps%20-%20Topographical%20intelligence%20in%20business%20%28complete%20audiobook%29.mp3">Simon Wardley: Wardley Maps - Topographical intelligence in business (complete audiobook, 305 MB)</a>

# MP3s (1 file per section)

{% for mp3 in site.static_files %}
{% if mp3.path contains 'mp3/' %}
<a href="{{ site.baseurl }}{{ mp3.path | escape }}">{{ mp3.path | remove: "/mp3/" | remove: ".mp3"}}</a> &nbsp;<a href="{{ site.baseurl }}{{ mp3.path | escape }}" download><i class="fa fa-download" aria-hidden="true"></i></a>
{% endif %}
{% endfor %}

To download all MP3s from this website, feel free to use this command on your Linux console:

```
wget -c -A '*.mp3' -r -l 1 -nd https://feststelltaste.github.io/wardley-maps-audiobook/
```
_Taken and adopted from <https://askubuntu.com/a/549368>._

# More information

Here you can find some awesome resources about Wardley Maps: <http://list.wardleymaps.com>


{% include open-embed.html %}
