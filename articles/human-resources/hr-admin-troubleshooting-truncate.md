---
title: Vermeiden Sie abgeschnittenen Text in der Positionshierarchie und beim Exportieren in Visio
description: In diesem Artikel wird erläutert, wie ein Problem gelöst wird, bei dem Namen von Einzelpersonen und Positionen abgeschnitten werden, wenn Kunden die Positionshierarchie in Microsoft Dynamics 365 Human Resources anzeigen. Das Abschneiden von Text erschwert das Erstellen von Screenshots oder das Drucken der Hierarchie.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dc723728801909c67cb823a043a2ae3e7eaf9f05
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892202"
---
# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a><span data-ttu-id="cbb93-104">Vermeiden Sie das Abschneiden von Text in der Positionshierarchie und beim Export nach Visio</span><span class="sxs-lookup"><span data-stu-id="cbb93-104">Avoid text truncation on the position hierarchy and export to Visio</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="cbb93-105">**Abgang**</span><span class="sxs-lookup"><span data-stu-id="cbb93-105">**Issue**</span></span>

<span data-ttu-id="cbb93-106">Wenn ein Kunde die Positionshierarchie in Microsoft Dynamics 365 Human Resources anzeigt, werden die Namen von Einzelpersonen und Positionen abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="cbb93-106">When a customer views the position hierarchy in Microsoft Dynamics 365 Human Resources, the names of individuals and positions are truncated.</span></span> <span data-ttu-id="cbb93-107">Daher kann es schwierig sein, ein Screenshot zu erstellen oder die Hierarchie zu drucken oder zu verteilen.</span><span class="sxs-lookup"><span data-stu-id="cbb93-107">Therefore, it can be difficult to take a screenshot, or to print and distribute the hierarchy.</span></span>

![Positionshierarchie](media/position-h.png)

<span data-ttu-id="cbb93-109">**Ursache**</span><span class="sxs-lookup"><span data-stu-id="cbb93-109">**Cause**</span></span>

<span data-ttu-id="cbb93-110">Dieses Verhalten ist beabsichtigt.</span><span class="sxs-lookup"><span data-stu-id="cbb93-110">This behavior is by design.</span></span>

<span data-ttu-id="cbb93-111">**Auflösung**</span><span class="sxs-lookup"><span data-stu-id="cbb93-111">**Resolution**</span></span>

<span data-ttu-id="cbb93-112">Leider können Benutzer die Größe des Texts nicht einfach ändern.</span><span class="sxs-lookup"><span data-stu-id="cbb93-112">Unfortunately, users can't easily change the size of the text.</span></span> <span data-ttu-id="cbb93-113">Sie können jedoch die Positionshierarchie von Human Resources heraus exportieren und sie dann in Microsoft Visio importieren.</span><span class="sxs-lookup"><span data-stu-id="cbb93-113">However, you can export the position hierarchy out of Human Resources and then import it into Microsoft Visio.</span></span> <span data-ttu-id="cbb93-114">Obwohl der folgende Artikel für Microsoft Dynamics AX 2012 verfasst wurde, gilt der Prozess nach wie vor für Human Resources: [Exportieren einer Positionshierarchie nach Microsoft Visio](/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).</span><span class="sxs-lookup"><span data-stu-id="cbb93-114">Although the following article was written for Microsoft Dynamics AX 2012, the process still applies to Human Resources: [Export a position hierarchy to Microsoft Visio](/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).</span></span>

<span data-ttu-id="cbb93-115">Gehen Sie folgendermaßen vor beim Export nach Visio.</span><span class="sxs-lookup"><span data-stu-id="cbb93-115">Follow these steps to export to Visio.</span></span>

1. <span data-ttu-id="cbb93-116">Öffnen Sie in Human Resources die Listenseite **Positionen**.</span><span class="sxs-lookup"><span data-stu-id="cbb93-116">In Human Resources, open the **Positions** list page.</span></span>

    <span data-ttu-id="cbb93-117">Um weitere Informationen im Organisationsstrukturdiagramm einzubeziehen, fügen Sie der Liste **Positionen** Felder hinzu, damit sie verfügbar sind, wenn Sie den Assistenten später in dieser Prozedur verwenden.</span><span class="sxs-lookup"><span data-stu-id="cbb93-117">To include more information in the organization structure diagram, add fields to the **Positions** list, so that they are available when you use the wizard later in this procedure.</span></span>

2. <span data-ttu-id="cbb93-118">Wählen Sie im Aktionsbereich die Schaltfläche **In Microsoft Office öffnen** aus, und wählen Sie dann unter **Nach Excel exportieren** die Option **Positionen** aus.</span><span class="sxs-lookup"><span data-stu-id="cbb93-118">On the Action Pane, select the **Open in Microsoft Office** button, and then, under **Export to Excel**, select **Positions**.</span></span> <span data-ttu-id="cbb93-119">Alternativ drücken Sie STRG+T.</span><span class="sxs-lookup"><span data-stu-id="cbb93-119">Alternatively, press Ctrl+T.</span></span>

    ![Exportieren der Listenseite „Positionen” nach Excel](media/org-admin.png)

3. <span data-ttu-id="cbb93-121">Speichern Sie die Excel-Datei, die exportiert wurde.</span><span class="sxs-lookup"><span data-stu-id="cbb93-121">Save the Excel file that is exported.</span></span>

    ![Dialogfeld „Nach Excel exportieren”](media/export-excel.png)

