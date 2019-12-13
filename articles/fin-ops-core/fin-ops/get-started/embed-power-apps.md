---
title: Einbetten von Power Apps
description: In diesem Thema wird beschrieben, wie Power Apps in den Client eingebettet werden, um die Funktionalität des Produkts zu erhöhen.
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
ms.openlocfilehash: 755a30f89725ca0a7e1c14252984c617d6ba280e
ms.sourcegitcommit: 4162d9ef4239c9d4e5297b8aaa903dd54f9cafc3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/21/2019
ms.locfileid: "2824492"
---
# <a name="embed-microsoft-power-apps"></a>Einbetten von Microsoft Power Apps

[!include [banner](../includes/banner.md)]

Plattformupdate 14 unterstützt die Integration in Microsoft Power Apps, einen Dienst für Entwickler und nicht technische Benutzer zur Erstellung benutzerdefinierter Geschäfts-Apps für mobile Geräte, Tablets und das Internet, ohne Code zu schreiben. Power Apps, die von Ihnen, Ihrer Organisation oder dem breiteren Ökosystem entwickelt werden, können dann in Finance and Operations-Apps eingebettet werden, um die Funktionalität des Produkts zu erhöhen. Beispielsweise bedingt dies eventuell, dass Sie eine Power-App installieren, um Finance and Operations-Apps durch die Informationen zu ergänzen, die aus einem anderen System abgerufen werden.

