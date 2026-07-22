# Reference Corpus for CS Curriculum Design Agent

Annotated bibliography covering the theoretical and empirical foundations for competency-based, spiral, UDL-aligned CS curriculum design. Organized by facet, with cross-references noted where bodies of literature intersect (e.g., notional machines ↔ cognitive load theory; spiral design ↔ mastery learning).

---

## 1. Notional Machines & Program Execution Understanding

The core literature on how students build (or fail to build) mental models of program execution — directly relevant to CS-101's memory-visualization and concurrency work.

- **du Boulay, B. (1986).** *Some difficulties of learning to program.* Journal of Educational Computing Research, 2(1), 57–73. — The foundational paper that coined "notional machine"; identifies the general orientation, notional machine, notation, structures, and pragmatics as five distinct sources of novice difficulty.
- **Sorva, J. (2013).** *Notional machines and introductory programming education.* ACM Transactions on Computing Education, 13(2), Article 8. — The definitive synthesis: connects notional machines to misconception research, mental model theory, constructivism, phenomenography, and threshold concepts. Essential first read; argues the notional machine should be an explicit learning objective, not a byproduct of coding practice.
- **Fincher, S., Jeuring, J., Miller, C. S., Donaldson, P., du Boulay, B., Hauswirth, M., Hellas, A., Hermans, F., Lewis, C., Mühling, A., Pearce, J. L., & Petersen, A. (2020).** *Notional Machines in Computing Education: The Education of Attention.* ITiCSE-WGR '20, pp. 21–50. — ACM working-group report defining NMs with formal criteria, tracing their origin, and cataloging examples from practicing teachers. Companion site: notionalmachines.github.io (curated collection, useful as a design reference when building visualizations).
- **Guzdial, M. — various.** *Reframing "notional machine" as a target of instruction rather than a byproduct of coding practice* — relevant to your SIGCSE argument that generative AI inverts the traditional notional-machine-development model. Worth searching Guzdial's blog/ICER papers directly for the most current framing given the GenAI angle.
- **Xie, B., et al. — SIGCSE 2023.** *Notional Machine in Mathematics and Introductory Computer Science Courses.* — Empirically compares NM effectiveness across course levels; finds intro students prefer template-like NMs while upper-level students rely on more conceptual ones — a useful data point for how much abstraction to expose at each spiral turn.
- **Second-generation critique:** *Notional Machines: Retrieving Background Practices of Perception and Action*, ACM TOCE (2024) — challenges the "mental model in the head" framing using embodied/enactive cognitive science; useful as a counterpoint if you want the curriculum to also account for procedural/tacit skill development, not just declarative mental models.

**Cross-reference:** Pair this section with §6 (Cognitive Load Theory) below — worked examples and Parsons problems are the dominant instructional techniques used to scaffold notional-machine acquisition without overloading working memory.

---

## 2. Broadening Participation in Computing (BPC)

- **Sax, L. J., Nhien, C., & Stormes, K. N. (2024).** *A quantitative methodological review of research on broadening participation in computing, 2005–2022.* SIGCSE '24, 1182–1188. (Expanded version in ACM TOCE, 2026.) — Meta-review of the BPC empirical literature's methodological rigor; useful for calibrating what counts as strong vs. weak evidence when your agent evaluates intervention claims.
- **Cheryan, S., Master, A., & Meltzoff, A. N. (2015).** *Computing Whether She Belongs: Stereotypes Undermine Girls' Interest and Sense of Belonging in Computer Science.* Journal of Educational Psychology / related SIBL Lab papers. — Classic experimental work showing that classroom environment cues (stereotype-laden decor, framing) causally affect girls' interest and belonging, independent of instructor gender or actual content. Directly actionable for course branding, marketing materials, and example selection in CS-101.
- **Culturally sustaining computing education systematic review** (2026, journal article, tandfonline) — Six-theme synthesis of what "culturally sustaining" looks like in CS pedagogy; useful if the foundational core needs to accommodate varied student populations across your four tracks.
- **NSF BPC Alliances / Expanding Computing Education Pathways (ECEP).** *Determining metrics for broadening participation in computing.* — Practical framework for what to actually measure (access, participation, retention metrics) at the program level — relevant to your competency-intelligence-platform's reporting layer.
- **Duke CS Broadening Participation program page** — aggregates ongoing empirical work (CS1/CS2 pedagogy, help-seeking behavior via CS-Ed Podcast) worth periodic re-scanning for new results.

