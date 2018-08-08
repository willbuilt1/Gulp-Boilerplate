# Gulp-Boilerplate

Boilerplate to get started on front end projects quickly. It uses:

 - PostCSS - for CSS nesting, variables and all other goodness
 - normalize.css - Improves cross browser consistency - see more here: https://necolas.github.io/normalize.css/
 - Gulp - for workflow automation
 - Webpack + Babel  - Use ES6 today with no qualms
 - Browser-sync - Live previewing across devices

To use, simply clone this repo and npm install. 

## Gulp
I have used Gulp as the taskrunner for this workflow. This handles the compiling and all copying and deleting in both development and production. The two main tasks are as follows:

**Development - gulp watch** 

Run `gulp watch` from the command line to start this task. This script is in charge of all the tasks required whilst in the development stage. The main tasks.

 - Starts Browser-sync 
 - Watches for any changes to your code. On save will compile and show you the results in the browser window
 - Uses PostCSS to handle all CSS compiling 
 - Uses webpack + babel to compile ES6 code into friendly ES5


**Production - gulp build**
Run `gulp build` from your command line to start this task. This task outputs production code and places it in the `./dist` folder. It does this by doing the following:

 - Minimizes images using `gulp-imagemin`
 - Minimizes CSS and JS using `gulp-rev` and `gulp-uglify` respectively
 - Adds cache busting revision numbers using `gulp-rev`

To see what your production build looks like run `gulp previewProd` from the command line.

Tip: if using Github Pages to host the project amend the location from `./dist` to `./docs`. For more info see https://help.github.com/articles/configuring-a-publishing-source-for-github-pages/

## PostCSS

I opted for PostCSS in this boilerplate as more of an experiment as I am used to using Sass but have found it very useful. What I like about it is that it provides alot of flexibility and allows you to import whatever plugin you require for your project. Below is listed the plugins I have used on this boilerplate but the full catalogue can be found at https://www.postcss.parts/ 

 - autoprefixer - Adds vendor prefixes to improve cross-browser compatibilty 
 - postcss-import - Allows functionalty to import CSS files  
 - postcss-mixins - adds mixins 
 - postcss-nested - allows you to nest CSS  
 - postcss-simple-vars - allows you to use variables using $
 - postcss-hexrgba - adds shorthand hex methods to rbga() values

## Dependencies
In this project I have pre-installed numerous packages that I find I use on nearly every project. These are listed below with brief descriptions.

 - jQuery - the popular Javascript library we all love.
 - jQuery Smooth Scroll - provides smooth scrolling within the page. Good for navigation
 - Lazysizes - Lazyloading for images - https://afarkas.github.io/lazysizes/index.html
 - Picturefill - Responsive images compatibilty - https://scottjehl.github.io/picturefill/
 - Waypoints - Sets a marker, when reached you can do something cool 😎 - http://imakewebthings.com/waypoints/

I can be found [@willbuilt1](https://twitter.com/willbuilt1) on twitter 