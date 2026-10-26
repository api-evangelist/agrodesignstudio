# AgroDesign Studios

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

**AgroDesign Studios** (株式会社アグロデザイン・スタジオ) is a Japanese structural-biology startup founded
30 March 2018 by CEO Yuki Nishigaya, based at the University of Tokyo Kashiwa-II campus in Kashiwa,
Chiba. It applies protein and nucleic-acid 3D structure information to the discovery of
molecular-targeted, environmentally safer crop-protection chemicals.

Its commercial surface is **contract research and physical goods, not software**. The **AgroBox®**
brand sells X-ray crystallography, cryo-EM, fragment screening and structure-based drug design
(SBDD) engagements; **AgroDesign.SHOP** sells lab-automation robot arms (as a UFACTORY xArm
authorized reseller), Arabidopsis cultivation kits, seeds and experimental materials.

### What this profile found

- **No first-party API contract.** No OpenAPI, GraphQL SDL, AsyncAPI, gRPC or WSDL was found on any
  host the company controls, after probing the corporate site, both Wix-hosted service sites, and
  every API host root.
- **Two live, unauthenticated remote MCP endpoints** — `https://www.agrobox.jp/_api/mcp` and
  `https://www.agrodesign.shop/_api/mcp`. Both answered `initialize` and `tools/list` with HTTP 200
  and returned 9 tools each. These are **Wix "Site Visitor Assistant" servers — platform-authored by
  the Wix site builder, not written by AgroDesign Studios.** They are real agent surfaces on hosts
  the company controls, but they describe the *website*, not the science service.
- **Two verbatim `llms.txt` files**, also Wix-generated, saved under `llms/`.
- **No `/.well-known` document of any kind.** The Wix edge returns HTTP 400 for every
  `/.well-known/*` path on both Wix hosts; the corporate site returns 404. No agent card, no
  `security.txt`, no OAuth metadata.
- **No packages.** PyPI `agrodesign` and the GitHub org `Agrobox-backend` were both examined and
  **rejected on ownership** — see `packages/agrodesignstudio-packages.yml`.
- **No idempotency and no reversibility** on a surface that can start a purchase — see
  `conventions/agrodesignstudio-conventions.yml`.

### Links

- Company: https://www.agrodesign.co.jp/
- AgroBox service site: https://www.agrobox.jp/
- AgroDesign.SHOP: https://www.agrodesign.shop/
- LinkedIn: https://jp.linkedin.com/company/agrodesignstudios
- Secondary-market listing (harvest source): https://equityzen.com/company/agrodesignstudio
