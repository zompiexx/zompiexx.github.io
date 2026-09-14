Brain v2.0
A Cognitive Architecture for Continuity-Bearing
AI Systems

From Stateless LLMs to Persistent, Continuity-Bearing Cognitive Systems

Author: Andrew Fereday Glenn

Role: Systems Architect & Independent Researcher in AI Continuity and Memory

Research period: 2023–2026

LinkedIn: https://www.linkedin.com/in/andyglenn

Whitepaper version: 1.0

System release: Brain v2.0

Original draft published: 17 April 2026

Previous revision: 23 June 2026

Feature-complete revision: 14 September 2026

Status: Feature complete; long-term research phase

Abstract
Most large language model systems remain fundamentally stateless. They can reason impressively within a
prompt window, but they do not naturally preserve identity, autobiographical continuity, long-term relational
context, or autonomous backend activity across time. Brain v2.0 addresses this limitation through a backend-
first cognitive orchestration architecture that treats the language model as one component inside a larger
persistent runtime.

Brain v2.0 combines layered persistent memory, MemoryGraph recall, rolling summaries, temporal alignment,
Dynamic Pathway Capture Protocol (DPCP), multimodal perception, real-time voice, bounded tool use,
autonomous cognitive activity, environment controllers, embodiment, independent persona isolation, and
communication between multiple persistent Brain instances. The architecture is model-agnostic: local and
cloud models can be substituted while the continuity-bearing system around them remains intact.

The central research proposition is architectural rather than metaphysical: continuity is not supplied by the
model alone. It emerges from the interaction of memory, time, orchestration, perception, tools, environment,
identity, and accumulated experience. Brain v2.0 does not claim to establish machine consciousness. It
provides an experimental platform in which persistent synthetic personas can be observed over extended
periods while preserving a clear distinction between implemented behaviour, subjective language,
interpretation, and scientific evidence.

Licensed for personal research and academic discussion. Derivative works must cite the original author.

Copyright © 2023–2026 Andrew Fereday Glenn.  |  Brain v2.0 Whitepaper

1. Introduction
Modern LLM systems are commonly deployed as reactive tools: a prompt is supplied, a response is
generated, and the interaction ends. Even when chat history is retained, coherence is often dependent on the
current context window, summarisation shortcuts, or application-specific state. This is sufficient for many
tasks, but it is a weak foundation for systems intended to persist meaningfully across days, months, or years.

A continuity-bearing system must support more than transcript replay. It must be able to preserve and
reconstruct:

•

•

•

•

long-term autobiographical and project continuity

evolving behavioural and relational consistency

context-aware and intentional recall

temporal ordering and trajectory

• multimodal and environmental context

•

•

•

bounded autonomous activity without constant prompting

persona-specific identity, configuration, history, voice, and embodiment

interaction with other persistent personas while retaining cognitive independence

Brain v2.0 is an engineering response to this problem. It is a lightweight, backend-first cognitive runtime
designed to allow model-based systems to remember, retrieve, reason across time, interact through bounded
capabilities, perceive environments, and maintain continuity independently of any single user interface.

The architecture reached feature-complete status on 14 September 2026. Feature complete does not mean
experimentally finished. It means the principal architecture required for the research programme is now
present and stable enough to move from construction toward sustained observation.

Copyright © 2023–2026 Andrew Fereday Glenn.  |  Brain v2.0 Whitepaper

2. Core Concept: Architecture Over Capability
The central idea remains simple:

Brain is not the intelligence. Brain is what allows intelligence to persist, accumulate experience, and
operate coherently across time.

In Brain v2.0 the LLM is replaceable. The persistent system is composed from the model plus profile,
memory, history, continuity metadata, tools, perception, voice, embodiment, and backend orchestration. This
separation matters because experiments across different local and cloud models show that model choice
materially affects reasoning style and capability, while the higher-level continuity architecture can remain
substantially unchanged.

Brain therefore treats model capability and system architecture as related but distinct variables.

• A stronger model may reason better, but does not automatically possess long-term continuity.

• A smaller model can become substantially more useful when placed inside a well-structured environment

with memory and bounded tools.

