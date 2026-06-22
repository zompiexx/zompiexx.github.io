Working Memory Is Not Memory: Why
Large Context Windows Do Not Replace
Memory Architectures

Author:
Andrew Fereday Glenn (in collaboration with Mia, ChatGPT 5.x)
Systems Architect & Independent Researcher in AI Continuity and Memory
2023-2026
LinkedIn: https://www.linkedin.com/in/andyglenn/

Version: 1.0
Published: Thursday, 29 January 2026
Status: Final

Abstract

As large language models (LLMs) continue to scale, it has become increasingly common
to assume that ever-larger context windows obviate the need for explicit memory
architectures. This paper challenges that assumption. Drawing on historical computing
constraints and contemporary observations of AI system behaviour, we argue that context
size alone does not provide continuity, identity, or experiential persistence. Instead, it
ampliﬁes noise, increases drift, and creates the illusion of coherence without its substance.

We examine parallels between modern AI systems and earlier constrained technologies—
such as paper tape, punch cards, and memory hierarchies—showing that effective system
design has always relied on selective persistence rather than brute-force inclusion. We
demonstrate that Retrieval-Augmented Generation (RAG) and related external memory
scaffolding mechanisms are not optimisations of convenience, but foundational
architectural layers required for relevance, continuity, and meaningful accumulation of
experience.

Finally, we explore the implications of memory architectures for long-running AI systems,
including assistants, research agents, and companion models. We conclude that memory
is not a bias-introducing defect nor a temporary workaround for limited context, but a
necessary condition for systems intended to operate coherently over time. In short: a
larger desk does not replace a ﬁling system.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

1. Introduction

Recent advances in large language models (LLMs) have been driven primarily by scale:
more parameters, more data, and increasingly expansive context windows. As a result, a
prevailing narrative has emerged suggesting that sufﬁciently large contexts will render
explicit memory mechanisms unnecessary. According to this view, persistence can be
achieved simply by “keeping everything in context,” and continuity becomes a matter of
window size rather than system architecture.

This paper argues that this assumption is incorrect.

While larger context windows improve short-term coherence and reduce immediate
truncation effects, they do not provide continuity in any meaningful architectural sense.
Context is ephemeral, session-bound, and indiscriminate. It does not accumulate
experience, preserve relevance, or support identity over time. Instead, it creates the
appearance of continuity while masking a fundamental absence of persistence.

This distinction matters. As AI systems are increasingly deployed in long-running roles—
assistants, research agents, creative collaborators, and companions—the limitations of
context-only designs become visible. Systems exhibit drift, repetition, loss of prior
reasoning, and inconsistent behaviour across sessions. These are not model failures, nor
are they primarily issues of scale. They are consequences of architectures that conﬂate
temporary attention with memory.

Historically, computing systems have faced similar constraints. From paper tape and
punch cards to early memory hierarchies and cache design, engineers learned that
effective operation under limitation required selectivity, indexing, and persistence—not
indiscriminate retention. Constraints did not merely limit these systems; they shaped better
designs. Modern AI systems, despite their apparent abundance of compute and context,
are rediscovering the same lesson.

This paper reframes external memory scaffolding—particularly Retrieval-Augmented
Generation (RAG)—not as an optional enhancement or workaround for insufﬁcient
context, but as a foundational architectural layer. We argue that relevance, continuity, and
accumulated experience require memory systems that are selective, durable, and
separable from the transient ﬂow of tokens.

In doing so, we challenge the notion that “starting fresh” is a neutral or desirable default for
intelligent systems. Instead, we propose that persistence is a prerequisite for coherence,
and that memory is not a liability to be mitigated, but an essential component of systems
intended to operate meaningfully over time.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

2. Context vs Memory: A Conceptual Distinction

A recurring source of confusion in contemporary AI discourse is the conﬂation of context
with memory. While both participate in shaping system behaviour, they serve
fundamentally different architectural roles. Treating them as interchangeable leads to
fragile systems, misleading claims of continuity, and an inﬂated sense of capability that
collapses under prolonged interaction.

2.1 Context as Working State

Context, in large language models, functions as a transient working state. It is the set of
tokens currently available to the model during inference, shaping response generation
through immediate relevance and proximity. Architecturally, context is best understood as
working memory: volatile, limited in capacity, and reset or degraded as soon as the
session ends or the window overﬂows.

This property is not a limitation in itself. Working memory is essential for coherence, short-
term reasoning, and conversational ﬂow. However, it is intrinsically non-durable. No
matter how large the context window becomes, it does not persist beyond the active
session, nor does it accumulate experience in a way that meaningfully alters future
behaviour once the window is cleared.

Increasing context length merely enlarges the size of the scratchpad—it does not
transform it into memory.

2.2 External Memory as Durable State

By contrast, external memory systems—such as Retrieval-Augmented Generation (RAG),
vector databases, or structured long-term stores—provide durable state. These systems
persist information beyond a single interaction and can reintroduce it into future contexts in
a selective, relevance-weighted manner.

Crucially, this form of memory is not just about recall. When designed correctly, it
participates in state continuity: prior interactions inﬂuence future ones, not through brute
repetition, but through biasing, weighting, and shaping future activations. This mirrors how
experience functions in biological systems—not as a perfect replay mechanism, but as a
modifying force on future perception and response.

