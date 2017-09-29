# Learning Git with GitKraken

### What are GitHooks? ~2 minutes
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

### Rebasing with conflicts
