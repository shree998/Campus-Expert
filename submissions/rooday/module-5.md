# ChatCloud

ChatCloud is a Node.js/Express.js web-app that allows you to create wordclouds from any Facebook chat. It uses the [facebook-chat-api](https://www.npmjs.com/package/facebook-chat-api) package to simulate a login to Facebook and scrape messages from chats. The messages are sent from the Node.js server to the client over [Socket.io](https://socket.io/). It then uses [WordFreq](https://timdream.org/wordfreq/) to generate counts of individual words, which is then fed to [wordcloud2.js](https://timdream.org/wordcloud2.js/) to create the visualization.

***NOTICE:*** ChatCloud is currently nonfunctional. Facebook has increased security around logins, and so the facebook-chat-api package is no longer able to get access. The plan is to convert the ChatCloud service into a Facebook chatbot using [this guide](https://developers.facebook.com/docs/messenger-platform). Feel free to make a PR! 

## Installation and Usage

First, make sure you have [Node.js](https://nodejs.org/en/) installed. Then, clone/download ChatCloud somewhere and run `npm install`. Once that finishes, start the app with:

    node index.js

Once the app is running, navigate to `http://localhost:3000` in your browser (if the port is already in use by another app/service, you can change it at the bottom of `index.js`). Once the page is ready, login and input the details of the ChatCloud.

              Thread ID:   The ID of the thread/chat you wish to create a wordcloud of
    First Message Index:   The index of the first message in the chat history you want to include
     Last Message Index:   The index of the last message in the chat history you want to include
    
To find the thread ID, copy it from the url when you are in a chat. For example:

          URL:  https://www.messenger.com/t/1700528966629083
    Thread ID:  1700528966629083
    
For first message index, usually 0 suffices. Last message index is a bit harder. At the moment, it requires you to guess and check. Make estimates based on how long the chat has been in use, e.g. 100, 1000, 10000, etc. Be wary that large numbers will require longer runtimes to generate the wordcloud.

Once all the details are ready, press Submit and wait while the wordcloud is created (should look something like this).

[![Running](https://i.imgur.com/xTPFiz6.png)

## Running on Heroku
[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)  
A Procfile is included for deployment onto Heroku (or you can just use the button above).  
***WARNING***: You will likely receive warnings from Facebook due to "unrecognized login attempts".
