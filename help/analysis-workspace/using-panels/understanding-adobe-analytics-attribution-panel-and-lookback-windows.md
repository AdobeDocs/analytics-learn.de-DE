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
exl-id: 1da9334b-0edb-4237-b7ca-57640865208c
source-git-commit: f1bb981a83eb698f4185a22c367346a9ddd0c755
workflow-type: tm+mt
source-wordcount: '1664'
ht-degree: 1%

---

# Grundlagen zum Adobe Analytics-Attributionsbedienfeld und zu Lookback-Fenstern

Als ich zum ersten Mal über das Attributionsbedienfeld [1} und das Lookback-Fenster **3} nachdachte, wurde ich sofort an das Konzept der *Zeitreise&#39;* erinnert. Dann wurde ich natürlich auch an unsere typische Antwort auf viele neue Tools wie diese erinnert, indem ich einfach versuchte, sie zu verwenden, weil sie so kompliziert aussehen.](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/panels/attribution.html?lang=en)**

Ich meine ehrlich, schauen Sie sich nur all diese Optionen an, Schalter, Bedienfelder, Auslesungen und Knöpfe.  Und im Ernst, sprechen wir über diese komplizierten blinkenden Lichter, Schläuche, Messgeräte... WARTEN!  Es ist nicht an der Zeit, abgelenkt über Zeitmaschinen zu reden, wir haben einfach keine Zeit... oder?

Ich gebe zu, dass das Attributionsbedienfeld **1} ein ziemlich komplexes Tool ist. Unsere typische Aufgabe als Analysten besteht jedoch darin, Tag für Tag ein- und auswärts ein weiteres bevorzugtes und hochkomplexes Tool zu verwenden, um auch einen Blick auf die Geschehnisse der Vergangenheit zu werfen.** Dieses Tool heißt ***Adobe Analytics***!  Also ja, um unsere sehr wichtige Frage zu beantworten, glaube ich, dass diese beiden Dinge sagen, dass wir viel Zeit haben.

Warum sollten wir es also zulassen, dass so etwas wie eine kleine Angst so erstaunlichen, ausgeklügelten und leistungsstarken Tools wie diesen im wahrsten Sinne des Wortes *rückwärts* in der Zeit, jeden einzelnen Tag, aussieht?

Schließlich - das ist TIME REISE, Leute!!  Wir sind alle über solche Sachen.  Richtig??!!

Worauf warten wir also - ein glänzendes Metallauto, eine Polizeikiste oder ein altes Telefonkabine, das die Verkabelung eines alten Regenschirms als Antenne verwendet, um sich vor unserer Haustür zu zeigen?

Nein!  Wir haben noch etwas Besseres, also schnallen wir uns ein und hängen!

Na ja... du hast die Idee.


Nun, da wir uns alle über Zeitreisen begeistern, lassen Sie uns tief atmen, ein wenig zurücktreten, feststellen, was das Attributionsbedienfeld **1} *wirklich* ist, und Dinge ein wenig aufschlüsseln:**

![Attribution](assets/attribution.png)

*Abbildung 1: Die angezeigten Zahlen sind inline mit Text weiter unter*

Überlegen Sie einfach, wie Ereignisse/Aktionen in **Attribution** von einer Person, mehreren Einzelanwendern oder einer beliebigen Anzahl verschiedener Ereignisse im Zeitverlauf verursacht werden können.

Gemäß [Adobe](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/overview.html?lang=en) bietet *Attribution* Analysten die Möglichkeit, anzupassen, wie *Dimension*-Elemente für *Erfolgsereignisse* zugeschrieben werden.


>[!WARNING]
>
>**Attributionsmodelle** sind so häufig mit **Marketingkanälen** verknüpft, dass ich im obigen Bild absichtlich *❷ KANAL durchkreuzt habe, um zu veranschaulichen, dass es möglich ist, eine **Attribution**-Analyse für die meisten anderen*** Dimensionen ***durchzuführen.*


In der Tat ist selten eine Journey wirklich linear und sogar noch seltener vorhersehbar.  Darüber hinaus geht jeder Kunde in seinem eigenen Tempo vor. Oft kann er sich verdoppeln, anhalten, abbrechen oder sich in einem anderen nicht linearen Verhalten engagieren. Diese organischen Aktionen machen es schwierig oder praktisch unmöglich, die Auswirkungen von Marketingmaßnahmen auf die Journey zu kennen. Außerdem werden die Bemühungen zur Verknüpfung mehrerer Datenkanäle behindert.

Das ist richtig.  Lassen Sie Ihre &quot;Domino&quot;-Analogien vor der Tür und öffnen Sie Ihren Geist zu Konzepten, die mehr dem Schmetterlingseffekt und der String-Theorie entsprechen - aber wie alles andere müssen wir mit einigen der Grundlagen beginnen.

## **Attributionsmodelle**

