---
layout: default
title: Privacy policy
permalink: /privacy/
---
<div class="wrap article" markdown="1">
<header class="article__head">
<p class="label label--accent">Privacy</p>
<h1 class="article__title">Privacy policy</h1>
</header>
<div class="prose" markdown="1">

*Last updated: 18 October 2026*

This policy covers the Lucidum publishing tool: a private, server-side tool used only by the owner of the Instagram account **@lucidum.science** to publish our own Reels, read our own account's statistics, and reply to comments on our own posts. It has no public sign-up and no other users. This website itself sets no tracking cookies.

## What data the tool accesses

Through the Instagram API, with the account owner's permission, the tool accesses only data belonging to or posted on **@lucidum.science**:

- **Our account and our media:** profile name, follower count and the posts we published (`instagram_business_basic`).
- **Our statistics:** views, reach, saves, shares and similar numbers for our own posts (`instagram_business_manage_insights`).
- **Publishing:** uploading Reels and Stories that the account owner has approved (`instagram_business_content_publish`).
- **Comments on our own posts:** the comment text, the commenter's public username and the time, so we can reply (`instagram_business_manage_comments`).

We never access other accounts' posts, private messages, followers lists or any data from accounts other than our own, except the public username and text of comments people leave on our posts.

## How we use it

- Statistics decide which topics and posting times to focus on.
- Comments on our posts are read so that the account owner can reply. The comment text may be passed to an AI assistant (Anthropic's Claude) to draft a reply. **A person approves every reply before it is posted**; nothing is posted automatically.
- We never sell data, never use it for advertising, and never share it with anyone except the service providers below, which process it only to run the tool.

## Where it is processed and stored

- **GitHub (Microsoft):** the tool runs on GitHub Actions; account statistics and pending comments are stored in a private GitHub repository.
- **Telegram:** drafted replies and statistics summaries are sent to the account owner's private Telegram chat.
- **Anthropic:** comment text may be sent to Claude to draft replies.

## Retention

Comments are kept only until they are answered and for at most **30 days**, then deleted from our storage. Aggregate statistics about our own posts are kept to compare performance over time and contain no personal data.

## Your choices and deletion

If you delete your comment on Instagram, the tool will no longer see it. To ask us to delete any data we hold about you (for example, a comment you left), follow the steps on our [data deletion page]({{ '/data-deletion/' | relative_url }}). We will delete it within 30 days.

## Contact

Send a direct message to [@lucidum.science on Instagram](https://www.instagram.com/lucidum.science/).

</div>
</div>
