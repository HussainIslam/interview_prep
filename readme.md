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




## Java
1. What is JVM?
2. What are the differences between JDK, JRE, and JVM?
3. Why is Java 'write once and run everywhere'?
4. What is classloader?
