
A program that allows us to run a series of terminal commands at once. Similar to bash, but make is useful because it will only run commands if there has been a modification since the last time it was run.

## Getting Started

In order to make a make file, it must be named: Makefile

### General Template

\# rule 1
Target: dependencies
	command(s) <- indent/tab is important
```
pandoc doc.md -o doc.html
pandoc doc.md -o doc.pdf
```
executes two commands to export to html and pdf

*Running make without the dependencies still work, but without the dependencies listed, make won't know to rerun when changes have been made to one of the dependencies*

## PHONY Targets
Bundles commands so that you can easily execute a series of commands, labeled as a action
common phony targets: clean, all, setup, help

if you create a phony action, you also need to include the name at the top after .PHONY: action_name

.PHONY:  all, clean

all: filename1 filename2

clean:
	command(s) - usually remove commands like 
	rm -f filename1



comment with \#
```
# this is a comment
```