---
title: Erfassungseinträge oder Buchungen anzeigen
description: Dieses Verfahren führt Sie durch die Verwendung der "Belegtransaktionsabfrage", um nach Erfassungseinträgen oder Transaktionen zu suchen.
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm, LedgerTransVoucher, LedgerTransBase, Originaldocuments
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f463b7764288918609cba364acf342eed28ad929
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443456"
---
# <a name="view-journal-entries-or-transactions"></a><span data-ttu-id="c54e8-103">Erfassungseinträge oder Buchungen anzeigen</span><span class="sxs-lookup"><span data-stu-id="c54e8-103">View journal entries or transactions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c54e8-104">Dieses Verfahren führt Sie durch die Verwendung der "Belegtransaktionsabfrage", um nach Erfassungseinträgen oder Transaktionen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="c54e8-104">This procedure shows how to use the Voucher transactions inquiry to search for journal entries or transactions.</span></span>

1. <span data-ttu-id="c54e8-105">Gehen Sie zu **Navigationsbereich > Module > Hauptbuch > Anfragen und Berichte > Belegtransaktionen**.</span><span class="sxs-lookup"><span data-stu-id="c54e8-105">Go to **Navigation pane > Modules > General ledger > Inquiries and reports > Voucher transactions**.</span></span>
2. <span data-ttu-id="c54e8-106">Wählen Sie das Feld aus, für das Sie ein Filterkriterium definieren wollen.</span><span class="sxs-lookup"><span data-stu-id="c54e8-106">Select the field for which you want to define a filter criteria.</span></span>
3. <span data-ttu-id="c54e8-107">Geben Sie die Filterkriterien für das ausgewählte Feld ein.</span><span class="sxs-lookup"><span data-stu-id="c54e8-107">Enter your filter critieria for the selected field.</span></span> <span data-ttu-id="c54e8-108">Sie können einen einzelnen Wert oder einen Bereich filtern.</span><span class="sxs-lookup"><span data-stu-id="c54e8-108">You could filter on a single value or a range.</span></span> <span data-ttu-id="c54e8-109">Wenn Sie einen Bereich definiert, stellen Sie sicher, dass die richtige Syntax verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c54e8-109">When defining a range, make sure the correct syntax is used.</span></span> <span data-ttu-id="c54e8-110">Die Werte sollten durch einen doppelten Punkt getrennt sein (..).</span><span class="sxs-lookup"><span data-stu-id="c54e8-110">The values should be separated by a double period (..).</span></span>  
4. <span data-ttu-id="c54e8-111">Klicken Sie auf die Registerkarte **Joins**, um weitere Tabellen hinzuzufügen, aus denen gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c54e8-111">Click the **Joins** tab to add additional tables from which to filter.</span></span>
5. <span data-ttu-id="c54e8-112">Wählen Sie im Baum **Tabellen/Allgemeine Journalbuchung**.</span><span class="sxs-lookup"><span data-stu-id="c54e8-112">In the tree, select **Tables/General journal entry**.</span></span>
6. <span data-ttu-id="c54e8-113">Klicken Sie auf **Tabellen-Join hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="c54e8-113">Click **Add table join**.</span></span>
7. <span data-ttu-id="c54e8-114">Klicken Sie auf **Abbrechen**, wenn Sie keine zusätzliche Tabelle hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="c54e8-114">Click **Cancel** if you decide not to add an additional table.</span></span>
8. <span data-ttu-id="c54e8-115">Klicken Sie auf die Registerkarte **Bereich**.</span><span class="sxs-lookup"><span data-stu-id="c54e8-115">Click the **Range** tab.</span></span>
9. <span data-ttu-id="c54e8-116">Klicken Sie zum Ausführen der Abfrage auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="c54e8-116">Click **OK** to run the query.</span></span>
10. <span data-ttu-id="c54e8-117">Klicken Sie im Aktionsbereich auf **Transaktionsursprung**.</span><span class="sxs-lookup"><span data-stu-id="c54e8-117">On the Action pane, click **Transaction origin**.</span></span> <span data-ttu-id="c54e8-118">Verschiedene Schaltflächen über dem Raster können verwendet werden, um zusätzliche Informationen zum Datensatz des ausgewählten Belegs zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="c54e8-118">Various buttons about the grid can be used to research additional information about the selected record of the voucher.</span></span> <span data-ttu-id="c54e8-119">Einige Schaltflächen sind möglicherweise nicht verfügbar, je nach der Buchungsart und den Merkmalen der Buchung.</span><span class="sxs-lookup"><span data-stu-id="c54e8-119">Some buttons may not be available, depending on the type of transaction and characteristics of the transaction.</span></span>
11. <span data-ttu-id="c54e8-120">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c54e8-120">Close the page.</span></span>
12. <span data-ttu-id="c54e8-121">Klicken Sie im Aktionsbereich auf **Originaldokument**.</span><span class="sxs-lookup"><span data-stu-id="c54e8-121">On the Action pane, Click **Original document**.</span></span>
13. <span data-ttu-id="c54e8-122">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c54e8-122">Close the page.</span></span>

