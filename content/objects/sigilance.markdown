---
title: SIGILANCE OpenPGP Smart Card
date: 2015-07-01
---

The SIGILANCE project predates Oddly Specific Objects by nearly a decade, but it was my first foray into making physical objects. As a product it was a monumental flop, but I learned a great deal from the failure. For posterity's sake, the original writeup is preserved below with minor edits.

<!--more-->

---

In 2014, I began working on a concept for secure cryptographic key generation via small, purpose-built systems. After testing and iterating on the concept, this evolved into SIGILANCE, an NFC-enabled OpenPGP smart card that brought smart card cryptography to mobile devices at a lower price point than existing solutions.

{{< figure src="/images/20150701-the-card.jpg" alt="A product shot of the SIGILANCE OpenPGP Smart Card, sitting on top of an RFID-blocking sleeve for the same." position="left" caption="The SIGILANCE OpenPGP Smart Card." captionPosition="left" >}}

## The Case for Smart Cards

PGP was designed in the early 1990s, a time when many people owned only one computer that spent most of its time offline. Back then, it was sufficient to store cryptographic keys on that computer and protect them with a passphrase. Times have changed, however. Today, people are much more likely to own multiple devices such as a smartphone, a tablet and a laptop, and it's safe to assume that they all have a persistent, always-on connection to the Internet. A user who wants to access their encrypted email on all of their devices would have to store their cryptographic key file on all of those devices, and type their passphrase into each of these devices. This dramatically increases the surface area available to an attacker seeking to compromise those keys.

The OpenPGP smart card, first specified in the early 2000s, was a solution to this problem. A smart card with cryptographic capabilities can function as a secure, air-gapped system that is capable of securely storing cryptographic keys and performing cryptographic tasks without disclosing the keys to a host machine. Since the initial publication of the specification, several manufacturers have created OpenPGP smart cards and compatible security tokens. But until the late 2010s, these smart cards only worked with desktop operating systems via USB smart card readers.

The SIGILANCE OpenPGP smart card included a traditional contact-based interface, which made it compatible with PC operating systems via a smart card reader. The key innovation was that it also included an NFC interface, which made it compatible with Android smartphones and tablets with NFC functionality. While some high-end security tokens of the time incorporated an NFC interface, the SIGILANCE OpenPGP Smart Card was the first NFC-enabled card to support OpenPGP, and it did so at a lower price point than any product then on the market.

## Software Support: OpenPGP on Mobile

In early 2015, the open source Android project OpenKeychain began implementing support for the Yubikey security token via NFC. At least initially, the support was limited to signing and decrypting messages; administrative tasks like generating keys for the token still needed to be done on a desktop machine.

I applied my knowledge of the OpenPGP specification to make some substantive contributions to that project, including functionality for changing card data and PINs, and for moving cryptographic keys from the Android tablet onto a smart card. This allowed a user to generate an OpenPGP identity on an Android tablet and move it to an NFC-enabled smart card, all through an intuitive graphical user interface rather than a complex command-line interaction.

{{< image src="/images/apps-sigilance-cardedit-screenshot-1.png" alt="A screenshot of the SIGILANCE CardEdit app listing information on a card." position="center" style="width: 48%; float: left" >}}{{< image src="/images/apps-sigilance-cardedit-screenshot-2.png" alt="A screenshot of the SIGILANCE CardEdit app's PIN change interface." position="center" style="width: 48%" >}}

In addition to my contributions to OpenKeychain, I also implemented a small utility app called SIGILANCE CardEdit, which allowed users to edit the metadata stored on their OpenPGP smart card in a manner similar to the GnuPG card-edit facility.

## Security Audit

While evaluating existing open source implementations of the OpenPGP smart card standard, I was able to identify a critical vulnerability ([CVE-2015-3298](https://developers.yubico.com/ykneo-openpgp/SecurityAdvisory%202015-04-14.html)) in the javacardopenpgp applet that affected the Yubikey NEO. I disclosed this vulnerability to the manufacturer of the vulnerable devices and offered a fix; they implemented this fix and announced a product replacement program in April of 2015.

## Design and Branding

I designed the logo and visual identity for SIGILANCE myself; while I am mostly a software engineer, I thought that good design would be imperative to get widespread adoption of a device like this. The SIGILANCE smart card design incorporates a clean look without extraneous logos or branding. A hologram on the face of the card serves the dual purpose of showing that the card is genuine, and displaying the card's unique serial number.

The face of the card also incorporates space for the two most important bits of information for most people who use OpenPGP's Web of Trust: your identifying information, and the key fingerprint tied to your identity. If you've ever signed someone's key or asked someone to sign your key, these are the two essential bits of data required for that task. You can either write on the card with a permanent marker, or print out a label and stick it on.

## The end of SIGILANCE

After a couple of years of slow sales, I decided to pull the plug on the SIGILANCE project. Still, it was the first physical object that I ever sold and shipped, and I learned valuable lessons from its failure to find market fit.
