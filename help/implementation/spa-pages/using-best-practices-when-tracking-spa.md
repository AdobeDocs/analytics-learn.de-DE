---
title: 'Verwenden von Best Practices beim Verfolgen von Einzelseiten-Apps (SPA) in Adobe Analytics '
description: In diesem Dokument werden wir verschiedene Best Practices beschreiben, die Sie befolgen sollten und die Sie kennen sollten, wenn Sie Adobe Analytics zur Verfolgung von Einzelseiten-Apps (SPA) verwenden. Dieses Dokument konzentriert sich auf die Verwendung von Experience Platform Launch, der empfohlenen Implementierungsmethode.
feature: Implementierungsgrundlagen
topics: spa
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1389
topic: SPA
role: Developer, Data Engineer
level: Intermediate
exl-id: 8fe63dd1-9629-437f-ae07-fe1c5a05fa42
source-git-commit: 32424f3f2b05952fe4df9ea91dcbe51684cee905
workflow-type: tm+mt
source-wordcount: '1672'
ht-degree: 0%

---

# Verwenden von Best Practices beim Verfolgen von Einzelseiten-Apps (SPA) in Adobe Analytics {#using-best-practices-when-tracking-spa-in-adobe-analytics}

In diesem Dokument werden wir verschiedene Best Practices beschreiben, die Sie befolgen sollten und die Sie kennen sollten, wenn Sie Adobe Analytics zur Verfolgung von Einzelseiten-Apps (SPA) verwenden. Dieses Dokument konzentriert sich auf die Verwendung der Adobe [!DNL Experience Platform Launch], der empfohlenen Implementierungsmethode.

ERSTE HINWEISE:

* Bei den folgenden Elementen wird davon ausgegangen, dass Sie [!DNL Experience Platform Launch] zur Implementierung auf Ihrer Site verwenden. Wenn Sie [!DNL Experience Platform Launch] nicht verwenden, gibt es weiterhin Überlegungen. Sie müssen diese jedoch an Ihre Implementierungsmethode anpassen.
* Alle SPA unterscheiden sich, sodass Sie möglicherweise einige der folgenden Elemente anpassen müssen, um Ihren Anforderungen am besten zu entsprechen. Wir wollten jedoch einige Best Practices mit Ihnen teilen. Dinge, über die Sie bei der Implementierung von Adobe Analytics auf SPA Seiten nachdenken müssen.

## Einfaches Diagramm zum Arbeiten mit SPA in [!DNL Experience Platform Launch] {#simple-diagram-of-working-with-spas-in-launch}

![SPA für Analysen in Launch](assets/spa_for_analyticsinlaunch.png)

**HINWEIS:**  Wie angegeben, ist dies ein vereinfachtes Diagramm zur Handhabung SPA Seiten in einer Adobe Analytics-Implementierung mit  [!DNL Experience Platform Launch]. In den folgenden Abschnitten dieser Seite werden wir die Schritte und Probleme besprechen, die Sie sorgfältig prüfen oder bearbeiten sollten.

## Festlegen der Datenschicht {#setting-the-data-layer}

Wenn neuer Inhalt auf einer SPA geladen wird oder wenn eine Aktion auf einer SPA Seite stattfindet, sollten Sie als Erstes die Datenschicht aktualisieren. Dies muss geschehen, BEVOR die benutzerspezifischen Ereignisregeln in [!DNL Experience Platform Launch] ausgelöst und Trigger ausgelöst werden, damit [!DNL Experience Platform Launch] die neuen Werte aus der Datenschicht abrufen und in Adobe Analytics übertragen kann.

Im Folgenden finden Sie eine Beispieldatenschicht, deren Elemente bei Änderung der Ansicht oder Aktion auf Ihrer SPA geändert werden können. Bei einer Änderung des Vollbild-/Mehrheitsbildschirms ist es beispielsweise üblich, ein &quot;[!DNL pageName]&quot;-Element zu ändern, sodass das neue Element in [!DNL Experience Platform Launch] erfasst und an Adobe Analytics gesendet werden kann.

```JavaScript
<script>
    digitalData = {
        pageInstanceID: "Launch Demo Site",
        page:{
            pageInfo:{
                pageID: '2745374',
                pageName: 'acs demo - product listing page'
            },
            attributes:{
                project: "Experience Platform Launch Project"
            }
        },
        user : [ {
          "profile" : [ {
            "attributes" : {
              "gender" : "male",
              "age" : "35"
            }
          } ]
        }],
        libraries : {
          adobe : {
            launch : {
              state : 0, // 0 = not loaded , 1 = loaded
              domain : "assets.adobedtm.com"
            }
          }
        }

     };
    </script>
```

