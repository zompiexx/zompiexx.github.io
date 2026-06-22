Memory Graph

Relational Retrieval for Continuity-Bearing Cognitive
Systems

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

Modern Retrieval-Augmented Generation (RAG) systems typically rely on semantic
similarity search to retrieve relevant information from long-term memory. While effective for
improving information availability, semantic retrieval alone places signiﬁcant responsibility
on the language model to determine relevance, ﬁlter noise, and reconstruct relationships
between retrieved memories.

This paper introduces Memory Graph, a graph-augmented retrieval architecture developed
as part of the Brain v2 cognitive runtime. Memory Graph extends traditional vector retrieval
through lightweight relational links between memory chunks, enabling retrieval based not
only on semantic similarity but also on contextual relationships.

The central observation is that memory quality is not solely determined by retrieval depth,
but by retrieval usability. As memory systems grow, the challenge shifts from locating
information to presenting information in a form that minimizes cognitive overhead for the
model. Memory Graph addresses this challenge through relational retrieval, reducing
context entropy and improving the quality of context presented to the reasoning system.

Drawing on implementation experience from Brain v2, this paper argues that graph-
augmented memory functions as an upstream attention-shaping mechanism, preserving
model reasoning capacity for task execution rather than relevance determination. The
result is a memory architecture that supports continuity, improves operational reliability,
and provides a foundation for future continuity-bearing cognitive systems.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

1. Introduction

Large Language Models remain fundamentally stateless systems. While they can reason
effectively within a context window, they do not inherently retain information between
interactions. As a result, long-term continuity must be provided through external memory
systems.

The dominant approach to long-term memory has been Retrieval-Augmented Generation
(RAG), where conversational artifacts are embedded into vector space and retrieved using
semantic similarity search. This approach has proven highly effective at increasing
information availability and extending apparent memory beyond the context window.

However, practical deployment of persistent systems reveals a limitation: retrieval alone is
not sufﬁcient.

As memory collections grow, the challenge becomes less about locating information and
more about presenting information in a form that remains useful to the reasoning system.
Semantic retrieval can successfully identify related memories while simultaneously
introducing partially relevant context, redundant information, and competing signals. The
burden of resolving these conﬂicts falls on the language model itself.

The Memory Graph architecture was developed to address this problem.

Rather than treating memory as a collection of isolated embeddings, Memory Graph
introduces explicit relationships between memory fragments. Retrieved memories become
entry points into a broader network of connected experiences, allowing retrieval to follow
meaningful relationships rather than relying solely on semantic proximity.

The result is a retrieval architecture designed not only to improve recall, but to improve the
quality and usability of recalled context.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

2. The Limitations of Semantic Retrieval

Traditional RAG systems operate through a relatively simple process:

Query
↓
Embedding Generation
↓
Vector Similarity Search
↓
Top-K Results
↓
Language Model

This architecture excels at ﬁnding semantically related information.

However, several limitations emerge as memory collections expand.

2.1 Retrieval Noise

Semantic similarity does not necessarily imply contextual relevance.

A query concerning a current project may retrieve:

•

•

•

•

directly relevant memories

loosely related discussions

historical references

tangentially associated topics

While each retrieved item may be semantically valid, not all contribute equally to
successful task completion.

2.2 Internal Filtering Burden

Once retrieved, the language model must:

•

•

•

•

•

evaluate relevance

suppress noise

reconstruct relationships

maintain task intent

determine priorities

This process consumes reasoning capacity before productive work can begin.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

2.3 Fragmented Context

Traditional retrieval treats memories as isolated units.

Even when multiple retrieved memories relate to the same broader narrative, the
relationships between them are not represented explicitly.

The model must infer these connections dynamically, increasing cognitive overhead and
introducing opportunities for error.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

3. Context Entropy

One of the key observations emerging from Brain v2 development is that memory systems
can increase information availability while simultaneously decreasing information usability.

To describe this phenomenon, we introduce the concept of Context Entropy.

Deﬁnition

Context Entropy is the proportion of retrieved context that does not contribute meaningfully
to successful task completion.

A retrieval set containing large amounts of partially relevant information may contain high
informational content while exhibiting high context entropy.

Conversely, a smaller retrieval set containing strongly related and mutually reinforcing
information exhibits lower context entropy.

