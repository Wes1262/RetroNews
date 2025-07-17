# RetroNews

**Retro computing news and guides archive**

------------------------------------------------------------------------------------------------------------------------

<img src="./embeds/logo192.png" align="right">

**Retro computer information has been steadily disappearing from the internet.** While _archive.org_ does an excellent
job most of the time, archived pages can sometimes fail to save correctly or become unusable later on. This often
happens due to the heavy use of JavaScript on these sites or, in some cases, major hardware failures at _archive.org_.
**With this repository, we aim to manually preserve interesting news articles, guides, and resources for retro computing
enthusiasts, ensuring they remain accessible even when the original pages are lost.**

<small>**Note:** despite sharing similar goals to _The Retro Web_'s, and despite having a deliberately similar logo,
this project is in no way affiliated with them. </small>

------------------------------------------------------------------------------------------------------------------------

## Removal request

If you are the owner of one the archived documents and you want them removed from this repository — first of all, are
you sure you want us to forget old documents that are only significant to retro computer enthusiasts? If you are,
contact us via the _Issues_ section and we will remove them promptly after proving your identity. You will be asked to
send us an email from the same domain of the archived site, or via a similar method.

------------------------------------------------------------------------------------------------------------------------

## How to archive a news page or a guide?

<!--------------------------------------------------------------------------------------------------------------------->

### 1. Check for duplicates

First of all, perform a search for the page(s) that you want to archive in this _github_ repository, as the page(s) might
have been archived already!

<!--------------------------------------------------------------------------------------------------------------------->

### 2. Prepare your _git_

Fork this repository to your _github_ account, clone it to your computer if you want.

<!--------------------------------------------------------------------------------------------------------------------->

### 3. Determine the _eTLD+1_
Otherwise, identify the _eTLD+1_ of the page you want to archive. The _eTLD+1_ of a _URL_ is the _second level domain_
part of the _URL_, plus its _eTLD_ suffix such as `.com`, `.net`, or `.co.uk`.

> Example: `https://www.anandtech.com/show/970` is `anandtech.com`.<br>
> Example: `https://forums.overclockers.co.uk/t/ati-radeon-x850-xt.../` is `overclockers.co.uk`.

<!--------------------------------------------------------------------------------------------------------------------->

### 4. Locate the base folder for the _eTLD+1_

In your local clone, head to the folder for such a _eTLD+1_, or create it if it doesn't exist.

> Example: `./archive/anandtech.com/`

<!--------------------------------------------------------------------------------------------------------------------->

### 5. Determine the date of the document

Determine the document's _ISO Date_ and note it down. If the date is not explicitly specified, try to guess it depending
on the content of the page. E.g. a review for a new graphics card will be published shortly after the release of the
card. If you can't determine with absolute certainty the day, the month, or even the year, replace the corresponding
digits with lowercase `x`s.

> Example: `2002-07-19`, `2002-07-xx`, `2002-xx-xx`, `xxxx-xx-xx`

<!--------------------------------------------------------------------------------------------------------------------->

### 6. Create a _pathified_ version of the document's title

If the title is not in english, translate it appropriately using sensible capitalization; i.e. own-names with capital
first letter and acronyms in all-caps. This is highly subjective, so just try to make it look good. Use only _ASCII_
letters, numbers and _hyphens_ (`0x2D`). Drop any other character. Avoid contiguous, trailing and leading _hyphens_.

> Example: `ATI-Radeon-9700-Pro-Delivering-as-promised`<br>
> Wrong: `ATI-Radeon-9700-Pro--Delivering-as-promised`<br>
> Wrong: `ATI-Radeon-9700-Pro-Delivering-as-promised-`<br>
> Wrong: `-ATI-Radeon-9700-Pro-Delivering-as-promised`<br>
> Wrong: `ATI Radeon 9700 Pro - Delivering as promised`<br>

<!--------------------------------------------------------------------------------------------------------------------->

### 7. Create the base folder for the document

Create a folder whose name is the concatenation of the _ISO Date_, a _hyphen_, and the "_pathified_" title.

> Example: `./archive/anandtech.com/2002-07-19-ATI-Radeon-9700-Pro-Delivering-as-promised/`

<!--------------------------------------------------------------------------------------------------------------------->

### 8. Create the file structure for the document

Open the directory that was just created and stub the following sub-folders and files: `attachments/`,
`screenshots/`, `readme.md`.

> Example: `./archive/anandtech.com/2002-07-19-ATI-`...`-promised/screenshots/`<br>
> Example: `./archive/anandtech.com/2002-07-19-ATI-`...`-promised/attachments/`<br>
> Example: `./archive/anandtech.com/2002-07-19-ATI-`...`-promised/readme.md`<br>

<!--------------------------------------------------------------------------------------------------------------------->

### 9. Archive the screenshots of the document

