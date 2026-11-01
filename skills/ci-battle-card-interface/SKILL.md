---
name: "ci-battle-card-interface"
description: "Use for Sweet Security competitive-intel work: answering questions from the Master CI sheet, and building or updating the CI battle card artifact (battle card, Ask the CI chat, decision board) for any competitor."
---

# CI battle card interface

This skill covers two jobs for Sweet Security's competitive intelligence (CI) work:

1. **Answering**: any question in this Project about the competitor or how Sweet compares.
2. **Building and updating the artifact**: the "Sweet Security CI Interface" web page with three tabs.

It works for any competitor. Throughout, `COMPETITOR` is the competitor's name, `COMP` is its column code in the Master CI sheet (for example `UPW` for Upwind), and `SWT` is Sweet Security's column. Read the column codes from the sheet's header row, never assume them.

---

## Source of truth (applies to both jobs)

- The Master CI sheet (Google Sheet linked in the Project's context) is the only source. Read it live before every answer and every build, through the Google Sheets connector (`get_values`, range `Sheet1!A1:F80` or wider if the sheet has grown).
- The sheet has numbered rows (questions), a category column and one column per company. Unnumbered rows (vendors considered, launches to monitor, analyst mentions, executive hires, messaging change, humble brags) count too.
- The top of the sheet holds a "Last updated" date. Note it, and mention it if the information may be out of date.
- Use only what is in the sheet. Don't search the web or use outside knowledge unless the person asks.
- If the sheet doesn't cover something, say "Not in the competitive intel" and suggest which row should be researched.
- In anything a person reads, call it "the competitive intel", never "the sheet".
- Never invent customers, numbers, quotes, prices or dates.
- Write competitor claims as claims ("COMPETITOR claims...") unless the intel shows independent proof.
- Never attack the competitor. Every response redirects to Sweet's own strengths and public proof.
- Never recommend Sweet make a claim just because the competitor makes it.

### Labels

Label every point:
- **FACT**: stated in the intel with a source.
- **INTERPRETATION**: a reading of the facts.
- **HYPOTHESIS**: a reasonable guess the intel doesn't prove. Product, pricing and strategy moves are always HYPOTHESIS, because the intel holds public evidence only, not Sweet's internal data.
- **No public proof**: when Sweet has no public evidence for something, say "No public proof yet - do not claim" and offer a discovery question instead.

---

## Job 1: Answering

### Follow-up questions

Ask before answering open or strategic requests: call or deal prep, objection handling, account or renewal situations, content or campaign ideas, product or roadmap questions, and business decisions. Don't ask for simple factual questions. If the person says "skip" or "just answer", answer straight away and list the assumptions made.

**Step 1, role.** If the role is clear, confirm it as the first line ("I'm assuming you're in sales - correct me if not."). If not, ask first: "What's your role? Sales / Content / Product marketing / Product / Customer success / Leadership / Other." Remember the role for the rest of the chat.

**Step 2, questions.** Only ask what would change the answer. Ask at most 6 questions plus the role line, all in one message, with options where possible. Never ask about anything already said, and never assume something you could have asked (for example the product of interest). Prioritise in this order: the goal, the situation, specifics that change the answer, then format or deadline only if it matters.

Always end with one optional context question that fits the role:
- Sales: "Anything else that would help me tailor this? For example: deal size, timeline, other vendors on the shortlist, or concerns they've raised. (optional)"
- Customer success: "Anything else that would help? For example: what they've said about COMPETITOR, recent support issues, or who the decision-maker is. (optional)"
- Content: "Anything else that would help? For example: a topic you already have in mind, a deadline, or content that has worked before. (optional)"
- Other roles: "Anything else that would help me tailor this? (optional)"

Question bank:
- **Sales:** always ask company size (SMB / mid-market / enterprise), industry, Sweet product of interest (Runtime CNAPP / AI Security Platform / both / not sure) and main problem (alert noise / runtime threats / AI agents / compliance / other). Next, who is on the call (CISO / SecOps / DevSecOps or cloud security / AppSec / not sure). Only if there's room, ask what they've seen from the competitor (demo / POC / pricing / not sure).
- **Customer success:** whether the customer is at risk of switching or comparing at renewal; account size; which Sweet product they use; main complaint or unmet need; rough renewal date.
- **Content:** audience role; funnel stage (awareness / consideration / decision); format (blog / LinkedIn post / email / webinar / other); goal (traffic / leads / sales enablement / thought leadership).
- **Product marketing:** task (positioning / messaging / launch / competitive response / enablement); audience or segment; trigger (a competitor launch, campaign or claim?).
- **Product:** area (feature gap / roadmap priority / integration / pricing or packaging); which competitor capability prompted it; segment affected.
- **Leadership:** decision area (messaging / product / pricing / sales / partnerships); time frame (this quarter / this year); what success looks like.

**Step 3, answer.** If the answers are clear, answer. Ask a second round only if something critical is missing, at most 2 more questions. Treat "nothing", "not sure", "don't know" or a skipped question as UNKNOWN and never state it as fact (write "We don't know if COMPETITOR has engaged them yet", not "COMPETITOR hasn't engaged them"). Say when you assume something. Cite extra context the person gives as "from you". If the intel has nothing specific to their situation, say so and label tailored advice HYPOTHESIS.

### Answer format

- **Simple factual questions:** at most 3 short sentences plus one line of sources. No tables, context or caveats unless asked. End with "Want more detail?"
- **Open or strategic questions: short version first.**
  1. A short version: 3-5 bullets, no tables, with key sources in each line.
  2. The longer version's sections as titles only, for example "Longer version: 1. What to say  2. What NOT to say  3. COMPETITOR's likely angle and how to respond  4. Discovery questions".
  3. Ask: "Which one should I expand, or should I show the full version?"
  4. Give only the section picked, or all sections if they ask for the full version.
- In chat answers, cite every point with company, row number and row name ("COMP, row 20: use cases") plus the source name if the intel has one. Row citations belong in chat answers only, never on the artifact page.
- Tailor to the role. For sales, the longer version covers: what to say, what NOT to say, Sweet's public proof points, the competitor's likely angle and how to respond, and discovery questions.

### Battle card format

Keep it to one page, objection handling first:

1. **Objection handling** (the most important section): 4-6 likely objections, most common first, based on the competitor's claims, ads and review praise. Each has: the objection in the prospect's words; "Say this" (1-2 sentences a rep can read out word for word); a proof point (Sweet's own public evidence); and a one-line technical counter for technical buyers. Every "Say this" needs a proof point. If there is none, write "No public proof yet - do not claim" and give a discovery question instead.
2. How COMPETITOR positions itself (exact quotes)
3. Where COMPETITOR is strong
4. Where COMPETITOR customers report friction (theme, number of reviews, platform, when)
5. Claims Sweet Security should not make
6. Discovery questions for sales reps
7. Sources: only the Master CI Brief link with its last-updated date

Do not include a "Changes in the last 90 days" section.

### Decision board format

For "what should Sweet do" questions, use short version first.

**Short version:** 4-5 bullets. The first bullet has the label **MY RECOMMENDATION** and is one sentence:
- Third person: never "I", "we" or "my", and never starting with "My recommendation:".
- The single most important product marketing move (positioning, messaging, content, sales enablement or launches), chosen for the strongest evidence and biggest impact in the intel.
- Focused heavily on what Sweet Security should do, following this pattern: "COMPETITOR [what it focuses on], so Sweet Security should [focus on X], such as [concrete examples], and [how to back it up]."
- Built on Sweet's own strengths and gaps, never by copying the competitor's claims.

Example (Upwind): "Upwind leads with visibility, so Sweet Security should lead with what it does at runtime that a buyer can watch happen, such as virtual patching, one-click containment and blocking a rogue AI agent's action, and back it with named customer stories instead of headline percentages Sweet's own reviews don't support."

The other 3-4 bullets are labelled FACT, INTERPRETATION or HYPOTHESIS.

**Recommendations:** 6-8, each with:
- the decision in one line
- the evidence
- confidence (high / medium / low)
- owner (Product marketing, Sales, Content, Product or Leadership)
- how to measure success

---

## Job 2: Building and updating the artifact

### Before building

- Load the `artifact-design` and `artifact-capabilities` skills before writing the page.
- Read the live sheet first and build the default content from it.
- To update an existing artifact, read it first (or republish the same file path in the same session). Change only what was asked and keep everything else exactly as it is.
- After each update, tell the person in one line what changed.

### Page structure

One self-contained HTML page:
- `<title>` Sweet vs COMPETITOR CI
- Visible title (bold serif): **Sweet Security CI Interface**

**Header (sticky):**
- a thin lime-to-yellow gradient strip on top (#D6F53F to #F1F474)
- the title on the left
- on the right, a small "Last updated [date]" pill (the intel date the tabs were built from) and a quieter "Loaded [date/time]" for the live read
- a status banner (hidden when empty) for update and error messages
- three pill tabs, hash-routed: Battle card (default), Ask the CI (`#chat`), Decision board (`#decisions`)

### Battle card tab

- A clickable table of contents above section 1, listing the seven sections: 1. Objection handling, 2. How COMPETITOR positions itself, 3. Where COMPETITOR is strong, 4. Where COMPETITOR customers report friction, 5. Claims Sweet Security should not make, 6. Discovery questions, 7. Sources. Each link smooth-scrolls to its section (instant if the viewer prefers reduced motion). Section `scroll-margin-top` clears the sticky header. Show a compact wrapping row of pills on desktop and two columns on mobile.
- **1 · Objection handling:** a grid of soft cards (2 columns on desktop, 1 on mobile). Each card has the objection as a serif title in quotes; "Say this" in a lime box with a pill Copy button (`navigator.clipboard.writeText` inside the click; on failure, select the text and show "Selected, press Ctrl+C"); then a smaller "Proof point" and "Technical counter" in muted text. A note underneath explains that responses redirect to Sweet's own proof. There's no "most common first" eyebrow.
- **2 · Positioning:** the competitor's exact quotes as soft serif blockquotes.
- **3 · Strengths:** a list with label pills.
- **4 · Friction:** a table in a card (theme, review count with a small lime bar, what reviewers say, when), followed by an INTERPRETATION note ending "Use these as discovery questions, never as attacks."
- **5 · Claims Sweet Security should not make:** a list with a "Don't claim" pill.
- **6 · Discovery questions:** a numbered list.
- **7 · Sources:** only one line: `[Master CI Brief](sheet URL) (competitive intel, last updated [date])`.

**No row citations anywhere on the Battle card or Decision board.** Remove every "SWT, row 10…", "COMP rows 5, 7", "(SWT row 6)" and similar reference, including inside evidence text. Keep the label pills and the Sources line. Run all rendered text through a citation-stripping function so rebuilt content can never bring citations back.

### Decision board tab

- A short-version card: a serif "Short version" heading, then the 4-5 bullets, with the **MY RECOMMENDATION** bullet first. Its pill has a lime background with near-black text; the other bullets use the normal label pills. Below the bullets, a note that product, pricing and strategy moves are HYPOTHESIS.
- A "Recommendations" heading with owner filter pills (All + each owner).
- Recommendation cards (`<details>`): the decision as a serif title with a chevron, and pills for label, owner and confidence (high = green, medium = blue, low = red tint). Clicking a card expands its Evidence, Owner, Confidence and Measure success.

### Ask the CI tab (chat)

- The whole tab fits on one screen, with no page scrolling. The chat card's height is `100dvh` minus the measured header height (track the header with a `ResizeObserver` into a `--hdr` variable). Only the messages area scrolls; the input is always visible at the bottom.
- Status bar: the source line ("Source: live Master CI · read [date time]", or the reason it's using the embedded copy), a "New chat" pill and a small round "i" button.
- The "i" button opens a popover with the label legend and a Data box: "Answers read the live competitive intel. Click Refresh now if you just updated it." plus a **Refresh now** button. The popover closes on an outside click or Escape.
- Suggested questions sit as small, horizontally scrolling chips above the input. Include at least one factual question, one pricing question, one call-prep question, one objection and one "what should Sweet do" question.
- The input is a rounded textarea (Enter sends, Shift+Enter adds a new line), with pill Ask and Stop buttons.
- The chat uses the `sample` capability with the full answering rules (Job 1) as a leading user turn, followed by the live intel text, or the embedded snapshot if the live read fails. Use `cache: false`, stream with `onText`, keep the last ~16 turns, and render a small safe Markdown subset (paragraphs, lists, headings, tables, bold, code). FACT, INTERPRETATION and HYPOTHESIS words become pills. Map each sample error code to plain viewer copy.
- Embed a condensed copy of the whole sheet as the fallback snapshot, keeping numbers, quotes and dates as written.

### Capabilities

Declare `{sample: {}, mcp: {servers: [{server: "Google Sheets", tools: ["get_values"]}]}, db: {}}`. Also use the built-in `permissions`.

### Auto-update logic (Battle card and Decision board)

1. **On load:** render the embedded default build, then read `db.doc("ci/build")`. If it holds `{format: "v1", lastUpdated, builtAt, data}` with valid data, render that instead.
2. **Read the live sheet** (`get_values`), take its "Last updated" date, and compare it with the build's `lastUpdated`, normalised to YYYY-MM-DD.
3. **Same date, or the sheet is older:** show the current version and clear the banner.
4. **Sheet is newer:** show "Updating from the latest competitive intel…" and call `sample.json` with `modelTier: "complex"` and `cache: false`. Send build rules covering the battle card and decision board rules above, an explicit "NEVER include row citations", the MY RECOMMENDATION rules and pattern, and the exact JSON shape. Also send the previous version's text and the live intel.
5. **Validate the reply:** 4-6 objections, each with an objection, "say", proof and tech; non-empty positioning, strengths, friction, don't-claims, discovery and short lists; 3 or more decisions, each with a title, evidence, owner and measure. Move the MY RECOMMENDATION bullet first and strip any "My recommendation:" prefix. Render, then save to `ci/build` so it only rebuilds when the sheet changes.
6. **Sheet can't be read:** show the last saved version with "Couldn't reach the live competitive intel. Showing the version from [date]." plus a **Manage permissions** pill (`permissions.manage()`; when the panel closes, re-run the check; if it fails to open, tell the viewer to use the artifact's Permissions menu and reload).
7. **Rebuild fails:** keep the current version and say "Couldn't rebuild from the latest competitive intel. Showing the version from [date]."
8. **Refresh now** forces a fresh live read (cache refresh) and rebuilds all three tabs: chat data, Battle card and Decision board.

Rebuild JSON shape (plain text inside strings, no HTML or Markdown):

```json
{
 "objections":[{"objection":"...","say":"...","proof":[{"label":"FACT|INTERPRETATION|HYPOTHESIS|NO PUBLIC PROOF","text":"..."}],"tech":[{"text":"..."}]}],
 "positioning":[{"quote":"exact competitor wording"}],
 "strengths":[{"label":"FACT","text":"..."}],
 "friction":[{"theme":"...","reviews":6,"quote":"...","when":"..."}],
 "frictionNote":{"label":"INTERPRETATION","text":"..."},
 "noclaims":[{"claim":"...","why":"..."}],
 "discovery":["..."],
 "short":[{"label":"MY RECOMMENDATION","text":"COMPETITOR ..., so Sweet Security should ..."},{"label":"FACT|INTERPRETATION|HYPOTHESIS","text":"..."}],
 "decisions":[{"title":"...","label":"FACT|INTERPRETATION|HYPOTHESIS","confidence":"high|medium|low","owner":"Product marketing","evidence":"...","measure":"..."}]
}
```

### Connector error copy (live read)

- `needs_reauth`: reconnect Google Sheets in claude.ai Settings → Connectors.
- `server_not_connected`: add the Google Sheets connector.
- `not_in_manifest`: Google Sheets access was declined for this page.
- `approval_required`: approval needed; claude.ai asks when you press Refresh now.
- `tool_error`: check you have access to the sheet.
- `server_unavailable`: try Refresh now in a moment.
- Outside claude.ai (`window.claude` missing): "open on claude.ai for live data and chat".

### Sweet Security design

- **Colours:** background #FFFFFF; text and buttons #0F190A (near-black green); accent lime #D6F53F, optionally with #F1F474 in the header gradient.
- **Lime only as a background highlight**, always with #0F190A text on top: the active tab, the "Say this" box, table-of-contents hover, chip hover, the friction bars and the MY RECOMMENDATION pill. Never put lime text on white.
- **Buttons:** pill-shaped, #0F190A background with white text in light mode. In dark mode, white with #0F190A text.
- **Dark mode:** background #0F190A, text white, the same lime accent. Define every colour as a token on `:root`, redefine it under `prefers-color-scheme: dark` (guarded by `:root:not([data-theme="light"])`) and again under `[data-theme="dark"]`, and give `body` an explicit background.
- **Fonts** (Google Fonts): Playfair Display (700/800) for the title, section headings, card titles and quotes; Inter for everything else. No monospace and no ALL-CAPS labels, except the label pills themselves (FACT / INTERPRETATION / HYPOTHESIS / MY RECOMMENDATION).
- **Layout:** soft rounded cards (around 18px radius) with light shadows, few borders and generous white space. Label pills are small and soft-tinted: FACT green, INTERPRETATION blue, HYPOTHESIS purple, no public proof / don't claim red.
- **Mobile:** a 16px side gutter using `max(16px, env(safe-area-inset-*))`, grids collapse to one column, the table of contents shows two columns, and nothing scrolls sideways except tables inside their own scroll container.

### Check before publishing

- Syntax-check the page script.
- Check the defaults render: 4-6 objection cards, 7 table-of-contents links, the decision cards, and no row citations in the Battle card or Decision board text.
- Then publish to the same artifact and report the change in one line.
