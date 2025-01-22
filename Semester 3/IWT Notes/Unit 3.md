# Unit 3: Cascading Style Sheets (CSS)



### **Introduction to CSS:**
CSS (Cascading Style Sheets) is used to style and layout HTML elements on a web page. It controls the look and feel of a website, including colors, fonts, and spacing. CSS separates the content (HTML) from its presentation (style), which helps with cleaner code and better maintainability.

### **Benefits of CSS:**
- **Separation of Content and Presentation:** HTML focuses on structure, while CSS handles presentation (design).
- **Consistency:** CSS allows you to apply a consistent style across multiple pages.
- **Improved Accessibility:** CSS enables better control over layout for responsive design.
- **Faster Page Load:** By using external stylesheets, browsers can cache the CSS, improving page load times.

### **CSS Syntax:**
CSS syntax consists of **selectors** and **declarations**:
```css
selector {
    property: value;
}
```
- **Selector**: Targets the HTML element you want to style.
- **Property**: The style you want to apply (e.g., `color`, `font-size`).
- **Value**: The value for the property (e.g., `red`, `14px`).

### **CSS Implementation:**
1. **Inline CSS**: Styles are applied directly within an HTML tag using the `style` attribute:
   ```html
   <p style="color: blue;">This is a paragraph.</p>
   ```
2. **Internal CSS**: CSS is written inside the `<style>` tag in the `<head>` section of the HTML document:
   ```html
   <style>
       p {
           color: blue;
       }
   </style>
   ```
3. **External CSS**: CSS is written in a separate file (e.g., `style.css`) and linked to the HTML document:
   ```html
   <link rel="stylesheet" type="text/css" href="style.css">
   ```

### **CSS Selectors:**
CSS selectors are used to target HTML elements for styling. Here are some common types:

1. **ID Selectors** (`#`): Targets an element with a specific `id` attribute.
   ```css
   #header {
       color: red;
   }
   ```

2. **Class Selectors** (`.`): Targets elements with a specific `class` attribute.
   ```css
   .menu {
       font-size: 18px;
   }
   ```

3. **Grouping Selectors**: Groups multiple selectors to apply the same styles to different elements.
   ```css
   h1, h2, p {
       color: green;
   }
   ```

4. **Universal Selectors** (`*`): Targets all elements in the document.
   ```css
   * {
       margin: 0;
       padding: 0;
   }
   ```

5. **CSS Pseudo-classes** (`:`): Targets elements in a specific state, such as when a user hovers over a link.
   ```css
   a:hover {
       color: red;
   }
   ```

### **CSS Properties:**
Here are some commonly used CSS properties:

1. **background-color**: Sets the background color of an element.
   ```css
   body {
       background-color: lightblue;
   }
   ```

2. **background-image**: Sets an image as the background.
   ```css
   body {
       background-image: url('background.jpg');
   }
   ```

3. **border-style**: Defines the style of the element's border.
   ```css
   div {
       border-style: solid;
   }
   ```

4. **height & width**: Sets the height and width of an element.
   ```css
   div {
       height: 200px;
       width: 300px;
   }
   ```

5. **color**: Sets the text color of an element.
   ```css
   p {
       color: red;
   }
   ```

6. **text-align**: Aligns text within an element (left, center, right).
   ```css
   h1 {
       text-align: center;
   }
   ```

7. **font-family**: Specifies the font for the text.
   ```css
   p {
       font-family: Arial, sans-serif;
   }
   ```

8. **font-style**: Sets the style of the font (normal, italic, etc.).
   ```css
   em {
       font-style: italic;
   }
   ```

9. **font-size**: Specifies the size of the font.
   ```css
   p {
       font-size: 16px;
   }
   ```

10. **font-weight**: Defines the thickness of the font (normal, bold, etc.).
    ```css
    h2 {
        font-weight: bold;
    }
    ```

### **Box Model in CSS:**
The box model defines the structure of elements in terms of their **content**, **padding**, **border**, and **margin**.

1. **Content**: The actual content of the element (text, images, etc.).
2. **Padding**: The space between the content and the element's border.
   ```css
   div {
       padding: 10px;
   }
   ```

3. **Border**: The area around the padding (if any) and content.
   ```css
   div {
       border: 1px solid black;
   }
   ```

4. **Margin**: The space outside the border, creating separation from other elements.
   ```css
   div {
       margin: 20px;
   }
   ```

The total width and height of an element include the content, padding, border, and margin. For example, if you set:
```css
div {
    width: 100px;
    padding: 10px;
    border: 5px solid black;
    margin: 20px;
}
```
The total width of the element would be `100px (width) + 10px (padding left) + 10px (padding right) + 5px (border left) + 5px (border right)`, and similarly for the height.

---
