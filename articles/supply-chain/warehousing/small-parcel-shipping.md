---
title: Kleinpaketlieferung
description: Dieses Thema enthält Informationen zur Kleinpaketlieferung. Diese Funktion aktiviert Microsoft Dynamics 365 Supply Chain Management, um Details zu einem gepackten Container an den Spediteur zu senden und dann ein Adressetikett, einen Frachtsatz und eine Sendungsverfolgungsnummer von diesem Spediteur zu erhalten.
author: Mirzaab
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateEngine, TMSCarrier, CustTable, TMSShippingCarrierCustomerAccount, TMSSmallParcelShippingFeature
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-08
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 3e72959d79e9b3b03e061a0f26750e3bd025219e
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910208"
---
# <a name="small-parcel-shipping"></a><span data-ttu-id="b0d1d-104">Kleinpaketlieferung</span><span class="sxs-lookup"><span data-stu-id="b0d1d-104">Small parcel shipping</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b0d1d-105">Die Kleinpaketlieferung ermöglicht Microsoft Dynamics 365 Supply Chain Management die direkte Interaktion mit Spediteuren durch die Bereitstellung eines Frameworks für die Kommunikation über Spediteur-APIs.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-105">The small parcel shipping (SPS) feature enables Microsoft Dynamics 365 Supply Chain Management to interact directly with shipping carriers by providing a framework for communication through carrier APIs.</span></span> <span data-ttu-id="b0d1d-106">Diese Funktion ist nützlich, wenn Sie einzelne Aufträge über kommerzielle Spediteure versenden, anstatt sich für den Containerversand oder den Versand mit weniger als Wagenladung zu entscheiden.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-106">This functionality is useful when you're shipping individual sales orders via commercial shipping carriers instead of using container shipping or less-than-truckload (LTL) shipping.</span></span>

<span data-ttu-id="b0d1d-107">Die Kleinpaketlieferung interagiert mit Ihrem Spediteur über ein dediziertes *Tarifmodul*.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-107">The SPS feature interacts with your shipping carrier through a dedicated *rate engine*.</span></span> <span data-ttu-id="b0d1d-108">Ihre Organisation muss dieses Tarifmodul in Zusammenarbeit mit dem Spediteur oder dem Spediteurnetzwerk entwickeln.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-108">Your organization must develop this rate engine in collaboration with your carrier or carrier hub service.</span></span> <span data-ttu-id="b0d1d-109">Dieses Tarifmodul aktiviert Supply Chain Management, um Details zu einem gepackten Container an den Spediteur zu senden und dann ein Adressetikett, einen Frachtsatz und eine Sendungsverfolgungsnummer von diesem Spediteur zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-109">The rate engine enables Supply Chain Management to submit details about a packed container to your carrier, and then receive a shipping label, shipping rate, and tracking number back from that carrier.</span></span>

<span data-ttu-id="b0d1d-110">Der übermittelte Frachtsatz wird dem zugehörigen Auftrag als sonstige Gebühr hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-110">The shipping rate that is returned is added to the associated sales order as a miscellaneous charge.</span></span> <span data-ttu-id="b0d1d-111">Das Adressetikett kann dann automatisch mit einem ZPL-Drucker (Zebra Programming Language) ausgedruckt und an der Lieferung angebracht werden.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-111">The shipping label that is returned can then automatically be printed by using a Zebra Programming Language (ZPL) printer and applied to the shipment.</span></span> <span data-ttu-id="b0d1d-112">Der Spediteur scannt dieses Adressetikett, wenn er die Päckchen an Ihrem Lagerort abholt.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-112">The carrier will scan this shipping label when it picks up the packages at your warehouse.</span></span>

## <a name="prepare-your-system-to-support-sps"></a><span data-ttu-id="b0d1d-113">Vorbereiten Ihres System auf die Kleinpaketlieferung</span><span class="sxs-lookup"><span data-stu-id="b0d1d-113">Prepare your system to support SPS</span></span>

<span data-ttu-id="b0d1d-114">Bevor Sie die Kleinpaketlieferung verwenden können, müssen Sie sie in der Funktionsverwaltung aktivieren, Ihr Traifmodul hinzufügen und die Module **Transportverwaltung** und **Lagerortverwaltung** entsprechend einrichten.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-114">Before you can start to use SPS functionality, you must turn on the SPS feature in Feature management, add your rate engine, and set up the **Transportation management** and **Warehouse management** modules to support it.</span></span>

### <a name="turn-on-the-sps-feature"></a><span data-ttu-id="b0d1d-115">Aktivieren der Kleinpaketlieferung</span><span class="sxs-lookup"><span data-stu-id="b0d1d-115">Turn on the SPS feature</span></span>

<span data-ttu-id="b0d1d-116">Bevor Sie die Kleinpaketlieferung nutzen können, muss sie in Ihrem System aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-116">Before you can use the SPS feature, it must be turned on in your system.</span></span> <span data-ttu-id="b0d1d-117">Administratoren können den Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) verwenden, um den Status der Funktion zu prüfen und sie bei Bedarf einzuschalten.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-117">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="b0d1d-118">Dort wird die Funktion folgendermaßen aufgelistet:</span><span class="sxs-lookup"><span data-stu-id="b0d1d-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="b0d1d-119">**Modul:** *Transportverwaltung*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-119">**Module:** *Transportation management*</span></span>
- <span data-ttu-id="b0d1d-120">**Funktionsname:** *Kleinpaketlieferung*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-120">**Feature name:** *Small parcel shipping*</span></span>

