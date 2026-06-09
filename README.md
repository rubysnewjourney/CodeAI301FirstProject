# CodeAI301FirstProject
My First open source project for CodePath AI 301
# Contribution [1]: [Add sortBy and filter to User.checkouts]

**Contribution Number:** [1]  
**Student:** [Ruby Khatoon]  
**Issue:** [https://github.com/saleor/saleor/issues/12520]  
**Status:** [Phase I] [Complete]

---

## Why I Chose This Issue

[I chose this issue because I immediately understood the confusion it creates for developers: the global checkouts query supports filtering and sorting, but the User.checkouts field does not. This inconsistency makes the API harder to use and breaks the expectation that similar fields behave similarly. Since I’ve been learning how GraphQL schemas are structured and how resolvers work, this felt like a great opportunity to apply that knowledge in a real project.
This issue also appealed to me as a first contribution because it is small enough to be approachable, yet meaningful enough to improve the clarity and usability of the API. By resolving this ambiguity, I can help make the developer experience more consistent while learning more about Saleor’s schema design patterns, filter/sort utilities, and resolver logic.]

---

## Understanding the Issue

### Problem Description
[The root‑level checkouts query in the GraphQL API already supports both sortBy and filter arguments. However, the User.checkouts field does not expose these same arguments. This creates an inconsistency in the API: developers can sort and filter checkouts globally, but cannot apply the same operations when querying checkouts for a specific user.]

[

The underlying queryset logic appears reusable, so adding these arguments should be straightforward and backward‑compatible.]

### Expected Behavior

[Extend the User.checkouts field to accept the same filter and sortBy arguments used by the root‑level checkouts query.

Update the resolver to pass these arguments into the existing checkout queryset logic.

Add tests to confirm sorting and filtering work correctly on User.checkouts.

Update API documentation to reflect the new arguments.]

### Current Behavior

[The checkouts root query (in graphql/checkout/schema.py) already implements filtering and sorting through existing filtersets and sorters.The User.checkouts field (in graphql/account/types.py) currently exposes pagination arguments but does not accept filter or sortBy.]

### Affected Components

[API file structure
The API files are in saleor/graphql/ directory. Every app has its directory inside with:

schema.py - with definitions of queries and mutations
sorters.py - with definitions of sorters
filters.py - with definitions of filters
types.py - with definitions of corresponding types
enums.py - with related enums
dataloaders.py - with data loaders for the given module
mutations file or directory
tests directory]

---

## Reproduction Process

### Environment Setup

[Notes on setting up your local development environment - challenges you faced, how you solved them]

### Steps to Reproduce

1. [Step 1]
2. [Step 2]
3. [Observed result]

### Reproduction Evidence

- **Commit showing reproduction:** [Link to commit in your fork]
- **Screenshots/logs:** [If applicable]
- **My findings:** [What you discovered during reproduction]

---

## Solution Approach

### Analysis

[Your analysis of the root cause - what's causing the issue?]

### Proposed Solution

[High-level description of your fix approach]

### Implementation Plan

Using UMPIRE framework (adapted):

**Understand:** [Restate the problem]

**Match:** [What similar patterns/solutions exist in the codebase?]

**Plan:** [Step-by-step implementation plan]
1. [Modify file X to do Y]
2. [Add function Z]
3. [Update tests]

**Implement:** [Link to your branch/commits as you work]

**Review:** [Self-review checklist - does it follow the project's contribution guidelines?]

**Evaluate:** [How will you verify it works?]

---

## Testing Strategy

### Unit Tests

- [ ] Test case 1: [Description]
- [ ] Test case 2: [Description]
- [ ] Test case 3: [Description]

### Integration Tests

- [ ] Integration scenario 1
- [ ] Integration scenario 2

### Manual Testing

[What you tested manually and results]

---

## Implementation Notes

### Week [X] Progress

[What you built this week, challenges faced, decisions made]

### Week [Y] Progress

[Continue documenting as you work]

### Code Changes

- **Files modified:** [List]
- **Key commits:** [Links to important commits]
- **Approach decisions:** [Why you chose certain approaches]

---

## Pull Request

**PR Link:** [GitHub PR URL when submitted]

**PR Description:** [Draft or final PR description - much of the content above can be adapted]

**Maintainer Feedback:**
- [Date]: [Summary of feedback received]
- [Date]: [How you addressed it]

**Status:** [Awaiting review / Iterating / Approved / Merged]

---

## Learnings & Reflections

### Technical Skills Gained

[What you learned technically]

### Challenges Overcome

[What was hard and how you solved it]

### What I'd Do Differently Next Time

[Reflection on your process]

---

## Resources Used

- [Link to helpful documentation]
- [Tutorial or Stack Overflow post that helped]
- [GitHub issues or discussions that helped]