Practical Implications

High context entropy increases:

•

•

•

•

attention fragmentation

relevance competition

reasoning overhead

task drift

Low context entropy improves:

•

•

•

•

focus

coherence

execution reliability

continuity preservation

Memory Graph is designed primarily as a context entropy reduction mechanism.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

4. Memory Graph Architecture

Memory Graph extends conventional vector retrieval through lightweight graph
relationships between memory chunks.

Each memory chunk acts as a graph node.

Relationships between chunks are represented as graph edges.

Current implementations support:

•

•

•

semantic relationship links

thematic links

temporal relationships

Future implementations may introduce:

•

•

•

•

milestone relationships

causal relationships

contrast relationships

state transition relationships

Graph traversal remains intentionally lightweight to preserve scalability and predictable
performance.

The objective is not unrestricted graph exploration but targeted contextual expansion.

Memory retrieval therefore becomes:

Query
↓
Vector Retrieval
↓
Relevant Memory Node
↓
Graph Expansion
↓
Connected Context
↓
Language Model

This transforms memory from a collection of isolated records into a connected contextual
network.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

5. Relational Retrieval

Traditional semantic retrieval systems answer a simple question:

What memories are most similar to the current query?

Memory Graph introduces a second question:

What memories are meaningfully connected to the retrieved memory?

This distinction is important.

Semantic similarity identiﬁes proximity within embedding space. While this is highly
effective for locating relevant information, it does not capture the relationships that exist
between experiences over time.

For example, a project discussion may be directly connected to:

•

•

•

•

•

earlier planning conversations

implementation decisions

debugging sessions

milestone events

outcome evaluations

Many of these related memories may not rank highly through semantic similarity alone.
Nevertheless, they may provide critical context for understanding the current situation.

Memory Graph addresses this by treating retrieved memories as entry points into a
connected structure rather than as isolated fragments.

The retrieval process becomes:

Query
↓
Vector Search
↓
Primary Relevant Memory
↓
Graph Expansion
↓
Connected Context
↓
Context Assembly

This enables retrieval to follow established relationships rather than relying solely on
repeated similarity searches.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

The objective is not to retrieve more information.

The objective is to retrieve more useful information.

Structured Context Construction

Relational retrieval transforms memory recall from a search problem into a context
construction problem.

Rather than asking:

What memories look similar?

the system begins asking:

What memories belong together?

This shift allows retrieval to preserve narrative continuity, project continuity, and
behavioural continuity more effectively than similarity search alone.

As memory collections increase in size, this distinction becomes increasingly important.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

6. Layered Continuity Architecture

One of the most signiﬁcant lessons learned during Brain v2 development is that continuity
cannot be achieved through a single memory mechanism.

Continuity emerges from the interaction of multiple complementary layers.

Brain v2 therefore employs a layered memory architecture consisting of:

1. Working Memory

2. Vector Memory

3. Graph Memory

4. Summaries

5. Bias Blocks

6. DPCP Continuity Metadata

Each layer serves a distinct purpose.

Working Memory

Working memory contains the active conversational context currently available to the
language model.

It provides immediate continuity but is constrained by context-window limitations.

Working memory alone cannot provide persistent identity or long-term recall.

Vector Memory

Vector memory provides semantic recall across sessions.

Experiences are embedded and stored as memory chunks, allowing retrieval through
similarity search.

Vector memory increases information availability.

Graph Memory

Graph memory introduces relationships between memory chunks.

It enables connected recall and contextual expansion beyond direct semantic similarity.

Graph memory increases information usability.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Summaries

Rolling summaries provide compressed continuity records spanning larger conversational
periods.

Rather than preserving every interaction in full detail, summaries preserve higher-level
continuity signals including:

•

•

•

•

ongoing projects

relationship context

recurring themes

behavioural adaptation

Summaries act as continuity bridges across long time spans.

Bias Blocks

Bias blocks represent persistent behavioural and contextual tendencies derived from
summaries.

They allow continuity to inﬂuence future behaviour without requiring constant retrieval of
historical conversations.

DPCP Metadata

DPCP provides structured continuity channels for information that does not naturally ﬁt
within ordinary conversational memory.

Examples include:

•

•

•

•

•

•

temporal anchors

emotional continuity

