# Module 08 - GraphQL

## Challenges

### Challenge 1: From your GitHub profile, list your repositories and their languages.

Code:

```
{
  user(login: "AparaV") {
    repositories(last: 10) {
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

Results:

```
{
  "data": {
    "user": {
      "repositories": {
        "edges": [
          {
            "node": {
              "name": "mercurysms",
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
                  }
                ]
              }
            }
          },
          {
            "node": {
              "name": "kaggle-competitions",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "Python"
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
          },
          {
            "node": {
              "name": "deep-learning-udacity",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "Jupyter Notebook"
                    }
                  }
                ]
              }
            }
          },
          {
            "node": {
              "name": "live-photo-interpreter",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "Jupyter Notebook"
                    }
                  },
                  {
                    "node": {
                      "name": "Python"
                    }
                  }
                ]
              }
            }
          },
          {
            "node": {
              "name": "artistic-style",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "Python"
                    }
                  }
                ]
              }
            }
          },
          {
            "node": {
              "name": "cu-appm-2350",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "Mathematica"
                    }
                  },
                  {
                    "node": {
                      "name": "Matlab"
                    }
                  }
                ]
              }
            }
          },
          {
            "node": {
              "name": "backend",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "Python"
                    }
                  },
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
              "name": "tensorflow-experiments",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "Jupyter Notebook"
                    }
                  },
                  {
                    "node": {
                      "name": "Python"
                    }
                  }
                ]
              }
            }
          },
          {
            "node": {
              "name": "models",
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
                      "name": "GLSL"
                    }
                  }
                ]
              }
            }
          },
          {
            "node": {
              "name": "hubot-alfred",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "Shell"
                    }
                  },
                  {
                    "node": {
                      "name": "Batchfile"
                    }
                  },
                  {
                    "node": {
                      "name": "CoffeeScript"
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

### Challenge 2: Fetch the issues for the [Facebook React repository](https://github.com/facebook/react).

Code:

```
{
  repository(owner: "facebook", name: "react") {
    issues(last: 10) {
      edges {
        node {
          title
        }
      }
    }
  }
}
```

Results:

```
{
  "data": {
    "repository": {
      "issues": {
        "edges": [
          {
            "node": {
              "title": "with redux  "
            }
          },
          {
            "node": {
              "title": "Add topics to categorize React repository and make it more discoverable"
            }
          },
          {
            "node": {
              "title": "Descriptive error on null PropType"
            }
          },
          {
            "node": {
              "title": "Buggy controlled number input on 15.5+"
            }
          },
          {
            "node": {
              "title": "inforamtion about internet with react"
            }
          },
          {
            "node": {
              "title": "React.js with asp.net core 2.0"
            }
          },
          {
            "node": {
              "title": "react-test-renderer does not mock React Native Animated"
            }
          },
          {
            "node": {
              "title": "[question] using only nextState in shouldComponentUpdate "
            }
          },
          {
            "node": {
              "title": "What is the bad effect of `react license` for a company?"
            }
          },
          {
            "node": {
              "title": "[Documentation] Add reference to onInvalid form event"
            }
          }
        ]
      }
    }
  }
}
```

### Challenge 3: Find your database ID.

Code:

```
{
  user(login: "AparaV") {
    databaseId
  }
}
```

Results:

```
{
  "data": {
    "user": {
      "databaseId": 16863215
    }
  }
}
```

### Challenge 4: Find the database ID of the GitHub CEO (@defunkt) and check whether he's a Campus Expert.

Code:

```
{
  user(login: "defunkt") {
    databaseId
    isCampusExpert
  }
}
```

Results:

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

#### 1. Querying the issue ID

Code:

```
{
  repository(owner: "wilhelmklopp", name: "github-graphql-workshop") {
    issues(last: 5) {
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

Results:

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

#### 2. Adding reaction

Code:

```
mutation {
  addReaction(input: {subjectId: "MDExOlB1bGxSZXF1ZXN0OTE3NTkxMTE=", content: THUMBS_UP}) {
    reaction {
      content
      id
    }
  }
}
```

Results:

Check the [issue](https://github.com/wilhelmklopp/github-graphql-workshop/issues/2) for a :thumbs_up: from me (@AparaV)