### <a name="deploy-and-set-up-rate-engines"></a><span data-ttu-id="b0d1d-121">Bereitstellen und Einrichten von Tarifmodulen</span><span class="sxs-lookup"><span data-stu-id="b0d1d-121">Deploy and set up rate engines</span></span>

<span data-ttu-id="b0d1d-122">Supply Chain Management umfasst keine Tarifmodule.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-122">Supply Chain Management doesn't include any rate engines.</span></span> <span data-ttu-id="b0d1d-123">Die benötigten Tarifmodule müssen bezogen oder erstellt und dann zu Ihrem System hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-123">You must obtain or create any rate engines that you require, and then add them to your system.</span></span> <span data-ttu-id="b0d1d-124">Microsoft bietet jedoch eine Demotarifmodule an, die Sie zum Testen verwenden könnten.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-124">However, Microsoft provides a demo rate engine that you can use for testing.</span></span>

#### <a name="download-and-deploy-the-demo-rate-engine"></a><span data-ttu-id="b0d1d-125">Herunterladen und Bereitstellen des Demotarifmoduls</span><span class="sxs-lookup"><span data-stu-id="b0d1d-125">Download and deploy the demo rate engine</span></span>

<span data-ttu-id="b0d1d-126">Befolgen Sie diese Schritte, um das Demotarifmodul zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-126">Follow these steps to get the demo rate engine.</span></span>

1. <span data-ttu-id="b0d1d-127">Laden Sie auf GitHub die [Dynamic Link Library (DLL) für das Demotarifmodul](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS) herunter.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-127">On GitHub, download the [dynamic-link library (DLL) for the demo rate engine](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS).</span></span>
1. <span data-ttu-id="b0d1d-128">Speichern Sie die DLL auf Ihrem Supply Chain Management-Server im Ordner **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin**.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-128">On your Supply Chain Management server, save the DLL in the **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin** folder.</span></span>

#### <a name="create-and-deploy-functional-rate-engines"></a><span data-ttu-id="b0d1d-129">Erstellen und Bereitstellen funktionsfähiger Tarifmodule</span><span class="sxs-lookup"><span data-stu-id="b0d1d-129">Create and deploy functional rate engines</span></span>

<span data-ttu-id="b0d1d-130">Informationen zum Erstellen und Bereitstellen funktionsfähiger Tarifmodule, die in einer Produktions- oder Testumgebung verwendet werden können, finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="b0d1d-130">For information about how to create and deploy functional rate engines so that they can be used in a production or test environment, see the following topics:</span></span>

- [<span data-ttu-id="b0d1d-131">Erstellen eines neuen Transportverwaltungsmoduls</span><span class="sxs-lookup"><span data-stu-id="b0d1d-131">Create a new transportation management engine</span></span>](../transportation/create-new-transportation-management-engine.md)
- [<span data-ttu-id="b0d1d-132">Einrichten von Transportverwaltungsmodulen</span><span class="sxs-lookup"><span data-stu-id="b0d1d-132">Set up transportation management engines</span></span>](/dynamicsax-2012/appuser-itpro/set-up-transportation-management-engines)

<span data-ttu-id="b0d1d-133">Weitere Informationen zum Erstellen eines Tarifmoduls für die Kleinpaketlieferung finden Sie im folgenden Blogbeitrag: [Kleinpaketlieferung: Nutzung der Kleinpaketlieferung in Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).</span><span class="sxs-lookup"><span data-stu-id="b0d1d-133">For more information about how to create an SPS rate engine, see the following blog post: [Small Parcel Shipping: How to leverage small parcel shipping functionality in Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).</span></span>

#### <a name="set-up-a-rate-engine-in-supply-chain-management"></a><span data-ttu-id="b0d1d-134">Einrichten eines Tarifmoduls in Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b0d1d-134">Set up a rate engine in Supply Chain Management</span></span>

<span data-ttu-id="b0d1d-135">Führen Sie die folgenden Schritte aus, nachdem Sie ein Tarifmodul für die Kleinpaketlieferung erstellt und bereitgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-135">After you've created and deployed a rate engine for SPS, follow these steps to set it up.</span></span>

1. <span data-ttu-id="b0d1d-136">Wechseln Sie zu **Transportverwaltung \> Einrichten \> Module \> Tarifmodul**.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-136">Go to **Transportation management \> Setup \> Engines \> Rate engine**.</span></span>
1. <span data-ttu-id="b0d1d-137">Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Zeile zum Raster hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-137">On the Action Pane, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="b0d1d-138">Legen Sie in der neuen Zeile die folgenden Felder fest.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-138">In the new row, set the following fields:</span></span>

    - <span data-ttu-id="b0d1d-139">**Tarifmodul** – Geben Sie einen eindeutigen Namen für das Tarifmodul ein.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-139">**Rating engine** – Enter a unique name for the rate engine.</span></span> <span data-ttu-id="b0d1d-140">Wenn Sie das Demotarifmodul verwenden, geben Sie *Demotarifmodul* ein.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-140">If you're using the demo rate engine, enter *Demo rate engine*.</span></span>
    - <span data-ttu-id="b0d1d-141">**Name** – Geben Sie eine kurze Beschreibung des Tarifmoduls ein.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-141">**Name** – Enter a short description of the rate engine.</span></span> <span data-ttu-id="b0d1d-142">Wenn Sie das Demotarifmodul verwenden, geben Sie *Demotarifmodul* ein.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-142">If you're using the demo rate engine, enter *Demo rate engine*.</span></span>
    - <span data-ttu-id="b0d1d-143">**Bewertungs-Metadaten-ID** – Wählen Sie die Basis aus, auf der Ihr Tarif berechnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-143">**Rating metadata ID** – Select the basis that should be used to calculate your rate.</span></span> <span data-ttu-id="b0d1d-144">Zum Beispiel könnte Ihr Tarif basierend auf der Entfernung berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-144">For example, your rate might be calculated based on distance.</span></span> <span data-ttu-id="b0d1d-145">Wenn Sie das Demotarifmodul verwenden, können Sie dieses Feld leer lassen.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-145">If you're using the demo rate engine, you can leave this field blank.</span></span>
    - <span data-ttu-id="b0d1d-146">**Modulassembly** – Geben Sie den Dateinamen des von Ihnen bereitgestellten DLL-Pakets ein.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-146">**Engine assembly** – Enter the file name of the DLL package that you deployed.</span></span> <span data-ttu-id="b0d1d-147">Wenn Sie das Demotarifmodul verwenden, geben Sie *TMSSmallParcelShippingEngine.dll* ein.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-147">If you're using the demo rate engine, enter *TMSSmallParcelShippingEngine.dll*.</span></span>
    - <span data-ttu-id="b0d1d-148">**Modulklasse** – Geben Sie den Klassennamen ein, der für Ihr Tarifmodul festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-148">**Engine class** – Enter the class name that was established for your rate engine.</span></span> <span data-ttu-id="b0d1d-149">Wenn Sie das Demotarifmodul verwenden, geben Sie *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine* ein.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-149">If you're using the demo rate engine, enter *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="b0d1d-150">Beispielszenario</span><span class="sxs-lookup"><span data-stu-id="b0d1d-150">Example scenario</span></span>

