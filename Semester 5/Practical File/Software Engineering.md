### Practical 1: Software Requirements Specification (SRS) for Online Food Ordering System

---

#### 1. Introduction

**1.1 Purpose:**  
The purpose of this document is to define the software requirements for an Online Food Ordering System (OFOS). This system allows users to browse restaurant menus, place orders, make payments, and track deliveries. It also enables restaurant administrators to manage their menus and orders efficiently.

**1.2 Scope:**  
The OFOS is a web and mobile-based platform designed to bridge the gap between restaurants and customers. It offers features such as menu browsing, real-time order placement, secure payment processing, and order tracking. The system also includes administrative functionalities for restaurant owners and delivery personnel.

**1.3 Definitions, Acronyms, and Abbreviations:**
- **OFOS:** Online Food Ordering System
- **UI:** User Interface
- **API:** Application Programming Interface
- **POS:** Point of Sale

**1.4 Overview:**  
This SRS document outlines the functional, non-functional, and system requirements for the Online Food Ordering System. It also includes use cases and system design details.

---

#### 2. Overall Description

**2.1 Product Perspective:**  
The OFOS will operate as a centralized platform where multiple restaurants can register and showcase their offerings. Customers can access the platform via web browsers or mobile applications. The system will use a modular architecture for scalability.

**2.2 Product Features:**
- User registration and login.
- Restaurant and menu browsing.
- Search and filter functionality.
- Order placement and payment.
- Real-time order status updates.
- Delivery tracking.
- Admin dashboard for restaurant owners.
- Notifications and alerts.

**2.3 User Classes and Characteristics:**
- **Customers:** Place orders and make payments.
- **Restaurant Owners:** Manage menus, view orders, and track sales.
- **Delivery Personnel:** View delivery assignments and update statuses.
- **System Admin:** Oversee platform operations and troubleshoot issues.

**2.4 Operating Environment:**
- **Web:** Compatible with modern browsers (e.g., Chrome, Firefox, Safari).
- **Mobile:** Android (5.0 and above) and iOS (12 and above).
- **Server:** Cloud-based hosting with Linux/Windows OS.

**2.5 Constraints:**
- High network dependency for real-time features.
- Must comply with local food safety and data protection regulations.

**2.6 Assumptions and Dependencies:**
- All users have internet access.
- Restaurants are responsible for updating their menus and prices.
- Payment gateways are integrated and functional.

---

#### 3. Functional Requirements

**3.1 User Registration and Authentication:**
- Users can register using an email ID or phone number.
- Authentication via password, OTP, or social media login.

**3.2 Menu Browsing and Search:**
- Customers can browse by restaurant, cuisine, or dish.
- Advanced filters for price range, ratings, and delivery time.

**3.3 Order Placement:**
- Add items to the cart.
- Specify delivery address and time.
- Confirm and place the order.

**3.4 Payment Processing:**
- Multiple payment options (credit/debit cards, UPI, wallets).
- Payment confirmation and invoice generation.

**3.5 Delivery Tracking:**
- Real-time updates on order status.
- Estimated delivery time displayed.

**3.6 Restaurant Management:**
- Admin dashboard for managing menus, prices, and offers.
- View order history and revenue reports.

**3.7 Notifications:**
- SMS, email, or app notifications for order status and promotions.

---

#### 4. Non-Functional Requirements

**4.1 Performance Requirements:**
- Support up to 10,000 simultaneous users.
- Average response time < 2 seconds.

**4.2 Security Requirements:**
- Data encryption for sensitive information.
- Secure payment gateway integration.
- Role-based access control.

**4.3 Usability Requirements:**
- Intuitive and user-friendly UI/UX design.
- Support for multiple languages.

**4.4 Reliability Requirements:**
- 99.9% uptime.
- Robust backup and recovery system.

---

#### 5. System Models

**5.1 Use Case Diagram:**
- A diagram showcasing interactions between customers, restaurant owners, delivery personnel, and the system admin.

