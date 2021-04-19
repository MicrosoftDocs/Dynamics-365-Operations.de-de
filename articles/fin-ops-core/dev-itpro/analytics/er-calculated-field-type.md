---
title: Unterstützen parametrisierter Aufrufe von ER-Datenquellen des Typs „Berechnetes Feld“
description: Dieses Thema enthält Informationen zum Verwenden des Typs „Berechnetes Feld“ für ER-Datenquellen.
author: NickSelin
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 897133a27f9d3da2f576ce675c0949f824cde881
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749488"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a><span data-ttu-id="175fe-103">Unterstützen parametrisierter Aufrufe von ER-Datenquellen des Typs „Berechnetes Feld“</span><span class="sxs-lookup"><span data-stu-id="175fe-103">Support parameterized calls of ER data sources of the Calculated field type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="175fe-104">In diesem Thema wird erläutert, wie Sie eine Datenquelle für die elektronische Berichterstellung (Electronic Reporting, ER) mithilfe des Typs **Berechnetes Feld** entwerfen können.</span><span class="sxs-lookup"><span data-stu-id="175fe-104">This topic explains how you can design an Electronic reporting (ER) data source by using the **Calculated field** type.</span></span> <span data-ttu-id="175fe-105">Diese Datenquelle enthält ggf. einen ER-Ausdruck, der bei Ausführung durch die Werte der Parameterargumente gesteuert werden kann, die in einer Bindung konfiguriert sind, die diese Datenquelle aufruft.</span><span class="sxs-lookup"><span data-stu-id="175fe-105">This data source may contain an ER expression that, when executed, can be controlled by the values of the parameter arguments that are configured in a binding that calls this data source.</span></span> <span data-ttu-id="175fe-106">Wenn Sie parametrisierte Aufrufe einer solchen Datenquelle konfigurieren, können Sie eine einzelne Datenquelle in vielen Bindungen wiederverwenden, wodurch die Gesamtanzahl der Datenquellen verringert wird, die in ER-Modellzuordnungen oder in ER-Formaten konfiguriert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="175fe-106">By configuring parameterized calls of such a data source, you can reuse a single data source in many bindings, which reduces the total number of data sources that must be configured in ER model mappings or ER formats.</span></span> <span data-ttu-id="175fe-107">Außerdem wird die konfigurierte ER-Komponente vereinfacht, wodurch sich die Instandhaltungskosten sowie die Kosten für die Verwendung durch andere Verbraucher verringern.</span><span class="sxs-lookup"><span data-stu-id="175fe-107">It also simplifies the configured ER component, which reduces the maintenance costs and the cost of use by other consumers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="175fe-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="175fe-108">Prerequisites</span></span>
<span data-ttu-id="175fe-109">Um die Beispiele in diesem Thema abzuschließen, müssen Sie den folgenden Zugriff haben:</span><span class="sxs-lookup"><span data-stu-id="175fe-109">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="175fe-110">Zugreifen auf eine dieser Rollen:</span><span class="sxs-lookup"><span data-stu-id="175fe-110">Access to one of these roles:</span></span>

    - <span data-ttu-id="175fe-111">Entwickler für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="175fe-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="175fe-112">Funktionaler Berater für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="175fe-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="175fe-113">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="175fe-113">System administrator</span></span>

- <span data-ttu-id="175fe-114">Zugriff auf die Regulatory Configuration Services (RCS), die für denselben Mandanten wie Finance and Operations bereitgestellt wurden, für eine der folgenden Rollen:</span><span class="sxs-lookup"><span data-stu-id="175fe-114">Access to Regulatory Configuration Services (RCS) that have been provisioned for the same tenant as Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="175fe-115">Entwickler für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="175fe-115">Electronic reporting developer</span></span>
    - <span data-ttu-id="175fe-116">Funktionaler Berater für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="175fe-116">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="175fe-117">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="175fe-117">System administrator</span></span>

