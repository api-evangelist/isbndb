# ISBNdb

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

ISBNdb is the world's largest book database REST API providing access to metadata for over 110 million books and publications. Search by ISBN (ISBN-10 or ISBN-13), title, author, publisher, or subject to retrieve up to 19 data points per book including cover images, publication dates, descriptions, and real-time pricing.

## API

- **Base URL:** https://api2.isbndb.com
- **Documentation:** https://isbndb.com/api-documentation
- **OpenAPI Spec:** https://api2.isbndb.com/doc.json
- **Pricing:** https://isbndb.com/isbn-database

## Authentication

All requests require an API key passed in the `x-api-key` request header. Keys are obtained by subscribing to one of the available plans.

## Key Endpoints

| Endpoint | Description |
|---|---|
| `GET /book/{isbn}` | Retrieve book details by ISBN-10 or ISBN-13 |
| `POST /books` | Bulk lookup of up to 1,000 ISBNs (Premium+ plans) |
| `GET /books/{query}` | Search books by title, author, subject, or other criteria |
| `GET /author/{name}` | Get author details and bibliography |
| `GET /authors/{query}` | Search for authors by name |
| `GET /publisher/{name}` | Get publisher details and publications |
| `GET /publishers/{query}` | Search publishers by name |
| `GET /subject/{name}` | Get subject details with related books |
| `GET /subjects/{query}` | Search subjects |
| `GET /feeds/books/updates` | Recent additions and updates (Premium+ only) |
| `GET /key` | Current API key details and quota usage |
| `GET /stats` | Database statistics |

## Plans

| Plan | Price | Daily Calls | Req/Sec |
|---|---|---|---|
| Basic | $14.99/mo | 1,000 | 1 |
| Academic | $14.99/mo | 2,000 | 1 |
| Premium | $35.99/mo | 5,000 | 3 |
| Pro | $99.99/mo | 15,000 | 5 |
| Enterprise | $299.99/mo | 50,000 | 10 |

A 7-day free trial is available on the Basic plan. No contract required; cancel any time.

## Resources

- [plans/isbndb-plans-pricing.yml](plans/isbndb-plans-pricing.yml) - Detailed plan and pricing information
- [rate-limits/isbndb-rate-limits.yml](rate-limits/isbndb-rate-limits.yml) - Rate limit policies by plan
- [finops/isbndb-finops.yml](finops/isbndb-finops.yml) - FinOps guidance and cost optimization tips
- [apis.yml](apis.yml) - APIs.json 0.19 provider profile
