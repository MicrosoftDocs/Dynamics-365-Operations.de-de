---
title: Buchungskonten für Anlagenveräußerung
description: Dieser Artikel beschreibt, wie Buchungskonten im Hauptbuch für den Abgang von Anlagen eingerichtet werden.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e9a46125dbe5262ba388e3958ea452975a98243f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187152"
---
# <a name="fixed-asset-disposal-posting-accounts"></a><span data-ttu-id="f68c6-103">Buchungskonten für Anlagenveräußerung</span><span class="sxs-lookup"><span data-stu-id="f68c6-103">Fixed asset disposal posting accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f68c6-104">Dieser Artikel beschreibt, wie Buchungskonten im Hauptbuch für den Abgang von Anlagen eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="f68c6-104">This topic explains how to set up general ledger posting accounts for disposing of assets.</span></span>

<span data-ttu-id="f68c6-105">Wählen Sie auf der Seite "Anlagenbuchungsprofile" im Inforegister "Sachkonten" die Optionen "Abgang – Verkauf" und "Abgang – Ausschuss" aus, um Buchungen im Sachkonto einzurichten.</span><span class="sxs-lookup"><span data-stu-id="f68c6-105">In the Fixed asset posting profiles page, on the Ledger accounts FastTab, select Disposal - sale and Disposal - scrap to set up postings to the ledger.</span></span>

<span data-ttu-id="f68c6-106">Für beide Buchungsarten wird der Abgangswert der Anlage dem Sachkonto gutgeschrieben.</span><span class="sxs-lookup"><span data-stu-id="f68c6-106">For both transaction types, the ledger account is credited for the disposal value of the fixed asset.</span></span> <span data-ttu-id="f68c6-107">Das Soll wird in einem Gegenkonto gebucht, das beispielsweise ein Bankkonto sein kann.</span><span class="sxs-lookup"><span data-stu-id="f68c6-107">The debit is posted to an offset account, which might be, for example, a bank account.</span></span> <span data-ttu-id="f68c6-108">Bei Veräußerung einer Anlage an einen Debitor wird anstelle des Gegenkontos das Debitorenkonto verwendet.</span><span class="sxs-lookup"><span data-stu-id="f68c6-108">If a fixed asset is sold to a customer, the customer account is used instead of the offset account.</span></span>

<span data-ttu-id="f68c6-109">Klicken Sie auf "Abgang" und anschließend auf "Verkauf" oder "Ausschuss", und richten Sie dann detaillierte Konten ein, um eine Rückbuchung des Nettobuchwerts der Anlage auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f68c6-109">Click Disposal and then click Sale or Scrap, and then set up detailed accounts to reverse the net book value of the fixed asset.</span></span> <span data-ttu-id="f68c6-110">Sie können auch Informationen in die Felder "Buchungswert" und "Verkaufswert" auf der Seite "Abgangsparameter" eingeben.</span><span class="sxs-lookup"><span data-stu-id="f68c6-110">You can also enter information in the Post value and Sales value type fields in the Disposal parameters page.</span></span> 

<span data-ttu-id="f68c6-111">Durch die Abgangsbuchung für eine Anlage in einem Low-Value-Pool verringert sich der Nettobuchwert des Low-Value-Pools lediglich um den Abgangsbetrag.</span><span class="sxs-lookup"><span data-stu-id="f68c6-111">The disposal transaction for an asset in a low-value pool reduces the net book value of the low-value pool by the disposed amount only.</span></span> <span data-ttu-id="f68c6-112">Übersteigt allerdings der Verkaufswert einer Anlage den Nettobuchwert des Low-Value-Pools, verringert sich der Nettobuchwert auf Null.</span><span class="sxs-lookup"><span data-stu-id="f68c6-112">However, when the sale of an asset exceeds the net book value of the low-value pool, the net book value is reduced to zero.</span></span>





