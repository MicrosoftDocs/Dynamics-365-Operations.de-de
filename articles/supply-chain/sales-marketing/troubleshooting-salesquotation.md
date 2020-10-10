---
title: Problembehandlung bei Verkaufsangeboten
description: In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Verkaufsangeboten auftreten können.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 67610a833be132399b2d47ae8c6b27119be9ce95
ms.sourcegitcommit: 91e101d7a51a8b63bd196ec80e9224e5e6e6fc95
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/22/2020
ms.locfileid: "3834361"
---
# <a name="troubleshoot-sales-quotations"></a><span data-ttu-id="aec64-103">Problembehandlung bei Verkaufsangeboten</span><span class="sxs-lookup"><span data-stu-id="aec64-103">Troubleshoot sales quotations</span></span>

<span data-ttu-id="aec64-104">In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Verkaufsangeboten auftreten können.</span><span class="sxs-lookup"><span data-stu-id="aec64-104">This topic describes how to fix issues that you might encounter while you work with sales quotations.</span></span>

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a><span data-ttu-id="aec64-105">Ich kann die Verkaufsmenge eines Verkaufsangebots für einen Serviceartikel nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="aec64-105">I can't change the sales quantity of a sales quotation for a service item.</span></span>

### <a name="issue-description"></a><span data-ttu-id="aec64-106">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="aec64-106">Issue description</span></span>

<span data-ttu-id="aec64-107">Wenn Sie versuchen, eine Verkaufsmenge (**SalesQty**-Feld) für einen Artikel vom Typ *Dienstleistung* auf einer Verkaufsangebotsposition festzulegen, wird die folgende Meldung angezeigt: „Aktualisierung für Feld Menge nicht zulässig.“</span><span class="sxs-lookup"><span data-stu-id="aec64-107">If you try to set a sales quantity (**SalesQty** field) for an item of the *Service* type on a sales quotation line, you will receive the following message: "Update not allowed for field Quantity."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="aec64-108">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="aec64-108">Issue resolution</span></span>

<span data-ttu-id="aec64-109">Sie können keine Verkaufsmenge für Produkte festlegen, bei denen es sich um Serviceartikel handelt.</span><span class="sxs-lookup"><span data-stu-id="aec64-109">You can't set a sales quantity for products that are service items.</span></span> <span data-ttu-id="aec64-110">Wenn Sie beispielsweise einen Service zum Installieren eines Artikels anbieten, ist es nicht sinnvoll, eine Menge zu erfassen, da kein physischer Artikel vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="aec64-110">For example, if you offer a service to install an item, it doesn't make sense to record a quantity, because there is no physical item.</span></span> <span data-ttu-id="aec64-111">Es gibt nur einen Service.</span><span class="sxs-lookup"><span data-stu-id="aec64-111">There is only a service.</span></span>

