---
title: Anlagenanschaffungen vorschlagen
description: In diesem Thema wird beschrieben, wie eine Anlage mithilfe des Anschaffungsvorschlags in der Anlagenerfassung angeschafft wird.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e08177aad2db2438c2d5d4ddd294c1056b88167c
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142730"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="20ff6-103">Anlagenanschaffungen vorschlagen</span><span class="sxs-lookup"><span data-stu-id="20ff6-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="20ff6-104">In diesem Thema wird beschrieben, wie eine Anlage mithilfe des Anschaffungsvorschlags in der Anlagenerfassung angeschafft wird.</span><span class="sxs-lookup"><span data-stu-id="20ff6-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="20ff6-105">Dabei werden die Buchhalterrolle und die Demodaten für die juristische Person USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="20ff6-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="20ff6-106">Wechseln Sie im Navigationsbereich zu **Module > Anlagen > Journaleinträge > Anlagenerfassung**.</span><span class="sxs-lookup"><span data-stu-id="20ff6-106">In the Navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="20ff6-107">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="20ff6-107">Select **New**.</span></span>
3. <span data-ttu-id="20ff6-108">Geben Sie im Feld **Name** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="20ff6-108">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="20ff6-109">Wählen Sie im Aktivitätsbereich **Positionen** aus.</span><span class="sxs-lookup"><span data-stu-id="20ff6-109">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="20ff6-110">Wählen Sie **Vorschläge** aus.</span><span class="sxs-lookup"><span data-stu-id="20ff6-110">Select **Proposals**.</span></span>
6. <span data-ttu-id="20ff6-111">Wählen Sie **Anschaffungsvorschlag** aus.</span><span class="sxs-lookup"><span data-stu-id="20ff6-111">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="20ff6-112">Wählen Sie **Filter** aus.</span><span class="sxs-lookup"><span data-stu-id="20ff6-112">Select **Filter**.</span></span> <span data-ttu-id="20ff6-113">Wählen Sie **Zurücksetzen** aus, um vorherige Werte zu löschen.</span><span class="sxs-lookup"><span data-stu-id="20ff6-113">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="20ff6-114">Wählen Sie die Zeile **Anlagennummer** aus.</span><span class="sxs-lookup"><span data-stu-id="20ff6-114">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="20ff6-115">Geben Sie im Feld **Kriterien** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="20ff6-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="20ff6-116">Legen Sie die verbleibenden Kriterien für die Anlagen fest, die Sie mit diesem Vorschlag abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="20ff6-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="20ff6-117">Wählen Sie zweimal **OK** aus, um den Bereich zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="20ff6-117">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="20ff6-118">Überprüfen Sie die erstellten Transaktionspositionen.</span><span class="sxs-lookup"><span data-stu-id="20ff6-118">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="20ff6-119">Nur Anlagen mit dem Anschaffungsdatum und dem Anschaffungspreis, die im Buch festgelegt sind, werden in den Anschaffungsvorschlag einbezogen.</span><span class="sxs-lookup"><span data-stu-id="20ff6-119">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="20ff6-120">Wählen Sie auf der Seite die Registerkarte **Bücher** aus.</span><span class="sxs-lookup"><span data-stu-id="20ff6-120">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="20ff6-121">Wählen Sie **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="20ff6-121">Select **Post**.</span></span>

