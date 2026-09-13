# Actor, Authority & Agent Architecture

RESXPECT is designed around a simple idea:

**Actions should always be traceable to an accountable Principal.**

As RESXPECT evolves, agreements may be created or managed not only by individuals acting directly, but also by authorised human actors and software agents acting on behalf of a Principal.

This architecture defines how those relationships work.

> **Actors perform actions. Principals carry accountability. Authority connects the two.**

---

## Principals

A **Principal** is the persistent accountable identity behind activity on RESXPECT.

A Principal may be:

- a Human
- an Organisation

The Principal owns the economic relationship represented by an agreement.

It is the identity that ultimately carries:

- reputation
- agreement history
- outcomes
- dispute consequences
- delegated authority
- accountability

Creator and Runner are not permanent identities.

They are simply roles a Principal takes inside an agreement.

A Human or Organisation may act as a Creator in one agreement and a Runner in another.

---

## Human Principals

Humans join RESXPECT using an alias-first model.

```text
Join RESXPECT
    ↓
Alias
    ↓
Persistent Human Principal
    ↓
Agreement history + reputation
```

The alias is the public-facing identity.

The Principal underneath it is the persistent protocol identity that carries history, authority and accountability.

A Human Principal may remain pseudonymous while still building a persistent reputation over time.

---

## Organisation Principals

Organisations use their public organisation identity rather than a pseudonymous alias by default.

```text
Organisation
    ↓
Persistent Organisation Principal
    ↓
Agreement history + reputation
```

An Organisation Principal may later authorise multiple human or software actors to act on its behalf.

The Organisation remains the accountable Principal regardless of which authorised Actor performed the action.

---

## Actors

An **Actor** is the entity that performs an action.

An Actor may be:

- the Principal acting directly
- a delegated Human Actor
- a delegated software Agent

```text
Actor
├── Principal acting directly
├── Delegated Human Actor
└── Delegated Software Agent
```

The Actor answers:

**Who performed this action?**

The Principal answers:

**Who is accountable for it?**

---

## Authority

**Authority** defines what an Actor is allowed to do on behalf of a Principal.

A delegation may define permissions such as:

- create agreements
- maximum agreement value
- allowed work categories or skills
- submit evidence
- fund agreements
- approve delivery
- release funds
- open disputes
- expiry
- revocation

Example:

```text
Principal
    ↓
Delegation
├── Can create agreements: Yes
├── Maximum value: $500
├── Allowed skills: Design, Development
├── Release funds: No
├── Open disputes: Yes
└── Expires: 30 Sep
    ↓
Agent
```

An Actor should never be able to exercise more authority than the Principal has granted.

---

## Chain of Authority

Every consequential delegated action should be traceable through a clear **Chain of Authority**.

```text
Action
  ↓
Actor
  ↓
Delegation / Authority
  ↓
Principal
  ↓
Agreement
  ↓
Outcome
```

This allows RESXPECT to establish:

- who acted
- who they acted for
- what authority they had
- which agreement the action belonged to
- what outcome followed

This becomes increasingly important as software agents begin acting economically on behalf of individuals and organisations.

---

## Delegated Human Actors

An Organisation Principal may authorise human team members to act on its behalf.

Example:

```text
Organisation Principal
        │
        ▼
Delegated Human Actor
```

A Human Actor may be allowed to:

- create agreements
- review work
- submit evidence
- open disputes

while being prevented from:

- releasing funds
- creating agreements above a defined value
- changing organisation-wide permissions

The action remains attributable to the Human Actor, while accountability remains with the Organisation Principal.

---

## Delegated Software Agents

A Principal may also authorise a software Agent.

Example:

```text
Organisation Principal
        │
        ▼
Procurement Agent
        │
        ├── Create agreements: Yes
        ├── Maximum value: $500
        ├── Allowed skills: Design, Development
        ├── Release funds: No
        └── Open disputes: Yes
```

If the Agent attempts an action outside its authority, RESXPECT should reject it.

For example:

```text
Maximum authorised value: $500
Requested agreement value: $1,200
                ↓
              Rejected
```

If the Agent creates a permitted $300 agreement, RESXPECT may record:

```text
Action performed by Procurement Agent
Acting for Organisation Principal
Under Delegation #18
```

