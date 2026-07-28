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
| [Oracle Linux & systems](#oracle-linux--systems) | OL tutorials, UEK, containers, QEMU, VPN | curated |
| [Systems & fun projects](#8-systems--side-projects) | Raspberry Pi, VPN, Rust, VB | 6 |
| [Organizations review](#organizations-review--all-github-orgs) | Every org you belong to + cleanup notes | 7 orgs |
| [Frontend / fullstack](#9-frontend--fullstack) | React + backend samples | 3 |

---

## 1. Go · APIs

**Golang tutorials for students** — from Python bridge and language workshops to Gin/Postgres and full-stack **gRPC**. Each lab has an SEO-friendly README (tutorial title, FAQ, keywords).

| # | Lab | Level | What you'll practice | Status |
|---|-----|-------|----------------------|--------|
| 0 | [goforpython](https://github.com/saurabhahuja71/goforpython) — *Go for Python developers* | Beginner | Side-by-side Python vs Go | README ready |
| 1 | [golang-workshop](https://github.com/saurabhahuja71/golang-workshop) — *Golang workshop basics* | Beginner | Arrays, slices, maps, JSON, concurrency | README ready |
| 2 | [gotraining-labs](https://github.com/saurabhahuja71/gotraining-labs) — *Go training labs* | Beginner → Intermediate | Pointers, structs, interfaces, IO | README ready |
| 3 | [fullstack-go-bookapp-example](https://github.com/saurabhahuja71/fullstack-go-bookapp-example) — *Gin + PostgreSQL book app* | Intermediate | REST API + HTML templates | README ready |
| 4 | [grpc-golang-todo](https://github.com/saurabhahuja71/grpc-golang-todo) — *gRPC Go full-stack todo* | Intermediate | gRPC, grpc-gateway, React, Postgres | README ready |

**Related (Java REST design, not Go):** [User-Management-REST-Service](https://github.com/saurabhahuja71/User-Management-REST-Service) — Jakarta EE user CRUD (layered architecture) · README ready

**Coming soon (currently private — will be opened after cleanup):** REST API samples, simple Go API demos.

## 2. Python · Data · APIs

**Python tutorials for students** — browser playground → FastAPI/Flask full stack → ML notebooks. Each lab has an SEO-friendly README (tutorial title, FAQ, keywords).

| # | Lab | Level | What you'll practice | Status |
|---|-----|-------|----------------------|--------|
| 0 | [python-by-example](https://github.com/saurabhahuja71/python-by-example) — *Python in the browser (Pyodide)* | Beginner | Interactive Python playground | README ready |
| 1 | [react-fastapi-todo](https://github.com/saurabhahuja71/react-fastapi-todo) — *FastAPI + React + PostgreSQL* | Intermediate | Full-stack todo, OpenAPI, Compose | README ready |
| 2 | [pets-updates](https://github.com/saurabhahuja71/pets-updates) — *Flask Pets + GitHub workshop* | Beginner → Intermediate | Flask/SQLAlchemy + Copilot labs | README ready |
| 3 | [sample-regression-model](https://github.com/saurabhahuja71/sample-regression-model) — *Linear regression (scikit-learn)* | Beginner (ML) | Bangalore rent prediction | README ready |
| 4 | [datascienceandmachinelearning](https://github.com/saurabhahuja71/datascienceandmachinelearning) — *NumPy / Pandas notebooks* | Intermediate | Multi-day DS curriculum | README ready |
| 5 | [algotrading-sample](https://github.com/saurabhahuja71/algotrading-sample) — *Algo trading learning stub* | Intermediate | Datetime + strategy scaffold | README ready |

**Containers companion:** [hello](https://github.com/saurabhahuja71/hello) — multi-arch Docker/buildah Hello World · README ready

**Coming soon (private):** Flask REST demos, cloud-native Python sample.

## 3. Java · Helidon microservices

**Helidon MicroProfile tutorials for students** — a numbered mini-course from unit testing to Slack integration. Each lab has an SEO-friendly README (tutorial title, FAQ, keywords) so Google and GitHub search can find them.

Do them in order:

| # | Lab | Level | What you'll practice | Status |
|---|-----|-------|----------------------|--------|
| 0 | [junit-labs](https://github.com/saurabhahuja71/junit-labs) — *JUnit 5 tutorial for beginners* | Beginner | Unit testing with JUnit Jupiter | README ready |
| 1 | [helidon-cloudnative-microservice-sample](https://github.com/saurabhahuja71/helidon-cloudnative-microservice-sample) — *Helidon cloud-native REST microservice* | Beginner+ | REST, health, metrics, Docker, K8s | README ready |
| 2 | [helidon-rest-db-connection-demo](https://github.com/saurabhahuja71/helidon-rest-db-connection-demo) — *Helidon JPA + H2 database* | Intermediate | REST + JPA + transactions | README ready |
| 3 | [helidon-openapi-demo](https://github.com/saurabhahuja71/helidon-openapi-demo) — *Helidon OpenAPI / Swagger UI* | Intermediate | API documentation | README ready |
| 4 | [helidon-security-demo](https://github.com/saurabhahuja71/helidon-security-demo) — *Helidon Basic Auth & RBAC* | Intermediate | AuthN / AuthZ / roles | README ready |
| 5 | [helidon-slack-demo](https://github.com/saurabhahuja71/helidon-slack-demo) — *Helidon Slack webhook* | Intermediate | Outbound integrations | README ready |
| — | [learning-java-springboot](https://github.com/saurabhahuja71/learning-java-springboot) | Beginner → Intermediate | Spring Boot learning materials | Code-first |
| — | [react-java-todo](https://github.com/saurabhahuja71/react-java-todo) | Intermediate | React + Java full-stack todo | Code-first |

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

**IaC tutorials for students** — Oracle Cloud with Terraform/Ansible, Azure Jenkins, plus private samples coming later. SEO-friendly READMEs on each public lab.

| # | Lab | Level | What you'll practice | Status |
|---|-----|-------|----------------------|--------|
| 1 | [oci_terraform_samples](https://github.com/saurabhahuja71/oci_terraform_samples) — *Terraform on OCI* | Intermediate | VCN, compute, LB, buckets, modules | README ready |
| 2 | [oci_ansible_samples](https://github.com/saurabhahuja71/oci_ansible_samples) — *Ansible on OCI* | Intermediate | Playbooks, facts, httpd | README ready |
| 3 | [terraform-azure-jenkins-sample](https://github.com/saurabhahuja71/terraform-azure-jenkins-sample) — *Jenkins on Azure VM* | Intermediate | azurerm + bootstrap script | README ready |

**Coming soon (private):** AWS/GCP/EKS/GKE Terraform basics, larger Azure web sample, Helm basics.

## 6. CI/CD

**CI/CD tutorials for students** — GitHub Actions custom actions and repo hygiene templates. Jenkins-on-VM is under the Terraform track.

| # | Lab | Level | What you'll practice | Status |
|---|-----|-------|----------------------|--------|
| 1 | [github-action-demo](https://github.com/saurabhahuja71/github-action-demo) — *Docker container action* | Beginner | action.yml, Dockerfile, workflow | README ready |
| 2 | [sample-template-repo](https://github.com/saurabhahuja71/sample-template-repo) — *GitHub template hygiene* | Beginner | README, SECURITY, CONTRIBUTING | README ready |
| — | [terraform-azure-jenkins-sample](https://github.com/saurabhahuja71/terraform-azure-jenkins-sample) | Intermediate | Self-hosted Jenkins via Terraform | README ready |

**Coming soon (private):** Jenkins sample pipelines.

## 7. AI · Agents · MCP

**Modern AI labs for students** — Model Context Protocol, terminal agents, LangChain ReAct, and Redis RAG. Each has an SEO-friendly README (tutorial title, FAQ, keywords).

| # | Lab | Level | What you'll practice | Status |
|---|-----|-------|----------------------|--------|
| 0 | [mcp-demo](https://github.com/saurabhahuja71/mcp-demo) — *MCP server in Go* | Beginner → Intermediate | Tools, stdio/HTTP, Docker | README ready |
| 1 | [agenterm](https://github.com/saurabhahuja71/agenterm) — *Terminal AI agent + MCP client* | Intermediate | Ollama/OpenAI TUI, tools | README ready |
| 2 | [agentic-ai-sample](https://github.com/saurabhahuja71/agentic-ai-sample) — *LangChain ReAct agent* | Intermediate | OpenAI + Tavily search loop | README ready |
| 3 | [workshop-redis-ai](https://github.com/saurabhahuja71/workshop-redis-ai) — *Redis vector search & RAG* | Intermediate | Hybrid search, semantic cache, guardrails | README ready |

## Oracle Linux & systems

**Oracle Linux learning path** for students and engineers—plus links where this maintainer **actively participates** in Oracle open source (containers, database images, operators).

### A. Official Oracle Linux learning (start here)

Study and contribute **upstream** (do not rely on stale personal forks of huge trees):

| # | Upstream project | What you'll learn |
|---|------------------|-------------------|
| 1 | [oracle/oracle-linux](https://github.com/oracle/oracle-linux) | Scripts, examples, tutorials to get started with **Oracle Linux** |
| 2 | [oracle/migrate-to-ol](https://github.com/oracle/migrate-to-ol) | Migrate existing systems **to Oracle Linux** |
| 3 | [oracle/container-images](https://github.com/oracle/container-images) | Official **Oracle Linux container images** |
| 4 | [oracle/linux-uek](https://github.com/oracle/linux-uek) | **Unbreakable Enterprise Kernel (UEK)** sources |
| 5 | [oracle/bpftune](https://github.com/oracle/bpftune) | BPF-based auto-tuning on Linux |
| 6 | [oracle/dtrace](https://github.com/oracle/dtrace) | DTrace on Linux |
| 7 | [oracle/qemu](https://github.com/oracle/qemu) | QEMU tree used in Oracle contexts |

Docs worth bookmarking: [docs.oracle.com/oracle-linux](https://docs.oracle.com/en/operating-systems/oracle-linux/) · [yum.oracle.com](https://yum.oracle.com/)

### B. Active open-source participation (containers & data)

These are **not “toy labs”**—they are production Oracle OSS repos this maintainer contributes to via PRs:

| Project | Focus | How to learn |
|---------|--------|--------------|
| [oracle/docker-images](https://github.com/oracle/docker-images) | Dockerfiles for Oracle Database, Java, Instant Client, … | Read `OracleDatabase/`, build lab images, study PR history |
| [oracle/oracle-database-operator](https://github.com/oracle/oracle-database-operator) | Kubernetes operator for Oracle Database | Operator patterns on OL/OKE-style clusters |

Personal working fork (for PRs only—prefer upstream for students): [saurabhahuja71/docker-images](https://github.com/saurabhahuja71/docker-images)

### C. Personal companion labs (SEO READMEs)

| Lab | Level | Practice |
|-----|-------|----------|
| [raspios-qemu](https://github.com/saurabhahuja71/raspios-qemu) | Intermediate | **QEMU aarch64 on Oracle Linux 9** hosts (bundle pattern when packages are missing) |
| [oraclevpn](https://github.com/saurabhahuja71/oraclevpn) | Intermediate | **Podman** + OpenConnect/AnyConnect-style VPN container |
| [hello](https://github.com/saurabhahuja71/hello) | Beginner+ | Multi-arch **buildah/Docker** images (amd64/arm64) |

### Suggested 2-week OL starter plan

| Week | Focus | Actions |
|------|--------|---------|
| 1 | Install & basics | Install OL (or OL container), work through [oracle/oracle-linux](https://github.com/oracle/oracle-linux), try [migrate-to-ol](https://github.com/oracle/migrate-to-ol) docs |
| 1 | Containers | Pull/build from [container-images](https://github.com/oracle/container-images); multi-arch with [hello](https://github.com/saurabhahuja71/hello) |
| 2 | Virtualization | [raspios-qemu](https://github.com/saurabhahuja71/raspios-qemu) on an OL9 laptop/server |
| 2 | Product containers | Skim [docker-images](https://github.com/oracle/docker-images) `OracleDatabase` samples (licensing applies) |

### SEO tags for this track

`oracle-linux` `uek` `enterprise-linux` `podman` `qemu` `containers` `oracle-database` `docker-images` `ol9` `linux-admin` `tutorial`

## 8. Systems & side projects

> Prefer the **[Oracle Linux & systems](#oracle-linux--systems)** track for OL/UEK/container study. This section keeps smaller personal experiments.

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

## Organizations review — all GitHub orgs

Complete inventory of GitHub **organizations** associated with [@saurabhahuja71](https://github.com/saurabhahuja71) (from API membership). Use this section to decide what students should follow vs what to archive or hide.

| Org | Role | Public on profile? | Public repos (approx.) | Purpose (today) | Student relevance | Suggested action |
|-----|------|--------------------|------------------------|-----------------|-------------------|------------------|
| [oracle](https://github.com/oracle) | member | **Yes** | ~315 | Open Source at Oracle (Graal, OCI SDKs, WebLogic, docker-images, OL, …) | **High** — primary professional OSS | Keep; link from Oracle Linux & container tracks |
| [Utilties](https://github.com/Utilties) *(name spelling)* | **admin** | No | ~35 | “Placeholder for forked repos” + skills sandboxes | **Low** for portfolio | Review forks; delete unused; rename org if kept |
| [LeafixOS](https://github.com/LeafixOS) | **admin** | No | 3 | Arch-based OS experiment (`leafix-iso`, forum) | Medium if ISO is real | Fill READMEs or archive if abandoned |
| [quantdlinux](https://github.com/quantdlinux) | **admin** | No | 2 | Debian-based QuantD Linux (`quantd-iso`, site) | Medium (distro/ISO learners) | SEO README + link from systems track if active |
| [quantg-linux](https://github.com/quantg-linux) | **admin** | No | 0 public (`quantg-iso` private) | QuantG ISO placeholder | Low until public | Publish or merge into quantdlinux |
| [quantr-linux](https://github.com/quantr-linux) | **admin** | No | 0 | Empty org | None | **Delete org** or park a single README |
| [Tradebots71](https://github.com/Tradebots71) | **admin** | No | 0 public (private trading bots) | Covered-call / m.Stock bots | None for public students | Keep private; never expose keys; optional later “paper trading” lab |

### Org-by-org notes

#### 1. `oracle` — keep & highlight

- **What it is:** Oracle’s main public OSS org ([developer.oracle.com/open-source](https://developer.oracle.com/open-source.html)).
- **Why it matters for students:** production-grade code, real PR process, Oracle Linux, containers, operators, Graal, OCI SDKs.
- **Your angle:** active PRs on **docker-images**, **oracle-database-operator**, plus OL/UEK/container learning path above.
- **Do not** treat personal forks as the source of truth—send students to `oracle/...` upstream.

#### 2. `Utilties` — cleanup candidate
### Utilties cleanup status (safe batch)

**Planned keep:** `docker-images`, `oracle-database-operator` (forks), plus originals `raspberrypios`, `oraclelinux-docker`, `ubuntu-docker`, `paxosworkshop`.

**Planned delete (31 one-shot forks):** GitHub Skills (`introduction-to-github`, `hello-github-actions`, `github-pages`, `communicate-using-markdown`, `review-pull-requests`), `Spoon-Knife`, and unused forks (`grafana`, `kubespray`, `fzf`, `nushell`, `bottlerocket`, `meetup-golang`, …).

**Blocked:** GitHub CLI token is missing the `delete_repo` scope (`HTTP 403`). To finish cleanup on a machine with `gh` logged in as org admin:

```bash
gh auth refresh -h github.com -s delete_repo
# then run the safe-batch script (saved as utilties-safe-cleanup.sh) or:
# for each non-keeper fork: gh repo delete Utilties/NAME --yes
```



- **What it is:** Admin org described as *“Placeholder for forked repos”* (note the spelling **Utilties**).
- **Contains:** forks such as `docker-images`, `oracle-database-operator`, GitHub Skills sandboxes (`introduction-to-github`, …), private `oraclelinux-docker` / `ubuntu-docker`.
- **Problem:** duplicates personal forks; noisy for discovery; typo in org name.
- **Suggested cleanup:**
  1. List every repo → keep only forks with **open PRs** or unique commits.
  2. Delete skills one-shot repos after completion.
  3. Either rename org to something clear (`saurabh-forks`) or fold remaining work under the user account.
  4. Document in org profile README: “Working forks only — prefer upstream.”

#### 3. `LeafixOS` — productize or archive

- Repos: `leafix-iso`, `leafix-forum`, `.github`.
- If ISO builds still matter: add SEO READMEs + install docs + link from systems track.
- If not maintained: archive the org repos and pin a “historical” note.

#### 4. `quantdlinux` — distro track (active-ish)

- `quantd-iso` — Debian-based ISO (you already merged prep/release PRs).
- `quantdlinux.github.io` — project site.
- **Next:** student-facing README (build ISO, burn, first boot), screenshots, license clarity.
- Optional: link under [Oracle Linux & systems](#oracle-linux--systems) as “related community distro experiments” only if you want that brand public.

#### 5. `quantg-linux` / `quantr-linux` — empty or private-only

- **quantg-linux:** private `quantg-iso` only → either open-source with README or delete org.
- **quantr-linux:** zero repos → **delete** empty org to reduce clutter.

#### 6. `Tradebots71` — keep private

- Private: `covered_call_bot`, `covered_call_bot_mstock`.
- **Not** part of the public student curriculum (financial risk + secrets).
- Hard rules: no API keys in git; prefer paper/sandbox modes; separate from `learning-path`.

### Summary scorecard

| Priority | Orgs | Action |
|----------|------|--------|
| **Strategic** | `oracle` | Feature in hub + profile; contribute upstream |
| **Tidy** | `Utilties` | Cull forks/skills; rename or document |
| **Decide** | `LeafixOS`, `quantdlinux` | Ship docs or archive |
| **Remove / merge** | `quantg-linux`, `quantr-linux` | Empty/private-only noise |
| **Private only** | `Tradebots71` | Stay off public learning hub |

### Profile visibility

Currently **only `oracle` is public** on the GitHub profile org list. Other orgs are private membership or not shown—fine for experiments; promote an org only when its README and purpose are clear.

### Related links

- Student hub: [learning-path](https://github.com/saurabhahuja71/learning-path)
- Oracle Linux track: [Oracle Linux & systems](#oracle-linux--systems)
- Profile: [saurabhahuja71.github.io](https://saurabhahuja71.github.io)

## About the author

**Saurabh Ahuja** — Principal Member of Technical Staff (Oracle), cloud & infrastructure, **Oracle Linux**, Kubernetes, Go, operators, and Oracle container images.

- Profile: [saurabhahuja71](https://github.com/saurabhahuja71)
- Site: [saurabhahuja71.github.io](https://saurabhahuja71.github.io)
- LinkedIn: [saurabhahuja71](https://linkedin.com/in/saurabhahuja71)

---

## License note

Each lab keeps its **own** license (or none yet). Check the individual repository before reusing code in coursework or products.

---

*Progress: hub + curriculum tracks + Oracle Linux + **orgs review** → next: Utilties/empty-org cleanup or open private demos.*
