zshmarks
========

A port of [Bashmarks (by huyng)](https://github.com/huyng/bashmarks) and [zshmarks
](https://github.com/linux-china/zshmarks), a directory bookmarks for the oh-my-zsh

### How to install

* Download the script or clone this repository in [oh-my-zsh](http://github.com/robbyrussell/oh-my-zsh) plugins directory:

        cd ~/.oh-my-zsh/custom/plugins
        git clone https://github.com/linux-china/zshmarks.git

* Activate the plugin in `~/.zshrc`:

        plugins=( [plugins...] zshmarks [plugins...])

* Source `~/.zshrc`  to take changes into account:

        source ~/.zshrc

### Shell Commands

    bookmark      <bookmark_name> - Saves the current directory as "bookmark_name"
    jumpmark      <bookmark_name> - Goes (cd) to the directory associated with "bookmark_name"
    showmark      <bookmark_name> - Prints the directory associated with "bookmark_name"
    showmark                      - Lists all available bookmarks
    deletemark    <bookmark_name> - Deletes the bookmark

### Alias

If you were expecting shorter command, you can setup zshmarks to do what you like.

    alias j="jumpmark"
    alias b="bookmark"
    alias del="deletemark"  # d is conflict with 'dirs -v | head -10' defined in oh-my-zsh
    alias p="showmarks"

### Example Usage

    $ cd /var/www/
    $ b webfolder
    $ cd /usr/local/lib/
    $ b locallib
    $ p
    $ j web<tab>
    $ j webfolder
