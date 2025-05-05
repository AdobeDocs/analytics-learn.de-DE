---
title: Grundlegendes zum Adobe Analytics-Attributionsbedienfeld und Lookback-Fenstern
description: Erfahren Sie, wie Sie das Attributionsbedienfeld und das Lookback-Fenster verwenden, um das Kundenverhalten zu verstehen und anzupassen, wie Dimensionselemente für Erfolgsereignisse angerechnet werden.
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

# Grundlegendes zum Adobe Analytics-Attributionsbedienfeld und Lookback-Fenstern

Als ich zum ersten Mal über das [Attributionsbedienfeld](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/panels/attribution.html?lang=de) und **Lookback-Fenster** nachdachte, wurde ich sofort an das Konzept der *Zeitreise“* erinnert; dann wurde ich natürlich auch an unsere typische Reaktion auf viele neue Tools wie diese erinnert, nämlich den Versuch, sie zu verwenden, einfach zu verschieben, weil sie so kompliziert aussehen.

Ich meine, ehrlich, schauen Sie sich nur all diese Optionen, Schalter, Bedienfelder, Auslesehilfen und Regler an.  Und ernsthaft, sprechen wir über diese komplizierten Blinklichter, Schläuche, Messgeräte… WARTE!!  Dies ist nicht die Zeit, um abgelenkt zu werden, wenn wir über Zeitmaschinen sprechen, wir haben einfach nicht die Zeit… oder tun wir das?

Ich gebe zu, dass **Attributionspanel** ein ziemlich komplexes Werkzeug ist; unsere typische Aufgabe als Analysten besteht jedoch darin, tagein, tagaus ein anderes unserer beliebtesten und hochkomplexen Tools zu verwenden, um auch einen Blick auf die Vergangenheit zu werfen. Dieses Tool heißt ***Adobe Analytics***!  Also ja, um unsere sehr wichtige Frage zu beantworten, ich glaube, diese beiden Dinge sagen, dass wir viel Zeit haben.

Warum sollten wir daher einer solchen kleinen Angst Einhalt gebieten, dass so erstaunliche, hoch entwickelte und mächtige Werkzeuge wie diese im Weg stehen, die uns buchstäblich erlauben, *rückwärts* in der Zeit zu schauen, jeden einzelnen Tag?

Schließlich - das ist ZEITREISE, Leute!!  Wir sind alle wegen solchen Dingen.  Rechts???!!

Worauf warten wir also - ein glänzendes Auto aus Metall, eine Polizeibox oder eine alte Telefonzelle, in der die Verkabelung eines alten Schirms als Antenne verwendet wird, um vor unserer Tür aufzutauchen?

Nein!  Wir haben etwas noch Besseres, also schnallen wir uns an und bleiben dran!

Nun… man versteht schon.


Jetzt, da wir alle von Zeitreisen begeistert sind, lassen Sie uns einen tiefen Atemzug nehmen, einen Schritt zurück gehen, feststellen, was das **Attributionsbedienfeld** *wirklich* ist, und die Dinge ein wenig aufschlüsseln:

![Attribution](assets/attribution.png)

*Abbildung 1: Die angezeigten Zahlen stehen inline mit dem weiter unten stehenden Text*

Überlegen Sie **Attribution** einfach, wie Ereignisse/Aktionen von einer Person, mehreren Personen oder einem der vielen verschiedenen Ereignisse im Laufe der Zeit verursacht werden können.

Laut [Adobe](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/overview.html?lang=de) können *Attribution* Analysten anpassen, wie *Dimension*-Elemente für *Erfolgsereignisse* angerechnet werden.


>[!WARNING]
>
>**Attributionsmodelle** werden so häufig mit **Marketing-Kanälen** verknüpft, dass ich im obigen Bild absichtlich *durchgestrichen* ❷ KANAL gezeigt habe, um zu veranschaulichen, dass es möglich ist, **Attribution** Analyse für fast jede andere ***Dimension*** durchzuführen.


Tatsächlich ist ein Journey-Vorgang eines Kunden nur selten wirklich linear und noch seltener vorhersehbar.  Mehr noch, jeder Kunde wird in seinem eigenen Tempo vorgehen; oft verdoppeln sie sich, bleiben stehen, fallen aus oder verhalten sich in anderem nichtlinearen Verhalten. Diese organischen Aktionen machen es schwierig oder praktisch unmöglich, die Auswirkungen von Marketing-Maßnahmen auf der gesamten Kunden-Journey zu kennen. Außerdem werden die Bemühungen zur Verknüpfung mehrerer Datenkanäle behindert.

Das ist richtig.  Lassen Sie Ihre „Domino“-Analogien vor der Tür und öffnen Sie Ihren Geist für Konzepte mehr nach dem Muster des Schmetterlingseffekts und der Stringtheorie - aber wie alles andere müssen wir mit einigen Grundlagen beginnen.

## **Attributionsmodelle**

