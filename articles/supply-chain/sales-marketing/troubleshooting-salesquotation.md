---
title: Problembehandlung bei Verkaufsangeboten
description: In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Verkaufsangeboten auftreten können.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 09529ba729170be7281e2ae04008d3ba4a58e060
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824749"
---
# <a name="troubleshoot-sales-quotations"></a><span data-ttu-id="f0025-103">Problembehandlung bei Verkaufsangeboten</span><span class="sxs-lookup"><span data-stu-id="f0025-103">Troubleshoot sales quotations</span></span>

<span data-ttu-id="f0025-104">In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Verkaufsangeboten auftreten können.</span><span class="sxs-lookup"><span data-stu-id="f0025-104">This topic describes how to fix issues that you might encounter while you work with sales quotations.</span></span>

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a><span data-ttu-id="f0025-105">Ich kann die Verkaufsmenge eines Verkaufsangebots für einen Serviceartikel nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="f0025-105">I can't change the sales quantity of a sales quotation for a service item.</span></span>

### <a name="issue-description"></a><span data-ttu-id="f0025-106">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="f0025-106">Issue description</span></span>

<span data-ttu-id="f0025-107">Wenn Sie versuchen, eine Verkaufsmenge (**SalesQty**-Feld) für einen Artikel vom Typ *Dienstleistung* auf einer Verkaufsangebotsposition festzulegen, wird die folgende Meldung angezeigt: „Aktualisierung für Feld Menge nicht zulässig.“</span><span class="sxs-lookup"><span data-stu-id="f0025-107">If you try to set a sales quantity (**SalesQty** field) for an item of the *Service* type on a sales quotation line, you will receive the following message: "Update not allowed for field Quantity."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f0025-108">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="f0025-108">Issue resolution</span></span>

<span data-ttu-id="f0025-109">Sie können keine Verkaufsmenge für Produkte festlegen, bei denen es sich um Serviceartikel handelt.</span><span class="sxs-lookup"><span data-stu-id="f0025-109">You can't set a sales quantity for products that are service items.</span></span> <span data-ttu-id="f0025-110">Wenn Sie beispielsweise einen Service zum Installieren eines Artikels anbieten, ist es nicht sinnvoll, eine Menge zu erfassen, da kein physischer Artikel vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f0025-110">For example, if you offer a service to install an item, it doesn't make sense to record a quantity, because there is no physical item.</span></span> <span data-ttu-id="f0025-111">Es gibt nur einen Service.</span><span class="sxs-lookup"><span data-stu-id="f0025-111">There is only a service.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]