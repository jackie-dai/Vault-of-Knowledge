
## The Architecture

**Model:** manipulates data and handle incoming requests
**View:** the interface the user interacts with
**Controller**: facilitates the interaction between view and model 

## Databases
Rails model operates on a database implementing the Active Record architectural pattern

What are the built in operations the model has: **CRUD**
**C**reate a new row in the table
**R**ead an existing row into a single object instance
**U**pdate an existing row with new attribute values from a modified object instance
**D**elete a row

\newpage

---
**Convention over configuration**
Rails requires specific naming convention for files because it will use the filename to make connections and execute the application. Mapping RESTful actions to controller action method names

---
## Controllers and Views

Web browsers can only generate HTTP Get and Post requests but rails defines seven routes:
1. Index
2. New
3. Create
4. Show
5. Edit
6. Update
7. Destroy

Each controller selects one view

---

How do we receive data from the user?
### Forms!
First we need to display the form for the user to fill out. This can be done with the *new* action.
Submitting a form will invoke the *create* action. Each form 

**Flash[]** - holds data from the current request to (only) the very next action.
	this is helpful for redirects after the submission of a form. HTTP is stateless so data does not persist between redirects. We can hold user data in flash[] to display a success confirmation after the form submission
