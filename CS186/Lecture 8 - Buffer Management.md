
Buffer manager (RAM) is the connection between the file manager and disk. It's job is to move data from disk to the files on your desktop.

The buffer manager is organized into frames. Each frame may store a page.
![[Pasted image 20250325113657.png]]

APIs
- Read page
	- Request to read page 1
	- Does page 1 exist in RAM?
	- If not -> retrieve from disk
- Write page

A **dirty page** is a page that is modified in ram (the page in ram is not the same as the page in disk)

How do we handle dirty pages?

Dirty bit on page --like CS61C!
Write back to disk manager

![[Pasted image 20250325114744.png]]
Pin count: if the page needs to be queried (we need the page for something), it can be pinned). Now, during the replacement cycle, we look for a unpinned frame for replacement

Replacement happens when a requested page is not in the buffer pool

**When a page is requested**
if requested page is not in pool:
- Choose un-pinned frame for replacement
- If frame is dirty -> write current page to disk and mark clean (not dirty)
- Read requested page into frame
Pin the page and return its address

Page Replacement Policy