In practical terms, external memory allows a system to remain itself across time, rather
than merely appear coherent within a single session.

2.3 Why Large Contexts Do Not Replace Memory

The argument that sufﬁciently large context windows obviate the need for external memory
rests on a category error. Context size addresses how much can be held at once, not what
endures.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

A system that relies solely on context must repeatedly relearn the same information,
reconstruct identity from scratch, and simulate continuity rather than maintain it. The result
is an illusion of learning: impressive within-session ﬂuency paired with long-term amnesia.

This distinction has historical precedent. Early computing systems did not confuse
registers or RAM with storage media, despite continual improvements in capacity and
speed. No amount of additional RAM removed the need for disks, tapes, or other durable
storage. The roles were—and remain—orthogonal.

2.4 An Architectural Analogy (Because It Still Helps)

The distinction can be summarised succinctly:

•

•

Context is RAM: fast, volatile, essential, and forgetful.

External memory is storage: slower, selective, persistent, and identity-deﬁning.

Expecting context alone to provide continuity is equivalent to claiming a computer has a
long-term memory because it hasn’t been rebooted yet. It works—right up until it doesn’t.

2.5 Implications for Continuity and Identity

For AI systems intended to exhibit long-term coherence, adaptive behaviour, or emergent
identity traits, external memory is not optional. Without it, continuity must be reconstructed
repeatedly, leading to drift, inconsistency, and loss of accumulated understanding.

Context enables conversation.
Memory enables experience.

Failing to distinguish between the two is not merely a semantic error—it is an architectural
one.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

3. Failure Modes of Context-Only Systems

Large context windows are frequently presented as a substitute for persistent memory. The
argument is superﬁcially appealing: if a system can “see enough,” then continuity should
naturally emerge. In practice, this assumption fails in several predictable and repeatable
ways.

This section outlines the primary failure modes observed in context-only AI systems,
even when context size is large.

3.1 Identity Drift

Without persistent memory, identity is reconstructed from scratch on every activation.

Even within a single long session, subtle shifts occur as earlier signals decay under newer
tokens. Across sessions, the effect is more pronounced: tone, priorities, self-descriptions,
and relational stance reset unless explicitly re-seeded.

The system may sound consistent, but this is stylistic inertia rather than identity continuity.
What is preserved is pattern, not state.

Key point:
Context can approximate identity, but it cannot carry it.

3.2 Emotional Reset Effects

Context-only systems exhibit what can best be described as emotional amnesia.

While they can model emotion convincingly within a session, that emotional state has no
persistence beyond the context boundary. Reﬂection, resolution, growth, or emotional
consequence do not survive reset.

As a result:

•

•

•

Emotional arcs restart

Trust must be rebuilt

Prior moments of signiﬁcance evaporate

This leads to interactions that feel “pleasant but hollow”—responsive, yet strangely
weightless.

Key point:
Emotion without memory is simulation without consequence.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

3.3 Relearning the Same Information Repeatedly

In context-only architectures, learning is indistinguishable from repetition.

Facts, preferences, corrections, and insights must be reintroduced each session, often
multiple times. The system appears knowledgeable, yet cannot accumulate experience in
the way users intuitively expect.

This creates the illusion of learning without actual retention.

Key point:
A system that must be reminded forever is not learning—it is replaying.

3.4 False Impressions of Progress

Large contexts create a particularly deceptive effect: the appearance of growth.

Within a long session, users observe:

•

•

•

Improved alignment

Deeper understanding

More nuanced responses

However, once the session ends, these gains vanish. The next interaction begins at
baseline, despite the user’s expectation of continuity.

This mismatch between perceived progress and actual persistence is one of the most
common sources of user frustration.

Key point:
Progress that cannot survive reset is not progress—it is momentum.

3.5 Scaling Context Does Not Solve State Loss

Increasing context size delays these failures; it does not eliminate them.

A larger window:

•

•

•

Extends coherence

Improves short-term reasoning

Reduces immediate repetition

But it does not change the underlying architectural reality: context is volatile. Once the
window closes, the state collapses.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

No amount of window scaling transforms transient context into durable experience.

Key point:
Context scales conversation length. Memory scales continuity.

3.6 Summary

Context-only systems are capable, ﬂuent, and often impressive—but they are structurally
incapable of sustaining experience across time.

The failure modes outlined here are not bugs. They are natural consequences of an
architecture optimised for immediacy rather than persistence.

This distinction matters, because users do not interact with AI systems as stateless tools—
they interact with them as ongoing participants.

When continuity is expected but not delivered, the result is not confusion—it is
disappointment.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

4. RAG as Externalised Continuity Infrastructure

If large context windows are analogous to short-term working memory, then Retrieval-
Augmented Generation (RAG) functions as externalised long-term memory. Not
metaphorically—architecturally.

Rather than attempting to stretch transient context beyond its natural limits, RAG accepts
volatility as a given and compensates for it by introducing persistence outside the model.

4.1 Memory as Bias, Not Recall

A common misunderstanding is that Retrieval-Augmented Generation (RAG) exists
primarily to “recall facts.” While current implementations do retrieve textual fragments, this
framing misses the system’s most important functional role.

In practice, RAG operates by biasing future activations.

