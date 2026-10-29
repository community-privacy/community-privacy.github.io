---
layout: post
permalink: /tough-puzzles/
title: tough puzzles at the community privacy residency
nav: true
nav_order: 4
external_source: false
content: content of the post is here??
feed_content: summary of post
date: 2026-10-13
tags: reflections
description: three weeks in a Brandenburg farmhouse, and the problems that threw out the textbook threat model
---

_Written by voboda. Originally published at [voboda.com](https://voboda.com/blog/community-privacy-residency/) on 13 October 2026; cross-posted with permission._

> "As soon as you're caught in the room, cryptography won't help you."

Most cryptographers are trained on that separation of concerns. If you're locked in a room, someone can coerce you into handing over your password and cryptographic keys, so that part is "out of scope".

During three weeks at the [Community Privacy Residency](https://community-privacy.github.io/), I met a journalist from an occupied territory, and his reality threw the whole distinction out.

There were daily roadblocks, with military police doing phone inspections. If you didn't unlock your phone, you were detained and your phone confiscated. If there was an encrypted chat app on your phone, you were detained and investigated. If there was a number from the wrong area code in your call log, you could be arrested on terrorism charges. If you were a regular suspect or a journalist, they had no problem leaning on your family with threats of detention. Detention without charge, potentially for years.

So if you need to go to the shop, you can't go with Signal on your phone. Not if you want to make it back home.

It's based on perception, not reality. WhatsApp is end-to-end encrypted, and nobody looks twice. Telegram isn't (by default), and it's treated as a cause for suspicion.

Anything that looks like encryption - an app with "secure" in the name, a blob of encoded text in a message, is like "waving a flag and saying, come take me."

Plausible deniability, one of cryptography's favourite answers to coercion, made it worse. A soldier at a roadblock who knows hidden profiles might exist on a phone can never know they've seen all of them. That obliges them to keep turning up the pressure. And the more uncomfortable part that took a while to say out loud: think about what this does to someone being interrogated or tortured.

That was one puzzle. There were plenty more.

## The short train

Before we arrived, everyone was pinging each other on Signal, working out who could ride together from Berlin to the house in Brandenburg. That's how I met the journalist, on the train platform, and it was an embarrassing start. I’d found a free bench at the far end of the platform, but didn't realise it was a short train. After an hour of waiting, we only saw the train as it pulled out, and we had three hours until the next one.

The village called our old farmhouse "the bunker" because after WWII its facade was redone in typical socialist concrete. About fifteen years before we arrived, a couple bought it, took the concrete off, and started restoring it. They had an ethos, and saw themselves as restoring an environment that had been designed to be adaptive and let people thrive.

High ceilings, big windows and creaky wooden floors. Downstairs, the huge kitchen opened into an even bigger common room, with a modular table long enough for thirty people. Couches ran along the walls. Thirteen bedrooms across two floors. A few tents in the big garden outside, surrounded by farms. The closest shop was in a town eight kilometres away.

We were about thirty people once you counted the mentors and guests staying overnight, and the organisers were putting final touches on the first puzzle: who slept where. A list of special requests, matched against the rooms of an old house.

Then we went round the table and introduced ourselves. I'd seen [last year's projects](https://community-privacy.github.io/2025-projects/), so I knew the people would be smart. I didn't expect to feel this out of my league. A Brazilian resident protecting activists and journalists who report on cartels. A digital rights lawyer from India, working on internet shutdowns and gender-based violence. New York protest organisers. Prisoners' rights researchers. Legal counsel for massive human rights orgs. A security director for a journalism protection association. A mathematician researching an emerging category in post-quantum cryptography. And someone who popped in a few times to help make lunch, modest but happy to talk shop, turned out to be the Mr. Wolf of TEE architecture.

A world-class cryptographer sat next to someone on the front lines of a freedom movement, and you could feel it both ways: everyone was accomplished, and everyone was a little intimidated. The game was "draw your life in 2 minutes" which was loads of fun, and let us glimpses of what really made us who we are beyond our credentials. But we still introduced ourselves through the institutions we'd passed through, the names that carry clout.

## Picking your teachers

On the day people settled on projects, I was tired and behind, and needed more time to read all the poster sessions taped up around the main room.

I'd brought a question with me: which problems really matter now, out in the world? And we'd spent a few days naming real problems from real communities, circulating them, and leaving them for other people to pick up. The idea was to team up around real needs rather than our pet projects. The project I applied with was a way to deliver apps [without depending on centralised app stores](https://voboda.com/blog/webpage-hijacks/). In one group session I asked, "Has anyone heard about [the F-Droid problem with Google's developer ID policy](https://f-droid.org/en/2026/02/24/open-letter-opposing-developer-verification.html)?" Most of the room put their hands up, but it didn't get anyone excited.

The guy doing operational security for researchers in South America was standing on his own, and I went over, thinking I'd love to learn from him. Like at university: pick the teacher, not the subject. I could just work on whatever he picked. But he was still undecided. Right beside was an abandoned poster: help journalists working in occupations with phone and device inspection/confiscation. If a journalist teamed up on this, would he be interested? I knew one from the train ride. I walked over and asked. He was in too. So it started with the three of us.

There was also a question on the wall I hadn't noticed.

> How do you get better forms of identity in chat apps, to keep out imposters?

I wrote a note back, half-joking:

> ZK. Who are you?

That note kicked off a collab: a chat app she later named Little Homes. What if the answer wasn't better identity, in the cryptographically verifiable sense, but accepting we can't rely on it, and working from there? Ink & Switch had built something like this, [Backchannel](https://github.com/inkandswitch/backchannel): no global key directory. Two people swap a short one-time code, their devices derive a shared key, and that key is the relationship. No global key, no global identifier. I'd been toying with the idea for [Infinite Build](https://www.infinite.build/), where I wanted everybody to have full agency over their group learning experiences. She was circling the same questions for direct action groups.

We kept meeting each other like quarks all over the house. Conversations in stairwells, over the kitchen sink, people exploring the grounds. I met a friend of a resident in the garden when she arrived. She introduced herself as being short but not too short to need children's shoes. Her friend introduced her as working for the UN. I kidded her about how all our modern organisations are built the same way, with the same hierarchies, then fail under the same pressures, in the same directions. And somehow we're surprised every time. She said, "we're going to be friends." We got on to talking about our parents who were displaced by political shifts, and what that means to our identities and responsibilities.

At the end of the week, we had an event in Berlin at the [Casino for Social Medicine](https://iniradar.org/casino-for-social-medicine/). It was packed, with people standing outside on the street looking in. From the shows-of-hands in different presentations, I picked up maybe a quarter of the room were cryptographers or deep in opsec. A huge number had made sure there was no online record of the events they go to. One of us started their presentation with a question, "If I say The Hegemonic Internet, do you know what I mean?" and the place erupted in snaps and laughter.

## The barn studio

Back at the farmhouse, some people could put on headphones and work right through the noise of the main room, with the kitchen next door. Some of us needed quiet. So the hosts let us use a studio above the barn.

That's where we worked out Little Homes, on a whiteboard. Arisu, Karoi, Satoshi and Taka stood in for Alice and Bob, and every step had the cryptographic protocol, the UI and the social graph drawn side by side, to keep them [congruent](https://voboda.com/blog/better-affordances-for-federated-systems/). We broke direct action groups down into roles: leadership, staff, super volunteers, and the general community. The horde!

My collaborator advises direct action groups, and she could tell the security needs they have from the ones they feel. They worry about infiltrators, and about adding the wrong person to a group or posting in the wrong place. [Hegsething themselves](https://www.theatlantic.com/politics/archive/2025/03/trump-administration-accidentally-texted-me-its-war-plans/682151/). Their more immediate risks are around operational security, data hanging around on insecure devices and that type of thing, but that's not something they tend to see until it's too late. Also chat group membership itself is becoming legal exposure: being in a group where others planned something is used in court to argue you were part of it. We wanted to address all of this.

For high-risk scenarios, we designed NFC check-ins as a countermeasure to group members being captured, coerced or losing their phones: check in with another member regularly, or you get kicked from the group and the phone auto-deletes message history.

Then started with the question she'd written on the wall. Identity and impersonation. Almost every chat app gives you one username and one public key that follows you everywhere. Say you've joined your local Alcoholics Anonymous group on Signal. Then you meet someone in a professional context and join their group too. Now they can see you're in AA. On Signal, seeing common groups is a feature. For these groups, it's doxxing. And the central user list gives rise to accidentally adding the wrong person, not to mention a place for people to create look-alike accounts.

So in Little Homes, if you and I are both in rooms A and B, we hold different keys for each other in each. Nothing in room B tells me you're the person I know from room A. No common username, IDs or keys at the protocol level. Only you can disclose this. This means every pair of people in a room needs to introduce themselves with a specific name and a unique signing key for that group.

It doesn't scale, but it doesn't have to: the groups we were designing for maxed out at twenty or thirty people.

Under this system, some things broke right away, like @mentions. The name I use for you, a [petname](http://www.skyhunter.com/marcs/petnames/IntroPetNames.html), is mine alone, and can be meaningless (or revealing) to others in the room. What if an @mention was stripped out and turned into a private notification for that message? But then nobody else knows who the message was for, so it's really more like a DM nudge for a public message. And also, one typo can leak your name for someone.

Backchannel syncs through Automerge, a CRDT that keeps its full history forever. That's the right thing for messages and the wrong thing for room keys that are meant to be rotated and destroyed. A rotated key stored there would never really be gone. So room keys live outside it, on the device, where deleting them actually deletes them.

I brought in a problem I keep seeing in online communities. Every online group has an admin who holds the control. But in real communities, the people actually leading often aren't the admins or the staff. They get frustrated and leave, and the admins go looking for new moderators. It turns out this happens a lot in larger US direct action groups too.

So in Little Homes, rooms have no admins. A room's policy is fixed when it's created. To change it, you fork: you start a new room with the new policy, and members of the old room prove their way in. In the app interface, that can still feel like changing the room's settings and pressing _Save_.

As we worked through each step, my collaborator and I sometimes pulled in different directions. She wanted to protect anonymity across groups more than I did, because accidental doxxing is how these groups get hurt. This design was already way safer for them and I didn't want to lose users to annoying security steps. My proposal: when joining a room, just announce the name you'd like to go by. If you'd rather stay anonymous, you can, and tell your name only to specific people. She wanted anonymity by default, with no announcing. But then every time a room split off, you'd have to swap names with each member again...

Whenever we got to an issue like this, we'd stop and ask what assumptions we weren't putting on the whiteboard. Sometimes we couldn't name the use case that called for a specific privacy property, it was more an instinct. Then a scenario would pop up later. There! That's why! It went both ways. We trusted each other's intuition and gave the other room to explore. We kept those options open.

She explored an "are you this person?" protocol. Say I'm in a new room and think I recognise you. Can I ask, "Are you Arisu?" The catch: just asking tells a possible stranger there might be an Arisu around, which is a doxxing problem. So we dropped it, but it got us somewhere I didn't expect. Members of a new room already had private one-to-one channels from the old room, so they could use those to share the new room's keys, without swapping codes from scratch. And each person joining could choose whether to introduce themselves, and to whom. Nothing was announced by default.

## Couch City

Riley, one of the organisers, grabbed a bunch of us and cut out half of the big table. What was left of it became a coworking table, where people worked with headphones on. We filled the other half of the room with unused couches, carrying them from the barn across the garden. Someone called it Couch City and the name stuck.

Couch City did a lot. Small teams worked there, and you could overhear and jump in. People were more willing to host a workshop, because the couches made it feel easy-going and less official. Around eleven every night there was an NYT crossword ritual on the projector, everyone shouting answers while one person typed madly. It's insane to watch someone finish the NYT crossword in a couple of minutes.

After dinner, people drifted out to the patio. More than once I passed conversations about old jams: you like that too? Then the stories went deeper. Our parents: the Nigerians would imitate theirs, full accents and body language, and argue with each other in character. The Indians would talk about theirs, and about dealing with their approval. All the coming-out experiences too. Poetry readings. Poetry divinings. A chess board appeared with a label you could flip: black turn / white turn. I'd catch up on games when I walked by, and played a few turns. There was always something to connect on.

Early in week two, we had our first big meeting since forming teams. Laptops open, people half-listening to each other's updates. I felt it was a bit corporate but didn't know how to say that nicely. Our UN friend was sat on a couch in the corner. She was asked if she'd like to share an update alongside our projects. Instead she said, "Thanks for offering me this space. I'm going to use it to share how I'm feeling." Looking around the table, she said, "Disconnected." Everyone in the room had been talking about their anti-colonial work, and she invited us to reflect on whether a boardroom table and status updates were the format we really wanted. It was a question for all of us, about habits we'd carried in from our academic and corporate lives. She knew the irony, and deals with it all the time: her own organisation still calls its work "missions".

Our journalism team had grown to six or seven of us, and I was struggling to organise and facilitate. A UX designer offered to run Cade Diehm's Anxiety Mapping workshop for us one evening: we individually brainstormed every troubling scenario we could think of. One stage of Anxiety Mapping combined our separate scenarios into one, literally using dice rolls:

> You've been arrested at a roadblock, with sensitive evidence on your phone, during an internet shutdown. Also there's a flood.

Oh come on, does this really happen? And the journalist said, actually, yeah it did. And later he pushed back even more:

> "[Security experts] are always thinking about the threat modeling top-down, like the state does. You're not looking at the human being who's actually fighting something."

My first thought was: that's a great line for the presentation. Then it hit me: I'd come to the residency partly to learn threat modeling from professionals, and here was the person I wanted to do it for, commenting on ten years of threat modeling done for him. But I've seen what good stuff comes out of just trying to see through the eyes of the individual people you're trying to help. It struck me that I might have something to offer here.

From there we split off, each of us researching one of the areas he'd identified.

The same designer helped with Little Homes. (She was everywhere - helping almost all the teams!) She sat with us for an hour, then the next day, in about twenty minutes, she speedran ten or fifteen flows. She'd taken our group relationship map, which was never meant for the interface, and told us that was the right mental model, but too complex for a small phone screen. So we jammed on it. What about skewing it into a grid-like space? Swipe sideways between separate social groups, scroll down to the rooms connected within one.

The harder part was telling rooms apart. We'd been debating whether rooms should have petnames too, a name each member sets, or one shared name to anchor some common purpose, like regular chat apps. We never settled it. But when we got to the descriptor text on each room's card, what distinguished a room was its size, the members you know, and most of all the policy for getting in: people in this room are admitted by being in rooms D, F or J, or by invitation from these specific people. The rule for who gets in, written in social terms, turned out to be more meaningful and orienting than a name alone.

## The house

Mentors and guests kept arriving. On Fridays, the organisers ran a happy hour at the house, and people they'd invited arrived from Berlin in waves by train.

Some of the visitors were last year's residents. They did a lot of weaving between us, and took care of people's human needs: inviting us to open up to each other, or to look after ourselves when we were pushing too hard.

The house had never hosted a group this big, for this long. It had one fridge, and one standard oven.

From the start, someone found masking tape lying around and labelled every kitchen cupboard, so nobody had to open each one to find a pan. Within hours, other labels appeared: "frozen assets" (on the freezer), "skeletons" (on the closet), "killer robots". Nobody could ever find the recycling box, until it got a huge label: "the future hope of humanity".

Groceries could only be delivered twice a week and overflowed the fridge and cupboards, onto windowsills. One of us had set up a shelf for special-diet food, but if one or two people didn't read the label, food ended up anywhere anyway. Not everyone signed up to the cleaning/cooking rota, which strained the people who did, so someone moved it off a spreadsheet and onto a whiteboard in the kitchen, to help make it easy. But people got confused. The cooking schedule lived in two places, and one day one of our best cooks turned up to find it had changed. Each fix was partial, and the people who broke something weren't doing it on purpose. Different ideas of what's normal, how things should work, what's intuitive, colliding constantly.

The house owners wanted to design an environment where people do good work. We were all designers of digital spaces that other people live in. And here we were tripping over each other on a cleaning rota. It felt a bit like a reality TV show.

One resident had a line for it: solidarity works until someone has to do the dishes. But someone was always in the kitchen, cleaning, loading or unloading the dishwasher, whether asked or not. In the first week, he and a few others took on an evening cleaning shift that wasn't even on the rota.

I took the first cooking shift, the stress test, and when not all the ingredients arrived, an Italian mentor helped me improvise a pasta Parmigiana on barbeques on the patio. I’ve run residencies like this before, and I couldn’t switch that part of my brain off. I kept pitching in, and some people started assuming I was one of the organisers when I wasn’t.

By the second week, some strain was showing. One evening, around the big patio table, the organisers offered an open space for feedback. We'd arrived with different expectations, some of us for the projects and some for the people. Some were juggling day jobs. Everyone spoke with understanding and gratitude, but some of the notes were sharp: hire a facilitator, hire ops people.

Mine was about the fridge. I'd been looking at the house as a system, and it seemed to me a lot of seemingly unrelated problems traced back to that one fridge. Only two deliveries a week meant the fridge was in constant 3D Tetris. Ingredients were always lost, making it hard to cook big lunches. Then we needed cooking schedules, and that took people away from other things... Really the venue should have provided this, knowing how many people they were hosting. Buying a big fridge for someone else's house seems crazy, but 500 euros would have easily saved a hundred hours across the 20 residents.

Tbh I thought a lot of the feedback was a bit unfair but the organisers just listened. They didn't defend themselves, not once, even for things that weren't on them. When we asked about budget, it came out that they had hired help, on a tight budget, and had been paying for a lot of things out of their own pockets.

It was their second residency. I'd asked Riley how they chose the residents, because twenty people who'd never met clicked within days. That's really hard to do so well. They told me they spent weeks imagining different combinations of us together in a house. What would we talk about? They know it's about people, not rubrics. And they just put in the time to get that right.

To me, the thing about residencies is that if you get the people mix right, they don't need much structure. Everyone finds who they need and makes use of the proximity and time together.

In the kitchen one day, I asked Janabel, a mathematician and one of the organisers, if she could express her goals for the residency in terms of group theory: what's the transformation you want here? She thought about it and said, "Our relationship graph goes to diameter 1." Everyone in direct relationship with everyone else.

They'd done this all without a big funder, because they wanted something like this to exist in the world: a place for journalists' needs to be met, for protesters to find protection, and for fabulous queer technologies to find their roots.

## The cucumbers

In the evenings people went for walks. The work came along on the walks too, but more in the way you could ask about the person behind a project. One path out of the village led to an industrial cucumber farm, fifty acres under the windmills. Most of the cucumbers had overgrown to three or four kilos.

There was a whole thing between the people from agricultural places and the people from supermarket places. A lot of us, me included, were nerds about agriculture without having lived it. So there were debates. I thought, those have to be zucchinis. Others said cucumbers, just not edible now. It became a game for me. I’d steer people with opposite takes toward each other and let them argue it out. It was nice to see such smart people let themselves be caught out on something trivial.

By the end, newcomers were walking out to see the giant cucumbers they'd heard about, and bringing them back for a big salad for everyone.

## What people carried

We were all drawn into these causes for different reasons. Look back at that round of introductions: cartels, internet shutdowns, gender-based violence, prisoners, protests. If you work on the front lines of something like that, you've been around trauma. You shoulder the pain of real people you've watched suffer, and have probably been through some shit yourself.

A trans resident talked about driver's licences being revoked, and valid documents with an X gender marker suddenly not being accepted. And about cities and towns where the likelihood of hate crime was enough to plan your day around.

One morning over breakfast, I realised the person I was talking with had been an international athlete, and mentioned that someone else in the house was too. He explained: if you look like me, you have to be the best before anyone will treat you with respect.

There was another resident I'd been looking forward to meeting, and I didn't meet her until three or four days in. She told me about a health project she did in The Gambia, where the local team asked her to get off a bus to make room for the white people, assuming they were the only donors and the doctors. She cried while she told it, the emotion still so present.

A lot of people talked about systemic privilege but her story made it hit home. She gets recruited by companies most people would work years just to interview with, and has turned them down because the reception desk, seeing her skin colour, assumed she was there to deliver something. Taken for a gig worker once, it's a story. When it happens everywhere you go, it's a drag you carry. When it happens in the lobby of a company that wants to hire you, it's a tell about what working there would be like. And there aren't many companies at that level to choose from, so standing your ground costs you. I've read Biko, I've watched Atlanta, and I still have no idea.

She always found the good and made a point of sharing it. When her flight was cancelled, a customer service agent got her onto another one, and she told the whole residency Signal group about it, by name. Thirty of us spent the evening cheering on Julie, in a call center somewhere, who will never know any of us were beaming our appreciation to her.

The protest organisers live with police violence as part of the work. You're trained to avoid a knee on your neck when you get arrested, but you also pick a great outfit for your arrest photo.

Everyone here was carrying pain, but still bringing light.

## The greenhouse

By the end of week two, a few of us took a conversation outside, to a table by the greenhouse. The others shared their stories first, and then I shared mine. It was the only time I did.

If I dress a certain way, I look white. If I dress according to my ancestry, I don’t. For that trip I’d only packed t-shirts and a baseball hat, so the first way was the only way people there saw me. Someone at the residency named it for me: white-passing.

My passport doesn’t pass. I know how border cops look at it, pointing at something they purposefully mispronounce. I’ve been down those hallways, to the small rooms with bad ventilation. People sat on rows of metal chairs facing a wall painted with a comically oversized government logo. Stone-faced mothers with toddlers playing on the floor.

On the street, I’ve been attacked by skinheads and had to fight for my life.

The mixed-race people in the house had a conversation of their own, about fractured roots: looking for your heritage and never finding it in one place. Our friend from the UN, whose parents had been displaced like mine, knew what was doing it. Whiteness.

She didn’t mean skin colour. She meant whiteness as erasure: corporate norms and consumerist culture spreading around the world and washing out what’s specific about anywhere, and anyone.

The search for roots is universal. I finally realised why my white friends do DNA tests and proudly tell me they’re 2.8% Irish or 1.9% Nordic. They’re feeling something that was washed out too.

This erasure is a Stephen King plot: something spreading through a town, cutting everyone off from each other and where they come from.

Stephen King's been writing about colonialism this whole time.

## Not everything

In week three, the journalist and I settled into a loop. I'd wake up with an idea, spend the morning researching and expanding it, then find him at some point during the day and see if it held water. Phone profiles died first: work profiles get checked, they're easy to spot, and they cause suspicion. What about a real sneakernet? A slow internet of USB drives moving around the region by car, with slow routing like [Fidonet](https://en.wikipedia.org/wiki/FidoNet)? It had been tried, and now police look for USB keys specifically at the checkpoints they use to control movement. They plug them in and if there's anything encrypted, the bus leaves without you. What about encrypted blobs, something PGP-like but not over email? Forget it. Something like that gets terrorism charges thrown at you. Most ideas ended there: been-there-done-that, or not worth it. But some of our ideas had a shred of something useful, and those became approaches worth a try, strategies that survive all the constraints at once, from network analysis to being detained and coerced into unlocking your phone. Even floods.

This whole time, a lawyer in the group had been deep in research. With us, they'd do that lawyer thing where they try to keep you out of trouble. The best defense is not to end up in court. That kinda thing. For fun, I kept bringing up Hunter S. Thompson's [activist lawyer](https://en.wikipedia.org/wiki/Oscar_Zeta_Acosta), someone who gets into trouble with you so they can get you out. But they were right. When the research was done, the lay of the land was clear. There are things governments and police do that wouldn’t stand up in court, but they know that doesn’t matter until your court date comes. Meanwhile, there are entire categories of ways to help journalists that steer far away from the state's ability to harass or coerce.

I couldn't stop thinking about another resident's project too. He'd applied with it but hadn't put it into the team formation exercise.

The morning after our group introductions, he'd started a conversation with me about where we were from, and put me onto [Langston Hughes' "Who's Passing For Who?"](https://genius.com/Langston-hughes-whos-passing-for-who-annotated)

So it was kinda fun that his pet project was helping workers form unions without disclosing to anyone, including each other, that they were doing it. He'd asked a few people, and they'd said the general version of the problem is considered impossible: the employer controls all the communication systems and all the records.

He wasn't a cryptographer but had come up with one of my favourite parts early on: make it a petition, not a vote. In a vote, an employer faking submissions fakes opposition and wins. In a petition, every fake signature works against whoever faked it.

If you know me, you won't be surprised to learn I thought ZK would solve it. Public and private inputs, a prover, a verifier. A [Semaphore](https://docs.semaphore.pse.dev/) Merkle-tree could handle membership proofs. What I hadn't spotted: Semaphore gives you anonymity within a group, but the employer holds all of the employee's information, so it can act as any employee.

I kept thinking, there must be something that made this case different from the general one, one little hook that made this not impossible in this specific case. The employer controls the mail servers, the directory, the devices. Not everything though: not personal phones, not the organisers' own Signal groups, not two people meeting in person.

That was enough to build on. The petition needs every employee to have one stable identifier, so nobody can sign twice. Normally you could hash something unique like an email address. But the employer just hashes the whole staff list, runs each one on the petition system, and knows who signed (and therefore who to fire). When this came up, we paraded over to Ying Tong, one of the organisers. She was in the kitchen, in the middle of cooking us all lunch. "We have this problem. Can I get you for five minutes?" She came over, sat down, drew us a little diagram, and explained [VOPRFs](https://www.rfc-editor.org/rfc/rfc9497.html). A VOPRF folds in a secret the employer doesn't have, and the server holding that secret never sees the email. I thought the name was hilarious, and that the idea deserved a pronounceable acronym, so I called them "VORPs". She kept correcting me so kindly and patiently it melted my heart a little each time. So I kept calling them VORPs.

Our first version was the standard pattern: publish the list of anonymised identifiers, so anyone can verify the count. Then a cryptographer pointed at the public list. The employer controls every mailbox, so it can submit as any employee and watch the list or the response. If it grows, that person hadn't signed. If it doesn't, they had. So an employer, with an idea of who signed, could verify their suspicion and deanonymise people.

Another problem was proving the results were valid, to third parties like courts. Someone suggested a blockchain, for immutability and proof, recording encrypted records as they were added, then revealing them all at the end. I suggested a massive zero-knowledge proof instead, over the tally itself: every signature valid, nobody counted twice, the total is N. And the list never leaves our hands.

For unionising, the NFC check-in from Little Homes turned out useful: a way for organisers to attest, in person, that someone was a real colleague, folded privately into their signature. It gave us another cryptographically provable path that the employer couldn't see or control.

## Encryption considered harmful

The last few days, we were all stressing about our presentations for Demo Day.

Then we got to Offline Place in Berlin, and Ying Tong and crew had made a huge effort to cook home-made food for everyone. The crowd that joined us were people from the Friday happy hours and the Casino, but now familiar faces instead of strangers. It was packed again, the front rows were people sat on the floor.

The journalist team presented "Encryption considered harmful". The main thread was simple. When you design cryptographic systems for these cases, the person in the room is exactly who you design for, which means key compromise, device compromise, network observation and metadata all matter. The person caught "in the room" isn't out of scope, they're in the crosshairs. As far as an interrogator is concerned, the more plausible your deniability, the more plausible your guilt.

Another team, [Garfield-Naruto](https://garfieldnaruto.com/), had come at it from the opposite direction. They hide messages in LLM slop: text that looks like nothing, instead of an encrypted blob that looks like something. They're candid that the prototype isn't ready for the most security-critical uses yet. I loved watching how much fun that team had the whole time, and this was the first time I saw a working demo.

I could finally see the other projects I hadn't had time to catch up on. A friend had come in with a great idea: a Gini Index but for privacy access. I wanted to be part of it, and tried to nudge it along but never managed more than cheering it on. By the end I could see how much had developed in his conversations with everyone. He explained how people on low incomes in some countries can only afford old Androids that won't get security updates. He talked about the cost of privacy beyond money, like time required and language barriers. It had really galvanised.

Another project was policy work on age verification, and how easily kids get around it. Seeing it presented in research photos and findings after all our little breakfast conversations, it was suddenly tangible. And a security project for national trains: "You were really working on this the whole time?" I asked her. "Yeah, that's why you didn't see me in the mornings. I was working in my room."

I was so tired, and still, I wanted to take this all in. Everything we'd done in this short time.

## Trading notes

My favourite moments were one-on-one conversations in some quiet corner of the house or the garden, lasting hours. Life, why we do what we do, the big problems. There's a melancholy in these friendships. What brought us together was our battles, and apart from those in the same cities or conference circles, we won't see each other again without real effort.

That closeness is what drove us to trade notes as travellers do: what's good, what's bad, what to avoid, what signposts to look out for.

When I got back home, that first show of hands stayed with me. About F-Droid. I'd arrived with a very technical, philosophical, and anti-Google view of my project. The [open letters](https://keepandroidopen.org/open-letter/) on this make the case top-down, in the abstract. So I started asking about the humanitarian impact of Google's developer verification by looking for real people with real stories. That pointed me to evidence about bigger numbers. Hundreds of thousands of people. Then millions. Then billions. I spent weeks on it, constantly pulled deeper as new questions opened up. And wrote it up here: [Google is taking what keeps them alive](https://voboda.com/blog/google-is-taking-what-keeps-them-alive/).

Engineering problems are objective: physics and math. That's what I'm used to. Most people I met at the residency are working against adversaries. Against other people. That's messier, and it brings an angry energy. Anger's useful though: with a constructive environment to direct it, it clears a path towards something better.

I'd never thought of myself as a policy person, but some residents encouraged me to dip into that world. I'm surprised how rare it is for the people designing policy to go and find the specific cases of who's affected. I applied for a few research grants, long shots for me, but one was accepted because of that approach.

I came looking for a way back to real people and real problems. I got here thanks to a house full of wonderful strangers, and the three organisers who bet their own time and money on us.