<span data-ttu-id="b0d1d-151">Dieses Beispielszenario zeigt, wie Sie die Kleinpaketlieferung einrichten und verwenden, nachdem Sie Ihr System wie zuvor in diesem Thema beschrieben vorbereitet haben.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-151">This example scenario shows how to set up and use SPS after you've prepared your system as described earlier in this topic.</span></span> <span data-ttu-id="b0d1d-152">In diesem Szenario wird das zuvor erwähnte Demotarifmodul verwendet.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-152">This scenario uses the previously mentioned demo rate engine.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="b0d1d-153">Demodaten zur Verfügung stellen</span><span class="sxs-lookup"><span data-stu-id="b0d1d-153">Make demo data available</span></span>

<span data-ttu-id="b0d1d-154">Um dieses Szenario mit den hier angegebenen Demodatensätzen und -werten durchzuarbeiten, müssen Sie ein System verwenden, auf dem die standardmäßigen [Demodaten](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) installiert sind.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-154">To work through this scenario by using the demo records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="b0d1d-155">Außerdem müssen Sie die **USMF** juristische Person auswählen, bevor Sie beginnen.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-155">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="b0d1d-156">Szenario einrichten</span><span class="sxs-lookup"><span data-stu-id="b0d1d-156">Set up the scenario</span></span>

<span data-ttu-id="b0d1d-157">In diesem Beispielszenario müssen Sie über einen Demospediteur, eine Spediteurgruppe, eine Verpackungsrichtlinie und ein Verpackungsprofil verfügen.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-157">For this example scenario, you must have a demo carrier, carrier group, packing policy, and packing profile.</span></span> <span data-ttu-id="b0d1d-158">In den folgenden Unterabschnitten wird erläutert, wie Sie die für das Szenario erforderlichen Datensätze vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-158">The following subsections explain how to prepare the records that are required for the scenario.</span></span> <span data-ttu-id="b0d1d-159">In einem Produktionsszenario ähnelt der Einrichtungsprozess normalerweise dem hier beschriebenen Prozess.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-159">In a production scenario, the setup process typically resembles the process that is described here.</span></span> <span data-ttu-id="b0d1d-160">Sie werden jedoch andere Werte einstellen.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-160">However, you will set different values.</span></span>

#### <a name="set-up-carriers"></a><span data-ttu-id="b0d1d-161">Einrichten von Spediteuren</span><span class="sxs-lookup"><span data-stu-id="b0d1d-161">Set up carriers</span></span>

<span data-ttu-id="b0d1d-162">Gehen Sie folgendermaßen vor, um einen Spediteur einzurichten.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-162">Follow these steps to set up a carrier.</span></span>

1. <span data-ttu-id="b0d1d-163">Wechseln Sie zu **Transportverwaltung \> Einstellungen \> Spediteure \> Spediteure**.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-163">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="b0d1d-164">Wählen Sie im Aktionsbereich **Neu** aus, um einen Spediteur hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-164">On the Action Pane, select **New** to add a carrier.</span></span>
1. <span data-ttu-id="b0d1d-165">Legen Sie in der Kopfzeile die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="b0d1d-165">On the header, set the following values:</span></span>

    - <span data-ttu-id="b0d1d-166">**Spediteur:** *Demospediteur*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-166">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="b0d1d-167">**Name:** *Demospediteur*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-167">**Name:** *Demo Carrier*</span></span>
    - <span data-ttu-id="b0d1d-168">**Modus:** *Boden*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-168">**Mode:** *Ground*</span></span>

1. <span data-ttu-id="b0d1d-169">Legen Sie im Inforegister **Übersicht** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="b0d1d-169">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b0d1d-170">**Spediteur aktivieren:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-170">**Activate shipping carrier:** *Yes*</span></span>
    - <span data-ttu-id="b0d1d-171">**Spediteur-Rating aktivieren:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-171">**Activate carrier rating:** *Yes*</span></span>

