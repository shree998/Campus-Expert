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


**OUT:**


<h2> Challenge 3 </h2>
**IN:**

**OUT:**

<h2> Challenge 4 </h2>
**IN:**

**OUT:**

<h2> Challenge 5 </h2>
**IN:**

**OUT:**

