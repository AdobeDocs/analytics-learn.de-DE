---
title: Best Practices für die Implementierung von Einzelseiten-Programmen (SPA)
description: Erfahren Sie mehr über Best Practices zur Implementierung von Adobe Analytics in Einzelseiten-Programmen (SPA). Dazu gehört die Verwendung von Experience Platform-Tags, der empfohlenen Implementierungsmethode.
feature: Implementation Basics
topics: spa
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1389
topic: SPA
role: Developer, Data Engineer
level: Intermediate
exl-id: 8fe63dd1-9629-437f-ae07-fe1c5a05fa42
source-git-commit: d78c3351d2a98704396ceb8f84d123dd463befe5
workflow-type: ht
source-wordcount: '1313'
ht-degree: 100%

---

# Best Practices für die Implementierung von Einzelseiten-Programmen (SPA) {#implementation-best-practices-for-single-page-appliations}

Erfahren Sie mehr über die Best Practices zur Implementierung von [!DNL Adobe Analytics] auf Einzelseiten-Programmen (SPA). Dazu gehört die Verwendung von [!DNL Experience Platform Tags], der empfohlenen Implementierungsmethode.

VORABBEMERKUNGEN:

* Der folgende Inhalt bezieht sich auf die Verwendung von [!DNL Experience Platform Tags] zur Implementierung von Adobe Analytics auf Ihrer Website. Diese Überlegungen gelten auch, wenn [!DNL Experience Platform Tags] nicht verwendet wird, und müssen daher an Ihre Implementierungsmethode angepasst werden.
* Es gibt Unterschiede in SPA. Daher sollten Sie Ihren Ansatz Ihren Bedürfnissen entsprechend anpassen.

## Einfaches Diagramm zum Arbeiten mit SPAs in [!DNL Experience Platform Tags] {#simple-diagram-of-working-with-spas-in-tags}

![SPA für Analysen in Tags](assets/spa_for_analyticsinlaunch.png)

**HINWEIS**: Dies ist ein vereinfachtes Diagramm, wie SPA-Seiten in einer Adobe Analytics-Implementierung mit [!DNL Experience Platform Tags] behandelt werden. In den folgenden Abschnitten werden die zu berücksichtigenden Schritte und Probleme beschrieben.

## Festlegen der Datenschicht {#set-the-data-layer}

Wenn neue Inhalte geladen werden oder eine Aktion auf einer SPA-Seite erfolgt, *aktualisieren Sie zuerst die Datenschicht*. Dies muss **vor** der Ausführung eines benutzerdefinierten Ereignisses, das eine Regel in [!DNL Experience Platform Tags] auslöst, geschehen. Dadurch wird sichergestellt, dass die richtigen Werte aus der Datenschicht in Tags und dann in Adobe Analytics übertragen werden.

Im Folgenden finden Sie ein Beispiel für eine Datenschicht. Jedes dieser Elemente kann sich basierend auf der ursprünglichen Ansicht oder einer nachträglichen Änderung der Ansicht aufgrund einer auf Ihrer SPA-Seite durchgeführten Aktion ändern. Bei einer Änderung der Voll- oder Mehrheitsansicht ist es beispielsweise üblich, einen eindeutigen „[!DNL pageName]“-Wert zu übergeben, um zwischen den Ansichten in Adobe Analytics-Berichten zu unterscheiden.

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

## Festlegen benutzerdefinierter Ereignisse und Überwachen dieser Ereignisse in [!DNL Experience Platform Tags] {#setting-custom-events-and-listening-in-tags}

Wenn neue Inhalte geladen werden oder eine Aktion auf der SPA erfolgt, müssen Experience Platform-Tags informiert werden, um eine Regel auszuführen, die Daten an [!DNL Analytics] sendet. Hierfür gibt es mehrere Ansätze: [!UICONTROL Direktaufrufregeln] oder benutzerdefinierte Ereignisse.

* [!UICONTROL Direktaufrufregeln]: Richten Sie eine [!UICONTROL Direktaufrufregel] ein, die ausgeführt wird, wenn sie direkt von der Seite aufgerufen wird. Wenn das Laden oder die Aktion der Seite einfach oder eindeutig ist und jedes Mal einen bestimmten Satz von Anweisungen ausführen kann (beispielsweise [!DNL eVar4] auf X setzen und [!DNL event2] jedes Mal auslösen), dann ist dieser Ansatz geeignet. Weitere Details zum Erstellen von [!UICONTROL Direktanrufregeln] finden Sie in der [!DNL Experience Platform Tags]-Dokumentation.
* Benutzerdefinierte Ereignisse: Wenn Sie eine Payload mit eindeutigen Werten für Ereignisse, die auf SPA-Seiten auftreten, dynamisch anhängen müssen, verwenden Sie benutzerdefinierte JavaScript-Ereignisse und überwachen Sie diese in [!DNL Experience Platform Tags]. Verwenden Sie die Payload, um Datenelemente und Analytics-Variablen in Tags festzulegen. Diese Methode wird als Best Practice betrachtet, da diese Anforderung normalerweise für SPAs gilt. Unsere folgenden Beispiele verwenden die Methode für benutzerdefinierte Ereignisse.

