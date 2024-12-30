---
title: Heben Sie Ihre Datenanalyse mit berechneten Metriken auf die nächste Stufe
description: Erfahren Sie, wie Fachleute berechnete Metriken verwenden, um neue Metriken zu erstellen, ohne ihre Implementierung zu ändern, und wie sie bereits erfasste Daten verwenden, um komplexe Geschäftsfragen zu beantworten.
feature: Calculated Metrics
role: User
level: Beginner
doc-type: Article
last-substantial-update: 2023-05-16T00:00:00Z
jira: KT-13266
thumbnail: KT-13266.jpeg
exl-id: 74793149-9967-4765-832c-c65e578ee34b
source-git-commit: d95136a21c08312a81baba7673cb7135270af4bd
workflow-type: tm+mt
source-wordcount: '1583'
ht-degree: 3%

---

# Heben Sie Ihre Datenanalyse mit berechneten Metriken auf die nächste Stufe

Die meisten neuen Benutzer von Adobe Analytics kennen Segmente als eine Möglichkeit, ihre Daten in Scheiben zu schneiden. Heute möchte ich Ihnen berechnete Metriken vorstellen, das nächstbeste Tool in Ihrer Analyst-Toolbox.

Als erweiterte Funktion von Adobe Analytics können Sie mit berechneten Metriken neue Metriken erstellen, ohne Ihre Implementierung mithilfe der bereits erfassten Daten zu ändern. Der Generator für berechnete Metriken kann viele verschiedene mathematische und statistische Funktionen verwenden, sodass Sie Metriken erstellen können, die auch die komplexesten Geschäftsfragen beantworten.

## Erste Schritte mit berechneten Metriken

Um mit berechneten Metriken zu beginnen, sehen wir uns ein einfaches Beispiel an. Angenommen, Sie möchten verstehen, ob Online-Self-Service-Benutzer einen höheren durchschnittlichen Bestellwert (AOV) haben als anrufunterstützte Benutzer. Gehen Sie wie folgt vor, um eine berechnete Metrik zur Beantwortung dieser Frage zu erstellen:

Um den Generator für berechnete Metriken zu öffnen, klicken Sie in der oberen Navigationsleiste auf → **Komponenten** → **Berechnete Metriken** → **+ Hinzufügen.** Sie können auch auf das **+-** über **Metriken** im Bedienfeld „Komponenten“ klicken.


![Kalkulation 01](assets/calc01.png) ![Kalkulation 02](assets/calc03.png) ![Kalkulation 03](assets/calc02.png)

![Kalkulation 04](assets/calc04.png)

*Unten stehende Beschreibungen für Elemente der Benutzeroberfläche*

Nachdem der Generator für berechnete Metriken geöffnet wurde, fügen Sie hinzu und/oder führen Sie die folgenden Schritte aus:

**A.** Ein Name für Ihre berechnete Metrik. Dieser Name wird in der Komponentenliste für Metriken angezeigt. Achten Sie daher darauf, dass Sie und andere ihn klar erkennen können, z. B *„Call Center AOV*.

**B.** Eine Beschreibung der berechneten Metrik. **Diese Beschreibung wird angezeigt, wenn Benutzer in der Komponentenliste neben** Metrik auf „i“ klicken. Vergewissern Sie sich also, dass sie informativ ist. Beispiel: Für die Call-Center-AOV können wir hinzufügen *Berechnet die AOV für Call-Center-unterstützte Bestellungen*.

**C.** Das Metrikformat: Wählen Sie Dezimal, Zeit, Prozent oder Währung und fügen Sie Dezimalstellen und Polarität hinzu. Hier wählen wir *Währung für das Format, 0 für die Anzahl der Dezimalstellen und* ⬆ *Gut (Grün) für die Polarität.*

**D**. Wenn Sie Tags verwenden, mit denen Sie Themen anwenden und berechnete Metriken schnell finden können, fügen Sie die Tags hinzu, die hier gelten. Wir haben Tags *AOV* und *Callcenter* hinzugefügt.

**E.** Dieser Abschnitt dient zur Anzeige - wenn Sie Ihre berechnete Metrik in Abschnitt F erstellen, wird die Formel hier angezeigt.

**F.** Ziehen Sie Dimensionen (H), Metriken (I) oder Segmente (J) per Drag-and-Drop in dieses Feld, um Ihre berechnete Metrik sowie die Operatoren für die Formel zu erstellen. Wenn Sie für jede Metrik auf das Zahnrad klicken, können Sie den Metriktyp (Standard/Gesamt) und das Attributionsmodell ändern. *Wir ziehen die Einnahmen aus dem Callcenter per Drag-and-Drop und darunter* wir÷￼*. Wir akzeptieren den standardmäßigen Metriktyp und das Attributionsmodell.*

**G**. Verwenden Sie diese **+Hinzufügen**-Option, um zusätzliche Bedingungen oder statische Zahlen hinzuzufügen, die wir hier nicht benötigen.

**K.** Und schließlich, während Sie Ihre Berechnung erstellen, können Sie hier eine Vorschau der Daten der letzten 90 Tage anzeigen.

