---
title: Verbessern Sie die Leistung von EB-Lösungen, indem Sie parametrisierte CALCULATED FIELD-Datenquellen hinzufügen
description: In diesem Thema wird erläutert, wie Sie die Leistung von EB-Lösungen (Electroinic Reporting) verbessern können, indem Sie parametrisierte CALCULATED FIELD-Datenquellen hinzufügen.
author: NickSelin
manager: AnnBe
ms.date: 09/02/2020
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
ms.openlocfilehash: a87098e82284a4951f3a4de050f6ba3f587fd20a
ms.sourcegitcommit: 5472005274f2f94fba82dda90de128f39d8b8390
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760081"
---
# <a name="improve-the-performance-of-er-solutions-by-adding-parameterized-calculated-field-data-sources"></a><span data-ttu-id="ef2f2-103">Verbessern Sie die Leistung von EB-Lösungen, indem Sie parametrisierte CALCULATED FIELD-Datenquellen hinzufügen</span><span class="sxs-lookup"><span data-stu-id="ef2f2-103">Improve the performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ef2f2-104">In diesem Thema wird erklärt, wie Sie [Leistungsnachverfolgungen](trace-execution-er-troubleshoot-perf.md) von [Elektronische Berichterstattung (ER)](general-electronic-reporting.md)-Formaten übernehmen können, die ausgeführt werden, und die dann die Informationen aus diesen Nachverfolgungen verwenden, um die Leistung durch das Konfigurieren eines Parameters zu verbessern, indem die **Berechnetes Feld**-Datenquelle parameterisiert wird.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-104">This topic explains how you can take [performance traces](trace-execution-er-troubleshoot-perf.md) of [Electronic reporting (ER)](general-electronic-reporting.md) formats that are run, and then use the information from those traces to help improve performance by configuring a parameterized **Calculated field** data source.</span></span>

<span data-ttu-id="ef2f2-105">Im Rahmen des Prozesses, EB-Konfigurationen zu entwerfen, um Geschäftsdokumente zu generieren, definieren Sie die Methode, mit der Daten aus der Anwendung abgerufen werden und in der generierten Ausgabe eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-105">As part of the process of designing ER configurations to generate business documents, you define the method that is used to retrieve data from the application and enter it in the generated output.</span></span> <span data-ttu-id="ef2f2-106">Durch das Entwerfen einer parametrisierten EB-Datenquelle des Typs **Berechnetes Feld** können Sie die Anzahl der Datenbankaufrufe reduzieren und den Zeit- und Kostenaufwand für das Sammeln der Details der Ausführung des EB-Formats erheblich reduzieren.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-106">By designing a parametrized ER data source of the **Calculated field** type, you can reduce the number of database calls, and significantly reduce the time and cost that are involved in collecting the details of ER format execution.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ef2f2-107">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="ef2f2-107">Prerequisites</span></span>

- <span data-ttu-id="ef2f2-108">Um die Beispiele in diesem Thema abzuschließen, müssen Sie den Zugriff auf eine der folgenden [Rollen](../sysadmin/tasks/assign-users-security-roles.md) haben:</span><span class="sxs-lookup"><span data-stu-id="ef2f2-108">To complete the examples in this topic, you must have the access to one of the following [roles](../sysadmin/tasks/assign-users-security-roles.md):</span></span>

    - <span data-ttu-id="ef2f2-109">Entwickler für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="ef2f2-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="ef2f2-110">Funktionaler Berater für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="ef2f2-110">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="ef2f2-111">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="ef2f2-111">System administrator</span></span>

