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
    * default: ``".tmp"``
