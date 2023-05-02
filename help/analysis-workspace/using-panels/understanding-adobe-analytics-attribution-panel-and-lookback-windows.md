---
title: Grundlegendes zu Adobe Analytics Attribution Panel & Lookback Windows
description: Erfahren Sie, wie Sie mit dem Attributionsbedienfeld und dem Lookback-Fenster das Kundenverhalten verstehen und anpassen können, wie Dimensionselemente Erfolgsereignissen zugeschrieben werden.
feature: Attribution
role: User
level: Experienced
doc-type: Article
last-substantial-update: 2023-05-02T00:00:00Z
jira: KT-13181
thumbnail: KT-13181.jpeg
source-git-commit: d7b1fac5c98080f9ca786ea21a3700d2937c7ebc
workflow-type: tm+mt
source-wordcount: '1883'
ht-degree: 2%

---


# Grundlegendes zu Adobe Analytics Attribution Panel &amp; Lookback Windows

Erfahren Sie, wie Sie mit dem Attributionsbedienfeld und dem Lookback-Fenster das Kundenverhalten verstehen und anpassen können, wie Dimensionselemente Erfolgsereignissen zugeschrieben werden.

## Verwenden des Bedienfelds „Attribution 

![Delorean](assets/delorean.png)

&quot;Großer Schottland!&quot;

Sobald ich an die [Attributionsbereich](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/panels/attribution.html) und **Lookback-Fenster**, wurde ich an das Lied &quot;Back in Time&quot; von Huey Lewis und den News erinnert. Dann wurde ich natürlich auch daran erinnert, dass unsere typische Antwort auf viele neue Werkzeuge wie diese einfach darin besteht, den Versuch zu verzögern, sie zu verwenden, weil sie so kompliziert aussehen.

Ich meine wirklich, schauen Sie sich all diese Optionen an, Schalter, Bedienfelder, Auslesungen und Knöpfe.  Und im Ernst, lassen Sie uns über diesen Flusskondensator sprechen.  Warte, habe ich gerade einen Flusskondensator gesagt?

Okay, ich gebe die **Attributionsbereich** ist ein recht komplexes Instrument; Unsere typische Aufgabe als Analysten besteht jedoch darin, Tag für Tag ein sehr komplexes Tool zu verwenden, um zu sehen, was in der Vergangenheit passiert ist.  Dieses Tool heißt **Adobe Analytics**!

Warum sollten wir es also zulassen, dass so etwas wie eine kleine Angst einem solch coolen und mächtigen Werkzeug im Weg steht, das es uns ermöglicht, jeden Tag buchstäblich rückwärts in der Zeit zu schauen?