Create "_full-page screenshots_" using _Chrome Dev Tools_ (or equivalent) of the relevant page(s), and save them into
the `screenshots` folder as `1.png` if there is only one page, `2.png` for the second page, `3.png` for the third, etc.
Include such screenshots (or alternatively relevant source code fragments) even if the result is not "pretty", as these
files are not meant to be read directly but kept for historical and attribution reasons.

> Example: `./archive/anandtech.com/2002-07-19-ATI-`...`-promised/screenshots/1.png`<br>
> Example: `./archive/anandtech.com/2002-07-19-ATI-`...`-promised/screenshots/2.txt`<br>
> Example: `./archive/anandtech.com/2002-07-19-ATI-`...`-promised/screenshots/3.htm`<br>

<!--------------------------------------------------------------------------------------------------------------------->

### 10. Convert the document to _Markdown_

Copy the following _Markdown_ structure to the `readme.md` file and edit it as explained. Keep everything original;
do not translate the text to english, do not remove any typos, improve grammar or punctuation. If you feel an improved
version of the text is absolutely required for the document to be useful, you can create a _corrected copy_, which is
explained later in this guide.

**This file must have hard line wraps at 120 characters.**

```md
# Article or guide title using the original language and formatting

**URL:**      https://anandtech.com/show/970 <!-- Preferably a permalink, if any. -->
**Date:**     YYYY-MM-DD                     <!-- ISO Dates... no 'murican dates. -->
**Time:**     23:44 Europe/Rome              <!-- Time is rarely important but you can include it if necessary. -->
**Author:**   Anand Lal Shimpi               <!-- The author, if known, otherwise omit this line. -->
**Keywords:** Review, Khan                   <!-- Extra keywords; words not already included in the page's body. -->

## First paragraph/page title.

First paragraph/page text.

## Second paragraph/page title.

Second paragraph/page text.
```

<!--------------------------------------------------------------------------------------------------------------------->

### 11. Improve the page with embed images

You can improve the result by embedding the original pictures in the document. Download the images from the original
site and save them to the `attachments` folder. To name such files, use the same pattern previously used to _pathify_
the document title. Use names that make sense, and that are easily searchable.

> Example: `./archive/`...`/attachments/Radeon-9700-Pro-box.jpg`<br>

You may generate smaller clickable thumbnails in the main document, by keeping them in the `thumbnails` folder. It is
very unlikely that thumbnails are necessary though, as image resolution of old webpages is usually very low already.

> Example: `./archive/`...`/attachments/thumbnails/Radeon-9700-Pro-box.png`<br>

Floating images **must** have a _width_ of 33% and they can be attached to both the _left_ and _right_ margins.
Instead, block images must be centered and their width should be determined automatically by _github_.

**Simple floating image:**

```html
<img src="./attachments/Radeon-9700-Pro-box.jpg"
    alt="[ATI Radeon 9700 Pro's retail box]" width="33%" align="right">
```

**Zoomable floating image:**

```html
<a href="./attachments/Radeon-9700-Pro-box.jpg">
    <img src="./attachments/thumbnails/Radeon-9700-Pro-box.jpg"
        alt="[ATI Radeon 9700 Pro's retail box]" width="33%" align="left">
</a>
```

**Simple block image:**

```html
<div align="center">
    <img src="./attachments/Radeon-9700-Pro-box.jpg"
        alt="[ATI Radeon 9700 Pro's retail box]">
</div>
```

**Zoomable block image:**

```html
<div align="center">
    <a href="./attachments/Radeon-9700-Pro-box.jpg">
        <img src="./attachments/thumbnails/Radeon-9700-Pro-box.jpg"
            alt="[ATI Radeon 9700 Pro's retail box]">
    </a>
</div>
```

### 12. Replace bar-graphs with table equivalents

You may use _HTML_ tables or _markdown_ <abbr title="sdf">equivalent</abbr> to re-crate the original bar-graphs on _github_:

<table align="center">
    <thead>
        <tr>
            <th colspan="4" align="center">
                Serious Sam 2<br>
                Little Trouble @ 1024x768
            </th>
        </tr>
        <tr>
            <th>Graphics Card</th>
            <th width="300">Graph</th>
            <th>Avg. FPS</th>
            <th>% Delta</th>
        </tr>
    </thead>
    <tbody
    <tr>
        <td>ATI Radeon 9700 Pro</td>
        <td><img src="./embeds/16.png" height="10" width="100%" alt="100%"></td>
        <td>130.3</td>
        <td>0%</td>
    </tr>
    <tr>
        <td>NVIDIA GeForce4 Ti 4600</td>
        <td><img src="./embeds/9.png" height="10" width="86%" alt="86.11%"></td>
        <td>112.2</td>
        <td>-13.89%</td>
    </tr>
</table>