**5.2 Sequence Diagram:**
- Illustrates the sequence of interactions during order placement and delivery.

**5.3 Data Flow Diagram (DFD):**
- Explains data movement between modules such as User Management, Order Processing, and Payment Gateway.

---

#### 6. Appendices

**6.1 References:**
- Industry standards for e-commerce platforms.
- Local data protection and food safety regulations.

**6.2 Glossary:**
- **OTP:** One-Time Password.
- **POS:** Point of Sale.

---

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>


### Practical:2 Software Requirements Specification (SRS) for Online Food Ordering System

---

#### 1. Introduction

**1.1 Purpose:**  
The purpose of this document is to define the software requirements for an Online Food Ordering System (OFOS). This system allows users to browse restaurant menus, place orders, make payments, and track deliveries. It also enables restaurant administrators to manage their menus and orders efficiently.

**1.2 Scope:**  
The OFOS is a web and mobile-based platform designed to bridge the gap between restaurants and customers. It offers features such as menu browsing, real-time order placement, secure payment processing, and order tracking. The system also includes administrative functionalities for restaurant owners and delivery personnel.

**1.3 Definitions, Acronyms, and Abbreviations:**
- **OFOS:** Online Food Ordering System
- **UI:** User Interface
- **API:** Application Programming Interface
- **POS:** Point of Sale

**1.4 Overview:**  
This SRS document outlines the functional, non-functional, and system requirements for the Online Food Ordering System. It also includes use cases and system design details.

---

#### 2. Overall Description

**2.1 Product Perspective:**  
The OFOS will operate as a centralized platform where multiple restaurants can register and showcase their offerings. Customers can access the platform via web browsers or mobile applications. The system will use a modular architecture for scalability.

**2.2 Product Features:**
- User registration and login.
- Restaurant and menu browsing.
- Search and filter functionality.
- Order placement and payment.
- Real-time order status updates.
- Delivery tracking.
- Admin dashboard for restaurant owners.
- Notifications and alerts.

**2.3 User Classes and Characteristics:**
- **Customers:** Place orders and make payments.
- **Restaurant Owners:** Manage menus, view orders, and track sales.
- **Delivery Personnel:** View delivery assignments and update statuses.
- **System Admin:** Oversee platform operations and troubleshoot issues.

**2.4 Operating Environment:**
- **Web:** Compatible with modern browsers (e.g., Chrome, Firefox, Safari).
- **Mobile:** Android (5.0 and above) and iOS (12 and above).
- **Server:** Cloud-based hosting with Linux/Windows OS.

**2.5 Constraints:**
- High network dependency for real-time features.
- Must comply with local food safety and data protection regulations.

**2.6 Assumptions and Dependencies:**
- All users have internet access.
- Restaurants are responsible for updating their menus and prices.
- Payment gateways are integrated and functional.

---

#### 3. Functional Requirements

**3.1 User Registration and Authentication:**
- Users can register using an email ID or phone number.
- Authentication via password, OTP, or social media login.

**3.2 Menu Browsing and Search:**
- Customers can browse by restaurant, cuisine, or dish.
- Advanced filters for price range, ratings, and delivery time.

**3.3 Order Placement:**
- Add items to the cart.
- Specify delivery address and time.
- Confirm and place the order.

**3.4 Payment Processing:**
- Multiple payment options (credit/debit cards, UPI, wallets).
- Payment confirmation and invoice generation.

**3.5 Delivery Tracking:**
- Real-time updates on order status.
- Estimated delivery time displayed.

**3.6 Restaurant Management:**
- Admin dashboard for managing menus, prices, and offers.
- View order history and revenue reports.

**3.7 Notifications:**
- SMS, email, or app notifications for order status and promotions.

---

#### 4. Non-Functional Requirements

**4.1 Performance Requirements:**
- Support up to 10,000 simultaneous users.
- Average response time < 2 seconds.

**4.2 Security Requirements:**
- Data encryption for sensitive information.
- Secure payment gateway integration.
- Role-based access control.

