---
title: Einbetten von PowerApps-Apps
description: In diesem Thema wird beschrieben, wie PowerApps in den Client eingebettet werden, um die Funktionalität des Produkts zu erhöhen.
author: jasongre
manager: AnnBe
ms.date: 09/20/2019
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
ms.openlocfilehash: 37faf2a7a880c384f6f01d06ef5c9f28055d5006
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191177"
---
# <a name="embed-powerapps-apps"></a>Einbetten von PowerApps-Apps

[!include [banner](../includes/banner.md)]

Plattformupdate 14 unterstützt die Integration in Microsoft PowerApps, einen Dienst für Entwickler und nicht technische Benutzer zur Erstellung benutzerdefinierter Geschäfts-Apps für mobile Geräte, Tablets und das Internet, ohne Code zu schreiben. PowerApps, die von Ihnen, Ihrer Organisation oder dem breiteren Ökosystem entwickelt werden, können dann in Finance and Operations-Apps eingebettet werden, um die Funktionalität des Produkts zu erhöhen. Beispielsweise bedingt dies eventuell, dass Sie eine PowerApp installieren, um Finance and Operations-Apps durch die Informationen zu ergänzen, die aus einem anderen System abgerufen werden.

Um weitere Informationen zum Einbetten von PowerApps zu erhalten, sehen Sie sich das kurze Video [Einbetten von PowerApps](https://www.youtube.com/watch?v=x3qyA1bH-NY) an.

## <a name="adding-an-embedded-powerapp-to-a-page"></a>Hinzufügen eines eingebetteten PowerApps zu einer Seite

### <a name="overview"></a>Übersicht

Bevor Sie eine PowerApp in den Client einbetten, müssen Sie zuerst eine PowerApp mit den gewünschten grafischen und/oder den Fähigkeiten suchen oder erstellen. Hier wird nicht der detaillierte Prozess der Erstellung einer PowerApp beschrieben. Das Thema [Einführung in PowerApps](https://docs.microsoft.com/powerapps/getting-started) ist ein guter Ausgangspunkt, wenn Sie noch nicht mit PowerApps vertraut sind.

Wenn Sie soweit sind, eine bestimmte PowerApp einzubetten, können Sie zwischen einer von zwei Methoden des Zugriffs auf die PowerApp auf einer Seite auswählen, je nachdem welche Route für Ihr Szenario besser geeignet ist. Die erste Methode erfolgt über die PowerApps-Schaltfläche, die dem Standardaktivitätsbereich hinzugefügt wurde. PowerApps, die über diesen Mechanismus hinzugefügt werden, werden in der PowerApps-Menüschaltfläche als Menüoptionen angezeigt. Wenn sie ausgewählt sind, öffnet jedes dieser Menüelemente einen Seitenbereich, der die eingebettete PowerApp enthält. Alternativ können Sie wählen, eine PowerApps direkt auf einer Seite als neue Registerkarte, Inforegister, Blatt oder als Bereich anzuzeigen.

Wenn Sie die eingebettete PowerApp konfigurieren, können Sie ein einzelnes Feld auswählen, das Sie als Eingabe an die PowerApp übermitteln wollen. Dies ermöglicht es der PowerApp, basierend auf den aktuell angezeigten Daten zu reagieren.

### <a name="details"></a>Detaildaten

Die folgenden Anweisungen zeigen, wie eine PowerApp in den Webclient eingebettet wird.

1. Gehe Sie zur Seite, in der Sie das PowerApps einbetten möchten. Dies ist die gleiche Seite, die sämtliche Daten enthält, die an die PowerApp als Eingabe zu übergeben ist.
2. Öffnet den Bereich **Hinzufügen eines PowerApps**:

    - Klicken Sie **Optionen** und wählen Sie anschließend **Personalisieren Sie dieses Formular** aus. Unter dem Menü **Einfügen** wählen Sie **PowerApp**. Schließlich wählen Sie die Region aus, in der Sie das PowerApps hinzufügen möchten. Wenn Sie die PowerApp unter der PowerApps-Menüschaltfläche einbetten möchten, wählen Sie den Aktivitätsbereich aus. Wenn Sie das PowerApps direkt auf der Seite einbetten möchten, wählen Sie die entsprechende Registerkarte, das Inforegister, das Etikett oder den Bereich aus (sofern Sie einen Arbeitsbereich sind).
    - Wenn die PowerApp über die PowerApps-Menüschaltfläche aufgerufen wird, können Sie alternativ im Standardaktivitätsbereich auf die Menüschaltfläche **PowerApps** klicken und dann **PowerApp einfügen** auswählen.

3. Konfigurieren Sie das eingebettete PowerApps:

    - Das Feld **Name** gibt den Text an, der für die Schaltfläche oder Registerkarte angezeigt wird, der die eingebettete PowerApp enthält. Oftmals können Sie ggf. den Namen des PowerApps in diesem Feld wiederholen.
    - **App ID** ist der GUID für das PowerApps, das Sie einbetten möchten. Um diesen Wert abzurufen, suchen Sie die PowerApp auf [web.powerapps.com](https://web.powerapps.com), und suchen Sie dann das Feld **App-ID** unter **Details**.
    - Für die **Eingabedaten für das PowerApps** können Sie optional das Feld auswählen, das die Daten enthält, die Sie dem PowerApps weitergegeben werden sollen. Weitere Informationen dazu, wie die PowerApp auf die von Finance and Operations-Apps gesendeten Daten zugreifen kann, finden Sie im Abschnitt [Erstellen einer PowerApp, die Daten aus Finance and Operations-Apps nutzt](#building-a-powerapp-that-leverages-data-sent-from-finance-and-operations-apps) weiter unten in diesem Thema.
    - Wählen Sie die **Anwendungsgröße** die zum Typ der PowerApps passt, die Sie einbetten. Wählen Sie **Dünn** für PowerApps, die für mobile Geräte erstellt wurden, und **Breit** für PowerApps aus, die für Tablets erstellt wurden. Dadurch wird sichergestellt, dass für die eingebettete PowerApp ausreichend Platz zugeteilt wird.
    - Das Inforegister **Juristische Personen** bietet die Möglichkeit, auszuwählen, für welche juristischen Personen die PowerApp verfügbar ist. Standardmäßig wird die PowerApp in allen juristischen Personen angezeigt.

4. Nachdem Sie bestätigt haben, dass die Konfiguration korrekt ist, klicken Sie **Einfügen**, um das PowerApps auf der Seite einzubetten. Sie werden dazu aufgefordert, den Browser zu aktualisieren, um die eingebettete PowerApp anzuzeigen.

## <a name="sharing-an-embedded-powerapp"></a>Freigeben einer eingebetteten PowerApp

Nachdem Sie ein PowerApps auf einer Seite eingebettet und bestätigt haben, dass sie bei jedem Datenenkontext ordnungsgemäß funktioniert, der von der Seite abgeschlossen wurde, sollten Sie dieses eingebetteten PowerApps für andere Benutzer im System freigeben. Dies kann auf zwei unterschiedliche Arten mithilfe der Personalisierungsfunktionen des Produkts ausgeführt werden:

- Das empfohlene Szenario erfolgt über den Systemadministrator, der eine Personalisierung an alle Benutzer oder eine Teilmenge der Benutzer mithilfe von Push übertragen kann.
- Alternativ können Sie Ihre Änderungen exportieren (genannt Personalisierungen), sie an einen oder mehrere Benutzer übermitteln und jeden dieser Benutzer dazu veranlassen, Ihre Änderungen zu importieren. Die Option Verwalten in der Personalisierungssymbolleiste ermöglich es Ihnen, Personalisierungen zu exportieren und importieren.

Unter [Personalisieren der Benutzeroberfläche](personalize-user-experience.md) finden Sie weitere Details zu den Personalisierungsfähigkeiten im Produkt und wie Sie diese verwenden können.

## <a name="building-a-powerapp-that-leverages-data-sent-from-finance-and-operations-apps"></a>Erstellen einer PowerApp, die Daten von Finance and Operations-Apps nutzt

Ein wichtiger Bestandteil für die Erstellung einer PowerApp, die in Finance and Operations-Apps eingebettet wird, ist die Nutzung der Eingabedaten von Finance and Operations-Apps. Innerhalb des PowerApps können auf diese Eingabedaten mithilfe der Variablen des Parameters ("EntityId" ) zugegriffen werden.

In der OnStart-Funktion der PowerApp können Sie die Eingabedaten von Finance and Operations-Apps auf eine Variable wie die folgende festlegen:

```
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-embedded-powerapp"></a>Anzeigen einer eingebetteten PowerApp

Um eine eingebettete PowerApp auf einer Seite in Finance and Operations-Apps anzuzeigen, wechseln Sie einfach zu einer Seite mit einer eingebetteten PowerApp. Denken Sie daran, dass PowerApps auf die PowerApps-Schaltfläche im Standardaktivitätsbereich zugreifen oder direkt auf der Seite als neue Registerkarte, neues Inforegister, neues Blatt oder als neuer Bereich in einem Arbeitsbereich angezeigt werden kann. Wenn ein Benutzer zunächst versucht, eine PowerApp auf einer Seite zu laden, wird er oder sie dazu aufgefordert, sich bei PowerApps anzumelden, um sicherzustellen, dass der Benutzer die entsprechenden Berechtigungen hat, um die PowerApp zu verwenden.

## <a name="editing-an-embedded-powerapp"></a>Anzeigen einer eingebetteten PowerApps

Nachdem ein PowerApps auf einer Seite eingebettet wurde, müssen Sie möglicherweise einige Änderungen der Variante von dieser PowerApps vornehmen. Angenommen, Sie möchten möglicherweise das Etikett ändern, das dem eingebetteten PowerApps zugeordnet ist, oder eine neue Version von einem PowerApps wurde erstellt und Sie müssen die-App Kennung aktualisieren, um die aktuellsten PowerApps zu verweisen.

Gehen Sie folgendermaßen vor, um die Konfiguration von einer eingebetteten PowerApps zu bearbeiten:

1. Gehen Sie zu **PowerApps bearbeiten**.

    - Wenn die eingebettete PowerApp über die PowerApps-Menüschaltfläche aufgerufen wird, klicken Sie mit der rechten Maustaste auf die PowerApps-Menüschaltfläche, und wählen Sie **Personalisieren** aus. Wählen Sie im Dropdownmenü **PowerApp auswählen** die PowerApp aus, die Sie konfigurieren möchten.
    - Wenn die eingebettete PowerApps direkt auf der Seite angezeigt wird, wählen Sie **Optionen** und **Personalisieren Sie dieses Formular** aus. Bei Verwendung des Tools **Auswählen** klicken Sie auf die eingebettete PowerApp.

2. Nehmen Sie die erforderlichen Änderungen an der PowerApps-Konfiguration vor, und klicken Sie anschließend auf **Speichern**.

## <a name="removing-an-embedded-powerapp"></a>Entfernen einer eingebetteten PowerApp

Nachdem eine PowerApps auf einer Seite eingebettet wurde, gibt es zwei Möglichkeiten, sie nach Bedarf zu entfernen:

- Wechseln Sie zum Bereich **Bearbeiten eines PowerApps** mithilfe der Anweisungen vom [Bearbeiten eines eingebetteten PowerApps](#editing-an-embedded-powerapp) Bereich oben in diesem Thema. Vergewissern Sie sich, dass der Bereich Informationen für das eingebettete PowerApps anzeigt, den Sie entfernen möchten, und klicken Sie dann auf die Schaltfläche **Löschen**.
- Da eine eingebettete PowerApp als Personalisierungsdaten gespeichert wird, werden durch die Entfernung der Personalisierung der Seite auch alle eingebetteten PowerApps auf dieser Seite entfernt. Beachten Sie, dass die Löschung der Personalisierung dauerhaft ist und nicht rückgängig gemacht werden kann. Um Ihre Personalisierungen auf einer Seite zu entfernen, wählen Sie **Optionen** aus, und klicken Sie dann auf **Dieses Formular personalisieren**. Unter dem Menü **Verwalten** wählen Sie die Schaltfläche **Löschen** aus. Nachdem Sie Ihrem Browser aktualisiert haben, werden auch alle vorherigen Personalisierungen für diese Seite entfernt. Unter [Personalisierung der Benutzeroberfläche](personalize-user-experience.md) finden Sie weitere Informationen darüber, wie Sie Seiten mithilfe der Personalisierung optimieren können.

## <a name="appendix"></a>Anhang

### <a name="developer-control-over-where-a-powerapp-can-be-embedded"></a>Entwickler steuern, ob eine PowerApps eingebettet werden kann

Standardmäßig können Benutzer PowerApps auf einer beliebigen Seite, entweder unter der PowerApps-Menüschaltfläche oder direkt auf der Seite als Registerkarte, Inforegister, Blatt oder als neuen Abschnitt in einen Arbeitsbereich einbetten. Entwickler können jedoch nach Bedarf diese Funktion konfigurieren, um nur die Einbettung von PowerApps für bestimmte Seiten zu ermöglichen, indem die folgenden Methoden implementiert werden:

- **isPowerAppsPersonalizationEnabled** – Wenn diese Methode für eine bestimmten Seite „False“ zurückgibt, wird die PowerApps-Menüschaltfläche nicht angezeigt, und Benutzer können dann PowerApps nirgends auf dieser Seite einbetten, auch nicht als Registerkarte.
- **isPowerAppsTabPersonalizationEnabled** – Wenn diese Methode für eine bestimmte Seite „False“ zurückgibt, kann der Benutzer PowerApps nicht direkt auf der Seite als Registerkarte, Inforegister oder Panoramaabschnitt einbetten. Benutzer können trotzdem noch PowerApps über die PowerApps-Menüschaltfläche einbetten, wenn das Einbetten auf der Seite zulässig ist.

Das folgende Beispiel zeigt eine neue Klasse mit den beiden Methoden an, die erforderlich sind, um zu konfigurieren, wo PowerApps eingebettet werden kann.

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
