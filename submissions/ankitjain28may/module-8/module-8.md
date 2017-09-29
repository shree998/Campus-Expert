# Module -8: GraphQL

## Challenges

### Challenge 1: From your GitHub profile, list your repositories and their languages.

>Query
```
{
  user(login:"ankitjain28may") {
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

>Response
```
{
  "data": {
    "user": {
      "repositories": {
        "edges": [
          {
            "node": {
              "name": "LibreEHR",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "PHP"
                    }
                  },
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
                  },
                  {
                    "node": {
                      "name": "ActionScript"
                    }
                  },
                  {
                    "node": {
                      "name": "Batchfile"
                    }
                  }
                ]
              }
            }
          },
          {
            "node": {
              "name": "phpmyadmin",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "PHP"
                    }
                  },
                  {
                    "node": {
                      "name": "JavaScript"
                    }
                  },
                  {
                    "node": {
                      "name": "CSS"
                    }
                  },
                  {
                    "node": {
                      "name": "Shell"
                    }
                  },
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
              "name": "BugSmash",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "PHP"
                    }
                  },
                  {
                    "node": {
                      "name": "ApacheConf"
                    }
                  },
                  {
                    "node": {
                      "name": "Vue"
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
              "name": "InteractiveRegistrationForm",
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
              "name": "Scilab-workshop",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "Scilab"
                    }
                  }
                ]
              }
            }
          },
          {
            "node": {
              "name": "registration",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "PHP"
                    }
                  },
                  {
                    "node": {
                      "name": "ApacheConf"
                    }
                  },
                  {
                    "node": {
                      "name": "Vue"
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
              "name": "piwik",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "PHP"
                    }
                  },
                  {
                    "node": {
                      "name": "JavaScript"
                    }
                  },
                  {
                    "node": {
                      "name": "C"
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
              "name": "AwesomeNodeJs",
              "languages": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "name": "js13kgames-2017",
              "languages": {
                "edges": [
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
              "name": "Studiuz",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "ApacheConf"
                    }
                  },
                  {
                    "node": {
                      "name": "PHP"
                    }
                  },
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
          }
        ]
      }
    }
  }
}
```

### Challenge 2: Fetch the issues for the Facebook React repository.

>Query
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

>Response
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

>Query
```
{
  user(login: "ankitjain28may") {
    databaseId
  }
}
```

>Response
```
{
  "data": {
    "user": {
      "databaseId": 14014254
    }
  }
}
```

### Challenge 4: Find the database ID of the GitHub CEO (@defunkt) and check whether he's a Campus Expert.

>Query
```
{
  user(login: "defunkt") {
    databaseId
    isCampusExpert
  }
}
```

>Response
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

>Query 1 (to find PR)
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

>Response 1 (For finding PR)
```
{
  "data": {
    "repository": {
      "pullRequests": {
        "edges": [
          {
            "node": {
              "id": "MDExOlB1bGxSZXF1ZXN0OTE0OTYzOTQ=",
              "title": "Filled in community assessment for UWaterloo"
            }
          },
          {
            "node": {
              "id": "MDExOlB1bGxSZXF1ZXN0OTE1MjI5ODQ=",
              "title": "Filled in community assessment for FH Dortmund"
            }
          },
          {
            "node": {
              "id": "MDExOlB1bGxSZXF1ZXN0OTE1NDE5ODM=",
              "title": "Filled in community assessment for UTN - FRSF."
            }
          },
          {
            "node": {
              "id": "MDExOlB1bGxSZXF1ZXN0OTE2NzUwMTk=",
              "title": "Add community assessment for Indian Institute of Information Technology Allahabad"
            }
          },
          {
            "node": {
              "id": "MDExOlB1bGxSZXF1ZXN0OTE3Mzg2NDQ=",
              "title": "Add FSU tech community assesment"
            }
          },
          {
            "node": {
              "id": "MDExOlB1bGxSZXF1ZXN0OTE3NTkxMTE=",
              "title": "Add TechSoc community assessment 📖"
            }
          },
          {
            "node": {
              "id": "MDExOlB1bGxSZXF1ZXN0OTE3ODM4OTE=",
              "title": "Community Assessment for Queensland University of Technology"
            }
          },
          {
            "node": {
              "id": "MDExOlB1bGxSZXF1ZXN0OTE3ODc0NTU=",
              "title": "Added HackSoc community assessment doc"
            }
          },
          {
            "node": {
              "id": "MDExOlB1bGxSZXF1ZXN0OTE4MDA2MjI=",
              "title": "Add Community Assessment for Durham's budding hacker community"
            }
          },
          {
            "node": {
              "id": "MDExOlB1bGxSZXF1ZXN0OTE4NTYwMDA=",
              "title": "Filled in community assessment for Diversity in the McMaster Tech Community"
            }
          },
          {
            "node": {
              "id": "MDExOlB1bGxSZXF1ZXN0OTE4NTc5ODQ=",
              "title": "UChicago Community Assesment"
            }
          },
          {
            "node": {
              "id": "MDExOlB1bGxSZXF1ZXN0OTE4ODA5Nzc=",
              "title": "Filled in community assessment for Occidental College"
            }
          },
          {
            "node": {
              "id": "MDExOlB1bGxSZXF1ZXN0OTE4ODk3NzE=",
              "title": "Add community assessment for ConU "
            }
          },
          {
            "node": {
              "id": "MDExOlB1bGxSZXF1ZXN0OTE5MTcwMjg=",
              "title": "Impact Proposal for Manitoba Hackers"
            }
          },
          {
            "node": {
              "id": "MDExOlB1bGxSZXF1ZXN0OTE5NDgyMTk=",
              "title": "Filled in community assessment for University of Buea"
            }
          },
          {
            "node": {
              "id": "MDExOlB1bGxSZXF1ZXN0OTE5NTgwMzc=",
              "title": "Community Assessment for \"nobody\""
            }
          },
          {
            "node": {
              "id": "MDExOlB1bGxSZXF1ZXN0OTIwODAwNDU=",
              "title": "Added community assessment for City Tech Society"
            }
          },
          {
            "node": {
              "id": "MDExOlB1bGxSZXF1ZXN0OTIyNzkwOTM=",
              "title": "Smith College-community-assessment.md"
            }
          },
          {
            "node": {
              "id": "MDExOlB1bGxSZXF1ZXN0OTIzODc2NTM=",
              "title": "Community assessment for CompSoc (Edinburgh)"
            }
          },
          {
            "node": {
              "id": "MDExOlB1bGxSZXF1ZXN0OTI0NTc3MDc=",
              "title": "create community-assessment.md"
            }
          }
        ]
      }
    }
  }
}
```


>Query 2 (to add reaction)
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

>Response 2 (from adding reaction)
```
{
  "data": {
    "addReaction": {
      "reaction": {
        "content": "THUMBS_UP",
        "id": "MDg6UmVhY3Rpb24xMzk4NTQ4NQ=="
      }
    }
  }
}
```
