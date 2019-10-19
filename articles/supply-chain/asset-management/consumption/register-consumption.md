---
title: Verbrauch registrieren
description: In diesem Abschnitt wird erläutert, wie Sie den Verbrauch im Anlagenmanagement erfassen.
author: josaw1
manager: AnnBe
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 174c816c7a6442b07e4722c03045293b94c59153
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024659"
---
# <a name="register-consumption"></a><span data-ttu-id="e991d-103">Verbrauch registrieren</span><span class="sxs-lookup"><span data-stu-id="e991d-103">Register consumption</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="e991d-104">Wenn ein Wartungsauftrag abgeschlossen ist, ist der nächste Schritt die Verbrauchserfassung und die Buchung der Journale.</span><span class="sxs-lookup"><span data-stu-id="e991d-104">When a maintenance job has been completed on a work order, the next step is to make consumption registrations and post the journals.</span></span> <span data-ttu-id="e991d-105">Sie können Anmeldungen zu den folgenden Verbrauchsarten vornehmen: Stunden, Elemente und Ausgaben.</span><span class="sxs-lookup"><span data-stu-id="e991d-105">You can make registrations on the following consumption types: Hours, items, and expenses.</span></span> <span data-ttu-id="e991d-106">Die verschiedenen Verbrauchsarten werden erfasst und auf der Seite **Arbeitsauftragserfassungen** gebucht.</span><span class="sxs-lookup"><span data-stu-id="e991d-106">The different consumption types are registered and posted on the **Work order journals** page.</span></span> <span data-ttu-id="e991d-107">Die Erfassungseinrichtung in **Anlagenmanagement** dient der Erstellung und Buchung von separaten Journalen für Stunden, Posten und Ausgaben im Modul **Projektmanagement und Abrechnung**.</span><span class="sxs-lookup"><span data-stu-id="e991d-107">The journal setup in **Asset Management** is used for creating and posting separate journals for hours, items, and expenses in the **Project management and accounting** module.</span></span>

