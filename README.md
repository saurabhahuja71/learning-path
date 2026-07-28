# Learning Path — Labs for College Students & New Engineers

Curated hands-on repositories from [saurabhahuja71](https://github.com/saurabhahuja71) for **college students**, **early-career engineers**, and anyone learning cloud-native development.

These are **practice labs**, not production frameworks. Each track is ordered from easier → harder when possible. Start with one track; finish a lab before jumping tracks.

> **How to use this hub**
> 1. Pick a track that matches what you want to learn.
> 2. Open the lab repo → read its README → follow **Quick start**.
> 3. When a lab still has a thin README, treat the code as the source of truth and open an issue if you get stuck.
> 4. Prefer building something small of your own after each lab.

---

## Tracks at a glance

| Track | Best for | Labs |
|-------|----------|-----:|
| [Go](#1-go--apis) | Backend APIs, gRPC, workshops | 6 |
| [Python](#2-python--data--apis) | Flask/FastAPI, data, ML intro | 7 |
| [Java / Helidon](#3-java--helidon-microservices) | Microservices on the JVM | 8 |
| [Cloud & Kubernetes](#4-cloud-kubernetes--containers) | Docker, K8s, operators | 5 |
| [Terraform & IaC](#5-terraform--infrastructure-as-code) | Infra as code (OCI / Azure / AWS ideas) | 3 |
| [CI/CD](#6-cicd) | GitHub Actions, pipelines | 1 |
| [AI & Agents](#7-ai--agents--mcp) | MCP, agents, Redis+AI | 4 |
| [Systems & fun projects](#8-systems--side-projects) | Raspberry Pi, VPN, Rust, VB | 6 |
| [Frontend / fullstack](#9-frontend--fullstack) | React + backend samples | 3 |

---

## 1. Go · APIs

Learn idiomatic Go, HTTP APIs, gRPC, and workshop-style exercises.

| # | Lab | Level | What you'll practice |
|---|-----|-------|----------------------|
| 1 | [golang-workshop](https://github.com/saurabhahuja71/golang-workshop) | Beginner | Core Go workshop material |
| 2 | [gotraining-labs](https://github.com/saurabhahuja71/gotraining-labs) | Beginner → Intermediate | Guided training labs |
| 3 | [goforpython](https://github.com/saurabhahuja71/goforpython) | Beginner | Go mental model if you already know Python |
| 4 | [fullstack-go-bookapp-example](https://github.com/saurabhahuja71/fullstack-go-bookapp-example) | Intermediate | Small full-stack book app in Go |
| 5 | [grpc-golang-todo](https://github.com/saurabhahuja71/grpc-golang-todo) | Intermediate | gRPC service + todo domain |
| 6 | [User-Management-REST-Service](https://github.com/saurabhahuja71/User-Management-REST-Service) | Intermediate | REST service design |

**Coming soon (currently private — will be opened after cleanup):** REST API samples, simple Go API demos.

---

## 2. Python · Data · APIs

| # | Lab | Level | What you'll practice |
|---|-----|-------|----------------------|
| 1 | [python-by-example](https://github.com/saurabhahuja71/python-by-example) | Beginner | Python patterns by example |
| 2 | [react-fastapi-todo](https://github.com/saurabhahuja71/react-fastapi-todo) | Intermediate | FastAPI + React todo app |
| 3 | [pets-updates](https://github.com/saurabhahuja71/pets-updates) | Intermediate | Small product-style Python app |
| 4 | [sample-regression-model](https://github.com/saurabhahuja71/sample-regression-model) | Beginner (ML) | Minimal regression model |
| 5 | [datascienceandmachinelearning](https://github.com/saurabhahuja71/datascienceandmachinelearning) | Intermediate | Notebooks / DS & ML practice |
| 6 | [algotrading-sample](https://github.com/saurabhahuja71/algotrading-sample) | Intermediate | Algo-trading learning project *(README + code being improved)* |
| 7 | [hello](https://github.com/saurabhahuja71/hello) | Beginner | Multi-arch Docker image basics |

**Coming soon (private):** Flask REST demos, cloud-native Python sample.

---

## 3. Java · Helidon microservices

Treat the Helidon repos as a **mini course**. Do them in order.

| # | Lab | Level | What you'll practice |
|---|-----|-------|----------------------|
| 1 | [junit-labs](https://github.com/saurabhahuja71/junit-labs) | Beginner | Unit testing with JUnit |
| 2 | [learning-java-springboot](https://github.com/saurabhahuja71/learning-java-springboot) | Beginner → Intermediate | Spring Boot learning dump |
| 3 | [helidon-cloudnative-microservice-sample](https://github.com/saurabhahuja71/helidon-cloudnative-microservice-sample) | Intermediate | Cloud-native Helidon service |
| 4 | [helidon-rest-db-connection-demo](https://github.com/saurabhahuja71/helidon-rest-db-connection-demo) | Intermediate | REST + database connectivity |
| 5 | [helidon-openapi-demo](https://github.com/saurabhahuja71/helidon-openapi-demo) | Intermediate | OpenAPI on Helidon |
| 6 | [helidon-security-demo](https://github.com/saurabhahuja71/helidon-security-demo) | Intermediate | Security patterns |
| 7 | [helidon-slack-demo](https://github.com/saurabhahuja71/helidon-slack-demo) | Intermediate | Integrating external APIs (Slack) |
| 8 | [react-java-todo](https://github.com/saurabhahuja71/react-java-todo) | Intermediate | React front end + Java backend |

**Coming soon (private):** `hello-world-java`.

---

## 4. Cloud, Kubernetes & containers

| # | Lab | Level | What you'll practice |
|---|-----|-------|----------------------|
| 1 | [hello](https://github.com/saurabhahuja71/hello) | Beginner | Multi-arch container builds |
| 2 | [docker-scout-example](https://github.com/saurabhahuja71/docker-scout-example) | Beginner | Image scanning / Scout concepts *(thin — expand soon)* |
| 3 | [memcached-operator](https://github.com/saurabhahuja71/memcached-operator) | Advanced | Kubernetes operator pattern |
| 4 | [raspios-qemu](https://github.com/saurabhahuja71/raspios-qemu) | Intermediate | Raspberry Pi OS under QEMU |
| 5 | [oraclevpn](https://github.com/saurabhahuja71/oraclevpn) | Intermediate | VPN-related systems work |

**Coming soon (private):** Kubernetes basics, demo container app, Helm basics, single-node kubeadm Vagrant setup.

---

## 5. Terraform & infrastructure as code

| # | Lab | Level | What you'll practice |
|---|-----|-------|----------------------|
| 1 | [oci_terraform_samples](https://github.com/saurabhahuja71/oci_terraform_samples) | Beginner → Intermediate | Terraform on Oracle Cloud |
| 2 | [oci_ansible_samples](https://github.com/saurabhahuja71/oci_ansible_samples) | Beginner → Intermediate | Ansible on OCI |
| 3 | [terraform-azure-jenkins-sample](https://github.com/saurabhahuja71/terraform-azure-jenkins-sample) | Intermediate | Azure + Jenkins via Terraform |

**Coming soon (private):** AWS / GCP / EKS / GKE Terraform basics and larger Azure static+dynamic web sample.

---

## 6. CI/CD

| # | Lab | Level | What you'll practice |
|---|-----|-------|----------------------|
| 1 | [github-action-demo](https://github.com/saurabhahuja71/github-action-demo) | Beginner | GitHub Actions intro |

**Coming soon (private):** Jenkins sample pipelines.

---

## 7. AI · Agents · MCP

Newer labs — good if you want current AI tooling, not only classic backend.

| # | Lab | Level | What you'll practice |
|---|-----|-------|----------------------|
| 1 | [mcp-demo](https://github.com/saurabhahuja71/mcp-demo) | Beginner → Intermediate | Model Context Protocol basics |
| 2 | [agentic-ai-sample](https://github.com/saurabhahuja71/agentic-ai-sample) | Intermediate | Agentic AI sample |
| 3 | [agenterm](https://github.com/saurabhahuja71/agenterm) | Intermediate | Agent terminal / tooling |
| 4 | [workshop-redis-ai](https://github.com/saurabhahuja71/workshop-redis-ai) | Intermediate | Redis + AI workshop |

---

## 8. Systems & side projects

| Lab | Notes |
|-----|--------|
| [raspios-qemu](https://github.com/saurabhahuja71/raspios-qemu) | Boot Raspberry Pi OS under QEMU |
| [oraclevpn](https://github.com/saurabhahuja71/oraclevpn) | VPN project |
| [Rust-learning](https://github.com/saurabhahuja71/Rust-learning) | Rust practice |
| [vbcookbook](https://github.com/saurabhahuja71/vbcookbook) | Visual Builder cookbook |
| [vbstudiolabs](https://github.com/saurabhahuja71/vbstudiolabs) | VB Studio labs |
| [hello_flutter](https://github.com/saurabhahuja71/hello_flutter) | Flutter sample *(needs content)* |

---

## 9. Frontend · fullstack

| # | Lab | Level | What you'll practice |
|---|-----|-------|----------------------|
| 1 | [ahujasa-frontend-backend-sample](https://github.com/saurabhahuja71/ahujasa-frontend-backend-sample) | Intermediate | Front + back sample |
| 2 | [react-fastapi-todo](https://github.com/saurabhahuja71/react-fastapi-todo) | Intermediate | React + FastAPI |
| 3 | [react-java-todo](https://github.com/saurabhahuja71/react-java-todo) | Intermediate | React + Java |

---

## Suggested 4-week starter plan (college)

If you are early in college and want a structured month:

| Week | Focus | Labs |
|------|--------|------|
| 1 | Language fundamentals | `python-by-example` **or** `golang-workshop` |
| 2 | First API | `react-fastapi-todo` **or** `grpc-golang-todo` |
| 3 | Containers | `hello` + read about multi-arch builds |
| 4 | Cloud / automation | `oci_terraform_samples` **or** `github-action-demo` |

Stretch: pick one Helidon lab or `mcp-demo` in week 4 if you already know Java/AI.

---

## Repo quality legend

We are improving labs over time. Use this when you open a repo:

| Status | Meaning |
|--------|---------|
| **Ready** | Code + usable README (goal for all public labs) |
| **Code-first** | Code works; README is thin — follow source + issues |
| **Shell** | Placeholder — being filled or retired |
| **Private → public** | Good lab still private; will open after cleanup |

This hub will be updated as READMEs are standardized (what / audience / prerequisites / quick start / next lab).

---

## Contributing as a learner

You do **not** need to be an expert:

- Open an issue: “Lab X failed on Ubuntu 24.04 with error …”
- Suggest README fixes (typos, missing steps)
- Share what you built after finishing a track

Keep PRs small and focused. Prefer clarity over cleverness.

---

## About the author

**Saurabh Ahuja** — Principal Member of Technical Staff (Oracle), cloud & infrastructure, Kubernetes, Go, operators.

- Profile: [saurabhahuja71](https://github.com/saurabhahuja71)
- Site: [saurabhahuja71.github.io](https://saurabhahuja71.github.io)
- LinkedIn: [saurabhahuja71](https://linkedin.com/in/saurabhahuja71)

---

## License note

Each lab keeps its **own** license (or none yet). Check the individual repository before reusing code in coursework or products.

---

*This is step 1 of an ongoing cleanup: hub first → per-track READMEs → open strong private demos → retire empty shells.*
