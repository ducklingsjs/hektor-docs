# sequence

## Implementation status

### Gulp: Implemented
### Grunt: None

## Options

  * tasks
    * array of tasks that should be executed
    * tasks will be executed one after other
    * if multiple tasks are inside of an array, they will be executed in parallel, e.g. ``['lint', ['styles', 'scripts'], 'minify']`` will execute styles and scripts tasks in parallel, but the minify task will wait for both of them to finish
    * default: ``[]``

## Common use case

Most common use cases will be to make complex tasks, e.g. build, that make use of all the other tasks. To use more sequence tasks, check out how to rename the tasks in the [main README](../README.md#how-to-rename-the-task-or-have-multiple-similar-tasks).
