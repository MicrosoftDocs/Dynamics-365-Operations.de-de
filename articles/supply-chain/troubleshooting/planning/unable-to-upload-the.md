---
title: Sie können die geplanten Einstandspreise nicht aktualisieren, wenn Sie Bedarfsplanungsdatensätze importieren
description: Wenn Sie Datenentitäten zum Importieren von Bedarfsplanungsdatensätzen verwenden, wird der Einstandspreis für vorhandene Datensätze nicht aktualisiert, um mit den importierten Daten übereinzustimmen.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c8ea8322a6c7bafe2dfcaaee3e9989f753c85e2a
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026545"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a><span data-ttu-id="9c8d5-103">Sie können die geplanten Einstandspreise nicht aktualisieren, wenn Sie Bedarfsplanungsdatensätze importieren</span><span class="sxs-lookup"><span data-stu-id="9c8d5-103">You can't update the forecasted unit cost when you import demand forecast records</span></span>

<span data-ttu-id="9c8d5-104">KB-Nummer: 4614109</span><span class="sxs-lookup"><span data-stu-id="9c8d5-104">KB number: 4614109</span></span>

## <a name="symptoms"></a><span data-ttu-id="9c8d5-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="9c8d5-105">Symptoms</span></span>

<span data-ttu-id="9c8d5-106">Wenn Sie Datenentitäten zum Importieren von Bedarfsplanungsdatensätzen verwenden, wird der Wert **Geplanter Einstandspreis** für vorhandene Datensätze nicht aktualisiert, um mit den importierten Daten übereinzustimmen.</span><span class="sxs-lookup"><span data-stu-id="9c8d5-106">When you use data entities to import demand forecast records, the **Forecasted unit cost** value for existing records isn't updated so that it matches the imported data.</span></span>

## <a name="cause"></a><span data-ttu-id="9c8d5-107">Ursache</span><span class="sxs-lookup"><span data-stu-id="9c8d5-107">Cause</span></span>

<span data-ttu-id="9c8d5-108">**Geplanter Einstandspreis** ist ein schreibgeschütztes Feld.</span><span class="sxs-lookup"><span data-stu-id="9c8d5-108">**Forecasted unit cost** is a read-only field.</span></span> <span data-ttu-id="9c8d5-109">Der Wert basiert auf dem Produkteinstandspreis und kann nicht direkt durch Import festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9c8d5-109">The value is based on the product unit cost and can't be set directly through import.</span></span>

## <a name="resolution"></a><span data-ttu-id="9c8d5-110">Lösung</span><span class="sxs-lookup"><span data-stu-id="9c8d5-110">Resolution</span></span>

<span data-ttu-id="9c8d5-111">Da das Feld schreibgeschützt ist, können Sie keine Werte dafür importieren.</span><span class="sxs-lookup"><span data-stu-id="9c8d5-111">Because the field is read only, you can't import values for it.</span></span> <span data-ttu-id="9c8d5-112">Der Wert wird gemäß der vorhandenen Geschäftslogik berechnet.</span><span class="sxs-lookup"><span data-stu-id="9c8d5-112">The value will be calculated according to the existing business logic.</span></span>
