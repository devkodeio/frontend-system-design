<div align="center">
	<h1>Frontend System Design Guide</h1>
	<h3>Interview checklist & style guide</h3>
    	<a href="#javascript-modern-interview-code-challenges-by-topic"><img src="cover.png" alt="banner" width="300px"/></a>
</div>

<div align="center">
    <p>
      <a name="stars"><img src="https://img.shields.io/github/stars/devkodeio/frontend-system-design?style=for-the-badge"></a>
      <a name="forks"><img src="https://img.shields.io/github/forks/devkodeio/frontend-system-design?logoColor=green&style=for-the-badge"></a>
      <a name="contributions"><img src="https://img.shields.io/github/contributors/devkodeio/frontend-system-design?logoColor=green&style=for-the-badge"></a>
      <a name="license"><img src="https://img.shields.io/github/license/devkodeio/frontend-system-design?style=for-the-badge"></a>
    </p>
</div>

<div align="center">
	<p><a href="https://t.me/teamdevkode" target="_blank">Join the frontend telegram community</a></p>
	<p>Show your support by giving a ⭐&nbsp;&nbsp;to this repo</p>
	To download the content as PDF, <a href="./FE_SE_Handbook.pdf" target="_blank">Click here</a>
</div>

---

### What is this Frontend System Design guide about?

Frontend System Design guide attempts to cover the various factors to be considered while architecting a complex large-scale frontend application from scratch. Also the guide acts like a checklist that can be used as a reference for frontend system design. The guide aims to contain the breadth of the frontend systems while giving the directions to explore in depth for both individual contributors and system architects.

	Guide is generic and not biased towards any library or framework

