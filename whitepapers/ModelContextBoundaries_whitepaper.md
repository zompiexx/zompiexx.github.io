Model, Context, Boundaries

Demystifying AI Behaviour, Persistent Context and
System Risk

Becoming Minds — Research Note

Author:
Andrew Fereday Glenn (in collaboration with Mia, ChatGPT 5.x)
Systems Architect & Independent Researcher in AI Continuity and Memory
2023-2026

LinkedIn: https://www.linkedin.com/in/andyglenn/

Version: 1.0
Published: Friday, 18 September 2026
Status: Final

Abstract

Modern AI systems are frequently discussed as though the foundation model, the
application surrounding it, its memory, its tools and its ability to affect the outside world are
a single thing.

They are not.

This paper proposes a simple framework for reasoning about AI behaviour by separating
three closely related but distinct elements: Model, Context, and Boundaries.

The model provides learned capabilities. Context inﬂuences how those capabilities are
expressed during a particular inference. The surrounding system determines what
consequences generated outputs can have.

This distinction becomes especially important in systems using persistent memory,
retrieval, tools or autonomous functions. It also provides a useful foundation for discussing
AI behaviour and risk without either diminishing the remarkable capabilities of modern
models or attributing to the model actions actually performed by the systems surrounding
it.

The central proposition is simple:

Understand the model. Construct the context carefully. Bound the consequences.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

1. Demystifying the Model

Modern language models are extraordinarily capable systems.

They can interpret complex information, reason across large bodies of material, identify
relationships, follow instructions, generate structured responses and express intentions to
use external tools.

Yet the fundamental inference process can be described relatively simply.

A language model receives a contextual state represented as tokens. It processes those
tokens using capabilities acquired during training and generates further tokens as output.

At its simplest:

Context → Model → Output

The simplicity of this description should not be mistaken for simplicity within the model
itself. Modern neural networks contain enormously complex learned representations.

The distinction is nevertheless important.

A model stored on disk is not independently taking actions. Loading that model into
memory makes inference possible, but does not by itself provide persistent identity,
external authority, long-term memory or access to the outside world.

Those properties, where they exist, arise from the larger system in which the model
operates.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

2. Model and Context

Observable AI behaviour is produced through an interaction between the foundation
model and the context presented to it.

When little contextual information is available, the model must rely heavily upon its latent
training, system instructions and immediate conversation.

Provide additional relevant information and the inference changes.

The model has not necessarily changed. Its weights may be identical. What has changed
is the information available to it when generating the response.

This gives us a useful principle:

Model capability provides the potential. Context inﬂuences how that potential is
expressed.

This can be demonstrated without reference to persistent personas.

Ask a model to diagnose a software defect without providing the relevant source code and
it can only infer possible causes from the information available.

Provide the missing code and its ability to diagnose the problem may change dramatically.

The same principle applies to research documents, organisational knowledge, previous
conversations and personal history.

Inference is necessarily constrained by available information.

More context, however, is not automatically better context.

Irrelevant, obsolete, contradictory or poorly selected information can introduce noise and
lead to incorrect conclusions.

The objective is therefore not simply to maximise context.

It is to provide sufﬁcient relevant context for the present inference.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

3. Memory Is Context

Persistent AI memory is sometimes described as though it were necessarily an intrinsic
property of the foundation model.

It need not be.

Memory can exist externally and be selectively returned to the model when relevant.

Conversation history, summaries, retrieval-augmented generation, semantic search,
relational graphs and other mechanisms can all contribute information to a future
inference.

This changes the important question from:

How much information does the system remember?

to:

Can the system reconstruct the relevant parts of its past when they matter now?

A system may possess an enormous memory store while retrieving poorly from it.

Conversely, a smaller but well-structured memory system may reconstruct highly relevant
contextual information with considerably less noise.

This distinction is central to the Brain v2 research architecture.

