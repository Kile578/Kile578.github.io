+++
date = '2025-07-14T17:48:13-07:00'
draft = false
title = 'TryHackMe How Websites Work'
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
- Exploring HTML structure and elements
- Understanding JavaScript functionality and interactivity
- Identifying common web application security vulnerabilities
- Developing a security-focused mindset for web technologies

---

## Foundation Knowledge: Understanding Websites

### What is a Website?

A website is essentially a collection of web pages that users can access through the internet. When you visit a website, your browser (like Safari or Google Chrome) makes a request to a web server asking for information about the page you're visiting. The web server - a dedicated computer somewhere else in the world - responds with data that your browser uses to display the page.

### The Request-Response Process

Understanding web communication starts with this simple concept: you make a request to a server, and it responds with data your browser uses to render information. While many other processes are involved in this communication, this fundamental request-response cycle powers every website interaction.

---

## Task 1: How Websites Work - The Foundation

### Understanding Web Architecture

By the end of this room, you'll know how websites are created and be introduced to some basic security issues that affect web applications.

### Major Components of Websites

There are two major components that make up every website:

**1. Front End (Client-Side)**
The frontend is the way your browser renders a website. This includes everything you see and interact with - the visual elements, buttons, text, images, and forms that make up the user interface.

**2. Back End (Server-Side)**
The backend is a server that processes your request and returns a response. This handles all the behind-the-scenes functionality like database operations, user authentication, and business logic.

### The Communication Process

When you visit a website:
1. Your browser makes a request to a web server
2. The server processes your request
3. The server responds with data
4. Your browser uses this data to render the webpage

### Task Challenge

**Question**: What term best describes the component of a web application rendered by your browser?

**Answer**: **Front End** (or **Client-Side**)

**Explanation**: The front end is the component that your browser renders and displays to you as the user interface.

**Key Insight**: Understanding the distinction between frontend and backend is crucial for web security, as vulnerabilities can exist in both layers and require different approaches to identify and prevent.

---

## Task 2: HTML - The Language of the Web

### Understanding HTML Fundamentals

Websites are primarily created using three core technologies:
- **HTML**: To build websites and define their structure
- **CSS**: To make websites look attractive by adding styling options
- **JavaScript**: To implement complex features and interactivity

**H**yper**T**ext **M**arkup **L**anguage (HTML) is the language websites are written in. Elements (also known as tags) are the building blocks of HTML pages and tell the browser how to display content.

### HTML Structure and Components

Every HTML document follows the same basic structure:

```html
<!DOCTYPE html>
<html>
   <head>
       <title>Page Title</title>
   </head>
   <body>
       <h1>Example Heading</h1>
       <p>Example paragraph</p>
   </body>
</html>
```

### HTML Structure Breakdown

**Essential HTML Components:**

- **`<!DOCTYPE html>`**: Defines that the page is an HTML5 document, helping with standardization across different browsers
- **`<html>`**: The root element of the HTML page - all other elements come after this element
- **`<head>`**: Contains information about the page (such as the page title)
- **`<body>`**: Defines the HTML document's body; only content inside the body is shown in the browser
- **`<h1>`**: Defines a large heading
- **`<p>`**: Defines a paragraph

### HTML Elements and Attributes

HTML offers many different elements for various purposes:
- **Buttons**: `<button>`
- **Images**: `<img>`
- **Lists**: `<ul>`, `<ol>`, `<li>`
- **Links**: `<a>`

### Working with Attributes

Tags can contain attributes that provide additional functionality:

**Class Attribute:**
```html
<p class="bold-text">This text can be styled</p>
```

**Source Attribute for Images:**
```html
<img src="img/cat.jpg">
```

**Multiple Attributes:**
```html
<p attribute1="value1" attribute2="value2">Content</p>
```

**ID Attribute:**
```html
<p id="example">Unique element</p>
```

**Important Note**: Unlike class attributes (where multiple elements can use the same class), each element must have a unique ID to identify it specifically. IDs are used for styling and JavaScript targeting.

### Viewing HTML Source Code

You can view the HTML of any website by:
- **Chrome**: Right-clicking and selecting "View Page Source"
- **Safari**: Right-clicking and selecting "Show Page Source"

### Task Challenges

**Challenge 1: Basic HTML Rendering**
*Task*: Click the "View Site" button and experiment with the HTML renderer

