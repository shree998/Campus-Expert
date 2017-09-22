# GitHub Pages

### S1\
[00:01.143]

> Hey there. I'm Hector. I'm a trainer with GitHub, and today, we're
> going to learn a little bit about GitHub Pages and the technology that
> backs it. It's called Jekyll. So let's jump right in. So as I
> mentioned, GitHub Pages is a technology that's backed on Jekyll, and
> what it does is that it allows you to publish your repository contents
> as a web page. So this is the public-facing GitHub Pages site that
> just talks a little bit about that technology. You could go here to
> maybe watch a video about how it works and how to get started. But you
> don't necessarily need to do this because I'm about to show you. So
> the way that it works is, you will-- any repository, essentially, you
> can generate as a GitHub Pages site. However, if the repository is
> owned by an individual, and if you name it something specifically, it
> will automatically be served for you. The URL at which it's served can
> be tricky depending on who owns it. So if the repository is owned by
> an individual, and the repository is named username.github.io where
> username is the person's username, then that will be the URL at which
> the site is served. If the repository is owned by an organization, and
> the organization names a repository with the same name as their
> organization .github.io, that is where that repository will be served.
> And then you can have repositories for specific projects within an
> individual's account or for specific projects within an organization's
> account. That gets kind of tricky, but I wanted to kind of show it up
> front just so that you get an idea where these URLs are coming from,
> and so that it's not confusing. So I will share this documentation
> with you, but in order to show you how it works, I'm going to go ahead
> and just generate or create a new repository for myself. I will call
> this repository hectorsector.github.io to be consistent with the
> naming convention that we just saw in the help documentation.\

### S1\
[02:01.944]

> And the website or the repository, rather, can be public or can be
> private. This is talking about the contents of the repository itself.
> So in other words, the source code. If you make the source code
> private, the published website will still be public, obviously,
> because we're learning how to make a public-facing website. So I'm
> going to go ahead and just create this completely blank with no files
> in it at all. And the easiest way to probably get a GitHub Pages site
> up and running is right from the web UI. So we'll do that first, and
> then we'll dig right into how to do it from the command line, how to
> create one from scratch, and all the other sorts of good stuff. So I'm
> going to go over to the Settings tab here, that's where my GitHub
> Pages settings live. If you scroll about halfway down, you'll see a
> section called GitHub Pages. This is where you can toggle the
> technology on and off for existing repositories. Since I don't have
> anything in this repository, it is turned off. I don't have any files
> either, so it cannot be turned on. But I can use this theme chooser
> here, so that's what I'm going to do. Now, this is a great way to use
> GitHub Pages if you are brand new to getting GitHub, or maybe brand
> new to developing websites to begin with, or you're teaching somebody
> that's brand new to these concepts. If you are familiar with HTML,
> CSS, Javascript, and if you are familiar with getting GitHub, then
> you'll probably want to do some of the more advanced creating of a
> GitHub Pages site which we'll talk about in a little bit. But it's
> always good to know how it works from a web-UI standpoint. So I'm
> going to go ahead and click on Choose a theme here. That'll take me to
> the theme chooser where I can choose the theme that I like best for my
> GitHub Pages site. So they're all up at the top here. You would pick
> your favorite. Today, I am liking Hack so that is what I will pick. Go
> ahead and select that theme.\
> \[silence\]\

### S1\
[4:07.400]

> And what this will do is it will generate an index.md file. If you're
> not familiar, that's for a Markdown file. That's one of the really
> nice things about generating a website with GitHub Pages and Jekyll,
> is that you can write in Markdown. So you don't have to worry so much
> about the HTML, and the CSS, and the JavaScript. That all gets taken
> care of for you on the backend. You just have to worry about styling
> the text in Markdown. The only thing I'm going to change here is
> instead of saying, "Welcome to GitHub Pages", I'm going to say,
> "Welcome to Hector's GitHub Pages Site". Just so that we can visibly
> see what I did differently here-- and I'm going to commit this
> directly to my master branch. This is, of course, not a recommended
> workflow. In any real, live repository, you would probably work
> through a pull request in using GitHub Flow. But we're just kind of
> demoing here, so I committed it directly to master, and I used a
> default commit message.\

