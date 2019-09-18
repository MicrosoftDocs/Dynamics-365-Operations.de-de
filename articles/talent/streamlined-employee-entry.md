---
title: Fortschrittlicher Mitarbeitereintrag und ‑Navigation
description: Dateneingabe für Arbeitskräfte in Dynamics 365 for Talent wurde verbessert, um eine schnelle Eingabe für alle Mitarbeiter zu ermöglichen, und zwar für ehemalige, aktive und künftige Mitarbeiter. Vereinfachtes/konsolidiertes Navigationsmodell wurde aktualisiert, um zugehörige Informationen und Anzeigen rasch zu finden und erforderliche Aktualisierungen vornehmen zu können.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent October 2019 update
ms.openlocfilehash: be0253ffc4396f36050ef02c51a20d378e44473d
ms.sourcegitcommit: 4176c333ce3f88c5c68e95bd47e5791d32365dd2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/22/2019
ms.locfileid: "1918201"
---
# <a name="streamlined-employee-entry-and-navigation"></a><span data-ttu-id="0f245-104">Fortschrittlicher Mitarbeitereintrag und ‑Navigation</span><span class="sxs-lookup"><span data-stu-id="0f245-104">Streamlined employee entry and navigation</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0f245-105">Dynamics 365 for Talent ermöglicht effiziente Eingabe des Mitarbeiters sowie Beschäftigungsdaten.</span><span class="sxs-lookup"><span data-stu-id="0f245-105">Dynamics 365 for Talent allows efficient entry of employee and employment data.</span></span> <span data-ttu-id="0f245-106">Sie können die Arbeitsverlaufinformationen für vergangene, aktive und künftige Mitarbeiter und Auftragnehmer aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="0f245-106">You can quickly update work history information for past, active, and future employees and contractors.</span></span>

<span data-ttu-id="0f245-107">Sie können auch eine vereinfachte Navigationserfahrung aktivieren, um zugehörige Informationen schnell zu finden und erforderliche Änderungen vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="0f245-107">You can also enable a simplified navigation experience to quickly find related information and make any necessary changes.</span></span> <span data-ttu-id="0f245-108">Diese Funktionalität ist in der Sandboxumgebung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0f245-108">This functionality is now available in sandbox environments.</span></span> <span data-ttu-id="0f245-109">Um diese Funktion zu aktivieren, navigieren Sie zu **> Systemverwaltung > Verknüpfung > Einstellungen > Systemparameter- > Vorschaufunktionen**.</span><span class="sxs-lookup"><span data-stu-id="0f245-109">To turn this feature on, navigate to **System administration > Links > Setup > System parameters > Preview features**.</span></span> <span data-ttu-id="0f245-110">Wählen Sie **Verbessertes Arbeitskraftformular und Navigation** aus.</span><span class="sxs-lookup"><span data-stu-id="0f245-110">Select **Enhanced worker form and navigation**.</span></span> <span data-ttu-id="0f245-111">Dies aktiviert diese Änderungen für alle Benutzer.</span><span class="sxs-lookup"><span data-stu-id="0f245-111">This will enable these changes for all users.</span></span> <span data-ttu-id="0f245-112">Sie können diese Option jederzeit deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="0f245-112">You can turn this option off at any time.</span></span>

## <a name="view-options"></a><span data-ttu-id="0f245-113">Optionen anzeigen</span><span class="sxs-lookup"><span data-stu-id="0f245-113">View options</span></span>

<span data-ttu-id="0f245-114">Sie können **Ansichtsoptionen** im Arbeitskraftformular verwenden, um beliebige Kombination aus Mitarbeitern von Auftragnehmern und von einer Einheitsliste auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="0f245-114">You can use **View options** on the worker form to select any combination of employees and contractors from a single list.</span></span> <span data-ttu-id="0f245-115">Diese Optionen ermöglichen Ihnen, die Arbeitskräfte über juristischen Personen oder für die juristische Person anzuzeigen, für die Sie aktuell angemeldet sind.</span><span class="sxs-lookup"><span data-stu-id="0f245-115">These options allow you to view workers across legal entities or for the legal entity you're currently signed into.</span></span> <span data-ttu-id="0f245-116">Sie können auch die aktiven, ausstehenden und abgeschlossenen Arbeitskräfte anzeigen und Sie können Ergebnisse basierend auf dem Arbeitskrafttyp einschränken (Mitarbeiter oder Auftragnehmer).</span><span class="sxs-lookup"><span data-stu-id="0f245-116">You can also view active, pending, and exited workers, and you can restrict results based on the type of worker (employee or contractor).</span></span> <span data-ttu-id="0f245-117">Wenn die erweiterte Sicherheit aktiviert ist, werden nur die Mitarbeiter und Auftragnehmer in den juristischen Personen angezeigt, auf die Sie Zugriff haben.</span><span class="sxs-lookup"><span data-stu-id="0f245-117">If advanced security is enabled, you will only see those employees and contractors in the legal entities you have access to.</span></span>

