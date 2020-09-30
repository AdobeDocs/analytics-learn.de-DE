---
title: Einführung und Verwendung von Journey IQ - geräteübergreifende Analyse
description: Wenn Benutzer mit Ihrer Marke interagieren, geschieht dies auf vielfältige Weise und auf mehreren Geräten. Geräteübergreifende Analysen werden mit dem Adobe Experience Platform-Identitätsdienst integriert, um herauszufinden, wie Geräte Personen zugeordnet werden. Anschließend nutzt es diese Intelligenz, um eine geräteübergreifende Ansicht des Benutzerverhaltens zu erstellen. Das führt dazu, dass man Analysen an Menschen und nicht an Geräten durchführen kann.
feature: cda
topics: null
audience: all
activity: use
doc-type: article
team: Technical Marketing
kt: 4138
translation-type: tm+mt
source-git-commit: 24ad92b0ccdf1112e3ed4a0968cd47db757598c3
workflow-type: tm+mt
source-wordcount: '1681'
ht-degree: 6%

---


# Verstehen und Verwenden [!DNL Journey IQ] - Geräteübergreifende Analyse

Wenn Benutzer mit Ihrer Marke interagieren, geschieht dies auf vielfältige Weise und auf mehreren Geräten. Geräteübergreifende Analysen werden mit dem integriert, [!DNL Adobe Experience Platform Identity Service] um zu ermitteln, wie Geräte Benutzern zugeordnet werden. Anschließend nutzt es diese Intelligenz, um eine geräteübergreifende Ansicht des Benutzerverhaltens zu erstellen. Das führt dazu, dass man Analysen an Menschen und nicht an Geräten durchführen kann.

## Übersicht über geräteübergreifende Analysen

### Ich bin nicht meine Geräte

Wenn Benutzer mit Ihrer Marke interagieren, geschieht dies auf vielerlei Weise und auf mehreren &quot;Oberflächen&quot;oder &quot;Geräten&quot;. Sie können einen Webbrowser auf einem PC oder Mobilgerät oder eine mobile App verwenden. In der klassischen Digitalanalyse, die in der Datenerfassung auf der Grundlage von Cookies aufwuchs, wird jede dieser Oberflächen als individueller &quot;Besucher&quot;dargestellt. Das bedeutet, dass jeder Ihrer menschlichen Benutzer als mehrere individuelle Besucher dargestellt wird.

Hier ein Beispiel. Nehmen wir an, Isabelle würde wie folgt mit Ihrer Marke interagieren:

*Isabelle ist drei Besucher*![Traditionelle Analytics-Reise](assets/cda-isabelle-journey-traditional-analytics.png)

Mit der traditionellen Analyse wird Isabels Reise in drei Teile aufgeteilt. Sie wird als drei individuelle Besucher dargestellt, von denen jeder ein anderes Gerät verwendet hat, um isolierte Aufgaben durchzuführen. Was wir brauchen, ist eine einheitliche, geräteübergreifende Ansicht von Isabels Interaktionen. [!DNL Journey IQ: Cross-Device Analytics] bietet diese Ansicht.

*Isabelle ist eine Person* für![geräteübergreifende Analytics-Reise](assets/cda-isabelle-journey-cross-device-analytics.png)

### Eine geräteübergreifende Ansicht bietet bessere Analysen

Eine personalzentrierte, geräteübergreifende Ansicht von Isabels Verhalten kann Ihre Analyse erheblich beeinflussen. So vermittelt Ihnen beispielsweise der herkömmliche Besucher-basierte Ansatz nicht das komplette Bild der Effektivität des Marketing-Kanals. Schauen wir uns einmal mehr Isabels Reise an, wobei wir uns darauf konzentrieren, welchen Kanal ihre Ansicht und ihren Einkauf zugeschrieben werden. Wir verwenden die [!UICONTROL Last Touch] -Zuordnung zur Einfachheit, aber dasselbe Problem tritt bei jedem Zuordnungsmodell auf, wenn Sie Isabels Verhalten in verschiedene Besucher unterteilen. Die Verwendung der traditionellen Besucher-basierten Ansicht der Welt führt zu ganz anderen, sogar irreführenden Ergebnissen:

*Klassische Analytics- oder geräteübergreifende Analytics*-![Kanal-Zuordnung](assets/channel-attribution.png)

Beachten Sie, dass der E-Mail-Kanal mit der geräteübergreifenden Ansicht sowohl für die Ansicht als auch für den Einkauf, der Isabels wahrheitsgetreuere Welterfahrung widerspiegelt, eine Anerkennung erhält.

Lesen Sie weiter, um mehr zu erfahren über:

