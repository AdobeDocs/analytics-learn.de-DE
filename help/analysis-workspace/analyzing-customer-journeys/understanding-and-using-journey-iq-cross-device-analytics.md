---
title: Verstehen und Verwenden von Journey IQ - geräteübergreifende Analyse
description: Wenn Benutzer mit Ihrer Marke interagieren, geschieht dies auf vielfältige Weise und auf mehreren Geräten. Geräteübergreifende Analysen werden mit dem Adobe Experience Platform-Identitätsdienst integriert, um herauszufinden, wie Geräte Personen zugeordnet werden. Anschließend nutzt es diese Intelligenz, um eine geräteübergreifende Ansicht des Benutzerverhaltens zu erstellen. Das führt dazu, dass man Analysen an Menschen und nicht an Geräten durchführen kann.
feature: CDA
topics: null
activity: use
doc-type: article
team: Technical Marketing
kt: 4138
role: Business Practitioner
level: Intermediate
translation-type: tm+mt
source-git-commit: f3b3fa7d91b0cb21005b57768ca23ed6700fcc03
workflow-type: tm+mt
source-wordcount: '1667'
ht-degree: 6%

---


# Grundlegendes und Verwenden von [!DNL Journey IQ] - Geräteübergreifende Analyse

Wenn Benutzer mit Ihrer Marke interagieren, geschieht dies auf vielfältige Weise und auf mehreren Geräten. Geräteübergreifende Analysen werden mit dem [!DNL Adobe Experience Platform Identity Service] integriert, um zu ermitteln, wie Geräte Benutzern zugeordnet werden. Anschließend nutzt es diese Intelligenz, um eine geräteübergreifende Ansicht des Benutzerverhaltens zu erstellen. Das führt dazu, dass man Analysen an Menschen und nicht an Geräten durchführen kann.

## Übersicht über geräteübergreifende Analysen

### Ich bin nicht meine Geräte

Wenn Benutzer mit Ihrer Marke interagieren, geschieht dies auf vielerlei Weise und auf mehreren &quot;Oberflächen&quot;oder &quot;Geräten&quot;. Sie können einen Webbrowser auf einem PC oder Mobilgerät oder eine mobile App verwenden. In der klassischen Digitalanalyse, die in der Datenerfassung auf der Grundlage von Cookies aufwuchs, wird jede dieser Oberflächen als individueller &quot;Besucher&quot;dargestellt. Das bedeutet, dass jeder Ihrer menschlichen Benutzer als mehrere individuelle Besucher dargestellt wird.

Hier ein Beispiel. Nehmen wir an, Isabelle würde wie folgt mit Ihrer Marke interagieren:

*Isabelle ist drei*
![BesucherTraditionelle Analytics-Journey](assets/cda-isabelle-journey-traditional-analytics.png)

Mit der traditionellen Analyse wird Isabels Journey in drei Teile zerteilt. Sie wird als drei individuelle Besucher dargestellt, von denen jeder ein anderes Gerät verwendet hat, um isolierte Aufgaben durchzuführen. Was wir brauchen, ist eine einheitliche, geräteübergreifende Ansicht von Isabels Interaktionen. [!DNL Journey IQ: Cross-Device Analytics] bietet diese Ansicht.

*Isabelle ist eine*
![PersonDevice-übergreifende Analytics-Journey](assets/cda-isabelle-journey-cross-device-analytics.png)

### Eine geräteübergreifende Ansicht bietet bessere Analysen

Eine personalzentrierte, geräteübergreifende Ansicht von Isabels Verhalten kann Ihre Analyse erheblich beeinflussen. So vermittelt Ihnen beispielsweise der herkömmliche Besucher-basierte Ansatz nicht das komplette Bild der Effektivität des Marketing-Kanals. Schauen wir uns noch einmal Isabels Journey an, in der es darum geht, welchen Kanal ihre Ansicht und ihren Einkauf gutgeschrieben werden. Wir verwenden zur Vereinfachung [!UICONTROL Last-Touch]-Zuordnung, aber dasselbe Problem tritt bei jedem Zuordnungsmodell auf, wenn Sie Isabels Verhalten in separate Besucher unterteilen. Die Verwendung der traditionellen Besucher-basierten Ansicht der Welt führt zu ganz anderen, sogar irreführenden Ergebnissen:

*Traditionelle Analytics- oder geräteübergreifende*
![Analytics-Kanalzuordnung](assets/channel-attribution.png)

Beachten Sie, dass der E-Mail-Kanal mit der geräteübergreifenden Ansicht sowohl für die Ansicht als auch für den Einkauf, der Isabels wahrheitsgetreuere Welterfahrung widerspiegelt, eine Anerkennung erhält.

