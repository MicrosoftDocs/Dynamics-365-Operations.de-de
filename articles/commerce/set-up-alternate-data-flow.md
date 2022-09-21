---
title: Richten Sie einen alternativen Dataflow für Empfehlungen ein
description: In diesem Artikel wird beschrieben, wie Sie eine Umgebung konfigurieren, indem Sie einen alternativen Dataflow verwenden, um Daten für den Empfehlungsdienst bereitzustellen.
author: bebeale
ms.date: 09/08/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: b507b9bb57c68aca9424b53f8ccc009efea733bc
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460162"
---
# <a name="set-up-an-alternate-dataflow-for-recommendations"></a>Richten Sie einen alternativen Dataflow für Empfehlungen ein

[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie eine Umgebung konfigurieren, indem Sie einen alternativen Dataflow verwenden, um Daten für den Empfehlungsdienst bereitzustellen.

## <a name="comparison-of-out-of-the-box-dataflow-with-alternate-dataflow"></a>Vergleich des vorkonfigurierten Dataflows mit einem alternativen Dataflow

Die folgende Abbildung zeigt den vorkonfigurierten Dataflow in einer Umgebung.

![Out-of-the-Box-Dataflow in einer Umgebung](media/reco-out-of-the-box-dataflow-2.png)

Die folgende Abbildung zeigt einen alternativen Dataflow, bei dem der Stapeljob für die Synchronisierung des Entitätsspeichers durch alternative Dataflowschritte ersetzt wird.

![Alternativer Dataflow in einer Umgebung](media/reco-alternate-dataflow-2.png)

## <a name="assumptions"></a>Voraussetzungen

- In diesem Artikel wird davon ausgegangen, dass Sie den Empfehlungsdienst bereits für Ihre Umgebung aktiviert haben. Weitere Informationen finden Sie unter [Produktempfehlungen aktivieren](enable-product-recommendations.md).
- Wenn Sie mit Dateien und Ordnern im Microsoft Azure Data Lake Storage-Konto arbeiten:

    - Sie können entweder die Benutzeroberfläche des Azure-Webportals oder die Azure Storage-Explorer-Anwendung verwenden.
    - Die Ausgangspunkte für die Arbeit mit Dateien und Ordnern befinden sich im **dynamics365-financeandoperations**-Container, der sich unter dem Ordner befindet, der so benannt ist, dass er Ihrer Umgebungs-URL entspricht.
    - Wenn der Name Ihrer Sandbox-Umgebung **MyUAT** lautet, lautet die Basis-URL der Umgebung `myuat.sandbox.operations.dynamics.com`.
    - Wenn mehr als eine Umgebung mit demselben Speicherkonto verbunden ist, verfügt jede Umgebung über einen eigenen Stammordner.

## <a name="prerequisites"></a>Voraussetzungen

Die folgenden Voraussetzungen müssen erfüllt sein, bevor Sie den alternativen Dataflowansatz implementieren können.

### <a name="set-up-microsoft-power-platform"></a>Microsoft Power Platform einrichten

Zum Einrichten von Microsoft Power Platform folgen Sie den Anweisungen in [Aktivieren Sie die Microsoft Power Platform-Integration](../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md).

### <a name="install-the-export-to-data-lake-add-in"></a>Export in Data Lake-Add-In installieren

Um das Add-In „In Data Lake exportieren“ zu installieren, befolgen Sie die Anweisungen in [Add-In für den Export in Azure Data Lake installieren](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

> [!NOTE]
> Notieren Sie sich die Konfigurationswerte, da Sie sie für einige der folgenden Schritte benötigen.

### <a name="configure-tables-to-export-in-dynamics-365"></a>Konfigurieren Sie Tabellen für den Export in Dynamics 365

Tabellensynchronisierung von Dynamics 365 zu Azure Data Lake Storage wird auf der **In Data Lake exportieren**-Seite verwaltet. Da diese Seite derzeit keinen Menüpunkt hat, können nur Benutzer mit **Systemadministrator**-Sicherheitsrolle es öffnen.

Gehen Sie folgendermaßen vor, um Tabellen für den Export in Dynamics 365 zu konfigurieren.

1. Zum Öffnen der **In Data Lake exportieren**-Seite fügen Sie die Zeichenfolge `?mi=DataFeedsDefinitionWorkspace` zur Basis-URL der Umgebung hinzu, wie im folgenden Beispiel gezeigt:

    `https://<environment-URL>/?mi=DataFeedsDefinitionWorkspace`

1. Auf der **In Data Lake exportieren**-Seite kopieren Sie die Tabellen, die im [Liste der RetailSales-Cube-Tabellen](#list-of-retailsales-cube-tables)-Abschnitt dieses Artikels aufgeführt sind.
1. In der **Systemname**-Spalte erweitern Sie die Liste der Filteroptionen.
1. Wählen Sie für den Filtertyp **ist einer von**. Setzen Sie dann den Cursor in das Textfeld und fügen Sie die Liste der Tabellen ein, die Sie aus der **In Data Lake exportieren**-Seite kopiert haben.
1. Wählen Sie unten in der Liste der Filteroptionen **Anwenden** aus.
1. Wählen Sie alle Zeilen im Raster aus, und wählen Sie dann **Aktivieren** aus.

> [!NOTE]
> Bevor Sie mit dem nächsten Schritt fortfahren, müssen alle Zeilen auf den Status **Ausgeführt** aktualisiert werden. Suchen und beheben Sie alle Fehler nach Bedarf.

### <a name="create-a-synapse-workspace"></a>Synapse-Arbeitsbereich erstellen

Um einen Synapse-Arbeitsbereich zu erstellen, wenn Sie noch keinen haben, folgen Sie den Anweisungen in [Schnellstart: Einen Synapse Workspace erstellen](/azure/synapse-analytics/quickstart-create-workspace).

Um Ihre Azure-Ressourcen organisiert zu halten, empfehlen wir, dass Sie das Data Lake Storage-Konto und den Synapse-Arbeitsbereich in einer Ressourcengruppe in Azure zusammenfassen. Sie können das Speicherkonto wiederverwenden, das Sie bei der Installation des Add-Ins „In Data Lake exportieren“ erstellt haben.

## <a name="create-a-database-in-synapse-for-recommendation-data-processing"></a>Erstellen Sie eine Datenbank in Synapse für die Verarbeitung von Empfehlungsdaten

Verwenden Sie die Konsolenanwendung des Common Data Model-Dienstprogramms (CDMUtil_ConsoleApp), um eine Datenbank in Ihrem Synapse-Arbeitsbereich zu erstellen und sie aus den Common Data Model-Tabellen in Data Lake Storage zu füllen. Wir empfehlen Ihnen, das Common Data Model-Dienstprogramm mit Ihrer Datenbank in einer Entwicklungsumgebung zu verwenden, falls es Erweiterungen gibt.

> [!NOTE]
> Bei den folgenden Schritten wird davon ausgegangen, dass dem RetailSales-Cube keine Erweiterungsdaten hinzugefügt werden.

Um eine Datenbank in Synapse zu erstellen, gehen Sie wie folgt vor.

1. Gehen Sie zum [Dynamics-365-FastTrack-Implementation-Assets GitHub](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Analytics/CDMUtilSolution#2-cdmutil-console-app), und befolgen Sie die Schritte zum Herunterladen der **CDMUtilConsoleApp.zip**-Datei.
1. Extrahieren Sie die ZIP-Datei in einen lokalen Ordner.
1. Öffnen Sie die **CDMUtil_ConsoleApp.dll.config**-Datei in einem Texteditor und aktualisieren Sie die folgenden Werte:

    1. Legen Sie den Wert **Mandanten-ID** (Azure-Mandanten-ID) fest.
    1. Stellen Sie den Wert **Zugriffsschlüssel** (Zugriffsschlüssel für das Data Lake Storage-Konto) ein.

        1. Öffnen Sie im Azure-Portal das Speicherkonto.
        1. Wählen Sie im Menü links auf der Seite **Zugriffsschlüssel** aus.
        1. Wählen Sie am oberen Seitenrand **Schlüssel anzeigen** aus.
        1. Wählen Sie die Kopieren-Schaltfläche für eines der beiden Schlüsselfelder und fügen Sie dann den Wert zwischen den doppelten Anführungszeichen in die Konfigurationsdatei ein.

    1. Stellen Sie den wert **ManifestURL** auf die URL Ihrer **Tables.manifest.cdm.json**-Datei in Azure Data Lake Storage ein. Navigieren Sie zum Abrufen der URL zu der Datei im Azure-Portal, wählen Sie die Auslassungspunkte (**...**) auf der rechten Seite der Ansicht und wählen Sie dann **Eigenschaften** aus. Die URL ist die erste Eigenschaft, die auf der **Überblick**-Registerkarte angezeigt wird.
    1. Stellen Sie den Wert **TargetDbConnectionString** auf die Verbindungszeichenfolge für den integrierten serverlosen SQL-Pool Ihres Synapse-Arbeitsbereichs ein.

        1. Wählen Sie im Synapse-Arbeitsbereich die **Verwalten**-Registerkarte aus.
        1. Wählen Sie im Untermenü **SQL-Pools** aus.
        1. Wählen Sie den Namen **Eingebaut** aus, um die Eigenschaften des Pools anzuzeigen.
        1. Wählen Sie im Eigenschaftendialogfeld den Verbindungstyp ADO.NET aus, den Sie verwenden möchten. Kopieren Sie dann den Wert der Verbindungszeichenfolge und fügen Sie ihn zwischen den doppelten Anführungszeichen in der Konfigurationsdatei ein.

        > [!NOTE]
        > Sie müssen die Berechtigung haben, Datenbanken zu erstellen. Zur einfacheren Verwendung möchten Sie vielleicht das integrierte **sqladminuser**-Administratorkonto verwenden.

    1. Entkommentieren Sie den **ProcessEntities**-Knoten, und setzen Sie seinen Wert auf **True** (zum Beispiel `<add key="ProcessEntities" value ="true"/>`).

1. Speichern und schließen Sie die **CDMUtil_ConsoleApp.dll.config**-Datei.
1. Kopieren Se die **EntityList.json**-Datei ins **/Manifest**-Verzeichnis.
1. Führen Sie in einem Eingabeaufforderungsfenster **cdmutil_consoleapp.exe** aus.

> [!NOTE]
> Wenn Sie die Ausgabe überprüfen, sollten 35 Entitäten/Ansichten, mindestens 75 Tabellen und keine Fehler vorhanden sein.

## <a name="prepare-the-data-lake-retailsales-aggregate-measurements-directory"></a>Bereiten Sie das Data Lake RetailSales Aggregate Measurements-Verzeichnis vor

### <a name="back-up-your-current-retailsales-cube-data-from-data-lake-storage"></a>Sichern Sie Ihre aktuellen RetailSales-Cube-Daten aus Data Lake Storage

Die einfachste Möglichkeit, Ihre aktuellen RetailSales-Cube-Daten zu sichern, besteht darin, das **RetailSales**-Verzeichnis in Data Lake Storage in **RetailSales-backup** oder ähnlich umzubenennen. Bei dieser Methode bleiben die vorhandenen Daten erhalten, falls später eine Fehlerbehebung erforderlich ist.

Der **/RetailSales**-Cube-Ordner befindet sich an folgendem Speicherort:

`<storage-account>/dynamics365-financeandoperations/<environment-url (for example, myuat.sandbox.operations.dynamics.com)>/AggregateMeasurements/RetailSales`

### <a name="create-a-new-retailsales-folder-and-upload-the-model-file"></a>Erstellen Sie einen neuen RetailSales-Ordner und laden Sie die Modelldatei hoch

Um ein neues **RetailSales**-Verzeichnis zu erstellen und die **model.json**-Datei hochzuladen, führen Sie die folgenden Schritte aus, um eine Datei in Data Lake Storage zu speichern.

1. Erstellen Sie ein neues leeres Verzeichnis auf derselben Ebene wie das vorherige Verzeichnis und benennen Sie es **RetailSales**.
1. Laden Sie die **model.json** Datei in das neue Verzeichnis hoch.

## <a name="create-a-pipeline-to-copy-the-retailsales-cube-data"></a>Erstellen Sie eine Pipeline, um die RetailSales-Cube-Daten zu kopieren

Die Pipeline liest die RetailSales-Cubeansichten und exportiert die Daten in CSV-Dateien in Data Lake Storage.

Zum Erstellen einer Pipeline zum Kopieren der RetailSales-Cube-Daten führen Sie die folgenden Schritte aus.

1. Wählen Sie im Synapse-Arbeitsbereich die **Integrieren**-Registerkarte aus.
1. Wählen Sie das Pluszeichen (**+**) und wählen Sie dann **Aus Pipeline-Vorlage importieren** aus.
1. Laden Sie die [ExportRetailSalesCubeViews.zip-Datei herunter und wählen Sie sie aus](https://aka.ms/reco-alternate-dataflow-files).
1. Wählen Sie Ihren verknüpften Dienst mit der SQL-Datenbank aus.
1. Wählen Sie Ihren mit dem Speicherkonto verknüpften Dienst aus.
1. Öffnen Sie das **Daten kopieren**-Tool und ändern Sie die **Ordnerpfad**-Eigenschaft in **\<environment_name\>/...**.

### <a name="test-execution-of-the-pipeline"></a>Testausführung der Pipeline

Wir empfehlen, die Pipeline mit nur einer Ansicht zu testen. Die **RetailSales_RetailMediaTemplateView**-Ansicht funktioniert gut, da sie normalerweise weniger als 10 Zeilen enthält.

## <a name="schedule-the-pipeline-to-run-on-a-recurring-schedule"></a>Planen Sie die Pipeline so, dass sie nach einem wiederkehrenden Zeitplan ausgeführt wird

Jedes Mal, wenn die Pipeline ausgeführt wird, findet eine Azure-Nutzung statt. Wir empfehlen, dass Sie Ausführungen in Abständen von 48 Stunden oder länger planen. Sie können die Pipeline jederzeit manuell ausführen, wenn Sie Daten sofort synchronisieren müssen. 
 
## <a name="table-list-for-synchronization-from-dynamics-365-to-data-lake-storage"></a>Tabellenliste für die Synchronisierung von Dynamics 365 zu Data Lake Storage

Die folgende Tabellenliste ist eine Teilmenge aller Tabellen, die für den gesamten RetailSales-Cube erforderlich sind. Nur 15 der Ansichten im RetailSales-Cube werden vom Empfehlungsdienst verwendet, und die Liste der erforderlichen Tabellen wurde entsprechend gefiltert.

### <a name="list-of-retailsales-cube-tables"></a>Liste der RetailSales-Cube-Tabellen

- BICalendarOffsets
- BIDateDimension
- BIDateDimensionValue
- Katalog
- CatalogProduct
- CatalogProductCategory
- CustInvoiceJour
- CustInvoiceTrans
- CustTable
- DataArea
- DimensionAttributeValueCombination
- DimensionAttributeValueSet
- DirPartyTable
- EcoResCategory
- EcoResCategoryHierarchy
- EcoResCategoryHierarchyRole
- EcoResColor
- EcoResConfiguration
- EcoResProduct
- EcoResProductCategory
- EcoResProductTranslation
- EcoResSize
- EcoResStyle
- HcmWorker
- InventDim
- InventDimCombination
- InventItemGroup
- InventItemGroupItem
- InventItemSetupSupplyType
- InventTable
- InventTrans
- LogisticsAddressCountryRegion
- LogisticsAddressCountryRegionTranslation
- LogisticsLocation
- LogisticsPostalAddress
- OMHIERARCHYPURPOSE
- RetailAssortmentLookup
- RetailAssortmentLookupChannelGroup
- RetailChannelProfile
- RetailChannelProfileProperty
- RetailChannelTable
- RetailChannelTableExt
- RetailConnDatabaseProfile
- RetailCustInvoiceJourTable
- RetailCustTable
- RetailMediaTemplate
- RetailOfflineProfile
- RetailPeriodicDiscount
- RetailRecoListConfigurationParameters
- RetailSalesTaxOverrideGroup
- RetailSharedParameters
- RetailSpecialCategoryMember
- RetailTenderTypeCardTable
- RetailTenderTypeTable
- RetailTerminalTable
- RetailTmpProductMedia
- RetailTransactionDiscountTrans
- RetailTransactionPaymentTrans
- RetailTransactionPaymentTransExt
- RetailTransactionSalesTrans
- RetailTransactionSalesTransExt
- RetailTransactionTable
- SalesLine
- SalesTable
- SystemParameters
- RETAILCATALOGINTERNALORG
- RETAILGROUPMEMBERLINE
- RETAILINTERNALORGANIZATION
- RETAILSPECIALCATEGORYPRODUCT
- RETAILPRODUCTCATEGORY
- ECORESCONFIGURATION
- DIMENSIONATTRIBUTE
- DIMENSIONATTRIBUTEVALUESET
- DIMENSIONHIERARCHY
- DIMENSIONHIERARCHYINTEGRATION
- DIMENSIONHIERARCHYLEVEL
- DIMENSIONPARAMETER
- OMExplodedOrganizationSecurityGraph

### <a name="view-list-for-the-parameter-to-pass-to-the-synapse-pipeline"></a>Liste der Parameter, die an die Synapse-Pipeline übergeben werden sollen, anzeigen

Die folgende durch Kommas getrennte Liste enthält die RetailSales-Cube-Ansichten, für die die Pipeline einen „Select“-Vorgang durchführt. Anschließend werden die Ergebnisse in Data Lake Storage kopiert.

RetailSales_RetailAssortmentRulesView,RetailSales_RetailChannelNavigationHierarchiesView,RetailSales_RetailChannelNavigationHierarchyCatalogProductsView,RetailSales_RetailChannelNavigationHierarchyCategoryNodesView,RetailSales_RetailChannelNavigationHierarchyCategoryProductsView,RetailSales_RetailMediaBaseUrlChannelView,RetailSales_RetailMediaRelativeUrlProductView,RetailSales_RetailMediaTemplateView,RetailSales_RetailOptOutCustomersView,RetailSales_RetailProductCategory,RetailSales_RetailProductTransaction,RetailSales_RetailProductVariantDimensionsView,RetailSales_RetailRecoListConfigurationParametersView,RetailSales_RetailRecoListsSharedParametersView,RetailSales_RetailEcoResProductTranslation

> [!IMPORTANT]
> Der Pipelineparameter muss eine Liste von Ansichtsnamen sein, die durch einzelne Kommas getrennt sind. Es dürfen keine Leerzeichen oder Zeilenumbrüche vorhanden sein.

## <a name="environment-specific-fixes"></a>Umgebungsspezifische Korrekturen

### <a name="retailchannelview-fix"></a>RETAILCHANNELVIEW behoben

Die **RETAILCHANNELVIEW**-Ansicht enthält eine fest codierte Ganzzahl, die eine Organisation des Typs „Einzelhandelskanal“ darstellt. Der tatsächliche Wert des Typs kann sich von Umgebung zu Umgebung oder von Mandant zu Mandant ändern.

```SQL
CREATE OR ALTER   VIEW [dbo].[RETAILCHANNELVIEW]
AS
SELECT T1.RECID AS RECID1,
       T1.STOREAREA AS STOREAREA,
       T1.OMOPERATINGUNITID AS OMOPERATINGUNITID,
       T1.DEFAULTCUSTACCOUNT AS DEFAULTCUSTOMER,
       T1.RETAILCHANNELID AS RETAILCHANNELID,
       T1.CHANNELTYPE AS CHANNELTYPE,
       T1.PARTITION AS PARTITION,
       T1.RECID AS RECID,
       T2.OMOPERATINGUNITNUMBER AS OMOPERATINGUNITNUMBER,
       T3.NAME AS NAME
FROM   dbo.RETAILCHANNELTABLE AS T1 CROSS JOIN dbo.DIRPARTYTABLE AS T2 CROSS JOIN dbo.DIRPARTYTABLE AS T3
WHERE  ((((T1.OMOPERATINGUNITID = T2.RECID)
          )
         AND ((T2.RECID = T3.RECID)
              ))
        AND T2.INSTANCERELATIONTYPE IN (8363));
```

Führen Sie die folgenden Schritte aus, um die fest kodierte Ganzzahl zu aktualisieren.

1. Suchen Sie in Dynamics 365 nach dem **ChannelID**-Wert für Ihren Online-Kanal.
1. Führen Sie in einer Instanz von SQL Server Management Studio (SSMS), die an die Synapse-Datenbank angefügt ist, die folgende Abfrage aus.

    ```SQL
    select INSTANCERELATIONTYPE, NAME, NAMEALIAS, * from dbo.DIRPARTYTABLE where RECID IN (select OMOPERATINGUNITID from dbo.RETAILCHANNELTABLE where RETAILCHANNELID =     <channelID>)
    ```

1. Kopieren Sie den Wert aus der ersten Spalte (**INSTANCERELATIONTYPE**), und fügen Sie ihn in die Ansichtsdefinition ein.

## <a name="troubleshooting"></a>Problembehandlung

### <a name="pipeline-task-fails"></a>Pipeline-Aufgabe schlägt fehl

Es sollten 15 Pipeline-Aufgaben-Ausführungen für die **CopyData**-Aufgabe vorhanden sein. Wenn eine Ausführung fehlschlägt, müssen Sie überprüfen, ob alle abhängigen SQL-Objekte vorhanden sind und ob die Abfragen ausgeführt werden. Der einfachste Weg, um zu allen Abhängigkeiten zu gelangen, besteht darin, SSMS zum Herstellen einer Verbindung mit der Datenbank zu verwenden. Sie können dann eine Ansicht auswählen und halten (oder mit der rechten Maustaste darauf klicken) und **CREATE für ein neues Fenster generieren** auswählen.

Die Fehlermeldung könnte den folgenden Text enthalten:

- Fehler: Fehler auf der Seite „Quelle“ aufgetreten
- Fehlerbehandlung bei externer Datei: „Max. Fehleranzahl“.
- /RetailSales/RetailSales_xxxxxx

#### <a name="example-scenario"></a>Beispielszenario

In diesem Beispiel schlägt die **RetailSales_RetailProductCategory**-Aufgabe fehl, und Sie erhalten die Fehlermeldung „Max. Fehleranzahl“.

Um den Fehler zu beheben, gehen Sie folgendermaßen vor.

1. Öffnen Sie die **EntityList.json**-Datei in einem Texteditor (z. B. Visual Studio Code).
1. Suchen Sie die Ansichtsdefinition für **RetailSales_RetailProductCategory**.

    ```SQL
    CREATE  VIEW [dbo].[RetailSales_RetailProductCategory] AS SELECT 0 AS ROW_UNIQUEKEY ,CATEGORY AS CATEGORYID ,PRODUCT AS PRODUCTID ,PRODUCTNAME ,CATEGORYNAME     ,PARENTCATEGORY AS PARENTCATEGORYID ,PARTITION ,RECID FROM RetailProductCategoryView
    ```

1. Diese Ansicht hängt nur von einer anderen Ansicht ab: **RetailProductCategoryView** _. Suchen Sie die Ansichtsdefinition für _*RetailProductCategoryView**.

    ```SQL
    CREATE VIEW [DBO].[RETAILPRODUCTCATEGORYVIEW] AS SELECT T1.CATEGORY AS CATEGORY, T1.PRODUCT AS PRODUCT, T1.PARTITION AS PARTITION, T1.RECID AS RECID, T2.PRODUCTNAME AS PRODUCTNAME, T2.PARTITION AS PARTITION#2, T3.NAME AS CATEGORYNAME, T3.PARENTCATEGORY AS PARENTCATEGORY, T3.PARTITION AS PARTITION#3 FROM RETAILPRODUCTCATEGORY T1 CROSS JOIN ECORESPRODUCTTRANSLATIONS T2 CROSS JOIN RETAILCATEGORYEXPANDED T3 WHERE((( T1.PRODUCT = T2.PRODUCT) AND ( T1.PARTITION = T2.PARTITION)) AND (( T1.CATEGORY = T3.RECID) AND ( T1.PARTITION = T3.PARTITION)))
    ```

1. Diese Ansicht hängt von drei anderen Ansichten ab: **RETAILPRODUCTCATEGORY**, **ECORESPRODUCTTRANSLATIONS** und **RETAILCATEGORYEXPANDED**. Suchen Sie die Definition für jede dieser Ansichten und listen Sie ihre Abhängigkeiten auf. Fahren Sie fort, bis Sie alle abhängigen Ansichten gefunden haben.

    Hier ist die gesamte Liste in der Reihenfolge der Abhängigkeitsbäume. Dreizehn Ansichten müssen validiert werden.

    - RetailSales_RetailProductCategory

        - RetailProductCategoryView

            - RETAILPRODUCTCATEGORY

                - ECORESPRODUCTCATEGORY
                - ECORESCATEGORYHIERARCHYROLE
                - RETAILSPECIALCATEGORYPRODUCT

                    - ECORESPRODUCT
                    - RETAILGROUPMEMBERLINE
                    - RETAILSPECIALCATEGORYMEMBER

            - ECORESPRODUCTTRANSLATIONS

                - ECORESPRODUCT
                - ECORESPRODUCTTRANSLATION
                - SYSTEMPARAMETERS

            - RETAILCATEGORYEXPANDED

                - ECORESCATEGORY
                - ECORESCATEGORYHIERARCHYROLE

1. Erstellen Sie in Excel die folgenden 13 **select count(\*) from \<view_name\>**-Anweisungen. Führen Sie diese Anweisungen in SSMS aus und senden Sie die Ergebnisse an Text. Scrollen Sie dann durch die Ergebnisse, um zu sehen, ob eine der Ansichten fehlgeschlagen ist. Der anfängliche Fehler deutet darauf hin, dass mindestens eine der Ansichten fehlschlagen wird.

    ```SQL
    select count(*) from RetailProductCategoryView
    select count(*) from RETAILPRODUCTCATEGORY
    select count(*) from ECORESPRODUCTCATEGORY
    select count(*) from ECORESCATEGORYHIERARCHYROLE
    select count(*) from RETAILSPECIALCATEGORYPRODUCT
    select count(*) from ECORESPRODUCT
    select count(*) from RETAILGROUPMEMBERLINE
    select count(*) from RETAILSPECIALCATEGORYMEMBER
    select count(*) from ECORESPRODUCTTRANSLATIONS
    select count(*) from ECORESPRODUCTTRANSLATION
    select count(*) from SYSTEMPARAMETERS
    select count(*) from RETAILCATEGORYEXPANDED
    select count(*) from ECORESCATEGORY
    ```

1. Eine Möglichkeit, das Gesehene zu validieren, besteht darin, eine stammabhängige Ansicht zu erstellen, um die Ansichtsdefinition in SSMS zu generieren. Stellen Sie dann sicher, dass eine Azure Data Lake-Dateispalte namens **r.filepath** vorhanden ist. Das Vorhandensein dieser Spalte weist darauf hin, dass die Ansicht, die Sie überprüfen, Daten aus Data Lake Storage liest.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über Produktempfehlungen](product-recommendations.md)

[Aktivieren von Azure Data Lake Storage in einer Dynamics 365 Commerce Umgebung](enable-adls-environment.md)

[Personalisierte Empfehlungen aktivieren](personalized-recommendations.md)

[Die Empfehlungen „Produkte mit ähnlichem Aussehen kaufen“ aktivieren](shop-similar-looks.md)

[Personalisierte Empfehlungen kündigen](personalization-gdpr.md)

[Produktempfehlungen am POS hinzufügen](product.md)

[Empfehlungen zum Transaktionsbildschirm hinzufügen](add-recommendations-control-pos-screen.md)

[Anpassung der Ergebnisse der AI-ML-Empfehlungen](modify-product-recommendation-results.md)

[Manuell kuratierte Empfehlungen erstellen](create-editorial-recommendation-lists.md)

[Empfehlungen mit Demodaten erstellen](product-recommendations-demo-data.md)

[Produktempfehlungs-FAQs](faq-recommendations.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
