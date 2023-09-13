---
title: "Git as a Research and Publishing Tool"
---


[Git](https://git-scm.com/) is a free and open source version control system.

Breaking down each term:
- Free: you don't have to pay.
- Open source: transparency, so no backdoors or unpleasant surprises.
- Version control: if you did something wrong, you can go back to any point in time.
  Also, you can easily collaborate with other people.

Here is a longer article motivating Git: [Why Git? Why GitHub?](https://happygitwithr.com/big-picture)

You can run Git from a command line shell, or from a third-party program.

Here are some Git tutorials and learning material:
- [Git cheat sheet](https://education.github.com/git-cheat-sheet-education.pdf) by GitHub
- [GitHub cheat sheet](https://training.github.com/downloads/github-git-cheat-sheet.pdf)
- [Version Control with Git](https://swcarpentry.github.io/git-novice/) by Software Carpentry
- [gittutorial - A tutorial introduction to Git](https://git-scm.com/docs/gittutorial) from Git's homepage
- [Hello World - GitHub Docs](https://docs.github.com/en/get-started/quickstart/hello-world) by GitHub
- [Happy Git and GitHub for the useR](https://happygitwithr.com/) from the STAT 545 course at UBC.

Note: these tutorials may cover advanced topics like branching, stashing, rebase, diffs, and refs,
but you really only need to learn a handful of basic concepts.

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

### GitHub Pages

[Markdown](https://commonmark.org/help/) is an easy-to-read, easy-to-write syntax for formatting plain text.

A lot of what happens in GitHub is formatted in Markdown: Issues, Pull Requests, Wikis, et cetera.

Here are some Markdown tutorials:
- [10 Minute Markdown Tutorial](https://commonmark.org/help/tutorial/) from Commonmark.org
- [Basic writing and formatting syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) for GitHub.
- You can also search for "Markdown cheat sheet" on the Internet.

Using software like [Jekyll](https://jekyllrb.com/), you can use Markdown to build websites.

[GitHub Pages](https://docs.github.com/en/pages) is one place to host such websites.
It comes with Jekyll support, so you don't have to install Ruby, RubyGems, GCC and Make,
which is what you'll usually need to use Jekyll.

# Hands-on Tutorial

You are free to use any of the alternatives listed [below](#alternatives), but you’ll be "on your own" in terms of getting things up and running.

## Creating your website

First, create an account on [GitHub](https://github.com) if you do not have one already.

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

To customize the Minimal Mistakes themes, check out their [Configuration](https://mmistakes.github.io/minimal-mistakes/docs/configuration/) page.

Spend some time customizing the theme.
Play around with `_config.yml`.
View the existing posts, or create a new one.

### Edit files online

To edit Markdown and other files, you will need a text editor.

Luckily, as we are creating a website and not running any code.
Therefore, we have a lot of options here.

#### `vscode.dev`

Use the Visual Studio Code editor, right from your browser.

Using `vscode.dev` online is very similar to using VS Code on your computer - you can [change the theme](https://code.visualstudio.com/docs/getstarted/themes) or [sync settings across devices](https://code.visualstudio.com/docs/editor/settings-sync) as usual.

However, with `vscode.dev`, you do not have to install software, or set up Git.

To get started, head over to <https://vscode.dev/>.

1. Click on "Open Repository...", and then "Open Repository from GitHub".
2. Click "Allow" and sign in with GitHub.
3. Repeat step 1, and choose the repository for your website.
4. You should now see a preview of `README.md` for that repository.
5. Click on "Restricted Mode" on the bottom-left corner.

##### Command Palette

VS Code has a lot of commands.
Fortunately, you do not have to memorize where things are;
the [Command Palette](https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette)
gives you access to all VS Code commands.

Use the Shift+Command+P (Mac) / Ctrl+Shift+P (Windows/Linux) shortcut to open the command palette.

Then, type to search for the command you are looking for.
For example, to **preview** the current markdown file, type "markdown" and choose "Markdown: Open Preview".

Because this command has a keyboard shortcut, you will see Shift+Command+V (Mac) / Ctrl+Shift+V (Windows/Linux) displayed here.

Try going back to the `.md` file and opening the Command Palette again.
Your most recent commands are remembered, so you can simply hit Enter to execute.

##### Push to GitHub

To upload your changes to GitHub:

1. Open a Markdown file and make some edits. Changes are saved automatically.
2. Click on the third icon on the left (Source Control).
3. Hover over the file(s) you have changed, and click on the plus sign to stage changes.
  This is equivalent to `git add`.
  You can also add everything by hovering over "Changes" and clicking on the plus sign there.
4. Type a commit message in the "Message" box.
5. Click on "Commit & Push".

#### From GitHub

From your repository, click on a file, say, `README.md`.

Click on the pen button to the top-right to edit the file.

On the top left, you can switch between "Edit" and "Preview" to see what the file will look like.

This method is for quick fixes - using it for file uploads or major changes is not recommended.

### Edit files locally

Install Git from <https://git-scm.com/downloads>.

Install [GitHub Desktop](https://desktop.github.com/) and login.

#### RStudio

RStudio comes with a "visual" editing mode.

To use it, open a `.md` file, and choose "Visual" on the top left.

Note that RStudio will reformat your `.md` file, making this process somewhat irreversible.

#### Visual Studio Code

[VS Code](https://code.visualstudio.com/) is a popular editor by Microsoft.
As mentioned above, you can also use VS Code directly from your browser.

After installing VS Code, you can visit the [Tips and Tricks](https://code.visualstudio.com/docs/getstarted/tips-and-tricks) page to get started.
There are also some [Intro Videos](https://code.visualstudio.com/docs/getstarted/introvideos) offered.

Refer to the [Command Palette](#command-palette) section above for how to access commands quickly.

##### VS Code and Git

Visit [this guide](https://code.visualstudio.com/docs/sourcecontrol/intro-to-git) to set up Git in VS Code.

To upload your changes to GitHub, you can use GitHub Desktop, or follow these steps:

1. Click on the third icon on the left (Source Control) to check that you have opened a Git folder.
2. Open a Markdown file, make some edits, and save the file.
3. Click on the third icon on the left (Source Control).
4. Hover over the file(s) you have changed, and click on the plus sign to stage changes.
  This is equivalent to `git add`.
  You can also add everything by hovering over "Changes" and clicking on the plus sign there.
5. Type a commit message in the "Message" box.
6. Click on "Commit".
7. Click on "Sync Changes".

#### GitHub Desktop

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

## Alternatives

These are listed in no particular order.

Git: not really, please just use Git.

GitHub & GitHub Pages:
- [GitLab Pages](https://docs.gitlab.com/ee/user/project/pages/)
- [BitBucket Pages](https://support.atlassian.com/bitbucket-cloud/docs/publishing-a-website-on-bitbucket-cloud/)

Visual Studio Code:
- [RStudio](https://posit.co/download/rstudio-desktop/) (Windows, MacOS, Linux)
- [Atom](https://github.com/atom/atom) (Windows, MacOS, Linux)
- [Sublime Text](https://www.sublimetext.com/) ($99, Windows, MacOS, Linux)
- and many more.

`vscode.dev`: GitHub [Codespaces](https://github.com/features/codespaces) (paid with a free tier)

GitHub Desktop: the Git website has a list of [GUI Clients](https://git-scm.com/downloads/guis/) by platform.
You can also learn to use Git via the command line.

Jekyll:
- Hugo
- Quarto
- Typecho
- MkDocs

Minimal Mistakes: GitHub Pages supports some [built-in themes](https://pages.github.com/themes/).
The documentation can be found here: [Adding a theme to your GitHub Pages site using Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/adding-a-theme-to-your-github-pages-site-using-jekyll).

## Tips

- Always `fetch` and `pull` changes before you start working locally.
  This can help you avoid merges, conflicts, and other advanced topics in Git.
- `commit` frequently.
  Use informative commit messages.
  Remember to `push` your changes.
- Visit the [Jekyll](https://jekyllrb.com/) homepage for documentation and tutorials
- If you have files larger than 50 MiB, read this guide: [About large files on GitHub](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-large-files-on-github).
  GitHub will warn you about files larger than 50 MiB, and reject files larger than 100 MiB.
