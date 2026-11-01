# Memory Sheet · GS Unit 3 · Topic 02 — Basics of Internet and E-mailing
> Questions: [../Questions/02-Internet-Email-Basics.md](../Questions/02-Internet-Email-Basics.md)

## 1. Core facts

### Timeline
| Year | Event |
|---|---|
| 1969 | ARPANET (US Dept of Defense) — first message UCLA → SRI |
| 1971 | Ray Tomlinson sends first network e-mail, introduces "@" |
| 1 Jan 1983 | ARPANET adopts TCP/IP (Vint Cerf & Bob Kahn) — "birth of the Internet" |
| 1989 | Tim Berners-Lee proposes WWW at CERN |
| 1990 | Archie — first internet search tool |
| 1991 | WWW made public; Linux kernel released |
| 1993 | Mosaic (NCSA) — first popular graphical browser |
| 15 Aug 1995 | VSNL launches public internet in India |
| 1998 | Google founded |
| 2004 | Gmail launched |

### Addressing
| Term | Meaning |
|---|---|
| IP address | Logical address of a device; IPv4 = 32-bit (e.g., 192.168.1.1), IPv6 = 128-bit (hex, colons) |
| MAC address | 48-bit physical address burnt into the network card |
| DNS | Domain Name System — domain name → IP address ("phonebook of the Internet") |
| ARP | IP address → MAC address |
| URL | Uniform Resource Locator, e.g. `https://www.example.ac.in/index.html` |
| URL parts | `https` = protocol; `www.example.ac.in` = domain/host; `.in` = country-code TLD; `/index.html` = path/file |
| ISP | Internet Service Provider |

### Protocols and ports
| Protocol | Job | Port |
|---|---|---|
| HTTP / HTTPS | Web pages / secure (SSL-TLS) web | 80 / 443 |
| FTP | File transfer | 20, 21 |
| SSH / Telnet | Secure / insecure remote login | 22 / 23 |
| SMTP | **Sending** e-mail | 25 |
| DNS | Name resolution | 53 |
| POP3 | Download mail to one device (usually deletes from server) | 110 |
| IMAP | Sync mail, stays on server, many devices | 143 |
| TCP vs UDP | Reliable, connection-oriented vs fast, connectionless (streaming, DNS queries) | — |

### Browsers, search engines, e-mail clients
| Browsers | Search engines | E-mail clients/services |
|---|---|---|
| Chrome, Firefox, Safari, Edge, Opera; Mosaic (first popular) | Google, Bing, Yahoo, DuckDuckGo, Baidu; Archie (first) | Outlook, Thunderbird; Gmail, Yahoo Mail |

### E-mail anatomy
| Field | Meaning |
|---|---|
| To | Main recipient |
| CC | Carbon Copy — visible to everyone |
| BCC | Blind Carbon Copy — hidden from other recipients |
| Subject | Topic line |
| Attachment | File sent with the mail (paper-clip icon) |
| Reply / Reply All / Forward | To sender / to sender + all visible recipients / to a new person |
| Draft, Inbox, Outbox, Sent, Spam/Junk, Trash | Folders |
| Signature | Auto-added footer |

### Networks
| Type | Range | Example |
|---|---|---|
| PAN | ~10 m | Bluetooth earphones |
| LAN | Building / campus | College computer lab |
| MAN | City | Cable-TV network of a city |
| WAN | Country / globe | The Internet |

| Device | Works with | Note |
|---|---|---|
| Hub | — | Broadcasts to all ports (dumb) |
| Switch | MAC address | Sends only to the intended port within a LAN |
| Router | IP address | Connects different networks |
| Repeater | Signal | Regenerates weak signal |
| Modem | Signal | Digital ↔ analog |
| Gateway | Protocols | Connects dissimilar networks |

Topologies: **Bus** (one backbone cable), **Star** (central hub/switch — most common), **Ring**, **Mesh** (every node linked — most reliable), **Tree**.

| Wireless | IEEE |
|---|---|
| Wi-Fi | 802.11 |
| Ethernet (wired) | 802.3 |
| Bluetooth | 802.15 |
| WiMAX | 802.16 |

