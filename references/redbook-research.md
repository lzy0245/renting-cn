# Xiaohongshu / Redbook Research

Use this reference when the task needs active Xiaohongshu/Redbook rental research, note credibility screening, comment analysis, or a fallback search plan.

## Tool Use

If a Redbook MCP exposing the following read-only tools is available, use it conservatively:

- `search_notes(keywords, limit)` for keyword search.
- `get_note_content(url)` for title, author, publish time, body text, and visible metadata.
- `get_note_comments(url)` for comment signals, follow-up questions, complaints, and author replies.

Do not use comment-posting, smart-comment, lead-generation, private-message, mass-scraping, or high-frequency automation tools. If login, cookies, or browser state are required, state the account and privacy risk before continuing.

## Search Planning

Generate several focused searches instead of one broad query. Combine:

- City + district + 租房 + 避雷.
- City + neighborhood/compound + 租房.
- Compound + 噪音 / 隔音 / 潮湿 / 虫 / 物业 / 电梯 / 停车.
- District + 通勤 destination + 租房.
- Brand/apartment/operator/agency + 避雷 / 押金 / 维修 / 退租.
- Sublet keywords: 转租 / 合租 / 室友 / 二房东 / 押一付三.

Prefer recent notes from the last 3-6 months when availability, price, or agent behavior matters. Older notes can still help with stable issues such as building quality, noise source, commute, property management, and neighborhood environment.

## Sampling

Use a small, relevant sample by default:

- 5-12 search results across 2-4 queries for an initial area or compound read.
- Include both high-engagement notes and low-engagement personal experience notes.
- Retrieve comments for notes that contain warnings, strong claims, specific compounds, agencies, operators, or unusually good prices.
- Stop when repeated signals stabilize or when further search is unlikely to change the decision.

If the MCP is unavailable, return the exact search terms, what to open first, and what fields the user should copy back.

## Classification

Classify each note before using it:

- Lived experience or neighborhood review.
- Direct landlord or listing lead.
- Agent or agency listing.
- Current tenant sublet or lease transfer.
- Roommate search.
- Long-term apartment or brand promotion.
- Warning or dispute report.
- Content marketing, traffic bait, or unclear role.

Treat hidden identity, repeated cross-city rental posts, copied captions, vague location, and quick redirection to private contact as credibility risks.

## Evidence Weight

High weight:

- Repeated complaints across notes and comments.
- Specific, checkable details about noise, dampness, pests, property management, commute, repairs, deposit, or move-out.
- Author history that matches the city, compound, and claimed role.
- Comment threads where other renters confirm or add details.

Medium weight:

- Rent ranges and availability signals.
- Lifestyle convenience and neighborhood vibe.
- Single detailed personal experience note.
- Photos or videos that show exact surroundings but not authority or current availability.

Low weight:

- Polished listing posts without exact details.
- Likes, saves, follower count, or generic comments.
- Claims about ownership, authorization, payment safety, or current availability.
- "No agency fee" or "urgent cheap room" claims without verifiable total cost and signer.

## Red Flags

- Price far below nearby alternatives without a concrete reason.
- Note hides the exact role: landlord, agent, tenant, roommate, operator, or second landlord.
- Comments repeatedly ask for price, fees, availability, or location with no public answer.
- Author pushes private chat before giving basic costs and signer details.
- Same photos/copy appear across many notes, cities, or accounts.
- Payment is requested before viewing or before authority verification.

## Extraction Fields

For each useful note, extract only decision-relevant fields:

```text
搜索词：
链接/标题：
发布时间：
作者声称角色：
涉及区域/小区/品牌/中介：
主要事实或体验：
评论区重复信号：
可信度：
需要线下/合同核验：
```

## Interpretation

Use Redbook to discover what to inspect and ask, not to close the decision. Translate social signals into verification actions:

- "隔音差" -> viewing noise test at likely noisy hours.
- "退押金难" -> inspect deposit clause, handover standard, evidence requirements, and platform complaints.
- "物业差" -> check security, elevator, repairs, trash, parcels, and resident comments.
- "中介避雷" -> verify fee schedule, authorization, exact unit, and written commitments.
