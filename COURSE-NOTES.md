# Introduction to Mathematical Ideas — conversion notes

This course covers voting theory, weighted voting and power, fair division, apportionment,
and game theory. It is institution-neutral and meant to be usable by any university.

The source was a set of printed worksheets and exams from four semesters plus an archive of
earlier exams. Each semester is one section (`\part`) of the xourse, and the archive is a
fifth section, **Previous Exams**:

| section | folder | activities |
| --- | --- | --- |
| Fall 2024 | `fa2024/` | 15: HW 2–9, Practice Exams 1–2, Exam 1 Review, Exams 1–3, Final |
| Spring 2025 | `sp2025/` | 17: HW 1–10, Practice Exams 1–3, Exams 1–3, Final |
| Fall 2025 | `fa2025/` | 15: HW 1–10, Practice Exam 3, Exams 1 and 3, Practice Final, Final |
| Spring 2026 | `sp2026/` | 12: HW 5–9, Practice Exams 1–3, Exams 2–3, Practice Final, Final |
| Previous Exams | `archive/` | 19: Exams 1–4, finals, and review sheets from earlier years |

Every problem with a definite answer is interactive (`\answer`, `\multipleChoice`,
`\selectAll`). Open-ended parts use `\freeResponse` with a model answer. Worked solutions
are in `feedback` environments, which stay hidden until the student checks their work.
All of the calculations were redone independently by script and checked against the
source keys: Borda counts, elimination rounds, pairwise tables, Banzhaf and
Shapley-Shubik power, sealed bids, markers, all five apportionment methods, and game
values. Where the two disagreed, the corrected value is used and listed below.

## What was left out

- **Syllabi, calendars, and schedules**, as requested. The same goes for anything that
  identifies an institution, course number, instructor, or local place. Local references
  in problems were replaced by generic ones (e.g. "a botanical garden", "a university",
  "a famous singer"), and one anecdote about the author was reworded in the third person.
- **Large-print (accommodation) exam copies.** Their questions match the regular exams,
  and one of them names a student.
- **Fall 2024 Practice Exam 3**: an unfinished draft. Problems 3–5 are placeholder text,
  and 1–2 repeat Exam 2.
- **Fall 2025 Exam 2**: the source file is empty.
- **A calculus test** (limits and derivatives) that was filed with the Exam 1 archive and
  belongs to a different course.
- **Duplicates in the archive**: the 2022 and 2023 Exam 3 reviews are nearly identical, as
  are the two final reviews, so each pair became one activity. The 2021 Exam 4 repeats 2020
  except for two wording changes. The two 2023 Exam 1 versions differ only in their
  true/false items, so they were merged. A fragment left after `\end{document}` in the
  2020 Exam 4 source (an unfinished older Exam 2) was ignored.
- Print-only front matter: name lines, device policies, and point totals.

## Errors in the source, and how they were resolved

Semester materials:

1. **Spring 2025 Exam 2**: a choice reads $2^8-8-1=248$. It is $247$, which is used here.
2. **Fall 2024 HW4 solution key**: the Banzhaf distribution in Problem 2 is miscalculated.
   The correct $(\frac12,\frac16,\frac16,\frac16)$ matches the Fall 2025 version.
3. **Fall 2024 Final**: in the finger game, parts (c) and (d) both ask for the
   proportion of *one* finger. Part (d) is read as *two* fingers.
4. **Fall 2025 HW8 (markers)**: one player's shares read `32--40` and `40--51`, so item 40 appears
   twice. It is read as `41--51`, which does not change the outcome.
5. **Fall 2025 HW8 numbering** skips Problem 3. The activity numbers problems sequentially.
6. **Fall 2025 Exam 3 source** repeats the sealed-bids chores problem after `\end{document}`. The
   version before it was used.
7. **Fall 2024 Exam 1 Review, Problem 6(a)**: Butterscotch has $88$ modified-Borda points,
   not $94$. It still wins.

