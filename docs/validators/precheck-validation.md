# Precheck Validation

Precheck Validation is the first Validator protection layer within RESXPECT.

It operates before work begins and is designed to identify agreements that may require additional review before they proceed.

## Purpose

An agreement should not have to fail before potential issues can be considered.

Precheck provides an opportunity to review questionable or higher-risk agreements before the Runner begins work and before the agreement progresses further.

## Core Flow

**Agreement Created → Precheck → Clear / Flagged**

### Clear

If the agreement does not require further review, it can continue through the normal agreement lifecycle.

### Flagged

If the agreement is flagged, Validators can be called to review it before the agreement proceeds.

Their role is to assess the agreement using the information available at that stage and determine whether it should continue.

## What Precheck Protects

Precheck focuses on the agreement itself before work begins.

It provides an additional layer of protection around:

- Agreement safety
- Agreement clarity
- Potentially questionable activity
- Conditions that may require independent review

## Validator Role

When Validator review is required, Validators assess the agreement independently of the Creator and Runner.

Their responsibility is to review the agreement according to the protocol rather than act on behalf of either party.

## Relationship to Other Validation

Precheck Validation is separate from the other Validator functions.

**Precheck Validation**  
Protects the agreement before work begins.

**Reputation Validation**  
Protects the integrity of reputation generated through completed work.

**Dispute Resolution**  
Provides resolution when the parties disagree about an agreement outcome.

Together they provide protection across different stages of the agreement lifecycle.

## Public Specification

This document describes the public role of Precheck Validation.

Internal risk-detection methods, security controls, anti-abuse mechanisms and production implementation are not disclosed here.
