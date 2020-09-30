---
title: Benutzerspezifische Linkverfolgung ohne Tag-Manager
description: Bei vielen Seitenaktionen sollte die Verfolgung nicht wie eine Ansicht behandelt werden. In diesem Video erfahren Sie, wie Sie einen Link-Tracking-Beacon mit Analytics kodieren, wenn Sie keinen Tag-Manager (z. B. Experience Platform Launch) verwenden. Sehen Sie sich den Code an und lernen Sie eine wichtige Tipps.
feature: appmeasurement implementation
topics: null
audience: implementer
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1845
translation-type: tm+mt
source-git-commit: 8276828e9e759a1964ca5ea89bb1395e5e78b500
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 4%

---


# Benutzerspezifische Linkverfolgung ohne Tag-Manager {#custom-link-tracking-without-a-tag-manager}

Bei vielen Seitenaktionen sollte die Verfolgung nicht wie eine Ansicht behandelt werden. In diesem Video erfahren Sie, wie Sie einen Link-Tracking-Beacon mit Analytics kodieren, wenn Sie keinen Tag-Manager verwenden (z. B. Adobe [!DNL Experience Platform Launch]). Sehen Sie sich den Code an und lernen Sie eine wichtige Tipps.

## Senden eines s.tl()-Beacon {#sending-an-s-tl-beacon}

Es gibt zwei Funktionen, mit denen Daten an Adobe Analytics gesendet werden:

1. s.t() - Ein &quot;track&quot;-Beacon, bei dem es sich um einen Seitentreffer handelt, bei dem die Ansichten für den jeweiligen Seitennamen erhöht werden und andere Ansichten festgelegt werden
1. s.tl() - ein Beacon für einen &quot;Track-Link&quot;, der häufig als &quot;benutzerspezifischer Link&quot;-Treffer/Beacon bezeichnet wird, wodurch keine Ansichten der Seite erhöht werden, und die Variable &quot;pageName&quot;ignoriert wird. Dies wird häufig verwendet, um kleinere Aktionen auf der Seite zu verfolgen, die keine neue Seite/keinen neuen Bildschirm laden, oder andere Aktionen, die nicht zum Laden einer neuen Seite führen.

>[!NOTE]
>
>In diesem Video zeigen wir Ihnen, wie Sie einen Treffer für benutzerspezifische Links codieren, wenn Sie KEINEN Tag-Manager wie Adobe verwenden [!DNL Experience Platform Launch]. Wir empfehlen Ihnen, [!DNL Experience Platform Launch]unsere Best-Practice-Empfehlung für die Implementierung zu verwenden. Wenn Sie jedoch Code in einem `s.tl()`erstellen müssen, hier die Vorgehensweise.

>[!VIDEO](https://video.tv.adobe.com/v/25832/?quality=12)

## Beispielcode {#sample-code}

Im Folgenden finden Sie den Beispielcode für den benutzerspezifischen Link im Video:

```JavaScript
<a href="#" onclick="
    s.linkTrackVars='events,eVar2,prop2';
    s.linkTrackEvents=s.events='event2';
    s.eVar2='facebook share';
    s.prop2='facebook share';
    s.tl(this,'o','Social Share');
    s.manageVars('clearVars',s.linkTrackVars,1);">
    Click here to share on FaceBook
</a>
```

Weitere Informationen zu benutzerspezifischen Links finden Sie in der [Dokumentation](https://marketing.adobe.com/resources/help/de_DE/sc/implement/function_tl.html).