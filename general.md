<div align="center">
<h1>General Questions</h1>
</div>
<ol>
<li>A/B testing</li>

<details><summary>Answer</summary><p>

- A/B testing (also known as split testing) is a process of showing two variants of the same web page to different segments of website visitors at the same time and comparing which variant drives more conversions.

</p></details>

<li>A11y: ARIA</li>

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

<li>A11y: examples of best practices</li>

<details><summary>Answer</summary><p>

- Providing alternative text for images and icon fonts
- Making all functionality of the site available using a keyboard
- Avoiding blinking or flashing elements
- Ensuring all ARIA roles and properties are valid
- Ensuring sufficient contrast between elements
- Avoiding the use of color as the sole means of communication information
- Avoiding the use of CSS pseudo-elements for non-decorative content

</p></details>

<li>A11y: How can we make a form more accessible? (interview)</li>
<li>A11y: skip links What benefit(s) do they provide some of their limitations</li>
<li>A11y: some of the tools available to test the accessibility of a website or web application</li>
<li>A11y: WCAG the differences between A, AA, and AAA compliance</li>
<li>Acceptance testing</li>
<li>Agile</li>
<li>Agile vs. Waterfall</li>
<li>AJAX</li>
<li>Ansible</li>
<li>API</li>

<details><summary>Answer</summary>
<p>

- An application programming interface (API) is a set of clearly defined methods of communication among various components.
- An API simplifies programming by abstracting the underlying implementation and only exposing objects or actions the developer needs.

