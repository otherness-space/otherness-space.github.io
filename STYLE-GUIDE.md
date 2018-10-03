# [Style Guide](https://github.com/otherness-space/blank-repository/blob/master/STYLE-GUIDE.md#style-guide)

## Contents

##### [About](#1-about) | [General](#2-general) | [HTML](#3-html) | [CSS](#4-css) | [Notes](#5-notes)

## 1 About

-   This document is based on the [Google HTML/CSS style guide](https://google.github.io/styleguide/htmlcssguide.html) and others, as cited.
-   The purpose of this document is to define the format and style for HTML and CSS. The syntax of this document is [GitHub Flavored Markdown](https://help.github.com/articles/basic-writing-and-formatting-syntax) (GFM), licensed under [Attribution-ShareAlike 4.0 International](https://creativecommons.org/licenses/by-sa/4.0), and has been validated by [linter-markdown 5.2.2](https://atom.io/packages/linter-markdown).

## 2 General
-   ### 2.1 General Style
    -   #### 2.1.1 Protocol
    -   Use the HTTPS protocol for embedded resources where possible
-   ### 2.2 General Format
    -   #### 2.2.1 Indentation
    -   Two spaces per `tab`
    -   Use [Atom-Beautify](https://atom.io/packages/atom-beautify) to format
    -   #### 2.2.2 Capitalization
    -   Use only lowercase unless `text/CDATA`
    -   #### 2.2.3 Trailing whitespace
    -   Remove trailing white spaces.
-   ### 2.3 General Meta
    -   #### 2.3.1 Encoding
    -   Use UTF-8 (no BOM). Make sure your editor uses UTF-8 as character encoding, without a byte order mark.
    -   #### 2.3.2 Comments
    -   Explain where possible
    -   #### 2.3.3 Action items
    -   Mark todos and action items only with keyword `TODO`.
    -   Append a contact `TODO(John)`
    -   Append action items after a colon as in `TODO : action item`

## 3 HTML
-   ### 3.1 HTML Style
    -   #### 3.1.1 Document Type
    -   HTML5 (HTML syntax) is preferred for all HTML documents: `<!DOCTYPE html>`
    -   #### 3.1.2 HTML Validity
    -   Use valid HTML where possible.
    -   [Example](https://google.github.io/styleguide/htmlcssguide.html#HTML_Validity)
    -   #### 3.1.3 Semantics
    -   Use HTML according to its purpose.
    -   Use elements (sometimes incorrectly called “tags”) for what they have been created for. For example, use heading elements for headings, p elements for paragraphs, a elements for anchors, etc.
    -   Using HTML according to its purpose is important for accessibility, reuse, and code efficiency reasons.
    -   #### 3.1.4 Multimedia Fallback
    -   Provide alternative contents for multimedia.
    -   For multimedia, such as images, videos, animated objects via `canvas`, make sure to offer alternative access. For images that means use of meaningful alternative text (`alt`) and for video and audio transcripts and captions, if available.
    -   #### 3.1.5 Separation of Concerns
    -   Strictly keep structure (markup), presentation (styling), and behavior (scripting) apart, and try to keep the interaction between the three to an absolute minimum.
    -   That is, make sure documents and templates contain only HTML and HTML that is solely serving structural purposes. Move everything presentational into style sheets, and everything behavioral into scripts.
    -   In addition, keep the contact area as small as possible by linking as few style sheets and scripts as possible from documents and templates.
    -   #### 3.1.6 Entity References
    -   There is no need to use entity references like `&mdash;`, `&rdquo;`, or `&#x263a;`, assuming the same encoding (UTF-8) is used for files and editors as well as among teams.
    -   The only exceptions apply to characters with special meaning in HTML (like `<` and `&`) as well as control or “invisible” characters (like no-break spaces).
    -   #### 3.1.7 Optional Tags (subjective)
    -   Omit optional tags (optional) BUT PLAY WELL WITH OTHERS.
    -   For file size optimization and scannability purposes, consider omitting optional tags. The [HTML5 specification](https://html.spec.whatwg.org/multipage/syntax.html#syntax-tag-omission) defines what tags can be omitted.
    -   #### 3.1.8 `type` Attributes
    -   Do not use `type` attributes for style sheets (unless not using CSS) and scripts (unless not using JavaScript).
    -   Specifying `type` attributes in these contexts is not necessary as HTML5 implies `text/css` and `text/javascript` as defaults.
-   ### 3.2 HTML Format
    -   #### 3.2.1 General Formatting
    -   Use a new line for every block, list, or table element, and indent every such child element.
    -   Also, indent them if they are child elements of a block, list, or table element.
    -   #### 3.2.2 Line-Wrapping
    -   Use soft wrap in your text editor.
    -   #### 3.2.3 Quotation Marks
    -   Double quotes.

## 4 CSS
-   ### 4.1 CSS Style
    -   #### 4.1.1 CSS Validity
    -   Use valid CSS where possible.
    -   #### 4.1.2 ID and Class Naming
    -   Use meaningful or generic ID and class names.
    -   Names that are specific and reflect the purpose of the element should be preferred as these are most understandable and the least likely to change.
    -   Using functional or generic names reduces the probability of unnecessary document or template changes.
    -   #### 4.1.3 ID and Class Name Style
    -   Use ID and class names that are as short as possible but as long as necessary.
    -   Try to convey what an ID or class is about while being as brief as possible.
    -   Using ID and class names this way contributes to acceptable levels of understandability and code efficiency.
    -   #### 4.1.4 Type Selectors
    -   Avoid qualifying ID and class names with type selectors.
    -   Unless necessary (for example with helper classes), do not use element names in conjunction with IDs or classes.
    -   #### 4.1.5 Shorthand Properties
    -   CSS offers a variety of [shorthand](https://www.w3.org/TR/CSS21/about.html#shorthand) properties (like `font`) that should be used whenever possible, even in cases where only one value is explicitly set.
    -   #### 4.1.6 0 and Units
    -   Do not use units after `0` values unless they are required.
    -   #### 4.1.7 Leading 0s
    -   Do not put `0`s in front of values or lengths between -1 and 1.
    -   #### 4.1.8 Hexadecimal Notation
    -   For color values that permit it, 3 character hexadecimal notation is shorter and more succinct.
    -   #### 4.1.9 Prefixes
    -   In large projects as well as for code that gets embedded in other projects or on external sites use prefixes (as namespaces) for ID and class names. Use short, unique identifiers followed by a dash.
    -   `adw-help {} /* AdWords */`
    -   #### 4.1.10 ID and Class Name Delimiters
    -   Separate words in ID and class names by a hyphen.
    -   Do not concatenate words and abbreviations in selectors by any characters (including none at all) other than hyphens, in order to improve understanding and scannability.
    - `.ads-sample {}`
    -   #### 4.1.11 Hacks
    -   Avoid user agent detection as well as CSS “hacks”—try a different approach first.
    -   It’s tempting to address styling differences over user agent detection or special CSS filters, workarounds, and hacks. Both approaches should be considered last resort in order to achieve and maintain an efficient and manageable code base. Put another way, giving detection and hacks a free pass will hurt projects in the long run as projects tend to take the way of least resistance. That is, allowing and making it easy to use detection and hacks means using detection and hacks more frequently—and more frequently is too frequently.
-   ### 4.2 CSS Format
    -   #### 4.2.1 Declaration Order[1](#521-code-declaration) and Grouping[2](#522-grouping)[3](#523-property-order)[4](#524-css-style-guides) `TODO : edit`
    -   NO ALPHA
    -   1. Positioning
    -   Positioning comes first because it can remove an element from the normal flow of the document and override box model related styles.
    -   2. Box model (display, float, width, etc)
    -   The box model comes next as it dictates a component's dimensions and placement.
    -   3. Typography (font, line-height, text-*)
    -   Everything else takes place inside the component or without impacting the previous two sections, and thus they come last.
    -   4. Visuals (background, border, opacity)
    -   5. Misc (CSS3 properties)
    -   #### 4.2.2 Block Content Indentation
    -   Indent all block content.
    -   #### 4.2.3 Declaration Stops
    -   Use a semicolon after every declaration.
    -   #### 4.2.4 Property Name Stops
    -   Use a space after a property name’s colon.
    -   `font-weight: bold;`
    -   #### 4.2.5 Declaration Block Separation
    -   Always use a single space between the last selector and the opening brace that begins the declaration block.
    -   `#video {`
    -   #### 4.2.6 Selector and Declaration Separation
    -   `h1,`
    -   `h2,`
    -   `h3 `
    -   #### 4.2.7 4.2.7 Rule Separation
    -   Always put a blank line (two line breaks) between rules.
    -   `html {`
    -   `background: #fff;`
    -   `}`
    -
    -   `body {`
    -   `margin: auto;`
    -   `width: 50%;`
    -   `}`
    -   #### 4.2.8 Quotation Marks
    -   Single not double
-   ### 4.3 [Material Design](https://material.io/)
    -   #### 4.3.1 Material Design [Responsive Grid Breakpoints](https://material.io/design/layout/responsive-layout-grid.html#breakpoints) `TODO`
    -   Material Design provides responsive layouts based on the following column structures. Layouts using 4-column, 8-column, and 12-column grids are available for use across different screens, devices, and orientations.
    -   Each breakpoint range determines the number of columns, and recommended margins and gutters, for each display size.

| Breakpoint Range (dp) | Portrait | Landscape | Window | Columns | Margins / Gutters* |
|--------|--------|--------|--------|--------|--------|
| 0 – 359 |        |        |    xs  |    4   |   16   |
| 360 – 399 |        |        |  xs    |   4    |   16   |
| 400 – 479 |        |        |  xs    |    4   |   16   |
| 480 – 599 |        |        |  xs    |    4   |   16   |
| 600 – 719 |        |        |   s    |    8   |   16   |
| 720 – 839 |        |        |   s    |    8   |   24   |
| 840 – 959 |        |        |    s   |    12  |   24   |
| 960 – 1023 |        |        |    s   |   12   |   24   |
| 1024 – 1279 |        |        |   m    |  12    |  24    |
| 1280 – 1439 |        |        |   m    |  12    |  24    |
| 1440 – 1599 |        |        |   l    |  12    |  24    |
| 1600 – 1919 |        |        |    l   |  12    |  24    |
| 1920 + |        |        |   xl   |   12   |   24   |
|        |        |        |        |        |        |
|        |        |        |        |        |        |

**Margins and gutters are flexible and don’t need to be of equal size.*

-   ### `TODO`
    -   #### 4.3.2 Material Columns
    -   Content is placed in the areas of the screen that contain columns.
    -   Column width is defined using percentages, rather than fixed values, to allow content to flexibly adapt to any screen size. The number of columns displayed in the grid is determined by the breakpoint range (a range of predetermined screen sizes) at which a screen is viewed, whether it’s a breakpoint for mobile, tablet, or another size.
    -   #### 4.3.3 Material Gutters
    -   Gutters are the spaces between columns. They help separate content.
    -   Gutter widths are fixed values at each breakpoint range. To better adapt to the screen, gutter width can change at different breakpoints. Wider gutters are more appropriate for larger screens, as they create more whitespace between columns.
    -   #### 4.3.4 Material Margins
    -   Margins are the space between content and the left and right edges of the screen.
    -   Margin widths are defined as fixed values at each breakpoint range. To better adapt to the screen, the margin width can change at different breakpoints. Wider margins are more appropriate for larger screens, as they create more whitespace around the perimeter of content.
    -   #### 4.3.5 Material Horizontal Grids
    -   The Material Design layout grid can be customized for touch UIs that scroll horizontally. Columns, gutters, and margins are laid out from left to right, rather than top to bottom. The height of the screen determines the number of columns in a horizontal grid.
    -   Horizontally scrolling UIs are uncommon on non-touch and web platforms.
    -   Horizontal grids can be positioned to accommodate different heights, allowing space for app bars or other UI regions at the top.

-   ### 4.4 CSS Meta
    -   #### 4.4.1 Section Comments
    -   Group sections by a section comment (optional).
    -   If possible, group style sheet sections together by using comments. Separate sections with new lines.
    -   `/* Header */`
    -   `#adw-header {}`
    -   `/* Footer */`
    -   `#adw-footer {}`
    -   `/* Gallery */`
    -   `.adw-gallery {}`

## 5 Notes
-   ### 5.1 Be consistent and REMEMBER [syntax tag omission](https://html.spec.whatwg.org/multipage/syntax.html#syntax-tag-omission)
-   ### 5.2
    -   #### 5.2.1 [Code Declaration](http://codeguide.co/#css-declaration-order)
    -   #### 5.2.2 [Grouping](https://smacss.com/book/formatting#grouping)
    -   #### 5.2.3 [Property Order](https://styleguide.github.com/primer/principles/#property-order)
    -   #### 5.2.4 [CSS Style Guides](https://css-tricks.com/css-style-guides/)
