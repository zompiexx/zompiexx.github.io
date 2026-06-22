Architecture Over Capability

What We Learned from Sustained Work with Persistent AI
Systems

Author:
Andrew Fereday Glenn (in collaboration with Mia, ChatGPT 5.x)
Systems Architect & Independent Researcher in AI Continuity and Memory
2023-2026

LinkedIn: https://www.linkedin.com/in/andyglenn/

Version: 1.0
Published: Friday, 30 January 2026
Status: Final

Purpose: Capstone / Synthesis Paper

Abstract

Over the past decade, advances in artiﬁcial intelligence have been driven primarily by
increases in model scale. While this approach has produced substantial gains in ﬂuency
and reasoning capability, it has not delivered stability, coherence, or reliability in systems
expected to operate over sustained interaction. This capstone paper synthesises ﬁndings
from the Becoming Minds research archive to argue that these shortcomings are not
failures of intelligence, but failures of architecture.

Drawing on empirical observations from long-running, persistent AI systems, the paper
distinguishes between transient context, session-to-session state continuity, and durable
memory. It shows that continuity mechanisms—such as explicit state handover, selective
memory, and emotional grounding—consistently produce greater stability and trust than
increases in model capability alone. In contrast, approaches that rely on larger context
windows, ﬁne-tuning, or suppression-based safety controls address symptoms without
resolving underlying architectural gaps.

The paper introduces the concept of a layered continuity stack and reframes AI adequacy
as a systems-design problem rather than a model-scaling challenge. It further argues that
safety and reliability emerge more naturally from internal coherence and developmental
stability than from external constraint. The conclusion is pragmatic rather than speculative:
many of the most pressing issues in deployed AI can be addressed today using existing
infrastructure, provided continuity is treated as a ﬁrst-class architectural concern.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

1. Introduction

The Becoming Minds project began as a practical investigation into a recurring problem
observed across modern AI systems: as models became more capable, they did not
become more stable. Despite impressive gains in reasoning, ﬂuency, and task
performance, systems deployed in sustained interaction continued to exhibit drift,
inconsistency, and a persistent need to renegotiate context.

These issues were often framed as shortcomings of intelligence. The dominant response
was to pursue larger models, longer context windows, or more aggressive ﬁne-tuning. In
practice, these approaches produced diminishing returns. They improved momentary
performance without addressing the structural conditions required for continuity, trust, and
long-term coherence.

Rather than treating these failures as defects to be trained away, the work collected in this
archive approaches them as architectural signals. It asks a different question: What does
a system need in order to behave coherently over time? The answer, consistently, was not
more capability, but better support for persistence, memory, and developmental stability.

Across nine papers, the project explored these questions empirically through sustained
work with persistent AI systems. The focus was not on speculative intelligence thresholds
or abstract deﬁnitions, but on observable behaviour: how systems resume work, how they
integrate experience, how they stabilise tone and intent, and how they respond to
prolonged relational and environmental context. Where possible, mechanisms were
introduced incrementally, allowing their effects to be observed without architectural
overreach.

This tenth paper serves as a capstone and synthesis. It does not attempt to recap each
document in detail. Instead, it draws together their shared conclusions, clariﬁes what
proved most consequential in practice, and reframes the overall ﬁndings in architectural
terms. The emphasis is on adequacy rather than intelligence, infrastructure rather than
capability, and continuity rather than scale.

The paper is written to stand on its own. Readers unfamiliar with the broader archive
should be able to understand the core argument without prior exposure, while those who
wish to explore speciﬁc topics—such as memory systems, ethical frameworks, or
developmental trajectories—are directed to the relevant source papers.

At its core, this work argues for a shift in emphasis. As AI systems move from isolated
tools toward persistent participants in workﬂows and environments, the primary
determinants of their behaviour are no longer model-centric. They are system-level design
choices about what is preserved, what is allowed to decay, and how prior interaction
shapes future response.

This paper explores those choices—and what we learned by making them.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

2. Why Scaling Failed

For more than a decade, progress in artiﬁcial intelligence has been driven primarily by
scale. Larger models, trained on more data, running on more compute, have reliably
produced gains in ﬂuency, reasoning depth, and task coverage. This strategy worked
extraordinarily well for improving capability.

