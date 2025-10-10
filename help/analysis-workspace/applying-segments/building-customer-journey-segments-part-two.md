---
title: Erstellen von Journey-Segmenten für Kunden - Teil 2
description: In Teil 2 erfahren Sie, wie Sie Zielgruppensegmente für Kauf und Kundenbindung erstellen, um das Kaufen von Journey und die Personalisierung von Inhalten durch Kunden zu verstehen. Mithilfe von Signalen wie „Jetzt buchen“-Klicks oder Logins identifizieren wir die Kauf- und Aufbewahrungsabsicht für eine effektive Analyse und zielgerichtetes Marketing.
feature: Segmentation
role: User
level: Experienced
last-substantial-update: 2023-07-21T00:00:00Z
jira: KT-13476
thumbnail: KT-13476.jpeg
exl-id: 2db73010-5cd0-4454-a4ba-fc1667a50cba
source-git-commit: d95136a21c08312a81baba7673cb7135270af4bd
workflow-type: tm+mt
source-wordcount: '1997'
ht-degree: 0%

---

# Erstellen von Journey-Segmenten für Kunden - Teil 2

In Teil 2 erfahren Sie, wie Sie Zielgruppensegmente für Kauf und Kundenbindung erstellen, um das Kaufen von Journey und die Personalisierung von Inhalten durch Kunden zu verstehen. Mithilfe von Signalen wie „Jetzt buchen“-Klicks oder Logins identifizieren wir die Kauf- und Aufbewahrungsabsicht für eine effektive Analyse und zielgerichtetes Marketing.

## Erstellen von Zielgruppensegmenten für Kauf und Kundenbindung

In unserem letzten Beitrag haben wir den Prozess der Erstellung von Besuchsabsichtssegmenten beschrieben und unser erstes Besuchsabsichtssegment, One Hit Wonders , erstellt. Heute werden wir unsere Kauf- und Kundenbindungssegmente erstellen. Wir hatten etwa 23 % unserer Besuche segmentiert und unsere Platzhalter für die verbleibenden Besuchsabsichtssegmente erstellt.

![Bild 1](assets/Image-1.png)

Die Besuchsabsichtssegmente, die wir jetzt erstellen, sind die Grundlage für die Erstellung besucherbasierter Kunden-Journey-Segmente. Wir erstellen diese besucherbasierten Journey-Segmente, nachdem wir unsere Besuchsabsichtssegmente erstellt haben.

Denken Sie daran, dass die Erstellung von Besuchsabsichtssegmenten ein Eliminierungsprozess ist. Wir erstellen diese Segmente also nicht in chronologischer Reihenfolge. Wir erstellen unsere Besuchsabsichtssegmente, damit sie am einfachsten zu definieren und schwieriger zu definieren sind:

1. Absicht: 0 - One Hit Wonders
1. Absicht: 3 - Kauf
1. Absicht: 4. Bindung
1. Absicht: 2 - Überlegungen
1. Absicht: 1 - Bewusstheit

In unserem letzten Beitrag habe ich das Segment „Kauf“ als „Buchung“ bezeichnet, da ich im Reisegeschäft bin. Künftig nennen wir es jedoch das Segment „Einkauf“, um es einfacher zu machen, es auf mehrere Branchen anzuwenden.

Je klarer das Signal, desto einfacher ist es, das Segment zu erstellen. In unserem letzten Beitrag haben wir unser Segment One Hit Wonders erstellt, das am einfachsten zu definieren war, da es nur Traffic zurückgibt. Sie werden feststellen, dass die Segmente Kaufabsicht und Kundenbindungsabsicht ebenfalls sehr einfach zu definieren sind, da sie auf sehr klaren Signalen basieren.

## Kunden-Journey unterscheidet sich von der Kaufneigung

Wenn wir uns mit dem Aufbau unseres Kaufabsichtssegments befassen, ist es wichtig, sich zu erinnern, dass die Identifizierung des Ortes, an dem sich ein Kunde in seinem Journey befindet, von der Tendenz unterscheidet. Möglicherweise verfügen Sie über einige Kaufneigungsmodelle, mit denen Web-Besucher bewerten, um vorherzusagen, mit welcher Wahrscheinlichkeit sie einen Kauf tätigen werden. Diese Modelle sind äußerst nützlich, unterscheiden sich jedoch von dem Segment der Kaufabsicht, das wir heute erstellen werden.

