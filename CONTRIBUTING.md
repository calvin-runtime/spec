# Contributing

Calvin is in the design stage. Contributions can improve the architecture,
challenge assumptions, define concrete contracts, or provide evidence from
integration experiments.

Start with the [README](README.md) and the
[architecture proposal](research/architecture.md). The proposal
is design research; its conceptual interfaces are not stable APIs.

## Discuss a change

Use [issues](https://github.com/calvin-runtime/spec/issues) for design questions
and substantial changes. Identify the affected section, the problem or attack
path, and the mechanism or evidence needed to resolve it.

For integration proposals, state the component roles the implementation can
supply, the guarantees it can enforce, its dependencies and configuration, and
what remains unsupported. Distinguish API compatibility from behavioral
conformance and security assurance.

Record substantial design proposals and decisions under `proposals/`. Use
`NNNN-short-title.md`, with the next unused number starting at `0001`.

## Place content by its purpose

- `research/`: architecture proposals and supporting studies. Keep proposal
  status, assumptions, and untested claims visible.
- `proposals/`: numbered changes, alternatives, and decisions.
- `specification/system/` and `specification/components/`: required system and
  component behavior, including failure handling.
- `contracts/`: machine-readable schemas and protocol bindings.
- `profiles/`: the guarantees and configuration a deployment must provide.
- `conformance/`: requirements, test cases, coverage, and evidence criteria.
- `implementations/`: implementation listings and scoped conformance evidence.

Create directories when adding content that belongs there. Keep coordinated
changes to identity, authorization, data scope, revocation, and accounting in
this repository.

## Write precise requirements

Write proposals and specifications according to
[ASD-STE100 Simplified Technical English](https://www.asd-ste100.org/).

- Use short sentences, active voice, and consistent terms.
- Separate proposed behavior, normative requirements, and demonstrated results.
- Name the component that enforces each requirement and the assumptions it needs.
- Describe failure, cancellation, revocation, retries, and uncertain outcomes
  where they affect the contract.
- Give normative requirements stable identifiers. Tests should cite those
  identifiers and declare their coverage and limits.
- State compatibility implications when changing a schema, profile, or required
  behavior. Do not treat one implementation's behavior as the standard by default.

## Submit a pull request

Describe the problem, resulting change, affected contracts, and relevant validation.
Link the related issue or proposal when one exists. Open pull requests as drafts
by default.

For document changes, check relative links, section anchors, code fences, and
formatting. Run `git diff --check` before submitting. For machine-readable
contracts or conformance work, include the checks relevant to the changed behavior.
Do not report tests that have not run or imply broader assurance than their
results support.
