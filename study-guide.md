# DoD AI & RMF Study Guide

A companion to the [106-question study quiz](index.html). Built entirely from publicly available policy and guidance. Unofficial, contains no CUI, and is not an official product of the U.S. Government, the Department of War/Defense, or the Army. Always verify against the cited primary source before relying on anything here for real work.

**How to use this guide:** read one section, then run the quiz filtered to that topic. The quiz's per-topic score bars tell you where to reread. Current as of July 2026.

---

## Part 1: The AI Policy Landscape

### 1. NIST AI Risk Management Framework (AI RMF 1.0, NIST AI 100-1)

Released January 2023 under the National AI Initiative Act of 2020. It is a **voluntary** framework for managing risks of AI systems and building trustworthiness into design, development, use, and evaluation. It is not a certification or compliance regime.

**The four core functions:**

| Function | What it does | Memory hook |
|---|---|---|
| **Govern** | Cross-cutting. Culture, policies, accountability, roles, risk tolerance. Infused through the other three. | The soil everything grows in |
| **Map** | Establish context: purpose, users, deployment setting, data, impacts. Identify risks in that context. | Know the terrain first |
| **Measure** | Analyze, assess, benchmark, and track risks using quantitative and qualitative methods, including TEVV. | Put numbers and evidence on it |
| **Manage** | Prioritize risks and act: mitigate, transfer, avoid, accept. Response and recovery plans. | Do something about it |

**Seven characteristics of trustworthy AI:** valid and reliable (the necessary baseline condition), safe, secure and resilient, accountable and transparent, explainable and interpretable, privacy-enhanced, fair with harmful bias managed.

**Three harm categories:** harm to people, harm to organizations, harm to ecosystems.

**Key concepts:**

