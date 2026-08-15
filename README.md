# git-demo-basics

A practice repository for learning the basics of Git and GitHub. The files here
are throwaway placeholders — the point is the workflow, not the content.

## What's in here

| File | Purpose |
|------|---------|
| `index.html` | Landing page ("Hello, Git!") |
| `about.html` | About page, added via PR #1 |
| `contacts.html` | Contact page, added via PR #3 |
| `hello.txt` | Edited both locally and on GitHub, to practice pulling remote changes |
| `demo.txt` | Added via PR #2 from a feature branch |
| `.gitignore` | Ignores `.env` |

Plain static HTML — no build step, no dependencies. Open any `.html` file in a
browser to view it.

## Git concepts practiced

- `git init`, `git add`, `git commit`, `git push`
- Feature branches (`feature/add-new-html-file`, `feature/added-new-text-file`,
  `feature/contribute-new-feature`)
- Pull requests and merge commits
- Pulling changes made directly on GitHub back into the local `main`
- Forking and contributing upstream — this clone has two remotes:

  ```
  origin    https://github.com/krtcrvy/git-demo-basics.git              (fork)
  upstream  https://github.com/kurtcarveycadenas1401/git-demo-basics.git
  ```

- Ignoring files with `.gitignore`

## Typical workflow used here

```bash
git switch -c feature/my-change   # branch off main
# ...edit files...
git add .
git commit -m "added my change"
git push -u origin feature/my-change
# open a pull request on GitHub, merge it
git switch main
git pull                          # bring the merge back down
```

Keeping the fork in sync with upstream:

```bash
git fetch upstream
git merge upstream/main
git push
```
