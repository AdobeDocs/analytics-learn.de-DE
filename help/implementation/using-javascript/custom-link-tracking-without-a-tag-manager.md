---
title: Benutzerspezifisches Linktracking ohne Tag-Manager
description: Bei vielen Aktionen auf der Seite sollte Tracking nicht wie eine Seitenansicht behandelt werden. In diesem Video erfahren Sie, wie Sie ein Linktracking-Beacon für Analytics codieren, wenn Sie keinen Tag-Manager (wie Experience Platform Launch) verwenden. Sehen Sie sich den Code an und lernen Sie einen wichtigen Tipp kennen.
feature: Appmeasurement Implementation
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1845
role: Developer
level: Intermediate
exl-id: e4567b1c-414e-44ad-982f-52b0150e7eda
source-git-commit: 474e68e2937c82efa459b6ed8048a4abd2753285
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 100%

---

# Benutzerspezifisches Linktracking ohne Tag-Manager {#custom-link-tracking-without-a-tag-manager}

Bei vielen Aktionen auf der Seite sollte Tracking nicht wie eine Seitenansicht behandelt werden. In diesem Video erfahren Sie, wie Sie ein Linktracking-Beacon für Analytics codieren, wenn Sie keinen Tag-Manager (wie Adobe [!DNL Experience Platform Launch]) verwenden. Sehen Sie sich den Code an und lernen Sie einen wichtigen Tipp kennen.

## Senden eines „s.tl()“-Beacons {#sending-an-s-tl-beacon}

Es gibt zwei Funktionen, die Daten an Adobe Analytics senden:

1. s.t(): Ein Beacon zur Nachverfolgung, bei dem es sich um einen Seitenansichtstreffer handelt, der Seitenansichten für den angegebenen Seitennamen erhöht und andere Variablen festlegt.
1. s.tl(): Ein Beacon zum Linktracking, häufig auch als Treffer/Beacon für benutzerspezifische Links bezeichnet, das Seitenansichten nicht inkrementiert und die Variable „pageName“ ignoriert. Dies wird häufig verwendet, um kleinere Aktionen auf der Seite, die keine neue Seite/keinen neuen Bildschirm laden, oder andere Aktionen, die nicht zum Laden einer neuen Seite führen, zu verfolgen.

>[!NOTE]
>
>In diesem Video zeigen wir Ihnen, wie Sie einen benutzerspezifischen Link-Treffer codieren, wenn Sie KEINEN Tag-Manager wie Adobe [!DNL Experience Platform Launch] verwenden. Wir empfehlen die Verwendung von [!DNL Experience Platform Launch], unserer Best-Practice-Empfehlung für die Implementierung. Wenn Sie jedoch Code mit `s.tl()` verwenden müssen, sehen Sie hier, wie das geht.

>[!VIDEO](https://video.tv.adobe.com/v/25832/?quality=12&learn=on)

## Beispiel-Code {#sample-code}

Im Folgenden finden Sie den Beispiel-Code für den benutzerspezifischen Link im Video:

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