**4.3 Usability Requirements:**
- Intuitive and user-friendly UI/UX design.
- Support for multiple languages.

**4.4 Reliability Requirements:**
- 99.9% uptime.
- Robust backup and recovery system.

---

#### 5. System Models

**5.1 Use Case Diagram:**
- A diagram showcasing interactions between customers, restaurant owners, delivery personnel, and the system admin.

**5.2 Sequence Diagram:**
- Illustrates the sequence of interactions during order placement and delivery.

**5.3 Data Flow Diagram (DFD):**

**Level 0 DFD:**
This represents the high-level overview of the system. It illustrates the major entities and processes.
- **External Entities:** Customers, Restaurants, Delivery Personnel.
- **Processes:** Order Placement, Payment Processing, Delivery Management.
- **Data Stores:** User Database, Order Database, Menu Database.

**Level 1 DFD:**
This provides a detailed breakdown of the processes:
1. **Order Placement Process:**
   - Input: Customer selects items, adds to cart.
   - Output: Order is stored in the Order Database.
2. **Payment Processing:**
   - Input: Payment details from the customer.
   - Output: Transaction confirmation and invoice.
3. **Delivery Management:**
   - Input: Order details and customer location.
   - Output: Delivery assignment to personnel.

---

#### 6. Appendices

**6.1 References:**
- Industry standards for e-commerce platforms.
- Local data protection and food safety regulations.

**6.2 Glossary:**
- **OTP:** One-Time Password.
- **POS:** Point of Sale.

---

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>




---

### Practical No: 3 - Develop Sequence Diagram

**Objective:**  
To create a sequence diagram illustrating the interactions between various components of the Online Food Ordering System during a typical order process.

---

#### Sequence Diagram Description

The sequence diagram demonstrates the flow of interactions between the system’s entities. This includes the Customer, System, Restaurant Owner, and Delivery Personnel, detailing the steps from placing an order to completing the delivery.

#### Key Components:
1. **Customer:** Initiates the process by browsing the menu and placing an order.
2. **System:** Processes the order, communicates with the restaurant, and manages payment.
3. **Restaurant Owner:** Prepares the food and updates the system when it’s ready for delivery.
4. **Delivery Personnel:** Picks up the order and delivers it to the customer.

---

#### Sequence of Operations:

1. **Browse Menu:** The Customer requests the menu from the System.
2. **Place Order:** The Customer selects items and places the order through the System.
3. **Payment:** The System processes the payment through an integrated Payment Gateway.
4. **Notify Restaurant:** The System notifies the Restaurant Owner of the new order.
5. **Order Preparation:** The Restaurant Owner prepares the food and updates the order status to "Ready for Delivery."
6. **Assign Delivery:** The System assigns the order to available Delivery Personnel.
7. **Pickup Confirmation:** The Delivery Personnel confirms the pickup of the order.
8. **Delivery:** The Delivery Personnel delivers the order to the Customer and updates the status to "Delivered."

---

#### Sequence Diagram Representation:

**Actors:**
- Customer
- System
- Restaurant Owner
- Delivery Personnel
- Payment Gateway

**Steps in Diagram Form:**
1. Customer sends "Browse Menu" request to System.
2. System fetches and displays menu to Customer.
3. Customer sends "Place Order" request.
4. System confirms order details and redirects to Payment Gateway.
5. Payment Gateway processes payment and sends confirmation to System.
6. System notifies Restaurant Owner of the new order.
7. Restaurant Owner updates order status to "Ready for Delivery."
8. System assigns order to Delivery Personnel.
9. Delivery Personnel picks up the order and confirms the status.
10. Delivery Personnel delivers the order to Customer and updates status to "Delivered."

---

<br>
<br>
<br>
<br>
<br>
<br>
<br>


**Practical: 4. Use Testing Tools such as JMeter, Canoo Web Test**

**Objective:**
The purpose of this practical is to understand and apply the usage of performance testing tools like JMeter and Canoo Web Test. These tools are designed to assess the functionality, performance, and reliability of web applications by simulating a variety of test scenarios.

