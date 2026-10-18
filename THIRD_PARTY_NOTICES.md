# Third-party skill sources and license scope

This repository contains skill files redistributed from the following public
repositories. The original source repositories and their licenses are listed
below.

These are separate license grants by source tree, not a single dual license
for the entire repository. Unless a file says otherwise, use the license
listed for its skill directory below and retain the applicable attribution and
notice requirements when redistributing it.

## Microsoft Azure Skills

- Source: <https://github.com/microsoft/azure-skills>
- License: MIT, reproduced verbatim in [`LICENSE-MIT`](LICENSE-MIT)
- Included paths: `skills/airunway-aks-setup/`, `skills/appinsights-instrumentation/`,
  `skills/azure-*`, `skills/discover-azure-skills/`, `skills/entra-*`,
  `skills/microsoft-foundry/`, and `skills/python-appservice-deploy/`
- Copyright: Microsoft Corporation

## Cloudflare Skills

- Source: <https://github.com/cloudflare/skills>
- License: Apache License 2.0, reproduced verbatim in [`LICENSE-APACHE-2.0`](LICENSE-APACHE-2.0)
- Included paths: `skills/agents-sdk/`, `skills/basin/`, `skills/cf-cli/`,
  `skills/cloudflare*/`, `skills/durable-objects/`, `skills/gateway-workers/`,
  `skills/k2/`, `skills/nextjs-on-cloudflare/`, `skills/sandbox-*/`,
  `skills/turnstile-spin/`, `skills/web-perf/`, `skills/workers-*/`, and
  `skills/wrangler/`
- Copyright: Cloudflare, Inc.

## Matt Pocock Skills

- Source: <https://github.com/mattpocock/skills>
- License: MIT, reproduced verbatim in [`LICENSE-MATTPOCOCK`](LICENSE-MATTPOCOCK)
- Included paths: `skills/ask-matt/`, `skills/chief-of-staff/`,
  `skills/claude-handoff/`, `skills/code-review/`, `skills/codebase-design/`,
  `skills/diagnosing-bugs/`, `skills/domain-modeling/`,
  `skills/git-guardrails-claude-code/`, `skills/grill-me/`,
  `skills/grill-with-docs/`, `skills/grilling/`, `skills/handoff/`,
  `skills/implement-spec/`, `skills/implement/`,
  `skills/improve-codebase-architecture/`, `skills/loop-me/`,
  `skills/migrate-to-shoehorn/`, `skills/pr/`, `skills/prototype/`,
  `skills/research/`, `skills/retro/`, `skills/scaffold-exercises/`,
  `skills/setup-matt-pocock-skills/`, `skills/setup-pre-commit/`,
  `skills/setup-ts-deep-modules/`, `skills/tdd/`, `skills/teach/`,
  `skills/to-questionnaire/`, `skills/to-spec/`, `skills/to-tickets/`,
  `skills/triage/`, `skills/wait-what/`, `skills/wayfinder/`,
  `skills/wizard/`, `skills/writing-beats/`, `skills/writing-for-agents/`,
  `skills/writing-fragments/`, and `skills/writing-shape/`
- Copyright: Matt Pocock

The skill contents are redistributed under their respective upstream licenses.
Changes to individual upstream files should be identified in those files or
in the repository history. This repository's collection, organization, and
any original additions are not intended to change the upstream license of the
redistributed files.

## Superpowers

- Source: <https://github.com/obra/superpowers>
- Stable release reviewed: `v7.0.0`
- Pinned commit: `bb92a77741419a4ab5f06e711a283343f1ada0c3`
- Included path: `integrations/superpowers/` as a Git submodule; its contents
  are intentionally separate from this repository's `skills/` namespace.
- Creator and maintainer attribution identified upstream: Jesse Vincent and
  Prime Radiant
- Contributors: [Superpowers contributors](https://github.com/obra/superpowers/graphs/contributors)
- License: MIT, preserved in the submodule's [`LICENSE`](integrations/superpowers/LICENSE)
- Upstream README: <https://github.com/obra/superpowers/blob/v7.0.0/README.md>

The upstream project and its original skills were not authored or maintained
by this repository's owner. The submodule preserves the upstream repository,
copyright notice, MIT license, and attribution. Any catalog entries,
organization, status tracking, or explanatory text outside the submodule are
personal documentation maintained in this repository and do not change the
upstream license or authorship.
