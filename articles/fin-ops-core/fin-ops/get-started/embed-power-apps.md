---
title: Einbetten von Canvas-Apps aus Power Apps
description: In diesem Thema wird erläutert, wie Canvas-Apps aus Microsoft Power Apps in den Client eingebettet werden, um die Funktionalität des Produkts zu erhöhen.
author: jasongre
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: c2f7b660d364be6e62d484e67908201027190a8a
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065100"
---
# <a name="embed-canvas-apps-from-power-apps"></a>Einbetten von Canvas-Apps aus Power Apps

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Microsoft Power Apps ist ein Dienst, mit dem Entwickler und nicht technische Benutzer benutzerdefinierte Geschäftsanwendungen für Mobilgeräte, Tablets und das Web erstellen können, ohne Code schreiben zu müssen. Apps für Finanzen und Betrieb unterstützen die Integration mit Power Apps. Canvas Apps, die Sie, Ihr Unternehmen oder das breitere Ökosystem entwickeln, können in Apps für Finanzen und Betrieb eingebettet werden, um die Funktionalität des Produkts zu erweitern. Sie könnten zum Beispiel eine Canvas App von Power Apps erstellen, um eine Finance und Operations App mit Informationen zu ergänzen, die aus einem anderen System abgerufen werden.

Um mehr über das Einbetten von Canvas Apps zu erfahren, sehen Sie sich das kurze Video [Wie man Canvas Apps einbettet](https://www.youtube.com/watch?v=x3qyA1bH-NY) an.

## <a name="adding-an-embedded-canvas-app-from-power-apps-to-a-page"></a>Hinzufügen einer eingebetteten Canvas-App zu einer Seite über Power Apps

Bevor Sie eine Canvas-App aus Power Apps in den Client einbetten, müssen Sie eine App mit den gewünschten Grafiken und/oder Funktionen suchen oder erstellen. Dieses Thema enthält keine detaillierte Beschreibung des Prozesses zum Erstellen von Apps. Wenn Sie noch nie mit Power Apps gearbeitet haben, lesen Sie die [Power Apps-Dokumentation](/powerapps/).

Es gibt drei Möglichkeiten, eine Canvas App in eine Finance und Operations App einzubinden. Sie können den Ansatz verwenden, der am besten zu Ihrem Szenario passt. 

- Betten Sie die Canvas App in die **Power Apps**-Schaltfläche im Standard-Aktionsbereich einer Seite ein. Apps, die Sie auf diese Weise hinzufügen, erscheinen als Elemente auf der Schaltfläche **Power Apps** des Menüs, und die Apps werden in Seitenfenstern geöffnet. 
- Betten Sie die Canvas App direkt auf einer bestehenden Seite als neue Registerkarte ein (Pivot-Registerkarte, Inforegister, Blade oder Arbeitsbereich).
- Erstellen Sie eine neue ganzseitige Erfahrung für die Canvas App vom Dashboard aus.

Wenn Sie die eingebettete Canvas-App konfigurieren, können Sie ein einzelnes Feld auswählen, das Sie als Kontext an die App übermitteln wollen. Dieser Schritt ermöglicht es der App, basierend auf den aktuell angezeigten Daten zu reagieren.

> [!NOTE]
> Sie können diesen Mechanismus nicht verwenden, um modellbasierte Apps einzubetten.

### <a name="embedding-a-canvas-app-on-an-existing-page"></a>Einbetten einer Canvas App auf einer bestehenden Seite

Das folgende Verfahren zeigt, wie Sie eine Canvas App auf einer bestehenden Seite aus Power Apps einbetten.

1. Rufen Sie die Seite auf, in die Sie die Canvas-App einbetten möchten. Diese Seite wird alle Daten enthalten, die als Eingabe an die App übergeben werden müssen.
2. Öffnen Sie das Feld **Eine App aus Power Apps hinzufügen**:

    - Wenn die App direkt auf der Seite eingebettet werden soll, wählen Sie **Optionen** \> **Personalisieren Sie diese Seite** \> **Mehr**, und folgen Sie dann einem der folgenden Schritte:

        - Wenn die Funktion **Ganzseitige Apps** eingeschaltet ist, wählen Sie **Seite hinzufügen** und dann den Bereich, in dem Sie die App hinzufügen möchten. Um die App in die **Power Apps** Menüschaltfläche einzubetten, wählen Sie den Aktionsbereich. Um die App direkt auf der Seite einzubetten, wählen Sie die entsprechende Registerkarte, das Inforegister, das Blatt oder den Bereich (wenn Sie sich in einem Arbeitsbereich befinden). Wählen Sie dann im Bereich **Eine App hinzufügen** die Option **Power Apps**.
        - Wenn die Funktion **Ganzseitige Apps** ausgeschaltet ist, wählen Sie **Eine App hinzufügen aus Power Apps** und wählen dann den Bereich, in dem Sie die App hinzufügen wollen. Um die App in die **Power Apps** Menüschaltfläche einzubetten, wählen Sie den Aktionsbereich. Um die App direkt auf der Seite einzubetten, wählen Sie die entsprechende Registerkarte, das Inforegister, das Blatt oder den Bereich (wenn Sie sich in einem Arbeitsbereich befinden).

    - Wenn der Zugriff auf die App über die Menüschaltfläche **Power Apps** erfolgt, können Sie die Menüschaltfläche **Power Apps** im Standard-Aktionsbereich wählen und dann **Eine App hinzufügen**.

3. Konfigurieren Sie die eingebettete App. Weitere Informationen finden Sie im Abschnitt [Konfigurieren einer Canvas App](#configuring-a-canvas-app) weiter unten in diesem Thema.
4. Nachdem Sie bestätigt haben, dass die Konfiguration korrekt ist, wählen Sie **Einfügen**.

    - Wenn die Funktion **Gespeicherte Ansichten** ausgeschaltet ist, werden Sie aufgefordert, den Browser zu aktualisieren, um die eingebettete App zu sehen.
    - Wenn die Funktion **Gespeicherte Ansichten** eingeschaltet ist, müssen Sie die Ansicht speichern, damit die Änderung beibehalten wird.

### <a name="embedding-a-canvas-app-as-a-full-page-experience-from-the-dashboard"></a>Einbetten einer Canvas App als Ganzseitenansicht vom Dashboard aus

Sie können eine Canvas App vom Dashboard aus einbetten, wenn die App nicht mit einer bestehenden Seite verknüpft ist, oder wenn Sie die App einfach als ganzseitigen Vorgang innerhalb der Finance und Operations App anzeigen möchten.

> [!NOTE]
> Um diese Funktionalitäten verfügbar zu machen, müssen Sie die Funktion **Ganzseitige Apps** in der Funktionsverwaltung einschalten. 

1. Öffnen Sie das Dashboard.
2. Wählen und halten Sie die Seite (oder klicken Sie mit der rechten Maustaste), wählen Sie **Personalisieren** und wählen Sie dann **Seite hinzufügen**.
3. Wählen Sie im Bereich **Seite hinzufügen** **Power Apps**.
4. Konfigurieren Sie die eingebettete App. Weitere Informationen finden Sie im Abschnitt [Konfigurieren einer Canvas App](#configuring-a-canvas-app) weiter unten in diesem Thema.
5. Wählen Sie **Speichern**, um die App dem Dashboard als neue Kachel hinzuzufügen.
6. Wählen Sie die neue Kachel auf dem Dashboard und bestätigen Sie, dass die Canvas App wie erwartet angezeigt wird.

### <a name="configuring-a-canvas-app"></a>Konfigurieren einer Canvas App

Wenn Sie eine Canvas App einbetten, müssen Sie die folgenden Parameter festlegen:

- **Name** - Geben Sie den Text ein, der für die Schaltfläche oder die Registerkarte angezeigt werden soll, die die eingebettete App enthalten wird. Oft werden Sie den Namen der App in diesem Feld wiederholen wollen.
- **App ID** - Geben Sie den global eindeutigen Bezeichner (GUID) für die Canvas App an, die Sie einbetten möchten. Um diesen Wert abzurufen, suchen Sie die App auf [make.powerapps.com](https://make.powerapps.com) und entnehmen Sie den Wert dem Feld **App-ID** unter **Details**.
- **Eingabekontext für die App** - Sie können optional das Feld auswählen, das die Daten enthält, die Sie als Eingabe an die App übergeben wollen. Informationen darüber, wie die App auf die Daten zugreifen kann, die von Apps für Finanzen und Betrieb gesendet werden, finden Sie im Abschnitt [Erstellung einer App, die von Apps für Finanzen und Betrieb gesendete Daten nutzt](#building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps) weiter unten in diesem Thema.

    Ab Version 10.0.19 wird auch die aktuelle juristische Entität als Kontext an die Canvas App übergeben, und zwar über den URL-Parameter **cmp**. Dieses Verhalten wirkt sich erst auf die Ziel-Canvas-App aus, wenn diese App diese Informationen verwendet.

- **Anwendungsgröße** - Wählen Sie den Typ der App, die Sie einbetten. Wählen Sie **Dünn** für Apps, die für mobile Geräte gebaut sind oder **Breit** für Apps, die für Tablets gebaut sind. Dieser Parameter stellt sicher, dass genügend Platz für die eingebettete App zur Verfügung steht.
- **Rechtliche Entitäten** - Sie können die juristischen Entitäten auswählen, für die die App verfügbar sein soll. Standardmäßig ist die App für alle juristischen Entitäten verfügbar. Diese Option ist nur verfügbar, wenn Sie direkt auf einer bestehenden Seite einbetten und die Funktion **[Gespeicherte Ansichten](saved-views.md)** ausgeschaltet ist.

## <a name="sharing-an-embedded-app"></a>Freigeben einer eingebetteten App

Nachdem Sie eine Canvas-App auf einer Seite eingebettet und bestätigt haben, dass sie korrekt funktioniert, möchten Sie die App vielleicht mit anderen Benutzern im System teilen. Führen Sie die folgenden Schritte aus, um eine eingebettete Canvas-App zu teilen.

1. [Teilen Sie die Canvas-App in Power Apps](/powerapps/maker/canvas-apps/share-app) mit den entsprechenden Benutzern, so dass diese in Power Apps direkt auf die App zugreifen können.
2. Teilen Sie die Personalisierungen, die mit der eingebetteten App verbunden sind, mit den gewünschten Benutzern. Sie können einen der folgenden Ansätze verwenden:

    - **Veröffentlichen Sie die Ansicht (empfohlen):** Wenn die Funktion **[Gespeicherte Ansichten](saved-views.md)** eingeschaltet ist, besteht die empfohlene und bevorzugte Vorgehensweise darin, eine Ansicht zu erstellen, die die eingebettete Canvas-App enthält, und diese Ansicht dann für die gewünschten Benutzer zu veröffentlichen. Dieser Ansatz stellt sicher, dass alle Benutzer, die über die Sicherheitsrollen verfügen, auf die die veröffentlichte Ansicht abzielt, die Canvas App auf der Seite sehen.

        Sie können eine Canvas App, die eingebettet wurde, auch als ganzseitige Ansicht vom Dashboard aus veröffentlichen. Wählen und halten Sie auf dem Dashboard die Kachel, die mit der App verknüpft ist (oder klicken Sie mit der rechten Maustaste), wählen Sie **Personalisieren** und dann **Seite veröffentlichen**. Es wird ein Erlebnis angezeigt, das dem *Veröffentlichen von Ansichten* ähnelt, und Sie können die Sicherheitsrollen auswählen, an die veröffentlicht werden soll. Wenn in Update 10.0.21 oder später die Funktion **Verbesserte Unterstützung juristischer Entitäten für gespeicherte Ansichten** aktiviert ist, können Sie die App auch für die gewünschten juristischen Entitäten veröffentlichen.

    - Wenn die Funktion **Gespeicherte Ansichten** ausgeschaltet ist, kann der System-Admin über die Seite **Personalisierung** eine Personalisierung, die die Canvas App enthält, an die entsprechenden Benutzer festlegen. Alternativ können Sie die Personalisierungen Ihrer Seite exportieren und sie dann an einen oder mehrere Benutzer senden. Jeder dieser Benutzer kann dann die Personalisierung importieren. Die Personalisierungs-Symbolleiste hat Schaltflächen, mit denen Sie Personalisierungen exportieren und importieren können.

> [!NOTE]
> Wenn die Canvas App für externe Benutzer freigegeben wurde, können diese Benutzer die eingebettete App innerhalb der Apps für Finanzen und Betrieb nicht verwenden. Sie können jedoch direkt in Power Apps auf die App zugreifen. Zu den externen Benutzern gehören Gäste und Benutzer, die nicht zu dem Azure-Verzeichnis Microsoft 365 gehören, in dem die Finance und Operations App bereitgestellt wird.

Unter [Personalisieren der Benutzeroberfläche](personalize-user-experience.md) finden Sie weitere Details zu den Personalisierungsfähigkeiten im Produkt und wie Sie diese verwenden können.

## <a name="building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps"></a>Erstellen einer Canvas App, die Daten verwendet, die von Apps für Finanzen und Betrieb gesendet werden

Wenn Sie eine Canvas App erstellen, die in eine Finance und Operations App eingebettet werden soll, besteht ein wichtiger Teil des Prozesses darin, die Eingabedaten aus dieser Finance und Operations App zu verwenden. Von der Power Apps-Entwicklungserfahrung aus können Sie über die Variable **Param("EntityId")** auf die Eingabedaten zugreifen, die von einer Finance und Operations App übergeben werden. Zusätzlich wird ab Version 10.0.19 auch die aktuelle juristische Entität über die Variable **Param(„cmp“)** an die Canvas App übergeben. 

In der OnStart-Funktion der App könnten Sie zum Beispiel die Eingabedaten aus den Apps Finance und Operations auf eine Variable wie diese festlegen:

``` Power Apps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));

If(!IsBlank(Param("cmp")), Set(FinOpsLegalEntity, Param("cmp")), Set(FinOpsLegalEntity, ""));
```

## <a name="viewing-a-canvas-app"></a>Anzeigen einer Canvas-App

Um eine eingebettete Canvas App auf einer Seite in Apps für Finanzen und Betrieb anzuzeigen, gehen Sie einfach auf eine Seite, die eine eingebettete App enthält. Denken Sie daran, dass Sie über die Schaltfläche **Power Apps** im Standardaktivitätsbereich auf Apps zugreifen können. Alternativ können Sie als neue Registerkarte, als Inforegister, als Blatt oder als neuer Bereich in einem Arbeitsbereich direkt auf der Seite angezeigt werden. Wenn Benutzer zum ersten Mal versuchen, eine App auf einer Seite zu laden, werden sie aufgefordert, sich anzumelden. Dieser Schritt stellt sicher, dass die Benutzer über die entsprechenden Berechtigungen zur Verwendung der App verfügen.

## <a name="editing-an-embedded-app"></a>Bearbeiten einer eingebetteten App

Nachdem eine Apps auf einer Seite eingebettet wurde, müssen Sie möglicherweise einige Änderungen der Variante von der App vornehmen. Angenommen, Sie möchten möglicherweise das Etikett ändern, das der eingebetteten App zugeordnet ist, oder eine neue Version der App wurde erstellt und Sie müssen die-App Kennung aktualisieren, um auf die aktuellste Version zu verweisen.

Gehen Sie folgendermaßen vor, um die Konfiguration von einer eingebetteten App zu bearbeiten:

1. Gehen Sie zum Bereich **App bearbeiten**.

    - Wenn der Zugriff auf die eingebettete App über die Schaltfläche Power Apps erfolgt, halten Sie die Schaltfläche Power Apps gedrückt (oder klicken Sie mit der rechten Maustaste) und wählen Sie **Personalisieren**. Wählen Sie im Dropdownmenü **App auswählen** die App aus, die Sie konfigurieren möchten.
    - Wenn die eingebettete App direkt auf der Seite angezeigt wird, wählen Sie **Optionen** und dann **Diese Seite personalisieren** aus. Bei Verwendung des Tools **Auswählen** klicken Sie auf die eingebettete App.
    - Wenn die eingebettete App über das Dashboard hinzugefügt wurde, öffnen Sie das Dashboard, wählen und halten Sie (oder klicken Sie mit der rechten Maustaste) die Kachel, die mit der Canvas App verknüpft ist, wählen Sie **Personalisieren** und wählen Sie dann **Seite bearbeiten**.

2. Nehmen Sie die erforderlichen Änderungen an der Appkonfiguration vor, und klicken Sie anschließend auf **Speichern**.

## <a name="removing-an-app"></a>App entfernen

Nachdem eine App in eine Seite eingebettet wurde, gibt es ein paar Möglichkeiten, sie bei Bedarf wieder zu entfernen:

- Wechseln Sie zum Bereich **Eine App bearbeiten** mithilfe der Anweisungen vom Bereich [Bearbeiten einer eingebetteten App](#editing-an-embedded-app) oben in diesem Thema. Vergewissern Sie sich, dass der Bereich Informationen für die eingebettete App anzeigt, den Sie entfernen möchten, und klicken Sie dann auf die Schaltfläche **Löschen**.
- Wenn die eingebettete App vom Dashboard aus hinzugefügt wurde, öffnen Sie das Dashboard, wählen und halten Sie (oder klicken Sie mit der rechten Maustaste) die Kachel, die mit der Canvas App verbunden ist, wählen Sie **Personalisieren** und dann **Seite entfernen**. 
- Da eine eingebettete App als Personalisierungsdaten gespeichert wird, werden durch die Entfernung der Personalisierung der Seite auch alle eingebetteten Apps auf dieser Seite entfernt. Beachten Sie, dass die Löschung der Personalisierung dauerhaft ist und nicht rückgängig gemacht werden kann. Um Ihre Personalisierungen auf einer Seite zu entfernen, wählen Sie **Optionen** aus, und klicken Sie dann auf **Dieses Seite personalisieren** und schließlich auf die Schaltfläche **Löschen**. Nachdem Sie Ihrem Browser aktualisiert haben, werden auch alle vorherigen Personalisierungen für diese Seite entfernt. Unter [Personalisieren der Benutzeroberfläche](personalize-user-experience.md) finden Sie weitere Informationen darüber, wie Sie Seiten mithilfe der Personalisierung optimieren können.

## <a name="appendix"></a>Anhang

### <a name="developer-modeling-a-canvas-app-on-a-form"></a>[Entwickler] Modellieren einer Canvas App auf einem Formular

Während sich dieses Thema auf das Einbetten von Canvas Apps durch Personalisierung konzentriert, haben Entwickler auch die Möglichkeit, eine Canvas App zu einem Formular hinzuzufügen, indem sie die Visual Studio Entwicklungserfahrung verwenden. Fügen Sie dazu einfach ein PowerAppsHostControl in das Formular ein. Die für das Steuerelement verfügbaren Metadaten-Eigenschaften bieten die gleichen Funktionalitäten wie die Personalisierung.

### <a name="developer-specifying-where-an-app-can-be-embedded"></a>[Entwickler] Festlegen, wo eine App eingebettet werden kann

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
