# Module 09 - Hubot Script


## Hubot script searches for railscast with the given keyword and pastes the top 5 result in the chat. 


### railscast.coffee

code: 

```
# Cheerio is used to parse the html and extract data
# Commands:
#   hubot get me <railscast keyword>

cheerio = require('cheerio')

RAILSCASTS_URL = "http://railscasts.com"

# Script

module.exports = (robot) ->
	robot.respond /get me (.*)/i, (msg) ->
		q = msg.match[1]
		URL = "http://railscasts.com/episodes?search=#{q}"

		robot.http(URL).get() (err, res, body) ->
			$ = cheerio.load(body)

			$('.episode').slice(0, 5).each ->
				msg.send "Title: " + $(this).find('h2 a').first().text().replace /^\s+|\s+$/g, ""
				msg.send $(this).find('.info .number').text()
				msg.send "Link: " + RAILSCASTS_URL + $(this).find('h2 a').first().attr('href')
				msg.send Array(4).join '~'

```