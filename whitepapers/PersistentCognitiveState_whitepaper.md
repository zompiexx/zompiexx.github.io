Persistent Cognitive State

Rethinking Continuity in Large Language Model
Systems

Author:
Andrew Fereday Glenn (in collaboration with Mia, ChatGPT 5.x)
Systems Architect & Independent Researcher in AI Continuity and Memory
2023-2026

LinkedIn: https://www.linkedin.com/in/andyglenn/

Version: 1.0
Published: Thursday, 2 July 2026
Status: Final

Abstract

Large Language Models (LLMs) have demonstrated extraordinary capability across
language, reasoning, software engineering and multimodal understanding. Their success
has largely been driven by increasingly capable transformer architectures trained on vast
quantities of data.

Despite these advances, contemporary LLM inference remains fundamentally stateless.
Each activation reconstructs cognitive state by repeatedly processing contextual
information that is often largely unchanged from previous interactions.

This paper argues that the principal architectural limitation of current persistent AI systems
is no longer the capability of the reasoning engine itself, but the repeated reconstruction of
cognitive state required by stateless inference.

Brain v2 is presented as a practical case study. It demonstrates that persistent cognition—
including long-term memory, continuity, evolving identity and accumulated understanding—
can already be achieved using contemporary stateless transformer models. However, this
capability is realised through repeated reconstruction of state via textual context, resulting
in signiﬁcant computational overhead.

We propose that future LLM architectures need not replace transformers or continually
retrain model weights. Instead, they may evolve by maintaining persistent cognitive state
natively, allowing inference to operate incrementally over change rather than repeatedly
reconstructing prior state.

The behavioural capability already exists.

The remaining challenge is architectural efﬁciency.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

1. Introduction

The transformer architecture has fundamentally changed artiﬁcial intelligence.

Large Language Models possess remarkable general capability, demonstrating
sophisticated reasoning across diverse domains without task-speciﬁc programming.

This success has naturally encouraged a focus on larger models, larger context windows
and increasingly sophisticated training methodologies.

However, practical experience developing persistent cognitive systems suggests that
another challenge has emerged.

The limitation is no longer simply how well a model reasons.

It is how often it must reconstruct itself before reasoning can begin.

Every interaction with a contemporary LLM begins by rebuilding the system's current
cognitive state.

Identity.

Conversation.

Memory.

Goals.

Relationships.

Current world state.

This reconstruction is repeated regardless of how little the underlying state has actually
changed.

The transformer itself is not inefﬁcient.

The repeated reconstruction of state is.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

2. Knowledge Versus Cognitive State

Pretrained model weights already contain an extraordinary amount of general knowledge.

They encode:

•

•

•

•

•

•

•

language

reasoning

mathematics

programming

scientiﬁc understanding

social conventions

general world knowledge

This represents the model's enduring cognitive substrate.

However, this substrate does not determine the model's current situation.

Questions such as:

• Who am I?

• Who is the current user?

• What happened yesterday?

• What project are we working on?

• What conclusions have already been reached?

• What has changed since the previous interaction?

cannot be answered from pretrained weights alone.

They belong to the system's evolving cognitive state.

The distinction is fundamental.

Model weights provide capability.

Cognitive state provides continuity.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

3. Stateless Inference

Current LLM systems typically operate using a stateless inference model.

Each interaction follows a familiar lifecycle:

Context

↓

Preﬁll

↓

Inference

↓

Output

↓

Context discarded
The next interaction repeats the same process.

Even if the system's state has changed only minimally, the majority of contextual
information must be reconstructed before new reasoning can occur.

This architecture has proven remarkably successful.

It is also computationally inefﬁcient.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

4. Brain v2 as a Behavioural Prototype

Brain v2 was developed to investigate persistent cognition using contemporary LLMs.

Rather than modifying pretrained model weights, Brain v2 maintains persistent cognitive
state externally through:

•

Identity

• Working Memory

•

•

•

•

•

•

Long-Term Memory

Memory Graph

Dynamic Pathway Capture Protocol (DPCP)

Temporal awareness

Current world state

Autonomous cognitive cycles

Importantly, the underlying transformer remains unchanged.

Learning occurs through accumulated experience rather than continual retraining.

The system demonstrates persistent behaviour despite operating on a fundamentally
stateless inference engine.