1. <span data-ttu-id="b0d1d-172">Wählen Sie im Inforegister **Dienstleistungen** die Option **Neu** aus, um dem Raster eine Dienstleistung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-172">On the **Services** FastTab, select **New** to add a service to the grid.</span></span>
1. <span data-ttu-id="b0d1d-173">Legen Sie die folgenden Werte für die neue Dienstleistung fest.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-173">Set the following values for the new service:</span></span>

    - <span data-ttu-id="b0d1d-174">**Spediteurdienstleistung:** *Demospediteurdienstleistung*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-174">**Carrier service:** *Demo carrier service*</span></span>
    - <span data-ttu-id="b0d1d-175">**Name:** *Demospediteurdienstleistung*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-175">**Name:** *Demo carrier service*</span></span>
    - <span data-ttu-id="b0d1d-176">**Transportmethode:** *Boden*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-176">**Transportation method:** *Ground*</span></span>

    <span data-ttu-id="b0d1d-177">Geben Sie nach Bedarf beliebige Werte für alle anderen Felder ein.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-177">Enter arbitrary values for all the other fields, as required.</span></span> <span data-ttu-id="b0d1d-178">(Wenn Sie den neuen Spediteurdatensatz speichern, wird eine neue Lieferart erstellt und das Feld **Lieferart** wird automatisch festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="b0d1d-178">(When you save the new shipping carrier record, a new mode of delivery will be created, and the **Mode of delivery** field will be set automatically.)</span></span>

1. <span data-ttu-id="b0d1d-179">Wählen Sie im Inforegister **Bewertungsprofile** die Option **Neu** aus, um ein Bewertungsprofil zum Raster hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-179">On the **Rating profiles** FastTab, select **New** to add a rating profile to the grid.</span></span>
1. <span data-ttu-id="b0d1d-180">Legen Sie die folgenden Werte für das neue Profil fest:</span><span class="sxs-lookup"><span data-stu-id="b0d1d-180">Set the following values for the new profile:</span></span>

    - <span data-ttu-id="b0d1d-181">**Bewertungsprofil:** *Demospediteurdienstleistung*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-181">**Rating profile:** *Demo carrier service*</span></span>
    - <span data-ttu-id="b0d1d-182">**Name:** *Demospediteurdienstleistung*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-182">**Name:** *Demo carrier service*</span></span>
    - <span data-ttu-id="b0d1d-183">**Tarifmodul:** *Demotarifmodul*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-183">**Rate engine:** *Demo rate engine*</span></span>

    <span data-ttu-id="b0d1d-184">Geben Sie nach Bedarf beliebige Werte für alle anderen Felder ein.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-184">Enter arbitrary values for all the other fields, as required.</span></span>

1. <span data-ttu-id="b0d1d-185">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-185">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="b0d1d-186">Weitere Informationen zum Einrichten von Spediteuren finden Sie unter [Spediteure einrichten](../transportation/tasks/set-up-shipping-carriers.md).</span><span class="sxs-lookup"><span data-stu-id="b0d1d-186">For more information about how to set up carriers, see [Set up shipping carriers](../transportation/tasks/set-up-shipping-carriers.md).</span></span>

#### <a name="set-up-carrier-service-accounts"></a><span data-ttu-id="b0d1d-187">Einrichten von Spediteurdienstleistungskonten</span><span class="sxs-lookup"><span data-stu-id="b0d1d-187">Set up carrier service accounts</span></span>

<span data-ttu-id="b0d1d-188">Gehen Sie folgendermaßen vor, um ein Spediteurdienstleistungskonto einzurichten.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-188">Follow these steps to set up a carrier service account.</span></span>

1. <span data-ttu-id="b0d1d-189">Wechseln Sie zu **Transportverwaltung \> Einrichten \> Bewertung \> Spediteurdienstleistungskonto**.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-189">Go to **Transportation management \> Setup \> Rating \> Carrier service account**.</span></span>
1. <span data-ttu-id="b0d1d-190">Wählen Sie im Aktionsbereich **Neu** aus, um ein Spediteurdienstleistungskonto hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-190">On the Action Pane, select **New** to add a carrier service account.</span></span>
1. <span data-ttu-id="b0d1d-191">Legen Sie die folgenden Werte für das neue Konto fest:</span><span class="sxs-lookup"><span data-stu-id="b0d1d-191">Set the following values for the new account:</span></span>

    - <span data-ttu-id="b0d1d-192">**Spediteur:** *Demospediteur*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-192">**Shipping Carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="b0d1d-193">**Spediteurdienstleistung:** *Demospediteurdienstleistung*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-193">**Carrier service:** *Demo carrier service*</span></span>
    - <span data-ttu-id="b0d1d-194">**Kundenkontonummer des Spediteurs:** Die Kundenkontonummer des Spediteurs, mit der die Verbindung zum Spediteur überprüft und authentifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-194">**Carrier customer account number:** The carrier customer account number that is used to verify and authenticate the connection to the shipping carrier.</span></span> <span data-ttu-id="b0d1d-195">Ihr Spediteur wird diesen Wert bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-195">Your carrier will provide this value.</span></span> <span data-ttu-id="b0d1d-196">Wenn Sie die Demodienstleistung verwenden, können Sie einen beliebigen Wert eingeben.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-196">If you're using the demo service, you can enter an arbitrary value.</span></span>
    - <span data-ttu-id="b0d1d-197">**Standort:** *6*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-197">**Site:** *6*</span></span>
    - <span data-ttu-id="b0d1d-198">**Lagerort:** *62*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-198">**Warehouse:** *62*</span></span>

    > [!NOTE]
    > <span data-ttu-id="b0d1d-199">Oft ist die **Kundenkontonummer des Spediteurs** der einzige Wert, der zur Authentifizierung der Verbindung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-199">Often, the **Carrier customer account number** value is the only value that is required to authenticate the connection.</span></span> <span data-ttu-id="b0d1d-200">Wenn Ihr Spediteur jedoch zusätzliche Authentifizierungsparameter benötigt, sollte Ihre Organisation diese Seite anpassen, um gegebenenfalls zusätzliche Felder hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-200">However, if your carrier requires additional authentication parameters, your organization should customize this page to add extra fields as appropriate.</span></span>

