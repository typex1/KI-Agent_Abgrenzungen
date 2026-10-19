## Bedingungen, die für/gegen die Nutzung eines KI Agenten sprechen

Ein guter Ausgangspunkt: Wenn menschliche Sprache als Input dient, kann ein KI-Agent besonders nützlich sein. Allerdings ist Sprache allein noch kein ausreichender Grund für einen Agenten. Ein klassischer Sprachverarbeitungsbaustein oder ein LLM-Aufruf ohne agentische Fähigkeiten kann dafür bereits ausreichen.

Entscheidend ist vielmehr, ob eine Aufgabe Flexibilität, Interpretation, dynamische Entscheidungen und die Koordination mehrerer Handlungsschritte erfordert – und ob diese Fähigkeiten den zusätzlichen Aufwand und die Risiken rechtfertigen.

## 1. Bedingungen, die für einen KI-Agenten sprechen

Ich würde die folgenden Kriterien sammeln und sie nach ihrem praktischen Nutzen ordnen.

1\. Unstrukturierter oder natürlichsprachlicher Input

Die Eingaben kommen als Freitext, E-Mail, Dokument, Chatnachricht oder gesprochene Sprache. Bedeutung und Absicht müssen interpretiert werden, statt nur feste Felder auszulesen.

Beispiel: Ein Agent versteht eine Kundenanfrage wie „Meine Bestellung ist immer noch nicht da – könnt ihr das bitte klären?“ und leitet daraus die nächsten Schritte ab.

2\. Unterschiedliche Lösungswege je nach Situation

Der Ablauf lässt sich nicht vollständig im Voraus als feste Sequenz definieren. Welche Aktion als Nächstes sinnvoll ist, hängt von den bisherigen Ergebnissen und dem aktuellen Kontext ab.

Beispiel: Bei einer Supportanfrage prüft der Agent je nach Fall zunächst den Bestellstatus, die Zahlungsdaten oder die Versandinformationen.

3\. Mehrstufige Aufgaben mit Zwischenentscheidungen

Die Aufgabe besteht aus mehreren voneinander abhängigen Schritten. Zwischenergebnisse beeinflussen, wie es weitergeht.

Beispiel: Eine Marktanalyse durchführen, passende Quellen suchen, Informationen vergleichen und daraus einen Bericht erstellen.

4\. Bedarf an dynamischer Tool-Auswahl

Das System muss entscheiden, welches Werkzeug es wann verwendet – etwa eine API, Datenbank, Suchmaschine, einen Rechner oder ein internes Geschäftssystem.

Beispiel: Ein Coding-Agent entscheidet, ob er zunächst den Code analysiert, Tests ausführt, eine Datei bearbeitet oder Dokumentation nachschlägt.

5\. Iteratives Vorgehen und Anpassung an Zwischenergebnisse

Die Lösung entsteht nicht unbedingt in einem einzigen Durchlauf. Das System kann Ergebnisse überprüfen, Fehler erkennen und weitere Schritte ausführen.

Beispiel: Ein Agent generiert Code, führt Tests aus, analysiert fehlgeschlagene Tests und versucht eine Korrektur.

6\. Kontextabhängige Entscheidungen

Für eine sinnvolle Entscheidung müssen mehrere Informationen kombiniert werden, beispielsweise Gesprächsverlauf, Nutzerabsicht, Geschäftsdaten und bisherige Ergebnisse.

Beispiel: Ein persönlicher Lernassistent passt Erklärungen an den Wissensstand und die bisherigen Schwierigkeiten eines Studierenden an.

7\. Hohe Variabilität der Fälle

Es gibt viele mögliche Eingabekombinationen, Ausnahmen und Sonderfälle. Ein umfassendes Regelwerk wäre schwer zu erstellen, zu testen und zu pflegen.

Beispiel: Die Bearbeitung sehr unterschiedlicher Kundenanliegen, bei denen die relevanten Informationen und erforderlichen Schritte variieren.

8\. Ein Ziel ist vorgegeben, aber nicht jeder Schritt

Das System erhält ein Ergebnisziel und muss selbst einen geeigneten Weg dorthin bestimmen. Es geht also nicht nur um die Ausführung einer vorgegebenen Prozedur.

Beispiel: „Finde drei geeignete Anbieter, vergleiche ihre Konditionen und begründe eine Empfehlung.“

9\. Die relevante Umgebung verändert sich