Um weitere Informationen zum Einbetten von Power Apps zu erhalten, sehen Sie sich das kurze Video [Einbetten von Power Apps](https://www.youtube.com/watch?v=x3qyA1bH-NY) an.

## <a name="adding-an-embedded-power-app-to-a-page"></a>Hinzufügen einer eingebetteten Power-App zu einer Seite

### <a name="overview"></a>Übersicht

Bevor Sie eine Power-App in den Client einbetten, müssen Sie zuerst eine Power-App mit den gewünschten grafischen und/oder den Fähigkeiten suchen oder erstellen. Hier wird nicht der detaillierte Prozess der Erstellung einer Power-App beschrieben. Das Thema [Einführung in Power Apps](https://docs.microsoft.com/powerapps/getting-started) ist ein guter Ausgangspunkt, wenn Sie noch nicht mit Power Apps vertraut sind.

Wenn Sie soweit sind, eine bestimmte Power-App einzubetten, können Sie zwischen einer von zwei Methoden des Zugriffs auf die Power-App auf einer Seite auswählen, je nachdem, welche Route für Ihr Szenario besser geeignet ist. Die erste Methode erfolgt über die Power Apps-Schaltfläche, die dem Standardaktivitätsbereich hinzugefügt wurde. Power Apps, die über diesen Mechanismus hinzugefügt werden, werden in der Power Apps-Menüschaltfläche als Menüoptionen angezeigt. Wenn sie ausgewählt sind, öffnet jedes dieser Menüelemente einen Seitenbereich, der die eingebettete Power-App enthält. Alternativ können Sie wählen, eine Power-App direkt auf einer Seite als neue Registerkarte, Inforegister, Blatt oder als neuen Bereich in einem Arbeitsbereich anzuzeigen.

Wenn Sie die eingebettete Power-App konfigurieren, können Sie ein einzelnes Feld auswählen, das Sie als Eingabe an die Power-App übermitteln wollen. Dies ermöglicht es der Power-App, basierend auf den aktuell angezeigten Daten zu reagieren.

### <a name="details"></a>Detaildaten

Die folgenden Anweisungen zeigen, wie eine Power-App in den Webclient eingebettet wird.

1. Gehe Sie zur Seite, in der Sie die Power-App einbetten möchten. Dies ist die gleiche Seite, die sämtliche Daten enthält, die an die Power-App als Eingabe zu übergeben ist.
2. Öffnet den Bereich **Hinzufügen einer Power-App**:

    - Klicken Sie **Optionen** und wählen Sie anschließend **Personalisieren Sie dieses Formular** aus. Unter dem Menü **Einfügen** wählen Sie **Power-App** aus. Schließlich wählen Sie die Region aus, in der Sie die Power-App hinzufügen möchten. Wenn Sie die Power-App unter der Power Apps-Menüschaltfläche einbetten möchten, wählen Sie den Aktivitätsbereich aus. Wenn Sie die Power-App direkt auf der Seite einbetten möchten, wählen Sie die entsprechende Registerkarte, das Inforegister, das Etikett oder den Bereich aus (sofern Sie in einem Arbeitsbereich sind).
    - Wenn die Power-App über die Power Apps-Menüschaltfläche aufgerufen wird, können Sie alternativ im Standardaktivitätsbereich auf die Menüschaltfläche **Power Apps** klicken und dann **Power-App einfügen** auswählen.

3. Konfigurieren Sie die eingebettete Power-App:

    - Das Feld **Name** gibt den Text an, der für die Schaltfläche oder Registerkarte angezeigt wird, die die eingebettete Power-App enthält. Oftmals können Sie ggf. den Namen der Power-App in diesem Feld wiederholen.
    - **App-Kennung** ist der GUID für die Power-App, die Sie einbetten möchten. Um diesen Wert abzurufen, suchen Sie die Power-App auf [web.powerapps.com](https://web.powerapps.com), und suchen Sie dann das Feld **App-ID** unter **Details**.
    - Für die **Eingabedaten für Power-App** können Sie optional das Feld auswählen, das die Daten enthält, die an die Power-App weitergegeben werden sollen. Weitere Informationen dazu, wie die Power-App auf die von Finance and Operations-Apps gesendeten Daten zugreifen kann, finden Sie im Abschnitt [Erstellen einer Power-App, die Daten aus Finance and Operations-Apps nutzt](#building-a-powerapp-that-leverages-data-sent-from-finance-and-operations-apps) weiter unten in diesem Thema.
    - Wählen Sie die **Anwendungsgröße** die zum Typ der Power-App passt, die Sie einbetten. Wählen Sie **Dünn** für Power Apps, die für mobile Geräte erstellt wurden, und **Breit** für Power Apps aus, die für Tablets erstellt wurden. Dadurch wird sichergestellt, dass für die eingebettete Power-App ausreichend Platz zugeteilt wird.
    - Das Inforegister **Juristische Personen** bietet die Möglichkeit, auszuwählen, für welche juristischen Personen die Power-App verfügbar ist. Standardmäßig wird die Power-App in allen juristischen Personen angezeigt.

4. Nachdem Sie bestätigt haben, dass die Konfiguration korrekt ist, klicken Sie **Einfügen**, um die Power-App auf der Seite einzubetten. Sie werden dazu aufgefordert, den Browser zu aktualisieren, um die eingebettete Power-App anzuzeigen.

## <a name="sharing-an-embedded-power-app"></a>Freigeben einer eingebetteten Power-App

Nachdem Sie eine Power-App auf einer Seite eingebettet und bestätigt haben, dass sie bei jedem Datenenkontext ordnungsgemäß funktioniert, der von der Seite abgeschlossen wurde, sollten Sie diese eingebettete Power-App für andere Benutzer im System freigeben. Dies kann auf zwei unterschiedliche Arten mithilfe der Personalisierungsfunktionen des Produkts ausgeführt werden:

- Das empfohlene Szenario erfolgt über den Systemadministrator, der eine Personalisierung an alle Benutzer oder eine Teilmenge der Benutzer mithilfe von Push übertragen kann.
- Alternativ können Sie Ihre Änderungen exportieren (genannt Personalisierungen), sie an einen oder mehrere Benutzer übermitteln und jeden dieser Benutzer dazu veranlassen, Ihre Änderungen zu importieren. Die Option Verwalten in der Personalisierungssymbolleiste ermöglich es Ihnen, Personalisierungen zu exportieren und importieren.

Unter [Personalisieren der Benutzeroberfläche](personalize-user-experience.md) finden Sie weitere Details zu den Personalisierungsfähigkeiten im Produkt und wie Sie diese verwenden können.

## <a name="building-a-power-app-that-leverages-data-sent-from-finance-and-operations-apps"></a>Erstellen einer Power-App, die Daten von Finance and Operations-Apps nutzt

Ein wichtiger Bestandteil für die Erstellung einer Power-App, die in Finance and Operations-Apps eingebettet wird, ist die Nutzung der Eingabedaten von Finance and Operations-Apps. Innerhalb der Power-App können auf diese Eingabedaten mithilfe der Variablen des Parameters („EntityId“) zugegriffen werden.

In der OnStart-Funktion der Power-App können Sie die Eingabedaten von Finance and Operations-Apps auf eine Variable wie die folgende festlegen:

```
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-embedded-power-app"></a>Anzeigen einer eingebetteten Power-App

Um eine eingebettete Power-App auf einer Seite in Finance and Operations-Apps anzuzeigen, wechseln Sie einfach zu einer Seite mit einer eingebetteten Power-App. Denken Sie daran, dass Power Apps auf die Power Apps-Schaltfläche im Standardaktivitätsbereich zugreifen oder direkt auf der Seite als neue Registerkarte, neues Inforegister, neues Blatt oder als neuer Bereich in einem Arbeitsbereich angezeigt werden kann. Wenn ein Benutzer zunächst versucht, eine Power-App auf einer Seite zu laden, wird er oder sie dazu aufgefordert, sich bei Power Apps anzumelden, um sicherzustellen, dass der Benutzer die entsprechenden Berechtigungen hat, um die Power-App zu verwenden.

## <a name="editing-an-embedded-power-app"></a>Bearbeiten einer eingebetteten Power-App

Nachdem eine Power-App auf einer Seite eingebettet wurde, müssen Sie möglicherweise einige Änderungen der Konfiguration dieser Power-App vornehmen. Angenommen, Sie möchten möglicherweise das Etikett ändern, das der eingebetteten Power-App zugeordnet ist, oder eine neue Version einer Power-App wurde erstellt und Sie müssen die App-Kennung aktualisieren, um auf die neueste Power-App zu verweisen.

Gehen Sie folgendermaßen vor, um die Konfiguration einer eingebetteten Power-App zu bearbeiten:

1. Gehen Sie zum Bereich **Power-App bearbeiten**.

    - Wenn die eingebettete Power-App über die Power Apps-Menüschaltfläche aufgerufen wird, klicken Sie mit der rechten Maustaste auf die Power Apps-Menüschaltfläche, und wählen Sie **Personalisieren** aus. Wählen Sie im Dropdownmenü **Power-App auswählen** die Power-App aus, die Sie konfigurieren möchten.
    - Wenn die eingebettete Power-App direkt auf der Seite angezeigt wird, wählen Sie **Optionen** und **Dieses Formular personalisieren** aus. Bei Verwendung des Tools **Auswählen** klicken Sie auf die eingebettete Power-App.

2. Nehmen Sie die erforderlichen Änderungen an der Power Apps-Konfiguration vor, und klicken Sie anschließend auf **Speichern**.

## <a name="removing-an-embedded-power-app"></a>Entfernen einer eingebetteten Power-App

Nachdem eine Power-App auf einer Seite eingebettet wurde, gibt es zwei Möglichkeiten, sie nach Bedarf zu entfernen:

- Wechseln Sie zum Bereich **Bearbeiten einer Power-App** mithilfe der Anweisungen vom Bereich [Bearbeiten einer eingebetteten Power-App](#editing-an-embedded-powerapp) oben in diesem Thema. Vergewissern Sie sich, dass der Bereich Informationen für die eingebettete Power-Apps anzeigt, den Sie entfernen möchten, und klicken Sie dann auf die Schaltfläche **Löschen**.
- Da eine eingebettete Power-App als Personalisierungsdaten gespeichert wird, werden durch die Entfernung der Personalisierung der Seite auch alle eingebetteten Power Apps auf dieser Seite entfernt. Beachten Sie, dass die Löschung der Personalisierung dauerhaft ist und nicht rückgängig gemacht werden kann. Um Ihre Personalisierungen auf einer Seite zu entfernen, wählen Sie **Optionen** aus, und klicken Sie dann auf **Dieses Formular personalisieren**. Unter dem Menü **Verwalten** wählen Sie die Schaltfläche **Löschen** aus. Nachdem Sie Ihrem Browser aktualisiert haben, werden auch alle vorherigen Personalisierungen für diese Seite entfernt. Unter [Personalisieren der Benutzeroberfläche](personalize-user-experience.md) finden Sie weitere Informationen darüber, wie Sie Seiten mithilfe der Personalisierung optimieren können.

## <a name="appendix"></a>Anhang

### <a name="developer-control-over-where-a-power-app-can-be-embedded"></a>Entwickler steuern, ob eine Power-App eingebettet werden kann

Standardmäßig können Benutzer Power Apps auf einer beliebigen Seite, entweder unter der Power Apps-Menüschaltfläche oder direkt auf der Seite als Registerkarte, Inforegister, Blatt oder als neuen Abschnitt in einen Arbeitsbereich einbetten. Entwickler können jedoch nach Bedarf diese Funktion konfigurieren, um nur die Einbettung von Power Apps für bestimmte Seiten zu ermöglichen, indem die folgenden Methoden implementiert werden:

- **isPowerAppsPersonalizationEnabled** – Wenn diese Methode für eine bestimmten Seite „False“ zurückgibt, wird die Power Apps-Menüschaltfläche nicht angezeigt, und Benutzer können dann Power Apps nirgends auf dieser Seite einbetten, auch nicht als Registerkarte.
- **isPowerAppsTabPersonalizationEnabled** – Wenn diese Methode für eine bestimmte Seite „False“ zurückgibt, kann der Benutzer Power Apps nicht direkt auf der Seite als Registerkarte, Inforegister oder Panoramaabschnitt einbetten. Benutzer können trotzdem noch Power Apps über die Power Apps-Menüschaltfläche einbetten, wenn das Einbetten auf der Seite zulässig ist.

Das folgende Beispiel zeigt eine neue Klasse mit den beiden Methoden an, die erforderlich sind, um zu konfigurieren, wo Power Apps eingebettet werden kann.

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