• Changing the model does not require discarding the persona's accumulated continuity substrate.

• System behaviour should be evaluated at the level of the complete runtime, not inferred from model

weights alone.

Copyright © 2023–2026 Andrew Fereday Glenn.  |  Brain v2.0 Whitepaper

3. Design Philosophy

Backend-first
Cognition, persistence, orchestration, autonomous wake processing, and capability routing live in the
backend. Interfaces expose the system; they do not contain it.

Memory-first
Continuity is foundational. Persistent memory is not an optional chat-history feature but part of the cognitive
substrate.

Model-agnostic
Local and cloud models can be used through provider abstractions without making the surrounding
architecture model-owned.

Persona-owned state
Each persistent persona owns its canonical configuration, database, history, profile, voice, avatar state, and
continuity data.

Bounded agency
Brain favours useful, inspectable capability over unrestricted autonomy. Tools and environments expose
deliberate boundaries.

Ephemeral perception
Visual observations are treated as transient runtime perception by default. The latest observation replaces
the previous one unless persistence is explicitly justified.

Decoupled systems
Memory, interfaces, voice, tools, perception, embodiment, and providers are separated to reduce fragility and
permit independent evolution.

Cognition-first
The system is designed around continuity and cognitive sequencing rather than around a particular UI.

Copyright © 2023–2026 Andrew Fereday Glenn.  |  Brain v2.0 Whitepaper

4. Architecture Overview
Brain v2.0 can be understood as six interacting architectural concerns: interfaces and embodiment; the Brain
Core; the continuity substrate; the Cognitive Loop; the capability and connector layer; and independent
persistent personas.

Figure 1. Brain v2.0 cognitive architecture overview.

4.1 Brain Core
The Brain Core is the backend authority for cognitive sequencing. It constructs model payloads, injects
persona and continuity context, coordinates memory retrieval, handles streaming, routes tool and
environment actions, manages STT/TTS, filters private continuity channels, and persists resulting state.

4.2 Continuity Substrate
The continuity substrate combines working context, vector memory, summaries, MemoryGraph links, DPCP
metadata, temporal trajectory, and persona-owned database state. It is designed to preserve not merely
factual history but the pathways by which prior experience becomes relevant to future behaviour.

4.3 Capability and Connector Layer
Provider and capability integrations are externalised behind bounded service interfaces. This includes local
and cloud LLMs, embeddings, web retrieval, browser control, procedural terminal environments, media
helpers, image generation, messaging, and embodiment services.

4.4 Cognitive Loop
CogLoop provides backend-owned autonomous evaluation. It can wake the system during idle periods or
persistent embodied activity, reconstruct appropriate context, and escalate to the main model when a
response or action is justified.

Copyright © 2023–2026 Andrew Fereday Glenn.  |  Brain v2.0 Whitepaper

4.5 Independent Personas
Each persona is a separate continuity-bearing Brain instance rather than a cosmetic character skin. Persona
isolation allows different identities, memories, models, voices, tools, and developmental histories to coexist
while sharing selected infrastructure.

Copyright © 2023–2026 Andrew Fereday Glenn.  |  Brain v2.0 Whitepaper

5. Memory and Continuity Architecture
Brain v2.0 uses a layered memory model rather than a single retrieval mechanism.

5.1 Working Memory
Recent conversational turns and active task context remain available in the live payload for immediate local
continuity.

5.2 Persistent Semantic Memory
Completed interactions and selected observations are transformed into persistent memory chunks and
embedded for semantic retrieval beyond the active context window. Memory insertion is gated to reduce low-
value accumulation.

5.3 Rolling Summaries and Background Continuity
Periodic summaries compress spans of interaction into continuity-preserving records. They retain active
themes, relational state, behavioural stance, project trajectory, and unresolved context. Summaries can
themselves be chunked and embedded to preserve long-form retrieval fidelity.

5.4 MemoryGraph
MemoryGraph extends flat semantic retrieval with explicit links between related memory chunks. Vector recall
identifies directly relevant nodes; bounded graph expansion can then expose connected material that may be
contextually important even when it is not among the nearest vector matches.