<span data-ttu-id="175fe-118">Sie müssen auch die folgenden Dateien herunterladen und lokal speichern.</span><span class="sxs-lookup"><span data-stu-id="175fe-118">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="175fe-119">**Inhalt**</span><span class="sxs-lookup"><span data-stu-id="175fe-119">**Content**</span></span>                           | <span data-ttu-id="175fe-120">**Dateiname**</span><span class="sxs-lookup"><span data-stu-id="175fe-120">**File name**</span></span>                                        |
|---------------------------------------|------------------------------------------------------|
| <span data-ttu-id="175fe-121">Beispiel-EB-Datenmodell-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="175fe-121">Sample ER data model configuration</span></span>    | [<span data-ttu-id="175fe-122">Model to learn parameterized calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="175fe-122">Model to learn parameterized calls.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)     |
| <span data-ttu-id="175fe-123">Beispiel-EB-Metadatenkonfiguration</span><span class="sxs-lookup"><span data-stu-id="175fe-123">Sample ER metadata configuration</span></span>      | [<span data-ttu-id="175fe-124">Metadata to learn parameterized calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="175fe-124">Metadata to learn parameterized calls.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |
| <span data-ttu-id="175fe-125">Beispiel-EB-Modellzuordnungskonfiguration</span><span class="sxs-lookup"><span data-stu-id="175fe-125">Sample ER model mapping configuration</span></span> | [<span data-ttu-id="175fe-126">Mapping to learn parameterized calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="175fe-126">Mapping to learn parameterized calls.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="175fe-127">Beispiel-EB-Formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="175fe-127">Sample ER format configuration</span></span>        | [<span data-ttu-id="175fe-128">Format to learn parameterized calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="175fe-128">Format to learn parameterized calls.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |

## <a name="sign-in-to-your-rcs-instance"></a><span data-ttu-id="175fe-129">Anmelden bei Ihrer RCS-Instanz</span><span class="sxs-lookup"><span data-stu-id="175fe-129">Sign in to your RCS instance</span></span>
<span data-ttu-id="175fe-130">In diesem Beispiel erstellen Sie eine Konfiguration für die Musterfirma Litware, Inc. Zunächst müssen Sie im RCS die Schritte in der Prozedur [Konfigurationsanbieter anlegen durchführen und als aktiv markieren](tasks/er-configuration-provider-mark-it-active-2016-11.md):</span><span class="sxs-lookup"><span data-stu-id="175fe-130">In this example, you will create a configuration for the sample company, Litware, Inc. First, in RCS, you must complete the steps in the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure:</span></span>

1. <span data-ttu-id="175fe-131">Wählen Sie im Standard-Dashboard **Elektronische Berichterstellung** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-131">On the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="175fe-132">Wählen Sie **Berichterstellungskonfigurationen** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-132">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="175fe-133">Importieren Sie die heruntergeladenen Konfigurationen in der folgenden Reihenfolge in RCS: Datenmodell, Metadaten, Modellzuordnung, Format.</span><span class="sxs-lookup"><span data-stu-id="175fe-133">Import the downloaded configurations to RCS in the following sequence: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="175fe-134">Führen Sie die folgenden Schritte für jede ER-Konfiguration aus:</span><span class="sxs-lookup"><span data-stu-id="175fe-134">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="175fe-135">Wählen Sie **Wechselkurs** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-135">Select **Exchange.**</span></span>
    2. <span data-ttu-id="175fe-136">Wählen Sie **Aus XML-Datei laden** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-136">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="175fe-137">Wählen Sie **Durchsuchen** und dann die erforderliche EB-Konfiguration im XML-Format aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-137">Select **Browse**, and then select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="175fe-138">Wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-138">Select **OK.**</span></span>

## <a name="review-the-provided-er-solution"></a><span data-ttu-id="175fe-139">Überprüfen der bereitgestellten ER-Lösung</span><span class="sxs-lookup"><span data-stu-id="175fe-139">Review the provided ER solution</span></span>

### <a name="review-model-mapping"></a><span data-ttu-id="175fe-140">Überprüfen der Modellzuordnung</span><span class="sxs-lookup"><span data-stu-id="175fe-140">Review model mapping</span></span>

1. <span data-ttu-id="175fe-141">Erweitern Sie in der Konfigurationsstruktur den Inhalt des Elements **Modell zum Ermitteln parametrisierter Aufrufe**.</span><span class="sxs-lookup"><span data-stu-id="175fe-141">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="175fe-142">Wählen Sie **Zuordnung zum Ermitteln parametrisierter Aufrufe** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-142">Select **Mapping to learn parameterized calls**.</span></span>
3. <span data-ttu-id="175fe-143">Wählen Sie **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-143">Select **Designer**.</span></span>
4. <span data-ttu-id="175fe-144">Wählen Sie **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-144">Select **Designer**.</span></span>  
   
    <span data-ttu-id="175fe-145">Diese ER-Modellzuordnung ist für die folgenden Aktionen vorgesehen:</span><span class="sxs-lookup"><span data-stu-id="175fe-145">This ER model mapping is designed to do the following:</span></span>

    - <span data-ttu-id="175fe-146">Holen Sie sich die Liste der Steuercodes (**Steuern** Datenquelle), die sich in der Tabelle **Steuertabelle** befinden.</span><span class="sxs-lookup"><span data-stu-id="175fe-146">Fetch the list of tax codes (**Tax** data source) residing in the **TaxTable** table.</span></span>
    - <span data-ttu-id="175fe-147">Holen Sie sich die Liste der Steuertransaktionen (**Trans** Datenquelle), die sich in der Tabelle **TaxTrans** befinden:</span><span class="sxs-lookup"><span data-stu-id="175fe-147">Fetch the list of tax transactions (**Trans** data source) residing in the **TaxTrans** table:</span></span>
    
        - <span data-ttu-id="175fe-148">Gruppieren Sie die Liste der abgerufenen Transaktionen (**GR**-Datenquelle) nach Steuercode.</span><span class="sxs-lookup"><span data-stu-id="175fe-148">Group the list of fetched transactions (**Gr** data source) by tax code.</span></span>
        - <span data-ttu-id="175fe-149">Berechnen Sie für gruppierte Transaktionen nach aggregierten Werten pro Steuercode:</span><span class="sxs-lookup"><span data-stu-id="175fe-149">Calculate for grouped transactions following aggregated values per tax code:</span></span>

            - <span data-ttu-id="175fe-150">Summe der Steuerbasiswerte</span><span class="sxs-lookup"><span data-stu-id="175fe-150">Sum of tax base values.</span></span>
            - <span data-ttu-id="175fe-151">Summe der Steuerwerte</span><span class="sxs-lookup"><span data-stu-id="175fe-151">Sum of tax values.</span></span>
            - <span data-ttu-id="175fe-152">Mindestwert des angewendeten Steuersatzes</span><span class="sxs-lookup"><span data-stu-id="175fe-152">Minimum value of applied tax rate.</span></span>

    <span data-ttu-id="175fe-153">Die Modellzuordnung in dieser Konfiguration implementiert das Basisdatenmodell für alle EB-Formate, für die dieses Modell erstellt und in Finance and Operations ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="175fe-153">The model mapping in this configuration implements the base data model for any of the ER formats created for this model and executed in Finance and Operations.</span></span> <span data-ttu-id="175fe-154">Demzufolge wird der Inhalt der **Steuer**- und **GR**-Datenquellen für ER-Formate wie abstrakte Datenquellen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="175fe-154">As a result, the content of the **Tax** and **Gr** data sources is exposed for ER formats such as abstract data sources.</span></span>

    ![Seite „Modellzuordnungsdesigner“ mit Steuer- und GR-Datenquellen](media/er-calculated-field-type-01.png)

5.  <span data-ttu-id="175fe-156">Schließen Sie die Seite **Modellzuordnungsdesigner**.</span><span class="sxs-lookup"><span data-stu-id="175fe-156">Close the **Model mapping designer** page.</span></span>
6.  <span data-ttu-id="175fe-157">Schließen Sie die Seite **Modellzuordnung**.</span><span class="sxs-lookup"><span data-stu-id="175fe-157">Close the **Model mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="175fe-158">Überprüfen des Formats</span><span class="sxs-lookup"><span data-stu-id="175fe-158">Review format</span></span>

1. <span data-ttu-id="175fe-159">Erweitern Sie in der Konfigurationsstruktur den Inhalt des Elements **Modell zum Ermitteln parametrisierter Aufrufe**.</span><span class="sxs-lookup"><span data-stu-id="175fe-159">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="175fe-160">Wählen Sie **Format zum Ermitteln parametrisierter Anrufe** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-160">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="175fe-161">Wählen Sie **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-161">Select **Designer**.</span></span> <span data-ttu-id="175fe-162">Dieses ER-Format ist für die folgenden Aktionen vorgesehen:</span><span class="sxs-lookup"><span data-stu-id="175fe-162">This ER format is designed to do the following:</span></span>

    - <span data-ttu-id="175fe-163">Generieren Sie einen Steuerauszug im XML-Format.</span><span class="sxs-lookup"><span data-stu-id="175fe-163">Generate a tax statement in XML format.</span></span>
    - <span data-ttu-id="175fe-164">Stellen Sie die folgenden Besteuerungsstufen im Steuerauszug dar: „Regulär“, „Reduziert“ und „Keine“.</span><span class="sxs-lookup"><span data-stu-id="175fe-164">Present the following levels of taxation in the tax statement: regular, reduced, and none.</span></span>
    - <span data-ttu-id="175fe-165">Stellen Sie mehrere Details für jedes Besteuerungsniveau dar, die jeweils eine andere Anzahl von Details auf jeder Stufe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="175fe-165">Present multiple details at each taxation level, having a different number of details in each level.</span></span>

    ![Formatdesignerseite](media/er-calculated-field-type-02.png)

4. <span data-ttu-id="175fe-167">Wählen Sie **Zuordnung** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-167">Select **Mapping**.</span></span>
5. <span data-ttu-id="175fe-168">Erweitern Sie die Elemente **Modell**, **Daten,** und **Zusammenfassung**.</span><span class="sxs-lookup"><span data-stu-id="175fe-168">Expand the **Model**, **Data,** and **Summary** items.</span></span> 

    <span data-ttu-id="175fe-169">Das berechnete Feld **Model.Data.Summary.Level** enthält den Ausdruck, der den Code des Besteuerungsniveaus (**Regulär**, **Reduziert**, **Kein,** oder **Sonstige**) als Textwert für jeden Steuercode zurückgibt, der zur Laufzeit aus der Datenquelle **Model.Data.Summary** abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="175fe-169">The calculated field **Model.Data.Summary.Level** contains the expression that returns the code of the taxation level (**Regular**, **Reduced**, **None,** or **Other**) as a text value for any tax code that can be retrieved from the **Model.Data.Summary** data source at run time.</span></span>

    ![Seite „Formatdesigner“ mit Details des Datenmodells „Modell zum Lernern parametrisierter Aufrufe“](media/er-calculated-field-type-03.png)

6. <span data-ttu-id="175fe-171">Erweitern Sie das Element **Modell**.**Data2**.</span><span class="sxs-lookup"><span data-stu-id="175fe-171">Expand the **Model**.**Data2** item.</span></span>
7. <span data-ttu-id="175fe-172">Erweitern Sie das Element **Modell**.**Data2.Summary2**.</span><span class="sxs-lookup"><span data-stu-id="175fe-172">Expand the **Model**.**Data2.Summary2** item.</span></span>
   
    <span data-ttu-id="175fe-173">Die Datenquelle **Modell**.**Data2.Summary2** ist zum Gruppieren der Transaktionsdetails der Datenquelle **Model.Data.Summary** nach Besteuerungsniveau (die vom berechneten Feld **Model.Data.Summary.Level** zurückgegeben werden) und zum Berechnen der Aggregationen konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="175fe-173">The **Model**.**Data2.Summary2** data source is configured to group the **Model.Data.Summary** data source transaction details by taxation level (returned by the **Model.Data.Summary.Level** calculated field) and compute the aggregations.</span></span>

    ![Die Seite „Formatdesigner“ mit Details der Datenquelle „Model.Data2.Summary2“](media/er-calculated-field-type-04.png)

8. <span data-ttu-id="175fe-175">Überprüfen Sie die berechneten Felder **Model**.**Data2.Level1**, **Model**.**Data2.Level2** und **Model**.**Data2.Level3.**</span><span class="sxs-lookup"><span data-stu-id="175fe-175">Review the calculated fields **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, and **Model**.**Data2.Level3.**</span></span> <span data-ttu-id="175fe-176">Diese berechneten Felder werden verwendet, um die Datensatzliste **Model**.**Data2.Summary2** zu filtern und nur Datensätze zurückzugeben, die ein bestimmtes Besteuerungsniveau darstellen.</span><span class="sxs-lookup"><span data-stu-id="175fe-176">These calculated fields are used to filter the **Model**.**Data2.Summary2** records list and return only records that represent a particular taxation level.</span></span>
9. <span data-ttu-id="175fe-177">Seite **Format-Designer** schließen.</span><span class="sxs-lookup"><span data-stu-id="175fe-177">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="175fe-178">Erstellen eines abgeleiteten Formats</span><span class="sxs-lookup"><span data-stu-id="175fe-178">Create a derived format</span></span>
<span data-ttu-id="175fe-179">Sie können das bereitgestellte Format verbessern, indem Sie ein berechnetes Feld hinzufügen, um das erforderliche Besteuerungsniveau zu filtern, anstatt die vorhandenen drei Felder zu verwenden: **Modell**.**Data2.Level1**, **Modell**.**Data2.Level2** und **Modell**.**Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="175fe-179">You can improve the provided format by adding one calculated field to filter the required taxation level instead of using the existing three fields: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** and **Model**.**Data2.Level3**.</span></span> <span data-ttu-id="175fe-180">Das erforderliche Besteuerungsniveau kann an dem Ort festgelegt werden, an dieses neue berechnete Feld aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="175fe-180">The required taxation level can be specified in the location where this new calculated field will be called.</span></span>

1. <span data-ttu-id="175fe-181">Erweitern Sie in der Konfigurationsstruktur den Inhalt des Elements **Modell zum Ermitteln parametrisierter Aufrufe**.</span><span class="sxs-lookup"><span data-stu-id="175fe-181">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="175fe-182">Wählen Sie **Format zum Ermitteln parametrisierter Anrufe** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-182">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="175fe-183">Wählen Sie **Konfiguration erstellen**.</span><span class="sxs-lookup"><span data-stu-id="175fe-183">Select **Create configuration**.</span></span>
4. <span data-ttu-id="175fe-184">Wählen Sie **Von Name ableiten: Formatieren zum Ermitteln parametrisierter Aufrufe, Microsoft** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-184">Select **Derive from Name: Format to learn parameterized calls, Microsoft**.</span></span>
5. <span data-ttu-id="175fe-185">Geben Sie im Feld **Name** den Text **Format zum Ermitteln parametrisierter Aufrufe (benutzerdefiniert)** ein.</span><span class="sxs-lookup"><span data-stu-id="175fe-185">In the **Name** field, enter **Format to learn parameterized calls (custom)**.</span></span>
6. <span data-ttu-id="175fe-186">Wählen Sie **Konfiguration erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-186">Select **Create configuration.**</span></span>

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a><span data-ttu-id="175fe-187">Konfigurieren eines parametrisierten berechneten Felds, das eine Liste der Datensätze zurückgibt</span><span class="sxs-lookup"><span data-stu-id="175fe-187">Configure a parameterized calculated field that returns a list of records</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="175fe-188">Hinzufügen eines neuen berechneten Felds</span><span class="sxs-lookup"><span data-stu-id="175fe-188">Start adding a new calculated field</span></span>

1. <span data-ttu-id="175fe-189">Wählen Sie **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-189">Select **Designer**.</span></span>
2. <span data-ttu-id="175fe-190">Wählen Sie **Erweitern/Reduzieren** aus, um alle Formatelemente zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="175fe-190">Select **Expand/collapse** to expand all format items.</span></span>
3. <span data-ttu-id="175fe-191">Wählen Sie **Zuordnung** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-191">Select **Mapping**.</span></span>
4. <span data-ttu-id="175fe-192">Erweitern Sie das Element **Model**.</span><span class="sxs-lookup"><span data-stu-id="175fe-192">Expand the **Model** item.</span></span>
5. <span data-ttu-id="175fe-193">Wählen Sie das Element **Modell.Data2** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-193">Select the **Model.Data2** item.</span></span>
6. <span data-ttu-id="175fe-194">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-194">Select **Add**.</span></span>
7. <span data-ttu-id="175fe-195">Wählen Sie das Feld **Funktionen\\Berechnet** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-195">Select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="175fe-196">Geben Sie im Feld **Name** **Ebenen** ein.</span><span class="sxs-lookup"><span data-stu-id="175fe-196">In the **Name** field, enter **Levels**.</span></span>
9. <span data-ttu-id="175fe-197">Wählen Sie **Formel bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-197">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="175fe-198">Definieren eines Parameters für das Hinzufügen eines berechneten Felds</span><span class="sxs-lookup"><span data-stu-id="175fe-198">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="175fe-199">Wählen Sie **Parameter** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-199">Select **Parameters**.</span></span>
2. <span data-ttu-id="175fe-200">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-200">Select **New**.</span></span>
3. <span data-ttu-id="175fe-201">Geben Sie im Feld **Name** **Besteuerungsniveau** ein.</span><span class="sxs-lookup"><span data-stu-id="175fe-201">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="175fe-202">Wählen Sie im Feld **Typ** **Zeichenfolge** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-202">In the **Type** field, select **String**.</span></span>

    <span data-ttu-id="175fe-203">Es können nur primitive Datentypen verwendet werden, um das Argument des Parametertyps anzugeben.</span><span class="sxs-lookup"><span data-stu-id="175fe-203">Only primitive data types can be used to specify the type of the parameter’s argument.</span></span> <span data-ttu-id="175fe-204">Daher können die Typen **Datensatzliste**, **Datensatz** und **Enumeration** nicht für diesen Zweck verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="175fe-204">Therefore, **Record list**, **Record**, and **Enum** types cannot be used for this purpose.</span></span>

    <span data-ttu-id="175fe-205">Für ein einzelnes berechnetes Feld können maximal 8 Parameter angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="175fe-205">The maximum number of parameters that can be specified for a single calculated field is 8.</span></span>

    ![Liste der Parameterdatenquellen](media/er-calculated-field-type-05.png)

5. <span data-ttu-id="175fe-207">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="175fe-207">Select **OK**.</span></span>

<span data-ttu-id="175fe-208">Durch das Hinzufügen dieses Parameters legen Sie die Bedingung fest, die vorliegen muss, um dieses berechnete Feld aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="175fe-208">By adding this parameter, you specify the condition that must be in place to call this calculated field.</span></span> <span data-ttu-id="175fe-209">Wenn Sie dieses berechnete Feld aufrufen, müssen Sie das Argument des Paramaters **Besteuerungsniveau** als Wert mit dem Format **Zeichenfolge** angeben.</span><span class="sxs-lookup"><span data-stu-id="175fe-209">When you call this calculated field, you need to specify the argument of the **Taxation Level** parameter as a value with **String** format.</span></span>

   <span data-ttu-id="175fe-210">Stellen Sie sicher, dass Sie Parameter nur für die berechneten Felder definieren, die sich in einem Container (**Datensatzliste**, **Datensatz** oder **Container**) befinden.</span><span class="sxs-lookup"><span data-stu-id="175fe-210">Make sure that you define parameters only for those calculated fields that reside in a container (either **Record list**, **Record**, or **Container**).</span></span>

   <span data-ttu-id="175fe-211">Der konfigurierte Parameter ist in der Liste der Datenquellen für dieses berechnete Feld verfügbar.</span><span class="sxs-lookup"><span data-stu-id="175fe-211">The configured parameter is available in the list of data sources for this calculated field.</span></span> <span data-ttu-id="175fe-212">Sie können dem konfigurierten Ausdruck den Parameter hinzuzufügen, indem Sie **Datenquelle hinzufügen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="175fe-212">You can add the parameter to the configured expression by selecting **Add data source**.</span></span>

   ![Datenquellenfelder](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="175fe-214">Definieren eines Ausdrucks für das Hinzufügen eines berechneten Felds</span><span class="sxs-lookup"><span data-stu-id="175fe-214">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="175fe-215">Geben Sie im Feld **Formel** Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="175fe-215">In the **Formula** field, enter:</span></span> 

    <span data-ttu-id="175fe-216">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span><span class="sxs-lookup"><span data-stu-id="175fe-216">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span></span>
    
2. <span data-ttu-id="175fe-217">Wählen Sie den Parameter **Besteuerungsniveau** in der Liste der Datenquellen aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-217">Select the **Taxation Level** parameter in the list of data sources.</span></span>
3. <span data-ttu-id="175fe-218">Wählen Sie **Datenquelle hinzufügen** aus:</span><span class="sxs-lookup"><span data-stu-id="175fe-218">Select **Add data source**.</span></span>
4. <span data-ttu-id="175fe-219">Stellen Sie den Ausdruck im Feld **Formel** folgendermaßen fertig:</span><span class="sxs-lookup"><span data-stu-id="175fe-219">In the **Formula** field, finalize the expression as:</span></span>  

    <span data-ttu-id="175fe-220">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span><span class="sxs-lookup"><span data-stu-id="175fe-220">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span></span>

5. <span data-ttu-id="175fe-221">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="175fe-221">Select **Save**.</span></span>

    ![Informationen zu Datenquellenfeldern](media/er-calculated-field-type-07.png)

6. <span data-ttu-id="175fe-223">Schließen Sie die Seite **Formeldesigner**.</span><span class="sxs-lookup"><span data-stu-id="175fe-223">Close the **Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="175fe-224">Abschließen des Hinzufügens eines neuen berechneten Felds</span><span class="sxs-lookup"><span data-stu-id="175fe-224">Finish adding a new calculated field</span></span>

- <span data-ttu-id="175fe-225">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="175fe-225">Select **OK**.</span></span>

<span data-ttu-id="175fe-226">Für das konfigurierte, parametrisierte berechnete Feld **Ebenen** auf der Seite **Formatdesigner** ist ein Argument vom Typ **Zeichenfolge** erforderlich.</span><span class="sxs-lookup"><span data-stu-id="175fe-226">On the **Format designer** page, the configured parameterized calculated field **Levels** requires a **String** argument.</span></span>

![Erweiterte Liste der Ebenen des berechneten Felds](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements&quot;></a><span data-ttu-id=&quot;175fe-228&quot;>Verwenden Sie das berechnete Feld für konfigurierte verbindliche Formatelemente</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;175fe-228&quot;>Use the configured calculated field for binding format elements</span></span>

1. <span data-ttu-id=&quot;175fe-229&quot;>Wählen Sie **Model.Data2.Levels** aus, um das konfigurierte berechnete Feld auszuwählen.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;175fe-229&quot;>Select **Model.Data2.Levels** to select the configured calculated field.</span></span>
2. <span data-ttu-id=&quot;175fe-230&quot;>Wählen Sie das Formatelement **Statement.Taxation.Regular** aus.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;175fe-230&quot;>Select the **Statement.Taxation.Regular** format element.</span></span>
3. <span data-ttu-id=&quot;175fe-231&quot;>Wählen Sie **Bindung** aus.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;175fe-231&quot;>Select **Bind**.</span></span>
4. <span data-ttu-id=&quot;175fe-232&quot;>Wählen Sie **Ja** aus, um die Ersetzung der derzeit verwendeten Datenquelle **Level1** durch die neue Datenquelle **Ebenen** in allen geschachtelten Formatelementen des ausgewählten Formatelements zu bestätigen.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;175fe-232&quot;>Select **Yes** to confirm the replacement of the currently used data source, **Level1**, by the new data source, **Levels**, in all nested format elements of the selected format element.</span></span>

    <span data-ttu-id=&quot;175fe-233&quot;>Die angewendete Bindung wurde als Aufruf des parametrisierten berechneten Felds erstellt.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;175fe-233&quot;>Applied binding has been built as a call of the parameterized calculated field.</span></span> <span data-ttu-id=&quot;175fe-234&quot;>Standardmäßig wird der Name des gebundenen Formatelements als Argument für das parametrisierte berechnete Feld unter den folgenden Bedingungen erstellt:</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;175fe-234&quot;>By default, the name of the bound format element is used as an argument for parameterized calculated field under the following conditions:</span></span>

      - <span data-ttu-id=&quot;175fe-235&quot;>Das berechnete Feld ist für die Verwendung eines einzelnen Parameters konfiguriert.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;175fe-235&quot;>The calculated field is configured to use a single parameter.</span></span>
      - <span data-ttu-id=&quot;175fe-236&quot;>Der Datentyp dieses Parameters ist als **Zeichenfolge** definiert.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;175fe-236&quot;>The data type of this parameter is defined as **String**.</span></span>

    <span data-ttu-id=&quot;175fe-237&quot;>Wenn der Name des gebundenen Formatelements leer ist, wird der Datenquellenname dieses Elements in der angewendeten Bindung verwendet.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;175fe-237&quot;>When the name of the bound format element is blank, the data source name of this element is used in applied binding.</span></span>

5. <span data-ttu-id=&quot;175fe-238&quot;>Wählen Sie das Formatelement **Statement.Taxation.Reduced** aus.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;175fe-238&quot;>Select the **Statement.Taxation.Reduced** format element.</span></span>
6. <span data-ttu-id=&quot;175fe-239&quot;>Wählen Sie **Bindung** aus.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;175fe-239&quot;>Select **Bind**.</span></span>
7. <span data-ttu-id=&quot;175fe-240&quot;>Wählen Sie **Ja** aus, um die Ersetzung der derzeit verwendeten Datenquelle **Level2** durch die neue Datenquelle **Ebenen** in allen geschachtelten Formatelementen unter dem ausgewählten Formatelement zu bestätigen.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;175fe-240&quot;>Select **Yes** to confirm the replacement of the currently used data source, **Level2**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>
8. <span data-ttu-id=&quot;175fe-241&quot;>Wählen Sie das Formatelement **Statement.Taxation.None** aus.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;175fe-241&quot;>Select the **Statement.Taxation.None** format element.</span></span>
9. <span data-ttu-id=&quot;175fe-242&quot;>Wählen Sie **Bindung** aus.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;175fe-242&quot;>Select **Bind**.</span></span>
10. <span data-ttu-id=&quot;175fe-243&quot;>Wählen Sie **Ja** aus, um die Ersetzung der derzeit verwendeten Datenquelle **Level3** durch die neue Datenquelle **Ebenen** in allen geschachtelten Formatelementen unter dem ausgewählten Formatelement zu bestätigen.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;175fe-243&quot;>Select **Yes** to confirm the replacement of the currently used data source, **Level3**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>

   <span data-ttu-id=&quot;175fe-244&quot;>Wenn Sie das Argument des parametrisierten berechneten Felds für das XML-Element angeben, das das Besteuerungsniveau darstellt (z. B. **Model.Data2.Levels(&quot;Reduced")** als Textwert), müssen Sie diesen Schritt nicht für die geschachtelten XML-Attribute ausführen. Deren Bindungen übernehmen den Wert des auf der übergeordneten Ebene zugeordneten Arguments (**Model.Data2.Levels.aggregated.Base**, nicht **Model.Data2.Levels("Reduced").aggregated.Base**).</span><span class="sxs-lookup"><span data-stu-id="175fe-244">When you specify the argument of the parameterized calculated field for the XML element representing taxation level (for example, **Model.Data2.Levels("Reduced")** as a text value), you don’t need to do the same for nested XML attributes—their bindings will automatically inherit the value of the argument defined on the parent level (**Model.Data2.Levels.aggregated.Base**, not **Model.Data2.Levels("Reduced").aggregated.Base**).</span></span>

<span data-ttu-id="175fe-245">Wiederkehrende Aufrufe von parametrisierten berechneten Feldern werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="175fe-245">Recurrent calls of any parameterized calculated field are not supported.</span></span>

<span data-ttu-id="175fe-246">Sie können **Formel bearbeiten** auswählen und das standardmäßig übernommene Argument des parametrisierten berechneten Felds in der ausgewählten Bindung ändern.</span><span class="sxs-lookup"><span data-stu-id="175fe-246">You can select **Edit formula**, and change the applied-by-default argument of the parameterized calculated field in the selected binding.</span></span> <span data-ttu-id="175fe-247">Wenn dieses Argument nicht vorhanden ist, kann dies zu Fehlern während der Laufzeit kommen. Benutzer werden über solch eine Situation informiert, wenn das aktuelle Format überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="175fe-247">If this argument is missing, it can cause errors at run time — users are informed about such a situation when the current format is validated.</span></span>

![Benachrichtigung zu Überprüfungswarnungen](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a><span data-ttu-id="175fe-249">Konfigurieren eines parametrisierten berechneten Felds für die Rückgabe eines Datensatzes</span><span class="sxs-lookup"><span data-stu-id="175fe-249">Configure a parameterized calculated field to return a record</span></span>
<span data-ttu-id="175fe-250">Wenn ein parametrisiertes berechnetes Feld einen Datensatz zurückgibt, müssen Sie die Bindung einzelner Felder dieses Datensatzes zu Formatelementen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="175fe-250">When a parameterized calculated field returns a record, you need to support binding of individual fields of this record to format elements.</span></span> <span data-ttu-id="175fe-251">In solchen Fällen ist keine übergeordnete Bindung vorhanden, die den Wert eines Arguments zum Aufrufen eines parametrisierten berechneten Felds enthält. Dieser Wert muss in der Bindung des Felds einen einzelnen Datensatz definiert werden.</span><span class="sxs-lookup"><span data-stu-id="175fe-251">In such cases there will be no parent binding that contains the value of an argument to call a parameterized calculated field — this value must be defined in the binding of a single record’s field.</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="175fe-252">Hinzufügen eines neuen berechneten Felds</span><span class="sxs-lookup"><span data-stu-id="175fe-252">Start adding a new calculated field</span></span>

1. <span data-ttu-id="175fe-253">Wählen Sie das Element **Modell.Data2** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-253">Select the **Model.Data2** item.</span></span>
2. <span data-ttu-id="175fe-254">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-254">Select **Add**.</span></span>
3. <span data-ttu-id="175fe-255">Wählen Sie das Feld **Funktionen\\Berechnet** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-255">Select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="175fe-256">Geben Sie im Feld **Name** die Bezeichnung **LevelRecord** ein.</span><span class="sxs-lookup"><span data-stu-id="175fe-256">In the **Name** field, enter **LevelRecord**.</span></span>
5. <span data-ttu-id="175fe-257">Wählen Sie **Formel bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-257">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="175fe-258">Definieren eines Parameters für das Hinzufügen eines berechneten Felds</span><span class="sxs-lookup"><span data-stu-id="175fe-258">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="175fe-259">Wählen Sie **Parameter** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-259">Select **Parameters**.</span></span>
2. <span data-ttu-id="175fe-260">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-260">Select **New**.</span></span>
3. <span data-ttu-id="175fe-261">Geben Sie im Feld **Name** **Besteuerungsniveau** ein.</span><span class="sxs-lookup"><span data-stu-id="175fe-261">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="175fe-262">Wählen Sie im Feld **Typ** **Zeichenfolge** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-262">In the **Type** field, select **String**.</span></span>
5. <span data-ttu-id="175fe-263">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="175fe-263">Select **OK**.</span></span>

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="175fe-264">Definieren eines Ausdrucks für das Hinzufügen eines berechneten Felds</span><span class="sxs-lookup"><span data-stu-id="175fe-264">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="175fe-265">Geben Sie im Feld **Formel** Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="175fe-265">In the **Formula** field, enter the following:</span></span>  
    
    <span data-ttu-id="175fe-266">**FIRSTORNULL(\@.Levels(**</span><span class="sxs-lookup"><span data-stu-id="175fe-266">**FIRSTORNULL(\@.Levels(**</span></span>

2. <span data-ttu-id="175fe-267">Wählen Sie den Parameter **Taxation Level** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-267">Select the **Taxation Level** parameter.</span></span>
3. <span data-ttu-id="175fe-268">Wählen Sie **Datenquelle hinzufügen** aus:</span><span class="sxs-lookup"><span data-stu-id="175fe-268">Select **Add data source**.</span></span>
4. <span data-ttu-id="175fe-269">Hängen Sie im Feld **Formel** **'Taxation Level'))** an die Eingabe in Schritt 1 an, um den Ausdruck abzuschließen:</span><span class="sxs-lookup"><span data-stu-id="175fe-269">In the **Formula** field, append **'Taxation Level'))** to what you entered in Step 1 to finalize the expression to:</span></span>  
    
    <span data-ttu-id="175fe-270">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span><span class="sxs-lookup"><span data-stu-id="175fe-270">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span></span>

5. <span data-ttu-id="175fe-271">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="175fe-271">Select **Save**.</span></span>
6. <span data-ttu-id="175fe-272">Schließen Sie die Seite **Formeldesigner**.</span><span class="sxs-lookup"><span data-stu-id="175fe-272">Close **the Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="175fe-273">Abschließen des Hinzufügens eines neuen berechneten Felds</span><span class="sxs-lookup"><span data-stu-id="175fe-273">Finish adding a new calculated field</span></span>

-   <span data-ttu-id="175fe-274">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="175fe-274">Select **OK**.</span></span>

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a><span data-ttu-id="175fe-275">Verwenden des konfigurierten berechneten Felds zum Binden von Formatelementen</span><span class="sxs-lookup"><span data-stu-id="175fe-275">Use the configured calculated field to bind format elements</span></span>

1. <span data-ttu-id="175fe-276">Erweitern Sie **Model.Data2.LevelRecord**, um das konfigurierte berechnete Feld auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="175fe-276">Expand **Model.Data2.LevelRecord** to select the configured calculated field.</span></span>
2. <span data-ttu-id="175fe-277">Erweitern Sie den Container **Model.Data2.LevelRecord.aggregated** des konfigurierten berechneten Felds.</span><span class="sxs-lookup"><span data-stu-id="175fe-277">Expand the **Model.Data2.LevelRecord.aggregated** container of the configured calculated field.</span></span>
3. <span data-ttu-id="175fe-278">Wählen Sie das Feld **Model.Data2.LevelRecord.aggregated.Base** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-278">Select the **Model.Data2.LevelRecord.aggregated.Base** field.</span></span>
4. <span data-ttu-id="175fe-279">Wählen Sie das Formatelement **Statement.Taxation.None** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-279">Select the **Statement.Taxation.None** format element.</span></span>
5. <span data-ttu-id="175fe-280">Wählen Sie **Bindung aufheben** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-280">Select **Unbind**.</span></span>
6. <span data-ttu-id="175fe-281">Wählen Sie das Formatelement **Statement.Taxation.None.Base** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-281">Select the **Statement.Taxation.None.Base** format element.</span></span>
7. <span data-ttu-id="175fe-282">Wählen Sie **Bindung** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-282">Select **Bind**.</span></span>
8. <span data-ttu-id="175fe-283">Wählen Sie **Formel bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-283">Select **Edit formula**.</span></span>
9. <span data-ttu-id="175fe-284">Ändern Sie den Ausdruck in **Model.Data2.LevelRecord("None").aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="175fe-284">Change the expression to **Model.Data2.LevelRecord("None").aggregated.Base**.</span></span>

![Aktualisierter Ausdruck](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a><span data-ttu-id="175fe-286">Entfernen von berechneten Feldern, die nicht verwendet werden</span><span class="sxs-lookup"><span data-stu-id="175fe-286">Remove calculated fields that are not used</span></span>

1. <span data-ttu-id="175fe-287">Wählen Sie **Model.Data2.Level1** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-287">Select **Model.Data2.Level1**.</span></span>
2. <span data-ttu-id="175fe-288">Wählen Sei **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="175fe-288">Select **Delete**.</span></span>
3. <span data-ttu-id="175fe-289">Wählen Sie **Model.Data2.Level2** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-289">Select **Model.Data2.Level2**.</span></span>
4. <span data-ttu-id="175fe-290">Wählen Sei **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="175fe-290">Select **Delete**.</span></span>
5. <span data-ttu-id="175fe-291">Wählen Sie **Model.Data2.Level3** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-291">Select **Model.Data2.Level3**.</span></span>
6. <span data-ttu-id="175fe-292">Wählen Sei **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="175fe-292">Select **Delete**.</span></span>
7. <span data-ttu-id="175fe-293">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="175fe-293">Select **Save**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="175fe-294">Sie haben dasselbe berechnete Feld **Model.Data2.Levels** mehrmals in Formatbindungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="175fe-294">You reused the same calculated field **Model.Data2.Levels** several times in format bindings.</span></span> <span data-ttu-id="175fe-295">Es ist viel einfacher, ein einzelnes berechnetes Feld zu verwenden und beizubehalten, anstatt diesen Schritt für mehrere ähnliche Felder auszuführen.</span><span class="sxs-lookup"><span data-stu-id="175fe-295">It is much easier to use and maintain a single calculated field instead of doing this for multiple similar fields.</span></span>

8. <span data-ttu-id="175fe-296">Seite **Format-Designer** schließen.</span><span class="sxs-lookup"><span data-stu-id="175fe-296">Close the **Format designer** page.</span></span>

## <a name="complete-adjusted-version-of-a-derived-format"></a><span data-ttu-id="175fe-297">Abschließen der angepassten Version eines abgeleiteten Formats</span><span class="sxs-lookup"><span data-stu-id="175fe-297">Complete adjusted version of a derived format</span></span>

1. <span data-ttu-id="175fe-298">Wählen Sie im Inforegister **Versions** **Status ändern** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-298">In the **Versions** FastTab, select **Change status**.</span></span>
2. <span data-ttu-id="175fe-299">Wählen Sie **Abgeschlossen** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-299">Select **Complete**.</span></span>

## <a name="export-completed-version-of-a-derived-format"></a><span data-ttu-id="175fe-300">Exportieren der abgeschlossenen Version eines abgeleiteten Formats</span><span class="sxs-lookup"><span data-stu-id="175fe-300">Export completed version of a derived format</span></span>

1. <span data-ttu-id="175fe-301">Wählen Sie in der Konfigurationsstruktur **Format zum Ermitteln parametrisierter Aufrufe (benutzerdefiniert)** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-301">Select **Format to learn parameterized calls (custom)** format in the configurations tree.</span></span>
2. <span data-ttu-id="175fe-302">Wählen Sie im Inforegister **Versionen** die abgeschlossene Version 1.1.1 aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-302">In the **Versions** FastTab, select the completed version 1.1.1.</span></span>
3. <span data-ttu-id="175fe-303">Wählen Sie **Wechselkurs** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-303">Select **Exchange**.</span></span>
4. <span data-ttu-id="175fe-304">Wählen Sie **Als XML-Datei exportieren** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-304">Select **Export as XML file**.</span></span>
5. <span data-ttu-id="175fe-305">Speichern Sie die lokal heruntergeladene Konfiguration im XML-Format.</span><span class="sxs-lookup"><span data-stu-id="175fe-305">Store the downloaded configuration locally, in XML format.</span></span>

## <a name="test-er-formats"></a><span data-ttu-id="175fe-306">Testen von ER-Formaten</span><span class="sxs-lookup"><span data-stu-id="175fe-306">Test ER formats</span></span> 
<span data-ttu-id="175fe-307">Sie können die anfänglichen und verbesserten ER-Formate ausführen, um sicherzustellen, dass parametrisierte berechnete Felder, die konfiguriert sind, ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="175fe-307">You can run the initial and improved ER formats to make sure that configured parameterized calculated fields work properly.</span></span>

### <a name="import-er-configurations"></a><span data-ttu-id="175fe-308">ER Konfigurationen importieren</span><span class="sxs-lookup"><span data-stu-id="175fe-308">Import ER configurations</span></span>
<span data-ttu-id="175fe-309">Sie können überprüfte Konfigurationen aus RCS importieren, indem Sie das ER-Repository des Typs **RCS** verwenden.</span><span class="sxs-lookup"><span data-stu-id="175fe-309">You can import reviewed configurations from RCS by using the ER repository of the **RCS** type.</span></span> <span data-ttu-id="175fe-310">Wenn Sie die Schritte im Thema [Importieren von elektronischen Berichtskonfigurationen (ER-Konfigurationen) aus Regulatory Configuration Services (RCS)](rcs-download-configurations.md) bereits durchgeführt haben, verwenden Sie das konfigurierte ER-Repository, um die zuvor in diesem Thema beschriebenen Konfigurationen in Ihre Umgebung zu importieren.</span><span class="sxs-lookup"><span data-stu-id="175fe-310">If you already went through the steps in the topic, [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](rcs-download-configurations.md), use the configured ER repository to import configurations discussed earlier in this topic to your environment.</span></span> <span data-ttu-id="175fe-311">Andernfalls führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="175fe-311">Otherwise, follow these steps:</span></span>

1. <span data-ttu-id="175fe-312">Wählen Sie das Unternehmen **DEMF** und im Standard-Dashboard die Option **Elektronische Berichterstellung** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-312">Select the **DEMF** company and on the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="175fe-313">Wählen Sie **Berichterstellungskonfigurationen** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-313">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="175fe-314">Importieren Sie die Konfigurationen aus dem Microsoft Download Center in der folgenden Reihenfolge: Datenmodell, Modellzuordnung, Format.</span><span class="sxs-lookup"><span data-stu-id="175fe-314">Import the configurations from Microsoft Download Center in the following sequence: data model, model mapping, format.</span></span> <span data-ttu-id="175fe-315">Führen Sie die folgenden Schritte für jede ER-Konfiguration aus:</span><span class="sxs-lookup"><span data-stu-id="175fe-315">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="175fe-316">Wählen Sie **Wechselkurs** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-316">Select **Exchange.**</span></span>
    2. <span data-ttu-id="175fe-317">Wählen Sie **Aus XML-Datei laden** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-317">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="175fe-318">Wählen Sie **Durchsuchen** aus, um die erforderliche EB-Konfiguration im XML-Format auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="175fe-318">Select **Browse** to select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="175fe-319">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="175fe-319">Select **OK**.</span></span>

4. <span data-ttu-id="175fe-320">Importieren Sie die aus RCS exportierte abgeschlossene Version 1.1.1 des Formats **Format zum Ermitteln parametrisierter Aufrufe (benutzerdefiniert)**:</span><span class="sxs-lookup"><span data-stu-id="175fe-320">Import the exported from RCS completed version 1.1.1 of the **Format to learn parameterized calls (custom)** format:</span></span>

    1. <span data-ttu-id="175fe-321">Wählen Sie **Wechselkurs** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-321">Select **Exchange.**</span></span>
    2. <span data-ttu-id="175fe-322">Wählen Sie **Aus XML-Datei laden** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-322">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="175fe-323">Wählen Sie **Durchsuchen** aus, um die lokal gespeicherte Datei **Format zum Ermitteln parametrisierter Anrufe (benutzerdefiniert)** im XML-Format auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="175fe-323">Select **Browse** to select the locally stored **Format to learn parameterized calls (custom)** file in XML format.</span></span>
    4. <span data-ttu-id="175fe-324">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="175fe-324">Select **OK**.</span></span>

### <a name="run-er-formats"></a><span data-ttu-id="175fe-325">Ausführen von ER-Formaten</span><span class="sxs-lookup"><span data-stu-id="175fe-325">Run ER formats</span></span>

1. <span data-ttu-id="175fe-326">Erweitern Sie in der Konfigurationsstruktur den Inhalt des Elements **Modell zum Ermitteln parametrisierter Aufrufe**.</span><span class="sxs-lookup"><span data-stu-id="175fe-326">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="175fe-327">Wählen Sie **Format zum Ermitteln parametrisierter Anrufe** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-327">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="175fe-328">Wählen Sie im oberen Menüband **Ausführen** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-328">Select **Run** on the top-most ribbon.</span></span>
4. <span data-ttu-id="175fe-329">Speichern Sie das lokal generierte Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="175fe-329">Save the locally generated output.</span></span>
5. <span data-ttu-id="175fe-330">Wählen Sie das Element **Format zum Ermitteln parametrisierter Aufrufe (benutzerdefiniert)** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-330">Select the **Format to learn parameterized calls (custom)** item.</span></span>
6. <span data-ttu-id="175fe-331">Wählen Sie im oberen Menüband **Ausführen** aus.</span><span class="sxs-lookup"><span data-stu-id="175fe-331">Select **Run** on the top-most ribbon.</span></span>
7. <span data-ttu-id="175fe-332">Speichern Sie das generierte Ergebnis lokal.</span><span class="sxs-lookup"><span data-stu-id="175fe-332">Save the generated output locally.</span></span> 
8. <span data-ttu-id="175fe-333">Vergleichen Sie den Inhalt der generierten Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="175fe-333">Compare the contents of the generated outputs.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="175fe-334">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="175fe-334">Additional resources</span></span>

- [<span data-ttu-id="175fe-335">Formeldesigner in der elektronischen Berichterstellung (EB)</span><span class="sxs-lookup"><span data-stu-id="175fe-335">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="175fe-336">Verbessern Sie die Leistung von EB-Lösungen, indem Sie parametrisierte CALCULATED FIELD-Datenquellen hinzufügen</span><span class="sxs-lookup"><span data-stu-id="175fe-336">Improve performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>](er-calculated-field-ds-performance.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]