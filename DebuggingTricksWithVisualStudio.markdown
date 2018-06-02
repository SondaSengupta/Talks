# Debugging Tips and Tricks with Visual Studio
## by Joseph Guadango
## Music City Code 2018, Nashville TN


Pdb - portable database has source code and symbols. 
- When you start debugging you attach to the process that allows debugger to attach to the program and intercepts every call. 
It takes less memory and is faster if you don’t debug.
- “Attach to Process” in Debug Menu: allows you to manually attach to another process. Good for debugging some other person’s code or to a server.
- Ozcode is a debug developer visual studio extension

## Options Menu for Debugging
- Break all processes. Breaks everything in multithreaded
- Enable Just My Code: the debugger only stops when its only the code you wrote, not in source code or other dlls.
- Enable .NET framework steps allows you to step through .NET source code 

## When you hit a breakpoint:
- Right Click and hit run to cursor same as continue with to that breakpoint. CTRL + 10
- You can go back by moving cursor, but it’s not an undo. It’s a redo this. Local variables get erased
- Dragging yellow arrow error during debugging skips execution.

## Breakpoint Settings
- Hit Count: Hit breakpoint after a certain amount of breakpoints hit
- You can set conditional expression and intellisense allows you to match on current context of variables. Now the breakpoint will be a diamond plus saying that this is a breakpoint plus
- You can export breakpoints to other people so they can debug where you are from breakpoint window.
- You can debug Tasks in the debug menu, same as Processes for Task Manager just for Visual Studio
- You can label breakpoints in the breakpoint window which allows you to only see a certain number breakpoints.
- You can pin the local dropdown and then you can see the values without having to look at the dropdown.

## Windows
- **Locals:** shows you all the variables in scope right now. You can also change the variable value in locals as well. When you change it, it is changed for the rest of the application.
- **Watch:** allows you to watch certain variables. You add these in to the watch window
- **Immediate Window:** Place to execute commands without changing your source code. It’s like Console window in Chrome. It only accesses what is in scope.
Windows > Exceptions allows you to turn/on/off which kind of exceptions you want. So you can turn/off what exceptions get thrown
Using System.Diagnostics => **Debugger Display** to control how the display looks when going through say a list. Full access to any property within that object when it is displayed on the debugger. You need to spell all the properties correctly, but doesn’t throw when there are null exceptions.
- Call Stack goes from specific, most recent to caller methods. Dll.Namespace.Class.method. Green at the spot means the entry point of the call stack
- **Autos:** try to give you variables that you want to know by what changed most recently or what did you specify in the watch. Most of the time, just use watch.
- **Diagnostic Tools:** show where exceptions and compares it to the timeline of the applications.
