---
title: Grundlagen zum Adobe Analytics-Attributionsbedienfeld und zu Lookback-Fenstern
description: Erfahren Sie, wie Sie das Attributionsbedienfeld und das Lookback-Fenster verwenden können, um das Kundenverhalten zu verstehen und anzupassen, wie Dimensionselemente Erfolgsereignissen zugeschrieben werden.
feature: Attribution
role: User
level: Experienced
doc-type: Article
last-substantial-update: 2023-06-20T00:00:00Z
jira: KT-13181
thumbnail: KT-13181.jpeg
source-git-commit: f38a35067bf95fe02200d1409e3e70c1ef28abb3
workflow-type: tm+mt
source-wordcount: '1681'
ht-degree: 3%

---


# Grundlagen zum Adobe Analytics-Attributionsbedienfeld und zu Lookback-Fenstern

Als ich zum ersten Mal an die [Attributionsbedienfeld](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/panels/attribution.html?lang=en) und **Lookback-Fenster**, wurde ich sofort an das Konzept von *Zeitreisen&quot;*; dann wurde ich natürlich auch daran erinnert, dass unsere typische Reaktion auf viele neue Werkzeuge wie diese einfach darin besteht, den Versuch zu verzögern, sie zu verwenden, weil sie so kompliziert aussehen.

Ich meine ehrlich, schauen Sie sich nur all diese Optionen an, Schalter, Bedienfelder, Auslesungen und Knöpfe.  Und im Ernst, sprechen wir über diese komplizierten blinkenden Lichter, Schläuche, Messgeräte... WARTEN!  Es ist nicht an der Zeit, abgelenkt über Zeitmaschinen zu reden, wir haben einfach keine Zeit... oder?

Ich gebe zu, dass **Attributionsbedienfeld** ist ein ziemlich komplexes Werkzeug; unsere typische Aufgabe als Analysten besteht jedoch darin, täglich und tagaus ein weiteres beliebtes und hochkomplexes Werkzeug zu verwenden, um auch einen Blick auf die Geschehnisse der Vergangenheit zu werfen. Dieses Tool heißt ***Adobe Analytics***!  Also ja, um unsere sehr wichtige Frage zu beantworten, glaube ich, dass diese beiden Dinge sagen, dass wir viel Zeit haben.

Warum sollten wir es zulassen, dass so etwas wie eine kleine Angst so erstaunlichen, ausgeklügelten und mächtigen Werkzeugen wie diesen, die es uns buchstäblich erlauben, auszusehen *backward* in der Zeit, jeden einzelnen Tag?

Schließlich - das ist TIME REISE, Leute!!  Wir sind alle über solche Sachen.  Richtig???!!

Worauf warten wir also - ein glänzendes Metallauto, eine Polizeikiste oder ein altes Telefonkabine, das die Verkabelung eines alten Regenschirms als Antenne verwendet, um sich vor unserer Haustür zu zeigen?

Nein!  Wir haben noch etwas Besseres, also schnallen wir uns ein und hängen!

Na ja... du hast die Idee.


Nun, da wir uns alle über Zeitreisen freuen, lassen Sie uns tief atmen, ein wenig zurücktreten, feststellen, was das **Attributionsbedienfeld** *wirklich* ist und Dinge ein wenig unterteilen:

![Attribution](assets/attribution.png)

*Abbildung 1: Inline-Anzeige von Zahlen mit Text weiter unten*

In **Attribution** berücksichtigen Sie einfach, wie Ereignisse/Aktionen von einer Person, mehreren Personen oder einer beliebigen Anzahl von verschiedenen Ereignissen über einen bestimmten Zeitraum verursacht werden können.

Gemäß [Adobe](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/overview.html?lang=en), *Attribution* gibt Analysten die Möglichkeit, die *Dimension* Artikel werden gutgeschrieben für *Erfolgsereignisse*.


>[!WARNING]
>
>Kurze Bemerkung: **Attributionsmodelle** sind so häufig mit **Marketing-Kanäle** dass ich *durchkreuzt* ❷ KANAL in der Abbildung oben, um zu veranschaulichen, dass es möglich ist, **Attribution** Analyse mit den meisten anderen ***Dimension***.


In der Tat ist selten eine Journey wirklich linear und sogar noch seltener vorhersehbar.  Darüber hinaus geht jeder Kunde in seinem eigenen Tempo vor. Oft kann er sich verdoppeln, anhalten, abbrechen oder sich in einem anderen nicht linearen Verhalten engagieren. Diese organischen Aktionen machen es schwierig oder praktisch unmöglich, die Auswirkungen von Marketingmaßnahmen auf die Journey zu kennen. Außerdem werden die Bemühungen zur Verknüpfung mehrerer Datenkanäle behindert.

Das ist richtig.  Lassen Sie Ihre &quot;Domino&quot;-Analogien vor der Tür und öffnen Sie Ihren Geist zu Konzepten, die mehr dem Schmetterlingseffekt und der String-Theorie entsprechen - aber wie alles andere müssen wir mit einigen der Grundlagen beginnen.

