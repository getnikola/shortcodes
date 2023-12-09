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

## mastodon

**Author:** [Anke K (encarsia)](https://github.com/encarsia)

**Gist:**
  * Jinja2 template: [mastodon.tmpl](https://gist.github.com/encarsia/52728167ac7d2fe79caf480c291931ea)
  * Mako template: [mastodon.tmpl](https://gist.github.com/encarsia/da438431ca42781045b4d63ac1b9ea5c)

Template-based shortcode to embed Mastodon posts.

### Usage:
```
{{% mastodon status=https://instance.domain/@user/tootnr %}}
```
Optional parameters:
 - ``width`` (default: 600)
 - ``height`` (default: 333)
    
Example:
```
{{% mastodon status=https://instance.domain/@user/tootnr % width=300 height=600}} will show a 300x600 frame instead of the default 600x300
```

## series-button

**Author:** [Diego Carrasco G. (dacog)](https://github.com/dacog)

**Download**: [series_buttons.tmpl](https://github.com/dacog/nikola-shortcodes/blob/main/series_buttons.tmpl)

Template engine: Jinja2

Template-based shortcode to add buttons to other articles. It has, in my opinio, sensible defautls. I use it for previous/next buttons for an article series.

### Usage

```jinja2
{{% series_buttons previous_url="/previous-article" previous_text="Previous Article Title" next_url="/next-article" next_text="Next Article Title" %}}
```
**Important**

- If there is no previous_url, it does not render the previous button.
- If there is no next_url, it does not render the next button.
- If there is no previous_text, it defaults to "Previous in series".
- If there is no next_text, it defaults to "Next in series".

You can use CSS to customize the look-and-feel. The buttons have an id `#series-buttons`

## infobox

**Author:** [Diego Carrasco G. (dacog)](https://github.com/dacog)

**Download**: [infobox.tmpl](https://github.com/dacog/nikola-shortcodes/blob/main/infobox.tmpl)

Template engine: Jinja2

Template-based shortcode used to display an infobox with a specific type of content. 
There is also an _optional_ `disclaimer` shortcode to add a disclaimer to an infobox by adding a font-awesome info icon at the end of the infobox. Defaults to no disclaimer.

### Usage

```
{{% infobox type="book" text="This is a book infobox"  disclaimer="true" %}}
```

It supports the following font-awesome icons:

- book
- video
- audio
- link
- quote
- image
- sticky-note

## disclaimer

**Author:** [Diego Carrasco G. (dacog)](https://github.com/dacog)

**Download**: [disclaimer.tmpl](https://github.com/dacog/nikola-shortcodes/blob/main/disclaimer.tmpl)

A really small shortcode to add a disclaimer somewhere on the page.

### Usage

`{{% disclaimer %}}`