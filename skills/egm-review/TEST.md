# Test Plan: EGM Review & Subagents

Frontmatter and link checks run in `pytest tests/unit` (see [TESTING.md](../../TESTING.md)).

## Protocol Verification Checklist

When evaluating or exploring `egm-review` interactively in chat, verify:

-   **Step 1 (Intake):** Gathers `TargetFile` and optional `GoldfishContext`.
-   **Step 2 (Preset Selection):** Offers the four review presets (interactive,
    consolidated, feature spec only, implementation plan only), or maps an
    explicit `Step` argument (a preset or an individual stage 5 to 9) to one.
-   **Step 3 (Semantic Split):** Discovers the split line between Feature Spec
    and Detailed Implementation Plan.
-   **Subflows:** Properly delegates Zoom Out, Comprehension, Critic Review, and Readiness Test.
