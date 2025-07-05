---
allowed-tools: mcp__taskmaster-ai__update, mcp__taskmaster-ai__update_task, mcp__taskmaster-ai__update_subtask, mcp__taskmaster-ai__get_tasks
description: Update tasks based on implementation changes
---

# Update Tasks

**User Request:** $ARGUMENTS

## Goal

Update tasks when implementation changes from the original plan. Just tell me what changed and I'll update the relevant tasks.

## What You Can Say

```
"We're using MongoDB instead of PostgreSQL"
"Update task 5 to use OAuth instead of JWT"
"All tasks from 10 onwards should use the new API structure"
"Task 7.2 needs a note about the Redis caching we added"
```

## How It Works

Based on what you tell me (User Request), I'll:

1. **Understand the change** from your description
2. **Find affected tasks** automatically or use the ones you specify
3. **Update them** with the new approach
4. **Confirm** what was updated
