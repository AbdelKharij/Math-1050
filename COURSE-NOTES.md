# Math 1050 (ISU) — conversion notes

Source: `MATH_1050(1).zip`, `FA2025/` only (HW1–HW10, Exam 1, Exam 3, Practice Exam 3,
Practice Final, Final). Original documents are print worksheets by Dr. Kirin J Martin,
Iowa State University.

**Not to be confused with `~/Documents/work/Math1050`**, which is a different MATH 1050
(chapter-based college algebra, published at `AbdelKharij/Math1050`). That repo was
left untouched; this course is Iowa State's "Introduction to Mathematical Ideas" —
voting theory, weighted voting, fair division, and apportionment.

Every problem with a determinate answer was converted to an interactive Ximera answer
(`\answer`, `\multipleChoice`, `\selectAll`); open-ended parts use `\freeResponse` with
a worked solution. All tabulations (Borda counts, elimination rounds, pairwise
comparisons, Banzhaf and Shapley-Shubik distributions, sealed bids, markers, and all
five apportionment methods) were computed programmatically and cross-checked by hand.

## Gaps and errors in the original materials

1. **There is no Exam 2.** `FA2025/Exams/Exam2.tex` is an empty file — one blank line,
   no content at all. The course therefore has no Exam 2 activity. If an Exam 2 exists
   elsewhere, it can be added as a new part in `math1050.tex`.

2. **HW8, Problem 4 (method of markers).** Caleb's row reads `32--40` and `40--51`, so
   **item 40 appears in two of his shares**. It is read here as `41--51`. This does not
   change the outcome: Caleb is awarded on his *first* marker (item 5), so his later
   markers never come into play.

3. **HW8 problem numbering** jumps from "Problem 2" to "Problem 4" — there is no
   Problem 3 in the source. The activity numbers them sequentially.

4. **Exam 3 source has dead content.** A duplicate of the sealed-bids chores problem
   appears *after* `\end{document}` and never renders. The version before
   `\end{document}` was used.

5. **`WIP FinalExam.tex`** is flagged work-in-progress in its own filename. It reads as
   complete (seven problems, all answerable) and was converted as `exams/finalExam.tex`,
   but it may not be the final version the instructor gave.

## Judgment calls worth confirming

6. **Exam 3, Problem 5(d)** asks "What is one fair division of the sundae?" — but with
   the shares as cut, both Jake and Joel bid only on `s_1`, which is a standoff. The
   solution explains the standoff and gives the standard resolution (Adam takes `s_2`,
   then Jake and Joel divider-chooser the rest). If the intended answer was a
   straightforward assignment, the value systems need re-checking.

7. **Exam 3 / Practice Exam 3, "every player above fair share."** Sealed Bids and
   Method of Markers are marked correct; Lone-Divider and Lone-Chooser are not, because
   the first divider always ends at exactly `1/N`. The solutions spell out that
   reasoning.

8. **HW7, Problem 5(c)**, "which division is most equitable?" is a matter of judgment.
   The solution names the division with the most even spread of perceived values, and
   notes which one instead maximizes the total.

## Deliberate omissions

- Exam front matter (name lines, device policy, point totals) is print-specific.
- The syllabus and schedule were excluded by request.
- **HW8, Problem 4** originally displayed 60 beanie baby photographs (filenames like
  `Screenshot 2024-11-03 at 3.16.26 AM.png`, which are hostile to `\includegraphics`).
  The photos carry no information needed to solve the problem — only the numbered
  positions 1–60 matter — so the array is presented numerically instead.
- **Practice Exam 3, Problem 4** used `roastbeef.png`, `veggie.png`, and `ruler.png` as
  full-page background images via `\AddToShipoutPicture`. These are decorative; the
  sandwich is described in text.

## Figures

Copied to `xmPictures/`, renamed where the original name was awkward:

| original | here |
| --- | --- |
| `FA2024/Homework/LuckyLuke.jpg` | `LuckyLuke.jpg` |
| `FA2024/Homework/sandwich.jpg` | `sandwich.jpg` |
| `SP2025/Exam3/Candies.jpg` | `candies.jpg` |
| `FA2024/Exam3/MarkersImage.png` | `markersArray.png` |

Marker positions were read off `candies.jpg` and `markersArray.png` directly, since the
values appear only in the images:

- **candies.jpg** (21 items, 4 players): A at 4, 9, 17 · B at 5, 11, 16 ·
  C at 6, 10, 15 · D at 6, 12, 16. Note `B₃` and `D₃` share a single arrow at 16, which
  forces a tiebreak and leaves *no* surplus — an unusual outcome worth flagging to
  students.
- **markersArray.png** (13 items, 3 players): A at 4, 9 · B at 3, 8 · C at 4, 7.
  Surplus is items 8 and 9.

## Build

Verified locally with `lualatex` against the class files in `.ximera_local` — all 15
activities and the `math1050.tex` xourse compile without errors (97pp).

Publishing uses the GitHub Actions workflow in `.github/workflows/serve-ximera.yml`.
Note that `XM_COMPILE_SEQUENCE` is set in `xmScripts/config.txt`, not as a workflow
`env:` — `xmlatex` only forwards six environment variables into the container, so a
workflow-level setting is silently ignored.
