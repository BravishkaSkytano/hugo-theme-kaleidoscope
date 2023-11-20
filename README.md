# Kaleidoscope: The most colorful Hugo theme you will ever find

I love a colorful site (as long as it's readable) and I thought it would be fun to create a theme with easily customizable colors!

## Features

* Fully responsive
* Based on [Tachyons CSS](https://tachyons.io/)
* Customizable colors and fonts
* Dark mode (working on it)
* Supports lastmod (from Git)
* Multilingual mode
* Featured posts with `featured: true` in frontmatter
* Related posts
* Taxonomy pages
* TOC with `toc: true` in frontmatter

## Why Tachyons?

Since Tachyons employs Single Utility Classes you are able to customize a lot of the theme without breaking things and having to copy and rewrite CSS files.

I also like the way Tachyons creates classes for fonts and colors. This makes it super easy to customize the theme in `config.yml` without rewriting CSS files.

## Installation

```bash
git submodule add https://github.com/BravishkaSkytano/hugo-theme-kaleidoscope.git themes/kaleidoscope
```

In your `config.yml` set `theme:` to kaleidoscope.

For more information on installing themes, refer to [Hugo's official setup guide.](https://gohugo.io/overview/installing/)

### Keeping your site up-to-date when the theme is updated using GitHub Actions

This works for both Git Submodules and Go Modules, you just need to specify which one you want to use by [enabling and configuring Dependabot](https://docs.github.com/en/code-security/dependabot/dependabot-version-updates/configuration-options-for-the-dependabot.yml-file).

```yml
version: 2
updates:
  # Enable version updates for git submodules
  - package-ecosystem: "gitsubmodule"
    # Look for submodules in the root directory
    directory: "/"
    # Check for updates once a week (on Monday)
    schedule:
      interval: "weekly"

  # Enable version updates for Go Modules
  - package-ecosystem: "gomod"
    # Look for a Go Modules in the `root` directory
    directory: "/"
    # Check for updates once a week
    schedule:
      interval: "weekly"
```

## Getting Started

You can copy the example config file.

```bash
cp -r themes/kaleidoscope/exampleSite/config.yml ./config.yml
```

Most of it is easy to understand, especially if you have worked with Hugo before. The only ones that you might want to change are the ones that have to do with Tachyons itself. Of course, it is all completely optional and you don't have to change it if you are happy with the default settings.

## Colors

To use your own colorscheme, you need to add `colors.css` to `static/css` in your root website folder.

```bash
cp -r themes/kaleidoscope/static/colors.css ./static/css/colors.css
```

Everything is easy, you don't need any coding knowledge. Just follow the instructions in the comments and you should be okay. If you need any help, go ahead and [open an issue.](https://github.com/BravishkaSkytano/hugo-theme-kaleidoscope/issues/new/choose)

## To-Do

* [X] Light/Dark toggle
* [ ] Add comments
* [ ] Configure search
* [X] Configure RSS
* [X] Featured posts
* [X] Related posts
* [X] TOC
* [X] Add FontAwesome
* [X] Socials
