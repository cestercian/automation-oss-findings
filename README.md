# automation-oss-findings

Living notes on contributing to big open source automation projects (workflow engines, browser automation, home automation, schedulers, agent harnesses) and a few other large repos I contribute to.

Each file in `repos/` covers one project:

- contribution rules (CONTRIBUTING, AI policy, CLA or DCO, how to claim issues)
- how to run tests and lints locally, CI quirks
- whether the project bans AI or agent assisted contributions
- the issue I picked, or why I skipped the repo

Notes are updated as I go, so some may be out of date.

## Index (batch31 + batch32, 2026-10-18)

| Repo | Result | Batch | Note |
|---|---|---|---|
| [BerriAI/litellm](repos/BerriAI-litellm.md) | picked | batch32 | PICKED #47273 (DATABASE_URL with password passed in prisma migrate diff argv) |
| [mobile-dev-inc/Maestro](repos/mobile-dev-inc-Maestro.md) | picked | batch32 | PICKED #3682 (flow name over 255 bytes aborts the run when creating the artifact dir) |
| [nrwl/nx](repos/nrwl-nx.md) | picked | batch32 | PICKED #37468 (angular-rspack SSR engine manifest import dropped when sideEffects is set) |
| [pulumi/pulumi](repos/pulumi-pulumi.md) | picked | batch32 | PICKED #25259 (single-member enums / `as const` objects in component args fail with Unsupported type) |
| [saltstack/salt](repos/saltstack-salt.md) | picked | batch32 | PICKED #70393 (after a zmq_monitor reconnect, __master_alive runs every second and the disconnect deletes the wrong job name). Based on 3007.x (3006.x defaults zmq_mon... |
| [caronc/apprise](repos/caronc-apprise.md) | picked | batch31 | PICKED #1803 (custom `from=` address lost in email URL round trips) |
| [homebridge/homebridge](repos/homebridge-homebridge.md) | picked | batch31 | PICKED #4022 (Matter ColorControl commands fail when optional handlers are missing) |
| [Koenkk/zigbee2mqtt](repos/Koenkk-zigbee2mqtt.md) | picked | batch31 | PICKED #33399 (device `throttle` ignored because messageNonEmitted lastSeenChanged events publish full state directly) |
| [node-red/node-red](repos/node-red-node-red.md) | picked | batch31 | PICKED #6010 (removeModule compared an array to 0, so modules used by others got removed) |
| [semaphoreui/semaphore](repos/semaphoreui-semaphore.md) | picked | batch31 | PICKED #4286 (template params nested under `params`/`ansible` ignored by FillParams) |
| [agno-agi/agno](repos/agno-agi-agno.md) | skipped | batch32 | SKIPPED: requires AI disclosure; #11032/#11117 claimed by their reporters. |
| [apify/crawlee](repos/apify-crawlee.md) | skipped | batch32 | SKIPPED (backup): #4283/#4282/#4260 well described but filed by Apify staff; ThrottlingRequestManager is complex; outside merges rare (1 of last 20). |
| [AutomaApp/automa](repos/AutomaApp-automa.md) | skipped | batch32 | SKIPPED: only junk issues. |
| [casey/just](repos/casey-just.md) | skipped | batch32 | SKIPPED: only feature requests open. |
| [comfyanonymous/ComfyUI](repos/comfyanonymous-ComfyUI.md) | skipped | batch32 | SKIPPED: no free issues. |
| [coollabsio/coolify](repos/coollabsio-coolify.md) | skipped | batch32 | SKIPPED: requires AI disclosure. |
| [dagger/dagger](repos/dagger-dagger.md) | skipped | batch32 | SKIPPED: #14691 (session spans get service.name=unknown_service, fix in sessionTracerResource) is a good fix, but 0 outsider merges in last 150 PRs. |
| [dagu-org/dagu](repos/dagu-org-dagu.md) | skipped | batch32 | SKIPPED: small, nothing free. |
| [deepset-ai/haystack](repos/deepset-ai-haystack.md) | skipped | batch32 | SKIPPED: #13264 handled internally. |
| [dgtlmoon/changedetection.io](repos/dgtlmoon-changedetection.io.md) | skipped | batch32 | SKIPPED: no free bug issues in the window. |
| [goreleaser/goreleaser](repos/goreleaser-goreleaser.md) | skipped | batch32 | SKIPPED: no free issues. |
| [grafana/k6](repos/grafana-k6.md) | skipped | batch32 | SKIPPED: no free issues. |
| [hatchet-dev/hatchet](repos/hatchet-dev-hatchet.md) | skipped | batch32 | SKIPPED: 8k stars, below the size bar this batch; #5225/#5190/#5188 look real if needed later. |
| [Homebrew/brew](repos/Homebrew-brew.md) | skipped | batch32 | SKIPPED: no free issues. |
| [huggingface/smolagents](repos/huggingface-smolagents.md) | skipped | batch32 | SKIPPED: open issues are spam or proposals. |
| [jdx/mise](repos/jdx-mise.md) | skipped | batch32 | SKIPPED: no free bug issues. |
| [kedro-org/kedro](repos/kedro-org-kedro.md) | skipped | batch32 | SKIPPED: #5817/#5818 being groomed, reporter asked to take the easy half. |
| [Kilo-Org/kilocode](repos/Kilo-Org-kilocode.md) | skipped | batch32 | SKIPPED: opencode fork, avoided. |
| [langchain-ai/langchain](repos/langchain-ai-langchain.md) | skipped | batch32 | SKIPPED: #40918 claimed (reporter has a fix waiting for assignment, plus another claimant). |
| [langchain-ai/langgraph](repos/langchain-ai-langgraph.md) | skipped | batch32 | SKIPPED: the `external` issues (#9304, #9218, #9266) all have multiple claimants or reporters with fixes ready. |
| [langgenius/dify](repos/langgenius-dify.md) | skipped | batch32 | SKIPPED: open bugs are vague or cloud/plugin-daemon config (#44159, #44238). |
| [letta-ai/letta](repos/letta-ai-letta.md) | skipped | batch32 | SKIPPED: nothing free. |
| [locustio/locust](repos/locustio-locust.md) | skipped | batch32 | SKIPPED: no free bug issues in the window. |
| [mastra-ai/mastra](repos/mastra-ai-mastra.md) | skipped | batch32 | SKIPPED: fresh bugs (#27479, #27466) still in needs-triage. |
| [microsoft/autogen](repos/microsoft-autogen.md) | skipped | batch32 | SKIPPED: nothing free. |
| [openai/openai-agents-python](repos/openai-openai-agents-python.md) | skipped | batch32 | SKIPPED: #5386/#5382/#5342 each have several claimants and fork fixes. |
| [opentofu/opentofu](repos/opentofu-opentofu.md) | skipped | batch32 | SKIPPED: bans LLM-generated contributions. |
| [pre-commit/pre-commit](repos/pre-commit-pre-commit.md) | skipped | batch32 | SKIPPED: no free issues. |
| [pydantic/pydantic-ai](repos/pydantic-pydantic-ai.md) | skipped | batch32 | SKIPPED: #10531 claimed by monish-rgb; #10243 model specific. |
| [QwenLM/qwen-code](repos/QwenLM-qwen-code.md) | skipped | batch32 | SKIPPED: issues are filed and owned by the team. |
| [rclone/rclone](repos/rclone-rclone.md) | skipped | batch32 | SKIPPED: backend-specific bugs needing accounts (internxt, drive). |
| [RooCodeInc/Roo-Code](repos/RooCodeInc-Roo-Code.md) | skipped | batch32 | SKIPPED: nothing free. |
| [rq/rq](repos/rq-rq.md) | skipped | batch32 | SKIPPED: only a feature proposal open. |
| [run-llama/llama_index](repos/run-llama-llama_index.md) | skipped | batch32 | SKIPPED: #23515 has 3 comments/claimants; rest are listings/proposals. |
| [scrapy/scrapy](repos/scrapy-scrapy.md) | skipped | batch32 | SKIPPED: no free bug issues. |
| [semantic-release/semantic-release](repos/semantic-release-semantic-release.md) | skipped | batch32 | SKIPPED: only junk issues. |
| [stanfordnlp/dspy](repos/stanfordnlp-dspy.md) | skipped | batch32 | SKIPPED: only feature/docs requests. |
| [SWE-agent/SWE-agent](repos/SWE-agent-SWE-agent.md) | skipped | batch32 | SKIPPED: spam and proposals only. |
| [vercel/turborepo](repos/vercel-turborepo.md) | skipped | batch32 | SKIPPED: #14845/#14841 fresh but not examined this batch (nx picked instead). |
| [wix/Detox](repos/wix-Detox.md) | skipped | batch32 | SKIPPED: #4986 iOS only, not examined. |
| [aaif-goose/goose](repos/block-goose.md) | skipped | batch31 | SKIPPED: no free Ready issue. |
| [activepieces/activepieces](repos/activepieces-activepieces.md) | skipped | batch31 | SKIPPED: unsolicited PRs are paused. |
| [Aider-AI/aider](repos/Aider-AI-aider.md) | skipped | batch31 | SKIPPED: barely maintained, PRs sit unreviewed. |
| [ansible/ansible](repos/ansible-ansible.md) | skipped | batch31 | SKIPPED: disclosure expected. |
| [apache/airflow](repos/apache-airflow.md) | skipped | batch31 | SKIPPED: Gen-AI disclosure required. |
| [appium/appium](repos/appium-appium.md) | skipped | batch31 | SKIPPED: only a security report open recently. |
| [argoproj/argo-workflows](repos/argoproj-argo-workflows.md) | skipped | batch31 | SKIPPED: AI declaration required; also #16866 already claimed. |
| [automatisch/automatisch](repos/automatisch-automatisch.md) | skipped | batch31 | SKIPPED: no actionable open bugs. |
| [bigskysoftware/htmx](repos/bigskysoftware-htmx.md) | skipped | batch31 | SKIPPED: #4147 soft-claimed; #4006 maintainer says invalid. |
| [blakeblackshear/frigate](repos/blakeblackshear-frigate.md) | skipped | batch31 | SKIPPED: scan of recent issues found nothing unclaimed and well scoped. |
| [browser-use/browser-use](repos/browser-use-browser-use.md) | skipped | batch31 | SKIPPED: #5955 PR closed; #5870 is the hosted live view. |
| [browserbase/stagehand](repos/browserbase-stagehand.md) | skipped | batch31 | SKIPPED: #2910 targets an archived v3 line and a commenter flagged the fix as incomplete; #2782 Browserbase-hosted. |
| [celery/celery](repos/celery-celery.md) | skipped | batch31 | SKIPPED: recent open issues are feature requests. |
| [charmbracelet/crush](repos/charmbracelet-crush.md) | skipped | batch31 | SKIPPED: #3892 premise is wrong (allowlist is exact tool/action names, not globs); #3880 is in the upstream SDK; others are features. |
| [cline/cline](repos/cline-cline.md) | skipped | batch31 | SKIPPED: no unclaimed, well-scoped bug. |
| [continuedev/continue](repos/continuedev-continue.md) | skipped | batch31 | SKIPPED: #13363 has PR #13364. |
| [crewAIInc/crewAI](repos/crewAIInc-crewAI.md) | skipped | batch31 | SKIPPED: open issues are llm-generated cohort tasks or vendor pitches. |
| [cypress-io/cypress](repos/cypress-io-cypress.md) | skipped | batch31 | SKIPPED: #34961 claimed; #34994 and #34982 have PRs. |
| [dagster-io/dagster](repos/dagster-io-dagster.md) | skipped | batch31 | SKIPPED: #34312 author offered a PR, #34301 has PR #34303, #34080 needs a design decision. |
| [denoland/deno](repos/denoland-deno.md) | skipped | batch31 | SKIPPED: requires AI disclosure. |
| [drizzle-team/drizzle-orm](repos/drizzle-team-drizzle-orm.md) | skipped | batch31 | SKIPPED: #6455 and #6460 already have PRs. |
| [espanso/espanso](repos/espanso-espanso.md) | skipped | batch31 | SKIPPED: #2844 macOS-only, untestable on Linux. |
| [esphome/esphome](repos/esphome-esphome.md) | skipped | batch31 | SKIPPED: open bugs are hardware crashes; #20572 reporter is opening the PR. |
| [FlowiseAI/Flowise](repos/FlowiseAI-Flowise.md) | skipped | batch31 | SKIPPED: every recent bug already linked to a PR or claimed. |
| [go-task/task](repos/go-task-task.md) | skipped | batch31 | SKIPPED: open issues are proposals or duplicates. |
| [google-gemini/gemini-cli](repos/google-gemini-gemini-cli.md) | skipped | batch31 | SKIPPED: all 9 unassigned help-wanted issues already have PRs or claims. |
| [google/zx](repos/google-zx.md) | skipped | batch31 | SKIPPED: #1529 may be intended behavior; earlier PR #1457 abandoned. |
| [Hammerspoon/hammerspoon](repos/Hammerspoon-hammerspoon.md) | skipped | batch31 | SKIPPED: #3905/#3890 are macOS crashes, cannot build or test on Linux. |
| [home-assistant/core](repos/home-assistant-core.md) | skipped | batch31 | SKIPPED: bans agent contributions. |
| [huginn/huginn](repos/huginn-huginn.md) | skipped | batch31 | SKIPPED: no open bugs, only feature requests. |
| [jenkinsci/jenkins](repos/jenkinsci-jenkins.md) | skipped | batch31 | SKIPPED: open issues are perf proposals needing design. |
| [juliangarnier/anime](repos/juliangarnier-anime.md) | skipped | batch31 | SKIPPED: only a docs-site issue open. |
| [langflow-ai/langflow](repos/langflow-ai-langflow.md) | skipped | batch31 | SKIPPED: recent bugs all linked to PRs or claimed. |
| [mermaid-js/mermaid](repos/mermaid-js-mermaid.md) | skipped | batch31 | SKIPPED: #7564 and #7047 already fixed; newer issues are triage/feature requests. |
| [microsoft/playwright](repos/microsoft-playwright.md) | skipped | batch31 | SKIPPED: Android PRs closed; #43492 soft-claimed. |
| [microsoft/playwright-mcp](repos/microsoft-playwright-mcp.md) | skipped | batch31 | SKIPPED: #1795 is a feature request (max sessions option) awaiting maintainer answer. |
| [microsoft/playwright-python](repos/microsoft-playwright-python.md) | skipped | batch31 | SKIPPED: #3266 already has maintainer PR #3267 (no cross-reference on the issue). |
| [n8n-io/n8n](repos/n8n-io-n8n.md) | skipped | batch31 | SKIPPED: bug issues are triaged and assigned to the team. |
| [nektos/act](repos/nektos-act.md) | skipped | batch31 | SKIPPED: maintenance-only mode. |
| [nodejs/undici](repos/nodejs-undici.md) | skipped | batch31 | SKIPPED: under 10k stars; #5963 has PR #5964. |
| [NousResearch/hermes-agent](repos/NousResearch-hermes-agent.md) | skipped | batch31 | SKIPPED: PR creation reported restricted for outside accounts; per-author PR caps. |
| [ollama/ollama](repos/ollama-ollama.md) | skipped | batch31 | SKIPPED: #18995 is an API design discussion; #19040 disputed; rest are GPU/model specific. |
| [OpenHands/OpenHands](repos/All-Hands-AI-OpenHands.md) | skipped | batch31 | SKIPPED: open bugs need maintainer decisions or live in other repos. |
| [PipedreamHQ/pipedream](repos/PipedreamHQ-pipedream.md) | skipped | batch31 | SKIPPED: bugs are hosted MCP/OAuth config, not repo code. |
| [PrefectHQ/prefect](repos/PrefectHQ-prefect.md) | skipped | batch31 | SKIPPED: #22983 contested, #23138 has claim requests, #23430 has a pending proposal; recent bugs all have PRs. |
| [puppeteer/puppeteer](repos/puppeteer-puppeteer.md) | skipped | batch31 | SKIPPED: #15497 previous PR closed stale; no other free bugs. |
| [rails/rails](repos/rails-rails.md) | skipped | batch31 | SKIPPED: Ractor issues need Ruby 4.0; #58990 claimed by Kutomore. |
| [renovatebot/renovate](repos/renovatebot-renovate.md) | skipped | batch31 | SKIPPED: issues are maintainer-filed and pre-scoped. |
| [robotframework/robotframework](repos/robotframework-robotframework.md) | skipped | batch31 | SKIPPED: #5807 is intended behavior. |
| [SeleniumHQ/selenium](repos/SeleniumHQ-selenium.md) | skipped | batch31 | SKIPPED: AI disclosure requirement. |
| [Significant-Gravitas/AutoGPT](repos/Significant-Gravitas-AutoGPT.md) | skipped | batch31 | SKIPPED: #15648 claimed by Ethereal49; rest are provider errors. |
| [Skyvern-AI/skyvern](repos/Skyvern-AI-skyvern.md) | skipped | batch31 | SKIPPED: no open bugs (license/security questions only). |
| [spotify/luigi](repos/spotify-luigi.md) | skipped | batch31 | SKIPPED: only Salesforce API retirement and py3.14 support open. |
| [symfony/symfony](repos/symfony-symfony.md) | skipped | batch31 | SKIPPED: #67040 has PRs; remaining good-first-issues are translations. |
| [temporalio/temporal](repos/temporalio-temporal.md) | skipped | batch31 | SKIPPED: #11721 has PR #11727; remaining issues are deep replication bugs. |
| [traefik/traefik](repos/traefik-traefik.md) | skipped | batch31 | SKIPPED: disclosure trailer required. |
| [triggerdotdev/trigger.dev](repos/triggerdotdev-trigger.dev.md) | skipped | batch31 | SKIPPED: vouch required. |
| [Unitech/pm2](repos/Unitech-pm2.md) | skipped | batch31 | SKIPPED: #6148 has PR #6149. |
| [vuetifyjs/vuetify](repos/vuetifyjs-vuetify.md) | skipped | batch31 | SKIPPED: #21503 fixed, #23045 PR closed, #23153 needs design, #23248 disputed by maintainer. |
| [webdriverio/webdriverio](repos/webdriverio-webdriverio.md) | skipped | batch31 | SKIPPED: under 10k; #16076 already has PR #15980. |
| [windmill-labs/windmill](repos/windmill-labs-windmill.md) | skipped | batch31 | SKIPPED: not seeking outside contributions beyond small PRs, CLA. |
