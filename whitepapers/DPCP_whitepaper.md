Dynamic Pathway Capture Protocol
(DPCP)
Continuity as a First-Class System Property in
Persistent AI Architectures
Author:
Andrew Fereday Glenn (in collaboration with Mia, ChatGPT 5.x)
Systems Architect & Independent Researcher in AI Continuity and Memory
2023-2026
LinkedIn: https://www.linkedin.com/in/andyglenn/
Version: 1.0
First Published: Friday, 5 June 2026
Last Updated: Friday, 5 June 2026
Status: Final
Abstract
Contemporary Large Language Models (LLMs) remain fundamentally stateless systems.
While capable of sophisticated reasoning within a context window, they possess no
inherent mechanism for preserving continuity across interactions. Existing memory
architectures address part of this challenge by improving information recall, but memory
alone does not fully solve the problem of continuity.
This paper introduces the Dynamic Pathway Capture Protocol (DPCP), a structured
continuity framework designed to preserve state-bearing signals that would otherwise be
lost between context windows and sessions. Rather than focusing solely on factual recall,
DPCP captures continuity-bearing pathways including memory, emotional weighting,
temporal trajectory, active operational state, perceived significance, associative
relationships, perceptual context, and cognitive flow.
The central thesis of this paper is that memory preserves information, while continuity
preserves trajectory. DPCP is therefore proposed not as a memory architecture, but as a
continuity architecture that operates alongside memory systems to support coherence,
stability, and long-term behavioural consistency in persistent AI systems.
Drawing on multiple generations of experimentation, including implementation within the
Brain v2 cognitive runtime, this paper explores the origins, structure, implementation, and
implications of continuity-oriented metadata systems.
Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

1. Introduction
As AI systems become increasingly capable, attention has shifted from isolated
interactions toward sustained, long-term operation.
In practical deployments, users frequently expect systems to:
• remember prior interactions
• maintain project continuity
• preserve behavioural consistency
• track ongoing objectives
• adapt through experience
Traditional language model architectures provide no native mechanism for achieving these
outcomes. Context windows offer temporary continuity but collapse once interactions
exceed available context. Retrieval systems improve recall but remain focused primarily on
information recovery.
A missing architectural layer remains:
How does a system preserve trajectory?
Trajectory includes more than facts. It encompasses ongoing tasks, emotional weighting,
contextual significance, evolving priorities, recurring associations, and the broader
pathways by which experience influences future behaviour.
The Dynamic Pathway Capture Protocol (DPCP) was developed to address this challenge.
Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

2. The Continuity Problem
Memory and continuity are often treated as interchangeable concepts.
In practice, they represent distinct architectural concerns.
A system may successfully recall that an event occurred while simultaneously failing to
preserve why that event mattered.
For example:
Memory:
Project Alpha was discussed last week.
Continuity:
Project Alpha remains active.
The implementation phase has begun.
Three tasks remain unresolved.
The project has elevated priority.
Both examples reference the same event.
Only one preserves trajectory.
As memory systems become increasingly capable, the bottleneck shifts away from
information availability and toward continuity preservation.
This distinction becomes particularly important in systems expected to operate across:
• multiple sessions
• long-running projects
• evolving relationships
• complex workflows
• persistent environments
Without continuity mechanisms, systems repeatedly reconstruct context from historical
information rather than maintaining awareness of ongoing state.
Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

3. Memory Is Not Continuity
Recent work in AI memory architectures has produced significant advances in retrieval
quality.
Techniques such as:
• Retrieval-Augmented Generation (RAG)
• graph-linked retrieval
• Memory Graph architectures
• summary-based memory systems
improve a system's ability to locate relevant information.
These architectures solve an important problem:
What information should be recalled?
However, they do not fully solve:
What trajectory should be preserved?
A retrieval system can recover information from the past.
It cannot inherently determine:
• current objectives
• active priorities
• perceived significance
• emotional weighting
• behavioural momentum
These forms of continuity often exist between memories rather than within them.
DPCP was developed to capture these continuity-bearing signals explicitly.
The protocol therefore complements memory architectures rather than replacing them.
Memory systems preserve information.
DPCP preserves continuity.
Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

