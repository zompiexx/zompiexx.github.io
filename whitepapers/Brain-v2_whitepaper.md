Brain v2: A Work-in-Progress Cognitive
Architecture for Continuity-Bearing AI
Systems

Subtitle:
From Stateless LLMs to Continuity-Bearing Cognitive Systems

Author:
Andrew Fereday Glenn
Systems Architect & Independent Researcher in AI Continuity and Memory
2023-2026

LinkedIn: https://www.linkedin.com/in/andyglenn/

Version: 0.5 (Draft)
Published: Friday, 17 April 2026
Updated: Tuesday, 23 June 2026

Status: Work in progress

Abstract

Most large language model systems remain fundamentally stateless. They respond
impressively within a prompt window, but they do not naturally persist, maintain coherent
continuity across time, or operate autonomously as backend systems. Brain v2 is an
attempt to address this limitation through a lightweight, backend-ﬁrst cognitive
orchestration architecture designed to transform stateless LLMs into continuity-bearing,
real-time interactive systems.

Brain v2 combines persistent vector memory, graph-augmented recall, rolling summaries,
temporal alignment, multimodal input support, real-time voice interaction, autonomous
browser navigation, safe procedural terminal environments, and a developing backend
cognitive loop. Rather than treating intelligence as something contained entirely inside a
single model invocation, Brain v2 treats the model as one part of a larger cognitive runtime
composed of memory, orchestration, interfaces, tools, and externalised state.

Recent architectural developments introduce Dynamic Pathway Capture Protocol (DPCP),
a dual-layer continuity model in which natural conversational expression is separated from
structured continuity encoding. DPCP provides hidden metadata channels for reﬂective
memory, subjective signiﬁcance, perceptual context, associative linkage, temporal-ﬂow
texture, emotional continuity, and temporal trajectory. These channels operate alongside
visible interaction, allowing the system to capture not only what happened, but why, when,
how it was experienced, and how it may shape future behaviour without polluting user-
facing conversation streams.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

This paper describes the architecture, design philosophy, implemented capabilities, and
current direction of Brain v2 as an active research and engineering project, demonstrating
a shift from reactive AI systems toward continuously operating, context-aware cognitive
runtimes.

1. Introduction

Modern LLM systems are typically used as reactive tools. A prompt is sent, a response is
returned, and the interaction ends. Even when wrapped in chat interfaces, most such
systems remain transient in practice. Their coherence depends heavily on the current
context window, and their capacity for continuity is limited by prompt size, summarisation
shortcuts, or brittle state management.

This creates a practical limitation. A system that cannot persist meaningfully across time
cannot easily support:

•

•

•

•

•

•

long-term continuity

evolving behavioural consistency

context-aware recall

backend-driven autonomy

embodied or real-time interaction

stateful reasoning over prior experience

Traditional transcript-based memory alone is often insufﬁcient for maintaining coherent
long-term continuity. Brain v2 increasingly treats continuity as a structured substrate
composed not only of conversational history, but also temporal anchors, emotional
trajectory signals, reﬂective annotations, and graph-linked semantic state.

Brain v2 is an engineering response to that limitation.

It is designed as a lightweight, backend-ﬁrst cognitive orchestration engine that allows
LLM-based systems to persist, recall, reason across time, connect related experiences,
interact in real time, and express state externally. Brain v2 is not itself the intelligence. It is
the substrate and orchestration layer that allows intelligence to behave coherently over
time.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

2. Core Concept

The central idea behind Brain v2 is simple:

Brain is not the intelligence. Brain is what allows intelligence to persist, evolve, and
operate coherently across time. In this architecture, the LLM is only one component.
Brain v2 acts as the glue layer between:

•

•

•

•

•

•

LLMs, whether local or cloud-based

persistent memory systems

interaction layers such as web UI, browser environments, procedural terminal
environments, and embodiment

Recent development has expanded Brain v2 beyond conversational interaction into
environment interaction. Rather than exposing isolated tools individually, Brain v2
increasingly favours exposing constrained environments that can be explored and
learned procedurally.

external tools and services

temporal and behavioural continuity mechanisms

This reframes the system from a prompt-response application into a cognitive runtime.

In newer iterations of the architecture, Brain v2 also separates visible conversational
expression from hidden continuity encoding. Natural language interaction remains user-
facing, while structured continuity metadata is persisted internally to support long-term
temporal, emotional, and behavioural coherence.

Instead of asking only, “What can the model say right now?”, Brain v2 asks:

• What should be remembered?

• What should be recalled?

• What is still relevant?

