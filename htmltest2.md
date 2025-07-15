# HTML Parsing Examples ✨

This document demonstrates the ability to parse and render raw HTML embedded directly within Markdown. Your marked.js library will convert this Markdown (including the HTML) into a single HTML string, and DOMPurify will then sanitize it before it's displayed on your page.

-----

## 1\. Basic HTML Elements

You can include standard HTML tags like paragraphs, headings, and lists.

```html
&lt;p&gt;This is a paragraph written in &lt;strong&gt;raw HTML&lt;/strong&gt;.&lt;/p&gt;
&lt;h3&gt;A Smaller Heading&lt;/h3&gt;
&lt;ul&gt;
  &lt;li&gt;List item one&lt;/li&gt;
  &lt;li&gt;List item two&lt;/li&gt;
&lt;/ul&gt;
&lt;ol&gt;
  &lt;li&gt;Ordered item A&lt;/li&gt;
  &lt;li&gt;Ordered item B&lt;/li&gt;
&lt;/ol&gt;
```

\<p\>This is a paragraph written in \<strong\>raw HTML\</strong\>.\</p\>
\<h3\>A Smaller Heading\</h3\>
\<ul\>
\<li\>List item one\</li\>
\<li\>List item two\</li\>
\</ul\>
\<ol\>
\<li\>Ordered item A\</li\>
\<li\>Ordered item B\</li\>
\</ol\>

-----

## 2\. HTML with Inline Styling

You can also apply inline CSS styles to your HTML elements.

```html
&lt;div style="background-color: #e0f7fa; padding: 15px; border-radius: 8px; margin-bottom: 20px;"&gt;
  &lt;h4 style="color: #00796b; text-align: center;"&gt;Styled Box Example&lt;/h4&gt;
  &lt;p style="font-family: 'Georgia', serif; font-size: 1.1em; color: #333;"&gt;
    This text is inside a `div` with a light blue background, rounded corners,
    and a specific font.
  &lt;/p&gt;
&lt;/div&gt;
&lt;span style="color: purple; font-weight: bold;"&gt;This is a purple, bold span.&lt;/span&gt;
```

\<div
style="background-color: \#e0f7fa; padding: 15px; border-radius: 8px; margin-bottom: 20px;"
\>
\<h4 style="color: \#00796b; text-align: center;"\>Styled Box Example\</h4\>
\<p style="font-family: 'Georgia', serif; font-size: 1.1em; color: \#333;"\>
This text is inside a div with a light blue background, rounded corners, and
a specific font.
\</p\>
\</div\>
\<span style="color: purple; font-weight: bold;"
\>This is a purple, bold span.\</span
\>

-----

## 3\. Images and Links

HTML `<img>` and `<a>` tags work as expected.

```html
&lt;p&gt;Here's an image embedded directly via HTML:&lt;/p&gt;
&lt;img
  src="https://placehold.co/300x150/FF6347/FFFFFF?text=HTML+Image"
  alt="Placeholder HTML Image"
  style="border: 2px solid tomato; border-radius: 5px; display: block; margin: 10px 0;"
/&gt;
&lt;p&gt;
  And a
  &lt;a
    href="https://www.example.com"
    target="_blank"
    style="color: #007bff; text-decoration: underline;"
    &gt;link to an external website&lt;/a
  &gt;.
&lt;/p&gt;
```

\<p\>Here's an image embedded directly via HTML:\</p\>
\<img
src="[https://placehold.co/300x150/FF6347/FFFFFF?text=HTML+Image](https://placehold.co/300x150/FF6347/FFFFFF?text=HTML+Image)"
alt="Placeholder HTML Image"
style="border: 2px solid tomato; border-radius: 5px; display: block; margin: 10px 0;"
/\>
\<p\>
And a
\<a
href="[https://www.example.com](https://www.example.com)"
target="\_blank"
style="color: \#007bff; text-decoration: underline;"
\>link to an external website\</a
\>.
\</p\>

-----

## 4\. Tables

Complex layouts like tables can be created using HTML.

```html
&lt;table style="width: 100%; border-collapse: collapse; margin-top: 20px;"&gt;
  &lt;thead&gt;
    &lt;tr style="background-color: #f2f2f2;"&gt;
      &lt;th style="border: 1px solid #ddd; padding: 8px; text-align: left;"&gt;
        Header 1
      &lt;/th&gt;
      &lt;th style="border: 1px solid #ddd; padding: 8px; text-align: left;"&gt;
        Header 2
      &lt;/th&gt;
      &lt;th style="border: 1px solid #ddd; padding: 8px; text-align: left;"&gt;
        Header 3
      &lt;/th&gt;
    &lt;/tr&gt;
  &lt;/thead&gt;
  &lt;tbody&gt;
    &lt;tr&gt;
      &lt;td style="border: 1px solid #ddd; padding: 8px;"&gt;Data A1&lt;/td&gt;
      &lt;td style="border: 1px solid #ddd; padding: 8px;"&gt;Data A2&lt;/td&gt;
      &lt;td style="border: 1px solid #ddd; padding: 8px;"&gt;Data A3&lt;/td&gt;
    &lt;/tr&gt;
    &lt;tr style="background-color: #f9f9f9;"&gt;
      &lt;td style="border: 1px solid #ddd; padding: 8px;"&gt;Data B1&lt;/td&gt;
      &lt;td style="border: 1px solid #ddd; padding: 8px;"&gt;Data B2&lt;/td&gt;
      &lt;td style="border: 1px solid #ddd; padding: 8px;"&gt;Data B3&lt;/td&gt;
    &lt;/tr&gt;
  &lt;/tbody&gt;
&lt;/table&gt;
```

