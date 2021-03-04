---
title: Einbetten von Canvas-Apps aus Power Apps
description: In diesem Thema wird erläutert, wie Canvas-Apps aus Microsoft Power Apps in den Client eingebettet werden, um die Funktionalität des Produkts zu erhöhen.
author: jasongre
manager: AnnBe
ms.date: 11/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: ba3b736aeae8540349309ddd82bd431720b9701c
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693482"
---
# <a name="embed-canvas-apps-from-power-apps"></a>Einbetten von Canvas-Apps aus Power Apps

[!include [banner](../includes/banner.md)]

Microsoft Power Apps ist ein Dienst, mit dem Entwickler und nicht technische Benutzer benutzerdefinierte Geschäftsanwendungen für Mobilgeräte, Tablets und das Web erstellen können, ohne Code schreiben zu müssen. Finance and Operations-Anwendungen unterstützen die Integration in Power Apps. Canvas-Apps, die Sie, Ihre Organisation oder das breitere Ökosystem entwickeln, können dann in Finance and Operations-Apps eingebettet werden, um die Funktionalität des Produkts zu erhöhen. Wenn Sie beispielsweise eine Canvas-App über Power Apps erstellen, die eine Finance and Operations-App mit Informationen ergänzen soll, die aus einem anderen System abgerufen werden.

