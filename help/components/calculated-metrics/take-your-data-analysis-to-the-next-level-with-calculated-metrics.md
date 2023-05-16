---
title: Mit berechneten Metriken können Sie Ihre Datenanalyse auf die nächste Ebene bringen.
description: Erfahren Sie, wie ein Experte mithilfe von berechneten Metriken neue Metriken erstellt, ohne die Implementierung zu ändern, und bereits erfasste Daten verwendet, um komplexe Geschäftsfragen zu beantworten.
feature: Calculated Metrics
role: User
level: Beginner
doc-type: Article
last-substantial-update: 2023-05-16T00:00:00Z
jira: KT-13266
thumbnail: KT-13266.jpeg
source-git-commit: c64f2fde1b91edd9f3d6c0f87aa889ed2c613d9b
workflow-type: tm+mt
source-wordcount: '1566'
ht-degree: 1%

---


# Mit berechneten Metriken können Sie Ihre Datenanalyse auf die nächste Ebene bringen.

Die meisten neuen Benutzer von Adobe Analytics sind mit Segmenten vertraut, um ihre Daten zu zerteilen und zu würzen. Heute möchte ich Ihnen die berechneten Metriken vorstellen, das nächste beste Tool in Ihrer Analyse-Toolbox.

Als erweiterte Funktion von Adobe Analytics können Sie mit berechneten Metriken neue Metriken erstellen, ohne Ihre Implementierung mithilfe der bereits erfassten Daten zu ändern. Der Generator für berechnete Metriken kann viele verschiedene mathematische und statistische Funktionen verwenden, sodass Sie Metriken erstellen können, die selbst die komplexesten Geschäftsfragen beantworten.

## Erste Schritte mit berechneten Metriken

Sehen wir uns ein einfaches Beispiel an, um mit berechneten Metriken zu beginnen. Stellen Sie sich vor, Sie möchten verstehen, ob Online-Self-Service-Benutzer einen höheren durchschnittlichen Bestellwert haben als anrufunterstützte Benutzer. Gehen Sie wie folgt vor, um eine berechnete Metrik zur Beantwortung dieser Frage zu erstellen:

Um den Generator für berechnete Metriken zu öffnen, klicken Sie in der oberen Navigation auf → **Komponenten** → **Berechnete Metriken** → **+ Hinzufügen.** Sie können auch auf die **+ sign** above **Metriken** im Bereich &quot;Komponenten&quot;.


![Calc 01](assets/calc01.png) ![Calc 02](assets/calc03.png) ![Calc 03](assets/calc02.png)

![Calc 04](assets/calc04.png)

*Nachstehende Beschreibungen für UI-Elemente*

Nachdem der Generator für berechnete Metriken geöffnet wurde, fügen Sie Folgendes hinzu und/oder führen Sie die folgenden Schritte aus:

**A.** Ein Name für Ihre berechnete Metrik. Dieser Name wird in der Liste der Metrikkomponenten angezeigt. Machen Sie es daher für Sie und andere klar, z. B. *Callcenter-AOV*.

**B.** Eine Beschreibung der berechneten Metrik. Diese Beschreibung wird angezeigt, wenn Benutzer auf &quot;**i**&#39; neben der Metrik in der Komponentenliste, also stellen Sie sicher, dass sie informativ ist. Beispielsweise könnten wir für Call Center AOV *Berechnet AOV für vom Callcenter unterstützte Bestellungen*.

**C.** Das Metrikformat: Wählen Sie Dezimalzahl, Zeit, Prozent oder Währung aus und fügen Sie Dezimalstellen und Polarität hinzu. Hier wählen wir *Währung für das Format, 0 für die Anzahl der Dezimalstellen und* ⬆ *Gut (Grün) für Polarität.*

**D**. Wenn Sie Tags verwenden, mit denen Sie Themen anwenden und berechnete Metriken schnell finden können, fügen Sie die hier zutreffenden Tags hinzu. Wir haben *AOV* und *Callcenter* Tags.

**E.** Dieser Abschnitt dient der Anzeige - während Sie Ihre berechnete Metrik in Abschnitt F erstellen, wird die Formel hier angezeigt.

**F.** Hier ziehen Sie Dimensionen (H), Metriken (I) oder Segmente (J) in den Arbeitsbereich, um Ihre berechnete Metrik sowie die Operatoren für die Formel zu erstellen. Wenn Sie für jede Metrik auf das Zahnrad klicken, können Sie den Metriktyp (Standard/Gesamtwert) und das Attributionsmodell ändern. *Wir ziehen den Call-Center-Umsatz per Drag-and-Drop, und darunter werden wir*÷ ￼*. Wir akzeptieren den standardmäßigen Metriktyp und das Attributionsmodell.*

**G**. Verwenden Sie diese **+Hinzufügen** -Option, um zusätzliche Bedingungen oder statische Zahlen hinzuzufügen, die hier nicht benötigt werden.

**K.** Und schließlich, während Sie Ihre Berechnung erstellen, können Sie die Daten der letzten 90 Tage hier in der Vorschau anzeigen.

