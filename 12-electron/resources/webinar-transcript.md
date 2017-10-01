# Electron

### S1\
[00:01.074]

> Hey, this video is about Electron and my name is Eric. I'm a trainer
> at GitHub. That's what I looked like on my first day at GitHub and
> today you can't see me so who knows if I still look like that? The way
> that we're going to break this down is as follows. First, I want to
> make sure that your local environment is set up appropriately. Then, I
> want to make sure that you know what Electron is. Then, we'll do a
> walkthrough of my team's Electron On Demand course. So we'll take you
> through each of these pieces and then you'll be fully ready to go with
> Electron.\

### S1\
[00:38.075]

> First up, prerequisites. This might be embedded in your description.
> If it's not, just go ahead and type the URL out. It'll take you to a
> Gist. This Gist gives you instructions for installing Git, getting
> familiar with Git commands, installing a text editor, and installing
> Node.js. If you have all of these, you're good to go. If you don't
> have any of these - I'm kind of expecting you might not have Node.js
> but you're probably good on the rest - then go through the list and
> just follow the instructions depending on your operating system. Once
> you have all four, once you're ready to go, let's keep going, let's
> move forward.\

### S1\
[01:21.247]

> What is Electron? Here's your first one-liner, we'll be extending
> this. It's a framework for building desktop apps. And what can they
> build? A few examples, Atom, of course. Popular apps like Slack,
> Visual Studio Code, GitHub desktop, hyper. You can build essentially
> everything from terminals to weather apps that sit in your navigation
> bar. Electron is incredibly versatile. If you're interested in looking
> at more apps, you can go to this link to do so. But generally, the
> idea is that a robust set of apps can be dealt.\


### S1\
[02:04.993]

> Let's extend this another piece. Electron is also a framework for
> building cross-platform desktop apps, so more than just desktop apps.
> You can build things pretty seamlessly cross-platform from Windows, to
> Linux, to Mac. Electron makes that process way easier than it used to
> be. But let's not get too carried away. First, I want to talk about
> the history of Electron which is intertwined with JavaScript, web
> browsers, and Atom. So follow me through memory lane. In 1995,
> JavaScript was created in 10 days by someone from Netscape and it
> sucked. It was super slow. It would cripple your browser. Basically,
> in any time before 2009, JavaScript would be interpreted at Runtime in
> computers and it was super slow. And if you wanted to refresh your
> page, it would cripple it. In 2009, Firefox made a new compiler called
> SpiderMonkey that sped up JavaScript by 10 to 40 times. So it made
> browsers 40 times faster which is impressive until we come to Chrome.
> Now, Google Chrome was released in 2008. 1995, JavaScript. 2009, the
> update for Firefox. Google Chrome in 2008. At this time, Google Chrome
> has a 50% market share of web browsers across all platforms combined
> which is insane. And that means that there's some popularity there
> that is based on something, right? When Chrome released, two things
> happened. One, they opened with an open-source basis. So they called
> that Chromium. You can still access it today and it's the majority of
> the Chrome web browser. So developers were able to not only acquire
> features and use these things for their own projects. But they were
> able to give back to that opensource browser community and make
> improvements in the duration, which increases the popularity of the
> thing.\

### S1\
[04:16.255]

> But also, in addition to Chromium, in 2009, Google made a competitive
> product to SpiderMonkey. It was a JavaScript engine called V8 that
> came out of the gate faster than SpiderMonkey which was already a
> revolution in JavaScript, and to this day is still the fastest
> JavaScript engine. So V8 compiles java script directly to the native
> machine code before it executes it which is super cool, which is super
> fast, which makes JavaScript a contender. 2009 was a big year for
> JavaScript because not only did we get these engine improvements
> within the browser, but then Node was actually created that took
> JavaScript out of the browser. So at its essence, Node's purpose was a
> way to run JavaScript outside of any web browser. Prior to 2009, there
> were very few ways to run JavaScript outside. No one was doing it. And
> JavaScript, remember, was seen as a toy. So Node made JavaScript
> powerful because even with engine improvements, it wasn't limited by
> the capabilities of a browser that a JavaScript program could run in.
> Node is super cool because it's also intertwined with npm which is a
> package registry for taking pieces of JavaScript, putting them
> together and then sharing them. So you can actually take pre-baked
> code, pre-baked JavaScript and just download it as a puzzle piece into
> whatever thing you're architecting.\

