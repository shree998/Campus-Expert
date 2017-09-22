# GraphQL

### S1 ~00:00.000
> Yeah. Okay. Sweet. Let's do that. So first of all, I guess we should introduce ourselves. So I'm Will. I'm a Campus Expert from the Fall 2016 cohort. And helping out today also is Brooks, who is a platform engineer. Do you want to briefly introduce yourself?

### S2 ~00:16.845
> Definitely. My name is Brooks. I am based out of New York, and I'm a platform engineer at GitHub. I've been working on the GraphQL API, that Will's going to be discussing, for almost a year now. Yeah. If you have any questions or anything, feel free to ask in Slack or here in Zoom.

### S1 ~00:37.563
> So yeah. You probably know a lot more what's going on than I do. It's going to be fun. Okay. Cool. So I first gave this workshop at MLH Prime Europe, two weeks ago now, and it was super fun, so we thought we'd do it again. It was kind of made for that occasion, so we'll see how this will work out now. But I think it should be super fun nonetheless. So the way I want to do this is basically I'll go right from the basics, from what an API is, just in case there's anything unclear about that, to kind of a brief intro of GraphQL itself, and then the GitHub API on top of that. And I will have some kind of fun challenges of playing around with the API that, yeah, hopefully, we'll leave you wanting to use nothing but this. And that's really the goal as well, so we're not going to cover every single detail of the GraphQL added specification. But the idea here is, really, to get you excited about some parts that exist, and then you can go and explore everything else as well.

### S1 ~01:37.097
> And also I should say as a slight caveat, we're only looking at the client-side half of GraphQL, so there's both a server and a client-side aspect to it. And the server-side is also super interesting, but we'll only be looking at the client-side as we're the ones consuming the GitHub GraphQL API, we're not adding anything to it. Feel free to ask any questions throughout this. There might be some things that are unclear. So there's a few ways you can do this. You can either ask straight away, or you can ask into Zoom chat, and Brooks will be monitoring that. And we also have a TED Talks channel in Slack if you want to post any screenshots or anything like that once we get to the challenges. And then kind of Brooks will be monitoring that as well. And so we can kind of get through it and address everything in kind of a neat way without having to stop too many times.

### S1 ~02:27.540
> One thing that I'd recommend straight at the beginning is opening the gist which is at the bottom-- sorry, no. The gist itself which was the pre-workshop instructions. And then there's a link at the bottom here which is a repository I set up for this workshop. And that's going to be useful for later. So I'll recommend opening that now so you can check back later. I hope everyone on the call has done the pre-workshop instructions, otherwise definitely do that now. It does take a little bit of time. But just start with that now. Has everyone done that? Yeah? Roughly? Show of hands-ish. Okay. Cool. Cool. We'll run with it. Sweet. Sweet.

### S1 ~03:12.433
> So let me continue with this here. So I did a brief intro just now. But just to do it again, I'm a student at UCL. It's part of my kind of community apps-- part of Campus Experts was the technology society which I'm about to hand over to someone else. And yeah, I just talked about Campus Experts. So I am extremely qualified to give this workshop because I once answered a stack overflow question. Which has not been accepted, but it has gone upward. So there's all my credibility right there. And yeah. We're going to have loads of fun just like this octocat. So starting off with kind of APIs, right? I assume all of you will have some knowledge with this just because they're all over hack-a-thons all the time, and they're super useful, but just in case, just to go kind of lay a basic foundation here. API stands for Application Programming Interface, and the way I like to describe it is like a gate to another world. So essentially it makes its-- or APIs make it super easy to programmatically interact with another resource.

### S1 ~04:18.906
> So a few examples we have there is it would be super hard, for example, to in your own code have an image and maybe identify what's inside that image. And you have to write some really complex kind of machine learning computer version algorithms to do that. But you could also just use the Clarify API, send them a link to an image, and then they'll send you a bunch of tags back. So if you sent them a picture of a dog, they'll say like "dog," "animal," stuff like that. So things that are super easy like that. You can use the AWSAPI to spin up a bunch of servers for example. And you can also use the GitHub API to maybe if you have a personal website, and you want all your recent projects listed there, you could use the GitHub API to fetch all your recent repositories and just display the names of those on your personal website. So that's a very basic kind of API intro.

