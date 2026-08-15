<!--
<div style="display: flex; justify-content: center; align-items: center; width: 100%; height: 300px; background-color: black;">
  <img src="https://github.com/msuliq/msuliq.github.io/raw/master/images/moving_stars_msuliq.gif" style="max-width: 100%; max-height: 100%;" alt="Moving Stars">
</div>
-->

## Hi, I'm Suleyman

I'm a senior backend and distributed-systems engineer who likes hard problems and ships them as production code.
Right now I'm the sole architect of the authentication, identity, and certificate-issuance platform at a top-10
certificate authority - designing the distributed services, scaling issuance through 10x growth, writing the
cryptography and algorithms underneath, and, because attackers come with the territory, running the fraud and abuse
defense too.

**What I do:**

* **Distributed systems & architecture** - extracted authentication into a standalone service with cross-service
  sessions; built multi-perspective certificate validation (MPIC) with quorum across vantage points; designed the API
  servers, async workers, and audit pipelines around them.
* **Scale & performance** - scaled a backend through 10x growth in issuance; cut latency up to 5x by killing N+1s, a
  hot-path regex, and a write storm, and by reworking batch jobs into per-record fan-out.
* **Algorithms & cryptography** - PKI and X.509, memory-hard password hashing, and post-quantum signatures
  (ML-DSA / FIPS 204); 14 gems published to RubyGems (~50k+ downloads).
* **Correctness in money & state** - idempotent billing, atomic multi-step writes, and APIs that stay
  backward-compatible as they grow.
* **Auth & identity** - OAuth2, OpenID Connect, SAML/SSO, and session architecture, as the provider, not just the client.
* **Fraud, security & abuse** - detection and defense at a CA where attackers probe daily (a few examples below).

**A few security wins I can talk about publicly:**

* Shut down months-long attacker reconnaissance across authorization, invitation, password-enumeration, and
  role-hijacking paths - every probed vector closed in code before exploitation.
* Bot and fake-account defense at 1,000+ fake signups/day, including countermeasures against human CAPTCHA-solving farms.
* Killed an SMS pumping attack burning ~$2,500/day - built and deployed the fix in 4 days; losses $0 since.
* Stopped a persistent session-hijacking attacker who survived password resets, 2FA resets, and full endpoint forensics.

## Open source

Fourteen published gems (~50k+ RubyGems downloads), across the areas I work in.

**Security, PKI & certificates**

* [domain_sanity](https://github.com/msuliq/domain_sanity) - strict domain-name validation the way a CA must do it: RFC 1035, IDN/punycode, Public Suffix List, CA/Browser Forum wildcard rules, IP and reserved-range detection
* [csr_peek](https://github.com/msuliq/csr_peek) - safe CSR and X.509 certificate inspection: SANs, key strength, weak-signature checks, and a pluggable Baseline Requirements policy, no runtime dependencies
* [svg_sentinel](https://github.com/msuliq/svg_sentinel) - lint or sanitize untrusted SVG: blocks scripts, event handlers, XXE, and external references, with a CLI and SARIF output for CI
* [ip_geo_lookup](https://github.com/msuliq/ip_geo_lookup) - zero-dependency IP geolocation for fraud scoring and access control

**Authentication & identity**

* [omniauth_oidc](https://github.com/msuliq/omniauth_oidc) - OmniAuth strategy for OpenID Connect, first-class Microsoft Entra ID support
* [openid_config_parser](https://github.com/msuliq/openid_config_parser) - fetch and parse OpenID Connect discovery configuration from any issuer endpoint
* [oidc](https://github.com/msuliq/oidc) - OpenID Connect server and client library

**Cryptography & post-quantum**

* [ml_dsa](https://github.com/msuliq/ml_dsa) - Ruby C extension wrapping ML-DSA (FIPS 204), the post-quantum digital signature standard
* [pqc_asn1](https://github.com/msuliq/pqc_asn1) - minimal ASN.1/DER/PEM/Base64 codec for post-quantum key serialization
* [balloon_hashing](https://github.com/msuliq/balloon_hashing) - pure Ruby Balloon memory-hard hashing (SHA-256, SHA-512, BLAKE2b)
* [yescrypt](https://github.com/msuliq/yescrypt) - Ruby C extension wrapping the yescrypt password hashing algorithm

**Ruby & Rails utilities**

* [pg_search_multiple_highlight](https://github.com/msuliq/pg_search_multiple_highlight) - extends pg_search to highlight matches across multiple columns
* [delayed_crud](https://github.com/msuliq/delayed_crud) - delayed_create, delayed_update, and delayed_destroy helpers for Rails
* [distributed_merge](https://github.com/msuliq/distributed_merge) - extends Array with a distributed_merge for two-dimensional arrays

## Writing

* [How I Parse Domain Names For a Certificate Authority](https://msuliq.medium.com/how-i-parse-domain-names-for-a-certificate-authority-92a940f32bea) - RFC label rules, IDN/punycode, the Public Suffix List, and the edge cases that break naive checks (companion to `domain_sanity`)
* [We Reset the Password. We Reset 2FA. The Attacker Came Back in Seconds.](https://msuliq.medium.com/we-reset-the-password-we-reset-2fa-the-attacker-came-back-in-seconds-17575ad55246) - a session hijacking war story and the application-layer defense that ended it
* [A Secret You Cannot See Is Safer: Building a Secure Memory Buffer in C](https://msuliq.medium.com/a-secret-you-cannot-see-is-safer-building-a-secure-memory-buffer-in-c-876839dd6a66) - keeping private keys off swap and out of core dumps (companion to `libpqcsb`)
* [Trust, but Instrument: The Insider Threat Playbook](https://msuliq.medium.com/trust-but-instrument-the-insider-threat-playbook-c134742b7de0) - a news-anchored playbook for catching insider threats
* [How to Stop SMS Pump Fraud From Draining Your Wallet (and Sanity)](https://medium.com/@msuliq/how-to-stop-sms-pump-fraud-from-draining-your-wallet-and-sanity-11ea5435608d)
* [Authenticating with OmniAuth and OpenID Connect (OIDC) in Rails](https://msuliq.medium.com/authenticating-with-omniauth-and-openid-connect-oidc-in-ruby-on-rails-applications-e136ec5b48c0)

Ruby/Rails, Python, C/C++, SQL. Before engineering: quantitative trading - risk modeling turned out to be good training for distributed systems and for fraud alike.

Open to senior/staff roles in backend, distributed systems, platform, and security engineering. US-remote (UTC+5, comfortable with US overlap).
