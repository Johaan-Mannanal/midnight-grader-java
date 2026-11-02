# Midnight Grader - CS193 Homework 9 Design Document

Johaan Joseph Mannanal | November 1, 2026

## 1.1 Problem statement

I want to help students check their practice quizzes without having to compare every answer manually.

## 1.2 Idea / solution

Midnight Grader will be a Java terminal program that compares a student's multiple-choice answers with an answer key. It will show their score, identify missed questions, and save the results.

## 2.1 Eisenhower Matrix and MVP

My [feature matrix](eisenhower-matrix.md) separates what I need for the first version from what I can add later. For the first version, I’ll load two CSV files, grade one quiz, and show and save the results.

### Basic grading rules

- Each question is worth one point.
- A blank or missing answer counts as incorrect and is reported as unanswered.
- Match answers by question number, not by row order.
- Report missing files or malformed input clearly.

## 2.2 Tech stack

I’ll write the program in Java using IntelliJ and track changes with Git and GitHub. I’ll use Java’s standard library to read and write CSV files, take input in the terminal, and format the score. I’ll make my own sample quiz files.

### Input format

Both input files use the header `question,answer`, followed by question-number and answer pairs. Student answers can be blank. Examples are in `examples/`.

## 2.3 Chunked build plan

1. Create the repository, folder structure, README, and sample input files.
2. Read an answer-key file and check that its entries are valid.
3. Read a student-answer file and handle missing or invalid input.
4. Match questions and calculate correct, incorrect, and unanswered totals.
5. Display the score and results for each question.
6. Export the results to a CSV file.
7. Test edge cases and finish the setup instructions.
8. On a separate branch, add grading for multiple student files, test it, and merge it.

I’ll test and commit each step before starting the next one.

## 2.4 System diagram

![Midnight Grader checks the input files, grades each answer, displays missed questions, and saves the results to a CSV file.](system-diagram.png)

[Editable diagram](system-diagram.drawio)

## 3.1 GitHub repository and README

Public repository: https://github.com/Johaan-Mannanal/midnight-grader-java

Homework Google Doc: https://docs.google.com/document/d/1RyccEZwJ1W4BKwszNWhDETVaH8-iuPGLJmULnyaFADA/edit