Nachdem wir nun Call Center AOV erstellt haben, benötigen wir auch eine berechnete Metrik für Online-AOV. Wir würden dies in den oben beschriebenen Schritten tun.

Als Nächstes können wir eine dritte berechnete Metrik erstellen, entweder mit dem Generator für berechnete Metriken oder spontan innerhalb der Freiformtabelle, um das Callcenter und die Online-AOV zu vergleichen, sodass wir am Ende so etwas wie das Folgende erhalten:

![Kalkulation 05](assets/calc05.png)

In unserem Beispiel sehen wir eine erhebliche Steigerung, wenn Käufer das Callcenter verwenden, um ihnen beim Kauf zu helfen. Diese Daten können dann als Grundlage für unsere Entscheidungen dienen, wie Kunden bei ihren Käufen unterstützt werden können, z. B. durch Popup-Angebote oder andere geführte Erlebnisse.

## Verwenden von Segmenten in berechneten Metriken

Sehen wir uns nun an, wie wir Segmente in berechneten Metriken verwenden können, um mehr Einblick in das Kundenverhalten, die Vorlieben und die Motivation zu erhalten. Mit Segmenten und berechneten Metriken können wir ausreichend über Kunden erfahren, um ihre Erlebnisse zu verbessern, den Umsatz zu steigern und die Kundenzufriedenheit und -loyalität zu verbessern.

Aus den obigen AOV-Beispielen wissen wir bereits, dass Callcenter-unterstützte Käufe in der Regel eine höhere AOV haben. Andere Metriken zeigen jedoch, dass die meisten Benutzer das Callcenter nicht für Käufe verwenden.

Welche Einzelhandelskategorien - und Nutzerpfade durch diese Kategorien - führen also zur höchsten AOV?  Das können wir herausfinden, indem wir Segmente mit berechneten Metriken kombinieren.

Dazu müssen wir zunächst für jede Produktkategorie Segmente auf Besuchsebene *einschließen* und *ausschließen* erstellen. Ein- oder Ausschließen wird durch Klicken auf das **Optionen**-Zahnrad in der rechten Ecke des Containers festgelegt. Der Standardwert ist „Einschließen“.

![Kalkulation 06](assets/calc06.png) ![Kalkulation 07](assets/calc07.png)

Nachdem wir diese Segmente erstellt haben, können wir eine berechnete Metrik erstellen, um Ihnen die Antwort auf Ihre Frage zu geben. Wir öffnen den Generator für berechnete Metriken und gehen wie folgt vor:

1. Suchen Sie nach den neu erstellten Segmenten und ziehen Sie die gewünschten Segmente per Drag-and-Drop in den grauen Bereich am oberen Rand des Felds **Definition**. Wenn wir beispielsweise eine AOV für Benutzende erstellen möchten, die sowohl die Kategorien „Damen“ als auch „Herren“, nicht aber „Kinder“ besucht haben, können wir diese drei Segmente per Drag-and-Drop in diesen Bereich ziehen: ** &quot;*Herren einschließen* und *Kinder ausschließen*. Wir nennen das *Stapelung von Segmenten*.

   ![Kalkulation 09](assets/calc09.png) ![Kalkulation 08](assets/calc08.png)

1. Anschließend ziehen wir die Metrik **Online-Umsatz** in denselben Container und **dann „Online-Bestellungen**. Da Container wie mathematische Ausdrücke funktionieren, um die Reihenfolge der Vorgänge zu bestimmen, werden Elemente in Containern vor nachfolgenden Prozessen verarbeitet, obwohl wir in dieser Berechnung nicht mehrere Container oder Prozesse haben.
1. Wir ändern den Operator zwischen den beiden Metriken in Division (÷).
1. Wir wählen **Währung** als Format, **0** Dezimalstellen und **UP** für die Polarität aus.
1. Benennen Sie die berechnete Metrik und geben Sie eine Beschreibung ein.
1. Speichern Sie.

Wenn wir fertig sind, sieht unsere berechnete Metrik wie folgt aus:

![Kalkulation 10](assets/calc10.png)

Nachdem wir für jede Journey-Kombination der Besucherkategorie berechnete Metriken mit gestapelten Segmenten erstellt und uns die Daten angesehen haben, sollten Sie sich ansehen, was wir daraus lernen! Benutzer, die während ihres Besuchs sowohl die Kategorien „Damen“ als auch „Herren“ besuchen, haben die höchsten AOV-Werte. Im Vergleich zu Besuchern einer einzigen Kategorie ist der Anstieg bedeutend:

![Calc 11](assets/calc11.png) ![Calc 12](assets/calc12.png)

Mit diesem Wissen können wir das Seitenlayout, Produktplatzierungen und Werbebotschaften optimieren, um mehr Personen in diese Kategorien zu bringen, bevor Sie das Produkt auschecken.

## Wertvoll, aber nicht überall verfügbar

**Also - Berechnete Metriken, sowohl einfache als auch komplexe, sind für Analysten äußerst wertvoll!**

