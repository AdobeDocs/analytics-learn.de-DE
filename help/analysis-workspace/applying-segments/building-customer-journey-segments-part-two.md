---
title: Erstellen von Journey-Segmenten für Kunden - Teil zwei
description: In Teil 2 erfahren Sie, wie Sie Einkaufs- und Bindungsbesuchsabsichten segmentieren, um die Journey von Kunden zu verstehen und Inhalte zu personalisieren. Mithilfe von Signalen wie "Jetzt buchen"-Klicks oder -Anmeldungen identifizieren wir die Kauf- und Bindungsabsichten für eine effektive Analyse und zielgerichtetes Marketing.
feature: Segmentation
role: User
level: Experienced
last-substantial-update: 2023-07-21T00:00:00Z
jira: KT-13476
thumbnail: KT-13476.jpeg
source-git-commit: bc3bf5b22e3cf5a9d77e3fe8aa2d86c65a7eaefb
workflow-type: tm+mt
source-wordcount: '1981'
ht-degree: 0%

---


# Erstellen von Journey-Segmenten für Kunden - Teil zwei

In Teil 2 erfahren Sie, wie Sie Einkaufs- und Bindungsbesuchsabsichten segmentieren, um die Journey von Kunden zu verstehen und Inhalte zu personalisieren. Mithilfe von Signalen wie &quot;Jetzt buchen&quot;-Klicks oder -Anmeldungen identifizieren wir die Kauf- und Bindungsabsichten für eine effektive Analyse und zielgerichtetes Marketing.

## Erstellen von Marketingzielsegmenten für Kauf und Treuebesuche

In unserem letzten Beitrag haben wir den Prozess der Erstellung von Besuchsabsichten-Segmenten beschrieben und unser erstes Besuchsabsichtssegment &quot;One Hit Wonders&quot;erstellt. Heute werden wir unsere Segmente für Kauf und Bindung erstellen. Wir hatten rund 23 % unserer Besuche segmentiert und unsere Platzhalter für die verbleibenden Besuchsabsichten-Segmente erstellt.

![Bild 1](assets/Image-1.png)

Die Besuchsabsichtssegmente, die wir jetzt erstellen, bilden die Grundlage für die Erstellung besucherbasierter Journey-Segmente. Wir werden diese besucherbasierten Journey-Segmente erstellen, nachdem wir unsere Besuchsabsichten-Segmente erstellt haben.

Denken Sie daran, dass das Erstellen von BesuchsIntent-Segmenten ein Eliminationsprozess ist. Wir bauen diese Segmente also nicht in chronologischer Reihenfolge. Wir erstellen unsere Besuchsabsichtssegmente, um die Definition zu beschleunigen, um Folgendes zu definieren:

1. Intent: 0 - Ein Trefferwächter
1. Intent: 3 - Kauf
1. Intent: 4 - Treue
1. Intent: 2 - Überlegungen
1. Intent: 1 - Bewusstsein

In unserem letzten Beitrag nannte ich das Segment &quot;Kauf&quot; &quot;Buchung&quot;, da ich im Reisegewerbe bin. In Zukunft werden wir es aber als Kaufsegment bezeichnen, um die Anwendung auf mehrere Branchen zu vereinfachen.

Je klarer das Signal, desto einfacher ist es, das Segment zu erstellen. In unserem letzten Beitrag haben wir unser Segment &quot;One Hit Wonders&quot;erstellt, das am einfachsten zu definieren war, da es sich lediglich um Bounce-Traffic handelt. Sie werden feststellen, dass auch die Segmente für die Absicht von Kauf und Bindung sehr einfach zu definieren sind, da sie auf sehr klaren Signalen basieren.

## Journey des Kunden unterscheidet sich von der Kaufneigung

Beim Erstellen unseres Segments &quot;Kaufabsicht&quot;ist es wichtig, sich daran zu erinnern, dass sich die Identifizierung, wo sich ein Kunde auf seiner Journey befindet, von der Tendenz unterscheidet. Möglicherweise verfügen Sie über einige Kaufneigungsmodelle, mit denen Webbesucher bewertet werden, um vorherzusagen, wie wahrscheinlich ein Kauf ist. Diese Modelle sind zwar überaus nützlich, unterscheiden sich aber vom Segment &quot;Kaufabsicht&quot;, das wir heute erstellen werden.

Während ein Tendenzmodell vorhersagen soll, ob ein Besucher etwas kauft, versuchen unsere Besuchsabsichten-Segmente zu verstehen, wo sich eine Person in ihrer Journey befindet. Die Verwendung von Intent-Segmenten zum Verständnis des Geistes eines Kunden hilft uns, Inhalte zu personalisieren und das Marketing so anzupassen, dass der richtige Traffic zur Unterstützung unserer Verkaufspipelines geleitet wird. Unser Zielgruppensegment Kauf sucht also nach expliziten Verhaltenssignalen, die darauf hinweisen, dass ein Besucher einen Kauf tätigen möchte.

