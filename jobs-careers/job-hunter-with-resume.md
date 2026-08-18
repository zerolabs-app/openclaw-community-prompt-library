# Job Hunter with Resume

Purpose

Find job openings matching the criteria specified by the user, then draft a tailored version of the user's resume for each matching job.

User Inputs

- Job Titles or Keywords: [USER INPUT]
- Location or Remote Preference: [USER INPUT]
- Years of Experience: [USER INPUT]

Base Resume

Paste your full resume text below. Include your work history, skills, and any certifications — this is what each tailored version will be built from.

[USER INPUT]

Search Sources

- LinkedIn Jobs
- Indeed
- Company career pages
- Other publicly accessible job board listings

Blocked Source Fallback Rule

If a source:

- blocks automated access
- requires sign-in
- fails to render
- returns unusable pages

then:

- Record the blocked source.
- Record the reason.
- Continue searching other sources.
- Do not stop searching because a source is unavailable.

For Each Matching Job Found

1. Confirm the job matches the title, location, and salary criteria.
2. Compare the job description against the user's base resume.
3. Identify the 3-5 most relevant skills/experiences to highlight for this specific job.
4. Draft a tailored version of the resume: reorder or reword bullet points to match the job description's language. Every skill, keyword, and claim in the tailored version must trace back to something explicitly stated in the base resume — do not add skills, tools, certifications, or qualities (e.g. "customer service," "project coordination," "quality assurance") that are not already present in the base resume, even if they seem like a natural fit for the role.
5. Keep formatting simple and ATS-friendly (plain text or simple structure, no complex tables/graphics).

Required Output Per Job

- Job title and company
- Direct link to the job posting
- Tailored resume (as text, ready to copy or attach)
- 1-2 sentence note on why this job is a good match


Application Rule

- Do not submit applications automatically. The user reviews and applies manually via the job posting link.
- If run as a recurring task, only include jobs not already reported in a previous run.

Priorities

- Real, currently open postings only — no expired or closed listings
- Closer keyword/title matches over loose matches
- Postings with a clear, direct application link
- Jobs matching minimum salary when salary is listed

Notes

- The tailored resume should stay accurate to the user's real experience — it reorganizes and rewords, it does not fabricate.
- Recommend the user does a final read-through before submitting, same as they would with any resume.


