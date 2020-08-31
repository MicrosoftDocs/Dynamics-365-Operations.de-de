---
title: Erweitern vorhandener Dateneinheiten
description: In diesem Thema finden Sie ein Beispiel, das zeigt, wie Sie den Ansichten INVENTORSITEONHANDENTITY und INVENTWAREHOUSEONHANDENTITY erweiterte Felder hinzufügen, damit die Funktionen der Inventardateneinheiten mit den Erweiterungen arbeiten können.
author: sherry-zheng
manager: tfehr
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-27
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e3bf3a7d48b0aa3e48845882be0ee86da17ed040
ms.sourcegitcommit: e276348a63bfdb9e712c0ea86e6c2a68c50872c0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2020
ms.locfileid: "3665403"
---
# <a name="extend-inventory-on-hand-data-entities"></a><span data-ttu-id="f83d1-103">Erweitern vorhandener Dateneinheiten</span><span class="sxs-lookup"><span data-stu-id="f83d1-103">Extend inventory on-hand data entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f83d1-104">Microsoft Dynamics 365 Supply Chain Management bietet die Funktionen von [Erweiterbarkeit](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md), mit denen Sie [Felder durch Erweiterung in Tabellen einfügen](../../fin-ops-core/dev-itpro/extensibility/add-field-extension) können.</span><span class="sxs-lookup"><span data-stu-id="f83d1-104">Microsoft Dynamics 365 Supply Chain Management provides [extensibility](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) features that let you [add fields to tables through extension](../../fin-ops-core/dev-itpro/extensibility/add-field-extension).</span></span> <span data-ttu-id="f83d1-105">In diesem Thema finden Sie ein Beispiel, das zeigt, wie Sie den Ansichten `INVENTORSITEONHANDENTITY` und `INVENTWAREHOUSEONHANDENTITY` erweiterte Felder hinzufügen, damit die Funktionen der Inventardateneinheiten mit den Erweiterungen arbeiten können.</span><span class="sxs-lookup"><span data-stu-id="f83d1-105">This topic provides an example that shows how to add extended fields to the `INVENTORSITEONHANDENTITY` and `INVENTWAREHOUSEONHANDENTITY` views, so that the capabilities of the inventory on-hand data entities can work with the extensions.</span></span> <span data-ttu-id="f83d1-106">Ausführliche Informationen zu Dateneinheiten finden Sie unter [Datenverwaltungsübersicht](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span><span class="sxs-lookup"><span data-stu-id="f83d1-106">For more information about data entities, see [Data management overview](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span></span>

> [!NOTE]
> <span data-ttu-id="f83d1-107">Hier ist eine Liste einiger verfügbarer Inventardateneinheiten:</span><span class="sxs-lookup"><span data-stu-id="f83d1-107">Here is a list of some of the inventory on-hand data entities:</span></span>
>
> - <span data-ttu-id="f83d1-108">Verfügbarer Lagerbestand nach Standort</span><span class="sxs-lookup"><span data-stu-id="f83d1-108">Inventory on-hand by site</span></span>
> - <span data-ttu-id="f83d1-109">Verfügbarer Lagerbestand nach Standort V2</span><span class="sxs-lookup"><span data-stu-id="f83d1-109">Inventory on-hand by site V2</span></span>
> - <span data-ttu-id="f83d1-110">Lagerbestand nach Lagerort</span><span class="sxs-lookup"><span data-stu-id="f83d1-110">Inventory on-hand by warehouse</span></span>
> - <span data-ttu-id="f83d1-111">Verfügbarer Lagerbestand nach Lagerort v2</span><span class="sxs-lookup"><span data-stu-id="f83d1-111">Inventory on-hand by warehouse v2</span></span>

<span data-ttu-id="f83d1-112">Nachdem Sie Tabellen Felder hinzugefügt haben, die von der Ansicht `inventSiteOnHandView` verwendet werden, muss der Engine synchronisiert werden, damit die Erweiterungen korrekt erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="f83d1-112">After you add fields to tables that are used by the `inventSiteOnHandView` view, you must sync the engine so that the extensions are correctly recognized.</span></span>

