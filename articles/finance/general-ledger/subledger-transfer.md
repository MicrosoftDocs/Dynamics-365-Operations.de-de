---
title: Untergeordnetes Sachkonto an das Hauptbuch übertragen
description: In diesem Thema werden Funktionen in Microsoft Dynamics 365 Finance beschrieben, die im Zusammenhang mit der Übertragung des untergeordneten Sachbuchs an das Hauptbuch stehen.
author: roschlom
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 1efdf095e379b73d553ca3525abbeee8ca35bcbb
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897503"
---
# <a name="subledger-transfer-to-the-general-ledger"></a><span data-ttu-id="d5d58-103">Untergeordnetes Sachkonto an das Hauptbuch übertragen</span><span class="sxs-lookup"><span data-stu-id="d5d58-103">Subledger transfer to the General ledger</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d5d58-104">In diesem Thema werden Funktionen in Microsoft Dynamics 365 Finance beschrieben, die sich auf die Regeln für die Übertragung von Chargen von untergeordneten Sachkontoeinträgen beziehen.</span><span class="sxs-lookup"><span data-stu-id="d5d58-104">This topic describes capabilities in Microsoft Dynamics 365 Finance that are related to the rules for transferring batches of subledger journal entries.</span></span>

<span data-ttu-id="d5d58-105">In Version 8.1 wurden Änderungen vorgenommen, um die Übertragung von Regeln zu ermöglichen, bei denen die **synchrone** Option veraltet wurde.</span><span class="sxs-lookup"><span data-stu-id="d5d58-105">In version 8.1, changes were made to allow the transfer of rules, which deprecated the **Synchronous** option.</span></span> <span data-ttu-id="d5d58-106">Weitere Informationen finden Sie unter [Entfernte oder veraltete Funktionen Finance and Operations](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).</span><span class="sxs-lookup"><span data-stu-id="d5d58-106">For more information, see [Removed or deprecated features for Finance and Operations](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).</span></span>

<span data-ttu-id="d5d58-107">Die folgenden Optionen stehen zum Übertragen von Chargen des untergeordneten Sachkontos zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="d5d58-107">The following options are available for transferring subledger batches.</span></span> 

 - <span data-ttu-id="d5d58-108">Asynchron – Mit dieser Option wird die Übertragung der untergeordneten Sachkontoeinträge in das Hauptbuch sofort geplant.</span><span class="sxs-lookup"><span data-stu-id="d5d58-108">Asynchronous – This option will immediately schedule the transfer of the subledger accounting entries to the general ledger.</span></span> <span data-ttu-id="d5d58-109">Der Hauptbuchbeleg wird erfasst, sobald die Ressourcen für die Verarbeitung dieser Anforderung auf dem Server frei sind.</span><span class="sxs-lookup"><span data-stu-id="d5d58-109">The general ledger voucher will be recorded as soon as resources are free to process this request on the server.</span></span> 

- <span data-ttu-id="d5d58-110">Geplante Charge – Diese Option fügt die Buchhaltungseinträge des untergeordneten Sachkontos hinzu, die in die Verarbeitungswarteschlange im Hauptbuch übertragen werden, wo die Einträge in der Reihenfolge ihres Eingangs verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="d5d58-110">Scheduled batch – This option will add the subledger accounting entries that are being transferred to the processing queue in the general ledger, where the entries will be processed in order received.</span></span> <span data-ttu-id="d5d58-111">Der Hauptbuchbeleg wird zur geplanten Zeit erfasst, sobald die Ressourcen für die Verarbeitung dieses Batchauftrags auf dem Server frei sind.</span><span class="sxs-lookup"><span data-stu-id="d5d58-111">The general ledger voucher will be recorded at the scheduled time if resources are free to process this batch job on the server.</span></span> 
 
<span data-ttu-id="d5d58-112">In Version 10.0.8 wurden Verbesserungen vorgenommen, um die Leistung der asynchronen Option zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="d5d58-112">In version 10.0.8, improvements were made to enhance the performance of the Asynchronous option.</span></span> <span data-ttu-id="d5d58-113">Diese Funktion wird unter dem Funktionsnamen **Übertragung des untergeordneten Sachkontos zur Leistungsoptimierung im Hauptbuch** aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d5d58-113">This feature is enabled under the feature name **Subledger transfer to General Ledger performance optimization**.</span></span> 
 
<span data-ttu-id="d5d58-114">Diese Funktionalität verbessert die Übertragung von Daten aus dem untergeordneten Sachkonto in das Hauptbuch.</span><span class="sxs-lookup"><span data-stu-id="d5d58-114">This functionality improves the transfer of data from the subledger to the general ledger.</span></span> <span data-ttu-id="d5d58-115">Dadurch kann der Prozess effizienter werden, und Gruppen kleinerer zu übertragender Transaktionen werden zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="d5d58-115">It allows the process to be more efficient, and it groups together sets of smaller transactions to transfer.</span></span> <span data-ttu-id="d5d58-116">Dies ermöglicht eine effizientere Nutzung des Batch-Servers.</span><span class="sxs-lookup"><span data-stu-id="d5d58-116">This allows for a more efficient use of the batch server.</span></span> <span data-ttu-id="d5d58-117">Diese Funktionalität setzt voraus, dass der Batch-Server eingerichtet, online ist und funktioniert, damit die asynchrone Übertragungsoption funktioniert.</span><span class="sxs-lookup"><span data-stu-id="d5d58-117">This functionality requires that the batch server be set up, online, and functioning in order for the Asynchronous transfer option to work.</span></span> 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]