**Introduction:**
Web applications are often subjected to a wide range of user traffic and various operational conditions. To ensure these applications can handle high user loads and perform efficiently, performance testing tools like JMeter and Canoo Web Test are used. JMeter is an open-source tool used for load and performance testing, while Canoo Web Test is used to automate browser-based tests for web applications.

**Tools Overview:**

1. **JMeter:**
   Apache JMeter is a popular open-source tool primarily designed for load testing web applications. It allows for the creation of complex test scenarios that simulate multiple users accessing a web application concurrently. JMeter can be used for both functional and performance testing, with features that allow users to test the behavior of servers, databases, and other services.

2. **Canoo Web Test:**
   Canoo Web Test is a Java-based tool used for automating functional tests of web applications. It uses a simple scripting language to simulate user actions, such as clicking buttons, filling out forms, and validating responses. It can be integrated into continuous integration systems for automated testing.

**Procedure:**

1. **Installation and Setup:**
   - Install JMeter from the official Apache website and ensure all dependencies are set up.
   - For Canoo Web Test, download the software and integrate it with a Java IDE like Eclipse for script development.

2. **Creating a Test Plan in JMeter:**
   - Launch JMeter and create a new test plan.
   - Add a Thread Group, which represents a group of virtual users.
   - Configure the Thread Group to simulate the desired number of users and set the ramp-up period and loop count.
   - Add HTTP Request Samplers to simulate interactions with a web server.
   - Include Listeners such as View Results Tree and Summary Report to monitor the test execution and collect data.
   - Run the test and analyze the results to evaluate the server’s response time, throughput, and other performance metrics.

3. **Creating a Test Script in Canoo Web Test:**
   - Create a new Web Test project in your Java IDE.
   - Define the test steps in a WebTest script, such as opening a browser, navigating to a webpage, and performing actions like filling out forms or clicking buttons.
   - Use assertions to validate that the application behaves as expected, checking elements like page titles, text, or URLs.
   - Execute the test to ensure the functionality is working as intended.
   - Automate the tests to run periodically or as part of a continuous integration pipeline.

4. **Performance Testing with JMeter:**
   - Configure JMeter to simulate different levels of user traffic, such as a small load and a large load.
   - Measure the response time under various conditions, such as normal traffic, peak load, and stress testing.
   - Adjust parameters to test different server configurations and determine the system's scalability.

5. **Functional Testing with Canoo Web Test:**
   - Define a sequence of actions that represent typical user interactions with the web application.
   - Use assertions to check whether the results match the expected behavior, ensuring that the web application functions correctly.
   - Analyze test results to identify any discrepancies between actual and expected outputs.

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>



**Practical: 5. Use a Project Management Tool such as Microsoft Project or GanttProject**

**Objective:**
The objective of this practical is to understand and apply the use of project management tools like Microsoft Project, GanttProject, and others such as Teamweek and TargetProcess. These tools are designed to plan, manage, and monitor project progress, ensuring that tasks are completed on time and resources are effectively allocated.

**Introduction:**
Effective project management is essential to the success of any project, ensuring that tasks are completed within the given timeline, resources are efficiently used, and any risks or issues are identified and addressed promptly. Tools like Microsoft Project, GanttProject, Teamweek, and TargetProcess allow project managers and teams to organize, track, and communicate project activities.

**Tools Overview:**

1. **Microsoft Project:**
   Microsoft Project is a comprehensive project management tool that provides functionalities for creating detailed project plans, assigning tasks, tracking project progress, and managing resources. It uses Gantt charts to visually represent the project schedule, highlighting task dependencies and milestones.

2. **GanttProject:**
   GanttProject is a free, open-source project management tool that focuses on Gantt chart-based scheduling. It allows users to plan and track projects, assign tasks, and manage resources. GanttProject is simple to use and provides essential features like task hierarchy, resource management, and progress tracking.

