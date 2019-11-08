---
title: Unterstützen parametrisierter Aufrufe von ER-Datenquellen des Typs „Berechnetes Feld“
description: Dieses Thema enthält Informationen zum Verwenden des Typs „Berechnetes Feld“ für ER-Datenquellen.
author: NickSelin
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 20d48795b23628bbba2896bf48940936a25e0435
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550083"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a><span data-ttu-id="2f3a5-103">Unterstützen parametrisierter Aufrufe von ER-Datenquellen des Typs „Berechnetes Feld“</span><span class="sxs-lookup"><span data-stu-id="2f3a5-103">Support parameterized calls of ER data sources of the Calculated field type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2f3a5-104">In diesem Thema wird erläutert, wie Sie eine Datenquelle für die elektronische Berichterstellung (Electronic Reporting, ER) mithilfe des Typs **Berechnetes Feld** entwerfen können.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-104">This topic explains how you can design an Electronic reporting (ER) data source by using the **Calculated field** type.</span></span> <span data-ttu-id="2f3a5-105">Diese Datenquelle enthält ggf. einen ER-Ausdruck, der bei Ausführung durch die Werte der Parameterargumente gesteuert werden kann, die in einer Bindung konfiguriert sind, die diese Datenquelle aufruft.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-105">This data source may contain an ER expression that, when executed, can be controlled by the values of the parameter arguments that are configured in a binding that calls this data source.</span></span> <span data-ttu-id="2f3a5-106">Wenn Sie parametrisierte Aufrufe einer solchen Datenquelle konfigurieren, können Sie eine einzelne Datenquelle in vielen Bindungen wiederverwenden, wodurch die Gesamtanzahl der Datenquellen verringert wird, die in ER-Modellzuordnungen oder in ER-Formaten konfiguriert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-106">By configuring parameterized calls of such a data source, you can reuse a single data source in many bindings, which reduces the total number of data sources that must be configured in ER model mappings or ER formats.</span></span> <span data-ttu-id="2f3a5-107">Außerdem wird die konfigurierte ER-Komponente vereinfacht, wodurch sich die Instandhaltungskosten sowie die Kosten für die Verwendung durch andere Verbraucher verringern.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-107">It also simplifies the configured ER component, which reduces the maintenance costs and the cost of use by other consumers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2f3a5-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="2f3a5-108">Prerequisites</span></span>
<span data-ttu-id="2f3a5-109">Um die Beispiele in diesem Thema abzuschließen, müssen Sie den folgenden Zugriff haben:</span><span class="sxs-lookup"><span data-stu-id="2f3a5-109">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="2f3a5-110">Zugreifen auf eine dieser Rollen:</span><span class="sxs-lookup"><span data-stu-id="2f3a5-110">Access to one of these roles:</span></span>

    - <span data-ttu-id="2f3a5-111">Entwickler für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="2f3a5-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="2f3a5-112">Funktionaler Berater für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="2f3a5-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="2f3a5-113">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="2f3a5-113">System administrator</span></span>

- <span data-ttu-id="2f3a5-114">Zugriff auf die Regulatory Configuration Services (RCS), die für denselben Mandanten wie Finance and Operations bereitgestellt wurden, für eine der folgenden Rollen:</span><span class="sxs-lookup"><span data-stu-id="2f3a5-114">Access to Regulatory Configuration Services (RCS) that have been provisioned for the same tenant as Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="2f3a5-115">Entwickler für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="2f3a5-115">Electronic reporting developer</span></span>
    - <span data-ttu-id="2f3a5-116">Funktionaler Berater für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="2f3a5-116">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="2f3a5-117">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="2f3a5-117">System administrator</span></span>

<span data-ttu-id="2f3a5-118">Laden Sie die gezippte (komprimierte) Datei **Unterstützen parametrisierter Aufrufe von ER-Datenquellen des Typs „Berechnetes Feld“** im [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684) herunter.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-118">From the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684), download the zipped (compressed) file **Support parameterized calls of ER data sources of Calculated field type**.</span></span> <span data-ttu-id="2f3a5-119">Sie enthält die folgenden ER-Konfigurationen, die lokal extrahiert und gespeichert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-119">It contains the following ER configurations that must be extracted and stored locally.</span></span>

| <span data-ttu-id="2f3a5-120">**Inhalt**</span><span class="sxs-lookup"><span data-stu-id="2f3a5-120">**Content**</span></span>                           | <span data-ttu-id="2f3a5-121">**Dateiname**</span><span class="sxs-lookup"><span data-stu-id="2f3a5-121">**File name**</span></span>                                        |
|---------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2f3a5-122">Beispiel-EB-Datenmodell-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="2f3a5-122">Sample ER data model configuration</span></span>    | <span data-ttu-id="2f3a5-123">Model to learn parameterized calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="2f3a5-123">Model to learn parameterized calls.version.1.xml</span></span>     |
| <span data-ttu-id="2f3a5-124">Beispiel-EB-Metadatenkonfiguration</span><span class="sxs-lookup"><span data-stu-id="2f3a5-124">Sample ER metadata configuration</span></span>      | <span data-ttu-id="2f3a5-125">Metadata to learn parameterized calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="2f3a5-125">Metadata to learn parameterized calls.version.1.xml</span></span>  |
| <span data-ttu-id="2f3a5-126">Beispiel-EB-Modellzuordnungskonfiguration</span><span class="sxs-lookup"><span data-stu-id="2f3a5-126">Sample ER model mapping configuration</span></span> | <span data-ttu-id="2f3a5-127">Mapping to learn parameterized calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="2f3a5-127">Mapping to learn parameterized calls.version.1.1.xml</span></span> |
| <span data-ttu-id="2f3a5-128">Beispiel-EB-Formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="2f3a5-128">Sample ER format configuration</span></span>        | <span data-ttu-id="2f3a5-129">Format to learn parameterized calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="2f3a5-129">Format to learn parameterized calls.version.1.1.xml</span></span>  |

