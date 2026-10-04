## Muazu Isah

Cloud Solution Architect at Microsoft. I work with enterprise customers on Azure platform architecture — mostly Azure and AI platform engineering, API management, and the cost-governance problems that surface once AI workloads stop being pilots and start carrying real traffic.

What I publish here is the reusable half of that work: the patterns that held up across more than one engagement, written down so the next team starts further along than the last one did.

*Opinions and designs here are my own and do not represent the positions, strategies, or opinions of my employer.*

---

### Current work

**[azure-ai-gateway-cost-attribution](https://github.com/zuman88/azure-ai-gateway-cost-attribution)** — Production-grade Terraform for running Azure API Management as a centralised AI Gateway in front of Microsoft Foundry models, with optional per-application cost attribution and chargeback.

It addresses three problems that recur on nearly every engagement:

- **A model name hard-coded into forty services.** Clients call a logical alias, never a deployment name, so a model upgrade is a gateway change rather than forty pull requests.
- **No defensible answer to "what did each team spend?"** Per-request token accounting across input, cached, output and reasoning classes, allocated against authoritative Azure Cost Management spend — gateway telemetry decides *who*, Azure decides *how much*.
- **A gateway that works until one region throttles.** Native APIM backend pools with priority groups and per-backend circuit breakers: reserved capacity first, automatic spillover, automatic cross-region failover.

Includes architecture documentation, eight architecture decision records explaining why each trade-off was made, and an honest list of what it does not do.

---

### Interests

Centralised AI gateways · Azure API Management policy engineering · Azure Infrastructure Architecture . DevOps and Automation . FinOps and chargeback for AI workloads · Terraform module design · Identity-based access over shared secrets
