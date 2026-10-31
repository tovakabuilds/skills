# The formats file (reference for every skill)

A business is not one format. The brief says who the business is; a format says how one kind of post gets made. Each business keeps its own `formats.md` beside its `brand-brief.md` in the project. Formats never cross businesses.

## Shape of one format

```
## <Format name>
- status: active | pending | retired
- purpose: what this lane is for, in one line
- when: topics or moments that fit (and any slot, for example morning)
- hook pattern: the hook types that fit, plus any hook rule for this lane
- beats: the structure with rough seconds
- look: style, colors, motion, character or style refs (file paths or links)
- voice: voice, speed, delivery notes
- cta rule: which live offer, keyword or Follow ends it
- first-frame rule: anything this lane adds to the standard first-frame check
- platform versions: what each platform gets (the full carousel, a complete shorter carousel, a reel made from the slides, or the same video); leave it out to use the defaults below
- run rule: who decides when this lane runs (default: the factory may propose it)
- winners: dated lines from save-winners
```

## Rules
- Only `active` formats are used. `pending` formats are never used until the owner confirms them in the conversation.
- A new or changed format follows one order, everywhere (content-factory and study-format use the same one):
  1. Draft the whole format.
  2. Show it to the owner whole.
  3. If the owner wants to keep it, save it as `pending`.
  4. It becomes `active` only on the owner's explicit confirmation.
  5. A run that is waiting on it continues only after it is active.
- Every platform gets a complete post, never a cut-off one. Each platform is its own post, so its version can differ:
  - Carousel defaults when a format says nothing: Instagram and Threads get the full carousel (up to 10 slides). Facebook gets a reel made from the slides, because carousels show as a grid there; the exception is a post that asks people to comment about a numbered slide, which stays photos with a caption telling people to tap through them. Bluesky (at most 4 images) gets a complete version of 4 slides or fewer that tells the whole story, or one summary image.
  - A reel made from slides holds each slide long enough to read twice, opens on the headline in frame 1, and gets its own cover.
  - Never drop the slides past a platform's limit and post the rest.
- A format cannot override the brief: never_say, facts and live offers always win.
- If there is no formats file, the factory drafts one on the first run from the business's own past posts (or from examples the owner likes, if there are none), each one going through the order above. A business does not need one set up beforehand.
