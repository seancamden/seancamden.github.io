---
title: Git Revert Commit Reset Hard Origin Master Saved My Bacon
date: 2012-03-30T12:38:22+00:00
author: seancamden
layout: post
st_tiny_url:
  - http://is.gd/llluCk
st_tweetmeme:
  - 's:85:"a:2:{s:7:"tm_link";s:37:"http://tweetmeme.com/story/9748200473";s:9:"url_count";i:0;}";'
st_reddit:
  - 'a:3:{s:9:"permalink";s:0:"";s:5:"score";i:0;s:12:"num_comments";i:0;}'
st_social_score:
  - "0"
st_last_socialized:
  - "1390044063"
st_twitter:
  - "0"
st_facebook:
  - "0"
st_googleplusones:
  - "0"
---
[<img class="alignnone size-full wp-image-428" title="twittergithub logo" src="http://www.seancamden.com/wp-content/uploads/2012/03/twittergithub2_reasonably_small.png" alt="twittergithub logo" width="128" height="128" />](http://www.seancamden.com/wp-content/uploads/2012/03/twittergithub2_reasonably_small.png)

Pushed a bunch of changes to the live site this morning (Friday) that weren&#8217;t supposed to go until Monday. Woops! Fortunately, I use Git and Git rocks!

First, to undo the changes I typed &lsquo;`git revert`&rsquo; and the SHA of the commit in question. (I think I could have just done &lsquo;`git reset --soft HEAD^`&rsquo; if it weren&#8217;t for the fact that I had already done another commit by the time I was informed of my mistake.) Now my working directory is back to the way it was before that commit (but preserving the one that came after).

Then I moved those files onto the live server, undoing my error. Whew! Pretty painless.

Now my working directory or branch is ahead of &lsquo;origin/master&rsquo; by 1 commit, and I want to bring back those changes so that I can push them Monday like I&#8217;m supposed to. I type &lsquo;`git reset --hard origin/master`&rsquo; and I&#8217;m back, like magic.

Thank you, [Git developers](https://github.com/).