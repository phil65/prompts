└── docs
    └── presentations
        ├── _columns-reveal.md
        ├── _columns.md
        ├── _creating-slides-reveal.md
        ├── _creating-slides.md
        ├── _incremental-lists-reveal.md
        ├── _incremental-lists.md
        ├── _incremental-pause-reveal.md
        ├── _incremental-pause.md
        ├── _speaker-notes.md
        ├── beamer.qmd
        ├── index.qmd
        ├── powerpoint.qmd
        └── revealjs
            ├── _background-video.md
            ├── _callout-auto-stretch-scrollable.qmd
            ├── _theme-basics.md
            ├── advanced.qmd
            ├── demo
                ├── actors.js
                ├── demo.pdf
                ├── images
                │   ├── beige.png
                │   ├── jupyter-edit.png
                │   ├── jupyter-preview.png
                │   ├── milky-way.jpeg
                │   ├── moon.png
                │   ├── overview-mode.png
                │   ├── presentation-chalkboard.png
                │   ├── presentation-menu.png
                │   ├── presentation-notes-canvas.png
                │   ├── quarto.png
                │   ├── rstudio.png
                │   ├── serif.png
                │   ├── sky.png
                │   └── speaker-view.png
                ├── index.qmd
                ├── mini
                │   ├── README.md
                │   ├── _metadata.yml
                │   ├── absolute.qmd
                │   ├── auto-animate-code.qmd
                │   ├── auto-animate-movement.qmd
                │   ├── auto-animate-stack.qmd
                │   ├── auto-animate.qmd
                │   ├── custom-blur.css
                │   ├── fragments-custom.qmd
                │   ├── fragments-nested.qmd
                │   ├── fragments.qmd
                │   ├── images
                │   │   ├── kitten-300-200.jpeg
                │   │   ├── kitten-300-300.jpeg
                │   │   ├── kitten-300-450.jpeg
                │   │   ├── kitten-350-300.jpeg
                │   │   ├── kitten-375-300.jpeg
                │   │   ├── kitten-400-350.jpeg
                │   │   ├── kitten-400-400.jpeg
                │   │   ├── kitten-450-200.jpeg
                │   │   ├── kitten-450-250.jpeg
                │   │   ├── kitten-450-300.jpeg
                │   │   └── kitten-450-350.jpeg
                │   ├── stack.qmd
                │   └── zoom.qmd
                └── styles.css
            ├── examples
                ├── _metadata.yml
                ├── _theme-dark.qmd
                ├── background-color.qmd
                ├── background-gradient.qmd
                ├── background-no-title.qmd
                ├── code-echo.qmd
                ├── columns.qmd
                ├── creating-slides-1.qmd
                ├── creating-slides-2.qmd
                ├── creating-slides-3.qmd
                ├── executable-code-figure-size.qmd
                ├── footer-and-logo.qmd
                ├── image-background.qmd
                ├── incremental-lists-1.qmd
                ├── incremental-lists-2.qmd
                ├── incremental-lists-3.qmd
                ├── incremental-pause.qmd
                ├── index.qmd
                ├── line-highlighting-1.qmd
                ├── line-highlighting-2.qmd
                ├── line-highlighting-3.qmd
                ├── line-highlighting-4.qmd
                ├── no-footer-on-a-slide.qmd
                ├── per-slide-footer.qmd
                ├── scrollable-and-smaller.qmd
                ├── scrollable.qmd
                ├── slide-with-speaker-notes.qmd
                ├── smaller.qmd
                └── tabset.qmd
            ├── images
                ├── canvas-icon.png
                ├── chalkboard-icon.png
                ├── chalkboard.png
                ├── drawing-canvas.png
                ├── footnote.png
                ├── line-highlight-discontinuous.png
                ├── line-highlight.png
                ├── matplotlib.png
                ├── navigation-menu-button.png
                ├── navigation-menu-icon.png
                ├── navigation-menu-open.png
                ├── overview-mode.png
                ├── print-to-pdf.png
                ├── reveal.js-vertical-slides.gif
                └── speaker-view.png
            ├── index.qmd
            ├── presenting.qmd
            └── themes.qmd


/docs/presentations/_columns-reveal.md:
--------------------------------------------------------------------------------
## Multiple Columns

To put material in side by side columns, you can use a native div container with class `.columns`, containing two or more div containers with class `.column` and a `width` attribute:

```{.markdown code-preview="examples/columns.qmd"}
:::: {.columns}

::: {.column width="40%"}
Left column
:::

::: {.column width="60%"}
Right column
:::

::::
```



--------------------------------------------------------------------------------
/docs/presentations/_columns.md:
--------------------------------------------------------------------------------
## Multiple Columns

To put material in side by side columns, you can use a native div container with class `.columns`, containing two or more div containers with class `.column`[ and a `width` attribute]{.content-visible unless-meta="is_pptx"}:

::: {.content-visible unless-meta="is_pptx"}
``` markdown
:::: {.columns}

::: {.column width="40%"}
contents...
:::

::: {.column width="60%"}
contents...
:::

::::
```
:::


::: {.content-hidden unless-meta="is_pptx"}
``` markdown
:::: {.columns}

::: {.column}
contents...
:::

::: {.column}
contents...
:::

::::
```

:::


--------------------------------------------------------------------------------
/docs/presentations/_creating-slides-reveal.md:
--------------------------------------------------------------------------------
## Creating Slides {#creating-slides}