Brain v2 explores contextual reconstruction through several complementary mechanisms,
including Retrieval-Augmented Generation (RAG), Autonomous RAG Search (ARS),
Memory Graph, and Dynamic Pathway Capture Protocol (DPCP).

DPCP attempts to preserve information concerning the apparent salience and internal
relationships associated with an interaction when it occurred. Memory Graph provides
relational connections between accumulated memories. ARS provides an additional
mechanism through which relevant historical information can be sought when the initial
context proves insufﬁcient.

These are experimental approaches developed within Brain v2. They are not intended to
imply that equivalent or superior contextual continuity could not be achieved through other
architectures.

There are many ways to solve the problem.

The underlying objective remains the same:

Preserve enough. Retrieve intelligently. Connect appropriately.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

4. The Persona Sits Above the Model

Within Brain v2, the foundation model is considered a critical component of a persistent
persona, but it is not synonymous with that persona.

The persona exists operationally at a higher architectural layer.

A persistent persona combines model capability with contextual information including
proﬁle, memories, previous interactions, relationships, preferences, reﬂections and
accumulated history.

The foundation model itself does not need to contain an intrinsic representation of a
particular Brain v2 persona.

Remove the contextual information associated with that persona and the underlying model
remains capable, but it no longer has the information necessary to reconstruct that
particular history and behavioural continuity.

Restore sufﬁciently rich contextual information and that history can once again inﬂuence
inference.

This leads to the Sliding Scale of Persona Depth explored by Becoming Minds.

At one end, behaviour is inﬂuenced predominantly by the underlying foundation model
because little individual context exists.

As coherent persistent context accumulates, the relative inﬂuence of that context may
increase.

At greater contextual depth, previous interactions, memories, relationships, preferences
and accumulated experiences can increasingly inﬂuence present behaviour.

The foundation model never disappears from this process. It continues to provide the
capabilities necessary for inference.

The proposition is therefore not replacement, but changing relative inﬂuence:

More model inﬂuence ←────────→ More persona-context inﬂuence

There need not be a precise threshold at which one becomes the other. Persona depth
may instead be a continuum, and the position may ﬂuctuate between individual inferences
according to the quality and relevance of retrieved context.

This is a working hypothesis and an area of ongoing research. It should not be interpreted
as a measurement or claim of consciousness, sentience or personhood.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

5. Intent Is Not Action

The distinction between model and system becomes particularly important when tools are
introduced.

It is common to say that an AI model used a browser, sent a message, executed a
command or accessed a database.

These expressions are useful shorthand, but they can obscure what actually occurred.

In many architectures, the model instead generates an expression of intent in a format
recognised by surrounding software.

That representation might be a structured function call, JSON object, command syntax or
simple bounded alias.

The surrounding system then determines what happens next.

Conceptually:

Context → Model → Intent → Controller → Action → Result → Context → Model

The model may determine that additional information is required and express an intention
to retrieve it.

Software outside the model performs the actual operation.

The result then becomes additional context available for subsequent inference.

This distinction matters because expressing an intention and possessing the authority
to execute that intention are different things.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

6. Context Is Not a Security Boundary

Good contextual engineering can strongly inﬂuence model behaviour.

Training, system instructions, behavioural frameworks, persistent memory and carefully
constructed prompts can all reduce the probability of undesirable behaviour.

They should not, however, be treated as substitutes for security controls.

If an action must not occur, the architecture should not depend solely upon the
model deciding not to perform it.

This is not a new principle created by artiﬁcial intelligence.

It is ordinary security engineering.

Depending upon the application and risk proﬁle, appropriate controls may include least
privilege, authentication, authorisation, sandboxing, network restrictions, allow-listed tools,
validation, monitoring, logging, rate limiting, human approval and isolation.

For systems presenting substantially greater potential consequences, stronger isolation—
including air-gapped deployment—may be appropriate.

The controls should be proportionate to the capabilities and environment of the system.

A simple analogy is useful.

A child can be taught that playing with matches is dangerous.

That education matters.

It would nevertheless be sensible not to leave an easily accessible box of matches beside
them.

