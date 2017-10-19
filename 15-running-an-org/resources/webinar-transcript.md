# Running an Organization

### S1\
[00:05.024]

> \[music\] So you've got an organization and perhaps you meet face to
> face a lot or you have \[inaudible\], or things like that, but you
> have a need to work with your organization outside of the times when
> you're able to meet. How do you do that? The short answer, or the
> tldr, is that you do it using GitHub. So this presentation is all
> about how to run your organization using GitHub. I'm Hector. My handle
> is hectorsector. I'm a trainer for the GitHub professional services
> team. I am based out of Orlando, Florida in the US. And in my spare
> time I like to visit theme parks as you might expect living in
> Orlando. My background is; I did a lot of work in higher ed. I've
> taught programming courses and I've also designed curriculum for
> programming course and math courses and before that, I was getting my
> master's degree in computer engineering at the University of Central
> Florida. So here's the basics of what we're going to cover. We're
> going to learn how to manage teams of people, how to communicate
> effectively, and how to get on the same page.\


### S1\
[01:09.832]

> So let's first talk about managing teams of people. This section right
> here is mostly going to be on the technical aspect of managing those
> teams of people on GitHub. So you're probably used to working with
> personal repository on GitHub and so I thought it'd be a good idea to
> highlight the two types of ownership that are possible using GitHub
> repositories. So on the left, you see what you may already be familiar
> with, which is a personal account, and on the right, you see an
> organizational account. Both of these are possible on GitHub and both
> of these can have repositories associated with them. There are some
> big differences between the personal and organizational, though. So
> with a personal account, we have a repository that's owned by an
> individual. You can only invite collaborators to that repository.
> Which is challenging if you're working in a team, because then you
> might have, let's say, a group of 5 to 10 collaborators, for example,
> and then as people enter and leave your team or enter and leave your
> organization or your group, it's kind of hard to maintain that. And
> then if you have more than one repository that these folks are
> collaborating on that becomes a bit of a nightmare.\


### S1\
[02:21.132]

> So the solution to that is to use an organization. In an organization,
> you invited the individuals to the organization. You group them into
> teams and then you give them access to the repositories that they need
> access to using those teams. Also, with a personal repository, you
> only have really two permission levels. You're either an owner of the
> project or you're a collaborator. Collaborate has a lot of-- has a
> very limited role, in term of they can't do things like delete the
> repository, for example. Whereas in an organizational model the teams
> themselves can have read, write, or admin permissions to specific
> repositories. So I could, for example, have read permission to a
> repository that another team is working on and I can have admin
> permissions to those projects that are near and dear to my heart. With
> a personal account, there is only that one admin, as I mentioned, the
> owner of the repository. With an organizational account, you can
> toggle that admin setting for the team, so that multiple people can be
> admins. Now both the personal and the organizational repositories,
> with those accounts you're able to do public repos and collaborators,
> add as many of those as you like. When you are a member of a team-- so
> you first have to be invited to the organization. So here's an example
> of the Campus Expert organization, and both Joe and myself are members
> of the Campus Expert organization, and that's enough for me to have
> access to the repositories that are public within that organization,
> but if for some reason I also needed to be able to access particular
> repositories, maybe have admin access to a subset of those
> repositories for example. I could be a part of say, a facilitator team
> and Joe could be a part of that team with me. But then Joe could also
> be a member of the reviewers' team. So each of these teams would
> probably have different access levels for different repositories. And
> you can use \[master?\] teams when you need finer grain control over
> exactly who is a member of which team, and when your organization gets
> large enough, when there's parent teams and child teams as well.\


### S1\
[04:38.787]