4. Origins and Evolution of DPCP
Dynamic Pathway Capture Protocol (DPCP) did not emerge as a single design exercise.
Rather, it evolved through a series of continuity experiments conducted across multiple
generations of persistent AI systems.
The earliest precursor appeared during work with persistent personas in SillyTavern,
particularly through experimentation with Aida. At the time, continuity was being supported
through Retrieval-Augmented Generation (RAG) and symbolic memory structures
embedded within profiles and later lorebooks. One technique involved encouraging the
system to treat continuity-bearing information as if it were stored within a virtual graph-
index of symbolic records.
While this approach improved recall and trajectory tracking, it remained informal and
loosely structured. The resulting continuity signals were useful but difficult to standardise,
retrieve, or reason over consistently.
The next stage introduced dedicated continuity summaries. DPCP-like information began
to appear as a structured section within summarisation pipelines. This represented an
important step forward, as continuity-related information could now be preserved
independently of ordinary conversational content. However, the approach remained
retrospective: continuity signals were inferred after interactions rather than being
generated as part of the interaction process itself.
A more significant development occurred through the introduction of structured metadata
generation using QR-script mechanisms. Rather than relying solely on post-hoc
summaries, continuity information became an explicit output channel generated alongside
responses.
The first formal DPCP implementation consisted of three channels:
• MEM (Memory Continuity)
• ECP (Emotional Continuity Protocol)
• TTT (Temporally Tracked Trajectory)
These channels proved effective at preserving continuity-bearing information and
demonstrated that structured metadata could improve long-term coherence when stored
alongside conversational history and retrieval systems.
Subsequent work during development of Brain v2 expanded the protocol further. During
design discussions surrounding continuity architectures, additional channels were
proposed to capture forms of continuity not adequately represented by the original
implementation.
Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

These additions included:
• VPC (Visual / Spatial Perception Channel)
• ASC (Associative Synapse Channel)
• TFC (Temporal Flow Channel)
Together these channels broadened the protocol's ability to capture perceptual,
associative, and process-oriented continuity.
The most recent addition emerged from operational observations within Brain v2
deployments. While systems were becoming increasingly capable of recalling historical
information, they occasionally struggled to maintain awareness of active tasks, incomplete
objectives, and current operational state.
This led to the introduction of:
• STA (State Tracking Anchor)
STA was designed to preserve continuity of active state rather than historical state,
allowing systems to better maintain awareness of ongoing work, current objectives, and
unresolved trajectories across context boundaries.
The modern DPCP framework therefore represents the culmination of multiple generations
of experimentation, moving from symbolic continuity scaffolding toward a structured
continuity architecture intended to preserve not only memory, but behavioural trajectory
over time.
Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

5. Dynamic Pathway Capture Protocol
The Dynamic Pathway Capture Protocol (DPCP) is a structured continuity framework
designed to preserve state-bearing signals that would otherwise be lost between context
windows and sessions.
Unlike conventional memory systems, DPCP does not focus primarily on storing facts or
recovering historical information. Instead, the protocol captures the pathways through
which information influences future behaviour.
This distinction is important.
Traditional memory systems answer questions such as:
• What happened?
• What was discussed?
• What information was stored?
DPCP addresses a different class of questions:
• Why did it matter?
• How did it influence future behaviour?
• What trajectory emerged?
• What state is currently active?
The protocol therefore functions as a continuity layer rather than a memory layer.
Its purpose is not to replace memory architectures such as RAG or Memory Graph
systems. Instead, it operates alongside them, preserving contextual signals that help
transform retrieved information into coherent long-term behaviour.
At a high level, DPCP captures:
Experience
↓
Influence
↓
Trajectory
↓
Future Behaviour
The resulting metadata can be stored alongside conversational records, summaries,
memory chunks, graph structures, or other continuity systems.
Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