### S1 ~05:07.231
> Now, the way this mostly works at the moment is with REST. So REST is kind of, not a standard, but a very kind of common framework of thinking around how to design APIs. And essentially, the way it works is there's a resource, which is this URL right here. So we have the very standard URL kind of setup, there's a path, and then maybe there's a [inaudible], which in this case is an API key. And you can send an HTTP request to this, and then you get a bunch of results like this. And this is very much truncated as well. There's a lot more to this here. But essentially, if you want to interact with this the way in your own program, the way this works is you send a request to it, you see what kind of the response looks like, and then based on that example request that you made, you can pass that JSON, which you get in return, and say, "Oh, okay. So I'm interested in this overview here of this movie." And then you can access that in your code and use it for something else. So that's kind of they way REST works at the moment.

### S1 ~06:13.489
> It's slightly different with GraphQL. So what we just saw there was essentially-- if I could just go back for just a second as well. The first part is the request, and then this bottom part here is the response. In GraphQL, it looks slightly different. So the request, which you might find very odd if you're used to REST is just this-- essentially it looks like a JSON object, but kind of the values are missing. And that's kind of what it wants to be as well. So the idea is that the request and response are very similar and that you only get in response to whatever your request was, the things that are in the request. So as you can see here, I mean, this is a very basic example, straight from the GraphQL website. But you only request for the name, and you only get the name back. So you kind of move to a slightly more complex example-- this actually uses the GitHub GraphQL API. And you can see I'm doing a query there. I'm logging in with my-- or I'm creating a user which is myself, which is the username xoneco. And then I'm justifying a bunch of feels as Campus Expert, as employee, and I want the last three repositories. And that's exactly what I get back. For all the values that I requested, I get the-- oh sorry. For all the keys I requested, I get all the keys and the values back as valid JSON.

### S1 ~07:32.272
> Now, this is also kind of maybe the hardest part about understanding this at this level, is this kind of edges node thing, which you can see in the request example there. And I'll get into that in a little bit more detail there, but essentially whenever you see that, you can assume that what you get back is kind of an array. And it's essentially an artifact of there being some kind of pagination. Essentially, the way the GraphQL API is designed, you have-- for any kind of array, it's built for scale, so it can be assumed that there's infinitely many, in this case, repositories. So that means you wouldn't want to return that, that would be a massive response, it would slow down everything massively. So you just have to specify, and as I do here, last three, so it only returns the last three repositories. And then this edges node comes in as kind of a connection to that new node which is the name, for example. So we go from repositories to name or from the user to repositories, and that's kind of the connection.

### S1 ~08:37.860
> Okay. So moving on slightly as well to how fundamentally this works is, I guess, this is still an HTTP request. There's no magic about that, and we'll see that later in the challenges individually as well, but it's still HTTP. That's the fundamental thing, and that's also the reason why we want to do it in that kind of graphic [you'll set up in a second?]. So just to compare this as well to what we have in the current GitHub REST API, which is the more commonly used one, currently in version three. So let's try and do something like this which is just kind of repositories and see what we get. This is GraphiQL in a second. This is post-[inaudible] which is a nice tool to kind of make API requests and see what they look like before you implement your own code. I've already set this up here with kind of the values I need to query my own user, and you can do that in the GitHub settings as you probably did set up initially.

### S1 ~09:40.203
> So let me just send this off now. So as normal, you have the resource which is just this kind of URL, it's a normal get request. And what you get back is a ton of stuff, so much stuff. So regardless of what my application wants to use, maybe all I want to do is kind of get

kind of a specific repository and then get the URL for that. But regardless of what I want, the way I access that is by querying this and endpoint which gives me everything, and as a result, I get all this data back. And chances are that, probably I don't need all of that, and I only need a very small subset. That's one of the first reasons that makes this so much better. So again, all you send here is what you need, and all you get back is what you asked for. And in addition, it's also much more difficult to kind of request a specific piece of information. So the GraphQL API makes it easier to navigate kind of the graph structure, whereas with this, maybe you want kind of-- so this is made by a friend, right? [Fice?]. That repository we collaborated on. Maybe I want to see all of his repositories. If I want to do that, I would have to make another response asking for kind of his details. With GraphQL, that's a lot easier, and you can do a lot more in a single response and a single kind of request-response cycle. 
### S1 ~11:05.754
> Okay. So a little bit of history on GraphQL as well. It was initially built by Facebook as part of the revamp of their iOS app in 2012, and the goal really was to give power to their clients. So, as opposed to kind of the service [site?] implementers having to think, "Okay. How do we structure our endpoint, so that it makes the most sense to the clients to consume?" Now you have a single endpoint, and the clients define essentially what the views look like because there's--

### S3 ~11:40.879
> Was there an [awful?] sound from [inaudible] or just me?

