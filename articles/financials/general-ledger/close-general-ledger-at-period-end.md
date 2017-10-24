---
title: Abschluss des Hauptbuchs am Ende der Periode
description: "In diesem Thema werden die Aufgaben beschrieben, die in der Regel ausgeführt werden, wenn ein Periodenabschluss für Hauptbuch ausgeführt wird."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 16acadf0b814ff5863873280cd8d6e6ddbdcffc8
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="close-the-general-ledger-at-period-end"></a><span data-ttu-id="77925-103">Abschluss des Hauptbuchs am Ende der Periode</span><span class="sxs-lookup"><span data-stu-id="77925-103">Close the general ledger at period end</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="77925-104">In diesem Thema werden die Aufgaben beschrieben, die in der Regel ausgeführt werden, wenn ein Periodenabschluss für Hauptbuch ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="77925-104">This topic describes the tasks that are typically completed when performing a period closing for General ledger.</span></span> 

<span data-ttu-id="77925-105">Im Hauptbuch können Sie Abschlussprozeduren für eine Periode oder ein Jahr ausführen.</span><span class="sxs-lookup"><span data-stu-id="77925-105">In General ledger, you can complete closing procedures for a period or a year.</span></span> <span data-ttu-id="77925-106">Abschlussvorgänge bereiten das System auf eine neue Periode vor.</span><span class="sxs-lookup"><span data-stu-id="77925-106">Closing processes prepare the system for a new period.</span></span> <span data-ttu-id="77925-107">Um das System auf ein neues Jahr vorzubereiten, müssen Sie den Jahresabschlussprozess ausführen.</span><span class="sxs-lookup"><span data-stu-id="77925-107">To prepare the system for a new year, you must run the year end close process.</span></span> <span data-ttu-id="77925-108">Jede Organisation hat unterschiedliche Verfahren und Schritte, die für das Ende einer Periode ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="77925-108">Each organization has different processes and steps that it performs for the end of a period.</span></span> <span data-ttu-id="77925-109">Nachfolgend sind einige Schritte für optionale Periodenenden beschrieben:</span><span class="sxs-lookup"><span data-stu-id="77925-109">Here are some optional steps for period ends:</span></span>

-   <span data-ttu-id="77925-110">Schließen Sie alle Aufgaben für alle anderen Module ab, z. B. Debitoren, Kreditoren und Bestand.</span><span class="sxs-lookup"><span data-stu-id="77925-110">Complete all the tasks for all other modules, such as Accounts receivable, Accounts payable, and Inventory.</span></span>
-   <span data-ttu-id="77925-111">Überprüfen Sie, ob alle Erfassungen gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="77925-111">Verify that all journals are posted.</span></span>
-   <span data-ttu-id="77925-112">Führen Sie die Neubewertung der Fremdwährung aus, um alle unrealisierten Gewinn- oder Verlustbeträge zu generieren.</span><span class="sxs-lookup"><span data-stu-id="77925-112">Run foreign currency revaluation to generate any unrealized gain or loss amounts.</span></span>
-   <span data-ttu-id="77925-113">Gleichen Sie Buchungen für jedes Sachkonto aus.</span><span class="sxs-lookup"><span data-stu-id="77925-113">Settle transactions for each ledger account.</span></span>
-   <span data-ttu-id="77925-114">Verarbeiten Sie alle erforderlichen Zuteilungen.</span><span class="sxs-lookup"><span data-stu-id="77925-114">Process any required allocations.</span></span>
-   <span data-ttu-id="77925-115">Buchen Sie manuelle Regulierungen für das Ende der Periode.</span><span class="sxs-lookup"><span data-stu-id="77925-115">Manually post period-end adjustments.</span></span>
-   <span data-ttu-id="77925-116">Journalisieren Sie Transaktionen und überprüfen Sie den **Sachkontoerfassungs** Bericht.</span><span class="sxs-lookup"><span data-stu-id="77925-116">Journalize transactions, and review the **Ledger journal** report.</span></span>
-   <span data-ttu-id="77925-117">Führen Sie eine Konsolidierung aus, indem Sie ein Konsolidierungsunternehmen oder eine Finanzberichterstellung verwenden.</span><span class="sxs-lookup"><span data-stu-id="77925-117">Perform a consolidation by using a consolidation company or Financial reporting.</span></span>
-   <span data-ttu-id="77925-118">Generieren Sie Finanzaufstellungen zum Periodenende, indem Sie Finanzberichterstellung verwenden.</span><span class="sxs-lookup"><span data-stu-id="77925-118">Generate period-end financial statements by using Financial reporting.</span></span>
-   <span data-ttu-id="77925-119">Legen Sie Sachkontoperioden auf **Gesperrt** fest, damit keine weitere Buchung stattfindet.</span><span class="sxs-lookup"><span data-stu-id="77925-119">Set ledger periods to **On hold**, so that no further posting occurs.</span></span> <span data-ttu-id="77925-120">Sie können für bessere Kontrolle eine Periode auf eine bestimmte Benutzergruppe begrenzen, wenn Aktivitäten zum Periodenende auftreten.</span><span class="sxs-lookup"><span data-stu-id="77925-120">You can also restrict a period to a specific user group while period-end activities are occurring, for better control.</span></span> <span data-ttu-id="77925-121">Es ist nicht sinnvoll, Perioden auf **Ständig Geschlossen** festzulegen, da eine geschlossene Periode nicht erneut geöffnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="77925-121">It's not a good idea to set periods to **Permanently closed**, because you can't reopen a period that has been closed.</span></span>

<span data-ttu-id="77925-122">Der Arbeitsbereich Finanzperioden schließen kann verwendet werden, um die Aufgaben, die für verschiedene Periodenendenprozesse erforderlich sind, zu organisieren und nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="77925-122">The Financial period close workspace can be used to organize and track the tasks required for various period end processes.</span></span> 


<span data-ttu-id="77925-123">Weitere Informationen zu Workflows finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="77925-123">For more information, see the following topics for more information:</span></span>
- [<span data-ttu-id="77925-124">Finanzperiodenabschluss-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="77925-124">Financial period close workspace</span></span>](financial-period-close-workspace.md) 
- [<span data-ttu-id="77925-125">Jahresabschluss</span><span class="sxs-lookup"><span data-stu-id="77925-125">Year end close</span></span>](Year-end-close.md)  
- [<span data-ttu-id="77925-126">Massen-Finanzperiodenabschluss</span><span class="sxs-lookup"><span data-stu-id="77925-126">Mass financial period close</span></span>](tasks/mass-financial-period-close.md)