Wir haben es mit diesem Zeug zu tun, oder?  Richtig??!! (Ich meine, c&#39;mon, ich bin mir ziemlich sicher, dass es immer noch in Ordnung und &quot;politisch korrekt&quot; ist, uns Geeks zu nennen.)

Ach, wem kümmert es?  Techies, Geeks, Nerds, Goober, Dweebs und Techies (ja, sogar die Trekkies), kann ich jetzt die Autostereoanlage hören:

&quot;Nimm mich weg, es macht mir nichts aus!  Aber du versprichst mir besser... Ich werde rechtzeitig zurückkommen!&quot;

Ich habe deine Aufmerksamkeit, nicht wahr?  Großartig!


Lasst uns die Dinge ein wenig zerbrechen.  Jetzt, da wir alle aufgeregt sind **Zeitreisen**, nehmen wir einen Schritt zurück und stellen fest, was die **Attributionsbereich** ist wirklich:

![Zeitsteuerung](assets/time-control.gif)

Nein, nein, nein, nein, nein!  Lassen Sie uns noch nicht ablenken!  Versuchen wir es vielleicht noch einmal:

![Attributionsfenster](assets/attribution-window.png)

In **Attribution** berücksichtigen Sie einfach, wie Ereignisse/Aktionen von einer Person, mehreren Einzelpersonen oder einer oder mehreren verschiedenen Elementen im Laufe der Zeit verursacht werden können.

Gemäß [Adobe](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/component-settings/attribution.html)bietet die Attribution Analysten die Möglichkeit, anzupassen, wie Dimensionselemente Erfolgsereignissen zugeschrieben werden.  Tatsächlich ist kein Kunde wirklich linear und ist weniger oft vorhersehbar.  Außerdem wird jeder Kunde in seinem eigenen Tempo fortfahren. häufig können sie sich verdoppeln, anhalten, aussteigen oder sich in einem anderen nicht-linearen Verhalten engagieren. Diese organischen Aktionen machen es schwierig oder praktisch unmöglich, die Auswirkungen von Marketingmaßnahmen auf die Journey zu kennen. Außerdem werden die Bemühungen zur Verknüpfung mehrerer Datenkanäle behindert.

Klingt dir irgendwas davon bekannt?  Denken Sie im Zusammenhang mit Marty McFly&#39;s Journey darüber nach:

![Zurück zur Zukunft 1](assets/back-to-the-future1.png)![Zurück zur Zukunft 2](assets/back-to-the-future2.png)

Von dem Moment, als er aus dem Parkplatz &quot;Twin Pines Mall&quot;flog, bis er sich buchstäblich aus der &quot;DeLorean&quot;warf, bevor er von einer 210-Tonnen-Lokomotive verdrängt wurde, scheint alles andere als linear, und es ist nichts, was jeder vorhersagen konnte.

Doch durch die Macht der Filmmagie können wir Marty mit der Zeit folgen und all seine Touchpoints, seine Stände, Doppelkappen und Ausfälle verstehen.

## Attributionsmodelle

In der Praxis können wir die **Attributionsbereich** um mehrere verschiedene Dinge zu sehen.  Beispielsweise wird die **Attributionsmodelle** Zeigen Sie uns, wie unsere **Konversionen** verteilt sind **Treffer** in einer bestimmten Gruppe.

Einfach gesagt, wenn 10 Leute auf einen Knopf drücken, um durch eine Tür zu gehen, werden unsere Attributionsmodelle uns sagen, welche von diesen 10 Leuten wir für das Drücken dieses Knopfes anschreiben wollen.  In diesem Zusammenhang finden Sie einige Beispiele dafür, wie sich die Attributionsmodelle auf diese 10 Personen auswirken können:
* **Erstkontakt**: Dieses hier klingt genau so.  In diesem Fall werden der ersten Person, die durch die Tür ging, 100 % zugeschrieben.  Daher verwenden Marketingexperten diese eher für Taktiken wie Social oder Display, aber sie sind häufig eine großartige Taktik für die Effektivität von Produktempfehlungen vor Ort.
* **Letztkontakt**: Auch genau wie es klingt.   Mit diesem Modell werden der letzten Person, die die Tür betritt, 100 % zugeschrieben.  Dieses Modell wird häufig verwendet, um Dinge wie Such- und kurzfristige Marketingzykluskampagnen zu analysieren.
* **Linear**: Das gibt jeder Person, die durch die Tür ging, die gleiche Anerkennung.  Das ist richtig - man bekommt einen DeLorean, und man bekommt einen DeLorean, und man bekommt einen DeLorean.  JEDER WIRD EIN DELOREAN!!!
* **U-förmig**: Diese vergibt 40% des Kredits an die erste in der Tür, verteilt 20% des Kredits an alle dazwischen und gibt dann 40% an die letzte bis.  Denken Sie an eine Situation, in der Sie die Mehrheitskonversionen sowohl im Front- als auch im Backend erkennen möchten, aber auch einen kleinen Teil der Gewichtung zwischen einigen der beitragenden Interaktionen darauf ablegen möchten.
* **Zeitverfall**: Ich würde es vermissen, wenn ich dieses nicht mit Ihnen teilen würde, bevor ich Sie an die offizielle Dokumentation schicke, um die verbleibenden Modelle zu überprüfen.  Wie das Plutonium von Doc Brown hat dieses Modell buchstäblich eine Halbwertszeit, die exponentiell abnimmt!  In diesem Fall beträgt der Standardparameter für die Halbwertszeit dieses Modells 7 Tage.  Die Funktionsweise besteht darin, die Gewichtung auf jeden Marketing-Kanal anzuwenden, basierend auf der Zeit, die nach dem ursprünglichen Touchpoint vergeht, und dem Zeitpunkt, zu dem der Kunde konvertiert.

Weitere Informationen hierzu und den übrigen **Attributionsmodelle**, [Hier klicken](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html?lang=de).

Um das noch interessanter zu machen, sprechen wir über die **Lookback Windows**.

Ja, hier gehen wir - nehmen Sie uns ZEIT zurück!  Denn hier beginnt der Spaß!

Adobe definiert **Lookback Windows** als &quot;die Zeit, die eine Konversion zurückblicken sollte, um Touchpoints aufzunehmen. Attributionsmodelle, die der ersten Interaktion mehr Gewicht zuschreiben, sehen bei der Anzeige verschiedener Lookback-Fenster größere Unterschiede.&quot;

* **Besuchs-Lookback-Fenster**: Blickt bis zum Beginn eines Besuchs zurück, wenn eine Konversion stattgefunden hat
* **Besucher-Lookback-Fenster**: Betrachtet alle Besuche bis zum 1. des Monats des aktuellen Datumsbereichs.
* **Benutzerdefiniertes Lookback-Fenster**: Ermöglicht Ihnen, das Attributionsfenster über den Datumsbereich des Berichts hinaus auf ein Maximum von **90 Tage**.

Wenn Sie alle &quot;Back to the Future&quot;-Filme gesehen haben, dann wissen Sie, dass Marty McFly mehr als einmal in der Zeit zurückging, und Sie wissen auch, dass er mehr als einmal mehr ins Jahr 1955 zurückgekehrt ist.  Wenn wir von der Akquisition von &quot;Gray&#39;s Sports Almanac&quot;als Konversionsereignis abhängig sind, beachten Sie Folgendes:

![Sportalmanac](assets/sports-almanac.png)

1. Ein bisschen früher **1:30 Uhr** on **26. Oktober 1985**, Marty McFly kehrt in der Zeit zurück zu **5. November 1955**, wo er zum ersten Mal über einen Kiefernbaum in einer zeitreisenden DeLorean läuft.  In den nächsten anderthalb Wochen interagiert er mit mehreren Leuten, einschließlich seiner Eltern, die letztlich die Zukunft beeinflussen, indem er seinen Vater dazu bringt, einem Bullen namens Biff standzuhalten, sodass sein Vater sein eigenes Potenzial erkennen kann, ein erfolgreicher Autor von Science-Fiction zu werden.
1. Später am selben Morgen am **26. Oktober 1985** Dr. Emmett Brown kommt auf Marty McFly&#39;s Einfahrt, um ihn und seine Freundin darüber zu informieren, dass etwas mit ihren Kindern schrecklich schiefgelaufen ist und sie müssen sich in die Zukunft begeben, um ihre Probleme zu lösen.  Während sie abreisen, wird ihre Abreise von Biff gesehen, der es seltsam findet, einen fliegenden DeLorean zu sehen.  Später, als Biff wieder Zeuge eines fliegenden DeLorean ist und später &quot;zwei Versionen&quot;von Marty erblickt, beginnt er, Dinge zusammenzufassen.   Als er Doc Brown und Marty mit dem Argument überhört, wie die &quot;Zeitmaschine&quot;nie für persönliche Gewinne und nur für die Forschung verwendet werden sollte (weil Marty sich über die Rückführung eines Sportalmanaks in die Vergangenheit gekümmert hatte, um einige persönliche Wetten zu tätigen), stiehlt Biff die Zeitmaschine, während die beiden abgelenkt werden, den Sportalmanac in der Vergangenheit an sein jüngeres Selbst zu liefern.
1. Nach ihrer Reise in die Zukunft kehren Doc Brown und Marty zu einem **26. Oktober 1985** sie erkennen nicht, und sie glauben, dass die Zeitpläne von einem bösen Biff verändert wurden.  In dem Bewusstsein, dass sie das, was geschehen ist, beheben müssen, beschließen Doc und Marty, zu **12. November 1955**, die schicksalhafte Nacht, in der Marty bei seinem ersten Besuch alles geändert hat **1955**.  Doc und Marty retten letzten Endes den Tag, indem sie den Sportalmanac, den Old Biff von der Zukunft an Young Biff in geliefert hatte, zurückstehlen **1955**, aber nicht ohne eine weitere Wendung müssen Sie wirklich die vollständige Trilogie der Filme zu sehen, um wirklich genießen und verstehen.

Je nach **Attributionsmodell** und **Lookback-Fenster** können wir am Ende einige interessante Szenarien sehen:

* Verwenden **Erstkontakt** und **Besuchs-Lookback-Fenster**, Attribution betrachtet Marty&#39;s Besuch, bei dem die letzte &quot;Konversion&quot; stattgefunden hat, bei der es ihm und Doc gelingt, den Sportalmanac von Young Biff zurück zu stehlen und seine Aversion gegen Dung aufrecht zu erhalten.

![Biff 1](assets/biff1.png)![Biff 2](assets/biff2.png)

* Ob Sie es glauben oder nicht, verwenden Sie **Erstkontakt** und **Besucher-Lookback-Fenster**, würde die Attribution die Konversion begünstigen, bei der Biff letztlich gewinnt.
* Anwenden einer **lineares Lookback-Fenster** würde zu einem Multiversum führen, in dem jede Timeline existiert.  Tut mir leid, das ist nicht **Marvel** oder **Star Trek**!

Und an diesem Punkt hoffe ich, dass Sie beginnen, die Idee zu bekommen.

Was bedeutet das also für uns als Analysten?

Die **Attributionsbereich** und **Lookback-Fenster** geben Sie uns die Macht, über die einfachen, oberflächlichen Daten hinaus zu schauen und tiefer in die Journey zu tauchen. Indem wir verstehen, welche Touchpoints den größten Einfluss auf Konversionen hatten, können wir fundierte Entscheidungen über unsere Marketing-Strategien treffen und Ressourcen effektiver zuweisen.

Denken Sie daran, nachdem Sie Ihre **Attributionsmodelle** und **Lookback Windows** ausgewählt haben, können Sie Ihre Daten weiterhin weiter bearbeiten, indem Sie sie mit einem Segment oder einer anderen Komponente filtern, die Sie möchten.  Außerdem verfügen Sie nach dem Rendern des Bedienfelds über alle Funktionen eines herkömmlichen **Arbeitsbereich**, was bedeutet, dass Sie offiziell für 88 mph fahren dürfen!

## Letztere in die Praxis umsetzen

Nachdem Sie nun die Konzepte festgelegt haben, stellen Sie sich vor, Sie führen eine Marketing-Kampagne durch und versuchen zu ermitteln, welcher Kanal am effektivsten für Konversionen geeignet ist. Mithilfe des **Attributionsbereich**, können Sie nicht nur die **Letztkontakt**, aber auch **Erstkontakt**, **Selber Kontakt** und jedes andere Modell, das Sie auswählen, um zu bestimmen, welche Kanäle am effektivsten zur Förderung Ihrer Konversionen beitragen. Diese Informationen können dann zur Optimierung Ihrer Kampagnen und zur Verbesserung der Gesamtleistung verwendet werden.

Nachdem Sie nun gesehen haben, was es tun kann, lassen Sie sich nicht von den scheinbar komplexen Merkmalen der **Attributionsbereich**.  **Gesicht** es.  **Embrace** es.  **Grundlegendes** es.  Vor allem sollten Sie es zu Ihrem Vorteil nutzen. Die **Attributionsbereich** und **Lookback-Fenster** sind die Schlüssel, um ein tieferes Verständnis Ihrer Kunden und ihrer Journey mit Ihrer Marke zu gewinnen.

Jetzt können wir &quot;zurück in die Zeit&quot; reisen, mit Sicherheit und mit der Kraft unserer Trustischen Zeitmaschine (alias,  **Adobe Analytics**) datengestützte Entscheidungen zu treffen; Und, was am wichtigsten ist, erinnern Sie sich: &quot;Wo wir hingehen, brauchen wir keine Straßen!&quot; (Nur ein Flusskondensator und ein scharfer Blick für die Attribution!)

![Zurück in die Zukunft](assets/back-to-the-future3.png)

## Autor

Dieses Dokument wurde verfasst von:

![Jeff Bloomer](assets/jeff-headshot.png)

**Jeff Bloomer**, Manager, Digital Analytics bei Kroger Personal Finance

Adobe Analytics-Experte
