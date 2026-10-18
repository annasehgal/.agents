# Superpowers integration catalog

This catalog records the Superpowers integrations documented by the upstream
project. The commands below are reference instructions only. They were not
executed as part of adding this repository integration.

## Repository snapshot

- Upstream repository: <https://github.com/obra/superpowers>
- Stable release reviewed: `v7.0.0`
- Pinned commit: `bb92a77741419a4ab5f06e711a283343f1ada0c3`
- Release page: <https://github.com/obra/superpowers/releases/tag/v7.0.0>
- Release notes: <https://github.com/obra/superpowers/blob/v7.0.0/RELEASE-NOTES.md>
- Review date: 2026-10-18
- Local integration: Git submodule at [`integrations/superpowers`](../../integrations/superpowers)

The upstream README says Superpowers must be installed separately for each
harness. This repository only records and pins the upstream source; it does not
install Superpowers into any coding agent.

## Shared capabilities

The upstream skill library at this pinned release contains:

- `brainstorming` — clarify intent and requirements before building.
- `writing-plans` — produce detailed implementation plans.
- `test-driven-development` — enforce RED-GREEN-REFACTOR.
- `systematic-debugging` — investigate root causes before fixes.
- `verification-before-completion` — verify results before claiming completion.
- `diagnosing-superpowers` — inspect why a Superpowers workflow behaved unexpectedly.
- `using-git-worktrees` — isolate work on branches and worktrees.
- `dispatching-parallel-agents` — coordinate concurrent subagents.
- `subagent-driven-development` — implement planned tasks with staged review.
- `executing-plans` — execute plans inline with review.
- `requesting-code-review` — request review against the plan.
- `receiving-code-review` — process review feedback.
- `finishing-a-development-branch` — verify and complete a branch.
- `writing-skills` — author and test new skills.
- `using-superpowers` — bootstrap and explain the skill system.

The upstream porting guide distinguishes the shared skills from each harness's
bootstrap and tool mapping. Similar local skill names are not treated as
duplicates unless their behavior has been compared directly.

## Integration status

| Integration | Investigated | Documented | Integrated into this repository | Installed locally | Tested successfully |
|---|---:|---:|---:|---:|---:|
| Claude Code | Yes | Yes | Yes | No | No |
| Antigravity | Yes | Yes | Yes | No | No |
| Codex App | Yes | Yes | Yes | No | No |
| Codex CLI | Yes | Yes | Yes | No | No |
| Cursor | Yes | Yes | Yes | No | No |
| Devin CLI | Yes | Yes | Yes | No | No |
| Factory Droid | Yes | Yes | Yes | No | No |
| Gemini CLI | Yes | Yes | Yes | No | No |
| GitHub Copilot CLI | Yes | Yes | Yes | No | No |
| Grok Build CLI | Yes | Yes | Yes | No | No |
| Kimi Code | Yes | Yes | Yes | No | No |
| OpenCode | Yes | Yes | Yes | No | No |
| Pi | Yes | Yes | Yes | No | No |
| Qwen Code | Yes | Yes | Yes | No | No |
| Hermes Agent | Yes | Yes | Yes | No | No |
| Muse | Yes | Yes | Yes | No | No |

“Integrated into this repository” means that the pinned upstream source and
the corresponding catalog entry are tracked here. It does not mean that any
harness plugin or extension has been installed.

## Supported integrations