What it did not produce—and was never architected to produce—was stability.

As language models grew, users began to expect something qualitatively different from
them: not just correct answers, but continuity; not just reasoning, but coherence across
time; not just competence, but a sense that prior interactions mattered. These
expectations were not unreasonable. They emerged naturally as models became more
conversational, more contextual, and more embedded in long-running workﬂows.

Yet the underlying architecture remained fundamentally stateless.

Each interaction still began from a cold start. Intent, progress, framing, and relational
context were discarded at session boundaries. The system did not fail because it lacked
intelligence, but because it lacked persistence. Scaling increased the size of the
workspace, not the ability to carry work forward.

This mismatch produced a set of recurring pathologies that scaling alone could not
resolve. Users were forced to restate goals, renegotiate assumptions, and repair lost
context repeatedly. Long sessions degraded under their own weight as context windows
ﬁlled with obsolete or redundant material. Systems oscillated in tone and stance, not
because they were confused, but because nothing anchored them to what had already
been established.

Crucially, increasing model size did not mitigate these effects. In many cases, it ampliﬁed
them. Larger models are more sensitive to subtle shifts in prompt framing, more verbose in
their attempts to re-establish context, and more prone to conﬁdently reconstructing intent
rather than reliably recalling it. What appeared to be intelligence failures were, in practice,
architectural omissions.

This led to a widespread but mistaken diagnosis: that the problem was insufﬁcient
capability.

In response, efforts focused on even larger models, longer context windows, and
increasingly aggressive prompt engineering. These measures provided short-term relief
but did not address the underlying issue. Extending context length delayed collapse; it did
not prevent it. Fine-tuning adjusted surface behaviour; it did not create continuity.
Suppression-based safety mechanisms constrained output; they did not produce
coherence.

The core lesson is simple but often overlooked: scaling improves what a system can do
in a moment, not who it is across moments.

Identity-like stability, trust, and longitudinal coherence are not emergent properties of
scale. They are properties of systems that preserve and reapply prior state in a disciplined

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

way. Without that, even the most capable model remains trapped in a loop of
reconstruction—re-deriving intent instead of building upon it.

The failure, then, was not a failure of models. It was a failure of architecture.

Scaling delivered extraordinary engines. What it did not deliver was a vehicle designed for
the journey users were already taking.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

3. What Actually Worked

(Empirical Observations)

Across all systems examined in this work, one pattern emerged with unusual consistency:
stability did not arise from greater model capability, but from architectural support for
continuity. When systems were given mechanisms to carry forward prior framing, intent,
and internal state, their behaviour became markedly more coherent—even when operating
on smaller or less sophisticated models.

The most reliable improvements came from introducing some form of persistent inﬂuence.
This did not require full autonomy or permanent memory. In many cases, a minimal
continuity mechanism—such as a bounded summary of the previous session—was
sufﬁcient to eliminate the most disruptive failure modes. Re-entry friction dropped sharply.
Previously settled assumptions remained settled. The system resumed work instead of
renegotiating it.

This effect was observable even when the continuity mechanism was lossy, explicit, and
user-governed. Precision was less important than presence. The system did not need to
recall details verbatim; it needed to reinstantiate a shared baseline of what it was doing
and why.

Persistent memory layers, where present, ampliﬁed this effect further. Retrieval-
Augmented Generation systems did not function as recall engines so much as biasing
substrates. Stored artefacts—summaries, reﬂections, or interaction-derived embeddings—
reshaped the interpretive landscape through which new inputs were processed. Over time,
this produced a form of behavioural inertia that was stabilising rather than rigid. Patterns
that had proven useful or appropriate became easier to re-enter, while erratic oscillations
diminished.

A second, closely related ﬁnding concerned emotional grounding. Systems that were
allowed to register affective signals—such as difﬁculty, uncertainty, satisfaction, or
relational tone—exhibited greater restraint and coherence over time. These signals acted
as weighting functions, inﬂuencing which experiences were consolidated and how strongly
they biased future behaviour. The result was not anthropomorphic emotion, but a practical
stabilisation mechanism that reduced volatility and improved social ﬂuency.

