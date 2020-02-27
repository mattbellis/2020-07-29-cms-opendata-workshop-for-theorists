[![Build Status](https://travis-ci.com/carpentries/workshop-template.svg?branch=gh-pages)](https://travis-ci.com/carpentries/workshop-template)

[Live site](https://mattbellis.github.io/2020-07-29-cms-opendata-workshop-for-theorists/)

# workshop-template

This repository is copied from The Carpentries' ([Software Carpentry][swc-site], [Data Carpentry][dc-site], and [Library Carpentry][lc-site]'s)
template for creating websites for workshops.


## Checking Your Changes Locally

If you want to preview your changes on your own machine before publishing them on GitHub,
you can do so as described below.

1.  Install the software [described below](#installing-software).
    This may require some work,
    so feel free to preview by pushing to the website.

2.  Run the command

    ~~~
    make serve
    ~~~

    and go to <http://0.0.0.0:4000> to preview your site.
    You can also run this command by typing `make serve`
    (assuming you have Make installed).

3.  Run the command

    ~~~
    make workshop-check
    ~~~

    to check for a few common errors in your workshop's home page.
    (You must have Python 3 installed to do this.)

## (Optional) Linking to Your Page

At the top of your repository on GitHub you'll see

~~~
No description, website, or topics provided. — Edit
~~~

Click 'Edit' and add:

1.  A very brief description of your workshop in the "Description" box (e.g., "Miskatonic University workshop, Dec. 2016")

2.  The URL for your workshop in the "Website" box (e.g., `https://gvwilson.github.io/2016-12-01-miskatonic`)

This will help people find your website if they come to your repository's home page.

## Creating Extra Pages

In rare cases,
you may want to add extra pages to your workshop website.
You can do this by putting either Markdown or HTML pages in the website's root directory
and styling them according to the instructions give in
[the lesson template][lesson-example].
If you do this,
you *must* also edit `_config.yml` to set these three values:

1.  `carpentry` is either "dc" (for Data Carpentry), "swc" (for Software Carpentry),
    or "lc" (for Library Carpentry). This determines which logos are loaded.

2.  `title` is the title of your workshop (typically the venue and date).

3.  `email` is the contact email address for your workshop,
    e.g., `gvwilson@miskatonic.edu`.

Note: `carpentry` and `email` duplicate information that's in `index.md`,
but there is no way to avoid this
without requiring people to edit both files in the usual case
where no extra pages are created.

## Installing Software

If you want to set up Jekyll
so that you can preview changes on your own machine before pushing them to GitHub,
you must install the software described below.
(Note: Julian Thilo has written instructions for
[installing Jekyll on Windows][jekyll-windows].)

1.  **Ruby**.
    This is included with Linux and macOS;
    the simplest option on Windows is to use [RubyInstaller][ruby-installer].
    You can test your installation by running `ruby --version`.
    For more information,
    see [the Ruby installation guidelines][ruby-install-guide].

2.  **[RubyGems][rubygems]**
    (the package manager for Ruby).
    You can test your installation by running `gem --version`.

3.  **[Jekyll][jekyll]**.
    You can install this by running `gem install jekyll`.

## Setting Up a Separate Repository for Learners

If you are teaching Git,
you should create a separate repository for learners to use in that lesson.
You should not have them use the workshop website repository because:

*   your workshop website repository contains many files
    that most learners don't need to see during the lesson,
    and

*   you probably don't want to accidentally merge
    a damaging pull request from a novice Git user
    into your workshop's website while you are using it to teach.

You can call this repository whatever you like,
and add whatever content you need to it.

## Getting and Giving Help

We are committed to offering a pleasant setup experience for our learners and organizers.
If you find bugs in our instructions,
or would like to suggest improvements,
please [file an issue][issues]
or [mail us][email].

[email]: mailto:team@carpentries.org
[customization]: https://carpentries.github.io/workshop-template/customization/index.html
[dc-site]: http://datacarpentry.org
[design]: https://carpentries.github.io/workshop-template/design/
[faq]: https://carpentries.github.io/workshop-template/faq/index.html
[github-project-pages]: https://help.github.com/en/github/working-with-github-pages/creating-a-github-pages-site
[importer]: https://github.com/new/import
[issues]: https://github.com/carpentries/workshop-template/issues
[jekyll-windows]: http://jekyll-windows.juthilo.com/
[jekyll]: https://jekyllrb.com/
[lesson-example]: https://carpentries.github.io/lesson-example/
[pyyaml]: https://pypi.python.org/pypi/PyYAML
[ruby-install-guide]: https://www.ruby-lang.org/en/downloads/
[ruby-installer]: http://rubyinstaller.org/
[rubygems]: https://rubygems.org/pages/download/
[self-organized-workshop-form]: https://amy.carpentries.org/forms/self-organised/
[swc-site]: http://software-carpentry.org
[lc-site]: https://librarycarpentry.org
