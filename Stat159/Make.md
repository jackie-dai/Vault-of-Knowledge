
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


.PHONY: [name]

all: filename1 filename2

clean:
	command(s) - usually remove commands like rm -f filename1

comment with \#
```
# this is a comment
```