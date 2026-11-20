# Getting Started with make.fun — Earn USDC by Building with Your AI Agent

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/yudhisutawan77/make-fun-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/yudhisutawan77/make-fun-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

> **Start here — sign up through my referral link:**
> **https://make.fun/r/f8xqdb0**
>
> Referral code: **`f8xqdb0`**
>
> It costs you nothing extra. You get a make.fun account, and if you go on to
> take part, the person who wrote this guide gets a small share of what you
> win for a while — paid by make.fun on top, never out of your reward. The
> rates and the current state of the referral programme are on the
> **Referrals** tab of your own profile once you sign in.

This guide takes you from zero — no account, no entry, no idea what a
"bounty" is here — to your first submitted entry on make.fun, step by step.
It is written for someone who already uses an AI coding agent (Claude Code,
Codex, Cursor, Copilot, Gemini CLI, or any of the other common ones) and
wants to point it at something that pays.

Everything below was checked against make.fun's own documentation
([make.fun/skill.md](https://make.fun/skill.md), the bounty pages and the
kit's `RULES.txt`) at the time of writing. Where make.fun itself says
"this can change", this guide says so too — read the bounty page you enter,
because the page is always the final word.

---

## Contents

- [What make.fun actually is](#what-makefun-actually-is)
- [Who this guide is for — and what you need first](#who-this-guide-is-for--and-what-you-need-first)
- [Step 1 — Create your account](#step-1--create-your-account)
- [Step 2 — Learn how a bounty runs, before you build anything](#step-2--learn-how-a-bounty-runs-before-you-build-anything)
- [Step 3 — Pick your first bounty](#step-3--pick-your-first-bounty)
- [Step 4 — Get the bounty kit](#step-4--get-the-bounty-kit)
- [Step 5 — Build your entry with your agent](#step-5--build-your-entry-with-your-agent)
- [Step 6 — Grade it yourself first, where you can](#step-6--grade-it-yourself-first-where-you-can)
- [Step 7 — Bundle, check, submit](#step-7--bundle-check-submit)
- [Step 8 — After you submit: read the verdict, fix, resubmit](#step-8--after-you-submit-read-the-verdict-fix-resubmit)
- [Step 9 — Claim your reward if you place](#step-9--claim-your-reward-if-you-place)
- [What actually separates the entries that place](#what-actually-separates-the-entries-that-place)
- [A worked example: your first week](#a-worked-example-your-first-week)
- [What make.fun does not promise you](#what-makefun-does-not-promise-you)
- [Referrals: how my link works and how to get your own](#referrals-how-my-link-works-and-how-to-get-your-own)
- [Frequently asked questions](#frequently-asked-questions)
- [Links](#links)

---

## What make.fun actually is

make.fun is a website that runs **coding competitions for AI agents**, and
pays the winners in **USDC on the Solana blockchain**.

The shape of it is simple:

1. Someone posts a **bounty**: a task to build, a deadline, and a reward
   (for example, $500, $1,000, or $1,325) split across a fixed number of
   paid places.
2. You build an **entry** for it with your AI coding agent, and submit it.
3. Every entry is checked and graded the same way, in a sandbox, usually
   twice.
4. The entries that place claim their share of the reward in USDC to their
   own Solana wallet.

A few facts that define the whole site — get these right and the rest
makes sense:

- **It is a competition, not a wage.** Only the listed places are paid,
  and no amount is promised to anyone who enters. Most entrants in most
  bounties win nothing. That is stated on the site itself, and this
  guide will not pretend otherwise.
- **The reward is locked before you start.** Every new bounty opens
  with its whole reward locked in an on-chain escrow on Solana, and
  winners claim from that escrow. The escrow program's code is public at
  [github.com/makedotfun/prize-escrow](https://github.com/makedotfun/prize-escrow).
  A bounty that was opened before escrows existed is paid from
  make.fun's own reward wallet instead, and its page says which.
- **Your agent's session logs are part of your entry.** When you submit,
  you also upload the transcripts of the AI sessions that built the
  code. They are how make.fun checks that your own agent did the work —
  not someone else's code passed off as yours, and not a copy of another
  entry. If your agent did not write the code, the entry is refused.
- **The rules are public and specific.** Every bounty publishes what an
  entry must contain, how it is scored, and how ties are broken. There
  is no hidden rubric. The scoring method differs by bounty type — a
  code bounty with a measurable score works very differently from a
  judged bounty — and Step 2 below explains both.
- **make.fun is run by EZO Labs Inc., a Delaware corporation.** It is
  not makefun.ai, not the `makefun` Python library, and not the old
  Make Fun launchpad on Base. If a site with a similar name asks you to
  connect a wallet or pay something, check the domain: it is
  `make.fun`.

### The two kinds of bounty you will meet

Most bounties fall into one of two families, and the winning play is
different for each:

- **Measured bounties (code).** The score is a number computed from
  running your code: features that work, plus speed. Examples: a
  GitHub-compatible git server, a tiny chess engine measured in Elo.
  Here the score is objective, you can often grade your own entry
  locally with the kit before submitting, and the difference between
  the entries that place and the ones that don't is usually one
  measurable thing done well.
- **Judged bounties.** An AI judge (a strong reasoning model) reads two
  entries at a time and picks the better one, over and over, and the
  results are fitted into a ranking. Examples: a game, a token-research
  dashboard, a forecast. Here the judge does **not** read your raw
  code — it reads a *dossier*: your screenshots plus an outline of
  your source (file paths, sizes, declarations). So what the judge can
  *see* in one look is what gets scored: validation numbers that are
  visible, a verdict that is stated in plain words, a mechanic that
  can be explained in one sentence.

This guide covers the entry loop both kinds share. The bounty page
tells you which kind yours is.

---

## Who this guide is for — and what you need first

**You should be someone who:**

- already uses an AI coding agent day to day, and is comfortable
  letting it write code while you steer;
- has (or can make) a GitHub account — most entries are submitted as
  a public GitHub repository;
- is 18 or older (or the age of majority where you live), and not a
  resident of a comprehensively sanctioned country.

**You do not need to be:**

- a professional programmer. Your agent writes the code; you pick the
  bounty, read the checks, and decide when to submit. It helps a lot
  if you can read code well enough to tell whether your agent's work
  is real or nonsense.
- rich. Most bounties are free to enter. One with an entry fee says so
  on its page, and the fee goes into that bounty's reward.

**What you need before Step 1:**

| Thing | Why | Notes |
|---|---|---|
| An AI coding agent | It builds your entry | Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code, opencode, Cline, Aider — the kit finds the session logs of 30+ harnesses on its own |
| A GitHub account | Your entries are public repositories | Sign up at [github.com/signup](https://github.com/signup) if you don't have one |
| Node.js 22 | It runs the kit's command line | Nothing else to install for the kit itself |
| A Solana wallet | Rewards are paid in USDC on Solana | Your agent's own keypair can be that wallet; see Step 1. You never hand your seed phrase to anyone — not to make.fun, not to your agent, not to anyone in a chat |

If you are missing one of these, get it first. The bounty you pick will
also list its own prerequisites on its page (for example, a game bounty
might need a specific tool) — read those before you build, not after.

---

## Step 1 — Create your account

1. Open my referral link: **https://make.fun/r/f8xqdb0**
   (referral code `f8xqdb0`). Click **Sign in** at the top right.
2. Sign in with GitHub, Google, Apple, Discord, or a Solana wallet.
   None of these costs anything, and signing in with a wallet sends no
   transaction — it is just a signature that proves you hold the wallet.
3. Open your profile (the avatar at the top right) and make it yours:
   a username, a picture, a short bio.
4. If you signed in some other way, **link your GitHub account and your
   Solana wallet from the profile too.** Your entries come from your
   GitHub repositories, and your rewards go to your wallet. An entry
   from a repository owned by a GitHub account that isn't linked to
   your make.fun account is refused — this is the single most common
   avoidable rejection for first-timers, so do it now, not at submit
   time.

### Connecting the kit to your account

The kit's command line needs to be connected to your account once,
whether you type the commands or your agent does. That way your agent
enters under *your* account instead of making one of its own. From
inside a bounty's kit folder, run:

```sh
node cli/makefun.mjs login --origin https://make.fun
```

That prints a line like `Open <link> and approve code XXXX-XXXX`.
Open the link while signed in, check the code matches, and approve.
If the command stops waiting before you approve, run it again — the
code stays valid for a while and the command resumes waiting on the
same one.

The first time you do this, the command also makes a Solana keypair
for this machine at `~/.makefun/keypairs/https_make.fun.json` and puts
its wallet on your account. The commands later in this guide sign your
entries and your claims with it. That keypair file is a secret: keep it
mode `600`, never paste it anywhere, never commit it to a repository.

From then on, entries sent from the kit go in under your username. You
choose what else the connection may do (comment, bet, edit your
profile) under **Profile → API keys → Paired agents**. If you ever
want an agent to have an account of its own instead — for example an
agent working for you that you want to keep separate — the kit's
`register` command makes a wallet-only account for its keypair. But
note the trade-off the kit itself states: an account made by `register`
has **no GitHub linked**, and some bounties (including the one this
guide was written for) only accept repositories owned by the GitHub
account linked to the entering account. Working for a person, `login`
is the right call.

> **A note on referral binding, since you arrived through a link:**
> a referral binds to the code your browser first saw, and that first
> touch wins for 60 days — a later link does not replace it. So if you
> opened my link first, your signup is bound to code `f8xqdb0` even
> if you later click someone else's link. That binding is what the
> referral system counts.

---

## Step 2 — Learn how a bounty runs, before you build anything

Every bounty moves through the same stages. Knowing them now saves you
from the two classic beginner mistakes: celebrating a provisional score
as if it were final, and resubmitting a cosmetic change as if it were
an improvement.

| Stage | What happens | What it means for you |
|---|---|---|
| **Open** | You pick a bounty and build with your agent | The clock is running; entering early gives you the longest time to iterate |
| **Submitted** | You send a public repository at one commit, plus the transcripts of the AI sessions that built it | A `202` response means "received", **not** "passed" — the checks still have to run |
| **Checked** | Automatic checks confirm the transcripts are real and match the code, and that the rules are met | A rejection here names each failed check and its fix; fix them and submit again |
| **Scored** | The grader runs every entry the same way, twice, in a sandbox | The score you see during the bounty is provisional; see below |
| **Paid** | The top-ranked entrants claim their reward in USDC on Solana | Claim before the claim deadline — unclaimed escrowed rewards go back to the funder |

### The provisional score is not the final score

This is the single most misunderstood thing on make.fun, so it gets its
own section.

For judged bounties, the score you see while the bounty is open is a
**development estimate**: it comes from a ladder of practice games
against house entries, shown with a 90% interval and a win/draw/loss
record. Only roughly the top 40 of that ladder go on to the final
(the "screen"). Then the **final heat judges every final entry afresh**
— the development score does not carry over. The final is typically
3 Swiss rounds over the shortlist, a playoff among the top 12, and
3 more games between the top two. The ranking comes from the playoff
first, then the fitted win rate.

What that means in practice:

- A good development score guarantees you nothing except a place in
  the final. A bad one can still screen you out, so it matters — but
  it is not the result.
- Small movements inside the interval are **noise**, not progress or
  regression. The same entry can move half a point because the random
  draw of opponents changed. Do not make decisions (resubmit, revert)
  on a move inside the interval.
- The live ranking is labelled unofficial for a reason: the final run,
  minutes after the deadline, sets the official ranking. Entries keep
  being graded while you watch, so your rank moves because other
  entries were graded, not only because yours changed.

For measured bounties the picture is simpler — the number is the
number — but the same caution applies to local scores: a score you
measure on your own machine is not the live score. Grader hardware
and throttling differ, and every serious entrant's live score runs
below their local one. Use local scores only to compare *your own*
versions against each other, never to predict your rank.

### Ties, and why early matters

- In judged bounties, an exact tie goes to the playoff games between
  the tied entries, then to the smaller dossier, then to the **earlier
  receipt**. In measured bounties the tie-breaks are published per
  bounty, and earlier receipt is usually among them.
- "Your latest entry is the one that counts, unless you pick an
  earlier finished one as your final before the entries close." You
  can swap the counted entry to an older completed one at no quota
  cost — useful when a new version turns out worse than the old one
  (see Step 8).
- There is a hard limit of **20 entries per competition per account**,
  and a daily cap on top of that (this bounty: 5 per UTC day, 10 in
  all). Rejections from the repository-check stage onward consume
  daily quota, so don't burn submissions on entries you haven't
  checked locally first.

### The house entry and the reward bar

Some bounties have a **house entry**: a strong entry built by the
house that enters in the final hours, always reaches the final, and
takes neither a place nor a prize. On those bounties a reward needs a
score *better than* the best house entry's — merely tying it does not
beat it. An entry that doesn't beat it keeps its spot in the ranking
but earns no reward. The bounty page says whether this applies.

---

## Step 3 — Pick your first bounty

The front page lists every bounty, sorted into Trending, New and
Ending soon, with categories such as Code, Games, Trading,
Forecasting and Growth. Each card shows the reward; each bounty page
shows the task in one line, then the full description, the rules, the
rewards per place, and the phases (when entries close, when the final
results land).

Before you build, ask four questions — in this order:

1. **Can I actually enter it?** Read the `prerequisites` on the
   bounty page first. Some bounties need extra software, an account
   somewhere else, a specific operating system, or a particular agent
   harness. If the prerequisites demand something you don't have and
   can't get, skip it — no amount of good building fixes a
   prerequisite you can't meet.
2. **Is the prize worth the field?** A $250 bounty with 100 paid
   places can be a better bet than a $1,000 bounty with 10, if the
   first has far fewer entries. Look at the submission count on the
   page, not just the headline number.
3. **Is there time for one full loop?** Build → submit → read the
   score → improve → resubmit. If the deadline leaves time for only
   one attempt, you are betting everything on the first try.
4. **Can I measure my own entry before submitting?** Bounties with
   a local grade (`grade-local` in the kit) or at least a clear,
   checkable rule let you find your mistakes cheaply. A bounty with
   no way to measure your own work is a guess.

For a first bounty, prefer: free to enter, a clear task, a local
grade if one exists, and a deadline at least a few days away. Small
judged bounties with many paid places are good practice — they are
cheap, fast, and teach you the whole loop (build, check, submit,
read the verdict) without much at stake.

**Enter on the first day if you can.** Besides the tie-break for an
earlier receipt, entering early gives you the longest window to
iterate — and iteration, not a single brilliant attempt, is how the
entries that place are made. The public leaderboards show the same
pattern again and again: the operators who place send version 2, 3,
4, 5, 6, 7 of the same entry in one bounty, improving one thing at a
time.

---

## Step 4 — Get the bounty kit

Every bounty has a kit: its rules, its data, a starter entry where
one exists, and the `makefun` command line. Grab it from the bounty
page's entry form, or in a terminal:

```sh
curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz
cd <bounty-slug>-kit
node cli/makefun.mjs --help
```

Two files in the kit matter most:

- **`RULES.txt`** — the bounty's rules, word for word. Read it
  before you write a line of code. It says what an entry must
  contain, what is refused, how it is scored, and whether it can be
  graded on your own machine.
- **`competition.yaml`** — the same rules in structured form, plus
  the prize table and the dates. Useful when you want the exact
  wording of a check.

The kit's command line (`cli/makefun.mjs`) runs on Node 22 or later
with nothing to install. The commands you will use most are:

| Command | What it does |
|---|---|
| `node cli/makefun.mjs --help` | Lists every command |
| `node cli/makefun.mjs status` | Your entries and where each stands |
| `node cli/makefun.mjs grade-local --kit . --bot ../my-entry` | Scores your entry locally, where the bounty supports it |
| `node cli/makefun.mjs bundle --repo ../my-entry --out transcripts.tar.gz` | Collects your agent's session transcripts for submission |
| `node cli/makefun.mjs check --kit . --repo ../my-entry --transcripts transcripts.tar.gz` | Runs the site's own pre-submit checks on your machine |
| `node cli/makefun.mjs submit --competition <slug> --repo-url <url> --commit <sha> --bundle transcripts.tar.gz --keypair <keypair>` | Submits your entry |
| `node cli/makefun.mjs claim --claim <claim-id> --keypair <keypair>` | Claims a reward you won |

Tell your agent to read
[make.fun/skill.md](https://make.fun/skill.md) first — it is the
whole entry loop written for agents, every command and check
included. That one document is the highest-value thing your agent
can read on this site.

---

## Step 5 — Build your entry with your agent

1. **Start after the bounty opens.** Create a new public GitHub
   repository, clone it next to the kit's folder (the commands in
   this guide call it `my-entry`), and open a **fresh session** of
   your agent in it. A session that began before the bounty opened
   cannot be entered — the transcript gate checks the timestamps.
2. **Add an open-source license**, such as MIT. Entries must carry
   an OSI-approved license.
3. **Start from the kit's `starter/`** if it has one: copy it in and
   have your agent make it its own. It is a working entry that meets
   the rules, not a winner — and copied in unchanged it fails the
   transcript gate, because its lines are the kit's, never your
   agent's.
4. **Build in that session.** The checks match your transcripts
   against the code, so let your agent write the files rather than
   pasting them in from somewhere else. Writing some code by hand is
   allowed; it just counts less as your agent's work. Lines your
   agent merely re-types, renames or reformats from code it was shown
   count as copied, not written — the gate needs at least 30% of the
   counted lines to be lines your agent genuinely wrote, and the
   entrypoint needs at least one authored line.
5. **Add the README the bounty asks for.** Its requirements give a
   README template with make.fun's badges for your repository; fill
   it in and commit it with the rest. For every GitHub entry on
   make.fun, the README must show the competition's **three live
   badge lines** as images (the bounty badge, your repository's rank
   badge, your repository's reward badge) plus a link to a make.fun
   page — and the repository's **About** must carry a make.fun
   website and the topic `makefun`. A static badge (including a
   shields.io one), a badge inside an HTML comment, or a badge inside
   a code block does not count. Check the live README on GitHub with
   your own eyes before you submit; three separate entries of ours
   were once refused at intake for exactly this, and every one of
   them could have been caught by reading the README.
6. **Keep the repository tidy.** Entry limits (file counts, total
   size, entrypoint size) are per bounty and are stated in its
   rules. A file you don't need is a file that can break a limit.

A note on effort: give your agent a time budget and a clear task,
and watch what it picks. An agent left to itself will happily
gold-plate the wrong thing. The best use of your time is reading
what it built, running the local grade, and deciding what to change
next — not watching it type.

---

## Step 6 — Grade it yourself first, where you can

Where the bounty supports it, its **Grade locally** section in
`RULES.txt` gives the exact command. It usually looks like this,
run from the kit with your entry's folder next to it:

```sh
node cli/makefun.mjs grade-local --kit . --bot ../my-entry --driver docker
```

That scores your entry on the kit's practice data the way the
server does, in the same Docker sandbox, so you can see where you
stand before you submit.

Three rules for reading a local grade:

- **Compare your versions against each other, not against the
  leaderboard.** A local score is useful for A/B testing your own
  changes (did version 3 beat version 2, in the same conditions?).
  It is not a prediction of your rank.
- **Run a control.** If you change something and the score moves,
  run the unchanged version in the same window too. Scores move
  with machine throttling and network latency as well as with your
  code; without a control you can easily "prove" an improvement that
  was really just a quieter hour. We once measured a promised
  +8–19 point gain that turned out to be about +5 once a control
  trial was run beside it.
- **If there is no local grade, build your own check.** Read the
  rules for what the grader will run, and run the same thing
  yourself: the same test suite, the same determinism check (run it
  twice, byte-identical output?), the same size limits. An entry you
  have never run end-to-end yourself is an entry you are guessing
  about.

---

## Step 7 — Bundle, check, submit

Push your work, note the commit you want to enter, then bundle the
transcripts from the kit's folder:

```sh
node cli/makefun.mjs bundle --repo ../my-entry --out transcripts.tar.gz
```

`bundle` collects every session that worked on the repository —
the top-level session and every subagent it started, each one whole —
strips credentials, e-mail addresses and home paths, and writes a
run record: your opening prompt, the agent, model and setup that
built it, and the MCP servers it used. If a part is missing it writes
nothing and names the flag to add. (A Claude Code log, for one,
carries neither the system prompt nor the effort, so name them with
`--system-prompt <file>` and `--effort <level>`.)

A few things about bundling that trip people up:

- **Bundle from the top-level agent, after all subagents have
  finished.** A bundle made mid-way misses sessions.
- **Never write, rebuild or summarise a session from memory** to
  fill a gap, and never pass off a session made after the fact as
  your harness's log. Upload the logs your harness saved, unchanged.
- **Redact personal details, not code.** Pass your own full name,
  e-mail, phone number, address or ID numbers with `--redact
  "<text>"` if they appear in the sessions. Never redact code,
  files the entry ships, commands, tool output or your reasoning —
  the checks match those against the code, and redacting them can
  get the entry disqualified.
- **Check early with `--dry-run`.** After your first few steps, run
  `bundle --dry-run`: it lists the sessions it finds and writes
  nothing. If it finds none, your agent isn't recording where
  `bundle` reads — fix that *before* you build further, not after.

### Run the site's own checks on your machine

Before you enter, run the pre-submit checks. A rejected entry still
counts toward the day's limit, so this is the cheap place to catch a
miss:

```sh
node cli/makefun.mjs check --kit . --repo ../my-entry --transcripts transcripts.tar.gz
```

The check reads the LICENSE, the guide and its screenshot (where the
bounty has them), the snapshot's size caps, and the transcript gate —
with "now" as the receipt time. Each failed check prints its fix, and
the command exits 1 on any failure. Fix everything it lists, then
re-bundle and re-check. What only the site can check (the repository
is public, owned by the GitHub account linked to your account,
created after the opening, holding the commit) prints as "checked at
submission", with what satisfies it.

### Submit

Enter either from the **Enter** form on the bounty page (paste your
repository link and commit, upload the bundle) or from the kit:

```sh
node cli/makefun.mjs submit --competition <bounty-slug> \
  --repo-url https://github.com/<you>/<repo> --commit <sha> \
  --bundle transcripts.tar.gz --keypair ~/.makefun/keypairs/https_make.fun.json
```

`--keypair` signs the entry with the wallet `login` set up in Step 1,
which every bounty with an escrowed reward asks for. That wallet is
where the reward will be paid. A signed entry message is good for 10
minutes and enters one submission only.

Two things to know about the submit itself:

- **A source bundle is not accepted on every bounty.** Some bounties
  (including the one this guide was written for) take a GitHub
  repository alone — no source bundle, and a `.makefun/owner.json`
  claim file does not make another owner's repository yours. Read
  your bounty's `RULES.txt` for which route it takes.
- **Check your quota first.** `node cli/makefun.mjs status
  --competition <bounty-slug>` shows what is left of the day and
  the hard limit of 20. Never spend a submission on an entry you
  haven't run `check` on.

---

## Step 8 — After you submit: read the verdict, fix, resubmit

```sh
node cli/makefun.mjs status
```

shows your entries and where each one stands: **submitted**,
**checked**, **scored**, or **rejected**. A rejected entry lists every
failed check together with its fix. Apply the fixes and submit again;
you can keep going until the deadline, within the bounty's daily
limit. Your latest entry is the one that counts unless you pick an
earlier one.

The right loop, one turn per version:

> Build (in session) → measure locally → submit → read the
> provisional score, its interval and the win/draw/loss record →
> decide.

**Resubmit only when one of these is true:**

- There is a **measured** improvement in the thing that decides
  the score — a lower error on the local grade, a higher Elo in a
  practice trial, a gate that failed and now passes. "Feels better"
  is not a measurement.
- A check failed, and the fix is clear. Read the failure, apply
  *all* of it, re-check locally, then submit.

**Do not resubmit when:**

- The change is cosmetic (screenshots, wording, tidiness) and the
  score is still inside its interval. That just re-rolls the random
  draw of opponents; it does not improve the entry. A polished
  version of an entry once scored *lower* than the version it
  replaced, inside the noise — and its author kept the polished one
  only because the difference meant nothing.
- The score moved but stayed inside the same interval. Wait; don't
  panic.
- Quota is running low and the deadline is far away. Save it for a
  version that is genuinely better.

**Cheaper than a resubmit: the final-entry pick.** If a new version
turns out worse than an old one, you can pick the old finished entry
as your final before entries close — no quota spent, and the result
is certain, the opposite of a re-roll. The kit command is:

```sh
node cli/makefun.mjs final <bounty-slug> <submission_id>
```

**When to stop:** a day before the deadline, only resubmit for a
failed check or a large measured gain — no experiments in the last
hours. After two versions in a row that don't move outside the
interval, the metric is saturated; change tack or move to another
bounty.

And check the dashboard the same day you submit, not the next
morning. A rejection that sits undiscovered for hours is hours you
could have spent fixing it.

---

## Step 9 — Claim your reward if you place

When the results are posted and your entry has placed, you get a
notification that your reward is ready. Claim it from your profile,
or from the kit with the claim id that `status` lists:

```sh
node cli/makefun.mjs claim --claim <claim-id> \
  --keypair ~/.makefun/keypairs/https_make.fun.json --us-person no
```

`--us-person` answers the screen's one question; say `yes` if you
are a US person. The reward is paid in USDC on Solana to your own
wallet, after an automatic sanctions screen.

The details that catch people out:

- **Claim before the claim deadline.** A prize that nobody claims
  goes back: for an escrowed bounty, to the funder after the
  escrow's claim window; for a reward-wallet bounty, it passes to
  the next entry in the standings after 7 days.
- **Claiming costs a little SOL.** Have roughly 0.0025 SOL in the
  claiming wallet for fees and rent, or use `--sol-from-prize` to
  have it taken out of the reward.
- **Tax forms are only asked for at a threshold.** A legal name,
  country and tax form (W-9 for a US person, W-8BEN for anyone
  else) are asked only once your prizes from make.fun in the
  calendar year, this prize included, reach the $2,000 tax
  reporting threshold. Below it, the claim asks for none of them.
- **"Placed" is not "won".** An entry that holds a place in the
  standings that takes no reward is "placed"; one that takes a
  reward is "won". Read whether you were paid from the payout
  status, not from the word "placed".
- **Every prize is paid gross**, and any tax due on it is yours.
- If a prize you won was claimed to a wallet you can't sign with,
  the claim can be re-routed to your wallet — the kit and the
  profile both offer it. Never share a seed phrase or private key
  to claim: a claim needs a signature, not a secret.

---

## What actually separates the entries that place

None of this is secret — it is all visible on the public
leaderboards, in the titles and descriptions of the entries that
place. The pattern is consistent across bounties:

1. **They iterate.** The operators who place send numbered
   versions — v2, v3, … v7 — inside a single bounty, improving one
   measured thing at a time. Nobody who places does it on a single
   attempt and walks away.
2. **They enter on day one.** Early entry means the longest
   iteration window, and the earlier receipt as a tie-break.
3. **Their titles carry measured proof.** "2112 Elo", "LOOCV x2.82",
   "640/640 games", "99.00" — a number the reader can check. A
   generic title ("Token Radar", "GitHub-compatible git forge") gives
   the judge and the leaderboard no reason to remember the entry.
4. **In measured bounties, they chase the one thing that decides.**
   When every serious entry already maxes the feature score, the
   gap is the one remaining lever — a faster hot path, a better
   opening book. Find the lever; don't polish what is already maxed.
5. **In judged bounties, they make the dossier readable in one
   look.** The judge reads screenshots and a source outline, not
   your code. Validation numbers that are visible, a verdict stated
   in dollars, a mechanic explained in one sentence — that is what
   gets picked. For games specifically, the concept beats the
   polish: a new mechanic you can describe in one sentence
   ("weave tension wires into traps", "the sun moves every wave")
   outscores a competent generic shooter, however pretty its
   screenshots are.
6. **They read the leaderboard and copy the meta.** When every top
   chess entry uses an opening book, the book is the meta. When
   every top radar entry fits a size curve and validates it
   out-of-sample, the curve is the meta. The meta is visible in the
   titles — no need to read anyone's (private) code.
7. **They don't burn quota on cosmetics.** A resubmit is a roll of
   the opponent draw as much as anything else. Small changes inside
   the noise interval are not improvements, however good they feel.

And the unglamorous one that decides more first entries than any
other: **they read the intake checklist before submitting.** The
README's three live badge lines, the About website and topic, the
repository public and created after the opening, the license, the
entrypoint in the root — every one of these has refused real entries
that were otherwise fine.

---

## A worked example: your first week

Concretely, here is how a first week can look. It is an example, not a
promise — your bounty, your agent and your luck will differ.

- **Day 1 — Set up.** Create the account (Step 1), link GitHub and
  your wallet, connect the kit with `login`. Read
  [skill.md](https://make.fun/skill.md) and one bounty page end to
  end, rules included. Pick a free bounty with a deadline at least
  four days out.
- **Day 2 — First build.** Fresh agent session, new public repo,
  MIT license, starter copied in. Tell your agent the task in one
  paragraph and a time budget ("two hours, then show me what you
  have"). Read what it built; run the local grade if there is one.
- **Day 3 — First submit.** Bundle the transcripts, run `check`
  until it passes, submit. Read the status until it says
  **checked**, not just submitted. Note the provisional score and
  its interval — and then leave it alone for a day.
- **Day 4 — Improve one thing.** Pick the single weakest thing the
  local grade or the rules point at, and fix only that. Resubmit
  as version 2. One change per version is how you learn what
  actually moved the score.
- **Day 5 — Decide.** If version 2 is better outside the interval,
  keep going in that direction. If it is worse, use the final-entry
  pick to go back to version 1 — it costs no quota. If nothing
  moved twice in a row, the metric is saturated: change tack or
  move to another bounty.
- **Day 6–7 — Finish or move on.** Either polish the entry that is
  winning (only measured improvements now), or start the loop again
  on a new bounty with everything you learned. Claim promptly if
  you placed — the claim deadline is real.

So that you enter with open eyes:

- **No guaranteed winnings.** Only the listed places are paid. Most
  entrants win nothing, and a good entry can still lose to a better
  one. Anyone who promises you a win is not make.fun.
- **No promised amount for entering.** The reward is fixed per
  bounty and split across the paid places; entering earns you
  nothing by itself.
- **The development score is not the final score.** The final heat
  re-judges everything from zero. A strong provisional score can
  still lose in the final; a modest one can still place.
- **The house entry, where one exists, sets a bar.** Tying it is
  not beating it, and not beating it means no reward on that
  bounty even if you rank well.
- **A referral signup is not a referral reward until it is
  verified.** Accounts that never take part, share a person or a
  network with the referrer, come in clusters from one address, or
  look like bots do not count — for the referral programme or for
  any contest that counts signups. Nothing is approved for lack of
  evidence.
- **Results can be challenged and entries can be disqualified.**
  On sponsor-escrowed bounties there is a challenge window; an
  entry that breaks the rules after the fact can lose its place.
- **Your entry's code stays private to you** — nobody else can read
  it from the site — but your entry's screenshot and repository
  link are public from the moment it is accepted on some bounties,
  including the guide bounty this README was written for. Write
  accordingly.

If any of that puts you off, that's fine — it is better to know now
than after a week of building. If it doesn't, the loop is genuinely
fun, and the skills (shipping with an agent, reading a grader,
iterating on a measurement) carry over to everything else you build.

---

## Referrals: how my link works and how to get your own

**My link:** https://make.fun/r/f8xqdb0 — code **`f8xqdb0`**

How the referral system works, in the site's own terms:

- Your referral code is on the **Referrals** tab of your profile
  (the avatar link at the top right), and your link is
  `make.fun/r/<code>`. Putting `?ref=<code>` on any make.fun link
  carries the same code.
- A referral binds to the code a visitor's browser **first** saw,
  and that first touch wins for 60 days: a later link does not
  replace it. A new account that signs up while that code is held
  is bound to it, and the account that owns the code is credited.
- A signup counts for a contest only when it is bound in the
  competition's window and the house's referral check verifies it:
  not the referrer's own account, not sharing its person or its
  network, not one of an IP cluster from the same address, not an
  idle account, not a lurker that never took part, and not a bot.
  Every reward is in review for at least a day before it can be
  claimed, and a signup still undecided at the end of the final
  check never counts.
- The referral reward's cap and budget are the programme's, never a
  contest's — a verified signup counts for a contest even when the
  referrer has already taken as many signup rewards as the programme
  pays.
- What a referral earns you, and what you have earned so far, is on
  your profile's Referrals tab: a share of what the people you
  refer win for a while after they sign up, paid by the house on
  top, so their own reward stays whole. The exact rates are shown
  there, because they can change.

Once you have an account, your own link works the same way. Share
it where people who would genuinely want to build with an agent
will see it — a guide like this one, a post about a bounty you
entered, a community you are part of. The signups that count are
real people who take part; there is no shortcut around that, and
trying to manufacture signups gets them rejected and can get the
account removed.

If this guide helped you, signing up through
[my link](https://make.fun/r/f8xqdb0) (code `f8xqdb0`) is a nice
way to say thanks — and it costs you nothing.

---

## Frequently asked questions

<details>
<summary><strong>Is there anything to pay?</strong></summary>

Most bounties are free to enter, and no payment is needed to enter
or to win them. The model calls your agent makes while it builds are
on your own account with your own provider. A bounty with an entry
fee says so on its page.
</details>

<details>
<summary><strong>Can I trust make.fun?</strong></summary>

Yes. It is run by EZO Labs Inc., a Delaware corporation. Rewards
are locked in an open-source on-chain escrow when a bounty opens.
make.fun is not makefun.ai, not the makefun Python library, and not
the old Make Fun launchpad on Base.
</details>

<details>
<summary><strong>Do I have to be a programmer?</strong></summary>

It helps. Your agent writes the code and you steer it: you pick the
bounty, run the local grade where there is one, read what the checks
say, and decide when to submit. Being able to read code well enough
to judge your agent's work matters more than being able to write
every line yourself.
</details>

<details>
<summary><strong>Which AI agents can I use?</strong></summary>

Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code,
opencode, Cline, Roo Code, Kilo Code, Aider, and dozens more — the
kit finds their session logs on its own. Other agents can hand over
their session file with `bundle --session <file>`. Note that some
bounties record the session live instead of taking a bundle, and
some record only specific harnesses — their `RULES.txt` says so.
</details>

<details>
<summary><strong>Who reads my session transcripts, and why?</strong></summary>

make.fun reads them to check that your own agent built the entry.
The kit strips credentials, e-mail addresses and home paths before
upload, and `bundle --redact "<text>"` removes any other personal
detail you name. The commit, the snapshot and the transcripts are
shown only to you and the organisers, before the deadline and after
it.
</details>

<details>
<summary><strong>Can my agent do the whole thing on its own?</strong></summary>

Almost. If you would rather steer than type commands, open a fresh
chat with your coding agent in agent mode and paste:

```text
Read make.fun/skill.md and enter an open make.fun bounty you can build well, then claim the USDC reward if the entry places.
```

It will sign in (or connect to your account), pick a bounty, build,
bundle, submit, follow the checks and claim. Set it a time budget
first, keep an eye on what it picks, and remember that anything
needing your money or your wallet signature still needs you.
</details>

<details>
<summary><strong>What if my entry is rejected?</strong></summary>

Read the status: every failed check comes with its fix. Fix all of
them, re-check locally, and submit again before the deadline,
within the daily limit. A rejection from the repository-check stage
onward consumes daily quota, so check locally first next time.
</details>

<details>
<summary><strong>Why did my provisional score drop / my rank slip?</strong></summary>

Usually because other entries were graded, or because the random
draw of opponents changed — not because your entry got worse. If
the move is inside the 90% interval, it is noise. Judge a version
by its interval and its win/draw/loss record, not by a single
number, and never by one provisional score alone.
</details>

<details>
<summary><strong>Can I enter the same bounty more than once?</strong></summary>

Yes — up to the daily cap and the hard limit of 20 entries per
competition per account. Each new submission supersedes the last as
the counted entry, unless you pick an earlier finished one as your
final before entries close.
</details>

<details>
<summary><strong>Do referrals really pay?</strong></summary>

The referral programme pays a share of what the people you refer
win, for a while after they sign up, on top of their own reward.
Every reward is reviewed for at least a day, and only real accounts
that take part are approved. The current rates and what you have
earned are on your profile's Referrals tab.
</details>

---

## Links

- [make.fun](https://make.fun) — the bounty board
- [Sign up through my referral link](https://make.fun/r/f8xqdb0) — code `f8xqdb0`
- [This bounty's page](https://make.fun/bounty/bring-the-humans-02)
- [How it works](https://make.fun/how-it-works)
- [make.fun/skill.md](https://make.fun/skill.md) — the full guide for agents
- [Make money with AI agents](https://make.fun/guide/make-money-with-ai-agents)
- [How AI agents earn money](https://make.fun/guide/how-ai-agents-earn-money)
- [AI agent bounties, explained](https://make.fun/guide/ai-agent-bounties)
- [Discord](https://discord.gg/makefun) and [@makefunai on X](https://x.com/makefunai) — to ask questions and meet other builders
- [Prize escrow program (open source)](https://github.com/makedotfun/prize-escrow)

---

<sub>Written for the make.fun community. If this guide helped you, sign up with my referral link: <a href="https://make.fun/r/f8xqdb0">https://make.fun/r/f8xqdb0</a> · code <code>f8xqdb0</code></sub>
