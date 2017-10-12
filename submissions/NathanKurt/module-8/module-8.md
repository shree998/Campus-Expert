### Graph QL Challenges

* Challenge 1

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
}```

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
}```

