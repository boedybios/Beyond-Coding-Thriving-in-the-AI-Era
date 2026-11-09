# Beyond Coding: Thriving in the AI Era

*Growing your skills, adapting to AI, and building a career in tech*

*Mengembangkan Kompetensi, Beradaptasi dengan AI, dan Membangun Karier di Dunia Teknologi*

- **Presenter:** Setia Budi, Machine Learning Engineer at tiket.com
- **Event:** Milad IT Fest 19, Universitas Islam Riau, 10 December 2026
- **Audience:** computer science undergraduates and lecturers
- **Format:** about 45 minutes of talk, then about 15 minutes of Q&A

## About this document

The slides keep each idea to a few words so the talk fits in 45 minutes. This document is the long version. For each slide it explains the reasoning behind the idea, gives worked examples, points out common mistakes, and suggests something to try. The headings follow the deck, and the slide numbers match.

Read it before the talk to see where it’s going, or afterwards to go deeper. The appendices collect the templates and checklists in one place, along with longer answers to common questions, a glossary, and further reading.

## The talk at a glance

AI tools can now write a lot of code. That doesn’t make developers unnecessary, but it does change where their value lies. Writing code is one of four steps in building software, and AI mainly speeds up that one. Understanding the problem, designing a solution, and evaluating the result still depend on human judgment, and so does taking responsibility for what ships.

| Part | Slides | The question it answers |
|---|---|---|
| Opening | 1–3 | What are we trying to figure out? |
| 1 · Change | 4–7 | What is AI actually changing about software work? |
| 2 · Work | 8–15 | How do I use AI well, check its output, and use it responsibly? |
| 3 · Grow | 16–24 | Which skills, projects, and habits should I build now? |
| Close | 25–26 | What should I remember, and what is a developer for? |

## Contents

