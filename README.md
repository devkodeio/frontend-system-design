<div align="center">
	<h1>Frontend System Design Guide</h1>
	<h3>Compact guide for building stable large-scale frontend systems</h3>
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

---

### What is this Frontend System Design guide about?

Frontend System Design guide attempts to cover the various factors to be considered while architecting a complex large-scale frontend application from scratch. Also guide acts like a checklist that can be used as a reference for frontend system design. The guide aims to contain the breadth of the frontend systems while giving the directions to explore in depth for both individual contributors and system architects.

	Guide is generic and not biased towards any library or framework

- [Engineering Design](#engineering-design)
- [High Level Design](#hld)
- [Low level Design](#lld)

---

### Engineering Design

- Requirements analysis

  Understand the requirements, clarify, brain storm, refine, PRD,

- Client expectations

  Get the expectations, timelines, focus areas, B2B, B2C, MVP

- Team size and expertise

  Plan the team size, work distribution, development strategies, team skills

- User base/Target audience

  Location, Devices, Internet speed, Technical user?

- Open source vs proprietary

  Licenses, cost, support, community, ease of use, documentation

- Documentation and sign-off

  Develop documentation, UX requirements, client approval

- Development methodology

  Agile / waterfall, TDD, release strategies

---

### HLD

- Platform

  Web, mobile, PWA, Tablet

- SPA vs MPA
- SSR, SSG

  Need for ssr, challenges, drawbacks, libraries

- UX

- Instrumentation

  Error logging, Debugging, user tracking, analytics

- Tech stack

  backend integration, compatibility,

- SEO

  Optimization, opengraph

- CI/CD

  Deployment setup, backup strategies, cloud services

- Server side architecture

  API design, Subdomains, SSO,

- State management

  state handling

- Internationalization

- Unit testing, E2E testing

  Approach, logic testing, UI testing, coverage, report

- Integration (linter, formatting, pre-commits)

  Rules, automation, standards

- Security

  XSS, Token, SSL, cookies, authentication and authorization

- Bundling

  build customization, tree shaking, img compress, micro frontend

- Volume

  QPS, Load testing/Stress test

---

### LLD

- Folder structure

  Flat, nested, atomic design

- Type rules

  Typescript

- Mobile first approach

  CSS rules, media queries, progressive enhancements

- System breakdown

  Components, modules, interfaces, Design Patterns

- Component Design

  Inputs, Outputs, CSS in JS

- Form development

  Form libraries

- Storage management

  Local storage, session, indexed DB, caching

- Routing management

  Routing, gaurds, redirection,

- CSS optimizations

  animations, reuse, css variables, layout,

- Lazy loading of modules

  loading, preloading,

- Accessibility

  contrast, screen readers, Crawling, Ranking, Sitemap, H1 Tag, Meta Keywords, Organic approach, alt, 301 Redirects (bad for SEO), Search visibility, Semantic tags, Open graph protocol

- Image optimizations

  screen size, image type, lazy loading,

- Pagination, Debouncing, Throttling

  Data control, request optimization

- Performance: FCP, LCP, TTI, CLS

  First load, next loads, 1st fold, CRP, shifts, Lighthouse score, RAIL model
