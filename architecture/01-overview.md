# Architecture Overview

RESXPECT is designed as an agreement protocol that connects agreements, funds, evidence, outcomes and reputation.

This document describes the high-level public architecture of the protocol. It does not describe the production backend, database structure, private APIs or security-sensitive infrastructure.

## High-Level Structure

Conceptually, RESXPECT is structured as:

RESXPECT  
↓  
Agreement Protocol  
↓  
USDC on Base  
↓  
Wallet and Payment Access

## Agreement Protocol

The Agreement Protocol coordinates the lifecycle of an agreement.

It is responsible conceptually for connecting:

**Agreement → Funding → Work → Evidence → Review → Outcome → Reputation**

The protocol defines the rules governing how these stages interact.

## Settlement

RESXPECT is designed around stablecoin settlement using **USDC on Base**.

Using a stable-value asset allows agreement values, payments and Validator rewards to remain understandable without requiring participants to rely on a volatile protocol token.

RESXPECT does not currently require its own token for the agreement system to function.

## Wallet Access

The protocol is intended to support different ways of accessing the same underlying payment system.

### Embedded Wallet

Users who do not already use crypto wallets can access RESXPECT through an embedded wallet experience.

The goal is to reduce the need for users to understand wallet infrastructure before using the protocol.

### Existing Wallet

Users who already have compatible wallets can connect and use them directly.

### Fiat Gateway

Users may also be able to enter the system using traditional payment methods such as card or bank payment through supported on-ramp infrastructure.

The goal is for these access methods to ultimately connect to the same underlying USDC settlement layer.

## Conceptual Flow

**RESXPECT**

↓

**Agreement Protocol**

↓

**USDC on Base**

↓

**Embedded Wallet / Existing Wallet / Fiat Gateway**

This allows the user experience to vary without changing the underlying agreement framework.

## Evidence and Reputation

Payment settlement is only one part of the architecture.

The agreement record also connects:

- Work
- Evidence
- Validation
- Outcomes
- Reputation

This allows financial settlement and reputation history to originate from the same agreement context.

## Validators

Validators provide an independent review layer across:

- Precheck Validation
- Reputation Validation
- Dispute Resolution

Validator activity interacts with the agreement system without replacing the underlying agreement between the Creator and Runner.

## Public Architecture Boundary

This repository documents the conceptual architecture and public protocol behaviour.

It intentionally does not disclose:

- Production backend implementation
- Database schemas
- Private APIs
- Authentication internals
- Wallet security implementation
- Infrastructure configuration
- Private keys or credentials
- Internal abuse-detection systems
- Security-sensitive monitoring

More components may be made public as the protocol develops and reaches appropriate stages of maturity.