### S1\
[05:51.040]

> At this time, there are over 475,000 npm packages which is really
> cool. So if we summarize all of the things, Java Script sucked, Chrome
> was cool. It was cool because it was open source and it made
> JavaScript better. And then Node took JavaScript and brought it
> outside of the browser which made it even better. And then all of
> these people made a billion things - not a billion. 475,000 packages -
> to do fun things with JavaScript that all exist outside of the
> browser. Here we go, now we have Atom.\

### S1\
[06:29.759]

> Now Atom was released in 2014 and the dream of Atom-- the story of
> Electron will always begin with the story of Atom. The dream of Atom
> was to build a desktop application with web technology, HTML, CSS,
> JavaScript. But at the time the existing technologies just weren't
> quite yet right. So they started building Electron. Electron predates
> Atom. In 2013, they began work on Electron. They open-sourced it in
> May 2014. They called it Atom's shell. Then in 2015, they launched
> Electron. That history lesson was designed to teach you just a few
> major things. 1. The story of Electron begins with Atom. The story of
> Atom's begins with Electron. They're intertwined. That's why they're
> names are Atom and Electron. It took me a long time to put that
> together. I'm-- I'm not-- not proud. 2nd, Electron is actually just a
> combination of Chrome and Node.js. So in order for JS to be executed
> outside of the browser, you originally had to use and install Node.
> But now we're bringing Node back into the browser. So it's like being
> in a candy shop. You have access to a million different things that
> you have access to within Chrome but from your local environment. Now
> you get death tools. Now you get ES6. Now you get geo location. Now
> you get CSS custom properties. No more cores, CSS containment, desktop
> notifications, push notifications to devices. The list goes on and
> it's really, really exciting.\


### S1\
[08:11.789]

> And last, JavaScript used to be bad and now JavaScript is good and
> it's changing the way that things can happen. Things like npm and Node
> are just revolutionizing the world and here we have Electron. So
> here's your final one-liner. Electron is a framework for building
> cross platform desktop apps with JavaScript, HTML, and CSS. So if you
> used to be just a web designer who knew how to design things on the
> web, you can now become a desktop app developer. Electron is that
> entry gate. And with all of that said, let's get started. Let's dive
> into putting our hands on Electron. Let's do that on the main course.
> Going to exit this slide deck, close it out, and then move over here
> to my Google Chrome, which we know so much about. And the link that
> I'd like you to navigate to if you aren't here already is
> services.github.com/on-demand. Then actually from on demand we can
> scroll down and click on Electron. Our training is broken into three
> parts here. We'll go through all three in varying degrees.\


### S1\
[09:34.627]

> And the first place we'll click on is Electron 101. This first page is
> largely skippable. We've already seen the contents of this video, but
> if you want to watch it, it's well made. It's really good. And there's
> also prerequisites that we've already seen which we should have
> already been, so it's a nice refresh. One thing that is valuable is
> this On Demand Elecron App Repo. If you have any questions throughout
> this course you can open it, you can open a new issue, and then you
> can ping at GitHub teacher with your question at any time whenever you
> need it. Continuing on. We're actually going to start on Electron app
> using an npm package. So this is a pre-made puzzle piece that just
> gets us started as is. I'm going to open up my terminal and I'm just
> going to immediately and globally type install NPM install-g
> electron-forge. It's going to take a moment so I'm going to skip this
> video ahead. Once that is done, we'll want to navigate-- let me zoom
> this in a bit for you. We'll want to navigate to where we want to keep
> our file. I'm going to just move to the desktop because that's where
> I'd like to keep my temp files. And I'm going to create a brand new
> project, and I'm going to call it Electron App. So I'll type electron
> forge init Electron App. What that's going to do is it's going to
> create a brand new forge project a nice template for me in a file
> folder directory called Electron App. This might take a second to
> install all the dependencies so I'll skip the video ahead again.\

