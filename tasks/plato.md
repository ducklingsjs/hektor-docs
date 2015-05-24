# exec

## Implementation status

### Gulp: Implemented
### Grunt: None

## Subtasks

  * [exec](exec.md)

## Options

  * jshint
    * which jshint file should be used
    * set to a falsy value to disable
    * default: ``".jshintrc"``
  * reportFolder
    * the folder where the report will be generated
    * default: ``"reports"``
  * name
    * the project name in the report
    * default: ``"ProjectName"``
  * excludes
    * list of folders to exclude from the report
    * default: ``"<%= paths.app %>/bower_components/*|<%= paths.app %>/scripts/vendor/*"``
  * path
    * path that should be analyzed
    * default: ``"<%= paths.app %>/*"``
