---
title: Produktionsausführungsoberfläche anpassen
description: In diesem Artikel wird erläutert, wie Sie aktuelle Formulare erweitern oder neue Formulare und Schaltflächen für die Ausführungsoberfläche der Produktionsumgebung erstellen.
author: johanhoffmann
ms.date: 05/04/2022
ms.topic: article
ms.search.form: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-11-08
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 13fa6c2f3c30a820585d1b5a758f57ec563664d1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845981"
---
# <a name="customize-the-production-floor-execution-interface"></a>Produktionsausführungsoberfläche anpassen

[!include [banner](../includes/banner.md)]

Entwickler können aktuelle Formulare erweitern oder eigene Formulare und Schaltflächen für die Ausführungsoberfläche der Produktionsumgebung erstellen. Nachdem Sie den Code für diese neuen Elemente hinzugefügt haben, können Administratoren oder Werkstatt-Manager sie mithilfe der standardmäßigen Konfigurationssteuerelemente problemlos zur Benutzeroberfläche hinzufügen.

Hier sind beispielsweise einige der möglichen Lösungen, wenn neue Spalten in einem Hauptformular benötigt werden:

- Erweitern Sie das Formular `JmgProductionFloorExecutionMainGrid`, und fügen Sie die gewünschten Felder hinzu.
- Erstellen Sie ein neues Formular und fügen Sie es als neue Hauptansicht (Registerkarte) hinzu.

## <a name="add-a-new-button-action"></a>Eine neue Schaltfläche hinzufügen (Aktivität)

Gehen Sie folgendermaßen vor, um eine neue Schaltfläche (Aktivität) hinzuzufügen, um eine Klasse zu erstellen, die Ihre benutzerdefinierte Aktivität implementiert.

1. Erstellen Sie eine neue Klasse mit dem Namen `<ExtensionPrefix>_JmgProductionFloorExecution<ActionName>Action`, wobei:

    - `<ExtensionPrefix>` Ihre Lösung eindeutig identifiziert, normalerweise unter Verwendung Ihres Firmennamens.
    - `<ActionName>` ein eindeutiger Name für die Klasse ist. Er identifiziert normalerweise die Art der Aktivität.

1. Die neue Klasse muss die `JmgProductionFloorExecutionAction`-Klasse erweitern.
1. Überschreiben Sie alle erforderlichen Methoden.

Sehen Sie sich für Beispiele den Code für die folgenden Klassen an:

- `JmgProductionFloorExecutionBreakAction` – Eine Klasse für eine einfache Aktivität, die keine Datensätze benötigt.
- `JmgProductionFloorExecutionReportFeedbackAction` – Eine Klasse, die komplexere Funktionen bereitstellt.

Wenn Sie fertig sind, wird die neue Schaltfläche (Aktivität) automatisch auf der Seite **Design-Registerkarten** in Microsoft Dynamics 365 Supply Chain Management aufgelistet. Dort können Sie (oder ein Administrator oder Werkstatt-Manager) sie einfach der primären oder sekundären Symbolleiste hinzufügen, genau wie Sie die Standardschaltflächen hinzufügen können. Anweisungen finden Sie unter [Produktionsausführungsoberfläche entwerfen](production-floor-execution-tabs.md).

## <a name="add-a-new-main-view"></a>Eine neue Hauptansicht hinzufügen

1. Erstellen Sie ein neues Formular mit den gewünschten Elementen und Funktionen. Beachten Sie, dass dieses Formular ein neues Formular ist, keine Erweiterung. Benennen Sie das Formular `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`, wobei:

    - `<ExtensionPrefix>` Ihre Lösung eindeutig identifiziert, normalerweise unter Verwendung Ihres Firmennamens.
    - `<FormName>` ein eindeutiger Name für das Formular ist.

1. Erstellen Sie einen Menüpunkt mit dem Namen `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`.
1. Erstellen Sie eine Erweiterung mit dem Namen `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension`, bei der die `getMainMenuItemsList`-Methode erweitert wird, indem der neue Menüpunkt zur Liste hinzugefügt wird. Der folgende Code zeigt ein Beispiel.

    ```xpp
    [ExtensionOf(classStr(JmgProductionFloorExecutionMenuItemProvider))]
    public final class <ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>_Extension{
        static public List getMainMenuItemsList()
        {
            List menuItemList = next getMainMenuItemsList();
            menuItemList.addEnd(menuItemDisplayStr(<ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>));
            return menuItemList;
        }
    ```

