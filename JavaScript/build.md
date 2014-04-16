# Build

People suck at repetitive tasks.

* Linting
* Transpiling
* Minifying
* Combining (concat)

* [Goodbye Compass](http://bensmithett.com/goodbye-compass/)

## Make?

* [Tim Lucas's approach](https://gist.github.com/toolmantim/6200029)
* [The ultimate fronted build tool: `make`](https://algorithms.rdio.com/post/make/)
* [I love the Unix philosophy, but...](http://mntr.dk/2014/i-love-the-unix-philisophy-but/)

## package.json

* [Cheatsheet](http://package.json.jit.su/)

## Component vs Bower

Bower is meant to work with build tools rather than replace them.
Bower is not built with opinions on scripting loader or modular loading. It is not concerned with how the assets it manages get included in your web pages.

* [Some arguments with @visionmedia](https://github.com/bower/bower/pull/62)

## Glob

* `!name` - Matches any single character not in `name`
* `{s1, s2, s3}` - Matches any of the strings given (separated by commas)

## Browser Sync

* [Cross browser CSS injection](http://css-tricks.com/cross-browser-css-injection/)

## Gulp

Gulp has built-in watcher.
Grunt uses JSON-like data configuration files; Gulp uses leaner, simpler JavaScript code.

```
gulp.src(glob)   /* Returns a readable stream */
gulp.dist(glob)  /* Returns a writable stream */
```

* [A blank project with Gulp.js as build system](https://github.com/kyleconrad/blank-gulp)
* [Presentation on Gulp](http://slid.es/contra/gulp)
* [Gulp - The streaming build system](http://www.bram.us/2014/01/20/gulp-the-streaming-build-system/)
* https://www.youtube.com/watch?v=Blqaio9HaHA

### Plugins

* [gulp-browser-sync](https://github.com/shakyShane/gulp-browser-sync)
* [gulp-jshint](https://github.com/wearefractal/gulp-jshint)
* [gulp-autoprefixer](https://github.com/Metrime/gulp-autoprefixer)
* [gulp-changed](https://github.com/sindresorhus/gulp-changed)
* [gulp-imagemin](https://github.com/sindresorhus/gulp-imagemin)
* [gulp-strip-debug](https://github.com/sindresorhus/gulp-strip-debug)
* [gulp-uglify](https://github.com/terinjokes/gulp-uglify)
* [gulp-concat](https://github.com/wearefractal/gulp-concat)
* [gulp-svgmin](https://github.com/ben-eb/gulp-svgmin)
* [gulp-cssmin](https://github.com/chilijung/gulp-cssmin)
* [gulp-htmlmin](https://github.com/jonschlinkert/gulp-htmlmin)
* [jshint-stylish](https://github.com/sindresorhus/jshint-stylish)
* [grunt-montage](https://github.com/globaldev/grunt-montage)


## Grunt

### Plugins

* [grunt-uncss](https://github.com/addyosmani/grunt-uncss)
* [grunt-spritesmith](https://github.com/Ensighten/grunt-spritesmith)

## Broccoli

* [Broccoli - A fast, reliable asset pipeline](https://github.com/joliss/broccoli)
* [Architecture of Broccoli](http://www.solitr.com/blog/2014/02/broccoli-first-release/)