> This is a screenshot of what it looks like to give a team access to a
> particular repo along with their access level. So using this feature
> right here, any members of the training team are automatically going
> to get admin access to this teacher-bought repository. That makes it
> very easy because I don't need to manage membership for this
> repository by individuals. I could do it using the teams. Some
> recommendations that we've seen work for groups that are using GitHub
> to run their organization is to stick with a single organization. And
> it may be attractive, the idea of maybe different organizations for
> different projects, or maybe different organizations for different
> initiatives. But the more organizations you have, the more complexity
> you add to the whole issue. And so it means that your teams won't
> carry over from organization to organization. So all that benefit that
> I just described about organizing people into teams goes out the
> window, because you have to manage that separately in each of the
> organizations. Organizations are fully self-contained units, so they
> do not talk to one another in any way. So the more you can stick to a
> single organization, the easier your work is going to be. You can
> manage the repositories within that organization by making them
> private or public, and then by assigning people to teams and then
> granting those teams access to the repositories.\


### S1\
[06:09.559]

> There's also no need to fork and I mention this because if you're
> coming from an open-source world, for example, you're likely going to
> be used to a workflow that requires you to fork. If you're hosting a
> group that you manage on GitHub, it's a lot easier to grant access via
> teams and collaborators and allow people the ability to create their
> own branches and merge \[pool?\] requests and close \[pool?\]
> requests. And you might wonder, "Oh my gosh, but if I do that, what's
> going to happen? It's going to be chaos." And I think what you will
> realize is that it won't be chaos if you take a little time to just
> write some guidelines out for your community and what they should do
> when they gain access. Right? But you really want to foster that
> creative vision and that freedom for people to create branches and
> contribute and all that sort of good stuff. And just removing the
> forking aspect just takes one extra step out of the equation. Now you
> can still fork, maybe for members of the rest of the community,
> members that are not part of your organization. You can still have a
> forking workflow. But for the folks that are a part of your
> organization, think about whether you really need forking to begin
> with.\


### S1\
[07:17.230]

> Allow the people within your organization to create ad hoc teams. So
> this means that you can create teams for all sorts of things. So these
> examples here are based on how much of GitHub is using teams. So we
> have an all employees team, which all employees are a part of. We have
> teams that are project-specific and they're meant to be torn down when
> a specific project is over. We have teams dealing with people's
> geographic locations. So I'm part of a southeast US team, for example.
> I believe I'm also part of a Florida team. A lot of people create
> teams that allow them to identify with a special interest. Maybe
> Bladerunner \[inaudible\] or something like that, as well as teams
> that align with certain affinity groups. So, for example, we have a
> Blacktocats team, we have a \[inaudible\] team that could help. So,
> there's many different ways in which people can organize themselves.
> Allow people that freedom. It'll make it much easier to manage
> conversations across these groups of people and it'll make it more
> inter-connected.\


### S1\
[08:26.860]

> Now that we've talked a little bit about how you manage the people
> themselves, once you've got the people in place, what are some good
> practices for communicating, and how do you do so effectively? So,
> that's what we'll talk about in this section, and the first thing I
> want to kind of kick it off with is that the right tool for the job is
> really important for you to pick. So, for example, if you have a
> pressing issue for example, you have something that needs to be fixed
> relatively quickly. Like maybe within the hour. Perhaps for that, a
> Pull Request comment doesn't make sense or an Issue comment doesn't
> make sense, right, because it has some urgency to it. So, maybe that's
> a scenario where you check if somebody's online on Slack and you send
> them a message, or you @mention them as \[inaudible\] the entire
> channel, or you schedule a quick Skype. Sync up with somebody if it's
> phase because it's that important of an issue, right? However, if
> something really doesn't require immediate, immediate attention, there
> is a huge case to be made for the fact that you should be doing that
> work on Issues in Pull Requests. So, those are our appropriate formats
> for things that have to do with your projects themselves, and
> oftentimes don't underestimate the power of face to face meetings. So,
> if you're leading a group that has a geographical component to it,
> then meeting face to face is sometimes the best solution, and again,
> just because you've always met face to face if you're a part of that
> group, doesn't mean that that's the only way you should continue to do
> the work. Because that means people have to take time out of their
> lives to meet and when people don't show up, well, what happens? They
> need to be able to be caught up or they feel left out. So, even when
> you do meet in person, back it up with some sort of written record of
> that.\

