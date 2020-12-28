---
title: Untergeordnetes Sachkonto an das Hauptbuch übertragen
description: In diesem Thema werden Funktionen in Microsoft Dynamics 365 Finance beschrieben, die im Zusammenhang mit der Übertragung des untergeordneten Sachbuchs an das Hauptbuch stehen.
author: roschlom
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 7addb1f26a33db84d947e6fede876be648d2c654
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645169"
---
# <a name="subledger-transfer-to-the-general-ledger"></a><span data-ttu-id="465c9-103">Untergeordnetes Sachkonto an das Hauptbuch übertragen</span><span class="sxs-lookup"><span data-stu-id="465c9-103">Subledger transfer to the General ledger</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="465c9-104">In diesem Thema werden Funktionen in Microsoft Dynamics 365 Finance beschrieben, die sich auf die Regeln für die Übertragung von Chargen von untergeordneten Sachkontoeinträgen beziehen.</span><span class="sxs-lookup"><span data-stu-id="465c9-104">This topic describes capabilities in Microsoft Dynamics 365 Finance that are related to the rules for transferring batches of subledger journal entries.</span></span>

<span data-ttu-id="465c9-105">In Version 8.1 wurden Änderungen vorgenommen, um die Übertragung von Regeln zu ermöglichen, bei denen die **synchrone** Option veraltet wurde.</span><span class="sxs-lookup"><span data-stu-id="465c9-105">In version 8.1, changes were made to allow the transfer of rules, which deprecated the **Synchronous** option.</span></span> <span data-ttu-id="465c9-106">Weitere Informationen finden Sie unter [Entfernte oder veraltete Funktionen Finance and Operations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20).</span><span class="sxs-lookup"><span data-stu-id="465c9-106">For more information, see [Removed or deprecated features for Finance and Operations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20).</span></span>

<span data-ttu-id="465c9-107">Die folgenden Optionen stehen zum Übertragen von Chargen des untergeordneten Sachkontos zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="465c9-107">The following options are available for transferring subledger batches.</span></span> 

 - <span data-ttu-id="465c9-108">Asynchron – Mit dieser Option wird die Übertragung der untergeordneten Sachkontoeinträge in das Hauptbuch sofort geplant.</span><span class="sxs-lookup"><span data-stu-id="465c9-108">Asynchronous – This option will immediately schedule the transfer of the subledger accounting entries to the general ledger.</span></span> <span data-ttu-id="465c9-109">Der Hauptbuchbeleg wird erfasst, sobald die Ressourcen für die Verarbeitung dieser Anforderung auf dem Server frei sind.</span><span class="sxs-lookup"><span data-stu-id="465c9-109">The general ledger voucher will be recorded as soon as resources are free to process this request on the server.</span></span> 

- <span data-ttu-id="465c9-110">Geplante Charge – Diese Option fügt die Buchhaltungseinträge des untergeordneten Sachkontos hinzu, die in die Verarbeitungswarteschlange im Hauptbuch übertragen werden, wo die Einträge in der Reihenfolge ihres Eingangs verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="465c9-110">Scheduled batch – This option will add the subledger accounting entries that are being transferred to the processing queue in the general ledger, where the entries will be processed in order received.</span></span> <span data-ttu-id="465c9-111">Der Hauptbuchbeleg wird zur geplanten Zeit erfasst, sobald die Ressourcen für die Verarbeitung dieses Batchauftrags auf dem Server frei sind.</span><span class="sxs-lookup"><span data-stu-id="465c9-111">The general ledger voucher will be recorded at the scheduled time if resources are free to process this batch job on the server.</span></span> 
 
<span data-ttu-id="465c9-112">In Version 10.0.8 wurden Verbesserungen vorgenommen, um die Leistung der asynchronen Option zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="465c9-112">In version 10.0.8, improvements were made to enhance the performance of the Asynchronous option.</span></span> <span data-ttu-id="465c9-113">Diese Funktion wird unter dem Funktionsnamen **Übertragung des untergeordneten Sachkontos zur Leistungsoptimierung im Hauptbuch** aktiviert.</span><span class="sxs-lookup"><span data-stu-id="465c9-113">This feature is enabled under the feature name **Subledger transfer to General Ledger performance optimization**.</span></span> 
 
<span data-ttu-id="465c9-114">Diese Funktionalität verbessert die Übertragung von Daten aus dem untergeordneten Sachkonto in das Hauptbuch.</span><span class="sxs-lookup"><span data-stu-id="465c9-114">This functionality improves the transfer of data from the subledger to the general ledger.</span></span> <span data-ttu-id="465c9-115">Dadurch kann der Prozess effizienter werden, und Gruppen kleinerer zu übertragender Transaktionen werden zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="465c9-115">It allows the process to be more efficient, and it groups together sets of smaller transactions to transfer.</span></span> <span data-ttu-id="465c9-116">Dies ermöglicht eine effizientere Nutzung des Batch-Servers.</span><span class="sxs-lookup"><span data-stu-id="465c9-116">This allows for a more efficient use of the batch server.</span></span> <span data-ttu-id="465c9-117">Diese Funktionalität setzt voraus, dass der Batch-Server eingerichtet, online ist und funktioniert, damit die asynchrone Übertragungsoption funktioniert.</span><span class="sxs-lookup"><span data-stu-id="465c9-117">This functionality requires that the batch server be set up, online, and functioning in order for the Asynchronous transfer option to work.</span></span> 
