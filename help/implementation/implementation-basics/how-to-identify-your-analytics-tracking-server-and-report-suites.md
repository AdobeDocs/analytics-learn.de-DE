---
title: Identifizieren Ihres Analytics-Tracking-Servers und Ihrer Report Suites
description: Beim Einrichten von Adobe Analytics oder beim Referenzieren in anderen Experience Cloud-Lösungen ist es oft hilfreich oder sogar notwendig, den von Ihnen verwendeten Analytics "Tracking-Server"oder auch die "Report Suite"zu kennen, in die Sie Daten senden. Dieses Video zeigt Ihnen, wie Sie beide Werte finden, unabhängig davon, ob Sie Adobe Analytics bereits implementiert haben oder nicht.
feature: implementation basics
topics: null
audience: implementer
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2358
translation-type: tm+mt
source-git-commit: 60f4ce4f563a990576b3331b01cd87c29d424f43
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 2%

---


# Identifizieren Ihrer Analytics- [!DNL Tracking Server] und [!UICONTROL Report Suites] {#how-to-identify-your-analytics-tracking-server-and-report-suites}

Beim Einrichten von Adobe Analytics oder beim Referenzieren in anderen Experience Cloud-Lösungen ist es oft hilfreich oder sogar notwendig, die [!DNL Analytics] &quot;[!DNL Tracking Server]&quot;, die Sie verwenden, oder auch die &quot;[!UICONTROL Report Suite]&quot;, an die Sie Daten senden, zu kennen. Dieses Video zeigt Ihnen, wie Sie beide Werte finden, unabhängig davon, ob Sie Adobe Analytics bereits implementiert haben oder nicht.

## Nach Implementierung {#after-implementation}

Nach der Implementierung [!DNL Analytics] auf einer Site können Sie die [!DNL tracking server] und die [!DNL report suite ID] rechte Seite im Tracking-Beacon finden. Der Hostname [!DNL tracking server] ist im Beacon, das ist einfach zu finden. Die [!UICONTROL Report Suite] -IDs sind eine kommagetrennte Liste direkt nach &quot;/b/ss/&quot;im Pfadnamen des Beacons.

Um den Beacon sowie alle anderen Informationen, die zu [!DNL Analytics] und anderen Experience Cloud-Lösungen kommen, zu sehen, installieren Sie die Chrome- [Erweiterung](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj?hl=de).

## Vor Implementierung {#before-implementation}

**[!DNL Tracking Server]** - Wenn Sie noch nicht mit der Adobe Analytics-Implementierung begonnen haben, wählen Sie eine Subdomäne für &quot;.sc.omtrdc.net&quot; [!DNL tracking server]. Nehmen wir zum Beispiel an, ich habe einen Online-Hutstore namens &quot;Jim’s Brims&quot;. Ich kann mich einfach [!DNL tracking server] auf Folgendes einstellen:

&quot;jimsbrims.sc.omtrdc.net&quot;.

**[!UICONTROL Report Suite]** - Wenn Sie eine Liste Ihrer [!UICONTROL Report Suites] finden möchten, melden Sie sich an [!DNL Analytics] und navigieren Sie im oberen Menü zu [!UICONTROL Admin] > [!UICONTROL Report Suites] , um eine Liste der [!UICONTROL Report Suites]einschließlich ID und Titel anzuzeigen.

Weitere Informationen finden Sie im Video unten.

>[!VIDEO](https://video.tv.adobe.com/v/26061/?quality=12)
