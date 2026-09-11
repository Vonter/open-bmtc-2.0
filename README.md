# Namma BMTC 2.0 OpenAPI

Unofficial reference for APIs and functionality used by Namma BMTC 2.0,
covering service discovery, live tracking, trip planning, ticketing, passes,
wallets, payments and ONDC mobility.

The reference was reverse-engineered from the [Namma BMTC 2.0 Android app](https://play.google.com/store/apps/details?id=com.bmtc.bmtcavls.two)
(`com.bmtc.bmtcavls.two`).

Operations in **Public**, **Other** and **Authentication** carry `security: []` and
reach the server with no credentials. **Public** contains the primary transit APIs,
followed by lower-priority public utilities in **Other** and the login flow in
**Authentication**. **Authenticated** operations require the `userId` and
`ACCESS_TOKEN` headers.

Response examples in the OpenAPI document come from captured live traffic. Request
examples come from captured traffic or the exact request serialization recovered from
the production client. Public operations include error or empty responses when a
feature is not available; large responses are shortened to representative
observed records.

Browse the reference at **[nimmbus.pages.dev](https://nimmbus.pages.dev)**.

## Caveats

- Authenticated requests may require client identification and request-signing
  headers in addition to a valid access token.
- Not affiliated with, endorsed by, or supported by BMTC or Chalo. For
  documentation and research purposes only.