## **Attributionsmodelle**

Wenn wir die **Attributionsbedienfeld** können wir anfangen, verschiedene Dinge zu beobachten.  Beispielsweise wird die **Attributionsmodelle** demonstrieren Sie uns, wie unsere *Konversionen* (d. h. ❶ **Erfolgsmetriken**) verteilt werden können. *Treffer* in jeder Gruppe.

Einfach ausgedrückt, wenn **10 Personen** drücken Sie eine **GROSSE ROTE SCHALTFLÄCHE** durch eine Tür zu treten, **Attributionsmodelle** werden uns sagen, welche von denen **10 Personen** Wir möchten &quot;Guthaben&quot; zuweisen - oder besser gesagt, wie *viel* &quot;Guthaben&quot; wollen wir sie zuweisen - für das Drücken des Knopfes.

![Schaltfläche](assets/button.png)

Im Folgenden finden Sie einige Beispiele dafür, wie die ❸ **Attributionsmodelle** kann sich auf **10 Personen**:

- **Erstkontakt**: Dieses Modell funktioniert genau wie es klingt, indem es **100 % Kredit** der *first* Person, die durch die Tür ging.  Marketingexperten werden diesen Ansatz eher für Taktiken wie ***Social Media*** oder ***display*** Es ist jedoch auch eine großartige Taktik, häufig für die Effektivität von Produktempfehlungen vor Ort zu verwenden.
- **Letztkontakt**: Diese Taktik funktioniert auch genau wie sie klingt, gibt aber stattdessen **100 % Kredit** zum LETZTEN, der durch die Tür ging.  Dieses Modell wird normalerweise verwendet, um Dinge wie ***natürliche (organische) Suche*** und andere *kurzfristig* Marketingzykluskampagnen.
- **Linear**: Dieses Modell verteilt die gleiche Gewichtung auf JEDE EINZELNE PERSON, die durch die Tür ging.

  >[!CAUTION]
  >
  >Vorsicht wird jedoch empfohlen, da Sie bei der Anwendung dieser Taktik sehr schnell Ihre Ergebnisse verbreiten können. Dabei ist zu berücksichtigen, je länger sie ausgeführt wird und je größer die Zielgruppe, die sie trifft.

- **U-förmig**: Dieser Ansatz weist **40 %** des Kredits an die *erste Person* in der Tür, breitet sich aus **20 %** des Kredits *alle dazwischen*, und gibt dann **40 %** der **letzte** durch. Dieses Modell wird meistens in Situationen verwendet, in denen Sie eine **langer Konversions-/Verkaufszyklus** contain *mehrere Touchpoints* auf dem Weg.  In diesem Fall besteht Ihr Ziel darin, in erster Linie die ***first*** und ***last*** Marketingtaktiken, die zur Kundenkonvertierung beigetragen haben.
- **J**-**förmig** und **Umgekehrtes J**:
   - Denken Sie darüber nach **U-förmig**, aber stattdessen weist dieses Modell **60 %** dem *letzte Person* durch die Tür gehen, **20 %** der *first*, und dann *divides* die verbleibenden **20 %** Überall *alle anderen* in der Mitte.  **Umgekehrtes J** tut genau das Gegenteil.

     Das Ziel besteht darin, den größten Teil Ihrer Aufmerksamkeit auf die *Anfang* oder *end* Ihrer Kampagne, aber Sie möchten dem beitragenden Element immer noch einen gewissen Anteil zuweisen, während Sie die &quot;kleinen Jungs&quot;auf dem Weg anerkennen.

- **Zeitverfall**: Nun, ich würde mich zurückweisen, wenn ich dieses nicht teilen würde. Dieses Modell hat buchstäblich eine Halbwertszeit, die exponentiell abnimmt - im Laufe der Zeit!  In diesem Fall wird die *default* Parameter für die Halbwertszeit dieses Modells ist **7 Tage**.  Die Funktionsweise ist dann die Anwendung *Gewichtung* jeder **Marketing-Kanal**, *basierend auf der Zeitdauer* , der nach der *erster Touchpoint* und wenn der Kunde konvertiert.

  **Zeitverfall** und **U-förmige Attributionsmodelle** werden in der Regel zur Messung längerfristiger Kampagnen verwendet. Wie Sie sehen können, haben sie jedoch etwas unterschiedliche Ziele, je nachdem, wie sie letztendlich aussehen *wiegen* Wert des Ergebnisses.

- **Benutzerdefiniert**: Sie wählen aus und wählen aus, wem ein Guthaben gutgeschrieben wird.  Das ist deine Kampagne!

Weitere Informationen zu diesen und anderen Attributionsmodellen finden Sie unter [Klicken Sie hier](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html?lang=de)

Um das noch interessanter zu machen, lassen Sie uns darüber reden, die Uhr zurückzudrehen!

## **Lookback-Fenster**

Jetzt ist es an der Zeit, Ihre Meinung auf die nächste Stufe zu bringen.  Hier fügen wir buchstäblich das Element Zeitreise zu unserer Analyse hinzu - und wieder beginnen wir mit den Grundlagen.

