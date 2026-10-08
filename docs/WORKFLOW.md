# Workflow

How work on this site is planned, built, reviewed and released, with AI agents doing
most of the building and a human deciding what gets built and what gets merged.

The process is adapted from JP Burford's Innovation Sprint Lab series, *Shipping Code
in the Age of AI* (September 2026): GitHub flow with a `dev` branch, Scrum in
two-week sprints, GitHub Projects as the board, and repo-local agent skills for the
repetitive steps. Where the lectures assume a multi-service codebase, this document
scales the process down to a one-file static site.

## Adoption status

This describes the target process. As of 2026-10-07 only part of it exists.

| Piece | State |
| --- | --- |
| `main` published by GitHub Pages | In place |
| Pull request template | Added, not yet used |
| `CLAUDE.md` agent guidance | Added |
| Content file (`content/site-content.md`) | Added; the `/sync-content` command that applies it is not written |
| `dev` branch | Created 2026-10-07; the first 33 commits went straight to `main` |
| Branch protection on `main` | Not configured |
| `.gitignore` | Missing |
| GitHub Project board, custom fields, issue types | Not created; the repo has only default labels and no issues |
| Agent skills (planning, merge, sprint reports) | Not written |

Until `dev` and branch protection exist, treat the rules below as the convention to
follow by hand.

## Principles

- **Describe the what, review the how.** The human writes the outcome wanted; the
  agent proposes the implementation; the human reviews it. Agents are not trusted on
  their word, and their output is challenged and iterated like a colleague's.
- **Small pieces.** Break work into tasks an agent can finish and a person can
  review in one sitting. Never ask for a whole redesign in one go.
- **Context lives in the repo.** Guidance, conventions and plans are checked in or
  written on the issue, so any agent on any machine starts from the same place.
- **Pull requests are the record.** Each one says what changed and why.
- **Discipline over speed.** Agents produce changes faster than they can be
  reviewed. The board and the merge rules keep that from becoming a pile-up.

## Branches

| Branch | Purpose | How changes arrive |
| --- | --- | --- |
| `main` | Production. GitHub Pages serves it. | Merge commit from `dev` only |
| `dev` | Integration. Finished work collects here before release. | Squash merge from feature branches |
| feature branches | Where work happens. One per task or bug. | Commits from one author |

Rules:

- Never modify `main` directly. With Pages publishing on every push, a direct commit
  is the fastest way to break the live site.
- No two people, or agents, work in the same branch. If two need to share a feature,
  cut a feature branch from `dev` and have each cut their own branch from that.
- Name branches `<issue-number>-<short-description>`, for example
  `12-add-sectional-screenshots`.
- Delete a branch once it merges. If something needs fixing later, cut a new branch
  from `dev`.

`dev` has no preview URL, because Pages serves only `main`. Review `dev` by serving
it locally.

### Everyday commands

Start a task:

```bash
git checkout dev
git pull
git checkout -b 12-add-sectional-screenshots
git push --set-upstream origin 12-add-sectional-screenshots
```

While working:

```bash
git status                       # which branch, which files
git add index.html               # add files by name
git commit -m "Add Sectional screenshots to project card"
git push                         # the remote is the backup; push several times a day
```

Before opening the pull request:

```bash
git status                       # everything committed?
git checkout dev && git pull
git checkout 12-add-sectional-screenshots
git merge dev                    # resolve conflicts here, then re-check the page
git push
```

Merge `dev` into the branch only when the branch needs those changes or when it is
about to become a pull request. Do the final local preview after that merge.

### Git habits

- Commit as often as is useful. There is no such thing as too many commits on a
  feature branch; they are squashed on merge.
- Do not stash. Commit to the branch, or cut a scratch branch to experiment.
- Do not add files blindly. `git status` first, then add by name.
- Set up `.gitignore` before anything else in a new project.

### Worktrees for parallel work

Git worktrees check out several branches of the same repository into separate
folders that share one history. They let more than one agent work at once without
overwriting each other's files.

```bash
git worktree add ../site-12-sectional -b 12-add-sectional-screenshots dev
git worktree list
git worktree remove ../site-12-sectional
```

Things to know:

