---
layout: lesson
title: Research and Publish with GitHub
purpose: "learn fundamentals of Git version control and publish a website using Markdown, GitHub, and Jekyll"
format: tutorial
term: sp25
---

Thanks to [Yifei Luo](https://hegsrr.github.io/people/yifei-luo/) for contributions to this lesson.

## Expectations

- Publish and customize a GitHub pages site with an 'about' page
- Add at least one blog post

## Git

[Git](https://git-scm.com/) is a free and open source version control system for a repositories.

- Free: you don't have to pay.
- Open source: transparency, so no backdoors or unpleasant surprises.
- Version control: if you did something wrong, you can go back to any point in time.
  Also, you can easily collaborate with other people.
- Repository: Git is designed to keep track of all of the changes for an entire project rather than just one file. A Git repository is folder containing all of the files for a given project. It may contain subfolders for organization within the project and a `.gitignore` file instructing Git not to track changes in specified parts of the repository.

[Git](https://git-scm.com/) can be run from a command line shell or from a simple GUI (graphical user interface), or from a third-party program.
In this course, we will primarily use GitHub's website <https://github.com> and [GitHub Desktop](https://desktop.github.com/) application.

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

## Create a GitHub Account

- Please create a [GitHub](https://github.com/)
- *Remember your email & password*
- Send the account name to your professor

### Key Git and GitHub Actions

- `Clone`: Download a repository (yours or someone else's) to a local computer
- `Commit`: Save a batch of changes to your repository, including a brief message and description
- `Revert`: Roll back a commit
- `Push`: Upload one or more commits from the local computer to the GitHub servers
- `Fetch origin`: Check whether there are new commits on the GitHub server for this repository
- `Pull`: Download one or more commits from the GitHub servers to your local computer and merge them into your repository. Or, if you have forked a repository and the original repository has continued to commit revisions, `pull` the revisions from the original version into your own forked version. An example case of this: you fork a repository with a course assignment and the professor subsequently makes a last-minute revision to the assignment. Just pull the changes into your own version!
- `Fork`: Make a copy of a repository (yours or someone else's) in your own online GitHub account. This copy may maintain association with the original repository.
- `Pull Request`: Send suggested commits from your own forked version of a repository to the original repository owner. An example case of this: you fork a version of an open source GIS plugin, fix some errors or make some improvements, and send suggested revisions back to the plugin developer.

### Example GitHub Repository

- QGIS code is stored in a GitHub Repository: [https://github.com/qgis/QGIS](https://github.com/qgis/QGIS)
  - including a forum for [Issues](https://github.com/qgis/QGIS/issues) like bug reports and feature requests.
  - and [pull requests](https://github.com/qgis/QGIS/pulls) containing proposed revisions to the QGIS source code
  - Issues and Pull Requests are the principle means by which the open source community contributes to the QGIS projects

## Markdown

Markdown is an easy-to-learn and very efficient language for formatting writing.
It can be used for writing webpages, blogs, books, computational notebooks, and even scientific articles.
Markdown is the language for writing issues, wikis, and readme pages on GitHub.

- GitHub has a [Markdown](https://guides.github.com/features/mastering-markdown/) language for writing and formatting everything from Readme documents to Wikis, Issues, and even webpages.
- Use this [markdown cheat sheet](/assets/markdown.pdf)
- Follow this [10 minute tutorial](https://commonmark.org/help/tutorial/)
- Guide to [Writing on GitHub](https://guides.github.com/features/mastering-markdown/)

You can use Markdown to author website content using software like [Jekyll](https://jekyllrb.com/).

## Create a GitHub Page

- [GitHub Pages](https://docs.github.com/en/pages) is a service running on GitHub that can serve websites. It can also use Jekyll to build the websites for you.

There are [two types](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages#types-of-github-pages-sites) of GitHub Pages sites.
You can have a **user** site, where the URL will look like `https://<username>.github.io`;
you can also have a **project** site, where the URL will look like `https://<username>.github.io/<repository>`.
In this course, we will create a **user** site.

We will start with the Jekyll theme [Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes), as a simple but highly customizable theme.
See documentation and examples [here](https://mmistakes.github.io/minimal-mistakes/).
Feel free to research and apply other themes on your own.

### Create your site

- Go to the [starter template](https://github.com/mmistakes/mm-github-pages-starter/)
- Use the green "Use this template" button to "Create a new repository".
- Set the `Repository name` to `<username>.github.io`. For example, if your GitHub user name is `josephholler`, the repository name should be `josephholler.github.io`
- Enter a short Description
- Click on the green "Create repository" button.
- If you created a **user** site, GitHub Pages should start building your website automatically.
- Go to the `Actions` tab of the site repository, and you should see a `pages build and deployment` action. A yellow dot indicates that GitHub is building your site, and a green check mark indicates that GitHub has finished and the site is ready to view.
- The site URL is the same as the repository name for a user site, e.g. `https://josephholler.github.io`
- *If* you are building a **project** site:
  - go to the repository "Settings" --> "Pages" menu
  - for "Source", choose "Deploy from a branch"
  - for "Branch", change "None" to "master" and click "Save"
  - To see the URL, click on the gear icon next to "About" on your repository's homepage
  - Under "Website", select "Use your GitHub Pages website", and save

### Edit your site online

You can make simple revisions to your site on GitHub.com.

- From your repository webpage, find the `_pages/about.md` file
- Click on the pen button to the top-right to edit the file.
- On the top left, you can switch between "Edit" and "Preview" to see what the file will look like.
- The first four lines are header information. Leave these as-is.
- Edit the content briefly to introduce yourself and the website.
- `Commit` the changes with the green button, providing a message and description of the change.
- Notice a new `Action` is triggered to rebuild your site every time you commit new changes.
- Once the site rebuild is complete, view the changes in a web browser. You may need to force your web browser to refresh (commonly the `F5` key) in order to see the changes.

### Edit your site locally

I suggest making more substantial revisions to your site on a local computer.

- Open the GitHub Desktop application.
- Go to File --> Options and log into your GitHub account.
- Then go to File --> Clone repository to download your repository to the local computer.
  - Pay attention to the folder to which you are cloning into.
- Open the [Visual Studio Code](https://code.visualstudio.com/) application
- Open the root folder of your website repository using the explorer (pages) icon at top left. You can trust yourself as the author.
- open the `about.md` file again
- Try the `preview` button (split window with magnifying glass) at the top right for quick previews of your markdown code. This preview does not render *exactly* the same way as Jekyll / GitHub sites, but it's close and saves a lot of trial-and-error time waiting for sites to build.
- Try making some more edits to the `about.md`.
- Try adding a table. Notice the empty line before and after the table, vertical bars for separating columns, first row for column headers, second row for indicating alignment with dashes and colons, and one row for each row of the table. There is an empty space between two bars for an empty cell.

```markdown

| First Column | Second Column | Last Column |
| :----------- | :-----------: | ----------: |
| left | centered | right |
| empty middle | | empty middle |

```

| First Column | Second Column | Last Column |
| :----------- | :-----------: | ----------: |
| left | centered | right |
| empty middle | | empty middle |

- Return to GitHub Desktop
- You should notice that GitHub has automatically detected changes in your repository and `staged` the changes in a list.
- Clicking on individual files shows a `diff` of the changes with deletions in red and additions in green.
- Down below, type a commit message, then `commit` the changes to the local repository.
- To upload the changes to GitHub online, `push` the changes.
- Check your repository `Actions` and when the build is finished, view your website in a web browser.

### Customize your site

Let's see how to edit the site content to make it your own.

- Open the `_config.yml`. This file is [YAML](https://yaml.org/) code consisting of easily readable `keys` followed by a colon and a `value` or a list of values denoted by dashes. Long values or lists are indented to indicate that they are part of the preceding key.
- Edit the title, email, description, and user names.
- Edit the `author` information, which has subkeys for `name`, `avatar` photo, `bio`, and `links` to websites and social media sites. You can delete the information for sites you do not use or add information for more sites. You can update the avatar photo by replacing the existing image file. Link `icons` are from [font awesome](https://fontawesome.com/)
- You may edit the `skin` by changing from `default` to any from [this list](https://mmistakes.github.io/minimal-mistakes/docs/configuration/#skin). Include the double quotes.
- `Save`, `commit`, and `push` the `changes`

### Create a new post

- Notice how the `.md` files in the `_posts` folder all begin with a date in `YYYY-MM-DD-post-name.md` format. Let's leave these here for now, but add a new one along the lines of `2023-09-14-gis-science.md`
- Open the file and add header information (YAML-style) as follows. You may change the `title` or `tags`, but use the same category of capitalized "Blog"

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

- Add the content of your post below the header information.
- Place each new sentence on a new line, and leave and empty line in between paragraphs. This way, Git can track and visualize your changes on a sentence basis, rather than a paragraph basis.
- Commit the post, and then try using some different formatting techniques, including lists, tables, bold, italics and links.
- Try linking to other posts. The convention in the Minimal Mistakes starter template is `/category/title/`. A link to the post `2023-09-14-gis-science.md` with the category `Blog` should be `[link](/Blog/gis-science/)`

### Save images and other files in an assets folder

Jekyll looks to an `assets` folder for images and other content, so lets create one now.

- Save an image into the `assets/images` folder, e.g. one of the [github logos](https://github.com/logos)
- Edit your page to include the image, e.g. `![GitHub Logo](/assets/images/GitHub-Logo.png)`

![GitHub Logo](/assets/images/GitHub-Logo.png)

## Keeping work in sync between GitHub.com and local repositories

To see how GitHub works when you are editing with more than one version of a repository, lets return to github.com

- Edit your `about.md` file
- add or revise some of the text in a small, irrelevant way
- commit the change
- return to GitHub Desktop
- `Fetch origin`
- now your local files should be updated!
- in Github Desktop, go to the `History` of your Repository to see the `commit` and visualize it's `diff`
- Now try deleting a bunch of the irrelevant default posts
- GitHub Desktop will detect the deletions, and you can `commit` it.
- Right-click that most recent commit and `revert changes`
- You should see the deleted posts reappear!
- **caution** if files are open in Visual Studio, do not delete or rename them outside of Visual Studio.
- **reminder** always `fetch` changes from GitHub.com before you start working locally, especially if you use multiple computers.
- **reminder** always remember to `commit` and `push` changes when you are finished working locally

## Cautions with Git

- Git and GitHub are not designed to handle large files `>100mb`
- Before working, always make sure that you have `pulled` the most recent `commits`
- Once `staged` changes are `committed` together, they are bundled for purposes of `pushing` and `reverting`. In other words, to undo one of the changes, you must undo them all.
- Therefore, `commit` frequently, in small packets of changes.
- Once finished, always remember to `push` your latest commits.

## Further Learning

#### Workshops and learning resources

- Software Carpentry Workshop [Version Control with GIT](https://swcarpentry.github.io/git-novice/)
- GitHub [learning resources](https://docs.github.com/en/get-started/quickstart/git-and-github-learning-resources)
- Visual Studio Code [Tips and Tricks](https://code.visualstudio.com/docs/getstarted/tips-and-tricks) and [Intro Videos](https://code.visualstudio.com/docs/getstarted/introvideos).

#### Readings on Git

- [Why Git? Why GitHub?](https://happygitwithr.com/big-picture)
- Bryan, J. (2018). Excuse Me, Do You Have a Moment to Talk About Version Control? *American Statistician*, *72*(1), 20–27. <https://doi.org/10.1080/00031305.2017.1399928>
- Beckman, M. D., Çetinkaya-Rundel, M., Horton, N. J., Rundel, C. W., Sullivan, A. J., &#38; Tackett, - M. (2021). Implementing Version Control With Git and GitHub as a Learning Objective in Statistics and Data Science Courses. *Journal of Statistics and Data Science Education*, *29*(S1), S132–S144. <https://doi.org/10.1080/10691898.2020.1848485>

#### Customizing Jekyll Sites

You can develop a more advanced Jekyll sites customized for portfolios, blogging, documentation, etc. by first forking or cloning a Jekyll template.
Some of these work directly with GitHub pages (building the site remotely on GitHub's servers), while others will require installing requisite software on your own computer to build the site locally.
Nearly every aspect of a Jekyll site is customizable by downloading the relevant files from the theme's GitHub repository into your own site's repository and modifying them.

Here are some places to start:

- Home of the [Jekyll project](https://jekyllrb.com/), with good documentation and tutorials
- More information on the [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) theme.
- A quick [magazine article](https://www.smashingmagazine.com/2014/08/build-blog-jekyll-github-pages/) introduction and start-up guide
- The [Jekyll Now](https://github.com/barryclark/jekyll-now) theme is easy to fork to start your own pages repository, and the readme contains step-by-step instructions for doing so
- [Yihui Xie's Blogdown book](https://bookdown.org/yihui/blogdown/) explains the R Blogdown / Hugo / Netlify stack for GitHub pages using RStudio and integrating visualizations and apps built in R. Bonus: it's very similar to [Bookdown](https://bookdown.org/) for creating print and online books.
