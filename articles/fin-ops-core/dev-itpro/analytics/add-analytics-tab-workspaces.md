---
title: Analysen zu Arbeitsbereichen mit Power BI Embedded hinzufügen
description: Dieses Thema zeigt, wie Sie in die Registerkarte "Analysen" eines Arbeitsbereichs einen Power BI-Bericht einbetten.
author: RichdiMSFT
ms.date: 06/21/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 14c8c36b90caa3a9378a739932d734b94985b46c
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6354444"
---
# <a name="add-analytics-to-workspaces-by-using-power-bi-embedded"></a>Analysen zu Arbeitsbereichen mit Power BI Embedded hinzufügen

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Diese Funktion wird in Finance and Operations (Version 7.2 und höher) unterstützt.

## <a name="introduction"></a>Einführung
Dieses Thema zeigt, wie Sie in die Registerkarte **Analysen** eines Arbeitsbereichs einen Microsoft Power BI-Bericht einbetten. Für das hier gezeigte Beispiel erweitern wir den Arbeitsbereich **Reservierungsverwaltung** in der Anwendung Flottenmanagement, um der Registerkarte **Analysen** einen analytischen Arbeitsbereich hinzuzufügen.

## <a name="prerequisites"></a>Voraussetzungen
+ Zugriff auf eine Entwicklerumgebung mit Plattform-Update 8 oder höher.
+ Einen Analysebericht (PBIX-Datei), der mit Microsoft Power BI Desktop erstellt wurde, und der ein Datenmodell verwendet, das von der Entitätsspeicher-Datenbank gespeist wird.

## <a name="overview"></a>Überblick
Egal, ob Sie einen vorhandenen Anwendungsarbeitsbereich erweitern oder einen eigenen neuen Arbeitsbereich anlegen, können Sie eingebettete analytische Ansichten nutzen, um informative und interaktive Ansichten Ihrer Geschäftsdaten bereitzustellen. Der Prozess für das Hinzufügen einer Registerkarte mit analytischem Arbeitsbereich umfasst 4 Schritte.

1. Eine .pbix-Datei als Dynamics 365-Ressource hinzufügen.
2. Eine Registerkarte für einen analytischen Arbeitsbereich definieren.
3. Die .pbix-Ressource in die Registerkarte mit dem Arbeitsbereich einbetten.
4. Optional: Erweiterungen hinzufügen, um die Ansicht zu personalisieren.

> [!NOTE]
> Weitere Informationen zum Erstellen von analytischen Berichten finden Sie unter [Erste Schritte mit Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/). Diese Seite enthält wichtige Informationen, die Ihnen helfen, attraktive Lösungen für analytische Berichte zu erstellen.

## <a name="add-a-pbix-file-as-a-resource"></a>Eine .pbix-Datei als Ressource hinzufügen
Bevor Sie anfangen, müssen Sie den Power BI-Bericht erstellen oder erhalten, den Sie in den Arbeitsbereich einbetten wollen. Weitere Informationen zum Erstellen von analytischen Berichten finden Sie unter [Erste Schritte mit Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).

Gehen Sie wie folgt vor, um eine PBIX-Datei als Visual Studio-Projektartefakt hinzuzufügen.

1. Erstellen Sie ein neues Projekt im entsprechenden Modell.
2. Wählen Sie das Projekt im Projektmappen-Explorer aus, klicken Sie mit der rechten Maustaste und wählen Sie dann **Hinzufügen** \> **Neues Element**.
3. Wählen Sie im Dialogfeld **Neues Element hinzufügen** unter **Operations-Artefakte** die Vorlage **Ressource** aus.
4. Geben Sie einen Namen ein, der für die Referenzierung des Berichts in X++-Metadaten verwendet wird, und klicken Sie dann auf **Hinzufügen**.

    ![Dialogfeld „Neues Element hinzufügen“.](media/analytical-workspace-add.png)

5. Suchen Sie die .pbix-Datei, die die Definition des analytischen Berichts enthält, und klicken Sie dann auf **Öffnen**.

    ![Dialogfeld „Auswählen einer Ressourcendatei“.](media/analytical-workspace-select-resource.png)