Während ein Tendenzmodell vorhersagen soll, ob eine Besucherin oder ein Besucher einen Kauf tätigt, versuchen unsere Besuchsabsichtssegmente zu verstehen, wo eine Person sich in ihrem kaufenden Journey befindet. Die Verwendung von Intent-Segmenten, um den Gemütszustand eines Kunden zu verstehen, hilft uns, Inhalte zu personalisieren und das Marketing so anzupassen, dass der richtige Traffic für unsere Vertriebs-Pipeline entsteht. Daher sucht unser Segment Kaufabsicht nach expliziten Verhaltenssignalen, die darauf hinweisen, dass ein Besucher einen Kauf tätigen möchte.

## Erstellen des Segments „Purchase Visit Intent“

Das Segment „Purchase Visit Intent“ lässt sich einfach definieren. In meinem Fall signalisiert jeder, der auf den „Jetzt buchen“-Button klickt, eine Art Absicht, eine Kreuzfahrt zu buchen. Dies ähnelt dem Klicken auf „Checkout“ für eine Online-retailer oder auf einen Link „Abonnieren“ in einem Medienkontext.

Bei der Entscheidung, welches Signal für die Ableitung der Kaufabsicht verwendet werden soll, müssen Sie ein gewisses Urteilsvermögen walten lassen. Wir möchten, dass unser Segment „Kaufabsicht“ alle Käufe enthält, aber die Konversionsrate sollte nicht 100 % betragen. Daher möchten wir für dieses Segment nicht die Seite mit der Kaufbestätigung oder der Dankeseite verwenden.

Ebenso ist die Seite Überprüfen eines Kaufs (oder was auch immer unmittelbar vor der Kaufbestätigung steht) zu weit unten in funnel, als dass sie für Analysen und Targeting nützlich wäre.

Wenn Sie den funnel weiter hinaufgehen, wird es möglicherweise weniger klar, ob das Signal nützlich ist, um anzuzeigen, dass ein Kunde einen Kauf beabsichtigt. In meinem Fall ähnelt „Jetzt buchen“ einem „Checkout“-Link für den Einzelhandel, und das ist das Signal, das ich verwendet habe. Im Einzelhandel kann es jedoch vorkommen, dass der Checkout zu weit unten im funnel liegt und Warenkorb anzeigen oder sogar Zum Warenkorb hinzufügen besser ist.

Wir können es uns wie einen Lebensmittelladen vorstellen. Wenn jemand ein Produkt aus dem Regal abholt, bedeutet das nicht, dass er beabsichtigt, es zu kaufen. Selbst wenn sie es in ihren Warenkorb legen, können sie es sofort wieder zurück ins Regal legen. Aber wenn sie das Produkt in den Warenkorb legen und anfangen damit herumzulaufen, ist die Wahrscheinlichkeit recht groß, dass sie es kaufen wollen. Und wenn sie mit diesem Produkt in die Kasse gehen, ist das eine ziemlich gute Wette, dass sie kaufen werden.

Ich schlage vor, besuchte Seiten oder andere explizite Kaufabsichtssignale zu verwenden und andere, weniger direkte Signale zu vermeiden, um die Kaufabsicht zu identifizieren. Beispielsweise würde ich nicht die Anzahl der Sitzungen oder die Anzahl der Seiten in einer Sitzung oder Ähnliches verwenden. Diese indirekten Signale deuten auf eine Berücksichtigung, nicht auf eine Kaufabsicht hin. Denken Sie daran, dass dieses Segment dazu dient, die Absicht des Besuchers für den Besuch abzuleiten, nicht seine Neigung.

### Verwenden von Analytics Workspace zur Identifizierung von Kaufabsichtssignalen

Der Fallout -Bericht ist sehr nützlich, um ein gutes Signal zu identifizieren, das auf eine Kaufabsicht hinweist. Suchen Sie nach einem Ort, der logisch Absicht anzeigt. Sie können bestätigen, dass der Schritt eine Absicht anzeigt, wenn Sie einen bemerkenswerten Fallout sehen, der zu diesem Schritt führt, oft gefolgt von einem kleineren Fallout für den Schritt unmittelbar danach.

![Bild 2](assets/Image-2.png)

Es ist auch nützlich, die Konversionsraten zu betrachten, die mit den verschiedenen Seiten auf Ihrer Site verbunden sind. Dies ist besonders hilfreich, um Seiten zu identifizieren, die eine Kaufabsicht anzeigen, aber möglicherweise nicht zu einem Kauf erforderlich sind (z. B. Finanzierungsseiten, Kaufkonfigurationsseiten usw.).

![Bild 3](assets/Image-3.png)

Schließlich ist es wichtig, alle Seiten zwischen Kaufstart und Kaufbestätigung in Ihrem Segment einzubeziehen. Besucher können an verschiedenen Punkten Ihren Kauffluss zurückschrauben und ihn erneut aufrufen.

### Andere Segmente ausschließen

