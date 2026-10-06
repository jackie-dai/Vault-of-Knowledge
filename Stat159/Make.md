
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

make sure you are using relative filepaths
A command can consist of multiple commands by using &&
```
cd code && python3 plot.py
python3 code/plot.py # equivalent
```

## PHONY Targets
Bundles commands so that you can easily execute a series of commands, labeled as a action
common phony targets: clean, all, setup, help

if you create a phony action, you also need to include the name at the top after .PHONY: action_name

.PHONY:  all, clean

all: target1 target2 <- all runs all these targets every time you run make

clean:    
	command(s) - usually remove commands like 
	rm -f filename1



comment with \#
```
# this is a comment
```

## Automatic Variables
These variables can be used within each recipe and is refreshed per recipe.

```
$^
```
list of all the dependencies

```
$<
```
name of the 1st dependency

```
$@
```
 target

```
# rule 1
report.pdf: intro.md results.md conclusion.md
	pandoc $^ -o $@ 
```
the variables become set to the values above

## User Defined Variables
 
Defined at the top of the script and used like a regular variable $(variable_name)
```
PYTHON = python3
SRC_DIR = src
DATA_DIR = data

# rule 1
results.pdf: script.py 
	$(PYTHON) script.py
```
Can be set to any value or command

# $.
wildcard to refer to name of the same extension 

```
.PHONY : outputs clean

outputs: isles.dat abyss.dat last.dat sierra.dat 

%.dat: books/%.txt
	python countwords.py $^ $@
```

```
.PHONY : outputs clean

outputs: isles.dat abyss.dat last.dat sierra.dat 

isles.dat : books/isles.txt
	python countwords.py $^ $@

abyss.dat : books/abyss.txt
	python countwords.py $^ $@

last.dat: books/last.txt
	python countwords.py $^ $@

sierra.dat: books/sierra.txt
	python countwords.py $^ $@

clean :
	rm -f *.dat
```