### S1\
[11:17.707]

> All right. It took a little bit to install the dependencies, but now
> that that's done, I could type CB and switch into the Electron App
> folder that just got created. A few interesting things. If I open this
> up in my text editors, open it in Atom, we'll note quite a few items.
> We'll see the index.html, we'll see an index.js, and then we'll see a
> package.json and a packagelock.json. All four of those files are
> pretty standard in any Electron App. In general, Electron, the way
> that it works, is you have a main process-- and actually I want to
> show you. So our main process would potentially just be all of these
> items up top. And then every individual pane that gets created, let's
> say we have several new windows, this is opening on my other screen
> which is unfortunate. But if we have repeated new windows or new
> files, we're just creating new renderer processes. So Electron works
> like that where you'll have your main processes potentially like
> index.js, these are your main items and your main renderers. So every
> time you open a new item, it might look like this. All right, let's
> move on to the next piece.\

### S1\
[12:47.762]

> We created a uninitialized repository. So it's initialized but we
> actually want to stage all of these changes. So if we just type git
> status, we'll see all of our files are currently untracked, and then
> we can git add the gitignore file. And this is really important to add
> first because gitignore will specify, it'll essentially take parts of
> our project that we don't want to include out. So gitignore is added,
> we'll commit it, gitignore file. And then after that, we can type git
> status again. And most of the files is actually will be the same, but
> we can type gitadd dot and include the rest of them. So we'll be
> adding our Electron boiler plate files. This is just what it looks
> like by default. Next up, we're going to do a few things with
> github.com. So we want to create a new repository, just click that
> button. We just gave it to you. It's really nice. And then it says,
> "To avoid errors, don't initialize the new repository with any other
> files." That's because we already have files that we want locally. It
> takes us to a link that tells us what to do, actually. I forgot it
> would do that. I go to github.com. And then click on the plus instead.
> I can just start with a new repository. So you can click on that link
> for more instructions but that's not helpful in a video. So I'll just
> create a new repository like so.\

### S1\
[14:32.636]
> I'm going to call my repository Electron App. And since that's already
> taken, I'll do Electron App 1. And then make sure that you don't add
> any of these three things. We don't want a read me, we don't want to
> get ignore, we don't want a license. We want a brand spanking new
> blank repository that we can push to. Create that repository when
> you're ready. And then we're just going to follow these two pieces,
> position existing repository from the command line. So I'll go back to
> my terminal, add the new origin to as a remote to the repository. And
> then I'll push that origin. I am forbidden that is because I am signed
> in as my user instead of GitHub teacher. So I'll adjust that and then
> we'll pick it right back up.\

### S1\
[15:31.946]

> So now I've fixed my error. I can push to the origin. It was something
> to do with collaborators, an error you likely won't have. And to test
> that it went through, you can actually go back to your remote. You can
> go to the GitHub link and refresh. And when you do, you should see a
> page similar to mine where you have pushed all of these different
> boiler plate files up. Great. Great.\


### S1\
[15:58.326]

