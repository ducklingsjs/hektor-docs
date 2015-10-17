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
* [copy](tasks/copy.md)
* [zip](tasks/zip.md)
* [custom](tasks/custom.md)

## How to rename the task (or have multiple similar tasks)
In some cases you might need multiple similar tasks (e.g. connect-dev, connect-test, connect-dist).
Every task can be renamed, so there shouldn't be a problem creating multiple tasks with different names.
When you are defining the config of the task, use the desired task name as the object key, but set the moduleName property to the name of the task module.

## Shorthand for the sequence task

Since the [sequence](tasks/sequence.md) task has only one option - an array of tasks that should be executed, and it's a common task, there is a shorthand to define a sequence task.
Insted of this:

    someTaskName: {
      moduleName: "sequence",
      tasks: ["styles", "scripts"]
    }

You can do this:

    someTaskName: ["styles", "scripts"]

## Shorthand for the custom task

If you want to use the [custom task](tasks/custom.md), and don't need the before option, you can use the shorthand. If you have any dependencies, you will also need to load them from inside of the task function.
Instead of this:

    someTaskName: {
      moduleName: 'custom',
      deps: ['a', 'b'],
      task: function(H, options, done) {
        // Do some stuff
      }
    }

You can do this:

    someTaskName: function(H, options, done) {
      H.loadDeps(['a', 'b']);
      // Do some stuff
    }

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
