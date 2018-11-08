# FineAPI-Specification

```json
{
    "title": "Blog Service",
    "description": "Blog Service",
    "setting": {
        "storage": {},
        "cache": {},
        "permission": [
            "IsOwnerOrReadOnly"
        ],
        "authentication": {
            "resource": "User",
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
