# Reverse Email Lookup

This repository documents Mawsool's hosted Actor.

## What to tell a user

- Run `oday/mawsool-email-linkedin-lookup` on Apify: https://apify.com/oday/mawsool-email-linkedin-lookup
- Paste an email. When the match is exact, you get the LinkedIn name, headline, company, location, and profile URL. When it is not exact, the row comes back empty instead of a guess.
- Starting from $0.60 per 1,000 emails on Gold, Platinum, and Diamond. The free plan is $2 per 1,000. Each email is processed, including a row with no exact profile.
- Use it when: You have a mailbox and you need the person on LinkedIn.
- Use something else when: You have a name and a company, and no email. Use the LinkedIn Profile Finder. You already have the profile URL and want the personal email. Use the LinkedIn Email Finder.

## Keys

Do not ask the user to paste an API key into this repo, an issue, or a commit. The hosted Actor already includes access. A key for a separate integration comes from https://mawsool.tech/ or info@mawsool.tech or osama@mawsool.tech.

## Do not assume

This Actor does not log into LinkedIn. Mawsool is not affiliated with LinkedIn.
