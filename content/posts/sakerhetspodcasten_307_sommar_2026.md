---
date: '2026-07-20T14:33:00'
tags:
- tema
title: 'Säkerhetspodcasten #307 - Sommar 2026'
---
Podden snackar sommar 2026!
Ett rörigt samtal om
  GPS störsändare, semester, pipeline-scanners, workflows, Hugo-ändringar,
  radioamatörer, DevOps, påven, SSPX, cellgifter, off-the-grid, 10 gigabit...

## Lyssna
* [mp3](https://traffic.libsyn.com/secure/sakerhetspodcasten/2026-07-06_Sommar.mp3?dest-id=117848), längd: 49:12

## Plugs
* [OWASP Gotheburg: BBQ with friends - Post summer kickoff](https://www.meetup.com/owasp-gothenburg-meetup-group/events/315425062/?eventOrigin=group_upcoming_events) \
  Wednesday 26/8 - 17:00
* [BSides Göteborg](https://bsidesgbg.com/) \
  Conference Date: 23th October \
  Call For Paper: 4th July - 10th September

## AI transkribering

_AI försöker förstå oss... Ha överseende med galna feltranskriberingar._

`1 00:00:00,000 --> 00:00:03,040`
Hej och välkommen till Säkerhetspodcasten.



`2 00:00:03,140 --> 00:00:04,920`
Jag som pratar heter Erika Bokfors.



`3 00:00:05,100 --> 00:00:06,940`
Med mig har jag Peter Magnusson.



`4 00:00:07,280 --> 00:00:08,700`
Stavfället i din uppsats.



`5 00:00:09,400 --> 00:00:10,640`
Jesper Larsson.



`6 00:00:11,080 --> 00:00:11,820`
Det kan du finna, ja.



`7 00:00:12,160 --> 00:00:13,480`
Och Mattias Sidhage.



`8 00:00:14,680 --> 00:00:18,900`
Tyvärr har vi inte Johan med oss som brukar påa oss i normala fall.



`9 00:00:19,140 --> 00:00:25,760`
Han tappade rösten så att vi får skänka honom en tankens honungste.



`10 00:00:26,140 --> 00:00:26,880`
Eller en vix.



`11 00:00:27,740 --> 00:00:28,720`
Ja, en vix kanske.



`12 00:00:28,720 --> 00:00:33,120`
I dag när vi spelar in så är det den sjätte juli.



`13 00:00:34,040 --> 00:00:35,060`
Annars 2026.



`14 00:00:35,660 --> 00:00:41,000`
Och vi är sponsrade av Börsjord som man kan läsa mer om på börsjord.se.



`15 00:00:41,800 --> 00:00:45,120`
Bordfors som man kan läsa mer om på bordfors.se.



`16 00:00:45,440 --> 00:00:50,240`
Och 0x4a som man kan läsa mer om på 0x4a.se.



`17 00:00:51,600 --> 00:00:53,380`
Har vi några plugs?



`18 00:00:53,740 --> 00:00:54,660`
Vi har några plugs.



`19 00:00:54,760 --> 00:00:55,360`
Vi har några plugs.



`20 00:00:55,660 --> 00:00:56,060`
Peter.



`21 00:00:57,220 --> 00:00:57,540`
Okej.



`22 00:00:57,540 --> 00:00:58,560`
Vad dumt.



`23 00:00:58,560 --> 00:00:59,800`
Det är du som har...



`24 00:00:59,800 --> 00:01:00,600`
Vi kan...



`25 00:01:00,600 --> 00:01:01,420`
B-Sides Göteborg.



`26 00:01:01,440 --> 00:01:02,160`
B-Sides Göteborg.



`27 00:01:02,300 --> 00:01:02,820`
Vi börjar där.



`28 00:01:03,300 --> 00:01:04,620`
Call for Paper.



`29 00:01:05,480 --> 00:01:06,080`
Vad sa du?



`30 00:01:06,140 --> 00:01:07,420`
Fjärde till tionde september.



`31 00:01:07,480 --> 00:01:08,500`
Är det det sista datumet då?



`32 00:01:09,160 --> 00:01:10,300`
Det är väl...



`33 00:01:10,300 --> 00:01:11,400`
Det skulle det kunna vara.



`34 00:01:11,660 --> 00:01:12,100`
Det låter rimligt.



`35 00:01:12,100 --> 00:01:15,680`
Nu kan jag kolla källan.



`36 00:01:15,960 --> 00:01:17,300`
Och nu går vi vidare till de andra plugsen.



`37 00:01:17,300 --> 00:01:18,760`
Konferensen är i alla fall 23 oktober.



`38 00:01:18,980 --> 00:01:19,120`
Ja.



`39 00:01:19,280 --> 00:01:22,720`
Och sen har vi då en liten ovasp-grej efter sommaren.



`40 00:01:23,060 --> 00:01:27,540`
Eftersom alla nu kanske då är på väg ut i någon form av semester-dvala.



`41 00:01:27,640 --> 00:01:28,280`
Så.



`42 00:01:28,560 --> 00:01:31,540`
Och vill man ju ha ett event att se fram emot i augusti.



`43 00:01:31,620 --> 00:01:32,520`
Så den 26...



`44 00:01:32,520 --> 00:01:33,580`
26?



`45 00:01:34,000 --> 00:01:35,040`
Jag kan inte prata längre.



`46 00:01:35,040 --> 00:01:35,500`
Det är 26.



`47 00:01:35,840 --> 00:01:37,320`
Jag fick en liten stroke där.



`48 00:01:37,900 --> 00:01:39,260`
Jag vill ha en semester jag med.



`49 00:01:39,380 --> 00:01:39,860`
Men det får jag inte.



`50 00:01:40,220 --> 00:01:44,520`
Men Ovas Göteborg har en barbecue på Scenics Group 26 augusti.



`51 00:01:45,000 --> 00:01:46,140`
Och det är alltså...



`52 00:01:46,140 --> 00:01:46,520`
Vad blir det?



`53 00:01:46,600 --> 00:01:47,860`
Är det den här juni-3-skrapan?



`54 00:01:47,920 --> 00:01:49,140`
Lindholmar räknas det kanske som?



`55 00:01:49,520 --> 00:01:51,380`
Det är väl typiskt Lindholmar.



`56 00:01:51,520 --> 00:01:53,540`
Ja, och där har man en fin liten terrass har de.



`57 00:01:53,760 --> 00:01:54,940`
I sitt nya fina kontor.



`58 00:01:55,340 --> 00:01:57,180`
Kan man få en liten grej?



`59 00:01:58,040 --> 00:01:58,540`
Ramla in.



`60 00:01:58,560 --> 00:02:01,000`
På Meetup och klicka till klicka.



`61 00:02:01,580 --> 00:02:02,740`
Och det...



`62 00:02:02,740 --> 00:02:03,920`
Just det. Meetup heter det.



`63 00:02:04,540 --> 00:02:08,740`
Nu har jag hittat BISÖDs Göteborgs officiella uppmarskningar.



`64 00:02:09,940 --> 00:02:13,480`
Det är alltså fjärde juli till tionde september.



`65 00:02:13,800 --> 00:02:17,240`
Så de har sin Call for Paper, eller Paper Submission.



`66 00:02:18,120 --> 00:02:20,000`
Och konferensen 23 oktober.



`67 00:02:20,380 --> 00:02:25,400`
Och det betyder alltså att CFPN vill ha förslag till talare för själva konferensen.



`68 00:02:25,460 --> 00:02:27,160`
Om man nu har undgått att förstå detta.



`69 00:02:27,820 --> 00:02:28,180`
Och\!



`70 00:02:28,560 --> 00:02:30,880`
Som ni alla har förstått så är det här ett strukturerat avsnitt.



`71 00:02:31,260 --> 00:02:31,740`
Jajamensan.



`72 00:02:31,760 --> 00:02:32,520`
Ja, men...



`73 00:02:32,520 --> 00:02:33,200`
Ett temaavsnitt.



`74 00:02:33,200 --> 00:02:34,080`
Det är väl nästan alltid.



`75 00:02:34,400 --> 00:02:35,920`
Som jag inte har förberett.



`76 00:02:36,140 --> 00:02:41,840`
Ni har så många möjligheter att komma till bästkusten och se den bästa av städer.



`77 00:02:42,340 --> 00:02:42,560`
Ja.



`78 00:02:43,040 --> 00:02:44,420`
För BISODS tänker du?



`79 00:02:45,000 --> 00:02:47,940`
Ja, för picknicken också.



`80 00:02:48,420 --> 00:02:50,360`
Ja, just det. Eller grillgrill.



`81 00:02:50,360 --> 00:02:52,640`
Det är faktiskt en väldigt fin...



`82 00:02:52,640 --> 00:02:56,640`
Det är som en liten skrapa som man ser utöver hela Göteborgs hamninlopp.



`83 00:02:57,680 --> 00:02:58,540`
Älvutsikt som vi kallar det.



`84 00:02:58,560 --> 00:03:00,200`
På vilken sida är det redan?



`85 00:03:00,200 --> 00:03:02,960`
Med andra ord, stockholmarna hade sagt sjöutsikt.



`86 00:03:03,340 --> 00:03:04,240`
För att de har inget hav.



`87 00:03:05,600 --> 00:03:06,180`
Det är bräckt.



`88 00:03:06,880 --> 00:03:07,520`
Åh\!



`89 00:03:08,660 --> 00:03:10,960`
Om bräckt vatten räknas inte.



`90 00:03:11,140 --> 00:03:11,700`
Nej, det gör inte det.



`91 00:03:11,900 --> 00:03:12,680`
Det är ingen riktig tav.



`92 00:03:12,700 --> 00:03:13,180`
Nej, det är så.



`93 00:03:13,340 --> 00:03:15,260`
Det är havsutsikt för en stockholmar.



`94 00:03:15,900 --> 00:03:17,420`
Det ligger på Lindholmssidan.



`95 00:03:17,640 --> 00:03:20,680`
Det ligger på den onda, skjutna Hisingsön.



`96 00:03:22,320 --> 00:03:24,720`
Okej, så tema sommar.



`97 00:03:24,920 --> 00:03:28,000`
Tema sommar var faktiskt Peter räddade mig.



`98 00:03:28,000 --> 00:03:34,120`
Jag hade tänkt att prata lite om AI-automation och CSDI-byggplattformar.



`99 00:03:34,280 --> 00:03:36,040`
Men det blev inget med det.



`100 00:03:36,240 --> 00:03:39,640`
Så den som lyssnar senare kanske får ett sådant avsnitt.



`101 00:03:39,880 --> 00:03:40,760`
Men det blir inte idag.



`102 00:03:41,500 --> 00:03:44,160`
Så idag tänker jag att vi kör ett traditionsenligt sommaravsnitt.



`103 00:03:45,180 --> 00:03:46,780`
Och för dem som inte har varit med förr.



`104 00:03:46,860 --> 00:03:51,700`
Ett traditionsenligt sommaravsnitt handlar egentligen om att vi sitter och pratar om vad vi har tänkt göra nu när det är sommar och semester.



`105 00:03:52,960 --> 00:03:57,540`
Och kanske framförallt fokus på eventuella säkerhetsaspekter av det vi tänker göra.



`106 00:03:57,540 --> 00:03:57,960`
Exakt.



`107 00:03:58,000 --> 00:04:00,940`
Badning kanske inte är så viktigt.



`108 00:04:01,160 --> 00:04:01,920`
Det är mer safety.



`109 00:04:02,680 --> 00:04:04,240`
Ja, det är sant. Det är safety, ja.



`110 00:04:04,860 --> 00:04:09,780`
Om vi har något coolt teknikprojekt som kan härledas till vatten. Varför inte?



`111 00:04:10,820 --> 00:04:11,300`
Nej, det har jag inte.



`112 00:04:12,100 --> 00:04:12,800`
Vem vill börja då?



`113 00:04:13,500 --> 00:04:18,220`
Jag kan ju prata om vad jag har gjort som är relevant för en podcast.



`114 00:04:18,700 --> 00:04:22,500`
Jag har ju kört igenom, nu försöker jag komma ihåg vad verktygen är där.



`115 00:04:22,500 --> 00:04:25,580`
Det är ju den här Sysmore-pipeline-scannen.



`116 00:04:26,140 --> 00:04:27,760`
Och sen den andra pipeline-scannen.



`117 00:04:28,000 --> 00:04:28,800`
Tillsammans hette den.



`118 00:04:29,800 --> 00:04:31,000`
Det kommer snart.



`119 00:04:31,720 --> 00:04:33,900`
Vad är en pipeline-scanner, Peter?



`120 00:04:34,300 --> 00:04:39,500`
Den försöker avgöra om du har en riktigt kass-pipeline som är ett stort säkerhetshål.



`121 00:04:40,180 --> 00:04:41,880`
Hur gör den det?



`122 00:04:43,360 --> 00:04:44,700`
Genom lite olika grejer.



`123 00:04:46,640 --> 00:04:52,540`
Dels kollar de ju på om du faktiskt har deklarativt skrivit ut vilka rättigheter du använder.



`124 00:04:53,480 --> 00:04:55,140`
Är det någon specifik?



`125 00:04:55,300 --> 00:04:57,740`
Alltså det är inte random pipeline de tittar på?



`126 00:04:57,740 --> 00:05:00,340`
Utan den har stöd för git-grejer då, eller?



`127 00:05:01,420 --> 00:05:05,140`
Ja, alltså nu vet jag absolut inte vad gränserna för vad de stödjer är.



`128 00:05:05,220 --> 00:05:14,740`
Men de har ju stöd för githubs, de här github-actions, deras jammel styrk workflow.



`129 00:05:15,620 --> 00:05:17,140`
Eller vad typ som de kallar det.



`130 00:05:17,160 --> 00:05:20,560`
Workflow, actions, gitlab, github.



`131 00:05:20,660 --> 00:05:24,560`
Har även stöd för olika specifika CICD.



`132 00:05:24,560 --> 00:05:26,560`
Alltså typ ha lite templating för...



`133 00:05:27,740 --> 00:05:28,780`
Konfig-analys.



`134 00:05:28,880 --> 00:05:31,520`
Snarare än att den kör i runtime och kolla vad den kommer åt.



`135 00:05:32,880 --> 00:05:38,380`
Ja, den tittar ju på workflow-konfigurationen.



`136 00:05:38,520 --> 00:05:40,340`
Alltså det vill säga den tittar på vad som kommer köras.



`137 00:05:40,940 --> 00:05:43,060`
Det är typ som en liten linter skulle man kunna säga.



`138 00:05:43,900 --> 00:05:45,960`
Statisk kodanalys av din jammel.



`139 00:05:46,880 --> 00:05:47,160`
Typ.



`140 00:05:47,580 --> 00:05:49,760`
Och sen så ger den då lite...



`141 00:05:49,760 --> 00:05:52,200`
Den kollar ju även på rättighetsmodeller.



`142 00:05:52,420 --> 00:05:53,820`
Vad som exekverar vad.



`143 00:05:53,820 --> 00:05:54,920`
Och hur.



`144 00:05:55,200 --> 00:05:57,720`
Vilka rättigheter som är applicerade i olika delar.



`145 00:05:57,740 --> 00:06:00,920`
Det är en ganska kompetent produkt.



`146 00:06:01,040 --> 00:06:03,460`
Vi har ju så pass enkla grejer.



`147 00:06:03,700 --> 00:06:06,160`
Så det är ju absolut inte så att vi har testat gränserna för dem.



`148 00:06:06,220 --> 00:06:09,740`
Men det ena verktyget då varnar ju bland annat för att...



`149 00:06:10,660 --> 00:06:13,920`
För att vi kör ett relativt ovanligt...



`150 00:06:13,920 --> 00:06:15,500`
Annan linter då liksom.



`151 00:06:16,320 --> 00:06:20,140`
Just att vi har en ovanlig grej i ett av våra testworkflows då.



`152 00:06:22,260 --> 00:06:26,220`
Och så fick vi klagomål på att vi inte explicit skriver ut.



`153 00:06:26,620 --> 00:06:27,540`
Så att de...



`154 00:06:27,540 --> 00:06:30,920`
De ville att man helst gör en tydlig dropp av alla rättigheter.



`155 00:06:31,040 --> 00:06:34,120`
Och så lägger man till specifikt de rättigheter man behöver i ett arbetsflöde.



`156 00:06:34,240 --> 00:06:39,020`
Så att man inte implicit tar med sig mer rättigheter än vad man borde ha.



`157 00:06:40,080 --> 00:06:40,620`
Och lite så.



`158 00:06:40,680 --> 00:06:42,460`
Vi fick inte jättemycket anmärkningar.



`159 00:06:43,000 --> 00:06:44,540`
Sen har ju jag...



`160 00:06:44,540 --> 00:06:47,060`
Det var ju någon attack vi pratade om för jättelänge sedan.



`161 00:06:48,060 --> 00:06:48,460`
Då...



`162 00:06:48,460 --> 00:06:51,820`
Då det utnyttjades i attacken att...



`163 00:06:53,080 --> 00:06:57,000`
Du kan ju lita på att workflowet är exakt vad du vill ha.



`164 00:06:57,540 --> 00:07:00,500`
Men du kan ju egentligen inte lita på speciellt mycket annat.



`165 00:07:00,680 --> 00:07:03,420`
Åtminstone var det så i tidigare versioner av...



`166 00:07:03,420 --> 00:07:05,460`
Av hur de här grunkorna funkade.



`167 00:07:05,580 --> 00:07:06,380`
Så...



`168 00:07:06,380 --> 00:07:09,780`
En sak vi hade var ju att vi hade...



`169 00:07:09,780 --> 00:07:12,220`
I och med att vi installerar Hugo i ett av våra workflows.



`170 00:07:12,880 --> 00:07:16,780`
Så har jag haft tja summat och kollat att om någon...



`171 00:07:16,780 --> 00:07:22,860`
Om någon byter ut den här artefakten eftersom vi laddar den från någonting vi inte har offlinat in i våra egna...



`172 00:07:22,860 --> 00:07:25,080`
Som vi inte kan formellt verifiera liksom.



`173 00:07:25,480 --> 00:07:26,180`
Då blir det en flagga.



`174 00:07:26,180 --> 00:07:27,500`
Så jag har haft en tja 256.



`175 00:07:27,540 --> 00:07:34,780`
Och den har jag alltså flyttat från att vi har haft en separat tja...



`176 00:07:34,780 --> 00:07:37,580`
Tja-sum-fil till att...



`177 00:07:37,580 --> 00:07:39,220`
Protein var det du...



`178 00:07:39,220 --> 00:07:39,440`
Ja\!



`179 00:07:40,340 --> 00:07:40,860`
Bra\!



`180 00:07:41,280 --> 00:07:41,820`
Det är bra.



`181 00:07:41,940 --> 00:07:42,640`
Vi satt långt in i det.



`182 00:07:42,940 --> 00:07:46,320`
Nej men så den har jag ju beskrivit om så att vi har en echo.



`183 00:07:46,580 --> 00:07:51,640`
Så att vårt workflow har inga beroenden egentligen utöver det som det borde ha nu.



`184 00:07:52,840 --> 00:07:56,540`
Sen så ska inte vårt workflow gå och köras via någon...



`185 00:07:57,540 --> 00:07:59,620`
Via någon push eller liknande.



`186 00:07:59,760 --> 00:08:03,000`
Så vi är ju lite mer skyddade.



`187 00:08:03,280 --> 00:08:03,880`
Eller liksom...



`188 00:08:03,880 --> 00:08:07,100`
Vi är ju inte ute i de mest riskiga waters liksom.



`189 00:08:07,780 --> 00:08:11,360`
Men nu är det lite mer säkrare.



`190 00:08:11,580 --> 00:08:12,440`
Och vi har faktiskt...



`191 00:08:12,440 --> 00:08:16,000`
För mig så känns det bra att vi har testat något av de här rektigen vi har pratat om.



`192 00:08:16,340 --> 00:08:16,480`
Mm.



`193 00:08:16,940 --> 00:08:18,240`
Och det är ganska...



`194 00:08:18,240 --> 00:08:18,780`
Dogfooding.



`195 00:08:18,780 --> 00:08:19,820`
De är ganska bra.



`196 00:08:20,060 --> 00:08:21,520`
Om inte annat så det blir ju...



`197 00:08:21,520 --> 00:08:23,780`
Det blir ju alltså en klassisk...



`198 00:08:24,420 --> 00:08:24,820`
Så här...



`199 00:08:24,820 --> 00:08:26,540`
CLI-linter-output.



`200 00:08:26,640 --> 00:08:27,380`
Så det blir ju ganska...



`201 00:08:27,380 --> 00:08:28,760`
Stökigt sådär.



`202 00:08:29,900 --> 00:08:31,120`
När det kommer ut i konsolen.



`203 00:08:31,200 --> 00:08:33,360`
Men det som är trevligt är att...



`204 00:08:33,360 --> 00:08:34,460`
Den lämnar förslag.



`205 00:08:34,520 --> 00:08:35,960`
Och den lämnar ändå så här...



`206 00:08:35,960 --> 00:08:38,520`
Men det är den här grejen jag har...



`207 00:08:38,520 --> 00:08:39,600`
Har agerat på.



`208 00:08:39,720 --> 00:08:41,220`
Alltså regex-baserat typ semgrej.



`209 00:08:41,280 --> 00:08:41,820`
Alltså det är ju så här...



`210 00:08:41,820 --> 00:08:42,940`
Det är ju patterns liksom.



`211 00:08:43,620 --> 00:08:44,680`
Och det är ganska bra.



`212 00:08:44,820 --> 00:08:47,600`
Även om mycket är kanske så här...



`213 00:08:47,600 --> 00:08:48,800`
If-then-else-år-grejer.



`214 00:08:48,880 --> 00:08:49,700`
Så är den ganska bra.



`215 00:08:49,700 --> 00:08:52,260`
För man får väldigt snabbt en idé om hur...



`216 00:08:52,260 --> 00:08:56,500`
Anomali eller hur konfigurations-patterns som är dåliga...



`217 00:08:56,500 --> 00:08:57,360`
Ser ut.



`218 00:08:57,380 --> 00:08:57,540`
Ser ut.



`219 00:08:58,340 --> 00:08:59,000`
Och det är ganska bra.



`220 00:08:59,160 --> 00:09:00,780`
Så att även om det blir en massa falsk-positiv...



`221 00:09:00,780 --> 00:09:02,700`
Så du kör det första gången och känner att det här är CAS.



`222 00:09:03,320 --> 00:09:04,860`
Så är det ganska bra att gå igenom det där.



`223 00:09:04,940 --> 00:09:06,140`
För att det är...



`224 00:09:06,140 --> 00:09:09,880`
Det är kanske inte applicerbart som en kritisk issue.



`225 00:09:10,300 --> 00:09:12,020`
Men du förstår hur den tänker.



`226 00:09:12,160 --> 00:09:14,520`
En annan ändring jag gjorde som...



`227 00:09:14,520 --> 00:09:15,400`
Egentligen inte...



`228 00:09:15,400 --> 00:09:16,900`
Det är nog ingen säkerhetsbest practice.



`229 00:09:17,000 --> 00:09:19,200`
Men jag tänkte rent logiskt att...



`230 00:09:19,200 --> 00:09:21,660`
Vi behöver ju aldrig någonsin checka ut vad en projekt...



`231 00:09:21,660 --> 00:09:22,500`
Om...



`232 00:09:22,500 --> 00:09:25,340`
Om andra saker kommer misslyckas.



`233 00:09:26,140 --> 00:09:27,340`
Så att när vi...



`234 00:09:27,340 --> 00:09:28,400`
Checka ut...



`235 00:09:28,400 --> 00:09:30,920`
Vi jobbar ju på vårt eget projekt från vårat workflow.



`236 00:09:31,400 --> 00:09:34,360`
Det kan man nog diskutera om det är en best practice.



`237 00:09:34,880 --> 00:09:35,080`
Ja.



`238 00:09:35,320 --> 00:09:35,880`
Men...



`239 00:09:35,880 --> 00:09:37,240`
Alltså...



`240 00:09:37,240 --> 00:09:39,140`
På min sida av den här pipelinen...



`241 00:09:39,140 --> 00:09:41,120`
Jag bygger allt som är tillgängligt.



`242 00:09:41,220 --> 00:09:42,480`
Jag tar allt som du ger mig.



`243 00:09:43,100 --> 00:09:44,120`
Ja, men jag gör...



`244 00:09:44,120 --> 00:09:44,700`
Ja, precis.



`245 00:09:44,860 --> 00:09:47,480`
Men på GitHub-sidan så gör vi check-out först.



`246 00:09:48,380 --> 00:09:49,000`
Först om...



`247 00:09:49,000 --> 00:09:51,520`
Funkade Hugo-installationen?



`248 00:09:51,740 --> 00:09:53,240`
Har allting i början gått bra?



`249 00:09:53,760 --> 00:09:55,800`
Har syssmor-checken gått bra?



`250 00:09:55,960 --> 00:09:56,320`
Och sådär liksom.



`251 00:09:56,420 --> 00:09:57,280`
Först liksom...



`252 00:09:57,280 --> 00:09:59,280`
Nu har vi avslöjat kritiska grejer här.



`253 00:09:59,280 --> 00:10:03,460`
Först om vi lyckas skjuta in nånting som renderar oss på jätten



`254 00:10:03,460 --> 00:10:04,960`
så kommer det byggas automatiskt.



`255 00:10:05,080 --> 00:10:05,620`
Bara så ni vet det.



`256 00:10:06,220 --> 00:10:08,000`
Det kommer bara hamna.



`257 00:10:09,160 --> 00:10:09,280`
Mm.



`258 00:10:09,820 --> 00:10:10,500`
Men det är... Ja.



`259 00:10:11,940 --> 00:10:13,880`
Nej, men som en liten grej faktiskt.



`260 00:10:16,260 --> 00:10:16,700`
Fy...



`261 00:10:16,700 --> 00:10:19,320`
Alltså vår hemsida har aldrig varit så uppdaterad som den är nu.



`262 00:10:19,340 --> 00:10:20,040`
Och så säker.



`263 00:10:21,140 --> 00:10:22,780`
Ah, fuck. Det där är ju ett svårt...



`264 00:10:22,780 --> 00:10:24,380`
Det där ska man inte säga i podcasten.



`265 00:10:24,480 --> 00:10:25,180`
Det är såhär...



`266 00:10:25,180 --> 00:10:26,860`
Vi är unhackable.



`267 00:10:27,280 --> 00:10:27,880`
Jag var...



`268 00:10:27,880 --> 00:10:29,660`
Jag var nära på att säga det.



`269 00:10:29,820 --> 00:10:30,500`
Och sen så bara såhär...



`270 00:10:30,500 --> 00:10:31,200`
Nej, det gör vi inte.



`271 00:10:31,200 --> 00:10:31,800`
Alltså...



`272 00:10:31,800 --> 00:10:32,740`
Men nu är det ute.



`273 00:10:32,740 --> 00:10:36,060`
Den största risken är ju att någon skulle äga något av våra konton.



`274 00:10:36,440 --> 00:10:39,140`
Och det har vi så bra säkerhet av inte att vi klarar det.



`275 00:10:39,160 --> 00:10:41,100`
Vi börjar dedosa alla andra sajter på samma yta.



`276 00:10:41,320 --> 00:10:41,960`
Det hade varit tråkigt.



`277 00:10:43,880 --> 00:10:48,540`
Men det är väl säkrare när vi hade en icke-mentor innan WordPress i vart fall.



`278 00:10:48,640 --> 00:10:50,400`
Ja, men det är Johans fel alltihop.



`279 00:10:51,140 --> 00:10:52,000`
Jag vågar hävda det.



`280 00:10:52,240 --> 00:10:53,580`
Ja, men du startade igång där, Peter.



`281 00:10:53,700 --> 00:10:54,000`
Fortsätt.



`282 00:10:54,000 --> 00:10:56,700`
Vad finns mer i sommarens sköte?



`283 00:10:56,700 --> 00:10:58,620`
Nu tror du att det finns så mycket mer.



`284 00:10:58,880 --> 00:11:04,700`
Jag har inte planerat så mycket mer än att jag har tänkt se lite grannländer.



`285 00:11:05,620 --> 00:11:11,320`
Och så har jag tänkt att försöka ha behörigt avstånd när Ukraina bombar Ryssland.



`286 00:11:12,260 --> 00:11:13,740`
Alltså inte åt det hållet då?



`287 00:11:14,300 --> 00:11:19,940`
Jag tänkte eventuellt vara borta vid Helsinki och sätta båten över till Tallinn.



`288 00:11:20,380 --> 00:11:21,680`
Och då är vi ju...



`289 00:11:21,680 --> 00:11:22,520`
Ändå ganska nära.



`290 00:11:22,520 --> 00:11:23,740`
Då är vi ju...



`291 00:11:23,740 --> 00:11:25,240`
Det är ju för fan bara...



`292 00:11:25,240 --> 00:11:25,900`
Vi får ju...



`293 00:11:25,900 --> 00:11:26,540`
Jag tänker mig...



`294 00:11:26,540 --> 00:11:33,340`
Vi får sätta oss högst upp på båten och titta med kikarna och se om det kommer några feta bränder liksom.



`295 00:11:33,460 --> 00:11:37,740`
Men du ska inte hälsa på våra grannländer som är världsmästare i fotboll då?



`296 00:11:38,060 --> 00:11:40,600`
Noterar du att jag säger det här den sjätte juli då?



`297 00:11:40,660 --> 00:11:41,600`
Får vi se om jag har rätt.



`298 00:11:43,300 --> 00:11:43,540`
Ja.



`299 00:11:44,120 --> 00:11:45,440`
Nej, Norge känns läskigt också.



`300 00:11:46,800 --> 00:11:48,920`
I Ostrukt kommer vi ha en fotbollsnyhet.



`301 00:11:48,920 --> 00:11:53,640`
Vi är ju verkligen en fotbollsintegrerad säkerhetspodcast just nu.



`302 00:11:53,780 --> 00:11:54,260`
Ja, rätt i tiden.



`303 00:11:54,800 --> 00:11:56,080`
Ja, det låter ändå...



`304 00:11:56,080 --> 00:11:56,500`
Men ja.



`305 00:11:56,540 --> 00:11:56,760`
Okej.



`306 00:11:57,380 --> 00:11:59,520`
Du ska bara över och titta lite på ryssarna egentligen.



`307 00:12:00,020 --> 00:12:02,000`
Ja, på behörigt avstånd.



`308 00:12:03,160 --> 00:12:04,480`
Flyger väldigt lågt i dag.



`309 00:12:04,740 --> 00:12:10,940`
Det är också så här att om ryssarna gör tillräckligt mycket GPS-störningar kommer båten då åka fel liksom.



`310 00:12:11,160 --> 00:12:14,700`
Vad är sannolikheten att båten liksom hamnar i Danmark eller något?



`311 00:12:14,700 --> 00:12:16,900`
De har ju ganska bra...



`312 00:12:16,900 --> 00:12:18,620`
Alltså vi får hoppas att det är någon skolad kapten.



`313 00:12:18,780 --> 00:12:21,280`
Då kan man ju ändå plottra kursen med kompass.



`314 00:12:21,500 --> 00:12:24,180`
De kan ju använda andra verktyg för att navigera.



`315 00:12:24,220 --> 00:12:26,020`
De får kappa någon så de kan ha en tröd.



`316 00:12:26,540 --> 00:12:30,640`
Men det är ju faktiskt nere i Östersjön, alltså nere i hörnet där.



`317 00:12:30,640 --> 00:12:36,640`
Där är det ju en konstant, jätteröd sån GPS-störnings...



`318 00:12:37,360 --> 00:12:38,860`
Det är väl där nere igenom?



`319 00:12:38,960 --> 00:12:44,420`
Ja, det finns ju hög sannolikhet för att mobiltelefon, GPS och sådana kommer...



`320 00:12:44,420 --> 00:12:45,060`
Spännande.



`321 00:12:45,960 --> 00:12:47,480`
Kanske telefonen blir på ryska.



`322 00:12:48,440 --> 00:12:49,940`
Men vad händer med tidscyk då?



`323 00:12:50,420 --> 00:12:51,480`
Ja, den blir ju...



`324 00:12:51,480 --> 00:12:54,560`
Om man använder en rysk satellit kanske det blir bättre.



`325 00:12:55,220 --> 00:12:55,660`
Men...



`326 00:12:56,540 --> 00:13:04,160`
Mobildelen av telefonen brukar väl använda typ MTP eller liknande?



`327 00:13:04,280 --> 00:13:05,940`
Den brukar väl inte använda GPS för tiden?



`328 00:13:05,940 --> 00:13:09,360`
Men synkas inte det via metadatat i SS7 då?



`329 00:13:09,840 --> 00:13:11,240`
Alltså, läker sig det?



`330 00:13:11,400 --> 00:13:11,800`
Maybe.



`331 00:13:12,360 --> 00:13:13,920`
Jag kan inte tillräckligt...



`332 00:13:13,920 --> 00:13:14,320`
För det känns väl inte...



`333 00:13:14,320 --> 00:13:18,260`
Det är som du säger, så länge man har IP i alla fall så borde man ju kunna köra det via MTP.



`334 00:13:18,380 --> 00:13:19,560`
Ja, det är sant.



`335 00:13:19,720 --> 00:13:20,500`
Om man har IP, ja.



`336 00:13:22,280 --> 00:13:24,020`
Ja, det är spännande.



`337 00:13:24,660 --> 00:13:25,460`
Jag ska inte dit.



`338 00:13:26,540 --> 00:13:28,880`
Du får rapportera tillbaka sen.



`339 00:13:29,200 --> 00:13:30,360`
Vart ska du i sommar då, Jesper?



`340 00:13:31,140 --> 00:13:32,340`
Jag vet inte än.



`341 00:13:32,540 --> 00:13:34,440`
Jag tror inte jag ska någonstans faktiskt.



`342 00:13:34,700 --> 00:13:37,040`
Jag tror att jag ska vara på vårat landställe.



`343 00:13:37,900 --> 00:13:39,040`
Det är vad jag tror.



`344 00:13:39,680 --> 00:13:41,480`
Men blir det dåligt väder så ska jag någonstans.



`345 00:13:42,420 --> 00:13:43,380`
Det är tanken.



`346 00:13:44,120 --> 00:13:44,880`
Så är det faktiskt.



`347 00:13:45,080 --> 00:13:46,540`
Sen så är det alltid lite pill hemma.



`348 00:13:46,940 --> 00:13:49,140`
Jag håller faktiskt på att bygga en applikation.



`349 00:13:50,080 --> 00:13:51,920`
Som ska släppas open source.



`350 00:13:52,580 --> 00:13:54,480`
För just det vi pratar om här på Jätten.



`351 00:13:54,480 --> 00:13:56,480`
Med problematik.



`352 00:13:56,540 --> 00:13:57,600`
Med de problematiska GitOps.



`353 00:13:58,140 --> 00:13:59,940`
Eller bara modern DevOps egentligen.



`354 00:14:00,900 --> 00:14:02,040`
Problematiken med



`355 00:14:02,040 --> 00:14:04,160`
federerade identiteter och



`356 00:14:04,160 --> 00:14:06,540`
ologiska konfigurationsalternativ.



`357 00:14:07,880 --> 00:14:08,820`
Så det håller på att göra



`358 00:14:08,820 --> 00:14:12,440`
en work flow faktiskt.



`359 00:14:12,560 --> 00:14:14,960`
Som man implementerar i sin Git-organisation.



`360 00:14:15,680 --> 00:14:16,540`
Som sedan körs.



`361 00:14:17,640 --> 00:14:18,920`
Man kan ha massa olika triggers



`362 00:14:18,920 --> 00:14:20,020`
när den här grejen ska köras.



`363 00:14:20,840 --> 00:14:22,600`
Men det det framförallt är



`364 00:14:22,600 --> 00:14:24,540`
är att den blir cloud-agnostisk.



`365 00:14:24,540 --> 00:14:25,820`
Det är agnostisk, säger man det.



`366 00:14:26,540 --> 00:14:29,420`
Det spelar ingen roll vilken målleverantör.



`367 00:14:29,740 --> 00:14:31,340`
Alltså idén bygger ju på att



`368 00:14:31,340 --> 00:14:33,760`
du bygger



`369 00:14:33,760 --> 00:14:35,980`
du hanterar kod



`370 00:14:35,980 --> 00:14:37,200`
och du bygger kod



`371 00:14:37,200 --> 00:14:38,640`
från ett Git-kontext.



`372 00:14:38,740 --> 00:14:40,100`
Alltså ett repo-kontext egentligen.



`373 00:14:40,320 --> 00:14:42,360`
Och det är sedan kopplat till



`374 00:14:42,360 --> 00:14:45,660`
en målleverantör, en byggpipeline.



`375 00:14:46,260 --> 00:14:47,420`
Så att man har ganska många



`376 00:14:47,420 --> 00:14:49,040`
gator. Nu kommer de att hämta en IP.



`377 00:14:49,060 --> 00:14:50,320`
Hej och välkommen till Göteborg.



`378 00:14:51,120 --> 00:14:53,580`
Du ser, vi har aldrig följt upp



`379 00:14:53,580 --> 00:14:55,340`
men så får vi lite lokalfärg.



`380 00:14:55,560 --> 00:14:56,220`
Ja, det är sant.



`381 00:14:56,540 --> 00:14:58,280`
Snart kommer det börja skjutas.



`382 00:14:58,400 --> 00:14:59,520`
Det är lugnt, vi sitter inomhus.



`383 00:15:00,020 --> 00:15:01,700`
Vi har inget skottsäkerhetsglas.



`384 00:15:02,200 --> 00:15:03,960`
Som ni vet så kan man inte bli skjuten



`385 00:15:03,960 --> 00:15:04,860`
om man sitter inomhus.



`386 00:15:05,300 --> 00:15:06,160`
Det är din gamla sanning.



`387 00:15:07,680 --> 00:15:08,860`
Det kan vi säga till ryssarna.



`388 00:15:08,940 --> 00:15:11,540`
Men vad ska ditt tool göra som är coolare



`389 00:15:11,540 --> 00:15:13,640`
än de som Peter pratade om?



`390 00:15:13,660 --> 00:15:15,740`
Inte så mycket coolare egentligen.



`391 00:15:15,840 --> 00:15:17,400`
Det gör ungefär samma sak.



`392 00:15:17,600 --> 00:15:19,020`
Men det det gör då är att



`393 00:15:19,020 --> 00:15:21,340`
för vad de här andra



`394 00:15:21,340 --> 00:15:22,580`
open source-alternativen gör



`395 00:15:22,580 --> 00:15:24,400`
det är att de använder sig av



`396 00:15:24,400 --> 00:15:26,420`
en generisk



`397 00:15:26,540 --> 00:15:27,820`
template, vad den letar efter.



`398 00:15:27,820 --> 00:15:29,900`
De patterns man letar efter



`399 00:15:29,900 --> 00:15:31,220`
som är felkonfigurationer



`400 00:15:31,220 --> 00:15:33,500`
de tar inte hänsyn till din sås.



`401 00:15:34,600 --> 00:15:35,840`
Så idén här då är att



`402 00:15:35,840 --> 00:15:37,820`
jag har byggt ett template-bibliotek



`403 00:15:37,820 --> 00:15:38,880`
som bygger på



`404 00:15:38,880 --> 00:15:42,260`
en mall för hur man definierar patterns.



`405 00:15:42,720 --> 00:15:43,860`
Så du kan liksom själv



`406 00:15:43,860 --> 00:15:45,160`
gå in och lägga till så här



`407 00:15:45,160 --> 00:15:47,240`
jag är intresserad av när



`408 00:15:47,240 --> 00:15:49,520`
min byggidentitet som heter



`409 00:15:49,520 --> 00:15:51,400`
Caliculas Service Account



`410 00:15:51,400 --> 00:15:53,760`
plockar rättigheter utanför



`411 00:15:53,760 --> 00:15:54,460`
det här skåpet.



`412 00:15:54,460 --> 00:15:56,460`
Eller när denna



`413 00:15:56,540 --> 00:15:58,880`
projektet ber om att få någonting



`414 00:15:58,880 --> 00:16:00,600`
som är över



`415 00:16:00,600 --> 00:16:03,120`
sitt eget projekt



`416 00:16:03,120 --> 00:16:04,260`
i administrationsmodellen.



`417 00:16:04,840 --> 00:16:05,980`
Då kan man bygga in



`418 00:16:05,980 --> 00:16:08,360`
den typen av dynamiskt stöd i



`419 00:16:08,360 --> 00:16:09,340`
sin pipeline direkt.



`420 00:16:09,940 --> 00:16:12,360`
Det här är gjort så att det blir



`421 00:16:12,360 --> 00:16:14,440`
en mer eller mindre cop-and-paste-förfarande.



`422 00:16:14,900 --> 00:16:17,020`
Det vill säga att din egen säkerhetsorganisation



`423 00:16:17,020 --> 00:16:18,040`
kan göra det här.



`424 00:16:18,420 --> 00:16:19,660`
Det här finns redan idag.



`425 00:16:19,960 --> 00:16:22,040`
Det är bara det att ofta så ligger det inte i



`426 00:16:22,040 --> 00:16:24,180`
din utvecklingskedja utan det ligger i



`427 00:16:24,180 --> 00:16:26,520`
målnet då. Så om man tar Google till exempel.



`428 00:16:26,540 --> 00:16:28,540`
Så har de SCC



`429 00:16:28,540 --> 00:16:30,540`
SCC heter det va?



`430 00:16:30,860 --> 00:16:32,720`
Nej, det heter



`431 00:16:32,720 --> 00:16:34,760`
Security Command



`432 00:16:34,760 --> 00:16:36,320`
Center tror jag det heter.



`433 00:16:36,820 --> 00:16:38,360`
Där kan du bygga. Det är en



`434 00:16:38,360 --> 00:16:40,460`
premium Google-produkt. Man får betala för



`435 00:16:40,460 --> 00:16:41,140`
att använda den.



`436 00:16:42,100 --> 00:16:44,380`
Men det gör ju många som har ett stort ekosystem i Google.



`437 00:16:44,800 --> 00:16:46,240`
Där inne kan man göra de här definitionerna



`438 00:16:46,240 --> 00:16:48,260`
och leta efter konstiga beroende. Men det går



`439 00:16:48,260 --> 00:16:50,540`
absolut lika bra att lägga det inne i



`440 00:16:51,200 --> 00:16:52,020`
din



`441 00:16:52,020 --> 00:16:54,480`
om du kör GitLab eller GitOps



`442 00:16:54,480 --> 00:16:55,120`
på GitHub.



`443 00:16:56,540 --> 00:16:58,520`
Men det det gör då är att man kan ha flera.



`444 00:16:58,640 --> 00:17:00,580`
Du behöver inte bara stödja VIF till



`445 00:17:00,580 --> 00:17:02,500`
eller Workload Identity Federation till Google



`446 00:17:02,500 --> 00:17:04,220`
utan du kan ha Azure, du kan ha



`447 00:17:04,220 --> 00:17:06,920`
gängse OpenID-connect-stackar



`448 00:17:06,920 --> 00:17:08,500`
där som du har patterns i.



`449 00:17:08,600 --> 00:17:10,540`
Och det gör att man får en bredare



`450 00:17:10,540 --> 00:17:12,580`
möjlighet att bygga ett tool som



`451 00:17:12,580 --> 00:17:14,580`
passar till allt. Och då behöver man



`452 00:17:14,580 --> 00:17:16,400`
inte vara beroende av en månleverantör.



`453 00:17:16,520 --> 00:17:18,540`
Så det är idén med det här. Och att det



`454 00:17:18,540 --> 00:17:20,360`
då sen kan monteras utav



`455 00:17:20,360 --> 00:17:22,240`
säkerhetspersonalen själva här, så typ



`456 00:17:22,240 --> 00:17:24,460`
Security Engineering. Och så kan man då



`457 00:17:24,460 --> 00:17:26,460`
baserat på pentest,



`458 00:17:26,540 --> 00:17:28,420`
bug-rapporter, hela tiden bygga



`459 00:17:28,420 --> 00:17:30,660`
patterns. Och det som är



`460 00:17:30,660 --> 00:17:32,340`
bra med det här då är att det kommer ju inte med



`461 00:17:32,340 --> 00:17:34,300`
en prislapp som man får tappa hakan på



`462 00:17:34,300 --> 00:17:36,440`
när man skickar allting till Datadog



`463 00:17:36,440 --> 00:17:38,380`
eller Splunk eller någon annan



`464 00:17:38,380 --> 00:17:40,420`
sån tredjepartsgrej. Utan det här



`465 00:17:40,420 --> 00:17:41,940`
är någonting som du aggregerar själv



`466 00:17:41,940 --> 00:17:44,280`
och som kan lätt



`467 00:17:44,280 --> 00:17:46,460`
huckas in på varje



`468 00:17:46,460 --> 00:17:48,160`
produktionsbygge, varje release



`469 00:17:48,160 --> 00:17:50,320`
eller vad Peter var inne på då med...



`470 00:17:50,320 --> 00:17:52,220`
Men den granskar inte config då utan den granskar



`471 00:17:52,220 --> 00:17:53,920`
log då eller? Nej, den



`472 00:17:53,920 --> 00:17:55,560`
tittar på kommitten.



`473 00:17:56,540 --> 00:17:58,920`
Och vad som kommer ske. Så man kan säga



`474 00:17:58,920 --> 00:18:00,140`
att den gör som en liten



`475 00:18:00,140 --> 00:18:02,960`
simulering. Så Terraform Plan, det gör



`476 00:18:02,960 --> 00:18:04,780`
den inte egentligen. Det är bara coolt att säga så.



`477 00:18:04,860 --> 00:18:06,760`
Men vad den gör är att den tittar på patterns som ligger



`478 00:18:06,760 --> 00:18:09,040`
i konfigurationen. Så det är en linter egentligen.



`479 00:18:09,460 --> 00:18:10,920`
Men det är en linter som gör att du kan



`480 00:18:10,920 --> 00:18:12,840`
själv definiera vad det är du vill titta



`481 00:18:12,840 --> 00:18:14,440`
efter utan att vara liksom en jävla



`482 00:18:14,440 --> 00:18:16,780`
ninja på konstiga



`483 00:18:16,780 --> 00:18:18,680`
rättighetsmodeller och så.



`484 00:18:19,280 --> 00:18:20,900`
Så då kan den... Och det som är bra



`485 00:18:20,900 --> 00:18:22,920`
då är att den... Det är här inte klart än, men nu



`486 00:18:22,920 --> 00:18:24,880`
då så har jag så att den kan titta



`487 00:18:24,880 --> 00:18:26,260`
på diffar mellan olika



`488 00:18:26,540 --> 00:18:28,820`
utkopplade till användare i organisationen.



`489 00:18:29,200 --> 00:18:30,960`
Och då kan den titta på hur saker och ting är



`490 00:18:30,960 --> 00:18:33,160`
skopat fram och tillbaka. Och då kan den se förändringar



`491 00:18:33,160 --> 00:18:34,700`
och sådär. Så då kan man lätt se om någon



`492 00:18:34,700 --> 00:18:36,800`
får för höga rättigheter eller om man har glömt



`493 00:18:36,800 --> 00:18:37,660`
att städa eller



`494 00:18:37,660 --> 00:18:40,300`
om Kalle i



`495 00:18:40,300 --> 00:18:42,900`
Hackathon-report som vi satte upp för att bygga



`496 00:18:42,900 --> 00:18:44,820`
en godisautomat kan ta



`497 00:18:44,820 --> 00:18:47,180`
över våran ekonomiserver



`498 00:18:47,180 --> 00:18:48,880`
för att vi har



`499 00:18:48,880 --> 00:18:50,900`
inte så bra koll på separation i organisationen.



`500 00:18:50,960 --> 00:18:51,780`
Sådana där grejer till exempel.



`501 00:18:52,620 --> 00:18:54,600`
Så det är ganska bra. Och det är inte så svårt, men det är ganska



`502 00:18:54,600 --> 00:18:56,520`
mäckigt och stökigt att leta manuellt.



`503 00:18:56,540 --> 00:18:58,380`
Det är svårt.



`504 00:18:58,680 --> 00:19:00,660`
Men ja, så det håller jag på med. Och det tänkte jag



`505 00:19:00,660 --> 00:19:01,480`
skulle komma vidare med.



`506 00:19:02,300 --> 00:19:04,040`
Och det kommer givetvis släppas open source.



`507 00:19:04,200 --> 00:19:05,940`
Alltså för liksom



`508 00:19:05,940 --> 00:19:08,480`
vem som helst att använda. Just för att jag tror att



`509 00:19:08,480 --> 00:19:09,340`
det är en bra grej.



`510 00:19:10,080 --> 00:19:12,100`
Ska vi ha ett release-party då när du släpper?



`511 00:19:12,640 --> 00:19:14,480`
Jag vet inte om det förtjänar ett release-party.



`512 00:19:14,660 --> 00:19:16,780`
En release-skål



`513 00:19:16,780 --> 00:19:18,320`
eller en release-kampanj på ett podcast.



`514 00:19:18,920 --> 00:19:20,280`
Ja, en liten release-ölja.



`515 00:19:20,300 --> 00:19:22,460`
Det var lite länge sedan vi fick en



`516 00:19:22,460 --> 00:19:23,740`
André Chloé. Ja, precis.



`517 00:19:23,740 --> 00:19:26,240`
Men jag hade det mest oseriösa



`518 00:19:26,240 --> 00:19:28,160`
instiget någonsin. Men du var så



`519 00:19:28,160 --> 00:19:30,000`
seriös att fokusera, så jag vill inte avbryta det.



`520 00:19:30,280 --> 00:19:32,100`
Men du var inne på svåra förkortningar på



`521 00:19:32,100 --> 00:19:33,640`
S. Ja. Och jag



`522 00:19:33,640 --> 00:19:35,820`
lärde mig typ nu att



`523 00:19:35,820 --> 00:19:38,240`
en påven på Polisius, han har



`524 00:19:38,240 --> 00:19:40,560`
nu exkommunikadat



`525 00:19:40,560 --> 00:19:42,660`
SSPX.



`526 00:19:43,400 --> 00:19:44,300`
Och det låter ju som att det är



`527 00:19:44,300 --> 00:19:45,440`
ett nätverksprotokoll, men



`528 00:19:45,440 --> 00:19:48,080`
om ni använder någonting som heter SSPX så är det



`529 00:19:48,080 --> 00:19:50,220`
nu. Det är inte godkänt av kataliker att köra det



`530 00:19:50,220 --> 00:19:51,200`
längre. Vad är det då?



`531 00:19:51,900 --> 00:19:54,200`
Det är en...



`532 00:19:54,200 --> 00:19:56,200`
Om jag fick förkortningen rätt nu så är det



`533 00:19:56,200 --> 00:19:57,080`
alltså en



`534 00:19:57,080 --> 00:20:00,040`
före detta förgrenning



`535 00:20:00,040 --> 00:20:02,320`
av katolicismen som nu



`536 00:20:02,320 --> 00:20:04,260`
då är helt



`537 00:20:04,260 --> 00:20:06,380`
no longer



`538 00:20:06,380 --> 00:20:08,200`
pope approved som då



`539 00:20:08,200 --> 00:20:10,140`
anser att det var



`540 00:20:10,140 --> 00:20:12,060`
typ olagligt



`541 00:20:12,060 --> 00:20:14,000`
av påvan och andra nötter att



`542 00:20:14,000 --> 00:20:16,440`
tillåta folk att börja snacka



`543 00:20:16,440 --> 00:20:18,420`
vanligt språk i kyrkan



`544 00:20:18,420 --> 00:20:20,220`
och så, utan det ska vara latin



`545 00:20:20,220 --> 00:20:21,140`
i kyrkan och så.



`546 00:20:21,580 --> 00:20:24,180`
Och lite annat som hände



`547 00:20:24,180 --> 00:20:25,940`
där i samband med det är liksom inte



`548 00:20:26,200 --> 00:20:27,480`
rätta tro nu, så att...



`549 00:20:27,480 --> 00:20:30,000`
Så nu finns det en ny typ



`550 00:20:30,000 --> 00:20:31,860`
tro som förut var



`551 00:20:31,860 --> 00:20:34,220`
en gren av katolicismen, men



`552 00:20:34,220 --> 00:20:36,920`
som nu är SSPX



`553 00:20:36,920 --> 00:20:37,260`
eller någonting.



`554 00:20:37,500 --> 00:20:40,060`
Det är lite som att Stålman går ut och säger att



`555 00:20:40,060 --> 00:20:41,300`
Vim är förbjuden nu.



`556 00:20:43,000 --> 00:20:44,440`
Nu är det Emax som gäller.



`557 00:20:45,500 --> 00:20:45,900`
Usch.



`558 00:20:46,480 --> 00:20:47,280`
Ja, hemskt.



`559 00:20:47,520 --> 00:20:50,440`
Det går ju produktivt inte noll om man ska vara Emax.



`560 00:20:52,440 --> 00:20:52,900`
Yes, yes.



`561 00:20:52,900 --> 00:20:54,660`
Jag får faktiskt



`562 00:20:54,660 --> 00:20:55,900`
tillstå att jag börjar...



`563 00:20:56,200 --> 00:20:57,740`
Jag började med Emax och sen



`564 00:20:57,740 --> 00:20:59,060`
konverterade jag till VI.



`565 00:20:59,880 --> 00:21:01,460`
Ja, jag är en...



`566 00:21:01,460 --> 00:21:03,840`
Det är för att du fortfarande inte har avslutat Emax-svänstret.



`567 00:21:05,880 --> 00:21:08,380`
Det var ett krav på universiteten



`568 00:21:08,380 --> 00:21:10,440`
att man skulle använda Emax i första kursen



`569 00:21:10,440 --> 00:21:11,520`
och det var så såhär



`570 00:21:11,520 --> 00:21:14,160`
jag fucking dör när jag ska köpa det här.



`571 00:21:14,160 --> 00:21:15,780`
Jävla penalistlärare då.



`572 00:21:15,900 --> 00:21:18,600`
Ja, det var ju på Chalmers



`573 00:21:18,600 --> 00:21:19,180`
som jag...



`574 00:21:19,180 --> 00:21:22,280`
Men det bästa med Emax är att man



`575 00:21:22,280 --> 00:21:24,340`
kunde i den så kunde man



`576 00:21:24,340 --> 00:21:26,100`
bli... Vad var det? Eliser?



`577 00:21:26,200 --> 00:21:28,200`
Eller något. Så kunde man få upp en liten



`578 00:21:28,200 --> 00:21:29,500`
psykolog där.



`579 00:21:30,060 --> 00:21:31,860`
Och jag och en kompis, vi satt där och såhär bara



`580 00:21:31,860 --> 00:21:33,440`
vi testar. Och så körde vi



`581 00:21:33,440 --> 00:21:36,160`
båda var för sig utan att titta



`582 00:21:36,160 --> 00:21:37,780`
på varandra. Så körde vi och blev



`583 00:21:37,780 --> 00:21:40,100`
psykanalyserade av denna



`584 00:21:40,100 --> 00:21:41,740`
eminenta, ofällbara AI.



`585 00:21:43,180 --> 00:21:44,100`
Och båda



`586 00:21:44,100 --> 00:21:46,180`
fick slutresultatet där den konstaterade



`587 00:21:46,180 --> 00:21:47,280`
att det var fel på våra vänner.



`588 00:21:48,160 --> 00:21:49,980`
Och vi konstaterade såhär, men vi har ju typ



`589 00:21:49,980 --> 00:21:52,160`
samma vänner. Så då har ju två



`590 00:21:52,160 --> 00:21:54,180`
instanser i den här AI konstaterat att det är våra



`591 00:21:54,180 --> 00:21:55,420`
vänner som är problemet.



`592 00:21:56,200 --> 00:21:57,960`
Vi är väldigt lyckliga. Har det något med Emax att göra?



`593 00:21:58,260 --> 00:22:00,160`
Ja, alltså det är en psykolog du kan få upp



`594 00:22:00,160 --> 00:22:01,760`
inne i Emax. Det låter bra.



`595 00:22:01,940 --> 00:22:04,100`
Det finns ju sjukt mycket sådana



`596 00:22:04,100 --> 00:22:05,120`
Emax extensions.



`597 00:22:06,340 --> 00:22:08,020`
Om man har behövt bygga



`598 00:22:08,020 --> 00:22:10,260`
en psykolog



`599 00:22:10,260 --> 00:22:12,120`
inne i sin happ, då har man gjort något fel.



`600 00:22:12,140 --> 00:22:14,120`
Det säger jag så mycket. Jag får liksom en bild av att någon



`601 00:22:14,120 --> 00:22:16,100`
som aldrig har gått ut. Det är ju inte så att vi



`602 00:22:16,100 --> 00:22:18,000`
själva hade insterat den, utan den låg där



`603 00:22:18,000 --> 00:22:20,480`
som med i defaulten på något sätt.



`604 00:22:20,980 --> 00:22:21,720`
Det är fantastiskt.



`605 00:22:22,860 --> 00:22:24,280`
Och där tänkte jag nog



`606 00:22:24,280 --> 00:22:26,060`
summera. Sen så ska jag...



`607 00:22:26,200 --> 00:22:29,980`
Ni som lyssnar känner inte mig, men jag har alltså



`608 00:22:29,980 --> 00:22:32,200`
lite datorförbud under semestern



`609 00:22:32,200 --> 00:22:34,320`
för att jag är inte så jävla bra på att skita i att sitta vid datorn.



`610 00:22:34,740 --> 00:22:36,200`
Så att jag försöker bara



`611 00:22:36,200 --> 00:22:38,180`
göra det en till två timmar om dagen.



`612 00:22:38,700 --> 00:22:39,820`
För annars är risken att jag



`613 00:22:39,820 --> 00:22:42,100`
spenderade fem veckor



`614 00:22:42,100 --> 00:22:43,460`
framför datorn i alla fall.



`615 00:22:43,960 --> 00:22:46,240`
Och då kommer jag känna mig smutsig



`616 00:22:46,240 --> 00:22:48,020`
efteråt. Så ja,



`617 00:22:48,240 --> 00:22:49,840`
det blir ganska begränsad



`618 00:22:49,840 --> 00:22:51,820`
datoranvändning under semestern av



`619 00:22:51,820 --> 00:22:53,460`
naturliga skäl.



`620 00:22:54,220 --> 00:22:56,180`
Jag har ju det klassiska ingenjörsproblemet.



`621 00:22:56,200 --> 00:22:58,180`
Det vill säga att jag har så svårt att bara göra



`622 00:22:58,180 --> 00:22:59,940`
saker. Allt måste ju planeras först.



`623 00:23:00,300 --> 00:23:02,200`
Såklart. Och då använder



`624 00:23:02,200 --> 00:23:04,000`
jag ju datorn till det. Den är ju



`625 00:23:04,000 --> 00:23:06,000`
ett fantastiskt verktyg för att surfa runt och hitta



`626 00:23:06,000 --> 00:23:06,960`
grejer på internet och så vidare.



`627 00:23:07,780 --> 00:23:10,160`
Så det resulterar i att jag



`628 00:23:10,160 --> 00:23:12,080`
gör nog en jävla massa



`629 00:23:12,080 --> 00:23:14,320`
planering, men exekvering blir det lite tunt med.



`630 00:23:14,780 --> 00:23:15,700`
Generellt. Men jag tänker



`631 00:23:15,700 --> 00:23:17,980`
det förbudet är att jobba med



`632 00:23:17,980 --> 00:23:20,160`
IT-säkerhetsrelaterade grejer.



`633 00:23:20,700 --> 00:23:21,840`
Men googla får man göra.



`634 00:23:21,980 --> 00:23:23,760`
Fråga Claude. Grejer får man göra.



`635 00:23:23,760 --> 00:23:25,520`
Men man får inte liksom sitta och



`636 00:23:26,200 --> 00:23:28,320`
kanske bygga IT-säkerhetsautomation.



`637 00:23:28,740 --> 00:23:30,200`
Det är liksom, det är såhär,



`638 00:23:30,280 --> 00:23:32,120`
man får, vi får lite moderation



`639 00:23:32,120 --> 00:23:33,280`
på det roliga, tänker jag.



`640 00:23:34,480 --> 00:23:36,460`
Jag har ju nästan haft mitt roliga



`641 00:23:36,460 --> 00:23:37,520`
hållet på att säga. Jag har haft



`642 00:23:37,520 --> 00:23:39,700`
bulken av min semester har jag haft.



`643 00:23:40,180 --> 00:23:42,440`
Vi skaffade ju hund, så då har jag haft lite semester



`644 00:23:42,440 --> 00:23:43,380`
för att ta hand om den där hunden.



`645 00:23:43,980 --> 00:23:46,060`
Så nu är det slut på semestern.



`646 00:23:47,400 --> 00:23:48,520`
Nu ska det arbetas.



`647 00:23:49,040 --> 00:23:50,220`
Men det är ju ändå lite



`648 00:23:50,220 --> 00:23:52,080`
lugnare sommartid



`649 00:23:52,080 --> 00:23:53,780`
när alla andra är på semester. Så jag hoppas



`650 00:23:53,780 --> 00:23:55,740`
faktiskt kunna bli lite produktivare än vanligt.



`651 00:23:56,200 --> 00:23:58,200`
Och en utav sakerna som vi har skjutit



`652 00:23:58,200 --> 00:24:00,180`
framför mig oändligt länge, det är



`653 00:24:00,180 --> 00:24:01,360`
just att prata med våra



`654 00:24:01,360 --> 00:24:04,180`
nya LLM overlords i en större



`655 00:24:04,180 --> 00:24:05,860`
utsträckning. Jag har en massa lite



`656 00:24:05,860 --> 00:24:08,200`
små mini-verktygsprojekt



`657 00:24:08,980 --> 00:24:10,260`
som kan hjälpa mig



`658 00:24:10,260 --> 00:24:11,600`
i min kundmiljö.



`659 00:24:12,540 --> 00:24:14,280`
Som är färdiga i min hjärna. De ska bara



`660 00:24:14,280 --> 00:24:16,140`
ta sig från hjärnan till



`661 00:24:16,140 --> 00:24:18,140`
tangentbordet och ett



`662 00:24:18,140 --> 00:24:20,080`
repository någonstans. Så nu hoppas jag faktiskt



`663 00:24:20,080 --> 00:24:21,480`
att det ska hända. Det ska bli lite nice.



`664 00:24:21,620 --> 00:24:23,820`
Men det där lät mycket mer som jobb än semester.



`665 00:24:23,820 --> 00:24:26,140`
Ja, det där var, som sagt, semestern är slut.



`666 00:24:26,200 --> 00:24:28,040`
Men det är fortfarande sommaravsnitt.



`667 00:24:28,180 --> 00:24:30,120`
Och det här är sommar. Det är definitivt jobb.



`668 00:24:31,700 --> 00:24:33,900`
Så när ni känner att



`669 00:24:33,900 --> 00:24:36,220`
ni kanske fick inte en sån



`670 00:24:36,220 --> 00:24:38,340`
semester när ni har sett fram emot. Tänk på att Mattias jobbar.



`671 00:24:38,700 --> 00:24:39,020`
Ja, precis.



`672 00:24:40,500 --> 00:24:41,920`
Men jag måste erkänna att de



`673 00:24:41,920 --> 00:24:43,900`
två veckorna, en och en halv veckorna



`674 00:24:43,900 --> 00:24:46,040`
jag fick runt midsommar, de gjorde



`675 00:24:46,040 --> 00:24:47,940`
jävla nytta. Jag fick bra fart



`676 00:24:47,940 --> 00:24:50,120`
i kroppen av att



`677 00:24:50,120 --> 00:24:51,940`
landa lite. Normalt brukar jag behöva



`678 00:24:51,940 --> 00:24:53,960`
riktigt mycket tid på mig för att



`679 00:24:53,960 --> 00:24:55,960`
komma ner. Men jag har inte riktigt



`680 00:24:56,200 --> 00:24:58,060`
fungerat. Det var ju jävligt bra värde runt midsommar.



`681 00:24:58,120 --> 00:24:58,920`
Det kan ju ha varit en faktor.



`682 00:24:59,800 --> 00:25:00,720`
Ja, det var det. Verkligen.



`683 00:25:01,560 --> 00:25:04,140`
Så det kommer hända i tanken.



`684 00:25:05,540 --> 00:25:05,580`
Och



`685 00:25:05,580 --> 00:25:08,040`
sen, tack vare hunden igen då



`686 00:25:08,040 --> 00:25:10,140`
som behöver tillsyn



`687 00:25:10,140 --> 00:25:12,260`
så kan ju mina ungdomar



`688 00:25:12,260 --> 00:25:14,020`
hemma inte sommarjobba som de hade tänkt sig.



`689 00:25:14,120 --> 00:25:15,800`
Så då sätter jag dem i sommarjobb.



`690 00:25:16,140 --> 00:25:17,760`
Så det kommer isoleras



`691 00:25:17,760 --> 00:25:20,020`
vinden och det kommer byggas



`692 00:25:20,020 --> 00:25:21,480`
om i förrådet.



`693 00:25:21,980 --> 00:25:24,260`
Och massor med andra sådana här hemmaprojekt.



`694 00:25:26,200 --> 00:25:27,400`
Mot betalning då givetvis.



`695 00:25:27,500 --> 00:25:29,380`
Pappa är någon slags arbetsgivare.



`696 00:25:29,620 --> 00:25:30,080`
Mat.



`697 00:25:30,780 --> 00:25:32,800`
De ska få lite pengar också faktiskt.



`698 00:25:33,020 --> 00:25:35,280`
Så de kan spendera på att köpa



`699 00:25:35,280 --> 00:25:36,380`
nya dyra datordelar.



`700 00:25:38,180 --> 00:25:39,520`
Så det ska också



`701 00:25:39,520 --> 00:25:40,120`
hända.



`702 00:25:41,580 --> 00:25:43,720`
Och sen så ska det äntligen



`703 00:25:43,720 --> 00:25:45,520`
hackas



`704 00:25:45,520 --> 00:25:46,340`
osiloskop.



`705 00:25:46,980 --> 00:25:49,720`
Just det, det var det här projektet. Det hade vi gett i avsnitten.



`706 00:25:50,160 --> 00:25:51,920`
Jag köpte ju det här osiloskopet



`707 00:25:51,920 --> 00:25:52,800`
som vi knappt har använt.



`708 00:25:52,800 --> 00:25:54,940`
Och jag researchade så in i helvete.



`709 00:25:55,040 --> 00:25:55,980`
För om man köpte rätt,



`710 00:25:56,200 --> 00:25:58,840`
den billiga versionen, så kunde man sen hacka



`711 00:25:58,840 --> 00:26:00,760`
den och få all funktionalitet.



`712 00:26:01,080 --> 00:26:02,700`
Hundra megaherts i stora



`713 00:26:02,700 --> 00:26:03,720`
minnet och alltihopa.



`714 00:26:03,980 --> 00:26:06,180`
Och om man dessutom köpte en liten



`715 00:26:06,180 --> 00:26:07,700`
add-on board



`716 00:26:07,700 --> 00:26:10,820`
och populerade den



`717 00:26:10,820 --> 00:26:12,740`
med rätt kretskort och borrade ett hål



`718 00:26:12,740 --> 00:26:15,040`
i chassit



`719 00:26:15,040 --> 00:26:16,880`
så kunde man dessutom få en logikanalysator.



`720 00:26:18,120 --> 00:26:18,900`
Då kunde man



`721 00:26:18,900 --> 00:26:21,000`
typ köpa den för nästan samma pengar.



`722 00:26:21,000 --> 00:26:22,720`
Men jag tänkte, det är så jävla roligt att man kan



`723 00:26:22,720 --> 00:26:25,040`
hacka sina grejer. Så jag köpte en sån också.



`724 00:26:25,040 --> 00:26:27,040`
Dels ska det mjukvaruhackas då



`725 00:26:27,040 --> 00:26:29,040`
och dels ska det hårdvaruhackas osiloskopet.



`726 00:26:29,040 --> 00:26:31,040`
Så det ser jag fram emot supermycket.



`727 00:26:31,040 --> 00:26:33,040`
Sen hoppas jag kunna använda



`728 00:26:33,040 --> 00:26:35,040`
Aset också.



`729 00:26:35,040 --> 00:26:37,040`
Vad är det för osiloskop?



`730 00:26:37,040 --> 00:26:39,040`
Rigol någonting.



`731 00:26:39,040 --> 00:26:41,040`
Jag kommer inte ihåg vilken det var jag köpte.



`732 00:26:41,040 --> 00:26:43,040`
Men jag läste på nogsamt innan.



`733 00:26:43,040 --> 00:26:45,040`
Så det borde bli rätt.



`734 00:26:47,040 --> 00:26:49,040`
Så det ska bli ball.



`735 00:26:49,040 --> 00:26:51,040`
Sen var det en grej till



`736 00:26:51,040 --> 00:26:53,040`
jag funderade på, men den har jag förträngt nu.



`737 00:26:53,040 --> 00:26:55,040`
Sen var det en grej till jag funderade på, men den har jag förträngt nu.



`738 00:26:55,040 --> 00:26:57,040`
Sen var det en grej till jag funderade på, men den har jag förträngt nu.



`739 00:26:57,040 --> 00:26:59,040`
Det var nog din grej jag gick igång på.



`740 00:26:59,040 --> 00:27:01,040`
Det passar nästan över till dig.



`741 00:27:01,040 --> 00:27:03,040`
Det passar nästan över till dig.



`742 00:27:03,040 --> 00:27:05,040`
Jag ser vad jag ska hitta på.



`743 00:27:05,040 --> 00:27:07,040`
Jag har haft en sabbatical



`744 00:27:07,040 --> 00:27:09,040`
jag har haft en sabbatical



`745 00:27:09,040 --> 00:27:11,040`
med cellgifter och skit.



`746 00:27:11,040 --> 00:27:13,040`
Men jag kommer ändå



`747 00:27:13,040 --> 00:27:15,040`
men jag kommer ändå



`748 00:27:15,040 --> 00:27:17,040`
kunna ägna mig lite åt



`749 00:27:17,040 --> 00:27:19,040`
extra kurrikulära aktiviteter



`750 00:27:19,040 --> 00:27:21,040`
även om jag inte tar någon regelrätt semester.



`751 00:27:21,040 --> 00:27:23,040`
även om jag inte tar någon regelrätt semester.



`752 00:27:23,040 --> 00:27:25,040`
Så,



`753 00:27:25,040 --> 00:27:27,040`
en grej som jag har halkat in på



`754 00:27:27,040 --> 00:27:29,040`
som



`755 00:27:29,040 --> 00:27:31,040`
två av mina kollegor



`756 00:27:31,040 --> 00:27:33,040`
har lekt med ett tag



`757 00:27:33,040 --> 00:27:35,040`
det är Louis och Thomas



`758 00:27:35,040 --> 00:27:37,040`
som har pildrat på det här



`759 00:27:37,040 --> 00:27:39,040`
är MeshCore



`760 00:27:39,040 --> 00:27:41,040`
som då är



`761 00:27:41,040 --> 00:27:43,040`
off-grid-kommunikation



`762 00:27:43,040 --> 00:27:45,040`
textbaserad off-grid-kommunikation



`763 00:27:45,040 --> 00:27:47,040`
textbaserad off-grid-kommunikation



`764 00:27:47,040 --> 00:27:49,040`
som bygger på LoRaWAN.



`765 00:27:49,040 --> 00:27:51,040`
Det är någon slags flavor av MeshTastic, va?



`766 00:27:51,040 --> 00:27:53,040`
Ja, det kan man säga.



`767 00:27:53,040 --> 00:27:55,040`
Typ samma



`768 00:27:55,040 --> 00:27:57,040`
bärare eller



`769 00:27:57,040 --> 00:27:59,040`
man kan säga samma typ av



`770 00:27:59,040 --> 00:28:01,040`
det är också LoRaWAN-baserat.



`771 00:28:01,040 --> 00:28:03,040`
MeshCore har lite



`772 00:28:03,040 --> 00:28:05,040`
mer logik



`773 00:28:05,040 --> 00:28:07,040`
vad gäller routing och sånt där



`774 00:28:07,040 --> 00:28:09,040`
så det blir inte så att du spammar ut



`775 00:28:09,040 --> 00:28:11,040`
till alla utan att



`776 00:28:11,040 --> 00:28:13,040`
det blir lite snyggare



`777 00:28:13,040 --> 00:28:15,040`
det blir lite snyggare protokoll.



`778 00:28:15,040 --> 00:28:17,040`
Och som det verkar



`779 00:28:17,040 --> 00:28:19,040`
så är det MeshCore som



`780 00:28:19,040 --> 00:28:21,040`
är mest poppis



`781 00:28:21,040 --> 00:28:23,040`
här omkring i alla fall.



`782 00:28:23,040 --> 00:28:25,040`
Och



`783 00:28:25,040 --> 00:28:27,040`
det har jag precis



`784 00:28:27,040 --> 00:28:29,040`
jag har ju gått



`785 00:28:29,040 --> 00:28:31,040`
haywire på



`786 00:28:31,040 --> 00:28:33,040`
AliExpress och



`787 00:28:33,040 --> 00:28:35,040`
Amazon men alla prylar



`788 00:28:35,040 --> 00:28:37,040`
har inte dykt upp än så att



`789 00:28:37,040 --> 00:28:39,040`
nu liksom verkligen törstar jag efter



`790 00:28:39,040 --> 00:28:41,040`
att få hit lite



`791 00:28:41,040 --> 00:28:43,040`
schyssta



`792 00:28:43,040 --> 00:28:45,040`
antenner och



`793 00:28:45,040 --> 00:28:47,040`
experimentkort som man kan hålla på



`794 00:28:47,040 --> 00:28:49,040`
och leka med och bygga repeaternoder.



`795 00:28:49,040 --> 00:28:51,040`
Det är väldigt, väldigt



`796 00:28:51,040 --> 00:28:53,040`
ensamt i Björlanda kan jag säga.



`797 00:28:53,040 --> 00:28:55,040`
Men repeaternoderna



`798 00:28:55,040 --> 00:28:57,040`
som man sätter upp får alla vara med på dem



`799 00:28:57,040 --> 00:28:59,040`
eller är det bara, alltså det blir som LoRa



`800 00:28:59,040 --> 00:29:01,040`
liksom att man delar, det blir open source.



`801 00:29:01,040 --> 00:29:03,040`
För det där är, jag vill ju ha en sån



`802 00:29:03,040 --> 00:29:05,040`
bara för att man hjälper till.



`803 00:29:05,040 --> 00:29:07,040`
Så tänker jag.



`804 00:29:07,040 --> 00:29:09,040`
Ja men det gör man och



`805 00:29:09,040 --> 00:29:11,040`
alla kan ha nytta av den liksom



`806 00:29:11,040 --> 00:29:13,040`
så att det är



`807 00:29:13,040 --> 00:29:15,040`
en



`808 00:29:15,040 --> 00:29:17,040`
en



`809 00:29:17,040 --> 00:29:19,040`
en



`810 00:29:19,040 --> 00:29:21,040`
en före detta arbetsgivare har en



`811 00:29:21,040 --> 00:29:23,040`
väldigt, väldigt bra



`812 00:29:23,040 --> 00:29:25,040`
LoRaWAN repeater på en väldigt, väldigt



`813 00:29:25,040 --> 00:29:27,040`
hög punkt som är ett skyddsobjekt



`814 00:29:27,040 --> 00:29:29,040`
här i stan.



`815 00:29:29,040 --> 00:29:31,040`
Men frågan är,



`816 00:29:31,040 --> 00:29:33,040`
kan du med din meshcore-burk



`817 00:29:33,040 --> 00:29:35,040`
rida på LoRa



`818 00:29:35,040 --> 00:29:37,040`
repeaters? Ja, alltså bara de



`819 00:29:37,040 --> 00:29:39,040`
som



`820 00:29:39,040 --> 00:29:41,040`
kör meshcore-protokollet.



`821 00:29:41,040 --> 00:29:43,040`
Så det installerar man också då?



`822 00:29:43,040 --> 00:29:45,040`
För det är ju, är det line of sight?



`823 00:29:45,040 --> 00:29:47,040`
Det är line of sight i princip. Så högt är bra?



`824 00:29:47,040 --> 00:29:49,040`
Högt är skitbra. Kalatornet



`825 00:29:49,040 --> 00:29:51,040`
hade varit vårt dröm. Ja, tja.



`826 00:29:51,040 --> 00:29:53,040`
Världens accepted. Hur svårt kan det vara att ta sig upp dit?



`827 00:29:53,040 --> 00:29:55,040`
Men betyder det då att för att det här



`828 00:29:55,040 --> 00:29:57,040`
ska bli optimalt i världen



`829 00:29:57,040 --> 00:29:59,040`
så är det bra om, när man bygger



`830 00:29:59,040 --> 00:30:01,040`
en repeaters så måste man ju supporta både



`831 00:30:01,040 --> 00:30:03,040`
meshcore, meshtastic och LoRa då?



`832 00:30:03,040 --> 00:30:05,040`
Kan man det?



`833 00:30:05,040 --> 00:30:07,040`
Så långt har jag faktiskt... För annars blir det ju 3D



`834 00:30:07,040 --> 00:30:09,040`
alltså trippelhårdvara istället för



`835 00:30:09,040 --> 00:30:11,040`
enkelhårdvara. Det låter kanont.



`836 00:30:11,040 --> 00:30:13,040`
Det blir nog svårt



`837 00:30:13,040 --> 00:30:15,040`
tror jag. Alltså mesh, meshtastic



`838 00:30:15,040 --> 00:30:17,040`
och meshcore kör ju olika.



`839 00:30:19,040 --> 00:30:21,040`
Så att de är ju inte rakt av kompatibla.



`840 00:30:21,040 --> 00:30:23,040`
Utan där får du ju, det är ju samma hårdvara



`841 00:30:23,040 --> 00:30:25,040`
du får flasha den med



`842 00:30:25,040 --> 00:30:27,040`
annan



`843 00:30:27,040 --> 00:30:29,040`
stack egentligen.



`844 00:30:29,040 --> 00:30:31,040`
Men du har ju med dig en liten hack i



`845 00:30:31,040 --> 00:30:33,040`
liten pryl här också. Den ser ju inte lyssnarna



`846 00:30:33,040 --> 00:30:35,040`
men den... Den ser ut som en



`847 00:30:35,040 --> 00:30:37,040`
liten gammaldags blackberry



`848 00:30:37,040 --> 00:30:39,040`
fast med en roligare antenn på.



`849 00:30:39,040 --> 00:30:41,040`
Så jag



`850 00:30:41,040 --> 00:30:43,040`
har roat mig nu med...



`851 00:30:43,040 --> 00:30:45,040`
Man blir väldigt nördig vad gäller topografi



`852 00:30:45,040 --> 00:30:47,040`
för att man går runt och ut



`853 00:30:47,040 --> 00:30:49,040`
i skogen och letar höga



`854 00:30:49,040 --> 00:30:51,040`
punkter och klättrar på berg



`855 00:30:51,040 --> 00:30:53,040`
och ser om...



`856 00:30:53,040 --> 00:30:55,040`
Vad når jag här då?



`857 00:30:55,040 --> 00:30:57,040`
Det är lite som old school mobiltelefoni.



`858 00:30:57,040 --> 00:30:59,040`
Absolut. Ja men upp på



`859 00:30:59,040 --> 00:31:01,040`
höga höjder och se



`860 00:31:01,040 --> 00:31:03,040`
vilka noder hör jag här?



`861 00:31:03,040 --> 00:31:05,040`
Och vem hör mig om jag skickar ett meddelande?



`862 00:31:05,040 --> 00:31:07,040`
Och det är ju mer



`863 00:31:07,040 --> 00:31:09,040`
för att liksom kunna



`864 00:31:09,040 --> 00:31:11,040`
planera. För jag är ju väldigt



`865 00:31:11,040 --> 00:31:13,040`
sugen på att i alla fall



`866 00:31:13,040 --> 00:31:15,040`
få ut trafik från



`867 00:31:15,040 --> 00:31:17,040`
innerstan ut till



`868 00:31:17,040 --> 00:31:19,040`
Björlanda. Sen är



`869 00:31:19,040 --> 00:31:21,040`
jag inte så... Ja men fine.



`870 00:31:21,040 --> 00:31:23,040`
Jag sätter den på taket så...



`871 00:31:23,040 --> 00:31:25,040`
Jag ser heliumballong framför mig.



`872 00:31:25,040 --> 00:31:27,040`
Ja det... En liten sån



`873 00:31:27,040 --> 00:31:29,040`
blimp. En siktig lösning bara.



`874 00:31:29,040 --> 00:31:31,040`
Ja. Men vad är visionen?



`875 00:31:31,040 --> 00:31:33,040`
Du vill ha konnektivitet.



`876 00:31:33,040 --> 00:31:35,040`
Jag vill ha konnektivitet och jag kommer även



`877 00:31:35,040 --> 00:31:37,040`
att skruva upp en i stugan. Där kommer jag vara



`878 00:31:37,040 --> 00:31:39,040`
skitensam.



`879 00:31:39,040 --> 00:31:41,040`
Men det finns en höjd där som...



`880 00:31:41,040 --> 00:31:43,040`
Så att om någon skulle få upp en sån där



`881 00:31:43,040 --> 00:31:45,040`
på typ...



`882 00:31:45,040 --> 00:31:47,040`
Vad heter...



`883 00:31:49,040 --> 00:31:51,040`
Fulefjället eller



`884 00:31:51,040 --> 00:31:53,040`
Fjällstangen eller



`885 00:31:53,040 --> 00:31:55,040`
Näsberget eller någonting liksom.



`886 00:31:55,040 --> 00:31:57,040`
Då kommer jag ju att höra dem.



`887 00:31:57,040 --> 00:31:59,040`
Så att Lövnäs ligger ju på



`888 00:31:59,040 --> 00:32:01,040`
440 meter



`889 00:32:01,040 --> 00:32:03,040`
ungefär vid sjön.



`890 00:32:03,040 --> 00:32:05,040`
Så att...



`891 00:32:05,040 --> 00:32:07,040`
Ja. Kommer det upp en repeater



`892 00:32:07,040 --> 00:32:09,040`
på någon av fjälltopparna så kommer jag ju



`893 00:32:09,040 --> 00:32:11,040`
att höra dem. Än så länge så finns



`894 00:32:11,040 --> 00:32:13,040`
det inga. Norra Dalarna är precis



`895 00:32:13,040 --> 00:32:15,040`
kolsvart. Det är så alltså. Ja så är det.



`896 00:32:15,040 --> 00:32:17,040`
Men någon måste vara först. Ja för det är intressant



`897 00:32:17,040 --> 00:32:19,040`
då. Det är så synd det här



`898 00:32:19,040 --> 00:32:21,040`
just att för Lora är väl ändå rätt



`899 00:32:21,040 --> 00:32:23,040`
utbyggt liksom. Ja. Och MeshTest



`900 00:32:23,040 --> 00:32:25,040`
det har funnits ganska länge så det kan jag tänka mig också



`901 00:32:25,040 --> 00:32:27,040`
är decentlig utbyggt i alla fall. Och så kommer



`902 00:32:27,040 --> 00:32:29,040`
nu ytterligare en jävla... Okej kanske



`903 00:32:29,040 --> 00:32:31,040`
bättre då men det är så synd att de inte är kompatibla



`904 00:32:31,040 --> 00:32:33,040`
menar jag för att då börjar man om på



`905 00:32:33,040 --> 00:32:35,040`
fansidan noll igen liksom.



`906 00:32:35,040 --> 00:32:37,040`
Börja bygga USB för radio.



`907 00:32:37,040 --> 00:32:39,040`
USB?



`908 00:32:39,040 --> 00:32:41,040`
Universal Serial Bus.



`909 00:32:41,040 --> 00:32:43,040`
Med U1.



`910 00:32:43,040 --> 00:32:45,040`
Trycka in alltihop.



`911 00:32:45,040 --> 00:32:47,040`
Jag kan väl hålla med till viss del.



`912 00:32:47,040 --> 00:32:49,040`
Framförallt...



`913 00:32:49,040 --> 00:32:51,040`
att det...



`914 00:32:51,040 --> 00:32:53,040`
det inte...



`915 00:32:53,040 --> 00:32:55,040`
alltså att inte använda



`916 00:32:55,040 --> 00:32:57,040`
samma protokoll. Men samtidigt som...



`917 00:32:57,040 --> 00:32:59,040`
Men det är väl snarare ett argument



`918 00:32:59,040 --> 00:33:01,040`
mellan att Rage forkar till



`919 00:33:01,040 --> 00:33:03,040`
Linux distrus och sådär. Ja. MeshCore



`920 00:33:03,040 --> 00:33:05,040`
har ju också forkats i två.



`921 00:33:05,040 --> 00:33:07,040`
Bara där liksom. Bara för det ja.



`922 00:33:07,040 --> 00:33:09,040`
MeshCore.co.uk



`923 00:33:09,040 --> 00:33:11,040`
som tydligen vibecodar alltihopa.



`924 00:33:11,040 --> 00:33:13,040`
Och sen så har du MeshCore.io



`925 00:33:13,040 --> 00:33:15,040`
som är då puristerna



`926 00:33:15,040 --> 00:33:17,040`
som då inte vibecodar



`927 00:33:17,040 --> 00:33:19,040`
vad de säger i alla fall.



`928 00:33:19,040 --> 00:33:21,040`
Okej.



`929 00:33:21,040 --> 00:33:23,040`
AI-skism i MeshCore



`930 00:33:23,040 --> 00:33:25,040`
lägret alltså.



`931 00:33:25,040 --> 00:33:27,040`
Nu vet man att man har kommit in i stugvärmen.



`932 00:33:27,040 --> 00:33:29,040`
Men long term vision då, det är att



`933 00:33:29,040 --> 00:33:31,040`
då ska du ha egentligen konnektivitet mellan stugan



`934 00:33:31,040 --> 00:33:33,040`
och hemmet.



`935 00:33:33,040 --> 00:33:35,040`
Alltså det kan man ju... man kan ju ful



`936 00:33:35,040 --> 00:33:37,040`
lösa det. Så jag skulle ju kunna repetera



`937 00:33:37,040 --> 00:33:39,040`
upp om jag använder... Ja, det räknas inte.



`938 00:33:39,040 --> 00:33:41,040`
Nej, det är ju det.



`939 00:33:41,040 --> 00:33:43,040`
Det räknas ju bara för om internet är nere.



`940 00:33:43,040 --> 00:33:45,040`
Ja, okej. Så det är internet som någon form



`941 00:33:45,040 --> 00:33:47,040`
av bär på. Ja, det hade jag ju kunnat göra.



`942 00:33:47,040 --> 00:33:49,040`
Jag har ju stugan och hemmet ihopkopplade.



`943 00:33:49,040 --> 00:33:51,040`
Ja, det känns fake. Det är fail.



`944 00:33:51,040 --> 00:33:53,040`
Men det hade ju varit roligt



`945 00:33:53,040 --> 00:33:55,040`
om man hade kunnat skicka...



`946 00:33:55,040 --> 00:33:57,040`
Sen begränsar man ju



`947 00:33:57,040 --> 00:33:59,040`
ofta antalet hopp och



`948 00:33:59,040 --> 00:34:01,040`
framförallt då



`949 00:34:01,040 --> 00:34:03,040`
utifrån



`950 00:34:03,040 --> 00:34:05,040`
alltså såhär



`951 00:34:05,040 --> 00:34:07,040`
regionsinformation.



`952 00:34:07,040 --> 00:34:09,040`
Så



`953 00:34:09,040 --> 00:34:11,040`
SE14 till exempel



`954 00:34:11,040 --> 00:34:13,040`
det är Göteborgsregionen



`955 00:34:13,040 --> 00:34:15,040`
eller Västra Götaland. Okej.



`956 00:34:15,040 --> 00:34:17,040`
Att du vill hålla kommunikationen lokalt.



`957 00:34:17,040 --> 00:34:19,040`
Ja, precis. Är det liksom del i syftet?



`958 00:34:19,040 --> 00:34:21,040`
Ja, man kan göra det och alltså Meshcore



`959 00:34:21,040 --> 00:34:23,040`
gör ju att



`960 00:34:23,040 --> 00:34:25,040`
du minskar ner trafiken



`961 00:34:25,040 --> 00:34:27,040`
så det blir inte det här fladdringen liksom.



`962 00:34:27,040 --> 00:34:29,040`
Ja, det är de här routing-funktionerna du pratar om liksom.



`963 00:34:29,040 --> 00:34:31,040`
Så du kan hålla



`964 00:34:31,040 --> 00:34:33,040`
kommunikationen lokal. Jag kan också säga



`965 00:34:33,040 --> 00:34:35,040`
att jag repeterar inte vidare



`966 00:34:35,040 --> 00:34:37,040`
Stjärna utan jag repeterar bara vidare



`967 00:34:37,040 --> 00:34:39,040`
SE och SE14 till exempel.



`968 00:34:39,040 --> 00:34:41,040`
Mm.



`969 00:34:41,040 --> 00:34:43,040`
Så även om det finns connection hela vägen upp



`970 00:34:43,040 --> 00:34:45,040`
till stugan så är det inte säkert att du kommer igenom?



`971 00:34:45,040 --> 00:34:47,040`
Nej, så är det. Åh.



`972 00:34:47,040 --> 00:34:49,040`
Det kan bli några hopp.



`973 00:34:49,040 --> 00:34:51,040`
Men återigen,



`974 00:34:51,040 --> 00:34:53,040`
syftet är liksom prio är lokal



`975 00:34:53,040 --> 00:34:55,040`
kommunikation, det är det jag vill prioritera.



`976 00:34:55,040 --> 00:34:57,040`
Men de här



`977 00:34:57,040 --> 00:34:59,040`
det här är helt dum repetering



`978 00:34:59,040 --> 00:35:01,040`
eller det är inte så att det finns någon spanning-protokoll



`979 00:35:01,040 --> 00:35:03,040`
eller hur? Nej, det är dum



`980 00:35:03,040 --> 00:35:05,040`
repetering. Men



`981 00:35:05,040 --> 00:35:07,040`
den har väl någon



`982 00:35:07,040 --> 00:35:09,040`
form av hoppcount så att



`983 00:35:09,040 --> 00:35:11,040`
Ja, just det.



`984 00:35:11,040 --> 00:35:13,040`
När du skickar ut ett meddelande så



`985 00:35:13,040 --> 00:35:15,040`
har den ett



`986 00:35:15,040 --> 00:35:17,040`
CTL och sen så



`987 00:35:17,040 --> 00:35:19,040`
Men kommer den ihåg på något sätt liksom att



`988 00:35:19,040 --> 00:35:21,040`
har jag hört det här paketet nyligen så repeterar



`989 00:35:21,040 --> 00:35:23,040`
den inte igen eller hur?



`990 00:35:23,040 --> 00:35:25,040`
Åh, du frågade mig saker



`991 00:35:25,040 --> 00:35:27,040`
som jag inte har varit inne och tittat på och inte



`992 00:35:27,040 --> 00:35:29,040`
alls kollat på.



`993 00:35:29,040 --> 00:35:31,040`
Så jag har ingen aning. Men det kan man säkert



`994 00:35:31,040 --> 00:35:33,040`
läsa sig till.



`995 00:35:33,040 --> 00:35:35,040`
Jag hade ju en sådan vision, jag har ju



`996 00:35:35,040 --> 00:35:37,040`
en brorsa i Hovås



`997 00:35:37,040 --> 00:35:39,040`
Achim trakterna någonstans



`998 00:35:39,040 --> 00:35:41,040`
en i Floda och mamma i



`999 00:35:41,040 --> 00:35:43,040`
Allingsås. Sen tänkte jag, mm, jag vill fan ha



`1000 00:35:43,040 --> 00:35:45,040`
ett meshnät som når alla dem.



`1001 00:35:45,040 --> 00:35:47,040`
Men line of sight är lite



`1002 00:35:47,040 --> 00:35:49,040`
besvärligt. Jag har upptäckt att det finns



`1003 00:35:49,040 --> 00:35:51,040`
jättemycket berg överallt. Det gör ju det.



`1004 00:35:51,040 --> 00:35:53,040`
Så att det krävs



`1005 00:35:53,040 --> 00:35:55,040`
best case



`1006 00:35:55,040 --> 00:35:57,040`
två stycken riktigt kraftfulla och välplacerande



`1007 00:35:57,040 --> 00:35:59,040`
nodar. Men



`1008 00:35:59,040 --> 00:36:01,040`
i verkligheten förmodligen



`1009 00:36:01,040 --> 00:36:03,040`
Men jag tänker också, det finns ju de här



`1010 00:36:03,040 --> 00:36:05,040`
Shago, vi har pratat om det, de här X



`1011 00:36:05,040 --> 00:36:07,040`
vad de nu heter, 6000 och sådär.



`1012 00:36:07,040 --> 00:36:09,040`
Det är ju radio



`1013 00:36:09,040 --> 00:36:11,040`
fast med någon digital tillämpning



`1014 00:36:11,040 --> 00:36:13,040`
på. Det finns massor med digitala



`1015 00:36:13,040 --> 00:36:15,040`
protokoll över amatörer och det.



`1016 00:36:15,040 --> 00:36:17,040`
Ja, för de har ju räckvidd, jättelång räckvidd.



`1017 00:36:17,040 --> 00:36:19,040`
Ja, ja, ja. För då kan man ju typ skicka



`1018 00:36:19,040 --> 00:36:21,040`
då kan man ju såhär provisionera



`1019 00:36:21,040 --> 00:36:23,040`
Men de måste väl ha jättedåliga mamror



`1020 00:36:23,040 --> 00:36:25,040`
eller vad? Jo, jo, men såhär för



`1021 00:36:25,040 --> 00:36:27,040`
medlande och sånt funkar ju. Ja, men du hörde



`1022 00:36:27,040 --> 00:36:29,040`
inte vad jag sa riktigt. Jag sa



`1023 00:36:29,040 --> 00:36:31,040`
mina två bröder och min mamma



`1024 00:36:31,040 --> 00:36:33,040`
de har ingen radiostation hemma.



`1025 00:36:33,040 --> 00:36:35,040`
Inte än.



`1026 00:36:35,040 --> 00:36:37,040`
Du har ju såhär, jag tänkte just att det skulle



`1027 00:36:37,040 --> 00:36:39,040`
vara ett lättanvänt



`1028 00:36:39,040 --> 00:36:41,040`
protokoll.



`1029 00:36:41,040 --> 00:36:43,040`
Mellan de parterna. Det hade varit bara



`1030 00:36:43,040 --> 00:36:45,040`
ett.



`1031 00:36:45,040 --> 00:36:47,040`
Ja, men ett av syftena



`1032 00:36:47,040 --> 00:36:49,040`
att det här togs fram, det är just



`1033 00:36:49,040 --> 00:36:51,040`
katastrofamråden där



`1034 00:36:51,040 --> 00:36:53,040`
infrastrukturen ligger i spillerur



`1035 00:36:53,040 --> 00:36:55,040`
att man då kan. Gilla av allt.



`1036 00:36:55,040 --> 00:36:57,040`
Ja. Posta på kvalitet. Så att man



`1037 00:36:57,040 --> 00:36:59,040`
man går igång lite på prep-hygienen också.



`1038 00:36:59,040 --> 00:37:01,040`
Exakt. Jag har gjort en



`1039 00:37:01,040 --> 00:37:03,040`
Du hade mer vatten än mig hemma



`1040 00:37:03,040 --> 00:37:05,040`
senast vi diskuterade. Ja, det



`1041 00:37:05,040 --> 00:37:07,040`
har jag säkert.



`1042 00:37:07,040 --> 00:37:09,040`
75 liter.



`1043 00:37:09,040 --> 00:37:11,040`
Ja, jag tror typ 30



`1044 00:37:11,040 --> 00:37:13,040`
eller något. Ja.



`1045 00:37:13,040 --> 00:37:15,040`
Det är bara en pool, men det vill man inte dricka kanske.



`1046 00:37:15,040 --> 00:37:17,040`
Nej. Det är rent.



`1047 00:37:17,040 --> 00:37:19,040`
Ja, och tre sjöar.



`1048 00:37:19,040 --> 00:37:21,040`
Ja, det är bra. Och jävligt många vattenreningspilar.



`1049 00:37:21,040 --> 00:37:23,040`
Har du inte målat



`1050 00:37:23,040 --> 00:37:25,040`
en mörkblå flagga i botten



`1051 00:37:25,040 --> 00:37:27,040`
av din? Nej. Men alltså



`1052 00:37:27,040 --> 00:37:29,040`
där får vi säga för



`1053 00:37:29,040 --> 00:37:31,040`
i Lövnäs så



`1054 00:37:31,040 --> 00:37:33,040`
hade vi inte tänkt



`1055 00:37:33,040 --> 00:37:35,040`
att vi behövde



`1056 00:37:35,040 --> 00:37:37,040`
vattendunka för vi har ju en hel jävla sjö



`1057 00:37:37,040 --> 00:37:39,040`
där. Ja. Ja. Och sen



`1058 00:37:39,040 --> 00:37:41,040`
blir det strömavbrott när det är minus



`1059 00:37:41,040 --> 00:37:43,040`
35 grader kallt. Ja.



`1060 00:37:43,040 --> 00:37:45,040`
Vad är det jobbigt. Ja.



`1061 00:37:45,040 --> 00:37:47,040`
Motorsåg. Ja, det hade jag ju



`1062 00:37:47,040 --> 00:37:49,040`
kunnat göra i och för sig faktiskt, men



`1063 00:37:49,040 --> 00:37:51,040`
isen är jävligt tjock. Alltså jag är inte



`1064 00:37:51,040 --> 00:37:53,040`
säker på att jag får igenom svärdet. Nej.



`1065 00:37:53,040 --> 00:37:55,040`
Det är ju lite gött för du jobbar i



`1066 00:37:55,040 --> 00:37:57,040`
varm. Ja. Så att. Klyvyxa.



`1067 00:37:57,040 --> 00:37:59,040`
Ja, men. En annan off topic



`1068 00:37:59,040 --> 00:38:01,040`
information.



`1069 00:38:01,040 --> 00:38:03,040`
Husqvarna började som vapenproducent



`1070 00:38:03,040 --> 00:38:05,040`
och i USA heter Husqvarna



`1071 00:38:05,040 --> 00:38:07,040`
Husky enligt dem som är



`1072 00:38:07,040 --> 00:38:09,040`
in the know. Ja. Jaha.



`1073 00:38:09,040 --> 00:38:11,040`
Så är det. Husqvarna.



`1074 00:38:11,040 --> 00:38:13,040`
Jag fick upp en motorsågs



`1075 00:38:13,040 --> 00:38:15,040`
influencer på.



`1076 00:38:15,040 --> 00:38:17,040`
Du, det är min Youtube liksom.



`1077 00:38:17,040 --> 00:38:19,040`
Ja.



`1078 00:38:19,040 --> 00:38:21,040`
Fast jag är mer, jag ska inte säga att jag är



`1079 00:38:21,040 --> 00:38:23,040`
mer stilkille för det är jag inte. För jag



`1080 00:38:23,040 --> 00:38:25,040`
har en av varje.



`1081 00:38:25,040 --> 00:38:27,040`
En Husqvarna och en Stil.



`1082 00:38:27,040 --> 00:38:29,040`
Jag har bara Husqvarna



`1083 00:38:29,040 --> 00:38:31,040`
faktiskt. Mm. Det blev så.



`1084 00:38:31,040 --> 00:38:33,040`
Hur står ni i



`1085 00:38:33,040 --> 00:38:35,040`
i el



`1086 00:38:35,040 --> 00:38:37,040`
motorsågen versus



`1087 00:38:37,040 --> 00:38:39,040`
bensin motorsåg. Ja, det är ju bensin



`1088 00:38:39,040 --> 00:38:41,040`
här alltså. Det är det enda jag säger. Ja, två stycken.



`1089 00:38:41,040 --> 00:38:43,040`
Men jag tror att de är ganska bra va?



`1090 00:38:43,040 --> 00:38:45,040`
Jag har en elmotorsåg



`1091 00:38:45,040 --> 00:38:47,040`
en sådan arboristsåg.



`1092 00:38:47,040 --> 00:38:49,040`
Och sen har jag



`1093 00:38:49,040 --> 00:38:51,040`
två bensin motorsågar



`1094 00:38:51,040 --> 00:38:53,040`
och två röjsågar.



`1095 00:38:53,040 --> 00:38:55,040`
Men den elgrejen den är väl okej



`1096 00:38:55,040 --> 00:38:57,040`
ändå? Absolut.



`1097 00:38:57,040 --> 00:38:59,040`
Men den håller ändå ett tag. Jaja, herregud.



`1098 00:38:59,040 --> 00:39:01,040`
Alltså det är, det är inget fel



`1099 00:39:01,040 --> 00:39:03,040`
på prestandan



`1100 00:39:03,040 --> 00:39:05,040`
och det är



`1101 00:39:05,040 --> 00:39:07,040`
det är till och med så att om man tittar på Husqvarnas



`1102 00:39:07,040 --> 00:39:09,040`
utbud så har de ju



`1103 00:39:09,040 --> 00:39:11,040`
röjsågar och



`1104 00:39:11,040 --> 00:39:13,040`
liksom proffsmotorsågar



`1105 00:39:13,040 --> 00:39:15,040`
som går på el så att



`1106 00:39:15,040 --> 00:39:17,040`
sen kanske man



`1107 00:39:17,040 --> 00:39:19,040`
ja, jag vet inte hur smidigt det är



`1108 00:39:19,040 --> 00:39:21,040`
att liksom ladda batteriet



`1109 00:39:21,040 --> 00:39:23,040`
i bilen liksom eller hur man nu gör.



`1110 00:39:23,040 --> 00:39:25,040`
Men



`1111 00:39:25,040 --> 00:39:27,040`
det är klart har du en elbil så kan ju det



`1112 00:39:27,040 --> 00:39:29,040`
funka om du har en inverter



`1113 00:39:29,040 --> 00:39:31,040`
i bilen och kan



`1114 00:39:31,040 --> 00:39:33,040`
ladda. Tänk hur det är alltså



`1115 00:39:33,040 --> 00:39:35,040`
utan att kunna den här branschen överhuvudtaget



`1116 00:39:35,040 --> 00:39:37,040`
så känns det som att man skulle ju kanske



`1117 00:39:37,040 --> 00:39:39,040`
vilja ha



`1118 00:39:39,040 --> 00:39:41,040`
alltså svappbara batteripacks



`1119 00:39:41,040 --> 00:39:43,040`
Ja men det är det.



`1120 00:39:43,040 --> 00:39:45,040`
Men du behöver ju ändå ha ett liksom



`1121 00:39:45,040 --> 00:39:47,040`
på laddning för att jag menar det är ju



`1122 00:39:47,040 --> 00:39:49,040`
med bensinmotorsågen så är det liksom bara



`1123 00:39:49,040 --> 00:39:51,040`
ja, fila kedjan



`1124 00:39:51,040 --> 00:39:53,040`
annars kan du ju bara räkna liksom



`1125 00:39:53,040 --> 00:39:55,040`
fylla på olja och sen kör man igen.



`1126 00:39:55,040 --> 00:39:57,040`
Hur många zombis ser du liksom?



`1127 00:39:57,040 --> 00:39:59,040`
Kommer batterikraften räcka innan?



`1128 00:39:59,040 --> 00:40:01,040`
Ja.



`1129 00:40:01,040 --> 00:40:03,040`
Ja.



`1130 00:40:03,040 --> 00:40:05,040`
Min elsåg är ju en Metabo



`1131 00:40:05,040 --> 00:40:07,040`
och den är jag väldigt glad i faktiskt.



`1132 00:40:07,040 --> 00:40:09,040`
Glad i?



`1133 00:40:09,040 --> 00:40:11,040`
Glad i. Ja, så är det.



`1134 00:40:11,040 --> 00:40:13,040`
Ja, nej men det är väl det



`1135 00:40:13,040 --> 00:40:15,040`
jag tänkte göra i sommar och



`1136 00:40:15,040 --> 00:40:17,040`
så lite utflykter



`1137 00:40:17,040 --> 00:40:19,040`
i skogen, kombinera



`1138 00:40:19,040 --> 00:40:21,040`
motion och bergsklättring



`1139 00:40:21,040 --> 00:40:23,040`
och klädklättring



`1140 00:40:23,040 --> 00:40:25,040`
med teknik.



`1141 00:40:25,040 --> 00:40:27,040`
Då gissar jag att planen är att bygga någon sån



`1142 00:40:27,040 --> 00:40:29,040`
repeater då som går på



`1143 00:40:29,040 --> 00:40:31,040`
sol och har någon slags lokal



`1144 00:40:31,040 --> 00:40:33,040`
batterilagen för att klara natten och så vidare.



`1145 00:40:33,040 --> 00:40:35,040`
Precis. Det behövs inte så mycket för att klara



`1146 00:40:35,040 --> 00:40:37,040`
en natt eller? Nej men



`1147 00:40:37,040 --> 00:40:39,040`
om den ska klara året runt



`1148 00:40:39,040 --> 00:40:41,040`
så är det svårare va?



`1149 00:40:41,040 --> 00:40:43,040`
Tappa både prestandan när det blir kallt och sen så



`1150 00:40:43,040 --> 00:40:45,040`
i februari, december, januari



`1151 00:40:45,040 --> 00:40:47,040`
är det fan inte mycket sol. Nej, precis.



`1152 00:40:47,040 --> 00:40:49,040`
Men man vill ha både och kanske.



`1153 00:40:49,040 --> 00:40:51,040`
Batterier och solceller.



`1154 00:40:51,040 --> 00:40:53,040`
Jag tänker i stugan kommer jag att PoE-mata den.



`1155 00:40:53,040 --> 00:40:55,040`
Aa, det går att göra.



`1156 00:40:55,040 --> 00:40:57,040`
Eller ja, det går inte men



`1157 00:40:57,040 --> 00:40:59,040`
jag har en PoE-converter som



`1158 00:40:59,040 --> 00:41:01,040`
en konverterar.



`1159 00:41:01,040 --> 00:41:03,040`
För det, jag ska byta



`1160 00:41:03,040 --> 00:41:05,040`
tak här också, det är kul.



`1161 00:41:05,040 --> 00:41:07,040`
Sådär. Dyt.



`1162 00:41:07,040 --> 00:41:09,040`
Ja, det är dyt.



`1163 00:41:09,040 --> 00:41:11,040`
Men det som är kul är att man får köpa



`1164 00:41:11,040 --> 00:41:13,040`
massa, om man har råd och visserligen,



`1165 00:41:13,040 --> 00:41:15,040`
men man får köpa solceller och massa jävla



`1166 00:41:15,040 --> 00:41:17,040`
ballteknik. Ja, det är kul. Och då är det nämligen så att



`1167 00:41:17,040 --> 00:41:19,040`
de som bodde i huset innan oss har ju haft



`1168 00:41:19,040 --> 00:41:21,040`
någon form av parabolfetisch.



`1169 00:41:21,040 --> 00:41:23,040`
Så att vi har liksom massa



`1170 00:41:23,040 --> 00:41:25,040`
stolpar i taket. Och de stolparna har jag



`1171 00:41:25,040 --> 00:41:27,040`
inte vågat röra för de går liksom genom



`1172 00:41:27,040 --> 00:41:29,040`
taket. Så det läcker inte så



`1173 00:41:29,040 --> 00:41:31,040`
de är kvar. Perfekt att sätta



`1174 00:41:31,040 --> 00:41:33,040`
antenner på. Exakt.



`1175 00:41:33,040 --> 00:41:35,040`
Och de är ju såhär motorstyrda så man kan liksom



`1176 00:41:35,040 --> 00:41:37,040`
de har haft sådana här. Och de har haft



`1177 00:41:37,040 --> 00:41:39,040`
motorstyrda satelliter.



`1178 00:41:39,040 --> 00:41:41,040`
Eller, det vet jag inte, men motorstyrda



`1179 00:41:41,040 --> 00:41:43,040`
parabolantennar. Ja. Jag vet inte om det funkar.



`1180 00:41:43,040 --> 00:41:45,040`
Jag har klippt alla de sladdarna. Men det är ju coolt.



`1181 00:41:45,040 --> 00:41:47,040`
Det är supercoolt. Du kan ju tweaka där.



`1182 00:41:47,040 --> 00:41:49,040`
Nej, då hade jag tänkt att där skulle jag sätta upp



`1183 00:41:49,040 --> 00:41:51,040`
en jättestor antenn



`1184 00:41:51,040 --> 00:41:53,040`
för att störa ut grannarna så de byter frekvens



`1185 00:41:53,040 --> 00:41:55,040`
givetvis. På mitt wifi.



`1186 00:41:55,040 --> 00:41:57,040`
För jag vill ha min egen rymd.



`1187 00:41:57,040 --> 00:41:59,040`
Mina kanaler är mina.



`1188 00:41:59,040 --> 00:42:01,040`
Det funkar svinbra ändå.



`1189 00:42:01,040 --> 00:42:03,040`
Men kanske man inte ska säga,



`1190 00:42:03,040 --> 00:42:05,040`
får man göra så? Det får man.



`1191 00:42:05,040 --> 00:42:07,040`
Men luften är fri. Det sa du till mig en gång.



`1192 00:42:07,040 --> 00:42:09,040`
Så luften är fri.



`1193 00:42:09,040 --> 00:42:11,040`
Det är en tanke. Det är inte så neighborly.



`1194 00:42:11,040 --> 00:42:13,040`
Nej, men vad fan, jag är inte så neighborly.



`1195 00:42:13,040 --> 00:42:15,040`
På tal om det.



`1196 00:42:15,040 --> 00:42:17,040`
Vet ni vad som går att ha



`1197 00:42:17,040 --> 00:42:19,040`
i sitt SSID-namn?



`1198 00:42:19,040 --> 00:42:21,040`
Nej.



`1199 00:42:21,040 --> 00:42:23,040`
Emojis.



`1200 00:42:23,040 --> 00:42:25,040`
De renderar också.



`1201 00:42:25,040 --> 00:42:27,040`
Det är coolt.



`1202 00:42:27,040 --> 00:42:29,040`
Undrar om alla gamla klienter klarar det på ett bra sätt.



`1203 00:42:29,040 --> 00:42:31,040`
Nej, det tror jag inte. Jag har en



`1204 00:42:31,040 --> 00:42:33,040`
dödskalle som går 1, 2, 3, 4,



`1205 00:42:33,040 --> 00:42:35,040`
5, 6, 7, 8, 9.



`1206 00:42:35,040 --> 00:42:37,040`
1, 2, 3, 4. Som broadcastar hela tiden.



`1207 00:42:37,040 --> 00:42:39,040`
Vadå, du ändrar SSID?



`1208 00:42:39,040 --> 00:42:41,040`
Ja.



`1209 00:42:41,040 --> 00:42:43,040`
Jag använder ju inte det. Det är bara det att det är



`1210 00:42:43,040 --> 00:42:45,040`
ball. Så när man går upp och söker



`1211 00:42:45,040 --> 00:42:47,040`
på sida så blir det såhär



`1212 00:42:47,040 --> 00:42:49,040`
Du har en anvenderad SSID.



`1213 00:42:49,040 --> 00:42:51,040`
Jag använder inte det. Det är bara för att det är kul.



`1214 00:42:51,040 --> 00:42:53,040`
Så då kan man titta såhär. Om du tar på



`1215 00:42:53,040 --> 00:42:55,040`
max Browse SSID



`1216 00:42:55,040 --> 00:42:57,040`
så kommer det komma upp en emoji



`1217 00:42:57,040 --> 00:42:59,040`
av en dödskalle som är 1, 2, 3, 4, 5.



`1218 00:42:59,040 --> 00:43:01,040`
1, 2, 3, 4, 5.



`1219 00:43:01,040 --> 00:43:03,040`
Det är väldigt roligt.



`1220 00:43:03,040 --> 00:43:05,040`
Är det inte det? Jo.



`1221 00:43:05,040 --> 00:43:07,040`
Det är en liten paj som gör det där.



`1222 00:43:07,040 --> 00:43:09,040`
Så det är ingen direkt uteffekt. Men



`1223 00:43:09,040 --> 00:43:11,040`
ändå ball. Ja.



`1224 00:43:11,040 --> 00:43:13,040`
Jag har en bokstavskombination.



`1225 00:43:13,040 --> 00:43:15,040`
Ni har ju det. Men det är kul.



`1226 00:43:15,040 --> 00:43:17,040`
Men



`1227 00:43:17,040 --> 00:43:19,040`
där skulle man ju kunna sätta en sån



`1228 00:43:19,040 --> 00:43:21,040`
liten grej. Poematning



`1229 00:43:21,040 --> 00:43:23,040`
är ju kanon. För det finns ju i närheten



`1230 00:43:23,040 --> 00:43:25,040`
tänker jag. Ja. Och det behöver ju



`1231 00:43:25,040 --> 00:43:27,040`
inte vara för att du behöver



`1232 00:43:27,040 --> 00:43:29,040`
E-ternet upp dit. Utan du kan ju bara plocka ut



`1233 00:43:29,040 --> 00:43:31,040`
strömmen. Hur mycket drar en sån



`1234 00:43:31,040 --> 00:43:33,040`
rackare då? Ingenting.



`1235 00:43:33,040 --> 00:43:35,040`
Typ 5 volt



`1236 00:43:35,040 --> 00:43:37,040`
30 till



`1237 00:43:37,040 --> 00:43:39,040`
50 milliampere. Du kan



`1238 00:43:39,040 --> 00:43:41,040`
komma ner i närmare 10



`1239 00:43:41,040 --> 00:43:43,040`
om du stänger av alla. Då kommer man inte till



`1240 00:43:43,040 --> 00:43:45,040`
Göteborg. Nej.



`1241 00:43:45,040 --> 00:43:47,040`
Det är det som är mäktigt med LoRa.



`1242 00:43:47,040 --> 00:43:49,040`
Du får fetingräckvidd ändå.



`1243 00:43:49,040 --> 00:43:51,040`
Okej. Det är ju samma sak



`1244 00:43:51,040 --> 00:43:53,040`
som sagt radioamatörer kan ju



`1245 00:43:53,040 --> 00:43:55,040`
säga



`1246 00:43:55,040 --> 00:43:57,040`
sub



`1247 00:43:57,040 --> 00:43:59,040`
är det milliwatt



`1248 00:43:59,040 --> 00:44:01,040`
till och med? Nej subwatt tror jag det är.



`1249 00:44:01,040 --> 00:44:03,040`
Ja. På en watt



`1250 00:44:03,040 --> 00:44:05,040`
så kan du komma jorden runt. Ja det är coolt.



`1251 00:44:05,040 --> 00:44:07,040`
Och då kör du såna



`1252 00:44:07,040 --> 00:44:09,040`
digitala moder



`1253 00:44:09,040 --> 00:44:11,040`
som då är extremt lågbandbredd.



`1254 00:44:11,040 --> 00:44:13,040`
De ligger under



`1255 00:44:13,040 --> 00:44:15,040`
noise floor liksom. Ja det är inte något man



`1256 00:44:15,040 --> 00:44:17,040`
flyttar ett par terabyte med. Nej herregud nej.



`1257 00:44:17,040 --> 00:44:19,040`
Det är inte, du streamar inte tv med den.



`1258 00:44:19,040 --> 00:44:21,040`
Nej. Men man kan skicka hej.



`1259 00:44:21,040 --> 00:44:23,040`
Ja precis. Ja coolt.



`1260 00:44:23,040 --> 00:44:25,040`
Nu blir jag jättetaggad på att köpa



`1261 00:44:25,040 --> 00:44:27,040`
LoRa grejer. Ja det



`1262 00:44:27,040 --> 00:44:29,040`
tycker jag ni ska göra. Vet fortfarande inte vad jag ska ha det till.



`1263 00:44:29,040 --> 00:44:31,040`
Men det ser coolt ut. Alltså jag



`1264 00:44:31,040 --> 00:44:33,040`
har ingen aning om vad jag ska ha det till. Det gör



`1265 00:44:33,040 --> 00:44:35,040`
jag och vill bara ha det. Ja.



`1266 00:44:35,040 --> 00:44:37,040`
Alltså 150%



`1267 00:44:37,040 --> 00:44:39,040`
igenkänning. Jag menar titta på den.



`1268 00:44:39,040 --> 00:44:41,040`
Ja och det är jätteroligt



`1269 00:44:41,040 --> 00:44:43,040`
att räkna på strömförbrukning



`1270 00:44:43,040 --> 00:44:45,040`
och batteristorlek



`1271 00:44:45,040 --> 00:44:47,040`
och behöver jag värma upp



`1272 00:44:47,040 --> 00:44:49,040`
batterierna. Nu hittade Thomas någon



`1273 00:44:49,040 --> 00:44:51,040`
kanadensisk sajt som tyckte att BFspa



`1274 00:44:51,040 --> 00:44:53,040`
kör. Men i Kanada kan man



`1275 00:44:53,040 --> 00:44:55,040`
lita på ändå. De tappar ju prestanda men liksom.



`1276 00:44:55,040 --> 00:44:57,040`
Jo men de hade kört



`1277 00:44:57,040 --> 00:44:59,040`
vinterförhållanden



`1278 00:44:59,040 --> 00:45:01,040`
uppe i Kanada med minus 40



`1279 00:45:01,040 --> 00:45:03,040`
grader Celsius och de



`1280 00:45:03,040 --> 00:45:05,040`
hade väl märkt en 10-20%



`1281 00:45:05,040 --> 00:45:07,040`
förlust på



`1282 00:45:07,040 --> 00:45:09,040`
batterikapaciteten liksom. Det låter för bra



`1283 00:45:09,040 --> 00:45:11,040`
för att vara sant också. Nej för grejen är



`1284 00:45:11,040 --> 00:45:13,040`
att när solen ligger på det är då



`1285 00:45:13,040 --> 00:45:15,040`
och sen så är det ju så små strömmar och det är inte farligt



`1286 00:45:15,040 --> 00:45:17,040`
att ladda ett litiumbatteri även om det är



`1287 00:45:17,040 --> 00:45:19,040`
små. Alltså så länge



`1288 00:45:19,040 --> 00:45:21,040`
det är små strömmar det är ju det här du ska inte trycka på



`1289 00:45:21,040 --> 00:45:23,040`
med full



`1290 00:45:23,040 --> 00:45:25,040`
spätta liksom.



`1291 00:45:25,040 --> 00:45:27,040`
Och



`1292 00:45:27,040 --> 00:45:29,040`
ja så det verkar funka.



`1293 00:45:31,040 --> 00:45:33,040`
Sen är det ju här i



`1294 00:45:33,040 --> 00:45:35,040`
Göteborg och



`1295 00:45:35,040 --> 00:45:37,040`
gråa Sverige så är ju



`1296 00:45:37,040 --> 00:45:39,040`
soltillgången lite sisådär på



`1297 00:45:39,040 --> 00:45:41,040`
vintern så att det är väl det som är utmaningen.



`1298 00:45:41,040 --> 00:45:43,040`
Ja som sagt det ser ju jag på mina



`1299 00:45:43,040 --> 00:45:45,040`
solceller. December och januari



`1300 00:45:45,040 --> 00:45:47,040`
då är det liksom zero.



`1301 00:45:47,040 --> 00:45:49,040`
Ja men



`1302 00:45:49,040 --> 00:45:51,040`
alltså PoE är ju klockrent.



`1303 00:45:51,040 --> 00:45:53,040`
Om det funkar så är det ju



`1304 00:45:53,040 --> 00:45:55,040`
då är det ju bra.



`1305 00:45:55,040 --> 00:45:57,040`
Ja då behöver man inte fundera på



`1306 00:45:57,040 --> 00:45:59,040`
uteffekt och välsen whistles.



`1307 00:45:59,040 --> 00:46:01,040`
Helst bara att den inte suger i sig



`1308 00:46:01,040 --> 00:46:03,040`
mer än vad den ska ha så att den dör.



`1309 00:46:03,040 --> 00:46:05,040`
Ja jo.



`1310 00:46:05,040 --> 00:46:07,040`
Men det tänker jag.



`1311 00:46:07,040 --> 00:46:09,040`
Om du då är lat och smackar in den i din switch bara



`1312 00:46:09,040 --> 00:46:11,040`
så får du notera att då har du en



`1313 00:46:11,040 --> 00:46:13,040`
attackvektor via taket.



`1314 00:46:13,040 --> 00:46:15,040`
Ja alltså alla har väl, nu vill jag bara



`1315 00:46:15,040 --> 00:46:17,040`
slå det här då. Alla har väl



`1316 00:46:17,040 --> 00:46:19,040`
ett eget separat vindnät.



`1317 00:46:19,040 --> 00:46:21,040`
Det har jag. Såklart.



`1318 00:46:21,040 --> 00:46:23,040`
Jag har alltså två PoE switchar på två takstolar



`1319 00:46:23,040 --> 00:46:25,040`
på vinden som bara är kopplade



`1320 00:46:25,040 --> 00:46:27,040`
på en port där alla kameror bor.



`1321 00:46:27,040 --> 00:46:29,040`
Och då kanske låra ström.



`1322 00:46:29,040 --> 00:46:31,040`
Det har väl alla?



`1323 00:46:31,040 --> 00:46:33,040`
Inte än. Nej. Men jag håller ju på med det när vi har



`1324 00:46:33,040 --> 00:46:35,040`
den nu så det kanske är dags då.



`1325 00:46:35,040 --> 00:46:37,040`
Det har ju spårat ur.



`1326 00:46:37,040 --> 00:46:39,040`
Det är alltså 10 gigabit hel switchat i hela huset nu.



`1327 00:46:39,040 --> 00:46:41,040`
Det är ju fan inte billigt alltså.



`1328 00:46:41,040 --> 00:46:43,040`
Nej.



`1329 00:46:43,040 --> 00:46:45,040`
Jag uppgraderade internet innan jag räknade på



`1330 00:46:45,040 --> 00:46:47,040`
vad alla switchar skulle kosta. Det var ju inte roligt alltså.



`1331 00:46:47,040 --> 00:46:49,040`
Men du måste ju inte ha samma kapacitet



`1332 00:46:49,040 --> 00:46:51,040`
i hela huset.



`1333 00:46:51,040 --> 00:46:53,040`
Vänta nu. Va? Du måste inte.



`1334 00:46:53,040 --> 00:46:55,040`
Du kan men du måste inte.



`1335 00:46:55,040 --> 00:46:57,040`
Nej det är sant. Men



`1336 00:46:57,040 --> 00:46:59,040`
accesslagret till mitt dataskåp



`1337 00:46:59,040 --> 00:47:01,040`
var ju tvungen att vara 10 gigabit. Det har du med om.



`1338 00:47:01,040 --> 00:47:03,040`
Sen så kan man ju



`1339 00:47:03,040 --> 00:47:05,040`
följfrågan är har du någonting där som kan prata 10 gigabit?



`1340 00:47:05,040 --> 00:47:07,040`
Nu har jag det.



`1341 00:47:07,040 --> 00:47:09,040`
Det hade jag inte.



`1342 00:47:09,040 --> 00:47:11,040`
Men kopierar man diskar vill man ju ofta ha 10 gigabit.



`1343 00:47:11,040 --> 00:47:13,040`
Exakt. Alltså ljuscasen är enormt



`1344 00:47:13,040 --> 00:47:15,040`
mycket.



`1345 00:47:15,040 --> 00:47:17,040`
Kopiera diskar det gör jag fan



`1346 00:47:17,040 --> 00:47:19,040`
flera dagar i veckan. För att man vill ha det.



`1347 00:47:19,040 --> 00:47:21,040`
Det är en god anledning.



`1348 00:47:21,040 --> 00:47:23,040`
Bara så.



`1349 00:47:23,040 --> 00:47:25,040`
Så tänk hur snabbt det går när ni surfar in



`1350 00:47:25,040 --> 00:47:27,040`
på säkerhetspodcasten.se



`1351 00:47:27,040 --> 00:47:29,040`
Kom.



`1352 00:47:29,040 --> 00:47:31,040`
SE. SE.



`1353 00:47:31,040 --> 00:47:33,040`
Det tänkte jag på just det här



`1354 00:47:33,040 --> 00:47:35,040`
AliExpress som du sa.



`1355 00:47:35,040 --> 00:47:37,040`
Köp hem nya roliga saker.



`1356 00:47:37,040 --> 00:47:39,040`
Jag har också köpt hem roliga saker fast i ett helt annat skrå.



`1357 00:47:39,040 --> 00:47:41,040`
Alltså på riktigt.



`1358 00:47:41,040 --> 00:47:43,040`
Köpt hem mobila



`1359 00:47:43,040 --> 00:47:45,040`
handbollsmål och



`1360 00:47:45,040 --> 00:47:47,040`
bollfångarnät.



`1361 00:47:47,040 --> 00:47:49,040`
Har jag klickat hem bara så sent som igår.



`1362 00:47:49,040 --> 00:47:51,040`
Bollfångar. Alltså man sätter



`1363 00:47:51,040 --> 00:47:53,040`
bakom målet. Ja precis.



`1364 00:47:53,040 --> 00:47:55,040`
Så att min son han vill göra



`1365 00:47:55,040 --> 00:47:57,040`
lite dedikerad handbollsträning under sommaren



`1366 00:47:57,040 --> 00:47:59,040`
och det vill jag ju som god far enabla.



`1367 00:47:59,040 --> 00:48:01,040`
Så att då klickar vi hem ett



`1368 00:48:01,040 --> 00:48:03,040`
ett portabelt handbollsmål



`1369 00:48:03,040 --> 00:48:05,040`
och så inser jag att det finns rutor på huset.



`1370 00:48:05,040 --> 00:48:07,040`
Så då köpte vi något



`1371 00:48:07,040 --> 00:48:09,040`
bollfångarnät



`1372 00:48:09,040 --> 00:48:11,040`
som vi ska montera där för att skydda rutorna.



`1373 00:48:11,040 --> 00:48:13,040`
När han missar.



`1374 00:48:13,040 --> 00:48:15,040`
Eftersom man ska ju sikta



`1375 00:48:15,040 --> 00:48:17,040`
nära stolpen liksom så då måste man ju missa någon gång.



`1376 00:48:17,040 --> 00:48:19,040`
Ja låter rimligt.



`1377 00:48:19,040 --> 00:48:21,040`
Låter som ett bra sommarprojekt.



`1378 00:48:21,040 --> 00:48:23,040`
Och jag tänker med det så tror jag



`1379 00:48:23,040 --> 00:48:25,040`
vi rundar av.



`1380 00:48:25,040 --> 00:48:27,040`
Och önskar alla



`1381 00:48:27,040 --> 00:48:29,040`
lyssnare en fantastisk



`1382 00:48:29,040 --> 00:48:31,040`
sommar och jag hoppas att ni också hittar på



`1383 00:48:31,040 --> 00:48:33,040`
en massa spännande



`1384 00:48:33,040 --> 00:48:35,040`
elektronik eller säkerhetsprojekt



`1385 00:48:35,040 --> 00:48:37,040`
eller kodarprojekt eller



`1386 00:48:37,040 --> 00:48:39,040`
bollprojekt.



`1387 00:48:39,040 --> 00:48:41,040`
Det viktiga är att ni laddar batterierna



`1388 00:48:41,040 --> 00:48:43,040`
inför hösten och



`1389 00:48:43,040 --> 00:48:45,040`
laddar igång



`1390 00:48:45,040 --> 00:48:47,040`
för en spännande



`1391 00:48:47,040 --> 00:48:49,040`
fortsättning på



`1392 00:48:49,040 --> 00:48:51,040`
våra galna



`1393 00:48:51,040 --> 00:48:53,040`
uppgångar.



`1394 00:48:53,040 --> 00:48:55,040`
Jag som pratade i dag



`1395 00:48:55,040 --> 00:48:57,040`
hette Richard Godfors och med



`1396 00:48:57,040 --> 00:48:59,040`
mig hade jag Peter Magnusson.



`1397 00:48:59,040 --> 00:49:01,040`
Det står till face i din



`1398 00:49:01,040 --> 00:49:03,040`
julegulta vän.



`1399 00:49:03,040 --> 00:49:05,040`
Jesper Larsson.



`1400 00:49:05,040 --> 00:49:07,040`
Han säger så mycket konstiga grejer men det stämmer.



`1401 00:49:07,040 --> 00:49:09,040`
Och Mattias Idhaga.



`1402 00:49:09,040 --> 00:49:11,040`
Ja.


