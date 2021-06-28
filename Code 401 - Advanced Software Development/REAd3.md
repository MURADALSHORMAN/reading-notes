## How Node JS middleware Works?

Middleware functions are functions that have access to the request object (req), the response object (res), and the next middleware function in the application’s request-response cycle. The next middleware function is commonly denoted by a variable named next.

- As name suggests it comes in middle of something and that is request and response cycle
- Middleware has access to request and response object
- Middleware has access to next function of request-response life cycle

![](https://miro.medium.com/max/2002/1*wIkLR_9twvmG-LitHYoftw.png)

Middleware functions can perform the following tasks:
- Execute any code.
- Make changes to the request and the response objects.
- End the request-response cycle.
- Call the next middleware in the stack.
If the current middleware function does not end the request-response cycle, it must call next() to pass control to the next middleware function. Otherwise, the request will be left hanging.



## What is this next()?
A middleware is basically a function that will the receive the Request and Response objects, just like your route Handlers do. As a third argument you have another function which you should call once your middleware code completed. This means you can wait for asynchronous database or network operations to finish before proceeding to the next step. This might look like the following:

![](https://miro.medium.com/max/700/1*ptNjzuT0m2BQ9YpQTVwVLg.png)


## Types of express middleware
- Application level middleware app.use
- Router level middleware router.use
- Built-in middleware express.static,express.json,express.urlencoded
- Error handling middleware app.use(err,req,res,next)
- Thirdparty middleware bodyparser,cookieparser


Application Level Middleware
Example 1 : Auth middleware
Suppose we are having five routes getUsers,getDetails,updateDetails,isLoggedIn,isLoggedOut
every route must be authenticated if the user is not authenticated then he is not able to call the above mentioned routes,so every GET,POST calls required authentication.In this case we build a authtication middleware.
Now once the request comes the auth middleware will do some authentication logic that we have written inside it.Once authentication successful then remaining routed must be called using next()
if auth fails then it wont perform next route exit the middleware with error response logic

![](https://miro.medium.com/max/2284/1*fbe04fcynkBuLo_CADxxHQ.png)


```
const express = require('express');

// custom middleware create
const LoggerMiddleware = (req,res,next) =>{
    console.log(`Logged  ${req.url}  ${req.method} -- ${new Date()}`)
    next();
}

const app = express()

// application level middleware
app.use(LoggerMiddleware);


// users route
app.get('/users',(req,res)=>{
    res.json({
        'status':true
    })
})


// save route
app.post('/save',(req,res)=>{
    res.json({
        'status':true
    })
})

app.listen(3002,(req,res)=>{
    console.log('server running on port 3002')
})
```


# Router Level Middleware

Router-level middleware works in the same way as application-level middleware, except it is bound to an instance of express.Router().
```
const router = express.Router()
```
Load router-level middleware by using the router.use() and router.METHOD() functions.

```
const express = require('express');

const app = express();

const router = express.Router()

router.use((req,res,next)=>{
    console.log("Time:",new Date())
    next()
})


router.get("/user/:id",(req,res,next)=>{
    console.log('Request URL:', req.originalUrl)
    next()
},(req,res,next)=>{
    console.log('Request Type:', req.method)
    next()
},(req,res)=>{
    res.json({
        status:true,
        id:req.params.id
    })
})


app.use('/',router)

app.listen(3000,(req,res)=>{
    console.log('server running on 3000')
})
```