### S1\
[0:12.972]

> So, I propose to you that you communicate differently if you're
> managing your organization on GitHub. You focus on inclusive
> communication. So, rather than forcing people to be there at that
> example that I just mentioned of a face to face meeting, be inclusive.
> Realize that some people may not be able to come to a face to face
> meeting, and so what do you do for them? Maybe you jot some notes down
> in an Issue. That's an example of something you can do. Rely on Async
> communication. Working face to face is awesome, but not everybody
> works well synchronously. There are folks, myself included, that
> thrive asynchronously. I love doing most of my work asynchronously.
> So, rely on Async communication as a backup, even when you do use
> synchronous communication, and as a record of what you talked about.
> Write everything down. Or, if you believe something strongly enough,
> you put a url on it and that's what we do at GitHub. No conversation
> happens really that doesn't have an Issue or a Pull Request backing it
> up. And also craft your communication for your future selfs. Think
> about how your team's going to evolve. Think about how your projects
> are going to change over time and write documentation. Write steps
> down so that you make your life easier in the future.\


### S1\
[11:28.023]

> Some things to keep in mind anytime that you have a message, is to
> think about the delivery methods. So, that goes back to using the
> right tool for the right job that I discussed a little earlier. Is an
> Issue the right thing? Is it a Slack message? Is it a face-to-face? Is
> it a Skype call? Is it, if you're actually contributing work, do it
> via Pull request. Maybe it doesn't need an Issue to start it with.
> Pull Requests is the right delivery method for that. Think about the
> type of content that you're developing. Is this good for written?
> Maybe it's a video. Think about the audience. And more importantly,
> not only the audience but the investment that that audience needs to
> spend on what it is that you are writing. Often times, you mean
> rewriting something for consumption within your immediate group so you
> can make some assumptions. But what if you could take the same exact
> documentation and write it in a way where an open source contributor
> could also pick it up and use it, right? So, think about that as well.
> And finally, think about using visuals. If you're not familiar with
> Markdown, become familiar with it. Use Markdown to style your text.
> Use emoji, liberally. Use images and Markdown tables to make sure that
> your point gets across.\


### S1\
[12:48.150]

> Here's just a couple of quick suggestions of things that we find works
> for us when we communicate asynchronously, and sometimes
> synchronously. So, the first thing is to include a TL;DR. We include a
> TL;DR, usually, at the top of every post or at the bottom of the post.
> If you're not familiar, TL;DR, stands for either, which depends on
> which one you subscribe to. Too long didn't read, or too lazy didn't
> read. And it's just a quick one-two sentence summary of what the
> entire post is doing. So, here's an example with Cinthia writing a
> TL;DR, for initial, it's a little bit longer than that.\


### S1\
[13:26.122]

> Identify the scope of your shift. So, I did this here in this issue
> where I was doing something pretty quickly. Something that didn't--
> wouldn't affect a lot of other systems, wouldn't change much, would
> just make life easier for a user. So, I kind of said, "I could shift
> this with one thumbs-up. That's all I needed. If instead, maybe, I'm
> changing the way that our team does something, or I'm changing a
> policy or procedure, what would I do at that point is I would say, ''I
> will not shift this until I have everybody's thumbs up, right?" So,
> think about the scope of the change you're proposing and be explicit
> about identifying that in your pull requests.\


### S1\
[14:05.219]

> We love taking quick polls, using emoji reaction. So, if you need to
> get a feel for your community and what they are thinking, their
> opinion about a certain issue, consider throwing up a poll with a
> simple issue comment, and asking people to upvote or downvote, or use
> whatever emoji is appropriate for each of the choices. And finally,
> you probably know this by now, but convey your tone with emoji. When
> you talk asynchronously, one of the things that you lose is the
> ability to add all that color that we add with spoken language, right?
> We are able to-- I'm talking to you right now and you can either tell
> that I'm excited or that I'm sad because you hear the sound of my
> voice. You lose a lot of that. You lose that tone when you're writing.
> So, use emoji liberally to help you convey your tone. Here's an
> example of Steve \[Fuente?\]. He's in the professional services team
> with me. And I can tell from reading this example that he's eager to
> help. And that he gave me a time estimate. He's excited to work on it.
> Those are all things that I can kind of gather from just reading
> this.\


