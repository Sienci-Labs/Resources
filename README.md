---
skip_file: yes
---

# Hello!

Welcome to the public space where we (Sienci) plan to store more of our guides and documentation moving forward. We want all our docs to be public so that:

- anyone can [comment or contribute to them](#contributing)
- all our writing work and pictures can be available as plainly as possible for others to see or use
- if you'd like to copy any text or pictures you just need to give us credit and use the same [CC BY-SA license](https://creativecommons.org/licenses/by-sa/4.0/)
- we chose this license to guarantee the most long-term benefit to all CNC hobbyists since it ensures that the things we all work hard on together stays open to the public

# Contributing

Do you want to make **[simple](#simple)** edits, or something more **[in-depth](#in-depth)**?

## Simple

If you're new to GitHub and aren't aiming to get your hands too dirty, the easiest way to get involved is just to leave comments about what changes you'd like to see. This could be a spelling mistake, or suggestions on how to improve a section that's missing information. Things like that.

To do this, just click the "**Issues**" tab near the top left of the page, and click the "**New issue**" button.

> ![The GitHub New Issue webpage](/_git/Docs-submit-issue.jpg)

Type out your thoughts, attach some pictures if you like, then click "**Submit new issue**" and that should notify us to start the process of looking at your idea and seeing what the next steps could be.

> ![How to write and submit a GitHub issue](/_git/Docs-write-issue.jpg)

## In-Depth

Below, we've tried to include as many instructions as possible so that you can feel confident **[making changes](#making-changes)** to our documentation yourself, even going as far as **[making new pages](#creating-new-pages)** from scratch! Let's start with the easiest one first.

### Making Changes

To find the page you'd like to change, the easiest way is to go to the page on our [Resources site](https://resources.sienci.com/) and click the "**Suggest edits to this Page**" button at the top,right of the page. Alternatively, you can go through the GitHub folders until you find a page with the same URL.

Once you're at the document, you'll be able to edit it with your changes by clicking the pencil.

> ![Editing a GitHub document](/_git/Docs-edit-page.jpg)

If you want to see a closer version of what your writing will look like once it's posted, you can also preview the changes you're making in the '**Preview**' tab at the top left.

While writing, keep in mind:

1. Try to keep writing succinct
1. Pages tend to be written in a simple tone, only using complex terms when necessary
1. **Writing** in plain text has no tricks, just write regularly and leave a blank line between paragraphs
1. **Headers** can use #, ##, ###, etc. but can also use `<h></h>` tags
1. Bolding uses `**bold**`, Italic uses `*italic*`
1. Make **lists** with HTML or like
    > &nbsp;- One &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1. One<br>
    > &nbsp;- Two &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1. Two<br>
    > &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Two A &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1. Two A<br>
    > &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Two B &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1. Two B<br>
    > &nbsp;- Three &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1. Three<br>
1. **Links** use `[Link text](URL)` or just `<URL>`
1. Links to other headers on the page `[Link text](#header)`
1. Link to other git pages with `[Test post](/test/article.md)`
1. If you want to link in a new tab `<a href="URL" target="_blank" rel="noopener">Link text</a>`
1. **Images** should always follow `![Alt text](/_images/FILE_NAME "Caption"){.aligncenter .size-medium}`
1. Non-standard images, add to ".size-medium` .`" then the name of the class you want
    - flie: for pictures that link to file downloads or other pages (remember to surround the image with the URL code)
    - nar: when you want a smaller picture with adjustable size
    - wid: full width pictures, only usually for "Parts Needed" of product assembly
    - non: rarely used, for small pictures with removed zooming
1. If you want to custom-style the image then you have to use raw HTML, like `<img class="aligncenter size-medium" style="padding: 5% 15%;" src="Sync the image to WP first, then come back and fill out this link"/>`
1. You can still use any **`[Shortcodes]`** from WordPress plugins, like:
    - Direct YouTube links
    - Direct product links `https://sienci.com/product/lightburn/`
    - Tabs `[tabby title="Title" open="yes"]Content[tabbyending]`
    - Spoilers `[su_spoiler title="Title" open="no" style="fancy" icon="chevron" anchor_in_url="no"]Content[/su_spoiler]`
    - Buttons `[su_button url="URL" target="self" style="flat" background="var(--sl-blue)" radius="3" color="#FFFFFF" size="8" wide="no" center="yes" icon="" icon_color="#FFFFFF" text_shadow="none"]Button text[/su_button]`
    - CSVs `[su_csv_table url="URL" header="yes" responsive="yes"]`
1. Code can be noted as `` `code` ``
1. All **normal HTML** still works, like:
    - `<h2>Welcome to Our Website!</h2>`
    - `<p>This is a sample HTML page with JavaScript and CSS styling.</p>`
    - Table setup and styling
    - `span class="redText", "blueText", "orgText", "greText"`
    - `<style> h1 {color: red;} </style>`
    - `&nbsp;` for adding extra spaces
    - `<section id="home"></section>`
    - `<button type="button" onclick="showMessage()">Show message</button>`
    - `<script> function showMessage() {alert('Thank you for contacting us!');}</script>`
1. If you still need more help, visit <https://www.markdownguide.org/basic-syntax/> for more formatting tips

Once you're satisfied, you can press the "**Commit changes...**" button.

> ![Previewing GitHub doc changes and Committing them](/_git/Docs-write-page.jpg)

After this, you'll be guided through giving your changes a **Title**, **Description**, and then the ability to make a new "**Branch**" where your changes can live until they're reviewed and implemented.

### Creating New Pages

When you go to make a new page, choose what Knowledge Base you'd like the page to be in, and you'll find that it has a corresponding folder in GitHub. Each folder has its own "**_template.md**" page that you can copy and paste to start off your own, new page.

Before you get started writing:

1. Set the **post_status** as "draft" before going to "pending" or "publish"
1. Write a **title** and **excerpt** for what the content of the page will be (emojis still work)
1. The excerpt shouldn't be over 160 characters
1. Set the knowledge base and section (cat) using the **KB section** slug
1. Write the **KBName** which is the normal, capitalized version of the knowledge base
1. Based on the menu location of the page, set a **post date** between the post dates of the surrounding pages
1. Choose a **featured image**
1. Add **optional tags**
1. Doing all this, the text from the template should stay **bolded**

Once done, you can begin writing. Please keep in mind the same rules as when **[making changes](#making-changes)**, then submit your page as a new branch for review.

If you encounter any other quirks, refer to the docs of the plugin being used to sync these pages to WordPress <https://www.aakashweb.com/docs/git-it-write/>.
