# Contributing Guidelines

First of all, thank you from all of the [contributors] for enjoying the theme
enough to want to give back. We have plenty of space for everyone to contribute.
Please check for any [issues] you may be able to solve, any [pull requests] you
can help review, any [projects] you can contribute to, or anything else you may
see.

The goal of this repository is to provide a great Hugo theme for everyone, as
well as being an opportunity for people to learn how to use Git and GitHub.

## Table of Contents


<!-- TOC depthFrom:2 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [Table of Contents](#table-of-contents)
- [Getting Set Up](#getting-set-up)
	- [Requirements](#requirements)
	- [Forking](#forking)
	- [Syncing](#syncing)
		- [Git Bash, Command Prompt, PowerShell](#git-bash-command-prompt-powershell)
		- [GitHub Desktop](#github-desktop)
- [Creating an Issue Ticket](#creating-an-issue-ticket)
- [Creating a Pull Request](#creating-a-pull-request)
- [Style Guide](#style-guide)
- [Thank You](#thank-you)

<!-- /TOC -->

## Getting Set Up

### Requirements

1. A [GitHub Account].
2. Either [Git] (preferable) or [GitHub Desktop]
3. The latest version of [Hugo][Hugo Release].
4. The latest version of [hugo-future-imperfect][Head].

### Forking

Navigate to the theme repository [jpescador/hugo-future-imperfect][head],
and then click **Fork** in the top right. This will create your copy of the
theme.

### Syncing

Since changes to one aspect of a Hugo theme tend to require changes in multiple
locations, this step is vital. Please *always* make sure you stay in sync with
the original, or create an issue or pull request so we know what files are being
worked on and we can manage it that way.

#### Git Bash, Command Prompt, PowerShell

*Note:* Substitute all `CAPS` with the applicable information pertaining to you.

1. **Set Up Git**

   If you haven't yet, you should first [set up Git][GitHub Git]. You will also
   need to [set up authentication to GitHub from Git][GitHub Authentication] as
   well.

2. **Create A Local Copy**

   ```
   cd PATH/TO/YOUR/LOCATION
   git clone https://github.com/YOUR-USERNAME/hugo-future-imperfect
   ```

   You have now cloned your fork to the location specified.

3. **Connecting Fork with Original**

   ```
   git remote add upstream https://github.com/jpescador/hugo-future-imperfect.git
   ````

   You have now connected your fork with `jpescador/hugo-future-imperfect`,
   the `upstream`.

   To confirm this:

   ```
   git remote -v
   ````

   Which should return:

   ```
   origin    https://github.com/YOUR_USERNAME/hugo-future-imperfect.git (fetch)
   origin    https://github.com/YOUR_USERNAME/hugo-future-imperfect.git (push)
   upstream  https://github.com/jpescador/hugo-future-imperfect.git (fetch)
   upstream  https://github.com/jpescador/hugo-future-imperfect.git (push)
   ```

4. **Keeping it synced**

   ```
   git fetch upstream
   git checkout master
   ```

   You have now fetched the files from the upstream and have confirmed that you
   are on the master branch.

   1. If you need to *merge* any changes you've made with the updated original,
   use the following:

      ```
      git merge upstream/master
      git push origin master
      ```

   2. If you need to *reset* any changes you've made back to the original for
   whatever reason, use the following:

      ```
      git reset --hard upstream/master
      git push origin master --force
      ```

#### GitHub Desktop

1. **Create A Local Copy**

   1. **File** -> **Clone Repository...**
   2. Select your fork, `YOUR_USERNAME\hugo-future-imperfect`
   3. Choose your local path
   4. Press **Clone**

   You have now cloned your fork to the location specified.

2. **Syncing Fork with Original** and **Keeping it Synced**

   This is currently not possible via GitHub Desktop, but is on the feature list
   for [v1.1][GitHub Desktop 1.1]. Keep an eye out for that release.

   In the meantime, the *best* way to stay in sync is to create a pull request
   where the `base fork` is `YOUR_USERNAME/hugo-future-imperfect` and the `head
   fork` is `jpescador/hugo-future-imperfect`.

## Creating an Issue Ticket

When you go to create an issue ticket, you will notice [a template][issue template]
appears. Please adhere to this for the sake of consistency and organization. A
couple of things to note from that template are:

1. **Check all the prerequisites**

   Make sure you have done all the steps at the top before submitting the issue
   ticket. Redundancy can easily clutter the repository meaning less time
   working on the theme and more time having to do clean-up. They are as follows:

   - [ ] I am running the [latest version of Hugo][Hugo Release]
   - [ ] I am using the [latest version of Hugo-Future-Imperfect][Theme Sync]
   - [ ] I checked the [documentation] and found no answer
   - [ ] I checked the [issues][All Issues] to make sure that this issue has not
   already been filed

2. **Be very clear with your descriptions.**

   Err on the side of too much information. It helps track the problem down
   quicker or figure out how to implement it easier.

## Creating a Pull Request

In an effort to increase simplicy of the theme, we are going to try to implement
this [branching model]. For most people, this will be common sense. If you are
new to Git, it's a good read that explains it well concisely.

When contributing to the project, please keep your `master` branch in sync with
the upstream `master` branch. Each new feature should have a new branch labeled
`my-feature`, `feature-fix`, or a similarly descriptive label. If you would like
to have a personal `master` branch, please label it whatever you'd like, but
preferably `YOUR_USERNAME`. This helps keep track of all changes and keeps the
[network] clean and easy to navigate. This is especially useful if some decides
to fork on their own, but may implement features we may want for the original.

When you go to create a pull request, you will also notice [a template][Pull Request Template]
appears. Again, please adhere to this for the sake of consistency and
organization. A couple of things to note from that template are:

1. **Check all the prerequisites**

   Make sure you have done all the steps at the top before submitting the pull
   request. Redundancy can easily clutter the repository meaning less time
   working on the theme and more time having to do clean-up. They are as follows:

   - [ ] I am running the [latest version of Hugo][Hugo Release]
   - [ ] I am using the [latest version of Hugo-Future-Imperfect][Theme Sync]
   - [ ] I checked the [issues][All Issues]
  to make sure that this feature has not been rejected before
   - [ ] I checked the [pull requests][All Pull Requests]
  to make sure that this feature is not already being developed

2. **Always include any related issues**

   Make sure in the comments that you include any issues this closes by writing
   `Closes #XXX` under *Motivation and Context*. This will automatically close
   the issue when the pull request is accepted.

## Style Guide

For the sake of consistency, please use the [Google HTML 5 and CSS 3 Style Guide].

You will notice that a large portion of the theme does not adhere to this style
guide. The original HTML 5 UP theme uses 4 space tabs instead of 2 space tabs.
This, again, adds to bloat, especially when using Hugo functions. If you are
making a change to a file, please go ahead and fix any styling in the region
relative to where you are working. This will help us slowly fix the theme. Once
theme theme becomes more active with people constantly resyncing, we can look at
doing an across the board change (we might actually look at doing this as part
of [v0.30][Next Release] since that will be a rather large change requiring
everyone to resync).


## Thank You

Thank you again for your interest in contributing to the theme. Feel free to ask
any questions you may have. We are here to help.

<!--- Project Specific References -->

[Issue Template]: https://github.com/jpescador/hugo-future-imperfect/blob/master/.github/ISSUE_TEMPLATE.md
[Issues]: https://github.com/jpescador/hugo-future-imperfect/issues
[All Issues]: https://github.com/jpescador/hugo-future-imperfect/issues?utf8=%E2%9C%93&q=is%3Aissue
[Pull Request Template]: https://github.com/jpescador/hugo-future-imperfect/blob/master/.github/PULL_REQUEST_TEMPLATE.md
[Pull Requests]: https://github.com/jpescador/hugo-future-imperfect/pulls
[All Pull Requests]: https://github.com/jpescador/hugo-future-imperfect/pulls?utf8=%E2%9C%93&q=is%3Apr
[Contributors]: https://github.com/jpescador/hugo-future-imperfect/graphs/contributors
[Documentation]: https://github.com/jpescador/hugo-future-imperfect/wiki
[Head]: https://github.com/jpescador/hugo-future-imperfect
[Network]: https://github.com/jpescador/hugo-future-imperfect/network
[Next Release]: https://github.com/jpescador/hugo-future-imperfect/milestone/1
[Projects]: https://github.com/jpescador/hugo-future-imperfect/projects
[Theme Sync]: #syncing

<!--- External References -->

[Branching Model]: http://nvie.com/posts/a-successful-git-branching-model/
[Git]: https://git-scm.com/downloads
[GitHub Account]: https://github.com/login
[GitHub Authentication]: https://help.github.com/articles/set-up-git#next-steps-authenticating-with-github-from-git
[GitHub Desktop]: https://desktop.github.com/
[GitHub Desktop 1.1]: https://github.com/desktop/desktop/milestone/11
[GitHub Git]: https://help.github.com/articles/set-up-gi
[Google HTML 5 and CSS 3 Style Guide]: https://google.github.io/styleguide/htmlcssguide.html
[Hugo Release]: https://github.com/gohugoio/hugo/releases
