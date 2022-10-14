# asdf cheat sheet

## asdf commands

```text
# install an asdf plugin
asdf plugin add <plugin_name>

# list all the installed plugins
asdf plugin list

# list all the available versions that the plugin can install
asdf list all <plugin_name>

# show latest stable version
asdf latest <plugin_name>

# show latest stable version that begins with a given string
asdf latest <plugin_name> <version>

# install a specific version of the tool. It can be used 'latest' to install the latest version
asdf install <plugin_name> <version>

# list all the installed versions of a tool
asdf list <plugin_name>

# filter versions to those that begin with a given string
asdf list <plugin_name> <version>

# define a tool version to be used globally. It can be used 'latest' to install the latest version 
asdf global <plugin_name> <version>

# view current version of all installed tools
asdf current

# view current version of a specific tool
asdf current <plugin_name>

# uninstall a version
asdf uninstall <plugin_name> <version>

# locate the binary of an installed tool
asdf which <plugin_name>
asdf where <plugin_name>

```

## References

* [getting started](https://asdf-vm.com/guide/getting-started.html)
* [introduction](https://asdf-vm.com/guide/introduction.html)
* [plugins list](https://github.com/asdf-vm/asdf-plugins/tree/master/plugins)
* [manage versions](https://asdf-vm.com/manage/versions.html)
* [configuration](https://asdf-vm.com/manage/configuration.html)
