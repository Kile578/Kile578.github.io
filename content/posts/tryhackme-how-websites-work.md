+++
date = '2025-07-14T17:48:13-07:00'
draft = true
title = 'Tryhackme How Websites Work'
+++

# TryHackMe How Websites Work: A Beginner's Journey into Web Security

*Learn web fundamentals and discover security vulnerabilities through hands-on practice*

---

## Introduction

Ever wondered what happens behind the scenes when you visit a website? Or how cybersecurity professionals find vulnerabilities in web applications? I recently completed TryHackMe's "How Websites Work" room, and I'm excited to share my journey from complete beginner to understanding the fundamentals of web security.

This comprehensive guide will walk you through everything I learned about website architecture, HTML structure, JavaScript functionality, and common security vulnerabilities that every web developer and cybersecurity enthusiast should know about.

**What you'll learn from this post:**
- How browsers and servers communicate
- HTML fundamentals and structure
- JavaScript basics and security implications
- Real-world security vulnerabilities
- Hands-on techniques for web security testing

---

## Room Information

- **Room Name**: How Websites Work
- **Difficulty**: Easy (Perfect for beginners!)
- **Platform**: TryHackMe
- **Room URL**: https://tryhackme.com/room/howwebsiteswork
- **Estimated Time**: 2-3 hours
- **Skills Required**: Basic computer literacy
- **Skills Gained**: Web fundamentals, HTML/JavaScript basics, security awareness

---

## Learning Objectives

This room covers essential web security concepts that form the foundation for more advanced cybersecurity topics:

- Understanding how websites function at a technical level
- Learning about web servers and client-side technologies
- Exploring HTTP/HTTPS protocols and communication
- Understanding DNS resolution and web infrastructure
- Identifying common web application security vulnerabilities
- Developing a security-focused mindset for web technologies

---

## Foundation Knowledge: Understanding Websites

### What is a Website?

A website is a collection of web pages hosted on the internet that individuals, groups, or companies create for others to access. Websites serve countless purposes in our digital world - from sharing information through blogs and news sites, to enabling appointment scheduling with interactive calendars, processing secure payments for e-commerce, displaying professional portfolios, running complex online stores, and facilitating social media interactions.

### URL and IP Addresses: The Internet's Address System

To access any website, you need either its URL (web address) or IP address. Every website lives on a server with a designated IP address (like 192.168.1.1 or 127.0.0.1). However, you rarely see these numerical addresses because we use the Domain Name System (DNS) - one of the internet's most crucial innovations.

DNS translates human-readable domain names (like google.com) into the IP addresses that computers actually use to communicate. When you type "google.com" into your browser, DNS servers work behind the scenes to convert that friendly name into the actual IP address where Google's servers are located.

This system makes the internet incredibly user-friendly - imagine having to remember "172.217.12.142" instead of just typing "google.com"! This translation process happens millions of times per second across the globe, making the modern web possible.

---

## Task 1: How Websites Work - The Foundation

### The Request-Response Process

Understanding web communication starts with a simple concept: your browser makes a request to a web server asking for information on a page. This fundamental process powers every website interaction you've ever had.

### Major Components: Frontend vs Backend

Modern web applications consist of two major components that work together seamlessly:

**1. Frontend** - Your side of the website (***What you see***)
The frontend encompasses everything that renders in your browser - visual elements, buttons, text, images, forms, and interactive features you interact with directly. It's the user interface that makes websites accessible and enjoyable to use.

**2. Backend** - Process the website
The backend handles all server-side processing, database operations, user authentication, business logic, and the complex computational work that makes websites functional. Users never see the backend directly, but it powers everything they experience.

### Task Challenge

**Question**: What term best describes the component of a web application rendered by your browser?

**Answer**: Frontend

**Explanation**: As we explored above, the frontend renders the website content that users see and interact with in their browsers.

**Key Insight**: This distinction between frontend and backend is crucial for understanding web security, as vulnerabilities can exist in both layers and require different defensive strategies.

---

## Task 2: HTML - The Language of the Web

