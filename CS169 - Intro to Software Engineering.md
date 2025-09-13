
### HTTP Error Codes
There are series of error codes such as the 200, 300, 400, and 500 series, often denoted as 2xx

2XX: Success
3XX: Redirection (action required)
	301: moved permanently
	302: found a temp redirect
	304: not modified, resource is available in cache
4XX: Client-side error
5XX: Server-side error

### Cookies
HTTP is stateless, it cannot remember your credentials or if you've logged in before.

We can implement states by using cookies to store our data and state

### CURL Commands

This command just accesses the base url

```
curl <base url>
```

but we can do a lot more

```
curl -v <base url>
```
This allows us to print out the request headers

```
curl -v -b <base url> 
```
Makes sure to use cookies if there are any

```
curl <base url>/<route>
```
Access different routes of the base urll

