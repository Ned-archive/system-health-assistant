# Internal Notes — System Health Assistant

⚠️ This file is for personal thinking, questions, and planning.
Not meant for users or recruiters.

---

## 1. Open Questions
Questions I don’t know the answer to yet.

- How often should system metrics be sampled?
- What counts as “normal” vs “problematic” for an elderly user?
- How much explanation is too much before it becomes overwhelming?

---

## 2. Feature Ideas (Unfiltered)
Ideas go here before deciding if they are good or bad.

- Battery health (for laptops)
- Simple “health score” instead of raw percentages
- System uptime (how long the computer has been running, can suggest a restart if very long)
- Temperature sensors (CPU/GPU temps, if available)
- Provide the contact information of a person or a company that can help resolve the issue the app finds. 

---

## 3. Risks & Concerns
Things that could break trust, safety, or usability.

- False positives causing unnecessary anxiety
- Performance impact on very old machines
- Over-explaining simple issues

---

## 4. Design Thoughts (Messy Allowed)
Half-formed ideas, sketches, and reasoning.

- Quick Scan = simple and non-overwhelming
- Modular = gives control without clutter
- Full Report = shows technical depth for portfolio/interview
- Might need different explanation levels (short vs detailed)
- Interactive fixes = provide guidance/instructions, never automate, keeps read-only guarantee intact.
---

## 5. Decisions To Make Later
Important choices that require experimentation or research.

- CLI vs simple GUI
- How to store system snapshots (if at all)
- Whether to support Windows-only first

---

## 6. Things I Learned While Building
Notes added over time.

- At first, I printed messages directly when something was wrong (like storage being too full). That works, but it mixes checking the problem with showing the message.
I learned it’s better to let the program check first and return a result, and then decide later how to show it
(print it, show it in a window, or hide it). This makes the code easier to reuse, change, and grow without rewriting everything.
- 
- 

---

## 7. Ideas I Explicitly Rejected (and Why)
Prevents going in circles later.

- Automatic fixes — too risky for target users
- Complex dashboards — defeats the purpose
