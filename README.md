# Sai Ram

**AI infrastructure and platform architect**

I help engineering teams run AI workloads in production on infrastructure they control:
GPU and Kubernetes model serving, private or hybrid setups, reliability, and what it all
costs per unit of useful work.

## Measured work

### [AI inference cost optimization](https://github.com/vjsairam/ai-inference-cost-optimization)

Managed model API vs self-hosted vLLM on EKS vs a policy-routed hybrid, on the same frozen
task sets. Results from the August 2026 runs (costs are inference-service cost per correct
task, not full platform TCO):

- **Classification:** the private 7B model was more accurate (94.3% vs 77.8% correct) and about
  40 times cheaper per correct answer ($0.0000505 vs $0.00214).
- **Structured extraction:** the managed premium model won on quality (99.9% vs 40.7%), so the
  quality requirement decides, not the token price.
- **Hybrid routing** priced the blend in between: 88.9% correct at $0.00071 per correct task
  across mixed quality tiers.
- **Failure drills:** a deleted vLLM pod recovered in 2m45s, and 150 of 150 requests hit by
  injected provider faults failed over with no client-visible errors.
- **Autoscaling with KEDA** on two pre-provisioned GPU nodes: scale decision about 10s after
  load arrived; the second replica was ready after a 7m40s pod-plus-model cold start. Node
  provisioning was not measured.

### [Terraform MCP analyzer](https://github.com/vjsairam/terraform-mcp-analyzer)

Terraform upgrade analysis exposed as an MCP server, written in Go.

### [Racing telemetry audit](https://github.com/vjsairam/racemake-pitstop)

Engagement-style audit and hardening case study for a Node.js, MongoDB and ClickHouse
telemetry stack.

## What I work on

- Inference architecture: managed, private or hybrid, decided on cost per correct result
- GPU and Kubernetes model serving: vLLM, KServe, autoscaling
- Reliability and failure testing for AI services
- AI FinOps: GPU utilisation, capacity planning, unit economics
- Platform engineering: AWS, Terraform, observability, security

15+ years in infrastructure and platform engineering, including regulated environments.
CKA and CKS certified.

**Contact:** [sai@vjsairam.com](mailto:sai@vjsairam.com) · [vjsairam.com](https://vjsairam.com)
