---
layout: page
permalink: /interoperable-accessible-e2ee/
title: "Interoperable and accessible E2EE"
nav: false
---

**Project description:**

In this project, we built a prototype for interoperable and accessible end-to-end encryption using Messaging Layer Security (MLS) layered on AT Protocol (atproto).

The problem: Many apps could be more privacy-centric with zero-trust E2EE, but developing such apps today requires cryptographic expertise. Additionally, most E2EE apps today create lock-in for users: they cannot leave the apps without losing their data or communicate with others over E2EE using different apps.

To solve for the above, we created a developer library that uses MLS on top of AT Protocol that handles group key agreement and defines a usable API, so developers can add E2EE without becoming crypto experts. Additionally, our library uses MLS's metadata field to keep message schema plaintext while message content is encrypted, so both credible exit (switching app providers) and interoperability (communicating with people who use different app providers) are preserved.

Additionally, we seek to do formal verification of keypair-identity binding under our proposed mitigations against server-side identity forgery, using atproto DIDs. MLS separates a trusted authn service (AS) from an untrusted delivery service (DS). Most deployments (Matrix, RCS, Discord), including ours, centralize both, undermining this assumption. Our formal verification aims to advance MLS security discussions under such configurations.

We will be applying for grants to continue this work, and working with a team that is developing a community portal that functions as a Slack alternative as the first developers and testers using our library. To get involved with this project or use the library we developed prior to its public release, please reach out to arushi@habitat.network.

**Contributors:**
Arushi, Harrison N
