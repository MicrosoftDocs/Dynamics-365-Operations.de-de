---
title: Verbrauch registrieren
description: In diesem Abschnitt wird erläutert, wie Sie den Verbrauch im Anlagenmanagement erfassen.
author: josaw1
manager: tfehr
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderJournal, EntAssetWorkOrderAddSparePart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2c9bbd51da23ea412bc124f932f73876a9506d47
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428817"
---
# <a name="register-consumption"></a><span data-ttu-id="a972c-103">Verbrauch registrieren</span><span class="sxs-lookup"><span data-stu-id="a972c-103">Register consumption</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="a972c-104">Wenn ein Wartungsauftrag abgeschlossen ist, ist der nächste Schritt die Verbrauchserfassung und die Buchung der Journale.</span><span class="sxs-lookup"><span data-stu-id="a972c-104">When a maintenance job has been completed on a work order, the next step is to make consumption registrations and post the journals.</span></span> <span data-ttu-id="a972c-105">Sie können Anmeldungen zu den folgenden Verbrauchsarten vornehmen: Stunden, Elemente und Ausgaben.</span><span class="sxs-lookup"><span data-stu-id="a972c-105">You can make registrations on the following consumption types: Hours, items, and expenses.</span></span> <span data-ttu-id="a972c-106">Die verschiedenen Verbrauchsarten werden erfasst und auf der Seite **Arbeitsauftragserfassungen** gebucht.</span><span class="sxs-lookup"><span data-stu-id="a972c-106">The different consumption types are registered and posted on the **Work order journals** page.</span></span> <span data-ttu-id="a972c-107">Die Erfassungseinrichtung in **Anlagenmanagement** dient der Erstellung und Buchung von separaten Journalen für Stunden, Posten und Ausgaben im Modul **Projektmanagement und Abrechnung**.</span><span class="sxs-lookup"><span data-stu-id="a972c-107">The journal setup in **Asset Management** is used for creating and posting separate journals for hours, items, and expenses in the **Project management and accounting** module.</span></span>

