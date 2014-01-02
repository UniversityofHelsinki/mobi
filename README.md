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


## Deployment

1. Build project
	* in project root directory `grunt build`
	* grunt will create new folder __dist__ that contains the published project
	* you can also test the built project with `grunt serve:dist` (will also build the project)
	* __NOTE__: you can preview the html files in browser without a web server but some image paths might not match
2. Move contents of the dist directory to a web server
	
