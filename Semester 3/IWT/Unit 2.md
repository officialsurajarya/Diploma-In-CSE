# Unit 2 of HTML

### **Basics of HTML:**
1. **HTML Document Structure:**
   - An HTML document typically starts with `<!DOCTYPE html>`, followed by the opening `<html>` tag, `<head>`, and `<body>` tags.
   - The `<head>` tag contains metadata (like title and links to external resources), while the `<body>` tag contains the content of the web page.
   
2. **HTML Tags and Attributes:**
   - Tags are the building blocks of HTML, such as `<html>`, `<head>`, `<body>`, etc.
   - Attributes provide additional information about elements. For example, `<a href="url">` contains an attribute `href` to specify the link destination.

3. **Types of HTML Tags:**
   - **Block-level tags:** Elements like `<div>`, `<p>`, `<h1>`, etc., which take up the full width of their container.
   - **Inline tags:** Elements like `<span>`, `<a>`, `<strong>`, etc., that only take up as much width as necessary.

4. **Rules of Nesting:**
   - HTML tags should be properly nested, meaning you should close tags in reverse order to how they were opened (e.g., `<div><p></p></div>`).

5. **Basic Tags:**
   - `<html>`: Defines the HTML document.
   - `<head>`: Contains meta information like title and links.
   - `<title>`: Sets the document title (appears in the browser tab).
   - `<body>`: Contains the content that is visible on the page.

### **Page Formatting:**
1. **Paragraphs and Line Breaks:**
   - `<p>`: Defines a paragraph.
   - `<br>`: Adds a line break.
   - Non-breaking space: `&nbsp;`.

2. **Background and Layout:**
   - Change background using the `<body>` tag with `style="background-color: color;"`.
   - `<div>`: A block-level container used for grouping elements.
   - `<span>`: An inline container used for styling specific parts of text.

### **Text Formatting:**
1. **Headings:**
   - `<h1>` to `<h6>`: Define headings of different levels.
   
2. **Text Formatting Elements:**
   - `<b>`: Bold text.
   - `<strong>`: Important text (usually bold).
   - `<i>`: Italic text.
   - `<em>`: Emphasized text (usually italic).
   - `<mark>`: Marked text (highlighted).
   - `<small>`: Smaller text.
   - `<del>`: Deleted text (strikethrough).
   - `<ins>`: Inserted text (underlined).
   - `<sub>`: Subscript text.
   - `<sup>`: Superscript text.

3. **Comments:**
   - Comments are added using `<!-- comment -->`.

4. **Horizontal Lines:**
   - `<hr>`: Draws a horizontal line.

### **Creating Lists:**
1. **Ordered List:**
   - `<ol>`: Defines an ordered (numbered) list.
   - `<li>`: List item.

2. **Unordered List:**
   - `<ul>`: Defines an unordered (bulleted) list.
   - `<li>`: List item.

3. **Definition List:**
   - `<dl>`: Defines a definition list.
   - `<dt>`: Defines a term.
   - `<dd>`: Defines a description.

### **Others:**
1. **Images:**
   - `<img src="image.jpg" alt="description" />`: Embeds an image.

2. **Links:**
   - `<a href="url">Link text</a>`: Creates a hyperlink.
   - To open in a new window or tab: `<a href="url" target="_blank">Link</a>`.

3. **Anchor Links (Same Page):**
   - Use `#` to link to an area on the same page: `<a href="#section1">Go to Section 1</a>`.

4. **Table Tags:**
   - `<table>`: Defines a table.
   - `<tr>`: Table row.
   - `<td>`: Table data (cell).
   - `<th>`: Table header.
   - Tables can be used to display data but have limitations in responsiveness.

5. **Frames & IFrames:**
   - `<iframe>`: Embeds an external document within the page.

6. **Forms:**
   - `<form>`: Defines a form.
   - `<input>`, `<textarea>`, `<select>`, `<button>`: Form elements for collecting user input.

7. **XHTML:**
   - XHTML is a stricter version of HTML that follows XML syntax rules (e.g., all tags must be properly closed).