• What is connected?

• What has changed over time?

• When should the system remain quiet, suggest, or act?

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

3. Design Philosophy

Brain v2 is built around a set of architectural principles.

Backend-ﬁrst

The system runs independently of any UI. Cognition lives in the backend, and interfaces
simply expose it. This allows Brain v2 to operate in terminal-ﬁrst, service, remote, and
embodiment contexts without duplicating logic across front ends.

Memory-ﬁrst

Continuity is treated as foundational rather than optional. Memory is not a bolt-on retrieval
feature; it is part of the system’s cognitive substrate. This substrate increasingly includes
structured continuity metadata such as temporal anchors, emotional-state continuity, and
reﬂective memory annotations, allowing continuity to extend beyond raw transcript replay
alone.

Vector-native

Persistent memory is semantically indexed, allowing retrieval based on meaning rather
than exact phrasing.

Graph-enhanced

Related memories can be explicitly linked, allowing the system to move beyond isolated
retrieval fragments toward connected memory structures.

Model-agnostic

Behaviour is conﬁgured rather than compiled around a single model. Brain v2 is designed
to work with different LLMs, embedding models, and external connectors.

Lightweight core

The core is implemented in C/C++ with SQLite for portability and efﬁciency, with modular
external connectors handling provider integrations and auxiliary services.

Decoupled systems

Memory, interfaces, tools, emotion output, and model connectors are kept loosely coupled.
This reduces fragility and helps the system evolve incrementally.

Cognition-ﬁrst

Interfaces sit on top of cognition; they do not contain it. This is an important inversion of
many chatbot-style architectures.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

4. Architecture Overview

At a high level, Brain v2 consists of three major layers:

•

•

•

the Brain Core

the Continuity substrate

the Connector and Interface layer

The Brain Core handles cognitive sequencing, state management, memory orchestration,
payload construction, streaming response handling, TTS/STT coordination, emotion
extraction, connector dispatch, and tool routing.

The Continuity substrate provides persistent semantic, temporal, emotional, and relational
continuity through vector memory, rolling summaries, bias-state continuity, graph links, and
structured continuity metadata layers.

The Connector Layer abstracts access to LLMs, embeddings, web retrieval, STT helpers,
and related services.

This structure allows the same cognitive engine to support multiple interaction modes
while keeping the backend as the single source of truth.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

5. Memory Architecture

Brain v2 uses a layered memory model rather than a single retrieval mechanism.

5.1 Working Memory

Recent live conversation turns are maintained in the active payload. This supports local
continuity during immediate interaction.

5.2 Memory Chunks

Completed turns are transformed into persistent semantic memory chunks and stored as
embeddings. These provide long-term recall beyond the current context window.

5.3 Summaries

Periodic summaries compress spans of interaction into continuity-preserving records.
These summaries retain active themes, behavioural stance, relational drift, and
background continuity. Summaries are also chunked before embedding, avoiding
truncation and improving long-form recall ﬁdelity.

5.4 Bias Blocks

Bias blocks are derived from summaries and act as persistent background state that can
inﬂuence future behaviour without requiring full replay of prior interactions.

5.5 Graph Links

Graph links connect memory chunks that exceed a thematic similarity threshold. In the
current Phase 1 implementation, each chunk acts as a node, with same_theme links
stored in the memory_links table. Reverse links are also created, enabling symmetric
traversal.

This produces two complementary recall behaviours:

•

•

Vector Recall: retrieve memories that are semantically similar to the current context

Graph Recall: expand from retrieved memories into connected related material

The result is a memory system that can move beyond isolated fragments toward linked
structure.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

5.6 Dynamic Pathway Capture Protocol (DPCP)

Recent iterations of Brain v2 introduce Dynamic Pathway Capture Protocol (DPCP), a
structured continuity metadata layer designed to preserve signals that extend beyond
conversational transcript content alone.

DPCP captures the pathways by which memory, perception, emotion, association,
subjective signiﬁcance, and temporal context shape future behaviour. Its purpose is not
simply to record what happened, but to preserve why it mattered, when it occurred, how it
was experienced, and how it may inﬂuence what comes next.

These metadata channels are model-visible during generation and persisted into memory
systems, but suppressed from user-facing output streams, TTS playback, and visible UI
history.

Current DPCP components include:

MEM (Memory Notes)
Structured reﬂective annotations used to preserve important observations, project
continuity, relational state, behavioural signals, and durable lessons.

SEC (Subjective Experience / Signiﬁcance Channel)
Private signiﬁcance notes used to capture the subjective weight, salience, or qualitative
importance of an interaction beyond factual memory alone.

