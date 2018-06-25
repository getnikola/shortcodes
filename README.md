# Shortcodes for Nikola

Community-maintained [shortcodes] for Nikola are listed in this file. To **add
your own**, put it in a repository or a [Gist], add a link and description for
your shortcode to this file and send a pull request. Please use the existing
entries as a guideline for formatting your new entry. The [Extending Nikola]
manual describes how to implement shortcodes.

To **use a template-based shortcode**: save it to the `shortcodes/` directory
of your Nikola site and follow the usage instructions given by shortcode's
author.

[shortcodes]: https://getnikola.com/handbook.html#shortcodes
[gist]: https://gist.github.com/
[extending nikola]: https://getnikola.com/extending.html#shortcodes

## slides

**Author:** [Roberto Alsina (ralsina)](https://github.com/ralsina)
**Gist:** https://gist.github.com/ralsina/e02a7bd0e27255dfac522ca16de78fb3

Create a carousel containing the images from a gallery. Meant to be used in bootstrap4-based themes.

## audio

**Author:** [Christopher Arndt (SpotlightKid)](https://github.com/SpotlightKid)

**Download:** [audio.tmpl](https://gist.github.com/SpotlightKid/70f3ccdfacd9cfb091941a91f349924f)

A Jinja2 template-based shortcode for Nikola to embed a HTML5 audio player and
download links.

### Usage:

    {{% audio src=http://example.com/my-track.mp3 %}}

Or:

    {{% audio src=http://example.com/my-track.mp3 formats=mp3,ogg %}}
    Sorry, your browser does not seem to support the HTML 5 audio element.
    {{% /audio %}}

The shortcode supports a few other parameters:

    {{% audio src=my-track.mp3 download="Datei herunterladen:" nocontrols=1 loop=1 autoplay=1 %}}

And:

    {{% audio src=http://example.com/my-track.mp3 nodownload=1 %}}

Boolean parameters must have a value to take effect, but it doesn't matter what
the value is.
