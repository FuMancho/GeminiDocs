# Gemini CLI Changelog

> Curated changelog sourced from the [official Gemini CLI releases](https://github.com/google-gemini/gemini-cli/releases).
> Last updated: 2026-04-13

## v0.37.1 (Latest Stable)


Released: April 09, 2026

For most users, our latest stable release is the recommended release. Install
the latest stable version with:

```
npm install -g @google/gemini-cli
```

## Highlights

- **Dynamic Sandbox Expansion:** Implemented dynamic sandbox expansion and
  worktree support for both Linux and Windows, enhancing development flexibility
  in restricted environments.
- **Tool-Based Topic Grouping (Chapters):** Introduced "Chapters" to logically
  group agent interactions based on tool usage and intent, providing a clearer
  narrative flow in long sessions.
- **Enhanced Browser Agent:** Added persistent session management, dynamic
  read-only tool discovery, and sandbox-aware initialization for the browser
  agent.
- **Security & Permission Hardening:** Implemented secret visibility lockdown
  for environment files and integrated integrity controls for Windows
  sandboxing.

## What's Changed

- fix(acp): handle all InvalidStreamError types gracefully in prompt
  [#24540](https://github.com/google-gemini/gemini-cli/pull/24540)
- feat(acp): add support for /about command
  [#24649](https://github.com/google-gemini/gemini-cli/pull/24649)
- feat(acp): add /help command
  [#24839](https://github.com/google-gemini/gemini-cli/pull/24839)
- feat(evals): centralize test agents into test-utils for reuse by @Samee24 in
  [#23616](https://github.com/google-gemini/gemini-cli/pull/23616)
- revert: chore(config): disable agents by default by @abhipatel12 in
  [#23672](https://github.com/google-gemini/gemini-cli/pull/23672)
- fix(plan): update telemetry attribute keys and add timestamp by @Adib234 in
  [#23685](https://github.com/google-gemini/gemini-cli/pull/23685)
- fix(core): prevent premature MCP discovery completion by @jackwotherspoon in
  [#23637](https://github.com/google-gemini/gemini-cli/pull/23637)
- feat(browser): add maxActionsPerTask for browser agent setting by
  @cynthialong0-0 in
  [#23216](https://github.com/google-gemini/gemini-cli/pull/23216)
- fix(core): improve agent loader error formatting for empty paths by
  @adamfweidman in
  [#23690](https://github.com/google-gemini/gemini-cli/pull/23690)
- fix(cli): only show updating spinner when auto-update is in progress by
  @scidomino in [#23709](https://github.com/google-gemini/gemini-cli/pull/23709)
- Refine onboarding metrics to log the duration explicitly and use the tier
  name. by @yunaseoul in
  [#23678](https://github.com/google-gemini/gemini-cli/pull/23678)
- chore(tools): add toJSON to tools and invocations to reduce logging verbosity
  by @alisa-alisa in
  [#22899](https://github.com/google-gemini/gemini-cli/pull/22899)
- fix(cli): stabilize copy mode to prevent flickering and cursor resets by
  @mattKorwel in
  [#22584](https://github.com/google-gemini/gemini-cli/pull/22584)
- fix(test): move flaky ctrl-c-exit test to non-blocking suite by @mattKorwel in
  [#23732](https://github.com/google-gemini/gemini-cli/pull/23732)
- feat(skills): add ci skill for automated failure replication by @mattKorwel in
  [#23720](https://github.com/google-gemini/gemini-cli/pull/23720)
- feat(sandbox): implement forbiddenPaths for OS-specific sandbox managers by
  @ehedlund in [#23282](https://github.com/google-gemini/gemini-cli/pull/23282)
- fix(core): conditionally expose additional_permissions in shell tool by
  @galz10 in [#23729](https://github.com/google-gemini/gemini-cli/pull/23729)
- refactor(core): standardize OS-specific sandbox tests and extract linux helper
  methods by @ehedlund in
  [#23715](https://github.com/google-gemini/gemini-cli/pull/23715)
- format recently added script by @scidomino in
  [#23739](https://github.com/google-gemini/gemini-cli/pull/23739)
- fix(ui): prevent over-eager slash subcommand completion by @keithguerin in
  [#20136](https://github.com/google-gemini/gemini-cli/pull/20136)
- Fix dynamic model routing for gemini 3.1 pro to customtools model by
  @kevinjwang1 in
  [#23641](https://github.com/google-gemini/gemini-cli/pull/23641)
- feat(core): support inline agentCardJson for remote agents by @adamfweidman in
  [#23743](https://github.com/google-gemini/gemini-cli/pull/23743)
- fix(cli): skip console log/info in headless mode by @cynthialong0-0 in
  [#22739](https://github.com/google-gemini/gemini-cli/pull/22739)
- test(core): install bubblewrap on Linux CI for sandbox integration tests by
  @ehedlund in [#23583](https://github.com/google-gemini/gemini-cli/pull/23583)
- docs(reference): split tools table into category sections by @sheikhlimon in
  [#21516](https://github.com/google-gemini/gemini-cli/pull/21516)
- fix(browser): detect embedded URLs in query params to prevent allowedDomains
  bypass by @tony-shi in
  [#23225](https://github.com/google-gemini/gemini-cli/pull/23225)
- fix(browser): add proxy bypass constraint to domain restriction system prompt
  by @tony-shi in
  [#23229](https://github.com/google-gemini/gemini-cli/pull/23229)
- fix(policy): relax write_file argsPattern in plan mode to allow paths without
  session ID by @Adib234 in
  [#23695](https://github.com/google-gemini/gemini-cli/pull/23695)
- docs: fix grammar in CONTRIBUTING and numbering in sandbox docs by
  @splint-disk-8i in
  [#23448](https://github.com/google-gemini/gemini-cli/pull/23448)
- fix(acp): allow attachments by adding a permission prompt by @sripasg in
  [#23680](https://github.com/google-gemini/gemini-cli/pull/23680)
- fix(core): thread AbortSignal to chat compression requests (#20405) by
  @SH20RAJ in [#20778](https://github.com/google-gemini/gemini-cli/pull/20778)
- feat(core): implement Windows sandbox dynamic expansion Phase 1 and 2.1 by
  @scidomino in [#23691](https://github.com/google-gemini/gemini-cli/pull/23691)
- Add note about root privileges in sandbox docs by @diodesign in
  [#23314](https://github.com/google-gemini/gemini-cli/pull/23314)
- docs(core): document agent_card_json string literal options for remote agents
  by @adamfweidman in
  [#23797](https://github.com/google-gemini/gemini-cli/pull/23797)
- fix(cli): resolve TTY hang on headless environments by unconditionally
  resuming process.stdin before React Ink launch by @cocosheng-g in
  [#23673](https://github.com/google-gemini/gemini-cli/pull/23673)
- fix(ui): cleanup estimated string length hacks in composer by @keithguerin in
  [#23694](https://github.com/google-gemini/gemini-cli/pull/23694)
- feat(browser): dynamically discover read-only tools by @cynthialong0-0 in
  [#23805](https://github.com/google-gemini/gemini-cli/pull/23805)
- docs: clarify policy requirement for `general.plan.directory` in settings
  schema by @jerop in
  [#23784](https://github.com/google-gemini/gemini-cli/pull/23784)
- Revert "perf(cli): optimize --version startup time (#23671)" by @scidomino in
  [#23812](https://github.com/google-gemini/gemini-cli/pull/23812)
- don't silence errors from wombat by @scidomino in
  [#23822](https://github.com/google-gemini/gemini-cli/pull/23822)
- fix(ui): prevent escape key from cancelling requests in shell mode by
  @PrasannaPal21 in
  [#21245](https://github.com/google-gemini/gemini-cli/pull/21245)
- Changelog for v0.36.0-preview.0 by @gemini-cli-robot in
  [#23702](https://github.com/google-gemini/gemini-cli/pull/23702)
- feat(core,ui): Add experiment-gated support for gemini flash 3.1 lite by
  @chrstnb in [#23794](https://github.com/google-gemini/gemini-cli/pull/23794)
- Changelog for v0.36.0-preview.3 by @gemini-cli-robot in
  [#23827](https://github.com/google-gemini/gemini-cli/pull/23827)
- new linting check: github-actions-pinning by @alisa-alisa in
  [#23808](https://github.com/google-gemini/gemini-cli/pull/23808)
- fix(cli): show helpful guidance when no skills are available by @Niralisj in
  [#23785](https://github.com/google-gemini/gemini-cli/pull/23785)
- fix: Chat logs and errors handle tail tool calls correctly by @googlestrobe in
  [#22460](https://github.com/google-gemini/gemini-cli/pull/22460)
- Don't try removing a tag from a non-existent release. by @scidomino in
  [#23830](https://github.com/google-gemini/gemini-cli/pull/23830)
- fix(cli): allow ask question dialog to take full window height by @jacob314 in
  [#23693](https://github.com/google-gemini/gemini-cli/pull/23693)
- fix(core): strip leading underscores from error types in telemetry by
  @yunaseoul in [#23824](https://github.com/google-gemini/gemini-cli/pull/23824)
- Changelog for v0.35.0 by @gemini-cli-robot in
  [#23819](https://github.com/google-gemini/gemini-cli/pull/23819)
- feat(evals): add reliability harvester and 500/503 retry support by
  @alisa-alisa in
  [#23626](https://github.com/google-gemini/gemini-cli/pull/23626)
- feat(sandbox): dynamic Linux sandbox expansion and worktree support by @galz10
  in [#23692](https://github.com/google-gemini/gemini-cli/pull/23692)
- Merge examples of use into quickstart documentation by @diodesign in
  [#23319](https://github.com/google-gemini/gemini-cli/pull/23319)
- fix(cli): prioritize primary name matches in slash command search by @sehoon38
  in [#23850](https://github.com/google-gemini/gemini-cli/pull/23850)
- Changelog for v0.35.1 by @gemini-cli-robot in
  [#23840](https://github.com/google-gemini/gemini-cli/pull/23840)
- fix(browser): keep input blocker active across navigations by @kunal-10-cloud
  in [#22562](https://github.com/google-gemini/gemini-cli/pull/22562)
- feat(core): new skill to look for duplicated code while reviewing PRs by
  @devr0306 in [#23704](https://github.com/google-gemini/gemini-cli/pull/23704)
- fix(core): replace hardcoded non-interactive ASK_USER denial with explicit
  policy rules by @ruomengz in
  [#23668](https://github.com/google-gemini/gemini-cli/pull/23668)
- fix(plan): after exiting plan mode switches model to a flash model by @Adib234
  in [#23885](https://github.com/google-gemini/gemini-cli/pull/23885)
- feat(gcp): add development worker infrastructure by @mattKorwel in
  [#23814](https://github.com/google-gemini/gemini-cli/pull/23814)
- fix(a2a-server): A2A server should execute ask policies in interactive mode by
  @kschaab in [#23831](https://github.com/google-gemini/gemini-cli/pull/23831)
- feat(core): define TrajectoryProvider interface by @sehoon38 in
  [#23050](https://github.com/google-gemini/gemini-cli/pull/23050)
- Docs: Update quotas and pricing by @jkcinouye in
  [#23835](https://github.com/google-gemini/gemini-cli/pull/23835)
- fix(core): allow disabling environment variable redaction by @galz10 in
  [#23927](https://github.com/google-gemini/gemini-cli/pull/23927)
- feat(cli): enable notifications cross-platform via terminal bell fallback by
  @genneth in [#21618](https://github.com/google-gemini/gemini-cli/pull/21618)
- feat(sandbox): implement secret visibility lockdown for env files by
  @DavidAPierce in
  [#23712](https://github.com/google-gemini/gemini-cli/pull/23712)
- fix(core): remove shell outputChunks buffer caching to prevent memory bloat
  and sanitize prompt input by @spencer426 in
  [#23751](https://github.com/google-gemini/gemini-cli/pull/23751)
- feat(core): implement persistent browser session management by @kunal-10-cloud
  in [#21306](https://github.com/google-gemini/gemini-cli/pull/21306)
- refactor(core): delegate sandbox denial parsing to SandboxManager by
  @scidomino in [#23928](https://github.com/google-gemini/gemini-cli/pull/23928)
- dep(update) Update Ink version to 6.5.0 by @jacob314 in
  [#23843](https://github.com/google-gemini/gemini-cli/pull/23843)
- Docs: Update 'docs-writer' skill for relative links by @jkcinouye in
  [#21463](https://github.com/google-gemini/gemini-cli/pull/21463)
- Changelog for v0.36.0-preview.4 by @gemini-cli-robot in
  [#23935](https://github.com/google-gemini/gemini-cli/pull/23935)
- fix(acp): Update allow approval policy flow for ACP clients to fix config
  persistence and compatible with TUI by @sripasg in
  [#23818](https://github.com/google-gemini/gemini-cli/pull/23818)
- Changelog for v0.35.2 by @gemini-cli-robot in
  [#23960](https://github.com/google-gemini/gemini-cli/pull/23960)
- ACP integration documents by @g-samroberts in
  [#22254](https://github.com/google-gemini/gemini-cli/pull/22254)
- fix(core): explicitly set error names to avoid bundling renaming issues by
  @yunaseoul in [#23913](https://github.com/google-gemini/gemini-cli/pull/23913)
- feat(core): subagent isolation and cleanup hardening by @abhipatel12 in
  [#23903](https://github.com/google-gemini/gemini-cli/pull/23903)
- disable extension-reload test by @scidomino in
  [#24018](https://github.com/google-gemini/gemini-cli/pull/24018)
- feat(core): add forbiddenPaths to GlobalSandboxOptions and refactor
  createSandboxManager by @ehedlund in
  [#23936](https://github.com/google-gemini/gemini-cli/pull/23936)
- refactor(core): improve ignore resolution and fix directory-matching bug by
  @ehedlund in [#23816](https://github.com/google-gemini/gemini-cli/pull/23816)
- revert(core): support custom base URL via env vars by @spencer426 in
  [#23976](https://github.com/google-gemini/gemini-cli/pull/23976)
- Increase memory limited for eslint. by @jacob314 in
  [#24022](https://github.com/google-gemini/gemini-cli/pull/24022)
- fix(acp): prevent crash on empty response in ACP mode by @sripasg in
  [#23952](https://github.com/google-gemini/gemini-cli/pull/23952)
- feat(core): Land `AgentHistoryProvider`. by @joshualitt in
  [#23978](https://github.com/google-gemini/gemini-cli/pull/23978)
- fix(core): switch to subshells for shell tool wrapping to fix heredocs and
  edge cases by @abhipatel12 in
  [#24024](https://github.com/google-gemini/gemini-cli/pull/24024)
- Debug command. by @jacob314 in
  [#23851](https://github.com/google-gemini/gemini-cli/pull/23851)
- Changelog for v0.36.0-preview.5 by @gemini-cli-robot in
  [#24046](https://github.com/google-gemini/gemini-cli/pull/24046)
- Fix test flakes by globally mocking ink-spinner by @jacob314 in
  [#24044](https://github.com/google-gemini/gemini-cli/pull/24044)
- Enable network access in sandbox configuration by @galz10 in
  [#24055](https://github.com/google-gemini/gemini-cli/pull/24055)
- feat(context): add configurable memoryBoundaryMarkers setting by @SandyTao520
  in [#24020](https://github.com/google-gemini/gemini-cli/pull/24020)
- feat(core): implement windows sandbox expansion and denial detection by
  @scidomino in [#24027](https://github.com/google-gemini/gemini-cli/pull/24027)
- fix(core): resolve ACP Operation Aborted Errors in grep_search by @ivanporty
  in [#23821](https://github.com/google-gemini/gemini-cli/pull/23821)
- fix(hooks): prevent SessionEnd from firing twice in non-interactive mode by
  @krishdef7 in [#22139](https://github.com/google-gemini/gemini-cli/pull/22139)
- Re-word intro to Gemini 3 page. by @g-samroberts in
  [#24069](https://github.com/google-gemini/gemini-cli/pull/24069)
- fix(cli): resolve layout contention and flashing loop in StatusRow by
  @keithguerin in
  [#24065](https://github.com/google-gemini/gemini-cli/pull/24065)
- fix(sandbox): implement Windows Mandatory Integrity Control for GeminiSandbox
  by @galz10 in [#24057](https://github.com/google-gemini/gemini-cli/pull/24057)
- feat(core): implement tool-based topic grouping (Chapters) by @Abhijit-2592 in
  [#23150](https://github.com/google-gemini/gemini-cli/pull/23150)
- feat(cli): support 'tab to queue' for messages while generating by @gundermanc
  in [#24052](https://github.com/google-gemini/gemini-cli/pull/24052)
- feat(core): agnostic background task UI with CompletionBehavior by
  @adamfweidman in
  [#22740](https://github.com/google-gemini/gemini-cli/pull/22740)
- UX for topic narration tool by @gundermanc in
  [#24079](https://github.com/google-gemini/gemini-cli/pull/24079)
- fix: shellcheck warnings in scripts by @scidomino in
  [#24035](https://github.com/google-gemini/gemini-cli/pull/24035)
- test(evals): add comprehensive subagent delegation evaluations by @abhipatel12
  in [#24132](https://github.com/google-gemini/gemini-cli/pull/24132)
- fix(a2a-server): prioritize ADC before evaluating headless constraints for
  auth initialization by @spencer426 in
  [#23614](https://github.com/google-gemini/gemini-cli/pull/23614)
- Text can be added after /plan command by @rambleraptor in
  [#22833](https://github.com/google-gemini/gemini-cli/pull/22833)
- fix(cli): resolve missing F12 logs via global console store by @scidomino in
  [#24235](https://github.com/google-gemini/gemini-cli/pull/24235)
- fix broken tests by @scidomino in
  [#24279](https://github.com/google-gemini/gemini-cli/pull/24279)
- fix(evals): add update_topic behavioral eval by @gundermanc in
  [#24223](https://github.com/google-gemini/gemini-cli/pull/24223)
- feat(core): Unified Context Management and Tool Distillation. by @joshualitt
  in [#24157](https://github.com/google-gemini/gemini-cli/pull/24157)
- Default enable narration for the team. by @gundermanc in
  [#24224](https://github.com/google-gemini/gemini-cli/pull/24224)
- fix(core): ensure default agents provide tools and use model-specific schemas
  by @abhipatel12 in
  [#24268](https://github.com/google-gemini/gemini-cli/pull/24268)
- feat(cli): show Flash Lite Preview model regardless of user tier by @sehoon38
  in [#23904](https://github.com/google-gemini/gemini-cli/pull/23904)
- feat(cli): implement compact tool output by @jwhelangoog in
  [#20974](https://github.com/google-gemini/gemini-cli/pull/20974)
- Add security settings for tool sandboxing by @galz10 in
  [#23923](https://github.com/google-gemini/gemini-cli/pull/23923)
- chore(test-utils): switch integration tests to use PREVIEW_GEMINI_MODEL by
  @sehoon38 in [#24276](https://github.com/google-gemini/gemini-cli/pull/24276)
- feat(core): enable topic update narration for legacy models by @Abhijit-2592
  in [#24241](https://github.com/google-gemini/gemini-cli/pull/24241)
- feat(core): add project-level memory scope to save_memory tool by @SandyTao520
  in [#24161](https://github.com/google-gemini/gemini-cli/pull/24161)
- test(integration): fix plan mode write denial test false positive by @sehoon38
  in [#24299](https://github.com/google-gemini/gemini-cli/pull/24299)
- feat(plan): support `Plan` mode in untrusted folders by @Adib234 in
  [#17586](https://github.com/google-gemini/gemini-cli/pull/17586)
- fix(core): enable mid-stream retries for all models and re-enable compression
  test by @sehoon38 in
  [#24302](https://github.com/google-gemini/gemini-cli/pull/24302)
- Changelog for v0.36.0-preview.6 by @gemini-cli-robot in
  [#24082](https://github.com/google-gemini/gemini-cli/pull/24082)
- Changelog for v0.35.3 by @gemini-cli-robot in
  [#24083](https://github.com/google-gemini/gemini-cli/pull/24083)
- feat(cli): add auth info to footer by @sehoon38 in
  [#24042](https://github.com/google-gemini/gemini-cli/pull/24042)
- fix(browser): reset action counter for each agent session and let it ignore
  internal actions by @cynthialong0-0 in
  [#24228](https://github.com/google-gemini/gemini-cli/pull/24228)
- feat(plan): promote planning feature to stable by @ruomengz in
  [#24282](https://github.com/google-gemini/gemini-cli/pull/24282)
- fix(browser): terminate subagent immediately on domain restriction violations
  by @gsquared94 in
  [#24313](https://github.com/google-gemini/gemini-cli/pull/24313)
- feat(cli): add UI to update extensions by @ruomengz in
  [#23682](https://github.com/google-gemini/gemini-cli/pull/23682)
- Fix(browser): terminate immediately for "browser is already running" error by
  @cynthialong0-0 in
  [#24233](https://github.com/google-gemini/gemini-cli/pull/24233)
- docs: Add 'plan' option to approval mode in CLI reference by @YifanRuan in
  [#24134](https://github.com/google-gemini/gemini-cli/pull/24134)
- fix(core): batch macOS seatbelt rules into a profile file to prevent ARG_MAX
  errors by @ehedlund in
  [#24255](https://github.com/google-gemini/gemini-cli/pull/24255)
- fix(core): fix race condition between browser agent and main closing process
  by @cynthialong0-0 in
  [#24340](https://github.com/google-gemini/gemini-cli/pull/24340)
- perf(build): optimize build scripts for parallel execution and remove
  redundant checks by @sehoon38 in
  [#24307](https://github.com/google-gemini/gemini-cli/pull/24307)
- ci: install bubblewrap on Linux for release workflows by @ehedlund in
  [#24347](https://github.com/google-gemini/gemini-cli/pull/24347)
- chore(release): allow bundling for all builds, including stable by @sehoon38
  in [#24305](https://github.com/google-gemini/gemini-cli/pull/24305)
- Revert "Add security settings for tool sandboxing" by @jerop in
  [#24357](https://github.com/google-gemini/gemini-cli/pull/24357)
- docs: update subagents docs to not be experimental by @abhipatel12 in
  [#24343](https://github.com/google-gemini/gemini-cli/pull/24343)
- fix(core): implement **read and **write commands in sandbox managers by
  @galz10 in [#24283](https://github.com/google-gemini/gemini-cli/pull/24283)
- don't try to remove tags in dry run by @scidomino in
  [#24356](https://github.com/google-gemini/gemini-cli/pull/24356)
- fix(config): disable JIT context loading by default by @SandyTao520 in
  [#24364](https://github.com/google-gemini/gemini-cli/pull/24364)
- test(sandbox): add integration test for dynamic permission expansion by
  @galz10 in [#24359](https://github.com/google-gemini/gemini-cli/pull/24359)
- docs(policy): remove unsupported mcpName wildcard edge case by @abhipatel12 in
  [#24133](https://github.com/google-gemini/gemini-cli/pull/24133)
- docs: fix broken GEMINI.md link in CONTRIBUTING.md by @Panchal-Tirth in
  [#24182](https://github.com/google-gemini/gemini-cli/pull/24182)
- feat(core): infrastructure for event-driven subagent history by @abhipatel12
  in [#23914](https://github.com/google-gemini/gemini-cli/pull/23914)
- fix(core): resolve Plan Mode deadlock during plan file creation due to sandbox
  restrictions by @DavidAPierce in
  [#24047](https://github.com/google-gemini/gemini-cli/pull/24047)
- fix(core): fix browser agent UX issues and improve E2E test reliability by
  @gsquared94 in
  [#24312](https://github.com/google-gemini/gemini-cli/pull/24312)
- fix(ui): wrap topic and intent fields in TopicMessage by @jwhelangoog in
  [#24386](https://github.com/google-gemini/gemini-cli/pull/24386)
- refactor(core): Centralize context management logic into src/context by
  @joshualitt in
  [#24380](https://github.com/google-gemini/gemini-cli/pull/24380)
- fix(core): pin AuthType.GATEWAY to use Gemini 3.1 Pro/Flash Lite by default by
  @sripasg in [#24375](https://github.com/google-gemini/gemini-cli/pull/24375)
- feat(ui): add Tokyo Night theme by @danrneal in
  [#24054](https://github.com/google-gemini/gemini-cli/pull/24054)
- fix(cli): refactor test config loading and mock debugLogger in test-setup by
  @mattKorwel in
  [#24389](https://github.com/google-gemini/gemini-cli/pull/24389)
- Set memoryManager to false in settings.json by @mattKorwel in
  [#24393](https://github.com/google-gemini/gemini-cli/pull/24393)
- ink 6.6.3 by @jacob314 in
  [#24372](https://github.com/google-gemini/gemini-cli/pull/24372)
- fix(core): resolve subagent chat recording gaps and directory inheritance by
  @abhipatel12 in
  [#24368](https://github.com/google-gemini/gemini-cli/pull/24368)
- fix(cli): cap shell output at 10 MB to prevent RangeError crash by @ProthamD
  in [#24168](https://github.com/google-gemini/gemini-cli/pull/24168)
- feat(plan): conditionally add enter/exit plan mode tools based on current mode
  by @ruomengz in
  [#24378](https://github.com/google-gemini/gemini-cli/pull/24378)
- feat(core): prioritize discussion before formal plan approval by @jerop in
  [#24423](https://github.com/google-gemini/gemini-cli/pull/24423)
- fix(ui): add accelerated scrolling on alternate buffer mode by @devr0306 in
  [#23940](https://github.com/google-gemini/gemini-cli/pull/23940)
- feat(core): populate sandbox forbidden paths with project ignore file contents
  by @ehedlund in
  [#24038](https://github.com/google-gemini/gemini-cli/pull/24038)
- fix(core): ensure blue border overlay and input blocker to act correctly
  depending on browser agent activities by @cynthialong0-0 in
  [#24385](https://github.com/google-gemini/gemini-cli/pull/24385)
- fix(ui): removed additional vertical padding for tables by @devr0306 in
  [#24381](https://github.com/google-gemini/gemini-cli/pull/24381)
- fix(build): upload full bundle directory archive to GitHub releases by
  @sehoon38 in [#24403](https://github.com/google-gemini/gemini-cli/pull/24403)
- fix(build): wire bundle:browser-mcp into bundle pipeline by @gsquared94 in
  [#24424](https://github.com/google-gemini/gemini-cli/pull/24424)
- feat(browser): add sandbox-aware browser agent initialization by @gsquared94
  in [#24419](https://github.com/google-gemini/gemini-cli/pull/24419)
- feat(core): enhance tracker task schemas for detailed titles and descriptions
  by @anj-s in [#23902](https://github.com/google-gemini/gemini-cli/pull/23902)
- refactor(core): Unified context management settings schema by @joshualitt in
  [#24391](https://github.com/google-gemini/gemini-cli/pull/24391)
- feat(core): update browser agent prompt to check open pages first when
  bringing up by @cynthialong0-0 in
  [#24431](https://github.com/google-gemini/gemini-cli/pull/24431)
- fix(acp) refactor(core,cli): centralize model discovery logic in
  ModelConfigService by @sripasg in
  [#24392](https://github.com/google-gemini/gemini-cli/pull/24392)
- Changelog for v0.36.0-preview.7 by @gemini-cli-robot in
  [#24346](https://github.com/google-gemini/gemini-cli/pull/24346)
- fix: update task tracker storage location in system prompt by @anj-s in
  [#24034](https://github.com/google-gemini/gemini-cli/pull/24034)
- feat(browser): supersede stale snapshots to reclaim context-window tokens by
  @gsquared94 in
  [#24440](https://github.com/google-gemini/gemini-cli/pull/24440)
- docs(core): add subagent tool isolation draft doc by @akh64bit in
  [#23275](https://github.com/google-gemini/gemini-cli/pull/23275)
- fix(patch): cherry-pick 64c928f to release/v0.37.0-preview.0-pr-23257 to patch
  version v0.37.0-preview.0 and create version 0.37.0-preview.1 by
  @gemini-cli-robot in
  [#24561](https://github.com/google-gemini/gemini-cli/pull/24561)
- fix(patch): cherry-pick cb7f7d6 to release/v0.37.0-preview.1-pr-24342 to patch
  version v0.37.0-preview.1 and create version 0.37.0-preview.2 by
  @gemini-cli-robot in
  [#24842](https://github.com/google-gemini/gemini-cli/pull/24842)

**Full Changelog**:
https://github.com/google-gemini/gemini-cli/compare/v0.36.0...v0.37.1
---

## v0.38.0-preview.0 (Preview)
# Preview release: v0.38.0-preview.0

Released: April 08, 2026

Our preview release includes the latest, new, and experimental features. This
release may not be as stable as our [latest weekly release](/docs/changelogs/latest).

To install the preview release:

```
npm install -g @google/gemini-cli@preview
```

## Highlights

- **Context Management:** Introduced a Context Compression Service to optimize
  context window usage and landed a background memory service for skill
  extraction.
- **Enhanced Security:** Implemented context-aware persistent policy approvals
  for smarter tool permissions and enabled `web_fetch` in plan mode with user
  confirmation.
- **Workflow Monitoring:** Added background process monitoring and inspection
  tools for better visibility into long-running tasks.
- **UI/UX Refinements:** Enhanced the tool confirmation UI, selection layout,
  and added support for selective topic expansion and click-to-expand.
- **Core Stability:** Improved sandbox reliability on Linux and Windows,
  resolved shebang compatibility issues, and fixed various crashes in the CLI
  and core services.

## What's Changed

- fix(cli): refresh slash command list after /skills reload by @NTaylorMullen in
  [#24454](https://github.com/google-gemini/gemini-cli/pull/24454)
- Update README.md for links. by @g-samroberts in
  [#22759](https://github.com/google-gemini/gemini-cli/pull/22759)
- fix(core): ensure complete_task tool calls are recorded in chat history by
  @abhipatel12 in
  [#24437](https://github.com/google-gemini/gemini-cli/pull/24437)
- feat(policy): explicitly allow web_fetch in plan mode with ask_user by
  @Adib234 in [#24456](https://github.com/google-gemini/gemini-cli/pull/24456)
- fix(core): refactor linux sandbox to fix ARG_MAX crashes by @ehedlund in
  [#24286](https://github.com/google-gemini/gemini-cli/pull/24286)
- feat(config): add experimental.adk.agentSessionNoninteractiveEnabled setting
  by @adamfweidman in
  [#24439](https://github.com/google-gemini/gemini-cli/pull/24439)
- Changelog for v0.36.0-preview.8 by @gemini-cli-robot in
  [#24453](https://github.com/google-gemini/gemini-cli/pull/24453)
- feat(cli): change default loadingPhrases to 'off' to hide tips by @keithguerin
  in [#24342](https://github.com/google-gemini/gemini-cli/pull/24342)
- fix(cli): ensure agent stops when all declinable tools are cancelled by
  @NTaylorMullen in
  [#24479](https://github.com/google-gemini/gemini-cli/pull/24479)
- fix(core): enhance sandbox usability and fix build error by @galz10 in
  [#24460](https://github.com/google-gemini/gemini-cli/pull/24460)
- Terminal Serializer Optimization by @jacob314 in
  [#24485](https://github.com/google-gemini/gemini-cli/pull/24485)
- Auto configure memory. by @jacob314 in
  [#24474](https://github.com/google-gemini/gemini-cli/pull/24474)
- Unused error variables in catch block are not allowed by @alisa-alisa in
  [#24487](https://github.com/google-gemini/gemini-cli/pull/24487)
- feat(core): add background memory service for skill extraction by @SandyTao520
  in [#24274](https://github.com/google-gemini/gemini-cli/pull/24274)
- feat: implement high-signal PR regression check for evaluations by
  @alisa-alisa in
  [#23937](https://github.com/google-gemini/gemini-cli/pull/23937)
- Fix shell output display by @jacob314 in
  [#24490](https://github.com/google-gemini/gemini-cli/pull/24490)
- fix(ui): resolve unwanted vertical spacing around various tool output
  treatments by @jwhelangoog in
  [#24449](https://github.com/google-gemini/gemini-cli/pull/24449)
- revert(cli): bring back input box and footer visibility in copy mode by
  @sehoon38 in [#24504](https://github.com/google-gemini/gemini-cli/pull/24504)
- fix(cli): prevent crash in AnsiOutputText when handling non-array data by
  @sehoon38 in [#24498](https://github.com/google-gemini/gemini-cli/pull/24498)
- feat(cli): support default values for environment variables by @ruomengz in
  [#24469](https://github.com/google-gemini/gemini-cli/pull/24469)
- Implement background process monitoring and inspection tools by @cocosheng-g
  in [#23799](https://github.com/google-gemini/gemini-cli/pull/23799)
- docs(browser-agent): update stale browser agent documentation by @gsquared94
  in [#24463](https://github.com/google-gemini/gemini-cli/pull/24463)
- fix: enable browser_agent in integration tests and add localhost fixture tests
  by @gsquared94 in
  [#24523](https://github.com/google-gemini/gemini-cli/pull/24523)
- fix(browser): handle computer-use model detection for analyze_screenshot by
  @gsquared94 in
  [#24502](https://github.com/google-gemini/gemini-cli/pull/24502)
- feat(core): Land ContextCompressionService by @joshualitt in
  [#24483](https://github.com/google-gemini/gemini-cli/pull/24483)
- feat(core): scope subagent workspace directories via AsyncLocalStorage by
  @SandyTao520 in
  [#24445](https://github.com/google-gemini/gemini-cli/pull/24445)
- Update ink version to 6.6.7 by @jacob314 in
  [#24514](https://github.com/google-gemini/gemini-cli/pull/24514)
- fix(acp): handle all InvalidStreamError types gracefully in prompt by @sripasg
  in [#24540](https://github.com/google-gemini/gemini-cli/pull/24540)
- Fix crash when vim editor is not found in PATH on Windows by
  @Nagajyothi-tammisetti in
  [#22423](https://github.com/google-gemini/gemini-cli/pull/22423)
- fix(core): move project memory dir under tmp directory by @SandyTao520 in
  [#24542](https://github.com/google-gemini/gemini-cli/pull/24542)
- Enable 'Other' option for yesno question type by @ruomengz in
  [#24545](https://github.com/google-gemini/gemini-cli/pull/24545)
- fix(cli): clear stale retry/loading state after cancellation (#21096) by
  @Aaxhirrr in [#21960](https://github.com/google-gemini/gemini-cli/pull/21960)
- Changelog for v0.37.0-preview.0 by @gemini-cli-robot in
  [#24464](https://github.com/google-gemini/gemini-cli/pull/24464)
- feat(core): implement context-aware persistent policy approvals by @jerop in
  [#23257](https://github.com/google-gemini/gemini-cli/pull/23257)
- docs: move agent disabling instructions and update remote agent status by
  @jackwotherspoon in
  [#24559](https://github.com/google-gemini/gemini-cli/pull/24559)
- feat(cli): migrate nonInteractiveCli to LegacyAgentSession by @adamfweidman in
  [#22987](https://github.com/google-gemini/gemini-cli/pull/22987)
- fix(core): unsafe type assertions in Core File System #19712 by
  @aniketsaurav18 in
  [#19739](https://github.com/google-gemini/gemini-cli/pull/19739)
- fix(ui): hide model quota in /stats and refactor quota display by @danzaharia1
  in [#24206](https://github.com/google-gemini/gemini-cli/pull/24206)
- Changelog for v0.36.0 by @gemini-cli-robot in
  [#24558](https://github.com/google-gemini/gemini-cli/pull/24558)
- Changelog for v0.37.0-preview.1 by @gemini-cli-robot in
  [#24568](https://github.com/google-gemini/gemini-cli/pull/24568)
- docs: add missing .md extensions to internal doc links by @ishaan-arora-1 in
  [#24145](https://github.com/google-gemini/gemini-cli/pull/24145)
- fix(ui): fixed table styling by @devr0306 in
  [#24565](https://github.com/google-gemini/gemini-cli/pull/24565)
- fix(core): pass includeDirectories to sandbox configuration by @galz10 in
  [#24573](https://github.com/google-gemini/gemini-cli/pull/24573)
- feat(ui): enable "TerminalBuffer" mode to solve flicker by @jacob314 in
  [#24512](https://github.com/google-gemini/gemini-cli/pull/24512)
- docs: clarify release coordination by @scidomino in
  [#24575](https://github.com/google-gemini/gemini-cli/pull/24575)
- fix(core): remove broken PowerShell translation and fix native \_\_write in
  Windows sandbox by @scidomino in
  [#24571](https://github.com/google-gemini/gemini-cli/pull/24571)
- Add instructions for how to start react in prod and force react to prod mode
  by @jacob314 in
  [#24590](https://github.com/google-gemini/gemini-cli/pull/24590)
- feat(cli): minimalist sandbox status labels by @galz10 in
  [#24582](https://github.com/google-gemini/gemini-cli/pull/24582)
- Feat/browser agent metrics by @kunal-10-cloud in
  [#24210](https://github.com/google-gemini/gemini-cli/pull/24210)
- test: fix Windows CI execution and resolve exposed platform failures by
  @ehedlund in [#24476](https://github.com/google-gemini/gemini-cli/pull/24476)
- feat(core,cli): prioritize summary for topics (#24608) by @Abhijit-2592 in
  [#24609](https://github.com/google-gemini/gemini-cli/pull/24609)
- show color by @jacob314 in
  [#24613](https://github.com/google-gemini/gemini-cli/pull/24613)
- feat(cli): enable compact tool output by default (#24509) by @jwhelangoog in
  [#24510](https://github.com/google-gemini/gemini-cli/pull/24510)
- fix(core): inject skill system instructions into subagent prompts if activated
  by @abhipatel12 in
  [#24620](https://github.com/google-gemini/gemini-cli/pull/24620)
- fix(core): improve windows sandbox reliability and fix integration tests by
  @ehedlund in [#24480](https://github.com/google-gemini/gemini-cli/pull/24480)
- fix(core): ensure sandbox approvals are correctly persisted and matched for
  proactive expansions by @galz10 in
  [#24577](https://github.com/google-gemini/gemini-cli/pull/24577)
- feat(cli) Scrollbar for input prompt by @jacob314 in
  [#21992](https://github.com/google-gemini/gemini-cli/pull/21992)
- Do not run pr-eval workflow when no steering changes detected by @alisa-alisa
  in [#24621](https://github.com/google-gemini/gemini-cli/pull/24621)
- Fix restoration of topic headers. by @gundermanc in
  [#24650](https://github.com/google-gemini/gemini-cli/pull/24650)
- feat(core): discourage update topic tool for simple tasks by @Samee24 in
  [#24640](https://github.com/google-gemini/gemini-cli/pull/24640)
- fix(core): ensure global temp directory is always in sandbox allowed paths by
  @galz10 in [#24638](https://github.com/google-gemini/gemini-cli/pull/24638)
- fix(core): detect uninitialized lines by @jacob314 in
  [#24646](https://github.com/google-gemini/gemini-cli/pull/24646)
- docs: update sandboxing documentation and toolSandboxing settings by @galz10
  in [#24655](https://github.com/google-gemini/gemini-cli/pull/24655)
- feat(cli): enhance tool confirmation UI and selection layout by @galz10 in
  [#24376](https://github.com/google-gemini/gemini-cli/pull/24376)
- feat(acp): add support for `/about` command by @sripasg in
  [#24649](https://github.com/google-gemini/gemini-cli/pull/24649)
- feat(cli): add role specific metrics to /stats by @cynthialong0-0 in
  [#24659](https://github.com/google-gemini/gemini-cli/pull/24659)
- split context by @jacob314 in
  [#24623](https://github.com/google-gemini/gemini-cli/pull/24623)
- fix(cli): remove -S from shebang to fix Windows and BSD execution by
  @scidomino in [#24756](https://github.com/google-gemini/gemini-cli/pull/24756)
- Fix issue where topic headers can be posted back to back by @gundermanc in
  [#24759](https://github.com/google-gemini/gemini-cli/pull/24759)
- fix(core): handle partial llm_request in BeforeModel hook override by
  @krishdef7 in [#22326](https://github.com/google-gemini/gemini-cli/pull/22326)
- fix(ui): improve narration suppression and reduce flicker by @gundermanc in
  [#24635](https://github.com/google-gemini/gemini-cli/pull/24635)
- fix(ui): fixed auth race condition causing logo to flicker by @devr0306 in
  [#24652](https://github.com/google-gemini/gemini-cli/pull/24652)
- fix(browser): remove premature browser cleanup after subagent invocation by
  @gsquared94 in
  [#24753](https://github.com/google-gemini/gemini-cli/pull/24753)
- Revert "feat(core,cli): prioritize summary for topics (#24608)" by
  @Abhijit-2592 in
  [#24777](https://github.com/google-gemini/gemini-cli/pull/24777)
- relax tool sandboxing overrides for plan mode to match defaults. by
  @DavidAPierce in
  [#24762](https://github.com/google-gemini/gemini-cli/pull/24762)
- fix(cli): respect global environment variable allowlist by @scidomino in
  [#24767](https://github.com/google-gemini/gemini-cli/pull/24767)
- fix(cli): ensure skills list outputs to stdout in non-interactive environments
  by @spencer426 in
  [#24566](https://github.com/google-gemini/gemini-cli/pull/24566)
- Add an eval for and fix unsafe cloning behavior. by @gundermanc in
  [#24457](https://github.com/google-gemini/gemini-cli/pull/24457)
- fix(policy): allow complete_task in plan mode by @abhipatel12 in
  [#24771](https://github.com/google-gemini/gemini-cli/pull/24771)
- feat(telemetry): add browser agent clearcut metrics by @gsquared94 in
  [#24688](https://github.com/google-gemini/gemini-cli/pull/24688)
- feat(cli): support selective topic expansion and click-to-expand by
  @Abhijit-2592 in
  [#24793](https://github.com/google-gemini/gemini-cli/pull/24793)
- temporarily disable sandbox integration test on windows by @ehedlund in
  [#24786](https://github.com/google-gemini/gemini-cli/pull/24786)
- Remove flakey test by @scidomino in
  [#24837](https://github.com/google-gemini/gemini-cli/pull/24837)
- Alisa/approve button by @alisa-alisa in
  [#24645](https://github.com/google-gemini/gemini-cli/pull/24645)
- feat(hooks): display hook system messages in UI by @mbleigh in
  [#24616](https://github.com/google-gemini/gemini-cli/pull/24616)
- fix(core): propagate BeforeModel hook model override end-to-end by @krishdef7
  in [#24784](https://github.com/google-gemini/gemini-cli/pull/24784)
- chore: fix formatting for behavioral eval skill reference file by @abhipatel12
  in [#24846](https://github.com/google-gemini/gemini-cli/pull/24846)
- fix: use directory junctions on Windows for skill linking by @enjoykumawat in
  [#24823](https://github.com/google-gemini/gemini-cli/pull/24823)
- fix(cli): prevent multiple banner increments on remount by @sehoon38 in
  [#24843](https://github.com/google-gemini/gemini-cli/pull/24843)
- feat(acp): add /help command by @sripasg in
  [#24839](https://github.com/google-gemini/gemini-cli/pull/24839)
- fix(core): remove tmux alternate buffer warning by @jackwotherspoon in
  [#24852](https://github.com/google-gemini/gemini-cli/pull/24852)
- Improve sandbox error matching and caching by @DavidAPierce in
  [#24550](https://github.com/google-gemini/gemini-cli/pull/24550)
- feat(core): add agent protocol UI types and experimental flag by @mbleigh in
  [#24275](https://github.com/google-gemini/gemini-cli/pull/24275)
- feat(core): use experiment flags for default fetch timeouts by @yunaseoul in
  [#24261](https://github.com/google-gemini/gemini-cli/pull/24261)
- Revert "fix(ui): improve narration suppression and reduce flicker (#2… by
  @gundermanc in
  [#24857](https://github.com/google-gemini/gemini-cli/pull/24857)
- refactor(cli): remove duplication in interactive shell awaiting input hint by
  @JayadityaGit in
  [#24801](https://github.com/google-gemini/gemini-cli/pull/24801)
- refactor(core): make LegacyAgentSession dependencies optional by @mbleigh in
  [#24287](https://github.com/google-gemini/gemini-cli/pull/24287)
- Changelog for v0.37.0-preview.2 by @gemini-cli-robot in
  [#24848](https://github.com/google-gemini/gemini-cli/pull/24848)
- fix(cli): always show shell command description or actual command by @jacob314
  in [#24774](https://github.com/google-gemini/gemini-cli/pull/24774)
- Added flag for ept size and increased default size by @devr0306 in
  [#24859](https://github.com/google-gemini/gemini-cli/pull/24859)
- fix(core): dispose Scheduler to prevent McpProgress listener leak by
  @Anjaligarhwal in
  [#24870](https://github.com/google-gemini/gemini-cli/pull/24870)
- fix(cli): switch default back to terminalBuffer=false and fix regressions
  introduced for that mode by @jacob314 in
  [#24873](https://github.com/google-gemini/gemini-cli/pull/24873)
- feat(cli): switch to ctrl+g from ctrl-x by @jacob314 in
  [#24861](https://github.com/google-gemini/gemini-cli/pull/24861)
- fix: isolate concurrent browser agent instances by @gsquared94 in
  [#24794](https://github.com/google-gemini/gemini-cli/pull/24794)
- docs: update MCP server OAuth redirect port documentation by @adamfweidman in
  [#24844](https://github.com/google-gemini/gemini-cli/pull/24844)

**Full Changelog**:
https://github.com/google-gemini/gemini-cli/compare/v0.37.0-preview.2...v0.38.0-preview.0
---


## v0.32.1 (Latest Stable)

### Highlights
- **Plan Mode Enhancements**: Significant updates to Plan Mode, including the ability to open and modify plans in an external editor, adaptations for complex tasks with multi-select options, and integration tests for plan mode.
- **Agent and Steering Improvements**: The generalist agent has been enabled to enhance task delegation, model steering is now supported directly within the workspace, and contiguous parallel admission is enabled for `Kind.Agent` tools.
- **Interactive Shell**: Interactive shell autocompletion has been introduced, significantly enhancing the user experience.
- **Core Stability and Performance**: Extensions are now loaded in parallel, fetch timeouts have been increased, robust A2A streaming reassembly was implemented, and orphaned processes when terminal closes have been prevented.
- **Billing and Quota Handling**: Implemented G1 AI credits overage flow with billing telemetry and added support for quota error fallbacks across all authentication types.

---

## v0.32.0-preview.0 (Preview)

### Highlights
- **Plan Mode Enhancements**: Significant updates to Plan Mode, including support for modifying plans in external editors, adaptive workflows based on task complexity, and new integration tests.
- **Agent and Core Engine Updates**: Enabled the generalist agent, introduced `Kind.Agent` for sub-agent classification, implemented task tracking foundation, and improved Agent-to-Agent (A2A) streaming and content extraction.
- **CLI & User Experience**: Introduced interactive shell autocompletion, added a new verbosity mode for cleaner error reporting, enabled parallel loading of extensions, and improved UI hints and shortcut handling.
- **Billing and Security**: Implemented G1 AI credits overage flow with enhanced billing telemetry, updated the authentication handshake to specification, and added support for a policy engine in extensions.
- **Stability and Bug Fixes**: Addressed numerous issues including 100% CPU consumption by orphaned processes, enhanced retry logic for Code Assist, reduced intrusive MCP errors, and merged duplicate imports across packages.

---

## v0.31.0

### Highlights
- **Gemini 3.1 Pro Preview**: Support for the new Gemini 3.1 Pro Preview model
- **Experimental Browser Agent**: New browser agent for direct web page interaction and context retrieval
- **Policy Engine Updates**: Project-level policies, MCP server wildcards, tool annotation matching
- **Web Fetch Enhancements**: Experimental direct web fetch tool with rate-limiting
- **Improved Plan Mode**: Custom storage directories, automatic model switching, post-execution summarization

### Notable Changes
- Ranged reads, limited searches, and fuzzy editing improvements (#19240)
- `gemini --resume` hint on exit (#16285)
- Alt+D for forward word deletion (#19300)
- macOS run-event notifications in interactive mode (#19056)
- MCP progress updates support (#19046)
- Devtools package migrated into monorepo (#18936)
- Admin settings only apply when `adminControlsApplicable = true` (#19453)
- `/dir add` directories included in @ autocomplete suggestions (#19246)
- Experimental in-progress steering hints (#19307)
- Plan mode documentation (#19467)

### Bug Fixes
- Fix bottom border color (#19266)
- Optimize height calculations for ask_user dialog (#19017)
- Support legacy onConfirm callback in ToolActionsContext (#19369)
- Plan mode safe fallback when experiment setting not enabled (#19439)
- Prevent empty history items (#19014)
- Ensure directory exists before writing conversation file (#18429)
- Ripgrep flag pattern fix (#18858)
- Disable auto-completion on Shift+Tab to preserve mode cycling (#19451)
- Unknown slash commands treated as regular input (#17393)

---

## v0.30.0

*See [full changelog](https://geminicli.com/docs/changelogs/) for earlier versions.*
