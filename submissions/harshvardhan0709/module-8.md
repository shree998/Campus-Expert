Module 8 - GraphQL answers
==========================

# Challenge 1

## Query
{
  user(login: "harshvardhan0709") {
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


## Answer
{
  "data": {
    "user": {
      "repositories": {
        "edges": [
          {
            "node": {
              "name": "RblBankAPP",
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
              "name": "Predict-the-happiness-NLP",
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
              "name": "Augmented-Reality-AR-Project-Basic",
              "languages": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "name": "Android-Tutorial-From-Scratch",
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
              "name": "RaceEye",
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
              "name": "open-enrollment-classes-introduction-to-github",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "Ruby"
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
          }
        ]
      }
    }
  }
}



# Challenge 2
## Query
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


## Answer
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


# Challenge 3
## Query
{
  user(login:"harshvardhan0709") {
    databaseId
  }
}

## Answer
{
  "data": {
    "user": {
      "databaseId": 29592607
    }
  }
}


# Challenge 4
## Query
{
  user(login:"defunkt") {
    databaseId
    isCampusExpert
  }
}

## Answer
{
  "data": {
    "user": {
      "databaseId": 2,
      "isCampusExpert": false
    }
  }
}


# Challenge 5
## Query
mutation {
  addReaction(input: {subjectId: "MDU6SXNzdWUyMTg2NjA4OTQ=", content: THUMBS_UP}) {
    reaction {
      content
      id
    }
  }
}

## Answer
{
  "data": {
    "addReaction": {
      "reaction": {
        "content": "THUMBS_UP",
        "id": "MDg6UmVhY3Rpb24xNDc0MTMzNQ=="
      }
    }
  }
}