*Solution*: Use the HTML box to enter code and click "Render HTML Code" to see results

**Challenge 2: Fixing Broken Images**
*Question*: One of the images on the cat website is broken - fix it, and the image will reveal the hidden text answer!

*Problem*: The broken image was missing the proper file extension
*Solution*: Add the correct file extension to complete the image path

*Answer Revealed*: ***HTMLHERO***

**Challenge 3: Adding New Elements**
*Task*: Add a dog image to the page by adding another img tag on line 11. The dog image location is img/dog-1.png. What is the text in the dog image?

*Solution*:
```html
<img src="img/dog-1.png">
```

*Answer*: [Text visible in the dog image after adding the element]

### HTML Security Implications

Understanding HTML is crucial for web security because:
- HTML comments can contain sensitive information
- Improperly structured HTML can lead to injection vulnerabilities
- Client-side code is always visible to users
- All HTML elements and attributes are accessible through browser developer tools

---

## Task 3: JavaScript - Bringing Websites to Life

### Understanding JavaScript's Role

JavaScript (JS) is one of the most popular coding languages in the world and allows pages to become interactive. While HTML creates the website structure and content, JavaScript controls the functionality of web pages.

### Static vs. Dynamic Content

**Without JavaScript**: Pages would not have interactive elements and would always be static
**With JavaScript**: Pages can:
- Dynamically update content in real-time
- Respond to user interactions (clicks, hovers, form submissions)
- Change styling based on events
- Display moving animations
- Provide complex functionality

### Adding JavaScript to Web Pages

JavaScript can be included in web pages in two primary ways:

**Inline JavaScript (within script tags):**
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

**Basic DOM Manipulation:**
```javascript
document.getElementById("demo").innerHTML = "Hack the Planet";
```

This code:
1. Finds an HTML element with the ID "demo"
2. Changes the element's content to "Hack the Planet"

**Interactive Button with Events:**
```html
<button onclick='document.getElementById("demo").innerHTML = "Button Clicked";'>Click Me!</button>
```

This creates a button that, when clicked, changes the content of the "demo" element to "Button Clicked".

### JavaScript Events

HTML elements can have events such as:
- **onclick**: Executes when the element is clicked
- **onhover**: Executes when the mouse hovers over the element
- **onload**: Executes when the page loads
- **onsubmit**: Executes when a form is submitted

**Important Note**: onclick events can be defined either directly on elements (as shown above) or inside JavaScript script tags.

### Task Challenges

**Challenge 1: Content Modification**
*Question*: Click the "View Site" button on this task. On the right-hand side, add JavaScript that changes the demo element's content to "Hack the Planet"

*Solution*: Add the JavaScript code to change the element content
```javascript
document.getElementById("demo").innerHTML = "Hack the Planet";
```

*Answer Revealed*: ***JSISFUN***

**Challenge 2: Interactive Button**
*Task*: Add the button HTML from this task that changes the element's text to "Button Clicked" on the editor on the right, update the code by clicking the "Render HTML+JS Code" button and then click the button.

*Solution*: Implement the onclick event handler:
```html
<button onclick='document.getElementById("demo").innerHTML = "Button Clicked";'>Click Me!</button>
```

### JavaScript Security Implications

Understanding JavaScript is crucial for web security because:
- **Client-side execution**: JavaScript runs in the user's browser, making it accessible and modifiable
- **DOM manipulation**: JavaScript can alter page content and behavior dynamically
- **Event-driven programming**: User interactions can trigger code execution
- **Input handling**: JavaScript often processes user input, creating potential injection points
- **Third-party scripts**: External JavaScript files can introduce vulnerabilities

---

## Task 4: Sensitive Data Exposure - A Critical Security Flaw

### Understanding the Vulnerability

Sensitive Data Exposure occurs when a website doesn't properly protect (or remove) sensitive clear-text information from the end-user. This vulnerability is usually found in a site's frontend source code and represents one of the most common security mistakes in web development.

### How Sensitive Data Gets Exposed

Since websites are built using HTML elements (tags), all of which we can see by "viewing the page source," developers may accidentally leave behind:
- Login credentials
- Hidden links to private parts of the website
- API keys and tokens
- Internal comments with sensitive information
- Database connection strings
- Other sensitive data in HTML or JavaScript

### The Investigation Process

When assessing a web application for security issues, one of the first things you should do is review the page source code to look for:
- Exposed login credentials
- Hidden links
- Comments containing sensitive information
- Hardcoded API keys
- Internal URLs and endpoints

