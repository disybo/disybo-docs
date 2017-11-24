 # Commit and Workflow Suggestions

The [git book](https://git-scm.com/book/en/v2) is a good overview and starting point. This document contains brief summaries of useful workflows.

## Feature Development
For larger features, it's a good idea to separate their commit history into a separate branch until the feature is fully developed and tested. When it is, it's "safe" to merge back into the main branch so that others can get a clean and functional version of the feature.

1. Create a new (local) branch
    ```bash
    git checkout -b <name-of-feature-branch>
    ```
1. Work on the feature, committing changes as you see fit
    ```bash
    git commit -m "Implement feature X and tests"
    ```
1. When fully implemented, merge it back into your _local_ master branch
    ```bash
    git checkout master
    git merge <name-of-feature-branch>
    ```
1. Resolve any merge conflicts locally and re-run all tests
1.  Update local master with origin
    ```bash
    git fetch
    git pull --rebase
    git push
    ```