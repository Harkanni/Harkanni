<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:13233A,100:2E57F0&height=190&section=header&text=Akanni%20Emmanuel&fontColor=ffffff&fontSize=46&fontAlignY=36&desc=Cloud%20%26%20DevOps%20Engineer&descAlignY=58&descSize=18" alt="Akanni Emmanuel, Cloud and DevOps Engineer" width="100%" />
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=IBM+Plex+Sans&weight=600&size=21&pause=1400&color=2E57F0&center=true&vCenter=true&width=640&lines=I+design+AWS+infrastructure+around+how+apps+actually+run;Terraform+%7C+Amazon+EKS+%7C+Kubernetes+%7C+GitHub+Actions;5%2B+years+shipping+software%2C+now+building+the+platform+underneath" alt="Typing intro" />
</p>

<p align="center">
  <!-- Replace YOUR-PORTFOLIO-URL once the site is live on CloudFront -->
  <a href="https://YOUR-PORTFOLIO-URL"><img src="https://img.shields.io/badge/Portfolio-13233A?style=for-the-badge&logo=amazonaws&logoColor=white" alt="Portfolio" /></a>
  <a href="https://www.linkedin.com/in/akanniemmanuel/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="https://medium.com/@cloudopstechlead"><img src="https://img.shields.io/badge/Medium-000000?style=for-the-badge&logo=medium&logoColor=white" alt="Medium" /></a>
  <a href="https://x.com/the_tech_lead"><img src="https://img.shields.io/badge/X-000000?style=for-the-badge&logo=x&logoColor=white" alt="X" /></a>
  <a href="mailto:akanniemmanuel2001@gmail.com"><img src="https://img.shields.io/badge/Email-2E57F0?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
</p>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=Harkanni&label=Profile%20views&color=2E57F0&style=flat" alt="Profile views" />
  <a href="https://www.credly.com/badges/e5ab176b-0334-428c-955b-ead8ee56cdd8/public_url"><img src="https://img.shields.io/badge/AWS%20Educate-Cloud%20Computing%20101-FF9900?style=flat&logo=amazonaws&logoColor=white" alt="AWS Educate Cloud Computing 101 badge on Credly" /></a>
  <img src="https://img.shields.io/badge/Open%20to-Cloud%20%7C%20DevOps%20%7C%20Infrastructure%20roles-178A66?style=flat" alt="Open to Cloud, DevOps and Infrastructure roles" />
</p>

---

### `$ terraform output akanni`

```hcl
module "akanni" {
  source   = "github.com/harkanni"
  role     = "Cloud & DevOps Engineer"
  location = "Lagos, Nigeria (open to remote)"

  focus = ["AWS", "Terraform", "Kubernetes (EKS)", "CI/CD", "Docker"]

  background = "5+ years building web apps, so I design infrastructure around what the application needs"

  currently = {
    studying = "Cloud Engineering at AltSchool Africa"
    preparing_for = "AWS Certified Solutions Architect – Associate"
    writing  = "medium.com/@cloudopstechlead"
  }

  fun_fact = "2600-rated chess player (I wish...)"
}
```

---

### 🛠️ Stack

<p align="left">
  <img src="https://skillicons.dev/icons?i=aws,terraform,kubernetes,docker,githubactions,ansible,linux,bash&perline=8" alt="AWS, Terraform, Kubernetes, Docker, GitHub Actions, Ansible, Linux, Bash" />
  <br />
  <img src="https://skillicons.dev/icons?i=go,python,ts,react,nextjs,nodejs,postgres,mysql,mongodb,redis,netlify,git&perline=12" alt="Go, Python, TypeScript, React, Next.js, Node.js, PostgreSQL, MySQL, MongoDB, Redis, Netlify, Git" />
</p>

| Layer | What I use |
|---|---|
| **Cloud** | EC2, EKS, VPC, IAM, S3, CloudFront, ALB, Lambda, RDS, DynamoDB, ElastiCache, ECR, Secrets Manager, CloudWatch |
| **Infrastructure as code** | Terraform modules, S3 remote state with locking, Ansible |
| **Containers** | Docker multi-stage builds, Docker Compose, Kubernetes, Helm, AWS Load Balancer Controller |
| **Delivery** | GitHub Actions, OIDC federation, multi-target deploys (S3 + CloudFront, Netlify, Render) |
| **Security** | Least-privilege IAM, IRSA, EKS Access Entries, namespace RBAC, External Secrets Operator |

---

### 🏗️ Featured work

#### [Project Bedrock](https://github.com/Harkanni/project-bedrock-0324): a microservices store on Amazon EKS