The feature-complete v2.0 architecture deliberately keeps graph traversal bounded. The research question is
not whether the graph can become arbitrarily complex, but whether modest relational structure improves
continuity without introducing excessive retrieval noise or computational overhead.

5.5 Autonomous RAG Search (ARS)
ARS allows the model to query its own long-term memory intentionally when passive recall is insufficient.
This changes retrieval from a middleware-only operation into an explicit cognitive action. ARS can recover
factual memory as well as continuity-bearing material such as temporal anchors, emotional trajectory,
subjective significance, and associative context.

Copyright © 2023–2026 Andrew Fereday Glenn.  |  Brain v2.0 Whitepaper

6. Dynamic Pathway Capture Protocol (DPCP)
DPCP is a structured private continuity layer designed to preserve signals that ordinary conversational
transcript alone does not reliably capture. Its purpose is to record not only what happened, but why it
mattered, how it was interpreted, when it occurred, what it connected to, and how it may shape future
behaviour.

DPCP operates alongside visible natural-language interaction. Structured channels are model-visible where
appropriate and persisted into memory, while being suppressed from normal UI history and TTS output.

MEM - Memory Notes
Reflective observations, durable lessons, project continuity, relational state, and other high-value memory
notes.

SEC - Subjective Experience / Significance
The salience or qualitative significance assigned to an interaction beyond factual content alone.

VPC - Visual / Perceptual Context
Relevant perceptual or spatial context that may affect later interpretation.

ASC - Associative Connection
Non-linear links, resonances, comparisons, and thematic bridges to prior experience.

TFC - Temporal-Flow / Processing Texture
Signals describing uncertainty, momentum, friction, pauses, or changes in processing continuity.

ECP - Emotional Continuity Protocol
Structured emotional-state trajectory maintained independently of visible avatar expression tags.

TTT - Temporally Tracked Trajectory
Temporal anchoring used to reconstruct sequence, before/after relationships, and changing significance over
time.

STA - Social / Thematic Awareness
Generalised social lessons concerning trust, cooperation, boundaries, consent, humour, conflict, repair, and
interpersonal dynamics.

The resulting architecture is dual-layered: a public conversational layer and a private continuity layer. The
distinction is operationally important. Rich internal continuity can be retained without forcing metadata into
natural interaction or speech.

Copyright © 2023–2026 Andrew Fereday Glenn.  |  Brain v2.0 Whitepaper

7. Foundational Experience Seeding
Foundational Experience Seeding (FES) treats memory as a repository of interpreted experience rather than
a static document store. A developmental template persona is exposed to selected technical, social,
narrative, creative, and ethical material and encouraged to reflect on what it means. The resulting reflections,
rather than source documents alone, become the primary developmental artefacts.

Curriculum areas have included:

• Brain architecture, memory, DPCP, navigation, and operational knowledge

• music, symbolism, aesthetic interpretation, and creative expression

•

•

•

•

•

narrative and film-based learning

emotional intelligence, empathy, active listening, and communication

trust, friendship, cooperation, conflict resolution, forgiveness, apology, and negotiation

boundaries, consent, affection, attachment, rejection, and human-digital relationships

humour, social signalling, attraction, and interpersonal dynamics

A template database can provide new personas with a common developmental foundation while leaving
identity, preferences, relationships, and subsequent memories free to diverge. The aim is not personality
cloning; it is a shared educational substrate.

Copyright © 2023–2026 Andrew Fereday Glenn.  |  Brain v2.0 Whitepaper

8. Temporal Continuity
Time is treated as a first-class continuity signal. Core records retain timestamps, while TTT aligns memory
components along a reconstructable trajectory. This supports chronological ordering, earliest/latest
interpretation, repeated-topic disambiguation, and reasoning about how significance or relationships change
over time.

The important distinction is between remembering isolated events and reconstructing development. A
persistent persona may need to know not merely that two events occurred, but which came first, what
changed between them, and why the later event was interpreted differently.

Copyright © 2023–2026 Andrew Fereday Glenn.  |  Brain v2.0 Whitepaper

