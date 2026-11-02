# Midnight Grader

A CS193 project to help students check multiple-choice practice quizzes without comparing every answer manually.

## Status

Planning stage. This repository currently contains the project plan, feature matrix, test checklist, and synthetic example files. There is no Java implementation to compile or run yet. The student-drawn system diagram is still pending.

## MVP scope

- Load an answer key and one student's answers from CSV files.
- Match questions, calculate the score, and identify missed or unanswered questions.
- Display results in the terminal and export a CSV report.

Every question is worth one point. Blank or missing answers count as incorrect. Questions are matched by number, so row order does not matter. Missing files and malformed input should produce useful error messages.

## Tech stack

- Java, using the JDK used in CS180
- Java standard library: file I/O, Scanner, and number formatting
- Local CSV storage; no database, external dependency, account, or API required
- IntelliJ, Git, and GitHub

Check the installed Java version with `java -version` and `javac -version`. Compile/run instructions will be added alongside the Java implementation.

## Input format

Answer key and student-answer files use two columns:

```csv
question,answer
1,B
2,A
3,D
```

See [sample answer key](examples/answer-key.csv) and [sample answers](examples/student-answers.csv). All example data is synthetic. The normal sample should score 3/4 (75%), with question 2 incorrect. The missing-answer sample should also score 3/4, with question 3 unanswered.

## Project files

- `src/` - future Java implementation
- `tests/` - future automated tests
- `examples/` - synthetic quiz CSV files
- `output/` - generated reports (ignored by Git)
- [Design document](docs/design.md)
- [Eisenhower Matrix (PDF)](docs/eisenhower-matrix.pdf) · [Markdown version](docs/eisenhower-matrix.md)
- [Manual test checklist](docs/test-plan.md)
- [Homework Google Doc](https://docs.google.com/document/d/1RyccEZwJ1W4BKwszNWhDETVaH8-iuPGLJmULnyaFADA/edit)

## Roadmap

- [x] Define the problem and MVP; create the repository and planning files
- [ ] Read and validate the answer key
- [ ] Read and validate student answers
- [ ] Compare answers and calculate scores
- [ ] Display per-question results
- [ ] Export CSV reports
- [ ] Test edge cases and finish setup documentation
- [ ] Draw and commit the system diagram and editable source
- [ ] Schedule feature: grade multiple quizzes in one run, developed on a feature branch
- [ ] Future: questions worth different points
- [ ] Future: results from previous attempts

## Outside this project

Handwriting recognition, AI essay grading, user accounts, and cloud syncing are outside the planned scope.
