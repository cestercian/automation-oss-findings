# automation-oss-findings

Living notes on contributing to big open source automation projects (workflow engines, browser automation, home automation, schedulers, agent harnesses) and a few other large repos I contribute to.

Each file in `repos/` covers one project:

- contribution rules (CONTRIBUTING, AI policy, CLA or DCO, how to claim issues)
- how to run tests and lints locally, CI quirks
- whether the project bans AI or agent assisted contributions
- the issue I picked, or why I skipped the repo

Notes are updated as I go, so some may be out of date.

## Index (batch31, 2026-10-18)

| Repo | Result | Note |
|---|---|---|
| [Koenkk/zigbee2mqtt](repos/Koenkk-zigbee2mqtt.md) | picked | PICKED #33399 (device `throttle` ignored because messageNonEmitted lastSeenChanged events publish full state directly) |
| [caronc/apprise](repos/caronc-apprise.md) | picked | PICKED #1803 (custom `from=` address lost in email URL round trips) |
| [homebridge/homebridge](repos/homebridge-homebridge.md) | picked | PICKED #4022 (Matter ColorControl commands fail when optional handlers are missing) |
| [node-red/node-red](repos/node-red-node-red.md) | picked | PICKED #6010 (removeModule compared an array to 0, so modules used by others got removed) |
| [semaphoreui/semaphore](repos/semaphoreui-semaphore.md) | picked | PICKED #4286 (template params nested under `params`/`ansible` ignored by FillParams) |
| [Aider-AI/aider](repos/Aider-AI-aider.md) | skipped | SKIPPED: barely maintained, PRs sit unreviewed. |
| [FlowiseAI/Flowise](repos/FlowiseAI-Flowise.md) | skipped | SKIPPED: every recent bug already linked to a PR or claimed. |
| [Hammerspoon/hammerspoon](repos/Hammerspoon-hammerspoon.md) | skipped | SKIPPED: #3905/#3890 are macOS crashes, cannot build or test on Linux. |
| [NousResearch/hermes-agent](repos/NousResearch-hermes-agent.md) | skipped | SKIPPED: PR creation reported restricted for outside accounts; per-author PR caps. |
| [OpenHands/OpenHands](repos/All-Hands-AI-OpenHands.md) | skipped | SKIPPED: open bugs need maintainer decisions or live in other repos. |
| [PipedreamHQ/pipedream](repos/PipedreamHQ-pipedream.md) | skipped | SKIPPED: bugs are hosted MCP/OAuth config, not repo code. |
| [PrefectHQ/prefect](repos/PrefectHQ-prefect.md) | skipped | SKIPPED: #22983 contested, #23138 has claim requests, #23430 has a pending proposal; recent bugs all have PRs. |
| [SeleniumHQ/selenium](repos/SeleniumHQ-selenium.md) | skipped | SKIPPED: AI disclosure requirement. |
| [Significant-Gravitas/AutoGPT](repos/Significant-Gravitas-AutoGPT.md) | skipped | SKIPPED: #15648 claimed by Ethereal49; rest are provider errors. |
| [Skyvern-AI/skyvern](repos/Skyvern-AI-skyvern.md) | skipped | SKIPPED: no open bugs (license/security questions only). |
| [Unitech/pm2](repos/Unitech-pm2.md) | skipped | SKIPPED: #6148 has PR #6149. |
| [aaif-goose/goose](repos/block-goose.md) | skipped | SKIPPED: no free Ready issue. |
| [activepieces/activepieces](repos/activepieces-activepieces.md) | skipped | SKIPPED: unsolicited PRs are paused. |
| [ansible/ansible](repos/ansible-ansible.md) | skipped | SKIPPED: disclosure expected. |
| [apache/airflow](repos/apache-airflow.md) | skipped | SKIPPED: Gen-AI disclosure required. |
| [appium/appium](repos/appium-appium.md) | skipped | SKIPPED: only a security report open recently. |
| [argoproj/argo-workflows](repos/argoproj-argo-workflows.md) | skipped | SKIPPED: AI declaration required; also #16866 already claimed. |
| [automatisch/automatisch](repos/automatisch-automatisch.md) | skipped | SKIPPED: no actionable open bugs. |
| [bigskysoftware/htmx](repos/bigskysoftware-htmx.md) | skipped | SKIPPED: #4147 soft-claimed; #4006 maintainer says invalid. |
| [blakeblackshear/frigate](repos/blakeblackshear-frigate.md) | skipped | SKIPPED: scan of recent issues found nothing unclaimed and well scoped. |
| [browser-use/browser-use](repos/browser-use-browser-use.md) | skipped | SKIPPED: #5955 PR closed; #5870 is the hosted live view. |
| [browserbase/stagehand](repos/browserbase-stagehand.md) | skipped | SKIPPED: #2910 targets an archived v3 line and a commenter flagged the fix as incomplete; #2782 Browserbase-hosted. |
| [celery/celery](repos/celery-celery.md) | skipped | SKIPPED: recent open issues are feature requests. |
| [charmbracelet/crush](repos/charmbracelet-crush.md) | skipped | SKIPPED: #3892 premise is wrong (allowlist is exact tool/action names, not globs); #3880 is in the upstream SDK; others are features. |
| [cline/cline](repos/cline-cline.md) | skipped | SKIPPED: no unclaimed, well-scoped bug. |
| [continuedev/continue](repos/continuedev-continue.md) | skipped | SKIPPED: #13363 has PR #13364. |
| [crewAIInc/crewAI](repos/crewAIInc-crewAI.md) | skipped | SKIPPED: open issues are llm-generated cohort tasks or vendor pitches. |
| [cypress-io/cypress](repos/cypress-io-cypress.md) | skipped | SKIPPED: #34961 claimed; #34994 and #34982 have PRs. |
| [dagster-io/dagster](repos/dagster-io-dagster.md) | skipped | SKIPPED: #34312 author offered a PR, #34301 has PR #34303, #34080 needs a design decision. |
| [denoland/deno](repos/denoland-deno.md) | skipped | SKIPPED: requires AI disclosure. |
| [drizzle-team/drizzle-orm](repos/drizzle-team-drizzle-orm.md) | skipped | SKIPPED: #6455 and #6460 already have PRs. |
| [espanso/espanso](repos/espanso-espanso.md) | skipped | SKIPPED: #2844 macOS-only, untestable on Linux. |
| [esphome/esphome](repos/esphome-esphome.md) | skipped | SKIPPED: open bugs are hardware crashes; #20572 reporter is opening the PR. |
| [go-task/task](repos/go-task-task.md) | skipped | SKIPPED: open issues are proposals or duplicates. |
| [google-gemini/gemini-cli](repos/google-gemini-gemini-cli.md) | skipped | SKIPPED: all 9 unassigned help-wanted issues already have PRs or claims. |
| [google/zx](repos/google-zx.md) | skipped | SKIPPED: #1529 may be intended behavior; earlier PR #1457 abandoned. |
| [home-assistant/core](repos/home-assistant-core.md) | skipped | SKIPPED: bans agent contributions. |
| [huginn/huginn](repos/huginn-huginn.md) | skipped | SKIPPED: no open bugs, only feature requests. |
| [jenkinsci/jenkins](repos/jenkinsci-jenkins.md) | skipped | SKIPPED: open issues are perf proposals needing design. |
| [juliangarnier/anime](repos/juliangarnier-anime.md) | skipped | SKIPPED: only a docs-site issue open. |
| [langflow-ai/langflow](repos/langflow-ai-langflow.md) | skipped | SKIPPED: recent bugs all linked to PRs or claimed. |
| [mermaid-js/mermaid](repos/mermaid-js-mermaid.md) | skipped | SKIPPED: #7564 and #7047 already fixed; newer issues are triage/feature requests. |
| [microsoft/playwright](repos/microsoft-playwright.md) | skipped | SKIPPED: Android PRs closed; #43492 soft-claimed. |
| [microsoft/playwright-mcp](repos/microsoft-playwright-mcp.md) | skipped | SKIPPED: #1795 is a feature request (max sessions option) awaiting maintainer answer. |
| [microsoft/playwright-python](repos/microsoft-playwright-python.md) | skipped | SKIPPED: #3266 already has maintainer PR #3267 (no cross-reference on the issue). |
| [n8n-io/n8n](repos/n8n-io-n8n.md) | skipped | SKIPPED: bug issues are triaged and assigned to the team. |
| [nektos/act](repos/nektos-act.md) | skipped | SKIPPED: maintenance-only mode. |
| [nodejs/undici](repos/nodejs-undici.md) | skipped | SKIPPED: under 10k stars; #5963 has PR #5964. |
| [ollama/ollama](repos/ollama-ollama.md) | skipped | SKIPPED: #18995 is an API design discussion; #19040 disputed; rest are GPU/model specific. |
| [puppeteer/puppeteer](repos/puppeteer-puppeteer.md) | skipped | SKIPPED: #15497 previous PR closed stale; no other free bugs. |
| [rails/rails](repos/rails-rails.md) | skipped | SKIPPED: Ractor issues need Ruby 4.0; #58990 claimed by Kutomore. |
| [renovatebot/renovate](repos/renovatebot-renovate.md) | skipped | SKIPPED: issues are maintainer-filed and pre-scoped. |
| [robotframework/robotframework](repos/robotframework-robotframework.md) | skipped | SKIPPED: #5807 is intended behavior. |
| [spotify/luigi](repos/spotify-luigi.md) | skipped | SKIPPED: only Salesforce API retirement and py3.14 support open. |
| [symfony/symfony](repos/symfony-symfony.md) | skipped | SKIPPED: #67040 has PRs; remaining good-first-issues are translations. |
| [temporalio/temporal](repos/temporalio-temporal.md) | skipped | SKIPPED: #11721 has PR #11727; remaining issues are deep replication bugs. |
| [traefik/traefik](repos/traefik-traefik.md) | skipped | SKIPPED: disclosure trailer required. |
| [triggerdotdev/trigger.dev](repos/triggerdotdev-trigger.dev.md) | skipped | SKIPPED: vouch required. |
| [vuetifyjs/vuetify](repos/vuetifyjs-vuetify.md) | skipped | SKIPPED: #21503 fixed, #23045 PR closed, #23153 needs design, #23248 disputed by maintainer. |
| [webdriverio/webdriverio](repos/webdriverio-webdriverio.md) | skipped | SKIPPED: under 10k; #16076 already has PR #15980. |
| [windmill-labs/windmill](repos/windmill-labs-windmill.md) | skipped | SKIPPED: not seeking outside contributions beyond small PRs, CLA. |