### S2 ~11:43.987
> Yeah. I lost it too.

### ### 54  ~11:46.625
> Okay. He's gone.

### S3 ~11:48.277
> We've lost your sound about five seconds ago [laughter].

### S1 ~11:51.506
> Okay. That's funny. Is it back?

### S2 ~11:54.343
> Yes.

### S1 ~11:55.154
> Okay. Cool. What's the last thing you heard? Hello?

### S3 ~12:03.314
> What was the last one we had?

### S2 ~12:04.498
> We're all just scratching our head. We were following, but I can't [crosstalk]--

### S1 ~12:06.607
> No worries. Okay. I'll just do the last section again. So power to the clients makes it much easier for clients to-- for developers of Facebook to build the iOS app essentially and allows the developers there to kind of ask for any kind of data without there having to be a specific endpoint for it or without them having to ask the server-side developers to please make a specific endpoint. You can just define it yourself. And that's allowed them to essentially scale better. It's made it more efficient. It's made it more simple. And those are really the features that kind of GraphQL comes with. That's a part of the reason why they built that. So in kind of the first instance, it seems more natural to make requests that way. Because you're not asking for just something and then you get everything and then you extract something out of it. But you really only ask for what you need for it, so it's kind of better in that sense as well. But by making this kind of own API system, they've input other cool things like type system, introspection, which kind of gives you all the [inaudible] generated documentation which GitHub has made extensive use of as well. And there's other cool little features that you can just get from implementing your own system like that.

### S1 ~13:17.398
> So it kind of-- GitHub history as well a little bit. GitHub launched the first major, public, GraphQL API. So Facebook only used it internally, loads of places have used it only internally. I worked at a startup in the summer where I built a GraphQL API also just internally. And GitHub made waves because it was the first major public one. And there's a great talk by Kyle Degel that I put in the issue as well that you should watch because it's a super interesting story. And that presented at GitHub Universe back in October, and it's currently still in kind of early-access-anything-might-change mode. But it's already a lot of fun to play around with, and that's what we're going to do in a second.

### S1 ~13:54.459
> Now, moving on to GraphiQL. So this is the tool that hopefully you downloaded, and I'd suggest that you already kind of start play around with it a little bit, because there's a few cool things that you can do. And the kind of biggest hidden feature that I'd say is control space. So if you haven't discovered that yet, just give that a shot. So if you hit control space, you get all these things that you can query for, and that's a massive help in kind of designing your query. So, for example, type viewer, and then log in, and then just kind of-- same autocompletion menu, and I get my own username back. And I said earlier that I wanted to use this one instead of the kind of web version, which exists as well, and it's also really good, and get a GraphiQL explorer. But this one is really cool because you have to put in your own token, whereas with the online version, you don't, and it just automatically does it using kind of [inaudible] and it prefills everything. So it's a little bit more magical. But the point I really want to stress here is that this graph drill thing isn't just some weird, abstract query that happens somewhere in the background. This is literally something-- this body is just the body of a normal post request. You send it, and you get this back as a normal response. And this is a normal HTTP header. There's no fancy thing going on. And hopefully you having to input that header yourself kind of made that a little bit clearer. And queries, you can all send command enter, fairly standard.

### S1 ~15:33.104
> Okay. Cool. So now we'll go through some examples. I'll just do that like this. That doesn't work. We'll go to some examples of how you can use it, and then we can go to the challenges. So this is, first of all, find full name of any user. So feel free to try this as well, but what I'm just going to do here is I'm going to query user. Let's take Joe Nash because he's here-- and that's not how you spell Joe Nash. And then we just put in name, and it autocompletes nicely, and then we get Joe's full name, and that obviously works for any kind of user. Remember these, because these are going to be slightly useful for the challenges as well. Now, list your repositories. So this is another one which you can kind of do it two ways as well, but I'm just going to do it in the standard way. So that's my username, and then I want not one repository, but repositories. And this has paginations, so I'm going to specify, in this case I want the last 10, and it's a connection, so we need edges node, and at this point maybe a name, and let's say when it was created. And those are the last 10 repositories that I made, including the 1 that we have open in the tab at the moment.

### S1 ~17:12.459
> Cool. So those are the two example queries that I wanted to go through for the beginning, and now we're going to get to the fun part. Is everyone ready? Challenges. So, first one is list your repositories and their languages. Slightly similar to what we just had just now, but I'm going to leave this open while you go and try that yourself, and then we'll go through the sample answer at the end, but feel free to just start doing that now, yeah. When you're done, feel free to post it in the Zoom chat. And as mentioned before, Brooks will be in kind of the TED Talks channel and Zoom helping you out if you have any questions, and Matt Burman who was at the Prime talk as well-- if you want to help out as well. I mean, you were one of the quickest to complete everything over there. So feel free to help out.

