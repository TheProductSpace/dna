---
title: Bun protocol
prev_section: communication.html
next_section: dashboard.html
---

The Bun Protocol
================

The Bun protocol is a lightweight, decentralized request routing protocol. It is designed to be the simplest possible way to handle requests that are shared by a distributed group of people. We use it mostly to handle incoming client requests.

> We introduced this to Product Space after seeing how effective it was at Nomad8, having a lightweight sales process.

The metaphor
------------

![Sia's Home baked Kanelbulle! Yum!](../assets/Bun.jpg "Sia's Home baked Kanelbulle! Yum!")

When a bun (= issue or request) comes in it is warm, juicy and soft. If it sits around for a day it will get cold. If it sits around several days it will become dry and hard. You can warm up an old bun in the microwave oven as long as it hasn't become too dry.

So, a bun should be eaten fairly quickly or thrown away. No use stuffing it in a box. If you can't eat it yourself, offer it to someone else - before it gets cold, dry and hard!

Sample buns
-----------

-   You get an email "Hi, we want a TDD course at company X. What will it cost and when can you come?". Now you have a bun!
-   You meet someone at conference who says "I want to join your company!". Now you have a bun!

How the protocol works
----------------------

A bun is born when someone asks you for something and you decide that "hey, this is a bun". Typically through email, but sometimes a phone call or a conference mingle.

**A bun always has an owner** - the person who received the bun. Or more specifically, the person responsible for the communication channel through which the bun appeared. For example, you are of course responsible for any emails sent directly to you.

**When you have a bun, you are responsible for taking care of it before it gets too dry!** Preferably within 1 working day, definitely within 2.

You have 3 options:

-   **Eat it yourself.** For example "Sure, I can come and do a TDD course at your company". The bun is now consumed, i.e. it has found a home and will not be routed anywhere.
-   **Give it to somebody else.** For example to a colleague who is more suitable than you, or another company. If you don't know exactly who should take it, email a broadcast to your colleagues or trusted partners: "Hi folks, does anybody want to take this bun?". Note that the bun is still yours until someone else takes it! Allow a day so that your colleagues have time to react, but if that takes more than a couple of days you need to keep the bun warm (for example tell the customer that you are searching for someone who can help). So you can't push the bun to someone, you can only offer it. The receiver has to pull the bun from you.
-   **Throw it away.** For example someone emails me "Can you come and teach a Cobol course?". I answer "No". Or I answer "No, we don't do Cobol courses, but I recommend you speak to Mr CobolGeek". That still counts as throwing away the bun, since I let it go and won't follow it up. Someone else might take it out of my garbage, but I don't need to know or care if that happens :o)

The one thing you should NOT do is just let the bun sit and dry. Better to explicitly throw it away in that case (i.e. tell the sender that we can't help).

So initially a buns appears through a "push" protocol, i.e. the initial recipient gets the bun whether he wants to or not. After that, however, everything is "pull"-based.

Summary of the rules
--------------------

-   **As receiver of a bun you are responsible** until it is eaten by you, taken by someone else, or thrown away. If several people are interested, sync with them.
-   **A bun should not get more than 1-2 days old** without being eaten by somebody, thrown away, or reheated (by talking to the customer/sender).
-   **You can't push a bun onto someone else, they have to pull**. The bun is yours until someone else explicitly takes it (for example by saying "I'll take the bun"). You can of course recommend (or even try to convince) someone else to take it from you. This goes both ways - if someone offers you a bun, you don't have to respond if you aren't interested.
-   When in doubt:
    -   Broadcast an email to everybody who might be interested or involved in this bun
    -   or send the bun to "upwards" or to a central person such the board or our business developer. For example if the bun seems to be strategic and might lead to a big dinner.
-   **When broadcasting to find interested bun-takers, give your colleagues one day** to indicate interest in the bun. Don't just let the first one that answers have the bun. There might be more interested. Letting the first one that answers having the bun leads to race conditions and might cause tension between colleagues.

We don't always succeed in following these rules, especially the 1-2 day age limit. But we really try our best, and we're at least aware of when we fail.




Why it works
------------

We've used the protocol for many years and it works really well. Here are some reasons:

-   **Nice metaphor** - buns are good :o)
-   **Simple**, anybody can learn it in 5 minutes.
-   **Can be extended** as needed. New rules can be added, tool support can be added. But don't. Keep it simple and add stuff only if you really, really need it.
-   **Doesn't require any specific artifacts** or documents that need to be maintained (unless you add that layer yourself...).
-   **Decentralized** - uses "wisdom of the crowds" to ensure that buns reach the right destination in the shortest possible time with the least possible effort. People such as our business developer can focus on important stuff and not become a bottleneck for all kinds of trivial requests.
-   It **scales**. We haven't tried in a bigger group than 25-ish, but it should scale to much higher.
-   **Customer focused** - customers normally get a response within a reasonable time.
-   It **promotes trust and collaboration**, and avoids bottlenecks and command & control
-   It is **Lean** - we minimize work in progress and maximize flow by ensuring that buns are handled quickly and don't pile up in queues. We minimize waste and stress in the system by discarding sour buns quickly.
-   We **still have the option to centralize & escalate** on a case-by-case basis. If someone bumps into a bun that needs to be escalated to some central authority then that can be done immediately.