### S1\
[05:01.749]

> So all right. This doesn't look like a web page. This just looks like
> GitHub rendering an index.markdown file for me, so let's look at what
> this looks like when it's published. I'm going to go over to the
> Setting tab, back to that section that talks about GitHub Pages. Now,
> you'll see there's a green bar that says your website is published. So
> you can see that the website will be generated under
> hectorsector.github.io with the green bar that you can see there. So
> all I need to do is navigate to that URL, and there is my fantastic
> public-facing website. So it was pretty quick. So in, what, maybe two
> to five minutes, you can walk somebody through how to create a GitHub
> Pages site on the web UI with very little code required. So if you
> wanted to edit this site, it's as simple as going back to the Code tab
> of your repository, opening that index file, and changing its
> contents. The site will be built on the backend and published at the
> same URL. That all happens automatically, so it's like an auto
> deployment, is how you can think of it.\



### S1\
[06:05.794]

> If you look at the files here-- so we know what index.md does, but
> there's one extra file here called config.yml. This extra file is used
> by Jekyll to set, usually, some default to some specific
> configurations for your website. Right now, there's nothing special
> here other than the theme that I chose, is a part of this config.yml
> file. If you're not familiar with YAML, it's essentially-- you're
> going to set key-value pairs. That's essentially the way that it
> works. So the key here is theme, the value is jekyll-theme-hacker, and
> so it kind of works like that. And YAML syntax also means that these
> key-value pairs can be indented. We'll work more with this as we get
> more familiar with it. All right. This is all well and good, but I
> want to be able to work on this locally, and I want to able to test
> the site locally as well. So let's go ahead and figure out how to do
> that. So what I'll do is I will clone this website first to my
> machine. Okay? And if I navigate right into that website, a couple of
> things that we'll notice is-- so first one, let's look at the files.
> So these are the same files that I had; the only exception is you're
> seeing that you have a .git folder here. That's just the Git Internals
> that live in that folder. We don't need to worry about that. You need
> to have Jekyll installed, and the best way to install Jekyll, or
> actually, the best documentation I can point you to is this GitHub
> Help document on setting up your GitHub Pages site locally with
> Jekyll. So I'll let you go ahead and read that. Essentially, you got
> to make sure you have Ruby. You have to make sure you have the Bundler
> gem installed, and then you also install the Jekyll gem, and the
> GitHub Pages gem.\



### S1\
[07:55.321]

> I have some of these things already, so the only thing that I need to
> do is I need to jump here to this step two which is all about
> installing Jekyll using Bundler. So I'm going to create a Gemfile.
> That's the only thing that's not already in my repository because I
> was using it right on the web UI. So that's taken care of for me, but
> if I'm going to do it locally, I need to do this first. So back on my
> repository here, let me open it up and add them. I'm going to create a
> new file, and I'm going to call that file Gemfile. It would help if I
> could spell Gemfile. And that file is a part of my repository now, and
> it's essentially what's going to be used by Bundler. So save that, and
> then you can do a bundle install. What that'll do is it'll install the
> GitHub Pages gem. So let's talk about the GitHub Pages gem. The GitHub
> Pages gem is what's used by GitHub, and it essentially is a set of
> dependencies that make it easier for you to be able to use Jekyll and
> GitHub Pages. And it has a few dependencies. This is probably the best
> place to see those dependencies. So this kind of tells you what's
> packaged or what's bundled with the GitHub Pages gem. So these are all
> the technologies that are used. The only one that's really of interest
> to us right now is our theme, jekyll-theme-hacker. So that's included
> as a gem in the GitHub Pages gem. All right. But I've got that
> installed, so now, to run my website locally, it's as simple as doing
> a command called jekyll serve. Now there's two Jekyll sub-commands
> that you're probably going to mess with - a jekyll build and a jekyll
> serve. A jekyll build will generate your website, and spit it out into
> a subdirectory. Usually, it's called \_site. And the jekyll serve will
> actually serve your website for you in port 4000. I forgot to wrap
> this in a bundle exec. And that's just so that I specify to use my
> Gemfile. So if I navigate to this on my local browser here, I can see
> my Jekyll pages site is built.\



