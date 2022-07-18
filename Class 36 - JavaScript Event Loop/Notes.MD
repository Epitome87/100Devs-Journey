# Class 36 - JavaScript Event Loops

**Queue**

Like a real queue, the first elemtn which was added to the list will be the first element out. This is called a _FIFO_ (First In First Out) structure.

**Stack**

The first element that enters the stack is the first one that is returned. This is called a stack. The first element which was added to the list will be the last one out. This is called a _LIFO_ (Last In First Out).

**JS Is Running In The Browser!**

V8 Engine
(Parse Code > Runnable Commands)

Windows Runtime (Hosting Environment)
Gives us access to web APIs
Passes stuff like _Libevent_ (event loop)

**Event Loop**

The event loop monitors the callback queue and job queue and decides what needs to be pushed to the call stack.

## Backend

C/C++ APIs in the Node.js environment, rather than Web APIs.

**Libuv** for Async I/O. Event loop with Libuv as well.

## Homework

Watch: https://www.youtube.com/watch?v=8aGhZQkoFbQ
Watch: https://www.youtube.com/watch?v=cCOL7MC4Pl0
Do: https://zellwk.com/blog/crud-express-mongodb/ (SUPER IMPORTANT)