### Understanding HTML Fundamentals

HTML stands for HyperText Markup Language. It's the way websites are written - essentially the native language that browsers understand to display web content. Think of HTML as the skeleton or foundation that gives structure to every webpage you visit.

### HTML Structure and Syntax

HTML uses a hierarchical tag-based structure that tells browsers how to interpret and display content. Here's the basic structure I learned:

```html
<!DOCTYPE html>   <!-- Tells the browser this document is HTML -->
<html>            <!-- Root element - every other element must be inside -->
   <head>        <!-- Page information and metadata -->
       <title>Page Title</title>
   </head>
   <body>        <!-- Everything in body is shown in the browser -->
       <h1>Example Heading</h1>
       <p>Example paragraph..</p>   <!-- Define a paragraph -->
   </body>
</html>
```
### Hands-On HTML Challenges

**Challenge 1: Modifying Page Headers**
*Question*: How would we change the page header to "YourName Website"?

*Solution*: Use the `<h1>` tag within the `<body>` element, since whatever is in the body is displayed in the browser.

**Challenge 2: Fixing Broken Images**
I encountered HTML code with a broken image:

```html
    <img src='img/cat-2.'>  <!-- Missing file extension! -->
```

*Problem*: The image was missing the `.jpg` file format extension.
*Solution*: Add the proper file extension: `<img src='img/cat-2.jpg'>`
*Answer Revealed*: ***HTMLHERO***

**Challenge 3: Adding New Elements**
*Task*: Add a dog image using the location `img/dog-1.png`

*Solution*:
```html
<img src='img/dog-1.png'>
```

markdown- HTML comments can contain sensitive information
- Improperly structured HTML can lead to injection vulnerabilities
- Client-side code is always visible to users
- Form validation must occur on both client and server sides

---

## Task 3: JavaScript - Bringing Websites to Life

### Why JavaScript Matters for Security

JavaScript is the game-changer that transforms static HTML websites into dynamic, functional web applications. It allows websites to update content in real-time, respond to user interactions, and create engaging user experiences. However, this power also introduces significant security considerations.

### How JavaScript Works in Web Pages

JavaScript can be added to web pages in two primary ways:

**Inline JavaScript:**
```html
<script>
   document.getElementById("demo").innerHTML = "Hack the Planet";
</script>
```

**External JavaScript Files:**
```html
<script src="/location/of/javascript_file.js"></script>
```

### Practical JavaScript Examples

**Basic Content Manipulation:**
```javascript
document.getElementById("demo").innerHTML = "Hack the Planet";
```

This code finds an element with the ID "demo" and replaces its content with "Hack the Planet".

**Interactive Button Example:**
```html
<button onclick='document.getElementById("demo").innerHTML = "Button Clicked";'>Click Me!</button>
```
This creates a button that, when clicked, changes the content of the "demo" element to "Button Clicked".
This creates an interactive button that changes the "demo" element's content when clicked.
### Task Challenges

**Challenge 1: Content Modification**
*Task*: Change the demo element's content to "Hack the Planet"

*Solution*: Use the provided JavaScript code to manipulate the DOM
*Answer Revealed*: ***JSISFUN***

**Challenge 2: Interactive Elements**
*Task*: Add a button that changes element text to "Button Clicked"

*Solution*: Implement the onclick event handler with proper JavaScript syntax

### JavaScript Security Implications

Understanding JavaScript is crucial for web security because:

- **Client-side execution**: JavaScript runs in the user's browser, making it accessible and modifiable
- **DOM manipulation**: Attackers can potentially alter page content and behavior
- **Event-driven programming**: User interactions can trigger unintended code execution
- **Third-party scripts**: External JavaScript files can introduce vulnerabilities

---

## Task 4: Sensitive Data Exposure - A Critical Security Flaw

### Understanding the Vulnerability

Sensitive data exposure occurs when developers accidentally leave confidential information in client-side code. This represents one of the most common and dangerous security mistakes in web development.

### The Investigation Process

