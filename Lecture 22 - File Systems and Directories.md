
## Components of File System
Directory, file header, data storage blocks, free space map

Filename/filepath -> file number (index to file header/inode)

### Inode
Stores pointers to data storage blocks

inode structure: 
- file metadata
- direct pointers
- indirect pointers
- double indirect pointers
- triple indirect pointers


## Directory
A director is just a file but contains <filename:filenumber> mappings


### File Allocation Table (FAT)
![[Pasted image 20260421163647.png|697]]
Fat entries are index of disk blocks

The root index (file number) links to the next block

## Berkeley FFS (Fast File System)
Underlying structure is an array of inodes
- metadata
- direct pointers
- indirect pointers

inumbers - file numbers/index of inode

**Helpful for