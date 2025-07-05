---
allowed-tools: mcp__taskmaster-ai__add_task, TodoWrite
description: Add tasks interactively with clarifying questions
---

# Add Tasks Interactively

## Context

- **User Request:** $ARGUMENTS
- **Current Tag:** !`jq -r '.currentTag // "master"' .taskmaster/state.json 2>/dev/null || echo "master"`

## Goal

Create well-defined tasks by asking clarifying questions about the feature requirements.

## Process

1. **Analyze Feature Request:** Think deeply about what tasks might be needed.

2. **Ask Clarifying Questions:**

   - Ask 4-6 targeted questions based on the feature
   - Provide lettered/numbered options for easy response
   - Focus on understanding scope and breakdown

3. **Generate Tasks:**
   - Create tasks based on answers
   - Add to current tag context

## Clarifying Questions Framework

Adapt questions based on the specific feature request provided above. Consider these areas:

- **Scope:** "How big is this feature?"
- **Components:** "What are the main parts that need to be built?"
- **Dependencies:** "Does this depend on any existing tasks or features?"
- **Priority:** "How urgent is this feature?"
- **Testing:** "What kind of testing will this need?"
- **Phases:** "Should this be built all at once or in phases?"

## Final Instructions

1. **Think deeply** about the feature request
2. **Ask clarifying questions** with lettered/numbered options
3. **Generate tasks** based on the answers
4. **Add tasks** to the current tag context

## Example Usage

```
/add-interactive user notification system
```

This will:

1. Ask about notification types and delivery methods
2. Understand scope and dependencies
3. Create appropriate tasks based on answers
