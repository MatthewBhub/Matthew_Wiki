Welcome to the Example Wiki Page!
This page demonstrates how you can combine standard Markdown syntax with raw HTML for more control over your content, especially for images.

Standard Markdown Elements
Here's a regular paragraph of text. You can use bold text, italic text, and even inline code.

Lists
Item one

Item two

Sub-item A

Sub-item B

Item three

Links
You can link to other pages or external websites:
Visit Google
Go to another wiki page (assuming 'AnotherPage.md' exists)

Images with HTML for Sizing
Now, let's look at how to embed images using HTML to control their size. Remember that DOMPurify is sanitizing this HTML for safety.

1. Standard Markdown Image (No explicit size)
This image will be rendered by marked.js with its default behavior (and typically max-width: 100%; height: auto; from your CSS).

2. Image with width and height attributes
You can specify exact pixel dimensions for your image using HTML attributes.

<img src="https://placehold.co/400x200/FF0000/FFFFFF?text=Fixed+400x200" alt="Fixed size image" width="400" height="200">

3. Image with style attribute for responsive sizing
Use inline styles for more flexible control, like percentages or max-width.

<img src="https://placehold.co/800x300/00FF00/000000?text=Responsive+50%25+Max+300px" alt="Responsive image" style="width: 50%; max-width: 300px; border-radius: 8px;">

4. Image with Tailwind CSS classes
If your wiki.css or Tailwind setup includes utility classes, you can use them directly.

<img src="https://placehold.co/100x100/0000FF/FFFFFF?text=Tailwind" alt="Tailwind styled image" class="w-32 h-32 rounded-full shadow-lg mx-auto block">

Security Demonstration (DOMPurify in Action)
This section contains an example of potentially unsafe HTML. Thanks to DOMPurify, the malicious part will be removed, and only the safe content (the paragraph) will be displayed.

<p>This paragraph is safe content.</p>
<script>alert('This script should NOT execute!');</script>
<img src="invalid.jpg" onerror="alert('This onerror should NOT trigger!');">

Note: You should not see any pop-up alerts from the <script> tag or the onerror attribute above. If you do, it indicates a security issue. DOMPurify is designed to strip these out, making your content safe for display.

Thank you for visiting this example page!