A five-service retail app on a production-grade EKS cluster, provisioned end to end with Terraform.

```mermaid
flowchart LR
  push([git push]) --> gha[GitHub Actions<br/>OIDC]
  gha --> tf[Terraform]
  gha --> helm[Helm]
  tf --> eks
  shopper([Shopper]) --> alb[ALB Ingress] --> eks[Amazon EKS<br/>retail-app namespace]
  helm --> eks
  eks --> rds[(RDS MySQL<br/>and PostgreSQL)]
  eks --> ddb[(DynamoDB)]
  sm[Secrets Manager] -. External Secrets .-> eks
  eks -. logs and metrics .-> cw[CloudWatch]
  s3[(S3 upload)] --> lambda[Lambda<br/>image processing]
```

Multi-AZ VPC · EKS 1.33 with Access Entries · per-service IRSA · External Secrets · CloudWatch Observability · S3-triggered Lambda · read-only, namespace-scoped developer access

<br />

| Project | What it shows |
|---|---|
| **StartTech** | React and Go on EKS behind a dual-origin CloudFront distribution (S3 + ALB), modular Terraform, three separate GitHub Actions pipelines, and a full rebuild on a new AWS account from the same code |
| **MuchToDo** | Go API in private subnets across two AZs with NAT, bastion host and a health-checked ALB, containerized as a non-root multi-stage image |
| **Huddle** | Cloud engineer for a cross-functional Agile team building a lightweight team messaging app, deploying to EC2 with Docker |
| **[Three-Tier Web App](https://github.com/Harkanni/3-tier-architecture)** | Serverless app on S3, CloudFront, API Gateway, Lambda and DynamoDB, written up as a [step-by-step guide](https://medium.com/@cloudopstechlead/build-a-three-tier-web-app-8762da58ea7a) |
| **[Status Splitter](https://github.com/Harkanni/status-chunks)** | Privacy-first video splitter PWA (ffmpeg-wasm), hosted on S3 + CloudFront, later migrated to Netlify |
| **odoo-cloud** | Terraform provisions the EC2 host, Ansible configures it over SSH |

---

### 🔥 Things I've broken and fixed

<details>
<summary><b>EKS nodes never joined the cluster</b> (<code>NodeCreationFailure</code>)</summary>
<br />
Subnets had no route table association and public IP assignment was off, so nodes couldn't reach the control plane. Fixed the subnet routing in Terraform.
</details>

<details>
<summary><b>Every CI run said resources "already exist"</b></summary>
<br />
No remote state backend, so each runner started from empty state. Moved state to S3 with locking and wrote an idempotent cleanup script for orphaned resources.
</details>

<details>
<summary><b>Pods couldn't reach instance metadata</b></summary>
<br />
The IMDSv2 hop limit of 1 blocks responses to containers. Raised it with a custom EKS launch template.
</details>

<details>
<summary><b>Terraform destroy stuck on External Secrets</b></summary>
<br />
The CRDs were removed before the objects depending on them. Disabled the dependent config, cleaned up state, emptied the bucket, and finished a clean teardown.
</details>

---

### ✍️ Writing

- [Build a Three-Tier Web App](https://medium.com/@cloudopstechlead/build-a-three-tier-web-app-8762da58ea7a): a 31-minute serverless AWS walkthrough
- [My Docker engineering interview with a big tech AI company](https://medium.com/@cloudopstechlead/i-had-an-engineering-interview-the-other-day-with-a-big-tech-ai-company-for-a-docker-engineering-e41a671cd9c7): what the role involved and how I prepared

---

### 📊 GitHub activity

<p align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=Harkanni&show_icons=true&count_private=true&hide_border=true&bg_color=00000000&title_color=2E57F0&icon_color=2E57F0&text_color=8B9BB4" alt="Harkanni's GitHub stats" />
  <img height="165" src="https://streak-stats.demolab.com?user=Harkanni&hide_border=true&background=00000000&ring=2E57F0&fire=2E57F0&currStreakLabel=2E57F0&sideLabels=8B9BB4&currStreakNum=8B9BB4&sideNums=8B9BB4&dates=8B9BB4" alt="Harkanni's GitHub streak" />
</p>

<p align="center">
  <img width="100%" src="https://github-readme-activity-graph.vercel.app/graph?username=Harkanni&bg_color=00000000&color=8B9BB4&line=2E57F0&point=2E57F0&area=true&area_color=2E57F0&hide_border=true" alt="Harkanni's contribution graph" />
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:2E57F0,100:13233A&height=110&section=footer" alt="" width="100%" />
</p>