**Adjacent and worth folding in:**
- **Cheryan, S., Plaut, V. C., Davies, P. G., & Steele, C. M. (2009).** *Ambient belonging: How stereotypical cues impact gender participation in computer science.* Journal of Personality and Social Psychology. — The original ambient-belonging study.
- **Good, C., Aronson, J., & Inzlicht, M. (2003).** *Improving adolescents' standardized test performance: An intervention to reduce the effects of stereotype threat.* Journal of Applied Developmental Psychology, 24, 645–662. — Classic stereotype-threat mitigation intervention design, transferable to intro CS.
- **Freeman, S., Eddy, S. L., McDonough, M., Smith, M. K., Okoroafor, N., Jordt, H., & Wenderoth, M. P. (2014).** *Active learning increases student performance in science, engineering, and mathematics.* PNAS, 111(23), 8410–8415. — Landmark meta-analysis: active learning reduces STEM failure rates by roughly a third to half relative to lecture; frequently cited as the strongest single lever for both learning outcomes and equity gaps.

---

## 3. Universal Design for Learning (UDL) in CS

- **UDL4CS Research-Practice Partnership (University of Florida, CSTA, district partners), NSF-funded.** udl4cs.education.ufl.edu — The most CS-specific, actively maintained UDL body of work. Key artifacts:
  - *UDL Guidelines for Computer Science Education* — a table mapping UDL 3.0 guidelines (engagement, representation, action & expression) to concrete K-12 CS strategies. Directly portable to your foundational core even though it targets K-12.
  - *UDL4CS-2*: extends the work to systems-change and teacher professional development for inclusion of students with disabilities specifically.
  - *UDL4AI* (emerging): adapting the same framework to AI literacy — relevant given your AI specialization track.
- **CAST (Rose, D. H., & Meyer, A., originators of UDL, 1984, refined through UDL Guidelines 3.0).** — The general (non-CS-specific) UDL framework and its three core principles: multiple means of engagement, representation, and action/expression. Primary source to cite when justifying *why* the framework applies broadly.
- **CS4All (NYC DOE) UDL resource site.** — Practical lesson-plan-level examples and an "UDL in CS" table; useful as an implementation-pattern reference rather than a theoretical one.
- **Israel, M., Lash, T., & Ray, M. (2017).** *Universal Design for Learning within Computer Science Education.* Creative Technology Research Lab, University of Illinois. — Practitioner-facing guidance on starting small (one or two checkpoints per unit) rather than attempting the full UDL framework at once — a useful implementation heuristic for a phased curriculum rollout.

**Note:** Most UDL-in-CS literature is K-12 focused. If your agent is applying this to an undergraduate program, flag that as a translation gap explicitly — the accessibility principles generalize, but the specific classroom exemplars will need adaptation for adult learners and a competency-based structure.

---

## 4. Mastery Learning

- **Bloom, B. S. (1968).** *Learning for Mastery.* Evaluation Comment, 1(2). — The originating paper; introduces the "two-sigma" framing later elaborated in Bloom (1984).
- **Bloom, B. S. (1984).** *The 2 Sigma Problem: The Search for Methods of Group Instruction as Effective as One-to-One Tutoring.* Educational Researcher, 13(6), 4–16. — The famous finding that mastery-learning + formative feedback approached (but did not fully close) the achievement gap between group instruction and 1:1 tutoring; frequently over-cited without the caveats — worth reading in full rather than relying on secondary summaries.
- **Guskey, T. R. (2007).** *Closing Achievement Gaps: Revisiting Benjamin S. Bloom's "Learning for Mastery."* Journal of Advanced Academics, 19(1), 8–31. — Best modern synthesis and defense of mastery learning against later critiques; also documents affective benefits (confidence, attendance, attitude) beyond raw achievement.
- **Kulik, C.-L. C., Kulik, J. A., & Bangert-Drowns, R. L. (1990).** *Effectiveness of mastery learning programs: A meta-analysis.* Review of Educational Research, 60(2), 265–299. — The most-cited quantitative meta-analysis; treat as the empirical anchor when justifying mastery-based progression gates in your competency system.
- **Critical counterpoint — Arlin, M. (1984).** Work cited across the above (via Guskey/Motamedi syntheses) disputes Bloom's claim that achievement *and* time variability can be minimized simultaneously; useful for building an honest gap-flagging design note (consistent with your stated value of not glossing over tensions) — mastery learning reliably narrows achievement variance but tends to increase time-to-mastery variance, which has direct implications for how your program handles pacing across a two-year core.
- **Corbett, A. (2001).** *Cognitive computer tutors: Solving the two-sigma problem.* — Bridges Bloom's mastery-learning claims to intelligent tutoring systems; relevant if your competency platform incorporates adaptive practice/tutoring components.