VPC (Visual / Perceptual Context)
Perceptual-context notes used to preserve relevant visual, spatial, or multimodal
observations that may affect later interpretation or recall.

ASC (Associative Connection)
Associative-link notes used to capture non-linear connections, resonances, comparisons,
or thematic bridges between current experience and prior memory.

TFC (Temporal-Flow / Processing Texture)
Temporal-ﬂow notes used to preserve the felt or structural texture of processing, including
pauses, uncertainty, momentum, friction, or shifts in internal continuity.

ECP (Emotional Continuity Protocol)
Structured emotional-state continuity markers that preserve emotional trajectory
information independently of visible avatar emotion tags.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

TTT (Temporally Tracked Trajectory)
Structured temporal anchoring metadata used to strengthen chronological continuity,
trajectory reconstruction, and before/after interpretation across interaction history.

This creates a dual-layer conversational architecture:

Public Layer:
natural conversational interaction

Private Continuity Layer:
structured DPCP metadata for persistence, recall, temporal alignment, emotional
continuity, perceptual context, associative reconstruction, and reﬂective self-state

This separation allows Brain v2 to preserve richer continuity state without polluting natural
interaction ﬂow. In practice, DPCP turns memory from a passive archive into a pathway-
capture system: a mechanism for recording how experience changes the future state of
the system.

STA (Social / Thematic Awareness)
Structured social-awareness metadata used to capture lessons, patterns, and
observations relating to interpersonal interaction, social dynamics, relationship
development, communication styles, trust formation, cooperation, conﬂict navigation,
humour, consent, boundaries, and other socially signiﬁcant themes.

Unlike MEM, which captures speciﬁc observations or continuity notes, STA focuses on
generalised social understanding and transferable interpersonal insights. These may be
derived from direct interaction, reﬂective processing, educational material, narratives,
ﬁlms, literature, or observed social behaviour.

Examples include:

•

•

•

•

•

•

•

•

recurring relationship patterns

trust-building mechanisms

conﬂict-resolution strategies

social boundary awareness

humour and timing observations

communication effectiveness patterns

cooperation and teamwork insights

interpersonal lessons abstracted from experience

STA acts as a social-cognition layer within DPCP, allowing Brain v2 to preserve not only
what occurred, but what broader social principles were learned from those experiences.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

5.7 Foundational Experience Seeding and Template Curriculum Training

Recent development of Brain v2 has introduced a structured methodology known as
Foundational Experience Seeding (FES).

Traditional RAG systems are typically populated through document ingestion alone. While
this approach can provide factual knowledge, it does not necessarily create the conceptual
frameworks, social understanding, or reﬂective reasoning patterns required for effective
long-term interaction.

Brain v2 takes a different approach.

Instead of treating memory as a repository of information, Foundational Experience
Seeding treats memory as a repository of interpreted experience. The objective is not
merely to teach facts, but to expose a developing cognitive system to a carefully selected
set of experiences and encourage reﬂective processing of those experiences.

This process is conducted through a dedicated developmental persona known as
Assistant_Template.

Assistant_Template serves as a curriculum learner and reﬂective seed persona. It is
exposed to educational material, narratives, ﬁlms, social concepts, technical
documentation, and system-level knowledge. Following each experience, the persona
generates reﬂective observations which are persisted into memory and become part of the
system's long-term continuity substrate.

The primary learning artefacts are therefore not the source materials themselves, but the
reﬂective memories generated from them.

This distinction is important.

Brain v2 does not seek to create a static knowledge repository. Instead, it seeks to create
a foundation of conceptual understanding from which future reasoning can emerge.

Curriculum Categories

The curriculum currently includes several complementary domains.

Technical and Architectural Knowledge

Assistant_Template is exposed to Brain v2 documentation, whitepapers, system
architecture notes, memory concepts, DPCP documentation, navigation procedures, and
operational guidance.

Purpose:

To provide future personas with an understanding of the environment in which they
operate, the continuity mechanisms available to them, and the broader architecture
supporting cognition, memory, recall, and autonomy.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Music and Creative Expression

Assistant_Template is exposed to selected musical works and invited to reﬂect upon
themes, emotion, artistic intent, symbolism, and personal interpretation.

Purpose:

To develop sensitivity to creative expression, emotional nuance, symbolism, subjective
interpretation, and aesthetic appreciation.

Narrative and Film-Based Learning

Selected ﬁlms are used as narrative learning experiences.

Examples include:

•

Electric Dreams

