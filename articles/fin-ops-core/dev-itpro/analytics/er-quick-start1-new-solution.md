---
title: Entwerfen einer neuen EB-Lösung zum Drucken eines benutzerdefinierten Berichts
description: In diesem Thema wird erläutert, wie Sie eine EB-Lösung (Elektronische Berichterstellung) zum Drucken eines benutzerdefinierten Berichts entwerfen.
author: NickSelin
manager: AnnBe
ms.date: 08/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ede88bc1767304a86a86ec27365db9403c5a951d
ms.sourcegitcommit: 4909e55529f03310d24b7e40d52751e24d35259b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/10/2020
ms.locfileid: "3678247"
---
# <a name="design-a-new-er-solution-to-print-a-custom-report"></a>Entwerfen einer neuen EB-Lösung zum Drucken eines benutzerdefinierten Berichts

[!include[banner](../includes/banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer in den Rollen "Systemadministrator", "Entwickler elektronischer Berichte" oder "Funktionsberater für elektronische Berichte" Parameter des ER-Frameworks konfigurieren und die erforderlichen ER-Konfigurationen einer neuen ER-Lösung für den Zugriff auf die Daten einer bestimmten Geschäftsdomäne entwerfen kann und einen benutzerdefinierten Bericht im Microsoft Office-Format erzeugen kann. Diese Schritte können im Unternehmen **USMF** ausgeführt werden.

- [Konfigurieren des EB-Frameworks](#ConfigureFramework)

    - [Parameter der elektronischen Berichterstellung konfigurieren](#ConfigureParameters)
    - [Aktivieren eines EB-Konfigurationsanbieters](#ActivateProvider)

        - [Überprüfen der Liste der EB-Konfigurationsanbieter](#ReviewProvidersList)
        - [Hinzufügen eines neuen EB-Konfigurationsanbieters](#AddProvider)
        - [Aktivieren eines EB-Konfigurationsanbieters](#ActivateAddedProvider)

- [Entwerfen eines domänenspezifischen Datenmodells](#DesignModel)

    - [Importieren einer neuen Datenmodellkonfiguration](#ImportDataModel)
    - [Neue Datenmodellkonfiguration erstellen](#DesignDataModel)

        - [Benennen des Datenmodells](#NameDataModel)
        - [Hinzufügen von Datenmodellfeldern](#FieldsEntry)
        - [Vervollständigen des Datenmodellentwurfs](#CompleteDataModel)

- [Entwerfen einer Modellzuordnung für das konfigurierte Datenmodell](#DesignMapping)

    - [Importieren einer neuen Modellzuordnungskonfiguration](#ImportModelMapping)
    - [Erstellen einer neuen Modellzuordnungskonfiguration](#CreateModelMapping)

        - [Entwerfen einer neuen Modellzuordnungskomponente](#DesignMappingComponent)
        - [Hinzufügen von Datenquellen für den Zugriff auf Anwendungstabellen](#AddMmDataSource1)
        - [Hinzufügen von Datenquellen für den Zugriff auf Anwendungsaufzählungen](#AddMmDataSource2)
        - [Hinzufügen von EB-Beschriftungen, um einen Bericht in einer bestimmten Sprache zu erzeugen](#AddMmLabels)
        - [Hinzufügen einer Datenquelle, um die Ergebnisse des Vergleichs von Aufzählungswerten mit einem Textwert](#AddMmDataSource3)
        - [Binden von Datenquellen an Datenmodellfelder](#AddMmBindings1)
        - [Vervollständigen des Designs der Modellzuordnung](#CompleteModelMapping)

- [Entwerfen einier Vorlage für einen benutzerdefinierten Bericht](#DesignReportTemplate)
- [Entwerfen eines Formats](#DesignFormat)

    - [Importieren einer entworfenen Formatkonfiguration:](#FormatImport)
    - [Dient zum Erstellen einer neuen Format-Konfiguration.](#FormatCreate)

        - [Importieren einer Berichtvorlage](#ImportReportTemplate)
        - [Konfigurieren eines Formats](#ConfigureFormat)
        - [Definieren Sie die Datenbindung für einen Berichtstitel](#DefineFormatBindings)
        - [Überarbeiten Sie die Modelldatenquelle](#ReviewModelDataSource)
        - [Binden von Formatelementen an Datenquellenfelder](#BindFormatElements)

    - [Verwenden eines entworfenen Formats aus EB](#RunFormatFromER)

- [Anpassen eines entworfenes Format](#TuneFormat)

    - [Ändern eines Formats, um den Namen eines generierten Dokuments zu ändern](#ModifyToChangeName)
    - [Ändern eines Formats, um die Abfolge von Fragen zu ändern](#ModifyToOrder)
    - [Verwenden eines geänderten Formats aus ER](#RunFormatFromER2)
    - [Abschließen des Formatentwurfs](#CompleteFormat)

- [Entwickeln von Anwendungsartefakte, um den entworfenen Bericht aufzurufen](#DevelopCustomCode)

    - [Quellcode ändern](#ModifySourceCode)

        - [Hinzufügen einer Datenvertragsklasse](#DataContractClass)
        - [Hinzufügen einer UI-Builder-Klasse](#UIBuilderClass)
        - [Hinzufügen einer Datenanbieterklasse](#DataProviderClass)
        - [Hinzufügen einer Etikettendatei](#LabelsFile)
        - [Hinzufügen einer Berichtserviceklasse](#ServiceClass)
        - [Hinzufügen einer Bericht-Controller-Klasse](#ControllerClass)
        - [Hinzufügen eines Menüpunkts](#MenuItem)
        - [Hinzufügen einer Menüoption in ein Menü](#Menu)
        - [Erstellen eines Visual Studio-Projekts](#BuildVSProject)

    - [Verwenden eines Formats von der Anwendung aus](#RunFormatFromApp)

- [Optimieren einer entworfenen EB-Lösung](#TuneSolution)

    - [Ändern einer Modellzuordnung](#ModifyModelMapping)

        - [Hinzufügen von Datenquellen für den Zugriff auf Datenvertragsobjekte](#AddDataSource1)
        - [Hinzufügen einer Datenquelle, um auf Zuordnungsdatensätze im EB-Format zuzugreifen](#AddDataSource2)
        - [Hinzufügen einer Datenquelle, um auf einen Formatzuordnungsdatensatz eines aktiven EB-Format zuzugreifen](#AddDataSource3)
        - [Eingeben des Namens des aktiven EB-Formats im Datenmodell](#AddBinding)
        - [Vervollständigen des Designs der Modellzuordnung](#CompleteModelMapping2)

    - [Ändern eines Formats](#ModifyFormat)

        - [Hinzufügen eines neuen Formatelements](#AddFormatElement)
        - [Binden des hinzugefügten Formatelements](#BindAddedFormatElement)
        - [Abschließen des Formatentwurfs](#CompleteFormat2)

    - [Verwenden eines Formats von der Anwendung aus](#RunFormatFromApp2)
    - [Verwenden eines Formats von EB aus](#RunFormatFromER3)
    - [Konfigurieren eines Formatziels für die Bildschirmvorschau](#ConfigureDestination)
    - [Ausführen eines Formats mit der Anwendung, um eine Vorschau als PDF-Dokument anzuzeigen](#RunFormatFromApp3)

- [Zusätzliche Ressourcen](#References)

In diesem Beispiel erstellen Sie eine neue EB-Lösung für das Modul [Fragebogen](https://docs.microsoft.com/dynamics365/human-resources/hr-learning-questionnaires). Mit dieser neuen EB-Lösung können Sie einen Bericht mithilfe eines Microsoft Excel-Arbeitsblatts als Vorlage erstellen. Sie können dann den Bericht **Fragebogen** im Excel- oder PDF-Format zusätzlich zum vorhandenen SSRS-Bericht (SQL Server Reporting Services) generieren. Auf Anfrage können Sie den neuen Bericht auch später ändern. Eine Codierung ist nicht erforderlich.

1. Um den vorhandenen Bericht auszuführen, wählen Sie **Fragebogen**\>**Entwurf**\>**Fragebogenbericht**.

    ![Auswählen des Fragebogenbericht-Menüpunkts im Fragebogenmodul, um den vorhandenen SSRS-Bericht auszuführen](./media/er-quick-start1-application-menu-origin.png)

2. Geben Sie im Dialogfeld **Fragebogenbericht** Auswahlkriterien angeben. Wenden Sie einen Filter an, sodass der Bericht nur den Fragebogen **SBCCrsExam** enthält.

    ![Festlegen von Auswahlkriterien im Dialogfeld "Fragebogenbericht"](./media/er-quick-start1-ssrs-report-dialog.png)

Die folgende Abbildung zeigt die generierte Version des SSRS-Berichts für den Fragebogen **SBCCrsExam**.

![Generierter SSRS-Bericht](./media/er-quick-start1-ssrs-report.png)

## <a name="configure-the-er-framework"></a><a name="ConfigureFramework"></a>Konfigurieren des EB-Frameworks

Als Benutzer mit der Rolle "Entwickler für elektronische Berichterstellung" müssen Sie den mindestens notwendigen EB-Parameter, bevor Sie mit dem Entwerfen Ihrer neuen EB-Lösung mithilfe des EB-Rahmens beginnen.

### <a name="configure-er-parameters"></a><a name="ConfigureParameters"></a>Parameter der elektronischen Berichterstellung konfigurieren

1. Wählen Sie **Organisationsverwaltung** \> **Arbeitsbereich** \> **Elektronische Berichterstellung** aus.
2. Klicken Sie im Arbeitsbereich **Elektronische Berichterstellung**  auf **Elektronische Berichterstellungsparameter**.
3. Setzen Sie auf der Seite **Elektronische Berichterstellungsparameter**  auf der Registerkarte **Allgemein**  die Option **Entwurfmodus aktivieren** auf **Ja**.
4. Legen Sie auf der Registerkarte **Anhänge**  die folgenden Parameter fest:

    - Setzen Sie das Feld **Konfigurationen** für das Unternehmen **USMF** auf **Datei**.
    - Wählen Sie in den Feldern **Einzelvorgangsarchiv**, **Temporär**, **Grundlage** und **Andere** den **Dateityp** aus.

Weitere Informationen zu EB-Parametern finden Sie unter [Konfigurieren des EB-Frameworks](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a name="ActivateProvider"></a>Aktivieren eines EB-Konfigurationsanbieters

Jede hinzugefügte EB-Konfiguration wird als Eigentum eines EB-Konfigurationsanbieters markiert. Daher müssen Sie im Arbeitsbereich **Elektronische Berichterstellung** einen EB-Konfigurationsanbieter aktivieren, bevor Sie mit dem Hinzufügen oder Bearbeiten von EB-Konfigurationen beginnen.

> [!NOTE]
> Nur der Besitzer einer EB-Konfiguration kann diese bearbeiten. Daher muss im Arbeitsbereich **Elektronische Berichterstellung** der entsprechende EB-Konfigurationsanbieter aktiviert werden, bevor eine EB-Konfigurationen bearbeitet werden kann.

#### <a name="review-the-list-of-er-configuration-providers"></a><a name="ReviewProvidersList"></a>Überprüfen der Liste der EB-Konfigurationsanbieter

1. Wählen Sie **Organisationsverwaltung** \> **Arbeitsbereich** \> **Elektronische Berichterstellung** aus.
2. Wählen Sie im Arbeitsbereich **Elektronische Berichterstellung** im Abschnitt **Zugehörige Links** die Option **Konfigurationsanbieter** aus.
3. Auf der Seite **Konfigurationsanbietertabelle** hat jeder Konfigurationsanbieterdatensatz einen eindeutigen Namen und eine eindeutige URL. Überprüfen Sie den Inhalt dieser Seite. Wenn bereits ein Datensatz für **Litware, Inc.** (`https://www.litware.com`) vorhanden ist, überspringen Sie die nächste Prozedur [Hinzufügen eines neuen EB-Konfigurationsanbieters](#ActivateProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a name="AddProvider"></a>Hinzufügen eines neuen EB-Konfigurationsanbieters

1. Wählen Sie auf der Seite **Konfigurationsanbieter** die Option **Neu** aus.
2. Geben Sie im Feld **Name** **Litware, Inc.** ein.
3. Geben Sie im Feld **Internetadresse**  `https://www.litware.com` ein.
4. Wählen Sie  **Speichern** aus.

#### <a name="activate-an-er-configuration-provider"></a><a name="ActivateAddedProvider"></a>Aktivieren eines EB-Konfigurationsanbieters

1. Wählen Sie **Organisationsverwaltung** \> **Arbeitsbereich** \> **Elektronische Berichterstellung** aus.
2. Wählen Sie im Arbeitsbereich **Elektronische Berichterstattung** **Litware, Inc.** für Ihren Konfigurationsanbieter aus.
3. Wählen Sie  **Als aktiv festlegen** aus.

Weitere Informationen zu EB-Konfigurationsanbietern finden Sie unter [Erstellen von Konfigurationsanbietern und Markieren als aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="design-a-domain-specific-data-model"></a><a name="DesignModel"></a>Entwerfen eines domänenspezifischen Datenmodells

Sie müssen eine neue EB-Konfiguration erstellen, die eine Komponente [Datenmodell](general-electronic-reporting.md#data-model-and-model-mapping-components) für den Geschäftsbereich **Fragebogen** enthält. Dieses Datenmodell wird später als Datenquelle verwendet, wenn Sie ein EB-Format zum Generieren des Berichts **Fragebogen** entwerfen.

Durch Ausführen der Schritte im Abschnitt [Importieren einer neuen Datenmodellkonfiguration](#ImportDataModel) können Sie das erforderliche Datenmodell aus der bereitgestellten XML-Datei importieren. Alternativ können Sie mit den Schritten im Abschnitt [Erstellen einer neuen Datenmodellkonfiguration](#DesignDataModel) dieses Datennmodell neu entwerfen.

### <a name="import-a-new-data-model-configuration"></a><a name="ImportDataModel"></a>Importieren einer neuen Datenmodellkonfiguration

1. Laden Sie die Datei [Fragebögen model.version.1.xml ](https://go.microsoft.com/fwlink/?linkid=851448) herunter und speichern Sie sie auf Ihrem lokalen Computer.
2. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
3. Wählen Sie im Arbeitsbereich **Elektronische Berichterstellung** die Option **Berichterstellungskonfigurationen** aus.
4. Wählen Sie im Aktivitätsbereich **Austausch** \> **Aus XML-Datei laden** aus.
5. Klicken Sie auf **Durchsuchen**, und wählen Sie die Datei **Questionnaires model.version.1.xml** aus.
6. Wählen Sie **OK** aus, um die Konfiguration zu importieren.

Überspringen Sie den nächsten Vorgang, um fortzufahren. [Erstellen Sie eine neue Datenmodellkonfiguration](#DesignDataModel).

### <a name="create-a-new-data-model-configuration"></a><a name="DesignDataModel"></a>Neue Datenmodellkonfiguration erstellen

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Wählen Sie im Arbeitsbereich **Elektronische Berichterstellung** die Option **Berichterstellungskonfigurationen** aus.
3. Wählen Sie **Konfiguration erstellen**.
4. Geben Sie im Drop-Down-Dialogfeld im Feld **Name** **Fragebotenmodell** ein.
5. Wählen Sie **Konfiguration erstellen** aus, um die Konfiguration zu erstellen.

#### <a name="name-the-data-model"></a><a name="NameDataModel"></a>Benennen Sie das Datenmodell

1. Wählen Sie auf der Seite **Konfigurationen** im Konfigurationsbaum **Fragebogenmodell** aus.
2. Wählen Sie **Designer** aus.
3. Geben Sie auf der Seite **Datenmodelldesigner** auf dem Inforegister **Allgemein** im Feld **Name** den Eintrag <a name="DataModeName"></a>**Fragebögen** ein.

#### <a name="add-new-data-model-fields"></a><a name="FieldsEntry"></a>Hinzufügen neuer Datenmodellfeldern

1. Wählen Sie auf der Seite **Datenmodelldesigner** die Option **Neu** aus.
2. Führen Sie im Dropdown-Dialogfeld zum Hinzufügen eines Datenmodellknotens die folgenden Schritte aus:

    1. Wählen Sie **Modellstamm** als Typ des neuen Knotens aus.
    2. Geben Sie im Feld **Name** die Bezeichnung <a name="RootDefinitionName"></a>**Stamm** ein.
    3. Wählen Sie zum Hinzufügen des neuen Knotens **Hinzufügen** aus.

    Dieser Stammdeskriptor wird verwendet, um Daten für den Bericht **Fragebogen** bereitzustellen. Ein einzelnes Datenmodell kann mehrere Deskriptoren haben. Jeder Deskriptor kann für ein einzelnes EB-Format angegeben werden, um Daten zu identifizieren, die zum Generieren des Berichts erforderlich sind.

3. Wählen Sie erneut **Neu** aus und führen Sie dann im Dropdown-Dialogfeld zum Hinzufügen eines Datenmodellknotens die folgenden Schritte aus:

    1. Wählen Sie **Untergeordnetes Element eines aktiven Knotens** als Typ des neuen Knotens aus.
    2. Geben Sie im Feld **Name** die Bezeichnung **Firmenname** ein.
    3. Wählen Sie im Feld **Artikeltyp** **Zeichenfolge** aus.
    4. Wählen Sie zum Hinzufügen des neuen Felds **Hinzufügen** aus.

    Dieses Feld ist erforderlich, um den Namen des aktuellen Unternehmens an einen EB-Bericht zu übergeben, der dieses Datenmodell als Datenquelle verwendet.

4. Wählen Sie erneut **Neu** aus und führen Sie dann im Dropdown-Dialogfeld zum Hinzufügen eines Datenmodellknotens die folgenden Schritte aus:

    1. Wählen Sie **Untergeordnetes Element eines aktiven Knotens** als Typ des neuen Knotens aus.
    2. Geben Sie im Feld **Name** die Bezeichnung **Fragebogen** ein.
    3. Wählen Sie im Feld **Artikeltyp** **Datensatzliste** aus.
    4. Wählen Sie zum Hinzufügen des neuen Felds **Hinzufügen** aus.

    Mit diesem Feld wird die Liste der Fragebögen an einen EB-Bericht übergeben, der dieses Datenmodell als Datenquelle verwendet.

5. Wählen Sie den Knoten **Fragebogen** aus.
6. Fügen Sie die erforderlichen Felder des bearbeitbaren Datenmodells auf dieselbe Weise hinzu, bis Sie die folgende Datenmodellstruktur abgeschlossen haben.

    | Feldpfad                                                    | Datentyp   | Feldbezeichnung/Rückgabewert |
    |---------------------------------------------------------------|-------------|----------------------------------|
    | Stamm                                                          |             | Der Bezugspunkt zum Anfordern von Fragebogendaten. |
    | Stamm\\CompanyName                                             | Zeichenfolge      | Der Name des aktuellen Unternehmens. |
    | Stamm\\ExecutionContext                                        | Aufzeichnen      | Formatausführungsdetails. |
    | Stamm \\ExecutionContext \\Formatname                            | Zeichenfolge      | Der Name des ausgeführten EB-Formats. |
    | Stamm\\Fragebogen                                           | Datensatzliste | Die Liste der Fragebögen |
    | Stamm\\Fragebogen\\Aktiv                                   | Zeichenfolge      | Der Status des aktuellen Fragebogens. |
    | Stamm\\Fragebogen\\Code                                     | Zeichenfolge      | Der Code des aktuellen Fragebogens. |
    | Stamm\\Fragebogen\\Beschreibung                              | Zeichenfolge      | Die Beschreibung des aktuellen Fragebogens. |
    | Stamm\\Fragebogen\\QuestionnaireType                        | Zeichenfolge      | Der Typ des aktuellen Fragebogens. |
    | Stamm\\Fragebogen\\QuestionOrder                            | Zeichenfolge      | Die numerische Reihenfolge des aktuellen Fragebogens. |
    | Stamm\\Fragebogen\\ResultsGroup                             | Aufzeichnen      | Die Ergebnisparameter des aktuellen Fragebogens. |
    | Stamm\\Fragebogen\\ResultsGroup\\Code                       | Zeichenfolge      | Der Identifikationscode der aktuellen Ergebnisgruppe. |
    | Stamm\\Fragebogen\\ResultsGroup\\Beschreibung                | Zeichenfolge      | Die Beschreibung der aktuellen Ergebnisgruppe. |
    | Stamm\\Fragebogen\\ResultsGroup\\MaxNumberOfPoints          | Gleitkommazahl        | Die maximale Anzahl von Punkten, die verdient werden können. |
    | Stamm\\Fragebogen\\Frage                                 | Datensatzliste | Die Liste der Fragen für den aktuellen Fragebogen. |
    | Stamm\\Fragebogen\\Frage\\CollectionSequenceNumber       | Ganzzahl     | Die Folgenummer der aktuellen Antwortsammlung. |
    | Stamm\\Fragebogen\\Frage\\ID                             | Zeichenfolge      | Der Identifikationscode der aktuellen Frage. |
    | Stamm\\Fragebogen\\Frage\\MustBeCompleted                | Zeichenfolge      | Ein Flag, das angibt, ob die aktuelle Frage beantwortet werden muss. |
    | Stamm\\Fragebogen\\Frage\\PrimaryQuestion                | Zeichenfolge      | Ein Flag, das angibt, ob die aktuelle Frage primär ist. |
    | Stamm\\Fragebogen\\Frage\\SequenceNumber                 | Ganzzahl     | Die Folgenummer der aktuellen Frage. |
    | Stamm\\Fragebogen\\Frage\\Text                           | Zeichenfolge      | Der Text der aktuellen Frage. |
    | Stamm\\Fragebogen\\Frage\\Antwort                         | Datensatzliste | Die Liste der Antworten für die aktuelle Frage. |
    | Stamm\\Fragebogen\\Frage\\Antwort\\CorrectAnswer          | Zeichenfolge      | Ein Flag, das angibt, ob die aktuelle Frage korrekt ist. |
    | Stamm\\Fragebogen\\Frage\\Antwort\\Punkte                 | Gleitkommazahl        | Die Punkte, die verdient werden, wenn die aktuelle Antwort ausgewählt wird. |
    | Stamm\\Fragebogen\\Frage\\Antwort\\SequenceNumber         | Ganzzahl     | Die Folgenummer der aktuellen Antwort. |
    | Stamm\\Fragebogen\\Frage\\Antwort\\Text                   | Zeichenfolge      | Der Text der aktuellen Antwort. |

    Die folgende Abbildung zeigt das fertige bearbeitbare Datenmodell auf der Seite **Datenmodelldesigner**.

    ![Konfiguriertes Datenmodell im EB-Datenmodelldesigner](./media/er-quick-start1-model2.png)

7. Speichern Sie die Änderungen.
8. Schließen Sie die Seite **Datenmodelldesigner**.

#### <a name="complete-the-design-of-the-data-model"></a><a name="CompleteDataModel"></a>Vervollständigen des Datenmodellentwurfs

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Wählen Sie auf der Seite **Konfigurationen** im Konfigurationsbaum **Fragebogenmodell** aus.
3. Wählen Sie im Inforegister **Versionen** die Konfigurationsversion mit dem Status **Entwurf** aus.
4. Wählen Sie **Status ändern** \> **Abgeschlossen**.

Der Status von Version 1 dieser Konfiguration wird von **Entwurf** zu **Abgeschlossen** geändert. Version 1 kann nicht mehr geändert werden. Diese Version enthält das konfigurierte Datenmodell und kann als Basis für andere EB-Konfigurationen verwendet werden. Version 2 dieser Konfiguration wird erstellt und hat den Status **Entwurf**. Sie können diese Version bearbeiten, um das Datenmodell **Fragebogen** anzupassen.

![Versionen der bearbeitbaren EB-Konfiguration auf der Seite "Konfigurationen"](./media/er-quick-start1-model-configuration.png)

Weitere Informationen zur Versionierung für EB-Konfigurationen finden Sie unter [Übersicht über die elektronische Berichterstattung (EB)](general-electronic-reporting.md#component-versioning).

> [!NOTE]
> Das konfigurierte Datenmodell ist Ihre abstrakte Darstellung der **Fragebogen**-Geschäftsdomäne und enthält keine Beziehungen zu spezifischen Artefakten in Microsoft Dynamics 365 Finance.

## <a name="design-a-model-mapping-for-the-configured-data-model"></a><a name="DesignMapping"></a>Entwerfen einer Modellzuordnung für das konfigurierte Datenmodell

Als Benutzer in der Rolle des Entwicklers für elektronische Berichterstellung müssen Sie eine neue EB-Konfiguration erstellen, die eine Komponente [Modellabbildung](general-electronic-reporting.md#data-model-and-model-mapping-components) für das Datenmodell **Fragebogen** enthält. Da diese Komponente das konfigurierte Datenmodell für Finanzen implementiert, ist es finanzspezifisch. Sie müssen die Modellzuordnungskomponente so konfigurieren, dass die Anwendungsobjekte angegeben werden, die zum Ausfüllen des konfigurierten Datenmodells mit Anwendungsdaten zur Laufzeit verwendet werden müssen. Um diese Aufgabe durchzuführen, müssen Sie die Implementierungsdetails der Datenstruktur der Geschäftsdomäne **Fragebogen** im Finanzbereich berücksichtigen.

Durch Ausführen der Schritte im Abschnitt [Importieren einer neuen Modellzuordnungskonfiguration](#ImportModelMapping) können Sie die erforderliche Modellzuordungskonfiguration aus der bereitgestellten XML-Datei importieren. Alternativ können Sie mit den Schritten im Abschnitt [Erstellen einer neuen Modellzuordnungskonfiguration](#CreateModelMapping) diese Modellzuordnung neu entwerfen.

### <a name="import-a-new-model-mapping-configuration"></a><a name="ImportModelMapping"></a>Importieren einer neuen Modellzuordnungskonfiguration

1. Laden Sie die Datei [Questionnaires mapping.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) herunter und speichern Sie sie auf Ihrem lokalen Computer.
2. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
3. Wählen Sie im Arbeitsbereich **Elektronische Berichterstellung** die Option **Berichterstellungskonfigurationen** aus.
4. Wählen Sie im Aktivitätsbereich **Austausch** \> **Aus XML-Datei laden** aus.
5. Klicken Sie auf **Durchsuchen** und wählen Sie die Datei **Questionnaires mapping.version.1.1.xml** aus.
6. Wählen Sie **OK** aus, um die Konfiguration zu importieren.

Überspringen Sie den nächsten Vorgang, um fortzufahren. [Erstellen einer neuen Datenmodellkonfiguration](#CreateModelMapping).

### <a name="create-a-new-model-mapping-configuration"></a><a name="CreateModelMapping"></a>Erstellen einer neuen Modellzuordnungskonfiguration

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Wählen Sie auf der Seite **Konfigurationen** im Konfigurationsbaum **Fragebogenmodell** aus.
3. Wählen Sie **Konfiguration erstellen**.
4. Führen Sie im Drop-Down-Dialogfeld die folgenden Schritte aus:

    1. Wählen Sie im Feld **Neu** die Option **Modellzuordnung basierend auf Datenmodellfragebogen**.
    2. Geben Sie im Feld **Name** **Fragebogenzuordnung** ein.
    3. Wählen Sie im Feld **Datenmodelldefinition** die Definition **Stamm** aus.
    4. Wählen Sie **Konfiguration erstellen** aus, um die Konfiguration zu erstellen.

#### <a name="design-a-new-model-mapping-component"></a><a name="DesignMappingComponent"></a>Entwerfen einer neuen Modellzuordnungskomponente

1. Wählen Sie auf der Seite **Konfigurationen** im Konfigurationsbaum **Fragebogenzuordnung** aus.
2. Wählen Sie **Designer** aus, um die Liste der Zuordnungen zu öffnen.
3. Wählen Sie die Zuordnung **Fragebogenzuordnung** aus, die automatisch für die Definition **Stamm** hinzugefügt wurden
4. Wählen Sie **Designer**, um mit der Konfiguration der ausgewählten Zuordnung zu beginnen.

Für die Definition **Stamm** wird automatisch eine neue Zuordnung hinzugefügt. Diese Zuordnung hat die Richtung **Zum Modell**. Daher kann diese Zuordnung verwendet werden, um ein Datenmodell mit den erforderlichen Daten zu füllen.

#### <a name="add-data-sources-to-access-application-tables"></a><a name="AddMmDataSource1"></a>Hinzufügen von Datenquellen für den Zugriff auf Anwendungstabellen

Sie müssen Datenquellen konfigurieren, um auf die Anwendungstabellen zuzugreifen, die Fragebogendetails enthalten.

1. Wählen Sie auf der Seite **Modellzuordnungsdesigner** im Bereich **Datenquellentypen** die Option **Dynamics 365 for Operations\\ Tabellendatensätze** aus.
2. Fügen Sie eine neue Datenquelle hinzu, die für den Zugriff auf die KMCollection-Tabelle verwendet wird, wobei jeder Datensatz einen einzelnen Fragebogen darstellt:

    1. Wählen Sie **Stamm hinzufügen** im Bereich **Datenquellen** aus.
    2. Geben Sie im Dialogfeld im Feld **Name** den Eintrag **Fragebogen** ein.
    3. Geben Sie im Feld **Tabelle** den Eintrag **KMCollection** ein.
    4. Setzen Sie die Option **Abfrage anfordern** auf **Ja**. Sie können zur Laufzeit dann Optionen von [Filtern](../../fin-ops/get-started/advanced-filtering-query-options.md) für diese Tabelle im Systemabfrage-Dialogfeld angeben.
    5. Wählen Sie **OK** aus, um die neue Datenquelle hinzuzufügen.

3. Wählen Sie im Bereich **Datenquellentypen** den Eintrag **Dynamics 365 for Operations\\Tabellendatensätze** aus.
4. Fügen Sie eine neue Datenquelle hinzu, die für den Zugriff auf die KMQuestion-Tabelle verwendet wird, wobei jeder Datensatz eine einzelne Frage in einem Fragebogen darstellt:

    1. Wählen Sie **Stamm hinzufügen** im Bereich **Datenquellen** aus.
    2. Geben Sie im Dialogfeld im Feld **Name** den Eintrag **Frage** ein.
    3. Geben Sie im Feld **Tabelle** den Eintrag **KMQuestion** ein.
    4. Wählen Sie **OK** aus, um die neue Datenquelle hinzuzufügen.

5. Wählen Sie im Bereich **Datenquellentypen** den Eintrag **Dynamics 365 for Operations\\Tabellendatensätze** aus.
6. Fügen Sie einen neuen Datenquellenversuch hinzu, der für den Zugriff auf die KMAnswer-Tabelle verwendet wird, wobei jeder Datensatz eine einzelne Antwort auf eine Frage in einem Fragebogen darstellt:

    1. Wählen Sie **Stamm hinzufügen** im Bereich **Datenquellen** aus.
    2. Geben Sie im Feld **Name** die Bezeichnung **Antwort** ein.
    3. Geben Sie im Feld **Tabelle** den Eintrag **KMAnswer** ein.
    4. Wählen Sie **OK** aus, um die neue Datenquelle hinzuzufügen.

7. Wählen Sie im Bereich **Datenquellentypen** den Eintrag **Funktionen\\Berechnetes Feld** aus.
8. Fügen Sie ein neues berechnetes Feld hinzu, mit dem aus jedem Datensatz der übergeordneten KMQuestionResultGroup-Tabelle aus jedem Datensatz der übergeordneten KMCollection-Tabelle zugegriffen wird:

    1. Wählen Sie **Fragebogen** im Bereich **Datenquellen** aus.
    2. Wählen Sie **Hinzufügen** aus.
    3. Geben Sie im Dialogfeld im Feld **Name** den Eintrag **\$ResultGroup** ein.
    4. Wählen Sie **Formel bearbeiten** aus.
    5. Geben Sie im [EB-Formeleditor](general-electronic-reporting-formula-designer.md) im Feld **Formel** den Eintrag **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)** ein, um den [Pfad](er-formula-language.md#paths) der 1:n-Beziehung zwischen den KMCollection- und KMQuestionResultGroup-Tabellen zu verwenden.
    6. Klicken Sie auf **Speichern** und schließen Sie den Formeleditor.
    7. Wählen Sie **OK** aus, um das neue berechnete Feld hinzuzufügen.

9. Wählen Sie im Bereich **Datenquellentypen** den Eintrag **Funktionen\\Berechnetes Feld** aus.
10. Fügen Sie ein neues berechnetes Feld hinzu, mit dem auf Fragendatensätze der KMQuestion-Tabelle aus jedem Datensatz der übergeordneten KMCollectionQuestion-Tabelle zugegriffen wird:

    1. Wählen Sie **Fragebogen** im Bereich **Datenquellen** aus.
    2. Erweitert Sie den Knoten **\<Beziehungen**, der 1:n-Beziehungen der KMCollection-Tabelle enthält.
    3. Wählen Sie die entsprechende Tabelle **KMCollectionQuestion** und dann **Hinzufügen** aus.
    4. Geben Sie im Dialogfeld im Feld **Name** den Eintrag **\$Frage** ein.
    5. Wählen Sie **Formel bearbeiten** aus.
    6. Geben Sie im Formeleditor im Feld **Formel** den Eintrag **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** ein, um die entsprechenden Fragendatensätze aus der KMQuestion-Tabelle zurückzugeben.
    7. Klicken Sie auf **Speichern** und schließen Sie den Formeleditor.
    8. Wählen Sie **OK** aus, um das neue berechnete Feld hinzuzufügen.

11. Wählen Sie im Bereich **Datenquellentypen** den Eintrag **Funktionen\\Berechnetes Feld** aus.
12. Fügen Sie ein neues berechnetes Feld hinzu, mit dem auf Antwortdatensätze der KMAnswer-Tabelle aus jedem Datensatz der übergeordneten KMQuestion-Tabelle zugegriffen wird:

    1. Wählen Sie im Bereich **Datenquellen** den Eintrag **Questionnaire.\<Relations.KMCollectionQuestion.\$Question** und dann **Hinzufügen** aus.
    2. Geben Sie im Dialogfeld im Feld **Name** den Eintrag **\$Antwort** ein.
    3. Wählen Sie **Formel bearbeiten** aus.
    4. Geben Sie im Formeleditor im Feld **Formel** den Eintrag **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)**, um die entsprechenden Antwortdatensätze aus der KMAnswer-Tabelle zurückzugeben.
    5. Klicken Sie auf **Speichern** und schließen Sie den Formeleditor.
    6. Wählen Sie **OK** aus, um das neue berechnete Feld hinzuzufügen.

13. Wählen Sie im Bereich **Datenquellentypen** den Eintrag **Dynamics 365 for Operations\\Table** aus.
14. Fügen Sie eine neue Datenquelle hinzu, die für den Zugriff auf Methoden der CompanyInfo-Tabelle verwendet wird. Beachten Sie, dass die Methode **find()** dieser Tabelle einen Datensatz zurück, der für ein Unternehmen der aktuellen Finanzinstanz steht, in dessen Kontext diese Zuordnung aufgerufen wird.

    1. Wählen Sie **Stamm hinzufügen** im Bereich **Datenquellen** aus.
    2. Geben Sie im Dialogfeld im Feld **Name** den Eintrag **CompanyInfo** ein.
    3. Geben Sie im Feld **Tabelle** den Eintrag **CompanyInfo** ein.
    4. Wählen Sie **OK** aus, um die neue Datenquelle hinzuzufügen.

#### <a name="add-data-sources-to-access-application-enumerations"></a><a name="AddMmDataSource2"></a>Hinzufügen von Datenquellen für den Zugriff auf Anwendungsaufzählungen

Sie müssen Datenquellen konfigurieren, um auf Anwendungsaufzählungen zuzugreifen und deren Werte mit den Werten der Felder des Typs **Aufzählung** in den Anwendungstabellen zu vergleichen. Sie müssen das Ergebnis des Vergleichs verwenden, um die entsprechenden Felder des Datenmodells auszufüllen.

1. Wählen Sie auf der Seite **Modellzuordnungsdesigner** im Bereich **Datenquellentypen** den Eintrag **Dynamics 365 for Operations\\ Aufzählung** aus.
2. Fügen Sie eine neue Datenquelle hinzu, mit der auf die Werte der Aufzählung **EnumAppNoYes** zugegriffen wird:

    1. Wählen Sie **Stamm hinzufügen** im Bereich **Datenquellen** aus.
    2. Geben Sie im Dialogfeld im Feld **Name** den Eintrag **EnumAppNoYes** ein.
    3. Geben Sie im Feld **Aufzählung** den Eintrag **NoYes** ein.
    4. Wählen Sie **OK** aus, um die neue Datenquelle hinzuzufügen.

3. Wählen Sie im Bereich **Datenquellentypen** den Eintrag **Dynamics 365 for Operations\\ Aufzählung** aus.
4. Fügen Sie eine neue Datenquelle hinzu, mit der auf die Werte der Aufzählung **KMCollectionQuestionMode** zugegriffen wird:

    1. Wählen Sie **Stamm hinzufügen** im Bereich **Datenquellen** aus.
    2. Geben Sie im Drop-Down-Dialogfeld im Feld **Name** den Eintrag **EnumAppQuestionOrder** ein.
    3. Geben Sie im Feld **Aufzählung** den Eintrag **KMCollectionQuestionMode** ein.
    4. Wählen Sie **OK** aus, um die neue Datenquelle hinzuzufügen.

#### <a name="add-er-labels-to-generate-a-report-in-a-specified-language"></a><a name="AddMmLabels"></a>Hinzufügen von EB-Beschriftungen, um einen Bericht in einer bestimmten Sprache zu erzeugen

Sie können EB-Beschriftungen hinzufügen, um einige Ihrer Datenquellen so zu konfigurieren, dass Werte zurückgegeben werden, die von der Sprache abhängen, die im Kontext des Aufrufs der Modellzuordnung definiert ist.

1. Wählen Sie auf der Seite **Modellzuordnungsdesigner** im Bereich **Datenquellen** den Eintrag **Antworten** und dann **Bearbeiten** aus.
2. Aktivieren Sie das Feld **Beschriftung**.
3. Wählen Sie **Übersetzen** aus.
4. Führen Sie im Dialogfeld **Textübersetzung** die folgenden Schritte aus:

    1. Geben Sie im Feld **Beschriftungskennung** den Wert **PositiveAnswer** ein.
    2. Geben Sie im Feld **Text in Standardsprache** den Eintrag **Ja** ein.
    3. Wählen Sie **Übersetzen** aus.
    4. Geben Sie im Feld **Beschriftungskennung** den Eintrag **NegativeAnswer** ein.
    5. Geben Sie im Feld **Text in Standardsprache** den Eintrag **Nein** ein.
    6. Wählen Sie **Übersetzen** aus.

5. Schließen Sie das Dialogfeld **Textübersetzung**.
6. Wählen Sie **Abbrechen** aus.

![Hinzufügen von EB-Beschriftungen für die bearbeitbare Modellzuordnung](./media/er-quick-start1-adding-labels.png)

Sie haben EB-Beschriftungen nur für die Standardsprache eingegeben. Informationen darüber, wie EB-Etiketten in andere Sprachen übersetzt werden können, finden Sie unter [Entwerfen mehrsprachiger Berichte](er-design-multilingual-reports.md).

#### <a name="add-a-data-source-to-transform-the-results-of-comparing-enumeration-values-to-a-text-value"></a><a name="AddMmDataSource3"></a>Hinzufügen einer Datenquelle, um die Ergebnisse des Vergleichs von Aufzählungswerten mit einem Textwert

Da Sie die Ergebnisse des Vergleichs zwischen Aufzählungswerten und Textwerten für Differenzquellen mehrmals transformieren müssen, empfiehlt es sich, diese Logik als einzelne Datenquelle zu konfigurieren. Um diese Datenquelle jedoch wiederverwendbar zu machen, müssen Sie sie dann als parametrisierte Datenquelle konfigurieren. Weitere Informationen finden Sie unter [Unterstützung für Parameter bei Aufrufen von EB-Datenquellen des Feldtyps "Berechnet"](er-calculated-field-type.md).

1. Wählen Sie auf der Seite **Modellzuordnungsdesigner** im Feld **Datenquellentypen** den Eintrag **Allgemein\\Leerer Container** aus.
2. Hinzufügen einer neuen Container-Datenquelle;

    1. Wählen Sie **Stamm hinzufügen** im Bereich **Datenquellen** aus.
    2. Geben Sie im Dialogfeld im Feld **Name** den Eintrag **Helper** ein.
    3. Wählen Sie **OK** aus, um die neue Container-Datenquelle hinzuzufügen.

3. Wählen Sie im Bereich **Datenquellentypen** den Eintrag **Funktionen\\Berechnetes Feld** aus.
4. Hinzufügen einer neuen Datenquelle:

    1. Wählen Sie im Bereich **Datenquellen** den Eintrag **Helper** aus.
    2. Wählen Sie **Hinzufügen** aus.
    3. Geben Sie im Drop-Down-Dialogfeld im Feld **Name** den Eintrag **NoYesEnumToString** ein.
    4. Wählen Sie **Formel bearbeiten** aus.
    5. Wählen Sie im Formeleditor **Parameter** aus.
    6. Führen Sie die folgenden Schritte aus, um Parameter für den konfigurierten Ausdruck anzugeben:

        1. Wählen Sie **Neu** aus.
        2. Geben Sie im Dialogfeld im Feld **Name** den Eintrag **Argument** ein.
        3. Wählen Sie im Feld **Typ** den Datentyp **Boolesch** aus.
        4. Wählen Sie **OK**.

    7. Geben Sie im Feld **Formel** den Eintrag **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")**, um den Text des entsprechenden EB-Labels einzugeben. Dies hängt von der Sprache des Ausführungskontexts und von dem Wert des angegebenen Parameters ab.
    8. Klicken Sie auf **Speichern** und schließen Sie den Formeleditor.
    9. Wählen Sie **OK** aus, um die neue Datenquelle hinzuzufügen.

![Konfigurierte Modellzuordnung im EB-Modellzuordnungsdesigner](./media/er-quick-start1-added-data-sources.png)

#### <a name="bind-data-sources-to-data-model-fields"></a><a name="AddMmBindings1"></a>Binden von Datenquellen an Datenmodellfelder

Sie müssen die konfigurierten Datenquellen an die Felder des Datenmodells binden, um anzugeben, wie das Datenmodell zur Laufzeit mit Anwendungsdaten gefüllt wird.

1. Wählen Sie auf der Seite **Modelzuordnungsdesigner** im Bereich **Datenmodell** den Eintrag **CompanyName** aus.
2. Erweitern Sie im Bereich **Datenquellen** den Eintrag **CompanyInfo** und führen Sie dann die folgenden Schritte durch:

    1. Erweitern Sie den Knoten **CompanyInfo.find()**, der für die Methode **find()** der CompanyInfo-Tabelle steht.
    2. Wählen Sie **CompanyInfo.find (). Name** aus.
    3. Wählen Sie **Binden**, um den Namen des Unternehmens einzugeben, für das die konfigurierte Modellzuordnung zur Laufzeit aufgerufen wird.

3. Wählen Sie **Fragebogen** im Bereich **Datenmodell** aus.
4. Wählen Sie im Bereich **Datenquellen** den Eintrag **Fragebogen** und dann **Binden** aus, um die Felder des Fragebogens auszufüllen.
5. Erweitern Sie im Bereich **Datenmodell** den Eintrag **Fragebogen** und führen Sie dann die folgenden Schritte durch:

    1. Wählen Sie **Aktiv** im Bereich **Datenmodell** aus.
    2. Wählen Sie **Bearbeiten** im Bereich **Datenmodell** aus.
    3. Geben Sie im Feld **Formel** den Eintrag **Helper.NoYesEnumToString ( \@.Active = EnumAppNoYes.Yes)** ein, um das text- und sprachabhängige Ergebnis des Vergleichs zwischen Aufzählungswerten zu füllen.

6. Binden Sie Datenquellen weiterhin auf dieselbe Weise an Datenmodellfelder, bis Sie das folgende Ergebnis erzielen.

    | Feldpfad                                              | Datentyp   | Vorgang | Bindungsausdruck |
    |---------------------------------------------------------|-------------|--------|--------------------|
    | CompanyName                                             | Zeichenfolge      | Binden   | CompanyInfo.'find()'.Name |
    | Fragebogen                                           | Datensatzliste | Binden   | Fragebogen |
    | Fragebogen\\Aktiv                                   | Zeichenfolge      | Bearbeiten   | Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes) |
    | Fragebogen\\Code                                     | Zeichenfolge      | Binden   | \@.kmCollectionId |
    | Fragebogen\\Beschreibung                              | Zeichenfolge      | Binden   | \@.Description |
    | Fragebogen\\QuestionnaireType                        | Zeichenfolge      | Binden   | \@.'&gt;Relations'.kmCollectionTypeId.Description |
    | Fragebogen\\QuestionOrder                            | Zeichenfolge      | Bearbeiten   | CASE (\@.questionMode,<br>EnumAppQuestionOrder.Conditional, "Conditional",<br>EnumAppQuestionOrder.Random, "Zufällig (Prozentsatz im Fragebogen)",<br>EnumAppQuestionOrder.RandomGroup, "Zufällig (Prozentsatz in Ergebnisgruppen)",<br>EnumAppQuestionOrder.Sequence, "Sequenziell",<br>"") |
    | Fragebogen\\ResultsGroup                             | Aufzeichnen      |        | |
    | Fragebogen\\ResultsGroup\\Code                       | Zeichenfolge      | Binden   | \@. ' \$ResultGroup'.kmQuestionResultGroupId |
    | Fragebogen\\ResultsGroup\\Beschreibung                | Zeichenfolge      | Binden   | \@.'\$ResultGroup'.description |
    | Fragebogen\\ResultsGroup\\MaxNumberOfPoints          | Gleitkommazahl        | Binden   | \@.'\$ResultGroup'.maxPoint |
    | Fragebogen\\Frage                                 | Datensatzliste | Binden   | \@.'&lt;Relations'.KMCollectionQuestion |
    | Fragen\\Frage\\CollectionSequenceNumber       | Ganzzahl     | Binden   | \@.answerCollectionSequenceNumber |
    | Fragebogen\\Frage\\ID                             | Zeichenfolge      | Binden   | \@.kmQuestionId |
    | Fragebogen\\Frage\\MustBeCompleted                | Zeichenfolge      | Bearbeiten   | Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes) |
    | Fragebogen\\Frage\\PrimaryQuestion                | Zeichenfolge      | Binden   | \@.parentQuestionId |
    | Fragebogen\\Frage\\SequenceNumber                 | Ganzzahl     | Binden   | \@.SequenceNumber |
    | Fragebogen\\Frage\\Text                           | Zeichenfolge      | Binden   | \@.'\$Question'.text |
    | Fragebogen\\Frage\\Antwort                         | Datensatzliste | Binden   | \@.'\$Question'.'\$Answer' |
    | Fragebogen\\Frage\\Antwort\\CorrectAnswer          | Zeichenfolge      | Bearbeiten   | Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes) |
    | Fragebogen\\Frage\\Antwort\\Punkte                 | Gleitkommazahl        | Binden   | \@.point |
    | Fragebogen\\Frage\\Antwort\\SequenceNumber         | Ganzzahl     | Binden   | \@.sequenceNumber |
    | Fragebogen\\Frage\\Antwort\\Text                   | Zeichenfolge      | Binden   | \@.text |

    Die folgende Abbildung zeigt den Endzustand der konfigurierten Modellzuordnung auf der Seite **Modellzuordnungsdesigner**.

    ![Vollkonfigurierte Modellzuordnung im EB-Modellzuordnungsdesigner](./media/er-quick-start1-mapping2.png)

7. Speichern Sie die Änderungen.
8. Schließen Sie die Seite **Modellzuordnungsdesigner**.

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping"></a>Vervollständigen des Designs der Modellzuordnung

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Wählen Sie auf der Seite **Konfigurationen** im Konfigurationsbaum **Fragebogenzuordnung** aus.
3. Wählen Sie im Inforegister **Versionen** die Konfigurationsversion mit dem Status **Entwurf** aus.
4. Wählen Sie **Status ändern** \> **Abgeschlossen**.

Der Status von Version 1.1 dieser Konfiguration wird von **Entwurf** zu **Abgeschlossen** geändert. Version 1.1 kann nicht mehr geändert werden. Diese Version enthält das konfigurierte Modellzuordnung und kann als Basis für andere EB-Konfigurationen verwendet werden. Version 1.2 dieser Konfiguration wird erstellt und hat den Status **Entwurf**. Sie können diese Version bearbeiten, um die Konfiguration **Fragebogenzuordnung** anzupassen.

![Versionen der bearbeitbaren EB-Konfiguration auf der Seite "Konfigurationen"](./media/er-quick-start1-mapping-configuration.png)

> [!NOTE]
> Die konfigurierte Modellzuordnung ist Ihre finanzspezifische Implementierung des abstrakten Datenmodells, das die Geschäftsdomäne **Fragebogen** darstellt.

## <a name="design-a-template-for-a-custom-report"></a><a name="DesignReportTemplate"></a>Entwerfen einier Vorlage für einen benutzerdefinierten Bericht

Das EB-Framework verwendet vordefinierte Vorlagen, um Berichte in Microsoft Office-Formaten zu generieren (Excel-Arbeitsmappen oder Word-Dokumente) zu erstellen. Während der Erstellung des erforderlichen Berichts wird eine Vorlage mit den erforderlichen Daten gemäß dem konfigurierten Datenfluss ausgefüllt. Daher müssen Sie zuerst eine Vorlage für Ihren benutzerdefinierten Bericht entwerfen. Diese Vorlage muss als Excel-Arbeitsmappe konzipiert sein, deren Struktur das Layout eines benutzerdefinierten Berichts darstellt. Sie müssen jedes Excel-Element benennen, das Sie mit den erforderlichen Daten füllen möchten.

1. Laden Sie die Datei [Questionnaires report template.xslx](https://go.microsoft.com/fwlink/?linkid=851448) herunter und speichern Sie sie auf Ihrem lokalen Computer.
2. Öffnen Sie die Datei in Excel und überprüfen Sie die Struktur der Arbeitsmappe.

Wie die folgende Abbildung zeigt, wurde die heruntergeladene Vorlage so gestaltet, dass bestimmte Fragebögen gedruckt werden, in denen die Fragen eines Fragebogens zusammen mit den entsprechenden Antworten dargestellt werden.

![Excel-Vorlage zum Drucken bestimmter Fragebögen](./media/er-quick-start1-template-layout.png)

Zu dieser Vorlage wurden Excel-Namen hinzugefügt, um die Details des Fragebogens auszufüllen. Mit dem Namensmanager können Sie die Excel-Namen überprüfen.

![Verwenden des Namensmanagers zum Überprüfen von Excel-Namen in der bereitgestellten Excel-Vorlage](./media/er-quick-start1-template-names.png)

Berichtsbezeichnungen wurden als fester Text in englischer Sprache hinzugefügt. Sie können die Berichtsbeschriftungen durch neue Excel-Namen ersetzen, die die Beschriftungen mit sprachabhängigem Text ausfüllen, indem Sie das EB-Format verwenden [Beschriftungen](#AddMmLabels), wie Sie es für sprachabhängige Ausdrücke in der konfigurierten Modellzuordnung getan haben. In diesem Fall müssen EB-Beschriftungen im bearbeitbaren EB-Format hinzugefügt werden.

Wie die folgende Abbildung zeigt, wurde der benutzerdefinierte Berichtskopf angegeben, damit Excel Paging ausführen kann.

![Benutzerdefinierter Berichtskopf in der bereitgestellten Excel-Vorlage](./media/er-quick-start1-template-header.png)

## <a name="design-a-format"></a><a name="DesignFormat"></a>Entwerfen eines Formats

Als Benutzer in der Rolle des Electronic Reporting Functional Consultant müssen Sie eine neue EB-Konfiguration erstellen, die eine Komponente [Format](general-electronic-reporting.md#FormatComponentOutbound) enthält. Sie müssen die Formatkomponente konfigurieren, um anzugeben, wie eine Berichtsvorlage zur Laufzeit mit den erforderlichen Daten gefüllt wird.

Durch Ausführen der Schritte im Abschnitt [Importieren einer entworfenen Formatkonfiguration](#FormatImport) können Sie das erforderliche Format aus der bereitgestellten XML-Datei importieren. Alternativ können Sie mit den Schritten im Abschnitt [Erstellen einer neuen Formatkonfiguration](#FormatCreate) dieses Format neu entwerfen.

### <a name="import-a-designed-format-configuration"></a><a name="FormatImport"></a>Importieren einer entworfenen Formatkonfiguration

1. Laden Sie die Datei [Questionnaires format.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) herunter und speichern Sie sie auf Ihrem lokalen Computer.
2. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
3. Wählen Sie im Arbeitsbereich **Elektronische Berichterstellung** die Option **Berichterstellungskonfigurationen** aus.
4. Wählen Sie im Aktivitätsbereich **Austausch** \> **Aus XML-Datei laden** aus.
5. Klicken Sie auf **Durchsuchen** und wählen Sie die Datei **Questionnaires format.version.1.1.xml** aus.
6. Wählen Sie **OK** aus, um die Konfiguration zu importieren.

Überspringen Sie den nächsten Vorgang, um fortzufahren. [Erstellen einer neuen Formatkonfiguration](#FormatCreate).

### <a name="create-a-new-format-configuration"></a><a name="FormatCreate"></a>Dient zum Erstellen einer neuen Format-Konfiguration.
 
1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Wählen Sie auf der Seite **Konfigurationen** im Konfigurationsbaum **Fragebogenmodell** aus.
3. Wählen Sie **Konfiguration erstellen**.
4. Führen Sie im Drop-Down-Dialogfeld die folgenden Schritte aus:

    1. Wählen Sie im Feld **Neu** die Option **Format basierend auf Datenmodellfragebogen**.
    2. Geben Sie im Feld **Name** den Eintrag **Fragebogenbericht** ein.
    3. Wählen Sie im Feld **Datenmodellversion** den Eintrag **1** aus.

        > [!NOTE]
        > - Wenn Sie eine bestimmte Version des Basisdatenmodells auswählen, wird Ihnen die Struktur der entsprechenden Version des Datenmodells als Struktur der Datenquelle **Modell** im erstellten Format dargestellt.
        > - Dieses Feld muss nicht ausgefüllt werden. In diesem Fall wird die Struktur der Version **Entwurf** des Datenmodells als Struktur der Datenquelle **Modell** in dem von Ihnen erstellten Format dargestellt. Sie können dann Ihr Modell anpassen und diese Anpassungen sofort in Ihrem Format anzeigen. Dieser Ansatz kann die Effizienz des EB-Lösungsdesigns verbessern, wenn Sie Ihr Datenmodell, Ihre Modellzuordnung und Ihr Format gleichzeitig konfigurieren.
        > - Wenn Sie eine bestimmte Version des Basisdatenmodells auswählen, können Sie später zur Verwendung der Version **Entwurf** wechseln, wenn Sie mit der Bearbeitung eines Formats beginnen.

    4. Wählen Sie im Feld **Datenmodelldefinition** die Definition **Stamm** aus.

5. Wählen Sie **Konfiguration erstellen** aus, um die Konfiguration zu erstellen.

#### <a name="import-a-report-template"></a><a name="ImportReportTemplate"></a>Importieren einer Berichtvorlage

1. Wählen Sie auf der Seite **Konfigurationen** im Konfigurationsbaum **Fragebogenbericht** aus.
2. Wählen Sie **Designer** aus, um ein benutzerdefiniertes Format zu konfigurieren.
3. Wählen Sie auf der Seite **Formatdesigner** im Aktivitätsbereich **Importieren** \> **Aus Excel importieren** aus.
4. Führen Sie im Dialogfeld die folgenden Schritte aus:

    1. Wählen Sie **Vorlage hinzufügen** aus.
    2. Suchen und wählen Sie die lokal gespeicherte Datei **Questionnaires report template.xslx**und dann **Öffnen** aus.
    3. Wählen Sie **OK** aus, um die Vorlage zu importieren.

    ![Importieren einer Berichtvorlage](./media/er-quick-start1-template-import.png)

Das Formatelement **Excel\\Datei** wird automatisch als Stammelement in das bearbeitbare Format eingefügt. Zusätzlich wird entweder das Formatelement **Excel\\Bereich** oder das Formatelement **Excel\\Zelle** automatisch für jeden erkannten Excel-Namen der importierten Vorlage hinzugefügt. Das Format **Excel\\Header**, in dem das verschachtelte Element **String** enthalten ist, wird automatisch entsprechend der Header-Einstellung der importierten Vorlage hinzugefügt.

![Formatstruktur, die automatisch hinzugefügte Elemente im EB Operation Designer enthält](./media/er-quick-start1-template-import2.png)

#### <a name="configure-a-format"></a><a name="ConfigureFormat"></a>Konfigurieren eines Formats

1. Wählen Sie auf der Seite **Formatdesigner** im Formatbaum das Stammelement **Excel** aus.
2. Geben Sie auf der Registerkarte **Format** rechts auf der Seite im Feld **Name** den Eintrag <a name="AddFormatRootElement"></a>**Bericht** ein.
3. Wählen Sie im Feld **Spracheinstellungen** den Eintrag **Benutzerpräferenz** aus, um den Bericht in der vom Benutzer bevorzugten Sprache auszuführen.
4. Wählen Sie im Feld **Kulturpräferenz** den Eintrag **Benutzerpräferenzen** aus, um den Bericht in der vom Benutzer bevorzugten Kultur auszuführen.

    Informationen zum Festlegen der Sprach- und Kulturkontexte für einen EB-Prozess finden Sie unter [Entwerfen mehrsprachiger Berichte](er-design-multilingual-reports.md).

    ![Konfigurieren der Sprach- und Kultureinstellungen für den erstellten Bericht im ER Operation Designer](./media/er-quick-start1-template-format-structure1.png)

5. Erweitern Sie im Formatbaum den Stammknoten und wählen Sie dann **ResultsGroup** aus.
6. Wählen Sie auf der Registerkarte **Format** im Feld **Replikationsrichtung** den Eintrag **Keine Replikation** aus, weil Sie nicht erwarten, mehrere Ergebnisgruppen für einen einzelnen Fragebogen zu haben.

    ![Definieren der Replikationsrichtung für Elemente im Bereichsformat im ER Operation Designer](./media/er-quick-start1-template-format-structure2.png)

7. Wählen Sie **Speichern** aus.

#### <a name="define-the-data-binding-for-a-report-title"></a><a name="DefineFormatBindings"></a>Definieren Sie die Datenbindung für einen Berichtstitel

Sie müssen eine Datenbindung für ein Formatelement angeben, mit dem der Titel eines generierten Berichts ausgefüllt wird.

1. Wählen Sie auf der Seite **Formatdesigner** auf der Registerkarte **Zuordnung** rechts das Element **Bericht\\ReportTitle** aus.
2. Wählen Sie **Formel bearbeiten** aus.
3. Wählen Sie im Formeleditor **Übersetzen** aus.
4. Führen Sie im Dialogfeld **Textübersetzung** die folgenden Schritte aus:

    1. Geben Sie im Feld **Beschriftungskennung** den Eintrag **ReportTitle** ein.
    2. Geben Sie im Feld **Text in Standardsprache** den Eintrag **Fragebogenbericht** ein.
    3. Wählen Sie **Übersetzen** und dann **Speichern** aus.
    4. Wählen Sie **Übersetzen** aus, um das Dialogfeld **Textübersetzung** zu schließen.

5. Schließen Sie den Formeleditor.

    ![Konfigurieren der Bindung zum Ausfüllen des Titels eines generierten Berichts](./media/er-quick-start1-add-report-title-label.png)

Mit dieser Methode können Sie alle anderen Beschriftungen der aktuellen Vorlagensprache abhängig machen. Informationen dazu, wie die hinzugefügten Beschriftungen einer einzelnen EB-Konfiguration in alle unterstützten Sprachen übersetzt werden können, finden Sie unter [Entwerfen mehrsprachiger Berichte](er-design-multilingual-reports.md).

#### <a name="review-model-data-source"></a><a name="ReviewModelDataSource"></a>Überarbeiten der Modelldatenquelle

1. Wählen Sie auf der Seite **Formatdesigner** auf der Registerkarte **Zuordnung** die Datenquelle <a name="ModelDSName"></a>**Modell** aus, die für das Basisdatenmodell dieses EB-Formats steht.
2. Wählen Sie **Bearbeiten** aus.
3. Überprüfen Sie die Informationen im Dialogfeld **Datenquelleneigenschaften**. Diese Datenquelle steht für die Version 1 des Datenmodell **Fragebögen**, die sich in der EB-Konfiguration **Fragebogenmodell** befinden.

![Eigenschaften der Modelldatenquelle im ER Operation Designer](./media/er-quick-start1-model-data-source.png)

#### <a name="bind-format-elements-to-data-source-fields"></a><a name="BindFormatElements"></a>Binden von Formatelementen an Datenquellenfelder

Um anzugeben, wie eine Vorlage zur Laufzeit ausgefüllt wird, müssen Sie jedes Formatelement, das einem geeigneten Excel-Namen zugeordnet ist, an ein einzelnes Feld der Datenquelle dieses Formats binden.

1. Wählen Sie auf der Seite **Formatdesigner** im Formatbaum das Formatelement **Bericht\\CompanyName**.
2. Wählen Sie auf der Registerkarte **Zuordnung** das Datenquellenfeld **model.CompanyName** des Typs **String** aus.
3. Wählen Sie **Binden** aus, um einen Firmennamen in eine Vorlage einzugeben.
4. Wählen Sie im Formatbaum das Element **Bericht \\Fragebogen** aus.
5. Wählen Sie auf der Registerkarte **Zuordnung** das Datenquellenfeld **model.Questionnaire** des Typs **Zuordnungsliste** aus.
6. Wählen Sie **Bindung** aus.
7. Wählen Sie **Details anzeigen**, um weitere Details für Formatelemente anzuzeigen.

    Das Bereichsformatelement **Fragebogen** ist als vertikal repliziert konfiguriert. Wenn es an einer Datenquelle des Typs **Datensatzliste** gebunden ist, wird der entsprechende Bereich **Fragebogen** der Excel-Vorlage für jeden Datensatz der gebundenen Datenquelle wiederholt.
 
    ![Binden des Fragebogenbereichsformatelements an die entsprechenden Datenquellen der Datensatzliste im ER Operation Designer](./media/er-quick-start1-bindings1.png)

    Weil der Bereich **Fragebogen** der Excel-Vorlage zwischen den Zeilen 5 und 14 definiert ist, werden diese Zeilen für jeden gemeldeten Fragebogen wiederholt.

    ![Zeilen in der Excel-Vorlage, die in einem generierten Bericht für jeden Datensatz der Datenquellen der Datensatzliste wiederholt werden](./media/er-quick-start1-template-questionnaire-range.png)

8. Konfigurieren Sie ähnliche Bindungen für die verbleibenden Formatelemente, wie in der folgenden Tabelle beschrieben.

    > [!NOTE]
    > In dieser Tabelle wird bei den Informationen in der Spalte "Datenquellenpfad" davon ausgegangen, dass die EB-Funktion [relativer Pfad ](relative-path-data-bindings-er-models-format.md) aktiviert ist.

    | Formatelementpfad                                      | Datenquellenpfad |
    |----------------------------------------------------------|------------------|
    | Excel \\ReportTitle                                       | **\@"GER\_LABEL:ReportTitle"** |
    | Excel\\CompanyName                                       | **model.CompanyName** |
    | Excel\\Fragebogen                                     | **model.Questionnaire** |
    | Excel\\Fragebogen\\Aktiv                             | **\@.Active**, wobei **\@** **model.Questionnaire** ist |
    | Excel\\Fragebogen\\Code                               | **\@.Code** |
    | Excel\\Fragebogen\\Beschreibung                        | **\@.Description** |
    | Excel\\Fragebogen\\QuestionnaireType                  | **\@.QuestionnaireType** |
    | Excel\\Fragebogen\\QuestionOrder                      | **\@.QuestionOrder** |
    | Excel\\Fragebogen\\ResultsGroup\\Code\_               | **\@.ResultsGroup.Code** |
    | Excel\\Fragebogen\\ResultsGroup\\Beschreibung\_        | **\@.ResultsGroup.Description** |
    | Excel\\Fragebogen\\ResultsGroup\\MaxNumberOfPoints    | **\@.ResultsGroup.MaxNumberOfPoint** |
    | Excel\\Fragebogen\\Frage                           | **\@.Question** |
    | Excel\\Fragebogen\\Frage\\CollectionSequenceNumber | **\@.CollectionSequenceNumber**, wobei **\@** **model.Questionnaire.Question** ist |
    | Excel\\Fragebogen\\Frage\\ID                       | **\@.Id** |
    | Excel\\Fragebogen\\Fragen\\MustBeCompleted          | **\@.MustBeCompleted** |
    | Excel\\Fragebogen\\Frage\\PrimaryQuestion          | **\@.PrimaryQuestion** |
    | Excel\\Fragebogen\\Frage\\SequenceNumber           | **\@.SequenceNumber** |
    | Excel\\Fragebogen\\Frage\\Text                     | **\@.Text** |
    | Excel\\Fragebogen\\Frage\\Antwort                   | **\@.Answer** |
    | Excel\\Fragebogen\\Frage\\Antwort\\CorrectAnswer    | **\@.CorrectAnswer**, wobei **\@** **model.Questionnaire.Answer** ist |
    | Excel\\Fragebogen\\Frage\\Antwort\\Punkte           | **\@.Points** |
    | Excel\\Fragebogen\\Frage\\Antwort\\Text             | **\@.Text** |

9. Klicken Sie abschließend auf **Speichern**.

Die folgende Abbildung zeigt den Endzustand der konfigurierten Datenbindungen auf der Seite **Formatdesigner**.

![Konfigurierte Datenbindungen im ER Operation Designer](./media/er-quick-start1-bindings2.png)

> [!IMPORTANT]
> Die gesamte Sammlung angegebener Datenquellen und Bindungen stellt eine Formatzuordnungskomponente des konfigurierten Formats dar. Diese Formatzuordnung wird aufgerufen, wenn Sie das konfigurierte Format für die Berichterstellung ausführen.

### <a name="run-a-designed-format-from-er"></a><a name="RunFormatFromER"></a>Verwenden eines entworfenen Formats aus EB

Sie können jetzt ein entworfenes Format für Testzwecke über die Seite **Konfigurationen** ausführen.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur **Zahlungsmodell** und wählen Sie dann **Fragebogenbericht** aus.
3. Wählen Sie **Designer** für die Formatversion mit dem Status **Entwurf** aus.
4. Wählen Sie auf der Seite **Formatdesigner** die Option **Ausführen** aus.
5. Konfigurieren Sie im Dialogfeld **EB-Parameter** im Inforegister **Einzuschließende Datensätze** die Filteroptionen, sodass nur der Fragebogen **SBCCrsExam** inhalten ist.
6. Wählen Sie **OK**, um die Filteroptionen zu bestätigen.
7. Wählen Sie zum Ausführen des Berichts **OK** aus.
8. Prüfen Sie den generierten Bericht.

Über [Standard ](electronic-reporting-destinations.md#default-behavior) wird ein generierter Bericht als Excel-Datei geliefert, die Sie herunterladen können. Die folgenden Abbildungen zeigen zwei Seiten des generierten Berichts im Excel-Format.

![Beispiel eines generierten Berichts im Excel-Format, Seite 1](./media/er-quick-start1-report1a.png)

![Beispiel eines generierten Berichts im Excel-Format, Seite 2](./media/er-quick-start1-report1b.png)

## <a name="tune-a-designed-format"></a><a name="TuneFormat"></a>Anpassen eines entworfenes Format

### <a name="modify-a-format-to-change-the-name-of-a-generated-document"></a><a name="ModifyToChangeName"></a>Ändern eines Formats, um den Namen eines generierten Dokuments zu ändern

Standardmäßig wird ein generiertes Dokument unter Verwendung des Alias des aktuellen Benutzers benannt. Durch Ändern des Formats können Sie dieses Verhalten so ändern, dass ein generiertes Dokument basierend auf Ihrer benutzerdefinierten Logik benannt wird. Der Name eines generierten Dokuments kann beispielsweise auf dem aktuellen Sitzungsdatum und der aktuellen Sitzungszeit sowie auf dem Titel des Berichts basieren.

1. Wählen Sie auf der Seite **Formatdesigner** das Stammobjekt **Bericht** aus.
2. Wählen Sie auf der Registerkarte **Zuordnung** den Eintrag **Dateinamen bearbeiten** aus.
3. Geben Sie im Feld **Formel** den Eintrag **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "JJJJ-MM-TT SS-MM-SS"))** ein.
4. Klicken Sie auf **Speichern** und schließen Sie den Formeleditor.
5. Wählen Sie **Speichern** aus.

### <a name="modify-a-format-to-change-the-order-of-questions"></a><a name="ModifyToOrder"></a>Ändern eines Formats, um die Abfolge von Fragen zu ändern

Die Fragen sind in einem generierten Bericht nicht richtig geordnet. Sie können die Reihenfolge ändern, indem Sie das Format ändern.

1. Wählen Sie auf der Seite **Formatdesigner** das Stammobjekt **Bericht** aus.
2. Erweitern Sie auf der Registerkarte **Zuordnung** in der Formatstruktur **Bericht\\Fragebogen\\Frage**.

    ![Fragenformatelement des Bereichstyps im ER Operation Designer](./media/er-quick-start1-bindings3.png)

3. Wählen Sie auf der Registerkarte **Zuordnung** den Eintrag **model.Questionnaire** aus.
4. Wählen Sie **Hinweis** \> **Funktionen\\Berechnetes Feld** aus und geben Sie im Feld **Name** den Eintrag **OrderedQuestions** ein.
5. Wählen Sie **Formel bearbeiten** aus.
6. Geben Sie im Formeleditor im Feld **Formel** den Eintrag **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** ein, um die Liste der Fragen des aktuellen Fragebogens nach der laufenden Nummer zu ordnen.
7. Klicken Sie auf **Speichern** und schließen Sie den Formeleditor.
8. Wählen Sie **OK** aus, um die Eingabe eines neuen berechneten Feldes abzuschließen.
9. Wählen Sie auf der Registerkarte **Zuordnung** den Eintrag **model.Questionnaire.OrderedQuestions** aus.
10. Wählen Sie in der Formatstruktur **Excel\\Fragebogen\\Frage** aus.
11. Wählen Sie **Binden** aus und bestätigen Sie dann, dass der aktuelle Pfad **model.Questionnaire.Questions** in allen Bindungen verschachtelter Elemente durch den neuen Pfad **model.Questionnaire.OrderedQuestions** ersetzt wird.
12. Wählen Sie **Speichern** aus.

![Binden des Fragenformatelements an die konfigurierte OrderedQuestions-Datenquelle im ER Operation Designer](./media/er-quick-start1-bindings4.png)

### <a name="run-a-modified-format-from-er"></a><a name="RunFormatFromER2"></a>Verwenden eines geänderten Formats aus EB

Sie können jetzt ein geändertes Format zu Testzwecken über das EB-Framework ausführen.

1. Wählen Sie auf der Seite **Formatdesigner** die Option **Ausführen** aus.
2. Konfigurieren Sie im Dialogfeld **EB-Parameter** im Inforegister **Einzuschließende Datensätze** die Filteroptionen, sodass nur der Fragebogen **SBCCrsExam** inhalten ist.
3. Wählen Sie **OK**, um die Filteroptionen zu bestätigen.
4. Wählen Sie zum Ausführen des Berichts **OK** aus.
5. Prüfen Sie den generierten Bericht.

Die folgende Abbildung zeigt einen generierten Bericht im Excel-Format, in dem die Fragen korrekt sortiert sind.

![Generierter Bericht im Excel-Format mit korrekt geordneten Fragen](./media/er-quick-start1-report2.png)

### <a name="complete-the-format-design"></a><a name="CompleteFormat"></a>Abschließen des Formatentwurfs

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur **Zahlungsmodell** und wählen Sie dann **Fragebogenbericht** aus.
3. Wählen Sie im Inforegister **Versionen** die Konfigurationsversion mit dem Status **Entwurf** aus.
4. Wählen Sie **Status ändern** \> **Abgeschlossen**.

Der Status von Version 1.1 dieser Konfiguration wird von **Entwurf** zu **Abgeschlossen** geändert. Version 1.1 kann nicht mehr geändert werden. Diese Version enthält das konfigurierte Format und kann zum Drucken Ihres benutzerdefinierten Berichts verwendet werden. Version 1.2 dieser Konfiguration wird erstellt und hat den Status **Entwurf**. Sie können diese Version bearbeiten, um das Format Ihres Berichts **Fragebogen** anzupassen.

![Versionen der bearbeitbaren EB-Konfiguration auf der Seite "Konfigurationen"](./media/er-quick-start1-format-configuration.png)

> [!NOTE]
> Das konfigurierte Format ist Ihr Design des Berichts **Fragebogen** und es enthält keine Beziehungen zu den finanzspezifischen Artefakten.

## <a name="develop-application-artefacts-to-call-the-designed-report"></a><a name="DevelopCustomCode"></a>Entwickeln von Anwendungsartefakten, um den entworfenen Bericht aufzurufen

Als Benutzer in der Rolle "Systemadministrator" müssen Sie eine neue Logik entwickeln, damit das konfigurierte EB-Format über die Benutzeroberfläche der Anwendung aufgerufen werden kann, um Ihren benutzerdefinierten Bericht zu generieren. Derzeit bietet EB keine Möglichkeit zum Konfigurieren dieser Art von Logik. Daher sind einige technische Arbeiten erforderlich. 

Zum Entwickeln der neuen Logik müssen Sie eine Topologie bereitstellen, die einen fortlaufenden Build unterstützt . Weitere Informationen finden Sie unter  [Bereitstellen von Topologien, die fortlaufenden Build und Testautomatisierung unterstützen](../perf-test/continuous-build-test-automation.md) Sie unter. Sie müssen zudem Zugriff auf die Entwicklungsumgebung für diese Topologie haben. Weitere Informationen zur verfügbaren ER API finden Sie unter [EB-Framework-API](er-apis-app73.md).

### <a name="modify-source-code"></a><a name="ModifySourceCode"></a>Quellcode ändern

#### <a name="add-a-data-contract-class"></a><a name="DataContractClass"></a>Hinzufügen einer Datenvertragsklasse

Fügen Sie die neue Klasse **QuestionnairesErReportContract** in Ihr Microsoft Visual Studio-Projekt ein und schreiben Sie den Code, mit dem der Datenvertrag angegeben wird, der zum Ausführen des konfigurierten EB-Formats verwendet werden kann.

```xpp
/// <summary>
///     This class is the data contract class for the <c>QuestionnairesErReportDP</c> class.
/// </summary>
/// <remarks>
///    This is the data contract class for the Questionnaires ER report.
/// </remarks>
[
    DataContractAttribute,
    SysOperationContractProcessingAttribute(classStr(QuestionnairesErReportUIBuilder))
    ]
    public class QuestionnairesErReportContract extends ERFormatMappingRunBaseContract implements SysOperationValidatable
{
    ERFormatMappingId formatMapping;

    /// <summary>
    ///    Validates the report parameters.
    /// </summary>
    /// <returns>
    ///    true if no errors; otherwise, false.
    /// </returns>
    public boolean validate()
    {
        boolean ret = true;
        if (!formatMapping)
        {
            ret = checkFailed(strFmt("@SYS26332", new SysDictType(extendedTypeNum(ERFormatMappingId)).label()));
        }
        return ret;
    }
    [
        DataMemberAttribute('FormatMapping'),
        SysOperationLabelAttribute(literalstr("@ElectronicReporting:FormatMapping")),
        SysOperationHelpTextAttribute(literalstr("@ElectronicReporting:FormatMapping"))
    ]
    public ERFormatMappingId parmFormatMapping(ERFormatMappingId _formatMapping = formatMapping)
    {
        formatMapping = _formatMapping;
        return formatMapping;
    }
}
```

#### <a name="add-a-ui-builder-class"></a><a name="UIBuilderClass"></a>Hinzufügen einer UI-Builder-Klasse

Fügen Sie die neue Klasse **QuestionnairesErReportUIBuilder** in Ihr Projekt Visual Studio ein und schreiben Sie Code, um ein Laufzeitdialogfeld zu generieren, mit deren Hilfe Sie die Formatzuordnungs-ID des EB-Formats gesucht wird, die ausgeführt werden muss. Der angegebene Code sucht nur EB-Formate, die eine Datenquelle des Typs **Datenmodell** enthalten, die sich auf das Datenmodell **[Questionnaires](#DataModeName)** bezieht, indem die Definition von **[Stamm](#RootDefinitionName)** verwendet wird.

> [!NOTE]
> Alternativ können Sie EB-Integrationspunkte verwenden, um EB-Formate zu filtern. Weitere Informationen finden Sie unter [API zum Anzeigen einer Formatzuordnungssuche](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).

```xpp
/// <summary>
/// The UIBuilder class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportUIBuilder extends SysOperationAutomaticUIBuilder
{
    public const str ERQuestionnairesModel = 'Questionnaires';
    public const str ERQuestionnairesDataContainer = 'Root';

    /// <summary>
    /// Action after build of the dialog UI.
    /// </summary>
    public void postBuild()
    {
        DialogField formatMapping;
        super();
        formatMapping = this.bindInfo().getDialogField(this.dataContractObject(),
            methodStr(QuestionnairesErReportContract, parmFormatMapping));
        formatMapping.registerOverrideMethod(
            methodStr(FormReferenceControl, lookupReference),
            methodStr(QuestionnairesErReportUIBuilder, formatMappingLookup),
            this);
    }

    /// <summary>
    /// Performs the lookup form for format mapping.
    /// </summary>
    /// <param name="_referenceGroupControl">
    /// The control to perform lookup form.
    /// </param>
    public void formatMappingLookup(FormReferenceControl _referenceGroupControl)
    {
        ERObjectsFactory::createFormatMappingTableLookupForControlAndModel(
            _referenceGroupControl,
            ERQuestionnairesModel,
            ERQuestionnairesDataContainer).performFormLookup();
    }
}
```

#### <a name="add-a-data-provider-class"></a><a name="DataProviderClass"></a>Hinzufügen einer Datenanbieterklasse

Fügen Sie die neue Klasse **QuestionnairesErReportContract** in Ihr Microsoft Visual Studio-Projekt ein und schreiben Sie den Code, mit dem der Datenanbieter eingeführt wird, der zum Ausführen des konfigurierten EB-Formats verwendet werden kann. Der bereitgestellte Code enthält nur den Datenvertrag für diesen Datenanbieter.

```xpp
/// <summary>
/// Data provider class for Questionnaires ER report.
/// </summary>
public class QuestionnairesErReportDP
{
    QuestionnairesErReportContract contract;
    public static QuestionnairesErReportDP construct()
    {
        QuestionnairesErReportDP  dataProvider;
        dataProvider = new QuestionnairesErReportDP();
        return dataProvider;
    }
}
```

#### <a name="add-a-labels-file"></a><a name="LabelsFile"></a>Hinzufügen einer Beschriftungsdatei

Fügen Sie die neue Beschriftungsdatei **QuestionnairesErReportLabels\_en-US** in Ihr Visual Studio-Projekt ein und geben Sie die folgenden Beschriftungen für neue UI-Ressourcen angeben:

- Die Beschrifung **\@QuestionnairesReport** für eine neue Menüoption, die den folgenden Text in US-Englisch (en-US) enthält: **Fragenbogenbericht (unterstützt von EB)**
- Die Bezeichnung **\@QuestionnairesReportBatchJobDescription** für einen Stapeljobtitel, wenn ein ausgewähltes EB-Format für die Ausführung als Stapeljob geplant ist

#### <a name="add-a-report-service-class"></a><a name="ServiceClass"></a>Hinzufügen einer Berichtserviceklasse

Fügen Sie die neue Klasse **QuestionnairesErReportService** in Ihr Visual Studio-Projekt ein und schreiben Sie Code, der ein EB-Format aufruft, es per Formatzuordnungs-ID identifiziert und einen Datenvertrag als Parameter bereitstellt.

```xpp
using Microsoft.Dynamics365.LocalizationFramework;
/// <summary>
/// The electronic reporting service class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportService extends SysOperationServiceBase
{
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'Questionnaires report';
    public const str ParametersDataSourceName = 'RunTimeParameters';

    /// <summary>
    /// Generates report by using Electronic reporting framework
    /// </summary>
    /// <param name = "_contract">The Questionnaires report contract</param>
    public void generateReportByGER(QuestionnairesErReportContract _contract)
    {
        ERFormatMappingId formatMappingId;
        QuestionnairesErReportDP  dataProvider;
        dataProvider = QuestionnairesErReportDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        if (formatMappingId)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, ParametersDataSourceName, _contract, true));

                // Call ER to generate the report.
                ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                if (formatMappingRun.parmShowPromptDialog(true))
                {
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());
                    formatMappingRun.run();
                }
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

Wenn Sie ein EB-Format verwenden müssen, in dem Anwendungsdaten ausgeführt werden, müssen Sie eine Datenquelle für den Typ **Datenmodell** in der Formatzuordnung konfigurieren. Diese Datenquelle bezieht sich auf einen bestimmten Teil des angegebenen Datenmodells unter Verwendung einer einzelnen Stammdefinition. Wenn das EB-Format ausgeführt wird, ruft es diese Datenquelle auf, um auf die entsprechende EB-Modellzuordnung zuzugreifen, die für ein bestimmtes Modell und eine bestimmte Stammdefinition konfiguriert ist.

Alle Informationen, die Sie möglicherweise im Quellcode vorbereiten und im Rahmen des Datenvertrags speichern, können mithilfe einer EB-Modellzuordnung dieses Typs an das laufende EB-Format übergeben werden. In der EB-Modellzuordnung müssen Sie eine Datenquelle des Typs **Objekt** konfigurieren, der sich auf die Klasse **[QuestionnairesErReportContract](#DataContractClass)** bezieht. Um eine Modellzuordnung zu identifizieren, müssen Sie eine Datenquelle angeben, die diese Modellzuordnung aufruft. Im bereitgestellten Code enthält diese Datenquelle, die durch die Konstante **ERModelDataSourceName** festgelegt wird, den Wert **[Modell](#ModelDSName)** enthält. Um festzustellen, welche Datenquelle zum Offenlegen des Datenvertrags in der Modellzuordnung verwendet wird, müssen Sie einen Datenquellennamen angeben. Im angegebenen Code wird dieser Name durch die Konstante **ParametersDataSourceName** angegeben, die den Wert <a name="DataContractDSName"></a>**RunTimeParameters** enthält.

> [!NOTE]
> In einer neuen Umgebung müssen Sie möglicherweise die EB-Metadaten aktualisieren, damit dieser Klassentyp im EB-Modellzuordnungsdesigner verfügbar ist. Weitere Informationen finden Sie unter [Konfigurieren des EB-Frameworks](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).

#### <a name="add-a-report-controller-class"></a><a name="ControllerClass"></a>Hinzufügen einer Bericht-Controller-Klasse

Fügen Sie die nee Klasse **QuestionnairesErReportController** in Ihr Visual Studio-Projekt ein und schreiben Sie Code, der ein EB-Format im synchronen oder Batch-Modus ausführt, im Dialogfeld, das entsprechend der Logik der angegebenen Klasse **QuestionnairesErReportUIBuilder** erstellt wird.

```xpp
/// <summary>
/// The controller for Questionnaires ER report
/// </summary>
class QuestionnairesErReportController extends ERFormatMappingRunBaseController
{
    /// <summary>
    /// The main entrance of the controller
    /// </summary>
    /// <param name = "args">The arguments</param>
    public static void main(Args args)
    {
        QuestionnairesErReportController operation;
        operation = new QuestionnairesErReportController(
            classStr(QuestionnairesErReportService),
            methodStr(QuestionnairesErReportService, generateReportByGER),
            SysOperationExecutionMode::Synchronous);
        operation.startOperation();
    }

    /// <summary>
    /// Gets caption of the dialog.
    /// </summary>
    /// <returns>Caption of the dialog</returns>
    public ClassDescription defaultCaption()
    {
        ClassDescription batchDescription;
        batchDescription = "Questionnaires report (powered by ER)";
        return batchDescription;
    }
}
```

#### <a name="add-a-menu-item"></a><a name="MenuItem"></a>Hinzufügen eines Menüpunkts

Fügen Sie den neuen Menüpunkt **QuestionnairesErReport** in Ihr Visual Studio-Projekt ein. In der Eigenschaft **Objekt** bezieht sich diese Menüoption auf die Klasse **QuestionnairesErReportController** und wird verwendet, um eine Benutzerberechtigung zum Auswählen und Ausführen eines EB-Formats festzulegen. In der Eigenschaft **Beschriftung** bezieht sich diese Menüoption auf die zuvor erstellte Beschriftung **\@QuestionnairesReport**, sodass korrekter Text in der Anwendungs-UI angegeben wird.

#### <a name="add-a-menu-item-to-a-menu"></a><a name="Menu"></a>Hinzufügen einer Menüoption in ein Menü

Fügen Sie das vorhandene Menü **KM** in Ihr Visual Studio-Projekt ein. Sie müssen ein neues Objekt von **QuestionnairesErReport** des Typs **Ausgabe** in dieses Menü einfügen. Dieser Artikel muss sich auf die Menüoption **QuestionnairesErReport** beziehen, die im vorigen Abschnitt beschrieben wird.

#### <a name="build-a-visual-studio-project"></a><a name="BuildVSProject"></a>Erstellen eines Visual Studio-Projekts

Erstellen Sie Ihr Projekt, um Benutzern eine neue Menüoption zur Verfügung zu stellen.

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp"></a>Verwenden eines Formats von der Anwendung aus

1. Wählen Sie **Fragebogen**\>**Design**\>**Fragebogenbericht (unterstützt von EB)** aus.

    ![Auswählen des Menüpunkts "Fragebogenbericht (unterstützt von EB)" im Modul "Fragebogen", um den vorhandenen SSRS-Bericht auszuführen](./media/er-quick-start1-application-menu-modified.png)

2. Wählen Sie im Dialogfeld im Feld **Formatzuordnung** den Eintrag **Fragebogenbericht** aus.
3. Wählen Sie **OK**.
4. Konfigurieren Sie im Dialogfeld **Elektronische Berichtparameter** im Inforegister **Einzuschließende Datensätze** die Filteroptionen, sodass nur der Fragebogen **SBCCrsExam** enthalten ist.
5. Wählen Sie **OK**, um die Filteroptionen zu bestätigen.
6. Wählen Sie zum Ausführen des Berichts **OK** aus.

    ![Festlegen der Auswahlkriterien im Dialogfeld "Elektronischer Bericht"](./media/er-quick-start1-report-run-dialog-page.png)

7. Prüfen Sie den generierten Bericht.

## <a name="tune-a-designed-er-solution"></a><a name="TuneSolution"></a>Optimieren einer entworfenen EB-Lösung

Sie können die konfigurierte EB-Lösung so ändern, dass sie die von Ihnen entwickelte Datenanbieterklasse verwendet, um auf Details des laufenden EB-Formats zuzugreifen, und den Namen dieses EB-Formats in einen generierten Bericht eingibt.

### <a name="modify-a-model-mapping"></a><a name="ModifyModelMapping"></a>Ändern einer Modellzuordnung

#### <a name="add-data-sources-to-access-a-data-contract-object"></a><a name="AddDataSource1"></a>Hinzufügen von Datenquellen für den Zugriff auf Datenvertragsobjekte

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur **Zahlungsmodell** und wählen Sie dann **Fragebogenzuordnung** aus.
3. Wählen Sie **Designer** aus, um die Seite **Modell für Datenquellenzuordnung** zu öffnen.
4. Wählen Sie **Designer** aus, um die ausgewählte Zuordnung im Modellzuordnungsdesigner zu öffnen.
5. Wählen Sie auf der Seite **Modellzuordnungsdesigner** im Bereich **Datenquellentypen** den Eintrag **Dynamics 365 for Operations\\Objekt** aus.
6. Wählen Sie **Stamm hinzufügen** im Bereich **Datenquellen** aus.
7. Geben Sie im Dialogfeld im Feld **Name** den Eintrag **[RunTimeParameters](#DataContractDSName)** ein, wie im Quellcode der Klasse **QuestionnairesErReportService** festgelegt.
8. Geben Sie im Feld **Klasse** den Eintrag **[QuestionnairesErReportContract ](#DataContractClass)** ein, der bereits codiert wurde.
9. Wählen Sie **OK**.
10. Erweitern Sie **RunTimeParameters**.

Die hinzugefügte Datenquelle enthält Informationen zur Datensatz-ID der laufenden EB-Formatzuordnung.

![Datenquelle im EB-Modellzuordnungsdesigner hinzugefügt](./media/er-quick-start1-mapping3.png)

#### <a name="add-a-data-source-to-access-er-format-mapping-records"></a><a name="AddDataSource2"></a>Hinzufügen einer Datenquelle, um auf EB-Formatzuordnungsdatensätze zuzugreifen

Bearbeiten Sie die ausgewählte Modellzuordnung weiter, indem Sie eine Datenquelle hinzufügen, um auf EB-Formatzuordnungsdatensätze zuzugreifen.

1. Wählen Sie auf der Seite **Modellzuordnungsdesigner** im Bereich **Datenquellentypen** die Option **Dynamics 365 for Operations\\ Tabellendatensätze** aus.
2. Wählen Sie **Stamm hinzufügen** im Bereich **Datenquellen** aus.
3. Geben Sie im Dialogfeld im Feld **Name** den Eintrag **ER1** ein.
4. Geben Sie im Feld **Tabelle** den Eintrag **ERFormatMappingTable** ein.
5. Wählen Sie **OK**.

#### <a name="add-a-data-source-to-access-a-format-mapping-record-of-a-running-er-format"></a><a name="AddDataSource3"></a>Hinzufügen einer Datenquelle, um auf einen Formatzuordnungsdatensatz eines aktiven EB-Formats zuzugreifen

Bearbeiten Sie die ausgewählte Modellzuordnung weiter, indem Sie eine Datenquelle hinzufügen, um auf den Formatzuordnungsdatensatz des aktiven EB-Formats zuzugreifen.

1. Wählen Sie auf der Seite **Modellzuordnungsdesigner** im Feld **Datenquellentypen** den Eintrag **Funktionen\\Berechnetes Feld** aus.
2. Wählen Sie **Stamm hinzufügen** im Bereich **Datenquellen** aus.
3. Geben Sie im Dialogfeld im Feld **Name** den Eintrag **ER2** ein.
4. Wählen Sie **Formel bearbeiten** aus.
5. Geben Sie im Formeleditor im Feld **Formel** den Eintrag **FIRSTORNULL (FILTER (ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))** ein.
6. Klicken Sie auf **Speichern** und schließen Sie den Formeleditor.
7. Wählen Sie **OK**.

#### <a name="enter-the-name-of-the-running-er-format-in-the-data-model"></a><a name="AddBinding"></a>Eingeben des Namens des aktiven EB-Formats im Datenmodell

Bearbeiten Sie die ausgewählte Modellzuordnung weiter, sodass der Name des aktiven EB-Formats in das Datenmodell eingegeben wird.

1. Erweitern Sie auf der Seite **Modellzuordnungsdesigner** im Bereich **Datenmodell** **ExecutionContext** und wählen Sie dann **ExecutionContext\\FormatName** aus.
2. Wählen Sie im Bereich **Datenmodell** die Option **Bearbeiten** aus, um eine Datenbindung für das Feld des ausgewählten Datenmodells zu konfigurieren.
3. Geben Sie im Formeleditor im Feld **Formel** den Eintrag **FIRSTORNULL (ER2.'\>Relations'.Format).Name** ein.
4. Klicken Sie auf **Speichern** und schließen Sie den Formeleditor.

Da Sie das Feld **FormatName** verwendet haben, zeigt die konfigurierte Modellzuordnung jetzt den Namen eines EB-Formats, durch den diese Modellzuordnung bei der Ausführung aufgerufen wird.

![Binden des Datenmodellfelds an die Methode der hinzugefügten Datenquelle im EB-Modellzuordnungsdesigner](./media/er-quick-start1-mapping4.png)

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping2"></a>Vervollständigen des Designs der Modellzuordnung

1. Wählen Sie auf der Seite **Modellzuordnungsdesigner** die Option **Speichern** aus.
2. Schließen Sie die Seite.
3. Schließen Sie die Seite "Modellzuordnungen".
4. Stellen Sie auf der Seite **Konfigurationen** sicher, das die Konfiguration **Fragebogenzuordnung** noch ausgewählt ist. Wählen Sie dann auf dem Inforegister **Versionen** die Konfigurationsversion mit dem Status **Entwurf** aus.
5. Wählen Sie **Status ändern** \> **Abgeschlossen**.

Der Status der Version 1.2 dieser Konfiguration wird von **Entwurf** zu **Abgeschlossen** geändert. Version 1.2 kann nicht mehr geändert werden. Diese Version enthält das konfigurierte Modellzuordnung und kann als Basis für andere EB-Konfigurationen verwendet werden. Version 1.3 dieser Konfiguration wird erstellt und hat den Status **Entwurf**. Sie können diese Version bearbeiten, um die Modellzuordnung **Fragebogen** anzupassen.

### <a name="modify-a-format"></a><a name="ModifyFormat"></a>Ändern eines Formats

Sie können das konfigurierte EB-Format so ändern, dass sein Name in der Fußzeile eines Berichts angezeigt wird, der beim Ausführen des EB-Formats generiert wird.

#### <a name="add-a-new-format-element"></a><a name="AddFormatElement"></a>Hinzufügen eines neuen Formatelements

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur **Zahlungsmodell** und wählen Sie dann **Fragebogenbericht** aus.
3. Wählen Sie **Designer** aus.
4. Wählen Sie auf der Seite **Formatdesigner** das Stammobjekt **Bericht** aus.
5. Wählen Sie **Hinzufügen**, um ein neues verschachteltes Formatelement für das ausgewählte Stammelement **Bericht** hinzuzufügen.
6. Wählen Sie **Excel \\Fußzeile** aus.
7. Geben Sie im Feld **Name** die Bezeichnung **Fußzeile** ein.
8. Wählen Sie **Bericht\Fußzeile** und dann **Hinzufügen** aus.
9. Wählen Sie **Text \\String** aus.

#### <a name="bind-the-added-format-element"></a><a name="BindAddedFormatElement"></a>Binden des hinzugefügten Formatelements

1. Wählen Sie auf der Seite **Formatdesigner** auf der Registerkarte **Zuordnung** in der Formatstruktur für das aktive Element **Fußzeile\\String** den Eintrag **Formel bearbeiten** aus.
2. Geben Sie im Formeleditor im Feld **Formel** den Eintrag **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))** ein.
3. Klicken Sie auf **Speichern** und schließen Sie den Formeleditor.
4. Wählen Sie **Speichern** aus.

Das konfigurierte Format wurde jetzt so geändert, dass sein Name in die Fußzeile eines generierten Berichts im Format **Fußzeile \\String**-Element eingegeben wird.

![Hinzufügen des Fußzeilenformatelements zum konfigurierten Format im ER Operation Designer](./media/er-quick-start1-template-format-structure3.png)

#### <a name="complete-the-format-design"></a><a name="CompleteFormat2"></a>Abschließen des Formatentwurfs

1. Seite **Format-Designer** schließen.
2. Stellen Sie auf der Seite **Konfigurationen** sicher, das die Konfiguration **Fragebogenbericht** noch ausgewählt ist. Wählen Sie dann auf dem Inforegister **Versionen** die Konfigurationsversion mit dem Status **Entwurf** aus.
3. Wählen Sie **Status ändern** \> **Abgeschlossen**.

Der Status der Version 1.2 dieser Konfiguration wird von **Entwurf** zu **Abgeschlossen** geändert. Version 1.2 kann nicht mehr geändert werden. Diese Version enthält das konfigurierte Format und kann als Basis für andere EB-Konfigurationen verwendet werden. Version 1.3 dieser Konfiguration wird erstellt und hat den Status **Entwurf**. Sie können diese Version bearbeiten, um den Bericht **Fragebogen** anzupassen.

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp2"></a>Verwenden eines Formats von der Anwendung aus

1. Wählen Sie **Fragebogen**\>**Design**\>**Fragebogenbericht (unterstützt von EB)** aus.
2. Wählen Sie im Dialogfeld im Feld **Formatzuordnung** den Eintrag **Fragebogenbericht** aus.
3. Wählen Sie **OK**.
4. Konfigurieren Sie im Dialogfeld **EB-Parameter** im Inforegister **Einzuschließende Datensätze** die Filteroptionen, sodass nur der Fragebogen **SBCCrsExam** inhalten ist.
5. Wählen Sie **OK**, um die Filteroptionen zu bestätigen.
6. Wählen Sie zum Ausführen des Berichts **OK** aus.
7. Überprüfen Sie die generierte Datei im Excel-Format.

Beachten Sie, dass die Fußzeile des generierten Berichts den Namen des EB-Formats enthält, mit dem er generiert wurde.

![Generierter Bericht im Excel-Format.](./media/er-quick-start1-report4.png)

### <a name="run-a-format-from-er"></a><a name="RunFormatFromER3"></a>Verwenden eines Formats von EB aus

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur **Zahlungsmodell** und wählen Sie dann **Fragebogenbericht** aus.
3. Wählen Sie im Aktivitätsbereich auf **Ausführen**.
4. Konfigurieren Sie im Dialogfeld **Elektronische Berichtparameter** im Inforegister **Einzuschließende Datensätze** die Filteroptionen, sodass nur der Fragebogen **SBCCrsExam** enthalten ist.
5. Wählen Sie **OK**, um die Filteroptionen zu bestätigen.
6. Wählen Sie zum Ausführen des Berichts **OK** aus.
7. Überprüfen Sie den generierten Bericht im Excel-Format.

Beachten Sie, dass die Fußzeile des generierten Berichts nicht den Namen des EB-Formats enthält, mit dem er generiert wurde, da das Datenvertragsobjekt nicht an die laufende Modellzuordnung übergeben wurde, als es vom EB-Format aufgerufen wurde, das in EB ausgeführt wurde.

### <a name="configure-a-format-destination-for-on-screen-preview"></a><a name="ConfigureDestination"></a>Konfigurieren eines Formatziels für die Bildschirmvorschau

1. Wählen Sie **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Ziel der elektronischen Berichterstellung**.
2. Fügen Sie auf der **Ziel der elektronischen Berichterstattung** einen Zieldatensatz für das konfigurierte EB-Format **Fragebogenbericht** hinzu.
3. Richten Sie auf dem Inforegister **Dateizielort** die **Anzeige** [Ziel](er-destination-type-screen.md) für die Formatkomponente **Bericht** ein, die mit [hinzugefügt](#AddFormatRootElement) als Stammelement des konfigurierten EB-Formats **Fragebogenbericht** aufgenommen wurde.
4. Geben Sie auf dem Inforegister **PDF-Konvertierungseinstellungen** das Ziel ein, um einem Bericht in das [PDF-Format](electronic-reporting-destinations.md#OutputConversionToPDF) zu konvertieren, das die Seitenausrichtung **Querformat** verwendet.

![Konfigurieren des benutzerdefinierten Bildschirmziels für das EB-Format auf der Zielseite für die elektronische Berichterstellung](./media/er-quick-start1-destination.png)

### <a name="run-a-format-from-the-application-to-preview-it-as-a-pdf-document"></a><a name="RunFormatFromApp3"></a>Ausführen eines Format von der Anwendung aus, um es als PDF-Dokument anzuzeigen

1. Wählen Sie **Fragebogen**\>**Design**\>**Fragebogenbericht (unterstützt von EB)** aus.
2. Wählen Sie im Dialogfeld im Feld **Formatzuordnung** den Eintrag **Fragebogenbericht** aus.
3. Wählen Sie **OK**.
4. Konfigurieren Sie im Dialogfeld **Elektronische Berichtparameter** im Inforegister **Einzuschließende Datensätze** die Filteroptionen, sodass nur der Fragebogen **SBCCrsExam** enthalten ist.
5. Wählen Sie **OK**, um die Filteroptionen zu bestätigen.

    Beachten Sie auf dem Inforegister **Zielorte**, dass das Feld **Ausgabe** auf **Anzeige** gesetzt ist. Wenn Sie das konfigurierte Ziel ändern möchten, wählen Sie **Ändern** aus.

    ![Dialogfeld zur Laufzeit des EB-Berichts, in dem Sie das konfigurierte Ziel ändern können](./media/er-quick-start1-run-settings.png)

6. Wählen Sie zum Ausführen des Berichts **OK** aus.
7. Überprüfen Sie den generierten Bericht im PDF-Format.

    ![Bildschirmvorschau des generierten Berichts im PDF-Format](./media/er-quick-start1-preview-PDF.png)

## <a name="additional-resources"></a><a name="References"></a>Zusätzliche Ressourcen

- [Überblick über die elektronische Berichterstellung](general-electronic-reporting.md)
- [Formelsprache in der elektronischen Berichterstellung](er-formula-language.md)
- [Mehrsprachige Berichte entwerfen](er-design-multilingual-reports.md)
- [ER-Framework-API](er-apis-app73.md)
- [CASE-Funktion](er-functions-logical-case.md)
- [CONCATENATE-Funktion](er-functions-text-concatenate.md)
- [DATETIMEFORMAT-Funktion](er-functions-datetime-datetimeformat.md)
- [FILTER-Funktion](er-functions-list-filter.md)
- [FIRSTORNULL-Funktion](er-functions-list-firstornull.md)
- [FORMAT-Funktion](er-functions-text-format.md)
- [IF-Funktion](er-functions-logical-if.md)
- [ORDERBY-Funktion](er-functions-list-orderby.md)
- [SESSIONNOW-Funktion](er-functions-datetime-sessionnow.md)
