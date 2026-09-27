# Practical 7: Privacy-Enhancing Technologies

## Aim

To study different Privacy-Enhancing Technologies (PETs), including VPNs, Tor and secure messaging applications, and evaluate their effectiveness in protecting privacy.

## Introduction

Privacy-Enhancing Technologies are technologies designed to reduce the amount of personal information exposed during online activities.

The technologies studied in this practical are:

1. VPN
2. Tor
3. Secure Messaging Applications

---

## 1. VPN

A Virtual Private Network creates an encrypted connection between a device and a VPN server.

### Advantages

- Encrypts traffic between the device and VPN server.
- Useful on untrusted networks such as public Wi-Fi.
- Can hide the user's IP address from websites by presenting the VPN server's IP.

### Limitation

A VPN does not make the user completely anonymous. The VPN provider may be able to observe certain information depending on its infrastructure and policies.

---

## 2. Tor

Tor routes internet traffic through multiple relays.

Basic working:

User -> Entry Relay -> Middle Relay -> Exit Relay -> Internet

### Advantages

- Provides stronger anonymity than ordinary direct browsing.
- Makes it harder to directly associate traffic with its original source.
- Useful for privacy-sensitive browsing.

### Limitations

- Usually slower than normal browsing.
- Some websites block or challenge Tor traffic.
- Tor does not automatically protect information that a user voluntarily provides.

---

## 3. Secure Messaging Applications

Secure messaging applications can use end-to-end encryption (E2EE).

In an E2EE system, the message is encrypted at the sender's device and decrypted at the intended recipient's device.

### Advantages

- Protects message contents from intermediaries.
- Useful for private communication.
- Reduces the risk of message interception.

### Limitations

- Metadata may still exist depending on the application.
- The security of the user's device is also important.
- Backups may have different privacy protections.

---

## Comparison

| Technology | Main Purpose | Main Limitation |
|------------|--------------|-----------------|
| VPN | Protects network traffic | VPN provider may see certain traffic information |
| Tor | Improves online anonymity | Slower and sometimes blocked |
| Secure Messaging | Protects message contents | Metadata and device security can still matter |

## Evaluation

No single technology provides complete privacy.

A VPN is useful for protecting network traffic, Tor provides stronger anonymity, and end-to-end encryption protects communication contents.

The appropriate technology depends on the privacy requirement and threat model.

## Result

VPNs, Tor and secure messaging technologies were studied. Their working, advantages, limitations and privacy protection capabilities were compared.
