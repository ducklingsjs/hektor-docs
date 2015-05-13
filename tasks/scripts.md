# scripts

## Status: Not yet implemented

## Subtasks

  * browserify
  * babelify
  * aliasify
  * hbsfy

## Options

  * src
    * entry point
    * default: {app}/scripts/main.js
  * filename
    * destination filename
    * default: main.js
  * moduleSystem
    * default: browserify
    * possible: browserify, requirejs
  * transpiler
    * default: none
    * possible: none, babel
  * templates
    * default: handlebars
  * dest
    * destination path
    * default: .tmp/scripts
  * debug
    * should the sourcemaps be generated
    * default: false
  * moduleSystemConfig
    * aliasify
      * options passed to aliasify module (if browserify used)
      * default: {}
    * nodePath
      * used node paths for browserify
      * default: process.env.NODE_PATH:./{app}/scripts
  * transpilerOptions
    * options passed to transpiler module (if used)
    * default: {}