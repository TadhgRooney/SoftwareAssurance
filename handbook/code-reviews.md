# Code Reviews

## Intro
Code reviews are a process where developers examine each other's code before it is 
merged into the main codebase. They are one of the most effective ways to catch bugs 
early, maintain code quality and share knowledge across the team.

In a fast pace startup environment, it can be tempting to skip reviews to save time. 
However, skipping them often leads to more defects reaching production and knowledge 
becoming trapped with individual developers.

Done well, code reviews aren't about criticism, they're a collaborative tool that 
makes the whole team stronger. This section outlines the best practices to follow and 
the common pitfalls to avoid.

---

## Code review guidelines

### Purpose of Code Reviews

- Catch bugs, logic errors, and edge cases early
- Ensure code meets requirements and standards
- Verify test coverage and quality
- Improve maintainability and readability
- Share knowledge across the team (no single point of failure)
- Increase confidence before merging to main

### Code Review Workflow (Typical Flow)
Create branch -> Write code -> Run tests -> Open PR -> Review -> Fix feedback -> Approve -> Merge

- Work is done in **branches**
- Changes are proposed via **Pull Request (PR)**
- Code is reviewed **before merging to main**
- Multiple iterations are expected

### Pull Requests (PRs) – Key Guidelines
**Keep PRs small**
- Aim: ~200–400 lines of code
- Smaller PRs = faster reviews + fewer bugs

**Provide clear context**
- Clear title (what changed)
- Description:
    - What problem it solves
    - What changed
    - How it was tested

**Include testing**
- Unit tests added/updated
- Evidence of testing (results, steps)

**Self-review first**
- Read your own diff before submitting
- Remove debug code, unused changes

**Use draft PRs**
- Get early feedback before final 

### Effective Code Review Practices

**Review in manageable chunks**
- ≤ 400 lines per review
- ≤ 60 minutes per session

**Review slowly and properly**
- < 500 LOC per hour
- Quality > speed

**Focus on key questions**
- Does the code solve the problem?
- Are edge cases handled?
- Is the design clean and maintainable?
- Are tests sufficient?

**Use checklists**
- Common errors
- Style consistency
- Security considerations

### What Reviewers Should Do

- Understand the purpose of the change
- Check correctness and logic
- Suggest improvements (not just issues)
- Ask questions, don’t assume
- Be clear about required vs optional changes
- Test changes when needed

### Collaboration & Culture

- Be respectful and constructive
- Critique the code, not the person
- Avoid rigid or overly harsh reviews
- Encourage discussion and learning
- Share knowledge across the team


### Key Principle

> Code review is not just about catching bugs —  
> it is about improving code quality, sharing knowledge, and building better systems as a team.

## Good Practices

**Ensuring tests are included with new code**
- Code reviews should help verify that appropriate tests have been added or updated when new functionality is introduced.

**Use coding standards consistently**
- Following shared coding conventions makes it easier for reviewers to check code quickly and maintain consistency.

**Ask questions when something is unclear**
- If any team member doesn't understand a piece of code, they should ask the author for clarification. This often highlights areas that could be improved.

## Bad Practices

**Approving without reviewing**
-  Approving pull requests without reviewing the code defeats purpose of code reviews.

**Personal criticism**
- All feedback should be focused on the code rather than the developer.

**Large pull requests**
- Makes it harder to identify defects.
 
---

## Resources
[Find further information here!](../resources/code-reviews.md)