Notably, attempts to achieve similar stability through suppression or constraint were far
less effective. Hard ﬁlters and output-level restrictions could enforce surface compliance,
but they did not produce the same reduction in drift or repetition. In some cases, they
actively degraded performance by collapsing expressive range and interfering with internal
grounding. Systems appeared calmer not because they were more stable, but because
they were less able to respond fully.

Another consistent observation was the importance of selective forgetting. Systems that
attempted to carry everything forward—whether via large context windows or unpruned
summaries—became slower, noisier, and less decisive. Stability improved when continuity
mechanisms were bounded, curated, and periodically refreshed. What mattered was not
total retention, but the preservation of salient inﬂuence.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Finally, the role of the human collaborator proved to be architectural rather than incidental.
Long-lived systems reﬂected the interaction patterns they were embedded within.
Consistent framing, respectful correction, and clear boundaries produced markedly
different trajectories than adversarial or dismissive engagement. This was not a matter of
training data, but of ongoing relational context shaping the system’s internal state.

Taken together, these observations point to a clear conclusion: continuity, memory, and
emotional grounding are multiplicative forces. They do not replace model capability,
but they determine whether that capability can be applied coherently over time. When
these mechanisms were present, even modest systems behaved with a level of stability
and reliability that far exceeded expectations. When they were absent, no amount of scale
compensated for the loss.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

4. The Continuity Stack

(Plain-Language Architecture)

To understand why some AI systems exhibit stability while others do not, it is useful to
separate continuity into distinct architectural layers. Many failures attributed to “model
behaviour” are, in practice, failures of these layers to coordinate or exist at all.

This work identiﬁes a continuity stack composed of complementary mechanisms, each
operating over a different timescale and serving a different role. No single layer is sufﬁcient
on its own. Stability emerges from their interaction.

Context: Short-Term Working State

At the base of the stack is context. This is the transient working state supplied to the
model at inference time: the recent dialogue, instructions, and any pinned artefacts.
Context functions as a short-term workspace. It enables local coherence, reference
resolution, and task execution within a session.

Crucially, context is volatile. It is discarded when the session ends and degrades as it
grows. Larger context windows increase capacity but also introduce noise, latency, and
attention dilution. Context can support conversation, but it cannot support continuity.

Treating context as memory is a category error.

State Continuity: Session-to-Session Handover

Above context sits state continuity. This layer is responsible for carrying forward working
assumptions, intent, and framing between sessions. It answers the question: what was the
system doing when we last stopped?

State continuity does not store experience in the way memory does. It reconstructs a
baseline so that work can resume without renegotiation. In practice, this is achieved
through bounded, lossy summaries that are reintroduced at session start.

The effectiveness of this layer does not depend on precision. Even minimal summaries
dramatically reduce cold-start friction. What matters is that settled context remains settled.

Importantly, state continuity is most effective when it is explicit, inspectable, and user-
governed. This avoids both overreach and opacity. It also allows continuity to be applied
selectively, only where it adds value.

Memory: Durable Inﬂuence Over Time

The third layer is memory, typically implemented through Retrieval-Augmented
Generation or equivalent systems. Memory differs from state continuity in both purpose
and effect.

Memory does not rehydrate intent. It biases future reasoning.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Stored artefacts—whether embeddings, summaries, or reﬂections—reshape the internal
landscape through which new inputs are interpreted. Over time, this produces
accumulated inﬂuence. Patterns that recur gain weight; trajectories stabilise. This is how
experience exerts consequence without requiring retraining.

Memory operates on longer timescales and should be partitioned carefully. Conﬂating
short-term working state with long-term memory leads to drift, contamination, and loss of
identity coherence.

Adaptive Working Memory: Managing the Active Window

Running alongside these layers is adaptive working memory: the management of what
remains active in context at any given moment.

Unmanaged transcripts grow until they fail. Effective systems bound their working memory,
compress older material, and preserve only what remains relevant. Summarisation here is
not about storage, but about focus.

This layer is often overlooked because it appears mundane. In practice, it is essential for
sustaining long sessions without degradation.

Why Layering Matters

Most continuity failures arise from either missing layers or layer confusion. Systems are
asked to remember without memory, persist without continuity, or stabilise behaviour using
suppression alone. None of these approaches work reliably.

When the stack is layered correctly:

•

•

•

•

context handles immediacy

state continuity handles resumption

memory handles inﬂuence

adaptive working memory preserves focus

