# YavaPy

Yet Another Virtual Aggregator for PyPI. A searchable directory of the Agent
Skills that live beside published Python command-line tools. Search it at
[yavapy.nakamaru.ca](https://yavapy.nakamaru.ca).

Some PyPI projects keep a `SKILL.md` in their source repository. It teaches an
agent how to drive the tool: which command, when, and why. An agent could use
it today, but nobody thinks to look there. YavaPy looks.

## What gets listed

A PyPI project is listed when all three hold:

- it carries the `Environment :: Console` classifier,
- it published a release in the last twelve months, and
- its source repository holds a `SKILL.md` at the release's tag.

That is the whole test. A polished skill and a broken one are listed the same
way. So is a strange one. The directory answers one plain question: what
actually exists?

## Searching

Search by what you already know: a package name, or a few words about the
task. Each result names the PyPI project and its licence, and links to both
its package page and the `SKILL.md` in its repository.

The original repository stays the source of truth. YavaPy points to a skill.
It never copies, rewrites, or summarizes one.

## What a listing means

A listing means a `SKILL.md` was found in a repository that a PyPI project
names as its source. Nothing more. It is not a review, and it does not say the
skill is correct, safe, maintained, or any good. Read a skill before you hand
it to an agent, as you would any instructions from a stranger.

## What it misses

The directory is useful, not complete. Only GitHub repositories are checked, at
a tag named `v{version}` or the bare version. A project on another host, or
tagged another way, goes unchecked and unlisted. Each harvest is capped, to go
gently on PyPI and GitHub, so older projects arrive slowly.

## How it stays current

A harvest reads PyPI's public release metadata. A new release sends a
project back for a fresh look, so a skill added today shows up after the
project's next release. The directory is a read-only site.

## The code and the data

This repository holds only this page. The work lives in the others:

- [yavapy-harvester](https://github.com/east-van-ai/yavapy-harvester) is the
  harvest, which writes the data.
- [yavapy-data](https://github.com/east-van-ai/yavapy-data) is the data: one CSV
  of every candidate, with or without a skill, and an index of every recent PyPI
  project beside it. Its README explains every column.

## Use of AI

Code and documentation are written in collaboration with remote and local AI; design
decisions, code review, semantic and auditory review, and final judgement stay human.

---

**East Van AI** · AI for the rest of us! · Vancouver, BC, Canada

[github.com/east-van-ai](https://github.com/east-van-ai) · <east-van-ai@proton.me>

Copyright (c) 2026 Go Nakamaru
