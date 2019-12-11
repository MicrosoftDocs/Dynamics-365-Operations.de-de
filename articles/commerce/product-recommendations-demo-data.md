---
title: Abrufen von Produktempfehlungen mithilfe von Demodaten
description: Dieses Dokument bietet Richtlinien zur Nutzung von Mehrkanal-Produktempfehlungen in einer Einfeldumgebung der Stufe 1 mithilfe der vorinstallierten, anpassbaren Demodaten.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: af8a30e69d9ed143e045950efdcece207f6da14c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697933"
---
# <a name="get-product-recommendations-using-demo-data"></a><span data-ttu-id="17fc4-103">Abrufen von Produktempfehlungen mithilfe von Demodaten</span><span class="sxs-lookup"><span data-stu-id="17fc4-103">Get product recommendations using demo data</span></span>
<span data-ttu-id="17fc4-104">Dieses Dokument bietet Richtlinien zur Nutzung von Mehrkanal-Produktempfehlungen in einer Einfeldumgebung der Stufe 1 mithilfe der vorinstallierten, anpassbaren Demodaten.</span><span class="sxs-lookup"><span data-stu-id="17fc4-104">This document provides guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="17fc4-105">Mehrkanal-Produktempfehlungen bieten eine Reihe von redaktionell kuratierten oder programmatisch erstellten Produktlisten.</span><span class="sxs-lookup"><span data-stu-id="17fc4-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated list of products.</span></span> <span data-ttu-id="17fc4-106">Diese Liste kann in einigen Szenarien je nach Geschäftsanforderung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="17fc4-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="17fc4-107">Weitere Informationen zu Produktempfehlungslisten finden Sie im [Produktempfehlungsüberblick](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="17fc4-107">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

<span data-ttu-id="17fc4-108">Für Stufe 2 und höhere Dynamics 365-Umgebungen werden Produktempfehlungen automatisch basierend auf Kundendaten berechnet.</span><span class="sxs-lookup"><span data-stu-id="17fc4-108">For Tier-2 and higher Dynamics 365 environments, product recommendations are automatically computed based on customer data.</span></span> <span data-ttu-id="17fc4-109">Das Verwenden der Empfehlungsdemodaten deaktiviert keine Produktempfehlungslösung, die bereits in der Umgebung ist und keine der seiner Nutzung zugeordneten Kosten.</span><span class="sxs-lookup"><span data-stu-id="17fc4-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="17fc4-110">Bei Umgebungen der Stufe 1 basieren Produktempfehlungen nur auf den statischen Demodaten, die in einer .csv-Datei gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="17fc4-110">For Tier-1 environments, product recommendations are based only off the static demo data stored in a .csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="17fc4-111">Aktivieren von Produktempfehlungsdemodaten in einer Umgebung</span><span class="sxs-lookup"><span data-stu-id="17fc4-111">Enabling product recommendations demo data in an environment</span></span>
<span data-ttu-id="17fc4-112">Um Demo-Daten für Produktempfehlungen zu aktivieren, müssen Sie die Dynamics 365 Commerce-Vorschau-Demoerweiterung für die entsprechende Umgebung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="17fc4-112">To enable product recommensations demo date, you need to deploy the Dynamics 365 Commerce Preview Demo Extension to the respective environment.</span></span> <span data-ttu-id="17fc4-113">Wenn Sie dies automatisch tun, werden Demo-Daten für Produktempfehlungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="17fc4-113">Doing so automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="17fc4-114">Standarddemodaten</span><span class="sxs-lookup"><span data-stu-id="17fc4-114">Default demo data</span></span>
<span data-ttu-id="17fc4-115">Jede Einzelfeld-Typumgebung verfügt über einen Satz vorab installierter Produktempfehlungsdemodaten, die in der Koma getrennten Datei „reco_demo_data.csv“ auf Retail Server gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="17fc4-115">Each Onebox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated ‘reco_demo_data.csv’ file, located on the Retail Server.</span></span>

<span data-ttu-id="17fc4-116">Die Daten werden in den folgenden Spalten strukturiert.</span><span class="sxs-lookup"><span data-stu-id="17fc4-116">The data is structured along the following columns.</span></span>

| <span data-ttu-id="17fc4-117">Spaltenname</span><span class="sxs-lookup"><span data-stu-id="17fc4-117">Column name</span></span>         | <span data-ttu-id="17fc4-118">Obligatorisch</span><span class="sxs-lookup"><span data-stu-id="17fc4-118">Mandatory</span></span>          | <span data-ttu-id="17fc4-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17fc4-119">Description</span></span>                                                                                                                                 | <span data-ttu-id="17fc4-120">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="17fc4-120">Possible Values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="17fc4-121">RecoList</span><span class="sxs-lookup"><span data-stu-id="17fc4-121">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="17fc4-123">Der bestimmte Produktempfehlungslistentyp, den der Demodatenpunkt generieren soll.</span><span class="sxs-lookup"><span data-stu-id="17fc4-123">The specific product recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="17fc4-124">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="17fc4-124">RecoBestSelling</span></span></li><li><span data-ttu-id="17fc4-125">RecoNew</span><span class="sxs-lookup"><span data-stu-id="17fc4-125">RecoNew</span></span></li><li><span data-ttu-id="17fc4-126">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="17fc4-126">RecoTrending</span></span></li><li><span data-ttu-id="17fc4-127">RecoCart</span><span class="sxs-lookup"><span data-stu-id="17fc4-127">RecoCart</span></span></li><li><span data-ttu-id="17fc4-128">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="17fc4-128">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="17fc4-129">OperatingUnitNumber</span><span class="sxs-lookup"><span data-stu-id="17fc4-129">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="17fc4-131">Die bestimmte Organisationseinheitsnummer, in der Produktempfehlungen angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="17fc4-131">The specific operating unit number where product recommendations are expected to be   surfaced.</span></span>                                        |                                                                              |
| <span data-ttu-id="17fc4-132">Kategorie</span><span class="sxs-lookup"><span data-stu-id="17fc4-132">Category</span></span>            |                    |    <span data-ttu-id="17fc4-133">Die Kategorie, für die die bestimmte Liste zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="17fc4-133">The category the specific list should be returned for.</span></span> <span data-ttu-id="17fc4-134">Wenn keine Kategorie angegeben wird, gilt die Liste nur für den Anfang der Navigationshierarchie.</span><span class="sxs-lookup"><span data-stu-id="17fc4-134">If no category is specified, the list is for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="17fc4-135">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="17fc4-135">SeedItemId</span></span>          |                    |    <span data-ttu-id="17fc4-136">Für Listen, für die ein Seed (RecoPeopleAlsoBuy und RecoCart) erforderlich ist, ist es das Produkt, für das diese Listen weitere Produkte anzeigen sollten.</span><span class="sxs-lookup"><span data-stu-id="17fc4-136">For lists that require seed (RecoPeopleAlsoBuy and RecoCart), the product those lists should show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="17fc4-137">ItemIds</span><span class="sxs-lookup"><span data-stu-id="17fc4-137">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="17fc4-139">Mindestens ein Produkt, das als Ergebnis durch „;“ getrennt zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="17fc4-139">One or more products to be returned as the result, separated by ‘;’.</span></span>                                                                  |                                                                              |

## <a name="customize-demo-data"></a><span data-ttu-id="17fc4-140">Demodaten anpassen</span><span class="sxs-lookup"><span data-stu-id="17fc4-140">Customize demo data</span></span>
<span data-ttu-id="17fc4-141">Sie können die Standarddemodaten mit sämtlichen Produkt und Kategorieinformationen bearbeiten, die in der Hauptniederlassung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="17fc4-141">You can edit the default demo data with any product and category information configured in HQ.</span></span> <span data-ttu-id="17fc4-142">Sobald Sie die .csv aktualisiert haben, werden die Produktempfehlungen, die den Kunden zurückgesendet werden, diese Änderungen wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="17fc4-142">Once you update the .csv, the product recommendations that are returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="17fc4-143">Die Erweiterung enthält die Datendatei „RecoMockDataset.csv“, mit der Sie den Datensatz für die Scheinempfehlungsergebnisse steuern können.</span><span class="sxs-lookup"><span data-stu-id="17fc4-143">The extension contains a datafile called 'RecoMockDataset.csv' which allows you to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="17fc4-144">Der Dateiname kann über die Erweiterungskonfiguration mithilfe der Einstellung **ext.Recommendations.DemoFilePath** gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="17fc4-144">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="17fc4-145">Damit können Sie über mehrere Datasets verfügen, zwischen denen durch Konfiguration leicht gewechselt werden kann.</span><span class="sxs-lookup"><span data-stu-id="17fc4-145">This enables you to have multiple datasets available that can be switched between easily through configuration.</span></span>


```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a><span data-ttu-id="17fc4-146">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="17fc4-146">Additional Resources</span></span>

[<span data-ttu-id="17fc4-147">Überblick über Produktempfehlungen</span><span class="sxs-lookup"><span data-stu-id="17fc4-147">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="17fc4-148">Umgebungsplanung</span><span class="sxs-lookup"><span data-stu-id="17fc4-148">Environment planning</span></span>](../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)
