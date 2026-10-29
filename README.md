# 👠 Happily Ever After, Inc.

> *A funny, mobile-first idle tycoon where you run fairytale and Wonderland businesses, restart your empire with a glass slipper in your pocket, and follow a fourth-wall-breaking, 14-chapter novel narrated by the Cheshire Cat.*

**One file. No ads. No accounts. No tracking. No install.** Open `index.html` and play.

---

## Table of Contents
1. [What is it?](#what-is-it)
2. [Play it / host it on GitHub Pages](#play-it--host-it)
3. [How to play](#how-to-play)
4. [The eleven worlds](#the-eleven-worlds)
5. [Shops, managers and upgrades](#shops-managers-and-upgrades)
6. [Per-world resets](#per-world-resets)
7. [Prestige layer 2: Turn the Page](#prestige-layer-2-turn-the-page)
8. [Plot Twists](#plot-twists)
9. [Crossovers](#crossovers)
10. [The 52-week Event World](#the-52-week-event-world)
11. [Guest stars](#guest-stars)
12. [Trophies](#trophies)
13. [The Cheshire Cat](#the-cheshire-cat)
14. [Longevity systems (no ads)](#longevity-systems-no-ads)
15. [The Story: twelve books, one per world](#the-story-twelve-books-one-per-world)
16. [Numbers and notation](#numbers-and-notation)
17. [Saving, offline earnings and resets](#saving-offline-earnings-and-resets)
18. [Controls and one-handed play](#controls-and-one-handed-play)
19. [Technical notes](#technical-notes)
20. [Tuning the economy](#tuning-the-economy)
21. [Roadmap ideas](#roadmap-ideas)
22. [License](#license)

---

## What is it?

*Happily Ever After, Inc.* is an **Adventure Capitalist–style incremental (idle) game** with a fairytale twist. You inherit a company from your missing great-aunt Hester and run absurd businesses staffed by storybook characters: Three Little Pigs Construction, Red Hood Basket Delivery, Gingerbread Express Sneakers, Mad Hatter Tea & Hat Emporium, Cheshire Cat Grin Insurance, Camel Rental Co., Zeus Lightning Rod Sales, and many more.

What makes it different:

- **Funny first.** Every shop, manager, upgrade, guest, trophy and pop-up is written as a joke about the characters.
- **Twelve economies.** Eleven permanent worlds and the weekly event world each have their own currency, their own shops and their own balance, so no two worlds feel the same.
- **Per-world resets** (every world has its own, so resetting one never touches the others), a Sequel layer on top, **Plot Twists** (over 120 risky random scenarios where you choose) and **Crossovers** (cross-world synergy bonuses).
- **A 52-week event calendar** with a different festival world every week of the year, and rewards that help the whole game.
- **A narrator who knows he is in a game.** The Cheshire Cat comments on your progress, the news, the characters, and you.
- **A real story.** 233 short story installments (about 275 words each) in twelve books, one per world, plus the Cat's Appendix, unlock as you play.
- **Long-term hooks without ads:** Wishing Well, Daily Gift streak, Daily Quests and Flash Days.

Theme: "Gilded Midnight" (and a different look for every world: its own backdrop, pattern, floating particles and shop-panel colours), a deep midnight-indigo base with antique gold, serif titles, and a jewel-toned accent colour for each world, tuned for phones.

## Play it / host it

### Option A: just open it
Download `index.html` and open it in any modern browser (phone or desktop). That is the whole game.

### Option B: GitHub Pages (recommended)
1. Create a new GitHub repository (for example `happily-ever-after-inc`).
2. Upload everything in this folder (`index.html`, `README.md`, `LICENSE`, `.nojekyll`).
3. Go to **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, branch `main`, folder `/ (root)`, and **Save**.
5. After a minute or two your game is live at `https://<your-username>.github.io/<repo-name>/`.
6. On a phone, open the link and use **Add to Home Screen** to make it feel like an app.

Saves live in the browser's `localStorage`, so each device and each browser keeps its own save.

## How to play

1. **Tap a shop** to put it to work. It runs for a few seconds and pays out in that realm's currency.
2. **Buy more copies** of a shop to multiply its income. Costs rise with each copy.
3. **Hire a manager** and the shop works on its own, forever, even while you are away.
4. **Buy upgrades** (per shop and global) to multiply profit.
5. **Hit milestones** (owning certain counts of a shop) for automatic profit boosts.
6. **Open new worlds**. Each one is a real project: spend a pile of the previous world's money, own enough of its reset points and complete enough resets there.
7. **Reset one world at a time** for its permanent bonus, then go further each time.

Goal: open every shop, grow your empire, collect Glass Slippers and Golden Quills, and see how the story ends.

## The eleven worlds

Worlds are meant to take a long time to open, but **there is no reset-count requirement any more.** Each world asks for just two things in the **previous** world: a pile of its cash (which is spent), and a number of its reset points (which you keep). The reset points are the real gate, and they grow slowly, so each new world arrives a few days after the last, and the gap between worlds does not shrink as you go.

| # | World | Currency | Reset point | What it takes to open it (from the previous world) |
|---|-------|----------|-------------|-----------------------------------------------------|
| 1 | **Storybook Forest** | Gold Coins | Glass Slippers | Start |
| 2 | **Wonderland** | Teacups | Unbirthday Candles | Spend 8.1e7 Gold Coins, and own 3 Glass Slippers |
| 3 | **Arabian Bazaar** | Dinars | Genie Lamps | Spend 3.2e8 Teacups, and own 6 Unbirthday Candles |
| 4 | **Camelot & Sherwood** | Crowns | Holy Grails | Spend 9e8 Dinars, and own 10 Genie Lamps |
| 5 | **Olympus Mall** | Drachmas | Golden Laurels | Spend 2.3e11 Crowns, and own 16 Holy Grails |
| 6 | **Frostbite Kingdom** | Snowflakes | Snow Globes | Spend 1.8e14 Drachmas, and own 45 Golden Laurels |
| 7 | **Neverland** | Pixie Dust | Pixie Wings | Spend 2e17 Snowflakes, and own 150 Snow Globes |
| 8 | **Land of Oz** | Emeralds | Emerald Keys | Spend 2.2e20 Pixie Dust, and own 500 Pixie Wings |
| 9 | **Mermaid Lagoon** | Pearls | Sea Shells | Spend 2.3e23 Emeralds, and own 1,600 Emerald Keys |
| 10 | **Sugarplum Sweetland** | Sugar Cubes | Sugar Plums | Spend 2.2e26 Pearls, and own 5,000 Sea Shells |
| 11 | **Dragonspine Peaks** | Embers | Dragon Scales | Spend 2e29 Sugar Cubes, and own 15,000 Sugar Plums |
| 12 | **The Weekly Event World** | Event Tickets | Festival Favor | Always open, changes every week |

Tap a locked world in the top bar and a window shows exactly what it needs and how close you are.

Every world has its own set of businesses, its own manager jokes, its own news ticker, its own twists and its own economy (cost curve, income curve, milestone strength). Early shops are cheap and quick; late shops are slow, huge and expensive.

Sample businesses:

- **Storybook Forest:** Three Little Pigs Construction, Red Hood Basket Delivery, Gingerbread Express Sneakers, and dozens more.
- **Wonderland:** White Rabbit Late-Fee Services, Mad Hatter Tea & Hat Emporium, Cheshire Cat Grin Insurance, and more.
- **Arabian Bazaar:** Camel Rental Co., Ali Baba Cave Storage, Sinbad Seasick Cruises, and more.
- **Camelot & Sherwood:** Excalibur Sword-in-Stone Gift Shop, Round Table Furniture Co., Robin Hood Wealth Redistribution, and more.
- **Olympus Mall:** Zeus Lightning Rod Sales, Hermes Express Delivery, Athena Owl Tutoring, and more.
- **Frostbite Kingdom:** Snow Queen Ice Sculptures, Nutcracker Dental Clinic, Gerda's Rescue Sleighs, and more.
- **Neverland, Oz, Mermaid Lagoon, Sugarplum Sweetland, Dragonspine Peaks:** 30 brand-new businesses each, with their own currencies, managers and jokes.

## Shops, managers and upgrades

- **390 permanent businesses.** The first three worlds have 50 shops each, the other eight permanent worlds have 30 each, and every weekly event has 8.
- **A unique manager per shop**, each with a quote and a personality. Managers automate their shop.
- **20 upgrade tiers per shop**, getting dramatically more powerful and expensive. Late tiers are far-future goals.
- **60 global upgrades per world**, each with a joke name, that boost every shop in that world.
- **Many milestones per shop.** Own certain counts of a shop and it earns automatic profit boosts; the ladder keeps going deep into the thousands.
- A **Buy All** button and a **next best purchase** button keep late-game play quick.

## Per-world resets

**Every world has its own reset, and resetting one never touches the others.** Opening a world is permanent. From then on you can restart that world alone, whenever you like, for reset points that boost it.

- **Storybook Forest:** *Live Happily Ever After* for **Glass Slippers**. Slippers give a permanent profit bonus in **every** world (3% each by default), and they open the late Mystery Shops.
- **Every other world** has its own reset and its own point (Unbirthday Candles, Genie Lamps, Holy Grails, Golden Laurels, Snow Globes, Pixie Wings, Emerald Keys, Sea Shells, Sugar Plums, Dragon Scales). Those points boost **that world** (5% each) and unlock **that world's** Mystery Shops.
- **World Mastery:** every reset you complete in any world adds a small permanent bonus to all worlds.
- The **Ever After** tab has one card per opened world showing what you would gain, plus the Sequel card.
- Points are earned from that world's lifetime earnings (roughly a square root, scaled for each world's economy), so later resets are steady rather than explosive.

## Prestige layer 2: Turn the Page

Once you have enough slippers (1,000 or more), you can **write a Sequel**. A Sequel is the only thing that resets everything.

- You trade in your slippers for **Golden Quills**.
- Each Quill gives **+25% profit** to everything.
- Quills are also spent in the **Quill Perks** shop.

### Quill Perks

| Perk | Effect |
|------|--------|
| 👠 Sturdier Soles | +1% profit per slipper, per level |
| 🎟️ Cobbler Coupons | Mystery shops need 20% fewer slippers, per level |
| 🚀 Head Start | Start every ending with a pile of gold (x100 per level) |
| 🧑‍💼 Union Busters | Shops hire their manager free when first opened |
| 🌙 Night Shift Elves | +50% offline earnings, per level |
| 🎭 Guest List | Guest stars visit 15% more often, per level |
| 🛡️ Plot Armor | Plot Twist losses are halved, per level |
| 🌀 Synergy Seminar | Crossover bonuses x1.5, per level |

## Plot Twists

Random story events pop up (every few minutes) and make you **choose**, with risk on both sides. There are now **over 120 scenarios**:

- **Every world has its own pool of 8 twists** that fit its story: the woodcutter's union in the Forest, the Queen's croquet match in Wonderland, the genie's fine print in the Bazaar, Zeus's tantrum in Olympus, the Snow Queen's mirror, Hook's meeting in Neverland, the Yellow Brick Road closing in Oz, Ursula's contract in the Lagoon, the gumdrop avalanche in Sweetland, the dragon's stapler hoard in Dragonspine, and many more.
- **The event world has its own pool** (stuck mascots, raffle trouble, confetti cannons, surprise VIPs).
- **25 general twists** can happen anywhere (the fourth wall leaking, the Narrator's typo, a door appearing in the office, a talking pig applying for a job).

Outcomes can be a cash windfall, a temporary profit buff, or a loss. Recently seen twists are not repeated. The Plot Armor perk halves the losses.

## Crossovers

There are **10 Crossover partnerships**, such as *The Great Commute Collab* (Pigs, Rabbits and Camels) or *Vertical Transit Alliance* (Beanstalks, Spas and Carpets). Own the required shops from different realms and you earn a permanent profit bonus across the game. Synergy Seminar makes these bonuses stronger.

## The 52-week Event World

Every week of the year a different **festival world** opens. Each is a self-contained mini-economy with:

- its own currency (Event Tickets), its own **8 shops**, its own pricing and speed,
- **bronze, silver and gold goals**, shown as three big chips in the event banner: the chip you have reached turns green and says *REACHED ✓*, and the next goal glows,
- a **Goal Reached celebration** every time you cross a goal: a medal pops up in a window with the stamp, your ticket total and what the next goal is (it can't be missed),
- **Stamps** for finishing, and a **game-wide reward** (the Stamp Dividend) that gives a permanent bonus to the main game.

**Events have their own reset: the Encore.** Restart the event shops without touching anything else in the game. You keep your goal progress and gain **Festival Favors** (+12% event profit each).

The calendar includes (a sample of all 52): New Year's Fable-Fest, Snow Queen's Frostival, Dwarf Mining Rush, The Beast's Banquet, Glass Slipper Valentine Ball, Sleeping Beauty's Hundred-Year Nap, Mad Hatter's Winter Tea, Leprechaun Gold Rush, Jack's Beanstalk Planting Week, Frog Prince Pond Party, Alice's Croquet Open, Pied Piper's Spring Parade, Cheshire Grin-a-Thon, Three Bears Porridge Cook-Off, Rapunzel's Long Hair Weekend, Sinbad's Seven Seas Week, Tortoise & Hare Summer Games, Queen of Hearts Tart Festival, Jabberwocky Gala, Looking-Glass Chess Tournament, Pinocchio Honest Week, Rumpelstiltskin Gold Spin, Haunted Gingerbread Manor, Witch's Cauldron Week, Sleepy Hollow Pumpkin Patch, Wonderland Unbirthday Spectacular, Cinderella's Midnight Rush, Nutcracker Toy Soldier March, Christmas Elf Overtime, and **The Happily Ever After Finale**.

The current week is chosen from the date, so the calendar rolls on its own.

## Guest stars

**80 guest stars** wander by (every few minutes, at random), each with a joke and a reward when you tap them. Rewards include cash, temporary profit boosts, Plot Twists, and Wishing Well charges. The Guest List perk makes them appear more often.

**The Guest Book pays out.** Meet 20, 40 and 60 different guests for wishes and boosts. **Meet every single guest and you get a golden title, 10 wishes and all profit ×1.5 forever**, which survives every reset, ending and sequel.

## Trophies

**82 trophies** track milestones across every system: shops owned, money earned, worlds opened, world resets, guests met, slippers, quills, twists survived, chapters read, streak days, and more. Each has a funny description and adds a small permanent profit bonus.

## The Cheshire Cat

The Cat floats at the top of the screen as your narrator. He:

- **Reacts to your progress:** hires, buys, milestones, restarts, new realms.
- **Reports the news:** each world has its own satirical headlines.
- **Shares opinions and sayings** about the characters.
- **Breaks the fourth wall:** he talks about the game, the buttons, the story, and **you** the player. He notices how long you were away, what time of day it is, how many times you have opened the game, and how many chapters you have read.
- **Reacts to being poked.** Tap him repeatedly and he gets personal.

Messages are held on screen for 10 to 16 seconds, queued by priority, and templated so they fit what is actually happening. Every world and the event world have their own news and opinion pools, and the Cat now draws from **many hundreds of lines** using a shuffle-bag: he goes through a whole pool before any line can come back, so he does not repeat himself.

## Longevity systems (no ads)

The game never shows ads and never asks you to watch one. Instead, it has four free systems that reward coming back. They were deliberately made gentler in v8 so they never overshadow normal play.

### 🌠 Wishing Well
- Hold up to **4 wishes**.
- Each wish gives **×1.5 profit for 1 hour**.
- A new wish regenerates every **3 hours**, banking up to **12 hours** worth.
- Wishes can also come from quests, the Guest Book and some guest stars.

### 🎁 Daily Gift and Streak
- Claim a gift once per day.
- Your streak adds **+2% profit per day**, up to **20 days** (+40%).
- **One missed day is forgiven.**

### 🎴 Charm Album and Story Packs

A second reason to come back, besides wishes. You start with no packs. A **story pack** arrives every **8 hours** (you can hold 3), and every third day of a Daily Gift streak adds one more. Each pack holds one **charm** from a world you have already opened. There are **66 charms**: six per world (four common, one rare at about 14%, one legendary at about 3%), all with silly names like *Sword Not Quite in the Stone* and *A Shadow That Stayed*.

- Every charm adds permanent profit to its world, and duplicates **level it up** (to level 5).
- A **full set of six** gives that world another ×1.25. A **full album** gives ×1.3 in every world.
- Every 12th pack is at least Rare, and a 7-day streak adds a pack that is guaranteed Rare or better.
- A maxed charm turns into 30 minutes of ×1.5 profit instead of being wasted.
- In my simulation, finishing a single world's six charms takes about 32 packs even when it is the only world open, and the packs spread across every world you have opened, so the whole album is a months-long collection.

Charms survive every reset, ending and sequel.

### 📋 Daily Quests
- Three new quests every day (for example, "Tap shops to work 50 times", "Make 3 wishes at the well", "Buy 6 upgrades").
- Rewards: a free wish, 15 minutes of instant income, or a 30-minute boost.

### ⚡ Flash Days
- Each day highlights one of the eleven worlds for **×1.5 profit**; the highlighted world rotates through the whole map.
- Every seventh day is the **Grand Gala**: every world gets **×1.25**.

These stack with the other multipliers, so check back often. If you ever find the game too fast, these constants in the source are the first to lower.

## The Story: twelve books, one per world

*Happily Ever After, Inc.* is a full-length story hidden in the **Storybook → Story** tab: **233 short installments (about 275 words each, so no long reads)**, narrated in the first person by the Cheshire Cat. **Every world has its own book**, and a book opens when you open its world:

| Book | World | Title |
|------|-------|-------|
| One | Storybook Forest | The Inheritance (the original opening chapters) |
| Two | Wonderland | Down the Rabbit Hole, Slightly Late (the Hatter, the Hare and a Queen with paperwork) |
| Three | Arabian Bazaar | One Thousand and One Nights of Cash Flow (a genie with terms, a Vizier with a spreadsheet) |
| Four | Camelot & Sherwood | The Table That Was Round (an open mic, a cheap cup) |
| Five | Olympus Mall | The Mall at the Top of the Mountain (Hermes, the Muses, a very long lease) |
| Six | Frostbite Kingdom | The Girl Who Wrote Herself Out (the finale of the first story, *The Last Page*) |
| Seven | Neverland | The Second Star on the Right (the Margin opens) |
| Eight | Land of Oz | The Road That Goes in a Circle |
| Nine | Mermaid Lagoon | Under the Sea (Terms Apply) |
| Ten | Sugarplum Sweetland | The Kingdom That Never Stopped Eating |
| Eleven | Dragonspine Peaks | The Mountain Made of Spines (with the epilogue) |
| Twelve | The Weekly Event World | Fifty-Two Weeks of Trouble (a calendar, a mascot, a pumpkin) |
| Appendix | (your play style) | The Cat's Appendix: short interludes unlocked by wishes, streaks, guests, twists, quills and trophies |

Each book is split into many small installments that unlock as you play (a milestone in that world, then more by keeping busy). The Story tab shows each book as a shelf with a progress bar, hides installments you have already read (with a button to show them), and tells you what unlocks the next one. A "New story" pill appears when something is ready. Old saves are converted automatically, so everything you had read stays read.

## Why the numbers slow down (the math)

Idle games feel fast when two things grow together: **cost grows exponentially** (each shop costs about 7% more than the last), while **income grows only linearly** with how many you own. That alone is a nice, slow curve. The trouble starts when every upgrade and milestone *multiplies* income too. Ten multipliers of 4x make 1,000,000x, and cost cannot keep up, so you fly through the numbers.

This version adds three brakes, all visible in the source:

1. **Bounded multiplier ladders.** Shop upgrades, global upgrades and milestones now use small steps (1.5x up to 12x for shop upgrades) instead of huge ones.
2. **Diminishing returns.** Your permanent multipliers are added up as normal until they reach 25x. Beyond that, only a fraction counts: roughly `25 × (M / 25)^0.55`. A 10,000x stack acts like about 700x. The constants are `DAMP_M0` and `DAMP_B`.
3. **Saturation (per run).** The more you earn in one run of a world, the less each coin of profit is worth, with the effect `(lifetime / 1000)^-0.18` once you pass the reference. Resetting a world clears it, so resets still feel fast and rewarding. The constants are `SAT_REF` and `SAT_G`.

On top of that, base income is 20% lower (`REVF = 0.20`) and reset points are a square-root of lifetime earnings, so each extra point costs more than the last. In my simulations, even a perfectly efficient player takes roughly nine minutes to reach 1 thousand lifetime earnings, a couple of hours to reach a million, and days to reach a billion, with every further jump taking longer than the one before.

Sources for the approach: the Game Developer series on the math of idle games (cost curves with exponential growth, linear income, prestige by roots).

## Numbers and notation

Numbers get ridiculous. The game uses:

- Short names (K, M, B, T, Qa, Qi, Sx, Sp, Oc, No, Dc),
- then **doubled-letter notation** (aa, ab, ac ...) for the deep late game,
- and an optional **scientific notation** toggle in settings.

Cash on screen **rolls with three decimal places** (for example `8.357 million`) so you always see it moving, even between big jumps. Values are clamped far below the JavaScript limit to avoid overflow.

## Saving, offline earnings and resets

- **Autosave** to `localStorage` under the key `haec2` (save version 8).
- **Offline earnings:** shops with managers keep earning while you are away; Night Shift Elves raises it.
- **What survives a world reset:** everything in the other worlds. Only the world you reset restarts.
- **What survives a Sequel:** slippers are traded for quills; quills, perks, trophies, guests, story progress, wishes, streak, quests and stats are kept.
- **Upgrading from an older version:** the economy was rebalanced in v8, so shop progress restarts once. Trophies, the guest book, event stamps, story progress and settings are kept.
- **Resetting everything** is available in Storybook → settings. It asks first.
- If you clear browser data or switch browsers, you start fresh. There is no cloud save.

## Controls and one-handed play

- Tabs along the bottom: **Shops, Managers, Upgrades, Events, Storybook, Ever After** (the restart screen).
- A **one-handed quick bar** puts **Work** (tap every shop), the **next best purchase**, and **Buy All** in thumb reach.
- Pop-up toasts appear at the bottom so they never cover your cash.
- Sound can be switched off in settings.

## Technical notes

- A single self-contained `index.html` (about 480 KB). Plain HTML, CSS and JavaScript. No frameworks, no build step, no external requests.
- Game loop: `setInterval` every 100 ms; UI uses signature-based re-rendering to stay light on phones.
- Economy: per-realm tables generated from parameters (`ECO_P`) with deterministic hash jitter; per-event economies generated from a seeded random per event index (`evEconomy`).
- Bot simulators were used offline to tune pacing and event medal thresholds.
- Tested with jsdom smoke tests (no runtime errors) and on mobile layouts.

## Tuning the economy

All numbers live in the source and are easy to adjust:

- Early-game speed: base costs and the `CK` cost growth multiplier.
- Per-realm feel: the `ECO_P` parameters (`s` scale, `ro` rate, `tm` time, `ce` cost exponent, `mg` milestone gain, `cs`, `rs`).
- Slipper strength: `SLIP_BONUS` and the `potSlip` formula.
- Global slowdown: `REVF` (all worlds) and `EVF` (events).
- World gating: `UNLOCK_COST` and `UNLOCK_PT` (there is no reset-count gate), plus the `PT_REF0` table for how fast each world earns reset points.
- Dampening: `DAMP_M0`, `DAMP_B`, `SAT_REF`, `SAT_G`, and the `UP_MULT` and `GUP_MULT` ladders.
- Optional boosts: `WISH_MAX`, `WISH_REGEN`, the wish multiplier, streak percentage, and the `flash()` function.
- Event difficulty: the `EVTH` bronze, silver and gold thresholds.

Search the file for these names. The first run is designed to be slow: the first shops are quick, but the later shops, world unlocks and resets are long-term goals.

## Roadmap ideas

- Cloud save or export and import codes
- More worlds (Atlantis, the Moon, the Land of Nod) and more event weeks
- Sequel 2 and 3 story arcs
- Achievements with in-game badges on the home screen
- Localization

## License

MIT. See [LICENSE](LICENSE). Fairytale characters used here come from public-domain folklore and classic literature; all jokes and story text are original to this project.


## Version 11 notes

- **Speed doubling.** Every shop doubles its speed at 25, 50, 75 and 100 owned. The shop panel shows the current speed and the next milestone.
- **Gentler diminishing returns.** The late-game saturation curve was eased (reference raised to 1e4), so the first reset arrives sooner.
- **Multi-tab guard.** Each browser tab tags its saves with a revision. A stale tab or old copy of the game can no longer overwrite newer progress (this was the likely cause of shop counts appearing to drop). Close any other open copies of the game.
- **Little Fortunes.** Hundreds of random pop-ups (thousands of combinations) arrive every 5 to 14 minutes with a cash gift, a short luck buff, or a free wish boost. Take it or dismiss it.
- **Calmer, more random pacing.** The Cat speaks every ~20 to 70 seconds (sometimes longer), Plot Twists every ~6 to 25 minutes, and guest stars every ~2.5 to 12 minutes. Pop-ups never interrupt an open window and pause while the tab is hidden.
- **Many more Cat lines** for the wall, status, player and idle pools.


## Version 12 notes

- **New title banner.** A gilded crest (open storybook under a crown, with twinkling stars and a slowly turning ring) sits beside a larger, embossed gold title. The header glow takes on the colour of the world you are in.
- **Time Warps (Storybook → ⏳ Time Warp).** Instantly collect 1, 4, 6, 8, 12 or 24 hours of earnings from the world you are in. Warps are bought with **Hourglass Sand**, a currency you only earn by playing (no ads, no real money):

| Warp | Sand cost |
|---|---|
| 🕰️ Pocket Watch, 1 hour | 12 |
| ⏳ Hourglass, 4 hours | 42 |
| 🕛 Mantel Clock, 6 hours | 60 |
| 🛎️ Grandfather Clock, 8 hours | 78 |
| 🐦 Cuckoo Tower, 12 hours | 110 |
| 🗼 Clock Tower, 1 day | 200 |

- **Where sand comes from:** the Daily Gift (6 plus streak days, up to 20), daily quests (5 / 8 / 12), guest stars (1 to 2 each), every trophy (3), every story installment read (1), Little Fortunes (8 to 20), and every Happily Ever After (10 and up). A 5-day streak also gifts a free 1-hour warp and a 7-day streak a free 4-hour warp.
- You can hold up to 9 of each size. Warps of 6 hours or more ask for confirmation, and they do not work in the weekly Festival world, so events stay fair.
- Four new trophies: Skipping Ahead, Chronic Skipper, Time Is Money, Sandman.

## Version 13 notes: every world has its own difficulty

Each world already had its own prices, speeds and payouts. Now each also has its own **difficulty**, shown as a badge at the top of its shop list. It changes income, how hard the late-game slowdown bites, how gentle the multiplier dampening is, and how much lifetime gold the first reset point needs.

| World | Difficulty | Feel |
|---|---|---|
| Storybook Forest | Gentle | Friendly start, quick resets |
| Wonderland | Easy | Cheap, quick and generous |
| Arabian Bazaar | Normal | Slow, fat paydays |
| Camelot | Hard | Steep tiers |
| Olympus | Hard | Feast and famine |
| Frostbite | Brutal | Fast bursts, cruel growth |
| Neverland | Easy | Flighty and quick |
| Oz | Normal | Long road, fat rewards |
| Mermaid Lagoon | Hard | Deep and pricey |
| Sweetland | Easy | Tiny, rapid sugar hits |
| Dragonspine | Brutal | Rare giant hoards |

In a 3-hour test with the same bot, lifetime earnings (relative to each world's own scale) ranged from about 0.35× the Forest in the Brutal worlds to about 3× in the Easy ones. Existing saves keep their progress; the new numbers apply immediately.
