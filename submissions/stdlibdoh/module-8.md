# GraphQL challenges

## Challenge 1

**In**

```
{
  user(login: "stdlibdoh") {
    repositories(last: 5) {
      edges {
        node {
          name
          languages(first: 3) {
            edges {
              node {
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

**Out**

```
{
  "data": {
    "user": {
      "repositories": {
        "edges": [
          {
            "node": {
              "name": "sudoku-solver-js",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "HTML"
                    }
                  },
                  {
                    "node": {
                      "name": "JavaScript"
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
              "name": "hack-the-police-2",
              "languages": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "name": "docs",
              "languages": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "name": "swproj-l",
              "languages": {
                "edges": []
              }
            }
          }
        ]
      }
    }
  }
}
```

## Challenge 2

**In**

```
{
  repository(owner: "facebook" name: "react") {
    issues(last: 5) {
      edges {
        node {
          title
        }
      }
    }
  }
}
```

**Out**

```
{
  "data": {
    "repository": {
      "issues": {
        "edges": [
          {
            "node": {
              "title": "How to use TestRenderer?"
            }
          },
          {
            "node": {
              "title": "onMouseEnter lost when hovering over children"
            }
          },
          {
            "node": {
              "title": "Add warnings on adding functions and components on State."
            }
          },
          {
            "node": {
              "title": "React-Test-Renderer@16 breaks trying to use internal property"
            }
          },
          {
            "node": {
              "title": "Automated release script"
            }
          }
        ]
      }
    }
  }
}
```

## Challenge 3

**In**

```
{
  user(login: "stdlibdoh") {
    databaseId
  }
}
```

**Out**

```
{
  "data": {
    "user": {
      "databaseId": 10576738
    }
  }
}
```

## Challenge 4

**In**

```
{
  user(login: "defunkt") {
    isCampusExpert
    databaseId
  }
}
```

**Out**

```
{
  "data": {
    "user": {
      "isCampusExpert": false,
      "databaseId": 2
    }
  }
}
```

## Challenge 5

#### Step 1

**In**

```
{
  repository(owner: "wilhelmklopp" name: "github-graphql-workshop") {
    issues(last: 2) {
      edges {
    		node {
          title
          id
        }
      }
    }
  }
}
```

**Out**

```
{
  "data": {
    "repository": {
      "issues": {
        "edges": [
          {
            "node": {
              "title": "Every repo needs a good issue",
              "id": "MDU6SXNzdWUyMTg2NTcwMzk="
            }
          },
          {
            "node": {
              "title": "Like me ✅",
              "id": "MDU6SXNzdWUyMTg2NjA4OTQ="
            }
          }
        ]
      }
    }
  }
}
```

#### Step 2

**In**

```
mutation {
  addReaction(input: {
    subjectId: "MDU6SXNzdWUyMTg2NjA4OTQ",
    content: HOORAY
  }) {
    reaction {
      content
      id
    }
  }
}
```

**Out**

```
{
  "data": {
    "addReaction": {
      "reaction": {
        "content": "HOORAY",
        "id": "MDg6UmVhY3Rpb24xNDcyMjM0Nw=="
      }
    }
  }
}
```
