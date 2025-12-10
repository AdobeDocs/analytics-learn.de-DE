---
title: So identifizieren Sie Ihre Analytics-Tracking-Server und Ihre Report Suite-ID
description: Beim Einrichten von Adobe Analytics oder beim Referenzieren in anderen Experience Cloud-Lösungen ist es oft hilfreich oder sogar notwendig, den von Ihnen verwendeten Analytics-„Tracking-Server“ oder auch die „Report Suite“ zu kennen, an die Sie Daten senden. Dieses Video zeigt Ihnen, wie Sie beide Werte finden, unabhängig davon, ob Sie Adobe Analytics bereits implementiert haben oder nicht.
feature: Implementation Basics
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2358
role: Developer
level: Beginner
exl-id: 3925026f-69f1-4425-b3a9-6fef26375fed
source-git-commit: 474e68e2937c82efa459b6ed8048a4abd2753285
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 100%

---

# So identifizieren Sie Ihren Analytics-[!DNL tracking server] und Ihre [!UICONTROL Report Suite-ID] {#how-to-identify-your-analytics-tracking-server-and-report-suites}

Beim Einrichten von Adobe Analytics oder beim Referenzieren in anderen Experience Cloud-Lösungen ist es oft hilfreich oder sogar notwendig, den von Ihnen verwendeten Analytics-„Tracking-Server“ oder auch die „[!UICONTROL Report Suite]“ zu kennen, an die Sie Daten senden. Dieses Video zeigt Ihnen, wie Sie beide Werte finden, unabhängig davon, ob Sie Adobe Analytics bereits implementiert haben oder nicht.

>[!IMPORTANT]
>
>Dieser Artikel und dieses Video gelten für eine „AppMeasurement“-Implementierung von Adobe Analytics und nicht für eine Implementierung mit dem Web SDK.

## Nach der Implementierung {#after-implementation}

Nach der Implementierung von Analytics auf einer Site finden Sie [!DNL tracking server] und [!DNL report suite ID] gleich im Tracking-Beacon. Der [!DNL tracking server] ist der Host-Name im Beacon. Dies ist also leicht zu finden. Die IDs der [!UICONTROL Report Suite] bilden eine kommagetrennte Liste direkt nach „/b/ss/“ im Pfadnamen des Beacons.

Um den Beacon sowie alle weiteren Informationen anzuzeigen, die zu Analytics und anderen Experience Cloud-Lösungen gelangen, installieren Sie die [Chrome-Erweiterung „Experience Cloud Debugger“](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj?hl=de).

## Vor der Implementierung {#before-implementation}

**[!DNL Tracking server]** – Wenn Sie noch nicht mit der Adobe Analytics-Implementierung begonnen haben, wählen Sie eine Subdomain für „.sc.omtrdc.net“ [!DNL tracking server] aus. Nehmen wir zum Beispiel an, ich habe einen Onlineshop für Hüte namens „Jim’s Brims“. Ich kann meinen [!DNL tracking server] einfach auf Folgendes setzen:

„jimsbrims.sc.omtrdc.net“.

**[!UICONTROL Report Suite]** – Um eine Liste Ihrer [!UICONTROL Report Suites] zu finden, die erstellt worden sind, melden Sie sich bei [!DNL Analytics] an und gehen Sie im oberen Menü zu [!UICONTROL Administration] > [!UICONTROL Report Suites], um eine Liste der [!UICONTROL Report Suites] einschließlich ID und Titel anzuzeigen.

Weiterführende Informationen finden Sie im folgenden Video.

>[!VIDEO](https://video.tv.adobe.com/v/26061/?quality=12&learn=on)