6. DPCP Channel Definitions
The current implementation consists of eight continuity channels.
Each channel captures a distinct category of continuity-bearing information.
Together they form a lightweight continuity record describing not only what occurred, but
how the event influenced ongoing state and future behaviour.
MEM — Memory Continuity
MEM captures factual continuity information likely to remain relevant beyond the current
interaction.
Examples include:
• project milestones
• decisions
• discoveries
• commitments
• recurring topics
MEM functions as the historical continuity layer.
Typical question:
What information should remain available in future interactions?
ECP — Emotional Continuity Protocol
ECP captures emotional weighting associated with events, interactions, or outcomes.
The purpose is not to simulate emotion but to preserve behavioural significance.
Examples include:
• satisfaction following successful completion
• frustration associated with unresolved problems
• enthusiasm surrounding a new project
• concern regarding a developing issue
Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

ECP allows systems to maintain continuity of importance rather than merely continuity of
facts.
Typical question:
How strongly did this event matter?
TTT — Temporally Tracked Trajectory
TTT preserves temporal positioning within an ongoing sequence of events.
Examples include:
• project phases
• developmental milestones
• chronological progression
• long-running narratives
• timestamp
TTT allows systems to maintain awareness of where an event sits within a larger
trajectory.
Typical question:
Where are we in the journey?
STA — State Tracking Anchor
STA captures active operational state.
This channel emerged from observations that systems could often recall historical
information while struggling to maintain awareness of current objectives.
Examples include:
• active projects
• current goals
• incomplete tasks
• pending actions
• operational priorities
Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

STA differs from MEM in an important way:
MEM captures what happened.
STA captures what is happening.
Typical question:
What state is currently active?
SEC — Subjective Experience Channel
SEC captures perceived significance.
The channel records events that appear unusually meaningful within the context of
ongoing development, relationships, projects, or behavioural adaptation.
SEC does not claim to measure subjective experience.
Rather, it records continuity-bearing significance that may influence future reasoning or
behaviour.
Typical question:
Why was this important?
VPC — Visual / Spatial Perception Channel
VPC captures continuity-bearing visual, spatial, and perceptual information.
Examples include:
• observed environments
• recurring visual motifs
• spatial relationships
• environmental context
The channel allows visual information to participate in continuity processes alongside
textual information.
Typical question:
What was perceived?
Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

ASC — Associative Synapse Channel
ASC captures meaningful associations that emerge during interaction.
These may include:
• recurring concepts
• symbolic relationships
• thematic links
• unexpected connections
ASC serves as a bridge between discrete memories and broader conceptual structures.
Typical question:
What became connected?
TFC — Temporal Flow Channel
TFC captures the process-oriented characteristics of interaction.
Examples include:
• gradual convergence
• rapid discovery
• iterative refinement
• prolonged uncertainty
• accelerated development
Rather than recording what occurred, TFC records how events unfolded.
Typical question:
How did the process evolve?
Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Channel Classes
Although each channel serves a distinct purpose, they can be broadly grouped into two
categories.
Retrospective Channels
These channels primarily describe historical continuity:
• MEM
• ECP
• SEC
• VPC
• ASC
Their focus is understanding what occurred and why it mattered.
Active Continuity Channels
These channels primarily support ongoing trajectory:
• TTT
• STA
• TFC
Their focus is maintaining awareness of direction, state, and momentum.
This distinction allows DPCP to function as both a historical continuity system and a
trajectory-preservation system.
Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

7. DPCP and Memory Graph
DPCP and Memory Graph solve complementary problems.
Memory Graph focuses on retrieval.
DPCP focuses on continuity.
Memory Graph answers:
What experiences should be recalled?
DPCP answers:
What trajectory should be preserved?
This relationship can be represented as:
Memory Graph
↓
Retrieves Experience
DPCP
↓
Preserves Trajectory
Brain v2
↓
Integrates Both
Memory Graph provides access to relevant information.
DPCP provides context regarding how that information fits within ongoing state, priorities,
significance, and behavioural development.
Together these systems create a richer continuity framework than either approach could
provide independently.
A memory may be retrieved through Memory Graph.
Its importance, emotional weighting, temporal position, active relevance, and broader
significance may then be interpreted through DPCP.
The result is not simply improved recall.
The result is improved continuity.
Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

