---
layout: post
title: Write your commit message first
---
You sit down to make a small tweak to a view. It unexpectedly turns out you also have to fiddle with a controller. And this requires you to poke around inside a couple of models. And now your event propagation system is looking a bit weird, so you decide to make a small refactor. 12 hours and 8 Bacardi Breezers later you think you’ve finished the refactoring, but you have absolutely no idea how you go there.

The next day you stand up to update 6 pages in your app to reflect some new properties on your User model (you have a standing desk now). You get out your Vim-based sledgehammer and break all of the pages so that you can rebuild them in parallel. 3 hours of constant context switching later you are still standing in an alarming amount of rubble with very little commitable code to show for it.

These are two incredibly typical examples of not defining your immediate scope tightly enough. When you don’t know where the next checkpoint you want to reach is, you can find yourself up a creek without a goalpost, feeling as muddled as these metaphors. Having found myself in this intensely confusing place one too many times, I’ve started using <a href="http://gitx.frim.nl/" target="_blank">Gitx</a> to write my commit messages before starting the commit. This forces me to think about keeping things small and contained, and makes me think twice before going off the reservation. Did I plan on this? Is this something I should be doing now? Is this going to be easy to unwind?

* “Added methods to PointsScorer to calculate points scored in the last game and add to the User’s total”
* “Content of congratulation email for user when they hit their target”
* “Refactor PointsTotal into its own table, separate from the User table”

are all much better than 8 commits of “Worked on points,” “More stuff on points”, “Fix bugs on points”, “Tidyups on points”, each of which touch every layer of the feature in seemingly random places and ways. As Confucius probably once said, he who tries to fix everything at once, fixes nothing. Of course, you will often run into challenges you didn’t know about before starting, and this is fine. You just change the commit message. But your planned message still serves as a record of what you had initially intended to do. If you keep finding yourself in dark and scary parts of town that you had no intention of visiting, you’ll know about and will be able to start curing yourself of this ruinous habit. Assuming you make it out alive this time.
