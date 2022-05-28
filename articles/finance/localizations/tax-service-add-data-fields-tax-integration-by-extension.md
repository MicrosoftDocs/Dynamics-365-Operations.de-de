---
title: Datenfelder in die Steuerintegration mithilfe von Erweiterungen einfügen
description: In diesem Thema wird erläutert, wie Sie mithilfe von X++-Erweiterungen Datenfelder in die Steuerintegration einfügen.
author: qire
ms.date: 04/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 64c68ef6804297f86b5d9dc1933b0c16a0d42aae
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8695387"
---
# <a name="add-data-fields-in-the-tax-integration-by-using-extension"></a>Datenfelder in die Steuerintegration mithilfe von Erweiterungen einfügen

[!include [banner](../includes/banner.md)]


In diesem Thema wird erläutert, wie Sie mithilfe von X++-Erweiterungen Datenfelder in die Steuerintegration einfügen. Diese Felder können auf das Steuerdatenmodell des Steuerdienstes erweitert und zur Ermittlung von Steuercodes verwendet werden. Weitere Informationen finden Sie unter [Datenfelder in Steuerkonfigurationen hinzufügen](tax-service-add-data-fields-tax-configurations.md).

## <a name="data-model"></a>Datenmodell

Die Daten im Datenmodell werden von Objekten getragen und von Klassen implementiert.

Dies sind die wesentlichen Objekte:

* AxClass/TaxIntegration **Document** Object
* AxClass/TaxIntegration **Line** Object
* AxClass/TaxIntegration **TaxLine** Object

Die folgende Abbildung zeigt, wie diese Objekte zusammenhängen.