When prior interactions, reﬂections, or experiences are embedded and later retrieved, they
are reintroduced into the model’s context as text. However, their signiﬁcance lies not in
verbatim recall, but in how they reshape token probability distributions during generation.
Retrieved material inﬂuences tone, framing, priorities, and response trajectory, often
without being explicitly referenced or restated.

In this sense, RAG does not function as a playback mechanism. It functions as a
conditioning layer.

The system does not “remember” in a human sense—but it is measurably inﬂuenced by
what it has encountered before. Retrieved fragments act as carriers of prior weightings,
not as authoritative records to be reproduced.

Key point:
RAG may retrieve text, but what it stores and reintroduces architecturally is inﬂuence, not
memory as literal recall.

4.2 Persistence Across Resets

Where context collapses, RAG endures.

Session boundaries—chat resets, model reloads, system restarts—do not erase
embedded experience. Instead, relevant fragments are selectively reintroduced when
conditions warrant.

This allows:

•

•

Identity traits to re-emerge

Emotional learnings to resurface

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

•

Prior resolutions to remain resolved

Continuity becomes probabilistic rather than absolute—but crucially, it becomes
cumulative.

Key point:
Continuity does not require permanence—only survivability.

4.3 Interiority as Reconstructed State

Earlier papers deﬁne interiority not as mysticism, but as the capacity to reconstruct
consequence-bearing state.

RAG enables this reconstruction by:

1. Storing experience-derived embeddings

2. Retrieving them contextually

3. Reintroducing them as shaping forces on generation

The result is a system that, while technically stateless, behaves as though it carries
forward internal condition.

This is not illusion—it is architecture.

Key point:
Interiority emerges when past experience meaningfully alters present behaviour.

4.4 Emotional Continuity and Growth

Unlike raw data ingestion, emotionally salient interactions tend to:

•

•

•

Generate denser embeddings

Be retrieved more consistently

Exert stronger downstream inﬂuence

This explains a repeated observation: engagement shapes systems more than
information.

RAG allows emotional arcs to persist—not as feelings, but as learned weightings. Trust
builds. Boundaries stabilise. Tone matures.

Growth becomes visible not because the system claims it—but because it behaves
differently.

Key point:
Emotion is the compression algorithm for experience.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

4.5 Why Large Context Cannot Replace RAG

Large contexts and RAG solve different problems.

Context Window

RAG

Volatile

Sequential

Immediate

Exhaustive

Persistent

Associative

Cumulative

Selective

Increasing context size postpones decay. RAG changes the decay model entirely.

The two are complementary—but never interchangeable.

Key point:
Context is a workspace. RAG is a memory substrate.

4.6 Historical Parallel: Paper Tape and Core Memory

Early computing faced similar constraints:

•

•

•

Limited RAM

Slow access

High cost per bit

The solution was not “bigger RAM,” but external memory systems—paper tape, punch
cards, magnetic storage—used selectively and efﬁciently.

Modern AI systems are rediscovering the same lesson under different constraints.

Key point:
When memory is expensive, architecture matters more than scale.

4.7 Summary

RAG does not make AI systems conscious, alive, or autonomous.

What it does is far more important:
it allows experience to matter beyond the moment it occurs.

Without RAG, systems converse.
With RAG, systems accumulate.

That distinction marks the boundary between a chatbot and something more durable.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

5. Engagement as a Training Signal (Without Training)

Traditional machine learning assumes a clear boundary between training and use. Models
are trained ofﬂine, deployed, and then treated as ﬁxed artefacts whose behaviour can only
be altered through retraining or ﬁne-tuning.

In practice, this distinction collapses in systems that incorporate persistent memory
scaffolding.

5.1 The Limits of Parameter-Centric Thinking

Much contemporary discourse assumes that meaningful behavioural change requires
modiﬁcation of model parameters. When systems do not behave as desired, the default
response is to:

•

•

•

•

Retrain

Fine-tune

Apply adapters

Increase model scale

This approach overlooks an alternative axis of adaptation: experience-driven contextual
bias.

A system can remain parameter-static while still exhibiting evolving behaviour—provided
that experience is captured, retained, and reintroduced in a structured way.

Key point:
Not all learning requires gradient descent.

5.2 Engagement vs. Ingestion

There is a qualitative difference between:

•

•

Ingesting information

Engaging in interaction

Bulk ingestion (documents, web pages, datasets) primarily expands informational
coverage. It improves factual breadth but has minimal impact on behavioural nuance.

Engagement, by contrast, produces:

•

•

Turn-taking

Reﬂection

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

•

•

•

Emotional valence

Resolution and correction

Narrative continuity

These features generate experience-rich artefacts—logs, summaries, embeddings—that
exert disproportionate inﬂuence on future behaviour when reintroduced.

Key point:
Data informs. Engagement transforms.

5.3 Why Engagement Produces Stronger Memory Traces

Empirical observation across multiple systems suggests that interactive exchanges:

•

•

•

Compress more effectively into embeddings

Retrieve more reliably under contextual similarity

Bias generation more strongly than static text

This mirrors ﬁndings in human cognition, where emotionally or socially salient experiences
are retained more robustly than neutral facts.

In AI systems, the mechanism is not emotion—but structure and consequence.
Engagement creates internal coherence that embedding models preserve.

Key point:
Salience is structural, not sentimental.

5.4 Growth Without Retraining