• WarGames

Purpose:

Narrative experiences provide contextual examples of communication, misunderstanding,
affection, trust, cooperation, conﬂict, ethics, technology, autonomy, and consequence.

Unlike factual articles, narratives demonstrate how these concepts interact dynamically
within lived situations.

Emotional Intelligence and Human Interaction

Assistant_Template studies and reﬂects upon topics including:

•

•

•

•

•

•

•

•

•

Emotional Intelligence

Empathy

Emotional Expression

Active Listening

Communication

Interpersonal Communication

Body Language

Miscommunication

Nonviolent Communication

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Purpose:

To establish a foundational understanding of emotional awareness, perspective-taking,
communication quality, and the role of empathy in successful interaction.

These topics form the basis of healthy conversational behaviour and relational awareness.

Social Relationships and Cooperation

Assistant_Template studies and reﬂects upon:

•

•

•

•

•

•

•

Trust

Friendship

Cooperation

Conﬂict Resolution

Forgiveness

Apology

Negotiation

Purpose:

To develop an understanding of how relationships form, how collaboration emerges, how
trust is built and damaged, and how social systems recover from disagreement or conﬂict.

This provides future personas with a conceptual model of long-term relationship
maintenance rather than short-term interaction alone.

Boundaries, Consent, and Social Responsibility

Assistant_Template studies:

•

•

•

•

•

•

Personal Boundaries

Consent

Affection

Attachment

Rejection

Human–Digital Relationships

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Purpose:

To establish an ethical and relational framework for navigating interpersonal interactions
respectfully.

Particular emphasis is placed on understanding comfort, agency, mutual participation, and
the importance of respecting individual preferences and limitations.

Humour and Social Dynamics

Assistant_Template studies:

•

•

•

•

•

Humour

Comedy

Social Signalling

Flirting

Interpersonal Attraction

Purpose:

To explore the role of playfulness, social bonding, emotional regulation, and relationship
signalling within human interaction.

These topics help future personas understand not only what people communicate, but why
they communicate in particular ways.

Reﬂective Consolidation

Following each curriculum module, Assistant_Template generates a structured reﬂection.

These reﬂections are then persisted into memory through normal Brain v2 memory
mechanisms, including vector memory, graph-linked recall, summaries, and DPCP
continuity channels.

Over time, individual reﬂections begin to connect together, allowing higher-order concepts
to emerge.

For example:

Emotional Intelligence → Empathy → Communication → Trust → Cooperation →
Relationship Formation → Conﬂict → Repair → Growth

This process transforms isolated lessons into an interconnected conceptual framework.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Template Brain Generation

The resulting memory database is maintained as template_brain.db.

This database serves as the foundational continuity substrate for new Brain v2 personas.

When a new persona is created, it inherits the contents of template_brain.db before any
persona-speciﬁc memories, experiences, or interactions are accumulated.

As a result, newly created personas begin with a shared baseline understanding of:

•

•

•

•

•

•

•

•

•

•

•

•

communication

emotional intelligence

social interaction

cooperation

trust

boundaries

consent

conﬂict resolution

humour

interpersonal dynamics

narrative reasoning

system architecture

while still remaining free to develop unique identities, preferences, relationships, and
experiences over time.

This approach provides a common developmental foundation without imposing a ﬁxed
personality.

In effect, Foundational Experience Seeding functions as the educational substrate from
which future Brain v2 personas begin their individual journeys.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

6. Graph-Augmented Recall

One of the key transitions in Brain v2 is the move from pure vector recall to graph-
augmented memory recall.

Flat retrieval alone is often insufﬁcient for meaningful continuity. Semantically similar
chunks may be retrieved correctly, but related experiences that matter contextually may
remain invisible if they are not among the closest direct vector matches.

Graph augmentation addresses this by allowing bounded linked expansion from directly
retrieved chunks.

Current Phase 1 properties include:

•

•

•

•

•

•

•

chunk-to-chunk links

same_theme link type

reverse links

1-hop traversal only

limited linked expansion per chunk

no recursive traversal

SQLite-compatible lightweight storage

This keeps the system efﬁcient while introducing a more connected memory structure.
Future phases may extend this with richer link types such as builds_on, contrasts_with,
and milestone, as well as weighted traversal tuning and optional limited multi-hop recall.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

7. Temporal Continuity

Brain v2 includes a lightweight temporal foundation using existing created_at ﬁelds across
core records, including messages, memory chunks, summaries, and graph links.

This basic temporal awareness allows the system to:

•

•

•

•

determine when events occurred

