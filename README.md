# 4) E-Collecting User Journey mit Nutzung der Erfahrung von SwissSign, ePost und E-Voting

*Over the course of two days, you will develop your solution for collecting electronic signatures for popular initiatives and referendums from A to Z, addressing the 10 topics outlined in the [guidelines](https://www.bk.admin.ch/bk/de/home/politische-rechte/e-collecting/aktuelles.html). Your prototype can be conceptual, clickable, and/or technical. Either way, you should clearly present the interactions and data flows between actors, software, and infrastructure components over time, as well as the user experience of these actors.*

## Approach

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

  
## Documentation and Diagrams


### Flowchart: High-level Process (First Example)

*An overall process flow showing the main steps and system/actor interactions for ordering a pizza online via a delivery website, including software, infrastructure, and handoff to the restaurant and delivery driver.*

```mermaid

flowchart TB
 subgraph B1["Bürger:innen"]
        B1_1["Erhalt Direktlink zur Initiative"]
        B1_2["Authentifizierung & einlogen"]
        B1_3["Unterstützungsbeurkundung"]
  end
 subgraph B2["Komitee"]
        B2_1["Erarbeiten Initiative"]
        B2_2["Initiative erfassen"]
        B2_3["Initiative teilen"]
  end
 subgraph B3["E-Collecting System"]
        B3_1["Initiative erfasst"]
        B3_2["Freigegebene Initiative"]
        B3_3["Unterstützungsbeurkundung"]
  end
 subgraph B6["Bundeskanzelei"]
        B6_1["Initiative prüfen"]
        B6_2["Initiative freigeben"]
  end
 subgraph B7["Gemeinde"]
        B7_1["Stimmregister"]
        B7_2["Unterstützungsbeurkundung"]
  end
    B2_1 --> B2_2
    B2_2 --> B3_1
    B3_1 --> B6_1
    B6_1 --> B6_2
    B6_2 --> B3_2
    B3_2 --> B2_3 & B1_3
    B2_3 --> B1_1
    B1_1 --> B1_2
    B1_2 --> B3_2
    B1_3 --> B3_3
    B3_3 -- Abgleich --> B7_1
    B7_1 --> B7_2
    B7_2 -->|Bescheinigung| B3_3
    B3_3 --> |Benachrichtigung| B1_3

```

## Topics addressed

| Topic | (How) is it addressed? |
| -| ------- |
| 1 | *Vom Unterstützungswillen zur Unterstützungsbekundung* <br> Mit dem Lösungsansatz wollen wir eine User-Journey erarbeiten für einen nationalen E-Collecting Ansatz.|
| 2 | *Zugang zu aktuellen Informationen über die eingereichten Unterstützungsbekundungen* <br> Hier könnten die Capabilities von ePost genutzt werden. |
| 3 | *Zuschreibung der Unterstützungsbekundungen an Komitees und Sammelunternehmen* <br> Hier könnten die Capabilities von ePost genutzt werden. |
| 4 | *Unterbreitung von Argumenten der Komitees via E-Collecting* <br> Hier könnten die Capabilities von ePost genutzt werden.|
| 5 | *Ausschluss unrechtmässiger Unterstützungsbekundungen* <br> Hier kann das Know How von E-Voting genutzt werden.|
| 6 | *Verhinderung unterschlagener Unterstützungsbekundungen* <br> Hier kann das Know How von E-Voting genutzt werden.|
| 7 | *Wahrung des Stimmgeheimnisses* <br> Gemeinsam definieren welche Stufe E-Collecting erreichen sollte. Hier kann das Know How von E-Voting genutzt werden.|
| 8 | *Integration mit dem papierbasierten Prozess* <br> Gemeinsam definieren welche Stufe E-Collecting erreichen sollte. Hier kann das Know How von E-Voting genutzt werden.|
| 9 | *Erleichterte Einführung für Gemeinden mit Effizienzgewinn; auf der Grundlage von bestehender Infrastruktur und bestehenden Prozessen* <br> Hier kann das Know How von E-Voting genutzt werden.|

## Key Strenghts and Weaknesses

### Strengths:
- Know How aus E-Voting 
- Capabilities der sicheren Zustellung mit ePost
- Capabilities bezüglich Unterschriften mit SwissSign

## Contributing

Please read [CONTRIBUTING.md](/CONTRIBUTING.md) for details on our code of conduct.

## Team Members

- Amina Bouzar
- Jörg Scchorr
- Marcel Eichmüller
- Roman Riesen
- Leonardo Moretti
- Lukas Erni
- Audhild Høgåsen


This software is licensed under a AGPL 3.0 License - see the [LICENSE](LICENSE) file for details. Please feel free to [choose any other](https://choosealicense.com/) [Open Source Initiative approved license](https://opensource.org/licenses) (e.g. a permissive license such as [MIT](https://opensource.org/license/mit)). Other content (e.g. text, images, etc.) is licensed under a [Creative Commons CC BY-SA 4.0 license](https://creativecommons.org/licenses/by-sa/4.0/deed.de). Exceptions are possible in consultation with the organizers.
