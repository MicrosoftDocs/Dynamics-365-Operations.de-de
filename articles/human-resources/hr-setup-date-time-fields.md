---
title: Datums- und Zeitfelder verstehen
description: Verstehen, was zu erwarten ist, wenn Sie Datums- und Zeitfelder in Microsoft Dynamics 365 Human Resources verwenden.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3a8bc27bb4560b4a15aef483ff465c4b943bf02b
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889883"
---
# <a name="understand-date-and-time-fields"></a><span data-ttu-id="e33d6-103">Datums- und Zeitfelder verstehen</span><span class="sxs-lookup"><span data-stu-id="e33d6-103">Understand Date and Time fields</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="e33d6-104">**Datum und Uhrzeit** Felder sind ein grundlegendes Konzept in Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e33d6-104">**Date and Time** fields are a fundamental concept in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="e33d6-105">Es ist wichtig, zu verstehen, wie Sie mit **Datum und Uhrzeit**-Daten in Formularen, Dataverse und externen Quellen arbeiten.</span><span class="sxs-lookup"><span data-stu-id="e33d6-105">It's important to understand how to work with **Date and Time** data in forms, Dataverse, and external sources.</span></span>

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a><span data-ttu-id="e33d6-106">Differenz zwischen Datum sowie Datums- und Zeitfeld Datentypen verstehen</span><span class="sxs-lookup"><span data-stu-id="e33d6-106">Understanding the difference between Date and Date and Time field data types</span></span>

<span data-ttu-id="e33d6-107">**Datum und Uhrzeit** Felder enthalten Zeitzoneninformationen, wohingegen **Datum** Felder nicht.</span><span class="sxs-lookup"><span data-stu-id="e33d6-107">**Date and Time** fields contain time zone information, while **Date** fields don't.</span></span> <span data-ttu-id="e33d6-108">Felder **Datum** werden die gleichen Informationen in jeder beliebigen elektronischen Adresse anzeigen.</span><span class="sxs-lookup"><span data-stu-id="e33d6-108">**Date** fields display the same information in any location.</span></span> <span data-ttu-id="e33d6-109">Wenn Sie ein Datum in ein Feld **Datum** eingeben, schreibt Human Resources das gleiche Datum mit der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e33d6-109">When you enter a date into a **Date** field, Human Resources writes that same date to the database.</span></span>

<span data-ttu-id="e33d6-110">Wenn Daten in einem Feld **Datum und Uhrzeit** angezeigt werden, wird Human Resources das Datum und die Uhrzeit auf der Zeitzone des Benutzers anpassen, die im Formular **Benutzeroptionen** eingestellt sind (**Allgemein > Einstellungen > Benutzeroptionen**).</span><span class="sxs-lookup"><span data-stu-id="e33d6-110">When displaying data in a **Date and Time** field, Human Resources adjusts the date and time based on the user's time zone set in the **User Options** form (**Common > Setup > User Options**).</span></span> <span data-ttu-id="e33d6-111">Die Datums- und Uhrzeitinformationen, die Sie im Feld eingeben, sind die gleichen wie die Informationen, die in die Datenbank geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e33d6-111">The date and time information you enter in the field might not be the same as the information written to the database.</span></span>

<span data-ttu-id="e33d6-112">[![Formular Benutzeroptionen](./media/useroptionsform.png)](./media/useroptionsform.png)</span><span class="sxs-lookup"><span data-stu-id="e33d6-112">[![User options form](./media/useroptionsform.png)](./media/useroptionsform.png)</span></span>

## <a name="understanding-date-and-time-fields-in-forms"></a><span data-ttu-id="e33d6-113">Datums- und Zeitfelder in Formularen verstehen</span><span class="sxs-lookup"><span data-stu-id="e33d6-113">Understanding Date and Time fields in forms</span></span> 

<span data-ttu-id="e33d6-114">**Datum und Uhrzeit**-Daten, die auf dem Bildschirm angezeigt werden, sind nicht die gleichen wie die Daten, die in der Datenbank gespeichert werden, wenn die Zeitzone des Benutzers nicht in der koordinierten Weltzeit (UTC) festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="e33d6-114">**Date and Time** data displayed on the screen isn't the same as the data stored in the database if the user's time zone isn't set to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="e33d6-115">Daten in **Datum und Uhrzeit** Felder werden immer als UTC gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e33d6-115">Data in **Date and Time** fields is always stored as UTC.</span></span>

<span data-ttu-id="e33d6-116">[![Arbeitskraftformular UTC](./media/worker-form.png)](./media/worker-form.png)</span><span class="sxs-lookup"><span data-stu-id="e33d6-116">[![Worker form UTC](./media/worker-form.png)](./media/worker-form.png)</span></span>

