---
title: "Jujutsu Meetup Talk"
date: "2026-02-18"
tags: ["jujutsu", "vcs", "git", "meetup"]
slug: "jujutsu-meetup-talk"
summary: "Hands-On with jj: A Git-Compatible VCS"
status: "done"
---

# `Jujutsu Meetup Talk`

Presentation notes from the Software Crafters meetup event in Athens.

## Presentation materials
- [Presentation slides (PDF)](./assets/Jujutsu.pdf)

## Slide 3
You probably heard by now about Jujutsu.
How they call themselves - a Git-compatible VCS that is both simple and powerful.
Now that I have played a little with it I think they are underselling themselves!

There's a hype: `jj` comes into your world like a spoon to replace a fork you've been struggling to eat your soup with.

## Slide 4
But in reality - I think it's more of an upgrade to your fork

Because `git` is a good and powerful tool. There is a reason why it got so popular so quickly. However `git` requires you to speak its language. `jj` was built to speak yours.
Jujutsu takes the good parts of git and addresses the bad.

## Slide 5
Let's have a look what is this evening going to be about
- I am going to highlight what jj does differently.
- Run quickly through some regularly used commands to get the idea of the flow.
- Go over 2 popular ways of doing jj.
- try to use the gained knowledge in an assisted workshop.

I will not going to be deep diving into many interesting parts of jj:
- we don't have enough time here today to cover it
- you don't have the brain capacity to take it all in(in just in over an hour)
- I don't know enough about it myself because I am not even a committed `jj` user yet.

any comfortable questions so far?

## Slide 6
So why it's an upgraded fork and not a ladle?
Because it still feels like you're doing git, but differently.
And that comes with a price.
You will need to rework your muscle memory.
You will need to train your eyes.
You will need to learn how to use it with your team.
Some things you will have to (re)learn, some things you will have to accept.

Goes example about me switching to left handed mouse and having to deal with the world designing everything for right handed people.

## Slide 7
So what did Jujutsu do right so that it started snowballing with its popularity?
Commits(git) vs changes(jj).

In git you `commit` to git log and from then on, you are `commited` to the work you produced AKA it's immutable. If you want to change something about it - you start doing the dance. Sometimes it's an easy one. Sometimes you end up with entangled limbs.

A `change` - is a unit of work. You do it. You move on. You get back, change something, again, move on. You change the work and its description whenever you please. If there are subsequent commits, your changes are automatically rebased.

## Slide 8
Branchless work

One big difference is in `jj` branches don't mean much. You're are constantly working in a detached HEAD. your worst nightmare is now your safe space. In `jj` you do branches mainly for your git buddies.

## Slide 9
Edit a parent change and the changes automatically will be propagated to the children.

## Slide 10
Conflicts are not emergencies. Commit them, deal with them later.

## Slide 11
OpLog/evolog

Oplog tracks your `jj` commands. does the snapshots whether you rebase or just do jj log. And it's amazing. Because when you corner yourself you just op log revert into the times before everything started falling apart.

Evolog is how your commit changed over the time :head_explode_emoji:

## Concepts to explore that aren't covered here today
- evolution log
- split
- rebase

## Whom `jj` is not for
- People who rely on git lfs.  
  There's an open pr that's getting some traction lately, but the issue has been open for years. So if your repo relies on things like git filters smudge/clean etc
- if your repositories are protected from force pushing.  
  In `jj` world it's an action that's safe to perform, however there's a reason some block it on git.
- you tell me
