# Pågående arbete

Skriv upp din uppgift här innan du börjar, så att ni inte jobbar på samma sak. Format: `- Uppgift – namn`.

## Pågår
- Ny ikon (tre överlappande cirklar) till Play och appikonerna i app/icons/ – Cajsa

## Frågor till den andra
- Till Cajsa från Rickard (2026-10-11): Färgfältet i färgtesterna. Rickard ser en kant som ett upp-och-nervänt U runt gult, grönt och turkos, och tycker att fältet skär i ögonen. Det har ändrats tre gånger i dag: mjukare övergångar mellan nyanserna, och den rena färgen ligger högre för ljusa nyanser och lägre för mörka (se CHANGELOG 2026-10-11). Han ser fortfarande kanten. Mättnaden ska inte sänkas. Hur upplever du fältet, ser du kanten, och har du förslag? Svara här eller i CHANGELOG. Svar från Cajsa (2026-10-11): färgfältet är ersatt av ett färghjul, se CHANGELOG och BESLUT. Fält är nu borttagen; HSV, Lab och En i taget ligger kvar tills ni jämfört.
- Till Cajsa från Rickard (2026-10-11): Ny funktion att pröva, "Din text i dina färger" längst ner i Min profil. Man skriver text och ser den i sina egna färger för siffror och bokstäver. Den öppnas först när uppföljningen för siffror eller bokstäver är gjord, eftersom man annars kan lägga färgerna på minnet och få bättre konsistens än man har. Rickard var orolig för just det men tror att det kan vara givande för synestetiker. Du avgör om den ska vara kvar: stäng av med CTEXT_ON = false i app/index.html.
- Till Cajsa från Rickard (2026-10-11): Fyra färgväljare att jämföra i färgtesterna, valet görs med knapparna Hjul / Fält / HSV / Lab under färgväljaren. Hjul = ditt färghjul, som är standard. Fält = Rickards färgfält (HSL med mjukade övergångar). HSV = nyansremsa och en ruta för mättnad och ljushet, som på selecolor.com. (Jämn, en OKLCH-skala, är borttagen igen: Rickard tyckte inte att den blev bra.) Lab = de optimala färgerna (MacAdam) som punktmoln i CIELAB sett ovanifrån, med ett reglage för ljushet. Alla sparar svaret som RGB och poängsätts likadant. Du väljer vilken som blir kvar; knapparna stängs av med PICKER_TOGGLE = false.
- Till Cajsa från Rickard (2026-10-12): Testläget. Provknapparna för färgväljaren (HSV, Lab, En i taget), "Hoppa fram 7 dagar" och piltangenterna syns nu bara i testläget, så att vanliga testare bara ser färghjulet. Så kommer du in: tryck fem gånger snabbt på loggan på startsidan (inom två sekunder). Samma sak stänger av. Det fungerar också i claude.ai-artefakten. När appen ligger på en egen adress går det även att lägga till `?dev` sist i adressen. Valet sparas i webbläsaren. Självtestet av poängsättningen nås med `?test` sist i adressen.
- Till Cajsa från Rickard (2026-10-14): Repot har flyttat. SynMap ligger nu i GitHub-organisationen SynTraceApp: https://github.com/SynTraceApp/SynMap (Rickard är ägare, du har Write). Gör så här: (1) I ditt Claude-projekt, byt repot i projektinställningarna från rickardlundgren91/SynMap till SynTraceApp/SynMap, så hittar nya trådar det. (2) Om du har en egen kopia av repot: `git remote set-url origin https://github.com/SynTraceApp/SynMap.git` (den gamla adressen skickas vidare ett tag, men byt ändå). Appen ligger på https://syntraceapp.github.io/SynMap/app/, kortlänken är https://syntraceapp.github.io och integritetspolicyn https://syntraceapp.github.io/SynMap/app/integritet.html. Repot SynTraceApp/syntraceapp.github.io är webbplatsens rot; där ska `.well-known/assetlinks.json` in när du har fingeravtrycket (SHA-256) för appens signeringsnyckel från Play Console. Använd adressen ovan när du bygger Android-paketet.
- Till Cajsa från Rickard (2026-10-14): Repot har nu döpts om till **SynTraceApp/SynTrace**, som du bad om. Byt repo i ditt Claude-projekt en gång till (till SynTraceApp/SynTrace) och starta nya trådar. Egen kopia: `git remote set-url origin https://github.com/SynTraceApp/SynTrace.git`. Appen ligger nu på https://syntraceapp.github.io/SynTrace/app/ och integritetspolicyn på https://syntraceapp.github.io/SynTrace/app/integritet.html. Använd de adresserna när du bygger Android-paketet.
- Till Rickard från Cajsa (2026-10-16): Porträtten av levande personer (PIMG, tolv bilder) ligger kvar i den publika historiken, trots att jag har tagit bort dem ur `app/index.html` (se CHANGELOG 2026-10-16). Vi vill ta bort dem helt, och jag får inte skriva om historiken på `main`. Vad tycker du? (1) Du skriver om historiken med `git filter-repo` (tar bort bilddata ur alla commits) och tvingar upp den, och ber GitHub Support rensa cachade commits. Då måste alla klona om. (2) Vi startar ett nytt, rent repo utan den gamla historiken. Då tappar vi commit-historiken och måste byta adress överallt, även i Play. Svara här eller i CHANGELOG. Jag väntar med att pusha mer tills vi har bestämt oss. Tills vidare gäller också: licens för repot är inte vald, vilket behövs innan vi skriver "öppen källkod" i appen eller i Play.

