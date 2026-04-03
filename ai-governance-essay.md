# Building Governance Infrastructure: Lessons from Federal Data Governance for AI Implementation

As artificial intelligence systems become embedded in critical
operations across government and industry, organizations face a
fundamental challenge: how do you govern technologies whose risks are
still being discovered? The National Institute of Standards and
Technology\'s AI Risk Management Framework identifies this tension at
the heart of AI governance. Establishing trustworthy systems requires
measuring and managing risks that are often opaque, context-dependent,
and evolving faster than traditional regulatory approaches can
accommodate (NIST, 2023). This challenge is not unique to AI. Over the
past year, I\'ve worked on developing NASA\'s enterprise Data Maturity
Assessment, a tool designed to benchmark and improve data governance
practices across the agency. The project required translating abstract
governance principles into an operational system that NASA centers would
actually use, complete with assessment questions, scoring mechanisms,
privacy controls, and stakeholder buy-in. While the technical domains
differ, the governance challenges proved strikingly similar: How do you
measure compliance when best practices are still emerging? How do you
balance transparency with privacy? How do you create standardized
metrics that remain meaningful across diverse contexts? How do you
ensure assessment validity when expertise levels vary widely? These are
not merely technical implementation details. They represent fundamental
tensions inherent to governance itself. Drawing from my experience
implementing data governance at a federal agency, I argue that four
critical challenges from data governance practice reveal unresolved
tensions in AI governance operationalization: the paradox of privacy
versus accountability, the tension between standardization and
contextualization, the gap between measurement and actionable insight,
and the challenge of balancing inclusive participation with expert
validity. Understanding these tensions matters because AI governance is
moving from abstract frameworks to operational reality, and
organizations need practical strategies that acknowledge, rather than
paper over, the inherent tradeoffs in governance design.

## The Privacy-Accountability Paradox

The NIST AI Risk Management Framework emphasizes that trustworthy AI
requires both transparency for accountability and privacy protection for
individual rights (NIST, 2023). The OECD guidelines similarly call for
data security safeguards while ensuring openness and individual rights
to access, erasure, and informed consent (OECD, 2024). Yet these
principles exist in fundamental tension. Governance mechanisms require
auditability and traceability to function effectively, but privacy
protections often demand opacity and anonymization.

I encountered this paradox directly while developing NASA\'s Data
Maturity Assessment. The system uses single sign-on authentication,
meaning it inherently knows each assessor\'s identity. When we attempted
to offer an anonymity option for sensitive responses, we faced a design
contradiction: how do you maintain data integrity and track
organizational accountability while masking user identity? Our solution
involved conditional data masking in the Dataverse architecture, but
this only highlighted the deeper issue. True anonymity undermines
governance oversight, yet mandatory identification can discourage honest
self-assessment, particularly when evaluating compliance failures.

For AI governance, this tension intensifies. AI systems require
extensive data logging for safety audits and bias detection, yet
individuals have legitimate privacy interests in how their data feeds
these systems. Unlike my NASA assessment where the tradeoff involved
internal stakeholders, AI governance must balance corporate
accountability with public privacy rights. There is no technical
solution that perfectly resolves this contradiction. Organizations must
make explicit choices about which value takes precedence in specific
contexts, rather than pretending both can be fully satisfied
simultaneously.

## Standardization vs. Contextualization

The NIST AI RMF is intentionally designed to be \"use-case agnostic\"
and \"non-sector specific,\" enabling broad applicability across
industries and applications (NIST, 2023). This approach allows
organizations to adopt common governance language and compare practices.
However, AI risks are inherently context-dependent. A facial recognition
system deployed in law enforcement carries fundamentally different risks
than the same technology used to unlock a smartphone. Generic risk
categories obscure these distinctions.

NASA\'s Data Maturity Assessment confronted this same tension. We
developed a standardized 0-6 scoring system applicable across all agency
centers to enable enterprise-wide benchmarking. Yet different centers
operate with vastly different missions, technical infrastructures, and
interpretations of what \"data maturity\" means. A score of 4 in data
governance at a research center focused on open science has different
implications than the same score at a center managing classified mission
data. Our generalized assessment questions risked either being too vague
to yield actionable insights or too specific to one context to apply
universally.

The challenge extends beyond scoring mechanisms to the fundamental
question of what governance success looks like. For AI systems, a
\"low-risk\" classification under standardized frameworks might miss
context-specific harms that only become visible when examining
particular use cases and affected populations. Effective governance
requires both interoperable standards for cross-organizational learning
and contextual assessment layers that capture domain-specific risks. The
solution is not choosing between standardization and contextualization,
but designing tiered approaches that serve both functions without
conflating them.