**Beispiele**: [In diesem](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html?lang=de) Hilfedokument gibt es Links zu Beispiel-SPA-Sites, die [!DNL Analytics] und andere Experience Cloud-Lösungen implementieren. In diesen Beispielen werden die folgenden benutzerdefinierten Ereignisse verwendet:

* **[!DNL Event-view-start]**: Wird beim Start der Ansicht/des Status ausgeführt, die/der geladen wird.
* **[!DNL Event-view-end]**: Wird ausgeführt, wenn eine Änderung der Ansicht/des Status erfolgt und alle SPA-Komponenten auf der Seite vollständig geladen sind. Dies ist das Ereignis, das normalerweise Daten an Adobe Analytics sendet.
* **[!DNL Event-action-trigger]**: Wird ausgeführt, wenn ein beliebiges Ereignis auf der Seite auftritt, mit Ausnahme des Ladevorgangs von Ansicht/Status. Beispiele hierfür sind ein Klick-Ereignis oder eine kleinere Inhaltsänderung ohne Änderung der Ansicht.

Weitere Informationen dazu, wie und wann diese Ereignisse ausgelöst werden, finden Sie auf den oben genannten Seiten und in den entsprechenden Dokumenten. Sie müssen nicht dieselben Ereignisnamen in Ihrer Implementierung verwenden. Es ist wichtig, den funktionalen Anwendungsfall für die verwendete Methode zu verstehen, da dies die empfohlene Best Practice für jede Methode ist. Das folgende Video zeigt eine beispielhafte SPA-Seite und einen Beispiel-Code in [!DNL Experience Platform Tags], der auf die benutzerdefinierten Ereignisse wartet.