> So the next thing that we want to do is we actually want to add a few
> other files. We want to add a style sheet and we want to add a new
> renderer to our process. So to do that, we're just going to type
> touch. Touch is kind of a replacement for add a new file, if you're
> not familiar with the command line. We'll do touch, source. In the
> source directory, a file called style.css. We'll do that again for a
> file called renderer.js. And we also, just because we're here, want to
> make sure that these are referenced in the index.html so that both of
> these get picked up. So if we go back to our steps, we can click
> continue to copy paste and we want to add this line of code to - let
> me open up Atom again - to our index following the title. That looks
> good. We want to add this line of code directly above the closing body
> statement. That looks good. Once that step's done, we'll continue on
> and our first goal is to just spin up the application locally. So
> we're creating the application by typing npm start. This is how you
> open a brand new Electron app. This is how you run it. So as long as
> it is an Electron app, you can type npm start and you'll get a pop-up.
> This is an Electron Desktop cross-platform with HTML, CSS, and
> JavaScript app which is not at all exciting because all it says is,
> "Well, hey there.", but it actually is super exciting because you know
> what else we just got? \[Debtools?\]. It's opened by default. We can
> set, actually the preference for this to open and this is super cool.
> So whenever you want to run a new Electron app or an Electron app
> locally, you'll type nmp start to do so. Also now, I'll type control C
> just to kill that process for now. Alternatively, I could have closed
> it by clicking on the X but that doesn't actually turn me at the whole
> process, so you'll still want to do control C.\

### S1\
[18:31.026]

> Next step. For our app, we're going to build a memory game so we can
> find the code from CodePen. Basically, the whole premise behind what
> we did here was when we first did our workshop on Electron, we wanted
> to show you how easy it was to take web technologies and reproduce
> them locally. So you can do something fantastic, where instead of
> Hello, World!, your basic item can just be some JavaScript, some CSS
> \[HCTMO?\] already exists. And you can make that exist on your own
> machine. And that's what we did here. So we'll have three sections of
> code from our CodePen at this link. And we're going to copy all of
> these pieces of the code and see this game that is running real well
> in the browser. We'll see this game but instead, we'll see it locally.
> Something important to pay attention to is that if I need these
> CodePen use dependencies, it's not going to work immediately as
> seamlessly as expected locally. So just keep that in mind if you're
> working. For now, though, we're going to grab the HTML text and we're
> going to insert it into our \[XC?\] index.html file locally. So I'll
> go back to Atom and in my index file, I will replace the body text
> with all of these stuff, which I actually teased before. I already
> showed you this one. I opened out them the first time. And now, we all
> have that.\

### S1\
[20:14.218]

> So if you're following the instructions, it wants us to do npm start
> again. Let's just do that just to see the different pieces here. And
> now we'll see up here, we've written an HTML document. So there's no
> styling. There's no interaction. We can't really, actually, do
> anything here. And that's step one. So let's close that out. We could
> save and commit our changes. I'm going to skip over that just in favor
> of time. So I'm going to move on now to the CSS file. And I want to
> put that in my style about CSS. I'll save that, and I'll go back again
> to my Electron Net, and this time, again, I will save it, npm, start.
> It launches. Now we've got some style. Good. Interactivity is still
> missing. We're missing our JavaScript, which is too bad. So let's add
> that last piece over here. Back to the JavaScript. And we want to
> place our JavaScript in our renderer.js file which we linked, if you
> recall, at the bottom of the index. So this is going to be called
> right at the bottom of this initial renderer index.html process. Use
> that code, save it. Shout out to our friend Jason who actually
> refactored so that we didn't use jQuery. And then we'll do an npm
> start one more time. And now the game works as we expect, which is
> very exciting. So I can show you my first pair right here that saves,
> which is great. The final step of this process, if you go back to your
> instructions, is to celebrate. But, actually, celebrate's good because
> it's going to point us to the next two pieces that we're going to jump
> through here. So we'll learn how to package the apps so that they can
> be distributed to different operating systems. So go ahead and click
> on that. But before we do that, we will actually-- let's store one
> commit now just so that we have a copy to head back to if we make any
> mistakes here. So the good status, git add, and then I'll commit
> working memory game to my history. And I'll push that just to have it
> there. All right. Excellent.\



### S1\
[22:57.885]

