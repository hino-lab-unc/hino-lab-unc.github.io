# Hino Lab Website

Welcome! This is a simple guide for updating our [Quarto](https://quarto.org/) website. You can clone, edit, and publish your updates with just a few steps.

## Prerequisites

1. [Git](https://git-scm.com/) installed on your machine.
2. An integrated development evironment (IDE) to code in.
   - [Positron](https://positron.posit.co/) is highly recommended.
   - [VS Code](https://code.visualstudio.com/) is similar but lacks R and Python data science tools.
3. Some familiarity with version management with Git and Quarto notebooks (`.qmd` files) will help!
   - [Basic Git tutorial docs](https://git-scm.com/docs/gittutorial)
   - [Interactive Git tutorial game](https://learngitbranching.js.org/)
   - [Quarto tutorial](https://quarto.org/docs/get-started/hello/positron.html)

## How to make updates

1. Clone this repo to your local machine.
2. Create a new issue and/or branch for your changes off `main`.
      - Issues can be created in [GitHub](https://docs.github.com/en/issues/tracking-your-work-with-issues/learning-about-issues/quickstart) or Positron/VS Code. Positron/VS Code will [automatically create a branch](https://code.visualstudio.com/docs/sourcecontrol/github#_working-on-issues) when you "start working" on an issue.
      - Branches can be created with an IDE or via the terminal: 
         - `git branch <branch-name>`
         - `git checkout <branch-name>`
3. [Commit edits](https://code.visualstudio.com/docs/sourcecontrol/staging-commits) to your branch.
      - More specific instructions on how to update website components are below.
4. Confirm your edits appear and work correctly by [rendering and previewing](https://quarto.org/docs/websites/#website-preview) each `.qmd` file you've modified.
      - In Positron, click "Preview" at the top left of the editor.
      - In terminal: `quarto preview path/to/modified.qmd`
5. Push your branch to the remote repo with an IDE or via the terminal: `git push`
6. Open a pull request to merge your changes into the `main` branch for deployment via [GitHub](https://docs.github.com/en/pull-requests/get-started/pull-request-quickstart#open-your-pull-request) or [Positron/VS Code](https://code.visualstudio.com/docs/sourcecontrol/github#_creating-pull-requests).


## How to add or update specific website components

### Lab member profile

Profiles are stored in `.yml` files in the `people/` folder. There is one `.yml` file for each role, e.g., `grad-student.yml`.

1. Open the `.yml` file corresponding to your role.
2. Add a new block of YAML to create a new profile, or find your existing profile block.
   - To create a new block, it's recommend to copy and paste an existing block and then update it.
3. Add profile images to the `files/people/` folder. Make sure the `image` path in your YAML block matches.

#### `people/*.yml` attributes

|Attribute|Description|Example|Required?|
|---|-------------------|---|---|
|`title`|First and last name|`"James Collins"`|Yes|
|`lastname`|Last name (for sorting)|`"Collins"`|Yes|
|`subtitle`|"Job" title|`"PhD Candidate"`|Yes|
|`image`|Path to profile photo|`"files/profiles/collins.jpg"`|Yes|
|`started`|Year started with lab|"2023"|No (alumni only)|
|`ended`|Year ended with lab|"2028"|No (alumni only)|
|`projects`|List of standard project names to affiliate with|`[Sunny Day, Carolinas RISA]`|No|
|`website`|Personal website URL|`https://jpcollins.me/`|No|
|`scholar`|Google Scholar profile URL|`https://scholar.google.com/ citations?hl=en&pli=1&user=n5r6I98AAAAJ`|No|
|`linkedin`|LinkedIn profile URL|`https://www.linkedin.com/ in/jamespcollins`|No|
|`orcid`|ORCID profile URL|`https://orcid.org/ 0000-0001-5751-9733`|No|
|`github`|GitHub profile URL|`http://github.com/ jamespcollins`|No|
|`bluesky`|Bluesky profile URL|`https://bsky.app/ profile/jpcollins.me`|No|
|`imagecredit`|Profile photo credit|`"Jess Abel"`|No|
|`description`|Bio text content. Can use HTML for multiple paragraphs (`<p>`) and links (`<a>`). Use the pipe `|` to enter multiple lines.||No|


### News item

News items are stored in the `news/` folder. A news items is either:

- a `*.qmd` file within that folder, e.g., `some-news-story.qmd` or
- an `index.qmd` file within arbitrarily titled subfolders, e.g., `news/some-news-story/index.qmd`.
   - The advantage of a subfolder is it can also store other images and media that accompany the `index.qmd` file.

TODO: finish how-to

### Publication

TODO: finish how-to

### Project

TODO: finish how-to

### Navigation bar or basic site details

Edit the the `_quarto.yml` file to configure the site’s basic settings.

TODO: finish how-to

## Need help?

The website czar as of July 2026 is [James](mailto:jpco@unc.edu)