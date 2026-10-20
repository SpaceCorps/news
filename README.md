# SpaceCorps news

Posts for the news card on the Dashboard of SpaceCorps 2027. A post is a text file in the `posts/` folder of this repository (branch `main`); a screenshot is a picture in the same folder.

The game server reads the `posts/` folder every 15 minutes and shows the newest posts to every pilot. Everything in this repository is **public**: never put anything secret
in it, not even in a draft. Everything committed to `posts/` goes in front of every pilot, so only a few people should have write access to this repository.

## Write a post

On github.com open the `posts/` folder, then **Add file** › **Create new file**. Name it with the date first, then a few words, ending in `.md`:

```
posts/2026-10-30-halloween-event.md
```

and write this:

```
---
title: Halloween event starts Friday
date: 2026-10-30
screenshot: 2026-10-30-spooky-sector.png, 2026-10-30-boss.jpg
---
Plain text with **bold** and *italic*.

- a list
- of two things

[Join the Discord](https://discord.gg/VjW67tkrTb)
```

Then **Commit changes**. The post shows in the game within 15 minutes.

* **title** (required): one line, at most 120 characters.
* **date** (required unless the file name starts with the date): `2026-10-30`, or with a time in UTC, `2026-10-30 14:00`. The newest date is first. A post shows as soon as it is committed, whatever its date.
* **screenshot** (optional): up to 3 pictures from this same folder, separated by commas.
* **draft: true** (optional) hides the post. It stays public in this repository.
* Write in English: the notes of the game are English. Any other line in the front matter is ignored.

The text is at most **4,000 characters**. What works: paragraphs (a blank line between), `## a heading`, lists (`- one` / `1. one`), `**bold**`, `*italic*`, and links `[text](https://address)`
(only `https` addresses; the game shows the address next to the text). Everything else is shown as plain text or left out: no HTML (it is removed), no pictures by address (use `screenshot:`),
no tables, no code blocks.

## Add screenshots

Open the `posts/` folder, **Add file** › **Upload files**, drop the pictures in, **Commit changes**. Then name them in the post's `screenshot:` line.

* PNG or JPEG only (it is checked by the file itself, not by its name). No GIF, no WebP, no SVG.
* At most **2 MB** (2,097,152 bytes) and **1,600 pixels** on the longer side. A bigger picture is not shown: save the screenshot as a JPEG or make it smaller first.
* Pictures share one folder with all the posts, so start every picture's name with the post's date and words: `2026-10-30-spooky-sector.png`. Use letters, digits, `.` `-` `_` only, no spaces.
* At most 3 pictures to a post, and the game keeps the newest 20 posts.

## Edit, hide or delete

Open the file on github.com, click the pencil, change it, **Commit changes**. To hide a post, add `draft: true` to the front matter. To delete it, open the file and use the trash can (delete its pictures too).

## If a post does not show

Wait 15 minutes. If it still does not show, ask an admin of the game: the server keeps a list of every file in `posts/` that it does not show, each with the reason in a sentence. The reasons you can
fix yourself (the server writes them in English, like this):

| The reason says | What to do |
|---|---|
| the file must start with a line --- , then lines like `title: ...` and `date: ...`, then a line --- | The first line of the file must be exactly `---`, and the front matter must end with another `---` line. |
| the front matter has no `title:` (or it is empty) | Add `title: Your title`. |
| the front matter has no `date:` and the file name does not start with a date like 2026-10-30 | Add `date: 2026-10-30`, or start the file name with the date. |
| `date: ...` is not a date like 2026-10-30 or 2026-10-30 14:00 (UTC, years 2020 to 2100) | Write the date as `2026-10-30` or `2026-10-30 14:00`. |
| the file name may only hold letters, digits . - _ | Rename the file: no spaces, no accents, no other signs. |
| N bytes: a picture is at most 2097152 bytes (2 MB) | Save the picture smaller (a JPEG is much smaller than a PNG). |
| W x H pixels: the longer side is at most 1600 pixels | Make the picture at most 1,600 pixels on its longer side. |
| not a PNG or a JPEG file | The file is another kind of picture with a `.png` or `.jpg` name; save it as a real PNG or JPEG. |
| named by FILE but not in the folder | The post names a picture that was not uploaded to `posts/` (or the name differs: check the spelling). |
| screenshot "NAME" is not a picture file name of this folder | A screenshot name may hold letters, digits `.` `-` `_` only and must end in `.png`, `.jpg` or `.jpeg`; no folders, no addresses. |
| screenshot "NAME" left out: a post shows at most 3 pictures | Name three pictures at most. |
| the text is longer than 4000 characters: cut | Shorten the text; the post is shown, cut at 4,000 characters. |
| only the newest 20 posts are shown | Nothing is wrong: the game keeps the newest 20 posts. |

The file names `README.md` and any starting with `_` or `.` are never read as posts: use `_notes.md` for notes.
