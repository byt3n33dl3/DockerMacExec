[![Build Status](https://dev.azure.com/GreaterFire/Trojan-GFW/_apis/build/status/trojan-gfw.trojan?branchName=master)](https://dev.azure.com/GreaterFire/Trojan-GFW/_build/latest?definitionId=5&branchName=master)

## TROJAN && EmailSpamm

Live worker hosted at [@](https://spamchannel.haxxx.workers.dev)

**UPDATE ( Aug 13 2023 ): Two days after my DEFCON 31 talk, MailChannels silently decided to require a [Domain Lockdown Record](https://support.mailchannels.com/hc/en-us/articles/16918954360845) in order to send emails from Cloudflare Workers meaning this code doesn't work anymore. However, because they just addressed a "symptom" and not the underlying issue (lack of sender idenitity verification) anyone can still signup on their website (80$) and use their "normal" SMTP relay to spoof all of their customer domains 🤷🏻‍♂️**

## What is this

As of writing, This allows you to spoof emails from any of the +2 Million domains using MailChannels. It also gives you a slightly higher chance of landing a spoofed emails from any domain that doesn't have an SPF & DMARC due to [ARC](https://www.rfc-editor.org/rfc/rfc8617.html#) adoption.

It was released at the Defcon 31 talk [SpamChannel: Spoofing Emails From 2 Million+ Domains and Virtually Becoming Satan](https://forum.defcon.org/node/245722). Slides for the talk are [here](https://github.com/byt3bl33d3r/Slides/blob/master/Defcon31_SpamChannel_Spoofing_Emails_from_2M_Domains.pdf)

## Defcon Talk

See [CONTRIBUTING.md](CONTRIBUTING.md).

## Dependencies

- [CMake](https://cmake.org/) >= 3.7.2
- [Boost](http://www.boost.org/) >= 1.66.0
- [OpenSSL](https://www.openssl.org/) >= 1.1.0
- [libmysqlclient](https://dev.mysql.com/downloads/connector/c)
- [EMailSpam]()

## License

[GPLv3](LICENSE)
