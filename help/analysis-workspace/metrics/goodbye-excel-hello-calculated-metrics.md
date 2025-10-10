---
title: Tschüss Excel, hallo berechnete Metriken
description: Erfahren Sie in diesem Artikel die Vorteile der Verwendung berechneter Metriken in Adobe Analytics und wie sie Ihnen eine kontinuierliche, dynamische Ansicht Ihrer Daten bieten kann.
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

Erfahren Sie in diesem Artikel die Vorteile der Verwendung berechneter Metriken in Adobe Analytics und wie sie Ihnen eine kontinuierliche, dynamische Ansicht Ihrer Daten bieten kann.

Hallo! Warum sind Sie gerade in Excel? Ich meine, ich weiß warum. Man hat Berichte, um die richtigen Leute zu finden. Sie geben Daten aus Adobe Analytics ein, berechnen Konversionsraten, zeichnen sie ab und bereiten sich darauf vor, sie in einen PowerPoint zu übertragen, der für Entscheidungsträger verfügbar ist. Ich hoffe wirklich, dass Sie zumindest Report Builder verwenden, um es zu tun, aber ich weiß, dass einige von Ihnen manuell Daten von einer Workspace nach Excel kopieren und einfügen.

Warum?

Warum sollte man jeden Monat einen manuellen Prozess durchlaufen? Warum sollten Sie einmal im Monat eine statische Ansicht anstelle einer kontinuierlichen, dynamischen Ansicht präsentieren? Warum sollte man das in PowerPoint kopieren? Warum lassen sich berechnete Metriken nicht direkt in Adobe Analytics erstellen?

## Berechnete Metriken sind leistungsstark

Berechnete Metriken sind leistungsstark, aber selbst die grundlegenden mathematischen Funktionen sind wirklich nützlich und eine erhebliche Verbesserung gegenüber der Mathematik in Excel. Sehen wir uns einige der Vorteile und einige Anwendungsfälle an:

1. **Berechnete Metriken sind aktuell und dynamisch**

   Wenn Sie Zahlen aus Adobe Analytics exportieren, werden sie zu einem bestimmten Zeitpunkt gesperrt. Sie müssen unbedingt wissen, wie Ihre Site oder App im Monat zuvor funktioniert hat, aber wie behalten Entscheidungsträger den Überblick darüber, wie es Mitte des Monats läuft? Wenn Ihre Konversionsrate einen Tag lang sinkt und dann am Ende des Monats zum Mittelwert zurückkehrt, wissen Sie das dann? Dieser Absturz könnte wertvolle Daten sein, die ein wichtiges Telemetrieproblem aufzeigen, oder sogar noch wichtiger, eine Änderung des Besucherverhaltens. Mit einer berechneten Metrik können Sie dies grafisch darstellen und den Tag sehen, an dem es geschieht. So können Sie sofort reagieren.

1. **Berechnete Metriken sparen Zeit**

   Ich war dort. Kopieren/Einfügen. Geben Sie die Formel ein oder ziehen Sie die Zelle darüber nach unten. Klicken Sie auf das Diagramm und ändern Sie den Bereich so, dass Sie die letzten zwölf oder dreizehn Monate haben. Kopieren Sie nun das Diagramm. Jetzt noch mal. Und nochmal. Und nochmal. Senden Sie den PowerPoint aus. Es ist mühsam und zeitaufwendig und es fühlt sich an, als müsste man es jeden Monat für immer tun.

   Stattdessen können Sie eine Workspace erstellen, die Ihre berechnete Metrik verwendet, die letzten zwölf oder dreizehn vollen Monate als Datumsbereich hat und die Daten und das Diagramm am ersten Tag jedes Monats um Mitternacht automatisch aktualisiert. Die Empfänger können direkt auf die Workspace zugreifen. Ihnen kann am ersten Tag des Monats oder nachdem Sie Textvisualisierungen verwendet haben, um Ihren Kommentar zu den Daten hinzuzufügen, automatisch eine PDF Copy per E-Mail gesendet werden (der unterhaltsame Teil des Reportings, wissen Sie).

1. **Berechnete Metriken können auf große Datensätze angewendet werden**

   Sie können alle Produktnamen nach Excel exportieren und mit der Berechnung der Konversionsraten und des Umsatzes pro Besucher beginnen, aber dies wird zu einem Ärger, wenn Sie etwa 100.000 haben. Kein Problem mit berechneten Metriken. Ziehen Sie Ihre Dimension wie gewohnt in eine Tabelle und verwenden Sie dann Ihre berechneten Metriken als Metriken. Jetzt haben Sie eine dynamische sortierbare Tabelle, die automatisch aktualisiert wird, wenn Produkte oder die Dimension, die Sie verwenden, zu Ihrem Katalog hinzugefügt werden.

1. **Berechnete Metriken verhindern Fehler**

   Excel-Fehler treten auf. Wir waren alle dort. Die gesamte griechische Wirtschaft und der Ruf zweier angesehener Akademiker waren ruiniert, aufgrund eines Excel-Formelfehlers. Wahrscheinlich haben Sie keine europäische Wirtschaft, die von Ihren Excel-Fähigkeiten abhängt, aber es gibt definitiv eine Entscheidung über Budgets, die sich basierend auf Ihren Zahlen verschieben wird. Die Verwendung von berechneten Metriken bedeutet, dass Sie eine Metrik erstellen, sie mit QS versehen und sich dann keine Gedanken mehr darüber machen können.

