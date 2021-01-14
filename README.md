# mkdocs-template

To use this template you need to run those commands first:

```
pip install mkdocs
```
```
pip install mkdocs-material
```

# How to use

Before you build your pages, the first step is to edit **mkdocs.yml** and configure it. Every change must be done in **docs_dir** to work properly.

### Adding pages

You can add your own pages in **pages/** folder (eg. example.md).

### Adding images

All images can be stored in any folder you want, so it's up to you, but the only requirement this theme has is that favicon MUST be stored in **assets/images** folder in docs_dir.

### Logo and favicon

To change them, edit **mkdocs.yml** file and set path for logo and favicon in **_theme_** section.

### Navigation and nesting

To add navigation links use **mkdocs.yml** file. Every link should be under nav property. 

Example:
```
nav:
  - Home: 'index.md'
  - 'Section':
    - About: 'about.md'
```
This example includes nested links too. Remember to add **tabs** where you want to have drop-down list.

### Variables

To use variables you need to install mkdocs extension

```
pip install mkdocs-macros-plugin
```

Then, edit **mkdocs.yml** and add your own variables.

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
