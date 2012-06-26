mapnik-on-heroku
================

Holy crap, it's Mapnik running on Heroku! This is a quick implementation of node-mapnik's default example, running on Heroku *with very little configuration*. Epic thanks to [Dane Springmeyer](https://github.com/springmeyer) for going [above and beyond](https://github.com/mapnik/node-mapnik/issues/95).

This application uses [node-mapnik-heroku](https://github.com/springmeyer/node-mapnik-heroku) to render a simple map using Mapnik on Heroku. **This changes everything**.

Installation
------------

Once you have it pushed to Heroku, just set the following environment variable:

    $ heroku config:add LD_LIBRARY_PATH=/app/node_modules/mapnik/lib
    
How?
-----
The mapnik binaries have been precompiled and included in the [node-mapnik-heroku](https://github.com/springmeyer/node-mapnik-heroku) module. This is a [little known feature](http://bindle.me/blog/index.php/405/running-binaries-on-heroku) of Heroku.