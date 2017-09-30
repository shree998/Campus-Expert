#GraphQL Challenges
#Challenge 1: From your GitHub profile, list your repositories and their languages.

{
  user(login: "yashovardhanagrawal") {
    repositories(last: 5) {
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

#Challenge 2: Fetch the issues for the Facebook React repository.

{
  repository(owner: "facebook", name: "react") {
    issues(last: 5) {
      edges {
        node {
          title
        }
      }
    }
  }
}

#Challenge 3: Find your database ID.

{
  user(login: "yashovardhanagrawal") {
    databaseId
  }
}

#Challenge 4: Find the database ID of the GitHub CEO (@defunkt) and check whether he's a Campus Expert.

{
  user(login: "defunkt") {
    databaseId
    isCampusExpert
  }
}

#Challenge 5: Add a reaction to this issue.

{
  repository(owner: "wilhelmklopp", name: "github-graphql-workshop") {
    issues(last: 5) {
      edges {
        node {
          title
          id
        }
      }
    }
  }
}

mutation {
  addReaction(input: {subjectId: "MDU6SXNzdWUyMTg2NjA4OTQ=", content: LAUGH}) {
    reaction {
      content
      id
    }
  }
}