To find exposed sensitive data, I followed these systematic steps:

1. **Navigate to the target website**
2. **Right-click** anywhere on the page
3. **Select "Inspect"** to open Developer Tools
4. **Examine the HTML source code** carefully
5. **Look through all expandable sections** and comments
6. **Search for common sensitive data patterns** (passwords, API keys, credentials)

### What I Discovered

After thorough investigation of the HTML source code, I found:
- **Username**: admin
- **Password**: testpasswd

These credentials were embedded directly in the HTML comments - a critical security vulnerability that granted immediate administrative access to the system.

### Task Challenge

**Question**: What is the password hidden in the source code?

**Answer**: ***testpasswd***

### Real-World Security Implications

This vulnerability demonstrates several critical security principles:

**Why This is Dangerous:**
- Anyone can view client-side source code
- Sensitive credentials enable unauthorized access
- Administrative accounts provide system-wide control
- This mistake is surprisingly common in real applications

**Real-World Examples:**
- API keys exposed in JavaScript files
- Database connection strings in client code
- Internal URLs and server information in comments
- User data inadvertently included in page source

**Prevention Strategies:**
- Never store sensitive data in client-side code
- Use environment variables for configuration
- Implement proper authentication systems
- Regular security code reviews
- Automated scanning for exposed secrets

## Task 5: HTML Injection - Understanding Client-Side Attacks

### What is HTML Injection?

HTML injection is a client-side security vulnerability that occurs when web applications fail to properly sanitize user input before displaying it on the webpage. This flaw allows attackers to inject malicious HTML code that gets executed by the browser, potentially compromising user security and website integrity.

### How HTML Injection Works
The vulnerable process follows this dangerous pattern:

User Input: Website accepts data through forms, search boxes, or URL parameters
Lack of Sanitization: Application fails to filter or validate the input
Direct Display: Unsanitized input gets inserted directly into the webpage
Browser Execution: Browser interprets injected code as legitimate HTML
Malicious Execution: Attacker gains control over page content and functionality

### The Technical Breakdown
Consider this vulnerable JavaScript function:
```javascript
function sayHi(name) {
    document.getElementById("output").innerHTML = "Hello " + name;
}
```

If a user enters <h1>Hacked!</h1>, the output becomes:
html<div id="output">Hello <h1>Hacked!</h1></div>
The browser renders this as actual HTML, displaying "Hacked!" as a large heading instead of plain text.
### Practical Exploitation
Objective: Inject HTML to display a malicious link to http://hacker.com
Solution:
How it works:

<a href="http://hacker.com"> creates a clickable link to the malicious site
Click here for free stuff! provides enticing text to trick users
</a> properly closes the HTML anchor tag

Advanced Payload Variations
html<!-- Basic malicious link -->
<!-- Opens in new tab to avoid suspicion -->
<a href="http://hacker.com" target="_blank">Important Update</a>

<!-- Styled to look official -->
<a href="http://hacker.com" style="color: red; font-weight: bold;">Security Alert - Click Here</a>
Task Challenge
Question: Inject HTML so that a malicious link to http://hacker.com is shown.
**Task Challenge**

**Challenge:**  
Inject HTML so that a malicious link to http://hacker.com is shown.

**Solution:**  
***HTML_INJ3CTI0N***

### Prevention Strategies

Input Sanitization: Filter and validate all user input
Output Encoding: Encode special characters before display
Content Security Policy (CSP): Restrict inline script execution
Regular Security Testing: Automated and manual vulnerability assessments


Key Takeaways and Lessons Learned
Technical Skills Developed
Web Architecture Understanding:

Mastered the client-server communication model
Learned the distinction between frontend and backend systems
Understood how DNS resolution enables user-friendly web navigation

HTML and JavaScript Proficiency:

Gained hands-on experience with HTML structure and syntax
Learned JavaScript DOM manipulation and event handling
Developed debugging skills using browser developer tools

Security Awareness:

Identified common vulnerability patterns in web applications
Learned systematic approaches to security testing
Understood the real-world impact of coding mistakes