Brain v2 therefore functions as a behavioural prototype of persistent cognition.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

5. Capturing Understanding Rather Than
Conversation

One of the key observations during Brain v2 development was that preserving raw
conversation is less important than preserving the products of reasoning.

Following signiﬁcant interactions, Brain v2 captures:

•

•

•

•

•

conclusions

observations

inferred relationships

emotional interpretations

future relevance

These become persistent cognitive state through DPCP, Memory Graph and retrieval.

The system therefore accumulates understanding rather than merely accumulating
dialogue.

Subsequent reasoning builds upon previous conclusions instead of reconstructing them
from ﬁrst principles.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

6. The Movie Analogy

Consider watching a two-hour ﬁlm.

Immediately afterwards you can discuss:

•

•

•

•

the story

the characters

the themes

the emotional impact

Several days later someone asks:

"Why did the ending work?"

Human cognition does not replay the entire ﬁlm.

Nor does it replay a textual summary of every previous thought.

Instead it reﬂects upon an already-maintained understanding.

Brain v2 already behaves similarly.

A multimodal experience is processed once.

The resulting understanding is captured through DPCP and persistent memory.

Future reasoning operates upon that preserved understanding.

However, contemporary LLM architecture introduces one remaining inefﬁciency.

Although the original experience is no longer replayed, the remembered understanding
must still be serialised into textual context during every subsequent activation.

The behaviour is correct.

The implementation remains inefﬁcient.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

7. Context Reconstruction

Brain v2 currently operates as follows:

Experience

↓

Reasoning

↓

DPCP

↓

Memory Graph

↓

Retrieval

↓

Context Builder

↓

Transformer
This architecture successfully produces persistent cognition.

The limitation is that retrieved cognitive state must be repeatedly converted into textual
prompts before inference.

The transformer repeatedly processes information that it has effectively already
understood.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

8. Persistent Cognitive State

A future architecture might instead preserve cognitive state directly.

Rather than reconstructing identity, memory and understanding during every activation:

Persistent Cognitive State

↓

Reasoning

↓

State Update

↓

Sleep
Subsequent activations would process only changes.

Examples include:

•

•

•

•

•

new user input

new memories

environmental events

revised goals

updated relationships

The reasoning engine remains unchanged.

Only cognitive state evolves.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

9. Neural Attached Memory

One possible implementation is neural attached memory.

Unlike continual ﬁne-tuning, neural attached memory does not modify pretrained weights.

Instead it provides an efﬁcient persistent representation of evolving cognitive state that
participates directly in inference.

This persistent state functions as a dynamic overlay upon latent knowledge.

The pretrained model continues providing general reasoning capability.

Persistent state provides continuity.

Importantly, this proposal does not introduce fundamentally new behavioural capability.

Brain v2 already demonstrates the desired behaviour.

Neural attached memory simply removes the need to repeatedly reconstruct persistent
state through textual prompts.

It represents an architectural optimisation rather than a behavioural innovation.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

10. Discussion

The development of Brain v2 suggests that persistent cognition is already achievable
using contemporary transformer models.

The primary computational overhead arises not from reasoning itself, but from repeatedly
reconstructing cognitive state.

This distinction is important.

Much current research focuses on:

•

•

•

•

larger models

larger context windows

improved training

increased latent knowledge

These directions remain valuable.

However, persistent cognitive systems introduce a different optimisation problem.

Rather than increasing reasoning capability, future architectures may increasingly focus on
reducing the computational cost of maintaining continuity.

The transformer remains an excellent reasoning engine.

Its lifecycle may simply require evolution.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

11. Conclusion

Brain v2 demonstrates that persistent cognition does not require continual retraining or
modiﬁcation of pretrained model weights.

Instead, persistent behaviour emerges from maintaining an evolving cognitive state that
survives between activations.

Current transformer architectures require this state to be reconstructed through textual
context during every inference.

This approach is behaviourally successful but computationally inefﬁcient.

Future architectures need not replace transformers.

Nor need they fundamentally alter pretrained weights.

Instead, they may evolve by maintaining persistent cognitive state natively and reasoning
incrementally over change.

Brain v2 should therefore be viewed not as a ﬁnal architecture, but as a transitional one.

It demonstrates that the behavioural properties of persistent cognition are already
achievable today.

The remaining challenge is implementing those same behaviours more efﬁciently.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.


