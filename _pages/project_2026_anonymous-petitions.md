---
layout: page
permalink: /anonymous-petitions/
title: "Anonymous Petitions"
nav: false
sitemap: false # unlisted: not in nav or sitemap until project members approve
---

**Project description:**

**One sentence summary:** A cryptographic system that lets employees sign a union authorization petition so that the count is publicly verifiable while the employer can never learn who signed.

**The problem:** In an organizing campaign the employer is the adversary, and the employer holds all the data — the mail servers, the identity directory, the staff list, the devices. Any system built purely on employer-controlled inputs is logically impossible to secure, because the employer can simply simulate it. Meanwhile the current practice — signed authorization cards carrying names — puts the identity of every signatory into a single document, and retaliation against real people is the cost of a leak.

**What we're building:** A petition system where an employee can prove "I am an employee of this company, as of a date before this campaign began, and I support this petition" without revealing which employee they are, and without any party — including us — being able to find out later. The output is a single number plus a proof: N distinct eligible employees signed, verifiable by a labor board, a court, or their expert, with no trust in the operators.

**How:** Employment is proven from DKIM signatures already sitting in employees' inboxes — the employer's own mail infrastructure signs every message, and zkEmail verifies that signature inside a zero-knowledge proof, revealing only the sending domain and a date cut-off. Double signing is prevented by a nullifier derived through a verifiable oblivious pseudorandom function (VOPRF), whose key is split across several independent operators so that no one — including an insider — can hash the staff list to find signatories. The tally itself stays private; a second recursive proof attests that every entry was valid, that no nullifier appears twice, and that the count is N. Because email alone can always be spoofed by whoever owns the mailboxes, submissions can additionally carry evidence from channels the employer does not control: membership in campaign Signal or Facebook groups via zkTLS web proofs, or in-person NFC attestation by designated organizers.

**Why it matters:** Petition and election privacy is the precondition for people exercising labor rights without fear, and right now that privacy rests on procedural promises rather than on mathematics. Making it structural rather than procedural also removes a whole class of intimidation tactics from the employer's repertoire. The same construction generalizes to any petition where the adversary owns the infrastructure.

**What's next:** The load-bearing open questions are what a receiving body actually accepts as a valid showing of support, and whether raw DKIM headers can be extracted onto a personal phone at all. We also want to build the system and test it with potential users to identify privacy or usability concerns. We'll need labor lawyers, cryptographers, and mobile engineers to help make this project a reality.

**Artifacts:**

- [Demo Day slides (PDF)]({{ '/assets/projects/2026/anonymous-petitions/demo-day-talk.pdf' | relative_url }})

**Contributors:**
Kentrell, Voboda, Ying Tong, Janabel

**Contact:**
[anonymouspetitions@duck.com](mailto:anonymouspetitions@duck.com)
