---
title: Einbetten von Power Apps
description: In diesem Thema wird beschrieben, wie Power Apps in den Client eingebettet werden, um die Funktionalität des Produkts zu erhöhen.
author: jasongre
manager: AnnBe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: 9585d5a399ebf45b0ad7640f3c4e48d8afc46cd8
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3017727"
---
# <a name="embed-microsoft-power-apps"></a>Einbetten von Microsoft Power Apps

[!include [banner](../includes/banner.md)]

Finance and Operations unterstützt die Integration in Microsoft Power Apps, einen Dienst für Entwickler und nicht technische Benutzer zur Erstellung benutzerdefinierter Geschäfts-Apps für mobile Geräte, Tablets und das Internet, ohne Code zu schreiben. Power Apps, die von Ihnen, Ihrer Organisation oder dem breiteren Ökosystem entwickelt werden, können dann in Finance and Operations-Apps eingebettet werden, um die Funktionalität des Produkts zu erhöhen. Beispielsweise erstellen Sie möglicherweise eine App von Power Apps, die eine Finance and Operations-App mit Informationen ergänzt, die von einem anderen System abgerufen werden.

Um weitere Informationen zum Einbetten von Power Apps zu erhalten, sehen Sie sich das kurze Video [Einbetten von Power Apps](https://www.youtube.com/watch?v=x3qyA1bH-NY) an.

## <a name="adding-an-embedded-app-from-power-apps-to-a-page"></a>Hinzufügen einer eingebetteten App von Power Apps zu einer Seite

### <a name="overview"></a>Übersicht

Bevor Sie eine App von Power Apps in den Client einbetten, müssen Sie zuerst eine App mit den gewünschten Grafiken und/oder den Fähigkeiten suchen oder erstellen. Hier wird nicht der detaillierte Prozess der Erstellung von Apps beschrieben. Das Thema [Einführung in Power Apps](https://docs.microsoft.com/powerapps/getting-started) ist ein guter Ausgangspunkt, wenn Sie noch nicht mit Power Apps vertraut sind.

Wenn Sie soweit sind, eine bestimmte App einzubetten, können Sie zwischen einer von zwei Methoden des Zugriffs auf die App auf einer Seite auswählen, je nachdem welche Route für Ihr Szenario besser geeignet ist. Die erste Methode erfolgt über die Power Apps-Schaltfläche, die dem Standardaktivitätsbereich hinzugefügt wurde. Apps, die über diesen Mechanismus hinzugefügt werden, werden in der Power Apps-Menüschaltfläche als Menüoptionen angezeigt. Wenn sie ausgewählt sind, öffnet jedes dieser Menüelemente einen Seitenbereich, der die eingebettete App enthält. Alternativ können Sie wählen, eine App direkt auf einer Seite als neue Registerkarte, Inforegister, Blatt oder als Bereich in einen Arbeitsbereich einzubetten.

Wenn Sie die eingebettete App konfigurieren, können Sie ein einzelnes Feld auswählen, das Sie als Kontext an die App übermitteln wollen. Dies ermöglicht es der App, basierend auf den aktuell angezeigten Daten zu reagieren.

### <a name="details"></a>Detaildaten

Die folgenden Anweisungen zeigen, wie eine App von Power Apps in den Webclient eingebettet wird.

1. Gehe Sie zur Seite, in der Sie die App einbetten möchten. Dies ist die gleiche Seite, die sämtliche Daten enthält, die an die App als Eingabe zu übergeben ist.
2. Öffnen Sie das Feld **Eine App aus Power Apps hinzufügen**:

    - Klicken Sie **Optionen** und wählen Sie anschließend **Diese Seite personalisieren** aus. Wählen Sie im Menü **Einfügen** **Power Apps**. Schließlich wählen Sie die Region aus, in der Sie die App hinzufügen möchten. Wenn Sie die App unter der Power Apps-Menüschaltfläche einbetten möchten, wählen Sie den Aktivitätsbereich aus. Wenn Sie die App direkt auf der Seite einbetten möchten, wählen Sie die entsprechende Registerkarte, das Inforegister, das Etikett oder den Bereich aus (sofern Sie in einem Arbeitsbereich sind).
    - Wenn die App über die Power Apps-Menüschaltfläche aufgerufen wird, können Sie alternativ im Standardaktivitätsbereich auf die Menüschaltfläche **Power Apps** klicken und dann **Eine App hinzufügen** auswählen.

3. Die eingebettete App konfigurieren:

    - Das Feld **Name** gibt den Text an, der für die Schaltfläche oder Registerkarte angezeigt wird, der die eingebettete App enthält. Oftmals können Sie ggf. den Namen der App in diesem Feld wiederholen.
    - **App-Kennung** ist der GUID für die App, die Sie einbetten möchten. Um diesen Wert abzurufen, suchen Sie die App auf [web.powerapps.com](https://web.powerapps.com), und suchen Sie dann das Feld **App-ID** unter **Details**.
    - Für die **Eingabekontext für die App** können Sie optional das Feld auswählen, das die Daten enthält, die an die App weitergegeben werden sollen. Weitere Informationen dazu, wie die [Apps auf die von Finance and Operations-Apps](#building-a-power-app-that-leverages-data-sent-from-finance-and-operations-apps) gesendeten Daten zugreifen kann, finden Sie im Abschnitt Erstellen einer App, die Daten aus Finance and Operations-Apps nutzt, weiter unten in diesem Thema.
    - Wählen Sie die **Anwendungsgröße** die zum Typ der App passt, die Sie einbetten. Wählen Sie **Schmal** für Apps aus, die für mobile Geräte erstellt wurden, und **Breit** für Apps aus, die für Tablets erstellt wurden. Dadurch wird sichergestellt, dass für die eingebettete App ausreichend Platz zugeteilt wird.
    - Das Inforegister **Juristische Personen** bietet die Möglichkeit, auszuwählen, für welche juristischen Personen die App verfügbar ist. Standardmäßig wird die App in allen juristischen Personen verfügbar gemacht. Diese Option ist nur verfügbar, wenn die Funktion [Gespeicherte Ansichten](saved-views.md) deaktiviert ist. 

4. Nachdem Sie bestätigt haben, dass die Konfiguration korrekt ist, klicken Sie **Einfügen**, um die Power-App auf der Seite einzubetten. Sie werden dazu aufgefordert, den Browser zu aktualisieren, um die eingebettete App anzuzeigen.

## <a name="sharing-an-embedded-app"></a>Freigeben einer eingebetteten App

Nachdem Sie ein Apps auf einer Seite eingebettet und bestätigt haben, dass sie bei jedem Datenkontext ordnungsgemäß funktioniert, der von der Seite abgeschlossen wurde, sollten Sie dies für andere Benutzer im System freigeben. Dies kann auf zwei unterschiedliche Arten mithilfe der Personalisierungsfunktionen des Produkts ausgeführt werden:

- Das empfohlene Szenario erfolgt über den Systemadministrator, der eine Personalisierung an alle Benutzer oder eine Teilmenge der Benutzer mithilfe von Push übertragen kann.
- Alternativ können Sie Ihre Änderungen exportieren (genannt Personalisierungen), sie an einen oder mehrere Benutzer übermitteln und jeden dieser Benutzer dazu veranlassen, Ihre Änderungen zu importieren. Die Personalisierungssymbolleiste verfügt über Aktionen, mit denen Sie Personalisierungen exportieren und importieren können.

Unter [Personalisieren der Benutzeroberfläche](personalize-user-experience.md) finden Sie weitere Details zu den Personalisierungsfähigkeiten im Produkt und wie Sie diese verwenden können.

## <a name="building-an-app-that-leverages-data-sent-from-finance-and-operations-apps"></a>Erstellen einer App, die die von Finance and Operations Apps gesendete Daten nutzt

Ein wichtiger Teil beim Erstellen einer App von Power Apps, die in eine Finance and Operations App eingebettet wird, verwendet die Eingabedaten dieser Anwendung. Von der Power Apps Entwicklungserfahrung können die Eingabedaten von einer Finance and Operations-App kann über die Param („EntityId“) zugegriffen werden.

In der OnStart-Funktion der App können Sie die Eingabedaten von Finance and Operations-Apps auf eine Variable wie die folgende festlegen:

```
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-app"></a>Anzeigen einer App

Um eine eingebettete App auf einer Seite in Finance and Operations-Apps anzuzeigen, wechseln Sie einfach zu einer Seite mit einer eingebetteten App. Denken Sie daran, dass Apps auf die Power Apps-Schaltfläche im Standardaktivitätsbereich zugreifen oder direkt auf der Seite als neue Registerkarte, neues Inforegister, neues Blatt oder als neuer Bereich in einem Arbeitsbereich angezeigt werden kann. Wenn ein Benutzer zunächst versucht, eine App auf einer Seite zu laden, wird er oder sie dazu aufgefordert, sich anzumelden, um sicherzustellen, dass der Benutzer die entsprechenden Berechtigungen hat, um die App zu verwenden.

## <a name="editing-an-embedded-app"></a>Bearbeiten einer eingebetteten App

Nachdem eine Apps auf einer Seite eingebettet wurde, müssen Sie möglicherweise einige Änderungen der Variante von der App vornehmen. Angenommen, Sie möchten möglicherweise das Etikett ändern, das der eingebetteten App zugeordnet ist, oder eine neue Version der App wurde erstellt und Sie müssen die-App Kennung aktualisieren, um auf die aktuellste Version zu verweisen.

Gehen Sie folgendermaßen vor, um die Konfiguration von einer eingebetteten App zu bearbeiten:

1. Gehen Sie zum Bereich **App bearbeiten**.

    - Wenn die eingebettete App über die Power Apps-Menüschaltfläche aufgerufen wird, klicken Sie mit der rechten Maustaste auf die Power Apps-Menüschaltfläche, und wählen Sie **Personalisieren** aus. Wählen Sie im Dropdownmenü **App auswählen** die App aus, die Sie konfigurieren möchten.
    - Wenn die eingebettete App direkt auf der Seite angezeigt wird, wählen Sie **Optionen** und dann **Diese Seite personalisieren** aus. Bei Verwendung des Tools **Auswählen** klicken Sie auf die eingebettete App.

2. Nehmen Sie die erforderlichen Änderungen an der Appkonfiguration vor, und klicken Sie anschließend auf **Speichern**.

## <a name="removing-an-app"></a>App entfernen

Nachdem eine App auf einer Seite eingebettet wurde, gibt es zwei Möglichkeiten, sie nach Bedarf zu entfernen:

- Wechseln Sie zum Bereich **Eine App bearbeiten** mithilfe der Anweisungen vom Bereich [Bearbeiten einer eingebetteten App](#editing-an-embedded-power-app) oben in diesem Thema. Vergewissern Sie sich, dass der Bereich Informationen für die eingebettete App anzeigt, den Sie entfernen möchten, und klicken Sie dann auf die Schaltfläche **Löschen**.
- Da eine eingebettete App als Personalisierungsdaten gespeichert wird, werden durch die Entfernung der Personalisierung der Seite auch alle eingebetteten Apps auf dieser Seite entfernt. Beachten Sie, dass die Löschung der Personalisierung dauerhaft ist und nicht rückgängig gemacht werden kann. Um Ihre Personalisierungen auf einer Seite zu entfernen, wählen Sie **Optionen** aus, und klicken Sie dann auf **Dieses Seite personalisieren** und schließlich auf die Schaltfläche **Löschen**. Nachdem Sie Ihrem Browser aktualisiert haben, werden auch alle vorherigen Personalisierungen für diese Seite entfernt. Unter [Personalisieren der Benutzeroberfläche](personalize-user-experience.md) finden Sie weitere Informationen darüber, wie Sie Seiten mithilfe der Personalisierung optimieren können.

## <a name="appendix"></a>Anhang

### <a name="developer-control-over-where-an-app-can-be-embedded"></a>Entwickler steuern, ob eine App eingebettet werden kann

Standardmäßig können Benutzer Apps auf einer beliebigen Seite, entweder unter der Power Apps-Menüschaltfläche oder direkt auf der Seite als Registerkarte, Inforegister, Blatt oder als neuen Abschnitt in einen Arbeitsbereich einbetten. Entwickler können jedoch nach Bedarf diese Funktion konfigurieren, um nur die Einbettung von Apps für bestimmte Seiten zu ermöglichen, indem die folgenden Methoden implementiert werden:

- **isPowerAppsPersonalizationEnabled** – Wenn diese Methode für eine bestimmten Seite „False“ zurückgibt, wird die Power Apps-Menüschaltfläche nicht angezeigt, und Benutzer können dann Apps nirgends auf dieser Seite einbetten, auch nicht als Registerkarte.
- **isPowerAppsTabPersonalizationEnabled** – Wenn diese Methode für eine bestimmten Seite „false“ zurückgibt, ist der Benutzer nicht in der Lage, Apps direkt auf der Seite als Registerkarte, Inforegister oder Panoramaabschnitt einzubetten. Benutzer können trotzdem noch Apps über die Power Apps-Menüschaltfläche einbetten, wenn das Einbetten auf der Seite zulässig ist.

Das folgende Beispiel zeigt eine neue Klasse mit den beiden Methoden an, die erforderlich sind, um zu konfigurieren, wo Apps eingebettet werden kann.

```
[ExtensionOf(classStr(FormRunConfigurationPowerAppsConfiguration))]

public final class ClassTest_Extension
{
    public static boolean isPowerAppPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppPersonalizationEnabled(pageName);
        return result;
    }
    
    public static boolean isPowerAppTabPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppTabPersonalizationEnabled(pageName);
        return result;
    }
}
```
