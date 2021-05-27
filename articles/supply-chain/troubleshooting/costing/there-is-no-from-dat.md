---
title: Die Registerkarte „Aktive Preise“ der Seite „Artikelpreis“ enthält kein „Startdatum“
description: Die Registerkarte „Aktive Preise“ der Seite „Artikelpreis“ enthält kein „Startdatum“.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dd13f6a3e5ce3c894e96f420358d337f2e43dba
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026556"
---
# <a name="there-is-no-from-date-value-on-the-active-prices-tab-of-the-item-price-page"></a><span data-ttu-id="670dc-103">Die Registerkarte „Aktive Preise“ der Seite „Artikelpreis“ enthält kein „Startdatum“</span><span class="sxs-lookup"><span data-stu-id="670dc-103">There is no From date value on the Active prices tab of the Item price page</span></span>

<span data-ttu-id="670dc-104">KB-Nummer: 4613548</span><span class="sxs-lookup"><span data-stu-id="670dc-104">KB number: 4613548</span></span>

## <a name="symptoms"></a><span data-ttu-id="670dc-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="670dc-105">Symptoms</span></span>

<span data-ttu-id="670dc-106">Die Registerkarte **Aktive Preise** der Seite **Artikelpreis** enthält kein **Startdatum**.</span><span class="sxs-lookup"><span data-stu-id="670dc-106">There is no **From date** value on the **Active prices** tab of the **Item price** page.</span></span>

## <a name="resolution"></a><span data-ttu-id="670dc-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="670dc-107">Resolution</span></span>

<span data-ttu-id="670dc-108">Der Wert **Startdatum** (Gültigkeitsdatum), das für den ausstehenden Preis festgesetzt ist, wird nicht auf den aktiven Preis übertragen.</span><span class="sxs-lookup"><span data-stu-id="670dc-108">The **From date** value (effective date) that is set on the pending price isn't transferred to the active price.</span></span>

<span data-ttu-id="670dc-109">Bei der Eingabe erhält ein Artikelkostendatensatz zunächst einen Status *Ausstehend* sowie ein gewünschtes Gültigkeitsdatum.</span><span class="sxs-lookup"><span data-stu-id="670dc-109">When an item cost record is first entered, it has a status of *Pending* and an intended effective date.</span></span> <span data-ttu-id="670dc-110">Bei Aktivierung des Artikelkostendatensatzes wird der Status zu *Aktiv* und das Gültigkeitsdatum in das Aktivierungsdatum aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="670dc-110">When you activate the item cost record, the status is updated to *Active*, and the effective date is updated to the activation date.</span></span> <span data-ttu-id="670dc-111">Daher ist das Aktivierungsdatum des aktiven Preises immer das tatsächliche Datum der Aktivierung.</span><span class="sxs-lookup"><span data-stu-id="670dc-111">Therefore, the active price's activation date is always the actual date of the activation.</span></span>

<span data-ttu-id="670dc-112">Weitere Informationen finden Sie unter [Nachkalkulationsversionen – Übersicht](../../cost-management/costing-versions.md).</span><span class="sxs-lookup"><span data-stu-id="670dc-112">For more information, see [Costing versions overview](../../cost-management/costing-versions.md).</span></span>
