# codecheck

## Implementation status

### Gulp: Implemented
### Grunt: None

## Subtasks

  * jshint
  * scss-lint

## Options

  * src
    * js
      * entry point
      * default: ``"<%= paths.app %>/scripts/**/*.js"``
    * scss
      * entry point
      * default: ``"<%= paths.app %>/styles/**/*.scss"``
  * config
    * scss
      * path to the linter config
      * default: ``".scss-lint.yml"``
  * fail
    * should the task fail if there is a problem
    * default: ``false``