> So now this next piece is using another npm module. Npm modules, I
> swear, just make everything with Electron easy. As I built a workshop
> for Electron, everything I wanted to do that I thought would take a
> long time, for example, instead of having to quit and reload Electron
> by typing npm start, there's an npm module for that. It's kind of like
> there's an app for that catchphrase. So keep that in mind whenever you
> think about adding functionality, there might be an npm module that's
> already there. There's already a puzzle that's made for you. And we'll
> explore that idea a little further.\



### S1\
[23:37.106]

> The npm module for this section, the one that's going to save our
> lives and make it so that our app runs really well natively on any
> operating system is called Electron Packager. This is the one that's
> most recommended. But there are absolutely other tools to package
> Electron apps. And it's widely adopted. It's maintained within the
> community. We like this one. So we're going to start out by just
> typing npm install Electron Packager. Oops, Packager. And then we'll
> do save dev. Before I do this, I want to show you what's going to
> happen. So if I look at my package.json, I see all of the modules that
> are used when I start with an Electron forge app. And I want you to
> note that the one that we're looking at here, Electron Packager,
> doesn't exist yet. It's not in our code yet. So that dev dependencies,
> that is missing. But when I type this, press enter. We'll wait for it
> to do its installation, but once it completes, we should actually see
> a show up here within the deb dependency and the version that we've
> installed.\



### S1\
[24:52.147]

> Now here is where the instructions are going to get a little tricky.
> Go back and look at how to use the Electron Packager. What's really
> nice is, when we type npm start-- and then another little intricacy
> for you, when we type npm start, we're really actually just launching
> this script right here where we're starting Electron Forge, which is
> probably launched somewhere else. Right? And it does different things.
> But whenever we, if we want to add a script for example to do a build,
> we can add that script right here. So here we're prompting you to, in
> the package json file, add the following scripts for bill. And we will
> do that just like so. I'm going to put it-- it doesn't matter where.
> Right here. And I'm also going to put a comma after. And now whenever
> I run-- once I save this, whenever I run npm build, it's going to
> actually launch Electron Packager which we triggered just by typing
> its name on all of the files within our directory called Electron App.
> So when it packages, we'll type it into a package called Electron App
> and then we'll over write one if it already exists. So I'll save that,
> and then that's pretty, pretty good. And then we'll do one more thing
> to fix it. In the next .js file, there's a first line pre-populated by
> Electron Forge. We don't like that. It doesn't work with Electron
> Packager.

### S1\
[26:29.271]

> So let's highlight this import file from Electron and just replace it
> with this const. It does things in a different way. So those two
> things should make this work. But at the time of this video, at the
> time that we created the course, we might run into an issue. So let's
> test it. If I type npm run build, we're going to start to build these
> files. And it's starting with Linux, which is normally a faster
> package, and it's going to follow up with the Mac file. And this is
> typically where we hit the error. There it is. There's the error. So
> this error is because Electron Packager isn't playing nicely with
> Node, and we're waiting for Node to update the version. There's
> already actually a PR into Node that fixes this, but for now, we're
> kind of just stuck. Excuse the abrupt cut. I actually just
> trouble-shooted a few things. I made my version of Node up to date as
> of today and reran the scripts and updated npm. And unfortunately,
> even if it's up to date, it might not work, depending on if you're on
> macOS. So we do have steps for those of you on macOS if you're getting
> errors. And since this might affect a large number of you, I just want
> to walk you through those. So help me troubleshoot. You would have to
> do these few items. You'll have to install XQuartz, you'll have to
> install Wine, and you'll have to install npm. You can just type all
> three of those just as it is, just like that. I've already installed
> those on my machine. So I'm just going to do the last step, which is
> mbm use six.\

### S1\
[28:39.994]

