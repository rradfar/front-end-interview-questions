<div align="center">
<h1>General Questions</h1>
</div>

🌼 A/B testing  

<details><summary>Answer</summary><p>

- A/B testing (also known as split testing) is a process of showing two variants of the same web page to different segments of website visitors at the same time and comparing which variant drives more conversions.

</p></details>

🌼 A11y: ARIA  

<details><summary>Answer</summary><p>

- Accessible Rich Internet Applications (ARIA) is a set of attributes that define ways to make web content and web applications more accessible to people with disabilities.

The following gives no indication to assistive technologies that it is a custom checkbox:

```html
<li tabindex="0" class="checkbox" checked>
  Receive promotional offers
</li>
```

We can improve it by using the `role` and `aria-checked` attributes:

```html
<li tabindex="0" class="checkbox" role="checkbox" checked aria-checked="true">
  Receive promotional offers
</li>
```

</p></details>

🌼 A11y: examples of best practices  

<details><summary>Answer</summary><p>

- Providing alternative text for images and icon fonts
- Making all functionality of the site available using a keyboard
- Avoiding blinking or flashing elements
- Ensuring all ARIA roles and properties are valid
- Ensuring sufficient contrast between elements
- Avoiding the use of color as the sole means of communication information
- Avoiding the use of CSS pseudo-elements for non-decorative content

</p></details>

🌱 A11y: How can we make a form more accessible? (interview)  
🌱 A11y: skip links What benefit(s) do they provide some of their limitations  
🌱 A11y: some of the tools available to test the accessibility of a website or web application  
🌱 A11y: WCAG the differences between A, AA, and AAA compliance  
🌱 Acceptance testing  
🌱 Agile  
🌱 Agile vs. Waterfall  
🌱 AJAX  
🌱 Ansible  
🌼 API  

<details><summary>Answer</summary>
<p>

- An application programming interface (API) is a set of clearly defined methods of communication among various components.
- An API simplifies programming by abstracting the underlying implementation and only exposing objects or actions the developer needs.