- <span data-ttu-id="ef2f2-112">Das Unternehmen muss auf **DEMF** festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-112">The company must be set to **DEMF**.</span></span>
- <span data-ttu-id="ef2f2-113">Folgen Sie den Schritten in [Anhang 1](#appendix1) dieses Themas, um die Komponenten der Microsoft EB-Beispiellösung herunterzuladen, die zum Abschließen der Beispiele in diesem Thema erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-113">Follow the steps in [Appendix 1](#appendix1) of this topic to download the components of the sample Microsoft ER solution that is required to complete the examples in this topic.</span></span>
- <span data-ttu-id="ef2f2-114">Befolgen Sie die Schritte in [Anlage 2](#appendix2) dieses Themas, um den minimalen Satz von EB-Parametern zu konfigurieren, der zur Verwendung des EB-Frameworks erforderlich ist, um die Leistung der Microsoft EB-Beispiellösung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-114">Follow the steps in [Appendix 2](#appendix2) of this topic to configure the minimal set of ER parameters that is required to use the ER framework to help improve the performance of the sample Microsoft ER solution.</span></span>

## <a name="import-the-sample-er-solution"></a><span data-ttu-id="ef2f2-115">EB-Beispiellösung importieren</span><span class="sxs-lookup"><span data-stu-id="ef2f2-115">Import the sample ER solution</span></span>

<span data-ttu-id="ef2f2-116">Stellen Sie sich vor, Sie müssen eine neue EB-Lösung entwerfen, um einen neuen Bericht zu generieren, der Kreditorentransaktionen zeigt.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-116">Imagine that you must design an ER solution to generate a new report that shows vendor transactions.</span></span> <span data-ttu-id="ef2f2-117">Aktuell können Sie die Transaktionen für einen ausgewählten Kreditor auf der Seite **Kreditorenbuchungen** suchen (wechseln Sie zu **Kreditor** \> **Kreditoren** \> **Alle Kreditoren**, wählen Sie einen Kreditor aus, und dann, im Aktivitätsbereich unter der Registerkarte **Kreditor** in der Gruppe **Transaktionen** wählen Sie **Transaktionen**).</span><span class="sxs-lookup"><span data-stu-id="ef2f2-117">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable** \> **Vendors** \> **All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="ef2f2-118">Sie möchten jedoch alle Kreditorenbuchungen zusammen in einem elektronischen Dokument im XML-Format haben.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-118">However, you want to have all vendor transactions together in one electronic document in XML format.</span></span> <span data-ttu-id="ef2f2-119">Diese Lösung besteht aus mehreren EB-Konfigurationen, die das erforderliche Datenmodell, die Modellzuordnung und Formatkomponenten enthalten.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-119">This solution will consist of several ER configurations that contain the required data model, model mapping, and format components.</span></span>

<span data-ttu-id="ef2f2-120">Der erste Schritt besteht darin, die Beispiel-EB-Lösung zu importieren, um einen Bericht über Lieferantentransaktionen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-120">The first step is to import the sample ER solution to generate a vendor transactions report.</span></span>

1. <span data-ttu-id="ef2f2-121">Melden Sie sich bei der Instanz von Microsoft Dynamics 365 Finance an, die für Ihr Unternehmen bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-121">Sign in to the instance of Microsoft Dynamics 365 Finance that is provisioned for your company.</span></span>
2. <span data-ttu-id="ef2f2-122">In diesem Thema erstellen und modifizieren Sie Konfigurationen für das Beispielunternehmen **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-122">In this topic, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="ef2f2-123">Stellen Sie sicher, dass dieser Konfigurationsanbieter Ihrer Finance-Instanz hinzugefügt wurde und als aktiv markiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-123">Make sure that this configuration provider has been added to your Finance instance and is marked as active.</span></span> <span data-ttu-id="ef2f2-124">Weitere Informationen finden Sie unter [Konfigurationsanbieter erstellen und als aktiv markieren](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="ef2f2-124">For more information, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="ef2f2-125">Im Arbeitsbereich **Elektronische Berichterstellung** wählen Sie die Kachel **Berichterstellungskonfigurationen** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-125">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="ef2f2-126">Auf der Seite **Konfigurationen** importieren Sie die EB-Konfigurationen, die Sie als Voraussetzung nach Finance heruntergeladen haben, in der folgenden Reihenfolge: Datenmodell, Modellzuordnung, Format.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-126">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into Finance, in the following order: data model, model mapping, format.</span></span> <span data-ttu-id="ef2f2-127">Führen Sie für jede Konfiguration die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="ef2f2-127">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="ef2f2-128">Wählen Sie im Aktivitätsbereich **Austausch** \> **Aus XML-Datei laden** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-128">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
    2. <span data-ttu-id="ef2f2-129">Wählen Sie **Durchsuchen** aus, und wählen Sie die entsprechende Datei für die erforderliche EB-Konfiguration im XML-Format auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-129">Select **Browse**, and select the appropriate file for the ER configuration in XML format.</span></span>
    3. <span data-ttu-id="ef2f2-130">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-130">Select **OK**.</span></span>

![Importierte Konfigurationen auf der Seite „Konfigurationen“](./media/er-calculated-field-ds-performance-imported-configurations.png)

## <a name="review-the-sample-er-solution"></a><span data-ttu-id="ef2f2-132">Die EB-Beispiellösung überprüfen</span><span class="sxs-lookup"><span data-stu-id="ef2f2-132">Review the sample ER solution</span></span>

### <a name="review-the-model-mapping"></a><span data-ttu-id="ef2f2-133">Die Modellzuordnung überprüfen</span><span class="sxs-lookup"><span data-stu-id="ef2f2-133">Review the model mapping</span></span>

1. <span data-ttu-id="ef2f2-134">Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur **Leistungsverbesserungsmodell** und wählen Sie dann **Leistungsverbesserungszuordnung** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-134">On the **Configurations** page, in the configuration tree, expand **Performance improvement model**, and select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="ef2f2-135">Wählen Sie im Aktivitätsbereich **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-135">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="ef2f2-136">Wählen Sie auf der Seite **Modell für Datenquellenzuordnung** im Aktionsbereich **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-136">On the **Model to datasource mapping** page, on the Action Pane, select **Designer**.</span></span>

    <span data-ttu-id="ef2f2-137">Diese EB-Modellzuordnung ist für die Durchführung der folgenden Aktionen vorgesehen:</span><span class="sxs-lookup"><span data-stu-id="ef2f2-137">This ER model mapping is designed to perform the following actions:</span></span>

    - <span data-ttu-id="ef2f2-138">Rufen Sie die Liste der Lieferantentransaktionen ab, die in der VendTrans-Tabelle gespeichert sind (**Trans**-Datenquelle).</span><span class="sxs-lookup"><span data-stu-id="ef2f2-138">Fetch the list of vendor transactions that are stored in the VendTrans table (**Trans** data source).</span></span>
    - <span data-ttu-id="ef2f2-139">Rufen Sie für jede Transaktion aus der VendTable-Tabelle den Datensatz eines Anbieters ab, für den die Transaktion gebucht wurde (**\#Vend**-Datenquelle).</span><span class="sxs-lookup"><span data-stu-id="ef2f2-139">For every transaction, fetch, from the VendTable table, the record of a vendor that the transaction has been posted for (**\#Vend** data source).</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef2f2-140">Die **\#Vend**-Datenquelle ist so konfiguriert, dass der entsprechende Lieferantendatensatz unter Verwendung der vorhandenen n:1-Beziehung **\@.'\>Relations'.VendTable\_AccountNum** abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-140">The **\#Vend** data source is configured to fetch the corresponding vendor record by using the existing many-to-one relation **\@.'\>Relations'.VendTable\_AccountNum**.</span></span>

    <span data-ttu-id="ef2f2-141">Die Modellzuordnung in dieser Konfiguration implementiert das Basisdatenmodell für alle EB-Formate, für die dieses Modell erstellt und in Finance ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-141">The model mapping in this configuration implements the base data model for any ER formats that are created for this model and run in Finance.</span></span> <span data-ttu-id="ef2f2-142">Demzufolge wird der Inhalt der **Trans** -Datenquellen für EB-Formate wie abstrakte **Modell**-Datenquellen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-142">Therefore, the content of the **Trans** data source is exposed for ER formats such as abstract **model** data sources.</span></span>

    ![Trans-Datenquelle auf der Modellzuordnungsdesigner-Seite](media/er-calculated-field-ds-performance-mapping-1.png)

4. <span data-ttu-id="ef2f2-144">Schließen Sie die Seite **Modellzuordnungsdesigner**.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-144">Close the **Model mapping designer** page.</span></span>
5. <span data-ttu-id="ef2f2-145">Schließen Sie die Seite **Modell für Datenquellenzuordnung**.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-145">Close the **Model to datasource mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="ef2f2-146">Überprüfen des Formats</span><span class="sxs-lookup"><span data-stu-id="ef2f2-146">Review format</span></span>

1. <span data-ttu-id="ef2f2-147">Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur **Leistungsverbesserungsmodell** und wählen Sie dann **Leistungsverbesserungsformat** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-147">On the **Configurations** page, in the configuration tree, expand **Performance improvement model**, and select **Performance improvement format**.</span></span>
2. <span data-ttu-id="ef2f2-148">Wählen Sie im Aktivitätsbereich **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-148">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="ef2f2-149">Auf der Seite **Formatdesigner** wählen Sie auf der Registerkarte **Zuordnung** **Erweitern/Reduzieren** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-149">On the **Format designer** page, on the **Mapping** tab, select **Expand/Collapse**.</span></span>
4. <span data-ttu-id="ef2f2-150">Erweitern Sie die Elemente **Modell**, **Daten,** und **Transaktion**.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-150">Expand the **Model**, **Data,** and **Transaction** items.</span></span>

    <span data-ttu-id="ef2f2-151">Dieses EB-Format dient zum Generieren eines Lieferantentransaktionsberichts im XML-Format.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-151">This ER format is designed to generate a vendor transactions report in XML format.</span></span>

    ![Formatieren Sie Datenquellen und konfigurierte Bindungen von Formatelementen auf der Seite Format-Designer](media/er-calculated-field-ds-performance-format.png)

5. <span data-ttu-id="ef2f2-153">Seite **Format-Designer** schließen.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-153">Close the **Format designer** page.</span></span>

## <a name="run-the-sample-er-solution-to-trace-execution"></a><span data-ttu-id="ef2f2-154">Ausführen der EB-Beispiellösung, um Ausführung nachzuverfolgen</span><span class="sxs-lookup"><span data-stu-id="ef2f2-154">Run the sample ER solution to trace execution</span></span>

<span data-ttu-id="ef2f2-155">Stellen Sie sich vor, dass Sie das Entwerfen der ersten Version der EB-Lösung beendet haben.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-155">Imagine that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="ef2f2-156">Jetzt möchten Sie die Lösung in Ihrer Finance-Instanz testen und die Ausführungsleistung analysieren.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-156">You now want to test the solution in your Finance instance and analyze the execution performance.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="ef2f2-157">Aktivieren der EB-Leistungsnachverfolgung</span><span class="sxs-lookup"><span data-stu-id="ef2f2-157">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="ef2f2-158">Wählen Sie das Unternehmen **DEMF** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-158">Select the **DEMF** company.</span></span>
2. <span data-ttu-id="ef2f2-159">Befolgen Sie die Schritte in [Aktivieren der EB-Leistungsverfolgung](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace), um eine Leistungsverfolgung zu generieren, während ein EB-Format ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-159">Follow the steps in [Turn on the ER performance trace](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) to generate a performance trace while an ER format is run.</span></span>

    ![Benutzerparameter-Dialogfeld](media/er-calculated-field-ds-performance-format-user-parameters.png)

### <a name="run-the-er-format"></a><a id="run-format"></a><span data-ttu-id="ef2f2-161">Das EB-Format ausführen</span><span class="sxs-lookup"><span data-stu-id="ef2f2-161">Run the ER format</span></span>

1. <span data-ttu-id="ef2f2-162">Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-162">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="ef2f2-163">Auf der Seite **Konfigurationen** in der Konfigurationsstruktur wählen Sie das Element **Leistungsverbesserungsformat** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-163">On the **Configurations** page, in the configuration tree, select **Performance improvement format**.</span></span>
3. <span data-ttu-id="ef2f2-164">Wählen Sie im Aktivitätsbereich auf **Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-164">On the Action Pane, select **Run**.</span></span>

## <a name="use-the-performance-trace-to-analyze-model-mapping-performance"></a><span data-ttu-id="ef2f2-165">Verwenden Sie die Leistungsverfolgung, um die Leistung der Modellzuordnung zu analysieren</span><span class="sxs-lookup"><span data-stu-id="ef2f2-165">Use the performance trace to analyze model mapping performance</span></span>

1. <span data-ttu-id="ef2f2-166">Auf der Seite **Konfigurationen** in der Konfigurationsstruktur wählen Sie das Element **Leistungsverbesserungszuordnung** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-166">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="ef2f2-167">Wählen Sie im Aktivitätsbereich **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-167">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="ef2f2-168">Wählen Sie auf der Seite **Modellzuordnung** im Aktionsbereich **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-168">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="ef2f2-169">Auf der Seite **Modellzuordnungsdesigner** im Aktivitätsbereich wählen Sie **Leistungsnachverfolgung** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-169">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="ef2f2-170">Wählen Sie die zuletzt generierte Nachverfolgung aus und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-170">Select the most recent trace that was generated, and then select **OK**.</span></span>

<span data-ttu-id="ef2f2-171">Neue Informationen sind jetzt für einige Datenquellelemente der aktuellen Modellzuordnung verfügbar:</span><span class="sxs-lookup"><span data-stu-id="ef2f2-171">New information is now available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="ef2f2-172">Tatsächlicher Zeitaufwand für das Abrufen von Daten mithilfe der Datenquelle</span><span class="sxs-lookup"><span data-stu-id="ef2f2-172">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="ef2f2-173">Die gleiche Zeit, ausgedrückt als Prozentsatz der gesamten Zeit, die für das Ausführen der gesamten Modellzuordnung aufgewendet wurde</span><span class="sxs-lookup"><span data-stu-id="ef2f2-173">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

![Details zur Ausführungszeit auf der Seite „Model Mapping Designer“](./media/er-calculated-field-ds-performance-mapping-2.png)

<span data-ttu-id="ef2f2-175">Das **Leistungsstatistik**-Raster zeigt, dass die **Trans**-Datenquelle die VendTrans-Tabelle einmal aufruft.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-175">The **Performance statistics** grid shows that the **Trans** data source calls the VendTrans table one time.</span></span> <span data-ttu-id="ef2f2-176">Der Wert **\[265\]\[M: 265\]** der **Trans**-Datenquelle gibt an, dass 265 Lieferantentransaktionen aus der Anwendungstabelle abgerufen und an das Datenmodell zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-176">The value **\[265\]\[Q:265\]** of the **Trans** data source indicates that 265 vendor transactions have been fetched from the application table and returned to the data model.</span></span>

<span data-ttu-id="ef2f2-177">Das **Leistungsstatistik**-Raster zeigt auch, dass die aktuelle Modellzuordnung die Datenbankanforderungen dupliziert, während die **\#Vend**-Datenquelle ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-177">The **Performance statistics** grid also shows that the current model mapping duplicates database requests while the **\#Vend** data source is run.</span></span> <span data-ttu-id="ef2f2-178">Diese Verdopplung tritt aus folgenden Gründen auf:</span><span class="sxs-lookup"><span data-stu-id="ef2f2-178">This duplication occurs for the following reasons:</span></span>

- <span data-ttu-id="ef2f2-179">Die Lieferantentabelle wird für jede der 265 durchlaufenen Lieferantentransaktionen zweimal aufgerufen, was insgesamt 530 Aufrufen entspricht:</span><span class="sxs-lookup"><span data-stu-id="ef2f2-179">The vendor table is called two times for each of the 265 iterated vendor transactions, for a total of 530 calls:</span></span>

    - <span data-ttu-id="ef2f2-180">Ein Anruf wird getätigt, um die Lieferantenkontonummer einzugeben.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-180">One call is made to enter the vendor account number.</span></span>
    - <span data-ttu-id="ef2f2-181">Ein Anruf wird getätigt, um den Lieferantennamen einzugeben.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-181">One call is made to enter the vendor name.</span></span>

- <span data-ttu-id="ef2f2-182">Die Lieferantentabelle wird für jede durchlaufene Lieferantentransaktion aufgerufen, obwohl die abgerufenen Transaktionen nur für fünf Lieferanten gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-182">The vendor table is called for each iterated vendor transaction, even though the fetched transactions have been posted for only five vendors.</span></span> <span data-ttu-id="ef2f2-183">Von den 530 Anrufen sind 525 Duplikate.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-183">Of the 530 calls, 525 are duplicates.</span></span> <span data-ttu-id="ef2f2-184">Die folgende Abbildung zeigt die Nachricht, die Sie über doppelte Aufrufe (Datenbankanforderungen) erhalten.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-184">The following illustration shows the message that you receive about duplicate calls (database requests).</span></span>

![Meldung zu doppelten Datenbankanforderungen auf der Seite Modellzuordnungsdesigner](./media/er-calculated-field-ds-performance-mapping-2a.png)

<span data-ttu-id="ef2f2-186">Beachten Sie, dass mehr als 80 Prozent (ungefähr sechs Sekunden) der Gesamtausführungszeit für die Modellzuordnung (ca. acht Sekunden) für das Abrufen von Werten aus der VendTable-Anwendungstabelle aufgewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-186">Of the total model mapping execution time (approximately eight seconds), notice that more than 80 percent (approximately six seconds) has been spent retrieving values from the VendTable application table.</span></span> <span data-ttu-id="ef2f2-187">Dieser Prozentsatz ist zu groß für zwei Attribute von fünf Anbietern im Vergleich zum Informationsvolumen aus der VendTrans-Anwendungstabelle.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-187">That percentage is too large for two attributes of five vendors, compared with the volume of information from the VendTrans application table.</span></span>

<span data-ttu-id="ef2f2-188">Um die Anzahl der Anrufe zu verringern, die getätigt werden, um die Lieferantendetails für jede Transaktion abzurufen, und um die Leistung der Modellzuordnung zu verbessern, können Sie Caching für die **\#Vend**-Datenquelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-188">To reduce the number of calls that are made to get the vendor details for every transaction, and to improve the performance of the model mapping, you can use caching for the **\#Vend** data source.</span></span>

> [!NOTE]
> <span data-ttu-id="ef2f2-189">Die **Trans\\\#Vend**-Datenquelle wird im Rahmen der aktuellen Transaktion der **Trans**-Datenquelle zur Laufzeit zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-189">The **Trans\\\#Vend** data source will be cached in the scope of the current transaction of the **Trans** data source at runtime.</span></span>

<span data-ttu-id="ef2f2-190">Durch das Zwischenspeichern der **\#Vend**-Datenquelle reduzieren die Anzahl der doppelten Anrufe von 525 auf 260, beseitigen die Duplizierung jedoch nicht vollständig.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-190">By caching the **\#Vend** data source, you reduce the number of duplicated calls from 525 to 260, but you don't completely eliminate the duplication.</span></span> <span data-ttu-id="ef2f2-191">Um die Verdopplung vollständig zu vermeiden, können Sie eine neue parametrisierte Datenquelle des Typs **Berechnetes Feld** konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-191">To completely eliminate duplication, you can configure a new parameterized data source of the **Calculated field** type.</span></span>

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="ef2f2-192">Verbessern der Modellzuordnung auf der Grundlage von Informationen aus der Ausführungsnachverfolgung</span><span class="sxs-lookup"><span data-stu-id="ef2f2-192">Improve the model mapping based on information from the execution trace</span></span>

### <a name="change-the-logic-of-the-model-mapping"></a><span data-ttu-id="ef2f2-193">Die Logik der Modellzuordnung ändern</span><span class="sxs-lookup"><span data-stu-id="ef2f2-193">Change the logic of the model mapping</span></span>

<span data-ttu-id="ef2f2-194">Befolgen Sie diese Schritte, um das Caching und eine Datenquelle des Typs **Berechnetes Feld** zu verwenden, um doppelte Aufrufe der Datenbank zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-194">Follow these steps to use caching and a data source of the **Calculated field** type, to help prevent duplicate calls to the database.</span></span>

1. <span data-ttu-id="ef2f2-195">Auf der Seite **Konfigurationen** in der Konfigurationsstruktur wählen Sie das Element **Leistungsverbesserungszuordnung** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-195">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="ef2f2-196">Wählen Sie im Aktivitätsbereich **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-196">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="ef2f2-197">Wählen Sie auf der Seite **Modellzuordnung** im Aktionsbereich **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-197">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="ef2f2-198">Befolgen Sie auf der **Modellzuordnungsdesigner**-Seite diese Schritte, um eine Datenquelle des Typs **Tabellendatensätze** hinzuzufügen, um auf Datensätze in der VendTable-Anwendungstabelle zuzugreifen:</span><span class="sxs-lookup"><span data-stu-id="ef2f2-198">On the **Model mapping designer** page, follow these steps to add a data source of the **Table records** type to access records in the VendTable application table:</span></span>

    1. <span data-ttu-id="ef2f2-199">Erweitern Sie im Bereich **Datenquellentypen** den Eintrag **Dynamics 365 for Operations** und wählen Sie **Tabellendatensätze** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-199">In the **Data source types** pane, expand **Dynamics 365 for Operations**, and select **Table records**.</span></span>
    2. <span data-ttu-id="ef2f2-200">Wählen Sie **Stamm hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-200">Select **Add root**.</span></span>
    3. <span data-ttu-id="ef2f2-201">Geben Sie im Drop-Down-Dialogfeld im Feld **Name** **Vend** ein.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-201">In the dialog box, in the **Name** field, enter **Vend**.</span></span>
    4. <span data-ttu-id="ef2f2-202">Geben Sie im Feld **Tabelle** den Eintrag **VendTable** ein.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-202">In the **Table** field, enter **VendTable**.</span></span>
    5. <span data-ttu-id="ef2f2-203">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-203">Select **OK**.</span></span>

5. <span data-ttu-id="ef2f2-204">Sie können Aufrufe von Datenquellen des Typs **Berechnetes Feld** nur prameterisieren, wenn sich diese Datenquellen in einem Container befinden.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-204">You can parameterize calls to data sources of the **Calculated field** type only if those data sources reside in a container.</span></span> <span data-ttu-id="ef2f2-205">Befolgen Sie daher diese Schritte, um eine Datenquelle des Typs **Leerer Container** hinzuzufügen, um eine neue parametrisierte Datenquelle des Typs **Berechnetes Feld** zu speichern:</span><span class="sxs-lookup"><span data-stu-id="ef2f2-205">Therefore, follow these steps to add a data source of the **Empty container** type to hold a new parameterized data source of the **Calculated field** type:</span></span>

    1. <span data-ttu-id="ef2f2-206">Erweitern Sie im Bereich **Datenquellentypen** den Eintrag **Allgemein** und wählen Sie **Leerer Container** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-206">In the **Data source types** pane, expand **General**, and select **Empty container**.</span></span>
    2. <span data-ttu-id="ef2f2-207">Wählen Sie **Stamm hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-207">Select **Add root**.</span></span>
    3. <span data-ttu-id="ef2f2-208">Geben Sie im Drop-Down-Dialogfeld im Feld **Name** **Box** ein.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-208">In the dialog box, in the **Name** field, enter **Box**.</span></span>
    3. <span data-ttu-id="ef2f2-209">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-209">Select **OK**.</span></span>

    ![Box-Datenquelle auf der Modellzuordnungsdesigner-Seite](./media/er-calculated-field-ds-performance-mapping-3.png)

6. <span data-ttu-id="ef2f2-211">Befolgen Sie diese Schritte, um eine parametrisierte Datenquelle des Typs **Berechnetes Feld** hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="ef2f2-211">Follow these steps to add a parameterized data source of the **Calculated field** type:</span></span>

    1. <span data-ttu-id="ef2f2-212">Wählen Sie **Box** im Bereich **Datenquellen** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-212">In the **Data sources** pane, select **Box**.</span></span>
    2. <span data-ttu-id="ef2f2-213">Erweitern Sie im Bereich **Datenquellentypen** **Funktionen**, und wählen Sie **Berechnetes Feld** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-213">In the **Data source types** pane, expand **Functions**, and select **Calculated field**.</span></span>
    3. <span data-ttu-id="ef2f2-214">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-214">Select **Add**.</span></span>
    4. <span data-ttu-id="ef2f2-215">Geben Sie im Drop-Down-Dialogfeld im Feld **Name** **Vend** ein.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-215">In the dialog box, in the **Name** field, enter **Vend**.</span></span>
    5. <span data-ttu-id="ef2f2-216">Wählen Sie **Formel bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-216">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="ef2f2-217">Wählen Sie auf der **Formeldesigner**-Seite **Parameter**, um die Parameter anzugeben, die beim Aufruf dieser Datenquelle angegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-217">On the **Formula designer** page, select **Parameters** to specify the parameters that must be provided when this data source is called.</span></span>
    7. <span data-ttu-id="ef2f2-218">Wählen Sie im Dialogfeld **Parameter** **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-218">In the **Parameters** dialog box, select **New**.</span></span>
    8. <span data-ttu-id="ef2f2-219">Geben Sie im Feld **Name** **parmVendAccNumber** ein.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-219">In the **Name** field, enter **parmVendAccNumber**.</span></span>
    9. <span data-ttu-id="ef2f2-220">Wählen Sie im Feld **Typ** **Zeichenfolge** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-220">In the **Type** field, select **String**.</span></span>
    10. <span data-ttu-id="ef2f2-221">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-221">Select **OK**.</span></span>
    11. <span data-ttu-id="ef2f2-222">Geben Sie im **Formel**-Feld **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))** ein.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-222">In the **Formula** field, enter **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**.</span></span>
    12. <span data-ttu-id="ef2f2-223">Wählen Sie **Speichern** und schließen Sie die Seite **Formeldesginer**.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-223">Select **Save**, and close the **Formula designer** page.</span></span>
    13. <span data-ttu-id="ef2f2-224">Wählen Sie **OK** aus, um die neue Datenquelle hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-224">Select **OK** to add the new data source.</span></span>

7. <span data-ttu-id="ef2f2-225">Führen Sie die folgenden Schritte aus, um die hinzugefügte Datenquelle während der Ausführung als zwischengespeichert zu markieren:</span><span class="sxs-lookup"><span data-stu-id="ef2f2-225">Follow these steps to mark the added data source as cached during the execution:</span></span>

    1. <span data-ttu-id="ef2f2-226">Wählen Sie im Bereich **Datenquellen** den Eintrag **Box\\Vend** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-226">In the **Data sources** pane, select **Box\\Vend**.</span></span>
    2. <span data-ttu-id="ef2f2-227">Wählen Sie **Cache** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-227">Select **Cache**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef2f2-228">Die **Box\\Vend**-Datenquelle wird im Rahmen aller Kreditorenbuchungsseite der **Trans**-Datenquelle zur Laufzeit zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-228">The **Box\\Vend** data source will be cached in the scope of all vendor transactions of the **Trans** data source at runtime.</span></span>

8. <span data-ttu-id="ef2f2-229">Befolgen Sie diese Schritte, um die verschachtelte **Trans\\\#Vend**-Datenquelle zu aktualisieren, so dass die **Box\\Vend**-Datenquelle verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="ef2f2-229">Follow these steps to update the nested **Trans\\\#Vend** data source so that it uses the **Box\\Vend** data source:</span></span>

    1. <span data-ttu-id="ef2f2-230">Erweitern Sie im Bereich **Datenquellen** den Eintrag **Trans**.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-230">In the **Data sources** pane, expand **Trans**.</span></span>
    2. <span data-ttu-id="ef2f2-231">Wählen Sie die **Trans\\\#Vend**-Datenquelle, und wählen Sie dann **Bearbeiten** \> **Formel bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-231">Select the **Trans\\\#Vend** data source, and then select **Edit** \> **Edit formula**.</span></span>
    3. <span data-ttu-id="ef2f2-232">Geben Sie auf der **Formeldesigner**-Seite im **Formel**-Feld **Box.Vend(\@.AccountNum)** ein.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-232">On the **Formula designer** page, in the **Formula** field, enter **Box.Vend(\@.AccountNum)**.</span></span>
    4. <span data-ttu-id="ef2f2-233">Wählen Sie **Speichern** und dann schließen Sie die Seite **Formeldesginer**.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-233">Select **Save**, and then close the **Formula designer** page.</span></span>
    5. <span data-ttu-id="ef2f2-234">Wählen Sie **OK**, um Ihre Änderungen an der ausgewählten Datenquelle abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-234">Select **OK** to complete your changes to the selected data source.</span></span>

9. <span data-ttu-id="ef2f2-235">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-235">Select **Save**.</span></span>

    ![Vend-Datenquelle auf der Modellzuordnungsdesigner-Seite](./media/er-calculated-field-ds-performance-mapping-4.png)

10. <span data-ttu-id="ef2f2-237">Schließen Sie die Seite **Modellzuordnungsdesigner**.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-237">Close the **Model mapping designer** page.</span></span>
11. <span data-ttu-id="ef2f2-238">Schließen Sie die Seite **Modellzuordnungen**.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-238">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="ef2f2-239">Die geänderte Version der EB-Modellzuordnung abschließen</span><span class="sxs-lookup"><span data-stu-id="ef2f2-239">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="ef2f2-240">Auf der Seite **Konfigurationen** im Inforegister **Versionen** wählen Sie die Version **1.2** der Konfiguration **Leistungsverbesserungszuordnung** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-240">On the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance improvement mapping** configuration.</span></span>
2. <span data-ttu-id="ef2f2-241">Wählen Sie **Status ändern** \> **Abschließen** und dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-241">Select **Change status** \> **Complete**, and then select **OK**.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="ef2f2-242">Ausführen der geänderten EB-Lösung, um Ausführung nachzuverfolgen</span><span class="sxs-lookup"><span data-stu-id="ef2f2-242">Run the modified ER solution to trace execution</span></span>

<span data-ttu-id="ef2f2-243">Wiederholen Sie die Schritte im Abschnitt [Das EB-Format ausführen](#run-format) weiter oben in diesem Thema, um eine neue Leistungsnachverfolgung zu generieren.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-243">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="use-the-performance-trace-to-analyze-adjustments-to-the-model-mapping"></a><span data-ttu-id="ef2f2-244">Verwenden Sie die Leistungsüberwachung, um Regulierungen der Modellzuordnung zu analysieren</span><span class="sxs-lookup"><span data-stu-id="ef2f2-244">Use the performance trace to analyze adjustments to the model mapping</span></span> 

1. <span data-ttu-id="ef2f2-245">Auf der Seite **Konfigurationen** in der Konfigurationsstruktur wählen Sie das Element **Leistungsverbesserungszuordnung** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-245">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="ef2f2-246">Wählen Sie im Aktivitätsbereich **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-246">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="ef2f2-247">Wählen Sie auf der Seite **Modellzuordnung** im Aktionsbereich **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-247">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="ef2f2-248">Auf der Seite **Modellzuordnungsdesigner** im Aktivitätsbereich wählen Sie **Leistungsnachverfolgung** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-248">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="ef2f2-249">Wählen Sie die zuletzt generierte Nachverfolgung aus und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-249">Select the most recent trace that was generated, and then select **OK**.</span></span>

<span data-ttu-id="ef2f2-250">Beachten Sie, dass die Regulierungen, die Sie an der Modellzuordnung vorgenommen haben, doppelte Abfragen an eine Datenbank beseitigt haben.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-250">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="ef2f2-251">Die Anzahl der Aufrufe an Datenbanktabellen und Datenquellen für diese Modellzuordnung ist auch reduziert worden.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-251">The number of calls to database tables and data sources for this model mapping has also been reduced.</span></span>

![Überwachungsinformationen auf der Modellzuordnungsdesigner-Seite 1](./media/er-calculated-field-ds-performance-mapping-5.png)

<span data-ttu-id="ef2f2-253">Die Gesamtausführungszeit wurde ungefähr 20 Mal reduziert (von ungefähr 8 Sekunden auf ungefähr 400 Millisekunden).</span><span class="sxs-lookup"><span data-stu-id="ef2f2-253">The total execution time has been reduced about 20 times (from about 8 seconds to about 400 milliseconds).</span></span> <span data-ttu-id="ef2f2-254">Daher wurde die Leistung der gesamten EB-Lösung verbessert.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-254">Therefore, the performance of the whole ER solution has been improved.</span></span>

![Überwachungsinformationen auf der Modellzuordnungsdesigner-Seite 2](./media/er-calculated-field-ds-performance-mapping-5a.png)

## <a name="appendix-1-download-the-components-of-the-sample-microsoft-er-solution"></a><a name="appendix1"></a><span data-ttu-id="ef2f2-256">Anhang 1: Laden Sie die Komponenten der Microsoft EB-Beispiellösung herunter</span><span class="sxs-lookup"><span data-stu-id="ef2f2-256">Appendix 1: Download the components of the sample Microsoft ER solution</span></span>

<span data-ttu-id="ef2f2-257">Sie müssen die folgenden Dateien herunterladen und lokal speichern.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-257">You must download the following files and store them locally.</span></span>

| <span data-ttu-id="ef2f2-258">Datei</span><span class="sxs-lookup"><span data-stu-id="ef2f2-258">File</span></span>                                        | <span data-ttu-id="ef2f2-259">Inhalt</span><span class="sxs-lookup"><span data-stu-id="ef2f2-259">Content</span></span> |
|---------------------------------------------|---------|
| <span data-ttu-id="ef2f2-260">Leistungsverbesserung model.version.1</span><span class="sxs-lookup"><span data-stu-id="ef2f2-260">Performance improvement model.version.1</span></span>     | [<span data-ttu-id="ef2f2-261">Beispiel-EB-Datenmodell-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="ef2f2-261">Sample ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="ef2f2-262">Leistungsverbesserung mapping.version.1.1</span><span class="sxs-lookup"><span data-stu-id="ef2f2-262">Performance improvement mapping.version.1.1</span></span> | [<span data-ttu-id="ef2f2-263">Beispiel-EB-Modellzuordnungskonfiguration</span><span class="sxs-lookup"><span data-stu-id="ef2f2-263">Sample ER model mapping configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="ef2f2-264">Leistungsverbesserung format.version.1.1</span><span class="sxs-lookup"><span data-stu-id="ef2f2-264">Performance improvement format.version.1.1</span></span>  | [<span data-ttu-id="ef2f2-265">Beispiel-EB-Formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="ef2f2-265">Sample ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

## <a name="appendix-2-configure-the-er-framework"></a><a name="appendix2"></a><span data-ttu-id="ef2f2-266">Anhang 2: Konfigurieren des EB-Frameworks</span><span class="sxs-lookup"><span data-stu-id="ef2f2-266">Appendix 2: Configure the ER framework</span></span>

<span data-ttu-id="ef2f2-267">Bevor Sie das EB-Framework verwenden können, um die Leistung der Microsoft EB-Beispiellösung zu verbessern, müssen Sie den minimalen Satz von EB-Parametern konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-267">Before you can start to use the ER framework to improve the performance of the sample Microsoft ER solution, you must configure the minimal set of ER parameters.</span></span>

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a><span data-ttu-id="ef2f2-268">Parameter der elektronischen Berichterstellung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="ef2f2-268">Configure ER parameters</span></span>

1. <span data-ttu-id="ef2f2-269">Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-269">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="ef2f2-270">Wählen Sie auf der Seite **Lokalisierungskonfigurationen** im Bereich **Zugehörige Links** die Option **Parameter für elektronische Berichterstellung** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-270">On the **Localization configurations** page, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="ef2f2-271">Auf der Seite **Parameter für elektronische Berichterstellung** legen Sie auf der Registerkarte **Allgemein** die Option **Entwurfsmodus aktivieren** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-271">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="ef2f2-272">Legen Sie auf der Registerkarte **Anhänge** die folgenden Parameter fest:</span><span class="sxs-lookup"><span data-stu-id="ef2f2-272">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="ef2f2-273">Wählen Sie im Feld **Konfigurationen** den **Dateityp** für das **DEMF**-Unternehmen aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-273">In the **Configurations** field, select the **File** type for the **DEMF** company.</span></span>
    - <span data-ttu-id="ef2f2-274">Wählen Sie in den Feldern **Einzelvorgangsarchiv**, **Temporär**, **Grundlage** und **Andere** den **Dateityp** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-274">In the **Job archive**, **Temporary**, **Baseline**, and **Others** fields, select the **File** type.</span></span>

<span data-ttu-id="ef2f2-275">Weitere Informationen zu EB-Parametern finden Sie unter [Konfigurieren des EB-Frameworks](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ef2f2-275">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="ef2f2-276">Aktivieren eines EB-Konfigurationsanbieters</span><span class="sxs-lookup"><span data-stu-id="ef2f2-276">Activate an ER configuration provider</span></span>

<span data-ttu-id="ef2f2-277">Jede hinzugefügte EB-Konfiguration wird als Eigentum eines EB-Konfigurationsanbieters markiert.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-277">Every ER configuration that is added is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="ef2f2-278">Der EB-Konfigurationsanbieter, der im Arbeitsbereich **Elektronische Berichterstellung** aktiviert ist, wird zu diesem Zweck verwendet.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-278">The ER configuration provider that is activated in the **Electronic reporting** workspace is used for this purpose.</span></span> <span data-ttu-id="ef2f2-279">Daher müssen Sie im Arbeitsbereich **Elektronische Berichterstellung** einen EB-Konfigurationsanbieter aktivieren, bevor Sie mit dem Hinzufügen oder Bearbeiten von EB-Konfigurationen beginnen.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-279">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="ef2f2-280">Nur der Besitzer einer EB-Konfiguration kann die Konfiguration bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-280">Only the owner of an ER configuration can edit the configuration.</span></span> <span data-ttu-id="ef2f2-281">Daher muss im Arbeitsbereich **Elektronische Berichterstellung** der entsprechende EB-Konfigurationsanbieter aktiviert werden, bevor eine EB-Konfigurationen bearbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-281">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a><span data-ttu-id="ef2f2-282">Überprüfen der Liste der EB-Konfigurationsanbieter</span><span class="sxs-lookup"><span data-stu-id="ef2f2-282">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="ef2f2-283">Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-283">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="ef2f2-284">Wählen Sie auf der Seite **Lokalisierungskonfigurationen** im Bereich **Zugehörige Links** die Option **Konfigurationsanbieter** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-284">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="ef2f2-285">Auf der Seite **Konfigurationsanbietertabelle** hat jeder Anbieterdatensatz einen eindeutigen Namen und eine eindeutige URL.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-285">On the **Configuration provider table** page, each provider record has a unique name and URL.</span></span> <span data-ttu-id="ef2f2-286">Überprüfen Sie den Inhalt dieser Seite.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-286">Review the contents of this page.</span></span> <span data-ttu-id="ef2f2-287">Wenn bereits ein Datensatz für **Litware, Inc.** vorhanden ist, überspringen Sie die nächste Prozedur [Hinzufügen eines neuen EB-Konfigurationsanbieters](#ActivateProvider).</span><span class="sxs-lookup"><span data-stu-id="ef2f2-287">If a record for **Litware, Inc.** already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="ef2f2-288">Hinzufügen eines neuen EB-Konfigurationsanbieters</span><span class="sxs-lookup"><span data-stu-id="ef2f2-288">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="ef2f2-289">Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-289">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="ef2f2-290">Wählen Sie auf der Seite **Lokalisierungskonfigurationen** im Bereich **Zugehörige Links** die Option **Konfigurationsanbieter** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-290">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="ef2f2-291">Wählen Sie auf der Seite **Konfigurationsanbieter** die Option **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-291">On the **Configuration providers** page, select **New**.</span></span>
4. <span data-ttu-id="ef2f2-292">Geben Sie im Feld **Name** **Litware, Inc.** ein.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-292">In the **Name** field, enter **Litware, Inc.**</span></span>
5. <span data-ttu-id="ef2f2-293">Geben Sie im Feld **Internetadresse** `https://www.litware.com` ein.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-293">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
6. <span data-ttu-id="ef2f2-294">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-294">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a><span data-ttu-id="ef2f2-295">Aktivieren eines EB-Konfigurationsanbieters</span><span class="sxs-lookup"><span data-stu-id="ef2f2-295">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="ef2f2-296">Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-296">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="ef2f2-297">Wählen Sie auf der Seite **Lokalisierungskonfigurationen** im Bereich **Konfigurationsanbieter** die Kachel **Litware, Inc.** aus. Wählen Sie dann **Als aktiv festlegen** aus.</span><span class="sxs-lookup"><span data-stu-id="ef2f2-297">On the **Localization configurations** page, in the **Configuration providers** section, select the **Litware, Inc.** tile, and then select **Set active**.</span></span>

<span data-ttu-id="ef2f2-298">Weitere Informationen zu EB-Konfigurationsanbietern finden Sie unter [Erstellen von Konfigurationsanbietern und Markieren als aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="ef2f2-298">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ef2f2-299">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ef2f2-299">Additional resources</span></span>

- [<span data-ttu-id="ef2f2-300">Überblick über die elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="ef2f2-300">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="ef2f2-301">Überwachen der Ausführung von ER-Formaten zur Behebung von Leistungsproblemen</span><span class="sxs-lookup"><span data-stu-id="ef2f2-301">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)
- [<span data-ttu-id="ef2f2-302">Unterstützen parametrisierter Aufrufe von ER-Datenquellen des Typs „Berechnetes Feld“</span><span class="sxs-lookup"><span data-stu-id="ef2f2-302">Support parameterized calls of ER data sources of the Calculated field type</span></span>](er-calculated-field-type.md)