- **TEVV**: test, evaluation, verification, and validation, performed continuously across the AI lifecycle, not as a one-time gate.
- **AI actors**: everyone with an active role in the lifecycle, including deployers and operators, not just developers.
- **Profiles**: implementations of the framework for a specific use case or technology (the Generative AI Profile is the flagship example).
- **Playbook**: voluntary suggested actions per subcategory, hosted at the [NIST AI Resource Center](https://airc.nist.gov/). Explicitly not a checklist.
- Why AI risk differs from traditional software risk: data dependency, post-deployment drift, opacity, and emergent behavior at scale.

Primary source: [NIST AI 100-1 (PDF)](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf)

### 2. Generative AI Profile (NIST AI 600-1)

Released July 2024 as a cross-sectoral AI RMF profile. Identifies **12 risk categories** unique to or exacerbated by generative AI and maps roughly 200 suggested actions to Govern, Map, Measure, and Manage.

**The 12 GenAI risk categories:**

| # | Risk | One-line meaning |
|---|---|---|
| 1 | CBRN Information or Capabilities | Lowering barriers to weapons-relevant knowledge |
| 2 | Confabulation | Confidently stated false content (hallucination) |
| 3 | Dangerous, Violent, or Hateful Content | Generation of harmful content at scale |
| 4 | Data Privacy | Leakage or reconstruction of personal or sensitive data |
| 5 | Environmental Impacts | Resource consumption of training and inference |
| 6 | Harmful Bias and Homogenization | Amplified bias, narrowing of outputs |
| 7 | Human-AI Configuration | Automation bias, over-reliance, misplaced trust |
| 8 | Information Integrity | Scaled generation of misleading content |
| 9 | Information Security | New attack surface: prompt injection, data poisoning, model exfiltration |
| 10 | Intellectual Property | Infringing or unlicensed content in and out of models |
| 11 | Obscene, Degrading, or Abusive Content | Non-consensual or abusive imagery and text |
| 12 | Value Chain and Component Integration | Opaque third-party models, datasets, and components |

**Why this matters for GRC work:** confabulation is the risk that AI-drafted compliance narratives contain plausible fiction, human-AI configuration is the risk that reviewers stop checking, and value chain is the risk hiding inside every vendor model. Those three deserve the most attention when AI enters the assessment workflow. Human verification of AI-drafted package content is the control that answers all three.

Primary source: [NIST AI 600-1 (PDF)](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf)

### 3. Federal Direction, 2025 to 2026

- **EO 14179** (January 2025), Removing Barriers to American Leadership in Artificial Intelligence: revoked the October 2023 AI executive order (EO 14110) and set a deregulatory, dominance-focused AI policy. [Federal Register](https://www.federalregister.gov/executive-order/14179)
- **America's AI Action Plan** (July 2025): three pillars. Accelerate AI Innovation, Build American AI Infrastructure, Lead in International AI Diplomacy and Security. Among its directives, it tasked NIST with revising the AI RMF. [White House PDF](https://www.whitehouse.gov/wp-content/uploads/2025/07/Americas-AI-Action-Plan.pdf)
- **NIST SP 800-53 Release 5.2.0** (August 2025): first big patch-style release. Added SA-24 (Design for Cyber Resiliency), SA-15(13) (logging syntax), SI-2(7) (root cause analysis), revised SI-7(12), driven by EO 14306 on software update security. [Change summary (PDF)](https://csrc.nist.gov/csrc/media/Projects/risk-management/800-53%20Comment%20Site/SP800-53-r5.2.0-changes.pdf)
- **NIST COSAiS** (concept paper August 2025): Control Overlays for Securing AI Systems. SP 800-53 overlays tailored to AI use cases such as generative and predictive AI. This is the emerging bridge between the 800-53 catalog and AI systems, worth watching closely if you write packages. [Project page](https://csrc.nist.gov/projects/cosais)

### 4. DoD AI Policy Timeline

| Year | Milestone | Know this |
|---|---|---|
| Feb 2020 | **DoD AI Ethical Principles** | Responsible, Equitable, Traceable, Reliable, Governable. Apply to combat and non-combat AI. |
| Jun 2022 | **CDAO stands up** | Consolidated JAIC, Defense Digital Service, Chief Data Officer, and Advana. |
| Jun 2022 | **Responsible AI Strategy & Implementation Pathway** | Operationalizes the principles via six tenets: RAI governance, warfighter trust, AI product and acquisition lifecycle, requirements validation, responsible AI ecosystem, AI workforce. |
| Jan 2023 | **DoDD 3000.09 update** (Autonomy in Weapon Systems) | Core standard: "appropriate levels of human judgment over the use of force." Senior review before formal development and again before fielding for covered systems. It governs weapon systems, not all AI. |
| Nov 2023 | **Data, Analytics, and AI Adoption Strategy** | AI hierarchy of needs with quality data at the base. |
| Aug 2023 to Dec 2024 | **Task Force Lima**, then **AI Rapid Capabilities Cell** | Lima assessed and synchronized GenAI; the AI RCC succeeded it to accelerate fielding. |
| Aug 2025 | **CDAO realigned** | Now sits under USD(R&E). |
| Jan 2026 | **AI Strategy for the Department of War** | "Accelerating America's Military AI Dominance." See below. |

**The January 2026 DoW AI Strategy** is the current north star. Key content:

- Seven pace-setting projects. Warfighting: Swarm Forge, Agent Network, Ender's Foundry. Intelligence: Open Arsenal, Project Grant. Enterprise: **GenAI.mil** and **Enterprise Agents**.
- Speed-first posture: "risks of not moving fast enough outweigh the risks of imperfect alignment," a 30-day cadence goal for deploying the latest AI models, modular architectures, and enforcement of data-access decrees.
- Contract direction: "any lawful use" language and model objectivity benchmarks.
- Practical read for compliance professionals: the department is optimizing for velocity, so risk management has to live inside the pipeline (continuous monitoring, automated evidence, cATO-style thinking) rather than as a gate at the end.

Primary source: [AI Strategy for the Department of War (PDF)](https://media.defense.gov/2026/Jan/12/2003855671/-1/-1/0/artificial-intelligence-strategy-for-the-department-of-war.pdf)

### 5. Army AI Policy

**Army CIO guidance on generative AI and LLMs.** The rules that matter:

- GenAI applications require **authorization to operate on the DODIN**; GenAI does not bypass the standard authorization path.
- Obtain required **approvals before processing sensitive or classified information**.
- **Transparency**: users should be able to identify which systems use GenAI; developers document training data sources and test in controlled environments.
- **Risk assessment**: command developers, system owners, and users apply appropriate risk assessment frameworks (the NIST AI RMF is the leading reference) and weigh risk against benefit. The posture is "govern it," not "ban it."

**Other Army AI landmarks:**

- **AI Layered Defense Framework**: the Army's defense-in-depth approach to protecting AI capabilities; industry input was gathered via RFI. [RFI materials (PDF)](https://api.army.mil/e2/c/downloads/2024/08/14/2b0c5337/ai-ldf-rfi-instructions.pdf)
- **Project Linchpin**: the Army's trusted AI/ML operations pipeline for delivering AI to programs at scale.
- **AI2C**: the Army Artificial Intelligence Integration Center, under Army Futures Command.
- **AR 25-2, Army Cybersecurity**: AI on Army networks still lives inside the Army cybersecurity program and RMF. No exemptions.

**The practical chain to remember:** NIST AI RMF (how to think about AI risk) feeds DoD principles and strategy (what the department values) which feed Army guidance (what you must do on Army networks) which lands in your RMF package (how it gets authorized).

---
## Part 2: Core RMF and ISSO Practice

### 6. The RMF Seven Steps (NIST SP 800-37 Rev 2)

Mnemonic: **P-C-S-I-A-A-M** (Prepare, Categorize, Select, Implement, Assess, Authorize, Monitor).

| Step | Purpose | Key outputs |
|---|---|---|
| **Prepare** | Organization and system readiness. Added in Rev 2 to cut rework. | Roles assigned, risk strategy, common control identification, boundary |
| **Categorize** | Determine impact of loss of C, I, A | Security categorization (DoD: per CNSSI 1253) |
| **Select** | Pick and tailor the control set | Initial baseline, tailoring decisions, overlays, ODP values |
| **Implement** | Put controls in place and describe them | Implemented controls, SSP implementation statements |
| **Assess** | Independent determination of control effectiveness | SAR |
| **Authorize** | Risk-based decision by the AO | ATO, ATO with conditions, IATT, or DATO |
| **Monitor** | Keep the picture current | ConMon results, updated SSP/SAR/POA&M, posture reporting |

**Three-tier risk model:** Tier 1 organization, Tier 2 mission and business processes, Tier 3 information systems. The AO is the bridge between system-level facts and organizational risk tolerance.

Primary source: [NIST SP 800-37 Rev 2 (PDF)](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-37r2.pdf)

### 7. Roles You Must Keep Straight

| Role | One-line job description |
|---|---|
| **AO** (Authorizing Official) | The only official who can accept risk and grant, deny, or revoke authorization. Cannot delegate the decision. |
| **ISO** (Information System Owner) | Owns the system: procurement, operation, mission, resources. |
| **ISSM** | Manages the security program across systems; program-level oversight. |
| **ISSO** | Hands-on security for a system day to day: controls, evidence, POA&M hygiene, ConMon. |
| **SCA** (Security Control Assessor) | Independent assessor; produces the SAR. |
| **Common Control Provider** | Implements controls that other systems inherit, and owns the evidence for them. |

### 8. DoD-Specific RMF Rules

- **DoDI 8500.01, Cybersecurity**: the umbrella instruction establishing the DoD cybersecurity program on the NIST framework family. [PDF](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/850001p.pdf)
- **DoDI 8510.01, Risk Management Framework for DoD Systems** (reissued July 2022): operationalizes RMF for DoD, defines authorization decisions, and mandates **reciprocity**. [PDF](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/851001p.pdf)
- **Authorization decisions**: ATO; ATO with conditions; **IATT** (testing only, limited scope and period, never a shortcut to operations); **DATO** (denial). Traditional ATOs run up to 3 years; ongoing authorization replaces the fixed clock with continuous risk visibility.
- **Reciprocity**: reuse another component's authorization package and body of evidence to the maximum extent practical, then assess only the delta for your environment. Neither "start over" nor "blind trust."
- **Assess Only**: for IT below the system level (applications, components) incorporated into an environment that already holds an ATO. Assessed and approved for use, inherits the host's controls, no separate authorization boundary.
- **Categorization**: DoD uses **CNSSI 1253**, which keeps separate impact values for confidentiality, integrity, and availability (for example M-M-L) instead of the FIPS 200 high-water mark.
- **cATO** (February 2022 memo): continuous authorization requires three demonstrated competencies: continuous monitoring of controls, active cyber defense, and DevSecOps adoption. [DoD CIO library](https://dodcio.defense.gov/library/)

### 9. Security Controls (NIST SP 800-53 Rev 5 Family)

- **20 control families** in Rev 5. New in Rev 5: **PT** (PII Processing and Transparency) and **SR** (Supply Chain Risk Management).
- Family codes worth cold recall: AC access control, AT awareness and training, AU audit and accountability, **CA assessment, authorization, and monitoring** (renamed in Rev 5), CM configuration management, CP contingency planning, IA identification and authentication, IR incident response, MA maintenance, MP media protection, PE physical and environmental, PL planning, PM program management, PS personnel security, PT PII processing, RA risk assessment, SA system and services acquisition, SC system and communications protection, SI system and information integrity, SR supply chain.
- **SP 800-53B**: the baselines (Low, Moderate, High, plus a privacy baseline) and tailoring guidance.
- **Tailoring** is expected, but every decision (scoping, compensating controls, parameters) needs documented rationale the AO can defend.
- **ODPs**: organization-defined parameters, the fill-in-the-blank parts of control text. DoD and component overlays often pre-set them, so the baseline text alone never tells the full story.
- **SP 800-53A**: assessment procedures. Three methods: **Examine, Interview, Test**, each with depth and coverage attributes.
- **AI connection**: model and dataset provenance questions map naturally to **SR** and **SA** controls today, and NIST's COSAiS overlays are formalizing that mapping.

Primary sources: [SP 800-53 Rev 5](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) · [SP 800-53B](https://csrc.nist.gov/pubs/sp/800/53/b/upd1/final) · [SP 800-53A Rev 5](https://csrc.nist.gov/pubs/sp/800/53/a/r5/final)

### 10. eMASS, POA&Ms, and the Authorization Package

- **eMASS** (Enterprise Mission Assurance Support Service): the DoD government off-the-shelf GRC application that automates RMF workflow: control status, artifacts, inheritance, POA&Ms, workflow approvals, and reporting. Components operate their own instances.
- **The core package**: SSP (what is implemented), SAR (what the independent assessment found), POA&M (what remains and the plan), supported by the risk assessment.
- **POA&M discipline**: every weakness gets corrective actions, required resources, milestones with dates, and honest status. Never mark a failing control compliant because a fix is planned; that is what the POA&M is for. The AO accepts residual risk based on it.
- **Risk vocabulary** (SP 800-30): risk is a function of **likelihood and impact**. Inherent or raw risk is before mitigations; **residual risk** is what remains after. Authorization is the formal acceptance of residual risk.
- **Writing strong test results**: tie specific evidence to the 800-53A determination statements. Name what you examined (artifact and date), who you interviewed, what you tested, and the conclusion. "Compliant, see documentation" is how packages die in review.
- **ConMon** (SP 800-137): defined metrics and frequencies, assessment of a control subset on a cadence, results feeding the POA&M and AO reporting. Deliberate sampling, not everything-always or nothing-until-reauthorization.

### 11. STIGs, SRGs, and Scanning

- **SRG**: requirements for a technology family, derived from 800-53 controls through **CCIs**.
- **STIG**: product-specific implementation of SRG requirements, published by DISA on a regular cycle at [public.cyber.mil/stigs](https://public.cyber.mil/stigs/).
- **No STIG for a commercial product?** Apply the most applicable SRG (or a general-purpose STIG like Application Security and Development), and document how each requirement is met or not applicable. The applicability mapping itself becomes package evidence. This situation is the norm, not the exception, in commercial-software-heavy environments.
- **Severity categories**: **CAT I** directly and immediately leads to loss of C, I, or A or unauthorized access (fix now or mitigate hard before authorization); **CAT II** can lead to compromise; **CAT III** degrades protections or detection.
- **CCI**: decomposes control language into discrete, measurable statements, giving traceability from a STIG check up to an 800-53 control.
- **SCAP**: automated scanning of benchmark-checkable requirements; the rest is manual review tracked in checklists (STIG Viewer). **ACAS** is the DoD enterprise vulnerability scanning solution; its results feed POA&Ms and ConMon.

### 12. CUI Essentials

- **Framework**: EO 13556 created the CUI program; **32 CFR Part 2002** implements it government-wide (NARA/ISOO as executive agent); **DoDI 5200.48** implements it for DoD. [DoDI 5200.48 (PDF)](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/520048p.pdf)
- **Marking**: new documents use CUI banner and category markings; FOUO is legacy. Dissemination follows **lawful government purpose** plus any limited dissemination controls. Clearances are not the gate; CUI is not classified information.
- **CUI Basic vs Specified**: Specified categories carry handling requirements mandated by their underlying law or regulation, which override the baseline.
- **Transmission**: encrypt CUI in transit (approved encrypted email or file transfer), mark it properly, and send only to people who need it for a lawful government purpose.
- **800-171** (Rev 3, May 2024): protection requirements for CUI in **nonfederal** systems (contractor environments). Federal and DoD systems use 800-53 through the RMF instead. [SP 800-171 Rev 3](https://csrc.nist.gov/pubs/sp/800/171/r3/final)

### 13. NAF IT (DoDI 1015.16)

Nonappropriated Fund Instrumentalities run the business side of the installation (recreation, lodging, resale, and similar operations funded by revenue rather than appropriations), and their IT has its own instruction: **DoDI 1015.16, Nonappropriated Fund Instrumentalities Information Technology Policies and Procedures** (March 18, 2022, Change 1 effective August 1, 2024, issued by USD(P&R)).

The points that matter:

- **NAF does not mean exempt.** NAF IT systems follow the **RMF** consistent with DoDI 8500.01 and 8510.01: formal authorization decisions by designated AOs, then continuous monitoring. The funding source changes the business model, not the security obligation.
- **Governance**: a **NAF IT Business Mission Area Owner (BMAO)** oversees the NAF IT portfolio and chairs the **NAF IT Working Group**; NAFI enterprise owners have designated Authorizing Officials.
- **Reciprocity**: the instruction provides for reciprocal acceptance of authorization decisions, so evidence and authorizations can be reused rather than rebuilt.
- **Business-world compliance stacks on top**: **PCI DSS** for systems handling payment card data (think point-of-sale), **Privacy Impact Assessments** for PII, **FISMA** reporting, and Section 508 accessibility.
- **Cloud**: NAFIs may use approved commercial cloud paths, including FedRAMP-compliant services and commercial cloud access points, with authorization still required.

Why this matters: NAF environments are heavy on commercial software, payment processing, and cloud services, so a NAF ISSO is constantly reconciling three rulebooks at once (RMF, PCI DSS, and privacy). DoDI 1015.16 is the document that says how they fit together.

Primary source: [DoDI 1015.16 (PDF)](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/101516p.PDF)

### 14. DoD Cloud Impact Levels (DISA Cloud Computing SRG)

| Level | Data |
|---|---|
| IL2 | Publicly releasable, non-CUI |
| IL4 | CUI |
| IL5 | Higher-sensitivity CUI and unclassified National Security System data |
| IL6 | Classified up to SECRET |

A GenAI platform intended to touch sensitive CUI needs IL5 authorization. This single table explains most "can we use this AI tool for that data" questions.

Source: [DoD Cloud Computing Security (DISA)](https://public.cyber.mil/dccs/)

---

## Cross-Walk: Where AI Policy Meets Your RMF Package

| AI concern | RMF home today |
|---|---|
| Model/dataset provenance | SR and SA controls; AI 600-1 value chain risk |
| AI drafting package content | Human review as the control; AI 600-1 confabulation and human-AI configuration |
| GenAI tool handling CUI | IL4/IL5 authorization, DoDI 5200.48, Army CIO GenAI guidance |
| New AI capability on the network | Standard authorization path (assess and authorize, or assess-only into a host) |
| AI behavior changing over time | ConMon strategy; AI RMF Measure with TEVV cadence |
| Who accepts AI risk | The AO, same as any risk. AI does not create a new risk-acceptance chain |

## Memory Hooks

- RMF steps: **P-C-S-I-A-A-M** ("Please Categorize Systems In A Astute Manner")
- AI RMF functions: **Go-M-M-M** (Govern, then Map, Measure, Manage)
- DoD AI principles: **R-E-T-R-G** (Responsible, Equitable, Traceable, Reliable, Governable)
- Trustworthy AI characteristics: Valid, Safe, Secure, Accountable, Explainable, Private, Fair
- Package trio: **SSP says, SAR checks, POA&M fixes**
- Impact levels: **2 public, 4 CUI, 5 sensitive CUI/NSS, 6 SECRET**

## Acronym Glossary

ACAS Assured Compliance Assessment Solution · AO Authorizing Official · ATO Authorization to Operate · BMAO Business Mission Area Owner · cATO Continuous ATO · CCI Control Correlation Identifier · CDAO Chief Digital and AI Office(r) · CNSSI Committee on National Security Systems Instruction · ConMon Continuous Monitoring · COSAiS Control Overlays for Securing AI Systems · CUI Controlled Unclassified Information · DATO Denial of ATO · DCWF DoD Cyber Workforce Framework · DODIN DoD Information Network · GOTS Government Off-The-Shelf · IATT Interim Authorization to Test · IL Impact Level · ISCM Information Security Continuous Monitoring · ISO Information System Owner · ISSM Information System Security Manager · ISSO Information System Security Officer · NAF Nonappropriated Fund · NAFI Nonappropriated Fund Instrumentality · ODP Organization-Defined Parameter · PCI DSS Payment Card Industry Data Security Standard · POA&M Plan of Action and Milestones · RMF Risk Management Framework · SAR Security Assessment Report · SCA Security Control Assessor · SCAP Security Content Automation Protocol · SRG Security Requirements Guide · SSP System Security Plan · STIG Security Technical Implementation Guide · TEVV Test, Evaluation, Verification, and Validation · USD(R&E) Under Secretary for Research and Engineering

## Master Source List

- [NIST AI 100-1, AI RMF 1.0](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf)
- [NIST AI 600-1, Generative AI Profile](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf)
- [NIST AI Resource Center (Playbook, roadmap, crosswalks)](https://airc.nist.gov/)
- [NIST SP 800-37 Rev 2](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-37r2.pdf)
- [NIST SP 800-53 Rev 5](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) · [Release 5.2.0 changes](https://csrc.nist.gov/csrc/media/Projects/risk-management/800-53%20Comment%20Site/SP800-53-r5.2.0-changes.pdf)
- [NIST COSAiS project](https://csrc.nist.gov/projects/cosais)
- [NIST SP 800-171 Rev 3](https://csrc.nist.gov/pubs/sp/800/171/r3/final)
- [DoDI 8510.01, RMF for DoD Systems](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/851001p.pdf)
- [DoDI 8500.01, Cybersecurity](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/850001p.pdf)
- [DoDD 3000.09, Autonomy in Weapon Systems](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodd/300009p.pdf)
- [DoDI 5200.48, CUI](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/520048p.pdf)
- [DoDI 1015.16, NAFI IT Policies and Procedures](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/101516p.PDF)
- [DoD AI Ethical Principles (2020)](https://www.defense.gov/News/Releases/Release/Article/2091996/dod-adopts-ethical-principles-for-artificial-intelligence/)
- [DoD RAI Strategy and Implementation Pathway (2022)](https://media.defense.gov/2022/Jun/22/2003022604/-1/-1/0/Department-of-Defense-Responsible-Artificial-Intelligence-Strategy-and-Implementation-Pathway.PDF)
- [AI Strategy for the Department of War (Jan 2026)](https://media.defense.gov/2026/Jan/12/2003855671/-1/-1/0/artificial-intelligence-strategy-for-the-department-of-war.pdf)
- [America's AI Action Plan (July 2025)](https://www.whitehouse.gov/wp-content/uploads/2025/07/Americas-AI-Action-Plan.pdf)
- [CDAO realignment announcement](https://www.ai.mil/Latest/News-Press/PR-View/Article/4281147/cdao-re-alignment-to-usdre-accelerates-ai-transformation-at-dod/)
- [Army AI Layered Defense Framework RFI](https://api.army.mil/e2/c/downloads/2024/08/14/2b0c5337/ai-ldf-rfi-instructions.pdf)
- [DoD Cyber Exchange: STIGs](https://public.cyber.mil/stigs/) · [DoD Cloud Computing Security](https://public.cyber.mil/dccs/)
- [32 CFR Part 2002 (CUI)](https://www.ecfr.gov/current/title-32/subtitle-B/chapter-XX/part-2002)
