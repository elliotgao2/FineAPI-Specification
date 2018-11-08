# FineAPI-Specification

```json
{
    "title": "Blog Service",
    "description": "Blog Service",
    "setting": {
        "database": {},
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