## <a name="sign-in-to-your-rcs-instance"></a><span data-ttu-id="2f3a5-130">Anmelden bei Ihrer RCS-Instanz</span><span class="sxs-lookup"><span data-stu-id="2f3a5-130">Sign in to your RCS instance</span></span>
<span data-ttu-id="2f3a5-131">In diesem Beispiel erstellen Sie eine Konfiguration für das Beispielunternehmen, Litware, Inc. In RCS müssen Sie zunächst die Schritte unter [Konfigurationsanbieter erstellen und als aktiv markieren](tasks/er-configuration-provider-mark-it-active-2016-11.md) abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-131">In this example, you will create a configuration for the sample company, Litware, Inc. First, in RCS, you must complete the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure:</span></span>

1. <span data-ttu-id="2f3a5-132">Wählen Sie im Standard-Dashboard **Elektronische Berichterstellung** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-132">On the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="2f3a5-133">Wählen Sie **Berichterstellungskonfigurationen** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-133">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="2f3a5-134">Importieren Sie die heruntergeladenen Konfigurationen in der folgenden Reihenfolge in RCS: Datenmodell, Metadaten, Modellzuordnung, Format.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-134">Import the downloaded configurations to RCS in the following sequence: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="2f3a5-135">Führen Sie die folgenden Schritte für jede ER-Konfiguration aus:</span><span class="sxs-lookup"><span data-stu-id="2f3a5-135">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="2f3a5-136">Wählen Sie **Wechselkurs** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-136">Select **Exchange.**</span></span>
    2. <span data-ttu-id="2f3a5-137">Wählen Sie **Aus XML-Datei laden** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-137">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="2f3a5-138">Wählen Sie **Durchsuchen** und dann die erforderliche EB-Konfiguration im XML-Format aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-138">Select **Browse**, and then select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="2f3a5-139">Wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-139">Select **OK.**</span></span>

## <a name="review-the-provided-er-solution"></a><span data-ttu-id="2f3a5-140">Überprüfen der bereitgestellten ER-Lösung</span><span class="sxs-lookup"><span data-stu-id="2f3a5-140">Review the provided ER solution</span></span>

### <a name="review-model-mapping"></a><span data-ttu-id="2f3a5-141">Überprüfen der Modellzuordnung</span><span class="sxs-lookup"><span data-stu-id="2f3a5-141">Review model mapping</span></span>

1. <span data-ttu-id="2f3a5-142">Erweitern Sie in der Konfigurationsstruktur den Inhalt des Elements **Modell zum Ermitteln parametrisierter Aufrufe**.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-142">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="2f3a5-143">Wählen Sie **Zuordnung zum Ermitteln parametrisierter Aufrufe** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-143">Select **Mapping to learn parameterized calls**.</span></span>
3. <span data-ttu-id="2f3a5-144">Wählen Sie **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-144">Select **Designer**.</span></span>
4. <span data-ttu-id="2f3a5-145">Wählen Sie **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-145">Select **Designer**.</span></span>  
   
<span data-ttu-id="2f3a5-146">Diese ER-Modellzuordnung ist für die folgenden Aktionen vorgesehen:</span><span class="sxs-lookup"><span data-stu-id="2f3a5-146">This ER model mapping is designed to do the following:</span></span>

- <span data-ttu-id="2f3a5-147">Rufen Sie die Liste der Steuercodes (**Steuer**-Datenquelle) ab, die sich in der **TaxTable**-Tabelle befinden.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-147">Fetch the list of tax codes (**Tax** data source) residing in the   **TaxTable** table.</span></span>
- <span data-ttu-id="2f3a5-148">Rufen Sie die Liste der Steuertransaktionen (**Trans**-Datenquelle) ab, die sich in der **TaxTrans**-Tabelle befinden.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-148">Fetch the list of tax transactions (**Trans** data source) residing in the   **TaxTrans** table:</span></span>
    
    - <span data-ttu-id="2f3a5-149">Gruppieren Sie die Liste der abgerufenen Transaktionen (**GR**-Datenquelle) nach Steuercode.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-149">Group the list of fetched transactions (**Gr** data source) by tax code.</span></span>
    - <span data-ttu-id="2f3a5-150">Führen Sie eine Berechnung für gruppierte Transaktionen nach aggregierten Werten pro Steuerkennzeichen durch:</span><span class="sxs-lookup"><span data-stu-id="2f3a5-150">Calculate for grouped transactions following aggregated values per   tax code:</span></span>

        - <span data-ttu-id="2f3a5-151">Summe der Steuerbasiswerte</span><span class="sxs-lookup"><span data-stu-id="2f3a5-151">Sum of tax base values.</span></span>
        - <span data-ttu-id="2f3a5-152">Summe der Steuerwerte</span><span class="sxs-lookup"><span data-stu-id="2f3a5-152">Sum of tax values.</span></span>
        - <span data-ttu-id="2f3a5-153">Mindestwert des angewendeten Steuersatzes</span><span class="sxs-lookup"><span data-stu-id="2f3a5-153">Minimum value of applied tax rate.</span></span>

<span data-ttu-id="2f3a5-154">Die Modellzuordnung in dieser Konfiguration implementiert das Basisdatenmodell für alle ER-Formate, für die dieses Modell erstellt und in Finance and Operations ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-154">The model mapping in this configuration implements the base data model for any of the ER formats created for this model and executed in Finance and Operations.</span></span> <span data-ttu-id="2f3a5-155">Demzufolge wird der Inhalt der **Steuer**- und **GR**-Datenquellen für ER-Formate wie abstrakte Datenquellen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-155">As a result, the content of the **Tax** and **Gr** data sources is exposed for ER formats such as abstract data sources.</span></span>

  ![Seite „Modellzuordnungsdesigner“ mit Steuer- und GR-Datenquellen](media/er-calculated-field-type-01.png)

5.  <span data-ttu-id="2f3a5-157">Schließen Sie die Seite **Modellzuordnungsdesigner**.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-157">Close the **Model mapping designer** page.</span></span>
6.  <span data-ttu-id="2f3a5-158">Schließen Sie die Seite **Modellzuordnung**.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-158">Close the **Model mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="2f3a5-159">Überprüfen des Formats</span><span class="sxs-lookup"><span data-stu-id="2f3a5-159">Review format</span></span>

