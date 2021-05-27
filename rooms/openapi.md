<!-- Generator: Widdershins v4.0.1 -->

<h1 id="rooms-microservice">Rooms Microservice v1.0.0</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

Rooms Microservice

Base URLs:

* <a href="https://localhost/v1">https://localhost/v1</a>

<h1 id="rooms-microservice-default">Default</h1>

## post__rooms

`POST /rooms`

*Creating a room*

POST Room 2

> Body parameter

```json
{
  "id": "string",
  "name": "string",
  "code": "string",
  "description": "string",
  "vacancies": 0,
  "rules": {
    "property1": true,
    "property2": true
  },
  "facilities": [
    "string"
  ],
  "album": [
    {
      "name": "string",
      "url": "string"
    }
  ]
}
```

<h3 id="post__rooms-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[Room](#schemaroom)|true|none|

<h3 id="post__rooms-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|CREATED|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__rooms

`GET /rooms`

*GET rooms from service*

GET Rooms

<h3 id="get__rooms-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|page|query|integer|false|none|
|perPage|query|integer|false|none|

> Example responses

> 200 Response

```json
{
  "pagination": {
    "current_page": 0,
    "total_pages": 0,
    "per_page": 0,
    "total_entries": 0
  },
  "data": [
    {
      "id": "string",
      "name": "string",
      "code": "string",
      "description": "string",
      "vacancies": 0,
      "rules": {
        "property1": true,
        "property2": true
      },
      "facilities": [
        "string"
      ],
      "album": [
        {
          "name": "string",
          "url": "string"
        }
      ]
    }
  ],
  "links": {
    "next": "string",
    "previous": "string"
  }
}
```

<h3 id="get__rooms-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|[SearchResponse](#schemasearchresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## get__rooms_{id}

`GET /rooms/{id}`

*GET rooms from service*

GET Room

<h3 id="get__rooms_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|

> Example responses

> 200 Response

```json
{
  "id": "string",
  "name": "string",
  "code": "string",
  "description": "string",
  "vacancies": 0,
  "rules": {
    "property1": true,
    "property2": true
  },
  "facilities": [
    "string"
  ],
  "album": [
    {
      "name": "string",
      "url": "string"
    }
  ]
}
```

<h3 id="get__rooms_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|A JSON array of user names|[Room](#schemaroom)|

<aside class="success">
This operation does not require authentication
</aside>

# Schemas

<h2 id="tocS_Pagination">Pagination</h2>
<!-- backwards compatibility -->
<a id="schemapagination"></a>
<a id="schema_Pagination"></a>
<a id="tocSpagination"></a>
<a id="tocspagination"></a>

```json
{
  "current_page": 0,
  "total_pages": 0,
  "per_page": 0,
  "total_entries": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|current_page|integer|false|none|none|
|total_pages|integer|false|none|none|
|per_page|integer|false|none|none|
|total_entries|integer|false|none|none|

<h2 id="tocS_Links">Links</h2>
<!-- backwards compatibility -->
<a id="schemalinks"></a>
<a id="schema_Links"></a>
<a id="tocSlinks"></a>
<a id="tocslinks"></a>

```json
{
  "next": "string",
  "previous": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|next|string|false|none|none|
|previous|string|false|none|none|

<h2 id="tocS_Room">Room</h2>
<!-- backwards compatibility -->
<a id="schemaroom"></a>
<a id="schema_Room"></a>
<a id="tocSroom"></a>
<a id="tocsroom"></a>

```json
{
  "id": "string",
  "name": "string",
  "code": "string",
  "description": "string",
  "vacancies": 0,
  "rules": {
    "property1": true,
    "property2": true
  },
  "facilities": [
    "string"
  ],
  "album": [
    {
      "name": "string",
      "url": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|string|false|none|none|
|name|string|false|none|none|
|code|string|false|none|none|
|description|string|false|none|none|
|vacancies|integer|false|none|none|
|rules|[Rules](#schemarules)|false|none|none|
|facilities|[string]|false|none|none|
|album|[[Image](#schemaimage)]|false|none|none|

<h2 id="tocS_Rules">Rules</h2>
<!-- backwards compatibility -->
<a id="schemarules"></a>
<a id="schema_Rules"></a>
<a id="tocSrules"></a>
<a id="tocsrules"></a>

```json
{
  "property1": true,
  "property2": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|**additionalProperties**|boolean|false|none|none|

<h2 id="tocS_Image">Image</h2>
<!-- backwards compatibility -->
<a id="schemaimage"></a>
<a id="schema_Image"></a>
<a id="tocSimage"></a>
<a id="tocsimage"></a>

```json
{
  "name": "string",
  "url": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|false|none|none|
|url|string|false|none|none|

<h2 id="tocS_SearchResponse">SearchResponse</h2>
<!-- backwards compatibility -->
<a id="schemasearchresponse"></a>
<a id="schema_SearchResponse"></a>
<a id="tocSsearchresponse"></a>
<a id="tocssearchresponse"></a>

```json
{
  "pagination": {
    "current_page": 0,
    "total_pages": 0,
    "per_page": 0,
    "total_entries": 0
  },
  "data": [
    {
      "id": "string",
      "name": "string",
      "code": "string",
      "description": "string",
      "vacancies": 0,
      "rules": {
        "property1": true,
        "property2": true
      },
      "facilities": [
        "string"
      ],
      "album": [
        {
          "name": "string",
          "url": "string"
        }
      ]
    }
  ],
  "links": {
    "next": "string",
    "previous": "string"
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|pagination|[Pagination](#schemapagination)|false|none|none|
|data|[[Room](#schemaroom)]|false|none|none|
|links|[Links](#schemalinks)|false|none|none|

