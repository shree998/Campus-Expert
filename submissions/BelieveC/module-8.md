# Module 08 - GraphQL

## Challenges

### Challenge 1: From your GitHub profile, list your repositories and their languages.

Answer: 

```
{
  "data": {
    "user": {
      "name": "Chaitanya Yadav",
      "repositories": {
        "edges": [
          {
            "node": {
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "Ruby"
                    }
                  },
                  {
                    "node": {
                      "name": "JavaScript"
                    }
                  },
                  {
                    "node": {
                      "name": "CoffeeScript"
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
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "Makefile"
                    }
                  },
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
                      "name": "HTML"
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
              "languages": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "Makefile"
                    }
                  },
                  {
                    "node": {
                      "name": "Shell"
                    }
                  }
                ]
              }
            }
          },
          {
            "node": {
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
              "languages": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "Ruby"
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
                      "name": "HTML"
                    }
                  }
                ]
              }
            }
          },
          {
            "node": {
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "Ruby"
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
              "languages": {
                "edges": []
              }
            }
          },
          {
            "node": {
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
                  },
                  {
                    "node": {
                      "name": "HTML"
                    }
                  },
                  {
                    "node": {
                      "name": "PowerShell"
                    }
                  },
                  {
                    "node": {
                      "name": "Python"
                    }
                  },
                  {
                    "node": {
                      "name": "Shell"
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

Result:

```
{
  "data": {
    "repository": {
      "issues": {
        "edges": [
          {
            "node": {
              "title": "Can't require() react-tools module",
              "labels": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "title": "Write tests for react-tools module",
              "labels": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "title": "must adding comments for JSX?",
              "labels": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "title": "Small update to Bower command",
              "labels": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "title": "Fix docs Rake \"update_version\" command to strip trailing spaces",
              "labels": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "title": "Make valid npm release",
              "labels": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "title": "React in RequireJS ?",
              "labels": {
                "edges": [
                  {
                    "node": {
                      "id": "MDU6TGFiZWw0NjU4MTI3OA=="
                    }
                  }
                ]
              }
            }
          },
          {
            "node": {
              "title": "Docs don't even mention reconciliation!",
              "labels": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "title": "Is es5-sham required for IE8?",
              "labels": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "title": "Uncaught SyntaxError: Unexpected token < ",
              "labels": {
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

### Challenge 3: Find your database ID.

Result:

```
{
  "data": {
    "viewer": {
      "login": "BelieveC",
      "databaseId": 14261624
    }
  }
}
```

### Challenge 4: Find the database ID of the GitHub CEO (@defunkt) and check whether he's a Campus Expert.

Result:

```
{
  "data": {
    "user": {
      "login": "defunkt",
      "databaseId": 2,
      "isCampusExpert": false
    }
  }
}
```

### Challenge 5: Add a reaction to this issue.

Result:

Check the [issue](https://github.com/wilhelmklopp/github-graphql-workshop/issues/2) for a :thumbs_up from me (@BelieveC)