4. <span data-ttu-id="cbb93-123">Wählen Sie in Visio **Visio – Neue erstellen** und wählen Sie die Vorlagenkategorie **Unternehmen** aus.</span><span class="sxs-lookup"><span data-stu-id="cbb93-123">In Visio, select **Visio - Create New**, and select the **Business** template category.</span></span>

    ![Neues Diagramm](media/new.png)

5. <span data-ttu-id="cbb93-125">Wählen Sie **Organigramm-Assistent** und dann **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="cbb93-125">Select **Organization Chart Wizard**, and then select **Create**.</span></span>

    ![Dialogfeld „Organigramm-Assistent”](media/orgchart-wizard.png)

6. <span data-ttu-id="cbb93-127">Wählen Sie **Informationen, die bereits in einer Datei oder Datenbank gespeichert sind** aus, und wählen Sie dann **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="cbb93-127">Select **Information that's already stored in a file or database**, and then select **Next**.</span></span>

    ![Organigramm-Assistent 1](media/orgchart-wizard7.png)

7. <span data-ttu-id="cbb93-129">Wählen Sie **Ein Text, Organisation Plus (\*.txt) oder Excel-Datei** aus, und wählen Sie dann **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="cbb93-129">Choose **A text, Org Plus (\*.txt), or Excel file**, and then select **Next**.</span></span>

    ![Organigramm-Assistent 2](media/orgchart-wizard3.png)

8. <span data-ttu-id="cbb93-131">Navigieren Sie zur Auswahl der exportierten Excel-Datei, die die Positionshierarchie enthält, und wählen Sie dann **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="cbb93-131">Browse to select the exported Excel file that contains the position hierarchy, and then select **Next**.</span></span>

    ![Organigramm-Assistent 3](media/orgchart-wizard2.png)

9. <span data-ttu-id="cbb93-133">Legen Sie das Feld **Name** auf **Position** fest, legen Sie das Feld **Vorgesetzter** auf **Position des Vorgesetzten** fest, und wählen Sie dann **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="cbb93-133">Set the **Name** field to **Position**, set the **Reports to** field to **Reports to position**, and then select **Next**.</span></span>

    ![Organigramm-Assistent 4](media/orgchart-wizard1.png)

10. <span data-ttu-id="cbb93-135">Wählen Sie die Felder aus, die in jedem Knoten angezeigt werden sollen, und wählen Sie dann **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="cbb93-135">Select the fields that should be shown on each node, and then select **Next**.</span></span>

    ![Organigramm-Assistent 5](media/orgchart-wizard5.png)

11. <span data-ttu-id="cbb93-137">Fügen Sie die Spalte **Position** der Liste **Formdatenfelder** hinzu, und wählen Sie dann **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="cbb93-137">Add the **Position** column to the **Shape Data fields** list, and then select **Next**.</span></span>

    ![Organigramm-Assistent 6](media/orgchart-wizard6.png)

12. <span data-ttu-id="cbb93-139">Bilder sind aktuell nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="cbb93-139">Pictures aren't currently available.</span></span> <span data-ttu-id="cbb93-140">Daher wählen Sie auf der nächsten Seite **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="cbb93-140">Therefore, on the next page, select **Next**.</span></span>
13. <span data-ttu-id="cbb93-141">Wählen Sie **Ich möchte, dass der Assistent mein Organigramm über mehrere Seiten hinweg darstellt** aus.</span><span class="sxs-lookup"><span data-stu-id="cbb93-141">Select **I want the wizard to automatically break my organization chart across pages**.</span></span>

    ![Organigramm-Assistent 7](media/orgchart-wizard4.png)

14. <span data-ttu-id="cbb93-143">Wählen Sie **Fertig stellen** aus.</span><span class="sxs-lookup"><span data-stu-id="cbb93-143">Select **Finish**.</span></span>

    <span data-ttu-id="cbb93-144">Wenn es Positionen gibt, die sich nicht in der Struktur befinden, werden Sie dazu aufgefordert, sie im Diagramm einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="cbb93-144">If there are any positions that aren't in the structure, you're asked to include them in the diagram.</span></span>

<span data-ttu-id="cbb93-145">Das in Visio generierte Diagramm zeigt jeden Manager auf einem getrennten Arbeitsblatt an.</span><span class="sxs-lookup"><span data-stu-id="cbb93-145">The diagram that is generated in Visio shows each manager on a separate worksheet.</span></span>

<span data-ttu-id="cbb93-146">Anhand der Felder, die Sie ausgewählt haben, um sie ins Diagramm einzubeziehen, zeigt jeder Knoten die entsprechenden Informationen an, wenn die Visio-Datei generiert wird.</span><span class="sxs-lookup"><span data-stu-id="cbb93-146">Based on the fields that you selected to include in the diagram, each node shows the appropriate information when the Visio file is generated.</span></span>

![Hierarchiediagramm](media/hierarchy.png)

<span data-ttu-id="cbb93-148">**Zusätzliche Option**</span><span class="sxs-lookup"><span data-stu-id="cbb93-148">**Additional option**</span></span>

<span data-ttu-id="cbb93-149">In Human Resources sind Sie möglicherweise auch in der Lage, den Arbeitsbereich **Personen** zu verwenden, um der Hierarchie zugehörige Informationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cbb93-149">In Human Resources, you might also be able to use the **People** workspace to view some hierarchy-related information.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]