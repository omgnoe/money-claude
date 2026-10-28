# AI Content Playbooks

Tactics distilled from dozens of public YouTube and TikTok creators who teach making money with AI. Inflated revenue numbers are marked **[hype]**; the reusable tactic underneath is kept. This is a map, not a promise.

Cross-cutting truths that show up everywhere:
- **Distribution beats the artifact.** The system around the code/site/model/prompt wins. Prompt is ~10%, harness is ~90%.
- **Most revenue claims are funnels** for a tool, course, or community. Separate the tactic from the number.
- **Prove demand before building** (a waitlist with a paid deposit beats a built product nobody asked for).
- **Biggest personal risk is shiny-object syndrome.** Focus until traction.

---

## 1. Building and monetizing apps

- **Don't chase the original idea.** Copy existing paying demand and make it ~10% better. Pull feature gaps from 1-3 star competitor reviews.
- **SLC over perfect**: Simple (1-2 core features), Lovable (it must look good), Complete (those features work). Don't scale or perfect prematurely.
- **Premium is proof, not polish.** What makes an app feel premium is the unglamorous states AI tools skip: undo, error recovery, "what is happening right now". The cheapest lever: deliberately break the product and design the recovery.
- **Paywall is a flow, not a screen.** Multi-page beats single-page; a longer trial often beats a discount; reducing *perceived risk* beats removing friction. A dual paywall (soft during onboarding, hard at the first real action) tends to beat one hard wall.
- **Conversion pages: simpler wins.** A/B tests repeatedly favor the plain screen, concrete benefit copy over cute copy, "1 month" over "30 days".
- **Churn is predictable.** Score each user's return probability from simple signals (how they open the app, number of actions, last use) and time a reminder to the right moment, instead of spamming.
- **Distribution is the moat.** Find one viral format, then scale it mechanically (revenue roughly = views x conversion).
- **Exit is real but slow.** Marketplaces price small apps/games around ~24x monthly profit, but want 6-12 months of revenue history and low maintenance. [hype] the "$400k/mo" titles; the method is real.

## 2. AI ads and video (image/video models + an agent)

Core idea: build an **asset chain** once, then reuse it. Hero image -> reusable elements -> video -> upscale -> ads. Each step builds on the last.

- **Start from one strong hero image** (full body, used as the reference for everything). Worth regenerating a few times.
- **Reusable elements**: generate a character, a product, and a location once, save each as a named reference, then pull them into any prompt by tag. Build every element on the **same model and resolution**, or consistency breaks.
  - Character sheet: front + back + close-up on a plain gray background with flat light (dramatic light bakes into every later shot). Erase extra faces from the full-body panel so the video model does not drift. For state changes (dry vs wet), build two sheets, not one you describe into.
  - Product: plain background, big simple wordmark (text is where image models fail).
  - Location: generate it empty (no person), or the model has two people to choose from.
- **Shoot angles cheaply.** A "generate N best angles" tool rebuilds one scene from many camera positions with consistency, far cheaper than N separate generations. Run it twice and swap out glitched frames.
- **Video**: leave the start frame empty and run text-to-video with elements as references (a fixed start frame locks your composition). Name each shot's lens/angle in **degrees** (an actual field of view the model can act on); "cinematic wide shot" gets ignored.
- **The shot-list hack**: never write prompts by hand at scale. Teach the agent (via a skill/file) to write a single connected shot list with a style-prefix block at the top (change once, changes everywhere) and named prompts (edit one without touching the rest).
- **Position map hack**: to lock object positions/sizes across takes, give the model a schematic/map ("mark the hydrant, lock the object to its right, 2x person height") instead of brute-forcing 20 generations.
- **Consistency tricks**: color-transfer from one reference keeps a whole film one palette; "clean the plate" (edit out text/clutter the video model breaks) before generating; a short video is often the best image editor because every frame matches by definition.
- **Choreography**: "he dances" means nothing; spell out moves, or drop the actual music track as an input and ask for on-beat motion.
- **Iteration is the skill.** The finished ad is the best few seconds out of ~100 tries, cut together. [hype] "one prompt, done".
- **Upscale only final cuts** (it is slow and costs credits); use a detail-rebuilding preset, not a sharpener.
- **Motion graphics**: agent + motion tooling can produce editable 2D/3D motion graphics, exportable to After Effects/Blender; regenerate only the shots you want to fix to save credits.

