---
title: Anlagenanschaffungen vorschlagen
description: In diesem Thema wird beschrieben, wie eine Anlage mithilfe des Anschaffungsvorschlags in der Anlagenerfassung angeschafft wird.
author: saraschi2
manager: AnnBe
ms.date: 07/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9259c9bbf52c1c09a7092db6976fc3fabca6601
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990438"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="68353-103">Anlagenanschaffungen vorschlagen</span><span class="sxs-lookup"><span data-stu-id="68353-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="68353-104">In diesem Thema wird beschrieben, wie eine Anlage mithilfe des Anschaffungsvorschlags in der Anlagenerfassung angeschafft wird.</span><span class="sxs-lookup"><span data-stu-id="68353-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="68353-105">Dabei werden die Buchhalterrolle und die Demodaten für die juristische Person USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="68353-105">It uses the accountant role and demo data for the USMF legal entity.</span></span> <span data-ttu-id="68353-106">Um eine Anlage durch eine Anlagenerfassung zu erwerben, müssen Sie zuerst den Anlagendatensatz erstellen und dann den Anschaffungspreis im Anlagenbuch festlegen.</span><span class="sxs-lookup"><span data-stu-id="68353-106">To acquire a fixed asset through a fixed asset proposal journal, you must first create the fixed asset record, and then define the acquisition price in the asset book.</span></span>

1. <span data-ttu-id="68353-107">Gehen Sie im Navigationsbereich zu **Module > Anlage > Journalbuchungen > Anlagenbuchhaltung**.</span><span class="sxs-lookup"><span data-stu-id="68353-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="68353-108">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="68353-108">Select **New**.</span></span>
3. <span data-ttu-id="68353-109">Geben Sie im Feld **Name** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="68353-109">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="68353-110">Wählen Sie im Aktivitätsbereich **Positionen** aus.</span><span class="sxs-lookup"><span data-stu-id="68353-110">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="68353-111">Wählen Sie **Vorschläge** aus.</span><span class="sxs-lookup"><span data-stu-id="68353-111">Select **Proposals**.</span></span>
6. <span data-ttu-id="68353-112">Wählen Sie **Anschaffungsvorschlag** aus.</span><span class="sxs-lookup"><span data-stu-id="68353-112">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="68353-113">Wählen Sie **Filter** aus.</span><span class="sxs-lookup"><span data-stu-id="68353-113">Select **Filter**.</span></span> <span data-ttu-id="68353-114">Wählen Sie **Zurücksetzen** aus, um vorherige Werte zu löschen.</span><span class="sxs-lookup"><span data-stu-id="68353-114">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="68353-115">Wählen Sie die Zeile **Anlagennummer** aus.</span><span class="sxs-lookup"><span data-stu-id="68353-115">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="68353-116">Geben Sie im Feld **Kriterien** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="68353-116">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="68353-117">Legen Sie die verbleibenden Kriterien für die Anlagen fest, die Sie mit diesem Vorschlag abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="68353-117">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="68353-118">Wählen Sie zweimal **OK** aus, um den Bereich zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="68353-118">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="68353-119">Überprüfen Sie die erstellten Transaktionspositionen.</span><span class="sxs-lookup"><span data-stu-id="68353-119">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="68353-120">Nur Anlagen mit dem Anschaffungsdatum und dem Anschaffungspreis, die im Buch festgelegt sind, werden in den Anschaffungsvorschlag einbezogen.</span><span class="sxs-lookup"><span data-stu-id="68353-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="68353-121">Wählen Sie auf der Seite die Registerkarte **Bücher** aus.</span><span class="sxs-lookup"><span data-stu-id="68353-121">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="68353-122">Wählen Sie **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="68353-122">Select **Post**.</span></span>