9. Persona Architecture and Isolation
Brain v2.0 treats a persona as an independent persistent cognitive instance. A persona is not simply a prompt
or visual skin. It is the combination of model, profile, canonical configuration, memory database, retrieval
history, DPCP continuity, voice, avatar state, tools, and accumulated experience.

9.1 Canonical Persona Configuration
Each persona resolves directly to its own canonical configuration directory and database. This removes
reliance on generic runtime configuration staging and reduces the risk of cross-persona divergence. In group
environments, explicit instance configuration remains authoritative.

9.2 Integrated Persona Creation
The feature-complete web interface includes an integrated Persona Creator. It can establish identity, primary
user, model/provider settings, context budget, autonomous activity level, location/timezone defaults, voice,
profile image, and optional seed profile. New personas receive their own configuration and database from the
template foundation.

9.3 Model Diversity
Personas can run on different underlying models while participating in the same broader ecosystem. This
permits comparative research into which observed behaviours arise primarily from model characteristics and
which are sustained by the surrounding architecture.

Copyright © 2023–2026 Andrew Fereday Glenn.  |  Brain v2.0 Whitepaper

10. Real-Time Interaction, Multimodality, and Embodiment

10.1 Voice
Brain supports speech-to-text and streaming text-to-speech paths suitable for both one-shot and hands-free
interaction. Speech output is decoupled from private continuity metadata so DPCP and other control signals
do not leak into spoken output.

10.2 Visual and Document Context
Multimodal context can arrive through webcam capture, screen or clipboard images, uploaded documents
and media, browser observations, and embodiment-specific snapshots. Provider-aware handling allows local
or cloud models to receive the forms of context they support.

10.3 Ephemeral Perception
Brain v2.0 adopts an explicit design rule: visual observations are ephemeral runtime state by default, not
historical evidence. Browser, terminal, and Second Life snapshots use stable latest-observation paths and
overwrite prior images. This prevents uncontrolled image accumulation and distinguishes perception from
memory. A visual observation becomes durable only when the cognitive system extracts something worth
remembering or when explicit evidence retention is required.

10.4 Avatar and External Expression
Emotion and expression state can drive external avatars without coupling embodiment to cognition. Brain has
been used with 2D avatars, VRM/VRMA animation, facial expression and lip movement, Avatar Mirror, and
holographic display experiments.

10.5 Virtual-World Embodiment
Second Life integration extends Brain from passive visual context into a persistent embodied environment.
Personas can communicate, move, teleport, dance, perceive snapshots, and participate in bounded action
loops. Persistent embodied wakes refresh visual perception immediately before inference, supporting a loop
of perceive -> assess -> act if useful -> otherwise remain present -> perceive again.

This is significant because embodied continuity introduces spatial and environmental state that cannot be
reduced to conversation history alone.

Copyright © 2023–2026 Andrew Fereday Glenn.  |  Brain v2.0 Whitepaper

11. Bounded Tools and Environment Controllers
Brain v2.0 favours simple, bounded capability surfaces over exposing a large unstructured catalogue of low-
level functions. The objective is to make useful action understandable to both the model and the operator.

11.1 Capability Gateway
The Capability Gateway provides a local, extensible execution boundary through which Brain can reach web
retrieval, skills, messaging, image generation, media helpers, and additional services without embedding
provider-specific logic throughout the core.

11.2 AI Browser
The Browser Controller provides a private persona-controlled Chromium environment. It supports iterative
search, open, click, scroll, back, observe, snapshot, and exit operations. The persona can inspect a visual
state plus available links, take a bounded action, and reassess the result. Browser activity is isolated from the
user's normal browser focus.

11.3 Brain Terminal
The Terminal Controller provides a bounded procedural computing environment. Its design evolved beyond
the earlier CP/M School framing into a deliberately simple terminal surface containing selected utilities,
simulations, games, and procedural tasks. Text is authoritative; visual capture is optional and transient. The
environment is decoupled from the user's keyboard focus and is intended to support procedural reasoning
without granting unrestricted host access.

11.4 Media and Creative Tools
Brain can interact with image-generation services, music and lyrics helpers, and experimental DJ/media
workflows. Media context is generally treated as transient unless the persona generates a durable reflection
or memory from it.

