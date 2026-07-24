# 🐻‍❄️ Bearwatch

A little movie and TV tracker that runs entirely in your browser. You can keep tabs on what you're watching, what's on your watchlist, and what you've already finished, plus ratings, episode progress, release reminders, a calendar, and a few stats. Nothing to install, no account to make, and no server involved. All your data just stays in your own browser.

(The name's a tip of the hat to my two dogs, Polar and Bear. Put them together and you get a polar bear.)

**Live app:** https://ninjakane.github.io/bearwatch/

## What it does

- Search for any movie or show and drop it straight into your list
- Sort everything into Watching, Watchlist and Watched, with a 10-star rating, notes, filters and sorting
- Track your way through a show season by season (there's a "+1 Ep" button and progress bars)
- See upcoming releases and next episodes on a calendar, grouped by today, this week, and later on
- Get reminders for release days, in-app and as desktop notifications if you turn them on
- Browse a "You might like" row built from the stuff you've rated highly
- Dig into your stats: hours watched, genre and decade breakdowns, rating spread, and a Wrapped-style card
- Import your history from Netflix, Letterboxd, IMDb, Trakt, or honestly just about any CSV
- Back the whole library up to a JSON file, and load it back in whenever
- Optionally sync across your devices with your own Google Drive (see below)
- Catch up on recent updates from the "What's new" list in Settings

## Getting started

The one thing you'll need is a free TMDb API key, which is what lets the app look titles up. It only takes a couple of minutes:

1. Make a free account at [themoviedb.org](https://www.themoviedb.org/signup) and confirm your email.
2. Head to [Settings → API](https://www.themoviedb.org/settings/api), click Create, pick Developer, and fill in the short form.
3. Copy your API Key (v3 auth). It's a long string of letters and numbers. (A v4 Read Access Token works too if you'd rather.)
4. Open the app, go to Settings, paste the key in and hit Save & Test.

The app runs you through these same steps the first time you open it, so you don't really need to keep this page around.

## Put it on your phone

It installs like an app without going anywhere near an app store. On Android, open the live link in Chrome, tap the menu, and pick "Add to Home screen" (or "Install app" if it offers that). On an iPhone, open it in Safari, tap Share, then "Add to Home Screen". Either way you get the Bearwatch icon on your home screen and it opens fullscreen, just like a normal app. By default your data lives on that one device, but if you'd like it in step across your phone and computer, see the next section.

## Syncing across devices

By default nothing leaves your browser, which also means your phone and your computer each keep their own separate library. If you'd rather have them stay in step, there's an optional Google Drive sync under **Settings → Cloud sync**. Connect it on each device with the same Google account and Bearwatch keeps them merged, and quietly backs your library up at the same time. It's free, and it uses your own Drive, so nobody else (me included) can see your data.

It only ever touches a single file it creates in your Drive, called `bearwatch-library.json`. It cannot see, open, or touch anything else in your Drive, so the rest of your files stay completely private to you.

**One thing to expect:** the first time you connect, Google shows a screen warning you that the app hasn't been verified (usually behind an "Advanced" link, then "Go to Bearwatch"). That's normal for a small personal project like this one rather than a sign anything's wrong. It comes up because I haven't paid to go through Google's formal verification, not because the app is doing anything it shouldn't, and because of the single-file limit above it genuinely can't reach the rest of your Drive. If you'd rather not sign in at all, you don't have to. The Export and Import buttons still move your data around by hand, exactly as before.

## Running it offline

If you'd rather not use the hosted version, grab `index.html` and just double-click it. It opens in your browser and works almost exactly the same, the one exception being Google Drive sync, which only works on the hosted link. The other catch: run as a local file, the browser ties your saved data to that file's exact spot, so try not to move or rename it once you've started adding things. Export a backup from Settings now and then just to be safe.

## A few things worth knowing

Out of the box, everything lives in your browser's local storage, so none of it gets uploaded anywhere. That does mean each browser and device keeps its own separate copy, so to move data around you've got the Export and Import buttons, or the optional Google Drive sync above if you'd like it kept in step automatically. And since there's no server running in the background, reminders only show up while the page is actually open. It can't ping your phone.

## License

Released under the [PolyForm Noncommercial License](LICENSE). Short version: use it, share it, mess about with it however you like, just don't sell it. If you pass on your own version, keep the Required Notice line in the LICENSE file.

## Attribution

This product uses the TMDB API but is not endorsed or certified by TMDB.
