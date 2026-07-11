<!--
<div style="display: flex; justify-content: center; align-items: center; width: 100%; height: 300px; background-color: black;">
  <img src="https://github.com/msuliq/msuliq.github.io/raw/master/images/moving_stars_msuliq.gif" style="max-width: 100%; max-height: 100%;" alt="Moving Stars">
</div>
-->

# Hi, I'm Suleyman

I build fraud detection and abuse prevention systems. Sole architect of the authentication and identity platform at a top-10 certificate authority, where
attacks are a daily fact of life.

Work I can talk about publicly:

* Killed an SMS pumping attack that was burning ~$2,500/day. Designed, built, and deployed the countermeasure in 4 days; losses have stayed at $0 since.
* Stopped a persistent session hijacking attacker who survived password resets, 2FA resets, and full endpoint forensics - by moving the defense into
  the application layer: session binding, replay detection, and automatic termination of suspect sessions.
* Built device fingerprinting, behavioral analytics, and IP intelligence pipelines protecting certificate issuance (TLS/SSL, code signing, identity)
  through 10x growth.
* Defend against account takeover, replay attacks, credential leaks, and privileged misuse, external and internal threats both.

## Open source

* [omniauth_oidc](https://github.com/msuliq/omniauth_oidc) - OmniAuth strategy for OpenID Connect, first-class Microsoft Entra ID support
* [ip_geo_lookup](https://github.com/msuliq/ip_geo_lookup) - zero-dependency IP geolocation for fraud scoring and access control
* [balloon_hashing](https://github.com/msuliq/balloon_hashing) - pure Ruby implementation of the Balloon memory-hard hashing algorithm
* [yescrypt](https://github.com/msuliq/yescrypt) - Ruby C extension wrapping the yescrypt password hashing algorithm

## Writing

* [How to Stop SMS Pump Fraud From Draining Your Wallet (and Sanity)](https://msuliq.medium.com/)
* [Authenticating with OmniAuth and OpenID Connect (OIDC) in Rails](https://msuliq.medium.com/)

Ruby/Rails, Python, C, SQL. Before engineering: quantitative trading, risk modeling and fraud modeling are the same discipline with different labels.

Open to senior fraud/abuse and security engineering roles, and solutions engineering at security vendors. US-remote (UTC+5, comfortable with US overlap).