<span data-ttu-id="0f245-118">Spalten in der Listenansicht ändern basierend auf der getroffenen Auswahl.</span><span class="sxs-lookup"><span data-stu-id="0f245-118">Columns in the list view change based on your selections.</span></span> <span data-ttu-id="0f245-119">Zum Beispiel wenn Sie ausgetretene Mitarbeiter anzeigen, wird das Kündigungsdatum und die erstellten Ursachencodes als zusätzliche Spalten in der Liste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0f245-119">For example, when viewing exited employees, the termination date and reason codes display as additional columns in the list.</span></span> 

<span data-ttu-id="0f245-120">[![Optionen anzeigen](./media/Worker-view-option.png)](./media/worker-view-option.png)</span><span class="sxs-lookup"><span data-stu-id="0f245-120">[![View options](./media/Worker-view-option.png)](./media/worker-view-option.png)</span></span>

## <a name="navigation-and-banner"></a><span data-ttu-id="0f245-121">Navigation und Banner</span><span class="sxs-lookup"><span data-stu-id="0f245-121">Navigation and banner</span></span>

<span data-ttu-id="0f245-122">Ein Banner zeigt die wichtigsten Informationen für jede Arbeitskraft an.</span><span class="sxs-lookup"><span data-stu-id="0f245-122">A banner displays key information for each worker.</span></span> <span data-ttu-id="0f245-123">Das aktive Banner für Arbeitskräfte zeigt die folgenden Felder an:</span><span class="sxs-lookup"><span data-stu-id="0f245-123">The banner for active workers displays the following fields:</span></span>

- <span data-ttu-id="0f245-124">**Titel**</span><span class="sxs-lookup"><span data-stu-id="0f245-124">**Title**</span></span>
- <span data-ttu-id="0f245-125">**Abteilung**</span><span class="sxs-lookup"><span data-stu-id="0f245-125">**Department**</span></span>
- <span data-ttu-id="0f245-126">**Positionstyp**</span><span class="sxs-lookup"><span data-stu-id="0f245-126">**Position type**</span></span>
- <span data-ttu-id="0f245-127">**Arbeitskrafttyp**</span><span class="sxs-lookup"><span data-stu-id="0f245-127">**Worker type**</span></span>
- <span data-ttu-id="0f245-128">**Vorgesetzter**</span><span class="sxs-lookup"><span data-stu-id="0f245-128">**Manager**</span></span>
- <span data-ttu-id="0f245-129">**Juristische Person**</span><span class="sxs-lookup"><span data-stu-id="0f245-129">**Legal entity**</span></span>

<span data-ttu-id="0f245-130">Das Banner für ausgetretene Arbeitskräfte zeigt die folgenden Felder an:</span><span class="sxs-lookup"><span data-stu-id="0f245-130">The banner for exited workers displays the following fields:</span></span>

- <span data-ttu-id="0f245-131">**Austrittsdatum**</span><span class="sxs-lookup"><span data-stu-id="0f245-131">**Exited date**</span></span>
- <span data-ttu-id="0f245-132">**Ursache**</span><span class="sxs-lookup"><span data-stu-id="0f245-132">**Reason**</span></span>

<span data-ttu-id="0f245-133">Das Banner für mögliche Arbeitskräfte zeigt die folgenden Felder an:</span><span class="sxs-lookup"><span data-stu-id="0f245-133">The banner for pending employees displays the following fields:</span></span>

- <span data-ttu-id="0f245-134">**Titel**</span><span class="sxs-lookup"><span data-stu-id="0f245-134">**Title**</span></span>
- <span data-ttu-id="0f245-135">**Abteilung**</span><span class="sxs-lookup"><span data-stu-id="0f245-135">**Department**</span></span>
- <span data-ttu-id="0f245-136">**Positionstyp**</span><span class="sxs-lookup"><span data-stu-id="0f245-136">**Position type**</span></span>
- <span data-ttu-id="0f245-137">**Vorgesetzter**</span><span class="sxs-lookup"><span data-stu-id="0f245-137">**Manager**</span></span>
- <span data-ttu-id="0f245-138">**Startdatum**</span><span class="sxs-lookup"><span data-stu-id="0f245-138">**Starting date**</span></span>
- <span data-ttu-id="0f245-139">**Juristische Person**</span><span class="sxs-lookup"><span data-stu-id="0f245-139">**Legal entity**</span></span>

<span data-ttu-id="0f245-140">Der Aktivitätsbereich auf der Arbeitskraftseite wurde neu organisiert, um weniger Optionen einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="0f245-140">The action pane of the worker page has been re-organized to include fewer options.</span></span> <span data-ttu-id="0f245-141">Informationen stehen nun in den folgenden Kategorien bereit:</span><span class="sxs-lookup"><span data-stu-id="0f245-141">Information is now organized in the following categories:</span></span> 

