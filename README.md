# Data Track — Week 1 Assignment (Template)

The HackYourFuture Data Track Week 1 assignment: **The Data Cleaning Pipeline**.

> 👩‍🎓 **Students:** you are in the wrong place. Do **not** fork or use this template.
> Go to your cohort's assignment repo under
> [`HackYourAssignment`](https://github.com/HackYourAssignment) (e.g. `c55-data-week1`,
> `c56-data-week1`, …). Your teacher posts the exact link in your cohort channel.
> Fork the cohort repo, branch, and open a PR back to it. Full instructions live in the
> [Week 1 Assignment on Notion](https://www.notion.so/hackyourfuture/Week-1-Assignment-The-Data-Cleaning-Pipeline-3cc37d4bf482470cbc6667bd1d1bb605).

## For instructors / track maintainers

This repo is the **upstream template** for the Week 1 assignment. At the start of each
cohort, generate a cohort-specific repo under the `HackYourAssignment` org from this
template (GitHub: **Use this template → Create a new repository**, owner =
`HackYourAssignment`, name = `c<NN>-data-week1`). Students then fork *that* cohort repo
and open PRs back to it; the auto-grader runs on every push.

Edits to the assignment, dataset, or grader belong here on the template, not on the
cohort copies.

## Tasks at a glance

| Task | Folder | Points | What you build |
|---|---|---|---|
| **Task 1** — Cleaner Pipeline | `task-1/` | 60 | A modular Python pipeline that reads `data/messy_users.csv`, cleans each field via helpers in `src/utils.py`, validates, and writes JSON to `output/clean_users.json`. |
| **Task 2** — AI Debug Report | `task-2/` | 20 | Document one debugging session where you used an LLM to fix a bug. Fill in the four sections of `AI_DEBUG.md`. |
| **Task 3** — HYF Azure proof | `task-3/` | 20 | Accept the HYF Azure tenant invite, switch to that directory, screenshot proof at `task-3/azure_proof.png`. |

Total: 100 · Passing: 60.

## Repository layout

```text
.
├── task-1/
│   ├── data/
│   │   └── messy_users.csv      # the dataset (committed; do not edit)
│   ├── src/
│   │   ├── cleaner.py           # entry point — fill in TODOs
│   │   └── utils.py             # field-cleaning helpers — fill in TODOs
│   └── output/
│       └── clean_users.json     # your cleaner writes here
├── task-2/
│   └── AI_DEBUG.md              # fill in the four sections
├── task-3/
│   └── azure_proof.png          # add your screenshot here
├── .hyf/
│   └── test.sh                  # auto-grader (read it to see exactly what it checks)
└── .github/workflows/
    └── grade-assignment.yml     # runs .hyf/test.sh on every PR
```

## Run the grader locally

Before opening a PR, run the same checks the auto-grader runs:

```bash
bash .hyf/test.sh
cat .hyf/score.json
```

This prints a per-task breakdown and writes `score.json`. Iterate until
`pass: true` (or until you've given it your best attempt), then push.

## Submission

Students submit on the cohort repo (`HackYourAssignment/c<NN>-data-week1`), not here:
open a PR from the student's fork against the cohort repo's `main`, then share the PR
URL with the teacher.
