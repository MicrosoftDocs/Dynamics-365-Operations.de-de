---
title: PowerApps-Apps einbetten
description: In diesem Thema wird beschrieben, wie PowerApps in den Finance and Operations-Client eingebettet werden, um die Funktionalität des Produkts zu erhöhen.
author: jasongre
manager: AnnBe
ms.date: 08/15/2019
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
ms.openlocfilehash: ed189a13574b3d6b486d98404722a5322ce1b7a7
ms.sourcegitcommit: e552111e148a80544a3468da60ea0464f02a658d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2019
ms.locfileid: "1875295"
---
# <a name="embed-powerapps-apps"></a>Einbetten von PowerApps-Apps

[!include [banner](../includes/banner.md)]

Im Plattformupdate 14 unterstützt Microsoft Dynamics 365 for Finance and Operations die Integration mit Microsoft PowerApps, einen Dienst für Entwickler und nicht technische Benutzer zur Erstellung benutzerdefinierter Geschäfts-Apps für mobile Geräte, Tablets und das Internet, ohne Code zu schreiben. PowerApps von Ihnen, Ihrer Organisation oder dem breiteren Ökosystem entwickelt, kann im Finance and Operations Client die Produktfunktionalität erweitern. Beispielsweise bedingt dies eventuell, dass Sie ein PowerApps installieren, um Finance and Operations mit den Informationen zu ergänzen, die aus einem anderen System abgerufen werden.

Um weitere Informationen zur Einbettung von PowerApps zu erhalten, sehen Sie sich das Kurzvideo [Vorgehensweise beim Einbetten von PowerApps in Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=x3qyA1bH-NY) an.

## <a name="adding-an-embedded-powerapp-to-a-page"></a>Hinzufügen eines eingebetteten PowerApps zu einer Seite

### <a name="overview"></a>Übersicht