### S1\
[15:19.640]

> And finally, enslave to synthetic, right? You got a picture of Proba
> up in the top right. If you're not familiar with Proba, it's a
> get-help app that lets you leverage to get help API to do get really
> cool things on get-help. There's a bunch of Proba plugins out there.
> So, it's just the beginning. So, you can contribute to Proba yourself.
> But I'm also showing here two examples of Hubot in particular, and how
> we leverage Hubot within get-help, and how you can do that, too,
> within your organization. So, the top example is Hubot commenting on
> an issue after we've linked that issue from Slack channel. So if I am
> on Slack, and in the services training channel, I'm trying to
> reference an issue Hubot will automatically dropping over the issue
> with a link to that conversation. That's important because often--
> because of these disjointed ways of communicating that we talked
> about. You saw a lot of logos out there when I said all the ways we
> talk at GitHub. So Hubot just helps us bridge that gap. Then on the
> bottom is an example of Hubot doing the inverse, which is Hubot
> reporting back to us on Slack when somebody has committed something,
> or when somebody's opened a pull request, and all that sort of other
> good stuff. Hubot sits in our Slack channel and he listens and he
> gives us useful information as well.\


### S1\
[16:44.207]

> All right. So, after you've organized your people into teams and you
> have a good communication strategy, how do you actually get work done?
> How do you get on the same page to get work done? So that's what this
> section is about here. I recommend you establish some patterns with
> your group of folks, right? Whatever that pattern might be for you. At
> GitHub, we actually employ all these over here. Weekly radars; this is
> an issue we open up in our team repositories, of what we are up to
> during the week, what we've got in the pipeline. If anybody needs help
> or is stuck on something, they use the weekly radar to tell that to
> other folks on the team. If somebody is reading something interesting,
> they also drop a note on the radar, and people sometimes have nice or
> heated conversations about some of the topics on the radar. Have
> regular stand ups. This can be synchronous, or this can be on Skype or
> Zune, Google Hangouts, whatever it may be. Or, sometimes we've done
> async stand ups as well, where we just kind of sit on the Slack
> channel at the same time and we go over some of the topics. Async
> stand ups are nice when, for example, some of us are out or
> travelling.\


### S1\
[18:03.777]

> Use projects. Projects on GitHub is a feature that allows you to
> create boards and then move issues and PRs and notes between those
> boards. So, projects are a great way to track your work. They're also
> extremely diverse, which I'll show you in a few minutes. They allow
> you to really be flexible about the way in which you track your
> projects; it's a lightweight project management tool. And when you
> create issues, include a checklist on them. This tells everybody in
> your group how they can contribute and what they can jump into right
> away, and it also gives you a nice bird's eye view of what's left to
> be done for your team. This is an example of an issue template, which
> I would recommend you use if you haven't already been using them in
> your organization. So an issue template tells anybody that opens a new
> issue exactly what they should be using or writing about in the issue.
> This is for our training kit repository, which hosts the on-demand
> training, that you may have seen by now. So what we ask people to do
> is include screenshots if they find a bug; if they're trying to fix
> something to include some reasoning about it. Then we give them a
> step-by-step list of how they can contribute.\


### S1\
[19:18.391]

