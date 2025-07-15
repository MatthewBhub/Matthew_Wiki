# HTML Parsing Examples ✨

This document demonstrates the ability to parse and render raw HTML embedded directly within Markdown. Your marked.js library will convert this Markdown (including the HTML) into a single HTML string, and DOMPurify will then sanitize it before it's displayed on your page.

-----

## 1\. Basic HTML Elements

You can include standard HTML tags like paragraphs, headings, and lists.

```html
<p>This is a paragraph written in <strong>raw HTML</strong>.</p>
<h3>A Smaller Heading</h3>
<ul>
  <li>List item one</li>
  <li>List item two</li>
</ul>
<ol>
  <li>Ordered item A</li>
  <li>Ordered item B</li>
</ol>
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
<div style="background-color: #e0f7fa; padding: 15px; border-radius: 8px; margin-bottom: 20px;">
  <h4 style="color: #00796b; text-align: center;">Styled Box Example</h4>
  <p style="font-family: 'Georgia', serif; font-size: 1.1em; color: #333;">
    This text is inside a `div` with a light blue background, rounded corners,
    and a specific font.
  </p>
</div>
<span style="color: purple; font-weight: bold;">This is a purple, bold span.</span>
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
<p>Here's an image embedded directly via HTML:</p>
<img
  src="https://placehold.co/300x150/FF6347/FFFFFF?text=HTML+Image"
  alt="Placeholder HTML Image"
  style="border: 2px solid tomato; border-radius: 5px; display: block; margin: 10px 0;"
/>
<p>
  And a
  <a
    href="https://www.example.com"
    target="_blank"
    style="color: #007bff; text-decoration: underline;"
    >link to an external website</a
  >.
</p>
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
<table style="width: 100%; border-collapse: collapse; margin-top: 20px;">
  <thead>
    <tr style="background-color: #f2f2f2;">
      <th style="border: 1px solid #ddd; padding: 8px; text-align: left;">
        Header 1
      </th>
      <th style="border: 1px solid #ddd; padding: 8px; text-align: left;">
        Header 2
      </th>
      <th style="border: 1px solid #ddd; padding: 8px; text-align: left;">
        Header 3
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="border: 1px solid #ddd; padding: 8px;">Data A1</td>
      <td style="border: 1px solid #ddd; padding: 8px;">Data A2</td>
      <td style="border: 1px solid #ddd; padding: 8px;">Data A3</td>
    </tr>
    <tr style="background-color: #f9f9f9;">
      <td style="border: 1px solid #ddd; padding: 8px;">Data B1</td>
      <td style="border: 1px solid #ddd; padding: 8px;">Data B2</td>
      <td style="border: 1px solid #ddd; padding: 8px;">Data B3</td>
    </tr>
  </tbody>
</table>
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
<details
  style="border: 1px solid #ccc; padding: 10px; border-radius: 5px; margin-top: 20px;"
>
  <summary style="font-weight: bold; cursor: pointer; color: #0056b3;">
    Click to reveal more information
  </summary>
  <p style="margin-top: 10px;">
    This content is hidden by default and appears when you click the summary.
  </p>
  <input type="checkbox" id="myCheckbox" name="myCheckbox" />
  <label for="myCheckbox"> Check me!</label>
</details>
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
<p>
  The following script tag will be removed by DOMPurify. You should
  <strong>not</strong> see an alert box when this page loads.
</p>
<script>
  alert('This alert should NOT appear!');
</script>
<p>
  Also, an `onclick` attribute like this:
  <button onclick="alert('This button click should NOT work!');">
    Click Me (Unsafe)
  </button>
  will have its `onclick` attribute removed, making the button safe but
  non-functional.
</p>
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
