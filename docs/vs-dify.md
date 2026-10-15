# Kortix vs Dify: two open source platforms, one workforce you own

Kortix is open source, and so is Dify. Both let a team deploy an AI system without building a model lab, and they aim at different work. [Dify](https://dify.ai) is a platform for production-ready agentic workflows: a collaborative workspace where you build workflows and RAG pipelines on a visual canvas and deploy them on Dify Cloud, in a VPC, or self-hosted. Kortix, the open-source AI Operating System, runs a workforce of agents you own. Checked October 2026.

## The head-to-head

| | Kortix | Dify |
| --- | --- | --- |
| What it is | The open-source AI Operating System. | A platform for agentic workflows and RAG. |
| Open source | Yes. | Yes, with a self-hosted Community Edition. |
| How the work runs | Agents run sessions on cloud computers and finish work. | You build workflows and agents on a visual canvas. |
| Where it runs | Kortix Cloud, your VPC, or on-prem. | Dify Cloud, a VPC, or self-hosted. |
| Who owns the config | You. Agents, skills and memory are files in your repo. | The Dify workspace, or your infrastructure when self-hosted. |
| Model choice | Any provider with your own keys, or your ChatGPT plan. | Hundreds of LLMs from dozens of providers, or your own key. |

## Canvas app-building against a workforce you own

Dify gives you a canvas. You drag nodes, wire a model to a knowledge base, test the flow, and publish it as a web app or an API. [Dify's home page](https://dify.ai) describes deploying on cloud, in a VPC, or self-hosted, so a team can move from prototype to production on one stack. Dify fits when the job is a pipeline you can draw: retrieval, a prompt, a branching decision, and an output.

Kortix answers a different question. It is the open-source AI Operating System: your agents, their skills, your company memory, and every connector live in one git repo you own, and each session runs on its own cloud computer ([Kortix docs](https://kortix.com/docs)). You define an agent in markdown, give it a job across your connected tools, and its output arrives as a change request a person reviews.

Both projects are open source, and both self-host. The difference shows in what you keep. In Dify's cloud, the workspace holds the apps, workflows and knowledge bases. In Kortix, the configuration is plain files in your repo:

```yaml
# kortix.yaml
agents:
  support-triage:
    file: agents/support-triage.md
    connectors: all
triggers:
  - slug: daily-digest
    type: cron
    cron: '0 0 9 * * 1-5'
```

That file is the company. You can grep it, diff it, roll it back, and run thousands of sessions from it. Choose Dify when the deliverable is a flowchart you want to draw by hand. Choose Kortix when the work spans a company and you want to own the whole system, from the agent definitions to the gate that lands each change.
