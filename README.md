# HY rwd mobile guide

Built with
* yeoman [generator-webapp](https://github.com/yeoman/generator-webapp)
	* [html5boilerplate](http://html5boilerplate.com)
  * [sass-bootstrap](http://getbootstrap.com)
	* [jquery](http://jquery.com)
  * [modernizr](http://modernizr.com)
* external dependencies
	* [compass-flexbox](https://github.com/timhettler/compass-flexbox)


## Getting started

1. Get source code
	1. create ssh key for Futurice gitlab `ssh-keygen -t rsa -C "name@domain.com"`
	2. view created public key `cat ~/.ssh/id_rsa.pub`
	3. click __Add public key__ in [code.futurice.com](https://code.futurice.com/profile) and copy paste key from terminal
	4. clone project repository `git clone git@code.futurice.com:hy_mobiiliohjeistus.git`
2. Install development environment
	1. install node.js and npm (with homebrew)
		1. update homebrew formulas `brew update`
		2. install [node.js](http://nodejs.org) `brew install node`
		3. install [npm](http://npmjs.org) `brew install npm`
	2. install compass and compass-flexbox (with ruby gem)
		1. update gems `gem update --system`
		2. install [compass](http://compass-style.org) `gem install compass`
		3. install [compass-flexbox](https://github.com/timhettler/compass-flexbox) `gem install compass-flexbox`
		
	3. install [yeoman](http://yeoman.io) which comes with [grunt](http://gruntjs.com) and [bower](http://bower.io) `npm install -g yo`
3. Install project dependencies
	1. install npm dependencies `npm install`
	2. install bower dependencies `bower update`
4. Start development server `grunt serve`
5. Open specified url in browser


## Deployment
  
  


# Antin stepit
1. ssh-keygen -t rsa -C "name@domain.com"
2. cat ~/.ssh/id_rsa.pub
3. copy paste key to code.futurice.com
4. git clone git@code.futurice.com:hy_mobiiliohjeistus.git
5. sudo npm install -g yo
6. sudo npm install -g grunt-cli
7. npm install
8. sudo gem update --system
9. sudo gem install compass
10. sudo gem install compass-flexbox
11. bower update
12. grunt serve
13. browse to http://127.0.0.1:9000



