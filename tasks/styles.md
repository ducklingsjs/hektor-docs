# styles

## Implementation status

### Gulp: Implemented
### Grunt: None

## Subtasks

  * node-sass
  * autoprefixer

## Options

  * src
    * entry point
    * default: ``"<%= paths.app %>/styles/main.scss"``
  * includePaths
    * paths that are automatically included
    * default: ``["<%= paths.app %>/bower_components"]``
  * browsers
    * browser support needed
    * default: ``['last 2 versions', 'ie 10']``
  * dest
    * destination path
    * default: ``"<%= paths.tmp %>/styles"``
  * loco
    * if [loco-sass](https://github.com/DarkoKukovec/loco-sass) should be used
    * NOTE: Autporefixer doesn't work yet with loco-sass in this task
    * default: ``null``
    * dest
      * destination where the mapping files should be saved
    * format
      * [format](https://github.com/DarkoKukovec/loco-sass#options) of the local selectors
