---
name: caption-variants
description: 'Write platform-native captions for one post: an Instagram caption, a Facebook version, a text-first Threads post and a short Bluesky post, each inside the limits the Tovaka Scheduler reports. Use when someone says "write the caption", "captions for all platforms", "hashtags", or "make a Threads version" or "a Bluesky version".'
argument-hint: "[script or post summary]"
user-invocable: true
---

# Caption Variants

One post, four native captions. Not one caption pasted four times.

## When to use
After builder, or on its own for any post. The factory runs it at step 8.

## What you'll need
The script or post summary, the call to action, and the brief (voice, offers, facts, never_say). Platform limits come from `get_business`; if it is not connected, use the defaults below.

## Instructions
- **Instagram.** First line repeats the hook's promise in new words (it shows above "more"). Then 2 to 5 short lines of value, the call to action, then hashtags if the brief uses them (default 3 to 5, relevant, no banned or generic tags). No links: Instagram captions cannot carry them; write "link in bio". Limit 2,200 characters and 30 hashtags (the scheduler also applies any lower brand hashtag cap).
- **Facebook.** Reads like a person talking to a neighbor: fuller sentences, fewer or no hashtags. A link is allowed if the brief's offers include one. The platform limit is very high; keep it short anyway.
- **Threads.** Text first and conversation starting: a short take or question someone wants to answer, not a shrunk Instagram caption. Hard limit 500 characters including spaces, and at most 1 hashtag. Count the characters and report the count. The scheduler refuses anything over the limit rather than cutting it, so never rely on it to trim. If the business has no Threads account connected in `get_business`, still write it but say it will not queue.
- **Bluesky.** Short and plain, written for Bluesky's own readers: one clear point or question, not a cut-down Instagram caption. Hard limit 300 characters, counted as a person sees them (an emoji counts as one); use the limit `get_business` reports if it differs. Hashtags are optional, at most 1 or 2. A link is allowed if the brief's offers include one. Count the characters and report the count. The scheduler refuses anything over the limit rather than cutting it. Media: text alone, up to 4 images, or one video. If the business has no Bluesky account connected in `get_business`, still write it but say it will not queue.

Write each caption for the version that platform actually gets (see the format's `platform versions`): a reel made from the slides on Facebook reads as a video, Facebook photos for a comment-a-number post say to tap through the photos, and a shorter Bluesky carousel is described as its own complete post.

Output each caption in its own block with its character count and hashtag count. Each platform is queued as its own `create_post` (same `post_group`), so each caption must stand alone.

## Rules
- Same call to action across platforms, written natively for each.
- Every claim needs a `facts` line; nothing on never_say.
- If a comment keyword is the call to action, write it exactly as the brief has it.
