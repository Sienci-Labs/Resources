---
skip_file: yes
---

## Hello!

Welcome to the public space where we (Sienci) plan to store more of our guides and documentation moving forward. We want all our docs to be public so that:

- anyone can [comment or contribute to them](#contributing)
- all our writing work and pictures can be available as plainly as possible for others to see or use
- if you'd like to copy any text or pictures you just need to give us credit and use the same [CC BY-SA license](https://creativecommons.org/licenses/by-sa/4.0/)
- we chose this license to guarantee the most long-term benefit to all CNC hobbyists since it ensures that the things we all work hard on together stays open to the public

## Contributing

Do you want to make **[simple](#simple)** edits, or something more **[in-depth](#in-depth)**? We also have sections on staying **[up-to-date](#stay-up-to-date)** on our docs and a recommended **[editing setup](#editing-setup)** if you plan to make frequent contributions.

### Simple

If you're new to GitHub and aren't aiming to get your hands too dirty, the easiest way to get involved is just to leave comments about what changes you'd like to see. This could be a spelling mistake, or suggestions on how to improve a section that's missing information. Things like that.

To do this, just click the "**Issues**" tab near the top left of the page, and click the "**New issue**" button.

> ![The GitHub New Issue webpage](/_git/Docs-submit-issue.jpg)

Type out your thoughts, attach some pictures if you like, then click "**Submit new issue**" and that should notify us to start the process of looking at your idea and seeing what the next steps could be.

> ![How to write and submit a GitHub issue](/_git/Docs-write-issue.jpg)

If you want to do a little more, you can also be more detailed with your feedback by pointing to specific areas that need fixing. You can find the page you want to comment on by going to the [Resources site](https://resources.sienci.com/) and clicking the "**Suggest edits to this Page**" button at the top, right of the page - or look for it in the GitHub folders. Once you're there, click the 'Code' tab and scroll down to find the text you'd like to comment on. You'll be able to click the line number, then the '...', then 'Copy permalink' which you can then reference in the issue you submit to us by pasting in the link.

> ![Code tab of GitHub document clicking a line to copy the permalink](/_git/Docs-code-line.jpg)

### In-Depth

Below, we've tried to include as many instructions as possible so that you can feel confident **[making changes](#making-changes)** to our documentation yourself, even going as far as **[making new pages](#creating-new-pages)** from scratch! Let's start with the easiest one first.

#### Making Changes

To find the page you'd like to change, the easiest way is to go to the page on our [Resources site](https://resources.sienci.com/) and click the "**Page Suggestions?**" button at the top, right of the page. Alternatively, you can go through the GitHub folders until you find a page with the same URL.

Once you're at the document, you'll be able to edit it with your changes by clicking the pencil.

> ![Editing a GitHub document](/_git/Docs-edit-page.jpg)

If you want to see a closer version of what your writing will look like once it's posted, you can also preview the changes you're making in the '**Preview**' tab at the top left.

While writing, keep in mind:

1. Try to keep writing succinct
1. Pages tend to be written in a simple tone, only using complex terms when necessary
1. **Writing** in plain text has no tricks, just write regularly and leave a blank line between paragraphs (hit 'enter' twice to put text on a separate line)
1. **Headers** can use `# H1`, `## H2`, `### H3`, etc. but can also use `<h></h>` tags
1. Bolding uses `**bold**`, Italic uses `*italic*`
1. Make **lists** with HTML or like below (note: indents need **4 spaces** to work, also the numbered lists should **always use 1** since they will be automatically formatted afterwards)
    > &nbsp;Bullet list &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Numbered List<br>
    > &nbsp;- One &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1. One<br>
    > &nbsp;- Two &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1. Two<br>
    > &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Two A &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1. Two A<br>
    > &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Two B &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1. Two B<br>
    > &nbsp;- Three &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1. Three<br>
1. **Links** use `[Link text](URL)` or just `<URL>`
1. Links to other headers on the page `[Link text](#header-text)`(will link to any header called "Header Text")
1. Link to other git pages with `[Test post](/test/article.md)`
1. Link that opens in a new browser tab `<a href="URL" target="_blank" rel="noopener">Link text</a>`
1. **Images** should always follow `![Alt text](/_images/FILE_NAME "Caption"){.aligncenter .size-medium}`
1. Non-standard images, add to "`.size-medium .`" then the name of the class you want
    - flie: for pictures that link to file downloads or other pages (remember to surround the image with the URL code)
    - nar: when you want a smaller picture with adjustable size
    - wid: full width pictures, only usually for "Parts Needed" of product assembly
    - non: rarely used, for small pictures with removed zooming
1. If you want to custom-style the image (height, width, padding, etc.) then you have to use raw HTML, like `<img class="aligncenter size-medium" style="padding: 5% 15%;" src="Sync the image to WP first, then come back and fill out this link" style="max-width: 300px/60%;"/>`
1. You can put links on images like `[![](/_images/FILE_NAME){.class}](URL)`
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
1. If you still need more help because something isn't listed or working, first check the **[caveats section](#caveats)** or otherwise visit <https://www.markdownguide.org/basic-syntax/> for more formatting tips
1. It's also technically [compatible with WordPress' block editor](https://developer.wordpress.org/block-editor/getting-started/faq/#how-is-data-stored-ive-seen-html-comments-what-is-their-purpose ) which isn't used for our docs, but interesting nonetheless

Once you're satisfied, you can press the "**Commit changes...**" button.

> ![Previewing GitHub doc changes and Committing them](/_git/Docs-write-page.jpg)

After this, you'll be guided through giving your changes a **Title**, **Description**, and then the ability to make a new "**Branch**" which you can name appropriately. Once you 'Propose Changes' all your ideas and changes will be saved and posted in the GitHubs 'Pull requests' tab where they can be reviewed, discussed, and implemented.

> ![Propose changes by giving a title, description, and making a new branch with an appropriate name](/_git/Docs-propose-changes.jpg)

#### Creating New Pages

When you go to make a new page, choose what Knowledge Base you'd like the page to be in, and you'll find that it has a corresponding folder in GitHub. Each folder has its own "**index.md**" page that you can use as a template to start off your own new page. Copy the index file text with the copy button, before creating your new file with the '+' button and pasting in the template text.

> ![Click the "copy raw" button, then the plus to make a new page](/_git/Docs-start-new.jpg)

Then name your new file the way you'd like it to appear as a URL and write ".md" at the end (example: **slb-welcome.md**).

Before you get started writing, look over the text you just pasted in and edit it to match the intent of your new page:

1. Write a **title** and **post_excerpt** for what the content of the page will be (emojis still work)
1. The excerpt shouldn't be over 160 characters
1. Write the **post_status** as "draft" if you don't plan on "publish"ing it yet
1. Choose what section the page will appear in in the docs by typing out the **knowledgebase_cat**, the template should list all current options for that Knowledge Base
1. Choose what specific order the page will appear in by entering a **post date** that falls between the post dates of the surrounding pages (**example:** go find the starting text of the other pages, then if you want to appear between the 'Welcome' page with date 2024-03-03 and the 'Upgrading' page with date 2024-03-22, then any date between them will make the page appear where you want - like 2024-03-12)
1. Choose a **featured image** or leave it blank if you don't have one yet
1. Add **optional tags**
1. Change **skip_file** to "no" if you'd like to begin syncing your page to the WordPress site
1. Doing all this, the text from the template should stay **bolded**

Once done, you can begin writing. Please keep in mind the same rules as when **[making changes](#making-changes)**, then submit your page as a new branch for review.

If you encounter any other quirks, refer to the docs of the plugin being used to sync these pages to WordPress <https://www.aakashweb.com/docs/git-it-write/>.

#### Caveats

If you're finding that something isn't working that you'd expect - check the README again or use 'Ctrl + F' to search the page, or otherwise see below some known compatibility issues:

- Image classes and WordPress shortcodes can't be rendered by GitHub because it doesn't know what they are, so the only way to do final checks is to push to WordPress and check there
- WordPress Galleries don't seem possible
- Sometimes having "$" surround text makes the Git Preview look odd, but it formats fine in WordPress
- Don't yet have docs explaining how to upload pictures or set featured pictures
- If you're changing a picture but keeping the same file name, then you'll need to delete the current picture off WordPress to sync the new one
- Image captions should work (more or less) as long as long as wp-content ➜ plugins ➜ git-it-write ➜ includes ➜ parsedown.php ➜ line 188 is changed to `'class' => 'wp-caption-text'` (see <https://github.com/vaakash/git-it-write/issues/46>)
- YouTube videos, Product links, and Button shortcodes should work as long as wp-content ➜ plugins ➜ git-it-write ➜ includes ➜ parsedown.php ➜ line 55 the extra function `public function inlineUrl($excerpt) {return;}` is added (see <https://github.com/vaakash/git-it-write/issues/45>)

## Stay Up-to-Date

- If you like what we're doing here, let others know by giving this repository a 'Star'
- If you want to be informed when we make updates to our docs, click the button to 'Watch' it as it changes
- You can edit how or how often you get notified by going to your Profile ➜ Settings ➜ Notifications

> ![How to Star and Watch GitHub repos](/_git/Docs-stay-informed.jpg)

## Editing Setup

If you plan to commit a more dedicated setup to editing CNC resources, we have some recommendations that should make your life a lot easier for bulk writing, uploading, and editing:

1. Create a new folder on your computer in the 'Documents' called "GitHub", then create another folder inside GitHub called "Resources"
1. [Download VS Code](https://code.visualstudio.com/download) and install it normally
1. When you open VS Code you can choose a Theme if you like, but you can always go back by going to Settings ➜ Themes ➜ Color Theme
1. In VS Code click File ➜ Open Folder ... ➜ then go to the "Resources" folder and press 'Select Folder'
1. Go to the source control tab on the left bar of VS Code and click the link to download and set up git ([should go here](https://git-scm.com/download/win))
1. During installation, you'll be prompted to make a lot of selections, and we recommend:
    1. Uncheck Windows Explorer integrated commands
    1. Use Visual Studio Code as Git's default editor
    1. Let Git decide its default branch name
    1. Git from the command line and also from 3rd-party software
    1. Use bundled OpenSSH
    1. Use the OpenSSL library
    1. Checkout Windows-style, commit Unix-style line endings
    1. Use MinTTY
    1. Fast-forward or merge
    1. Git Credential Manager
    1. Enable file system caching
1. Once it's installed, open the 'Git Bash' application and in the command line send the following commands one at a time to save your GitHub login to your computer
    1. `git config --global user.name "YourUsername"`
    1. `git config --global user.email "your-email@website.com"`
    1. `git config --global user.password "1234321"`
    1. `git config --global credential.helper store`
1. Go back to VS Code and click the 'refresh' link. After it reloads, you'll be able to click `...` ➜ Clone ➜ then paste in the URL of this repo (`https://github.com/Sienci-Labs/Resources.git`) and sync it to the Documents ➜ GitHub folder you made at the start
1. If this all looks like it set up correctly, try to test out making a contribution
    1. Go to the File Tab in GitHub and open a file like the README
    1. Type something, then File ➜ Save or Ctrl+S
    1. Go back to the source control tab and click `...` ➜ Branch ➜ Create Branch... ➜ type the Branch name ➜ hit 'Enter'
    1. In this new branch, you should be able to leave a 'Commit message', then click the `⌄` part of the blue Commit button, then click 'Commit and Push'
    1. If it says you haven't authorized the git ecosystem, then go through the steps to do that
    1. It also might alert you that you haven't staged anything yet, but you can just click 'Always' for this
    1. At the end of all this you should be able to go back to the online GitHub page and click the dropdown next to 'main' and see the new branch you just created
1. Once done, go to the Extensions tab and install:
    - **markdownlint** (we've set it up to give yellow warnings if your writing might cause structural issues <https://github.com/DavidAnson/markdownlint/blob/main/schema/.markdownlint.jsonc>)
    - **Code Spell Checker** (set up to help check spelling)
    - **Canadian English - Code Spell Checker** (since we tend to write in Canadian English)
    - **Batch Rename** (if you plan to rename large groups of files)
1. Also a great website if you end up frequently making HTML tables is <https://www.tablesgenerator.com/html_tables#>

Guide on using Git source control: <https://code.visualstudio.com/docs/sourcecontrol/overview>

## Content Migration

If you're looking to bulk-transfer content over from another source, here are some tips on doing that:

1. Make sure you have permission or a compatible license from the source you're using and give attribution where necessary
1. Once text is pasted over, if you're making a new page then please first go through the process outlined in **[Creating New Pages](#creating-new-pages)** where you set a title, description, URL, date, etc.
1. Make any applicable text updates
1. Check for and correct any warnings or spelling errors
1. Upload all raw pictures to GitHub, and if you want to organize them into folders then ensure new folders begin with an underscore, spaces are replaced with a dash, and there aren't any capital letters
1. Replace all image references to proper markdown using the new file names and locations unless the images have specialized styling in which case leave them as HTML and just update the image link once it gets synced to WordPress
1. Insert "ytsb" into page URLs and Titles if you'd like to sync commit them as drafts and make final 1-to-1 comparisons on the WordPress site
1. GiW can only handle syncing about 80 pictures at a time, so if you're pushing more than that to main then you'll need to manually Pull Changes repeatedly until everything comes through
1. Only once you're ready, publish pages with matched up the Titles and URLs to existing pages - this will have GIW overwrite the new page onto the old one and keep it synced moving forward (don't forget to "undraft" the pages)
1. Check that page navigation is still good, sometimes bringing in new pages requires that you go to the Article Order and Reset the Order so that pages navigate between each other properly

<sub>For smaller text</sub>

```js
   Paste your macro code here.
```

> [!NOTE]
> I want the readers to read it carefully as it contains many important docs.

> [!TIP]
> Use the command line to detect and resolve the errors!

> [!WARNING]
> DON'T DELETE THE `package.json` file!

> [!CAUTION]
> Don't execute the code without commenting the test cases.

> [!IMPORTANT]  
> Read the contribution guideline before adding a pull request.