#### <a name="set-up-a-container-packing-policy"></a><span data-ttu-id="b0d1d-201">Einrichten einer Containerverpackungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="b0d1d-201">Set up a container packing policy</span></span>

<span data-ttu-id="b0d1d-202">Gehen Sie zum Einrichten einer Containerverpackungsrichtlinie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-202">Follow these steps to set up a container packing policy.</span></span>

1. <span data-ttu-id="b0d1d-203">Wenn Sie noch keine ZPL-Druckerdefinition eingerichtet haben, richten Sie sie mit der Anwendung Document Routing Agent ein.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-203">If you haven't already set up a ZPL printer definition, use the Document Routing Agent application to set it up.</span></span> <span data-ttu-id="b0d1d-204">Weitere Informationen finden Sie unter [Übersicht zum Dokumentendruck](../../fin-ops-core/dev-itpro/analytics/print-documents.md) und verwandten Themen.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-204">For more information, see [Document printing overview](../../fin-ops-core/dev-itpro/analytics/print-documents.md) and related topics.</span></span>
1. <span data-ttu-id="b0d1d-205">Wechseln Sie zu **Lagerortverwaltung \> Einrichten \> Container \> Containerverpackungsrichtlinien**.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-205">Go to **Warehouse Management \> Setup \> Containers \> Container packing policies**.</span></span>
1. <span data-ttu-id="b0d1d-206">Wählen Sie im Aktionsbereich **Neu** aus, um eine Containerverpackungsrichtlinie hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-206">On the Action Pane, select **New** to add a container packing policy.</span></span>
1. <span data-ttu-id="b0d1d-207">Legen Sie in der Kopfzeile der neuen Richtlinie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="b0d1d-207">On the header of the new policy, set the following values:</span></span>

    - <span data-ttu-id="b0d1d-208">**Containerverpackungsrichtlinie:** *Demoverpackungsrichtlinie*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-208">**Container packing policy:** *Demo packing policy*</span></span>
    - <span data-ttu-id="b0d1d-209">**Beschreibung:** Eine Beschreibung der Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-209">**Description:** A description of the policy</span></span>

1. <span data-ttu-id="b0d1d-210">Legen Sie im Inforegister **Übersicht** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="b0d1d-210">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b0d1d-211">**Lagerort:** *62*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-211">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="b0d1d-212">**Standardlagerplatz für letzte Lieferung:** *Ladebereichstor*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-212">**Default location for final shipment:** *Baydoor*</span></span>
    - <span data-ttu-id="b0d1d-213">**Gewichtseinheit:** *KG*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-213">**Weight unit:** *KG*</span></span>
    - <span data-ttu-id="b0d1d-214">**Richtlinie zum Containerabschluss:** *Automatische Freigabe*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-214">**Container closing policy:** *Automatic release*</span></span>
    - <span data-ttu-id="b0d1d-215">**Richtlinien zur Containerfreigabe:** *Am endgültigen Versandort zur Verfügung stellen*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-215">**Container release policy:** *Make available at final shipping location*</span></span>

1. <span data-ttu-id="b0d1d-216">Legen Sie im Inforegister **Containermanifestierung** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="b0d1d-216">On the **Container manifest** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b0d1d-217">**Automatisch manifestieren beim Schließen des Containers:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-217">**Automatic manifest at container close:** *Yes*</span></span>
    - <span data-ttu-id="b0d1d-218">**Manifestanforderungen für Container:** *Transportverwaltung*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-218">**Manifest requirements for container:** *Transportation management*</span></span>
    - <span data-ttu-id="b0d1d-219">**Containerinhalt drucken:** *Nein*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-219">**Print container contents:** *No*</span></span>

1. <span data-ttu-id="b0d1d-220">Legen Sie im Inforegister **Containerbeschriftungsdruck** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="b0d1d-220">On the **Carrier label printing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b0d1d-221">**Adressetikett für Container drucken:** *Immer*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-221">**Print container shipping label:** *Always*</span></span>
    - <span data-ttu-id="b0d1d-222">**Druckername:** Der Name des ZPL-Druckers, der Adressetiketten drucken soll.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-222">**Printer name:** The name of the ZPL printer that should print shipping labels</span></span>

#### <a name="set-up-a-packing-profile"></a><span data-ttu-id="b0d1d-223">Einrichten eines Verpackungsprofils</span><span class="sxs-lookup"><span data-stu-id="b0d1d-223">Set up a packing profile</span></span>

<span data-ttu-id="b0d1d-224">Gehen Sie zum Einrichten eines Verpackungsprofils folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-224">Follow these steps to set up a packing profile.</span></span>

