# Module -8: GraphQL

## Challenges

### Challenge 1: From your GitHub profile, list your repositories and their languages.

#### Query
```
{
  user(login:"tomasjames") {
    repositories(last: 10) {
      edges {
        node {
          name
          languages(first: 6) {
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

### Response
```
{
  "data": {
    "user": {
      "repositories": {
        "edges": [
          {
            "node": {
              "name": "Global-Map",
              "languages": {
                "edges": [
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
              "name": "Exoplanet-Project",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "Python"
                    }
                  },
                  {
                    "node": {
                      "name": "TeX"
                    }
                  }
                ]
              }
            }
          },
          {
            "node": {
              "name": "citsciportal",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "Python"
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
                  },
                  {
                    "node": {
                      "name": "HTML"
                    }
                  },
                  {
                    "node": {
                      "name": "Shell"
                    }
                  },
                  {
                    "node": {
                      "name": "Nginx"
                    }
                  }
                ]
              }
            }
          },
          {
            "node": {
              "name": "ZiggyStarDust",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "Python"
                    }
                  },
                  {
                    "node": {
                      "name": "TeX"
                    }
                  },
                  {
                    "node": {
                      "name": "IDL"
                    }
                  }
                ]
              }
            }
          },
          {
            "node": {
              "name": "gitterbot",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "JavaScript"
                    }
                  },
                  {
                    "node": {
                      "name": "Shell"
                    }
                  },
                  {
                    "node": {
                      "name": "CSS"
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
              "name": "arduino-workshop",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "Arduino"
                    }
                  },
                  {
                    "node": {
                      "name": "C++"
                    }
                  },
                  {
                    "node": {
                      "name": "Shell"
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
              "name": "astropy-tutorials",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "Python"
                    }
                  },
                  {
                    "node": {
                      "name": "Shell"
                    }
                  },
                  {
                    "node": {
                      "name": "CSS"
                    }
                  },
                  {
                    "node": {
                      "name": "Smarty"
                    }
                  },
                  {
                    "node": {
                      "name": "HTML"
                    }
                  },
                  {
                    "node": {
                      "name": "Jupyter Notebook"
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

### Challenge 2: Fetch the issues for the Facebook React repository.

### Query
```
{
  repository(owner:"facebook", name: "react") {
      issues(first: 10) {
        edges {
          node {
            title
          }
        }
      }
    }
}
```

### Response
```
{
  "data": {
    "repository": {
      "issues": {
        "edges": [
          {
            "node": {
              "title": "Can't require() react-tools module"
            }
          },
          {
            "node": {
              "title": "Write tests for react-tools module"
            }
          },
          {
            "node": {
              "title": "must adding comments for JSX?"
            }
          },
          {
            "node": {
              "title": "Small update to Bower command"
            }
          },
          {
            "node": {
              "title": "Fix docs Rake \"update_version\" command to strip trailing spaces"
            }
          },
          {
            "node": {
              "title": "Make valid npm release"
            }
          },
          {
            "node": {
              "title": "React in RequireJS ?"
            }
          },
          {
            "node": {
              "title": "Docs don't even mention reconciliation!"
            }
          },
          {
            "node": {
              "title": "Is es5-sham required for IE8?"
            }
          },
          {
            "node": {
              "title": "Uncaught SyntaxError: Unexpected token < "
            }
          }
        ]
      }
    }
  }
}
```

### Challenge 3: Find your database ID.

### Query
```
{
  user(login: "tomasjames") {
    databaseId
  }
}
```

### Response
```
{
  "data": {
    "user": {
      "databaseId": 5236734
    }
  }
}
```

### Challenge 4: Find the database ID of the GitHub CEO (@defunkt) and check whether he's a Campus Expert.

### Query
```
{
  user(login: "defunkt") {
    databaseId
    isCampusExpert
  }
}
```

### Response
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

### Challenge 5: Add a reaction to this issue.

### Query 1 (to find PR)
```
{
  repository(owner: "campus-experts", name: "fall-2016") {
    pullRequests(first: 20) {
      edges {
        node {
          id
          title
        }
      }
    }
  }
}
```

### Query 2 (to add reaction)
```
mutation {
  addReaction(input: {
    subjectId: "MDExOlB1bGxSZXF1ZXN0OTE3NTkxMTE=",
    content:THUMBS_UP
  }) {
    reaction {
      content
      id
    }
  }
}
```

### Response (from adding reaction)
```
{
  "data": {
    "addReaction": {
      "reaction": {
        "content": "THUMBS_UP",
        "id": "MDg6UmVhY3Rpb24xMzYyODQ2Nw=="
      }
    }
  }
}
```