<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
MODEL-PROVENANCE-PACK — repository governance and provenance
-->

# Roadmap

Implemented tooling validates closed repository metadata and provides deterministic capability inventory construction. The initial repository foundation also requires source, workflow, dependency, rendered-documentation and complete preflight validation; these requirements do not confer model-processing capability by themselves.

Planned domain work includes collection of explicit model facts, assembly of referenced evidence, policy-based offline verification and human-readable pack rendering. Intended commands are `init`, `collect`, `sign`, `verify`, `inspect` and `render`; they are not available commands in the current tooling.

Domain acceptance requires the selected original schema, complete required fields, reproducible encodings and numeric variants, independent reference cases, actual producer/consumer integration and the sole qualified evidence-manifest implementation for signing and verification. Unknown facts remain unknown rather than inferred from filenames. Attachments are references with verified identity; optional frameworks are not imported merely to inspect a pack.