Denken Sie an unseren ersten Beitrag. Unsere Besuchsabsichtssegmente müssen sich gegenseitig ausschließen und vollständig erschöpfend sein. Dieser Refrain wird in dieser Serie viel zu hören sein.

Stellen Sie sicher, dass Ihr Kaufabsichtssegment das Segment „Ein“ und „Fertig“ ausschließt. Sie sollten nur das Segment „Ein“ und „Fertig“ ausschließen müssen, da die Signale, die wir für die Kaufabsicht verwenden, sehr spezifisch sind.

Beachten Sie, dass beim Ausschließen des Segments Eins und Fertig möglicherweise eine Person ausgeschlossen wird, die auf einer Checkout-Seite erneut auf Ihre Website gelangt. Das ist in Ordnung. Die Definition von Eins und Fertig ist eine Seitenansicht, was bedeutet, dass selbst dann, wenn ein Besucher eine Checkout-Seite betritt oder auf dieser aktualisiert, sein Besuch nicht fortgeschritten ist, daher kein Ausdruck der Kaufabsicht vorhanden ist.

### Das Segment Kaufabsicht in Segment Builder

Die Segmentdefinition für die Kaufabsicht ist sehr einfach.

Schließen Sie mit dem Besuchs-Container die Seiten oder andere Aktionen ein, die explizit eine Kaufabsicht anzeigen. Wenn Sie mehrere Einschlussbedingungen haben, stellen Sie sicher, dass Sie sie in einen Container einfügen, der durch die „Und“-Bedingung verbunden ist.

Fügen Sie einen Ausschluss -Container zu dem Segment hinzu, das durch die Bedingung „Und“ verbunden ist. Fügen Sie Ihre Segmentdefinition One Hit Wonders (Seitenansichten gleich 1) zum Ausschluss-Container hinzu.

![Bild 4](assets/Image-4.png)

Als Best Practice sollten Sie sicherstellen, dass Sie Ihre Container beschriften. Sie werden sich freuen, dass Sie dies getan haben, insbesondere da unsere Segmentdefinitionen komplexer werden.

Nachdem wir nun das Segment „Kaufabsicht“ erstellt haben, können wir die Workspace „Besuchsabsicht - Datenqualität“ verwenden, um zu sehen, dass sich unser Segment „Kaufabsicht“ und unser Segment „Eins und Fertig“ gegenseitig ausschließen.

![Bild 5](assets/Image-5.png)

## Erstellen des Segments „Retention Visit Intent“

Im Kreuzfahrtgeschäft kommen viele Gäste auf unsere Website, um eine Buchung zu verwalten, aber nicht unbedingt, um einen Kauf zu tätigen. Sie können auf die Website kommen, um Reiseinformationen einzugeben, ihre Reiseroute zu überprüfen, Abendessenreservierungen vorzunehmen oder eine Reihe anderer Dinge, ohne für eine Kreuzfahrt einzukaufen. Unsere Gäste können auch Landausflüge oder andere Verbesserungen ihrer Erfahrung erwerben. Wir betrachten diese Verbesserungen als Teil der Bindung, daher halten wir sie von unserem Buchungssegment (das wir in dieser Blog-Reihe als „Kauf“ bezeichnen) getrennt.

Einzelhandelskunden können möglicherweise Rücksendungen vornehmen oder ihr Treueprogramm verwalten. Abonnentinnen und Abonnenten von Medien oder Technologie verwenden das Produkt möglicherweise. Wenn sich Ihr Gast auf Ihrer Website befindet, um seine Beziehung zu Ihnen zu verwalten, ist dies ein Kundenbesuch, und wir sollten uns diese Signale ansehen. Und wenn Sie ein Online-Produkt bereitstellen, wie etwa Media, Tech, Online Banking oder andere, gibt es wahrscheinlich viele andere Arten von Besuchsabsichtssegmenten, die wir in dieser Serie nicht besprechen werden.

Wie beim Segment „Kaufabsicht“ suchen wir nach sehr expliziten Anzeichen für eine Absicht. Für mich gibt es einen ganzen Bereich der Website, der sich mit der Verwaltung einer Kreuzfahrt beschäftigt, damit diese Seiten leicht zu erkennen sind. Dies könnte für andere Unternehmen komplexer sein. Achten Sie auf Signale wie Anmeldungen, Kontoverwaltung, Besuche auf Support-Seiten und Ähnliches.

Ich sollte beachten, dass „Bindung“ ein etwas seltsamer Name für diesen Besuchswunsch ist, da der Besucher nicht auf unserer Website ist, „sodass ich als Kunde beibehalten werden kann“. Die Bindung ist unsere Absicht für diesen Besuch. Denken Sie nur daran, gegenüber unseren Kunden empathisch zu sein und einen Customer-First-Fokus zu bewahren!