\<table style="width: 100%; border-collapse: collapse; margin-top: 20px;"\>
\<thead\>
\<tr style="background-color: \#f2f2f2;"\>
\<th style="border: 1px solid \#ddd; padding: 8px; text-align: left;"\>
Header 1
\</th\>
\<th style="border: 1px solid \#ddd; padding: 8px; text-align: left;"\>
Header 2
\</th\>
\<th style="border: 1px solid \#ddd; padding: 8px; text-align: left;"\>
Header 3
\</th\>
\</tr\>
\</thead\>
\<tbody\>
\<tr\>
\<td style="border: 1px solid \#ddd; padding: 8px;"\>Data A1\</td\>
\<td style="border: 1px solid \#ddd; padding: 8px;"\>Data A2\</td\>
\<td style="border: 1px solid \#ddd; padding: 8px;"\>Data A3\</td\>
\</tr\>
\<tr style="background-color: \#f9f9f9;"\>
\<td style="border: 1px solid \#ddd; padding: 8px;"\>Data B1\</td\>
\<td style="border: 1px solid \#ddd; padding: 8px;"\>Data B2\</td\>
\<td style="border: 1px solid \#ddd; padding: 8px;"\>Data B3\</td\>
\</tr\>
\</tbody\>
\</table\>

-----

## 5\. Interactive Elements (Static)

Elements like `<details>` and `<input type="checkbox">` can provide basic interactivity without JavaScript, which is safe to embed.

```html
&lt;details
  style="border: 1px solid #ccc; padding: 10px; border-radius: 5px; margin-top: 20px;"
&gt;
  &lt;summary style="font-weight: bold; cursor: pointer; color: #0056b3;"&gt;
    Click to reveal more information
  &lt;/summary&gt;
  &lt;p style="margin-top: 10px;"&gt;
    This content is hidden by default and appears when you click the summary.
  &lt;/p&gt;
  &lt;input type="checkbox" id="myCheckbox" name="myCheckbox" /&gt;
  &lt;label for="myCheckbox"&gt; Check me!&lt;/label&gt;
&lt;/details&gt;
```

\<details
style="border: 1px solid \#ccc; padding: 10px; border-radius: 5px; margin-top: 20px;"
\>
\<summary style="font-weight: bold; cursor: pointer; color: \#0056b3;"\>
Click to reveal more information
\</summary\>
\<p style="margin-top: 10px;"\>
This content is hidden by default and appears when you click the summary.
\</p\>
\<input type="checkbox" id="myCheckbox" name="myCheckbox" /\>
\<label for="myCheckbox"\> Check me\!\</label\>
\</details\>

-----

## 6\. DOMPurify Sanitization Example (Important\! 🔒)

**DOMPurify** is crucial for security. It will remove potentially malicious content like `<script>` tags, `on*` event handlers, and other unsafe attributes.

```html
&lt;p&gt;
  The following script tag will be removed by DOMPurify. You should
  &lt;strong&gt;not&lt;/strong&gt; see an alert box when this page loads.
&lt;/p&gt;
&lt;!-- This script tag will be stripped by DOMPurify --&gt;
&lt;script&gt;
  alert('This alert should NOT appear!');
&lt;/script&gt;
&lt;p&gt;
  Also, an `onclick` attribute like this:
  &lt;button onclick="alert('This button click should NOT work!');"&gt;
    Click Me (Unsafe)
  &lt;/button&gt;
  will have its `onclick` attribute removed, making the button safe but
  non-functional.
&lt;/p&gt;
```

\<p\>
The following script tag will be removed by DOMPurify. You should
\<strong\>not\</strong\> see an alert box when this page loads.
\</p\>
\<script\>
alert('This alert should NOT appear\!');
\</script\>
\<p\>
Also, an `onclick` attribute like this:
\<button onclick="alert('This button click should NOT work\!');"\>
Click Me (Unsafe)
\</button\>
will have its `onclick` attribute removed, making the button safe but
non-functional.
\</p\>

This demonstrates the flexibility of embedding HTML within Markdown while maintaining security through **DOMPurify**.
