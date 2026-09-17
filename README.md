<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/hero-dark.svg">
  <img src="assets/hero-light.svg" alt="Akanni Emmanuel, Cloud and DevOps Engineer. I design AWS infrastructure around how applications actually run." width="100%">
</picture>

<p align="center">
  <!-- Replace YOUR-PORTFOLIO-URL once the site is live on CloudFront -->
  <a href="https://YOUR-PORTFOLIO-URL"><img src="https://img.shields.io/badge/Portfolio-2E57F0?style=for-the-badge&logo=amazonaws&logoColor=white" alt="Portfolio"></a>
  <a href="https://www.linkedin.com/in/akanniemmanuel/"><img src="https://img.shields.io/badge/LinkedIn-13233A?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="https://medium.com/@cloudopstechlead"><img src="https://img.shields.io/badge/Medium-13233A?style=for-the-badge&logo=medium&logoColor=white" alt="Medium"></a>
  <a href="https://x.com/the_tech_lead"><img src="https://img.shields.io/badge/X-13233A?style=for-the-badge&logo=x&logoColor=white" alt="X"></a>
  <a href="mailto:akanniemmanuel2001@gmail.com"><img src="https://img.shields.io/badge/Email_me-13233A?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
  <a href="https://www.credly.com/badges/e5ab176b-0334-428c-955b-ead8ee56cdd8/public_url"><img src="https://img.shields.io/badge/AWS_Educate-Verified_on_Credly-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white" alt="AWS Educate Cloud Computing 101, verified on Credly"></a>
</p>

<br>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/terminal-dark.svg">
  <img src="assets/terminal-light.svg" alt="Terminal showing kubectl get pods and terraform output: Cloud and DevOps Engineer based in Lagos, working with AWS, Terraform, Amazon EKS, Helm, GitHub Actions and Docker" width="100%">
</picture>

## The stack, layer by layer

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/stack-dark.svg">
  <img src="assets/stack-light.svg" alt="Stack by layer. Application: Go, TypeScript, React, Next.js, Node.js, Python. Delivery: GitHub Actions, OIDC, Docker, ECR, Helm, Netlify, Render. Orchestration: Kubernetes, EKS, Load Balancer Controller, External Secrets, IRSA. Infrastructure as code: Terraform, Ansible, Bash. AWS: VPC, EC2, IAM, S3, CloudFront, Lambda, RDS, DynamoDB, ElastiCache, CloudWatch" width="100%">
</picture>

## Flagship build

<a href="https://github.com/Harkanni/project-bedrock-0324">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/bedrock-dark.svg">
    <img src="assets/bedrock-light.svg" alt="Project Bedrock: a five-service retail store on Amazon EKS, provisioned with Terraform, with IRSA, EKS Access Entries, External Secrets and CloudWatch observability" width="100%">
  </picture>
</a>

## More builds

<p>
  <picture><source media="(prefers-color-scheme: dark)" srcset="assets/starttech-dark.svg"><img src="assets/starttech-light.svg" alt="StartTech: React and Go on EKS" width="49%"></picture>
  <picture><source media="(prefers-color-scheme: dark)" srcset="assets/huddle-dark.svg"><img src="assets/huddle-light.svg" alt="Huddle: cloud engineer for a cross-functional team" width="49%"></picture>
  <a href="https://github.com/Harkanni/3-tier-architecture"><picture><source media="(prefers-color-scheme: dark)" srcset="assets/threetier-dark.svg"><img src="assets/threetier-light.svg" alt="Three-Tier Web App on AWS" width="49%"></picture></a>
  <a href="https://github.com/Harkanni/status-chunks"><picture><source media="(prefers-color-scheme: dark)" srcset="assets/status-dark.svg"><img src="assets/status-light.svg" alt="Status Splitter: privacy-first video tool" width="49%"></picture></a>
  <picture><source media="(prefers-color-scheme: dark)" srcset="assets/muchtodo-dark.svg"><img src="assets/muchtodo-light.svg" alt="MuchToDo: a Go API in private subnets" width="49%"></picture>
  <picture><source media="(prefers-color-scheme: dark)" srcset="assets/odoo-dark.svg"><img src="assets/odoo-light.svg" alt="odoo-cloud: provision with Terraform, configure with Ansible" width="49%"></picture>