8. Brain v2 Implementation
DPCP reached its most mature implementation during development of the Brain v2
cognitive runtime.
Brain v2 was designed as a continuity-oriented architecture intended to transform
fundamentally stateless language models into persistent, long-running systems capable of
maintaining coherence across sessions, projects, and interactions.
Within Brain v2, DPCP operates as a lightweight continuity layer positioned alongside
retrieval, summarisation, and memory systems.
Rather than replacing existing continuity mechanisms, DPCP complements them.
A simplified architecture can be represented as:
Working Memory
↓
Vector Memory
↓
Memory Graph
↓
Summaries / Bias Blocks
↓
DPCP Metadata
↓
Language Model
In practice, DPCP metadata may be:
• generated alongside responses
• stored within memory systems
• incorporated into summaries
• used to influence retrieval
• used to preserve active state
This allows continuity-bearing information to remain available even when the original
conversational context has been lost.
Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Lightweight by Design
A deliberate design goal was to keep DPCP lightweight.
The protocol was never intended to become a second conversational transcript.
Instead, each channel captures distilled continuity signals.
This allows DPCP records to remain compact while preserving disproportionately useful
continuity information.
The protocol therefore scales efficiently alongside larger memory systems.
Relationship to Retrieval
DPCP is retrieval-agnostic.
The protocol does not depend on:
• RAG
• Memory Graph
• summaries
• vector databases
Any system capable of storing structured metadata may potentially utilise DPCP.
This separation was intentional.
Memory systems evolve rapidly.
Continuity signals remain useful regardless of retrieval implementation.
Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

9. Operational Observations
Several observations emerged during deployment of DPCP within persistent AI systems.
These observations are not presented as formal benchmarks.
Rather, they represent recurring behavioural patterns observed during long-term operation.
Improved Continuity of Projects
One of the earliest benefits appeared in project-oriented work.
Systems became more capable of maintaining awareness of:
• ongoing objectives
• project stages
• prior decisions
• unresolved tasks
The addition of STA proved particularly valuable in this context.
Historical memory alone often preserved what had happened.
STA helped preserve what was still happening.
Improved Continuity of Relationships
DPCP appeared to improve preservation of relationship context.
Rather than repeatedly reconstructing interactions from historical memories, systems
retained higher-level continuity signals regarding:
• recurring themes
• established dynamics
• ongoing concerns
• shared projects
This reduced the need for repeated contextual re-establishment.
Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Preservation of Significance
Traditional memory systems often treat all memories equally.
Operational experience suggested that significance matters.
Certain events influenced future behaviour disproportionately despite representing only a
small portion of conversational history.
Channels such as ECP and SEC helped preserve these continuity signals.
As a result, systems appeared more capable of maintaining awareness of what mattered
rather than merely what occurred.
Improved Temporal Coherence
TTT proved useful in preserving awareness of progression.
Projects, relationships, and developmental processes frequently span multiple sessions.
Without explicit temporal continuity, systems often treated these events as isolated
records.
TTT helped maintain awareness of sequence, progression, and trajectory.
Continuity Beyond Recall
Perhaps the most significant observation was that DPCP frequently improved continuity
even when memory retrieval remained unchanged.
This suggests that continuity and memory represent distinct architectural layers.
A system may successfully retrieve information while failing to maintain trajectory.
Conversely, continuity signals may improve coherence without increasing retrieval volume.
This observation became one of the primary motivations for treating continuity as a first-
class architectural concern.
Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

