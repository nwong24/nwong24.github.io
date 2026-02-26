---
layout: essay
type: essay
title: "Bootstrap and Abstracting CSS"
# All dates must be YYYY-MM-DD format!
date: 2026-02-25
published: true
labels:
  - Software Engineering
  - HTML & CSS
  - BootStrap 5
---

<img width="300px" class="rounded float-start pe-4" src="../img/ui-frameworks/388.png">

### Why not just use HTML and CSS?
When I was first introduced to the idea of Bootstrap, I didn't see the point of using it. After all, why would I spend time learning how to use Bootstrap when I could build any site I wanted to just using HTML and CSS. However, after spending some time digging into a UI framework like Bootstrap, I realized that limiting myself to HTML and CSS would be like writing programs in C without using functions. It would still work the same but it requires a lot more work and rewriting redundant code. With UI frameworks, which are written by developers who are familiar with the tools that people typically use to build websites, we can use write less code and still create a beautiful UI.

### What can Bootstrap do for you?
Bootstrap 5 allows you to modify HTML elements with their predefined classes. For example, if I wanted to enable flexbox I could add the class "d-flex" to an element. Bootstrap also makes the CSS box model easier to use. Instead of going into your style.css file and adding a new line, with Bootstrap you could define that in just a few characters. For example, the class "py-5" means that it will add padding (p) vertically (y). The 5 specifies how much padding you want and is based on a scale that goes from 0-5. This can be changed depending on if you want padding or margin applied, in which direction it should be applied, and its size.

### Advantages of Bootstrap
Using UI frameworks can offer a similar benefit to coding styles. They provide a shared language that team members can use. Different developers working on a single codebase might write custom CSS with their own conventions and styles that other developers would have to spend time reading to understand and work around. On the other hand, Bootstrap's provided classes are a standard that each developer would understand immediately. Using Bootstrap can also speed up the development process. Instead of rewriting common CSS patterns every time for a new site, Bootstrap already has built utilities in mind for developers to quickly plop in. This cuts down on redundant work and allows developers to focus on the contents of the site over the lower level details.
