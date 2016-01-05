# Example conflict project

Git project to show how a conflict works.

* Branch graph: https://github.com/nmaletm/example-conflict/network
* Commits: https://github.com/nmaletm/example-conflict/commits/master

## Steps to reproduce it

You can follow this steps to reproduce this project:

```
$ git init

$ vi book.txt # Set the initial text of the file

$ git add book.txt
$ git commit -m "Initial commit"

$ git checkout -b title-branch

$ vi book.txt # Introduce one change (for the example the title)

$ git add book.txt
$ git commit -m "Set the title"

$ git checkout master

$ vi book.txt # Introduce another change (for the example the first sentence)

$ git commit -m "Set the first sentence"

$ git merge title-branch

$ vi book.txt # Solve the merge conflict
$ git commit # To mark as solved

```