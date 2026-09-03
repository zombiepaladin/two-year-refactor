+++
title = "AP Cybersecurity Alignment Analysis"
weight = 50
ordinal = "6.5"
+++

> *Working draft for faculty review. Maps the College Board AP Cybersecurity curriculum (Course and Exam Description, 2026–27) against the two-year core to answer two questions: (1) where does a student who earned AP Cybersecurity credit already have foundation, and (2) where does the core **not** deliver what the AP course develops? The binding use case is the Cybersecurity specialization: this analysis identifies the pre-college foundation the specialization can build on and the gaps it must address.*
>
> Checked against the real, drafted course-design pages — mainly CIS 251 (Foundations of Cybersecurity), CIS 225 (Foundations of Computer Networks), CIS 400, CIS 260, and CIS 120. **CIS 251's real content is uneven**: CIA triad, authentication/authorization, MFA, malware, and social-engineering content are all explicitly named — but least privilege, formal threat modeling, and applied cryptography tied to the core's modular-arithmetic content are *not* in the real course (the same finding made in `specializations/cybersecurity.md`'s 2026-08-04 revisit). Status ratings below reflect the real content directly.

## About the AP Cybersecurity course

AP Cybersecurity launched as a pilot in 2024–25, expanded in 2025–26, and goes nationwide in 2026–27 with the first official AP exam in May 2027. The course is a year-long, high-school-level introduction organized into **five units** (roughly 32 instructional weeks) and assessed against **three spiraling core skills** — *Analyze Risk*, *Mitigate Risk*, and *Detect Attacks* — each weighted at 25%–40% of the AP exam score.

The five units:

| Unit | Title | Approx. weeks |
|---|---|---|
| 1 | Introduction to Security | 1–4 |
| 2 | Securing Spaces | 5–10 |
| 3 | Securing Networks | 11–18 |
| 4 | Securing Devices | 19–26 |
| 5 | Securing Applications & Data | 27–32 |

---

## Unit-by-unit coverage mapping

### Unit 1 — Introduction to Security

| AP topic | AP content | Core coverage | Course | Status |
|---|---|---|---|---|
| 1.1 Social Engineering | Phishing, spear-phishing, whaling; vishing; smishing; pretexting; urgency and intimidation tactics | CIS 251's real Week 4 ("Threats and Attackers") explicitly names phishing, social engineering, and insider threats. Channel-specific variants (vishing, smishing, spear-phishing, whaling) and specific tactics are not named. | CIS 251 | **Partial** |
| 1.2 Authentication | Password attacks (brute force, credential stuffing, password spraying); strengthening with length and uniqueness; MFA (know/have/are factors) | CIS 251's Week 2 covers authentication explicitly; Week 5 ("Protecting Systems and Data") explicitly names MFA. Attack specifics (brute force, credential stuffing, spraying) and the formal know/have/are factor model are not named. | CIS 251 | **Partial** |
| 1.3 Public Networks | Public Wi-Fi interception risks; evil twin and rogue access points; VPNs as encrypted tunnels on untrusted networks | CIS 225's real content (socket-based network programming; security and encryption of network communications) and CIS 251's Week 5 (encryption) together give a general foundation, but neither names VPNs, TLS specifically, or wireless-attack specifics (evil twin, rogue access points). | CIS 225; CIS 251 | **Partial** |
| 1.4 AI-Powered Threats | AI-generated phishing (scaled, multilingual); deepfakes and voice cloning for impersonation; LLM prompt injection; training-data poisoning; AI-assisted malware and reconnaissance | Not covered. The bounded AI-Assisted Development practice addresses AI as a code-writing collaborator, not as an attack vector. | — | **Gap** |
| 1.5 AI in Defense | AI-powered threat detection and automated incident response | CIS 141 (the confirmed terminal pass for the AI-Assisted Development practice) covers high-stakes verification of AI-generated code for security, but AI as a defensive/detection tool in cyber operations generally is not covered. | CIS 141 (adjacent) | **Gap** |

---

### Unit 2 — Securing Spaces

| AP topic | AP content | Core coverage | Course | Status |
|---|---|---|---|---|
| 2.1 Security Foundations | CIA triad (confidentiality, integrity, availability); risk assessment (likelihood × severity matrix); risk response strategies (accept, transfer, mitigate, avoid); threat actor taxonomy (script kiddies to nation-states); six-phase cyberattack lifecycle (recon → weaponize → deliver → exploit → maintain → exfil); defense-in-depth | CIS 251's SLO 2 explicitly names the **CIA triad**, and Week 6 ("Risk Management and Incident Response") covers risk assessment directly. The formal risk matrix, response-strategy taxonomy, threat-actor taxonomy, attack lifecycle, and defense-in-depth as a named pattern are not in the real content. | CIS 251 | **Partial** |
| 2.2 Physical Attacks | Tailgating; shoulder surfing; dumpster diving; card cloning and RFID skimming | Not covered anywhere in the core. | — | **Gap** |
| 2.3 Physical Protection | Physical access controls (locks, card readers, mantraps/vestibules, bollards); clean-desk policy; insider threat program | Not covered anywhere in the core. | — | **Gap** |
| 2.4 Detecting Physical Attacks | Security cameras; guards; motion sensors; placement and coverage strategy | Not covered anywhere in the core. | — | **Gap** |

Unit 2 is the largest single gap between the two curricula. The K-State core has a strong *software* security posture but no physical security content at all — by design, since the core is a programming and systems foundation rather than a security-operations curriculum.

---

### Unit 3 — Securing Networks

| AP topic | AP content | Core coverage | Course | Status |
|---|---|---|---|---|
| 3.1 Network Attacks | ARP spoofing and ARP poisoning; MAC flooding; DNS poisoning; DoS and DDoS; on-path (man-in-the-middle) attacks; packet sniffing | CIS 225's real, confirmed content (OSI 7-layer model, packet encapsulation, common protocols, security assessment) gives the protocol-layer foundation that makes these attacks comprehensible, but the specific attack procedures, tools, and defenses are not named in its drafted SLOs. | CIS 225 | **Partial** |
| 3.2 Wireless Controls | Managerial and administrative controls; WPA2/3 and wireless authentication; SSID management; war driving awareness | CIS 225 introduces the network stack conceptually; CIS 251's Week 5 (encryption) is a light foundation for the WPA2/3 encryption model. Operational wireless security — SSID management, war driving, wireless access control policies — is not covered. | CIS 225; CIS 251 (foundation) | **Partial** |
| 3.3 Network Segmentation | Network segmentation strategy; VLANs and VLAN tagging; DMZ architecture for public-facing services | CIS 225 covers IP addressing and protocol structure generally — the foundation for understanding why segmentation works — but VLANs and DMZ as named architectural patterns aren't in its drafted content. | CIS 225 | **Partial** |
| 3.4 Firewalls | Stateless packet filtering; stateful inspection; next-generation firewalls (NGFW, deep packet inspection, application-layer filtering); writing and reading firewall rules | CIS 225 covers the protocol layer packet filtering operates on; CIS 400's confirmed "harden the system before it goes live" content (Confirmed Design Intent) is a real, applied deployment-security pass. Firewall architecture and rule syntax specifically are not named anywhere. | CIS 225; CIS 400 | **Partial** |
| 3.5 Monitoring | IDS vs. IPS (detect-and-alert vs. detect-and-block); SIEM (centralized log aggregation and correlation); network traffic analysis | CIS 400's confirmed deployment/monitoring content (containers, monitoring and logging tooling) covers operational monitoring of a live system generally. IDS/IPS and SIEM as specific security-monitoring architectures are not named. | CIS 400 (partial) | **Partial** |

Students arrive at the Cybersecurity specialization with real protocol-layer theory from CIS 225 (OSI model, encapsulation, protocols) that makes Unit 3 concepts comprehensible, even though the specific attack procedures and tooling this unit covers aren't in the core. That residual gap — security-operations specifics: attack procedures, wireless access management, VLAN administration, and firewall rule authoring — belongs naturally in the first Cybersecurity specialization course, which can teach it against a real theoretical foundation students already have.

---

### Unit 4 — Securing Devices

| AP topic | AP content | Core coverage | Course | Status |
|---|---|---|---|---|
| 4.1 Malware | Nine malware types: virus, worm, trojan horse, ransomware, spyware, keylogger, logic bomb, rootkit, fileless malware; infection vectors | CIS 251's Week 4 explicitly names malware as a topic. The nine-type taxonomy and specific propagation mechanisms are not covered. | CIS 251 | **Partial** |
| 4.2 Authentication & Hashing | Four authentication factors (something you know/have/are/somewhere you are); password storage via cryptographic hashing; collision resistance and pre-image resistance; MD5, SHA-1 (deprecated), SHA-256, SHA-512 | CIS 251 covers authentication (Week 2) and encryption generally (Week 5). Grounding this in the core's discrete-math modular-arithmetic content is proposed design intent, not yet drafted into the course (per `specializations/cybersecurity.md`'s 2026-08-04 revisit). Specific algorithm names and hash properties (collision/pre-image resistance) are not covered. | CIS 251 | **Partial** |
| 4.3 Device Hardening | Anti-malware and endpoint detection; patch management; host-based firewall; configuration hardening; least privilege; IoT security considerations; mobile device management (MDM) | CIS 400's confirmed hardening content applies here directly. CIS 251's real SLOs have no explicit least-privilege framing (see the same 2026-08-04 revisit). Patch management, MDM, and IoT-specific controls are not covered. | CIS 400 | **Partial** |
| 4.4 Detecting Device Attacks | Indicators of compromise (IoC); log analysis for device-level anomalies; detection controls and alerting | CIS 400 covers operational monitoring. A "blameless postmortem" pass that instills incident-response culture lives at the Year 3–4 program capstone, outside the two-year core (see `signature-assessments.md`'s 2026-08-04 finding). IoC as a named concept and device-level detection specifics are not covered. | CIS 400 (partial) | **Partial** |

---

### Unit 5 — Securing Applications & Data

| AP topic | AP content | Core coverage | Course | Status |
|---|---|---|---|---|
| 5.1 Application Attacks | SQL injection (untrusted input into database queries); XSS — reflected (Type I) and stored (Type II) cross-site scripting | CIS 260 provides the SQL foundation needed to understand injection; CIS 120 (Web Foundations) provides the DOM/web context for XSS. Neither course nor CIS 251 names these attack patterns explicitly. | CIS 260; CIS 120 | **Partial** |
| 5.2 Access Controls | Role-based access control; authorization vs. authentication; principle of least privilege | CIS 251 covers authentication and authorization (Week 2). CIS 260's access-control-as-schema-dimension content is confirmed design intent that hasn't actually been drafted into the course (see `cis-260.md`'s "Proposed Changes," logged during the 2026-08-04 lens-pass review) — not yet real content. Least privilege isn't explicitly named in either course. | CIS 251; CIS 260 (proposed) | **Partial** |
| 5.3–5.4 Cryptography | Symmetric encryption (AES — shared secret); asymmetric encryption (RSA — public/private pair); key exchange; digital signatures and non-repudiation; PKI and certificate authority trust chains; HTTPS and TLS handshake | CIS 251's Week 5 covers encryption generically ("passwords, MFA, encryption, backups, updates"). Symmetric/asymmetric distinction, key exchange, digital signatures, PKI, and HTTPS/TLS are not named anywhere in its real content. | CIS 251 (light) | **Partial** |
| 5.5 Input Sanitization | Input validation and sanitization as a secure-by-design coding practice; parameterized queries as SQL-injection defense; output encoding as XSS defense | Not covered. Secure coding practices as a named category are absent from the core's drafted content. | — | **Gap** |
| 5.6 Data Integrity | Hash-based integrity verification (file and message integrity); detecting data tampering through hash comparison; monitoring for data-integrity violations | CIS 251's Week 5 encryption content is a light, generic foundation; hash-based integrity verification as a specific use case is not named. | CIS 251 (light) | **Partial** |

---

## The AP core skills and where the core develops them

| AP skill | Description (from CED) | Core development |
|---|---|---|
| **Analyze Risk** (25–40%) | Evaluate risk to organizational assets by identifying threats, vulnerabilities, and likelihood × impact | CIS 251's Week 6 (risk assessment) and Week 4 (threats/attackers) are the primary home. The Trustworthy Computing lens applies risk thinking wherever security is relevant throughout the core. The formal risk-assessment frameworks (likelihood/severity matrix, risk response strategies) the AP course uses are not in the real content. |
| **Mitigate Risk** (25–40%) | Implement protective and deterrent controls across people, networks, devices, and applications | Covered at the *principle* level (data minimization, hardening, trust boundaries as contracts, defensive best practices per CIS 251's Week 5). Physical, network, and many device controls are outside the core's scope. |
| **Detect Attacks** (25–40%) | Implement detection methods, monitor systems, analyze logs and network data as evidence | CIS 400's confirmed operational-monitoring content covers the software-operations side. IDS/IPS, SIEM, IoC detection, and network traffic analysis are outside the core. |
| **Collaborate** | Work with others and with AI tools to accomplish tasks | Covered strongly — CIS 400's confirmed team-project content (Sociotechnical Structure) and the AI-Assisted Development bounded practice. |
| **Communicate Concepts** | Explain key cybersecurity concepts to technical and non-technical audiences | The Professional Practices lens (documentation) and CIS 320's bounded Human-Centered Computing content develop technical communication broadly; security-concept explanation specifically is not practiced. |

---

## Coverage summary

### Covered by the core (AP student arrives with this foundation)

| Topic | Core home |
|---|---|
| Authentication and authorization concepts | CIS 251 |
| CIA triad | CIS 251 |
| Malware and social-engineering awareness | CIS 251 |
| Errors as attack surface (verbose stack traces, information leakage) | Computational Models thread + Trustworthy Computing lens |
| Trust boundaries as explicit contracts | Boundaries & Contracts thread |
| Security hardening before deployment | CIS 400 |
| Operational monitoring of live systems | CIS 400 |
| OSI protocol stack theory (7-layer model, packet encapsulation, common protocols) | CIS 225 |

### Partially covered (concept is in the core, AP depth not fully matched)

| Topic | What the core has | What's missing |
|---|---|---|
| Threat identification | CIS 251 names threats/attackers, risk | CIA-triad-adjacent frameworks (attack lifecycle, threat actor taxonomy) not named |
| Social engineering | CIS 251 Week 4 names phishing, social engineering, insider threats | Channel-specific variants (vishing/smishing/spear-phishing) not required |
| Malware | CIS 251 Week 4 names malware | Nine-type taxonomy and propagation mechanics not required |
| MFA | CIS 251 Week 5 names MFA explicitly | Know/have/are factor model not formalized |
| Cryptographic hashing / encryption | CIS 251 Week 5 names encryption generically | Algorithm names, symmetric/asymmetric distinction, hash properties not required |
| SQL injection / XSS | CIS 260 + CIS 120 prerequisite foundations | Named attack patterns not required |
| Access controls | CIS 251 authn/authz | Least privilege not named; CIS 260's schema-level access control is proposed, not built |
| Device hardening | CIS 400 hardening content | Patching, anti-malware, MDM, IoT not required |
| Security monitoring | CIS 400 operational monitoring | IDS/IPS, SIEM not named |
| Network-layer attacks (ARP, MAC, DNS, DoS, MitM, packet sniffing) | CIS 225 covers the protocols under each attack | Attack procedures, tools, and defenses not required |
| VPN as encrypted tunnel; public Wi-Fi risk | CIS 225 protocol foundation + CIS 251 encryption | Wireless-attack specifics (evil twin, rogue AP) not required |
| Network segmentation | CIS 225 IP/protocol foundation | VLANs and DMZ as named architecture not required |
| Firewalls | CIS 225 protocol layer + CIS 400 hardening | Stateless/stateful/NGFW architecture and rule writing not required |

### Gaps — not in the core

| Topic | AP unit | Why it is absent from the core |
|---|---|---|
| Formal risk-assessment methodology (matrix, response strategies) | 2.1 | Core addresses risk implicitly in design decisions and CIS 251's general framing, not as a formal operational methodology |
| Defense-in-depth as an explicit strategy | 2.1 | The Trustworthy Computing lens *is* defense-in-depth in practice but never names it as a pattern |
| Threat actor taxonomy | 2.1 | Out of scope — the core is a programming and systems foundation, not a security-operations curriculum |
| Cyberattack lifecycle / kill chain | 2.1 | Same — security-operations framing not in the core's scope |
| Physical security (Units 2.2–2.4, ~10 weeks) | 2.2–2.4 | Entirely out of scope for a programming core |
| IDS/IPS and SIEM | 3.5 | Security-operations tooling, not covered in the core |
| Input sanitization / secure-by-design coding | 5.5 | Not required anywhere in the core's drafted content |
| PKI, digital signatures, HTTPS/TLS handshake | 5.3–5.4 | Not in CIS 251's real content |
| AI as an attack vector (deepfakes, voice cloning, LLM manipulation) | 1.4 | The AI-Assisted Development bounded practice covers AI as a collaborator, not as a threat |

---

## Implications for the Cybersecurity specialization

The AP Cybersecurity mapping reveals two distinct gaps that the specialization must address:

**1. Security-operations vocabulary and frameworks.** The core develops a *design* security posture (data minimization, defensive best practices, hardening, trust boundaries) but not the *operational* vocabulary the AP course teaches: formal risk matrices, attack lifecycle, threat actor taxonomy, IDS/IPS, SIEM, IoC. A first course in the Cybersecurity specialization should introduce these frameworks explicitly, positioning them as the professional language that organizes what the student already understands from the core.

**2. The CIS 225 networking foundation.** CIS 225 (Foundations of Computer Networks, Y2 Fall) resolves what used to be a major prerequisite gap: students now arrive at the Cybersecurity specialization with real protocol theory (the OSI 7-layer model, packet encapsulation, common protocols) that makes network attacks, segmentation, and firewalls comprehensible. The residual gap is security-operations specifics: attack procedures, wireless access management, VLAN administration, and firewall rule authoring. These belong naturally in the first Cybersecurity specialization course. All Cybersecurity specialization courses that require network-layer knowledge should list CIS 225 as a prerequisite.

**What the core does deliver.** A student completing the two-year core arrives at the Cybersecurity specialization with:

- Real, though genuinely thin in places, security foundations from CIS 251: CIA triad, authentication/authorization, malware and social-engineering awareness, risk assessment, defensive best practices
- Real protocol-layer networking theory from CIS 225
- Security hardening as a practiced deployment step (CIS 400)
- Trust-boundary thinking embedded across the entire Boundaries & Contracts thread
- Applied cryptography and least-privilege framing are **not yet real content** — both are confirmed design intent for CIS 251 that hasn't been drafted in, a genuine open item rather than settled foundation (see `specializations/cybersecurity.md`'s faculty concerns)

These are foundations for advanced cybersecurity coursework built through building and operating systems rather than through survey study — but genuinely thin in places (applied cryptography, formal risk frameworks, least privilege). The gap is both operational breadth (frameworks, physical security, network tooling) *and* some core content that was planned but never drafted.

---

## Open questions for faculty review

1. **CIS 251's undrafted content.** Applied cryptography (tied to the core's modular-arithmetic content) and least privilege are both confirmed design intent for CIS 251 that never made it into the course's real SLOs or schedule. Whether to draft them in, or accept the thinner real scope, is a live decision — see `specializations/cybersecurity.md`'s faculty concerns for the same finding from a different angle.
2. **Networking prerequisite sequencing.** CIS 225 (Y2 Fall) resolves the placement question. The remaining question for the Cybersecurity specialization is sequencing: specialization courses that build on network-layer theory should list CIS 225 as a prerequisite, which means they cannot be taken earlier than Y2 Fall. A student who enters the specialization immediately after completing the core is well positioned; a student seeking earlier entry would need a bridging arrangement.
3. **Placement credit.** Should AP Cybersecurity satisfy any core requirement or grant placement into the specialization? This mapping suggests it is *not* a core substitute (the AP course does not cover the programming, systems-thinking, and software-security-design content the core provides), but it may warrant placement into an accelerated track within the specialization.
4. **AP alignment for incoming students.** Students who took AP Cybersecurity will have strong operational vocabulary (CIA triad, attack lifecycle, threat actor taxonomy, network attack names) that the core does not develop. Acknowledging this in specialization advising — treating AP Cybersecurity as complementary rather than overlapping — would help those students understand the value of the core rather than feeling they've already "done security."