---

## 5. Spiral Curriculum Design

- **Bruner, J. S. (1960).** *The Process of Education.* Harvard University Press. — Originating text; the core claim is that "any subject can be taught effectively in some intellectually honest form to any child at any stage of development," achieved by revisiting fundamental ideas with increasing formal rigor.
- **Harden, R. M., & Stamper, N. (1999).** *What is a spiral curriculum?* Medical Teacher, 21(2), 141–143. — The most widely used *design* elaboration of Bruner's concept (originally for medical education, now broadly applied): topics are revisited, difficulty increases, new learning explicitly links to prior learning, competence is made visible to learners over time, and the whole structure must remain coherent rather than merely repetitive. This is probably the single most directly applicable paper for your CS-101 "spiral with OS concepts woven throughout" design, since it gives concrete design criteria rather than just the metaphor.
- **Critical caveat (Cambridge Assessment, "Perspectives on curriculum design: comparing the spiral and the network models").** — Notes that Bruner's original 1960 book offered no empirical evidence for the spiral approach's efficacy, and that spiral curricula are difficult to evaluate because they're usually bundled with other constructivist/inquiry-based methods. Worth citing explicitly in any design-log entry where you're asked to defend the spiral choice — the honest answer is "strong theoretical and face-validity case, thin direct causal evidence," which is consistent with your stated preference for honest gap-flagging.
- **ERIC ED538282 (2012).** *The Spiral Curriculum.* Research into Practice, Education Partnerships, Inc. — Concise practitioner summary of the three defining features (revisiting, increasing complexity, connection to prior learning) and claimed benefits; good as a one-page justification document if you need something short for stakeholder communication (e.g., department curriculum committee).
- **Domain-specific precedent:** University of Detroit Mercy's spiral ECE curriculum (robotics-themed, hands-on Fund I/Fund II integration) is a useful existing structural analog for an engineering-adjacent spiral built around a recurring project theme — potentially informative for how CS-101's Go/CSP thread could anchor later-course callbacks.

---

## 6. Competency-Based Assessment

- **Shifting from traditional engineering education towards competency-based approach** (Education and Information Technologies, Springer, 2023) — Review paper giving the KA/KU/LO (knowledge area / knowledge unit / learning outcome) decomposition model for competency-based engineering programs; structurally close to what ABET-style CS programs need.
- **"Standardizing course assessment in competency-based higher education: an experience report"** (Frontiers in Education, 2025) — Describes the C-A&M model: Competencies → Learning Outcomes → Global Indicators → Specific Indicators → Assessment Tools. This decompositional chain maps directly onto a "preponderance of evidence across multiple assessments" design like yours — worth using as a structural template for the competency-intelligence-platform's Identity/assessment domains.
- **Competency-based assessment tools for engineering higher education: complex problem-solving case study** (2024, Taylor & Francis) — Empirically compares Bloom's taxonomy against Marzano & Kendall's revised (cognitive/psychomotor/affective) taxonomy for competency assessment; relevant if your rubric design needs a taxonomy that captures more than cognitive competencies alone (e.g., collaboration, professional practice competencies common in CS capstones).
- **Assessment in Undergraduate Competency-Based Medical Education: A Systematic Review** (2021) — Medical education is the most mature CBE-with-accreditation domain and has already solved many of the "how do you gate progression, and with what evidence" problems your curriculum faces; worth mining directly for assessment-instrument patterns (workplace-based assessment, milestone frameworks, entrustable professional activities) that translate surprisingly well to a CS competency ladder.
- **Northern Arizona University Personalized Learning program** — You've already identified this as the closest existing structural analog for a dual-record (transcript + competency report) ABET-accredited CS program; worth maintaining as a running case study rather than a one-time benchmark, since it's the nearest real-world precedent for the specific tension you're navigating.

---

## 7. Doll's Postmodern Curriculum Theory (the 4Rs)

A foundational influence on this project's overall design conception, distinct from — and arguably prior to — the other facets above: several of them (spiral curriculum, mastery learning's iterative feedback loops, competency-based "preponderance of evidence") can be read as more operational/empirical instantiations of moves Doll makes at a more general theoretical level.

