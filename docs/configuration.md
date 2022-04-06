---
layout: default
title: Instruction 1
nav_order: 2
---

# Setting up Git
{: .no_toc }

After this setup, users should have a functional git with an attached username and email.
\_config.yml file.
{: .fs-6 .fw-300 }

## Table of contents
{: .no_toc .text-delta }

1. Windows setup
2. Mac (OSX) setup
{:toc}

---

View this site's [\_config.yml](https://github.com/just-the-docs/just-the-docs/tree/main/_config.yml) file as an example.

## Windows Setup

1. Download the 64-bit version of the Git Windows setup using the following link:
https://git-scm.com/download/win


```yaml
Note: If you're using a 10-year-old system or older, consider using the 32-bit Windows Setup. The 64-bit version may not be compatible with your system.
```

2. Open the installer and accept all the defaults *except* for the default editor "Vim". Vim is hard to use and not recommended for beginners. I'd recommend selecting Notepad++.
   
```yaml
Note: If you don't have Notepad++ already, download it with the prompt from the installer and install it with default settings.

Once Notepad++ is done installing, press "Back" on the Git installer and "Next" again to refresh the option to continue.
```

3. Once the installer is finished, launch git by right-clicking on an empty space on your desktop or window and selecting "Git Bash here"

4. In the console, type the following to edit your name and email:

```yaml
Username:
git config --global user.name "Adam Savage"
(replace Adam Savage with your name)

Email:
git config --global user.email "adam@hotmail.ca"
(replace adam@hotmail.ca with your email)
```

5. Verify your information by type the following:
```yaml
git config --list
```
and look at the user.name and user.email field to double-check that they've been set properly.

## Mac (OSX) Setup

1. Press Command-space to launch Spotlight and type "Terminal" then double click the search result.
https://brew.sh/
1. Install [homebrew](https://brew.sh/) if it's not already installed by typing:

```yaml
$ brew install git
```

_note: `footer_content` is deprecated, but still supported. For a better experience we have moved this into an include called `_includes/footer_custom.html` which will allow for robust markup / liquid-based content._

- the "page last modified" data will only display if a page has a key called `last_modified_date`, formatted in some readable date format
- `last_edit_time_format` uses Ruby's DateTime formatter; see examples and more information [at this link.](https://apidock.com/ruby/DateTime/strftime)
- `gh_edit_repository` is the URL of the project's GitHub repository
- `gh_edit_branch` is the branch that the docs site is served from; defaults to `main`
- `gh_edit_source` is the source directory that your project files are stored in (should be the same as [site.source](https://jekyllrb.com/docs/configuration/options/))
- `gh_edit_view_mode` is `"tree"` by default, which brings the user to the github page; switch to `"edit"` to bring the user directly into editing mode

## Color scheme

```yaml
# Color scheme supports "light" (default) and "dark"
color_scheme: dark
```

<button class="btn js-toggle-dark-mode">Preview dark color scheme</button>

<script>
const toggleDarkMode = document.querySelector('.js-toggle-dark-mode');

jtd.addEvent(toggleDarkMode, 'click', function(){
  if (jtd.getTheme() === 'dark') {
    jtd.setTheme('light');
    toggleDarkMode.textContent = 'Preview dark color scheme';
  } else {
    jtd.setTheme('dark');
    toggleDarkMode.textContent = 'Return to the light side';
  }
});
</script>

See [Customization]({{ site.baseurl }}{% link docs/customization.md %}) for more information.

## Google Analytics

```yaml
# Google Analytics Tracking (optional)
# e.g, UA-1234567-89
ga_tracking: UA-5555555-55
ga_tracking_anonymize_ip: true # Use GDPR compliant Google Analytics settings (true by default)
```

## Document collections

By default, the navigation and search include normal [pages](https://jekyllrb.com/docs/pages/).
Instead, you can also use [Jekyll collections](https://jekyllrb.com/docs/collections/) which group documents semantically together.

For example, put all your documentation files in the `_docs` folder and create the `docs` collection:

```yaml
# Define Jekyll collections
collections:
  # Define a collection named "docs", its documents reside in the "_docs" directory
  docs:
    permalink: "/:collection/:path/"
    output: true

just_the_docs:
  # Define which collections are used in just-the-docs
  collections:
    # Reference the "docs" collection
    docs:
      # Give the collection a name
      name: Documentation
      # Exclude the collection from the navigation
      # Supports true or false (default)
      nav_exclude: false
      # Exclude the collection from the search
      # Supports true or false (default)
      search_exclude: false
```

You can reference multiple collections.
This creates categories in the navigation with the configured names.

```yaml
collections:
  docs:
    permalink: "/:collection/:path/"
    output: true
  tutorials:
    permalink: "/:collection/:path/"
    output: true

just_the_docs:
  collections:
    docs:
      name: Documentation
    tutorials:
      name: Tutorials
```
