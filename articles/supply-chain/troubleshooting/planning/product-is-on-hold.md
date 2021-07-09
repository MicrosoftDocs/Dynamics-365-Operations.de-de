---
title: Produkt liegt für Transaktionen in Wartestellung
description: Nachdem Sie Planungsaufträge fixiert haben, erhalten Sie eine Nachricht, die besagt, dass ein Element für Transaktionen zurückgestellt ist.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6654e6437a088218db116b955631be4c7e62de5f
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301278"
---
# <a name="product-is-on-hold-for-transactions"></a><span data-ttu-id="f2ee2-103">Produkt liegt für Transaktionen in Wartestellung</span><span class="sxs-lookup"><span data-stu-id="f2ee2-103">Product is on hold for transactions</span></span>

<span data-ttu-id="f2ee2-104">Fehlercode: SYS13295</span><span class="sxs-lookup"><span data-stu-id="f2ee2-104">Error code: SYS13295</span></span>

## <a name="symptoms"></a><span data-ttu-id="f2ee2-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="f2ee2-105">Symptoms</span></span>

<span data-ttu-id="f2ee2-106">Nachdem Sie geplanter Aufträge fixiert haben, erhalten Sie die folgende Fehlermeldung:</span><span class="sxs-lookup"><span data-stu-id="f2ee2-106">After you firm planned orders, you receive the following error message:</span></span>

> <span data-ttu-id="f2ee2-107">Artikel '%1' gesperrt für Buchungen in '%2'.</span><span class="sxs-lookup"><span data-stu-id="f2ee2-107">Item %1 is on hold for transactions in %2.</span></span>

## <a name="cause"></a><span data-ttu-id="f2ee2-108">Ursache</span><span class="sxs-lookup"><span data-stu-id="f2ee2-108">Cause</span></span>

<span data-ttu-id="f2ee2-109">Bei der Beschreibung von gesperrten Artikeln verwendet das System die Begriffe *gesperrt*, *gestoppt* und *gehalten* austauschbar.</span><span class="sxs-lookup"><span data-stu-id="f2ee2-109">When describing blocked items, system uses the terms *blocked*, *stopped*, and *on hold* interchangeably.</span></span> <span data-ttu-id="f2ee2-110">Dieser Fehler bedeutet, dass das Element in seinen Standardauftragseinstellungen als **Gestoppt** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f2ee2-110">This error means that the item is set as **Stopped** in its default order settings.</span></span>

<span data-ttu-id="f2ee2-111">Wenn ein Element gesperrt ist und Sie es zu einer Bestell- oder Verkaufsauftragszeile hinzufügen, erhalten Sie eine Warnmeldung.</span><span class="sxs-lookup"><span data-stu-id="f2ee2-111">If an item is blocked, and you add it to a purchase order or sales order line, you receive a warning message.</span></span> <span data-ttu-id="f2ee2-112">Wenn ein Element gesperrt ist, können Bestandstransaktionen, die sich auf die Bestell- oder Verkaufsauftragszeile beziehen, nicht geändert werden (z. B. wenn Sie einen Lieferschein oder eine Rechnung buchen).</span><span class="sxs-lookup"><span data-stu-id="f2ee2-112">When an item is blocked, inventory transactions that are related to the purchase order or sales order line can't be modified (for example, when you post a packing slip or an invoice).</span></span> <span data-ttu-id="f2ee2-113">Sie können einen gekauften Artikel sperren und gleichzeitig den Artikel verkaufen.</span><span class="sxs-lookup"><span data-stu-id="f2ee2-113">You can block a purchased item, and, at the same time, sell the item.</span></span> <span data-ttu-id="f2ee2-114">In diesem Fall ist das Kontrollkästchen **Gestoppt** auf einer Bestellung aktiviert, aber der Artikel ist nicht im Bestand oder auf einem Verkaufsauftrag gesperrt.</span><span class="sxs-lookup"><span data-stu-id="f2ee2-114">In this case, the **Stopped** check box is selected on a purchase order, but the item isn't blocked in inventory or on a sales order.</span></span>

<span data-ttu-id="f2ee2-115">Hier sind einige der Bedingungen, die dazu führen können, dass eine Artikelnummer für den Verkauf gesperrt wird:</span><span class="sxs-lookup"><span data-stu-id="f2ee2-115">Here are some of the conditions that can cause an item number to be blocked from being sold:</span></span>

- <span data-ttu-id="f2ee2-116">Das Element befindet sich noch in der Entwicklung oder Herstellung.</span><span class="sxs-lookup"><span data-stu-id="f2ee2-116">The item is still under development or manufacture.</span></span> <span data-ttu-id="f2ee2-117">Sie möchten daher nicht, dass er verkauft oder reserviert wird.</span><span class="sxs-lookup"><span data-stu-id="f2ee2-117">Therefore, you don't want it to be sold or reserved.</span></span>
- <span data-ttu-id="f2ee2-118">Sie haben viele fehlerhafte Elemente erhalten, und die Fehler müssen behoben werden, bevor das Element verkauft werden kann.</span><span class="sxs-lookup"><span data-stu-id="f2ee2-118">You've received many defective items, and the defects must be corrected before the item can be sold.</span></span>

<span data-ttu-id="f2ee2-119">In Fällen dieser Art können Sie das Element sperren, bis das Problem behoben ist.</span><span class="sxs-lookup"><span data-stu-id="f2ee2-119">In cases of this type, you can block the item until the issue is resolved.</span></span>

<span data-ttu-id="f2ee2-120">Wenn ein Element gesperrt ist und Sie eine Zeile für die Rücklieferung erstellen, erhalten Sie eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="f2ee2-120">If an item is blocked, and you create a return order line, you receive a message.</span></span> <span data-ttu-id="f2ee2-121">Sie können eine Serie oder ein Los eines Elements nicht sperren.</span><span class="sxs-lookup"><span data-stu-id="f2ee2-121">You can't block a series or a lot of an item.</span></span> <span data-ttu-id="f2ee2-122">Wenn Teile eines Elements gesperrt werden müssen, können Sie sie durch Verschieben des Bestands oder durch Sperren des gesamten Bestands des Elements für diesen Zeitraum sperren.</span><span class="sxs-lookup"><span data-stu-id="f2ee2-122">If parts of an item must be blocked, you can block them by moving inventory or by blocking the full stock of the item for that period.</span></span>

## <a name="resolution"></a><span data-ttu-id="f2ee2-123">Lösung</span><span class="sxs-lookup"><span data-stu-id="f2ee2-123">Resolution</span></span>

- <span data-ttu-id="f2ee2-124">Öffnen Sie die Seite **Standardauftragseinstellungen** für das Element, und deaktivieren Sie das Kontrollkästchen **Stopp**.</span><span class="sxs-lookup"><span data-stu-id="f2ee2-124">Open the **Default order settings** page for the item, and clear the **Stopped** checkbox.</span></span>