![API visual](../../blob/master/images/api.png)  
Image credit: [https://learn.g2.com/api](https://learn.g2.com/api)

</p></details>

🌱 Apollo  
🌱 AWS  
🌱 AWS Lambda  
🌱 Babel  
🌱 BDD vs. TDD  
🌱 Bootstrap vs. Bulma  
🌱 Bootstrap vs. Materialize  
🌱 Caching  
🌱 CI/CD  
🌱 CLI  
🌱 CMS  
🌱 Concurrency vs. Parallelism  
🌱 Content strategy  
🌱 CORS. What issue does it address?  
🌱 Cross Site Scripting (XSS)  
🌱 CRUD  
🌱 Data binding  
🌱 Database sharding  
🌱 Databases: ACID properties of a transaction  
🌱 Deadlocks & Mutex  
🌱 Dependency injection  
🌱 DevTools: some ways that Chrome DevTools can help us with finding ways to improve our site performance  
🌱 DNS  
🌱 Docker  
🌱 Elasticsearch  
🌱 Extreme Programming (XP)  
🌱 Flash of Unstyled Content (FOUC). How do you avoid FOUC?  
🌱 Flutter  
🌱 Forms: some best practices when designing a form  
🌼 Four pillars of OOP  
🌱 Functional programming. How does it differ from object oriented programming?  
🌱 GraphQL  
🌱 How would you go about accepting payments via Credit cards or PayPal for a shopping cart feature you are developing for a client  
🌱 HTTP: How does a 403 differ from 404 error  
🌱 HTTP: HTTP vs HTTPS  
🌱 HTTP: Is HTTP the same as REST  
🌱 HTTP: List some of the HTTP methods that you are familiar with.  
🌱 HTTP: Purpose of a HTTP header  
🌱 HTTP: some best practices for a 404 page  
🌱 HTTP: some causes of a 500 error  
🌱 HTTP: Status codes  
🌱 HTTP: What happens behind the scenes when you enter a URL into the browser and press enter? (interview)  
🌱 Imperative vs. Declarative Programming  
🌱 JIRA  
🌱 JPEG vs. PNG vs. GIF  
🌱 jQuery  
🌱 jQuery: Why has jQuery become less popular in recent years?  
🌱 JSON vs. XML  
🌱 JSONP  
🌱 Kubernetes  
🌱 Lazyloading  
🌼 Library vs. framework  
🌱 Linters  
🌼 Load Balancer and its advantages  
🌱 Low-fidelity vs. High-fidelity prototyping  
🌱 Microservices and how do they differ from monoliths  
🌱 Middleware  
🌱 MVC  
🌱 MVC: Are MVCs and frameworks the same  
🌱 MVC: some pros and cons of using an MVC  
🌱 MVVC  
🌱 Native vs. Hybrid apps  
🌱 Nginx  
🌼 Node.js  
🌱 NPM & Yarn  
🌱 ORM  
🌱 Performance: CDN and the benefit of using one  
🌱 Performance: domain pre-fetching and how does it help with performance  
🌱 Performance: How many resources will a browser download from a given domain at a time the exceptions  
🌱 Performance: Is it better to perform animations on a webpage using CSS or JavaScript  
🌱 Performance: Minifying Is it always a good idea to minify  
🌱 Performance: Name 3 ways to decrease page load (perceived or actual load time).  
🌱 Performance: some things you can do to make a website compatible with some earlier versions of IE  
🌱 Performance: some ways to improve performance of a page  
🌱 Performance: some ways to increase code maintainability  
🌱 Performance: some ways to optimize an image for web  
🌱 Performance: What does it mean for an image to be optimized for web  
🌱 Polyfill  
🌱 Progressive enhancement vs. graceful degradation  
🌱 Progressive rendering  
🌼 PUT vs. PATCH methods in RESTful APIs  
🌱 PWA  
🌱 React  
🌱 React: Is it always a better idea to use React than Vanilla JavaScript in a project  
🌱 React: Is React a framework Why or why not  
🌱 React: some advantages of using React over Vanilla JavaScript  
🌱 ReactNative  
🌱 Redis  
🌱 Redux  
🌱 REPL  
🌼 REST  

<details><summary>Answer</summary>
<p>

- REST is acronym for REpresentational State Transfer.
- It is an architectural style that developers follow when they create their RESTful APIs.

</p></details>

🌱 REST vs. SOAP APIs  
🌼 RESTful API (6 constraints)  

<details><summary>Answer</summary>
<p>

- In order to be a true RESTful API, a web service must adhere to the following six REST architectural constraints:
  
1. **Client-Server based**:  
The client and the server should be separate from each other and allowed to evolve individually and independently.
2. **Use of a uniform interface (UI)**:  
The key to the decoupling client from server is having a uniform interface that allows independent evolution of the application without having the application’s services, models, or actions tightly coupled to the API layer itself. The uniform interface lets the client talk to the server in a single language, independent of the architectural backend of either.
3. **Stateless operations**:  
Meaning that requests can be made independently of one another, and each request contains all of the data necessary to complete itself successfully. A REST API should not rely on data being stored on the server or sessions to determine what to do with a request, but rather solely rely on the data that is provided in that request itself. Identifying information is not being stored on the server when making requests. Instead, each request has the necessary data in itself, such as the API key, access token, user ID, etc.
4. **Caching**:  
A REST API should be designed to encourage the storage of cacheable data on the client side in order to reduce the number of interactions with the API. This means that when data is cacheable, the response should indicate that the data can be stored up to a certain time (expires-at), or in cases where data needs to be real-time, that the response should not be cached by the client.
5. **Layered system**:  
REST allows for an architecture composed of multiple layers of servers. The requesting client need not know whether it’s communicating with the actual server, a proxy, or any other intermediary.
6. **Code on demand (optional)**:  
Most of the time, a server will send back static representations of resources in the form of XML or JSON. However, when necessary, servers can send executable code to the client.

</p></details>

🌼 RESTful APIs are stateless. What does this mean?  

<details><summary>Answer</summary>
<p>

- It means that API requests can be made independently of one another, and each request contains all of the data necessary to complete itself successfully.

</p></details>

🌼 RESTful web service request (its four components)  
🌱 SaaS vs. PaaS  
🌱 Scrum  
🌱 Scrum artifacts  
🌱 Scrum ceremonies  
🌱 Scrum vs. Kanban  
🌱 Selenium  
🌱 SEO: best practices  
🌱 Server side rendering and why would you want to do it  
🌱 Server side rendering vs. Client side rendering  
🌱 Serverless architecture  
🌱 Shadow DOM  
🌱 Software Development Life Cycle (SDLC)  
🌱 SOLID principles  
🌱 SPA  
🌱 SPA: When would you not want to use a Single Page Application  
🌱 SQL injection: As front-end developers, do we need to worry about SQL injections? (interview)  
🌱 SQL vs. NoSQL databases  
🌱 SSH  
🌱 SSL  
🌱 Static site  
🌱 Static cite: Gatsby vs. Jekyll  
🌱 Storage: Cookie vs. SessionStorage vs. LocalStorage.  
🌱 Storage: Cookies vs. Sessions  
🌱 Storage: the lifetime of local storage  
🌱 Svelte  
🌱 SVG  
🌼 TC39  
🌱 TCP vs. UDP (Interview)  
🌱 TCP/IP  
🌱 Templating languages  
🌱 Unit testing vs. functional/integration testing  
🌱 URL vs. URI  
🌱 URL: Clean URL  
🌱 Usability testing  
🌱 UX  
🌱 UX personas  
🌱 UX user journey maps  
🌱 Vector vs. raster images  
🌱 Virtual DOM  
🌱 Visual hierarchy  
🌱 VMs vs. Containers  
🌱 Web 2.0  
🌱 Web components  
🌱 Web workers  
🌱 Web workers vs. Service worker  
🌼 WebAssembly (WASM)  
🌱 WebPack  
🌱 WebSockets  
🌱 Wireframe: are you familiar with any wireframing tools?  
🌱 WordPress  
🌱 WordPress vs. Drupal vs. Joomla  