### S1\
[10:27.208]

> Now, I can keep that running if I want to. And one of the nice things
> is while I keep that running, I can change some of the contents of,
> let's say, my index.markdown file. And lets say that here, instead, I
> wanted to maybe include, let's say, my picture because it is my
> website after all, right? So I'm going to use my profile picture from
> GitHub here. And again, if you're familiar with Markdown, this is the
> Markdown syntax for that. So I'm just going to save it, and then if
> you look back at my website-- at my Terminal here, it's going to
> regenerate the website. So if I just refresh, there's my picture. So
> making changes to your website is as simple as making changes directly
> to the Markdown files when you're ready to publish that. Because this
> isn't public up on GitHub yet, you can just stage and commit that. So
> I'm going to go ahead and-- I don't want my \_site directory. So
> that's the next thing you probably want to figure out, is the \_site
> directory. This is your generated site. That's actually the static
> site. So you're looking here at the static website itself. Okay?\



### S1\
[11:47.830]

> So you probably don't necessarily want to version control that, you
> don't want that to be in GitHub, so what I'll do is I'll add this to
> my gitignore file. If you're not familiar with gitignore, all it does
> is it ignores some files so that they don't become part of version
> control. So I'm going to do that really quick, create a .gitignore,
> and add the \_site directory to that. Here we go. All right. So now,
> if I do git status, I'm going to stage my gitignore-- actually, I am
> going to stage all these things. Here we go. I'm going to commit them,
> and I'm going to push it up to GitHub. So now, if we looked back at my
> website on github.com, you see that all these new files are here. If I
> go to the Settings tab, you can take a look at how the deployment is
> going. So notice that this is no longer green. It says my website is
> ready to be published at this URL, but it's not there yet. So all that
> means is that on the backend, my website is getting built and
> deployed. So I can just refresh that, and soon enough, that will be
> published, and now it is. So if I navigate to a new tab here, and
> again, this is probably cached. There is my published website with my
> profile picture on it. Okay? So that's some of the basics of how to
> use Jekyll in GitHub Pages starting off with the web UI. But what if
> you wanted to actually create something locally? How would that work
> and how would you get it pushed up to GitHub?\



### S1\
[13:25.005]

> So let's take a look at another command now. So I'm going to cd out of
> this directory, and let's say that I wanted to generate a brand new
> Jekyll website from my machine. So I'm going to do jekyll new. Oh, and
> I need to specify a name. So jekyll new and maybe we'll call this
> one-- let's say that I'm creating a website for my community, and I
> live in Orlando. And I actually live in an area called Lake Hancock,
> and we have a community program called Lake Hancock Green Alliance. So
> let's say that I wanted to create a website for that. So I'll do
> jekyll new lgha. Okay? So that created a directory for me called LGHA.
> So let's go into LGHA and take a look at that. And so there's a few
> things that are here. Jekyll assumes that, essentially, I'm going to
> create a blog. So I'm getting the contents of this or the structure of
> a blog here. You can take a look at how this website works by running
> jekyll serve. So I just want to look at the boilerplate content here.
> So you can take a look at the boilerplate website that was created for
> me using jekyll new. Now, you can hit Control C anytime to stop that
> from running. Let's open that up and add them, and take a look at
> what's going on here. So we're familiar with the config file, but this
> config file is a little bit more complex than the one we were looking
> at. It has a lot more key-value pairs. So we can step through some of
> these. Some of the interesting ones are things like title, email,
> descriptions. So these are all kind of customizable, and there are
> layouts that have been created that make use of these key-value pairs.
> So that's why these are here.\



### S1\
[15:22.263]

