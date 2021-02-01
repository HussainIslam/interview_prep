# Developer Interview Preparation

1. **What is HTTP/3?** HTTP-over-QUIC (encrypted general purpose transport layer protocol). This can create multiple streams of data using multiplexing. QUIC also improves privacy.

2. **What is CORS?** Cross-Origin Resource Sharing. HTTP header-base mechanism to allow a server to indicate any other origins than it's own from which a browser should permit loading of resources. The browser makes a preflight request to the server hosting cross-origin resouce to check whether the server will allow actual request. In the preflight request, browser indicates which method and headers will be used in actual header. ([References](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS)).

3. **What are the advantages of HTTP/2 over HTTP/1?** Differences between HTTP/1 and HTTP/2 are ([References](https://moz.com/blog/http2-a-fast-secure-bedrock-for-the-future-of-seo):
	* HTTP/2 is binary, instead of textual
	* HTTP/2 is fully multiplexed vs ordered and blocking
	* HTTP/2 can use one connection for parallelism
	* HTTP/2 uses header compression to readuce overhead
	* HTTP/2 allows servers to 'push' responses to client caches


4. **What is difference between 'null' and 'undefined' values?** The definitions are: 
	* **null**: variable has been created explicitly assigning no value to it; intensional absence of any object value; one of Javascript's primitive types; treated as _false_ for boolean operations. It's type is _object_. 
	* **undefined**: this is where the variable is declared but value has been defined; also a primitive type of Javascript; property of global object;

5. **What is Scope in Javascript? What are the different types of scopes?** _Scope_ is the portion of code where a variable, function, or object is accessible. This defines the visibility of that resource. There are two types of scopes in Javascript:
	1. **Global Scope**: Any variable/function/object defined in global scope is available to all the other scopes. There is only one Global scope throughout a JS document.
	2. **Local Scope**: Variables defined inside a function are in local scope.

6. **How to optimize your website's loading time?** The ways to speedup the webpages would be ([Reference](https://www.crazyegg.com/blog/speed-up-your-website/):
	* Minimize HTTP requests
	* Minify and combine files
	* Asynchronous loading of CSS and JS files
	* Minimize Titme to first byte (TTFB)
	* Reduce server response time
	* Right type of hosting
	* Enable compression
	* Enable browser caching
	* Reduce image size
	* Use CDN
	* Lazy loading 
	* Reduce redirects

7. **What are the different HTTP request types supported by RESTful Web Services?** HTTP request types supported by RESTful Web Services ([References](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods)):
	1. GET: requests data
	2. HEAD: similar to GET but don't get response body
	3. POST: submit an entity to resource
	4. PUT: replaces all current representations with payload
	5. DELETE: deletes resouces
	6. CONNECT: creates a tunnel to server
	7. OPTIONS: used to describe communication options
	8. TRACE: performs message loop-back test to target
	9. PATCH: partial modifications to resources

8. **Explain the difference between stateless and stateful protocols. Which type of protocol is HTTP?** A _stateless_ communications protocol treats each request as an independent transaction. So, it does not require the server to retain any identity, or status information spanning multiple requests from the same source. Similarly, the requestor can not rely on any such information being retained by the responder. In contrast, a _stateful_ communications protocol is one in which the responder maintains “state” information (session data, identity, status, etc.) across multiple requests from the same source.

HTTP is a stateless protocol. HTTP does not require server to retain information or status about each user for the duration of multiple requests.

9. **What is the difference between PUT and POST?** The primary difference between these two is that PUT requests are idempotent. That is, calling the same PUT multiple times produces the same result. For example, the first time PUT is called, it will create if the resource doesn't exists; otherwise, it will update the resource. On the contrary, if POST is called multiple times, it will create multiple resouces [Reference](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/PUT).

10. **What is a stack and what is a heap? What's a stack overflow?**

11. **What are first-party cookies and third-party cookies? What are the differences?**

12. **What are differences between REST and SOAP?**

13. **What is statelessness?**

14. **What is MVC?**

15. **What would you do to understand if your code has a bad design?**

16. **Why has Object-Oriented Design dominated the market for so many years?**

17. **What's the difference between cohesion and coupling?**

18. **What are the basic concepts of Object-oriented design?**
19. **Can you name two programming paradigms important for JavaScript app developers?**

JavaScript is a multi-paradigm language, supporting imperative/procedural
programming along with OOP (Object-Oriented Programming) and functional
programming. JavaScript supports OOP with prototypal inheritance.

20. **What is functional programming?**

Functional programming produces programs by composing mathematical functions and
avoids shared state & mutable data. Lisp (specified in 1958) was among the first
languages to support functional programming, and was heavily inspired by lambda
calculus. Lisp and many Lisp family languages are still in common use today.
Functional programming is an essential concept in JavaScript (one of the two
    pillars of JavaScript). Several common functional utilities were added to
JavaScript in ES5.

21. **What is the difference between classical inheritance and prototypal inheritance?**

**Class Inheritance:** instances inherit from classes (like a blueprint — a
    description of the class), and create sub-class relationships, hierarchical
class taxonomies. Instances are typically instantiated via constructor functions
with the `new` keyword. Class inheritance may or may not use the `class` keyword
from ES6.

**Prototypal Inheritance:** instances inherit directly from other objects. Instances
are typically instantiated via factory functions or `Object.create()`. Instances
may be composed from many different objects, allowing for easy selective
inheritance.

22. **What are the pros and cons of functional programming vs object-oriented programming?**

**OOP Pros:** It’s easy to understand the basic concept of objects and easy to
interpret the meaning of method calls. OOP tends to use an imperative style
rather than a declarative style, which reads like a straight-forward set of
instructions for the computer to follow.  

OOP Cons: OOP Typically depends on
shared state. Objects and behaviors are typically tacked together on the same
entity, which may be accessed at random by any number of functions with
non-deterministic order, which may lead to undesirable behavior such as race
conditions.  

**FP Pros**: Using the functional paradigm, programmers avoid any
  shared state or side-effects, which eliminates bugs caused by multiple
  functions competing for the same resources. With features such as the
  availability of point-free style (aka tacit programming), functions tend to be
  radically simplified and easily recomposed for more generally reusable code
  compared to OOP.  FP also tends to favor declarative and denotational styles,
  which do not spell out step-by-step instructions for operations, but instead
concentrate on what to do, letting the underlying functions take care of the
how. This leaves tremendous latitude for refactoring and performance
optimization, even allowing you to replace entire algorithms with more efficient
ones with very little code change. (e.g., memoize, or use lazy evaluation in
    place of eager evaluation.) Computation that makes use of pure functions is
also easy to scale across multiple processors, or across distributed computing
clusters without fear of threading resource conflicts, race conditions, etc… 

**FP** Cons: Over exploitation of FP features such as point-free style and large
compositions can potentially reduce readability because the resulting code is
often more abstractly specified, more terse, and less concrete.  More people are
familiar with OO and imperative programming than functional programming, so even
common idioms in functional programming can be confusing to new team members.
FP has a much steeper learning curve than OOP because the broad popularity of
OOP has allowed the language and learning materials of OOP to become more
conversational, whereas the language of FP tends to be much more academic and
formal. FP concepts are frequently written about using idioms and notations from
lambda calculus, algebras, and category theory, all of which requires a prior
knowledge foundation in those domains to be understood.

23. **What does “favor object composition over class inheritance” mean?**

This is a quote from “Design Patterns: Elements of Reusable Object-Oriented
Software”. It means that code reuse should be achieved by assembling smaller
units of functionality into new objects instead of inheriting from classes and
creating object taxonomies.

In other words, use can-do, has-a, or uses-a relationships instead of is-a relationships.

**Good to hear:**
Avoid class hierarchies.
Avoid brittle base class problem.
Avoid tight coupling.
Avoid rigid taxonomy (forced is-a relationships that are eventually wrong for new use cases).
Avoid the gorilla banana problem (“what you wanted was a banana, what you got was a gorilla holding the banana, and the entire jungle”).
Make code more flexible.

25. **What are the pros and cons of monolithic vs microservice architectures?**

Monolithic Pros: The major advantage of the monolithic architecture is that most
apps typically have a large number of cross-cutting concerns, such as logging,
     rate limiting, and security features such audit trails and DOS protection.
     When everything is running through the same app, it’s easy to hook up
     components to those cross-cutting concerns.  There can also be performance
     advantages, since shared-memory access is faster than inter-process
     communication (IPC).

Monolithic cons: Monolithic app services tend to get tightly coupled and
entangled as the application evolves, making it difficult to isolate services
for purposes such as independent scaling or code maintainability.  Monolithic
architectures are also much harder to understand, because there may be
dependencies, side-effects, and magic which are not obvious when you’re looking
at a particular service or controller.

Microservice pros: Microservice architectures are typically better organized,
             since each microservice has a very specific job, and is not
             concerned with the jobs of other components. Decoupled services are
             also easier to recompose and reconfigure to serve the purposes of
             different apps (for example, serving both the web clients and
                 public API).  They can also have performance advantages
             depending on how they’re organized because it’s possible to isolate
             hot services and scale them independent of the rest of the app.

Microservice cons: As you’re building a new microservice architecture, you’re
likely to discover lots of cross-cutting concerns that you did not anticipate at
design time. A monolithic app could establish shared magic helpers or middleware
to handle such cross-cutting concerns without much effort.  In a microservice
architecture, you’ll either need to incur the overhead of separate modules for
each cross-cutting concern, or encapsulate cross-cutting concerns in another
service layer that all traffic gets routed through.  Eventually, even monolthic
architectures tend to route traffic through an outer service layer for
cross-cutting concerns, but with a monolithic architecture, it’s possible to
delay the cost of that work until the project is much more mature.
Microservices are frequently deployed on their own virtual machines or
containers, causing a proliferation of VM wrangling work. These tasks are
frequently automated with container fleet management tools.

## Java
1. What is JVM?
2. What are the differences between JDK, JRE, and JVM?
3. Why is Java 'write once and run everywhere'?
4. What is classloader?