### Verwenden von Analytics Workspace zur Identifizierung von Aufbewahrungsabsichtssignalen

Auch hier hilft uns Analytics Workspace bei der Identifizierung der Aufbewahrungsabsicht. Sie können die Seiten, den Site-Bereich oder benutzerdefinierte Segmentdimensionen verwenden, um Ihre Seiten zu kategorisieren. Suchen Sie nach Seiten mit niedrigen Kaufkonversionsraten. In unserem Fall stellen wir fest, dass die Seiten für Online-Check-In und Shore-Exkursion (Shorex) relativ niedrigere Konversionsraten aufweisen als andere Seiten, die logischer mit Shopping und Einkauf verbunden sind.

![Bild 6](assets/Image-6.png)

Es empfiehlt sich auch, in Workspace nach Seiten mit hohem Traffic zu suchen. Scannen Sie die Liste der Seiten mit hohem Traffic und entscheiden Sie, ob sie eine Aufbewahrungsabsicht anzeigen.

## Andere Segmente ausschließen

Auch hier müssen sich unsere Besuchsabsichtssegmente gegenseitig ausschließen und vollständig erschöpfend sein. Wenn Sie es noch nicht leid sind, dies zu lesen, werden Sie es sein! Für unser Segment „Aufbewahrungsabsicht“ ist es von entscheidender Bedeutung, Kaufabsichtsverhaltensweisen auszuschließen.

Für die meisten von uns schließen Kaufabsicht und Aufbewahrungsabsicht sich nicht gegenseitig aus. Wir haben Gäste, die auf die Website kommen, um ihre bevorstehende Kreuzfahrt zu verwalten, aber auch um ihre nächste Reise zu buchen (danke!). Wenn Sie ein Restaurant sind, kann ein Besucher seine Treuepunkte überprüfen und dann eine Online-Bestellung aufgeben.

Auch wenn sich das Verhalten nicht gegenseitig ausschließt, müssen unsere Segmente für die Analyse des Kunden-Journey verwendet werden. Wir können weitere sehr interessante Segmente erstellen, um die Überschneidung zwischen Kauf- und Treueverhalten zu analysieren. Für unsere aktuellen Zwecke müssen diese Segmente sich jedoch gegenseitig ausschließen.

Da die Nachfragegenerierung eines der Hauptziele des Marketings ist, schließt unser Segment „Retention Intent“ die Kaufabsicht aus. Mit anderen Worten, wenn jemand auf unsere Website kommt, um eine Kreuzfahrt zu verwalten, aber auch die Absicht zeigt, eine neue Kreuzfahrt zu buchen, wird dieser Besuch zum Segment Kaufabsicht gehen.

### Segment Builder für die Aufbewahrungsabsicht

Unsere Segmentdefinitionen werden immer knapper. Besichtigungen in Ihr Segment einschließen. Fügen Sie Ihre Retention Intent-Signale hinzu. Für mich war das ganz einfach. Wenn der Seitenname mit „bge:“ (unsere gebuchten Gastseiten) beginnt, befinden Sie sich im Segment. Ich habe Seitenansichten hinzugefügt, die größer als eins für zusätzliche Kennzahlen sind (aber wir schließen unten immer noch ein Trefferwunder aus).

Fügen Sie dann Ausschluss-Container für Ihre One-Hit-Wunder und Kaufabsichtsbesuche hinzu. Stellen Sie sicher, dass Ihre Container mit der Bedingung „Und“ verbunden sind.

![Bild 7](assets/Image-7.png)

Sehen Sie sich erneut Ihre Besuchsabsicht Data Quality Workspace an, um sicherzustellen, dass sich Ihre Segmente gegenseitig ausschließen. Unsere Visit Intent-Segmente nehmen eine schöne Form an!

![Bild 8](assets/Image-8.png)

Zu diesem Zeitpunkt haben wir drei unserer fünf Besuchsabsichtssegmente konfiguriert. Diese Segmente schließen sich unseres Erachtens gegenseitig aus. In unserem nächsten Beitrag erstellen wir die endgültigen Besuchsabsichtssegmente Überlegungen und Bewusstseinsbildung, und unsere Segmente sind alle vollständig erschöpfend. Sobald unsere Besuchsabsichtssegmente eingerichtet sind, bringen wir sie zu besucherbasierten Segmenten zusammen, die Sie für die Analyse und Personalisierung sehr nützlich finden.

## Autor

Dieses Dokument wurde verfasst von:

![Aaron Fossum](assets/aaron-headshot.png)

**Aaron Fossum**, Director, Digital Analytics

Adobe Analytics-Expertin
