# Dinari

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

Dinari provides tokenized US stocks and ETFs (dShares) backed 1:1 by real securities, giving businesses an API to offer global customers regulated access to over a hundred equities and index tokens across 85+ jurisdictions. The Dinari Enterprise API covers entity onboarding and KYC/KYB, brokerage account management, market data (prices, quotes, splits, dividends, news), managed and on-chain (EIP-155 permit) order requests, order fulfillment, blockchain wallet connection, token transfers, withdrawals, and a USD+ stablecoin for dividend payments. dShares settle on-chain across Arbitrum One, HyperEVM, and Avalanche C-Chain. Surfaced as a portfolio company of 500 Global and Version One Ventures and enriched into the API Evangelist network.

**Areas:** Company · Tokenized Securities · Stocks · ETFs · Brokerage · Market Data · Blockchain · Stablecoins · Fintech · KYC · Order · Wallets

## Dinari on APIs.io

Everything profiled for Dinari is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/dinari/](https://apis.io/providers/dinari/)** — or go straight to one of the APIs or properties below.

### APIs (10)

- [Dinari Accounts API](https://apis.io/apis/dinari/dinari-accounts-api/) — **`Accounts` represent the financial accounts of an `Entity`.** `Orders`, dividends, and other transactions are associated with an `Account`.
- [Dinari Corporate Actions API](https://apis.io/apis/dinari/dinari-corporate-actions-api/) — **Corporate actions are events that affect the ownership of a `Stock`.** Corporate actions include dividends and stock splits.
- [Dinari Entities API](https://apis.io/apis/dinari/dinari-entities-api/) — **`Entities` represent a business or organization that uses the API, and their customers.** Dinari Partners are represented as an organization `Entity` in…
- [Dinari KYC API](https://apis.io/apis/dinari/dinari-kyc-api/) — **KYC (Know Your Customer) is a process of verifying the identity of customer `Entities`.** KYC is required for all customer `Entities` that transact on…
- [Dinari Managed Orders API](https://apis.io/apis/dinari/dinari-managed-orders-api/) — **Managed `Orders` represent the buying and selling of assets using a Dinari-managed `Wallet`.** Similar to Proxied `Orders`, placing a managed `Order`…
- [Dinari Market Data API](https://apis.io/apis/dinari/dinari-market-data-api/) — **Dinari provides basic market data for `Stocks` and `Alloys` that are available to transact on.** This data is provided on a best-effort basis and we…
- [Dinari Order Requests API](https://apis.io/apis/dinari/dinari-order-requests-api/) — **`Order Requests` represent requests for Dinari to create `Orders` on behalf of an `Account`.** `Order Requests` are created when placing **proxied…
- [Dinari Orders API](https://apis.io/apis/dinari/dinari-orders-api/) — **`Orders` represent the buying and selling of assets under an `Account`.** For `Accounts` using self-custodied `Wallets`, `Orders` are created and…
- [Dinari Wallets API](https://apis.io/apis/dinari/dinari-wallets-api/) — **`Wallets` represent the blockchain wallet that holds the assets of an `Account`.** An `Account` may be connected to a single `Wallet`. Individual…
- [Dinari Withdrawals API](https://apis.io/apis/dinari/dinari-withdrawals-api/) — **`Withdrawals` represent the transfer of stablecoins from an `Account` connected to a managed `Wallet` to another `Account` that is owned by the…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Arazzo workflows (2)

Multi-step workflows that chain operations into a business task.

- [Connect a wallet and fund an account](https://apis.io/arazzos/dinari/dinari-connect-wallet-and-fund/)
- [Onboard a customer and place a dShare order](https://apis.io/arazzos/dinari/dinari-onboard-and-trade/)

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Dinari Streaming (WebSocket) API](https://apis.io/asyncapis/dinari/dinari-streaming-asyncapi/)

#### Event channels (1)

Individual events and webhooks the provider emits.

- [/](https://apis.io/channels/dinari/connection/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [dinari](https://apis.io/servers/dinari/dinari/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Dinari Agentic Access](https://apis.io/agentic-access/dinari/dinari-agentic-access/)

#### Collections (20)

Postman and Open Collection request collections.

- [Dinari Enterprise Accounts API](https://apis.io/collections/dinari/open-dinari-accounts-api/)
- [Dinari Enterprise Accounts Corporate Actions API](https://apis.io/collections/dinari/open-dinari-corporate-actions-api/)
- [Dinari Enterprise Accounts Entities API](https://apis.io/collections/dinari/open-dinari-entities-api/)
- [Dinari Enterprise Accounts KYC API](https://apis.io/collections/dinari/open-dinari-kyc-api/)
- [Dinari Enterprise Accounts Managed Orders API](https://apis.io/collections/dinari/open-dinari-managed-orders-api/)
- [Dinari Enterprise Accounts Market Data API](https://apis.io/collections/dinari/open-dinari-market-data-api/)
- [Dinari Enterprise Accounts Order Requests API](https://apis.io/collections/dinari/open-dinari-order-requests-api/)
- [Dinari Enterprise Accounts Orders API](https://apis.io/collections/dinari/open-dinari-orders-api/)
- [Dinari Enterprise Accounts Wallets API](https://apis.io/collections/dinari/open-dinari-wallets-api/)
- [Dinari Enterprise Accounts Withdrawals API](https://apis.io/collections/dinari/open-dinari-withdrawals-api/)
- [Dinari Enterprise Accounts API](https://apis.io/collections/dinari/postman-dinari-accounts-api/)
- [Dinari Enterprise Accounts Corporate Actions API](https://apis.io/collections/dinari/postman-dinari-corporate-actions-api/)
- [Dinari Enterprise Accounts Entities API](https://apis.io/collections/dinari/postman-dinari-entities-api/)
- [Dinari Enterprise Accounts KYC API](https://apis.io/collections/dinari/postman-dinari-kyc-api/)
- [Dinari Enterprise Accounts Managed Orders API](https://apis.io/collections/dinari/postman-dinari-managed-orders-api/)
- [Dinari Enterprise Accounts Market Data API](https://apis.io/collections/dinari/postman-dinari-market-data-api/)
- [Dinari Enterprise Accounts Order Requests API](https://apis.io/collections/dinari/postman-dinari-order-requests-api/)
- [Dinari Enterprise Accounts Orders API](https://apis.io/collections/dinari/postman-dinari-orders-api/)
- [Dinari Enterprise Accounts Wallets API](https://apis.io/collections/dinari/postman-dinari-wallets-api/)
- [Dinari Enterprise Accounts Withdrawals API](https://apis.io/collections/dinari/postman-dinari-withdrawals-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Dinari Openapi Overlay](https://apis.io/overlays/dinari/dinari-openapi-overlay/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Dinari Authentication](https://apis.io/security/dinari/dinari-authentication/)
- [Dinari Domain Security](https://apis.io/security/dinari/dinari-domain-security/)
- [Dinari Vulnerability Disclosure](https://apis.io/security/dinari/dinari-vulnerability-disclosure/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://dinari.com)
- [Documentation](https://docs.dinari.com)
- [Getting started](https://docs.dinari.com/docs/quickstart)
- [API reference](https://docs.dinari.com/reference)
- [Pricing](https://docs.dinari.com/docs/fees)
- [Sign up](https://partners.dinari.com)
- [Support](https://dinari.com/contact-us)
- [Changelog](https://docs.dinari.com/changelog)
- [Blog](https://dinari.com/blog)
- [Security](https://docs.dinari.com/docs/security)
- [Terms of service](https://dinari.com/terms)
- [Privacy policy](https://dinari.com/privacy)
- [GitHub](https://github.com/dinaricrypto)
- [Status](https://status.dinari.com)

## API Evangelist rating

**Kin Score 44.0** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 60.6 |
| Contract governance | 4.5 |
| Operational transparency | 39.5 |
| Developer ergonomics | 50.6 |
| Access clarity | 26.3 |

**Agent readiness 29.0** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | — |
| Rate Limit Signal | — |
| Event Surface Described | derived (partial credit) |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | partial |
| Operation Distinctiveness | distinct |

**Regulatory alignment 28.7** — Securities & Market Data

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/dinari/](https://apis.io/providers/dinari/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Dinari: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/dinari/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