Nachdem Sie die .pbix-Datei als Dynamics 365-Ressource hinzugefügt haben, können Sie die Berichte in Arbeitsbereiche einbetten und unter Verwendung von Menüeinträgen direkte Links hinzufügen.

## <a name="add-a-tab-control-to-an-application-workspace"></a>Hinzufügen eines Registerkarten-Steuerelements zu einem Anwendungsarbeitsbereich
In diesem Beispiel erweitern wir den Arbeitsbereich **Reservierungsverwaltung** im Flottenmanagement-Modell, indem wir der Definition des Formulars **FMClerkWorkspace** die Registerkarte **Analysen** hinzufügen.

Die folgende Abbildung zeigt, wie das Formular **FMClerkWorkspace** im Designer in Microsoft Visual Studio aussieht.

![Formular FMClerkWorkspace vor den Änderungen.](media/analytical-workspace-definition-before.png)

Gehen Sie wie folgt vor, um die Formulardefinition für den Arbeitsbereich **Reservierungsverwaltung** zu erweitern.

1. Öffnen Sie den Formulardesigner, um die Designdefinition zu erweitern.
2. In dieser Designdefinition wählen Sie das oberste Element aus, **Design | Muster: Arbeitsbereich operational**
3. Klicken Sie mit der rechten Maustaste und wählen Sie dann **Neu** \> **Registerkarte**, um das neue Steuerelement **FormTabControl1** hinzuzufügen.
4. Wählen Sie im Formulardesigner **FormTabControl1**.
5. Klicken Sie mit der rechten Maustaste und wählen Sie dann **Neue Registerkartenseite**, um eine neue Registerkartenseite hinzuzufügen.
6. Geben Sie der Registerkarte einen sprechenden Namen, wie beispielsweise **Arbeitsbereich**.
7. Wählen Sie im Formulardesigner **FormTabControl1**.
8. Klicken Sie mit der rechten Maustaste und wählen Sie dann **Neue Registerkartenseite**.
9. Geben Sie der Registerkarte einen sprechenden Namen, wie beispielsweise **Analysen**.
10. Wählen Sie im Formulardesigner **Analysen (Registerkartenseite)**.
11. Legen Sie die Eigenschaft **Bildbeschriftung** auf **Analytik** und die Eigenschaft **Automatische Deklaration** auf **Ja** fest.
12. Klicken Sie mit der rechten Maustaste auf das Steuerelement und wählen Sie dann **Neu** \> **Gruppe**, um ein neues Formulargruppensteuerelement hinzuzufügen.
13. Geben Sie der Formulargruppe einen sprechenden Namen, wie beispielsweise **powerBIReportGroup**.
14. Wählen Sie im Formulardesigner **PanoramaBody (Registerkarte)** und ziehen Sie das Steuerelement auf die Registerkarte **Arbeitsbereich**.
15. In dieser Designdefinition wählen Sie das oberste Element aus, **Design | Muster: Arbeitsbereich operational**
16. Klicken Sie mit der rechten Maustaste und wählen Sie dann **Muster entfernen**.
17. Klicken Sie erneut mit der rechten Maustaste und wählen Sie dann **Muster hinzufügen** \> **Arbeitsbereich mit Registerkarten**.
18. Führen Sie einen Build aus, um Ihre Änderungen zu überprüfen.

Die folgende Abbildung zeigt, wie das Design nach Anwendung dieser Änderungen aussieht.

![FMClerkWorkspace nach den Änderungen.](media/analytical-workspace-definition-after.png)

Nachdem Sie die Steuerelemente für das Formular hinzugefügt haben, die für die Einbettung des Arbeitsbereichberichts verwendet werden, müssen Sie die Größe des übergeordneten Steuerelements definieren, sodass es zum Layout passt. Standardmäßig werden die Seite **Filter** und die Seite **Registerkarte** auf dem Bericht angezeigt. Sie können die Sichtbarkeit dieser Steuerelemente jedoch abhängig vom Zielpublikum des Berichts abändern.