</p>

## Incident log

Most of what I know came from things breaking. Open one.

<details>
<summary><b>🔴 EKS nodes never joined the cluster</b> &nbsp;·&nbsp; <code>NodeCreationFailure</code></summary>

> **Cause:** node subnets had no route table association and public IP assignment was off, so nodes couldn't reach the control plane.<br>
> **Fix:** corrected subnet routing and IP settings in Terraform.<br>
> **Lesson:** a Kubernetes failure can start at the VPC layer.
</details>

<details>
<summary><b>🔴 Every CI run said resources "already exist"</b> &nbsp;·&nbsp; Terraform state</summary>

> **Cause:** no remote backend, so each runner started from empty state and parallel runs left orphaned resources.<br>
> **Fix:** S3 remote state with locking, plus an idempotent Bash cleanup script.
</details>

<details>
<summary><b>🔴 Pods couldn't reach instance metadata</b> &nbsp;·&nbsp; EKS networking</summary>

> **Cause:** the IMDSv2 hop limit of 1 drops responses that need an extra hop into a container.<br>
> **Fix:** a custom EKS launch template that raises the hop limit.
</details>

<details>
<summary><b>🔴 Logged-in users got a 401 on every request</b> &nbsp;·&nbsp; Go backend behind HTTPS</summary>

> **Cause:** Viper wasn't binding environment variables, so cookie domain and secure flags never applied in production.<br>
> **Fix:** explicit <code>BindEnv()</code> calls and correct <code>COOKIE_DOMAINS</code> and <code>SECURE_COOKIE</code> values.
</details>

<details>
<summary><b>🔴 <code>terraform destroy</code> got stuck halfway</b> &nbsp;·&nbsp; teardown</summary>

> **Cause:** External Secrets CRDs were removed before the objects that depended on them.<br>
> **Fix:** disabled the dependent config, cleaned stale state, emptied the bucket, finished a clean destroy.
</details>

## Writing

<p>
  <a href="https://medium.com/@cloudopstechlead/build-a-three-tier-web-app-8762da58ea7a"><picture><source media="(prefers-color-scheme: dark)" srcset="assets/post-threetier-dark.svg"><img src="assets/post-threetier-light.svg" alt="Build a Three-Tier Web App, on Medium" width="49%"></picture></a>
  <a href="https://medium.com/@cloudopstechlead/i-had-an-engineering-interview-the-other-day-with-a-big-tech-ai-company-for-a-docker-engineering-e41a671cd9c7"><picture><source media="(prefers-color-scheme: dark)" srcset="assets/post-docker-dark.svg"><img src="assets/post-docker-light.svg" alt="My Docker engineering interview with a big tech AI company, on Medium" width="49%"></picture></a>
</p>

<details>
<summary><b>GitHub stats</b></summary>
<br>
<p align="center">
  <img height="160" src="https://github-readme-stats.vercel.app/api?username=Harkanni&show_icons=true&count_private=true&hide_border=true&bg_color=00000000&title_color=2E57F0&icon_color=2E57F0&text_color=8B9BB4" alt="GitHub stats">
  <img height="160" src="https://streak-stats.demolab.com?user=Harkanni&hide_border=true&background=00000000&ring=2E57F0&fire=2E57F0&currStreakLabel=2E57F0&sideLabels=8B9BB4&currStreakNum=8B9BB4&sideNums=8B9BB4&dates=8B9BB4" alt="GitHub streak">
</p>
</details>

<p align="center"><img src="https://komarev.com/ghpvc/?username=Harkanni&label=profile%20views&color=2E57F0&style=flat-square" alt="Profile views"></p>
