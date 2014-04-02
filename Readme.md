*This repository is a mirror of the [component](http://component.io) module [visionmedia/node-querystring](http://github.com/visionmedia/node-querystring). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/visionmedia-node-querystring`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*
# node-querystring [![Build Status](https://travis-ci.org/visionmedia/node-querystring.png?branch=master)](https://travis-ci.org/visionmedia/node-querystring)

  query string parser for node and the browser supporting nesting, as it was removed from `0.3.x`, so this library provides the previous and commonly desired behaviour (and twice as fast). Used by [express](http://expressjs.com), [connect](http://senchalabs.github.com/connect) and others.

## Installation

    $ npm install qs

## Examples

```js
var qs = require('qs');

qs.parse('user[name][first]=Tobi&user[email]=tobi@learnboost.com');
// => { user: { name: { first: 'Tobi' }, email: 'tobi@learnboost.com' } }

qs.stringify({ user: { name: 'Tobi', email: 'tobi@learnboost.com' }})
// => user[name]=Tobi&user[email]=tobi%40learnboost.com
```

## Testing

Install dev dependencies:

    $ npm install -d

and execute:

    $ make test

browser:

    $ open test/browser/index.html
