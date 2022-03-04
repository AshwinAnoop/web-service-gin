# Basic working of RESTful API with Go and Gin 

A basic RESTful web service API with Go and the Gin Web Framework (Gin), which consist of the following sections:

* Handler to return all items
* Handler to add a new item
* Handler to return a specific item




## Running the code

At the command line, use go get . to get/download dependencies for code in the current directory.

```bash
$ go get .
```

use go run . to run code in the current directory

```bash
$ go run .
```

#### to return all items

use curl in another terminal to make a request to your running web service

```bash
$ curl http://localhost:8080/albums
```
The command should display all the data you seeded the service with.

#### to add a new item

use curl to make a request to your running web service

```bash
$ curl http://localhost:8080/albums \
    --include \
    --header "Content-Type: application/json" \
    --request "POST" \
    --data '{"id": "4","title": "The Modern Sound of Betty Carter","artist": "Betty Carter","price": 49.99}'
```

The command should display headers and JSON for the added album.

#### to return a specific item

```bash
$ curl http://localhost:8080/albums/2
```
The command should display JSON for the album whose ID you used. If the album wasn’t found, you’ll get JSON with an error message.





For more detailed reference : [web-service-gin-tutorial](https://go.dev/doc/tutorial/web-service-gin)
