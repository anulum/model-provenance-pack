<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
MODEL-PROVENANCE-PACK — repository governance and provenance
-->

# Validation tooling API

The metadata command accepts `--root` and `--json`. The inventory command additionally accepts `--mode generate|verify` and requires `--output` only for generation. All commands emit safe structured JSON. Exits are 0 for the requested scope, 2 for refusal, 3 for unavailable required inputs or tools, and 4 for invalid invocation or configuration.

Metadata validation accepts no generated inventory dependency. Inventory generation publishes deterministic new bytes; verification requires the canonical inventory and complete initial paths. A successful operation does not qualify model provenance or establish release readiness.

## Metadata acceptance

::: mpp_validation.metadata.validate_metadata

## Finite input

::: mpp_validation.inputs.read_file

::: mpp_validation.inputs.read_json

## Capability inventory

::: mpp_validation.capabilities.inventory_bytes

::: mpp_validation.capabilities.create_inventory

::: mpp_validation.capabilities.validate_capabilities

## Diagnostics

::: mpp_validation.report.Finding

::: mpp_validation.report.Report

## Command interfaces

::: mpp_validation.cli.metadata_main

::: mpp_validation.cli.inventory_main

## Source ownership and maintained tree

::: mpp_validation.provenance.validate_notice

::: mpp_validation.provenance.validate_provenance

::: mpp_validation.structure.maintained_paths

::: mpp_validation.structure.validate_structure

## YAML and workflow policy

::: mpp_validation.yaml_input.read_yaml

::: mpp_validation.workflows.validate_workflows

## Complete dependency observations

Release candidates and observed installed metadata are separate records. The hash lock covers the entire selected development graph. Exact source-builder constraints also use that lock. Recorded installation RECORD hashes are observations; relocated entry-script paths prevent treating them as universal build identities. Custom licence references retain exact source terms and do not infer permissions.

::: mpp_validation.dependency_lock.parse_direct

::: mpp_validation.dependency_lock.parse_lock

::: mpp_validation.dependency_records.Artifact

::: mpp_validation.dependency_records.LicenseEvidence

::: mpp_validation.dependency_records.LicenseSource

::: mpp_validation.dependency_records.PackageRecord

::: mpp_validation.dependency_records.read_provenance

::: mpp_validation.dependencies.verify_records

::: mpp_validation.dependencies.verify_installed

::: mpp_validation.dependencies.verify_configuration

::: mpp_validation.dependencies.validate_dependencies

::: mpp_validation.native_tools.verify_native_tools

## Actual documentation rendering

::: mpp_validation.documentation.References

::: mpp_validation.documentation.render_markdown

::: mpp_validation.documentation.inspect_markdown

::: mpp_validation.documentation.build_site

::: mpp_validation.documentation.inspect_projection

::: mpp_validation.documentation.validate_documentation

## Tool completion and scoped preflight

Every tool uses a fixed absolute executable, literal arguments and a finite deadline. Actual exits survive communication errors where observed. Output limits apply to accepted completed output; the caller reserves process memory separately. A named preflight subset reports its narrower scope. The complete operation requires the entire compiled profile. Missing tools, invalid protocol and native failures retain their real states.

::: mpp_validation.execution.ToolResult

::: mpp_validation.execution.run_tool

::: mpp_validation.preflight.Check

::: mpp_validation.preflight.Outcome

::: mpp_validation.preflight.PreflightReport

::: mpp_validation.preflight.validate_checker_report

::: mpp_validation.preflight.run_check

::: mpp_validation.preflight.run_checks

::: mpp_validation.preflight.source_payload

::: mpp_validation.validation_profile.scaffold_checks

::: mpp_validation.preflight_cli.preflight_main

## Shared command and protocol interfaces

::: mpp_validation.inputs.parse_json

::: mpp_validation.report.Refusal

::: mpp_validation.cli.Parser

::: mpp_validation.cli.check_main

::: mpp_validation.cli.emit_report

::: mpp_validation.ci_dependencies.verify_ci_dependencies

## Native workflow composition

The coordinator executes the eight complete native jobs from the maintained workflow sources. Each of four category gates requires every actual descendant result, and the stable required gate checks all four category results. The workflow policy verifies exact job equality with each source and rejects missing descendants, masked outcomes, altered commands and workflow calls. This preserves all category checks without depending on an unsupported reusable-workflow syntax. Both native syntax and unchanged pedantic workflow checks inspect the actual executable configuration; no projected input or suppressed finding is used.
