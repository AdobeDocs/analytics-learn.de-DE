---
title: Tschüss Excel, hallo berechnete Metriken
description: Erfahren Sie in diesem Artikel, welche Vorteile die Verwendung berechneter Metriken in Adobe Analytics bietet und wie Sie mit ihnen eine kontinuierliche, dynamische Ansicht Ihrer Daten erhalten können.
feature: Calculated Metrics
role: User
level: Experienced
doc-type: Article
last-substantial-update: 2023-05-02T00:00:00Z
jira: KT-13178
thumbnail: KT-13178.jpeg
exl-id: d4f69244-6614-41f3-ac48-70adabb8a8e7
source-git-commit: d95136a21c08312a81baba7673cb7135270af4bd
workflow-type: tm+mt
source-wordcount: '1286'
ht-degree: 2%

---

# Tschüss Excel, hallo berechnete Metriken

Erfahren Sie in diesem Artikel, welche Vorteile die Verwendung berechneter Metriken in Adobe Analytics bietet und wie Sie mit ihnen eine kontinuierliche, dynamische Ansicht Ihrer Daten erhalten können.

He! Warum bist du gerade in Excel? Ich meine, ich weiß, warum. Man muss berichten, um die richtigen Leute zu erreichen. Sie sind damit beschäftigt, Daten aus Adobe Analytics einzugeben, Konversionsraten zu berechnen, sie zu kartieren und darauf vorzubereiten, sie alle in einen PowerPoint zu bringen, der sich an Entscheidungsträger richtet. Ich hoffe wirklich, dass Sie zumindest Report Builder dazu verwenden, aber ich weiß, dass einige von Ihnen Daten manuell aus einer Workspace in Excel kopieren und einfügen.

Warum?

Warum jeden Monat einen manuellen Prozess durchlaufen? Warum wird eine statische Ansicht einmal im Monat anstatt einer kontinuierlichen, dynamischen Ansicht angezeigt? Warum kopieren Sie das in PowerPoint? Warum werden berechnete Metriken nicht direkt in Adobe Analytics erstellt?

## Berechnete Metriken sind leistungsstark

Berechnete Metriken sind leistungsstark, aber selbst die grundlegenden mathematischen Funktionen sind wirklich nützliche und ernsthafte Verbesserungen gegenüber der Mathematik in Excel. Sehen wir uns einige Vorteile und Anwendungsfälle an:

1. **Berechnete Metriken sind aktuell und dynamisch**

   Wenn Sie Zahlen aus Adobe Analytics exportieren, sind sie zu einem bestimmten Zeitpunkt gesperrt. Sie müssen unbedingt wissen, wie Ihre Site oder App im Vormonat abgeschnitten hat, aber wie können Entscheidungsträger verfolgen, wie die Dinge mitten im Monat verlaufen? Wenn Ihre Konversionsrate einen Tag fällt und dann am Ende des Monats wieder zum Mittelwert zurückkehrt, wissen Sie das? Dieser Rückgang könnte wertvolle Daten sein, die ein wichtiges Telemeterieproblem aufzeigen oder noch wichtiger eine Änderung des Besucherverhaltens. Mit einer berechneten Metrik können Sie dies grafisch darstellen und am Tag des Auftretens anzeigen, sodass Sie bereit sind, zu reagieren.

1. **Berechnete Metriken sparen Ihnen Zeit**

   Ich war dort. Kopieren/Einfügen. Geben Sie die Formel ein oder ziehen Sie die Zelle darüber nach unten. Klicken Sie auf die Grafik und ändern Sie den Bereich, sodass Sie die letzten zwölf oder dreizehn Monate haben. Kopieren Sie nun das Diagramm. Jetzt mach es noch einmal. Und wieder. Und wieder. Senden Sie den PowerPoint. Es ist mühsam und zeitaufwendig, und es fühlt sich an, als müsste man es jeden Monat für immer tun.

   Stattdessen können Sie eine Workspace erstellen, die Ihre berechnete Metrik verwendet, die letzten Zwölf oder dreizehn vollen Monate als Datumsbereich verwenden und die Daten und das Diagramm am ersten Tag jedes Monats um Mitternacht automatisch aktualisieren lassen. Die Empfänger können direkt auf die Workspace zugreifen. Sie können eine PDF-Kopie automatisch per E-Mail an den ersten Tag des Monats oder nach der Verwendung von Textvisualisierungen erhalten lassen, um Ihren Kommentar zu den Daten hinzuzufügen (wissen Sie, der lustige Teil der Berichterstellung).

1. **Berechnete Metriken können auf große Datenmengen angewendet werden**

   Sie können alle Produktnamen in Excel exportieren und mit der Berechnung der Konversionsraten und des Umsatzes pro Besucher beginnen. Dies wird jedoch schwierig, wenn Sie etwa 100.000 haben. Kein Problem mit berechneten Metriken. Ziehen Sie Ihre Dimension wie gewohnt in eine Tabelle und verwenden Sie dann Ihre berechneten Metriken als Metriken. Jetzt haben Sie eine dynamische sortierbare Tabelle, die automatisch aktualisiert wird, wenn Produkte oder beliebige Dimensionen, die Sie verwenden, zu Ihrem Katalog hinzugefügt werden.

1. **Berechnete Metriken verhindern Fehler**

   Excel-Fehler treten auf. Wir waren alle dort. Heck, die gesamte Wirtschaft Griechenlands und die Reputation zweier angesehener Akademiker wurden wegen eines Excel-Formelfehlers ruiniert. Sie haben wahrscheinlich keine europäische Wirtschaft, die auf Ihren Excel-Fähigkeiten basiert, aber es gibt definitiv eine Entscheidung über Budgets, die basierend auf Ihren Zahlen verschoben werden. Die Verwendung berechneter Metriken bedeutet, dass Sie eine Metrik erstellen, Qualitätssicherung einrichten und sich anschließend keine Gedanken mehr darüber machen können.

