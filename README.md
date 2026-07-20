# 🧩 Prompt Add-Ons

**Small, surgical prompt snippets that fix the specific way AI image/text generators fail.**

Most prompts fail quietly. You ask for a "translation" and get grammatically correct, emotionally dead text. You ask for "add this to the photo" and get a lighting mismatch that screams *fake*. You ask for "make it look like the 80s" and get a sepia filter slapped on modern clothes.

The model didn't misunderstand you — it just did the *literal* thing instead of the *intended* thing.

An add-on is a short block of text you paste **after** your main instruction to close that gap. Not a new prompt. Not a framework. Just the missing sentence that tells the model what you actually meant.

```
[your instruction]  +  [add-on]  =  the result you actually wanted
```

---

## Why this exists

Every add-on here started the same way: I hit a wall, got a technically-correct-but-wrong output, figured out *why* it was wrong, and wrote the fix as a reusable snippet. This repo is that collection.

No theory. No prompt-engineering jargon for its own sake. Just: *here's the problem, here's the sentence that fixes it.*

---

## How to use an add-on

1. Find the add-on for your task below.
2. Copy the block.
3. Paste it right after your normal instruction.
4. Fill in any `[bracketed]` placeholders.

**Example:**

> Translate this manga into English.
>
> *[paste Cultural Localization Add-on here]*

That's it. No special tools, no plugins — works with any image/text generator that takes a prompt.

---

## 📚 Add-On Index

| Add-on | Fixes this problem |
|---|---|
| [Cultural Localization](./addons/cultural-localization.md) | Translations that are technically correct but emotionally flat — jokes, tension, and subtext get lost even when every word is "right." |
| Text Legibility & Font-Matching *(coming soon)* | Replaced text that looks pasted-on instead of matching the original font weight, style, and texture. |
| Lighting & Shadow Consistency *(coming soon)* | Composited objects/people that don't match the scene's light direction or color temperature. |
| Era-Accurate Restyling *(coming soon)* | "Make it look like the 80s" turning into a filter instead of accurate clothing, hair, and grading. |
| Idiom-to-Visual Translation *(coming soon)* | Visual puns/gags that die in translation because only the text got translated, not the joke. |
| Brand/Product Consistency *(coming soon)* | Logos and label text subtly warping during background/lighting edits. |
| Emotional Expression Preservation *(coming soon)* | Style transfers that flatten a subtle facial expression into a generic one. |
| Regional Sign/Menu Realism *(coming soon)* | Signs/menus translated word-for-word instead of restructured the way locals actually format them. |
| Body Language & Gesture Localization *(coming soon)* | Gestures that mean something different (or nothing) in the target culture. |
| Age/Generation-Appropriate Slang *(coming soon)* | Dialogue translated into "correct" language instead of how that character would actually talk. |
| Panel Flow & Reading Direction *(coming soon)* | Manga translated right-to-left → left-to-right without fixing panel/reading order, breaking the story flow. |

---

## 🗂 Repo structure

>constantly changing

Each add-on file follows the same format:

```
## [Add-on Name]

**Problem:** What goes wrong without it, in one or two sentences.

**Add-on prompt:**
> The actual copy-pasteable snippet.

**Use after:** Example of the instruction it pairs with.

**Example:** Link to before/after in /examples, if available.
```

---

## Contributing

Found a failure mode with a clean fix? Open a PR.

Good add-ons are:
- **Problem-specific** — solve one failure mode, not five
- **Copy-pasteable** — no setup, just text
- **Short** — if it needs a paragraph of explanation to use, it needs more editing
- **Proven** — you've actually seen it fix the output, not just theorized it would

---

## License

MIT — use these anywhere, no attribution required. Attribution appreciated though 🙂
