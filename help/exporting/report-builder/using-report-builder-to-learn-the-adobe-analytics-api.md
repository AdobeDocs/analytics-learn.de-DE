---
title: Verwenden von Report Builder, um mehr über die Adobe Analytics-API zu erfahren
description: Report Builder ist etwas, das wir alle kennen und lieben. Was also, wenn ich Ihnen sage, dass Sie das, was Sie über Report Builder wissen, nutzen können, um Ihr Adobe Analytics-Skillset noch weiter zu erweitern? In diesem Video erfahren Sie, wie Sie Debugging-Report Builder-Anfragen ausführen und diese verwenden können, um zu erfahren, wie Sie Ihre eigenen Analytics-API-Abfragen erstellen.
feature: Report Builder
topics: null
activity: use
doc-type: feature video
team: Technical Marketing
kt: 2345
role: User
level: Intermediate
exl-id: 8b8e0dac-2498-4fba-ba4b-585b309ae1fd
source-git-commit: 32424f3f2b05952fe4df9ea91dcbe51684cee905
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 7%

---

# Verwenden von [!UICONTROL Report Builder] zum Kennenlernen der Adobe Analytics-API {#using-report-builder-to-learn-the-adobe-analytics-api}

[!UICONTROL Report ] Builder ist etwas, das wir alle kennen und lieben. Was also, wenn ich Ihnen sage, dass Sie das, was Sie über [!UICONTROL Report Builder] wissen, verwenden können, um Ihr Adobe Analytics-Skillset noch weiter zu erweitern? In diesem Video erfahren Sie, wie Sie Debugging-Anfragen für [!UICONTROL Report Builder] ausführen und diese verwenden, um zu erfahren, wie Sie Ihre eigenen [!DNL Analytics]-API-Abfragen erstellen.

>[!VIDEO](https://video.tv.adobe.com/v/25442/?quality=12)

**UPDATE**:  [!UICONTROL Report ] Builder hat die Art und Weise aktualisiert, wie die Daten geringfügig angefordert werden. Sie können den Ansatz dieses Videos weiterhin verwenden, aber die Informationen unterscheiden sich in einem Debugger geringfügig.

In einem Debugger:

1 - Suchen Sie nach api5.omniture.com. Die Anzahl variiert je nach Rechenzentrum zwischen 1 und 5.

2 - Navigieren Sie zur Registerkarte [!UICONTROL Anfrage] .

3 - Suchen Sie in der Anfrage nach &quot;[!DNL Report.Queue]&quot;.

Es gibt auch eine alternative Methode zum Debugging von Anforderungen wie dieser, und es funktioniert auch. Sie können die Protokollierung von [!UICONTROL Report Builder] über das Menü [!UICONTROL Optionen] aktivieren. Dadurch werden dieselben Informationen aufgezeichnet wie bei einem Debugger. Protokolle finden Sie unter [!UICONTROL Dokumente] > [!UICONTROL ReportBuilderLogs] und werden nach Tag organisiert. Sie können die Datei nach &quot;Report.Queue&quot;durchsuchen, um jede Ihrer Anforderungen zu finden. Protokolle helfen auch bei der Fehlerbehebung von Problemen.

Weitere Informationen zu dieser Funktion finden Sie in der [Dokumentation](https://www.adobe.io/).
