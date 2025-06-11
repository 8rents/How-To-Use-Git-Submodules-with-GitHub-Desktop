# How To Use Git Submodules with GitHub Desktop

> *A quick guide to using git submodules with GitHub Desktop*

---

In Git a submodule is a separate git repository that is added to another git repository as a dependency.

This guide will cover:

1. Adding an existing repository as a submodule
2. Pulling and cloning submodules
3. Updating repositories added as a submodule

## Adding an Existing Repository as a Submodule

Submodules are handled through a file in the root of the main repository called `.gitmodules`. 

First clone a repository into your existing one into your desired location.

### The `.gitmodules` file

If there are no submodules in your repository already first create a new file called `.gitmodules` or if the file already exists open it.

Each submodule needs to include the following lines:

1. Submodule declaration
2. The path within the parent repo
3. The remote URL

The following code snippet will register a submodule called `sm1` from the URL `https://github.com/example-user/submodule-example1` into the folder called `sm1folder`. 

```
[submodule "sm1"]
 path = sm1folder
 url = https://github.com/example-user/submodule-example1
```

- The first line with the brackets `[submodule]` declares the submodule.
- The second line `path` says where the submodule will be cloned to in the future
- The third line `url` says where the submodule will be cloned from.

Note that you can call the submodule something different that what it is called in the remote repo. You can also place different submodules in different locations. 

To add another submodule add another declaration line:

```
[submodule "sm1"]
 path = sm1folder
 url = https://github.com/example-user/submodule-example1
[submodule "submod2"]
 path = folder-for-sm2
 url = https://github.com/example-user/submodule2-example
```

You can add as many submodules as you like this way. Make sure to clone and commit them after adding these lines to the file.

## Pulling and Cloning Submodules

Fortunately GitHub Desktop makes it pretty easy to 

## Updating Submodules from a Parent Repository



## Sources

- [Atlassian Guide to Git Submodules](https://www.atlassian.com/git/tutorials/git-submodule)