Wenn wir das **Attributionsbedienfeld** verwenden, können wir verschiedene Dinge beobachten.  Beispielsweise zeigen uns die **Attributionsmodelle** wie unsere *Konversionen* (d. h. ❶ **Erfolgsmetriken**) auf *Treffer* in einer bestimmten Gruppe verteilt werden können.

Einfach ausgedrückt, wenn **10 Personen** einen **GROSSEN ROTEN KNOPF** drücken, um durch eine Tür zu treten, werden uns unsere **Attributionsmodelle** sagen, welche dieser **10 Personen** wir „Anerkennung“ zuweisen wollen - oder noch besser gesagt, wie *viel* „Anerkennung“ wir ihnen zuweisen wollen - für das Drücken des besagten Knopfes.

![Schaltfläche](assets/button.png)

Vor diesem Hintergrund sind hier einige Beispiele, wie sich die ❸ **Attributionsmodelle** auf diese **10 Personen auswirken**:

- **First Touch**: Dieses Modell funktioniert genau so, wie es klingt, indem es **100%** die *erste* Person, die durch die Tür ging.  Marketing-Experten verwenden diesen Ansatz eher für Taktiken wie ***Social Media*** oder ***Display***. Es ist jedoch auch eine großartige Taktik, sie häufig für die Effektivität von Produktempfehlungen auf der Site zu verwenden.
- **Letztkontakt**: Diese Taktik funktioniert auch genau so, wie sie klingt, sondern gibt stattdessen **100%** an die LETZTE Person, die durch die Tür ging.  Dieses Modell wird in der Regel verwendet, um Dinge wie ***natürliche (organische) Suche*** und andere *kurzfristige* Marketing-Zyklus-Kampagnen zu analysieren.
- **Linear**: Dieses Modell verteilt den gleichen Wert auf JEDE EINZELNE PERSON, die durch die Tür ging.

  >[!CAUTION]
  >
  >Hier ist jedoch Vorsicht geboten, da Sie das Potenzial haben, Ihre Ergebnisse bei der Anwendung dieser Taktik sehr schnell zu verbreiten, wenn Sie berücksichtigen, je länger sie läuft und je größer die Zielgruppe ist, die sie trifft.

- **U-förmig**: Dieser Ansatz weist **40%** des Kredits der *ersten Person* in der Tür zu, verteilt **20%** des Kredits auf *alle dazwischen* und gibt dann **40%** an **letzte**. Dieses Modell wird am häufigsten in Situationen verwendet, in denen Sie einen **langen Konversions-/Verkaufszyklus** mit *mehreren Touchpoints* unterwegs haben.  In diesem Fall besteht Ihr Ziel darin, in erster Linie die Marketing ***Taktiken &quot;***&quot; und &quot;***&quot;***, die zur Konversion beim Kunden beigetragen haben.
- **J**-**Shaped** und **Inverse J**:
   - Denken Sie an **U-förmig**, aber stattdessen weist dieses Modell dem *letzten Person*, der durch die Tür geht, **60%**, **20%** dem *zuerst* zu und dann *teilt* die verbleibenden **20%** über *alle anderen*.  **Umgekehrt J** macht genau das Gegenteil.

     Das Ziel hier ist es, den größten Teil des Schwerpunkts zu setzen, entweder am *Anfang* oder am *Ende* der Kampagne. Allerdings möchten Sie dem beitragenden Element am anderen Ende dennoch einen bestimmten Betrag zuweisen, während Sie die „kleinen Leute“ auf dem Weg anerkennen.

- **Zeitverfall**: Nun, ich wäre nachlässig, wenn ich dieses hier nicht teilen würde. Dieses Modell hat buchstäblich eine Halbwertszeit, die exponentiell zerfällt - mit der Zeit!  In diesem Fall beträgt der *Standard*-Parameter für die Halbwertszeit dieses Modells **7 Tage**.  Es funktioniert folgendermaßen: Wenden Sie *Gewichtung* auf jeden **Marketing-Kanal** an *basierend auf der Zeit* die nach dem *ersten Touchpoint* vergeht, wenn der Kunde konvertiert.

  **Zeitverfall** und **U-förmige Attributionsmodelle** werden normalerweise beide verwendet, um längerfristige Kampagnen zu messen. Wie Sie jedoch sehen können, haben sie geringfügig unterschiedliche Ziele, die darauf basieren, wie sie *letztendlich den Wert des Ergebnisses*.

- **Benutzerdefiniert** Sie wählen aus, wer eine Gutschrift erhalten soll.  Es ist Ihre Kampagne!

Weitere Informationen zu diesen und anderen Attributionsmodellen finden Sie [hier](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html?lang=de)

Um dies noch interessanter zu machen, lassen Sie uns über das Zurückdrehen der Uhr sprechen!

## **Lookback-Fenster**

Jetzt ist es an der Zeit, Ihren Geist auf die nächste Stufe zu bringen.  Hier fügen wir unserer Analyse buchstäblich das Element Zeitreise hinzu - und wieder beginnen wir mit den Grundlagen.