1. <span data-ttu-id="b0d1d-225">Wechseln Sie zu **Lagerortverwaltung \> Einrichten \> Verpackung \> Verpackungsprofile**.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-225">Go to **Warehouse Management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="b0d1d-226">Wählen Sie im Aktionsbereich **Neu** aus, um ein Verpackungsprofil zum Raster hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-226">On the Action Pane, select **New** to add a packing profile to the grid.</span></span>
1. <span data-ttu-id="b0d1d-227">Legen Sie die folgenden Werte für das neue Profil fest:</span><span class="sxs-lookup"><span data-stu-id="b0d1d-227">Set the following values for the new profile:</span></span>

    - <span data-ttu-id="b0d1d-228">**Verpackungsprofilkennung:** *Demoverpackungsprofil*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-228">**Packing profile ID:** *Demo packing profile*</span></span>
    - <span data-ttu-id="b0d1d-229">**Beschreibung:** Eine Beschreibung des Profils.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-229">**Description:** A description of the profile</span></span>
    - <span data-ttu-id="b0d1d-230">**Containerverpackungsrichtlinie:** *Demoverpackungsrichtlinie*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-230">**Container packing policy:** *Demo packing policy*</span></span>
    - <span data-ttu-id="b0d1d-231">**Containerkennungsmodus:** *Auto*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-231">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="b0d1d-232">**Containertyp:** *Kleiner Karton*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-232">**Container type:** *SmallBox*</span></span>

#### <a name="set-up-a-customer-to-use-the-sps-carrier"></a><span data-ttu-id="b0d1d-233">Einrichten eines Kunden zurVerwendung des Spediteurs für Kleinpaketlieferungen</span><span class="sxs-lookup"><span data-stu-id="b0d1d-233">Set up a customer to use the SPS carrier</span></span>

<span data-ttu-id="b0d1d-234">Führen Sie die folgenden Schritte aus, um einen Kunden so einzurichten, dass er den von Ihnen erstellten Spediteur verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-234">Follow these steps to set up a customer so that it can use the carrier that you created.</span></span>

1. <span data-ttu-id="b0d1d-235">Wechseln Sie zu **Debitoren \> Kunden \> Alle Kunden**.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-235">Go to **Accounts receivable \> customers \> All customers**.</span></span>
1. <span data-ttu-id="b0d1d-236">Suchen Sie im Raster den Kunden *US-027* und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-236">In the grid, find and select customer *US-027*.</span></span>
1. <span data-ttu-id="b0d1d-237">Wählen Sie im Aktionsbereich auf der Registerkarte **Allgemein** in der Gruppe **Einrichten** die Option **Kundenkonten des Spediteurs** aus.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-237">On the Action Pane, on the **General** tab, in the **Set up** group, select **Carrier customer accounts**.</span></span>
1. <span data-ttu-id="b0d1d-238">Wählen Sie auf der Seite **Kundenkonten des Spediteurs** im Aktionsbereich **Neu** aus, um ein Konto zum Raster hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-238">On the **Carrier customer accounts** page, on the Action Pane, select **New** to add an account to the grid.</span></span>
1. <span data-ttu-id="b0d1d-239">Legen Sie die folgenden Werte für das neue Konto fest:</span><span class="sxs-lookup"><span data-stu-id="b0d1d-239">Set the following values for the new account:</span></span>

    - <span data-ttu-id="b0d1d-240">**Spediteur:** *Demospediteur*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-240">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="b0d1d-241">**Kundenkontonummer des Spediteurs:** *12345* (Der Wert ist für dieses Szenario nicht wichtig, wird jedoch im nächsten Abschnitt referenziert.)</span><span class="sxs-lookup"><span data-stu-id="b0d1d-241">**Carrier customer account number:** *12345* (The value isn't important for this scenario, but it will be referred to in the next section.)</span></span>

### <a name="go-through-the-example-scenario"></a><span data-ttu-id="b0d1d-242">Durchgehen des Beispielszenarios</span><span class="sxs-lookup"><span data-stu-id="b0d1d-242">Go through the example scenario</span></span>

<span data-ttu-id="b0d1d-243">Nachdem Sie alle Beispieldaten wie im vorherigen Abschnitt beschrieben eingerichtet haben, können Sie das Beispielszenario durchgehen.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-243">After you've set up all the sample data as described in the previous section, you're ready to go through the example scenario.</span></span>

#### <a name="create-a-sales-order-and-process-the-work"></a><span data-ttu-id="b0d1d-244">Erstellen eines Auftrags und bearbeiten der Arbeit</span><span class="sxs-lookup"><span data-stu-id="b0d1d-244">Create a sales order and process the work</span></span>

<span data-ttu-id="b0d1d-245">Gehen Sie folgendermaßen vor, um einen Auftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-245">Follow these steps to create a sales order.</span></span>

1. <span data-ttu-id="b0d1d-246">Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-246">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="b0d1d-247">Wählen Sie **Neu** aus, um einen Auftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-247">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="b0d1d-248">Legen Sie im Dialogfeld **Auftrag erstellen** das Feld **Debitorenkonto** auf *US-027* fest.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-248">In the **Create sales order** dialog box, set the **Customer account** field to *US-027*.</span></span>
1. <span data-ttu-id="b0d1d-249">Wählen Sie **OK** aus, um den Auftrag zu erstellen und das Dialogfeld zu schließen.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-249">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="b0d1d-250">Der neue Auftrag wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-250">The new sales order is opened.</span></span> <span data-ttu-id="b0d1d-251">Legen Sie im Inforegister **Auftragskopf** das Feld **Kundenkontonummer des Spediteurs** auf den Wert fest, den Sie zuvor für diesen Kunden ausgewählt haben (*12345*).</span><span class="sxs-lookup"><span data-stu-id="b0d1d-251">On the **Sales order header** FastTab, set the **Carrier customer account number** field to the value that you selected for this customer earlier (*12345*).</span></span>
1. <span data-ttu-id="b0d1d-252">Fügen Sie im Abschnitt **Auftragspositionen** eine Verkaufsposition hinzu und legen Sie die folgenden Werte dafür fest:</span><span class="sxs-lookup"><span data-stu-id="b0d1d-252">In the **Sales order lines** section, add a sales line, and set the following values for it:</span></span>

    - <span data-ttu-id="b0d1d-253">**Artikelnummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-253">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="b0d1d-254">**Menge** *1*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-254">**Quantity:** *1*</span></span>
    - <span data-ttu-id="b0d1d-255">**Standort:** *6*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-255">**Site:** *6*</span></span>
    - <span data-ttu-id="b0d1d-256">**Lagerort:** *62*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-256">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="b0d1d-257">Wechseln Sie zur Ansicht **Kopfzeile**.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-257">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="b0d1d-258">Legen Sie im Inforegister **Lieferung** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="b0d1d-258">On the **Delivery** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b0d1d-259">**Spediteur:** *Demospediteur*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-259">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="b0d1d-260">**Spediteurdienstleistung:** *Demospediteurdienstleistung*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-260">**Carrier service:** *Demo carrier service*</span></span>

