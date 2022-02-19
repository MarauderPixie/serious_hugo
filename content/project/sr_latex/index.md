---
output: hugodown::md_document
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Mimic the Shadowrun 6 Layout in LaTeX"
summary: "a complete template for all your homebrewing needs"
authors: []
tags: [sr, latex]
categories: []
date: 2020-12-04T12:37:30+01:00

# Optional external URL for project (replaces project detail page).
external_link: ""

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: "Shadowrun-Logo und Inhalte mit freundlicher Genehmigung von Pegasus Spiele unter Lizenz von Catalyst Game Labs und Topps Company, Inc. © 2020 Topps Company, Inc. Alle Rechte vorbehalten. Shadowrun ist eine eingetragene Handelsmarke von Topps Company, Inc."
  focal_point: ""
  preview_only: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
rmd_hash: d513f30c51bfd635

---

**tl;dr:** I made a $\LaTeX$ layout so my notes look somewhat like the official material. If you want to use it and feel comfortable tinkering a bit on your own, take a look at the font section of this post (to get the right ones) and [follow this link](https://u.pcloud.link/publink/show?code=XZCVskVZTWMIC2LGQ1SEcGMQLe0pWzCGHAIX) to download a zip file with the `.cls` and some other necessary ressources.

**Disclaimer**

The layout is still unfinished and pretty much work in progress. There's no (proper) ToC yet, there are problems with spacing in headings, it's all right pages, etc., but I think it's already working and looking well enough to write a post about it.

# What's this?

I never really delved deep into $\LaTeX$.

# Ressources

In order to get this thing rolling, we're going to need a few items. Here's a list.

## Alternatives to official fonts

The official books use a bunch of fonts, some commercial and maybe a bit too pricey just to get a more official feeling to your hobby, so let me point you towards the ones we can get for free and a few alternatives for the ones we can't, so that we might at least get close.

### Headers

The original font is **Njord**, which you can actually get for a reasonable \~16€. Free fonts similar to it are

-   [Montserrat](https://fonts.google.com/specimen/Montserrat) - is *really* close, it's a little bit more sleek and the only major differences are in the letters J and Q (and minor ones in E, F, L and Z); either the medium 500 or 600 weight in all caps will do
-   [Charger Sport Black Extended](https://www.whatfontis.com/FF_Charger-Sport-Black-Extended.font) - this better matches the thickness of Njord, but otherwise is off in quite a few ways

### Text Body

Mostly, the main text bodies use **Sabon LT Std**, which you can get [here](https://fontsup.com/family/sabon+lt+std.html).

### Text Boxes and Tables

There is a difference (one of many, actually) between the english and the german versions in the font used for text boxes and tables. The english versions use **Amplitude**; a great choice in my opinion, available [here](https://www.azfonts.net/families/amplitude.html). I'll leave it to you to pick the correct one(s). As of writing this, I'm not entirely sure whether the actual variant is the *Condensed* or *Compressed*. Sticking to *Regular* is probably fine. <!-- There are also several variants (e.g. _Bold_, _Book_) available, but only commercially, so we'll stick to the _Regular_ Variant. -->

Due to a lack of german umlauts (you know; ä, ö, ü), the font used there is **Switzerland Condensed**, also available [for free](https://best-font.com/fonts/download-switzerland-condensed%3A-font.html), but sadly quite different to **Amplitude** and not quite for the better. So if you're at all like me, you might consider one of these alternatives:

-   [Cheyenne Sans Medium](https://www.ffonts.net/Cheyenne-Sans-Medium.font) - gets pretty close, but it's the overall details that are off; somewhat more 'compressed' looking, wider/longer bows, that sorta thing; unfortunately, that's most noticeable in all lowercase letters
-   [Mukta Mahee](https://fonts.google.com/specimen/Mukta+Mahee) - might be a better choice, either with the *Regular 400* or the *Medium 500* weight

## Artwork

Aside from the fonts used, the most important elements of the layout are the background used on the pages, the several uses of the Shadowrun logo and the chapter pages. You can assemble these more or less easily by yourself from readily available sources (like [the fankit provided by Pegasus Press](https://www.shadowrun6.de/index.php/fanstuff-2/fankit.html)), but this wouldn't be a proper ressource guide if I wouldn't provide you the ones I use, would it?

-   **General background**
-   **Chapter background**
-   **Cover picture**

Here's another difference between the several sources and my stuff: the logo on the chapter background is darker across all original sources, sometimes even a different color (a dark, menacing red). What is used in which cases doesn't matter for this guide, but the difference is easily explained: I used the logo from previously mentioned fankit, but I think that's good enough.

# Elements of the Layout

Now to the actual $\LaTeX$ part. Let's break the layout down to some key elements. There are:

1.  the standard page 1.1 use the **general background** picture 1.2 position chapter, subchapter and pagenumber
2.  on pages where a new chapter starts, use the **chapter background** picture 2.1 orient the text and header accordingly

