# README

Without token
```
curl http://localhost:3000/items
{"error":"Not authorized"}
```

With token
``` request a token
curl -H "Content-Type: application/json" -X POST -d '{"email":"example@email.com","password":"password"}' http://localhost:3000/authenticate

{"auth_token":"eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoxLCJleHAiOjE1Njk3NDE4NTd9.liNetMljz6-RgSSXF2Q0TgFqobvhPumde5uEy6Z6asc"}
```

``` request a resource
curl -H "Authorization: eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoxLCJleHAiOjE1Njk3NDE4NTd9.liNetMljz6-RgSSXF2Q0TgFqobvhPumde5uEy6Z6asc" http://localhost:3000/items
[{"id":1,"name":"item 1","description":"item 1","created_at":"2019-09-28T07:26:18.576Z","updated_at":"2019-09-28T07:26:18.576Z"}]%
```

test13
