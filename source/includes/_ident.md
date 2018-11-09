# ident

## Status


```shell
curl -i https://ident.provide.services/status
HTTP/2 204
```

This endpoint checks the status of the ident microservice.

### HTTP Request

`GET /api/vi/status`


## Apps: Get Applications


```shell
curl -i \
    -H 'Authorization: bearer yoUr-AutH-TOKeN-FrOm-sIgnINg-in' \
    https://ident.provide.services/api/v1/applications
HTTP/2 200
```


> The above command returns JSON structured like this:

```json
[
  {
        "id": "cf6ae66a-7cba-48ce-bbd5-9dcd674267be",
        "created_at": "2018-10-09T01:28:52.704799Z",
        "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
        "user_id": "3d9d62e8-0acf-47cd-b74f-52c1f96f8397",
        "name": "Enterprise Advantage",
        "description": null,
        "config": {
            "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4"
        },
        "hidden": false
    },
    {
        "id": "6fd50c17-0d3f-463f-811e-0015e0373f1a",
        "created_at": "2018-10-09T01:30:05.575747Z",
        "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
        "user_id": "3d9d62e8-0acf-47cd-b74f-52c1f96f8397",
        "name": "Process Turbo",
        "description": null,
        "config": {
            "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4"
        },
        "hidden": false
    }
]
```

This endpoint enumerates platform Applications visible to the authorized caller.

### HTTP Request

`GET /api/v1/applications`

## Apps: Post an Application


```shell
curl -i -H 'content-type: application/json' \
    -H 'Authorization: bearer yoUr-AutH-TOKeN-FrOm-sIgnINg-in' \
    https://ident.provide.services/api/v1/applications \
    -d '{"name": "SavvyApp"}'
HTTP/2 201
```


> The above command returns JSON structured like this:

```json
[
  {
    "id": "77cb2094-9a99-4de6-ac86-bbd2353b49c8",
    "created_at": "2018-10-09T02:03:19.617250119Z",
    "network_id": "00000000-0000-0000-0000-000000000000",
    "user_id": "3d9d62e8-0acf-47cd-b74f-52c1f96f8397",
    "name": "SavvyExec",
    "description": null,
    "config": null,
    "hidden": false
}
]
```

This endpoint creates a new Application on behalf of the authorized platform User.

### HTTP Request

`POST /api/v1/applications`

## Apps: Get Application details


```shell
curl -i \
    -H 'Authorization: bearer yoUr-AutH-TOKeN-FrOm-sIgnINg-in' \
    https://ident.provide.services/api/v1/applications/cf6ae66a-7cba-48ce-bbd5-9dcd674267be
HTTP/2 200
```


> The above command returns JSON structured like this:

```json
[
  {
    "id": "cf6ae66a-7cba-48ce-bbd5-9dcd674267be",
    "created_at": "2018-10-09T01:28:52.704799Z",
    "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
    "user_id": "3d9d62e8-0acf-47cd-b74f-52c1f96f8397",
    "name": "Enterprise Advantage",
    "description": null,
    "config": {
        "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4"
    },
    "hidden": false
}
]
```

This endpoint retrieves the details of the specified Application.

### HTTP Request

`GET /api/vi/applications/:id`

### Query Parameters

Parameter | Description
--------- | -----------
id | The ID of the Application to retrieve


## Apps: Update Application details


```shell
curl -i -XPUT \
    -H 'content-type: application/json' \
    -H 'Authorization: bearer yoUr-AutH-TOKeN-FrOm-sIgnINg-in' \
    https://ident.provide.services/api/v1/applications/6fd50c17-0d3f-463f-811e-0015e0373f1a \
    -d '{"name": "Turbo Process"}'
HTTP/2 204
```

This endpoint updates details of the specified Application.

### HTTP Request

`PUT /api/vi/applications/:id`

### Query Parameters

Parameter | Description
--------- | -----------
id | The ID of the Application to retrieve


## Apps: Get Application tokens

```shell
curl -i \
    -H 'Authorization: bearer yoUr-AutH-TOKeN-FrOm-sIgnINg-in' \
    https://ident.provide.services/api/v1/applications/cf6ae66a-7cba-48ce-bbd5-9dcd674267be/tokens
HTTP/2 200
```


> The above command returns JSON structured like this:

```json
[
    {
        "id": "ba562b25-ff4e-4f9d-a332-31550ead9f41",
        "created_at": "2018-10-09T01:28:52.726631Z",
        "issued_at": "2018-10-09T01:28:52.725677Z",
        "expires_at": null,
        "token": "an-apPliCaTIOn-aPi-tOkEn",
        "data": null
    }
]
```

This endpoint fetches the Tokens of the specified Application.

### HTTP Request

`GET /api/vi/applications/:id/tokens`

### Query Parameters

Parameter | Description
--------- | -----------
id | The ID of the Application to retrieve

## Apps: Delete an Application


```shell
curl -i -XDELETE \
    -H 'Authorization: bearer yoUr-AutH-TOKeN-FrOm-sIgnINg-in' \
    https://ident.provide.services/api/v1/applications/77cb2094-9a99-4de6-ac86-bbd2353b49c8
HTTP/2 501
```


> The above command returns JSON structured like this:

```json
[
  {
    "message": "not implemented"
}
]
```

This endpoint removes the specified Application.
<i>(Not yet implemented)</i>

### HTTP Request

`DELETE /api/vi/applications/:id`

### Query Parameters

Parameter | Description
--------- | -----------
id | The ID of the Application to retrieve


## Tokens: Get Tokens