***Adobe*** definiert ❹ **Lookback-Fenster** als „die Zeit, die eine Konversion zurückblicken soll, um Touchpoints einzuschließen. Attributionsmodelle, die ersten Interaktionen mehr Gewichtung verleihen, sehen größere Unterschiede bei der Anzeige verschiedener Lookback-Fenster.“


Mit anderen Worten: **Lookback-Fenster** bestimmen den Zeitraum, in dem *Konversionen* berücksichtigt werden, und liefern *Kontext* für die Attributionsanalyse. ***Adobe Analytics*** bietet drei Typen von **Lookback-Fenstern**:

- **Besuchs-Lookback-Fenster:** Sucht nach dem Beginn eines ***Besuchs***, als eine Konversion stattfand, und bietet Einblicke in die direkten Interaktionen, die zu Konversionen führten.

  Denken Sie daran, dass dies normalerweise das kürzeste **Lookback-Fenster** ist.
- **Besucher-Lookback-Fenster:** Zeigt alle ***Besuche*** bis zum ersten Tag des Monats innerhalb des ausgewählten **Datumsbereichs** an, bietet einen wesentlich breiteren Überblick über die Kundeninteraktionen und hilft bei der Identifizierung von Mustern im Zeitverlauf.
- **Benutzerdefiniertes Lookback-Fenster:** Ermöglicht Ihnen, das **Attributionsfenster** über den **Datumsbereich** hinaus auf *maximal* **90 Tage zu**.  Sie bietet *Flexibilität* bei der Erfassung von Touchpoints, *außerhalb* ausgewählten **Datumsbereichs)**, um eine umfassende Analyse sicherzustellen.

Durch die Anpassung eines bestimmten **Lookback-Fensters** können Analysten dann die Auswirkungen eines oder mehrerer Touchpoints innerhalb bestimmter Zeitrahmen untersuchen und größere Einblicke in die Frage erhalten, wie verschiedene Zeiträume sich auf die Attributionsergebnisse auswirken.

## **Alles zusammenbringen**

Was bedeutet das nun für uns Analysten?

Das **Attributionsbedienfeld** und **Lookback-Fenster** geben uns die Möglichkeit, über die banalen Daten auf Oberflächenebene hinauszublicken und tiefer in die Kunden-Journey einzutauchen. Indem wir verstehen, welche Touchpoints die größte Auswirkung auf *Konversionen* hatten, können wir fundierte Entscheidungen über unsere Marketing-Strategien treffen und Ressourcen effektiver zuweisen.

Denken Sie daran, dass Sie nach der Auswahl **Attributionsmodelle** und **Lookback-Fenster** Ihre Daten noch weiter bearbeiten können, indem Sie sie mit einem ❺ (Segment **,** oder einer anderen Komponente filtern, die Sie an dieser Stelle benötigen.  Darüber hinaus stehen Ihnen nach dem Rendern des Bedienfelds alle Funktionen einer herkömmlichen Workspace zur Verfügung.

## **Endlich in die Praxis umsetzen**

Jetzt, da Sie die Konzepte haben, stellen Sie sich vor, Sie führen eine Marketing-Kampagne aus und versuchen herauszufinden, welcher Kanal der *effektivste* um Konversionen zu fördern. Mithilfe des **Attributionsbedienfelds** können Sie nicht nur den **Letztkontakt**, sondern auch den **Erstkontakt**, **Selber Kontakt** und jedes andere **Modell** sehen, welche **Kanäle** die *effektivsten* zur Steigerung Ihrer *Konversionen*. Diese Informationen können dann verwendet werden, um Ihre Kampagnen *zu optimieren* und die Gesamtleistung zu verbessern, indem Sie einfach die Uhr mit dem **Lookback-Fenster** Ihrer Wahl zurückdrehen.

Nachdem Sie nun gesehen haben, was sie kann, lassen Sie sich nicht von den scheinbar komplexen Funktionen des Attributionsbedienfelds täuschen oder einschüchtern.  **Stell dich der Sache**.  *Umarme*.  **Verstehen**.
ABER VOR ALLEM - *Nutzen Sie es zu Ihrem Vorteil.* Das **Attributionsbedienfeld** und **Lookback-Fenster** sind die Schlüssel für ein tieferes Verständnis Ihrer Kundinnen und Kunden und deren Journey mit Ihrer Marke.

Jetzt können wir mit Zuversicht &quot;[zurück in der Zeit](https://youtu.be/gVryJmZNFdU) reisen und die Leistung unserer vertrauenswürdigen Zeitmaschine (auch bekannt als ***Adobe Analytics***) nutzen, um datengesteuerte Entscheidungen zu treffen.

## Autor

Dieses Dokument wurde verfasst von:

![Jeff Bloomer](assets/jeff-headshot.png)

**Jeff Bloomer**, Manager, Digital Analytics bei Kroger Personal Finance

Adobe Analytics-Expertin
