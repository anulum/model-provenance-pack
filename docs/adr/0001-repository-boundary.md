<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
MODEL-PROVENANCE-PACK — repository governance and provenance
-->

# Repository boundary

Status: accepted for local tooling construction.

MODEL-PROVENANCE-PACK owns model-provenance collection and pack policy interfaces once implemented. It owns its repository validators now. It does not own a second evidence signing root, a copied manifest verifier, a neuron simulator or a framework installation manager.

Initial metadata is local governance data, not a globally registered evidence schema. Planned schema identifiers remain separate from qualified identifiers. This separation allows useful infrastructure validation while domain work still awaits its complete actual implementation and evidence.

Consequences: validation commands report their exact infrastructure scope; unknown model facts remain unknown; no runtime distribution or domain entry point is declared before it exists. Later domain changes must add their real tests, documentation, dependencies and consumer qualifications in the same change.
