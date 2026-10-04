---
name: demo-review
description: Review an AI-built prototype against its promised user task, checking actual behavior and distinguishing implemented features from mockups. Use when a demo is ready to try or its claimed readiness is unclear.
---

# Demo review

Read the user's brief and identify the main task. Evaluate the current result against that task and their explicit choices, without expanding the feature list.

Use [the review sheet](../../templates/demo-review.md) when useful. Try a normal input and an input that omits or contradicts an important detail. Review the actual output, including whether invented business facts or simulated features appear real.

For an action that can send, book, pay or change external state, test its preview or a permitted test environment. Do not perform a live action merely to prove the demo works; use existing user authorization and record what was actually tested.

If tools allow, open the implementation at a phone width and try the full main path. Check an error or empty state when relevant. Do not turn unavailable tools into a fabricated pass: record NOT RUN and its specific consequence.

Report the most important failure first, then fixes needed for the intended demo. Keep optional improvements separate. After a fix, repeat the affected check and save evidence of the observed result. Avoid universal claims that an app is ready for all users from a single successful example.