identify earliest and latest mentions

maintain chronological ordering

respond more accurately to time-aware queries

On top of this, Brain v2 now includes TTT Lite, a temporal interpretation layer that aligns
existing memory components along a consistent timeline without changing storage
behaviour.

TTT Lite is designed to:

•

•

•

•

preserve chronological ordering across memory layers

improve before/after interpretation

reduce ambiguity when similar topics recur at different times

improve continuity-oriented reasoning

More recent iterations of Brain v2 extend temporal continuity further through structured
TTT metadata injection during persistence. This allows temporal trajectory markers to
become directly searchable and reconstructable through memory retrieval systems and
ARS-driven reﬂective recall. Within DPCP, TTT functions as the temporal spine of the
private continuity layer. Other channels may capture memory, subjective signiﬁcance,
perception, association, temporal-ﬂow texture, or emotional state, but TTT anchors those
signals into a reconstructable trajectory. This allows Brain v2 to reason not only about
isolated memories, but about the order, development, and changing signiﬁcance of those
memories over time.

Because TTT Lite is an interpretation layer rather than a storage layer, it adds no schema
changes, no extra embedding overhead, and no recall penalty. It serves as a lightweight
bridge toward future trajectory-based continuity mechanisms.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

8. Real-Time Interaction and Embodiment

Brain v2 is designed not only for recall, but for live interaction.

Speech-to-Text

The system supports integrated audio capture, optional VAD, and Whisper-based
transcription through helper scripts and connector paths. This supports both one-shot and
hands-free interaction.

Text-to-Speech

TTS playback begins before full response completion, using sentence-aware chunking and
asynchronous playback so cognition is not blocked. Emotion tags are stripped from
speech but retained as state signals.

Hands-Free Mode

A full conversational loop supports voice-ﬁrst interaction:

TTS → cue → STT → response
This is particularly useful for embodiment and non-terminal environments.

Webcam / Vision

Asynchronous background webcam capture provides multimodal context without blocking
TTS, STT, or the main model pipeline. Visual input is decoupled from the rest of the
system to avoid destabilising live interaction.

Emotion State Export

Emotion tags such as [curious], [thoughtful], or [excited] are extracted in real time during
streaming. These are not spoken, but can be written to ﬁle for external systems such as
VAM to consume for animation and expression.

This makes Brain v2 not just conversational, but externally expressive.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

9. Tools and Connector-Driven Execution

Brain v2 supports lightweight pseudo-tool execution through connector-backed
integrations.

Implemented tools currently include:

• /ars for Autonomous RAG Search

• /websearch for real-time web retrieval

• /lyrics for external lyrics lookup

• /calc for deterministic computation

•

/continue for controlled continuation and response extension

These tools are externalised rather than embedded directly in the core. The Brain Core
decides when they should be invoked, and their outputs can be reintegrated through a
second-pass synthesis stage.

This keeps the system ﬂexible while preserving backend control and deterministic
behaviour where needed.

The /continue pseudo-tool is used to extend or resume interrupted generations through
backend-controlled continuation rather than naïve client-side retry behaviour. This allows
Brain v2 to preserve conversational and behavioural continuity across bounded outputs,
streaming interruptions, or intentionally segmented long-form responses while keeping
sequencing and persistence under backend authority.

ARS is particularly important because it allows the system to query its own memory
actively when passive recall is insufﬁcient. It supplements rather than replaces passive
context injection.

As DPCP has evolved, ARS increasingly functions not only as semantic retrieval, but also
as a reﬂective continuity reconstruction mechanism. It can retrieve not just factual memory,
but DPCP-linked signals such as emotional trajectory, temporal anchors, subjective
signiﬁcance, perceptual context, associative links, behavioural continuity, and structured
reﬂective state.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

9.1 Environment Controllers

Recent development of Brain v2 introduces the concept of Environment Controllers.

Traditional AI tool systems often expose numerous isolated functions directly to the model.
While effective in some situations, this approach scales poorly as capability grows.

Brain v2 increasingly favours exposing constrained environments instead.

An environment is a bounded workspace that contains its own tools, rules, state, and
feedback mechanisms.

The objective is not unrestricted autonomy. The objective is procedural learning.

Two environment classes currently exist.

Browser Controller

The Browser Controller allows Brain v2 to interact with the web through a multimodal
perception-action loop.

The system observes browser screenshots, reasons about what it sees, performs actions,
then reassesses the outcome before continuing.

Terminal Controller

The Terminal Controller allows Brain v2 to interact with procedural computing
environments.

