# Cathay Circle: Family Pool Prototype

Prototype for the Cathay Pacific Hackathon 2026, Student Track (Lifestyle).
Challenge: *What can we do in terms of membership proposition which help the family and students that travel with us?*

**Live demo:** https://cloveeng.github.io/cathay_family_pool/

> This is a student concept prototype. It is not an official Cathay Pacific product and is not connected to any Cathay system. All names, balances and fares are made-up sample data.

## The idea

Members only engage with Cathay when they book a flight. Cathay Circle gives a family one shared Asia Miles pool and a reason to come back every week:

- **Family pool:** up to 8 named members add miles to one shared goal (for example, Tokyo for four). Pooled miles can only be used for trips by named members.
- **Student membership:** verified students get a flat 10% fare, and perks grow in three tiers: Starter (+1 bag, 1 free change, welcome miles), Regular after 4 trips (+10 kg, free seat choice, 1.25× miles) and Frequent after 8 trips (+15 kg and sports gear, unlimited changes, 1.5× miles and lounge passes).
- **Weekly streak and badges:** adding to the pool in any week keeps the family streak going, and four weeks in a row completes it. The streak is recognition only and pays no miles.

## What the prototype shows

The page shows two phones side by side: the organiser (Grace) and a student (Ethan).

- Add miles to the pool and watch the goal and streak move.
- Redeem a trip. Requests above the spend limit go to the organiser for approval, and trips above 25,000 miles ask for a passkey (simulated).
- Book a student trip to see the 10% fare and the next perk unlock.
- Invite a new member with a code and see the 7-day cooling-off.
- Use the buttons under the phones: **Reset demo**, **show a non-member's view**, **Cathay's view** and **Judge phone (QR)**.

### Judge phone (optional live link)

Clicking **Judge phone (QR)** shows a QR code. Scanning it opens a single full-screen student phone. Whatever the person taps on it happens on the organiser screen too, so a trip request can be approved live.

This needs an internet connection. It uses the PeerJS library, loaded from a public CDN only when this button is used, and a free public connection service. Only the fake demo state is sent. If the connection fails, the rest of the prototype works as normal.

## Safeguards (design intent)

- A new member waits 7 days before redeeming (cooling-off).
- A passkey is required above 25,000 miles.
- Households can redeem up to 150,000 miles a day.
- Each member can add up to 50,000 miles a month.
- A member who leaves takes their remaining share and cannot rejoin for 12 months.
- Families share the goal, not their personal data. Children under 18 join by organiser invite, and students are verified by a third party.

These are design ideas for the hackathon. They have not been reviewed by Cathay legal or checked against data-protection rules.

## Running it

It is a single HTML file with no build step.

1. Download `index.html`.
2. Open it in a browser.

The only part that needs the internet is the optional Judge phone link.

## Tech notes

- Plain HTML, CSS and JavaScript in one file, with the Inter font embedded.
- No accounts, no cookies, no stored personal data. State lives in the page and resets when you reload.
- Colours follow the Cathay palette. The Cathay logo is not used.

## Team

Clovee, Karissa, Clement, Theodora and Katherine.
