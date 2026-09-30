<div align="center">

  <img src="https://raw.githubusercontent.com/gradientgeeks/.github/main/profile/assets/logo.png" width="160" alt="Gradient Geeks Logo" />

  # Gradient Geeks

  ### High-Performance Distributed Systems • Cloud-Native Infrastructure • Systems Programming

  [![Website](https://img.shields.io/badge/Website-gradientgeeks.com-00E5FF?logo=googlechrome&logoColor=white)](https://gradientgeeks.com)
  [![Sponsor](https://img.shields.io/badge/Sponsor_on_GitHub-%E2%9D%A4-ea4aaa?style=flat&logo=githubsponsors&logoColor=white)](https://github.com/sponsors/gradientgeeks)
  [![AeroStream](https://img.shields.io/badge/AeroStream-Core_Engine-00ADD8?logo=apachekafka&logoColor=white)](https://aerostream.gradientgeeks.com/)
  [![Docs](https://img.shields.io/badge/Docs-MkDocs_Material-526CFE?logo=materialformkdocs&logoColor=white)](https://aerostream.gradientgeeks.com/docs/)
  [![License](https://img.shields.io/badge/License-Apache--2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

  <br/>

</div>

---

## 🌟 About Gradient Geeks

**Gradient Geeks** is an open-source engineering collective dedicated to building ultra-low-latency, resilient, and hardware-efficient distributed systems. We bridge the gap between mechanical sympathy and developer ergonomics—leveraging modern systems languages (**Rust**, **Go**) to craft infrastructure capable of processing hundreds of thousands of operations per second with microsecond tail latencies.

---

## 💖 Support Our Work via GitHub Sponsors

We believe in open infrastructure and building software with zero vendor lock-in. Your sponsorship directly accelerates our open-source research, hardware benchmark infrastructure (AWS / bare-metal), and multi-platform client SDK development.

<div align="center">

[![Sponsor Gradient Geeks](https://img.shields.io/badge/Sponsor_Gradient_Geeks-ea4aaa?style=for-the-badge&logo=githubsponsors&logoColor=white)](https://github.com/sponsors/gradientgeeks)

*Sponsorships are powered by GitHub Sponsors with Stripe integration.*

</div>

---

## 🚀 Ongoing Flagship: AeroStream

[**AeroStream**](https://github.com/gradientgeeks/aerostream) is an ultra-high-performance distributed event-streaming and messaging engine engineered for extreme throughput, microsecond latencies, and modern multi-cloud workloads.

```
                          ┌────────────────────────┐
                          │   Kafka Clients        │
                          │   (:9092 / :9093)      │
                          └───────────┬────────────┘
                                      │ Kafka Wire Protocol
                                      ▼
┌─────────────────────────┐       ┌────────────────────────┐
│  Go Control Plane       │       │  Rust Data Plane       │
│  (go-controller/)       │◄─────►│  (rust-broker/)        │
│  - HashiCorp Raft FSM   │ gRPC  │  - Shard-per-Core      │
│  - Schema Registry      │:8001  │  - Zero-Copy Storage   │
│  - Kafka Connect 100%   │       │  - Paced Page Cache    │
│  - Web Console UI:9001  │       │  - Native Port :9091   │
└─────────────────────────┘       └────────────────────────┘
```

Built with a **Dual-Engine Architecture**—pairing a resilient **Go-based Raft control plane** with a zero-copy **Rust-based shard-per-core storage and networking data plane**—AeroStream delivers next-generation event streaming with Kafka wire-protocol compatibility, built-in multi-cloud tiered storage, schema governance, inline stream transforms, and an integrated Web Management Console.

### 📦 AeroStream Ecosystem Repositories

| Repository | Description | Tech Stack | Status |
| :--- | :--- | :--- | :---: |
| [**`aerostream`**](https://github.com/gradientgeeks/aerostream) | Primary distributed engine, Raft consensus daemon, and zero-copy broker | Go 1.26 • Rust 1.98 • Docker | [![Status](https://img.shields.io/badge/Engine-v0.1.0-orange)](https://github.com/gradientgeeks/aerostream) |
| [**`aerostream-sdk`**](https://github.com/gradientgeeks/aerostream-sdk) | Official client SDKs for ultra-low-latency native binary protocol (`0xAE 0x01` on `:9091`) | Go • Rust • Java • .NET • Node.js | [![Status](https://img.shields.io/badge/SDKs-Preview-blue)](https://github.com/gradientgeeks/aerostream-sdk) |
| [**`aerostream-ui`**](https://github.com/gradientgeeks/aerostream-ui) | Modern Web Management Console with dynamic topology, live message inspector, and lag monitoring | Angular 21 • Material • Tailwind | [![Status](https://img.shields.io/badge/UI-Angular_21-DD0031)](https://github.com/gradientgeeks/aerostream-ui) |
| [**`aerostream-docs`**](https://github.com/gradientgeeks/aerostream-docs) | Official documentation portal, architecture whitepapers, LaTeX math formulas, and interactive diagrams | MkDocs Material • MathJax | [![Docs](https://img.shields.io/badge/Docs-Live-526CFE)](https://aerostream.gradientgeeks.com/docs/) |
| [**`aerostream-examples`**](https://github.com/gradientgeeks/aerostream-examples) | Production-ready example applications across multiple languages and frameworks | Java • Go • Rust • C# • FastAPI | [![Examples](https://img.shields.io/badge/Examples-Multi--Lang-success)](https://github.com/gradientgeeks/aerostream-examples) |

### ⚡ Performance Highlights (OpenMessaging Benchmark)

Measured with the Linux Foundation **OpenMessaging Benchmark (OMB)** framework on an AWS `c6id.2xlarge` (8 vCPU, 16 GiB NVMe):

* 🚀 **100,000 msg/s** (fixed load): **0.7 ms** $p_{50}$ • **1.4 ms** $p_{99}$ • **0 errors**
* ⚡ **200,000 msg/s** (fixed load): **0.7 ms** $p_{50}$ • **1.7 ms** $p_{99}$ • **0 errors**
* 🏁 **Peak Saturation**: **271,350 msg/s (265.0 MB/s)** sustained with zero record loss.

---

## 🛡️ Quantum-Safe Identity: DilithiAuth

[**DilithiAuth**](https://github.com/gradientgeeks/dilithiauth) is a research-grade, post-quantum Identity Provider (IdP) and OAuth 2.0 Authorization Server designed to neutralize **"Harvest Now, Forge Later" (HNFL)** attacks.

[![Repository](https://img.shields.io/badge/Repo-gradientgeeks%2Fdilithiauth-blue?logo=github)](https://github.com/gradientgeeks/dilithiauth)
[![PQC](https://img.shields.io/badge/PQC-NIST_FIPS_204_ML--DSA--44-blueviolet)](https://github.com/gradientgeeks/dilithiauth)
[![Classical](https://img.shields.io/badge/Classical-Ed25519_Hybrid-black)](https://github.com/gradientgeeks/dilithiauth)
[![Go](https://img.shields.io/badge/Go-1.24+-00ADD8?logo=go&logoColor=white)](https://github.com/gradientgeeks/dilithiauth)
[![License](https://img.shields.io/badge/License-Apache--2.0-blue.svg)](https://github.com/gradientgeeks/dilithiauth/blob/main/LICENSE)

* **Hybrid Cryptographic Signatures**: Seamlessly merges classical **Ed25519** with post-quantum **ML-DSA-44** (NIST FIPS 204 Module-Lattice Digital Signature Algorithm).
* **Solves Token Bloat**: Post-quantum signatures are ~2.4 KB (vs. 64 B Ed25519). DilithiAuth solves reverse proxy header drops via the **Edge Proxy Offloading Gateway**, **Thin JWTs** with out-of-band `SigStore` verification, and compact **CBOR Web Tokens (CWT)**.
* **Full OAuth 2.0 & OIDC Engine**: PKCE authorization code grant, distributed key rotation (`KeyStore`), authorization code deduplication (`AuthzStore`), and modern Developer Portal.

---

## 🛠 Other Open-Source Initiatives

* [**Aegis**](https://github.com/gradientgeeks/aegis): Cloud security posture management and runtime policy enforcement engine.
* [**Bhasa**](https://github.com/gradientgeeks/bhasa): Compiled programming language and compiler research.

---

## 📬 Connect & Collaborate

* 🌐 **Website**: [gradientgeeks.com](https://gradientgeeks.com)
* 📖 **Documentation Portal**: [aerostream.gradientgeeks.com/docs/](https://aerostream.gradientgeeks.com/docs/)
* 📧 **Contact**: [contact@gradientgeeks.com](mailto:contact@gradientgeeks.com)
* 🤝 **Governance**: All contributions are welcomed under the [AeroStream CLA](https://aerostream.gradientgeeks.com/docs/cla/) and Apache 2.0.