1. <span data-ttu-id="2f3a5-160">Erweitern Sie in der Konfigurationsstruktur den Inhalt des Elements **Modell zum Ermitteln parametrisierter Aufrufe**.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-160">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="2f3a5-161">Wählen Sie **Format zum Ermitteln parametrisierter Anrufe** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-161">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="2f3a5-162">Wählen Sie **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-162">Select **Designer**.</span></span> <span data-ttu-id="2f3a5-163">Dieses ER-Format ist für die folgenden Aktionen vorgesehen:</span><span class="sxs-lookup"><span data-stu-id="2f3a5-163">This ER format is designed to do the following:</span></span>

  - <span data-ttu-id="2f3a5-164">Generieren Sie einen Steuerauszug im XML-Format.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-164">Generate a tax statement in XML format.</span></span>
  - <span data-ttu-id="2f3a5-165">Stellen Sie die folgenden Besteuerungsstufen im Steuerauszug dar: „Regulär“, „Reduziert“ und „Keine“.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-165">Present the following levels of taxation in the tax statement: regular, reduced, and none.</span></span>
  - <span data-ttu-id="2f3a5-166">Stellen Sie mehrere Details für jedes Besteuerungsniveau dar, die jeweils eine andere Anzahl von Details auf jeder Stufe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-166">Present multiple details at each taxation level, having a different number of details in each level.</span></span>

  ![Formatdesignerseite](media/er-calculated-field-type-02.png)

4. <span data-ttu-id="2f3a5-168">Wählen Sie **Zuordnung** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-168">Select **Mapping**.</span></span>
5. <span data-ttu-id="2f3a5-169">Erweitern Sie die Elemente **Modell**, **Daten,** und **Zusammenfassung**.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-169">Expand the **Model**, **Data,** and **Summary** items.</span></span> 

   <span data-ttu-id="2f3a5-170">Das berechnete Feld **Model.Data.Summary.Level** enthält den Ausdruck, der den Code des Besteuerungsniveaus (**Regulär**, **Reduziert**, **Kein,** oder **Sonstige**) als Textwert für jeden Steuercode zurückgibt, der zur Laufzeit aus der Datenquelle **Model.Data.Summary** abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-170">The calculated field **Model.Data.Summary.Level** contains the expression that returns the code of the taxation level (**Regular**, **Reduced**, **None,** or **Other**) as a text value for any tax code that can be retrieved from the **Model.Data.Summary** data source at run time.</span></span>

  ![Seite „Formatdesigner“ mit Details des Datenmodells „Modell zum Lernern parametrisierter Aufrufe“](media/er-calculated-field-type-03.png)

6. <span data-ttu-id="2f3a5-172">Erweitern Sie das Element **Modell**.**Data2**.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-172">Expand the **Model**.**Data2** item.</span></span>
7. <span data-ttu-id="2f3a5-173">Erweitern Sie das Element **Modell**.**Data2.Summary2**.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-173">Expand the **Model**.**Data2.Summary2** item.</span></span>
   
   <span data-ttu-id="2f3a5-174">Die Datenquelle **Modell**.**Data2.Summary2** ist zum Gruppieren der Transaktionsdetails der Datenquelle **Model.Data.Summary** nach Besteuerungsniveau (die vom berechneten Feld **Model.Data.Summary.Level** zurückgegeben werden) und zum Berechnen der Aggregationen konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-174">The **Model**.**Data2.Summary2** data source is configured to group the **Model.Data.Summary** data source transaction details by taxation level (returned by the **Model.Data.Summary.Level** calculated field) and compute the aggregations.</span></span>

  ![Die Seite „Formatdesigner“ mit Details der Datenquelle „Model.Data2.Summary2“](media/er-calculated-field-type-04.png)

8. <span data-ttu-id="2f3a5-176">Überprüfen Sie die berechneten Felder **Model**.**Data2.Level1**, **Model**.**Data2.Level2** und **Model**.**Data2.Level3.**</span><span class="sxs-lookup"><span data-stu-id="2f3a5-176">Review the calculated fields **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, and **Model**.**Data2.Level3.**</span></span> <span data-ttu-id="2f3a5-177">Diese berechneten Felder werden verwendet, um die Datensatzliste **Model**.**Data2.Summary2** zu filtern und nur Datensätze zurückzugeben, die ein bestimmtes Besteuerungsniveau darstellen.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-177">These calculated fields are used to filter the **Model**.**Data2.Summary2** records list and return only records that represent a particular taxation level.</span></span>
9. <span data-ttu-id="2f3a5-178">Seite **Format-Designer** schließen.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-178">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="2f3a5-179">Erstellen eines abgeleiteten Formats</span><span class="sxs-lookup"><span data-stu-id="2f3a5-179">Create a derived format</span></span>
<span data-ttu-id="2f3a5-180">Sie können das bereitgestellte Format verbessern, indem Sie ein berechnetes Feld hinzufügen, um das erforderliche Besteuerungsniveau zu filtern, anstatt die vorhandenen drei Felder zu verwenden: **Modell**.**Data2.Level1**, **Modell**.**Data2.Level2** und **Modell**.**Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-180">You can improve the provided format by adding one calculated field to filter the required taxation level instead of using the existing three fields: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** and **Model**.**Data2.Level3**.</span></span> <span data-ttu-id="2f3a5-181">Das erforderliche Besteuerungsniveau kann an dem Ort festgelegt werden, an dieses neue berechnete Feld aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-181">The required taxation level can be specified in the location where this new calculated field will be called.</span></span>

