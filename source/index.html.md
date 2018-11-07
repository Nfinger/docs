---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - go
  - groovy
  - javascript
  - python
  - ruby
  - swift

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes:
  - ident
  - goldmine
  - errors

search: true
---

# Introduction

Welcome to the [Provide](http://provide.services/) ident and goldmine API  portal. Ident API lets you manage Provide platform users and applications. Goldmine gives you the power to leverage public blockchain information in building best-of-breed applications. Both ident and goldmine API are RESTful and use HTTP. Requests and responses are formatted JSON.

We have language bindings in go, groovy, javascript, python, ruby, and swift. View code examples on the right. Switch the example format with the tabs on the top right.

# Authentication

> To authorize, use this code:

```ruby
require 'Provide'

api = Provide::APIClient.authorize!('meowmeowmeow')
```

```python
import Provide

api = Provide.authorize('meowmeowmeow')
```

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: meowmeowmeow"
```

```javascript
const Provide = require('Provide');

let api = Provide.authorize('meowmeowmeow');
```

Provide uses API keys to allow access to the API. You can register a new Provide API key at our [developer portal](http://example.com/developers).

Provide expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: bearer`

<aside class="notice">
You must replace <code>bearer</code> with your personal API key.
</aside>