>[!VIDEO](https://video.tv.adobe.com/v/23024/?quality=12)

## Ausführen von s.t() oder s.tl() in [!DNL Experience Platform Tags] {#running-s-t-or-s-tl-in-the-launch-rule}

Ein wichtiges Konzept für [!DNL Analytics] bei der Arbeit mit einer SPA ist der Unterschied zwischen `s.t()` und `s.tl()`. Ihr Code löst die eine oder die andere dieser Methoden in [!DNL Experience Platform Tags] aus, um Daten an [!DNL Analytics] zu senden.

* **s.t()**: „t“ steht für „track“ (nachverfolgen) und stellt eine Seitenansicht dar. Wenn sich die Ansicht so stark ändert, dass Sie sie als neue „Seite“ *ansehen*, verwenden Sie diesen Aufruf. Setzen Sie einen eindeutigen Wert für die Variable [!DNL s.pageName] und verwenden Sie `s.t()`, um die Daten an [!DNL Analytics] zu senden.

* **s.tl()**: Das „tl“ steht für „track link“ (Link nachverfolgen) und repräsentiert einen Link-Klick oder eine kleine Inhaltsänderung. Wenn die Änderung der Ansicht minimal ist, verwenden Sie `s.tl()`, um einen eindeutigen Wert über die Interaktion an [!DNL Analytics] zu übergeben. Diese übergebene Variable ist nicht [!DNL s.pageName], da dies in Analytics ignoriert wird, wenn `s.tl()`-Aufrufe empfangen werden.

**TIPP:** Als allgemeine Richtlinie sollte man, wenn sich der Bildschirm um mehr als 50 % ändert, den `s.t()`-Seitenansicht-Aufruf verwenden. Verwenden Sie andernfalls `s.tl()`. Überlegen Sie jedoch nach eigenem Ermessen, welche Aktionen eine neue „Seite“ darstellen und wie dies in Adobe Analytics-Berichten dargestellt werden soll.

Das folgende Video zeigt, wo und wie Sie `s.t()` oder `s.tl()` in Tags auslösen.

>[!VIDEO](https://video.tv.adobe.com/v/23048/?quality=12)

## Löschen von Variablen {#clear-variables}

Senden Sie die richtigen Daten zur richtigen Zeit an [!DNL Analytics]. In einer SPA-Umgebung bleibt ein in einer [!DNL Analytics]-Variable gespeicherter Wert bestehen und wird erneut an [!DNL Analytics] gesendet, möglicherweise auch dann, wenn Sie ihn nicht mehr benötigen. In der [!DNL Analytics] [!DNL Tags]-Erweiterung gibt es eine Funktion zum Löschen der Variablen, um sicherzustellen, dass beim nächsten Aufruf nicht versehentlich Daten an [!DNL Analytics] gesendet werden.

Das obige Diagramm zeigt Variablen, die geleert werden, *nachdem* Sie Daten hinein gesendet haben. In Wirklichkeit kann dies vor ODER nach dem Aufruf geschehen, aber seien Sie für eine saubere Implementierung konsequent in Ihren [!DNL Experience Platform Tags]-Regeln. Wenn Sie Variablen löschen, *bevor* Sie `s.t()` ausführen, legen Sie die neuen Variablen sofort nach dem Aufruf fest und fahren Sie dann fort, die neuen Daten in [!DNL Analytics] zu senden.

**HINWEIS:** Das Löschen von Variablen ist nicht immer erforderlich, wenn `s.tl()` ausgeführt wird. Dieser Aufruf erfordert die Verwendung der Variable [!DNL linkTrackVars], um [!DNL Analytics] anzuweisen, welche Variablen gesetzt werden sollen. Dies geschieht automatisch in [!DNL Experience Platform Tags] durch Konfiguration. Es verhindert, dass fehlerhafte Variablen gesetzt werden, im Gegensatz zum Verhalten bei `s.t()`-Aufrufen in einer SPA-Umgebung. Um die sauberste und zuverlässigste Implementierung zu gewährleisten, ist es wahrscheinlich einfacher, die Funktion „clear variables“ (Variablen bereinigen) für beide Aufrufe in einer SPA-Umgebung zu verwenden.

Das folgende Video zeigt, wo und wie man Variablen in [!DNL Tags] löscht.

>[!VIDEO](https://video.tv.adobe.com/v/23049/?quality=12)

## Weitere Überlegungen {#additional-considerations}

### Fenster mit benutzerdefiniertem Code in [!DNL Experience Platform Tags] {#custom-code-windows-in-tags}

In der [!DNL Tags] [!DNL Analytics]-Erweiterung gibt es zwei Stellen, an denen benutzerdefinierter Code eingefügt werden kann: die Abschnitte [!UICONTROL Bibliotheksverwaltung] und [!UICONTROL Konfiguration des Trackers mit benutzerdefiniertem Code].

![Benutzerdefinierte Code-Fenster in Tags Analytics](assets/launch_analyticscustomcodewindows.png)

An jedem dieser Orte wird der darin enthaltene Code einmal beim ersten Laden Ihrer SPA-Seite ausgeführt. Wenn der Code bei einer Ansicht- oder Aktionsänderung ausgeführt werden soll, implementieren Sie diesen Code in der entsprechenden **[!UICONTROL Regel]** (beispielsweise die Regel „page load: event-view-end“), um sicherzustellen, dass der Code jedes Mal ausgeführt wird, wenn die [!UICONTROL Regel] ausgeführt wird. Wenn Sie die Aktion in der [!UICONTROL Regel] erstellen, setzen Sie *Extension = Core* und *Action Type = Custom Code*.

### „Hybride“ SPA und traditionelle Sites {#hybrid-spa-and-traditional-sites}

Einige Websites bestehen aus einer Kombination von herkömmlichen und SPA Seiten. In diesem Fall sollten Sie eine Strategie verwenden, die für beide Seitentypen funktioniert. Beim Konfigurieren Ihrer benutzerdefinierten Ereignisse auf der Site und dem Auslösen von Regeln in [!DNL Experience Platform Tags] stellen Sie sicher, dass keine doppelten Treffer in [!DNL Analytics] aufgrund von Hash-Änderungen und ähnlichem gesendet werden. Unterdrücken Sie in diesem Fall eine der Seitenansichten, um zu verhindern, dass doppelte Daten an Adobe Analytics übergeben werden.

Wenn Sie sich entscheiden, die Funktionalität in einzelne [!UICONTROL Regeln] aufzuteilen, um mehr Kontrolle zu haben, denken Sie daran, dies zu dokumentieren. Wenn Sie eine [!UICONTROL Regel] ändern, nehmen Sie die gleiche Änderung an der anderen [!UICONTROL Regel] vor.

### Integration mit [!DNL Target] über A4T {#integration-with-target-using-a4t}

Bei der Integration mit [!DNL Target] über A4T stellen Sie sicher, dass die [!DNL Target]- und [!DNL Analytics]-Anfragen, die über dieselbe Ansicht oder Aktion gesendet werden, denselben SDID-Parameterwert übergeben. Dadurch wird sichergestellt, dass Ihre Daten im Backend ordnungsgemäß synchronisiert werden.

Verwenden Sie zum Anzeigen dieser Treffer einen Debugger oder ein Tool zur Paketüberwachung. Adobe bietet zu diesem Zweck einen Experience Platform Debugger. Es handelt sich um eine Chrome-Erweiterung, die [hier heruntergeladen werden kann](https://chrome.google.com/webstore/detail/adobe-experience-platform/bfnnokhpnncpkdmbokanobigaccjkpob?hl=de). [!DNL Target] sollte zuerst auf der Seite ausgeführt werden. Dies kann auch im Debugger überprüft werden.

## Zusätzliche Ressourcen {#additional-resources}

* [SPA in den Adobe-Foren](https://experienceleaguecommunities.adobe.com:443/t5/adobe-experience-platform-launch/best-practices-for-single-page-apps/m-p/267940?lang=de)
* [Referenz-Sites zur Architektur, die zeigen, wie SPA in Experience Platform Launch implementiert wird](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html?lang=de)
