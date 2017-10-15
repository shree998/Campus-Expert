> Challenge 1: From your GitHub profile, list your repositories and their languages.

### To find repos & their languages:
```
{
  user(login: "kunall17") {
    repositories(first: 20) {
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

### Response:
```
{
  "data": {
    "user": {
      "repositories": {
        "edges": [
          {
            "node": {
              "name": "zulip-android",
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
              "name": "Toolkit-mobile-templates",
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
                  }
                ]
              }
            }
          },
          {
            "node": {
              "name": "afwall",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "Makefile"
                    }
                  },
                  {
                    "node": {
                      "name": "Java"
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
              "name": "EntryScreenManager",
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
              "name": "GigaGet",
              "languages": {
                "edges": [
                  {
                    "node": {
                      "name": "HTML"
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
              "name": "BuildmLearn-Toolkit-Android",
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
              "name": "android-client",
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
              "name": "IONAutoLogin",
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
              "name": "awesome-android-ui",
              "languages": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "name": "android_top_1000",
              "languages": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "name": "DateRangePicker",
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
              "name": "android_guides",
              "languages": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "name": "awesome-android",
              "languages": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "name": "awesome-android-1",
              "languages": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "name": "android-awesome-libraries",
              "languages": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "name": "Awesome-Mobile-UI",
              "languages": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "name": "TopAndroid",
              "languages": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "name": "AndroidLibrary",
              "languages": {
                "edges": []
              }
            }
          },
          {
            "node": {
              "name": "awesome-android-libraries",
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
```


> Challenge 2: Fetch the issues for the Facebook React repository.

### To fetch issues used:
```
{
  repository(owner: "facebook", name: "react") {
    issues(first: 80) {
      edges {
        node {
          title
        }
      }
    }
  }
}
```

### Response:

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
          },
          {
            "node": {
              "title": "grunt test just hangs"
            }
          },
          {
            "node": {
              "title": "bin/jsx should not relativize required module IDs unless --relativize is passed"
            }
          },
          {
            "node": {
              "title": "Support comments in JSX"
            }
          },
          {
            "node": {
              "title": "Add a demo using .coffee files to implement a React component"
            }
          },
          {
            "node": {
              "title": "Mocking not working with EventPluginRegistry"
            }
          },
          {
            "node": {
              "title": "Scoped css?"
            }
          },
          {
            "node": {
              "title": "React + Browserify module issues"
            }
          },
          {
            "node": {
              "title": "React.renderComponent() tries to update components without checking their constructor type"
            }
          },
          {
            "node": {
              "title": "React should throw on nested <p> tags"
            }
          },
          {
            "node": {
              "title": "Come up with a convention for forcing bin/jsx rebuilds without manually clearing .module-cache"
            }
          },
          {
            "node": {
              "title": "commoner's grep for @providesModule turns up vim swap files"
            }
          },
          {
            "node": {
              "title": "Stop requiring docblock for JSX transformer"
            }
          },
          {
            "node": {
              "title": "Parens () inside of {} causes a syntax error when passed through JSXTransformer"
            }
          },
          {
            "node": {
              "title": "Adding 0.1 incrementally with setState gives out approximate numbers"
            }
          },
          {
            "node": {
              "title": "Remove content property"
            }
          },
          {
            "node": {
              "title": "Getting JSX syntax to play nicely with jslint?"
            }
          },
          {
            "node": {
              "title": "Pending state updates may be confusing"
            }
          },
          {
            "node": {
              "title": "Id selection"
            }
          },
          {
            "node": {
              "title": "[0.4] Write docs for React.props"
            }
          },
          {
            "node": {
              "title": "Maybe interpolate within JSX attributes?"
            }
          },
          {
            "node": {
              "title": "Have ReactNativeComponent throw on invalid property names"
            }
          },
          {
            "node": {
              "title": "jsx overwrites modules without --relativize"
            }
          },
          {
            "node": {
              "title": "Consider allowing `setState` while UNMOUNTING"
            }
          },
          {
            "node": {
              "title": "onClick broken on iOS."
            }
          },
          {
            "node": {
              "title": "Address EMFILE (too many open files) errors for clean `grunt test` runs"
            }
          },
          {
            "node": {
              "title": "Not all tests running?"
            }
          },
          {
            "node": {
              "title": "Allow custom (nonstandard) attributes."
            }
          },
          {
            "node": {
              "title": "Document mouseEnter and mouseLeave on event handling page"
            }
          },
          {
            "node": {
              "title": "Export createDOMComponentClass()"
            }
          },
          {
            "node": {
              "title": "Missing autofocus in DOMProperty.js standard properties enumeration."
            }
          },
          {
            "node": {
              "title": "Figure out how to make global available"
            }
          },
          {
            "node": {
              "title": "Fix failing test"
            }
          },
          {
            "node": {
              "title": "Enable mocking of required modules during tests"
            }
          },
          {
            "node": {
              "title": "Support for <{'Module'} {'key'}={'value'}>"
            }
          },
          {
            "node": {
              "title": "Bad NPM package-- Fatal error: Cannot find module './build/modules/React'"
            }
          },
          {
            "node": {
              "title": "Animations before unmounting (and in general)"
            }
          },
          {
            "node": {
              "title": "Rename onChange to onSomethingNotInTheSpecAlready"
            }
          },
          {
            "node": {
              "title": "Document forms changes / best practices"
            }
          },
          {
            "node": {
              "title": "Add all contributors"
            }
          },
          {
            "node": {
              "title": "Changelog in the repo"
            }
          },
          {
            "node": {
              "title": "Fix tests when using phantomjs 1.9.1-1"
            }
          },
          {
            "node": {
              "title": "Parent's onClick squashed by child's onClick"
            }
          },
          {
            "node": {
              "title": "this.h3 'Foo' instead of verbose React.DOM.h3 null, 'Foo'"
            }
          },
          {
            "node": {
              "title": "Better event docs"
            }
          },
          {
            "node": {
              "title": "Pass rootNode for componentWillUnmount"
            }
          },
          {
            "node": {
              "title": "setState (and others) parameters format"
            }
          },
          {
            "node": {
              "title": "Maybe make sure we work with all $.trigger events"
            }
          },
          {
            "node": {
              "title": "Auto-assigned keys can conflict with user-specified ones"
            }
          },
          {
            "node": {
              "title": "Allow stringified aliases for className and htmlFor."
            }
          },
          {
            "node": {
              "title": "Children array should allow to use numbers and booleans."
            }
          },
          {
            "node": {
              "title": "Parsing error for HTML entity in nested JSX."
            }
          },
          {
            "node": {
              "title": "Add support for touch-action attribute for Polymer PointerEvents"
            }
          },
          {
            "node": {
              "title": "Allow html attribute names in React.DOM / JSX"
            }
          },
          {
            "node": {
              "title": "onContextMenu event?"
            }
          },
          {
            "node": {
              "title": "Firefox: div contentEditable triggers \"TypeError: setting a property that has only a getter\""
            }
          },
          {
            "node": {
              "title": "Add invariant to make sure we pass a node to componentDidMount"
            }
          },
          {
            "node": {
              "title": "Few issues in the (upcoming) doc"
            }
          },
          {
            "node": {
              "title": "ReactCompositeComponent.mountComponent needs a try/finally"
            }
          },
          {
            "node": {
              "title": "Some lifecycle methods are broken"
            }
          },
          {
            "node": {
              "title": "Swap the todo example to the one on todomvc"
            }
          }
        ]
      }
    }
  }
}
```
> Challenge 3: Find your database ID.

### To find database id
```
query {
  user(login:"kunall17"){
    databaseId
  }
}
```
### Response:

```
{
  "data": {
    "user": {
      "databaseId": 12700799
    }
  }
}
```

> Challenge 4: Find the database ID of the GitHub CEO (@defunkt) and check whether he's a Campus Expert.
### To find id and boolean
```
query{
  user(login: "defunkt") {
    databaseId
    isCampusExpert
  }
}
```

### Response:
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

> Challenge 5: Add a reaction to this issue.

### To find the id used query:

```
{
  repository(owner: "wilhelmklopp", name: "github-graphql-workshop") {
    issue(number: 2) {
        id
        title
    }
  }
}
```

### To add reaction used query:

```
mutation {
  addReaction(input: {subjectId: "MDU6SXNzdWUyMTg2NjA4OTQ=", content: THUMBS_UP}) {
    reaction {
      content
      id
    }
  }
}
```

### Response:

```
{
  "data": {
    "addReaction": {
      "reaction": {
        "content": "THUMBS_UP",
        "id": "MDg6UmVhY3Rpb24xNDc0NDE3OQ=="
      }
    }
  }
}
```
