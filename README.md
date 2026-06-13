# ISBNdb

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