Wenn Sie fertig sind, wird die neue Hauptansicht automatisch im Kombinationsfeld **Hauptansicht** auf der Seite **Design-Registerkarten** in Supply Chain Management aufgelistet. Dort können Sie (oder ein Administrator oder Werkstatt-Manager) sie einfach neuen oder vorhandenen Registerkarten hinzufügen, genau wie Sie die Standardhauptansichten hinzufügen können. Anweisungen finden Sie unter [Produktionsausführungsoberfläche entwerfen](production-floor-execution-tabs.md).

## <a name="add-a-details-view"></a>Detailansicht hinzufügen

1. Erstellen Sie ein neues Formular mit den gewünschten Elementen und Funktionen. Beachten Sie, dass dieses Formular neu ist, keine Erweiterung. Benennen Sie das Formular `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`, wobei: 

    - `<ExtensionPrefix>` Ihre Lösung eindeutig identifiziert, normalerweise unter Verwendung Ihres Firmennamens.
    - `<FormName>` ein eindeutiger Name für das Formular ist.

1. Erstellen Sie einen Menüpunkt mit dem Namen `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`.
1. Erstellen Sie eine Erweiterung mit dem Namen `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension`, bei der die `getDetailsMenuItemList`-Methode erweitert wird, indem der neue Menüpunkt zur Liste hinzugefügt wird.

Wenn Sie fertig sind, wird die neue Detailansicht automatisch im Kombinationsfeld **Detailansicht** auf der Seite **Design-Registerkarten** in Supply Chain Management aufgelistet. Dort können Sie (oder ein Administrator oder Werkstatt-Manager) sie einfach neuen oder vorhandenen Registerkarten hinzufügen, genau wie Sie die Standarddetailansichten hinzufügen können. Anweisungen finden Sie unter [Produktionsausführungsoberfläche entwerfen](production-floor-execution-tabs.md).

## <a name="add-a-numeric-keypad-to-a-form-or-dialog"></a>Zehnertastatur zu einem Formular oder Dialogfeld hinzufügen

Das folgende Beispiel zeigt, wie einem Formular Zehnertastaturen hinzugefügt werden.

1. Die Anzahl der Zehnertastatur-Controller, die jedes Formular enthält, muss der Anzahl der Zehnertastaturen in diesem Formular entsprechen.

    ```xpp
    private JmgProductionFloorExecutionNumpadController   numpadController1;
    private JmgProductionFloorExecutionNumpadController   numpadController2;
    private JmgProductionFloorExecutionNumpadController   numpadController3;
    ```

1. Richten Sie das Verhalten jedes Zehnertastatur-Controllers ein, und verbinden Sie jeden Zehnertastatur-Controller mit einem Zehnertastatur-Formularteil.

    ```xpp
    /// <summary>
    /// Initializes all numpad controllers, defines their behavior and connects them with numpad form parts.
    /// </summary>
    public void initializeNumpadController()
    {
        numpadController1 = new JmgProductionFloorExecutionNumpadController();
        numpadController1.getValueFromNumpadDelegate += eventhandler(this.setQuanityValueFromNumpad_1);
        QuantityNumpad1.getPartFormRun().setNumpadController(numpadController1);
    
        numpadController2 = new JmgProductionFloorExecutionNumpadController();
        numpadController2.parmNumpadEnabled(false);
        numpadController2.parmNumpadValue(333.56);
        numpadController2.getValueFromNumpadDelegate += eventhandler(this.setQuanityValueFromNumpad_2);
        QuantityNumpad2.getPartFormRun().setNumpadController(numpadController2);
    }
    ```

## <a name="use-a-numeric-keypad-as-a-pop-up-dialog"></a>Zehnertastatur als Popup-Dialogfeld verwenden

Das folgende Beispiel zeigt eine Möglichkeit zum Einrichten eines Zehnertastatur-Controllers für ein Popup-Dialogfeld.

```xpp
private void setupNumpadController()
{
    numpadController = new JmgProductionFloorExecutionNumpadController();
    numpadController.parmShouldNumpadShowOkCancelButtons(true);
    numpadController.setNumpadValueToParentFormDelegate += eventhandler(this.setQtyValueFromNumpad);
}
```

Das folgende Beispiel zeigt eine Möglichkeit zum Aufrufen des Popup-Dialogfelds für eine Zehnertastatur.

```xpp
Args args = new Args();
args.name(formstr(JmgProductionFloorExecutionNumpad));
args.menuItemName(menuItemDisplayStr(JmgProductionFloorExecutionNumpad));
args.caller(element);
Object formRun = classfactory.formRunClass(args);
formRun.init();
formRun.setNumpadController(numpadController);
numpadController.setValueToNumpad(333.56);
formRun.run();
```

## <a name="add-a-date-and-time-controls-to-a-form-or-dialog"></a>Formular oder Dialogfeld ein Datums- und Uhrzeitsteuerelement hinzufügen