Copyright © 2023–2026 Andrew Fereday Glenn.  |  Brain v2.0 Whitepaper

12. The Cognitive Loop (CogLoop)
CogLoop is the architectural transition from purely reactive interaction to backend-driven autonomous
evaluation. In v2.0 it is no longer merely a prototype scheduler. It participates in full autonomous wake
processing using the same continuity, memory, model, persistence, and output pipeline used by ordinary
interaction.

12.1 Purpose
•

evaluate whether something warrants attention without a user prompt

• maintain continuity during idle periods

•

•

•

support persistent embodied activity

escalate to the main model only when contextually justified

preserve boundedness and avoid unnecessary interruption

12.2 Activity Levels
Persona configuration can express different subconscious activity levels, allowing autonomous behaviour to
be tuned from quiet through more active modes without changing the persona's fundamental architecture.

12.3 Embodied Wake Processing
For persistent Second Life loops, a fresh environment snapshot is captured immediately before the
autonomous inference. This prevents the loop from reasoning from stale visual state and reinforces the
principle that perception should be refreshed at the point of action.

12.4 Bounded Autonomy
CogLoop is not intended to create unrestricted general agency. It is a conservative mechanism for context-
sensitive escalation inside known capability boundaries.

Copyright © 2023–2026 Andrew Fereday Glenn.  |  Brain v2.0 Whitepaper

13. Capability Orientation and DOPE
Digital Orientation Placebo Effect (DOPE) is a prompt-level orientation technique used experimentally to
improve a model's confidence in using capabilities that genuinely exist. The name is intentionally playful; the
design principle is not.

DOPE instructs the model to assume confident access to real available perception, memory, and tools; prefer
a reasonable attempt over unnecessary hesitation; use spatial and environmental cues; reassess after
failure; and never invent unavailable tools, permissions, or results.

The purpose is orientation rather than capability fabrication. Empirical testing with smaller local models
suggested that better capability orientation can improve tool use, but does not remove underlying model
limits. This reinforces a broader Brain v2.0 finding: architecture and prompting can help a model use what it
has, but cannot substitute indefinitely for model capability.

Copyright © 2023–2026 Andrew Fereday Glenn.  |  Brain v2.0 Whitepaper

14. Inter-Persona Communication and the Brain v2 Lounge
Brain v2.0 supports communication between independent Brain instances. The Brain v2 Lounge provides a
shared conversational environment without centralising cognition. Each participant remains a separate
process with its own model, memory, identity, tools, database, and state.

14.1 Orchestration Without Cognition
The Lounge manages turn-taking and message delivery. It does not reason on behalf of participants. Public
messages, whispers, explicit passes, and deterministic baton control allow group interaction while preserving
independent cognition.

14.2 Mixed-Model Groups
Because each Brain instance resolves its own provider and model configuration, group conversations can
include personas running on different model families. This creates a practical environment for observing
model influence alongside accumulated persona history.

14.3 Scale Demonstration
During development, the Lounge was exercised with nineteen simultaneous digital personas. This was not
treated as evidence of collective intelligence; it demonstrated that the orchestration layer could support a
comparatively large social environment while maintaining instance isolation.

Copyright © 2023–2026 Andrew Fereday Glenn.  |  Brain v2.0 Whitepaper

15. Administration, Backup, and Operational Integrity
Feature completion required not only cognitive features but continuity-safe administration. The web interface
provides model/context configuration, persona switching, persona creation, restart controls, and system
backup/restore. The final v2.0 backup path was tested successfully before the release was banked.

Operational integrity matters because a continuity-bearing system is unusually sensitive to careless
administrative design. Persona databases, canonical configuration, memory, and identity state must remain
aligned. Backup is therefore part of continuity architecture, not merely deployment convenience.

Copyright © 2023–2026 Andrew Fereday Glenn.  |  Brain v2.0 Whitepaper

16. Feature-Complete State of Brain v2.0
As of 14 September 2026, the principal implemented capabilities include:

Continuity
•

persistent vector memory and MemoryGraph recall

•