Der Agent muss auf neue Informationen, veränderte Daten oder unerwartete Tool-Ergebnisse reagieren können, statt nur einen statischen Ablauf abzuarbeiten.

Beispiel: Ein Recherche-Agent passt seine Suche an, wenn die ursprünglichen Quellen nicht verfügbar sind oder neue Erkenntnisse eine andere Suchrichtung nahelegen.

10\. Interaktion mit Menschen während der Aufgabenerledigung

Das System muss Rückfragen stellen, fehlende Informationen ermitteln, Präferenzen berücksichtigen oder bei Unsicherheit eine Freigabe einholen.

Beispiel: Ein Reiseplanungsagent fragt nach dem Budget, wenn dieses fehlt, und lässt eine Buchung vor ihrer Ausführung bestätigen.

11\. Erforderliches Schlussfolgern unter Unsicherheit

Informationen sind unvollständig, mehrdeutig oder widersprüchlich. Das System muss mehrere Hypothesen abwägen und gegebenenfalls zusätzliche Informationen beschaffen.

Beispiel: Ein IT-Support-Agent untersucht anhand von Logs, Fehlermeldungen und Systeminformationen eine mögliche Fehlerursache.

12\. Länger laufende Aufgaben mit persistentem Zustand

Die Aufgabe erstreckt sich über mehrere Interaktionen oder Zeitpunkte. Der Agent muss den Fortschritt, offene Aufgaben und relevante Ergebnisse berücksichtigen.

Beispiel: Ein Projektassistent verfolgt offene Arbeitspakete, erinnert an Abhängigkeiten und passt einen Arbeitsplan an neue Termine an.

13\. Personalisierung und flexible Präferenzen

Die optimale Vorgehensweise hängt von individuellen Präferenzen ab, die sich nicht sinnvoll in wenige feste Kategorien abbilden lassen.

Beispiel: Ein Lernagent verändert Schwierigkeitsgrad, Erklärstil und Übungsform anhand von Feedback und Lernfortschritt.

14\. Koordination unterschiedlicher Fähigkeiten oder Systeme

Die Aufgabe erfordert die Zusammenarbeit mehrerer spezialisierter Komponenten, Werkzeuge oder gegebenenfalls Agenten.

Beispiel: Ein System koordiniert Recherche, Datenanalyse und Berichterstellung. Dafür muss allerdings nicht zwingend eine Multi-Agent-Architektur verwendet werden.

## 2. Wann ist eine regelbasierte Lösung die bessere Wahl?

Die Kriterien oben beschreiben, wann agentische Fähigkeiten nützlich sein können. Für die Architekturentscheidung ist die Gegenseite mindestens genauso wichtig.

| Bedingung         | Eher regelbasiert                             | Eher KI-Agent                                              |
| ----------------- | --------------------------------------------- | ---------------------------------------------------------- |
| Prozess           | Feste, bekannte Abläufe                       | Variable Abläufe                                           |
| Eingaben          | Strukturierte Felder und klare Kategorien     | Freitext, mehrdeutige Informationen                        |
| Entscheidungen    | Explizite Regeln und Schwellenwerte           | Kontextabhängige Abwägungen                                |
| Ausnahmen         | Wenige, vorhersehbare Fälle                   | Viele unterschiedliche Sonderfälle                         |
| Tool-Nutzung      | Vorgegebenes Tool in fester Reihenfolge       | Dynamische Auswahl und Reihenfolge                         |
| Anforderungen     | Deterministisches, reproduzierbares Verhalten | Flexibilität und adaptive Problemlösung                    |
| Fehlerfolgen      | Müssen durch feste Regeln kontrolliert werden | Erfordern zusätzliche Absicherung, Prüfungen und Freigaben |
| Kosten und Latenz | Möglichst gering                              | Zusätzlicher Aufwand ist gerechtfertigt                    |

Wichtig: Eine hohe Anzahl von Regeln allein rechtfertigt noch keinen KI-Agenten. Ein komplexer, aber stabiler Prozess kann weiterhin hervorragend durch eine Zustandsmaschine, einen Workflow oder ein Regelwerk abgebildet werden.

## 3. Die entscheidende Unterscheidung: LLM oder Agent?

Gerade für Studierende würde ich drei Architekturen auseinanderhalten:

A. Regelbasierte Automatisierung

Wenn A eintritt, führe B aus; andernfalls C. Der Ablauf ist vorgegeben.

Beispiel: Bei einem Bestellwert über 500 Euro wird eine zusätzliche Freigabe angefordert.

