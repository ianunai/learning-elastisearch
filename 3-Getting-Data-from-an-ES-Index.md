## Part 3: Getting Data from an ES Index

In this part, we will work with getting data from employees in a corporation. 
The index that the data will be fetched from is called `megacorp` and the document type is `employee`. It is the same index and document type that we pushed some data to in part 2.

The format for getting data from ES is similar to pushing data to it, which is as follows:  

`{ES Host}:{ES Port}/{index}/{type}/{id}`

This tutorial uses cURL to get data, however, Postman can be utilized as well.

__Example:__  

* Getting the document from index `megacorp` and document type `employee` with id `1`:  

```
curl -X GET "localhost:9200/megacorp/employee/1?pretty"
```

* From part 2, we know the `-X` flag represents the request type that follows after, which is a `GET` request in our case. And it retrieves the document with id `1` stored as document type `employee` in the `megacorp` index.

* Response:  

```
{
  "_index" : "megacorp",
  "_type" : "employee",
  "_id" : "1",
  "_version" : 2,
  "_seq_no" : 3,
  "_primary_term" : 2,
  "found" : true,
  "_source" : {
    "first_name" : "John",
    "last_name" : "Smith",
    "age" : 25,
    "about" : "I love to go rock climbing",
    "interests" : [
      "sports",
      "music"
    ]
  }
}
```
The actual response is the value for the `_source` key.  

The next part of learning Elasticsearch deals with tailoring queries to the index.