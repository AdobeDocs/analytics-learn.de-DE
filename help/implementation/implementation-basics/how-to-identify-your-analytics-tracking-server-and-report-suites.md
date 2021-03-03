---
title: Identifizieren Ihres Analytics-Tracking-Servers und Ihrer Report Suites
description: Beim Einrichten von Adobe Analytics oder beim Referenzieren in anderen Experience Cloud-Lösungen ist es oft hilfreich oder sogar notwendig, den von Ihnen verwendeten Analytics "Tracking-Server"oder auch die "Report Suite"zu kennen, in die Sie Daten senden. Dieses Video zeigt Ihnen, wie Sie beide Werte finden, unabhängig davon, ob Sie Adobe Analytics bereits implementiert haben oder nicht.
feature: Implementierungsgrundlagen
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2358
role: '"Entwickler, Dateningenieur"'
level: Anfänger
translation-type: tm+mt
source-git-commit: f3b3fa7d91b0cb21005b57768ca23ed6700fcc03
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 2%

---


# Identifizieren Ihrer Analytics [!DNL Tracking Server]- und [!UICONTROL Report Suites] {#how-to-identify-your-analytics-tracking-server-and-report-suites}

Beim Einrichten von Adobe Analytics oder beim Referenzieren in anderen Experience Cloud-Lösungen ist es oft hilfreich oder sogar notwendig, die [!DNL Analytics] &quot;[!DNL Tracking Server]&quot;zu kennen, die Sie verwenden, oder auch die &quot;[!UICONTROL Report Suite]&quot;, an die Sie Daten senden. Dieses Video zeigt Ihnen, wie Sie beide Werte finden, unabhängig davon, ob Sie Adobe Analytics bereits implementiert haben oder nicht.

## Nach Implementierung {#after-implementation}

Nach der Implementierung von [!DNL Analytics] auf einer Site finden Sie die [!DNL tracking server]- und [!DNL report suite ID]-Variablen rechts im Tracking-Beacon. Das [!DNL tracking server] ist der Hostname im Beacon, sodass das leicht zu finden ist. Die [!UICONTROL Report Suite]-IDs sind eine kommagetrennte Liste direkt nach &quot;/b/ss/&quot;im Pfadnamen des Beacons.

Um den Beacon sowie alle weiteren Informationen, die zu [!DNL Analytics] und anderen Experience Cloud-Lösungen gelangen, anzuzeigen, installieren Sie die [&quot;Experience Cloud Debugger&quot; Chrome Extension](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj?hl=de).

## Vor Implementierung {#before-implementation}

**[!DNL Tracking Server]** - Wenn Sie noch nicht mit der Adobe Analytics-Implementierung begonnen haben, wählen Sie eine Subdomäne für &quot;.sc.omtrdc.net&quot; [!DNL tracking server]. Nehmen wir zum Beispiel an, ich habe einen Online-Hutstore namens &quot;Jim’s Brims&quot;. Ich kann meine [!DNL tracking server] einfach auf Folgendes setzen:

&quot;jimsbrims.sc.omtrdc.net&quot;.

**[!UICONTROL Report Suite]**  - Um eine Liste Ihrer  [!UICONTROL Report ] Suites zu finden, melden Sie sich an  [!DNL Analytics] und gehen Sie zu  [!UICONTROL Admin] >  [!UICONTROL Report ] Suites im oberen Menü, um eine Liste der  [!UICONTROL Report Suites] einschließlich ID und Titel anzuzeigen.

Weitere Informationen finden Sie im Video unten.

>[!VIDEO](https://video.tv.adobe.com/v/26061/?quality=12)
