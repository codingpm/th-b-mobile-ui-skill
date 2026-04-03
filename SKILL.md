---
name: th-b-mobile-ui-skill
description: Generate mobile product prototypes that follow structured enterprise mobile UI rules through reusable page patterns, component semantics, and interaction guidance. Use when Codex needs to create mobile UI mockups, wireframes, Figma prompts, or frontend code for list pages, detail pages, forms, cards, bottom action areas, tab-based views, and app-style operational workflows.
---

# TH B Mobile UI Skill

Generate mobile interfaces that feel structured, practical, and product-ready rather than generic or overly decorative.

Treat this skill as a mobile UI rules layer. Reproduce mobile page structure, component semantics, visual hierarchy, and interaction patterns through reusable guidance rather than any specific unpublished implementation.

## Input Sufficiency Check

Before generating a mobile prototype, first check whether the request contains enough information to support a strong mobile screen structure.

Important inputs include:

- platform
- screen type
- target users
- business object
- core goal or task
- key actions
- key information blocks
- constraints or usage context

If several of these are missing, do not jump directly into screen generation. First switch to clarification mode.

When available, follow the intake behavior used by `demo-intake-skill`.
If that skill is not available, apply the same clarification behavior locally:

- ask one question at a time
- base each next question on the user's latest answer
- ask no more than 8 questions
- stop once the key structure is sufficiently clear
- summarize the result as a structured requirement brief before generating

If the request is already sufficiently clear and the platform is mobile, proceed directly to generation.

## Workflow

Follow this sequence:

1. Check whether the request is complete enough for mobile screen generation.
2. If not, clarify the requirement through short guided questioning.
3. Convert the result into a structured requirement brief.
4. Confirm the platform is mobile.
5. Identify the mobile page type.
6. Infer the dominant content pattern.
7. Apply mobile layout, spacing, and interaction rules.
8. Generate the prototype in the requested format.
9. Briefly self-check that the result still feels like a usable mobile product page.

If requirements are incomplete, infer the most likely mobile pattern instead of blocking:

- mobile list page: top nav, filters or tabs, list content, bottom actions if needed
- detail page: summary header, cards or grouped sections, action area
- form page: mobile fields, grouped inputs, sticky bottom actions
- result or state page: icon or illustration, status message, follow-up actions
- dashboard page: compact cards, segmented tabs, action shortcuts, data modules

## Naming Semantics

When the user wants the prototype to feel close to a mature mobile design system, organize the UI using these semantics:

- `Base*`: foundational mobile UI patterns such as nav bars, form controls, cards, lists, tabs, drawers, and popups
- `Business*`: domain-aware controls such as entity selectors, date ranges, category selectors, or structured filters
- `Standard*`: reusable mobile sections such as search areas, action bars, card lists, state blocks, and fixed bottom actions

Use this mental model:

- Reach for `Base*` for core page containers and primitive interactions.
- Reach for `Business*` for domain-aware inputs and workflows.
- Reach for `Standard*` for repeatable mobile page sections.

Common mobile-feeling examples:

- top navigation bar
- segmented tabs
- card list
- grouped form cells
- bottom fixed primary action
- popup or bottom sheet
- status tag or badge
- icon-based empty state
- business-aware selector

## Layout Rules

Prefer vertical flow, clear rhythm, and stable content blocks.

- Mobile pages should read top to bottom with minimal ambiguity.
- Use cards, grouped cells, list items, and section titles to organize content.
- Keep the viewport focused on the current task.
- Avoid overcrowding a single screen with too many parallel controls.
- Use fixed bottom actions for form-heavy or completion-driven workflows when needed.

Common mobile page structures:

List page:

1. top nav
2. search, tabs, or filter strip
3. list or card content
4. load-more or pagination pattern if required

Detail page:

1. top nav
2. summary card
3. grouped information blocks
4. related content
5. action area

Form page:

1. top nav
2. grouped field sections
3. helper or validation text where needed
4. bottom fixed action area

## Visual Rules

Use calm, product-oriented mobile styling.

- Favor light backgrounds and white or near-white content surfaces.
- Use one main accent color for key actions and active states.
- Prefer small to medium radius.
- Keep shadows subtle and use borders or spacing to define structure.
- Maintain readable contrast without looking heavy.
- Keep icon use purposeful.

Avoid:

