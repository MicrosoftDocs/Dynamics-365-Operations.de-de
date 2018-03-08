---
title: "Externe Kataloge für PunchOut eProcurement verwenden"
description: "In diesem Thema wird erläutert, wie Sie externe Kataloge verwenden können, um Anforderungen zu erstellen und zu senden."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: 76d0c911bdddbc5a34644dc96ec13dd8fd53a338
ms.contentlocale: de-de
ms.lasthandoff: 03/07/2018

---

# <a name="use-external-catalogs-for-punchout-eprocurement"></a><span data-ttu-id="6f5ef-103">Externe Kataloge für PunchOut eProcurement verwenden</span><span class="sxs-lookup"><span data-stu-id="6f5ef-103">Use external catalogs for PunchOut eProcurement</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6f5ef-104">Wenn Sie externe Kataloge für PunchOut E-Procurement verwenden, müssen Sie Informationen zu den Produkten Ihrer Kreditoren in den eigenen Masterdaten nicht verwaltet.</span><span class="sxs-lookup"><span data-stu-id="6f5ef-104">By using external catalogs for PunchOut e-procurement, you don't have to maintain information about your vendors' products in your own master data.</span></span> <span data-ttu-id="6f5ef-105">Stattdessen wird der Einkaufskorb auf der Website des Kreditors auf Anforderungspositionen konvertiert, die die korrekte Produktinformationen haben.</span><span class="sxs-lookup"><span data-stu-id="6f5ef-105">Instead, the shopping cart on a vendor's website is converted to requisition lines that have the correct product information.</span></span> 

<span data-ttu-id="6f5ef-106">Sie sollten die Verwaltung von Beschreibungen und Preisen der Produkte der Kreditoren in den eigenen Produktmasterdaten vermeiden.</span><span class="sxs-lookup"><span data-stu-id="6f5ef-106">You should avoid maintaining the descriptions and prices of your vendors’ products in your own product master data.</span></span> <span data-ttu-id="6f5ef-107">Nutzen Sie stattdessen externe Kataloge für PunchOut E-Procurement.</span><span class="sxs-lookup"><span data-stu-id="6f5ef-107">Instead, use external catalogs for PunchOut e-procurement.</span></span> <span data-ttu-id="6f5ef-108">Wenn Mitarbeiter Anforderungen erstellen, können sie auf die externe Katalogwebsite eines Kreditors zugreifen (das heißt, wenn sie das System verlassen und auf die Seite des Kreditors gehen).</span><span class="sxs-lookup"><span data-stu-id="6f5ef-108">Then, when employees create requisitions, they can “punch out” to a vendor’s external catalog site (in other words, they leave your system and go to the vendor’s site).</span></span> <span data-ttu-id="6f5ef-109">Die Produkte, die dem Einkaufskorb auf der Website des Kreditors hinzugefügt werden, können auf dann in Anforderungspositionen konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="6f5ef-109">The products that are added to the shopping cart on the vendor’s website can then be converted to requisition lines.</span></span> <span data-ttu-id="6f5ef-110">Deshalb erhalten Sie die korrekten Produktinformationen ab: Produktkennung, Name, Preis, usw.</span><span class="sxs-lookup"><span data-stu-id="6f5ef-110">Therefore, you get the correct product information: product ID, name, price, and so on.</span></span>

<span data-ttu-id="6f5ef-111">Wenn Sie externe Kataloge verwenden, muss ein Mitarbeiter die Anforderung auf der Seite **Eigene Bestellanforderungen** erstellen.</span><span class="sxs-lookup"><span data-stu-id="6f5ef-111">To use external catalogs, an employee must create a requisition on the **My purchase requisitions** page.</span></span>

<span data-ttu-id="6f5ef-112">Der Mitarbeiter, der eine Bestellanforderung erstellt, ist der Antragsteller der Bestellanforderung.</span><span class="sxs-lookup"><span data-stu-id="6f5ef-112">The employee who creates a requisition is referred to as the preparer of the requisition.</span></span> <span data-ttu-id="6f5ef-113">Als Antragsteller können Sie die folgenden Aufgaben durchführen.</span><span class="sxs-lookup"><span data-stu-id="6f5ef-113">As a preparer, you can complete the following tasks.</span></span>

<span data-ttu-id="6f5ef-114">Verwenden Sie die **Externe Kataloge** Positionsaktivität, um eine Seite zu öffnen, die alle externen Kataloge enthält, die für die jeweilige anfordernde Person, die einkaufende juristische Person und die empfangende Organisationseinheit verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="6f5ef-114">Use the **External catalogs** line action to open a page that includes all external catalogs that are available for the specified requester, buying legal entity, and receiving operating unit.</span></span>