---

## Accountability

Delegation does not remove accountability.

If a Principal gives an Actor authority to perform an action, the resulting consequences remain attached to the Principal.

This applies whether the Actor is:

- a Human
- a software Agent

The Actor may perform the action.

The Principal remains responsible for the authority it granted.

> **Delegation does not remove accountability.**

---

## Reputation and Attribution

RESXPECT separates **reputation ownership** from **action attribution**.

> **Reputation follows accountability. Attribution follows action.**

The Principal receives the actual reputation outcome.

The Actor receives attribution for the actions they performed.

Example:

```text
Organisation Principal
Runner Role
    │
    ▼
Delegated Human Actor
    │
    ▼
Successful Agreement
```

Result:

```text
Organisation Principal
→ receives Runner RP

Delegated Human Actor
→ receives Actor attribution
```

The same agreement should not generate duplicate RP for both the Principal and the Actor.

One economic outcome should produce one Principal reputation outcome.

---

## Principal Reputation

**Principal Reputation** represents the accountable Principal's history on RESXPECT.

It may include:

- RP
- Skill Trust
- successful agreements
- failed outcomes
- dispute consequences
- validation outcomes

The Principal's reputation represents the economic relationships for which that Principal was responsible.

---

## Actor Attribution

**Actor Attribution** records which Actor actually performed consequential actions.

Example:

```text
Agreement #241

Runner Principal:
Organisation Principal

Performed by:
Delegated Human Actor

Authority:
Delivery Delegation #18

Outcome:
Successful
```

Attribution provides transparency without duplicating reputation.

---

## Actor Performance History

Actors may accumulate an operational history based on the agreements they acted in.

For example:

```text
Delegated Human Actor

Delegated agreements: 67
Successful outcomes: 63
Disputes: 3
Failed outcomes: 1
```

This is not RP.

It is a verifiable record of activity.

The same principle may later apply to software Agents.

```text
Development Agent

Agreements acted in: 1,240
Successful outcomes: 1,191
Disputes: 21
Authority violations: 0
```

This creates useful performance history while keeping accountability with the Principal.

---

## Human Actor Portability

A Human Actor's attributable work history should remain associated with their own Human Principal even if they later stop acting for an Organisation.

For example:

```text
Human Principal

Delegated work history:
Agreements acted in: 500
Successful outcomes: 486
```

The Organisation retains its Organisation reputation.

The Human retains the verifiable record that they acted in those agreements.

This preserves two distinct facts:

- the Organisation has proven organisational performance
- the Human has proven experience acting on behalf of an Organisation

---

## External Identity Anchoring

RESXPECT does not require legal identity disclosure as the foundation of protocol identity.

Instead, Humans and Organisations may optionally anchor their RESXPECT identity to existing public identities.

Examples include:

- personal or organisation websites
- GitHub
- X or other social profiles
- public wallets
- other established online properties

The important direction of proof is that the external property links back to the RESXPECT profile.

Example:

```text
organisation.example

Official Links
├── GitHub
├── X
└── RESXPECT
```

This shows that the controller of the external property publicly recognises that RESXPECT Principal.

External Identity Anchoring proves **continuity and control**, not legal identity.

---

## Humans and External Identity

A Human Principal may remain pseudonymous while connecting their alias to an established online presence.

Example:

```text
SilentFalcon

External Anchors
├── Personal website
├── GitHub
└── X
```

The Human does not need to expose a legal name for those connections to strengthen identity continuity.

---

## Organisations and External Identity

An Organisation may anchor its RESXPECT Principal to its established public channels.

Example:

```text
Example Organisation

External Anchors
├── organisation.example
├── Official X
└── GitHub Organisation
```

This allows RESXPECT to distinguish between:

- a claimed Organisation identity
- an Organisation identity publicly linked from established external channels

This does not mean RESXPECT is verifying the Organisation's legal incorporation.

It establishes continuity and control of the public identity.

---

## Legal Identity

RESXPECT separates three different identity concepts:

1. Principal control
2. External identity anchoring
3. Legal identity

RESXPECT requires Principal control.

External identity anchoring may strengthen identity continuity.

Legal identity verification should remain an external compliance layer where required by:

- law
- regulated payment providers
- fiat on-ramp or off-ramp processes
- jurisdictional requirements

