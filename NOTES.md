# My Dev Notes

These are the steps to build the site locally for testing and fine-tuning before committing and pushing to GitHub.

## Build

Open `Terminal` and navigate to git repo using the bash alias I created. Then, pull down the latest git changes from GitHub. Finally, start the jekyll script to run a server and regenerate the site when code or content changes.

``` bash
cd-cv # alias to james-priest.github.io repo
git pull origin master
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

## Linting

Both JSHint & ESLint are enabled by default (as a dev exercise). Also installed `eslint-plugin-html` to lint js blocks in html files. Added these files to the working directory:

* `.eslintrc.json`
  * "env": {"browser": true, "es6": true, "jquery": true}
  * "extends": "eslint:recommended"
  * "plugins": [ "html" ]
* `.eslintignore` - ignore generated `_site` directory
* `.jshintrc` - set default set of jshint rules with these mods
  * "browser" : true, "devel" : true , "jquery" : true
* `.jshintignore` - ignore generated `_site` directory