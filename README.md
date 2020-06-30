# [NGROK server](https://ngrok.com/) - secure introspectable tunnels to localhost

Ngrok tunnels for localhost + JSON server

---------------------------
Init project & install dependencies
``` 
npm init
npm i json-server ngrok
npm audit fix
```

Create a db.json file with some data
``` 
// db.json

{
  "posts": []
}
```

Customize package.json
``` 
// package.json

  "scripts": {
    "db": "json-server -w db.json -p 3001",
    "tunnel": "ngrok http 3001 "
  },
```

Terminal #1
``` 
npm run db
```

Terminal #2
``` 
npm run tunnel
```

-------------------

Result:

``` 
> json-server -w db.json -p 3001


  \{^_^}/ hi!

  Loading db.json
  Done

  Resources
  http://localhost:3001/posts

  Home
  http://localhost:3001

  Type s + enter at any time to create a snapshot of the database
  Watching...

```

``` 
ngrok by @inconshreveable         

Session Status                online                                                                                                                        
Session Expires               7 hours, 59 minutes                                                                                                           
Version                       2.3.35                                                                                                                        
Region                        United States (us)                                                                                                            
Web Interface                 http://127.0.0.1:4040                                                                                                         
Forwarding                    http://14b09b91c21e.ngrok.io -> http://localhost:3001                                                                         
Forwarding                    https://14b09b91c21e.ngrok.io -> http://localhost:3001     
```
