# Dev Journal — Devin S. Wolson

**CISSP** · B.S. Cybersecurity, Champlain College

This repo started as my first real interaction with GitHub (the "hello-world"
quickstart). It's since become a running journal of my move into cybersecurity
and software development — what I'm learning, what broke, and how I fixed it.

Entries are irregular, not scheduled — I add one when something is worth
writing down.

For code, see my other repositories:

| Project | What it does | Stack |
|---|---|---|
| [web-scoping-tool](https://github.com/adkchrgr/web-scoping-tool) | Web checker for engagement scoping | Python |
| [Friendsapp](https://github.com/adkchrgr/Friendsapp) | First Ruby on Rails app (tutorial plus my own fixes) | Rails |
| [sort_screenshots_MacOS](https://github.com/adkchrgr/sort_screenshots_MacOS) | Auto-organizes macOS screenshots | Python |
| [it-cert-automation-practice](https://github.com/adkchrgr/it-cert-automation-practice) | Google IT Automation with Python coursework | Python |
| [My-Claude-Architect-Examples](https://github.com/adkchrgr/My-Claude-Architect-Examples) | Runnable examples from the Claude Certified Architect track | Python |

---

## 13 March 2022

A few months into the COVID-19 pandemic I lost my job in automotive sales after
almost 10 years. I had just moved into a 230-plus-year-old stone cottage, in need
of major renovations, with my wife and one-year-old child. It was a change we had
not foreseen, but it did not take me long to decide I needed to make a career
choice. Within two weeks I applied to and was accepted into the online
cybersecurity undergraduate program at Champlain College.

I have always had a strong interest in computers, coding, and technology, and yet
I had never taken a deliberate approach to making it the foundation for a career.
Starting this journey was exciting and nerve-racking. I was only able to transfer
in 30 credits from my associate degree, and I had only enough savings to take me
so far.

I spoke with my academic advisor and scheduled 18 credit hours per semester, plus
a full summer term. That pace would let me complete the three years of coursework
in about 1.5 years and finish right around the end of my savings.

That brings me to today: halfway through my last semester with a 3.988 GPA, one
three-credit course and a capstone class left. With a mix of relief, disbelief,
and pride, I also realize there is more work to be done to increase my
marketability. Between classes, family, and side jobs I had never taken a real
moment to build a portfolio of the projects I have worked on. Now that I have a
little more room in my schedule, I have decided to populate this repository with
what I have produced, been exposed to, and am working on. This post was a good
first step toward getting comfortable with Markdown syntax while following the
GitHub quickstart guide.

Thanks for reading. I look forward to sharing what I can.

## 02 January 2024

Time flies when you are having fun — or struggling, or on days ending in "y."

Since my first post, a lot has changed. In August 2022 I found a great position
with a fantastic team at Synack as a weekend ops engineer. The last year and a
third have been packed with learning and growth, professionally and personally.

My most recent focus has been learning Ruby on Rails by following a free YouTube
tutorial (<https://www.youtube.com/watch?v=fmyvWz5TUWg&t=8117s>). It has been a
big help for learning the framework and deploying an app locally. The video is a
few years old and some of it did not line up with the current version of Rails,
but I appreciated the effort it took to work through those mismatches.

My biggest struggle was with the sign-out route using the Devise gem. Everything
in my code, routes, and syntax matched what the documentation and tutorials said
should work, but signing a user out threw an error saying there was no route for
`[GET] users/sign_out#destroy`. Several Stack Overflow posts had possible fixes
that did not solve it, and ChatGPT did not offer anything I had not already
tried.

Then I found one post from someone with the same problem. Devise's default HTTP
method for `sign_out` is `DELETE` (which every doc confirms), but this person
changed the default to `GET` to match the route in the error, and it worked. A
three-letter change ended a three-day runaround. 🤡 Oh well — now it is something
I will not forget.

Next up: using GitHub to version-control my Rails project and maybe developing it
into a fully functional app that solves a real problem. I am thinking about a
pantry inventory app that uses AI to scan receipts, break a purchase into
individual items and quantities, and store them in a database. It might also use
current inventory to suggest meals. It would need to remove items as they are
used or expire, and alert when stock runs low.

## 28 August 2026

New track: I'm working through the **Claude Certified Architect** material and
keeping every exercise as a small, runnable example in
[My-Claude-Architect-Examples](https://github.com/adkchrgr/My-Claude-Architect-Examples).
The goal is to actually understand how an agent is wired, not just call an API.

What I've built so far:

- **Tool-use loop from first principles.** A manual Messages API loop that reads
  `stop_reason` on every turn to decide whether to run a tool and keep going
  (`tool_use`) or stop and print the answer (`end_turn`). Seeing the full
  `messages` list get resent each turn made the stateless design click.
- **Loop control.** A focused example on ending a run correctly instead of
  letting it spin — checking stop conditions and turn limits rather than
  trusting the model to stop on its own.
- **Decision-making patterns.** Prompts and scaffolding for getting the model to
  choose between options in a structured, checkable way.
- **Multi-agent coordination.** A basic coordinator that hands narrow,
  well-scoped subtasks to worker agents and assembles the results — plus notes
  on why breaking a task down small matters more than I expected.

Running everything on Haiku to keep the API bill near zero while I iterate.

Next: turning these pieces into one end-to-end agent and studying where the
handoffs get fragile.
