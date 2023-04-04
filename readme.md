# Kaleidoscope

A beautiful blog theme that changes color based on the time of day.

## Features

* Fully responsive
* Based on [PureCSS](https://purecss.io)
* FontAwesome
* [Fleur De Leah](https://fonts.google.com/specimen/Fleur+De+Leah) and [Playfair Display](https://fonts.google.com/specimen/Playfair+Display) fonts.
* 4 different colors schemes that change to match the morning, day, evening, and night.
* Supports lastmod
* Related posts
* Taxonomy pages
* TOC with `toc: true` in frontmatter

## Getting started

Inside your project folder, copy the theme to your `themes` folder.

```bash
git submodule init
git submodule add https://github.com/BravishkaSkytano/hugo-theme-kaleidoscope.git themes/kaleidoscope
```

If you'd like some example content and an example config file to get started, you can copy the `exampleSite` directory into your root Hugo directory.

```bash
cp -r themes/kaleidoscope/exampleSite/* ./
```

To learn more about building themes in Hugo, refer to Hugo's [templating documentation](https://gohugo.io/templates/).

## Keeping your site up-to-date when theme is updated using GitHub Actions

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

## To-Do

- [ ] Upload images of different themes
- [ ] Let user choose fonts
- [ ] Use your own colorschemes
- [ ] Add comments
- [ ] Configure search
- [ ] Configure RSS
- [X] Related posts
- [X] TOC