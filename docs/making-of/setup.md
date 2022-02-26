# Feature: Project Setup

Goal: Project setup is ready to begin.


## Details

- [x] [Git repository on Github](#git-repository-on-github)
- [x] [Making-Of setup on Github Pages](#making-of-setup-on-github-pages)
- [x] [VS Code setup](#vs-code-setup)
- [x] [Empty Elm project](#empty-elm-project)


## Git repository on Github

I start with my Github user for "not yet ready" projects.
This project is named "elm-maker".
The main branch is "main".

For accessing the Github repository I execute the following steps:

```text
$ git config credential.github.com.usehttppath true
$ git credential approve
url=https://github.com/<user>
username=<user>
password=<personal-access-token>
<newline>
```

After that I'm able to push to the repository.


## Making-Of setup on Github Pages

The branch name is "gh-pages".
It is an orphaned branch,
so its commit history is independent of the other branches.

The contents is located in the "docs" subdirectory.

In order to have both the Making-Of docs and the sources checked out simultaneously,
I create a git-ignored subdirectory named ".gh-pages".
In this subdirectory I have the "gh-pages" branch checked out.


## VS Code setup

I create a workspace with both the top-level and the ".gh-pages" folders.
Because this workspace is needed mainly to be able to edit the Making-Of docs in parallel,
I name the workspace file "making-of.code-workspace".

Of course I use my VS Code extension [making-of-vscode](https://github.com/pitnyr/making-of-vscode) 😀

The configuration is pretty normal:
```text
making-of.localPath  = /docs/
making-of.publishUrl = https://pitnyr.github.io/elm-maker/
making-of.sourceUrl  = https://github.com/pitnyr/elm-maker/
```


## Empty Elm project

All there is to do is executing "elm init" and creating a simple "Main.elm" file.

I also add a short README.


<a id="commit-2022-02-26-08-59"></a>

## Summary so far

Nothing very special so far. To summarize the commit:

```text
.gitignore               - for elm-stuff and .gh-pages directories
README.md                - short text with link to GH Pages docs
elm.json                 - generated
making-of.code-workspace - VS Code workspace (2 folders, settings)
src/Main.elm             - Hello world Elm code
```

[commit-2022-02-26-08-59](https://github.com/pitnyr/elm-maker/commit/c3a209e148bf4d2fd197ba9fb00e631621955d78)
```email
subject: Create basic project structure
```


## Done

OK, ready to be [merged into the main branch](main.md#commit-2022-02-26-09-48).