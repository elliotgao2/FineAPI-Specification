# FineAPI-Specification

## Service Define

```json
{
    "title": "Blog Service",
    "description": "Blog Service",
    "setting": {
        "root": "/api",
        "database": {},
        "cache": {},
        "upload": {},
        "permission": [
            "IsOwnerOrReadOnly"
        ],
        "authentication": {
            "resource": "User",
            "type": "jwt",
            "username": "username",
            "password": "password"
        }
    },
    "resources": {
        "users": {
            "title": "User",
            "description": "User",
            "search_fields": [
                "username"
            ],
            "filter_fields": [
                "username"
            ],
            "fields": {
                "username": {
                    "type": "String"
                },
                "password": {
                    "type": "String"
                },
                "role": {
                    "type": "String"
                }
            }
        },
        "articles": {
            "title": "Article",
            "description": "Article",
            "search_fields": [
                "username"
            ],
            "filter_fields": [
                "username"
            ],
            "fields": {
                "title": {
                    "type": "String"
                },
                "content": {
                    "type": "String"
                },
                "author": {
                    "type": "User",
                    "relation": "ManyToOne"
                }
            }
        }
    }
}
```

## Data Example

```json
{
    "meta": {
        "type": "resources",
        "page_size": 25,
        "page": 1,
        "total": 2,
        "links": {
            "parent": {
                "title": "home",
                "href": "/"
            },
            "self": {
                "title": "works",
                "href": "works"
            },
            "next": {
                "title": "next page",
                "href": "works?page=2"
            },
            "last": {
                "title": "last page",
                "href": "works?page=2"
            }
        }
    },
    "data": [
        {
            "meta": {
                "type": "resource",
                "links": {
                    "self": {
                        "title": "Work",
                        "href": "works/5bd899a9435e700004888e16"
                    }
                }
            },
            "data": {
                "_id": "5bd899a9435e700004888e16",
                "title": "Book Title #25",
                "description": "Description #25",
                "owner": "5bd899a8435e700004888df9",
                "_etag": "401943a986ab49a2e630a977579fd6d80b51f081",
                "_updated": 1234567890,
                "_created": 1234567890
            }
        }
    ]
}
```
