Web API using ASP.NET (6.0) core controllers

# To build and run the program

Run the following commands:

1. `dotnet run`

Open another terminal with the app running:
 
2. `httprepl https://localhost:{PORT}`

3. `connect https://localhost:{PORT}`

4. `cd Pizza`

5. `ls`

6. Perform CRUD Operations:

Create a new pizza item:
`post -c "{"name":"Hawaii", "isGlutenFree":false}"`

Preceding command returns the pizza:

```
HTTP/1.1 201 Created
Content-Type: application/json; charset=utf-8
Date: Fri, 02 Apr 2021 23:23:09 GMT
Location: https://localhost:{PORT}/Pizza?id=3
Server: Kestrel
Transfer-Encoding: chunked

{
    "id": 3,
    "name": "Hawaii",
    "isGlutenFree": false
}
```

Update pizza item with id=3:
`put 3 -c  "{"id": 3, "name":"Hawaiian", "isGlutenFree":false}"`

Get the pizza item with id=3:
`get 3`

Delete the pizza item with id=3:
`delete 3`