> Some of the important ones that you're going to see over and over
> again as you continue working with Jekyll and GitHub Pages is URL and
> base URL, and these are used to help your Jekyll site figure out where
> things are served. So for example, if you were serving this under--
> let's say I was serving this under hectorsector.com/blog, then I would
> like to put blog here so that everything is served under that
> subdirectory, right? The other things that are here like my Twitter
> username, GitHub username, so these are used to actually display them
> on the website. This Markdown, kramdown, so this is the Markdown
> processor that's you used. With the Jekyll site, you can kind of
> specify all sorts of very specific things, and all these things I
> should also mention are detailed in the Jekyll documentation. So if
> you go into the Jekyll documentation, and you go into the
> configuration section, you're going to get a look at some of the
> default configurations and what they should be set at. Here you go,
> down here. So all sorts of stuff that you can use for your
> configuration file. And throughout the documentation, you're going to
> see references to them. Another really interesting part is this
> default configuration where you can take a look if you don't specify
> anything at what the default configuration is. Okay? That's great.\



### S1\
[17:00.145]

> Before we change anything around, let's get this pushed up to GitHub
> so you can see how this would look. So the first thing I need to do is
> generate a new repository for this, right, because this doesn't live
> anywhere. Now, I think I may already have an LGHA repository. Give me
> just a second to check. Indeed, I do. So what I'll do is I'll create a
> new repository and I will name it-- why not bookish-giggle? So the
> name of the repository up in GitHub doesn't have to match the name of
> your repository locally. That's not necessary at all. And now that I
> created this, I'm just going to go ahead and push this up. So let me
> first set the remote. First, I need to-- so this wasn't a Git
> repository. So my git init command will initialize it as a Git
> repository. And I'm going to do, now, that command again, git remote
> add. All right. Take a look at my git status here. I am interested in
> all of those files. Notice that when I used jekyll new, it
> automatically created a .gitignore for me. So let's take a look at the
> .gitignore and see if it has what I want. And indeed, it does. It has
> that \_site directory so that I'm not trying to push up my
> \[generated?\] website up to GitHub. So that's pretty nice. I'm going
> to stage these. I'm going to commit them, and push it up.\



### S1\
[18:43.539]

> All righty. So now that I've pushed this up, I'm going to go ahead and
> refresh bookish-giggle here. And if you go to the Settings tab, that
> is where your GitHub Pages settings are. Now, notice that because I
> didn't name this website, my username.github.io, GitHub Pages is not
> turned on here by default either. I need to turn it on myself. And so
> you have some options here when you turn GitHub Pages on manually. You
> can choose which branch you want to serve, so I want to serve my
> master branch. Another option you have is, if you have a docs folder
> within your master branch, you can serve your website just under that
> folder. You also have a third option which is you can create a branch
> called GH Pages, and that branch will become your GitHub Pages branch.
> And that's useful if you have a repository that contains, maybe, some
> source code that's not a web page, but you also want to have a
> public-facing web page. I'm going to go ahead and serve my master
> branch. So I'm going to go ahead and do that and hit Save. And then
> what you'll see happen is that my website will start getting built. So
> it says my website is ready to be published, so that means it's
> starting to get built, but it's not built yet. I'm going to give that
> a little bit. There it is. Let's go there, take a look at it, and
> there is my website. Now, you notice that there are some issues with
> styling. That has to do with subdirectories. And so if you want to
> pause the video, maybe think a little bit about why that could be
> happening, go ahead and do that. If you already thought about it or
> you don't want to take the opportunity, I'm about to-- spoiler alert.
> I'm about to tell you why it's not doing that.\



### S1\
[20:21.046]

> And that's because if you look at the URL at which this is served-- so
> this is served at hectorsector.github.io/bookish-giggle. Excuse me.
> That doesn't match how it's being served locally. So if you look back
> to how I'm serving my website locally, I don't have a base URL set. So
> Jekyll is assuming that my website is being served at the root
> directory, which, of course, it's not in this case. Something else to
> keep in mind is that back over here-- so you may be wondering, rather,
> why it's being served at hectorsector.github.io/bookish-giggle. And
> what I would do there is point you to that documentation that we were
> looking a bit earlier. Here it goes. User, organization, and project
> pages. So this documentation helps you navigate how your website is
> served. So in this case, I have a repository that lives under my
> personal account, hectorsector. So it's its own project within my
> personal account. So I can look here and I can say, "All right--" so
> this is not just a user pages site because I didn't name it
> username.github.io, but it is a project pages site owned by a user
> account. So therefore, it's going to be username.github.io/ the name
> of the project or the name of the repository. So in this case, because
> it's called bookish-giggle, my repository is called bookish-giggle, my
> website is served under hectorsector.github.io/bookish-giggle. If you
> say bookish-giggle enough times, it's kind of fun. I recommend doing
> it.\



