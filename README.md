# Battleship HQ — the front door

One page. It carries the icon and the link preview that Apps Script refuses to,
then sends you into the game.

## Putting it live (about ten minutes, once)

**GitHub Pages**
1. github.com → sign up if needed → **New repository** → name it `battleship-hq` → Public → Create.
2. On the empty repo page: **uploading an existing file** → drag in every file from this
   folder → **Commit changes**.
3. **Settings → Pages** → Source: *Deploy from a branch* → Branch: `main`, folder `/ (root)`
   → Save. Give it a minute.
4. Your URL: `https://<your-username>.github.io/battleship-hq/`

**Netlify** is the shorter route if you'd rather: netlify.com/drop, drag this folder on,
done in thirty seconds. Same result, no repo.

## Adding it to a home screen
Open the page with **`#stay`** on the end — `.../battleship-hq/#stay` — so it doesn't
jump straight into the game. Then Share → Add to Home Screen. The icon and the name
come from this page. From then on, tapping it goes straight through.

Without `#stay` the page waits 600ms and forwards you into the game, which is what you
want every other time.

## Sending it to Ben
Text him this URL instead of the tinyurl. He'll see a card with the ship and
"Battleship, except every shot costs you a run" rather than a grey script.google.com box.

## If the game's web app URL ever changes
Change the one `href` on the `#go` link in `index.html`, and the line beneath it. That
happens if the deployment is ever recreated rather than updated — it hasn't yet.

## Later, if you want a real domain
Buy one (~$12/yr), point it here (GitHub: Settings → Pages → Custom domain). Nothing
else changes. That is also the point at which moving the game's front end off Apps
Script becomes worth discussing — same repo, and it would end the Safari storage
trouble, because that is caused by the game running in a frame from another site.

## Files
  index.html          the page
  icon-180.png        home screen (iOS)
  icon-192/512.png    home screen (Android) via site.webmanifest
  icon-32.png         browser tab
  og.png              the preview image in messages
  site.webmanifest    Android icon + name
