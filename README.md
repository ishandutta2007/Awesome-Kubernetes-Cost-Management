# Awesome-Kubernetes-Cost-Management

Top Kubernetes Cost Management Tools Ecosystem

Curated List of SaaS Products & Open-Source GitHub Projects
Focused on Cost Visibility, Resource Rightsizing, Autoscaling & FinOps for Kubernetes
Last updated: September 2026

This repository tracks notable SaaS platforms and open-source projects for Kubernetes Cost Management. These tools help platform teams, FinOps practitioners, and DevOps engineers monitor cluster spend, optimize resource allocation, rightsize workloads, and reduce cloud waste through intelligent scheduling and autoscaling.

Examples include Kubecost, Cast AI, Fairwinds Insights, OpenCost, StormForge, Densify, Spot Ocean, PerfectScale, Karpenter, Komodor, CloudZero, ScaleOps, nOps, Harness CCM, and Vantage (the category leaders).

Open-source emphasis: This section is heavily expanded with every major active project for self-hosting, custom FinOps workflows, and transparent cost allocation — ideal for platform teams and FinOps engineers who need deep visibility into Kubernetes and cloud spend without vendor lock-in or agent-heavy deployments.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

Table of Contents

SaaS/Hosted Platforms

Open-Source GitHub Projects

How to Contribute

Disclaimer

SaaS/Hosted Platforms

Kubecost
Commercial Kubernetes cost management platform built on the OpenCost engine, now part of IBM/Apptio. Adds bill reconciliation for enterprise discounts, reserved instances, and spot pricing, plus multi-cluster aggregation, budget alerts, and rightsizing recommendations. Free edition supports unlimited clusters up to 250 cores with 15-day metric retention -
1
-
7
.

Cast AI
Autonomous Kubernetes cost optimization platform. Unlike visibility-only tools, Cast AI actively right-sizes pods, selects optimal instance types, manages spot interruptions, and consolidates nodes without manual intervention. For teams ready to act on cost data rather than just observe it -
7
.

Fairwinds Insights
Kubernetes governance platform with cost optimization as part of a broader security and compliance offering. Provides resource efficiency recommendations alongside admission control and CVE auditing.

StormForge
ML-powered Kubernetes resource optimization. Deploys an agent to collect workload metrics, applies machine learning for rightsizing recommendations, and integrates with Karpenter, HPA, VPA, and GitOps workflows.

Densify
Cloud resource optimization using machine learning for rightsizing and workload placement across Kubernetes and virtualized environments.

Spot Ocean
Serverless container infrastructure from NetApp Spot. Automates cluster scaling, bin-packing, and spot instance management to reduce Kubernetes compute costs by 60–90% while maintaining reliability.

PerfectScale
Automated Kubernetes optimization with intent-aware rightsizing. Incorporates traffic patterns and workload criticality into every recommendation, reducing the risk of performance regressions from overly aggressive optimization -
13
.

CloudZero
Cloud cost intelligence platform with Kubernetes cost allocation folded into a broader unit-economics model. Answers "what does this customer or feature cost us" rather than just infrastructure totals. Single subscription, hourly granularity, long retention -
3
.

ScaleOps
Automated Kubernetes resource management platform that continuously adjusts allocations based on real-time demand.

nOps
AWS cost optimization with container visibility, automated tagging, and commitment management.

Harness CCM
Cloud cost management module within the Harness platform. Kubernetes cost visibility, anomaly detection, and optimization recommendations.

Vantage
Cloud cost transparency platform with Kubernetes cost reporting. Flat annual fee, virtual tagging for allocation where native tags are missing -
3
.

Open-Source GitHub Projects

OpenCost
CNCF Incubating open-source cost monitoring for Kubernetes and cloud spend. Real-time cost allocation by cluster, node, namespace, controller, service, or pod. Multi-cloud support (AWS, Azure, GCP), on-prem CSV pricing, GPU costs, carbon costs, and a built-in MCP server for AI agents (opt-in as of v1.118). Originally created by Kubecost. Apache-2.0 -
2
-
4
-
8
.

