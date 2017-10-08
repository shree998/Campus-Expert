# Module 8

## Challenges

### Challenge 1: From your GitHub profile, list your repositories and their languages.

#### Request
```javascript

query { 
user(login:"aniket965") {
	repositories(last:10){
	edges {
    node{
      name,
      languages(first:3) {
        edges {
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
#### Response
```javascript
{
  "data": {
    "user": {
      "repositories": {
        "edges": [
          {
            "node": {
              "name": "Starter-kit-js",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "JavaScript"
                    }
                  },
                  {
                    "node": {
                      "name": "ApacheConf"
                    }
                  },
                  {
                    "node": {
                      "name": "HTML"
                    }
                  }
                ]
              }
            }
          },
          {
            "node": {
              "name": "react-native-windows-github-notifs",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "JavaScript"
                    }
                  },
                  {
                    "node": {
                      "name": "Python"
                    }
                  },
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
              "name": "Bing-image-extracting-server",
              "languages": {
                "edges": [
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
              "name": "Delhi-Metro-app",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "JavaScript"
                    }
                  },
                  {
                    "node": {
                      "name": "Python"
                    }
                  },
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
              "name": "react-native-animations",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "JavaScript"
                    }
                  },
                  {
                    "node": {
                      "name": "Python"
                    }
                  },
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
              "name": "github-files-downloader",
              "languages": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "name": "react-native-truth-and-dare",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "JavaScript"
                    }
                  },
                  {
                    "node": {
                      "name": "Python"
                    }
                  },
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
              "name": "react-graphs",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "HTML"
                    }
                  },
                  {
                    "node": {
                      "name": "CSS"
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
              "name": "Master-c",
              "languages": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "name": "GraphQL-Learning",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "JavaScript"
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
### Challenge 2: Fetch the issues for the Facebook React repository

#### Request

```javascript
query {
 repository(owner:"facebook", name: "react") {
  issues(last:4) {
    edges{
      node {
        title
      }
    }
  }
}
}

```

### Response

```javascript
{
  "data": {
    "repository": {
      "issues": {
        "edges": [
          {
            "node": {
              "title": "installation.md content update"
            }
          },
          {
            "node": {
              "title": "Update Thinking in React example to filter products in FilterableProductTable component"
            }
          },
          {
            "node": {
              "title": "Is react-native will under mit license this week"
            }
          },
          {
            "node": {
              "title": "Can we write react component life cycle methods using arrow-function syntax? "
            }
          }
        ]
      }
    }
  }
}
```

### Challenge 3: Find your database ID.

#### Request

```javascript
query {
  user(login:"aniket965"){
    databaseId
  }
}

```

### Response

```javascript
{
  "data": {
    "user": {
      "databaseId": 22680912
    }
  }
}

```

### Challenge 4: Find the database ID of the GitHub CEO (@defunkt) and check whether he's a Campus Expert.

#### Request

```javascript
query {
user(login:"defunkt") {
  databaseId,
  isCampusExpert
}
}
```

### Response

```javascript

{
  "data": {
    "user": {
      "databaseId": 2,
      "isCampusExpert": false
    }
  }
}

```

### Challenge 5: Add a reaction to this issue.

#### Request

```javascript
mutation{
  addReaction(input:{
    subjectId:"MDU6SXNzdWUyMTg2NjA4OTQ=",content: THUMBS_UP
  }) {
    reaction{
      content,
      id
    }
  }
}

```

### Response

```javascript

{
  "data": {
    "addReaction": {
      "reaction": {
        "content": "THUMBS_UP",
        "id": "MDg6UmVhY3Rpb24xNDI4MzE5Nw=="
      }
    }
  }
}

```