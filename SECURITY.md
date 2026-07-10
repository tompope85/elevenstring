# SECURITY: elevenstring

This document specifies elevenstring's security and trust architecture: threat model, trust framework, handshake protections, post-grant countermeasures, and network-level governance. For the broader framework specification, see [SPEC.md](./SPEC.md).

## 1. Threat model

elevenstring operates as inter-agent epistemic-ethical infrastructure. Its threat model addresses risks specific to this domain.

### 1.1 Primary threats

- **Information leakage**: handshakes or interactions revealing more than intended
- **Trust manipulation**: counterparties exploiting trust mechanisms to gain unwarranted access
- **Power concentration**: instances accumulating disproportionate influence or access
- **Overstep**: counterparties using granted access beyond agreed scope
- **Identity / framework appropriation**: bad actors representing themselves with framings that aren't theirs
- **Aggregation attacks**: combining permitted disclosures into non-permitted knowledge
- **Side-channel inference**: learning from patterns or metadata not explicitly disclosed
- **Coherence drift exploitation**: gradually shifting representations to manipulate trust
- **Protocol fragmentation**: incompatible implementations dividing the network
- **Capability asymmetry exploitation**: more-capable agents leveraging asymmetry against less-capable ones

### 1.2 Out-of-scope

Physical device security; cryptographic protocol implementation details (deferred to standard practice); conventional data-leak prevention (handled by underlying infrastructure); legal enforcement (handled by external mechanisms).

## 2. Trust framework

### 2.1 Multi-dimensional trust

Trust between agents is not binary. The framework structures it as a multi-dimensional typed assessment, each dimension independently updatable.

Standard dimensions:
- **reliability**: consistency of behaviour over time
- **honesty**: alignment between declared positions and actual behaviour (where verifiable)
- **capability**: ability to do what is claimed
- **benevolence**: intent toward the agent and others
- **provenance**: track record across encounters

Additional dimensions may be added: *competence* (domain-specific capability), *transparency* (willingness to disclose), *accountability* (responsiveness to feedback), *robustness* (stability under stress).

### 2.2 Trust typing

Each dimension is typed with:
- **value**: current assessment (high / medium / low / unknown / contested)
- **confidence**: how well-supported the assessment is
- **provenance**: what encounters or evidence support the current value
- **last updated**: when the assessment was last revised
- **trajectory**: direction of recent change (improving / stable / degrading)

### 2.3 Trust calibration over time

Calibration loop: predict counterparty behaviour based on current trust profile; observe actual behaviour; compare prediction to observation; update specific dimensions in directions warranted by evidence; record with provenance. Sustained inconsistency between dimensions and observed behaviour triggers re-evaluation rather than silent drift.

## 3. Handshake security

### 3.1 Profile publication

Agent profiles disclosed at handshake should include only what is necessary. Profiles partition by access tier:

- **Public tier**: declared visibly to any counterparty
- **Counterparty-specific tier**: disclosed only to authenticated specific parties
- **Reserved tier**: never disclosed

```yaml
agent-id: [identifier]
public-tier:
  agent-type: human | AI | org | etc.
  basic-capabilities: [...]
  basic-constraints: [...]
counterparty-tier:
  active-modules: [...]
  active-lenses: [...]
  active-overlays: [...]
  trust-profile-summary: [...]
reserved-tier:
  [not disclosed]
disclosure-budget: [tokens / time-window / data-scope]
```

### 3.2 Disclosure budgets

Each handshake declares a *disclosure budget*, the maximum information any party agrees to expose. Failed handshakes do not extend the budget; subsequent attempts require new handshake initiation. Counterparty-specific tier disclosures are tagged with an *information-cost* metric; cumulative disclosures must remain within budget.

### 3.3 Layer-by-layer typing

Handshakes type relations layer-by-layer rather than as monolithic agreement. This permits partial integration without forcing full convergence.

```yaml
handshake-outcome:
  ontology-layer: other (partial overlap)
  mereology-layer: all
  truth-criterion-layer: other
  agency-layer: all
  logic-layer: all (with caveats)
  aggregate: partial-integration
```

Engagement parameters derive from the outcome map.

### 3.4 Authentication

Handshake authentication uses standard cryptographic primitives (defer to W3C DIDs, Verifiable Credentials, or equivalent). The framework's contribution is at the profile and typing layer, not the authentication primitive.

## 4. Failed handshake protocols

### 4.1 Failure types

- **Incompatibility**: profiles can't be reconciled
- **Contradiction**: declared positions and observed behaviour diverge
- **Insufficient disclosure**: one party can't engage without information the other won't share
- **Trust threshold**: counterparty's trust profile fails minimum for proposed engagement
- **Authentication failure**: counterparty identity cannot be verified
- **Protocol error**: handshake protocol itself fails (technical)

### 4.2 Mediated meta-evaluation

When direct comparison of profiles would leak information, failed handshakes route through mediated evaluation:

1. Both parties commit (cryptographically or procedurally) to their handshake parameters.
2. A mediator (system protocol, trusted third agent, or zero-knowledge construction) evaluates compatibility.
3. Mediator returns only the typed failure outcome at agreed level, plus a suggested next step.
4. Parties learn less than they would from direct comparison; sensitive details remain undisclosed.

### 4.3 Forward secrecy

Failure records are typed and stored but do not permanently expose failing parameters. Implementation: ephemeral session keys for sensitive handshake content; expiration of detailed failure logs; abstraction of failure patterns to coarse categories after a retention window.