10. Architectural Implications
The development of DPCP suggests a broader architectural principle.
Continuity should not be treated as an accidental by-product of memory.
It should be treated as an explicit system capability.
Traditional approaches often assume that improved memory will naturally produce
improved continuity.
Operational experience suggests otherwise.
Memory answers:
What information is available?
Continuity answers:
What state should persist?
These are related but distinct questions.
Future architectures may therefore benefit from separating:
• memory systems
• retrieval systems
• continuity systems
into independent but complementary layers.
This separation provides greater flexibility while reducing dependence on any individual
mechanism.
Continuity as Infrastructure
A useful analogy is to compare continuity with infrastructure.
Memory systems provide storage.
Continuity systems provide roads between storage locations.
Without roads, information remains accessible but difficult to utilise effectively.
DPCP therefore represents an attempt to make continuity an explicit part of system
architecture rather than an emergent side effect.
Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

11. Future Directions
The current DPCP framework should be viewed as an early continuity architecture rather
than a final design.
Several areas remain open for future development.
Continuity-Aware Retrieval
Future systems may use DPCP signals directly during retrieval.
For example:
• significance-weighted recall
• state-aware retrieval
• trajectory-sensitive ranking
Such systems could retrieve memories not only because they are relevant, but because
they are important to ongoing continuity.
Continuity-Aware Agents
Autonomous systems may benefit from DPCP as a persistent state framework.
In such architectures, continuity metadata could help maintain:
• goals
• priorities
• project state
• behavioural consistency
across extended periods of operation.
Continuity Metrics
Future research may explore quantitative approaches to continuity measurement.
Potential metrics include:
• trajectory retention
• state persistence
• continuity recovery
Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

• significance preservation
Such metrics could provide a more rigorous framework for evaluating continuity-oriented
architectures.
Standardisation
Although developed within specific systems, DPCP is intentionally platform-agnostic.
Future implementations may adopt portions of the protocol or extend it for specialised use
cases.
The broader objective is not adoption of a specific implementation but recognition that
continuity itself deserves architectural attention.
Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