> There's a high likelihood that you're going to have to do some
> brainstorming, and it's great if you can do a brainstorming session
> face-to-face, but sometimes it's actually even nicer to be able to do
> one on GitHub. So try using an issue or a pull request for a
> brainstorming session. This allows people to chime in during the time
> that they feel they are most creative and productive. I do a lot of
> good work in the morning, and late at night-- I do not do good work in
> the middle of the day. If there's an ideation phase, a brainstorming
> phase, I'm not going to do that in the middle of the day because I'm
> not great at thinking through things in the middle of the day. So I'll
> leave that for the morning. Now if I was stuck in a room with a group
> full of people and at 3:00 PM it was time to do some brainstorming, I
> kind of have no choice, but the ideas you get out of me might be very
> different from the ideas you would get out of me in an issue or a pull
> request. Another recommendation is again that tldr. You include a tldr
> at the very top and you state what the problem is and ask for input so
> that people know what they're brainstorming for, the reason they're
> brainstorming for. Before you submit an idea or something or you start
> trying to do a little bit of ideation, do a little bit of research and
> cross-link past issues, past conversations that happened. Maybe
> research what's happened online for your teammates so they don't have
> to do that themselves. And then include a very direct line that tells
> people how they can contribute in under five minutes. And finally, be
> explicit about the purpose and when the ideation phase will be
> complete.\


### S1\
[21:01.050]

> But talking about doing the work itself, it's important for the entire
> group to follow one way of doing work. And so our recommended way of
> doing work is using the GitHub Flow. If you haven't heard of the
> GitHub Flow by now, it's this idea that all the work that's live, all
> the work that your team has already agreed on, lives on the master
> branch, right? And this can be a software project or this can just be
> like your group's charter. It doesn't need to be code necessarily.
> Everything can be kept on GitHub. So your master branch contains live
> code or the version of the documents that everybody's already agreed
> on. When it comes time to change something you always do it on a
> branch. So you create a branch off a master and then once our branch
> is created add some commits to that branch. Commits like snapshots. If
> you've gone through the Git module already, this is probably something
> a little bit familiar, right? At some point, you're going to want to
> talk to your teammates about it so you do that via a pull request. And
> the pull request is really the place where you should have heated
> discussions about the direction that your branch is going in.
> Furthermore, it should not be the end of the commit. In fact, that
> should make way for additional commits. Maybe commits authored by, not
> the original author, but all the teammates. And so, this means that
> people are not so attached to their work that they're not willing to
> listen to what other folks are willing to say or what they're willing
> to bring to the table. And the whole reason you want to do your work
> on GitHub is so that you rely on other people for ideas and you have a
> diverse group of opinions.\


### S1\
[22:38.130]

> This is the deploy step. So if we're talking about a software project,
> for example, this would be the stage at which you could deploy from
> your branch to an environment and have folks test it out and the last
> of the GitHub Flow is merging, which is where the works
> that's happened on the branch becomes live by being merged in with
> master branch. I bring the GitHub Flow up during this part of the
> conversation because folks come from all sorts of different
> backgrounds. Going back to being inclusive about the way you're doing
> work. It's important that you train people on a common way of work. So
> training people across the board to use the GitHub Flow is going to
> pay off in the end. If you do implement the GitHub Flow, or whatever
> workflow you end up implementing, you can protect your master branch,
> for example, from people force pushing to it or from people committing
> to it directly. You can require pull requests from each individual, or
> you can even leverage one of our newer features, code owners, to alert
> specific people that are in charge of specific portions of the code.\


### S1\
[23:45.810]

> I mentioned that there's a lot of ways to use project boards, so here
> are some flexible ways to use project boards. So the top example is
> how the training team does that. Which is, we specify what's shipping
> every month. And so every time we open a new issue or a pull request,
> if it's on our roadmap, we'll drop that issue or pull request on the
> proper column of the project board, depending on when that particular
> project is shipping. Some teams don't like that. Some teams prefer to
> use something that's happening within the next 60, 30 days, 7 days or
> so-- thinking about the things that have already been launched and
> just putting them into that board. Some teams would rather keep track
> of a backlog. What's in progress, what's done, what's coming up next.
> And then some teams identify their milestones, for example, or
> something that is just in the icebox for awhile. So hopefully this is
> a good run through of how to run an organization using GitHub. If you
> have any questions at all don't hesitate to ask. \[music\]
