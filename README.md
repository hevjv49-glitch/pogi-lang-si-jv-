# JIV'S BLASTT

A neon block puzzle game for desktop and mobile browsers.

## Latest upgrade

- Three visual themes: Neon, Sunset, and Mint. Tap the half-circle theme button to cycle through them.
- Automatic save/continue for the current board, score, combo, and sound setting on the same browser/device.
- Best score remains saved locally.
- Offline app cache refreshed to version 2.

## Play

Open the GitHub Pages site. On iPhone, open it in Safari and choose **Share → Add to Home Screen**. On Android, open it in Chrome and choose **Install app** or **Add to Home screen**.

## How to customize the game

1. Open this repository on GitHub.
2. Click **index.html**.
3. Click the pencil **Edit this file** button.
4. Make your changes.
5. Click **Commit changes**. GitHub Pages will publish the update after its deployment finishes.

### Change the block colors

In `index.html`, find the `colors` array near the start of the game script. Replace its hex color values, for example `#55dff7`, with your own hex colors.

### Add a new block shape

Find the `shapes` array in the game script. Each shape is a list of grid coordinates. For example:

```js
[[0,0],[1,0],[2,0]] // three blocks in a horizontal line
```

Add another coordinate list inside the `shapes` array, separated by a comma.

### Add a new theme

Find the CSS rules for `body[data-theme="sunset"]` and `body[data-theme="mint"]`. Add another theme rule with your chosen CSS colors, then add its name to the `themes` array in the script.

**Tip:** Make one small change at a time, commit it, then test the website on PC and phone.

## Offline support

The service worker caches the game shell after the first visit. GitHub Pages serves the site over HTTPS, which is required for service workers.
