# 5. OSINT method

## Learning outcomes

- Define OSINT as a disciplined process, not a list of search tools.
- Collect public information ethically, legally, and proportionately.
- Verify claims and communicate uncertainty.

## A repeatable OSINT workflow

1. **Define purpose:** connect the research question to an authorized defensive decision.
2. **Set boundaries:** identify allowed sources, data subjects, collection methods, time window, and stop conditions.
3. **Collect:** use appropriate public sources and retain URLs, timestamps, and context.
4. **Verify:** compare independent sources, check original publication, distinguish copied claims, and test whether a page is current.
5. **Analyze:** assess relevance, confidence, alternatives, and potential harm from disclosure.
6. **Disseminate:** share only what the audience needs and respect source terms and handling restrictions.

## Useful source categories

Public advisories, technical research, public registries, documentation, certificate-transparency data, code repositories, public DNS and network measurement services, and reputable incident reports can all contribute context. The best source depends on the question; broad search is not a substitute for source evaluation.

## Reliability, bias, and privacy

Public availability does not make information accurate, ethical to collect, or safe to republish. Confirm a claim at its origin, seek independent corroboration, and check dates and methodology. Avoid collecting personal data that is not necessary to the defensive question. Do not interact with exposed services or accounts in ways that exceed authorization.

Threat actors also use public information. Defenders can apply the same discipline to their organization's own exposure review, under approved scope, to identify accidental disclosure and improve controls.

## Note-taking template

| Field | Record |
|---|---|
| Question and authorized purpose | What decision will this research support? |
| Source and original URL | Where did the claim originate? |
| Collection time and publication time | Are they distinct? |
| Claim and supporting evidence | What is directly observed? |
| Reliability / confidence | Why should this claim be trusted? |
| Corroboration and alternatives | What else could explain it? |
| Restrictions and sensitivity | What can be shared, with whom, and for how long? |
| Assessment and next step | What action is justified? |

## Review prompts

1. Why is source triangulation necessary when multiple articles repeat one vendor report?
2. What is the minimum data needed to answer a defensive exposure question?
3. How will you distinguish an observed fact from your analytic interpretation?
