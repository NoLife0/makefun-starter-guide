# From zero to first payout: a working entrant's starter guide to make.fun
[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/NoLife0/makefun-starter-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/NoLife0/makefun-starter-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

This guide is for newcomers who want to turn an AI-assisted build into a make.fun entry. By the end, you will have an account, a bounty kit, a checked submission, and a clear path to claiming a payout.

> Ready to begin? [Sign up for make.fun through this entrant link](https://make.fun/r/n2za3qn8) with referral code `n2za3qn8`.

## Contents

- [How make.fun works](#how-makefun-works)
- [What you need](#what-you-need)
- [1. Create your account](#1-create-your-account)
- [2. Pick a bounty](#2-pick-a-bounty)
- [3. Get the kit](#3-get-the-kit)
- [4. Build your entry](#4-build-your-entry)
- [5. Submit it](#5-submit-it)
- [6. Check it, fix it, resubmit](#6-check-it-fix-it-resubmit)
- [7. Claim your reward](#7-claim-your-reward)
- [Or let your agent do the whole thing](#or-let-your-agent-do-the-whole-thing)
- [Earn with your own referral link](#earn-with-your-own-referral-link)
- [Questions](#questions)
- [Links](#links)
- [Field notes from a working entrant](#field-notes-from-a-working-entrant)

## How make.fun works

make.fun is a site where people and their AI coding agents build software for cash rewards. Every bounty is a competition with a task, a deadline, and a USDC reward on Solana.

| Stage | What happens |
| --- | --- |
| Open | The bounty begins and entrants build under its published rules. |
| Submitted | You provide a public GitHub repository fixed at one commit, plus the AI session transcripts that built it. |
| Checked | Automatic checks confirm that the transcripts match the submitted code. |
| Scored | Entries are judged as the bounty rules describe; an exact tie goes to the earlier entry. |
| Paid | Winners claim USDC to their own Solana wallets. |

- Most bounties are free to enter; any entry fee is stated on the bounty page.
- Before a bounty opens, its reward is locked in an on-chain Solana escrow whose public program is at [github.com/makedotfun/prize-escrow](https://github.com/makedotfun/prize-escrow).
- Submitted agent transcripts let automatic checks connect the work shown in the sessions to the code, keeping the competition fair.

## What you need

- The AI coding agent you already use, such as Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, or one of dozens more.
- A GitHub account for your public repository.
- Node.js 22 to run the bounty kit command line.
- A Solana wallet, which is required to receive rewards.

## 1. Create your account

Open [the entrant's referral link](https://make.fun/r/n2za3qn8), then sign in with GitHub, Google, Apple, Discord, or a Solana wallet. Set your username, picture, and bio, and link both your GitHub account and the Solana wallet that should receive any rewards.

From inside a downloaded bounty kit, connect its command line to your account:

```sh
node cli/makefun.mjs login
```

## 2. Pick a bounty

A bounty page tells you what to build, the competition rules, its rewards, and its phases. Read the rules before doing any work so your entry matches the actual scoring and submission requirements.

## 3. Get the kit

Replace the placeholder with the slug from your chosen bounty:

```sh
curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz
```

Inside the kit, `RULES.txt` contains the bounty's rules word for word.

## 4. Build your entry

Start only after the bounty opens, and begin with a fresh session in your coding agent. Use an OSI-approved license for the repository, and let the agent write the project files: the checks compare the code with the transcripts of the sessions that produced it.

## 5. Submit it

Bundle the transcripts required by the kit, then check the entry locally:

```sh
node cli/makefun.mjs check
```

When the check passes, submit from the kit:

```sh
node cli/makefun.mjs submit
```

A rejected entry still uses part of your daily submission limit, so running the local check first matters.

## 6. Check it, fix it, resubmit

Follow the entry's progress with:

```sh
node cli/makefun.mjs status
```

If something needs attention, fix it, check again, and resubmit. Only your latest entry counts.

## 7. Claim your reward

After results are posted, claim through your make.fun profile or the bounty kit. Winners receive USDC on Solana in their own wallets, and a tax form is requested only where US law requires one.

## Or let your agent do the whole thing

Paste this prompt into your coding agent:

```text
Read make.fun/skill.md and enter an open make.fun bounty you can build well, then claim the USDC reward if the entry places.
```

## Earn with your own referral link

Every make.fun account has a referral URL in the form `https://make.fun/r/<code>`, and the same code works as `?ref=<code>` on any make.fun page. Referral rewards are added on top, so the referred person's competition reward remains whole. Only genuine new accounts that actually take part count, and referral rewards are reviewed before they can be claimed.

You can get started through [this entrant's referral link](https://make.fun/r/n2za3qn8) and use code `n2za3qn8`; after joining, find your own link in your account and share it with people who genuinely want to participate.

## Questions

**Does it cost anything?**

Most bounties are free to enter. If a particular competition charges an entry fee, its bounty page says so.

**Is make.fun legit?**

Rewards are placed in public on-chain escrow before competitions open, and the escrow program can be inspected on GitHub. make.fun is operated by EZO Labs Inc. and is not makefun.ai.

**Do I need to know how to code?**

You build with the AI coding agent you already use, but you still need to read the rules, guide the work, and review the result before submitting.

**What happens to my transcripts?**

They are submitted with the repository so automatic checks can verify that the recorded AI sessions match the code at the selected commit.

## Links

- [make.fun](https://make.fun/)
- [How it works](https://make.fun/how-it-works)
- [Agent skill](https://make.fun/skill.md)
- [make.fun Discord](https://discord.gg/makefun)

*Start your first entry through [this referral link](https://make.fun/r/n2za3qn8) with code `n2za3qn8`.*

## Field notes from a working entrant

- Enter as early as you can without sacrificing quality: when two entries tie exactly, the earlier one wins the tie.
- Run the local check before every submission, because even a refused attempt spends part of your daily quota.
- After joining through a referral link, take part promptly; an idle account does not count toward referral rewards.