1. <span data-ttu-id="2f3a5-182">Erweitern Sie in der Konfigurationsstruktur den Inhalt des Elements **Modell zum Ermitteln parametrisierter Aufrufe**.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-182">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="2f3a5-183">Wählen Sie **Format zum Ermitteln parametrisierter Anrufe** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-183">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="2f3a5-184">Wählen Sie **Konfiguration erstellen**.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-184">Select **Create configuration**.</span></span>
4. <span data-ttu-id="2f3a5-185">Wählen Sie **Von Name ableiten: Formatieren zum Ermitteln parametrisierter Aufrufe, Microsoft** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-185">Select **Derive from Name: Format to learn parameterized calls, Microsoft**.</span></span>
5. <span data-ttu-id="2f3a5-186">Geben Sie im Feld **Name** den Text **Format zum Ermitteln parametrisierter Aufrufe (benutzerdefiniert)** ein.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-186">In the **Name** field, enter **Format to learn parameterized calls (custom)**.</span></span>
6. <span data-ttu-id="2f3a5-187">Wählen Sie **Konfiguration erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-187">Select **Create configuration.**</span></span>

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a><span data-ttu-id="2f3a5-188">Konfigurieren eines parametrisierten berechneten Felds, das eine Liste der Datensätze zurückgibt</span><span class="sxs-lookup"><span data-stu-id="2f3a5-188">Configure a parameterized calculated field that returns a list of records</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="2f3a5-189">Hinzufügen eines neuen berechneten Felds</span><span class="sxs-lookup"><span data-stu-id="2f3a5-189">Start adding a new calculated field</span></span>

1. <span data-ttu-id="2f3a5-190">Wählen Sie **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-190">Select **Designer**.</span></span>
2. <span data-ttu-id="2f3a5-191">Wählen Sie **Erweitern/Reduzieren** aus, um alle Formatelemente zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-191">Select **Expand/collapse** to expand all format items.</span></span>
3. <span data-ttu-id="2f3a5-192">Wählen Sie **Zuordnung** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-192">Select **Mapping**.</span></span>
4. <span data-ttu-id="2f3a5-193">Erweitern Sie das Element **Model**.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-193">Expand the **Model** item.</span></span>
5. <span data-ttu-id="2f3a5-194">Wählen Sie das Element **Modell.Data2** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-194">Select the **Model.Data2** item.</span></span>
6. <span data-ttu-id="2f3a5-195">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-195">Select **Add**.</span></span>
7. <span data-ttu-id="2f3a5-196">Wählen Sie das Feld **Funktionen\\Berechnet** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-196">Select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="2f3a5-197">Geben Sie im Feld **Name** **Ebenen** ein.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-197">In the **Name** field, enter **Levels**.</span></span>
9. <span data-ttu-id="2f3a5-198">Wählen Sie **Formel bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-198">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="2f3a5-199">Definieren eines Parameters für das Hinzufügen eines berechneten Felds</span><span class="sxs-lookup"><span data-stu-id="2f3a5-199">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="2f3a5-200">Wählen Sie **Parameter** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-200">Select **Parameters**.</span></span>
2. <span data-ttu-id="2f3a5-201">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-201">Select **New**.</span></span>
3. <span data-ttu-id="2f3a5-202">Geben Sie im Feld **Name** **Besteuerungsniveau** ein.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-202">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="2f3a5-203">Wählen Sie im Feld **Typ** **Zeichenfolge** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-203">In the **Type** field, select **String**.</span></span>

    <span data-ttu-id="2f3a5-204">Es können nur primitive Datentypen verwendet werden, um das Argument des Parametertyps anzugeben.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-204">Only primitive data types can be used to specify the type of the parameter’s argument.</span></span> <span data-ttu-id="2f3a5-205">Daher können die Typen **Datensatzliste**, **Datensatz** und **Enumeration** nicht für diesen Zweck verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-205">Therefore, **Record list**, **Record**, and **Enum** types cannot be used for this purpose.</span></span>

    <span data-ttu-id="2f3a5-206">Für ein einzelnes berechnetes Feld können maximal 8 Parameter angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-206">The maximum number of parameters that can be specified for a single calculated field is 8.</span></span>

    ![Liste der Parameterdatenquellen](media/er-calculated-field-type-05.png)

5. <span data-ttu-id="2f3a5-208">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-208">Select **OK**.</span></span>

