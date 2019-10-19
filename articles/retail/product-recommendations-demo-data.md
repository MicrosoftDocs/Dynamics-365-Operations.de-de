---
title: Omni-Channel-Produkt-Empfehlungsdemodaten
description: Dieses Dokument bietet Richtlinien zur Nutzung von Omni-Channel-Produktempfehlungen in einer Einfeldumgebung der Stufe 1 mithilfe der vorinstallierten, anpassbaren Demodaten.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 81af4c1bb7828c9b346a3ef514d8657e853dcefb
ms.sourcegitcommit: c526cfd1f823df1ff33ded95e599a72f0a15cc5a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2225955"
---
# <a name="omni-channel-product-recommendations-demo-data"></a><span data-ttu-id="443f0-103">Omni-Channel-Produkt-Empfehlungsdemodaten</span><span class="sxs-lookup"><span data-stu-id="443f0-103">Omni-channel product recommendations demo data</span></span>

<span data-ttu-id="443f0-104">Dieses Dokument bietet Richtlinien zur Nutzung von Omni-Channel-Produktempfehlungen in einer Einfeldumgebung der Stufe 1 mithilfe der vorinstallierten, anpassbaren Demodaten.</span><span class="sxs-lookup"><span data-stu-id="443f0-104">This document aims to provide guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="443f0-105">Omni-Channel-Produktempfehlungen bieten einen Satz redaktionell zusammengestellter oder programmgesteuert generierter geordneter Liste von Produkten.</span><span class="sxs-lookup"><span data-stu-id="443f0-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated ordered list of products.</span></span> <span data-ttu-id="443f0-106">Diese Liste kann in einigen Szenarien je nach Geschäftsanforderung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="443f0-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="443f0-107">Weitere Informationen zu Produktempfehlungslisten finden Sie im [Produktempfehlungsüberblick](product-recommendaitons-overview.md).</span><span class="sxs-lookup"><span data-stu-id="443f0-107">For more information about product recommendation lists, see [Product recommendations overview.](product-recommendaitons-overview.md)</span></span>

<span data-ttu-id="443f0-108">Für Stufe 2 und höhere Dynamics-Umgebungen werden Produktempfehlungen automatisch basierend auf Kundendaten berechnet.</span><span class="sxs-lookup"><span data-stu-id="443f0-108">For Tier-2 and higher Dynamics Environments product recommendations are automatically computed based on customer data.</span></span>
<span data-ttu-id="443f0-109">Das Verwenden der Empfehlungsdemodaten deaktiviert keine Produktempfehlungslösung, die bereits in der Umgebung ist und keine der seiner Nutzung zugeordneten Kosten.</span><span class="sxs-lookup"><span data-stu-id="443f0-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="443f0-110">Bei Umgebungen der Stufe 1 basieren Produktempfehlungen nur auf den statischen Demodaten, die in einer csv-Datei gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="443f0-110">For Tier-1 environments product recommendations are based only off the static demo data stored in a csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="443f0-111">Aktivieren von Produktempfehlungsdemodaten in einer Umgebung</span><span class="sxs-lookup"><span data-stu-id="443f0-111">Enabling product recommendations demo data in an environment</span></span>

<span data-ttu-id="443f0-112">Debitoren müssen die **Dynamics 365 Commerce-Vorschaudemoerweiterung** in der entsprechenden Umgebung bereitstellen, die automatisch Produktempfehlungsdemodaten aktiviert.</span><span class="sxs-lookup"><span data-stu-id="443f0-112">Customers need to deploy the **Dynamics 365 Commerce Preview Demo Extension** to the respective environment, which automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="443f0-113">Standarddemodaten</span><span class="sxs-lookup"><span data-stu-id="443f0-113">Default demo data</span></span>
<span data-ttu-id="443f0-114">Jede Einzelfeld-Typumgebung verfügt über einen Satz vorab installierter Produktempfehlungsdemodaten, die in der Koma getrennten Datei **„reco_demo_data.csv“** im gleichen Ordner wie das Dokument auf Retail Server gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="443f0-114">Each Onebox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated **‘reco_demo_data.csv’** file, located in the same folder as this document on Retail Server.</span></span>

<span data-ttu-id="443f0-115">Diese Daten werden in den folgenden Spalten strukturiert</span><span class="sxs-lookup"><span data-stu-id="443f0-115">This data is structured along the following columns</span></span>