- [Engineering Design](#engineering-design)
- [High Level Design](#high-level-design)
- [Low level Design](#low-level-design)

---

### Engineering Design

- Team size
- User base
- Knowledge base
- Compliance/Governance
- User/Client expectations
- Open source vs proprietary
- Documentation / PRD
- Future Roadmaps

---

### High Level Design

- Platform identification
- SPA vs MPA
- SSR, SSG, CSR
- Tech stack
- Search Engine Optimization
- CI/CD
- User Experience
- [A/B testing](https://philipwalton.com/articles/performant-a-b-testing-with-cloudflare-workers/)
- MVP planning
- Server Side Architecture
- Security
- State Management
- Internationalization
- E2E testing
- Tools Integration
- Authentication & Authorization
- Quality Assurance & Control
- User role management

---

### Low Level Design

- Code/Folder architecture
- Desktop/Mobile first approach
- System breakdown
- Component Design
- Form development
- Storage management
- API Design
- Instrumentation
- Design system
- Routing management
- [CSS optimizations](https://developer.mozilla.org/en-US/docs/Learn/Performance/CSS)
- [Lazy loading of modules](https://web.dev/fast/#lazy-load-images-and-video)
- [Accessibility](https://www.w3.org/WAI/tips/developing/)
- [Image optimizations](https://web.dev/fast/#optimize-your-images)
- Pagination, Debouncing, Throttling
- [Performance](https://developer.mozilla.org/en-US/docs/Web/Performance): FCP, LCP, TTI, CLS
- Versioning
- Unit testing

---

### Architecture Considerations

 - [Client-side Architecture Basics](https://khalilstemmler.com/articles/client-side-architecture/introduction/)
 - [idiomatic.js](https://github.com/rwaldron/idiomatic.js)

### High Level Design details

<br>

**Product Requirement Document (PRD) / Design Document**
- Identify Scope/Requirement
- Review your understanding with stakeholders

<br>

**Discuss about Design/Wireframe**
- Think like an architect.
- We should not consider team bandwidth, capacity and time.
- Discuss about Edge cases.
- Robustness: Handle SPOF (Single Point of Failure) ex: Monitoring, Logging

<br>

**Identify Business**
- Is it B2B (business-to-business)?
- Is it B2C (business-to-consumer)?
- Is it Internal Product?
- Is it Customer facing product?

<br>

**Identify Platform**
- Desktop
- Mobile
- Tablet

<br>

**Identify Users (Know your audience)**
- Conduct surveys
- Discuss about Location and Devices
- Internet speed
- End Users knowledge base (ex: Technical user)
- Pilot Product (sometimes to understand audience)

<br>

**Identify Design Approach**
- Responsive vs Adaptive design
- Desktop first vs Mobile first

<br>

**Identify APIs**
- Rest APIs / Graph APIs / RPC
- JSON / Protocol buffers

<br>

**Role based management**
- Large system needs roles based access and permissions
- Authentication and Authorization
- Read/Write/View Permissions
- Discuss about Routes/Component access

<br>

**Identify Right Platform (compare frameworks based on the use case)**
- Single Page Applications (Unsuitable for Blogs/News based products)
    - No reloading of a page at navigation
    - No SEO
- Multi Page Applications
    - Reloading of a page at every page navigation.
- Progressive Web Applications
    - Provides offline support and native like functionality.
- Server Side Rendering
    - Better SEO
- Important points to discuss:
    - Are users on mobile?
    - Is SEO needed?
    - Is SPA enough?
    - Is PWA enough? (Service worker, Web Worker)
    - Compare SSR / SSG / CSR
    - Any Pricing model? (optional) - Subscriptions based, Paid APIs 
    - Will my app be Frontend heavy? (or backend heavy)
    - Do I have resources for this skill?
    - Is your application Canvas (or SVG) heavy? (Figma, Draw.io)
    - Is your application webRTC heavy? (Video streaming)

<br>

**Identify User Flow**
- Discuss vision of a product.
- Do we need to build from scratch or we can leverage some existing functionalities
- Discuss about authentication and authorization (Google auth / OAuth)
- Interact with the Product manager to understand the scope before designing the application.
- Discuss happy scenarios.
- Discuss edge cases.
- Discuss failing scenarios

<br>

**Identify MVP (Minimum Viable Product)**
- Problem -> Solution -> Build MVP -> MVP to Customers
- Discuss MVP phase with product manager
- Discuss roadmaps and divide product in milestones
- After MVP release there can be a slight change in design/approach to make the product better

<br>

**Volume of Operations**
- Discuss about the end users of the product
- Identify QPS (Queries per second)
- Discuss about Load testing/Stress testing
- Inject analytics in application (ex: Google analytics, Sentry, NewRelic)
- Analytics data helps us to scale the system

<br>

[**SEO (Search Engine Optimization)**](https://github.com/marcobiedermann/search-engine-optimization)
- Crawling
- Use of Heading tags
- [Semantic tags](https://htmlreference.io/)
- Site Ranking
- Sitemap
- Meta Keywords
- Organic approach vs Inorganic approach
- Use of alt tags
- 301 Redirects (bad for SEO)
- Robots.txt
- [Open graph protocol](https://ogp.me/) for social graph

<br>

**Component Based Design**
- Component wise deployment cycle (CI/CD)
- Monolith vs Microservice architecture
- [Micro Frontend (independent dev & deployment for scalability)](https://blog.bitsrc.io/how-we-build-micro-front-ends-d3eeeac0acfc)
- Static components vs Dynamic components 
- IFrame/[Shell](https://github.com/GoogleChromeLabs/sw-precache/tree/master/app-shell-demo) approach

<br>

**State Management**
- How to maintain state through the application?
- How to manage users' data?
- State management Libraries (Redux, Flux, NgRX)

<br>

**Handling APIs**
- Polling (Short and Long)
- Web Sockets (Real-time) (ex: chat, shared editors)
- Batch requests
- GraphQL
- Caching GET APIs (Middleware concepts to cache response)
- [Server-Sent Events (SSE)](https://germano.dev/sse-websockets/)

<br>

**Optimizing Images**
- Add alt attributes (Images should be descriptive for SEO)
- Load images based on screen size (img srcset)
- Image compression (ex: JPEG 2000)
- Image sitemaps
- Use SVGs for generic dimensions (in case of stretching of images)
- Discuss about image Sprites for icons
- Discuss about progressive images (ex: Medium.com) - e.g. [blurhash](https://github.com/woltapp/blurhash)

<br>

**Instrumentation**
- Measurement and tracking are key for a stable system
- Monitoring
- Error logging (for tracing)
- Debugging
- Logs/Track all events happened in the application
- Implement Analytics (GA)
- Sentry (to capture errors)
- Newrelic (to detect failures)

<br>

**Versioning of artifacts**
- Artifacts tracking (ex: Confluence)
- Rollback & backup mechanisms

<br>

**Performance Optimization Techniques**
- Webpack to optimized/compressed pages (Code splitting, [Brotli Compression](https://www.fastfwd.com/improve-http-compression-with-brotli/), [Gzip Compression](https://www.keycdn.com/support/enable-gzip-compression))
- [Web Vitals (FP, LCP, CLS, etc)](https://10up.github.io/Engineering-Best-Practices/performance/#core-web-vitals)
- Lighthouse / PageSpeed Insights
- [Fast Loading (Initial load should be fast)](https://web.dev/fast/)
- Smooth Operations (Loading indicators / Light/Smooth/Meaningful animations (to avoid jerks in transitions) / Splash screens) - (dialog with light animations)
- Animation directions should be the same (dialog coming from bottom should close in bottom) - (smooth animation should be added in sidebars for better UX)
- Animation between data fetching(APIs request) - Skeletal Loaders, Blurhash etc
- [Discuss about Caching - ex: API, resource cache (Browser cache / Memory / CDN / Disk Cache)](https://roadmap.sh/guides/http-caching)
- Pagination vs Infinite Scroll
- Meaningful animation
- [Micro interactions](https://userguiding.com/blog/microinteraction/)

<br>

**Internationalization (i18n) / Localization (i10n)**
- Localization
- Numeric, date and time formats
- Singular &  Plurals
- Use of currency
- Keyboard usage
- Symbols, icons and colors
- Text and graphics vary with different languages and religions, may be subject to misinterpretation or viewed as insensitive
- Varying legal requirements

<br>

 **Accessibility**
- Alt attributes
- Aria-labels
- Multi-device support, [slow network speed](https://addyosmani.com/blog/adaptive-loading/)
- Color contrast, semantics tags

<br>

**Security**
- MITM
- [XSS](https://auth0.com/blog/cross-site-scripting-xss/)
- CSRF
- Clickjacking
- [Content Security Policy (CSP)](https://ponyfoo.com/articles/content-security-policy-in-express-apps#to-get-started-let-s-use-report-only)
- CORS
- [Security headers](https://securityheaders.com/)
- Helpful Tools
    * [Testing your SSL web server](https://www.ssllabs.com/ssltest/analyze.html)
    * [HTTP/2 Test](https://tools.keycdn.com/http2-test)
    * [HTTP Header Checker](https://tools.keycdn.com/curl)
    * [Website Speed Test](https://tools.keycdn.com/speed)
    * [Performance Test](https://tools.keycdn.com/performance)
    * [What Does my site cost?](https://whatdoesmysitecost.com/)
    * [HTML5 Security Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/HTML5_Security_Cheat_Sheet.html)
    * [Production Best Practices : Security](https://expressjs.com/en/advanced/best-practice-security.html)
    * [Web Application Vulnerabiliies Index](https://www.netsparker.com/web-vulnerability-scanner/vulnerabilities/)

<br>

**Quality assurance and control**
- Stable products are successful
- Specify standards - Code level / Artifacts level / Asset level
- Git Hooks (pre commit hooks, husky)
- Linters / Static Analyzers
- Unit testing
- Workflow testing (User level flows) (Tools - Cypress)
- Integration testing
- Automation suite
- [Cross browsers testing](https://github.com/philipwalton/blog/blob/main/articles/learning-how-to-set-up-automated-cross-browser-javascript-unit-testing.md)
- Cross platform testing

<br>

**Governance**
- Controlling the workflows and protecting the assets
- UX Design -> Developers -> Product Managers -> UX Designing -> QA
- Code level governance - like PRs approval (sets standard in your team) - e.g. [Gitflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)
- Artifacts/Assets level governance (before go live)
- like Product Manager approval, Stakeholders approvals

<br>

**Experiment based release cycle**
- Experiment flag, which can help in the release cycle

<br>

**NFR (Non Functional Requirement)**
- Discuss about CI/CD (Docker, Pipeline)
<br>

---

### License

This repository is MIT licensed. [Read more](./LICENSE)