![API visual](../../blob/master/images/api.png)  
Image credit: [https://learn.g2.com/api](https://learn.g2.com/api)

</p></details>

<li>Apollo</li>
<li>AWS</li>
<li>AWS Lambda</li>
<li>Babel</li>
<li>BDD vs. TDD</li>
<li>Bootstrap vs. Bulma</li>
<li>Bootstrap vs. Materialize</li>
<li>Caching</li>
<li>CI/CD</li>
<li>CLI</li>
<li>CMS</li>
<li>Concurrency vs. Parallelism</li>
<li>Content strategy</li>
<li>CORS. What issue does it address?</li>
<li>Cross Site Scripting (XSS)</li>
<li>CRUD</li>
<li>Data binding</li>
<li>Database sharding</li>
<li>Databases: ACID properties of a transaction</li>
<li>Deadlocks & Mutex</li>
<li>Dependency injection</li>
<li>DevTools: some ways that Chrome DevTools can help us with finding ways to improve our sit</li>performance  
<li>DNS</li>
<li>Docker</li>
<li>Elasticsearch</li>
<li>Extreme Programming (XP)</li>
<li>Flash of Unstyled Content (FOUC). How do you avoid FOUC?</li>
<li>Flutter</li>
<li>Forms: some best practices when designing a form</li>
<li>Four pillars of OOP</li>
<li>Functional programming. How does it differ from object oriented programming?</li>
<li>GraphQL</li>
<li>How would you go about accepting payments via Credit cards or PayPal for a shopping car</li>feature you are developing for a client  
<li>HTTP: How does a 403 differ from 404 error</li>
<li>HTTP: HTTP vs HTTPS</li>
<li>HTTP: Is HTTP the same as REST</li>
<li>HTTP: List some of the HTTP methods that you are familiar with.</li>
<li>HTTP: Purpose of a HTTP header</li>
<li>HTTP: some best practices for a 404 page</li>
<li>HTTP: some causes of a 500 error</li>
<li>HTTP: Status codes</li>
<li>HTTP: What happens behind the scenes when you enter a URL into the browser and press enter</li>(interview)  
<li>Imperative vs. Declarative Programming</li>
<li>JIRA</li>
<li>JPEG vs. PNG vs. GIF</li>
<li>jQuery</li>
<li>jQuery: Why has jQuery become less popular in recent years?</li>
<li>JSON vs. XML</li>
<li>JSONP</li>
<li>Kubernetes</li>
<li>Lazyloading</li>
<li>Library vs. framework</li>
<li>Linters</li>
<li>Load Balancer and its advantages</li>
<li>Low-fidelity vs. High-fidelity prototyping</li>
<li>Microservices and how do they differ from monoliths</li>
<li>Middleware</li>
<li>MVC</li>
<li>MVC: Are MVCs and frameworks the same</li>
<li>MVC: some pros and cons of using an MVC</li>
<li>MVVC</li>
<li>Native vs. Hybrid apps</li>
<li>Nginx</li>
<li>Node.js</li>
<li>NPM & Yarn</li>
<li>ORM</li>
<li>Performance: CDN and the benefit of using one</li>
<li>Performance: domain pre-fetching and how does it help with performance</li>
<li>Performance: How many resources will a browser download from a given domain at a time th</li>exceptions  
<li>Performance: Is it better to perform animations on a webpage using CSS or JavaScript</li>
<li>Performance: Minifying Is it always a good idea to minify</li>
<li>Performance: Name 3 ways to decrease page load (perceived or actual load time).</li>
<li>Performance: some things you can do to make a website compatible with some earlier versions o</li>IE  
<li>Performance: some ways to improve performance of a page</li>
<li>Performance: some ways to increase code maintainability</li>
<li>Performance: some ways to optimize an image for web</li>
<li>Performance: What does it mean for an image to be optimized for web</li>
<li>Polyfill</li>
<li>Progressive enhancement vs. graceful degradation</li>
<li>Progressive rendering</li>
<li>PUT vs. PATCH methods in RESTful APIs</li>
<li>PWA</li>
<li>React</li>
<li>React: Is it always a better idea to use React than Vanilla JavaScript in a project</li>
<li>React: Is React a framework Why or why not</li>
<li>React: some advantages of using React over Vanilla JavaScript</li>
<li>ReactNative</li>
<li>Redis</li>
<li>Redux</li>
<li>REPL</li>
<li>REST</li>

<details><summary>Answer</summary>
<p>

- REST is acronym for REpresentational State Transfer.
- It is an architectural style that developers follow when they create their RESTful APIs.

</p></details>

<li>REST vs. SOAP APIs</li>
<li>RESTful API (6 constraints)</li>

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

<li>RESTful APIs are stateless. What does this mean?</li>

<details><summary>Answer</summary>
<p>

- It means that API requests can be made independently of one another, and each request contains all of the data necessary to complete itself successfully.

</p></details>

<li>RESTful web service request (its four components)</li>
<li>SaaS vs. PaaS</li>
<li>Scrum</li>
<li>Scrum artifacts</li>
<li>Scrum ceremonies</li>
<li>Scrum vs. Kanban</li>
<li>Selenium</li>
<li>SEO: best practices</li>
<li>Server side rendering and why would you want to do it</li>
<li>Server side rendering vs. Client side rendering</li>
<li>Serverless architecture</li>
<li>Shadow DOM</li>
<li>Software Development Life Cycle (SDLC)</li>
<li>SOLID principles</li>
<li>SPA</li>
<li>SPA: When would you not want to use a Single Page Application</li>
<li>SQL injection: As front-end developers, do we need to worry about SQL injections? (interview)</li>
<li>SQL vs. NoSQL databases</li>
<li>SSH</li>
<li>SSL</li>
<li>Static site</li>
<li>Static site: Gatsby vs. Jekyll</li>
<li>Storage: Cookie vs. SessionStorage vs. LocalStorage.</li>
<li>Storage: Cookies vs. Sessions</li>
<li>Storage: the lifetime of local storage</li>
<li>Svelte</li>
<li>SVG</li>
<li>TC39</li>
<li>TCP vs. UDP (Interview)</li>
<li>TCP/IP</li>
<li>Templating languages</li>
<li>Unit testing vs. functional/integration testing</li>
<li>URL vs. URI</li>
<li>URL: Clean URL</li>
<li>Usability testing</li>
<li>UX</li>
<li>UX personas</li>
<li>UX user journey maps</li>
<li>Vector vs. raster images</li>
<li>Virtual DOM</li>
<li>Visual hierarchy</li>
<li>VMs vs. Containers</li>
<li>Web 2.0</li>
<li>Web components</li>
<li>Web workers</li>
<li>Web workers vs. Service worker</li>
<li>WebAssembly (WASM)</li>
<li>WebPack</li>
<li>WebSockets</li>
<li>Wireframe: are you familiar with any wireframing tools?</li>
<li>WordPress</li>
<li>WordPress vs. Drupal vs. Joomla</li>
</ol>