### Potential Impact

Sensitive information can be leveraged to:
- Gain unauthorized access to other parts of the application
- Access backend components of the site
- Escalate privileges within the system
- Discover hidden functionality
- Compromise user accounts

### Task Challenge

**Question**: View the website on this link. What is the password hidden in the source code?

**Investigation Process**:
1. Navigate to the target website
2. Right-click and select "View Page Source"
3. Search through the HTML source code
4. Look for comments, hidden fields, or JavaScript variables
5. Search for common keywords like "password", "admin", "login"

**Answer**: ***testpasswd***

**Real-World Security Implications**:
- Anyone can view client-side source code
- This type of exposure is surprisingly common in real applications
- Automated tools can scan for exposed credentials across entire websites
- Such vulnerabilities can lead to complete system compromise

### Prevention Strategies

- **Never store sensitive data in client-side code**
- **Use environment variables for configuration**
- **Implement proper authentication systems**
- **Regular security code reviews**
- **Automated scanning for exposed secrets**
- **Remove all debug information from production**

---

## Task 5: HTML Injection - Understanding Client-Side Attacks

### What is HTML Injection?

HTML Injection is a vulnerability that occurs when unfiltered user input is displayed on the page. If a website fails to sanitize user input (filter any "malicious" text that a user inputs into a website), and that input is used on the page, an attacker can inject HTML code into a vulnerable website.

### The Importance of Input Sanitization

Input sanitization is very important in keeping a website secure because:
- Information a user inputs is often used in other frontend and backend functionality
- Unsanitized input can lead to various injection attacks
- User input should never be trusted without proper validation
- This vulnerability affects client-side functionality directly

### How HTML Injection Works

When a user has control of how their input is displayed, they can:
1. Submit HTML (or JavaScript) code in input fields
2. The browser processes this code as legitimate HTML
3. The injected code becomes part of the page
4. The attacker gains control over page appearance and functionality

### Technical Example

Consider a form that outputs text to the page. If user input from a "What's your name" field is passed directly to a JavaScript function without sanitization:

**Vulnerable Code Pattern**:
```javascript
function displayName(name) {
    document.getElementById("output").innerHTML = "Hello " + name;
}
```

**If a user enters**: `<h1>Hacked!</h1>`
**The output becomes**: `Hello <h1>Hacked!</h1>`

The browser renders this as actual HTML, displaying "Hacked!" as a large heading instead of plain text.

### Practical Exploitation

**Objective**: Inject HTML to display a malicious link to http://hacker.com

**Solution**:
```html
<a href="http://hacker.com">Click here for free stuff!</a>
```

**How it works**:
- `<a href="http://hacker.com">` creates a clickable link to the malicious site
- `Click here for free stuff!` provides enticing text to trick users
- `</a>` properly closes the HTML anchor tag

### Advanced Payload Examples

**Basic malicious link**:
```html
<a href="http://hacker.com">Click here for free stuff!</a>
```

**Opens in new tab to avoid suspicion**:
```html
<a href="http://hacker.com" target="_blank">Important Update</a>
```

**Styled to look official**:
```html
<a href="http://hacker.com" style="color: red; font-weight: bold;">Security Alert - Click Here</a>
```

### Task Challenge

**Question**: View the website on this task and inject HTML so that a malicious link to http://hacker.com is shown.

**Solution**: Enter the HTML injection payload in the vulnerable input field:
```html
<a href="http://hacker.com">Click here for free stuff!</a>
```

**Answer Revealed**: ***HTML_INJ3CTI0N***

### The General Security Rule

**Never trust user input.** To prevent malicious input, website developers should sanitize everything the user enters before using it in any function. In the case of HTML injection, developers should remove or encode HTML tags to prevent them from being interpreted as code.

### Prevention Strategies

- **Input Sanitization**: Filter and validate all user input before processing
- **Output Encoding**: Encode special characters before displaying user input
- **Content Security Policy (CSP)**: Implement CSP headers to restrict inline script execution
- **Regular Security Testing**: Conduct automated and manual vulnerability assessments
- **Input Validation**: Implement both client-side and server-side validation
- **Principle of Least Privilege**: Limit what user input can affect on the page

### Real-World Security Implications

