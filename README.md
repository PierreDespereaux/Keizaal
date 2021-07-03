
This repo hosts the website for Keizaal. This file is the repo's readme page, shown when the repo is directly accessed on GitHub, and so should not have Jekyll "[front matter](https://jekyllrb.com/docs/front-matter/)" added to it.

The site currently relies on Jekyll, run through GitHub Pages, as a build system. Editors should take note of the following details:

* Most pages are written in Markdown and contain Jekyll front matter, which is what allows them to be built as part of the site. Pages should specify their layout and titles; no defaults are specified in the configuration file. The site homepage is at `index.md`, which should generate as `index.html`.

* The "testimonials" page is an exception, being written in HTML with front matter to allow the use of [Utterances](https://utteranc.es/) as a comment system.

* We use fully custom site CSS. This CSS *does not* support Jekyll's theming system, because GitHub Pages makes it impossible to *not* use a theme. You are [supposed to be able](https://github.com/github/pages-gem/blob/master/lib/github-pages/configuration.rb#L108) to disable the default theme (Primer) by setting `theme: null` in your Jekyll configuration file, but this doesn't actually work; Primer is still used as the theme. Alternatively, you are supposed to be able to [select a "remote theme"](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/adding-a-theme-to-your-github-pages-site-using-jekyll), such as an empty no-op theme, but this also does not work, and there is no useful error messaging to indicate why. Our choice, then, was between dealing with Primer's cruft, or simply building the site so that it never actually includes theme files or CSS.