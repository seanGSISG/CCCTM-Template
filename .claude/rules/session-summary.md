# Session Summary
**Session Summary Template Adherence**

**Trigger Phrases:** "session summary", "end of session summary", "summarize this session", "end of session report", "give me a summary"

**Action:**
When any of the trigger phrases are detected, the Claude *must* generate a session summary in @.claude/sessions/ in markdown with the filename format of MM-DD-YY_SESSION-SUMMARY_HHMM.md The following template should be filled with  with relevant information from the current conversation or session, including:

- **Session Date:** The date of the session being summarized.
- **Created:** Current or Modified date and time use `UTC-6` or `IANA time zone identifier`: `America/Denver` .
- **Session Duration:** An estimated duration of the session.
- **Developer:** SSwanson
- **Session Overview:** A concise summary of the main topics and goals, files created or eddited.
- **Accomplishments:** List key achievements, solutions, and their impacts, using the ✅ emoji for completed items.
- **Technical Decisions Made:** Detail any significant technical choices and their rationale.
- **Blockers and Unresolved Issues:** Identify any current obstacles, their impact, and proposed resolutions. Include your opinion on any alternative options that should be considered.
- **Next Steps:** Outline immediate, short-term, medium-term goals - identify if the current session has altered any pre-planned goals.
- **Lessons Learned:** Reflect on insights gained during the session.
- **Repository State:** Summarize the status of any ongoing projects or code.
- **Concluding Statement:** A final paragraph summarizing the overall success and impact of the session, and proposed next actionable steps.

The AI *must not* deviate from the structure, headings, subheadings, and general formatting of the provided template. It should adapt the content to fit the context of the current conversation.

**GitHub Issue Creation:**
After creating the session summary markdown file, Claude must:
1. Create a GitHub issue using the gh CLI with the session summary content
2. Use a descriptive title format: "Session Summary - [Date] [Time]"
3. Apply the "type: session-summary" label
4. Provide the issue URL to the user and append the URL in the markdown file for reference

The command format should be:
```bash
gh issue create \
  --title "Session Summary - $(date +'%Y-%m-%d %I:%M%p')" \
  --body-file ".claude/sessions/[actual-filename]" \
  --label "type: session-summary"
```
