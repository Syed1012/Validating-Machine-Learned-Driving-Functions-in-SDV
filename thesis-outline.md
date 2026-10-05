# Thesis outline

Working notes, will update continous. Chapter titles are placeholders until the findings exist.

The thesis in one line: who decides that the evidence for an ML driving function is enough to release, on what basis, and what happens to that decision when the model is retrained and pushed over the air.

Two things I keep mixing up, so writing them down:

- Accuracy is not sufficiency. A model can be very good and the evidence for releasing it can still be thin. The thesis is about the second.
- UN R156 and ISO 24089 deal with how an update is managed and risk-assessed. From what I have read so far they do not say how to judge whether a retrained model behaves acceptably. Not sure about that yet, need to read both properly before I claim it anywhere.

---

## Abstract

Problem, three RQs, method, main finding. Under 200 words.

## 1. The release problem

Start with one concrete case, not statistics: a lane keeping or emergency braking model gets retrained and goes out over the air. What was signed off before, and what is signed off now? The RAND number (about 11 billion miles to show a 20% improvement with 80% confidence) comes in here as the reason road testing cannot be the answer.

- 1.1 Starting point
- 1.2 The gap
- 1.3 Research questions
- 1.4 What I claim
- 1.5 What I am not doing (no new safety method, no accuracy benchmark, no fully autonomous driving)
- 1.6 How the thesis is laid out


## 2. A car that changes after it is sold

Short, three or four pages. The point is only this: the thing that was approved is not necessarily the thing running in the car a year later.

- 2.1 From one control unit per function to central compute
- 2.2 Updates as a regulated activity (R156, ISO 24089)
- 2.3 Where learned functions sit in this

## 3. Three standards, three different questions

26262 asks what happens when something breaks. 21448 asks what happens when nothing breaks and the function is still not good enough. 8800 asks what changes when the behaviour came from data. I want a table here with columns: question it asks, evidence it expects, what it says about updates. The last column will probably have a lot of "nothing" in it.

Worth noting that 8800 is a PAS, not a full international standard. Check what that means for how assessors actually use it. Also read Salay et al. on where 26262 assumptions break for ML.

- 3.1 ISO 26262
- 3.2 ISO 21448 (SOTIF)
- 3.3 ISO/PAS 8800
- 3.4 Side by side

## 4. What has already been answered

Organise by the question each body of work answers, not by author. An author-by-author list reads like a catalogue and hides the gap.

| Question | Where to look | What it leaves open |
|---|---|---|
| Can 26262 cope with ML at all? | Salay et al., Borg et al. (deep learning V&V in automotive) | Says what breaks, not what teams do about it |
| How do you build a safety case for an ML component? | AMLAS (York), UL 4600, the SMIRK pedestrian braking case | Gives the structure of an argument, not how an organisation decides it is strong enough |
| What do practitioners think of validation evidence? | interview studies | Mostly opinions on methods, not release decisions |
| How do teams learn under constraint? | continuous experimentation literature (Münch's group) | Assumes release is allowed to be the experiment |
| AI and standards in other regulated domains | Straub et al. (space) | Automotive not covered |

Then one plain paragraph stating the gap. I should write that paragraph first and then check every row of the table supports it.

## 5. Study design

Runeson and Höst. Single case, embedded units, interviews as main source, documents as second source. Purposive sampling across product, architecture, ML engineering, safety and quality, project leads.

- 5.1 Why a case study and not a survey
- 5.2 Case and units
- 5.3 Data collection
- 5.4 Analysis (content analysis, iterative coding, categories allowed to move)
- 5.5 My position: I work at the company I am studying. Say it here, early, plainly.
- 5.6 Validity
- 5.7 If access shrinks

5.7 matters. Realistically it is five or six interviews and not much internal material. Plan B: lean on documents I can get, and on public safety-case material (the SMIRK case, the AMLAS example) as a second, open data source. Say now what the thesis can and cannot claim with that.

## 6. Working with a small corpus

Local retrieval over transcripts and documents, used while coding. Local because the data cannot leave the building anyway, so that is a constraint I am working with and not a preference. Describe it as a method step with a limit, not as a product. Keep it short, two or three pages. Details sit in `application-ideas/`.

- 6.1 Why local
- 6.2 What it indexes and what a query looks like
- 6.3 Where it changed my coding, and where it got in the way

6.3 needs real examples from the analysis, so this chapter gets written after chapter 9, not before.

## 7. The case

Anonymised. What a release looks like at the company, who is in the room, what documents exist. Short. R&H say describe the context before the findings, otherwise the findings float.

## 8. How features get picked (RQ1)

Findings. Who proposes an ML feature, what counts as worth building, how much of that is decided before safety people see it. I suspect the interesting part is where product and safety disagree. Wait for the data.

## 9. What stands in for experimentation (RQ2)

Shadow mode, re-simulation against recorded drives, proving ground, scenario-based testing, staged rollout where it is allowed at all. Which ones are really used, at what point, and who trusts them.

## 10. Evidence ledger (RQ3, part one)

A table I build from the findings: for each practice, what it can show, what it cannot show, who relies on it. Idea is to make "what stays unknown" something you can read off a page. Compare against the 8800 expectations from chapter 3.

## 11. Open at release, and after retraining (RQ3, part two)

Two parts. First, the register of questions that are still open on release day, as people describe them. Second, one retraining walked through step by step: what is re-run, what is assumed to carry over, who decides. This is the chapter I care most about and the one I am least sure the data will fill.

## 12. Discussion

- 12.1 What "enough" turned out to mean
- 12.2 What a team could do differently on Monday
- 12.3 Propositions for other regulated domains (medical devices, avionics) and where I think they would not hold
- 12.4 Threats to validity checked against what I actually found

## 13. Conclusion

Three contributions matching three RQs, limits stated plainly (interview count, one company), and what a study with wider access would look at.

## Appendix

- A. Interview guide
- B. Coding book
- C. Consent and anonymisation
- D. Evidence ledger template
- E. Notes on the retrieval tool

---

## Still to read properly

- AMLAS paper (York) and one worked example
- UL 4600, at least the safety case parts
- SMIRK safety case paper
- Salay et al. on ISO 26262 and ML
- UN R156 and ISO 24089 texts, for the retraining claim in the notes above
- ISO/PAS 8800 itself, through the university library if possible

## Open Doubts

- Is a separate case chapter (7) expected, or should it sit inside the method chapter?
- How should the retrieval tool be weighted: method detail or contribution?
- Which language: English throughout, or German for the abstract as well?
- Does the PSE program have its own template, or does the INF one apply?
