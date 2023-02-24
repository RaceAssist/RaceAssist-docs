# Race API

## Open Data

### Race List

```http
    GET http://race-assist.example.com/race/list
```

<details>
<summary>Response Example</summary> 

Example
```json
    {
        "data" : { 
            "list" : [ "test_1" , "test_2"]
        }
    }
```
</details>


## Privacy Data (need jwt token)

### Race Config