Security Mindset Development
Always Assume User Input is Malicious:
This room reinforced the fundamental security principle that user input should never be trusted without proper validation and sanitization.
Client-Side Code is Public:
Everything sent to the browser is accessible to users, making it crucial to never include sensitive information in client-side code.
Small Mistakes Have Big Consequences:
Simple oversights like missing input validation or exposed credentials can lead to complete system compromise.
Real-World Applications
For Web Developers:

Implement proper input validation and output encoding
Use secure coding practices from the beginning
Regular security testing should be part of the development process

For Security Professionals:

Understand common vulnerability patterns
Develop systematic testing methodologies
Learn to think like both attacker and defender

For General Users:

Be cautious of suspicious links and forms
Understand that not all websites implement proper security
Develop awareness of common attack techniques


Tools and Resources for Continued Learning
Essential Browser Tools
Developer Tools (F12):

Elements Tab: Inspect and modify HTML structure
Console Tab: Test JavaScript and view error messages
Network Tab: Monitor HTTP requests and responses
Security Tab: Check SSL certificates and connection security


Common Challenges and How to Overcome Them
Challenge 1: Information Overload
Problem: Too many new concepts at once
Solution:

Take breaks between tasks to process information
Create personal notes and summaries
Practice concepts multiple times in different contexts

Challenge 2: Technical Terminology
Problem: Unfamiliar security and web development terms
Solution:

Maintain a personal glossary of terms
Research concepts thoroughly using multiple sources
Join cybersecurity communities for discussion and clarification

Challenge 3: Connecting Theory to Practice
Problem: Understanding concepts but struggling with real-world application
Solution:


Conclusion
Completing TryHackMe's "How Websites Work" room provided an excellent foundation for understanding web security fundamentals. This beginner-friendly introduction successfully bridges the gap between basic computer literacy and cybersecurity expertise.
Most Valuable Insights:

Security is everyone's responsibility: Even simple websites can have serious vulnerabilities
Fundamentals matter: Understanding basic web technologies is crucial for advanced security work
Hands-on practice is essential: Reading about security concepts is different from actually finding and exploiting vulnerabilities

Impact on My Cybersecurity Journey:
This room transformed my understanding of how websites work and opened my eyes to the constant security challenges faced by web developers and security professionals. The hands-on approach made abstract concepts concrete and actionable.
For Fellow Learners:
Whether you're a complete beginner in cybersecurity, a web developer wanting to understand security better, or anyone curious about how the internet works, this room provides invaluable insights that will change how you think about websites forever.
The journey into cybersecurity starts with understanding the basics, and "How Websites Work" provides exactly that foundation. Every expert was once a beginner, and rooms like this make that journey accessible to everyone.

Connect with Me
Found this writeup helpful? I'd love to connect and discuss cybersecurity, web development, and continuous learning!
Find me on:

TryHackMe: [https://tryhackme.com/p/Kile578](https://tryhackme.com/p/Kile578)
LinkedIn: [Kile-driscoll](https://www.linkedin.com/in/kile-driscoll/)
GitHub: [Kile578](https://github.com/Kile578)
Blog: [https://Kile578.github.io/]

Questions or stuck on any part? Feel free to reach out! The cybersecurity community thrives on collaboration and knowledge sharing. We're all learning together on this journey.

Final Words
Remember: always hack ethically and with proper permission. The skills learned here should be used to improve security, not to cause harm. Use your knowledge responsibly to make the internet a safer place for everyone.
Happy learning, and welcome to the world of cybersecurity!

Tags: #TryHackMe #WebSecurity #Cybersecurity #BeginnerFriendly #HTML #JavaScript #SecurityTesting #EthicalHacking #WebDevelopment #InfoSec #CyberSecurity #VulnerabilityAssessment #PenetrationTesting #SecurityAwareness #WebApplicationSecurity

This comprehensive guide represents my personal learning journey through TryHackMe's "How Websites Work" room. All techniques and vulnerabilities discussed are for educational purposes and should only be practiced in authorized environments.