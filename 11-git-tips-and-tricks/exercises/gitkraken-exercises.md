# Git Tips & Tricks

One of the best things about using GitKraken, is how it helps visualize Git operations for beginners and pros alike. It’s one thing to type out git commands in the CLI, and another to do it in a GUI that visually shows you what you did with each command.

## Tasks

### Exercise 1: Creating SSH key pair

- Create your own SSH key pair manually. Follow the steps on this [GitHub help page.](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/#generating-a-new-ssh-key)

- Create SSH key pair for GitHub using GitKraken. Follow the video instructions or refer to our docs via our [SSH documentation page.](https://support.gitkraken.com/getting-started/authentication). Note: There is no need to set up a passphrase for this step.

*Questions:*
Write the answers to these questions in a file named "module-11.md".

- What is the value in using an SSH agent or GitKraken to setup your SSH keys?
- How could you help a Git newbie understand what's happening when they push and pull their contributions to their repo?


### Exercise 2: Enabling a GitHook

- Initialize a new test repository [from the command line](https://git-scm.com/docs/git-init). You will need to first create a new folder called *test* before initializing git. (Note, we need to initialize from the CLI in order to get access to the default `.git/hooks` folder.)

- Navigate to your `.git/hooks` directory inside your repository. If you are on OSX, you may need to first [enable hidden folders.](https://stackoverflow.com/questions/11197249/show-system-files-show-git-ignore-in-osx_)

- You should see a list of GitHooks with `.sample` appended to name of each file. Open the `pre-commit.sample` hook in a text editor.

- This default pre-commit hook checks for lines with trailing whitespaces and aborts the commit when such a line is found. Rename this file `pre-commit` instead of `pre-commit.sample` from your text editor to enable to hook.

- Let's try to activate the hook in GitKraken! Open your test repo from Step 1 using GitKraken.

- Modify any file in your repo by adding a trailing whitespace, then save the change in your text editor.

- You should now see a WIP node at top of the graph in GitKraken. Select to stage your files.

- Commit your changes. GitKraken should detect your GitHook and provide an error---which is exactly what we want!

*Questions:*
Add the answers to these questions to your file named "module-11.md".

- Why would a team use GitHooks?
- How might you write your own custom hook? What would you want it to do?

## Submitting the exercise

- Navigate to your fork, at https://github.com/YOUR-USERNAME/open-training.
- Create a new branch.
- Navigate to submissions/YOUR-USERNAME and create a new file named "module-11.md".
- Enter the contents of your completed exercise, as described above.
- Commit the file.
- Navigate to https://github.com/campus-experts/open-training.
- Start a pull request and complete the pull request template.
- Make sure you apply the correct labels.
- Open the pull request.
- You're done! We'll review as soon as possible.
