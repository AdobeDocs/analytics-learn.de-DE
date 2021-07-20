---
title: Anleitung zum Identifizieren Ihres Analytics Tracking Servers und Ihrer Report Suites
description: Beim Einrichten von Adobe Analytics oder beim Referenzieren in anderen Experience Cloud-Lösungen ist es oft hilfreich oder sogar notwendig, den von Ihnen verwendeten Analytics Tracking Server oder auch die Report Suite zu kennen, an die Sie Daten senden. Dieses Video zeigt Ihnen, wie Sie beide Werte finden, unabhängig davon, ob Sie Adobe Analytics bereits implementiert haben oder nicht.
feature: Implementierungsgrundlagen
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2358
role: Developer, Data Engineer
level: Beginner
exl-id: 3925026f-69f1-4425-b3a9-6fef26375fed
source-git-commit: 32424f3f2b05952fe4df9ea91dcbe51684cee905
workflow-type: ht
source-wordcount: '305'
ht-degree: 100%

---

# Anleitung zum Identifizieren Ihres Analytics [!DNL Tracking Server] und Ihrer [!UICONTROL Report Suites] {#how-to-identify-your-analytics-tracking-server-and-report-suites}

Beim Einrichten von Adobe Analytics oder beim Referenzieren in anderen Experience Cloud-Lösungen ist es oft hilfreich oder sogar notwendig, den von Ihnen verwendeten [!DNL Analytics]-[!DNL Tracking Server] oder auch die [!UICONTROL Report Suite] zu kennen, an die Sie Daten senden. Dieses Video zeigt Ihnen, wie Sie beide Werte finden, unabhängig davon, ob Sie Adobe Analytics bereits implementiert haben oder nicht.

## Nach der Implementierung {#after-implementation}

Nach der Implementierung von [!DNL Analytics] auf einer Site finden Sie [!DNL tracking server] und [!DNL report suite ID] gleich im Trackingbeacon. Der [!DNL tracking server] ist der Hostname im Beacon. Dies ist also leicht zu finden. Die [!UICONTROL Report Suite]-IDs sind eine kommagetrennte Liste direkt nach „/b/ss/“ im Pfadnamen des Beacons.

Um den Beacon sowie alle weiteren Informationen, die zu [!DNL Analytics] und anderen Experience Cloud-Lösungen gelangen, anzuzeigen, installieren Sie die [Chrome-Erweiterung „Experience Cloud Debugger“](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj?hl=de).

## Vor der Implementierung {#before-implementation}

**[!DNL Tracking Server]** – Wenn Sie noch nicht mit der Adobe Analytics-Implementierung begonnen haben, wählen Sie eine Sub-Domäne für „.sc.omtrdc.net“ [!DNL tracking server]. Nehmen wir zum Beispiel an, ich habe einen Onlineshop für Hüte namens „Jim’s Brims“. Ich kann meinen [!DNL tracking server] einfach auf Folgendes setzen:

„jimsbrims.sc.omtrdc.net“.

**[!UICONTROL Report Suite]** – Um eine Liste Ihrer [!UICONTROL Report Suites], die erstellt worden sind, zu finden, melden Sie sich bei [!DNL Analytics] an und gehen Sie zu [!UICONTROL Administrator] > [!UICONTROL Report Suites] im oberen Menü, um eine Liste der [!UICONTROL Report Suites] einschließlich ID und Titel anzuzeigen.

Weiterführende Informationen finden Sie im folgenden Video.

>[!VIDEO](https://video.tv.adobe.com/v/26061/?quality=12)