HTML injection can lead to:
- **Phishing attacks**: Malicious links that appear legitimate
- **Content modification**: Changing page content to mislead users
- **Social engineering**: Using injected content to trick users
- **XSS preparation**: HTML injection can be a stepping stone to Cross-Site Scripting
- **User trust compromise**: Users may lose confidence in the website's security

---

## Key Takeaways and Lessons Learned

### Technical Skills Developed

**Web Architecture Understanding:**
- Mastered the client-server communication model
- Learned the distinction between frontend and backend systems
- Understood how browsers process and render web content

**HTML and JavaScript Proficiency:**
- Gained hands-on experience with HTML structure and syntax
- Learned JavaScript DOM manipulation and event handling
- Developed debugging skills using browser developer tools
- Understanding of how HTML elements and attributes work together

**Security Awareness:**
- Identified common vulnerability patterns in web applications
- Learned systematic approaches to security testing
- Understood the real-world impact of coding mistakes
- Developed skills in source code analysis

### Security Mindset Development

**Always Assume User Input is Malicious:**
This room reinforced the fundamental security principle that user input should never be trusted without proper validation and sanitization.

**Client-Side Code is Public:**
Everything sent to the browser is accessible to users, making it crucial to never include sensitive information in client-side code.

**Small Mistakes Have Big Consequences:**
Simple oversights like missing input validation or exposed credentials can lead to complete system compromise.

**Security is Everyone's Responsibility:**
Even simple websites can have serious vulnerabilities, making security awareness important for all web developers.

### Real-World Applications

**For Web Developers:**
- Implement proper input validation and output encoding
- Use secure coding practices from the beginning
- Regular security testing should be part of the development process
- Never store sensitive information in client-side code

**For Security Professionals:**
- Understand common vulnerability patterns
- Develop systematic testing methodologies
- Learn to think like both attacker and defender
- Master source code analysis techniques

**For General Users:**
- Be cautious of suspicious links and forms
- Understand that not all websites implement proper security
- Develop awareness of common attack techniques
- Know how to inspect page source for learning purposes

---

## Tools and Resources for Continued Learning

### Essential Browser Tools

**Developer Tools (F12):**
- **Elements Tab**: Inspect and modify HTML structure
- **Console Tab**: Test JavaScript and view error messages
- **Network Tab**: Monitor HTTP requests and responses
- **Security Tab**: Check SSL certificates and connection security
- **Sources Tab**: View and debug JavaScript code

### Recommended Learning Resources

**TryHackMe Rooms:**
- OWASP Top 10 - Learn about the most critical web application security risks
- Web Fundamentals - Deeper dive into web technologies
- Burp Suite Basics - Learn professional web application testing tools

**External Resources:**
- MDN Web Docs - Comprehensive HTML, CSS, and JavaScript documentation
- OWASP Foundation - Web application security guidelines and best practices
- PortSwigger Web Security Academy - Free online web security training

---

## Common Challenges and How to Overcome Them

### Challenge 1: Information Overload

**Problem**: Too many new concepts at once
**Solution:**
- Take breaks between tasks to process information
- Create personal notes and summaries
- Practice concepts multiple times in different contexts
- Focus on understanding one concept thoroughly before moving to the next

### Challenge 2: Technical Terminology

**Problem**: Unfamiliar security and web development terms
**Solution:**
- Maintain a personal glossary of terms
- Research concepts thoroughly using multiple sources
- Join cybersecurity communities for discussion and clarification
- Use browser developer tools to see concepts in action

### Challenge 3: Connecting Theory to Practice

**Problem**: Understanding concepts but struggling with real-world application
**Solution:**
- Practice on safe, legal testing environments
- Build simple websites to experiment with concepts
- Use browser developer tools on legitimate websites (for learning only)
- Join beginner-friendly cybersecurity communities

### Challenge 4: Source Code Analysis

**Problem**: Difficulty finding information in HTML source code
**Solution:**
- Use browser search function (Ctrl+F) to find keywords
- Learn to read HTML structure systematically
- Practice on different websites to build pattern recognition
- Use developer tools "Elements" tab for easier navigation

---

## Conclusion

Completing TryHackMe's "How Websites Work" room provided an excellent foundation for understanding web security fundamentals. This beginner-friendly introduction successfully bridges the gap between basic computer literacy and cybersecurity expertise.

### Most Valuable Insights:

**Security is Everyone's Responsibility**: Even simple websites can have serious vulnerabilities, making security awareness crucial for developers, security professionals, and users alike.