3. **Teamweek:**
   Teamweek is a visual project management tool designed for planning and tracking team projects. It emphasizes ease of use, providing an intuitive interface for managing tasks, milestones, and team schedules. Teamweek offers real-time collaboration, making it ideal for teams looking to coordinate and track progress on projects.

4. **TargetProcess:**
   TargetProcess is an agile project management tool designed to help teams working on software development projects. It supports Scrum, Kanban, and other agile methodologies, enabling users to manage sprints, backlogs, user stories, and track progress in a visual, customizable interface.

**Procedure:**

1. **Getting Started with Microsoft Project:**
   - Open Microsoft Project and create a new project file.
   - Define the project’s start date, end date, and major milestones.
   - Create tasks and subtasks, specifying their duration and start/end dates.
   - Link tasks that depend on one another to form a logical sequence of events.
   - Assign resources (e.g., people, equipment) to tasks.
   - Use the Gantt chart view to visualize the project timeline, adjust task durations, and identify any overlaps or resource constraints.
   - Track progress by updating task completion percentages and noting any delays or issues.

2. **Using GanttProject:**
   - Open GanttProject and create a new project by specifying the project’s start date and deadlines.
   - Define tasks and subtasks, specifying their durations, start and end dates.
   - Organize tasks in a hierarchical manner to show task dependencies.
   - Allocate resources to each task and set their working hours.
   - Use the Gantt chart to track task completion and ensure the project stays on schedule.
   - Generate reports to monitor task progress and evaluate project performance.

3. **Managing Projects with Teamweek:**
   - Create a new project in Teamweek and define key milestones and deadlines.
   - Break the project into tasks, and assign them to specific team members.
   - Visualize the project schedule using a timeline view, making it easy to see which tasks are in progress and which ones are upcoming.
   - Use color coding to indicate task priority and progress.
   - Collaborate with team members by commenting on tasks and sharing files.
   - Adjust timelines based on team availability and any changes in the project scope.

4. **Tracking Agile Projects with TargetProcess:**
   - Set up a project in TargetProcess, defining the project’s goals and agile methodology (Scrum, Kanban, etc.).
   - Create user stories, epics, and tasks that align with the project’s objectives.
   - Organize the backlog and plan sprints to assign tasks and estimate their effort.
   - Track the progress of each sprint using a Burndown chart and monitor any changes to the backlog.
   - Review the project’s progress and iterate as necessary to ensure goals are met by adjusting tasks and priorities.
 ---

 <br>
 <br>
 <br>
 <br>
 <br>
 <br>
 <br>

**Practical: 6. Write Test Cases for a Known Application**

**Objective:**
The objective of this practical is to learn how to write test cases for a known application, ensuring that all functional and non-functional requirements are met. Writing effective test cases helps verify the application’s behavior under different conditions and improves the overall quality of the software.

**Introduction:**
Test cases are a fundamental part of software testing, outlining the steps to verify that a software application performs as expected. They are written to assess various aspects of an application, including its functionality, user interface, performance, and security. This practical will involve writing test cases for a commonly used application, focusing on different functionalities and usage scenarios.

For this practical, we will write test cases for a simple **Login Functionality** of a web-based application.

**Test Case Writing Principles:**
A well-written test case typically includes the following components:
1. **Test Case ID**: A unique identifier for each test case.
2. **Test Case Description**: A brief description of what is being tested.
3. **Preconditions**: Any requirements or setup steps before executing the test case.
4. **Test Steps**: Detailed instructions to execute the test.
5. **Test Data**: Any data required to execute the test (e.g., usernames, passwords).
6. **Expected Results**: What the system should do for the test to be considered successful.
7. **Actual Results**: The actual outcome after executing the test.
8. **Status**: Pass or Fail, based on whether the actual results match the expected results.

**Test Case Example: Login Functionality**

