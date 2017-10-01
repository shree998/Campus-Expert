Module 8 - GraphQL answers
==========================

# Challenge 1

## Query
```graphql
{
  user(login: "SCOTTLB") {
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
## Answer
```graphql
{
  "data": {
    "user": {
      "repositories": {
        "edges": [
          {
            "node": {
              "name": "TheSupremeMemeTeam",
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
              "name": "DiscordBot",
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
              "name": "ProgrammingFundamentalsCW1",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "Makefile"
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
              "name": "ProgrammingFundamentals_Group-Project",
              "languages": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "name": "ProgrammingFundamentalsCW2",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "C++"
                    }
                  },
                  {
                    "node": {
                      "name": "Makefile"
                    }
                  }
                ]
              }
            }
          },
          {
            "node": {
              "name": "BlockchainVoting",
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
              "name": "PermissionBot",
              "languages": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "name": "scottlb.github.io",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "HTML"
                    }
                  },
                  {
                    "node": {
                      "name": "Ruby"
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
              "name": "SourceFetch-atom",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "JavaScript"
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
              "name": "Caesar",
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
          }
        ]
      }
    }
  }
}
```

# Challenge 2
## Query
```graphql
{
  repository(owner: "Facebook", name: "react") {
    issues(first: 20) {
      edges {
        node {
          title
        }
      }
    }
  }
}
```
## Answer
```graphql
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
          },
          {
            "node": {
              "title": "Work with compile-to-JS languages (like CoffeeScript)"
            }
          },
          {
            "node": {
              "title": "The name \"JSX\" is already taken, use \"XJS\" instead?"
            }
          },
          {
            "node": {
              "title": "jsx not able to watch subdirs"
            }
          },
          {
            "node": {
              "title": "JSX page gives 404 - linked from \"Why React\" blog post"
            }
          },
          {
            "node": {
              "title": "JSX whitespace coalescing should work like regular HTML"
            }
          },
          {
            "node": {
              "title": "Automatically bind scope of all user provided methods."
            }
          },
          {
            "node": {
              "title": "jsx offline transform exits with error code 1 on any change (Ubuntu 12.10)"
            }
          },
          {
            "node": {
              "title": "Allow namespacing in component names in JSX"
            }
          },
          {
            "node": {
              "title": "Ordering of componentDidMount events"
            }
          },
          {
            "node": {
              "title": "Preserve line numbers in \"grunt test\""
            }
          }
        ]
      }
    }
  }
}
```

# Challenge 3
## Query
```graphql
{
  user(login:"SCOTTLB") {
    databaseId
  }
}
```
## Answer
```graphql
{
  "data": {
    "user": {
      "databaseId": 17150260
    }
  }
}
```

# Challenge 4
## Query
```graphql
{
  user(login:"defunkt") {
    databaseId
    isCampusExpert
  }
}
```
## Answer
```graphql
{
  "data": {
    "user": {
      "databaseId": 2,
      "isCampusExpert": false
    }
  }
}
```

# Challenge 5
## Query
```graphql
{
repository(owner:"wilhelmklopp", name:"github-graphql-workshop"){
  issues(last: 1){
    edges{
      node{
        title
        id
      }
    }
  }
}
}
mutation{
  addReaction(input: {
    subjectId:"MDU6SXNzdWUyMTg2NjA4OTQ=",
    content: THUMBS_UP
  }){
    reaction{
      content
      id
    }
  }
}
```
## Answer
```graphql
{
  "data": {
    "repository": {
      "issues": {
        "edges": [
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
