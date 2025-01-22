### ** Practical No: 1**
**Object:** Create web forms and pages that properly use HTTP GET and POST protocol as appropriate.

### Creating a Web Form Using GET Method:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Registration Form</title>
</head>
<body>
    <?php if (isset($_GET['form_submitted'])): ?>
        <?php if (!isset($_GET['agree'])): ?>
            <p>You have not accepted our terms of service.</p>
            <p>Go <a href="javascript:history.back()">back</a> to the form.</p>
        <?php else: ?>
            <h2>Thank You, <?php echo htmlspecialchars($_GET['firstname']) . ' ' . htmlspecialchars($_GET['lastname']); ?>!</h2>
            <p>Now you are studying in <?php echo htmlspecialchars($_GET['branch']); ?>.</p>
            <p>Go <a href="javascript:history.back()">back</a> to the form.</p>
        <?php endif; ?>
    <?php else: ?>
        <form action="" method="GET">
            <h2>Registration Form</h2>
            <label for="firstname">First name:</label>
            <input type="text" name="firstname" id="firstname" required><br><br>
            <label for="lastname">Last name:</label>
            <input type="text" name="lastname" id="lastname" required><br><br>
            <label for="branch">Branch:</label>
            <input type="text" name="branch" id="branch" required><br><br>
            <label>
                <input type="checkbox" name="agree">
                Agree to Terms of Service
            </label><br><br>
            <input type="hidden" name="form_submitted" value="1">
            <input type="submit" value="Submit">
        </form>
    <?php endif; ?>
</body>
</html>
```
**Result:** The GET method displays form data in the browser's address bar after submission.

---

### Creating a Web Form Using POST Method:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Registration Form</title>
</head>
<body>
    <?php if (isset($_POST['form_submitted'])): ?>
        <?php if (!isset($_POST['agree'])): ?>
            <p>You have not accepted our terms of service.</p>
            <p>Go <a href="javascript:history.back()">back</a> to the form.</p>
        <?php else: ?>
            <h2>Thank You, <?php echo htmlspecialchars($_POST['firstname']) . ' ' . htmlspecialchars($_POST['lastname']); ?>!</h2>
            <p>Now you are studying in <?php echo htmlspecialchars($_POST['branch']); ?>.</p>
            <p>Go <a href="javascript:history.back()">back</a> to the form.</p>
        <?php endif; ?>
    <?php else: ?>
        <form action="" method="POST">
            <h2>Registration Form</h2>
            <label for="firstname">First name:</label>
            <input type="text" name="firstname" id="firstname" required><br><br>
            <label for="lastname">Last name:</label>
            <input type="text" name="lastname" id="lastname" required><br><br>
            <label for="branch">Branch:</label>
            <input type="text" name="branch" id="branch" required><br><br>
            <label>
                <input type="checkbox" name="agree">
                Agree to Terms of Service
            </label><br><br>
            <input type="hidden" name="form_submitted" value="1">
            <input type="submit" value="Submit">
        </form>
    <?php endif; ?>
</body>
</html>
```
**Result:** The POST method does not display form data in the browser's address bar.

---

**Practical No: 2**
**Object:** Create PHP code that utilizes commonly used API library functions built into PHP.

### PHP Code for API Requests:
```php
<?php
// Include the Requests library (assuming you have it installed via Composer)
require_once 'vendor/autoload.php';

// Define headers and authentication options
$headers = array('Accept' => 'application/json');
$options = array(
    'auth' => array('user', 'pass') // Replace with actual credentials
);

// Make a GET request to the GitHub API
$request = Requests::get('https://api.github.com/gists', $headers, $options);

// Check the content type from the headers
var_dump($request->headers["content-type"]); // Expecting "application/json; charset=utf-8"

// Check the body of the response (the content returned from the API)
var_dump($request->body);
?>
```

### JavaScript Code Using Fetch API:
```html
<html>
<body>
    <h1>Using JavaScript's Fetch API</h1>
    <script>
        // GET request
        fetch('https://jsonplaceholder.typicode.com/todos')
            .then(response => response.json())
            .then(json => console.log(json));

        // GET specific resource
        fetch('https://jsonplaceholder.typicode.com/todos/5')
            .then(response => response.json())
            .then(json => console.log(json));

        // POST request
        fetch("https://jsonplaceholder.typicode.com/todos", {
            method: 'POST',
            body: JSON.stringify({
                userId: 1,
                title: "clean room",
                completed: false
            }),
            headers: {
                "Content-type": "application/json; charset=UTF-8"
            }
        })
        .then(response => response.json())
        .then(json => console.log(json));

        // DELETE request
        fetch('https://jsonplaceholder.typicode.com/todos/1', {
            method: 'DELETE'
        })
        .then(response => response.json())
        .then(json => console.log(json));
    </script>
</body>
</html>
```
**Result:** Successfully created PHP and JavaScript codes to utilize API library functions.

---

**Practical No: 3**
**Object:** Create a basic blogging website on WordPress.