<span data-ttu-id="a972c-108">In einigen Fällen können Sie einem Arbeitsauftrag Prognosezeile hinzufügen oder löschen.</span><span class="sxs-lookup"><span data-stu-id="a972c-108">In some cases, you may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="a972c-109">Die Einrichtung eines Arbeitsauftrags-Lebenszykluszustands, der zugehörige Projekttyp und die mit dem Projekttyp verbundenen Stufenregeln bestimmen, ob Sie Erfassungszeilen hinzufügen oder bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="a972c-109">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determine if you are able to add or edit journal lines.</span></span> <span data-ttu-id="a972c-110">Weitere Informationen über den Lebenszyklus von Arbeitsaufträgen und die damit verbundenen Projektphasen finden Sie unter [Prognosen, Arbeitsaufträge und Projekte](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span><span class="sxs-lookup"><span data-stu-id="a972c-110">Read more about work order lifecycle states and related project stages in [Forecasts, work orders, and projects](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

>[!NOTE]
><span data-ttu-id="a972c-111">Es ist möglich, eine automatische Buchung von Erfassungen über den Lebenszyklus eines Arbeitsauftrags einzurichten.</span><span class="sxs-lookup"><span data-stu-id="a972c-111">It is possible to set up automatic posting of journals on a work order lifecycle state.</span></span> <span data-ttu-id="a972c-112">Weitere Informationen finden Sie unter [Lebenszykluszustand von Arbeitsaufträgen](../setup-for-work-orders/work-order-lifecycle-states.md).</span><span class="sxs-lookup"><span data-stu-id="a972c-112">Refer to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) for more information.</span></span>

1. <span data-ttu-id="a972c-113">Klicken Sie auf **Anlagenverwaltung** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge**.</span><span class="sxs-lookup"><span data-stu-id="a972c-113">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="a972c-114">Wählen Sie den Arbeitsauftrag aus und klicken Sie auf **Erfassungen**.</span><span class="sxs-lookup"><span data-stu-id="a972c-114">Select the work order, and click **Journals**.</span></span>

3. <span data-ttu-id="a972c-115">Klicken Sie auf **Kopieren von Prognose**, um alle Prognosepositionen zu übertragen, die mit dem Arbeitsauftrag verbunden sein können.</span><span class="sxs-lookup"><span data-stu-id="a972c-115">Click **Copy from forecast** to transfer any forecast lines that may be connected to the work order.</span></span> <span data-ttu-id="a972c-116">Sie können auswählen, welche Verbrauchsarten Sie übernehmen möchten.</span><span class="sxs-lookup"><span data-stu-id="a972c-116">You can select which consumption types you want to transfer.</span></span>

4. <span data-ttu-id="a972c-117">Bei Bedarf können Sie auf der entsprechenden FastTab weitere Verbrauchspositionen hinzufügen, indem Sie auf **Zeile hinzufügen** klicken und die Daten auf der Zeile ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="a972c-117">If necessary, you can add more consumption lines on the relevant FastTab by clicking **Add line** and filling out data on the line.</span></span>

5. <span data-ttu-id="a972c-118">Klicken Sie auf **Erfassungen validieren**, um die Erfassungszeilen vor der Buchung zu validieren.</span><span class="sxs-lookup"><span data-stu-id="a972c-118">Click **Validate journals** to validate the journal lines before posting.</span></span>

6. <span data-ttu-id="a972c-119">Klicken Sie auf **Erfassungen buchen**, um die Erfassungszeilen zu buchen.</span><span class="sxs-lookup"><span data-stu-id="a972c-119">Click **Post journals** to post the journal lines.</span></span>

7. <span data-ttu-id="a972c-120">Nachdem Sie die Verbrauchserfassungen gebucht haben, können Sie den Arbeitsauftragslebenszyklusstatus aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a972c-120">After you've posted the consumption journals, you can update the work order lifecycle state.</span></span> <span data-ttu-id="a972c-121">Beispielsweise um anzugeben, dass der Arbeitsauftrag abgeschlossen wurde, können Sie den Lebenszyklusstatus in „Abgeschlossen“ aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a972c-121">For example, to indicate that the work order has been completed, you can update the lifecycle state to "Ended".</span></span>

    - <span data-ttu-id="a972c-122">Wählen Sie im Feld **Anzeigen** oben auf der Seite **Arbeitsauftragserfassungen** aus, welche Erfassungszeilen Sie sehen möchten: **Alle**, **Nicht gebucht** oder **Gebucht**.</span><span class="sxs-lookup"><span data-stu-id="a972c-122">In the **Show** field at the top of the **Work order journals** page, select which journal lines you want to see: **All**, **Not posted**, or **Posted**.</span></span> <span data-ttu-id="a972c-123">Die gebuchten Erfassungen haben ein Häkchen im Kontrollkästchen **Gebucht**.</span><span class="sxs-lookup"><span data-stu-id="a972c-123">Posted journals have a check mark in the **Posted** check box.</span></span>  
    - <span data-ttu-id="a972c-124">Wenn Artikelzeilen im Arbeitsauftragserfassungen erstellt werden, werden Produktdimensionen und Tracking-Dimensionen, die sich auf den Artikel beziehen, automatisch in die Journalzeile übertragen.</span><span class="sxs-lookup"><span data-stu-id="a972c-124">When item lines are created in the work order journal, product dimensions and tracking dimensions related to the item are automatically transferred to the journal line.</span></span>  

<span data-ttu-id="a972c-125">Der folgende Screenshot zeigt ein Beispiel für Stunden- und Artikelregistrierungen auf einem Arbeitsauftrag in **Arbeitsauftragserfassungen**.</span><span class="sxs-lookup"><span data-stu-id="a972c-125">The screenshot below shows an example of hour and item registrations on a work order in **Work order journals**.</span></span>

![Abbildung 1](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a><span data-ttu-id="a972c-127">Teilzeitarbeitszeit auf Arbeitsaufträgen mit mehreren Arbeitsaufträgen</span><span class="sxs-lookup"><span data-stu-id="a972c-127">Split hours on work orders with several work order jobs</span></span>

<span data-ttu-id="a972c-128">Wenn ein Arbeitsauftrag mehrere Arbeitsaufträge enthält, können Sie die Arbeitszeiten mit der Funktionalität **Stundenteilung** erfassen, d.h. eine Stundenregistrierungszeile kann gleichmäßig auf jeden Arbeitsauftrag verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="a972c-128">If a work order contains several work order jobs, you can register work hours using the **Split hours** functionality, meaning one hour registration line can be distributed evenly on each work order job.</span></span>

1. <span data-ttu-id="a972c-129">Klicken Sie auf **Anlagenverwaltung** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge**.</span><span class="sxs-lookup"><span data-stu-id="a972c-129">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="a972c-130">Wählen Sie den Arbeitsauftrag aus und klicken Sie auf **Erfassungen**.</span><span class="sxs-lookup"><span data-stu-id="a972c-130">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="a972c-131">Wählen Sie die Stundenregistrierungszeile aus, die Sie aufteilen möchten, und klicken Sie auf **Stunden teilen**.</span><span class="sxs-lookup"><span data-stu-id="a972c-131">Select the hour registration line you want to split, and click **Split hours**.</span></span>

4. <span data-ttu-id="a972c-132">Im Dialog **Stunden für Wartungsarbeiten am Arbeitsauftrag teilen** wird der Name des angemeldeten Mitarbeiters automatisch im Feld **Arbeiter** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a972c-132">In the **Split hours on work order maintenance jobs** dialog, the name of the worker who is logged in is automatically shown in the **Worker** field.</span></span> <span data-ttu-id="a972c-133">Bei Bedarf können Sie einen anderen Mitarbeiter auswählen.</span><span class="sxs-lookup"><span data-stu-id="a972c-133">If required, you can select another worker.</span></span>

5. <span data-ttu-id="a972c-134">Wählen Sie im Feld **Kategorie** eine Kategorie für die Stundenerfassung aus.</span><span class="sxs-lookup"><span data-stu-id="a972c-134">Select a category for the hour registration in the **Category** field.</span></span>

6. <span data-ttu-id="a972c-135">Geben Sie in das Feld **Stunden** die Anzahl der zu teilenden Arbeitsstunden ein.</span><span class="sxs-lookup"><span data-stu-id="a972c-135">Insert number of work hours to be split in the **Hours** field.</span></span>

    ![Abbildung 2](media/02-consumption.png)

7. <span data-ttu-id="a972c-137">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="a972c-137">Click **OK**.</span></span>

<span data-ttu-id="a972c-138">*Beispiel:* Im folgenden Screenshot werden Journalzeilen für einen Arbeitsauftrag mit drei Arbeitsaufträgen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a972c-138">*Example:* In the screenshot below, journal lines for a work order containing three work order jobs are shown.</span></span> <span data-ttu-id="a972c-139">Die erste Zeile mit drei Arbeitsstunden wurde aufgeteilt, und für jeden Arbeitsauftrag wird eine Arbeitsstunde registriert.</span><span class="sxs-lookup"><span data-stu-id="a972c-139">The first line, containing three work hours, has been split, and one work hour is registered on each work order job.</span></span> <span data-ttu-id="a972c-140">Nachdem die dreistündigen Registrierungszeilen erstellt wurden, entscheiden Sie, was mit der ursprünglichen Stundenregistrierungszeile (der ersten Zeile im Beispiel) geschehen soll.</span><span class="sxs-lookup"><span data-stu-id="a972c-140">After the three hour registration lines have been created, you decide what to do with the original hour registration line (the first line in the example).</span></span> <span data-ttu-id="a972c-141">Sie können es so lassen, wie es ist, oder es löschen.</span><span class="sxs-lookup"><span data-stu-id="a972c-141">You can keep it as is or delete it.</span></span> 

![Abbildung 3](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a><span data-ttu-id="a972c-143">Finanzielle Dimensionen der Verbrauchserfassung</span><span class="sxs-lookup"><span data-stu-id="a972c-143">Financial dimensions on consumption registrations</span></span>

<span data-ttu-id="a972c-144">Wenn Sie Verbrauchserfassungen durchführen, werden die Registrierungen in einer bestimmten Reihenfolge um finanzielle Aspekte der verschiedenen Registrierungsarten ergänzt.</span><span class="sxs-lookup"><span data-stu-id="a972c-144">When you make consumption registrations, financial dimensions related to the different registration types are added to the registrations in a specific sequence.</span></span> 

- <span data-ttu-id="a972c-145">*Stunden- und Ausgabenregistrierungen:* Zunächst werden die finanziellen Dimensionen aus dem Erfassungs-Header hinzugefügt, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a972c-145">*Hour and Expense registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="a972c-146">Als nächstes werden die finanziellen Dimensionen aus dem zugehörigen Arbeitsauftragsprojekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a972c-146">Next, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="a972c-147">Schließlich werden die finanziellen Dimensionen der Ressource (Arbeiter) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a972c-147">Finally, financial dimensions from the resource (worker) are added.</span></span>

- <span data-ttu-id="a972c-148">*Elementregistrierungen:* Zunächst werden finanzielle Dimensionen aus dem Erfassungskopf hinzugefügt, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a972c-148">*Item registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="a972c-149">Dann werden die finanziellen Dimensionen aus dem zugehörigen Arbeitsauftragsprojekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a972c-149">Then, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="a972c-150">Als nächstes werden die finanziellen Dimensionen des Standorts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a972c-150">Next, financial dimensions from the site are added.</span></span> <span data-ttu-id="a972c-151">Schließlich werden die finanziellen Dimensionen aus der Position hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a972c-151">Finally, financial dimensions from the item are added.</span></span>

>[!NOTE]
><span data-ttu-id="a972c-152">Für alle drei Registrierungsarten wird die Kombination der finanziellen Dimension validiert und ungültige Kombinationen werden ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="a972c-152">For all three registration types, the financial dimension combination is validated, and invalid combinations are blanked.</span></span> <span data-ttu-id="a972c-153">Dies ist Standard-Setup mit anderen Finance and Operations Apps.</span><span class="sxs-lookup"><span data-stu-id="a972c-153">This is standard setup with other Finance and Operations apps.</span></span>