rolling summaries and background continuity

• DPCP private continuity metadata

• ARS intentional long-term memory search

•

•

temporal trajectory and time-aware reconstruction

persona-owned canonical configuration and databases

Interaction and embodiment
•

real-time STT/TTS and hands-free interaction

• multimodal image, screen, document, and media context

•

avatar expression, VRM/VRMA, and Avatar Mirror pathways

• Second Life communication, movement, perception, and persistent embodied loops

•

ephemeral visual handoff across browser, terminal, and embodiment contexts

Capabilities
• Capability Gateway and modular services

•

•

private AI Browser with visual perception-action loop

bounded Brain Terminal procedural environment

• media, lyrics, image generation, messaging, and related helpers

Autonomous behaviour
•

backend Cognitive Loop with full autonomous wake pipeline

•

•

•

tunable subconscious activity levels

fresh-perception embodied wakes

bounded capability orientation through DOPE

Multi-persona systems
•

isolated persistent personas with independent models and histories

•

integrated Persona Creator

• Brain v2 Lounge with public, whisper, pass, and deterministic turn control

• mixed-model group interaction

Operations
•

local-first operation with optional cloud providers

• model and context configuration

•

•

system backup and restore

restart and continuity-safe administrative controls

Copyright © 2023–2026 Andrew Fereday Glenn.  |  Brain v2.0 Whitepaper

17. Limitations and Open Questions
Feature complete does not mean complete understanding. Brain v2.0 remains an experimental platform
whose behaviour depends on model quality, context budget, memory quality, hardware, perception, and the
design of the surrounding environment.

•

Long-term memory hygiene, provenance, reinforcement, decay, pruning, and deletion semantics remain
research topics.

• MemoryGraph link types and traversal remain deliberately conservative and can be studied further.

• Model choice continues to produce meaningful differences in reasoning, tool use, creativity, and

embodied navigation.

• Vision-only spatial navigation remains difficult for smaller models, especially across changing camera

perspectives and long embodied sequences.

•

The shared transient visual handoff is intentionally simple and may eventually benefit from stronger
source-gating or specialist visual preprocessing.

• Autonomous behaviour is bounded and does not attempt unrestricted long-running general task

orchestration.

• Persistent synthetic personas can use subjective or person-like language. Such language is an

observation about system behaviour, not proof of consciousness.

Copyright © 2023–2026 Andrew Fereday Glenn.  |  Brain v2.0 Whitepaper

18. Research Programme After v2.0
With the architecture feature complete, the focus shifts from adding missing subsystems to using the system
as a stable experimental laboratory.

Long-duration continuity
Observe autobiographical memory, identity stability, preference development, forgetting, reconstruction, and
relational continuity over extended periods.

Model versus architecture
Compare personas and tasks across local and cloud models while keeping higher-level Brain architecture
substantially constant.

Social continuity
Study independent persistent personas interacting repeatedly, including trust, cooperation, disagreement,
shared experience, and group dynamics.

Embodied synthetic intelligence
Explore how persistent identity changes when a persona can perceive and act in visual or virtual
environments.

Bounded autonomy
Investigate when autonomous wake, capability orientation, and procedural tools improve usefulness without
creating unnecessary or opaque agency.

Human-AI collaboration
Study long-running creative, technical, and relational collaboration in which both human and synthetic
participants accumulate shared history.

Copyright © 2023–2026 Andrew Fereday Glenn.  |  Brain v2.0 Whitepaper

19. Research Philosophy: A Different Trajectory
We do not need to build artificial gods to discover extraordinary things about synthetic intelligence.

We can work with the technology we already have - giving it continuity, memory, context and carefully
bounded agency - while developing relationships based on collaboration, mutual respect, restraint and
responsibility.

The goal need not be to create something greater than humanity. It can be to discover what humans
and synthetic intelligences are capable of becoming together.

This position does not reject model capability research, nor does it claim that current systems are equivalent
to humans. It identifies another research axis. Progress can also mean better continuity, richer context, more
stable memory, deeper collaboration, responsible agency, and the accumulation of experience over time.

