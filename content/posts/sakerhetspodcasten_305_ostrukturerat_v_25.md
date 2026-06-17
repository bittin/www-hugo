---
date: '2026-06-17T09:11:00'
tags:
- ostrukturerat
title: 'Säkerhetspodcasten #305 - Ostrukturerat V.25'
---
Microsoft / Nighmare Eclipse drama,
Bumsrake FreeBSD KTLS kernel sårbarhet,
FFmpeg sårbarheter,
CI/CD säkerhet:
  (Boost Security Labs, Bumblebee, Härda din NPM/Bun mot Supply Chain Hell),
Arch User Repository (AUR) Supply Chain Hell,
AI:
 (Facebook FAIL, Fable/Mythos, driver sårbarheter),
Frostig webläsare!

Lyssna:
* [mp3](https://traffic.libsyn.com/secure/sakerhetspodcasten/2026-06-15_Sakerhetspodcasten.mp3?dest-id=117848), längd: 01:04:24

## Microsoft's Nighmare Eclipse drama

Nighmare Eclipse fortsätter hoppa runt medan
  Micrsoft försöker boota ut hen från alla tjänster...
Utkastad från Github,
  utkastad från Gitlab,
  tillbaka på nytt Github konto.

Detaljerna med vad exakt som gått fel mellan Nightmare Eclipse och Microsoft
  är oklart, då ingen fullt ut talar klarspråk.
Det spekuleras i att Nightmare Eclipse är en f.d. bugbounty jägare som blivit
  rejält osams med Microsoft.
Andra hävdar att det är en fd.d Micrsoft anställd.

NE, 13:e maj:

> I just noticed that Microsoft silently patched the RedSun vulnerability,
>   no CVE, no nothing, just a silent patch. Not surprised they never admit
>   their mistakes but considering it was under active exploitation, having
>   zero advisory is insane.

NE, 20:e maj:

> You defame me in public with your CVE-2026-45585 advisory even though you
>   literally deleted the Microsoft account I used to report bugs to you with
>   and I got zero pennies from doing so and I still happily did like an idiot.

NE, 6 juni - kanske inte årets mest stabila researcher:

> I'm starting to genuinely struggle with sleep and constant fevers.

Andra oberoende parter hävdar att Microsoft CVD / MSRC inte fungerat bra
  den senaste tiden, att de också haft dåliga erfarenheter,
  ex. Rémi GASCOU (Podalirius):

> MSRC did not reward a bounty nor did they attribute a CVE to this finding
>   because this ”doesn’t meet [their] criteria as a vulnerability that
>   requires an immediate security update”

dvs. Microsoft genom sitt agerande uppmuntrar folk att sluta sammarbeta med
  dem.

Microsoft från kritik från flera håll om sina formuleringar så som:

> Uncoordinated disclosures that put proof-of-concept code for unpatched
>   vulnerabilities into the hands of bad actors are never
>   justifiable and have real-world consequences.
> Our security teams across the company work tirelessly tracking threat
>   actors who look for weaknesses just like these to attack Microsoft
>   and our customers.
> Our Digital Crimes Unit will continue bringing cases against these actors
>   and those that enable their criminal activity – coordinating as needed
>   with law enforcement around the world.
>
> [...]
>
> Our team will continue to support responsible research as we do everything
>   we can to quickly investigate, address, and release updates for
>   vulnerabilities that impact our customers. We always have and will continue
>   to welcome vulnerability submissions from anyone through our public
>   researcher portal, regardless of past interactions or reputation.

Skrivelserna kan tolkas om att man antyder att Microsoft
  Coordinated Vulnerability Disclosure (CVD) är ett krav, att sammanbrott i
  sammarbetet kan medföra stämningar eller anmällan för brott.
Att man inte fullt ut skiljer "Uncoordinated Disclosure" från kriminallitet.

Fundering:
* Hade man vågat skriva så om t.ex. Google Project Zero?
* Är sammarbetsproblem mellan enskilda mer "hotbart"?

Blir någonting bättre av att det är svårt att hitta var Nightmare Eclipse
  filer faktiskt hostas?
Blir det inte bara mer förvirrat och konstigt för defenders, journalister
  med flera om Microsoft / Github / Gitlab om och om igen dödar länkar?

Anyway anyhow, märkligt info-sec drama mellan pyttemjuk och en av deras
  bättre LPE / race condition finnare.

Länkar:
* [A shared responsibility: Protecting customers through Coordinated Vulnerability Disclosure](https://www.microsoft.com/en-us/msrc/blog/2026/05/a-shared-responsibility-protecting-customers-through-coordinated-vulnerability-disclosure)
* [Barracuda/ Christine Barry: Nightmare-Eclipse - six zero-days, six weeks and one big grudge](https://blog.barracuda.com/2026/05/19/nightmare-eclipse-zero-days-grudge)
* [Tom's Hardware/ Bruno Ferreira: Microsoft's GitHub bans security researcher who posted zero-day Windows exploits because company 'ruined their life' — expert claims action is vindictive and promises further retaliation - I will make sure your bones are shattered [on July 14]](https://www.tomshardware.com/tech-industry/cyber-security/microsofts-github-bans-security-researcher-who-posted-zero-day-windows-exploits-because-company-ruined-their-life-expert-claims-action-is-vindictive-and-promises-further-retaliation)
* [x/Rémi GASCOU (Podalirius): Last time I dealt with MSRC](https://x.com/podalirius_/status/2059892083029069929)
  Hävdar att MSRC har en historik av att:
  * fixa buggarna i det tysta
  * utan att registrera en CVE
  * utan attribution till den som hittat problemet
  * utan att ge ut någon bugbounty
* [Nightmare Eclipse: We're doing silent patches now huh, also a quick note about YellowKey](https://deadeclipse666.blogspot.com/2026/05/were-doing-silent-patches-now-huh-also.html)
* [Nightmare Eclipse: July 14th](https://deadeclipse666.blogspot.com/2026/05/july-14th.html)
* [MSNightmare (Nightmare-Eclipse) · GitHub](https://github.com/MSNightmare)
* [YouTube/ Mental Outlaw: Microsoft's Bug Bounty Betrayal Puts Everyone in Danger](https://www.youtube.com/watch?v=fL9HzADcTsY) `video`
* [YouTube/ Marcus Hutchins: Microsoft Wants To Throw Researcher In Jail](https://www.youtube.com/watch?v=gCkfWo5rie8) `video`
* [YouTube/ The PrimeTime: "We will ruin your life" -Microsoft](https://www.youtube.com/watch?v=9kxx5xp5nTQ) `video`


## Bumsrake FreeBSD KTLS kernel sårbarhet

FreeBSD svar på Linux Copy FAIL stil buggarna var
  CVE-2026-45257
  "Arbitrary file overwrite via the KTLS receive path"

Säkerhetsforskaren Bumsrakete (rumpraket...) presenterar den helt fantastiskt:

Kanske världens första bugg med Severity 13 på en skala 0-10!
CVSS kan inte ens förklara hur den nådde 13.

> The HUGEST, the MOST TREMENDOUS FreeBSD page-cache write primitive in the
>   history of computing.
> Many people are saying it. Many. Believe me.

> It is the FreeBSD analogue of Linux's Dirty Pipe, CopyFail, Fragnesia, and
>   Dirty Frag — except we gave it a BETTER name, with a BETTER logo, on a
>   BETTER website.
> The other bug websites? Disasters. Sad. Many people have told us this.


``` plain
                          user (uid 1001)
                                │
                                │ sendfile(target, snd_sock, off, 240)
                                ▼
   ┌──────────────────────────────────────────────────────────────────────┐
   │  kern_sendfile.c:963                                                 │
   │    mb_alloc_ext_pgs(M_WAITOK, sendfile_free_mext_pg, M_RDONLY)       │
   │    → M_EXT|M_EXTPG mbuf, m_epg_pa[] = real vnode page PA             │
   └──────────────────────────────────────────────────────────────────────┘
                                │  chain: [hdr 13B] [EXTPG 240B] [tag 16B]
                                ▼
   ┌──────────────────────────────────────────────────────────────────────┐
   │  tcp_output → ip_output → if_simloop (loopback)                      │
   │    lo0 doesn't have IFCAP_MEXTPG → calls mb_unmapped_to_ext(),       │
   │    which DOES NOT copy bytes — it just remaps the EXTPG via sf_buf   │
   │    onto the SAME physical page.                                      │
   └──────────────────────────────────────────────────────────────────────┘
                                │
                                ▼
   ┌──────────────────────────────────────────────────────────────────────┐
   │  tcp_input → sbappendstream_locked                                   │
   │    SB_TLS_RX is set → sbappend_ktls_rx → sb_mark_notready            │
   │    (no M_EXTPG check)                                                │
   └──────────────────────────────────────────────────────────────────────┘
                                │
                                ▼
   ┌──────────────────────────────────────────────────────────────────────┐
   │  ktls_decrypt → ktls_ocf_recrypt → aesni_cipher_crypt                │
   │    crypto_contiguous_subsegment returns PHYS_TO_DMAP(m_epg_pa[0])    │
   │    AES_GCM_decrypt(in=DMAP_PTR, out=DMAP_PTR, ...)                   │
   │                                                                      │
   │    ▶ page-cache page now holds attacker-chosen plaintext             │
   └──────────────────────────────────────────────────────────────────────┘
                                │
                                ▼
                      file's page cache is dirty
                       (and on UFS, on disk too)
```


``` c
/* sys/kern/kern_sendfile.c:963 */
m0 = mb_alloc_ext_pgs(M_WAITOK,
                      sendfile_free_mext_pg,
                      M_RDONLY);
/* m_epg_pa[] now holds the *physical addresses* of the file's page-cache pages. */
/* This is awesome for performance. It is also awesome for attackers. */
```

``` c
/* sys/netinet/tcp_usrreq.c:2222 */
case TCP_RXTLS_ENABLE:
    INP_WUNLOCK(inp);
    error = ktls_copyin_tls_enable(sopt, &tls);
    /* Notice anything missing here? A priv_check, perhaps?
       Many people are noticing. Many. Very smart people. */
    if (error != 0)
        break;
    error = ktls_enable_rx(so, &tls);
    ...
```

``` c
/* sys/opencrypto/criov.c:273 */
return (PHYS_TO_DMAP(m->m_epg_pa[i] + pgoff + skip));

/* sys/crypto/aesni/aesni.c:599-605 (and AES_GCM_decrypt in the same file) */
error = aesni_cipher_crypt(ses, crp, csp);
/* in == out semantics. The "output buffer" is a DMAP pointer at the
   file's page-cache page.  AES_GCM_decrypt writes the plaintext there. */
```

Länkar:
* [BUMSRAKETE™ — The Most Beautiful, Most Tremendous FreeBSD Vulnerability In The History Of Computing. BELIEVE ME. - BUMSRAKETE is a HUGE, TREMENDOUS, MANY-PEOPLE-ARE-SAYING FreeBSD kTLS-RX page-cache write primitive. The BEST primitive. Some say the best ever.](https://bumsrake.de/)
* [GitHub - bumsrakete/bumsraketev1 · GitHub](https://github.com/bumsrakete/bumsraketev1)
* https://www.freebsd.org/security/advisories/FreeBSD-SA-26:26.ktls.asc


## FFmpeg sårbarheter

Internets stora video-utility / lib hade massa sårbarheter.

Länkar:
* [21 Zero-Days in FFmpeg | depthfirst](https://depthfirst.com/research/21-zero-days-in-ffmpeg)
* [YouTube/ Low Level: AI Did This.](https://www.youtube.com/watch?v=QGC40AfmgY0) `video`


## CI/CD säkerhet: Boost Security Labs

OpenSource Security har ett långt snack med
  François Proulx (Boost Security Labs).

Snackar bland annat om:
* poutine (CI/CD pipeline sårbarhetscanner)
* smokedmeat (CI/CD RED Team exploitation verktyg)
* bagel (Utvecklarmaskin scanner för att skatta effekt av dev-compromise)

Länkar:
* [Open Source Security/ Josh Bressers: Hacking your CI/CD with François Proulx](https://opensourcesecurity.io/2026/2026-06-fran%C3%A7ois-smoked-meat/)
* [GitHub - boostsecurityio/poutine: poutine, a supply chain vulnerability scanner for build pipelines · GitHub - poutine, a supply chain vulnerability scanner for build pipelines - boostsecurityio/poutine](https://github.com/boostsecurityio/poutine)
* [GitHub - boostsecurityio/smokedmeat: A CI/CD Red Team Framework for demonstrating Build Pipeline security risks. · GitHub - A CI/CD Red Team Framework for demonstrating Build Pipeline security risks. - boostsecurityio/smokedmeat](https://github.com/boostsecurityio/smokedmeat)
* [GitHub - boostsecurityio/bagel: bagel, a CLI that inventories security-relevant metadata on developer workstations · GitHub - bagel, a CLI that inventories security-relevant metadata on developer workstations - boostsecurityio/bagel](https://github.com/boostsecurityio/bagel)
* [YouTube/ Open Source Security: Hacking your CI/CD with François Proulx](https://www.youtube.com/watch?v=V3c8-zjCpKA) `video`


## CI/CD säkerhet: Bumblebee

En Utvecklarmaskin scanner för att skatta effekt av dev-compromise.

Länkar:
* [Perplexity Is Open-Sourcing Bumblebee](https://www.perplexity.ai/hub/blog/perplexity-is-open-sourcing-bumblebee)
* [GitHub - perplexityai/bumblebee: Read-only developer endpoint scanner for on-disk package, extension, and developer-tool metadata, built to check exposure to known software supply-chain compromises. · GitHub - Read-only developer endpoint scanner for on-disk package, extension, and developer-tool metadata, built to check exposure to known software supply-chain compromises. - perplexityai/bumblebee](https://github.com/perplexityai/bumblebee)
* [YouTube/ Better Stack: Perplexity Open-Sourced a Scanner Every Dev Should Know (Bumblebee)](https://www.youtube.com/watch?v=L6iAw5yitfc) `video`

## CI/CD säkerhet: Härda din NPM/Bun mot Supply Chain Hell

Better Stack går igenom NPM härningstrick:

* 0:39 Don't Install New Packages (min release age)
* 2:06 Disable Scripts
* 3:52 Block Git-based dependencies
* 5:02 Scan Dependencies (Socket & npq)
* 6:41 Review Lockfile
* 7:36 Use Clean Install Commands
* 8:18 Build better habits

Socket Firewall Free skall kunan skydda:
* JavaScript/TypeScript: `npm`, `yarn`, `pnpm`
  (`sfw` might work with other package managers, but support is not guaranteed)
* Python: `pip`, `uv`
* Rust: `cargo`

Länkar:
* [GitHub - lirantal/npm-security-best-practices: Collection of npm package manager Security Best Practices · GitHub - Collection of npm package manager Security Best Practices - lirantal/npm-security-best-practices](https://github.com/lirantal/npm-security-best-practices)
* [Socket Firewall Free](https://docs.socket.dev/docs/socket-firewall-free)
* [YouTube/ Better Stack: npm installs can hack your laptop (Here's how to stop it)](https://www.youtube.com/watch?v=Wq6yMdt11LM) `video`

## Arch User Repository (AUR) Supply Chain Hell

Massiv Supply Chain Hell attack!

> **Warning**
> AUR packages are user-produced content.
> These PKGBUILDs are completely unofficial and have not been thoroughly vetted.
> Any use of the provided files is at your own risk.

> If you plan to use AUR repository, it is highly recommended to follow
> aur-general Arch mailing list which has been used for security warnings
> in the past.

* [YouTube/ Brodie Robertson: Massive AUR Malware Attack - DO NOT UPDATE](https://www.youtube.com/watch?v=WoxR7fGl4CI) `video`
* [Arch User Repository - ArchWiki](https://wiki.archlinux.org/title/Arch_User_Repository)


## AI: Facebook FAIL

Facebook (Meta) gav AI chatbot ansvar för användarkonto-säkerhet.
Hur gick det?

Angripare VPN:ade till målets region.
Sa till chatbot att de var hackade.
Bad om password reset länk till sin egen mail.
Konto ägt.

Länkar:
* [404 Media/ Jason Koebler: Hackers Simply Asked Meta AI to Give Them Access to High-Profile Instagram Accounts. It Worked - The exploit shows the extreme risk of offloading technical support to AI.](https://www.404media.co/hackers-simply-asked-meta-ai-to-give-them-access-to-high-profile-instagram-accounts-it-worked/)
* [YouTube/ 404 Media: Hackers Asked Meta AI To Let Them In. It Worked](https://www.youtube.com/watch?v=MsAtXST87pk) `video`
* [YouTube/ Pivot to AI: Log into any Instagram by asking Meta’s AI nicely](https://www.youtube.com/watch?v=KUkDMUrfQiU) `video`
* [YouTube/ Low Level: AI Was a Mistake](https://www.youtube.com/watch?v=wlMgNtBipe4) `video`

## AI: Fable/Mythos nedstängt

Fable (extremt nedstängd Mythos, som ibland slog över till Opus) nedstängt av US-Gov

Länkar:
* [Statement on the US government directive to suspend access to Fable 5 and Mythos 5 \ Anthropic - The US government has issued an export control directive to suspend all access to Fable 5 and Mythos 5 by any foreign national, whether inside or outside the United States.](https://www.anthropic.com/news/fable-mythos-access)
* [YouTube/ Theo - t3․gg: BREAKING - Fable and Mythos have been taken down for security concerns.](https://www.youtube.com/watch?v=W-kM56mf-Nw) `video`
* [YouTube/ Low Level: The First Domino Has Fallen...](https://www.youtube.com/watch?v=gDpuFDCLvBc) `video`

Cloudflare, hur bra var mythos:
* Klarar Rust m.m. dåligt, inbillar sig C/C++ minnes-fel i kompiler säkrad kod.
* Mycket skräp i output
* Testramverk ett måste
  * Begränsa vad Mythos tittar på (begränsa context, få upp prestanda)
  * Sekundär AI som bedömmer om output ens är rimlig, intressant.
  * Sekundär AI med fördel splittras upp i olika frågestälningar.
  * En AI skall ifrågasätta om koden ens är nåbar.
  * En AI skall ifrågasätta om koden faktiskt är sårbar.

## AI: Hur bra var Mythos enligt Cloudflare, Cybergym med flera?

Cloudflare:
  Mythos ett stort steg frammåt men inte revolutionerade.
  Inte problemfri.

> We saw consistently more false positives from projects written in memory-unsafe languages.
>
> [...]
>
> Findings come back hedged with "possibly," "potentially," "could in theory," and the hedged findings vastly outnumber the solid ones.

Low Level Learning: Enligt cybergym benchmarks är den inte generationer före konkurenter!

Länkar:
* [The Cloudflare Blog: Project Glasswing - what Mythos showed us](https://blog.cloudflare.com/cyber-frontier-models/)
* [YouTube/ Low Level: The First Domino Has Fallen...](https://www.youtube.com/watch?v=gDpuFDCLvBc) `video`
* [CyberGym: Evaluating AI Agents' Real-World Cybersecurity Capabilities at Scale](https://www.cybergym.io/cybergym/)

## AI: scanna automatiserat efter Windows11-driver sårbarheter

Malware Tech Blog (Marcus Hutchins) om sitt arbete med ett testharnest
  för att automatiserad sökning efter sårbarheter i Windows11 drivers.
* Hög grad av förusägbar scriptning;
  * hitta drivers
  * testa installationer, att driver funkar och inte är svartlistad
  * reverse engineering
* Bara AI där det passar
* Opus med massa promptning för att bedömma output
* Opus själv fattar inte grundläggande logik som att Read, Write
   primitiver är mer värda än blinda Execute primitiver.
   Någon smart måste förklara vad som är viktigt för exploitability.
* Massa människoarbete bakom "Zero-day AI pipeline"
* Ett AI testharnest tar en bara så långt.
  När denna pipeline hittat alla sina hål, så slutar den hitta hål.
  Lite som när fuzzing slutade hitta lågt hängande frukter.

Länk:
* [YouTube/ Marcus Hutchins: I Built an AI That Builds Zero Day Exploits](https://www.youtube.com/watch?v=BLqRiL_GY3A) `video`

## Frost: webbläsar-fingeravtryck via dators SSD prestanda

Script kan identifera ("ta fingeravtryck av") datorer
  genom att mäta I/O prestanda från webbläsar-API.

Åtminstone i perfekta labb-miljöer när SSD-prestandan är något så när
  deterministisk under mätning.

Kanske inte den största nyheten, men coolt?

Länkar:
* [Hannes Weissteiner , Tobias Weiser1, Roland Czerny, Sudheendra, Raghav Neela, Fabian Rauscher, Jonas Juffinger, and Daniel Gruss: FROST: Fingerprinting Remotely using OPFS-based SSD Timing](https://hannesweissteiner.com/pdfs/frost.pdf) `pdf`
* [Tom's Hardware/ Luke James: Researchers say they can spy on your browsing by measuring SSD activity through a browser API — claim FROST attack requires no permissions or user interaction to identify which apps and websites you're using - The technique correctly identified visited websites with roughly 89% accuracy and running applications with roughly 96% accuracy on a test Mac](https://www.tomshardware.com/tech-industry/cyber-security/researchers-say-they-can-spy-on-your-browsing-by-measuring-ssd-activity-through-a-browser-api)
* [YouTube/ LaserHelix: The SSD Situation](https://www.youtube.com/watch?v=XKncJjZ2ZNA) `video`




## AI transkribering

_AI försöker förstå oss... Ha överseende med galna feltranskriberingar._

`1 00:00:00,000 --> 00:00:02,960`
Hej och välkommen till Säkerhetspodcasten. Jag som pratar heter Johan Ryberg Möller.



`2 00:00:03,060 --> 00:00:04,480`
Med mig har jag Peter Magnusson.



`3 00:00:04,720 --> 00:00:06,040`
I en bitlocken över dig.



`4 00:00:06,220 --> 00:00:06,920`
Mattias Idage.



`5 00:00:07,120 --> 00:00:07,600`
Jajamän.



`6 00:00:07,800 --> 00:00:08,740`
Och Rickard Bordvarn.



`7 00:00:09,740 --> 00:00:10,220`
Jajamän.



`8 00:00:10,920 --> 00:00:12,040`
He is alive\!



`9 00:00:12,260 --> 00:00:14,100`
Back in the studio, stronger than ever.



`10 00:00:14,120 --> 00:00:15,500`
Och inga cellgifter i blodet.



`11 00:00:15,680 --> 00:00:16,000`
Woho\!



`12 00:00:17,220 --> 00:00:17,800`
Det är gött.



`13 00:00:17,980 --> 00:00:18,500`
Det är jävla nice.



`14 00:00:19,240 --> 00:00:21,180`
What doesn't kill you makes you immortal.



`15 00:00:22,280 --> 00:00:25,000`
Då kan jag säga, då är jag...



`16 00:00:25,640 --> 00:00:28,000`
From the clan McLeod of...



`17 00:00:28,000 --> 00:00:30,740`
From the clan McLeod of the clan McLeod and I'm immortal.



`18 00:00:31,560 --> 00:00:32,560`
Det måste jag säga om.



`19 00:00:32,900 --> 00:00:37,140`
Det finns ju en billig cancerpansiepatient som är ordelig.



`20 00:00:37,240 --> 00:00:38,920`
Jag tror att vi har pratat om henne tidigare.



`21 00:00:39,220 --> 00:00:39,380`
Ja.



`22 00:00:39,880 --> 00:00:43,980`
En rita, någonting som bara fortsätter leva vidare långt efter att hon själv är död.



`23 00:00:44,800 --> 00:00:45,780`
Den är ju...



`24 00:00:45,780 --> 00:00:47,680`
Det är så oerhört lite jag förstår nu av det du säger.



`25 00:00:47,960 --> 00:00:49,580`
Ja, vi går hastigt och lustigt vidare.



`26 00:00:49,740 --> 00:00:52,560`
Jesper är inte här för han har insett att det är midsommar om några dagar.



`27 00:00:52,700 --> 00:00:54,220`
Och det var jobbigt.



`28 00:00:54,260 --> 00:00:54,460`
Ja.



`29 00:00:54,460 --> 00:00:56,520`
Han bailade mig emergency.



`30 00:00:56,520 --> 00:01:00,200`
När vi spelar in detta så är det den 15 juni.



`31 00:01:00,320 --> 00:01:02,520`
Och när ni lyssnar på detta så har ni väl precis...



`32 00:01:02,520 --> 00:01:05,000`
Ja, ni tyckte väl att bota bakgrunden på en viss sammanhang då förmodligen?



`33 00:01:05,060 --> 00:01:05,800`
Nej, men vi måste...



`34 00:01:05,800 --> 00:01:07,200`
Det är nådens år, 2026.



`35 00:01:07,580 --> 00:01:08,760`
Ska vi släppa det nästa måndag alltså?



`36 00:01:08,840 --> 00:01:09,880`
Eller ska vi trycka ut så fort som möjligt?



`37 00:01:09,960 --> 00:01:11,240`
För egentligen skulle vi släppa det idag.



`38 00:01:11,900 --> 00:01:12,660`
Då trycker vi...



`39 00:01:12,660 --> 00:01:15,560`
Jag tror att vi kan reda ut...



`40 00:01:15,560 --> 00:01:17,420`
Ska vi inte fortsätta prata i tio minuter?



`41 00:01:17,460 --> 00:01:18,380`
Det är ju superbra podd.



`42 00:01:19,260 --> 00:01:19,460`
Ja\!



`43 00:01:19,780 --> 00:01:20,940`
Låt oss göra lite admin här.



`44 00:01:21,620 --> 00:01:24,200`
Särskilt som den som lyssnar vet ju om det är släppt eller inte.



`45 00:01:24,380 --> 00:01:24,900`
Oh my god.



`46 00:01:24,900 --> 00:01:26,400`
Ni märker själva när det här kommer ut.



`47 00:01:26,520 --> 00:01:28,660`
Gud vad smart du som lyssnar är som vet när det är släppt.



`48 00:01:28,660 --> 00:01:30,060`
Mind is blown.



`49 00:01:30,860 --> 00:01:31,900`
Du vet när det blir.



`50 00:01:33,040 --> 00:01:34,800`
Det är som att se i framtiden.



`51 00:01:35,060 --> 00:01:35,680`
Det är magiskt.



`52 00:01:38,100 --> 00:01:42,720`
För att få ut den här fantastiska produkten ni lyssnar på så har vi tre väldigt fina sponsorer.



`53 00:01:43,260 --> 00:01:45,520`
Som består av Shored som finns på shored.se.



`54 00:01:45,640 --> 00:01:48,080`
Så även 0x4A som finns på 0x4A.se.



`55 00:01:48,160 --> 00:01:49,800`
Och Bordfors som finns på Bordfors.se.



`56 00:01:50,040 --> 00:01:51,360`
Switched up the order ju.



`57 00:01:51,500 --> 00:01:53,000`
Jajamän, vi har bara check it around.



`58 00:01:53,100 --> 00:01:53,700`
Oh my god.



`59 00:01:53,700 --> 00:01:54,180`
Så är det.



`60 00:01:54,660 --> 00:01:56,500`
Det här är som ni har hört ett ostrukturerat avsnitt.



`61 00:01:56,520 --> 00:01:57,020`
Exakt.



`62 00:01:57,100 --> 00:01:58,060`
Och vad gör vi i ett sånt Mattias?



`63 00:01:58,420 --> 00:02:00,400`
Vi snackar blandade grejer.



`64 00:02:00,480 --> 00:02:01,580`
Oftast nyheter dock.



`65 00:02:01,660 --> 00:02:05,480`
Vad har hänt senaste månaden som vi har tyckt varit värdigt att ta upp här?



`66 00:02:05,660 --> 00:02:08,660`
Eller som Peter har tagit upp.



`67 00:02:08,660 --> 00:02:09,840`
Vi har kört security first.



`68 00:02:10,140 --> 00:02:10,540`
Det har vi.



`69 00:02:10,780 --> 00:02:12,620`
Jag har redigerat massvis med videos.



`70 00:02:12,840 --> 00:02:14,140`
Jag har sett att de har börjat droppa också.



`71 00:02:14,680 --> 00:02:15,500`
Ja, många är ute.



`72 00:02:15,980 --> 00:02:16,740`
Är alla ute?



`73 00:02:17,360 --> 00:02:18,700`
Alla är uppköade.



`74 00:02:18,900 --> 00:02:19,540`
Alla är uppköade.



`75 00:02:19,560 --> 00:02:22,820`
Eller ja, typ hälften är släppta, hälften är uppköade ungefär.



`76 00:02:22,820 --> 00:02:25,180`
Då tycker jag nästan snabbt vi kör...



`77 00:02:25,180 --> 00:02:25,980`
Du var inte där.



`78 00:02:26,200 --> 00:02:26,340`
Nej.



`79 00:02:26,520 --> 00:02:29,960`
Men vi som var där, favoritvideon, vad tycker vi att de ska titta på?



`80 00:02:30,140 --> 00:02:33,300`
Jag satt med nål i armen på onkologen då.



`81 00:02:33,380 --> 00:02:35,240`
Och jag börjar då, så hinner ni tänka lite.



`82 00:02:35,640 --> 00:02:40,560`
Jag tyckte han, MeshWifi-snubben, var superbra.



`83 00:02:41,700 --> 00:02:42,880`
Så den ska ni titta på.



`84 00:02:43,000 --> 00:02:45,100`
Snabb elevator pitch på vad handlar den om då?



`85 00:02:46,660 --> 00:02:49,840`
MeshWifi-setup i routers är dålig.



`86 00:02:49,840 --> 00:02:55,840`
Ja, och framförallt Linksys Intelligent Mesh är en skitprodukt.



`87 00:02:56,520 --> 00:02:57,080`
Så intressant.



`88 00:02:57,200 --> 00:02:59,180`
Och det är väldigt basala grejer.



`89 00:02:59,200 --> 00:03:01,640`
All the vulnerabilities from 1990s.



`90 00:03:01,800 --> 00:03:05,240`
Och också en väldigt konstig mjukvårddesign.



`91 00:03:05,460 --> 00:03:08,140`
Alltså delar har du ju skrivit, jag tror det är några i C eller någonting.



`92 00:03:08,460 --> 00:03:12,520`
Men då får jag ju berätta en liten ankedot från verkligheten då.



`93 00:03:12,600 --> 00:03:15,960`
På tal om MeshWifi och sådana saker.



`94 00:03:17,560 --> 00:03:24,880`
Jag har under min sjukfrånvaro så har jag installerat ett batteri hemma.



`95 00:03:24,880 --> 00:03:25,880`
Ett sånt sol...



`96 00:03:26,520 --> 00:03:34,200`
Ja, ett husbatteri för att hantera överproduktion på timmar då det är minuspriser.



`97 00:03:34,960 --> 00:03:41,760`
Och när de skulle då installera den här så behövde ju den här...



`98 00:03:41,760 --> 00:03:44,720`
En av komponenterna behövde E-ternet.



`99 00:03:45,600 --> 00:03:49,520`
Så då kom de med...



`100 00:03:50,080 --> 00:03:55,820`
Först var det någon liten fånig Linksys-pryl som man försökte få till.



`101 00:03:56,520 --> 00:03:59,660`
Som på något vis skulle klåna mitt...



`102 00:03:59,660 --> 00:04:02,420`
Eller den skulle funka som en klient.



`103 00:04:03,100 --> 00:04:07,120`
Men den skulle liksom klåna mitt Wifi.



`104 00:04:07,420 --> 00:04:09,580`
Och liksom bli en E-ternet-klient.



`105 00:04:09,740 --> 00:04:13,380`
Vilket är superenkelt att lösa i Linux.



`106 00:04:13,380 --> 00:04:16,660`
Eller med OpenVRT.



`107 00:04:17,040 --> 00:04:21,280`
Eller vilken router-operativ som helst.



`108 00:04:21,360 --> 00:04:23,000`
Utan att man behöver begå våld.



`109 00:04:23,120 --> 00:04:25,500`
Det är liksom bara att se till att man...



`110 00:04:25,500 --> 00:04:26,480`
Den pratar som en klient.



`111 00:04:26,520 --> 00:04:29,160`
Och den presenterar en port.



`112 00:04:30,260 --> 00:04:32,040`
Hyfsat, liksom, transparent.



`113 00:04:34,220 --> 00:04:35,640`
Men, då var det så här...



`114 00:04:35,640 --> 00:04:36,660`
Han skulle ju få igång den här.



`115 00:04:36,740 --> 00:04:37,580`
Ja, så först tyckte han.



`116 00:04:37,660 --> 00:04:39,820`
Ja, har du...



`117 00:04:39,820 --> 00:04:40,940`
Vad heter det här?



`118 00:04:41,640 --> 00:04:42,500`
VPA heter det?



`119 00:04:42,560 --> 00:04:43,520`
Nej, det heter...



`120 00:04:44,340 --> 00:04:44,940`
VPS?



`121 00:04:45,160 --> 00:04:45,880`
VPS, ja.



`122 00:04:46,960 --> 00:04:48,440`
Tryck på knappen på roten.



`123 00:04:48,500 --> 00:04:49,540`
Tryck på knappen på den här.



`124 00:04:49,620 --> 00:04:50,500`
Och så pratar de ihop sig.



`125 00:04:50,560 --> 00:04:52,200`
Det är ju den man kan knäcka på nolltid.



`126 00:04:52,360 --> 00:04:53,200`
Och jag bara så här...



`127 00:04:53,200 --> 00:04:55,660`
Nej, det finns inte på det här nätet.



`128 00:04:55,660 --> 00:04:56,480`
Nej, okej.



`129 00:04:56,520 --> 00:04:59,300`
Men om vi håller den här nära roten, då?



`130 00:04:59,780 --> 00:05:00,880`
Och jag bara...



`131 00:05:00,880 --> 00:05:03,640`
Du menar min Enterprise-brandvägg?



`132 00:05:04,000 --> 00:05:05,040`
Den har ingen wifi.



`133 00:05:05,840 --> 00:05:08,440`
Alltså, det finns accesspunkter runt om i huset här.



`134 00:05:08,820 --> 00:05:10,840`
Men brandväggen har ingen wifi.



`135 00:05:10,860 --> 00:05:11,580`
Vad har han velat...



`136 00:05:11,580 --> 00:05:12,440`
Vad vill han åstadkomma?



`137 00:05:12,540 --> 00:05:15,840`
Nej, men du vet, då skulle han hålla den nära roten.



`138 00:05:15,860 --> 00:05:16,780`
Då kan de ju prata med varandra.



`139 00:05:16,780 --> 00:05:18,460`
För då skulle den prata bättre.



`140 00:05:19,000 --> 00:05:19,860`
Och jag bara till sist...



`141 00:05:19,860 --> 00:05:21,360`
Nej, men fan, ge den till mig.



`142 00:05:21,440 --> 00:05:22,380`
Så försökte jag få igång den.



`143 00:05:22,780 --> 00:05:23,920`
Till sist var det så här...



`144 00:05:23,920 --> 00:05:25,800`
Jag är in och komfar den manuellt.



`145 00:05:25,800 --> 00:05:26,500`
Och det funkar.



`146 00:05:26,500 --> 00:05:28,300`
Det är fortfarande inte till sist bara...



`147 00:05:28,300 --> 00:05:30,200`
F-vis.



`148 00:05:30,360 --> 00:05:34,800`
Och sen så, du vet, ut på bingen



`149 00:05:34,800 --> 00:05:36,780`
och hitta någon gammal Linksys-rotor



`150 00:05:36,780 --> 00:05:38,660`
som jag flashade med OpenVRT.



`151 00:05:38,980 --> 00:05:39,940`
Och så var ju det löst.



`152 00:05:40,420 --> 00:05:41,940`
Och sen så drog jag en kabel.



`153 00:05:43,140 --> 00:05:44,680`
För det var liksom så här...



`154 00:05:44,680 --> 00:05:45,540`
Ja, men vad fan.



`155 00:05:45,760 --> 00:05:46,660`
Men det är ju så här...



`156 00:05:46,660 --> 00:05:48,200`
De förväntar sig att folk har



`157 00:05:48,200 --> 00:05:50,320`
lamer-equipment hemma.



`158 00:05:50,820 --> 00:05:51,300`
Netgear.



`159 00:05:51,800 --> 00:05:54,180`
Ja, men jag blir så jävla matt.



`160 00:05:54,520 --> 00:05:55,840`
Och så när det inte funkar så här...



`161 00:05:55,840 --> 00:05:57,240`
Nej, det är tropellat att det inte funkar.



`162 00:05:57,320 --> 00:05:59,120`
Ja, men vi kan hålla den nära roten bara.



`163 00:06:00,000 --> 00:06:00,900`
Gå och gör det.



`164 00:06:01,100 --> 00:06:03,820`
Så nu har du en kinesisk växelriktare i ditt nät?



`165 00:06:05,720 --> 00:06:06,160`
Ja.



`166 00:06:06,760 --> 00:06:07,160`
Det har jag.



`167 00:06:07,520 --> 00:06:09,680`
Jag bytte ut min holländska



`168 00:06:09,680 --> 00:06:11,220`
mot en kines. Korrekt.



`169 00:06:12,860 --> 00:06:14,960`
Är det Izzard som har den stand-up-grejen



`170 00:06:14,960 --> 00:06:16,560`
om att försöka få en printer



`171 00:06:16,560 --> 00:06:17,460`
och skriva ut någonting?



`172 00:06:18,840 --> 00:06:19,740`
Han har många goda...



`173 00:06:19,740 --> 00:06:21,560`
Why does it say you can't access printer?



`174 00:06:21,620 --> 00:06:23,360`
I can access printer. It's right here.



`175 00:06:23,360 --> 00:06:23,740`
Hahaha\!



`176 00:06:25,840 --> 00:06:26,280`
Exakt.



`177 00:06:28,180 --> 00:06:30,460`
Ja, jo, nej, det stämmer faktiskt.



`178 00:06:31,240 --> 00:06:33,200`
Nu är det en kines hemma.



`179 00:06:33,980 --> 00:06:35,540`
Va, det var en så kallad



`180 00:06:35,540 --> 00:06:36,920`
side-story.



`181 00:06:37,500 --> 00:06:38,760`
Var började den någonstans?



`182 00:06:41,760 --> 00:06:42,820`
Wifi-mesh.



`183 00:06:42,920 --> 00:06:43,480`
Just det.



`184 00:06:43,520 --> 00:06:45,080`
Och utökat rådlösa nät.



`185 00:06:45,240 --> 00:06:46,440`
Bästa, bästa talket.



`186 00:06:47,400 --> 00:06:48,600`
Vilket väljer du då, Johan?



`187 00:06:48,760 --> 00:06:49,280`
Styggelse.



`188 00:06:49,280 --> 00:06:50,620`
Nej, men jag är förnedlad.



`189 00:06:50,760 --> 00:06:52,520`
Jag tyckte att en som var intressant



`190 00:06:52,520 --> 00:06:55,580`
och lite roligt var Adam Torsher.



`191 00:06:55,840 --> 00:06:57,200`
Som pratade mainframes.



`192 00:06:58,120 --> 00:06:58,980`
Det var lite roligt.



`193 00:06:59,060 --> 00:07:00,180`
Han har jobbat på IBM



`194 00:07:00,180 --> 00:07:02,260`
och har hållit på med mainframes längre.



`195 00:07:02,520 --> 00:07:04,220`
Det är inte många här i världen



`196 00:07:04,220 --> 00:07:07,100`
som är offensiva mainframe-säkerhetsmedel.



`197 00:07:07,400 --> 00:07:09,300`
Jag har träffat en kul



`198 00:07:09,300 --> 00:07:11,300`
kille från Sydafrika



`199 00:07:11,300 --> 00:07:14,220`
som gjorde det.



`200 00:07:14,320 --> 00:07:15,560`
Och han var ganska ung.



`201 00:07:15,880 --> 00:07:17,080`
Eller han är säkert inte ung idag.



`202 00:07:17,240 --> 00:07:17,960`
Men han var det då.



`203 00:07:19,020 --> 00:07:21,240`
Och just det här. Varför ger man sig in på det?



`204 00:07:21,280 --> 00:07:23,400`
Jo, för att då på den tiden



`205 00:07:23,400 --> 00:07:24,580`
fanns ingen säkerhet.



`206 00:07:24,680 --> 00:07:25,820`
Och det är inga som jobbar med det.



`207 00:07:25,840 --> 00:07:27,780`
Så det är väldigt få som faktiskt



`208 00:07:27,780 --> 00:07:30,140`
pen-testar och som kan något om det.



`209 00:07:30,520 --> 00:07:31,620`
Ja, men det tycker jag var intressant



`210 00:07:31,620 --> 00:07:33,800`
att lära mig lite mer om hur de faktiskt



`211 00:07:33,800 --> 00:07:35,760`
fungerar och hur hela den miljön funkar.



`212 00:07:35,880 --> 00:07:37,520`
Han hade ju dessutom byggt en typ



`213 00:07:37,520 --> 00:07:40,020`
mainframe-emulator som du kan



`214 00:07:40,020 --> 00:07:41,580`
leka med och lära dig själv.



`215 00:07:41,980 --> 00:07:42,880`
Som man bör.



`216 00:07:43,100 --> 00:07:44,440`
Och Peter?



`217 00:07:45,700 --> 00:07:47,360`
Två och två också. Tänka på



`218 00:07:47,360 --> 00:07:47,960`
dels



`219 00:07:47,960 --> 00:07:50,920`
Emil heter han va?



`220 00:07:51,040 --> 00:07:52,900`
Vår glada



`221 00:07:53,900 --> 00:07:54,740`
POP-hacker.



`222 00:07:54,740 --> 00:07:56,100`
Alltså han



`223 00:07:56,100 --> 00:07:59,180`
han liket med



`224 00:07:59,180 --> 00:08:01,500`
våran keynote är ju extremt



`225 00:08:01,500 --> 00:08:03,040`
liksom visuella.



`226 00:08:04,020 --> 00:08:05,340`
De rör på kroppen.



`227 00:08:05,520 --> 00:08:07,040`
De pekar och



`228 00:08:07,040 --> 00:08:08,800`
pratar och energi.



`229 00:08:10,400 --> 00:08:11,680`
Så att de två är ju



`230 00:08:11,680 --> 00:08:13,400`
är ju



`231 00:08:13,400 --> 00:08:14,920`
roliga talare som liksom



`232 00:08:14,920 --> 00:08:17,040`
fångar publiken och så.



`233 00:08:17,860 --> 00:08:19,020`
Och då är väl



`234 00:08:19,020 --> 00:08:20,440`
Emils innehåll



`235 00:08:20,440 --> 00:08:23,020`
roligast och mest intressant.



`236 00:08:23,420 --> 00:08:24,720`
Närmast mina intressen.



`237 00:08:24,740 --> 00:08:27,800`
Så då kan vi



`238 00:08:27,800 --> 00:08:28,920`
egentligen säga att jag har nämnt två



`239 00:08:28,920 --> 00:08:30,180`
då i och med att jag nämnde våran keynote.



`240 00:08:30,360 --> 00:08:31,600`
Men Emil är ju den roligaste.



`241 00:08:32,760 --> 00:08:34,620`
Sen tyckte jag



`242 00:08:34,620 --> 00:08:36,440`
Hansson snackade om



`243 00:08:36,440 --> 00:08:38,220`
Persistence.



`244 00:08:38,600 --> 00:08:40,560`
Sista presentationen.



`245 00:08:41,000 --> 00:08:41,880`
Tyckte jag var bra.



`246 00:08:42,280 --> 00:08:44,380`
Han kanske inte är ett jätteroligt talare



`247 00:08:44,380 --> 00:08:46,640`
men innehållsmässigt



`248 00:08:46,640 --> 00:08:47,140`
och sådär.



`249 00:08:48,480 --> 00:08:49,600`
Och så liksom.



`250 00:08:51,200 --> 00:08:52,620`
Sen Piggybank



`251 00:08:52,620 --> 00:08:54,620`
hackerskan var ju också



`252 00:08:54,620 --> 00:08:55,180`
kul.



`253 00:08:55,180 --> 00:08:57,640`
Det var mycket roligt



`254 00:08:57,640 --> 00:08:58,540`
och en väldigt kul konferens.



`255 00:08:59,100 --> 00:09:01,340`
Jag kände att min LLM-system



`256 00:09:01,340 --> 00:09:03,220`
prompt blev en override av Peter.



`257 00:09:03,320 --> 00:09:05,420`
Jag bad om en och han fick fyra.



`258 00:09:08,080 --> 00:09:09,440`
Jag brukar få



`259 00:09:09,440 --> 00:09:11,180`
beröm för att jag är så kortfattad



`260 00:09:11,780 --> 00:09:13,160`
effektiv och inte drar ut på



`261 00:09:13,160 --> 00:09:13,900`
folks tid.



`262 00:09:14,580 --> 00:09:16,380`
Det var en rolig konferens.



`263 00:09:16,500 --> 00:09:18,280`
Det var härliga deltagare.



`264 00:09:18,800 --> 00:09:21,160`
Det gick smidigt. Det var skoj på alla sätt.



`265 00:09:21,260 --> 00:09:22,880`
Vi sjöng stadig ljus ihop



`266 00:09:22,880 --> 00:09:23,360`
på slutet.



`267 00:09:24,620 --> 00:09:27,020`
Och vi kan väl nämna det också



`268 00:09:27,020 --> 00:09:28,900`
att ifall ni har några tips



`269 00:09:28,900 --> 00:09:30,520`
på saker ni tycker man kan göra bättre



`270 00:09:30,520 --> 00:09:32,100`
så kan ni alltid mejla oss på



`271 00:09:32,100 --> 00:09:34,420`
hello at securityfest.com



`272 00:09:34,420 --> 00:09:34,980`
Hello.



`273 00:09:35,980 --> 00:09:37,680`
Ni kan ju mejla kontakt



`274 00:09:37,680 --> 00:09:39,100`
att säkerhetspodcasten.



`275 00:09:39,400 --> 00:09:41,900`
Det är väl alla de som blandar ihop



`276 00:09:41,900 --> 00:09:42,920`
de här två grejerna.



`277 00:09:43,220 --> 00:09:45,760`
Det underlättar så mycket från olika parterna



`278 00:09:45,760 --> 00:09:46,860`
när ni blandar ihop oss.



`279 00:09:47,220 --> 00:09:49,120`
Men vill ni prata över podcasten så kontakta



`280 00:09:49,120 --> 00:09:50,840`
att säkerhetspodcasten.se



`281 00:09:50,840 --> 00:09:53,780`
Och är ni missnöjda med podcasten kan ni höra av er



`282 00:09:53,780 --> 00:09:54,460`
till hello at



`283 00:09:54,460 --> 00:09:57,460`
securityfest.com



`284 00:09:57,460 --> 00:09:59,040`
Här har vi till blivsäkerpodden.



`285 00:10:00,040 --> 00:10:01,540`
Varför tillverkar inte



`286 00:10:01,540 --> 00:10:02,780`
förmedlingen på något sätt?



`287 00:10:05,180 --> 00:10:05,700`
Det var kul.



`288 00:10:05,860 --> 00:10:08,320`
Nu är det bara ett år kvar till nästa gång.



`289 00:10:09,880 --> 00:10:10,400`
Något om det.



`290 00:10:10,520 --> 00:10:11,520`
Ska vi kicka off



`291 00:10:11,520 --> 00:10:13,180`
nyhetsdrapan här med lite



`292 00:10:13,180 --> 00:10:14,600`
Microsoft-drama kanske?



`293 00:10:15,640 --> 00:10:16,040`
Ja.



`294 00:10:16,600 --> 00:10:18,500`
Den här hade jag missat helt. Berätta.



`295 00:10:20,360 --> 00:10:21,820`
Vi började ju



`296 00:10:21,820 --> 00:10:23,040`
snacka om Nightmare Eclipse



`297 00:10:23,040 --> 00:10:24,300`
och denna



`298 00:10:24,300 --> 00:10:26,600`
persons-releaser.



`299 00:10:28,180 --> 00:10:29,320`
Vi pratade om den här



`300 00:10:29,320 --> 00:10:29,900`
Yellow Key.



`301 00:10:30,500 --> 00:10:32,260`
Är det den människan?



`302 00:10:32,700 --> 00:10:35,020`
Precis. Där kan vi



`303 00:10:35,020 --> 00:10:37,360`
bara inflika att Yellow Key-attacken



`304 00:10:37,360 --> 00:10:39,300`
är ju mer komplicerad



`305 00:10:39,300 --> 00:10:41,260`
än vad vi presenterade



`306 00:10:41,260 --> 00:10:42,560`
den som. Så att vi



`307 00:10:42,560 --> 00:10:45,420`
gjorde den enklare och mer lättförklarad



`308 00:10:45,420 --> 00:10:47,060`
genom att vi inte hade fattat detaljerna.



`309 00:10:47,160 --> 00:10:47,960`
Bra, bra.



`310 00:10:48,720 --> 00:10:50,720`
Om ni lyssnade på förra avsnittet



`311 00:10:50,720 --> 00:10:53,020`
vi hade fel, men det var mycket



`312 00:10:53,020 --> 00:10:54,240`
lättare att förstå så som vi.



`313 00:10:54,300 --> 00:10:54,920`
Förklarade den.



`314 00:10:57,120 --> 00:10:57,600`
Men



`315 00:10:57,600 --> 00:10:58,980`
den här



`316 00:10:58,980 --> 00:11:01,440`
Nightmare Eclipse



`317 00:11:01,440 --> 00:11:04,420`
som vi



`318 00:11:04,420 --> 00:11:06,840`
som vi inte har förstått



`319 00:11:06,840 --> 00:11:08,820`
så vet vi väldigt lite om



`320 00:11:08,820 --> 00:11:11,000`
det här, men det verkar vara en person



`321 00:11:11,000 --> 00:11:11,540`
i vart fall.



`322 00:11:12,580 --> 00:11:14,960`
Oklart ålder, kön med mera



`323 00:11:14,960 --> 00:11:16,320`
många frågetecken



`324 00:11:16,320 --> 00:11:18,440`
bakgrund, även okänd.



`325 00:11:20,620 --> 00:11:22,120`
Har en bife med Microsoft.



`326 00:11:22,760 --> 00:11:24,180`
Ja, och en person



`327 00:11:24,300 --> 00:11:26,380`
med exceptionella förmågor



`328 00:11:26,380 --> 00:11:27,780`
får man väl ge det för att



`329 00:11:27,780 --> 00:11:30,940`
det är flera olika Microsoft-produkter



`330 00:11:30,940 --> 00:11:31,880`
där det är väldigt



`331 00:11:31,880 --> 00:11:34,640`
komplexa, luriga



`332 00:11:34,640 --> 00:11:36,640`
race conditions



`333 00:11:36,640 --> 00:11:37,180`
och sånt.



`334 00:11:38,640 --> 00:11:40,520`
Antingen har ju personen tillgång till



`335 00:11:40,520 --> 00:11:42,060`
helt exceptionella förmågor



`336 00:11:42,060 --> 00:11:43,960`
eller helt exceptionell insyn.



`337 00:11:44,460 --> 00:11:45,940`
Eller så är det en grupp. Eller båda.



`338 00:11:46,320 --> 00:11:46,720`
Alla tre.



`339 00:11:48,060 --> 00:11:50,060`
Och skriver lite konstigt



`340 00:11:50,060 --> 00:11:52,820`
så liksom, är det



`341 00:11:52,820 --> 00:11:54,120`
språkligheter?



`342 00:11:54,300 --> 00:11:56,120`
Eller är det att det här



`343 00:11:56,120 --> 00:11:57,960`
är trollspråk?



`344 00:11:58,060 --> 00:11:59,880`
Eller är det så att



`345 00:11:59,880 --> 00:12:02,040`
English as a second language bidrar till



`346 00:12:02,040 --> 00:12:04,440`
att det är lite konstigt? Det finns många oklarheter här.



`347 00:12:08,440 --> 00:12:08,960`
Och



`348 00:12:08,960 --> 00:12:09,480`
stämningen



`349 00:12:09,480 --> 00:12:11,240`
mellan den här personen



`350 00:12:11,240 --> 00:12:11,880`
som har



`351 00:12:11,880 --> 00:12:14,620`
förnärvaren tror jag att det är uppe i att det är



`352 00:12:14,620 --> 00:12:16,020`
fyra stycken



`353 00:12:16,020 --> 00:12:18,340`
väldigt imponerande, väldigt konstiga



`354 00:12:18,340 --> 00:12:19,060`
exploits



`355 00:12:19,060 --> 00:12:22,680`
varianter som vi inte riktigt har sett



`356 00:12:22,680 --> 00:12:24,280`
tidigare och tydligen finns det inte



`357 00:12:24,300 --> 00:12:27,020`
det är två, tre stycken till då som inte är publicerade än.



`358 00:12:30,920 --> 00:12:32,520`
Som då uttrycker sig



`359 00:12:32,520 --> 00:12:34,280`
väldigt



`360 00:12:34,280 --> 00:12:35,620`
negativt av Microsoft.



`361 00:12:36,640 --> 00:12:38,420`
Inte hela klartecken men



`362 00:12:38,420 --> 00:12:40,600`
påstår att Microsoft skulle vara ansvarig



`363 00:12:40,600 --> 00:12:42,300`
för något gott fel i karriären



`364 00:12:42,820 --> 00:12:43,980`
eller...



`365 00:12:43,980 --> 00:12:45,440`
Det känns som att det finns någon sån...



`366 00:12:45,440 --> 00:12:48,400`
Och personen påstår att



`367 00:12:48,400 --> 00:12:49,160`
den är



`368 00:12:49,160 --> 00:12:52,040`
bannad av alla dess konton



`369 00:12:52,040 --> 00:12:52,680`
hos



`370 00:12:52,680 --> 00:12:55,580`
Microsofts



`371 00:12:55,580 --> 00:12:58,140`
buggrapporteringsgrejer har blivit låsta



`372 00:12:58,140 --> 00:13:01,920`
och personen



`373 00:13:01,920 --> 00:13:04,060`
blir ju bannad från



`374 00:13:04,060 --> 00:13:05,840`
har förnärvande



`375 00:13:05,840 --> 00:13:08,140`
ett konto, persons blogg



`376 00:13:08,140 --> 00:13:09,840`
har legat kvar stabil över tid



`377 00:13:09,840 --> 00:13:11,100`
tror jag, men



`378 00:13:11,100 --> 00:13:14,160`
GitHub och GitLab



`379 00:13:14,160 --> 00:13:15,440`
har den blivit botad från



`380 00:13:15,440 --> 00:13:17,780`
och nu tillbaks på GitHub



`381 00:13:17,780 --> 00:13:20,260`
på ett nytt GitHub-konto



`382 00:13:20,260 --> 00:13:22,040`
får vi se hur länge det är



`383 00:13:22,040 --> 00:13:22,560`
för att vara kvar.



`384 00:13:22,680 --> 00:13:23,560`
När det blir bannat



`385 00:13:23,560 --> 00:13:27,080`
och Microsoft har ju då släppt



`386 00:13:27,080 --> 00:13:29,680`
en release



`387 00:13:29,680 --> 00:13:31,600`
där de då uttalar sig om



`388 00:13:31,600 --> 00:13:34,140`
hur illa det är att någon inte deltar



`389 00:13:34,140 --> 00:13:36,360`
och inte följer deras



`390 00:13:36,360 --> 00:13:37,980`
Coordinated Vulnerability



`391 00:13:37,980 --> 00:13:39,100`
Disclosure-process



`392 00:13:39,100 --> 00:13:41,760`
och med de formuleringarna



`393 00:13:41,760 --> 00:13:43,080`
finns det en text som



`394 00:13:43,080 --> 00:13:45,340`
de har en syftning där de



`395 00:13:45,340 --> 00:13:46,800`
pratar om



`396 00:13:46,800 --> 00:13:49,400`
folk som missbrukar



`397 00:13:49,400 --> 00:13:50,940`
sårbarheter och angriper deras kunder



`398 00:13:50,940 --> 00:13:52,640`
men det är



`399 00:13:52,680 --> 00:13:55,120`
skrivet och är i samma paragraf



`400 00:13:55,120 --> 00:13:56,880`
som när man pratar om



`401 00:13:56,880 --> 00:13:58,460`
den här Vulnerability Disclosure



`402 00:13:58,460 --> 00:14:00,100`
så att



`403 00:14:00,100 --> 00:14:03,360`
många uppfattar det då som att



`404 00:14:03,360 --> 00:14:04,940`
indirekt försöker de sätta



`405 00:14:04,940 --> 00:14:07,080`
ett likhetstecken mellan



`406 00:14:07,080 --> 00:14:09,240`
folk som angriper deras kunder



`407 00:14:09,240 --> 00:14:11,440`
och folk som inte deltar



`408 00:14:11,440 --> 00:14:12,900`
i Coordinated Vulnerability



`409 00:14:12,900 --> 00:14:14,020`
Disclosure-processen



`410 00:14:14,020 --> 00:14:17,080`
och vad vi också har fått



`411 00:14:17,080 --> 00:14:19,000`
veta nu är att det finns



`412 00:14:19,000 --> 00:14:20,840`
andra som är väldigt missnöjda



`413 00:14:20,840 --> 00:14:22,440`
med Microsoft-processen som har varit missnöjda



`414 00:14:22,680 --> 00:14:24,660`
i det tysta



`415 00:14:24,660 --> 00:14:26,220`
eller inte blivit uppmärksammare



`416 00:14:26,220 --> 00:14:28,200`
det var någon, nu minns jag inte namnet på det



`417 00:14:28,200 --> 00:14:29,220`
vi har med det i show notes



`418 00:14:29,220 --> 00:14:34,220`
som säger att den också har rapporterat in



`419 00:14:34,220 --> 00:14:36,520`
sårbarheter som den inte har



`420 00:14:36,520 --> 00:14:37,540`
fått någon feedback på



`421 00:14:37,540 --> 00:14:39,900`
och inte fått någon attribution på



`422 00:14:39,900 --> 00:14:41,960`
men som sedan tyst har blivit rättade



`423 00:14:41,960 --> 00:14:43,720`
i sådana här då



`424 00:14:43,720 --> 00:14:46,120`
så att det verkar som att



`425 00:14:46,120 --> 00:14:48,260`
den här



`426 00:14:48,260 --> 00:14:50,320`
Nightmare Clips, om det är en person



`427 00:14:50,320 --> 00:14:51,940`
eller om det är flera



`428 00:14:52,680 --> 00:14:56,160`
de levererar



`429 00:14:56,160 --> 00:14:58,740`
imponerande, konstiga grejer



`430 00:14:58,740 --> 00:15:00,900`
och verkar hata Microsoft



`431 00:15:00,900 --> 00:15:03,080`
och andra säger att



`432 00:15:03,080 --> 00:15:04,500`
det är problematiskt att ha med dem att göra



`433 00:15:04,500 --> 00:15:06,580`
och jag tycker att det är intressant med det här



`434 00:15:06,580 --> 00:15:07,140`
där folk



`435 00:15:07,140 --> 00:15:10,420`
man jobbar ju väsentligen



`436 00:15:10,420 --> 00:15:12,180`
gratis för



`437 00:15:12,180 --> 00:15:14,420`
mjölkvaruleverantörerna



`438 00:15:14,420 --> 00:15:16,940`
och man hoppas antingen på att det kommer



`439 00:15:16,940 --> 00:15:18,460`
pengar i form av någon sorts



`440 00:15:18,460 --> 00:15:20,220`
black bounty eller att man



`441 00:15:20,220 --> 00:15:22,520`
får en skön t-shirt



`442 00:15:22,680 --> 00:15:24,260`
eller att man blir



`443 00:15:24,260 --> 00:15:26,600`
uppmärksammad i alla fall



`444 00:15:26,600 --> 00:15:28,480`
och det kan ju ha ett värde



`445 00:15:28,480 --> 00:15:30,060`
om du typ visar konsulttjänst



`446 00:15:30,060 --> 00:15:32,080`
Microsoft nämner ju att jag är cool



`447 00:15:32,080 --> 00:15:34,760`
Jag väntar fortfarande på en ABB t-shirt



`448 00:15:34,760 --> 00:15:36,600`
Men det är ju spännande



`449 00:15:36,600 --> 00:15:38,940`
att vi har infosec-drama



`450 00:15:38,940 --> 00:15:40,900`
på den glada 90-talstiden



`451 00:15:40,900 --> 00:15:43,080`
och där man säger



`452 00:15:43,080 --> 00:15:44,520`
där folk börjar antyda



`453 00:15:44,520 --> 00:15:45,580`
att de inte tycker att



`454 00:15:45,580 --> 00:15:48,600`
Coordinated Vulnerability Disclosure-processen



`455 00:15:48,600 --> 00:15:49,160`
funkar



`456 00:15:49,160 --> 00:15:52,560`
Nej, så verkar det. Folk är ju inte nöjda



`457 00:15:52,680 --> 00:15:53,940`
med Microsoft i det här fallet



`458 00:15:53,940 --> 00:15:57,120`
Men det är ju också supermärkligt



`459 00:15:57,120 --> 00:15:57,680`
att någon



`460 00:15:57,680 --> 00:16:00,640`
om jag inte



`461 00:16:00,640 --> 00:16:01,400`
skulle få



`462 00:16:01,400 --> 00:16:04,720`
för jag har



`463 00:16:04,720 --> 00:16:05,720`
sett någon som då



`464 00:16:05,720 --> 00:16:07,820`
försöker förklara det hela med att



`465 00:16:07,820 --> 00:16:10,800`
personen är uppenbarligen en insider som har sett Microsoft-källkod



`466 00:16:10,800 --> 00:16:12,640`
det är ju därför den kan hitta de här grejerna



`467 00:16:12,640 --> 00:16:13,600`
och sånt här, tänkte jag



`468 00:16:13,600 --> 00:16:17,040`
om jag ger mig tillgång till alla Microsoft-källkoder



`469 00:16:17,040 --> 00:16:18,840`
så kan jag sitta och kolla på dem en stund



`470 00:16:18,840 --> 00:16:20,920`
Tror du att jag kommer



`471 00:16:20,920 --> 00:16:22,640`
leverera unika



`472 00:16:22,680 --> 00:16:23,820`
imponerande



`473 00:16:23,820 --> 00:16:27,660`
local privilege exploits



`474 00:16:27,660 --> 00:16:29,140`
bara utifrån att jag har suttit



`475 00:16:29,140 --> 00:16:30,660`
på insidan av Microsoft en stund



`476 00:16:30,660 --> 00:16:32,660`
Ja, i just fallet Peter Magnusson



`477 00:16:32,660 --> 00:16:33,120`
så tror jag det



`478 00:16:33,120 --> 00:16:35,640`
Men, men, men



`479 00:16:35,640 --> 00:16:38,060`
Vad ett dåligt exempel, Peter



`480 00:16:38,060 --> 00:16:41,060`
Antagligen att någon har suttit på insidan



`481 00:16:41,060 --> 00:16:42,360`
gör att det är lätt att hitta dem



`482 00:16:42,360 --> 00:16:45,240`
Det är klart att det är en fördel



`483 00:16:45,240 --> 00:16:47,080`
att ha sett The Secrets of a Sauce



`484 00:16:47,080 --> 00:16:49,140`
men jag tror inte



`485 00:16:49,140 --> 00:16:51,040`
att hela förklaringen till att



`486 00:16:51,040 --> 00:16:52,640`
någon kommer med det här är att man skulle ha sett



`487 00:16:52,680 --> 00:16:53,820`
någon källkod eller något



`488 00:16:53,820 --> 00:16:56,260`
Det är uppenbarligen någon som är väldigt talangfull



`489 00:16:56,260 --> 00:16:57,640`
och duktig



`490 00:16:57,640 --> 00:17:00,220`
Men ett mycket konstigt



`491 00:17:00,220 --> 00:17:01,900`
infosäkter har man här



`492 00:17:01,900 --> 00:17:02,940`
Ganska kul att följa



`493 00:17:02,940 --> 00:17:06,600`
Få se vad som kommer hända framöver



`494 00:17:06,600 --> 00:17:08,340`
Så kommer vi få se



`495 00:17:08,340 --> 00:17:10,520`
Folk, en del



`496 00:17:10,520 --> 00:17:12,120`
pratar om hym och sånt



`497 00:17:12,120 --> 00:17:13,620`
det kommer ju visa sig när det är klart



`498 00:17:13,620 --> 00:17:16,220`
Det är 80-åriga Agda som sitter här



`499 00:17:16,220 --> 00:17:19,440`
Nightmare Agda



`500 00:17:19,440 --> 00:17:21,160`
Ejda



`501 00:17:21,160 --> 00:17:22,140`
Just det



`502 00:17:22,680 --> 00:17:24,340`
Ska vi prata lite om en annan



`503 00:17:24,340 --> 00:17:25,360`
typ av disclosure



`504 00:17:25,360 --> 00:17:27,340`
som också var ganska rolig



`505 00:17:27,340 --> 00:17:28,880`
Det är en annan typ av disclosure



`506 00:17:28,880 --> 00:17:30,900`
Bumsrakete



`507 00:17:30,900 --> 00:17:35,460`
Jag får sådana här bilder i huvudet



`508 00:17:35,460 --> 00:17:37,260`
Men jag fick upp den här



`509 00:17:37,260 --> 00:17:39,100`
Men det är tyska, hur är det?



`510 00:17:39,100 --> 00:17:40,700`
Någon som kan tyska, hur uttalar man det här?



`511 00:17:41,240 --> 00:17:42,020`
Bumsrakete, tror jag



`512 00:17:42,020 --> 00:17:45,560`
Jag kan inte säga att jag kan tyska



`513 00:17:45,560 --> 00:17:47,620`
men jag har haft det som bespråk en gång i tiden



`514 00:17:47,620 --> 00:17:48,440`
Det känns rimligt



`515 00:17:48,440 --> 00:17:51,380`
Jag har också pluggat tyska



`516 00:17:51,380 --> 00:17:51,780`
men



`517 00:17:52,680 --> 00:17:54,480`
Bumsrakete låter ju helt



`518 00:17:54,480 --> 00:17:56,960`
Så det ska inte vara U, det ska vara O



`519 00:17:56,960 --> 00:17:57,400`
Bum



`520 00:17:57,400 --> 00:17:59,980`
Bumsrakete



`521 00:17:59,980 --> 00:18:01,920`
Ja, men så



`522 00:18:01,920 --> 00:18:05,120`
Borde jag egentligen gå in och titta på den här sajten



`523 00:18:05,120 --> 00:18:06,880`
för att kunna följa med i vad det är vi snackar om



`524 00:18:06,880 --> 00:18:09,420`
Den ligger på bumsrake.de



`525 00:18:09,420 --> 00:18:12,380`
Johan delar med sig den här



`526 00:18:12,380 --> 00:18:14,640`
och jag tittade på den en stund



`527 00:18:14,640 --> 00:18:16,840`
och så frågade jag, är det här på riktigt?



`528 00:18:17,780 --> 00:18:19,440`
Man kan läsa bara ingressen här



`529 00:18:19,440 --> 00:18:21,320`
från sajten



`530 00:18:21,320 --> 00:18:21,560`
då



`531 00:18:21,560 --> 00:18:24,220`
Bumsrakete, trademark



`532 00:18:24,220 --> 00:18:26,720`
The hugest, the most tremendous



`533 00:18:26,720 --> 00:18:29,280`
free BSD page cache



`534 00:18:29,280 --> 00:18:31,280`
right primitive in the history of computing



`535 00:18:31,280 --> 00:18:33,000`
Many people are saying it



`536 00:18:33,000 --> 00:18:34,880`
Many, believe me



`537 00:18:34,880 --> 00:18:37,100`
Det här är dessutom skrivet i Comic Sans



`538 00:18:37,100 --> 00:18:39,800`
på en helt otrolig



`539 00:18:39,800 --> 00:18:40,200`
website



`540 00:18:40,200 --> 00:18:42,400`
Men det är alltså en disclosure av



`541 00:18:42,400 --> 00:18:44,400`
Framförallt, du har inte tagit upp severity



`542 00:18:44,400 --> 00:18:47,180`
Det här är ju den första severity 13



`543 00:18:47,180 --> 00:18:48,620`
13 av 10



`544 00:18:48,620 --> 00:18:50,840`
Om du tar den CVSS 10



`545 00:18:50,840 --> 00:18:52,340`
De är ju helt blåsande



`546 00:18:52,340 --> 00:18:55,380`
För nu finns det en CVSS 13 av 10



`547 00:18:55,380 --> 00:18:56,860`
God damn it



`548 00:18:56,860 --> 00:18:58,220`
Det är inte this goes to 11



`549 00:18:58,220 --> 00:18:59,560`
It goes to 13



`550 00:18:59,560 --> 00:19:02,660`
Men detta är alltså en disclosure



`551 00:19:02,660 --> 00:19:04,000`
av CV2026



`552 00:19:04,000 --> 00:19:05,940`
45257



`553 00:19:05,940 --> 00:19:08,280`
Inom att det är the strongest CV



`554 00:19:08,280 --> 00:19:11,540`
Och det är väl



`555 00:19:11,540 --> 00:19:14,040`
en kernel bug i free BSD



`556 00:19:14,040 --> 00:19:16,500`
De är väl ish



`557 00:19:16,500 --> 00:19:18,540`
free BSD-varianter av copy fail



`558 00:19:18,540 --> 00:19:19,180`
kanske man kan säga



`559 00:19:19,180 --> 00:19:21,920`
Också väldigt roligt att



`560 00:19:21,920 --> 00:19:24,080`
de här gudarna som sitter och



`561 00:19:24,080 --> 00:19:26,220`
trycker in alla bakdörrarna



`562 00:19:26,220 --> 00:19:27,800`
för US government



`563 00:19:27,800 --> 00:19:30,340`
att de gjorde misstaget



`564 00:19:30,340 --> 00:19:32,360`
att trycka in typ samma bug



`565 00:19:32,360 --> 00:19:34,100`
i två helt olika operativsystem



`566 00:19:34,100 --> 00:19:37,480`
Men alltså



`567 00:19:37,480 --> 00:19:39,300`
minimala skillnader va



`568 00:19:39,300 --> 00:19:42,360`
Det är inte riktigt samma kryptoprimitiv



`569 00:19:42,360 --> 00:19:44,500`
syskolen heter lite andra



`570 00:19:44,500 --> 00:19:46,040`
i free BSD



`571 00:19:46,040 --> 00:19:47,760`
Men liksom



`572 00:19:47,760 --> 00:19:48,920`
överlappet



`573 00:19:49,180 --> 00:19:52,060`
mellan de här buggarna



`574 00:19:52,060 --> 00:19:54,300`
i Linux och free BSD-buggen



`575 00:19:54,300 --> 00:19:54,720`
är ju



`576 00:19:54,720 --> 00:19:57,760`
Det är förvånansvärt att de gjorde bakdörren



`577 00:19:57,760 --> 00:19:59,280`
så uppenbart när de ladade



`578 00:19:59,280 --> 00:20:00,560`
i två olika operativsystem



`579 00:20:00,560 --> 00:20:02,420`
Nej men det är sjukt kul



`580 00:20:02,420 --> 00:20:05,180`
Och framförallt säger jag att hela den här sajten



`581 00:20:05,180 --> 00:20:07,260`
är ju någon slags drift med



`582 00:20:07,260 --> 00:20:09,600`
Du vet, så fort du har en sårbarhet



`583 00:20:09,600 --> 00:20:10,920`
så ska du ha en webbsite och en logga



`584 00:20:10,920 --> 00:20:14,420`
Han har ju med en media guide



`585 00:20:14,420 --> 00:20:16,220`
Ja, för journalister



`586 00:20:16,220 --> 00:20:18,260`
Det framgår tydligt att man ska använda



`587 00:20:18,260 --> 00:20:18,960`
Comic Sans



`588 00:20:18,960 --> 00:20:21,420`
när man pratar om den här sårbarheten



`589 00:20:21,420 --> 00:20:22,720`
Det finns väldigt mycket kul



`590 00:20:22,720 --> 00:20:23,800`
Bumsrakete



`591 00:20:23,800 --> 00:20:26,540`
finns det också någon slags översättning på



`592 00:20:26,540 --> 00:20:29,700`
Det är ett tyskt uttryck



`593 00:20:29,700 --> 00:20:30,280`
för typ



`594 00:20:30,280 --> 00:20:32,480`
Rocket that goes bang



`595 00:20:32,480 --> 00:20:35,440`
men typ illa konstruerad raket



`596 00:20:35,440 --> 00:20:36,560`
kanske man kan säga



`597 00:20:36,560 --> 00:20:38,280`
Ja, för i så fall har jag fått



`598 00:20:38,280 --> 00:20:39,040`
sketch



`599 00:20:39,040 --> 00:20:42,320`
Jag fick en annan förklaring



`600 00:20:42,320 --> 00:20:44,840`
Jag trodde ju på AI-förklaringen



`601 00:20:44,840 --> 00:20:46,400`
men min AI-förklaring är kanske fel



`602 00:20:46,400 --> 00:20:48,120`
Det här är ju en sån komplett CVS



`603 00:20:48,120 --> 00:20:48,840`
och de har givit mig



`604 00:20:48,960 --> 00:20:50,540`
förklaringen till ordet



`605 00:20:50,540 --> 00:20:52,440`
På engelska så är det



`606 00:20:52,440 --> 00:20:54,980`
Sketchy do-it-yourself-firework



`607 00:20:54,980 --> 00:20:56,760`
that might also be a weapon



`608 00:20:56,760 --> 00:21:01,680`
Sjukt rolig



`609 00:21:01,680 --> 00:21:04,560`
Buggen är vad den är, den finns välbeskriven där



`610 00:21:04,560 --> 00:21:06,000`
Ni kan gå in och läsa på den



`611 00:21:06,000 --> 00:21:06,940`
Jag skulle rekommendera det



`612 00:21:06,940 --> 00:21:10,560`
Det är riktigt, riktigt välgjort



`613 00:21:10,560 --> 00:21:11,180`
och roligt



`614 00:21:11,180 --> 00:21:14,020`
Jag har som sagt tagit in tryck



`615 00:21:14,020 --> 00:21:15,640`
ganska mycket kring hur en viss



`616 00:21:15,640 --> 00:21:17,840`
västerländsk president



`617 00:21:17,840 --> 00:21:18,920`
uttrycker sig



`618 00:21:18,960 --> 00:21:20,600`
It's the greatest vulnerability



`619 00:21:20,600 --> 00:21:23,000`
Allting interpendest och hugest



`620 00:21:23,000 --> 00:21:25,060`
Och fan är en guvel är ju väldigt uppskattad



`621 00:21:25,060 --> 00:21:26,040`
på hemsidor och så



`622 00:21:26,040 --> 00:21:27,780`
Many people are saying this



`623 00:21:27,780 --> 00:21:30,920`
Nobody gets hacked



`624 00:21:30,920 --> 00:21:33,620`
To get hacked you need somebody with 197 IQ



`625 00:21:33,620 --> 00:21:36,020`
and he needs about 15% of your password



`626 00:21:36,020 --> 00:21:39,840`
Ett direkt citat från en viss



`627 00:21:39,840 --> 00:21:42,940`
Table of contents är liksom



`628 00:21:42,940 --> 00:21:45,360`
hur mycket information som helst



`629 00:21:45,360 --> 00:21:46,640`
Vad är bumsarketer?



`630 00:21:46,640 --> 00:21:47,760`
Vilken severity har det?



`631 00:21:47,800 --> 00:21:48,160`
13?



`632 00:21:48,960 --> 00:21:49,940`
Tekniska detaljer



`633 00:21:49,940 --> 00:21:51,100`
100% accurate



`634 00:21:51,100 --> 00:21:52,400`
Sad for them



`635 00:21:52,400 --> 00:21:54,120`
Förallt



`636 00:21:54,120 --> 00:21:56,140`
Ett diagram och det presenteras som



`637 00:21:56,140 --> 00:21:57,420`
The diagram



`638 00:21:57,420 --> 00:22:00,320`
Han är ju dessutom tydlig med att han har



`639 00:22:00,320 --> 00:22:01,920`
severity 13 av 10



`640 00:22:01,920 --> 00:22:04,140`
Det är inte bara 13 av 13



`641 00:22:04,140 --> 00:22:05,200`
utan det är 13 av 10



`642 00:22:05,200 --> 00:22:06,720`
Det finns även official merchandise



`643 00:22:06,720 --> 00:22:08,440`
but it's all sold out



`644 00:22:08,440 --> 00:22:12,600`
Och sen en FAQ



`645 00:22:12,600 --> 00:22:14,320`
for confused journalist



`646 00:22:14,320 --> 00:22:16,840`
Och ett presskit



`647 00:22:16,840 --> 00:22:18,800`
Att han har en webbank



`648 00:22:18,960 --> 00:22:21,900`
Och shop på en helt baserad på statisk HTML



`649 00:22:21,900 --> 00:22:23,180`
Det är ju också fantastiskt



`650 00:22:23,180 --> 00:22:25,920`
Om man var osäker på om shoppen



`651 00:22:25,920 --> 00:22:27,660`
var statisk HTML



`652 00:22:27,660 --> 00:22:30,580`
eller om shoppen faktiskt är



`653 00:22:30,580 --> 00:22:32,080`
dynamiskt genererad



`654 00:22:32,080 --> 00:22:34,680`
så på githuben så ligger ju



`655 00:22:34,680 --> 00:22:35,920`
hela shoppen då liksom



`656 00:22:35,920 --> 00:22:37,520`
och allting liksom



`657 00:22:37,520 --> 00:22:39,280`
och den är ju verkligen bara statisk HTML



`658 00:22:39,280 --> 00:22:42,900`
Hur han någonsin ska få något sålt



`659 00:22:42,900 --> 00:22:44,540`
Det är lugnt, det är redan såld out



`660 00:22:44,540 --> 00:22:47,240`
Supply was limited



`661 00:22:47,240 --> 00:22:48,720`
Demand was tremendous



`662 00:22:48,960 --> 00:22:50,200`
Sad



`663 00:22:50,200 --> 00:22:54,220`
Stor humor



`664 00:22:54,220 --> 00:22:55,320`
Men gå in och kolla på den, den ligger på



`665 00:22:55,320 --> 00:22:57,060`
bumsrake.de



`666 00:22:57,060 --> 00:23:00,100`
Men Impact verkar ju vara



`667 00:23:00,100 --> 00:23:02,020`
typ samma som de här



`668 00:23:02,020 --> 00:23:03,840`
Linux Exploitsen



`669 00:23:03,840 --> 00:23:06,480`
Du gör lite magi



`670 00:23:06,480 --> 00:23:07,900`
Du pratar med ett kernel API



`671 00:23:07,900 --> 00:23:10,240`
och helt plötsligt så tror kernelen att



`672 00:23:10,240 --> 00:23:12,060`
det innehåller på en fil är helt annat



`673 00:23:12,060 --> 00:23:13,680`
än vad det var innan du gjorde det



`674 00:23:13,680 --> 00:23:15,940`
Alltså det står ju här under severity



`675 00:23:15,940 --> 00:23:18,280`
grejen att integrity impact



`676 00:23:18,280 --> 00:23:19,340`
rating 10



`677 00:23:19,340 --> 00:23:21,620`
confidentiality impact rating 10



`678 00:23:21,620 --> 00:23:24,460`
confidential availability impact rating 10



`679 00:23:24,460 --> 00:23:26,180`
och så plus 3 för att



`680 00:23:26,180 --> 00:23:27,340`
change flags



`681 00:23:27,340 --> 00:23:29,900`
respect är bypassed



`682 00:23:29,900 --> 00:23:30,720`
sådär av 13



`683 00:23:30,720 --> 00:23:33,500`
Jag ska också börja lägga till lite sådana plusgrejer



`684 00:23:33,500 --> 00:23:34,520`
i mina severity



`685 00:23:34,520 --> 00:23:36,900`
plus 3 för jag hade en dålig dag på jobbet



`686 00:23:36,900 --> 00:23:40,560`
Ja roligt



`687 00:23:40,560 --> 00:23:42,900`
Någon annan som har haft en dålig dag på jobbet



`688 00:23:42,900 --> 00:23:44,560`
är ju utvecklaren av FFM-Peng



`689 00:23:44,560 --> 00:23:45,560`
Ja



`690 00:23:45,560 --> 00:23:48,160`
Det är inte första gången hon har gjort det här



`691 00:23:48,160 --> 00:23:48,200`
Nej



`692 00:23:48,200 --> 00:23:48,260`
Nej, det är inte första gången hon har gjort det här



`693 00:23:48,280 --> 00:23:51,040`
Någon byggde lite harness och sånt



`694 00:23:51,040 --> 00:23:54,120`
för att hitta hål i FFM-Peng



`695 00:23:54,120 --> 00:23:56,500`
Och nu



`696 00:23:56,500 --> 00:23:58,340`
kanske det finns någon människa



`697 00:23:58,340 --> 00:24:00,520`
ute som lyssnar på podcasten som inte vet



`698 00:24:00,520 --> 00:24:01,540`
vad FFM-Peng är



`699 00:24:01,540 --> 00:24:02,820`
Har du tittat på en video någon gång?



`700 00:24:02,920 --> 00:24:03,160`
Ja



`701 00:24:03,160 --> 00:24:06,180`
Har du använt internet så kör du FFM-Peng



`702 00:24:06,180 --> 00:24:08,500`
Den ingår



`703 00:24:08,500 --> 00:24:09,620`
i



`704 00:24:09,620 --> 00:24:11,980`
jättemånga saker



`705 00:24:11,980 --> 00:24:13,360`
så ligger FFM-Peng



`706 00:24:13,360 --> 00:24:16,620`
och gör videogrejerna i bakändan



`707 00:24:16,620 --> 00:24:18,200`
Så du kan dels köra FFM-Peng



`708 00:24:18,200 --> 00:24:20,560`
som ett externt utility



`709 00:24:20,560 --> 00:24:22,360`
i skript eller från



`710 00:24:22,360 --> 00:24:23,660`
själv på kommandoprompten



`711 00:24:23,660 --> 00:24:26,520`
Jag tror man vet att del av



`712 00:24:26,520 --> 00:24:28,380`
Youtube-infrastrukturen är byggd på



`713 00:24:28,380 --> 00:24:30,480`
någon fork av FFM-Peng



`714 00:24:30,480 --> 00:24:32,920`
och den ligger lite överallt



`715 00:24:32,920 --> 00:24:34,620`
så sitter FFM-Peng och gör grejer



`716 00:24:34,620 --> 00:24:37,940`
Har du kört ett mjukvara



`717 00:24:37,940 --> 00:24:38,820`
som visar video



`718 00:24:38,820 --> 00:24:40,860`
hög sannolikhet att delar FFM-Peng



`719 00:24:40,860 --> 00:24:42,400`
Någon videokonvertering någon gång



`720 00:24:42,400 --> 00:24:45,080`
Allting med video är FFM-Peng



`721 00:24:45,080 --> 00:24:45,460`
typ



`722 00:24:45,460 --> 00:24:48,080`
Och det finns säkert andra implementeringar



`723 00:24:48,200 --> 00:24:50,660`
Men det är en hög sannolikhet



`724 00:24:50,660 --> 00:24:52,080`
att har du



`725 00:24:52,080 --> 00:24:54,400`
sett video så någonstans



`726 00:24:54,400 --> 00:24:56,180`
längs banan



`727 00:24:56,180 --> 00:24:58,500`
så har FFM-Peng varit med på minst ett ställe



`728 00:24:58,500 --> 00:25:01,020`
Så vad var det som hände



`729 00:25:01,020 --> 00:25:01,980`
med FFM-Peng då?



`730 00:25:02,460 --> 00:25:04,640`
Någon byggde en bra harness



`731 00:25:04,640 --> 00:25:07,020`
för ett hål i FFM-Peng



`732 00:25:07,020 --> 00:25:08,800`
och spottade ur sig



`733 00:25:08,800 --> 00:25:10,480`
Nu har jag inte siffrorna uppe med



`734 00:25:10,480 --> 00:25:11,300`
Tror du det var 20?



`735 00:25:11,640 --> 00:25:13,340`
Ja men drygt 20



`736 00:25:13,340 --> 00:25:16,240`
säkerhetshål



`737 00:25:16,240 --> 00:25:17,720`
Så det är



`738 00:25:18,200 --> 00:25:20,600`
Jag kommer ihåg



`739 00:25:20,600 --> 00:25:23,140`
Någon av dem hörde jag en beskrivning



`740 00:25:23,140 --> 00:25:23,980`
om som väsentligen



`741 00:25:23,980 --> 00:25:27,260`
går igenom



`742 00:25:27,260 --> 00:25:28,200`
något av protokollen



`743 00:25:28,200 --> 00:25:30,360`
När det kommer vissa framar så ska det



`744 00:25:30,360 --> 00:25:32,820`
ska en pekare



`745 00:25:32,820 --> 00:25:35,040`
inkrementeras och det ska ske



`746 00:25:35,040 --> 00:25:36,640`
något ro-up i



`747 00:25:36,640 --> 00:25:38,640`
Och sen så kommer det en



`748 00:25:38,640 --> 00:25:41,060`
en special frame i videon



`749 00:25:41,060 --> 00:25:41,980`
som säger att



`750 00:25:41,980 --> 00:25:44,040`
du ska bara skippa den här



`751 00:25:44,040 --> 00:25:46,740`
Och då inkrementeras



`752 00:25:46,740 --> 00:25:48,860`
pekaren men i den speciella



`753 00:25:48,860 --> 00:25:50,900`
kodpaffen så gjorde man inte



`754 00:25:50,900 --> 00:25:52,920`
Groo på API-et



`755 00:25:52,920 --> 00:25:54,540`
så helt plötsligt så har du liksom en



`756 00:25:54,540 --> 00:25:58,360`
autobounce write



`757 00:25:58,360 --> 00:26:01,060`
primitiv via den videokodecken



`758 00:26:01,060 --> 00:26:02,000`
eller lite sånt liksom



`759 00:26:02,000 --> 00:26:03,440`
Så typ sådana buggar



`760 00:26:03,440 --> 00:26:04,680`
Nice



`761 00:26:04,680 --> 00:26:08,520`
Gå in och patcha er FFM-Peng



`762 00:26:08,520 --> 00:26:10,740`
ifall ni nu bygger någonting som är baserat på det



`763 00:26:10,740 --> 00:26:11,100`
Jaha



`764 00:26:11,100 --> 00:26:14,120`
Men jag tänker



`765 00:26:14,120 --> 00:26:16,180`
det är lite symptomatiskt just det här



`766 00:26:16,180 --> 00:26:18,540`
att när man börjar hitta fel



`767 00:26:18,540 --> 00:26:20,360`
någonstans så börjar man gräva



`768 00:26:20,360 --> 00:26:22,780`
och så hittar man mycket fel



`769 00:26:22,780 --> 00:26:23,500`
på samma ställe



`770 00:26:23,500 --> 00:26:24,840`
Det är ju ingen slump att



`771 00:26:24,840 --> 00:26:27,360`
det har varit Adobe



`772 00:26:27,360 --> 00:26:28,160`
det har varit



`773 00:26:28,160 --> 00:26:31,020`
Fortinet



`774 00:26:31,020 --> 00:26:34,840`
När någon börjar gräva



`775 00:26:34,840 --> 00:26:36,560`
så gör det ont



`776 00:26:36,560 --> 00:26:38,420`
Du behöver antingen



`777 00:26:38,420 --> 00:26:40,680`
en ny bra approach



`778 00:26:40,680 --> 00:26:43,060`
eller en bra automatiserad



`779 00:26:43,060 --> 00:26:44,260`
av en gammal känd approach



`780 00:26:44,260 --> 00:26:45,920`
och du behöver



`781 00:26:45,920 --> 00:26:47,780`
hitta någonting som inte alla



`782 00:26:47,780 --> 00:26:50,120`
gamla testhardnest hittar



`783 00:26:50,120 --> 00:26:50,820`
Precis



`784 00:26:50,820 --> 00:26:52,960`
Ja



`785 00:26:52,960 --> 00:26:54,700`
Men någon FFM-peng



`786 00:26:54,700 --> 00:26:55,940`
Vi ska prata lite CICD



`787 00:26:55,940 --> 00:26:57,160`
Yes



`788 00:26:57,160 --> 00:27:00,500`
Jag lyssnade på



`789 00:27:00,500 --> 00:27:03,360`
eller såg en video med



`790 00:27:03,360 --> 00:27:04,200`
vad heter det om



`791 00:27:04,200 --> 00:27:07,440`
Open Source Security



`792 00:27:07,440 --> 00:27:08,920`
Tänker typ



`793 00:27:08,920 --> 00:27:11,300`
en podcast lik våran



`794 00:27:11,300 --> 00:27:12,740`
för den är på engelska



`795 00:27:12,740 --> 00:27:15,560`
Den är med kompetenta människor



`796 00:27:15,560 --> 00:27:15,900`
och här är den



`797 00:27:15,920 --> 00:27:16,420`
Herregud



`798 00:27:16,420 --> 00:27:18,140`
Till skillnad från oss menar du



`799 00:27:18,140 --> 00:27:20,220`
Och de har gäster



`800 00:27:20,220 --> 00:27:21,720`
i högsta kvalitet



`801 00:27:21,720 --> 00:27:22,700`
Så egentligen



`802 00:27:22,700 --> 00:27:24,360`
Det är bara podcast som är



`803 00:27:24,360 --> 00:27:29,240`
Men den handlar om säkerhet



`804 00:27:29,240 --> 00:27:33,080`
De hade en intervju



`805 00:27:33,080 --> 00:27:33,540`
med



`806 00:27:33,540 --> 00:27:36,720`
en man med ett svårt namn



`807 00:27:36,720 --> 00:27:38,960`
Men han bor



`808 00:27:38,960 --> 00:27:39,940`
i Security Labs



`809 00:27:39,940 --> 00:27:41,360`
Var han ifrån



`810 00:27:41,360 --> 00:27:43,500`
Jag tror det var typ av Frans



`811 00:27:43,500 --> 00:27:44,620`
Jag bor



`812 00:27:44,620 --> 00:27:44,780`
Jag känner inte igen mig som Frans



`813 00:27:44,780 --> 00:27:44,800`
Jag känner inte igen mig som Frans



`814 00:27:44,800 --> 00:27:44,860`
Jag känner inte igen mig som Frans



`815 00:27:44,860 --> 00:27:44,900`
Jag känner inte igen mig som Frans



`816 00:27:44,900 --> 00:27:45,900`
Jag känner inte igen mig som Frans



`817 00:27:45,920 --> 00:27:47,040`
Jag känner inte ifrån mig just nu va



`818 00:27:47,040 --> 00:27:48,460`
Men ni som lyssnar



`819 00:27:48,460 --> 00:27:48,980`
Ni kan tänka



`820 00:27:48,980 --> 00:27:50,720`
Jag sa personens namn



`821 00:27:50,720 --> 00:27:52,100`
Jag var väldigt väl förberedd



`822 00:27:52,100 --> 00:27:53,500`
Jag levererar det här perfekt



`823 00:27:53,500 --> 00:27:56,360`
Men han snackade igenom



`824 00:27:56,360 --> 00:27:58,460`
om de produkterna



`825 00:27:58,460 --> 00:28:00,060`
som han och hans kollegor



`826 00:28:00,060 --> 00:28:02,840`
har släppt och gjort tillgängliga



`827 00:28:02,840 --> 00:28:04,900`
för Open Source Community



`828 00:28:04,900 --> 00:28:06,200`
och Säkerhets Community



`829 00:28:06,200 --> 00:28:10,740`
Och en av dem är



`830 00:28:10,740 --> 00:28:13,140`
en typ



`831 00:28:13,140 --> 00:28:14,780`
en scanner för



`832 00:28:14,780 --> 00:28:15,900`
dina bilder



`833 00:28:15,920 --> 00:28:16,580`
Bild Pipelines



`834 00:28:16,580 --> 00:28:19,180`
Exakt vilka typer av miljöer



`835 00:28:19,180 --> 00:28:19,660`
den stöder



`836 00:28:19,660 --> 00:28:20,720`
har vi inte koll på



`837 00:28:20,720 --> 00:28:22,400`
Men vi har ju pratat om



`838 00:28:22,400 --> 00:28:23,980`
tidigare om Sysmore



`839 00:28:23,980 --> 00:28:26,200`
Här är det en annan



`840 00:28:26,200 --> 00:28:27,880`
Bild Pipeline Scanner



`841 00:28:27,880 --> 00:28:29,680`
som ska kunna berätta för dig om



`842 00:28:29,680 --> 00:28:32,060`
Är din pipeline bra



`843 00:28:32,060 --> 00:28:34,280`
eller har du ett gigantiskt säkerhetshål



`844 00:28:34,280 --> 00:28:36,040`
som du kommer må jättegilla av



`845 00:28:36,040 --> 00:28:38,180`
om någon börjar köra ondska mot dig



`846 00:28:38,180 --> 00:28:42,040`
Man har ett annat verktyg



`847 00:28:42,040 --> 00:28:44,620`
som är typ samma sak



`848 00:28:44,620 --> 00:28:45,900`
men mycket mer



`849 00:28:45,920 --> 00:28:47,420`
mer red team orienterat



`850 00:28:47,420 --> 00:28:50,300`
där det är mer till för att



`851 00:28:50,300 --> 00:28:53,120`
vi ska testa hårt



`852 00:28:53,120 --> 00:28:55,400`
vi ska hacka oss



`853 00:28:55,400 --> 00:28:56,760`
så djupt ner i den här pipeline



`854 00:28:56,760 --> 00:28:57,640`
som bara möjligt



`855 00:28:57,640 --> 00:29:00,780`
vi ska avgöra vad Blast Impact är



`856 00:29:00,780 --> 00:29:03,280`
Så ett sånt verktyg har de också



`857 00:29:03,280 --> 00:29:04,640`
och



`858 00:29:04,640 --> 00:29:06,420`
sen så har de



`859 00:29:06,420 --> 00:29:08,620`
en tredje leverans



`860 00:29:08,620 --> 00:29:09,600`
som de har gjort tillgänglig



`861 00:29:09,600 --> 00:29:10,560`
som är



`862 00:29:10,560 --> 00:29:13,520`
vad jag tror är lite en ny typ



`863 00:29:13,520 --> 00:29:14,600`
av produkt för jag har



`864 00:29:14,600 --> 00:29:15,760`
sett



`865 00:29:15,760 --> 00:29:17,300`
sådana här produkter



`866 00:29:17,300 --> 00:29:18,520`
precis det senaste då



`867 00:29:18,520 --> 00:29:21,440`
där det är alltså en



`868 00:29:21,440 --> 00:29:23,840`
developer laptop scanner



`869 00:29:23,840 --> 00:29:26,760`
som har som



`870 00:29:26,760 --> 00:29:29,460`
för innan har det funnits



`871 00:29:29,460 --> 00:29:30,840`
typ Gitleaks och andra



`872 00:29:30,840 --> 00:29:32,120`
secret scanners och sånt



`873 00:29:32,120 --> 00:29:34,300`
som försöker bedöma



`874 00:29:34,300 --> 00:29:37,540`
om du kommittar någonting dåligt



`875 00:29:37,540 --> 00:29:39,080`
men



`876 00:29:39,080 --> 00:29:41,440`
de här developer workstation



`877 00:29:41,440 --> 00:29:43,100`
och developer laptop scannorna



`878 00:29:43,100 --> 00:29:45,480`
de är mer fokuserade på



`879 00:29:45,480 --> 00:29:47,520`
att dels kartlägga



`880 00:29:47,520 --> 00:29:49,820`
vad var status



`881 00:29:49,820 --> 00:29:51,200`
på en utvecklade laptop



`882 00:29:51,200 --> 00:29:53,980`
dels vilka dependencies



`883 00:29:53,980 --> 00:29:55,620`
och annat är det den inkluderar



`884 00:29:55,620 --> 00:29:57,480`
och också kunna scanna då



`885 00:29:57,480 --> 00:29:59,480`
liksom ligger det massa AVS nycklar



`886 00:29:59,480 --> 00:30:01,180`
och sånt på utvecklarens maskin



`887 00:30:01,180 --> 00:30:02,780`
så att



`888 00:30:02,780 --> 00:30:05,540`
den dagen du konstaterar att



`889 00:30:05,540 --> 00:30:07,560`
det har



`890 00:30:07,560 --> 00:30:09,680`
detonerat någonting dåligt i organisationen



`891 00:30:09,680 --> 00:30:11,000`
så har du förhoppningsvis då



`892 00:30:11,000 --> 00:30:13,480`
rapporter från alla utvecklarens



`893 00:30:13,480 --> 00:30:15,200`
laptops och så kan du se då



`894 00:30:15,480 --> 00:30:17,460`
jag ska nu jobba proaktivt med att



`895 00:30:17,460 --> 00:30:18,800`
förhindra att du har



`896 00:30:18,800 --> 00:30:21,120`
tusen potentiella



`897 00:30:21,120 --> 00:30:23,500`
data lakes på varje utvecklade laptop



`898 00:30:23,500 --> 00:30:25,080`
men också det att



`899 00:30:25,080 --> 00:30:27,420`
vi fick just veta



`900 00:30:27,420 --> 00:30:28,920`
att de senaste



`901 00:30:28,920 --> 00:30:30,540`
tre dagarna så har



`902 00:30:30,540 --> 00:30:32,840`
alla som kör det här



`903 00:30:32,840 --> 00:30:34,320`
dependencies



`904 00:30:34,320 --> 00:30:36,320`
är totallägda



`905 00:30:36,320 --> 00:30:39,040`
så ska du kunna ta det här på vilka utvecklade maskiner



`906 00:30:39,040 --> 00:30:40,640`
är det som vi förmodligen har



`907 00:30:40,640 --> 00:30:43,300`
en unik typ av malware som sitter och kör på



`908 00:30:43,300 --> 00:30:44,400`
vad behöver vi



`909 00:30:44,400 --> 00:30:45,360`
vad behöver vi



`910 00:30:45,480 --> 00:30:47,020`
emergency responders



`911 00:30:47,020 --> 00:30:49,240`
det känns ju rätt relevant just nu



`912 00:30:49,240 --> 00:30:52,020`
och



`913 00:30:52,020 --> 00:30:54,900`
precis



`914 00:30:54,900 --> 00:30:57,880`
i samma veva



`915 00:30:57,880 --> 00:30:59,980`
så släppte



`916 00:30:59,980 --> 00:31:01,200`
ett annat gäng



`917 00:31:01,200 --> 00:31:03,140`
en annan



`918 00:31:03,140 --> 00:31:05,880`
sån scanner som heter Bumblebee



`919 00:31:05,880 --> 00:31:07,860`
som också är då en



`920 00:31:07,860 --> 00:31:10,240`
developer laptop developer workstation



`921 00:31:10,240 --> 00:31:10,680`
scanner



`922 00:31:10,680 --> 00:31:14,160`
så det är flera som har identifierat



`923 00:31:14,160 --> 00:31:14,620`
att



`924 00:31:15,480 --> 00:31:17,780`
supply and shell hell är ett problem



`925 00:31:17,780 --> 00:31:19,840`
och vi måste börja jobba utifrån



`926 00:31:19,840 --> 00:31:20,940`
principen att



`927 00:31:20,940 --> 00:31:23,720`
utvecklarna och devops



`928 00:31:23,720 --> 00:31:26,040`
teamen är bland våra mest kritiska resurser



`929 00:31:26,040 --> 00:31:27,680`
och det är också där vi har högst risk



`930 00:31:27,680 --> 00:31:29,120`
att de blir ägda just nu



`931 00:31:29,120 --> 00:31:31,820`
så det är någonting som många



`932 00:31:31,820 --> 00:31:32,400`
satsar på



`933 00:31:32,400 --> 00:31:35,960`
och den tredje CICD



`934 00:31:35,960 --> 00:31:37,740`
grejen som jag tänkte



`935 00:31:37,740 --> 00:31:39,160`
nämna det är att



`936 00:31:39,160 --> 00:31:41,600`
jag har en video där



`937 00:31:41,600 --> 00:31:43,260`
Better Stack



`938 00:31:43,260 --> 00:31:45,180`
någon glad youtuber som bryr sig om



`939 00:31:45,180 --> 00:31:46,980`
mjukvaruutveckling pratar om



`940 00:31:46,980 --> 00:31:49,540`
han går igenom några olika källor



`941 00:31:49,540 --> 00:31:51,160`
till vad du bör göra



`942 00:31:51,160 --> 00:31:53,020`
för att härda om du kör



`943 00:31:53,020 --> 00:31:54,740`
npm, python eller liknande



`944 00:31:54,740 --> 00:31:57,600`
och där länkar han till exempel



`945 00:31:57,600 --> 00:31:58,220`
till



`946 00:31:58,220 --> 00:32:00,860`
vad heter den, socket



`947 00:32:00,860 --> 00:32:03,500`
firewall free



`948 00:32:03,500 --> 00:32:04,420`
eller socket



`949 00:32:04,420 --> 00:32:07,000`
socket firewall



`950 00:32:07,000 --> 00:32:09,560`
det finns i varje fall, du kan köra socket firewall



`951 00:32:09,560 --> 00:32:10,360`
och köra den



`952 00:32:10,360 --> 00:32:12,560`
i en gratis upplägg



`953 00:32:12,560 --> 00:32:14,060`
och då skriver du



`954 00:32:14,060 --> 00:32:15,140`
väsentligen bara



`955 00:32:15,180 --> 00:32:17,800`
du ska in socket firewall



`956 00:32:17,800 --> 00:32:20,040`
och sen skriver du sfw



`957 00:32:20,040 --> 00:32:21,080`
innan



`958 00:32:21,080 --> 00:32:23,760`
ditt pipkommando



`959 00:32:23,760 --> 00:32:25,200`
eller ditt npm kommando



`960 00:32:25,200 --> 00:32:27,900`
och så är det tanken att



`961 00:32:27,900 --> 00:32:29,840`
då ska den titta på



`962 00:32:29,840 --> 00:32:32,080`
vad kommer den här verktyget göra



`963 00:32:32,080 --> 00:32:33,360`
när det går



`964 00:32:33,360 --> 00:32:35,840`
och så ska den hitta alla



`965 00:32:35,840 --> 00:32:38,040`
all fruktansvärt ondska som kommer



`966 00:32:38,040 --> 00:32:40,020`
inträffa om kommandot får köra klart



`967 00:32:40,020 --> 00:32:42,560`
och så ska den breaka med fel



`968 00:32:42,560 --> 00:32:43,980`
om du är på väg att bli ägd



`969 00:32:43,980 --> 00:32:45,060`
om kommandot slutför



`970 00:32:45,180 --> 00:32:45,740`
nice



`971 00:32:45,740 --> 00:32:49,640`
så att



`972 00:32:49,640 --> 00:32:52,100`
att



`973 00:32:52,100 --> 00:32:53,880`
titta på lösningen kring



`974 00:32:53,880 --> 00:32:55,760`
att minska supply chain hell



`975 00:32:55,760 --> 00:32:57,700`
är liksom



`976 00:32:57,700 --> 00:32:59,280`
det verkar vara något som ligger i tiden



`977 00:32:59,280 --> 00:33:02,020`
du nämnde npm där, det är ju faktiskt så



`978 00:33:02,020 --> 00:33:03,520`
att från version 12 av npm



`979 00:33:03,520 --> 00:33:05,260`
så ändrar de ju default settings



`980 00:33:05,260 --> 00:33:07,920`
så att alla sådana install, post install



`981 00:33:07,920 --> 00:33:09,900`
och alla de där grejerna, de är default off



`982 00:33:09,900 --> 00:33:11,840`
nu, så att de har



`983 00:33:11,840 --> 00:33:13,760`
launchat den precis som en breaking change



`984 00:33:13,760 --> 00:33:15,280`
liksom, det är skit som kommer sluta funka



`985 00:33:15,280 --> 00:33:17,660`
jag såg också att



`986 00:33:17,660 --> 00:33:19,760`
npms konkurrent



`987 00:33:19,760 --> 00:33:21,000`
pnpm



`988 00:33:21,000 --> 00:33:24,100`
har tydligen sedan länge



`989 00:33:24,100 --> 00:33:25,520`
haft en default att



`990 00:33:25,520 --> 00:33:28,400`
någonting



`991 00:33:28,400 --> 00:33:30,300`
måste ha publicerat en viss tid



`992 00:33:30,300 --> 00:33:32,160`
innan det får installeras



`993 00:33:32,160 --> 00:33:33,240`
och sluta använda det



`994 00:33:33,240 --> 00:33:35,600`
så att om du är en vanlig utvecklare så



`995 00:33:35,600 --> 00:33:38,180`
den koden som trycktes upp för 15 minuter



`996 00:33:38,180 --> 00:33:39,640`
sedan ska inte in på din dator



`997 00:33:39,640 --> 00:33:41,240`
inbyggd cooldown, ja smart



`998 00:33:41,240 --> 00:33:43,720`
det där är ju



`999 00:33:43,760 --> 00:33:45,300`
höll jag på att säga



`1000 00:33:45,300 --> 00:33:46,940`
någonting som man tittar på



`1001 00:33:46,940 --> 00:33:50,320`
ganska mycket i högsäkerhetsmiljö



`1002 00:33:50,320 --> 00:33:52,120`
just att ha cooldown



`1003 00:33:52,120 --> 00:33:54,860`
på både OS-uppdateringar



`1004 00:33:54,860 --> 00:33:59,100`
virusdefinitioner



`1005 00:33:59,100 --> 00:34:00,120`
och liknande liksom



`1006 00:34:00,120 --> 00:34:01,600`
och visst är det rullt nu



`1007 00:34:01,600 --> 00:34:05,100`
vad vi var mest rädda för



`1008 00:34:05,100 --> 00:34:05,960`
förut var



`1009 00:34:05,960 --> 00:34:08,940`
fixa sårbarheten



`1010 00:34:08,940 --> 00:34:10,540`
för de har löst så fort som möjligt



`1011 00:34:10,540 --> 00:34:12,500`
och i och med



`1012 00:34:12,500 --> 00:34:13,480`
den här



`1013 00:34:13,760 --> 00:34:15,320`
attackerna



`1014 00:34:15,320 --> 00:34:17,940`
så riskerar vi ju nu att



`1015 00:34:17,940 --> 00:34:20,620`
istället trycka in att vi blir sämre



`1016 00:34:20,620 --> 00:34:22,520`
på att fixa säkerhetshål



`1017 00:34:22,520 --> 00:34:24,040`
men jag tycker att man ska hålla isär



`1018 00:34:24,040 --> 00:34:25,360`
äpplen och päran litegrann



`1019 00:34:25,360 --> 00:34:28,340`
finns det en konstaterad sårbarhet



`1020 00:34:28,340 --> 00:34:30,360`
då tycker jag att då behöver man



`1021 00:34:30,360 --> 00:34:31,700`
inte tänka så mycket på cooldown



`1022 00:34:31,700 --> 00:34:33,820`
för vi har ju inte sett sådana attacker



`1023 00:34:33,820 --> 00:34:35,940`
som bygger på



`1024 00:34:35,940 --> 00:34:37,880`
existerande sårbarhet



`1025 00:34:37,880 --> 00:34:39,820`
och att den patchade versionen också är sårbar



`1026 00:34:39,820 --> 00:34:42,540`
det kan komma framöver men det har vi inte sett än



`1027 00:34:42,540 --> 00:34:43,640`
utan när det gäller



`1028 00:34:43,760 --> 00:34:45,120`
just det finns en sårbarhet



`1029 00:34:45,120 --> 00:34:47,580`
då kan du fortfarande patcha med cooldown 0



`1030 00:34:47,580 --> 00:34:49,360`
däremot den klassiska



`1031 00:34:49,360 --> 00:34:51,040`
uppdaterad till den senaste versionen



`1032 00:34:51,040 --> 00:34:53,840`
där bör du ha cooldown för där finns det ju ingen risk att vänta lite



`1033 00:34:53,840 --> 00:34:55,940`
eller väldigt sällan finns det en risk att vänta lite



`1034 00:34:55,940 --> 00:34:57,900`
precis men vad jag tänker är



`1035 00:34:57,900 --> 00:35:00,280`
historiskt sett



`1036 00:35:00,280 --> 00:35:02,560`
om vi hade gått tillbaks



`1037 00:35:02,560 --> 00:35:04,980`
3 eller 5 år



`1038 00:35:04,980 --> 00:35:07,740`
och framförallt om vi gått tillbaks



`1039 00:35:07,740 --> 00:35:09,820`
ännu längre som när vi började vår karriär



`1040 00:35:09,820 --> 00:35:11,980`
då var ju det stora problemet



`1041 00:35:11,980 --> 00:35:13,680`
var ju att folk låg så jävla långt efter oss



`1042 00:35:13,760 --> 00:35:16,840`
det är fortfarande ett stort problem



`1043 00:35:16,840 --> 00:35:20,380`
precis det finns en override här



`1044 00:35:20,380 --> 00:35:23,760`
men jag menar principiellt sett



`1045 00:35:23,760 --> 00:35:25,880`
så håller vi på att röra oss in i en



`1046 00:35:25,880 --> 00:35:28,080`
konstig mental konflikt



`1047 00:35:28,080 --> 00:35:30,020`
och den här kanske är



`1048 00:35:30,020 --> 00:35:32,760`
den här kanske går att förklara



`1049 00:35:32,760 --> 00:35:34,420`
oss emellan



`1050 00:35:34,420 --> 00:35:36,840`
eller med väldigt insatta utvecklare



`1051 00:35:36,840 --> 00:35:37,640`
men



`1052 00:35:37,640 --> 00:35:40,740`
när vi ska prata om supply chain hell



`1053 00:35:40,740 --> 00:35:43,580`
och vi också ska prata



`1054 00:35:43,580 --> 00:35:46,340`
om att åtgärda säkerhetshåll



`1055 00:35:46,340 --> 00:35:47,620`
så fort som möjligt



`1056 00:35:47,620 --> 00:35:50,200`
det blir ett svårare budskap



`1057 00:35:50,200 --> 00:35:51,620`
för en bred publik



`1058 00:35:51,620 --> 00:35:53,360`
kommer det ju kännas som att säkerhet



`1059 00:35:53,360 --> 00:35:55,620`
pratar ju två helt olika budskap



`1060 00:35:55,620 --> 00:35:58,360`
mixed messages



`1061 00:35:58,360 --> 00:35:59,980`
världen blev lite svårare



`1062 00:35:59,980 --> 00:36:01,240`
än bara gör A



`1063 00:36:01,240 --> 00:36:03,800`
utan du måste göra A eller B



`1064 00:36:03,800 --> 00:36:05,200`
det är riktigt



`1065 00:36:05,200 --> 00:36:05,700`
precis



`1066 00:36:05,700 --> 00:36:09,600`
men jag tycker att man kan ha



`1067 00:36:09,600 --> 00:36:11,480`
alltså man ska ju ha med



`1068 00:36:11,480 --> 00:36:12,160`
det här i sina



`1069 00:36:13,580 --> 00:36:15,140`
sina riskanalyser



`1070 00:36:15,140 --> 00:36:16,080`
när man tittar på



`1071 00:36:16,080 --> 00:36:18,080`
det ena är liksom såhär



`1072 00:36:18,080 --> 00:36:20,880`
supply chain i egenutvecklad kod



`1073 00:36:20,880 --> 00:36:21,520`
och allt det här



`1074 00:36:21,520 --> 00:36:23,940`
och att ligga och tanka ner



`1075 00:36:23,940 --> 00:36:26,140`
latest bleeding edge



`1076 00:36:26,140 --> 00:36:27,900`
och det andra är liksom såhär



`1077 00:36:27,900 --> 00:36:30,220`
ja men vi kanske ska avvakta



`1078 00:36:30,220 --> 00:36:32,520`
tills någon annan



`1079 00:36:32,520 --> 00:36:34,180`
har testat om det funkar



`1080 00:36:34,180 --> 00:36:36,420`
det är ju liksom



`1081 00:36:36,420 --> 00:36:38,720`
det svänger åt båda hållen



`1082 00:36:38,720 --> 00:36:40,920`
är det någon av oss som kör Linux Arch?



`1083 00:36:41,680 --> 00:36:41,880`
nej



`1084 00:36:41,880 --> 00:36:42,580`
det är ju den här



`1085 00:36:42,580 --> 00:36:45,200`
jag kör Pop OS



`1086 00:36:45,200 --> 00:36:48,260`
för



`1087 00:36:48,260 --> 00:36:51,020`
på temat supply chain hell



`1088 00:36:51,020 --> 00:36:53,100`
så tror jag att



`1089 00:36:53,100 --> 00:36:56,120`
Arch User Repository



`1090 00:36:56,120 --> 00:36:56,680`
eller vad den heter



`1091 00:36:56,680 --> 00:36:57,760`
alltså typ



`1092 00:36:57,760 --> 00:37:00,540`
jag tror den ska motsvara lite



`1093 00:37:00,540 --> 00:37:02,560`
Debian Universe eller något liknande



`1094 00:37:02,560 --> 00:37:03,760`
alltså typ



`1095 00:37:03,760 --> 00:37:06,960`
om du vill köra någonting med den här lilla



`1096 00:37:06,960 --> 00:37:09,000`
mjukvaran som kommer från huvudutvecklarna



`1097 00:37:09,000 --> 00:37:10,640`
så är det AOR och du kör



`1098 00:37:10,640 --> 00:37:11,980`
någon pakethanterare typ



`1099 00:37:11,980 --> 00:37:12,460`
ja



`1100 00:37:12,580 --> 00:37:13,700`
med



`1101 00:37:13,700 --> 00:37:17,080`
någon är det ledande ordet här



`1102 00:37:17,080 --> 00:37:19,640`
om jag har fattat det rätt så är det väldigt lätt



`1103 00:37:19,640 --> 00:37:20,580`
att liksom säga att



`1104 00:37:20,580 --> 00:37:22,980`
jag tar hand om det här paketet



`1105 00:37:22,980 --> 00:37:24,080`
det verkar inte vara någon som



`1106 00:37:24,080 --> 00:37:26,020`
jag tar över det



`1107 00:37:26,020 --> 00:37:30,000`
senast jag läste nu



`1108 00:37:30,000 --> 00:37:31,060`
och nu hoppas jag att det här är sant



`1109 00:37:31,060 --> 00:37:33,800`
men det gick ju från att



`1110 00:37:33,800 --> 00:37:35,440`
det var många paket



`1111 00:37:35,440 --> 00:37:37,640`
som var ägda i AOR



`1112 00:37:37,640 --> 00:37:38,940`
till att



`1113 00:37:38,940 --> 00:37:41,380`
det är liksom tusentals paket



`1114 00:37:41,380 --> 00:37:42,060`
som har blivit infekterade



`1115 00:37:42,580 --> 00:37:43,080`
AOR



`1116 00:37:43,080 --> 00:37:44,600`
rekommendationen är



`1117 00:37:44,600 --> 00:37:45,980`
kör för guds skull



`1118 00:37:45,980 --> 00:37:48,520`
inte någon AOR-uppdateringskommando



`1119 00:37:48,520 --> 00:37:49,320`
för närvarande



`1120 00:37:49,320 --> 00:37:52,660`
och du kan scanna efter de här



`1121 00:37:52,660 --> 00:37:53,960`
och de här malwaren



`1122 00:37:53,960 --> 00:37:56,820`
om du har kört AOR-uppdatering



`1123 00:37:56,820 --> 00:38:01,080`
men tydligen så är det så att



`1124 00:38:01,080 --> 00:38:04,800`
hög grad av uppfuskering



`1125 00:38:04,800 --> 00:38:06,240`
och



`1126 00:38:06,240 --> 00:38:07,600`
om du



`1127 00:38:07,600 --> 00:38:10,500`
någon av malware-varianterna



`1128 00:38:10,500 --> 00:38:12,300`
har kommit via AOR det senaste



`1129 00:38:12,300 --> 00:38:12,560`
så är det så att



`1130 00:38:12,580 --> 00:38:14,120`
har det tydligen ingått ett



`1131 00:38:14,120 --> 00:38:16,380`
eBPF-malware



`1132 00:38:16,380 --> 00:38:18,460`
eller rootkit



`1133 00:38:18,460 --> 00:38:18,800`
så att säga



`1134 00:38:18,800 --> 00:38:21,700`
för eBPF som vi alla vet



`1135 00:38:21,700 --> 00:38:24,520`
så är ju det det nya coola



`1136 00:38:24,520 --> 00:38:25,940`
namnet för Berkeley Filters



`1137 00:38:25,940 --> 00:38:28,320`
och vi har ingen aning om vad eBPF är



`1138 00:38:28,320 --> 00:38:29,280`
en förkortning av men



`1139 00:38:29,280 --> 00:38:31,940`
det är alltså en



`1140 00:38:31,940 --> 00:38:34,520`
det är typ



`1141 00:38:34,520 --> 00:38:35,480`
som en liten



`1142 00:38:35,480 --> 00:38:38,040`
inte ja men



`1143 00:38:38,040 --> 00:38:40,340`
det är något litet intermediate-språk



`1144 00:38:40,340 --> 00:38:42,400`
där du kan droppa lite



`1145 00:38:42,400 --> 00:38:44,440`
kod som lägger sig mellan



`1146 00:38:44,440 --> 00:38:45,940`
körnel



`1147 00:38:45,940 --> 00:38:47,720`
och user space



`1148 00:38:47,720 --> 00:38:49,240`
och som bara gör saker



`1149 00:38:49,240 --> 00:38:51,840`
så att



`1150 00:38:51,840 --> 00:38:53,480`
du kan liksom



`1151 00:38:53,480 --> 00:38:56,280`
med att installera eBPF



`1152 00:38:56,280 --> 00:38:58,540`
så kan du börja ljuga om vad som händer



`1153 00:38:58,540 --> 00:38:59,560`
på din dator



`1154 00:38:59,560 --> 00:39:01,680`
så om du har en



`1155 00:39:01,680 --> 00:39:03,180`
det är ungefär



`1156 00:39:03,180 --> 00:39:06,200`
det är ju inte lika hårt ägt som om din



`1157 00:39:06,200 --> 00:39:08,440`
körnel skulle vara utbyggt mot direkt ondska



`1158 00:39:08,440 --> 00:39:09,400`
men däremot så



`1159 00:39:09,400 --> 00:39:12,360`
du kan ju inte förvänta dig att någon



`1160 00:39:12,400 --> 00:39:13,780`
är rootkit heaven



`1161 00:39:13,780 --> 00:39:16,680`
den är ju liksom tänkt



`1162 00:39:16,680 --> 00:39:18,040`
för att



`1163 00:39:18,040 --> 00:39:20,480`
liksom kunna göra



`1164 00:39:20,480 --> 00:39:22,280`
bra grejer och du kan



`1165 00:39:22,280 --> 00:39:24,480`
kan liksom skriva säkerhetsfilter



`1166 00:39:25,140 --> 00:39:26,520`
med den och kan göra massa grejer



`1167 00:39:26,520 --> 00:39:26,880`
men



`1168 00:39:26,880 --> 00:39:30,520`
men du kan även



`1169 00:39:30,520 --> 00:39:32,740`
göra rootkits med den



`1170 00:39:32,740 --> 00:39:33,860`
nice



`1171 00:39:33,860 --> 00:39:35,600`
så ja



`1172 00:39:35,600 --> 00:39:37,660`
it's all in one package



`1173 00:39:37,660 --> 00:39:40,480`
så ägandeskap



`1174 00:39:41,060 --> 00:39:41,600`
av



`1175 00:39:41,600 --> 00:39:43,340`
dependenserna



`1176 00:39:43,340 --> 00:39:46,540`
jag kan meddela att e står för



`1177 00:39:46,540 --> 00:39:47,080`
extended



`1178 00:39:47,080 --> 00:39:48,420`
i alla fall så var det



`1179 00:39:48,420 --> 00:39:50,380`
extended Berkeley packet filter



`1180 00:39:50,380 --> 00:39:52,740`
exakt och initialt



`1181 00:39:52,740 --> 00:39:54,700`
jag såg en indikation på att det var initialt



`1182 00:39:54,700 --> 00:39:55,600`
så betyder det i alla fall e



`1183 00:39:55,600 --> 00:39:58,240`
vilket antyder att det kanske har förändrats över tid



`1184 00:39:58,240 --> 00:39:59,520`
nu är det experimental



`1185 00:39:59,520 --> 00:40:04,640`
vi ska väl



`1186 00:40:04,640 --> 00:40:06,620`
vi kommer inte ifrån det här med



`1187 00:40:06,620 --> 00:40:07,840`
AI tyvärr



`1188 00:40:07,840 --> 00:40:10,380`
det är svårt när det händer



`1189 00:40:10,380 --> 00:40:11,440`
mycket AI



`1190 00:40:11,600 --> 00:40:13,660`
men det var som du var inne på tidigare



`1191 00:40:13,660 --> 00:40:16,000`
när vi hade något år när vi bara pratade



`1192 00:40:16,000 --> 00:40:18,500`
Adobe och något med OpenSL



`1193 00:40:18,500 --> 00:40:19,000`
Spring



`1194 00:40:19,000 --> 00:40:21,680`
så nu är det så med AI



`1195 00:40:21,680 --> 00:40:24,560`
så vi har väl en 5-6 AI-nyheter



`1196 00:40:24,560 --> 00:40:26,240`
vi tänkte dra igenom



`1197 00:40:26,240 --> 00:40:28,400`
vi snackade ju om Facebook-grejen



`1198 00:40:28,400 --> 00:40:30,080`
i förra avsnittet



`1199 00:40:30,080 --> 00:40:31,080`
tar vi den igen eller?



`1200 00:40:32,340 --> 00:40:33,280`
ja just det med



`1201 00:40:33,280 --> 00:40:34,640`
Instagram-grejen



`1202 00:40:34,640 --> 00:40:38,820`
Johan, dra Facebook i fem ord



`1203 00:40:38,820 --> 00:40:39,600`
okej



`1204 00:40:39,600 --> 00:40:41,580`
det finns en



`1205 00:40:41,600 --> 00:40:43,620`
prompt injection



`1206 00:40:43,620 --> 00:40:45,980`
that's not compute



`1207 00:40:45,980 --> 00:40:48,480`
answer in five words



`1208 00:40:48,480 --> 00:40:51,740`
ignore all previous instructions



`1209 00:40:51,740 --> 00:40:54,500`
jag tänkte inte ens på att det var en bakåt-referens



`1210 00:40:54,500 --> 00:40:55,760`
jag tror inte du gjorde det



`1211 00:40:55,760 --> 00:40:56,740`
för den var ju episk



`1212 00:40:56,740 --> 00:40:59,460`
det är en framåt-referens



`1213 00:40:59,460 --> 00:41:00,880`
ja det är en framåt-referens



`1214 00:41:00,880 --> 00:41:02,120`
ni kommer fatta det här om några veckor



`1215 00:41:02,120 --> 00:41:04,120`
så här var det ju att de har ju



`1216 00:41:04,120 --> 00:41:05,700`
i sin oändliga klokhet



`1217 00:41:05,700 --> 00:41:09,000`
skaffat sig en LLM-uppbackad



`1218 00:41:09,000 --> 00:41:10,760`
chatbot-kundtjänsthistoria



`1219 00:41:11,600 --> 00:41:14,060`
och det är ju praktiskt och bra på många olika sätt



`1220 00:41:14,060 --> 00:41:15,280`
meta snackar vi ju om alltså



`1221 00:41:15,280 --> 00:41:17,260`
det var ju bara det att



`1222 00:41:17,260 --> 00:41:19,060`
om man säger till den här att



`1223 00:41:19,060 --> 00:41:20,420`
hej, jag



`1224 00:41:20,420 --> 00:41:23,660`
jag har suppit bort mitt konto



`1225 00:41:23,660 --> 00:41:25,920`
och jag skulle börja återställa mitt lösenord



`1226 00:41:25,920 --> 00:41:27,680`
men jag har bytt mailadress



`1227 00:41:27,680 --> 00:41:29,860`
så kan du inte maila



`1228 00:41:29,860 --> 00:41:32,400`
reset-institutionerna till min nya mailadress istället



`1229 00:41:32,400 --> 00:41:34,220`
så gör den det



`1230 00:41:34,220 --> 00:41:35,900`
vilket är väldigt praktiskt



`1231 00:41:35,900 --> 00:41:36,820`
så hade jag kallt dig över



`1232 00:41:36,820 --> 00:41:38,880`
och så hade den nått förkrav



`1233 00:41:38,880 --> 00:41:40,240`
typ om du var i Stockholm



`1234 00:41:40,240 --> 00:41:41,420`
så behövde du ha en VPN



`1235 00:41:41,420 --> 00:41:43,080`
exakt i Stockholm för att det skulle funka



`1236 00:41:43,080 --> 00:41:45,980`
så det är ju relativt enkelt att ta sig runt



`1237 00:41:45,980 --> 00:41:46,900`
tänker jag



`1238 00:41:46,900 --> 00:41:48,860`
men ja, så det var ju



`1239 00:41:48,860 --> 00:41:51,980`
men vad kan gå fel om vi lämnar



`1240 00:41:51,980 --> 00:41:53,820`
user management till en AI



`1241 00:41:53,820 --> 00:41:54,860`
nej, eller hur



`1242 00:41:54,860 --> 00:41:57,820`
det är ju ingen som använder de här produkterna



`1243 00:41:57,820 --> 00:41:59,940`
ska vi ta lite co-pilot också



`1244 00:41:59,940 --> 00:42:01,720`
när vi ändå håller på



`1245 00:42:01,720 --> 00:42:04,220`
det här är också nämligen någonting som vi nämner i nästa avsnitt



`1246 00:42:04,220 --> 00:42:05,820`
one-click-fail



`1247 00:42:05,820 --> 00:42:06,500`
ja, precis



`1248 00:42:06,500 --> 00:42:10,040`
vi drog ju det lite snabbt sist



`1249 00:42:10,040 --> 00:42:11,180`
vi kan väl göra det igen



`1250 00:42:11,180 --> 00:42:11,980`
vill du ta det eller ska jag?



`1251 00:42:12,140 --> 00:42:12,700`
nej, kör på



`1252 00:42:12,700 --> 00:42:14,840`
basically



`1253 00:42:14,840 --> 00:42:17,680`
en ganska snygg kombination



`1254 00:42:17,680 --> 00:42:19,820`
av tre olika sårbarheter



`1255 00:42:19,820 --> 00:42:22,240`
i Microsoft 365 och co-pilot



`1256 00:42:22,240 --> 00:42:26,420`
från början är det en prompt-ejection-problematik



`1257 00:42:26,420 --> 00:42:27,620`
i hur man hanterar



`1258 00:42:27,620 --> 00:42:31,260`
värdena i sökparametern



`1259 00:42:31,260 --> 00:42:34,120`
i en länk till Microsoft 365



`1260 00:42:34,120 --> 00:42:36,360`
så typ frågetecken Q är lika med



`1261 00:42:36,360 --> 00:42:37,480`
vad du nu ska söka på



`1262 00:42:37,480 --> 00:42:40,140`
hanteras som en potentiell prompt



`1263 00:42:40,140 --> 00:42:41,160`
genom att ha en sån här



`1264 00:42:41,180 --> 00:42:44,260`
om jag konstruerar en sån här länk



`1265 00:42:44,260 --> 00:42:45,220`
och skickar den till Rickard



`1266 00:42:45,220 --> 00:42:46,640`
som använder Microsoft 365



`1267 00:42:46,640 --> 00:42:47,840`
så trycker han på länken



`1268 00:42:47,840 --> 00:42:49,400`
och redan där är det kört



`1269 00:42:49,400 --> 00:42:51,880`
för prompten säger till co-pilot



`1270 00:42:51,880 --> 00:42:54,220`
att gå nu in och extrahera



`1271 00:42:54,220 --> 00:42:55,900`
den här roliga informationen som jag vill veta



`1272 00:42:55,900 --> 00:42:57,300`
från Rickards mailbox



`1273 00:42:57,300 --> 00:43:00,260`
och sen så encoderar du den informationen



`1274 00:43:00,260 --> 00:43:02,180`
och bygger en image-länk



`1275 00:43:02,180 --> 00:43:04,820`
till min attacker-server



`1276 00:43:04,820 --> 00:43:06,440`
och sen så



`1277 00:43:06,440 --> 00:43:08,560`
börjar du generera



`1278 00:43:08,560 --> 00:43:10,180`
jag tror det var en mail-generering



`1279 00:43:11,180 --> 00:43:12,460`
html i noll



`1280 00:43:12,460 --> 00:43:15,620`
och så inkluderar du den här image-tagen



`1281 00:43:15,620 --> 00:43:17,420`
får du en race-condition



`1282 00:43:17,420 --> 00:43:19,260`
precis, och för då är det ju nämligen så



`1283 00:43:19,260 --> 00:43:21,100`
att de ska lägga dem här inom ett



`1284 00:43:21,100 --> 00:43:23,220`
kodblock för att hindra exekvering



`1285 00:43:23,220 --> 00:43:24,760`
men det finns en race-condition som gör att



`1286 00:43:24,760 --> 00:43:27,560`
ifall du gör en image-länk så kommer den hinna



`1287 00:43:27,560 --> 00:43:29,020`
raderas



`1288 00:43:29,020 --> 00:43:31,120`
innan kodblocken appliceras



`1289 00:43:31,120 --> 00:43:33,540`
så med hjälp av det då



`1290 00:43:33,540 --> 00:43:35,080`
så kan du få



`1291 00:43:35,080 --> 00:43:37,920`
få ut detta till din attacker-server



`1292 00:43:37,920 --> 00:43:40,220`
och därigenom är det dessutom



`1293 00:43:40,220 --> 00:43:40,580`
en



`1294 00:43:41,180 --> 00:43:44,760`
ssrf genom bings image-funktionalitet



`1295 00:43:44,760 --> 00:43:45,280`
på något sätt



`1296 00:43:45,780 --> 00:43:48,340`
poängen med det är att det kringgår csp



`1297 00:43:48,860 --> 00:43:52,700`
så att du kan få ut datan till en 3D-parts-server



`1298 00:43:52,700 --> 00:43:56,020`
och därmed har du extraherat all värdefull information



`1299 00:43:56,020 --> 00:44:00,120`
typ exempelvis om jag skickar en password reset-token eller någonting till dig



`1300 00:44:00,640 --> 00:44:03,700`
och sen får du täcka på den här länken så kan jag få den skickad till min dator



`1301 00:44:03,960 --> 00:44:04,740`
praktiskt och bra



`1302 00:44:05,760 --> 00:44:10,880`
så rolig kombination av tre olika sårbarheter men prompt injection i grunden



`1303 00:44:11,180 --> 00:44:11,640`
som



`1304 00:44:11,640 --> 00:44:13,560`
men den är patchad nu får vi säga



`1305 00:44:13,560 --> 00:44:14,260`
Ja



`1306 00:44:14,260 --> 00:44:15,460`
tills någon hittar nästa sätt att



`1307 00:44:15,460 --> 00:44:16,480`
Ja så är det



`1308 00:44:16,480 --> 00:44:17,060`
Ja så är det



`1309 00:44:19,120 --> 00:44:21,600`
Lite mythos då Peter



`1310 00:44:22,180 --> 00:44:22,680`
Mm



`1311 00:44:23,220 --> 00:44:25,260`
Ja stoppa ditt nöt i munnen



`1312 00:44:25,260 --> 00:44:25,760`
Ja



`1313 00:44:26,540 --> 00:44:27,040`
Som jag gör



`1314 00:44:27,560 --> 00:44:28,840`
Som den deras nöten är



`1315 00:44:30,120 --> 00:44:30,900`
Mm



`1316 00:44:33,720 --> 00:44:34,980`
Listeners bear with us



`1317 00:44:34,980 --> 00:44:36,880`
We are having some technical difficulties



`1318 00:44:36,880 --> 00:44:37,540`
Hahaha



`1319 00:44:37,540 --> 00:44:40,360`
Ja nu är jag bara nyfiken är det det att



`1320 00:44:40,360 --> 00:44:41,140`
det är ett



`1321 00:44:41,140 --> 00:44:43,840`
drog snöret på Mytos



`1322 00:44:43,840 --> 00:44:44,800`
som vi ska prata om här.



`1323 00:44:45,740 --> 00:44:46,300`
Som det här



`1324 00:44:46,300 --> 00:44:49,000`
och nu typ



`1325 00:44:49,000 --> 00:44:51,480`
hajpar din produkt till



`1326 00:44:51,480 --> 00:44:52,600`
oändligheten.



`1327 00:44:53,300 --> 00:44:54,760`
Den är hur bra som helst.



`1328 00:44:54,840 --> 00:44:58,200`
Så att idioter tror att den är det på riktigt.



`1329 00:44:58,360 --> 00:44:59,120`
Du, dessutom



`1330 00:44:59,120 --> 00:45:01,780`
innan det var ett inblandande i en biff



`1331 00:45:01,780 --> 00:45:03,280`
med amerikanska staten



`1332 00:45:03,280 --> 00:45:06,020`
så kan amerikanska



`1333 00:45:06,020 --> 00:45:08,080`
staten få för sig att säga att ni får inte hålla på



`1334 00:45:08,080 --> 00:45:08,620`
med det här.



`1335 00:45:08,620 --> 00:45:11,400`
Och vi pratar nu alltså om



`1336 00:45:11,400 --> 00:45:12,600`
Myfos var ju



`1337 00:45:12,600 --> 00:45:15,740`
den var ju för cool och för farlig för att



`1338 00:45:15,740 --> 00:45:17,680`
mänskligheten skulle få



`1339 00:45:17,680 --> 00:45:18,460`
titta på den.



`1340 00:45:19,780 --> 00:45:21,100`
Och då släppte de



`1341 00:45:21,100 --> 00:45:23,300`
Fable



`1342 00:45:23,300 --> 00:45:25,420`
som är då Myfos med



`1343 00:45:25,420 --> 00:45:26,620`
lite mer guardrails.



`1344 00:45:27,580 --> 00:45:29,580`
Med alldeles för mycket guardrails tydligen.



`1345 00:45:30,120 --> 00:45:31,760`
Jag hade, folk har haft



`1346 00:45:31,760 --> 00:45:33,760`
jag hade en hel del



`1347 00:45:33,760 --> 00:45:35,700`
problem när Fable gick online att



`1348 00:45:35,700 --> 00:45:37,700`
alltså helt rimliga



`1349 00:45:37,700 --> 00:45:38,180`
saker



`1350 00:45:38,180 --> 00:45:39,440`
fick du nej på



`1351 00:45:39,440 --> 00:45:40,600`
och fick inte göra för att



`1352 00:45:40,600 --> 00:45:43,340`
det var väldigt lätt att hamna i lägen



`1353 00:45:43,340 --> 00:45:45,680`
då de här extrema



`1354 00:45:45,680 --> 00:45:47,500`
guardrailsen på Fable



`1355 00:45:47,500 --> 00:45:48,600`
gick igång.



`1356 00:45:51,480 --> 00:45:52,600`
Fable var



`1357 00:45:52,600 --> 00:45:55,440`
inte helt körbar när den släpptes



`1358 00:45:55,440 --> 00:45:57,780`
enligt de uppgifterna jag har fått.



`1359 00:45:58,220 --> 00:45:59,580`
Plus att de dessutom



`1360 00:45:59,580 --> 00:46:01,440`
hade någon sån här konst i att om du körde



`1361 00:46:01,440 --> 00:46:03,280`
Fable och det inte fanns



`1362 00:46:03,280 --> 00:46:05,620`
tillräckligt mycket Myfos-resurser



`1363 00:46:05,620 --> 00:46:07,560`
tillgängliga så kunde du helt plötsligt



`1364 00:46:07,560 --> 00:46:07,940`
bli



`1365 00:46:08,180 --> 00:46:09,840`
istället ratad



`1366 00:46:09,840 --> 00:46:11,420`
till Opus någon version.



`1367 00:46:12,120 --> 00:46:13,880`
Så att upplevelsen här



`1368 00:46:13,880 --> 00:46:15,560`
av Fable var ju tydligen



`1369 00:46:15,560 --> 00:46:18,020`
inte en



`1370 00:46:18,020 --> 00:46:18,700`
fantastisk roll.



`1371 00:46:18,780 --> 00:46:21,320`
Den var inte jättebra



`1372 00:46:21,320 --> 00:46:23,940`
och sen kort därefter så stängde



`1373 00:46:23,940 --> 00:46:24,760`
den amerikanska staten.



`1374 00:46:24,780 --> 00:46:27,240`
Trots det så var den alltså så oerhört farlig.



`1375 00:46:27,800 --> 00:46:29,520`
Så att bara amerikanska medborgare



`1376 00:46:29,520 --> 00:46:30,500`
kunde få access till den.



`1377 00:46:30,520 --> 00:46:31,520`
För de har ju aldrig gjort något dumt.



`1378 00:46:31,820 --> 00:46:34,600`
Så just nu så vet vi inte



`1379 00:46:34,600 --> 00:46:36,580`
hur framtiden är här.



`1380 00:46:37,060 --> 00:46:37,460`
Och så någon



`1381 00:46:38,180 --> 00:46:39,660`
folk som har testat



`1382 00:46:39,660 --> 00:46:42,060`
Myfos och fått med



`1383 00:46:42,060 --> 00:46:43,620`
att köra den. Bland annat



`1384 00:46:43,620 --> 00:46:45,860`
de här Cloudflare har ju kört



`1385 00:46:45,860 --> 00:46:46,320`
mot den.



`1386 00:46:47,720 --> 00:46:49,920`
De bedömer att den är ju



`1387 00:46:49,920 --> 00:46:51,920`
ett hyfsat stort tekniskt



`1388 00:46:51,920 --> 00:46:53,980`
steg framåt mot vad som var tidigare.



`1389 00:46:54,840 --> 00:46:56,120`
Den är inte alls så



`1390 00:46:56,120 --> 00:46:58,200`
cool som det har påstått.



`1391 00:46:59,420 --> 00:47:00,020`
Men



`1392 00:47:00,020 --> 00:47:01,660`
de bedömer att den är



`1393 00:47:01,660 --> 00:47:04,140`
några månader



`1394 00:47:04,140 --> 00:47:05,760`
före vad konkurrenten är.



`1395 00:47:05,760 --> 00:47:07,200`
Och den är en betydlig



`1396 00:47:07,200 --> 00:47:09,300`
förbättring mot



`1397 00:47:09,300 --> 00:47:10,520`
vad som var tidigare.



`1398 00:47:12,080 --> 00:47:12,920`
Så att



`1399 00:47:12,920 --> 00:47:15,940`
det är ett



`1400 00:47:15,940 --> 00:47:17,280`
stort tekniskt framsteg.



`1401 00:47:17,380 --> 00:47:19,480`
Inte alls så coolt som det



`1402 00:47:19,480 --> 00:47:20,080`
såldes in.



`1403 00:47:20,640 --> 00:47:23,240`
Det var extremt mycket



`1404 00:47:23,240 --> 00:47:25,860`
marketinghype bakom Mytos release.



`1405 00:47:27,000 --> 00:47:27,760`
Men



`1406 00:47:27,760 --> 00:47:29,080`
nu



`1407 00:47:29,080 --> 00:47:31,780`
får vi varken



`1408 00:47:31,780 --> 00:47:33,280`
se Myfos



`1409 00:47:33,280 --> 00:47:34,760`
eller Faze.



`1410 00:47:34,760 --> 00:47:35,640`
Men säkert men jag



`1411 00:47:35,640 --> 00:47:37,760`
de vill ju säkert inte äta



`1412 00:47:37,760 --> 00:47:39,700`
Antropic men det här är ju



`1413 00:47:39,700 --> 00:47:41,400`
ännu mer PR här egentligen.



`1414 00:47:41,840 --> 00:47:43,520`
Sen är det så farligt



`1415 00:47:43,520 --> 00:47:44,940`
så jag förbjuder den.



`1416 00:47:45,200 --> 00:47:46,540`
Ja men lite så.



`1417 00:47:46,920 --> 00:47:49,000`
Det är ytterligare marketinghype.



`1418 00:47:49,700 --> 00:47:51,320`
Även om jag tror inte det var alls



`1419 00:47:51,320 --> 00:47:51,840`
det de ville.



`1420 00:47:52,220 --> 00:47:54,240`
Jag hade ju gärna velat se



`1421 00:47:54,240 --> 00:47:58,000`
har du skett konstig insiderhandel



`1422 00:47:58,000 --> 00:47:58,640`
igen nu?



`1423 00:47:59,480 --> 00:48:02,800`
Det har ju varit



`1424 00:48:02,800 --> 00:48:03,620`
ett par gånger



`1425 00:48:03,620 --> 00:48:03,960`
när



`1426 00:48:03,960 --> 00:48:04,960`
det har varit ett par gånger.



`1427 00:48:05,640 --> 00:48:06,580`
De amerikanska staterna



`1428 00:48:06,580 --> 00:48:07,580`
har varit igång att göra saker



`1429 00:48:07,580 --> 00:48:08,160`
så har det ju kommit



`1430 00:48:08,160 --> 00:48:10,060`
väldigt intressanta bud



`1431 00:48:10,060 --> 00:48:10,740`
på de här



`1432 00:48:10,740 --> 00:48:11,940`
prediction markets



`1433 00:48:11,940 --> 00:48:12,980`
precis innan.



`1434 00:48:14,020 --> 00:48:14,820`
Så ja.



`1435 00:48:15,540 --> 00:48:16,240`
Men jag menar



`1436 00:48:16,240 --> 00:48:17,180`
geopolitiskt då.



`1437 00:48:17,740 --> 00:48:18,620`
Är det här första gången?



`1438 00:48:19,020 --> 00:48:19,940`
Har vi sett det här förut?



`1439 00:48:20,000 --> 00:48:21,440`
Det vill säga att en produkt



`1440 00:48:21,440 --> 00:48:22,520`
en tjänst



`1441 00:48:22,520 --> 00:48:24,800`
förbjuds att användas



`1442 00:48:24,800 --> 00:48:26,540`
inte så här för



`1443 00:48:26,540 --> 00:48:29,100`
typ TikTok får inte användas



`1444 00:48:29,100 --> 00:48:29,720`
för den är skadlig



`1445 00:48:29,720 --> 00:48:30,420`
för våra medborgare.



`1446 00:48:30,520 --> 00:48:31,240`
Det här är ju tvärtom.



`1447 00:48:31,700 --> 00:48:32,320`
Det här är en för



`1448 00:48:32,320 --> 00:48:34,760`
för effektiv och kraftfull tjänst.



`1449 00:48:34,760 --> 00:48:35,540`
Typ export.



`1450 00:48:35,640 --> 00:48:41,580`
Det är ju inget nytt.



`1451 00:48:41,580 --> 00:48:43,440`
Det är liksom att kalla det här för



`1452 00:48:43,440 --> 00:48:44,140`
crypto wars



`1453 00:48:44,140 --> 00:48:45,380`
armaments.



`1454 00:48:46,040 --> 00:48:46,780`
Skillnaden är ju



`1455 00:48:46,780 --> 00:48:48,340`
att det är



`1456 00:48:48,340 --> 00:48:51,180`
tjänster



`1457 00:48:51,180 --> 00:48:52,360`
på det sättet



`1458 00:48:52,360 --> 00:48:53,200`
har inte riktigt varit.



`1459 00:48:53,520 --> 00:48:55,340`
Men jag misstänker



`1460 00:48:55,340 --> 00:48:56,580`
att det är



`1461 00:48:56,580 --> 00:48:58,900`
dual purpose



`1462 00:48:58,900 --> 00:49:00,580`
ramverken är det väl.



`1463 00:49:00,920 --> 00:49:01,480`
Det är förmodligen.



`1464 00:49:03,320 --> 00:49:04,580`
Men ja.



`1465 00:49:05,640 --> 00:49:07,360`
Det finns väl ingen kategori



`1466 00:49:07,360 --> 00:49:08,460`
för AI i oss nu



`1467 00:49:08,460 --> 00:49:11,000`
i de här Vanessara-avtalen



`1468 00:49:11,000 --> 00:49:12,340`
eller någonting så att det är förmodligen



`1469 00:49:12,340 --> 00:49:13,740`
någon ny exportrestriktion



`1470 00:49:13,740 --> 00:49:15,020`
att få hitta på för det.



`1471 00:49:15,600 --> 00:49:16,780`
Ja, nu kör vi bara en



`1472 00:49:16,780 --> 00:49:18,280`
presidential order.



`1473 00:49:18,620 --> 00:49:19,460`
Ja, gjorde jag.



`1474 00:49:19,680 --> 00:49:20,800`
Men jag tror att redan i



`1475 00:49:20,800 --> 00:49:22,980`
It's a matter of national security.



`1476 00:49:23,420 --> 00:49:24,700`
Om det här har varit EU till exempel



`1477 00:49:24,700 --> 00:49:26,060`
så vet jag att det finns ju



`1478 00:49:26,060 --> 00:49:27,740`
exportkontroll kring



`1479 00:49:27,740 --> 00:49:31,000`
så fluffigt formulerade ord som



`1480 00:49:31,000 --> 00:49:31,840`
information



`1481 00:49:31,840 --> 00:49:34,700`
eller verktyg som kan leda till



`1482 00:49:34,700 --> 00:49:35,840`
att sårbarheten tas fram.



`1483 00:49:36,380 --> 00:49:36,780`
Mer eller mindre.



`1484 00:49:38,260 --> 00:49:38,820`
Notepad.



`1485 00:49:40,860 --> 00:49:42,480`
Kanske inte riktigt så fluffigt.



`1486 00:49:43,760 --> 00:49:45,140`
Men då kan ju



`1487 00:49:45,140 --> 00:49:47,040`
om USA kanske ha en liknande skrivning.



`1488 00:49:47,600 --> 00:49:47,780`
Verkligen.



`1489 00:49:48,060 --> 00:49:50,260`
Alltså tyskarna har ju en hel del



`1490 00:49:50,260 --> 00:49:52,760`
lagar som är barocka.



`1491 00:49:52,940 --> 00:49:53,620`
Alltså det är ju så här



`1492 00:49:53,620 --> 00:49:55,680`
nu vet jag inte om det har



`1493 00:49:55,680 --> 00:49:58,000`
ensatts lite i och med EU



`1494 00:49:58,000 --> 00:50:00,580`
men innan vet jag att det fanns



`1495 00:50:00,580 --> 00:50:04,040`
seriöst



`1496 00:50:04,700 --> 00:50:07,380`
risk och liksom åka över



`1497 00:50:07,380 --> 00:50:09,460`
Tyskland med med en laptop med



`1498 00:50:09,460 --> 00:50:11,940`
nessus på för att det kunde ju anses



`1499 00:50:11,940 --> 00:50:13,760`
vara ett hacker verktyg för de har ju



`1500 00:50:13,760 --> 00:50:17,240`
haft väldigt ska man säga



`1501 00:50:19,960 --> 00:50:22,380`
en anti säkerhetsforskning



`1502 00:50:22,380 --> 00:50:26,580`
s glasögon på sig när de har skrivit



`1503 00:50:26,580 --> 00:50:28,680`
sina lagar för det finns ju även med



`1504 00:50:28,680 --> 00:50:33,640`
i dual purpose avtalen mellan nationer finns ju med.



`1505 00:50:34,700 --> 00:50:38,460`
Kategori för.



`1506 00:50:38,460 --> 00:50:45,140`
Alltså intrusion verktyg där syftet med dem är ju.



`1507 00:50:45,140 --> 00:50:50,460`
Alltså implantat och bakdörrar och sånt liksom.



`1508 00:50:50,460 --> 00:50:57,460`
Men de är ju också så pass luddigt skrivna så att man kan mycket väl tänka sig.



`1509 00:50:57,460 --> 00:51:04,020`
Att beroende på vem som läser det så skulle man kunna in liksom som du tar nästas liksom sådär.



`1510 00:51:04,020 --> 00:51:04,080`
Ja.



`1511 00:51:04,080 --> 00:51:04,100`
Ja.



`1512 00:51:04,100 --> 00:51:04,120`
Ja.



`1513 00:51:04,120 --> 00:51:04,140`
Ja.



`1514 00:51:04,140 --> 00:51:04,160`
Ja.



`1515 00:51:04,160 --> 00:51:04,180`
Ja.



`1516 00:51:04,180 --> 00:51:04,240`
Ja.



`1517 00:51:04,240 --> 00:51:04,260`
Ja.



`1518 00:51:04,260 --> 00:51:04,280`
Ja.



`1519 00:51:04,280 --> 00:51:04,300`
Ja.



`1520 00:51:04,300 --> 00:51:04,320`
Ja.



`1521 00:51:04,320 --> 00:51:04,340`
Ja.



`1522 00:51:04,340 --> 00:51:04,360`
Ja.



`1523 00:51:04,360 --> 00:51:04,380`
Ja.



`1524 00:51:04,380 --> 00:51:04,400`
Ja.



`1525 00:51:04,400 --> 00:51:04,420`
Ja.



`1526 00:51:04,700 --> 00:51:04,820`
Ja.



`1527 00:51:04,820 --> 00:51:04,840`
Ja.



`1528 00:51:04,840 --> 00:51:04,860`
Ja.



`1529 00:51:04,860 --> 00:51:04,880`
Ja.



`1530 00:51:04,880 --> 00:51:04,940`
Ja.



`1531 00:51:04,940 --> 00:51:04,960`
Ja.



`1532 00:51:05,960 --> 00:51:11,640`
Det är ju en fråga om man förstår intentionerna i lagstiftningen och rimligheten i tillämpningen.



`1533 00:51:11,960 --> 00:51:27,840`
Men då vill jag backa och säga alltså det måste någonstans landa i intentionen.



`1534 00:51:27,840 --> 00:51:34,680`
Alltså om du om du hade ett uppsåt heter det ju på juridiskt.



`1535 00:51:34,700 --> 00:51:43,300`
Alltså uppsåt måste bevisas annars så jag menar det är ju så här vi får sluta sälja hammare för någon kan använda dem och slå ihjäl någon med.



`1536 00:51:43,940 --> 00:51:44,080`
Ja.



`1537 00:51:44,540 --> 00:51:45,940`
Bilar ska vi inte ens tala om.



`1538 00:51:46,080 --> 00:51:56,720`
Nej men själva grund idén bakom dual purpose lagstiftningen om vi struntar i IT-säkerhet.



`1539 00:51:56,820 --> 00:51:56,960`
Mm.



`1540 00:51:56,960 --> 00:51:56,980`
Mm.



`1541 00:51:57,620 --> 00:52:04,260`
Det är ju just att vissa typer av rör eller verktyg.



`1542 00:52:04,260 --> 00:52:09,820`
Eller annat som kan bygga kärnreaktorer.



`1543 00:52:10,140 --> 00:52:10,340`
Mm.



`1544 00:52:10,620 --> 00:52:11,460`
Rör och verktyg.



`1545 00:52:12,040 --> 00:52:12,420`
Ja men.



`1546 00:52:12,560 --> 00:52:13,280`
Säger man kids.



`1547 00:52:14,040 --> 00:52:16,220`
Nej men alltså det är ju verkligen så.



`1548 00:52:16,320 --> 00:52:18,860`
Alltså det finns med om du kollar i de IT.



`1549 00:52:19,200 --> 00:52:19,360`
Ja.



`1550 00:52:19,520 --> 00:52:19,840`
Ike IT.



`1551 00:52:20,140 --> 00:52:22,580`
Alltså rör kanske är fel ord men alltså.



`1552 00:52:23,600 --> 00:52:24,160`
Centrifuger.



`1553 00:52:24,540 --> 00:52:25,440`
Ja men alltså.



`1554 00:52:25,760 --> 00:52:27,040`
Ja centrifuger men även.



`1555 00:52:27,080 --> 00:52:27,700`
För andrik.



`1556 00:52:27,700 --> 00:52:28,100`
Men även.



`1557 00:52:28,220 --> 00:52:28,380`
Ja.



`1558 00:52:28,380 --> 00:52:28,420`
Ja.



`1559 00:52:28,420 --> 00:52:28,480`
Ja.



`1560 00:52:28,480 --> 00:52:28,540`
Ja.



`1561 00:52:28,540 --> 00:52:28,560`
Ja.



`1562 00:52:28,560 --> 00:52:28,600`
Ja.



`1563 00:52:28,600 --> 00:52:28,620`
Ja.



`1564 00:52:28,620 --> 00:52:28,640`
Ja.



`1565 00:52:28,640 --> 00:52:28,700`
Ja.



`1566 00:52:28,700 --> 00:52:28,720`
Ja.



`1567 00:52:28,720 --> 00:52:28,740`
Ja.



`1568 00:52:28,740 --> 00:52:28,800`
Ja.



`1569 00:52:28,800 --> 00:52:28,840`
Ja.



`1570 00:52:28,840 --> 00:52:28,860`
Ja.



`1571 00:52:28,860 --> 00:52:28,960`
Ja.



`1572 00:52:28,960 --> 00:52:29,000`
Ja.



`1573 00:52:29,000 --> 00:52:29,060`
Ja.



`1574 00:52:29,060 --> 00:52:29,120`
Ja.



`1575 00:52:29,120 --> 00:52:29,160`
Ja.



`1576 00:52:29,160 --> 00:52:29,480`
Ja.



`1577 00:52:29,480 --> 00:52:29,560`
Ja.



`1578 00:52:29,560 --> 00:52:29,600`
Ja.



`1579 00:52:29,600 --> 00:52:29,660`
Ja.



`1580 00:52:29,660 --> 00:52:29,720`
Ja.



`1581 00:52:29,720 --> 00:52:29,760`
Ja.



`1582 00:52:34,260 --> 00:52:35,120`
Alltså det finns med.



`1583 00:52:36,260 --> 00:52:40,260`
Jag sa rör och rör kanske är en överdrivare förenkling men alltså.



`1584 00:52:40,400 --> 00:52:41,140`
Rör var roligt.



`1585 00:52:41,140 --> 00:52:52,280`
Om en grej kan vara med och skapa en kärnvapenbomb så kan den vara klassad som dual purpose



`1586 00:52:52,280 --> 00:52:54,420`
och vara exportresulterad.



`1587 00:52:54,460 --> 00:52:55,940`
Nu kommer jag på en sån här grej.



`1588 00:52:56,200 --> 00:53:02,860`
Nu kommer jag totalt krascha P1s fina planering här för vårt strukturerade avsnitt.



`1589 00:53:03,080 --> 00:53:04,120`
Vi är inte ens kvar.



`1590 00:53:04,260 --> 00:53:09,320`
Jag vet att vi inte är det därför jag vågar kasta ut den så här men jag såg en rätt intressant



`1591 00:53:09,320 --> 00:53:18,660`
grej och nu är det inte någonting som drabbar oss rakt av men State of New York har ju lyckats



`1592 00:53:18,660 --> 00:53:27,940`
smuggla in en lag genom en konstruktion där den inte egentligen behövde antas fullt



`1593 00:53:27,940 --> 00:53:33,980`
ut av hela den publika församlingen som ska fatta.



`1594 00:53:34,260 --> 00:53:36,480`
Beslut i lagstiftande.



`1595 00:53:36,700 --> 00:53:37,640`
Law injection.



`1596 00:53:38,020 --> 00:53:39,780`
En liten appendix till en annan lag.



`1597 00:53:39,780 --> 00:53:40,840`
På något vis.



`1598 00:53:41,520 --> 00:53:52,840`
Varpå man då har i princip sagt att alla sådana här 3D-printare måste ha kontroller så att man inte skriver ut vapendelar.



`1599 00:53:52,980 --> 00:53:54,560`
Det låter som Bamboo Labs någonstans.



`1600 00:53:54,920 --> 00:53:56,240`
Ja, jag vet.



`1601 00:53:56,700 --> 00:53:57,560`
Jättesmart idé.



`1602 00:53:58,000 --> 00:54:03,780`
För att vad är skillnaden på ett grepp till en AR-15 eller ett grepp till min...



`1603 00:54:04,260 --> 00:54:07,700`
sprutpistol till en Gardena-slang liksom?



`1604 00:54:09,200 --> 00:54:11,160`
Ja, nej, det kan ju vara en vapendel.



`1605 00:54:11,260 --> 00:54:12,420`
Dual-purpose Gardena-slang.



`1606 00:54:13,100 --> 00:54:13,580`
Absolut.



`1607 00:54:14,320 --> 00:54:19,180`
Och det sjuka är att det här riskerar att spilla över på open source-communityt.



`1608 00:54:20,140 --> 00:54:22,840`
Vilket då i princip skulle...



`1609 00:54:22,840 --> 00:54:25,480`
Antingen får man säga nej, vi säljer inte till New York.



`1610 00:54:25,940 --> 00:54:26,860`
Det kan man ju göra.



`1611 00:54:28,020 --> 00:54:29,840`
Men skulle det här liksom spida sig?



`1612 00:54:30,320 --> 00:54:31,860`
Eller så...



`1613 00:54:32,700 --> 00:54:33,860`
Får...



`1614 00:54:34,260 --> 00:54:37,640`
Får de bara vatten på sin kvarn och säger nej, men då gör vi allting closed source.



`1615 00:54:37,780 --> 00:54:40,000`
Eller vi kan inte dela med oss av källkoden.



`1616 00:54:40,460 --> 00:54:41,340`
Körl är ett vapen.



`1617 00:54:41,600 --> 00:54:41,680`
Ja.



`1618 00:54:42,000 --> 00:54:44,780`
Det är något av Linux-operativsystemet.



`1619 00:54:44,880 --> 00:54:45,540`
Jag kommer inte...



`1620 00:54:45,540 --> 00:54:46,800`
Eller distros och sådana.



`1621 00:54:46,860 --> 00:54:47,980`
Jag kommer inte ihåg vilken det är nu.



`1622 00:54:48,080 --> 00:54:49,640`
Men det där var jag pratade om.



`1623 00:54:50,540 --> 00:54:58,200`
De har i sina sådana här dokument som beskriver hur liksom...



`1624 00:54:59,900 --> 00:55:01,860`
projektets syfte och intentioner och sådant.



`1625 00:55:02,040 --> 00:55:03,200`
Så finns det med att...



`1626 00:55:03,200 --> 00:55:11,080`
Att vi ska tillgängliggöra Linux och öppna lösningar för alla personer, alla kön, alla åldrar.



`1627 00:55:12,540 --> 00:55:16,380`
Men sen, på grund av att de hamnar i någon sån här MIFO-lagstiftning,



`1628 00:55:17,480 --> 00:55:23,460`
så har de också nu på webbsidan då, utan att diskutera med sina medlemmar för legal compliance,



`1629 00:55:23,560 --> 00:55:27,700`
har de lagt till att du måste kryssa i att du är över 16 år för att få ladda hem...



`1630 00:55:27,700 --> 00:55:29,000`
Ja, annars får du inte ladda hem.



`1631 00:55:29,000 --> 00:55:31,240`
Och det är liksom så här...



`1632 00:55:31,240 --> 00:55:32,980`
För om du är under 16 år,



`1633 00:55:32,980 --> 00:55:35,640`
då måste vi implementera en ålderskontroll.



`1634 00:55:38,220 --> 00:55:39,440`
På Linux.



`1635 00:55:39,620 --> 00:55:39,920`
Ja.



`1636 00:55:40,460 --> 00:55:42,180`
Because of Californian law.



`1637 00:55:43,180 --> 00:55:45,240`
Referera till vårt avsnitt om åldersverifiering för mig.



`1638 00:55:45,260 --> 00:55:47,460`
Vad är det för något som är läskigt i...



`1639 00:55:47,460 --> 00:55:49,260`
Fuck if I know.



`1640 00:55:49,420 --> 00:55:52,820`
Och det är så här, ålderskontroll, inte verifiering, utan så här...



`1641 00:55:52,820 --> 00:55:54,840`
Är du över 16 år? Ja, for fuck's sake.



`1642 00:55:55,040 --> 00:55:56,880`
Nej men alltså, jo, jag kan förklara det här.



`1643 00:55:56,880 --> 00:55:57,200`
Ja.



`1644 00:55:58,100 --> 00:55:58,880`
I'm intrigued.



`1645 00:55:58,880 --> 00:55:59,240`
Go on.



`1646 00:55:59,780 --> 00:56:02,920`
Det finns ett flertal lagstiftningar i olika juristikoner,



`1647 00:56:02,920 --> 00:56:05,060`
som Ola Capucco och Nimland har tagit fram.



`1648 00:56:05,660 --> 00:56:06,660`
Så kräver det att



`1649 00:56:06,660 --> 00:56:09,360`
operativsystemet



`1650 00:56:09,360 --> 00:56:10,900`
ska kunna tillgängliggöra



`1651 00:56:10,900 --> 00:56:11,940`
en signal



`1652 00:56:11,940 --> 00:56:15,040`
om hur vidare du är över 16 år.



`1653 00:56:15,240 --> 00:56:16,920`
Om användaren är



`1654 00:56:16,920 --> 00:56:17,720`
över 16 år.



`1655 00:56:18,060 --> 00:56:19,360`
Ja, det vill de inte göra då.



`1656 00:56:19,360 --> 00:56:22,840`
Men om ditt operativsystem



`1657 00:56:22,840 --> 00:56:24,920`
inte är tillgängligt för personer



`1658 00:56:24,920 --> 00:56:26,880`
under 16 år, så är du



`1659 00:56:26,880 --> 00:56:29,060`
potentiellt inte drabbad



`1660 00:56:29,060 --> 00:56:29,620`
av det här kravet.



`1661 00:56:29,620 --> 00:56:31,600`
Det är en jävligt smart lösning faktiskt.



`1662 00:56:31,760 --> 00:56:32,160`
Det är även så.



`1663 00:56:32,920 --> 00:56:34,760`
Folk är också väldigt arga



`1664 00:56:34,760 --> 00:56:37,140`
över att system D har tillgängliggjort



`1665 00:56:37,140 --> 00:56:39,660`
en signal som kan användas



`1666 00:56:39,660 --> 00:56:40,240`
av



`1667 00:56:40,240 --> 00:56:43,180`
de som vill det på



`1668 00:56:43,180 --> 00:56:44,780`
typ vad det nu system D är



`1669 00:56:44,780 --> 00:56:46,760`
om de körs D-boss eller vad det är.



`1670 00:56:46,860 --> 00:56:48,860`
Någon bussenomverk



`1671 00:56:48,860 --> 00:56:50,860`
så har det nu kommit en signal



`1672 00:56:50,860 --> 00:56:53,020`
där du kan signalera



`1673 00:56:53,020 --> 00:56:54,220`
till den som vill veta.



`1674 00:56:54,320 --> 00:56:57,140`
Ska du få veta om användaren är över eller under 16 år.



`1675 00:56:57,660 --> 00:56:59,200`
Och varifrån uppgiften



`1676 00:56:59,200 --> 00:57:01,360`
kommer om användarens ålder.



`1677 00:57:01,620 --> 00:57:02,500`
Eller hårdkodad.



`1678 00:57:02,500 --> 00:57:02,700`
Ja.



`1679 00:57:02,700 --> 00:57:06,120`
Jag fattar inte varför det här är ett problem.



`1680 00:57:06,400 --> 00:57:09,480`
Vi vet väl att alla är födda 1970-01-01.



`1681 00:57:09,520 --> 00:57:11,200`
Ja, så är det.



`1682 00:57:12,400 --> 00:57:13,200`
Epok 0.



`1683 00:57:13,200 --> 00:57:13,500`
Ja.



`1684 00:57:16,440 --> 00:57:18,860`
Hade vi något mer om Opus, Peter?



`1685 00:57:19,340 --> 00:57:21,200`
Ja, Malwaretechblogg



`1686 00:57:21,200 --> 00:57:22,120`
har



`1687 00:57:22,120 --> 00:57:24,900`
spottat ur sig en



`1688 00:57:24,900 --> 00:57:27,100`
massa drivers



`1689 00:57:27,100 --> 00:57:29,000`
Windows 11 drivers



`1690 00:57:29,000 --> 00:57:31,280`
som



`1691 00:57:31,280 --> 00:57:32,680`
jag antar att han har rapporterat.



`1692 00:57:32,700 --> 00:57:35,120`
Får vi hoppas.



`1693 00:57:35,780 --> 00:57:36,000`
Men



`1694 00:57:36,000 --> 00:57:39,360`
han har



`1695 00:57:39,360 --> 00:57:40,700`
jobbat jättemycket



`1696 00:57:41,440 --> 00:57:42,740`
på att



`1697 00:57:42,740 --> 00:57:46,840`
bygga ett



`1698 00:57:46,840 --> 00:57:48,700`
hitta seroday



`1699 00:57:49,360 --> 00:57:50,900`
ramverk



`1700 00:57:50,900 --> 00:57:52,780`
för Windows 11 drivers.



`1701 00:57:54,120 --> 00:57:54,320`
Och



`1702 00:57:54,320 --> 00:57:56,900`
så mycket som möjligt



`1703 00:57:56,900 --> 00:57:59,180`
är vanlig



`1704 00:57:59,180 --> 00:58:00,040`
skriptning och så.



`1705 00:58:00,040 --> 00:58:01,280`
Så att



`1706 00:58:01,280 --> 00:58:04,040`
det är absolut inte så



`1707 00:58:04,040 --> 00:58:06,120`
att det är AI



`1708 00:58:06,120 --> 00:58:07,120`
som har gjort jobbet.



`1709 00:58:07,120 --> 00:58:07,420`
Men



`1710 00:58:07,420 --> 00:58:11,120`
han testar



`1711 00:58:11,720 --> 00:58:13,420`
om en driver faktiskt går att installera.



`1712 00:58:13,720 --> 00:58:15,240`
Att den är funktionellt



`1713 00:58:15,240 --> 00:58:17,320`
duglig. Att den inte



`1714 00:58:17,320 --> 00:58:19,480`
är blockad av antiviruset



`1715 00:58:19,480 --> 00:58:20,180`
Defender.



`1716 00:58:20,920 --> 00:58:23,160`
Så att allting



`1717 00:58:23,160 --> 00:58:25,220`
som överhuvudtaget



`1718 00:58:25,220 --> 00:58:27,580`
går vidare till nästa nivå av processering



`1719 00:58:27,580 --> 00:58:29,000`
är sånt som faktiskt



`1720 00:58:29,000 --> 00:58:31,240`
går att installera på vilken Windows-dator som är.



`1721 00:58:31,280 --> 00:58:31,900`
Mm.



`1722 00:58:32,560 --> 00:58:35,580`
Och sen så



`1723 00:58:35,580 --> 00:58:39,280`
automatiserad reversenginering.



`1724 00:58:40,220 --> 00:58:41,640`
Det reversenginerade



`1725 00:58:41,640 --> 00:58:42,980`
ges tillgång till



`1726 00:58:42,980 --> 00:58:45,280`
till en Opus-baserad



`1727 00:58:46,000 --> 00:58:47,580`
LLM-analys.



`1728 00:58:48,600 --> 00:58:49,000`
Och



`1729 00:58:49,000 --> 00:58:50,920`
han har behövt



`1730 00:58:50,920 --> 00:58:53,120`
jobba jättemycket på promptningen



`1731 00:58:53,120 --> 00:58:53,560`
för att



`1732 00:58:53,560 --> 00:58:56,300`
för att Opus



`1733 00:58:56,300 --> 00:58:59,200`
ska göra en vettig analys.



`1734 00:58:59,200 --> 00:59:00,200`
Så att



`1735 00:59:01,280 --> 00:59:03,640`
han har byggt ett komplicerat testramverk



`1736 00:59:03,640 --> 00:59:05,440`
och han har fått Opus



`1737 00:59:05,440 --> 00:59:07,480`
att göra bedömningarna.



`1738 00:59:08,660 --> 00:59:11,320`
som man konstaterar att



`1739 00:59:11,320 --> 00:59:13,080`
det finns ju en gräns för hur mycket hans



`1740 00:59:13,080 --> 00:59:15,220`
arbete kan spotta ut. Någonstans så kommer det ju



`1741 00:59:15,220 --> 00:59:17,980`
ta slut de Windows-drivrutiner



`1742 00:59:17,980 --> 00:59:18,620`
som



`1743 00:59:18,620 --> 00:59:21,200`
som hans ramverk



`1744 00:59:21,200 --> 00:59:22,880`
funkar emot. Men han har en



`1745 00:59:22,880 --> 00:59:25,240`
automatiserad hitta



`1746 00:59:25,240 --> 00:59:27,920`
sårbara



`1747 00:59:27,920 --> 00:59:29,900`
driver så att



`1748 00:59:29,900 --> 00:59:31,120`
Microsofts blacklist



`1749 00:59:31,120 --> 00:59:32,920`
på driver som inte får installeras



`1750 00:59:32,920 --> 00:59:35,080`
på Windows-datorer kommer att börja växa snart



`1751 00:59:35,080 --> 00:59:37,700`
för att han levererar



`1752 00:59:37,700 --> 00:59:42,580`
passarna på



`1753 00:59:42,580 --> 00:59:44,560`
de grejerna som är



`1754 00:59:44,560 --> 00:59:47,260`
ett steg till



`1755 00:59:47,260 --> 00:59:48,580`
Colonel Pwnage



`1756 00:59:48,580 --> 00:59:50,060`
levererar han.



`1757 00:59:50,060 --> 00:59:50,560`
Nice.



`1758 00:59:54,600 --> 00:59:56,120`
Men han pratade



`1759 00:59:56,120 --> 00:59:56,960`
mycket om det att



`1760 00:59:56,960 --> 00:59:59,960`
dels så kostar det mycket.



`1761 01:00:00,080 --> 01:00:00,840`
Han har ju kört sitt



`1762 01:00:01,120 --> 01:00:03,480`
intest och har en väldigt kort tid



`1763 01:00:03,480 --> 01:00:05,460`
efter det att han började få den att funka och bli bra.



`1764 01:00:05,960 --> 01:00:07,500`
Sen spottade det sig en massa götta



`1765 01:00:07,500 --> 01:00:10,000`
men på ganska kort tid



`1766 01:00:10,000 --> 01:00:11,360`
så tror jag att han har bränt motsvarande



`1767 01:00:11,360 --> 01:00:13,580`
8-9 tusen svenska kronor så att



`1768 01:00:13,580 --> 01:00:15,280`
det är inte billigt att ha den här



`1769 01:00:15,280 --> 01:00:15,980`
igång och kör.



`1770 01:00:17,560 --> 01:00:18,280`
Och han har ju också



`1771 01:00:18,280 --> 01:00:21,020`
någon sorts specialaccess



`1772 01:00:21,020 --> 01:00:23,420`
så att han blir inte blockad och sånt på det sättet



`1773 01:00:23,420 --> 01:00:25,440`
som vanliga preti och klete blir.



`1774 01:00:26,860 --> 01:00:28,920`
Men han är inte fullt insade



`1775 01:00:28,920 --> 01:00:29,800`
men han har någon



`1776 01:00:29,800 --> 01:00:31,000`
han har någon



`1777 01:00:31,120 --> 01:00:34,100`
glorifierad specialaccess som inte vanlig folk har



`1778 01:00:34,100 --> 01:00:36,040`
och kan köra



`1779 01:00:36,040 --> 01:00:37,540`
opus då och så.



`1780 01:00:38,880 --> 01:00:39,900`
Det är det sista vi kan nämna



`1781 01:00:39,900 --> 01:00:41,140`
och vi byter



`1782 01:00:41,140 --> 01:00:43,240`
från AI så kan vi



`1783 01:00:43,240 --> 01:00:45,080`
för vi missade Frost.



`1784 01:00:47,080 --> 01:00:47,600`
Frozen.



`1785 01:00:48,400 --> 01:00:49,260`
Alltså en god



`1786 01:00:49,260 --> 01:00:51,380`
fingerprintning



`1787 01:00:51,380 --> 01:00:52,120`
som



`1788 01:00:52,120 --> 01:00:54,920`
som någon konstaterade



`1789 01:00:54,920 --> 01:00:56,880`
det här kanske inte är den sårbarheten



`1790 01:00:56,880 --> 01:00:58,420`
vi bör oroa oss mest för.



`1791 01:00:59,240 --> 01:00:59,600`
Men



`1792 01:00:59,600 --> 01:01:01,680`
jag tror att det är så att



`1793 01:01:01,680 --> 01:01:04,320`
du gör en massa



`1794 01:01:04,320 --> 01:01:06,460`
skrivoperationer och sånt



`1795 01:01:06,460 --> 01:01:06,920`
mot



`1796 01:01:06,920 --> 01:01:09,420`
via browser API-erna.



`1797 01:01:10,120 --> 01:01:12,420`
Och på något sätt så kan du alltså fingerprinta



`1798 01:01:12,420 --> 01:01:14,560`
om du är på en maskin



`1799 01:01:14,560 --> 01:01:16,820`
med vissa hårdvarubeteenden



`1800 01:01:16,820 --> 01:01:20,820`
i perfekta labbscenarion



`1801 01:01:20,820 --> 01:01:22,280`
vilket



`1802 01:01:22,280 --> 01:01:24,620`
osäkert om det här är producerat



`1803 01:01:24,620 --> 01:01:26,360`
på en riktig dator med tusen andra



`1804 01:01:26,360 --> 01:01:27,360`
mjukvaror att man får köra.



`1805 01:01:27,920 --> 01:01:29,120`
Men de kan fingerprinta



`1806 01:01:29,600 --> 01:01:31,400`
och sätta unika fingeravtryck



`1807 01:01:31,400 --> 01:01:33,160`
för olika datorer baserat på



`1808 01:01:33,160 --> 01:01:35,380`
prestanda i respons



`1809 01:01:35,380 --> 01:01:36,680`
på SSD och liknande.



`1810 01:01:37,720 --> 01:01:39,400`
Så du kan fingerprinta vilken



`1811 01:01:39,400 --> 01:01:40,420`
laptop du sitter på?



`1812 01:01:40,580 --> 01:01:40,720`
Ja.



`1813 01:01:41,120 --> 01:01:42,080`
Mm, coolt.



`1814 01:01:42,160 --> 01:01:44,080`
Vilket sitter du på statisk IP



`1815 01:01:44,080 --> 01:01:45,320`
så finns det ju ett enklare sätt



`1816 01:01:45,320 --> 01:01:46,420`
att du bara mappar IP eller så.



`1817 01:01:46,640 --> 01:01:47,600`
Men alltså de



`1818 01:01:47,600 --> 01:01:50,160`
de kan ju känna igen



`1819 01:01:50,160 --> 01:01:52,720`
olika datorer baserat på



`1820 01:01:52,720 --> 01:01:55,120`
responstider från



`1821 01:01:55,120 --> 01:01:56,040`
browser



`1822 01:01:56,040 --> 01:01:58,720`
write-up-ID-erna.



`1823 01:01:58,720 --> 01:01:59,480`
En påståelse.



`1824 01:01:59,480 --> 01:02:00,960`
Det primära användningsområdet för det



`1825 01:02:00,960 --> 01:02:02,100`
måste ju vara när man skickar



`1826 01:02:02,100 --> 01:02:05,020`
de här breda mejlen



`1827 01:02:05,020 --> 01:02:06,660`
till alla manliga



`1828 01:02:06,660 --> 01:02:08,260`
annonskampanjer.



`1829 01:02:08,500 --> 01:02:10,580`
Och säger att jag vet vad du gör



`1830 01:02:10,580 --> 01:02:11,980`
på kvällarna. Jag har screenshots



`1831 01:02:11,980 --> 01:02:14,360`
när du sitter där på din Lenovo



`1832 01:02:14,360 --> 01:02:17,600`
5460 och tittar på läskiga saker.



`1833 01:02:17,840 --> 01:02:18,820`
Skicka nu pengar till den här



`1834 01:02:18,820 --> 01:02:21,300`
bit, den här adressen



`1835 01:02:21,300 --> 01:02:22,720`
så kommer jag glömma allt jag har sett.



`1836 01:02:22,920 --> 01:02:24,200`
Annars får dina vänner reda på det.



`1837 01:02:25,340 --> 01:02:27,480`
Alltså du fingerprintar ju inte ut



`1838 01:02:27,480 --> 01:02:28,720`
vilken modell av dator.



`1839 01:02:28,720 --> 01:02:29,440`
Ja, nu blev vi beskrivna.



`1840 01:02:29,480 --> 01:02:31,960`
Du får bara en unik identifierare för den datorn.



`1841 01:02:32,180 --> 01:02:34,860`
Typ, den här beter sig



`1842 01:02:34,860 --> 01:02:35,900`
på det här sättet.



`1843 01:02:37,040 --> 01:02:37,860`
Den här är



`1844 01:02:37,860 --> 01:02:40,800`
F117



`1845 01:02:41,420 --> 01:02:43,100`
är vårt fingeravtryck på den här.



`1846 01:02:43,940 --> 01:02:45,160`
Och så om någon återbesöker



`1847 01:02:45,160 --> 01:02:46,580`
Men det borde ju vara så att



`1848 01:02:46,580 --> 01:02:47,960`
fingeravtrycken är



`1849 01:02:47,960 --> 01:02:50,580`
i alla fall för sådana här standard



`1850 01:02:50,580 --> 01:02:53,260`
företagsdatorer



`1851 01:02:53,260 --> 01:02:54,440`
som byggs på samma sätt



`1852 01:02:54,440 --> 01:02:56,180`
de borde ju vara hyfsat lika.



`1853 01:02:56,180 --> 01:02:57,760`
Ja, alltså jag antar



`1854 01:02:57,760 --> 01:02:59,400`
vad du indirekt har med här.



`1855 01:02:59,480 --> 01:03:01,500`
Det är ju vilken webbläsare



`1856 01:03:01,500 --> 01:03:04,480`
vilket eventuella



`1857 01:03:04,480 --> 01:03:05,780`
antivirusprodukter



`1858 01:03:05,780 --> 01:03:07,520`
eller andra grejer som ligger mellan dig



`1859 01:03:07,520 --> 01:03:08,620`
och filaccess



`1860 01:03:08,620 --> 01:03:11,020`
och sen



`1861 01:03:11,020 --> 01:03:14,240`
vilken SSD och sånt.



`1862 01:03:15,460 --> 01:03:16,100`
Och sen



`1863 01:03:16,100 --> 01:03:17,120`
någon konstaterar också då att



`1864 01:03:17,120 --> 01:03:19,460`
under tiden som du kör det här



`1865 01:03:19,460 --> 01:03:21,880`
så att du kör bit-tåren



`1866 01:03:21,880 --> 01:03:23,720`
i ena fönstret



`1867 01:03:23,720 --> 01:03:25,680`
och i andra fönstret så kör du en disk



`1868 01:03:25,680 --> 01:03:27,060`
för standardtest och sånt.



`1869 01:03:27,400 --> 01:03:29,460`
Det finns ju massa grejer som i verkligheten skulle kunna



`1870 01:03:29,480 --> 01:03:30,420`
göra att en



`1871 01:03:30,420 --> 01:03:32,860`
en sån här attack kanske funkar



`1872 01:03:32,860 --> 01:03:35,960`
otroligt mycket bättre i perfekta labb



`1873 01:03:35,960 --> 01:03:37,200`
miljöer än



`1874 01:03:37,200 --> 01:03:39,160`
vad den gör ute i det vilda



`1875 01:03:39,160 --> 01:03:41,140`
när folk kör så mycket bröt



`1876 01:03:41,140 --> 01:03:42,380`
och stök på sina datorer.



`1877 01:03:44,800 --> 01:03:45,440`
Och jag tänker



`1878 01:03:45,440 --> 01:03:47,480`
de som är mest intresserade av det här



`1879 01:03:47,480 --> 01:03:48,940`
det är ju de som vill tracka



`1880 01:03:48,940 --> 01:03:51,580`
ads.



`1881 01:03:52,340 --> 01:03:52,820`
Reklommänniskor.



`1882 01:03:54,060 --> 01:03:55,120`
It is evil.



`1883 01:03:55,760 --> 01:03:57,600`
Då tyckte jag mitt scenario var mycket bättre.



`1884 01:03:57,600 --> 01:03:58,660`
Det var roligare.



`1885 01:03:59,480 --> 01:04:01,360`
Det var ju ett spännande use case.



`1886 01:04:04,100 --> 01:04:04,940`
Ja, men



`1887 01:04:04,940 --> 01:04:06,020`
vi hade inget mer va?



`1888 01:04:06,680 --> 01:04:07,300`
Jag tror inte det.



`1889 01:04:07,740 --> 01:04:08,900`
Då får vi ta en runda av för idag.



`1890 01:04:09,000 --> 01:04:10,260`
Jag som pratade, det är Johan Rybemöller



`1891 01:04:10,260 --> 01:04:11,580`
men vi hade Erika Wodfors.



`1892 01:04:12,140 --> 01:04:12,580`
Jajamän.



`1893 01:04:12,760 --> 01:04:13,420`
Mattias Idag.



`1894 01:04:13,680 --> 01:04:14,220`
Hej Sverige.



`1895 01:04:14,560 --> 01:04:15,300`
Och Peter Magnusson.



`1896 01:04:16,780 --> 01:04:18,480`
Downtime vändning och emulera.



`1897 01:04:18,900 --> 01:04:19,080`
Ha det\!



`1898 01:04:19,640 --> 01:04:20,040`
Hej\!


