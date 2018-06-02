# Unit Testing for Mere Mortals
## by Phil Japikse
## Music City Code 2018, Nashville Tennessee

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



