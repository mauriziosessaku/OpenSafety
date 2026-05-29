# OpenSafety

**Open-source AI for pharmacovigilance** · University of Copenhagen, Drug Safety Group

> *The tools that protect patients should be held to the same standards as the science that informs clinical decisions. That means transparency. That means openness. That means peer review — not just for papers, but for the software we rely on every day.*

---

## The Problem

Every step of drug development is governed by transparency, peer review, and reproducibility. You cannot publish a clinical trial without registering it. You cannot claim a safety signal without showing your data.

And yet, the tools we use to do this science are proprietary, closed, and unverifiable. Most have no published whitepaper, no open code, no independent validation study. When you ask how the algorithm works, you get a commercial presentation, not a scientific answer.

This is a structural contradiction we cannot ignore.

| Current State | What We Need |
|---|---|
| No published whitepapers | Transparent, inspectable methods |
| No open source code | Peer-reviewed algorithms |
| No independent validation | Independent benchmarking |
| Commercial answers to scientific questions | Community-driven validation |
| Protected by patent law — cannot be challenged | Reproducible, auditable results |
| Black-box outputs influencing regulatory decisions | The same standards we apply to science |

---

## The Initiative

Our group at the University of Copenhagen is developing and releasing open-source tools specifically designed for the pharmacovigilance community. Tools that can be inspected, challenged, improved, and published. Tools that sit alongside — and can be validated against — the proprietary solutions currently in use.

**This is not a product. This is not a company. This is a public good for our scientific community.**

The infrastructure is open. The code is open. The results will be published.

### Focus Areas

| # | Macro-category | Examples |
|---|---|---|
| 01 | **Pharmacovigilance** | Signal detection and disproportionality analysis; individual case safety report processing; causality assessment; case narrative generation; literature monitoring; aggregate safety reporting (PSUR, PBRER) |
| 02 | **Pharmacoepidemiology** | Disease phenotyping from EHR and register data; exposure and outcome definition; confounder identification; causal inference and target trial emulation; real-world evidence generation |
| 03 | **Regulatory Science** | Regulatory document intelligence (SmPC, EPAR, labelling); benefit-risk assessment support; inspection readiness; compliance monitoring across EMA, FDA, MHRA, and WHO frameworks |

---

## Who Can Participate

You do not need to be a programmer to participate. The pharmacovigilance community — academics, regulators, industry scientists, and patient advocates — can and should shape how this field evolves.

### Academic scope and publication commitment

**Access to the OpenSafety infrastructure is granted exclusively for academic and scientific research purposes.**

Every project using the shared sandbox is expected to result in a peer-reviewed publication. This is not a bureaucratic requirement — it is the founding principle of this initiative. We are building this to advance the science of drug safety in the open, and publication is the mechanism by which that happens. Results that remain unpublished do not serve the community this infrastructure exists to support.

When you apply, you should be able to describe:
- The research question your project addresses
- The target journal or conference you intend to submit to
- A realistic timeline for manuscript preparation

Co-authorship or acknowledgement will be determined jointly during the scoping call, in line with ICMJE authorship criteria.

**Commercial use, proprietary development, and internal-only benchmarking are outside the scope of this initiative.**

You can contribute:
- Ideas and use cases
- Datasets
- Code and algorithms
- Domain expertise
- Feedback and engagement

---

## How to Join — Onboarding Procedure

### Step 1 — Send an email · *Rolling*
Write to **maurizio.sessa@sund.ku.dk** and include the following:

1. **Who you are** — name, role, institution, and country
2. **What you are working on** — a brief project description (2–5 sentences)
3. **What you need the infrastructure for** — e.g. signal detection, LLM benchmarking, narrative processing, disproportionality analysis
4. **What you can contribute** — data, code, domain expertise, or engagement
5. **Your publication plan** — the research question, target journal or conference, and expected timeline for manuscript submission

### Step 2 — Acknowledgement · *Day 1–5*
You will receive a confirmation within 5 working days. Every message is reviewed personally.

### Step 3 — Internal Triage · *Day 5–10*
We assess fit, resource needs, and overlap with existing work in the group.

### Step 4 — Decision · *Day 10*
Accept, defer, or redirect — you receive a tailored reply with next steps or a waitlist notice.

### Step 5 — Scoping Call · *Week 2–3*
A 30-minute call to define the use case, agree on access level, and align expectations.

### Step 6 — Sandbox Access · *Week 3*
Access is granted alongside a lightweight use agreement and data handling note.

### Step 7 — Ongoing Collaboration · *Ongoing*
Monthly check-ins or async updates. Outputs published openly with co-authorship or acknowledgement as appropriate.

---

## Infrastructure Configuration

The OpenSafety sandbox runs on the following hardware, hosted at the University of Copenhagen:

**Dell PowerEdge R7725 — Configuration #20 (with RAM upgrade)**

| Component | Specification |
|---|---|
| **CPU** | 2× AMD EPYC 9655 (96C/192T per socket, 192 cores total) |
| **GPU** | 1× NVIDIA H200 NVL (141 GB VRAM, single GPU) |
| **RAM** | 1,536 GB DDR5-6400 (upgraded from base 384 GB) |
| **Estimated cost** | ~794,000–800,000 DKK |
| **Rubus compliant** | Yes |

### Rationale

The base configuration is priced at 617,333 DKK, leaving approximately 182,667 DKK within the 800,000 DKK budget. Rather than leaving this headroom unused, the full margin is invested in maximising system RAM — bringing it from 384 GB up to 1,536 GB.

As a reference: Configuration #13 (same server, same CPU, 1,536 GB RAM, no GPU) is priced at 593,225 DKK — so the upgrade from 384 GB to 1,536 GB represents approximately 593,225 − 416,254 = ~177,000 DKK for the additional DIMMs, which fits comfortably within the remaining budget margin of 182,667 DKK.

The H200 NVL provides 141 GB of unified GPU memory on a single chip, making it the best option within budget for running very large language models (70B+ parameters in full precision) without the complexity and overhead of multi-GPU setups. With 1,536 GB of system RAM, the RAM:VRAM ratio reaches approximately 11:1 — well above NVIDIA's recommended 2:1 minimum — ensuring no memory pressure during parallel CPU-side processing while the GPU handles inference or fine-tuning tasks simultaneously.

---

## Contact

**Maurizio Sessa, Associate Professor**  
Drug Safety Group · Department of Drug Design and Pharmacology  
University of Copenhagen

📩 [maurizio.sessa@sund.ku.dk](mailto:maurizio.sessa@sund.ku.dk)

---

## License

This repository and all associated tools are released under the [MIT License](LICENSE).

---

*We are building this in the open, from day one.*

---

🔗 [github.com/mauriziosessaku/OpenSafety](https://github.com/mauriziosessaku/OpenSafety/blob/main/README.md)