[![Datenmodell-Objektbeziehung.](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)

Ein **Dokument**-Objekt kann viele **Position**-Objekte enthalten. Jedes Objekt enthält Metadaten für den Steuerdienst.

- `TaxIntegrationDocumentObject` hat `originAddress`-Metadaten, die Informationen zur Quelladresse enthalten, und `includingTax`-Metadaten, die angeben, ob der Positionsbetrag die Mehrwertsteuer enthält.
- `TaxIntegrationLineObject` hat `itemId`-, `quantity`- und `categoryId`-Metadaten.

> [!NOTE]
> `TaxIntegrationLineObject` implementiert auch **Belastung**-Objekte.

## <a name="integration-flow"></a>Integrationsflow

Die Daten im Flow werden durch Aktivitäten manipuliert.

### <a name="key-activities"></a>Schlüsselaktivitäten

* AxClass/TaxIntegration **Calculation** ActivityOnDocument
* AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument
* AxClass/TaxIntegration **DataPersistence** ActivityOnDocument
* AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument
* AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument

Die Aktivitäten werden in der folgenden Reihenfolge ausgeführt:

1. Einstellungsabruf
2. Datenabruf
3. Berechnungsdienst
4. Währungswechselkurs
5. Datenpersistenz

Erweitern Sie zum Beispiel **Datenabruf** vor **Berechnungsservice**.

#### <a name="data-retrieval-activities"></a>Datenabrufaktivitäten

**Datenabruf**-Aktivitäten rufen Daten aus der Datenbank ab. Adapter für verschiedene Transaktionen stehen zum Abrufen von Daten aus verschiedenen Transaktionstabellen zur Verfügung:

- AxClass/TaxIntegration **PurchTable** DataRetrieval
- AxClass/TaxIntegration **PurchParmTable** DataRetrieval
- AxClass/TaxIntegration **PurchREQTable** DataRetrieval
- AxClass/TaxIntegration **PurchRFQTable** DataRetrieval
- AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval
- AxClass/TaxIntegration **SalesTable** DataRetrieval
- AxClass/TaxIntegration **SalesParm** DataRetrieval

In diesen **Datenabruf**-Aktivitäten werden Daten aus der Datenbank nach `TaxIntegrationDocumentObject` und `TaxIntegrationLineObject` kopiert. Da alle diese Aktivitäten dieselbe abstrakte Vorlagenklasse erweitern, verfügen sie über gemeinsame Methoden.

#### <a name="calculation-service-activities"></a>Berechnungsdienstaktivitäten

Die **Berechnungsdienst**-Aktivität ist die Verbindung zwischen dem Steuerdienst und der Steuerintegration. Diese Aktivität ist für folgende Funktionen verantwortlich:

1. Konstruieren der Anforderung.
2. Senden der Anforderung an den Steuerdienst.
3. Erhalten der Antwort vom Steuerdienst.
4. Analysieren der Antwort.

Ein Datenfeld, das Sie der Anforderung hinzufügen, wird zusammen mit anderen Metadaten gesendet. 

## <a name="extension-implementation"></a>Implementierung der Erweiterung

Dieser Abschnitt enthält detaillierte Schritte, in denen die Implementierung der Erweiterung erläutert wird. Er verwendet die Finanzdimensionen **Kostenstelle** und **Projekt** als Beispiele.

### <a name="step-1-add-the-data-variable-in-the-object-class"></a>Schritt 1. Datenvariable in die Objektklasse einfügen

Die Objektklasse enthält die Datenvariablen und Getter-/Setter-Methoden für die Daten. Fügen Sie das Datenfeld entweder `TaxIntegrationDocumentObject` oder `TaxIntegrationLineObject` hinzu, abhängig von der Ebene des Feldes. Im folgenden Beispiel wird die Positionsebene verwendet, und der Dateiname lautet `TaxIntegrationLineObject_Extension.xpp`.

> [!NOTE]
> Wenn sich das hinzugefügte Datenfeld auf Dokumentebene befindet, ändern Sie den Dateinamen in `TaxIntegrationDocumentObject_Extension.xpp`.

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

**Kostenstelle** und **Projekt** werden als private Variablen hinzugefügt. Erstellen Sie Getter- und Setter-Methoden für diese Datenfelder, um die Daten zu bearbeiten.

### <a name="step-2-retrieve-data-from-the-database"></a>Schritt 2. Daten aus der Datenbank abrufen

Geben Sie die Transaktion an und erweitern Sie die entsprechenden Adapterklassen, um die Daten abzurufen. Zum Beispiel, wenn Sie eine **Bestellung**-Transaktion verwenden, müssen Sie `TaxIntegrationPurchTableDataRetrieval` und `TaxIntegrationVendInvoiceInfoTableDataRetrieval` erweitern. 

> [!NOTE]
> `TaxIntegrationPurchParmTableDataRetrieval` wird von `TaxIntegrationPurchTableDataRetrieval` geerbt. Es sollte nicht geändert werden, es sei denn, die Logik der Tabellen `purchTable` und `purchParmTable` unterscheidet sich.

Wenn das Datenfeld für alle Transaktionen hinzugefügt werden soll, erweitern Sie alle `DataRetrieval`-Klassen.

Weil alle **Datenabruf**-Aktivitäten dieselbe Vorlagenklasse erweitern, sind die Klassenstrukturen, Variablen und Methoden ähnlich.

```X++
protected TaxIntegrationDocumentObject document;

/// <summary>
/// Copies to the document.
/// </summary>
protected abstract void copyToDocument()
{
    // It is recommended to implement as:
    //
    // this.copyToDocumentByDefault();
    // this.copyToDocumentFromHeaderTable();
    // this.copyAddressToDocument();
}
 
/// <summary>
/// Copies to the current line of the document.
/// </summary>
/// <param name = "_line">The current line of the document.</param>
protected abstract void copyToLine(TaxIntegrationLineObject _line)
{
    // It is recommended to implement as:
    //
    // this.copyToLineByDefault(_line);
    // this.copyToLineFromLineTable(_line);
    // this.copyQuantityAndTransactionAmountToLine(_line);
    // this.copyAddressToLine(_line);
    // this.copyToLineFromHeaderTable(_line);
}
```

Das folgende Beispiel zeigt die Grundstruktur, wenn die `PurchTable`-Tabelle verwendet wird.

```X++
public class TaxIntegrationPurchTableDataRetrieval extends TaxIntegrationAbstractDataRetrievalTemplate
{
    protected PurchTable purchTable;
    protected PurchLine purchLine;

    // Query builder methods
    [Replaceable]
    protected SysDaQueryObject getDocumentQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineQueryObject()
    [Replaceable]
    protected SysDaQueryObject getDocumentChargeQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineChargeQueryObject()

    // Data retrieval methods
    protected void copyToDocument()
    protected void copyToDocumentFromHeaderTable()
    protected void copyToLine(TaxIntegrationLineObject _line)
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    ...
}
```

Wenn die `CopyToDocument`-Methode aufgerufen wird, existiert der `this.purchTable`-Puffer bereits. Der Zweck dieser Methode besteht darin, alle erforderlichen Daten von `this.purchTable` zum `document`-Objekt mit der Setter-Methode zu kopieren, die in der `DocumentObject`-Klasse erstellt wurde.

Ebenso existiert bereits ein `this.purchLine`-Puffer in der `CopyToLine`-Methode. Der Zweck dieser Methode besteht darin, alle erforderlichen Daten von `this.purchLine` zum `_line`-Objekt mit der Setter-Methode zu kopieren, die in der `LineObject`-Klasse erstellt wurde.

Der einfachste Ansatz ist die Erweiterung der `CopyToDocument`- und `CopyToLine`-Methoden. Wir empfehlen jedoch, dass Sie die Methoden `copyToDocumentFromHeaderTable` und `copyToLineFromLineTable` zuerst versuchen. Wenn sie nicht wie gewünscht funktionieren, implementieren Sie Ihre eigene Methode und rufen Sie sie in `CopyToDocument` und `CopyToLine` auf. Es gibt drei häufige Situationen, in denen Sie diesen Ansatz verwenden können:

- Das erforderliche Feld befindet sich in `PurchTable` oder `PurchLine`. In dieser Situation können Sie `copyToDocumentFromHeaderTable` und `copyToLineFromLineTable` erweitern. Hier ist der Beispielcode.

    ```X++
    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        next copyToLineFromLineTable(_line);
        // if we already added XXX in TaxIntegrationLineObject
        _line.setXXX(this.purchLine.XXX);
    }
    ```

- Die erforderlichen Daten befinden sich nicht in der Standardtabelle der Transaktion. Es gibt jedoch einige Verknüpfungsbeziehungen mit der Standardtabelle, und das Feld ist in den meisten Zeilen erforderlich. In dieser Situation ersetzen Sie `getDocumentQueryObject` oder `getLineObject`, um die Tabelle nach Verknüpfungsbeziehung abzufragen. Im folgenden Beispiel wird das Feld **Jetzt liefern** auf Positionsebene in den Auftrag integriert.

    ```X++
    public class TaxIntegrationSalesTableDataRetrieval
    {
        protected MCRSalesLineDropShipment mcrSalesLineDropShipment;

        /// <summary>
        /// Gets the query for the lines of the document.
        /// </summary>
        /// <returns>The query for the lines of the document</returns>
        [Replaceable]
        protected SysDaQueryObject getLineQueryObject()
        {
            return SysDaQueryObjectBuilder::from(this.salesLine)
                .where(this.salesLine, fieldStr(SalesLine, SalesId)).isEqualToLiteral(this.salesTable.SalesId)
                .outerJoin(this.mcrSalesLineDropShipment)
                .where(this.mcrSalesLineDropShipment, fieldStr(MCRSalesLineDropShipment, SalesLine)).isEqualTo(this.salesLine, fieldStr(SalesLine, RecId))
                .toSysDaQueryObject();
        }
    }
    ```

    In diesem Beispiel wird ein `mcrSalesLineDropShipment`-Puffer deklariert und die Abfrage in `getLineQueryObject` definiert. Die Abfrage verwendet die Beziehung `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`. Während Sie in dieser Situation erweitern, können Sie `getLineQueryObject` mit Ihrem eigenen konstruierten Abfrageobjekt ersetzen. Beachten Sie jedoch die folgenden Punkte:

    * Weil der Rückgabewert der `getLineQueryObject`-Methode `SysDaQueryObject` ist, müssen Sie dieses Objekt mithilfe des SysDa-Ansatzes erstellen.
    * Vorhandene Tabelle kann nicht entfernt werden.

- Die erforderlichen Daten werden durch eine komplizierte Verknüpfungsbeziehung mit der Transaktionstabelle verknüpft, oder die Beziehung ist nicht eins zu eins (1:1), sondern eins zu viele (1:N). In dieser Situation werden die Dinge etwas kompliziert. Diese Situation gilt für das Beispiel der Finanzdimensionen. 

    In dieser Situation können Sie Ihre eigene Methode zum Abrufen der Daten implementieren. Hier ist der Beispielcode in der `TaxIntegrationPurchTableDataRetrieval_Extension.xpp`-Datei.

    ```X++
    [ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
    final class TaxIntegrationPurchTableDataRetrieval_Extension
    {
        private const str CostCenterKey = 'CostCenter';
        private const str ProjectKey = 'Project';

        /// <summary>
        /// Copies to the current line of the document from.
        /// </summary>
        /// <param name = "_line">The current line of the document.</param>
        protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
        {
            Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
            if (dimensionAttributeMap.exists(CostCenterKey))
            {
                _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
            }
            if (dimensionAttributeMap.exists(ProjectKey))
            {
                _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
            }
            next copyToLineFromLineTable(_line);
        }
        private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
        {
            DimensionAttribute dimensionAttribute;
            DimensionAttributeValue dimensionAttributeValue;
            DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
            Map ret = new Map(Types::String, Types::String);

            select Name, RecId from dimensionAttribute
                join dimensionAttributeValue
                    where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
                join DimensionAttributeValueSetItem
                    where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                        && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;

            while(dimensionAttribute.RecId)
            {
                ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
                next dimensionAttribute;
            }
            return ret;
        }
    }
    ```

### <a name="step-3-add-data-to-the-request"></a>Schritt 3. Daten zur Anforderung hinzufügen

Erweitern Sie die Methode `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` oder `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` zum Hinzufügen von Daten zur Anforderung. Hier ist der Beispielcode in der `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp`-Datei.

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define the field name in the request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';
    // private const str IOEnumExample = 'Enum Example';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());

        // If the field to be extended is an enum type, use enum2Symbol to convert an enum variable exampleEnum of ExampleEnumType to a string
        // _destination.SetField(IOEnumExample, enum2Symbol(enumNum(ExampleEnumType), _source.getExampleEnum()));
    }
}
```

In diesem Code ist `_destination` das Wrapper-Objekt, mit dem die Anforderung generiert wird, und `_source` ist das `TaxIntegrationLineObject`-Objekt.

> [!NOTE]
> Definieren Sie den Feldnamen, der im Anforderungsformular verwendet wird, als **private const str**. Die Zeichenfolge sollte genau mit dem im Thema [Datenfelder in Steuerkonfigurationen hinzufügen](tax-service-add-data-fields-tax-configurations.md) hinzugefügten Knotennamen (nicht das Etikett) übereinstimmen.
> 
> Legen Sie das Feld in der Methode **copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine** mit der **SetField**-Methode fest. Der Datentyp des zweiten Parameters sollte **Zeichenfolge** sein. Wenn der Datentyp nicht **Zeichenfolge** ist, konvertieren Sie ihn zu einer Zeichenfolge.
> Wenn der Datentyp X++ **enum-Typ** ist, empfehlen wir die Verwendung der **enum2Symbol**-Methode zum Konvertieren des Enumerationswerts in eine Zeichenfolge. Der in der Steuerkonfiguration hinzugefügte Enumerationswert sollte genau mit dem Enumerationsnamen übereinstimmen. Im Folgenden finden Sie eine Liste der Unterschiede zwischen Enumerationswert, Etikett und Name.
> 
>   - Der Name der Enumeration ist ein symbolischer Name im Code. **enum2Symbol()** kann den Enumerationswert zu seinem Namen konvertieren.
>   - Der Enumerationswert ist ein Integer.
>   - Die Bezeichnung der Enumeration kann in den bevorzugten Sprachen unterschiedlich sein. **enum2Str()** kann den Enumerationswert zu seinem Etikett konvertieren.

## <a name="model-dependency"></a>Modellabhängigkeit

Um das Projekt erfolgreich zu erstellen, fügen Sie die folgenden Referenzmodelle zu den Modellabhängigkeiten hinzu:

- ApplicationPlatform
- ApplicationSuite
- Steuermodul
- Dimensionen, wenn die Finanzdimension verwendet wird
- Andere notwendige Modelle, auf die im Code verwiesen wird

## <a name="validation"></a>Prüfung

Nachdem Sie die vorherigen Schritte erledigt haben, können Sie Ihre Änderungen validieren.

1. Gehen Sie in Finance zu **Kreditorenkonten** und fügen Sie der URL **&debug=vs%2CconfirmExit&** hinzu. Zum Beispiel: `https://usnconeboxax1aos.cloud.onebox.dynamics.com/?cmp=DEMF&mi=PurchTableListPage&debug=vs%2CconfirmExit&`. Das **&** am Ende darf auf keinen Fall fehlen.
2. Öffnen Sie die Seite **Bestellung** und wählen Sie **Neu** aus, um eine Bestellung zu erstellen.
3. Legen Sie den Wert für das angepasste Feld fest und wählen Sie dann **Mehrwertsteuer** aus. Eine Problembehebungsdatei mit dem Präfix **TaxServiceTroubleshootingLog** wird automatisch heruntergeladen. Diese Datei enthält die an den Steuerberechnungsdienst gesendeten Transaktionsinformationen. 
4. Überprüfen Sie, ob das hinzugefügte angepasste Feld im Abschnitt **JSON-Eingabe für die Steuerdienstberechnung** vorhanden und ob sein Wert korrekt ist. Wenn der Wert nicht korrekt ist, gehen Sie die Schritte in diesem Dokument noch einmal durch.

