# Contribution to [publiclab/image-sequencer](https://github.com/publiclab/image-sequencer)

I found the project from [https://open-source.now.sh/](https://open-source.now.sh/), and it seemed like a good one to start off with since I have a decent amount of experience with JavaScript. I created a [PR](https://github.com/publiclab/image-sequencer/pull/102) that addressed two issues (they were related):

- [Add module options to CLI](https://github.com/publiclab/image-sequencer/issues/97)
- [Multiple step support for CLI](https://github.com/publiclab/image-sequencer/issues/100)

The changes in the PR splits the `step` argument by spaces into an array of steps, as well as iterating through those steps to retrieve their inputs and prompt for their values. This allows a user to specify multiple steps for the sequencer when using it, as well as specify options for inputs that have them.
