---
title: "Buchungskonten für die Anlagenveräußerung"
description: "Dieser Artikel beschreibt, wie Buchungskonten im Hauptbuch für den Abgang von Anlagen eingerichtet werden."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0129eae177d44100b09c2b7bce553dd5bde5ce0c
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="fixed-asset-disposal-posting-accounts"></a><span data-ttu-id="f1ed2-103">Buchungskonten für die Anlagenveräußerung</span><span class="sxs-lookup"><span data-stu-id="f1ed2-103">Fixed asset disposal posting accounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f1ed2-104">Dieser Artikel beschreibt, wie Buchungskonten im Hauptbuch für den Abgang von Anlagen eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="f1ed2-104">This article explains how to set up general ledger posting accounts for disposing of assets.</span></span>

<span data-ttu-id="f1ed2-105">Wählen Sie auf der Seite "Anlagenbuchungsprofile" im Inforegister "Sachkonten" die Optionen "Abgang – Verkauf" und "Abgang – Ausschuss" aus, um Buchungen im Sachkonto einzurichten.</span><span class="sxs-lookup"><span data-stu-id="f1ed2-105">In the Fixed asset posting profiles page, on the Ledger accounts FastTab, select Disposal - sale and Disposal - scrap to set up postings to the ledger.</span></span>

<span data-ttu-id="f1ed2-106">Für beide Buchungsarten wird der Abgangswert der Anlage dem Sachkonto gutgeschrieben.</span><span class="sxs-lookup"><span data-stu-id="f1ed2-106">For both transaction types, the ledger account is credited for the disposal value of the fixed asset.</span></span> <span data-ttu-id="f1ed2-107">Das Soll wird in einem Gegenkonto gebucht, das beispielsweise ein Bankkonto sein kann.</span><span class="sxs-lookup"><span data-stu-id="f1ed2-107">The debit is posted to an offset account, which might be, for example, a bank account.</span></span> <span data-ttu-id="f1ed2-108">Bei Veräußerung einer Anlage an einen Debitor wird anstelle des Gegenkontos das Debitorenkonto verwendet.</span><span class="sxs-lookup"><span data-stu-id="f1ed2-108">If a fixed asset is sold to a customer, the customer account is used instead of the offset account.</span></span>

<span data-ttu-id="f1ed2-109">Klicken Sie auf "Abgang" und anschließend auf "Verkauf" oder "Ausschuss", und richten Sie dann detaillierte Konten ein, um eine Rückbuchung des Nettobuchwerts der Anlage auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f1ed2-109">Click Disposal and then click Sale or Scrap, and then set up detailed accounts to reverse the net book value of the fixed asset.</span></span> <span data-ttu-id="f1ed2-110">Sie können auch Informationen in die Felder "Buchungswert" und "Verkaufswert" auf der Seite "Abgangsparameter" eingeben.</span><span class="sxs-lookup"><span data-stu-id="f1ed2-110">You can also enter information in the Post value and Sales value type fields in the Disposal parameters page.</span></span> 

<span data-ttu-id="f1ed2-111">Durch die Abgangsbuchung für eine Anlage in einem Low-Value-Pool verringert sich der Nettobuchwert des Low-Value-Pools lediglich um den Abgangsbetrag.</span><span class="sxs-lookup"><span data-stu-id="f1ed2-111">The disposal transaction for an asset in a low-value pool reduces the net book value of the low-value pool by the disposed amount only.</span></span> <span data-ttu-id="f1ed2-112">Übersteigt allerdings der Verkaufswert einer Anlage den Nettobuchwert des Low-Value-Pools, verringert sich der Nettobuchwert auf Null.</span><span class="sxs-lookup"><span data-stu-id="f1ed2-112">However, when the sale of an asset is exceeds the net book value of the low-value pool, the net book value is reduced to zero.</span></span>






