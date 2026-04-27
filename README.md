# Sabia Website

A shared academic website for the **Sabia research group** — a team working at Chalmers University of Technology and the University of Gothenburg.

This repository contains the source code for our group website, built using **Jekyll** and the **al-folio template**. It serves as a central place to present our work: projects, member profiles, and blog posts. Think of it as our digital front door — a place to communicate what we do and document what we learn.

---

## Structure

```
sabia-website/
├── _pages/           # main website pages (About, Publications, Blog, etc.)
├── _posts/           # blog posts
├── _projects/        # research project pages
├── _bibliography/    # publication data (BibTeX)
├── assets/           # images and static files
├── _layouts/         # page templates (do not modify unless needed)
├── _includes/        # reusable UI components
├── _sass/            # styling (CSS)
├── _data/            # structured data files
├── _plugins/         # custom Jekyll plugins
├── _scripts/         # helper scripts
├── _news/            # news posts on the main page
├── _teachings/       # teaching content (currently not displayed)
├── .github/          # script to deploy the website
├── _config.yml       # main configuration file
├── Gemfile           # Ruby dependencies
└── Gemfile.lock      # dependency lockfile
```

We keep one concept per folder and try to use clear, descriptive filenames. Most contributors will only interact with `_pages`, `_posts`, `_projects`, and `_bibliography`.

---

## Repository Structure (Detailed)

### Core Content

#### `_pages/`

Contains the **main pages of the website**.

Examples:

* `about.md` → homepage
* `publications.md`
* `projects.md`
* `profiles.md`
* `blog.md`

Each file defines a page in the navigation bar. Currently `teaching.md` is not displayed in the navigation bar.

---

#### `_posts/`

Contains **blog posts**.

Each post follows:

```
YYYY-MM-DD-title.md
```

Example:

```
2026-03-10-my-first-post.md
```

---

#### `_projects/`

Contains pages describing **research projects**.

---

#### `_bibliography/`

Stores **publications in BibTeX format**.

Example:

```
papers.bib
```

---

#### `_data/`

Stores structured data used across the site.

---

### Website Templates

#### `_layouts/`

Defines page templates. Usually no edits needed.

---

#### `_includes/`

Reusable UI components like navbar and footer.

---

#### `_sass/`

Controls styling (colors, layout, fonts).

---

### Supporting Files

#### `assets/`

Images, icons, and other static files.

---

#### `_plugins/`

Custom Jekyll plugins.

---

#### `_scripts/`

Helper scripts.

---

#### `_news/`

Short updates on the main page.

---

#### `_teachings/`

Teaching-related content.

---

### Configuration Files

#### `_config.yml`

Main configuration file controlling the site.

---

#### `Gemfile`

Lists dependencies.

---

#### `Gemfile.lock`

Auto-generated dependency lockfile.

---

#### `.gitignore`

Files ignored by Git.

---

## Contributing

There are two main ways to contribute:

1. Add your **profile**
2. Write **blog posts**

---

## Adding Your Profile

### Step 1 — Create a file

Go to:

```
_pages/
```

Create:

```
about_yourname.md
```

Example:

```
about_francisco.md
```

---

### Step 2 — Add header

```markdown
---
layout: page
title: Your Name
permalink: /about/yourname/
nav: false
---
```

---

### Step 3 — Write your content

```markdown
## About Me

A short introduction about you
- Topic 1
- Topic 2
```

---

### Step 4 — Add image

Place image in:

```
assets/img/yourname.jpg
```

---

## Writing a Blog Post

### Step 1 — Create file

```
_posts/YYYY-MM-DD-title.md
```

---

### Step 2 — Add header

```markdown
---
layout: post
title: My First Blog Post
date: 2026-03-13
description: Short description
tags: [research]
categories: blog
---
```
You can explore existing post templates for reference.

---

### Step 3 — Write content

```markdown
# Title of your post

Write your blog post here, using Markdown.
```

---

### Step 4 — Preview locally

See instructions below.

---

## Running the Website Locally

### Mac Setup

#### 1. Install Homebrew

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
````

---

#### 2. Install Ruby

```bash
brew install ruby
```

Add to PATH:

```bash
echo 'export PATH="/usr/local/opt/ruby/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
```

---

#### 3. Install Bundler

```bash
gem install bundler
```

---

#### 4. Clone repo

```bash
git clone https://github.com/Sabia-Lab/sabia-website.git
cd sabia-website
```

---

#### 5. Install dependencies

```bash
bundle install
```

---

#### 6. Run server

```bash
bundle exec jekyll serve
```

---

#### 7. Open browser

[http://localhost:4000](http://localhost:4000)

---

### Windows Setup

#### 1. Install Ruby

Download from: [https://rubyinstaller.org/](https://rubyinstaller.org/)
Install **Ruby + Devkit**

---

#### 2. Install Bundler

```bash
gem install bundler
```

---

#### 3. Install Git

Download from: [https://git-scm.com/download/win](https://git-scm.com/download/win)

---

#### 4. Clone repo

```bash
git clone https://github.com/Sabia-Lab/sabia-website.git
cd sabia-website
```

---

#### 5. Install dependencies

```bash
bundle install
```

---

#### 6. Run server

```bash
bundle exec jekyll serve
```

---

#### 7. Open browser

[http://localhost:4000](http://localhost:4000)

---

## Publishing Changes

```bash
git add .
git commit -m "Your message"
git push
```

The site will automatically update via GitHub Pages.

---

## Useful Resources

* Jekyll: [https://jekyllrb.com/docs/](https://jekyllrb.com/docs/)
* Markdown: [https://www.markdownguide.org/](https://www.markdownguide.org/)
