# 4) E-Collecting User Journey mit Nutzung der Erfahrung von SwissSign, ePost und E-Voting

*Over the course of two days, we developed our solution for collecting electronic signatures for popular initiatives and referendums from A to Z, addressing the 10 topics outlined in the [guidelines](https://www.bk.admin.ch/bk/de/home/politische-rechte/e-collecting/aktuelles.html). Your prototype is conceptual. We clearly present the interactions and data flows between actors, software, and infrastructure components over time, as well as the user experience of these actors.*

---

# Projektdokumentation – Hackathon Team 4  

## Team Members
Amina Bouzar, Jörg Scchorr, Marcel Eichmüller, Roman Riesen, Leonardo Moretti, Lukas Erni, Audhild Høgåsen, Florian Moser

## Inhaltsverzeichnis
1. [Ausgangslage](#ausgangslage)
2. [Herangehensweise](#herangehensweise)
   - [Phase 0](#phase-0)
   - [Phase 1](#phase-1)
   - [Phase 2](#phase-2)
   - [Phase 3](#phase-3)
   - [Phase 4](#phase-4)
   - [Phase 5](#phase-5)
   - [Phase 6](#phase-6)
3. [Fazit](#fazit)

---

## Ausgangslage
Die Schweizerische Post versteht sich seit jeher eine der Vertrauensinfrastruktur der Schweiz. 

Wo früher Briefe, Zahlungen oder amtliche Dokumente physisch zugestellt wurden, übernehmen heute digitale Dienste wie  

- SwissSign, - stellt digitale Zertifikate und Signaturen bereit 
- ePost – ist der digitale Briefkasten der Schweiz oder  
- E-Voting – elektronische Stimmabgebe  

 diese Rolle.  

E-Collecting kann nur funktionieren, wenn Bürgerinnen und Bürger Vertrauen in den Prozess haben. Die Post bringt dieses Vertrauen mit – durch, ihren gesetzlichen Auftrag, als Bundesnahesunternehmen und ihre Erfahrung im sicheren Informationsaustausch. Wir betrachten den gesamten Prozess – von der digitalen Unterstützungsbeurkundung bis zur Auszählung der Unterstützungsbekundungen: 

- Elektronisches Unterstützungsbeurkundung 
- Elektronisches Sammeln 
- Elektronische Prüfung
- Elektronisches Zählen 

Dabei liegt unser Fokus auf einer einfachen, nachvollziehbaren und barrierefreien User Journey für alle Beteiligten – Bürgerinnen, Komitees, Gemeinden & Kantone und die Bundeskanzlei. Vorschlag: E-Collecting in der Schweiz sollte sicher, transparent und für alle zugänglich sein. Im Rahmen dieses Hackathons wollen wir mit euch gemeinsam herausfinden: 

- Wie könnte eine E-Collecting-Customer-Journey aussehen, die sicher und nutzerfreundlich ist, und die das Vertrauen der Bevölkerung gewinnt? 
- Wie können wir eine praktikable Lösung finden, die Teilnahmegeheimnis und Verifizierbarkeit gewährleistet? Können wir die Erfahrungen der Post aus Projekten wie SwissSign, E-Voting und ePost nutzen, um eine solche Lösung zu finden?

---

## Herangehensweise

### Phase 0
In einem ersten Schritt haben wir prüfen wollen, wie weit ein Stimmgeheimnis im Bereich E-Collecting eingeführt werden könnte. Dafür haben wir die bereits erarbeiteten Ideen und Gedanken aus dem Paper von Florian und Audhild angeschaut (Verlinkung Paper + Verlinkung Bild). Dabei sind wir zum Schluss gekommen, dass ein Stimmgeheimnis auf Stufe 4 machbar wäre, jedoch die aktuelle Ausgangslage bei den Gemeinden und den Softwareanbietern es nicht ermöglicht, die Idee umzusetzen.

---

### Phase 1
Aufgrund des Inputs der Gemeinde haben wir verstanden, wie ein Stimmregister entsteht und auf Basis welcher Daten, nämlich der Einwohnerdienste, es erstellt wird. Diese Hoheit der Daten obliegt den Gemeinden und sollte bei den Gemeinden bleiben. Ebenfalls hat uns die Gemeinde Einblick gegeben in den Prozess einer Unterschriftenprüfung und das Bedürfnis geäußert, dass es für sie einfacher wäre, wenn alle Daten aus einer zentralen Stelle kommen, bereits digital, und diese nur noch geprüft werden müssen. Somit sind wir auf die Idee gekommen, dass es eine zentrale E-Collecting-Plattform braucht, welche die Unterstützungsbeurkundungen digital sammelt und der Gemeinde zur Verfügung stellt.

---

### Phase 2
Was passiert noch auf dieser Plattform? Die Komitees, die Gemeinde & der Kanton, der Bürger und die BK sind Akteure, welche auf diese Plattform zugreifen müssen. Das Komitee muss die Initiative einreichen können und so einen Workflow auslösen, welcher die BK auffordert zu prüfen und freizugeben. Die freigegebene Initiative ist nun aufgeschaltet. Dank eines Links, eines QR-Codes auf der Straße oder durch Weiterleiten des PDFs kann die Initiative verbreitet werden. Der Bürger kann dann:

- entweder über die Plattform das Formular in seinen digitalen Briefkasten der Post (ePost App) zustellen lassen und dort unterschreiben  
- oder über den QR-Code das Formular in seine ePost App zustellen lassen  
- oder das erhaltene PDF in die ePost App hochladen  

Anschließend wird die digitale Unterstützungsbeurkundung digital an die Gemeinde gesendet. Falls die Gemeinde an die ePost angeschlossen ist, in den digitalen Briefkasten der Gemeinde oder via Schnittstelle ins entsprechende System. Die Gemeinde prüft die Unterstützungsbeurkundung auf Stimmrecht und Wohnsitz und gibt diese dann frei. Die Freigabe löst zwei weitere Workflows/Prozesse aus:

1. Die Unterstützungsbeurkundung wird per Sedex zurück an die zentrale E-Collecting-Plattform gesendet und gezählt  
2. Der Bürger erhält eine Bestätigung in seinen digitalen Briefkasten, dass die Unterstützungsbeurkundung gültig angekommen ist  

Das zentrale Zurücksenden der Unterstützungsbeurkundung in die Plattform hilft einerseits den Komitees, den aktuellen Stand zu sehen, aber auch anschließend der BK, einen Überblick und eine Überprüfung vornehmen zu können.

---

### Phase 3
Was passiert mit den noch physisch abgegebenen Unterstützungsbeurkundungen? Hier sehen wir die Schweizerische Post als zentrale Infrastruktur, die mit der E-Collecting-Plattform interagieren kann. Die Post könnte diese sammeln bzw. an eine zentrale Stelle zugeschickt bekommen und digitalisieren. Die digitalisierten Unterstützungsbeurkundungen werden in der Plattform eingegeben oder automatisch mit dem Scan erfasst und so direkt der Gemeinde übermittelt.

---

### Phase 4
Was definieren wir als Unterstützungsbeurkundung? Wir können mit einer digitalen Unterschrift wie mit SwissSign eine gewisse Sicherheitsstufe erreichen, sind aber unentschlossen gewesen, ob ein Modell wie St. Gallen vorzuziehen ist. Je nachdem, welche Sicherheitsstufe erwartet wird, würde der Lösungsansatz angepasst werden.

---

### Phase 5
Um einen weiteren «Unterschriftenbeschiss» zu verhindern, finden wir es essenziell, dass der Bürger, welcher eine Unterstützungsbeurkundung abgegeben hat, eine Bestätigung erhält. Somit kann, wenn jemand eine Bestätigung erhält und nicht unterschrieben hat, eingegriffen und eine Meldung bei einer Meldestelle (sei es Gemeinde oder BK) gemacht werden.

---

### Phase 6
Als Identifikation & Authentifikation ist es für uns keine Diskussion, dass die E-ID, aber auch weitere Identity Provider zugelassen werden sollen.

---

## Fazit
Die Phasen sollen unsere Diskussion strukturieren und transparent darlegen, was unsere Gedanken waren, bis wir zum vorgestellten Lösungsansatz gekommen sind. Daraus schliessen wir folgende Merkmale die für uns Goals and Requirements für E-Collecting ist.

### Goals and Requirements

| Goal / Requirement | Beschreibung | Muss / Kann
| - | ------- | -
| Nationale Lösung | Die Lösung soll alle Ebenen abdecken | Muss
| Papier und Digital | Alle abgegebene Unterstützungsbekundungen sollen für die Bescheinigung digitalisert sein | Muss
| Souveränität der Stakeholders | Bescheinigung für alle Kanäle (Papier und Digital) ist bei den Gemeinden | Muss
| Identifikation & Authorizierung | Eindeutige Identifikation & Authentifizierung für die Beurkudung durch elektronische ID für den digitalen Kanal; es wird keine digitale Unterschrift benötigt, ist aber möglich | Muss
| Mehrfache Unterstützungbekundung Verbieten | Die erste Unterstützungsbekundung gilt, mehrfache Unterstützungsbekundungen müssen entdeckt werden (innerhalb einer Gemeinde und vom Kanton) | Muss
| Nichtabstreitbarkeit & Nachvollziehbarkeit | Eine Person kann nicht seine Unterstützungsbekundung widerrufen und kann nicht bestreiten seine Unterstüzungsbekundung abgegeben zu haben. Es ist Nachvollziehbar wer was wann gemacht hat. <br> Bestätigung der Unterstützungsbeurkundung; der Stimmberechtigter muss wissen können ob er eune Unterstützungsbekundung abgegeben hat oder nicht. | Muss
| Stimmgeheimnis (1) | Stufe 1 | Muss
| Verifizierter Unterstützungsbekundungsammler | Es ist nachvollziehbar für welches "Komitee" eine Unterstützungbekundung eingegangen ist | Kann
| Stimmgeheimnis (2) | Stufe 4 | Kann
| Count-as-recorded | Benötigt die Krypto | Kann
| Participation-as-intended | Benötigt die Krypto | Kann


## Topics addressed

| Topic | (How) is it addressed? |
| -| ------- |
| 1 | *Vom Unterstützungswillen zur Unterstützungsbekundung* <br> Je nach dem, welchen Digitalisierungsgrad man für E-Collecting möchte gibt es verschiedene Varianten. Eine rein digitale User-Journey, wäre wie in unserem möglichen vorgestellten Lösungsansatz, indem ein Link zur Initative versendet wird. Bei einem hybriden Ansatz ginge es so, dass das Komitee einem beispielsweise auf der Strasse anspricht, und mit einem QR-Code zur Initiative gelangt. Wie kann verhindert werden, dass Betrügerinnen oder Betrüger eine Unterstützungsbekundung für ein anderes als das auf dem Handy angezeigte Volksbegehren erschleichen? Mit dem Lösungsanstaz, dass wenn die Gemeinde geprüft hat, eine Bestätigung auslöst beisoielsweise. Ausserdem sollen die gängigen Sicherheitsstandards erfüllt sein, dass man die URL prüfen kann und ein Schlosssymbol besteht, Prüfung bei der Installation der App möglich. In welcher Reihenfolge müssten die Volksbegehren aufgelistet sein, damit kein politisches Ungleichgewicht entsteht? Dies kann mit einer nuetralen Regel bestimmt sein, wie beispielsweise nach Fristen oder nach Einreichung.|
| 2 | *Zugang zu aktuellen Informationen über die eingereichten Unterstützungsbekundungen* <br> Das Komitee hat Zugriff auf die zentrale E-Collecting Plattform. Dort werden die Daten für das Komitee anonymistiert bis auf die PLZ. Sobald die Unterstützungsbeurkundung geprüft ist von der Gemeinde, wird diese zurück in die E-Collecting Plattform gespielt und dort aufbereitet.|
| 3 | *Zuschreibung der Unterstützungsbekundungen an Komitees und Sammelunternehmen* <br> Hash von Name,Adress wird an E-Collecting Platform gesendet, zusammen mit der Komitee-ID welche den Link ausstellte. Nach Eintreffen der Verifizierung durch die Gemeinden kann Anzahl Übereinstimmungen gezählt werden.|
| 4 | *Unterbreitung von Argumenten der Komitees via E-Collecting* <br> Den Komitees steht wie bereits heute der Unterschriftenbogen zu Verfügung und sie dürfen frei eine Webseite gestalten. AUf der E-Collecting Plattform werden die selben Informationen wie als Antrag bei der Bundeskanzelei angezeigt, damit alle Komitees die gleiche voraussetzung haben. Sobald eine Webseite besteht, dann diese verlinkt werden für weitere Informationen, weitere Inhalte werden jedoch nicht angezeigt. Es besteht uach digital das gleiche Inhaltsformat wie heute.|
| 5 | *Ausschluss unrechtmässiger Unterstützungsbekundungen* <br> Durch die Qualified Electronic Signature deutlich stärker erreicht als bisher und wie mit dem aufgezeigen Lösungsansatz die Bestätigung der Unterstützungsbeurkundung.|
| 6 | *Verhinderung unterschlagener Unterstützungsbekundungen* <br> Dadurch, dass alle Unterstützungsbekundungen direkt in die E-Collecting Plattform zentral zusammenkommen, können die Unterstützungsbekundungen gezählt werden. Dadurch, dass die verifizierung der Unterstützungsbekundungen immer noch bei der Gemeinde liegt, kann ein menschlicher Fehler nicht ausgeschlossen werden. Beim Austausch der Daten, digital, kann aber vieles minimiert werden. Ebenfalls, weil man davon ausgeht, dass einige Unterstützungsbekundungen noch physisch kommen. Diese müssen gescannt werden, in der E-Collecting Plattform erfasst werden, der Gemeinde digital weitergeleitet werden.|
| 7 | *Wahrung des Stimmgeheimnisses* <br> Durch einen Ansatz, welcher von Florian und Audhild erarbeitet wurde kann ein Stimmgeheimniss Stufe 4 gewährt werden. Der mögliche Lösungsansatz kann auf ein Stimmgehemniss Stufe 1 gebracht werden, was unserer Meinung nach ein muss ist.|
| 8 | *Integration mit dem papierbasierten Prozess* <br> Mit unserem möglichen Lösungsansatz, können physische Unterstützungsbekundungen weiterhin erfolgen. diese werden gescannt und die Daten werden in der E-Collecting Plattform erfasst, gemeinsam mit den eingegangen digitalen Unterstützungsbekundungen werden diese an die Gemeinde weitergeleitet. SO kann die Gemeinde auf einmal alle prüfen, validieren und zurück an die E-Collecting Plattform weitergeleitet werden.|
| 9 | *Erleichterte Einführung für Gemeinden mit Effizienzgewinn; auf der Grundlage von bestehender Infrastruktur und bestehenden Prozessen* <br> Da alle Unterstützungsbekundungen über die E-Collecting Plattform kommen können, kann die Gemeinde entlastet werden. So erhält die Gemeinde Daten, welche sie prüfen muss die bereits digital sind. Die Gemeinde gewinnt an Effizienz.|
| 10 | *E-Collecting für alle föderalen Ebene* <br> Eine zentrale E-Collecting Plattform, welche dank einer Schnitstelle zum Einwohneramt, welche die Stimmrechtsausweis hat garantieren. So können auch kantonale und kommunale Sammlungen möglöich sein.|


## Contributing
Please read [CONTRIBUTING.md](/CONTRIBUTING.md) for details on our code of conduct.

