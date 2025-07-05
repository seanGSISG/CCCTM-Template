---
allowed-tools: mcp__taskmaster-ai__set_task_status, mcp__taskmaster-ai__next_task, TodoWrite
description: Mark task as complete and optionally get next task
---

# Task Done

**User Request:** $ARGUMENTS

## Goal

Mark task(s) as complete. By default, also shows the next task.

## What You Can Say

```
/done 3                    # Mark task 3 as done, show next
/done 3 stop               # Mark done, don't show next
/done 5,7,9               # Mark multiple tasks done
/done                     # Mark current task done (if tracking)
```
