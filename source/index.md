---
title: API Reference

language_tabs:
- instructions

toc_footers:
- <a href='#'>Some Link</a>

includes:
- errors

search: true
---

# Lernhow Documentation

> Install dev shit

> Install dev shit

> Install dev shit

> Install dev shit

Intro text blah and install instructions

Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
consequat.

Duis aute irure dolor in reprehenderit in voluptate velit esse
cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

Lorem ipsum dolor sit amet, consectetur adipisicing elit.

# Protected Endpoints

> To access a protected endpoint, use this code:

```shell
# you must pass the correct header with each request
curl "api_endpoint_goes_here"
  -H "x-access-token: thetokenthatyoucopiedearlierfromlocalstorage"
```

**Lernhow** protects all endpoints that perform *write* operations to **Guide** or **Step** records. All protected endpoints will be marked with a '`*`'.

1. You must navigate to <a href="https://lernhow.herokuapp.com/#signup" target="_blank">lernhow/#signup</a>, and sign up for a standard user account before you can access the **Lernhow** API.

2. Open the developer console, and navigate to the **Resources** tab.

3. Copy the **token** value in **Local Storage** stored in the https://lernhow.herokuapp.com/ section.

# Users

## Create a User (**signup**) *

```javascript
```

```shell
curl "https://lernhow.herokuapp.com/api/endpoint"
  -H "x-access-token: someridiculouslylongstringthatyoushouldputhere"
```

> The above command returns JSON structured like this:

```json
[
{
  "id": 1,
  "name": "Fluffums",
  "breed": "calico",
  "fluffiness": 6,
  "cuteness": 7
},
{
  "id": 2,
  "name": "Isis",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
]
```

This endpoint **creates** a new **User** record in the database.

### HTTP Request

**`POST https://lernhow.herokuapp.com/api/users/signup`**

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.

<aside class="success">
  Remember — a happy kitten is an authenticated kitten!
</aside>

## Get a Specific Kitten

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get(2)
```

```shell
curl "http://example.com/api/kittens/3"
-H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Isis",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific kitten.

<aside class="warning">If you're not using an administrator API key, note that some kittens will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`GET http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the cat to retrieve

