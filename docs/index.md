---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: post
---
Here you can download the audio version of Simon Wardley's book "Wardley Maps - Topographical intelligence in business".

_Please note that this website and its content are currently in the alpha version. Take a look at the [issues on GitHub](https://github.com/feststelltaste/wardley-maps-audiobook/issues) and feel to provide feedback, too!_



# MP3 (full version)

{% for mp3 in site.static_files %}
{% if mp3.path contains 'mp3_full/' %}
<a href="{{ site.baseurl }}{{ mp3.path | escape }}">{{ mp3.path | remove: "/mp3_full/" | remove: ".mp3"}}</a> &nbsp;<a href="{{ site.baseurl }}{{ mp3.path | escape }}" download><i class="fa fa-download" aria-hidden="true"></i></a>

{% endif %}
{% endfor %}
# MP3s (1 file per section)

{% for mp3 in site.static_files %}
{% if mp3.path contains 'mp3/' %}
<a href="{{ site.baseurl }}{{ mp3.path | escape }}">{{ mp3.path | remove: "/mp3/" | remove: ".mp3"}}</a> &nbsp;<a href="{{ site.baseurl }}{{ mp3.path | escape }}" download><i class="fa fa-download" aria-hidden="true"></i></a>
{% endif %}
{% endfor %}

To download all MP3s, feel free to use this command on your Linux console:

```
wget -c -A '*.mp3' -r -l 1 -nd https://feststelltaste.github.io/mp3/
```

_Taken and adopted from <https://askubuntu.com/a/549368>._

{% include open-embed.html %}
