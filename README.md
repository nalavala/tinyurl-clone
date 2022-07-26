# tinyurl-clone

## _Tech Stack_
- Java
- Spring boot
- Mysql

## _Design_ 
![alt text](https://github.com/nalavala/tinyurl-clone/blob/main/Screenshot%202022-07-26%20at%206.31.31%20PM.png)

## _Data Models_

| field | types | constraints |
| ------ | ------ | ------- | 
| url | varchar |  - |
| key | varchar | primary key |
| created_at | time stamp | - |
| last_accessed_at | time stamp | - |
| expire_at | time stamp | - |

## _API_

**_Generate tiny url_**:
URL : /tinyurl-clone/generate
METHOD : POST

Request : 

```sh
{
    "url" : "https://dillinger.io/",
    "expire_in" : 360000
}
```
Response : 
```sh
{
    "key" : "https://tinyurl-clone/d3f32d",
}
```

**_Get Info_**:

URL : //tinyurl-clone/{key}/info
Method : GET
Response : 
```sh
{
    "url" : "https://dillinger.io/",
    "redirection_url" : "https://tinyurl-clone/d3f32d",
    "expires_at" : "",
}
```

**_Redirection api_**:
URL : //tinyurl-clone/{key}
Method : GET

