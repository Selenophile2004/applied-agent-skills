---
name: design-system-builder
description: "Build or extend design tokens, reusable component variants and usage rules from a visual direction or existing product screens."
---

# Design System Builder

Translate a visual direction or recurring product patterns into tokens, components and usage rules. Establish the supported surfaces, modes, languages, design or code source of truth and consuming teams.

## Build from real use

1. Inventory representative flows and repeated patterns. Note current token and component APIs, divergent variants, gaps and high-risk consumers. Prioritize components that unblock actual screens. Preserve existing names and behavior where feasible.
2. Define primitives and semantic roles for color, spacing, typography and motion. Add component tokens when a real override boundary is needed. Map roles across supported themes and density modes and document alias or fallback behavior. Example: a raw palette value can feed a foreground or background role, which a button state consumes. Verify contrast using the actual foreground and background pairs.
3. Specify each component's anatomy, properties, defaults, variants, states, events and usage boundaries. Include relevant focus, keyboard, pending, disabled, error and validation behavior. Separate visually disabled appearance from behavioral and accessibility semantics. For slots and content, define wrapping, overflow and text expansion.
4. Document responsive rules and RTL behavior, including logical spacing and deliberate treatment of directional icons. Apply reduced-motion behavior when motion is part of the component. Use native or project-standard patterns where possible.
5. Implement or specify a representative screen with the chosen components. Check realistic content, keyboard interaction, visual states and supported modes. Record exceptions and evidence. Map tokens and component names between design and code when both are part of the task.

## Deliver and evolve

Provide a token map with roles and mode mappings, a component inventory with state examples, usage guidance and verification results. For changes to an existing system, include affected consumers, old-to-new mappings, compatibility or deprecation behavior and a migration sequence. Define how drift between artifacts is identified. Consult platform documentation only when the selected implementation depends on it.
