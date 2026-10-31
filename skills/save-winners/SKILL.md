---
name: save-winners
description: After posts have run, find which ones won against the business's own recent average and save what made them work back into the brand brief, so the next batch compounds. Use when someone says "what worked", "save the winners", "review last week", or "which hook won".
argument-hint: "[time window, default the last 7 to 14 days]"
user-invocable: true
---

# Save Winners

Every batch should start from what the last one taught.

## When to use
A week or two after a batch went out. The factory offers it at step 11.

## What you'll need
The posts that ran (`list_posts`, `get_post` for status and live links) and their numbers. If the scheduler does not show metrics, ask the owner for them from their platform insights: views, average watch time, shares or sends, likes, comments, follows. Compare against the business's own last 10 posts, never against other accounts.

## Instructions
1. Build a small table: post, hook type, format, views, watch time, sends per view, likes per view, comments, follows.
2. Winners: clearly above the business's own recent average on watch time and on sends or likes per view. Say how many posts the comparison rests on; under 5 is a hint, not a pattern.
3. For each winner, name what is reusable: hook type, format, angle, first-frame move, call to action. If several hook variants of one topic ran, say which won.
4. Write a short winners block, for example:
   `Winners (Oct 2026): result-first hooks beat questions on watch time; 3-step demo format; comment keyword CTA drew the most comments.`
5. **Per format.** Group results by format. Add a dated winners line under each format in `formats.md`. A format that has lost against the business's average on its last 3 or more posts gets flagged to the owner with the numbers; never retire or change it without the owner's yes.
6. Save the general lesson: show the owner the updated brief, then `save_brand` with the full brief and the winners block added to `notes` (the brief has no separate winners field). It is pending until the owner confirms it in the scheduler. With no scheduler, add it to `brand-brief.md`.

## Rules
- Never save without showing the owner first.
- Report numbers as they are. Do not call a post a winner on likes alone, or on one post.
- Never put client names or private notes into the brief.
