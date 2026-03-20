<!-- Header -->
<div align="center">

```
████████╗██╗   ██╗███╗   ██╗████████╗██╗   ██╗
╚══██╔══╝██║   ██║████╗  ██║╚══██╔══╝██║   ██║
   ██║   ██║   ██║██╔██╗ ██║   ██║   ██║   ██║
   ██║   ██║   ██║██║╚██╗██║   ██║   ██║   ██║
   ██║   ╚██████╔╝██║ ╚████║   ██║   ╚██████╔╝
   ╚═╝    ╚═════╝ ╚═╝  ╚═══╝   ╚═╝    ╚═════╝ 
```

### `mwakalasya@systems:~$ whoami`

*Just love computers man*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/tuntu-mwakalasya)

</div>

---

## ⚡ What I'm Building

```go
type Engineer struct {
    Focus       []string
    CurrentWork []string
    Interests   []string
}

me := Engineer{
    Focus: []string{
        "Scalable System Design",
        "Distributed Systems",
    },
    CurrentWork: []string{
        "Distributed High-Performance Key-Value Store — Golang",
        "Distributed Content Ingestion Pipeline  — Netflix-scale architecture",
        "Project Lazarus — Chaos-driven backup integrity validation",
    },
    Interests: []string{
        "Artificial Intelligence & Machine Learning",
        "Mathematics",
    },
}
```

---

## 🛠 Tech Stack

### Languages
![Go](https://img.shields.io/badge/Go-%2300ADD8.svg?style=for-the-badge&logo=go&logoColor=white)
![C](https://img.shields.io/badge/C-%2300599C.svg?style=for-the-badge&logo=c&logoColor=white)
![C++](https://img.shields.io/badge/C++-%2300599C.svg?style=for-the-badge&logo=c%2B%2B&logoColor=white)
![Java](https://img.shields.io/badge/Java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Python](https://img.shields.io/badge/Python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)

### Infrastructure & Cloud
![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-%23326CE5.svg?style=for-the-badge&logo=kubernetes&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![OrbStack](https://img.shields.io/badge/OrbStack-000000?style=for-the-badge&logo=orbstack&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-%235835CC.svg?style=for-the-badge&logo=terraform&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)

---

## 🔬 Areas of Focus

| Domain | What I'm Exploring |
|---|---|
| 🗄️ **Distributed Systems** | Consensus protocols, replication strategies, partition tolerance |
| ⚙️ **System Design** | Designing systems that scale horizontally without sacrificing consistency |
| 🤖 **AI / ML** | Model architecture, inference pipelines, applied ML at scale |
| 📐 **Mathematics** | Linear algebra, probability theory, stochastic processes |

---

## 🏗 Active Projects

### ☣️ [`project-lazarus`](https://github.com/Tmwakalasya/project-lazarus) — Automated Data Integrity Pipeline
> *"Trust, but Verify."*
>
> A chaos engineering platform that validates database backups by intentionally corrupting them.
> Existence of a backup file isn't enough — silent corruption and version skew can render backups useless when it matters most.
> Lazarus **proves** integrity by acting as a Chaos Monkey: it tries to break the data to confirm the validation logic actually catches it.
>
> **Pipeline lifecycle:**
> `Dump (Postgres 13)` → `Sanitize (version skew via sed)` → `Sabotage (chaos injection)` → `Restore (ephemeral clean-room container)` → `Verify (row-count analysis + alerts)`
>
> **Key engineering decisions:**
> - **Version skew handling** — Airflow runs Postgres 17 client tools against a v13 production DB; a `sed` layer strips incompatible directives on the fly
> - **Fail-fast reliability** — enforces `-v ON_ERROR_STOP=1` on all restores; one bad byte crashes the pipeline immediately
> - **Secrets hygiene** — zero hardcoded credentials; all secrets injected via Docker Compose from a git-ignored `.env`
> - **Data Bridge pattern** — Docker Volume mounts bridge the isolated filesystems of the Airflow worker and DB containers
>
> **Stack:** Python · PostgreSQL · Apache Airflow · Docker · Docker Compose · OrbStack
>
> **What's next:** Multi-DB support (MySQL, MongoDB) · Restore-time performance metrics as a reliability KPI

---

### `distributed-kv` — High-Performance Key-Value Store
> Built in Go. Focuses on performance, consistency, and fault tolerance at scale.
> Exploring Raft consensus, WAL persistence, and LSM-tree storage engines.

### `ingest-pipeline` — Distributed Content Ingestion
> Netflix-inspired architecture for large-scale media ingestion.
> Event-driven, horizontally scalable, built for throughput.

---

<div align="center">

*"The art of systems design is knowing what to leave out."*

</div>
