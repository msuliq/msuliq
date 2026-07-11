<!--
<div style="display: flex; justify-content: center; align-items: center; width: 100%; height: 300px; background-color: black;">
  <img src="https://github.com/msuliq/msuliq.github.io/raw/master/images/moving_stars_msuliq.gif" style="max-width: 100%; max-height: 100%;" alt="Moving Stars">
</div>
-->

# Hi, I'm Suleyman

I build fraud detection and abuse prevention systems. Sole architect of the authentication, identity, and anti-fraud platform
at a top-10 certificate authority, where attackers probe the platform daily. I pair LLM-augmented detection with human-led
forensics to take an attack from detection to mitigation in minutes, not days.

Work I can talk about publicly:

* Detected and shut down months-long attacker reconnaissance across authorization policies, invitation flows, password
  enumeration, and role-hijacking paths - every probed vector closed in code before exploitation.
* Bot and fake-account defense handling 1,000+ fake signups per day, including countermeasures against human
  CAPTCHA-solving farms (reCAPTCHA v2/v3, Cloudflare Turnstile).
* Insider-threat detection: staff and admin abuse, admins colluding with external attackers, attackers impersonating staff.
* Identity-theft detection that cross-matches IP geolocation, billing, shipping, personal details, and phone numbers
  across applications.
* Killed an SMS pumping attack that was burning ~$2,500/day. Designed, built, and deployed the countermeasure in 4 days;
  losses have stayed at $0 since.
* Stopped a persistent session hijacking attacker who survived password resets, 2FA resets, and full endpoint forensics -
  session binding, replay detection, and automatic termination of suspect sessions at the application layer.
* Under the hood: device fingerprinting, behavioral analytics, IP intelligence, and velocity controls protecting
  certificate issuance (TLS/SSL, code signing, identity) through 10x growth.

## Open source

* [omniauth_oidc](https://github.com/msuliq/omniauth_oidc) - OmniAuth strategy for OpenID Connect, first-class Microsoft Entra ID support
* [ip_geo_lookup](https://github.com/msuliq/ip_geo_lookup) - zero-dependency IP geolocation for fraud scoring and access control
* [balloon_hashing](https://github.com/msuliq/balloon_hashing) - pure Ruby implementation of the Balloon memory-hard hashing algorithm
* [yescrypt](https://github.com/msuliq/yescrypt) - Ruby C extension wrapping the yescrypt password hashing algorithm

## Writing

* [How to Stop SMS Pump Fraud From Draining Your Wallet (and Sanity)](https://medium.com/@msuliq/how-to-stop-sms-pump-fraud-from-draining-your-wallet-and-sanity-11ea5435608d)
* [Authenticating with OmniAuth and OpenID Connect (OIDC) in Rails](https://msuliq.medium.com/authenticating-with-omniauth-and-openid-connect-oidc-in-ruby-on-rails-applications-e136ec5b48c0)

Ruby/Rails, Python, C, SQL. Before engineering: quantitative trading, risk modeling and fraud modeling are the same discipline with different labels.

Open to senior fraud/abuse and security engineering roles, and solutions engineering at security vendors. US-remote (UTC+5, comfortable with US overlap).