<span data-ttu-id="e991d-108">Sie könnenin einem Arbeitsauftrag Prognosezeile hinzufügen oder löschen.</span><span class="sxs-lookup"><span data-stu-id="e991d-108">You may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="e991d-109">Die Einrichtung eines Arbeitsauftrags-Lebenszykluszustands, der zugehörige Projekttyp und die mit dem Projekttyp verbundenen Stufenregeln bestimmen, ob Sie Erfassungszeilen hinzufügen oder bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="e991d-109">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determine if you are able to add or edit journal lines.</span></span> <span data-ttu-id="e991d-110">Lesen Sie mehr über den Lebenszyklus von Arbeitsaufträgen und die damit verbundenen Projektphasen unter [Integration in das Projektmanagement und Rechnungswesen](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span><span class="sxs-lookup"><span data-stu-id="e991d-110">Read more about work order lifecycle states and related project stages in [Integration to project management and accounting](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

>[!NOTE]
><span data-ttu-id="e991d-111">Es ist möglich, eine automatische Buchung von Erfassungen über den Lebenszyklus eines Arbeitsauftrags einzurichten.</span><span class="sxs-lookup"><span data-stu-id="e991d-111">It is possible to set up automatic posting of journals on a work order lifecycle state.</span></span> <span data-ttu-id="e991d-112">Weitere Informationen finden Sie unter [Lebenszykluszustand von Arbeitsaufträgen](../setup-for-work-orders/work-order-lifecycle-states.md).</span><span class="sxs-lookup"><span data-stu-id="e991d-112">Refer to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) for more information.</span></span>

1. <span data-ttu-id="e991d-113">Klicken Sie auf **Anlagenverwaltung** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge**.</span><span class="sxs-lookup"><span data-stu-id="e991d-113">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="e991d-114">Wählen Sie den Arbeitsauftrag aus und klicken Sie auf **Erfassungen**.</span><span class="sxs-lookup"><span data-stu-id="e991d-114">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="e991d-115">Klicken Sie auf **Kopieren von Prognose**, um alle Prognosepositionen zu übertragen, die mit dem Arbeitsauftrag verbunden sein können.</span><span class="sxs-lookup"><span data-stu-id="e991d-115">Click **Copy from forecast** to transfer any forecast lines that may be connected to the work order.</span></span> <span data-ttu-id="e991d-116">Sie können auswählen, welche Verbrauchsarten Sie übernehmen möchten.</span><span class="sxs-lookup"><span data-stu-id="e991d-116">You can select which consumption types you want to transfer.</span></span>

4. <span data-ttu-id="e991d-117">Bei Bedarf können Sie auf der entsprechenden FastTab weitere Verbrauchspositionen hinzufügen, indem Sie auf **Zeile hinzufügen** klicken und die Daten auf der Zeile ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="e991d-117">If necessary, you can add more consumption lines on the relevant FastTab by clicking **Add line** and filling out data on the line.</span></span>

5. <span data-ttu-id="e991d-118">Klicken Sie auf **Erfassungen validieren**, um die Erfassungszeilen vor der Buchung zu validieren.</span><span class="sxs-lookup"><span data-stu-id="e991d-118">Click **Validate journals** to validate the journal lines before posting.</span></span>

6. <span data-ttu-id="e991d-119">Klicken Sie auf **Erfassungen buchen**, um die Erfassungszeilen zu buchen.</span><span class="sxs-lookup"><span data-stu-id="e991d-119">Click **Post journals** to post the journal lines.</span></span>

7. <span data-ttu-id="e991d-120">Nachdem Sie die Verbrauchserfssungen gebucht haben, können Sie den Lebenszykluszustand des Arbeitsauftrags, z.B. auf „Beendet“, aktualisieren, um anzuzeigen, dass der Arbeitsauftrag abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="e991d-120">After you've posted the consumption journals, you can update the work order lifecycle state, for example to "Ended", to indicate that the work order has been completed.</span></span>

- <span data-ttu-id="e991d-121">Wählen Sie im Feld **Anzeigen** oben auf der Seite **Arbeitsauftragserfassungen** aus, welche Erfassungszeilen Sie sehen möchten: Alle, Nicht gebucht oder gebucht.</span><span class="sxs-lookup"><span data-stu-id="e991d-121">In the **Show** field placed at the top of the **Work order journals** page, select which journal lines you want to see: All, Not posted, or Posted.</span></span> <span data-ttu-id="e991d-122">Die gebuchten Erfassungen haben ein Häkchen im Kontrollkästchen **Gebucht**.</span><span class="sxs-lookup"><span data-stu-id="e991d-122">Posted journals have a check mark in the **Posted** check box.</span></span>  
- <span data-ttu-id="e991d-123">Wenn Artikelzeilen im Arbeitsauftragserfassungen erstellt werden, werden Produktdimensionen und Tracking-Dimensionen, die sich auf den Artikel beziehen, automatisch in die Journalzeile übertragen.</span><span class="sxs-lookup"><span data-stu-id="e991d-123">When item lines are created in the work order journal, product dimensions and tracking dimensions related to the item are automatically transferred to the journal line.</span></span>  

<span data-ttu-id="e991d-124">Der folgende Screenshot zeigt ein Beispiel für Stunden- und Artikelregistrierungen auf einem Arbeitsauftrag in **Arbeitsauftragserfassungen**.</span><span class="sxs-lookup"><span data-stu-id="e991d-124">The screenshot below shows an example of hour and item registrations on a work order in **Work order journals**.</span></span>

![Abbildung 1](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a><span data-ttu-id="e991d-126">Teilzeitarbeitszeit auf Arbeitsaufträgen mit mehreren Arbeitsaufträgen</span><span class="sxs-lookup"><span data-stu-id="e991d-126">Split hours on work orders with several work order jobs</span></span>

<span data-ttu-id="e991d-127">Wenn ein Arbeitsauftrag mehrere Arbeitsaufträge enthält, können Sie die Arbeitszeiten mit der Funktionalität **Stundenteilung** erfassen, d.h. eine Stundenregistrierungszeile kann gleichmäßig auf jeden Arbeitsauftrag verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="e991d-127">If a work order contains several work order jobs, you can register work hours using the **Split hours** functionality, meaning one hour registration line can be distributed evenly on each work order job.</span></span>

1. <span data-ttu-id="e991d-128">Klicken Sie auf **Anlagenverwaltung** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge**.</span><span class="sxs-lookup"><span data-stu-id="e991d-128">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="e991d-129">Wählen Sie den Arbeitsauftrag aus und klicken Sie auf **Erfassungen**.</span><span class="sxs-lookup"><span data-stu-id="e991d-129">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="e991d-130">Wählen Sie die Stundenregistrierungszeile aus, die Sie aufteilen möchten, und klicken Sie auf **Stunden teilen**.</span><span class="sxs-lookup"><span data-stu-id="e991d-130">Select the hour registration line you want to split, and click **Split hours**.</span></span>

4. <span data-ttu-id="e991d-131">Im Dialog **Stunden für Wartungsarbeiten am Arbeitsauftrag teilen** wird der Name des angemeldeten Mitarbeiters automatisch im Feld **Arbeiter** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e991d-131">In the **Split hours on work order maintenance jobs** dialog, the name of the worker who is logged in is automatically shown in the **Worker** field.</span></span> <span data-ttu-id="e991d-132">Bei Bedarf können Sie einen anderen Mitarbeiter auswählen.</span><span class="sxs-lookup"><span data-stu-id="e991d-132">If required, you can select another worker.</span></span>

5. <span data-ttu-id="e991d-133">Wählen Sie im Feld **Kategorie** eine Kategorie für die Stundenerfassung aus.</span><span class="sxs-lookup"><span data-stu-id="e991d-133">Select a category for the hour registration in the **Category** field.</span></span>

6. <span data-ttu-id="e991d-134">Geben Sie in das Feld **Stunden** die Anzahl der zu teilenden Arbeitsstunden ein.</span><span class="sxs-lookup"><span data-stu-id="e991d-134">Insert number of work hours to be split in the **Hours** field.</span></span>

![Abbildung 2](media/02-consumption.png)

7. <span data-ttu-id="e991d-136">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="e991d-136">Click **OK**.</span></span>

<span data-ttu-id="e991d-137">*Beispiel:* Im folgenden Screenshot werden Journalzeilen für einen Arbeitsauftrag mit drei Arbeitsaufträgen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e991d-137">*Example:* In the screenshot below, journal lines for a work order containing three work order jobs are shown.</span></span> <span data-ttu-id="e991d-138">Die erste Zeile mit drei Arbeitsstunden wurde aufgeteilt, und für jeden Arbeitsauftrag wird eine Arbeitsstunde registriert.</span><span class="sxs-lookup"><span data-stu-id="e991d-138">The first line, containing three work hours, has been split, and one work hour is registered on each work order job.</span></span> <span data-ttu-id="e991d-139">Nachdem die dreistündigen Registrierungszeilen erstellt wurden, entscheiden Sie, was mit der ursprünglichen Stundenregistrierungszeile (der ersten Zeile im Beispiel) geschehen soll.</span><span class="sxs-lookup"><span data-stu-id="e991d-139">After the three hour registration lines have been created, you decide what to do with the original hour registration line (the first line in the example).</span></span> <span data-ttu-id="e991d-140">Sie können es so lassen, wie es ist, oder es löschen.</span><span class="sxs-lookup"><span data-stu-id="e991d-140">You can keep it as is or delete it.</span></span> 

![Abbildung 3](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a><span data-ttu-id="e991d-142">Finanzielle Dimensionen der Verbrauchserfassung</span><span class="sxs-lookup"><span data-stu-id="e991d-142">Financial dimensions on consumption registrations</span></span>

<span data-ttu-id="e991d-143">Wenn Sie Verbrauchserfassungen durchführen, werden die Registrierungen in einer bestimmten Reihenfolge um finanzielle Aspekte der verschiedenen Registrierungsarten ergänzt.</span><span class="sxs-lookup"><span data-stu-id="e991d-143">When you make consumption registrations, financial dimensions related to the different registration types are added to the registrations in a specific sequence.</span></span> 

<span data-ttu-id="e991d-144">*Stunden- und Ausgabenregistrierungen:* Zunächst werden die finanziellen Dimensionen aus dem Erfassungs-Header hinzugefügt, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e991d-144">*Hour and Expense registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="e991d-145">Als nächstes werden die finanziellen Dimensionen aus dem zugehörigen Arbeitsauftragsprojekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e991d-145">Next, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="e991d-146">Schließlich werden die finanziellen Dimensionen der Ressource (Arbeiter) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e991d-146">Finally, financial dimensions from the resource (worker) are added.</span></span>

<span data-ttu-id="e991d-147">*Elementregistrierungen:* Zunächst werden finanzielle Dimensionen aus dem Erfassungskopf hinzugefügt, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e991d-147">*Item registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="e991d-148">Dann werden die finanziellen Dimensionen aus dem zugehörigen Arbeitsauftragsprojekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e991d-148">Then, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="e991d-149">Als nächstes werden die finanziellen Dimensionen des Standorts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e991d-149">Next, financial dimensions from the site are added.</span></span> <span data-ttu-id="e991d-150">Schließlich werden die finanziellen Dimensionen aus der Position hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e991d-150">Finally, financial dimensions from the item are added.</span></span>

>[!NOTE]
><span data-ttu-id="e991d-151">Für alle drei Registrierungsarten wird die Kombination der finanziellen Dimension validiert und ungültige Kombinationen werden ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="e991d-151">For all three registration types, the financial dimension combination is validated, and invalid combinations are blanked.</span></span> <span data-ttu-id="e991d-152">Dies ist Standardeinstellung in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e991d-152">This is standard setup in Finance and Operations.</span></span>