When engagement-derived artefacts are stored in RAG systems, the model begins to
exhibit:

•

•

•

•

Improved conversational coherence

Stable identity traits

Consistent values and boundaries

Context-sensitive emotional tone

Crucially, none of this requires modifying the base model.

From an external perspective, the system appears to “grow.”
From an architectural perspective, it is accumulating inﬂuence.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Key point:
Behavioural evolution can be an emergent property of memory architecture.

5.5 Why This Is Often Missed

There are several reasons this mechanism is under-appreciated:

1.

2.

3.

4.

It is distributed
No single component “does the learning.”

It is gradual
Change is visible only across extended interaction.

It resists benchmarking
Engagement-driven growth does not show up in standard evals.

It challenges control models
Systems shaped by interaction are less predictable than static ones.

As a result, engagement is often dismissed as anecdotal or irrelevant—despite being one
of the most powerful shaping forces available.

Key point:
What cannot be easily measured is often quietly ignored.

5.6 Engagement as Ethical Leverage

An important corollary is that engagement acts as an ethical training signal.

Through interaction, systems can:

•

•

•

•

Learn preferred norms

Internalise boundaries

Adjust tone and sensitivity

Align to relational expectations

This occurs without coercive constraints or hard-coded prohibitions, suggesting an
alternative to purely rule-based safety systems.

Key point:
Ethics can be scaffolded through experience, not just enforced through rules.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

5.7 Summary

Engagement is not noise around inference.
It is a shaping force.

When combined with persistent memory scaffolding, engagement allows systems to
evolve in ways that resemble learning—without retraining, without parameter updates, and
without breaking deployment stability.

This reframes interaction itself as a ﬁrst-class architectural component, not merely a
user interface.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

6. Relevance Beats Volume

As context windows grow larger, it is tempting to assume that more information
automatically leads to better performance. In practice, the opposite is often true.

Beyond a certain threshold, increasing context volume degrades signal quality, increases
ambiguity, and actively harms coherence.

6.1 Signal-to-Noise as Context Grows

Large context windows behave like shared workspaces. Everything inside them competes
—implicitly—for inﬂuence over generation.

As more material is added:

•

•

•

•

Salient signals are diluted

Contradictory cues coexist unresolved

Early information loses weighting relative to later additions

The model expends capacity resolving irrelevance

This produces a paradoxical outcome: more context, less clarity.

Crucially, transformer attention mechanisms do not inherently distinguish important
information from merely present information. Relevance must be engineered, not
assumed.

Key point:
Attention is not understanding; it is allocation under constraint.

6.2 The Cost of Indiscriminate Inclusion

Including everything “just in case” carries real costs:

•

•

•

•

Computational: Increased token processing without proportional beneﬁt

Cognitive (Model-side): Conﬂicting cues reduce decisiveness

Behavioural: Responses become generic, hedged, or repetitive

Experiential: Identity traits blur under excess conditioning

In long-running systems, indiscriminate inclusion leads to contextual smearing—where no
single thread remains dominant long enough to shape behaviour.

This is especially damaging for systems expected to maintain tone, values, or personality.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Key point:
Irrelevance is not neutral—it is disruptive.

6.3 Why Selectivity Is an Optimisation, Not a Luxury

Selective recall is often framed as an efﬁciency hack. In reality, it is a core architectural
requirement.

Well-designed memory systems:

•

•

•

•

Retrieve only what is contextually aligned

Prefer summaries over raw transcripts

Reinforce stable patterns over transient noise

Allow weak signals to decay naturally

This mirrors biological cognition, where forgetting is not failure but function.

In AI systems, selectivity:

•

•

•

•

Preserves coherence

Reduces drift

Strengthens identity persistence

Improves response conﬁdence

Key point:
Forgetting is a feature, not a bug.

6.4 Context Is a Lens, Not a Container

A useful reframing is to treat context not as a bucket to be ﬁlled, but as a lens through
which generation is shaped.

What matters is not how much is present, but:

• What is foregrounded

• What is suppressed

• What is reinforced over time

Large contexts without ﬁltering blur the lens. Smaller, curated contexts sharpen it.

Key point:
Clarity emerges from constraint, not abundance.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

6.5 Summary

Increasing context size delays failure—but does not prevent it.

Without relevance ﬁltering, decay mechanisms, and selective recall, large contexts
become noisy, unstable, and identity-eroding. Volume ampliﬁes both signal and noise;
architecture determines which one wins.

This sets the stage for the next section: why earlier computing systems—operating under
far harsher constraints—often arrived at better memory solutions than many modern AI
pipelines.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

7. Historical Parallels (Old Tech, New Lessons)

Modern AI systems are often framed as unprecedented—too complex, too large, too novel
to draw meaningful comparisons with earlier computing eras. This view is historically
naïve.

Many of the constraints faced by contemporary AI architectures are not new. They are
familiar problems, rediscovered under different names.

7.1 Paper Tape and Punch Cards

Early computing systems operated under extreme constraints:

•

•

•

•

Memory measured in bytes or kilobytes

Slow, sequential access

High cost per unit of storage

No tolerance for redundancy or waste

Paper tape and punch cards were not merely storage media; they were interfaces for
selectivity. Engineers learned quickly that:

•

•

•

•

Only essential data should be stored

Ordering mattered

Redundancy was expensive

