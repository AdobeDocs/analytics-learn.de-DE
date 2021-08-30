---
title: Verstehen und Verwenden von Journey IQ - Geräteübergreifende Analyse
description: Wenn Benutzer mit Ihrer Marke interagieren, tun sie dies auf viele Arten und auf mehreren Geräten. Die geräteübergreifende Analyse kann mit dem Adobe Experience Platform Identity-Dienst integriert werden, um zu ermitteln, wie Geräte Personen zugeordnet sind. Anschließend nutzt es diese Intelligenz, um eine geräteübergreifende Ansicht des Benutzerverhaltens zu erstellen. Dies führt dazu, dass Analysen an Personen durchgeführt werden können, nicht an Geräten.
feature: CDA
topics: null
activity: use
doc-type: article
team: Technical Marketing
kt: 4138
role: User
level: Intermediate
exl-id: 3748d5d7-d250-4057-8131-afdc66c80200
source-git-commit: fe861dfd541c1b9cb3b233fa3f56d55054305fd9
workflow-type: tm+mt
source-wordcount: '1641'
ht-degree: 4%

---

# Verstehen und Verwenden von [!DNL Journey IQ] - Geräteübergreifende Analyse

Wenn Benutzer mit Ihrer Marke interagieren, tun sie dies auf viele Arten und auf mehreren Geräten. Die geräteübergreifende Analyse kann mit dem [!DNL Adobe Experience Platform Identity Service] integriert werden, um zu ermitteln, wie Geräte Personen zugeordnet sind. Anschließend nutzt es diese Intelligenz, um eine geräteübergreifende Ansicht des Benutzerverhaltens zu erstellen. Dies führt dazu, dass Analysen an Personen durchgeführt werden können, nicht an Geräten.

## Überblick über die geräteübergreifende Analyse

### Ich bin nicht meine Geräte

Wenn Benutzer mit Ihrer Marke interagieren, tun sie dies auf viele Arten und auf mehreren &quot;Oberflächen&quot;oder &quot;Geräten&quot;. Sie können einen Webbrowser auf einem PC oder Mobilgerät verwenden oder eine mobile App verwenden. In der herkömmlichen digitalen Analyse, die in der Datenerfassung auf der Grundlage von Cookies aufwuchs, wird jede dieser Oberflächen als Unique Visitor dargestellt. Das bedeutet, dass jeder Ihrer menschlichen Benutzer als mehrere Unique Visitors dargestellt wird.

Hier ein Beispiel. Nehmen wir an, Isabelle interagierte wie folgt mit Ihrer Marke:

*Isabelle ist drei*
![BesucherHerkömmliche Analytics-Journey](assets/cda-isabelle-journey-traditional-analytics.png)

Isabels Journey wird mithilfe herkömmlicher Analysen in drei Teile zerteilt. Sie wird als drei Unique Visitors dargestellt, von denen jeder ein anderes Gerät zur Durchführung isolierter Aufgaben verwendet hat. Was wir brauchen, ist eine einheitliche, geräteübergreifende Sicht der Interaktionen von Isabelle. [!DNL Journey IQ: Cross-Device Analytics] bietet diese Ansicht.

*Isabelle ist eine*
![PersonGeräteübergreifende Analyse-Journey](assets/cda-isabelle-journey-cross-device-analytics.png)

### Eine geräteübergreifende Ansicht bietet bessere Analysen

Eine personenorientierte, geräteübergreifende Betrachtung des Verhaltens von Isabelle kann einen wesentlichen Unterschied zu Ihrer Analyse darstellen. Der herkömmliche besucherbasierte Ansatz vermittelt Ihnen beispielsweise kein vollständiges Bild der Effektivität des Marketing-Kanals. Schauen wir uns noch einmal die Journey von Isabelle an, die sich darauf konzentriert, auf welchen Kanal sie sich für ihre Produktansicht und für ihren Kauf verdient. Zur Vereinfachung wird die Attribution [!UICONTROL last-touch] verwendet. Dasselbe Problem tritt jedoch bei Verwendung eines beliebigen Attributionsmodells auf, wenn Sie Isabelles Verhalten in separate Besucher unterteilen. Die Verwendung der traditionellen Besucher-basierten Sicht auf die Welt liefert sehr unterschiedliche, sogar irreführende Ergebnisse:

*Herkömmliche Analytics- vs. geräteübergreifende*
![Analysesystem-Attribution](assets/channel-attribution.png)

Beachten Sie, dass der E-Mail-Kanal bei der geräteübergreifenden Ansicht sowohl für die Produktansicht als auch für den Kauf gewertet wird, was Isabelles reales Erlebnis genauer widerspiegelt.

