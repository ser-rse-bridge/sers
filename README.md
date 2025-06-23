# Website for the workshop "Software Engineering and Research Software"

Submitted to ICSE 2026.

## Introduction

This repository is based on a template (in the GitHub sense) to facilitate setting up
sub-sites of <ser-rse-bridge.github.io> with styling consistent to the main site.

## Install & serve locally

To encapsulate the dependencies for building this site locally, you can use `conda` (or as used here: `mamba`).

1. Create a new `conda` environment with the name `jekyll` and the main dependencies from the environment definition file `conda-env.yml`:

`mamba env create -n jekyll --file conda-env.yml`

2. Activate the environment:

`mamba activate jekyll`

3. Install the website dependencies using the Ruby `bundler`:

`bundle install`

4. Serve the website on `http://127.0.0.1:4000`:

`bundle exec jekyll serve` (optionally using `-w` to watch changes and update live)

5. Stop the server with `CTRL` + `C`

## Deploy

Pushing to `main` will trigger a GitHub Action that builds and deploys the website to https://ser-rse-bridge.github.io/sers/.

## Notes

This repository originally contained a modified version of the Minimal Mistakes file `_includes/masthead.html` in which the masthead links (on the logo, title, and subtitle) are directed to the parent site rather than the top of the current site. This makes the masthead link behavior consistent between the main site and the sub-site.
The files has been removed to isolate the page from the main repository until we know if the workshop has been accepted.
If it is accepted, the behavior should be re-added, e.g., from [this commit](https://github.com/ser-rse-bridge/sers/blob/6bb6cc484d58a1c75705ec671c97d6e2c56a8c34/_includes/masthead.html).
