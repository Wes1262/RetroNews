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

## How to archive a news page or a guide?

1. First of all, perform a search for the page(s) you want to archive in this _github_ repository,<br>
   as the page(s) might have been archived already!

2. Otherwise, identify the _second level domain_ of the page you want to archive.<br>
   Example: The _SLD_ of `https://www.anandtech.com/show/970` is `anandtech.com`

3. Head to the folder for such _SLD_, or create it if it doesn't exist.<br>
   Example: `./archive/anandtech.com/`

4. Determine the document's _ISO Date_ and note it down. If the date is not explicitly specified, try to determine it
   depending on the content of the page. E.g. a review for a new graphic card will be published shortly after the
   release of the card. If you can't determine with absolute certainty the day, the month,  or even the year, replace
   the corresponding digits with lowercase `x`s.<br>
   Example: `2002-07-19`, `2002-07-xx`, `2002-xx-xx`, `xxxx-xx-xx`

5. Determine the "_pathified_" document title. If the title is not in english, translate it to english as necessary. Use
   only _ASCII letters and numbers_, _spaces_  (`0x20`), and _hyphens_ (`0x2D`). Drop any other character. Avoid
   contiguous _spaces_ and contiguous _hyphens_. An _hyphen_ character must always follow and be followed by a _space_
   character.<br>
   Example: `"ATI Radeon 9700 Pro - Delivering as Promised"`<br>
   Invalid: `"ATI Radeon 9700 Pro-Delivering as Promised"`<br>
   Invalid: `"ATI Radeon 9700 Pro -- Delivering as Promised"`<br>
   Invalid: `"ATI Radeon 9700 Pro    	    	   -    	 	     Delivering as Promised"`<br>
   Invalid: `"ATI Radeon 9700 Pro - Delivering as Promised ????"`<br>

6. Create a folder whose name is the concatenation of the _ISO Date_, a _hyphen_ and the "_pathified_" title.
   Example: `./archive/anandtech.com/2002-07-19 - ATI Radeon 9700 Pro - Delivering as Promised/`

6. Open the folder and create the following sub-folders: `images`, `screenshots`.<br>
   Example: `./archive/anandtech.com/2002-07-19 - ATI Radeon 9700 Pro - Delivering as Promised/images/`

7. Create full-page screenshots using _Chrome Dev Tools_ (or equivalent) of the relevant page(s) and save them into the
   `screenshots` folder as `1.png` if there is only one page, `2.png` for the second page, `3.png` for the third, etc.
   Also include the screenshots, or the the relevant source code fragments, even if the result is not "pretty", as these files are not meant to be read directly; they are kept for historical and attribution reasons.<br>
   Example: `./archive/anandtech.com/2002-07-19 - ATI Radeon 9700 Pro - Delivering as Promised/screenshots/1.png`<br>
   Example: `./archive/anandtech.com/2002-07-19 - ATI Radeon 9700 Pro - Delivering as Promised/screenshots/1.md`<br>

8. Create a `readme.md` file under the main `sha1` folder.
   For example: `./archive/anandtech.com/9d779bb21ee9ed8d7adbb86d5111cf7d4010fe3e/screenshots/`

9. Copy the following _markdown_ structure to that file:

```
# Article or guide title using the original language and formatting

**Archived URL:** https://www.anandtech.com/show/970 <!-- Preferably a permalink, if any. -->
**Date:** YYYY-MM-DD                                 <!-- ISO Date... no 'murican dates. -->
**Author:** John Titor                               <!-- The author, or the site name. -->
**Keywords:** `review` `9700` `ati`                  <!-- Lowercase keywords to ease search. -->

```





| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | <img src="./embeds/logo96.png" width="50%" height="10">  |
| Content Cell  | <img src="./embeds/logo96.png" width="100%" height="10">  |