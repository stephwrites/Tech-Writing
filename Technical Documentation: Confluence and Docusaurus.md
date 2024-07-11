# Technical Documentation: Confluence and Docusaurus

Technical Documentation: Confluence and Docusaurus is a high-level overview and comparison of the content management solutions Confluence and Docusaurus, as well as a general guide for technical documentation best practices. Use this guide as a resource when creating documentation for your projects, products, processes, or anything that requires technical instruction. 

This guide is not a set of rules that must be strictly followed and never modified to suit varying use cases. Use your best judgment to determine what's best for your users!

# Hosting Documentation
Confluence and Docusaurus are highly regarded, industry standard content management systems used for both technical and non-technical documentation. Consider the advantages and disadvantages of each, outlined below, when deciding which is the best fit for your use case.

> [!TIP]
> **Don't reinvent the wheel!** Make sure sufficient documentation doesn't already exist for your use case, especially if you're using industry standard tools. Vendors may already have teams dedicated to writing robust documentation for their users. Take advantage of existing official documentation to either replace or supplement your available knowledgebase.

## Atlassian Confluence
[Atlassian Confluence](https://www.atlassian.com/software/confluence) is an enterprise wiki solution with a wide range of capabilities. A wiki is a set of web pages that allows collaborative editing of its content and structure by contributors. Wiki pages are contained and stored within a wiki space. Some larger documentation efforts may have their own wiki spaces, but much documentation will live in en existing wiki space for an organization within an enterprise.

Confluence is recommended for **genereal documentation** not associated with any specific project.

| The Good :+1: | The Bad :-1: |
|----------|---------|
|• **Good for general documentation not associated with any specific project** |• Lives outside associated project, resulting in less impetus to keep documentation up-to-date |
|• Widely used and understood; the "default" solution | • Limited version control |
|• Easily searchable and discoverable on most enterprise intranets | • Limited "dark mode" availability |
|• Easily editable by anyone; full rich text editor | |
|• Integration with apps like Jira, Microsoft Office, and many others | |
|• Analytics functionality available | |
|• High availability | |
|• Internal templating capabilities available | |

If your documentation effort will be large or if you want more control over the wiki space in which it resides, consider creating a new wiki space specifically for your documentation. To get started with your Confluence docs, see the [official Confluence documentation](https://confluence.atlassian.com/doc/get-started-777010817.html).

## Docusaurus
[Docusaurus](https://docusaurus.io) is a content management tool designed to make it easy for teams to publish documentation without having to worry about the infrastructure and design details. According to [Introducing Docusaurus:](https://docusaurus.io/blog/2017/12/14/introducing-docusaurus)

> At its core, all a user has to provide are documentation files written in markdown, customization of a provided home page written in React, and a few configuration modifications. Docusaurus handles the rest by providing default styles, site formatting, and simple navigation. Getting started is easy, as users can install it using `npm` or `yarn` via a simple initialization script that creates a working example website out of the box.

Docusaurus is recommended for **technical documentation** associated with a specific project.

| The Good :+1: | The Bad :-1: |
|----------|---------|
|• **Good for technical documentation associated with a sepcific project** |• May present a learning curve for non-developers or developers not familiar with markdown |
|• Cleaner, more modern look and feel | • May not be easily discoverable on enterprise intranets |
|• Includes out-of-the-box documentation features | • Not easily editable by anyone; requires merge requests |
|• Documentation can be contained within associated project | • Not ideal for non-technical documentation |
|• Release documentation updates when ready via pipeline | • Hosting via GitLab does not ensure availability |
|• Better version control | • Changes to source can be impacted by testing controls |
|• Industry standard for tech companies like Google, Facebook, and others | |
|• Advanced features like versioning, i18n, search, and theme customizations | |
|• "Dark mode" available | |

To get started with your Docusaurus docs, see the [official Docusuarus documentation](https://docusaurus.io/docs/category/getting-started).

# Formatting, Organizing, and Writing Documentation

In general, each page in your documentation should include the following:
* **Title:** What is this documentation?
* **Table of contents:** Internal navigation
* **Overview/introduction:** Context and a brief description of what users will learn or accomplish
* **Main content:** The a ctual content of the documentation—prerequisites, step-by-step instructions, code snippets, and anything else your users need to know
* **Additional info:** Related documentation, internal or external, that might be helpful for users
* **Support:** If available, support avenues such as Slack channels, email distros, or request forms

Use headings to denote new sections. If a section has many sub-sections and/or a lot of content, consider breaking it up into child pages to avoid confusion and promote readability and scannability.

Your documentation should be structured and organized in a way that makes sense to the user and can be easily (and quickly) parsed. When organizing content, ask yourself: What are the main topics that users will search for? Under each of those topics, what specific questions or instructions will they be looking for? If you were a user of this docuemntation, what organization would be most effective for your learning?

> [!TIP]
> Remember the four tenets of technical writing:
> 1. **Write like a human.** Use simple, clear language as much as possible with a friendly-neutral tone.
> 2. **Don't assume your users understand.** Your users are not you! Something that may seem obvious might not be obvious to the user. Be specific in your instructions, and write out acronyms where appropriate.
> 3. **Be concise.** Brevity is the soul of technical writing (and wit). Write as much as needed to be necessary and helpful, but not much more. Use intuitive formatting to break up large chunks of text. Utilize tables, callouts, alerts, code blocks, and other tools to organize and call attention to certain information.
> 4. **Use visuals.** When possible, visualize what you're trying to say. Use screenshots, diagrams, code snippets, and other visuals to supplement the information you present and give users another way to consume your content.

## Best Practices
Below are some additional tips and tricks that will improve your documentation quality.

### Keeping Docs Up-to-Date
The single most important best practice for documentation is ensuring it stays up-to-date. Designate team members as owners and maintainers, and schedule period content reviews. If no dedicated technical writers are available on the team after documentation creation, hold a quick training session between technical writers and owners/maintainers to ensure knowledge of editing and maintenanace practices persevere. 

## Ensuring Accessibility
Writing accessible documentation ensures _all_ users can consume your content. For documentation accessibility, keep in mind some key points:

* **Always give images alt text.** Alt text makes your images readable by screen readers and offers a default display if the images fail to render.
* **Avoid overly complicated formatting.** Screen readers have difficulty reading complicated formatting and macros, and the result is often garbled words and nonsensical sentences. If necessary, split up your content into multiple sub-pages rather than relying on complex formatting schemes.
* **Use high contrast.** Make sure your text is readable by using highly contrasting colors, such as white on black or black on white. Many free tools are availble online to test the contrast of colors.
* **Write links seamlessly into text.** Don't use "here" or "this page" for link text. Users experience links differently. Screen reader software will often jump from one link to the next without reading the text in between, for example, while other users might visually scan your documentation looking for specific links.
* **Keep it simple.** When in doubt, the simplest solution is often the best.

## Linking Correctly to Pages
When linking to _any_ page, use descriptive phrases that give context for the material you're linking. Avoid using text like "here" or "this page." Effective link text improves accessibility and scannability.

* **Example of a good link:** Check [Yale University's link usability guidance](https://usability.yale.edu/web-accessibility/articles/links) to learn more about link accessibility.
* **Example of a bad link:** [Click here](https://usability.yale.edu/web-accessibility/articles/links) to learn more about link accessibility.

When possible, always use a link generated by a web page's "Share" button instead of just copying the URL from your address bar. This ensures link lifespan in case, for example, changing a page's title also changes its URL.

## Tagging/Labeling Pages

If available, adding a label or tag to a page helps keep your documentation organized and makes it easier for users to discover. Both Confluence and Docusaurus offer built-in tagging and tagging functions.

# Key Resources & Support
For any technical documentation questions not addressed by this guide, defer to the [Microsoft Writing Style Guide](https://learn.microsoft.com/en-us/style-guide/welcome/), available in full and free online.
