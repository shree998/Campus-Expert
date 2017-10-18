## GraphQL Challenges

### Challenge 1

Input:-

{
  user(login: "sukhbir-singh"){
    repositories(first:10){
      edges{
        node{
          name
          languages(first: 20){
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


Output:-

{
  "data": {
    "user": {
      "repositories": {
        "edges": [
          {
            "node": {
              "name": "crossJump-game-opengl",
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
              "name": "Learning-new-words",
              "languages": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "name": "festnimbus",
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
              "name": "open-event-android",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "Java"
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
              "name": "NewsBuzz",
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
              "name": "tipsNtricks",
              "languages": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "name": "group-messenger",
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
              "name": "AgriculturalApp",
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
              "name": "NithApp",
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
              "name": "demo_git",
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


### Challenge 2

Input:-

{
  repository(owner: "facebook", name:"react"){
    issues(first:10, orderBy:{field: CREATED_AT, direction: DESC}){
      edges{
        node{
          title
          createdAt
        }
      }
    }
  }
}

Output:-

{
  "data": {
    "repository": {
      "issues": {
        "edges": [
          {
            "node": {
              "title": "\"Cannot create property for a non-extensible object\".",
              "createdAt": "2017-10-16T16:00:03Z"
            }
          },
          {
            "node": {
              "title": "How to combine theme.breakpoints on React?",
              "createdAt": "2017-10-16T15:39:55Z"
            }
          },
          {
            "node": {
              "title": "test",
              "createdAt": "2017-10-16T15:24:08Z"
            }
          },
          {
            "node": {
              "title": "shallow test renderer calls shouldComponentUpdate on forceUpdate",
              "createdAt": "2017-10-16T15:10:37Z"
            }
          },
          {
            "node": {
              "title": "React props are not available when arguments are set in html tag",
              "createdAt": "2017-10-16T12:46:26Z"
            }
          },
          {
            "node": {
              "title": "Request to release react 15.6.2 which based on MIT License",
              "createdAt": "2017-10-16T09:27:50Z"
            }
          },
          {
            "node": {
              "title": "keyup event not fired on Firefox for Android",
              "createdAt": "2017-10-16T07:21:36Z"
            }
          },
          {
            "node": {
              "title": " ReactiveFormsModule like angular4 in react",
              "createdAt": "2017-10-15T07:20:12Z"
            }
          },
          {
            "node": {
              "title": "Issue with dangerouslySetInnerHTML and markup rehydration",
              "createdAt": "2017-10-14T20:17:18Z"
            }
          },
          {
            "node": {
              "title": "[Feature] Async componentWillReceiveProps to allow state update",
              "createdAt": "2017-10-14T00:28:00Z"
            }
          }
        ]
      }
    }
  }
}

### Challenge 3

Input:-

{
  user(login: "sukhbir-singh"){
    databaseId
  }
}

Output:-

{
  "data": {
    "user": {
      "databaseId": 13816752
    }
  }
}

### Challenge 4

Input:-

{
  user(login: "defunkt"){
    databaseId
    isCampusExpert
  }
}

Output:-

{
  "data": {
    "user": {
      "databaseId": 2,
      "isCampusExpert": false
    }
  }
}

### Challenge 5

Input1:-

query{
  repository(owner: "wilhelmklopp", name: "github-graphql-workshop"){
    issues(last:1){
      edges{
        node{
          id
          title
        }
      }
    }
  }
}


Output1:-

{
  "data": {
    "repository": {
      "issues": {
        "edges": [
          {
            "node": {
              "id": "MDU6SXNzdWUyMTg2NjA4OTQ=",
              "title": "Like me ✅"
            }
          }
        ]
      }
    }
  }
}

Input2:-

mutation{
  addReaction(input:{
    subjectId: "MDU6SXNzdWUyMTg2NjA4OTQ=",
    content: HEART
  }){
    reaction{
      content
      id
    }
  }
}

Output2:-

{
  "data": {
    "addReaction": {
      "reaction": {
        "content": "HEART",
        "id": "MDg6UmVhY3Rpb24xNTA2NTAzMA=="
      }
    }
  }
}