The official source for the installation commands is the pinned upstream
[README installation section](https://github.com/obra/superpowers/blob/v7.0.0/README.md#installation).
Where upstream does not document an update or uninstall command, this catalog
says so explicitly.

### Claude Code

- Official instructions: [upstream README](https://github.com/obra/superpowers/blob/v7.0.0/README.md#claude-code)
- Mechanism: official Claude plugin marketplace, or the Superpowers marketplace.
- Prerequisite: Claude Code. Upstream does not state a minimum version.
- Install:

  ```text
  /plugin install superpowers@claude-plugins-official
  ```

  Alternative:

  ```text
  /plugin marketplace add obra/superpowers-marketplace
  /plugin install superpowers@superpowers-marketplace
  ```

- Capabilities: shared library above, delivered through the Claude plugin bootstrap.
- Update: not specified in the upstream README.
- Uninstall: not specified in the upstream README.

### Antigravity

- Official instructions: [upstream README](https://github.com/obra/superpowers/blob/v7.0.0/README.md#antigravity)
- Mechanism: Git URL plugin install.
- Prerequisite: Antigravity with the `agy` command. Upstream does not state a minimum version.
- Install:

  ```bash
  agy plugin install https://github.com/obra/superpowers
  ```

- Capabilities: shared library; Antigravity exposes installed skill descriptions and uses the `using-superpowers` description to prompt bootstrap loading. The v7.0.0 release adds a native Antigravity manifest.
- Update: reinstall using the same command.
- Uninstall: not specified in the upstream README.

### Codex App

- Official instructions: [upstream README](https://github.com/obra/superpowers/blob/v7.0.0/README.md#codex-app)
- Mechanism: official Codex plugin marketplace in the desktop app.
- Prerequisite: Codex App. Upstream does not state a minimum version.
- Install: open Plugins in the sidebar, find `Superpowers` in Coding, and click `+`.
- Capabilities: shared library through the Codex plugin package; the README does not provide a separate App-specific capability matrix.
- Update: not specified in the upstream README.
- Uninstall: not specified in the upstream README.

### Codex CLI

- Official instructions: [upstream README](https://github.com/obra/superpowers/blob/v7.0.0/README.md#codex-cli)
- Mechanism: official Codex plugin marketplace.
- Prerequisite: Codex CLI. Upstream does not state a minimum version in the README.
- Install: open `/plugins`, search for `superpowers`, and select `Install Plugin`.
- Capabilities: shared library through the Codex plugin package. Subagent behavior and tool availability depend on the Codex CLI/plugin environment; no additional requirement is stated in the v7.0.0 README.
- Update: not specified in the upstream README.
- Uninstall: not specified in the upstream README.

### Cursor

- Official instructions: [upstream README](https://github.com/obra/superpowers/blob/v7.0.0/README.md#cursor)
- Mechanism: Cursor plugin marketplace.
- Prerequisite: Cursor with Agent chat. Upstream does not state a minimum version.
- Install:

  ```text
  /add-plugin superpowers
  ```

  Marketplace search for `superpowers` is also documented.
- Capabilities: shared library through the Cursor plugin and session-start hook.
- Update: not specified in the upstream README.
- Uninstall: not specified in the upstream README.

### Devin CLI

- Official instructions: [upstream README](https://github.com/obra/superpowers/blob/v7.0.0/README.md#devin-cli)
- Mechanism: plugin installed from the upstream repository.
- Prerequisite: Devin CLI. Upstream does not state a minimum version.
- Install:

  ```bash
  devin plugins install obra/superpowers
  ```

- Capabilities: shared library; v6.3.0 release notes state that skills auto-trigger at session start.
- Update:

  ```bash
  devin plugins update superpowers
  ```

- Uninstall: not specified in the upstream README.

### Factory Droid

- Official instructions: [upstream README](https://github.com/obra/superpowers/blob/v7.0.0/README.md#factory-droid)
- Mechanism: Droid plugin marketplace using the upstream Git repository.
- Prerequisite: Factory Droid. Upstream does not state a minimum version.
- Install:

  ```bash
  droid plugin marketplace add https://github.com/obra/superpowers
  droid plugin install superpowers@superpowers
  ```

- Capabilities: the upstream porting guide says Factory Droid consumes the Claude Code plugin and needs no separate Superpowers harness directory.
- Update: not specified in the upstream README.
- Uninstall: not specified in the upstream README.

### Gemini CLI

- Official instructions: [upstream README](https://github.com/obra/superpowers/blob/v7.0.0/README.md#gemini-cli)
- Mechanism: Gemini extension installed from a Git URL.
- Prerequisite: Gemini CLI. Upstream does not state a minimum version.
- Install:

  ```bash
  gemini extensions install https://github.com/obra/superpowers
  ```

- Capabilities: shared library through the Gemini extension and its context/bootstrap integration.
- Update:

  ```bash
  gemini extensions update superpowers
  ```

- Uninstall: not specified in the upstream README.

### GitHub Copilot CLI

- Official instructions: [upstream README](https://github.com/obra/superpowers/blob/v7.0.0/README.md#github-copilot-cli)
- Mechanism: Copilot plugin marketplace.
- Prerequisite: GitHub Copilot CLI. Upstream does not state a minimum version.
- Install:

  ```bash
  copilot plugin marketplace add obra/superpowers-marketplace
  copilot plugin install superpowers@superpowers-marketplace
  ```

- Capabilities: shared library through the Copilot plugin and shell-hook bootstrap.
- Update: not specified in the upstream README.
- Uninstall: not specified in the upstream README.

### Grok Build CLI

- Official instructions: [upstream README](https://github.com/obra/superpowers/blob/v7.0.0/README.md#grok-build-cli)
- Mechanism: official xAI plugin marketplace.
- Prerequisite: Grok Build CLI. Upstream does not state a minimum version.
- Install:

  ```bash
  grok plugin install superpowers@xai-official --trust
  ```

  The TUI alternative is `/marketplace`, then search for Superpowers.
- Capabilities: shared library through the official Grok plugin.
- Update: not specified in the upstream README.
- Uninstall: not specified in the upstream README.

### Kimi Code

- Official instructions: [upstream README](https://github.com/obra/superpowers/blob/v7.0.0/README.md#kimi-code)
- Mechanism: Kimi plugin marketplace or direct repository install.
- Prerequisite: Kimi Code. Upstream does not state a minimum version.
- Install using the plugin manager: open `/plugins`, choose `Marketplace`, then `Superpowers`.
- Direct install:

  ```text
  /plugins install https://github.com/obra/superpowers
  ```

- Capabilities: shared library through the Kimi plugin manifest. Detailed upstream notes are in [`docs/README.kimi.md`](../../integrations/superpowers/docs/README.kimi.md).
- Update: not specified in the upstream README.
- Uninstall: not specified in the upstream README.

### OpenCode

- Official instructions: [upstream README](https://github.com/obra/superpowers/blob/v7.0.0/README.md#opencode) and [`.opencode/INSTALL.md`](../../integrations/superpowers/.opencode/INSTALL.md)
- Mechanism: OpenCode's own Git-backed plugin manager.
- Prerequisite: OpenCode. OpenCode V2 requires version 2.0.4 or later.
- Install: ask OpenCode to fetch and follow the upstream [`.opencode/INSTALL.md`](../../integrations/superpowers/.opencode/INSTALL.md). That file documents V1's `plugin` key and V2's `plugins` key with a Git-backed package specification.
- Capabilities: shared library plus OpenCode-specific plugin bootstrap and tool mappings. V1 and V2 mappings differ; V2 has no todo tool and uses a markdown plan instead.
- Update: restart, clear the package cache, or reinstall if a Git dependency is cached. Version tags or commits can be pinned. The upstream guide says V2 requires Superpowers `v6.4.1` or later; this repository pins `v7.0.0`.
- Uninstall: the upstream guide documents removal of legacy symlink-based installs, but does not provide one universal uninstall command for the current V1/V2 plugin-manager configuration.

### Pi

- Official instructions: [upstream README](https://github.com/obra/superpowers/blob/v7.0.0/README.md#pi)
- Mechanism: Pi package installed from the upstream Git repository.
- Prerequisite: Pi. Upstream does not state a minimum version.
- Install:

  ```bash
  pi install git:github.com/obra/superpowers
  ```

  For local development only, the upstream README documents `pi -e /path/to/superpowers`.
- Capabilities: shared skills plus a small extension that injects the bootstrap at session start and after compaction. Pi has native skills, so no compatibility `Skill` tool is required. Subagent and task-list tools remain optional companion packages.
- Update: not specified in the upstream README.
- Uninstall: not specified in the upstream README.

### Qwen Code

- Official instructions: [upstream README](https://github.com/obra/superpowers/blob/v7.0.0/README.md#qwen-code)
- Mechanism: Qwen extension installer using Claude Code marketplaces.
- Prerequisite: Qwen Code. Upstream does not state a minimum version.
- Install:

  ```bash
  qwen extensions install obra/superpowers
  ```

  Select `superpowers` when prompted.
- Capabilities: shared library through the Claude-compatible marketplace integration.
- Update:

  ```bash
  qwen extensions update superpowers
  ```

- Uninstall: not specified in the upstream README.

### Hermes Agent

- Official instructions: [upstream README](https://github.com/obra/superpowers/blob/v7.0.0/README.md#hermes-agent)
- Mechanism: Hermes plugin installed from the upstream repository.
- Prerequisite: Hermes Agent. Upstream does not state a minimum version.
- Install:

  ```bash
  hermes plugins install obra/superpowers --enable
  ```

- Capabilities: shared library with Hermes-native skill registration and bootstrap.
- Limitation: Hermes has no post-compaction hook. A long session that compacts over its first turn can lose the bootstrap; upstream says to start a fresh session if skills stop triggering.
- Update: not specified in the upstream README.
- Uninstall: not specified in the upstream README.

### Muse

- Official instructions: [upstream README](https://github.com/obra/superpowers/blob/v7.0.0/README.md#muse)
- Mechanism: native Muse plugin; hooks require explicit approval.
- Prerequisite: Muse. Upstream does not state a minimum version.
- Install from a local checkout:

  ```bash
  muse plugins install ./
  muse plugins approve superpowers
  ```

  Or from a clone:

  ```bash
  git clone https://github.com/obra/superpowers.git
  muse plugins install ./superpowers
  muse plugins approve superpowers
  ```

- Capabilities: shared library; the `using-superpowers` bootstrap is injected through Muse's native `SessionStart` hook.
- Limitation: restart active sessions after installation; skills are immediate, but hooks require approval on first install. Upstream suggests verifying from a fresh session with a brainstorming-triggering prompt.
- Update:

  ```bash
  muse plugins update superpowers
  ```

- Uninstall: not specified in the upstream README.

## Local submodule maintenance

Initialize the pinned source after cloning this repository:

```bash
git submodule update --init --recursive
```

Inspect the recorded version:

```bash
git -C integrations/superpowers describe --tags --exact-match
git -C integrations/superpowers rev-parse HEAD
```

To update this repository later, first verify a new upstream stable release and
its full commit, then update the submodule to that exact commit and update the
release metadata at the top of this document. Do not replace the detached
commit with `main` or another moving branch.

This submodule is intentionally not linked into [`skills/`](../../skills/),
and `skills-lock.json` intentionally does not track its contents. The upstream
skills remain discoverable under `integrations/superpowers/` without becoming
part of this repository's personal skill namespace.

## Official references

- [Superpowers README](https://github.com/obra/superpowers/blob/v7.0.0/README.md)
- [Superpowers porting guide](https://github.com/obra/superpowers/blob/v7.0.0/docs/porting-to-a-new-harness.md)
- [OpenCode installation guide](https://github.com/obra/superpowers/blob/v7.0.0/.opencode/INSTALL.md)
- [Superpowers license](https://github.com/obra/superpowers/blob/v7.0.0/LICENSE)
- [Superpowers contributors](https://github.com/obra/superpowers/graphs/contributors)
