<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
MODEL-PROVENANCE-PACK — repository governance and provenance
-->

# Architecture

The executable surface is repository governance tooling under `tools/mpp_validation`, exposed through fixed scripts in `tools/`. It reads repository files; it does not load a plugin or executable selected by those files. JSON reports describe a named infrastructure operation.

The metadata operation precedes capability generation. A reviewed closed schema is pinned independently in executable policy. Metadata binds that schema's expected identity and governing profile, actual interpreter and raw development lock. Generation consumes accepted metadata and writes a new exclusive output. Verification reads existing bytes and never repairs them automatically.

Detailed component and trust boundaries appear in [the architecture guide](docs/ARCHITECTURE.md) and [threat model](docs/THREAT_MODEL.md). [Validation](VALIDATION.md) defines command scopes and exit meanings. No metadata or inventory pass establishes model lineage, signature validity, training reproducibility or physical execution.
