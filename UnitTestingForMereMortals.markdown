# Unit Testing for Mere Mortals
## by Phil Japikse @ Music City Code 2018

"The main thing that distinguishes legacy code from non-legacy code is tests, or rather the lack of tests" -Michael Feathers

## Why add tests?
- Based on a 2001 study from "Software defect reduction top 10 list" from IEE Computer, Maintenance costs 14,100 dollars as opposed to coding which is around 1000 dollars so its better to add tests that help with maintenance early on.
- Tests help provide documentation on how the code is supposed to behave
- You achieve confidence that what you are coding is doing what is supposed to do
- You give your coworkers and future maintainers courage to change your code since they know they can run the unit tests to make sure the pieces work

## What is Test/Behavioral Driven Development and why you should do it
- It is making sure all your code blocks work as expected
- The problem with TDD is when you put things together, it misses behavior and how things interact together. Behavioral Driven Development helps you determine the spec from your users.
- TDD helps the YAGNI and gold-plating -- just write enough code to make tests pass.
- You end writing less code with single responsibility methods that are small and readable.
- Often there isn't time to go back and add tests to a project

## Unit Test "Code of Honor"
- Test must be indpendent of all other tests
- Test must not be dependent on other data
- Don't use fakes. Use Mocks. Fakes are working implementations. Mocks are a specification that record behavior.

## Structure of a Test
- Arrange: create your dependencies
- Act: one method that you are testing <-- Highlander Principle: there can only be one
- Assert: make as many assertions you need to make sure you test it correctly

## Handling Squirrels
- As I think of something to do, I write it on a piece of paper. When we're working, the hardest thing to do is deal with squirrels-- you are writing something and we multitask and now you have a lot of half-implementations.
- As ideas come up, write it down
- Tackle them in order of confidence
- At the end of day, sometimes you leave a test broken or leave a sentence half-done in order to know where exactly you left off.

## So how do you start
- Start with BDD where you make a report of the behaviors and give it to your BA on whether these are the accurate requirements of the feature. If that is true, go on to TDD part of test or rewrite the BDD tests until they do.
- Start with class and the test class you want to work on.
- Fill out your test, and with the name of the method you are going to use.
- Go back to class and add the method.
- Now, do the most naive implemenation to make it pass.
- Now, add more tests for unhappy/breaking paths and also make those tests pass.

## Keep in mind
- Doing TDD/BDD at first, you will lose productivity. There was study that showed the Agile/TDD/BDD will be slower to release and go to prod, but the code is much better about maintenance and bugs.
- He uses XUnit b/c it gets rid of some problems with NUnit
- Humans should test UI development. UI automation is not worth it.
- Use EF Core to make a fresh database and you drop and recreate the database. He does not use InMemoryProvider and use LocalDB instead.


## Resources
- https://github.com/skimedic/presentations
- www.skimedic.com/blog
- Example of TDD Process: https://www.guru99.com/test-driven-development.html