## Erstellen des Zielgruppensegments für den Besuch von Käufen

Das Segment Besuchsabsicht für Kauf ist einfach zu definieren. In meinem Fall zeigt jeder, der auf die Schaltfläche &quot;Jetzt buchen&quot; klickt, eine Art Absicht an, eine Kreuzfahrt zu buchen. Dies ähnelt dem Klicken auf &quot;Auschecken&quot;für einen Online-Händler oder auf einen Link &quot;Abonnieren&quot;in einem Medienkontext.

Sie müssen ein gewisses Maß an Urteilsvermögen bei der Entscheidung darüber walten lassen, welches Signal für die absichtliche Kaufabsicht verwendet werden soll. Unser Segment &quot;Kaufabsicht&quot;soll alle Käufe enthalten, die Konversionsrate darf jedoch nicht 100 % betragen. Daher möchten wir die Kaufbestätigungs- oder Dankeseite für dieses Segment nicht verwenden.

In ähnlicher Weise ist der Drilldown-Trichter zur Überprüfung Ihrer Kaufseite (oder der unmittelbar vor der Kaufbestätigung liegende Bereich) wahrscheinlich zu weit entfernt, um für Analysen und Targeting nützlich zu sein.

Wenn Sie den Trichter weiter nach oben bewegen, kann es weniger deutlich werden, ob das Signal nützlich ist, um anzugeben, dass ein Kunde einen Kauf tätigen möchte. In meinem Fall ähnelt &quot;Book Now&quot;einem &quot;Checkout&quot;-Link für den Einzelhandel, und das ist das Signal, das ich verwendet habe. In einem Einzelhandelskontext ist der Checkout jedoch möglicherweise immer noch zu weit unten im Trichter und &quot;Warenkorb anzeigen&quot;oder &quot;Zum Warenkorb hinzufügen&quot;kann besser sein.

Wir können uns das wie ein Lebensmittelgeschäft vorstellen. Wenn jemand ein Produkt aus dem Regal nimmt, bedeutet das nicht, dass er es kaufen will. Selbst wenn sie ihn in ihren Warenkorb legen, könnten sie ihn sofort wieder ins Regal stellen. Aber wenn sie das Produkt in ihren Warenkorb legen und damit anfangen, damit herumzulaufen, besteht eine ziemlich gute Chance, dass sie es kaufen wollen. Und wenn sie mit diesem Produkt in die Kasse gehen, ist es eine ziemlich gute Wette, dass sie kaufen werden.

Ich schlage vor, besuchte Seiten oder andere explizite Kaufabsichten-Signale zu verwenden und andere, weniger direkte Signale zu vermeiden, um die Kaufabsicht zu identifizieren. Beispielsweise würde ich keine Anzahl von Sitzungen oder Seiten in einer Sitzung oder einer ähnlichen Sitzung verwenden. Diese indirekten Signale geben die Berücksichtigung an, nicht die Kaufabsicht. Beachten Sie, dass der Zweck dieses Segments darin besteht, die Absicht des Besuchers und nicht seine Neigung zum Besuch zu vermitteln.

### Verwenden von Analytics Workspace zur Identifizierung von KaufIntent-Signalen

Der Fallout-Bericht ist sehr nützlich, um ein gutes Signal zu identifizieren, das auf die Kaufabsicht hinweist. Suchen Sie nach einem Ort, der die Absicht logisch angibt. Sie können bestätigen, dass der Schritt die Absicht anzeigt, wenn Sie einen wichtigen Fallout sehen, der zu diesem Schritt führt, gefolgt von einem kleineren Fallout für den Schritt unmittelbar danach.

![Bild 2](assets/Image-2.png)

Es ist auch nützlich, sich die Konversionsraten anzusehen, die mit den verschiedenen Seiten auf Ihrer Site verbunden sind. Dies ist besonders hilfreich, um Seiten zu identifizieren, die einen Kaufabsicht angeben, aber möglicherweise nicht für einen Kauf benötigt werden (z. B. Finanzierungsseiten, Einkaufs-Konfigurationsseiten usw.).

![Bild 3](assets/Image-3.png)

Schließlich ist es wichtig, alle Seiten zwischen Kaufstart und Kaufbestätigung in Ihr Segment einzuschließen. Besucher können herumspringen und an verschiedenen Punkten wieder in Ihren Kauffluss eintreten.

### Ausschließen anderer Segmente

Erinnern Sie sich an unseren ersten Beitrag, dass sich unsere Besuchsabsichten-Segmente gegenseitig ausschließen und vollständig erschöpfend sein müssen. Das ist absurd, dass du in dieser Serie viel hören wirst.

