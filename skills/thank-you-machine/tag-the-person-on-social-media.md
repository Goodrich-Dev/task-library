---
name: tag-the-person-on-social-media
description: Post the thank-you publicly and tag the person so they see it, feel it, and share it — their reshare carries your gratitude to their entire audience with their endorsement attached.
category: Thank You Machine
stage: Post
definitive_article: /thank-you-machine
status: complete
---

# Tag the person on social media

**Use this when** the thank-you assets are staged and the private send is done — the public post is where gratitude becomes amplification.

## Inputs
- The staged social post (native video + story caption) from the Content Factory step
- The person's **verified** profile handle(s) per platform, from the trigger log
- Access to the brand's social channels (post from the Public Figure page for personal brands)

## Steps
1. Post the thank-you video natively on the platforms where the person actually lives — their home platform first; a tag they never see amplifies nothing.
2. Verify the handle before tagging: right person, right company page. A mis-tag thanks a stranger and embarrasses two people.
3. Write the caption as the story, not a shoutout: who, exactly what they did, why it mattered — the video's three beats in text, for everyone scrolling with sound off.
4. Tag honestly and sparingly: the person, their company if relevant. No tag-wall audience farming — this is gratitude, not growth-hacking cosplay.
5. Work the response window: reply when they comment, answer others, thank the sharers. Comments are the flywheel that tells the algorithm — and the human — this matters.
6. The reshare is the win condition: when the person shares it to their own audience, your gratitude travels their network with their endorsement attached. Don't ask for the share; sincere and specific earns it.
7. Log the post URLs and early signal (their reaction, comments, reshares) in the trigger log, and hand the post to the Dollar a Day boost step.

## Definition of done (QA checklist)
- [ ] Posted natively on the person's home platform(s) with the correct profile tagged
- [ ] Caption carries the three beats (name, deed, why it mattered)
- [ ] Replies and comment threads engaged during the response window
- [ ] Post URLs + recipient reaction logged; winner handed to boost-with-dollar-a-day
- [ ] Linked back to the definitive article and relevant siblings
- [ ] Complies with Blog Posting Guidelines (if it publishes content)

## Example(s)
- Worked example to document: a public thank-you tagging Zach Peyton (Superior Fence & Rail) that he reshared to his own network. Example needed — run the Meta-Article Prompt after first real run.

## Run on a persistent agent (Fable 5)
A persistent agent (Claude Fable 5 or comparable OpenAI/Google models) runs this through the whole response window, not just the post: verify the handle against the trigger log, post natively, work the comments, log URLs and the recipient's reaction — looping until the Definition of done fully passes, because a post with an unverified tag or an unworked comment thread is a failed run.
Memory keeps verified handles and past reactions per person, so a mis-tag never happens twice and the agent learns whose reshares actually travel.
Log each tagged post and its reshare outcome as a meta-article example so the library compounds.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: /thank-you-machine
- Related: /personal-brand (Phase 3 — authority via association) · /social-amplification (engagement signals feed boosting)
- Run order (TYM): process-through-content-factory → **tag-the-person-on-social-media** → boost-with-dollar-a-day