| <span data-ttu-id="443f0-116">Spaltenname</span><span class="sxs-lookup"><span data-stu-id="443f0-116">Column name</span></span>         | <span data-ttu-id="443f0-117">Obligatorisch</span><span class="sxs-lookup"><span data-stu-id="443f0-117">Mandatory</span></span>          | <span data-ttu-id="443f0-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="443f0-118">Description</span></span>                                                                                                                                 | <span data-ttu-id="443f0-119">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="443f0-119">Possible Values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="443f0-120">RecoList</span><span class="sxs-lookup"><span data-stu-id="443f0-120">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="443f0-122">Der bestimmte Produktempfehlungslistentyp, den der Demodatpunkt generieren soll.</span><span class="sxs-lookup"><span data-stu-id="443f0-122">The specific product   recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="443f0-123">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="443f0-123">RecoBestSelling</span></span></li><li><span data-ttu-id="443f0-124">RecoNew</span><span class="sxs-lookup"><span data-stu-id="443f0-124">RecoNew</span></span></li><li><span data-ttu-id="443f0-125">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="443f0-125">RecoTrending</span></span></li><li><span data-ttu-id="443f0-126">RecoCart</span><span class="sxs-lookup"><span data-stu-id="443f0-126">RecoCart</span></span></li><li><span data-ttu-id="443f0-127">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="443f0-127">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="443f0-128">OperatingUnitNumber</span><span class="sxs-lookup"><span data-stu-id="443f0-128">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="443f0-130">Die bestimmte Organisationseinheitsnummer, in der Produktempfehlungen auftauchen sollen.</span><span class="sxs-lookup"><span data-stu-id="443f0-130">The specific   operating unit number where product recommendations are expected to be   surfaced in.</span></span>                                        |                                                                              |
| <span data-ttu-id="443f0-131">Kategorie</span><span class="sxs-lookup"><span data-stu-id="443f0-131">Category</span></span>            |                    |    <span data-ttu-id="443f0-132">Die Kategorie, für die die bestimmte Liste zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="443f0-132">The category the   specific list should be returned for.</span></span> <span data-ttu-id="443f0-133">Wenn keine Kategorie angegeben wird, gilt die Liste nur für den Anfang der Navigationshierarchie.</span><span class="sxs-lookup"><span data-stu-id="443f0-133">If no category is specified, list is   for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="443f0-134">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="443f0-134">SeedItemId</span></span>          |                    |    <span data-ttu-id="443f0-135">Für Listen, für die ein Seed (RecoPeopleAlsoBuy und RecoCart) erforderlich ist, ist es das Produkt, für das diese Listen weitere Produkte anzeigen sollten.</span><span class="sxs-lookup"><span data-stu-id="443f0-135">For lists that   require seed (RecoPeopleAlsoBuy and RecoCart) the product those lists should   show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="443f0-136">ItemIds</span><span class="sxs-lookup"><span data-stu-id="443f0-136">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="443f0-138">Mindestens ein Produkt, das als Ergebnis durch **„;“** getrennt zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="443f0-138">One or more products   to be returned as the result, separated by **‘;’**.</span></span>                                                                  |                                                                              |


## <a name="customize-demo-data"></a><span data-ttu-id="443f0-139">Demodaten anpassen</span><span class="sxs-lookup"><span data-stu-id="443f0-139">Customize demo data</span></span>
<span data-ttu-id="443f0-140">Debitoren können die Standarddemodaten mit sämtlichen Produkt und Kategorieinformationen bearbeiten, die in der Hauptniederlassung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="443f0-140">Customers can edit the default demo data with any product and category information that is configured in HQ.</span></span> <span data-ttu-id="443f0-141">Sobald die CSV aktualisiert wird, werden die Produktempfehlungen, die den Kunden zurückgesendet werden, diese Änderungen wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="443f0-141">Once the CSV is updated, the Product Recommendations returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="443f0-142">Die Erweiterung enthält die Datendatei RecoMockDataset.csv, mit der ein Debitor den Datensatz für die Scheinempfehlungsergebnisse steuern kann.</span><span class="sxs-lookup"><span data-stu-id="443f0-142">The extension contains a datafile called RecoMockDataset.csv which allows the customer to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="443f0-143">Der Dateiname kann über die Erweiterungskonfiguration mithilfe der Einstellung **ext.Recommendations.DemoFilePath** gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="443f0-143">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="443f0-144">Damit können die Kunden über mehrere Datasets verfügen, zwischen denen durch Konfiguration leicht gewechselt werden kann.</span><span class="sxs-lookup"><span data-stu-id="443f0-144">This enables the customers to have multiple datasets available that can be switched between easily through configuration.</span></span>

```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a><span data-ttu-id="443f0-145">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="443f0-145">Additional resources</span></span>

[<span data-ttu-id="443f0-146">Produktempfehlungsübersicht</span><span class="sxs-lookup"><span data-stu-id="443f0-146">Product recommendations overview</span></span>](product-recommendations-overview.md)

[<span data-ttu-id="443f0-147">Umgebungsplanung</span><span class="sxs-lookup"><span data-stu-id="443f0-147">Environment planning</span></span>](environment-planning.md)