## <a name="understand-date-and-time-fields-in-the-database"></a><span data-ttu-id="e33d6-117">Datums- und Zeitfelder in Formularen verstehen</span><span class="sxs-lookup"><span data-stu-id="e33d6-117">Understand Date and Time fields in the database</span></span> 

<span data-ttu-id="e33d6-118">Wenn Human Resources **Datum und Uhrzeit** Wert in die Datenbank schreibt, werden die Daten in UTC gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e33d6-118">When Human Resources writes a **Date and Time** value to the database, it stores the data in UTC.</span></span> <span data-ttu-id="e33d6-119">Dies ermöglicht es Benutzern, alle **Datum und Uhrzeit** Daten in der Zeitzone anzuzeigen, die in ihren Benutzeroptionen definiert wird.</span><span class="sxs-lookup"><span data-stu-id="e33d6-119">This allows users to see any **Date and Time** data relative to the time zone defined in their user options.</span></span>
 
<span data-ttu-id="e33d6-120">Im Beispiel oben ist die Startzeit ein Zeitpunkt, kein bestimmtes Datum.</span><span class="sxs-lookup"><span data-stu-id="e33d6-120">In the example above, the start time is a point in time, not a particular date.</span></span> <span data-ttu-id="e33d6-121">Durch das Ändern der Zeitzone des angemeldeten Benutzers für +12 GMT: 00 zu GMT UTC, zeigt derselbe Datensatz 04/30/2019 12:00: 00 statt 05/01/2019 12:00: 00.</span><span class="sxs-lookup"><span data-stu-id="e33d6-121">By changing the time zone of the logged in user from GMT +12:00 to GMT UTC, the same record shows 04/30/2019 12:00:00 instead of 05/01/2019 12:00:00.</span></span>
  
<span data-ttu-id="e33d6-122">Im Beispiel weiter unten wird das Beschäftigungsverhältnis des Mitarbeiters 000724 aktiv, unabhängig von der Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="e33d6-122">In the example below, employee 000724’s employment becomes active at the same time regardless of time zone.</span></span> <span data-ttu-id="e33d6-123">Der Mitarbeiter wird auf 04/30/2019 in der GMT-Zeitzone aktiv, die gleich ist wie 05/01/2019 in GMT+12:00 Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="e33d6-123">The employee will be active on 04/30/2019 in the GMT time zone, which is the same as 05/01/2019 in GMT+12:00 time zone.</span></span> <span data-ttu-id="e33d6-124">Beide beziehen sich auf den gleichen Zeitpunkt und nicht auf ein bestimmtes Datum.</span><span class="sxs-lookup"><span data-stu-id="e33d6-124">Both refer to the same point in time and not a particular date.</span></span> 

<span data-ttu-id="e33d6-125">[![Arbeitskraftformular GMT](./media/worker-form2.png)](./media/worker-form2.png)</span><span class="sxs-lookup"><span data-stu-id="e33d6-125">[![Worker form GMT](./media/worker-form2.png)](./media/worker-form2.png)</span></span>

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a><span data-ttu-id="e33d6-126">Datums- und Uhrzeitdaten im Datenverwaltungsframework, Excel, Dataverse und Power BI</span><span class="sxs-lookup"><span data-stu-id="e33d6-126">Date and Time data in Data Management Framework, Excel, Dataverse, and Power BI</span></span> 

<span data-ttu-id="e33d6-127">Datenverwaltungs-Framework, Excel-Add-In, Dataverse, und Power BI sind Berichte sind alle dazu entworfen, um mit Daten direkt in der Datenbankebene zu interagieren.</span><span class="sxs-lookup"><span data-stu-id="e33d6-127">The Data Management Framework, Excel Add-In, Dataverse, and Power BI reporting are all designed to interact with data directly on the database level.</span></span> <span data-ttu-id="e33d6-128">Da es keinen Clients auftritt, **Datum und Uhrzeit** Daten auf der Zeitzone des Benutzers angepasst, sind alle **Datum und Uhrzeit**-Werte in UTC, das auf mehrere falsche Annahmen führen kann, wenn Daten ein oder anzeigt.</span><span class="sxs-lookup"><span data-stu-id="e33d6-128">Since there's no client to adjust **Date and Time** data to the time zone of the user, all **Date and Time** values are in UTC, which can lead to some incorrect assumptions when entering or viewing data.</span></span>  
 
<span data-ttu-id="e33d6-129">**Datum und Uhrzeit** Daten, die zu DMF, Excel oder Dataverse übermittelt werden, werden wohl auch in UTC von der Datenbank verwendet.</span><span class="sxs-lookup"><span data-stu-id="e33d6-129">**Date and Time** data submitted via DMF, Excel, or Dataverse is assumed to be in UTC by the database.</span></span> <span data-ttu-id="e33d6-130">Dies kann einige Unklarheiten verursachen, wenn der **Datum und Uhrzeit** Wert nicht wie erwartete angezeigt wird, weil der Benutzer, der die Daten anzeigt, nicht die Zeitzone des Benutzers anzeigt, die in UTC festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e33d6-130">This can cause some confusion when the submitted **Date and Time** value doesn't display as expected because the user viewing the data doesn't have their user time zone  set to UTC.</span></span> 
 