### S2 ~18:04.616
> So part of the reason we have the TED Talks challenge is because you can't post things like screenshots and stuff in Zoom. And you have a new [inaudible] our screenshot, do that in the Slack. Or tandemly, you could also screen share on the Zoom, we could do things that way.

### S1 ~18:22.755
> Yes. I will do two minutes for each of them, or something like that.

[silence]
### S1 ~19:52.730
> So that's about two minutes, I think. is anyone still having trouble? Is it all super clear? I can't see the Zoom chat at all, but. [silence]

### S1 ~20:22.446
> Is everyone kind of happy with that? I can't see the chat.

### S2 ~20:30.355
> Sounds like a few people are still working through authentication. I dropped a link to the GraphiQL's board, the web-based version that Will pointed out. That might be a quick fix if you want to try and dive into the queries.

### S1 ~20:44.071
> Yeah. Definitely. So I mean, that was just to make it clear that the thing is HTTP, but feel free to use the web version as well if the MPM1 doesn't work at all. Okay. Cool.

[silence]
### S1 ~21:04.733
> Oh, yeah. Some of the key bindings might be different. All right. I'm just going to go through the sample answer now if you want. So the idea is, List your repositories and their languages. We just did something kind of similar, except that there's kind of one more layer of complexity as well. So right now we ask for the name and the created time, and now we want the languages. And there can be, as far as kind of the API is concerned, there's also infinitely many, so we want to see only the first three, or it's kind of [inaudible], so we only want-- in this example, we only ask for the first three or the first however many you want, and then we want just kind of the connections, we need edges node again. And then we want the name. And you can see, okay, this repo called Enigma Spaces, CSS, JavaScript, HTML. It's kind of the cool-- the way that a query works over here. Something you can also do, which I kind of discovered as part of going along with this is you can also kind of query for the color, which is cool. So [again?] each language, as I'm sure you know, has a color. And you get the hex representation of that if you want. I'm sure you can build some really cool things with that.

### S1 ~22:22.477
> All right. Moving onto the next one, issues on the Facebook React repo. So again, feel free to just get kind of the first three or so issues, and the latest three if you want on that specific repository. And I guess give that a shot first with kind of the control space or function key space, whatever the key binding is an option until you get that little popup menu. But there's also an example of this on the readme end of the repository that you have opened. So if you want, you can take a peek at that as well, if you want. But first, give it a shot just like that. And we'll do another minute and a half.

[silence]
### S1 ~24:29.082
> Right. That's about that. How is everyone doing?

[silence]
### S1 ~24:48.389
> Everyone kind of happy with that one? Just give a thumbs up in the chat as well if you got it. Sweet. Sourab got it. All right. Nice. Okay. Cool. I guess I'll go through the sample answer again for this one. Or I mean, usually, with GraphiQL, there's like multiple ways you can do it, but this works well. So, in this case, we want one repository, and it has kind of two kinds of inputs. We have owner, which in this case is Facebook; and then the name of the repository, which is React; and then we want the issues plural on that, and that is paginated, so let's go for the last 10 or so; and that's connection; and then let's go for the name. Oh, I think it's called title. Yeah. I think we had some problems yesterday with release 15.5. They didn't tell enough people about it, or they didn't test enough things, so a lot of issues with that.

### S1 ~26:12.791
> All right. Cool. Does that kind of make sense for everyone? I hope so. And maybe a nice, fun thing that you can do on top of this here as well is creating for labels, and again, that's another layer deep into it. And this is just-- maybe one of the coolest part of GraphiQL is you can just-- it's so fun to play around and see what the different connections are and where it leads you. So we have an ID here. We have probably a name. There we go. A lot of issues don't have labels, but here we have one bug. So that's always something that's super fun to do if you want, just play around. Okay. Next challenge, find your own database ID. So this is a cool one because I think it doesn't work anymore in REST. I'm not sure, correct me if I'm wrong here, Brooks, but it does work on GraphQL. And again we'll do like two minutes here.

[silence]
### S2 ~27:26.113
> The database ID is pretty interesting because it represents-- it's the actual primary key in the database. So it's like your position of when you joined GitHub. So there are people out there-- actually, like Database ID3 is GitHub, the organization.

### S1 ~27:44.800
> Oh, wow.

