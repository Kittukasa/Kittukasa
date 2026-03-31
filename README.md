<!-- ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
     GitHub Profile README — DevOps & Cloud Engineer
     Stack: AWS · Jenkins · GitHub Actions · Terraform
            Docker · Prometheus · Grafana · Shell · Linux
     Replace YOUR_USERNAME and YOUR_NAME throughout
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ -->

<div align="center">

```
╔─────────────────────────────────────────────────────────╗
│  $ whoami                                               │
│  > YOUR_NAME — DevOps & Cloud Engineer                  │
│  > AWS · Jenkins · Terraform · Docker · Linux           │
╚─────────────────────────────────────────────────────────╝
```

<a href="https://git.io/typing-svg">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=14&duration=2600&pause=900&color=89B4FA&center=true&vCenter=true&width=560&lines=terraform+plan+%E2%94%80+12+to+add%2C+0+to+destroy;docker+buildx+build+--push+api%3Av2.4.1;aws+eks+update-kubeconfig+--name+prod;jenkins+pipeline+%23847+%E2%94%80+SUCCESS;prometheus+alert+%E2%94%80+all+rules+passing;shellcheck+*.sh+%E2%94%80+0+errors+found" alt="Typing SVG" />
</a>

</div>

---

## Workflow · deploy.yml

```yaml
# .github/workflows/deploy.yml
name: CI/CD Pipeline
on:
  push:
    branches: [main]
jobs:
  pipeline:
    runs-on: ubuntu-latest
    steps:
```

```
  Checkout   Lint/SAST  Unit Tests  Docker     ECR Push   Terraform  EKS Deploy
  ────────   ─────────  ──────────  ───────    ────────   ─────────  ──────────
     ✓ 3s      ✓ 48s     ✓ 1m12s   ▶ running   ○ queue   ○ queue    ○ queue
     └──────────┴──────────┴──────────┴───────────┴──────────┴──────────┘
                                    run #1847 · on: push · main@c8f3a12
```

| Stage | Tool | Detail |
|---|---|---|
| `checkout` | `actions/checkout@v4` | Fetch source, set SHA |
| `lint-sast` | `shellcheck` + `tfsec` | Shell scripts + Terraform security scan |
| `unit-tests` | `pytest` | Gate — fails fast on broken logic |
| `docker-build` | `docker buildx` | Multi-arch linux/amd64, cached layers |
| `ecr-push` | `aws-actions/amazon-ecr-login` | Push to private ECR registry |
| `tf-apply` | `hashicorp/setup-terraform` | `terraform apply -auto-approve` |
| `eks-deploy` | `kubectl rollout` | Rolling update to EKS cluster |

---

## Stack

**Cloud · AWS**
`EC2` `EKS` `S3` `ECR` `SNS` `SQS` `EventBridge` `CodePipeline` `API Gateway` `CloudWatch`

**CI/CD · IaC · Containers**
`Jenkins` `GitHub Actions` `AWS CodePipeline` `Terraform` `Docker`

**Observability · OS · VCS**
`Prometheus` `Grafana` `Shell` `Linux` `Git` `GitHub`

---

## Infrastructure at a glance

```
uptime (prod)      ████████████████████  99.97%
deploys / month    320+
pipelines managed  14
avg deploy time    < 4 min
```

---

## Currently working on

```yaml
current:
  - "EKS cluster autoscaler tuning — Karpenter migration"
  - "Jenkins to GitHub Actions full migration"
  - "Grafana dashboards for AWS CodePipeline metrics"

learning:
  - "AWS CDK — replacing select Terraform modules"
  - "OpenTelemetry for distributed tracing on EKS"
  - "Trivy + ECR scan integration in CodePipeline"
```

---

## GitHub Stats

<div align="center">

<img height="160" src="https://github-readme-stats.vercel.app/api?username=YOUR_USERNAME&show_icons=true&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=89b4fa&icon_color=a6e3a1&text_color=cdd6f4&count_private=true" />
&nbsp;
<img height="160" src="https://github-readme-stats.vercel.app/api/top-langs/?username=YOUR_USERNAME&layout=compact&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=89b4fa&text_color=cdd6f4&langs_count=6" />

</div>

<div align="center">
<img src="https://github-readme-streak-stats.herokuapp.com/?user=YOUR_USERNAME&theme=github-dark-blue&hide_border=true&background=0d1117&ring=89b4fa&fire=a6e3a1&currStreakLabel=89b4fa&sideLabels=6c7086&dates=45475a" width="48%" />
</div>

---

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white&labelColor=0d1117)](https://linkedin.com/in/YOUR_USERNAME)
&nbsp;
[![GitHub](https://img.shields.io/badge/GitHub-171515?style=flat&logo=github&logoColor=white&labelColor=0d1117)](https://github.com/YOUR_USERNAME)
&nbsp;
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat&logo=gmail&logoColor=white&labelColor=0d1117)](mailto:your@email.com)

<sub><code>all systems operational · aws · jenkins · terraform · docker</code></sub>

</div>
