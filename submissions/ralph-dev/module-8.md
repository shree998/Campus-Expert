# Challenge 1: From your GitHub profile, list your repositories and their languages.
# Answer: Grabbed the first 10 repo's and the first(Mostly used) 3 languages in that repo from my profile
query {
  user(login: "ralph-dev") {
    repositories(first: 10) {
      edges {
        node {
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
# Challenge 2: Fetch the issues for the Facebook React repository.
# Answer: Grabbed the last 10 issues from the repo
query {
  repository(owner: "facebook", name: "react") {
    issues(last: 10){
      edges {
        node {
          title
        }
      }
    }
  }
}
# Challenge 3: Find your database ID.
# Answer: My databaseID for my profile. I am 7469722
query {
	user(login: "ralph-dev") {
    databaseId
  }
}
# Challenge 4: Find the database ID of the GitHub CEO (@defunkt) and check whether he's a Campus Expert.
# Answer: He is 2nd.
query {
	user(login: "defunkt") {
    databaseId
  }
}
# Challenge 5: Add a reaction to this issue.
# Adds a reaction to an issue
mutation {
  addReaction(input: {
    subjectId: "MDExOlB1bGxSZXF1ZXN0OTE3NTkxMTE=",
    content: THUMBS_UP
  }) {
    reaction {
      content
      id
    }
  }
}