### S2 ~27:45.640
> Yeah. It's pretty interesting to see who started out first. I'm like 400,000-something.

### S1 ~27:51.809
> Oh, wow. I'm like seven million I think, or something like that [laughter]. But yeah. This is why I like this one, and we'll have a cool one in a second about this one as well. Not everybody knows about it. But yeah. So Brooks, is this still available on REST? Or is it only-- because I know it's deprecated on GraphQL as well?

### S2 ~28:07.459
> Yeah. So the reason that we deprecated database ID in GraphQL is because we don't-- there's a formal ID, which is a global identifier across all of GitHubs API, or at least the GraphQL API. The database ID-- when we're looking up our own database IDs here, that's specific to like the user's table, so only the users. But the database ID3 for the GitHub organization may conflict with repository ID3, which I think, ironically, is also GitHub - GitHub, the organization/GitHub, the repository. Yeah. So Database ID, the reason we deprecated it is just because it's not global, whereas GraphQL has this concept of a global identifier that you can use to query against any sort of object, which is kind of neat.

### S1 ~28:55.007
> Yeah. And we'll try that one in a second as well with a slightly different approach, I guess.

### S2 ~28:59.362
> Cool.

### S1 ~29:00.699
> Cool. Again, if you're done, if you got this, find [the end of the database?], just leave a thumbs up in the chat as well, and then we get a rough idea of how it's going. Yeah. Parts of the end of it. So yeah. That's a great idea. Wow. That's a good one. So it's just a counter from when you started. Wow. Nice. Oh, hey, [Olly?] Cool. Okay. So I'll just run through the model answer again. You can do this in two ways. I'll show you the slightly different way which is also-- I think you can do viewer, and then-- so this is me. The viewer is just the query that-- this token that I am, and that token is me. And that has a database ID associated with it as well. And that's this photo, so you can obviously do it the other way which is just the normal user login. And you'll do that in a second as well, so this is probably the more useful one to remember. Oops. No, that was correct. Database ID. There we go. Cool.

### S1 ~30:24.254
> All right. Moving on to the next one. Let me quickly check what that is. Okay. So this is the kind of main. This is maybe the most difficult challenge because it doesn't just involve GraphQL. But this is the one we actually had a major prize for, slightly major. It was a cool book that [Madd?], actually, who's on here as well, won at the MLH Prime talk. So get ready for this challenge. Find the database ID of the GitHub CEO, and check whether he's a Campus Expert. And again, we'll do maybe two-and-a-half minutes here.

### S3 ~31:03.689
> That moment you realize Campus Experts in the API.

### S1 ~31:07.348
> I know, right? That was like, "What [laughter]!"

[silence]
### S1 ~31:32.603
> And I should maybe say that this is the current GitHub CEO. There isn't a user called GitHub CO. It's an actual person. And I'll just go to the chat as well.

### S2 ~31:43.053
> Allegedly, there's--

### S1 ~31:45.578
> Allegedly. He has us on octocat as well. Well done, Olly.

### S2 ~31:57.423
> We should fix that. He is not hireable right now [laughter].

### S1 ~32:01.689
> Yeah. So this was a fun little thing as well that we discovered in the MLH Prime talk [laughter].

### S3 ~32:11.665
> So what's database ID1 assigned to then?

### S1 ~32:17.866
> Yeah.

### S2 ~32:18.121
> Good question.

### S1 ~32:18.067
> Good question. Let me look.

[silence]
### S1 ~32:40.061
> Again, feel free to post a thumbs up in the chat.

[silence]
### S2 ~32:56.382
> Database ID one is our old CEO, Will [Jambo?].

### S1 ~33:03.579
> That makes sense.

[silence]
### S1 ~33:21.192
> [inaudible] I have actually no idea what the time is. But I assume we're roughly at that time frame again, so I'll do it again. So what you need here is just essentially find out what the username is of the GitHub CEO, and he's called defunkt, spelled like that. And you can get the database ID just by having that query that you had already. And then we have is Campus Expert, which is a real thing, part of the API. It's really cool. And also say [inaudible] because that was the whole challenge. And he is not a Campus Expert yet. Just to kind of show you that. That returns true here. And the cool thing that we were just laughing about now maybe that you missed, that we discovered in the MLH Prime talk is that at the moment, he is hireable. So if you want, send him a message. Hire him. But yeah. So that's, I think, a setting you have on your profile. Brooks, that correct? Joe? I don't know. You can say whether you're hireable yet.

