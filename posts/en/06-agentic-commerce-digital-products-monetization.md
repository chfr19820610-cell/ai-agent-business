# The AI Donghua Pipeline I Actually Run, Costs and All.

I make AI-generated animated episodes and sell them and a few digital products. People ask how, assuming there's a trick. There isn't one. There's a pipeline, and it's specific enough to describe.

The production line runs through a few stages, each owned by a different tool or agent:

1. A script draft from a source outline.
2. Frames generated from each shot's description, then upscaled.
3. Voiceover from the script.
4. Assembly, captions, and export into a finished episode.

The reason the economics changed isn't a magic button. It's that each stage used to need a specialist, and now each stage can be pointed at by a prompt with a fixed cost. I can tell you the actual numbers for a single episode in my setup: the frame generation alone used to be the expensive part, and switching to a cheaper model with upscaling cut that line item by roughly an order of magnitude per episode. Total production cost per episode now runs in the low tens of dollars, versus the hundreds or thousands a studio's per-episode budget starts at. Those are my numbers, and yours will differ based on models, length, and how much you redo shots.

The business side is plainer than the production side. I sell the episodes on one channel, and digital products on Gumroad, because a digital product has no inventory and no shipping, and the marginal cost of another copy is zero. That's not a miracle of passive income. It's that the per-unit cost is basically zero, so every sale past the first is nearly all margin. Small numbers, repeated, are the whole model.

Two things I'd do differently if starting over, and they're concrete:

- Set a hard cap on redo rounds per shot. The biggest time sink is an agent regenerating the same frame forever. Two passes max, then take the best one.
- Version the pipeline as code from day one, so you can rerun any episode's build instead of rebuilding it by hand.

If you want the exact script-to-export setup with the tools and prompts, I've written it out and it's on my site. It's the same process I run, and if something breaks in it, that's documented too.

#AIDonghua #Gumroad #DigitalProducts #CreatorEconomy #AIAgents
