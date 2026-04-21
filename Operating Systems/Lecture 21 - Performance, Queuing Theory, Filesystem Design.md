
## Introduction to Queuing Theory

### Little's Law
Average arrival rate = average departure rate
"What comes in must come out"

$$
L_Q=\lambda T_Q
$$
## Disk Management
Accessed as linear array of sectors

## File Allocation Table (FAT)
Files are a collection of disk blocks

FAT is a linked list. In order to access a file, we translate the path to a file number. The file number is the index of the head of the linked list for the file. We follow the linked to the disk blocks of the memory.
![[Pasted image 20260417124657.png]]

FAT is stored on the disk.