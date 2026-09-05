# I Made a Complete AI-Animated Series With Open-Source Tools — Here's the Full Pipeline and Every Tool I Used

Most "AI animation" posts stop at a single generated clip. This is the story of an actual finished series — 12 episodes, consistent characters, a real story arc — and the exact pipeline that produced it. No magic button. Every tool named, every setting documented, every cost accounted for.

## The Series: Nine Turns of the Crimson Heavens

"Nine Turns of the Crimson Heavens" (九转丹霄) is a Xianxia-style AI-animated web series. Twelve episodes, each 1-5 minutes long, in vertical format (1080x1920) optimized for mobile viewing. Every frame is AI-generated. Every voice is AI-synthesized. The story follows Su Chen, a young man whose village burns, who is saved by an immortal cultivator, and who must walk the path of the Nine Turns to survive.

It's not a tech demo. It's a watchable show.

**Watch the free 30-second sample (no signup):** [https://chfr1982.gumroad.com/l/hrscll](https://chfr1982.gumroad.com/l/hrscll)

## The Pipeline: Six Stages, All Open-Source

### Stage 1: Script → Shot-by-Shot Breakdown

The source material was a Xianxia novel outline. Each episode was broken into a shot list: scene description, character, emotion, camera angle, estimated duration. This is the cheapest stage and the one most people skip — and it's where the entire episode's quality is decided.

A shot list entry looks like:

```
Scene 1: Village at night, warm light from windows
Character: Su Chen (young, determined face)
Emotion: Calm before the storm
Camera: Wide establishing shot, slow zoom
Duration: 4s
```

### Stage 2: Character Frames with SDXL + Custom LoRA

This is the core. Without character consistency, AI animation is a slideshow of different people.

**Tools:**
- **Stable Diffusion XL** as the base model
- A **custom-trained LoRA** on 30 character reference images for the protagonist
- **ComfyUI** as the generation frontend, with a modular workflow

**Key settings:**
- Resolution: 1080x1920 (vertical)
- Sampler: DPM++ 2M Karras, 30 steps
- LoRA weight: 0.7-0.8 (too high fries the composition, too low loses the face)
- Batch size: 10-20 frames per run

The LoRA was the single biggest quality jump. Before training it, every frame produced a different-looking character. After, Su Chen stayed recognizable across all 12 episodes.

### Stage 3: Animation via Ken Burns + Parallax

AI image-to-video models (Kling, Runway, Pika) are still inconsistent for long-form animation — they hallucinate, warp, and lose character identity after 3-5 seconds.

Instead, I used:
- **Ken Burns effect** (programmatic pan + zoom) on static frames
- **Parallax layers** — background and foreground separated, animated at different speeds
- **Motion graphics overlays** for effects (sword slashes, energy auras, particle systems)

This gives full control over pacing and doesn't require expensive video generation models. The result looks intentional, not like a glitchy AI video.

### Stage 4: TTS Voiceover

Chinese voiceover was generated using TTS. The script was broken into dialogue chunks, each synthesized separately, then timed to the animation.

**Tips that actually matter:**
- Keep dialogue chunks under 15 seconds for natural pacing
- Use SSML tags to control emphasis and pauses
- Generate 3 takes per line and pick the best one — costs nothing, saves everything

### Stage 5: Compositing in Blender

Blender handled final assembly:
- Layered frames + motion effects + text overlays
- Color grading for consistent visual tone across episodes
- Export to MP4 (H.264, 1080x1920)
- Hardcoded subtitles for non-Chinese speakers

### Stage 6: Publishing

The series is published on Gumroad with a deliberate funnel structure:
1. **Free 30s sample** (no email wall) — lets people see the quality before committing
2. **Episode 1** (Free) — no-risk entry point, full first episode
3. **Complete 12-episode season** ($4.99, 50% off with SEASON50 code) — for binge watchers
4. **AICG Animation Production Handbook** ($1.99, 50% off with LAUNCH50 code) — for people who want to build their own pipeline

## What It Actually Costs Per Episode

| Stage | Cost share | Notes |
|---|---|---|
| Script | Negligible | Prompt + outline time |
| Frames (SDXL + LoRA) | ~60% | Electricity + compute time |
| Voiceover (TTS) | ~10% | Per-minute pricing |
| Compositing | ~20% | Blender is free; time is the cost |
| Assembly + Export | ~10% | Mostly automated |

Total per-episode cost runs in the **low tens of dollars**. A traditional animation studio's per-episode budget starts at hundreds or thousands. The pipeline is what makes this possible — not any single model, but the structure that lets each stage be cheap, repeatable, and automated.

## What I Learned (That I Wish Someone Had Told Me)

1. **Character consistency is everything.** Without a LoRA, AI animation is a slideshow of strangers. Train the LoRA early. It's the highest-ROI step in the entire pipeline.

2. **Control beats realism.** Ken Burns + parallax gives you cinematic control that AI video models can't match. You decide the pacing. You decide the zoom. The result looks directed, not random.

3. **The pipeline matters more than any single model.** SDXL, ComfyUI, TTS, Blender — each piece is replaceable. The pipeline structure is what makes it scalable. Swap any tool and the pipeline adapts.

4. **Vertical video is the format.** 1080x1920 works for mobile, YouTube Shorts, TikTok, and the Gumroad preview player. Don't fight it.

5. **The free sample is the most important product.** It's not a giveaway — it's the top of the funnel. Every product description links to it. Every social post points to it. It's how strangers become buyers.

## Watch It / Build Your Own

- **Free 30s sample (no signup):** [https://chfr1982.gumroad.com/l/hrscll](https://chfr1982.gumroad.com/l/hrscll)
- **Episode 1 (Free):** [https://chfr1982.gumroad.com/l/lrruav](https://chfr1982.gumroad.com/l/lrruav)
- **Complete 12-Episode Season ($4.99, use code SEASON50 for 50% off):** [https://chfr1982.gumroad.com/l/vvbxej](https://chfr1982.gumroad.com/l/vvbxej)
- **AICG Animation Production Handbook ($1.99, use code GUIDE50 for 50% off):** [https://chfr1982.gumroad.com/l/aicg-handbook](https://chfr1982.gumroad.com/l/aicg-handbook)
- **Vertical Manhua AI Toolkit ($0.99):** [https://chfr1982.gumroad.com/l/vsrbx](https://chfr1982.gumroad.com/l/vsrbx)
- **White-Label AI Animation Suite ($2.99):** [https://chfr1982.gumroad.com/l/uanaek](https://chfr1982.gumroad.com/l/uanaek)

The handbook covers the entire pipeline in detail — ComfyUI workflow setup, LoRA training, motion graphics techniques, TTS integration, and Blender compositing. If you're building AI animations, it's the manual I wish I'd had.

---

*This is a real production pipeline, not a concept demo. Every tool named above is open-source or free-tier. Every cost figure is from actual production runs. If you have questions about any stage, the comments are open.*