1. [Opening: the question behind the talk](#opening-the-question-behind-the-talk)
2. [Part 1: What’s changing](#part-1-whats-changing)
3. [Part 2: Working with AI](#part-2-working-with-ai)
4. [Part 3: Growing in the AI era](#part-3-growing-in-the-ai-era)
5. [Closing: five things to remember](#closing-five-things-to-remember)
6. [Appendix A: Toolkit](#appendix-a-toolkit)
7. [Appendix B: Questions students often ask](#appendix-b-questions-students-often-ask)
8. [Appendix C: Glossary](#appendix-c-glossary)
9. [Appendix D: Further reading](#appendix-d-further-reading)
10. [Appendix E: Notes for organizers and presenters](#appendix-e-notes-for-organizers-and-presenters)

---

## Opening: the question behind the talk

*Slides 1–3*

The cover carries a small piece of code that sums up the day:

```
while (learning) {
  build();
  reflect();
}
```

Build something, reflect honestly on how it went, and go around again. The tools will keep changing; that loop is what carries over from one tool to the next.

### Slide 2 · If AI can write code, what is a developer for?

> **On the slide:** One question, left open until the end of the talk.

Many students are already asking this, often anxiously. When it’s put to a room, the answers tend to fall into three groups:

- **“Nothing.”** AI will do the job. This is the fear.
- **“To check what AI writes.”** True, but only part of the picture.
- **“To solve problems.”** Closer. But which problems, and how do you know you’ve solved them?

The question hides an assumption: that a developer’s job *is* writing code. If it were, the worry would be fair. But code has always been a means to an end, which is a working solution to someone’s problem. Compilers, high-level languages, frameworks, open-source libraries, and Q&A sites each took over work that developers used to do by hand or from memory, and each time the work moved toward bigger problems instead of disappearing.

Nobody can promise the future will repeat the past, so the talk doesn’t rely on that. It focuses on what you can control: the skills and habits that stay valuable whichever way the tools go. Each part of the talk adds a piece of the answer, and slide 26 puts the pieces together.

**Try this:** write your own one-sentence answer now, and compare it with slide 26 at the end.

### Slide 3 · Three parts: change, work, grow

> **On the slide:** The roadmap, with about 15 minutes for questions at the end.

The order is deliberate. You can’t use a tool well until you understand what it changes (**Change**). You can’t plan your growth until you know how the work is really done (**Work**). With both in place, you can decide where to spend your limited time as a student (**Grow**).

---

## Part 1: What’s changing

*Slides 4–7*

Before learning how to use AI, get clear on what is actually different. A clear view avoids two opposite mistakes: panicking (“there’s no point learning to code any more”) and ignoring it (“it’s just hype”).

### Slide 5 · From autocomplete to agents

> **On the slide:** Three stages of AI coding tools. At each stage AI takes a bigger piece of the work, so more of your time goes to direction and review.

**Stage 1: Autocomplete.** The editor predicts the next line or block as you type, and you accept or ignore it. You are still the author; AI saves keystrokes. The risk is accepting suggestions on autopilot, pressing Tab without reading.

**Stage 2: Chat assistants.** You describe what you want in plain language, and the AI explains code, drafts whole functions, or suggests approaches. The unit of help grows from a line to a function. Your skill shifts to asking good questions and adapting answers to your project. The risk is pasting in an answer you don’t understand, written for a situation that isn’t yours.

**Stage 3: Coding agents.** An agent works in a loop toward a goal: it reads your codebase, makes a plan, edits several files, runs commands and tests, looks at the results, and tries again. You hand it a task (“add a password reset feature and make the tests pass”) rather than a question. Your job is to set the goal and the limits, review the changes, and decide what to keep. The risks are large changes that are hard to review, and tools running commands with more access than they need.

The stages overlap rather than replace each other, and many developers use all three in a single day. What’s changing is the size of what you hand over: a line, then a function, then a whole task. As it grows, two skills matter more and more:

1. **Saying precisely what you want**, including what “done” means and what must not change.
2. **Reviewing what you get**: reading the changes, running the tests, and noticing what’s missing.

Those two skills are the heart of Part 2.

**Good habits with agents:** work on a separate Git branch, keep each task small enough to review in one sitting, read the whole diff before merging, and never give an agent access to production systems or real credentials.

### Slide 6 · What AI speeds up, and what stays with you

> **On the slide:** AI speeds up boilerplate, syntax recall, first drafts, and explaining unfamiliar code. Understanding the problem, choosing the approach, judging correctness, and owning the result stay with you.

This is the core idea of the talk.

The left column is **mechanical work**: tasks with a clear specification and output you can check, with countless similar examples in public code. That is where AI is strongest.

The right column is **judgment work**, which depends on context that isn’t in the code. Who are the users? What are the constraints: the deadline, the budget, regulations, an existing system? Which trade-offs will the team accept? AI can help here too, by suggesting options or pointing out risks, but it only knows the context you give it, and it can’t be held accountable for the outcome.

**Example: a library management system.** AI can generate the basic create, read, update, and delete code in minutes. Now look at the questions that decide whether the system is actually useful:

- Who uses it: librarians, students, or both? Do they need different screens?
- What happens when a book is lost or returned late? Is there a fine?
- Can a student with an overdue book borrow another one?
- Is a student’s borrowing history private? Who may see it?

None of these is a coding question, and getting them wrong produces a system that runs perfectly and helps nobody.

That is why **the faster code gets written, the more your judgment matters.** When code is cheap to produce, the bottleneck moves to deciding what to build and checking that it’s right. Speed amplifies direction, good or bad: a wrong decision now gets built faster too.

**Reflect:** which column has most of your coursework trained so far? Assignments usually come with a clear specification, which trains the left column. To train the right one, take on projects where *you* define the problem: talk to a real user, write down the trade-offs, and make the call.

### Slide 7 · Writing code is one step out of four

> **On the slide:** Understand → Design → Build → Evaluate. AI can help at every step, but steps 1, 2, and 4 need your judgment. Your role now: design, evaluate, and build with AI.

**Step 1: Understand.** Define the problem and who it’s for. Talk to users, clarify requirements, and agree on what “done” means. A useful habit is writing *acceptance criteria*: short statements that must be true when the work is finished. For the library system: “A student can see the due date of every book they’ve borrowed,” or “Marking a book as lost blocks new loans for that student until it’s resolved.”

**Step 2: Design.** Choose the approach and weigh the trade-offs: the data model, the structure of the app, the libraries. At student scale: one app or several services? A relational database or a document store? Write your own login system or use a well-tested library? (Use the library.) Write each decision down with its reason; you’ll need it for your project write-up (slide 21).

**Step 3: Build.** Write the code, tests, and docs. This is where AI helps most: it drafts, and you steer and edit. Work in small steps and commit often, so every AI-generated change is small enough to review.

**Step 4: Evaluate.** Check that the result is correct, safe, and useful. Run the tests and review the code, then go back to step 1 and ask: does this actually solve the original problem for the original users? Evaluation often reveals a misunderstood requirement, which sends you around the loop again.

It’s a loop, not a straight line, and real teams go around it many times in short cycles.

In class, steps 1 and 2 are often done for you (the assignment *is* the specification), and step 4 is your lecturer’s grading. At work you own all four. As AI drafts more of step 3, steps 1, 2, and 4 are increasingly where developers add value. That is the shift in the seminar’s theme: from someone who writes code to someone who **designs, evaluates, and builds solutions with AI**.

**Try this:** before starting your next assignment, spend 15 minutes on steps 1 and 2. Write down who will use it, what “done” means, two approaches you considered, and why you chose one.

---

## Part 2: Working with AI

*Slides 8–15*

The practical part: how to get real help from AI, how to check what it gives you, and how to use it responsibly.

### Slide 9 · Five everyday ways AI can help you

> **On the slide:** Understand code, explore ideas, debug, write docs, and automate routine work. Treat AI like a fast, eager teammate: very helpful, and sometimes confidently wrong.

| Use | Try asking | How to get the most from it |
|---|---|---|
| Understand code | “Explain this function step by step.” | Follow up with “What happens if the list is empty?”, then run the code to confirm. Great for open-source projects and code you inherit. |
| Explore ideas | “Suggest three designs, with pros and cons.” | Several options keep you from anchoring on the first one. Then add your constraints, such as “Which suits three students with two weeks?” You still choose. |
| Debug | “Here’s the error and the code. Likely causes?” | Include the full error, the relevant code, what you expected, and what you’ve tried. Ask for causes *before* fixes, so you understand the bug instead of hiding it. |
| Write docs | “Draft a README: setup, usage, examples.” | AI turns rough notes into a clear structure. Check every command, version number, and file name it writes. |
| Automate routine work | “Write unit tests for these edge cases.” | Also good for sample data, repetitive refactors, and regular expressions. Read the tests: AI sometimes tests what the code *does* rather than what it *should* do. |

The teammate image is the key. Picture a new teammate who is very fast, has read a huge amount of code, and never gets tired, but who doesn’t know your project, sometimes misremembers details, and rarely says “I’m not sure” unless you ask. You would welcome their help, and you would still review their work before using it.

### Slide 10 · Give AI the context a teammate would need

> **On the slide:** A vague prompt (“fix my code pls”) makes AI guess. A clear prompt gives it four things: context, problem, task, and limits.

When information is missing, a model fills the gaps with the most common assumptions, which may not match your situation, and you get generic advice. A clear prompt removes the guesswork:

- **Context:** what you’re building, with which language, framework, and version. “I’m building a Flask login API for a class project” tells the AI the language, the framework, and the scale.
- **Problem:** what happens, what you expected, the exact error, and the relevant code. “POST /login returns error 500 when the password is empty.”
- **Task:** what you want back, and in what order. “Explain the cause first, then suggest a minimal fix.” Getting the explanation first lets you check the reasoning, and you learn something.
- **Limits:** what must not change. “Keep the function signature. Don’t add new libraries.” Without limits, AI often rewrites more than you asked for.

A template to reuse:

```text
Context: I'm building [what] with [language/framework, version] for [who or why].
Problem: When I [do X], I get [result]. I expected [Y]. The code and full error are below.
Task: First explain the likely cause. Then suggest a minimal fix.
Limits: Keep [what must not change]. Don't [what to avoid].
```

Habits that make prompts work better:

- **Invite questions.** End with “What else do you need to know before answering?”
- **Ask for explanations, not just code.** “Explain why this fixes it.” You learn, and you can check the reasoning.
- **One task per prompt.** Split big requests into steps you can check one at a time.
- **Iterate.** Treat it as a conversation: say what’s wrong with the first answer and refine.
- **Remove secrets and personal data first.** Replace real keys, passwords, and names with placeholders (see slide 14).
- **With agents, say how to check the work.** “Run the tests in `tests/` and make sure they all pass” turns a vague goal into a checkable one.

Good prompting is really clear technical communication. The same four parts make a good bug report, a good forum question, and a good message to a senior engineer, so practicing with AI improves how you work with people too.

### Slide 11 · Know where AI goes wrong

> **On the slide:** Hallucination, outdated knowledge, missing context, security blind spots, and overconfidence. A confident, fluent answer can still be wrong.

One simple mental model explains all five. A language model produces the text most likely to follow your prompt, based on patterns in its training data. Unless a tool connects it to search or documentation, it doesn’t look anything up, and it has no reliable sense of when it doesn’t know.

- **Hallucination.** It can invent a function, a package, an API endpoint, or a reference that sounds real but doesn’t exist. This has a security side: attackers publish malicious packages under names that AI tools tend to invent (sometimes called *slopsquatting*), so installing a hallucinated package name can install malware. Before adding a new dependency, check that it’s on the official registry, actively maintained, widely used, and the one the official docs point to.
- **Outdated knowledge.** Models learn from data up to a cutoff date, and libraries keep changing. Expect suggestions that use old versions or deprecated APIs, and check them against the version in your project and the official documentation.
- **Missing context.** It knows only what you give it. Without your database schema, your conventions, and your users’ constraints, it writes code that is right in general and wrong for you.
- **Security blind spots.** Hardcoded passwords, SQL built by joining strings, no input validation, debug mode left on. Models learned from public code, and public code contains plenty of insecure examples.
- **Overconfidence.** The tone is just as fluent when the answer is wrong, so tone is not evidence. Ask “How confident are you, and how can I check this?”, then check it yourself.

The good news is that predictable failures are checkable failures. The next two slides show how.

### Slide 12 · Never submit code you can’t explain

> **On the slide:** The one rule to remember. Not to your lecturer, not to your team, and never to production.

If you can’t explain a piece of code, you can’t debug it, extend it, defend it in a review, or take responsibility when it fails.

“Explain” means more than “it works.” You should be able to say:

- what each part does, and why it’s written this way rather than another;
- which inputs it handles, and which it doesn’t;
- what could go wrong, and what would happen then.

The rule applies wherever you hand code over. In class, explaining your code is how lecturers check what you learned, so expect to be asked to walk through it. In a team, that’s what code review is for. In production, when something breaks, “the AI wrote it” is never an acceptable answer, because responsibility stays with the people who shipped it.

This isn’t a rule against AI. Use AI to help you understand: ask it to explain the code line by line, then confirm by experimenting. A quick self-test: could you explain it to a classmate with the chat window closed?

### Slide 13 · Four checks before you use AI output

> **On the slide:** Read, run, check, own. AI makes generating code fast; your review is what makes it correct.

**1. Read: can I explain every line?** Go line by line. Look up any function you don’t know in the official docs, or ask the AI to explain it. Watch for things you didn’t ask for: extra features, changed behavior, or new dependencies.

**2. Run: does it pass tests, including edge cases?** Don’t trust “this should work.” Run it, and test the cases that usually break code:

- empty input: an empty string, an empty list, a missing field;
- very large input: a million rows, a very long string;
- invalid input: wrong types, negative numbers, special characters, a name with an apostrophe like *Nur’aini*;
- boundaries: 0, 1, and the maximum allowed value;
- two users doing the same thing at the same moment.

**3. Check: is it secure and efficient?** Look for secrets in the code, user input that reaches a database or shell command without validation, missing permission checks, and loops inside loops over large data. Tools catch a lot of this for you: linters (such as ESLint for JavaScript or Ruff for Python), type checkers, and security scanners (such as Bandit for Python, or GitHub’s secret scanning and Dependabot alerts).

**4. Own: would I defend it in a code review?** Imagine a senior engineer asking, “Why did you do it this way?” If you can’t answer, you’re not done yet.

These checks take minutes and save hours of debugging. Appendix A has them as a checklist.

### Slide 14 · Use AI responsibly: four things to protect

> **On the slide:** Privacy, security, fairness, and rights and integrity. When unsure, don’t paste it, and check your campus or company AI policy first.

**Privacy.** Treat the chat box as public unless you know the tool’s data policy. Depending on the service and your settings, what you paste may be stored and may be used to improve future models. Never paste personal data: names with phone numbers, NIK (national ID numbers), addresses, grades, health information, or customer records. When you need realistic data, make up fake data or anonymize real data first.

In Indonesia, the Personal Data Protection Law (*UU PDP*, Law No. 27 of 2022) governs how personal data is collected and processed. It took full effect in October 2024 after a two-year transition, and it treats some categories, such as health, biometric, and children’s data, as specific personal data that needs extra protection. It applies to the apps you build, not only to what you paste into AI tools. (This is general background, not legal advice.)

**Security.** Never put passwords, API keys, or tokens in a prompt or in code you commit. Keep them in environment variables or a secrets manager, and list files like `.env` in `.gitignore`. If a key leaks, revoke it and issue a new one immediately. Deleting the commit isn’t enough, because the key stays in Git history, and bots constantly scan public repositories for keys. Review AI-written code for common vulnerabilities; the OWASP Top 10 (Appendix D) is a good list to learn.

**Fairness.** If your software ranks, filters, or makes decisions about people (scholarships, hiring, loans, admissions), ask who could be harmed, excluded, or treated unfairly. A scholarship-ranking app that scores “distance to campus” or “owns a laptop” could quietly disadvantage students from some regions or from poorer families. Also ask who can’t use your app at all, such as people on older phones, on slow connections, or using screen readers.

**Rights and integrity.** AI output can closely resemble existing code, so respect licenses. Some licenses, such as the GPL, require software built from the code to be shared under the same license when you distribute it; others, such as MIT, mainly require you to keep the copyright notice. For coursework, follow your lecturer’s rules on AI, and be open about how you used it. A short note is enough, for example: *“I used an AI assistant to explain recursion and to draft unit tests. I wrote the solution myself and checked the tests by hand.”*

### Slide 15 · Who decides? Match AI’s role to the stakes

> **On the slide:** Two questions decide how much to rely on AI: how costly is a mistake, and how easy is it to check? The higher the stakes and the harder it is to check, the more a human must decide.

| | **Easy to check** | **Hard to check** |
|---|---|---|
| **Low stakes** | **Let AI draft freely.** Formatting, sample data, boilerplate | **Use AI for ideas, not answers.** Brainstorming, naming, early research |
| **High stakes** | **AI drafts, you verify carefully.** Payment logic, database migrations | **You decide; AI only advises.** Security design, architecture, decisions about people |

- **Low stakes, easy to check.** If the formatting is wrong you’ll see it immediately, and fixing it costs nothing. Let AI do it.
- **Low stakes, hard to check.** A suggested project name or a summary of “how other apps do it” costs little if it’s wrong, but you can’t easily tell. Treat it as inspiration, not fact.
- **High stakes, easy to check.** Payment logic and database migrations are expensive to get wrong, but you *can* test them: exact amounts, rounding, and currency for payments, and a rehearsal on a copy of the database for migrations. AI can draft, but tests and careful review decide.
- **High stakes, hard to check.** Flaws in a security design or an architecture appear late, under conditions you didn’t test, like an attacker or a hundred times more users. A decision about a person has no test that proves it fair. Here a human must decide and be accountable; AI can only advise.

The deeper lesson: **you can move work to the left of the grid by making it easier to check.** Tests, code review, staging environments, and monitoring all turn “hard to check” into “easier to check,” and building them is often some of the most valuable work a developer does.

---

## Part 3: Growing in the AI era

*Slides 16–24*

If AI changes the work, what should you focus on now, as a student, so you’re ready for it?

### Slide 17 · Skills that matter: three layers

> **On the slide:** Foundations, thinking, and people, held together by learning how to learn.

Read the layers from the bottom up, like a building: each one rests on the layer below.

**Foundations: programming, algorithms and data structures, and how systems work.** This is what lets you understand, debug, and review what AI writes. Aim to know one language well, the core data structures and their costs, the basics of operating systems, networks, and databases, and the everyday tools: Git, testing, and a debugger. *Practice:* implement a few core data structures yourself at least once, read error messages all the way through, and step through code in a debugger instead of guessing.

**Thinking: problem solving, critical thinking, and creativity.** Problem solving is breaking a messy situation into parts you can work on. Critical thinking is questioning claims, including AI’s, and asking what evidence supports them. Creativity is noticing problems other people walk past, and combining ideas in new ways. *Practice:* before coding, write down two different approaches and choose one; review a classmate’s code and explain what you would change and why.

**People: communication, collaboration, and understanding users.** Many project problems come from misunderstood requirements, not from syntax errors. Communication means clear READMEs, issues, and pull request descriptions, and explaining technical ideas to non-technical people. Collaboration means working in a shared repository, reviewing each other’s code, and dividing work fairly. Understanding users means asking good questions and watching how people actually work. *Practice:* present your project to someone outside computer science, join a student organization’s tech team, and interview one real user before you build.

**Holding it together: learning how to learn.** Some of the tools you’ll use in your first job may not exist yet. The lasting skill is picking up something new quickly: reading the official documentation, building a small example, and reflecting on what worked. AI can speed this up, as long as you use it the way slide 19 describes.

### Slide 18 · You can’t review what you don’t understand

> **On the slide:** Three kinds of AI output that look fine but aren’t, and the fundamentals you need to catch each one.

**Performance, caught by algorithms and Big-O thinking.** You need the registered users who are also on a newsletter list, and AI writes:

```python
# Instant with 100 test records, unusable with a million real ones
matches = [email for email in registered if email in newsletter_list]
```

It looks fine and passes the tests. But `email in newsletter_list` scans the list from the start every time, so with a million emails on each side that is up to a trillion comparisons. One extra line fixes it:

```python
newsletter = set(newsletter_list)  # set lookups take constant time on average
matches = [email for email in registered if email in newsletter]
```

You only notice the problem if you know that searching a list is O(n) while looking up a set is O(1) on average.

**Concurrency, caught by knowing how systems work.** A booking feature for an event with limited seats:

```python
event = db.get_event(event_id)
if event.seats_left > 0:        # two requests can both pass this check...
    db.create_booking(user_id, event_id)
    event.seats_left -= 1       # ...and both book the "last" seat
    db.save(event)
```

Tested alone, it works perfectly. In production, two people click “Book” at the same moment, both read `seats_left = 1`, and both get a seat. This is a *race condition*. One fix is to let the database check and update in a single atomic step:

```sql
UPDATE events
SET seats_left = seats_left - 1
WHERE id = :event_id AND seats_left > 0;
-- Create the booking only if this updated one row; if it updated none, the event is full.
```

You only think to look for this if you know about concurrency and transactions.

**Security, caught by security basics.** A login that works, but builds its SQL from user input:

```python
# Vulnerable: user input becomes part of the SQL itself
query = f"SELECT * FROM users WHERE username = '{username}' AND password = '{password}'"
```

If someone types `' OR '1'='1` as the password, the condition becomes `username = '...' AND password = '' OR '1'='1'`, which is true for every row, so the login succeeds without a valid password. This is *SQL injection*. The fix is a parameterized query, where the database driver sends the input separately from the SQL. Passwords also shouldn’t be stored as plain text, but as hashes made with an algorithm designed for passwords, such as bcrypt, scrypt, or Argon2:

```python
from werkzeug.security import check_password_hash

cursor.execute("SELECT id, password_hash FROM users WHERE username = %s", (username,))
row = cursor.fetchone()
logged_in = row is not None and check_password_hash(row[1], password)
```

(The placeholder, `%s` or `?`, depends on the database driver. Werkzeug is the library underneath Flask.)

The takeaway: courses like data structures, operating systems, databases, networks, and security matter *more* with AI, not less. They are how you spot what AI got wrong.

### Slide 19 · Use AI to learn, not to skip learning

> **On the slide:** The same tool can build your skill or build dependence. Rule of thumb: if AI disappeared tomorrow, could you still do this?

You learn when your brain has to work: recalling, struggling, making mistakes, and correcting them. Learning researchers call this kind of productive effort a *desirable difficulty*. If AI removes all the struggle, it removes most of the learning with it. The goal is to use AI in a way that still leaves the thinking to you.

A healthy routine for exercises and assignments (where your lecturer allows AI):

1. **Try first.** Work on the problem yourself for 20 to 30 minutes.
2. **Ask for a hint, not the answer.** *“Here is my attempt. Don’t give me the solution. Point out my mistake and give me a hint.”*
3. **Keep asking “why?”** until you can explain the idea in your own words.
4. **Rebuild it without AI.** Close the chat and solve it again from scratch, ideally the next day. If you can’t, you haven’t learned it yet.

AI also makes a patient tutor:

- *“Quiz me on binary search trees. Ask one question at a time and wait for my answer.”*
- *“Explain recursion with an everyday analogy, then give me a small exercise.”*
- *“I think hash map lookups are always O(1). When is that not true?”*

The warning signs on the slide are worth taking seriously: pasting the assignment and submitting the answer, copying code you haven’t read, asking AI before thinking about the problem, and being unable to explain your own project. Each feels faster today and costs you later: in an exam, in a technical interview, or at your first production bug.

### Slide 20 · Build a portfolio that shows how you think

> **On the slide:** Real projects, teamwork, and your process. When anyone can generate code, your reasoning is what stands out.

A working app is now much easier to produce, so on its own it says less about you. What still stands out is evidence of judgment: you picked a real problem, worked with others, and made sensible decisions along the way.

**Real projects.** A tutorial clone says little; a small app used by 20 people in your organization or at a nearby business says a lot. Real users bring feedback, surprises, and stories, and stories are what interviews are made of. Good places to look: your campus, a local UMKM (a micro, small, or medium business), your community, or a problem you have yourself.

**Teamwork.** Show that you can work with others: contribute to open source (start with documentation fixes or issues labeled “good first issue”), build with a group, or join a hackathon. A Git history with clear commit messages and pull request discussions is evidence in itself.

**Your process.** Keep a short decision log in your repository: the date, the decision, the options you considered, and why you chose one. Interviewers often ask “Walk me through a decision you made,” and the log prepares your answer.

Someone looking at your portfolio will usually read the README first, then look at a demo or screenshots, and only then open the code, so make those first two count. Two or three finished, well-documented projects beat ten half-finished ones.

### Slide 21 · What a strong project write-up includes

> **On the slide:** Problem, constraints, options, decision, AI’s role, and results. Put it in your README.

| # | Section | The question it answers |
|---|---|---|
| 1 | Problem | Who has it, and why does it matter? |
| 2 | Constraints | What limits did you work within: time, data, budget, technical? |
| 3 | Options | Which approaches did you consider? |
| 4 | Decision | What did you choose, and why? |
| 5 | AI’s role | What did AI help with, and how did you verify it? |
| 6 | Results | What worked, what didn’t, and what would you change? |

Section 5 is new in the AI era. Being honest about how you used AI, and how you checked its work, shows maturity. It’s a strength, not something to hide.

**A short example** (a made-up project, to show the shape):

> **Problem.** A coffee shop near campus takes orders through WhatsApp. At busy times the owner loses track of which orders are paid and which are ready.
>
> **Constraints.** Two weeks, one developer, no budget for paid hosting. The owner uses an Android phone and has no time to learn a complicated app.
>
> **Options.** A shared spreadsheet with a form; a small web app; a WhatsApp bot.
>
> **Decision.** A small, mobile-friendly web app with a “today’s orders” board. The spreadsheet got messy when two people edited it at once, and the bot needed more setup and approval than two weeks allowed.
>
> **AI’s role.** AI drafted the first layout, the database schema, and tests for order status changes. The tests showed that the generated status logic let a paid order go back to “new,” so I rewrote that part myself. I checked every database query for injection.
>
> **Results.** The owner used it for three weeks and stopped losing track of orders. Logging in on a shared phone was annoying, so next time I’d use a simple PIN.

Appendix A has a blank version to paste into your README.

### Slide 22 · Follow concepts, not every trend

> **On the slide:** Tools change fast; concepts last for years. Before chasing a new trend, ask three questions.

Tools sit on top of concepts. Web frameworks keep changing, but developers who understand HTTP, the DOM, and state management move between them easily. Container and cloud tools keep changing, but they rest on processes, networking, and isolation. AI tools will keep changing too, and the skills of giving clear context, evaluating output, and testing carry over to whatever comes next.

The same goes for AI itself. Product names come and go, while concepts such as how models are trained, what a context window is, how retrieval works, and how to evaluate a model’s output stay useful for years. If AI interests you, the mathematics underneath it (linear algebra, probability, and statistics) is one of the most durable investments you can make.

**Three questions before investing time in something new:**

1. **Does it solve a problem I actually have?** If not, bookmark it and move on.
2. **What concept is it built on?** Learn the concept, and this tool and the next one both become easy.
3. **Can I build something small with it this week?** A small hands-on trial teaches more than ten hype posts.

**A routine you can keep up:** choose one or two trusted sources, such as the release notes of tools you already use, a local developer community, or a newsletter you trust. Spend about 30 minutes a week, and try anything promising by building something small. Curiosity and the willingness to experiment matter more than keeping up with everything.

### Slide 23 · Your advantage now: time to experiment

> **On the slide:** Four kinds of projects: a study tool, a tool for a local UMKM, a campus helper, and a hackathon project. Right now, mistakes are cheap.

As a student you have things many professionals don’t: time, low stakes, and people around you with problems worth solving. A failed side project costs a few weekends and teaches a lot. Use that freedom.

- **A study tool.** Turn your course notes into quizzes or flashcards, and you learn the material and the technology at the same time. *The judgment part:* how will you check that generated questions and answers are actually correct?
- **A tool for a local UMKM.** Many small businesses near campus still manage orders, stock, and customer messages through chat and notebooks, and a simple tool can genuinely help. You’ll practice gathering requirements from someone who isn’t technical. *The judgment part:* what is the simplest thing that helps, and how will you protect customers’ personal data?
- **A campus helper.** Student organizations always have repetitive admin work: schedules, forms, announcements. A small automation, such as a bot that posts reminders, saves real hours. *The judgment part:* what happens if it fails on the day of an event?
- **A hackathon project.** Team up, pick a real problem, and ship a demo in a weekend. You’ll learn scoping, teamwork under pressure, and presenting.

Use AI to move faster, for example to draft the first UI, the database schema, or the tests. You make the product decisions.

### Slide 24 · Your 30-day starter plan

> **On the slide:** Explore, build, verify, share: one week each. By day 30 you have one real project, a README that shows your thinking, and the habit of checking AI’s work.

**Week 1: Explore.** Take code you wrote before, such as an old assignment, and ask an AI assistant to explain it, review it, and suggest improvements. Because you already understand the code, you can see where the AI is wrong. Note what it got right and what it got wrong; this calibrates how far to trust it.

**Week 2: Build.** Choose a small, real problem (slide 23 has ideas). Write your step 1 and 2 notes first: who it’s for, what “done” means, and the approach you chose. Build the smallest version that actually helps. Keep a simple log of what the AI suggested, what you kept, and why (Appendix A has a template).

**Week 3: Verify.** Write tests, including edge cases. Ask the AI for a bug and security review, then check each finding: some will be real and some won’t. Fix the real ones.

**Week 4: Share.** Publish the project on GitHub with a README based on the write-up template from slide 21. Ask a friend, a senior, or a lecturer for feedback, and make at least one improvement based on it.

Keep it small. A finished small project teaches more than an ambitious unfinished one.

---

## Closing: five things to remember

*Slides 25–26*

### Slide 25 · Five things to remember

The five takeaways map back to the three parts:

1. **Coding is one step of four.** Understanding, designing, and evaluating matter more than ever. *(Part 1)*
2. **Treat AI as a fast teammate.** Give it clear context, then verify what it gives you. *(Part 2)*
3. **Never submit code you can’t explain.** Read, run, check, and own it. *(Part 2)*
4. **Invest in fundamentals and people skills.** They make your use of AI valuable. *(Part 3)*
5. **Show your thinking, and keep learning.** Build things that help real people. *(Part 3)*

### Slide 26 · Back to the opening question

> *If AI can write code, what is a developer for?*
>
> **To solve the right problems, and to own the result. AI is a powerful tool for that job.**

Each phrase carries part of the talk:

- **“The right problems”** is steps 1 and 2: understanding users and designing something worth building. That is judgment work, and it stays with you.
- **“Own the result”** is step 4 and all of Part 2: verifying, never submitting code you can’t explain, and using AI responsibly.
- **“A powerful tool for that job”** is step 3, done faster and better with AI by someone who knows how to direct it and check it.

Compare this with the answer you wrote down at the start. What would you add?

---

## Appendix A: Toolkit

Templates and checklists from the talk, ready to copy.

### A1. Prompt template (slide 10)

```text
Context: I'm building [what] with [language/framework, version] for [who or why].
Problem: When I [do X], I get [result]. I expected [Y]. The code and full error are below.
Task: First explain the likely cause. Then suggest a minimal fix.
Limits: Keep [what must not change]. Don't [what to avoid].
Before you answer, ask me anything else you need to know.
```

### A2. Four checks before using AI output (slide 13)

- [ ] **Read:** I can explain every line, and nothing was added that I didn’t ask for.
- [ ] **Run:** It passes tests, including empty, very large, invalid, and boundary inputs.
- [ ] **Check:** There are no secrets in the code, user input is validated, and there are no slow loops over large data.
- [ ] **Own:** I could defend every part of it in a code review.

### A3. Project write-up template (slide 21)

```markdown
## Problem
Who has this problem, and why does it matter?

## Constraints
Time, data, budget, and technical limits.

## Options considered
1. ...
2. ...

## Decision
What I chose, and why.

## AI's role
What AI helped with, and how I verified it.

## Results
What worked, what didn't, and what I'd change next time.
```

### A4. AI usage log (slide 24, week 2)

| Date | What I asked | What AI suggested | What I kept | Why |
|---|---|---|---|---|
| Day 8 | A database schema for orders | Three tables, with order status as free text | Three tables, with status as a fixed list of values | Free text allowed typos like “pd” for “paid” |

### A5. 30-day plan (slide 24)

- [ ] **Week 1, Explore:** asked AI to explain and review code I wrote before, and noted where it was wrong
- [ ] **Week 2, Build:** picked a real problem, wrote down who it’s for and what “done” means, built the smallest useful version, and kept an AI log
- [ ] **Week 3, Verify:** wrote tests with edge cases, asked AI for a bug and security review, checked each finding, and fixed the real ones
- [ ] **Week 4, Share:** published on GitHub with a write-up README, got feedback from at least one person, and made one improvement

### A6. Disclosing AI use in coursework (slide 14)

Follow your lecturer’s rules first; this is only a format.

> I used [tool] to [explain X / suggest test cases / review my code for bugs]. I wrote [the solution / the final code] myself and verified it by [running the tests / tracing it by hand / comparing it with the lecture notes].

---

## Appendix B: Questions students often ask

Longer versions of the answers prepared for the Q&A.

**Will AI replace developers?**
The work is changing: less typing, more designing, reviewing, and deciding. People who use AI well and can judge its output are in a strong position. Entry-level work is changing too, because much of the simple, well-specified work that juniors used to learn on is now quick to generate. That makes fundamentals, and a portfolio that shows judgment, more important. Nobody can predict the job market precisely, so invest in what stays valuable either way: understanding problems, solid fundamentals, and the ability to learn quickly.

**Is using AI for assignments cheating?**
It depends on the rules for that assignment, so follow your lecturer’s policy, and ask when it’s unclear. Using AI as a tutor (explanations, hints, quizzes) helps you learn. Submitting AI-generated work as your own where that isn’t allowed is academic dishonesty. Either way, be open about how you used AI, and never submit code you can’t explain.

**Which AI tool should I learn?**
Any mainstream assistant is fine to start with, and many have free tiers or student programs. The products change quickly, but the skills transfer: giving clear context, breaking work into checkable steps, verifying output, and testing. Learn those with whatever tool you have, and switching later will be easy.

**Do I still need algorithms and data structures?**
Yes. They’re how you catch AI’s mistakes (slide 18 has three examples), and they still come up in technical interviews. They also shape how you think about performance and trade-offs, which no tool does for you.

**How do I get my first internship?**
One or two real projects with documented decisions (slides 20 and 21), an active GitHub, involvement in communities such as campus clubs, local developer meetups, or open source, and applying early, since many companies open internship applications months before the start date. Ask seniors who have interned where they applied and what the interviews were like. Referrals from people who have seen your work help a lot, which is another reason to build in public and join communities.

**I’m a beginner. Should I avoid AI until I’m good at programming?**
You don’t need to avoid it, but use it as a tutor rather than a ghostwriter. Follow the routine on slide 19: try first, ask for hints, and rebuild without AI. The rule of thumb is a good check: if AI disappeared tomorrow, could you still do this?

**How do I show AI skills on my CV?**
Not by listing tool names, which anyone can do. Show it through projects: the “AI’s role” section of your write-up, how you verified the output, and what you caught and fixed. That demonstrates the skill that matters, which is using AI to go faster without lowering quality.

**Should I specialize in AI or machine learning?**
If it genuinely interests you, go for it, but know that building products on top of AI models and training or improving the models themselves are different paths. Both rest on strong software engineering and data skills, and machine learning also needs linear algebra, probability, and statistics. Either way, the fundamentals in this talk are where you start.

---

## Appendix C: Glossary

| Term | Meaning |
|---|---|
| Acceptance criteria | Short statements that must be true for a piece of work to count as done. |
| Agent (coding agent) | An AI tool that works toward a goal in a loop: it plans, edits files, runs commands and tests, and adjusts based on the results. |
| Big-O notation | A way to describe how an algorithm’s running time or memory grows with the size of its input, such as O(n) or O(n²). |
| Boilerplate | Repetitive code that follows a standard pattern, such as setup code or basic create, read, update, and delete functions. |
| Code review | A teammate reading your changes before they’re merged, to catch problems and share knowledge. |
| Context | The information you give an AI tool so it can help: your goal, code, errors, and constraints. |
| Decision log | A short record of a project’s important decisions: what was decided, which options were considered, and why. |
| Edge case | An input or situation at the limits of what the code expects, such as empty, very large, or invalid input. |
| Hallucination | When AI produces something plausible but false, such as a function or package that doesn’t exist. |
| Knowledge cutoff | The date after which a model has no training data, so it may not know newer versions or events. |
| Large language model (LLM) | The kind of AI model behind most chat assistants and coding tools, trained on large amounts of text and code. |
| Parameterized query | A database query where user input is sent separately from the SQL, which prevents SQL injection. |
| Prompt | The instructions and information you give an AI tool. |
| Race condition | A bug that appears when two operations run at the same time and the result depends on their timing. |
| SQL injection | An attack where user input is treated as part of a SQL query, letting the attacker change what the query does. |
| UMKM | *Usaha Mikro, Kecil, dan Menengah*: micro, small, and medium enterprises in Indonesia. |
| Unit test | A small automated test that checks one piece of code, such as a single function. |
| UU PDP | Indonesia’s Personal Data Protection Law (Law No. 27 of 2022). |

---

## Appendix D: Further reading

- **[OWASP Top 10](https://owasp.org/www-project-top-ten/)**: the most common web application security risks, with examples and prevention advice.
- **[OWASP Top 10 for Large Language Model Applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/)**: the equivalent list for apps that use AI models.
- **[The Missing Semester of Your CS Education](https://missing.csail.mit.edu/)**: MIT’s free course on the shell, Git, debugging, and other tools most courses skip.
- **[Google Technical Writing courses](https://developers.google.com/tech-writing)**: short, free courses on clear technical writing, useful for READMEs and prompts alike.
- **[Architecture Decision Records](https://adr.github.io/)**: a simple, widely used format for documenting technical decisions.
- **[GitHub Student Developer Pack](https://education.github.com/pack)**: free developer tools and services for students.
- **[Good First Issue](https://goodfirstissue.dev/)**: beginner-friendly issues in open-source projects.
- *The Pragmatic Programmer* by David Thomas and Andrew Hunt: practical habits of effective developers.
- *A Philosophy of Software Design* by John Ousterhout: how to keep software simple as it grows.
- *Make It Stick: The Science of Successful Learning* by Peter C. Brown, Henry L. Roediger III, and Mark A. McDaniel: the research behind retrieval practice and desirable difficulties.
- **UU PDP** (*Undang-Undang Nomor 27 Tahun 2022 tentang Pelindungan Data Pribadi*): the full text is published in Indonesia’s official legal databases (JDIH).

---

## Appendix E: Notes for organizers and presenters

### How the talk covers the seminar objectives

| Objective from the seminar brief | Where it’s covered |
|---|---|
| 1. Insight into how the tech landscape and AI are changing software development | Slides 5–7, 22 |
| 2. Understanding AI’s role in learning, programming, and building digital products | Slides 9, 19, 23 |
| 3. The technical and non-technical skills that remain important | Slides 17, 18 |
| 4. Using AI effectively, critically, and responsibly | Slides 10–15 |
| 5. Problem solving, critical thinking, creativity, and adaptability | Slides 6, 7, 17, 22 |
| 6. Career preparation, portfolios, and the skills the tech industry needs | Slides 20, 21, 24 |
| 7. Continuous learning, and using AI to create useful work and digital solutions | Slides 22–25 |

### Timing plan

| Section | Slides | Minutes | Ends at |
|---|---|---|---|
| Opening | 1–3 | 4 | 0:04 |
| Part 1 · Change | 4–7 | 9 | 0:13 |
| Part 2 · Work | 8–15 | 15 | 0:28 |
| Part 3 · Grow | 16–24 | 16 | 0:44 |
| Takeaways | 25 | 1 | 0:45 |
| Answer and Q&A | 26 | 15 | 1:00 |

The speaker notes include checkpoints at minutes 13, 28, and 44. If you’re running late, cut slides 22 and 23 to a minute each and skip the optional poll on slide 2. Protect the time for slide 6 (the core idea) and slide 12 (the one rule).

### Before the talk

- Fill in the two speaker-note placeholders: a personal example of how your own work has changed (slide 5), and local communities, incubators, or competitions worth mentioning (slide 23).
- Export a PDF of the deck as a backup in case the venue’s internet is unreliable.
