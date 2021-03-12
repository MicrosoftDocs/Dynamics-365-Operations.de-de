---
title: Qualitätsprüfung
description: Dieses Thema enthält Informationen zur Qualitätsprüf+ungsfunktion. Mit dieser Funktion können Lagerarbeiter schnelle Stichproben der Qualität durchführen, während sie Artikel an der Eingangsrampe in Empfang nehmen.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSQualityCheckTemplate, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSQualityCheckResult
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 585ca933726cb932290f8abf8504aeb13848a0e5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996250"
---
# <a name="quality-check"></a><span data-ttu-id="bf52b-104">Qualitätsprüfung</span><span class="sxs-lookup"><span data-stu-id="bf52b-104">Quality check</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bf52b-105">Mit der Funktion *Qualitätsprüfung* können Lagerarbeiter schnelle Stichproben der Qualität durchführen, während sie Artikel an der Eingangsrampe in Empfang nehmen.</span><span class="sxs-lookup"><span data-stu-id="bf52b-105">The *Quality check* feature lets warehouse workers do quick spot checks for quality while they receive items to the inbound dock area.</span></span> <span data-ttu-id="bf52b-106">Diese Stichproben sind hilfreich, wenn Arbeiter Verpackungen oder andere leicht erkennbare Teile eines Artikels inspizieren.</span><span class="sxs-lookup"><span data-stu-id="bf52b-106">These spot checks are beneficial when workers inspect packaging or other easily recognizable parts of an item.</span></span> <span data-ttu-id="bf52b-107">Die Funktion hilft den Mitarbeitern, schnell zu überprüfen, ob etwas offensichtlich fehlerhaft oder beschädigt ist, bevor sie die Bestände an ihren Einlagerungslagerplatz lagern.</span><span class="sxs-lookup"><span data-stu-id="bf52b-107">The feature guides workers to take a quick look to see whether anything is obviously faulty or damaged before they stock the inventory in its putaway location.</span></span>

<span data-ttu-id="bf52b-108">Diese Funktion ist eine Alternative zum Standardverfahren zur Qualitätsprüfung.</span><span class="sxs-lookup"><span data-stu-id="bf52b-108">This feature is an alternative to the standard quality check process.</span></span> <span data-ttu-id="bf52b-109">Sie bietet mehr Flexibilität und eine schnellere Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="bf52b-109">It offers more flexibility and faster processing.</span></span>

<span data-ttu-id="bf52b-110">Wenn Sie diese Funktion verwenden, erfolgt die Wareneingangs- und Qualitätsprüfung wie folgt:</span><span class="sxs-lookup"><span data-stu-id="bf52b-110">When you use this feature, the arrival and quality check occur in the following way:</span></span>

1. <span data-ttu-id="bf52b-111">Wenn eine Lieferung eintrifft, zeichnet ein Lagerarbeiter den Wareneingang auf.</span><span class="sxs-lookup"><span data-stu-id="bf52b-111">When a shipment arrives, a warehouse worker registers the arrival.</span></span> <span data-ttu-id="bf52b-112">Der Arbeiter scannt auch einen Ladungsträger, um den Standort aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="bf52b-112">The worker also scans a license plate to register the location.</span></span>
1. <span data-ttu-id="bf52b-113">Der Mitarbeiter führt eine schnelle Qualitätsprüfung durch und zeichnet das Ergebnis (bestanden oder nicht bestanden) für diesen Ladungsträger auf.</span><span class="sxs-lookup"><span data-stu-id="bf52b-113">The worker does a quick quality check and records the result (pass or fail) for that license plate.</span></span>
1. <span data-ttu-id="bf52b-114">Eine der folgenden Aktionen erfolgt:</span><span class="sxs-lookup"><span data-stu-id="bf52b-114">One of the following actions occurs:</span></span>

    - <span data-ttu-id="bf52b-115">Wenn die Qualitätsprüfung bestanden ist, wird der Ladungsträger angenommen und wie gewohnt zu einem Empfangsort weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="bf52b-115">If the quality check is passed, the license plate is accepted and guided to a receiving location, as usual.</span></span>
    - <span data-ttu-id="bf52b-116">Wenn die Qualitätsprüfung nicht bestanden wird, wird der Ladungsträger abgelehnt und laufende Einlagerungsarbeiten werden zur weiteren Überprüfung an einen anderen Ort umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="bf52b-116">If the quality check is failed, the license plate is rejected, and existing putaway work for it is redirected to an alternate location for further inspection.</span></span> <span data-ttu-id="bf52b-117">Ein neuer Qualitätsprüfungsauftrag wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="bf52b-117">A new quality order is created.</span></span> <span data-ttu-id="bf52b-118">Um den Qualitätsprüfungsauftrag anzusehen, der aus der fehlgeschlagenen Qualitätsprüfung erstellt wurde, gehen Sie zu **Bestandsverwaltung \> Periodische Aufgaben \> Qualitätsmanagement \> Qualitätsprüfungsauftrag**.</span><span class="sxs-lookup"><span data-stu-id="bf52b-118">To view the quality order that is created from the failed quality check, go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>

<span data-ttu-id="bf52b-119">Dieser Vorgang kann auch so eingerichtet werden, dass alle gescannten Ladungsträger sofort an den Ort der Qualitätsprüfung umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="bf52b-119">This process can also be set up so that all scanned license plates are immediately diverted to the quality check location.</span></span>

## <a name="turn-on-the-quality-check-feature"></a><span data-ttu-id="bf52b-120">Die Qualitätsprüfungsfunktion aktivieren</span><span class="sxs-lookup"><span data-stu-id="bf52b-120">Turn on the Quality check feature</span></span>