Wenn wir das Attributionsbedienfeld **1} verwenden, werden wir möglicherweise mehrere verschiedene Dinge beobachten.**  Beispielsweise zeigen uns die **Attributionsmodelle**, wie unsere *Konversionen* (d. h. ❶ **Erfolgsmetriken**) in jeder beliebigen Gruppe auf *Treffer* verteilt werden können.

Wenn **10 Personen** einfach einen **BIG RED BUTTON** drücken, um durch eine Tür zu gehen, werden unsere **Attributionsmodelle** uns mitteilen, welche dieser **10 Personen** wir &quot;Guthaben&quot; zuweisen wollen - oder besser gesagt, wie *viel* &quot;Guthaben&quot; wir ihnen zuweisen wollen.

![Schaltfläche](assets/button.png)

Beachten Sie dies bei einigen Beispielen, wie die ❸ **Attributionsmodelle** diese **10 Personen** beeinflussen können:

- **Erstkontakt**: Dieses Modell funktioniert genau so, wie es klingt, indem **100% der** Person *zuerst* zugeschrieben wird, die durch die Tür ging.  Marketingexperten verwenden diesen Ansatz eher für Taktiken wie ***Social Media*** oder ***display***. Es ist jedoch auch eine großartige Taktik, häufig für die Effektivität von Produktempfehlungen vor Ort zu verwenden.
- **Letztkontakt**: Diese Taktik funktioniert auch genau so, wie sie sich anhört, sondern gibt **100% des Guthabens** der letzten Person, die durch die Tür ging.  Dieses Modell wird normalerweise verwendet, um Dinge wie ***natürliche (organische) Suche*** und andere *kurzfristige* Marketingzykluskampagnen zu analysieren.
- **Linear**: Dieses Modell verteilt die gleiche Gewichtung auf JEDE EINZELNE PERSON, die durch die Tür ging.

  >[!CAUTION]
  >
  >Vorsicht wird jedoch empfohlen, da Sie bei der Anwendung dieser Taktik sehr schnell Ihre Ergebnisse verbreiten können. Dabei ist zu berücksichtigen, je länger sie ausgeführt wird und je größer die Zielgruppe, die sie trifft.

- **U-förmig**: Bei diesem Ansatz wird **40%** des Guthabens der *ersten Person* in der Tür zugewiesen, **20%** des Guthabens wird auf *alle zwischen* verteilt und **40%** auf die **letzte Person** übertragen. . Dieses Modell wird in den meisten Fällen verwendet, wenn Sie einen **langen Konversions-/Verkaufszyklus** haben, der auf dem Weg *mehrere Touchpoints* enthält.  In diesem Fall besteht Ihr Ziel darin, in erster Linie die Marketingtaktiken ***first*** und ***last*** hervorzuheben, die zur Konversion des Kunden beigetragen haben.
- **J**-**förmig** und **umgekehrt J**:
   - Denken Sie an **U-förmig**, aber stattdessen weist dieses Modell der *letzten Person*, die durch die Tür geht, **60%** die Gutschrift zu, **20%** der *ersten* und dann teilt *die verbleibenden **20%**auf* alle anderen *in der Mitte.*  **Umgekehrter J** bewirkt das genaue Gegenteil.

     Das Ziel besteht hier darin, den größten Teil Ihrer Betonung entweder am *Anfang* oder am *Ende* Ihrer Kampagne zu platzieren. Sie möchten dem beitragenden Element jedoch trotzdem eine gewisse Gutschrift am anderen Ende zuweisen, während Sie dabei die &quot;kleinen Kerle&quot;anerkennen.

- **Zeitverfall**: Jetzt würde ich mich zurückweisen, wenn ich diesen nicht teilen würde. Dieses Modell hat buchstäblich eine Halbwertszeit, die exponentiell abnimmt - im Laufe der Zeit!  In diesem Fall beträgt der Parameter *default* für die Halbwertszeit dieses Modells **7 Tage**.  Anschließend wird *Gewichtung* auf jeden **Marketing-Kanal**, *auf Grundlage der Zeit* angewendet, die nach dem *ursprünglichen Touchpoint* vergeht, und wenn der Kunde konvertiert.

  **Zeitverfall** und **U-förmige Attributionsmodelle** werden normalerweise verwendet, um längerfristige Kampagnen zu messen. Wie Sie sehen können, haben sie jedoch etwas andere Ziele, je nachdem, wie sie letztendlich den Wert des Ergebnisses *gewichten*.

- **Benutzerdefiniert**: Sie wählen aus, wer eine Gutschrift erhält.  Das ist deine Kampagne!

Weitere Informationen zu diesen und anderen Attributionsmodellen finden Sie hier [](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html?lang=en)

Um das noch interessanter zu machen, lassen Sie uns darüber reden, die Uhr zurückzudrehen!

## **Lookback-Fenster**

Jetzt ist es an der Zeit, Ihre Meinung auf die nächste Stufe zu bringen.  Hier fügen wir buchstäblich das Element Zeitreise zu unserer Analyse hinzu - und wieder beginnen wir mit den Grundlagen.