Dateibeispiel:

```
===Tax service calculation input JSON:===
{
  "TaxableDocument": {
    "Header": [
      {
        "Lines": [
          {
            "Line Type": "Normal",
            "Item Code": "",
            "Item Type": "Item",
            "Quantity": 0.0,
            "Amount": 1000.0,
            "Currency": "EUR",
            "Transaction Date": "2022-1-26T00:00:00",
            ...
            /// The new fields added at line level
            "Cost Center": "003",
            "Project": "Proj-123"
          }
        ],
        "Amount include tax": true,
        "Business Process": "Journal",
        "Currency": "",
        "Vendor Account": "DE-001",
        "Vendor Invoice Account": "DE-001",
        ...
        // The new fields added at header level, no new fields in this example
        ...
      }
    ]
  },
}
...
```

## <a name="appendix"></a>Anhang

Dieser Anhang zeigt den vollständigen Beispielcode für die Integration der Finanzdimensionen **Kostenstelle** und **Projekt** auf Positionsebene an.

### <a name="taxintegrationlineobject_extensionxpp"></a>TaxIntegrationLineObject_Extension.xpp

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

### <a name="taxintegrationpurchtabledataretrieval_extensionxpp"></a>TaxIntegrationPurchTableDataRetrieval_Extension.xpp

```X++
[ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
final class TaxIntegrationPurchTableDataRetrieval_Extension
{
    private const str CostCenterKey = 'CostCenter';
    private const str ProjectKey = 'Project';

    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
        if (dimensionAttributeMap.exists(CostCenterKey))
        {
            _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
        }
        if (dimensionAttributeMap.exists(ProjectKey))
        {
            _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
        }
        next copyToLineFromLineTable(_line);
    }
    private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
    {
        DimensionAttribute dimensionAttribute;
        DimensionAttributeValue dimensionAttributeValue;
        DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
        Map ret = new Map(Types::String, Types::String);
        select Name, RecId from dimensionAttribute
            join dimensionAttributeValue
                where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
            join DimensionAttributeValueSetItem
                where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                    && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;
        while(dimensionAttribute.RecId)
        {
            ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
            next dimensionAttribute;
        }
        return ret;
    }
}
```

### <a name="taxintegrationcalculationactivityondocument_calculationservice_extensionxpp"></a>TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define the field name in the request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```
