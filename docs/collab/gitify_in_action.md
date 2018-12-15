# Using Gitify to Collaborate on Themes

You mist have [Gitify set up](collab/gifiy.md) with your theme in order to follow these instructions.

## Working with Gitify

A common purpose of collaborating on a Theme will be to build a series of Elements, Bluepints, Options, and RTE Configs.

Once you’ve installed and worked on a Theme with a team, you’ll find yourself needing to do some common things:

### Get the latest contributions from your collaborators

TODO: @theboxer … this section needs more explanation/clarification for git CLI newbies.

For the purposes of this tutorial, our theme will only have one branch in Git (master). As such, you’ll need to set the remote branch for future git commands:

```
git branch --set-upstream-to=origin/master
```

When all your changes are pushed to the local repository you’re working on: 

```
cd ~/www
git pull
gitify package:install --all
gitify build
```

If you have changes in your instance, perform the following. You’ll see messages about Extracting various Fred-related things:

```
cd ~/www
gitify extract
git add --all # or git add on files you want to commit
git commit -m "Your commit message here" # please write your own message!
git pull
# resolve conflicts if any
gitify package:install --all
gitify build
```

#### Working with `git` from the command line

If you're not familiar with Vi or Vim, chance are you’ll be lost when creating the commit message. You can make commits without specifying the message, which puts you into a Vi editor. The benefit of this is that you get to review what all will be pushed. 

Here are a few pointers:  

- Write the commit title on the first line. A more detailed description can go on subesequent lines.
- Things with a `#` in front will be ignored. 
- When you’re done, press the `esc` key then type `:wq` to exit.
- If you really get stuck, it is Vi after all, [StackExchange to the rescue]()!

### Push your changes back to your Github repository

```
cd ~/www/
gitify extract
git add --all # or git add only the files you wish to commit
git commit -m "Your commit message here" # please write your own message!
git push origin master # replace master with branch name you want to push into
```

## Submit a Pull Request (PR) to the main Project

TODO: @theboxer 

Need to describe how to do this from Github, and possibly from the CLI.