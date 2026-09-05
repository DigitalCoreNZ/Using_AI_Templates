# README: Using AI Templates

This repository contains an example of my workflow for producing YouTube video scripts with AI. It shows you what I built and how I built it, in four stages:

1. My **template prompt**, which specifies how I want the videos template to be built.
2. My **videos template** — the structured style guide that accompanies my script prompt. It carries the (pending) placeholders, my custom production metadata, my immutables, This template provides an AI agent with a structural layout for writing scripts.
3. My **script prompt** identifies the content of a script, and is used in conjunction with the **template prompt**.
4. My **shooting scripts** — the end product, which my AI agent generates using the videos template as the style guide and the script prompt that provides content, context, and direction.

I write my prompts in Markdown (`.md`), my templates and scripts in AsciiDoc (`.ad`), and I based my script-writing structure on the [StudioBinder "Script Writing on YouTube"](https://www.studiobinder.com/blog/script-writing-on-youtube/) article.

## Repository Contents

| File | Description |
| ---- | ----------- |
| [Template_Prompt.md](Template_Prompt.md) | The prompt that results in the [Videos_Template.ad](Videos_Template.ad) |
| [Videos_Template.ad](Videos_Template.ad) | The template that is used with the [Script_Prompt.md](Script_Prompt.md) |
| [Script_Prompt.md](Script_Prompt.md) | The prompt that results in the Recovery Scripts |
| [Recovery_Script_v0.5.1.ad](Recovery_Script_v0.5.1.ad) | "CloneZilla Recovery v0.5.1" — my shooting script for creating a disk image and restoring a system |
| [Recovery_Script_v0.5.2.ad](Recovery_Script_v0.5.2.ad) | "CloneZilla Recovery v0.5.2" — my rewrite of the original script, framed around keeping my system and my data separate so my recovery can be deliberately destructive |

## How My Workflow Fits Together

```
Template_Prompt.md  →  Videos_Template.ad  →  Script_Prompt.md  →  Recovery_Script_v0.5.1.ad  →  Recovery_Script_v0.5.2.ad
```

### 1. My Template Prompt

[Template_Prompt.md](Template_Prompt.md) holds the three conversational prompts that sit behind this
work. The key requirements I set out, in summary:

- **I do not constrain word count** — my template guides the creation process, it does not limit it.
- **I treat the number of scenes as structure, not a boundary.**
- **I build my scene anatomy around AV columns:** each scene carries a Scene Number (which I use in production) and a Scene Title (which is displayed on-screen), and I present it as a table with **Shot | Visuals | Dialogue | Duration**.
- **I default to a Storytelling framework** — my products are YouTube explainer videos, and I find Storytelling (Hook → Conflict → Resolution → Lesson) best suits this style of video.
- **I keep my voice-over style energetic, punchy, enthusiastic, and free of filler** — I capture that in the front matter rather than in the body of my template.
- **I scope my Cold Open and my Review clearly:** I start with my immutable *Open Greeting* ("Tēnā koe e hoa (Hello friend). Haere mai (Welcome).") deliver my hook within 15-seconds, and end with my immutable *Signature Sign On* ("My name is Brian, I'm an AI Generalist, and this is DigitalCoreNZ") **before** the title sequence rolls, and I close my Review with a quick recap, my immutable CTA, and my immutable *Signature Sign Off* ("Until next time: Be safe, be kind, be awesome, kia kaha!!").
- **I give my AI agent production metadata to consume:** specialist front-matter attributes that tell it my scope, my aesthetic, and my guidance.

In the example prompt, I ask for a two-part CloneZilla Live script (part 1: how I create an image; part 2: how I use that image to restore a system, with disclaimers on the destructive nature of a restore, written in the first person and the present tense), and I follow up with my rewrite brief for the v0.5.2 version.

### 2. My Videos Template

[Videos_Template.ad](Videos_Template.ad) is the reusable style guide.

**Highlights:**

- **My front-matter metadata** — my document details, plus a "Video Production Metadata" block (`videoType`, `coreTopic`, `sourceMaterial`, `corePromise`, `framework`, `targetRuntime`, `voiceOverStyle`, `structure`, and so on) that I keep deliberately *out* of the body.
- **My scope for the Cold Open and the Review** — machine-readable definitions of what each of my sections must achieve.
- **My immutables** — `signOn`, `cta`, and `signOff`, which I deliver verbatim, never paraphrased.
- **My scene anatomy** — my "Scene Number: Scene Title" heading convention and my four-column AV table (Shot, Visuals, Dialogue, Duration), including a reusable scene section that I repeat as many times as my topic needs.
- **My fixed structure:** Cold open → Title sequence → Scenes → Review.

### 3. My Script Prompt

[Script_Prompt.md](Script_Prompt.md) is the prompt that, when used with the [Videos_Template.ad](Videos_Template.ad) style guide, results in the My Recovery Scripts.

### 4. My Recovery Scripts

I film my shooting script from my own perspective (first person, present tense), and I base it on the [CloneZilla Live documentation](https://clonezilla.org/clonezilla-live-doc.php).

#### [Recovery_Script_v0.5.1.ad](Recovery_Script_v0.5.1.ad)

> *Create a disk image, and restore my system from it* — v0.5.1, target runtime 12 minutes.

I frame this one as a generic disaster-recovery story ("my hard drive died on a Tuesday"):

- **Scene 1 — One Bad Day:** the conflict that pushes me to make a disk image.
- **Scene 2 — Boot the Rescue Disk:** how I set up my CloneZilla live environment from a USB stick.
- **Scene 3 — Save a Disk Image:** I walk `device-image → local_dev → sdb1 → savedisk`.
- **Scene 4 — The Warning:** I deliver my disclaimers on the destructive nature of a restore.
- **Scene 5 — Restore the System:** I walk through `restoredisk`.
- **Scene 6 — In Review:** I recap, I deliver my CTA, and I sign off.

#### [Recovery_Script_v0.5.2.ad](Recovery_Script_v0.5.2.ad)

> *I separate my system from my data. Restoring my system overwrites everything — and that's the point*
> — v0.5.2, target runtime 12 minutes.

I rewrite this one to line up with my actual setup, where my AI-Generalist work constantly bricks my system and my data is therefore safe on my NAS:

- **Scene 1 — The Warning:** I deliver my strong disclaimer **immediately after the title sequence** — I restore a system from an image and it **OVERWRITES EVERYTHING** on my target drive or partition.
- **Scene 2 — System vs Data:** I show you my 4-drive NAS (4 × 6TB, RAID-5, 18TB usable) and my 5TB external USB drive that backs the NAS up on a schedule — and I explain why that makes destructive recovery safe for me.
- **Scene 3 — Boot the Rescue Disk:** I set up my CloneZilla live environment, with my 5TB USB drive ready for my system image.
- **Scene 4 — Save a Disk Image:** I image `sda` onto `sdb1` with `savedisk`.
- **Scene 5 — Destroy and Rebuild:** I walk through `restoredisk`, and I re-emphasise how destructive that step is.
- **Scene 6 — In Review:** I recap, I land my core promise, I deliver my CTA, and I sign off.

## My Sources

- **My style guide:** [Script Writing on YouTube — StudioBinder](https://www.studiobinder.com/blog/script-writing-on-youtube/)
- **The CloneZilla Live documentation I use:** [https://clonezilla.org/clonezilla-live-doc.php](https://clonezilla.org/clonezilla-live-doc.php)

## License

This repository is distributed under the permissive MIT license.

© Copyright 2020–2026 DigitalCoreNZ. All rights reserved.