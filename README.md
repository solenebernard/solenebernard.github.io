# Template website

This website project is geared towards an academic audience.

Creation, modification and customization of the template is fairly easy since it powered by [Jekyll](https://jekyllrb.com/) and [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/).

Note

- the editable content of your website is in the `master` branch
- the `gh-pages` branch is meant for GitHub Pages to deploy it
- your website `https://<github-username>.github.io` will be publicly available, regardless your repository is public or private

## Prerequisites

### Set up your GitHub repository

- [Register for a GitHub account](https://github.com/join),

Two different paths are suggested:

1. [Fork](https://github.com/CRIStAL-Sigma/cristal-sigma.github.io/fork) the repository.

    This will allow you to interact with [github.com/CRIStAL-Sigma/cristal-sigma.github.io](https://github.com/CRIStAL-Sigma/cristal-sigma.github.io/repository) and [github.com/mmistakes/minimal-mistakes](https://github.com/mmistakes/minimal-mistakes) repositories (raise [issues](https://github.com/CRIStAL-Sigma/cristal-sigma.github.io/issues), get updates, propose [pull requests](https://github.com/CRIStAL-Sigma/cristal-sigma.github.io/pulls), etc.) based on the fact that you'll share a common history.

    a) Rename the repository as `<github-username>.github.io` in `Settings/Options/Repository name`.

    Note: [this long history](https://github.com/CRIStAL-Sigma/cristal-sigma.github.io/commits/master) may take some space on your local machine.

2. [Create a new repository from the template](https://github.com/CRIStAL-Sigma/cristal-sigma.github.io/generate)

    The new repository will start with the same files and folders as [CRIStAL-Sigma/cristal-sigma.github.io](https://github.com/CRIStAL-Sigma/cristal-sigma.github.io), but with your own fresh history.
    You will be able to interact with [CRIStAL-Sigma/cristal-sigma.github.io](https://github.com/CRIStAL-Sigma/cristal-sigma.github.io) only by raising [issues](https://github.com/CRIStAL-Sigma/cristal-sigma.github.io/issues).

    a) Name the repository as `<github-username>.github.io`,

    b) Tick the box "Include all branches".

---

In both cases, make sure to set up GitHub Pages to deploy your site from the `gh-pages` branch:

- Go to `Settings/Pages/Source`,
- Select the `gh-pages` branch and `/ (root)` folder.

At this point you can check the url `https://<github-username>.github.io`, it should look like [https://cristal-sigma.github.io](https://cristal-sigma.github.io/).

### Get a local copy of your remote GitHub repository

- Make sure you have [`git`](https://git-scm.com/) installed on your computer,
- Clone your repository on your computer:

  ```bash
    cd <directory-of-your-choice>
    git clone https://github.com/<github-username>/<github-username>.github.io.git
  ```

### Install local dependencies

Your website is powered by [Jekyll](https://jekyllrb.com/) and [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/).
In order to [build and serve your site locally](#Build-and-serve-your-site-locally) your need to install some dependencies.

- Follow the [installation instructions](https://jekyllrb.com/docs/installation/) of [Jekyll](https://jekyllrb.com/) to get

  - Ruby,
  - Bundler,
  - Jekyll.

- Install the project dependencies (`github-pages`, `minimal-mistakes-jekyll`, `jekyll-scholar`) stored in the `Gemfile` file:

  ```bash
    cd <path-to-github-username.github.io>
    git checkout master
    bundle install
  ```

## Build and serve your site locally

```bash
  cd <path-to-your-directory.github.io>
  git checkout master
  bundle exec jekyll serve --livereload
```

Part of the output should look like

```bash
  ...
   Auto-regeneration: enabled for '<path-to-your-directory.github.io>'
  LiveReload address: http://127.0.0.1:35729
      Server address: http://127.0.0.1:4000
    Server running... press ctrl-c to stop.
  ...
```

If you go to [http://127.0.0.1:4000](http://127.0.0.1:4000) on your browser you should get a live view of the current state of your website.

More specifically,

- `bundle exec` builds the site and outputs `.html` files, stored in the `_site` folder,
- `jekyll serve` opens a port to make the site available in a local server, here `http://127.0.0.1:4000`,
- `--livereload` automatically refreshes the page according to each change made to the source files.

## Modify the content of your site

You can create pages, posts, add images etc., using simple Markdown syntax in `.md` files.

Have a look at

- [Minimal Mistake's documentation](https://mmistakes.github.io/minimal-mistakes/docs/configuration/),
- [Jekyll's documentation](https://jekyllrb.com/docs/),
- [Markdown syntax guide](https://www.markdownguide.org/),
- [Liquid syntax guide](https://shopify.github.io/liquid/).

Note: you can also write plain HTML in `.md` files.

### Meta-data

Fill in the `_config.yml` with your meta-data.

Note: any changes made to the `_config.yml` file require the site to be rebuilt, see [build and serve your site locally](#Build-and-serve-your-site-locally).

### Color skin

For this project we have selected the "dark" skin as default, but you can choose a different one:

- change the `minimal_mistakes_skin: "dark" # "air", "aqua", "contrast", "dark", "default", "dirt", "neon", "mint", "plum" "sunrise"` in the `_config.yml` file,
- skins are showcased [here](https://mmistakes.github.io/minimal-mistakes/docs/configuration/#skin).

### Main/Home page

The main/home page of your website is defined in the `index.md` (or `index.html`) file at the root of the project.

### Bibliography

This project makes use of the [jekyll-scholar](https://github.com/inukshuk/jekyll-scholar) plugin to manage bibliographic entries.

- The default `.bib` file is
  - located at `_bibliography/example.bib`,
  - set as default in `scholar:` section of the `_config.yml` file.
- The default "Publications" page is
  - declared in `_pages/publications.md`,
  - set as a website page in `_data/navigation.yml`.
- Configuration options of your bibliography can be passed in the `scholar:` section of the `_config.yml` file, see also [jekyll-scholar's documentation](https://github.com/inukshuk/jekyll-scholar).

#### Buttons with links

Buttons with links will appear for references having non empty fields

```bibtex
@type{bib-key
...
url = {}
arxivid = {}
code = {<link-to-code-repository>}
video = {<link-to-video>}
...
}
```

Additionally, if you store poster and slides files as `/assets/pds/<bib-key>_poster.pdf` or `/assets/pds/<bib-key>_slides.pdf`
the corresponding buttons will also be displayed.

## Deploy your site

Your site `https://<github-username>.github.io` will be deployed by GitHub Pages from your remote `gh-pages` branch (set up as the source branch for GitHub Pages in [set up your GitHub repository](#Set-up-your-GitHub-repository))

However, this project uses the [`jekyll-scholar`](https://github.com/inukshuk/jekyll-scholar) plugin to render bibliography contents, which is incompatible with the GitHub Pages workflow.

Nevertheless, you can still push the website built source files (content of the `_site` folder) to the `gh-pages` branch and let GitHub Pages deploy it for you.

To do this (see also the [GitHub gist](https://gist.github.com/cobyism/4730490#gistcomment-3288642))

- Make sure `_site` is not listed in the `.gitignore` file
- Save and commit your last changes (content of the `_site` folder)

  ```bash
    git commit -m "<my-message>"
  ```

- Push to the remote `gh-pages` branch

  ```bash
    git push origin `git subtree split --prefix _site master`:gh-pages --force
  ```

  GitHub Pages will automatically generate your website from the source files you've pushed on the `gh-pages` branch.

- That's it! You can check the results at `https://<github-username>.github.io`

  Note: you may need to clean some of your browser's navigation data like cache or cookies to see the changes online.
