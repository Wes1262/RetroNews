# RetroNews

**Retro computing news and guides archive**

------------------------------------------------------------------------------------------------------------------------

<img src="./embeds/logo192.png" align="right">

**Retro computer information has been steadily disappearing from the internet.** While _archive.org_ does an excellent
job most of the time, archived pages can sometimes fail to save correctly or become unusable later on. This often
happens due to the heavy use of JavaScript on these sites or, in some cases, major hardware failures at _archive.org_.
With this repository, we aim to manually preserve interesting news articles, guides, and resources for retro computing
enthusiasts, ensuring they remain accessible even when the original pages are lost.

<small>**Note:** despite sharing similar goals to _The Retro Web_'s, and despite having a deliberately similar logo,
this repository is in no way affiliated with them. </small>

## How to archive a news page or a guide?

1. First of all, perform a search for the page(s) you want to archive in this _github_ repository,<br>
   as the page(s) might have been archived already!

2. Otherwise, identify the _second level domain_ of the page you want to archive.<br>
   For example: The _SLD_ of `https://www.anandtech.com/show/970` is `anandtech.com`

3. Head to the folder for such _SLD_, or create it if it doesn't exist.<br>
   For example: `./archive/anandtech.com/`

4. Perform a `sha1` on the title of the page (or the first page) that you want to archive.<br>
   For example: `sha1("ATI Radeon 9700 Pro - Delivering as Promised")`

5. Create a folder whose name is the result of the `sha1` call.<br>
   For example: `./archive/anandtech.com/9d779bb21ee9ed8d7adbb86d5111cf7d4010fe3e/`

6. Open the folder and create the following sub-folders: `images`, `screenshots`.<br>
   For example: `./archive/anandtech.com/9d779bb21ee9ed8d7adbb86d5111cf7d4010fe3e/screenshots/`

7. Create full-page screenshots using _Chrome Dev Tools_ (or equivalent) of the relevant page(s) and save them into the
   `screenshots` folder as `1.png` if there is only one page, `2.png` for the second page, `3.png` for the third, etc.
   Also include the screenshots, or the the relevant source code fragments, even if the result is not "pretty", as these files are not meant to be read directly; they are kept for historical and attribution reasons.
   For example: `./archive/anandtech.com/9d779bb21ee9ed8d7adbb86d5111cf7d4010fe3e/screenshots/1.png`
   or `./archive/anandtech.com/9d779bb21ee9ed8d7adbb86d5111cf7d4010fe3e/screenshots/1.md` for source code.

8. Create a `readme.md` file under the main `sha1` folder.
   For example: `./archive/anandtech.com/9d779bb21ee9ed8d7adbb86d5111cf7d4010fe3e/screenshots/`

9. Copy the following _markdown_ structure to that file:

```
# Article or guide title using the original language and formatting

**Site:** anandtech.com
**Date:** YYYY-MM-DD HH:SS
**Author:** Author
**Archived URL:** https://www.anandtech.com/show/970
**Keywords:** `review` `9700` `pro` `ati`



   Wrap Line Length of 128
```



| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | <img src="./embeds/logo96.png" width="50%" height="10">  |
| Content Cell  | <img src="./embeds/logo96.png" width="100%" height="10">  |