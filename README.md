# Easy-Blog-Setup

This repository and initial instructions are modified from a [repo by Chad Baldwin](https://chadbaldwin.net/2021/03/14/how-to-build-a-sql-blog.html)

**Git** - a version control software  

**Github** - an online platform for hosting and collaborating on git repositories (basically folders with files you want to keep track of)

Requirements:
- Github account
- Basic understanding of Markdown syntax (or you can use HTML if you know that)
    - [R Markdown reference guide](https://www.rstudio.com/wp-content/uploads/2015/03/rmarkdown-reference.pdf?_ga=2.243129861.649238065.1666362515-276851843.1648675901)
    - Blog uses [github's markdown syntax](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) which is pretty similar
- (Optional) Use of R Markdown via RStudio
- (Optional) Connecting github with RStudio
    - [Install git](https://happygitwithr.com/install-git.html)
    - [Configure your computer with your git account](https://happygitwithr.com/hello-git.html)
    - The first time you create a repository in RStudio from version control and try to push up the changes you make, it should prompt you to log-in via a browser, setting up the rest of what you need.  If not there is much more information [here](https://happygitwithr.com/rstudio-git-github.html)


## Steps

1. Get an account on github.com (your blog site will end up having a URL of https://username.github.io)
2. Fork this repo by clicking on the "Fork" button in the top right of the page
    + This copies this repo to your account.
    + Rename the repo to {Your GitHub username}.github.io (without the {})
    + Make sure the repo is set to public
3. Edit the `index.md` file with a blurb about yourself/your blog/or whatever you want people to see when they land on your page.
    + This page uses markdown, so you can add all sorts of things!
4. Edit the `_config.yml` file with your information (shows at the bottom of each page)
5. (Option 1) Add posts in the `_posts` folder.
6. (Option 2) If you have RStudio and github connected, you can render any .Rmd file to your blog (so it will include R output!!)
    + Works with python code chunks, SQL, etc.
    + Open RStudio: 
        - File --> New Project 
        - Choose from Version Control
        - Choose Git
        - Paste in the repo info (green button on right side of main repo page gives you an easy way to copy it)
        - Choose folder to save your repo and create it
    + Create a new .Rmd file in the `_Rmd` folder (see the example file in that folder).
        + Note that the output type is `github_document`
        + The code `knitr::opts_chunk$set(fig.path = "../img/")` in the setup code chunk
        + The render code in the top code chunk should be run in the console
    + Push the changes up to github
        + Can use git tab in RStudio
        + Or command line/terminal  
             + git add -A
             + git commit -m "Message about the commit"
             + git push