## 3. Short-form and faceless video

- **The algorithm is consistent across platforms**: a seed audience plus a hidden trust score, "test and expand", daily consistency. A verified/aged account and eligibility matter; falsely marking "made for kids" kills a channel.
- **Hook in the first seconds**: show the result or stake immediately, open a loop, resolve it at the end. A roleplay hook (make the viewer a character in second one) travels well.
- **Structure**: hook / message / metaphor / conclusion, with a visual change every few seconds.
- **Packaging before production**: title and thumbnail decide ~80% before anyone clicks. Generate many title options, pick three; test 3 thumbnails; keep text minimal so it works across languages. Study already-high-performing thumbnails in the niche and adapt proven concepts to your brand/face, rather than generating something merely pretty (pretty and high click-through rarely correlate).
- **Dubbing** multiplies what already works; it does not save a weak video.
- **Monetization reality**: real short-form RPMs are roughly $0.2-$0.5 per 1,000 views in tier-1 regions; **clipping** pays roughly $1 per 1,000 eligible views. [hype] the "$30k-$120k/month" systems are mostly ads for communities and affiliate tools; your own image/video + agent stack usually replaces the tools they sell.
- **Clipping as a service** scales from pay-per-view campaigns, to a monthly retainer for creators with long content but no shorts, to full content strategy. The honest edge is speed and selection.

## 4. AI personas

- **The common formula**: take a proven viral format and swap in a consistent AI character (via image/video models driven by an agent). A pattern-interrupt character (mascot or unexpected persona) can beat a generic attractive model.
- **Consistency and realism**: a 360 reference sheet and many reference images for face consistency; draft at low resolution first, then upscale the keepers (saves credits); pick the model by purpose (one for people, one for locations, one for motion).
- **Monetization**: digital products (audience-first, a single-purpose web app, price only after a demand test), affiliate and shop links, brand deals, selling the account.
- **Ethics and platform rules matter.** Many platforms restrict undisclosed or fully-synthetic accounts; always label AI content, never fabricate experts, hardships, or results. Adult/"AI OnlyFans" monetization is manipulative and against most platform terms; skip it. Keep the neutral technique, drop the deceptive model.

## 5. Offers and client acquisition

- **Research and prospect in the same ad library.** Public ad libraries show how long an ad has run and its reach: long-running, high-reach ads are the likely winners, so copy those patterns. The same library lists businesses already spending on ads: reach them via the advertiser card. They already pay for ads, so they listen. You take the "what ad do we run next?" loop off their plate.
- **Copy frameworks**: for e-commerce, a proof-led structure (callout diagram, review card, offer card); for services, a quest structure (quiz, case-study-as-story, direct offer with a guarantee). Services formula: hook a pain point -> show the end result -> close with a high-value free lead magnet that filters for qualified leads.
- **Niching down raises price** (a general course vs a specific-audience program).
- **The simplest ads convert best.** Don't over-complicate visuals.
- **Test organically first** (post as organic reels, see what gets interest), then scale winners. For A/B tests, never rebuild a working ad from scratch; export its performance report and vary one element at a time.
- **Package it**: e.g. a fixed number of videos per month as a retainer. An AI-automation service for local small businesses is a strong fit for a solo operator with an agent stack.
- **Validate before inventory**: scan a niche, derive the product angle from real review complaints, build a waitlist page with the content, and only produce once demand is proven. [hype] the "6x ROI in days" math usually counts unrealized waitlist signups, not delivered sales.

## 6. Content automation with an agent

- **A content factory as a skill**: a four-stage pipeline the agent runs end to end: research (what is trending/converting in the niche) -> content plan (a dated production calendar) -> generate (images and videos, with a permission gate per batch so you approve as it goes) -> schedule (into ad campaigns). One window, the agent already knows the brand, so no re-prompting.
- **Thumbnails as a repeatable system**: agent researches top-performing thumbnails in the niche, writes a design brief you review, then generates several variations. Record a short video of yourself moving in all directions and extract stills as a reusable "face bank".
- **Package any working workflow as a skill/command** so it becomes one invocation.

---

### Sources and honesty
These notes summarize publicly posted content from many creators for educational purposes. Credit stays with the originals. Where a creator's numbers could not be verified, or where the claim exists to sell a tool/course/community, it is marked **[hype]**. The tactics are what to keep.
