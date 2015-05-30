# replace

## Implementation status

### Gulp: Implemented
### Grunt: None

## Options

  * from
    * string, regex or function
    * the string/regex to search for
    * if it's a function it will be called on runtime and should return either string or regex
    * default: ``"{{replaceme}}"``
  * to
    * string or function
    * the replacement string
    * if it's a function it will be called on runtime and it will get the strig to replace as an argument
    * default: ``"Hello world!"``
  * src
    * path to the source files (string or array)
    * default: ``"<%= paths.tmp %>/scripts/main.js"``
  * dest
    * path where te files will be saved
    * if left empty, it will replace the source files
    * default: ``null``