> Now Node is going to go back to a version that we absolutely know it's
> compatible. And I can do npm run build again and it will go through
> this time. So that's our guarantee for you, that there's something
> wonky with Node as of the time of this video. But it should work in
> the future. Just going to let this kickoff and then I'll catch back up
> with you and tell you if the package is open and stuff. All right. So
> that stuff actually takes a long time. But once it's done, you'll be
> able to see all of these new packaged programs ready to go on there in
> your directory. So I can open this up actually even and look at the
> one from my system. I'll get the darwin and see that this Electron App
> package is ctually ready to go. It's actually ready to be open. And it
> is that game as we expect. So we can actually, if we really wanted,
> drag with over and put it in our list of preview items. But it's not
> actually ready yet. We're going to do one more extension. And should
> work for whatever system you have. You should be able to see that it
> works and it's ready to go.\

### S1\
[30:07.649]

> As I open this Linux ones, we can see that it's not going to work on
> Mac, which makes sense, and the Windows one as well. But what we want
> to do is instead of having that Electron default icon, that's where we
> want to make our own icon. So we want to add something new and
> special. So if we click on the add an icon, we can check out this icon
> library, if we're curious about an icon to add. I really don't want to
> spend a lot of time in here. So I am going to pick arbitrarily the--
> please excuse the rough cut again. I definitely took a long time to
> pick this. And I like the puzzle piece one. So now I know I want the
> puzzle piece icon. But to get it, I'm going to have to download this
> whole bunch. So if you click download, you can open up. It's a zip
> file. And then we can scroll down into the PNGs here and actually find
> the one that we liked, which in my case was puzzle. Puzzle, puzzle,
> puzzle piece. There's a bunch of different versions of this puzzle
> piece. I'm just going to pick one that is small, the three times. And
> what I want to do with this is actually pick it up and put it on my
> desktop so that I can have easy access to it.\

### S1\
[31:42.128]

> So now that it's on the desktop and I'm even going to rename it to
> unicorn.png which you'll understand why I did that in a moment. So
> grab that file. Grab whichever icon you like, and then take it to the
> desktop and then rename it or wherever your folder is. Okay. Once
> you've done that, you will do the following. So we'll go back to our
> Electron Net, type mkdir icons. We want an icons directory. And we're
> going to generate an icon file for Windows, Mac, and Linux. The best
> place to do that is to go back to your instructions and scroll down
> within the add an icon page and click on this tool recommended under
> converting the image. So we moved it to the desktop on purpose.
> Specifically, we will click to add that file, the unicorn.png. And at
> the bottom, we can convert the icon like so. So here we have the ico
> file, I can download that, double click what downloads. Actually,
> let's open this. This'll be different depending on who you are. I'll
> show it in finder. And then I want that one to go on my desktop too.
> Then I will download this again as an icons file. Open that in finder.
> You'll have to do this differently depending on your operating system.
> And I'll load that to the desktop as well. So close that out. We'll go
> back. And now on my desktop, I have these three files. I have
> unicorn. png-- oops. Unicorn.png.icons and then unicorn.png.ico. So
> let me quickly rename these to unicorn.ico. And if I'm supposed to be
> saying I-C-O or I-C-N-S, I apologize to those of you that that might
> be bothering, but I don't know the intricacies here. So I have that.
> Those are all ready. Go back to my finder. I want to pick those three
> up, and I could have just done this from the desktop, but I want to
> make it very clear depending on wherever that you're at that I'm
> picking these three files up, icons, png, and ico. I'm going to drag
> them all into the Electron App. And then I drop them into the icons
> folder.\

### S1\
[34:33.958]

