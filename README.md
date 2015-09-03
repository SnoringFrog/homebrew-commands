A collection of custom commands for the [Homebrew](http://brew.sh/) package manager.

-----

# Commands

- [brew executables](#brew-executables)

# Installation

Clone the repo, then copy the commands you want to use to any directory in your `$PATH`. 

-----

## brew executables

### Usage

    brew executable formula_name

### Description
Returns a list of commands associated with an installed formula. Only considers the version currently in use (for now). Removes the need to `brew unlink <formula> && brew link --verbose <formula>` to see what commands were included in a formula. However, if you don't want to use this command, here's a line you can paste into the terminal to get a rougher version of the same info `brew executables` provides:

```sh
formula="formulaYouWant"; brew unlink $formula && brew link --verbose $formula | grep "$(brew --prefix)/bin"
```

### Exit codes

*  0: No error
*  1: No argument supplied
*  2: Formula not installed
