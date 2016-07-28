# reddit-net-api
This repository contains a simple proof-of-concept of a Reddit API written in C#.

# Features

- [x] Get a list if subreddits
- [x] Retrieve data of a specific subreddit
- [x] Retrieve data of a specific post
- [x] Search subreddits

# Usage

```
var redditService = new RedditService();

var subRedditList = await redditService.GetSubredditsAsync();
var subReddit = await redditService.GetSubredditAsync("csharp");

var subRedditPosts = subReddit.Posts;
var post = await redditService.GetPostAsync(subRedditPosts[0].Id);

var title = post.Title;
var score = post.Score;
```
