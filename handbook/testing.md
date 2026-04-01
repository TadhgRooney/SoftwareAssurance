# Testing

## Introduction

Software testing is a vital part of software development, helping ensure that systems work as expected and reducing the risk of defects reaching production. By testing this software often, teams can quickly identify issues early and improve overall system reliability.


This section showcases how testing should be approached within our team, including key guidelines, examples of good and bad testing practices, and useful resources.

---

## Testing Guidelines

### What testing should achieve
* Ensure code behaves as expected
* Provide fast reliable feedback
* Catch issues early before production
* Make changes safer and easier

### How we organise tests
- **Unit tests** -> Test small pieces of logic
- **Integration tests** -> Test how components work together
- **End-to-end tests** -> Test full user flows

>**Rule**
> - More low level tests, fewer high level tests
> - Avoid over reliance on UI/end-to-end tests 

### Types of tests we use

**Unit Tests**
- Fast and isolated
- Test functions/classes only
- Use mocks for external dependencies

**Integration Tests**
- Test APIs, databases, services working together
- Focus on real interactions between components
- Provide strong confidence in behaviour

**End-to-End Tests**
- Simulate real user behaviour
- Cover only critical flows (e.g. login, checkout)
- Keep minimal due to cost and flakiness

**Exploratory Testing**
- Manual testing to find edge cases
- Useful for usability and unexpected issues

### Automation & workflow
- Automate tests wherever possible
- Run tests in CI/CD pipeline
- Run fast tests first, slower tests later
- Fail builds immediately when tests fail

### Writing effective tests
- Follow: **Arrange → Act → Assert**
- Test behaviour, not internal implementation
- Keep tests small and focused
- One scenario per test
- Prioritise readability over cleverness

### Reliability of tests
- Tests must be consistent and repeatable
- Fix or remove flaky tests immediately
- Avoid reliance on timing, shared state, or external systems
- Reliable tests are more valuable than many tests

### Testing beyond normal cases
- Test failure scenarios (e.g. downtime, slow responses)
- Simulate real-world conditions where possible
- Use controlled experiments to improve system resilience

### Key principle
- Focus on **quality over quantity**
- A small set of reliable tests is better than many weak ones
- Testing should increase confidence, not slow the team down
---


## Good & Bad practices

### ✅ Good Practices

- **Follow the test pyramid** — write many unit tests, fewer integration tests, 
  and minimal end-to-end tests. More low level tests means faster, cheaper feedback.
- **Test behaviour, not implementation** — tests should verify what the code does, 
  not how it does it internally. This makes tests resilient to refactoring.
- **Fix or remove flaky tests immediately** — a test that sometimes passes and 
  sometimes fails is worse than no test at all. It erodes trust in the entire test suite.
- **Run tests in your CI/CD pipeline** — every push should trigger automated tests. 
  Catching failures early is far cheaper than catching them in production.
- **Test failure scenarios** — intentionally simulate failures like downtime or slow 
  responses to find weaknesses before they cause real problems. Netflix built an 
  entire practice around this called Chaos Engineering.
- **Adapt your strategy to your architecture** — in a microservices system, 
  integration tests matter more than unit tests. Spotify found that focusing 
  on how services interact caught more real bugs than testing services in isolation.

### ❌ Bad Practices

- **Over-relying on end-to-end tests** — they are slow, expensive and flaky. 
  A test suite dominated by end-to-end tests will slow the team down significantly.
- **Ignoring flaky tests** — at Google, over 16% of tests showed some level of 
  flakiness. Ignoring them means the team stops trusting test results entirely.
- **Testing implementation details** — tests that break every time you refactor 
  are not useful. They add maintenance overhead without adding confidence.
- **Skipping tests under time pressure** — in a fast moving startup it is tempting 
  to skip tests to ship faster. This leads to defects in production and slower 
  progress in the long run.
- **Applying the same test strategy everywhere** — a strategy that works for a 
  monolith may actively harm a microservices architecture. Blindly following 
  the test pyramid without considering your system's structure is a common mistake.


---

## Resources

[Find further information here!](../resources/TestingResouce.md)
