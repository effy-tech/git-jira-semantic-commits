# Semantic Git commit messages

Inspired by Alexrochas' awesome article on [git semantic commits](https://github.com/alexrochas/git-semantic-commits).

## What is this?
These are **very simple** custom git commands that enforce the git user to write better git commit messages. If still confused, read the article above.

## Installation:

Install with [Antigen](https://github.com/zsh-users/antigen): antigen bundle alexrochas/git-semantic-commits

Or if you feel like doing it the old-fashioned way:

```shell
mkdir -p ~/src
git clone git@github.com:effy-tech/git-jira-semantic-commits.git  ~/src/git-jira-semantic-commits
print 'source ~/src/git-jira-semantic-commits/git-jira-semantic-commits.plugin.zsh' >> ~/.zshrc
```

## Usage

First of all, the current branch you're working on should include the jira reference to your ticket / task / epic / story. (Like `QUA-1234`)

There are 8 new Git commands now.
Each commands will find in the current branch name, and the jira tag contained in it : like `QUA-1338` in `QUA-1338_cost_estimator_for_serenity_projects`.
If you type `git-feat "with a message"`, it will prefill the commit message like following : ```feature() [QUA-1338]: with a message```
Messages are optionals, so you can do `git-feat` and get ```feature() [QUA-1338]: ```

You just have to complete or just save !

New command -> what it does:
* ```git-feat "commit-message-here"``` ->     ```git commit -m 'feature() [ABC-1234]: commit-message-here'```
* ```git-docs "commit-message-here"``` ->     ```git commit -m 'docs() [ABC-1234]: commit-message-here'```
* ```git-chore "commit-message-here"``` ->    ```git commit -m 'chore() [ABC-1234]: commit-message-here'```
* ```git-fix "commit-message-here"``` ->      ```git commit -m 'fix() [ABC-1234]: commit-message-here'```
* ```git-refactor "commit-message-here"``` -> ```git commit -m 'refactor() [ABC-1234]: commit-message-here'```
* ```git-style "commit-message-here"``` ->    ```git commit -m 'style() [ABC-1234]: commit-message-here'```
* ```git-test "commit-message-here"``` ->     ```git commit -m 'test() [ABC-1234]: commit-message-here'```
* ```git-localize "commit-message-here"``` -> ```git commit -m 'localize() [ABC-1234]: commit-message-here'```

If you would still like to use your text editor for your commit messages
you can omit the message, and do your commit message in your editor.

* ```git-feat``` -> ```git commit -m 'feat() [ABC-1234]: ' -e```

## How to contribute
Open a pull request/issue or fork this repo and submit your changes via a pull request.