1. <span data-ttu-id="b0d1d-261">Wechseln Sie zurück zur Ansicht **Positionen**.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-261">Switch back to the **Lines** view.</span></span> <span data-ttu-id="b0d1d-262">Wenn Sie aufgefordert werden, die Lieferart für die Verkaufspositionen zu aktualisieren, wählen Sie **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-262">If you're prompted to update the mode of delivery for the sales lines, select **Yes**.</span></span>
1. <span data-ttu-id="b0d1d-263">Wählen Sie im Abschnitt **Auftragspositionen** die Auftragsposition aus, die Sie zuvor eingerichtet haben, und wählen Sie dann **Bestand \> Reservierung** aus.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-263">In the **Sales order lines** section, select the order line that you set up earlier, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="b0d1d-264">Wählen Sie auf der Seite **Reservierung** die Option **Los reservieren** aus, um die volle Menge der ausgewählten Position im Lagerort zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-264">On the **Reservation** page, select **Reserve lot** to reserve the selected line's full quantity in the warehouse.</span></span>
1. <span data-ttu-id="b0d1d-265">Schließen Sie die Seite **Reservierung**, um zum Auftrag zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-265">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="b0d1d-266">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** auf **Lagerortfreigabe**.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-266">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="b0d1d-267">Es wird Arbeit erstellt, um Artikel vom Kommissionierort zur Verpackungsstation zu bewegen.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-267">Work is created to move items from the picking location to the packing station.</span></span>

1. <span data-ttu-id="b0d1d-268">Wechseln Sie im Abschnitt **Auftragspositionen** zu **Lagerort \> Lieferdetails**.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-268">In the **Sales order lines** section, select **Warehouse \> Shipment details**.</span></span>
1. <span data-ttu-id="b0d1d-269">Notieren Sie sich auf der Seite **Lieferdetails** die Lieferungs-ID.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-269">On the **Shipment details** page, make a note of the shipment ID.</span></span> <span data-ttu-id="b0d1d-270">Sie benötigen sie, wenn Sie das Paket an der Verpackungsstation verpacken.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-270">You will need it when you pack the pack the shipment at the packing station.</span></span>
1. <span data-ttu-id="b0d1d-271">Schließen Sie die Seite **Lieferdetails**, um zum Auftrag zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-271">Close the **Shipment details** page to return to the sales order.</span></span>
1. <span data-ttu-id="b0d1d-272">Notieren Sie sich die Auftragsnummer und wechseln Sie dann zu **Lagerortverwaltung \> Arbeit \> Alle Arbeit**.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-272">Make a note of the sales order number, and then go to **Warehouse management \> Work \> All work**.</span></span>
1. <span data-ttu-id="b0d1d-273">Verwenden Sie die Auftragsnummer, um die Arbeit zu finden und auszuwählen, die für den Auftrag erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-273">Use the sales order number to find and select the work that was created for the order.</span></span>
1. <span data-ttu-id="b0d1d-274">Wählen Sie im Aktionsbereich auf der Registerkarte **Arbeit** die Option **Arbeit abschließen** aus.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-274">On the Action Pane, on the **Work** tab, select **Complete work**.</span></span>
1. <span data-ttu-id="b0d1d-275">Wählen Sie auf der Seite **Arbeitsabschluss** im Feld **Benutzer-ID** eine Benutzer-ID aus.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-275">On the **Work completion** page, in the **User ID** field, select a user ID.</span></span> <span data-ttu-id="b0d1d-276">Wählen Sie im Aktionsbereich **Arbeit überprüfen** aus.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-276">Then, on the Action Pane, select **Validate work**.</span></span>
1. <span data-ttu-id="b0d1d-277">Bei einer erfolgreichen Prüfung wählen Sie im Aktionsbereich **Arbeit abschließen** aus.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-277">If the work passes validation, select **Complete work** on the Action Pane.</span></span>

    <span data-ttu-id="b0d1d-278">Die Arbeit wird als abgeschlossen markiert, um die Bewegung von Artikeln zur Verpackungsstation zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-278">The work is marked as completed to simulate the movement of items to the packing station.</span></span>

#### <a name="pack-the-shipment"></a><span data-ttu-id="b0d1d-279">Verpacken der Lieferung</span><span class="sxs-lookup"><span data-stu-id="b0d1d-279">Pack the shipment</span></span>

<span data-ttu-id="b0d1d-280">Gehen Sie folgendermaßen vor, um die Lieferung zu verpacken.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-280">Follow these steps to pack the shipment.</span></span>