> [!NOTE]
> Für eingebettete Arbeitsbereiche empfehlen wir, der Konsistenz halber Erweiterungen zu verwenden, um die Seiten **Filter** und **Registerkarte** auszublenden.

Damit haben Sie die Aufgabe fertiggestellt, die Definition des Anwendungsformulars zu erweitern. Weitere Informationen zur Verwendung von Erweiterungen für Anpassungen finden Sie in [Anpassen durch Erweiterungen und Überlagerung](../extensibility/customization-overlayering-extensions.md).

## <a name="add-x-business-logic-to-embed-a-viewer-control"></a>Hinzufügen einer X++-Geschäftslogik, um ein Viewer-Steuerelement einzubetten
Gehen Sie wie folgt vor, um eine Geschäftslogik hinzuzufügen, die das Steuerelement für den Bericht-Viewer initialisiert, das in den Arbeitsbereich **Reservierungsverwaltung** eingebettet ist.

1. Öffnen Sie den Formulardesigner **FMClerkWorkspace**, um die Designdefinition zu erweitern.
2. Drücken Sie F7, um auf den Code hinter der Codedefinition zuzugreifen.
3. Fügen Sie den folgenden X++-Code hinzu.

    ```xpp
    [Form] 
    public class FMClerkWorkspace extends FormRun
    {
        private boolean initReportControl = true;
        protected void initAnalyticalReport()
        {
            if (!initReportControl)
            {
                return;
            }
            // Note: secure entry point into the Workspace's Analytics report
            if (Global::hasMenuItemAccess(menuItemDisplayStr(FMClerkWorkspace), MenuItemType::Display))
            {
                // initialize the PBI report control using shared helper
                PBIReportHelper::initializeReportControl('FMPBIWorkspaces', powerBIReportGroup);
            }
            initReportControl = false;
        }
        /// <summary>
        /// Initializes the form.
        /// </summary>
        public void init()
        {
            super();
            this.initAnalyticalReport();
        }
    }
    ```

4. Führen Sie einen Build aus, um Ihre Änderungen zu überprüfen.

Damit haben Sie die Aufgabe abgeschlossen, die Geschäftslogik hinzuzufügen, mit der das eingebettete Steuerelement für den Bericht-Viewer initialisiert wird. Die folgende Abbildung zeigt, wie der Arbeitsbereich nach Anwendung dieser Änderungen aussieht.

![In den Arbeitsbereich eingebetteter Bericht.](media/analytical-workspace-final.png)

> [!NOTE]
> Über die Registerkarten des Arbeitsbereichs unterhalb der Seitenüberschrift können Sie auf die vorhandene sofort ausgeführte Ansicht zugreifen.

## <a name="reference"></a>Referenz

### <a name="pbireporthelperinitializereportcontrol-method"></a>Die Methode PBIReportHelper.initializeReportControl
Dieser Abschnitt enthält Informationen über die Helferklasse, mit der ein Power BI-Bericht (PBIX-Ressource) in ein Formular-Gruppensteuerelement eingebettet wird.

#### <a name="syntax"></a>Syntax
```xpp
public static void initializeReportControl(
    str                 _resourceName,
    FormGroupControl    _formGroupControl,
    str                 _defaultPageName = '',
    boolean             _showFilterPane = false,
    boolean             _showNavPane = false,
    List                _defaultFilters = new List(Types::Class))
```

#### <a name="parameters"></a>Parameter

| Name             | Beschreibung                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------|
| resourceName     | Der Name der .pbix-Ressource.                                                                              |
| formGroupControl | Das Formular-Gruppensteuerelement, auf das das Power BI-Berichtssteuerelement angewendet wird.                                              |
| defaultPageName  | Der Standardseitenname.                                                                                       |
| showFilterPane   | Ein boolescher Wert, der angibt, ob der Filterbereich angezeigt (**true**) oder ausgeblendet (**false**) werden soll.     |
| showNavPane      | Ein boolescher Wert, der angibt, ob der Navigationsbereich angezeigt (**true**) oder ausgeblendet (**false**) werden soll. |
| defaultFilters   | Die Standardfilter für den Power BI-Bericht.                                                                 |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]