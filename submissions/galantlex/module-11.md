The value in using an SSH agent at all is that it is more convenient. Specifically in the case of GitKraken, it's one button press as opposed to lots of command line work, copyiing and pasting, and potential missteps. So that's pretty neat!

I typically talk about the server as being some public square where everyone puts their work out for everyone to see, and everyone can make copies, edit, and redisplay their work. At some point, everyone comes together and agrees (hopefully) on a unified body of work, and that's the master branch. SSH is like a secure delivery of someone's work to and from that square.

A team would use GitHooks to ensure that every push to their repo follows certain standards, such as no trailing whitespaces, or other linter standards. This could reduce the time spent in code review, as well as the time spent manually reinforcing the same standards over and over again.

Personally I would really like a script that runs an eslint before I commit and doesn't let me commit linter errors. So many of my commit messages are just "oops, appeasing linter", and this hook would prevent that.