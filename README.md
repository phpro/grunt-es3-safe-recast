# grunt-es3-safe-recast

> Recasts all ECMA3 reserved words to their safe alternatives.

## Getting Started
This plugin requires Grunt `^1.0.1`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-es3-safe-recast --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-es3-safe-recast');
```

## The "es3_safe_recast" task

### Overview
In your project's Gruntfile, add a section named `es3_safe_recast` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
  es3_safe_recast: {
    options: {
      // Task-specific options go here.
    },
    your_target: {
      // Target-specific file lists and/or options go here.
    },
  },
});
```

### Options

#### trailingComma
Type: Boolean  
Default value: `false`

Whether to remove trailing commas from array and object literals.

### Usage Examples

#### Default Options
In this example the incompatible methods and parameters are compiled and merged into a compatible javascript file. Also, trailing commas in array and object literals are removed.

```js
grunt.initConfig({
  es3_safe_recast: {
    options: {
      trailingComma: true
    },
    files: [
      {
        src: [
          'test/fixtures/incompatible-methods.js',
          'test/fixtures/incompatible-parameters.js',
        ],
        dest: 'tmp/compatible.js',
      },
    ],
  },
});
```

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/).

## Release History
```
2014-07-11    v0.1.0    Basic version based on es3-safe-recast
2015-06-24    v0.1.1    Fix peerDependencies error in newest npm versions.
2015-06-24    v0.1.2    Upgrade es3-safe-recast version.
2018-02-09    v1.0.0    Upgrade es3-safe-recast, add trailingComma option
2018-02-28    v1.0.1    Update to new repo location, add author
```