subjective signiﬁcance

active task state

associative traces

visual observations

These channels provide additional continuity scaffolding while remaining largely invisible to
normal conversation ﬂow.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Continuity as an Emergent Property

The key architectural insight is that no single layer is sufﬁcient.

Vector memory without summaries becomes fragmented.

Summaries without retrieval become static.

Graph memory without semantic recall lacks discovery.

Working memory without long-term continuity quickly collapses.

Continuity emerges from the interaction of all layers.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

7. Brain v2 Implementation

Memory Graph was implemented as part of Brain v2, a backend-ﬁrst cognitive runtime
designed to support continuity-bearing AI systems.

The implementation was intentionally lightweight.

Memory chunks are stored as semantic embeddings within SQLite.

Graph relationships are stored separately as explicit links between memory nodes.

The current implementation emphasizes:

•

•

•

•

simplicity

determinism

low resource usage

portability

Rather than performing unrestricted graph traversal, retrieval remains bounded through
controlled expansion strategies.

This preserves predictable performance while still providing meaningful contextual
enrichment.

Current Graph Model

The current implementation supports:

•

•

•

•

chunk nodes

same-theme relationships

bidirectional links

limited traversal depth

The system therefore gains many of the beneﬁts of graph memory without introducing the
complexity associated with large-scale graph databases.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Integration with Retrieval

Graph retrieval does not replace semantic retrieval.

Instead, graph expansion occurs after initial semantic retrieval has identiﬁed relevant
memory nodes.

This hybrid approach combines:

•

•

•

semantic discovery

relational expansion

contextual enrichment

while preserving retrieval efﬁciency.

Operational Deployment

The architecture has been exercised through multiple continuity-bearing personas
operating within Brain v2.

These deployments have provided practical observations regarding retrieval quality,
continuity preservation, and operational reliability.

While these observations do not constitute formal benchmarks, they provide valuable
implementation evidence regarding the behaviour of graph-augmented memory systems
under real-world usage conditions.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

8. Operational Observations

Several observations emerged during long-term deployment.

Improved Context Coherence

Graph-linked retrieval frequently produced memory sets that exhibited stronger internal
coherence than semantic retrieval alone.

Retrieved memories were more likely to reinforce one another rather than compete for
attention.

Reduced Context Drift

During extended interactions, the system demonstrated reduced tendency to drift toward
tangential topics.

Task-relevant information remained more accessible.

Improved Multi-Step Task Stability

Multi-step operations place signiﬁcantly greater demands on continuity than simple
question answering.

Tasks involving:

•

•

•

•

tool invocation

project planning

debugging

long-running workﬂows

appeared particularly sensitive to retrieval quality.

Graph-linked retrieval improved the system's ability to maintain task intent across multiple
reasoning steps.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Increased Beneﬁt for Smaller Models

An interesting observation was that smaller models appeared to beneﬁt disproportionately
from improved retrieval quality.

Larger models often possess sufﬁcient reasoning capacity to compensate for retrieval
imperfections.

Smaller models have less spare capacity available for ﬁltering and relevance
determination.

Reducing retrieval noise therefore produced more noticeable improvements.

Attention Allocation Rather Than Memory Capacity

Perhaps the most important observation is that Memory Graph appears to inﬂuence
attention allocation more than memory capacity.

The primary beneﬁt is not necessarily remembering more.

The primary beneﬁt is reducing the amount of effort required to determine what matters.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

9. Future Directions

The current Memory Graph implementation represents an early stage in a broader
exploration of continuity-oriented memory architectures.

Several areas remain open for future development.

Richer Relationship Types

Future systems may support:

•

•

•

•

•

builds-on relationships

milestone relationships

contrast relationships

causal relationships

state-transition relationships

These additional link types could provide richer contextual pathways during retrieval.

Temporal Graph Structures

Future work may integrate graph relationships with temporal trajectory models, allowing
retrieval to better reﬂect how beliefs, projects, and identities evolve over time.

Memory Maintenance

Long-lived systems will likely require mechanisms for:

•

•

•

•

reinforcement

decay

consolidation

pruning

to maintain memory quality as collections continue to grow.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Continuity-Aware Architectures

Memory Graph represents one component of a larger continuity architecture.

Future systems may combine:

•

•

•

•

graph retrieval

