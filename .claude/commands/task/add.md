---
allowed-tools: mcp__taskmaster-ai__add_task, TodoWrite
description: Add one or more tasks to the current tag
---

# Add Tasks

- **User Request:** $ARGUMENTS

## Goal

Add new tasks to your current tag context. Can handle single tasks or multiple tasks at once.

## What You Can Say

### Single Task

```
/add implement user login with email and password
/add create API endpoint for user profile
```

### Multiple Tasks

```
/add
1. Setup database schema
2. Create user authentication
3. Add email verification
4. Implement password reset
```

### With Details

```
/add high priority: implement payment processing with Stripe
/add depends on 5: add payment confirmation emails
```

## How It Works

Based on your input (User Request), I'll:

1. **Parse your request** - Single task or numbered list
2. **Create tasks** in the current tag context
3. **Set dependencies** if you mention "depends on X"
4. **Set priority** if you mention high/medium/low
5. **Confirm** what was added

## Examples

### Quick Add

- `/add fix the login bug` → Creates task "fix the login bug"

### Batch Add

- `/add 1. Setup 2. Test 3. Deploy` → Creates 3 tasks

### With Context

- `/add urgent: fix security vulnerability in auth` → High priority task
- `/add after task 3: add unit tests` → Sets dependency

The command is smart enough to understand your intent from natural language.