***Adobe*** definiert ❹ **Lookback-Fenster** als &quot;die Zeit, die eine Konversion zurückblicken sollte, um Touchpoints aufzunehmen. Attributionsmodelle, die der ersten Interaktion mehr Gewicht verleihen, sehen bei der Anzeige verschiedener Lookback-Fenster größere Unterschiede.&quot;


Mit anderen Worten: **Lookback-Fenster** bestimmen den Zeitraum, in dem *Konversionen* berücksichtigt werden, und stellen *Kontext* für die Attributionsanalyse bereit. ***Adobe Analytics*** bietet drei Arten von **Lookback-Fenstern**:

- **Besuchs-Lookback-Fenster:** Blickt zurück zum Anfang eines ***Besuchs***, wenn eine Konversion stattgefunden hat, und bietet Einblicke in die direkten Interaktionen, die zu Konversionen führten.

  Beachten Sie, dass dies normalerweise das kürzeste **Lookback-Fenster** ist, das verwendet werden kann.
- **Besucher-Lookback-Fenster:** Betrachtet alle ***Besuche*** bis zum ersten des Monats innerhalb des ausgewählten **Datumsbereichs**, bietet einen viel breiteren Überblick über die Interaktionen des Kunden und hilft, Muster im Zeitverlauf zu identifizieren.
- **Benutzerdefiniertes Lookback-Fenster:** Ermöglicht Ihnen, das **Attributionsfenster** über den Berichterstellungsdatumsbereich **5} hinaus auf maximal *maximal* von** 90 Tagen **zu erweitern.**  Es bietet *Flexibilität* bei der Erfassung von Touchpoints, die außerhalb des ausgewählten **Datumsbereichs** aufgetreten sind, um eine umfassende Analyse zu gewährleisten.**

Durch Anpassung eines gegebenen **Lookback-Fensters** können Analysten dann die Auswirkungen eines oder mehrerer Touchpoints innerhalb bestimmter Zeitrahmen untersuchen und bessere Einblicke in die Auswirkungen verschiedener Dauern auf die Attributionsergebnisse erhalten.

## **Alles zusammenbringen**

Was bedeutet das also für uns Analysten?

Das **Attributionsbedienfeld** und das **Lookback-Fenster** geben uns die Möglichkeit, über die alltäglichen, oberflächlichen Daten hinauszublicken und tiefer in die Journey des Kunden zu tauchen. Indem wir verstehen, welche Touchpoints den größten Einfluss auf *Konversionen* hatten, können wir fundierte Entscheidungen über unsere Marketing-Strategien treffen und Ressourcen effektiver zuweisen.

Denken Sie daran, dass Sie nach Auswahl Ihrer **Attributionsmodelle** und **Lookback-Fenster** Ihre Daten weiter bearbeiten können, indem Sie sie mit einem ❺ **Segment,** oder einer anderen Komponente filtern, die Sie zu diesem Zeitpunkt wünschen.  Darüber hinaus steht Ihnen nach dem Rendern des Bedienfelds die gesamte Funktionalität eines herkömmlichen Workspace zur Verfügung.

## **Letzte Umsetzung in die Praxis**

Nun, da Sie die Konzepte festgelegt haben, stellen Sie sich vor, Sie führen eine Marketing-Kampagne durch und versuchen zu ermitteln, welcher Kanal der *effektivste* für Konversionen ist. Mithilfe des Attributionsbedienfelds **1} können Sie nicht nur den** letzten Kontakt **sehen, sondern auch den** ersten Kontakt **, den** gleichen Kontakt **und jedes andere** Modell **, mit dem Sie bestimmen, welche** Kanäle **die *effektivste Konvertierung* bei der Steigerung Ihres *sind sions*.** Diese Informationen können dann verwendet werden, um Ihre Kampagnen zu *optimieren* und die Gesamtleistung zu verbessern, indem Sie einfach die Uhr mit dem gewünschten **Lookback-Fenster** zurückschalten!

Nachdem Sie nun gesehen haben, was es kann, lassen Sie sich nicht von den scheinbar komplexen Funktionen des Attributionsbedienfelds täuschen oder einschüchtern.  **Stellen Sie es sich vor**.  *Embrace*.  **Verstehen** Sie es.
ABER DIE MEISTEN - *NUTZEN SIE SIE ZU IHREM VORTEIL.* Das **Attributionsbedienfeld** und das **Lookback-Fenster** sind die Schlüssel zum Entsperren eines tieferen Verständnisses Ihrer Kunden und ihrer Journey mit Ihrer Marke.

Jetzt können wir mit Sicherheit &quot;[Zurück in der Zeit](https://youtu.be/gVryJmZNFdU)&quot; reisen und die Leistung unseres Trustists-Zeitgeräts (auch ***Adobe Analytics*** genannt) nutzen, um datengesteuerte Entscheidungen zu treffen.

## Autor

Dieses Dokument wurde verfasst von:

![Jeff Bloomer](assets/jeff-headshot.png)

**Jeff Bloomer**, Manager, Digital Analytics bei Kroger Personal Finance

Adobe Analytics-Expertin
