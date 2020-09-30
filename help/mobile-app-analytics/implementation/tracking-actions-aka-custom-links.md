---
title: Verfolgungsaktionen (AKA Custom Links) in einer mobilen App mit dem Experience Platform SDK
description: 'Aktionen sind Ereignis, die in Ihrer mobilen App auftreten. In diesem Video erfahren Sie, wie Sie mit der trackAction-API eine Aktion verfolgen und messen. '
feature: mobile sdk
topics: null
audience: implementer
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2563
translation-type: tm+mt
source-git-commit: a42658cfd4bae7b077ddd48b4cf5c7db54e35c98
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 1%

---


# Verfolgungsaktionen (AKA Custom Links) in einer mobilen App mit dem Experience Platform SDK {#tracking-actions-aka-custom-links-in-a-mobile-app-with-the-experience-platform-sdk}

Aktionen sind Ereignis, die in Ihrer mobilen App auftreten. In diesem Video erfahren Sie, wie Sie mit der trackAction-API eine Aktion verfolgen und messen.

>[!VIDEO](https://video.tv.adobe.com/v/26268/?quality=12)

Dies ist die API, die Sie zur Verfolgung aller Aktionen ohne Bildschirmauslastung auf Ihrer Site verwenden sollten. Wenn der Bildschirm angezeigt wird, verwenden Sie trackState, was einen Seitentreffer auslöst. Verwenden Sie andernfalls trackAction, um Variablen einzureichen, die mit der ausgeführten Aktion verknüpft sind.

Diese Daten werden als `contextData`inklusive, was bedeutet, dass Sie dann [!UICONTROL Verarbeitungsregeln] verwenden müssen, um die mobilen Daten aus diesen `contextData` Variablen abzurufen und sie [!DNL eVars], [!DNL Props], Ereignissen usw. zuzuordnen. in Adobe Analytics.

Weitere Informationen zu trackAction finden Sie in der [Dokumentation](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/configuration-reference/mobile-core-api-reference).
