
A program that allows us to run a series of terminal commands at once. 

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
	command(s)

