<h1> Graph QL Challenges </h1>

<h2> Challenge 1 </h2>

**IN:**
```{
  user(login: "nathankurt") {
    contributedRepositories(last: 5, privacy:PUBLIC ) {
      edges {
        node {
          name
          languages(first: 2) {
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

**OUT:**

```{
  "data": {
    "user": {
      "contributedRepositories": {
        "edges": [
          {
            "node": {
              "name": "OddsGame",
              "languages": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "name": "nathankurt.github.io",
              "languages": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "name": "robotax",
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
                  }
                ]
              }
            }
          },
          {
            "node": {
              "name": "Calendar-Readme",
              "languages": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "name": "Slack-Tally-Bot",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "PHP"
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


<h2>Challenge 2</h2>

**IN:**
```{
  repository(owner: "facebook", name: "react") {
    issues(last: 3) {
      edges {
        node {
          title
        }
      }
    }
  }
}
```

**OUT:**
```{
  "data": {
    "repository": {
      "issues": {
        "edges": [
          {
            "node": {
              "title": "Automated release script"
            }
          },
          {
            "node": {
              "title": "Docs for older versions of React are unavailable"
            }
          },
          {
            "node": {
              "title": "React error decoder page broken"
            }
          }
        ]
      }
    }
  }
}
```

<h2> Challenge 3 </h2>

**IN:**
```{
  user(login: "nathankurt") {
    databaseId
  }
}
```
**OUT:**
```{
  "data": {
    "user": {
      "databaseId": 9864281
    }
  }
}
```
<h2> Challenge 4 </h2>

**IN:**
```
{
  user(login: "defunkt"){
    databaseId
    isCampusExpert
  }
}
```
**OUT:**
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
<h2> Challenge 5 </h2>


<h3> First Querey </h3>

**IN:**
```{
  repository(owner:"wilhelmklopp" name: "github-graphql-workshop"){
    issues(first: 1){
      edges{
        node{
  				id
        }
      }
    }
  }
}

```

**OUT:**
```{
  "data": {
    "repository": {
      "issues": {
        "edges": [
          {
            "node": {
              "id": "MDU6SXNzdWUyMTg2NTcwMzk="
            }
          }
        ]
      }
    }
  }
}
```

<h3> Second Querey </h3>

**IN:**
```mutation {
  addReaction(input: {subjectId: "MDU6SXNzdWUyMTg2NTcwMzk=", content: THUMBS_UP}) {
    reaction {
      content
      id
    }
  }
}

```
**OUT:**
```{
  "data": {
    "addReaction": {
      "reaction": {
        "content": "THUMBS_UP",
        "id": "MDg6UmVhY3Rpb24xNDkwMzA3NA=="
      }
    }
  }
}
```