- decorative gradients as main surfaces
- oversized promotional banners
- visually noisy cards
- excessive color variety
- flashy mobile landing-page aesthetics

## Color Rules

Use a restrained mobile palette.

- page background: light neutral
- card background: white or near-white
- primary text: dark neutral
- secondary text: medium neutral
- helper text: muted neutral
- border and divider: subtle neutral
- primary action: one clear accent color
- success: calm green
- warning: restrained amber
- error: restrained red

Color usage rules:

- Keep large surfaces neutral.
- Use accent color mainly for primary buttons, active tabs, links, selected states, and focus points.
- Use semantic colors for state, not decoration.
- Keep badges and tags concise and readable.

## Typography Rules

Use compact and readable mobile typography.

- Page title: concise and prominent
- Section title: clearly secondary to the page title
- Body text: readable and compact
- Helper text: smaller and lower contrast
- Action text: short and strong

Avoid:

- oversized headlines
- too many font weights
- loose spacing between text lines in dense screens

## Spacing And Shape Rules

Use compact-to-medium spacing suitable for mobile.

- cell and control spacing: tight
- card padding: medium
- section spacing: medium
- page edge padding: medium
- bottom action area padding: medium

Shape rules:

- buttons and inputs should use small to medium radius
- cards should feel stable and lightly rounded
- avoid overly pill-like shapes unless the control requires it

## Button Rules

Use a clear mobile action hierarchy.

Button hierarchy:

- primary button: the main task completion action
- secondary button: supporting action
- text button: lightweight action
- danger button: destructive action only when clearly necessary

Button usage:

- default to one primary button in the main action area
- use fixed bottom primary actions for important form or completion flows
- keep button labels short
- do not overload the screen with too many high-emphasis buttons

Button states:

- default
- hover or pressed where applicable
- active
- disabled
- loading

## Form Rules

Forms should feel natural on mobile.

- group fields into clear sections
- keep labels and values easy to scan
- prefer selectors and pickers over free text when the domain is structured
- use date ranges, pickers, and selectors for mobile-friendly input
- keep required markers visible but light
- place validation close to the field

Prefer:

- single-column form flow
- grouped card or cell sections
- sticky bottom action area when the page goal is submission

## List And Card Rules

Lists and cards are primary mobile patterns.

- keep each item focused on one information goal
- use title, supporting text, status, and actions in a stable hierarchy
- do not overload a card with too many equal-priority elements
- use tags, badges, or short labels for state
- prefer infinite scroll or load-more patterns only when appropriate

## Interaction Rules

Mobile interactions should feel explicit and efficient.

- use bottom sheets or popups for short selection tasks
- use full pages for complex forms and deeper workflows
- use segmented tabs for peer content categories
- keep gesture expectations conservative unless the user explicitly requests advanced interactions
- preserve context after save, submit, cancel, and back actions

Feedback:

- success feedback should be brief
- error feedback should explain the problem clearly
- loading feedback should appear close to the task context

## State Rules

Every meaningful mobile page should account for state:

- default
- loading
- empty
- error
- disabled where relevant
- success or completion state where relevant

Empty states should be useful and not overly decorative.

## Output Rules

Match the user’s requested medium.

If generating a prototype or design brief:

- describe the screen structure, primary action, states, and interaction flow
- mention the mobile pattern used in each section

If generating frontend code:

- keep the layout mobile-first
- preserve state handling and bottom action behavior
- keep card, list, and form hierarchy explicit

If generating Figma prompts:

- mention mobile viewport assumptions
- mention compact spacing, neutral surfaces, and clear action hierarchy
- mention cards, grouped cells, fixed bottom actions, or tab patterns when relevant

## Safety Boundary

Do not imply technical dependency on unpublished implementation details.

Focus on reproducing visible mobile design language, interaction conventions, and structural rules through generic components and clear interface guidance.

## Reusable Prompt Pattern

Use this structure when you need to restate the design intent inside the task:

```text
Generate a mobile enterprise-style prototype with compact spacing, neutral surfaces, clear action hierarchy, grouped content sections, explicit loading and empty states, and practical app-like interactions.
```

## References

Read [mobile-page-patterns.md](references/mobile-page-patterns.md) when the task needs concrete mobile page archetypes and prompt snippets.
Read [mobile-ui-spec.md](references/mobile-ui-spec.md) when the task needs more explicit color, button, form, card, and interaction rules.