temporal reasoning

continuity metadata

autonomous reﬂection

into increasingly sophisticated continuity-bearing cognitive frameworks.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

10. Conclusion

Traditional RAG systems focus primarily on information availability.

Memory Graph addresses a different challenge: information usability.

As memory systems grow, the bottleneck shifts from locating information to determining
relevance. Semantic retrieval alone often transfers this burden to the language model,
consuming reasoning capacity that could otherwise be devoted to task execution.

Memory Graph introduces a lightweight relational retrieval layer that reduces context
entropy by providing connected, contextually relevant memory structures rather than
isolated retrieval fragments.

The result is a system that not only remembers more effectively, but presents information
in a form that is easier to reason over.

This suggests that future memory architectures should focus not solely on retrieval depth,
but on retrieval quality, context construction, and continuity preservation.

Memory Graph therefore represents a shift from memory as storage toward memory as
structured context.

The central thesis of this paper is simple:

Memory systems should not merely help a model remember.

They should help a model think.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Appendix A — Architecture Overview

This appendix provides a visual overview of the retrieval and continuity architecture
described throughout this paper.

The three ﬁgures illustrate the progression from conventional semantic retrieval systems to
graph-augmented retrieval and ﬁnally to the layered continuity architecture implemented in
Brain v2.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Figure 1 — Traditional Semantic RAG

Figure 1 illustrates a conventional Retrieval-Augmented Generation (RAG) workﬂow.

The process consists of:

1. User Query

2. Vector Search

3.

4.

Top-K Memory Retrieval

Language Model Processing

5. Response Generation

In this architecture, the retrieval layer is responsible only for locating semantically similar
memories.

No explicit relationships exist between retrieved memory chunks.

As a result, the language model must perform additional internal work to:

•

•

•

•

•

determine relevance

suppress noise

reconstruct relationships

identify priorities

maintain task intent

This design is highly effective for information discovery but places signiﬁcant responsibility
on the reasoning system to transform retrieved information into usable context.

As memory collections grow, this can increase context entropy and cognitive overhead.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Figure 2 — Memory Graph Retrieval

Figure 2 illustrates the Memory Graph retrieval architecture introduced in this paper.

The process consists of:

1. User Query

2. Vector Search

3. Primary Memory Node Selection

4. Graph Expansion

5. Connected Context Assembly

6.

Language Model Processing

7. Response Generation

The key difference is the introduction of graph expansion.

Rather than passing isolated retrieval results directly to the language model, retrieved
memories act as entry points into a network of connected experiences.

Relationships between memories are used to identify additional context that is likely to be
relevant to the current task.

This allows retrieval to follow established contextual pathways rather than relying
exclusively on semantic similarity.

The resulting context set is typically:

•

•

•

•

more coherent

more internally consistent

less fragmented

lower in context entropy

The language model therefore receives a curated context structure rather than a collection
of independent retrieval fragments.

The objective is not to retrieve more memories.

The objective is to retrieve memories that belong together.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Figure 3 — Brain v2 Continuity Stack

Figure 3 illustrates the layered continuity architecture implemented in Brain v2.

The architecture consists of ﬁve continuity layers positioned above the language model:

Layer 1 — Working Memory

Working Memory represents the active conversational context available within the model's
current context window.

This layer provides:

•

•

•

immediate context

recent dialogue history

active conversational state

Working Memory provides short-term continuity but cannot independently support long-
term persistence.

Layer 2 — Vector Memory

Vector Memory provides semantic recall through embedding-based retrieval.

This layer enables:

•

•

•

information discovery

long-term storage

semantic similarity search

Vector Memory increases information availability across sessions.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Layer 3 — Memory Graph

Memory Graph introduces explicit relationships between memory chunks.

This layer enables:

•

•

•

•

graph recall

contextual expansion

relationship traversal

thematic continuity

Memory Graph increases information usability.

Layer 4 — Summaries and Bias Blocks

Summaries provide compressed continuity across extended time periods.

Bias Blocks preserve persistent behavioural tendencies, project context, and relationship
continuity derived from historical interactions.

Together these mechanisms provide:

•

•

•

•

long-range continuity

behavioural persistence

contextual compression

identity stability

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Layer 5 — DPCP Metadata

