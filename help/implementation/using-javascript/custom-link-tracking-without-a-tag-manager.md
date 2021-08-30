---
title: Benutzerspezifisches Linktracking ohne Tag-Manager
description: Bei vielen Aktionen auf der Seite sollte Tracking nicht wie ein Seitenaufruf behandelt werden. In diesem Video erfahren Sie, wie Sie ein Linktracking-Beacon für Analytics codieren, wenn Sie keinen Tag-Manager (wie Experience Platform Launch) verwenden. Sehen Sie sich den Code an und lernen Sie einen wichtigen Tipp kennen.
feature: Appmeasurement Implementation
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1845
role: Developer, Data Engineer
level: Intermediate
exl-id: e4567b1c-414e-44ad-982f-52b0150e7eda
source-git-commit: fe861dfd541c1b9cb3b233fa3f56d55054305fd9
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 5%

---

# Benutzerspezifisches Linktracking ohne Tag-Manager {#custom-link-tracking-without-a-tag-manager}

Bei vielen Aktionen auf der Seite sollte Tracking nicht wie ein Seitenaufruf behandelt werden. In diesem Video erfahren Sie, wie Sie ein Linktracking-Beacon für Analytics codieren, wenn Sie keinen Tag-Manager verwenden (z. B. Adobe [!DNL Experience Platform Launch]). Sehen Sie sich den Code an und lernen Sie einen wichtigen Tipp kennen.

## Senden eines s.tl()-Beacons {#sending-an-s-tl-beacon}

Es gibt zwei Funktionen, die Daten an Adobe Analytics senden:

1. s.t() - Ein &quot;track&quot;-Beacon, bei dem es sich um einen Seitenansichtstreffer handelt, der Seitenansichten für den angegebenen Seitennamen erhöht und andere Variablen festlegt
1. s.tl() - ein Beacon &quot;Link verfolgen&quot;, das häufig als &quot;benutzerspezifischer Link&quot;-Treffer/-Beacon bezeichnet wird, wodurch die Seitenansichten nicht inkrementiert werden und die Variable &quot;pageName&quot;ignoriert wird. Dies wird häufig verwendet, um kleinere Aktionen auf der Seite zu verfolgen, die keine neue Seite/keinen neuen Bildschirm laden, oder andere Aktionen, die nicht zum Laden einer neuen Seite führen.

>[!NOTE]
>
>In diesem Video zeigen wir Ihnen, wie Sie einen Treffer für benutzerspezifische Links codieren, wenn Sie KEINEN Tag-Manager wie Adobe [!DNL Experience Platform Launch] verwenden. Es wird empfohlen, [!DNL Experience Platform Launch], unsere Best-Practice-Empfehlung für die Implementierung, zu verwenden. Wenn Sie jedoch in einem `s.tl()` programmieren müssen, finden Sie hier eine Anleitung dazu.

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
