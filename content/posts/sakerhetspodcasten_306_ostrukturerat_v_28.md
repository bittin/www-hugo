---
date: '2026-07-07T15:56:00+02:00'
tags:
- ostrukturerat
title: 'Säkerhetspodcasten #306 - Ostrukturerat V.28'
---
Github actions/checkout,
Hacker äger FIFA,
Dataöverförings lagkaos,
Windows (massa),
Acer Wave's feta CVEs,
Apple A12/A13 bootsäkerhet knäckt!

## Lyssna
* [mp3](https://traffic.libsyn.com/secure/sakerhetspodcasten/2026-07-06_Sakerhetspodcasten.mp3?dest-id=117848), längd: 41:00

## Plugs
* [OWASP Gotheburg: BBQ with friends - Post summer kickoff](https://www.meetup.com/owasp-gothenburg-meetup-group/events/315425062/?eventOrigin=group_upcoming_events) \
  Wednesday 26/8 - 17:00
* [BSides Göteborg](https://bsidesgbg.com/) \
  Conference Date: 23th October \
  Call For Paper: 4th July - 10th September

## Github actions/checkout: stoppar vissa typer av Pipeline Poisoning attacker

Stoppa vissa typer av attacker mot Github CI Workflows via
  kontroller i `actions/checkout`:

> TL;DR; This PR adds a check that refuses to check out fork pull request code
> when the workflow trigger is either `pull_request_target` or `workflow_run`,
> unless the workflow author explicitly opts in via a new input
> `allow-unsafe-pr-checkout: true`.

Länkar:
* [The Hacker News: GitHub Updates actions/checkout to Block Common Pwn Request Attack Patterns - GitHub’s actions/checkout v7 now blocks risky fork PR checkouts in privileged workflows to reduce common pwn request attacks.](https://thehackernews.com/2026/06/github-updates-actionscheckout-to-block.html)
* [Release v7.0.0 · actions/checkout · GitHub](https://github.com/actions/checkout/releases/tag/v7.0.0)
* [block checking out fork pr for pull\_request\_target and workflow\_run by aiqiaoy · Pull Request #2454 · actions/checkout · GitHub - Action for checking out a repo. Contribute to actions/checkout development by creating an account on GitHub.](https://github.com/actions/checkout/pull/2454)

Detta är lite en uppföljning på Github NPM v12 säkrare defaults som vi talade
  om förra månaden;

Säkrare defaults:
* `allowScripts` `off`
* `--allow-git` `none`
* `--allow-remote` `none`

Länkar:
* [The GitHub Blog/ Allison: Upcoming breaking changes for npm v12 - GitHub Changelog](https://github.blog/changelog/2026-06-09-upcoming-breaking-changes-for-npm-v12/)
* [YouTube/ Low Level: big news](https://www.youtube.com/watch?v=cX3G0cPRJiA) `video`

## Hacker tar över FIFA

(tips från Love)

> FIFA:s interna applikationer använder Microsoft Entra för autentisering och
>   rollbaserad åtkomstkontroll.
>
> Frontend-lösningarna (byggda i Angular, React
>   eller Vue) kontrollerar JWT-tokenet efter rollinformation och visar sidor
>   för nekad åtkomst vid behov.
>
> Backend-API:erna litar däremot på alla autentiserade medlemmar i
>   klientorganisationen (tenant) och levererar data oavsett roll.

Attackkedja:

* Register on agents.fifa.org (public)
* Get added to FIFA's Entra tenant
* Authenticate against any FIFA internal app
* Client says "access denied"
* Server says "here's everything"

Attacken berörde åtminstone:

* fdp.fifa.org (Football Data Platform)
* cis.fifa.org (Commentator Information System)
* xxxxxxxxx-spreadsheets-api.azurewebsites.net (dev environment)

Länkar:
* [I Could've Rickrolled the Entire FIFA World Cup. All I Needed Was My ID. | bobdahacker - How I found that anyone could register on FIFA's public Agent Platform, gain access to the Football Data Platform's Streaming Management panel, and get RTMP ingest URLs and stream keys for every live FIFA World Cup 2026 camera feed. I then spent hours calling FIFA, MediaKind, HBS, CISA, and the FBI trying to get someone to pick up the phone.](https://bobdahacker.com/blog/fifa-hack)


## Dataöverföringar och Digital suveränitet

Nu när USA kaosar runt bl.a. FTC, lagar m.m. börjar det snackas om exit från
  USA.
Ett Shrems III "fly från USA" kanske kommer komma?

Begreppet **Digital suveränitet** går varmt i nyheterna.

> We call upon the Commission to start an orderly exit from the US cloud –
>   which is not easy, but unfortunately unavoidable.

Länkar:
* [noyb.eu: US Supreme Court just blew up EU-US Data Transfers](https://noyb.eu/en/us-supreme-court-just-blew-eu-us-data-transfers)
* [SVT Nyheter: Analys - ”Europa vill bryta digitala beroendet”](https://www.svt.se/nyheter/ekonomi/europa-vill-bryta-digitala-beroendet)
* [SVT Nyheter: Så bröt tyska delstaten beroendet av tech från USA](https://www.svt.se/nyheter/utrikes/sa-brot-tyska-delstaten-beroendet-av-tech-fran-usa)
* [YouTube/ Nikka Systems Sverige: Podd 357 - Sveriges digitala suveränitet (specialavsnitt med Daniel Melin, Teracom)](https://www.youtube.com/watch?v=PrJXouuCnc0) `video`

## Windows fet update

Massvis med sårbarheter rättade, bl.a. några av Nightmare Eclipse's
  uncoordinated disclosure nolldagar sårbarheter.

Påstås förekomma brickade PCs till följd av jättestor Patch Tuesday m.m.
Inte alla PC's hade hjälp-partioner stora nog att ta emot patchen.
Microsoft släppt lite hjälp om hur man löser det.

Länkar:
* [Security Update Guide - Microsoft Security Response Center](https://msrc.microsoft.com/update-guide/releaseNote/2026-Jun)
* [Windows I1317180](https://admin.cloud.microsoft/Adminportal/Home?source=applauncher#/windowsreleasehealth/:/issue/WI1317180)
* [BleepingComputer/ Sergiu Gatlan: Microsoft - Some Windows PCs fail to install latest monthly updates - Microsoft warned customers on Tuesday that they may have issues installing the latest monthly updates on some Windows devices that were upgraded to Windows 11 24H2 or 25H2.](https://www.bleepingcomputer.com/news/microsoft/microsoft-some-upgraded-windows-pcs-fail-to-install-monthly-updates/)
* [Medium: Yet ANOTHER Windows Update is Breaking Computers. AGAIN. | by Michael Swengel | Jun, 2026 - Yet ANOTHER Windows Update is Breaking Computers. AGAIN. Seriously, Microsoft. What are you guys even doing at this point? I’ve used Windows long enough to know that any time Microsoft releases a …](https://medium.com/@michaelswengel/yet-another-windows-update-is-breaking-computers-again-6a3af88277c3)
* [June 2026 Patch Tuesday: Updates and Analysis | CrowdStrike](https://www.crowdstrike.com/en-us/blog/patch-tuesday-analysis-june-2026/)
* [Rapid7: Patch Tuesday - June 2026](https://www.rapid7.com/blog/post/em-patch-tuesday-june-2026/)
* [YouTube/ LMGClips: Windows Update Broke Everything](https://www.youtube.com/watch?v=MSGKMBfTEzw) `video`

## Windows secure boot certifikat

Microsofts gamla Secure Boot certifikat gick ut nyligen.
Hade man inte fått patchen med det nya har man problem.

Länkar:
* [June 23, 2026—KB5095093 (OS Builds 26200.8737 and 26100.8737) Preview - Microsoft Support](https://support.microsoft.com/en-us/topic/june-23-2026-kb5095093-os-builds-26200-8737-and-26100-8737-preview-0e2a20f2-cf9e-46f8-9f08-e6996220882d)

## Windows Defender RougePlanet Exploit

Nightmare Eclipse droppar en ny Windows/Defender sårbarhet.
Poppa `cmd.exe` som `SYSTEM` som lågprivilegerad användare.

Länkar:
* [Picus Security/ Sıla Özeren Hacıoğlu: RoguePlanet - Anatomy of the Nightmare Eclipse Microsoft Defender Zero-Day - Learn how autonomous penetration testing platforms use AI agents to scope, execute, validate, and revalidate real attack paths.](https://www.picussecurity.com/resource/blog/rogueplanet-anatomy-of-the-nightmare-eclipse-microsoft-defender-zero-day)

## Router säkerhet...

Broken Access Control - CVE-2026-49200
  `acer_cgi.log` är oautentiserad och innehåller lösenord...

Hardcoded Cryptographic Key - CVE-2026-49201
  `upload.cgi` alla krypterade backuper i hela universium delar samma AES nyckel.

Länkar:
* [Acer Community: Security Advisory - Upcoming Firmware Update for Acer Wave 7 Router - Overview Acer has been notified of system vulnerabilities in the Acer Wave 7 router identified through independent security research. These flaws, which focus on access control structures and firmware cryptographic protection mechanisms, are currently being addressed. Acer is actively developing a security firmware update…](https://community.acer.com/en/kb/articles/19673)
* [BleepingComputer/ Sergiu Gatlan: Acer working to patch max severity zero-days in Wave 7 routers - Acer is working to address two maximum-severity zero-day vulnerabilities affecting its Wave 7 mesh routers.](https://www.bleepingcomputer.com/news/security/acer-warns-of-max-severity-zero-days-affecting-wave-7-routers/)
* [YouTube/ Low Level: I hate to say it but the router situation is insane](https://www.youtube.com/watch?v=gEMx7kt7n4E) `video`

## Apple A12 A13 boot säkerhet knäckt

Kanske mest ett problem för de som har statsmakten / våldsmonopolet som hot,
  men gamla Apple mobiler kan nu hackas via roliga USB-paket under uppstart.

Eller ptja, de har väl alltid kunnat det, men nu vet även vi det.

(Har forensikbolag känt till attack-tekniken tidigare? Vem vet?)

Länkar:
* [Paradigm Shift - Introducing usbliter8](https://ps.tc/pages/blog-usbliter8.html)
* [GitHub - prdgmshift/usbliter8: An A12/A13 SecureROM exploit · GitHub](https://github.com/prdgmshift/usbliter8)
* [Security Affairs: usbliter8 Brings Unpatchable BootROM Exploit to Apple A12 and A13 Devices - usbliter8 is an unpatchable BootROM exploit affecting Apple A12 and A13 devices, enabling code execution....](https://securityaffairs.com/193965/hacking/usbliter8-brings-unpatchable-bootrom-exploit-to-apple-a12-and-a13-devices.html)
* [YouTube/ Billy Ellis: The iPhone USB Exploit that Apple Can’t Fix](https://www.youtube.com/watch?v=9l_u3wj4qBY) `video`


## AI transkribering

_AI försöker förstå oss... Ha överseende med galna feltranskriberingar._

`1 00:00:00,000 --> 00:00:02,960`
Hej och välkommen till Säkerhetspodcasten.



`2 00:00:03,320 --> 00:00:07,300`
Jag som pratar heter Rickard Bogfors och med mig har jag Peter Magnusson.



`3 00:00:08,100 --> 00:00:09,080`
Registreringsbetalen är...



`4 00:00:09,080 --> 00:00:11,080`
Jesper Larsson.



`5 00:00:11,740 --> 00:00:12,560`
Jag vet inte vad jag ska säga.



`6 00:00:13,260 --> 00:00:14,320`
Och Mattias Idagge.



`7 00:00:16,100 --> 00:00:19,720`
Och tyvärr har vi inte Johan med oss idag för han har tappat rösten.



`8 00:00:20,140 --> 00:00:21,760`
Han har hejat sönder rösten kanske.



`9 00:00:21,920 --> 00:00:23,000`
Så kan det vara.



`10 00:00:23,560 --> 00:00:25,460`
Han måste ha hejat på Norrbaggarna igår.



`11 00:00:25,640 --> 00:00:27,340`
Det kan han mycket väl ha varit så.



`12 00:00:27,340 --> 00:00:29,060`
Ja, det är han faktiskt.



`13 00:00:29,060 --> 00:00:31,340`
Johan är en sån som skriker bara ja, så är det faktiskt.



`14 00:00:31,420 --> 00:00:35,800`
Och sen kan det ju ha varit så att han, jag menar matchen var slut vid midnatt och då kanske inte firandet slutade.



`15 00:00:36,140 --> 00:00:37,140`
Så kan det också vara.



`16 00:00:37,720 --> 00:00:40,600`
Så rösten kanske tog mer stryk på någon karaokebar eller någonstans.



`17 00:00:40,600 --> 00:00:41,960`
Så kan det mycket väl ha varit.



`18 00:00:42,500 --> 00:00:48,540`
Det är i alla fall den sjätte juli och det är nådens år 2026.



`19 00:00:49,300 --> 00:00:56,140`
Och vi är sponsrade av bland annat Ashore som man kan läsa om på ashore.se.



`20 00:00:57,020 --> 00:00:58,940`
0x4a som man kan läsa om på 0x4a.



`21 00:00:59,060 --> 00:01:03,940`
0x4a.se och Bordfors som man kan läsa om på bordfors.se.



`22 00:01:06,600 --> 00:01:12,520`
Vi spelar in idag ett ostrukturerat avsnitt som ni kanske redan märker.



`23 00:01:13,040 --> 00:01:16,380`
Vi har precis spelat in en sommaravsnitt.



`24 00:01:16,480 --> 00:01:18,160`
Ja, så det kommer strax.



`25 00:01:19,160 --> 00:01:25,220`
Men vi har väl några plugs som vi passar på att ta även i detta avsnittet tänker jag.



`26 00:01:25,220 --> 00:01:27,520`
Det tycker jag eftersom det lider mot sommar nu.



`27 00:01:28,020 --> 00:01:28,880`
Och man.



`28 00:01:29,060 --> 00:01:30,240`
Man vill ju.



`29 00:01:30,840 --> 00:01:33,160`
När man går på semester så längtar man ju tillbaka till jobbet.



`30 00:01:33,300 --> 00:01:33,480`
Ja.



`31 00:01:33,740 --> 00:01:34,560`
Det är så det brukar vara.



`32 00:01:34,700 --> 00:01:35,560`
Nästan första dagen.



`33 00:01:35,700 --> 00:01:36,060`
Exakt.



`34 00:01:36,320 --> 00:01:37,860`
Och då ska man inte misströsta.



`35 00:01:38,160 --> 00:01:40,260`
För man behöver ju ett säkerhetsevent som kan pigga upp.



`36 00:01:41,060 --> 00:01:44,140`
Och om du inte har köpt biljetter till Säkte, vilket man borde ha gjort.



`37 00:01:44,780 --> 00:01:46,140`
Så kanske man inte kan gå dit.



`38 00:01:46,220 --> 00:01:47,940`
Då kan man gå på ett event här i stan.



`39 00:01:48,080 --> 00:01:50,380`
Det är Ovas i Göteborg som då i augusti.



`40 00:01:50,820 --> 00:01:53,340`
Efter semesterna har en grillfest hos Scenics Group.



`41 00:01:53,420 --> 00:01:54,140`
Där kan man gå in på.



`42 00:01:55,120 --> 00:01:55,940`
Vad heter det event-sajten?



`43 00:01:55,980 --> 00:01:56,300`
Meetup.



`44 00:01:56,600 --> 00:01:57,400`
Meetup-grejen.



`45 00:01:57,880 --> 00:01:58,800`
Och signa upp sig.



`46 00:01:58,800 --> 00:02:01,240`
För att gå dit och grilla en korv.



`47 00:02:01,320 --> 00:02:02,240`
Eller något annat.



`48 00:02:02,560 --> 00:02:03,640`
26 augusti är datumet.



`49 00:02:03,820 --> 00:02:04,260`
Så är det.



`50 00:02:04,460 --> 00:02:06,220`
Var där eller var en fyrkant.



`51 00:02:06,940 --> 00:02:07,180`
Men.



`52 00:02:07,520 --> 00:02:10,520`
Sen har vi ju också våra off-sec-herrar.



`53 00:02:11,240 --> 00:02:11,860`
Och damer.



`54 00:02:12,240 --> 00:02:12,580`
Vad vet jag.



`55 00:02:14,060 --> 00:02:14,500`
Som.



`56 00:02:15,160 --> 00:02:16,780`
Det var felplugg.



`57 00:02:16,980 --> 00:02:17,440`
Inser jag nu.



`58 00:02:17,820 --> 00:02:18,960`
Så välkommen till oss.



`59 00:02:19,240 --> 00:02:21,540`
Vi ska prata om B-Sides Göteborg.



`60 00:02:21,720 --> 00:02:21,840`
Ja.



`61 00:02:22,200 --> 00:02:24,280`
För eventet som Jesper var inne på.



`62 00:02:24,360 --> 00:02:25,000`
Det har redan varit.



`63 00:02:25,320 --> 00:02:25,880`
Det har redan varit.



`64 00:02:25,880 --> 00:02:27,620`
Och var ni där så var det bra.



`65 00:02:27,620 --> 00:02:30,320`
Och lyssnade ni på det här avsnittet.



`66 00:02:30,560 --> 00:02:31,920`
Så ni är försenade.



`67 00:02:32,100 --> 00:02:33,860`
För att det är redan över när vi har spelat in.



`68 00:02:34,100 --> 00:02:36,780`
Men B-Sides Göteborg kommer köra.



`69 00:02:37,160 --> 00:02:39,440`
Och de har en call for paper.



`70 00:02:39,640 --> 00:02:42,500`
Där du skriver in dina perfekta idéer.



`71 00:02:42,520 --> 00:02:43,680`
Som du vill snacka om.



`72 00:02:43,920 --> 00:02:47,260`
Här i den finaste av fina städer.



`73 00:02:47,360 --> 00:02:48,660`
På den bästa av bästa sidor.



`74 00:02:49,400 --> 00:02:51,760`
Och då kan du skicka in ditt paper.



`75 00:02:52,760 --> 00:02:53,280`
Proposal.



`76 00:02:53,440 --> 00:02:54,480`
Till den.



`77 00:02:54,800 --> 00:02:56,620`
Mellan den fjärde juli.



`78 00:02:56,620 --> 00:02:56,660`
Och den fjärde juli.



`79 00:02:56,660 --> 00:02:56,760`
Och den fjärde juli.



`80 00:02:56,760 --> 00:02:56,780`
Och den fjärde juli.



`81 00:02:56,780 --> 00:02:57,600`
Och den fjärde juli.



`82 00:02:57,620 --> 00:02:59,520`
Och den tionde september.



`83 00:02:59,680 --> 00:03:01,060`
Tar de emot förslag.



`84 00:03:02,440 --> 00:03:05,240`
Och själva eventet.



`85 00:03:05,240 --> 00:03:07,860`
Kommer gå den tjugotredje oktober.



`86 00:03:09,060 --> 00:03:09,880`
Så är det.



`87 00:03:09,960 --> 00:03:10,780`
Och där kan man också vara.



`88 00:03:10,880 --> 00:03:13,100`
Eller vara en annan geometrisk figur.



`89 00:03:13,960 --> 00:03:14,820`
Tror det att.



`90 00:03:15,960 --> 00:03:18,900`
Man får identifiera sig som vilken geometrisk figur som helst.



`91 00:03:19,540 --> 00:03:19,740`
Ja.



`92 00:03:21,080 --> 00:03:22,100`
Det får man.



`93 00:03:23,040 --> 00:03:23,940`
Inte komma på något coolt.



`94 00:03:23,960 --> 00:03:24,760`
En fraktal.



`95 00:03:25,560 --> 00:03:27,120`
Det finns många kanter.



`96 00:03:27,620 --> 00:03:27,760`
Ja.



`97 00:03:27,980 --> 00:03:28,980`
Men det är inte därför vi är här.



`98 00:03:29,040 --> 00:03:31,040`
Vi ska prata om FIFA och fotboll.



`99 00:03:31,120 --> 00:03:33,300`
För det här är ju fotbollspodcasten.



`100 00:03:33,600 --> 00:03:33,800`
Mm.



`101 00:03:34,560 --> 00:03:36,580`
Och jävlar vad hade gått ut direkt då.



`102 00:03:36,700 --> 00:03:36,880`
Ja.



`103 00:03:37,320 --> 00:03:38,100`
Så bara stäng av.



`104 00:03:38,360 --> 00:03:39,120`
Vad har du för.



`105 00:03:39,400 --> 00:03:39,900`
Hej hej.



`106 00:03:39,920 --> 00:03:40,200`
Hej.



`107 00:03:40,800 --> 00:03:45,820`
Och vi är ju som välkänd tekniska experter på det här med sportboll och kan hela kittet liksom.



`108 00:03:45,980 --> 00:03:47,820`
Jag har inte kollat på en enda fotbollsmatch.



`109 00:03:47,880 --> 00:03:48,360`
Inte jag heller.



`110 00:03:48,380 --> 00:03:48,980`
Det har jag gjort.



`111 00:03:49,400 --> 00:03:50,860`
Jag har sett alla Sveriges matcher.



`112 00:03:51,520 --> 00:03:51,920`
Nej.



`113 00:03:52,160 --> 00:03:53,340`
Fan jag såg på natten såg jag inte.



`114 00:03:53,480 --> 00:03:54,640`
De sparkade boll.



`115 00:03:54,640 --> 00:03:56,000`
Går inte alla på natten?



`116 00:03:56,260 --> 00:03:56,560`
Nej.



`117 00:03:56,560 --> 00:03:56,620`
Nej.



`118 00:03:56,920 --> 00:03:57,960`
Som ikväll.



`119 00:03:58,420 --> 00:03:59,940`
Det hjälper inte er som lyssnar nu då.



`120 00:04:00,040 --> 00:04:01,920`
Men så spelar Portugal Spanning klockan nio.



`121 00:04:02,800 --> 00:04:03,040`
Ja.



`122 00:04:03,140 --> 00:04:04,880`
Det är ändå nära natt då.



`123 00:04:05,780 --> 00:04:06,700`
Då sover jag.



`124 00:04:08,000 --> 00:04:13,900`
Och andra sidan med mina dåliga nattvanor så hade jag kunnat se flera av matcherna.



`125 00:04:14,020 --> 00:04:15,420`
För jag har ändå vaknat klockan två på.



`126 00:04:15,520 --> 00:04:16,500`
Då kan jag tipsa dig om.



`127 00:04:16,540 --> 00:04:18,660`
Jag tror det är Mexiko-England klockan två i natt.



`128 00:04:18,680 --> 00:04:19,600`
Fast jag hatar fotboll.



`129 00:04:19,640 --> 00:04:20,100`
Ja exakt.



`130 00:04:20,220 --> 00:04:21,180`
Det är det lilla problemet.



`131 00:04:21,900 --> 00:04:22,980`
Hade det varit något annat.



`132 00:04:22,980 --> 00:04:24,240`
Jag lyssnar hellre på ljudbok.



`133 00:04:24,460 --> 00:04:24,940`
Schack.



`134 00:04:25,300 --> 00:04:25,780`
Schack.



`135 00:04:25,900 --> 00:04:26,340`
Exakt.



`136 00:04:26,560 --> 00:04:28,120`
Titta på när färg torkar.



`137 00:04:28,260 --> 00:04:28,340`
Ja.



`138 00:04:29,060 --> 00:04:30,660`
Det vinner nog fan med alltså.



`139 00:04:31,960 --> 00:04:33,260`
Jävlar vad folk kommer hata.



`140 00:04:33,380 --> 00:04:35,420`
Men det kan vara riktigt underhållande.



`141 00:04:35,440 --> 00:04:35,660`
Fotboll och FIFA.



`142 00:04:35,940 --> 00:04:36,560`
Det kan det vara klart.



`143 00:04:37,020 --> 00:04:37,320`
Jaha.



`144 00:04:37,500 --> 00:04:43,760`
Love tipsade oss om att vi borde snacka om den här FIFA-hacket.



`145 00:04:43,880 --> 00:04:49,880`
Där någon konstaterade att det går ju att anmäla sig till



`146 00:04:49,880 --> 00:04:55,900`
och få någon sorts användare in i deras, jag tror det är en



`147 00:04:55,900 --> 00:04:56,540`
Azure-tenant.



`148 00:04:56,560 --> 00:04:57,680`
Om jag minns rätt.



`149 00:04:57,940 --> 00:04:58,360`
Klart det.



`150 00:04:58,380 --> 00:05:02,520`
Så du kan liksom skapa en användare via ett publikt gränssnitt.



`151 00:05:02,560 --> 00:05:03,960`
Så är du en användare där.



`152 00:05:04,760 --> 00:05:07,560`
Någon sån där self-sign-up-svarbarhet typ.



`153 00:05:08,060 --> 00:05:11,780`
Och om du sen går mot olika tjänster och sånt så funkar ju



`154 00:05:11,780 --> 00:05:16,680`
säkerheten helt okej så länge som du är i liksom användargränssnittet.



`155 00:05:16,680 --> 00:05:17,800`
Liksom är du.



`156 00:05:18,320 --> 00:05:19,180`
I FIFAs.



`157 00:05:19,420 --> 00:05:19,720`
Ja.



`158 00:05:19,720 --> 00:05:20,840`
Har du inte där att göra.



`159 00:05:20,840 --> 00:05:24,760`
Du hoppar in i lite olika sådana här interna nut för nut-applikationer.



`160 00:05:24,760 --> 00:05:25,180`
Så.



`161 00:05:25,680 --> 00:05:26,180`
Så säger.



`162 00:05:26,180 --> 00:05:27,020`
Säger du ju nej.



`163 00:05:27,080 --> 00:05:27,920`
Du får inte vara där och så.



`164 00:05:28,420 --> 00:05:33,000`
Men den kollen av att du liksom är en.



`165 00:05:33,880 --> 00:05:34,320`
Rogue.



`166 00:05:34,400 --> 00:05:38,760`
Att du är en externt liksom upp-signad användare.



`167 00:05:38,780 --> 00:05:39,700`
Jag vill se vart vi är på väg nu.



`168 00:05:40,180 --> 00:05:42,340`
Den ligger helt och hållet i client-side.



`169 00:05:42,640 --> 00:05:44,500`
Och massa back-in-tjänster.



`170 00:05:44,680 --> 00:05:45,080`
Exakt.



`171 00:05:45,280 --> 00:05:50,100`
Om du liksom tar bort den här client-side-kontrollen så är du ju plötsligt



`172 00:05:50,100 --> 00:05:54,320`
inne i interna applikationer.



`173 00:05:54,320 --> 00:05:56,140`
Och den här glada hackaren testade.



`174 00:05:56,180 --> 00:05:59,960`
Två olika system.



`175 00:05:59,960 --> 00:06:03,240`
Ett av dem där man kunde se olika transfermeddelanden och annat.



`176 00:06:03,240 --> 00:06:04,680`
Och man kunde planera om.



`177 00:06:04,680 --> 00:06:07,060`
Och man kunde skicka lite med den i olika tjänster och sådär.



`178 00:06:07,060 --> 00:06:08,980`
Det är det som man skrev där.



`179 00:06:09,020 --> 00:06:10,680`
Det verkar som att om han.



`180 00:06:11,180 --> 00:06:19,280`
Om man skulle våga trycka och liksom verkligen köra skarpt så skulle han kanske kunna ryckerolla hela hela fotbollsvärlden.



`181 00:06:19,820 --> 00:06:26,080`
Och han kunde även då med det här kunde han komma in och få någon.



`182 00:06:26,080 --> 00:06:34,580`
Sorts rättigheter in i deras dev-miljö också så att han kunde gå från produktion till att få någon sorts högre rättigheter inne i utvecklingsmiljön.



`183 00:06:34,580 --> 00:06:48,220`
Så att han han slutade när han hade konstaterat att han kunde ta över en dev-miljö och han hade definitivt rättigheter att köra grejer i två system.



`184 00:06:49,040 --> 00:06:49,980`
Jag är inte förvånad.



`185 00:06:52,140 --> 00:06:54,860`
Good work client-side security liksom.



`186 00:06:55,340 --> 00:06:56,060`
Men man kan säga det.



`187 00:06:56,080 --> 00:06:57,460`
Nej men jag kan nog, jag kan säga det här.



`188 00:06:58,400 --> 00:07:00,160`
Ta bort alla företagsnamn.



`189 00:07:00,160 --> 00:07:02,020`
Ja exakt, jag behöver inte nämna det.



`190 00:07:02,100 --> 00:07:07,460`
Men jag har liksom lyckats registrera i min GCP-konsol för 0x4A.



`191 00:07:08,100 --> 00:07:12,940`
Så jag har lyckats registrera en app för ett annat bolag.



`192 00:07:13,180 --> 00:07:18,720`
Och fått Googles AI att validera min branch, alltså min, vad säger man?



`193 00:07:18,860 --> 00:07:20,560`
Brand verification.



`194 00:07:21,560 --> 00:07:22,860`
Med logotyper.



`195 00:07:23,620 --> 00:07:23,940`
DPR.



`196 00:07:24,780 --> 00:07:25,580`
User agreement.



`197 00:07:25,580 --> 00:07:26,880`
Avtal som inte är mina.



`198 00:07:27,680 --> 00:07:28,080`
Oh.



`199 00:07:28,920 --> 00:07:32,780`
Så de, det är såhär, vi säger ja.



`200 00:07:33,640 --> 00:07:35,760`
Du får, det är okej, allt har gått igenom.



`201 00:07:36,420 --> 00:07:38,240`
Vi återkommer om det är något problem.



`202 00:07:38,780 --> 00:07:39,480`
Och det har de inte gjort.



`203 00:07:39,580 --> 00:07:42,520`
Det är typ två eller tre månader senare.



`204 00:07:43,240 --> 00:07:45,300`
Jag tror att den här hette Agents eller någonting.



`205 00:07:45,460 --> 00:07:46,040`
Det är det hemskt.



`206 00:07:46,060 --> 00:07:47,360`
Man kunde ha regerat sig hos FIFA.



`207 00:07:47,460 --> 00:07:51,320`
Jag vet inte riktigt vad en agent är i fotbollstärmen.



`208 00:07:52,040 --> 00:07:54,640`
Men det är en sån som företräder för spelare tror jag.



`209 00:07:54,800 --> 00:07:55,020`
Ja.



`210 00:07:55,580 --> 00:07:58,980`
Men om man då har nycklat det till till exempel Tenenten.



`211 00:07:59,140 --> 00:08:01,980`
Så att det finns en massa andra såhär under applikationer.



`212 00:08:02,000 --> 00:08:05,960`
Alltså det blir en riktig användare i deras Windows Azure Domain.



`213 00:08:06,240 --> 00:08:09,780`
Då kan man ju tänka sig att om man då bygger en applikation med inloggning.



`214 00:08:10,000 --> 00:08:14,840`
Om man tar då application registrar grejen som identitetskontroll.



`215 00:08:15,060 --> 00:08:18,580`
Så är det såhär, ja alla i våran organisation får väl använda den här.



`216 00:08:18,580 --> 00:08:21,160`
Jo men det är ju några nivåer som gått fel.



`217 00:08:21,160 --> 00:08:25,080`
Det första är ju att en sorts extern användare automatiskt får.



`218 00:08:25,080 --> 00:08:25,620`
Får lov att göra self-sign-up.



`219 00:08:25,620 --> 00:08:26,960`
Får lov att komma in i de interna.



`220 00:08:27,380 --> 00:08:28,780`
Det är ganska vanligt också i alla fall.



`221 00:08:28,960 --> 00:08:32,720`
Kanske inte att, om man typ tuklar med API så kan man ju ibland hitta.



`222 00:08:32,960 --> 00:08:35,040`
Ja men liksom första nivån är ju.



`223 00:08:35,300 --> 00:08:37,140`
Alltså alla får komma in över det.



`224 00:08:37,160 --> 00:08:39,280`
Alltså att uppenbarligen känner man inte till de modellerna.



`225 00:08:39,340 --> 00:08:40,120`
Men det är ju också såhär.



`226 00:08:40,980 --> 00:08:43,220`
Om du faktiskt får gå runt och pilla och läsa allting.



`227 00:08:43,360 --> 00:08:44,940`
Bara du är med i domänen.



`228 00:08:45,160 --> 00:08:46,680`
Så är det ju ganska låga.



`229 00:08:47,120 --> 00:08:48,560`
Ganska låga sådana här.



`230 00:08:49,440 --> 00:08:49,800`
Tröstgrupp.



`231 00:08:49,800 --> 00:08:52,520`
Eller individnivåkontroller i de här API.



`232 00:08:52,900 --> 00:08:54,920`
De har inte gjort någon form av identitets.



`233 00:08:55,080 --> 00:08:55,600`
Identitetsanalys.



`234 00:08:55,840 --> 00:08:58,500`
Så att även om man rättar det här problemet på deras sida.



`235 00:08:59,240 --> 00:08:59,920`
Och det var ju för övrigt.



`236 00:08:59,940 --> 00:09:03,900`
Det var ju tydligen otroligt svårt för honom att få kontakt med någon.



`237 00:09:04,240 --> 00:09:06,960`
Till slut kom han upp och försökte meddela FIFA.



`238 00:09:07,160 --> 00:09:08,440`
Och började höra av sig till FBI.



`239 00:09:08,560 --> 00:09:10,580`
Och be dem fixa det hela på något sätt.



`240 00:09:11,140 --> 00:09:12,440`
Någon får ta det här.



`241 00:09:12,520 --> 00:09:14,920`
För jag får inte FIFA att rätta sina hål.



`242 00:09:15,800 --> 00:09:18,140`
Det är därför Trump nu då vill att han ska komma in i den här.



`243 00:09:18,180 --> 00:09:18,560`
Så är det.



`244 00:09:19,120 --> 00:09:21,620`
För att annars så kommer FBI att stänga av.



`245 00:09:21,620 --> 00:09:24,300`
Ja FBI gjorde FIFA en tjänst nu då kanske.



`246 00:09:24,600 --> 00:09:25,000`
Ja exakt.



`247 00:09:25,600 --> 00:09:29,200`
Återtjänsten är då att det här röda kortet tas bort från den amerikanska spelaren.



`248 00:09:29,280 --> 00:09:30,440`
Så han får spela mot Belgien.



`249 00:09:30,700 --> 00:09:33,200`
Vilket så här för tio år sedan hade varit helt konstigt.



`250 00:09:33,280 --> 00:09:34,960`
Idag typ rätt rimligt ändå.



`251 00:09:35,140 --> 00:09:36,060`
Det är inte alls rimligt.



`252 00:09:36,220 --> 00:09:38,200`
Men det är inte så att man blir förvånad.



`253 00:09:38,680 --> 00:09:43,000`
Om någon lyssnar på det här i framtiden så kan vi ju föra fram termer och teser.



`254 00:09:43,060 --> 00:09:46,360`
Som inte kommer att make any sense at all om man lyssnar på det här i framtiden.



`255 00:09:46,820 --> 00:09:54,460`
Men min nya tes då det är ju att det är FIFA som har klippt hål i liningen där nere i botten.



`256 00:09:54,460 --> 00:09:55,460`
Ja just det på hans pool.



`257 00:09:57,340 --> 00:09:59,100`
Jag tänkte vad han pratar om.



`258 00:09:59,100 --> 00:10:06,580`
Och sen kan man ju då hoppas att ni som lyssnar om tio år i framtiden inte sitter i någon form av idiocracy i samhället.



`259 00:10:06,940 --> 00:10:07,520`
Ja det kan jag ju hoppas.



`260 00:10:07,540 --> 00:10:10,660`
För vi får hoppas att begåvningserisärmen inte bara den rasade.



`261 00:10:11,260 --> 00:10:14,780`
Så om ni hör det här nu att hela Coca-Cola på majsfälten.



`262 00:10:15,380 --> 00:10:15,920`
Bad idea.



`263 00:10:16,160 --> 00:10:16,980`
De behöver vatten.



`264 00:10:18,320 --> 00:10:18,440`
Ja.



`265 00:10:19,060 --> 00:10:24,420`
Men på tal om trasa identiteter och en trasa identitet.



`266 00:10:24,420 --> 00:10:24,440`
Ja.



`267 00:10:24,460 --> 00:10:27,380`
Alltså i molnleverantör som borde ge upp.



`268 00:10:27,460 --> 00:10:28,240`
Jag tänkte annars.



`269 00:10:29,100 --> 00:10:29,940`
Jag följer bara listan.



`270 00:10:30,100 --> 00:10:34,360`
Ja men om vi nu har en seggo i här på den galna presidenten faktiskt.



`271 00:10:34,360 --> 00:10:35,080`
Ja det har vi.



`272 00:10:35,200 --> 00:10:38,340`
Så tänker jag att vi kan fortsätta på den bogen.



`273 00:10:38,440 --> 00:10:42,560`
Alltså det är ju verkligen något som premieras på ett ostruktur.



`274 00:10:42,740 --> 00:10:44,060`
Att vi bara skiter i struktur.



`275 00:10:44,280 --> 00:10:45,660`
Så kör stenhårt.



`276 00:10:45,660 --> 00:10:49,660`
Och jag tänker att det var ju ett supreme court case.



`277 00:10:50,420 --> 00:10:53,600`
Där president Donald Trump var.



`278 00:10:54,460 --> 00:11:08,540`
Ja det är han ju för han valde att byta ut de två demokratiska ledamöterna av Federal Trade Commission.



`279 00:11:08,980 --> 00:11:11,620`
Innan deras term var uppe.



`280 00:11:11,820 --> 00:11:13,100`
Liksom att de skulle inte bytas ut.



`281 00:11:13,760 --> 00:11:18,660`
Och det finns ganska hårda regler för när man får sparka en commissioner från FTC.



`282 00:11:19,660 --> 00:11:21,340`
Men det gjorde han.



`283 00:11:21,340 --> 00:11:23,240`
Och han tog bort dem.



`284 00:11:23,240 --> 00:11:25,580`
För de dansade inte efter hans pipa.



`285 00:11:26,960 --> 00:11:30,560`
Och det här är en av dem.



`286 00:11:31,180 --> 00:11:33,240`
En kvinna som heter Slaughter.



`287 00:11:34,700 --> 00:11:35,240`
I efternamn.



`288 00:11:37,040 --> 00:11:38,820`
Kommer inte ihåg vad hon hette i förnamn dock.



`289 00:11:39,220 --> 00:11:43,400`
Men hon stämde ju presidenten för det här.



`290 00:11:43,500 --> 00:11:45,460`
För det är unconstitutional.



`291 00:11:46,840 --> 00:11:47,520`
Men.



`292 00:11:48,520 --> 00:11:51,660`
Fick rätt uppe i district court.



`293 00:11:51,660 --> 00:11:51,940`
Men.



`294 00:11:53,240 --> 00:11:54,520`
Högsta domstolen.



`295 00:11:55,000 --> 00:11:56,940`
I sin outgrundliga vishet.



`296 00:11:57,020 --> 00:11:59,360`
Och då vet vi ju vem som tillsätter supreme court justices.



`297 00:12:01,020 --> 00:12:07,380`
Tyckte ju att det är unconstitutional att inte presidenten ska få liksom kunna utnyttja sin.



`298 00:12:08,480 --> 00:12:09,180`
Grejen var.



`299 00:12:09,240 --> 00:12:09,760`
Jag läste.



`300 00:12:10,600 --> 00:12:13,920`
Jag läste några av de här utlåtandena.



`301 00:12:14,800 --> 00:12:17,120`
Från de supreme court justices då.



`302 00:12:18,120 --> 00:12:18,800`
Och.



`303 00:12:18,800 --> 00:12:22,480`
Några argumenterade för att det här är liksom del av checks and balances.



`304 00:12:22,480 --> 00:12:27,720`
Precis det det får inte ske på detta viset finns väldigt tydliga regler för när du får avsätta en kommissionär.



`305 00:12:28,360 --> 00:12:28,880`
Blabla.



`306 00:12:29,140 --> 00:12:41,160`
Och så fanns det de som tyckte att ja när fast det här är ju en del av presidentens exekutiva bransch då så att han borde kunna tillsätta och avsätta hur han vill.



`307 00:12:41,680 --> 00:12:42,700`
Och.



`308 00:12:43,720 --> 00:12:49,880`
Det var fler supreme court justices som tyckte att det var en jättebra idé att presidenten kan få köra haywire som han vill.



`309 00:12:50,120 --> 00:12:52,180`
Har inte ni upplevt att det gör liksom.



`310 00:12:52,480 --> 00:12:59,640`
Man har sett ont i den när man tittar på nya tecken det här liksom det är det är det är så läskigt för det är sånt jävla maktspel.



`311 00:13:00,920 --> 00:13:01,440`
Det.



`312 00:13:01,960 --> 00:13:03,480`
Sjuka med den här då.



`313 00:13:03,740 --> 00:13:06,040`
Är ju att det här då får ju.



`314 00:13:06,300 --> 00:13:07,840`
Förlåt.



`315 00:13:08,100 --> 00:13:09,380`
Alla.



`316 00:13:09,640 --> 00:13:13,480`
Som som är sådana riktiga privacy nördar men.



`317 00:13:13,980 --> 00:13:14,500`
Men.



`318 00:13:15,780 --> 00:13:18,080`
Om jag säger så här privacy maffian då.



`319 00:13:18,340 --> 00:13:21,660`
I Europa som Mattias Schrems i.



`320 00:13:22,480 --> 00:13:23,000`
För en.



`321 00:13:24,520 --> 00:13:25,800`
När de vädrar.



`322 00:13:26,060 --> 00:13:29,640`
En en sårbarhet och det här är ju en sårbarhet för det.



`323 00:13:30,420 --> 00:13:34,520`
Federal Trade Commission är det som de som har haft översyn av.



`324 00:13:35,020 --> 00:13:38,860`
Det här som har ersatt privacy shield och så vidare och så vidare.



`325 00:13:39,120 --> 00:13:39,880`
Vad är det den heter?



`326 00:13:40,140 --> 00:13:41,160`
Jag kommer inte ens ihåg.



`327 00:13:41,420 --> 00:13:45,000`
Någon data privacy act kanske.



`328 00:13:45,520 --> 00:13:50,380`
Något data privacy som har gjort att att adekvansbeslutet gäller i EU.



`329 00:13:50,640 --> 00:13:52,180`
Adekvansbeslutet gäller fortfarande.



`330 00:13:52,480 --> 00:13:53,760`
Inte upprivet men.



`331 00:13:54,280 --> 00:13:55,300`
De har skickat ett.



`332 00:13:55,800 --> 00:13:57,600`
Ett argt och långt brev.



`333 00:13:57,860 --> 00:14:03,480`
Till kommissionen och de har stämt dem i EU domstolen så det här kommer bli Schrems 3.



`334 00:14:03,740 --> 00:14:07,580`
Grundproblemet är väl det att det skulle vara en oberoende organisation.



`335 00:14:07,840 --> 00:14:11,160`
Och nu anser de att Federal Trade Commission då inte är en oberoende organisation.



`336 00:14:11,420 --> 00:14:12,200`
Med viss rätta.



`337 00:14:12,440 --> 00:14:16,800`
Ja för att det har ju Supreme Court fastställt att det är presidentens förlängda arm.



`338 00:14:17,320 --> 00:14:20,380`
Det har ju varit lite kött på.



`339 00:14:20,640 --> 00:14:21,160`
Oj.



`340 00:14:21,160 --> 00:14:22,440`
På.



`341 00:14:22,700 --> 00:14:25,000`
Militära grejer där.



`342 00:14:25,520 --> 00:14:27,560`
De pratar om vad fan var ord.



`343 00:14:27,820 --> 00:14:31,920`
Vad var ordformuleringen men någonting typ att vi har.



`344 00:14:32,940 --> 00:14:36,260`
För lite agens eller för lite kontroll över vår egen data.



`345 00:14:36,520 --> 00:14:37,540`
Digital suveränitet.



`346 00:14:37,800 --> 00:14:40,100`
Digital suveränitet kanske var just det.



`347 00:14:40,360 --> 00:14:41,900`
Så att.



`348 00:14:42,660 --> 00:14:49,060`
Vi måste bygga bort den här skiten och ingen vet riktigt hur man gör det snabbt men.



`349 00:14:49,840 --> 00:14:51,880`
Nej och man kan väl säga.



`350 00:14:52,440 --> 00:14:58,580`
Stalltipset är väl att i alla fall börja titta på en exitplan ifrån 365 för att.



`351 00:14:58,840 --> 00:14:59,860`
Ja.



`352 00:15:01,400 --> 00:15:06,000`
Here we go again. Jag tror säkert att det kommer att lösa sig för återigen.



`353 00:15:06,260 --> 00:15:09,840`
Om man läser GDPR och det här blir jag så galen på.



`354 00:15:10,360 --> 00:15:12,160`
Bara för att.



`355 00:15:13,180 --> 00:15:20,600`
USA leds av en idiot och är en totalitär stat så betyder inte det att.



`356 00:15:20,860 --> 00:15:22,140`
Att.



`357 00:15:22,440 --> 00:15:24,480`
Personuppgifter missbrukas.



`358 00:15:24,740 --> 00:15:27,300`
Per definition för att de ligger i Microsofts moln.



`359 00:15:27,560 --> 00:15:28,320`
De kan göra.



`360 00:15:28,580 --> 00:15:29,360`
De kan göra.



`361 00:15:29,600 --> 00:15:30,880`
Men det är frågan då.



`362 00:15:31,140 --> 00:15:31,920`
När.



`363 00:15:33,200 --> 00:15:39,340`
Ska du inte göra en transfer. För jag menar det är ingen som frågar om en transfer till Uzbekistan eller till Ulaanbaatar.



`364 00:15:39,600 --> 00:15:43,940`
Eller till Indien. Hur många använder inte call centers i Indien?



`365 00:15:45,480 --> 00:15:46,500`
Indien.



`366 00:15:46,760 --> 00:15:47,280`
Alltså.



`367 00:15:47,520 --> 00:15:51,120`
Väsentligt sämre skydd för personuppgifter än i USA.



`368 00:15:52,440 --> 00:15:56,280`
Så jag menar. Du måste göra den riskbedömningen.



`369 00:15:56,540 --> 00:15:59,600`
Det är det som stör mig att man liksom inte gör den riskbedömningen.



`370 00:15:59,860 --> 00:16:02,940`
Det är inget som hindrar dig att göra en överfung till tredje land.



`371 00:16:03,200 --> 00:16:08,320`
Så länge du gör riskbedömningen och vidtar åtgärder för att säkerställa att.



`372 00:16:09,080 --> 00:16:12,160`
Det låter dock både jobbigt och tråkigt.



`373 00:16:12,400 --> 00:16:19,580`
Nej det gör ju inte folk. Arrekvansbeslutet har gjort att du inte behöver göra en data transfer impact analysis.



`374 00:16:19,840 --> 00:16:22,140`
Jag tänkte. De håller på att dunka över öronen.



`375 00:16:22,440 --> 00:16:25,260`
Så skriker de. YOLO YOLO YOLO när ni kommer till den.



`376 00:16:25,520 --> 00:16:26,020`
Ja. Jo.



`377 00:16:26,280 --> 00:16:26,800`
Lite så.



`378 00:16:27,300 --> 00:16:33,440`
Nej. Så stalltipset är väl att here we go again. Nu kommer det en ny tjänstdom snart.



`379 00:16:33,700 --> 00:16:36,260`
Och så är USA på svarta listan igen.



`380 00:16:36,520 --> 00:16:39,840`
Och så bygger de ett nytt. Och så bygger de ett nytt privacy shield 3.



`381 00:16:40,100 --> 00:16:43,680`
Ja exakt. Och så kommer det efter ett tag att rivas igen.



`382 00:16:43,940 --> 00:16:46,500`
Grundproblemet finns ju där fortfarande. Men där kommer vi inte ifrån.



`383 00:16:47,280 --> 00:16:52,140`
Vi behöver en vettig president som river upp massa idiotbeslut som.



`384 00:16:52,140 --> 00:16:53,680`
Andra har fattat.



`385 00:16:54,960 --> 00:16:55,460`
Yes yes.



`386 00:16:55,720 --> 00:16:58,280`
Typ Cloudact och lite sådana här.



`387 00:16:59,300 --> 00:17:03,400`
Ska vi hoppa tillbaka nu då för att inte följa någon form utav symmetri?



`388 00:17:03,660 --> 00:17:04,680`
Ja. Nu hoppar vi tillbaka.



`389 00:17:04,940 --> 00:17:06,740`
Då tänkte jag att vi skulle prata om. Hör och häpna.



`390 00:17:07,240 --> 00:17:08,260`
GitHub Actions.



`391 00:17:08,520 --> 00:17:09,300`
Yay\!



`392 00:17:09,540 --> 00:17:11,080`
För det har jag aldrig pratat om tidigare.



`393 00:17:11,600 --> 00:17:12,880`
Men nu ska vi faktiskt prata om en bra sak.



`394 00:17:13,380 --> 00:17:18,760`
Och vi ska då alltså prata om att GitHub har faktiskt uppdaterat Actions Checkout till version 7.



`395 00:17:19,540 --> 00:17:21,840`
Och det är ganska bra.



`396 00:17:22,140 --> 00:17:24,180`
Ja det är ju kanon.



`397 00:17:24,440 --> 00:17:27,780`
Det är det faktiskt. Nu har de implementerat.



`398 00:17:28,800 --> 00:17:36,480`
De har blockerat ganska standardiserade attackvägar som är



`399 00:17:36,740 --> 00:17:39,540`
Insecure defaults kan man säga i en checkout.



`400 00:17:39,800 --> 00:17:40,820`
I ett checkout-flöde.



`401 00:17:41,340 --> 00:17:42,880`
Och det de har gjort nu då det är att



`402 00:17:43,380 --> 00:17:45,940`
Har vi koll på git checkout vad den gör?



`403 00:17:46,200 --> 00:17:49,280`
Nej jag tänkte just fråga det. Vet alla vad en checkout är?



`404 00:17:49,540 --> 00:17:51,060`
Jag kan ju killlisa vad det är.



`405 00:17:51,060 --> 00:17:51,840`
Action Checkout.



`406 00:17:51,840 --> 00:17:55,160`
Det är typ det första som händer när man kör en action.



`407 00:17:55,420 --> 00:17:56,960`
Det är typ git clone.



`408 00:17:57,220 --> 00:17:59,780`
Vanligt sätt att bygga det kan man säga.



`409 00:18:00,040 --> 00:18:00,540`
Ja exakt.



`410 00:18:00,800 --> 00:18:01,320`
Det är sant.



`411 00:18:01,560 --> 00:18:02,600`
Det här är ju också då en switch.



`412 00:18:02,840 --> 00:18:04,900`
Det pratade vi om förut att Peter har valt att inte göra så.



`413 00:18:05,160 --> 00:18:05,660`
Exakt.



`414 00:18:05,660 --> 00:18:10,020`
Och det finns en massa olika grejer som det här vi kommer prata om inte.



`415 00:18:10,520 --> 00:18:13,860`
Git clone och git checkout är väl olika saker.



`416 00:18:14,120 --> 00:18:18,460`
Nu är inte jag utvecklare så jag har ingen aning om vad jag pratar om.



`417 00:18:18,720 --> 00:18:20,760`
Ja men action checkout.



`418 00:18:20,760 --> 00:18:26,900`
Ja alltså tänkte jag att det här är en hel bröta med grejer.



`419 00:18:27,420 --> 00:18:31,000`
Du skriver en rad i din yaml och sen bara



`420 00:18:31,520 --> 00:18:36,380`
magiinträffar inne i kod och grejer som du aldrig ser.



`421 00:18:36,640 --> 00:18:40,720`
Clone är ju bara så här. Det jag menar med att det första som händer är git clone.



`422 00:18:40,980 --> 00:18:44,060`
Då drar du ner källkod och sen kan du börja titta på källkoden.



`423 00:18:44,320 --> 00:18:48,920`
Actions checkout är liksom det första raden som actionen ska göra.



`424 00:18:48,920 --> 00:18:52,500`
Precis som Peter säger det kan innehålla hur mycket mayhem som helst.



`425 00:18:52,760 --> 00:18:58,140`
Men vad den gör i ett standardläge som svar på frågan det är ju att den



`426 00:18:59,160 --> 00:19:04,020`
Den griper ju ett tag. Någonstans så finns det ju ett



`427 00:19:05,040 --> 00:19:08,640`
Ett token som är kortlivat.



`428 00:19:09,140 --> 00:19:12,220`
Som har vissa rättigheter kopplade till det här workflowet.



`429 00:19:12,480 --> 00:19:13,500`
Ja.



`430 00:19:13,760 --> 00:19:16,820`
Action checkout tar det tokenet och lägger in det



`431 00:19:16,820 --> 00:19:20,920`
På någon ställe inne i den här virtuella maskinen som



`432 00:19:21,180 --> 00:19:22,460`
Execuerar ditt workflow.



`433 00:19:22,700 --> 00:19:26,540`
För att gå på Rickards analogi för att vara asenkelt.



`434 00:19:27,060 --> 00:19:30,900`
Den klonar repot till en virtuell maskin som kör workflowet.



`435 00:19:31,160 --> 00:19:32,940`
Och den löser allt det som



`436 00:19:33,200 --> 00:19:37,040`
Är jobbigt som inte vi fattar om vi är dumma och inte analyserar problem mycket.



`437 00:19:37,300 --> 00:19:38,840`
Allt det som gör det enkelt.



`438 00:19:39,100 --> 00:19:42,940`
Som gör att ingen behöver tänka när de jobbar med det.



`439 00:19:43,180 --> 00:19:45,500`
Actions slash checkout är det som



`440 00:19:45,740 --> 00:19:46,520`
Som den gör allt.



`441 00:19:46,820 --> 00:19:49,900`
All git-magin och alla rättigheters magier och sånt för att det ska funka.



`442 00:19:50,140 --> 00:19:51,180`
Och här finns det massa



`443 00:19:51,420 --> 00:19:52,460`
Exploateringsvektorer.



`444 00:19:52,700 --> 00:19:53,740`
Ni som pratar med mig



`445 00:19:53,980 --> 00:19:56,540`
Vet att det finns en miljard och ni som har liksom



`446 00:19:56,800 --> 00:19:58,600`
Googlat vet att det finns en miljard



`447 00:19:59,100 --> 00:19:59,880`
Sårbarheter här.



`448 00:20:00,640 --> 00:20:05,260`
Och det finns en miljon olika scanners och linters och best practices och så vidare. Men det som händer nu då är att de har



`449 00:20:05,500 --> 00:20:06,280`
Tatt ansvar själva.



`450 00:20:06,540 --> 00:20:09,340`
Så de har patchat eller blockerat har de gjort såhär



`451 00:20:09,600 --> 00:20:10,880`
Kända



`452 00:20:11,140 --> 00:20:13,700`
Pwn requests har de väl valt att döpa det till.



`453 00:20:13,960 --> 00:20:14,980`
Och det är typ som att



`454 00:20:15,240 --> 00:20:16,780`
Actionen vägrar hämta koden.



`455 00:20:17,080 --> 00:20:20,140`
Både ifrån till exempel forkade push requests eller pull requests.



`456 00:20:20,920 --> 00:20:24,760`
I olika workflows som kör. För det här kan ju nästla då så man kan ju liksom



`457 00:20:25,260 --> 00:20:30,140`
Köra igång någonting som hämtar någonting här borta som hämtar någonting där som gör det här så att



`458 00:20:30,380 --> 00:20:30,900`
Då har de



`459 00:20:31,160 --> 00:20:31,660`
Då har de sagt att



`460 00:20:31,920 --> 00:20:33,200`
Ja men vi har dratt



`461 00:20:33,720 --> 00:20:39,100`
När vi tittar på hur saker och ting körs och när vi tittar på malicious payloads så kan vi konstatera att de här partsen



`462 00:20:39,340 --> 00:20:42,680`
Har egentligen ingen legitim idé att finnas på det här sättet.



`463 00:20:42,940 --> 00:20:44,220`
Så då plockar vi bort dem.



`464 00:20:46,000 --> 00:20:46,780`
Och vad som händer då



`465 00:20:47,080 --> 00:20:51,180`
Om man kör en pull request target eller workflow run



`466 00:20:52,960 --> 00:20:58,600`
Då triggas de här olika rättigheterna då med precis som Peter är inne på här med tokens och det är de här tredje.



`467 00:20:59,100 --> 00:21:00,140`
Och det är det de har



`468 00:21:00,380 --> 00:21:01,660`
Idén med det här



`469 00:21:01,920 --> 00:21:04,220`
Tror jag det är för att man ska försöka mota



`470 00:21:04,480 --> 00:21:08,060`
Mota bort de här supply chain attackerna nu då så att man inte bara helt



`471 00:21:08,580 --> 00:21:10,880`
Blint lita på saker och ting



`472 00:21:11,400 --> 00:21:13,700`
Jag vågar hävda att det gör man ändå



`473 00:21:13,960 --> 00:21:14,980`
För att det finns



`474 00:21:15,240 --> 00:21:16,780`
Oändligt mycket



`475 00:21:17,080 --> 00:21:21,180`
Funktionalitet som kan konsumera osäker kod och paths ändå



`476 00:21:21,680 --> 00:21:24,760`
Men vad det gör är att den har i alla fall en



`477 00:21:25,260 --> 00:21:26,300`
Vissa patterns



`478 00:21:26,800 --> 00:21:29,880`
Får inte förekomma liksom shit that should not be



`479 00:21:30,140 --> 00:21:31,160`
Har de ändå tagit bort



`480 00:21:31,420 --> 00:21:32,700`
Och det är en bra grej



`481 00:21:33,200 --> 00:21:33,720`
Så



`482 00:21:34,480 --> 00:21:39,340`
Normalt är väl det vanligaste är väl pull request target det är väl en av de vanligaste



`483 00:21:39,600 --> 00:21:41,400`
Och action checkouts det är typ att man



`484 00:21:41,900 --> 00:21:46,780`
Man kör ett basrepo i ett kontext man tror men den plockar ner massa grejer som den är.



`485 00:21:47,080 --> 00:21:47,840`
Som den inte kan validera



`486 00:21:48,100 --> 00:21:49,900`
Och det gör den ju oftast med ganska höga rättigheter



`487 00:21:50,140 --> 00:21:51,940`
Det är en sån här klassisk supply chain



`488 00:21:52,460 --> 00:21:54,240`
Stöka då det vill säga att vi



`489 00:21:54,760 --> 00:22:00,140`
Vi bygger en Node.js applikation och så plockar vi hem de här olika npm-paketen och vi validerar inte dem



`490 00:22:00,380 --> 00:22:01,160`
Och vad de kör



`491 00:22:01,420 --> 00:22:04,480`
För det liksom ligger utanför våran kontroll liksom



`492 00:22:05,000 --> 00:22:06,020`
Det är väl en klassisk sån grej



`493 00:22:06,780 --> 00:22:12,160`
Och det de gör nu då är att de vägrar checka ut forkad kod i vissa workflows då



`494 00:22:13,180 --> 00:22:14,980`
Så det är bra så då kan man liksom



`495 00:22:15,240 --> 00:22:16,000`
Ja när



`496 00:22:16,260 --> 00:22:18,040`
Pull requesten kommer så kan det liksom



`497 00:22:18,560 --> 00:22:21,380`
Ja eller när man försöker checka ut något eller vad man nu vill göra så



`498 00:22:21,640 --> 00:22:23,940`
Sen tror man kan tänka på det här som att



`499 00:22:25,720 --> 00:22:31,100`
De vet att i action checkouts används i nästan alla workflow och



`500 00:22:31,620 --> 00:22:33,160`
Framförallt workflow som vill



`501 00:22:33,660 --> 00:22:35,720`
Jobba med den här tokenet och sånt



`502 00:22:36,740 --> 00:22:37,240`
Och



`503 00:22:38,020 --> 00:22:39,300`
Då har man liksom



`504 00:22:39,560 --> 00:22:42,880`
Och det här tokenet vi pratar om nu då det är liksom när workflowen drar igång



`505 00:22:43,140 --> 00:22:45,180`
Så får den en liten liten sträng



`506 00:22:45,180 --> 00:22:47,480`
Den strängen lever ganska kort men har



`507 00:22:47,740 --> 00:22:49,540`
Normalt sett extremt höga rättigheter



`508 00:22:50,560 --> 00:22:53,120`
Ja och det är komfa, det är ju lite workflow också



`509 00:22:53,380 --> 00:22:55,940`
Men grejen är alltså att den



`510 00:22:57,220 --> 00:23:00,020`
Vad de gör i den här action-grunkan är att de



`511 00:23:01,300 --> 00:23:02,580`
Har identifierat



`512 00:23:02,840 --> 00:23:04,900`
Ett antal kända abuse case



`513 00:23:05,140 --> 00:23:07,700`
Och de kan då blockas då så att



`514 00:23:07,960 --> 00:23:12,060`
Man lägger lite plåster på grejet där där man tar bort



`515 00:23:12,320 --> 00:23:14,100`
Ett par stycken kända



`516 00:23:14,360 --> 00:23:14,860`
Ja



`517 00:23:14,860 --> 00:23:19,720`
Vi har pratat om post-hoc, vi har pratat om lite emacs magi



`518 00:23:19,980 --> 00:23:21,260`
Kubernetes EEL



`519 00:23:21,520 --> 00:23:22,280`
Var ju en grej



`520 00:23:22,540 --> 00:23:25,100`
Så att det här är ju för att liksom



`521 00:23:25,620 --> 00:23:28,680`
Mota de här supply chain trenderna



`522 00:23:28,940 --> 00:23:30,980`
Och i förra avsnittet snackade vi om att



`523 00:23:32,020 --> 00:23:37,640`
GitHub som tydligen på något sätt är med och driver npm det var en nyhet för mig men



`524 00:23:38,160 --> 00:23:42,000`
Man har härdat upp den mot vissa attackvektorer och sånt



`525 00:23:42,260 --> 00:23:44,300`
Postinstall är väl default av till exempel



`526 00:23:44,860 --> 00:23:48,440`
Men nu så tar man i en annan del av den här



`527 00:23:48,700 --> 00:23:53,060`
Lösningen och infrastrukturen så patchar man bort några av de här attackvektorerna till och så



`528 00:23:53,560 --> 00:23:56,900`
Så det känns som att en av de här är ett helhetsgrepp



`529 00:23:57,140 --> 00:24:00,980`
Men att man på olika ställen börjar man lappa undan de vanligaste



`530 00:24:01,500 --> 00:24:05,600`
Men i sann Göteborgslanda så måste man göra lite ironi och satir av saker och ting



`531 00:24:06,880 --> 00:24:08,660`
För att i och med att man har patchat det här



`532 00:24:08,920 --> 00:24:14,300`
Så har man givetvis skapat allow, unsafe, PR, checkout, true or false



`533 00:24:14,860 --> 00:24:16,900`
Som en cool liten flagga



`534 00:24:17,420 --> 00:24:22,280`
Så om man känner att jag är fan men inte nymodig nog att ta de här



`535 00:24:22,540 --> 00:24:23,560`
Version 7 så kan man



`536 00:24:23,820 --> 00:24:24,840`
Unleaving all the edge



`537 00:24:25,100 --> 00:24:27,140`
Så kan man faktiskt behålla det gamla



`538 00:24:27,400 --> 00:24:30,220`
Gamla beteendet men då får man också äga den risken



`539 00:24:30,980 --> 00:24:32,780`
Men okej vad behöver man göra som utvecklare då



`540 00:24:34,060 --> 00:24:40,200`
Om man har pull request target som checkar ut forkadkort som man inte kontrollerar själv så kommer de inte att fejla liksom



`541 00:24:40,460 --> 00:24:41,220`
Det kommer inte gå



`542 00:24:41,480 --> 00:24:42,000`
Helt enkelt



`543 00:24:42,500 --> 00:24:43,540`
Och då är



`544 00:24:43,780 --> 00:24:44,820`
Githubs rekommendation



`545 00:24:45,120 --> 00:24:46,900`
Att man ska byta till vanliga pull request



`546 00:24:47,160 --> 00:24:47,940`
Byt jobb



`547 00:24:48,440 --> 00:24:50,240`
Ja men absolut



`548 00:24:51,000 --> 00:24:52,540`
Och du behöver liksom inte



`549 00:24:52,800 --> 00:24:53,300`
Liksom



`550 00:24:53,560 --> 00:24:54,080`
Som du



`551 00:24:54,340 --> 00:24:55,360`
Peter säger som är edspotlån



`552 00:24:55,620 --> 00:24:57,140`
Man behöver liksom inte hålla på och greja med



`553 00:24:57,400 --> 00:25:01,500`
Rättigheter och göra massa konstiga grejer utan det blir nog bra men det är ju



`554 00:25:02,520 --> 00:25:03,800`
Det täcker ju bara



`555 00:25:04,060 --> 00:25:05,860`
Action checkouts i nuläget då



`556 00:25:07,140 --> 00:25:08,920`
Men tar du till exempel då



`557 00:25:10,200 --> 00:25:11,480`
Ska jag hitta på något där, ja snabbt på uppstånd



`558 00:25:11,740 --> 00:25:13,280`
Men typ git fetch till exempel



`559 00:25:13,780 --> 00:25:14,560`
Ja det kommer



`560 00:25:14,860 --> 00:25:16,140`
Det funkar precis som vanligt



`561 00:25:16,400 --> 00:25:18,960`
Nej men ett annan tips kan ju vara om du har kodat



`562 00:25:19,720 --> 00:25:21,780`
Hela din egen snurra där du



`563 00:25:22,020 --> 00:25:23,820`
Till exempel du kan ju lägga upp en sån här



`564 00:25:24,340 --> 00:25:28,180`
Person access token eller någonting du kan lägga upp som en secret



`565 00:25:28,420 --> 00:25:30,480`
Pat är ju jättevanligt och det funkar ju



`566 00:25:30,740 --> 00:25:31,500`
Precis lika bra



`567 00:25:31,760 --> 00:25:34,320`
Och den håller sjukt mycket längre än de andra tokensarna



`568 00:25:34,580 --> 00:25:35,600`
Precis men gör inte det



`569 00:25:35,860 --> 00:25:37,640`
Men fuckar du upp det här



`570 00:25:38,160 --> 00:25:39,700`
Och



`571 00:25:39,940 --> 00:25:40,980`
Så vet ju



`572 00:25:41,480 --> 00:25:42,000`
Alltså sån där



`573 00:25:42,260 --> 00:25:43,780`
Action check out vet ju inte om



`574 00:25:43,780 --> 00:25:44,300`
Dom



`575 00:25:44,860 --> 00:25:47,160`
Problem och fel som du själv skapar liksom



`576 00:25:47,420 --> 00:25:49,460`
Och så har du byggt



`577 00:25:49,720 --> 00:25:53,060`
Har du byggt din egen sätt att få ut källkod och få ut grejer och sånt liksom



`578 00:25:53,300 --> 00:25:59,700`
Då kommer ju inte det här hjälpa dig för då är du inte med i den säkrade workflow vägen



`579 00:25:59,960 --> 00:26:01,500`
Så det här är ju



`580 00:26:02,020 --> 00:26:07,380`
Om man nu använder det så som det är tänkt att användas vilket alla gör uppenbarligen för att det är därför man behöver imprimera en



`581 00:26:07,640 --> 00:26:08,920`
Flagga som heter



`582 00:26:09,180 --> 00:26:10,720`
Allow and save PRs



`583 00:26:11,220 --> 00:26:12,260`
Som ni hör



`584 00:26:12,500 --> 00:26:13,780`
Då



`585 00:26:13,780 --> 00:26:17,620`
Men men men det är ju en bra bit på vägen det är också så här vi har förstått att det här



`586 00:26:17,880 --> 00:26:18,640`
Är svårt



`587 00:26:18,900 --> 00:26:20,700`
Så vi tar bort de mest obvious



`588 00:26:20,940 --> 00:26:21,460`
Insecure defaults



`589 00:26:21,720 --> 00:26:23,000`
Så det blir ju ett litet plåster då



`590 00:26:23,760 --> 00:26:29,900`
Det finns ju kanske några människor som faktiskt är gurus och gudar på det här som faktiskt kan förstå



`591 00:26:30,420 --> 00:26:31,960`
Alla säkerhetsimplementationer



`592 00:26:32,460 --> 00:26:34,260`
Kan ta andras push



`593 00:26:34,520 --> 00:26:36,560`
Såhär och exekvera dom



`594 00:26:36,820 --> 00:26:38,360`
Och veta att det är säkert



`595 00:26:38,620 --> 00:26:39,120`
Och så såhär



`596 00:26:39,380 --> 00:26:41,680`
Det finns ju tusen möjligheter att skjuta sig i foten



`597 00:26:41,940 --> 00:26:43,740`
Som folk har gjort tidigare men



`598 00:26:44,040 --> 00:26:45,060`
Men det är ju säkert så



`599 00:26:45,820 --> 00:26:48,900`
Det är ju inte alla som har använt pull request target som varit osäkra i det stora sättet



`600 00:26:49,160 --> 00:26:52,740`
Så att det finns ju några människor som kan get to work plus och är



`601 00:26:53,500 --> 00:26:56,320`
Liksom kan bolla med dom här glada lava bollarna



`602 00:26:56,580 --> 00:26:57,860`
Det här är ju en trendgrej nu



`603 00:26:58,120 --> 00:27:00,420`
Det vill säga att vi ska identitetskoppla



`604 00:27:00,680 --> 00:27:02,460`
Tråkiga grejer som repon



`605 00:27:02,980 --> 00:27:04,780`
Det gjorde man ju inte förr i tiden det var liksom inte



`606 00:27:05,280 --> 00:27:08,860`
Man hade sin jävla SSO-nyckel så genererade man en patt eller så



`607 00:27:09,120 --> 00:27:13,740`
Man hade en PGP-nyckel för det här också liksom men det var liksom jävligt boring



`608 00:27:14,040 --> 00:27:17,880`
Och sen så gjorde man någon form av nyckelsarmoni på sitt utvecklad bolag och så



`609 00:27:18,140 --> 00:27:19,160`
Fick man access till repon



`610 00:27:19,420 --> 00:27:24,280`
Men nu har man ju kopplat logik och andra IAM-rättigheter och cloud och



`611 00:27:24,540 --> 00:27:27,860`
Orkestrering och allting så man tog någonting som var svårt att förstå



`612 00:27:28,120 --> 00:27:30,420`
Kopplade ihop det med någonting som var ännu svårare att förstå



`613 00:27:30,680 --> 00:27:33,740`
Och sen så slängde man in oåterringen också för att



`614 00:27:34,000 --> 00:27:36,300`
Do something with complex authentication



`615 00:27:36,560 --> 00:27:38,100`
Och sen tänkte man det här blir bra



`616 00:27:38,620 --> 00:27:41,940`
Det är ju så jävla roligt för det är liksom mer



`617 00:27:42,200 --> 00:27:43,740`
Mer av samma soppa egentligen



`618 00:27:44,040 --> 00:27:44,540`
Bara att



`619 00:27:44,800 --> 00:27:46,340`
Okej nu funkar det ändå ganska bra



`620 00:27:46,600 --> 00:27:47,880`
Let's make it over again



`621 00:27:48,140 --> 00:27:51,720`
Och det är ju ändå bra att man tar lite ansvar här från GIT-sidan då



`622 00:27:52,740 --> 00:27:54,540`
Det var nästan en liten bakåtreferens där



`623 00:27:54,780 --> 00:27:56,060`
Let's make GIT upgrade again



`624 00:27:56,320 --> 00:27:56,840`
Ja exakt



`625 00:27:57,100 --> 00:27:57,600`
Hashtag



`626 00:27:58,620 --> 00:27:59,400`
Morotsmannen



`627 00:28:00,940 --> 00:28:06,560`
Och där tänker jag att vi är klara där och kanske ska prata lite Windows när vi ändå är inne på dåliga saker



`628 00:28:10,140 --> 00:28:10,920`
En intressant bygga



`629 00:28:11,180 --> 00:28:11,680`
Ja



`630 00:28:11,940 --> 00:28:13,220`
Ja



`631 00:28:13,480 --> 00:28:16,040`
, de har ju haft intressanta dagar



`632 00:28:16,300 --> 00:28:17,060`
Ja de är väl jämnt



`633 00:28:17,320 --> 00:28:19,620`
Är det någon gång någon på Microsoft kommer hit och säger



`634 00:28:19,880 --> 00:28:20,640`
Undrar vad ska jag göra idag



`635 00:28:22,180 --> 00:28:24,220`
Och som inte har med att släcka någon form av eld



`636 00:28:24,480 --> 00:28:31,660`
Men med bland nyheterna vi strök vid något tidigare tillfälle var ju det faktum att



`637 00:28:32,420 --> 00:28:34,460`
Lite Secure Boot



`638 00:28:34,720 --> 00:28:36,520`
Certifikat håller på att gå ut



`639 00:28:37,280 --> 00:28:41,900`
Så om man inte fått in uppdateringen för att stödja nya Secure Boots



`640 00:28:42,140 --> 00:28:43,180`
Certifikaten om man hade



`641 00:28:43,480 --> 00:28:43,980`
En väldigt



`642 00:28:44,760 --> 00:28:49,620`
Gammal installation så helt plötsligt så botade ju inte datorn längre



`643 00:28:52,440 --> 00:28:58,580`
Och det var ju någon gång, jag tror det var i juni när omstarten gick ut så en liten procentandel hade ju problem



`644 00:28:58,840 --> 00:28:59,860`
Med detta



`645 00:29:00,620 --> 00:29:03,440`
Samtidigt så släpptes det



`646 00:29:04,220 --> 00:29:04,720`
Typ



`647 00:29:06,260 --> 00:29:08,820`
200 fixar



`648 00:29:10,360 --> 00:29:12,660`
Varav några av fixarna



`649 00:29:12,660 --> 00:29:13,940`
På senast patch 2



`650 00:29:14,200 --> 00:29:15,480`
Varav några av fixarna då



`651 00:29:15,980 --> 00:29:17,020`
Löste



`652 00:29:17,260 --> 00:29:18,300`
Några av den här



`653 00:29:18,540 --> 00:29:19,580`
Nightmare Eclipse



`654 00:29:19,820 --> 00:29:22,380`
Rage Disclosures



`655 00:29:23,660 --> 00:29:24,180`
Och



`656 00:29:27,000 --> 00:29:27,760`
Han har ju



`657 00:29:28,020 --> 00:29:30,060`
Han, hon, vem nu



`658 00:29:30,320 --> 00:29:31,100`
Den det



`659 00:29:31,340 --> 00:29:34,940`
Den det som är Nightmare Eclipse har ju också då släppt



`660 00:29:35,440 --> 00:29:36,460`
Ytterligare än en



`661 00:29:36,720 --> 00:29:37,740`
Rogue Planet



`662 00:29:40,060 --> 00:29:41,840`
Attack kedja där du går



`663 00:29:42,660 --> 00:29:46,240`
Från lägsta rättigheterna i Windows



`664 00:29:46,760 --> 00:29:50,860`
Studsar lite via Windows Defender och så helt plötsligt så



`665 00:29:51,360 --> 00:29:54,940`
Hoppas det att se om det är Skal som kör med



`666 00:29:55,200 --> 00:29:57,000`
Vad är det, Local System?



`667 00:29:57,260 --> 00:30:01,860`
Jäkligt cool time of check, time of use attack där alltså



`668 00:30:02,120 --> 00:30:03,400`
Blev det kalk?



`669 00:30:04,420 --> 00:30:08,780`
När han bytte



`670 00:30:09,540 --> 00:30:11,080`
Eller hon, henne



`671 00:30:11,340 --> 00:30:12,360`
Den, den



`672 00:30:12,660 --> 00:30:18,800`
Personen med oklar könighet



`673 00:30:19,060 --> 00:30:21,100`
Poppade ett riktigt



`674 00:30:21,360 --> 00:30:22,900`
CMD-skala istället för kalk



`675 00:30:23,160 --> 00:30:24,440`
Det är 2.0



`676 00:30:24,700 --> 00:30:29,040`
Vill du specifikt köra kalk så får du liksom skriva kalk där när du lägger in och kör som system



`677 00:30:29,560 --> 00:30:31,340`
Vilket jag inte vet om man kan göra men det



`678 00:30:31,600 --> 00:30:32,120`
Kanske man kan



`679 00:30:32,880 --> 00:30:34,160`
Ja men det kan man



`680 00:30:34,940 --> 00:30:35,440`
Har du testat?



`681 00:30:36,220 --> 00:30:37,740`
I CMD är det bara att skriva kalk



`682 00:30:38,260 --> 00:30:39,800`
Även om man är system så



`683 00:30:40,060 --> 00:30:41,840`
Det tänker jag, system räknar bäst



`684 00:30:42,660 --> 00:30:46,500`
Jag kör, jag kör alla mina kalks



`685 00:30:46,760 --> 00:30:49,320`
Jag kör alla mina kalks som system



`686 00:30:49,580 --> 00:30:50,860`
Bara för att säga



`687 00:30:51,100 --> 00:30:53,920`
Man vill inte att kalk ska ha problem med att den är för låg



`688 00:30:54,180 --> 00:30:55,460`
I do it as system



`689 00:30:56,740 --> 00:30:59,820`
Run as administrator



`690 00:31:00,060 --> 00:31:02,120`
Men någonstans i de här



`691 00:31:03,140 --> 00:31:05,960`
Rörorna där det hänt ett antal grejer så



`692 00:31:06,460 --> 00:31:09,540`
Har det ju kommit olika gnäll om att folk har



`693 00:31:09,800 --> 00:31:10,560`
Problem



`694 00:31:10,560 --> 00:31:14,140`
Och jag vet inte hur mycket som är allmänt buss



`695 00:31:14,400 --> 00:31:16,700`
Microsoft hade släppt om någon normal



`696 00:31:16,960 --> 00:31:18,760`
Släppte en advisory där det var en



`697 00:31:19,000 --> 00:31:21,820`
Small percentage eller någonting liknande



`698 00:31:22,080 --> 00:31:24,640`
Eller few affected users eller något sådant



`699 00:31:25,160 --> 00:31:29,500`
Dels så var det tydligen vissa laptopar som installerade med en



`700 00:31:30,780 --> 00:31:32,060`
Med en sån här



`701 00:31:35,900 --> 00:31:38,980`
En Windows recovery partition eller någonting som var för liten



`702 00:31:39,240 --> 00:31:40,260`
Någon av de här



`703 00:31:40,560 --> 00:31:44,140`
Små osynliga partitionerna var ju i varje fall för små på en del laptops



`704 00:31:44,400 --> 00:31:46,440`
Det gick liksom inte att installera uppdateringarna



`705 00:31:46,960 --> 00:31:49,000`
I och med att man installerar



`706 00:31:49,520 --> 00:31:50,280`
Ja



`707 00:31:50,540 --> 00:31:53,620`
Så det är ju kommet instruktioner på hur



`708 00:31:54,120 --> 00:31:57,720`
Hur gör du för att få igång din dator när den inte kan bota överhuvudtaget



`709 00:31:58,480 --> 00:32:01,300`
Och lite annat sådant där



`710 00:32:02,320 --> 00:32:03,340`
Så ja



`711 00:32:04,360 --> 00:32:05,140`
Coolt



`712 00:32:05,400 --> 00:32:07,960`
Mycket blandat Windows drama



`713 00:32:08,200 --> 00:32:10,260`
Det låter som vilken annan vecka som helst



`714 00:32:10,560 --> 00:32:13,120`
Jag tycker att vi ska prata routersäkerhet nu för symmetri



`715 00:32:13,380 --> 00:32:14,140`
Är ju värdelöst



`716 00:32:14,920 --> 00:32:15,940`
Hur menar du?



`717 00:32:16,200 --> 00:32:17,980`
Att vi hoppar ner en öppen



`718 00:32:18,240 --> 00:32:21,560`
Jasper reorder on the fly



`719 00:32:21,820 --> 00:32:22,600`
Treadmark



`720 00:32:22,840 --> 00:32:24,120`
Ja men jag ska prata routersäkerhet



`721 00:32:25,400 --> 00:32:27,960`
Det är två stycken jätteroliga



`722 00:32:28,220 --> 00:32:30,280`
CVR som kommit ut i



`723 00:32:30,520 --> 00:32:31,040`
Du sa



`724 00:32:31,300 --> 00:32:35,140`
Du kallar det för Acker, jag kallar det för Acer, vad kallar ni det? A-C-E-R



`725 00:32:35,400 --> 00:32:35,900`
Acer



`726 00:32:36,160 --> 00:32:37,180`
Acer är ännu bättre



`727 00:32:37,440 --> 00:32:38,720`
Acer tror jag du också kallar det



`728 00:32:38,980 --> 00:32:40,260`
Vad kallar du det? Acker?



`729 00:32:40,560 --> 00:32:41,580`
Acer, han sa Acker



`730 00:32:41,840 --> 00:32:42,360`
Acker?



`731 00:32:42,860 --> 00:32:43,640`
Acer säger vi



`732 00:32:45,680 --> 00:32:47,220`
Hur fan kan det bli K?



`733 00:32:47,480 --> 00:32:47,980`
Ja skitsamma



`734 00:32:48,240 --> 00:32:50,040`
Men det är engelska eller?



`735 00:32:50,280 --> 00:32:52,840`
Acer säger jag, det är på svenska Acer



`736 00:32:53,360 --> 00:32:54,640`
Men Acer låter ju helt rätt



`737 00:32:54,900 --> 00:32:55,660`
Det låter ju helt rätt



`738 00:32:55,920 --> 00:32:56,440`
Acer



`739 00:32:56,680 --> 00:32:58,480`
Jag tänker också att det är så



`740 00:32:58,740 --> 00:32:59,240`
Ja förlåt



`741 00:32:59,500 --> 00:33:02,840`
Acer de bygger massa grejer bland annat routers



`742 00:33:03,080 --> 00:33:03,860`
Bland annat



`743 00:33:04,120 --> 00:33:05,140`
Mesh routers



`744 00:33:05,640 --> 00:33:07,960`
Vad vet vi om mesh routers från förra avsnittet?



`745 00:33:08,200 --> 00:33:10,520`
Att vi har en tåg på Securitfest



`746 00:33:10,820 --> 00:33:12,600`
Men det här är då



`747 00:33:12,860 --> 00:33:15,420`
Av modellen Wave 7



`748 00:33:15,680 --> 00:33:18,240`
Då vet man ju förmodligen att det finns Wave 1, 2, 3, 4, 5, 6, 7 också



`749 00:33:19,520 --> 00:33:22,080`
Men två stycken feta



`750 00:33:22,340 --> 00:33:23,100`
Sårbeter



`751 00:33:23,360 --> 00:33:24,640`
Båda ser vi i



`752 00:33:24,900 --> 00:33:25,660`
Eller ser vi i SS10



`753 00:33:26,680 --> 00:33:27,460`
Den första



`754 00:33:27,960 --> 00:33:30,020`
Är ju mest bizarr då i min bok



`755 00:33:30,280 --> 00:33:31,560`
För det är



`756 00:33:32,320 --> 00:33:33,860`
De bygger en logg



`757 00:33:34,120 --> 00:33:35,900`
I den här routrarna



`758 00:33:36,160 --> 00:33:39,480`
Och den loggen är läsbar från världen



`759 00:33:39,740 --> 00:33:40,260`
Eller fel



`760 00:33:40,560 --> 00:33:41,320`
Från webbinterfacet



`761 00:33:41,580 --> 00:33:42,860`
Och webbinterfacet är exponerat



`762 00:33:43,120 --> 00:33:45,940`
Så i normala fall ska inte det här vara ett problem för du exponerar väl



`763 00:33:46,200 --> 00:33:47,480`
Inte ditt webbinterface utåt



`764 00:33:47,720 --> 00:33:50,040`
Men om du gör det så är loggarna läsbara



`765 00:33:50,280 --> 00:33:51,060`
icke-autentiserat



`766 00:33:51,320 --> 00:33:52,080`
Från världen



`767 00:33:52,340 --> 00:33:52,840`
Praktiskt



`768 00:33:53,100 --> 00:33:53,880`
Och



`769 00:33:54,120 --> 00:33:55,920`
Det hade ju bara varit halvdåligt



`770 00:33:56,180 --> 00:33:58,220`
Om det inte hade varit för det faktum att



`771 00:33:58,480 --> 00:34:01,300`
Credentials skrivs ner i klartext i loggen och dessutom



`772 00:34:01,800 --> 00:34:02,320`
Så det betyder att



`773 00:34:02,580 --> 00:34:04,880`
Men tänk vilken support man får



`774 00:34:05,140 --> 00:34:05,900`
Så genom att



`775 00:34:06,420 --> 00:34:10,520`
Läsa loggen och hitta credentials så kan du logga in som av whatever användare



`776 00:34:10,820 --> 00:34:12,100`
Som nu har läckt sina credentials



`777 00:34:12,360 --> 00:34:14,660`
Så någon jävel har väl loggat in som root någon gång kan man tänka sig



`778 00:34:15,160 --> 00:34:15,940`
Eller som admin



`779 00:34:16,440 --> 00:34:19,260`
Eller rättare sagt alla som loggar in i sin router gör ju det som admin



`780 00:34:19,520 --> 00:34:20,040`
Visningsvis



`781 00:34:20,540 --> 00:34:24,120`
Så det var en clear and motherfucking cvss 10



`782 00:34:24,900 --> 00:34:26,680`
Sen hade de en cvss 10 till



`783 00:34:26,940 --> 00:34:28,480`
Som var



`784 00:34:29,760 --> 00:34:32,840`
Om du gör en backup



`785 00:34:33,600 --> 00:34:37,700`
Så att om du vill ladda ner en backup på den här och lagra den på ett hemligt viktigt ställe



`786 00:34:37,960 --> 00:34:39,740`
Så



`787 00:34:39,740 --> 00:34:41,540`
Krypteras eller den kan nog krypteras



`788 00:34:41,780 --> 00:34:44,100`
Jag tror inte det alltid måste vara så men den kan krypteras iallafall



`789 00:34:44,340 --> 00:34:45,880`
Backupen så att ingen kan läsa den



`790 00:34:46,400 --> 00:34:47,940`
Och då görs den med en



`791 00:34:48,180 --> 00:34:49,980`
IS-nyckel det vill säga symmetrisk kryptering



`792 00:34:50,240 --> 00:34:51,520`
Unbreakable



`793 00:34:51,780 --> 00:34:53,820`
Precis det är förmodligen military grade på den



`794 00:34:54,340 --> 00:34:55,860`
Quantum safe



`795 00:34:56,120 --> 00:34:56,640`
Förmodligen



`796 00:34:56,900 --> 00:35:01,760`
Och problemet var ju då att det var samma IS-nyckel i alla enheter



`797 00:35:02,260 --> 00:35:02,780`
Praktiskt



`798 00:35:03,040 --> 00:35:06,100`
Vilket ju gör det hela mindre effektivt helt plötsligt



`799 00:35:06,360 --> 00:35:08,660`
Underlätta supporten återigen



`800 00:35:08,920 --> 00:35:09,440`
Tänk i det



`801 00:35:09,740 --> 00:35:14,100`
För det här är ju deras OTA-stöd ish också då kan man säga för att då kan du alltså



`802 00:35:14,600 --> 00:35:17,940`
Du kan ladda ner en sån här config



`803 00:35:18,180 --> 00:35:21,780`
Dekryptera den då och göra de ändringar du vill kryptera det igen och skjuta upp den



`804 00:35:22,020 --> 00:35:24,080`
Nu kräver det här givetvis återigen att du har en



`805 00:35:24,580 --> 00:35:26,380`
Du måste ha en möjlighet att göra det här



`806 00:35:26,640 --> 00:35:28,180`
Men tillsammans de här två



`807 00:35:28,420 --> 00:35:31,760`
Betyder ju det att du kan ändra firmwares överallt i



`808 00:35:32,020 --> 00:35:34,820`
Valfri sådana här router på internet



`809 00:35:35,080 --> 00:35:39,700`
Som publiceras i webbinterface och sen bygga en bakdörr typ och kryptera den och skicka ihop den



`810 00:35:40,000 --> 00:35:41,280`
Den nya backuppen



`811 00:35:42,300 --> 00:35:42,560`
Snyggt



`812 00:35:42,820 --> 00:35:43,580`
Ja, väldigt vackert



`813 00:35:44,100 --> 00:35:45,620`
Och det som är



`814 00:35:45,880 --> 00:35:47,940`
Lite maceball så här det är ju ändå



`815 00:35:48,180 --> 00:35:49,220`
Vi sackar 2026



`816 00:35:49,460 --> 00:35:51,000`
Alltså halvvägs mot 2027



`817 00:35:51,260 --> 00:35:54,080`
Och vi ser fortfarande sådana här tumheter



`818 00:35:54,340 --> 00:35:56,640`
Var det någon som kom ihåg vilket märke det var



`819 00:35:57,140 --> 00:35:58,680`
På mesh-loutrarna, vad är det?



`820 00:35:58,940 --> 00:35:59,960`
Så nu har vi både Acer



`821 00:36:00,220 --> 00:36:02,520`
Och det ägs nog av Cisco tror jag Linksys namn är



`822 00:36:02,780 --> 00:36:03,800`
Linksys är ett Cisco



`823 00:36:04,060 --> 00:36:05,600`
Som gör väldigt suspekta saker



`824 00:36:06,360 --> 00:36:08,920`
Ja det var också inte så himla moderna



`825 00:36:09,180 --> 00:36:09,700`
Det är sant



`826 00:36:10,000 --> 00:36:10,500`
Det är väldigt så här



`827 00:36:10,760 --> 00:36:12,820`
Men man kan ju också förstå det



`828 00:36:13,320 --> 00:36:16,140`
Ska ju tjäna pengar på grejerna också, kan man ju inte hålla på att utveckla, det är ju dyrt



`829 00:36:16,400 --> 00:36:16,900`
Ja



`830 00:36:17,160 --> 00:36:21,520`
Det räcker ju bara att kalla dem en ny siffra, en ny färg på burken



`831 00:36:22,020 --> 00:36:22,540`
Wayvate



`832 00:36:22,800 --> 00:36:23,300`
Wayvate



`833 00:36:23,560 --> 00:36:25,100`
Den kommer ju inte ha de här problemen



`834 00:36:25,360 --> 00:36:27,140`
Den har post-quantum kryptostöd



`835 00:36:27,400 --> 00:36:29,200`
Ja det lär den ju ha garanterat



`836 00:36:29,460 --> 00:36:30,980`
ROT13 minns han



`837 00:36:31,240 --> 00:36:36,620`
Men frågan är om vi ska summera dagens avsnitt här



`838 00:36:37,140 --> 00:36:38,160`
Vi hade en kvar



`839 00:36:38,420 --> 00:36:39,700`
Ska vi ta den Apple



`840 00:36:40,000 --> 00:36:40,500`
Grej också



`841 00:36:40,760 --> 00:36:41,780`
Ja den är



`842 00:36:42,300 --> 00:36:43,060`
Den



`843 00:36:43,320 --> 00:36:44,340`
Jag kan väl nämna den



`844 00:36:44,600 --> 00:36:45,120`
Nu har vi ju sagt det



`845 00:36:45,380 --> 00:36:46,400`
Ja nu har vi sagt det



`846 00:36:46,660 --> 00:36:50,500`
Peppel har ju en Secure Boot när du



`847 00:36:51,000 --> 00:36:55,100`
När du startar upp din telefon



`848 00:36:55,360 --> 00:36:56,900`
Och vad är bra med Secure Boats



`849 00:36:57,140 --> 00:36:59,700`
Vilka egenskaper förväntar vi oss från en Secure Boat



`850 00:36:59,960 --> 00:37:01,240`
Tamper Protection



`851 00:37:01,500 --> 00:37:02,020`
Ja



`852 00:37:02,260 --> 00:37:09,440`
Det brukar ju vara bra om den säkra booten är säker och inte går att ta över kontrollen



`853 00:37:09,740 --> 00:37:10,260`
Ja



`854 00:37:10,500 --> 00:37:18,700`
Det blir ju lite sämre då om du i två olika Apple-generationer då har buggar i din



`855 00:37:19,460 --> 00:37:21,520`
USB-implementation



`856 00:37:21,780 --> 00:37:23,560`
Så du kunde alltså i



`857 00:37:23,820 --> 00:37:26,380`
Tydligen i A12



`858 00:37:26,640 --> 00:37:28,180`
Så var det bara att hamra



`859 00:37:28,680 --> 00:37:35,340`
Några setup-paket med lite konstig information så får du på något sätt skriva access och kan beskrivas under minnet och kan



`860 00:37:36,100 --> 00:37:38,160`
Injusera och ta över telefonen



`861 00:37:38,660 --> 00:37:39,440`
Och



`862 00:37:39,740 --> 00:37:44,340`
I generationen senare A13



`863 00:37:44,600 --> 00:37:49,220`
Så har de ändrat lite i koden så den är en gnutta säkrare men fortfarande osäker



`864 00:37:49,720 --> 00:37:50,740`
Samma



`865 00:37:51,000 --> 00:37:53,300`
Sårbarhet men mer komplicerat exploit



`866 00:37:53,560 --> 00:37:56,120`
Funkar även på A13



`867 00:37:56,380 --> 00:38:01,240`
Och A12 och A13 var väl inte de allra nyaste iPhone-modellerna va



`868 00:38:01,500 --> 00:38:05,080`
Det är gamla modeller så de är snart end of life



`869 00:38:05,340 --> 00:38:07,640`
Har du någon fäll



`870 00:38:07,900 --> 00:38:08,420`
Typ



`871 00:38:08,660 --> 00:38:09,180`
Vad kan det vara



`872 00:38:09,180 --> 00:38:10,460`
iPhone 8, 9



`873 00:38:12,000 --> 00:38:14,040`
Ja då har de inte patchats på ett tag till och med



`874 00:38:14,300 --> 00:38:15,840`
Vad heter de XR



`875 00:38:16,100 --> 00:38:18,400`
XR heter väl någon modell också tror jag



`876 00:38:19,940 --> 00:38:22,740`
Skitsamma men men grejen är att



`877 00:38:25,300 --> 00:38:25,820`
Hot



`878 00:38:26,340 --> 00:38:29,920`
Analysen man behöver göra här det är ju så här är det här ett jätteproblem



`879 00:38:30,180 --> 00:38:32,220`
Nej det är väl



`880 00:38:32,480 --> 00:38:32,980`
Alltså det är väl



`881 00:38:33,240 --> 00:38:34,520`
Så länge du har kontroll över din



`882 00:38:34,780 --> 00:38:38,880`
Fysiska enhet så är det inte ett jätteproblem det är ett problem om du om du är



`883 00:38:39,180 --> 00:38:44,300`
Dissident och tycker illa om Trump och ska åka över TSA gränser



`884 00:38:44,560 --> 00:38:47,620`
Där de har rätt att plocka din telefon



`885 00:38:47,880 --> 00:38:49,420`
Ja men det är väl



`886 00:38:49,680 --> 00:38:53,260`
Och då vill jag säga att den extrema attackvektorn som



`887 00:38:53,520 --> 00:38:56,080`
Disable face identity eller vad heter det



`888 00:38:56,340 --> 00:38:57,100`
Face ID är lättare



`889 00:38:57,360 --> 00:38:58,900`
Det är liksom bara ta telefonen



`890 00:38:59,140 --> 00:39:00,180`
Visa den för ansiktet inne



`891 00:39:01,460 --> 00:39:03,240`
Ja precis



`892 00:39:03,500 --> 00:39:06,320`
Men det här



`893 00:39:06,580 --> 00:39:08,360`
Skulle ju funka även om du har



`894 00:39:08,360 --> 00:39:09,640`
Om man inte har ditt face



`895 00:39:09,900 --> 00:39:12,460`
Avstängt och disable biometri och annat sådant



`896 00:39:12,720 --> 00:39:13,480`
Ja men exakt



`897 00:39:15,520 --> 00:39:19,620`
Men det är ju det primära attackvektorn



`898 00:39:19,880 --> 00:39:21,680`
Skulle ju vara eller det är ju



`899 00:39:21,920 --> 00:39:26,280`
Polis, stat, makt de som har våldsmonopolet



`900 00:39:26,540 --> 00:39:27,820`
Och i



`901 00:39:28,320 --> 00:39:29,600`
Mer långsökta fall



`902 00:39:29,860 --> 00:39:31,660`
Skulle det ju vara avancerat industrispionage



`903 00:39:31,920 --> 00:39:34,720`
När man gör sig besväret och snor någons mobiltelefon men det är liksom



`904 00:39:35,240 --> 00:39:36,260`
Det är ju mer långsökt



`905 00:39:36,520 --> 00:39:37,280`
Jag kan tänka mig att



`906 00:39:37,540 --> 00:39:38,060`
Det här är säkert



`907 00:39:38,360 --> 00:39:40,400`
En sån här sårbarhet som MSA och



`908 00:39:40,660 --> 00:39:41,680`
Vad heter de andra



`909 00:39:41,940 --> 00:39:42,960`
Har suttit på länge



`910 00:39:43,220 --> 00:39:44,760`
De har suttit på den här och nu blir de såhär



`911 00:39:45,020 --> 00:39:46,560`
Ja men den är unpatchable ändå



`912 00:39:46,800 --> 00:39:47,580`
Ja exakt



`913 00:39:48,860 --> 00:39:49,620`
Alltså är den



`914 00:39:49,880 --> 00:39:51,920`
Nerbönt i rumen så kan den ju inte rätta oss



`915 00:39:52,180 --> 00:39:55,520`
Vi pratat ju i tidigare avsnitt



`916 00:39:55,760 --> 00:39:57,040`
För länge sedan om



`917 00:39:57,300 --> 00:39:58,320`
Vad hette de här



`918 00:39:59,360 --> 00:40:04,220`
Imax-processoren eller någonting från någon av de här secure chip-tillverkarna



`919 00:40:04,480 --> 00:40:04,980`
Någonting



`920 00:40:05,240 --> 00:40:07,040`
Vi pratade om det tidigare med



`921 00:40:07,040 --> 00:40:10,620`
Chip där secure-booten är en kass



`922 00:40:11,140 --> 00:40:13,440`
Det är en sån där antingen lever du vidare



`923 00:40:13,700 --> 00:40:17,020`
Vetande som att din säkra boot är osäker eller så är det



`924 00:40:17,800 --> 00:40:22,400`
Vi har en recall på några miljoner enheter och börjat skrappa dem och skicka ut replacements och så



`925 00:40:23,160 --> 00:40:23,680`
Ja



`926 00:40:23,940 --> 00:40:24,960`
Jag bara köper nytt



`927 00:40:27,000 --> 00:40:27,520`
Gott



`928 00:40:27,780 --> 00:40:31,100`
Men med det tänker jag att vi rundar



`929 00:40:31,360 --> 00:40:33,400`
Aftonens



`930 00:40:33,660 --> 00:40:35,200`
Ostrukturerade avsnitt



`931 00:40:35,460 --> 00:40:35,960`
Och



`932 00:40:35,960 --> 00:40:36,740`
Hoppar vi



`933 00:40:36,740 --> 00:40:41,340`
Hoppas att ni har fått med er lite nyheter från cybervärlden



`934 00:40:42,380 --> 00:40:48,520`
Jag som pratade heter Rickard Bortfors och med mig hade jag Mattias Idhage



`935 00:40:48,780 --> 00:40:49,800`
Jesper Larsson



`936 00:40:50,060 --> 00:40:51,580`
Ja men det kan du finna ju



`937 00:40:51,840 --> 00:40:52,860`
Och Peter Magnusson



`938 00:40:53,120 --> 00:40:54,140`
Några konstiga ljud



`939 00:40:54,400 --> 00:40:55,180`
Tackar jag till din boot



`940 00:40:56,460 --> 00:40:56,960`
Ha det gott



`941 00:40:57,220 --> 00:40:57,740`
Tjena


