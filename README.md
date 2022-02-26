#### Simple HTTP Web Server / REST API

Build The Program

```bash
go build
```

Run The Binary

```bash
./golang-http-server-rest-api
```

Now the REST API / HTTP Server Will Be Running on `http://localhost:9000`

#### Web UI

UI Can Be Accessed On `http://localhost:9000/home`

#### Testing Using `curl` HTTP Client
#### Check API Health/Status (HTTP GET)

```bash
curl -H "accept:application/json" -H "content-type:application/json" -X GET http://localhost:9000/api/health 2>/dev/null | python -m json.tool
```

Response

```json
{
    "ok": true
}
```

#### HTTP GET Request

```bash
curl -H "accept:application/json" -H "content-type:application/json" -X GET http://localhost:9000/api/v1/getData 2>/dev/null | python -m json.tool
```

Response

```json
{
    "error": "",
    "serverResponse": {
        "_id": "6219dd7e3fd9fb007a4d6fe7",
        "about": "Laborum pariatur fugi",
        "address": "460 Dahlgreen Place, Fedora, Kansas, 9718",
        "age": 21,
        "balance": "$1,995.17",
        "company": "KAGE",
        "email": "bridgettegriffin@kage.com",
        "eyeColor": "blue",
        "favoriteFruit": "strawberry",
        "friends": [
            {
                "id": 0,
                "name": "Serena Davis"
            }
        ],
        "gender": "female",
        "greeting": "Hello, Bridgette Griffin! You have 5 unread messages.",
        "guid": "b4dd0bf4-dbff-44bd-a1af-a5a6fb44231a",
        "index": 0,
        "isActive": "false",
        "latitude": 12.471153,
        "longitude": 118.329655,
        "name": "Bridgette Griffin",
        "phone": "+1 (811) 510-3853",
        "picture": "http://placehold.it/32x32",
        "registered": "2018-07-28T02:25:46 +07:00",
        "tags": [
            "labore",
            "magna",
            "do"
        ]
    }
}
```

#### HTTP POST Request

```bash
curl -H "accept:application/json" -H "content-type:application/json" -d '{"length1": 15, "length2": 25}' -X POST http://localhost:9000/api/v1/processData 2>/dev/null | python -m json.tool
```

Response

```json
{
    "error": "",
    "serverResponse": [
        "Xl3Cd4Zj9ie9j4S",
        "aJmKXHRUzFZyWXu6wegiEXEmO"
    ]
}
```