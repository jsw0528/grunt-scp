# grunt-scp

> Copy files to remote server

## Getting Started

This plugin requires Grunt `~0.4.0`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-scp
```

One the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-scp');
```

## The "scp" task

### Overview

In your project's Gruntfile, add a section named `scp` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
  pkg: grunt.file.readJSON('package.json'),

  scp: {
    options: {
        host: 'localhost',
        username: 'username',
        password: 'password'
    },
    your_target: {
        files: [{
            cwd: 'directory',
            src: '**/*',
            // path on the server
            dest: '/home/username/static/<%= pkg.name %>/<%= pkg.version %>'
        }]
    },
  },
})
```

### Options


#### options.host
Type: `String`
Default value: `localhost`

A string value that is the host of the server.

#### options.port
Type: `Number`
Default value: `22`

The ssh port of the server.


#### options.username
Type: `String`

The username of the server.


#### options.password
Type: `String`

The password of the user on the remote server.


## Changelog

**2013-03-29** `0.1.1`

Add client.on('error') handler.

**2013-03-08** `0.1.0`

First version.
