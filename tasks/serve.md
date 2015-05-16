# serve

## Implementation status

### Gulp: None
### Grunt: None

## Subtasks

  * watch

## Options

  * server
    * default: ``"connect"``
    * possible: ``"connect"``, ``"nodemon"``
  * watch
    * default:
        ```
        {
          {
            path: "<%= paths.app %>/styles/{,**/}*.scss",
            tasks: ["styles"]
          }, {
            path: "<%= paths.app %>/scripts/{,**/}*.{js,hbs}",
            tasks: ["scripts"]
          }
        }
        ```
