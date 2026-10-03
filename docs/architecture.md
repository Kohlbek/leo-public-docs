# LEO Household Support Platform — Public Architecture

_Public overview. Live addresses, credentials, device identifiers, household locations, private paths, and operational configuration are intentionally omitted._

## Purpose

LEO explores simple household support for an older adult together with practical caregiver diagnostics and continuity tools.

The person-facing interface and caregiver tools serve different needs and are intentionally separated.

## Prototype layout

The current prototype uses a local controller for a simple dashboard, scheduled daily printing, caregiver operations, and selected device integrations.

The public repository documents the design and lessons learned. It is **not** the live route to household devices.

## Components

- **Person-facing dashboard:** large, single-purpose controls for selected tested household and entertainment actions.
- **Daily sheet:** a one-page scheduled print containing selected household-support information.
- **Caregiver Admin:** local system status, maintenance actions, inventory refresh, and read-only diagnostic checks.
- **Visual inventory:** a configured processor requests images and writes shared inventory state. Item-specific sensing rules and human confirmation remain necessary.
- **Camera Admin:** a separate caregiver surface displaying available camera status and saved images. A new download does not prove a new camera capture.
- **Live View:** a local player workflow using bounded stream handling and cleanup. Decoding success is treated separately from visible presentation and capture freshness.
- **Entertainment control:** local device-control experiments designed to reduce multi-step remote-control tasks to a few large actions.
- **Device diagnostics:** read-only observations that help diagnose reachability or health without treating those results as proof of physical state.
- **Continuity materials:** human-readable fallback and caregiver-handoff concepts intended to reduce dependence on one operator.

## Data and control boundaries

- Device commands and account authentication remain on the private operational side.
- Shared state should have a clearly defined authoritative writer.
- Public source must not contain live credentials, household-specific device configuration, network addresses, camera images, private paths, or participant-identifying records.
- Uncertainty and freshness should remain explicit rather than being converted into false certainty.

## Design principles

1. Keep person-facing controls simple.
2. Reduce task complexity rather than merely documenting complicated workflows.
3. Separate caregiver diagnostics from person-facing interaction.
4. Preserve uncertainty in image interpretation and physical-state inference.
5. Distinguish local download time from source capture time.
6. Treat decoded media as evidence of decoder output, not proof of freshness or visible presentation.
7. Keep read-only status checks distinct from control actions.
8. Preserve manual fallback and recovery paths.
9. Prefer bounded experiments over claims of broad reliability.
10. Keep private operational configuration out of public documentation.

## Deployment boundary

This public architecture is intentionally incomplete as an operational blueprint. The live implementation, household configuration, authentication material, private logs, and device-specific settings are maintained outside the public repository.
