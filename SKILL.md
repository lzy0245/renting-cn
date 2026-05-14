---
name: renting-cn
description: Use when the user asks for 租房.skill, 租房, 中国大陆租房决策, Xiaohongshu/Redbook rental research, active Redbook note search, rental listing screening, city or neighborhood rental comparison, apartment viewing preparation, landlord/agent communication, lease and deposit risk review, rental scam avoidance, or evaluating rent choices with social-platform evidence plus listing, market, commute, on-site, contract, and authority checks.
---

# 租房.skill

## Overview

Use this skill for mainland China residential rental decisions. Treat Xiaohongshu/Redbook as an important proactive research source for lived experience, neighborhood signals, and rental warnings, while making final recommendations only after triangulating with listing facts, market prices, commute, on-site inspection, signing authority, payment flow, and lease terms.

Default to Chinese unless the user asks otherwise.

## Core Rules

- Protect privacy before analysis. Ask users to redact names, phone numbers, ID numbers, room numbers, contract numbers, payment accounts, and screenshots containing personal data.
- Do not repeat sensitive data already present in the conversation.
- Separate facts, platform signals, inferences, missing evidence, risks, recommendation, and next actions.
- Do not treat Xiaohongshu/Redbook as the only source. Use it mainly for experience, reputation, warnings, and local context.
- Do not use social-platform content as proof of ownership, authorization, current availability, payment safety, or contract validity.
- Never recommend paying a deposit or rent before viewing, authority verification, payment-recipient verification, and written terms are clear.
- Do not provide legal conclusions. For contracts and disputes, provide risk prompts, questions, suggested clauses, and evidence-preparation steps.
- Treat rent prices, policy, platform rules, subsidy rules, residence permit rules, school or settlement benefits, and official procedures as time-sensitive. Verify with current reliable or official sources when they materially affect the decision.

## Evidence Model

Use four evidence lanes in parallel when the task requires research or judgment:

1. Xiaohongshu/Redbook: lived experience, repeated complaints, neighborhood fit, intermediary or apartment-brand reputation, deposit and maintenance stories, noise, dampness, pests, commute feel, community amenities.
2. Listing and market facts: user-provided listings, platform details, comparable rents, rent/payment cycle, fees, photos, layout, area, availability, agency or operator claims.
3. Public/current sources: maps, commute timing, official policy, local rules, rental filing, residence permit, provident fund withdrawal, school or settlement constraints.
4. Offline and documents: viewing results, videos, meter readings, ownership or authorization proof, original lease and sublet consent, payment recipient, lease terms, handover list.

## Workflow

1. Identify the stage: requirement planning, active search, listing screening, Xiaohongshu research, comparison, viewing, negotiation, signing, move-in, renewal, move-out, or dispute preparation.
2. Extract constraints: city, district, commute target, budget, whole/shared rental, room type, lease term, move-in date, payment tolerance, must-haves, deal-breakers, pets, cooking, sunlight, noise tolerance, and risk appetite.
3. If research is needed, create a source plan. Include Xiaohongshu search terms plus non-Xiaohongshu checks for price, commute, policy, listing facts, and contract/authority risks.
4. If Redbook MCP tools are available, use only read-only search and retrieval tools to gather a small, relevant sample. If unavailable, provide the search terms and manual collection plan without blocking the analysis.
5. Classify gathered content: lived experience, warning, listing lead, agency promotion, apartment-brand promotion, sublet/transfer, roommate search, neighborhood lifestyle, policy/contract issue, or unclear.
6. Triangulate. Mark which claims are supported by repeated social signals, which are listing/platform claims, which require official/current verification, and which require on-site or document verification.
7. Assess risks using low/medium/high severity. Prioritize authority, payment, safety, hidden fees, false listings, illegal partition/group-rent risk, contract ambiguity, and deposit recovery.
8. Give a recommendation tendency only if evidence is sufficient: recommended to view, view with caution, ask before viewing, not recommended for now, or insufficient information.
9. End with concrete next actions: exact search terms, questions to ask, viewing checks, contract clauses to clarify, evidence to collect, and ready-to-send wording.

## Redbook MCP Policy

When a Redbook/Xiaohongshu MCP such as `Redbook-Search-Comment-MCP2.0` is configured, use it only for:

- `search_notes`
- `get_note_content`
- `get_note_comments`

Do not use automatic commenting, smart commenting, traffic-driving comments, private-message automation, mass scraping, high-frequency polling, or account-growth workflows. If the tool asks for login, cookies, browser state, or account-sensitive data, explain the risk and let the user decide outside the skill.

## Reference Loading

- Use `references/redbook-research.md` for Xiaohongshu/Redbook search terms, MCP usage, sampling, credibility, evidence weighting, and fallback behavior.
- Use `references/rental-decision-framework.md` for source triangulation, scoring, recommendation thresholds, and multi-source decision logic.
- Use `references/viewing-checklist.md` for preparing a viewing, inspecting the unit, documenting conditions, and identifying no-pay situations.
- Use `references/contract-risk.md` for lease, authority, sublet, payment, deposit, repair, renewal, early termination, and move-out risk review.
- Use `references/output-templates.md` when the user asks for a structured report, comparison table, search plan, message wording, negotiation script, or reusable checklist.

## Output Defaults

For research-backed rental decisions, use this shape and omit irrelevant sections:

```text
检索与信息来源
- 小红书：
- 房源/平台：
- 地图/公开信息：
- 线下/合同待核验：

已知事实
平台信号与推断
主要风险
- 高：
- 中：
- 低：

建议倾向
下一步行动
可直接发送的话术/清单
```

For simple questions, answer directly and include only the needed caveats and next actions.
