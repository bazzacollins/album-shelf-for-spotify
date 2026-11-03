# Album Shelf (for Spotify)

A CD shelf for your Spotify library, built to run full-screen on a spare tablet.

Your saved Spotify albums sit on wooden shelves as CD spines, each coloured from its cover art. Tap a spine and it pulls out face-on with Play and Tracks buttons. The album that's playing turns face-out in the middle of the shelf, and the track list is one tap away. Playback goes through Spotify Connect, so the music comes out of whichever speaker, phone or tablet you pick.

It's a single `index.html` with no build step and no server code. Everyone runs their own copy with their own free Spotify developer app; there's no shared service. Open it and tap **Try demo shelf** to see it without a Spotify account.

## What you need

- **Spotify Premium.** Spotify requires it for personal developer apps and for remote playback.
- **A free Spotify developer app.** It's yours alone; development-mode apps allow up to five users.
- **Somewhere to host the page over https.** GitHub Pages works.

## Setup

1. **Fork this repository** to your own GitHub account.
2. **Add the Spotify logo.** Spotify requires its logo next to its content. Download the full logo from [Spotify's design guidelines](https://developer.spotify.com/documentation/design), and add the white version to the repository as `spotify-logo.svg` or `spotify-logo.png`. Until you do, the shelf shows an empty placeholder where the logo goes.
3. **Turn on GitHub Pages.** In this repository go to **Settings → Pages**, set the source to *Deploy from a branch*, and choose `main` and `/ (root)`. After a minute the site appears at `https://<your-username>.github.io/album-shelf-for-spotify/`.
4. **Create a Spotify app.** At [developer.spotify.com/dashboard](https://developer.spotify.com/dashboard), create an app and tick **Web API**.
5. **Add the redirect URI.** Open your Pages address, tap the settings (gear) button, and copy the redirect URI it shows. Paste it into the Spotify app's **Redirect URIs** field exactly as shown, then save.
6. **Connect.** Copy the app's **Client ID** into the shelf's settings and tap **Connect Spotify**.
7. **Make it feel like a device.** On the tablet, open the page in Chrome, use **Add to Home screen**, and launch it from there. Use the full-screen button and, in settings, pick a default speaker.

If Spotify says your account isn't registered for the app, add your Spotify email under **User Management** in the developer dashboard.

## Good to know

- **The Client ID isn't in this repository.** It's typed into the page and stored only in the tablet's browser, so the repo holds nothing private.
- **Sign-in lasts about six months.** Spotify now expires sign-ins after that, so you'll need to tap **Connect Spotify** again roughly twice a year.
- **New albums appear automatically.** While the shelf is on screen it checks Spotify for added or removed albums every 15 minutes, and again when you come back to it. Use **Refresh albums** in settings to update it straight away.
- **Settings** cover how many shelves to show, what a tap on a spine does, the face-out cover, grey or clear CD cases, keeping the screen on, and fading the controls when idle.

## Privacy

Album Shelf runs entirely in the browser. Your Spotify sign-in, album list and settings are stored only on the device you use it on, and are never sent anywhere except to Spotify. **Sign out** in settings removes them, and you can also remove the app's access from your Spotify account page under **Manage apps**.

## Licence

MIT — see [LICENSE](LICENSE). Album Shelf isn't affiliated with or endorsed by Spotify. Spotify and the Spotify logo are trademarks of Spotify AB.