- A branch can be checked out in only one worktree at a time.
- Each worktree gets its own copy of the files, including about 114 MB of `assets/`.
- Create worktrees beside the repo folder, not inside it.
- Worktrees stop agents colliding on disk. They do not stop merge conflicts, and on
  this site nearly every branch edits `index.html`. Merge order matters; see
  [Merging](#merging).

## Pull requests

GitHub fills new pull requests from `.github/PULL_REQUEST_TEMPLATE.md`.

- One task or bug per pull request.
- Open a draft early if it helps capture context before it is forgotten.
- Splitting one feature across several pull requests is fine and often better.
- Review is for catching problems and sharing context. It is not punitive.

### Merging

| From → to | Merge type | Result |
| --- | --- | --- |
| feature → `dev` | Squash and merge | One commit per pull request on `dev` |
| `dev` → `main` | Merge commit | The release point is recorded in history |

When several pull requests are ready at once, merge them through a staging branch
instead of one at a time:

1. Cut a staging branch from `dev`.
2. Squash-merge each ready pull request into it, in the order that causes the fewest
   conflicts, resolving conflicts against the plan on each linked issue.
3. Make one clean-up commit: check the merged page renders, links and asset paths
   resolve, markup is consistent with the conventions in `CLAUDE.md`.
4. Merge staging into `dev` with a merge commit.

`dev` ends up with one commit per issue plus one clean-up commit, and the checking
is done once for the batch.

## Planning work

### Issue hierarchy

All work is tracked as GitHub issues on a GitHub Project board.

| Type | What it is | Example on this site |
| --- | --- | --- |
| Epic | A collection of user stories | The Projects section |
| User story | Something a visitor does | A recruiter skims a project and downloads the deliverable |
| Feature | What the site provides to satisfy a story | Project cards with download buttons |
| Task | The work to implement a feature | Add the Sectional project card |
| Bug | Something that does not work or behave as intended | Footer overlaps content on mobile |

Epics, user stories and usually features are organizing structure. Tasks and bugs
are the work: one task or bug is normally one branch and one pull request.

How items reach the board:

- **Epics and user stories** are written by hand, then explored with an agent in a
  spike to fill in detail and settle the approach.
- **Features** mostly come out of spikes, and sometimes surface while working tasks.
- **Tasks** are mostly created by the agent, during spikes or in response to work
  and review.
- **Bugs** are filed by whoever finds them, human or agent.

### Size

| Size | Effort |
| --- | --- |
| XS | 4 hours or less |
| S | 1 day |
| M | 2 to 3 days |
| L | 1 week |
| XL | 2 weeks (one sprint) |
| XXL | 4 weeks (two sprints) |

Most work on this site is XS or S. Anything L or larger should be split.

### Priority

| Priority | Meaning |
| --- | --- |
| Low | Nice to have |
| Medium | Need to have |
| High | Need to have, and it blocks visitors or other tasks |
| Emergency | Only when unavoidable, for example the live site is broken |

### Board statuses

| Status | Meaning | Who moves it on |
| --- | --- | --- |
| Backlog | Captured, not yet planned | Human |
| Planning | Needs a detailed implementation plan written on the issue | Agent writes the plan; human approves |
| Ready | Plan approved; can be picked up | Human starts an agent on it |
| In progress | Being built on a branch | Agent opens a pull request |
| In review | Pull request open | Human reviews, fixes, refines |
| Ready to merge | Approved | Batch merge picks it up |
| Done | On `dev` | |

The plan on the issue is the design document. An agent picking up a task reads the
issue first and builds from that plan.

## Sprints

Two-week sprints, with the schedule and capacity fixed and scope the thing that is
negotiated. Every sprint should end with something that can be shown.

| Event | When | Output |
| --- | --- | --- |
| Sprint planning | Start | Sprint backlog chosen from the board, balanced by priority, size, type and dependencies |
| Daily check | Each working day | What is planned today and what is blocked |
| Sprint review | End | Demo of what reached `dev`; release to `main` |
| Retrospective | End | What went well, what did not, what changes next sprint |

Retrospectives also record how much was finished against how much was planned. That
figure sets the load for the next sprint, so sprints stay predictable and
sustainable.

## A working day

The lectures describe a daily loop built around when a human has to be present:

1. **Evening.** Start agents on `Ready` issues that have a good chance of succeeding
   unattended. Each runs in its own worktree.
2. **Morning.** Review the pull requests produced overnight. Fix, refine, and mark
   the good ones `Ready to merge`.
3. **Through the day.** Work the harder issues interactively with an agent. How many
   run at once depends on usage limits and on how much review one person can do.
4. **Midday.** Run the batch merge over everything marked `Ready to merge`.
5. **After the batch merge.** Merge the staging branch into `dev`.
6. **Afternoon.** Run planning over issues in `Planning`, review the plans, and move
   approved ones to `Ready`.

For a site this size the loop will often be a few issues a week, not a daily cycle.
The order of the steps is what matters.

## Agent skills

The lectures automate the repetitive steps as skills checked into the repo, so they
are shared across machines. None exist here yet. This is the planned set, with names
from the lectures.

| Skill | Step | What it does |
| --- | --- | --- |
| `plan-issue` | Issue planning | Writes a detailed implementation plan onto a GitHub issue |
| `plan-queue` | Issue planning | Runs `plan-issue` over every issue in `Planning` |
| `get-issue` | Implementation | Loads an issue's plan as the basis for building it |
| `sprint-plan` | Sprint planning | Spreads issues across the sprint by dependency, size and priority |
| `sprint-kickoff` | Sprint planning | Produces the sprint backlog and a plain-language sprint summary |
| `plan-my-day` | Daily | Checks today's plans are current with the repo and ready to build |
| `get-my-day` | Daily | Lists today's issues with a burndown for the sprint |
| `multi-merge` | Merging | Orders and squash-merges every `Ready to merge` pull request into a staging branch |
| `cleanup` | Merging | Checks the merged result against repo conventions and verifies it renders |
| `retro-note` | Sprint reporting | Appends a note to the sprint retrospective |
| `sprint-wrapup` | Sprint reporting | Produces the sprint summary, release notes and retrospective |

For this repo, `cleanup` means HTML validity, link and asset checks and a rendered
look at desktop and phone widths, since there is no linter or test suite to run.

## Working with agents

- Give the agent a role that fits the task (accessibility reviewer, copy editor, UI
  designer).
- Write prompts in full sentences with normal punctuation. It makes intent clearer.
- Start a fresh session when an agent drifts from the task.
- Pick the model and effort level to suit the task. Both drive usage.
- Agent runs are started by a person. Do not script around interactive sign-in or
  usage limits to make runs start themselves.

## Setting this up

In order:

1. Add a `.gitignore` and decide what in `.claude/` is shared (`settings.json`) and
   what stays local (`settings.local.json`).
2. Create `dev` from `main` and protect `main` against direct pushes.
3. Create the GitHub Project with Status, Size, Priority and Type fields matching
   the tables above.
4. Seed the board with epics for the site's sections and the first tasks.
5. Write the skills, starting with `plan-issue` and `get-issue`, then `multi-merge`
   and `cleanup`.
6. Add automated checks for `cleanup` to run (HTML validation, link checking).