Nachdem wir jetzt Call Center AOV erstellt haben, benötigen wir auch eine berechnete Metrik für Online AOV. Wir würden dies nach den oben beschriebenen Schritten tun.

Als Nächstes können wir eine dritte berechnete Metrik erstellen, entweder mithilfe des Generators für berechnete Metriken oder direkt aus der Freiformtabelle heraus, um das Callcenter und Online-AOV zu vergleichen, sodass wir am Ende Folgendes erreichen:

![Calc 05](assets/calc05.png)

In unserem Beispiel sehen wir eine erhebliche Steigerung, wenn Käufer das Callcenter verwenden, um ihnen beim Kauf zu helfen. Diese Daten können dann unsere Entscheidungen darüber informieren, wie Kunden bei Käufen unterstützt werden können, z. B. durch Popup-Angebote oder andere geführte Erlebnisse.

## Verwenden von Segmenten in berechneten Metriken

Sehen wir uns nun an, wie wir Segmente in berechneten Metriken verwenden können, um mehr Einblicke in Kundenverhalten, Präferenzen und Motivationen zu erhalten. Mit Segmenten und berechneten Metriken können wir genug über Kunden lernen, um ihr Erlebnis zu verbessern, den Umsatz zu steigern und die Kundenzufriedenheit und -loyalität zu verbessern.

Aus den obigen AOV-Beispielen wissen wir bereits, dass Call-Center-gestützte Käufe in der Regel einen höheren AOV-Wert aufweisen. Andere Metriken zeigen uns jedoch, dass die meisten Benutzer das Callcenter nicht für Käufe verwenden.

Welche Einzelhandelskategorien - und Benutzerpfade durch diese Kategorien - führen also zum höchsten AOV?  Wir können dies ermitteln, indem wir Segmente mit berechneten Metriken kombinieren.

Dazu müssen wir zunächst Besuchsebene erstellen *include* und *exclude* Segmente für jede Produktkategorie. Ein- oder Ausschließen wird durch Klicken auf das **Optionen** Zahnrad in der rechten Ecke des Containers. Der Standardwert ist &quot;Einschließen&quot;.

![Calc 06](assets/calc06.png) ![Calc 07](assets/calc07.png)

Nachdem wir diese Segmente erstellt haben, können wir eine berechnete Metrik erstellen, die Ihnen die Antwort auf Ihre Frage gibt. Wir öffnen den Generator für berechnete Metriken und führen folgende Schritte aus:

1. Suchen Sie nach den neu erstellten Segmenten und ziehen Sie die gewünschten Segmente per Drag-and-Drop in den grauen Bereich oben im **Definition** ankreuzen. Wenn wir z. B. einen AOV für Benutzer erstellen möchten, die sowohl die Kategorie &quot;Frauen&quot;als auch die Kategorie &quot;Männer&quot;besucht haben, aber keine Kategorie &quot;Kinder&quot;haben, können wir diese drei Segmente per Drag-and-Drop in diesen Bereich ziehen: *Frauen einschließen*, *Männer einschließen* und *Kid ausschließen*. Wir nennen das *Segmentstapelung*.

   ![Calc 09](assets/calc09.png) ![Calc 08](assets/calc08.png)

1. Anschließend ziehen wir die **Online-Umsatz** Metrik in denselben Behälter hinein, und **Online-Bestellungen**. Da Container wie mathematische Ausdrücke funktionieren, um die Reihenfolge der Vorgänge zu bestimmen, werden Elemente in Containern vor nachfolgenden Prozessen verarbeitet, obwohl wir in dieser Berechnung nicht mehrere Container oder Prozesse haben.
1. Wir ändern den Operator zwischen den beiden Metriken in Division ().
1. Auswahl **Währung** als Format, **0** Dezimalstellen und **UP** für Polarität.
1. Benennen Sie die berechnete Metrik und geben Sie eine Beschreibung ein.
1. Speichern.

Wenn wir fertig sind, sieht unsere berechnete Metrik wie folgt aus:

![Calc 10](assets/calc10.png)

Nachdem wir errechnete Metriken mit gestapelten Segmenten für jede Kombination der Journey der Besucherkategorie erstellt haben und uns die Daten anschauen, sehen Sie sich an, was wir lernen! Benutzer, die während ihres Besuchs sowohl die Kategorie &quot;Frauen&quot;als auch die Kategorie &quot;Männer&quot;besuchen, haben den höchsten AOV, und im Vergleich zu Besuchern einer Kategorie ist die Steigerung erheblich:

![Calc 11](assets/calc11.png) ![Calc 12](assets/calc12.png)

Da wir dies wissen, können wir das Seitenlayout, die Produktplatzierungen und die Werbebotschaften optimieren, um mehr Personen in diese Kategorien zu bringen, bevor sie auschecken.

## Wertvoll, aber nicht überall verfügbar

**Also - berechnete, sowohl einfache als auch komplexe Metriken sind super wertvoll für Analysten!**

Diese Metriken sind jedoch nicht in allen Bereichen von Adobe Analytics verfügbar. Berechnete Metriken können nicht in folgenden Bereichen verwendet werden:

