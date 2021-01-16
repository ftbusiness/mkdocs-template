# mkdocs-template

To use this template you need to run those commands first:

```
pip install mkdocs
```
```
pip install mkdocs-material
```

### Preview

https://swaggin.github.io/mkdocs-template/

# How to use

Before you build your pages, the first step is to edit **_mkdocs.yml_** and configure it. Every content change must be done in **_docs_dir_** to work properly.

You can run
```
mkdocs serve
```
command to see your changes in browser. 

### Adding pages

You can add your own pages in **_pages/_** folder (eg. example.md).

### Adding images

All images can be stored in any folder you want, so it's up to you, but the only requirement this theme has is that favicon MUST be stored in **_assets/images_** folder in docs_dir.

### Logo and favicon

To change them, edit **_mkdocs.yml_** file and set path for logo and favicon in **_theme_** section.

Example:
```
theme:
  logo: 'assets/images/FT-logo.png'
  favicon: 'assets/images/favicon.ico'
```

### Navigation and nesting

To add navigation links use **_mkdocs.yml_** file. Every link should be under nav section. 

Example:
```
nav:
  - Home: 'index.md'
  - 'Section':
    - About: 'about.md'
```
This example includes nested links too. Remember to add **_tabs_** where you want to have drop-down list.
As you can see, you don't have to set path for drop-down list element, but you need to use single apostrophes to make it work.

### Variables

To use variables you need to install mkdocs extension:

```
pip install mkdocs-macros-plugin
```

Then, edit **_mkdocs.yml_** and add your own variables.

Here's the example: 
```
extra:
  example:
    title: 'FT Docs'
  example2: 'Hello World'
```

To use variables you need to insert them in .md files like this:
```
Hello, {{ example.title }}
```
or

```
Hello, {{ example2 }}
```

Variables can be stored in an external file or in **_mkdocs.yml_** under **_extra_** section. See more info [here](https://squidfunk.github.io/mkdocs-material/reference/variables/).

# Deploying

When you're done building you docs, run:
```
mkdocs build
```
This command generates static sites you can view or deploy to your repo. To do this, run:
```
mkdocs gh-deploy
```
It creates new branch where your entire docs are stored.

# Useful links

[mkdocs](https://www.mkdocs.org/) official documentation

[mkdocs material theme](https://squidfunk.github.io/mkdocs-material/getting-started/) official documentation
