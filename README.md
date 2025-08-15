# TryHackMe & Hack The Box Write-ups

This repo contains my personal notes and non-spoiler walkthroughs for rooms/machines I complete on TryHackMe and Hack The Box while studying cybersecurity at WGU.

## Structure
- `tryhackme/<room-slug>/README.md`
- `hackthebox/<machine-slug>/README.md`
- `assets/screenshots/<room-or-machine>/...` (images used by write-ups)
- `_template/WRITEUP_TEMPLATE.md` (copy this into a new folder for each write-up)

## How to add a new write-up
1. Copy `_template/WRITEUP_TEMPLATE.md` into the destination folder (e.g., `tryhackme/<room-slug>/README.md`).
2. Create a screenshots folder at `assets/screenshots/<room-or-machine>/` and drag images there.
3. Reference images with a **relative path**, e.g. `![dirb scan](../../assets/screenshots/thm-fakebank/dirb.png)`.
4. Commit with a clear message: `add: thm/<room> write-up` or `update: notes for <topic>`.

> Respect platform rules. If flags or answers shouldn’t be public, show **method** not the exact flag.