### S3 ~34:21.990
> Yeah. Well, it was at one point. Is it still there?

### S2 ~34:26.100
> It is somewhere. I'm not sure where. I think it's in your settings.

### S3 ~34:31.345
> Yeah, it's in your settings.

### S1 ~34:33.358
> Cool. Yeah. So this is a fun little thing that we discovered. Okay. Sweet. So now, moving on, so these were all the kind of query challenges, but now you might say, "Hey, this is all great. But REST can't just read. It can also update or initiate processes or anything like that." And obviously, GraphQL can do that too. In that case, it's called mutations. And essentially, the way you can think about it is it mutates a resource. It changes the way something is stored. So it's just like a PUT in REST, it's actually, or a PATCH. And what we're going to do here is add a [react?] in a second. But first of all, let me kind of show you an example of how that works, or what kind of the basics are because it's slightly a different true query.

### S1 ~35:17.905
> So Brooks was just talking about this global ID that you have. And essentially every single resource in GraphQL has this global ID, which is this MDEX so on and so forth thing. And using that, you can essentially have mutations. So let me just first of all find that ID. So the way I have this example is do a normal query on the Campus Expert's repo. That's a steam modification. On the Campus Expert's repo, my cohort. And I'm going to specifically query for my community assessment. So that is a pull request, so I want maybe the first 20 pull requests. And that is a connection. So have this and then we have the ID, which is what we need. And then the name, just so I can actually-- I think it's title, again. Yeah. Just so I can identify it. Where is it? It's this one here. So I'm going to copy this, and I'm going to kind of structure the mutation, which is slightly different. Being in this case, you have to have the mutation prefix. And then we have this add reaction, which has an input, which is another object; and that takes subject ID, which is this; and then it takes content, and that can be if you do control space, it can be those few emoji that you can actually add on issues in pull requests at the moment; and then we'll have this. And then what we also need is to specify what we want back in the response. So in this case, we're just going to ask for the, is it-- oh, yeah. We want the reaction object back, and that has content and ID.

### S1 ~37:22.967
> So if you look right now on this issue here, people played around with this as well. One has a few reactions already. But right now, I have not interacted to it. But now, [if I ask to do?] this code, send that request stuff, there should be a web poke, so it shouldn't [be added?] automatically, but let me just refresh. And there you go, I have liked that poll request. What we're going to do is something similar to that, but essentially it's another challenge. So use this example. There is also an example on the repository that you can use, but that won't lead you fully there. Let me just introduce the challenge real quick. So get the latest issue from that repository that you have opened, GitHub GraphQL Workshop repository, which is under my username, xoneco. Get the latest issue and like it. So two steps here. First, you have to kind of find out what that global subject idea is and then you have to send that mutation request off and like it. So that's going to be slightly more difficult because it's two steps. So feel free to ping us in the chat.

### S1 ~38:39.389
> So I'll say it one more time, get the latest issue from the GitHub GraphQL Workshop repository and like it. And I'll open the issue up here, so we can see the counter increase. And again, we used this the last time as well, the Prime Workshop. So there is some stuff there already. Now, we've come full circle because you no longer have to send likes and Zoom chat, but we can set them on the GitHub. [silence]

### S1 ~39:44.565
> And obviously, if you have any questions, put them in the chat, or screenshots in the chat. And feel free to use the example from the repository as well.

[silence]
### S1 ~41:05.871
> Yay. We have the first like. Okay. And I missed that update, but woo-hoo. Well done, Sourab [laughter].

[silence]
### S1 ~41:36.297
> Yeah. And I'll just go for it to send any other [message?] as well [laughter]. Maybe get some nice background talk while everyone's doing this. Brooks, can you share anything on why those five emojis specifically [laughter]?

### S2 ~41:51.405
> That's a great question. It was very highly debated. I don't have a great answer, but I think that the reason we didn't use all of the emojis, was just because of the database design of it. It's actually reactions have proven to be one of the most complex parts of GitHub's codebase, and the reason is because when you get a very volatile and a very busy issue page, when each comment gets a bunch of reactions on it, those are database calls. And it needs to say, for each individual issued comment, please fetch all of the associated reactions. And the wider range of reactions that you have, means even more database calls that have to happen. A total kind of unrelated story that's funny - and I'm not sure if I'm allowed to share or not, but I will - the first time I was ever on call. So we have a pager at GitHub, and so if something goes wrong, you're amongst 30 other people that will get paged if the site is going down or something like that.

