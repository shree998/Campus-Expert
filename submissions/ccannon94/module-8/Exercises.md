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

Fetch the issues for the Facebook React repository

Input
```
query{
	repository(owner: "facebook", name:"react"){
    issues(last: 10){
      edges{
        node{
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
  "data": {
    "repository": {
      "issues": {
        "edges": [
          {
            "node": {
              "title": "Remove performWithPriority from scheduler"
            }
          },
          {
            "node": {
              "title": "eifjccgigekurdbfdijghgfbdhbhticgjvcfkjhfjcbj"
            }
          },
          {
            "node": {
              "title": "Interactive documentation for JSX"
            }
          },
          {
            "node": {
              "title": "ReactChildFiber.coerceRef does not like undefined ref on a component"
            }
          },
          {
            "node": {
              "title": "picture srcset error"
            }
          },
          {
            "node": {
              "title": "cannot set property 'nextEffect' of undefined"
            }
          },
          {
            "node": {
              "title": "BFcache, SSR and form elements"
            }
          },
          {
            "node": {
              "title": "React doesn't correctly re-render dynamically created Components added to an <svg> via state"
            }
          },
          {
            "node": {
              "title": "What's the difference between yarn and npm ??"
            }
          },
          {
            "node": {
              "title": "Where can I find information about React 16?"
            }
          }
        ]
      }
    }
  }
}
```

### Exercise 3

Find your database ID

Input
```
query{
	viewer{
    databaseId
  }
}

```
Response
```
{
  "data": {
    "viewer": {
      "databaseId": 16315060
    }
  }
}
```

### Exercise 4

Find the database ID of the GitHub CEO and check whether he's a campus expert

Input
```
query{
	user(login:"defunkt"){
    databaseId
    isCampusExpert
  }
}
```
Response
```
{
  "data": {
    "user": {
      "databaseId": 2,
      "isCampusExpert": false
    }
  }
}
```

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
