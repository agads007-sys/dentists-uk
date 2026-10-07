# Google Review Outreach — United Kingdom

## NON-NEGOTIABLE

DRAFTS ONLY. NEVER SEND EMAILS AUTOMATICALLY.

This repository is only for dental practices physically located in United Kingdom. Never use prospects or exclusions from another country campaign.

The objective is speed, verification and natural writing. Do not search for perfect prospects. Use the first suitable prospects that can be verified quickly.

## Prospect eligibility

Every prospect must satisfy ALL of these conditions:

1. Dentist, orthodontist or dental practice only.
2. Physically located in United Kingdom.
3. Located in a genuine city or town. Small towns are allowed. Villages, hamlets, isolated rural locations and genuinely rural settlements without town character are excluded. If this cannot be verified confidently, skip the prospect.
4. Current Google or Google Maps review count is between 2 and 25 inclusive.
5. The exact current review count must be verified. Never estimate it and never rely on an obviously stale count.
6. An appropriate contact email must be officially published by the practice or its official organisation. Never guess an address.
7. Before selection, both the practice name and email address must be checked against the campaign exclusion log and the in-memory exclusions for the current run.

Among readily available eligible prospects, prefer lower review counts. Do not spend extra time hunting for a 3-review practice when an otherwise good 8-review practice is already verified.

Visible marketing activity is only a secondary prioritisation signal. If active advertising, promotional pages, cosmetic treatment marketing, SEO/local landing pages, active social media or strong booking calls-to-action are obvious during normal verification, that can favour a prospect. Do not perform separate marketing research just to score prospects. Never invent marketing activity.

If any mandatory detail is difficult to verify quickly, skip the candidate and move on.

## Persistent exclusions

The only persistent deduplication file for normal runs is:

`data/exclusions-log.txt`

Each successful drafted prospect is stored as:

`email@example.com | Practice Name`

At the beginning of a run, read this file once and build two in-memory sets from it:

- normalised email addresses
- normalised practice names

As soon as a prospect is selected, immediately add both its email and practice name to the in-memory sets so it cannot appear again during the same run.

Do not load exclusion files from another repository or another country.

Do not add city, review count, marketing notes or other research fields to the exclusion log. Keep the hot dedupe data minimal.

## Batch workflow

Work in batches of 5 successful drafts.

For each batch:

1. Research only enough prospects to obtain 5 valid candidates.
2. Verify eligibility and deduplicate before selection.
3. Immediately add each selected practice name and email to the in-memory dedupe sets.
4. Create 5 Gmail drafts.
5. Confirm each draft was actually created.
6. Append only successful draft recipients to `data/exclusions-log.txt`.
7. Commit the updated exclusion log.
8. Continue directly to the next batch.

Never log a prospect whose Gmail draft failed.

For a standard run, continue until exactly 25 NEW successful drafts have been created unless a genuine technical limitation prevents completion.

## Gmail distribution

Read `data/gmail_accounts.txt` once at the beginning of the run.

Spread new drafts across all 10 available Gmail accounts as evenly as practical. Do not duplicate a prospect to fill an account.

DRAFTS ONLY. NEVER SEND.

## Mandatory sales skeleton

Every email must preserve this exact logical order. Natural wording may vary, but the reasoning and order must not.

1. Michael found the dental practice while looking at dentists on Google in the area.
2. Mention the practice's exact CURRENT VERIFIED Google review count.
3. Say that Michael also looked at other nearby dental practices and there is clearly room to build the practice's review count. Do not quote competitor numbers unless separately verified.
4. Explain why this matters to patients comparing several dentists on Google.
5. Explain that reviews can also contribute to local visibility on Google. Never promise rankings.
6. Naturally say that this is why Michael is getting in touch.
7. Introduce a very simple system for asking real patients for Google reviews.
8. After an appointment, the practice enters the patient's mobile number.
9. The patient receives an SMS with a direct link to the practice's Google profile and can leave a review immediately.
10. Emphasise that this requires almost no work from the practice.
11. State with genuine conviction that consistent use can make a meaningful difference to the practice's Google presence over time.
12. Michael sets everything up and handles the rest.
13. State the exact price: **£34 per month**.
14. State that there is no long-term commitment.
15. End with a short, natural question offering to show how it works.
16. Sign exactly:

Best,
Michael Berg

Never reorder the pitch into a different sales argument.

Never promise a specific Google position, number of patients, number of reviews or revenue increase.

## Voice

Write in natural contemporary British English.

The email should sound like Michael personally noticed the practice and wrote a short, thoughtful message himself.

Direct, conversational and confident.
Professional, but not formal.
Human, but not artificially casual.
No agency voice.
No brochure language.
No hype.
No fake compliments.
No invented personalisation.
No headings or bullet points inside the email.
Use short natural paragraphs and simple punctuation.
Avoid em dashes, semicolons and stylistic colons.

Use British spelling and ordinary UK dental-practice terminology.
Prefer "dental practice" or "practice". Never call it a "dental office".
Use "mobile number", not "cell number".
Keep the tone understated and matter-of-fact rather than enthusiastic or Americanised.

Do not force local slang or stereotypes.

### Phrases and styles to avoid

Do not write phrases such as:

- I hope this email finds you well
- I wanted to reach out
- I am reaching out
- enhance your online presence
- leverage
- streamline
- seamless solution
- innovative solution
- unlock your potential
- boost your business
- drive growth
- game changer
- take your practice to the next level
- I'd love to connect
- touch base
- circle back

Prefer concrete language.

Bad:
"Your practice has a tremendous opportunity to significantly enhance its online reputation."

Good:
"There's still plenty of room to build your review count."

Bad:
"Our innovative solution streamlines the review-generation journey."

Good:
"After an appointment, you enter the patient's mobile number and they get a text with the link to your Google profile."

## Natural variation

A batch must not contain five near-identical emails.

Vary naturally:
- the opening
- the way the review gap is described
- the patient-comparison explanation
- the local-Google explanation
- the simple SMS explanation
- the low-effort sentence
- the conviction sentence
- the CTA

Do not create variation by inventing facts.

## Canonical example

This is a tone and structure reference, not text to copy repeatedly.

Subject: Quick question about your Google reviews

Hi,

I came across your practice while looking at dentists in your area on Google and noticed you've currently got 8 reviews.

I had a look at a few other practices nearby as well. There's still quite a bit of room to build that number up, and it's something patients notice when they're comparing dentists.

When someone is choosing a new dentist, they'll often look through several Google profiles before deciding. A practice with more genuine reviews can feel more established and reassuring at a glance. Reviews can also play a part in local visibility on Google.

That's why I'm getting in touch.

I've put together a very simple system that helps dental practices ask more of their real patients for reviews. After an appointment, you enter the patient's mobile number. They get an SMS with a direct link to your Google profile and can leave a review straight away.

There's almost nothing for you to manage. Used consistently, I'm convinced it can make a real difference to how your practice looks on Google over time.

I set everything up and handle the rest. It's £34 per month with no long-term commitment.

Want me to show you quickly how it works?

Best,
Michael Berg

## Final check before creating each draft

Confirm:

- Correct country
- Genuine city or town
- Dentist / orthodontist / dental practice only
- Current Google review count between 2 and 25 inclusive
- Exact count verified
- Officially published contact email
- Name and email not excluded
- Same mandatory sales skeleton and order
- Natural British English
- Exact country price
- No long-term commitment
- Exact Michael Berg signature
- Draft only, never send
