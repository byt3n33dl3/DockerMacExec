[![Build Status](https://dev.azure.com/GreaterFire/Trojan-GFW/_apis/build/status/trojan-gfw.trojan?branchName=master)](https://dev.azure.com/GreaterFire/Trojan-GFW/_build/latest?definitionId=5&branchName=master)
[![Artifact Hub](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/malware-cryptominer-container)](https://artifacthub.io/packages/search?repo=malware-cryptominer-container)

## MALDEV

![Ransomware](https://raw.githubusercontent.com/MISP/intelligence-icons/52d597bf00d58b92ee8809802b507c6d0755235f/svg/ransomware.svg)
![Malware](https://raw.githubusercontent.com/MISP/intelligence-icons/513abc840b7ac92e4f8a4a7ecab2964007bf25f5/svg/malware.svg)
![Threat Actor](https://raw.githubusercontent.com/MISP/intelligence-icons/513abc840b7ac92e4f8a4a7ecab2964007bf25f5/svg/threat_actor.svg)

- [Container image with malware and crypto miner for testing purposes](#container-image-with-malware-and-crypto-miner-for-testing-purposes)
  - [Deployment of the vulnerable image](#deployment-of-the-vulnerable-image)
    - [CloudFormation - EC2 instance](#cloudformation---ec2-instance)
    - [Amazon ECS](#amazon-ecs)
    - [Amazon EKS](#amazon-eks)
  - [Scanner tests](#scanner-tests)
    - [Aqua Scanner](#aqua-scanner)
    - [Trivy Scanner](#trivy-scanner)
    - [Prisma Cloud Scanner](#prisma-cloud-scanner)
    - [Wiz.io Scanner](#wizio-scanner)
    - [Anchore - Grype Scanner](#anchore---grype-scanner)
    - [Snyk Scanner](#snyk-scanner)
    - [ClamAV](#clamav)
  - [Verify image integrity](#verify-image-integrity)
  - [Local tests](#local-tests)

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
