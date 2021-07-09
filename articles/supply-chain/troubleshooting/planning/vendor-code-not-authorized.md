---
title: Der Kreditor-Code ist für ein bestimmtes Produkt und Datum nicht autorisiert
description: Wenn Sie versuchen, einen geplanten Auftrag zu fixieren oder eine Zeile zu einer Bestellung hinzuzufügen, erhalten Sie eine Fehlermeldung, die besagt, dass der Kreditor-Code für ein Produkt und ein Datum nicht autorisiert ist.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO_ReqTransPoMarkFirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e6b1189e4fedfdb029f4b4503f0635133df9d87e
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294086"
---
# <a name="vendor-code-isnt-authorized-for-a-specific-product-and-date"></a><span data-ttu-id="74a52-103">Der Kreditor-Code ist für ein bestimmtes Produkt und Datum nicht autorisiert</span><span class="sxs-lookup"><span data-stu-id="74a52-103">Vendor code isn't authorized for a specific product and date</span></span>

<span data-ttu-id="74a52-104">Fehlercode: SYP4881415</span><span class="sxs-lookup"><span data-stu-id="74a52-104">Error code: SYP4881415</span></span>

## <a name="symptoms"></a><span data-ttu-id="74a52-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="74a52-105">Symptoms</span></span>

<span data-ttu-id="74a52-106">Wenn Sie versuchen, einen geplanten Auftrag zu fixieren oder eine Zeile zu einer Einkaufsbestellung hinzuzufügen, erhalten Sie die folgende Fehlermeldung:</span><span class="sxs-lookup"><span data-stu-id="74a52-106">When you try to firm a planned order or add a line to a purchase order, you receive the following error message:</span></span>

> <span data-ttu-id="74a52-107">Der Lieferantencode %1 ist für %2 auf %3 nicht autorisiert.</span><span class="sxs-lookup"><span data-stu-id="74a52-107">Vendor code %1 is not authorized for %2 on %3.</span></span>

## <a name="cause"></a><span data-ttu-id="74a52-108">Ursache</span><span class="sxs-lookup"><span data-stu-id="74a52-108">Cause</span></span>

<span data-ttu-id="74a52-109">Der Fehler tritt auf, weil das Feld **Prüfmethode für genehmigte Kreditor** für das angegebene Produkt auf *Nur Warnung* oder *Nicht zulässig* festgelegt ist und der Kreditor derzeit nicht berechtigt ist, dieses Produkt zu liefern.</span><span class="sxs-lookup"><span data-stu-id="74a52-109">The error occurs because the **Approved vendor check method** field is set to *Warning only* or *Not allowed* for the specified product, and the vendor isn't currently authorized to supply that product.</span></span>

## <a name="resolution"></a><span data-ttu-id="74a52-110">Lösung</span><span class="sxs-lookup"><span data-stu-id="74a52-110">Resolution</span></span>

<span data-ttu-id="74a52-111">Um dieses Problem zu beheben, deaktivieren Sie entweder die Lieferantenprüfung für das betreffende Produkt oder genehmigen Sie den Kreditor.</span><span class="sxs-lookup"><span data-stu-id="74a52-111">To fix this issue, either disable the vendor check for the relevant product or approve the vendor.</span></span>

<span data-ttu-id="74a52-112">Gehen Sie folgendermaßen vor, um die Lieferantenprüfung für ein Produkt zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="74a52-112">To disable the vendor check for a product, follow these steps.</span></span>

1. <span data-ttu-id="74a52-113">Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="74a52-113">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="74a52-114">Öffnen Sie das entsprechende Produkt.</span><span class="sxs-lookup"><span data-stu-id="74a52-114">Open the relevant product.</span></span>
1. <span data-ttu-id="74a52-115">Legen Sie auf der Inforegister-Registerkarte **Kauf** das Feld **Zugelassene Methode der Lieferantenprüfung** auf einen anderen Wert als *Nur Warnung* oder *Nicht zugelassen* fest.</span><span class="sxs-lookup"><span data-stu-id="74a52-115">On the **Purchase** FastTab, set the **Approved vendor check method** field to a value other than *Warning only* or *Not allowed*.</span></span>

<span data-ttu-id="74a52-116">Gehen Sie folgendermaßen vor, um einen Kreditor für ein Produkt zu genehmigen.</span><span class="sxs-lookup"><span data-stu-id="74a52-116">To approve a vendor for a product, follow these steps.</span></span>

1. <span data-ttu-id="74a52-117">Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="74a52-117">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="74a52-118">Öffnen Sie das entsprechende Element.</span><span class="sxs-lookup"><span data-stu-id="74a52-118">Open the relevant item.</span></span>
1. <span data-ttu-id="74a52-119">Wählen Sie im Aktionsbereich auf der Registerkarte **Einkauf** in der Gruppe **Genehmigter Kreditor** die Option **Einrichten**.</span><span class="sxs-lookup"><span data-stu-id="74a52-119">On the Action Pane, on the **Purchase** tab, in the **Approved vendor** group, select **Setup**.</span></span>
1. <span data-ttu-id="74a52-120">Fügen Sie auf der Listenseite **Genehmigter Kreditor** eine Zeile zum Raster hinzu und legen Sie die folgenden Werte dafür fest:</span><span class="sxs-lookup"><span data-stu-id="74a52-120">On the **Approved vendor** list page, add a row to the grid, and set the following values for it:</span></span>

    - <span data-ttu-id="74a52-121">**Lieferant** – Wählen Sie den zu genehmigenden Kreditor für das aktuelle Produkt aus.</span><span class="sxs-lookup"><span data-stu-id="74a52-121">**Vendor** – Select the vendor to approve for the current product.</span></span>
    - <span data-ttu-id="74a52-122">**Gültig ab** – Wählen Sie das erste Datum, für das der Kreditor genehmigt wird.</span><span class="sxs-lookup"><span data-stu-id="74a52-122">**Effective date** – Select the first date that the vendor is approved for.</span></span>
    - <span data-ttu-id="74a52-123">**Ablaufdatum** – Wählen Sie das letzte Datum aus, für das der Kreditor genehmigt ist.</span><span class="sxs-lookup"><span data-stu-id="74a52-123">**Expiration date** – Select the last date that the vendor is approved for.</span></span>

<span data-ttu-id="74a52-124">Weitere Informationen finden Sie unter [Lieferanten für bestimmte Produkte genehmigen](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).</span><span class="sxs-lookup"><span data-stu-id="74a52-124">For more information, see [Approve vendors for specific products](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).</span></span>
