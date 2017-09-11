### Exercise 1

### Exercise 2

### Exercise 3

### Exercise 4

### Exercise 5

Add a thumbs-up to Wilhelm's most recent issue in _github-graphql-workshop_

Input
```
query{
  repository(owner: "wilhelmklopp", name: "github-graphql-workshop"){
    issues(last: 1){
      edges{
        node{
          id
          title
        }
      }
    }
  }
}
```
Response
```
{
  "data": null,
  "errors": [
    {
      "message": "No operation named \"\""
    }
  ]
}
```
Input
```
mutation{
  addReaction(input: {
    subjectId: "MDU6SXNzdWUyMTg2NjA4OTQ",
    content: THUMBS_UP
  }){
    reaction{
      content
      id
    }
  }
}
```
Response
```
{
  "data": {
    "addReaction": {
      "reaction": {
        "content": "THUMBS_UP",
        "id": "MDg6UmVhY3Rpb24xMzc1MTYwNw=="
      }
    }
  }
}
```