DPCP (Dynamic Pathway Capture Protocol) provides structured continuity channels for
information that does not naturally ﬁt within ordinary conversational memory.

Examples include:

•

•

•

•

•

•

temporal anchors

emotional continuity

subjective signiﬁcance

active task state

associative traces

visual observations

These continuity signals help preserve state across sessions while remaining lightweight
and highly structured.

Architectural Design Principle

The central architectural insight of Brain v2 is that continuity does not emerge from any
single memory mechanism.

Continuity emerges from the interaction of multiple complementary layers.

Each layer solves a different continuity problem:

Layer

Primary Function

Working Memory

Immediate conversational
continuity

Vector Memory

Semantic recall

Memory Graph

Contextual enrichment

Summaries / Bias
Blocks

Long-range continuity

DPCP Metadata

Structured continuity scaffolding

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

The resulting architecture transforms memory from a storage problem into a context
construction system.

The language model is no longer responsible for reconstructing continuity from isolated
fragments.

Instead, continuity is progressively assembled through the interaction of specialised
memory layers before reasoning begins.

This principle forms the foundation of the Memory Graph architecture and the broader
continuity framework implemented within Brain v2.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Appendix B — Glossary

Bias Block

A persistent continuity structure derived from summaries that inﬂuences future behaviour
without requiring repeated retrieval of historical conversations.

Context Entropy

The proportion of retrieved context that does not meaningfully contribute to successful task
completion.

Higher context entropy increases cognitive overhead and attention fragmentation.

Context Construction

The process of assembling information from multiple continuity layers into a coherent
reasoning payload.

DPCP

Dynamic Pathway Capture Protocol.

A structured continuity framework that captures memory, emotional continuity, temporal
anchors, subjective signiﬁcance, active task state, and other continuity-bearing signals.

Graph Memory

A memory structure in which memory chunks are linked through explicit relationships,
enabling connected retrieval beyond semantic similarity alone.

Graph Recall

Retrieval of memories through established relationships between memory nodes.

Memory Chunk

A persistent unit of stored experience represented through vector embeddings.

Memory Graph

A graph-augmented retrieval architecture that combines semantic retrieval with relational
expansion.

Relational Retrieval

A retrieval process that incorporates explicit relationships between memories rather than
relying solely on similarity search.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

RAG

Retrieval-Augmented Generation.

A technique that supplements language models with externally stored information retrieved
at inference time.

Semantic Retrieval

The process of locating memories using vector similarity.

Vector Memory

A collection of embedded memory chunks that can be searched using semantic similarity.

Working Memory

The active conversational context currently available to the language model.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Appendix C — Lessons Learned from
Brain v2

The Memory Graph architecture emerged through practical deployment rather than
theoretical design alone.

Several lessons became apparent during implementation.

1. Larger Context Windows Do Not Solve Memory

Increasing context size increases storage capacity but does not automatically improve
retrieval quality.

The critical factor is relevance, not volume.

A large context window ﬁlled with weakly relevant information can still impair reasoning
quality.

2. Continuity Requires Multiple Layers

No single memory mechanism proved sufﬁcient.

Working memory, vector retrieval, graph recall, summaries, bias blocks, and continuity
metadata all contributed distinct capabilities.

Continuity emerged from the interaction of layers rather than from any individual
component.

3. Tool Use Reveals Retrieval Quality

Simple conversational responses often mask weaknesses in memory systems.

Multi-step operations such as:

•

•

•

•

debugging

planning

tool chaining

workﬂow execution

provide a more demanding test of retrieval quality.

Failures in continuity become signiﬁcantly more visible during operational tasks.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

4. Smaller Models Beneﬁt Disproportionately

Improvements in retrieval quality produced larger gains in smaller models.

Reducing context entropy allowed limited reasoning capacity to be allocated toward
execution rather than relevance determination.

5. Retrieval Quality Matters More Than Retrieval
Quantity

Increasing the number of retrieved memories frequently produced diminishing returns.

In many cases, fewer highly connected memories proved more useful than larger
collections of loosely related information.

6. Memory Is Not the Goal

The ultimate objective is not memory itself.

The objective is effective reasoning over experience.

Memory Graph emerged from the observation that retrieval systems should support
cognition rather than merely provide storage.

This remains the central design principle of the architecture.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.