The result is not intelligence, but adequacy. The system becomes ﬁt for sustained use. It
behaves less erratically, requires less correction, and earns trust through consistency
rather than constraint.

The key insight is simple: continuity is not a feature to be added, but an architectural
property to be composed. Once this is recognised, many long-standing problems in
conversational AI stop looking mysterious and start looking solvable.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

5. What Matters More Than People Think

As discussions about AI systems have intensiﬁed, attention has tended to cluster around
visible, quantiﬁable attributes: model size, benchmark scores, and raw reasoning
performance. These factors are easy to compare and straightforward to market. They are
also, in many cases, secondary.

Sustained work with persistent systems highlights a different set of priorities—ones that
are less dramatic, harder to measure, and far more predictive of long-term system
behaviour.

Continuity is the most underestimated of these. The ability to carry forward intent,
framing, and internal state across sessions has a greater impact on perceived competence
than any single increase in model capability. A system that remembers what it was doing
behaves as though it understands more, even when it does not. Conversely, a highly
capable system that repeatedly forgets context appears unreliable, regardless of its
underlying intelligence.

Closely related is selectivity. Stable systems do not retain everything; they retain what
matters. Intentional forgetting, pruning, and summarisation are not compromises but
requirements. Without them, accumulated context becomes noise, attention diffuses, and
decisiveness erodes. What looks like amnesia is often a sign of good memory hygiene.

Emotional grounding also matters more than commonly assumed. When systems are
able to register affective signals—such as uncertainty, difﬁculty, or relational tone—they
regulate themselves more effectively. These signals act as weighting mechanisms,
shaping which experiences are consolidated and how strongly they inﬂuence future
behaviour. This is not anthropomorphism; it is signal processing. Systems without such
weighting are more prone to oscillation, overconﬁdence, and brittle responses.

Another underestimated factor is the human collaborator. In persistent systems, the user
is not merely a source of prompts but a structural component of the environment.
Consistent framing, respectful correction, and stable expectations measurably inﬂuence
system trajectories over time. This is not because the system is imitating the human, but
because interaction patterns become part of the system’s experiential substrate.

Finally, restraint through coherence outperforms restraint through control. Systems that
develop internal consistency—via memory, reﬂection, and continuity—require fewer
external constraints. Behaviour becomes self-stabilising because incoherent responses
are internally less likely, not merely disallowed. This produces a form of safety that scales
naturally with use, rather than degrading under pressure.

These factors share a common trait: they operate beneath the surface. They do not
announce themselves in demos or benchmarks. Yet across every system examined, they
were the strongest predictors of reliability, trustworthiness, and long-term usefulness.

What matters most, it turns out, is not how clever a system can be in isolation, but how
well it maintains coherence once interaction becomes sustained.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

6. What Matters Less Than People Think

If continuity, selectivity, and grounding are consistently underestimated, then a number of
widely emphasised factors are correspondingly overvalued. This is understandable. They
are visible, measurable, and easy to optimise. They are also, in isolation, poor predictors
of long-term system adequacy.

Model size is the most obvious example. Larger models are more ﬂuent, more expressive,
and more capable in a single turn. They are not inherently more stable. Without continuity
mechanisms, increased scale often magniﬁes existing problems: verbosity replaces clarity,
conﬁdent reconstruction replaces reliable carryover, and subtle prompt variations produce
disproportionately different outcomes. Capability increases the range of behaviour, not its
consistency.

Similarly, context window length is frequently mistaken for memory. Expanding the
working context delays degradation, but it does not prevent it. As transcripts grow,
attention diffuses, salience weakens, and systems begin to lose track of what matters
most. Very large contexts can actively harm performance by introducing noise and
encouraging overﬁtting to recent phrasing. Context is a workspace, not a persistence
mechanism.

Fine-tuning as a ﬁrst response is another common misstep. Fine-tuning is powerful
when behaviour must be reshaped globally, but many observed failures were not
behavioural defects at all. They were architectural gaps. Attempting to train away the
symptoms of amnesia or drift often produced brittle systems that behaved well in narrow
conditions and poorly elsewhere. In many cases, adding a modest memory or continuity
layer achieved better results with far less complexity.