FAQ
---

### Does this work for all types of requests?

We don't know. But it has worked well enough so far, and we haven't come up with any kind of request where it wouldn't work.

### What if several people want the same bun?

If several people are interested in the same bun, they talk to each other and sort it out.

Strictly speaking, the first person to take the bun has it, so in theory we have a race condition. In practice, however, when a potential conflict arises the involved people talk to each other (by phone or email) and decide on who should take the bun, based on who can serve the client best, who needs the bun most, and other relevant factors.

So being the bun holder doesn't really mean "this is MY client", it means more like "I'll make sure this gets taken care of!" - (by me or whoever else is most suitable).

We've used this protocol for years and we very rarely have serious conflicts around bun routing. We get **potential** conflicts regularly (typically 2-3 people offering to take the same bun), but it is almost always resolved in a gentlemanly fashion, using good ol' communication and trust between the interested parties. I help you today, you help me tomorrow, and in the long it run it more or less evens out.

The [conflict handling process](conflict-handling.html) should help solve the edge cases.

### What if it is a business-critical request? Shouldn't some central authority handle it?

The closest thing we have to a central authority is the [board](board.html), and our business developer. If one of them received the request then, well, they already have it.

What if you received the request? Well, do you think it is business critical and should be handled by the business developer? In that case get in touch and ask her to take it from you. If you don't know what to do, broadcast it to all Product Spaceers (or even external partners that have bought into this protocol) and ask who wants to take it.

But don't forget - the bun is still yours until someone else explicitly takes it from you!

### But what if I accidentally throw away an important bun!?

Example: Customer X calls you and says they needs agile coaching. You respond "Sorry, but I can't help right now." But you didn't know that your colleague Hans is available and could have taken this client, and you didn't know that Customer X was an important strategic customer. Ouch.

You shouldn't have thrown away that bun. Would have been better to email your colleagues and at least given somebody a chance to take the bun before you threw it away. Live & learn!

So, yes, you might accidentally throw away an important bun. But that doesn't mean you have to :o)

### Why not forbid people to throw away buns?

Sure, we could do that if we were very scared of losing important customers. But fear comes with a price tag. Sometimes we receive distinctly sour buns. "Can you help my dad install Windows on his PC". Or "MAKE MONEY FAST $$$$$" :o)

What if **all** sour buns received by **everyone** were routed to the business developer or the whole team? That would be a horrible waste of time.

There is great strength in having "waste filters" at all inputs channels to the organization, so we can focus on the important buns rather than waste time on obviously sour ones.

Sure there is a risk that we might accidentally filter out some tasty buns, but that's OK. Our guiding principle is "ask for forgiveness rather than permission", and learn as we go.

### What about traceability?

We visualise our buns in the Product Space customer funnel Trello board.


### How do we avoid buns falling through the cracks

Be very clear in your communication. Short, clear phrases like:

-   "Who will take this bun?"
-   "I'm taking the bun!"
-   "I will throw this bun away if nobody takes it by Tuesday"


### What are the potential disadvantages of the bun protocol?

-   Requires discipline and trust from everyone involved. But we kinda want that anyway...
-   No built-in traceability and visibility. We can't easily see which active buns are in our system unless we add a visibility layer.
-   Slightly silly metaphor. Not sure that's a disadvantage though :o)