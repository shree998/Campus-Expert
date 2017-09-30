# Learning Git with GitKraken

### What are GitHooks? ~2 minutes
[Video](https://www.youtube.com/watch?v=ZZgyILr-TjA&list=PLe6EXFvnTV7-_41SpakZoTIYCgX4aMTdU&index=1)
Githooks are shell scripts that trigger when you perform a specific action in git. They are useful tools for automating checks as you move through your general workflow.

 You can trigger githooks around specific git actions. For example, you can set up a githook that prevents you from committing if the hook script detects a problem.  

Githooks exist as simple text files in your .git/hooks directory.

If you just initialized a repo, there will be a .git folder in your repo with some of the sample git hooks under the hooks folder. If you do not see this folder, you will need to first make sure you can see hidden folders on your operating system.

As another example, let’s set up a pre-commit git hook and trigger it using GitKraken.

Here I have my .git/hook directory and inside we have our pre-commit git hook, which checks for trailing whitespace, lines that only have whitespace, and more.

I’m going to make a quick change in one of my files but leave a few trailing whitespaces so I trigger the hook.

Next let’s go to GitKraken where I have my repo up. I will stage my files, type a quick message, and commit.

Boom. The pre-commit hook has been automatically triggered by the trailing whitespace and GitKraken has aborted the commit. However --- I can review what triggered the hook, then use that information to correct the problem and commit with no issue. Yay git hooks!

This is just one example git hook as the trigger conditions are up to your imagination. The possibilities are endless, so be sure to take them for a spin.


### What is Squashing? ~2 minutes
[Video](https://www.youtube.com/watch?v=cr1N8VTRmfM&t=2s&list=PLe6EXFvnTV7-_41SpakZoTIYCgX4aMTdU&index=2)
What is squashing? And why would you squash commits?

Squashing is a way to rewrite your commit history.

It can help clean up and reduce the noise in your commit history before you share your work with others.

When squashing commits, you are taking the changes from one commit and introducing those changes into its parent commit.

You can do this a number of times, to go from many commits --- to just one single commit with all your changes.

As an example, let’s squash commits in GitKraken.

GitKraken will let you squash commits that meet the following criteria:

More than one commit selected
Youngest commit is also the current HEAD commit
Genealogically consecutive
Chronologically consecutive
Oldest commit in the list has a parent

If all these conditions are met, the Squash option appears when you right click the commit node after selecting your commits in GitKraken.

You can select multiple commits by first selecting one commit, then hold the shift key as you click the another commit. From here, you can squash.

And then voila! GitKraken has cleaned up your commit history and it is now ready to share with others.





### What is SSH? ~3 minutes
[Video](https://www.youtube.com/watch?v=z7jVOenqFYk&list=PLe6EXFvnTV7-_41SpakZoTIYCgX4aMTdU&index=3)
SSH is a network protocol that allows one computer to securely connect to another computer over an unsecured network, like the internet.

Without encryption, data travels over the web in plain text --- which makes it easy for someone to intercept username or password data, and then use it.

However, SSH encrypts your data through a tunnel so you can :

Securely log in to a remote machine
Securely transmit files
Or safely issue remote commands and more


SSH is commonly implemented using the client-server model.  One computer is called the “SSH client” and another machine acts as the “SSH Server.”

SSH can then be setup using  a pair of keys.

a public key that is stored on the SSH server
And a private key that is locally stored on the SSH client

The SSH Client (which is usually your computer) will make contact with the SSH server, and provides the ID of the key pair it wants to use to prove its identity.

The SSH server then creates a challenge which is encrypted by the public key, and sent back to the client.

You as the client then take challenge, decrypt it with your private key and send the original challenge back to the SSH server. Once the negotiation is complete, the connection is established and you can get to work.

So how does GitKraken play a role with SSH?

Well instead of using your local machine as the SSH Client, your local machine can use an SSH Agent to negotiate with the SSH Server as an additional layer of security and convenience.

While GK is not a traditional SSH agent that can be used by other applications, it can negotiate with SSH Servers on your behalf.

Let’s see it in action!

[Goes to GK]

Navigate over to preferences and then click Authentication to access your SSH settings.

If you already have a pair of SSH keys, this is where you can set the path to your public and private keys. Otherwise you can also tell GK to generate a new pair for you.

If you are using any of the integrations, you may either again just provide the path to your existing SSH key pair or tell GK to generate a key pair for you.

GitKraken will use these SSH keys to communicate to the SSH servers. And all actions between your local repository and remotes will travel safely through your SSH connection.

If you like this video, please subscribe to our channel or watch other videos in this series. Thanks for watching and we’ll see you in the next video.


### Rebasing with no conflicts
[Video](https://www.youtube.com/watch?v=xKanizFigpk&list=PLe6EXFvnTV7-_41SpakZoTIYCgX4aMTdU&index=4)

Hi, everyone. I wanted to make a quick video comparing rebasing in GitKraken and the command line.

So first I'm going to show rebasing in the command line, and then I'll do the exact same rebase using GitKraken.

I've got one branch called working branch that I'm going to rebase on my remote dev branch.

Let's quickly take a look at what's going on with these remote branches. Now you can see a little bit of the graph and can see the-- okay.

I've got my working branch is here, and then I've got my dev branch, and I just want to rebase, replay my changes on top of the dev branch. I would just do: git rebase origin dev.

And then, we'll just take a look at those changes. And now you can see, I've got my dev changes here and my working branch has been replayed and rebased on top of it.

But firstly, just to take a look at that same thing in GitKraken, here's my working branch and here's dev.

And really just to do the same rebase, I will just drag the working branch on top of the dev branch and select rebase.

Now you can see it's very clean and I've got my dev branch here and the work is replayed right on top of it.

So not only is rebasing very quick in GitKraken, it's also just very clear as to see what exactly is going on.

If you would like to see the differences between rebasing with the CLI versus GitKraken when a conflict occurs, then click on this link for the video.

Okay. That's it. Thanks for watching, and be sure to click the subscribe button if you haven't already.

### Rebasing with conflicts
[Video](https://www.youtube.com/watch?v=-3yqteu-pLM&list=PLe6EXFvnTV7-_41SpakZoTIYCgX4aMTdU&index=5)

In this video, I'm going to cover the differences between rebasing in the CLI versus GitKraken when a conflict occurs.

If you haven't seen the previous video in which I cover rebasing with the CLI, versus rebasing with GitKraken, I recommend you do so before watching this video.

What I want to do is just quickly show another rebase where we're getting a conflict. So I'm going to clear out and I'm going to switch to another branch, git checkout to a branch that's called my changes.

And now I want to rebase on top of a branch called punch-up. Again, I've just got a couple of changes just called my changes and I want to rebase it on top of my punch-up branch.

Git rebase origin punch-up. And now I can see we're actually getting a merge conflict, which can happen during rebasing.

It's a little bit difficult to see what's going on, so I'm just going to do a quick git status. Now we can see, okay, there's an issue. Both are just trying to modify this throne room file.

So let's just open it up in our text editor and now we can see here's the merge conflict. We've got two conflicting changes and we have to just resolve the conflict before we can continue with our rebase.

I've got two versions right here. One where, actually, Chewbacca gets his medal, which is great, and one where he does not. So let's be nice and let's give Chewbacca his medal.

Let's just delete this head version and clean out this other section to resolve the conflict and get it to the state that we want. Go ahead and save.

Now, we need, of course, to stage those changes. And I'll do a quick git status again. Great. So now it says that all conflicts have been resolved. I can go continue the rebase, git rebase continue.

And now there's another conflict, so I've got to do the same thing over again. I'll just do a quick git status. Now I see, all right, it's the opening crawl.

Let's update this in our text editor. They wanted to make it called A New Hope and we wanted to call it Episode IV: The Hope Awakens.

So that's an awesome title so let's just call it that and resolve that merge conflict. Save. Now, of course, we have to stage our changes again.

So it says that all conflicts have been resolved and I can continue on with my rebase. So git rebase continue. And now we're finally done because it's not giving any errors so we assume that everything has gone right.

So now let's take a look at doing those exact same changes in GitKraken. I've got my branch called my changes that I want to rebase on top of this punch-up that was done remotely.

To do this, we just drag and drop, and click rebase my changes on top of punch-up. All right. Now, of course, we would expect to actually get a merge conflict because we did the same thing in the command line but GitKraken actually has its own merge editor so I can see it.

All right. It's the throne room scene that has conflict. This is GitKraken's merge editor. So we could very easily just see the changes on each branch and all we need to do is just select which changes.

I've got this version where Chewy gets a medal, this one where he does not. Let's just give Chewbacca a medal. Now, let's continue on. Just say continue rebase. And now I've got my second conflict, and I can just pull this here.

So do we want A New Hope or The Hope Awakens? So I'm going to select The Hope Awakens. And now, one of the great things with GitKraken Pro is that we can actually edit the output right here.

I can just say, "Okay. Let's call it The Phantom Hope Awakens." And now I can just go and save that. All of my changes have been done. Let's continue the rebase and we're all finished.

So now you can see I've got my changes branch on top of punch-up and everything is a nice, clear line. So it's very easy to see exactly what has been done in GitKraken.

kay. That's it. Thanks for watching. And be sure to click the subscribe button if you haven't already.
