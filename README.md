# Upvotes

*A reddit clone with no hate!*

### My motivation to create this:

Many sites online receive a lot of hate on peoples posts with dislikes/down votes so I created a site with only up votes!

## How it works

Upvotes is a single page web app (a single index.html) powered by Supabase.

## The basics

- **Subs**: s/<name> communities. Anyone can create a sub (3-21 characters of letters, numbers, and/or underscores) and have a description. By creating a sub you get added to it.

- **Posts**: Select a sub, enter a title (up to 200 characters), then include a link and/or an image (JPG, PNG, GIF or WebP, up to 5 MB).

- **Upvotes only**: click on to upvote a post, click on again to undo the upvote. And there is no downvote button in any place.

- **Sort**: Posts can be sorted by Top (most upvoted) or New (most recent).

- **Browsing**: Browse all of your own posts, or only the posts from the subs you have joined, using the account menu. See all posts, or limit to only those you have joined in the account menu.

- **As you scroll**, new posts and subs are added dynamically.

### Who are you?

You first visit to post creates an account for you, once you do so you can log into this account from anywhere.

### Moderation

Moderators can Log in from account menu with an email and password. Logged in moderators can:
- Remove any post (as well as the image)
- One entire sub and all its posts.

The button for grant to mod is restricted by role: moderator in app_metadata on db in supabase auth, and it is not only hidden from UI but also row level security on db.

### Tech stack

- Plain HTML, CSS and JavaScript (no build step)
- Supabase, https://supabase.com: Postgres DB, Auth, Storage (for posting images and pfp's) and Realtime (live feed)
- @supabase/supabase-js loaded from jsDelivr
