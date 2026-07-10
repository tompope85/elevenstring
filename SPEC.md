# SPEC: elevenstring

This is the framework specification. For introduction, see [PRIMER.md](./PRIMER.md); for worked examples, see [EXAMPLES.md](./EXAMPLES.md).

## 1. Foundational concepts

### 1.1 The kernel

The kernel is the load-bearing minimum any instance must honour. It contains four primitives, identical across all instances:

- **distinction**: the primitive operation of cutting this from not-this. Without it, nothing is nameable.
- **iteration-identity**: the criterion by which a re-application of an operation counts as the same operation rather than a new one. Without it, recursion collapses.
- **perspective**: the vantage from which considerations are individuated. Without it, "from where" has no meaning.
- **coherence-constraint**: the minimum consistency required for the framework's statements to be statements at all. Without it, the framework cannot be uttered.

These are not assertions about reality. They are the operational requirements for the framework to be expressible and used.

### 1.2 The triad

Three reference markers used to type any relation between an agent and what they encounter:

- **All**: the encountered thing maps onto the framework as a configuration of its commitments. Subsumable.
- **Other**: the encountered thing is irreducibly different but remains in relation. Engagement proceeds with awareness of difference.
- **Nothing**: no relation is possible in this transfer. Void.

The triad lives at the meta-of-meta level as referential markers, not as relata. When a relation is typed "nothing," it points to the canonical Nothing marker; it does not relate to Nothing. The triad does not admit a fourth type; the catuṣkoṭi's fourth corner is declined because additional types generate regress.

Typings are epistemic and pragmatic, not alethic. They are considerations, not metaphysical claims.

### 1.3 Operations

- **distinguish**: apply the distinction primitive
- **iterate**: apply an operation again, retaining iteration-identity
- **perspectivise**: establish a vantage
- **encounter**: engage with something outside current frame
- **type**: apply all/nothing/other to a consideration
- **handshake**: negotiate inter-instance interaction
- **review**: examine the framework (architectural or metapraxis)
- **commit**: snapshot a version

### 1.4 Meta-principles

- **pluralism**: this instance is one self-consistent option, not the universal meta-frame.
- **revisability**: all typings, commitments, and framings are provisional and updatable.
- **operation-primary**: the framework is the ongoing recursive operation, not a static structure.
- **relational mastery**: the framework's reach is its capacity to type relations, not to subsume content.
- **triad-as-consideration**: all/nothing/other are epistemic typings, not alethic claims.
- **coherence-of-representation**: at meta-of-meta, coherent representation of other agents is the respect criterion.

## 2. Architectural layers

### 2.1 Modules

A *module slot* is a configurable position. Each accepts one *commitment* at a time; alternatives are available as inactive options.

- **ontology**: substance / process / relational / nominalist / pluralist...
- **mereology**: classical / fuzzy / lived-boundary / mereotopological...
- **truth-criterion**: correspondence / coherence / pragmatic / deflationary / coherence-plus-ownership...
- **agency**: individual / distributed / project-oriented / effortless / collective...
- **logic**: classical / intuitionistic / paraconsistent / fuzzy / dialetheist...
- **temporality**: linear / cyclical / processual / thick-present / longue-durée / blockworld...
- **causation**: efficient / formal / final / probabilistic / downward / mixed...
- **modality**: necessary / contingent / dispositional / Lewisian / Aristotelian...
- **narrative**: propositional / episodic / arc / fragmentary...
- **affect**: noise / data / motivation / constitutive...
- **embodiment**: disembodied / embodied / extended / distributed...
- **semiotics**: Saussurean dyadic / Peircean triadic / post-structuralist...
- **metacognition**: active / passive / scheduled / continuous...

New slots can be added by extension.

### 2.2 Framings

Evaluative lenses applied across module commitments. Multiple framings can be active simultaneously; they may be rotated, stacked, or weighted.

- **coherence**: do the parts fit together?
- **correspondence**: does this match the world?
- **pragmatic**: does this work toward goals?
- **generativity**: does this produce new possibilities?
- **power**: what does this enable or constrain?
- **care**: to whom or what is this answerable?
- **viability**: does this sustain itself?
- **parsimony**: is this minimal?
- **disclosure**: what does this reveal or hide?
- **existentialist**: does this own its situatedness?
- **sense-based-geometry**: does this respect gradient and gestalt structure?
- **aesthetic**: is this fitting or elegant?
- **ethical**: what should be?

### 2.3 Overlays

Context-specific configurations loaded for particular domains, jurisdictions, or cultures. Overlays do not replace active commitments; they sit alongside as working vocabularies.

- **Domain overlays**: medical, software-engineering, legal, ML / data-science, consulting. Each declares the domain's working ontology, mereology, agency model, and translation operations to the agent's meta-framework.
- **Regulatory overlays**: GDPR, HIPAA, EU AI Act, regional privacy regimes, professional codes. Each declares jurisdictional scope, trigger conditions, required and prohibited behaviours, audit requirements.
- **Cultural overlays**: linguistic, traditional, disciplinary. Handle vocabulary, framings, and translation for cross-cultural engagement.

