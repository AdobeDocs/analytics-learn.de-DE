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
TQID: https://experienceleague.adobe.com/msvft7mQiNGjLqGEezPIbwruvSbsunPGUIFF1q7vlT0
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2:
  - id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 677e5a22dab92be7ff021c8410525b9091975aef
workflow-type: tm+mt
source-wordcount: 184
ht-degree: 73%

---

# Tracking von Aktionen (auch „benutzerspezifische Links“ genannt) in einer mobilen App mit dem Experience Platform-SDK {#tracking-actions-aka-custom-links-in-a-mobile-app-with-the-experience-platform-sdk}

Aktionen sind Ereignisse, die in Ihrer Mobile App auftreten. In diesem Video erfahren Sie, wie Sie mit der trackAction-API eine Aktion verfolgen und messen.

>[!VIDEO](https://video.tv.adobe.com/v/328306/?captions=ger&quality=12&learn=on)

Dies ist die API, die Sie zur Verfolgung aller Aktionen ohne Bildschirmauslastung auf Ihrer Site verwenden sollten. Wenn der Bildschirm angezeigt wird, verwenden Sie trackState, was einen Seitenansicht-Treffer auslöst. Verwenden Sie andernfalls trackAction, um Variablen zu senden, die mit der ausgeführten Aktion verknüpft sind.

Diese Daten werden als `contextData` bereitgestellt, was bedeutet, dass Sie dann [!UICONTROL Verarbeitungsregeln] verwenden müssen, um die Mobile-Daten aus diesen `contextData`-Variablen [!DNL eVars], [!DNL Props], Ereignissen usw. in Adobe Analytics zuzuordnen.

Weitere Informationen zu trackAction finden Sie in der [Dokumentation](https://developer.adobe.com/client-sdks/documentation/getting-started/track-events/#track-user-actions-for-adobe-analytics).