### Nachdem wir nun über die Vorteile der Verwendung berechneter Metriken hinausgegangen sind, sehen wir uns an, wie wir sie in die Praxis umsetzen können.

**Nutzungsszenario 1: Konversionsraten**

Die meisten Konversionsraten sind nur eine einfache Division. Teilen Sie die Anzahl der Konversionen durch die Anzahl der Besucher oder Besuche auf. Teilen Sie die Anzahl der Seitenansichten für die letzte Seite eines Trichters durch die Anzahl der Seitenansichten für die erste Seite eines Trichters. Teilen Sie die Anzahl der internen Kampagnen-Clickthroughs durch die Anzahl der Impressionen auf. All diese Funktionen lassen sich einfach als berechnete Metriken durchführen und in ein Dashboard platzieren, das eine niedrige Datenlatenz, eine Aktualisierung der Visualisierungen und eine bessere Freigabe aufweist.

**Anwendungsfall 2: Interne Suche**

Die interne Suche ist eines der wichtigsten Werkzeuge zum Verständnis Ihrer Site. Die Site-Suchergebnisse zeigen Ihnen, woran Ihre Besucher interessiert sind und ob sie sie leicht über die Navigation finden können oder nicht. Sie müssen feststellen können, ob Ihre Site-Suche gut funktioniert, und die Verwendung einer einfachen Ergänzung und Teilung kann Ihnen diese Antwort geben.

Beginnen wir mit Suchergebnissen. Sie möchten wissen, ob ein Suchbegriff Ergebnisse erhält oder nichts aufruft. Dies sind normalerweise separate Ereignisse. Möchten Sie die Mühe erleben, ein drittes Ereignis für alle hinzugefügten internen Site-Suchvorgänge zu erhalten? Geben Sie stattdessen Ihren Entwicklern eine Pause und verwenden Sie berechnete Metriken, um die interne Suche hinzuzufügen: Ergebnisse und interne Suche: Keine Ergebnisse zusammen, um die Gesamtzahl der internen Suchvorgänge zu erhalten.

Welcher Prozentsatz der Suchvorgänge liefert keine Ergebnisse? Interne Suche aufteilen: Keine Ergebnisse durch die neue berechnete Metrik &quot;Gesamte interne Suche&quot;. Jetzt wissen Sie, ob die Erstellung neuer Inhalte, die diesen Suchbegriffen entsprechen, dringend ist oder ob Ihr Content-Team möglicherweise höhere Prioritäten setzen kann.

Wir möchten wissen, wie viele dieser Suchen mit Ergebnissen Clickthroughs erhalten und für gewöhnlich auch eine separate Metrik vorhanden ist. Verwenden Sie berechnete Metriken , um die Anzahl der Clickthroughs durch die Anzahl der Suchergebnisse durch den Begriff zu dividieren und als Prozentsatz anzuzeigen. Jetzt haben Sie die Klickrate für jeden internen Suchbegriff auf Ihrer Site. Sie können die Suchbegriffe isolieren, die zu wenig hilfreichen Ergebnissen führen. Es stehen Ihnen alle historischen Daten zur Verfügung, damit Sie sie grafisch darstellen können, und wenn Sie Verbesserungen vornehmen, können Sie einfach sehen, ob sie funktionieren, indem Sie diese Rate nach oben oder unten beobachten.

Teilen Sie die Anzahl der internen Suchen nach der Anzahl der gesuchten Besucher. Sie haben nach Besuchern für jeden Begriff gesucht. Wenn diese Zahl hoch ist (je näher sie an 1,0 liegt, desto besser), haben Sie eines von zwei möglichen Problemen. Entweder werden die Ergebnisse angeklickt und Ihre Besucher suchen mehrere, um die besten Ergebnisse zu finden, oder sie können die Seiten, nach denen sie suchen, nicht über die Navigationsleiste finden.

Wie können Sie messen, ob diese wichtigen Seiten über Ihr Navigationsmenü zu finden sind? Erstellen Sie eine berechnete Metrik für Seitenansichten, die auf die Seitenansicht der Suchergebnisse folgten. Teilen Sie dies durch die Gesamtzahl der Seitenansichten für diese Seite auf. Jetzt wissen Sie, wie viel Prozent der Seitenansichten aus den Suchergebnissen stammten. Wenn Sie einen hohen Prozentsatz haben, haben Sie wahrscheinlich noch einiges zu tun, was die Navigation betrifft.

### Berechnete Metriken sind leistungsstark

Ich hoffe, dass Ihnen dies einige der Möglichkeiten gezeigt hat, grundlegende mathematische Funktionen in berechneten Metriken zu verwenden, und dass Sie damit beginnen werden, einige selbst zu erstellen. Dies beginnt nur mit einer Beschreibung der Möglichkeiten der Mathematik, die Sie in berechneten Metriken ausführen können, selbst mit vier einfachen Funktionen. Berechnete Metriken können Ihnen dabei helfen, das Besucherverhalten auf einer völlig neuen Ebene zu verstehen, und sobald Sie den Hang dazu haben, haben Sie die Tür für die Verwendung komplexerer Funktionen geöffnet, die Ihnen ebenfalls zur Verfügung stehen.

## Autor

Dieses Dokument wurde verfasst von:

![Gittai-Headshot](assets/gittai.png)

**Gitai Ben-Ammi**, Principal Consultant bei Concentrix Catalyst

Adobe Analytics-Experte
