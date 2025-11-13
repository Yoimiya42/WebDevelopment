
# HTML Syntax

## Basics

The `<!DOCTYPE>` declaration represents the documents type, and helps browsers to display web page correctly.  

The `<html>` define the root of the HTML document, we should should always include the `lang` attribute inside the this tag, to declare the language of the Web page. This is meant to assist search engines and browsers.  
For example: `<html lang="en-GB">`, `<html lang="en_US">`,`<html, lang="zh-CN">`,`<html lang="zh-HK"`...  

`&lt` less than, to display `<`   
`&gt` greater than, to display `>`    
`&amp` ampersand, to display `&`  
`&quot` double quote, to display `"`  
`&nbsp` non-breaking space, to display a space that will not break into a new line.  
 

## Head Elements
`<head>` contains metadata about the document, and not displayed on the page.  
- `<title>` define the title of this document, shown in the browser title bar or page tab
- define the character set for the document, UTF-8 is the most common character set.
   ```html 
  <meta charset="UTF-8">
    ``` 
- For Search Engine Optimization (SEO):
  ```html
  <meta name="description" content="define the description of the page">
  <meta name="keywords" content="define the keywords for search engine">
  <meta name="author" content="the name of web author">
  ```
- Refresh the page every 30 seconds:
  ```html
  <meta http-equiv="refresh" content="30">
  ```
- `link` is most often to link to the external style sheets:
  ```html
  <link rel="stylesheet" href="styles.css">
  ```
  and set the favicon for the page:
  ```html
  <link rel="icon" type="image/x-icon" href="favicon.ico">
  ```
- `base` tag specifies the base URL for all relatives URLs in a page:
  ```html
  <base href="http://www.example.com/" target="_blank">
  ```
  So in this document, all following hyperlinks can use relative URLs which based on `http://www.example.com/`.

## Hyperlinks
`<a>` defines a hyperlink, syntax:
```html     
<a href="url">Visible content</a>
```
- Absolute URL: use the full URL to link to a web page
- Relative URL: link to a page within the same website or folder
- `title` attribute: provides additional description of the link,     displayed as a tooltip when mouse over the link
- `target` attribute:
  - `_blank` open in a **new window/tab**
  - `_self` open in the **current window/tab**   

You can create bookmarks in a page:
```html
<h2 id="C7">Chapter 7></h2>   <!-- destination -->
<a href="#C7">Jump to Chapter 7</a> 
<!-- use the '#' followed by the id of the destination -->
```

## Images

`<img>` tag is used to embed an image into page. Syntax:
  ```html
  <img src="url" alt="text" width="100" height="100">
  ```
  - `src` specifies the absolute/relative path of the image
  - `alt` provides an alternate text for this image, displayed when the image is not loaded(maybe cause by slow connection, error in src attribute, under a screen reader, etc.)
  - `width` and `height` specify the size of the image in **pixels**.
  - you can use the property `float` of `style` tp float the image to the left/right of the text.
 
## Paragraphs

- `<p>` starts with a new line, a block of text 
  - `<h1> ... <h6>` heading tags from largest to smallest
  - `<p title="text">` title attribute, displayed as a tooltip when mouse over the text
- `<br>` line break  
- `<hr>` horizontal line  
- The text inside a `<pre>`  is displayed in a **fixed-width** font, and it **preserves both spaces and line breaks**.
- `<!-- comment -->` comments in HTML


## Formatting

- `<b>` bold text, `<strong>` has the same visual effect with additional semantic meaning.
- `<i>` italic text, `<em>` has the same visual effect with additional semantic meaning.
- `<mark>`  highlight text  
- `<u>` underline text  
  
- `<del>` deleted text  
- `<ins>` insert text  
  
- `<sub>` subscript text
- `<sup>` superscript text  


## Quotation

- Browsers automatically indent all content within the `<blockquote>`.
- `<q>` defines a short quotation, quotation marks will be added around the quotation.
- The contact information(email address, URLs, physical address, phone number, social media handle,etc,) within `<address>` will be displayed in **italic** style.
- `<abbr>` 
  ```html
  <!--template-->
  <p><abbr title="Full name">Abbreviation</abbr></p>

  <p>The <abbr title="Cascading Style Sheets">CSS</abbr> is used to design the web page.</p>
  ```
  Use global `title` attribute to show the description for abbreviation when the mouse over the abbreviation. 

## Color

- **RGB color**:  
   `rgb(red, green, blue )` or `#rrggbb`
   black: ``rgb(0,0,0)` or ` #000000`
   white: `rgb(255,255,255)` or` #ffffff`
   grey:  red = green = blue
- **RGBA color**: 
  `rgba(red,green,blue,alpha)`
  "A" means `alpha channel`, control the transparency of the color, **0.0 is fully transparency and 1.0 is fully opaque**

  