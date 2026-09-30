# =============================================================
# Story Sidecar Metadata
# Place this .md file next to its matching .html Twine export.
# Filename should match the .html file (e.g. my-story.md / my-story.html)
# =============================================================

layout: story                  # Uses _layouts/story.html
title: "My Story Title"        # Displayed in index and library
date: 2026-09-30               # Publication date (YYYY-MM-DD)
author: "VincentD"

# --- Classification ---
category: aventure             # Must match the subfolder name in /library/
tags:
  - twine
  - harlowe
  - aventure

# --- Display ---
description: >
  A short description of the story, displayed on the library
  index card and in the og:description meta tag.

cover_image: /assets/images/covers/mon-histoire.png   # Optional cover art

# --- Story link ---
story_url: /library/aventure/mon-histoire.html        # Path to the Twine .html export

# --- Status ---
status: published              # published | draft | wip

# --- Optional ---
play_time: "~20 min"           # Estimated play time
content_warning: ""            # e.g. "Violence, themes of loss" — leave empty if none

---

<!-- 
  This body content appears on the individual story page (/library/aventure/mon-histoire/).
  Write a longer description, dev notes, or a teaser here.
  Markdown is fully supported.
-->

## About this story

Write a longer description here. This is the full story page,
not just the index card. You can include:

- Background on the story
- Development notes
- Changelog / version history

## How to play

Click the **Play** button above to launch the story in your browser.
No installation required.

# =====[EOF]=================================================
