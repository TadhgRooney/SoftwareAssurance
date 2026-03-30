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



---

## Resources

[Find further information here!](../resources/TestingResouce.md)
