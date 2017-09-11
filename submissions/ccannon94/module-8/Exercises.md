### Exercise 1

From your GitHub profile, list your repositories and their languages

Input
```
query{
	viewer{
    repositories(last: 10){
      edges{
        node{
          name
          languages(first: 3){
            edges{
              node{
                name
              }
            }
          }
        }
      }
    }
  }
}
```

Response
```
{
  "data": {
    "viewer": {
      "repositories": {
        "edges": [
          {
            "node": {
              "name": "ncat-ecen433-final-project",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "KiCad"
                    }
                  },
                  {
                    "node": {
                      "name": "Batchfile"
                    }
                  },
                  {
                    "node": {
                      "name": "C"
                    }
                  }
                ]
              }
            }
          },
          {
            "node": {
              "name": "ncat-geen165-lab-quiz-solution-a",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "Java"
                    }
                  }
                ]
              }
            }
          },
          {
            "node": {
              "name": "ncat-geen165-lab-quiz-solution-b",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "Java"
                    }
                  }
                ]
              }
            }
          },
          {
            "node": {
              "name": "PracticalSourceControl",
              "languages": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "name": "FlightDispatcher",
              "languages": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "name": "ncat-comp285-repository",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "C++"
                    }
                  }
                ]
              }
            }
          },
          {
            "node": {
              "name": "Lab-0821",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "Java"
                    }
                  }
                ]
              }
            }
          },
          {
            "node": {
              "name": "open-training",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "HTML"
                    }
                  },
                  {
                    "node": {
                      "name": "Roff"
                    }
                  }
                ]
              }
            }
          },
          {
            "node": {
              "name": "lab-2-arrays-and-methods-ccannon94",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "Java"
                    }
                  }
                ]
              }
            }
          },
          {
            "node": {
              "name": "extra-credit-lab-ccannon94",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "Java"
                    }
                  }
                ]
              }
            }
          }
        ]
      }
    }
  }
}
```

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
