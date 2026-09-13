# Actor, Authority & Agent Architecture

RESXPECT is designed around a simple idea:

**Actions should always be traceable to an accountable Principal.**

As RESXPECT evolves, agreements may be created or managed not only by individuals acting directly, but also by authorised human actors and software agents acting on behalf of a Principal.

> **Actors perform actions. Principals carry accountability. Authority connects the two.**

---

## Principals

A **Principal** is the persistent accountable identity behind activity on RESXPECT.

A Principal may be:

- a Human
- an Organisation

The Principal is the identity that ultimately carries:

- reputation
- agreement history
- outcomes
- delegated authority
- accountability

Creator and Runner are not permanent identities.

They are roles a Principal takes within an agreement.

```text
Principal
    │
    ▼
Agreement
├── Creator Role
└── Runner Role
```

---

## Human Principals

Humans join RESXPECT using an alias-first model.

The alias is the public-facing identity.

The Principal underneath it is the persistent protocol identity that carries history and accountability.

A Human Principal may remain pseudonymous while still building a persistent reputation over time.

---

## Organisation Principals

Organisations use their public organisation identity by default.

```text
Organisation
    ↓
Persistent Organisation Principal
    ↓
Agreement history + reputation
```

An Organisation may authorise other Actors to act on its behalf while remaining the accountable Principal.

---

## Actors

An **Actor** is the entity that performs an action.

An Actor may be:

- the Principal acting directly
- a delegated Human Actor
- a delegated software Agent

The Actor answers:

**Who performed the action?**

The Principal answers:

**Who is accountable for it?**

---

## Authority

**Authority** defines what a delegated Actor is permitted to do on behalf of a Principal.

Authority may be limited by:

- permitted actions
- agreement value
- scope
- duration
- revocation

An Actor should never be able to exercise more authority than the Principal has granted.

---

## Chain of Authority

Every consequential delegated action should be traceable through a clear **Chain of Authority**.

```text
Action
  ↓
Actor
  ↓
Authority
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

## Delegation

A Principal may delegate authority to another Actor.

For example:

```text
Principal
    │
    ▼
Delegated Actor
    │
    ▼
Agreement Action
```

Delegated Actors may be human or software-based.

The action remains attributable to the Actor.

Accountability remains with the Principal.

> **Delegation does not remove accountability.**

---

## Reputation and Attribution

RESXPECT separates **reputation ownership** from **action attribution**.

> **Reputation follows accountability. Attribution follows action.**

The Principal receives the reputation outcome.

The Actor receives attribution for the action performed.

```text
Agreement
    │
    ├── Principal → reputation
    │
    └── Actor → attribution
```

This prevents one agreement from generating duplicate reputation while still preserving a verifiable record of who performed the work.

---

## Actor History

Actors may build a verifiable history of activity performed under delegation.

This may include:

- agreements acted in
- successful outcomes
- disputes
- failed outcomes

Actor history is separate from Principal reputation.

This allows RESXPECT to preserve both:

- the reputation of the accountable Principal
- the performance history of the Actor

---

## External Identity Anchoring

RESXPECT does not require legal identity disclosure as the foundation of protocol identity.

Humans and Organisations may optionally anchor their RESXPECT identity to established public properties such as:

- websites
- GitHub
- X or other social profiles
- public wallets

The external property should link back to the RESXPECT identity.

```text
External Website / Profile
          ↕
     RESXPECT Principal
```

This establishes **continuity and control**, not legal identity.

---

## Pseudonymity

Human Principals may remain pseudonymous.

> **Pseudonymity is allowed, but reputation reset is not free.**

A new Principal begins without:

- RP
- agreement history
- status
- previous outcomes
- delegated authority history
- Actor history
- established external anchors

Abandoning an established Principal therefore means abandoning the economic history attached to it.

RESXPECT therefore treats persistent history as an important part of accountability.

---

## Legal Identity

RESXPECT separates:

1. Principal control
2. External identity anchoring
3. Legal identity

Principal control is fundamental to the protocol.

External identity anchoring may strengthen identity continuity.

Legal identity verification remains separate and may be required where regulation, payment providers, or fiat services make it necessary.

Legal identity is not the foundation of RESXPECT reputation.

---

## Validators and AI

Software Agents should not initially make consequential Validator decisions.

AI may assist Human Validators by helping organise and analyse agreement information and evidence.

Human Validators retain final judgement.

```text
Agreement + Evidence
        ↓
AI Assistance
        ↓
Human Validator
        ↓
Decision
```

---

## Development Direction

AAA should be developed incrementally.

The first focus is:

```text
Human Principal
     │
     ├── Direct Action
     └── Delegated Agent
```

Once the authority model is proven, the same architecture can expand to Organisations:

```text
Organisation Principal
       │
       ├── Delegated Human Actors
       └── Delegated Agents
```

> **Build the authority primitive once; expand who can use it later.**

---

## Core Principles

> **Actors perform actions. Principals carry accountability. Authority connects the two.**

> **Delegation does not remove accountability.**

> **Identity can be established through continuity and proof of control.**

> **Every consequential action must trace back to a persistent Principal.**

> **Reputation follows accountability. Attribution follows action.**

> **Pseudonymity is allowed, but reputation reset is not free.**

> **Build the authority primitive once; expand who can use it later.**

> **Vision expands. Architecture accommodates it. Launch scope stays narrow.**