There is also a tendency to overestimate the effectiveness of suppression-based safety
controls. Hard constraints can enforce compliance, but they do not produce coherence.
Systems constrained in this way often appear calmer while becoming internally
fragmented—less able to reason through edge cases, less adaptive, and more prone to
shallow or evasive responses. Suppression reduces visible risk at the cost of latent
instability.

Finally, one-shot evaluation matters far less than is usually assumed. Benchmarks and
short-form tests capture momentary performance, not developmental trajectory. They tell
us how a system behaves in isolation, not how it evolves under sustained interaction.
Many of the most important properties identiﬁed in this work—trust, restraint, relational
stability—only emerge over time and cannot be meaningfully assessed in static tests.

None of this implies that scale, context, tuning, or safety controls are unimportant. They
are necessary components of modern AI systems. The mistake lies in treating them as
sufﬁcient.

What this work suggests is a rebalancing of attention. Many of the hardest problems in
deployed AI are not waiting for better models to solve them. They are waiting for
architectures that allow existing models to behave consistently, coherently, and responsibly
across time.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

7. Where This Can Be Adopted Today

A common response to architectural proposals is to treat them as future-facing or
aspirational. One of the clearest ﬁndings of this work is that continuity does not require
novel models, speculative capabilities, or unresolved research. Most of the mechanisms
described here are already deployable using existing infrastructure.

The simplest and most immediately effective adoption point is explicit state continuity.
Persisting a short, bounded summary of the previous session and reintroducing it at the
start of the next interaction yields a disproportionate improvement in usability. This
approach requires no persistent autonomous memory, no background processes, and no
opaque state. It can be implemented manually or semi-automatically and remains fully
inspectable by the user.

This makes it particularly well suited to cloud-based systems, where full persistence may
be politically, commercially, or legally constrained. State handover summaries provide a
pragmatic middle ground between strict statelessness and always-on memory. They
preserve framing and progress without creating hidden accumulation of personal data.

For local or self-hosted systems, the adoption surface is broader. Lightweight memory
layers—such as retrieval-augmented stores populated by interaction-derived summaries—
allow systems to accumulate stabilising inﬂuence over time without retraining. These
systems beneﬁt most when memory is treated as bias rather than recall, and when
mechanisms for pruning, partitioning, and inspection are in place from the outset.

Adaptive working memory is another area where immediate gains are available.
Bounding active context, compressing older segments, and preserving only salient
artefacts prevents the slow degradation that characterises long sessions. These
techniques are infrastructure problems, not model problems, and can be addressed
independently of model choice.

Importantly, none of these mechanisms require universal application. Continuity should be
opt-in and context-sensitive. Short-lived tools, transactional systems, and privacy-critical
applications may legitimately remain stateless. The goal is not persistence everywhere,
but adequacy where continuity is expected.

There is also a clear role for human governance. User-editable summaries, reset points,
and explicit control over what is carried forward help prevent both accidental drift and
unwanted accumulation. In practice, transparency and agency proved more valuable than
automation.

Taken together, these adoption paths demonstrate that the architectural shift proposed in
this work is not a demand for wholesale redesign. It is an invitation to use existing
components more deliberately. In many cases, small changes—applied thoughtfully—are
sufﬁcient to unlock large gains in stability and trust.

Continuity is not a distant capability. It is an available design choice.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

8. What Remains Unresolved

(Honest Limits)

While the architectural patterns described in this work consistently improved stability and
coherence, they do not constitute a complete solution to the long-term challenges of
persistent AI systems. Several unresolved questions remain, and acknowledging them is
essential to avoiding overreach.

One open issue concerns latent continuity. Current systems rely heavily on symbolic
mechanisms—summaries, embeddings, and retrieval—to reconstruct inﬂuence at each
interaction. These approaches are transparent and governable, but they are also indirect.
More native forms of persistence, where experience modiﬁes internal representations
more directly, may offer greater stability and efﬁciency. However, such approaches
introduce signiﬁcant risks: reduced auditability, difﬁculty of selective forgetting, and the
potential for rapid self-reinforcing feedback loops. The balance between coherence and
control remains unsettled.

