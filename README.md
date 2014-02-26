# HY rwd mobile guide

Built with

* [yeoman](http://yeoman.io) [generator-webapp](https://github.com/yeoman/generator-webapp)
	* [html5boilerplate](http://html5boilerplate.com)
  	* [sass-bootstrap](http://getbootstrap.com)
	* [jquery](http://jquery.com)
  	* [modernizr](http://modernizr.com)
* external dependencies
	* [compass-flexbox](https://github.com/timhettler/compass-flexbox)

The web pages are built with Bootstrap 3 grid and components and don't contain any written javascript at the moment—just HTML and CSS. Thus these pages won't work on older browsers that don't support, e.g. css flexbox. That's where Javascript will prove useful.


## Getting started

1. Get source code
	1. create ssh key for Futurice gitlab `ssh-keygen -t rsa -C "name@domain.com"`
	2. view created public key `cat ~/.ssh/id_rsa.pub`
	3. click __Add public key__ in [code.futurice.com](https://code.futurice.com/profile) and copy paste key from terminal
	4. clone project repository `git clone git@code.futurice.com:hy_mobiiliohjeistus.git`
	5. go to project root directory `cd hy_mobiiliohjeistus`
2. Install development environment
	1. install [node.js](http://nodejs.org) and [npm](http://npmjs.org) (with homebrew)
		1. update homebrew formulas `brew update`
		2. install node.js `brew install node`
	2. install compass and compass-flexbox (with ruby gem)
		1. update gems `sudo gem update --system`
		2. install [compass](http://compass-style.org) `sudo gem install compass`
		3. install [compass-flexbox](https://github.com/timhettler/compass-flexbox) `sudo gem install compass-flexbox`
		
	3. install [yeoman](http://yeoman.io) which comes with [grunt](http://gruntjs.com) and [bower](http://bower.io) `npm install -g yo`
3. Install project dependencies
	1. install npm dependencies `npm install`
	2. install bower dependencies `bower update`
4. Start development server `grunt serve`
5. Url should open automatically in default browser. If not, browse to url at the end of prompt.


## Project dependencies

This project has three different dependencies

* npm dependencies in package.json
  * add new npm dependency by `npm install packagename --save-dev` 
  --save-dev adds packagename and version to package.json
  * after committing/pushing the changes to git, others will have to run `npm install`  
  after they have pulled the changes to install updated/added versions of the dependencies to their local machine
* bower dependencies in bower.json
  * add new bower dependency by `bower install packagename --save`  
  --save adds packagename and version to bower.json
  * after committing/pushing the changes to git, others will have to run `bower install`  
  after they have pulled the changes to install updated/added versions of the dependencies to their local machine
* compass dependencies in Gruntfile.js compass:options:require
  * install new compass dependency from gem
  * add new compass dependency to Gruntfile.js
  * after committing/pushing the changes to git, others will have to install the required compass dependencies from gem to their local machine after they have pulled the changes


## Development

All the development happens in __app__ directory

You should not make changes to __dist__ directory, because each `grunt build` will overwrite the changes. The files contain also all the css and js from bower dependencies, e.g. __bootstrap css and js__ which you shouldn't touch.


## Deployment

1. Build project
	* in project root directory `grunt build`
	* grunt will create new folder __dist__ that contains the published project
	* you can also test the built project with `grunt serve:dist` (will also build the project)
2. Move contents of the dist directory to a web server
