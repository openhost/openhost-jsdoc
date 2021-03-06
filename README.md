Openhost JSDoc
=============
JSDoc 3 Template for AngularJS.  

Features
----------
  * Left side TOC, table of contents, for navigation by Directives, Services, Controllers, etc.
  * Right side menu for navigation by component members.
  * Read and process @ngdoc tag.

Install
-------
    $ npm install jsdoc openhost-jsdoc --save-dev

Run In Command Line
-------------------
Run jsdoc command to generate your documentation. 
All command line options are the options of [jsdoc](http://usejsdoc.org/about-commandline.html)  
    
    $ path/to/jsdoc -c path to conf> -t <template> <your source code>

In example,  

    $ node_modules/jsdoc/jsdoc.js -c node_modules/openhost-jsdoc/conf -t node_modules/openhost-jsdoc/template -r myDir

Run with gulp-jsdoc
-------------------
1. install gulp-shell  
    `$ npm install gulp-shell --save-dev`

2. add the following to the gulpfile.json  
   ```
   var shell = require('gulp-shell'); 
   gulp.task('docs', shell.task([ 
     'node_modules/jsdoc/jsdoc.js '+ 
       '-c node_modules/angular-jsdoc/conf.json '+   // config file
       '-t node_modules/angular-jsdoc/template '+    // template file
       '-d build/docs '+                             // output directory
       './README.md ' +                              // to include README.md as index contents
       '-r app/scripts'                              // source code directory
   ])); 
   ```
3. run gulp task  
    `$ gulp docs`
