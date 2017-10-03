# GraphQL challenges

This exercise is to complete the challenges given in the module.

## Task

Complete the challenges above using GraphQL, and add the answers and results to a file called "module-8.md". 

- Challenge 1: From your GitHub profile, list your repositories and their languages.


### Query for your own name:
```graphql
query { 
  user(login: "toxtli") { 
    repositories(last: 100) {
      edges {
        node {
          name
          primaryLanguage {
            name
          }
        }
      }
    }
  }
```
### Result
```graphql
{
  "data": {
    "user": {
      "repositories": {
        "edges": [
          {
            "node": {
              "name": "Verilog-project",
              "primaryLanguage": {
                "name": "Verilog"
              }
            }
          },
          {
            "node": {
              "name": "VisualBasic-project",
              "primaryLanguage": {
                "name": "Visual Basic"
              }
            }
          },
          {
            "node": {
              "name": "Haskell-project",
              "primaryLanguage": {
                "name": "Haskell"
              }
            }
          },
          {
            "node": {
              "name": "Julia-project",
              "primaryLanguage": {
                "name": "Julia"
              }
            }
          },
          {
            "node": {
              "name": "Arduino-project",
              "primaryLanguage": {
                "name": "Arduino"
              }
            }
          },
          {
            "node": {
              "name": "Scheme-project",
              "primaryLanguage": {
                "name": "Scheme"
              }
            }
          },
          {
            "node": {
              "name": "Racket-project",
              "primaryLanguage": {
                "name": "Racket"
              }
            }
          },
          {
            "node": {
              "name": "AppleScript-project",
              "primaryLanguage": {
                "name": "AppleScript"
              }
            }
          },
          {
            "node": {
              "name": "Forth-project",
              "primaryLanguage": {
                "name": "Forth"
              }
            }
          },
          {
            "node": {
              "name": "Visual-Basic-project",
              "primaryLanguage": {
                "name": "Visual Basic"
              }
            }
          },
          {
            "node": {
              "name": "ActionScript-project",
              "primaryLanguage": {
                "name": "ActionScript"
              }
            }
          },
          {
            "node": {
              "name": "ABAP-project",
              "primaryLanguage": {
                "name": "ABAP"
              }
            }
          },
          {
            "node": {
              "name": "COBOL-project",
              "primaryLanguage": {
                "name": "COBOL"
              }
            }
          },
          {
            "node": {
              "name": "FORTRAN-project",
              "primaryLanguage": {
                "name": "Fortran"
              }
            }
          },
          {
            "node": {
              "name": "Cuda-project",
              "primaryLanguage": {
                "name": "Cuda"
              }
            }
          },
          {
            "node": {
              "name": "Makefile-project",
              "primaryLanguage": {
                "name": "Makefile"
              }
            }
          },
          {
            "node": {
              "name": "Clojure-project",
              "primaryLanguage": {
                "name": "Clojure"
              }
            }
          },
          {
            "node": {
              "name": "JavaScript-project",
              "primaryLanguage": {
                "name": "JavaScript"
              }
            }
          },
          {
            "node": {
              "name": "HTML-project",
              "primaryLanguage": {
                "name": "HTML"
              }
            }
          },
          {
            "node": {
              "name": "CoffeeScript-project",
              "primaryLanguage": {
                "name": "CoffeeScript"
              }
            }
          },
          {
            "node": {
              "name": "C-project",
              "primaryLanguage": {
                "name": "C"
              }
            }
          },
          {
            "node": {
              "name": "Pascal-project",
              "primaryLanguage": {
                "name": "Pascal"
              }
            }
          },
          {
            "node": {
              "name": "Common-Lisp-project",
              "primaryLanguage": {
                "name": "Common Lisp"
              }
            }
          },
          {
            "node": {
              "name": "Scala-project",
              "primaryLanguage": {
                "name": "Scala"
              }
            }
          },
          {
            "node": {
              "name": "Lua-project",
              "primaryLanguage": {
                "name": "Lua"
              }
            }
          },
          {
            "node": {
              "name": "Matlab-project",
              "primaryLanguage": {
                "name": "Matlab"
              }
            }
          },
          {
            "node": {
              "name": "Swift-project",
              "primaryLanguage": {
                "name": "Swift"
              }
            }
          },
          {
            "node": {
              "name": "Groovy-project",
              "primaryLanguage": {
                "name": "Groovy"
              }
            }
          },
          {
            "node": {
              "name": "Assembly-project",
              "primaryLanguage": {
                "name": "Assembly"
              }
            }
          },
          {
            "node": {
              "name": "C-Sharp-project",
              "primaryLanguage": {
                "name": "C#"
              }
            }
          },
          {
            "node": {
              "name": "ASP-project",
              "primaryLanguage": {
                "name": "ASP"
              }
            }
          },
          {
            "node": {
              "name": "Perl6-project",
              "primaryLanguage": {
                "name": "Perl6"
              }
            }
          },
          {
            "node": {
              "name": "Java-project",
              "primaryLanguage": {
                "name": "Java"
              }
            }
          },
          {
            "node": {
              "name": "C-Plus-Plus-project",
              "primaryLanguage": {
                "name": "C++"
              }
            }
          },
          {
            "node": {
              "name": "Erlang-project",
              "primaryLanguage": {
                "name": "Erlang"
              }
            }
          },
          {
            "node": {
              "name": "Elixir-project",
              "primaryLanguage": {
                "name": "Elixir"
              }
            }
          },
          {
            "node": {
              "name": "R-project",
              "primaryLanguage": {
                "name": "R"
              }
            }
          },
          {
            "node": {
              "name": "Dart-project",
              "primaryLanguage": {
                "name": "Dart"
              }
            }
          },
          {
            "node": {
              "name": "Go-project",
              "primaryLanguage": {
                "name": "Go"
              }
            }
          },
          {
            "node": {
              "name": "Ruby-project",
              "primaryLanguage": {
                "name": "Ruby"
              }
            }
          },
          {
            "node": {
              "name": "PHP-project",
              "primaryLanguage": {
                "name": "PHP"
              }
            }
          },
          {
            "node": {
              "name": "Python-project",
              "primaryLanguage": {
                "name": "Python"
              }
            }
          },
          {
            "node": {
              "name": "facebook-chat-api",
              "primaryLanguage": {
                "name": "JavaScript"
              }
            }
          },
          {
            "node": {
              "name": "todelete",
              "primaryLanguage": null
            }
          },
          {
            "node": {
              "name": "microvolunteering-extractor",
              "primaryLanguage": {
                "name": "Python"
              }
            }
          },
          {
            "node": {
              "name": "linkedin-profile-scraper",
              "primaryLanguage": {
                "name": "Python"
              }
            }
          },
          {
            "node": {
              "name": "microvolunteering",
              "primaryLanguage": {
                "name": "HTML"
              }
            }
          },
          {
            "node": {
              "name": "volinterface",
              "primaryLanguage": {
                "name": "HTML"
              }
            }
          },
          {
            "node": {
              "name": "fbbot",
              "primaryLanguage": {
                "name": "JavaScript"
              }
            }
          },
          {
            "node": {
              "name": "chrome-extension",
              "primaryLanguage": {
                "name": "JavaScript"
              }
            }
          },
          {
            "node": {
              "name": "simple-meteor-angularjs-crud",
              "primaryLanguage": {
                "name": "JavaScript"
              }
            }
          },
          {
            "node": {
              "name": "chrome-extension-bot-tools",
              "primaryLanguage": {
                "name": "JavaScript"
              }
            }
          },
          {
            "node": {
              "name": "youtubell",
              "primaryLanguage": {
                "name": "Python"
              }
            }
          },
          {
            "node": {
              "name": "twitter-account-selector",
              "primaryLanguage": {
                "name": "Python"
              }
            }
          },
          {
            "node": {
              "name": "LuzDeploy",
              "primaryLanguage": {
                "name": "JavaScript"
              }
            }
          },
          {
            "node": {
              "name": "GuakbotTCD2016",
              "primaryLanguage": {
                "name": "Python"
              }
            }
          },
          {
            "node": {
              "name": "oauth2_proxy",
              "primaryLanguage": {
                "name": "Go"
              }
            }
          },
          {
            "node": {
              "name": "bobabot",
              "primaryLanguage": null
            }
          },
          {
            "node": {
              "name": "Mirai-Source-Code",
              "primaryLanguage": {
                "name": "C"
              }
            }
          },
          {
            "node": {
              "name": "bot-course-botcamp",
              "primaryLanguage": {
                "name": "JavaScript"
              }
            }
          },
          {
            "node": {
              "name": "bot",
              "primaryLanguage": {
                "name": "Python"
              }
            }
          },
          {
            "node": {
              "name": "BotBuilder",
              "primaryLanguage": {
                "name": "C#"
              }
            }
          },
          {
            "node": {
              "name": "testbot01",
              "primaryLanguage": {
                "name": "JavaScript"
              }
            }
          },
          {
            "node": {
              "name": "conversational-form",
              "primaryLanguage": {
                "name": "HTML"
              }
            }
          },
          {
            "node": {
              "name": "starter-slapp-app",
              "primaryLanguage": {
                "name": "JavaScript"
              }
            }
          },
          {
            "node": {
              "name": "linkedin-deleter-bot",
              "primaryLanguage": {
                "name": "Python"
              }
            }
          },
          {
            "node": {
              "name": "twitter-deleter-bot",
              "primaryLanguage": {
                "name": "Python"
              }
            }
          },
          {
            "node": {
              "name": "twitter-accounts-creator-bot",
              "primaryLanguage": {
                "name": "Python"
              }
            }
          },
          {
            "node": {
              "name": "linkedin-invites-sender-bot",
              "primaryLanguage": {
                "name": "Python"
              }
            }
          },
          {
            "node": {
              "name": "facebook-profile-scraper-bot",
              "primaryLanguage": {
                "name": "Python"
              }
            }
          },
          {
            "node": {
              "name": "apiai-weather-webhook-sample",
              "primaryLanguage": {
                "name": "Python"
              }
            }
          },
          {
            "node": {
              "name": "bot-api-ai-webhook",
              "primaryLanguage": {
                "name": "Python"
              }
            }
          },
          {
            "node": {
              "name": "deprecated",
              "primaryLanguage": null
            }
          },
          {
            "node": {
              "name": "testing",
              "primaryLanguage": {
                "name": "Python"
              }
            }
          },
          {
            "node": {
              "name": "temporal",
              "primaryLanguage": null
            }
          },
          {
            "node": {
              "name": "bots-workflow-designer",
              "primaryLanguage": {
                "name": "HTML"
              }
            }
          },
          {
            "node": {
              "name": "pychimerge",
              "primaryLanguage": {
                "name": "Python"
              }
            }
          },
          {
            "node": {
              "name": "chimerge",
              "primaryLanguage": {
                "name": "Python"
              }
            }
          },
          {
            "node": {
              "name": "edubot",
              "primaryLanguage": {
                "name": "JavaScript"
              }
            }
          },
          {
            "node": {
              "name": "gogo",
              "primaryLanguage": {
                "name": "CSS"
              }
            }
          },
          {
            "node": {
              "name": "demo-workflow",
              "primaryLanguage": {
                "name": "Python"
              }
            }
          },
          {
            "node": {
              "name": "deep-learning-tweets-text-classifier-word2vec",
              "primaryLanguage": {
                "name": "Python"
              }
            }
          },
          {
            "node": {
              "name": "learning-to-learn",
              "primaryLanguage": {
                "name": "Python"
              }
            }
          },
          {
            "node": {
              "name": "todosbot",
              "primaryLanguage": {
                "name": "JavaScript"
              }
            }
          },
          {
            "node": {
              "name": "image-predictor-pre-trained-model-keras",
              "primaryLanguage": {
                "name": "Python"
              }
            }
          },
          {
            "node": {
              "name": "word-predictor-word2vec-sklearn",
              "primaryLanguage": {
                "name": "Python"
              }
            }
          },
          {
            "node": {
              "name": "twitter-tweets-streaming-api-extractor",
              "primaryLanguage": {
                "name": "Python"
              }
            }
          },
          {
            "node": {
              "name": "google-apps-script-mail-to-json",
              "primaryLanguage": {
                "name": "JavaScript"
              }
            }
          },
          {
            "node": {
              "name": "futuristic-3d-spherical-news-visualization-three-js",
              "primaryLanguage": {
                "name": "JavaScript"
              }
            }
          },
          {
            "node": {
              "name": "rss-feed-crawler-cron-python-mongodb",
              "primaryLanguage": {
                "name": "Python"
              }
            }
          }
        ]
      }
    }
  }
}
```