<span data-ttu-id="6f5ef-115">Abhängig von Ihren Berechtigungen ändern Sie die anfordernde Person, die juristische Person und die empfangende Organisationseinheit.</span><span class="sxs-lookup"><span data-stu-id="6f5ef-115">Depending on your permissions, change the requester, buying legal entity, and receiving operating unit.</span></span> <span data-ttu-id="6f5ef-116">Eine Änderung in diesen Werten ändert möglicherweise die Liste der externen Kataloge, die für eine anfordernde Person bereitstehen.</span><span class="sxs-lookup"><span data-stu-id="6f5ef-116">A change in those values might change the list of external catalogs that are available to a requester.</span></span> <span data-ttu-id="6f5ef-117">Die externen Kataloge, die verfügbar sind, hängen von der aktuellen aktiven Einkaufsrichtlinien für die kaufende juristische Person und die empfangende Organisationseinheit ab.</span><span class="sxs-lookup"><span data-stu-id="6f5ef-117">The external catalogs that are available depend on the current active purchasing policies for the buying legal entity or the receiving operating unit.</span></span> <span data-ttu-id="6f5ef-118">Diese Richtlinie kann Zugriffe auf bestimmte Beschaffungskategorien gestatten oder verhindern.</span><span class="sxs-lookup"><span data-stu-id="6f5ef-118">These policies can allow or prevent access to specific procurement categories.</span></span> <span data-ttu-id="6f5ef-119">Daher kann die Liste der externen Kataloge, die diesen Beschaffungskategorien zugeordnet sind, betroffen sein.</span><span class="sxs-lookup"><span data-stu-id="6f5ef-119">Therefore, the list of external catalogs that are mapped to these procurement categories can be affected.</span></span>

<span data-ttu-id="6f5ef-120">Weitere Informationen zum Einrichten von Richtlinien finden Sie unter [Einkaufsrichtlinien](../procurement/purchase-policies.md)</span><span class="sxs-lookup"><span data-stu-id="6f5ef-120">For more information about policies, see [Purchasing policies](../procurement/purchase-policies.md).</span></span>

- <span data-ttu-id="6f5ef-121">Wenn Sie externe Kataloge für bestimmte Beschaffungskategorien suchen, geben Sie Text im Feld "Katalogsuchgebiete" ein.</span><span class="sxs-lookup"><span data-stu-id="6f5ef-121">To find external catalogs for specific procurement categories, enter text in the catalog search field.</span></span>
- <span data-ttu-id="6f5ef-122">Um Produkte aus dem externen Katalog eines Lieferanten auf der Website des Kreditors hinzuzufügen, klicken auf den externen Katalog.</span><span class="sxs-lookup"><span data-stu-id="6f5ef-122">To add products from a vendor’s external catalog on the vendor’s website, click the external catalog.</span></span> <span data-ttu-id="6f5ef-123">Fügen Sie dann Produkte zum Einkaufskorb hinzu und gehen Sie zur Kasse. Die Einkaufskorbpositionen werden an Microsoft Dynamics 365 übertragen.</span><span class="sxs-lookup"><span data-stu-id="6f5ef-123">Then add products to the shopping cart, and check out. The shopping cart lines will be transferred to Microsoft Dynamics 365.</span></span>

<span data-ttu-id="6f5ef-124">Sind mehrere Optionen für Beschaffungskategorien vorhanden, wählen Sie die gewünschte Beschaffungskategorie aus, bevor Sie die Positionen der Bestellanforderung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6f5ef-124">If there are multiple options for procurement categories, select the correct procurement category before you add the lines to the requisition.</span></span>
<span data-ttu-id="6f5ef-125">Nachdem Positionen zu einer Anforderung hinzugefügt wurden, können Sie mehrere Positionen hinzufügen, ohne externe Kataloge zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6f5ef-125">After lines have been added to a requisition, you can add more lines without using external catalogs.</span></span> <span data-ttu-id="6f5ef-126">Alternativ können Sie fortfahren, um externe Kataloge zu verwenden, um Positionen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="6f5ef-126">Alternatively, you can continue to use external catalogs to add lines.</span></span>

<span data-ttu-id="6f5ef-127">Wenn die Bestellanforderung bereit ist, verwenden Sie die Aktivität **Workflow** > **Übermitteln**, zur Genehmigung.</span><span class="sxs-lookup"><span data-stu-id="6f5ef-127">When the requisition is ready, use the **Workflow** > **Submit** action to submit it for approval.</span></span>

