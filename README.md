# Hello!
Welcome to the public space where we (Sienci) plan to store more of our guides and documentation moving forward. We want all our docs to be public so that:
- anyone can [comment or contribute to them](#contributing)
- all our writing work and pictures can be available as plainly as possible for others to see or use
- if you'd like to copy any text or pictures you just need to give us credit and use the same license of [CC BY-SA](https://creativecommons.org/licenses/by-sa/4.0/) 
- we chose this license to guarantee the most long-term benefit to all CNC hobbyists since it ensure the things we all work hard on together stays open to the public

# Contributing
## Simple
If you're new to GitHub and aren't aiming to get your hands too dirty, the easiest way to get involved is just to leave comments about what changes you'd like to see. This could be a spelling mistake, or suggestions on how to improve a section that's missing information. Things like that.

To do this, just click the "Issues" tab near the top left of the page, and click the "New issue" button.

![The GitHub New Issue webpage](/_images/Docs-submit-issue.jpg)

Type out your thoughts, attach some pictures if you like, then click "Submit new issue" and that should notify us to start the process of looking at your idea and seeing what the next steps could be.

![How to write and submit a GitHub issue](/_images/Docs-write-issue.jpg)

## In-Depth
Below, we've tried to include as many instructions as possible so that you can feel confident [making changes](#making-changes) to our documentation yourself, even going as far as [making new pages](creating-new-pages) from scratch! Let's start with the easiest one first.

### Making Changes

When writing the page:
- plain text has no tricks, just write regularly
- headers can use <h></h> tags but can also be #, ##, ###, etc.
- links to external pages ......
- internal links......
- images should always follow "![alt text](/_images/FILE_NAME "Caption"){.aligncenter .size-medium}"
- non-standard images, add to ".size-medium ." then the name of the class you want 
  - flie: for pictures that link to file downloads or other pages
  - nar: when you want a smaller picture with adjustable size
  - wid: full width pictures, only usually for "Parts Needed" of product assembly
  - non: rarely used, for small pictures with removed zooming
- you can still use [shortcodes]
- all normal HTML still works, like:
  - `<h2>Welcome to Our Website!</h2>`
  - `<p>This is a sample HTML page with JavaScript and CSS styling.</p>`
  - Table setup and styling
  - `<button type="button" onclick="showMessage()">Show message</button>`
  - `<script> function showMessage() {alert('Thank you for contacting us!');}</script>`
  - `<section id="home"></section>`
  - `<style> h1 {color: red;} </style>`

### Creating New Pages

title: Test Post 3
menu_order: 4
post_status: draft
post_excerpt: See more on SLB settings and troubleshooting, especially useful on DIY CNC setups to better understand how to configure your SLB for your machine.
post_date: 2024-04-03 18:14:53
taxonomy:
    knowledgebase_cat: slb-handbook
    knowledgebase_tag:
        - slb
custom_fields:
    KBName: SuperLongBoard
    basepress_post_icon: 10
skip_file: no
featured_image: _images/post-image.jpg

When you go to make a new page:
    - set the post_status as "draft" before going to: pending or publish
    - write a title and excerpt for what the content of the page will be
    - the excerpt shouldn't be over 160 characters
    - set the knowledge base and section (cat) using the KB section slug
    - write the KBName which is the normal, capitalized version of the knowledge base
    - based on the menu location of the page, set a post date between the post dates of the surrounding pages    
    - choose a featured image
    - add optional tags
    - doing all this, the above text should stay *bolded*
