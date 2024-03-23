---
title: Design Elements
toc: toc-design.html
print: print-button.html
---

I am using the [CSS Reference](https://www.w3schools.com/cssref/index.php){:target="blank"} and much more from W3Schools to learn how to be stylish. This is the best reference out there. Try to avoid the rat holes of Stack Overflow when searching for how to do something.

All of the design elements you see here are implemented by the style sheet in **assets/css**. Some features require the use of HTML in markdown file. When you edit these files, you will see how.

### <span style="color:#069">Site Menu Made Easy</span>
If you want the site menu button to appear in the upper left corner of the page header, update **_includes/site-menu.html** and then call it out in **_config.yml** using the site **menu** varariable. If not specified in the config file, the button will not be displayed.

### <span style="color:#069">TOC Made Easy</span>
Open **_includes/toc-design.html** to see just how easy it is. Each header in a page will be assigned an **id** that you can reference in the TOC, with spaces in the header repaced with dashes when the site is built.

**TIP:** If you use any non-alphanumeric characters in your headers, you may need to view the page source in your browser to get the **id** that was assigned. Those characters may be removed.

After you have created a TOC **html** file, you need to call it out in the **front matter** of the page using the **title, toc** and optional **print** variable, like this:

```
---
title: Design Elements
toc: toc-design.html
print: print-button.html
---
<blank line>
I am using the CSS Reference from W3Schools...
```

---

### Media Screen Styles
Fully optimized for viewing on small screens by reducing font sizes, header sizes, bottom margins and left/right page margins for all content. Grids are reset to one column. Description and logo are removed from header. Tagline is removed from footer. When designing your pages, it's important to consider how they are going to look on phones and tablets.

### Media Print Style
Description and all link buttons are removed from header. Footer is removed.

---

### Color Scheme and Table Style
The colors are shown using html "<span style=...>" in the markdown. This [color site](https://www.color-hex.com/){:target="_blank"} is a good reference.

| Color1 | Color2 | Selector |
| ------ | ------ | -------- |
| <span style="background:#6C7989;padding:2px 16px;color:white;">#6C7989</span> | <span style="background:#434B55;padding:2px 16px;color:white;">#434B55</span> | html background, footer background (color2) |
| <span style="background:#069;padding:2px 17px;color:white;">#006699</span> | | header (h1, p, li, toc-button, border}, th |
| <span style="background:#d1e5fc;padding:2px 14px;">#D1E5FC</span> | <span style="background:#b3d5fb;padding:2px 12px;">#B3D5FB</span> | header background, drop-content background |
| <span style="background:aliceblue;padding:2px 16px">aliceblue</span> | | wrapper background (content) |
| <span style="background-color:#e0eefd;padding:2px 14px">#E0EEFD</span> | | tr:even |
| <span style="background-color:white;padding:2px 28px">white</span> | | tr:hover |
| <span style="background:azure;padding:2px 28px;">azure</span> | | blockquote background |
| <span style="background:silver;padding:2px 28px">silver</span> | | border: th, td, toc-button, menu-button, footer |

---

### Image Styles
Use one of the custom **image classes** to to create a picture frame or round over the corners:

```
<img width="20%" src="images/zion-np.jpg">
 <img class="img-noborder" width="20%" src="images/zion-np.jpg">
 <img class="img-border2" width="20%" src="images/zion-np.jpg">
 <img class="img-border4" width="20%" src="images/zion-np.jpg">
```

<img width="20%" src="images/zion-np.jpg">
 <img class="img-noborder" width="20%" src="images/zion-np.jpg">
 <img class="img-border2" width="20%" src="images/zion-np.jpg">
 <img class="img-border4" width="20%" src="images/zion-np.jpg">

---

## Other Elements
#### <span style="color:#069">Code Highlighting</span>
This is the default Rouge highlighter for GitHub Pages. Many other options are available.

```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

#### <span style="color:#069">Formatted Text</span>
<pre>
Formatted monospace text
Without highlighting by using html < pre > tag.
</pre>

#### <span style="color:#069">List Item Spacing</span>
Lists with a little space between. Easy to find and adjust in the style sheet.

1. numbered list with break<br>
more text
2. two
3. three

* bullet list with break<br>
more text
* next bullet
    * four spaces to get nested bullet with break<br>
    and more text
    * and one more
    * last nested bullet
* last one

#### <span style="color:#069">Blockquote</span>

> blockquote text with break<br>more text
>
> second paragraph

#### <span style="color:#069">Keyboard Keys</span>
Press <kbd>Ctrl</kbd> + <kbd>c</kbd>

```
Press <kbd>Ctrl</kbd> + <kbd>c</kbd>
```

#### <span style="color:#069">Definition List</span>

Style Sheet
: Lets people know  how stylish you are

Wrapper (Generic Term)
: Used to encapsulate content on a web page

HTML Grids
: Used to encapsulate content on a web page in a defined pattern of columns or rows.

# Test Header1
content
## Test Header2
content
### Test Header3
content
#### Test Header4
content
##### Test Header5
content
###### Test Header6
content

---

### Grid Styles
Placing text and other content next to an image can be done in several ways and gets really complicated really fast, but I got his working with grid classes in the style sheet and html in the markdown. This appears to be the only way to create a grid out of markdown. You will see how when you edit **test.md**.

You can run wild with these, provided you don't mind editing raw html in your pages, which is prone to the slightest slip or miss that makes your web page run wild, too. Easy to copy/paste the basic structure needed and then fill in the content.

### 50-50 Grid
Each element in the grid starts with a horizontal rule that spans the width of the column, with a 32px gap.

Other grid classes include **grid-6633 and grid-3366**. Like I said, you can run wild.

<div class="grid-5050">
<div class="grid-c1">
<hr>
<h4>First Element in the Grid</h4>
<p>With image width=50%</p>
<img width="50%" class="img-border2" src="images/zion-np.jpg">
</div>
<div class="grid-c2">
<hr>
<h4>Second Element</h4>
<hr>
<p>Virgin River - Zion National Park</p>
<hr>
<p>800x600 image resized to fit 50% of the grid column.</p>
</div>
<div class="grid-c1">
<hr>
<h4>Third Element</h4>
<p>Formatted text. Code highlighting doesn't work here.</p>
<pre>
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
</pre>
</div>
<div class="grid-c2">
<hr>
<h4>Fourth Element</h4>
<p>More content</p>
</div>
</div>

Next markdown paragraph after the grid.

---

### 66-33 Grid

<div class="grid-6633">
<div class="grid-c1">
<hr>
<h4>First Element in the Grid</h4>
<p>With image width=66%</p>
<img width="66%" class="img-noborder" src="images/zion-np.jpg">
</div>
<div class="grid-c2">
<hr>
<h4>Second Element</h4>
<hr>
<p>Virgin River - Zion National Park</p>
<hr>
</div>
</div>

Next markdown paragraph after the grid.

---

### Pipe Testing
Using the Pipe/Vertical Bar Symbol yields table cells

| One pipe, one table data cell

| Two pipes with image after the second  | <img class="img-border2" width="160" src="images/zion-np.jpg">

---

End of Document