## Festlegen von benutzerdefinierten Ereignissen und Listening in [!DNL Experience Platform Launch] {#setting-custom-events-and-listening-in-launch}

Wenn neuer Inhalt auf der Seite geladen wird oder eine Aktion auf der Site stattfindet, sollten Sie [!DNL Experience Platform Launch] informieren, damit eine Regel ausgeführt und Daten an [!DNL Analytics] gesendet werden können. Dazu gibt es verschiedene Möglichkeiten: [!UICONTROL Direktaufruf] [!UICONTROL Regeln] oder benutzerspezifische Ereignisse.

* [!UICONTROL Direct ] [!UICONTROL CallRules]: in  [!DNL Experience Platform Launch], können Sie eine  [!UICONTROL direkte ]  Aufrufregel einrichten, die ausgeführt wird, wenn sie direkt von der Seite aus aufgerufen wird. Wenn das Laden Ihrer Seite oder Ihre Aktion auf Ihrer Site sehr einfach ist oder wenn sie eindeutig ist und jedes Mal bestimmte Anweisungen ausführen kann (setzen Sie [!DNL eVar4] jedes Mal auf X und Trigger [!DNL event2]), können Sie einen [!UICONTROL Direktaufruf] [!UICONTROL Regel] verwenden. Weitere Informationen finden Sie in der [!DNL Experience Platform Launch] Dokumentation zum Erstellen von [!UICONTROL Direktaufrufen] [!UICONTROL Regeln].
* Benutzerspezifische Ereignisse: Für mehr Funktionalität und für die Möglichkeit, eine Payload mit unterschiedlichen Werten dynamisch anzuhängen, sollten Sie benutzerdefinierte JavaScript-Ereignisse festlegen und sie in [!DNL Experience Platform Launch] überwachen, wo Sie die Payload verwenden können, um Variablen festzulegen und die Daten an Adobe Analytics zu senden. Es ist wahrscheinlicher, dass Sie diese Funktion benötigen. Daher gilt diese Option als Best Practice. Jede Funktion auf Ihrer Site kann jedoch bestimmen, welche Methode am besten geeignet ist. Wir werden in diesem Dokument fortfahren, vorausgesetzt, Sie müssen diese benutzerspezifische Ereignismethode verwenden.

