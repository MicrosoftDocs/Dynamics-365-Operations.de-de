---
title: Anlagenanschaffungen vorschlagen
description: In diesem Verfahren wird eine Anlage mithilfe des Anschaffungsvorschlags in der Anlagenerfassung abgerufen.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1891206bb266b126eccfa789b8c8062c9bfa688b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570879"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="11b42-103">Anlagenanschaffungen vorschlagen</span><span class="sxs-lookup"><span data-stu-id="11b42-103">Propose fixed asset acquisitions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="11b42-104">In diesem Verfahren wird eine Anlage mithilfe des Anschaffungsvorschlags in der Anlagenerfassung abgerufen.</span><span class="sxs-lookup"><span data-stu-id="11b42-104">This procedure shows how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="11b42-105">Dabei werden die Buchhalterrolle und die Demodaten für die juristische Person USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="11b42-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="11b42-106">Wechseln Sie zu "Anlagen" > "Journaleinträge" > "Anlagenerfassung".</span><span class="sxs-lookup"><span data-stu-id="11b42-106">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="11b42-107">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="11b42-107">Click New.</span></span>
3. <span data-ttu-id="11b42-108">Geben Sie im Feld "Name" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="11b42-108">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="11b42-109">Klicken Sie auf "Positionen".</span><span class="sxs-lookup"><span data-stu-id="11b42-109">Click Lines.</span></span>
5. <span data-ttu-id="11b42-110">Klicken Sie auf "Vorschläge".</span><span class="sxs-lookup"><span data-stu-id="11b42-110">Click Proposals.</span></span>
6. <span data-ttu-id="11b42-111">Klicken Sie auf "Anschaffungsvorschlag".</span><span class="sxs-lookup"><span data-stu-id="11b42-111">Click Acquisition proposal.</span></span>
7. <span data-ttu-id="11b42-112">Klicken Sie auf "Filter".</span><span class="sxs-lookup"><span data-stu-id="11b42-112">Click Filter.</span></span>
8. <span data-ttu-id="11b42-113">Klicken Sie auf "Zurücksetzen, um vorherige Werte zu löschen".</span><span class="sxs-lookup"><span data-stu-id="11b42-113">Click Reset to clear out previous values.</span></span>
9. <span data-ttu-id="11b42-114">Wählen Sie die Zeile "Anlagenummer" aus.</span><span class="sxs-lookup"><span data-stu-id="11b42-114">Select the Fixed asset number row.</span></span>
10. <span data-ttu-id="11b42-115">Geben Sie im Feld "Kriterien" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="11b42-115">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="11b42-116">Legen Sie die verbleibenden Kriterien für die Anlagen fest, die Sie mit diesem Vorschlag abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="11b42-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
11. <span data-ttu-id="11b42-117">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="11b42-117">Click OK.</span></span>
12. <span data-ttu-id="11b42-118">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="11b42-118">Click OK.</span></span>
    * <span data-ttu-id="11b42-119">Überprüfen Sie die erstellten Transaktionspositionen.</span><span class="sxs-lookup"><span data-stu-id="11b42-119">Verify the transaction lines created.</span></span>  
    * <span data-ttu-id="11b42-120">Nur Anlagen mit dem Anschaffungsdatum und dem Anschaffungspreis, die im Buch festgelegt sind, werden in den Anschaffungsvorschlag einbezogen.</span><span class="sxs-lookup"><span data-stu-id="11b42-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
13. <span data-ttu-id="11b42-121">Klicken Sie auf die Registerkarte 'Bücher'.</span><span class="sxs-lookup"><span data-stu-id="11b42-121">Click the Books tab.</span></span>
14. <span data-ttu-id="11b42-122">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="11b42-122">Click Post.</span></span>