***Adobe*** definiert ❹ **Lookback-Fenster** als &quot;die Zeit, die eine Konversion zurückblicken sollte, um Touchpoints aufzunehmen. Attributionsmodelle, die der ersten Interaktion mehr Gewicht zuschreiben, sehen bei der Anzeige verschiedener Lookback-Fenster größere Unterschiede.&quot;


Mit anderen Worten: **Lookback-Fenster** den Zeitraum festlegen, in dem *Konversionen* berücksichtigt werden und *context* zur Attributionsanalyse. ***Adobe Analytics*** bietet drei Arten von **Lookback-Fenster**:

- **Besuchs-Lookback-Fenster:** Blickt zurück zum Anfang eines ***Besuch*** wenn eine Konversion stattgefunden hat, und bietet Einblicke in die unmittelbaren Interaktionen, die zu Konversionen führten.

  Beachten Sie, dass dies normalerweise der kürzeste ist **Lookback-Fenster** verwendet werden.
- **Besucher-Lookback-Fenster:** Sieht überhaupt aus ***Besuche*** Sicherung bis zum ersten des Monats innerhalb des ausgewählten **Datumsbereich** bietet einen viel breiteren Überblick über die Interaktionen des Kunden und hilft, Muster im Laufe der Zeit zu identifizieren.
- **Benutzerdefiniertes Lookback-Fenster:** Ermöglicht Ihnen das Erweitern der **Attributionsfenster** über die Berichterstellung hinaus **Datumsbereich** bis zu einem *maximum* von **90 Tage**.  Sie bietet *Flexibilität* Erfassen von Touchpoints, die aufgetreten sind *outside* die ausgewählte **Datumsbereich**, um eine umfassende Analyse zu gewährleisten.

Durch Anpassung eines bestimmten **Lookback-Fenster** können Analysten dann die Auswirkungen eines oder mehrerer Touchpoints innerhalb bestimmter Zeitrahmen untersuchen und bessere Einblicke in die Auswirkungen verschiedener Dauern auf die Attributionsergebnisse erhalten.

## **Alles zusammenbringen**

Was bedeutet das also für uns Analysten?

Die **Attributionsbedienfeld** und **Lookback-Fenster** geben uns die Macht, über die alltäglichen, oberflächlichen Daten hinaus zu schauen und tiefer in die Journey zu tauchen. Durch Verständnis, welche Touchpoints den größten Einfluss auf *Konversionen* können wir fundierte Entscheidungen über unsere Marketingstrategien treffen und Ressourcen effektiver zuweisen.

Denken Sie daran, nachdem Sie Ihre **Attributionsmodelle** und **Lookback-Fenster** ausgewählt ist, können Sie Ihre Daten weiter bearbeiten, indem Sie sie mit einem ❺ filtern. **Segment,** oder einer anderen Komponente, die Sie an dieser Stelle wünschen.  Darüber hinaus steht Ihnen nach dem Rendern des Bedienfelds alle Funktionen eines traditionellen Arbeitsbereichs zur Verfügung.

## **Letztere in die Praxis umsetzen**

Nun, da Sie die Konzepte festgelegt haben, stellen Sie sich vor, Sie führen eine Marketing-Kampagne und versuchen zu ermitteln, welcher Kanal der *höchste Effizienz* für Konversionen. Mithilfe des **Attributionsbedienfeld** nicht nur können Sie die **Letztkontakt**, aber auch die **Erstkontakt**, **derselbe Kontakt** und anderen **model** Sie entscheiden, welche **channels** sind *höchste Effizienz* bei der *Konversionen*. Diese Informationen können dann für *optimieren* Ihre Kampagnen und verbessern die Gesamtleistung, indem Sie einfach die Uhr mit der **Lookback-Fenster** Ihrer Wahl!

Nachdem Sie nun gesehen haben, was es kann, lassen Sie sich nicht von den scheinbar komplexen Funktionen des Attributionsbedienfelds täuschen oder einschüchtern.  **Gefällt mir**.  *Embrace* es.  **Grundlegendes** es.
ABER DIE MEISTEN VON ALLEN - *Nutze es zu deinem Vorteil.* Die **Attributionsbedienfeld** und **Lookback-Fenster** sind die Schlüssel, um ein tieferes Verständnis Ihrer Kunden und ihrer Journey mit Ihrer Marke zu gewinnen.

Jetzt können wir reisen &quot;[zurück in der Zeit](https://youtu.be/gVryJmZNFdU)&quot; mit Vertrauen und nutzen Sie die Leistungsfähigkeit unserer Trusty Time Machine (auch bekannt als a.k. ***Adobe Analytics***), um datenbasierte Entscheidungen zu treffen.

## Autor

Dieses Dokument wurde verfasst von:

![Jeff Bloomer](assets/jeff-headshot.png)

**Jeff Bloomer**, Manager, Digital Analytics bei Kroger Personal Finance

Adobe Analytics-Experte