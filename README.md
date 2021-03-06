<h1 align="center">
  <img src="http://usbac.com.ve/images/Tundra.svg" alt="Tundra title" width="150">
  <br>
  Tundra
  <br>
</h1>

<p align="center">The comprehensive template engine for Nodejs.</p>

<p align="center">
    <img src="https://img.shields.io/badge/stability-stable-green.svg">
    <img src="https://img.shields.io/badge/coverage-100%25-green">
    <img src="https://img.shields.io/badge/version-1.2.0-blue.svg">
    <img src="https://img.shields.io/badge/license-MIT-orange.svg">
</p>

Tundra is a small, fast, customizable and easy to use template engine for Nodejs. It perfectly integrates with any back-end made in Js, even pure Nodejs.

## Features

* Easy to learn and with a small codebase.

* Cache system for speeding up the loading of views.

* Standard library with useful functions.

* Customizable syntax.

* Inheritance capabilities.

* Reusable code blocks.

* And more...

## Code snippets

```html
{{ print_variable }}

{! print_variable_without_escaping_it !}

{# comment #}

{% var code_inside_this_tags = true %}

~{{ escape_template_tags }}

@require(imported_view.html)

@spread(hello)

{[ spread hello ]}
{[ endspread ]}

@extends(parent_view.html)

{[ block name ]}
    {[ parent block_name ]}
{[ endblock ]}
```

## Example

Rendering a view in pure Nodejs is this simple:

main.js:

```js
var http = require('http');
var Tundra = require('tundrajs');
var view = new Tundra();

http.createServer((req, res) => {
    let data = {
        title: 'Tundra',
        msg: 'Hello World!'
    };

    view.render(res, 'home.html', data);
    res.end();
}).listen(8080);
```

home.html:
```html
<!DOCTYPE html>
    <head>
        <title>{{ title }}</title>
    </head>
    <body>
        {{ msg }}
    </body>
</html>
```

## Tests

To run the test suite, follow these steps:

1. Open your terminal and move to your Tundra folder.

2. Run `npm update --save-dev` to install the dependencies.

3. Run `npm test`.

## Documentation

The documentation is available at the [wiki page](https://github.com/Usbac/tundra/wiki).

* [General usage](https://github.com/Usbac/tundra/wiki/General)

* [Standard library](https://github.com/Usbac/tundra/wiki/Standard-library)

* [Syntax](https://github.com/Usbac/tundra/wiki/Syntax)

* [View inheritance](https://github.com/Usbac/tundra/wiki/Syntax)

## Contributing

Any contribution or support to this project in the form of a issue, pull request or message will be highly appreciated. ❤️

Don't be shy :)

## License

Tundra is open-source software licensed under the [MIT license](https://github.com/Usbac/Tundra/blob/master/LICENSE).