- Fallout in Analysis Workspace
- Kohortenanalyse in Analysis Workspace
- Data Warehouse
- Echtzeitberichte
- Aktuelle Datenberichte
- Analytics for Target
- Report Builder

## Best Practices für berechnete Metriken

Nachdem Sie nun wissen, wie wertvoll berechnete Metriken sein können, sollten Sie sich einige Best Practices bei der Erstellung ansehen.

1. **Überprüfen Sie die Formelsyntax.** Achten Sie darauf, dass die Formelsyntax richtig ist und der Adobe Analytics-Syntax folgt, um aussagekräftige Informationen zu erhalten.
1. **Überprüfen Sie die Reihenfolge der Vorgänge.** Stellen Sie sicher, dass Sie Container sorgfältig verwenden und die Dinge in die richtige mathematische Reihenfolge der Vorgänge stellen.
1. **Daten nicht doppelt zählen**. Sie können eine Doppelzählung von Daten vermeiden, indem Sie sicherstellen, dass die in der berechneten Metrik verwendete Formel nicht dieselben Daten mehrmals zählt. Dies wird oft durch die Kombination von *Einschließen* und *Ausschließen* Bedingungen in der berechneten Metrik oder durch die Verwendung von Segmenten.
1. **Überprüfen Sie die Zeitgranularität.** Stellen Sie sicher, dass die berechnete Metrik dieselbe Zeitgranularität wie die in der Formel verwendeten Quellmetriken aufweist.
1. **Verwenden genauer Daten:** Sie erhalten nur wertvolle Ergebnisse, wenn Sie genaue und zuverlässige Daten in der Berechnung verwenden.

## Best Practices für benutzerspezifische Segmente

Beachten Sie beim Erstellen von Segmenten in Adobe Analytics die folgenden Best Practices:

1. **Halten Sie es einfach.** Vermeiden Sie eine Überkomplikation des Segments. Halten Sie es so einfach wie möglich und verwenden Sie nur die Bedingungen, die zur Gewährleistung der Genauigkeit erforderlich sind.
1. **Verwenden Sie die richtigen Behältertypen**. Stellen Sie sicher, dass Sie in der Segmentdefinition den richtigen Behältertyp - Besucher, Besuch oder Treffer - verwenden, um zu vermeiden, dass falsche Ergebnisse angezeigt werden.
1. **Daten nicht doppelt zählen**. Stellen Sie wie bei berechneten Metriken sicher, dass das Segment nicht dieselben Daten mehrmals zählt. Ein- und Ausschließen von Containern kann dabei helfen.
   1. Wenn ein Include-Container verwendet wird, *include* *den gesamten Inhalt des Besuchs* , wenn ein Treffer mit der Bedingung innerhalb des Besuchs übereinstimmt.
   1. Wenn ein Exclude-Container verwendet wird, *schließt den gesamten Inhalt des Besuchs aus* , wenn ein Treffer mit der Bedingung innerhalb des Besuchs übereinstimmt.
1. **Container ordnungsgemäß verschachteln**. Bestimmen Sie, welche Daten mit dem äußersten Container eingeschlossen werden, und wenden Sie dann verschachtelte Regeln auf die verbleibenden Daten an. Da verschachtelte Regeln angewendet werden, fungiert der Segmentfluss als Trichter und nachfolgende Regeln gelten nicht für Treffer, die von der ersten Regel ausgeschlossen wurden.
1. **Stellen Sie sicher, dass Ihre Daten auf dem neuesten Stand sind.** Stellen Sie sicher, dass Sie in der Segmentdefinition genaue und aktuelle Daten verwenden, um genaue Ergebnisse zu erhalten.
1. **Testen Sie das Segment.** Testen Sie das Segment immer, um sicherzustellen, dass es wie gewünscht funktioniert, bevor es für andere freigegeben wird.
1. **Betrachten Sie die Leistung.** Segmente können die Berichtsverarbeitung verlangsamen. Beachten Sie daher, dass sich dies beim Erstellen der Segmente auswirkt.

## Wichtige Schlussfolgerungen

Die Kombination von Segmenten und berechneten Metriken in Adobe Analytics kann absolut zu einer robusteren und effektiveren Datenanalyse führen. Durch die Aufteilung und Auswertung Ihrer Daten und die Erstellung von Vergleichsberechnungen erhalten Sie tiefere Einblicke in das Kundenverhalten, mit denen Sie Ihre Marketing-Kampagnen optimieren und maßgeschneiderte Dashboards und Berichte erstellen können. Beachten Sie jedoch, dass berechnete Metriken nicht in allen Bereichen von Adobe Analytics verfügbar sind, und achten Sie auf Best Practices, um sicherzustellen, dass Sie genaue und nützliche Daten erhalten.


## Autor

Dieses Dokument wurde verfasst von:

![Debbie Kern](assets/calc13.jpeg)

**Debbie Kern**, Senior Adobe Analytics Manager bei Adswerve

![Adswerve](assets/calc14.png)