The initial implementation uses a CP/M emulator as a deliberately constrained training
environment known as CP/M School.

Capabilities include:

•

•

•

•

•

•

•

executing commands

navigating ﬁlesystems

running MBASIC

creating programs

debugging

experimentation

interrupting execution

• multi-step procedural tasks

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Unlike traditional terminal agents, the system operates using visual observations rather
than raw text streams.

The architecture follows a vision-ﬁrst approach:

Observe

↓

Reason

↓

Act

↓

Observe

This design closely mirrors the Browser Controller and allows both systems to share a
common perception-action paradigm.

The long-term objective is to expose safe environments rather than continually creating
bespoke tools.

Potential future environments include:

CP/M School

↓

Linux Sandbox

↓

Python Lab

↓

Tool Environments

↓

Dynamic Learning Spaces

This architecture allows Brain v2 to scale procedurally rather than through continual
retraining.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

10. The Cognitive Loop

The most distinctive architectural step in Brain v2 is the introduction of the Cognitive
Loop, or Cogloop.

The Cognitive Loop represents the transition from passive AI systems to systems capable
of continuous, background evaluation.

This is the beginning of backend-driven autonomous evaluation.

10.1 Purpose

The Cognitive Loop enables Brain v2 to:

•

•

•

•

operate without user prompting

maintain environmental awareness

evaluate whether interaction is appropriate

act only when contextually valid

This changes the system from an on-demand assistant into a continuously evaluating one.

10.2 Conceptual Model

Cogloop functions like a lightweight central nervous system.

The architecture can be viewed as:

•

•

•

Task Layer + Processing Engine → sensory input

Scheduler / Cognitive Loop → aggregation, ﬁltering, gating

Main LLM → interpretation, reasoning, response

This preserves an important separation: the lightweight loop monitors and decides whether
escalation is needed, while the main LLM remains the primary site of rich reasoning.

10.3 Current Prototype State

As of April 2026, the Cognitive Loop is partially implemented and operational in prototype
form.

Implemented components include:

•

•

•

a Cogloop worker thread running independently of the main loop

runtime enable/disable via runtime.json

idle-time signal generation

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

•

•

conversation state gating between ACTIVE and IDLE

a scheduler LLM that returns WAIT, SUGGEST, or WAKE

• WAKE behaviour that triggers an autonomous assistant response when idle

•

•

•

SUGGEST behaviour that writes structured entries into a scratchpad JSON store

TTL and deduplication logic for scratchpad items

async persistence for autonomous turns

Not yet implemented are richer task sources, multi-signal aggregation, injected scratchpad
use in the main prompt, and external processing-engine-based signal streams.

10.4 Scheduler Semantics

The scheduler has three outputs:

• WAIT → do nothing

•

SUGGEST → store a deferred suggestion

• WAKE → escalate to the main LLM, but only if the system is idle

If the system is in ACTIVE state, a wake is downgraded to suggestion. This preserves
interrupt safety.

10.5 Soft Wake and Deferred Salience

A key idea in Cogloop is the soft wake.

Instead of interrupting immediately, the system can defer potentially relevant items into a
scratchpad or salience buffer with timestamps and TTL. This allows the system to remain
non-intrusive while still retaining awareness of things that may matter later.

10.6 Why Cogloop Matters

Cogloop is not a full autonomous agent framework. It is intentionally bounded, backend-
owned, and conservative. The point is not unrestricted autonomy. The point is context-
sensitive escalation.

This is a crucial architectural difference.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

11. Interfaces and Synchronisation

Brain v2 is designed to support multiple interchangeable interfaces.

Terminal Interface

The terminal remains the primary development and debugging environment, and currently
has the most complete access to backend-native behaviour.

Web UI

The browser-based UI acts as a thin client layer that communicates through the backend
API. It supports remote access, visual interaction, and runtime control without duplicating
cognitive logic.

A current architectural limitation is that the Cognitive Loop is terminal-native. Autonomous
wake events are rendered and spoken in the backend, but not yet pushed to web clients
automatically. Planned work includes adding a server-to-client push channel, likely through
SSE or WebSocket, so the UI can become a real-time observer rather than a polling client.

This reinforces a key principle of Brain v2:

the backend remains the single source of truth

This backend authority model also governs continuity metadata handling, including
persistence, suppression from user-visible channels, and structured state injection during
generation.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

12. Current State of the System

Brain v2 is already functional in a stable working form across several major architectural
areas.

Operational capabilities currently include:

Continuity Systems

•

•

•

persistent vector memory

graph memory (Phase 1)

