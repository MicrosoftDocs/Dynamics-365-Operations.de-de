---
title: Datenfelder in die Steuerintegration mithilfe von Erweiterungen einfügen
description: In diesem Thema wird erläutert, wie Sie mithilfe von X++-Erweiterungen Datenfelder in die Steuerintegration einfügen.
author: qire
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 8e3573f9c9971d4a5af33ece08b7e0b43f2e813a
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921164"
---
# <a name="add-data-fields-in-the-tax-integration-by-using-extension"></a><span data-ttu-id="c5a44-103">Datenfelder in die Steuerintegration mithilfe von Erweiterungen einfügen</span><span class="sxs-lookup"><span data-stu-id="c5a44-103">Add data fields in the tax integration by using extension</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="c5a44-104">In diesem Thema wird erläutert, wie Sie mithilfe von X++-Erweiterungen Datenfelder in die Steuerintegration einfügen.</span><span class="sxs-lookup"><span data-stu-id="c5a44-104">This topic explains how to use X++ extensions to add data fields in the tax integration.</span></span> <span data-ttu-id="c5a44-105">Diese Felder können auf das Steuerdatenmodell des Steuerdienstes erweitert und zur Ermittlung von Steuercodes verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c5a44-105">These fields can be extended to the tax data model of the tax service and used to determine tax codes.</span></span> <span data-ttu-id="c5a44-106">Weitere Informationen finden Sie unter [Datenfelder in Steuerkonfigurationen hinzufügen](tax-service-add-data-fields-tax-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="c5a44-106">For more information, see [Add data fields in tax configurations](tax-service-add-data-fields-tax-configurations.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="c5a44-107">Datenmodell</span><span class="sxs-lookup"><span data-stu-id="c5a44-107">Data model</span></span>

<span data-ttu-id="c5a44-108">Die Daten im Datenmodell werden von Objekten getragen und von Klassen implementiert.</span><span class="sxs-lookup"><span data-stu-id="c5a44-108">The data in the data model is carried by objects and implemented by classes.</span></span>

<span data-ttu-id="c5a44-109">Dies sind die wesentlichen Objekte:</span><span class="sxs-lookup"><span data-stu-id="c5a44-109">Here is a list of the major objects:</span></span>

* <span data-ttu-id="c5a44-110">AxClass/TaxIntegration **Document** Object</span><span class="sxs-lookup"><span data-stu-id="c5a44-110">AxClass/TaxIntegration **Document** Object</span></span>
* <span data-ttu-id="c5a44-111">AxClass/TaxIntegration **Line** Object</span><span class="sxs-lookup"><span data-stu-id="c5a44-111">AxClass/TaxIntegration **Line** Object</span></span>
* <span data-ttu-id="c5a44-112">AxClass/TaxIntegration **TaxLine** Object</span><span class="sxs-lookup"><span data-stu-id="c5a44-112">AxClass/TaxIntegration **TaxLine** Object</span></span>

<span data-ttu-id="c5a44-113">Die folgende Abbildung zeigt, wie diese Objekte zusammenhängen.</span><span class="sxs-lookup"><span data-stu-id="c5a44-113">The following illustration shows how these objects are related.</span></span>

