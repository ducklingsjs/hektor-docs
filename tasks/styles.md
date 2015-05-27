# styles

## Implementation status

### Gulp: Implemented
### Grunt: None

## Subtasks

  * sass
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