Multi-loaded operation is supported. Multiple overlays simultaneously surface conflicts as typed tensions requiring explicit resolution.

### 2.4 Instances

An *instance* is a versioned configuration of the framework: kernel + active modules + active framings + active overlays + meta-principles at a point in time. Instances are committed via the version protocol.

```
my-OS/
├── kernel/
├── modules/
├── framings/
├── overlays/
├── relations/
├── handshakes/
├── reviews/
├── trust/
├── instances/
│   ├── v0.1.md ... vN.M.md
│   └── current -> latest
├── daily/
└── projects/
```

### 2.5 Relations

The *relational atlas* is the agent's accumulated record of typed encounters. Organised by aggregate typing:

- `/relations/alls/`: encounters typed as subsumable configurations
- `/relations/others/`: encounters typed as irreducibly different
- `/relations/nothings/`: encounters typed as void
- `/relations/mixed/`: encounters with layered typings

Each relation record contains: object, perspective coordinates, per-layer typings with confidence and rationale, aggregate typing, links to other relations, next-steps.

### 2.6 Handshakes

The structured exchange protocol between agent instances. Recorded under:

- `/handshakes/humans/`: typed relations with human counterparties
- `/handshakes/AIs/`: typed relations with AI agents
- `/handshakes/digital/`: typed relations with digital systems
- `/handshakes/non-human/`: typed relations with animals, ecosystems, material objects
- `/handshakes/orgs/`: typed relations with organisations

### 2.7 Trust

A multi-dimensional typed assessment of a counterparty. Not binary; structured by dimension and updated through encounter.

- **reliability**: consistency of behaviour over time
- **honesty**: alignment between declared positions and actual ones (where verifiable)
- **capability**: ability to do what is claimed
- **benevolence**: intent toward the agent and others
- **provenance**: track record across encounters

Each dimension is independently updatable, with traceable rationale.

## 3. Operations and protocols

### 3.1 Encounter typing

1. Encounter trigger: agent meaningfully engages with material outside current frame.
2. Pre-encounter note (recommended): active modules and framings recorded.
3. Engagement: read, study, work with, or experience the material.
4. Initial typing pass: per active module, type the material's stance as all / nothing / other with rationale.
5. Aggregate typing: overall typing based on per-layer pattern.
6. Provenance annotation: source (studied / experienced / both), date, OS version, active modules.
7. Storage: file in appropriate `/relations/` subdirectory.
8. Linking: connect to related prior relations.
9. Next steps: schedule metapraxis review if experiential follow-up appropriate.

### 3.2 Handshake protocol

1. Profile publication: each agent publishes or makes queryable their agent profile.
2. Exchange: profiles exchanged via shared protocol.
3. Layer-by-layer typing: each agent types relations between their commitments and the other's at each module slot.
4. Aggregate handshake outcome: integrated / partial / failed, with which layers are which.
5. Engagement parameters: derive what engagement is possible.
6. Record: handshake stored in appropriate `/handshakes/` subdirectory.
7. Trust update: relevant trust dimensions updated based on outcome.

### 3.3 Architectural review

1. Open `/reviews/architectural/{date}-{topic}.md`.
2. Declare framing under which review is conducted.
3. Examine each active module: is it serving? Does evidence (from relations, friction journal, recent encounters) support it?
4. Identify revision candidates.
5. Decide: keep, modify, replace, or mark provisional.
6. Commit changes; if significant, snapshot as new instance version.

Triggers: scheduled (typically quarterly), N encounters typed, friction-note pattern, major transition.

### 3.4 Metapraxis review

1. Open `/reviews/metapraxis/{date}-{topic}.md`.
2. *Phase 1, bracketing*: suspend current module vocabulary; attend to what came up in the doing; write freeform.
3. *Phase 2, articulation*: re-engage framework vocabulary; map experiential content to module slots; identify where current modules accommodate and where they strain.
4. *Phase 3, integration*: decide framework changes and commit; link review to triggering experience and resulting changes.

Triggers: after immersive engagement with a domain, sustained friction, significant encounter, metapraxis-flag tag in daily capture.

### 3.5 Resolution protocols

When incoherence surfaces:

- **Self-other representation mismatch** → re-handshake with updated typings, new record linking to prior.
- **Word-deed gap** → align action with claim or revise claim to match practice.
- **Framing conflict** → surface the difference; seek shared ground or proceed with awareness of divergence.
- **Schema imposition** → load the appropriate overlay or explicitly type it as other.
- **Goal-frame mismatch** → surface divergent endpoints; choose convergence or typed coexistence.

Resolution outcomes are themselves typed (resolved / partial / unresolvable-explicitly-typed) and recorded.

### 3.6 Security and trust protocols

For failed handshakes and post-grant interactions:

- **Mediated meta-evaluation** for failed handshakes
- **Information budgets** that don't expand on failure
- **Forward secrecy** for failure records
- **Rate limiting** for repeated failures
- **Capability-based access** for post-handshake interaction
- **Time-bounded grants** with expiration
- **Differential disclosure** preventing aggregation attacks
- **Reversibility requirement** for all access grants

