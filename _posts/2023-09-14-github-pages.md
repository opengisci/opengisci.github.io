---
layout: lesson
title: Research and Publish with GitHub
purpose: "publish a website with GitHub, Jekyll, and Markdown and learn purpose and concepts for Git version control"
format: tutorial
date: 2023-09-14 13:30
term: fa23
---

## Expectations

- Publish and customize a GitHub pages site with an 'about' page
- Add at least one blog post



## Git

[Git](https://git-scm.com/) is a free and open source version control system.

Breaking down each term:
- Free: you don't have to pay.
- Open source: transparency, so no backdoors or unpleasant surprises.
- Version control: if you did something wrong, you can go back to any point in time.
  Also, you can easily collaborate with other people.

Here is a longer article motivating Git: [Why Git? Why GitHub?](https://happygitwithr.com/big-picture)

- [Git](https://git-scm.com/) can be run from a command line shell or from a simple GUI (graphical user interface), or from a third-party program.
- Software Carpentry has a free workshop, [Version Control with GIT](https://swcarpentry.github.io/git-novice/)

## GitHub

[GitHub](https://github.com) is one of many places you can host your Git repositories.

Let's take a look at [QGIS](https://github.com/qgis/QGIS), which is hosted on GitHub.
- The Code page is the home page.
  It lists the files inside the repository, and information about the repository.
- The [Issues](https://github.com/qgis/QGIS/issues) page is where people can report bugs,
  request features, or propose changes.
- The [Pull Requests](https://github.com/qgis/QGIS/pulls) page is where people have written code for QGIS,
  and are wanting to have their code reviewed and merged into the main QGIS repository.
- There are also several other pages with different functions.
  For example, the [Contributors](https://github.com/qgis/QGIS/graphs/contributors) page under "Insights"
  shows you who contributed to QGIS over time.

- [GitHub](https://github.com) is one of many services implementing Git, making it more convenient to use and providing web servers for backing up and sharing repositories.
  - [GitHub](https://github.com) is a popular platform for hosting open-source software projects, including [QGIS](https://github.com/qgis/QGIS).
  - The [GitHub](https://github.com) web application provides many of Git's editing and version control features without downloading any software.
  - GitHub also has its own [Desktop Application](https://desktop.github.com/).

### Example GitHub Repository

- QGIS code is stored in a GitHub Repository: [https://github.com/qgis/QGIS](https://github.com/qgis/QGIS)
  - including a forum for [Issues](https://github.com/qgis/QGIS/issues) like bug reports and feature requests.
  - and [pull requests](https://github.com/qgis/QGIS/pulls) containing proposed revisions to the QGIS source code
  - Issues and Pull Requests are the principle means by which the open source community contributes to the QGIS projects

## Markdown

Markdown is an easy-to-learn and very efficient language for formatting writing.
It can be used for writing webpages, blogs, books, computational notebooks, and even scientific articles.
Markdown is the language for writing issues, wikis, and readme pages on GitHub.

- GitHub has a [Markdown](https://guides.github.com/features/mastering-markdown/) language for writing and formatting everything from Readme documents to Wikis, Issues, and even webpages. Read and bookmark this guide: https://guides.github.com/features/mastering-markdown/
- Use this [markdown cheat sheet](/assets/markdown.pdf)
- Follow this [10 minute tutorial](https://commonmark.org/help/tutorial/)

Using software like [Jekyll](https://jekyllrb.com/), you can use Markdown to build websites.

## Create a GitHub Page

- [GitHub Pages](https://docs.github.com/en/pages) is a service running on GitHub that can serve websites. It can also use Jekyll to build the websites for you.

There are [two types](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages#types-of-github-pages-sites) of GitHub Pages sites.
You can have a **user** site, where the URL will look like `https://<username>.github.io`;
you can also have a **project** site, where the URL will look like `https://<username>.github.io/<repository>`.

We will be using the Jekyll theme [Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes).

Head over to [the template](https://github.com/mmistakes/mm-github-pages-starter/) and click on the green "Use this template" button.
Then, click "Create a new repository".

For "Repository name", if you want a **user** site, enter `<username>.github.io`;
if you want a **project** site, enter a name for your project, such as `geo-blog`.

Enter an optional Description, and then click on the green "Create repository" button.

If you created a **user** site, GitHub Pages should start building your website automatically.

For **project** sites, head over to "Settings" --> "Pages" on the left sidebar.
For "Source", choose "Deploy from a branch";
for "Branch", change "None" to "master" and click "Save".

The yellow dot besides your "Initial commit" indicates that GitHub is building your site.
Your site is live once the yellow dot turns into a green check mark.

To see the URL, click on the gear icon next to "About" on your repository's homepage.
Under "Website", select "Use your GitHub Pages website", and save.

## Editing your website

### From GitHub

From your repository, click on a file, say, `README.md`.

Click on the pen button to the top-right to edit the file.

On the top left, you can switch between "Edit" and "Preview" to see what the file will look like.

This method is for quick fixes - using it for file uploads or major changes is not recommended.

### From GitHub Desktop and VS Code

- In GitHub Desktop, go to File --> Options and add your account information.
- Then go to File --> Clone repository to download your repository to the local computer.
  - Pay attention to the folder to which you are cloning into.
- Edit some files and save them.
- Return to GitHub Desktop
- You should notice that GitHub has detected changes in your repository and automatically staged the changes in a list.
  Clicking on individual files shows a `diff` of the changes with deletions in red and additions in green.
- Down below, type a commit message, then `commit` the changes to the local repository.
- To sync with your online GitHub content, `push` the changes.
- Revisit or refresh your website in a browser. It may take some time for the changes you just made to be reflected online; you can check the "Actions" tab on GitHub.com for details.

[VS Code](https://code.visualstudio.com/) is a popular editor by Microsoft.
You can use it by installing on your local computer or online at <https://vscode.dev/>

After installing VS Code, you can visit the [Tips and Tricks](https://code.visualstudio.com/docs/getstarted/tips-and-tricks) page to get started.
There are also some [Intro Videos](https://code.visualstudio.com/docs/getstarted/introvideos) offered.

### Make the site your own

Let's see how to edit the site content to make it your own

- customize title, description and user names in `_config.yml`
- Return to GitHub Desktop
- You should notice that GitHub has detected changes in your repository and automatically `staged` the changes in a list. Clicking on individual files shows a `diff` of the changes with deletions in red and additions in green.
- Down below, type a commit message, then `commit` the changes to the local repository.
- To sync with your online GitHub content, `push` the changes.
- Revisit or refresh your website in a browser. It may take up to 10 to 15 minutes for the changes you just made to be reflected online.

- View online, including the GitHub Actions to render the page
- customize the `_pages/about.md` page to state the purpose of this page.
- Save, commit, and push the changes.
- notice how the `.md` files in the `_posts` folder all begin with a date in `YYYY-MM-DD-post-name.md` format. Let's leave these here for now, but add a new one along the lines of `2023-09-14-gis-science.md`

- Open the file and add header information:
```
---
title: "Is GIS a Science?"
categories:
  - Blog
tags:
  - science
  - GIS
---
```

- Then add the content of your post! I suggest adding a new sentence on every line.
- Commit the post, and then try using some different formatting techniques, including lists, tables, bold, italics and links.

### Keep images and other files in an assets folder

- Jeckyll looks to an `assets` folder for images and other content, so lets create one now.
- add an `assets` folder inside your repository's root directory
- save an image into the `assets` folder, e.g. one of the [github logos](https://github.com/logos)
- edit your page to include the image, e.g. `![GitHub Logo](/assets/GitHub-Logo.png)`

![GitHub Logo?](/assets/GitHub-Logo.png)

## Keeping work in sync between GitHub.com and local repositories

To see how GitHub works when you are editing with more than one version of a repository, lets return to github.com

- Edit your index.md file
- add or revise some of the text in a small, irrelevant way
- commit the change
- return to GitHub Desktop
- `Fetch origin`
- now your local files should be updated!
- in Github Desktop, go to the `History` of your Repository
- right-click your most recent commit and `revert changes`
- You should see that your most recent changes made on GitHub.com have been undone. This may require reloading the markdown document in Atom.
- **caution** if files are open in Atom, do not delete or rename them outside of Atom.
- **reminder** always `fetch` changes from GitHub.com before you start working locally, especially if you use multiple computers.
- **reminder** always remember to `commit` and `push` changes when you are finished working locally


- Header information in between `---` lines is [YAML Front Matter](https://jekyllrb.com/docs/front-matter/), and code inside `< >` tags is [HTML](https://developer.mozilla.org/en-US/docs/Web/HTML).



## Template Customization

Virtually every aspect of a Jekyll template can be customized.
If you want to do so, copy individual files that you want to customize from the original Jekyll repository, so that your local copy will override the template.
Alternatively, clone the entire repository to your own local version and customize from there.

## Fancier Options

You can develop a more advanced sites customized for portfolios, blogging, documentation, etc. by first forking or cloning a Jekyll template. Some of these work directly with GitHub pages (building the site remotely on GitHub's servers), while others will require installing requisite software on your own computer to build the site locally. Here are some places to start:

- Home of the [Jekyll project](https://jekyllrb.com/), with good documentation and tutorials
- A quick [magazine article](https://www.smashingmagazine.com/2014/08/build-blog-jekyll-github-pages/) introduction and start-up guide
- The [Jekyll Now](https://github.com/barryclark/jekyll-now) theme is easy to fork to start your own pages repository, and the readme contains step-by-step instructions for doing so
- [Yihui Xie's Blogdown book](https://bookdown.org/yihui/blogdown/) explains the R Blogdown / Hugo / Netlify stack for GitHub pages using RStudio and integrating visualizations and apps built in R. Bonus: it's very similar to [Bookdown](https://bookdown.org/) for creating publications with your research in R.


## Cautions with Git

- Git and GitHub are not designed to handle large files `>100mb`
- Before working, always make sure that you have `pulled` the most recent `commits`
- Once `staged` changes are `committed` together, they are bundled for purposes of `pushing` and `reverting`. In other words, to undo one of the changes, you must undo them all.
- Therefore, `commit` frequently.
- Once finished, always remember to `push` your latest commits.
