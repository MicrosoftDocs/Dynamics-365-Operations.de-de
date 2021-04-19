---
title: Anlagenanschaffungen vorschlagen
description: In diesem Thema wird beschrieben, wie eine Anlage mithilfe des Anschaffungsvorschlags in der Anlagenerfassung angeschafft wird.
author: saraschi2
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d529cd53b41827a78b282afd4d2c69d2f2db555e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817164"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="71d2c-103">Anlagenanschaffungen vorschlagen</span><span class="sxs-lookup"><span data-stu-id="71d2c-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="71d2c-104">In diesem Thema wird beschrieben, wie eine Anlage mithilfe des Anschaffungsvorschlags in der Anlagenerfassung angeschafft wird.</span><span class="sxs-lookup"><span data-stu-id="71d2c-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="71d2c-105">Dabei werden die Buchhalterrolle und die Demodaten für die juristische Person USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="71d2c-105">It uses the accountant role and demo data for the USMF legal entity.</span></span> <span data-ttu-id="71d2c-106">Um eine Anlage durch eine Anlagenerfassung zu erwerben, müssen Sie zuerst den Anlagendatensatz erstellen und dann den Anschaffungspreis im Anlagenbuch festlegen.</span><span class="sxs-lookup"><span data-stu-id="71d2c-106">To acquire a fixed asset through a fixed asset proposal journal, you must first create the fixed asset record, and then define the acquisition price in the asset book.</span></span>

## <a name="create-an-asset-acquisition-proposal"></a><span data-ttu-id="71d2c-107">Vorschlag zum Anlagenerwerb erstellen</span><span class="sxs-lookup"><span data-stu-id="71d2c-107">Create an asset acquisition proposal</span></span>

<span data-ttu-id="71d2c-108">Führen Sie die folgenden Schritte aus, um einen Vorschlag zum Anlagenerwerb zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="71d2c-108">Complete the following steps to create an asset acquisition proposal.</span></span> 

1. <span data-ttu-id="71d2c-109">Gehen Sie im Navigationsbereich zu **Module > Anlage > Journalbuchungen > Anlagenbuchhaltung**.</span><span class="sxs-lookup"><span data-stu-id="71d2c-109">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="71d2c-110">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="71d2c-110">Select **New**.</span></span>
3. <span data-ttu-id="71d2c-111">Geben Sie im Feld **Name** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="71d2c-111">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="71d2c-112">Wählen Sie im Aktivitätsbereich **Positionen** aus.</span><span class="sxs-lookup"><span data-stu-id="71d2c-112">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="71d2c-113">Wählen Sie **Vorschläge** aus.</span><span class="sxs-lookup"><span data-stu-id="71d2c-113">Select **Proposals**.</span></span>
6. <span data-ttu-id="71d2c-114">Wählen Sie **Anschaffungsvorschlag** aus.</span><span class="sxs-lookup"><span data-stu-id="71d2c-114">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="71d2c-115">Wählen Sie **Filter** aus.</span><span class="sxs-lookup"><span data-stu-id="71d2c-115">Select **Filter**.</span></span> <span data-ttu-id="71d2c-116">Wählen Sie **Zurücksetzen** aus, um vorherige Werte zu löschen.</span><span class="sxs-lookup"><span data-stu-id="71d2c-116">Select **Reset** to clear previous values.</span></span>
8. <span data-ttu-id="71d2c-117">Wählen Sie die Zeile **Anlagennummer** aus.</span><span class="sxs-lookup"><span data-stu-id="71d2c-117">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="71d2c-118">Geben Sie im Feld **Kriterien** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="71d2c-118">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="71d2c-119">Legen Sie die verbleibenden Kriterien für die Anlagen fest, die Sie mit diesem Vorschlag abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="71d2c-119">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="71d2c-120">Wählen Sie zweimal **OK** aus, um den Bereich zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="71d2c-120">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="71d2c-121">Überprüfen Sie, ob die Transaktionspositionen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="71d2c-121">Verify that the transaction lines are created.</span></span>  
- <span data-ttu-id="71d2c-122">Nur Anlagen mit dem Anschaffungsdatum und dem Anschaffungspreis, die im Buch festgelegt sind, werden in den Anschaffungsvorschlag einbezogen.</span><span class="sxs-lookup"><span data-stu-id="71d2c-122">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="71d2c-123">Wählen Sie auf der Seite die Registerkarte **Bücher** aus.</span><span class="sxs-lookup"><span data-stu-id="71d2c-123">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="71d2c-124">Wählen Sie **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="71d2c-124">Select **Post**.</span></span>

## <a name="include-default-financial-dimensions-in-an-acquisition-proposal"></a><span data-ttu-id="71d2c-125">Standardfinanzdimensionen in einen Anschaffungsvorschlag aufnehmen</span><span class="sxs-lookup"><span data-stu-id="71d2c-125">Include default financial dimensions in an acquisition proposal</span></span>

<span data-ttu-id="71d2c-126">Die Anschaffungstransaktion kann mithilfe von Excel-Add-Ins erstellt werden, indem Sie zu **Anlagen > Journaleinträge > Anlagenerfassung** gehen.</span><span class="sxs-lookup"><span data-stu-id="71d2c-126">The acquisition transaction can be created using Excel add-ins, by going to **Fixed assets > Journal entries > Fixed asset journal**.</span></span> <span data-ttu-id="71d2c-127">Erstellen Sie eine neue Erfassung und wechseln Sie zum **Positionen**-Abschnitt auf der Seite und wählen Sie das Excel-Symbol und dann eine Anlagenerfassungsposition.</span><span class="sxs-lookup"><span data-stu-id="71d2c-127">Create a new journal and move to the **Lines** section on the page and select the Excel icon, and then select a Fixed asset journal line.</span></span> <span data-ttu-id="71d2c-128">Das System erstellt und öffnet eine Excel-Vorlage, die Erfassungspositionen darstellt.</span><span class="sxs-lookup"><span data-stu-id="71d2c-128">The system will create and open an Excel template representing journal lines.</span></span> <span data-ttu-id="71d2c-129">Sie können Daten für die Erfassungspositionen hinzufügen, die Sie der Vorlage hinzufügen, und diese Informationen dann wieder im System veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="71d2c-129">You can add data for the journal lines you're adding into the template, and then publish that information back into the system.</span></span> 

<span data-ttu-id="71d2c-130">Wenn für das ausgewählte Anlagenbuch und die entsprechenden Anlagen, die in die Excel-Vorlage eingegeben wurden, Standarddimensionen eingerichtet wurden, werden die Standardfinanzdimensionen von den Anlagenbuch-Masterdaten aufgerufen, wenn die Erfassung aus Excel heraus im System veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="71d2c-130">If default dimensions have been set up for the selected asset book and the corresponding fixed assets that were entered in the Excel template, the default financial dimensions will be called from the asset book master data when the journal is published from the Excel to the system.</span></span> <span data-ttu-id="71d2c-131">Um Finanzdimensionen automatisch in ein Anlagenbuch aufzunehmen, während die Anlagenerfassung über das Excel-Add-In veröffentlicht wird, müssen die Standarddimensionen im Voraus eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="71d2c-131">To include financial dimensions on an asset book automatically while publishing the fixed asset journal from the Excel add-in, the default dimensions must be set up in advance.</span></span>  


[!INCLUDE [footer-include](../../../includes/footer-banner.md)]
