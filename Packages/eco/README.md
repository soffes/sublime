Syntax highlighting for [Eco](http://github.com/sstephenson/eco) *Embedded CoffeeScript Templates* in [Sublime Text 2](http://www.sublimetext.com/)

It is based on an edited version the HTML (RAILS) Syntax from the [rails textmate bundle](https://github.com/drnic/ruby-on-rails-tmbundle).

## Installation

* First, install [Package Control](http://wbond.net/sublime_packages/package_control/installation).

  > The following instructions are temporary until sublime-eco is added to the package control source repository.

* Hit `command+shift+p` and type `"Package Control: Add Repository"` and hit `return`
* Enter `https://github.com/davidjrice/sublime-eco.git` in the sublime console that appears and hit `return`.
* Now the repository is available, follow the rest of the instructions below to install the package.

  > The following instructions will be all that's necessary after sublime-eco is available through package control directly.

* Hit `command+shift+p` and type `"Package Control: Install Package"` and hit `return`
* Type "eco", this package should appear in the dropdown, select it from the list and hit `return`

## Optional

To get "Textmate ERB Style" opening and closing of ECO blocks. You will also want to;

* Install [SublimeERB](https://github.com/eddorre/SublimeERB#installation)

You should then open your `Preferences -> Keybindings - User` and add the key binding for the ERB command.

The simple option is to allow this command in any file.

```javascript
[
  { "keys": ["ctrl+shift+."], "command": "erb" }
]
```

However if you're like me you may want to restrict the key binding to those files where it makes sense to have that command. (Note the added text.html.eco at the end of the string)

```javascript
[
  { "keys": ["ctrl+shift+."], "command": "erb", "context":
    [
      { "key": "selector",
        "operator": "equal",
        "operand": "text.html.ruby, text.haml, source.yaml, source.css, source.scss, source.js, source.coffee, text.html.eco" }
    ]
  }
]
`