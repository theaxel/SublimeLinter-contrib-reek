SublimeLinter-contrib-reek
================================

[![Build Status](https://travis-ci.org/theaxel/SublimeLinter-contrib-reek.svg?branch=master)](https://travis-ci.org/theaxel/SublimeLinter-contrib-reek)

***This is a fork, updating it to SublimeLinter v4 and reek v5***

    
This linter plugin for [SublimeLinter][docs] provides an interface to [reek](https://github.com/troessner/reek). It will be used with files that have the `ruby`, `ruby on rails`, `rspec`, `betterruby`, `better rspec`, `ruby experimental` or `cucumber steps` syntaxes.

## Installation
SublimeLinter 4 must be installed in order to use this plugin. If SublimeLinter 4 is not installed, please follow the instructions [here][installation].

### Linter installation
Before using this plugin, you must ensure that `reek` is installed on your system. To install `reek`, do the following:

1. Install [Ruby](http://www.ruby-lang.org).

1. Install `reek` by typing the following in a terminal:
   ```
   [sudo] gem install reek
   ```

1. If you are using `asdf`, `rbenv` or `rvm`, ensure that they are loaded in your shell’s correct startup file. See [here](http://sublimelinter.readthedocs.org/en/latest/troubleshooting.html#shell-startup-files) for more information.

### Linter configuration
In order for `reek` to be executed by SublimeLinter, you must ensure that its path is available to SublimeLinter. Before going any further, please read and follow the steps in [“Finding a linter executable”](http://sublimelinter.readthedocs.org/en/latest/troubleshooting.html#finding-a-linter-executable) through “Validating your PATH” in the documentation.

Once you have installed and configured `reek`, you can proceed to install the SublimeLinter-contrib-reek plugin if it is not yet installed.

### Plugin installation
Please use [Package Control][pc] to install the linter plugin. This will ensure that the plugin will be updated when new versions are available. If you want to install from source so you can modify the source code, you probably know what you are doing so we won’t cover that here.

To install via Package Control, do the following:

1. Make sure you don't have an installed version of `SublimeLinter-contrib-reek`. If you do, _uninstall_ it with Package Control `Remove Package` command
  
2. Within Sublime Text, use Package Control `Add Repository` command (see this [SO](https://stackoverflow.com/questions/23026201/sublime-text-3-how-to-install-plugins-from-github)) - Add https://github.com/theaxel/SublimeLinter-contrib-reek

3. Within Sublime Text, bring up the [Command Palette][cmd] and type `install`. Among the commands you should see `Package Control: Install Package`. If that command is not highlighted, use the keyboard or mouse to select it. There will be a pause of a few seconds while Package Control fetches the list of available plugins.

4. When the plugin list appears, type `reek`. Among the entries you should see `SublimeLinter-contrib-reek`. If that entry is not highlighted, use the keyboard or mouse to select it. You should see this repo `github.com/theaxel/SublimeLinter-contrib-reek` on package entry's _footnote_

## Settings
For general information on how SublimeLinter works with settings, please see [Settings][settings]. For information on generic linter settings, please see [Linter Settings][linter-settings].

You can configure reek exactly the way you would from the command line, using `config.reek` configuration files. For more information, see the [reek documentation](https://github.com/troessner/reek#configuration-file).

By default, the linter plugin looks for a config file called `config.reek` in the current directory and its parents. To override the config file path, you would add this to the linter settings:

```json
"reek": {
    "args": ["-c", "path/to/config.reek"]
}
```

## Contributing
If you would like to contribute enhancements or fixes, please do the following:

1. Fork the plugin repository.
1. Hack on a separate topic branch created from the latest `master`.
1. Commit and push the topic branch.
1. Make a pull request.
1. Be patient.  ;-)

Please note that modifications should follow these coding guidelines:

- Indent is 4 spaces.
- Code should pass flake8 and pep257 linters.
- Vertical whitespace helps readability, don’t be afraid to use it.
- Please use descriptive variable names, no abbreviations unless they are very well known.

Thank you for helping out!

[docs]: http://sublimelinter.readthedocs.org
[installation]: http://sublimelinter.readthedocs.org/en/latest/installation.html
[locating-executables]: http://sublimelinter.readthedocs.org/en/latest/usage.html#how-linter-executables-are-located
[pc]: https://sublime.wbond.net/installation
[cmd]: http://docs.sublimetext.info/en/sublime-text-3/extensibility/command_palette.html
[settings]: http://sublimelinter.readthedocs.org/en/latest/settings.html
[linter-settings]: http://sublimelinter.readthedocs.org/en/latest/linter_settings.html
[inline-settings]: http://sublimelinter.readthedocs.org/en/latest/settings.html#inline-settings