Detail in [SECURITY.md](./SECURITY.md).

## 4. Record formats

### 4.1 Common metadata

```yaml
---
type: relation | handshake | review | instance | commitment
created: YYYY-MM-DD
os-version: vN.M
perspective:
  framings: [framings active at creation]
  modules: [modules active at creation]
provenance: [studied / experienced / dialogue / inferred / ...]
links: [related records]
confidence: high | medium | low | provisional
---
```

### 4.2 Relation record

```yaml
---
type: relation
object: [name/identifier of what was encountered]
[standard metadata]
---

## Per-layer typings
[for each relevant module: type + rationale]

## Aggregate consideration
[overall typing with reasoning]

## Next
[scheduled reviews, related encounters, open questions]
```

### 4.3 Handshake record

```yaml
---
type: handshake
counterparty: [identifier]
counterparty-type: human | AI | digital | non-human | org
[standard metadata]
---

## Profile exchanged
[summary of each party's declared profile]

## Per-layer typings
[outcomes per module slot]

## Engagement parameters
[what engagement is possible]

## Trust dimensions updated
[which dimensions, direction, rationale]
```

### 4.4 Review record

```yaml
---
type: review | metapraxis-review
trigger: [what initiated]
[standard metadata]
---

## Phase 1
[bracketing / framing-selection]

## Phase 2
[thinking / module-examination]

## Phase 3
[integration / commits with evidence; new version if applicable]
```

### 4.5 Instance snapshot

```yaml
---
type: instance
version: vN.M
date-committed: YYYY-MM-DD
prior-version: v(N.M-1)
summary: [what changed and why]
---

## Active modules
## Active framings
## Active overlays
## Meta-principles
## Coordinates
## Changes from prior version (diff with rationale)
```

## 5. Coordinates and queries

### 5.1 Coordinate system

Every record carries coordinates along three axes:

- **time**: date, OS version, version history, position in trace
- **space**: file location, layer (kernel / module / framing / overlay / relation / handshake / review / instance)
- **perspective**: active framings, active modules, agent identity, provisional flags

### 5.2 Query patterns

- *temporal*: "what was X like at version v1.4?"
- *spatial*: "all typings of frameworks at module-ontology layer"
- *perspectival*: "all relations typed under coherence framing"
- *combined*: "how has my consideration of X evolved across versions, under different framings?"

Query implementation is environment-dependent (Git log + grep, knowledge-graph query, SPARQL) but coordinate structure is invariant.

## 6. Network mode

### 6.1 Federated architecture

elevenstring operates as federated meta-cognitive infrastructure when multiple instances interact. Each instance is sovereign at lower layers; all share meta-of-meta protocols.

### 6.2 Shared protocols

The meta-of-meta level specifies:

- kernel primitives (identical across instances)
- triad typology (universal markers)
- handshake protocol specification
- trust dimension structure
- coordinate system
- coherence-of-representation as inter-instance respect criterion

### 6.3 Governance

Multi-stakeholder governance of the meta-of-meta level. Versioning follows IETF / W3C-style processes. Implementation conformance is testable; protocol fragmentation mitigated through shared reference implementation.

### 6.4 Interoperability

Instances with different module commitments interoperate via the handshake protocol. Sovereignty plus interoperability: each retains its commitments while coordination remains possible.

## 7. Extensibility

The framework supports extension without modification of the kernel. New module slots, framings, overlays, agent profile schemas, handshake protocols, and operations can be added as extensions. The kernel remains stable; the architecture grows.

Extension proposals follow the framework's own logic: an extension is itself typed, with provenance, evidence, and impact analysis.

## 8. Vocabulary

| Term | Definition |
|------|------------|
| distinction | the primitive this/not-this cut (kernel) |
| iteration-identity | criterion for same-operation re-applied (kernel) |
| perspective | vantage that individuates considerations (kernel) |
| coherence-constraint | minimum consistency for expressibility (kernel) |
| triad | the three reference markers (all/nothing/other) |
| typing | application of all/nothing/other to a consideration |
| consideration | the unit being typed |
| module slot | a configurable position in the framework |
| commitment | what is currently loaded in a module slot |
| framing | evaluative lens applied across module contents |
| overlay | context-specific working configuration (domain / regulatory / cultural) |
| handshake | structured exchange protocol between agent instances |
| trust dimension | one axis of a multi-dimensional trust profile |
| trace | temporally-ordered chain of typings or commitments |
| coordinate | position in time / space / perspective |
| instance | a versioned configuration of the whole |
| atlas | the totality of typed relations |
| iteration | an application of the recursive operation |
| iteration-depth | apparent recursive depth (often called "level") |
| reflexivity | the operation turned back on itself |

---

This specification is itself a version-controlled artifact. Revisions follow the framework's own protocols. Contributions are welcome under the Developer Certificate of Origin; see [CONTRIBUTING.md](./CONTRIBUTING.md).

