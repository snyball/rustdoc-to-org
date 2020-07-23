# Rustdoc to org
A Pandoc filter that converts rust documentation to .org-files! This is still in a very early state, but hopefully this can end up helping someone.
![Demo with helm ag](demo.gif)

## Installation

* Install Pandoc https://pandoc.org/
* Install ripgrep https://github.com/BurntSushi/ripgrep#installation
* Install helm-ag https://github.com/bridgesense/emacs-helm-ag
* Copy `rustdoc-to-org-mode.el` and load it with `(load-file rustdoc-to-org-mode.el)`
* Generate all `.html` files for std by running `rustup doc`, which will put the files somewhere in `~/.rustup/`, in my case in `~/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/share/doc/rust/html/std/)`. You can also convert docs generated by `cargo doc`
* Run `M-x rustdoc-to-org--convert-directory` to convert all `.html` files in a directory.
* You can now use `C-c C-d` to run `search-rustdoc`.

## Development

* Install Haskell Stack https://docs.haskellstack.org/en/stable/README/
* Clone the project and get started!

## TODO

* Figure out a way to get links working. All links point to .html files, they should be updated to point to .org files.
* Make code not awful and not slow.
* Pandoc seems to be keen on inserting extra linebreaks between sections. For example, there is an extra linebreak after each header. It would be nice to remove this.
* There is a redundant title string before the actual Header title, which should be removed.
* Fill out this list.

All suggestions, comments and more are welcomed!