In markdown, slides are delineated using headings. For example, here is a simple slide show with two slides (each defined with a level 2 heading (`##`):

``` {.markdown code-preview="examples/creating-slides-1.qmd"}
---
title: "Habits"
author: "John Doe"
format: {{< meta slide-format >}}
---

## Getting up

- Turn off alarm
- Get out of bed

## Going to sleep

- Get in bed
- Count sheep
```

You can also divide slide shows into sections with title slides using a level 1 heading (`#`). For example:

``` {.markdown code-preview="examples/creating-slides-2.qmd"}
---
title: "Habits"
author: "John Doe"
format: {{< meta slide-format >}}
---

# In the morning

## Getting up

- Turn off alarm
- Get out of bed

## Breakfast

- Eat eggs
- Drink coffee

# In the evening

## Dinner

- Eat spaghetti
- Drink wine

## Going to sleep

- Get in bed
- Count sheep
```

Finally, you can also delineate slides using horizontal rules (for example, if you have a slide without a title):

``` {.markdown code-preview="examples/creating-slides-3.qmd"}
---
title: "Habits"
author: "John Doe"
format: {{< meta slide-format >}}
---

- Turn off alarm
- Get out of bed

---

- Get in bed
- Count sheep
```

The examples above all use level 2 headings for slides and level 1 headings for sections/title slides. You can customize this using the `slide-level` option (See the Pandoc documentation on [structuring the slide show](https://pandoc.org/MANUAL.html#structuring-the-slide-show) for additional details.

### Title Slide

You'll notice in the above examples that a title slide is automatically created based on the `title` and `author` provided in the document YAML options. However, sometimes you don't want an explicit title slide (e.g. if your first slide consists entirely of a background image). It's perfectly valid to create a presentation without a title slide, just exclude the `title` and `author` options:

``` markdown
---
format: {{< meta slide-format >}}
---

## Getting up

- Turn off alarm
- Get out of bed

## Going to sleep

- Get in bed
- Count sheep
```



--------------------------------------------------------------------------------
/docs/presentations/_creating-slides.md:
--------------------------------------------------------------------------------
## Creating Slides {#creating-slides}

In markdown, slides are delineated using headings. For example, here is a simple slide show with two slides (each defined with a level 2 heading (`##`)):

``` markdown
---
title: "Habits"
author: "John Doe"
format: {{< meta slide-format >}}
---

## Getting up

- Turn off alarm
- Get out of bed

## Going to sleep

- Get in bed
- Count sheep
```

You can also divide slide shows into sections with title slides using a level 1 heading (`#`). For example:


``` markdown
---
title: "Habits"
author: "John Doe"
format: {{< meta slide-format >}}
---

# In the morning

## Getting up

- Turn off alarm
- Get out of bed

## Breakfast

- Eat eggs
- Drink coffee

# In the evening

## Dinner

- Eat spaghetti
- Drink wine

## Going to sleep

- Get in bed
- Count sheep
```

Finally, you can also delineate slides using horizontal rules (for example, if you have a slide without a title):

``` markdown
---
title: "Habits"
author: "John Doe"
format: {{< meta slide-format >}}
---

- Turn off alarm
- Get out of bed

---

- Get in bed
- Count sheep

```

The examples above all use level 2 headings for slides and level 1 headings for sections/title slides. You can customize this using the `slide-level` option (See the Pandoc documentation on [structuring the slide show](https://pandoc.org/MANUAL.html#structuring-the-slide-show) for additional details).



--------------------------------------------------------------------------------
/docs/presentations/_incremental-lists-reveal.md:
--------------------------------------------------------------------------------
## Incremental Lists

By default number and bullet lists within slides are displayed all at once. You can override this globally using the `incremental` option. For example:

```{.yaml code-preview="examples/incremental-lists-1.qmd"}
title: "My Presentation"
format:
  {{< meta slide-format >}}:
    incremental: true   
```

You can also explicitly make any list incremental or non-incremental by surrounding it in a div with an explicit class that determines the mode. To make a list incremental do this:

```{.markdown code-preview="examples/incremental-lists-2.qmd"}
::: {.incremental}
- Eat spaghetti
- Drink wine
:::
```

To make a list non-incremental do this:

```{.markdown code-preview="examples/incremental-lists-3.qmd"}
::: {.nonincremental}
- Eat spaghetti
- Drink wine
:::
```



--------------------------------------------------------------------------------
/docs/presentations/_incremental-lists.md:
--------------------------------------------------------------------------------


## Incremental Lists

By default number and bullet lists within slides are displayed all at once. You can override this globally using the `incremental` option. For example:

``` yaml
title: "My Presentation"
format:
  {{< meta slide-format >}}:
    incremental: true   
```

You can also explicitly make any list incremental or non-incremental by surrounding it in a div with an explicit class that determines the mode. To make a list incremental do this:

``` markdown
::: {.incremental}

- Eat spaghetti
- Drink wine

:::
```

To make a list non-incremental do this:

``` markdown
::: {.nonincremental}

- Eat spaghetti
- Drink wine

:::
```



--------------------------------------------------------------------------------
/docs/presentations/_incremental-pause-reveal.md:
--------------------------------------------------------------------------------
You can also insert a pause within a slide (keeping the content after the pause hidden) by inserting three dots separated by spaces:

```{.markdown code-preview="examples/incremental-pause.qmd"}
## Slide with a pause

content before the pause

. . .

content after the pause
```

Note this only works below headings that are creating slides (see [Creating slides](#creating-slides)).


--------------------------------------------------------------------------------
/docs/presentations/_incremental-pause.md:
--------------------------------------------------------------------------------
You can also insert a pause within a slide (keeping the content after the pause hidden) by inserting three dots separated by spaces:

``` markdown
## Slide with a pause

content before the pause

. . .

content after the pause
```

Note this only works below headings that are creating slides (see [Creating slides](#creating-slides)).


--------------------------------------------------------------------------------
/docs/presentations/_speaker-notes.md:
--------------------------------------------------------------------------------
## Speaker Notes

You can add speaker notes to a slide using a div with class `.notes`. For example:

```{.markdown}
## Slide with speaker notes

Slide content

::: {.notes}
Speaker notes go here.
:::
```




--------------------------------------------------------------------------------
/docs/presentations/beamer.qmd:
--------------------------------------------------------------------------------
---
title: "Beamer"
slide-format: beamer
---

## Overview

You can create [Beamer](https://ctan.org/pkg/beamer) (LaTeX/PDF) presentations using the `beamer` format. Beamer presentations support core presentation features like incremental content and 2-column layouts, and also provide facilities for customizing column layout, specifying frame attributes, and using Beamer themes.

By default, the Beamer format has `echo: false` and `warning: false`. As a result, executable code cells in standard Beamer documents won't show their source or warnings generated. As with other options, you can override this behavior in the document metadata or individually in each executable cell.

See the Beamer [format reference](/docs/reference/formats/presentations/beamer.qmd) for a complete list of all options available for Beamer output.

{{< include _creating-slides.md >}}

In Beamer, headings below `slide-level` will place content inside a `block` environment:

``` markdown
---
title: "Habits"
author: "John Doe"
format: 
  beamer:
    slide-level: 2
---

## Slide

### Simple block

Content
```

Add the `.alert` or `.example` class to place content inside an `alertblock` or `exampleblock` environment respectively:

``` markdown
---
title: "Habits"
author: "John Doe"
format: 
  beamer:
    slide-level: 2
---

## Slide

### Alert block {.alert}

Content

### Example block {.example}

Content
```

{{< include _incremental-lists.md >}}

{{< include _incremental-pause.md >}}

{{< include _columns.md >}}

The div containers with classes `columns` and `column` can optionally have an `align` attribute. The class `columns` can optionally have a `totalwidth` attribute or an `onlytextwidth` class.

``` markdown
:::: {.columns align=center totalwidth=8em}

::: {.column width="40%"}
contents...
:::

::: {.column width="60%" align=bottom}
contents...
:::

:::: 
```

The `align` attributes on `columns` and `column` can be used with the values `top`, `top-baseline`, `center` and `bottom` to vertically align the columns. It defaults to `top` in `columns`.

The `totalwidth` attribute limits the width of the columns to the given value.

``` markdown
::::  {.columns align=top .onlytextwidth}

::: {.column width="40%" align=center}
contents...
:::

::: {.column width="60%"}
contents...
:::

:::: 
```

The class `onlytextwidth` sets the `totalwidth` to `\textwidth`.

See Section 12.7 of the [Beamer User's Guide](http://mirrors.ctan.org/macros/latex/contrib/beamer/doc/beameruserguide.pdf) for more details.

## Beamer Options

Set additional options to change the appearance of PDF slides using `beamer`:

``` yaml
---
title: "Presentation"
format: 
  beamer: 
    aspectratio: 32
    navigation: horizontal
    theme: AnnArbor
    colortheme: lily
---
```

The options available are:

| Option | Description |
|------------------------|------------------------------------------------|
| `aspectratio` | Slide aspect ratio: `43` for 4:3 \[default\], `169` for 16:9, `1610` for 16:10, `149` for 14:9, `141` for 1.41:1, `54` for 5:4, `32` for 3:2 |
| `beamerarticle` | Produce an article from Beamer slides |
| `beameroption` | Extra beamer options provided to `\setbeameroption{}` |
| `institute` | Author affiliations: can be a list when there are multiple authors |
| `logo` | Logo image for slides |
| `navigation` | Controls navigation symbols (default is `empty` for no navigation symbols; other valid values are `frame`, `vertical`, and `horizontal`) |
| `section-titles` | Enables "title pages" for new sections (default is true) |
| `theme, colortheme, fonttheme, innertheme, outertheme` | Beamer themes |
| `themeoptions` | Options for LaTeX beamer themes (a list) |
| `titlegraphic` | Image for title slide |

## Frame Attributes

Sometimes it is necessary to add the LaTeX `[fragile]` option to a frame in beamer (for example, when using the `minted` environment). This can be forced by adding the `fragile` class to the heading introducing the slide:

``` markdown
# Fragile slide {.fragile}
```

All of the other frame attributes described in Section 8.1 of the [Beamer User's Guide](http://mirrors.ctan.org/macros/latex/contrib/beamer/doc/beameruserguide.pdf) may also be used: `allowdisplaybreaks`, `allowframebreaks`, `b`, `c`, `t`, `environment`, `label`, `plain`, `shrink`, `standout`, `noframenumbering`.

## Background Images

To provide a common background image for all slides in a Beamer presentation, use the `background-image` format option. For example:

``` yaml
---
format:
  beamer:
    background-image: background.png
---    
```


--------------------------------------------------------------------------------
/docs/presentations/index.qmd:
--------------------------------------------------------------------------------
---
title: Presentations
format: html
slide-format: revealjs
---

## Overview

Quarto supports a variety of formats for creating presentations, including:

-   `revealjs` --- [reveal.js](revealjs/index.qmd) (HTML)

-   `pptx` --- [PowerPoint](powerpoint.qmd) (MS Office)

-   `beamer` --- [Beamer](beamer.qmd) (LaTeX/PDF)

There are pros and cons to each of these formats. The most capable format by far is `revealjs`, so it is highly recommended unless you have specific Office or LaTeX output requirements. Note that `revealjs` presentations can be presented as HTML slides or can be printed to PDF for easier distribution.

Below, we'll describe the basic syntax for presentations that applies to all formats. See the format-specific articles for additional details on their native capabilities.

{{< include _creating-slides.md >}}

{{< include _incremental-lists.md >}}

{{< include _columns.md >}}


## Learning More

See these format-specific articles for additional details on the additional capabilities of each format:

-   `revealjs` --- [reveal.js](revealjs/index.qmd) (HTML)

-   `pptx` --- [PowerPoint](powerpoint.qmd) (MS Office)

-   `beamer` --- [Beamer](beamer.qmd) (LaTeX/PDF)



--------------------------------------------------------------------------------
/docs/presentations/powerpoint.qmd:
--------------------------------------------------------------------------------
---
title: "PowerPoint"
slide-format: pptx
is_pptx: true
---

## Overview

You can create [PowerPoint](https://en.wikipedia.org/wiki/Microsoft_PowerPoint) presentations using the `pptx` format. PowerPoint presentations support core presentation features like incremental bullets, 2-column layouts, and speaker notes, and can also be rendered using custom [PowerPoint templates].

See the PowerPoint [format reference](/docs/reference/formats/presentations/pptx.qmd) for a complete list of all options available for PowerPoint output.

{{< include _creating-slides.md >}}

{{< include _incremental-lists.md >}}

{{< include _columns.md >}}

{{< include _speaker-notes.md >}}


## PowerPoint Templates

By default PowerPoint output uses a fairly plain looking template. You can customize what template is used via the `reference-doc` option. For example:

``` yaml
---
title: "Presentation"
format:
  pptx:
    reference-doc: template.pptx
---
```

Nearly all templates included with recent versions of PowerPoint (either with `.pptx` or `.potx` extension) are known to work, as are most templates derived from these.

The specific requirement is that the template should contain layouts with the following names (as seen within PowerPoint, click on `Layout` under the `Home` menu to check):

-   Title Slide
-   Title and Content
-   Section Header
-   Two Content
-   Comparison
-   Content with Caption
-   Blank

For each name, the first layout found with that name will be used. If no layout is found with one of the names, Pandoc will output a warning and use the layout with that name from the default `reference-doc` instead.

### Creating a Template

To create a template from scratch, start with the default PowerPoint template as follows:

```{.bash filename="Terminal"}
quarto pandoc -o template.pptx --print-default-data-file reference.pptx 
```

Then edit the `template.pptx` file within PowerPoint as desired, and use it as the value for `reference-doc` (as shown above) when rendering your slides:

## Slide Layouts

When creating slides, the pptx writer chooses from a number of pre-defined layouts, based on the content of the slide:

**Title Slide**

:   This layout is used for the initial slide, which is generated and filled from the metadata fields `date`, `author`, and `title`, if they are present.

**Section Header**

:   This layout is used for what pandoc calls "title slides", i.e. slides which start with a header which is above the slide level in the hierarchy.

**Two Content**

:   This layout is used for two-column slides, i.e. slides containing a div with class `columns` which contains at least two divs with class `column`.

**Comparison**

:   This layout is used instead of "Two Content" for any two-column slides in which at least one column contains text followed by non-text (e.g. an image or a table).

**Content with Caption**

:   This layout is used for any non-two-column slides which contain text followed by non-text (e.g. an image or a table).

**Blank**

:   This layout is used for any slides which only contain blank content, e.g. a slide containing only speaker notes, or a slide containing only a non-breaking space.

**Title and Content**

:   This layout is used for all slides which do not match the criteria for another layout.

These layouts are chosen from the default `pptx` reference doc included with Pandoc, unless an alternative reference doc is specified using `reference-doc`.

## Background Images

To provide a common background image for multiple slides in a PowerPoint presentation, include the background image within the relevant slide layouts of a custom PowerPoint template (see [Creating a Template] for details on creating templates).

To add a background image to an individual slide, add the `background-image` attribute to the slide's heading. For example:

``` markdown
## Slide Title {background-image="background.png"}
```

Note that this also works even if you don't have slide heading text. For example:

``` markdown
## {background-image="background.png"}
```

For background images, only the "stretch" mode is supported, and the background image is centred around the slide in the image's larger axis, matching the observed default behaviour of PowerPoint.



--------------------------------------------------------------------------------
/docs/presentations/revealjs/_background-video.md:
--------------------------------------------------------------------------------


| **Attribute**            | **Default** | **Description**                                                                         |
|:-------------------------|:------------|:----------------------------------------------------------------------------------------|
| `background-video`       |             | A single video source, or a comma separated list of video sources.                      |
| `background-video-loop`  | false       | Flags if the video should play repeatedly.                                              |
| `background-video-muted` | false       | Flags if the audio should be muted.                                                     |
| `background-size`        | cover       | Use `cover` for full screen and some cropping or `contain` for letterboxing.            |
| `background-opacity`     | 1           | Opacity of the background video on a 0-1 scale. 0 is transparent and 1 is fully opaque. |

For example:

``` markdown
## Slide Title {background-video="video.mp4" background-video-loop="true" background-video-muted="true"}

This slides's background video will play in a loop with audio muted.
```



--------------------------------------------------------------------------------
/docs/presentations/revealjs/_callout-auto-stretch-scrollable.qmd:
--------------------------------------------------------------------------------
::: {.callout-note}

## Limitation: Auto-stretch and Scrollable 

When a slide is [scrollable](index.qmd#content-overflow) the image size calculations used by [auto-stretch](advanced.qmd#stretch) may not work well and images may not appear. Two solutions depending on your needs are:

- Disable auto-stretch at the presentation level, `auto-stretch: false`, and use `.r-stretch` on individual images only where needed.

- On slides that are scrollable, add the `.nostretch` class to disable auto-stretch on the slide.

:::


--------------------------------------------------------------------------------
/docs/presentations/revealjs/_theme-basics.md:
--------------------------------------------------------------------------------
There are 11 built-in themes provided for Reveal presentations (you can also create your own themes). The `default` and `dark` themes use fairly classic typography and color schemes and are a good place to start.

The `default` theme is used automatically --- use the `theme` option to switch to an alternate theme. For example

```yaml
---
title: "Presentation"
format:
  revealjs: 
    theme: dark
---
```

Here is the full list of available themes:

-   `beige`
-   `blood`
-   `dark`
-   `default`
-   `league`
-   `moon`
-   `night`
-   `serif`
-   `simple`
-   `sky`
-   `solarized`




--------------------------------------------------------------------------------
/docs/presentations/revealjs/advanced.qmd:
--------------------------------------------------------------------------------
---
title: "Advanced Reveal"
---

## Title Slide

The main title slide is the first slide of the presentation, and its content is generated based on a variety document options (title, subtitle, date, author, institute, etc.). 

### Custom Background

If you want to provide a custom background for the title slide, then do the following:

1. Use the `title-slide-attributes` key to provide background options.
2. Within this key, specify any of the supported [slide background options](index.qmd#slide-backgrounds),  but with `data-` prepended to them. 

For example:

```yaml
---
title: My Slide Show
title-slide-attributes:
  data-background-image: /path/to/title_image.png
  data-background-size: contain
  data-background-opacity: "0.5"
---
```

### Custom Template

You can replace the default title slide entirely with your own template. To do this, specify a `title-slide.html` [template partial](/docs/journals/templates.qmd#template-partials). For example:

```yaml
title: My Slide Show
format:
  revealjs:
    template-partials:
      - title-slide.html
```

Quarto natively supports a title slide which improves the handling of authors and affiliations. While it is backward compatible with `author` and `institute`, we now recommend that you use standard [author metadata](/docs/authoring/front-matter.qmd#authors-and-affiliations). To provide your own partial for `title-slide.html`, you can start from the source code for this [fancier title slide template](https://github.com/quarto-dev/quarto-cli/blob/main/src/resources/formats/revealjs/pandoc/title-fancy/title-slide.html). Customize this template as required, then save the results to `title-slide.html` alongside your presentation. 

If you prefer pandoc's default title slide you can opt-in using `title-slide-style: pandoc` in your YAML --- this uses this [simpler title slide template partial](https://github.com/quarto-dev/quarto-cli/blob/main/src/resources/formats/revealjs/pandoc/title-slide.html). However, this simpler partial does not leverage our improved handling for [Authors & Affiliations](/docs/journals/authors.qmd), so we recommend using the fancy one as a starter for custom title slides. 

### Centering {#sec-revealjs-title-center}

By default, the title slide is centered while all slides are top aligned (i.e. `center: false`). You can prevent the title slide centering by setting `center-title-slide` options: 

```yaml
title: My Slide Show
format:
  revealjs:
    center-title-slide: false
```

If `center: true` is set, `center-title-slide` will be ignored. There is currently no way to have content slide centered and title slides top aligned. For slide content centering, see @sec-revealjs-slide-center.

## Slide Transitions

Reveal supports a number of animated transition effects for both slide changes and slide background changes. By default no transitions are used, however you can enable them either globally or per-slide using the options described below.

Here are the available transition types:

| Transition | Description                                                            |
|------------|------------------------------------------------------------------------|
| `none`     | No transition (switch instantly)                                       |
| `fade`     | Cross fade                                                             |
| `slide`    | Slide horizontally                                                     |
| `convex`   | Slide at a convex angle                                                |
| `concave`  | Slide at a concave angle                                               |
| `zoom`     | Scale the incoming slide so it grows in from the center of the screen. |

Here's how you would set the global transition style for both slides and backgrounds:

``` yaml
---
title: "Presentation"
format:
  revealjs:
    transition: slide
    background-transition: fade
---
```

You can also specify the `transition-speed` as `default`, `fast`, or `slow`:

``` yaml
---
title: "Presentation"
format:
  revealjs:
    transition: slide
    transition-speed: fast
---
```

You can also specify the `transition` and/or `transition-speed` for an individual slide:

``` markdown
## Slide Title {transition="fade" transition-speed="fast"}
```

You can also specify separate in and out transitions, for example:

``` markdown
## Slide Title {transition="fade-in slide-out"}
```

## Slide Visibility

You can hide a slide by adding the `visibility="hidden"` attribute to the slide heading. For example:

``` markdown
## Slide Title {visibility="hidden"}
```

### Uncounted Slides

When preparing a presentation it can sometimes be helpful to prepare optional slides that you may or may not have time to show. This is easily done by appending a few slides at the end of the presentation, however this means that the Reveal progress bar and slide numbering will hint that there are additional slides.

To "hide" those slides from the numbering system you can use `visibility="uncounted"`. For example:

``` markdown
## Slide 1

## Slide 2

## Slide 3 {visibility="uncounted"}
```

## Presentation Size

All presentations have a "normal" size, that is, the resolution at which they are authored. This default "normal" size is 1050 x 700, which is used to match as nearly as possible the aspect ratio of most laptops.

Reveal will automatically scale presentations uniformly based on the normal size to ensure that everything fits on any given display or viewport without changing the aspect ratio or layout of your content.

You can change the slide size, the margin around content, as well as set limits on content scaling using the following options:

| Option      | Description                                                                              |
|-------------|------------------------------------------------------------------------------------------|
| `width`     | Normal width (defaults to 1050)                                                          |
| `height`    | Normal height (defaults to 700)                                                          |
| `margin`    | Factor of the display size that should remain empty around the content (defaults to 0.1) |
| `min-scale` | Smallest possible scale to apply to content (defaults to 0.2)                            |
| `max-scale` | Largest possible scale to apply to content (defaults to 2.0)                             |

## Absolute Position

The `absolute` class lets you position elements at arbitrary positions on a slide. These elements have CSS `position: absolute` and can be placed relative to the `top`, `left`, `bottom`, and/or `right` edges of the slide.

For example, here we add the `.absolute` class to three images and give them each a distinct position on the slide (note that we use also `width` and `height` to control their dimensions):

``` {.markdown .reveal-demo code-preview="demo/mini/absolute.qmd"}
![](image1.png){.absolute top=200 left=0 width="350" height="300"}

![](image2.png){.absolute top=50 right=50 width="450" height="250"}

![](image3.png){.absolute bottom=0 right=50 width="300" height="300"}
```

The following attributes can be used with `absolute`. All of these values can be specified in CSS units (e.g. `px`, `em`, etc.). If a number with no units is specified (as in the above example) then pixels are assumed.

| Attribute | Description                   |
|-----------|-------------------------------|
| `width`   | Width of element              |
| `height`  | Height of element             |
| `top`     | Distance from top of slide    |
| `left`    | Distance from left of slide   |
| `bottom`  | Distance from bottom of slide |
| `right`   | Distance from right of slide  |

Note that default size of presentation slides is 1050 x 700. See [Presentation Size] for details on customizing this.

## Layout Helpers

Reveal provides some helper classes for controlling the layout of content.

### Stack Layout

The `r-stack` layout class lets you center and place multiple elements on top of each other. This is intended to be used together with [fragments] to incrementally reveal elements.

For example, here we create a div with the `.r-stack` class and then include 3 images (each of which uses `.fragment` so they display incrementally):

``` {.markdown .reveal-demo code-preview="demo/mini/stack.qmd"}
::: {.r-stack}
![](image1.png){.fragment width="450" height="300"}

![](image2.png){.fragment width="300" height="450"}

![](image3.png){.fragment width="400" height="400"}
:::
```

### Fit Text

The `r-fit-text` class makes text as large as possible without overflowing the slide. This is great when you want BIG text without having to manually find the right font size. For example:

``` markdown
::: {.r-fit-text}
Big Text
:::
```

### Center {#sec-revealjs-slide-center}

The `center` class when applied to a slide, will vertically center the slide content by adding the appropriate spacing at the top of the slide. Vertical distances between elements will not be modified. For example:

``` markdown
## This will be centered {.center}

This text is moved as well
```

For controlling title slide centering, see @sec-revealjs-title-center.

### Stretch

The `r-stretch` layout helper lets you resize an element, like an image or video, to cover the remaining vertical space in a slide. For example, here the image will automatically be resized to fit space remaining outside of the slide title and text before and after it:

``` markdown
## Slide Title

Here is an image:

![](image.png){.r-stretch}

Some text after the image.
```

For slides that contain only a single top-level image, the `.r-stretch` class is automatically applied to the image. You can disable this behavior by setting the `auto-stretch: false` option:

``` yaml
format:
  revealjs:
    auto-stretch: false
```

You can also disable auto-stretch for an individual slide by adding the `.nostretch` class:

``` markdown
## Slide Title {.nostretch}
```

Or apply `.nostretch` directly to an individual image:

```markdown
![](image.png){.nostretch fig-align="center" width="800px"}
```

`auto-stretch` will only apply to non-nested images, which means an image in a feature block (e.g fragments, layout panel, columns, ... ) or a custom Div will be ignored. For custom Divs, you can opt-in to `auto-stretch` behavior by adding the class `.r-stretch` to the outer div. 

{{< include _callout-auto-stretch-scrollable.qmd >}}

## Auto Animate

Revealjs can automatically animate elements across slides. All you need to do is add the `auto-animate` attribute to two adjacent slides and Auto-Animate will animate all matching elements between the two.

Here's a simple example to give you a better idea of how it can be used. Note that the slides don't have titles in this example (rather just the `auto-animate` attribute) however they could also include a title.

``` {.markdown .reveal-demo code-preview="demo/mini/auto-animate.qmd"}
## {auto-animate=true}

::: {style="margin-top: 100px;"}
Animating content
:::

## {auto-animate=true}

::: {style="margin-top: 200px; font-size: 3em; color: red;"}
Animating content
:::
```

This example uses the `margin-top` property to move the element but internally Reveal will use a CSS transform to ensure smooth movement. This same approach to animation works with most animatable CSS properties meaning you can transition things like `position`, `font-size`, `line-height`, `color`, `background-color`, `padding` and `margin`.

### Code Animations

You can also animate between code blocks to show changes in code. For example:

```` {.markdown .reveal-demo code-preview="demo/mini/auto-animate-code.qmd"}
## {auto-animate="true"}

```r
# Fill in the spot we created for a plot
output$phonePlot <- renderPlot({
  # Render a barplot
})
```

## {auto-animate=true}

```r
# Fill in the spot we created for a plot
output$phonePlot <- renderPlot({
  # Render a barplot
  barplot(WorldPhones[,input$region]*1000, 
          main=input$region,
          ylab="Number of Telephones",
          xlab="Year")
})
```
````

### Movement Animations

Animations are not limited to changes in style. Auto-Animate can also be used to automatically move elements into their new position as content is added, removed or rearranged on a slide. All without a single line of inline CSS. For example, here the delta between the content on two slides is implicitly animated:

``` {.markdown .reveal-demo code-preview="demo/mini/auto-animate-movement.qmd"}
## {auto-animate=true}

Animation

## {auto-animate=true}

Implicit

Animation
```

### Element Matching

When you navigate between two auto-animated slides we'll do our best to automatically find matching elements in the two slides. For text, we consider it a match if both the text contents and node type are identical. For images, videos and iframes we compare the `src` attribute. We also take into account the order in which the element appears in the DOM.

In situations where automatic matching is not feasible you can give the objects that you want to animate between a matching `data-id` attribute. We prioritize matching `data-id` values above our automatic matching.

Here's an example where we've given several blocks a matching ID since automatic matching has no content to go on. This example also makes use of some additional animation attributes (`auto-animate-easing` and `auto-animate-delay`), which we'll describe in the next section.

``` {.markdown .reveal-demo code-preview="demo/mini/auto-animate-stack.qmd"}
## {auto-animate=true auto-animate-easing="ease-in-out"}

::: {.r-hstack}
::: {data-id="box1" auto-animate-delay="0" style="background: #2780e3; width: 200px; height: 150px; margin: 10px;"}
:::

::: {data-id="box2" auto-animate-delay="0.1" style="background: #3fb618; width: 200px; height: 150px; margin: 10px;"}
:::

::: {data-id="box3" auto-animate-delay="0.2" style="background: #e83e8c; width: 200px; height: 150px; margin: 10px;"}
:::
:::

## {auto-animate=true auto-animate-easing="ease-in-out"}

::: {.r-stack}
::: {data-id="box1" style="background: #2780e3; width: 350px; height: 350px; border-radius: 200px;"}
:::

::: {data-id="box2" style="background: #3fb618; width: 250px; height: 250px; border-radius: 200px;"}
:::

::: {data-id="box3" style="background: #e83e8c; width: 150px; height: 150px; border-radius: 200px;"}
:::
:::
```

### Animation Settings

You can override specific animation settings such as easing and duration either for the whole presentation, per-slide or individually for each animated element. The following configuration attributes can be used to change the settings for a specific slide or element:

| **Attribute**            | **Default** | **Description**                                                                                                                |
|:-------------------------|:-----------:|:-------------------------------------------------------------------------------------------------------------------------------|
| `auto-animate-easing`    |    ease     | A CSS [easing function](https://developer.mozilla.org/en-US/docs/Web/CSS/easing-function).                                     |
| `auto-animate-unmatched` |    true     | Determines whether elements with no matching auto-animate target should fade in. Set to `false` to make them appear instantly. |
| `auto-animate-duration`  |     1.0     | Animation duration in seconds.                                                                                                 |
| `auto-animate-delay`     |      0      | Animation delay in seconds (can only be set for specific elements, not at the slide level).                                    |
| `auto-animate-id`        |  *absent*   | An id tying auto-animate slides together.                                                                                      |
| `auto-animate-restart`   |  *absent*   | Breaks apart two adjacent auto-animate slides (even with the same id).                                                         |

You can override the global defaults for easing, unmatched, and duration as follows:

``` yaml
---
title: "My Slide"
format:
  revealjs:
    auto-animate-easing: ease-in-out
    auto-animate-unmatched: false
    auto-animate-duration: 0.8
---
```

## Fragments {data-link="fragments"}

Fragments are used to highlight or incrementally reveal individual elements on a slide. Every element with the class `fragment` will be stepped through before moving on to the next slide.

Note that fragments as discussed here are a relatively advanced form of incremental content display---see [Incremental Lists](index.qmd#incremental-lists) for documentation on creating incremental bullet lists and inserting content pauses in slides.

The default fragment style is to start out invisible and fade in. This style can be changed by appending a different class to the fragment. For example:

``` {.markdown .reveal-demo code-preview="demo/mini/fragments.qmd"}
::: {.fragment}
Fade in
:::

::: {.fragment .fade-out}
Fade out
:::

::: {.fragment .highlight-red}
Highlight red
:::

::: {.fragment .fade-in-then-out}
Fade in, then out
:::

::: {.fragment .fade-up}
Slide up while fading in
:::
```

### Fragment Classes

Here are all of the available fragment classes:

| **Name**                  | **Effect**                                          |
|:--------------------------|:----------------------------------------------------|
| `fade-out`                | Start visible, fade out                             |
| `fade-up`                 | Slide up while fading in                            |
| `fade-down`               | Slide down while fading in                          |
| `fade-left`               | Slide left while fading in                          |
| `fade-right`              | Slide right while fading in                         |
| `fade-in-then-out`        | Fades in, then out on the next step                 |
| `fade-in-then-semi-out`   | Fades in, then out to 50% on the next step          |
| `grow`                    | Scale up                                            |
| `semi-fade-out`           | Fade out to 50%                                     |
| `shrink`                  | Scale down                                          |
| `strike`                  | Strike through                                      |
| `highlight-red`           | Turn text red                                       |
| `highlight-green`         | Turn text green                                     |
| `highlight-blue`          | Turn text blue                                      |
| `highlight-current-red`   | Turn text red, then back to original on next step   |
| `highlight-current-green` | Turn text green, then back to original on next step |
| `highlight-current-blue`  | Turn text blue, then back to original on next step  |

### Nested Fragments

Multiple fragments can be applied to the same element sequentially by wrapping it. The following example will fade in the text on the first step, turn it red on the second and partially fade out on the third:

``` {.markdown .reveal-demo code-preview="demo/mini/fragments-nested.qmd"}
::: {.fragment .fade-in}
::: {.fragment .highlight-red}
::: {.fragment .semi-fade-out}
Fade in > Turn red > Semi fade out
:::
:::
:::
```

### Fragment Order

By default fragments will be stepped through in the order that they appear in the DOM. This display order can be changed using the `fragment-index` attribute. Note that multiple elements can appear at the same index:

``` markdown
::: {.fragment fragment-index=3}
Appears last
:::

::: {.fragment fragment-index=1}
Appears first
:::

::: {.fragment fragment-index=2}
Appears second
:::
```

### Custom Fragments

Custom effects can be created by specifying CSS styles for `.fragment.effectname` and `.fragment.effectname.visible`. The `visible` class is applied to each fragment as they are navigated through during the presentation. A `custom` class can be added to each fragment to tell reveal.js to avoid applying its default fade-in fragment styles.

For example, the following defines a fragment style where elements are initially blurred but become focused when stepped through.

``` {.markdown .reveal-demo code-preview="demo/mini/fragments-custom.qmd"}
::: {.fragment .custom .blur}
First item to be unblurred
:::

::: {.fragment .custom .blur}
Second one to be revealed
:::
```

with this CSS for the style associated with `blur` class.
````css
.reveal .slides section .fragment.blur {
  filter: blur(5px);
}

.reveal .slides section .fragment.blur.visible {
  filter: none
}
````

## Parallax Background

If you want to use a parallax scrolling background, add the `parallax-background-image` and `parallax-background-size` options. For example:

``` yaml
---
title: "Presentation"
format:
  revealjs:
     parallax-background-image: background.png
     parallax-background-size: "2100px 900px"
     parallax-background-horizontal: 200
     parallax-background-vertical: 50
---
```

Note that the `parallax-background-horizontal` and `parallax-background-vertical` options are not required (the defaults shown above will be used if they are not specified).

## Vertical Slides

Reveal uses classic linear slide navigation by default. If you wish you can also configure slide navigation to nest multiple slides within a single top-level slide to create a vertical stack.

Use the `navigation-mode` option to fine tune Reveal navigation behavior:

| Navigation Mode | Behavior                                                                                                                                                                  |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `linear`        | Left/right arrows keys step through all slides (both horizontal and vertical).                                                                                            |
| `vertical`      | Left/right arrow keys step between horizontal slides. Up/down arrow keys step between vertical slides. Space key steps through all slides (both horizontal and vertical). |
| `grid`          | When enabled, stepping left/right from a vertical stack to an adjacent vertical stack will land you at the same vertical index.                                           |

If you use `vertical` or `grid` navigation, you should structure your slides using level 1 headings for the horizontal axis and level 2 headings for the vertical axis. For example:

``` markdown
---
title: "Presentation"
format:
  revealjs:
    navigation-mode: vertical
---

# Slide 1

## Slide 1.1

## Slide 1.2

# Slide 2

## Slide 2.1

## Slide 2.2
```

### Slide Controls

When you enable `vertical` or `grid` navigation, controls will appear to provide a visual cue to where you are in the presentation (e.g. if there are vertical slides below you'll see a down control).

By default these controls appear at the edges of the presentation, you can position them in the bottom right corner using the `controls-layout` option. You can also provide an extra visual cue to viewers that the controls are available using the `controls-tutorial` option. For example:

``` yaml
---
title: "Presentation"
format: 
  revealjs:
    navigation-mode: vertical
    controls-layout: bottom-right
    controls-tutorial: true
---
```

Note that using `controls-layout: bottom-right` isn't compatible with including a `logo` (as the logo appears in the bottom right corner as well).

You can also disable the controls entirely with `controls: false`.

::: callout-warning
While vertical slides do provide some additional flexibility over the traditional linear model, they are in practice very confusing for end users (mostly because they are so unexpected). Users will often skip the vertical content because they simply don't know it's there.

If your content benefits from vertical orientation (e.g. you have optional drill-down content that you don't want in the main flow of the presentation), you can by all means use the vertical mode. Just know that if you distribute your slides to users they will very likely not end up viewing any of the vertical content.
:::

## Touch Navigation

You can swipe to navigate through a presentation on any touch-enabled device. 

If you wish to disable this you can set the `touch` option to `false`:

``` yaml
---
title: "Presentation"
format:
  revealjs:
    touch: false
    controls: true
---
```

Note that we also enable `controls` at the same time (as users on phones or tablets don't have access to a keyboard).

## Reveal Plugins

To use [Revealjs plugins](https://github.com/hakimel/reveal.js/wiki/Plugins,-Tools-and-Hardware), you need to package them into a directory with a config file (`plugin.yml`). The config file lets Quarto know how to inject the plugin into the presentation (e.g. what scripts and/or css files to include, what the default configuration should be, etc.).

See the source code of the plugins that are built into Quarto Reveal for examples:

<https://github.com/quarto-dev/quarto-cli/tree/main/src/resources/formats/revealjs/plugins>

To use a plugin, just include a reference to its directory in the list of `revealjs-plugins`. For example:

``` yaml
---
title: "Presentation"
format:
  revealjs:
    revealjs-plugins:
      - myplugin
---
```

Note that many of the most popular Reveal plugins are already included with the Quarto version of Reveal, so there is no need to include them separately. Built-in plugins include:

-   [Multiplex](https://github.com/reveal/multiplex)
-   [RevealMenu](https://github.com/denehyg/reveal.js-menu)
-   [RevealChalkboard](https://github.com/rajgoel/reveal.js-plugins/tree/master/chalkboard)
-   [PdfExport](https://github.com/McShelby/reveal-pdfexport)

### Example

Let's show an example with the [fullscreen](https://github.com/rajgoel/reveal.js-plugins/tree/master/fullscreen) plugin. Here are the steps to bundle this plugin to use within your Quarto HTML presentation:

1.  Create a folder with the name you want for the plugin, here we'll call it `fullscreen`.

2.  Download the plugin files into the created folder. Here the plugin only have a JS file called `plugin.js` that you can find [on the repo *rajgoel/reveal.js-plugins*](https://raw.githubusercontent.com/rajgoel/reveal.js-plugins/master/fullscreen/plugin.js). You can keep the name or rename it, e.g `fullscreen.js`.

3.  In that folder add a `plugin.yml` file, as in [Quarto Reveal examples](https://github.com/quarto-dev/quarto-cli/tree/main/src/resources/formats/revealjs/plugins).

    -   `name` is a mandatory field which should be the name of the JS function the JS plugin is defining. Open the JS script you downloaded to look for it.
    -   Other fields are for the resources to be used. In our example, only a JS script so we'll use `script`

    Our `plugin.yml` would be:

    ``` yaml
    name: RevealFullscreen
    script: [fullscreen.js]
    ```

4.  Now add the plugin reference into your document YAML header, using the path of the folder your created:

    ``` yaml
    format: 
     revealjs:
       revealjs-plugins:
         - fullscreen
    ```

5.  The custom plugin will be loaded in your presentation and you can use it. The plugin *fullscreen* documentation shows an example of adding a Map fullscreen in a slide by adding an attribute on the section, and using stretch on the content. This would translate to having this slide in the `.qmd` file:

    ``` markdown
    ## {fullscreen=true}

    <iframe class="stretch" data-src="https://www.google.com/maps/embed?pb=!1m14!1m12!1m3!1d61206.89156051744!2d-151.77366863890407!3d-16.50433878928727!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!5e0!3m2!1sen!2sde!4v1467468929561"></iframe>
    ```

## Learning More

See these articles lo learn more about using Reveal:

-   [Reveal Basics](index.qmd) covers the basic mechanics of creating presentations.
-   [Presenting Slides](presenting.qmd) describes slide navigation, printing to PDF, drawing on slides using a chalkboard, and creating multiplex presentations.
-   [Reveal Themes](themes.qmd) talks about using and customizing existing themes as well as creating brand new themes.



--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/actors.js:
--------------------------------------------------------------------------------
import * as regression from 'https://cdn.skypack.dev/d3-regression';
import * as d3 from 'https://cdn.skypack.dev/d3';

export function plotActors(actors, talentWeight, looksWeight, minimum) {
    
  actors = transpose(actors).map(v => ({
    talent: v.x,
    looks: v.y,
    fame: v.x * talentWeight + v.y * looksWeight
  }));

  const w = 600;
  const h = 470;
  const result = d3.create("svg").attr("width", w).attr("height", h);
  const margin = 20;
  const xScale = d3.scaleLinear().domain([-2, 2]).range([margin, w - margin]);
  const yScale = d3.scaleLinear().domain([-2, 2]).range([h - margin, margin]);
  const points = result
    .append("g")
    .selectAll("circle")
    .data(actors)
    .join(enter => {
       const sel = enter
         .append("circle")
         .attr("r", 3)
         .attr("cx", d => xScale(d.talent))
         .attr("cy", d => yScale(d.looks))
         .attr("fill", d3.lab(50, 40, 20));
       return sel.filter(d => d.fame <= minimum)
         .attr("fill", "rgb(200, 200, 200)")
         .attr("r", 2);
    });
    
  const linearRegression = regression.regressionLinear()
    .x(d => d.talent)
    .y(d => d.looks)
    .domain([-2, 2]);

  const chosenActors = actors
    .filter(d => d.fame > minimum);

  const line = result
    .append("g")
    .append("line")
    .attr("stroke", d3.lab(20, 40, 20))
    .attr("stroke-width", 1.5)
    .datum(linearRegression(chosenActors))
    .attr("x1", d => xScale(d[0][0]))
    .attr("x2", d => xScale(d[1][0]))
    .attr("y1", d => yScale(d[0][1]))
    .attr("y2", d => yScale(d[1][1]));


  const xAxis = d3.axisBottom(xScale).ticks(3);
  result.append("g")
    .attr("transform", `translate(0, ${yScale(0)})`)
    .call(xAxis);

  result.append("text")
    .attr("x", xScale(0.05))
    .attr("y", yScale(2))
    .text("Looks");

  result.append("text")
    .attr("y", yScale(0.1))
    .attr("x", xScale(-2))
    .text("Talent");

  const yAxis = d3.axisLeft(yScale).ticks(3);
  result.append("g")
    .attr("transform", `translate(${xScale(0)}, 0)`)
    .call(yAxis);
  
  return result.node();
}

function transpose(df) {
  const keys = Object.keys(df);
  return df[keys[0]]
    .map((v, i) => Object.fromEntries(keys.map(key => [key, df[key][i] || undefined])))
    .filter(v => Object.values(v).every(e => e !== undefined));
}






--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/demo.pdf:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/demo/demo.pdf


--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/images/beige.png:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/demo/images/beige.png


--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/images/jupyter-edit.png:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/demo/images/jupyter-edit.png


--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/images/jupyter-preview.png:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/demo/images/jupyter-preview.png


--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/images/milky-way.jpeg:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/demo/images/milky-way.jpeg


--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/images/moon.png:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/demo/images/moon.png


--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/images/overview-mode.png:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/demo/images/overview-mode.png


--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/images/presentation-chalkboard.png:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/demo/images/presentation-chalkboard.png


--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/images/presentation-menu.png:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/demo/images/presentation-menu.png


--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/images/presentation-notes-canvas.png:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/demo/images/presentation-notes-canvas.png


--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/images/quarto.png:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/demo/images/quarto.png


--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/images/rstudio.png:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/demo/images/rstudio.png


--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/images/serif.png:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/demo/images/serif.png


--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/images/sky.png:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/demo/images/sky.png


--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/images/speaker-view.png:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/demo/images/speaker-view.png


--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/index.qmd:
--------------------------------------------------------------------------------
---
title: "Quarto Presentations"
subtitle: "Create beautiful interactive slide decks with Reveal.js"
format:
  revealjs: 
    slide-number: true
    chalkboard: 
      buttons: false
    preview-links: auto
    logo: images/quarto.png
    css: styles.css
    footer: '[https://{{< meta prerelease-subdomain >}}quarto.org](https://{{< meta prerelease-subdomain >}}quarto.org)'
resources:
  - demo.pdf
---

## Hello, There

This presentation will show you examples of what you can do with Quarto and [Reveal.js](https://revealjs.com), including:

-   Presenting code and LaTeX equations
-   Including computations in slide output
-   Image, video, and iframe backgrounds
-   Fancy transitions and animations
-   Activating scroll view

...and much more

## Pretty Code {auto-animate="true"}

-   Over 20 syntax highlighting themes available
-   Default theme optimized for accessibility

``` r
# Define a server for the Shiny app
function(input, output) {
  
  # Fill in the spot we created for a plot
  output$phonePlot <- renderPlot({
    # Render a barplot
  })
}
```

::: footer
Learn more: [Syntax Highlighting](https://{{< meta prerelease-subdomain >}}quarto.org/docs/output-formats/html-code.html#highlighting)
:::

## Code Animations {auto-animate="true"}

-   Over 20 syntax highlighting themes available
-   Default theme optimized for accessibility

``` r
# Define a server for the Shiny app
function(input, output) {
  
  # Fill in the spot we created for a plot
  output$phonePlot <- renderPlot({
    # Render a barplot
    barplot(WorldPhones[,input$region]*1000, 
            main=input$region,
            ylab="Number of Telephones",
            xlab="Year")
  })
}
```

::: footer
Learn more: [Code Animations](https://{{< meta prerelease-subdomain >}}quarto.org/docs/presentations/revealjs/advanced.html#code-animations)
:::

## Line Highlighting

-   Highlight specific lines for emphasis
-   Incrementally highlight additional lines

``` {.python code-line-numbers="4-5|7|10"}
import numpy as np
import matplotlib.pyplot as plt

r = np.arange(0, 2, 0.01)
theta = 2 * np.pi * r
fig, ax = plt.subplots(subplot_kw={'projection': 'polar'})
ax.plot(theta, r)
ax.set_rticks([0.5, 1, 1.5, 2])
ax.grid(True)
plt.show()
```

::: footer
Learn more: [Line Highlighting](https://{{< meta prerelease-subdomain >}}quarto.org/docs/presentations/revealjs/#line-highlighting)
:::

## Executable Code

```{r}
#| echo: true
#| fig-width: 10
#| fig-height: 4.5
library(ggplot2)
ggplot(mtcars, aes(hp, mpg, color = am)) +
  geom_point() +
  geom_smooth(formula = y ~ x, method = "loess")
```

::: footer
Learn more: [Executable Code](https://{{< meta prerelease-subdomain >}}quarto.org/docs/presentations/revealjs/#executable-code)
:::

## LaTeX Equations

[MathJax](https://www.mathjax.org/) rendering of equations to HTML

::: columns
::: {.column width="40%"}
``` tex
\begin{gather*}
a_1=b_1+c_1\\
a_2=b_2+c_2-d_2+e_2
\end{gather*}

\begin{align}
a_{11}& =b_{11}&
  a_{12}& =b_{12}\\
a_{21}& =b_{21}&
  a_{22}& =b_{22}+c_{22}
\end{align}
```
:::

::: {.column width="60%"}
```{=tex}
\begin{gather*}
a_1=b_1+c_1\\
a_2=b_2+c_2-d_2+e_2
\end{gather*}
```
```{=tex}
\begin{align}
a_{11}& =b_{11}&
  a_{12}& =b_{12}\\
a_{21}& =b_{21}&
  a_{22}& =b_{22}+c_{22}
\end{align}
```
:::
:::

::: footer
Learn more: [LaTeX Equations](https://{{< meta prerelease-subdomain >}}quarto.org/docs/authoring/markdown-basics.html#equations)
:::

## Column Layout {.smaller}

Arrange content into columns of varying widths:

::: columns
::: {.column width="35%"}
#### Motor Trend Car Road Tests

The data was extracted from the 1974 Motor Trend US magazine, and comprises fuel consumption and 10 aspects of automobile design and performance for 32 automobiles.
:::

::: {.column width="3%"}
:::

::: {.column width="62%"}
```{r}
knitr::kable(head(mtcars)[,c("mpg",	"cyl", "disp", "hp", "wt")])
```
:::
:::

::: footer
Learn more: [Multiple Columns](https://{{< meta prerelease-subdomain >}}quarto.org/docs/presentations/revealjs/#multiple-columns)
:::

## Incremental Lists

Lists can optionally be displayed incrementally:

::: incremental
-   First item
-   Second item
-   Third item
:::

. . .

<br/> Insert pauses to make other types of content display incrementally.

::: footer
Learn more: [Incremental Lists](https://{{< meta prerelease-subdomain >}}quarto.org/docs/presentations/revealjs/#incremental-lists)
:::

## Fragments

Incremental text display and animation with fragments:

<br/>

::: {.fragment .fade-in}
Fade in
:::

::: {.fragment .fade-up}
Slide up while fading in
:::

::: {.fragment .fade-left}
Slide left while fading in
:::

::: {.fragment .fade-in-then-semi-out}
Fade in then semi out
:::

. . .

::: {.fragment .strike}
Strike
:::

::: {.fragment .highlight-red}
Highlight red
:::

::: footer
Learn more: [Fragments](https://{{< meta prerelease-subdomain >}}quarto.org/docs/presentations/revealjs/advanced.html#fragments)
:::

## Slide Backgrounds {background="#43464B"}

Set the `background` attribute on a slide to change the background color (all CSS color formats are supported).

Different background transitions are available via the `background-transition` option.

::: footer
Learn more: [Slide Backgrounds](https://{{< meta prerelease-subdomain >}}quarto.org/docs/presentations/revealjs/#color-backgrounds)
:::

## Media Backgrounds {background="#43464B" background-image="images/milky-way.jpeg"}

You can also use the following as a slide background:

-   An image: `background-image`

-   A video: `background-video`

-   An iframe: `background-iframe`

::: footer
Learn more: [Media Backgrounds](https://{{< meta prerelease-subdomain >}}quarto.org/docs/presentations/revealjs/#image-backgrounds)
:::

## Absolute Position

Position images or other elements at precise locations

![](mini/images/kitten-400-350.jpeg){.absolute top="170" left="30" width="400" height="400"}

![](mini/images/kitten-450-250.jpeg){.absolute .fragment top="150" right="80" width="450"}

![](mini/images/kitten-300-200.jpeg){.absolute .fragment bottom="110" right="130" width="300"}

::: footer
Learn more: [Absolute Position](https://{{< meta prerelease-subdomain >}}quarto.org/docs/presentations/revealjs/advanced.html#absolute-position)
:::

## Auto-Animate {auto-animate="true" auto-animate-easing="ease-in-out"}

Automatically animate matching elements across slides with Auto-Animate.

::: r-hstack
::: {data-id="box1" auto-animate-delay="0" style="background: #2780e3; width: 200px; height: 150px; margin: 10px;"}
:::

::: {data-id="box2" auto-animate-delay="0.1" style="background: #3fb618; width: 200px; height: 150px; margin: 10px;"}
:::

::: {data-id="box3" auto-animate-delay="0.2" style="background: #e83e8c; width: 200px; height: 150px; margin: 10px;"}
:::
:::

::: footer
Learn more: [Auto-Animate](https://{{< meta prerelease-subdomain >}}quarto.org/docs/presentations/revealjs/advanced.html#auto-animate)
:::

## Auto-Animate {auto-animate="true" auto-animate-easing="ease-in-out"}

Automatically animate matching elements across slides with Auto-Animate.

::: r-stack
::: {data-id="box1" style="background: #2780e3; width: 350px; height: 350px; border-radius: 200px;"}
:::

::: {data-id="box2" style="background: #3fb618; width: 250px; height: 250px; border-radius: 200px;"}
:::

::: {data-id="box3" style="background: #e83e8c; width: 150px; height: 150px; border-radius: 200px;"}
:::
:::

::: footer
Learn more: [Auto-Animate](https://{{< meta prerelease-subdomain >}}quarto.org/docs/presentations/revealjs/advanced.html#auto-animate)
:::

## Slide Transitions {.smaller}

The next few slides will transition using the `slide` transition

| Transition | Description                                                            |
|------------|------------------------------------------------------------------------|
| `none`     | No transition (default, switch instantly)                              |
| `fade`     | Cross fade                                                             |
| `slide`    | Slide horizontally                                                     |
| `convex`   | Slide at a convex angle                                                |
| `concave`  | Slide at a concave angle                                               |
| `zoom`     | Scale the incoming slide so it grows in from the center of the screen. |

::: footer
Learn more: [Slide Transitions](https://{{< meta prerelease-subdomain >}}quarto.org/docs/presentations/revealjs/advanced.html#slide-transitions)
:::

## Tabsets {.smaller .scrollable transition="slide"}

::: panel-tabset
### Plot

```{r}
library(ggplot2)
ggplot(mtcars, aes(hp, mpg, color = am)) +
  geom_point() +
  geom_smooth(formula = y ~ x, method = "loess")
```

### Data

```{r}
knitr::kable(mtcars)
```
:::

::: footer
Learn more: [Tabsets](https://{{< meta prerelease-subdomain >}}quarto.org/docs/presentations/revealjs/#tabsets)
:::

## Interactive Slides {.smaller transition="slide"}

Include Jupyter widgets and htmlwidgets in your presentations

```{r}
#| echo: false
#| fig-height: 5
library(leaflet)
leaflet() %>%
  addTiles() %>%  # Add default OpenStreetMap map tiles
  addMarkers(lng=174.768, lat=-36.852, popup="The birthplace of R")
```

::: footer
Learn more: [Jupyter widgets](https://{{< meta prerelease-subdomain >}}quarto.org/docs/interactive/widgets/jupyter.html), [htmlwidgets](https://{{< meta prerelease-subdomain >}}quarto.org/docs/interactive/widgets/htmlwidgets.html)
:::

## Interactive Slides {.smaller transition="slide"}

Turn presentations into applications with Observable and Shiny. Use component layout to position inputs and outputs.

```{r}
ojs_define(actors = data.frame(
  x = rnorm(100),
  y = rnorm(100)
))
```

```{ojs}
//| panel: sidebar
viewof talentWeight = Inputs.range([-2, 2], { value: 0.7, step: 0.01, label: "talent weight" })
viewof looksWeight = Inputs.range([-2, 2], { value: 0.7, step: 0.01, label: "looks weight" })
viewof minimum = Inputs.range([-2, 2], { value: 1, step: 0.01, label: "min fame" })
```

```{ojs}
//| panel: fill
import { plotActors } from './actors.js';
plotActors(actors, talentWeight, looksWeight, minimum)
```

::: footer
Learn more: [Observable](https://{{< meta prerelease-subdomain >}}quarto.org/docs/interactive/ojs/), [Shiny](https://{{< meta prerelease-subdomain >}}quarto.org/docs/interactive/shiny/), [Component Layout](https://{{< meta prerelease-subdomain >}}quarto.org/docs/interactive/layout.html)
:::

## Preview Links

Navigate to hyperlinks without disrupting the flow of your presentation.

Use the `preview-links` option to open links in an iframe on top of your slides. Try clicking the link below for a demonstration:

::: {style="text-align: center; margin-top: 1em"}
[Matplotlib: Visualization with Python](https://matplotlib.org/){preview-link="true" style="text-align: center"}
:::

::: footer
Learn more: [Preview Links](https://{{< meta prerelease-subdomain >}}quarto.org/docs/presentations/revealjs/presenting.html#preview-links)
:::

## Themes

10 Built-in Themes (or [create your own](https://{{< meta prerelease-subdomain >}}quarto.org/docs/presentations/revealjs/themes.html#creating-themes))

::: {layout-ncol="2"}
![](images/moon.png)

![](images/sky.png)
:::

::: footer
Learn more: [Themes](https://{{< meta prerelease-subdomain >}}quarto.org/docs/presentations/revealjs/themes.html)
:::

## Easy Navigation

::: {style="margin-bottom: 0.9em;"}
Quickly jump to other parts of your presentation
:::

::: {layout="[1, 20]"}
![](images/presentation-menu.png){width="41"}

Toggle the slide menu with the menu button (bottom left of slide) to go to other slides and access presentation tools.
:::

You can also press {{< kbd m >}} to toggle the menu open and closed.

You can also press {{< kbd g >}} to toggle 'Jump To Slide' modal box to quickly go to one of your slide using its number or id.

::: footer
Learn more: [Navigation](/docs/presentations/revealjs/presenting.qmd#navigation-menu) / [Jump To Slide](/docs/presentations/revealjs/presenting.qmd#jump-to-slide)
:::

## Jump To Slide

::: {style="margin-bottom: 0.9em;"}
Quickly jump to other parts of your presentation
:::

## Chalkboard {chalkboard-buttons="true"}

::: {style="margin-bottom: 0.9em;"}
Free form drawing and slide annotations
:::

::: {layout="[1, 20]"}
![](images/presentation-chalkboard.png){width="41"}

Use the chalkboard button at the bottom left of the slide to toggle the chalkboard.
:::

::: {layout="[1, 20]"}
![](images/presentation-notes-canvas.png){width="41"}

Use the notes canvas button at the bottom left of the slide to toggle drawing on top of the current slide.
:::

You can also press {{< kbd b >}} to toggle the chalkboard or {{< kbd c >}} to toggle the notes canvas.

::: footer
Learn more: [Chalkboard](https://{{< meta prerelease-subdomain >}}quarto.org/docs/presentations/revealjs/presenting.html#chalkboard)
:::

## Point of View

press {{< kbd o >}} to toggle overview mode:

![](images/overview-mode.png){.border}

Hold down the {{< kbd Alt linux=Ctrl >}} and click on any element to zoom towards it---try it now on this slide.

::: footer
Learn more: [Overview Mode](https://{{< meta prerelease-subdomain >}}quarto.org/docs/presentations/revealjs/presenting.html#overview-mode), [Slide Zoom](https://{{< meta prerelease-subdomain >}}quarto.org/docs/presentations/revealjs/presenting.html#slide-zoom)
:::

## Speaker View

press {{< kbd s >}} (or use the tools in presentation menu ![](../images/navigation-menu-icon.png){style="padding-bottom: 1px; margin: 0" width="0.5em" height="0.5em"}) to open speaker view

![](images/speaker-view.png){fig-align="center" style="border: 3px solid #dee2e6;" width="780"}

::: footer
Learn more: [Speaker View](https://{{< meta prerelease-subdomain >}}quarto.org/docs/presentations/revealjs/presenting.html#speaker-view)
:::

## Scroll View {#scroll-view}

Press {{< kbd r >}} (or use the tools in presentation menu ![](../images/navigation-menu-icon.png){style="padding-bottom: 1px; margin: 0" width="0.5em" height="0.5em"}) to open scroll view

Try it now on this slide --- You'll see a scroll bar on the right and you can scroll down the presentation using your mouse.

Scroll view behavior can be configured using `scroll-view` configuration. 

::: footer
Learn more: [Scroll View](https://{{< meta prerelease-subdomain >}}quarto.org/docs/presentations/revealjs/presenting.html#scroll-view)
:::

## Authoring Tools {.smaller}

Live side-by-side preview for any notebook or text editor including Jupyter and VS Code

::: columns
::: {.column width="50%"}
![](images/jupyter-edit.png){.border .border-thick}
:::

::: {.column width="50%"}
![](images/jupyter-preview.png){.border .border-thick}
:::
:::

::: footer
Learn more: [Jupyter](https://{{< meta prerelease-subdomain >}}quarto.org/docs/tools/jupyter-lab.html), [VS Code](https://{{< meta prerelease-subdomain >}}quarto.org/docs/tools/vscode.html), [Text Editors](https://{{< meta prerelease-subdomain >}}quarto.org/docs/tools/text-editors.html)
:::

## Authoring Tools {.smaller}

RStudio includes an integrated presentation preview pane

![](images/rstudio.png){.border width="900"}

::: footer
Learn more: [RStudio](https://{{< meta prerelease-subdomain >}}quarto.org/docs/tools/rstudio.html)
:::

## And More...

-   [Touch](https://{{< meta prerelease-subdomain >}}quarto.org/docs/presentations/revealjs/advanced.html#touch-navigation) optimized (presentations look great on mobile, swipe to navigate slides)
-   [Footer & Logo](https://{{< meta prerelease-subdomain >}}quarto.org/docs/presentations/revealjs/#footer-logo) (optionally specify custom footer per-slide or hide global footer)
-   [Auto-Slide](https://{{< meta prerelease-subdomain >}}quarto.org/docs/presentations/revealjs/presenting.html#auto-slide) (step through slides automatically, without any user input)
-   [Multiplex](https://{{< meta prerelease-subdomain >}}quarto.org/docs/presentations/revealjs/presenting.html#multiplex) (allows your audience to follow the slides of the presentation you are controlling on their own phone, tablet or laptop).

::: footer
Learn more: [Quarto Presentations](https://{{< meta prerelease-subdomain >}}quarto.org/docs/presentations/revealjs/)
:::



--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/mini/README.md:
--------------------------------------------------------------------------------
## Revealjs Mini Demos

This folder contains the source code for the embedded mini demos used in the Quarto [Revealjs documentation](https://quarto.org/docs/presentation/revealjs/).



--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/mini/_metadata.yml:
--------------------------------------------------------------------------------
format: 
  revealjs:
    controls: true
    menu: false
    progress: false
search: false



--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/mini/absolute.qmd:
--------------------------------------------------------------------------------
## Absolute

![](images/kitten-350-300.jpeg){.absolute top="200" left="0" width="350" height="300"}

![](images/kitten-450-250.jpeg){.absolute top="50" right="50" width="450" height="250"}

![](images/kitten-300-300.jpeg){.absolute bottom="20" right="100" width="300" height="300"}



--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/mini/auto-animate-code.qmd:
--------------------------------------------------------------------------------
---
format: 
  revealjs:
    width: 650
    height: 300
---

##  {auto-animate="true"}

``` r
# Fill in the spot we created for a plot
output$phonePlot <- renderPlot({
  # Render a barplot
})
```

##  {auto-animate="true"}

``` r
# Fill in the spot we created for a plot
output$phonePlot <- renderPlot({
  # Render a barplot
  barplot(WorldPhones[,input$region]*1000, 
          main=input$region,
          ylab="Number of Telephones",
          xlab="Year")
})
```



--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/mini/auto-animate-movement.qmd:
--------------------------------------------------------------------------------
---
format: 
  revealjs:
    width: 650
    height: 300
---

##  {auto-animate="true"}

Animation

##  {auto-animate="true"}

Implicit

Animation



--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/mini/auto-animate-stack.qmd:
--------------------------------------------------------------------------------
--- 
format: 
  revealjs:
    width: 1050
    height: 500
---

## Element Matching  with `data-id` {auto-animate=true auto-animate-easing="ease-in-out"}

::: {.r-hstack style="margin-top: 1em;"}
::: {data-id="box1" auto-animate-delay="0" style="background: #2780e3; width: 200px; height: 150px; margin: 10px;"}
:::

::: {data-id="box2" auto-animate-delay="0.1" style="background: #3fb618; width: 200px; height: 150px; margin: 10px;"}
:::

::: {data-id="box3" auto-animate-delay="0.2" style="background: #e83e8c; width: 200px; height: 150px; margin: 10px;"}
:::
:::

## Element Matching  with `data-id` {auto-animate=true auto-animate-easing="ease-in-out"}

::: {.r-stack style="margin-top: 1em;"}
::: {data-id="box1" style="background: #2780e3; width: 350px; height: 350px; border-radius: 200px;"}
:::

::: {data-id="box2" style="background: #3fb618; width: 250px; height: 250px; border-radius: 200px;"}
:::

::: {data-id="box3" style="background: #e83e8c; width: 150px; height: 150px; border-radius: 200px;"}
:::
:::



--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/mini/auto-animate.qmd:
--------------------------------------------------------------------------------
##  {auto-animate="true"}

::: {style="margin-top: 100px;"}
Animating content
:::

##  {auto-animate="true"}

::: {style="margin-top: 200px; font-size: 3em; color: red;"}
Animating content
:::



--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/mini/custom-blur.css:
--------------------------------------------------------------------------------
.reveal .slides section .fragment.blur {
  filter: blur(5px);
}

.reveal .slides section .fragment.blur.visible {
  filter: none
}


--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/mini/fragments-custom.qmd:
--------------------------------------------------------------------------------
---
format: 
  revealjs: 
    css: custom-blur.css
---

### Advance the slide to see custom fragment style (from blurred to focus)

<br/>

::: {.fragment .custom .blur}
First item to be unblurred
:::

::: {.fragment .custom .blur}
Second one to be revealed
:::



--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/mini/fragments-nested.qmd:
--------------------------------------------------------------------------------
---
format: revealjs
---

### Advance the slide to see three different fragment states:

<br/>

::: {.fragment .fade-in}
::: {.fragment .highlight-red}
::: {.fragment .semi-fade-out}
Fade in > Turn red > Semi fade out
:::
:::
:::



--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/mini/fragments.qmd:
--------------------------------------------------------------------------------
## Fragments

Click the arrow to advance through the fragments:

::: {style="margin-top: 2em; margin-left: 1em;"}
::: fragment
Fade in
:::

::: {.fragment .fade-out}
Fade out
:::

::: {.fragment .highlight-red}
Highlight red
:::

::: {.fragment .fade-in-then-out}
Fade in, then out
:::

::: {.fragment .fade-up}
Slide up while fading in
:::
:::



--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/mini/images/kitten-300-200.jpeg:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/demo/mini/images/kitten-300-200.jpeg


--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/mini/images/kitten-300-300.jpeg:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/demo/mini/images/kitten-300-300.jpeg


--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/mini/images/kitten-300-450.jpeg:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/demo/mini/images/kitten-300-450.jpeg


--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/mini/images/kitten-350-300.jpeg:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/demo/mini/images/kitten-350-300.jpeg


--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/mini/images/kitten-375-300.jpeg:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/demo/mini/images/kitten-375-300.jpeg


--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/mini/images/kitten-400-350.jpeg:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/demo/mini/images/kitten-400-350.jpeg


--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/mini/images/kitten-400-400.jpeg:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/demo/mini/images/kitten-400-400.jpeg


--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/mini/images/kitten-450-200.jpeg:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/demo/mini/images/kitten-450-200.jpeg


--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/mini/images/kitten-450-250.jpeg:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/demo/mini/images/kitten-450-250.jpeg


--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/mini/images/kitten-450-300.jpeg:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/demo/mini/images/kitten-450-300.jpeg


--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/mini/images/kitten-450-350.jpeg:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/demo/mini/images/kitten-450-350.jpeg


--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/mini/stack.qmd:
--------------------------------------------------------------------------------
---
format: revealjs
---

## Stack

Click the arrow to advance to the next image in the stack.

::: r-stack
![](images/kitten-450-300.jpeg){.fragment width="450" height="300"}

![](images/kitten-300-450.jpeg){.fragment width="300" height="450"}

![](images/kitten-400-400.jpeg){.fragment width="400" height="400"}
:::



--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/mini/zoom.qmd:
--------------------------------------------------------------------------------
---
format: revealjs
---

![](images/kitten-375-300.jpeg){.absolute top="175" left="0" width="375" height="300"}

![](images/kitten-450-200.jpeg){.absolute top="50" right="50" width="450" height="250"}

![](images/kitten-300-300.jpeg){.absolute bottom="20" right="100" width="300" height="300"}



--------------------------------------------------------------------------------
/docs/presentations/revealjs/demo/styles.css:
--------------------------------------------------------------------------------


.border {
  border: 1px solid #dee2e6;
}

.border-thick {
  border-width: 3px;
}



--------------------------------------------------------------------------------
/docs/presentations/revealjs/examples/_metadata.yml:
--------------------------------------------------------------------------------
format: 
  revealjs:
    controls: true
    menu: false
    progress: false
    width: 1050
    height: 300
search: false



--------------------------------------------------------------------------------
/docs/presentations/revealjs/examples/_theme-dark.qmd:
--------------------------------------------------------------------------------
---
title: "Presentation"
format:
  revealjs:
    theme: dark
---

## Slide 1

* Eat spaghetti
* Drink wine




--------------------------------------------------------------------------------
/docs/presentations/revealjs/examples/background-color.qmd:
--------------------------------------------------------------------------------
---
format: revealjs
---

## Slide, `aquamarine` {background-color="aquamarine"}

## Slide, `#806040` {background-color="#806040"}



--------------------------------------------------------------------------------
/docs/presentations/revealjs/examples/background-gradient.qmd:
--------------------------------------------------------------------------------
---
format: revealjs
---

## Slide with linear-gradient {background-gradient="linear-gradient(to bottom, #283b95, #17b2c3)"}

## Slide with radial-gradient {background-gradient="radial-gradient(#283b95, #17b2c3)"}



--------------------------------------------------------------------------------
/docs/presentations/revealjs/examples/background-no-title.qmd:
--------------------------------------------------------------------------------
---
format: revealjs
---

## {background-color="aquamarine"}

(A slide with no title)

## {background-color="black" background-image="https://placekitten.com/100/100" background-size="100px" background-repeat="repeat"}

(Another slide with no title)



--------------------------------------------------------------------------------
/docs/presentations/revealjs/examples/code-echo.qmd:
--------------------------------------------------------------------------------
---
format:
  revealjs:
    height: 500
---

```{python}
#| echo: true
#| fig-align: center

import numpy as np
import matplotlib.pyplot as plt

r = np.arange(0, 2, 0.01)
theta = 2 * np.pi * r
fig, ax = plt.subplots(subplot_kw={"projection": "polar"})
ax.plot(theta, r)
ax.set_rticks([0.5, 1, 1.5, 2])
ax.grid(True)
plt.show()
```



--------------------------------------------------------------------------------
/docs/presentations/revealjs/examples/columns.qmd:
--------------------------------------------------------------------------------
---
format: 
  revealjs
---

:::: {.columns}

::: {.column width="40%"}
Left column
:::

::: {.column width="60%"}
Right column
:::

::::



--------------------------------------------------------------------------------
/docs/presentations/revealjs/examples/creating-slides-1.qmd:
--------------------------------------------------------------------------------
---
title: "Habits"
author: "John Doe"
format: revealjs
---

## Getting up

- Turn off alarm
- Get out of bed

## Going to sleep

- Get in bed
- Count sheep



--------------------------------------------------------------------------------
/docs/presentations/revealjs/examples/creating-slides-2.qmd:
--------------------------------------------------------------------------------
---
title: "Habits"
author: "John Doe"
format: revealjs
---

# In the morning

## Getting up

- Turn off alarm
- Get out of bed

## Breakfast

- Eat eggs
- Drink coffee

# In the evening

## Dinner

- Eat spaghetti
- Drink wine

## Going to sleep

- Get in bed
- Count sheep



--------------------------------------------------------------------------------
/docs/presentations/revealjs/examples/creating-slides-3.qmd:
--------------------------------------------------------------------------------
---
title: "Habits"
author: "John Doe"
format: revealjs
---

- Turn off alarm
- Get out of bed

---

- Get in bed
- Count sheep



--------------------------------------------------------------------------------
/docs/presentations/revealjs/examples/executable-code-figure-size.qmd:
--------------------------------------------------------------------------------
---
format: revealjs
---

```{python}
#| echo: false
import altair as alt
from vega_datasets import data
cars = data.cars()
```

```{python}
alt.Chart(cars).mark_point().encode(
    x='Horsepower',
    y='Miles_per_Gallon',
    color='Origin',
).properties(
    width=700,
    height=300
).interactive()
```



--------------------------------------------------------------------------------
/docs/presentations/revealjs/examples/footer-and-logo.qmd:
--------------------------------------------------------------------------------
---
format:
  revealjs:
    logo: ../../../../quarto.png
    footer: "Footer text"
---

## Slide 1

Footer and logo are shared across all slides.

## Slide 2



--------------------------------------------------------------------------------
/docs/presentations/revealjs/examples/image-background.qmd:
--------------------------------------------------------------------------------
---
format: revealjs
---

## Slide Title {background-color="black" background-image='{{< placeholder 100 100 >}}' background-size="100px" background-repeat="repeat"}

This slide's background image will be sized to 100px and repeated.



--------------------------------------------------------------------------------
/docs/presentations/revealjs/examples/incremental-lists-1.qmd:
--------------------------------------------------------------------------------
---
format:
  revealjs:
    incremental: true   
---

## Slide 1

- incremental list, 1
- incremental list, 2

## Slide 2

- incremental list, 3
- incremental list, 4



--------------------------------------------------------------------------------
/docs/presentations/revealjs/examples/incremental-lists-2.qmd:
--------------------------------------------------------------------------------
---
format: revealjs
---

## Slide 1, incrementally

::: {.incremental}

- Eat spaghetti
- Drink wine

:::

## Slide 2, non-incrementally

- Eat spaghetti
- Drink wine





--------------------------------------------------------------------------------
/docs/presentations/revealjs/examples/incremental-lists-3.qmd:
--------------------------------------------------------------------------------
---
format: 
  revealjs:
    incremental: true
---

## Slide 1, incrementally

- Eat spaghetti
- Drink wine

## Slide 2, non-incrementally

::: {.nonincremental}
- Eat spaghetti
- Drink wine
:::



--------------------------------------------------------------------------------
/docs/presentations/revealjs/examples/incremental-pause.qmd:
--------------------------------------------------------------------------------
## Slide with a pause

content before the pause

. . .

content after the pause



--------------------------------------------------------------------------------
/docs/presentations/revealjs/examples/index.qmd:
--------------------------------------------------------------------------------
---
title: All revealjs examples
format:
  revealjs: 
    slide-level: 0
    slide-number: c/t
# listing: default
---

````{r}
#| echo: false
#| output: asis
files <- fs::dir_ls('.', regexp = '^[^_].*[.]qmd$', all = TRUE)
files <- files[!files %in% c("index.qmd")]
links <- glue::glue("* [{fs::path_ext_remove(files)}]({files})")

bucket_size <- 5
buckets <- split(links, ceiling(seq_along(links) / bucket_size))

# Add new slides after each bucket except last
for (i in 1:(length(buckets)-1)) {
  buckets[[i]] <- c(buckets[[i]], "", "----", "")
}

purrr::map(buckets, \(x) {
  glue::glue("
{glue::glue_collapse(x, sep = '\n')}
")
}) |> unlist() |> cat(sep = "\n")

````



--------------------------------------------------------------------------------
/docs/presentations/revealjs/examples/line-highlighting-1.qmd:
--------------------------------------------------------------------------------
---
format: revealjs
---

```{.python code-line-numbers="6-8"}
import numpy as np
import matplotlib.pyplot as plt

r = np.arange(0, 2, 0.01)
theta = 2 * np.pi * r
fig, ax = plt.subplots(subplot_kw={'projection': 'polar'})
ax.plot(theta, r)
ax.set_rticks([0.5, 1, 1.5, 2])
ax.grid(True)
plt.show()
```



--------------------------------------------------------------------------------
/docs/presentations/revealjs/examples/line-highlighting-2.qmd:
--------------------------------------------------------------------------------
---
format: revealjs
---

```{.python code-line-numbers="7,9"}
import numpy as np
import matplotlib.pyplot as plt

r = np.arange(0, 2, 0.01)
theta = 2 * np.pi * r
fig, ax = plt.subplots(subplot_kw={'projection': 'polar'})
ax.plot(theta, r)
ax.set_rticks([0.5, 1, 1.5, 2])
ax.grid(True)
plt.show()
```



--------------------------------------------------------------------------------
/docs/presentations/revealjs/examples/line-highlighting-3.qmd:
--------------------------------------------------------------------------------
---
format: revealjs
---

```{.python code-line-numbers="|6|9"}
import numpy as np
import matplotlib.pyplot as plt

r = np.arange(0, 2, 0.01)
theta = 2 * np.pi * r
fig, ax = plt.subplots(subplot_kw={'projection': 'polar'})
ax.plot(theta, r)
ax.set_rticks([0.5, 1, 1.5, 2])
ax.grid(True)
plt.show()
```



--------------------------------------------------------------------------------
/docs/presentations/revealjs/examples/line-highlighting-4.qmd:
--------------------------------------------------------------------------------
---
format:
  revealjs:
    height: 450
---

```{python}
#| echo: true
#| code-line-numbers: "|6|9"

import numpy as np
import matplotlib.pyplot as plt

r = np.arange(0, 2, 0.01)
theta = 2 * np.pi * r
fig, ax = plt.subplots(subplot_kw={'projection': 'polar'})
ax.plot(theta, r)
ax.set_rticks([0.5, 1, 1.5, 2])
ax.grid(True)
plt.show()
```



--------------------------------------------------------------------------------
/docs/presentations/revealjs/examples/no-footer-on-a-slide.qmd:
--------------------------------------------------------------------------------
---
format:
  revealjs:
    footer: "Footer text"
---

## Slide 1

Footer is shown on all slides

## Slide 2 {footer=false}

unless `{footer=false}` is set


--------------------------------------------------------------------------------
/docs/presentations/revealjs/examples/per-slide-footer.qmd:
--------------------------------------------------------------------------------
---
format:
  revealjs:
    logo: ../../../../quarto.png
---

## Slide Title

Slide content

::: footer
Custom footer text
:::

## Another Slide Title

::: footer
A different custom footer
:::



--------------------------------------------------------------------------------
/docs/presentations/revealjs/examples/scrollable-and-smaller.qmd:
--------------------------------------------------------------------------------
---
format:
  revealjs:
    smaller: true
    scrollable: true
---

## Slide 1

* Bullet Point 1
* Bullet Point 2
* Bullet Point 3
* Bullet Point 4
* Bullet Point 5
* Bullet Point 6
* Bullet Point 7
* Bullet Point 8
* Bullet Point 9
* Bullet Point 10
* Bullet Point 11
* Bullet Point 12
* Bullet Point 13
* Bullet Point 14
* Bullet Point 15
* Bullet Point 16

## Slide 2

* Bullet Point 1
* Bullet Point 2
* Bullet Point 3
* Bullet Point 4
* Bullet Point 5
* Bullet Point 6
* Bullet Point 7
* Bullet Point 8
* Bullet Point 9
* Bullet Point 10
* Bullet Point 11
* Bullet Point 12
* Bullet Point 13
* Bullet Point 14
* Bullet Point 15
* Bullet Point 16



--------------------------------------------------------------------------------
/docs/presentations/revealjs/examples/scrollable.qmd:
--------------------------------------------------------------------------------
---
format: revealjs
---

## Non-scrollable Slide

* Bullet Point 1
* Bullet Point 2
* Bullet Point 3
* Bullet Point 4
* Bullet Point 5
* Bullet Point 6
* Bullet Point 7
* Bullet Point 8
* Bullet Point 9
* Bullet Point 10
* Bullet Point 11
* Bullet Point 12
* Bullet Point 13
* Bullet Point 14
* Bullet Point 15
* Bullet Point 16

## Scrollable Slide {.scrollable}

* Bullet Point 1
* Bullet Point 2
* Bullet Point 3
* Bullet Point 4
* Bullet Point 5
* Bullet Point 6
* Bullet Point 7
* Bullet Point 8
* Bullet Point 9
* Bullet Point 10
* Bullet Point 11
* Bullet Point 12
* Bullet Point 13
* Bullet Point 14
* Bullet Point 15
* Bullet Point 16



--------------------------------------------------------------------------------
/docs/presentations/revealjs/examples/slide-with-speaker-notes.qmd:
--------------------------------------------------------------------------------
---
format:
  revealjs
---

## Slide with speaker notes

Slide content

::: {.notes}
Speaker notes go here.
:::



--------------------------------------------------------------------------------
/docs/presentations/revealjs/examples/smaller.qmd:
--------------------------------------------------------------------------------
---
format: revealjs
---

## Slide Title (without `.smaller`)

* Bullet Point 1
* Bullet Point 2

## Slide Title (with `.smaller`) {.smaller}

* Bullet Point 1
* Bullet Point 2



--------------------------------------------------------------------------------
/docs/presentations/revealjs/examples/tabset.qmd:
--------------------------------------------------------------------------------
---
format: revealjs
---

## Title

::: {.panel-tabset}

### Tab A

Content for `Tab A`

### Tab B

Content for `Tab B`

:::



--------------------------------------------------------------------------------
/docs/presentations/revealjs/images/canvas-icon.png:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/images/canvas-icon.png


--------------------------------------------------------------------------------
/docs/presentations/revealjs/images/chalkboard-icon.png:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/images/chalkboard-icon.png


--------------------------------------------------------------------------------
/docs/presentations/revealjs/images/chalkboard.png:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/images/chalkboard.png


--------------------------------------------------------------------------------
/docs/presentations/revealjs/images/drawing-canvas.png:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/images/drawing-canvas.png


--------------------------------------------------------------------------------
/docs/presentations/revealjs/images/footnote.png:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/images/footnote.png


--------------------------------------------------------------------------------
/docs/presentations/revealjs/images/line-highlight-discontinuous.png:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/images/line-highlight-discontinuous.png


--------------------------------------------------------------------------------
/docs/presentations/revealjs/images/line-highlight.png:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/images/line-highlight.png


--------------------------------------------------------------------------------
/docs/presentations/revealjs/images/matplotlib.png:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/images/matplotlib.png


--------------------------------------------------------------------------------
/docs/presentations/revealjs/images/navigation-menu-button.png:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/images/navigation-menu-button.png


--------------------------------------------------------------------------------
/docs/presentations/revealjs/images/navigation-menu-icon.png:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/images/navigation-menu-icon.png


--------------------------------------------------------------------------------
/docs/presentations/revealjs/images/navigation-menu-open.png:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/images/navigation-menu-open.png


--------------------------------------------------------------------------------
/docs/presentations/revealjs/images/overview-mode.png:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/images/overview-mode.png


--------------------------------------------------------------------------------
/docs/presentations/revealjs/images/print-to-pdf.png:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/images/print-to-pdf.png


--------------------------------------------------------------------------------
/docs/presentations/revealjs/images/reveal.js-vertical-slides.gif:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/images/reveal.js-vertical-slides.gif


--------------------------------------------------------------------------------
/docs/presentations/revealjs/images/speaker-view.png:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/quarto-dev/quarto-web/main/docs/presentations/revealjs/images/speaker-view.png


--------------------------------------------------------------------------------
/docs/presentations/revealjs/index.qmd:
--------------------------------------------------------------------------------
---
title: "Revealjs"
slide-format: revealjs
---

## Overview

You can create [Revealjs](https://revealjs.com/) presentations using the `revealjs` format. The best way to get a sense for the capabilities of Revealjs is this [demo](demo/){target="_blank"} presentation:

<div>

```{=html}
<iframe class="slide-deck" src="demo/"></iframe>
```

</div>

If you prefer to view the demo in a standalone browser you can do that [here](demo/){target="_blank"}. Check out the [source code](https://github.com/quarto-dev/quarto-web/blob/main/docs/presentations/revealjs/demo/index.qmd) for the demo to see how the slides were created.

See the Revealjs [format reference](/docs/reference/formats/presentations/revealjs.qmd) for a comprehensive overview of all options supported for Revealjs output.

{{< include ../_creating-slides-reveal.md >}}

{{< include ../_incremental-lists-reveal.md >}}

{{< include ../_incremental-pause-reveal.md >}}

{{< include ../_columns-reveal.md >}}


## Content Overflow

If you have a slide that has more content than can be displayed on a single frame there are two slide-level classes you can apply to mitigate this:

1.  Use the `.smaller` class to use a smaller typeface so that more text fits on the slide. For example:

    ``` {.markdown code-preview="examples/smaller.qmd"}
    ## Slide Title {.smaller}
    ```

2.  Use the `.scrollable` class to make off-slide content available by scrolling. For example:

    ``` {.markdown code-preview="examples/scrollable.qmd"}
    ## Slide Title {.scrollable}
    ```

Both of these options can also be applied globally to all slides as follows:

``` {.yaml code-preview="examples/scrollable-and-smaller.qmd"}
---
format:
  revealjs:
    smaller: true
    scrollable: true
---
```

Please note that section title slides are centered by default which prevents them from being scrollable.
If you want to make title slides scrollable, you need to make them non-centered.

``` {.yaml}
---
format:
  revealjs:
    scrollable: true
    center-title-slide: false
---
```

{{< include _callout-auto-stretch-scrollable.qmd >}}

{{< include ../_speaker-notes.md >}}

This is a Revealjs feature from [built-in plugin](https://revealjs.com/plugins/#built-in-plugins) which brings limitation:  the content cannot rely on external dependencies. For instance, if you want to include a mermaid diagram that typically needs mermaid.js, it will need to be embed as an SVG or PNG image.

Press the <kbd>S</kbd> key (or use the [Navigation Menu](presenting.qmd#navigation-menu)) to show the presentation speaker view:

![](images/speaker-view.png){.border fig-alt="Screenshot of reveal.js presentation in Speaker View. On the right, the active slide is shown. The left column contains three sections which show (from top to bottom): the upcoming slide, time (both elapsed and clock time), and a section where speaker notes go."}

You'll typically use this view on one screen (e.g. your laptop) while presenting the slides on another screen.

## Themes

{{< include _theme-basics.md >}}


See the article on [Reveal Themes](themes.qmd) for additional details on customizing themes and creating brand new themes of your own.

## Asides & Footnotes

Asides contain content of more peripheral interest, and are displayed in a smaller, lighter font at the bottom of the slide. Creates asides using a div with the `aside` class. For example:

``` markdown
## Slide Title

Slide content

::: aside
Some additional commentary of more peripheral interest.
:::
```

Footnotes have a similar visual treatment to asides, but include a footnote number. For example, here we use a footnote and an aside on a single slide:

``` markdown
## Slide Title

- Green ^[A footnote]
- Brown
- Purple

::: aside
Some additional commentary of more peripheral interest.
:::
```

Which looks like this when rendered:

![](images/footnote.png){.border fig-alt="Rendered slide with title at the top, followed by a bulleted list (the first item of which has a footnote). The bottom of the slide shows the aside (Some additional commentary of more peripheral interest.), and below that the footnote."}

If you prefer that footnotes be included at the end of the document, specify the `reference-location: document` option:

``` yaml
---
format:
  revealjs:
    reference-location: document
---
```

Note that when specifying this option footnotes can still be viewed while on the slide by hovering over the footnote number.

## Footer & Logo

You can include footer text and a logo at the bottom of each slide using the `footer` and `logo` options. For example:

``` {.yaml code-preview="examples/footer-and-logo.qmd"}
---
format:
  revealjs:
    logo: logo.png
    footer: "Footer text"
---
```

Using `{footer=false}` on a slide heading allows to remove the presentation footer for this slide.

```{.yaml code-preview="examples/no-footer-on-a-slide.qmd"}
---
format:
  revealjs:
    footer: "Footer text"
---

## Slide with default footer

Content

## No footer {footer=false}

No footer is shown on this slide
```

You can also include a custom footer per-slide by adding a footer div at the bottom of the slide. 

``` {.markdown code-preview="examples/per-slide-footer.qmd"}
## Slide Title

Slide content

::: footer
Custom footer text
:::
```

## Code Blocks

Most of the core capabilities of Quarto [HTML Code Blocks](/docs/output-formats/html-code.qmd) are available for Reveal slides, including code folding, code copy, and the ability to pick a custom syntax highlighting theme. Note that if you choose a dark Reveal theme then the default Quarto dark syntax highlighting theme will be used.

### Line Highlighting

You may want to highlight specific lines of code output (or even highlight distinct lines over a progression of steps). You can do this using the `code-line-numbers` attribute of code blocks. For example:

```` {.java code-preview="examples/line-highlighting-1.qmd"}
```{.python code-line-numbers="6-8"}
import numpy as np
import matplotlib.pyplot as plt

r = np.arange(0, 2, 0.01)
theta = 2 * np.pi * r
fig, ax = plt.subplots(subplot_kw={'projection': 'polar'})
ax.plot(theta, r)
ax.set_rticks([0.5, 1, 1.5, 2])
ax.grid(True)
plt.show()
```
````

Note that you can also highlight disparate ranges of lines by separating them with a comma. For example:

```` {.java code-preview="examples/line-highlighting-2.qmd"}
```{.python code-line-numbers="7,9"}
import numpy as np
import matplotlib.pyplot as plt

r = np.arange(0, 2, 0.01)
theta = 2 * np.pi * r
fig, ax = plt.subplots(subplot_kw={'projection': 'polar'})
ax.plot(theta, r)
ax.set_rticks([0.5, 1, 1.5, 2])
ax.grid(True)
plt.show()
```
````

Finally, you can highlight different line ranges progressively by separating them with `|`. For example, here we start by showing all lines, then progress to highlighting line 6, and finally to highlighting line 9:

```` {.java code-preview="examples/line-highlighting-3.qmd"}
```{.python code-line-numbers="|6|9"}
import numpy as np
import matplotlib.pyplot as plt

r = np.arange(0, 2, 0.01)
theta = 2 * np.pi * r
fig, ax = plt.subplots(subplot_kw={'projection': 'polar'})
ax.plot(theta, r)
ax.set_rticks([0.5, 1, 1.5, 2])
ax.grid(True)
plt.show()
```
````

You can use this same option within an executable code cell by using the `code-line-numbers` cell options:

```` {.java code-preview="examples/line-highlighting-4.qmd"}
```{{python}}
#| code-line-numbers: "|6|9"

import numpy as np
import matplotlib.pyplot as plt

r = np.arange(0, 2, 0.01)
theta = 2 * np.pi * r
fig, ax = plt.subplots(subplot_kw={'projection': 'polar'})
ax.plot(theta, r)
ax.set_rticks([0.5, 1, 1.5, 2])
ax.grid(True)
plt.show()
```
````

### Code Block Height

By default, code blocks are limited to a maximum height of 500px. Code that exceeds this height introduces a scrollbar. To avoid a scrollbar you can increase the maximum height with the `code-block-height` option:

```{.yaml}
---
format:
  revealjs: 
    code-block-height: 650px
---
```

## Executable Code

You can include the output of executable code blocks on slides just the same as with other Quarto documents. This works essentially the same for slides as it does for other formats, however there are a couple of special considerations for slides covered below.

### Figure Size

You will frequently need to customize the size of figures created for slides so that they either fill the entire slide or whatever region of the slide you need them to. Quarto provides some help here: for Python the figure sizes for [Matplotlib](https://matplotlib.org/) and [Plotly Express](https://plotly.com/python/plotly-express/) are set to fill the slide area below the title, and for R the Knitr figure width and height are similarly defaulted.

Nevertheless, you will frequently need to change these defaults for a given figure. The details on how to do this vary by graphics library. Here's an example of explicitly sizing an [Altair](https://altair-viz.github.io/) plot:

``` {.python code-preview="examples/executable-code-figure-size.qmd"}
alt.Chart(cars).mark_point().encode(
    x='Horsepower',
    y='Miles_per_Gallon',
    color='Origin',
).properties(
    width=700,
    height=300
).interactive()
```

### Code Echo

Unlike with ordinary documents, within Quarto presentations executable code blocks do not `echo` their source code by default (this is because often the code produces a figure that wants to occupy as much vertical space as possible). You can override this behavior using the `echo` option. For example:

```` {.java code-preview="examples/code-echo.qmd"}
```{{python}}
#| echo: true

import numpy as np
import matplotlib.pyplot as plt

r = np.arange(0, 2, 0.01)
theta = 2 * np.pi * r
fig, ax = plt.subplots(subplot_kw={"projection": "polar"})
ax.plot(theta, r)
ax.set_rticks([0.5, 1, 1.5, 2])
ax.grid(True)
plt.show()
```
````

### Output Location

By default, output from executable code blocks is displayed immediately after the code. You can use the `output-location` option to modify this behavior as follows:

|                   |                                                                                                                                         |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `fragment`        | Display output as a [Fragment](advanced.qmd#fragments) (delay showing it until it is explicitly stepped through by advancing the slide). |
| `slide`           | Display output on the subsequent slide.                                                                          |
| `column`          | Display output in a column adjacent to the code.                                                                                        |
| `column-fragment` | Display output in a column adjacent to the code and delay showing it until it is explicitly stepped through by advancing the slide.        |

For example, here we display cell output on its own slide:

```{{r}}
#| echo: true
#| output-location: slide
library(ggplot2)
ggplot(airquality, aes(Temp, Ozone)) + 
  geom_point() + 
  geom_smooth(method = "loess")
```

See the documentation on [Execution Options](/docs/computations/execution-options.qmd) for more details on the various other ways to customize output from code execution.

## Tabsets

You can add tabbed content to slides using the standard Quarto syntax for [tabsets](/docs/output-formats/html-basics.qmd#tabsets). For example:

``` {.markdown code-preview="examples/tabset.qmd"}
::: {.panel-tabset}

### Tab A

Content for `Tab A`

### Tab B

Content for `Tab B`

:::
```

Note that one significant disadvantage to tabsets is that only the first tab will be visible when printing to PDF.

## Slide Backgrounds

Slides are contained within a limited portion of the screen by default to allow them to fit any display and scale uniformly. You can apply full page backgrounds outside of the slide area by adding a `background` attribute to your slide headings. Five different types of backgrounds are supported: color, gradient, image, video and iframe.

### Color Background

All CSS color formats are supported, including hex values, keywords, `rgba()` or `hsl()`. For example:

``` {.markdown code-preview="examples/background-color.qmd"}
## Slide Title {background-color="aquamarine"}
```

::: {.callout-tip appearance="simple"}
Note that if the background color of your media differs from your presentation's theme (e.g. a dark image when using a light theme) then you should also explicitly set the `background-color` so that text on top of the background appears in the correct color (e.g. light text on a dark background).
:::

### Gradient Background

{{< include /docs/prerelease/1.6/_pre-release-feature.qmd >}}

All CSS gradient formats are supported, including `linear-gradient`, `radial-gradient` and `conic-gradient`.

```{.markdown code-preview="examples/background-gradient.qmd"}
## Slide Title {background-gradient="linear-gradient(to bottom, #283b95, #17b2c3)"}

## Slide Title {background-gradient="radial-gradient(#283b95, #17b2c3)"}
```

### Image Backgrounds

By default, background images are resized to cover the full page. Available options:

| **Attribute**         | **Default** | **Description**                                                                                   |
|:----------------------|:------------|:--------------------------------------------------------------------------------------------------|
| `background-image`    |             | URL of the image to show. GIFs restart when the slide opens.                                      |
| `background-size`     | cover       | See [background-size](https://developer.mozilla.org/docs/Web/CSS/background-size) on MDN.         |
| `background-position` | center      | See [background-position](https://developer.mozilla.org/docs/Web/CSS/background-position) on MDN. |
| `background-repeat`   | no-repeat   | See [background-repeat](https://developer.mozilla.org/docs/Web/CSS/background-repeat) on MDN.     |
| `background-opacity`  | 1           | Opacity of the background image on a 0-1 scale. 0 is transparent and 1 is fully opaque.           |

For example:

``` {.markdown code-preview="examples/image-background.qmd"}
## Slide Title {background-color="black" background-image="https://placekitten.com/100/100" background-size="100px" background-repeat="repeat"}

This slide's background image will be sized to 100px and repeated.
```

Since this image has a dark background and our slides use the default (light) theme, we explicitly set the `background-color` to black so that text drawn on top of it is light.

### Video Backgrounds

Automatically plays a full size video behind the slide.


{{< include _background-video.md >}}

### IFrame Backgrounds

Embeds a web page as a slide background that covers 100% of the reveal.js width and height. The iframe is in the background layer, behind your slides, and as such it's not possible to interact with it by default. To make your background interactive, you can add the `background-interactive` attribute.

| **Attribute**            | **Default** | **Description**                                                                                                                                 |
|:-------------------------|:------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| `background-iframe`      |             | URL of the iframe to load                                                                                                                       |
| `background-interactive` | false       | Include this attribute to make it possible to interact with the iframe contents. Enabling this will prevent interaction with the slide content. |

For example:

``` markdown
## Slide Title {background-iframe="https://example.com"}
```

### Slide Backgrounds Without a Title

You can always omit the title text, and specify only the slide background information:

``` {.markdown code-preview="examples/background-no-title.qmd"}
## {background-color="aquamarine"}

(A slide with no title)

## {background-color="black" background-image="https://placekitten.com/100/100" background-size="100px" background-repeat="repeat"}

(Another slide with no title)
```

### Main Title Slide Background

The main title slide is the first slide, which is generated via document YAML options. As a result, the methods described above won't work for providing a background for the title slide. Rather, you need to do the following:

1. Provide the title slide background options under `title-slide-attributes`
2. Prepend the background options with `data-`

For example:

```yaml
---
title: My Slide Show
title-slide-attributes:
    data-background-image: /path/to/title_image.png
    data-background-size: contain
    data-background-opacity: "0.5"
---
```

## Learning More

See these articles lo learn about more advanced capabilities of Reveal:

-   [Presenting Slides](presenting.qmd) describes slide navigation, printing to PDF, drawing on slides using a chalkboard, and creating multiplex presentations.
-   [Advanced Reveal](advanced.qmd) delves into transitions, animations, advanced layout and positioning, and other options available for customizing presentations.
-   [Reveal Themes](themes.qmd) talks about using and customizing existing themes as well as creating brand new themes.



--------------------------------------------------------------------------------
/docs/presentations/revealjs/presenting.qmd:
--------------------------------------------------------------------------------
---
title: "Presenting Slides"
---

## Overview

This article covers the mechanics of presenting slides with Reveal. Basic navigation is done using the following keyboard shortcuts:

+----------------------------+--------------------------------------------+
| Action                     | Keys                                       |
+============================+============================================+
| Next slide                 | <kbd>→</kbd> <kbd>SPACE</kbd> <kbd>N</kbd> |
+----------------------------+--------------------------------------------+
| Previous slide             | <kbd>←</kbd> <kbd>P</kbd>                  |
+----------------------------+--------------------------------------------+
| Navigate without fragments | <kbd>Alt →</kbd> <kbd>Alt ←</kbd>          |
+----------------------------+--------------------------------------------+
| Jump to first/last slide   | <kbd>Shift →</kbd> <kbd>Shift ←</kbd>      |
+----------------------------+--------------------------------------------+

::: {.callout-tip appearance="simple"}
You will often want to enter fullscreen mode when presenting. You can do this by pressing the {{< kbd F >}} key.
:::

In addition to basic keyboard navigation, Reveal supports several more advanced capabilities, including:

-   Navigation menu and overview mode
-   Speaker view (w/ speaker notes,timer, and preview of upcoming slides)
-   Printing to PDF and publishing as self contained HTML
-   Drawing on top of slides & chalkboard/whiteboard mode
-   Multiplex, which allows your audience to follow the slides of the presentation you are controlling on their own phone, tablet or laptop.

These capabilities are described below.

## Navigation Menu {#navigation-menu}

Quarto includes a built in version of the [reveal.js-menu](https://github.com/denehyg/reveal.js-menu) plugin. You can access the navigation menu using the button <kbd>![](images/navigation-menu-icon.png){style="padding-bottom: 1px;" width="15" height="13"}</kbd> located in the bottom left corner of the presentation. Clicking the button opens a slide navigation menu that enables you to easily jump to any slide:

::: {layout="[4,4]"}
![](images/navigation-menu-button.png){.border fig-alt="Screen shot of basic reveal.js slide with no overlays."}

![](images/navigation-menu-open.png){.border fig-alt="Screenshot of reveal.js slide with menu plugin open on the left. The menu bar has the Slides tab open, which shows a selectable list of all of the slides in the presentation."}
:::

::: {.callout-tip appearance="simple"}
You can also open the navigation menu by pressing the {{< kbd M >}} key.
:::

The navigation menu also includes a **Tools** pane that provides access to the various other navigation tools including Fullscreen, Speaker View, Overview Mode, and Print to PDF.

Use the following options to customize the appearance and behavior of the menu:

+-----------+--------------------------------------------------------------------------------------------------------------------+
| Option    | Description                                                                                                        |
+===========+====================================================================================================================+
| `side`    | Side of the presentation where the menu will be shown. `left` or `right` (defaults to `left`).                     |
+-----------+--------------------------------------------------------------------------------------------------------------------+
| `width`   | Width of the menu (`normal`, `wide`, `third`, `half`, `full`, or any valid css length value). Defaults to `normal` |
+-----------+--------------------------------------------------------------------------------------------------------------------+
| `numbers` | Add slide numbers to menu items.                                                                                   |
+-----------+--------------------------------------------------------------------------------------------------------------------+

For example:

``` yaml
format:
  revealjs:
    menu:
      side: right
      width: wide
```

You can hide the navigation menu by specifying the `menu: false` option:

``` yaml
format:
  revealjs:
    menu: false
```

Note that you can still open the menu using the {{< kbd M >}} key even if the button is hidden.

## Jump To Slide {#jump-to-slide}

{{< include /docs/prerelease/1.6/_pre-release-feature.qmd >}}

You can skip ahead to a specific slide using reveal.js' jump-to-slide shortcut. Here's how it works:

-   Press {{< kbd G >}} to activate
-   Type a slide number or an id
-   Press Enter to confirm

You can either enter - a numeric value to navigate to the desired slide number - a string, which will try to locate a slide with a matching id and navigate to it.

This feature can be opt-out by setting `jump-to-slide: false` option:

``` yaml
format:
  revealjs:
    jump-to-slide: false
```

## Overview Mode

Overview mode provides an alternate view that shows you a thumbnail for each slide:

![](images/overview-mode.png){.border fig-alt="Screenshot of slides shown in overview mode, showing a series of thumbnails for the slides in the presentation."}

::: {.callout-tip appearance="simple"}
You can enable Overview Mode by pressing the {{< kbd O >}} key.
:::

## Scroll View {#scroll-view}

{{< include /docs/prerelease/1.6/_pre-release-feature.qmd >}}

Reveal presentations can be presented in [Scroll View](https://revealjs.com/scroll-view/) with vertically scrolled navigation instead of Slides. This is a new view mode introduced in Revealjs 5. It is always available in presentations as an alternative view mode (like [Print view](#print-to-pdf)), and it will be used as the default view on small screens (e.g. viewing a presentation on a mobile).

Our demo presentation can be seen [in scroll view mode](https://{{< meta prerelease-subdomain >}}quarto.org/docs/presentations/revealjs/demo/?view=scroll) and below

<div>

```{=html}
<iframe class="slide-deck" src="demo/index.html?view=scroll"></iframe>
```

</div>

### Entering Scroll View {#scroll-view-toggle}

To enter Scroll View , do one the following:

-   Toggle into Scroll View using the {{< kbd R >}} key

-   Toggle into Scroll View using the [Navigation Menu](#navigation-menu)

-   Toggle into Scroll View by adding `?view=scroll` to the url, e.g. `https://quarto.org/docs/presentations/revealjs/demo/?view=scroll`

You can easily toggle out of Scroll View by the same action.

### Default View Mode

Scroll View can be set as the default mode for the presentation using the `scroll-view` option:

``` yaml
format:
  revealjs:
    scroll-view: true
```

### Scroll View Options

Scroll View can be configured using the following options under `scroll-view`:

+--------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Option             | Description                                                                                                                                                                                                                                               |
+====================+===========================================================================================================================================================================================================================================================+
| `progress`         | `auto`: Show the scrollbar while scrolling and hide while idle (default). Set to `true` to always show, `false` to always hide.                                                                                                                           |
+--------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| `snap`             | `mandatory`: When scrolling, it will automatically snap to the closest slide (default). Only snap when close to the top of a slide using `proximity`. Disable snapping altogether by setting to `false`.                                                  |
+--------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| `layout`           | `full`: Each slide will be sized to be as tall as the viewport (default). If you prefer a more dense layout with multiple slides visible in parallel, set to `compact`.                                                                                   |
+--------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| `activation-width` | Control scroll view activation width. The scroll view is automatically activated when the viewport reaches mobile widths. Set to `0` to disable automatic scroll view or to another value in pixels to automatically trigger on bigger or smaller widths. |
+--------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| `activate`         | Activate scroll view by default for the presentation (default `false`). Otherwise, entering scroll view require a manual trigger (See [Entering Scroll View](#scroll-view-toggle)). `scroll-view: true` is equivalent to                                  |
|                    |                                                                                                                                                                                                                                                           |
|                    | ``` yaml                                                                                                                                                                                                                                                  |
|                    | scroll-view:                                                                                                                                                                                                                                              |
|                    |   activate: true                                                                                                                                                                                                                                          |
|                    | ```                                                                                                                                                                                                                                                       |
+--------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

For example, the following specifies that we want a compact layout, proximity snap mode, to always show the progress scrollbar, and to never automatically activate for small screens:

``` yaml
---
title: "Presentation"
format:
  revealjs:
    scroll-view:
      layout: compact
      snap: proximity
      progress: true
      activation-width: 0
---
```

## Slide Zoom

Hold down the {{< kbd Alt linux=Ctrl >}} key and click on any element to zoom towards it. Try zooming in on one of these images:

```{=html}
<iframe class="reveal-demo border" src="demo/mini/zoom.html"></iframe>
```

{{< kbd Alt >}} or {{< kbd Ctrl >}} click again to zoom back out.

## Speaker View

The speaker view shows the current slide along with the upcoming slide, a timer, and any speaker notes associated with the current slide:

![](images/speaker-view.png){.border fig-alt="Screenshot of reveal.js presentation in Speaker View. On the right, the active slide is shown. The left column contains three sections which show (from top to bottom): the upcoming slide, time (both elapsed and clock time), and a section where speaker notes go."}

::: {.callout-tip appearance="simple"}
You can enable Speaker View by pressing the {{< kbd S >}} key.
:::

You can add speaker notes to a slide using a div with class `.notes`. For example:

``` markdown
## Slide with speaker notes

Slide content

::: {.notes}
Speaker notes go here.
:::
```

## Slide Numbers

You can add slide numbers to your presentation using the `slide-number` option. You can also control in which contexts slide numbers appear using the `show-slide-number` option. For example, here we configure slides numbers for printed output only:

``` yaml
---
title: "Presentation"
format:
  revealjs:
    slide-number: true
    show-slide-number: print
---
```

In addition to a simple `true` or `false` value, the `slide-number` option can also specify a format. Available formats include:

| Value | Description                           |
|-------|---------------------------------------|
| `c/t` | Slide number / total slides (default) |
| `c`   | Slide number only                     |
| `h/v` | Horizontal / Vertical slide number    |
| `h.v` | Horizontal . Vertical slide number    |

See [Vertical Slides](advanced.qmd#vertical-slides) for additional information on vertical slides.

The `show-slide-number` option supports the following values:

| Value     | Description                                  |
|-----------|----------------------------------------------|
| `all`     | Show slide numbers in all contexts (default) |
| `print`   | Only show slide numbers when printing to PDF |
| `speaker` | Only show slide numbers in the speaker view  |

## Print to PDF {#print-to-pdf}

Reveal presentations can be exported to PDF via a special print stylesheet.

::: callout-note
Note: This feature has been confirmed to work in [Google Chrome](https://google.com/chrome), [Chromium](https://www.chromium.org/Home) as well as in [Firefox](https://www.mozilla.org/en-US/firefox/).
:::

To Print to PDF, do the following:

1.  Toggle into Print View using the {{< kbd E >}} key (or using the [Navigation Menu](#navigation-menu))
2.  Open the in-browser print dialog {{< kbd Ctrl+P win=Ctrl+P mac=Command+P >}}.
3.  Change the **Destination** setting to **Save as PDF**.
4.  Change the **Layout** to **Landscape**.
5.  Change the **Margins** to **None**.
6.  Enable the **Background graphics** option.
7.  Click **Save** 🎉

If you entered print mode in the same window, you can toggle out of Print View using the same {{< kbd E >}} key, or navigate back to last slide seen using usual back button in your browser.

Here's what the Chrome print dialog would look like with these settings enabled:

![](images/print-to-pdf.png){.border fig-alt="Screenshot of Chrome print dialog with the first slide/page of 27 shown on the left, and print options on the right. The Destination print option has Save as PDF selected."}

### Print Options

There are a number of options that affected printed output that you may want to configure prior to printing:

+---------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Option                    | Description                                                                                                                                                                          |
+===========================+======================================================================================================================================================================================+
| `show-notes`              | Include speaker notes (`true`, `false`, or `separate-page)`                                                                                                                          |
+---------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| `slide-number`            | Include slide numbers (`true` or `false`)                                                                                                                                            |
+---------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| `pdf-max-pages-per-slide` | Slides that are too tall to fit within a single page will expand onto multiple pages. You can limit how many pages a slide may expand to using the `pdf-max-pages-per-slide` option. |
+---------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| `pdf-separate-fragments`  | Slides with multiple fragments are printed on a single page by default. To create a page for each fragment set this option to `true`.                                                |
+---------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

For example, the following specifies that we want to print speaker notes on their own page and include slide numbers:

``` yaml
---
title: "Presentation"
format:
  revealjs:
    show-notes: separate-page
    slide-number: true
---
```

## Preview Links

Reveal makes it easy to incorporate navigation to external websites into the flow of presentations using the `preview-links` option.

When you click on a hyperlink with `preview-links: true`, the link will be navigated to in an iframe that overlays the slide. For example, here we've clicked on a [Matplotlib](https://matplotlib.org/) link and the website opens on top of the slide (you'd click the close button at top right to hide it):

![](images/matplotlib.png){.border fig-alt="Screenshot of matplotlib landing page."}

Available values for `preview-link` include:

+------------+-----------------------------------------------------------------------------------------+
| Value      | Description                                                                             |
+============+=========================================================================================+
| `auto`     | Preview links when presenting in full-screen mode (otherwise navigate to them normally) |
+------------+-----------------------------------------------------------------------------------------+
| `true`     | Always preview links                                                                    |
+------------+-----------------------------------------------------------------------------------------+
| `false`    | Never preview links (the default)                                                       |
+------------+-----------------------------------------------------------------------------------------+

For example, here we set `preview-links` to `auto`:

``` yaml
---
title: "Presentation"
format:
  revealjs:
    preview-links: auto
---
```

You can also set this option on a per-link basis. These two links respectively enable and disable preview:

``` markdown
[Preview](https://example.com){preview-link="true"}

[NoPreview](https://example.com){preview-link="false"}
```

Previewing website in HTML format will use an `<iframe>`, which not all websites will allow (e.g. they could set in their response header [`X-Frame-Options` to `deny`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options), or [`frame-ancestor` restriction in their `Content-Security-Policy`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/frame-ancestors)). If a website disallow `iframe` usage, the preview will not be working in the Quarto document output.

## Slide Tone

Slide tone plays a subtle sound when you change slides. It was [requested by a blind user](https://github.com/yihui/xaringan/issues/214) and enables presenters to hear an auditory signal of their progress through the slides. Enable slide tone with:

``` yaml
format:
  revealjs:
    slide-tone: true
```

The tones increase in pitch for each slide from a low C to a high C note. The tone pitch stays the same for incremental slides.

The implementation of slide tone was adapted from the [slide tone plugin](https://github.com/gadenbuie/xaringanExtra/blob/master/docs/slide-tone/libs/slide-tone/slide-tone.js) in xaringanExtra.

## Auto-Slide

Presentations can be configured to step through slides automatically, without any user input. To enable this you will need to specify an interval for slide changes using the `auto-slide` option (the interval is provided in milliseconds). The `loop` option can additionally be specified to continue presenting in a loop once all the slides have been shown.

For example, here we specify that we want to advance every 5 seconds and continue in a loop:

``` yaml
---
title: "Presentation"
format: 
  revealjs: 
    auto-slide: 5000
    loop: true
---
```

A play/pause control element will automatically appear for auto-sliding decks. Sliding is automatically paused if the user starts interacting with the deck. It's also possible to pause or resume sliding by pressing {{< kbd A >}} on the keyboard.

You can disable the auto-slide controls and prevent sliding from being paused by specifying `auto-slide-stoppable: false`.

### Slide Timing

It's also possible to override the slide duration for individual slides and fragments by using the `autoslide` attribute (this attribute also works on [Fragments](advanced.qmd#fragments){data-heading="Fragments"}). For example, here we set the auto-slide value to 2 seconds:

``` markdown
## Slide Title {autoslide=2000}
```

## Publishing

There are two main ways to publish Reveal presentations:

1.  As a PDF file---see [Print to PDF](#print-to-pdf) above for details on how to do this.

2.  As an HTML file. For HTML, it's often most convenient to distribute the presentation as a single self contained file. To do this, specify the `embed-resources` option:

    ``` yaml
    ---
    title: "Presentation"
    format:
      revealjs:
        embed-resources: true
    ---
    ```

    All of the dependent images, CSS styles, and other assets will be contained within the HTML file created by Quarto.

    ::: {.callout-note appearance="simple"}
    Note that specifying `embed-resources` can slow down rendering by a couple of seconds, so you may want to enable `embed-resources` only when you are ready to publish. Also note that Reveal plugin [Chalkboard] is not compatible with `embed-resources` --- when [Chalkboard] plugin is enabled, specifying `embed-resources: true` will result an error.
    :::

See the documentation on [Publishing HTML](/docs/publishing/index.qmd) for details on additional ways to publish Reveal presentations including GitHub Pages and Posit Connect.

## Navigation Options

There are several navigational cues provided as part of Reveal presentations and corresponding options that control them:

+-------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Option      | Description                                                                                                                                                                  |
+=============+==============================================================================================================================================================================+
| `controls`  | Show arrow controls for navigating through slides (defaults to `auto`, which will show controls when vertical slides are present or when the deck is embedded in an iframe). |
+-------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| `progress`  | Show a progress bar at the bottom (defaults to `true`).                                                                                                                      |
+-------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| `history`   | Push slide changes to the browser history. Defaults to `true`, which means that the browser Forward/Back buttons can be used for slide navigation.                           |
+-------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| `hash-type` | Type of URL hash to use for slides. Defaults to `title` which is derived from the slide title. You can also specify `number`.                                                |
+-------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

For example, the following configuration hides the progress bar and specifies that we want to use browser history:

``` yaml
---
title: "Presentation"
format:
  revealjs:
    progress: false
    history: true
---
```

## Chalkboard

Quarto includes a built-in version of the [reveal.js-chalkboard](https://github.com/rajgoel/reveal.js-plugins/tree/master/chalkboard) plugin. Specify the `chalkboard: true` option to enable the plugin, which enables you to draw on a notes canvas on top of your slides and/or open up an empty chalkboard within your presentation:

``` yaml
---
title: "Presentation"
format:
  revealjs:
    chalkboard: true
---
```

::: {.callout-warning appearance="simple"}
Note that Reveal plugin [Chalkboard] is not compatible with `embed-resources` output --- when [Chalkboard] plugin is enabled, specifying `embed-resources: true` will result an error.
:::

Here are what the notes canvas and chalkboard look like when activated:

::: {layout="[4,4]"}
![](images/drawing-canvas.png){.border fig-alt="Slide with notes canvas activated has a panel on the left to select colors, and a menu bar at the bottom with a paintbrush. One of the words in the slide header has been underlined with the brush in blue."}

![](images/chalkboard.png){.border fig-alt="Screenshot of chalkboard canvas with color selector on the left, and paintbrush tool at the bottom. The background is dark, and the equation 'y = mx + b' has been drawn in white with a chalky texture."}
:::

To toggle the notes canvas on and off use the <kbd>![](images/canvas-icon.png){width="19" height="17"}</kbd> button or the {{< kbd C >}} key.

To toggle the chalkboard on and off use the <kbd>![](images/chalkboard-icon.png){width="19" height="20"}</kbd> button or the {{< kbd B >}} key.

Here are all of the keyboard shortcuts associated with the notes canvas and chalkboard:

| Action                  | Key                   |
|-------------------------|-----------------------|
| Toggle notes canvas     | {{< kbd C >}}         |
| Toggle chalkboard       | {{< kbd B >}}         |
| Reset all drawings      | {{< kbd BACKSPACE >}} |
| Clear drawings on slide | {{< kbd DEL >}}       |
| Cycle colors forward    | {{< kbd X >}}         |
| Cycle colors backward   | {{< kbd Y >}}         |
| Download drawings       | {{< kbd D >}}         |

The following mouse and touch gestures can be used for interacting with drawings:

-   Click on the buttons at the bottom left to toggle the notes canvas or chalkboard

-   Click on the color picker at the left to change the color (the color picker is only visible if the notes canvas or chalkboard is active)

-   Click on the up/down arrows on the right to switch among multiple chalkboard (the up/down arrows are only available for the chalkboard)

-   Click the left mouse button and drag to write on notes canvas or chalkboard

-   Click the right mouse button and drag to wipe away previous drawings

-   Touch and move to write on notes canvas or chalkboard

-   Touch and hold for half a second, then move to wipe away previous drawings

### Restoring Drawings

The {{< kbd D >}} key downloads any active drawings into a JSON file. You can then restore these drawings when showing your presentation using the `src` option. For example:

``` yaml
---
title: "Presentation"
format:
  revealjs:
    chalkboard:
      src: drawings.json
---
```

### Chalkboard Options

The following options are available to customize the behavior and appearance of the chalkboard:

+---------------------+-------------------------------------------------------------------------------------------------------------------------------------------------+
| Option              | Description                                                                                                                                     |
+=====================+=================================================================================================================================================+
| `theme`             | Can be set to either `chalkboard` (default) or `whiteboard`.                                                                                    |
+---------------------+-------------------------------------------------------------------------------------------------------------------------------------------------+
| `boardmarker-width` | The drawing width of the boardmarker; larger values draw thicker line. Defaults to `3`.                                                         |
+---------------------+-------------------------------------------------------------------------------------------------------------------------------------------------+
| `chalk-width`       | The drawing width of the chalk; larger values draw thicker lines. Defaults to `7`.                                                              |
+---------------------+-------------------------------------------------------------------------------------------------------------------------------------------------+
| `chalk-effect`      | A float in the range `[0.0, 1.0]`, the intensity of the chalk effect on the chalk board. Full effect (default) `1.0`, no effect `0.0`.          |
+---------------------+-------------------------------------------------------------------------------------------------------------------------------------------------+
| `src`               | Optional file name for pre-recorded drawings (download drawings using the {{< kbd D >}} key).                                                   |
+---------------------+-------------------------------------------------------------------------------------------------------------------------------------------------+
| `read-only`         | Configuration option to prevent changes to existing drawings. `true`: no changes can be made, `false` (default): changes can be made.           |
+---------------------+-------------------------------------------------------------------------------------------------------------------------------------------------+
| `buttons`           | Add chalkboard buttons at the bottom of the slide (defaults to `true`).                                                                         |
+---------------------+-------------------------------------------------------------------------------------------------------------------------------------------------+
| `transition`        | Gives the duration (in milliseconds) of the transition for a slide change, so that the notes canvas is drawn after the transition is completed. |
+---------------------+-------------------------------------------------------------------------------------------------------------------------------------------------+

For example, the following configuration specifies that we want to use the `whiteboard` theme with a (thicker) boardmarker width, and that we want to hide the chalkboard buttons at the bottom of each slide:

``` yaml
---
title: "Presentation"
format:
  revealjs:
    chalkboard:
      theme: whiteboard
      boardmarker-width: 5
      buttons: false
---
```

If you disable the chalkboard buttons globally you can selectively re-enable them for individual slides with the `chalkboard-buttons` attribute. For example:

``` markdown
## Slide Title {chalkboard-buttons="true"}
```

You can also use `chalkboard-buttons="false"` to turn off the buttons for individual slides.

## Multiplex

Quarto includes a built-in version of the [Reveal Multiplex](https://github.com/reveal/multiplex) plugin. The multiplex plugin allows your audience to follow the slides of the presentation you are controlling on their own phone, tablet or laptop. When you change slides in your master presentations everyone will follow and see the same content on their own device.

Creating a Reveal presentation that supports multiplex is straightforward. Just specify the `multiplex: true` option as follows:

``` yaml
---
title: "Presentation"
format:
  revealjs:
    multiplex: true
---
```

Rendering the presentation will result in two HTML files being created by Quarto:

+-----------------------------+------------------------------------------------------------------------------------------------------------------------------------+
| File                        | Description                                                                                                                        |
+=============================+====================================================================================================================================+
| `presentation.html`         | This is the file you should publish online and that your audience should view.                                                     |
+-----------------------------+------------------------------------------------------------------------------------------------------------------------------------+
| `presentation-speaker.html` | This is the file that you should present from . This file can remain on your computer and does not need to be published elsewhere. |
+-----------------------------+------------------------------------------------------------------------------------------------------------------------------------+

The two versions of the presentation will be synchronized such that when the speaker version switches slides the viewers also all switch to the same slide.

### Multiplex Server {.unlisted}

Behind the scenes there is a multiplex server that is synchronizing slide events between the viewer and speaker versions of the presentation. Note that the this server does not actually see any of the slide content, it is only used to synchronize events.

By default, a server created and hosted by the Revealjs team is used for this: <https://reveal-multiplex.glitch.me/>. This server is used by default when you specify `multiplex: true`.

#### Running your own server

If you want to run your own version of this server its source code is here: <https://github.com/reveal/multiplex/blob/master/index.js>.

You can then configure multiplex to use an alternate server as follows:

``` yaml
---
title: "Presentation"
format:
  revealjs:
    multiplex: 
      url: 'https://myserver.example.com/
---
```

Note that Quarto calls the multiplex server behind the scenes to provision a id and secret for your presentation. If you want to provision your own id and secret you can do so at <https://reveal-multiplex.glitch.me/> (or using your custom hosted server URL) and provide them explicitly in YAML:

``` yaml
---
title: "Presentation"
format:
  revealjs:
    multiplex: 
      id: '1ea875674b17ca76'
      secret: '13652805320794272084'
---
```

Note that the `secret` value will be included in only the speaker version of the presentation.

## Learning More

See these articles lo learn more about using Reveal:

-   [Reveal Basics](index.qmd) covers the basic mechanics of creating presentations.
-   [Advanced Reveal](advanced.qmd) delves into transitions, animations, advanced layout and positioning, and other options available for customizing presentations.
-   [Reveal Themes](themes.qmd) talks about using and customizing existing themes as well as creating brand new themes.


--------------------------------------------------------------------------------
/docs/presentations/revealjs/themes.qmd:
--------------------------------------------------------------------------------
---
title: "Reveal Themes"
---

## Using Themes

{{< include _theme-basics.md >}}


## Customizing Themes

You can customize the built-in themes by adding your own [Sass](https://sass-lang.com/) theme file to the theme declaration. For example:

``` yaml
---
title: "Presentation"
format:
  revealjs: 
    theme: [default, custom.scss]
---
```

Here's what the contents of `custom.scss` might look like:

``` default
/*-- scss:defaults --*/

$body-bg: #191919;
$body-color: #fff;
$link-color: #42affa;

/*-- scss:rules --*/

.reveal .slide blockquote {
  border-left: 3px solid $text-muted;
  padding-left: 0.5em;
}
```

Theme files use [Sass](https://sass-lang.com/) (a variant of CSS that supports variables and other extended features) and are divided into sections.

-   `/*-- scss:defaults --*/` is used to define variables that affect fonts, colors, borders, etc. (note that variables start with a `$`)

-   `/*-- scss:rules --*/` is used to create CSS rules. Note that CSS rules that target Reveal content generally need to use the `.reveal .slide` prefix to successfully override the theme's default styles.

See the [Sass Variables] documentation for a list of what's available to customize.

## Creating Themes

Creating a new theme is just a matter of re-defining one or more of the default Sass variables (you don't need to re-specify values that you don't want to override) and adding any additional CSS rules you need to.

See the [Sass Variables] documentation for a list of what can be customized within a theme.

For example, here is the source code for the built in `serif` theme:

``` default
/*-- scss:defaults --*/

// fonts
$font-family-sans-serif: "Palatino Linotype", "Book Antiqua", Palatino,
  FreeSerif, serif !default;

// colors
$body-bg: #f0f1eb !default;
$body-color: #000 !default;
$link-color: #51483d !default;
$selection-bg: #26351c !default;

// headings
$presentation-heading-font: "Palatino Linotype", "Book Antiqua", Palatino,
  FreeSerif, serif !default;
$presentation-heading-color: #383d3d !default;

/*-- scss:rules --*/

.reveal a {
  line-height: 1.3em;
}
```

In this theme file you'll notice that the `!default` suffix is placed after variable definitions. This is to make sure that anyone using this theme can override the variable value (without that the value is defined as not overrideable).

You can use a custom theme by just specifying it as the `theme` option (all theme files implicitly inherit from the `default` theme). For example:

``` yaml
---
title: "Presentation"
format:
  revealjs: 
    theme: mytheme.scss
---
```

Here is the source code for all of the built-in themes for inspiration and examples:

<https://github.com/quarto-dev/quarto-cli/tree/main/src/resources/formats/revealjs/themes>

## Sass Variables

Here's a list of all Sass variables (and their default values) used by Reveal themes. Note that some variables are defined using other variables, and several of the color variables use the `lighten()` Sass function to create a lighter variant of another color.

### Colors

| Variable                               | Default                                  |
|----------------------------------------|------------------------------------------|
| `$body-bg`                             | #fff                                     |
| `$body-color`                          | #222                                     |
| `$text-muted`                          | lighten(\$body-color, 50%)               |
| `$link-color`                          | #2a76dd                                  |
| `$link-color-hover`                    | lighten(\$link-color, 15%)               |
| `$selection-bg`                        | lighten(\$link-color, 25%)               |
| `$selection-color`                     | \$body-bg                                |
| `$light-bg-text-color`                 | #222                                     |
| `$light-bg-link-color`                 | #2a76dd                                  |
| `$light-bg-code-color`                 | #4758ab                                  |
| `$dark-bg-text-color`                  | #fff                                     |
| `$dark-bg-link-color`                  | #42affa                                  |
| `$dark-bg-code-color`                  | #ffa07a                                  |

### Fonts

| Variable                               | Default                                  |
|----------------------------------------|------------------------------------------|
| `$font-family-sans-serif`              | "Source Sans Pro", Helvetica, sans-serif |
| `$font-family-monospace`               | monospace                                |
| `$presentation-font-size-root`         | 40px                                     |
| `$presentation-font-smaller`           | 0.7                                      |
| `$presentation-line-height`            | 1.3                                      |

### Headings

| Variable                               | Default                                  |
|----------------------------------------|------------------------------------------|
| `$presentation-h1-font-size`           | 2.5em                                    |
| `$presentation-h2-font-size`           | 1.6em                                    |
| `$presentation-h3-font-size`           | 1.3em                                    |
| `$presentation-h4-font-size`           | 1em                                      |
| `$presentation-heading-font`           | \$font-family-sans-serif                 |
| `$presentation-heading-color`          | \$body-color                             |
| `$presentation-heading-line-height`    | 1.2                                      |
| `$presentation-heading-letter-spacing` | normal                                   |
| `$presentation-heading-text-transform` | none                                     |
| `$presentation-heading-text-shadow`    | none                                     |
| `$presentation-heading-font-weight`    | 600                                      |
| `$presentation-h1-text-shadow`         | none                                     |

### Code Blocks

| Variable                               | Default                                  |
|----------------------------------------|------------------------------------------|
| `$code-block-bg`                       | \$body-bg                                |
| `$code-block-border-color`             | lighten(\$body-color, 60%)               |
| `$code-block-font-size`                | 0.55em                                   |

### Inline Code

| Variable                               | Default                                  |
|----------------------------------------|------------------------------------------|
| `$code-color`                          | var(--quarto-hl-fu-color)                |
| `$code-bg`                             | transparent                              |

### Tabsets

| Variable                               | Default                                  |
|----------------------------------------|------------------------------------------|
| `$tabset-border-color`                 | \$code-block-border-color                |

### Layout

| Variable                               | Default                                  |
|----------------------------------------|------------------------------------------|
| `$border-color`                        | lighten(\$body-color, 30%)               |
| `$border-width`                        | 1px                                      |
| `$border-radius`                       | 3px                                      |
| `$presentation-block-margin`           | 12px                                     |
| `$presentation-slide-text-align`       | left                                     |
| `$presentation-title-slide-text-align` | center                                   |

### Callouts

+--------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Variable                 | Notes                                                                                                                                                              |
+==========================+====================================================================================================================================================================+
| `$callout-border-width`  | The left border width of callouts. Defaults to `0.3rem`.                                                                                                           |
+--------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| `$callout-border-scale`  | The border color of callouts computed by shifting the callout color by this amount. Defaults to `0%`.                                                              |
+--------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| `$callout-icon-scale`    | The color of the callout icon computed by shifting the callout color by this amount. Defaults to `10%`.                                                            |
+--------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| `$callout-margin-top`    | The amount of top margin on the callout. Defaults to `1rem`.                                                                                                       |
+--------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| `$callout-margin-bottom` | The amount of bottom margin on the callout. Defaults to `1rem`.                                                                                                    |
+--------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| `$callout-color-<type>`  | The colors for the various types of callouts. Defaults:                                                                                                            |
|                          |                                                                                                                                                                    |
|                          | | type        | default                 |                                                                                                                          |
|                          | |-------------|-------------------------|                                                                                                                          |
|                          | | `note`      | [`#0d6efd`]{.color-box} |                                                                                                                          |
|                          | | `tip`       | [`#198754`]{.color-box} |                                                                                                                          |
|                          | | `caution`   | [`#dc3545`]{.color-box} |                                                                                                                          |
|                          | | `warning`   | [`#fd7e14`]{.color-box} |                                                                                                                          |
|                          | | `important` | [`#ffc107`]{.color-box} |                                                                                                                          |
|                          |                                                                                                                                                                    |
|                          | Note that style for callout is to have left border using type color, and header background to use a variation of this color.                                       |
+--------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+

You'll notice that some of the Sass variables use a `presentation-` prefix and some do not. The `presentation-` prefixed variables are specific to presentations, whereas the other variables are the same as ones used for standard Quarto [HTML Themes](/docs/output-formats/html-themes.qmd).

Since all Quarto themes use the same Sass format, you can use a single theme file for both HTML / website documents and presentations.

## Learning More

See these articles to learn more about using Reveal:

-   [Reveal Basics](index.qmd) covers the basic mechanics of creating presentations.
-   [Presenting Slides](presenting.qmd) describes slide navigation, printing to PDF, drawing on slides using a chalkboard, and creating multiplex presentations.
-   [Advanced Reveal](advanced.qmd) delves into transitions, animations, advanced layout and positioning, and other options available for customizing presentations.
-   [More About Quarto Themes](/docs/output-formats/html-themes-more.qmd) describes the layering system in more detail, including interactions with other SCSS files and [`_brand.yml`](/docs/authoring/brand.qmd).


--------------------------------------------------------------------------------