**Test Case 1: Valid Login**
- **Test Case ID**: TC_Login_01
- **Description**: Test login functionality with valid credentials.
- **Preconditions**: The user must have a registered account with a valid username and password.
- **Test Steps**:
  1. Open the web browser.
  2. Navigate to the login page of the application.
  3. Enter a valid username (e.g., “user123”).
  4. Enter the correct password (e.g., “password123”).
  5. Click on the "Login" button.
- **Test Data**: 
  - Username: user123
  - Password: password123
- **Expected Results**: The user should be successfully logged into the application and redirected to the dashboard.
- **Actual Results**: [To be filled during testing]
- **Status**: [Pass/Fail]

**Test Case 2: Invalid Login (Incorrect Username)**
- **Test Case ID**: TC_Login_02
- **Description**: Test login functionality with an invalid username.
- **Preconditions**: The user must have access to the login page.
- **Test Steps**:
  1. Open the web browser.
  2. Navigate to the login page of the application.
  3. Enter an invalid username (e.g., “user999”).
  4. Enter a valid password (e.g., “password123”).
  5. Click on the "Login" button.
- **Test Data**:
  - Username: user999
  - Password: password123
- **Expected Results**: The system should display an error message, such as “Invalid username or password.”
- **Actual Results**: [To be filled during testing]
- **Status**: [Pass/Fail]

**Test Case 3: Invalid Login (Incorrect Password)**
- **Test Case ID**: TC_Login_03
- **Description**: Test login functionality with an incorrect password.
- **Preconditions**: The user must have access to the login page.
- **Test Steps**:
  1. Open the web browser.
  2. Navigate to the login page of the application.
  3. Enter a valid username (e.g., “user123”).
  4. Enter an incorrect password (e.g., “wrongpassword”).
  5. Click on the "Login" button.
- **Test Data**:
  - Username: user123
  - Password: wrongpassword
- **Expected Results**: The system should display an error message, such as “Invalid username or password.”
- **Actual Results**: [To be filled during testing]
- **Status**: [Pass/Fail]

**Test Case 4: Empty Username and Password Fields**
- **Test Case ID**: TC_Login_04
- **Description**: Test login functionality when the username and password fields are left empty.
- **Preconditions**: The user must have access to the login page.
- **Test Steps**:
  1. Open the web browser.
  2. Navigate to the login page of the application.
  3. Leave both the username and password fields empty.
  4. Click on the "Login" button.
- **Test Data**:
  - Username: [Empty]
  - Password: [Empty]
- **Expected Results**: The system should display an error message such as “Please enter both username and password.”
- **Actual Results**: [To be filled during testing]
- **Status**: [Pass/Fail]

**Test Case 5: Password Masking**
- **Test Case ID**: TC_Login_05
- **Description**: Ensure that the password field is masked when typing.
- **Preconditions**: The user must have access to the login page.
- **Test Steps**:
  1. Open the web browser.
  2. Navigate to the login page of the application.
  3. Enter a valid username (e.g., “user123”).
  4. Enter a password (e.g., “password123”) in the password field.
  5. Observe the password field while typing.
- **Test Data**:
  - Username: user123
  - Password: password123
- **Expected Results**: The password field should display masked characters (e.g., asterisks) while typing.
- **Actual Results**: [To be filled during testing]
- **Status**: [Pass/Fail]

---

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

**Practical: 7. Study the System Specification of a Known Application and Report Various Bugs**

**Objective:**
The objective of this practical is to study the system specifications of a known application and identify and report various bugs or issues that affect its functionality, usability, or performance. By doing so, you can understand the importance of thorough testing and the role of bug reporting in the software development lifecycle.

**Introduction:**
System specifications define the requirements and expected behavior of a system, serving as the basis for development, testing, and quality assurance activities. These documents detail the system's functionalities, performance criteria, user interface, security, and other essential features. Bugs are discrepancies between the expected behavior described in the specifications and the actual behavior of the system during testing.

For this practical, let’s assume we are studying the system specification for a **Web-based E-commerce Application**.

