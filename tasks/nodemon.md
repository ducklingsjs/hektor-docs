# nodemon

## Implementation status

### Gulp: Implemented
### Grunt: None

## Options

  * script
    * the script that nodemon should start
    * default: ``"index.js"``
  * ext
    * the watched extensions
    * default: ``"js"``
  * ignore
    * paths that should be ignored
    * default: ``[
      '.tmp/',
      '<%= paths.app %>/',
      '<%= paths.dist %>/',
      'node_modules/'
    ]``
  * tasks
    * tasks that should run on change
    * default: ``null``
  * env
    * defined envirnoment variables
    * default: ``{}``
