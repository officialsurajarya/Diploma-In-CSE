# Unit 6: Bootstrap 

Bootstrap is an open-source framework for developing responsive, mobile-first web pages. It provides pre-designed components, such as navigation bars, buttons, forms, and grids, that make it easier and faster to create well-designed web pages. This unit covers various features of Bootstrap, including color management, buttons, tables, navigation bars, images, and more.

---

### **1. Color Management in Bootstrap**
Bootstrap provides a variety of utility classes to manage colors for different elements of a webpage.

- **Text Color**: You can change the text color using classes like:
  - `.text-primary`: Blue text.
  - `.text-success`: Green text.
  - `.text-danger`: Red text.
  - `.text-warning`: Yellow text.
  - `.text-info`: Light blue text.
  - `.text-muted`: Muted text (gray).
  - `.text-white`: White text.

  Example:
  ```html
  <p class="text-success">This is a success message.</p>
  ```

- **Background Color**: Bootstrap also provides background color utility classes:
  - `.bg-primary`, `.bg-success`, `.bg-danger`, `.bg-warning`, `.bg-info`, `.bg-light`, `.bg-dark`, `.bg-white`.

  Example:
  ```html
  <div class="bg-primary text-white">This is a primary background with white text.</div>
  ```

---

### **2. Buttons**
Bootstrap comes with a variety of predefined button styles for different purposes. These buttons are fully customizable.

- **Basic Button Styles**:
  - `.btn-primary`: Blue button.
  - `.btn-secondary`: Gray button.
  - `.btn-success`: Green button.
  - `.btn-danger`: Red button.
  - `.btn-warning`: Yellow button.
  - `.btn-info`: Light blue button.
  - `.btn-light`: Light button.
  - `.btn-dark`: Dark button.
  - `.btn-link`: Button styled as a link.

  Example:
  ```html
  <button class="btn btn-primary">Primary Button</button>
  ```

- **Button Sizes**:
  - `.btn-lg`: Large button.
  - `.btn-sm`: Small button.
  - `.btn-block`: Full-width button.

  Example:
  ```html
  <button class="btn btn-sm btn-success">Small Success Button</button>
  ```

---

### **3. Tables**
Bootstrap makes it easy to style tables with built-in classes for table formatting.

- **Basic Table**:
  ```html
  <table class="table">
    <thead>
      <tr>
        <th>#</th>
        <th>Name</th>
        <th>Age</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>1</td>
        <td>John Doe</td>
        <td>25</td>
      </tr>
      <tr>
        <td>2</td>
        <td>Jane Smith</td>
        <td>30</td>
      </tr>
    </tbody>
  </table>
  ```

- **Table Stripes**: `.table-striped` adds zebra-striping to table rows.
  ```html
  <table class="table table-striped">
    <!-- table content here -->
  </table>
  ```

- **Table Borders**: `.table-bordered` adds borders to the table and its cells.
  ```html
  <table class="table table-bordered">
    <!-- table content here -->
  </table>
  ```

- **Table Hover**: `.table-hover` adds a hover effect to rows.
  ```html
  <table class="table table-hover">
    <!-- table content here -->
  </table>
  ```

---

### **4. Drop-downs**
Bootstrap provides a simple way to create dropdowns using `.dropdown` classes.

- **Basic Drop-down**:
  ```html
  <div class="dropdown">
    <button class="btn btn-secondary dropdown-toggle" type="button" data-bs-toggle="dropdown" aria-expanded="false">
      Dropdown button
    </button>
    <ul class="dropdown-menu">
      <li><a class="dropdown-item" href="#">Action</a></li>
      <li><a class="dropdown-item" href="#">Another action</a></li>
      <li><a class="dropdown-item" href="#">Something else here</a></li>
    </ul>
  </div>
  ```

- **Alignment**: You can align dropdowns to the right using `.dropdown-menu-end` class.
  ```html
  <div class="dropdown">
    <button class="btn btn-secondary dropdown-toggle" type="button" data-bs-toggle="dropdown" aria-expanded="false">
      Dropdown button
    </button>
    <ul class="dropdown-menu dropdown-menu-end">
      <li><a class="dropdown-item" href="#">Action</a></li>
    </ul>
  </div>
  ```

---

### **5. Navigation Bar**
Bootstrap offers a flexible and responsive navigation bar component.