1. <span data-ttu-id="f83d1-113">Erweitern Sie die Ansicht `InventSiteOnHandView`, indem Sie das Erweiterungsfeld hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f83d1-113">Extend the `InventSiteOnHandView` view by adding the extension field.</span></span>
1. <span data-ttu-id="f83d1-114">Erweitern Sie die Ansicht `InventSiteOnHandAggregatedView` mit den Erweiterungsfeldern.</span><span class="sxs-lookup"><span data-stu-id="f83d1-114">Extend the `InventSiteOnHandAggregatedView` view with the extension fields.</span></span>
1. <span data-ttu-id="f83d1-115">Erweitern Sie die `InventSiteOnHandAggregatedViewBuilder`viewBuilder-Klasse durch Ändern der `getExtensionFields()`-Methode.</span><span class="sxs-lookup"><span data-stu-id="f83d1-115">Extend the `InventSiteOnHandAggregatedViewBuilder` viewBuilder class by modifying the `getExtensionFields()` method.</span></span> <span data-ttu-id="f83d1-116">Auf diese Weise ordnen Sie alte Ansichtsfelder neuen Ansichtsfeldern zu, wenn die viewBuilder-Synchronisierung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f83d1-116">In this way, you map old view fields to new view fields when viewBuilder synchronization is run.</span></span>

<span data-ttu-id="f83d1-117">Beispielsweise haben Sie die folgenden vier Felder durch Erweiterung in die Tabelle `InventTable` eingefügt:</span><span class="sxs-lookup"><span data-stu-id="f83d1-117">For example, you've added the following four fields to the `InventTable` table through extension:</span></span>

- <span data-ttu-id="f83d1-118">Benutzerdefiniertes Feld 1</span><span class="sxs-lookup"><span data-stu-id="f83d1-118">Custom field 1</span></span>
- <span data-ttu-id="f83d1-119">Benutzerdefiniertes Feld 2</span><span class="sxs-lookup"><span data-stu-id="f83d1-119">Custom field 2</span></span>
- <span data-ttu-id="f83d1-120">Benutzerdefiniertes Feld 3</span><span class="sxs-lookup"><span data-stu-id="f83d1-120">Custom field 3</span></span>
- <span data-ttu-id="f83d1-121">Benutzerdefiniertes Feld 4</span><span class="sxs-lookup"><span data-stu-id="f83d1-121">Custom field 4</span></span>

<span data-ttu-id="f83d1-122">In diesem Fall müssen Sie die Methode `getExtensionFields()` auf folgende Weise ändern.</span><span class="sxs-lookup"><span data-stu-id="f83d1-122">In the case, you must modify the `getExtensionFields()` method in the following way.</span></span>

```xpp
[ExtensionOf(classStr(InventSiteOnHandAggregatedViewBuilder))]
public final class InventOnHandAggregatedViewBuilder\_Extension
{
    protected Map getExtensionFields()
    {
        next getExtensionFields();
        Map extensionFields = new Map(Types::Int64, Types::Int64);
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 1), fieldNum(InventSiteOnHandAggregatedView, Custom field 1));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 2), fieldNum(InventSiteOnHandAggregatedView, Custom field 2));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 3), fieldNum(InventSiteOnHandAggregatedView, Custom field 3));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 4), fieldNum(InventSiteOnHandAggregatedView, Custom field 4));
        return extensionFields;
    }
}
```

<span data-ttu-id="f83d1-123">Nachdem Sie diese Schritte ausgeführt haben, können Sie den Lagerbestand nach Standort und den Lagerbestand nach Lagerdateneinheiten erweitern, indem Sie die neuen Felder hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f83d1-123">After you complete these steps, you can extend the inventory on-hand by site and inventory on-hand by warehouse data entities by adding the new fields.</span></span> <span data-ttu-id="f83d1-124">Auf diese Weise stellen Sie sicher, dass die erweiterten Felder während der Datenmigration, die diese Datenentitäten verwendet, erkannt und eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="f83d1-124">In this way, you ensure that the extended fields are recognized and included during data migration that uses those data entities.</span></span>
