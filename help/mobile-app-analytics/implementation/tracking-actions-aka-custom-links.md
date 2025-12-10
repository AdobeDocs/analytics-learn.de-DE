---
title: Tracking von Aktionen (auch „benutzerspezifische Links“ genannt) in einer mobilen App mit dem Experience Platform-SDK
description: Aktionen sind Ereignisse, die in Ihrer Mobile App auftreten. In diesem Video erfahren Sie, wie Sie mit der trackAction-API eine Aktion verfolgen und messen.
feature: Mobile SDK
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2563
topic: Mobile
role: Developer
level: Experienced
exl-id: 541c51b8-638e-43b4-90ac-0ce94290a141
source-git-commit: 474e68e2937c82efa459b6ed8048a4abd2753285
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 99%

---

# Tracking von Aktionen (auch „benutzerspezifische Links“ genannt) in einer mobilen App mit dem Experience Platform-SDK {#tracking-actions-aka-custom-links-in-a-mobile-app-with-the-experience-platform-sdk}

Aktionen sind Ereignisse, die in Ihrer Mobile App auftreten. In diesem Video erfahren Sie, wie Sie mit der trackAction-API eine Aktion verfolgen und messen.

>[!VIDEO](https://video.tv.adobe.com/v/328306/?captions=ger&quality=12&learn=on)

Dies ist die API, die Sie zur Verfolgung aller Aktionen ohne Bildschirmauslastung auf Ihrer Site verwenden sollten. Wenn der Bildschirm angezeigt wird, verwenden Sie trackState, was einen Seitenansicht-Treffer auslöst. Verwenden Sie andernfalls trackAction, um Variablen zu senden, die mit der ausgeführten Aktion verknüpft sind.

Diese Daten werden als `contextData` geliefert. Dies bedeutet auch, dass Sie [!UICONTROL Verarbeitungsregeln] verwenden müssen, um die mobilen Daten aus diesen `contextData`-Variablen abzurufen und sie [!DNL eVars], [!DNL Props], Ereignissen usw. zuzuordnen. in Adobe Analytics.

Weitere Informationen zu trackAction finden Sie in der [Dokumentation](https://developer.adobe.com/client-sdks/documentation/getting-started/track-events/#track-user-actions-for-adobe-analytics).
