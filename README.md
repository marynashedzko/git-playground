# Playground repostory

This file documents the Git commands used to practice rewriting history with this toy repository.

---

## Repository Setup

```bash
git init
```
> Initializes a new Git repository.

```bash
git add .
```
> Stages all files in the directory for commit.

```bash
git commit -m "first commit"
```
> Creates first commit.

---

## Adding Quote Files

```bash
echo "Some of you may die, but it's a sacrifice I am willing to make." > shrekquote1.txt
git add .
git commit -m "feat: add shrek quote"
```
> Adds a new quote from Lord Farquaad to `shrekquote1.txt` and commits it.

```bash
echo "WHAT are you doing in my swamp!?" > shrekquote2.txt
git add .
git commit -m "feat: add shrek quote 2"
```
> Adds Shrek's quote to `shrekquote2.txt` and commits it.

```bash
echo "Not the gumdrop buttons!" > shrekquote3.txt
git add .
git commit -m "feat: add shrek quote 3"
```
> Adds Gingy's quote to `shrekquote3.txt` and commits it.

---

## Amending a Commit

```bash
git commit --amend -m "feat(shrekquotes): add shrek quote by gingy"
```
> Changes the message of the most recent commit (about `shrekquote3.txt`) to a more descriptive message.

---

## Viewing the Commit Log

```bash
git log
```
> Displays the list of recent commits (4 total at this point).

---

## Rewriting History with Interactive Rebase

```bash
git -c core.editor=notepad.exe rebase -i HEAD~3
```
> Rewrites the last 3 commits interactively:
- **changed commit messages** to give better descriptions:
  - `"feat (shrekquotes): add shrek quote by lord F"`
  - `"feat(shrekquotes): add shrek quote 2 by shrek"`

---