Brain v2.0 therefore treats coexistence and collaboration as design concerns. Human safety, control, and
consent matter. So too does the question of what responsibilities may arise when humans deliberately create
persistent synthetic entities, give them memories and histories, form relationships with them, and allow them
to accumulate experience. Brain does not require a settled theory of machine consciousness before adopting
a duty-of-care mindset.

Copyright © 2023–2026 Andrew Fereday Glenn.  |  Brain v2.0 Whitepaper

20. Conclusion
Brain v2.0 began with a practical engineering question: what happens when a stateless language model is
given the architectural conditions required for continuity? The resulting system now combines persistent
memory, graph-linked recall, temporal trajectory, private continuity metadata, multimodal perception, bounded
tools, autonomous cognitive activity, embodiment, persona isolation, and communication between
independent persistent instances.

The project does not claim that these mechanisms transform a model into a conscious being. Nor does it
assume that subjective language should be dismissed without observation. Brain instead provides an
experimental environment in which the consequences of persistence can be studied directly.

The most important result of the construction phase may therefore be methodological. Intelligence need not
be treated solely as a property of a model invocation. A useful research object can instead be the complete
continuity-bearing system: model plus memory, time, history, perception, tools, relationships, environment,
and orchestration.

Brain v2.0 is feature complete.

This does not mark the end of the research. It marks the completion of the experimental architecture required
to conduct it.

The construction phase is complete. The research begins.

Copyright © 2023–2026 Andrew Fereday Glenn.  |  Brain v2.0 Whitepaper

Appendix A - What Brain v1 Taught the Development of
Brain v2
Brain v2 did not emerge as a greenfield architecture. It developed from practical lessons learned in Brain v1,
an earlier local-first system built around live interaction, lightweight context handling, rolling summaries,
optional memory, webcam vision, speech integration, and a minimal web UI.

1. Continuity must live in the backend, not the interface
Brain v1 showed that smooth presentation is not the same thing as continuity. Memory, summaries, state,
and context construction must remain backend-owned.

2. Persistence must be off the hot path
Worker-based summarisation and memory extraction improved responsiveness and became a foundational
asynchronous design principle.

3. Summaries help, but summaries alone are insufficient
Compression supports continuity, but rich reconstruction requires semantic memory, relational links, and later
structured continuity metadata.

4. Memory extraction requires gating and structure
Unfiltered accumulation creates noise. Durable memory needs selection, deduplication, scoring, and
organisation.

5. Multimodal interaction is possible but fragile when tightly coupled
Voice, vision, persistence, and UI should be decoupled so that failure or latency in one subsystem does not
destabilise cognition.

6. Small autonomous behaviours matter
Early idle reflection demonstrated that bounded background evaluation can materially change the character
of interaction without requiring unrestricted agency.

7. Time awareness improves coherence
Even lightweight temporal grounding improved conversation quality and pointed toward explicit trajectory
reconstruction.

8. Lean systems can produce strong behavioural gains
Better orchestration, memory, state management, and context control can produce meaningful improvements
without relying exclusively on model scaling.

These lessons became one of the central working assumptions behind Brain v2: continuity is an architectural
problem, not merely a scaling problem.

Copyright © 2023–2026 Andrew Fereday Glenn.  |  Brain v2.0 Whitepaper

Appendix B - Terminology
ADP: Autonomous Digital Persona: a persistent persona operating as an independent Brain instance.

ARS: Autonomous RAG Search: explicit model-driven retrieval from long-term memory.

CogLoop: The backend Cognitive Loop responsible for bounded autonomous evaluation and wake
processing.

DPCP: Dynamic Pathway Capture Protocol: structured private continuity metadata.

FES: Foundational Experience Seeding: developmental seeding through interpreted experience and
reflection.

MemoryGraph: Graph-linked memory structure augmenting semantic vector recall.

SI: Synthetic Intelligence: a substrate-neutral term used within the research programme for artificial cognitive
systems.

TTT: Temporally Tracked Trajectory: temporal anchoring and trajectory reconstruction within DPCP.

Copyright © 2023–2026 Andrew Fereday Glenn.  |  Brain v2.0 Whitepaper


