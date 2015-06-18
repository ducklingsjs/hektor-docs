# copy

## Implementation status

### Gulp: Implemented
### Grunt: None

## Options
  dest: '<%= paths.dist %>',
  paths: [
    '<%= paths.app %>/fonts',
    '<%= paths.app %>/images'
  ]

  * dest
    * destination folder
    * default: ``"<%= paths.dist %>"``
  * paths
    * array of files and folders that should be copied
    * defaults: ``["<%= paths.app %>/fonts", "<%= paths.app %>/images"]``
