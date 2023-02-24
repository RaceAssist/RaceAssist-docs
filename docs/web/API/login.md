# Login API

## Open Data

### get login token

```http
    POST https://race-assist.example.com/login
```

<details>
<summary>Request Example</summary> 

```json
    {
        "username" : "Notch" ,
        "password" : "pass"
    }
```
</details>

<details>
<summary>Response Example</summary> 

```json
    {
        "token" : "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.SflKxwRJSMeKKF2QT4fwpMeJf36POk6yJV_adQssw5c",
        "refreshToken" : "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM2NTQ3fQ.bYF9gy9DqMdQK9-_qfcMbfsdzdyNByfzyhev741iLmY"
    }
```
</details>

### get refresh token (need refresh jwt token)

```http
    POST https://race-assist.example.com/refresh
```

<details>
<summary>Response Example</summary> 

```json
    {
        "token" : "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoiMTExMTExNDU2NTQ0MyJ9.i2OzAoSmfyXGR4fdLDnSPOpSpK0SVP58ae9a2A1r32U"
    }
```
</details>