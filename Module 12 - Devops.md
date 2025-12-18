
OKAY you've deployed your app, so now what?

## The three tier architecture
1. Presentation tier (web server)
	1. Handles HTTP requests and serves the statics assets suhc as images and stylesheets to the user
2. Logic tier (application)
	1. Hosts your application
	2. computes the logic to fulfill the HTTP requests
3. Persistence tier (database)
	1. databases guarantees data remains safe through crashes and unexpected errors
	2. Organizes the data for easy write and read access


## Feature flags
If we need to make changes to a integral part of the architecture (such as the schema of the database) and not affect the user experience. We can either:
1. bring the application offline to make the changes
2. split code paths to not use the part that is down so the application can keep running