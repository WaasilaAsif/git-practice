# Git Practice 

A safe sandbox for your **first pull request**. Nothing here is real code, so you can't break anything. Fork it, make a change, open a PR, get it merged. That's the whole open source workflow, and once you've done it once it stops being scary.

Used in the GDGoC **Git & GitHub** workshop (module 00 of [Learn Your Own X](https://github.com/WaasilaAsif/learn-your-own-x)).

---

## Do this

Follow the workshop checkpoints, or these steps on your own:

1. **Fork** this repo (button, top right).
2. **Clone your fork:**
   ```bash
   git clone https://github.com/<your-username>/git-practice.git
   cd git-practice
   ```
3. **Branch:**
   ```bash
   git switch -c add-<your-username>
   ```
4. **Add yourself:** create `contributors/<your-username>.md`. Copy the format from [contributors/README.md](contributors/README.md).
5. **Commit:**
   ```bash
   git add contributors/<your-username>.md
   git commit -m "Add <your-username> to contributors"
   ```
6. **Push:**
   ```bash
   git push -u origin add-<your-username>
   ```
7. **Open a pull request** from your branch to this repo's `main`. Fill in the template.
8. **Respond to review:** a maintainer leaves a comment. Make the fix on the same branch, commit, push. The PR updates itself.

When it's merged, your file is on `main` and your name is on the contributors wall. 🎉

## Why one file each?

So 50 people don't all edit the same line and fight merge conflicts. One file per person means every PR is independent. (Want to *see* a conflict on purpose? That's the bonus round below.)

## Bonus round: cause a merge conflict 💥

Pair up. Both of you add a line to the **same spot** in [guestbook.md](guestbook.md) on separate branches, and both open PRs. Whoever merges second gets a conflict. Resolve it locally:

```bash
git switch main
git pull upstream main        # get the other person's merged change
git switch add-<your-username>
git merge main                # conflict appears here
# edit guestbook.md, delete the <<<< ==== >>>> markers, keep both lines
git add guestbook.md
git commit
git push
```

Merge conflicts look terrifying until you've fixed one. Now you have.

## This is a sandbox

It gets reset every semester. Your real "first contribution that counts" is adding yourself to the [Learn Your Own X](https://github.com/WaasilaAsif/Learn-your-own-x) repo after you finish a module.

## Contributors wall

Everyone who's merged a PR here. Your face shows up automatically once your PR lands. 👇

[![Contributors](https://contrib.rocks/image?repo=WaasilaAsif/git-practice)](https://github.com/WaasilaAsif/git-practice/graphs/contributors)