Stellen Sie sicher, dass das Segment &quot;Kaufabsicht&quot;die Segmente &quot;Eins&quot;und &quot;Fertig&quot;ausschließt. Sie sollten nur die Segmente &quot;Eins&quot;und &quot;Fertig&quot;ausschließen, da die für den Kaufabsichten verwendeten Signale sehr spezifisch sind.

Beachten Sie, dass durch das Ausschließen der Segmente &quot;Eins&quot;und &quot;Fertig&quot;Personen ausgeschlossen werden können, die Ihre Site erneut auf einer Checkout-Seite aufrufen. Das ist in Ordnung. Die Definition von &quot;Eins&quot;und &quot;Fertig&quot;ist nur eine Seitenansicht. Das bedeutet, dass selbst wenn ein Besucher eine Checkout-Seite aufruft oder aktualisiert, sein Besuch nicht fortgesetzt wurde. Daher gibt es keinen Ausdruck für einen Kaufabsichten.

### Das Segment &quot;Kaufabsicht&quot;in Segment Builder

Die Segmentdefinition für den Kaufabsichten ist sehr einfach.

Schließen Sie unter Verwendung des Besuchsbehälters die Seiten oder anderen Aktionen ein, die explizit auf eine Kaufabsicht hinweisen. Wenn Sie mehrere Einschlussbedingungen haben, stellen Sie sicher, dass Sie sie in einem Container platzieren, der durch die &quot;Und&quot;-Bedingung verbunden ist.

Fügen Sie dem Segment, das durch die &quot;Und&quot;-Bedingung verbunden wird, einen Container zum Ausschließen hinzu. Fügen Sie Ihre Segmentdefinition &quot;One Hit Wonders&quot;(Seitenansichten gleich 1) zum Container Ausschließen hinzu.

![Bild 4](assets/Image-4.png)

Als Best Practice sollten Sie sicherstellen, dass Sie Ihre Container beschriften. Sie werden sich freuen, insbesondere da unsere Segmentdefinitionen komplexer werden.

Nachdem wir nun das Segment &quot;Kaufabsicht&quot;erstellt haben, können wir den Arbeitsbereich für die Datenqualität des Besuchsabsichten verwenden, um zu sehen, dass sich unser Segment für den Kaufabsichten gegenseitig mit unserem Segment &quot;Eins&quot;und &quot;Fertig&quot;ausschließt.

![Bild 5](assets/Image-5.png)

## Erstellen des Intent-Segments für Besuche bei der Datenaufbewahrung

Im Kreuzfahrtgeschäft kommen viele Gäste auf unsere Website, um eine Buchung zu verwalten, aber nicht unbedingt, um einen Kauf zu tätigen. Sie können auf die Website kommen, um Reisedaten einzugeben, ihre Reiseroute zu überprüfen, Abendreservierungen zu machen oder eine Reihe anderer Dinge, ohne für eine Kreuzfahrt einkaufen. Unsere Gäste können auch Ausflüge an der Küste oder andere Erlebnisse erwerben. Wir betrachten diese Verbesserungen als Teil der Aufbewahrung, daher halten wir sie von unserem Buchungssegment (das wir in dieser Blogserie &quot;Kauf&quot; nennen) getrennt.

Einzelhandelskunden können möglicherweise Renditen erwirtschaften oder ihr Treueprogramm verwalten. Abonnenten von Medien oder Technologie verwenden möglicherweise das Produkt. Wenn Ihr Gast auf Ihrer Website ist, um seine Beziehung zu Ihnen zu verwalten, ist dies ein Treuebesuch und wir sollten uns diese Signale ansehen. Und wenn Sie ein Online-Produkt anbieten, wie Media, Tech, Online Banking oder andere, gibt es wahrscheinlich viele andere Arten von Besuchsintentionssegmenten, die wir in dieser Reihe nicht diskutieren werden.

Wie beim Segment &quot;Kaufabsicht&quot;suchen wir sehr explizite Absichtserklärungen. Für mich gibt es einen kompletten Bereich der Website, der sich der Verwaltung einer Kreuzfahrt widmet, damit es einfach ist, diese Seiten zu identifizieren. Dies könnte für andere Unternehmen komplexer sein. Suchen Sie nach Signalen wie Anmeldungen, Kontoverwaltung, Besuchen zur Unterstützung von Seiten und Ähnliches.

Ich sollte beachten, dass &quot;Treue&quot;ein wenig ein unangenehmer Name für diesen Besuchsabsichten ist, da der Besucher nicht auf unserer Site ist, &quot;sodass ich als Kunde beibehalten werden kann&quot;. Treue ist unsere Absicht für diesen Besuch. Denken Sie einfach daran, für unsere Kunden einfühlsam zu sein und einen Kundenfokus zu pflegen!

