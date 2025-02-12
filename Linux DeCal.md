
Lecture 2 - Shell Scripting

**How to copy file in cd and prepend new**
for FILE in $(ls *)
do 
	cp $FILE new_$FILE
done