- <span data-ttu-id="0f245-142">Arbeit</span><span class="sxs-lookup"><span data-stu-id="0f245-142">Work</span></span>
- <span data-ttu-id="0f245-143">Person</span><span class="sxs-lookup"><span data-stu-id="0f245-143">Person</span></span>
- <span data-ttu-id="0f245-144">Verlasen</span><span class="sxs-lookup"><span data-stu-id="0f245-144">Leave</span></span>
- <span data-ttu-id="0f245-145">Kompensation</span><span class="sxs-lookup"><span data-stu-id="0f245-145">Compensation</span></span>
- <span data-ttu-id="0f245-146">Vergütungen</span><span class="sxs-lookup"><span data-stu-id="0f245-146">Benefits</span></span>
- <span data-ttu-id="0f245-147">Konformität</span><span class="sxs-lookup"><span data-stu-id="0f245-147">Compliance</span></span>

<span data-ttu-id="0f245-148">Zudem gibt es eine Registerkarte neue **Links** auf der Hauptarbeitskraftseite, die Benutzern einen zentralen Ort gibt, um auf alle zugehörigen Informationen für eine Arbeitskraft zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="0f245-148">In addtion, a new **Links** tab on the main worker page gives users a central location to access all related information for a worker.</span></span>

<span data-ttu-id="0f245-149">Aufgrund dieser Änderungen erscheinen Informationen möglicherweise an einem anderen Speicherort, als Sie ihn verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="0f245-149">Due to these changes, information may appear in a different location than you're used to.</span></span> <span data-ttu-id="0f245-150">Beispielsweise werden Lohndaten, die zuvor im Feld Arbeitskraftformular angezeigt wurden, nun im Aktivitätsbereich unter**Kompensation > Lohn** in der Registerkarte **Persönliche Daten** angezeigt, wo es nun eine Schaltfläche **Weitere Informationen** gibt, um Felder auszublenden, auf die häufig zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="0f245-150">For example, payroll information that previously displayed on the worker form now appears in the action pane under **Compensation > Payroll**, and the **Personal information** tab now has a **More information** button to hide fields that aren't accessed often.</span></span>

<span data-ttu-id="0f245-151">[![Banner](./media/Banner.png)](./media/Banner.png)</span><span class="sxs-lookup"><span data-stu-id="0f245-151">[![Banner](./media/Banner.png)](./media/Banner.png)</span></span>

## <a name="work-history"></a><span data-ttu-id="0f245-152">Arbeitshistorie</span><span class="sxs-lookup"><span data-stu-id="0f245-152">Work history</span></span>

<span data-ttu-id="0f245-153">Die Registerkarte **Arbeitsverlauf** zeigt den Verlauf für alle juristischen Personen und steht für ausgetretene, aktive und mögliche Mitarbeiter und Auftragnehmer bereit.</span><span class="sxs-lookup"><span data-stu-id="0f245-153">The **Work history** tab shows work history accross all legal entities and is available for exited, active, and pending employees and contractors.</span></span> <span data-ttu-id="0f245-154">Sie können nun der Verlauf der Arbeit auf einmal für die juristische Personen anzeigen, auf die Sie Zugriff haben.</span><span class="sxs-lookup"><span data-stu-id="0f245-154">You can now view all work history at once for the legal entities you have access to.</span></span> <span data-ttu-id="0f245-155">Zudem können Sie Informationen für jeden der Arbeitsverlaufeinträge bearbeiten, ohne den Datenenkontext zu ändern.</span><span class="sxs-lookup"><span data-stu-id="0f245-155">In addition, you can edit information for each of the work history entries without changing the data context.</span></span> <span data-ttu-id="0f245-156">Sie können alle Informationen direkt auf der Seite aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="0f245-156">You can update all information directly on the page.</span></span> 

<span data-ttu-id="0f245-157">[![Arbeitshistorie](./media/Worker-work-history.png)](./media/Worker-work-history.png)</span><span class="sxs-lookup"><span data-stu-id="0f245-157">[![Work history](./media/Worker-work-history.png)](./media/Worker-work-history.png)</span></span>

## <a name="position-history"></a><span data-ttu-id="0f245-158">Positionsverlauf</span><span class="sxs-lookup"><span data-stu-id="0f245-158">Position history</span></span>

<span data-ttu-id="0f245-159">Die Registerkarte **Positionen** auf der Hauptarbeitskraftseite enthält eine Vollansicht aller Positionen, die innerhalb der Organisation durch Personal besetzt werden, mit ausgetretenen, aktuellen und künftigen Zuweisungen.</span><span class="sxs-lookup"><span data-stu-id="0f245-159">The **Positions** tab on the main worker page provides a full view of all positions held within the organization, including past, present, and any future assignments.</span></span> <span data-ttu-id="0f245-160">Sie können direkt in den Positionsverlauf der Arbeitskraft im Aktivitätsbereich navigieren.</span><span class="sxs-lookup"><span data-stu-id="0f245-160">You can still navigate directly to the worker's position history in the action pane as well.</span></span>

<span data-ttu-id="0f245-161">[![Positionen](./media/Worker-position-history.png)](./media/Worker-position-history.png)</span><span class="sxs-lookup"><span data-stu-id="0f245-161">[![Positions](./media/Worker-position-history.png)](./media/Worker-position-history.png)</span></span>

