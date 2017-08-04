# My Dev Notes

These are the steps to build the site locally for testing and fine-tuning before committing and pushing to GitHub.

## Build

Open `Terminal` and navigate to git repo using the bash alias I created. Then, pull down the latest git changes from GitHub. Finally, start the jekyll script to run a server and regenerate the site when code or content changes.

``` bash
cd-cv
git pull
bundle exec jekyll server
```

## Structure

Jekyll app generates all code in the `_site` directory so no code should be changed in there. The files in the following locations should be modified instead:


* HTML - `./layouts/default.html`
* CSS - `./assets/css/style.scss`
* JS - `./layouts/default.html`
* images/icons - `./assets/images/icons`
* titles - `./_config.yml`
* content - `./README.md`