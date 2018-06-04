# Awesome C#: Asynchronous Programming
## by Jeremy Clark, Music City Code 2018

C# takes away a lot of extra lines of code by using async/await. However, under the hood its actually running a variation of tasks, so when you are debugging async/await, you can try thinking of it in terms of task runners.

## What is the Task Asynchronous Pattern?
- Task Based
- Method returns a Task
- Task represents a concurrent operation that may or may not be on a separate thread that can be chained and combined.

## Using Tasks
- If you use task.result then you are locking that thread until it finishes.
- If you use task.ContinueWith has problems:
	- There are 40 overloads :/
	- You can use task.Result in ContinueWith and that result will only run when it is finishes and does not deadlock
	- You can move it into delegate method
	- Await is a syntatic wrapper around task and it pauses the current method until Task is complete, but it is a nonblocking method.
	- Async is a hint to the user. It doesn't make something run asynchronously.
- **Parameter type inference** -- if the compiler can figure out the type of my parameter, I don't have to write it. Note also, if there is only one parameter in a lambda, you don't have to use parantheses
	
- ConfigureAwait(false) means you don't care which thread that the operation. It is good for library threads where you don't need access to the calling context.

## Resources
- Parallel Programming with Microsoft .NET Selecting the Right Pattern for parallel programming, especially if you search for the diagram for "Selecting the Right Pattern" that helps you figure out good pattern to use based on the characteristics you need.
https://adeetc.thothapp.com/classes/PC/1213i/LI51D/resources/1303
- Async in C# 5.0 is a book that talks about using await specifically
- Concurrency in C# is a good cookbook gives sample code
- Learn from people like Stephen Cleary and Stephen Taub
- Jeremy's Blog: http://www.jeremybytes.com/Demos.aspx#TaskAndAwait

