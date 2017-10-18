## Hubot scripting

I created a but which would rename a github repo to someother name, For example in my bot if I write

`jarvis rename oldrepo to newrepo`

It would rename the oldrepo to the new repo

Script used:

```
HUBOT_GITHUB_TOKEN ="***"
HUBOT_GITHUB_USER ="kunall17"

module.exports = (robot) ->
  github = require('githubot')(robot)
  robot.respond /rename\s([a-z]*)\sto\s([a-z]*)/i, (msg) ->
    owner = "#{HUBOT_GITHUB_USER}"
    repo="#{msg.match[1]}"
    newrepo="#{msg.match[2]}"
    oauth_token = "#{HUBOT_GITHUB_TOKEN}"

    data = JSON.stringify({
      name: "#{newrepo}"
    })
    msg.http("https://api.github.com/repos/#{owner}/#{repo}")
      .headers(Authorization: "token #{oauth_token}", Accept: "application/json")
      .patch(data) (err, res, body) ->
        if err
          msg.send "GitHub says: #{err}"
          return
        issues = JSON.parse(body)
        msg.send "Done"
```
