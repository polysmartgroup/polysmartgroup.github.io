# [TL;DR] Two steps to edit and update the website

- Step 1: Edit the content;
- Step 2: Commit and push.

> The website will be updated automatically by the GitHub Actions.
> - It will take a 3-5 minutes to see the changes on the website.
> - The process can be checked in the Actions tab of the repository.
> - The website is updated successfully as long as the `pages-build-deployment` job is marked with a green check. You can ignore the error message in the `Prettier code formatter` and `Check for broken links` jobs.

Website url: [https://polysmartgroup.github.io/](https://polysmartgroup.github.io/)

# How to edit the content?

Note:
1. To include images, please put the images file (e.g., `icon.png`) to the `assets/img` folder, then just use the file name `icon.png` in the markdown file (e.g., `icon: icon.png` in `_config.yml` file).
2. Keep changes in the default `master` Branches, NO need to switch to `gh-pages` (this will be updated by the GitHub Actions automatically).

## 1. To edit the basic configuration of the website

- Edit the `_config.yml` file.
- Such as `title`, `email`, `description`, `icon`, etc.

## 2. To add news

1. Add a new Markdown file in the [\_news](_news/) directory, such as `this-is-a-news.md`.
2. Two types of news: **inline news** and **news with a link**. 
   - **inline news** are displayed directly in the about page (set `inline: true`).
   - **news with a link** take you to a new page (set `inline: false`);

3. The easiest way to create yours is to copy an existing news in the [\_news](_news/) directory and modify it.

## 3. To add blog posts

1. Add a new Markdown file in the [\_posts](_posts/) directory, and the [name of the file must follow](https://jekyllrb.com/docs/posts/#creating-posts) the format `YYYY-MM-DD-title.md`, such as `2024-06-13-introducing-the-homepage-of-polysmart.md`.
2. The easiest way to do this is to copy an existing blog post and modify it, check all example blog posts [here](https://github.com/alshedivat/al-folio/tree/master/_posts).

## 4. To add publications

1. create a new entry in the [\_bibliography/papers.bib](_bibliography/papers.bib) file. 
   - You can find the BibTeX entry of a publication in Google Scholar by clicking on the quotation marks below the publication title, then clicking on "BibTeX", or also in the conference page itself.
2. You can add extra information to a publication, like a PDF file in the `assets/pdfs/` directory and add the path to the PDF file in the BibTeX entry with the `pdf` field. Some of the supported fields are: `abstract`, `altmetric`, `arxiv`, `bibtex_show`, `blog`, `code`, `dimensions`, `doi`, `eprint`, `html`, `paper`, `isbn`, `pdf`, `pmid`, `poster`, `slides`, `supp`, `video`, and `website`.

## 5. To add projects

1. create new projects by adding new Markdown files in the [\_projects](_projects/) directory, such as `this-is-a-project.md`.
2. The easiest way to do this is to copy an existing project and modify it, check all example projects [here](https://github.com/alshedivat/al-folio/tree/master/_projects).

## 6. To add people

1. modify the `_pages/profiles.md` file.
2. Follow the instructions (`Usage example`) in the file to add a new person.

## 7. To add teaching

1. modify the `_pages/teaching.md` file.