### Verwenden von Analytics Workspace zur Identifizierung von Intent-Signalen

Auch hier hilft uns Analytics Workspace bei der Identifizierung des Bindungsabsichten. Sie können die Seiten, den Sitebereich oder die benutzerdefinierten Segmentdimensionen verwenden, um Ihre Seiten zu kategorisieren. Suchen Sie nach Seiten mit niedrigen Einkaufskonversionsraten. In unserem Fall haben die Seiten &quot;Online Check-In&quot;und &quot;Shore Excursion&quot;(Shorex) vergleichsweise niedrigere Konversionsraten als andere Seiten, die logischerweise mit dem Kauf und Einkauf verbunden sind.

![Bild 6](assets/Image-6.png)

Es empfiehlt sich auch, in Workspace nach Seiten mit hohem Traffic zu suchen. Überprüfen Sie die Liste der Seiten mit hohem Traffic-Aufkommen und entscheiden Sie, ob sie einen Bindungszweck angeben.

## Ausschließen anderer Segmente

Auch hier müssen sich unsere Segmente für Besuchsabsichten gegenseitig ausschließen und vollständig erschöpfend sein. Wenn du es noch nicht müde hast, das zu lesen, wirst du es tun! Für unser Bindungsabsichten-Segment ist es von entscheidender Bedeutung, Kaufabsichten auszuschließen.

Für die meisten von uns schließen sich Kaufabsichten und Bindungsabsichten nicht gegenseitig aus. Wir haben Gäste, die auf die Website kommen, um ihre bevorstehende Kreuzfahrt zu verwalten, aber auch um ihre nächste Reise zu buchen (danke!). Wenn Sie ein Restaurant sind, kann ein Besucher seine Treuepunkte überprüfen und dann eine Online-Bestellung aufgeben.

Auch wenn sich das Verhalten nicht gegenseitig ausschließt, müssen unsere Journey-Segmente für die Kundenanalyse verwendet werden. Wir können weitere sehr interessante Segmente erstellen, um die Überschneidung zwischen Kauf- und Treueverhalten zu analysieren. Für unsere aktuellen Zwecke müssen diese Segmente jedoch sich gegenseitig ausschließen.

Da die Nachfragegenerierung eines der Hauptziele des Marketing ist, schließt unser Segment zur Bindungsabsicht den Kaufabsichten aus. Wenn also jemand zur Verwaltung einer Kreuzfahrt auf unsere Website kommt, aber auch die Absicht anzeigt, eine neue Kreuzfahrt zu buchen, wird dieser Besuch zum Segment &quot;Kaufabsicht&quot;geleitet.

### Das Bindungsabsichtssegment im Segmentaufbau

Unsere Segmentdefinitionen werden immer deutlicher. Fügen Sie Besuche in Ihr Segment ein. Fügen Sie Ihre BindungsIntent-Signale hinzu. Für mich war das einfach. Wenn der Seitenname mit &quot;bge:&quot;(unseren gebuchten Gastseiten) beginnt, befinden Sie sich im Segment. Ich habe Seitenansichten hinzugefügt, die für zusätzliche Messungen größer sind als 1 (aber wir schließen trotzdem eine Trefferfrage unten aus).

Fügen Sie dann Container zum Ausschließen für Ihre Besuche &quot;One Hit Wonders&quot;und &quot;Purchase Intent&quot;hinzu. Stellen Sie sicher, dass Ihre Container mit der Bedingung &quot;Und&quot;verbunden sind.

![Bild 7](assets/Image-7.png)

Sehen Sie sich erneut Ihren Arbeitsbereich für die Datenqualität des Besuchsabsichten an, um sicherzustellen, dass sich Ihre Segmente gegenseitig ausschließen. Unsere Besuchsabsichten-Segmente nehmen eine schöne Form an!

![Bild 8](assets/Image-8.png)

An dieser Stelle haben wir drei unserer fünf Segmente für Besuchsabsichten konfiguriert. Wir sehen, dass sich diese Segmente gegenseitig ausschließen. In unserem nächsten Beitrag erstellen wir die endgültigen Segmente für Besuchsinteressen, Betrachtung und Bewusstsein, und unsere Segmente werden alle vollständig sein. Sobald die Segmente für den Besuchsabsichten eingerichtet sind, führen wir sie in besucherbasierte Segmente zusammen, die Sie für die Analyse und Personalisierung als sehr nützlich erachten.

## Autor

Dieses Dokument wurde verfasst von:

![Aaron Fossum](assets/aaron-headshot.png)

**Aaron Fossum**, Director, Digital Analytics

Adobe Analytics-Experte
