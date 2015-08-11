## Resume Source

The source for my resume static site. Instructions below:

##### To dev
```
$ git status // dev on gh-pages branch
$ grunt less // run after any Less changes
$ grunt // generates the js files and serves the project
```

##### To deploy
```
$ grunt build // builds the static site in the "build" directory
* git loop // (to push gh-pages branch containing everything to dev remote)
$ git subtree push --prefix build prod gh-pages (to push only "build" directory to prod remote)
```

Visit [http://localhost:8888](http://localhost:8888) to see changes.

##### Testing JSON changes
Test changes by updating `resume.json` file inside `node_modules/resume-schema/` folder. Rerun `grunt` optional: `exec:run_server` after any changes to `resume.json`

##### Updating styles
All the LESS files are organized under the folder `assets/less/`. Check the comments inside `theme.less` to find out which file to make LESS changes. Grunt compiles `assets/less/theme.less` to `assets/css/theme.css` which is used eventually in the theme. 

##### Updating Javascript
All the javascript changes go into `index.js` which is responsible for rendering the resume.
