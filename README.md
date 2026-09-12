# RESXPECT Protocol

**Agreements. Evidence. Reputation.**

RESXPECT is an agreement protocol designed to create a verifiable record between people doing work and the people paying for it.

This repository contains the public specification for the RESXPECT protocol.

It explains how the protocol is designed to work without exposing security-sensitive production implementation.

## What RESXPECT Connects

A RESXPECT agreement connects:

**Agreement → Funding → Work → Evidence → Review → Outcome → Reputation**

The principle is simple:

**Reputation should not be built on what someone claims they can do, but on what they can prove they have done.**

## Start Here

The protocol documentation is best read in this order:

1. [Protocol Overview](docs/overview.md)
2. [Agreement Routes](docs/agreement-routes.md)
3. [Agreement Lifecycle](docs/agreement-lifecycle.md)
4. [Funding and Settlement](docs/funding-and-settlement.md)
5. [Evidence](docs/evidence.md)
6. [Reputation](docs/reputation/overview.md)
   - [Reputation Points](docs/reputation/reputation-points.md)
   - [Skill Trust](docs/reputation/skill-trust.md)
7. [Validators](docs/validators/overview.md)
   - [Precheck Validation](docs/validators/precheck-validation.md)
   - [Reputation Validation](docs/validators/reputation-validation.md)
   - [Dispute Resolution](docs/validators/dispute-resolution.md)
8. [Architecture Overview](architecture/overview.md)

## Agreement Routes

RESXPECT supports direct agreement creation from either side of the relationship.

An agreement may begin through:

- Creator Funded
- Creator Proposal
- Runner Proposal

Proposal links allow the intended participant to review and accept an agreement before it proceeds into the protected agreement lifecycle.

## Funding and Settlement

Protected agreements are designed around committed funds before work begins.

Once active, the agreement connects funding, work, evidence and the eventual settlement outcome.

RESXPECT is designed around **USDC on Base** for settlement.

## Evidence

Evidence connects the agreement to the work that was actually performed.

Depending on the agreement, evidence may include written submissions, images, files, source outputs or other relevant proof.

Evidence can support normal review, reputation validation and dispute resolution.

## Reputation

RESXPECT reputation is generated through agreement activity rather than standalone ratings or self-declared claims.

### Reputation Points

Reputation Points represent broader agreement history and outcomes across the protocol.

### Skill Trust

Skill Trust represents evidence-backed experience connected to a particular skill.

The two systems are related, but serve different purposes.

## Validators

Validators provide independent review across three core areas:

**Precheck Validation**  
Reviews agreements that require additional assessment before work begins.

**Reputation Validation**  
Checks whether reputation being generated is supported by the work and evidence behind it.

**Dispute Resolution**  
Provides neutral resolution when the parties to an agreement cannot reach the same conclusion about the outcome.

Together, these functions provide protection across:

**Agreement Safety → Reputation Integrity → Resolution**

## Public Specification

This repository describes the rules, architecture and intended behaviour of the RESXPECT protocol.

The production application, backend implementation, database structure, security systems, infrastructure and other security-sensitive components remain private.

The public specification may evolve as the protocol is tested, refined and implemented.

## Development Status

RESXPECT is currently under active development.

Documentation in this repository represents the current public protocol design and may change as development progresses.

---

**Website:** https://resxpect.com