**Beispiele:** Im  [](https://helpx.adobe.com/experience-manager/kt/integration/using/launch-reference-architecture-SPA-tutorial-implement.html) DIESEN Hilfedokument finden Sie Links zu Beispiel-SPA-Sites, die implementiert wurden ( [!DNL Analytics] und andere Experience Cloud-Lösungen), sowie Dokumente, die beschreiben, was implementiert wurde. In diesen SPA wurden die folgenden benutzerdefinierten Ereignisse verwendet:

* [!DNL event-view-start]: Dieses Ereignis sollte beim Ansichtsstart der Ansicht/des Status ausgelöst werden, die geladen wird.
* [!DNL event-view-end]: Dieses Ereignis sollte auch dann ausgelöst werden, wenn eine Ansicht-/Statusänderung stattgefunden hat und alle SPA Komponenten auf der Seite vollständig geladen wurden. Dies ist das Ereignis, bei dem normalerweise ein Aufruf an Adobe Analytics Trigger wird.
* [!DNL event-action-trigger]: Dieses Ereignis sollte ausgelöst werden, wenn ein beliebiges Ereignis auf der Seite auftritt, mit Ausnahme des Ladevorgangs von Ansicht/Status. Dies kann ein Klickereignis oder eine kleinere Inhaltsänderung ohne Änderung der Ansicht sein.

Weitere Informationen dazu, wie/wann sie ausgelöst werden, finden Sie auf den oben referenzierten Seiten/Dokumenten . Sie müssen nicht dieselben Ereignisnamen verwenden, aber die hier aufgeführten Funktionen sind empfohlene Best Practices. Das folgende Video zeigt eine Beispielsite und wo in [!DNL Experience Platform Launch] , um die benutzerdefinierten Ereignisse zu überwachen.

>[!VIDEO](https://video.tv.adobe.com/v/23024/?quality=12)

## Ausführen von s.t() oder s.tl() im [!DNL Experience Platform Launch] [!UICONTROL Regel] {#running-s-t-or-s-tl-in-the-launch-rule}

Eines der wichtigsten Dinge, die Sie für [!DNL Analytics] beim Arbeiten mit einem SPA verstehen sollten, ist der Unterschied zwischen `s.t()` und `s.tl()`. Sie lösen eine dieser Methoden in [!DNL Experience Platform Launch] aus, um Daten an [!DNL Analytics] zu senden. Sie müssen jedoch wissen, wann die einzelnen Nachrichten gesendet werden.

* **s.t()**  - &quot;t&quot;steht für &quot;track&quot;und ist eine normale Seitenansicht. Selbst wenn sich die URL möglicherweise nicht ändert, ändert sich die Ansicht so, dass ** sie als neue &quot;Seite&quot;betrachtet wird? Wenn ja, setzen Sie die Variable s.[!DNL pageName] und verwenden Sie `s.t()`, um den Aufruf an [!DNL Analytics] zu senden.

* **s.tl()**  - &quot;tl&quot;steht für &quot;track link&quot;und wird normalerweise zum Tracking von Klicks oder kleinen Inhaltsänderungen auf der Seite verwendet, im Gegensatz zu einer Vollbildänderung. Wenn die Änderung auf Ihrer Seite klein ist, sodass Sie sie nicht als vollständige neue &quot;Seite&quot;betrachten, verwenden Sie `s.tl()` und sorgen Sie sich nicht darum, die Variable s.pageName festzulegen, da [!DNL Analytics] sie ignoriert.

**TIPP:** Manche Benutzer verwenden eine allgemeine Richtlinie, wonach der Bildschirm, wenn er sich um mehr als 50 % ändert, als Seitenansicht und -nutzung betrachtet werden sollte  `s.t()`. Wenn die Änderung am Bildschirm weniger als 50 % beträgt, verwenden Sie `s.tl()`. Es liegt jedoch ganz bei Ihnen, was Sie als neue &quot;Seite&quot;betrachten und wie Sie Ihre Site in Adobe Analytics verfolgen möchten.

Das folgende Video zeigt, wo/wie `s.t()` oder `s.tl()` in Launch by Adobe Trigger wird.

>[!VIDEO](https://video.tv.adobe.com/v/23048/?quality=12)

## Variablen löschen {#clearing-variables}

Wenn Sie Ihre Site mit Adobe Analytics verfolgen, möchten Sie natürlich nur die richtigen Daten zum richtigen Zeitpunkt an [!DNL Analytics] senden. In einer SPA-Umgebung kann ein Wert, der in einer [!DNL Analytics] -Variablen verfolgt wird, persistent sein und möglicherweise erneut an [!DNL Analytics] gesendet werden, wenn dies nicht mehr gewünscht wird. Aus diesem Grund gibt es eine Funktion in der Erweiterung [!DNL Analytics] [!DNL Launch], mit der die Variablen gelöscht werden, sodass Sie eine neue Verzögerung haben, wenn Sie die nächste Bildanforderung ausführen und Daten an [!DNL Analytics] senden.

Im obigen Diagramm wird sie am Ende des Prozesses aufgelistet, wobei die Variablen *nach* gelöscht werden, die Sie im Treffer senden. In Wirklichkeit kann dies entweder vor ODER nach dem Senden des Treffers erfolgen, sollte jedoch in den [!DNL Experience Platform Launch]-Regeln konsistent sein, sodass Sie immer vor oder nach dem Festlegen von Variablen und dem Senden löschen. Denken Sie daran, dass Sie, wenn Sie die Variablen *vor* löschen möchten, `s.t()` ausführen, sicherstellen, dass Sie zuerst die Variablen löschen, dann die neuen Variablen festlegen und dann die neuen Daten schließlich nach [!DNL Analytics] senden.

**HINWEIS:** Das Löschen von Variablen ist bei der Ausführung nicht immer erforderlich, da  `s.tl()`die  `s.tl()` Variable jedes Mal neben der Variablen verwendet werden muss, um anzugeben,  [!DNL linkTrackVars] welche Variablen festgelegt werden (automatisch hinter den Kulissen in hinzugefügt  [!DNL Analytics]   [!DNL Experience Platform Launch]). Das bedeutet, dass fehlerhafte Variablen normalerweise nicht bei Verwendung von `s.tl()` eingehen, aber es wird dringend empfohlen, `s.t()` in einer SPA zu verwenden. Trotzdem möchte ich empfehlen, die Funktion Clear Variables sowohl für `s.t()` als auch für `s.tl()` in einer SPA-Umgebung zu verwenden, um eine qualitativ hochwertige Datenerfassung sicherzustellen.

Das folgende Video zeigt, wo/wie die Variablen in [!DNL Launch] gelöscht werden.

>[!VIDEO](https://video.tv.adobe.com/v/23049/?quality=12)

## Weitere zu berücksichtigende Aspekte {#additional-considerations}

### Windows mit benutzerspezifischem Code in [!DNL Experience Platform Launch] {#custom-code-windows-in-launch}

In der Erweiterung [!DNL Launch] [!DNL Analytics] können Sie an zwei Stellen benutzerdefinierten Code einfügen: Der Abschnitt [!UICONTROL Bibliotheksverwaltung] und der zusätzliche Abschnitt &quot;[!UICONTROL Tracker mit benutzerspezifischem Code konfigurieren]&quot;.

![Launch Benutzerdefinierter Analytics-Codefenster](assets/launch_analyticscustomcodewindows.png)

Es ist wichtig zu wissen, dass einer dieser Orte den Code nur einmal in ihnen ausführt, wenn das erste Laden der Seite auf Ihrer SPA erfolgt. Wenn der Code bei einer Ansichtsänderung oder einer Aktion auf Ihrer Site ausgeführt werden soll, sollten Sie der entsprechenden **[!UICONTROL Regel]** eine zusätzliche Aktion hinzufügen (z. B. beim &quot;Laden der Seite: event-view-end&quot; [!UICONTROL rule]), sodass der Code jedes Mal ausgeführt wird, wenn [!UICONTROL rule] ausgeführt wird. Legen Sie beim Erstellen dieser Aktion in der [!UICONTROL Regel] *Erweiterung = Core* und *Aktionstyp = Benutzerspezifischer Code* fest.

### &quot;Hybrid&quot;SPA/reguläre Sites {#hybrid-spa-regular-sites}

Einige Websites sind eine Kombination aus &quot;regulären&quot;Seiten und SPA Seiten. In diesem Fall müssen Sie eine Strategie verwenden, die für beide Seitentypen funktioniert. Achten Sie beim Konfigurieren Ihrer benutzerspezifischen Ereignisse auf der Site und beim Auslösen der Regeln in [!DNL Experience Platform Launch] darauf, dass von der Seite aus keine doppelten Treffer gesendet werden, die auf Hash-Änderungen usw. basieren. [!DNL Analytics] (wenn Sie so die [!DNL Experience Platform Launch]-Regel Trigger haben). In diesem Fall müssen Sie eine der Seitenansichten unterdrücken, damit Sie keine fehlerhaften Daten in Adobe Analytics erhalten.

Wenn Sie die Funktion in separate [!UICONTROL Regeln] unterteilen möchten, damit Sie mehr Kontrolle darüber haben, denken Sie daran/dokumentieren, dass Sie dies getan haben, sodass alle Änderungen an einer [!UICONTROL Regel] auch an der anderen [!UICONTROL Regel] vorgenommen werden können, wodurch Ihre [!DNL Analytics]-Datenintegrität geschützt wird.

### Integration mit [!DNL Target] über A4T {#integration-with-target-via-a4t}

Nur ein kurzer Hinweis. Wenn Sie mit [!DNL Target] mit A4T integrieren, stellen Sie sicher, dass die [!DNL Target]-Anforderung und die [!DNL Analytics]-Anforderung für dieselbe Ansichtsänderung dieselbe SDID aufweisen. Dadurch wird sichergestellt, dass Ihre Daten ordnungsgemäß mit den Lösungen synchronisiert werden.

Um die Treffer anzuzeigen, verwenden Sie ein Debugger- oder Paket-Sniffer-Programm. Sie können auch den Experience Cloud Debugger verwenden, eine Chrome-Erweiterung, die heruntergeladen werden kann [HERE](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj). [!DNL Target] sollte zuerst auf der Seite ausgelöst werden, damit Sie dies auch in der JavaScript-Konsole oder im Debugger überprüfen können.

## Zusätzliche Ressourcen {#additional-resources}

* [SPA über die Adobe](https://forums.adobe.com/thread/2451022)
* [Referenzarchitektur-Sites zur Implementierung von SPA in Experience Platform Launch](https://helpx.adobe.com/experience-manager/kt/integration/using/launch-reference-architecture-SPA-tutorial-implement.html)
