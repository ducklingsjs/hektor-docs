# minify

## Implementation status

### Gulp: Implemented
### Grunt: None

## Subtasks

  * [clean](clean.md)
  * useref
  * uglify
  * minify-css

## Options

  * src
    * path to the html files
    * default: ``"<%= paths.app %>/index.html"``
  * dest
    * folder where the modified html, css and js files will be saved
    * default: ``"<%= paths.dist %>"``
  * searchPath
    * folder where the linked css and script files can be found
    * default: ``"<%= paths.tmp %>"``

## Options in HTML files

Example: [hektor-projects](/infinumjs/hektor-projects/blob/master/backbone.marionette-es6-gulp/index.html)

  * concatinate css between comments:
    * ``<!-- build:css styles.css --><!-- endbuild -->``
    * ``styles.css`` defines where the concatenated file will be saved inside of the dest folder
  * concatinate scripts between comments:
    * ``<!-- build:js scripts.js --><!-- endbuild -->``
    * ``scripts.js`` defines where the concatenated file will be saved inside of the dest folder