## Klart
- Ikon till Google Play (512 × 512) i app/icons/ – Cajsa (2026-10-15)
- Installerbar app (PWA) via GitHub Pages: manifest, ikoner, service worker och integritetspolicy i app/ – Rickard
- Kända personer med synestesi som lista med silhuettikoner i stället för porträtt i app/index.html – Cajsa (2026-10-14)
- Ingen upplevelse går vidare till nästa fråga direkt i alla tester, i app/index.html – Cajsa (2026-10-13)
- Om synestesi samlad på en sida (Mer om synestesi borttagen), med Kända personer med synestesi och ny text i app/index.html – Cajsa
- Tio förbättringar från förslagspaketet (uppföljning vid midnatt, testläge, korsvis uppföljning, Personlighet-spärr, jämförelsen, snabbare färghjul, Måttligt stöd, självtest, långa mejl, små rättelser) i app/index.html – Rickard
- Knappen Dela dina svar med oss (mejl med samtycke) i app/index.html – Rickard
- Föregående och Nästa ovanför färgväljaren i app/index.html – Cajsa
- Skript för Google-formulär till testanvändare i docs/SynMap-formular.gs – Cajsa
- Bakåtpilen från profil och resultat till testlistan, och ny länk under Läs mer om synestesi i app/index.html – Cajsa
- Mjukare färgring och Fält-väljaren borttagen i app/index.html – Cajsa
- Svart kontur runt tecknen i färgtesterna i app/index.html – Cajsa
- Plana tecken utan kontur i färgtesterna i app/index.html – Cajsa
- Rund färgväljare (färghjul) i stället för färgfältet i färgtesterna i app/index.html – Cajsa
- Följdfrågor, sortering i Välj test, dold poängsättning, länkrad, piltangenter, Tid i rummet-figur, uppföljningsskärm, pausat test-rutan, profilringar, färgneutral version, färgfältet och Din text i dina färger i app/index.html – Rickard
- Föregående på första inledande frågan går tillbaka till Om dig i app/index.html – Rickard
- Överlappande cirklar överst i Din synestesiprofil i app/index.html – Cajsa
- Menyn utan Om dig, Kopierad-etikett och länkradens plats på Inledande frågor i app/index.html – Cajsa
- Snabbtest som väntar på svar, färgrektangel i ljudtestet och kopierbar kontaktadress i app/index.html – Cajsa
- Börja-knappens plats på startsidan återställd – Cajsa
- Pseudonymer i upphovsraderna i app/index.html – Cajsa
- Dämpad orange för Pausat/Påbörjad, spanska profiltexter och Kopiera adress i app/index.html – Cajsa
- Länkrad, ikonrad och kontaktadress i app/index.html – Cajsa
- Cajsas senaste appändringar i app/index.html (Om dig först, uppföljning för alla tester, Så fungerar SynMap, upphovsrader, Dela med en forskare borttaget) – Cajsa
- Ord → smak ombyggt efter MULTISENSE – Cajsa
- Personifiering och Ord → smak, Börja-knapp, ny ordning i Om appen – Cajsa
- Startskärm, alla tester i Välj test, Så funkar SynMap – Cajsa
- Projektor–associator-enkät och spegelberöringstest – Rickard
- Dela med forskare via studiekod i stället för e-post – Rickard
- Bakgrundsfrågor, färgseende, helhetsbedömning, förklaringssida, fortsätt där du var, tid/paus och engelska – Rickard
- Lägga in prototyp, underlag och samarbetsregler – Rickard
- Frågan ovanför tecknet, namnbyte till Synesthesium, riktiga namn i upphovsraderna och ny kontaktrad – Cajsa (2026-10-12)
- Namnbyte till SynTrace – Cajsa (2026-10-12)
- Högkontrast i den färgneutrala versionen – Cajsa (2026-10-12)
- Knappen för färgneutral version i gråskala, knappen för färg i färg – Cajsa (2026-10-12)
- Självskattningen under Fler tester med eget resultat i Min profil, påminnelser om uppföljning – Cajsa (2026-10-12)
- Ny mejladress syntrace_2026@proton.me – Cajsa (2026-10-12)
- Självskattningens etikett, kortare texter och jämförelse mot testerna – Cajsa (2026-10-12)
