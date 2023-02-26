# Place API

## Open Data

### Place List

```http
    GET http://race-assist.example.com/place/list
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
    GET https://race-assist.example.com/place/config/{raceId}
```
<details>
<summary>Response Example</summary> 

```json
{
   "data":{
      "placeId":"test_1",
      "centralX":-5112,
      "centralY":452,
      "goalDegree":180,
      "reverse":false,
      "inside":{
         "points":[
            {
               "first":-5160,
               "second":452
            },
            {
               "first":-5160,
               "second":471
            },
            {
               "first":-5160,
               "second":589
            },
            {
               "first":-5159,
               "second":600
            }
         ]
      },
      "outside":{
         "points":[
            {
               "first":-5184,
               "second":452
            },
            {
               "first":-5184,
               "second":594
            },
            {
               "first":-5183,
               "second":600
            },
            {
               "first":-5181,
               "second":607
            }
         ]
      },
      "owner":"5e45fdbb-5aa4-4d70-b1dc-f5fd1d562db9",
      "staff":[
         "5e45fdbb-5aa4-4d70-b1dc-f5fd1d562db9"
      ],
      "image" : "iVBORw0KGgoAAAANSUhEUgAAAC4AAAArCAIAAACIFi3TAAAASklEQVR4Xu3OMQ0AIADAMGThDk8oRAD74WjSa9fG2vMT406vWClWipVipVgpVoqVYqVYKVaKlWKlWClWipVipVgpVoqVYqV8tHIAXsHl4SNKTX0AAAAASUVORK5CYII="
   }
}
```
</details>

## Need jwt

### Push Place Config

```http
    POST http://race-assist.example.com/place/config/{placeId}
```

<details>
<summary>Request Example</summary> 

Example
```json
    {
      "placeId":"test_1",
      "centralX":-5112,
      "centralY":452,
      "goalDegree":180,
      "reverse":false,
      "inside":{
         "points":[
            {
               "first":-5160,
               "second":452
            },
            {
               "first":-5160,
               "second":471
            },
            {
               "first":-5160,
               "second":589
            },
            {
               "first":-5159,
               "second":600
            }
         ]
      },
      "outside":{
         "points":[
            {
               "first":-5184,
               "second":452
            },
            {
               "first":-5184,
               "second":594
            },
            {
               "first":-5183,
               "second":600
            },
            {
               "first":-5181,
               "second":607
            }
         ]
      },
      "owner":"5e45fdbb-5aa4-4d70-b1dc-f5fd1d562db9",
      "staff":[
         "5e45fdbb-5aa4-4d70-b1dc-f5fd1d562db9"
      ],
      "image" : "iVBORw0KGgoAAAANSUhEUgAAAC4AAAArCAIAAACIFi3TAAAASklEQVR4Xu3OMQ0AIADAMGThDk8oRAD74WjSa9fG2vMT406vWClWipVipVgpVoqVYqVYKVaKlWKlWClWipVipVgpVoqVYqV8tHIAXsHl4SNKTX0AAAAASUVORK5CYII="
   }
```
</details>