- **Basic Navigation Bar**:
  ```html
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <a class="navbar-brand" href="#">Navbar</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item active">
          <a class="nav-link" href="#">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Features</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Pricing</a>
        </li>
      </ul>
    </div>
  </nav>
  ```

---

### **6. Images**
Bootstrap provides classes to style and control the layout of images.

- **Responsive Images**: The `.img-fluid` class makes images responsive, adjusting to the width of their container.
  ```html
  <img src="image.jpg" class="img-fluid" alt="Responsive image">
  ```

- **Rounded and Circle Images**: `.rounded` and `.rounded-circle` classes apply rounded borders or circular styles to images.
  ```html
  <img src="image.jpg" class="rounded" alt="Rounded Image">
  ```

---

### **7. Pagination**
Bootstrap provides styles for pagination controls to navigate through pages.

- **Basic Pagination**:
  ```html
  <ul class="pagination">
    <li class="page-item"><a class="page-link" href="#">1</a></li>
    <li class="page-item"><a class="page-link" href="#">2</a></li>
    <li class="page-item"><a class="page-link" href="#">3</a></li>
  </ul>
  ```

---

### **8. Jumbotron**
The **jumbotron** component is used to showcase important content or information.

- **Basic Jumbotron**:
  ```html
  <div class="jumbotron">
    <h1 class="display-4">Welcome to Bootstrap</h1>
    <p class="lead">This is a simple hero unit, a simple jumbotron-style component for calling extra attention to featured content or information.</p>
    <hr class="my-4">
    <p>It uses utility classes for typography and spacing to space content out within the larger container.</p>
  </div>
  ```

---

### **9. Alerts**
Bootstrap includes pre-defined classes for creating alerts that can be used to convey messages to users.

- **Basic Alerts**:
  ```html
  <div class="alert alert-success" role="alert">
    This is a success alert.
  </div>
  ```

  Other alert types:
  - `.alert-primary`, `.alert-secondary`, `.alert-danger`, `.alert-warning`, `.alert-info`, `.alert-light`, `.alert-dark`.

- **Dismissible Alerts**:
  ```html
  <div class="alert alert-danger alert-dismissible fade show" role="alert">
    This is a danger alert.
    <button type="button" class="btn-close" data-bs-dismiss="alert" aria-label="Close"></button>
  </div>
  ```

---

### **10. Forms**
Bootstrap provides extensive styling options for creating forms.

- **Basic Form**:
  ```html
  <form>
    <div class="mb-3">
      <label for="exampleInput" class="form-label">Email address</label>
      <input type="email" class="form-control" id="exampleInput" placeholder="Enter email">
    </div>
    <button type="submit" class="btn btn-primary">Submit</button>
  </form>
  ```

- **Form Controls**: Classes like `.form-control` style input fields, `.form-check` for checkboxes, and `.form-group` for grouping labels and inputs.

---

### **11. Progress Bar**
Bootstrap provides progress bars for indicating the progress of a task.

- **Basic Progress Bar**:
  ```html
  <div class="progress">
    <div class="progress-bar" role="progressbar" style="width: 50%" aria-valuenow="50" aria-valuemin="0" aria-valuemax="100"></div>
  </div>
  ```

---

### **12. Grid**
Bootstrap's grid system is designed to help you build responsive layouts. It is based on a 12-column grid.

- **Basic Grid Layout**:
  ```html
  <div class="row">
    <div class="col-6">Column 1</div>
    <div class="col-6">Column 2</div>
  </div>
  ```

- **Column Sizing**: You can adjust the number of columns that take up space depending on the screen size using classes like `.col-lg-4`, `.col-md-6`, `.col-sm-12`.

---

### **13. Utilities & Filters**
Bootstrap provides utility classes for quick customization of elements.

- **Spacing Utilities**: Classes like `.m-2`, `.p-3` for margins and padding.
- **Text Alignment**: `.text-center`, `.text-left`, `.text-right`.
- **Display**: `.d-none`, `.d-block`, `.d-flex`.

These utilities allow you to make fast layout and design adjustments.

---

### **Conclusion**
Bootstrap simplifies front-end web development by providing a powerful set of pre-designed components and responsive layout features. It helps developers create aesthetically pleasing, responsive websites quickly. Whether you’re managing color schemes, creating buttons, building forms, or designing a navigation bar, Bootstrap offers a range of tools to streamline the process.