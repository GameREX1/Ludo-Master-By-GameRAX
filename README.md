# Ludo Master by GameRAX

A free, responsive HTML5 Ludo game where you play against Nexus, a robot opponent.

## Features

- Play against a built-in robot AI with Smart and Normal difficulty.
- Animated dice, token movement, safe squares, captures, extra turns on a six, and an exact-roll finish.
- Responsive dark gaming interface with GameRAX branding.
- Sound effects with an on/off toggle.
- No build tools or paid services required — the game is a single `index.html` file.

## Run locally

Open `index.html` in a modern browser.

## Publish with GitHub Pages

In the repository, open **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**, set the branch to `main` and folder to `/ (root)`, then save. GitHub will show the published website URL in that Pages section once deployment completes.

GameRAX: https://gamerax.online/


## Account and friend-invite setup

The login/sign-up and username invite UI uses the existing GameRAX Supabase project, but it has its own `ludo_profiles` and `ludo_friend_requests` tables. It does not modify GameRAX's existing tables.

1. Open the project's Supabase dashboard.
2. Go to **SQL Editor → New query**.
3. Open [supabase-setup.sql](./supabase-setup.sql), copy its contents into the SQL editor, and click **Run**.
4. In **Authentication → URL Configuration**, set the site URL to your GitHub Pages URL and add that URL to the redirect allow list if email confirmation is enabled.
5. Ensure email/password authentication is enabled. With email confirmation enabled, users need to verify their email before logging in.

After the SQL setup is run, users can create accounts, choose unique usernames, send friend requests by username, accept/decline incoming requests, and see their friend list. The sidebar refreshes periodically.

The invite list is online; actual private room codes and real-time multiplayer Ludo gameplay are not included yet. The current board remains a local match against the robot.
