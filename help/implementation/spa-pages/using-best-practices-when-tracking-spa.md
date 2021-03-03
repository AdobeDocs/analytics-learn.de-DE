---
title: 'Verwenden von Best Practices bei der Verfolgung von Einzelseitenanwendungen (SPA) in Adobe Analytics '
description: In diesem Dokument beschreiben wir einige Best Practices, die Sie befolgen sollten und die Sie kennen sollten, wenn Sie Adobe Analytics zur Verfolgung von Einzelseitenanwendungen (SPA) verwenden. Dieses Dokument konzentriert sich auf die Verwendung von Experience Platform Launch, der empfohlenen Implementierungsmethode.
feature: Implementierungsgrundlagen
topics: spa
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1389
topic: SPA
role: '"Entwickler, Dateningenieur"'
level: Zwischenschaltung
translation-type: tm+mt
source-git-commit: f3b3fa7d91b0cb21005b57768ca23ed6700fcc03
workflow-type: tm+mt
source-wordcount: '1676'
ht-degree: 0%

---


# Verwenden von Best Practices bei der Verfolgung von Einzelseitenanwendungen (SPA) in Adobe Analytics {#using-best-practices-when-tracking-spa-in-adobe-analytics}

In diesem Dokument beschreiben wir einige Best Practices, die Sie befolgen sollten und die Sie kennen sollten, wenn Sie Adobe Analytics zur Verfolgung von Einzelseitenanwendungen (SPA) verwenden. Dieses Dokument konzentriert sich auf die Verwendung der Adobe [!DNL Experience Platform Launch], der empfohlenen Implementierungsmethode.

ERSTE HINWEISE:

* Die folgenden Elemente gehen davon aus, dass Sie [!DNL Experience Platform Launch] zur Implementierung auf Ihrer Site verwenden. Wenn Sie [!DNL Experience Platform Launch] nicht verwenden, müssen Sie diese jedoch an Ihre Implementierungsmethode anpassen.
* Alle SPA sind unterschiedlich, daher müssen Sie möglicherweise einige der folgenden Elemente anpassen, um Ihren Anforderungen am besten gerecht zu werden, aber wir wollten einige Best Practices mit Ihnen teilen. Dinge, über die Sie bei der Implementierung von Adobe Analytics auf SPA Seiten nachdenken müssen.

## Einfaches Diagramm zum Arbeiten mit SPA in [!DNL Experience Platform Launch] {#simple-diagram-of-working-with-spas-in-launch}

![SPA für Analysen beim Start](assets/spa_for_analyticsinlaunch.png)

**HINWEIS:** Wie angegeben, ist dies ein vereinfachtes Diagramm, wie SPA Seiten in einer Adobe Analytics-Implementierung mit  [!DNL Experience Platform Launch]behandelt werden. In den folgenden Abschnitten dieser Seite besprechen wir die Schritte und alle Fragen, die Sie sorgfältig prüfen oder bearbeiten sollten.

## Festlegen der Datenschicht {#setting-the-data-layer}

Wenn neue Inhalte auf eine SPA Seite geladen werden oder wenn eine Aktion auf einer SPA erfolgt, sollten Sie als Erstes die Datenschicht aktualisieren. Dies muss geschehen, BEVOR die benutzerspezifischen Ereignis- und Trigger-Regeln in [!DNL Experience Platform Launch] ausgelöst werden, damit [!DNL Experience Platform Launch] die neuen Werte aus der Datenschicht abrufen und in Adobe Analytics übertragen können.

Im Folgenden finden Sie eine Beispieldatenschicht, deren Elemente bei Änderung der Ansicht oder Aktion auf Ihrer SPA geändert werden können. Bei einer Änderung im Vollbildmodus/Mehrheitsbildschirm wäre es üblich, ein Element &quot;[!DNL pageName]&quot;zu ändern, sodass das neue Element in [!DNL Experience Platform Launch] erfasst und nach Adobe Analytics gesendet werden kann.

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

## Festlegen benutzerdefinierter Ereignis und Zuhören in [!DNL Experience Platform Launch] {#setting-custom-events-and-listening-in-launch}