B. LLM-Aufruf innerhalb eines festen Workflows

Ein Sprachmodell übernimmt eine klar begrenzte Aufgabe; der umgebende Programmablauf bleibt fest.

Beispiel: Eine E-Mail wird klassifiziert und anschließend nach festen Regeln weitergeleitet.

C. KI-Agent

Das Modell entscheidet innerhalb definierter Grenzen über nächste Schritte, Tool-Aufrufe und die Fortsetzung der Aufgabe.

Beispiel: Der Agent interpretiert eine E-Mail, prüft bei Bedarf Kundendaten, sucht nach einer Lösung und entscheidet, welche weitere Aktion erforderlich ist.

Ein KI-Agent ist also nicht einfach ein System, das ein LLM verwendet. Ein wesentliches Unterscheidungsmerkmal ist, dass das Modell einen Teil der Steuerung des Lösungsprozesses übernimmt.

## 4. Eine kompakte Entscheidungsregel für die Praxis

Ich würde den Studierenden diese fünf Fragen mitgeben:

Beantworte die Fragen für einen konkreten Anwendungsfall.

1\. Muss das System unstrukturierte oder mehrdeutige Informationen interpretieren?

Zum Beispiel Freitext, Dokumente oder unvollständige Nutzeranfragen.

Ja

Teilweise

Nein

2\. Muss es abhängig von Kontext und Zwischenergebnissen unterschiedliche nächste Schritte wählen?

Nicht nur Inhalte klassifizieren, sondern den Ablauf selbst steuern.

Ja

Teilweise

Nein

3\. Muss es Werkzeuge dynamisch auswählen oder wiederholt einsetzen?

Zum Beispiel APIs, Datenbanken, Suche oder Code-Ausführung.

Ja

Teilweise

Nein

4\. Sind die möglichen Lösungswege so variabel, dass ein fester Workflow unpraktisch wäre?

Viele unterschiedliche Fälle, unerwartete Ergebnisse oder schwer vorab definierbare Pfade.

Ja

Teilweise

Nein

5\. Rechtfertigt der Nutzen die zusätzlichen Kosten und Risiken?

Latenz, Modellkosten, Nichtdeterminismus, Evaluierung und Sicherheitsmaßnahmen.

Ja

Teilweise

Nein


## Gegenindikatoren für einen Agenten

Hier ist eine regelbasierte Lösung, ein fester Workflow oder ein einzelner LLM-Aufruf die bessere Wahl:

- **Der Ablauf ist deterministisch und bekannt.** Ein fester Workflow ist günstiger, schneller und nachvollziehbarer; ohne unstrukturierte Eingaben reicht Stufe 0.
- **Exakte Berechnungen, Buchungen, rechtlich verbindliche Entscheidungen ohne Review.**
- **Strenge Audit- und Compliance-Anforderungen**, bei denen jeder Pfad vorab dokumentiert sein muss.
- **Hohes Volumen bei niedriger Latenz und engem Budget.** Jeder Agentenschritt kostet Tokens und Zeit.

## Faustregel

Beschreib den Vorfall einem Sachbearbeiter.

- Sagt er *"kommt drauf an, ich muss erst mal nachschauen"*, ist das ein Agenten-Kandidat (Stufe 3).
- Zieht er eine Checkliste aus der Schublade und muss dabei Freitext, E-Mails oder Dokumente lesen, ist es ein Workflow mit LLM-Schritten (Stufe 1 oder 2).
- Zieht er eine Checkliste aus der Schublade und alle Angaben stehen bereits in Feldern, ist es eine Regel (Stufe 0). Hier braucht es keine KI.

## Checkliste zur Einordnung

- [ ] Steht die Reihenfolge der Schritte vorab fest?
- [ ] Lassen sich alle Entscheidungen als Regeln formulieren?
- [ ] Sind die Eingaben strukturiert?
- [ ] Ist das Ergebnis ein strukturierter Datensatz?
- [ ] Muss jeder Pfad auditierbar und reproduzierbar sein?

Auswertung:

- **Alle Häkchen gesetzt:** Stufe 0, rein regelbasiert. Keine KI nötig.
- **Die meisten Häkchen gesetzt, aber Eingaben oder Ergebnis unstrukturiert:** Stufe 1 oder 2, fester Ablauf mit LLM-Schritten.
- **Die meisten Kästchen leer:** Stufe 3, ein Agent ist den Aufwand wert.
