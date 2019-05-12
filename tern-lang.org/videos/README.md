![Tern](https://raw.githubusercontent.com/tern-lang/tern-site/master/tern-lang.org/img/logo-small.png)
  
This guide illustrates how to get started with developing in the Tern language. Short video clips
are used to provide an overview of how to use the command line interpreter as well as the development environment.

  * [Getting Started](#getting-started)  
      * [Command Line Interpreter](#command-line-interpreter)      
      * [Development Environment](#development-environment)
  * [Debugging](#debugging)
      * [Browser Debugging](#browser-debugging)   
      * [Conditional Debugging](#conditional-debugging)
      * [Debug Coroutines](#debug-coroutines)   
      * [Debug Remote Process](#debug-remote-process)
      * [Reverse Debugging](#reverse-debugging)
  * [Editor](#editor)
      * [Code Completion](#code-completion) 
      * [Error Detection](#error-detection)
  * [Example Programs](#example-programs)
      * [Mario](#mario)      
      * [Space Invaders](#space-invaders) 
      * [Android](#android)
         * [Flappy Bird](#flappy-bird)  


## Getting Started

To get started you will first need to download the command line interpreter and if required the development environment.
This section provides some very short clips of how to dowload both of these tools and runs through some example code
to clarify how to use them.

### Command Line Interpreter

The command line interpreter is the most basic tool available for running Tern programs. It has several options to specify 
the search path to use in order to locate scripts and assets. However all that is needed is a single argument specifying
the location of the script to run.

[![Command Line Interpreter](http://img.youtube.com/vi/_jJHeyFPBu4/0.jpg)](https://www.youtube.com/watch?v=_jJHeyFPBu4)

The following options can be specified with the command line interpreter.

|Short| Long         | Description |
|-----|--------------|-------------|
|--d  |  --directory |   Specify directory to execute in|
|--u  |  --url       |   Specify a URL to download sources from|
|--s  |  --script    |   Script to execute|
|--e  |  --expression|   Expression to evaluate|
|--cp |  --classpath |   Optional classpath file|
|--v  |  --verbose   |   Enable verbose logging|
|--c  |  --check     |   Compile script only|
|--n  |  --notify    |   Specify the URL for debug notifications |
|--p  |  --port      |   Debug port|
|--w  |  --wait      |   Wait for debugger|
|--ve |  --version   |   Implementation version|


### Development Environment

In order to develop sophisticated applications it is often necessary to debug various parts of the code. The following
short clip shows how to download and run the development environment. Several examples are provided for further clarification.

[![Development Environment](http://img.youtube.com/vi/jx1vFXRpW_I/0.jpg)](https://www.youtube.com/watch?v=jx1vFXRpW_I)

The following key bindings are available for the development environment.

| Key Binding | Description |
|-------------|-------------|
| Alt-Left	 |  Navigate Back|
| Alt-Right	 |  Navigate Forward|
| Ctrl-N	 |  New File|
| Ctrl-S	 |  Save File|
| Ctrl-Q	 |  Close File|
| Ctrl-Shift-S	 |  Search Types|
| Ctrl-Shift-O	 |  Search Outline|
| Ctrl-Tab	 |  Format Source|
| Ctrl-Shift-E	 |  Evaluate Expression|
| Ctrl-Shift-M	 |  Toggle Full Screen|
| Ctrl-Shift-L	 |  Switch Layout|
| Ctrl-Shift-P	 |  Switch Project|
| Ctrl-Shift-G	 |  Find Files|
| Ctrl-Shift-H	 |  Global Search & Replace|
| Ctrl-Shift-F	 |  Global Search|
| Ctrl-H	 |  Search & Replace|
| Ctrl-F	 |  Search|
| Ctrl-R	 |  Run Script|
| Ctrl-Shift-R	 |  Run Script With Arguments|
| Ctrl-B	 |  Debug Script|
| Ctrl-Shift-B	 |  Debug Script With Arguments|
| Ctrl-K	 |  Debug Remote Script|
| F8	 |  Resume Script|
| F5	 |  Step In|
| F7	 |  Step Out|
| F6	 |  Step Over|

## Debugging

The development environment comes with a wide array of features that enable you to step through your application and inspect variables. 
The environment itself is a HTML 5 application written with TypeScript and CSS so it is possible to debug applications through the
standalone application or through a web browser. In addition to standard debug actions there are additional capabilities such as
conditional and remote debugging.

### Browser Debugging

The standalone development environment is essentially a web application wrapped with the [Chrome Embedded Framework](https://en.wikipedia.org/wiki/Chromium_Embedded_Framework). To run in server mode you can specify
the port to connect to and debug with a conventional web browser.

[![Web Development Environment](http://img.youtube.com/vi/t0BHpvCC9gw/0.jpg)](https://www.youtube.com/watch?v=t0BHpvCC9gw)

### Conditional Debugging

It can often be useful when debugging large complex applications to set a breakpoint that suspends execution when a specific condition
has been satisfied. For simplicity a debug statement is available in the Tern language. This is similar to the debugger statement in
JavaScript only that it can accept any conditional expression. This debug statement will always be executed for consistency, however it will suspend
execution only when the application is running within the debugger.

[![Conditional Debugging](http://img.youtube.com/vi/Y-1a86jziMc/0.jpg)](https://www.youtube.com/watch?v=Y-1a86jziMc)

### Debug Coroutines

When a function contains a yield expression it becomes a coroutine. It is useful to think of a coroutine as a cursor that will suspend
the execution of the function when something has been yielded from it. This cursor will resume execution after the yield statement with
the same stack variables and execution pointer. 

[![Debug Coroutines](http://img.youtube.com/vi/57vPgs0xNJI/0.jpg)](https://www.youtube.com/watch?v=57vPgs0xNJI)

### Debug Remote Process

During the development process it is useful to be able to debug an application. There are also obvious benefits in the ability to attach
the development environment to a remote process that could be running on another machine. In order to enable remote debugging you need
to specify a debug port that the process will listen on. You can also specify whether the application should wait to start running until
the debugger is attached. The following video shows how to attach the development environment to a running process.

[![Debug Remote Process](http://img.youtube.com/vi/JuFA5ZZdOwc/0.jpg)](https://www.youtube.com/watch?v=JuFA5ZZdOwc)

A key benefit to this remote debugging process is that the running application can push its sources to the debugger. You do not need
to have the sources locally. This allows you to see exactly what is running and avoids any issues that can occur when local source
code does not match that of the running process.

### Reverse Debugging

There are often cases where an application may have an issue that is difficult to replicate. In such scenarios it would be much easier
if the application could notify a debug service when the issue has occured and suspend execution. With reverse debugging you can specify
the URL of the debugger to be notified when a debug statement evaluates to true. When suspended you can navigate through the whole
application and have the debug agent push the sources to the debugger.

[![Reverse Debugging](http://img.youtube.com/vi/BmgmMrOfP0c/0.jpg)](https://www.youtube.com/watch?v=BmgmMrOfP0c)

## Editor

The development environment has an embedded editor for reading and writing code. In addition to syntax highlighting it provides
some tools to assist the developer. Two features of note are the code completion tool and the error detection system.

### Code Completion

For productivity code completion is provided from the development environment editor. It supports import completion as well as variable,
function, and type completion. Below is a short example of these features.

[![Code Completion](http://img.youtube.com/vi/RZVid8GfXAM/0.jpg)](https://www.youtube.com/watch?v=RZVid8GfXAM)

### Error Detection

When a language supports static analysis it is useful to report where there is a code error, either through an incorrect control
flow or through a syntax error. The development environment will highlight the sources and the offending lines of code when such
an error occurs.

[![Error Detection](http://img.youtube.com/vi/6wZS9vyyptU/0.jpg)](https://www.youtube.com/watch?v=6wZS9vyyptU)

## Example Programs

The best way to learn any language is through examples. Below is a collection of examples from applications that have been written in Tern. The source code for these examples are available on Github and are free to download.

### Mario

This is a clone of the [Mario](https://en.wikipedia.org/wiki/Mario_Bros.) game comes with the full source code in addition to the images and sounds. It has
been written twice, once with full static typing and one with dynamic typing. Below is a YouTube video of the 
program being run and debugged with Tern Studio.

[![Debug Desktop Game](http://img.youtube.com/vi/yK4ZyIS3w9o/0.jpg)](https://www.youtube.com/watch?v=yK4ZyIS3w9o)

[Source Code](https://github.com/tern-lang/tern-studio/tree/master/tern-studio/work/demo/games/src/mario)

### Space Invaders

This is a very basic clone of the classic [Space Invaders](https://en.wikipedia.org/wiki/Space_Invaders) game. The implementation is short but leverages some
of the more interesting language features such as async await.

[![Debug Desktop Game](http://img.youtube.com/vi/SXc0eNvrAZs/0.jpg)](https://www.youtube.com/watch?v=SXc0eNvrAZs)

[Source Code](https://github.com/tern-lang/tern-studio/tree/master/tern-studio/work/demo/games/src/spaceinvaders)

### Android

The primary target for this language when it was written was Android. Building, dexing, and uploading APK files to an enumlator is
a very unproductive and frustrating process. Tern is 100% compatible with very early versions of Android and the development 
experience is very simple. To run a Tern application you simply need to include the debug agent in to your application and 
specify the URL for the development environment. The application will connect to the debugger and you can then push and execute
your applications on to the Android device.

#### Flappy Bird

This is a clone of the [Flappy Bird](https://en.wikipedia.org/wiki/Flappy_Bird) game and is targeted for Android. Below is a YouTube vide of the application
being run and debugged remotely with Tern Studio.

[![Debug Android Game](http://img.youtube.com/vi/oJoTgxaNs8I/0.jpg)](https://www.youtube.com/watch?v=oJoTgxaNs8I)

[Source Code](https://github.com/tern-lang/tern-studio/tree/master/tern-studio/work/android/flappybird/src/flappybird)