### Cloud computing
| Model | You get | Example |
|---|---|---|
| SaaS | Ready software | Gmail, Google Docs |
| PaaS | Platform to build apps | Google App Engine |
| IaaS | Virtual servers, storage | AWS EC2 |
Deployment: public, private, hybrid, community. India's government cloud initiative: **MeghRaj**.

### Cyber threats
| Threat | Meaning |
|---|---|
| Spam | Unsolicited bulk e-mail |
| Phishing / Smishing / Vishing | Fake e-mail / SMS / voice call to steal data |
| Pharming | Redirect to fake website |
| Spoofing | Faking sender identity |
| Malware | Virus (needs host file), Worm (self-spreading), Trojan (disguised), Ransomware (encrypts, demands ransom), Spyware |
| DoS / DDoS | Flooding a server to crash it |
| Firewall | Filters incoming/outgoing traffic |
| 2FA / MFA | Password + OTP/biometric |

## 2. Memory hooks
1. **The Internet as the postal system.** IP address = house address; DNS = the phone directory that turns "Sharma ji" (domain) into the address; router = the post office that sorts parcels between cities; packets = postcards.
2. **E-mail as an office memo.** CC = copying a colleague openly; **BCC = the "secret copy"** slipped into the boss's tray — nobody else knows.
3. **"SMTP = Send Mail To People."** POP3 and IMAP *receive*. **POP = "pop it out" (download and remove)**; **IMAP = "I Maintain All Places"** (synced everywhere).
4. **Port number tricks:** HTTP **80** — "**8**0 for the **W**eb"; HTTPS **443** — "**4** **4**-**3**: Safe in 3 locks"; SMTP **25** — "Twenty-five letters a day"; DNS **53**; FTP **20-21** — "transferring files at age 20-21".
5. **Timeline chain "69-71-83-89-95":** ARPANET born (69) → e-mail (71) → TCP/IP (83) → WWW (89) → India online on Independence Day (95). "Each step is a decade-ish; India joins on 15 August."
6. **IPv4 vs IPv6: "4 → 32, 6 → 128".** IPv6 is 4 times longer in bits — enough addresses for every grain of sand.
7. **"-ishing" family by medium:** **Ph**ishing = e-mail (fishing with a mail bait); **Sm**ishing = **SM**S; **V**ishing = **V**oice. Pharming = poisoning the "farm" (DNS), so even the correct address leads to a fake site.
8. **Network size ladder "P-L-M-W" = "Please Let Me Win":** Personal < Local < Metropolitan < Wide.
9. **Cloud as food:** IaaS = renting a kitchen; PaaS = renting a kitchen with chef's tools ready; SaaS = ordering food on Zomato — just eat.
10. **Hub vs switch vs router:** Hub = shouting in a classroom (everyone hears); Switch = passing a note to a specific student; Router = sending a letter to another school.
11. **Bluetooth = a Danish king, Harald "Bluetooth"** — the logo combines his initials in runes; short-range, like a king's personal messenger (PAN).

## 3. Don't mix up
| Pair | Difference |
|---|---|
| Internet vs WWW | Internet = network of networks (infrastructure); WWW = web pages served over it |
| CC vs BCC | Visible vs hidden recipients |
| POP3 vs IMAP | Download & delete vs synced on server |
| DNS vs ARP | Name → IP vs IP → MAC |
| Switch vs Router | MAC, within a LAN vs IP, between networks |
| Virus vs Worm | Needs a host file vs self-replicates across networks |
| Browser vs Search engine | Chrome (software to view pages) vs Google (website to find pages) |
| Tim Berners-Lee vs Vint Cerf | WWW vs TCP/IP |
| Phishing vs Pharming | Bait message vs poisoned redirection |

## 4. Exam traps
- DNS does **not** give MAC addresses.
- SMTP only **sends**; it cannot fetch mail.
- Reply All does **not** go to BCC recipients.
- Google Chrome is a **browser**; Google Search is a **search engine**.
- The Internet in India opened to the public on **15 August 1995 (VSNL)**.
- In PaaS the **provider** manages hardware; the user controls the most in **IaaS**.
- Linux is an **OS**, not a browser.