**System Specification Overview:**
The e-commerce application specification typically includes details on:
1. **User Authentication**: Registration, login, and password recovery functionalities.
2. **Product Management**: Displaying products, searching, and filtering options.
3. **Shopping Cart**: Adding, removing, and viewing products in the cart.
4. **Payment System**: Processing payments via credit card, PayPal, etc.
5. **Order Management**: Managing and tracking customer orders.
6. **Admin Panel**: Access and management of customer orders, products, and users.

**Procedure:**

1. **Review the System Specifications:**
   - Understand the features and functionalities outlined in the system specification document.
   - Focus on key modules such as user authentication, product management, and payment processing.
   - Identify expected behavior for each feature (e.g., correct login credentials, accurate product display, successful payment processing).

2. **Test the System Against the Specifications:**
   - Use the application as an end user to verify the functionality of different modules.
   - Ensure that each functionality behaves according to the specifications.

3. **Documenting Bugs:**
   While interacting with the application, record any issues or discrepancies you observe. These could include functional bugs, UI issues, performance problems, or security vulnerabilities.

**Example Bugs Reported for the E-commerce Application:**

**Bug 1: Invalid Login Handling**
- **Description**: When entering incorrect login credentials, the system does not display an error message.
- **Expected Behavior**: The system should show an error message such as "Invalid username or password" when incorrect credentials are entered.
- **Actual Behavior**: No error message appears when invalid credentials are provided. The user remains on the login page without any feedback.
- **Severity**: High
- **Steps to Reproduce**:
  1. Open the application login page.
  2. Enter an invalid username and password.
  3. Click "Login."
- **Environment**: Google Chrome, Windows 10
- **Screenshot**: [Include a screenshot of the issue, if possible]

**Bug 2: Product Display Inconsistency**
- **Description**: Some product images are not loading correctly on the product listing page.
- **Expected Behavior**: All product images should load properly on the product listing page.
- **Actual Behavior**: A few products display broken image icons instead of product images.
- **Severity**: Medium
- **Steps to Reproduce**:
  1. Open the product listing page.
  2. Scroll through the products.
  3. Observe the product images.
- **Environment**: Mozilla Firefox, macOS
- **Screenshot**: [Include a screenshot showing the broken images]

**Bug 3: Cart Calculation Error**
- **Description**: The total amount in the shopping cart is not updated after adding/removing products.
- **Expected Behavior**: The total amount should update immediately after adding or removing items from the shopping cart.
- **Actual Behavior**: The total amount remains the same even after modifying the cart. Only after refreshing the page does the total amount update.
- **Severity**: High
- **Steps to Reproduce**:
  1. Add a product to the shopping cart.
  2. Remove a product from the cart.
  3. Observe the total amount displayed.
- **Environment**: Safari, iPhone 12
- **Screenshot**: [Include a screenshot showing the issue]

**Bug 4: Payment Gateway Timeout**
- **Description**: The payment gateway times out after a few seconds, preventing the user from completing the payment.
- **Expected Behavior**: The payment gateway should process payments without timing out, even if the transaction takes longer.
- **Actual Behavior**: The payment page shows a "Timeout Error" after 10-15 seconds of waiting.
- **Severity**: Critical
- **Steps to Reproduce**:
  1. Add products to the shopping cart.
  2. Proceed to checkout and select a payment method (e.g., credit card).
  3. Wait for the payment process to complete.
- **Environment**: Google Chrome, Windows 11
- **Screenshot**: [Include a screenshot showing the timeout error]

**Bug 5: Missing Terms and Conditions Link**
- **Description**: The "Terms and Conditions" link in the footer is missing on the checkout page.
- **Expected Behavior**: The "Terms and Conditions" link should be visible and functional on the checkout page.
- **Actual Behavior**: The link is not present on the checkout page.
- **Severity**: Low
- **Steps to Reproduce**:
  1. Navigate to the checkout page.
  2. Look for the "Terms and Conditions" link in the footer.
- **Environment**: Microsoft Edge, Windows 10
- **Screenshot**: [Include a screenshot showing the missing link]