> Now the last step I have to take-- I accidentally closed the
> instructions. But if we go back to where we were at, the last thing I
> want to do is change the way that my files are building. So I want
> specific builds for each upgrading system, and that can be copy-pasted
> here from instruction number four. Specific builds for each operating
> system and then when we run build, it's actually going to be specific
> for each one. So what changes is not actually too much, it's just the
> type of icon that it's pulling when it gets created. So we'll take
> these pieces, copy-paste, and go back to our package.json. And instead
> of this build line here, I will paste all of these builds, including
> the replace build which notice something different and just builds all
> the four above, I'll add a comma to make sure that that's all taken
> care of. Now go back to my terminal and I will take npm run build. It
> will take a bit, and I'll check back in when it's done. All right. Now
> that this is done, I'm just going to double check what it looks like.
> So if I go back to my finder and I open these files, I can check on
> Darwin because I know what that one looks like for sure, and it looks
> like that photo. So this puzzle icon kind of looks garbage-ey because
> I chose the lowest res version, but if we did eight times it wouldn't
> look so bad.\

### S1\
[36:20.102]

> And then if I went into each of these other ones, it wouldn't actually
> help me to see because my operating system is different. So that
> brings us to, actually, our final step of packaging. When you are
> done, when it does look good locally for you, you can-- the obvious
> way to figure out if it works for everyone is to share it with
> yourself or with friends, so on the other operating systems. That's
> outside of the scope of this tutorial. But Spectron is something that
> you can check out, which is what the Electron community recommends for
> testing. It's a framework. So go ahead and follow up with that if
> you're interested, but that takes us to the end of that section.\

### S1\
[37:05.081]

> So for our final piece, there are only two more things I want to show
> you, but we'll learn how to share your app. So most of this is going
> to be at your own discretion. But I want to just point you to a few
> resources. When you're sharing your app, you want to be aware of
> legality. So if you choose the right license, you can do that by going
> to the Choose a License website, which was made by one of our teams at
> GitHub, to help you figure out what you want to do when you're working
> in open source. Additionally, if you want to list your file on app
> stores, we prepared a series of collections for you. But the last
> piece I'm going to walk you through is right here in Share on
> Websites. All right.\

### S1\
[37:55.395]

> So this last step can actually be a little trickier than it appears at
> first glance. But it tells you that, most commonly Electron apps are
> shared via GitHub releases. So if you've been staging, adding,
> committing this whole time, you might run into a scary error where you
> will have added all of these bundled packages, and they do not
> recommend doing that. I actually just did it by trying to take a short
> cut. And there's no need for GitHub to have all of those things on it
> if you're trying to share. So I'm going to add my package.json. I'm
> going to be deliberate about my adds. I'm going to add everything in
> source. Index, let's just do that. Git.status again. I will add the
> icons directory and then I will not add these bundled apps. I won't
> push those up. So I'll commit, add finished game, and then I will push
> it. I will force-push it. Don't do this. I'm force-pushing because I
> accidentally pushed things I shouldn't have before, so yours should
> just work right away if you're following instructions.\

### S1\
[39:10.496]

> The point, really, of this section is to cover two things. The first
> is that releases can be super bulky if you're trying to actually
> package the bundled versions-- or the package versions of the code.
> And two, how you even set up a tag and a release. So I'll refresh
> this. I have my finished game. If anyone clones this locally they'll
> be able to type npm run build. I might put instructions for that in a
> Read Me. And last up, I'll just add a release to GitHub. So I can
> create a new release. I'll call it version 1.0 of my Flippy Memory
> Game. And then I'm not going to describe this for now, but I want you
> to see that it's as easy as just creating a release just like that
> where I'll publish it and now anyone who wants can come into my code,
> or I can distribute a zip version of my code for people to download
> the source code version up. It's just right there. It's a nice
> release. And if I want to iterate on top of this and maybe make
> changes that break it, I'll always still have this source code to
> distribute to others. And that's it. That's the last piece.\


### S1\
[40:26.117]

> So now you are ready to go create an app of your own. You can write it
> in JavaScript HTML CSS. Find a bunch of cool Node modules. Put them
> together in ways that no one's ever done. Try and mimic things that
> exist. Build your own version of Slack. Enjoy. Stick with it. If you
> have any questions, remember that you can get to us here. I hope that
> your Electron journey is illustrious. Have a good one.