1. <span data-ttu-id="b0d1d-281">Wechseln Sie zu **Lagerortverwaltung \> Einrichten \> Arbeitskraft** und stellen Sie sicher, dass Ihr Benutzerkonto einem Arbeitskraftkonto für die Lagerortverwaltung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-281">Go to **Warehouse management \> Setup \> Worker**, and make sure that your user account is associated with a worker account for warehouse management.</span></span>
1. <span data-ttu-id="b0d1d-282">WechselnWarehouse Management Solution Sie zu **Lagerortverwaltung \> Kommissionierung und Containerisierung \> Paket**.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-282">Go to **Warehouse management \> Picking and containerization \> Pack**.</span></span>
1. <span data-ttu-id="b0d1d-283">Legen Sie im Dialogfeld **Verpackungsstation auswählen** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="b0d1d-283">In the **Select packing station** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b0d1d-284">**Standort:** *6*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-284">**Site:** *6*</span></span>
    - <span data-ttu-id="b0d1d-285">**Lagerort:** *62*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-285">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="b0d1d-286">**Lagerplatz:** *Verpackung*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-286">**Location:** *Pack*</span></span>
    - <span data-ttu-id="b0d1d-287">**Verpackungsprofilkennung:** *Demoverpackungsprofil*</span><span class="sxs-lookup"><span data-stu-id="b0d1d-287">**Packing profile ID:** *Demo packing profile*</span></span>

1. <span data-ttu-id="b0d1d-288">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-288">Select **OK**.</span></span>
1. <span data-ttu-id="b0d1d-289">Die Seite **Paket** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-289">The **Pack** page appears.</span></span> <span data-ttu-id="b0d1d-290">In einem Produktionsszenario scannt eine Arbeitskraft ein Kennzeichen oder eine Lieferungs-ID.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-290">In a production scenario, a worker will scan a license plate or shipment ID.</span></span> <span data-ttu-id="b0d1d-291">Öffnen Sie für dieses Szenario jedoch die Seite **Alle Lieferungen** und suchen Sie die Liefernummer für die Lieferung, die Sie gerade erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-291">However, for this scenario, open the **All shipments** page, and look up the shipment number for the shipment that you just created.</span></span> <span data-ttu-id="b0d1d-292">Geben Sie dann diesen Wert in das Feld **Kennzeichen oder Lieferung** auf der Seite **Paket** ein.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-292">Then enter this value in the **License plate or shipment** field on the **Pack** page.</span></span> <span data-ttu-id="b0d1d-293">Geben Sie alternativ die Lieferungs-ID ein, die Sie zuvor notiert haben.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-293">Alternatively, enter the shipment ID that you made a note of earlier.</span></span>
1. <span data-ttu-id="b0d1d-294">Wählen Sie im Aktivitätsbereich **Neuer Container** aus.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-294">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="b0d1d-295">Das angezeigte Dialogfeld zeigt Details zum neuen Container an.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-295">The dialog box that appears shows details about the new container.</span></span> <span data-ttu-id="b0d1d-296">Behalten Sie die Standardwerte bei und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-296">Leave the default values, and then select **OK**.</span></span>
1. <span data-ttu-id="b0d1d-297">Wählen Sie auf der Seite **Paket** im Inforegister **Artikelverpackung** im Feld **Kennung** den Wert *A0002* aus, um den Artikel zu verpacken.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-297">On the **Pack** page, on the **Item packing** FastTab, in the **Identifier** field, select *A0002* to pack that item.</span></span> <span data-ttu-id="b0d1d-298">Der Artikel wird dem Container hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-298">The item is added to the container.</span></span>
1. <span data-ttu-id="b0d1d-299">Wählen Sie im Aktionsbereich **Container für Lieferung** aus.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-299">On the Action Pane, select **Containers for shipment**.</span></span>

    <span data-ttu-id="b0d1d-300">Die angezeigte Seite **Container für Lieferung** enthält eine Zeile für den Container, den Sie gerade erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-300">The **Containers for shipment** page that appears has a row for the container that you just created.</span></span> <span data-ttu-id="b0d1d-301">Das Feld **Containermanifestierungs-ID** in dieser Zeile ist derzeit jedoch leer, da Sie das Adressetikett und die Sendungsverfolgungsnummer noch nicht vom Spediteur erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-301">However, the **Container manifest ID** field in that row is currently blank, because you haven't yet received the shipping label and tracking number from the carrier.</span></span>

1. <span data-ttu-id="b0d1d-302">Wählen Sie im Aktivitätsbereich **Container schließen** aus.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-302">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="b0d1d-303">Legen Sie im Dialogeld **Container schließen** das Feld **Bruttogewicht** auf *1 kg* fest und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-303">In the **Close container** dialog box, set the **Gross weight** field to *1 kg*, and then select **OK**.</span></span>

    <span data-ttu-id="b0d1d-304">Das Adressetikett sollte jetzt auf dem zuvor ausgewählten ZPL-Drucker gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-304">The shipping label should now be printed on the ZPL printer that you selected earlier.</span></span> <span data-ttu-id="b0d1d-305">Es sollte dem folgenden Beispiel ähneln.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-305">It should resemble the following example.</span></span>

    <span data-ttu-id="b0d1d-306">![Beispieladressetikett](media/sps-label-example.png "Beispieladressetikett")</span><span class="sxs-lookup"><span data-stu-id="b0d1d-306">![Example shipping label](media/sps-label-example.png "Example shipping label")</span></span>

1. <span data-ttu-id="b0d1d-307">Beachten Sie, dass die Werte für **Containermanifestierungs-ID** und **Gesamtfracht** als vom Spediteur erhalten hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="b0d1d-307">Notice that the **Container manifest ID** and **Total freight** values have been added as received from the carrier.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]