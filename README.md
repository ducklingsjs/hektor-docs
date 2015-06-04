# Common docs for [hektor-grunt](https://github.com/infinumjs/hektor-grunt) &amp; [hektor-gulp](https://github.com/infinumjs/hektor-gulp)

## Tasks
* [styles](tasks/styles.md)
* [scripts](tasks/scripts.md)
* [connect](tasks/connect.md)
* [nodemon](tasks/nodemon.md)
* [serve](tasks/serve.md)
* [codecheck](tasks/codecheck.md)
* [minify](tasks/minify.md)
* [clean](tasks/clean.md)
* [exec](tasks/exec.md)
* [plato](tasks/plato.md)
* [replace](tasks/replace.md)
* [rev](tasks/rev.md)
* [sequence](tasks/sequence.md)

## How to rename the task (or have multiple similar tasks)
In some cases you might need multiple similar tasks (e.g. connect-dev, connect-test, connect-dist).
Every task can be renamed, so there shouldn't be a problem creating multiple tasks with different names.
When you are defining the config of the task, use the desired task name as the object key, but set the moduleName property to the name of the task module.

### Example

    {
      connect: {}, // Default options
      'connect-dist': {
        moduleName: 'connect',
        root: ['dist'],
        port: 8080,
        livereload: false
      },

      serve: {}, // Will default to 'connect'
      default: {
        // Use serve as default task
        moduleName: 'serve',

        // Serve the dist version
        server: 'connect-dist'
      },

      build: {
        moduleName: 'sequence',
        tasks: ['styles', 'scripts', 'codecheck', 'minify', 'rev']
      }
    }


### Status

Implemented in hektor-gulp
