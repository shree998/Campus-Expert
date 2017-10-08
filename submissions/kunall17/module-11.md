## Exercise 1: Creating SSH key pair

**What is the value in using an SSH agent or GitKraken to setup your SSH keys?**

SSH Agent is the SSH key which GitKraken uses to add an extra layer of security


<img width="318" src="https://user-images.githubusercontent.com/12700799/30783252-29e94952-a15d-11e7-9e46-3d4133f17781.png">

*(Removed some part due to security reasons)*

**How could you help a Git newbie understand what's happening when they push and pull their contributions to their repo?**

I'll explain how GitHub counts the contributions

- All commits having authored as your email & username which are merged into a standalone repo.
- Opening Pull Request 
- Opening Issue
- Reviewing Pull requests
- Profile setting of counting contributions to private repositories

And recommend a read to this webpage by GitHub https://help.github.com/articles/why-are-my-contributions-not-showing-up-on-my-profile/


## Exercise 2: Enabling a GitHook

After following the exercise I got 

<img width="309" src="https://user-images.githubusercontent.com/12700799/30783296-2f205220-a15e-11e7-81b8-bf28c6d779a6.png">

**Why would a team use GitHooks?**

A team would use GitHooks to execute some task before constructing/creating a new commit.

*(Next answer for an example)*

**How might you write your own custom hook? What would you want it to do?**

I have been working on a React native project ([zulip-mobile](https://github.com/zulip/zulip-mobile)) so to check if the code written follows the code styles (using [prettier](https://github.com/prettier/prettier)) I used the travis CI to check it. 

For more aggressive checking before creating a new commit, I could have used git hooks to make sure whatever is being commited, the code is properly formatted.
As following the code style is pretty easy (& fixing the style as well) this could be used in the git hook, and avoid a travis CI run to check for this error.