Previous exams:

8. **2022 Exam 2**, divider-chooser: the key values Charli's land at \$80K instead of
   \$120K. The correct values are $s_1=172$K and $s_2=108$K. Charli still picks $s_1$.
9. **2023 Exam 2**: the gridlock check for $[18:7,4,2,1]$ compares with $15$; the total
   weight is $14$. The other figures are correct.
10. **2022 Exam 3**, Jefferson: the key's sum for $d=280$ starts with $12$ where it should
    be $13$. The conclusion is unchanged.
11. **2023 Exam 3 review**: one allocation sentence gives "$s_3$ to D" twice. There are $5$
    fair allocations. The estate-sale surplus is $\$166.67$, or $\$55.56$ each; the key
    has $166.66$ and $55.55$.
12. **Fall 2023 final, Hamilton**: the lower quota for the first college is $9$, not $6$.
    The correct apportionment is $9,15,8,4,7,7$; the key's version totals only $47$.
13. **Fall 2023 final, Shapley-Shubik**: in $[11:6,5,4,3]$ the pivotal counts are
    $8,8,4,4$. The exam gives C a count of $6$. The activity uses $4$ and says so.
14. **Fall 2022 final, Shapley-Shubik**: in $[10:6,5,4,1]$ the counts are $10,6,6,2$. The
    exam gives C $4$. The activity uses $6$, so A's index is $\frac5{12}$.
15. **Fall 2022 final, Hamilton**: the key's table has a mismatched population row. The
    final apportionment $7,15,8,4,7,9$ is correct.
16. **Final review**: in the $3\times4$ game, column 1 does not dominate column 4 in the
    full matrix, because of the $-8$. It dominates only after A's dominated row is removed,
    and the question is reworded that way. The saddle point is row 3, column 1, value 5.
17. **Final review, clothing problem**: the key uses a jacket-in-sun payoff of $0$ and a
    60/40 forecast, but the problem states $1$ and 50/50. With the stated data, the
    coin-flip payoff is $0.75$ (the key has $0.3$).

## Judgment calls worth confirming

- **Fall 2024 HW6(c)**: "\$205 in gold coins, tobacco, and bourbon" is treated as a
  *combination* of discrete (coins) and continuous (tobacco, bourbon) assets.
- **Exam 3, "every player above a fair share"**: Sealed Bids and Markers are marked
  correct. Lone-Divider and Lone-Chooser are not, because the first divider always ends
  at exactly $\frac1N$.
- **2023 Exam 3, candy markers**: the original asks students to choose their own markers.
  The activity fixes one valid set so the allocation can be graded, and breaks the tie
  for the first share by coin flip.
- **2020 Exam 3 take-home**: to resolve the standoff, Jared takes $s_3$, and the rest is
  shared by divider-chooser. Taking $s_2$ is equally valid.
- **HW7, "most equitable division"** is a matter of judgment. The feedback names the most
  even division and notes which one maximizes the total.

## Figures

In `xmPictures/`: `LuckyLuke.jpg`, `sandwich.jpg`, `candies.jpg`, `markersArray.png`, and
`cakeShares.png` (the cake-cutting solution sketch). Pizza, sub, and cake diagrams whose
images were missing from the source are drawn in TikZ. Marker positions come from the
images: `candies.jpg` has A at 4, 9, 17; B at 5, 11, 16; C at 6, 10, 15; D at 6, 12, 16.
`markersArray.png` has A at 4, 9; B at 3, 8; C at 4, 7.

## Build

Every activity compiles with `lualatex` against the class files. `xmPreamble.tex` is loaded
automatically by `ximera.cls`, so activities must not `\input` it. Publishing uses the
GitHub Actions workflow in `.github/workflows/serve-ximera.yml`. `XM_COMPILE_SEQUENCE`
belongs in `xmScripts/config.txt`, because a workflow-level `env:` is silently ignored.
