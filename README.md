##List of commands and procedure for setting up the server and running it.

A. Creating a controller command:
node ace make:controller ControllerName

## To Add Auth middleware, first:
1. Register the auth inside the start/kernel.ts file by adding the code:
```
Server.middleware.RegisterNamed({
    auth: 'App/Middleware/Auth'
})

```

2. Once the middleware is registered, it can be used into the routes like:
```
Route
.get('/dashboard', 'DashboardController.index')
.middleware('auth')
```