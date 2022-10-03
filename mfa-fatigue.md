# Multi-Factor Authentication "Fatigue" and Social Media Discussion Surrounding Uber Hack

MFA fatige was a key player in the Uber hack last month. Below is a message from the alleged hacker, according to Kevin Beaumont on Twitter. (https://twitter.com/GossiTheDog/status/1570717994397073410)

![image](https://pbs.twimg.com/media/FcxPrr3WQAEShcs?format=png&name=medium)

According to Steve Elovitz, Vice President of Mandiant on Twitter, there is a trend towards the abuse of MFA push notifications:
> Seeing an increasing amount of abuse of MFA prompt "push" notifications. Attackers are simply spamming it until the users approve. Suggest disabling push in favor of pin, or something like Yubico for simplicity. In the meantime, alert on volume of push attempts per account.
(https://twitter.com/SElovitz/status/1497598379622293504)

He goes on to say that in the mean time, OTP, or better FIDO2, should be implemented. He mentions Yubico, a well-known manufacturer of hardware MFA keys, most utilizing the FIDO2 standards. Yubico has been quick to capitalize on the attention surrounding the MFA fatigue attack at Uber, claiming that their product is resistant to phishing techniques like MFA fatigue. They even produced a video with Rachel Tobac, CEO of SocialProof Security, to demonstrate.

![video](https://twitter.com/i/status/1575172627387162624)

So although it seems like Yubico, and thus FIDO2, are about to be on the up-and-up, a recent paper presented in ESORICS 2022 by Guan et al. titled "A Formal Analysis of the FIDO2 Protocols" found that FIDO2 "fails to achieve some strong authentication properties." (Guan et al., 2022)

According to the paper, FIDO2's client PIN feature can be exploited, and the standard's Elliptic-Curve Diffie-Hellman (ECDH) key agreement is not authenticated in Client to Authenticator Protocol v2 (CTAP2). So while FIDO2 certainly seems like the next step in securing MFA against the rise of fatigue-based and other phishing attacks, it might need some work before it can be considered universally reliable and secure.


# References
Guan, J., Li, H., Ye, H., & Zhao, Z. (2022). A formal analysis of the FIDO2 protocols. _Computer Security – ESORICS 2022_, 3–21. https://doi.org/10.1007/978-3-031-17143-7_1