# rev

## Implementation status

### Gulp: None
### Grunt: None

## Options

  * src
    * source path
    * default: ``"<%= paths.dist %>/**(?!html)$"``
    * default value explanation: all files in dist, except for the ones ending in .html
  * dest
    * destination folder
    * if left empty, it will save to the same folder
    * default: ``null``
  * delete
    * should the original files be deleted
    * useful if destination is the same folder
    * default: ``true``
