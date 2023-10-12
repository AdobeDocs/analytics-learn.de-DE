---
title: Identifizieren des Analytics-Tracking-Servers und der Report Suite-ID
description: Bei der Einrichtung von Adobe Analytics oder beim Referenzieren in anderen Experience Cloud-Lösungen ist es häufig hilfreich oder sogar erforderlich, den von Ihnen verwendeten Analytics-"Tracking-Server"oder auch die "Report Suite"zu kennen, an die Sie Daten senden. Dieses Video zeigt Ihnen, wie Sie beide Werte finden, unabhängig davon, ob Sie Adobe Analytics bereits implementiert haben oder nicht.
feature: Implementation Basics
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2358
role: Developer, Data Engineer
level: Beginner
exl-id: 3925026f-69f1-4425-b3a9-6fef26375fed
source-git-commit: 42bf16df9585d1f41206b81bf509a72c10f1d7f2
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 17%

---

# Identifizierung Ihrer Analyse [!DNL tracking server] und [!UICONTROL Report Suite-ID] {#how-to-identify-your-analytics-tracking-server-and-report-suites}

Beim Einrichten von Adobe Analytics oder beim Referenzieren in anderen Experience Cloud-Lösungen ist es häufig hilfreich oder sogar erforderlich, den von Ihnen verwendeten Analytics-&quot;Tracking-Server&quot;oder auch die[!UICONTROL Report Suite]&quot;, an die Sie Daten senden. Dieses Video zeigt Ihnen, wie Sie beide Werte finden, unabhängig davon, ob Sie Adobe Analytics bereits implementiert haben oder nicht.

>[!IMPORTANT]
>
>Dieser Artikel und dieses Video gelten für eine &quot;AppMeasurement&quot;-Implementierung von Adobe Analytics und nicht für eine Implementierung mit dem Web SDK.

## Nach der Implementierung {#after-implementation}

Nach der Implementierung von Analytics auf einer Site finden Sie die [!DNL tracking server] und [!DNL report suite ID] direkt im Tracking-Beacon. Die [!DNL tracking server] ist der Hostname im Beacon, also ist das leicht zu finden. Die [!UICONTROL Report Suite] IDs sind eine kommagetrennte Liste direkt nach &quot;/b/ss/&quot;im Pfadnamen des Beacons.

Um das Beacon sowie alle anderen Informationen zu Analytics- und anderen Experience Cloud-Lösungen anzuzeigen, installieren Sie die [Chrome-Erweiterung &quot;Experience Cloud Debugger&quot;](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj?hl=de).

## Vor der Implementierung {#before-implementation}

**[!DNL Tracking server]** - Wenn Sie noch nicht mit Ihrer Adobe Analytics-Implementierung begonnen haben, wählen Sie eine Subdomain für &quot;.sc.omtrdc.net&quot; [!DNL tracking server]. Nehmen wir zum Beispiel an, ich habe einen Online-Hutstore namens &quot;Jim&#39;s Brims&quot;. Ich kann meinen [!DNL tracking server] einfach auf Folgendes setzen:

&quot;jimsbrims.sc.omtrdc.net&quot;.

**[!UICONTROL Report Suite]** - Um eine Liste Ihrer [!UICONTROL Report Suites] die erstellt wurden, melden Sie sich bei [!DNL Analytics] und gehen Sie zu [!UICONTROL Admin] > [!UICONTROL Report Suites] im oberen Menü, um eine Liste von [!UICONTROL Report Suites], einschließlich ID und Titel.

Weiterführende Informationen finden Sie im folgenden Video.

>[!VIDEO](https://video.tv.adobe.com/v/26061/?quality=12&learn=on)
