# Onboarding to the ROOST Model Community

A short orientation for people new to the ROOST Model Community (RMC) and to ROOST's work on open safety models. It explains what ROOST does with open safety models, what the RMC is and how to take part, and where Pigeon (the model translation layer) fits in.

This guide is a map, not the full story. Two documents in this repo go deeper, and you should read them next:

- [ROOST Model Community README](README.md): the RMC's mission, partners, membership, and how to get involved.
- [RMC Guide to Using Open Safety Models](resources/RMC%20Guide%20to%20Using%20Open%20Safety%20Models.md): how open models apply across a trust and safety architecture, with case studies.

## What ROOST does with open safety models

Trust and safety teams have relied on machine learning to find policy violations for a long time, but safety-tuned AI models now make it possible to detect and classify harmful content against custom policies far more flexibly than before. Those capabilities have mostly been available only to well-resourced organizations. ROOST's goal is to change that by making the models openly accessible and wiring them into open source safety tooling, so smaller platforms, individual developers, and self-hosted communities can use them too.

ROOST organizes safety work around the DIRE framework: Detection, Investigation, Review, and Enforcement (see the [RMC Guide](resources/RMC%20Guide%20to%20Using%20Open%20Safety%20Models.md) for the full breakdown). Safety-tuned models help across all four stages and are strongest at Detection and Review. ROOST's part of the work has three threads that reinforce each other:

1. **Community.** The RMC connects the people who use open safety models with the people who build them.
2. **Models.** ROOST partners with model creators who openly release safety-tuned model weights that are free, platform-agnostic, and free of commercial or output restrictions.
3. **Tooling.** ROOST builds open safety tools ([Coop](https://github.com/roostorg/coop) for review and [Osprey](https://github.com/roostorg/osprey) for real-time rules) and is prototyping ways to plug open models directly into them.

## The ROOST Model Community (RMC)

The RMC's mission is to make open safety AI models accessible and beneficial to the safety community. It is built for developers trying to make their platforms safer and curious about how AI models can help, whether they sit in a formal trust and safety role or run a self-hosted platform on their own. Members get a community of trust around vetted models, education and implementation support, and a direct line to model creators for feedback.

A few things worth knowing early:

- **What "open safety model" means here.** ROOST treats an open safety model as one that is free to access, platform-agnostic to deploy, and fine-tuned specifically for trust and safety. The [README](README.md#whats-an-open-safety-model) covers the reasoning, including why non-commercial and output-restricting licenses are a poor fit for the teams the RMC supports.
- **RMC Partners.** Partners are model creators whose models meet the RMC's eligibility bar. Current partners are Mila (suicide-prevention output guardrail), OpenAI (gpt-oss-safeguard), and Zentropi (CoPE-B). See the [README](README.md#rmc-partners) for links and partner benefits.
- **How to take part.** Join the bi-weekly office hours, drop into project sprints, start or join a discussion, open an issue, or chat in the [Discord server](https://discord.gg/UXmBqy7kFX). None of it is obligatory; engage as much as suits you.

### Finding your way around this repo

The [README's "Navigating this repo" section](README.md#navigating-this-repo) lists everything. If you are brand new, a good reading order is:

1. This guide, then the [README](README.md).
2. The [RMC Guide to Using Open Safety Models](resources/RMC%20Guide%20to%20Using%20Open%20Safety%20Models.md).
3. A partner model folder that matches your interest: [gpt-oss-safeguard/](gpt-oss-safeguard), [cope-b/](cope-b), [mila/](mila), or [shieldstral/](shieldstral).
4. The cross-cutting [resources/](resources) and demo [projects/](projects).

## Pigeon: the model translation layer

Every open safety model has its own shape: different input formats, different ways of expressing a policy, and different outputs. Today an adopter who wants to try a new model, or swap one for another, has to wire each one up by hand, and the same is true for the tools that call them. That friction is the problem [Pigeon](https://github.com/roostorg/pigeon) exists to solve.

Pigeon is prototyping open-weight safety models as [Coop](https://github.com/roostorg/coop) signals and [Osprey](https://github.com/roostorg/osprey) rule functions. Its first milestone is to standardize YAML-based model specs so that open safety models become plug-and-play: a tool or adopter describes a model once in a common format, and any compatible model can drop into the same slot without custom integration work.

Where it stands:

- **Early prototype.** Pigeon is explicitly not production-ready. Prototyping happens on the [`prototype` branch](https://github.com/roostorg/pigeon/tree/prototype), and the shape of the project is still being decided.
- **A "Now" item on the ROOST roadmap.** It sits under the Detection pillar; the current focus is [aligning on the approach](https://github.com/roostorg/pigeon/milestone/1) rather than shipping.
- **Where to help.** Chime in on the repo's [issues](https://github.com/roostorg/pigeon/issues) and [discussions](https://github.com/roostorg/pigeon/discussions), or join [#pigeon](https://discord.gg/JkSpezAnp6) in the ROOST Discord.

How this relates to the RMC: the RMC curates and supports the models themselves and the community around them, while Pigeon is about standardizing how tools and adopters talk to those models. The two are complementary. A model vetted through the RMC is exactly the kind of model Pigeon aims to make interoperable.

## Where to go next

- Read the [README](README.md) and the [RMC Guide to Using Open Safety Models](resources/RMC%20Guide%20to%20Using%20Open%20Safety%20Models.md).
- Explore the ROOST tools that open models plug into: [Coop](https://github.com/roostorg/coop) and [Osprey](https://github.com/roostorg/osprey).
- Follow [Pigeon](https://github.com/roostorg/pigeon) if model interoperability is your interest.
- Join the [Discord server](https://discord.gg/UXmBqy7kFX) and the bi-weekly [office hours](https://github.com/roostorg/model-community/discussions/categories/office-hours).
- Questions about partnering a model: email hello@roost.tools.