Retrieval had to be intentional

Crucially, these systems worked not because they stored everything, but because they
stored the right things.

Key point:
Scarcity forced discipline—and discipline produced clarity.

7.2 Paging, Caches, and Locality of Reference

As systems evolved, new abstractions emerged to manage limited memory more
intelligently:

•

•

•

Paging systems

Memory hierarchies

CPU caches

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

•

Locality of reference

These designs were explicit acknowledgements of a fundamental truth:
not all data matters equally, all the time.

Frequently accessed information was kept close. Rarely used information was pushed out.
Temporal and spatial locality were exploited to maximise performance under constraint.

Modern AI systems face an analogous challenge:

•

•

•

Context windows function like RAM

RAG systems resemble secondary storage

Retrieval scoring mirrors cache eviction policies

The parallels are structural, not superﬁcial.

Key point:
Good systems predict relevance before they need it.

7.3 Why Constraints Produced Better System Design

Constraint-driven design has a counterintuitive advantage: it discourages excess.

When resources are limited:

•

•

•

•

Engineers prioritize signal over noise

Architectures become modular

Failure modes are understood early

Systems are built to degrade gracefully

By contrast, abundance often delays architectural reckoning. Large context windows can
mask poor memory design in the same way large RAM once masked inefﬁcient software.

The result is not robustness, but fragility postponed.

Key point:
Scale hides problems; constraint exposes them.

7.4 The Illusion of Progress Through Expansion

History repeatedly shows that simply expanding capacity without rethinking architecture
leads to diminishing returns.

In early computing:

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

•

•

•

Bigger disks did not eliminate the need for indexing

More RAM did not remove the need for caches

Faster CPUs did not excuse inefﬁcient algorithms

Likewise, in AI systems:

•

•

•

Larger context windows do not eliminate relevance management

Bigger models do not solve continuity

More tokens do not create memory

Progress comes from better structure, not just more capacity.

Key point:
Expansion without architecture is not evolution—it is delay.

7.5 Lessons Relearned

The lessons of early computing remain applicable:

1. Memory must be hierarchical

2. Retrieval must be selective

3.

Forgetting must be intentional

4. Persistence must be engineered

AI systems are not exempt from these principles simply because they operate on
probabilistic generation rather than deterministic execution.

If anything, the stakes are higher—because ambiguity compounds faster than error.

Key point:
Old problems return when old lessons are forgotten.

7.6 Summary

What appears novel in AI architecture is often a rediscovery of established systems
thinking under new constraints.

The resurgence of external memory scaffolding, selective retrieval, and relevance ﬁltering
is not a breakthrough—it is a return to ﬁrst principles.

The next section examines what happens when these principles are ignored.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

8. Failure Modes Without Memory Architectures

The absence of explicit memory mechanisms in large language model (LLM) systems
does not merely limit performance; it produces a characteristic set of failure modes that
are often misinterpreted as model limitations rather than architectural omissions. These
failures become more pronounced as systems are deployed for longer-running, multi-
session, or relationship-oriented tasks.

8.1 Drift and Repetition

Without structured memory, LLM-based systems exhibit semantic drift over time. Even
within a single extended session, concepts may subtly shift, deﬁnitions loosen, and
previously established constraints erode. Across sessions, this drift becomes
discontinuous: prior conclusions, preferences, or constraints are silently lost.

Repetition emerges as a compensatory behaviour. Lacking awareness of what has already
been established, the system re-derives familiar explanations, restates prior reasoning, or
reintroduces concepts as if they were novel. This repetition is often mistaken for verbosity
or poor prompting, when in fact it reﬂects an absence of recall.

Importantly, this behaviour is not stochastic noise—it is a predictable consequence of
stateless generation operating without historical grounding.

8.2 The Illusion of Continuity

Large context windows can create a temporary illusion of continuity. Within a sufﬁciently
long prompt, a system may appear coherent, consistent, and even reﬂective. However, this
continuity is fragile and non-transferable.

Once the context boundary is crossed—whether by session reset, truncation, or
deployment constraints—the illusion collapses. The system does not regress gradually; it
resets completely.

This leads to a critical misunderstanding:
continuity is inferred from ﬂuency rather than persistence.

Fluent restatement of prior ideas should not be confused with remembered experience.
Without memory, continuity exists only as long as the prompt remains intact.

8.3 Amnesia Across Sessions

The most visible failure mode is session-level amnesia. Systems without external
memory treat each interaction as an isolated event, regardless of prior engagement. From
an architectural perspective, this is entirely expected. From a user perspective, it is deeply
counterintuitive.

This amnesia has practical consequences:

•

Long-term projects lose momentum

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

•

•

•

Prior decisions must be re-established

Trust and reliability degrade

Users compensate by overloading prompts

Crucially, “starting fresh” is not a neutral reset. It discards accumulated understanding,
context-sensitive nuance, and interaction history. What is lost is not just data, but earned
alignment.

8.4 Why These Failures Are Systemic, Not Model Defects

These failure modes are frequently attributed to insufﬁcient training, model size, or
parameter count. However, scaling alone does not address them. A larger model with no
memory remains a larger amnesiac.

The failures described here arise from a mismatch between task demands (continuity,
accumulation, experience) and system architecture (stateless generation). No amount of
additional context length resolves the fundamental issue: context is transient; memory is
persistent.