<span data-ttu-id="c5a44-114">[![Datenmodell-Objektbeziehung](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)</span><span class="sxs-lookup"><span data-stu-id="c5a44-114">[![Data model object relationship](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)</span></span>

<span data-ttu-id="c5a44-115">Ein **Dokument**-Objekt kann viele **Position**-Objekte enthalten.</span><span class="sxs-lookup"><span data-stu-id="c5a44-115">A **Document** object can contain many **Line** objects.</span></span> <span data-ttu-id="c5a44-116">Jedes Objekt enthält Metadaten für den Steuerdienst.</span><span class="sxs-lookup"><span data-stu-id="c5a44-116">Each object contains metadata for the tax service.</span></span>

- <span data-ttu-id="c5a44-117">`TaxIntegrationDocumentObject` hat `originAddress`-Metadaten, die Informationen zur Quelladresse enthalten, und `includingTax`-Metadaten, die angeben, ob der Positionsbetrag die Mehrwertsteuer enthält.</span><span class="sxs-lookup"><span data-stu-id="c5a44-117">`TaxIntegrationDocumentObject` has `originAddress` metadata, which contains information about the source address, and `includingTax` metadata, which indicates whether the line amount includes sales tax.</span></span>
- <span data-ttu-id="c5a44-118">`TaxIntegrationLineObject`hat `itemId`-,`quantity`- und`categoryId`-Metadaten.</span><span class="sxs-lookup"><span data-stu-id="c5a44-118">`TaxIntegrationLineObject` has `itemId`, `quantity`, and `categoryId` metadata.</span></span>

> [!NOTE]
> <span data-ttu-id="c5a44-119">`TaxIntegrationLineObject`implementiert auch **Belastung**-Objekte.</span><span class="sxs-lookup"><span data-stu-id="c5a44-119">`TaxIntegrationLineObject` also implements **Charge** objects.</span></span>

## <a name="integration-flow"></a><span data-ttu-id="c5a44-120">Integrationsflow</span><span class="sxs-lookup"><span data-stu-id="c5a44-120">Integration flow</span></span>

<span data-ttu-id="c5a44-121">Die Daten im Flow werden durch Aktivitäten manipuliert.</span><span class="sxs-lookup"><span data-stu-id="c5a44-121">The data in the flow is manipulated by activities.</span></span>

### <a name="key-activities"></a><span data-ttu-id="c5a44-122">Schlüsselaktivitäten</span><span class="sxs-lookup"><span data-stu-id="c5a44-122">Key activities</span></span>

* <span data-ttu-id="c5a44-123">AxClass/TaxIntegration **Calculation** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="c5a44-123">AxClass/TaxIntegration **Calculation** ActivityOnDocument</span></span>
* <span data-ttu-id="c5a44-124">AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="c5a44-124">AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument</span></span>
* <span data-ttu-id="c5a44-125">AxClass/TaxIntegration **DataPersistence** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="c5a44-125">AxClass/TaxIntegration **DataPersistence** ActivityOnDocument</span></span>
* <span data-ttu-id="c5a44-126">AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="c5a44-126">AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument</span></span>
* <span data-ttu-id="c5a44-127">AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="c5a44-127">AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument</span></span>

<span data-ttu-id="c5a44-128">Die Aktivitäten werden in der folgenden Reihenfolge ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="c5a44-128">Activities are run in the following order:</span></span>

1. <span data-ttu-id="c5a44-129">Einstellungsabruf</span><span class="sxs-lookup"><span data-stu-id="c5a44-129">Setting Retrieval</span></span>
2. <span data-ttu-id="c5a44-130">Datenabruf</span><span class="sxs-lookup"><span data-stu-id="c5a44-130">Data Retrieval</span></span>
3. <span data-ttu-id="c5a44-131">Berechnungsdienst</span><span class="sxs-lookup"><span data-stu-id="c5a44-131">Calculation Service</span></span>
4. <span data-ttu-id="c5a44-132">Währungswechselkurs</span><span class="sxs-lookup"><span data-stu-id="c5a44-132">Currency Exchange</span></span>
5. <span data-ttu-id="c5a44-133">Datenpersistenz</span><span class="sxs-lookup"><span data-stu-id="c5a44-133">Data Persistence</span></span>

<span data-ttu-id="c5a44-134">Erweitern Sie zum Beispiel **Datenabruf** vor **Berechnungsservice**.</span><span class="sxs-lookup"><span data-stu-id="c5a44-134">For example, extend **Data Retrieval** before **Calculation Service**.</span></span>

#### <a name="data-retrieval-activities"></a><span data-ttu-id="c5a44-135">Datenabrufaktivitäten</span><span class="sxs-lookup"><span data-stu-id="c5a44-135">Data Retrieval activities</span></span>

<span data-ttu-id="c5a44-136">**Datenabruf**-Aktivitäten rufen Daten aus der Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="c5a44-136">**Data Retrieval** activities retrieve data from the database.</span></span> <span data-ttu-id="c5a44-137">Adapter für verschiedene Transaktionen stehen zum Abrufen von Daten aus verschiedenen Transaktionstabellen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="c5a44-137">Adapters for different transactions are available to retrieve data from different transaction tables:</span></span>

- <span data-ttu-id="c5a44-138">AxClass/TaxIntegration **PurchTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="c5a44-138">AxClass/TaxIntegration **PurchTable** DataRetrieval</span></span>
- <span data-ttu-id="c5a44-139">AxClass/TaxIntegration **PurchParmTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="c5a44-139">AxClass/TaxIntegration **PurchParmTable** DataRetrieval</span></span>
- <span data-ttu-id="c5a44-140">AxClass/TaxIntegration **PurchREQTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="c5a44-140">AxClass/TaxIntegration **PurchREQTable** DataRetrieval</span></span>
- <span data-ttu-id="c5a44-141">AxClass/TaxIntegration **PurchRFQTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="c5a44-141">AxClass/TaxIntegration **PurchRFQTable** DataRetrieval</span></span>
- <span data-ttu-id="c5a44-142">AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="c5a44-142">AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval</span></span>
- <span data-ttu-id="c5a44-143">AxClass/TaxIntegration **SalesTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="c5a44-143">AxClass/TaxIntegration **SalesTable** DataRetrieval</span></span>
- <span data-ttu-id="c5a44-144">AxClass/TaxIntegration **SalesParm** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="c5a44-144">AxClass/TaxIntegration **SalesParm** DataRetrieval</span></span>

<span data-ttu-id="c5a44-145">In diesen **Datenabruf**-Aktivitäten werden Daten aus der Datenbank nach `TaxIntegrationDocumentObject` und `TaxIntegrationLineObject` kopiert.</span><span class="sxs-lookup"><span data-stu-id="c5a44-145">In these **Data Retrieval** activities, data is copied from the database to `TaxIntegrationDocumentObject` and `TaxIntegrationLineObject`.</span></span> <span data-ttu-id="c5a44-146">Da alle diese Aktivitäten dieselbe abstrakte Vorlagenklasse erweitern, verfügen sie über gemeinsame Methoden.</span><span class="sxs-lookup"><span data-stu-id="c5a44-146">Because all these activities extend the same abstract template class, they have common methods.</span></span>

#### <a name="calculation-service-activities"></a><span data-ttu-id="c5a44-147">Berechnungsdienstaktivitäten</span><span class="sxs-lookup"><span data-stu-id="c5a44-147">Calculation Service activities</span></span>

<span data-ttu-id="c5a44-148">Die **Berechnungsdienst**-Aktivität ist die Verbindung zwischen dem Steuerdienst und der Steuerintegration.</span><span class="sxs-lookup"><span data-stu-id="c5a44-148">The **Calculation Service** activity is the link between the tax service and the tax integration.</span></span> <span data-ttu-id="c5a44-149">Diese Aktivität ist für folgende Funktionen verantwortlich:</span><span class="sxs-lookup"><span data-stu-id="c5a44-149">This activity is responsible for the following functions:</span></span>

1. <span data-ttu-id="c5a44-150">Konstruieren der Anforderung.</span><span class="sxs-lookup"><span data-stu-id="c5a44-150">Construct the request.</span></span>
2. <span data-ttu-id="c5a44-151">Senden der Anforderung an den Steuerdienst.</span><span class="sxs-lookup"><span data-stu-id="c5a44-151">Post the request to the tax service.</span></span>
3. <span data-ttu-id="c5a44-152">Erhalten der Antwort vom Steuerdienst.</span><span class="sxs-lookup"><span data-stu-id="c5a44-152">Get the response from the tax service.</span></span>
4. <span data-ttu-id="c5a44-153">Analysieren der Antwort.</span><span class="sxs-lookup"><span data-stu-id="c5a44-153">Parse the response.</span></span>

<span data-ttu-id="c5a44-154">Ein Datenfeld, das Sie der Anforderung hinzufügen, wird zusammen mit anderen Metadaten gesendet.</span><span class="sxs-lookup"><span data-stu-id="c5a44-154">A data field that you add to the request will be posted together with other metadata.</span></span> 

## <a name="extension-implementation"></a><span data-ttu-id="c5a44-155">Implementierung der Erweiterung</span><span class="sxs-lookup"><span data-stu-id="c5a44-155">Extension implementation</span></span>

<span data-ttu-id="c5a44-156">Dieser Abschnitt enthält detaillierte Schritte, in denen die Implementierung der Erweiterung erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="c5a44-156">This section provides detailed steps that explain how to implement the extension.</span></span> <span data-ttu-id="c5a44-157">Er verwendet die Finanzdimensionen **Kostenstelle** und **Projekt** als Beispiele.</span><span class="sxs-lookup"><span data-stu-id="c5a44-157">It uses the **Cost center** and **Project** financial dimensions as examples.</span></span>

### <a name="step-1-add-the-data-variable-in-the-object-class"></a><span data-ttu-id="c5a44-158">Schritt 1.</span><span class="sxs-lookup"><span data-stu-id="c5a44-158">Step 1.</span></span> <span data-ttu-id="c5a44-159">Datenvariable in die Objektklasse einfügen</span><span class="sxs-lookup"><span data-stu-id="c5a44-159">Add the data variable in the object class</span></span>

<span data-ttu-id="c5a44-160">Die Objektklasse enthält die Datenvariablen und Getter-/Setter-Methoden für die Daten.</span><span class="sxs-lookup"><span data-stu-id="c5a44-160">The object class contains the data variable and getter/setter methods for the data.</span></span> <span data-ttu-id="c5a44-161">Fügen Sie das Datenfeld entweder `TaxIntegrationDocumentObject` oder `TaxIntegrationLineObject` hinzu, abhängig von der Ebene des Feldes.</span><span class="sxs-lookup"><span data-stu-id="c5a44-161">Add the data field to either `TaxIntegrationDocumentObject` or `TaxIntegrationLineObject`, depending on the level of the field.</span></span> <span data-ttu-id="c5a44-162">Im folgenden Beispiel wird die Positionsebene verwendet, und der Dateiname lautet `TaxIntegrationLineObject_Extension.xpp`.</span><span class="sxs-lookup"><span data-stu-id="c5a44-162">The following example uses the line level, and the file name is `TaxIntegrationLineObject_Extension.xpp`.</span></span>

> [!NOTE]
> <span data-ttu-id="c5a44-163">Wenn sich das hinzugefügte Datenfeld auf Dokumentebene befindet, ändern Sie den Dateinamen in `TaxIntegrationDocumentObject_Extension.xpp`.</span><span class="sxs-lookup"><span data-stu-id="c5a44-163">If the data field that you're adding is at the document level, change the file name to `TaxIntegrationDocumentObject_Extension.xpp`.</span></span>

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

<span data-ttu-id="c5a44-164">**Kostenstelle** und **Projekt** werden als private Variablen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c5a44-164">**Cost center** and **Project** are added as private variables.</span></span> <span data-ttu-id="c5a44-165">Erstellen Sie Getter- und Setter-Methoden für diese Datenfelder, um die Daten zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="c5a44-165">Create getter and setter methods for these data fields to manipulate the data.</span></span>

### <a name="step-2-retrieve-data-from-the-database"></a><span data-ttu-id="c5a44-166">Schritt 2.</span><span class="sxs-lookup"><span data-stu-id="c5a44-166">Step 2.</span></span> <span data-ttu-id="c5a44-167">Daten aus der Datenbank abrufen</span><span class="sxs-lookup"><span data-stu-id="c5a44-167">Retrieve data from the database</span></span>

<span data-ttu-id="c5a44-168">Geben Sie die Transaktion an und erweitern Sie die entsprechenden Adapterklassen, um die Daten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c5a44-168">Specify the transaction, and extend the appropriate adapter classes to retrieve the data.</span></span> <span data-ttu-id="c5a44-169">Zum Beispiel, wenn Sie eine **Bestellung**-Transaktion verwenden, müssen Sie `TaxIntegrationPurchTableDataRetrieval` und `TaxIntegrationVendInvoiceInfoTableDataRetrieval` erweitern.</span><span class="sxs-lookup"><span data-stu-id="c5a44-169">For example, if you use a **Purchase order** transaction, you must extend `TaxIntegrationPurchTableDataRetrieval` and `TaxIntegrationVendInvoiceInfoTableDataRetrieval`.</span></span> 

> [!NOTE]
> <span data-ttu-id="c5a44-170">`TaxIntegrationPurchParmTableDataRetrieval` wird von `TaxIntegrationPurchTableDataRetrieval` geerbt.</span><span class="sxs-lookup"><span data-stu-id="c5a44-170">`TaxIntegrationPurchParmTableDataRetrieval` is inherited from `TaxIntegrationPurchTableDataRetrieval`.</span></span> <span data-ttu-id="c5a44-171">Es sollte nicht geändert werden, es sei denn, die Logik der Tabellen `purchTable` und `purchParmTable` unterscheidet sich.</span><span class="sxs-lookup"><span data-stu-id="c5a44-171">It should not be changed unless the logic of the `purchTable` and `purchParmTable` tables differs.</span></span>

<span data-ttu-id="c5a44-172">Wenn das Datenfeld für alle Transaktionen hinzugefügt werden soll, erweitern Sie alle `DataRetrieval`-Klassen.</span><span class="sxs-lookup"><span data-stu-id="c5a44-172">If the data field should be added for all transactions, extend all `DataRetrieval` classes.</span></span>

<span data-ttu-id="c5a44-173">Weil alle **Datenabruf**-Aktivitäten dieselbe Vorlagenklasse erweitern, sind die Klassenstrukturen, Variablen und Methoden ähnlich.</span><span class="sxs-lookup"><span data-stu-id="c5a44-173">Because all **Data Retrieval** activities extend the same template class, the class structures, variables, and methods are similar.</span></span>

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

<span data-ttu-id="c5a44-174">Das folgende Beispiel zeigt die Grundstruktur, wenn die `PurchTable`-Tabelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c5a44-174">The following example shows the basic structure when the `PurchTable` table is used.</span></span>

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

<span data-ttu-id="c5a44-175">Wenn die `CopyToDocument`-Methode aufgerufen wird, existiert der `this.purchTable`-Puffer bereits.</span><span class="sxs-lookup"><span data-stu-id="c5a44-175">When the `CopyToDocument` method is called, the `this.purchTable` buffer already exists.</span></span> <span data-ttu-id="c5a44-176">Der Zweck dieser Methode besteht darin, alle erforderlichen Daten von `this.purchTable` zum `document`-Objekt mit der Setter-Methode zu kopieren, die in der `DocumentObject`-Klasse erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="c5a44-176">The purpose of this method is to copy all the required data from `this.purchTable` to the `document` object by using the setter method that was created in the `DocumentObject` class.</span></span>

<span data-ttu-id="c5a44-177">Ebenso existiert bereits ein `this.purchLine`-Puffer in der `CopyToLine`-Methode.</span><span class="sxs-lookup"><span data-stu-id="c5a44-177">Likewise, a `this.purchLine` buffer already exists in the `CopyToLine` method.</span></span> <span data-ttu-id="c5a44-178">Der Zweck dieser Methode besteht darin, alle erforderlichen Daten von `this.purchLine` zum `_line`-Objekt mit der Setter-Methode zu kopieren, die in der `LineObject`-Klasse erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="c5a44-178">The purpose of this method is to copy all the required data from `this.purchLine` to the `_line` object by using the setter method that was created in the `LineObject` class.</span></span>

<span data-ttu-id="c5a44-179">Der einfachste Ansatz ist die Erweiterung der `CopyToDocument`- und `CopyToLine`-Methoden.</span><span class="sxs-lookup"><span data-stu-id="c5a44-179">The most straightforward approach is to extend the `CopyToDocument` and `CopyToLine` methods.</span></span> <span data-ttu-id="c5a44-180">Wir empfehlen jedoch, dass Sie die Methoden `copyToDocumentFromHeaderTable` und `copyToLineFromLineTable` zuerst versuchen.</span><span class="sxs-lookup"><span data-stu-id="c5a44-180">However, we recommend that you try the `copyToDocumentFromHeaderTable` and `copyToLineFromLineTable` methods first.</span></span> <span data-ttu-id="c5a44-181">Wenn sie nicht wie gewünscht funktionieren, implementieren Sie Ihre eigene Methode und rufen Sie sie in `CopyToDocument` und `CopyToLine` auf.</span><span class="sxs-lookup"><span data-stu-id="c5a44-181">If they don't work as you require, implement your own method, and call it in `CopyToDocument` and `CopyToLine`.</span></span> <span data-ttu-id="c5a44-182">Es gibt drei häufige Situationen, in denen Sie diesen Ansatz verwenden können:</span><span class="sxs-lookup"><span data-stu-id="c5a44-182">There are three common situations where you might use this approach:</span></span>

- <span data-ttu-id="c5a44-183">Das erforderliche Feld befindet sich in `PurchTable` oder `PurchLine`.</span><span class="sxs-lookup"><span data-stu-id="c5a44-183">The required field is in `PurchTable` or `PurchLine`.</span></span> <span data-ttu-id="c5a44-184">In dieser Situation können Sie `copyToDocumentFromHeaderTable` und `copyToLineFromLineTable` erweitern.</span><span class="sxs-lookup"><span data-stu-id="c5a44-184">In this situation, you can extend `copyToDocumentFromHeaderTable` and `copyToLineFromLineTable`.</span></span> <span data-ttu-id="c5a44-185">Hier ist der Beispielcode.</span><span class="sxs-lookup"><span data-stu-id="c5a44-185">Here is the sample code.</span></span>

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

- <span data-ttu-id="c5a44-186">Die erforderlichen Daten befinden sich nicht in der Standardtabelle der Transaktion.</span><span class="sxs-lookup"><span data-stu-id="c5a44-186">The required data isn't in the default table of the transaction.</span></span> <span data-ttu-id="c5a44-187">Es gibt jedoch einige Verknüpfungsbeziehungen mit der Standardtabelle, und das Feld ist in den meisten Zeilen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c5a44-187">However, there are some join relationships with the default table, and the field is required on most lines.</span></span> <span data-ttu-id="c5a44-188">In dieser Situation ersetzen Sie `getDocumentQueryObject` oder `getLineObject`, um die Tabelle nach Verknüpfungsbeziehung abzufragen.</span><span class="sxs-lookup"><span data-stu-id="c5a44-188">In this situation, replace `getDocumentQueryObject` or `getLineObject` to query the table by join relationship.</span></span> <span data-ttu-id="c5a44-189">Im folgenden Beispiel wird das Feld **Jetzt liefern** auf Positionsebene in den Auftrag integriert.</span><span class="sxs-lookup"><span data-stu-id="c5a44-189">In the following example, the **Deliver Now** field is integrated with the sales order at the line level.</span></span>

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

    <span data-ttu-id="c5a44-190">In diesem Beispiel wird ein `mcrSalesLineDropShipment`-Puffer deklariert und die Abfrage in `getLineQueryObject` definiert.</span><span class="sxs-lookup"><span data-stu-id="c5a44-190">In this example, a `mcrSalesLineDropShipment` buffer is declared, and the query is defined in `getLineQueryObject`.</span></span> <span data-ttu-id="c5a44-191">Die Abfrage verwendet die Beziehung `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`.</span><span class="sxs-lookup"><span data-stu-id="c5a44-191">The query uses the relationship `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`.</span></span> <span data-ttu-id="c5a44-192">Während Sie in dieser Situation erweitern, können Sie `getLineQueryObject` mit Ihrem eigenen konstruierten Abfrageobjekt ersetzen.</span><span class="sxs-lookup"><span data-stu-id="c5a44-192">While you're extending in this situation, you can replace `getLineQueryObject` with your own constructed query object.</span></span> <span data-ttu-id="c5a44-193">Beachten Sie jedoch die folgenden Punkte:</span><span class="sxs-lookup"><span data-stu-id="c5a44-193">However, note the following points:</span></span>

    * <span data-ttu-id="c5a44-194">Weil der Rückgabewert der `getLineQueryObject`-Methode `SysDaQueryObject` ist, müssen Sie dieses Objekt mithilfe des SysDa-Ansatzes erstellen.</span><span class="sxs-lookup"><span data-stu-id="c5a44-194">Because the return value of the `getLineQueryObject` method is `SysDaQueryObject`, you must construct this object by using the SysDa approach.</span></span>
    * <span data-ttu-id="c5a44-195">Vorhandene Tabelle kann nicht entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="c5a44-195">Can't remove existed table.</span></span>

- <span data-ttu-id="c5a44-196">Die erforderlichen Daten werden durch eine komplizierte Verknüpfungsbeziehung mit der Transaktionstabelle verknüpft, oder die Beziehung ist nicht eins zu eins (1:1), sondern eins zu viele (1:N).</span><span class="sxs-lookup"><span data-stu-id="c5a44-196">The required data is related to the transaction table by a complicated join relationship, or the relation isn't one to one (1:1) but one to many (1:N).</span></span> <span data-ttu-id="c5a44-197">In dieser Situation werden die Dinge etwas kompliziert.</span><span class="sxs-lookup"><span data-stu-id="c5a44-197">In this situation, things become a little complicated.</span></span> <span data-ttu-id="c5a44-198">Diese Situation gilt für das Beispiel der Finanzdimensionen.</span><span class="sxs-lookup"><span data-stu-id="c5a44-198">This situation applies to the example of financial dimensions.</span></span> 

    <span data-ttu-id="c5a44-199">In dieser Situation können Sie Ihre eigene Methode zum Abrufen der Daten implementieren.</span><span class="sxs-lookup"><span data-stu-id="c5a44-199">In this situation, you can implement your own method to retrieve the data.</span></span> <span data-ttu-id="c5a44-200">Hier ist der Beispielcode in der `TaxIntegrationPurchTableDataRetrieval_Extension.xpp`-Datei.</span><span class="sxs-lookup"><span data-stu-id="c5a44-200">Here is the sample code in the `TaxIntegrationPurchTableDataRetrieval_Extension.xpp` file.</span></span>

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

### <a name="step-3-add-data-to-the-request"></a><span data-ttu-id="c5a44-201">Schritt 3.</span><span class="sxs-lookup"><span data-stu-id="c5a44-201">Step 3.</span></span> <span data-ttu-id="c5a44-202">Daten zur Anforderung hinzufügen</span><span class="sxs-lookup"><span data-stu-id="c5a44-202">Add data to the request</span></span>

<span data-ttu-id="c5a44-203">Erweitern Sie die Methode `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` oder `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` zum Hinzufügen von Daten zur Anforderung.</span><span class="sxs-lookup"><span data-stu-id="c5a44-203">Extend the `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` or `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` method to add data to the request.</span></span> <span data-ttu-id="c5a44-204">Hier ist der Beispielcode in der `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp`-Datei.</span><span class="sxs-lookup"><span data-stu-id="c5a44-204">Here is the sample code in the `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp` file.</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define key for the form in post request
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

<span data-ttu-id="c5a44-205">In diesem Code ist `_destination` das Wrapper-Objekt, mit dem die Post-Anforderung generiert wird, und `_source` ist das `TaxIntegrationLineObject`-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c5a44-205">In this code, `_destination` is the wrapper object that is used to generate the post request, and `_source` is the `TaxIntegrationLineObject` object.</span></span> 

> [!NOTE]
> * <span data-ttu-id="c5a44-206">Definieren Sie den im Anforderungsformular verwendeten Schlüssel als `private const str`.</span><span class="sxs-lookup"><span data-stu-id="c5a44-206">Define the key that is used in the request form as `private const str`.</span></span>
> * <span data-ttu-id="c5a44-207">Stellen Sie das Feld in der `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine`-Methode unter Verwendung der `SetField`-Methode ein.</span><span class="sxs-lookup"><span data-stu-id="c5a44-207">Set the field in the `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` method by using the `SetField` method.</span></span> <span data-ttu-id="c5a44-208">Der Datentyp des zweiten Parameters sollte `string` sein.</span><span class="sxs-lookup"><span data-stu-id="c5a44-208">The data type of the second parameter should be `string`.</span></span> <span data-ttu-id="c5a44-209">Wenn der Datentyp nicht `string` ist, konvertieren Sie ihn in `string`.</span><span class="sxs-lookup"><span data-stu-id="c5a44-209">If the data type isn't `string`, convert it to `string`.</span></span>

## <a name="appendix"></a><span data-ttu-id="c5a44-210">Anhang</span><span class="sxs-lookup"><span data-stu-id="c5a44-210">Appendix</span></span>

<span data-ttu-id="c5a44-211">Dieser Anhang zeigt den vollständigen Beispielcode für die Integration der Finanzdimensionen (**Kostenstelle** und **Projekt**) auf Positionsebene.</span><span class="sxs-lookup"><span data-stu-id="c5a44-211">This appendix shows the complete sample code for the integration of financial dimensions (**Cost center** and **Project**) at the line level.</span></span>

### <a name="taxintegrationlineobject_extensionxpp"></a><span data-ttu-id="c5a44-212">TaxIntegrationLineObject_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="c5a44-212">TaxIntegrationLineObject_Extension.xpp</span></span>

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

### <a name="taxintegrationpurchtabledataretrieval_extensionxpp"></a><span data-ttu-id="c5a44-213">TaxIntegrationPurchTableDataRetrieval_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="c5a44-213">TaxIntegrationPurchTableDataRetrieval_Extension.xpp</span></span>

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

### <a name="taxintegrationcalculationactivityondocument_calculationservice_extensionxpp"></a><span data-ttu-id="c5a44-214">TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="c5a44-214">TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define key for the form in post request
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