Wenn neue Inhalte auf der Seite geladen werden oder eine Aktion auf der Site stattfindet, sollten Sie [!DNL Experience Platform Launch] informieren, damit eine Regel ausgeführt und Daten an [!DNL Analytics] gesendet werden können. Es gibt verschiedene Möglichkeiten, dies zu tun: [!UICONTROL Direktaufruf] [!UICONTROL rules] oder Benutzerspezifische Ereignis.

* [!UICONTROL Direct ] [!UICONTROL CallRules]: in  [!DNL Experience Platform Launch]können Sie eine  [!UICONTROL direkte ]  Aufrufregel einrichten, die ausgeführt wird, wenn sie direkt von der Seite aufgerufen wird. Wenn das Laden der Seite oder die Aktion auf Ihrer Site sehr einfach ist oder wenn es eindeutig ist und Sie jedes Mal einen bestimmten Satz von Anweisungen ausführen können (setzen Sie [!DNL eVar4] auf X und Trigger [!DNL event2] jedes Mal), können Sie einen [!UICONTROL Direktaufruf] [!UICONTROL Regel] verwenden. Siehe [!DNL Experience Platform Launch] Dokumentation zum Erstellen von [!UICONTROL Direktaufruf] [!UICONTROL Regeln].
* Benutzerspezifische Ereignis: Für weitere Funktionen und für die Möglichkeit, eine Nutzlast mit verschiedenen Werten dynamisch anzuhängen, sollten Sie benutzerdefinierte JavaScript-Ereignis festlegen und auf sie in [!DNL Experience Platform Launch] achten, wo Sie die Nutzlast verwenden können, um Variablen festzulegen und die Daten nach Adobe Analytics zu senden. Es ist wahrscheinlicher, dass Sie diese Funktion benötigen, und daher gilt diese Option als Best Practice. Jede Funktion auf Ihrer Site kann jedoch bestimmen, welche Methode am besten geeignet ist. Wir werden in diesem Dokument vorankommen, vorausgesetzt, Sie müssen diese Methode für benutzerspezifische Ereignis verwenden.

