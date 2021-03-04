---
title: Tracking von Aktionen (auch „benutzerspezifische Links“ genannt) in einer mobilen App mit dem Experience Platform-SDK
description: 'Aktionen sind Ereignisse, die in Ihrer Mobile App auftreten. In diesem Video erfahren Sie, wie Sie mit der trackAction-API eine Aktion verfolgen und messen. '
feature: Mobile SDK
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2563
topic: Mobile
role: '"Entwickler, Dateningenieur"'
level: Erfahren
translation-type: tm+mt
source-git-commit: f3b3fa7d91b0cb21005b57768ca23ed6700fcc03
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 97%

---


# Tracking von Aktionen (aka benutzerspezifische Links) in einer Mobile App mit dem Experience Platform-SDK {#tracking-actions-aka-custom-links-in-a-mobile-app-with-the-experience-platform-sdk}

Aktionen sind Ereignisse, die in Ihrer Mobile App auftreten. In diesem Video erfahren Sie, wie Sie mit der trackAction-API eine Aktion verfolgen und messen.

>[!VIDEO](https://video.tv.adobe.com/v/26268/?quality=12)

Dies ist die API, die Sie zur Verfolgung aller Aktionen ohne Bildschirmauslastung auf Ihrer Site verwenden sollten. Wenn der Bildschirm angezeigt wird, verwenden Sie trackState, was einen Seitenansicht-Treffer auslöst. Verwenden Sie andernfalls trackAction, um Variablen zu senden, die mit der ausgeführten Aktion verknüpft sind.

Diese Daten werden als `contextData` geliefert. Dies bedeutet auch, dass Sie [!UICONTROL Verarbeitungsregeln] verwenden müssen, um die mobilen Daten aus diesen `contextData`-Variablen abzurufen und sie [!DNL eVars], [!DNL Props], Ereignissen usw. zuzuordnen. in Adobe Analytics.

Weitere Informationen zu trackAction finden Sie in der [Dokumentation](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/configuration-reference/mobile-core-api-reference).
