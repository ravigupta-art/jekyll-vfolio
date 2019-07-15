---
layout: post
title: Getting started with Jekyll-Vfolio
summary: Learn how to use Jekyll-Vfolio theme and modify it as per your needs.
---

<br>
## Installing for local development

1. Install Jekyll on your machine. You can install Jekyll using this guide: [https://jekyllrb.com/docs/installation/](https://jekyllrb.com/docs/installation/)
2. Download the master branch from the repository. ( If you downloaded a zip file, unzip it first. )
3. Go to the root of the project and open '`_config.yml`' in a text editor. Make necessary changes to the file. You may use the hints in the comments or follow the documentation at [jekyllrb.com](https://jekyllrb.com). _Note: After any changes we make to this file, we need to build the site again using the command`'jekyll serve'`._
4. If you followed up the Jekyll installation using the guide in step 1, you can build up the site for first time using the command `bundle exec jekyll serve` in terminal.
5. The site would be available at `http://127.0.0.1:4000`

## Setting up jekyll-vfolio on GitHub pages to host your site.
1. If you don't have a GitHub account, create one.
2. Fork this repository and create a branch named gh-pages, then start editing the `_config.yml` file. Delete the `README.md` and `favicon.ico` files. You may add your own `favicon.ico` file as well.
3. To start learning about the GitHub Pages you may visit our simple '[Hello-World](/2019/07/03/hello-world-github-pages.html)' tutorial.

### Setting up the Homepage
- `index.md` file is the one which is use to serve the Homepage.
- The `index.md` files has HTML snippet with `Liquid Syntax` which calls in data from the `'_data/index.yml'` file.
- Use the `'_data/index.yml'` file to make the changes.

### Setting up the Film Reel pages
- Use `'_data/film-reel.yml'`
- Similarly find the appropriate files under `'_data'` folder to make changes to the 'fiction-films' and 'non-fiction-films' pages.

### Navigation
`'_data/film-reel.yml'` file translates for the navigation on the site.

### Banner
Text on the banner can be changed from `'_includes/banner.html'` file. Make necessary changes under `<h1>` and `<p>` tags.

### News pages
News page is written in Markdown syntax ( except the line with `<h1>` tag, this tag controls the title for this page ). To learn more about the markdown syntax follow this guide: [https://www.markdownguide.org/basic-syntax](https://www.markdownguide.org/basic-syntax)
> **Note**: _The same guide can be used to edit or create the blog posts under `_posts` folder._

### Awards & Recognition page
Use the `'awards-and-recognition.md'` file to make changes to Awards & Recognition page. Markdown syntax is used here.

### Contact page
The `'contact.md'`file controls the contact page. Find the following code in file and make changes accordingly:
```
<h1 class="text-title text-center">CONTACT</h1>
<p class="text-center">If you have a project to develop or have any question you would like to ask me, feel free to get in touch.</p>
<p class="text-center">Please, contact me at <a href="mailto:maildesk.ravi@gmail.com">maildesk.ravi@gmail.com</a></p>
<img class="img-fluid center-block" src="/img/paperplane.png" aria-hidden="true" alt="">
```

[ << back to all posts](/blog)