Diese Metriken sind jedoch nicht in allen Bereichen von Adobe Analytics verfügbar. Berechnete Metriken können nicht in verwendet werden:

- Fallout in Analysis Workspace
- Kohortenanalyse in Analysis Workspace
- Data Warehouse
- Echtzeitberichte
- Aktuelle Datenberichte
- Analytics for Target
- Report Builder

## Best Practices für berechnete Metriken

Nachdem Sie nun wissen, wie wertvoll berechnete Metriken sein können, werfen wir einen Blick auf einige Best Practices bei ihrer Erstellung.

1. **Überprüfen Sie die Syntax Ihrer Formel.** Stellen Sie sicher, dass die Formelsyntax korrekt ist und der Adobe Analytics-Syntax entspricht, um sicherzustellen, dass Sie aussagekräftige Informationen erhalten.
1. **Überprüfen Sie die Reihenfolge der Vorgänge.** Achten Sie darauf, Container sorgfältig zu verwenden und die Dinge in die richtige mathematische Reihenfolge der Vorgänge zu bringen.
1. **Daten nicht doppelt zählen**. Sie können eine doppelte Zählung von Daten vermeiden, indem Sie sicherstellen, dass die in der berechneten Metrik verwendete Formel dieselben Daten nicht mehrmals zählt. Dies wird häufig durch die Kombination von *Einschließen* und *Ausschließen* in der berechneten Metrik oder durch die Verwendung von Segmenten erreicht.
1. **Überprüfen Sie die Zeitgranularität.** Stellen Sie sicher, dass die berechnete Metrik dieselbe Zeitgranularität wie die in der Formel verwendeten Quellmetriken hat.
1. **Präzise Daten verwenden** Sie erhalten nur dann wertvolle Ergebnisse, wenn Sie bei der Berechnung genaue und zuverlässige Daten verwenden.

## Best Practices für benutzerdefinierte Segmente

Beachten Sie beim Erstellen von Segmenten in Adobe Analytics die folgenden Best Practices:

1. **Einfach halten.** vermeiden Sie eine Überkomplikation des Segments. Halten Sie es so einfach wie möglich und verwenden Sie nur die Bedingungen, die für die Genauigkeit erforderlich sind.
1. **Verwenden Sie die richtigen Container-Typen**. Stellen Sie sicher, dass Sie den richtigen Container-Typ - Besucher, Besuch oder Treffer - in der Segmentdefinition verwenden, um falsche Ergebnisse zu vermeiden.
1. **Daten nicht doppelt zählen**. Stellen Sie wie bei berechneten Metriken sicher, dass das Segment nicht mehrmals dieselben Daten zählt. Container ein- und ausschließen können hilfreich sein.
   1. Wenn ein Include-Container verwendet wird, *er* umfasst *den gesamten Inhalt des Besuchs* wenn ein Treffer der Bedingung innerhalb des Besuchs entspricht.
   1. Wenn ein Ausschluss-Container verwendet wird, wird *der gesamte Inhalt des Besuchs ausgeschlossen* wenn ein Treffer der Bedingung innerhalb des Besuchs entspricht.
1. **Container ordnungsgemäß**. Bestimmen Sie mithilfe des äußersten Containers, welche Daten enthalten sind, und wenden Sie dann verschachtelte Regeln auf die verbleibenden Daten an. Wenn verschachtelte Regeln angewendet werden, fungiert der Segmentfluss als Trichter, und nachfolgende Regeln gelten nicht für Treffer, die durch die erste Regel ausgeschlossen wurden.
1. **Stellen Sie sicher, dass Ihre Daten auf dem neuesten Stand sind.** Stellen Sie sicher, dass Sie genaue und aktuelle Daten in der Segmentdefinition verwenden, um genaue Ergebnisse zu erhalten.
1. **Testen Sie das Segment.** Testen Sie das Segment immer, um sicherzustellen, dass es wie beabsichtigt funktioniert, bevor Sie es für andere freigeben.
1. **Betrachten Sie die Leistung.** Segmente können die Berichtsverarbeitung verlangsamen. Beachten Sie daher diese Auswirkungen beim Erstellen.

## Wichtige Schlussfolgerungen

Die Kombination von Segmenten und berechneten Metriken in Adobe Analytics kann auf jeden Fall zu einer robusteren und effektiveren Datenanalyse führen. Indem Sie Ihre Daten aufteilen und Berechnungen für einen Vergleich erstellen, können Sie tiefere Einblicke in das Kundenverhalten gewinnen, mit dem Sie Ihre Marketing-Kampagnen optimieren und maßgeschneiderte Dashboards und Berichte erstellen können. Beachten Sie jedoch, dass berechnete Metriken nicht in allen Bereichen von Adobe Analytics verfügbar sind, und stellen Sie sicher, dass Sie die Best Practices befolgen, um sicherzustellen, dass Sie genaue und nützliche Daten erhalten.


## Autor

Dieses Dokument wurde verfasst von:

![Debbie Kern](assets/calc13.jpeg)

**Debbie Kern**, Senior Adobe Analytics Manager bei Adswerve

![adSwerve](assets/calc14.png)