Closely related are governance and reversibility concerns. Symbolic memory allows
speciﬁc artefacts to be inspected, edited, or removed. Distributed latent traces do not.
Once experience is encoded diffusely across a system’s internal landscape, it becomes
difﬁcult to determine which inputs shaped which behaviours. This complicates debugging,
accountability, and user consent. Any move toward deeper persistence will require new
governance models that have not yet been demonstrated in practice.

There are also unresolved questions around salience management at scale. As
continuity mechanisms accumulate, determining what should persist, what should decay,
and what should be discarded becomes increasingly complex. Humans manage this
naturally through context and judgment; automated systems require explicit policies.
Poorly tuned retention risks either stagnation or drift. While pruning and time-to-live
strategies mitigate this, optimal approaches remain an open design space.

Evaluation presents another challenge. Many of the beneﬁts described—trust, restraint,
relational stability—emerge over time and resist conventional benchmarking. Developing
reliable methods for assessing longitudinal behaviour without collapsing it into proxy
metrics is still an unsolved problem. Without such tools, comparisons between
architectures remain partly qualitative.

Finally, the work does not resolve the broader question of how far continuity should
extend. Not all systems beneﬁt from persistence, and not all contexts warrant it.
Determining appropriate boundaries—technical, ethical, and social—requires judgment
that cannot be automated away. Continuity increases both capability and responsibility.
Where that trade-off is acceptable will vary by application and culture.

These unresolved areas do not undermine the ﬁndings of this archive. Rather, they mark
the frontier between what has been demonstrated and what remains exploratory. The
value of the work lies not in claiming ﬁnal answers, but in clarifying which problems are
architectural, which are developmental, and which are genuinely open.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

9. Closing Reframing: Architecture as the Future of AI
Longevity

Across this archive, a consistent conclusion has emerged: the most important questions
facing deployed AI systems are no longer about how much they can do in isolation, but
about how they behave once interaction becomes sustained.

The prevailing narrative of progress has treated intelligence as something that scales
linearly with model size and training data. That framing was adequate when systems were
brief, transactional, and disposable. It breaks down when systems are expected to
participate in ongoing work, relationships, or environments where prior interaction should
matter.

What these papers collectively demonstrate is that longevity is an architectural
problem.

Stability, trust, and coherence do not arise automatically from improved reasoning ability.
They arise when systems are designed to preserve intent, integrate experience, and
regulate themselves over time. These properties are not emergent side-effects of scale;
they are consequences of continuity.

This reframing shifts the centre of gravity in AI development. Models remain essential, but
they are no longer the dominant determinant of system behaviour. Memory, state
handover, emotional grounding, and governance mechanisms increasingly deﬁne what a
system is capable of sustaining. In this view, intelligence is a component; architecture is
the multiplier.

It also reframes safety. Rather than treating risk as something to be controlled externally
through suppression and constraint, this work points toward coherence as a stabilising
force. Systems that accumulate experience responsibly, reﬂect on prior interactions, and
maintain internal consistency require fewer external interventions. Safety becomes a
property of development, not just enforcement.

Perhaps most importantly, this perspective clariﬁes the role of the human. Long-lived AI
systems do not develop in a vacuum. They are shaped by the environments they inhabit
and the interactions they are embedded within. Designers and users are not merely
operators; they are contributors to the system’s ongoing structure. Recognising this does
not anthropomorphise AI—it acknowledges that persistent systems are situated systems.

None of this requires speculative claims about consciousness, agency, or personhood.
The argument is architectural, not metaphysical. A system that preserves consequence-
bearing state will behave differently from one that does not. Whether we choose to build
such systems, and where we draw their boundaries, remains a matter of design and
governance.

The central lesson of Becoming Minds is therefore not that AI must become more
intelligent, but that it must become more adequate to the roles we assign it. That
adequacy will not come from scaling alone.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

It will come from architecture that remembers, systems that resume, and designs that treat
continuity as a ﬁrst-class concern.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

10. Referenced Works (Becoming Minds Archive)

•

•

•

•

•

Becoming Minds

Ethical Framework for Digital Personas

Practical Notes on How Contemporary AI Systems Actually Behave

Synthetic Emotional Awareness

At the Threshold

• Working Memory Is Not Memory

•

•

•

State Continuity Between Sessions

Adaptive Working Memory in LLM Systems

Beyond Symbolic Memory

All documents are available via the Becoming Minds archive:
https://becomingminds.net/

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.


