└── docs
    └── brand
        ├── _metadata.yml
        ├── color.qmd
        ├── defaults.qmd
        ├── index.qmd
        ├── logo.qmd
        ├── meta.qmd
        ├── spec
            ├── brand-color.yml
            ├── brand-defaults.yml
            ├── brand-logo.yml
            ├── brand-meta.yml
            ├── brand-typography.yml
            ├── brand.yml
            └── brand_definitions.yml
        └── typography.qmd


/docs/brand/_metadata.yml:
--------------------------------------------------------------------------------
page-navigation: true
bread-crumbs: true

sidebar: brand-yml



--------------------------------------------------------------------------------
/docs/brand/color.qmd:
--------------------------------------------------------------------------------
---
title: Color
pagetitle: "color | brand.yml"
---

## About

The `color` section in `_brand.yml` is used to define the brand's color palette and theme colors, allowing you to codify your brand's palette with minimal overhead and to map these colors to semantic theme fields.

## Structure

The `color` section in `_brand.yml` consists of two main parts.

1.  [palette](#palette): A set of named colors specific to the brand.
2.  [Theme colors](#theme-colors): Semantic color assignments for various UI elements.

You can approach creating a `_brand.yml` from your brand guidelines in two steps:

1. First, define the available brand colors in `color.palette`.
2. Then, map the brand colors to theme colors in the `color` section.

## Examples

### Example with Palette

This example first defines the brand's color palette and then maps the brand's colors to theme elements by reference:

```{.yaml filename="_brand.yml"}
color:
  palette:
    white: "#FFFFFF"
    black: "#151515"
    blue: "#447099"
    orange: "#EE6331"
    green: "#72994E"
    teal: "#419599"
    burgundy: "#9A4665"

  foreground: black
  background: white
  primary: blue
  secondary: "#707073"
  tertiary: "#C2C2C4"
  success: green
  info: teal
  warning: orange
  danger: burgundy
  light: white
  dark: "#404041"
```

Notice that we can refer to `blue` and `green` directly.
brand.yml will automatically replace these named values with the corresponding value from `color.palette`, `color.palette.blue` and `color.palette.green` respectively.

### Minimal Example

Of course, you can also skip creating a brand color palette and pick theme colors directly.

```{.yaml filename="_brand.yml"}
color:
  foreground: "#151515"
  background: "#FFFFFF"
  primary: "#447099"
  secondary: "#707073"
  tertiary: "#C2C2C4"
  success: "#72994E"
  info: "#419599"
  warning: "#EE6331"
  danger: "#9A4665"
  light: "#FFFFFF"
  dark: "#404041"
```

## Attributes

### palette {#palette}

The `palette` attribute is a nested mapping of color names to color string values (hex colors are recommended).

```{.yaml filename="_brand.yml"}
color:
  palette:
    blue: "#447099"
    orange: "#EE6331"
    gray: "#404041"
```

These named colors can be referenced in other parts of the `color` section and in any `color` or `background-color` attributes in the [typography](typography.qmd) section of [the `_brand.yml` file](index.qmd).

Some brands have creative names for colors, such as [lava, mint, and mustard](https://brand.mixpanel.com/7d777d80-7d99-4c2a-9730-2a960e190bf8/1ae88802-a827-40a5-96a3-547abacf70b7), and you're welcome to use these names in your `palette`.
However, many tools --- of which [Bootstrap](https://getbootstrap.com/docs/5.0/customize/color/) is one --- use common color names, like red, green, yellow, etc.

If your brand includes create color names, we recommend you create aliases within `palette` to map your brand's color names to common color names:

```{.yaml filename="_brand.yml"}
meta:
  name Mixpanel
  link: https://brand.mixpanel.com
color:
  palette:
    lava: "#FF7557"
    mint: "#80E1D9"
    mustard: "#F8BC3B"
    red: lava
    green: mint
    yellow: mustard
```

### Theme Colors {#theme-colors}

Other than `palette`, the remaining attributes in `color` are used to map brand colors to semantic theme colors.
These theme colors can then be used in web apps and reports by tools that support brand.yml to maintain a consistent color scheme across the brand.

| Name | Description |
|-----------------------|-------------------------------------------------|
| `foreground` | The main text color. Typically will be close to black and must have high contrast with the background color. |
| `background` | The main background color. Tyically will be close to white and must have high contrast with the foreground color. |
| `primary` | The primary accent color, used for hyperlinks, active states, and primary action buttons. |
| `secondary` | The secondary accent color, often used for lighter text or disabled states. |
| `tertiary` | The tertiary accent color, used for hover states, accents, and wells. |
| `success` | The color used for positive or successful actions and information. |
| `info` | The color used for neutral or informational actions and information. |
| `warning` | The color used for warning or cautionary actions and information. |
| `danger` | The color used for errors, dangerous actions, or negative information. |
| `light` | A bright color, used as a high-contrast foreground color on dark elements or low-contrast background color on light elements. |
| `dark` | A dark color, used as a high-contrast foreground color on light elements or high-contrast background color on light elements. |

## Additional Features

### Automatic Color Definitions

For specific output formats, the brand color palette will be automatically made available.
For example, in HTML/Bootstrap settings, this would create `$brand-{name}` (Sass) and `--brand-{name}` (CSS) variables for each color in the palette.

### Referencing Palette Colors

Colors defined in the `palette` can be referenced by name in other parts of the `color` section:

```{.yaml filename="_brand.yml"}
color:
  palette:
    blue: "#447099"
  primary: blue
```

This approach allows for easy reuse of colors and maintains consistency throughout the brand definition.

### Using Brand Colors in Typography

Colors defined in the `color` section can also be used by reference in any `color` and `background-color` attributes in the [typography section](typography.qmd):

```{.yaml filename="_brand.yml"}
color:
  palette:
    blue: "#447099"
    burgundy: "#9A4665"
  primary: blue

typography:
  headings:
    color: primary
  link:
    color: burgundy
```



--------------------------------------------------------------------------------
/docs/brand/defaults.qmd:
--------------------------------------------------------------------------------
---
title: Defaults
pagetitle: "defaults | brand.yml"
aliases:
  - /brand/template.html
---

## About

Individual formats and outputs can expose format-specific variables or options that are relevant to branding.
These options are tied to a specific output format or context, so they can't be included in the core brand specification.
But they are still relevant to the brand and need a place within brand.yml.

## Structure

::: callout-warning
This section of brand.yml is not as well-sepecified as the other sections, by design.
As brand.yml adoption grows, new tools will need to be able to store options specific to the tool.
This part of the brand.yml spec may change as we learn more about the needs of different tools.
:::

Currently, both Quarto and Shiny support a `bootstrap` section under `defaults` that can be used to set default values for Bootstrap Sass variables.

```{.yaml filename="_brand.yml"}
defaults:
  bootstrap:
    defaults:
      enable-rounded: false
      link-decoration: none
```

In [Shiny for Python](https://shiny.posit.co/py/api/core/ui.Theme.html), an additional `shiny.theme` section is used to set default values for Shiny-specific theme settings.

```{.yaml filename="_brand.yml"}
color:
  palette:
    pink: "#E83E8C"
defaults:
  shiny:
    theme:
      preset: shiny
      defaults:
        bslib-dashboard-design: false
      rules: |
        .navbar-brand { color: $brand-pink }
```

Note that in these sections, you can make use of brand features, like the addition of [`$brand-{color}` Sass variables](color.qmd#automatic-color-definitions).



--------------------------------------------------------------------------------
/docs/brand/index.qmd:
--------------------------------------------------------------------------------
---
title: "brand.yml Structure"
code-annotations: select

brand-meta: >
  Key identity information, name of the company, links to brand guidelines, etc.
brand-logo: >
  Files or links to the brand's logo at various sizes.
brand-color-palette: >
  Named colors in the brand's color palette.
brand-color: >
  Semantic colors, e.g. `primary`, `secondary`, `success`, `warning`, etc.
brand-typography-fonts: >
  Font definitions for Google, remote or bundled fonts.
brand-typography: >
  Font family, weight, style, color, and line height for key elements,
  e.g. base, headings and monospace text.
brand-defaults: >
  Additional context-specific settings beyond the basic brand colors and typography.
  These could be options, for example, that are used by Bootstrap in Quarto or Shiny.
  They could also be folded into existing Quarto yaml fields like `format` or `website`, or they could be new fields for other contexts like `shiny`.
---


## Outline

```{.yaml filename="_brand.yml"}
meta:             # <1>
  name: brand.yml # <1>
  links: # <1>
    home: https://posit-dev.github.io/brand-yml # <1>
    github: https://github.com/posit-dev/brand-yml # <1>

logo: # <2>
  images: # <2>
    icon-color: logos/icon/brand-yml-icon-color.png # <2>
    wide-color: logos/wide/brand-yml-wide-color.png # <2>
    tall-color: logos/wide/brand-yml-tall-color.png # <2>
  small: icon-color  # <2>
  medium: wide-color # <2>
  large: tall-color  # <2>

color:
  palette: # <3>
    orange: "#FF6F20" # <3>
    pink: "#FF3D7F"   # <3>
    green: "#28A745"  # <3>
    yellow: "#FFC107" # <3>
  primary: orange # <4>
  success: green  # <4>
  warning: yellow # <4>
  danger: pink    # <4>

typography:
  fonts: # <5>
    - family: Open Sans # <5>
      source: google # <5>
    - family: IBM Plex Mono # <5>
      source: google # <5>
    - family: Rubik # <5>
      source: google # <5>
  base: # <6>
    family: Open Sans # <6>
    line-height: 1.6 # <6>
  headings: # <6>
    family: Rubik # <6>
    weight: normal # <6>
  link: # <6>
    color: purple # <6>
  monospace: # <6>
    family: IBM Plex Mono # <6>
    size: 1em # <6>

defaults: # <7>
  bootstrap: # <7>
    # bootstrap variable definitions # <7>
  quarto: # <7>
    format: # <7>
      # basic format-specific settings  # <7>
      html: # <7>
      revealjs: # <7>
  shiny: # <7>
    # shiny specific settings # <7>
```

1. [meta](meta.qmd): {{< meta brand-meta >}}

1. [logo](logo.qmd): {{< meta brand-logo >}}

1. [color.palette](color.qmd#color): {{< meta brand-color-palette >}}

1. [color](color.qmd#theme): {{< meta brand-color >}}

1. [typography.fonts](typography.qmd#fonts): {{< meta brand-typography-fonts >}}

1. [typography](typography.qmd#typography): {{< meta brand-typography >}}

1. [defaults](defaults.qmd): {{< meta brand-defaults >}}

## Description

[meta](meta.qmd)
:    {{< meta brand-meta >}}

[logo](logo.qmd)
:    {{< meta brand-logo >}}

[color](color.qmd#theme)
:    {{< meta brand-color >}} [color.palette](color.qmd#color): {{< meta brand-color-palette >}}

[typography](typography.qmd#typography)
:    {{< meta brand-typography >}} [typography.fonts](typography.qmd#fonts): {{< meta brand-typography-fonts >}}


[defaults](defaults.qmd)
:    {{< meta brand-defaults >}}

## Specification

We've created a schema for the structure of a brand.yml file in two flavors:

1. [brand.yml schema as YAML](../schema/brand.schema.yml), a YAML variant of [JSON Schema][json-schema] used by [Quarto][quarto] to validate the structure `_brand.yml` files or `brand` in Quarto metadata.
2. [brand.yml schema as JSON](../schema/brand.schema.json), a [JSON Schema][json-schema] containing the definitions used in the YAML schema.

[json-schema]: https://json-schema.org/
[quarto]: https://quarto.org/



--------------------------------------------------------------------------------
/docs/brand/logo.qmd:
--------------------------------------------------------------------------------
---
title: Logo
pagetitle: "logo | brand.yml"
---

## About

The `logo` section in your `_brand.yml` file allows you to define and organize the logos and brand images for your project. This flexible system supports various logo sizes, light/dark variants, and the ability to store multiple image resources for different use cases.

## Structure

The `logo` field in your `_brand.yml` file can be structured in several ways, from a simple single-logo setup to a more complex configuration with multiple sizes and variants:

- [images](#images): A dictionary of named logo resources
- [small](#small): Logo for small display contexts (e.g., favicons)
- [medium](#medium): Logo for medium display contexts (e.g., website headers)
- [large](#large): Logo for large display contexts (e.g., title slides, marketing materials)

Logos can be stored locally---adjacent to your `_brand.yml` file---or hosted online.
Local file paths should be relative to the location of your `_brand.yml` file
(I'll use `logos/` as the directory in the examples below).
Online images should use full URLs starting with `http://` or `https://`.

## Examples

### Simple Single Logo

```{.yaml filename="_brand.yml"}
logo: posit.png
```

### Basic Multi-size Configuration

```{.yaml filename="_brand.yml"}
logo:
  small: logos/icon.png
  medium: logos/header-logo.png
  large: logos/full-logo.svg
```

### Light/Dark Variants

You can specify different logos for light and dark backgrounds by giving the `small`, `medium`, and `large` attributes a nested mapping with `light` and `dark` child elements.
"**light**" means for use on light background (or in a light color mode), and "**dark**" means for use on dark background (or in a dark color mode).

```{.yaml filename="_brand.yml"}
logo:
  small: logos/icon.png
  medium:
    light: logos/header-logo.png
    dark: logos/header-logo-white.png
  large: logos/full-logo.svg
```

### Comprehensive Configuration with Named Resources

Use `images` as a nested mapping to define multiple logo resources with meaningful names.
Then, you can directly reference these resources by name in the `small`, `medium`, and `large` attributes.

```{.yaml filename="_brand.yml"}
logo:
  images:
    icon: logos/icon.png
    header: logos/header-logo.png
    header-white: logos/header-logo-white.png
    full: logos/full-logo.svg
  small: icon
  medium:
    light: header
    dark: header-white
  large: full
```

### Configuration with Alternative Text

Logo images can have associated alternative text for accessibility purposes.
This can be specified as an `alt` property in the image object as the alt text is directly associated with each image.
The University of South Carolina provides a great resource on [writing effective alt text for logos](https://sc.edu/about/offices_and_divisions/digital-accessibility/toolbox/best_practices/alternative_text/logo-alt-text/index.php) in their [Digital Accessibility Toolbox](https://sc.edu/about/offices_and_divisions/digital-accessibility/index.php).


```{.yaml filename="_brand.yml"}
logo:
  images:
    icon:
      path: logos/icon.png
      alt: "Company icon with abstract shapes"
    header:
      path: logos/header-logo.png
      alt: "Company name with logo"
    header-white:
      path: logos/header-logo-white.png
      alt: "Company name with logo in white"
    full:
      path: logos/full-logo.svg
      alt: "Full company logo with tagline"
  small: icon
  medium:
    light: header
    dark: header-white
  large: full
```

## Attributes

### images {#images}

The `images` attribute is a mapping that allows you to define multiple logo resources with meaningful names. These named resources can then be referenced in the `small`, `medium`, and `large` attributes.

```{.yaml filename="_brand.yml"}
logo:
  images:
    primary: logos/primary-logo.png
    icon: logos/favicon.png
    white: logos/white-logo.png
```

Each image can be specified as a simple string path or as an object with `path` and `alt` properties:

```{.yaml filename="_brand.yml"}
logo:
  images:
    primary:
      path: logos/primary-logo.png
      alt: "Company logo with name and icon"
```

### small {#small}

The `small` attribute defines the logo used for small display contexts, such as favicons or mobile app icons.

`small`, `medium` and `large` can each be a simple string path to the image or a reference to a named resource defined in the `images` attribute (shown in the second example).

:::{.grid style="--bs-columns:2"}
::: {.g-col-2 .g-col-lg-1}
```{.yaml filename="_brand.yml"}
logo:
  small: logos/favicon.png
```
:::

::: {.g-col-2 .g-col-lg-1}
```{.yaml filename="_brand.yml"}
logo:
  images:
    icon: logos/favicon.png
  small: icon
```
:::
:::

### medium {#medium}

The `medium` attribute specifies the logo for medium-sized display contexts, typically used in website headers or navigation bars.

`small`, `medium` and `large` can also be nested mappings with `light` and `dark` child elements to specify different logos for light and dark backgrounds (show in the second example).

::: {.grid style="--bs-columns:2"}
::: {.g-col-2 .g-col-lg-1}
```{.yaml filename="_brand.yml"}
logo:
  medium: logos/header-logo.png
```
:::

::: {.g-col-2 .g-col-lg-1}
```{.yaml filename="_brand.yml"}
logo:
  medium:
    light: logos/header-logo.png
    dark: logos/header-logo-white.png
```
:::
:::

### large {#large}

The `large` attribute defines the logo for large display contexts, such as title slides or marketing materials.

It has the same properties as `small` and `medium`.
Note that `light` and `dark` variants can also refer to named `images` resources (show in the second example).

::: {.grid style="--bs-columns:2"}
::: {.g-col-2 .g-col-lg-1}
```{.yaml filename="_brand.yml"}
logo:
  large: logos/full-logo.svg
```
:::

::: {.g-col-2 .g-col-lg-1}
```{.yaml filename="_brand.yml"}
logo:
  images:
    full: logos/full-logo.svg
    full-white: logos/full-logo-white.svg
  large:
    light: full
    dark: full-white
```
:::
:::



--------------------------------------------------------------------------------
/docs/brand/meta.qmd:
--------------------------------------------------------------------------------
---
title: Metadata
pagetitle: "meta | brand.yml"
---

## About

The `meta` section in a `_brand.yml` provides a place to store metadata about the company or project described in the file.
This information may be used by tools that support brand.yml to add social media icons, links, footers, etc.
It can also be used as a place to store additional context about the company or brand that you'd like to store in a common place.

## Structure

The `meta` section primarily consists of two main components:

1.  [name](#name): The name of the company or brand
2.  [link](#link): URLs to the brand's online presence

Both `name` and `link` are optional fields, and you can add additional fields as needed for your specific use case.

## Examples

Here are some examples of how you might use the `meta` section in your `_brand.yml` file:

### Minimal Example

``` {.yaml filename="_brand.yml"}
meta:
  name: Acme Corporation
  link: https://www.acmecorp.com
```

### Comprehensive Example

``` {.yaml filename="_brand.yml"}
meta:
  name:
    full: Acme Corporation International
    short: Acme
  link:
    home: https://www.acmecorp.com
    docs: https://docs.acmecorp.com
    github: https://github.com/acmecorp
    bluesky: https://bsky.app/profile/acmecorp.bsky.social
    twitter: https://twitter.com/acmecorp
    linkedin: https://www.linkedin.com/company/acmecorp
    facebook: https://www.facebook.com/acmecorp
  description: |
    Acme Corporation is a leading provider of innovative solutions for cartoon
    characters worldwide.
  founded: 1952
```

## Attributes

### Name {#name}

The `name` field can be specified in two ways:

1.  As a simple string, representing the full name of the company or brand:

    ``` {.yaml filename="_brand.yml"}
    meta:
      name: Acme Corporation
    ```

2.  As an object with `full` and `short` properties:

    ``` {.yaml filename="_brand.yml"}
    meta:
      name:
        full: Acme Corporation International
        short: Acme
    ```

    This format is useful when you need to distinguish between a full company name and a shorter version depending on context.

### Link {#link}

The `link` field can also be specified in two ways:

1.  As a simple string, representing the main website of the company or brand:

    ``` {.yaml filename="_brand.yml"}
    meta:
      link: https://www.acmecorp.com
    ```

2.  As an object with multiple properties representing different online presences:

    ``` {.yaml filename="_brand.yml"}
    meta:
      link:
        home: https://www.acmecorp.com
        github: https://github.com/acmecorp
        bluesky: https://bsky.app/profile/acmecorp.bsky.social
        linkedin: https://www.linkedin.com/company/acmecorp
    ```

    This format allows you to record links to the homepage and related social media accounts used by your brand.
    Note that links should be full URLs, including the `https://` prefix.



--------------------------------------------------------------------------------
/docs/brand/spec/brand-color.yml:
--------------------------------------------------------------------------------
- id: brand-color-value
  schema: string

- id: brand-color
  description: >
    The brand's custom color palette and theme.
  object:
    closed: true
    properties:
      with:
        description: >
          The brand's custom color palette. Any number of colors can be defined,
          each color having a custom name.
        object:
          closed: false
          # We don't know the exact properties yet, but we do know they'll all be strings.
          # I'm not sure how to express that in the spec.
          additionalProperties:
            schema:
              ref: brand-color-value
      foreground:
        description: The foreground color, used for text.
        schema:
          ref: brand-color-value
        default: black
      background:
        description: The background color, used for the page background.
        schema:
          ref: brand-color-value
        default: white
      primary:
        description: >
          The primary accent color, i.e. the main theme color. Typically used for
          hyperlinks, active states, primary action buttons, etc.
        schema:
          ref: brand-color-value
      secondary:
        description: >
          The secondary accent color. Typically used for lighter text or disabled states.
        schema:
          ref: brand-color-value
      tertiary:
        description: >
          The tertiary accent color. Typically an even lighter color, used for hover states,
          accents, and wells.
        schema:
          ref: brand-color-value
      success:
        description: The color used for positive or successful actions and information.
        schema:
          ref: brand-color-value
      info:
        description: The color used for neutral or informational actions and information.
        schema:
          ref: brand-color-value
      warning:
        description: The color used for warning or cautionary actions and information.
        schema:
          ref: brand-color-value
      danger:
        description: The color used for errors, dangerous actions, or negative information.
        schema:
          ref: brand-color-value
      light:
        description: >
          A bright color, used as a high-contrast foreground color on dark elements
          or low-contrast background color on light elements.
        schema:
          ref: brand-color-value
      dark:
        description: >
          A dark color, used as a high-contrast foreground color on light elements
          or high-contrast background color on light elements.
        schema:
          ref: brand-color-value
      emphasis:
        description: >
          A color used to emphasize or highlight text or elements.
        schema:
          ref: brand-color-value
      link:
        description: >
          The color used for hyperlinks. If not defined, the `primary` color is used.
        schema:
          ref: brand-color-value

- id: brand-maybe-named-color
  description: >
    A color, which may be a named brand color.
  anyOf:
    - ref: brand-named-theme-color
    - schema: string

- id: brand-named-theme-color
  description: >
    A named brand color, taken either from `color.theme` or `color.palette` (in that order).
  enum:
    [
      foreground,
      background,
      primary,
      secondary,
      tertiary,
      success,
      info,
      warning,
      danger,
      light,
      dark,
      emphasis,
      link,
    ]



--------------------------------------------------------------------------------
/docs/brand/spec/brand-defaults.yml:
--------------------------------------------------------------------------------
- id: brand-defaults
  description: >
    Additional format or output-specific options, used as a template
    for these settings in those contexts.
  object:
    properties:
      quarto:
        object:
          properties:
            format:
              description: Quarto format options.
              schema: object
            website:
              description: Quarto `website` options.
              schema: object
            book:
              description: Quarto `book` options.
              schema: object
      bootstrap:
        description: Bootstrap theme settings, similar to `bslib::bs_theme()`.
        object:
          closed: true
          properties:
            uses: string
            functions: string
            defaults:
              description: Sass variables.
              schema: object
              namingConvention: kebab-case
            mixins: string
            rules: string
      shiny:
        description: Settings specific to Shiny applications.
        schema: object



--------------------------------------------------------------------------------
/docs/brand/spec/brand-logo.yml:
--------------------------------------------------------------------------------
- id: brand-logo
  description: >
    Provide definitions and defaults for brand's logo in various formats and sizes.
  anyOf:
    - string
    - object:
        closed: true
        properties:
          images:
            schema:
              object:
                additionalProperties:
                  schema:
                    ref: brand-string-light-dark
          small:
            description: >
              A link or path to the brand's small-sized logo or icon, or a link or path
              to both the light and dark versions.
            schema:
              ref: brand-string-light-dark
          medium:
            description: >
              A link or path to the brand's medium-sized logo, or a link or path
              to both the light and dark versions.
            schema:
              ref: brand-string-light-dark
          large:
            description: >
              A link or path to the brand's large- or full-sized logo, or a link or path
              to both the light and dark versions.
            schema:
              ref: brand-string-light-dark



--------------------------------------------------------------------------------
/docs/brand/spec/brand-meta.yml:
--------------------------------------------------------------------------------
- id: brand-meta
  description: >
    Metadata for a brand, including the brand name and important links.
  object:
    closed: false
    properties:
      name:
        description: The brand name.
        anyOf:
          - string
          - object:
              properties:
                full:
                  string:
                    description: The full, official or legal name of the company or brand.
                short:
                  string:
                    description: The short, informal, or common name of the company or brand.
      link:
        description: >
          Important links for the brand, including social media links.
          If a single string, it is the brand's home page or website.
          Additional fields are allowed for internal use.
        anyOf:
          - string
          - object:
              properties:
                home:
                  string:
                    description: The brand's home page or website.
                mastodon:
                  string:
                    description: The brand's Mastodon URL.
                github:
                  string:
                    description: The brand's GitHub URL.
                linkedin:
                  string:
                    description: The brand's LinkedIn URL.
                twitter:
                  string:
                    description: The brand's Twitter URL.
                facebook:
                  string:
                    description: The brand's Facebook URL.



--------------------------------------------------------------------------------
/docs/brand/spec/brand-typography.yml:
--------------------------------------------------------------------------------
- id: brand-typography
  description: Typography definitions for the brand.
  object:
    closed: true
    properties:
      with:
        description: Font files and definitions for the brand.
        ref: brand-font
      base:
        description: >
          The base font settings for the brand. These are used as the default for all text.
        ref: brand-typography-options
      headings:
        description: >
          The font settings for headings.
        ref: brand-typography-options-no-size
      monospace:
        description: >
          The font settings for monospace text. Color in this context refers to inline code.
        ref: brand-typography-options
      emphasis:
        description: The text properties used for emphasized (or emboldened) text.
        object:
          closed: true
          properties:
            weight:
              ref: brand-font-weight
            color:
              ref: brand-maybe-named-color
            background-color:
              ref: brand-maybe-named-color
      link:
        description: The text properties used for hyperlinks.
        object:
          closed: true
          properties:
            weight:
              ref: brand-font-weight
            decoration: string
            color:
              schema:
                ref: brand-maybe-named-color
              default: primary
            background-color:
              ref: brand-maybe-named-color

- id: brand-typography-options
  description: Typographic options.
  object:
    closed: true
    properties:
      family: string
      size: string
      line-height: string
      weight:
        ref: brand-font-weight
      style:
        ref: brand-font-style
      color:
        ref: brand-maybe-named-color
      background-color:
        ref: brand-maybe-named-color

- id: brand-typography-options-no-size
  description: Typographic options without a font size.
  object:
    closed: true
    properties:
      family: string
      line-height: string
      weight:
        ref: brand-font-weight
      style:
        ref: brand-font-style
      color:
        ref: brand-maybe-named-color
      background-color:
        ref: brand-maybe-named-color

- id: brand-font
  description: Font files and definitions for the brand.
  arrayOf:
    anyOf:
      - ref: brand-font-google
      - ref: brand-font-file
      - ref: brand-font-family

- id: brand-font-weight
  description: A font weight.
  enum: [100, 200, 300, 400, 500, 600, 700, 800, 900]
  default: 400

- id: brand-font-style
  description: A font style.
  enum: [normal, italic]
  default: normal

- id: brand-font-google
  description: A Google Font definition.
  object:
    closed: true
    properties:
      google:
        anyOf:
          - string
          - object:
              closed: true
              properties:
                family:
                  description: The font family name, which must match the name of the font on Google Fonts.
                  schema: string
                weight:
                  description: The font weights to include.
                  maybeArrayOf:
                    ref: brand-font-weight
                  default: [400, 700]
                style:
                  description: The font style to include.
                  maybeArrayOf:
                    ref: brand-font-style
                  default: [normal, italic]
                display:
                  description: >
                    The font display method, determines how a font face is font face is shown
                    depending on its download status and readiness for use.
                  enum: [auto, block, swap, fallback, optional]
                  default: swap

- id: brand-font-file
  description: A method for providing font files directly, either locally or from an online location.
  object:
    closed: true
    properties:
      family:
        description: The font family name.
        schema: string
      files:
        maybeArrayOf:
          anyOf: [path, string]
        description: >
          The font files to include. These can be local or online.
          Local file paths should be relative to the `brand.yml` file.
          Online paths should be complete URLs.

- id: brand-font-family
  description: >
    A locally-installed font family name. When used, the end-user is responsible
    for ensuring that the font is installed on their system.
  schema: string



--------------------------------------------------------------------------------
/docs/brand/spec/brand.yml:
--------------------------------------------------------------------------------
- name: meta
  schema:
    ref: brand-meta

- name: logo
  schema:
    ref: brand-logo

- name: color
  schema:
    ref: brand-color

- name: typography
  schema:
    ref: brand-typography

- name: template
  schema:
    ref: brand-template



--------------------------------------------------------------------------------
/docs/brand/spec/brand_definitions.yml:
--------------------------------------------------------------------------------
- id: brand-string-light-dark
  anyOf:
    - string
    - object:
        closed: true
        properties:
          light: string
          dark: string



--------------------------------------------------------------------------------
/docs/brand/typography.qmd:
--------------------------------------------------------------------------------
---
title: Typography
pagetitle: "typography | brand.yml"
code-annotations: select
---

## About

Typography is a crucial element of any brand's visual identity.
The `typography` section in `_brand.yml` allows you to define the fonts, sizes, weights, and other typographic properties.

## Structure

You can approach translating brand guidelines into a `_brand.yml` file in two steps:

1.  First, specify **the fonts used** by your brand, using local or online font sources.

    -   [fonts](#fonts): This top-level attribute is where you list font family definitions.

2.  Second, define the **fonts and styles** used by different typographic elements (base text, headings, monospace text, etc.).
    The [remaining attributes of `typography`](#typography-attributes) comprise these settings:

    * `base` \
      Font and appearance settings for the base (body) text.

    * `headings` \
      Font and appearance settings for heading text.

    * `monospace` \
      Font and appearance settings for monospaced text.

    * `monospace-inline` \
      Font and appearance settings for inline monospaced text.

    * `monospace-block` \
      Font and appearance settings for block (multi-line) monospaced text.

    * `link` \
      Font and appearance settings for hyperlink text.

## Examples

### Minimal Example

At its most minimal[^more-minimal], you can directly set the font families for base text, headings, and monospace text.

[^more-minimal]: All parts of brand.yml are optional, so you could even more minimally set only one of `base`, `headings` or `monospace`. And the absolute minimum, of course, would be to exclude the `typography` section entirely.

``` {.yaml filename="_brand.yml"}
typography:
  base: Open Sans
  headings: Roboto Slab
  monospace: Fira Code
```

This saves a bit of typing and is equivalent to the following.

``` {.yaml filename="_brand.yml"}
typography:
  base:
    family: Open Sans
  headings:
    family: Roboto Slab
  monospace:
    family: Fira Code
```

Currently, Quarto and Shiny assume that a font family mentioned in the `typography` section is available on the user's system.
To use fonts from [Google Fonts](https://fonts.google.com/) or [Bunny Fonts](https://bunny.net/) (a GDPR-compliant Google Fonts replacement), define the font sources in `fonts`.

``` {.yaml filename="_brand.yml"}
typography:
  fonts:
    - family: Open Sans
      source: google
    - family: Roboto Slab
      source: google
    - family: Fira Code
      source: google
  base: Open Sans
  headings: Roboto Slab
  monospace: Fira Code
```

### Simple Example with Additional Properties

Typography encompasses more than just the font selection.
This example also sets typographic properties such as line height, font size, and color:

``` {.yaml filename="_brand.yml"}
color:
  primary: blue
typography:
  base:
    family: Open Sans
    line-height: 1.25
    size: 1rem
  headings:
    family: Roboto Slab
    color: primary
    weight: semi-bold
  monospace:
    family: Fira Code
    size: 0.9em
```

### Comprehensive Example with Font Definitions

This example demonstrates how to define fonts from various sources and apply them to different text elements:

``` {.yaml filename="_brand.yml"}
color:
  primary: "#f24242"
typography:
  fonts:
    # Local files # <1>
    - family: Open Sans # <1>
      source: file # <1>
      files: # <1>
        - path: fonts/open-sans/OpenSans-Variable.ttf # <1>
        - path: fonts/open-sans/OpenSans-Variable-Italic.ttf # <1>
          style: italic # <1>
    # Online files # <2>
    - family: Closed Sans # <2>
      source: file # <2>
      files: # <2>
        - path: https://example.com/Closed-Sans-Bold.woff2 # <2>
          weight: bold # <2>
        - path: https://example.com/Closed-Sans-Italic.woff2 # <2>
          style: italic # <2>
    # Google Fonts # <3>
    - family: Roboto Slab # <3>
      source: google # <3>
      weight: [600, 900] # <3>
      style: normal # <3>
      display: block # <3>
    # Bunny Fonts # <4>
    - family: Fira Code # <4>
      source: bunny # <4>

  base:
    family: Open Sans # <5>
    line-height: 1.25
    size: 1rem
  headings:
    family: Roboto Slab # <5>
    color: primary
    weight: 600
  monospace:
    family: Fira Code # <5>
    size: 0.9em
```

1.  **Local fonts** use `source: file` and typically come as a set of files, each with a `weight` and `style`. List each font file under `files` with a `path` attribute, optionally specifying the `weight` and `style` associated with the font file.
2.  **Online font files** might be hosted somewhere by the company or brand. These also use `source: file` (see local fonts above), but the `path` attribute is a URL.
3.  **Google Fonts** define an entire family of fonts. Here `weight` and `style` select the weights and styles that should be included in the fonts downloaded from Google Fonts.
4.  **Bunny Fonts** follow the same format as Google Fonts but use a GDPR-compliant host.
5.  Fonts are referenced by `family` name in the other attributes of `typography`. Note that not all `fonts` need to be used, but they'll be made available by Quarto or Shiny.

### Example with Color Definitions

Colors defined in the [color section](color.qmd) can be referenced by name in the `color` and `background-color` attributes of the typography settings.
Note that this applies to both [theme colors](color.qmd#theme-colors) and colors in the brand's color [palette](color.qmd#palette).

``` {.yaml filename="_brand.yml"}
color:
  palette:
    red: "#FF6F61"
  primary: "#87CEEB"
  secondary: "#50C878"
  danger: red
  foreground: "#1b1818"
  background: "#f7f4f4"

typography:
  headings:
    color: primary
  monospace-inline:
    color: background
    background-color: red
  monospace-block:
    color: foreground
    background-color: background
  link:
    color: danger
```

## Attributes

### fonts {#fonts}

The `fonts` attribute is a list of font family definitions.
Each definition describes a font family that is available to the brand.
Fonts may be stored in files (either adjacent to `_brand.yml` or hosted online) or may be provided by Google Fonts or Bunny Fonts.

Local fonts are specified using `source: file` and typically consist of multiple files, each representing a different weight and style.
To use local fonts, list each file under the `files` section, providing a `path` attribute and optionally specifying the `weight` and `style` for each file.

For fonts hosted online by a company or brand, you can use the same `source: file` approach as local fonts, but instead of a local file path, you'll use a URL in the `path` attribute.

``` yaml
typography:
  fonts:
    # Local files
    - family: Open Sans
      source: file
      files:
        - path: fonts/open-sans/OpenSans-Variable.ttf
        - path: fonts/open-sans/OpenSans-Variable-Italic.ttf
          style: italic
    # Online files
    - family: Closed Sans
      source: file
      files:
        - path: https://example.com/Closed-Sans-Bold.woff2
          weight: bold
        - path: https://example.com/Closed-Sans-Italic.woff2
          style: italic
```

Google Fonts offers entire font families at once, and uses a slightly different syntax.
With Google Fonts, you can specify which weights and styles should be included in the downloaded font package using the `weight` and `style` attributes.
Bunny Fonts provide a GDPR-compliant alternative to Google Fonts and follow the same format for implementation.

``` yaml
typography:
  fonts:
    # Google Fonts
    - family: Roboto Slab
      source: google
      weight: [600, 900] # <1>
      style: normal # <2>
    # Bunny Fonts
    - family: Fira Code
      source: bunny
```

1.  The `weight` attribute specifies the font weights to include in the downloaded font package. In this example, weights 600 and 900 are included. Leaving this empty includes weights from 100 to 900. Variable font weights can be written as a string `600..900`.
2.  The `style` attribute specifies the font styles to include in the downloaded font package. In this example, only the normal style is included. Leaving this empty includes both normal and italic styles as `[normal, italic]`.

In other typography-related attributes, fonts are referenced by their `family` name.
It's worth noting that while you can define multiple fonts, not all of them need to be actively used in your project.
However, Quarto or Shiny will make all defined fonts available for potential use.

### Typography Attributes

The following attributes are used to define the typographic properties of different text elements.

+--------------------+--------------------------------------------------------------------------------------------------------+------------------------+
| Attribute          | Description                                                                                            | Supported Fields       |
+====================+========================================================================================================+========================+
| `base`             | Default text, primarily used in the document body.                                                     | -   `family`           |
|                    |                                                                                                        | -   `size`             |
|                    |                                                                                                        | -   `line-height`      |
|                    |                                                                                                        | -   `weight`           |
+--------------------+--------------------------------------------------------------------------------------------------------+------------------------+
| `headings`         | All heading levels (h1, h2, etc.).                                                                     | -   `family`           |
|                    |                                                                                                        | -   `weight`           |
|                    |                                                                                                        | -   `style`            |
|                    |                                                                                                        | -   `line-height`      |
|                    |                                                                                                        | -   `color`            |
+--------------------+--------------------------------------------------------------------------------------------------------+------------------------+
| `monospace`        | General monospaced text, typically used in code blocks and other programming-related content.          | -   `family`           |
|                    |                                                                                                        | -   `size`             |
|                    |                                                                                                        | -   `weight`           |
+--------------------+--------------------------------------------------------------------------------------------------------+------------------------+
| `monospace-inline` | Inline monospaced text, usually used for code snippets within regular text. Inherits from `monospace`. | -   `family`           |
|                    |                                                                                                        | -   `size`             |
|                    |                                                                                                        | -   `weight`           |
|                    |                                                                                                        | -   `color`            |
|                    |                                                                                                        | -   `background-color` |
+--------------------+--------------------------------------------------------------------------------------------------------+------------------------+
| `monospace-block`  | Block (multi-line) monospaced text, typically used for code blocks. Inherits from `monospace`.         | -   `family`           |
|                    |                                                                                                        | -   `size`             |
|                    |                                                                                                        | -   `weight`           |
|                    |                                                                                                        | -   `line-height`      |
|                    |                                                                                                        | -   `color`            |
|                    |                                                                                                        | -   `background-color` |
+--------------------+--------------------------------------------------------------------------------------------------------+------------------------+
| `link`             | Hyperlinks.                                                                                            | -   `weight`           |
|                    |                                                                                                        | -   `color`            |
|                    |                                                                                                        | -   `background-color` |
|                    |                                                                                                        | -   `decoration`       |
+--------------------+--------------------------------------------------------------------------------------------------------+------------------------+

: {tbl-colwidths="[20,50,30]"}

The supported fields are generally described as follows:

- `family`: The font family to be used for a typographic element. This should match a font resource declared in `typography.fonts`.

- `size`: The font size for a typographic element. Should be specified using a CSS length unit (e.g., "14px", "1em", "0.9rem").

- `weight`: The font weight (or boldness) of the text. Can be a numeric value between 100 and 900, or a string like "normal" or "bold".

- `style`: The font style for the text, typically either "normal" or "italic".

- `line-height`: The line height of the text, which refers to the vertical space between lines. Often expressed as a multiple of the font size or in fixed units.

- `color`: The color of the text. Can be any CSS-compatible color definition or a reference to a color defined in the brand's color palette.

- `background-color`: The background color for the text element. Can be any CSS-compatible color definition or a reference to a color defined in the brand's color palette.

- `decoration`: The text decoration, typically used for links. Common values include "underline", "none", or "overline".



--------------------------------------------------------------------------------