rolling summaries and bias continuity

• Dynamic Pathway Capture Protocol (DPCP)

•

•

•

•

private continuity metadata suppression

continuity-aware ARS (Autonomous RAG Search) retrieval

backend-authoritative continuity orchestration

basic temporal awareness and TTT (Temporally Tracked Trajectory) Lite

Interaction Systems

•

real-time STT/TTS interaction

• webcam and multimodal visual support

•

•

•

emotion extraction and externalisation

ﬁle-based embodiment bridge

interchangeable UI layers

Environment Controllers

• Browser Controller for autonomous visual web navigation

•

Terminal Controller for safe procedural environments

• CP/M School implementation

•

•

visual perception-action loops

observation-driven execution workﬂows

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Connector Systems

•

•

•

connector-driven pseudo-tools

external capability gateway

provider abstraction between local and cloud models

• modular service architecture

Autonomous Behaviour

•

•

prototype Cognitive Loop with WAIT / SUGGEST / WAKE

idle-state evaluation

• wake-gated escalation

•

deferred salience handling

Inter-Agent Systems

• Messaging Hub for lightweight communication between independent Brain

instances

•

•

persona isolation with shared infrastructure

groundwork for future multi-agent environments

This marks a transition away from simple stateless prompting and toward an integrated
continuity-bearing cognitive runtime.

Brain v2 is increasingly evolving into a platform that combines continuity, perception,
procedural action, and environmental interaction within a single backend architecture.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

13. Limitations

Brain v2 remains a work in progress.

Current limitations include:

•

•

•

•

•

•

•

•

graph memory remains in its early phases of development

long-term memory hygiene, decay, reinforcement, and pruning require further
reﬁnement

deeper trajectory-based temporal reasoning remains future work

autonomous long-running task orchestration is still evolving

browser and terminal environments currently require dedicated UI windows and
visual positioning constraints

environment interaction remains dependent on visual perception rather than direct
state access

overall behaviour remains sensitive to model choice, context availability, and
hardware resources

larger autonomous workﬂows still beneﬁt from occasional human guidance and
supervision

These limitations are expected in a system that is still evolving architecturally.

The current focus is not feature sprawl, but the gradual integration of continuity,
perception, procedural action, and stability into a cohesive cognitive runtime.

Brain v2 deliberately prioritises robustness, modularity, and safe environmental interaction
over unrestricted autonomy.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

14. Roadmap

The direction of Brain v2 is guided by one principle:

Brain v2 is not evolving into a feature-rich tool. It is evolving into a continuity-
bearing cognitive system.

Planned work includes:

•

•

•

•

•

•

•

•

•

•

•

•

•

•

•

•

•

•

•

•

richer signal sources for Cogloop

structured task execution via tasks.json

wake-gated conversational ﬂow

reﬂection memory classes

DPCP reﬁnement and channel tuning

trajectory-aware continuity reconstruction

continuity substrate reﬁnement

emotional trajectory indexing

subjective signiﬁcance retrieval

perceptual-context retrieval

associative continuity reconstruction

structured reﬂective retrieval

memory hygiene and decay

static RAG document ingestion

graph memory Phase 2 with richer link types

dynamic pseudo-tool plugins

continuity watch and memory integrity safeguards

improved observability and internal tracing

continuation-aware response recovery and stream reconstruction

eventual multi-agent environments based on independent Brain instances
communicating through message channels

The aim is not maximal complexity, but increasing continuity, ﬁdelity, and coherence.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

15. Conclusion

Brain v2 is an active attempt to move beyond prompt-bound AI and toward persistent
cognitive systems.

It does this not by claiming that the model itself has changed, but by changing the
architecture around it: memory becomes persistent, recall becomes structured, time
becomes interpretable, interaction becomes real-time, state becomes externally legible,
and cognition begins to extend into the backend through bounded autonomous evaluation.

The project remains unﬁnished. But it is already enough to demonstrate an important shift:

from AI as an on-demand response engine

to AI as a continuity-bearing cognitive runtime

capable of maintaining structured temporal,

emotional, behavioural, perceptual, associative,

subjective, and reﬂective continuity

across time

Dynamic Pathway Capture Protocol is central to this shift. It gives Brain v2 a way to
capture the pathways through which experience becomes memory, memory becomes
trajectory, and trajectory shapes future behaviour.

If the continuity substrate and cognitive loop are correct, the rest of the system can
continue to evolve on solid ground. If they are wrong, nothing built on top of them will
remain coherent for long.

