
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