Dieser Abschnitt zeigt, wie Sie einem Formular oder Dialogfeld Datums- und Uhrzeitsteuerelemente hinzufügen. Die berührungsfreundlichen Steuerelemente für Datum und Uhrzeit ermöglichen es den Mitarbeitern, Datum und Uhrzeit festzulegen. Die folgenden Screenshots zeigen, wie die Steuerelemente normalerweise auf der Seite angezeigt werden. Die Zeitsteuerung bietet sowohl 12-Stunden- als auch 24-Stunden-Versionen; die angezeigte Version folgt den Einstellungen für das Benutzerkonto, unter dem die Schnittstelle ausgeführt wird.

![Beispiel für Datumssteuerung.](media/pfe-customize-date-control.png "Beispiel für Datumssteuerung")

![Beispiel für Uhrzeitsteuerung mit einer 12-Stunden-Uhr.](media/pfe-customize-time-control-12h.png "Beispiel für Uhrzeitsteuerung mit einer 12-Stunden-Uhr")

![Beispiel für Uhrzeitsteuerung mit einer 24-Stunden-Uhr.](media/pfe-customize-time-control-24h.png "Beispiel für Uhrzeitsteuerung mit einer 24-Stunden-Uhr")

Das folgende Verfahren zeigt ein Beispiel für das Hinzufügen von Datums- und Uhrzeitsteuerelementen zu einem Formular.

1. Fügen Sie dem Formular für jedes Datums- und Uhrzeitsteuerelement, das das Formular enthalten soll, einen Controller hinzu. (Die Anzahl der Controller muss der Anzahl der Datums- und Uhrzeitsteuerelemente im Formular entsprechen.)

    ```xpp
    private JmgProductionFloorExecutionDateTimeController  dateFromController; 
    private JmgProductionFloorExecutionDateTimeController  dateToController; 
    private JmgProductionFloorExecutionDateTimeController  timeFromController; 
    private JmgProductionFloorExecutionDateTimeController  timeToController;
    ```

1. Deklarieren Sie die erforderlichen Variablen (vom Typ `utcdatetime`).

    ```xpp
    private utcdatetime fromDateTime;
    private utcdatetime toDateTime;
    ```

1. Erstellen Sie Methoden, bei denen „Datetime“ von den „Datetime“-Controllern aktualisiert wird. Das folgende Beispiel zeigt eine solche Methode.

    ```xpp
    private void setFromDateTime(utcdatetime _value)
        {
            fromDateTime = _value;
        }
    ```

1. Richten Sie das Verhalten jedes „Datetime“-Controllers ein und verbinden Sie jeden Controller mit einem Formularteil. Das folgende Beispiel zeigt, wie Sie Daten für „Datum ab“- und „Uhrzeit ab“-Steuerelemente einrichten. Sie könnten ähnlichen Code für „Datum bis“- und „Uhrzeit bis“-Steuerelemente hinzufügen (nicht gezeigt).

    ```xpp
    /// <summary>
    /// Initializes all date and time controllers, defines their behavior, and connects them with the form parts.
    /// </summary>
    private void initializeDateControlControllers()
    {
        dateFromController = new JmgProductionFloorExecutionDateTimeController();
        dateFromController.setDateControlValueToCallerFormDelegate += eventhandler(this.setFromDateTime);
        dateFromController.parmDateTimeValue(fromDateTime);
    
        timeFromController = new JmgProductionFloorExecutionDateTimeController();
        timeFromController.setDateControlValueToCallerFormDelegate += eventhandler(this.setFromDateTime);
        timeFromController.parmDateTimeValue(fromDateTime);
        
        DateFromFormPart.getPartFormRun().setDateControlController(dateFromController, timeFromController);
        TimeFromFormPart.getPartFormRun().setTimeControlController(timeFromController, dateFromController);
        
        ...

    }
    ```

    Wenn Sie nur eine Datumssteuerung benötigen, können Sie die Einrichtung der Zeitsteuerung überspringen und stattdessen einfach die Datumssteuerung einrichten, wie im folgenden Beispiel gezeigt:

    ```xpp
    {
        dateFromController = new JmgProductionFloorExecutionDateTimeController();
        dateFromController.setDateControlValueToCallerFormDelegate += eventhandler(this.setFromDateTime);
        dateFromController.parmDateTimeValue(fromDateTime);
    
        DateFromFormPart.getPartFormRun().setDateControlController(dateFromController, null);
    }
    ```

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Stil der Produktionsausführungsoberflächenschnittstelle](production-floor-execution-styles.md)
- [Produktionsausführungsoberfläche entwerfen](production-floor-execution-tabs.md)