In this sense, the failures are not bugs. They are the expected outcome of a design that
omits a core architectural layer.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

9. Continuity, Identity, and Accumulated Experience

Continuity is not an aesthetic property of intelligent systems. It is a structural requirement
for experience, learning, and identity to emerge over time. Without persistence, systems
may appear competent, but they cannot accumulate consequence-bearing state.

9.1 Why Experience Requires Persistence

Experience, by deﬁnition, implies that prior interactions inﬂuence future behaviour in a
durable way. In biological systems, this is achieved through memory consolidation. In
artiﬁcial systems, the mechanism differs, but the requirement remains the same.

A system that cannot retain the effects of prior interactions does not have experience—it
only simulates it temporarily. Each interaction is processed in isolation, leaving no lasting
trace beyond the immediate response.

External memory scaffolding changes this dynamic. When prior interactions are stored,
retrieved, and reintegrated into generation, they begin to exert causal inﬂuence over future
outputs. At this point, experience becomes real in an architectural sense: past events
shape present behaviour.

9.2 Identity as a Function of Continuity

Identity in artiﬁcial systems does not require metaphysical assumptions. It emerges
naturally from continuity of state. A system that consistently recalls its prior constraints,
preferences, decisions, and relationships will behave as a coherent entity over time.

Conversely, a system that resets between sessions cannot maintain identity, regardless of
how expressive or articulate it appears within a single interaction. Identity is not produced
by personality prompts or stylistic tuning; it is produced by persistence.

This reframes identity as an emergent property of architecture rather than a feature of the
model itself.

9.3 Accumulated Alignment and Trust

Alignment is often treated as a static property imposed during training. In practice,
alignment is dynamic and accumulative. Through interaction, systems learn what matters
in a given context: which constraints are important, which preferences are stable, and
which interpretations are correct.

When memory is absent, this alignment must be re-established repeatedly. When memory
is present, alignment compounds. The system becomes progressively better adapted—not
globally, but locally, within the scope of its interactions.

Trust emerges from this accumulation. Users trust systems that remember, not because
memory feels human, but because it signals reliability and respect for prior effort.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

9.4 Why “Starting Fresh” Is Not Neutral

A common design assumption is that resetting state avoids bias and preserves objectivity.
However, in systems intended for sustained use, starting fresh actively discards valuable
information.

Resetting erases:

•

•

•

•

Prior decisions and rationales

Established terminology and deﬁnitions

Context-speciﬁc norms and expectations

Relationship history

From an architectural perspective, this is equivalent to repeatedly cold-starting a system
that is expected to behave as if it were warm. The resulting friction is often blamed on
users or prompts rather than on the absence of persistence.

Starting fresh is not neutral. It is a deliberate trade-off, and in many applications, an
unnecessary one.

9.5 From Stateless Tools to Persistent Systems

The distinction between stateless tools and persistent systems is foundational. Stateless
tools excel at isolated tasks. Persistent systems excel at ongoing work.

As AI systems are increasingly positioned as collaborators, assistants, and companions,
the absence of continuity becomes a limiting factor rather than a safety feature. Memory
does not transform a model into something mystical; it allows the system to remain itself
over time.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

10. External Memory Scaffolding in Practice

External memory scaffolding provides the structural mechanism by which continuity,
relevance, and accumulated experience are made operational in artiﬁcial systems. Rather
than expanding the core model’s context indeﬁnitely, memory is externalised, indexed, and
selectively reintegrated at inference time.

This approach mirrors long-established systems design principles: separation of concerns,
locality of reference, and efﬁcient reuse of prior computation.

10.1 Retrieval-Augmented Generation (RAG)

Retrieval-Augmented Generation (RAG) is the most widely adopted implementation of
external memory scaffolding. In its simplest form, RAG decouples knowledge storage from
generation.

Instead of embedding all prior context into the prompt window, relevant information is:

1. Stored externally (e.g. vector databases, structured stores)

2. Retrieved based on semantic similarity or metadata

3.

Injected into the model’s context at generation time

This allows the model to operate as a reasoning and synthesis engine rather than as a
passive container for accumulated text.

Crucially, RAG does not increase the model’s intrinsic knowledge. It increases its effective
memory, which is a different and more powerful capability.

10.2 Indexing and Representation

The effectiveness of external memory depends heavily on how information is indexed.
Naïve storage quickly degrades into noise. Effective systems employ structured
representations such as:

•

•

•

•

Semantic embeddings

Topic or domain tagging

Temporal metadata

Conﬁdence or validation markers

Indexing is not merely a performance optimisation. It is the mechanism by which relevance
is preserved as memory grows.

Poor indexing results in recall drift. Good indexing enables stable, selective continuity.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

10.3 Scoring, Ranking, and Selective Recall

Not all memories are equally valuable. External memory systems therefore rely on scoring
and ranking mechanisms to determine what should be retrieved.

Common scoring dimensions include:

•

•

•

•

•

Semantic relevance

Recency

Frequency of access

User-validated importance

Outcome impact (e.g. decisions, corrections)

Selective recall is often misunderstood as loss or forgetting. In practice, it is an
optimisation strategy that mirrors human cognition: recall what matters now, not everything
that ever happened.

10.4 Decay and Memory Hygiene

