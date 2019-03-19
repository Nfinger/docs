---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
# shell
  - shell

includes:
  - ident
  - goldmine
  - errors

search: true
---

# Welcome

Welcome to the [Provide](http://provide.services/) ident and goldmine API  portal.
- Ident microservice lets you manage Provide platform users and applications.
- Goldmine API gives you the power to leverage public blockchain information in building best-of-breed applications. *Both ident and goldmine are RESTful.*

<aside class="caution">
**NOTE:** to access the API you need to [create an account](https://dawn.provide.services/sign-up) and create a dApp on one of the many networks available to you.
</aside>

# Authentication

## API Token Generation

> To authorize a Token on behalf of an authorized User or Application:

```shell
curl -i -H 'content-type: application/json' \
    https://ident.provide.services/api/v1/authenticate \
    -d '{"email": "user42@domain.tld", "password": "S00perS3cr3t"}'
HTTP/2 201
```

> The above command returns JSON structured like this:

```
{
    "user": {
        "id": "3d9d62e8-0acf-47cd-b74f-52c1f96f8397",
        "created_at": "2018-10-08T23:34:18.70074Z",
        "name": "Doc U. Mentation",
        "email": "user42@domain.tld"
    },
    "token": {
        "id": "52d9caf3-0a56-4670-886e-8136b633d52b",
        "token": "yoUr-AutH-TOKeN-FrOm-sIgnINg-in"
    }
}
```

Provide uses API keys to allow access to the API. If you already have an account on the [Provide console](https://dawn.provide.services/sign-in), you can get a token by simply deploying an application. We recommend you check the status of the service before making requests.

Provide expects for the key to be included in all API requests to the server in a header that looks like the following:

`Authorization: bearer yoUr-AutH-TOKeN-FrOm-sIgnINg-in`

The `bearer` authorization header is scoped to an authorized platform user or application. This header may contain a sub to further limit scope to a specific token, smart contract, wallet or other entity.

<aside class="success">
To receive a token, use the email and password you used to create a Provide account.
</aside>
