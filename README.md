# Upvotes
*A reddit clone with no hate!*

## Why I made it
Lots of platforms online get extreme hate on peoples posts with dislikes or downvotes, so I made a platform with only upvotes!

## How it works
Upvotes is a single-page web app (one 'index.html') backed by [Supabase] (https://supabase.com).

### The basics
- **Subs**: Communities named 's/<name>'. Anyone can make one (3-21 characters: letters, numbers or underscores) and it comes with a description. Creating a sub automatically joins you to it.

- **Posts**: Pick a sub, add a title (up to 200 characters), and optionally attach a link and/or an image (JPG, PNG, GIF or WebP, up to 5 MB).

- **Upvotes only**: Click the ▲ to upvote a post, click it again to take the upvote back. There is no downvote button, anywhere.

- **Sorting**: View posts by **Top** (most upvotes) or **New** (most recent).

- **Joining**: Join or leave subs from the sidebar. Use the account menu to see only your own posts or only posts from subs you have joined.

- **Live updates**: New posts and subs show up in real time without reloading.

### Who are you?
You create an account on first visit to post, and then you can sign in to that account anywhere.

### Moderation
Moderators can sign in from the account menu with an email and password. Signed-in moderators can:
- Delete any post (its image is removed too)
- Delete an entire sub along with all of its posts


Moderator access is granted by setting `role: moderator` in a user's `app_metadata` in Supabase Auth, and it is enforced by Row Level Security in the database, not just by hiding buttons in the UI.

## Tech stack
- Plain HTML, CSS and JavaScript (no build step)
- [Supabase](https://supabase.com): Postgres database, Auth, Storage (post images and pfp's) and Realtime (live feed)
- [`@supabase/supabase-js`](https://github.com/supabase/supabase-js) loaded from jsDelivr