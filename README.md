# Stacked-PRs Demo

This repository is used to demonstrate how to build stacked-PRs, and how to manage them.

## References

- What are stacked-PRs: https://graphite.com/blog/stacked-prs
- How to rebase them: https://medium.com/@bruce.ho98/a-better-way-to-rebase-stacked-prs-aa9b4dc600f1
- Official `git rebase` documentation: https://git-scm.com/docs/git-rebase
- Git 2.38 release notes with new `--update-refs` option: https://github.blog/open-source/git/highlights-from-git-2-38/#rebase-dependent-branches-with-update-refs

## Cheat sheet

- Refresh distant reference branch status:

  ```sh
  git fetch origin develop:develop
  ```

- Rebase all local branches at once (from the top-most branch):

  ```sh
  git rebase -i --update-refs develop
  ```

- Rebase all local branches at once, including fixup commits on arbitrary branches (from the top-most branch):

  ```sh
  git rebase -i --update-refs --autosquash develop
  ```

  - make a fixup/squash commit

    ```sh
    git commit --fixup|--squash <commit ID>
    ```

- Rebase all local branches, as well as the feature branch, if any (from the top-most branch):

  ```sh
  git rebase -i --update-refs --autosquash --rebase-merges develop
  ```

  Option `--rebase-merges` is used to [preserve merge commits](https://git-scm.com/docs/git-rebase#_rebasing_merges) of already-merged PRs on the feature branch.

- Push all local branches at once:

  ```sh
  git push  --force-with-lease --force-if-includes origin <list of updated branches…>
  ```

  (list of updated branches returned by the `git rebase --update-refs` commands above)