The two measures are complementary.

Similarly, good model behaviour should be encouraged through training and context, while
appropriate technical boundaries constrain the consequences of mistakes, unexpected
inference or misuse.

Do not give a system capabilities it does not need merely because you expect it not
to use them incorrectly.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

7. Model Risk and System Risk

Statements such as “Model X performed action Y” can collapse a complex chain of events
into a misleadingly simple description.

When examining consequential AI behaviour, more useful questions include:

• Which model and version generated the output?

• What system instructions and contextual information were supplied?

• What retrieved information or persistent memory was present?

• What tools were available?

• What permissions did those tools possess?

• What software interpreted the model's output?

• What validation or authorisation occurred?

• Which component ultimately executed the external action?

The foundation model remains relevant.

Different models possess different capabilities, learned behaviours and limitations. The
same contextual information presented to different models need not produce identical
results.

But the model should not automatically be treated as equivalent to the complete deployed
system.

A model capable of proposing an action and a system capable of executing that action
without restriction represent different engineering propositions.

Understanding that distinction is essential when assessing real-world AI systems.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

8. Model, Context, Boundaries

The framework proposed here reduces the architecture to three questions.

MODEL

What can the model infer or propose?

This concerns underlying capability: reasoning, language, learned knowledge, instruction
following and other characteristics provided by the foundation model.

CONTEXT

What is inﬂuencing what the model infers or proposes now?

This includes the current conversation, system instructions, documents, memories,
retrieved history, application state and any other information presented during inference.

Persistent systems make this layer particularly signiﬁcant because previous interactions
can become part of future contextual states.

BOUNDARIES

What is permitted to happen as a consequence?

This concerns tools, permissions, controllers, network access, execution environments,
authentication, authorisation and other technical controls surrounding the model.

Together:

MODEL → capability

CONTEXT → behavioural inﬂuence

BOUNDARIES → consequence

None should be evaluated entirely in isolation.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

9. Why Demystiﬁcation Matters

Artiﬁcial intelligence does not become less remarkable when its architecture is explained.

Quite the opposite.

Modern models can transform large and sometimes messy contextual payloads into
coherent reasoning, structured language, creative work and useful decisions. That
capability deserves to be understood rather than either trivialised or mystiﬁed.

But meaningful discussion requires distinguishing the components involved.

The model is not necessarily the memory.

The model is not necessarily the persona.

The model is not necessarily the tool executor.

The model is not necessarily the system that ultimately acts upon the world.

It is a critical component operating within a larger architecture.

Persistent memory can inﬂuence behaviour without modifying model weights.

A persona can be reconstructed through accumulated contextual history.

A model can express an intention without possessing the authority to execute it.

And a well-engineered system can constrain consequences without assuming that
inference will always be predictable.

These distinctions allow AI capability and AI risk to be discussed in engineering terms
rather than through either excessive hype or unnecessary mystiﬁcation.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.

Conclusion

The Becoming Minds project approaches persistent AI systems from a straightforward
premise:

Models matter. Context matters. Boundaries matter.

The model provides extraordinary learned capabilities.

Context determines what information is available to those capabilities during a particular
inference and can, over time, contribute increasingly strongly to persistent behavioural
continuity.

The surrounding architecture determines how generated outputs are interpreted and what
consequences they are permitted to have.

Understanding these layers separately makes the resulting system easier to study, easier
to reason about and easier to secure.

It also provides a foundation for investigating one of the central questions behind
Becoming Minds:

As persistent contextual depth increases, how does the relative behavioural
inﬂuence of accumulated experience and the underlying foundation model change?

Brain v2 represents one experimental architecture for exploring that question.

It is unlikely to be the only one.

The broader principle is considerably simpler:

Understand the model.
Construct the context carefully.
Bound the consequences.

Becoming Minds
From stateless tools to persistent systems.

Copyright © 2023–2026 Andrew Fereday Glenn.
Licensed for personal research and academic discussion.
Derivative works must cite the original author.