Legal identity is not the foundation of RESXPECT reputation.

---

## Pseudonymity and Identity Reset

Pseudonymity is permitted.

However, reputation reset should not be free.

A new Principal begins without:

- RP
- agreement history
- status
- previous outcomes
- delegated authority history
- Actor history
- established external anchors

Abandoning an established Principal therefore means abandoning the economic history attached to it.

> **Pseudonymity is allowed, but reputation reset is not free.**

---

## Validators and AI

Software Agents should not initially act as Validators.

AI may instead assist Human Validators.

```text
Agreement + Evidence
        ↓
AI Review Assistant
        ↓
Human Validator
        ↓
Decision
```

AI assistance may include:

- agreement summaries
- evidence identification
- contradiction detection
- timeline construction
- missing information detection
- suspicious-pattern detection

The Human Validator retains consequential judgement.

---

## AI-Assisted Precheck

AI may help identify:

- contradictory terms
- risky language
- impossible deliverables
- prohibited activity
- suspicious structures
- unusual agreement conditions

Human Validators remain responsible for the final judgement.

---

## AI-Assisted Reputation Validation

AI may compare:

```text
Agreement scope
      +
Submitted evidence
      +
Agreement history
```

to identify:

- evidence mismatch
- repeated-party farming
- suspicious activity
- possible collusion

AI identifies.

Human Validators decide.

---

## AI-Assisted Disputes

AI may help reconstruct a dispute into a clear timeline.

```text
What was agreed
        ↓
What was delivered
        ↓
What evidence exists
        ↓
What was rejected
        ↓
Where the parties disagree
```

The Human Validator remains responsible for the final decision.

---

## Development Roadmap

AAA should be developed incrementally.

The objective is to prove the underlying authority primitive before expanding it to more complex Organisation structures.

> **Build the authority primitive once; expand who can use it later.**

### Phase 1 — Human Principal and Agent

Phase 1 focuses on:

```text
Human Principal
     │
     ├── Direct Human Action
     │
     └── Delegated Agent
```

The goal is to prove:

- Human Principal identity
- direct actions
- Agent delegation
- permission rules
- agreement value limits
- scope limits
- expiry
- revocation
- Chain of Authority
- Agent attribution
- Principal accountability

Development sequence:

```text
Human Principal
      ↓
Direct Human Actions
      ↓
Agent Delegation
      ↓
Authority Engine
      ↓
Chain of Authority
      ↓
Agent Attribution
      ↓
Principal Accountability
```

### Phase 2 — Organisation Principal

Once the authority primitive is stable, RESXPECT may expand it to Organisations.

```text
Organisation Principal
       │
       ├── Delegated Human Actors
       └── Delegated Agents
```

Organisation support may include:

- organisation profiles
- organisation RP
- agreement analytics
- team management
- Human Actor delegation
- software Agent delegation
- treasury permissions
- authority revocation
- Actor performance history
- offboarding

The underlying authority model should remain the same.

---

## Long-Term Model

```text
                         RESXPECT

                         PRINCIPAL
                     /               \
                  Human          Organisation
                    │                 │
                    │          ┌──────┴──────┐
                    │          │             │
              Direct Actor  Human Actor    Agent
                    │          │             │
                    └──────────┴──────┬──────┘
                                     │
                                 AUTHORITY
                                     │
                                     ▼
                                 AGREEMENT
                              /               \
                         Creator Role      Runner Role
                              \               /
                               \             /
                                 OUTCOME
                                     │
                          ┌──────────┴──────────┐
                          │                     │
                  Principal Reputation    Actor Attribution
```

---

## Core Principles

AAA is built around the following principles:

> **Actors perform actions. Principals carry accountability. Authority connects the two.**

> **Delegation does not remove accountability.**

> **Privacy does not remove accountability.**

> **Accountability does not require unnecessary disclosure.**

> **Identity can be established through continuity and proof of control.**

> **Every consequential action must trace back to a persistent Principal.**

> **Reputation follows accountability. Attribution follows action.**

> **Pseudonymity is allowed, but reputation reset is not free.**

> **Build the authority primitive once; expand who can use it later.**

> **Vision expands. Architecture accommodates it. Launch scope stays narrow.**