## The Measurement-Action Gap

A 2024 survey by the International Association of Privacy Professionals
found that while 93% of organizations recognize AI governance risks,
only 9% feel prepared to address them (IAPP, 2024). This gap between
awareness and action reveals a fundamental limitation of governance
frameworks: metrics alone do not drive organizational change.
Understanding that risks exist differs fundamentally from knowing what
to do about them.

Building NASA\'s Data Maturity Assessment forced me to confront this
challenge directly. Collecting assessment data and generating maturity
scores was the straightforward part. The harder question was: what
should leadership actually do with a score of 3 out of 6 in data
governance? Does that score mean \"acceptable progress\" or \"critical
deficiency\"? What specific actions should follow? Without clear
pathways from diagnosis to intervention, assessment becomes performative
rather than operational. We struggled to translate aggregated scores
into meaningful narratives that would guide resource allocation and
policy decisions.

For AI governance, this problem compounds. Organizations can measure
model accuracy, document training data sources, and quantify bias
metrics, yet still lack clarity on acceptable thresholds or remediation
strategies. Assessment frameworks must embed decision logics, not just
measurement methodologies. This means defining not only what to measure,
but what scores trigger specific governance responses, who has authority
to act, and what interventions are available. Governance infrastructure
requires actionable pathways, not just diagnostic capabilities.

## The Expertise Paradox

The OECD principles emphasize that data quality directly affects the
accuracy of AI outputs (OECD, 2024). This same principle applies to
governance assessment itself: the validity of governance evaluations
depends on the quality of assessor inputs. Yet determining who is
qualified to assess complex socio-technical systems remains an
unresolved challenge.

NASA\'s Data Maturity Assessment spans six pillars, from technical
infrastructure to organizational culture. An assessment question about
data protection and privacy compliance might be answered by a
cybersecurity expert with two decades of regulatory experience or by a
program manager with minimal technical background. Both responses
contribute equally to the aggregate maturity score, yet their inputs
carry vastly different validity. The expert understands nuanced
compliance requirements, while the novice offers an educated guess.
Aggregating these responses produces scores that obscure rather than
clarify actual governance maturity.

For AI governance, this challenge intensifies. Who should assess whether
an AI system is \"trustworthy\"? Engineers understand technical
architectures but may miss societal implications. Ethicists grasp
normative concerns but may lack implementation expertise. Affected
communities have lived experience but may not understand system
internals. Inclusive governance suggests broad participation, yet valid
assessment requires domain expertise. Weighting inputs by role or
expertise creates hierarchies that undermine democratic participation.
Stratifying assessments by expertise level risks fragmenting
organizational understanding. There is no clean resolution, only
conscious design choices about whose knowledge counts and how competing
perspectives are reconciled.

## Conclusion

These four tensions will not disappear as AI governance frameworks
mature. Privacy will continue to conflict with accountability.
Standardized metrics will remain inadequate for capturing
context-specific risks. Organizations will struggle to translate
assessment data into action. Questions about whose expertise counts in
governance evaluation will persist. Acknowledging these tensions as
inherent to governance design, rather than temporary implementation
challenges, is essential for building effective systems.

My experience developing NASA\'s Data Maturity Assessment revealed that
practical implementation surfaces governance challenges that abstract
frameworks obscure. Moving from principle to practice requires making
explicit tradeoffs: Which value takes precedence when privacy conflicts
with oversight? How do we balance interoperability with contextual
validity? What mechanisms translate measurement into meaningful
organizational change? How do we honor diverse perspectives while
ensuring assessment rigor?

AI governance is entering an operational phase where these questions
demand answers. The path forward requires honesty about tradeoffs rather
than aspirational rhetoric claiming all values can be simultaneously
maximized. Organizations that acknowledge governance tensions and design
systems with conscious awareness of these tradeoffs will build more
effective, legitimate, and sustainable governance infrastructure than
those that pretend such tensions do not exist.

**References**

International Association of Privacy Professionals (IAPP). (2024). *AI
Governance in Practice Report 2024*. Retrieved from
<https://iapp.org/resources/article/ai-governance-in-practice-report>

National Institute of Standards and Technology (NIST). (2023).
*Artificial Intelligence Risk Management Framework (AI RMF 1.0)*. U.S.
Department of Commerce. <https://doi.org/10.6028/NIST.AI.100-1>

Organisation for Economic Co-operation and Development (OECD). (2024).
*Recommendation of the Council on Artificial Intelligence*. OECD Legal
Instruments. Retrieved from
<https://legalinstruments.oecd.org/en/instruments/OECD-LEGAL-0449>