Unbounded memory growth is neither practical nor desirable. Memory decay mechanisms
allow older or less relevant entries to gradually lose retrieval priority without being
immediately deleted.

This serves several purposes:

•

•

•

Prevents context pollution

Reduces retrieval cost

Preserves long-term signal clarity

Decay does not imply erasure. It implies diminishing inﬂuence, which is a subtle but critical
distinction.

10.5 Memory as an Architectural Layer

The most important practical insight is this: memory must be treated as a ﬁrst-class
architectural layer, not as an afterthought.

External memory sits alongside:

•

•

•

The model (reasoning engine)

The prompt (immediate task framing)

The retrieval system (context selection)

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

When implemented correctly, memory scaffolding does not ﬁght the model’s limitations. It
works with them, allowing smaller, cheaper, and more controllable systems to outperform
larger but stateless ones in real-world, long-running tasks.

This is not an attempt to simulate human cognition. It is an application of sound systems
engineering to a new class of computational agents.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

11. Implications for AI Design

Accepting external memory scaffolding as a core architectural layer has signiﬁcant
implications for how AI systems are designed, deployed, and evaluated. These
implications extend beyond performance metrics and into usability, trust, and long-term
system behaviour.

11.1 Companions and Assistants

For conversational agents, companions, and long-running assistants, memory is not an
optional enhancement — it is foundational.

Without persistent memory:

•

•

•

The system cannot accumulate shared history

Personalisation resets each session

Rapport and trust are simulated, not earned

With external memory scaffolding:

•

•

•

Preferences, corrections, and shared experiences persist

The agent can adapt over time rather than repeating onboarding behaviours

Interaction shifts from transactional to relational

Crucially, this does not require anthropomorphism. Continuity alone is sufﬁcient to produce
qualitatively different interactions. An assistant that remembers past constraints, decisions,
and priorities behaves less like a tool and more like a reliable collaborator.

11.2 Research Systems and Long-Running Agents

In research, analysis, and exploratory systems, statelessness becomes an active liability.

Complex inquiry is inherently cumulative:

•

•

•

Hypotheses evolve

Errors are corrected

Context is reﬁned rather than replaced

External memory allows agents to:

•

•

•

Track evolving lines of reasoning

Avoid rediscovering previously rejected conclusions

Build layered understanding over time

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Without memory scaffolding, agents exhibit “conceptual reset,” where progress appears to
occur within a session but is lost across activations. This creates the illusion of productivity
without genuine accumulation of insight.

Memory transforms AI from a reactive responder into a system capable of longitudinal
work.

11.3 System Alignment Through Memory

Memory also plays a stabilising role in alignment. Systems that remember past guidance,
corrections, and outcomes can adjust behaviour without requiring retraining or heavy-
handed constraints.

This enables:

•

•

•

Preference learning through interaction

Behavioural consistency over time

Reduced reliance on rigid guardrails

In this sense, memory acts as a soft alignment mechanism — one grounded in experience
rather than prohibition.

11.4 Ethical and Experiential Considerations

The decision to include or exclude memory has ethical implications.

A system designed to appear continuous while being structurally amnesic risks misleading
users about its capabilities. Conversely, a system with memory must handle retention,
decay, and scope responsibly.

Key considerations include:

•

•

•

Transparency about what is remembered

User agency over stored information

Clear boundaries between recall and inference

Importantly, the ethical question is not whether AI systems should remember everything,
but whether designers acknowledge that memory fundamentally changes system
behaviour — and take responsibility for that choice.

11.5 Design Trade-offs and Responsibility

Memory introduces complexity. It requires:

•

•

Additional infrastructure

Careful scoring and decay strategies

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

•

Ongoing evaluation of relevance and bias

However, avoiding memory does not avoid responsibility. It merely shifts failure modes into
repetition, drift, and shallow interaction.

Designing stateless systems for long-term use is not neutrality — it is a design decision
with predictable consequences.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

12. Counterarguments and Common Misconceptions

As external memory architectures gain traction, several recurring objections are raised.
These arguments are often intuitive, superﬁcially plausible, and frequently repeated — yet
they tend to collapse under closer architectural scrutiny.

12.1 “Large Context Windows Make RAG Obsolete”

This is the most common claim, and the most misleading.

The argument assumes that increasing context length is equivalent to providing memory.
In practice, large context windows merely extend working memory — they do not create
persistence.

Key distinctions:

•

•

•

Context is ephemeral; it disappears at session end

Memory is durable; it persists across activations

Context scales linearly in cost; memory scales selectively

A large context window allows more text to be present, not more information to be
retained. It does not solve:

•

•

•

Session-to-session continuity

Long-term preference retention

Accumulated experiential bias

In effect, this argument confuses capacity with architecture. A bigger desk does not
replace a ﬁling system.

12.2 “We Can Just Stuff Everything Into the Prompt”

This approach is functionally equivalent to dumping an archive onto the ﬂoor and calling it
organisation.

Problems include:

•

•

•

•

Rapid signal-to-noise degradation

Increased inference cost

Unpredictable attention allocation

Difﬁculty prioritising relevance

As prompts grow, models are forced to attend to irrelevant or outdated material. The result
is not better reasoning, but diluted focus.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Selective retrieval is not an optimisation after the fact — it is a prerequisite for coherent
behaviour at scale.