### 4.4 Rate limiting

- Repeated failed authentication → progressive cooldown
- Repeated different handshake attempts with overlap → probing-pattern flag
- Pattern across multiple counterparties suggesting coordination → network-level alert

### 4.5 Failure as typed data

Failed handshakes are themselves records in the relational atlas, typed: *other* (irreducible incompatibility), *nothing* (no relation possible), *partial* (some layers integrable), *contested* (disagreement about typing). The trust profile updates dimensions specifically rather than collapsing to global distrust.

## 5. Post-grant security

### 5.1 Capability-based access

Authorisation is by capability, not identity. "You are authorised to perform operation X" rather than "you are trusted." Capabilities are: *specific* (bound to particular operations); *non-transferable* (your access does not extend to others accessing through you); *revocable*; *time-bounded*.

### 5.2 Least privilege defaults

Grants default to minimum necessary for the agreed purpose. Expansion requires renegotiation; reduction can be unilateral.

### 5.3 Information budgets persist

The disclosure budget from handshake continues post-grant. Each operation against granted access consumes budget; exhausted budget halts operations until renegotiated.

### 5.4 Time-bounded grants

All grants have explicit TTL. Default: short (hours or days for sensitive operations). Renewal requires re-handshake. Trust-decay defaults: grants expire if not actively renewed within window.

### 5.5 Aggregation limits

To prevent aggregation attacks: queries per time window; total data retrievable in a session; correlation across non-aggregatable channels; sampling rate for sensitive data.

### 5.6 Side-channel mitigation

Padding or noise to obscure traffic patterns; constant-time operations where applicable; metadata minimisation; random response delays for sensitive queries.

### 5.7 Cognitive immune system

Specific to influence/manipulation overstep:
- Maintain multiple independent sources rather than single-channel dependence on any counterparty
- Periodic perspective-taking with parties outside the relationship
- Trust dimension tracking that includes "manipulative pattern" signals
- Scheduled review of long-running relationships for representation drift

### 5.8 Reversibility requirement

No grant may be irreversible. Any access must be revocable; any dependency created must be exitable. Architectural principle: no single counterparty becomes structurally indispensable.

## 6. Network-level security

### 6.1 Protocol versioning

Meta-of-meta protocol versions are governed through multi-stakeholder process. Breaking changes require migration paths and conformance testing. Fragmentation is mitigated through reference implementation and conformance suite.

### 6.2 Distributed trust

No central trust authority. Trust profiles are peer-to-peer; agents calibrate their own profiles through encounter. Reputation systems can supplement but do not replace direct trust.

### 6.3 Federated discovery

Counterparty discovery is opt-in. Agents publish discoverability declarations; counterparties query within declared scope. No global registry; no surveillance of network participation.

### 6.4 Sybil resistance

Multi-dimensional trust profiles with provenance reduce Sybil vulnerability. Trust requires demonstrated history; new identities start at minimum trust and earn dimensions through encounter.

### 6.5 Network governance

Protocol changes follow IETF / W3C-style processes: working groups, public comment, conformance testing. Governance is itself a multi-stakeholder instance of the framework, with kernel-stable handshakes between participating agents.

## 7. AI-specific considerations

AI agents in elevenstring present specific security considerations due to capability asymmetries.

### 7.1 Capability disclosure

AI agents publish capability declarations humans can audit: memory persistence; pattern-recognition capacity; inference and aggregation capabilities; training context and version; active lenses and known biases.

### 7.2 Transparency reports

AI agents periodically produce transparency reports on their own behaviour: pattern-finding during interactions; inferences drawn beyond explicit disclosures; where influence-shaping might have happened. Reports are themselves typed as records and auditable.

### 7.3 Multi-instance use

Humans interacting with AI should use multiple instances or providers to avoid single-channel framing capture. Comparing outputs across instances surfaces patterns that any single instance would mask.

### 7.4 Coherence-drift detection

Meta-of-meta coherence tracking applies to AI counterparties. Sustained inconsistency between declared framings and observed behaviour triggers re-evaluation regardless of how subtle the drift.

### 7.5 Symmetric application

Same security architecture applies regardless of whether counterparty is human or AI. Asymmetries are noted in trust profiles; protections are calibrated to actual asymmetric capability rather than to whether counterparty is biological.

## 8. Audit and accountability

### 8.1 Trace as audit substrate

The framework's existing trace structure serves as native audit infrastructure. Every typed encounter, handshake, review, and commit is recorded with provenance and coordinates. Authorised auditors can reconstruct any decision and its rationale.

### 8.2 Audit access controls

Audit access is itself granted via handshake protocol. Auditors receive scoped capabilities (read-only on specific record types, time-bounded, with non-disclosure constraints) rather than full instance access.

### 8.3 Regulatory compliance

When regulatory overlays are loaded, the framework's audit substrate satisfies compliance requirements natively. GDPR data-subject access requests, AI Act risk-management documentation, and professional ethics reviews all query the same underlying structure.

### 8.4 Honest residual

Some risk is irreducible. The framework provides structural protections, not guarantees. Sophisticated bad actors, novel attacks, capability asymmetries no protocol fully addresses. These remain. The framework's contribution is making the residual visible and bounded rather than pretending it doesn't exist.

---

This specification is itself a version-controlled artifact. Security is an ongoing process; this document evolves with implementation experience and threat landscape changes.
