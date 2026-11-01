---
layout: page
permalink: /little-homes/
title: "Little Homes: Secure Chat for Direct Action Groups"
nav: false
sitemap: false # unlisted: not in nav or sitemap until project members approve
---

**Project description:**

Little Homes is a design for encrypted group chat reconsidered for activists, organisers and civic volunteer groups. It extends Ink & Switch's Backchannel, in which nobody has a name or key that follows them from one relationship to the next.

**The problem:** Groups like these rely on Signal, which encrypts messages well but gives every user one identity across all their groups. Anyone who shares a single group with you can see which other groups you're in, and a seized phone reveals every group on it and everyone in them. Meanwhile, their biggest risks are operational: people added to the wrong group, messages sent to the wrong room, data that lingers on devices across sprawling membership, and membership itself increasingly being treated as evidence of complicity in crime.

**What we did:** We extended Ink & Switch's Backchannel, a one-to-one messenger with no global identity, to support groups. The design covers the cryptographic protocol (a shared, rotating room key, keys unique to each pair of members in each room, and zero-knowledge proofs that you're entitled to enter a room), along with interface flows and wireframes. We also ported Backchannel's frontend from React to Svelte as the base for a prototype, modifying it for group chat using patterns from Encrypted Spaces.

**How we did it:** We worked through scenarios on a whiteboard, with the cryptographic steps, the interface and the social dynamics side by side, so each design choice had to make sense at all three levels. Porting the code meant reading Backchannel and Encrypted Spaces closely, which settled key decisions such as joiners generating their own keys and room keys being kept out of the synced history.

**Potential impact:** Little Homes makes good security habits the easy path rather than an expert's job. Room templates set expiring messages, physical check-ins and visible security levels by default. A room is described by who may enter it rather than by a global name, and splitting into a smaller room is as ordinary as starting a thread. That lets small groups protect themselves from infiltration, wrong-room mistakes and device seizure without a security professional on the team, and mitigates leaving a trail of shared memberships that exposes them.

**Artifacts:**

- [Writeup](https://notes.infinite.build/wBslAozkQzCdMFryCnWskg?view)
- [Description](https://notes.infinite.build/M6XT6VZ9SWa9DksBBhdzCA?both)
- [Code](https://gitlab.com/voboda/little-homes)

**Contributors:**
Voboda, Ada, Michele
