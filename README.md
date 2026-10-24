# HireMe: Job Application Assistant for Claude

**HireMe** is a free Claude skill that turns Claude into your personal job-application assistant. Tell it about your experience once, then paste any job description to get:

- ✍️ **A tailored cover letter, straight away**, written only from your real experience (no invented numbers)
- 📊 **A quick match rating** (Good / Normal / Poor) with what you're missing and what to watch out for
- 💬 **Answers to HR questions**: reason for leaving, salary, notice period, visa sponsorship, plus any interview question you ask about
- 🔄 **It remembers you**: Claude saves your experience and HR answers, so you never have to repeat them

No coding needed. Works in the regular Claude app on web, desktop and mobile, for jobs in any country.

---

## How it works

1. **Quick setup (a few minutes).** Upload your resume. Claude reads it, asks a couple of questions if something is missing, then asks five essential HR questions: reason for leaving each job, last drawn salary, expected salary, notice period, and visa sponsorship. It helps you phrase your reasons for leaving professionally.
2. **Claude remembers it.** Your details are saved to Claude's memory. You can update them any time ("I got a new job", "add this project").
3. **Paste a job description.** You get a match rating and a ready-to-use cover letter. Ask for an email version, a shorter version, or help with any interview question.

---

## Install (Claude app, no coding)

1. Download **`job-application-assistant.zip`** from the [Releases](../../releases) page. Don't unzip it.
2. In Claude's settings, turn on:
   - **Code execution and file creation** (needed for skills)
   - **Memory** ("Generate memory from chat history"), so Claude can remember your details between chats
3. Go to **Customize → Skills**, click **+ → Create skill → Upload a skill**, and choose the ZIP file.
4. Make sure the skill is toggled **on**. It appears in your list as **job-application-assistant**.
5. Start a new chat and say: **"Help me set up my job applications."**

> Menu names in the Claude app can change. If you can't find them, see Anthropic's guide: [Use skills in Claude](https://support.claude.com/en/articles/12512180).

**Note on privacy settings:** depending on your Claude settings, some details, such as salary figures or visa status, may not be stored in memory. If so, Claude will simply ask for them when an application needs them.

---

## Install (Claude Code)

```bash
git clone https://github.com/kahwaichew/hireme-claude-job-skill.git
cp -r hireme-claude-job-skill/job-application-assistant ~/.claude/skills/
```

In Claude Code, if memory isn't available, the skill keeps your details in a `career-profile.md` file in your current folder and updates it automatically.

---

## Example prompts

- "Here's my resume, set me up." *(attach PDF)*
- *(paste a job description)*. That's it; you'll get a rating and a cover letter.
- "Make it an email instead."
- "How should I answer 'why are you leaving your current job'?"
- "I just started a new job at X, update my experience."
- "Let's practise interview questions for this role."

---

## Honest by design

HireMe helps you present yourself at your best. It reframes tricky topics, such as reasons for leaving, in a positive way. It won't invent experience or make up false reasons, because those tend to fall apart in interviews and reference checks.

## What's inside

```
job-application-assistant/
├── SKILL.md                  # Main instructions Claude follows
└── references/
    ├── hr-questions.md       # The essential HR questions and how to answer them
    └── writing-guide.md      # Rules for cover letters and emails
```

## Contributing

Ideas and pull requests are welcome: translations, writing conventions for more countries, or a better match rating. Please open an issue first for bigger changes.

## License

MIT
