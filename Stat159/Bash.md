
## Getting Started

Ends in .sh extension
hello.sh

Example script
```
echo "Running python script"
python3 hello.py
echo "Running R script"
Rscript greet.py Alice
```


## Running a Bash Script

In order to run, we need to make sure the bash script is executable.

Check with 
```
ls -l
```

if it is read only "r", we need to change the mod to executable "x"
```
chmod +x filename
```

Now run the  bash script
```
./script.sh
```

## Limitations
It always runs everything, even when nothing changed.
Solution: use [[Make]]