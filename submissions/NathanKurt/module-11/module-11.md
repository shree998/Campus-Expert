
* What is the value in using an SSH agent or GitKraken to setup your SSH keys?

  * It takes a lot of the trouble for newbies and dealing with making an SSH key pair, when very few beginners have any idea what an ssh key pair is. It's pretty much idiot proof with GitKraken, while with GitHub there are a lot of things that could go wrong and cause you to screw up.
  
  
* How could you help a Git newbie understand what's happening when they push and pull their contributions to their repo?

  * I normally get out a sheet of paper and make a diagram to show them how it works. Something like ![this](https://github.com/campus-experts/open-training/blob/nathankurt-module-11/submissions/NathanKurt/module-11/Image%20uploaded%20from%20iOS.jpg)
  
  
  
* Why would a team use GitHooks?
  * A team would probably write this to make sure that no formatting errors were made that would be hard to find. For example the whitespace would be very hard to notice if you just looked at the list of changes before committing. Also it could force people to stick to a certain style and format for commits, rebases and other things. It's also a safety measure so you don't screw anything else up. 
  
* How might you write your own custom hook? What would you want it to do?
  * I wrote a bot for slack that would used for imcoming web hoooks by using normal HTTP requests with a JSON payload, which includes the message and a few other optional details. It would first go look at our website, it would check if it returned a 500 error meaning our site was down and we would need to fix it. If it did, it would spam the slack channel every 45 seconds alerting the three people in charge of the website letting them know the site was down. If it didn't have that, it would be fine. It worked pretty well and was super nice.

  
  

