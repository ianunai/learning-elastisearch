## Part 2: Pushing Data to an ES Index

In this part, we will work with employees in a corporation. 
The index that the data will be pushed to is called `megacorp` and the document type is `employee`.  

The format for pushing data to ES is as follows:  

`{ES Host}:{ES Port}/{index}/{type}/{id}`

This tutorial uses cURL to push data, however, Postman can be utilized as well.

__Examples:__  

1. Pushing a document of type `employee` in the index `megacorp` with `id` `1`: 

```
curl -X PUT "localhost:9200/megacorp/employee/1?pretty" -H 'Content-Type: application/json' -d'
{
    "first_name" : "John",
    "last_name" :  "Smith",
    "age" :        25,
    "about" :      "I love to go rock climbing",
    "interests": [ "sports", "music" ]
}
'
```

* The `pretty` parameter after `?` in the request URL is simply to return a pretty JSON response.

* From the above cURL command, we notice that it is issued in the format mentioned in the beginning of the tutorial. The `-X` flag that follows after `curl` is for specifying the HTTP request type, which corresponds to `PUT` in this case as we are pushing new data to Elasticsearch.

* The `-H` flag is for specifying a header, which is accompanied by the `Content-Type` header, which is `application/json` specifying the document in the request body.

2. Second example:  

```
curl -X PUT "localhost:9200/megacorp/employee/2?pretty" -H 'Content-Type: application/json' -d'
{
    "first_name" :  "Jane",
    "last_name" :   "Smith",
    "age" :         32,
    "about" :       "I like to collect rock albums",
    "interests":  [ "music" ]
}
'
```

3. Third example:  

```
curl -X PUT "localhost:9200/megacorp/employee/3?pretty" -H 'Content-Type: application/json' -d'
{
    "first_name" :  "Douglas",
    "last_name" :   "Fir",
    "age" :         35,
    "about":        "I like to build cabinets",
    "interests":  [ "forestry" ]
}
'
```