<span data-ttu-id="e33d6-131">Dasselbe kann umgekehrt auftreten, wenn Daten exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="e33d6-131">The same thing can happen in reverse when data is exported.</span></span> <span data-ttu-id="e33d6-132">Die **Datum und Uhrzeit** Daten in der exportierten DMF-Entität können sich davon unterscheiden, was im Dynamics-Client angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e33d6-132">The **Date and Time** data in the exported DMF entity can be different than what is displayed in the Dynamics client.</span></span> 
 
<span data-ttu-id="e33d6-133">Wenn externe Quellen wie DMF verwendet werden, um Daten anzuzeigen oder zu erstellen, müssen Sie daran zu denken, dass **Datum und Uhrzeit**-Werte standardmäßig in UTC berücksichtigt werden, unabhängig von der Zeitzone des Computers des Benutzers oder der aktuellen Benutzerzeitzoneneinstellung.</span><span class="sxs-lookup"><span data-stu-id="e33d6-133">When using external sources like DMF to view or author data, keep in mind that the **Date and Time** values are considered by default to be in UTC regardless of the time zone of the user's computer or their current user time zone settings.</span></span> 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a><span data-ttu-id="e33d6-134">Beispiele desselben Datensatzes, der in verschiedenen Produktbereichen angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="e33d6-134">Examples of the same record being displayed in different product areas</span></span> 

<span data-ttu-id="e33d6-135">**Human Resources mit Benutzerzeitzone ist auf UTC festgelegt**</span><span class="sxs-lookup"><span data-stu-id="e33d6-135">**Human Resources with user time zone set to UTC**</span></span>

<span data-ttu-id="e33d6-136">[![Auf UTC festgelegtes Arbeiterformular](./media/worker-form3.png)](./media/worker-form3.png)</span><span class="sxs-lookup"><span data-stu-id="e33d6-136">[![Worker form set to UTC](./media/worker-form3.png)](./media/worker-form3.png)</span></span>

<span data-ttu-id="e33d6-137">**Human Resources mit Benutzerzeitzone ist auf GMT + 12.00 festgelegt**</span><span class="sxs-lookup"><span data-stu-id="e33d6-137">**Human Resources with user time zone set to GMT +12:00**</span></span> 

<span data-ttu-id="e33d6-138">[![Auf GMT festgelegtes Arbeiterformular](./media/worker-form4.png)](./media/worker-form4.png)</span><span class="sxs-lookup"><span data-stu-id="e33d6-138">[![Worker form set to GMT](./media/worker-form4.png)](./media/worker-form4.png)</span></span>

<span data-ttu-id="e33d6-139">**Excel über ODaten**</span><span class="sxs-lookup"><span data-stu-id="e33d6-139">**Excel Via OData**</span></span>

<span data-ttu-id="e33d6-140">[![Excel über ODaten](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span><span class="sxs-lookup"><span data-stu-id="e33d6-140">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span></span>

<span data-ttu-id="e33d6-141">**D;F Staging:-**</span><span class="sxs-lookup"><span data-stu-id="e33d6-141">**DMF Staging**</span></span>

<span data-ttu-id="e33d6-142">[![DMF Staging:-](./media/DMFStaging.png)](./media/DMFStaging.png)</span><span class="sxs-lookup"><span data-stu-id="e33d6-142">[![DMF Staging](./media/DMFStaging.png)](./media/DMFStaging.png)</span></span>

<span data-ttu-id="e33d6-143">**DMF Export**</span><span class="sxs-lookup"><span data-stu-id="e33d6-143">**DMF Export**</span></span>

<span data-ttu-id="e33d6-144">[![DMF-Export](./media/DMFexport.png)](./media/DMFexport.png)</span><span class="sxs-lookup"><span data-stu-id="e33d6-144">[![DMF Export](./media/DMFexport.png)](./media/DMFexport.png)</span></span>

<span data-ttu-id="e33d6-145">**Excel zu Dataverse**</span><span class="sxs-lookup"><span data-stu-id="e33d6-145">**Excel via Dataverse**</span></span>

<span data-ttu-id="e33d6-146">[![Excel zu Dataverse](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span><span class="sxs-lookup"><span data-stu-id="e33d6-146">[![Excel via Dataverse](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="e33d6-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e33d6-147">See also</span></span>

[<span data-ttu-id="e33d6-148">Datum und Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="e33d6-148">Date and time data</span></span>](/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[<span data-ttu-id="e33d6-149">Bevorzugte Zeitzone des Benutzers</span><span class="sxs-lookup"><span data-stu-id="e33d6-149">User preferred time zones</span></span>](/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]