**Fundamentals Matter**: Understanding basic web technologies (HTML, JavaScript, client-server communication) is crucial for advanced security work.

**Hands-on Practice is Essential**: Reading about security concepts is different from actually finding and exploiting vulnerabilities in a controlled environment.

**User Input is Never Trustworthy**: The importance of input validation and sanitization cannot be overstated in web security.

### Impact on My Cybersecurity Journey:

This room transformed my understanding of how websites work and opened my eyes to the constant security challenges faced by web developers and security professionals. The hands-on approach made abstract concepts concrete and actionable, providing a solid foundation for more advanced web security topics.

### For Fellow Learners:

Whether you're a complete beginner in cybersecurity, a web developer wanting to understand security better, or anyone curious about how the internet works, this room provides invaluable insights that will change how you think about websites forever.

The journey into cybersecurity starts with understanding the basics, and "How Websites Work" provides exactly that foundation. Every expert was once a beginner, and rooms like this make that journey accessible to everyone.

---

## Connect with Me

Found this writeup helpful? I'd love to connect and discuss cybersecurity, web development, and continuous learning!

Find me on:
- **TryHackMe**: [https://tryhackme.com/p/driscollkile](https://tryhackme.com/p/driscollkile)
- **LinkedIn**: [Kile-driscoll](https://www.linkedin.com/in/kile-driscoll/)
- **GitHub**: [Kile578](https://github.com/Kile578)
- **Blog**: [https://kile578.github.io/](https://kile578.github.io/)

Questions or stuck on any part? Feel free to reach out! The cybersecurity community thrives on collaboration and knowledge sharing. We're all learning together on this journey.

---

## Questions for Further Exploration

**Advanced Web Security Concepts:**

With the fundamentals of HTML, JavaScript, and common vulnerabilities covered, several advanced questions emerge for further exploration:

**Consider these questions:**

1. **Input Validation vs. Output Encoding**: We learned about HTML injection and the importance of input sanitization. What's the difference between input validation and output encoding, and when should each be used?

2. **Client-Side vs. Server-Side Security**: Since we discovered that client-side code is always visible, how do we balance functionality with security? What security measures should be implemented on the server-side?

3. **Modern Web Security Headers**: What are Content Security Policy (CSP) headers, and how do they help prevent the types of attacks we explored in this room?

4. **Progressive Security Learning**: This room covered basic vulnerabilities, but how do these relate to more advanced attacks like Cross-Site Scripting (XSS), SQL Injection, and Cross-Site Request Forgery (CSRF)?

5. **Defensive Development**: As a developer, how can you implement security-by-design principles from the beginning of a project rather than adding security as an afterthought?

**Research Challenge:**

Explore the OWASP Top 10 list and identify how the vulnerabilities we learned about in this room relate to the most critical web application security risks. How do Sensitive Data Exposure and HTML Injection fit into the broader web security landscape?

**Discussion Points:**

- What are the legal and ethical implications of testing for these vulnerabilities on websites you don't own?
- How do modern web frameworks help prevent the basic vulnerabilities we explored?
- What role does security awareness training play in preventing these common mistakes?
- How has web security evolved with the rise of single-page applications and modern JavaScript frameworks?

These questions bridge the gap between learning basic web concepts and understanding the advanced security methodologies that make cybersecurity a constantly evolving field. They prepare you for deeper exploration into web application security testing and secure development practices.

---

## Final Words

Remember: always practice ethically and with proper permission. The skills learned here should be used to improve security, not to cause harm. Use your knowledge responsibly to make the internet a safer place for everyone.

The concepts covered in this room form the foundation for advanced web security topics. Continue practicing in authorized environments, stay curious, and always keep learning. The web security field is constantly evolving, and understanding these fundamentals will serve you well as you advance in your cybersecurity journey.

Happy learning, and welcome to the world of web security!

---

**Tags:** #TryHackMe #WebSecurity #Cybersecurity #BeginnerFriendly #HTML #JavaScript #SecurityTesting #EthicalHacking #WebDevelopment #InfoSec #VulnerabilityAssessment #SecurityAwareness #WebApplicationSecurity #HTMLInjection #SensitiveDataExposure

---

*This comprehensive guide represents my personal learning journey through TryHackMe's "How Websites Work" room. All techniques and vulnerabilities discussed are for educational purposes and should only be practiced in authorized environments.*