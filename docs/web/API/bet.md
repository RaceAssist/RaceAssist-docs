# Bet API

## Open Data

### Jockey Odds

raceIdと賭け一単位当たりの金額及びオッズなどを取得します

```http
    GET https://race-assist.example.com/bet/jockey/{raceId}
```
<details>
<summary>Response Example</summary> 

```json
    {
        "data" : { 
        "raceId" : "test_1" ,
        "betUnit" : "100",
        "dataList" : [
            {
                "jockey" : "87599344-cec1-438a-9ea0-aa20c34c96af" ,
                "horse": "5bbbbf5d-8900-4bfe-990b-91dafe1cf44e",
                "odds" : "1.82"
            },
            {
                "jockey" : "8160f4c9-74f5-45e7-a5b9-af445c44a80b" ,
                "horse" : "ab2fb6f4-d4e9-4f05-9928-acec19aafe61",
                "odds" : "3.76"
            }
        ]
    }
    }
```

</details>

### Bet Available

```http
    GET https://race-assist.example.com/bet/available/{raceId}
```
<details>
<summary>Response Example</summary> 

```json
    {
        "data" : { 
        "raceId" : "test_1" ,
        "betUnit" : "100",
        "dataList" : [
            {
                "jockey" : "87599344-cec1-438a-9ea0-aa20c34c96af" ,
                "horse": "5bbbbf5d-8900-4bfe-990b-91dafe1cf44e",
                "odds" : "1.82"
            },
            {
                "jockey" : "8160f4c9-74f5-45e7-a5b9-af445c44a80b" ,
                "horse" : "ab2fb6f4-d4e9-4f05-9928-acec19aafe61",
                "odds" : "3.76"
            }
        ]
    }
    }
```

</details>

## Privacy Data (need jwt token)

### Jockey Odds

raceIdと賭け一単位当たりの金額及びオッズなどを取得します

```http
    PUSH https://race-assist.example.com/bet/push/{raceId}
```

<details>
<summary>Request Example</summary> 

```json
    {
        "data" : [
            {
                "jockeyUniqueId" : "80e2e186-a91b-46e0-ac7f-cc2fa98c1fe5" ,
                "multiple": 25,
            },
            {
                "jockey" : "f9754960-6b23-4cf2-b070-166abbe5508f" ,
                "multiple" : 15,
            }
        ]
    }
```
</details>

<details>
<summary>Response Example</summary> 

```json
    {
   "data":{
      "error":null, // Error type NO_MONEY, NOT_AVAILABLE,
      "betUniqueId":[
         "f4791dbe-28bc-4ccf-a4dc-d30e353004ac",
         "eeb5537a-6de2-4ec6-bb75-a77779c8b689"
      ],
      "sum":4000
   }
}
```
</details>