- **Doll, W. E., Jr. (1993).** *A Post-Modern Perspective on Curriculum.* Teachers College Press. — The primary source. Argues for replacing the linear, closed, pre-determined ("modernist") curriculum matrix with an open one built on chaos theory, Piaget, Dewey, Prigogine, Bruner, and Whitehead, "without 'tops' or 'bottoms,' with no beginnings (in a foundational sense) and no endings (in a terminal sense)." Introduces the **4Rs**:
  - **Richness** — depth, layers of meaning, and multiple legitimate interpretations in curriculum content; deliberate openness/indeterminacy rather than a single settled reading, generative of dialogue and hypothesis-generation.
  - **Recursion** — reflective looping back on one's own prior work/understanding, where "every completion prompts a fresh start while each fresh start ascends from an earlier completion" — recursion in Doll's sense is not mere repetition (that's closer to Bruner's spiral) but the transformation of understanding through reflecting on it.
  - **Relation** — multi-dimensional connections both *within* the curriculum (pedagogical relations: how ideas connect to each other) and *beyond* it (cultural relations: how the curriculum connects to a wider social/ecological/cosmological frame) — narration and dialogue are the primary carriers of relation.
  - **Rigor** — not rigor-as-rigidity, but the deliberate, disciplined search for alternative framings and hidden assumptions, and the negotiation of passages between them, so dialogue stays "meaningful and transformative" rather than anything-goes relativism. This is the R that keeps richness/relation/recursion from collapsing into unstructured openness.
- **Doll, W. E., Jr. (2002).** *Ghosts and the Curriculum*, in *Chaos, Complexity, Curriculum, and Culture* (Doll, Fleener, Trueit, & St. Julien, Eds.). — Extends the 4Rs with the **5 Cs** (currere, complexity, cosmology, conversation, community), situating individual curriculum design within a broader ecological/cultural frame. Relevant if the program-wide "embedding-systems" scope of notional-machine thinking (organizational/social/infrastructural context) needs deeper theoretical grounding than the 4Rs alone provide.
- **Secondary synthesis (useful for quick orientation or for justifying the framework to stakeholders unfamiliar with curriculum theory):** *"The Four R's — An Alternative to the Tyler Rationale"* summaries and *"The Intersection of Post-Modernity and Classroom Practice"* (Teacher Education Quarterly, 2004) both give accessible restatements of the 4Rs and their relationship to the traditional linear/Tyler model this project is explicitly departing from.

**Direct connections to this project's design decisions, made explicit:**

- **Recursion (Doll) vs. spiral curriculum (Bruner, §5):** these are related but not identical. Bruner's spiral is fundamentally about *content* — the same topic revisited with increasing formal complexity. Doll's recursion is about the *learner's relationship to their own prior understanding* — reflection that transforms rather than just deepens. A spiral-threads design can satisfy Bruner's criteria (revisit, increase complexity, link to prior learning) while still being fairly linear in spirit if it never asks students to reflect on and revise their earlier mental model rather than just add to it. Worth treating Doll's recursion as a check on whether the spiral is doing transformative work, not just cumulative work — e.g., does revisiting mutability in the context of threads *change* how a student understands the variable-swap example from earlier, or does it just add a new fact alongside the old one unchanged?
- **Relation (Doll) and the three-scope notional machine (artifact-internal / human-interaction / embedding-systems):** this is close to a direct implementation of Doll's "relation" — pedagogical relation maps to artifact-internal (how concepts within the computational artifact connect to each other) and cultural/social relation maps to human-interaction and embedding-systems (how the artifact connects to the people and systems around it). Systems thinking as the program-wide through-line can be understood as this project's concrete answer to what Doll leaves more abstract.
- **Rigor (Doll) as the check against the whole design becoming too loose:** as more threads, pairings, and scopes accumulate, Doll's rigor is the explicit reminder to keep interrogating assumptions (e.g., "is concurrency-as-norm actually earning its place in this block, or are we forcing a pairing to appear thorough?") rather than letting richness/relation/recursion produce an open but incoherent curriculum. This is consistent with — and gives theoretical backing to — this project's existing norm of honest gap-flagging over glossing.
- **Richness and the deliberate non-closure of the design process itself:** the project's own iterative, still-evolving design log, the practice of proposing rather than finalizing competency/thread changes, and treating block-inventory.md as "living state" rather than a finished spec are all consistent with (and can be explicitly framed as) Richness in Doll's sense — multiple legitimate interpretations under active negotiation, rather than a single fixed answer decided once.

