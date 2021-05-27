---
title: Die Stornierung der Fertigmeldung führt zu einer unerwarteten offenen Buchung
description: Durch die Stornierung der Fertigmeldung mit Kennzeichnung wird eine offene Buchung erstellt, bei der die stornierte Menge die gleichen Bestandsdimensionen wie die stornierte Buchung aufweist.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ea9044a9008e766c7fc92f98e27cfb91076f5b44
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026553"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a><span data-ttu-id="ec327-103">Die Stornierung der Fertigmeldung führt zu einer unerwarteten offenen Buchung</span><span class="sxs-lookup"><span data-stu-id="ec327-103">Reversal of reporting as finished creates an unexpected open transaction</span></span>

<span data-ttu-id="ec327-104">KB-Nummer: 4612469</span><span class="sxs-lookup"><span data-stu-id="ec327-104">KB number: 4612469</span></span>

## <a name="symptoms"></a><span data-ttu-id="ec327-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="ec327-105">Symptoms</span></span>

<span data-ttu-id="ec327-106">Wenn Sie die Fertigmeldung mit Kennzeichnung stornieren, erstellt das System eine offene Buchung, bei der die stornierte Menge die gleichen Bestandsdimensionen wie die stornierte Buchung aufweist.</span><span class="sxs-lookup"><span data-stu-id="ec327-106">If you reverse reporting as finished that has marking, the system creates an open transaction where the reversed quantity has the same inventory dimensions as the transaction that was reversed.</span></span>

## <a name="resolution"></a><span data-ttu-id="ec327-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="ec327-107">Resolution</span></span>

<span data-ttu-id="ec327-108">Wenn Sie einen als fertig gemeldeten Vorgang stornieren , wird die Bestandsdimension aus der Produktionserfassung initialisiert.</span><span class="sxs-lookup"><span data-stu-id="ec327-108">When you reverse a report-as-finished operation, the inventory dimension is initialized from the production journal.</span></span> <span data-ttu-id="ec327-109">Daher erhält es die Chargennummer.</span><span class="sxs-lookup"><span data-stu-id="ec327-109">Therefore, it gets the batch number.</span></span> <span data-ttu-id="ec327-110">Aufgrund der Kennzeichnung erben die Auftragsbuchungen die Chargennummer.</span><span class="sxs-lookup"><span data-stu-id="ec327-110">Because of marking, the sales order transactions will inherit the batch number.</span></span>

<span data-ttu-id="ec327-111">Die Dimension kann zurückgesetzt werden, wenn die Fertigmeldung gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="ec327-111">The dimension can be reset when the reporting as finished is posted.</span></span>