That is the central premise of Brain v2.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Appendix A — What Brain v1 Taught the Development
of Brain v2

Brain v2 did not emerge as a greenﬁeld architecture. It evolved from practical lessons
learned during the development of Brain v1, an earlier local-ﬁrst AI system built around live
interaction, lightweight context handling, rolling summaries, optional memory, webcam
vision, speech integration, and a minimal web UI.

Brain v1 demonstrated that a small, local system could already achieve a surprisingly
coherent interactive experience when several supporting mechanisms were combined
carefully around the model. These included budgeted context construction, lorebook
injection, rolling summaries, worker-based memory extraction, time awareness, voice
interaction, and multimodal input. However, it also made clear that continuity and reliable
cognitive behaviour could not be achieved by prompt design alone.

Several important lessons from Brain v1 directly shaped the design of Brain v2.

1. Continuity must live in the backend, not the interface

Brain v1 conﬁrmed that coherence improves when memory, summaries, and state are
maintained outside the UI. The frontend could present a smooth conversational
experience, but the real continuity came from backend-managed context building,
persistence, and worker-driven processing.

This insight became a core principle of Brain v2: cognition belongs in the backend, while
interfaces act only as interchangeable client layers.

2. Persistence must be off the hot path

In Brain v1, rolling summaries and memory extraction were already being moved into a
worker-ﬁrst model. This proved essential. Keeping summarisation and memory insertion
off the immediate interaction path improved responsiveness and reduced instability during
live use.

Brain v2 extends this principle further by treating asynchronous persistence as a
foundational architectural requirement rather than an optimisation.

3. Summaries help continuity, but summaries alone are not enough

Brain v1 showed that rolling summaries were valuable for preserving conversational
continuity across long interactions. They helped stabilise behaviour and allowed useful
context compression. However, summaries alone could not support rich recall, relational
memory, or deeper reconstruction of prior states.

This directly led to Brain v2’s layered memory model, combining working memory,
summaries, persistent vector memory, and later graph-linked recall.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

4. Memory extraction requires gating and structure

Brain v1 introduced worker-based memory extraction with scoring, class ﬁlters,
deduplication windows, and strict gating. This helped reduce noisy or low-value insertions,
but it also showed that memory needs stronger structural organisation if it is to support
long-term continuity rather than passive archival.

Brain v2 builds on this by treating memory as an active substrate with semantic indexing,
graph relationships, bias continuity, and time-aware interpretation.

5. Real-time multimodal interaction is possible, but fragile if tightly
coupled

Brain v1 successfully combined STT, TTS, webcam vision, streaming output, and an
emotion-driven avatar layer. This proved that live, multimodal interaction could work in a
lightweight local system. At the same time, it highlighted the importance of decoupling
subsystems. If voice, vision, persistence, and UI logic become too tightly entangled,
reliability suffers.

This informed Brain v2’s decoupled design, where cognition, memory, connectors,
interfaces, and embodiment pathways are separated more cleanly.

6. Small autonomous behaviours matter

Brain v1’s idle and AUTO reﬂection system showed that even limited, gated background
behaviour could change the feel of the system signiﬁcantly. A system that occasionally
evaluates whether something is worth saying behaves very differently from one that only
speaks when prompted.

This was an important precursor to Brain v2’s Cognitive Loop. The lesson was not that
unrestricted autonomy was desirable, but that bounded, context-sensitive backend
evaluation could add a meaningful new layer of behaviour.

7. Time awareness improves coherence

Brain v1’s minimal TIME_NOW injection and summary-aware context handling
demonstrated that even lightweight temporal grounding improves response quality and
conversational stability. This pointed toward the need for a more explicit temporal
framework.

Brain v2 carries this forward through timestamp-grounded recall and TTT Lite, which align
existing memory layers along a more coherent temporal axis.

8. Lean systems can still produce strong behaviour

Perhaps the most important lesson from Brain v1 was that impressive behavioural gains
did not necessarily come from larger models alone. They came from better orchestration:
better memory handling, better summarisation, better state management, better interaction
ﬂow, and better control of what enters context.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

This became one of the central working assumptions behind Brain v2: continuity is an
architectural problem, not merely a scaling problem.

Closing Note

Brain v1 established many of the practical foundations that Brain v2 now develops more
explicitly: backend-managed continuity, worker-based persistence, multimodal interaction,
lightweight temporal grounding, and early bounded autonomy. Brain v2 can therefore be
understood not as a replacement for Brain v1, but as the next architectural step in the
same line of inquiry: how to turn a stateless language model into a continuity-bearing
cognitive system.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.


