# Workshop Plan

This is an idea for **Promises as Monads in JS** - a talk I may give later on,
celebrating that I get Monads.

The audience is either web dev gurus interested in Haskell or web dev beginners
who want to understand fundamentals.

This is an outline... I may link slides if I end up giving this talk.

### Learning Goals

- They will understand how knowing Monads helps them think about processes.
- They will understand why promises exist and how to use them.
- They will feel ready to use promises creatively to avoid ["callback hell"](http://callbackhell.com/)

## Outline

### Demos and examples (first 5 - 10 minutes)

(This could get unfeasible, but assuming much more time than I have *right* now...)

Some interesting examples:
- Have a sample page without the async, but some slow backend.
- Open the inspector on messenger or slack to show the async requests.
- Show some local file IO in node. (Or, depending on the crowd, Haskell.)
- Have an example of 3 or 4 chained promises. (Or a `foldM` in Haskell, so lots of IO.)

#### Stop for questions

### Discussions and Pairing (minutes 10 to 40)

- Have them tweak the synchronous webpage to use promises.
    - This will hopefully be some pairing.
    - There will be a review phase.
- Talk about other uses. (This would be around minute 35 or 40.)
    - Sort of a lead discussion. I may have to mention threading and user input.
- What's a good type signature for `.then`? (Lead on to `>>=` in Haskell and the big reveal that promises are Monads.)

Last 10 minutes will be for questions. And glory -> people used Monads!

### After the event

I'll be available in the community spaces to offer in person help.
Furthermore, the community slack channels would allow me to post my slides and
answer any lingering questions.

## Notes on Participatory Learning