### Procedure:
1. **Open WordPress**:
   - Navigate to [WordPress](https://www.wordpress.com).
2. **Select "Create Blog"**.
3. **Create an Account**:
   - Provide email, username, and password.
4. **Complete Blog Setup**:
   - Verify email and choose a theme.
5. **Customize Blog**:
   - Add posts, change appearance, and configure settings.

**Result:** A basic blog website is created on WordPress.

---














### Practical No: 4
#### Object:
Design a Website using WordPress

#### Theory:
To design a website on WordPress, follow these steps:

1. **Opening WordPress:**
   - Open a web browser and type `www.wordpress.com` in the address bar. Press Enter to open the website.

2. **Choosing Website Option:**
   - On the WordPress homepage, two options are presented:
     - **Create Website**
     - **Create Blog**
   - Select the **Create Website** option.

3. **Creating an Account:**
   - A new webpage will appear asking you to enter your details. Provide the following:
     - **Email ID:** Enter a valid email address.
     - **Username:** Choose a unique username.
     - **Password:** Create a secure password.
   - After filling in the details, click on the **Create Your Account** button.
   - Once the account is created, you will have access to the WordPress dashboard.

4. **Designing the Website:**
   After creating the website, follow these steps to design it:

   i. **Make the Website Viewable by the Public:**
      - Navigate to `Settings → Reading`.
      - Ensure the option "Discourage search engines from indexing this site" is unchecked to make your website visible to the public.

   ii. **Set Title and Tagline:**
       - Go to `Settings → General`.
       - Set the Title and Tagline for your website to define its identity.

   iii. **Allow Comments on Your Website:**
        - Navigate to `Settings → Discussion`.
        - Enable or disable comment settings to allow visitors to leave comments on your posts and pages.

   iv. **Change the Theme:**
       - Go to `Appearance → Themes` in the WordPress dashboard.
       - Browse and select a theme that suits the design you want for your website.

   v. **Customize Typography:**
      - Click on `Settings → Typography`.
      - Change the font style, font color, background color, and other typography settings to personalize the website’s text appearance.

   vi. **Insert Plugins:**
       - Plugins extend the functionality of your website. Navigate to `Plugins → Add New` and search for the desired plugins to install them.

   vii. **Create Basic Pages:**
        - To create a new page, go to `Pages → Add New` in the dashboard.
        - Add the page title and content:
          - **Title Section:** Enter the title of the page.
          - **Body Section:** Write the content for the page.
          - Insert images, audio, and video using the editor options.
        - Click **Publish** to make the page live.

   viii. **Navigate the Website:**
         - Use the `Menu` option to navigate through your website.
         - Depending on the selected theme, add and arrange menu items for your website’s navigation bar.

#### Result:
Thus, the website is designed on WordPress, with customizations for title, tagline, theme, typography, comments, plugins, and pages, along with navigation settings.

---
 







### Practical No: 5
#### Object:
Designing Web Pages using PHP, CSS, XHTML, Syntax, and Structure

#### Theory:
In this practical, a webpage is designed using PHP, CSS, and XHTML by structuring it with a header, body, and footer page. PHP dynamically fetches and displays the content. Follow these steps:

1. **Creating the Header Page (`header.html`):**
   - The header page contains the opening structure of the website, including meta tags, title, and an optional logo or image.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Suraj Arya</title>
</head>
<body>
<header>
    <h1>Hey, I'm Suraj</h1>
    <p>This is a Random Page</p>
    <p>Date: October 23, 2024</p>
</header>
</body>
</html>
```
Save this file as `header.html`.

2. **Creating the Body Page (`body.html`):**
   - The body page contains the main content of the website.

```html
<p>It helps the designer plan where the content will sit. It helps in creating drafts of the content on the pages of the website. It originates from the Latin text but is seen as gibberish. Sometimes, the reader gets distracted while creating or working on the website. That’s why this language is important. This tool makes the work easier for the webmaster.</p>
```
Save this file as `body.html`.

3. **Creating the Footer Page (`footer.html`):**
   - The footer page typically contains copyright and other footer information.

```html
<footer>
    <p>All rights reserved.</p>
</footer>
```
Save this file as `footer.html`.

4. **Creating the Index Page (`index.php`):**
   - The index page fetches the content from the header, body, and footer pages using PHP’s `file_get_contents` function.

```php
<?php echo file_get_contents("html/header.html"); ?>
<?php echo file_get_contents("html/body.html"); ?>
<?php echo file_get_contents("html/footer.html"); ?>
<!-- Adding copyright and dynamic year -->
<p>Copyright © Suraj Arya <?php echo date("Y"); ?></p>
```
- The `file_get_contents()` function fetches the content of the HTML files and embeds it into the index page.
- The `date("Y")` function in PHP dynamically displays the current year.

#### Result:
When running the `index.php` file in a browser, it will display the content from the header, body, and footer files, along with a dynamically updated copyright notice showing the current year.