---

## 8. Additional Facets Worth Including

Beyond the six you named, the search surfaced two clusters that are directly load-bearing for the specific artifacts you're building (CS-101, memviz prototype, Sonic Pi DSL):

### 8a. Cognitive Load Theory & Worked-Example/Parsons-Problem Research
This is the mechanistic bridge between "notional machines" (§1) and concrete pedagogy — it explains *why* certain instructional formats help students build accurate mental models without overwhelming working memory.

- **Sweller, J., van Merriënboer, J. J. G., & Paas, F. G. W. C. (1998).** *Cognitive architecture and instructional design.* Educational Psychology Review, 10(3), 251–296. — Canonical statement of intrinsic/extraneous/germane load and design implications.
- **Morrison, B. B., Margulieux, L. E., & Guzdial, M. (2015).** *Subgoals, context, and worked examples in learning computing problem solving.* ICER 2015. — Subgoal-labeled worked examples measurably improve learning transfer in programming; directly applicable to how you structure worked examples in the memory-visualization tool.
- **Nelson, G. L., & Ko, A. J. — Cognitive Load Theory in Computing Education Research: A Review**, ACM TOCE (2022) — Systematic mapping of how CLT has actually been used (and misused) across computing-ed research venues since 2010; a good check against over-applying CLT uncritically.
- **Parsons, D., & Haden, P. (2006).** *Parson's Programming Puzzles: A Fun and Effective Learning Tool for First Programming Courses.* — Originating Parsons-problems paper; subsequent work (Ericson, Hou, et al.) on faded/adaptive/distractor variants is directly relevant to interactive exercise design in a spiral CS-101.

### 8b. Threshold Concepts
Sorva (2013, §1) explicitly ties notional machines to threshold-concept theory (Meyer & Land). Given that your spiral design is explicitly trying to introduce concurrency and OS concepts *early* rather than deferring them to upper-division courses, threshold-concept theory (concepts that are transformative, irreversible, and often initially "troublesome") is worth adding as its own strand:

- **Meyer, J. H. F., & Land, R. (2003).** *Threshold concepts and troublesome knowledge: Linkages to ways of thinking and practising.* — Original framework; useful for identifying *which* CS-101 concepts (pointers/references, recursion, concurrency, state) are likely to be threshold concepts requiring dedicated "liminal space" pedagogy rather than standard scaffolding.

### 8c. Motivation / Self-Determination Theory
Not explicitly requested, but adjacent to both broadening-participation and mastery-learning literatures — Deci & Ryan's Self-Determination Theory (autonomy, competence, relatedness) is frequently used in CS-ed papers to explain *why* mastery-based progression and belonging interventions work when they do, and would give your agent a unifying motivational lens across §2 and §4.

---

## Suggested Use Notes for the Agent

1. **Weight by evidence strength, not just relevance.** Several facets here (spiral curriculum, UDL) have strong face validity and design guidance but comparatively thin causal evidence; mastery learning and active learning (Freeman et al.) have the strongest quantitative backing. Doll's 4Rs (§7) sit in a different category entirely — a theoretical/philosophical frame for curriculum design, not an empirically-tested intervention — and should be cited as such (grounding for *why* the design is shaped this way) rather than as evidence that it *works* in the causal-claim sense. Flag this distinction explicitly when the agent cites a rationale in design-log entries, consistent with the project's existing norm of honest gap-flagging.
2. **Doll's 4Rs (§7) function as the overarching theoretical frame; the other facets are more operational instantiations of it.** When justifying a specific design choice, prefer grounding it in the more concrete, checkable facet (e.g., Harden & Stamper's spiral criteria, or the C-A&M competency decomposition) and use Doll's Rs to explain *why that facet matters here* rather than citing Doll alone as the justification for a concrete decision — Doll's framework is deliberately abstract and doesn't itself specify testable design criteria.
2. **Most UDL-in-CS literature targets K-12.** When applying UDL guidance to the undergraduate foundational core, treat it as a translation, not a direct lift.
3. **CLT and notional-machine literatures should be read together** when designing any new visualization or interactive tool (like memviz) — CLT explains the *mechanism*, notional-machine theory explains the *target*.
4. **NAU's Personalized Learning program and medical-education CBE literature** are your two best "existing implementation" analogs and worth returning to whenever a design decision needs a real-world precedent rather than pure theory.