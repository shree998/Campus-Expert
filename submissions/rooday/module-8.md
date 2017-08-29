***Challenge 1: From your GitHub profile, list your repositories and their languages.***

    {
      user(login:"ROODAY"){
        repositories(last: 100) {
          edges {
            node {
              name
              languages(first: 3) {
                edges {
                  node{
                    name
                    color
                  }
                }
              }
            }
          }
        }
      }
    }

***Challenge 2: Fetch the issues for the Facebook React repository.***

    {
      repository(owner:"facebook", name: "react") {
        issues(last: 10) {
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

***Challenge 3: Find your database ID.***  

    {
      user(login:"ROODAY"){
        databaseId
      }
    }

***Challenge 4: Find the database ID of the GitHub CEO (@defunkt) and check whether he's a Campus Expert.***  

    {
      user(login:"defunkt"){
        databaseId
        isCampusExpert
      }
    }

***Challenge 5: Add a reaction to this issue.***  

    {
      repository(owner:"wilhelmklopp", name:"github-graphql-workshop") {
        issues(first: 20) {
          edges{
            node {
              id # To get the ID of the issue we want
              title
            }
          }
        }
      }
    }

    mutation { # To actually like the issue
      addReaction(input: {
        subjectId: "MDU6SXNzdWUyMTg2NjA4OTQ=",
        content: THUMBS_UP
      }) {
        reaction {
          content
          id
        }
      }
    }