```shell
curl -i \
    -H 'Authorization: bearer yoUr-AutH-TOKeN-FrOm-sIgnINg-in' \
    https://ident.provide.services/api/v1/tokens
HTTP/2 200
```


> The above command returns JSON structured like this:

```json
[
  {
        "id": "234da41d-0970-4561-bdf9-797ef6807fb5",
        "created_at": "2018-10-08T23:34:18.843828Z",
        "issued_at": "2018-10-08T23:34:18.842733Z",
        "expires_at": null,
        "token": "a-New-toKeN-VaLuE",
        "data": null
    },
    {
        "id": "84557020-0180-4e87-ae01-ffa05a587df4",
        "created_at": "2018-10-08T23:58:28.631901Z",
        "issued_at": "2018-10-08T23:58:28.630644Z",
        "expires_at": null,
        "token": "anOthEr-New-toKeN-VaLuE",
        "data": null
    }
]
```

This endpoint enumerates previously authorized Tokens for the authorized User or Application.

### HTTP Request

`GET /api/v1/tokens`


## Tokens: Post Tokens


```shell
curl -i -XPOST \
    -H 'content-type: application/json' \
    -H 'Authorization: bearer an-apPliCaTIOn-aPi-tOkEn' \
    https://ident.provide.services/api/v1/tokens \
    -d '{"name": "PurposeToken"}'
HTTP/2 201
```


> The above command returns JSON structured like this:

```json
[
  {
    "id": "ed3d83ec-8b4f-4538-a240-bf759a2545ff",
    "created_at": "2018-10-09T02:47:25.981937848Z",
    "issued_at": "2018-10-09T02:47:25.980910555Z",
    "expires_at": null,
    "token": "a-New-toKeN-VaLuE",
    "data": null
}
]
```

This endpoint authorizes a Token on behalf of the authorized User or Application.

### HTTP Request

`POST /api/v1/tokens`


## Tokens: Delete Tokens


```shell
curl -i -XDELETE \
    -H 'Authorization: bearer yoUr-AutH-TOKeN-FrOm-sIgnINg-in' \
    https://ident.provide.services/api/v1/tokens/84557020-0180-4e87-ae01-ffa05a587df4
HTTP/2 204
```

This endpoint destroys a previously authorized Token on behalf of the authorized User or Application.

### HTTP Request

`DELETE /api/v1/tokens/:id`

### Query Parameters

Parameter | Description
--------- | -----------
id | The ID of the Application to retrieve

## Users: Get Users


```shell
curl -i \
    -H 'Authorization: bearer an-apPliCaTIOn-aPi-tOkEn' \
    https://ident.provide.services/api/v1/users
HTTP/2 200
```


> The above command returns JSON structured like this:

```json
[
  {
        "id": "7fc90f5a-45e3-42ed-84b9-c13aed6481f1",
        "created_at": "2018-10-09T02:29:30.580961Z",
        "name": "EntArchitect",
        "email": "big-arch@example.com",
        "password": "$2a$10$TzD5muUNH0BFrfwwzsuthOlipQ45e5q3ba8l8wIB9ESPD4d5z/e5G"
    },
    {
        "id": "876e4fc6-b379-432c-8f76-7e42a955d527",
        "created_at": "2018-10-09T02:21:14.531578Z",
        "name": "SavvyExec",
        "email": "vip@example.com",
        "password": "$2a$10$5ebxXX.iWe7OMOHr5CGeye6.G/uj3sb4gRzXxyCEYI2B6KCFYRrz."
    }
]
```

This endpoint enumerates previously created Users for the authorized Application.

### HTTP Request

`GET /api/v1/users`


## Users: Post Users


```shell
curl -i -H 'content-type: application/json' \
    -H 'Authorization: bearer an-apPliCaTIOn-aPi-tOkEn' \
    https://ident.provide.services/api/v1/users \
    -d '{"name": "SavvyExec", "email": "vip@example.com", password": "Str0ngPa55w0rd"}'
HTTP/2 201
```


> The above command returns JSON structured like this:

```json
[
  {
    "id": "876e4fc6-b379-432c-8f76-7e42a955d527",
    "created_at": "2018-10-09T02:21:14.531577683Z",
    "name": "SavvyExec",
    "email": "vip@example.com"
}
]
```

This endpoint creates a new platform User or a User on behalf of an authorized Application..

### HTTP Request

`POST /api/v1/users`


## Users: Update Users


```shell
curl -i -XPUT \
    -H 'content-type: application/json' \
    -H 'Authorization: bearer an-apPliCaTIOn-aPi-tOkEn' \
    https://ident.provide.services/api/v1/users/876e4fc6-b379-432c-8f76-7e42a955d527 \
    -d '{"name": "Professional Executive"}'
HTTP/2 204
```


This endpoint updates an existing User record.

### HTTP Request

`PUT /api/vi/users/:id`

### Query Parameters

Parameter | Description
--------- | -----------
id | The ID of the Application to retrieve


## Users: Delete Users


```shell
curl -i -XDELETE \
    -H 'Authorization: bearer an-apPliCaTIOn-aPi-tOkEn' \
    https://ident.provide.services/api/v1/users/876e4fc6-b379-432c-8f76-7e42a955d527
HTTP/2 501
```


> The above command returns JSON structured like this:

```json
[
  {
    "message": "not implemented"
}
]
```

This endpoint removes a User record.
<i> (Not yet implemented)</i>

### HTTP Request

`DELETE /api/vi/users/:id`

### Query Parameters

Parameter | Description
--------- | -----------
id | The ID of the Application to retrieve