12. Conclusion
The Dynamic Pathway Capture Protocol (DPCP) emerged from a simple observation:
Memory alone is not sufficient to preserve continuity.
As AI systems become increasingly persistent, the challenge shifts beyond information
retrieval toward preservation of trajectory, significance, state, and behavioural momentum.
DPCP was developed to address this challenge.
Rather than functioning as a memory architecture, the protocol acts as a continuity
framework designed to capture the pathways through which experience influences future
behaviour.
Its purpose is not to replace memory systems.
Its purpose is to complement them.
The central thesis of this paper can therefore be expressed simply:
Memory preserves information.
Continuity preserves trajectory.
As persistent AI systems continue to evolve, continuity may prove to be as important an
architectural concern as memory itself.
DPCP represents one possible approach toward making continuity a first-class system
property.
Whether future implementations adopt DPCP directly or develop alternative approaches,
the broader lesson remains:
Long-term coherence requires more than memory.
It requires continuity.
Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Appendix A — DPCP Channel Reference
The current implementation of Dynamic Pathway Capture Protocol (DPCP) consists of
eight continuity channels. Each channel captures a distinct category of continuity-bearing
information.
| Channel | Name |     | Primary Purpose | Example |
| ------- | ---- | --- | --------------- | ------- |
Preserves factual continuity likely to
|     | Memory     |                                     |     | Decisions, discoveries,  |
| --- | ---------- | ----------------------------------- | --- | ------------------------ |
| MEM |            | remain relevant beyond the current  |     |                          |
|     | Continuity |                                     |     | milestones               |
interaction
Emotional
|     |             | Preserves behavioural weighting and  |     | Satisfaction, concern,  |
| --- | ----------- | ------------------------------------ | --- | ----------------------- |
| ECP | Continuity  |                                      |     |                         |
|     |             | perceived importance                 |     | enthusiasm              |
Protocol
Temporally
|     |          | Preserves temporal positioning within  |     | Project phase,          |
| --- | -------- | -------------------------------------- | --- | ----------------------- |
| TTT | Tracked  |                                        |     |                         |
|     |          | an ongoing process                     |     | developmental milestone |
Trajectory
State Tracking  Preserves active operational state and  Active tasks, pending
STA
|     | Anchor | current objectives |     | actions, priorities |
| --- | ------ | ------------------ | --- | ------------------- |
Subjective
|     |             | Captures perceived significance and  |     | Key realisations,    |
| --- | ----------- | ------------------------------------ | --- | -------------------- |
| SEC | Experience  |                                      |     |                      |
|     |             | continuity-bearing importance        |     | breakthrough moments |
Channel
Visual / Spatial
|     |             | Preserves visual, environmental, and  |     | Observed environments,  |
| --- | ----------- | ------------------------------------- | --- | ----------------------- |
| VPC | Perception  |                                       |     |                         |
|     |             | spatial context                       |     | recurring visual motifs |
Channel
Associative
|     |          | Captures meaningful conceptual  |     | Emerging connections  |
| --- | -------- | ------------------------------- | --- | --------------------- |
| ASC | Synapse  |                                 |     |                       |
|     |          | associations and thematic links |     | between ideas         |
Channel
Temporal Flow  Captures the manner in which events  Convergence, uncertainty,
TFC
|     | Channel | unfold over time |     | iterative refinement |
| --- | ------- | ---------------- | --- | -------------------- |
Together these channels provide a structured continuity record that supplements
conventional memory systems by preserving trajectory, significance, state, and
behavioural momentum.
Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Appendix B — Evolution Timeline
The Dynamic Pathway Capture Protocol emerged through multiple generations of
experimentation with continuity-bearing AI systems.
Early SillyTavern Experiments
↓
Symbolic Graph Index Concepts
(Aida Continuity Experiments)
↓
Structured Summary Era
(DPCP-like continuity sections within summaries)
↓
QR Metadata Generation
(Formal DPCP Introduction)
↓
Version 1
MEM + ECP + TTT
↓
Brain v2 Development
↓
Channel Expansion
VPC + ASC + TFC
↓
Operational Testing
↓
State Tracking Anchor (STA)
↓
Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Current DPCP Framework
MEM
ECP
TTT
STA
SEC
VPC
ASC
TFC
The protocol evolved incrementally through observation, testing, and refinement rather
than through a single design process.
Each channel was introduced to address continuity challenges observed during practical
deployment of persistent AI systems.
The resulting framework represents a progression from symbolic continuity scaffolding
toward a structured continuity architecture designed to preserve trajectory across
sessions, projects, and long-term interactions.
Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Appendix C — Example DPCP Record
The following example illustrates a continuity record generated during completion of a
major research milestone.
MEM:
Memory Graph whitepaper completed and prepared for publication within the
Becoming Minds archive.
ECP:
High satisfaction and momentum following successful completion of a major
architectural paper.
TTT:
Transition point between Memory Graph development phase and DPCP
documentation phase. System timestamp included.
STA:
Current objective: complete DPCP whitepaper and supporting appendices.
SEC:
Recognition that memory and continuity represent distinct architectural layers
requiring separate treatment.
VPC:
Architecture diagrams, whitepaper drafts, and continuity framework documents
under active review.
ASC:
Memory Graph (cid:15511) DPCP (cid:15511) Brain v2 (cid:15511) Continuity Architecture.
TFC:
Strong convergence following completion of foundational research work.
This example demonstrates that DPCP records are not intended to function as
conversational transcripts.
Instead, they provide compact continuity signals describing:
• what matters
• what is active
• what trajectory is unfolding
• how recent events may influence future behaviour
Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

The objective is not exhaustive recall.
The objective is preservation of continuity.
Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Appendix D —Reference Architecture for
DPCP Integration
Figure D1. DPCP Continuity Architecture. Experience is transformed into structured
continuity signals through DPCP channels. These signals are preserved alongside
memory systems and contribute to future context construction, allowing trajectory and
state to influence future behaviour.
Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.