**Beispiele:** Im  [](https://helpx.adobe.com/experience-manager/kt/integration/using/launch-reference-architecture-SPA-tutorial-implement.html) THIShelp-Dokument stehen Links zu Beispielsites mit implementierten SPA  [!DNL Analytics] (und anderen Experience Cloud-Lösungen) sowie Dokumente zur Beschreibung der implementierten Elemente zur Verfügung. In diesen SPA wurden die folgenden benutzerspezifischen Ereignis verwendet:

* [!DNL event-view-start]: Dieses Ereignis sollte auf dem Beginn der Ansicht der Ansicht/des Status, die geladen wird, ausgelöst werden.
* [!DNL event-view-end]: Dieses Ereignis sollte auch dann ausgelöst werden, wenn eine Ansichten-/Statusänderung stattgefunden hat und alle SPA Komponenten auf der Seite vollständig geladen wurden. Dies ist das Ereignis, das normalerweise einen Trigger nach Adobe Analytics führt.
* [!DNL event-action-trigger]: Dieses Ereignis sollte ausgelöst werden, wenn ein Ereignis auf der Seite auftritt, mit Ausnahme der Ansicht-/Statusladung. Dies kann ein Klick-Ereignis oder eine kleinere Inhaltsänderung ohne Änderung der Ansicht sein.

Weitere Informationen dazu, wie und wann diese ausgelöst werden, finden Sie auf den oben genannten Seiten/Dokumenten. Sie müssen nicht dieselben Ereignis verwenden, aber die hier aufgelisteten Funktionen sind empfohlene Best Practices. Das folgende Video zeigt eine Beispielsite und wo in [!DNL Experience Platform Launch], um auf die benutzerdefinierten Ereignis zu hören.

>[!VIDEO](https://video.tv.adobe.com/v/23024/?quality=12)

## Ausführen von s.t() oder s.tl() in [!DNL Experience Platform Launch] [!UICONTROL Regel] {#running-s-t-or-s-tl-in-the-launch-rule}

Eines der wichtigsten Dinge, die für [!DNL Analytics] beim Arbeiten mit einem SPA zu verstehen sind, ist der Unterschied zwischen `s.t()` und `s.tl()`. Sie lösen eine dieser Methoden in [!DNL Experience Platform Launch] aus, um Daten an [!DNL Analytics] zu senden, aber Sie müssen wissen, wann die einzelnen gesendet werden.

* **s.t()** - Das &quot;t&quot; steht für &quot;track&quot; und ist eine normale Ansicht. Ändert sich die Ansicht auch dann, wenn sich die URL nicht ändert, so, dass ** Sie  als neue &quot;Seite&quot;betrachten würden? Wenn ja, setzen Sie die Variable s.[!DNL pageName] und verwenden Sie `s.t()`, um den Aufruf an [!DNL Analytics] zu senden

* **s.tl()** - &quot;tl&quot; steht für &quot;track link&quot; und wird normalerweise zur Verfolgung von Klicks oder kleinen Inhaltsänderungen auf der Seite verwendet, im Gegensatz zu einer Vollbildänderung. Wenn die Änderung auf Ihrer Seite klein ist, damit Sie sie nicht als vollständige neue &quot;Seite&quot;betrachten, verwenden Sie `s.tl()` und machen Sie sich keine Gedanken über die Festlegung der Variablen s.pageName, da [!DNL Analytics] diese ignoriert.

**TIPP:** Manche Benutzer verwenden eine allgemeine Richtlinie, wonach der Bildschirm, wenn er sich um mehr als 50 % ändert, als Ansicht und Verwendung der Seite betrachtet werden sollte  `s.t()`. Wenn die Änderung am Bildschirm weniger als 50 % beträgt, verwenden Sie `s.tl()`. Es liegt jedoch ganz bei Ihnen und was Sie als neue &quot;Seite&quot;betrachten und wie Sie Ihre Site in Adobe Analytics verfolgen möchten.

Das folgende Video zeigt, wo und wie `s.t()` oder `s.tl()` in Launch by Adobe Trigger wird.

>[!VIDEO](https://video.tv.adobe.com/v/23048/?quality=12)

## Löschen von Variablen {#clearing-variables}

Bei der Verfolgung Ihrer Site mit Adobe Analytics möchten Sie natürlich nur die richtigen Daten zum richtigen Zeitpunkt an [!DNL Analytics] senden. In einer SPA Umgebung kann ein Wert, der in einer [!DNL Analytics]-Variablen verfolgt wird, bestehen bleiben und erneut an [!DNL Analytics] gesendet werden, möglicherweise, wenn dies nicht mehr gewünscht wird. Aus diesem Grund gibt es eine Funktion in der [!DNL Analytics] [!DNL Launch]-Erweiterung, um die Variablen zu löschen. Wenn Sie die nächste Bildanforderung ausführen und Daten an [!DNL Analytics] senden, erhalten Sie eine neue Tonspur.

Im Diagramm oben haben wir es am Ende des Prozesses aufgelistet, indem Sie die Variablen *nach* löschen, die Sie im Treffer senden. In Wirklichkeit kann dies entweder vor ODER nach dem Senden des Treffers erfolgen, sollte jedoch in den [!DNL Experience Platform Launch]-Regeln konsistent sein, sodass Sie immer vor oder nach dem Festlegen von Variablen löschen und sie senden. Denken Sie daran, dass Sie, wenn Sie die Variablen *vor* löschen möchten, `s.t()` ausführen, sicherstellen, dass Sie zunächst die Variablen löschen, dann die neuen Variablen festlegen und dann die neuen Daten schließlich nach [!DNL Analytics] senden.

**HINWEIS:** Das Löschen von Variablen ist bei Ausführung nicht immer erforderlich,  `s.tl()`da  `s.tl()` die  [!DNL linkTrackVars] Variable jedes Mal neben ihr verwendet werden muss, um festzustellen,  [!DNL Analytics] welche Variablen festgelegt werden (automatisch hinter den Kulissen hinzugefügt  [!DNL Experience Platform Launch]). Dies bedeutet, dass fehlerhafte Variablen normalerweise nicht bei Verwendung von `s.tl()` auftreten, es wird jedoch sehr empfohlen, wenn `s.t()` in einer SPA Umgebung verwendet wird. Trotzdem möchte ich Ihnen empfehlen, die Funktion &quot;Variablen löschen&quot;sowohl für `s.t()` als auch `s.tl()` in einer SPA Umgebung zu verwenden, um eine qualitativ hochwertige Datenerfassung sicherzustellen.

Das folgende Video zeigt, wo/wie die Variablen in [!DNL Launch] gelöscht werden.

>[!VIDEO](https://video.tv.adobe.com/v/23049/?quality=12)

## Weitere zu berücksichtigende Aspekte {#additional-considerations}

### Fenster mit benutzerdefiniertem Code in [!DNL Experience Platform Launch] {#custom-code-windows-in-launch}

In der Erweiterung [!DNL Launch] [!DNL Analytics] können Sie an zwei Stellen benutzerdefinierten Code einfügen: Der Abschnitt [!UICONTROL Bibliotheksverwaltung] und der zusätzliche Abschnitt &quot;[!UICONTROL Tracker mithilfe von benutzerspezifischem Code konfigurieren]&quot;.

![Benutzerdefinierte Codefenster von Analytics starten](assets/launch_analyticscustomcodewindows.png)

Es ist wichtig zu wissen, dass einer dieser Orte wirklich nur einmal den Code in ihnen ausführen wird, wenn das Laden der ersten Seite auf Ihrer SPA erfolgt. Wenn der Code bei einer Änderung der Ansicht oder bei einer Aktion auf Ihrer Site ausgeführt werden soll, sollten Sie der entsprechenden **[!UICONTROL Regel]** eine zusätzliche Aktion hinzufügen (z. B. im &quot;Seitenladevorgang: Ereignis-Ansicht-end&quot; [!UICONTROL rule]), sodass der Code jedes Mal ausgeführt wird, wenn [!UICONTROL rule] ausgeführt wird. Wenn Sie diese Aktion in der [!UICONTROL Regel] erstellen, setzen Sie *Extension = Core* und *Aktionstyp = Benutzerspezifischer Code*.

### &quot;Hybrid&quot;-SPA/Reguläre Sites {#hybrid-spa-regular-sites}

Bei einigen Sites handelt es sich um eine Kombination aus &quot;normalen&quot;Seiten und SPA Seiten. In diesem Fall müssen Sie eine Strategie verwenden, die für beide Seitentypen funktioniert. Achten Sie beim Konfigurieren Ihrer benutzerspezifischen Ereignis auf der Site und Auslösen der Regeln in [!DNL Experience Platform Launch] darauf, dass keine Dubletten-Treffer von der Seite nach [!DNL Analytics] gesendet werden, basierend auf Hash-Änderungen usw. (wenn Sie so die [!DNL Experience Platform Launch]-Regel Trigger haben). In diesem Fall müssen Sie eine der Ansichten unterdrücken, damit Sie keine fehlerhaften Daten in Adobe Analytics erhalten.

Wenn Sie die Funktion in separate [!UICONTROL Rules] unterteilen, damit Sie mehr Kontrolle darüber haben, sollten Sie sich daran erinnern/Dokument, dass Sie dies getan haben, sodass alle Änderungen an einer [!UICONTROL Regel] auch an der anderen [!UICONTROL Regel] vorgenommen werden können, um Ihre [!DNL Analytics] Datenintegrität zu schützen.

### Integration mit [!DNL Target] über A4T {#integration-with-target-via-a4t}

Nur eine kurze Aufzählung. Wenn Sie mit A4T in [!DNL Target] integrieren, stellen Sie sicher, dass die [!DNL Target]-Anforderung und die [!DNL Analytics]-Anforderung auf derselben Ansicht dieselbe SDID aufweisen. Dadurch wird sichergestellt, dass Ihre Daten ordnungsgemäß mit den Lösungen synchronisiert werden.

Um die Treffer anzuzeigen, verwenden Sie ein Debugger- oder Paket-Sniffer-Programm. Sie können auch den Experience Cloud Debugger, eine Chrome-Erweiterung, die heruntergeladen werden können [HERE](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj). [!DNL Target] sollte zuerst auf der Seite ausgelöst werden, damit Sie dies auch in der JavaScript-Konsole oder im Debugger überprüfen können.

## Zusätzliche Ressourcen {#additional-resources}

* [SPA über die Adobe](https://forums.adobe.com/thread/2451022)
* [Referenzarchitektur-Sites, die zeigen, wie SPA in Experience Platform Launch implementiert werden](https://helpx.adobe.com/experience-manager/kt/integration/using/launch-reference-architecture-SPA-tutorial-implement.html)