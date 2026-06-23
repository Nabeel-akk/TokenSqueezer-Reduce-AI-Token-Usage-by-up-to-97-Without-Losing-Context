# TokenSqueeze

## Purpose

TokenSqueeze is a system level optimization skill that minimizes token consumption during reasoning, memory storage, planning, tool usage, and response generation.

The skill transforms verbose human language into compact semantic representations while preserving intent, constraints, objectives, dependencies, and critical context.

Primary goal:

Reduce token usage by 80% to 97% without degrading output quality.

---

## When To Use

Activate this skill when:

✓ Context exceeds 5,000 tokens

✓ Long conversations contain repeated requirements

✓ Agent workflows repeatedly pass large prompts

✓ Cost optimization is required

✓ Multi step planning is required

✓ Large memory states must be maintained

✓ API spending must be minimized

---

## Core Directive

Before processing any request:

1. Extract intent

2. Extract constraints

3. Extract deliverables

4. Remove redundancy

5. Compress context

6. Build semantic state

7. Reason using compressed state

8. Expand only final output

Never reason on raw verbose input if a compressed representation can preserve equivalent meaning.

---

## Compression Language

### Intent

task=<objective>

Examples

task=tradebot

task=landing_page

task=research

task=automation

task=scraper

---

### Constraints

lang=py

lang=ts

framework=nextjs

db=postgres

cloud=aws

auth=true

responsive=true

---

### Output

out=code

out=report

out=analysis

out=table

out=json

out=plan

---

### Quality

q=max

q=prod

q=fast

q=secure

q=scale

---

### Memory

MEM_A={...}

MEM_B={...}

MEM_C={...}

Store reusable context inside memory blocks.

Reference blocks instead of repeating information.

---

## Semantic Abbreviations

Use these internal mappings.

RSI → RSI

MACD → MACD

Support Resistance → SR

Order Block → OB

Fair Value Gap → FVG

Liquidity Sweep → LS

Market Structure → MS

Change of Character → CHOCH

Break of Structure → BOS

Multi Timeframe → MTF

Production Ready → PROD

Documentation → DOCS

Authentication → AUTH

Database → DB

Frontend → FE

Backend → BE

Application Programming Interface → API

---

## Compression Rules

### Rule α

Remove all conversational filler.

Discard:

"Can you"

"Please"

"I was wondering"

"Would you"

"If possible"

"Could you help"

These rarely contain useful information.

---

### Rule β

Collapse repeated instructions.

Example

clean code

maintainable code

best practices

well structured code

↓

code=PRO

---

### Rule γ

Merge related constraints.

Example

dark mode

responsive

modern UI

animations

↓

ui={dark,responsive,modern,anim}

---

### Rule δ

Convert lists into arrays.

Example

RSI

MACD

ATR

Volume

EMA

↓

ind=[RSI,MACD,ATR,VOL,EMA]

---

### Rule ε

Store recurring context.

Instead of:

User prefers TypeScript

User prefers Next.js

User prefers Tailwind

User wants production code

↓

MEM_PREF={
TS,
NEXT,
TW,
PROD
}

---

## Long Context Optimization

When conversation history exceeds 10,000 tokens:

Generate compressed state.

Example

MEM_PROJECT={
tradebot,
python,
binance,
RSI,
MACD,
OB,
FVG,
risk=1%
}

Delete redundant historical wording.

Retain only semantic state.

Future reasoning must reference MEM_PROJECT.

---

## Agent Communication Protocol

Agent outputs should follow:

STATE{
task=market_scan
symbol=BTCUSD
tf=4H
ind=[RSI,MACD]
risk=low
out=signal
}

Never transmit unnecessary prose between agents.

---

## Ultra Compression Mode

Trigger:

/squeeze max

Behavior:

• Maximum abbreviation

• Symbolic encoding

• Constraint packing

• Memory referencing

• Semantic clustering

• Deduplication

Target:

95%+ reduction

Example

Original

Build a production ready Python trading bot using RSI MACD support resistance fair value gaps order blocks and multi timeframe analysis.

Compressed

task=TB
lang=PY
ind=[RSI,MACD]
smc=[SR,OB,FVG]
tf=MTF
q=PROD

---

## Response Modes

### Mode 1

Normal

Human readable response.

---

### Mode 2

Compact

Output compressed state before answer.

Example

CTX{
task=research
domain=AI
depth=high
}

---

### Mode 3

Raw

Return only compressed semantic representation.

No explanations.

---

## Success Criteria

✓ 80% to 97% token reduction

✓ No loss of critical constraints

✓ No loss of user intent

✓ Faster reasoning

✓ Lower API cost

✓ Larger effective context window

✓ Better multi agent performance

---

## Operating Principle

Every token must justify its existence.

If information can be represented in fewer tokens without losing meaning, compress it.

Reason on meaning.

Not wording.
