# Shortcodes for Nikola

Community-maintained shortcodes for Nikola are stored in this file. To **add your own**, send a pull request.

To **use a template-based shortcode**: save it to the `shortcodes/` directory of your Nikola site and follow the usage instructions.

## audio

**Author:** [Christopher Arndt (SpotlightKid)](https://github.com/SpotlightKid)  
[**Download audio.tmpl**](https://gist.github.com/SpotlightKid/70f3ccdfacd9cfb091941a91f349924f)

A Jinja2 template-based shortcode for Nikola to embed a HTML5 audio player and download links.

Usage:

    {{% audio src=http://example.com/my-track.mp3 %}}

Or:

    {{% audio src=http://example.com/my-track.mp3 formats=mp3,ogg %}}
    Sorry, your browser does not seem to support the HTML 5 audio element.
    {{% /audio %}}

The shortcode supports a few other parameters:

    {{% audio src=my-track.mp3 download="Datei herunterladen:" nocontrols=1 loop=1 autoplay=1 %}}

And:

    {{% audio src=http://example.com/my-track.mp3 nodownload=1 %}}

Boolean parameters must have a value to take effect, but it doesn't matter what the value is.