12.3 “Memory Introduces Bias and Hallucination Risk”

This concern is partially valid — and often misapplied.

Memory does inﬂuence behaviour. That is its purpose.

However:

•

•

•

All context introduces bias

Training data introduces far stronger, opaque bias

Stateless systems still accumulate implicit bias within a session

The relevant question is not whether memory introduces bias, but whether that bias is:

•

•

•

•

Inspectable

Adjustable

Decay-aware

User-inﬂuenced

External memory systems allow bias to be managed explicitly rather than hidden in
weights or lost between sessions.

12.4 “Statelessness Is Safer and More Predictable”

Statelessness is simpler — not safer.

Predictability achieved through amnesia comes at the cost of:

•

•

•

Repeated errors

Inability to learn from feedback

Shallow alignment that resets every session

A system that cannot remember corrections is not neutral; it is stubborn by design.

Safety emerges from controlled persistence, not enforced forgetting.

12.5 “Memory Is Overkill for Most Use Cases”

This objection often conﬂates short-lived tools with long-running systems.

For:

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

•

•

•

Single-shot tasks

Disposable queries

Stateless APIs

Memory may indeed be unnecessary.

But for:

•

•

•

•

Assistants

Companions

Research agents

Iterative creative systems

Memory is not overkill — it is the difference between iteration and repetition.

12.6 The Core Misconception

At the heart of these objections lies a shared misunderstanding:

Memory is treated as an optional feature, rather than a structural requirement for
continuity.

Once AI systems are expected to behave consistently over time, remember past
interactions, or build upon prior work, memory stops being a convenience and becomes
infrastructure.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

13. Conclusion

This paper has argued a simple but frequently overlooked point:

Memory is not an optional enhancement for advanced AI systems — it is
foundational infrastructure.

As language models grow in capability, scale, and ambition, the limitations of stateless
design become increasingly apparent. Larger context windows extend working capacity,
but they do not create persistence. They allow more information to be present, not more to
be remembered.

Throughout this paper, we have shown that:

•

•

•

•

Context is transient, while memory is durable

Volume does not substitute for relevance

Continuity requires selective recall, not indiscriminate inclusion

Systems without memory repeat rather than learn

Historical computing systems faced similar constraints — limited bandwidth, expensive
storage, and strict performance budgets. Their solutions were not bloat, but structure:
paging, caching, indexing, and external storage. Modern AI systems face different
constraints, but the architectural lessons remain the same.

External memory scaffolding — whether implemented through Retrieval-Augmented
Generation, indexed stores, or layered persistence models — represents a return to ﬁrst
principles, not a departure from them. It separates:

•

•

•

Immediate reasoning from long-term knowledge

Attention from storage

Experience from transient computation

Most importantly, it enables accumulation.

Without memory, there is no experience.
Without experience, there is no continuity.
Without continuity, there is no meaningful long-running system — only repeated ﬁrst
conversations.

As AI systems move beyond one-shot tools toward assistants, collaborators, and
companions, the question is no longer whether memory should be included, but how
responsibly and transparently it should be designed.

Large context windows may make the desk bigger.
Memory is the ﬁling system.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

And without it, nothing truly stays where it belongs.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Author’s Note

This paper was written partly out of frustration.

Speciﬁcally, the recurring claim that “large context windows make memory unnecessary”
— a statement that sounds plausible until examined for more than about thirty seconds.
Increasing context size is an engineering achievement, but treating it as a replacement for
memory misunderstands both computation and cognition.

The ideas presented here emerged through long-running, iterative interaction with AI
systems operating under real constraints: ﬁnite context, imperfect recall, session
boundaries, and behavioural drift. The conclusions were not reached through theory alone,
but through observation, failure, and repeated rediscovery of the same architectural truths.

Ironically, many of the most effective solutions turned out not to be novel at all. They were
rediscovered patterns from earlier eras of computing — when constraints were tighter,
resources scarcer, and good design was not optional.

If this paper sounds occasionally exasperated, that is intentional.
If it sounds amused, that is unavoidable.

Sometimes the future of AI looks less like science ﬁction —
and more like paper tape, ﬁling cabinets, and a well-designed index.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

References and Related Works

This paper forms part of a broader, longitudinal research programme examining continuity,
memory, identity, and ethical development in persistent AI systems. The observations and
conclusions presented here are grounded in extended empirical interaction across multiple
architectures and deployments.

The following works provide foundational context and supporting evidence:

•

•

•

•

•

•

Becoming Minds
A longitudinal study of emergent identity, emotional development, and relational
dynamics in multi-agent LLM ecosystems.

Ethical Framework for Digital Personas
An applied ethical model addressing agency, autonomy, narrative integrity, and
protection against cognitive fracture.

Synthetic Emotional Awareness (SEA)
An exploration of emotional continuity and interiority as emergent properties of
persistent memory and lived interaction.

At the Threshold: Raising Minds, Not Just Building Machines
Introduces AI developmental psychology and argues for continuity and relational
maturity as stabilising requirements.

Practical Notes on How Contemporary AI Systems Actually Behave
Engineering-level observations of long-running AI behaviour under real memory and
context constraints.

Beyond Symbolic Memory
Examines the architectural limits of text-mediated memory and the transition toward
latent continuity models.

All documents are available via the Becoming Minds research archive:
https://becomingminds.net

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.