- Challenge 2: Fetch the issues for the [Facebook React repository](https://github.com/facebook/react).

### Query:
```graphql
query {
  repository(owner:"facebook", name: "react") {
    issues(first: 20) {
      edges {
        node {
          title
          labels(first: 100) {
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
### Result
```graphql
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
                      "name": "Component: Documentation & Website"
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
          },
          {
            "node": {
              "title": "Work with compile-to-JS languages (like CoffeeScript)",
              "labels": {
                "edges": [
                  {
                    "node": {
                      "name": "Type: Enhancement"
                    }
                  }
                ]
              }
            }
          },
          {
            "node": {
              "title": "The name \"JSX\" is already taken, use \"XJS\" instead?",
              "labels": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "title": "jsx not able to watch subdirs",
              "labels": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "title": "JSX page gives 404 - linked from \"Why React\" blog post",
              "labels": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "title": "JSX whitespace coalescing should work like regular HTML",
              "labels": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "title": "Automatically bind scope of all user provided methods.",
              "labels": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "title": "jsx offline transform exits with error code 1 on any change (Ubuntu 12.10)",
              "labels": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "title": "Allow namespacing in component names in JSX",
              "labels": {
                "edges": [
                  {
                    "node": {
                      "name": "Type: Enhancement"
                    }
                  }
                ]
              }
            }
          },
          {
            "node": {
              "title": "Ordering of componentDidMount events",
              "labels": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "title": "Preserve line numbers in \"grunt test\"",
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

- Challenge 3: Find your database ID.

### Query
```graphql
query {
  viewer {
    databaseId
  }
}
```

### Result
```graphql
{
  "data": {
    "viewer": {
      "databaseId": 1299233
    }
  }
}
```

- Challenge 4: Find the database ID of the GitHub CEO (@defunkt) and check whether he's a Campus Expert.

### Query
```graphql

query {
  user (login: "defunkt") {
    databaseId
    isCampusExpert
  }
}
```

### Result
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

- Challenge 5: Add a reaction to [this](https://github.com/wilhelmklopp/github-graphql-workshop/issues/2) issue.


### Get ID
```graphql
query {
  repository(owner:"wilhelmklopp", name:"github-graphql-workshop") {
    issue(number:2) {
      id
      title
    }
  }
}
```

### Result
```graphql
{
  "data": {
    "repository": {
      "issue": {
        "id": "MDU6SXNzdWUyMTg2NjA4OTQ=",
        "title": "Like me ✅"
      }
    }
  }
}
```

### Mutate
```graphql
mutation {
  addReaction(input: {
    subjectId: "MDU6SXNzdWUyMTg2NjA4OTQ=",
    content: HOORAY
  }) {
    reaction {
      content
      id
    }
  }
}
```

### Result
```graphql
{
  "data": {
    "addReaction": {
      "reaction": {
        "content": "HOORAY",
        "id": "MDg6UmVhY3Rpb24xNDQ3NzA5OQ=="
      }
    }
  }
}
```