### Nachdem wir nun die Vorteile der Verwendung von berechneten Metriken untersucht haben, schauen wir uns an, wie wir sie in die Praxis umsetzen können

**Anwendungsfall 1: Konversionsraten**

Die meisten Konversionsraten sind nur eine einfache Division. Dividieren Sie die Anzahl der Konversionen durch die Anzahl der Besucher oder Besuche. Teilen Sie die Anzahl der Seitenansichten für die letzte Seite einer funnel durch die Anzahl der Seitenansichten für die erste Seite einer funnel. Dividieren Sie die Anzahl der internen Kampagnen-Clickthroughs durch die Anzahl der Impressionen. All diese Vorgänge können einfach als berechnete Metriken ausgeführt und in einem Dashboard platziert werden, das eine niedrige Datenlatenz, eine Aktualisierung von Visualisierungen und eine bessere Freigabe bietet.

**Anwendungsfall 2: Interne Suche**

Die interne Suche ist eines der wichtigsten Tools zum Verständnis Ihrer Site. Die Site-Suchergebnisse geben Aufschluss darüber, was Ihre Besucher interessiert und ob sie es über die Navigation leicht finden können oder nicht. Sie müssen in der Lage sein zu erkennen, ob Ihre Site-Suche gut funktioniert und mit ein wenig grundlegenden Zusatz und Division können Sie diese Antwort geben.

Beginnen wir mit den Suchergebnissen. Sie möchten wissen, ob ein Suchbegriff Ergebnisse erzielt oder nichts hervorbringt. Dies sind in der Regel separate Ereignisse. Möchten Sie die Mühe auf sich nehmen, ein drittes Ereignis für alle hinzugefügten internen Site-Suchen zu erhalten? Stattdessen sollten Sie Ihren Entwicklern eine Pause gönnen und berechnete Metriken verwenden, um die interne Suche: Ergebnisse und die interne Suche: Keine Ergebnisse hinzuzufügen, um insgesamt interne Suchen zu erhalten.

Welcher Prozentsatz von Suchvorgängen gibt keine Ergebnisse zurück? Interne Suche teilen: Keine Ergebnisse nach dieser neuen berechneten Metrik für die interne Gesamtsuche. Jetzt wissen Sie, ob es dringend ist, neue Inhalte zu erstellen, die diesen Suchbegriffen entsprechen, oder ob Ihr Content-Team höhere Prioritäten setzen kann.

Wir möchten wissen, wie viele dieser Suchvorgänge mit Ergebnissen zu Clickthroughs führen und normalerweise auch dafür eine separate Metrik haben. Verwenden Sie berechnete Metriken, um die Anzahl der Clickthroughs durch die Anzahl der Fälle zu teilen, in denen dieser Begriff Suchergebnisse hervorgebracht hat, und um ihn als Prozentsatz anzuzeigen. Jetzt haben Sie die Clickthrough-Rate für jeden internen Suchbegriff auf Ihrer Site. Sie können die Suchbegriffe isolieren, die zu wenig hilfreichen Ergebnissen führen. Sie enthält alle historischen Daten, um sie grafisch darzustellen, und durch Verbesserungen kann man leicht erkennen, ob sie funktionieren, indem man die Steigerung beobachtet.

Dividieren Sie die Anzahl der internen Suchen durch die Anzahl der suchenden Besucher. Sie haben für jeden Begriff Suchvorgänge pro Besucher. Wenn diese Zahl hoch ist (je näher sie bei 1,0 liegt, desto besser), haben Sie eines von zwei möglichen Problemen. Entweder sind die angeklickten Ergebnisse schlecht und Ihre Besucher führen mehrere Suchvorgänge durch, um die besten Ergebnisse zu finden, oder sie können die gesuchten Seiten nicht über die Navigationsleiste finden.

Wie kann man messen, ob diese Schlüsselseiten über die Navigationsleiste auffindbar sind? Erstellen Sie eine berechnete Metrik für Seitenansichten, die einer Suchergebnisseitenansicht folgt. Teilen Sie dies durch die Gesamtzahl der Seitenansichten für diese Seite. Jetzt kennen Sie den Prozentsatz der Seitenansichten, die aus Suchergebnissen stammen. Wenn Sie einen hohen Prozentsatz haben, haben Sie wahrscheinlich einige Arbeit auf der Navigation zu tun.

### Berechnete Metriken sind leistungsstark

Ich hoffe, dies hat Ihnen einige der Möglichkeiten gezeigt, grundlegende mathematische Funktionen in berechneten Metriken zu verwenden, und dass Sie damit beginnen werden, selbst welche zu erstellen. Dies beschreibt nur die Möglichkeiten der Mathematik, die Sie in berechneten Metriken ausführen können, auch mit vier einfachen Funktionen. Berechnete Metriken können Ihnen dabei helfen, das Besucherverhalten auf einer völlig neuen Ebene zu verstehen. Und sobald Sie den Dreh heraus haben, haben Sie die Tür für die Verwendung komplexerer Funktionen geöffnet, die Ihnen auch zur Verfügung stehen.

## Autor

Dieses Dokument wurde verfasst von:

![Gittai-Kopfzeilenaufnahme](assets/gittai.png)

**Gitai Ben-Ammi**, Principal Consultant bei Concentrix Catalyst

Adobe Analytics-Experte