Lesen Sie weiter, um mehr zu erfahren über:

* So funktioniert [!DNL Cross-Device Analytics]
* Voraussetzungen für [!DNL Cross-Device Analytics]
* Geräteübergreifende Daten interpretieren
* Geräteübergreifende Daten in Analysis Workspace analysieren

## So funktioniert [!DNL Cross-Device Analytics]

[!DNL Journey IQ: Cross-Device Analytics (CDA)] integriert in die  [!DNL Adobe Experience Platform Identity Service]und verwendet entweder die  [[!DNL Co-op Graph]](https://docs.adobe.com/content/help/de-DE/device-co-op/using/home.html) oder  [!DNL Private Graph] um zu identifizieren, wie Geräte zu Personen zugeordnet werden. Anschließend nutzt es diese Intelligenz, um eine geräteübergreifende Ansicht des Benutzerverhaltens zu erstellen. CDA bietet unübertroffene Funktionen und Tools, mit denen Ihr Unternehmen die Nutzung mehrerer Geräte und die Kundenerfahrung auf all diesen Geräten in ihrer Interaktion mit Ihrer Marke verstehen kann. Er befindet sich als Ebene unter Analysis Workspace, um einen tiefen Einblick in die personalbasierte Analyse der Audience und geräteübergreifende Zuordnung, Segmentierung und Journey-Analyse zu erhalten, indem leistungsstarke Tools wie [!UICONTROL Trichteranalyse], [!DNL Flow], [!DNL Cohort], [!DNL Segment IQ] und [!DNL Attribution IQ] eingesetzt werden.

### Der [!DNL Cross-Device Virtual Report Suite]

CDA wird über eine spezielle geräteübergreifende [[!UICONTROL Virtual Report Suite]](https://docs.adobe.com/content/help/de-DE/analytics/components/virtual-report-suites/vrs-about.html) präsentiert. Auf diese Weise können Sie die ursprüngliche gerätebasierte Report Suite weiterhin verwenden, während Sie geräteübergreifende Analysen in Ihrem Unternehmen einführen. Die Einrichtung einer CDA VRS ist einfach.

Wählen Sie in Schritt eins des VRS-Builders die [!UICONTROL Report Suite], die von Adobe als CDA-fähig konfiguriert wurde:

*Wählen Sie eine CDA-fähige Basis-(Quell-) [!UICONTROL Report]*
![[!UICONTROL SuiteVirtual Report ] SuiteSchritt 1](assets/cda-vrs-step-one.png)

Schalten Sie dann [!UICONTROL Berichtszeitverarbeitung] ein und aktivieren Sie [!UICONTROL geräteübergreifendes Zuordnen]:

*Aktivieren der  [!UICONTROL Berichtszeitverarbeitung ] und  [!UICONTROL geräteübergreifenden]*
![[!UICONTROL SucheVirtual Report ] SuiteSchritt 2](assets/cda-vrs-step-two.png)

Schließen Sie das VRS-Setup ab und speichern Sie es. Die CDA-VRS wird in Analysis Workspace mit einem Sondersymbol angezeigt, das wie folgt dargestellt ist:

*Wählen Sie die CDA VRS in Analyse*
![[!UICONTROL WorkspaceVirtual Report ] SuiteSchritt drei](assets/cda-vrs-step-three.png)

>[!TIP]
>
>Sie können so viele CDA [!UICONTROL Virtual Report Suites] erstellen, wie Sie möchten, und zwar über der CDA-fähigen Basis [!UICONTROL Report Suite].

### Wiederherstellen des Verlaufs

Manchmal dauert es eine Weile, bis sich Ihre Benutzer anmelden und [!DNL Co-op Graph] oder [!DNL Private Graph], um sie zu identifizieren und ihre Geräte zuzuordnen. CDA verwendet ein 30-tägiges Lookback-Fenster, mit dem ein zuvor nicht identifizierter Besucher bis zu 30 Tage in der Vergangenheit erneut aufgeführt werden kann.

Wie hilft das? Nehmen Sie die Journey von Isabelle aus der oben genannten Diskussion in Erinnerung:

![[!DNL Cross-Device Analytics] Journey](assets/cda-isabelle-journey-cross-device-analytics.png)

Es ist möglich, dass sich Isabelle erst kurz vor dem Kauf angemeldet hat und dass die [!DNL Co-op Graph] oder [!DNL Private Graph] die Isabelle-Geräte erst irgendwann nach ihrem Kauf zugeordnet haben. Aber CDAs 30-Tage-Lookback ermöglicht es CDA, Isabels vergangenes Verhalten auf der persönlichen Ebene neu zu erklären und Ihnen die geräteübergreifende Ansicht ihrer Journey zu bieten, die Sie brauchen.

>[!NOTE]
>
>Da der Verlauf neu angegeben werden kann, können sich Ihre Daten im Laufe der Zeit in einer CDA-fähigen [!UICONTROL Virtual Report Suite] ändern. Berücksichtigen Sie dies, wenn Sie Einblicke aus einer CDA-basierten Analyse übermitteln.

## Voraussetzungen für [!UICONTROL Geräteübergreifende Analysen]

CDA ist in [[!DNL Analytics Ultimate]](https://helpx.adobe.com/legal/product-descriptions/adobe-analytics.html) enthalten. Ab September 2019 sind [!DNL Analytics Ultimate]-Kunden, die die unten aufgeführten Voraussetzungen erfüllen, berechtigt, CDA zu verwenden. Voraussetzung für CDA sind:

* Ihre Firma muss Mitglied von [!DNL Adobe Experience Platform Identity Service] [[!DNL Co-op Graph]](https://docs.adobe.com/content/help/en/device-co-op/using/home.html) sein oder ein [!DNL Adobe Experience Platform Identity Service Private Graph] verwenden.
* Sie müssen alle erforderlichen Elemente für [!DNL Co-op Graph] oder [!DNL Private Graph] implementieren, einschließlich [Experience Cloud-ID (ECID)](https://docs.adobe.com/content/help/de-DE/id-service/using/home.html) und ID-Synchronisierung mit dem Diagramm. Beachten Sie, dass das [!DNL Co-op Graph] neben technischen Anforderungen auch andere rechtliche und vertragliche Anforderungen hat.
* Es ist derzeit nicht möglich, zwei IMS-Orgs mit einem einzelnen [!DNL Private Graph] zu verwenden. Daher müssen Sie auf einem IMS-Org standardisieren. In einigen Fällen ist es für einen Kunden mit mehreren IMS-Orgs möglich, das [!DNL Co-op Graph] in Verbindung mit CDA zu verwenden.
* Die Komponenten [!DNL Co-op graph] und [!DNL Private Graph] sowie bestimmte Komponenten von CDA werden in [!DNL Microsoft Azure] gehostet. Das bedeutet, dass [!DNL Analytics]-Daten zwischen dem Datenverarbeitungscenter der Adobe und der Präsenz der Adobe in [!DNL Microsoft Azure] hin- und herkopiert werden. Einige [!DNL Analytics]-Daten werden in [!DNL Azure] gespeichert. Ihre Firma muss dieser Vereinbarung zustimmen.
* CDA erfordert eine &quot;geräteübergreifende&quot; [!UICONTROL Report Suite]. Das heißt, die [!UICONTROL Report Suite], die Sie für CDA verwenden, muss Daten aus verschiedenen Gerätetypen oder &quot;Oberflächen&quot;wie Desktop-Web, mobiles Web und mobile App enthalten. Ab September 2019 muss das Serveraufrufvolumen für diese [!UICONTROL Report Suite] 100-MM-Serveraufrufe/Tag oder weniger betragen. (In den nächsten Monaten werden die Mengenbeschränkungen für Server-Aufrufe zunehmen.)
* Seit September 2019 sind die [!DNL Co-op Graph] und [!DNL Private Graph] nur in Nordamerika verfügbar. Der Zeitplan für die Graphpräsenz in EMEA und APAC wird zu einem späteren Zeitpunkt bekannt gegeben. Wenn Sie sich in diesen Regionen befinden, empfehlen wir Ihnen, diese Voraussetzungen jetzt zu Beginn zu prüfen, damit Sie bereit sind zu gehen, sobald das Diagramm verfügbar ist.

## Geräteübergreifende Daten interpretieren

### Personen, nicht Besucher

Innerhalb der CDA [!UICONTROL Virtual Report Suite] werden einige Änderungen angezeigt. Beispielsweise wird die Metrik [!UICONTROL Individuelle Besucher] durch zwei neue Metriken ersetzt: [!UICONTROL Personen] und [!UICONTROL Unique Devices]. Diese neuen Metriken geben Ihnen deutlich bessere Einblicke in die Größe der Audience.

*Personen und Unique*
![DevicesCDA-Metrik  [!UICONTROL &quot;Personen&quot;]](assets/cda-people-metric.png)

Im Segmentaufbau [[!UICONTROL unter ]](https://docs.adobe.com/content/help/de-DE/analytics/components/segmentation/segmentation-workflow/seg-build.html) wurde der Container [!UICONTROL Besucher] durch den Container [!UICONTROL Person] ersetzt. Mithilfe einer CDA-VRS können Sie geräteübergreifende Segmente erstellen, z. B.:

* Personen, die mehr als ein Gerät verwenden
* Personen, die ihre Journey auf einem Mobilgerät beginnen und dann später auf einem Desktop-Gerät erwerben
* Besuche, bei denen Benutzer mehr als ein Gerät zum Durchführen einer Aufgabe verwenden

*Segmente auf*
![[!DNL Segment Builder]  BenutzerebenePersonContainer](assets/cda-segment-builder-person-container.png)

### Dimension Persistenz

Innerhalb einer CDA-VRS bleiben Dimensionen wie [!DNL eVars] jetzt automatisch geräteübergreifend erhalten. Beispiel: Ein [!DNL eVar], das wie folgt konfiguriert ist:

* Zuordnung: Zuletzt verwendet (Letzter)
* Läuft ab nach: Kauf

wird nun automatisch von einem Gerät zum nächsten fortgesetzt, bis das Ereignis &quot;Kauf&quot;ausgelöst wird.

## Geräteübergreifende Daten in Analysis Workspace analysieren

### Analyse der personellen Audience

Haben Sie sich schon einmal gefragt, wie viele Menschen mit Ihrer Marke interagieren? Wollten Sie wissen, wie viele und welche Geräte sie verwenden? Wie überschneidet sich ihre Nutzung? Mithilfe einer CDA-VRS können Sie geräteübergreifende [Venn-Diagramme](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/visualizations/venn.html) und Geräte-pro-Person [Histogramme](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/visualizations/histogram.html) erstellen.

*Personenbasierte*
![Analyse der AudienceVenn- und Histogramm-Analyse](assets/cda-venn-and-histogram.png)

### Geräteübergreifend [!DNL Flow]

Mit CDA und Analysis Workspace können Sie visualisieren, wie Personen im [[!DNL Flow visualization]](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/visualizations/flow/flow.html) von einem Gerät zum nächsten wechseln. Sie können sehen, wo sie in ihrer Journey aussteigen und wo sie weitermachen.

*[!DNL Flow]mit CDA*
![[!DNL Flow Visualization]](assets/cda-flow-viz.png)

### Geräteübergreifend [!DNL Fallout]

Wahrscheinlich verwenden Sie mehrere [[!DNL Fallout visualizations]](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/visualizations/fallout/fallout-flow.html), um zu analysieren, wie gut Benutzer es durch eine bestimmte Reihe von Schritten machen, bevor Sie Erfolg erzielen. Wussten Sie, dass Ihre Ansicht dieser [!DNL Fallout visualizations] bei der Verwendung herkömmlicher gerätebasierter Analysen eingeschränkt ist? Um erfolgreich durchlaufen zu können, muss der nächste Schritt im selben Browser oder in derselben App wie der vorherige Schritt erfolgen. Bei der gerätebasierten Analyse sind Sie blind für Personen, die den nächsten Schritt auf einem anderen Gerät erfolgreich abgeschlossen haben.

Keine Sorge, CDA hat Sie abgedeckt. CDA erstellt die geräteübergreifende Ansicht, die [!DNL Fallout visualizations] viel nützlicher macht. Schließlich ist es wirklich wichtig, ob der Mensch letztlich irgendwo in seiner Aufgabe Erfolg hatte.

*[!DNL Fallout]mit CDA*
![[!DNL Fallout Visualization]](assets/cda-fallout-viz.png)

### [!DNL Cross-Device Attribution IQ]

Da CDA eine Schicht geräteübergreifender Daten unter Analysis Workspace erstellt, wird Ihre gesamte Analyse geräteübergreifend aromatisiert. Ein mächtiges Beispiel ist [[!DNL Attribution IQ]](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/attribution/models.html). [!DNL Attribution IQ] in Analysis Workspace können Sie mehrere Zuordnungsmodelle nebeneinander vergleichen. Mithilfe dieser Funktion können Sie jetzt vergleichen, wie verschiedene Geräte zum Erfolg beitragen.

Angenommen, Sie möchten verstehen, wie oft ein Mobiltelefon das erste Gerät ist, das in einer Interaktion verwendet wird, die letztlich zum Erfolg führt. Dies entspricht der &quot;Akquise-Rate&quot; des Mobiltelefons. Mit CDA + [!DNL Attribution IQ] können Sie diese Analyse durchführen:

*[!DNL Attribution IQ]mit CDA*
![[!DNL Attribution IQ]](assets/cda-attribution-iq.png)

Weitere Informationen finden Sie in der [[!DNL Cross-Device Analytics] Hilfedokumentation](https://docs.adobe.com/content/help/de-DE/analytics/components/cda/cda-home.html).