### S1\
[22:11.213]

> All right. So in order to get this to work properly, what I'm going to
> do is I'm going to change the base URL on my local site here into
> bookish-giggle. Save that. You can always check this out locally
> before you push it up by doing a bundle exec jekyll serve. Serve. Here
> we go. And now, you'll notice that it's served at my-- it's served
> locally, but /bookish-giggle. Now, it still looks normal when I go
> through it. You'll just notice that bookish-giggle is prepended before
> every part of the URL. Okay? So if I stage and commit this now...\
> \[silence\]\



### S1\
[23:06.649]

> And I go back to my options here-- so remember that this is always
> going to give me the status of the build. So it's building right now.
> And there we go, it's published. And now, if I refresh this, all my
> references should be resolved. And now, everything is pointing to my
> username.github.io/bookish-giggle which is exactly what I wanted. So
> pretty nice. So again, in just a few steps, a few more complex steps,
> but in just a few steps, I was able to get this website up and running
> using just a handful of commands, a little bit of \[scoothing?\], and
> maybe just some experience of troubleshooting this kind of thing
> before. But I have a fully functional blog.\



### S1\
[23:47.848]

> So now, let's learn how Jekyll itself is supposed to work, keeping in
> mind that GitHub Pages will support most of the things that Jekyll has
> available to you. So couple of things is, let's say-- well, it's not
> fun to have my awesome title. Actually, I want to have my awesome
> title. So I want to change that, so how do I go ahead and do that?
> Well, you may have noticed that that was in the config file here. So
> in your config file, you can change your title around. And you know
> what? Rather than looking at my published website, I'm going to jump
> to looking at my local website here. Let me start serving it.
> Actually, before I do that, let me change the title. So that's the
> other thing, is I showed you a little bit earlier how you could make
> changes while the website is being served. And that works for
> everything except your changes to your config file. If you change your
> config file, you actually need to stop your website from running, and
> serve it again in order to get those changes to appear. So I'm going
> to say Hector's Rockin' Site because I'm not very creative. So if I
> remember correctly, this part here appears on the footer of the site.
> So maybe I'll say something here like, "Welcome to my awesome site!"
> Because, again, I'm not very creative. Save that. Let's do bundle exec
> jekyll serve. Take a look at what that looks like. There you go.\


### S1\
[25:24.871]

> So now, the site title has been changed. In addition to that, the
> footer has been changed. So this part right here, the reason that's
> been changed is that's all set by the theme that I'm using. And the
> default theme that I'm using was set up-- it's called Minima, and it
> was set up when I used jekyll new. Okay? Now, this is all coming from
> my index.md file. Notice that it's using a layout called Home. I don't
> see that layout here because it's already part of the theme. But I
> can, if I want to, create custom layouts. So there's the link to the
> documentation right there on how to do it. Let's go ahead and practice
> creating a custom layout just so we can see how that works. So the way
> that it works is you would need to create a folder that's called
> \_layouts. And inside that folder, you would create a file - I'm going
> to call this one Hectors - for your layout. Now, that file needs to
> have some front matter in it. So you do that by including some three
> dashes before and after the front matter. And the reason for that is
> so that Jekyll's able to see it. Essentially, Jekyll won't be able to
> see anything that doesn't have front matter on it, the three dashes
> before and after it. Okay?\


### S1\
[26:51.365]