<span data-ttu-id="2f3a5-209">Durch das Hinzufügen dieses Parameters legen Sie die Bedingung fest, die vorliegen muss, um dieses berechnete Feld aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-209">By adding this parameter, you specify the condition that must be in place to call this calculated field.</span></span> <span data-ttu-id="2f3a5-210">Wenn Sie dieses berechnete Feld aufrufen, müssen Sie das Argument des Paramaters **Besteuerungsniveau** als Wert mit dem Format **Zeichenfolge** angeben.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-210">When you call this calculated field, you need to specify the argument of the **Taxation Level** parameter as a value with **String** format.</span></span>

   <span data-ttu-id="2f3a5-211">Stellen Sie sicher, dass Sie Parameter nur für die berechneten Felder definieren, die sich in einem Container (**Datensatzliste**, **Datensatz** oder **Container**) befinden.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-211">Make sure that you define parameters only for those calculated fields that reside in a container (either **Record list**, **Record**, or **Container**).</span></span>

   <span data-ttu-id="2f3a5-212">Der konfigurierte Parameter ist in der Liste der Datenquellen für dieses berechnete Feld verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-212">The configured parameter is available in the list of data sources for this calculated field.</span></span> <span data-ttu-id="2f3a5-213">Sie können dem konfigurierten Ausdruck den Parameter hinzuzufügen, indem Sie **Datenquelle hinzufügen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-213">You can add the parameter to the configured expression by selecting **Add data source**.</span></span>

   ![Datenquellenfelder](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="2f3a5-215">Definieren eines Ausdrucks für das Hinzufügen eines berechneten Felds</span><span class="sxs-lookup"><span data-stu-id="2f3a5-215">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="2f3a5-216">Geben Sie im Feld **Formel** Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="2f3a5-216">In the **Formula** field, enter:</span></span> 

    <span data-ttu-id="2f3a5-217">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span><span class="sxs-lookup"><span data-stu-id="2f3a5-217">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span></span>
    
2. <span data-ttu-id="2f3a5-218">Wählen Sie den Parameter **Besteuerungsniveau** in der Liste der Datenquellen aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-218">Select the **Taxation Level** parameter in the list of data sources.</span></span>
3. <span data-ttu-id="2f3a5-219">Wählen Sie **Datenquelle hinzufügen** aus:</span><span class="sxs-lookup"><span data-stu-id="2f3a5-219">Select **Add data source**.</span></span>
4. <span data-ttu-id="2f3a5-220">Stellen Sie den Ausdruck im Feld **Formel** folgendermaßen fertig:</span><span class="sxs-lookup"><span data-stu-id="2f3a5-220">In the **Formula** field, finalize the expression as:</span></span>  

    <span data-ttu-id="2f3a5-221">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span><span class="sxs-lookup"><span data-stu-id="2f3a5-221">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span></span>

5. <span data-ttu-id="2f3a5-222">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-222">Select **Save**.</span></span>

    ![Informationen zu Datenquellenfeldern](media/er-calculated-field-type-07.png)

6. <span data-ttu-id="2f3a5-224">Schließen Sie die Seite **Formeldesigner**.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-224">Close the **Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="2f3a5-225">Abschließen des Hinzufügens eines neuen berechneten Felds</span><span class="sxs-lookup"><span data-stu-id="2f3a5-225">Finish adding a new calculated field</span></span>

- <span data-ttu-id="2f3a5-226">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-226">Select **OK**.</span></span>

<span data-ttu-id="2f3a5-227">Für das konfigurierte, parametrisierte berechnete Feld **Ebenen** auf der Seite **Formatdesigner** ist ein Argument vom Typ **Zeichenfolge** erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-227">On the **Format designer** page, the configured parameterized calculated field **Levels** requires a **String** argument.</span></span>

![Erweiterte Liste der Ebenen des berechneten Felds](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a><span data-ttu-id="2f3a5-229">Verwenden Sie das berechnete Feld für konfigurierte verbindliche Formatelemente</span><span class="sxs-lookup"><span data-stu-id="2f3a5-229">Use the configured calculated field for binding format elements</span></span>

1. <span data-ttu-id="2f3a5-230">Wählen Sie **Model.Data2.Levels** aus, um das konfigurierte berechnete Feld auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-230">Select **Model.Data2.Levels** to select the configured calculated field.</span></span>
2. <span data-ttu-id="2f3a5-231">Wählen Sie das Formatelement **Statement.Taxation.Regular** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-231">Select the **Statement.Taxation.Regular** format element.</span></span>
3. <span data-ttu-id="2f3a5-232">Wählen Sie **Bindung** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-232">Select **Bind**.</span></span>
4. <span data-ttu-id="2f3a5-233">Wählen Sie **Ja** aus, um die Ersetzung der derzeit verwendeten Datenquelle **Level1** durch die neue Datenquelle **Ebenen** in allen geschachtelten Formatelementen des ausgewählten Formatelements zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-233">Select **Yes** to confirm the replacement of the currently used data source, **Level1**, by the new data source, **Levels**, in all nested format elements of the selected format element.</span></span>

    <span data-ttu-id="2f3a5-234">Die angewendete Bindung wurde als Aufruf des parametrisierten berechneten Felds erstellt.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-234">Applied binding has been built as a call of the parameterized calculated field.</span></span> <span data-ttu-id="2f3a5-235">Standardmäßig wird der Name des gebundenen Formatelements als Argument für das parametrisierte berechnete Feld unter den folgenden Bedingungen erstellt:</span><span class="sxs-lookup"><span data-stu-id="2f3a5-235">By default, the name of the bound format element is used as an argument for parameterized calculated field under the following conditions:</span></span>

      - <span data-ttu-id="2f3a5-236">Das berechnete Feld ist für die Verwendung eines einzelnen Parameters konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-236">The calculated field is configured to use a single parameter.</span></span>
      - <span data-ttu-id="2f3a5-237">Der Datentyp dieses Parameters ist als **Zeichenfolge** definiert.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-237">The data type of this parameter is defined as **String**.</span></span>

    <span data-ttu-id="2f3a5-238">Wenn der Name des gebundenen Formatelements leer ist, wird der Datenquellenname dieses Elements in der angewendeten Bindung verwendet.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-238">When the name of the bound format element is blank, the data source name of this element is used in applied binding.</span></span>

5. <span data-ttu-id="2f3a5-239">Wählen Sie das Formatelement **Statement.Taxation.Reduced** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-239">Select the **Statement.Taxation.Reduced** format element.</span></span>
6. <span data-ttu-id="2f3a5-240">Wählen Sie **Bindung** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-240">Select **Bind**.</span></span>
7. <span data-ttu-id="2f3a5-241">Wählen Sie **Ja** aus, um die Ersetzung der derzeit verwendeten Datenquelle **Level2** durch die neue Datenquelle **Ebenen** in allen geschachtelten Formatelementen unter dem ausgewählten Formatelement zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-241">Select **Yes** to confirm the replacement of the currently used data source, **Level2**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>
8. <span data-ttu-id="2f3a5-242">Wählen Sie das Formatelement **Statement.Taxation.None** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-242">Select the **Statement.Taxation.None** format element.</span></span>
9. <span data-ttu-id="2f3a5-243">Wählen Sie **Bindung** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-243">Select **Bind**.</span></span>
10. <span data-ttu-id="2f3a5-244">Wählen Sie **Ja** aus, um die Ersetzung der derzeit verwendeten Datenquelle **Level3** durch die neue Datenquelle **Ebenen** in allen geschachtelten Formatelementen unter dem ausgewählten Formatelement zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-244">Select **Yes** to confirm the replacement of the currently used data source, **Level3**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>

   <span data-ttu-id="2f3a5-245">Wenn Sie das Argument des parametrisierten berechneten Felds für das XML-Element angeben, das das Besteuerungsniveau darstellt (z. B. **Model.Data2.Levels("Reduced")** als Textwert), müssen Sie diesen Schritt nicht für die geschachtelten XML-Attribute ausführen. Deren Bindungen übernehmen den Wert des auf der übergeordneten Ebene zugeordneten Arguments (**Model.Data2.Levels.aggregated.Base**, nicht **Model.Data2.Levels("Reduced").aggregated.Base**).</span><span class="sxs-lookup"><span data-stu-id="2f3a5-245">When you specify the argument of the parameterized calculated field for the XML element representing taxation level (for example, **Model.Data2.Levels("Reduced")** as a text value), you don’t need to do the same for nested XML attributes—their bindings will automatically inherit the value of the argument defined on the parent level (**Model.Data2.Levels.aggregated.Base**, not **Model.Data2.Levels("Reduced").aggregated.Base**).</span></span>

<span data-ttu-id="2f3a5-246">Wiederkehrende Aufrufe von parametrisierten berechneten Feldern werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-246">Recurrent calls of any parameterized calculated field are not supported.</span></span>

<span data-ttu-id="2f3a5-247">Sie können **Formel bearbeiten** auswählen und das standardmäßig übernommene Argument des parametrisierten berechneten Felds in der ausgewählten Bindung ändern.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-247">You can select **Edit formula**, and change the applied-by-default argument of the parameterized calculated field in the selected binding.</span></span> <span data-ttu-id="2f3a5-248">Wenn dieses Argument nicht vorhanden ist, kann dies zu Fehlern während der Laufzeit kommen. Benutzer werden über solch eine Situation informiert, wenn das aktuelle Format überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-248">If this argument is missing, it can cause errors at run time — users are informed about such a situation when the current format is validated.</span></span>

![Benachrichtigung zu Überprüfungswarnungen](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a><span data-ttu-id="2f3a5-250">Konfigurieren eines parametrisierten berechneten Felds für die Rückgabe eines Datensatzes</span><span class="sxs-lookup"><span data-stu-id="2f3a5-250">Configure a parameterized calculated field to return a record</span></span>
<span data-ttu-id="2f3a5-251">Wenn ein parametrisiertes berechnetes Feld einen Datensatz zurückgibt, müssen Sie die Bindung einzelner Felder dieses Datensatzes zu Formatelementen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-251">When a parameterized calculated field returns a record, you need to support binding of individual fields of this record to format elements.</span></span> <span data-ttu-id="2f3a5-252">In solchen Fällen ist keine übergeordnete Bindung vorhanden, die den Wert eines Arguments zum Aufrufen eines parametrisierten berechneten Felds enthält. Dieser Wert muss in der Bindung des Felds einen einzelnen Datensatz definiert werden.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-252">In such cases there will be no parent binding that contains the value of an argument to call a parameterized calculated field — this value must be defined in the binding of a single record’s field.</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="2f3a5-253">Hinzufügen eines neuen berechneten Felds</span><span class="sxs-lookup"><span data-stu-id="2f3a5-253">Start adding a new calculated field</span></span>

1. <span data-ttu-id="2f3a5-254">Wählen Sie das Element **Modell.Data2** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-254">Select the **Model.Data2** item.</span></span>
2. <span data-ttu-id="2f3a5-255">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-255">Select **Add**.</span></span>
3. <span data-ttu-id="2f3a5-256">Wählen Sie das Feld **Funktionen\\Berechnet** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-256">Select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="2f3a5-257">Geben Sie im Feld **Name** die Bezeichnung **LevelRecord** ein.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-257">In the **Name** field, enter **LevelRecord**.</span></span>
5. <span data-ttu-id="2f3a5-258">Wählen Sie **Formel bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-258">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="2f3a5-259">Definieren eines Parameters für das Hinzufügen eines berechneten Felds</span><span class="sxs-lookup"><span data-stu-id="2f3a5-259">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="2f3a5-260">Wählen Sie **Parameter** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-260">Select **Parameters**.</span></span>
2. <span data-ttu-id="2f3a5-261">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-261">Select **New**.</span></span>
3. <span data-ttu-id="2f3a5-262">Geben Sie im Feld **Name** **Besteuerungsniveau** ein.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-262">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="2f3a5-263">Wählen Sie im Feld **Typ** **Zeichenfolge** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-263">In the **Type** field, select **String**.</span></span>
5. <span data-ttu-id="2f3a5-264">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-264">Select **OK**.</span></span>

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="2f3a5-265">Definieren eines Ausdrucks für das Hinzufügen eines berechneten Felds</span><span class="sxs-lookup"><span data-stu-id="2f3a5-265">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="2f3a5-266">Geben Sie im Feld **Formel** Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="2f3a5-266">In the **Formula** field, enter the following:</span></span>  
    
    <span data-ttu-id="2f3a5-267">**FIRSTORNULL(\@.Levels(**</span><span class="sxs-lookup"><span data-stu-id="2f3a5-267">**FIRSTORNULL(\@.Levels(**</span></span>

2. <span data-ttu-id="2f3a5-268">Wählen Sie den Parameter **Taxation Level** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-268">Select the **Taxation Level** parameter.</span></span>
3. <span data-ttu-id="2f3a5-269">Wählen Sie **Datenquelle hinzufügen** aus:</span><span class="sxs-lookup"><span data-stu-id="2f3a5-269">Select **Add data source**.</span></span>
4. <span data-ttu-id="2f3a5-270">Hängen Sie im Feld **Formel** **'Taxation Level'))** an die Eingabe in Schritt 1 an, um den Ausdruck abzuschließen:</span><span class="sxs-lookup"><span data-stu-id="2f3a5-270">In the **Formula** field, append **'Taxation Level'))** to what you entered in Step 1 to finalize the expression to:</span></span>  
    
    <span data-ttu-id="2f3a5-271">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span><span class="sxs-lookup"><span data-stu-id="2f3a5-271">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span></span>

5. <span data-ttu-id="2f3a5-272">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-272">Select **Save**.</span></span>
6. <span data-ttu-id="2f3a5-273">Schließen Sie die Seite **Formeldesigner**.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-273">Close **the Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="2f3a5-274">Abschließen des Hinzufügens eines neuen berechneten Felds</span><span class="sxs-lookup"><span data-stu-id="2f3a5-274">Finish adding a new calculated field</span></span>

-   <span data-ttu-id="2f3a5-275">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-275">Select **OK**.</span></span>

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a><span data-ttu-id="2f3a5-276">Verwenden des konfigurierten berechneten Felds zum Binden von Formatelementen</span><span class="sxs-lookup"><span data-stu-id="2f3a5-276">Use the configured calculated field to bind format elements</span></span>

1. <span data-ttu-id="2f3a5-277">Erweitern Sie **Model.Data2.LevelRecord**, um das konfigurierte berechnete Feld auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-277">Expand **Model.Data2.LevelRecord** to select the configured calculated field.</span></span>
2. <span data-ttu-id="2f3a5-278">Erweitern Sie den Container **Model.Data2.LevelRecord.aggregated** des konfigurierten berechneten Felds.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-278">Expand the **Model.Data2.LevelRecord.aggregated** container of the configured calculated field.</span></span>
3. <span data-ttu-id="2f3a5-279">Wählen Sie das Feld **Model.Data2.LevelRecord.aggregated.Base** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-279">Select the **Model.Data2.LevelRecord.aggregated.Base** field.</span></span>
4. <span data-ttu-id="2f3a5-280">Wählen Sie das Formatelement **Statement.Taxation.None** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-280">Select the **Statement.Taxation.None** format element.</span></span>
5. <span data-ttu-id="2f3a5-281">Wählen Sie **Bindung aufheben** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-281">Select **Unbind**.</span></span>
6. <span data-ttu-id="2f3a5-282">Wählen Sie das Formatelement **Statement.Taxation.None.Base** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-282">Select the **Statement.Taxation.None.Base** format element.</span></span>
7. <span data-ttu-id="2f3a5-283">Wählen Sie **Bindung** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-283">Select **Bind**.</span></span>
8. <span data-ttu-id="2f3a5-284">Wählen Sie **Formel bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-284">Select **Edit formula**.</span></span>
9. <span data-ttu-id="2f3a5-285">Ändern Sie den Ausdruck in **Model.Data2.LevelRecord("None").aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-285">Change the expression to **Model.Data2.LevelRecord("None").aggregated.Base**.</span></span>

![Aktualisierter Ausdruck](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a><span data-ttu-id="2f3a5-287">Entfernen von berechneten Feldern, die nicht verwendet werden</span><span class="sxs-lookup"><span data-stu-id="2f3a5-287">Remove calculated fields that are not used</span></span>

1. <span data-ttu-id="2f3a5-288">Wählen Sie **Model.Data2.Level1** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-288">Select **Model.Data2.Level1**.</span></span>
2. <span data-ttu-id="2f3a5-289">Wählen Sei **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-289">Select **Delete**.</span></span>
3. <span data-ttu-id="2f3a5-290">Wählen Sie **Model.Data2.Level2** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-290">Select **Model.Data2.Level2**.</span></span>
4. <span data-ttu-id="2f3a5-291">Wählen Sei **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-291">Select **Delete**.</span></span>
5. <span data-ttu-id="2f3a5-292">Wählen Sie **Model.Data2.Level3** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-292">Select **Model.Data2.Level3**.</span></span>
6. <span data-ttu-id="2f3a5-293">Wählen Sei **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-293">Select **Delete**.</span></span>
7. <span data-ttu-id="2f3a5-294">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-294">Select **Save**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="2f3a5-295">Sie haben dasselbe berechnete Feld **Model.Data2.Levels** mehrmals in Formatbindungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-295">You reused the same calculated field **Model.Data2.Levels** several times in format bindings.</span></span> <span data-ttu-id="2f3a5-296">Es ist viel einfacher, ein einzelnes berechnetes Feld zu verwenden und beizubehalten, anstatt diesen Schritt für mehrere ähnliche Felder auszuführen.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-296">It is much easier to use and maintain a single calculated field instead of doing this for multiple similar fields.</span></span>

8. <span data-ttu-id="2f3a5-297">Seite **Format-Designer** schließen.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-297">Close the **Format designer** page.</span></span>

## <a name="complete-adjusted-version-of-a-derived-format"></a><span data-ttu-id="2f3a5-298">Abschließen der angepassten Version eines abgeleiteten Formats</span><span class="sxs-lookup"><span data-stu-id="2f3a5-298">Complete adjusted version of a derived format</span></span>

1. <span data-ttu-id="2f3a5-299">Wählen Sie im Inforegister **Versions** **Status ändern** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-299">In the **Versions** FastTab, select **Change status**.</span></span>
2. <span data-ttu-id="2f3a5-300">Wählen Sie **Abgeschlossen** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-300">Select **Complete**.</span></span>

## <a name="export-completed-version-of-a-derived-format"></a><span data-ttu-id="2f3a5-301">Exportieren der abgeschlossenen Version eines abgeleiteten Formats</span><span class="sxs-lookup"><span data-stu-id="2f3a5-301">Export completed version of a derived format</span></span>

1. <span data-ttu-id="2f3a5-302">Wählen Sie in der Konfigurationsstruktur **Format zum Ermitteln parametrisierter Aufrufe (benutzerdefiniert)** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-302">Select **Format to learn parameterized calls (custom)** format in the configurations tree.</span></span>
2. <span data-ttu-id="2f3a5-303">Wählen Sie im Inforegister **Versionen** die abgeschlossene Version 1.1.1 aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-303">In the **Versions** FastTab, select the completed version 1.1.1.</span></span>
3. <span data-ttu-id="2f3a5-304">Wählen Sie **Wechselkurs** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-304">Select **Exchange**.</span></span>
4. <span data-ttu-id="2f3a5-305">Wählen Sie **Als XML-Datei exportieren** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-305">Select **Export as XML file**.</span></span>
5. <span data-ttu-id="2f3a5-306">Speichern Sie die lokal heruntergeladene Konfiguration im XML-Format.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-306">Store the downloaded configuration locally, in XML format.</span></span>

## <a name="test-er-formats"></a><span data-ttu-id="2f3a5-307">Testen von ER-Formaten</span><span class="sxs-lookup"><span data-stu-id="2f3a5-307">Test ER formats</span></span> 
<span data-ttu-id="2f3a5-308">Sie können die anfänglichen und verbesserten ER-Formate ausführen, um sicherzustellen, dass parametrisierte berechnete Felder, die konfiguriert sind, ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-308">You can run the initial and improved ER formats to make sure that configured parameterized calculated fields work properly.</span></span>

### <a name="import-er-configurations"></a><span data-ttu-id="2f3a5-309">ER Konfigurationen importieren</span><span class="sxs-lookup"><span data-stu-id="2f3a5-309">Import ER configurations</span></span>
<span data-ttu-id="2f3a5-310">Sie können überprüfte Konfigurationen aus RCS importieren, indem Sie das ER-Repository des Typs **RCS** verwenden.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-310">You can import reviewed configurations from RCS by using the ER repository of the **RCS** type.</span></span> <span data-ttu-id="2f3a5-311">Wenn Sie die Schritte im Thema, [Importieren von Konfigurationen für die elektronische Berichterstellung (Electronic Reporting, ER) aus den gesetzlichen Konfigurationsdiensten (Regulatory Configuration Services, RCS)](rcs-download-configurations.md) bereits ausgeführt haben, verwenden Sie das ER-Repository, um die weiter oben in diesem Thema erläuterten Konfigurationen in Ihre Umgebung zu importieren.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-311">If you already went through the steps in the topic, [Import Electronic reporting configurations from Regulatory Configuration Services](rcs-download-configurations.md), use the configured ER repository to import configurations discussed earlier in this topic to your environment.</span></span> <span data-ttu-id="2f3a5-312">Andernfalls führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="2f3a5-312">Otherwise, follow these steps:</span></span>

1. <span data-ttu-id="2f3a5-313">Wählen Sie das Unternehmen **DEMF** und im Standard-Dashboard die Option **Elektronische Berichterstellung** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-313">Select the **DEMF** company and on the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="2f3a5-314">Wählen Sie **Berichterstellungskonfigurationen** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-314">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="2f3a5-315">Importieren Sie die Konfigurationen aus dem Microsoft Download Center in der folgenden Reihenfolge: Datenmodell, Modellzuordnung, Format.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-315">Import the configurations from Microsoft Download Center in the following sequence: data model, model mapping, format.</span></span> <span data-ttu-id="2f3a5-316">Führen Sie die folgenden Schritte für jede ER-Konfiguration aus:</span><span class="sxs-lookup"><span data-stu-id="2f3a5-316">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="2f3a5-317">Wählen Sie **Wechselkurs** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-317">Select **Exchange.**</span></span>
    2. <span data-ttu-id="2f3a5-318">Wählen Sie **Aus XML-Datei laden** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-318">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="2f3a5-319">Wählen Sie **Durchsuchen** aus, um die erforderliche EB-Konfiguration im XML-Format auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-319">Select **Browse** to select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="2f3a5-320">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-320">Select **OK**.</span></span>

4. <span data-ttu-id="2f3a5-321">Importieren Sie die aus RCS exportierte abgeschlossene Version 1.1.1 des Formats **Format zum Ermitteln parametrisierter Aufrufe (benutzerdefiniert)**:</span><span class="sxs-lookup"><span data-stu-id="2f3a5-321">Import the exported from RCS completed version 1.1.1 of the **Format to learn parameterized calls (custom)** format:</span></span>

    1. <span data-ttu-id="2f3a5-322">Wählen Sie **Wechselkurs** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-322">Select **Exchange.**</span></span>
    2. <span data-ttu-id="2f3a5-323">Wählen Sie **Aus XML-Datei laden** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-323">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="2f3a5-324">Wählen Sie **Durchsuchen** aus, um die lokal gespeicherte Datei **Format zum Ermitteln parametrisierter Anrufe (benutzerdefiniert)** im XML-Format auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-324">Select **Browse** to select the locally stored **Format to learn parameterized calls (custom)** file in XML format.</span></span>
    4. <span data-ttu-id="2f3a5-325">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-325">Select **OK**.</span></span>

### <a name="run-er-formats"></a><span data-ttu-id="2f3a5-326">Ausführen von ER-Formaten</span><span class="sxs-lookup"><span data-stu-id="2f3a5-326">Run ER formats</span></span>

1. <span data-ttu-id="2f3a5-327">Erweitern Sie in der Konfigurationsstruktur den Inhalt des Elements **Modell zum Ermitteln parametrisierter Aufrufe**.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-327">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="2f3a5-328">Wählen Sie **Format zum Ermitteln parametrisierter Anrufe** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-328">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="2f3a5-329">Wählen Sie im oberen Menüband **Ausführen** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-329">Select **Run** on the top-most ribbon.</span></span>
4. <span data-ttu-id="2f3a5-330">Speichern Sie das lokal generierte Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-330">Save the locally generated output.</span></span>
5. <span data-ttu-id="2f3a5-331">Wählen Sie das Element **Format zum Ermitteln parametrisierter Aufrufe (benutzerdefiniert)** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-331">Select the **Format to learn parameterized calls (custom)** item.</span></span>
6. <span data-ttu-id="2f3a5-332">Wählen Sie im oberen Menüband **Ausführen** aus.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-332">Select **Run** on the top-most ribbon.</span></span>
7. <span data-ttu-id="2f3a5-333">Speichern Sie das generierte Ergebnis lokal.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-333">Save the generated output locally.</span></span> 
8. <span data-ttu-id="2f3a5-334">Vergleichen Sie den Inhalt der generierten Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="2f3a5-334">Compare the contents of the generated outputs.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2f3a5-335">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2f3a5-335">Additional resources</span></span>
[<span data-ttu-id="2f3a5-336">Formeldesigner in der elektronischen Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="2f3a5-336">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
