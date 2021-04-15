---
title: Einzelhandelsshop wird nicht in der Liste an Shops angezeigt, in denen abgeholt werden kann
description: Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn ein Einzelhandelsshop nicht in der Liste der Shops aufgeführt ist, in denen Artikel abgeholt werden können.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 9974b3e10bbdcd2e8a8723a3be4b70401bb9e546
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801602"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a><span data-ttu-id="d996a-103">Einzelhandelsshop wird nicht in der Liste an Shops angezeigt, in denen abgeholt werden kann</span><span class="sxs-lookup"><span data-stu-id="d996a-103">Retail store doesn't appear in the list of stores to pick up from</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d996a-104">Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn ein Einzelhandelsshop nicht in der Liste der Shops aufgeführt ist, in denen Artikel abgeholt werden können.</span><span class="sxs-lookup"><span data-stu-id="d996a-104">This topic provides troubleshooting guidance that can help when a retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="description"></a><span data-ttu-id="d996a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d996a-105">Description</span></span>

<span data-ttu-id="d996a-106">Ein Einzelhandelsshop wird nicht in der Liste der Shops angezeigt, in denen Artikel abgeholt werden können.</span><span class="sxs-lookup"><span data-stu-id="d996a-106">A retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="resolution"></a><span data-ttu-id="d996a-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="d996a-107">Resolution</span></span>

### <a name="configure-the-longitude-and-latitude-for-the-store-address-in-commerce-headquarters"></a><span data-ttu-id="d996a-108">Den Längen- und Breitengrad für die Shopadresse in der Commerce-Zentralverwaltung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="d996a-108">Configure the longitude and latitude for the store address in Commerce headquarters</span></span>

<span data-ttu-id="d996a-109">Befolgen Sie diese Schritte, um den Längen- und Breitengrad für die Shopadresse in der Commerce-Zentralverwaltung zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d996a-109">To configure the longitude and latitude for the store address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="d996a-110">Rufen Sie **Retail und Commerce \> Kanäle \> Shops \> Alle Shops** auf.</span><span class="sxs-lookup"><span data-stu-id="d996a-110">Go to **Retail and Commerce \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="d996a-111">Suchen Sie das Geschäft, das in den Abholoptionen auf der E-Commerce-Website angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d996a-111">Find the store that you want to appear among the pickup options on the e-commerce site.</span></span> <span data-ttu-id="d996a-112">Notieren Sie sich den Wert seiner **Organisationseinheit**.</span><span class="sxs-lookup"><span data-stu-id="d996a-112">Make a note of its **Operating unit number** value.</span></span>
1. <span data-ttu-id="d996a-113">Rufen Sie **Organisationsverwaltung \> Organisationen \> Organisationseinheiten** auf.</span><span class="sxs-lookup"><span data-stu-id="d996a-113">Go to **Organization administration \> Organizations \> Operating units**.</span></span>
1. <span data-ttu-id="d996a-114">Suchen Sie nach der Nummer der Organisationseinheit, die Sie zuvor notiert haben, und wählen Sie dann die Organisationseinheit in den Suchergebnissen aus.</span><span class="sxs-lookup"><span data-stu-id="d996a-114">Search for the operating unit number that you noted earlier, and then select the operating unit in the search results.</span></span>
1. <span data-ttu-id="d996a-115">Wählen Sie im Inforegister **Adressen** **Weitere Optionen** und anschließend **Erweitert** aus.</span><span class="sxs-lookup"><span data-stu-id="d996a-115">On the **Addresses** FastTab, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="d996a-116">Vergewissern Sie sich, dass im Inforegister **Allgemein** die Felder **Längengrad** und **Breitengrad** korrekt eingestellt sind.</span><span class="sxs-lookup"><span data-stu-id="d996a-116">On the **General** FastTab, make sure that the **Longitude** and **Latitude** fields are correctly set.</span></span> <span data-ttu-id="d996a-117">Vergewissern Sie sich, dass im Rahmen dieses Schritts die Werte korrekt als positive oder negative Zahlen angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="d996a-117">As part of this step, make sure that the values are correctly specified as positive or negative numbers.</span></span>

### <a name="configure-fulfillment-groups-in-commerce-headquarters"></a><span data-ttu-id="d996a-118">Erfüllungsgruppen in der Commerce-Zentralverwaltung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="d996a-118">Configure fulfillment groups in Commerce headquarters</span></span>

<span data-ttu-id="d996a-119">Befolgen Sie diese Schritte, um Erfüllungsgruppen in der Commerce-Zentralverwaltung zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d996a-119">To configure fulfillment groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="d996a-120">Rufen Sie **Retail und Commerce \> Kanäle \> Onlineshops** auf.</span><span class="sxs-lookup"><span data-stu-id="d996a-120">Go to **Retail and Commerce \> Channels \> Online stores**.</span></span>
1. <span data-ttu-id="d996a-121">Wählen Sie den zu konfigurierenden Onlineshop aus.</span><span class="sxs-lookup"><span data-stu-id="d996a-121">Select the online store to configure.</span></span>
1. <span data-ttu-id="d996a-122">Wählen Sie im Aktionsbereich die Option **Einrichten** und anschließend **Erfüllungsgruppenzuweisung** aus.</span><span class="sxs-lookup"><span data-stu-id="d996a-122">On the Action Pane, select **Set up**, and then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="d996a-123">Wählen Sie auf der Seite **Erfüllungsgruppenzuweisung** die Erfüllungsgruppe für den Onlineshop aus.</span><span class="sxs-lookup"><span data-stu-id="d996a-123">On the **Fulfillment group assignment** page, select the fulfillment group for the online store.</span></span>
1. <span data-ttu-id="d996a-124">Vergewissern Sie sich, dass das Einzelhandelsgeschäft unter **Einrichtung** korrekt für die Erfüllungsgruppe konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="d996a-124">Under **Setup**, make sure that the retail store is correctly configured for the fulfillment group.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d996a-125">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d996a-125">Additional resources</span></span> 

[<span data-ttu-id="d996a-126">Erstellen einer Organisationseinheit</span><span class="sxs-lookup"><span data-stu-id="d996a-126">Create an operating unit</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit)

[<span data-ttu-id="d996a-127">Einen Onlinechannel einrichten</span><span class="sxs-lookup"><span data-stu-id="d996a-127">Set up an online channel</span></span>](../channel-setup-online.md)