Karpenter
Kubernetes node autoscaler that improves efficiency and cost by watching for unschedulable pods, evaluating scheduling constraints, and provisioning right-sized nodes. Removes nodes when no longer needed via consolidation policies. CNCF project. Apache-2.0 -
5
.

KubeSurvival
Reduces Kubernetes costs by finding the cheapest machine types that can run your workloads. Analyzes resource requirements and recommends optimal instance types -
15
.

Fadvisor
FinOps Advisor from the Crane project. Collects cloud resource pricing and billing data, providing cost allocation insight for containers and Kubernetes resources -
15
.

OptScale
Open-source FinOps platform supporting AWS, Azure, GCP, Alibaba Cloud, and Kubernetes. Cost analytics, anomaly detection, rightsizing recommendations, budget management, and MLOps cost optimization -
15
.

Komiser
Open-source cloud resource manager that scans cloud accounts, builds full inventory, and surfaces misconfigurations, underutilized infrastructure, and hidden cost drivers. Supports AWS, Azure, GCP, DigitalOcean, Civo, and more -
15
.

Cloud Custodian
CNCF Incubating cloud governance tool using YAML-based DSL to create and enforce rules, including scheduling off-hours for resources. Can be used for cost optimization policies -
15
.

Koku
Open-source cost management for cloud and hybrid cloud environments. Cost visibility and reporting across providers.

Steampipe
Query live cloud APIs using SQL without ETL pipelines. 150+ plugins covering AWS, Azure, GCP, and Kubernetes. Can surface idle resources, underutilized instances, and spend patterns.

Wozz
Agentless Kubernetes cost auditor. Runs locally using existing kubectl context (read-only), grabs kubectl top metrics, compares to requests/limits, and calculates cost gap using standard cloud pricing. No persistent agents or pods installed — ideal for security-restricted environments. MIT licensed -
9
.

Kubeidle
Scale down Kubernetes workloads during specified time intervals. Simple cost-saving operator for non-production environments -
15
.

Kubefin
Unified cost allocation insights and optimization in multi-cloud, multi-cluster for Kubernetes -
15
.

Additional Strong Open-Source Options

Autoscaling: KEDA (event-driven autoscaling), Vertical Pod Autoscaler (VPA), Horizontal Pod Autoscaler (HPA) for dynamic resource adjustment.

Cost Models: Kubecost cost-model (cross-cloud cost allocation models), KubeModel (OpenCost Data Model 2.0 foundation for scalable cost tracking) -
15
-
20
.

Idle Detection: kubeidle (scale down during off-hours), cloudelephant (find idle resources in AWS/Azure) -
15
.

Spot Management: SpotKube (open-source Kubernetes-managed service optimizing deployment cost of microservices) -
15
.

Terraform Cost Estimation: terracost (estimate infrastructure costs from Terraform plans) -
15
.

Frameworks for building custom systems: Combine OpenCost for cost allocation and Prometheus metrics, Karpenter for intelligent node provisioning, KEDA for event-driven scaling, and Grafana for dashboards. Add Prometheus + Thanos/Mimir for long-term metric storage. Use Wozz for agentless initial audits before committing to persistent tooling.

How to Contribute

Fork the repo.

Add/edit entries in README.md (follow existing format).

Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

Submit PR with a short explanation.

Star the repo if you find it useful!

Disclaimer

This is a community-curated list — not exhaustive and not an endorsement.

Kubernetes cost tools require accurate cloud billing API integration; on-demand list pricing may misrepresent actual invoices by 30–50% without reconciliation -
7
.

Self-hosted open-source solutions require Prometheus, storage, and engineering time for dashboards and maintenance — the hidden cost of "free." Maintaining OpenCost with custom alerting and billing pipelines can consume 0.1–0.25 FTE annually -
7
.

Made for platform engineers, FinOps practitioners, SREs, and cloud architects.
Let's make Kubernetes cost management more open, transparent, and efficient.
