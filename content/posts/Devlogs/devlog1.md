+++
title = 'Devlog #1'
description = 'Exploring the world of behaviour trees'
slug = 'hello-world'
date = 2025-12-02T06:36:05Z
draft = false
tags = ['games']
categories = ['devlog']
+++

## This week in game development

Recently I have been working on a more advanced enemy.
It is relatively trivial to setup an enemy you can hit, or if you touch will hurt you.
Likewise it is straightforward to create an enemy that wanders around randomly. You can even go a bit further and add some simple logic to such a wander that makes sure it doesn't go into walls or fall off ledges.

More complicated is creating an enemy who behaves a bit more predictably, but might string together different actions.
I found my finite state machine method I had been using so far was becoming overly cumbersome.

Let me introduce behaviour trees.
Behaviour trees are fairly old and well understood, you can see references

- wiki
- gamasutra project zomboid
- unity behavior

## Exploring options

I explored a few different options but ultimately went with the Unity Behavior package.
I understand this to no longer be getting support (typical Unity) but it was last updated only a few days before I implemented it and ultimately I'm not looking for anything too fancy at this stage.

I've touched behaviour trees before in both Unity and Unreal however I always bounced off them as being overly complex and dense to understand. This time round I approached it a bit differently and built from scratch my own behaviour tree implementation.
This was a rough as guts, code only set up. However this allowed me to really come to grips with two key aspects I had struggled to wrap my head around before.

1. Every tick if the tree has finished it will re-evaluate from the start.
2. Every node needs to return at least three responses
   1. Running - Still ongoing, do not proceed and do not re-evaluate.
   2. Success - The work is done and the node is completed.
   3. Failure - The work is not done (it may have done some of it) but we cannot continue.
