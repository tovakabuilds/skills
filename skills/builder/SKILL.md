---
name: builder
description: Turn a script into a beat-by-beat build sheet (voiceover, on-screen text, visual, timing), render it with the owner's own editing tools if they have them, and run the first-frame check (motion plus a complete claim in the first second, a visual change every 2 to 3 seconds, the picture lands on the exact word, no banned words in real screenshots, nothing over a face). Use when someone says "build the reel", "make the video", "beat sheet", or "check my first frame".
argument-hint: "[script, or a finished video to check]"
user-invocable: true
---

# Builder

From script to something watchable, then a hard check on the first seconds, where most short videos are lost.

## When to use
After scripter. Also standalone to check a video the owner already made. The factory runs it at step 7.

## What you'll need
The script table and the brief's visual style (voice field and notes: colors, fonts, pace, look). Tools are optional: use whatever the owner already has (a video framework like HyperFrames or Remotion, a voice clone, an editor, a phone). Do not ask them to buy or install anything new. With no tools, the output is the build sheet for a person to film and edit.

## Instructions
1. **Beat sheet.** One row per visual change:

| Beat | Start to end (s) | Voiceover words | On-screen text | Visual | Motion |
|---|---|---|---|---|---|

   Beats should be 2 to 3 seconds. The visual for a beat starts on the word it shows, not before or after.
2. **Style.** Apply the chosen format's beats, look, refs and voice, inside this business's brief. Never borrow another business's look.
3. **Image brief.** Before generating any image, write one image brief per picture and keep it with the build sheet: subject, framing (where faces and bodies sit), setting, light, colors from the brief, aspect ratio, and what must never appear (never_say words, other brands, real client faces without consent). Every tool works from this same brief, so a backup tool continues the job without changing the creative direction.
4. **Image fallback order.** Decide this by what each tool can do, not by vendor name, and only from tools the owner already has and has allowed for this business:
   1. The owner's primary image tool.
   2. Another image tool the owner already has access to and has said may be used (for example an image model inside another agent they run).
   3. The owner's own photos or footage, or stock they already hold rights to.
   4. Stop and ask the owner.

   Move down the list only when a tool is unavailable (down, rate limited, out of credits, refused). Say which tool failed and which one takes over, then continue from the same image brief. Never buy, upgrade, top up or spend credits beyond what the owner already allowed, and never switch silently.
5. **Render** (if tools exist). Voiceover first, then time captions and cuts to the real word timings (a speech-to-text pass with word timestamps, such as Whisper). Use the voice and speed the brief or owner sets.
6. **Placement per photo.** Do not assume one fixed layout. For each photo, place text cards, stickers, tape and other overlays where that photo has room, and vary placement between photos as needed. Two rules hold on every frame: a card never covers a face, and tape never crosses a body.
7. **First-frame check.** On the render (or the beat sheet if there is no render), pass or fail each:
   - **Motion in the first second.** Something moves in frame 1. A still title card fails.
   - **Complete claim in the first second.** The opening text or line makes sense alone.
   - **Visual change every 2 to 3 seconds.** List any gap over 3 seconds with its timestamps.
   - **Picture lands on the exact word.** List any visual that arrives early or late against the word timing.
   - **Format rule.** Anything the chosen format adds to the first-frame check.
   - **Readable.** On-screen text stays clear of the platform's top and bottom bars and is on screen long enough to read.
   - **Never-say in real screens.** Read every visible word inside real screenshots, app or UI captures and photos of signs or packaging, including the first frame, and check them against the brief's never_say (and claims without a `facts` line). Menus, sidebars, badges, footers and banners count. Fix a hit by using a clean copy of the screen (for example a demo account or a setting that hides it) or by cropping or plainly masking it out. Never edit a real screen so it shows something the product does not do.
   - **Faces and bodies.** No card covers a face and no tape crosses a body, in any frame. List each fail with its timestamp and the photo.
8. Fix every fail and check again. Report the final results as a short pass list with timestamps.
9. **Platform versions.** Make each platform's complete version from the format's `platform versions` line, or the defaults in FORMATS-FILE.md: for a carousel, the full set, a complete shorter set for a platform with a lower slide limit (Bluesky 4), and a reel made from the slides where the format says so (Facebook by default). Never cut a carousel off at a platform's limit. Run the first-frame check on every reel you make this way, and watch it end to end (one frame per second is enough): every slide must appear, in order, for its full hold. In a reel made from slides, each slide's hold (long enough to read twice) replaces the 2 to 3 second visual change rule, as long as something moves on screen.

## Output
The beat sheet, the image briefs, which image tool made each picture (and any fallback taken, with the reason), the file path of any render with its type and size, the version each platform gets, and the first-frame check results.

## Rules
- The check is a checklist, not a forecast. Never call it a virality scan.
- Use only media the owner owns or has rights to.
- Media headed to the scheduler goes through its secure upload (`request_media_upload`, upload to the returned temporary link, `finalize_media_upload`, then the verified asset id in `create_post`; the factory's queue step has the details). Hand on each final file path, its type (JPEG, PNG, MP4 or MOV) and its size in bytes, in slide order for a carousel, and mark a reel cover as the cover (a JPEG). Do not make a public link for it.
