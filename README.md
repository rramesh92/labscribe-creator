# Lab Assistant Pro

Prompt 1: Natural-language lab blueprinting agent (Admin / Authoring view)

Use this prompt in your UI/prototype tool to generate a new screen under the same design system as the admin-events URL (same nav, typography, spacing, cards, etc.).magicpatterns

Prompt:
Create a new admin-side “Lab Blueprint Assistant” screen for the Hatsize portal, matching the visual style, layout, and components from this reference URL: https://ascend-mocks.vinod-patil-302.workers.dev/hatsize/portal/admin-events (same top navigation, left sidebar structure, typography scale, card styles, button treatments, spacing, and color tokens).

Layout requirements:

Keep the existing top app bar and side navigation. Highlight a new nav item called “AI Lab Assistant” under the authoring/administration section.

The main content area is split into two columns:

Left column (approx. 40%): “Input & Interaction” panel.

Right column (approx. 60%): “Generated Blueprint” panel.



Left column: Input & Interaction panel

Add a card titled “Describe your lab in plain language”.

Inside the card, show:

A mic icon button labelled “Hold to speak” at the left, a text input placeholder “Describe the lab you want to create…” filling the rest of the row, and a smaller “Submit” button on the right.

When mic is “active”, animate a pulsing ring around the mic icon and show a subtle “Listening…” chip.

Under the input, show a 2–3 line example transcript to illustrate the NLP interaction, such as greyed-out text appearing line by line:

“Instructor: ‘I want a 45-minute beginner lab on SQL injection using a vulnerable web app. Students should learn how to exploit a basic login form and then patch it.’”

“Assistant: ‘Got it. I’ll propose a lab with 5 steps, 1 VM template, and auto-grading for final screenshots. Review the blueprint on the right.’”



Include a small “Preset prompts” section (chips) like “CCNA VLAN lab”, “Linux hardening”, “Basic SQL injection”.



Right column: Generated Blueprint panel

Add a card titled “Draft Lab Blueprint”.

Inside the card, show a structured, read-only preview with the following sections, each styled like neatly separated subpanels:

“Lab Title” (editable text field with a generated title, e.g., “Intro to SQL Injection on Login Forms”).

“Learning Objectives” (bullet list with 3–4 generated objectives).

“Lab Duration & Difficulty” (two pill-style badges like “45 minutes” and “Beginner”).

“Environment & Topology” (simple diagram-like list: 1 vulnerable web server VM, 1 database, 1 attacker machine; each as item rows with icons).

“Step-by-step Flow” (numbered list of 5 steps, each step row includes: step title, short description, and a small “Expected outcome” tag).

“Assessment & Grading Rubric” (table-style block: columns for “Deliverable”, “How it is checked”, “Weight”).



At the bottom of the card, add primary and secondary actions:

Primary: “Accept & Create Lab Template”.

Secondary: “Edit Details” and “Regenerate Blueprint”.



States and microcopy

Show a default state with an empty input and a subtle tip text: “Use voice or text to describe your lab. The assistant will propose a complete blueprint you can refine.”

Show a “loading” state in the right panel when the user hits “Submit” or finishes speaking: a skeleton for each section plus a spinner with the label “Drafting your lab blueprint…”.

Overall tone: professional, minimal, enterprise SaaS. Prioritize clarity and hierarchy: lab description input on the left, generated lab blueprint on the right, with well-labelled sections. The screen should look like a natural new section of the existing Hatsize portal, not a separate app.

This project was built with [Lovable](https://lovable.dev).

**Live app**: https://labscribe-creator.lovable.app

## Build with Lovable

Continue developing this project in the [Lovable editor](https://lovable.dev/projects/766468ca-2967-4556-92f6-ea2629d43a8a).

- **Ship faster**: describe what you want to build and Lovable handles the code.
- **Stay in sync**: every change made in Lovable is committed straight to this repository.
- **Full ownership**: this code is yours. Push to `main` on GitHub and your changes sync back into Lovable, ready for your next prompt.

## Development

Prefer working locally? You need Node.js and npm — [install with nvm](https://github.com/nvm-sh/nvm#installing-and-updating).

```sh
git clone <this-repository-url>
cd <repository-name>
npm i
npm run dev
```
