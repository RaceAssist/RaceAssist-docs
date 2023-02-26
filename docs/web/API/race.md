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

### Place Config

```http
    GET https://race-assist.example.com/race/config/{raceId}
```
<details>
<summary>Response Example</summary> 

```json
{
   "data":{
      "raceId":"test_1",
      "raceName":"test_1",
      "placeId":"test_1",
      "betConfig":{
         "available":false,
         "returnPercent":75,
         "spreadSheetId":null,
         "betUnit":100,
         "autoReturn":false,
         "money":0.0
      },
      "owner":"559c175b-bdc8-4fb2-9c98-0f4e118233ba",
      "staff":[
         "559c175b-bdc8-4fb2-9c98-0f4e118233ba"
      ],
      "jockeys":[
         
      ],
      "lap":0,
      "replacement":{
         
      },
      "horse":{
         
      }
   }
}
```
</details>


## Privacy Data (need jwt token)

### Push Place Config

```http
    POST http://race-assist.example.com/place/config/{placeId}
```

<details>
<summary>Request Example</summary> 

Example
```json
{
      "raceId":"test_1",
      "raceName":"test_1",
      "placeId":"test_1",
      "betConfig":{
         "available":false,
         "returnPercent":75,
         "spreadSheetId":null,
         "betUnit":100,
         "autoReturn":false,
         "money":0.0
      },
      "owner":"559c175b-bdc8-4fb2-9c98-0f4e118233ba",
      "staff":[
         "559c175b-bdc8-4fb2-9c98-0f4e118233ba"
      ],
      "jockeys":[
         
      ],
      "lap":0,
      "replacement":{
         
      },
      "horse":{
         
      }
}
```
</details>

