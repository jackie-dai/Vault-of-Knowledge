
## Architeture Definition

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

**Convention over configuration**
Rails requires specific naming convention for files because it will use the filename to make connections and execute the application

Each controller selects one view