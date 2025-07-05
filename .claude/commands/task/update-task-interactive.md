---
allowed-tools: mcp__taskmaster-ai__update, mcp__taskmaster-ai__update_task, mcp__taskmaster-ai__update_subtask, mcp__taskmaster-ai__get_tasks
description: Update tasks interactively with clarifying questions
---

# Update Tasks Interactively

## Context

- **User Request:** $ARGUMENTS
- **Current Tag:** !`jq -r '.currentTag // "master"' .taskmaster/state.json 2>/dev/null || echo "master"`

## Goal

Update tasks based on implementation changes by asking clarifying questions to ensure accurate updates.

## Process

1. **Analyze Change:** Think deeply about the implications of the change.

2. **Ask Clarifying Questions:**

   - Ask 4-6 targeted questions about the change
   - Provide lettered/numbered options for easy response
   - Focus on understanding impact and scope

3. **Update Tasks:**
   - Update affected tasks based on answers
   - Show what was changed

## Clarifying Questions Framework

Adapt questions based on the change described above. Consider these areas:

- **Scope:** "Which tasks are affected by this change?"
- **Reason:** "Why was this change made?"
- **Impact:** "How does this affect the implementation approach?"
- **Dependencies:** "Does this change affect task dependencies?"
- **Testing:** "How should test strategies be updated?"
- **Documentation:** "What additional context should be added?"

## Final Instructions

1. **Think deeply** about the change and its implications
2. **Ask clarifying questions** with lettered/numbered options
3. **Update tasks** based on the answers
4. **Confirm** what was updated

## Example Usage

```
/project:task:update-interactive switching to microservices architecture
```

This will:

1. Ask about which components are affected
2. Understand the migration approach
3. Update relevant tasks with new architecture details
