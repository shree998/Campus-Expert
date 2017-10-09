# GraphQL challenges

## Challenge 1

```
{
  user(login: "stdlibdoh") {
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
```

## Challenge 2

```
{
  repository(owner: "facebook" name: "react") {
    issues(last: 10) {
      edges {
        node {
          title
        }
      }
    }
  }
}
```

## Challenge 3

```
{
  user(login: "stdlibdoh") {
    databaseId
  }
}
```

## Challenge 4

```
{
  user(login: "defunkt") {
    isCampusExpert
    databaseId
  }
}
```

## Challenge 5

#### Step 1

```
{
  repository(owner: "wilhelmklopp" name: "github-graphql-workshop") {
    issues(last: 2) {
      edges {
    		node {
          title
          id
        }
      }
    }
  }
}
```

#### Step 2

```
mutation {
  addReaction(input: {
    subjectId: "MDU6SXNzdWUyMTg2NjA4OTQ",
    content: HOORAY
  }) {
    reaction {
      content
      id
    }
  }
}
```
