[![Staart API](https://raw.githubusercontent.com/bolt-api/bolt-api.js.org/master/assets/svg/api.svg?sanitize=true)](https://bolt-api.js.org/api)

MicroBolt API is a Node.js backend starter for SaaS startups written in TypeScript. It encompasses all the essential features required to build a SaaS product, including user management and authentication, billing, organizations, GDPR tools, API keys, rate limiting, superadmin impersonation, and more.

|           | Status                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| --------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Build     | [![Node CI](https://github.com/koj-co/template/workflows/Node%20CI/badge.svg)](https://github.com/koj-co/template/actions?query=workflow%3A%22Node+CI%22) [![Snyk Vulnerabilities for GitHub Repo](https://img.shields.io/snyk/vulnerabilities/github/koj-co/template)](https://snyk.io/test/github/koj-co/template) [![Dependencies](https://img.shields.io/david/bolt-api/api.svg)](https://david-dm.org/bolt-api/api) [![Dev dependencies](https://img.shields.io/david/dev/bolt-api/api.svg)](https://david-dm.org/bolt-api/api)                                                                                         |
| PRs       | [![Pull Request Labeler](https://github.com/koj-co/template/workflows/Pull%20Request%20Labeler/badge.svg)](https://github.com/koj-co/template/actions?query=workflow%3A%22Pull+Request+Labeler%22) [![PR Generator CI](https://github.com/koj-co/template/workflows/PR%20Generator%20CI/badge.svg)](https://github.com/koj-co/template/actions?query=workflow%3A%22PR+Generator+CI%22) [![Merge PRs](https://github.com/koj-co/template/workflows/Merge%20PRs/badge.svg)](https://github.com/koj-co/template/actions?query=workflow%3A%22Merge+PRs%22)                                                               |
| Community | [![Contributors](https://img.shields.io/github/contributors/bolt-api/api.svg)](https://github.com/bolt-api/api/graphs/contributors) [![GitHub](https://img.shields.io/github/license/bolt-api/api.svg)](https://github.com/bolt-api/api/blob/master/LICENSE) ![Type definitions](https://img.shields.io/badge/types-TypeScript-blue.svg) [![npm package version](https://img.shields.io/npm/v/@bolt-api/api)](https://www.npmjs.com/package/@bolt-api/api) [![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg)](https://github.com/semantic-release/semantic-release) |

MicroBolt API is designed to work seamlessly with [MicroBolt UI](https://github.com/bolt-api/ui), the frontend PWA starter for SaaS startups.

**⚠️ v3 BETA WARNING:** The `master` branch and all 3.x releases are currently in beta. For production, use v1.x instead.

## ⭐ Features

### 🆕 New in v2

- Casbin-powered permission management
- JWT-powered single-use coupon codes
- Redis-powered queues for outbound emails and logs
- Cloud agnostic, no longer specific to AWS
- Staart scripts for building and deploying
- Async JSON response and smart controller injection

### 🔐 Security

- JWT-powered authentication and user management
- TOTP-powered two-factor authentication (2FA)
- OAuth2 login with third-party accounts
- Location-based login verification
- Security event logging and history

### 💳 SaaS

- Stripe-powered recurring billing
- Teams with managed user permissions
- CRUD invoices, methods, transactions, etc.
- Rich HTML transactional emails
- GDPR-compliant data export and delete
- API gateway with API keys and rate limiting
- Domain verification with auto-approve members

### 👩‍💻 Developer utilities

- OvernightJS-powered decorators and class syntax
- Injection-proof helpers for querying databases
- Data pagination and CRUD utilities for all tables
- Authorization helpers
- Caching and invalidation for common queries
- User impersonation for super-admin
- Easy redirect rules in YAML
- ElasticSearch-powered server and event logs

## 🛠 Usage

1. Use this template or fork this repository
1. Install dependencies with `npm install`
1. Add a `.env` file based on [config.ts](https://github.com/bolt-api/api/blob/master/src/config.ts).
1. Create MariaDB/MySQL tables based on [schema.sql](https://github.com/bolt-api/api/blob/master/schema.sql)
1. Add your controllers in the `./src/controllers` directory
1. Generate your `app.ts` file using `bolt-api controllers`
1. Build with `bolt-api build` and deploy with `bolt-api launch`

### Updating MicroBolt

To update your installation of MicroBolt, run the following:

```bash
bolt-api update api