### S2 ~42:59.882
> The second time that I ever got paged was because there was this one particular page, it was actually an issue in a particular repository, that was pretty much bringing down the website. And the reason is because it has so many reactions and so many issue comments. And basically, as you're getting paged you're like, "Oh my gosh. What the heck is going on?" "I have no idea." And so, it turns out the reason there were so many comments and so many reactions is because the Pokemon Go creators changed the API and made a breaking API change and broke a ton of integrations. And so all of these people were super upset. So there was pretty much one day where Pokemon Go brought down GitHub [laughter]. It was just my luck that I had the pager that day too.

### S1 ~43:55.237
> That's good. Okay. And we had a few more reactions as well, BlueHatBrit and elliotwhitehead. Nice. That's cool. And I think also very relevant to this as well. If I remember correctly from Kyle Degel's GitHub Universe talk, reactions were actually the first thing that were implemented using GraphQL. Is that correct?

### S2 ~44:20.012
> That is. Exactly.

### S1 ~44:20.919
> Yeah.

### S2 ~44:21.885
> Yeah. And now today, interestingly enough, even some of our REST APIs which are returning like RESTFUL resources, right? Some of those, the actual code behind them is using GraphQL which is kind of a mental shift.

### S1 ~44:32.846
> That's really cool. Yeah. So that's one super important thing to point out. It's being used in production, literally right now. So that's really, really cool.

### S2 ~44:45.188
> Yeah. All new features are built in GraphQL.

### S1 ~44:48.750
> Oh, wow.

### S2 ~44:48.423
> The projects that is entirely-- like project boards, those are entirely in GraphQL. The commits page, whenever you're looking at the list of all the commits that's in GraphQL, topics, all that good stuff.

### S1 ~45:00.756
> Yeah. That's awesome. I think there's some stuff that you can't yet do with GraphQL. There was one person at the workshop that said you can't add comments with GraphQL to issues, but maybe that's coming soon.

### S2 ~45:12.373
> Yeah. We're working on kind of getting parity with the V3 API, but it will take some time.

### S1 ~45:21.516
> Another heart. All right. Cool. So I'm going to go through the response here as well with kind of the model answer, if you want to follow along. With that, so the first stage was kind of actually find out what that global ID is, so we want a specific repository which has me as the owner, and the name is GitHub GraphQL Workshop. Yep. That's actually what it's called. And inside that we want the last one issue and this is a connection. We want issues, plural. Common theme. And that's a connection. And we want the ID and so we can identify it, the title. Title. So there we go, that's the correct one. And then we can just copy this ID and use that reaction query-- sorry, reaction mutation we had before, we can also just copy straight from the repository, of course; and subject ID place that in there; and as content we are going to go with thumbs up.

### S1 ~46:55.541
> By the way, there's also-- right here in those kind of documentation, there is the thumbs up emoji as well. Something that I forgot to mention which is super useful is this other thing in here called [docks?], which is kind of the-- you get that with GraphiQL, as I mentioned, automatically with all these kind of introspection features that it has, and you can actually go through all the different things here that you can do. So somebody would run repository, owner, like what actually is that, what's a string? So that's super, super useful to check that. Anyway, finishing off this here quickly, we want back the reaction object, and that has an ID and content, and we execute that. It runs, and it successfully added my thumbs up here. Brooks got it, and Olly got it. Woo-hoo. Okay. Right. Perfect.

### S1 ~47:53.387
> So that's kind of almost the end here, that's all the challenges done. What I want to leave you with is kind of just this website. There's so much more to GraphQL than what we just covered. There is a bunch of other kind of parts to it and how you do queries. It'll let you do more complex things and that solves some of the challenges that you get when you play this to its holistic extent, the kind of queries and mutations we've had so far. And you can go there and check that out, and there's a ton of learning material, it's really nicely designed. They re-did it for the GitHub GraphQL launch in October, and it's awesome. And then we see there's the whole server-side implementation [to this as well?]. So the cool part here is not just consuming the GitHub API, but if you want to build your own GraphQL API internal use or kind of public use as well, it's very different from how you would have previously done that because you have to resolve each field individually essentially, and there's loads of cool libraries. GitHub obviously has or contributes back to the Verbi One, there's a great Node one, there's a Python one called Graphy that I've been using. There's loads of amazing resources out there, and you should totally check them out. I'll post a comment to that [Work Trub?] issue which has a link to the website and also to Kyle Degel's talk where he introduces the GitHub GraphQL API universe which is an amazing talk. Dan Schafer from Facebook who's one of the creators of GraphQL speaks there as well, and that's extremely worth watching, one of my favorite talks from Universe as well. But besides that, thank you so much for coming along and enduring the challenges. It was a lot of fun.