Um weitere Informationen zum Einbetten von Power Apps zu erhalten, sehen Sie sich das kurze Video [Einbetten von Power Apps](https://www.youtube.com/watch?v=x3qyA1bH-NY) an.

## <a name="adding-an-embedded-canvas-app-from-power-apps-to-a-page"></a>Hinzufügen einer eingebetteten Canvas-App zu einer Seite über Power Apps

### <a name="overview"></a>Übersicht

Bevor Sie eine Canvas-App aus Power Apps in den Client einbetten, müssen Sie eine App mit den gewünschten Grafiken und/oder Funktionen suchen oder erstellen. Dieses Thema enthält keine detaillierte Beschreibung des Prozesses zum Erstellen von Apps. Wenn Sie noch nie mit Power Apps gearbeitet haben, lesen Sie die [Power Apps-Dokumentation](https://docs.microsoft.com/powerapps/).

Es gibt zwei Möglichkeiten, um auf eine bestimmte Canvas-App auf einer Seite zuzugreifen, wenn Sie bereit sind, die App einzubetten. Sie können wählen, welcher Ansatz besser zu Ihrem Szenario passt. Der erste Ansatz verwendet die Schaltfläche **Power Apps**, die dem Standardaktivitätsbereich hinzugefügt wurde. Apps, die Sie mithilfe dieses Ansatzes hinzufügen, werden als Elemente auf Menütaste **Power Apps** angezeigt. Wenn Sie eines dieser Elemente auswählen, wird ein Seitenbereich angezeigt, der die eingebettete App enthält. Alternativ können Sie eine App direkt auf einer Seite als neue Registerkarte, als Inforegister, als Blatt oder als neuen Bereich in einen Arbeitsbereich einbetten.

Wenn Sie die eingebettete Canvas-App konfigurieren, können Sie ein einzelnes Feld auswählen, das Sie als Kontext an die App übermitteln wollen. Dieser Schritt ermöglicht es der App, basierend auf den aktuell angezeigten Daten zu reagieren.

> [!NOTE]
> Sie können diesen Mechanismus derzeit nicht zum Einbetten modellierter Apps verwenden.  

### <a name="details"></a>Detaildaten

Die folgende Prozedur zeigt, wie eine Canvas-App über Power Apps in den Webclient eingebettet wird.

1. Rufen Sie die Seite auf, in die Sie die Canvas-App einbetten möchten. Hierbei handelt es sich um die Seite, die sämtliche Daten enthält, die an die App als Eingabe werden müssen.
2. Öffnen Sie das Feld **Eine App aus Power Apps hinzufügen**:

    - Klicken Sie **Optionen** und wählen Sie anschließend **Diese Seite personalisieren** aus. Wählen Sie im Menü **Einfügen** **Power Apps**. Schließlich wählen Sie die Region aus, in der Sie die App hinzufügen möchten. Wenn Sie die App unter der Power Apps-Menüschaltfläche einbetten möchten, wählen Sie den Aktivitätsbereich aus. Wenn Sie die App direkt auf der Seite einbetten möchten, wählen Sie die entsprechende Registerkarte, das Inforegister, das Etikett oder den Bereich aus (sofern Sie in einem Arbeitsbereich sind).
    - Wenn die App über die Power Apps-Menüschaltfläche aufgerufen wird, können Sie alternativ im Standardaktivitätsbereich auf die Menüschaltfläche **Power Apps** klicken und dann **Eine App hinzufügen** auswählen.

3. Die eingebettete App konfigurieren:

    - Das Feld **Name** gibt den Text an, der für die Schaltfläche oder Registerkarte angezeigt wird, der die eingebettete App enthält. Oftmals können Sie ggf. den Namen der App in diesem Feld wiederholen.
    - Das Feld **App-ID** gibt den Globally Unique Identifier (GUID) für die Canvas-App an, die Sie einbetten möchten. Um diesen Wert abzurufen, suchen Sie die App auf [make.powerapps.com](https://make.powerapps.com) und entnehmen Sie den Wert dem Feld **App-ID** unter **Details**.
    - Für die **Eingabekontext für die App** können Sie optional das Feld auswählen, das die Daten enthält, die an die App weitergegeben werden sollen. Siehe den Abschnitt weiter unten in diesem Thema mit dem Titel [Erstellung einer Anwendung, die von Finance and Operations Anwendungen](#building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps) gesendete Daten nutzt, für Einzelheiten darüber, wie die Anwendung auf die von Finance and Operations Anwendungen gesendeten Daten zugreifen kann.
    - Wählen Sie die **Anwendungsgröße** die zum Typ der App passt, die Sie einbetten. Wählen Sie **Schmal** für Apps aus, die für mobile Geräte erstellt wurden, und **Breit** für Apps aus, die für Tablets erstellt wurden. Dadurch wird sichergestellt, dass für die eingebettete App ausreichend Platz zugeteilt wird.
    - Das Inforegister **Juristische Personen** bietet die Möglichkeit, auszuwählen, für welche juristischen Personen die App verfügbar ist. Standardmäßig wird die App in allen juristischen Personen verfügbar gemacht. Diese Option ist nur verfügbar, wenn die Funktion [Gespeicherte Ansichten](saved-views.md) deaktiviert ist. 

4. Nachdem Sie bestätigt haben, dass die Konfiguration korrekt ist, klicken Sie **Einfügen**, um die Power-App auf der Seite einzubetten. Sie werden dazu aufgefordert, den Browser zu aktualisieren, um die eingebettete App anzuzeigen.

## <a name="sharing-an-embedded-app"></a>Freigeben einer eingebetteten App

Nachdem Sie eine Canvas-App auf einer Seite eingebettet und bestätigt haben, dass sie mit jedem Datenkontext, der von dieser Seite weitergegeben wird, ordnungsgemäß funktioniert, können Sie die App mit anderen Benutzern im System teilen. Führen Sie die folgenden Schritte aus, um eine eingebettete Canvas-App zu teilen.

1. [Teilen Sie die Canvas-App](https://docs.microsoft.com/powerapps/maker/canvas-apps/share-app) mit den entsprechenden Benutzern, damit sie in Power Apps auf die App zugreifen können. 

2. Stellen Sie sicher, dass die Zielbenutzer über die entsprechenden Personalisierungen verfügen, damit die eingebettete App angezeigt wird, wenn diese Benutzer die Seite anzeigen. Sie können einen der folgenden Ansätze verwenden:

    - Empfohlen: Verwenden Sie die Funktion [Gespeicherte Ansichten](saved-views.md) zum Erstellen und Veröffentlichen einer Ansicht, die die eingebettete App enthält. Dieser Ansatz stellt sicher, dass alle Benutzer mit den Sicherheitsrollen, auf die die veröffentlichte Ansicht abzielt, die App in den Finance and Operations-Apps sehen können. 
    - Wenn Sie die Funktion „Gespeicherte Ansichten“ nicht aktiviert haben, kann der Systemadministrator eine Personalisierung, die die eingebettete App enthält, an alle Benutzer oder eine Gruppe von Benutzern senden. Alternativ können Sie die Personalisierungen Ihrer Seite exportieren und an einen oder mehrere Benutzer senden. Jeder dieser Benutzer kann die Personalisierungen dann importieren. Die Personalisierungssymbolleiste verfügt über Aktionen, mit denen Sie Personalisierungen exportieren und importieren können. 
    
> [!NOTE]
> Wenn die Canvas-App mit externen Benutzern geteilt wurde, können diese Benutzer die darin eingebettete App nicht in den Finance and Operations-Apps verwenden. Sie können jedoch direkt in Power Apps auf die App zugreifen. Zu den externen Benutzern gehören Gäste und Benutzer, die nicht zum Microsoft 365 Azure-Verzeichnis gehören, in dem die Finance and Operations-App bereitgestellt wird.

Unter [Personalisieren der Benutzeroberfläche](personalize-user-experience.md) finden Sie weitere Details zu den Personalisierungsfähigkeiten im Produkt und wie Sie diese verwenden können.

## <a name="building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps"></a>Erstellen einer Canvas-App, die von Finance and Operations-Apps gesendete Daten verwendet

Wenn Sie eine Canvas-App erstellen, die in eine Finance and Operations-App eingebettet wird, müssen Sie unbedingt die Eingabedaten aus dieser Finance and Operations-App verwenden. Über die Power Apps-Entwicklung kann auf die Eingabedaten, die von einer Finance and Operations-App weitergegeben werden, mit der Variable **Param("EntityId")** zugegriffen werden.

In der OnStart-Funktion der App können Sie die Eingabedaten von Finance and Operations-Apps auf eine Variable wie die folgende festlegen:

```powerapps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-a-canvas-app"></a>Anzeigen einer Canvas-App

Um eine eingebettete Canvas-App auf einer Seite in den Finance and Operations-Apps anzuzeigen, wechseln Sie einfach zu einer Seite mit einer eingebetteten App. Denken Sie daran, dass Sie über die Schaltfläche **Power Apps** im Standardaktivitätsbereich auf Apps zugreifen können. Alternativ können Sie als neue Registerkarte, als Inforegister, als Blatt oder als neuer Bereich in einem Arbeitsbereich direkt auf der Seite angezeigt werden. Wenn Benutzer zum ersten Mal versuchen, eine App auf einer Seite zu laden, werden sie aufgefordert, sich anzumelden. Dieser Schritt stellt sicher, dass die Benutzer über die entsprechenden Berechtigungen zur Verwendung der App verfügen.

## <a name="editing-an-embedded-app"></a>Bearbeiten einer eingebetteten App

Nachdem eine Apps auf einer Seite eingebettet wurde, müssen Sie möglicherweise einige Änderungen der Variante von der App vornehmen. Angenommen, Sie möchten möglicherweise das Etikett ändern, das der eingebetteten App zugeordnet ist, oder eine neue Version der App wurde erstellt und Sie müssen die-App Kennung aktualisieren, um auf die aktuellste Version zu verweisen.

Gehen Sie folgendermaßen vor, um die Konfiguration von einer eingebetteten App zu bearbeiten:

1. Gehen Sie zum Bereich **App bearbeiten**.

    - Wenn die eingebettete App über die Power Apps-Menüschaltfläche aufgerufen wird, klicken Sie mit der rechten Maustaste auf die Power Apps-Menüschaltfläche, und wählen Sie **Personalisieren** aus. Wählen Sie im Dropdownmenü **App auswählen** die App aus, die Sie konfigurieren möchten.
    - Wenn die eingebettete App direkt auf der Seite angezeigt wird, wählen Sie **Optionen** und dann **Diese Seite personalisieren** aus. Bei Verwendung des Tools **Auswählen** klicken Sie auf die eingebettete App.

2. Nehmen Sie die erforderlichen Änderungen an der Appkonfiguration vor, und klicken Sie anschließend auf **Speichern**.

## <a name="removing-an-app"></a>App entfernen

Nachdem eine App auf einer Seite eingebettet wurde, gibt es zwei Möglichkeiten, sie nach Bedarf zu entfernen:

- Wechseln Sie zum Bereich **Eine App bearbeiten** mithilfe der Anweisungen vom Bereich [Bearbeiten einer eingebetteten App](#editing-an-embedded-app) oben in diesem Thema. Vergewissern Sie sich, dass der Bereich Informationen für die eingebettete App anzeigt, den Sie entfernen möchten, und klicken Sie dann auf die Schaltfläche **Löschen**.
- Da eine eingebettete App als Personalisierungsdaten gespeichert wird, werden durch die Entfernung der Personalisierung der Seite auch alle eingebetteten Apps auf dieser Seite entfernt. Beachten Sie, dass die Löschung der Personalisierung dauerhaft ist und nicht rückgängig gemacht werden kann. Um Ihre Personalisierungen auf einer Seite zu entfernen, wählen Sie **Optionen** aus, und klicken Sie dann auf **Dieses Seite personalisieren** und schließlich auf die Schaltfläche **Löschen**. Nachdem Sie Ihrem Browser aktualisiert haben, werden auch alle vorherigen Personalisierungen für diese Seite entfernt. Unter [Personalisieren der Benutzeroberfläche](personalize-user-experience.md) finden Sie weitere Informationen darüber, wie Sie Seiten mithilfe der Personalisierung optimieren können.

## <a name="appendix"></a>Anhang

### <a name="developer-specifying-where-an-app-can-be-embedded"></a>[Developer] Festlegen, wo eine App eingebettet werden kann

Standardmäßig können Benutzer Apps auf einer beliebigen Seite, entweder unter der Power Apps-Menüschaltfläche oder direkt auf der Seite als Registerkarte, Inforegister, Blatt oder als neuen Abschnitt in einen Arbeitsbereich einbetten. Entwickler können jedoch nach Bedarf diese Funktion konfigurieren, um nur die Einbettung von Apps für bestimmte Seiten zu ermöglichen, indem die folgenden Methoden implementiert werden:

- **isPowerAppsPersonalizationEnabled** – Wenn diese Methode für eine bestimmten Seite „False“ zurückgibt, wird die Power Apps-Menüschaltfläche nicht angezeigt, und Benutzer können dann Apps nirgends auf dieser Seite einbetten, auch nicht als Registerkarte.
- **isPowerAppsTabPersonalizationEnabled** – Wenn diese Methode für eine bestimmten Seite „false“ zurückgibt, ist der Benutzer nicht in der Lage, Apps direkt auf der Seite als Registerkarte, Inforegister oder Panoramaabschnitt einzubetten. Benutzer können trotzdem noch Apps über die Power Apps-Menüschaltfläche einbetten, wenn das Einbetten auf der Seite zulässig ist.

Das folgende Beispiel zeigt eine neue Klasse mit den beiden Methoden an, die erforderlich sind, um zu konfigurieren, wo Apps eingebettet werden kann.

```powerapps
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]