<span data-ttu-id="bf52b-121">Bevor Sie die Funktion *Qualitätsprüfung* nutzen können, muss sie auf Ihrem System aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="bf52b-121">Before you can use the *Quality check* feature, it must be turned on in your system.</span></span> <span data-ttu-id="bf52b-122">Administratoren können mit den Einstellungen in der [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie gegebenenfalls aktivieren.</span><span class="sxs-lookup"><span data-stu-id="bf52b-122">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="bf52b-123">Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="bf52b-123">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="bf52b-124">**Module:** *Lagerortverwaltung*</span><span class="sxs-lookup"><span data-stu-id="bf52b-124">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="bf52b-125">**Funktionsname:** *Qualitätsprüfung*</span><span class="sxs-lookup"><span data-stu-id="bf52b-125">**Feature name:** *Quality check*</span></span>

## <a name="set-up-the-feature-for-the-example-scenario"></a><span data-ttu-id="bf52b-126">Funktion für das Beispielszenario einrichten</span><span class="sxs-lookup"><span data-stu-id="bf52b-126">Set up the feature for the example scenario</span></span>

<span data-ttu-id="bf52b-127">Dieser Abschnitt enthält Richtlinien und ein Beispiel, das zeigt, wie Sie die Funktion *Qualitätsprüfung* einrichten und Beispieldaten für das Beispielszenario vorbereiten, das später in diesem Thema bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="bf52b-127">This section provides guidelines and an example that shows how to set up the *Quality check* feature and prepare sample data for the example scenario that is provided later in this topic.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="bf52b-128">Beispieldaten zur Verfügung stellen</span><span class="sxs-lookup"><span data-stu-id="bf52b-128">Make sample data available</span></span>

<span data-ttu-id="bf52b-129">Um das [Beispielszenario](#example-scenario) mithilfe der Beispieldatensätze und -werte, die hier angegeben sind, zu verarbeiten, müssen Sie ein System verwenden, auf dem die standardmäßigen [Demodaten](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) installiert sind.</span><span class="sxs-lookup"><span data-stu-id="bf52b-129">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="bf52b-130">Außerdem müssen Sie die **USMF** juristische Person auswählen, bevor Sie beginnen.</span><span class="sxs-lookup"><span data-stu-id="bf52b-130">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="quality-check-template"></a><a name="quality-template"></a><span data-ttu-id="bf52b-131">Qualitätsprüfungsvorlage</span><span class="sxs-lookup"><span data-stu-id="bf52b-131">Quality check template</span></span>

<span data-ttu-id="bf52b-132">Die Qualitätsprüfungsvorlage legt die Regeln für die schnelle Stichprobenprüfung der Qualität beim Wareneingang fest.</span><span class="sxs-lookup"><span data-stu-id="bf52b-132">The quality check template defines the rules for doing quick spot checks for quality at the time of receiving.</span></span>

1. <span data-ttu-id="bf52b-133">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Qualitätprüfungsvorlage**.</span><span class="sxs-lookup"><span data-stu-id="bf52b-133">Go to **Warehouse management \> Setup \> Work \> Quality check template**.</span></span>
1. <span data-ttu-id="bf52b-134">Wählen Sie **Neu** aus, um dem Raster eine Vorlage hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="bf52b-134">Select **New** to add a template to the grid.</span></span>
1. <span data-ttu-id="bf52b-135">Legen Sie für die neue Vorlage die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="bf52b-135">Set the following values to define the new template:</span></span>

    - <span data-ttu-id="bf52b-136">**Name der Qualitätsprüfungsvorlage:** *Eingangsrampenprüfung*</span><span class="sxs-lookup"><span data-stu-id="bf52b-136">**Quality check template name:** *Dock check*</span></span>

        <span data-ttu-id="bf52b-137">Geben Sie einen Namen ein, der die für diese Vorlage geltenden Richtlinien angibt.</span><span class="sxs-lookup"><span data-stu-id="bf52b-137">Enter a name that identifies the policies applied for this template.</span></span>

    - <span data-ttu-id="bf52b-138">**Annahmerichtlinie:** *Benutzer auffordern*</span><span class="sxs-lookup"><span data-stu-id="bf52b-138">**Acceptance policy:** *Prompt user*</span></span>

        <span data-ttu-id="bf52b-139">+Geben Sie an, ob Benutzer aufgefordert werden sollen, die Qualität des Bestands während der Erledigung der Arbeit anzunehmen oder abzulehnen oder ob die Qualität automatisch abgelehnt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bf52b-139">Specify whether users should be prompted to accept or reject the quality of the inventory while they process the work, or whether the quality should automatically be rejected.</span></span> <span data-ttu-id="bf52b-140">Die verfügbaren Optionen sind *Automatisch ablehnen* und *Benutzer auffordern*.</span><span class="sxs-lookup"><span data-stu-id="bf52b-140">The available options are *Auto reject* and *Prompt user*.</span></span>

    - <span data-ttu-id="bf52b-141">**Qualitätsverarbeitungspolitik:** *Qualitätsprüfungsauftrag erstellen*</span><span class="sxs-lookup"><span data-stu-id="bf52b-141">**Quality processing policy:** *Create quality order*</span></span>

        <span data-ttu-id="bf52b-142">Wählen Sie die Richtlinie aus, die verwendet werden soll, wenn die Bestandsqualität abgelehnt wurde.</span><span class="sxs-lookup"><span data-stu-id="bf52b-142">Select the policy that should be used when the quality of the inventory is rejected.</span></span> <span data-ttu-id="bf52b-143">Die folgenden Optionen stehen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="bf52b-143">The following options are available:</span></span>

        - <span data-ttu-id="bf52b-144">*Nur Arbeit erstellen*: Erstellen Sie nur die Arbeit, um die Bestandsumlagerung zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="bf52b-144">*Create work only* – Just create work to facilitate inventory movement.</span></span>
        - <span data-ttu-id="bf52b-145">*Qualitätsprüfungsauftrag erstellen*: Erstellen Sie einen Qualitätsprüfungsauftrag, um Qualitätstests zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="bf52b-145">*Create quality order* – Create a quality order to facilitate quality tests.</span></span>

    - <span data-ttu-id="bf52b-146">**Testgruppe:** *Anlage*</span><span class="sxs-lookup"><span data-stu-id="bf52b-146">**Test group:** *Enclosure*</span></span>

        <span data-ttu-id="bf52b-147">Geben Sie die Testgruppe an, die in dem erstellten Qualitätsprüfungsauftrag verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bf52b-147">Specify the test group that should be used in the quality order that is created.</span></span> <span data-ttu-id="bf52b-148">Testgruppen werden im Modul **Bestandsverwaltung** eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="bf52b-148">Test groups are set up in the **Inventory management** module.</span></span>

        <span data-ttu-id="bf52b-149">Lassen Sie die Option **Zerstörungstest** für die Testgruppe deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="bf52b-149">Leave the **Destructive text** option turned off for the test group.</span></span> <span data-ttu-id="bf52b-150">Diese Option legt fest, ob das Muster im Rahmen der Tests in der Testgruppe zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="bf52b-150">This option defines whether the sample will be destroyed as part of the tests in the test group.</span></span> <span data-ttu-id="bf52b-151">Wird ein Zerstörungstest verwendet, generiert das System beim Erstellen eines Qualitätsprüfungsauftrags für einen Artikel eine Lagerbuchung.</span><span class="sxs-lookup"><span data-stu-id="bf52b-151">If a destructive test is used, the system generates an inventory transaction when a quality order is created for an item.</span></span> <span data-ttu-id="bf52b-152">Mit der neuen Lagerbuchung wird die Bestandsverringerung für die Testmenge antizipiert.</span><span class="sxs-lookup"><span data-stu-id="bf52b-152">The new inventory transaction predicts the inventory reduction for the test quantity.</span></span> <span data-ttu-id="bf52b-153">Die Bestandsverringerung wird durchgeführt, wenn der Qualitätsprüfungsauftrag durch den Überprüfungsschritt abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="bf52b-153">The inventory reduction occurs when the quality order is completed through the validation step.</span></span> <span data-ttu-id="bf52b-154">Die Lagerbuchung wird als Qualitätsprüfungsauftrag gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bf52b-154">The inventory transaction is identified as a quality order.</span></span>

### <a name="work-class--quality-check"></a><a name="work-class"></a><span data-ttu-id="bf52b-155">Arbeitsklasse – Qualitätsprüfung</span><span class="sxs-lookup"><span data-stu-id="bf52b-155">Work class – Quality check</span></span>

<span data-ttu-id="bf52b-156">Arbeitsklassen werden verwendet, um den Typ der Arbeitsauftragspositionen zuzuweisen und/oder einzuschränken, die Lagerarbeiter auf einem mobilen Gerät verarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="bf52b-156">Work classes are used to direct and/or limit the type of work order lines that warehouse workers can process on a mobile device.</span></span>

1. <span data-ttu-id="bf52b-157">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsklassen**.</span><span class="sxs-lookup"><span data-stu-id="bf52b-157">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="bf52b-158">Wählen Sie **Neu** aus, um eine Arbeitsklasse zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="bf52b-158">Select **New** to create a work class.</span></span>
1. <span data-ttu-id="bf52b-159">Legen Sie im Header die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="bf52b-159">In the header, set the following values:</span></span>

    - <span data-ttu-id="bf52b-160">**Arbeitsklassen-ID:** *QC-Prüfung*</span><span class="sxs-lookup"><span data-stu-id="bf52b-160">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="bf52b-161">Geben Sie den Namen für die Arbeitsklasse ein.</span><span class="sxs-lookup"><span data-stu-id="bf52b-161">Enter a name that identifies the work class.</span></span>

    - <span data-ttu-id="bf52b-162">**Beschreibung:** *QC-Prüfung*</span><span class="sxs-lookup"><span data-stu-id="bf52b-162">**Description:** *QC Check*</span></span>

        <span data-ttu-id="bf52b-163">Geben Sie eine kurze Beschreibung ein, die angibt, wofür die Arbeitsklasse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bf52b-163">Enter a short description that indicates what the work class is used for.</span></span>

    - <span data-ttu-id="bf52b-164">**Arbeitsauftragstyp:** *Qualität in der Qualitätsprüfung*</span><span class="sxs-lookup"><span data-stu-id="bf52b-164">**Work order type:** *Quality in quality check*</span></span>

        <span data-ttu-id="bf52b-165">Wählen Sie den Typ des Arbeitsauftrags aus, der mit der Arbeitsklasse erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="bf52b-165">Select the type of work order that is created by the work class.</span></span> <span data-ttu-id="bf52b-166">Wenn Sie Qualitätskontrollarbeiten einrichten, wählen Sie immer *Qualität in der Qualitätsprüfung*.</span><span class="sxs-lookup"><span data-stu-id="bf52b-166">When you set up quality control work, always select *Quality in quality check*.</span></span>

1. <span data-ttu-id="bf52b-167">Im Inforegister **Gültige Einlagerungsorttypen** lassen Sie das Feld **Lagerplatztyp** leer.</span><span class="sxs-lookup"><span data-stu-id="bf52b-167">On the **Valid put location types** FastTab, leave the **Location type** field blank.</span></span>

    <span data-ttu-id="bf52b-168">Wenn Sie einen Lagerplatztyp auswählen, begrenzen Sie die Lagerorte, an denen Artikel nach der Entnahme abgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="bf52b-168">If you select a location type, you limit the locations where items can be put after they are picked.</span></span> <span data-ttu-id="bf52b-169">Dieses Feld wird verwendet, wenn eine Lagerplatzrichtlinie versucht, den Lagerplatz aufzulösen oder ein Lagerarbeiter manuell den Speicherort für die Menüoption des mobilen Geräts festlegt.</span><span class="sxs-lookup"><span data-stu-id="bf52b-169">This field is used when a location directive tries to resolve the location, or when a warehouse worker manually specifies the location for the mobile device menu item.</span></span>

<span data-ttu-id="bf52b-170">Weitere Informationen zu Arbeitsklassen und deren Erstellung finden Sie unter [Eine Arbeitsklasse erstellen](tasks/create-work-class.md).</span><span class="sxs-lookup"><span data-stu-id="bf52b-170">For more information about work classes and how to create them, see [Create a work class](tasks/create-work-class.md).</span></span>

### <a name="work-template"></a><span data-ttu-id="bf52b-171">Arbeitsvorlage</span><span class="sxs-lookup"><span data-stu-id="bf52b-171">Work template</span></span>

<span data-ttu-id="bf52b-172">Mithilfe von Arbeitsvorlagen können Sie die Arbeitsvorgänge definieren, die am Lagerplatz ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="bf52b-172">Work templates let you define the work operations that must be performed in the warehouse.</span></span> <span data-ttu-id="bf52b-173">In der Regel bestehen Lagerplatzarbeitsabläufe aus folgenden Aktivitäten: Ein Lagerarbeiter entnimmt verfügbaren Lagerbestand an einem Lagerplatz und legt anschließend den entnommenen Bestand an einem anderen Lagerplatz ab.</span><span class="sxs-lookup"><span data-stu-id="bf52b-173">Typically, warehouse work operations consist of a pair of actions: a warehouse worker picks on-hand inventory up in one location and then puts the picked inventory down in another location.</span></span> <span data-ttu-id="bf52b-174">Eine Arbeitsvorlage für die Qualitätskontrolle legt die Arbeitsabläufe für Qualitätsprüfungen fest.</span><span class="sxs-lookup"><span data-stu-id="bf52b-174">A work template for quality control defines the work operations for doing quality checks.</span></span>

#### <a name="purchase-orders"></a><span data-ttu-id="bf52b-175">Bestellungen</span><span class="sxs-lookup"><span data-stu-id="bf52b-175">Purchase orders</span></span>

1. <span data-ttu-id="bf52b-176">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="bf52b-176">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="bf52b-177">Wählen Sie in der Kopfzeile **Arbeitsauftragstyp** die Option *Bestellungen* aus.</span><span class="sxs-lookup"><span data-stu-id="bf52b-177">In the header, set the **Work order type** field to *Purchase orders*.</span></span>
1. <span data-ttu-id="bf52b-178">Wählen Sie im Aktionsbereich **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="bf52b-178">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="bf52b-179">Wählen Sie eine Arbeitsvorlage aus, die einen Qualitätsprüfungsschritt enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="bf52b-179">Select a work template that should include a quality check step.</span></span> <span data-ttu-id="bf52b-180">Wählen Sie im Abschnitt **Übersicht** im Feld **Arbeitsvorlage** *51 PO-Eingang* aus.</span><span class="sxs-lookup"><span data-stu-id="bf52b-180">In the **Overview** section, in the **Work template** field, select *51 PO Receipt*.</span></span>
1. <span data-ttu-id="bf52b-181">Im Abschnitt **Arbeitsvorlagendetails** hat das im Raster zwei Positionen: eine für *Entnahme* und eine für *Einlagerung*.</span><span class="sxs-lookup"><span data-stu-id="bf52b-181">In the **Work template details** section, notice that the grid has two existing lines: one for *Pick* and one for *Put*.</span></span>
1. <span data-ttu-id="bf52b-182">Wählen Sie im Abschnitt **Arbeitsvorlagendetails** **Neu** aus, um dem Raster einer Zeile zur Qualitätskontrolle hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="bf52b-182">In the **Work template details** section, select **New** to add a row for quality control to the grid.</span></span> <span data-ttu-id="bf52b-183">Beachten Sie, dass das Feld **Positionsnummer** für die neue Zeile auf *3* gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="bf52b-183">Notice that the **Line number** field for the new line is set to *3*.</span></span>
1. <span data-ttu-id="bf52b-184">Legen Sie die folgenden Werte für die neue Position fest.</span><span class="sxs-lookup"><span data-stu-id="bf52b-184">On the new line, set the following values.</span></span> <span data-ttu-id="bf52b-185">Übernehmen Sie für alle verbleibenden Felder die Standardwerte.</span><span class="sxs-lookup"><span data-stu-id="bf52b-185">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="bf52b-186">**Arbeitstyp:** *Qualitätsprüfung*</span><span class="sxs-lookup"><span data-stu-id="bf52b-186">**Work type:** *Quality check*</span></span>
    - <span data-ttu-id="bf52b-187">**Arbeitsklassen-ID:** *Kauf*</span><span class="sxs-lookup"><span data-stu-id="bf52b-187">**Work class ID:** *Purchase*</span></span>
    - <span data-ttu-id="bf52b-188">**Name der Qualitätsprüfungsvorlage:** *Eingangsrampenprüfung*</span><span class="sxs-lookup"><span data-stu-id="bf52b-188">**Quality check template name:** *Dock check*</span></span>

        <span data-ttu-id="bf52b-189">Wählen Sie die eindeutige Kennung für die Arbeitsklasse aus.</span><span class="sxs-lookup"><span data-stu-id="bf52b-189">Select the unique ID for the work class.</span></span> <span data-ttu-id="bf52b-190">Sie verwenden diesen Wert, um die Menüoptionen im mobilen Gerät und die Typen der Arbeit, die diese Menüoptionen verarbeiten können, zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="bf52b-190">You use this value to configure the menu items on the mobile device and the types of work that those menu items can process.</span></span>

1. <span data-ttu-id="bf52b-191">Wählen Sie im Aktionsbereich **Speichern**, um Ihre bisherige Arbeit zu speichern.</span><span class="sxs-lookup"><span data-stu-id="bf52b-191">On the Action Pane, select **Save** to save your work so far.</span></span>

    <span data-ttu-id="bf52b-192">Sie erhalten eine Informationsmeldung mit dem Titel „Ungültig – Qualitätsprüfung muss direkt nach einer Entnahme erfolgen“.</span><span class="sxs-lookup"><span data-stu-id="bf52b-192">You receive an informational message that states, "Invalid - Quality check must come directly after a pick."</span></span> <span data-ttu-id="bf52b-193">Daher müssen Sie die **Positionsnummer** für die gerade hinzugefügte Position ändern.</span><span class="sxs-lookup"><span data-stu-id="bf52b-193">Therefore, you must change the **Line number** value for the line that you just added.</span></span>

1. <span data-ttu-id="bf52b-194">Ändern Sie den Wert der **Positionsnummer** für die neue Position wie folgt:</span><span class="sxs-lookup"><span data-stu-id="bf52b-194">Follow these steps to change the **Line number** value for the new line:</span></span>

    1. <span data-ttu-id="bf52b-195">Im Bereich **Arbeitsvorlagendetails** wählen sie die Position aus, in der das Feld **Arbeitstyp** auf *Qualitätsprüfung* gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="bf52b-195">In the **Work template details** section, select the line where the **Work type** field is set to *Quality check*.</span></span>
    2. <span data-ttu-id="bf52b-196">Nutzen Sie die Schaltfläche **Nach oben** oder **Nach unten**, um die Position *Qualitätsprüfung* hinter die Position *Entnahme* zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="bf52b-196">Select the **Move up** or **Move down** button to move the *Quality check* line so that it's after the *Pick* line.</span></span>

1. <span data-ttu-id="bf52b-197">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="bf52b-197">On the Action Pane, select **Save**.</span></span>

#### <a name="quality-in-quality-check"></a><span data-ttu-id="bf52b-198">Qualität in Qualitätsprüfung</span><span class="sxs-lookup"><span data-stu-id="bf52b-198">Quality in quality check</span></span>

<span data-ttu-id="bf52b-199">Erstellen Sie als Nächstes eine Arbeitsvorlage für die Qualitätsprüfung.</span><span class="sxs-lookup"><span data-stu-id="bf52b-199">Next, create a work template for the quality check.</span></span>

1. <span data-ttu-id="bf52b-200">Ändern Sie in der Kopfzeile der Seite **Arbeitsvorlagen** den Wert des Felds **Arbeitsauftragstyp** auf *Qualität in der Qualitätsprüfung*.</span><span class="sxs-lookup"><span data-stu-id="bf52b-200">In the header of the **Work templates** page, change the value of the **Work order type** field to *Quality in quality check*.</span></span>
1. <span data-ttu-id="bf52b-201">Wählen Sie im Aktivitätsbereich **Neu** aus, um dem Raster im Bereich **Übersicht** eine Zeile hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="bf52b-201">On the Action Pane, select **New** to add a row to the grid in the **Overview** section.</span></span>
1. <span data-ttu-id="bf52b-202">Legen Sie in der neuen Zeile die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="bf52b-202">In the new row, set the following values:</span></span>

    - <span data-ttu-id="bf52b-203">**Arbeitsvorlage:** *51 Qualitätsprüfung*</span><span class="sxs-lookup"><span data-stu-id="bf52b-203">**Work template:** *51 Quality Check*</span></span>

        <span data-ttu-id="bf52b-204">Geben Sie einen Namen für die Vorlage ein.</span><span class="sxs-lookup"><span data-stu-id="bf52b-204">Enter a name for the template.</span></span>

    - <span data-ttu-id="bf52b-205">**Arbeitsvorlagenbeschreibung:** *51 Qualitätsprüfung*</span><span class="sxs-lookup"><span data-stu-id="bf52b-205">**Work template description:** *51 Quality Check*</span></span>

1. <span data-ttu-id="bf52b-206">Wählen Sie im Aktionsbereich **Speichern** aus, um den Abschnitt **Arbeitsvorlagendetails** verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="bf52b-206">On the Action Pane, select **Save** to make the **Work template details** section available.</span></span>
1. <span data-ttu-id="bf52b-207">Während die neue Vorlage noch im Abschnitt **Übersicht** ausgewählt ist, wählen Sie **Neu** im Abschnitt **Arbeitsvorlagendetails**, um dort eine Zeile zum Raster hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="bf52b-207">While the new template is still selected in the **Overview** section, select **New** in the **Work template details** section to add a row to the grid there.</span></span>
1. <span data-ttu-id="bf52b-208">Legen Sie in der neuen Zeile die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="bf52b-208">In the new row, set the following values:</span></span>

    - <span data-ttu-id="bf52b-209">**Arbeitstyp:** *Entnahme*</span><span class="sxs-lookup"><span data-stu-id="bf52b-209">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="bf52b-210">**Arbeitsklassen-ID:** *QC-Prüfung*</span><span class="sxs-lookup"><span data-stu-id="bf52b-210">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="bf52b-211">Wählen Sie den Namen der [Arbeiterklasse](#work-class) aus, die Sie zuvor für die Qualitätskontrolle erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="bf52b-211">Select the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

1. <span data-ttu-id="bf52b-212">In dem Abschnitt **Arbeitsvorlagendetails** wählen Sie wieder **Neu**, um eine weitere Zeile hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="bf52b-212">In the **Work template details** section, select **New** again to add another row.</span></span>
1. <span data-ttu-id="bf52b-213">Legen Sie in der neuen Zeile die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="bf52b-213">In the new row, set the following values:</span></span>

    - <span data-ttu-id="bf52b-214">**Arbeitstyp:** *Einlagern*</span><span class="sxs-lookup"><span data-stu-id="bf52b-214">**Work type:** *Put*</span></span>
    - <span data-ttu-id="bf52b-215">**Arbeitsklassen-ID:** *QC-Prüfung*</span><span class="sxs-lookup"><span data-stu-id="bf52b-215">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="bf52b-216">Wählen Sie den Namen der [Arbeiterklasse](#work-class) aus, die Sie zuvor für die Qualitätskontrolle erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="bf52b-216">Select the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

1. <span data-ttu-id="bf52b-217">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="bf52b-217">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="bf52b-218">Weitere Informationen zu Arbeitsvorlagen, finden Sie unter [Steuern von Lagerarbeit mithilfe von Arbeitsvorlagen und Lagerplatzrichtlinien](control-warehouse-location-directives.md)</span><span class="sxs-lookup"><span data-stu-id="bf52b-218">For more information about work templates, see [Control warehouse work by using work templates and location directives](control-warehouse-location-directives.md)</span></span>

### <a name="location-directive--quality-failures"></a><span data-ttu-id="bf52b-219">Lagerplatzrichtlinie – Qualitätsmängel</span><span class="sxs-lookup"><span data-stu-id="bf52b-219">Location directive – Quality failures</span></span>

<span data-ttu-id="bf52b-220">Lagerplatzrichtlinien sind Regeln, die dabei helfen, Entnahme- und Einlagerungslagerorte für die Lagerumlagerung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="bf52b-220">Location directives are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="bf52b-221">In einer Auftragsbuchung bestimmt eine Lagerplatzrichtlinie z. B., wo die Artikel entnommen und wo die entnommenen Artikel eingelagert werden.</span><span class="sxs-lookup"><span data-stu-id="bf52b-221">For example, in a sales order transaction, a location directive determines where the items will be picked and where the picked items will be put.</span></span> <span data-ttu-id="bf52b-222">Sie müssen eine Lagerplatzrichtlinienregel konfigurieren, um zu definieren, wie fehlgeschlagene Qualitätsprüfungen behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="bf52b-222">You must configure a location directive rule to define how failed quality checks will be handled.</span></span>

1. <span data-ttu-id="bf52b-223">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerplatzrichtlinien**.</span><span class="sxs-lookup"><span data-stu-id="bf52b-223">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="bf52b-224">Stellen Sie im linken Bereich das Feld **Arbeitsauftragstyp** auf *Bestellungen*, um mit Lagerplatzrichtlinien dieses Typs zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="bf52b-224">In the left pane, set the **Work order type** field to *Purchase orders* to work with location directives of that type.</span></span>
1. <span data-ttu-id="bf52b-225">Wählen Sie im Aktivitätsbereich die Option **Neu** aus, um eine Lagerplatzrichtlinie für Qualitätsprüfungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="bf52b-225">On the Action Pane, select **New** to create a location directive for quality checks.</span></span>
1. <span data-ttu-id="bf52b-226">Legen Sie im Header die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="bf52b-226">In the header, set the following values:</span></span>

    - <span data-ttu-id="bf52b-227">**Sequenznummer:** Akzeptieren Sie den Standardwert.</span><span class="sxs-lookup"><span data-stu-id="bf52b-227">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="bf52b-228">**Name:** *51 zu Qualität*</span><span class="sxs-lookup"><span data-stu-id="bf52b-228">**Name:** *51 To Quality*</span></span>

1. <span data-ttu-id="bf52b-229">Legen Sie im Inforegister **Lagerplatzrichtlinien** die folgenden Werte fest.</span><span class="sxs-lookup"><span data-stu-id="bf52b-229">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="bf52b-230">Übernehmen Sie für alle verbleibenden Felder die Standardwerte.</span><span class="sxs-lookup"><span data-stu-id="bf52b-230">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="bf52b-231">**Arbeitstyp:** *Einlagern*</span><span class="sxs-lookup"><span data-stu-id="bf52b-231">**Work type:** *Put*</span></span>
    - <span data-ttu-id="bf52b-232">**Standort:** *5*</span><span class="sxs-lookup"><span data-stu-id="bf52b-232">**Site:** *5*</span></span>
    - <span data-ttu-id="bf52b-233">**Lagerort:** *51*</span><span class="sxs-lookup"><span data-stu-id="bf52b-233">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="bf52b-234">Wählen Sie im Aktionsbereich **Speichern** aus, um Ihre Richtlinie zu speichern und das Inforegister **Positionen** verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="bf52b-234">On the Action Pane select **Save** to save your directive and make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="bf52b-235">Wählen Sie im Inforegister **Positionen** die Option **Neu** aus, um dem Raster eine Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="bf52b-235">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="bf52b-236">Legen Sie die folgenden Werte für die neue Position fest.</span><span class="sxs-lookup"><span data-stu-id="bf52b-236">On the new line, set the following values.</span></span> <span data-ttu-id="bf52b-237">Übernehmen Sie für alle verbleibenden Felder die Standardwerte.</span><span class="sxs-lookup"><span data-stu-id="bf52b-237">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="bf52b-238">**Von Menge:** *1*</span><span class="sxs-lookup"><span data-stu-id="bf52b-238">**From quantity:** *1*</span></span>
    - <span data-ttu-id="bf52b-239">**Bis Menge:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="bf52b-239">**To quantity:** *1000000*</span></span>

1. <span data-ttu-id="bf52b-240">Wählen Sie im Aktionsbereich **Speichern** aus, um die neue Position zu speichern und das Inforegister **Lagerplatzrichtlinienaktivitäten** verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="bf52b-240">On the Action Pane, select **Save** to save the new line and make the **Location directive actions** FastTab available.</span></span>
1. <span data-ttu-id="bf52b-241">Während die neue Position noch im Inforegister **Positionen** ausgewählt ist, gehen Sie auf **Neu** im Inforegister **Lagerplatzrichtlinienaktivitäten**, um dort eine Zeile zum Raster hinzuzufügen, damit Sie eine Aktion für die Position festlegen können.</span><span class="sxs-lookup"><span data-stu-id="bf52b-241">While the new line is still selected on the **Lines** FastTab, select **New** on the **Location directive actions** FastTab to add a row to the grid there, so that you can set up an action for the line.</span></span>
1. <span data-ttu-id="bf52b-242">Stellen Sie in der neuen Zeile das Feld **Name** auf *Qualität*.</span><span class="sxs-lookup"><span data-stu-id="bf52b-242">In the new row, set the **Name** field to *Quality*.</span></span> <span data-ttu-id="bf52b-243">Übernehmen Sie für alle verbleibenden Felder die Standardwerte.</span><span class="sxs-lookup"><span data-stu-id="bf52b-243">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="bf52b-244">Wählen Sie im Aktionsbereich **Speichern** aus, um die Schaltfläche **Abfrage bearbeiten** im Inforegister **Lagerplatzrichtlinienaktivitäten** verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="bf52b-244">On the Action Pane, select **Save** to make the **Edit query** button on the **Location directive actions** FastTab available.</span></span>
1. <span data-ttu-id="bf52b-245">Während die gerade hinzugefügte Position im Inforegister **Lagerplatzrichtlinienaktivitäten** noch ausgewählt ist, gehen Sie auf **Abfrage bearbeiten**, um ein Dialogfeld zu öffnen, in dem Sie die Abfrage für die Aktion bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="bf52b-245">While the line that you just added is still selected on the **Location directive actions** FastTab, select **Edit query** to open a dialog box where you can edit the query for the action.</span></span>
1. <span data-ttu-id="bf52b-246">Wählen Sie auf der Registerkarte **Bereich** die Option **Hinzufügen** aus, um dem Raster eine Abfrage hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="bf52b-246">On the **Range** tab, select **Add** to add a row to the query.</span></span>
1. <span data-ttu-id="bf52b-247">Legen Sie in der neuen Zeile die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="bf52b-247">In the new row, set the following values:</span></span>

    - <span data-ttu-id="bf52b-248">**Tabelle:** *Lagerorte*</span><span class="sxs-lookup"><span data-stu-id="bf52b-248">**Table:** *Locations*</span></span>
    - <span data-ttu-id="bf52b-249">**Abgeleitete Tabelle:** *Lagerorte*</span><span class="sxs-lookup"><span data-stu-id="bf52b-249">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="bf52b-250">**Feld:** *Lagerplatz*</span><span class="sxs-lookup"><span data-stu-id="bf52b-250">**Field:** *Location*</span></span>
    - <span data-ttu-id="bf52b-251">**Kriterien:** *QMS*</span><span class="sxs-lookup"><span data-stu-id="bf52b-251">**Criteria:** *QMS*</span></span>

    <span data-ttu-id="bf52b-252">Der *QMS*-Lagerplatz ist ein Lagerort für die Qualität.</span><span class="sxs-lookup"><span data-stu-id="bf52b-252">The *QMS* location is a warehouse location for quality.</span></span>

1. <span data-ttu-id="bf52b-253">Klicken Sie auf **OK**, um das Dialogfeld zu schließen.</span><span class="sxs-lookup"><span data-stu-id="bf52b-253">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="bf52b-254">Jetzt müssen Sie die Reihenfolge der vorhandenen Bestellungs-Lagerplatzrichtlinien für Lagerort *51* ändern.</span><span class="sxs-lookup"><span data-stu-id="bf52b-254">You must now change the sequence of purchase order location directives for warehouse *51*.</span></span> <span data-ttu-id="bf52b-255">Speichern Sie die neue Lagerplatzrichtlinie *51 zu Qualität* aus, aktualisieren Sie die Seite und wählen Sie die Lagerplatzrichtlinie in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="bf52b-255">Save the new *51 To Quality* location directive, refresh the page, and select the location directive in the list.</span></span> <span data-ttu-id="bf52b-256">Benutzen Sie dann die Schaltflächen **Nach oben** und **Nach unten** im Aktionsbereich, um die Lagerplatzrichtlinie für Lagerort *51* in der folgenden Reihenfolge festzulegen.</span><span class="sxs-lookup"><span data-stu-id="bf52b-256">Then use the **Move up** and **Move down** buttons on the Action Pane to put the location directive for warehouse *51* in the following order.</span></span> <span data-ttu-id="bf52b-257">(Bevor Sie **Nach oben** oder **Nach unten** wählen, müssen Sie eine Lagerplatzrichtlinie in der Liste auswählen.)</span><span class="sxs-lookup"><span data-stu-id="bf52b-257">(Before you select **Move up** or **Move down**, you must select a location directive in the list.)</span></span>

    1. <span data-ttu-id="bf52b-258">51 zu Qualität</span><span class="sxs-lookup"><span data-stu-id="bf52b-258">51 To Quality</span></span>
    2. <span data-ttu-id="bf52b-259">51 PO direkt</span><span class="sxs-lookup"><span data-stu-id="bf52b-259">51 PO Direct</span></span>
    3. <span data-ttu-id="bf52b-260">51 QMS</span><span class="sxs-lookup"><span data-stu-id="bf52b-260">51 QMS</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="bf52b-261">Menüelemente des mobilen Geräts</span><span class="sxs-lookup"><span data-stu-id="bf52b-261">Mobile device menu items</span></span>

<span data-ttu-id="bf52b-262">Konfigurieren Sie ein Menüelement, damit mobile Geräte die Funktion **Qualitätsprüfung** ausführen können.</span><span class="sxs-lookup"><span data-stu-id="bf52b-262">Configure a menu item so that mobile devices can perform the **Quality Check** function.</span></span>

#### <a name="purchase-putaway"></a><span data-ttu-id="bf52b-263">Kauf einlagern</span><span class="sxs-lookup"><span data-stu-id="bf52b-263">Purchase putaway</span></span>

1. <span data-ttu-id="bf52b-264">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.</span><span class="sxs-lookup"><span data-stu-id="bf52b-264">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="bf52b-265">Wählen Sie aus der Liste das Menüelement **Kauf einlagern** aus.</span><span class="sxs-lookup"><span data-stu-id="bf52b-265">In the list, select the **Purchase put-away** menu item.</span></span>
1. <span data-ttu-id="bf52b-266">Wählen Sie im Aktionsbereich **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="bf52b-266">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="bf52b-267">Wählen Sie im Bereich **Arbeitsklassen** die Option **Neu** aus, um dem Raster eine Zeile hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="bf52b-267">In the **Work classes** section, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="bf52b-268">Legen Sie in der neuen Zeile die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="bf52b-268">In the new row, set the following values:</span></span>

    - <span data-ttu-id="bf52b-269">**Arbeitsklassen-ID:** *QC-Prüfung*</span><span class="sxs-lookup"><span data-stu-id="bf52b-269">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="bf52b-270">Geben Sie den Namen der [Arbeiterklasse](#work-class) ein, die Sie zuvor für die Qualitätskontrolle erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="bf52b-270">Enter the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

    - <span data-ttu-id="bf52b-271">**Arbeitsauftragstyp:** *Qualität in der Qualitätsprüfung*</span><span class="sxs-lookup"><span data-stu-id="bf52b-271">**Work order type:** *Quality in quality check*</span></span>

1. <span data-ttu-id="bf52b-272">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="bf52b-272">On the Action Pane, select **Save**.</span></span>

#### <a name="purchase-order-line-receiving"></a><span data-ttu-id="bf52b-273">Bestellposition – Empfang</span><span class="sxs-lookup"><span data-stu-id="bf52b-273">Purchase order line receiving</span></span>

1. <span data-ttu-id="bf52b-274">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.</span><span class="sxs-lookup"><span data-stu-id="bf52b-274">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="bf52b-275">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="bf52b-275">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="bf52b-276">Legen Sie im Header die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="bf52b-276">In the header, set the following values:</span></span>

    - <span data-ttu-id="bf52b-277">**Name des Menüpunkts:** *PO-Positionsempfang*</span><span class="sxs-lookup"><span data-stu-id="bf52b-277">**Menu item name:** *PO line receiving*</span></span>
    - <span data-ttu-id="bf52b-278">**Titel:** *PO-Positionsempfang*</span><span class="sxs-lookup"><span data-stu-id="bf52b-278">**Title:** *PO line receiving*</span></span>
    - <span data-ttu-id="bf52b-279">**Modus:** *Arbeit*</span><span class="sxs-lookup"><span data-stu-id="bf52b-279">**Mode:** *Work*</span></span>
    - <span data-ttu-id="bf52b-280">**Vorhandene Arbeit verwenden:** *Nein*</span><span class="sxs-lookup"><span data-stu-id="bf52b-280">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="bf52b-281">Legen Sie im Inforegister **Allgemein** die folgenden Werte fest.</span><span class="sxs-lookup"><span data-stu-id="bf52b-281">On the **General** FastTab, set the following values.</span></span> <span data-ttu-id="bf52b-282">Übernehmen Sie für alle verbleibenden Felder die Standardwerte.</span><span class="sxs-lookup"><span data-stu-id="bf52b-282">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="bf52b-283">**Arbeitserstellungsprozess:** *Bestellungspositionsempfang und Einlagerung*</span><span class="sxs-lookup"><span data-stu-id="bf52b-283">**Work creation process:** *Purchase order line receiving and put away*</span></span>
    - <span data-ttu-id="bf52b-284">**Kennzeichen generieren:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="bf52b-284">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="bf52b-285">**Arbeitsvorlage:** *51 PO-Eingang*</span><span class="sxs-lookup"><span data-stu-id="bf52b-285">**Work template:** *51 PO Receipt*</span></span>

1. <span data-ttu-id="bf52b-286">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="bf52b-286">On the Action Pane, select **Save**.</span></span>

#### <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="bf52b-287">Hinzufügen der Menüoption zu einem mobilen Gerät</span><span class="sxs-lookup"><span data-stu-id="bf52b-287">Add the menu item to a mobile device menu</span></span>

1. <span data-ttu-id="bf52b-288">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menü für mobiles Gerät**.</span><span class="sxs-lookup"><span data-stu-id="bf52b-288">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="bf52b-289">Wählen Sie im linken Bereich das Menü **Eingehend** aus.</span><span class="sxs-lookup"><span data-stu-id="bf52b-289">In the left pane, select the **Inbound** menu.</span></span>
1. <span data-ttu-id="bf52b-290">Wählen Sie im Aktionsbereich **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="bf52b-290">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="bf52b-291">Wählen Sie in der Liste **Verfügbare Menüs und Menüelemente** das Menüelement **PO-Positionseingang** aus.</span><span class="sxs-lookup"><span data-stu-id="bf52b-291">In the **Available menus and menu items** column, select the new **PO line receiving** menu item.</span></span>
1. <span data-ttu-id="bf52b-292">Wählen Sie die rechte Pfeiltaste, um **PO-Positionseingang** zur Spalte **Menüstruktur** zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="bf52b-292">Select the right arrow button to move **PO line receiving** to the **Menu structure** column.</span></span>
1. <span data-ttu-id="bf52b-293">In der Spalte **Menüstruktur** wählen Sie **PO-Positionseingang** und verschieben das Menüelement dann mit den Nach-oben- und Nach-unten-Tasten an die gewünschte Position im Menü des mobilen Geräts.</span><span class="sxs-lookup"><span data-stu-id="bf52b-293">In the **Menu structure** column, select **PO line receiving**, and then select the up arrow or down arrow button to move the menu item to the desired position on the mobile device menu.</span></span>
1. <span data-ttu-id="bf52b-294">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="bf52b-294">On the Action Pane, select **Save**.</span></span>

## <a name="example-scenario"></a><a name="example-scenario"></a><span data-ttu-id="bf52b-295">Beispielszenario</span><span class="sxs-lookup"><span data-stu-id="bf52b-295">Example scenario</span></span>

<span data-ttu-id="bf52b-296">Nachdem Sie alle zuvor beschriebenen Beispieldaten verfügbar gemacht und eingerichtet haben, können Sie dieses Szenario durcharbeiten, um die Funktion *Qualitätsprüfung* zu testen.</span><span class="sxs-lookup"><span data-stu-id="bf52b-296">After you've made all the previously described sample data available and set it up, you can work through this scenario to try out the *Quality check* feature.</span></span> <span data-ttu-id="bf52b-297">Bei den in diesem Szenario angezeigten Werten wird davon ausgegangen, dass Sie mit den Standarddemodaten arbeiten, die juristische Person **USMF** ausgewählt und die Beispieldatensätze vorbereitet haben, die weiter oben in diesem Thema beschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="bf52b-297">The values that are shown in this scenario assume that you're working with the standard demo data, that you selected the **USMF** legal entity, and that you prepared the sample records that are described earlier in this topic.</span></span> <span data-ttu-id="bf52b-298">Dieses Szenario dient auch als Beispiel, das zeigt, wie die Funktion in einer Produktionseinstellung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="bf52b-298">This scenario also serves as an example that shows how the feature can be used in a production setting.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="bf52b-299">Eine Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="bf52b-299">Create a purchase order</span></span>

1. <span data-ttu-id="bf52b-300">Wechseln Sie zu **Beschaffung \> Bestellungen \> Alle Bestellungen**.</span><span class="sxs-lookup"><span data-stu-id="bf52b-300">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="bf52b-301">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="bf52b-301">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="bf52b-302">Legen Sie im Dialogfeld **Bestellung erstellen** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="bf52b-302">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="bf52b-303">**Kreditorenkonto:** *104*</span><span class="sxs-lookup"><span data-stu-id="bf52b-303">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="bf52b-304">**Lagerort:** *51*</span><span class="sxs-lookup"><span data-stu-id="bf52b-304">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="bf52b-305">Wählen Sie **OK** aus, um das Dialogfeld zu schließen und die neue Bestellung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="bf52b-305">Select **OK** to close the dialog box and open the new purchase order.</span></span>
1. <span data-ttu-id="bf52b-306">Das Raster im Inforegister **Bestellpositionen** enthält eine neue, leere Position.</span><span class="sxs-lookup"><span data-stu-id="bf52b-306">On the **Purchase order lines** FastTab, the grid contains a new, blank line.</span></span> <span data-ttu-id="bf52b-307">Legen Sie die folgenden Werte für diese Position fest:</span><span class="sxs-lookup"><span data-stu-id="bf52b-307">On this line, set the following values:</span></span>

    - <span data-ttu-id="bf52b-308">**Artikelnummer:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="bf52b-308">**Item number:** *M9203*</span></span>
    - <span data-ttu-id="bf52b-309">**Menge** *3*</span><span class="sxs-lookup"><span data-stu-id="bf52b-309">**Quantity:** *3*</span></span>
    - <span data-ttu-id="bf52b-310">**Einheit:** *PL*</span><span class="sxs-lookup"><span data-stu-id="bf52b-310">**Unit:** *PL*</span></span>

1. <span data-ttu-id="bf52b-311">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="bf52b-311">On the Action Pane, select **Save**.</span></span>

### <a name="process-quality-check-receiving"></a><span data-ttu-id="bf52b-312">Eingangsqualitätsprüfung durchführen</span><span class="sxs-lookup"><span data-stu-id="bf52b-312">Process quality check receiving</span></span>

<span data-ttu-id="bf52b-313">Nachdem die Bestellung erstellt wurde, kann sie über das Menüelement **PO-Positionseingang** und die Funktionalität der Funktion *Qualitätsprüfung* empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="bf52b-313">After the purchase order has been created, it can be received by using the **PO line receiving** menu item and the functionality of the *Quality check* feature.</span></span>

#### <a name="receive-pallet-1"></a><span data-ttu-id="bf52b-314">Palette 1 empfangen</span><span class="sxs-lookup"><span data-stu-id="bf52b-314">Receive pallet 1</span></span>

1. <span data-ttu-id="bf52b-315">Melden Sie sich bei der Warehouse-App als ein Benutzer für Lagerort *51* an.</span><span class="sxs-lookup"><span data-stu-id="bf52b-315">Sign in to the warehouse app as a user for warehouse *51*.</span></span> <span data-ttu-id="bf52b-316">(Geben Sie *51* als Benutzer-ID und *1* als Passwort ein.)</span><span class="sxs-lookup"><span data-stu-id="bf52b-316">(Enter *51* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="bf52b-317">Gehen Sie zu **Eingehend \> PO-Positionseingang**.</span><span class="sxs-lookup"><span data-stu-id="bf52b-317">Go to **Inbound \> PO line receiving**.</span></span>
1. <span data-ttu-id="bf52b-318">Geben Sie im Feld **PONUM** die Bestellnummer ein.</span><span class="sxs-lookup"><span data-stu-id="bf52b-318">In the **PONUM** field, enter the purchase order number.</span></span>
1. <span data-ttu-id="bf52b-319">Bestätigen Sie die Bestellnummer.</span><span class="sxs-lookup"><span data-stu-id="bf52b-319">Confirm the purchase order number.</span></span>
1. <span data-ttu-id="bf52b-320">Geben Sie im Feld **POSNUM** die Zahl der eingegangenen Bestellposition ein.</span><span class="sxs-lookup"><span data-stu-id="bf52b-320">In the **LINENUM** field, enter the number of the purchase order line that is being received.</span></span> <span data-ttu-id="bf52b-321">Da die Bestellung in diesem Szenario nur eine Position enthält, geben Sie *1* im Feld **POSNUM** bei jedem Eingangsschritt ein.</span><span class="sxs-lookup"><span data-stu-id="bf52b-321">Because the order has only one line in this scenario, you will enter *1* in the **LINENUM** field for each receiving step.</span></span>
1. <span data-ttu-id="bf52b-322">Bestätigen Sie die Positionsnummer.</span><span class="sxs-lookup"><span data-stu-id="bf52b-322">Confirm the line number.</span></span>
1. <span data-ttu-id="bf52b-323">Geben Sie im Feld **MENGE** die eingehende Menge ein.</span><span class="sxs-lookup"><span data-stu-id="bf52b-323">In the **QTY** field, enter the quantity to receive.</span></span> <span data-ttu-id="bf52b-324">Weil die Bestellung in diesem Szenario drei Paletten (*PL*) umfasst und es drei Eingangsschritte gibt, geben Sie für jeden Schritt *1* im Feld **MENGE** ein.</span><span class="sxs-lookup"><span data-stu-id="bf52b-324">Because the purchase order is for three pallets (*PL*) in this scenario, and there are three receiving steps, you will enter *1* in the **QTY** field for each receiving step.</span></span>
1. <span data-ttu-id="bf52b-325">Bestätigen Sie die Menge.</span><span class="sxs-lookup"><span data-stu-id="bf52b-325">Confirm the quantity.</span></span>

    <span data-ttu-id="bf52b-326">Eine Seite **Qualitätsprüfung** öffnet sich, die aber keine Eingagefelder enthält.</span><span class="sxs-lookup"><span data-stu-id="bf52b-326">The **Quality check** page that appears has no entry fields.</span></span> <span data-ttu-id="bf52b-327">Sie hat nur die Bestätigungstaste (Häkchen) unten und die Menütaste (**≡**) oben.</span><span class="sxs-lookup"><span data-stu-id="bf52b-327">It has only the confirmation (check mark) button at the bottom and the Menu button (**≡**) at the top.</span></span> <span data-ttu-id="bf52b-328">(Die Menütaste wird manchmal als Hamburger- oder Hamburgerschaltfläche bezeichnet.) Um den Qualitätsprüfungsprozess zu beschleunigen, bestätigt der Benutzer nur die Seite **Qualitätsprüfung**, wenn die Palette die Qualitätsprüfung passiert.</span><span class="sxs-lookup"><span data-stu-id="bf52b-328">(The Menu button is sometimes referred to as the hamburger or the hamburger button.) To expedite the quality check process, when the pallet passes the quality check, the user just confirms the **Quality check** page.</span></span>

    <span data-ttu-id="bf52b-329">![Qualitätsprüfungsseite](media/quality-check.png "Qualitätsprüfungsseite")</span><span class="sxs-lookup"><span data-stu-id="bf52b-329">![Quality check page](media/quality-check.png "Quality check page")</span></span>

1. <span data-ttu-id="bf52b-330">Wählen Sie die Bestätigungsschaltfläche, um die Qualitätsprüfung für Palette 1 aus Position 1 als bestanden zu kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="bf52b-330">Select the confirmation button to pass the quality check for pallet 1 from line 1.</span></span>

    <span data-ttu-id="bf52b-331">Die Seite **Bestellungen: Einlagern**, die sich öffnet, enthält die Details der Einlagerungsarbeit:</span><span class="sxs-lookup"><span data-stu-id="bf52b-331">The **Purchase orders: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="bf52b-332">**LOC:** Das System hat den Lagerplatz ermittelt</span><span class="sxs-lookup"><span data-stu-id="bf52b-332">**LOC:** The system determined location</span></span>

        <span data-ttu-id="bf52b-333">Dieser Lagerplatz ist der vorgesehene Einlagerungsort für die eingehende Bestellung.</span><span class="sxs-lookup"><span data-stu-id="bf52b-333">This location is the designated putaway location for purchase order receiving.</span></span>

    - <span data-ttu-id="bf52b-334">**LP:** Die vom System generierte Ladungsträger-ID</span><span class="sxs-lookup"><span data-stu-id="bf52b-334">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="bf52b-335">**Artikel:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="bf52b-335">**Item:** *M9203*</span></span>
    - <span data-ttu-id="bf52b-336">**Menge:** *1 PL: 100 Stück*</span><span class="sxs-lookup"><span data-stu-id="bf52b-336">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="bf52b-337">Die Artikelbeschreibung wird ebenfalls angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bf52b-337">The item description is also shown.</span></span>

1. <span data-ttu-id="bf52b-338">Bestätigen Sie die Einlagerungsarbeiten.</span><span class="sxs-lookup"><span data-stu-id="bf52b-338">Confirm the putaway work.</span></span>

    <span data-ttu-id="bf52b-339">Auf der Seite **Aufgabe** der eingehenden Bestellposition erhalten Sie die Meldung „Arbeit abgeschlossen“.</span><span class="sxs-lookup"><span data-stu-id="bf52b-339">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="bf52b-340">Das Feld **POSNUM** ist verfügbar, damit Sie mit dem Eingang der nächsten Palette beginnen können.</span><span class="sxs-lookup"><span data-stu-id="bf52b-340">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

#### <a name="receive-pallet-2"></a><span data-ttu-id="bf52b-341">Palette 2 empfangen</span><span class="sxs-lookup"><span data-stu-id="bf52b-341">Receive pallet 2</span></span>

<span data-ttu-id="bf52b-342">In diesem Szenario wird Palette 2 abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="bf52b-342">For this scenario, pallet 2 will be rejected.</span></span>

1. <span data-ttu-id="bf52b-343">Geben Sie in dem Feld **POSNUM** *1* ein und bestätigen Sie die Positionsnummer.</span><span class="sxs-lookup"><span data-stu-id="bf52b-343">In the **LINENUM** field, enter *1*, and confirm the line number.</span></span>
1. <span data-ttu-id="bf52b-344">Das Feld **MENGE** ist jetzt verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bf52b-344">The **QTY** field is now available.</span></span> <span data-ttu-id="bf52b-345">Geben Sie *1* ein und bestätigen Sie die Menge.</span><span class="sxs-lookup"><span data-stu-id="bf52b-345">Enter *1*, and confirm the quantity.</span></span>

    <span data-ttu-id="bf52b-346">Die Seite **Qualitätsprüfung** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bf52b-346">The **Quality check** page appears.</span></span> <span data-ttu-id="bf52b-347">Für diesen Wareneingang wird die Palette aus Qualitätsgründen abgelehnt und am Qualitätslagerplatz *QMS* eingelagert.</span><span class="sxs-lookup"><span data-stu-id="bf52b-347">For this receipt, the pallet will be rejected for quality, and it will be put into the *QMS* quality location.</span></span>

1. <span data-ttu-id="bf52b-348">Wählen Sie die Menütaste (**≡**) oben auf der Seite und wählen Sie dann im Menü die Option **Ablehnen**.</span><span class="sxs-lookup"><span data-stu-id="bf52b-348">Select the Menu button (**≡**) at the top of the page, and then, on the menu, select **Reject**.</span></span>
1. <span data-ttu-id="bf52b-349">Auf der Seite **Aufgabe**, die angezeigt wird, geben Sie **QMS** als Lagerplatz für das *Einlagern* ein, um die Palette zur weiteren Überprüfung zu senden.</span><span class="sxs-lookup"><span data-stu-id="bf52b-349">On the **Task** page that appears, enter **QMS** as the *Put* location to send the pallet to for further inspection.</span></span>

    <span data-ttu-id="bf52b-350">Die Seite **Qualität in der Qualitätsprüfung: Einlagern**, die sich öffnet, enthält die Details der Einlagerungsarbeit:</span><span class="sxs-lookup"><span data-stu-id="bf52b-350">The **Quality in quality check: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="bf52b-351">**LOC:** *QMS*</span><span class="sxs-lookup"><span data-stu-id="bf52b-351">**LOC:** *QMS*</span></span>

        <span data-ttu-id="bf52b-352">Dieser Lagerplatz ist der vorgesehene Einlagerungsort für abgelehnte eingehende Qualität.</span><span class="sxs-lookup"><span data-stu-id="bf52b-352">This location is the designated putaway location for rejected quality receiving.</span></span>

    - <span data-ttu-id="bf52b-353">**LP:** Die vom System generierte Ladungsträger-ID</span><span class="sxs-lookup"><span data-stu-id="bf52b-353">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="bf52b-354">**Artikel:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="bf52b-354">**Item:** *M9203*</span></span>
    - <span data-ttu-id="bf52b-355">**Menge:** *1 PL: 100 Stück*</span><span class="sxs-lookup"><span data-stu-id="bf52b-355">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="bf52b-356">Die Artikelbeschreibung wird ebenfalls angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bf52b-356">The item description is also shown.</span></span>

1. <span data-ttu-id="bf52b-357">Bestätigen Sie die Einlagerungsarbeiten.</span><span class="sxs-lookup"><span data-stu-id="bf52b-357">Confirm the putaway work.</span></span>

    <span data-ttu-id="bf52b-358">Auf der Seite **Aufgabe** der eingehenden Bestellposition erhalten Sie die Meldung „Arbeit abgeschlossen“.</span><span class="sxs-lookup"><span data-stu-id="bf52b-358">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="bf52b-359">Das Feld **POSNUM** ist verfügbar, damit Sie mit dem Eingang der nächsten Palette beginnen können.</span><span class="sxs-lookup"><span data-stu-id="bf52b-359">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

<span data-ttu-id="bf52b-360">Sie haben nun die Qualitätsprüfung abgeschlossen und einen Qualitätsprüfungsauftrag für die abgelehnte Palette erstellt.</span><span class="sxs-lookup"><span data-stu-id="bf52b-360">You've now completed the quality check and created a quality order for the rejected pallet.</span></span> <span data-ttu-id="bf52b-361">Um den erstellten Auftrag anzusehen gehen Sie zu **Bestandsverwaltung \> Periodische Aufgaben \> Qualitätsmanagement \> Qualitätsprüfungsauftrag**.</span><span class="sxs-lookup"><span data-stu-id="bf52b-361">To view the order that was created, go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>

<span data-ttu-id="bf52b-362">Jetzt können Tests zu Qualitätsprüfungsaufträge verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="bf52b-362">Quality order testing can now be processed.</span></span> <span data-ttu-id="bf52b-363">Qualitätstests werden in diesem Thema nicht behandelt.</span><span class="sxs-lookup"><span data-stu-id="bf52b-363">Quality testing isn't covered in this topic.</span></span>

<span data-ttu-id="bf52b-364">Weitere Informationen zum Qualitätsmanagement finden Sie unter [Qualitätsmanagement – Übersicht](../inventory/enable-quality-management.md)</span><span class="sxs-lookup"><span data-stu-id="bf52b-364">For more information about quality management, see [Quality management overview](../inventory/enable-quality-management.md)</span></span>

#### <a name="receive-pallet-3"></a><span data-ttu-id="bf52b-365">Palette 3 empfangen</span><span class="sxs-lookup"><span data-stu-id="bf52b-365">Receive pallet 3</span></span>

<span data-ttu-id="bf52b-366">In diesem Szenario wird Palette 3 angenommen.</span><span class="sxs-lookup"><span data-stu-id="bf52b-366">For this scenario, pallet 3 will be accepted.</span></span>

1. <span data-ttu-id="bf52b-367">Geben Sie in dem Feld **POSNUM** *1* ein und bestätigen Sie die Positionsnummer.</span><span class="sxs-lookup"><span data-stu-id="bf52b-367">In the **LINENUM** field, enter *1*, and confirm the line number.</span></span>
1. <span data-ttu-id="bf52b-368">Das Feld **MENGE** ist jetzt verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bf52b-368">The **QTY** field is now available.</span></span> <span data-ttu-id="bf52b-369">Geben Sie *1* ein und bestätigen Sie die Menge.</span><span class="sxs-lookup"><span data-stu-id="bf52b-369">Enter *1*, and confirm the quantity.</span></span>

    <span data-ttu-id="bf52b-370">Die Seite **Qualitätsprüfung** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bf52b-370">The **Quality check** page appears.</span></span> <span data-ttu-id="bf52b-371">Für diesen Wareneingang wird die Palette aus Qualitätsgründen angenommen und am Massenlagerplatz eingelagert.</span><span class="sxs-lookup"><span data-stu-id="bf52b-371">For this receipt, the pallet will be accepted for quality, and it will be put into a bulk putaway location.</span></span>

1. <span data-ttu-id="bf52b-372">Wählen Sie die Bestätigungsschaltfläche, um die Qualitätsprüfung als bestanden zu kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="bf52b-372">Select the confirmation button to pass the quality check.</span></span>

    <span data-ttu-id="bf52b-373">Die Seite **Bestellungen: Einlagern**, die sich öffnet, enthält die Details der Einlagerungsarbeit:</span><span class="sxs-lookup"><span data-stu-id="bf52b-373">The **Purchase orders: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="bf52b-374">**LOC:** Das System hat den Lagerplatz ermittelt</span><span class="sxs-lookup"><span data-stu-id="bf52b-374">**LOC:** The system determined location</span></span>

        <span data-ttu-id="bf52b-375">Dieser Lagerplatz ist der vorgesehene Einlagerungsort für die eingehende Bestellung.</span><span class="sxs-lookup"><span data-stu-id="bf52b-375">This location is the designated putaway location for purchase order receiving.</span></span>

    - <span data-ttu-id="bf52b-376">**LP:** Die vom System generierte Ladungsträger-ID</span><span class="sxs-lookup"><span data-stu-id="bf52b-376">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="bf52b-377">**Artikel:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="bf52b-377">**Item:** *M9203*</span></span>
    - <span data-ttu-id="bf52b-378">**Menge:** *1 PL: 100 Stück*</span><span class="sxs-lookup"><span data-stu-id="bf52b-378">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="bf52b-379">Die Artikelbeschreibung wird ebenfalls angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bf52b-379">The item description is also shown.</span></span>

1. <span data-ttu-id="bf52b-380">Bestätigen Sie die Einlagerungsarbeiten.</span><span class="sxs-lookup"><span data-stu-id="bf52b-380">Confirm the putaway work.</span></span>

    <span data-ttu-id="bf52b-381">Auf der Seite **Aufgabe** der eingehenden Bestellposition erhalten Sie die Meldung „Arbeit abgeschlossen“.</span><span class="sxs-lookup"><span data-stu-id="bf52b-381">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="bf52b-382">Das Feld **POSNUM** ist verfügbar, damit Sie mit dem Eingang der nächsten Palette beginnen können.</span><span class="sxs-lookup"><span data-stu-id="bf52b-382">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

1. <span data-ttu-id="bf52b-383">Wählen Sie die Menütaste (**≡**) oben auf der Seite und wählen Sie dann im Menü die Option **Abbrechen**, um zum Menü zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="bf52b-383">Select the Menu button (**≡**) at the top of the page, and then, on the menu, select **Cancel** to return to the menu.</span></span>

<span data-ttu-id="bf52b-384">Sie können jetzt die mobile App schließen.</span><span class="sxs-lookup"><span data-stu-id="bf52b-384">You can now close the mobile app.</span></span>