Bevor Sie ein PowerApps in den Finance and Operations Client einbetten, müssen Sie zuerst ein PowerApps mit den gewünschten grafischen und/oder den Fähigkeiten suchen oder erstellen. Hier wird nicht der detaillierte Prozess der Erstellung einer PowerApp beschrieben. Das Thema [Einführung in PowerApps](https://docs.microsoft.com/powerapps/getting-started) ist ein guter Startpunkt, wenn Sie neu bei PowerApps sind.

Wenn Sie soweit sind, eine bestimmte PowerApp einzubetten, können Sie zwischen einer von zwei Methoden des Zugriffs auf die PowerApp auf einer Seite auswählen, je nachdem welche Route für Ihr Szenario besser geeignet ist. Die erste Methode erfolgt über die PowerApps-Schaltfläche, die dem Standardaktivitätsbereich hinzugefügt wurde. PowerApps, die während diesem Mechanismus hinzugefügt werden, erscheinen als Elemente in der PowerApps-Menüschaltfläche. Wenn sie ausgewählt sind, öffnet jedes dieser Menüelemente einen Seitenbereich, der die eingebettete PowerApp enthält. Alternativ können Sie wählen, eine PowerApps direkt auf einer Seite als neue Registerkarte, Inforegister, Blatt oder als Bereich anzuzeigen.

Wenn Sie Ihre eingebettete PowerApp in Finance and Operations konfigurieren, können Sie ein einzelnes Feld auswählen, das Sie als Eingabe an die PowerApp übermitteln wollen. Dies ermöglicht es der PowerApp, basierend auf den Daten, die Sie aktuell in Finance and Operations anzeigen, zu reagieren.

### <a name="details"></a>Details

Die folgenden Anweisungen zeigen, wie eine PowerApp in den Finance and Operations-Webclient eingebettet wird.

1. Gehe Sie zur Seite, in der Sie das PowerApps einbetten möchten. Dies ist die gleiche Seite, die sämtliche Daten enthält, die an die PowerApp als Eingabe zu übergeben ist.
2. Öffnet den Bereich **Hinzufügen eines PowerApps**:

    - Klicken Sie **Optionen** und wählen Sie anschließend **Personalisieren Sie dieses Formular** aus. Unter dem Menü **Einfügen** wählen Sie **PowerApp**. Schließlich wählen Sie die Region aus, in der Sie das PowerApps hinzufügen möchten. Wenn Sie das PowerApps unter der PowerApps-Menüschaltfläche einbetten möchten, wählen Sie Aktivitätsbereich aus. Wenn Sie das PowerApps direkt auf der Seite einbetten möchten, wählen Sie die entsprechende Registerkarte, das Inforegister, das Etikett oder den Bereich aus (sofern Sie einen Arbeitsbereich sind).
    - Wenn auf die PowerApps mithilfe der PowerApps-Menüschaltfläche zugegriffen wird, können Sie auf die im Standardaktivitätsbereich alternativ Menüschaltfläche **PowerApps** klicken und dann **Hinzufügen einer PowerApps** auswählen.

3. Konfigurieren Sie das eingebettete PowerApps:

    - Das Feld **Name** gibt den Text an, der für die Schaltfläche oder Registerkarte angezeigt wird, der die eingebettete PowerApp enthält. Oftmals können Sie ggf. den Namen des PowerApps in diesem Feld wiederholen.
    - **App ID** ist der GUID für das PowerApps, das Sie einbetten möchten. Um diesen Wert abzurufen, suchen Sie die PowerApp auf [web.powerapps.com](https://web.powerapps.com), und suchen Sie dann das Feld **App-ID** unter **Details**.
    - Für die **Eingabedaten für das PowerApps** können Sie optional das Feld auswählen, das die Daten enthält, die Sie dem PowerApps weitergegeben werden sollen. Im Abschnitt später in diesem Thema mit dem Titel [Erstellen einer PowerApp, die Daten aus Finance and Operations nutzt](#building-a-powerapp-that-leverages-data-sent-from-finance-and-operations) finden Sie Details darüber, wie die PowerApp auf die Daten zugreifen kann, die von Finance and Operations übermittelt werden.
    - Wählen Sie die **Anwendungsgröße** die zum Typ der PowerApps passt, die Sie einbetten. Wählen Sie **Schmal** für PowerApps aus, die für mobile Geräte erstellt wurden, und **Breit** für PowerApps aus, die für Tablets erstellt wurden. Dadurch wird sichergestellt, dass für die eingebettete PowerApp ausreichend Platz zugeteilt wird.
    - Das Inforegister **Juristische Personen** bietet die Möglichkeit, auszuwählen, für welche juristischen Personen die PowerApp verfügbar ist. Standardmäßig wird die PowerApp in allen juristischen Personen angezeigt.

4. Nachdem Sie bestätigt haben, dass die Konfiguration korrekt ist, klicken Sie **Einfügen**, um das PowerApps auf der Seite einzubetten. Sie werden dazu aufgefordert, den Browser zu aktualisieren, um die eingebettete PowerApp anzuzeigen.

## <a name="sharing-an-embedded-powerapp"></a>Freigeben einer eingebetteten PowerApp

Nachdem Sie ein PowerApps auf einer Seite eingebettet und bestätigt haben, dass sie bei jedem Datenenkontext ordnungsgemäß funktioniert, der von der Seite abgeschlossen wurde, sollten Sie dieses eingebetteten PowerApps für andere Benutzer im System freigeben. Dies kann auf zwei unterschiedliche Arten mithilfe der Personalisierungsfunktionen des Produkts ausgeführt werden:

- Das empfohlene Szenario erfolgt über den Systemadministrator, der eine Personalisierung an alle Benutzer oder eine Teilmenge der Benutzer mithilfe von Push übertragen kann.
- Alternativ können Sie Ihre Änderungen exportieren (genannt Personalisierungen), sie an einen oder mehrere Benutzer übermitteln und jeden dieser Benutzer dazu veranlassen, Ihre Änderungen zu importieren. Die Option Verwalten in der Personalisierungssymbolleiste ermöglich es Ihnen, Personalisierungen zu exportieren und importieren.

Unter [Personalisieren der Benutzeroberfläche](personalize-user-experience.md) finden Sie weitere Details zu den Personalisierungsfähigkeiten im Produkt und wie Sie diese verwenden können.

## <a name="building-a-powerapp-that-leverages-data-sent-from-finance-and-operations"></a>Das Erstellen einer PowerApps, die Daten von Finance and Operations nutzt.

Ein wichtiger Bestandteil für die Erstellung einer PowerApps, die in Finance and Operations eingebettet ist, verwendet die Eingabedaten von Finance and Operations. Innerhalb des PowerApps können auf diese Eingabedaten mithilfe der Variablen des Parameters ("EntityId" ) zugegriffen werden.

In der OnStart-Funktion des PowerApps, können Sie die Eingabedaten von Finance and Operations auf eine Variable so festlegen:

```
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-embedded-powerapp"></a>Anzeigen einer eingebetteten PowerApp

Um eine eingebettete PowerApp auf einer Seite in Finance and Operations anzuzeigen, wechseln Sie einfach zu einer Seite mit einer eingebetteten PowerApp. Erinnert, dass PowerApps auf die PowerApps-Schaltfläche im Standardaktivitätsbereich zugreifen kann oder direkt auf der Seite als neue Inforegister Blatt Registerkarte, oder als neuer Bereich in einen Arbeitsbereich angezeigt werden kann. Wenn ein Benutzer zunächst versucht, eine PowerApp auf einer Seite zu laden, wird er oder sie dazu aufgefordert, sich bei PowerApps anzumelden, um sicherzustellen, dass der Benutzer die entsprechenden Berechtigungen hat, um die PowerApp zu verwenden.

## <a name="editing-an-embedded-powerapp"></a>Anzeigen einer eingebetteten PowerApps

Nachdem ein PowerApps auf einer Seite eingebettet wurde, müssen Sie möglicherweise einige Änderungen der Variante von dieser PowerApps vornehmen. Angenommen, Sie möchten möglicherweise das Etikett ändern, das dem eingebetteten PowerApps zugeordnet ist, oder eine neue Version von einem PowerApps wurde erstellt und Sie müssen die-App Kennung aktualisieren, um die aktuellsten PowerApps zu verweisen.

Gehen Sie folgendermaßen vor, um die Konfiguration von einer eingebetteten PowerApps zu bearbeiten:

1. Gehen Sie zu **PowerApps bearbeiten**.

    - Wenn die eingebettete PowerApps durch die PowerApps-Menüschaltfläche zugegriffen wird, klicken Sie auf der PowerApps-Menüschaltfläche mit der rechten Maustaste und wählen Sie **Anpassen** aus. Wählen Sie im Dropdownmenü **PowerApp auswählen** die PowerApp aus, die Sie konfigurieren möchten.
    - Wenn die eingebettete PowerApps direkt auf der Seite angezeigt wird, wählen Sie **Optionen** und **Personalisieren Sie dieses Formular** aus. Bei Verwendung des Tools **Auswählen** klicken Sie auf die eingebettete PowerApp.

2. Nehmen Sie die erforderlichen Änderungen an den Informationen zur Anfrage vor, und klicken Sie anschließend auf **Speichern und schließen**.

## <a name="removing-an-embedded-powerapp"></a>Entfernen einer eingebetteten PowerApp

Nachdem eine PowerApps auf einer Seite eingebettet wurde, gibt es zwei Möglichkeiten, sie nach Bedarf zu entfernen:

- Wechseln Sie zum Bereich **Bearbeiten eines PowerApps** mithilfe der Anweisungen vom [Bearbeiten eines eingebetteten PowerApps](#editing-an-embedded-powerapp) Bereich oben in diesem Thema. Vergewissern Sie sich, dass der Bereich Informationen für das eingebettete PowerApps anzeigt, den Sie entfernen möchten, und klicken Sie dann auf die Schaltfläche **Löschen**.
- Da eine eingebettete PowerApps als Personalisierungsdaten gespeichert ist, wird durch die Entfernung der Personalisierung der Seite auch jede eingebettete PowerApps auf dieser Seite entfernt. Beachten Sie, dass die Löschung der Personalisierung dauerhaft ist und nicht rückgängig gemacht werden kann. Um Ihre Personalisierungen auf einer Seite zu entfernen, wählen Sie **Optionen** aus, und klicken Sie dann auf **Dieses Formular personalisieren**. Unter dem Menü **Verwalten** wählen Sie die Schaltfläche **Löschen** aus. Nachdem Sie Ihrem Browser aktualisiert haben, werden auch alle vorherigen Personalisierungen für diese Seite entfernt. Unter [Personalisierung der Benutzeroberfläche](personalize-user-experience.md) finden Sie weitere Informationen darüber, wie Sie Seiten mithilfe der Personalisierung optimieren können.

## <a name="appendix"></a>Anhang

### <a name="developer-control-over-where-a-powerapp-can-be-embedded"></a>Entwickler steuern, ob eine PowerApps eingebettet werden kann

Standardmäßig können Benutzer PowerApps auf einer beliebigen Seite, entweder unter der PowerApps-Menüschaltfläche oder direkt auf der Seite als Registerkarte, Inforegister, Blatt oder als neuer Abschnitt in einem Arbeitsbereich einbetten. Entwickler können jedoch nach Bedarf diese Funktion konfigurieren, um nur die Einbettung von PowerAppss für bestimmte Seiten zu ermöglichen, indem die folgenden Methoden implementiert werden:

- **isPowerAppsPersonalizationEnabled** -, Wenn diese Methode für eine bestimmten Seite False zurückgibt, dann wird die PowerApps-Menüschaltfläche nicht angezeigt, und Benutzer können dann PowerApps nirgends auf dieser Seite einbetten, auch nicht als Registerkarte.
- **isPowerAppsTabPersonalizationEnabled** - Wenn diese Methode nicht erfüllt für eine bestimmten Seite zurückgibt, ist der Benutzer nicht in der Lage, PowerApps direkt auf der Seite als Registerkarte, Panoramaabschnitt oder Inforegister einzubetten. Benutzer können trotzdem noch PowerApps über die PowerApps-Menüschaltfläche einbetten, wenn das Einbetten auf der Seite zulässig ist.

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