* How [!DNL Cross-Device Analytics] Works
* Voraussetzungen für [!DNL Cross-Device Analytics]
* Geräteübergreifende Daten interpretieren
* Geräteübergreifende Daten in Analysis Workspace analysieren

## How [!DNL Cross-Device Analytics] Works

[!DNL Journey IQ: Cross-Device Analytics (CDA)] integriert mit dem [!DNL Adobe Experience Platform Identity Service]unter Verwendung des [[!DNL-Co-op-Diagramms]](https://docs.adobe.com/content/help/de-DE/device-co-op/using/home.html) oder [!DNL Private Graph] zur Identifizierung, wie Geräte Menschen zugeordnet werden. Anschließend nutzt es diese Intelligenz, um eine geräteübergreifende Ansicht des Benutzerverhaltens zu erstellen. CDA bietet unübertroffene Funktionen und Tools, mit denen Ihr Unternehmen die Nutzung mehrerer Geräte und die Kundenerfahrung auf all diesen Geräten in ihrer Interaktion mit Ihrer Marke verstehen kann. Er befindet sich unterhalb von Analysis Workspace, um einen tiefen Einblick in die personalbasierte Analyse der Audience und die geräteübergreifende Zuordnung, Segmentierung und Analyse der Reise zu erhalten, und zwar mithilfe leistungsfähiger Tools wie [!UICONTROL Trichteranalyse], [!DNL Flow], [!DNL Cohort][!DNL Segment IQ] und [!DNL Attribution IQ].

### Der [!DNL Cross-Device Virtual Report Suite]

CDA wird über eine spezielle geräteübergreifende [[!UICONTROL Virtual Report Suite]](https://docs.adobe.com/content/help/de-DE/analytics/components/virtual-report-suites/vrs-about.html)präsentiert. Auf diese Weise können Sie die ursprüngliche gerätebasierte Report Suite weiterhin verwenden, während Sie geräteübergreifende Analysen in Ihrem Unternehmen einführen. Die Einrichtung einer CDA VRS ist einfach.

Wählen Sie in Schritt 1 des VRS-Builders die [!UICONTROL Report Suite] aus, die von der Adobe als CDA-fähig konfiguriert wurde:

*Wählen Sie eine CDA-fähige Basis-(Quell-)[!UICONTROL Report Suite]*![[!UICONTROL Virtual Report Suite] Schritt 1](assets/cda-vrs-step-one.png)

Aktivieren Sie dann die [!UICONTROL Berichtszeitverarbeitung] und aktivieren Sie die [!UICONTROL geräteübergreifende Suche]:

*Aktivieren der[!UICONTROL Berichtszeitverarbeitung]und der[!UICONTROL geräteübergreifenden Verknüpfung]* der![[!UICONTROL Virtual Report Suite] Schritt 2](assets/cda-vrs-step-two.png)

Schließen Sie das VRS-Setup ab und speichern Sie es. Die CDA-VRS wird in Analysis Workspace mit einem Sondersymbol angezeigt, das wie folgt dargestellt ist:

*Wählen Sie die CDA VRS in Analysis Workspace*![[!UICONTROL Virtual Report Suite] Schritt 3](assets/cda-vrs-step-three.png)

>[!TIP]
>
>Sie können beliebig viele CDA- [!UICONTROL Virtual Report Suites] über der CDA-fähigen Basis- [!UICONTROL Report Suite]erstellen.

### Wiederherstellen des Verlaufs

Manchmal dauert es eine Weile, bis Ihre Benutzer sich anmelden und die Geräte identifizieren [!DNL Co-op Graph] oder [!DNL Private Graph] zuordnen können. CDA verwendet ein 30-tägiges Lookback-Fenster, mit dem ein zuvor nicht identifizierter Besucher bis zu 30 Tage in der Vergangenheit erneut aufgeführt werden kann.

Wie hilft das? Erinnern Sie sich an die Benutzerreise von Isabelle aus der obigen Diskussion:

![[!DNL Cross-Device Analytics] Reise](assets/cda-isabelle-journey-cross-device-analytics.png)

Es ist möglich, dass sich Isabelle erst kurz vor dem Kauf angemeldet hat und dass die Geräte von Isabelle erst irgendwann nach ihrem Kauf zugeordnet wurden [!DNL Co-op Graph] oder [!DNL Private Graph] nicht zugeordnet wurden. Aber CDAs 30-Tage-Lookback ermöglicht es CDA, Isabels vergangenes Verhalten auf der persönlichen Ebene neu zu erklären und Ihnen die geräteübergreifende Ansicht ihrer Reise zu geben, die Sie brauchen.

>[!NOTE]
>
>Da der Verlauf neu festgelegt werden kann, können sich Ihre Daten im Laufe der Zeit in einer CDA-fähigen [!UICONTROL Virtual Report Suite]ändern. Berücksichtigen Sie dies, wenn Sie Einblicke aus einer CDA-basierten Analyse übermitteln.

## Voraussetzungen für [!UICONTROL geräteübergreifende Analysen]

CDA ist im Lieferumfang von [[!DNL Analytics Ultimate]](https://helpx.adobe.com/legal/product-descriptions/adobe-analytics.html)enthalten. Ab September 2019 können [!DNL Analytics Ultimate] Kunden, die die unten aufgeführten Voraussetzungen erfüllen, CDA nutzen. Voraussetzung für CDA sind:

* Ihre Firma muss Mitglied des [!DNL Adobe Experience Platform Identity Service] [!DNL-Co-op-Diagramms] [sein oder eine](https://docs.adobe.com/content/help/de-DE/device-co-op/using/home.html)[!DNL Adobe Experience Platform Identity Service Private Graph].
* Sie müssen alles implementieren, was für die Synchronisierung von [!DNL Co-op Graph] Experience Cloud-ID (ECID) [!DNL Private Graph] und IDs mit dem Diagramm erforderlich ist oder [](https://docs.adobe.com/content/help/de-DE/id-service/using/home.html) inklusive. Beachten Sie, dass die [!DNL Co-op Graph] Agentur neben technischen Anforderungen auch andere rechtliche und vertragliche Anforderungen hat.
* Es ist derzeit nicht möglich, zwei IMS-Orgs mit einem einzigen zu verwenden, [!DNL Private Graph]daher müssen Sie auf einem IMS-Org standardisieren. In einigen Fällen ist es möglich, dass ein Kunde mit mehreren IMS-Orgs das [!DNL Co-op Graph] in Verbindung mit CDA verwenden kann.
* Die [!DNL Co-op graph] und [!DNL Private Graph]sowie bestimmte Komponenten von CDA werden in gehostet [!DNL Microsoft Azure]. Dies bedeutet, dass [!DNL Analytics] Daten zwischen dem Datenverarbeitungscenter der Adobe und der Präsenz der Adobe in [!DNL Microsoft Azure]ein- und auskopiert werden. Einige [!DNL Analytics] Daten werden in gespeichert [!DNL Azure]. Ihre Firma muss dieser Vereinbarung zustimmen.
* CDA erfordert eine geräteübergreifende [!UICONTROL Report Suite]. Das heißt, die [!UICONTROL Report Suite] , die Sie für CDA verwenden, muss Daten aus verschiedenen Gerätetypen oder &quot;Oberflächen&quot;wie Desktop-Web, mobiles Web und mobile App enthalten. Ab September 2019 muss das Serveraufrufvolumen für diese [!UICONTROL Report Suite] 100-MM-Serveraufrufe pro Tag oder weniger betragen. (In den nächsten Monaten werden die Mengenbeschränkungen für Server-Aufrufe zunehmen.)
* Seit September 2019 gibt es das [!DNL Co-op Graph] und nur in Nordamerika [!DNL Private Graph] . Der Zeitplan für die Graphpräsenz in EMEA und APAC wird zu einem späteren Zeitpunkt bekannt gegeben. Wenn Sie sich in diesen Regionen befinden, empfehlen wir Ihnen, diese Voraussetzungen jetzt zu Beginn zu prüfen, damit Sie bereit sind zu gehen, sobald das Diagramm verfügbar ist.

## Geräteübergreifende Daten interpretieren

### Personen, nicht Besucher

Innerhalb der CDA [!UICONTROL Virtual Report Suite]werden Sie einige Änderungen sehen. Beispielsweise wird die Metrik [!UICONTROL Individuelle Besucher] durch zwei neue Metriken ersetzt: [!UICONTROL Personen] und [!UICONTROL Unique Devices]. Diese neuen Metriken geben Ihnen deutlich bessere Einblicke in die Größe der Audience.

*Metrik &quot;Personen und Unique Devices*![CDA- [!UICONTROL Personen&quot;]](assets/cda-people-metric.png)

Im [[!UICONTROL Segmentaufbau]](https://docs.adobe.com/content/help/de-DE/analytics/components/segmentation/segmentation-workflow/seg-build.html)wurde der Segment-Container [!UICONTROL Besucher] durch einen Segment-Container [!UICONTROL Person] ersetzt. Mithilfe einer CDA-VRS können Sie geräteübergreifende Segmente erstellen, z. B.:

* Personen, die mehr als ein Gerät verwenden
* Personen, die ihre Reise auf einem Mobilgerät beginnen und dann später auf einem Desktop-Gerät erwerben
* Besuche, bei denen Benutzer mehr als ein Gerät zum Durchführen einer Aufgabe verwenden

*Segmente*![[!DNL Segment Builder] auf [!UICONTROL Benutzerebene] Container](assets/cda-segment-builder-person-container.png)

### Dimension Persistenz

Innerhalb einer CDA-VRS bleiben Dimensionen wie [!DNL eVars] jetzt automatisch geräteübergreifend erhalten. Beispiel: Eine [!DNL eVar] , die wie folgt konfiguriert ist:

* Zuordnung: Zuletzt verwendet (Letzter)
* Läuft ab nach: Kauf

wird nun automatisch von einem Gerät zum nächsten fortgesetzt, bis das Ereignis &quot;Kauf&quot;ausgelöst wird.

## Geräteübergreifende Daten in Analysis Workspace analysieren

### Analyse der personellen Audience

Haben Sie sich schon einmal gefragt, wie viele Menschen mit Ihrer Marke interagieren? Wollten Sie wissen, wie viele und welche Geräte sie verwenden? Wie überschneidet sich ihre Nutzung? Mithilfe einer CDA-VRS können Sie geräteübergreifende [Venn-Diagramme](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/visualizations/venn.html) und Geräte-pro-Person- [Histogramme](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/visualizations/histogram.html)erstellen.

*Analyse* der Audience![Venn und Histogramm](assets/cda-venn-and-histogram.png)

### Geräteübergreifend [!DNL Flow]

Mit CDA und Analysis Workspace können Sie visualisieren, wie sich Menschen im Laufe der Zeit von einem Gerät zum nächsten bewegen. Dies geschieht in der Visualisierung des [[!DNL-Flusses]](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/visualizations/flow/flow.html). Sie können sehen, wo sie auf ihrer Reise aussteigen und wo sie weitermachen.

*[!DNL Flow]mit CDA*
![[!DNL Flow Visualization]](assets/cda-flow-viz.png)

### Geräteübergreifend [!DNL Fallout]

Wahrscheinlich verwenden Sie mehrere [[!DNL-Fallout-Visualisierungen]](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/visualizations/fallout/fallout-flow.html) , um zu analysieren, wie gut Benutzer es durch eine bestimmte Reihe von Schritten machen, bevor sie Erfolg erzielen. Wussten Sie, dass Ihre Ansicht dieser Daten bei der Verwendung herkömmlicher gerätebasierter Analysen eingeschränkt [!DNL Fallout visualizations] ist? Um erfolgreich durchlaufen zu können, muss der nächste Schritt im selben Browser oder in derselben App wie der vorherige Schritt erfolgen. Bei der gerätebasierten Analyse sind Sie blind für Personen, die den nächsten Schritt auf einem anderen Gerät erfolgreich abgeschlossen haben.

Keine Sorge, CDA hat Sie abgedeckt. CDA erstellt eine geräteübergreifende Ansicht, die [!DNL Fallout visualizations] viel nützlicher ist. Schließlich ist es wirklich wichtig, ob der Mensch letztlich irgendwo in seiner Aufgabe Erfolg hatte.

*[!DNL Fallout]mit CDA*
![[!DNL Fallout Visualization]](assets/cda-fallout-viz.png)

### [!DNL Cross-Device Attribution IQ]

Da CDA eine Schicht geräteübergreifender Daten unter Analysis Workspace erstellt, wird Ihre gesamte Analyse geräteübergreifend aromatisiert. Ein gutes Beispiel dafür ist der [[!DNL Attribution IQ]](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/attribution/models.html). [!DNL Attribution IQ] in Analysis Workspace können Sie mehrere Zuordnungsmodelle nebeneinander vergleichen. Mithilfe dieser Funktion können Sie jetzt vergleichen, wie verschiedene Geräte zum Erfolg beitragen.

Angenommen, Sie möchten verstehen, wie oft ein Mobiltelefon das erste Gerät ist, das in einer Interaktion verwendet wird, die letztlich zum Erfolg führt. Dies entspricht der &quot;Akquise-Rate&quot; des Mobiltelefons. Mit CDA + [!DNL Attribution IQ] können Sie diese Analyse durchführen:

*[!DNL Attribution IQ]mit CDA*
![[!DNL Attribution IQ]](assets/cda-attribution-iq.png)

For more information, see the [[!DNL Cross-Device Analytics] help documentation](https://docs.adobe.com/content/help/de-DE/analytics/components/cda/cda-home.html).