> So now that I've done that, I can go ahead and change my index file to
> use that layout instead of Home. So I'm going to say use Hectors. Now,
> things are going to look kind of funky because my Hectors layout
> doesn't really have anything on it. So notice it's blank. That's
> because the Hectors layout doesn't include anything. I could, if I
> want to, say that this also uses the Home layout. So what that'll do
> is it'll bring in the Home layout into this as well. Or I could start
> building some of this on my own. So I could start making references to
> some of the variables in my config file using Liquid syntax. So let me
> take out the layout for just a second. I believe that's how you
> comment front matter. Yup. There it is. And let me say that, instead,
> here, I want-- so I'm going to go ahead and do something static. So
> I'm just going to say, "Some static text..." here. Show you what that
> looks like. So notice that this static text is showing even though
> this is actually trying to render my index file. That index file has
> been classified as having a layout called Hectors. And that layout
> just has some static text on it. Nothing special. But what I can do is
> start using some of the variables in my config file. So let me go
> ahead and do that. So I can say some things like, "The title of this
> website is--" and then using some Liquid syntax here which is
> essentially two curly braces, you can say anything that's in the
> config file lives under the site object. So you can say, "site.", and
> then the name of the variable - site.title here.\

### S1\
[28:36.041]

> Now, if I save this, and go back here, you'll see that it says, "The
> title of this website is Hector's Rockin' Site," because that is the
> title variable inside the site object. And I can make references to
> any of the other specifics here as well. So you can now imagine how
> that Minima layout that I'm not using anymore, but I can set it back
> again here. Or set it back to that Home layout that I'm not using
> anymore. You could figure out how that layout is doing all these
> things now. So it's getting things like the title, the blog posts
> themselves, the email, the Twitter handle, and all that other good
> stuff. It's getting that from the config file using Liquid, calling
> site. the variable name, and then it's rendering them using HTML, CSS,
> and all that other fun stuff. There is some HTML and CSS on the
> backend that does all this. Okay? And then one more thing I probably
> want to show you is how to use it as a blog because using Jekyll as a
> blogging tool is probably the most popular and common option for using
> Jekyll. So by default, any blog posts live under a posts folder.
> That's what you're seeing here. And they're titled using a four-digit
> year, two-digit month, two-digit day. And they kind of follow this
> format here. So this one right here has a Markdown extension. That
> means that everything is in Markdown. And because there is a Markdown
> processor that we specified - remember, on this config file - we are
> able to read that Markdown.\


### S1\
[30:10.281]

> And so this blog post was dated today. It uses a layout called Post.
> Now, remember how I talked about there's a layout called Home. There's
> another layout called Post. It has a title. It also has some
> categories. So that's also some things that you can specify for your
> Jekyll site, and then this is the body of the layout of the post
> itself. So if I go to Welcome to Jekyll here, you can see how that's
> laid out on the page. Now, if I wanted to create a new post, all I
> have to do is create a new file and date it. Let me actually date this
> one, maybe yesterday, and then you need to give it some front matter
> so that Jekyll is able to see it. And I'm going to call this one, "A
> sample post". So this is the body of my sample post. So save this. And
> now, what I want you to look at is some of the Jekyll magic that gets
> done for you. So back on my root here, if I just refresh this, not
> only do you see the boilerplate post, but then you also see my sample
> post appears here on September 6. And I can go there, and I can say
> this is the body of my sample post. Now, this isn't styled because I
> didn't include the layout in it. So if I go back here, well, the
> layout of this will be-- I believe it was called Post. Yes. So layout,
> Post. And if I refresh this now, now this is properly laid out like a
> post.\


### S1\
[31:47.047]

> So hopefully, I showed you some interesting things you can do with
> Jekyll and GitHub Pages using some simple technologies, using Markdown
> mostly, for styling all your text. You can go as deep down this rabbit
> hole as you like. Just to give you an idea, we have an on-demand
> learning resource. This on-demand learning resource is all powered by
> Jekyll and GitHub Pages. So you can go pretty deep down this rabbit
> hole and do some pretty interesting things. So this is some JavaScript
> and we're hitting the Google Maps API to do some interesting things
> here. We've set up some custom behavior here with these drop-downs,
> and as well as we're using some JavaScript to tell us which part of
> the nav bar we're in, and all other sorts of fun stuff. So the sky is
> the limit for a Jekyll site pretty much, and using GitHub Pages to
> back it up. Hope you enjoyed.
