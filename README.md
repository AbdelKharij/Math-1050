# Introduction to Mathematical Ideas

An interactive online version of this course, built with
[Ximera](https://ximera.osu.edu/). Students read the page, type answers into the
problems, and get immediate feedback with a full worked solution.

**Live site:** <https://xerxes.ximera.org/abdelkharij-math-1050/mathematicalIdeas>

Topics: voting theory and the fairness criteria, weighted voting and the Banzhaf and
Shapley-Shubik power indices, fair division, apportionment and its paradoxes, and game
theory.

## What is in it

Each semester is its own section of the course, and the older exams are collected in a
final section:

| section | folder | activities |
| --- | --- | --- |
| Fall 2024 | `fa2024/` | 15 |
| Spring 2025 | `sp2025/` | 17 |
| Fall 2025 | `fa2025/` | 15 |
| Spring 2026 | `sp2026/` | 12 |
| Previous Exams | `archive/` | 19 |

78 activities in all, holding 369 problems: 2570 answer blanks, 374 multiple-choice and
70 select-all questions, 33 open-ended questions, 1021 worked solutions, and 185 hints.

**Previous Exams** holds exams and review sheets from earlier years, converted the same
way: six Exam 1s, two Exam 2s, three Exam 3s and a review, a non-cumulative Exam 4, five
finals, and a final review. Several of those had no answer key at all, so the answers
there were worked out and checked independently.

Students can work any section; nothing is hidden or locked. A worked solution stays
hidden until the student clicks **Check work**.

## Using it with a class

Send students the live link above. There is no enrollment, login, or grade book —
Ximera records progress in the student's own browser, so this works as practice and
review material rather than as something to collect.

**The real exams are included and are publicly visible.** That was a deliberate choice.
If you ever want a problem taken off the public site, delete or comment out its
`\activity{...}` line in `mathematicalIdeas.tex` and push.

## Editing

- One activity = one `.tex` file. Edit it like any LaTeX document.
- `mathematicalIdeas.tex` is the table of contents. `\part{...}` starts a section and
  `\activity{folder/file.tex}` adds an activity in order.
- To add a semester, make a folder, put the `.tex` files in it, and add a new `\part`
  with its `\activity` lines.
- Add shared macros to `xmPreamble.tex`, not to individual activities. Activities must
  **not** `\input` the preamble; Ximera loads it automatically. This course defines
  `\set`, `\seq`, and `\ballotcol` there.
- Pictures live in `xmPictures/` and are referenced by filename alone.
- A feedback that refers to "Homework N" means that semester's numbering, which differs
  between terms — check the reference if you move an activity.

Every push to `main` rebuilds and republishes the site automatically (a few minutes).
You can watch it under the repository's **Actions** tab. If a publish ever fails at the
last step with a `502` from the server, just re-run the failed job.

## Notes on the conversion

`COURSE-NOTES.md` records everything worth knowing: which source material was left out
and why, about twenty errors found in the original worksheets, exams, and answer keys
(the online version uses the corrected values), and a few judgment calls that are worth
your review.

The course is written to be institution-neutral, so it carries no university name,
course number, instructor name, or local references, and can be used by anyone.
