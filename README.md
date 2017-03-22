# Micua Home（a webapp template）---传智播客中，王磊老是的gulp案例。
[![Build Status](https://secure.travis-ci.org/Micua/Home.svg?branch=master)](http://travis-ci.org/Micua/Home)

## 自动任务介绍

* gulp.task('styles', () => {});   编译sass文件，压缩

* function lint(files, options) {});  语法校验

* gulp.task('html', ['styles'], () => {});  压缩html以及修改所引用的文件路径，如css js

* gulp.task('reversion', ['html'], () => {});  版本管理任务

* gulp.task('images', () => {}); 压缩图片大小

* gulp.task('fonts', () => {}); 字体图标全部放到根目录

* gulp.task('extras', () => {}); 扩展

* gulp.task('clean', del.bind(null, ['temp', 'dist', '.publish'])); 先清除临时文件

* gulp.task('serve', ['styles', 'fonts'], () => {});

* gulp.task('build', ['lint', 'reversion', 'images', 'fonts', 'extras'], () => {});  

* gulp.task('default', ['clean'], () => {
*  gulp.start('build');
* });



## Features

Please see our [gulpfile](app/templates/gulpfile.babel.js) for up to date information on what we support.

* CSS Autoprefixing
* Built-in preview server with BrowserSync
* Automagically compile Sass with [libsass](http://libsass.org)
* Automagically lint your scripts
* Map compiled CSS to source stylesheets with source maps
* Awesome image optimization
* Automagically wire-up dependencies installed with [Bower](http://bower.io)
* The gulpfile makes use of [ES2015 features](https://babeljs.io/docs/learn-es2015/) by using [Babel](https://babeljs.io)

*For more information on what this generator can do for you, take a look at the [gulp plugins](app/templates/_package.json) used in our `package.json`.*


## libsass

Keep in mind that libsass is feature-wise not fully compatible with Ruby Sass. Check out [this](http://sass-compatibility.github.io) curated list of incompatibilities to find out which features are missing.

If your favorite feature is missing and you really need Ruby Sass, you can always switch to [gulp-ruby-sass](https://github.com/sindresorhus/gulp-ruby-sass) and update the `styles` task in gulpfile accordingly.


## Getting Started

- Run `gulp serve` to preview and watch for changes
- Run `bower install --save <package>` to install frontend dependencies
- Run `gulp serve:test` to run the tests in the browser
- Run `gulp` to build your webapp for production
- Run `gulp serve:dist` to preview the production build


## License

ISC © [iceStone](https://github.com/Micua/)

## Install
- npm i babel-core babel-preset-es2015 browser-sync del gulp gulp-autoprefixer gulp-cache gulp-cssnano gulp-eslint gulp-gh-pages gulp-htmlmin gulp-if gulp-imagemin gulp-load-plugins gulp-plumber gulp-reversion gulp-sass gulp-size gulp-sourcemaps gulp-uglify gulp-useref main-bower-files wiredep --save-dev