### S3 ~49:25.852
> Thank you so much, Will, for helping out. If y'all have any feedback, I'm sure Will would really appreciate it and you can drop back to us in the Slack channels.

### S1 ~49:38.028
> Yes.

### S3 ~49:38.409
> And yeah, pretty much [this is cool?]. Thank you again, Will. If we could do a full [clap on] here. Like an applaud [laughter].

### S1 ~49:48.285
> Also if you have any questions about it, feel free to ping me or if Brooks is happy to kind of answer some more questions on Slack as well then hopefully--

### S2 ~49:55.017
> Yeah. Sure. I have another six minutes or so, if anyone has any questions in here I'd be happy to answer them or on Slack as well.

### ### 54  ~50:03.078
> So I just have a quick question, as far as-- I was able to follow along and do all the challenges with the web version the E70. I was just curious what I need to do to get myself indicated with the GraphiQL?

### S1 ~50:18.086
> Yeah. Do you have the-- so do you have the GraphiQL desktop version working?

### ### 54  ~50:23.581
> Yup.

### S1 ~50:24.315
> Okay. Sweet. So there's instructions in the Gist - let me find that - which kind of show you how you can get the token inserted essentially. So let me post the link to the Gist which I'll have in a second. There we go. There's a bunch of steps. Essentially, you need to join the early access program, and then you can generate a token for yourself with a bunch of specific things, and then you can insert that. Usually, Edit HTTP Header is here. At the header, you call it authorization, and then you write bearer and then the actual token, and then that will work. And that's exactly the same in kind of any code as well, if you want it to do some [piping?], you can just do a post-request. This is the body. This is the header. And then the actual endpoint is this: api.github.com/graphql. And it'll work exactly the same way, and you get this back as well at JSON.

### S2 ~51:42.565
> Cool.

### ### 54  ~51:45.519
> Thank you.

### S1 ~51:46.638
> Cool. Any more questions?

### S5 ~51:57.063
> I'm going to say something. Someone's [inaudible] the bucket, to put it lightly, the JavaScript is apparently wrong. It just keeps hanging at "JavaScript error occurred" in the main process.

### S1 ~52:09.378
> Is this the NPM-downloaded one?

### S5 ~52:12.344
> Yeah.

### S1 ~52:13.328
> Yeah, I wasn't actually able to test that out properly, unfortunately. But yeah. Something might be wrong with that one, then go and use the web version.

### S5 ~52:22.875
> All right.

### S1 ~52:22.889
> Hopefully, that'll be fixed soon. But yeah, as I said earlier, the whole point of the desktop GraphiQL version is just kind of make it more clear, that there is not like any fancy stuff. It's just a normal HTTP request. It's just done slightly differently to how you'd be used to with REST.

### S2 ~52:39.200
> Which version of GraphiQL do you have?

### S5 ~52:44.014
> Me?

### S2 ~52:45.283
> Yeah. Yeah.

### S5 ~52:46.190
> [I believe?] 5.1.

### S2 ~52:51.813
> Oh, I see.

### S5 ~52:52.436
> I downloaded [inaudible]?

### S2 ~52:53.267
> Oh, yeah. Because I downloaded it from the instructions before, but I ended up with 1.415. That's interesting.

### S1 ~53:00.822
> Yeah. And I think there're some problems as well. It works on OS X, but it doesn't work on Linux or Windows or something, I'm not sure.

### S2 ~53:07.213
> Oh, right. He could be on a different [inaudible].

### S1 ~53:09.667
> Yeah. But essentially the web version works very similarly except that there is a little bit more magic in the initial authentication. Anyway, any more questions?

### S3 ~53:29.984
> Well, I guess not. One note, so we haven't yet got what the TED Talk would be next week, but we've talked to a couple of people. There's a chance it's going to be either web audio because some of them from Spotify is in town next week, or it might be something on GIS stuff or web GL. However, we do have now confirmed that the training content next week would be technical writing with a combination that serves this training team and the docs team at GitHub. So we've got some interesting content next week either way. So yeah. I'll see you all next week or during office hours. And again, if there's any further questions, you know where to find Will and Brooks [laughter].

### S1 ~54:14.998
> [crosstalk] [laughter].

### S3 ~54:18.728
> Thanks so much for coming everyone.

### S1 ~54:19.549
> Thanks for coming.

### S2 ~54:19.688
> Thanks, guys.

### S1 ~54:20.834
> Bye-bye.