Lesen Sie weiter, um mehr über Folgendes zu erfahren:

* Funktionsweise von [!DNL Cross-Device Analytics]
* Voraussetzungen für [!DNL Cross-Device Analytics]
* Interpretieren geräteübergreifender Daten
* Geräteübergreifende Daten in Analysis Workspace analysieren

## Funktionsweise von [!DNL Cross-Device Analytics]

[!DNL Journey IQ: Cross-Device Analytics (CDA)] integriert in die  [!DNL Adobe Experience Platform Identity Service], wobei entweder  [[!DNL Co-op Graph]](https://experienceleague.adobe.com/docs/device-co-op/using/home.html?lang=de) oder verwendet wird,  [!DNL Private Graph] um zu identifizieren, wie Geräte Personen zugeordnet sind. Anschließend nutzt es diese Intelligenz, um eine geräteübergreifende Ansicht des Benutzerverhaltens zu erstellen. Die geräteübergreifende Analyse umfasst unübertroffene Funktionen und Tools, mit denen Ihr Unternehmen die Nutzung mehrerer Geräte und das Kundenerlebnis auf diesen Geräten bei der Interaktion mit Ihrer Marke verstehen kann. Er befindet sich als Ebene unterhalb von Analysis Workspace, um mithilfe leistungsstarker Tools wie [!UICONTROL Fallout], [!DNL Flow], [!DNL Cohort], [!DNL Segment IQ] und [!DNL Attribution IQ] einen tiefen Einblick in die personenbasierte Zielgruppenanalyse und geräteübergreifende Attribution, Segmentierung und Journey-Analyse zu bieten.

### Der [!DNL Cross-Device Virtual Report Suite]

Die geräteübergreifende Analyse wird über eine spezielle geräteübergreifende [[!UICONTROL Virtual Report Suite]](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-about.html) präsentiert. Auf diese Weise können Sie die ursprüngliche gerätebasierte Report Suite weiterhin verwenden, während Sie geräteübergreifende Analysen in Ihre Organisation einführen. Die Einrichtung einer VRS für die geräteübergreifende Analyse ist einfach.

Wählen Sie in Schritt 1 des VRS-Builders die [!UICONTROL Report Suite] aus, die von Adobe als CDA-fähig konfiguriert wurde:

*Auswahl einer CDA-fähigen Basis (Quelle)  [!UICONTROL Report]*
![[!UICONTROL SuiteVirtual Report ] SuiteSchritt 1](assets/cda-vrs-step-one.png)

Aktivieren Sie dann [!UICONTROL Berichtszeitverarbeitung] und aktivieren Sie [!UICONTROL geräteübergreifendes Stitching]:

*Aktivieren der  [!UICONTROL Berichtszeitverarbeitung ] und  [!UICONTROL geräteübergreifenden]*
![[!UICONTROL ZuordnungVirtual Report ] SuiteSchritt 2](assets/cda-vrs-step-two.png)

Schließen Sie das VRS-Setup ab und speichern Sie es. Die VRS für die geräteübergreifende Analyse wird in Analysis Workspace mit einem speziellen Symbol daneben angezeigt, wie unten dargestellt:

*CDA-VRS in Analysis*
![[!UICONTROL Workspace auswählen Virtual Report ] SuiteSchritt 3](assets/cda-vrs-step-three.png)

>[!TIP]
>
>Sie können so viele CDA [!UICONTROL Virtual Report Suites] erstellen, wie Sie auf der CDA-fähigen Basis [!UICONTROL Report Suite] möchten.

### Wiederherstellen des Verlaufs

Manchmal dauert es eine Weile, bis sich Ihre Benutzer anmelden und [!DNL Co-op Graph] oder [!DNL Private Graph] die  verwenden, um sie zu identifizieren und ihre Geräte zuzuordnen. Die geräteübergreifende Analyse verwendet ein 30-tägiges Rückblickfenster, sodass ein zuvor nicht identifizierter Besucher bis zu 30 Tage in der Vergangenheit als Person erneut angezeigt werden kann.

Wie hilft das? Erinnern Sie sich an die Journey von Isabelle aus der obigen Diskussion:

![[!DNL Cross-Device Analytics] Journey](assets/cda-isabelle-journey-cross-device-analytics.png)

Es ist möglich, dass sich Isabelle erst kurz vor dem Kauf angemeldet hat und dass die [!DNL Co-op Graph] oder [!DNL Private Graph] die Geräte von Isabelle erst nach einem späteren Kauf zugeordnet haben. Aber der 30-tägige Rückblick der CDA ermöglicht es der CDA, Isabelles vergangenes Verhalten auf Personenebene erneut darzustellen und Ihnen die geräteübergreifende Ansicht ihrer benötigten Journey zu liefern.

>[!NOTE]
>
>Da der Verlauf neu angegeben werden kann, können sich Ihre Daten im Laufe der Zeit in einer CDA-fähigen [!UICONTROL Virtual Report Suite] ändern. Beachten Sie dies bei der Kommunikation von Einblicken aus einer CDA-basierten Analyse.

## Voraussetzungen für [!UICONTROL Geräteübergreifende Analyse]

Die geräteübergreifende Analyse ist in [[!DNL Analytics Ultimate]](https://helpx.adobe.com/legal/product-descriptions/adobe-analytics.html) enthalten. Ab September 2019 sind [!DNL Analytics Ultimate]-Kunden, die die unten aufgeführten Voraussetzungen erfüllen, zur Verwendung der geräteübergreifenden Analyse berechtigt. Die Voraussetzungen für die geräteübergreifende Analyse lauten wie folgt:

* Ihr Unternehmen muss Mitglied von [!DNL Adobe Experience Platform Identity Service] [[!DNL Co-op Graph]](https://experienceleague.adobe.com/docs/device-co-op/using/home.html) sein oder ein [!DNL Adobe Experience Platform Identity Service Private Graph] verwenden.
* Sie müssen alle erforderlichen Elemente für [!DNL Co-op Graph] oder [!DNL Private Graph] implementieren, einschließlich [Experience Cloud-ID (ECID)](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=de) und ID-Synchronisierung mit dem Diagramm. Beachten Sie, dass das [!DNL Co-op Graph] neben technischen Anforderungen auch andere rechtliche und vertragliche Anforderungen hat.
* Es ist derzeit nicht möglich, zwei IMS-Organisationen mit einem einzelnen [!DNL Private Graph] zu verwenden. Daher müssen Sie eine Standardisierung für eine IMS-Organisation vornehmen. In einigen Fällen ist es für einen Kunden mit mehreren IMS-Organisationen möglich, [!DNL Co-op Graph] in Verbindung mit der geräteübergreifenden Analyse zu verwenden.
* Die [!DNL Co-op graph] und [!DNL Private Graph] sowie bestimmte Komponenten der geräteübergreifenden Analyse werden in [!DNL Microsoft Azure] gehostet. Das bedeutet, dass [!DNL Analytics] Daten zwischen dem Datenverarbeitungscenter der Adobe und der Präsenz der Adobe in [!DNL Microsoft Azure] hin- und herkopiert werden. Einige [!DNL Analytics] Daten werden in [!DNL Azure] gespeichert. Ihr Unternehmen muss dieser Vereinbarung zustimmen.
* Die geräteübergreifende Analyse erfordert eine [!UICONTROL Report Suite]. Das heißt, die [!UICONTROL Report Suite], die Sie für die geräteübergreifende Analyse verwenden, muss Daten aus verschiedenen Gerätetypen oder &quot;Oberflächen&quot;enthalten, z. B. Desktop-Web, mobiles Web und mobile App. Ab September 2019 muss das Server-Aufrufvolumen für diese [!UICONTROL Report Suite] 100MM Server-Aufrufe/Tag oder weniger betragen. (Das Volumen der Server-Aufrufe wird in den nächsten Monaten steigen.)
* Ab September 2019 sind die [!DNL Co-op Graph] und [!DNL Private Graph] nur noch in Nordamerika verfügbar. Der Zeitplan für die Diagrammpräsenz in EMEA und APAC wird zu einem späteren Zeitpunkt bekannt gegeben. Wenn Sie sich in diesen Regionen befinden, empfehlen wir Ihnen, sich diese Voraussetzungen jetzt anzusehen, damit Sie bereit sind zu gehen, sobald das Diagramm verfügbar wird.

## Interpretieren geräteübergreifender Daten

### Personen, nicht Besucher

Innerhalb der geräteübergreifenden Analyse [!UICONTROL Virtual Report Suite] werden einige Änderungen angezeigt. Beispielsweise wird die Metrik [!UICONTROL Unique Visitors] durch zwei neue Metriken ersetzt: [!UICONTROL Personen] und [!UICONTROL Eindeutige Geräte]. Diese neuen Metriken geben Ihnen deutlich bessere Einblicke in die Zielgruppengröße.

*Personen und Unique*
![DevicesCDA- [!UICONTROL Metrik für Personen]](assets/cda-people-metric.png)

Im Segment Builder [[!UICONTROL a1/>](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html?lang=de) wurde der Segment-Container [!UICONTROL Besucher] durch einen Segment-Container [!UICONTROL Person] ersetzt. ] Mithilfe einer CDA-VRS können Sie geräteübergreifende Segmente erstellen, z. B.:

* Personen, die mehr als ein Gerät verwenden
* Personen, die ihre Journey auf einem Mobilgerät starten und dann später auf einem Desktop-Gerät kaufen
* Besuche, bei denen Benutzer mehrere Geräte zur Erfüllung einer Aufgabe verwenden

*Personenebenensegmente*
![[!DNL Segment Builder]  PersonContainer](assets/cda-segment-builder-person-container.png)

### Dimension-Persistenz

Innerhalb einer CDA-VRS bleiben Dimensionen wie [!DNL eVars] jetzt automatisch geräteübergreifend bestehen. Beispiel: ein [!DNL eVar] , der wie folgt konfiguriert ist:

* Zuordnung: Zuletzt verwendet (Letzter)
* Läuft ab nach: Kauf

wird nun automatisch von einem Gerät zum anderen beibehalten, bis das Kaufereignis ausgelöst wird.

## Geräteübergreifende Daten in Analysis Workspace analysieren

### Personenbasierte Zielgruppenanalyse

Haben Sie sich schon einmal gefragt, wie viele Menschen mit Ihrer Marke interagieren? Wollten Sie wissen, wie viele und welche Arten von Geräten sie verwenden? Wie überschneidet sich ihre Verwendung? Mithilfe einer CDA-VRS können Sie geräteübergreifende [Venn-Diagramme](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/venn.html?lang=de) und Geräte-pro-Person [Histogramme](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/histogram.html?lang=de) erstellen.

*Benutzerbasierte Zielgruppenanalyse*
![Venn und Histogramm](assets/cda-venn-and-histogram.png)

### Geräteübergreifend [!DNL Flow]

Mit CDA und Analysis Workspace können Sie visualisieren, wie Benutzer im [[!DNL Flow visualization]](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/flow/flow.html) von einem Gerät zum anderen wechseln. Sie können sehen, wo sie auf ihrer Journey abbrechen und wo sie weitermachen.

*[!DNL Flow]mit CDA*
![[!DNL Flow Visualization]](assets/cda-flow-viz.png)

### Geräteübergreifend [!DNL Fallout]

Wahrscheinlich verwenden Sie mehrere [[!DNL Fallout visualizations]](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/fallout/fallout-flow.html?lang=de), um zu analysieren, wie gut Benutzer es durch eine bestimmte Reihe von Schritten schaffen, bevor sie erfolgreich sind. Wussten Sie, dass Ihre Ansicht der [!DNL Fallout visualizations] bei der Verwendung herkömmlicher gerätebasierter Analysen eingeschränkt ist? Um erfolgreich durchfallen zu können, muss der nächste Schritt im selben Browser oder in der App wie der vorherige Schritt erfolgen. In der gerätebasierten Analyse sind Sie blind für Personen, die den nächsten Schritt auf einem anderen Gerät erfolgreich abgeschlossen haben.

Keine Sorge, die geräteübergreifende Analyse hat Sie abgedeckt. Die geräteübergreifende Analyse erstellt die geräteübergreifende Ansicht, die [!DNL Fallout visualizations] viel nützlicher macht. Schließlich ist es wirklich wichtig, ob die Person ihre Aufgabe letztendlich irgendwo erfüllt hat.

*[!DNL Fallout]mit CDA*
![[!DNL Fallout Visualization]](assets/cda-fallout-viz.png)

### [!DNL Cross-Device Attribution IQ]

Da die geräteübergreifende Analyse eine Schicht geräteübergreifender Daten unter Analysis Workspace erstellt, wird all Ihre Analyse geräteübergreifend aromatisiert. Ein leistungsstarkes Beispiel ist [[!DNL Attribution IQ]](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/attribution/attribution.html). [!DNL Attribution IQ] In Analysis Workspace können Sie mehrere Attributionsmodelle nebeneinander vergleichen. Mithilfe dieser Funktion mit der geräteübergreifenden Analyse können Sie jetzt vergleichen, wie verschiedene Geräte zum Erfolg beitragen.

Angenommen, Sie möchten verstehen, wie oft ein Mobiltelefon das erste Gerät ist, das in einer Interaktion verwendet wird, die letztendlich zum Erfolg führt. Dies entspricht der &quot;Akquise-Rate&quot;des Mobiltelefons. Mit CDA + [!DNL Attribution IQ] können Sie diese Analyse durchführen:

*[!DNL Attribution IQ]mit CDA*
![[!DNL Attribution IQ]](assets/cda-attribution-iq.png)

Weitere Informationen finden Sie in der [[!DNL Cross-Device Analytics] Hilfedokumentation](https://experienceleague.adobe.com/docs/analytics/components/cda/cda-home.html).
