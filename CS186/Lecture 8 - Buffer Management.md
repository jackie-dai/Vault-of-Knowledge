
Buffer manager (RAM) is the connection between the file manager and disk. It's job is to move data from disk to the files on your desktop.

The buffer manager is organized into frames. Each frame may store a page.
![[Pasted image 20250325113657.png]]

APIs
- Read page
	- Request to read page 1
	- Does page 1 exist in RAM?
	- If not -> retrieve from disk
- Write page

How do we handle dirty pages?
