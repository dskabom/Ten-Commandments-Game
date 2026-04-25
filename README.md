# The Tablets of Stone

A two-team scripture quest game for LDS Primary classes (built for ages 10–12). Teams take turns looking up scriptures from across the standard works — Old Testament, Book of Mormon, Doctrine and Covenants, and Pearl of Great Price — and matching each one to the Ten Commandments it teaches.

## How to Play

1. Split the class into two teams: **Team A** and **Team B**.
2. Each round, the active team is given a short story summary and a scripture reference.
3. The team finds the verse in their own physical scriptures and reads it aloud.
4. The team chooses which of the Ten Commandments the story teaches.
   - **Correct** → they earn a tablet for their team.
   - **Wrong** → the other team gets a chance to steal — with a *brand new scripture about the same commandment*.
5. If both teams miss, no tablet is awarded that round.
6. Teams alternate who goes first. Whoever finishes with the most tablets wins.

Both teams need their own copy of the scriptures (or a phone with the Gospel Library app).

## Running the Game

This is a single, self-contained HTML file. There are no servers, no build steps, and no dependencies to install.

### Option 1: Open it locally
Just download `index.html` and double-click it. It opens in any modern browser.

### Option 2: Host it on GitHub Pages (free)
1. Fork or clone this repo to your own GitHub account.
2. Go to **Settings → Pages**.
3. Under **Source**, choose `main` branch and `/ (root)`.
4. Save. After a minute, your game will be live at `https://<your-username>.github.io/<repo-name>/`.

### Option 3: Project a phone or tablet to a screen
The game is mobile-friendly. Open it on a phone or tablet, then mirror to a TV or projector with AirPlay, Chromecast, or an HDMI adapter.

## What's Inside

- **Ten rounds**, one per commandment.
- **Two scriptures per commandment** — one primary, one used for the "steal" attempt — drawn from across the standard works.
- **Score tracking** for both teams, with a tablet visualization that fills in as the game progresses.
- **Final results screen** showing which team won each commandment and the overall winner.
- **Review mode** — a "Review the Ten" button on the title screen lets you walk the class through the commandments before the game starts.

## Stories and References

Every commandment has two paired scriptures so no two playthroughs feel the same:

| Commandment | Primary Story | "Steal" Story |
|---|---|---|
| 1. No other gods | Daniel and the Lions' Den (Daniel 6:10) | Abraham Refuses False Gods (Abraham 1:5) |
| 2. No graven images | The Golden Calf (Exodus 32:4) | Abinadi Warns King Noah (Mosiah 13:13) |
| 3. Don't take God's name in vain | The Lord Speaks at Sinai (Exodus 20:7) | A Modern Warning (D&C 63:61) |
| 4. Keep the Sabbath holy | The Lord's Day in Latter-Days (D&C 59:9–10) | Nehemiah Closes the Gates (Nehemiah 13:19) |
| 5. Honor thy father and mother | Nephi Honors His Father (1 Nephi 3:7) | Ruth and Naomi (Ruth 1:16) |
| 6. Thou shalt not kill | Cain and Abel (Moses 5:32) | David Sends Uriah to Battle (2 Samuel 11:15) |
| 7. Be morally clean | Joseph Flees Temptation (Genesis 39:9) | The Sons of Helaman (Alma 53:20) |
| 8. Thou shalt not steal | Achan's Hidden Treasure (Joshua 7:21) | A Modern Commandment (D&C 59:6) |
| 9. Don't bear false witness | The Coat of Many Colors (Genesis 37:32) | Korihor the Anti-Christ (Alma 30:53) |
| 10. Thou shalt not covet | King Noah's Greedy Heart (Mosiah 11:3–4) | Naboth's Vineyard (1 Kings 21:4) |

## Customizing the Game

Want to change story summaries, swap in different scriptures, or adjust the wording? All the game content lives in the `ROUNDS` array near the bottom of `index.html` (search for `const ROUNDS = [`). Each round looks like:

```javascript
{
  commandment: 1,
  stories: [
    {
      title: "Daniel and the Lions' Den",
      source: "Old Testament",
      summary: "...",
      ref: "Daniel 6:10",
      hint: "Old Testament — Daniel, chapter 6, verse 10",
      verse: "...",
      explain: "..."
    },
    {
      // second scripture for the same commandment
    }
  ]
}
```

Just edit the text and reload the page. No build step, no compiling.

## Tech Notes

- One self-contained HTML file. No JavaScript framework, no dependencies, no build.
- All fonts loaded from Google Fonts (Cormorant Garamond, IM Fell English SC, Crimson Pro).
- Works offline once the page loads (fonts may fall back to system serifs without internet).
- Designed mobile-first; scales up nicely on larger screens.

## License

Free to use, modify, and share for Primary, Sunday School, family home evening, seminary, or any other personal or church use. See [LICENSE](LICENSE) for details.

## Contributing

Suggestions and improvements welcome. Open an issue or pull request if you have ideas for additional scripture pairings, story improvements, or new features.
