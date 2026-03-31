<!-- ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  SETUP INSTRUCTIONS
  1. Create repo named: YOUR_USERNAME/YOUR_USERNAME
  2. Upload pipeline.svg and stack.svg to the root of that repo
  3. Replace every YOUR_USERNAME with your GitHub handle
  4. Replace YOUR_NAME with your real name
  ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ -->

<div align="center">

```
$ whoami
> Kittukasa  ·  DevOps & Cloud Engineer
> AWS  ·  Jenkins  ·  Terraform  ·  Docker  ·  Linux
```

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=13&duration=2400&pause=800&color=58A6FF&center=true&vCenter=true&width=540&lines=terraform+plan+%E2%80%94+12+to+add%2C+0+to+destroy;docker+buildx+build+--push+api%3Av2.4.1;aws+eks+update-kubeconfig+--name+prod;jenkins+pipeline+%23847+%E2%80%94+SUCCESS;prometheus+%E2%80%94+all+alerting+rules+passing;shellcheck+*.sh+%E2%80%94+0+errors+found)](https://git.io/typing-svg)

</div>

---

### CI/CD Pipeline

![pipeline](https://raw.githubusercontent.com/Kittukasa/Kittukasa/main/pipeline.svg)

| Stage | Tool | What it does |
|---|---|---|
| `checkout` | `actions/checkout@v4` | Fetch source at commit SHA |
| `lint-sast` | `shellcheck` + `tfsec` | Shell lint + Terraform security scan |
| `unit-tests` | `pytest` | Hard gate — pipeline stops on failure |
| `docker-build` | `docker buildx` | Multi-arch build, layer cache enabled |
| `ecr-push` | `aws-actions/amazon-ecr-login` | Push image to private AWS ECR |
| `tf-apply` | `hashicorp/setup-terraform` | `terraform apply` against prod state |
| `eks-deploy` | `kubectl rollout` | Rolling update — zero downtime |

---

### Stack

![stack](https://raw.githubusercontent.com/Kittukasa/Kittukasa/main/stack.svg)

---

### Stats

<div align="center">

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=YOUR_USERNAME&show_icons=true&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=58a6ff&icon_color=3fb950&text_color=8b949e&count_private=true)
&nbsp;&nbsp;
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=YOUR_USERNAME&layout=compact&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=58a6ff&text_color=8b949e&langs_count=6)

![Streak](https://github-readme-streak-stats.herokuapp.com/?user=YOUR_USERNAME&theme=github-dark-blue&hide_border=true&background=0d1117&ring=58a6ff&fire=3fb950&currStreakLabel=58a6ff&sideLabels=484f58&dates=30363d)

</div>

---

### Currently

```yaml
building:
  - EKS cost optimisation  →  Karpenter node provisioner
  - Jenkins → GitHub Actions migration
  - Grafana alerting for AWS CodePipeline runs

learning:
  - OpenTelemetry on EKS  (replacing CloudWatch agent)
  - Trivy image scan in CodePipeline gate
  - AWS CDK  (replacing select Terraform modules)
```

---

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white&labelColor=0d1117)](https://linkedin.com/in/YOUR_USERNAME)
&nbsp;
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat&logo=gmail&logoColor=white&labelColor=0d1117)](mailto:YOUR_EMAIL)

`all systems operational`

</div>
