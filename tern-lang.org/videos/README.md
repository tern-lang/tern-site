![Tern](https://raw.githubusercontent.com/tern-lang/tern-site/master/tern-lang.org/img/logo-small.png)
  
This guide illustrates how to get started with developing in the Tern language. Short video clips
are used to provide an overview of how to use the command line interpreter as well as the development environment.

  * [Getting Started](#getting-started)  
      * [Command Line Interpreter](#command-line-interpreter)      
      * [Development Environment](#development-environment)  
      * [Web Development Environment](#web-development-environment)  
      * [Debug Remote Process](#debug-remote-process) 
 * [Example Programs](#example-programs)
      * [Mario](#mario)      
      * [Space Invaders](#space-invaders)  
      * [Flappy Bird](#flappy-bird)  


## Getting Started

To get started you will first need to download the command line interpreter and if require the development environment.
This section provides some very short clips of how to dowload both of these tools and runs through some example code
to clarify how to use them.

### Command Line Interpreter

The command line interpreter is the most basic tool available for running Tern programs. It has several options to specify 
the search path to use in order to locate scripts and assets. However all that is needed is a single argument specifying
the location of the script to run.

[![Command Line Interpreter](http://img.youtube.com/vi/MG27d-g2iSI/0.jpg)](https://www.youtube.com/watch?v=MG27d-g2iSI)

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


### Web Development Environment

The standalone development environment is essentially a web application wrapped with the [Chrome Embedded Framework](https://en.wikipedia.org/wiki/Chromium_Embedded_Framework). To run in server mode you can specify
the port to connect to and debug with a conventional web browser.

[![Web Development Environment](http://img.youtube.com/vi/t0BHpvCC9gw/0.jpg)](https://www.youtube.com/watch?v=t0BHpvCC9gw)

### Debug Remote Process

During the development process it is useful to be able to debug an application. There are also obvious benefits in the ability to attach
the development environment to a remote process that could be running on another machine. In order to enable remote debugging you need
to specify a debug port that the process will listen on. You can also specify whether the application should wait to start running until
the debugger is attached. The following video shows how to attach the development environment to a running process.

[![Debug Remote Process](http://img.youtube.com/vi/JuFA5ZZdOwc/0.jpg)](https://www.youtube.com/watch?v=JuFA5ZZdOwc)

A key benefit to this remote debugging process is that the running application can push its sources to the debugger. You do not need
to have the sources locally. This allows you to see exactly what is running and avoids any issues that can occur when local source
code does not match that of the running process.

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

### Flappy Bird

This is a clone of the [Flappy Bird](https://en.wikipedia.org/wiki/Flappy_Bird) game and is targeted for Android. Below is a YouTube vide of the application
being run and debugged remotely with Tern Studio.

[![Debug Android Game](http://img.youtube.com/vi/oJoTgxaNs8I/0.jpg)](https://www.youtube.com/watch?v=oJoTgxaNs8I)

[Source Code](https://github.com/tern-lang/tern-studio/tree/master/tern-studio/work/android/flappybird/src/flappybird)
