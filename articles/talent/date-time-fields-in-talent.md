---
title: Arbeiten mit Datum und Uhrzeit in Microsoft Dynamics 365 Talent
description: Verstehen, was zu erwarten ist, wenn Sie Datums- und Zeitfelder in Microsoft Dynamics 365 Talent verwenden. Erhalten Sie Klarheit, was Sie erwartet, wenn Sie mit Datums- und Zeitdaten in einem Formular in Talent interagieren, als externe Quelle, oder in Common Data Service.
author: Darinkramer
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-06-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: abd215243cbda68ba3f57b5fa41054a10745d11f
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551025"
---
# <a name="work-with-date-and-time-in-microsoft-dynamics-365-talent"></a><span data-ttu-id="bca7c-104">Arbeiten mit Datum und Uhrzeit in Microsoft Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="bca7c-104">Work with date and time in Microsoft Dynamics 365 Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bca7c-105">**Datum und Uhrzeit** Felder sind ein grundlegendes Konzept in Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="bca7c-105">**Date and Time** fields are a fundamental concept in Dynamics 365 Talent.</span></span> <span data-ttu-id="bca7c-106">Es ist wichtig, zu verstehen, wie **Datum und Uhrzeit** Daten in einem Dynamics 365 Formular, Common Data Service, und externen Quellen arbeiten.</span><span class="sxs-lookup"><span data-stu-id="bca7c-106">It's important to understand how to work with **Date and Time** data in a Dynamics 365 form, Common Data Service, and external sources.</span></span>

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a><span data-ttu-id="bca7c-107">Differenz zwischen Datum sowie Datums- und Zeitfeld Datentypen verstehen</span><span class="sxs-lookup"><span data-stu-id="bca7c-107">Understanding the difference between Date and Date and Time field data types</span></span>

<span data-ttu-id="bca7c-108">**Datum und Uhrzeit** Felder enthalten Zeitzoneninformationen, wohingegen **Datum** Felder nicht.</span><span class="sxs-lookup"><span data-stu-id="bca7c-108">**Date and Time** fields contain time zone information, while **Date** fields don't.</span></span> <span data-ttu-id="bca7c-109">Felder **Datum** werden die gleichen Informationen in jeder beliebigen elektronischen Adresse anzeigen.</span><span class="sxs-lookup"><span data-stu-id="bca7c-109">**Date** fields display the same information in any location.</span></span> <span data-ttu-id="bca7c-110">Wenn Sie ein Datum in ein Feld **Datum** eingeben, schreibt Talent das gleiche Datum mit der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="bca7c-110">When you enter a date into a **Date** field, Talent writes that same date to the database.</span></span>

<span data-ttu-id="bca7c-111">Wenn Daten in einem Feld **Datum und Uhrzeit** angezeigt werden, wird Talent das Datum und die Uhrzeit auf der Zeitzone des Benutzers anpassen, die im Formular **Benutzeroptionen** eingestellt sind (**Allgemein > Einstellungen > Benutzeroptionen**).</span><span class="sxs-lookup"><span data-stu-id="bca7c-111">When displaying data in a **Date and Time** field, Talent adjusts the date and time based on the user's time zone set in the **User Options** form (**Common > Setup > User Options**).</span></span> <span data-ttu-id="bca7c-112">Die Datums- und Uhrzeitinformationen, die Sie im Feld eingeben, sind die gleichen wie die Informationen, die in die Datenbank geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="bca7c-112">The date and time information you enter in the field might not be the same as the information written to the database.</span></span>

<span data-ttu-id="bca7c-113">[![Formular Benutzeroptionen](./media/useroptionsform.png)](./media/useroptionsform.png)</span><span class="sxs-lookup"><span data-stu-id="bca7c-113">[![User options form](./media/useroptionsform.png)](./media/useroptionsform.png)</span></span>

## <a name="understanding-date-and-time-fields-in-forms"></a><span data-ttu-id="bca7c-114">Datums- und Zeitfelder in Formularen verstehen</span><span class="sxs-lookup"><span data-stu-id="bca7c-114">Understanding Date and Time fields in forms</span></span> 

<span data-ttu-id="bca7c-115">Wenn sie Daten in einem Feld **Datum und Uhrzeit** eingeben, sind die Daten, die auf dem Bildschirm angezeigt werden, nicht die gleichen wie die Daten, die in der Datenbank gespeichert werden, wenn die Zeitzone des Benutzers nicht in der koordinierten Weltzeit (UTC) festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="bca7c-115">When entering data in a **Date and Time** field, the data displayed on the screen isn't the same as the data stored in the database if the user's time zone isn't set to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="bca7c-116">Daten in **Datum und Uhrzeit** Felder werden immer als UTC gespeichert.</span><span class="sxs-lookup"><span data-stu-id="bca7c-116">Data in **Date and Time** fields is always stored as UTC.</span></span>

<span data-ttu-id="bca7c-117">[![Formular Arbeitskraft](./media/worker-form.png)](./media/worker-form.png)</span><span class="sxs-lookup"><span data-stu-id="bca7c-117">[![Worker form](./media/worker-form.png)](./media/worker-form.png)</span></span>

## <a name="understand-date-and-time-fields-in-the-database"></a><span data-ttu-id="bca7c-118">Datums- und Zeitfelder in Formularen verstehen</span><span class="sxs-lookup"><span data-stu-id="bca7c-118">Understand Date and Time fields in the database</span></span> 

<span data-ttu-id="bca7c-119">Wenn Talent **Datum und Uhrzeit** Wert in die Datenbank schreibt, werden die Daten in UTC gespeichert.</span><span class="sxs-lookup"><span data-stu-id="bca7c-119">When Talent writes a **Date and time** value to the database, it stores the data in UTC.</span></span> <span data-ttu-id="bca7c-120">Dies ermöglicht es Benutzern, alle **Datum und Uhrzeit** Daten in der Zeitzone anzuzeigen, die in ihren Benutzeroptionen definiert wird.</span><span class="sxs-lookup"><span data-stu-id="bca7c-120">This allows users to see any **Date and Time** data relative to the time zone defined in their user options.</span></span>
 
<span data-ttu-id="bca7c-121">Im Beispiel oben ist die Startzeit ein Zeitpunkt, kein bestimmtes Datum.</span><span class="sxs-lookup"><span data-stu-id="bca7c-121">In the example above, the start time is a point in time, not a particular date.</span></span> <span data-ttu-id="bca7c-122">Durch das Ändern der Zeitzone des angemeldeten Benutzers für +12 GMT: 00 zu GMT UTC, wird dieselbe Anzeige erstellt die  04/30/2019 12:00: 00 statt 05/01/2019 12:00: 00 anzeigt.</span><span class="sxs-lookup"><span data-stu-id="bca7c-122">By changing the time zone of the logged in user from GMT +12:00 to GMT UTC, the same record just created shows 04/30/2019 12:00:00 instead of 05/01/2019 12:00:00.</span></span>
  
<span data-ttu-id="bca7c-123">Im Beispiel weiter unten wird das Beschäftigungsverhältnis des Mitarbeiters 000724 aktiv, unabhängig von der Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="bca7c-123">In the example below, employee 000724’s employment becomes active at the same time regardless of time zone.</span></span> <span data-ttu-id="bca7c-124">Der Mitarbeiter wird auf 04/30/2019 in der GMT-Zeitzone aktiv, die gleich ist wie 05/01/2019 in GMT+12:00 Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="bca7c-124">The employee will be active on 04/30/2019 in the GMT time zone, which is the same as 05/01/2019 in GMT+12:00 time zone.</span></span> <span data-ttu-id="bca7c-125">Beide beziehen sich auf den gleichen Zeitpunkt und nicht auf ein bestimmtes Datum.</span><span class="sxs-lookup"><span data-stu-id="bca7c-125">Both refer to the same point in time and not a particular date.</span></span> 

<span data-ttu-id="bca7c-126">[![Formular Arbeitskraft](./media/worker-form2.png)](./media/worker-form2.png)</span><span class="sxs-lookup"><span data-stu-id="bca7c-126">[![Worker form](./media/worker-form2.png)](./media/worker-form2.png)</span></span>

## <a name="date-and-time-data-in-data-management-framework-excel-common-data-service-and-power-bi"></a><span data-ttu-id="bca7c-127">Datums- und Uhrzeitdaten im Datenverwaltungsframework, Excel, Common Data Service und Power BI</span><span class="sxs-lookup"><span data-stu-id="bca7c-127">Date and Time data in Data Management Framework, Excel, Common Data Service, and Power BI</span></span> 

<span data-ttu-id="bca7c-128">Datenverwaltungs-Framework, Excel-Add-In, Common Data Service, und Power BI sind Berichte sind alle dazu entworfen, um mit Daten direkt in der Datenbankebene zu interagieren.</span><span class="sxs-lookup"><span data-stu-id="bca7c-128">The Data Management Framework, Excel Add-In, Common Data Service, and Power BI reporting are all designed to interact with data directly on the database level.</span></span> <span data-ttu-id="bca7c-129">Da es keinen Clients auftritt, **Datum und Uhrzeit** Daten auf der Zeitzone des Benutzers angepasst, sind alle **Datum und Uhrzeit**-Werte in UTC, das auf mehrere falsche Annahmen führen kann, wenn Daten ein oder anzeigt.</span><span class="sxs-lookup"><span data-stu-id="bca7c-129">Since there is no client to adjust **Date and Time** data to the time zone of the user, all **Date and Time** values are in UTC, which can lead to some incorrect assumptions when entering or viewing data.</span></span>  
 
<span data-ttu-id="bca7c-130">**Datum und Uhrzeit** Daten, die zu DMF, Excel oder Common Data Service übermittelt werden, werden wohl auch in UTC von der Datenbank verwendet.</span><span class="sxs-lookup"><span data-stu-id="bca7c-130">**Date and Time** data that is submitted via DMF, Excel, or Common Data Service is assumed to be in UTC by the database.</span></span> <span data-ttu-id="bca7c-131">Dies kann einige Unklarheiten verursachen, wenn der **Datum und Uhrzeit** Wert nicht wie erwartete angezeigt wird, weil der Benutzer, der die Daten anzeigt, nicht die Zeitzone des Benutzers anzeigt, die in UTC festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="bca7c-131">This can cause some confusion when the submitted **Date and Time** value doesn't display as expected because the user viewing the data doesn't have their user time zone  set to UTC.</span></span> 
 
<span data-ttu-id="bca7c-132">Dasselbe kann umgekehrt auftreten, wenn Daten exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="bca7c-132">The same thing can happen in reverse when data is exported.</span></span> <span data-ttu-id="bca7c-133">Die **Datum und Uhrzeit** Daten in der exportierten DMF-Entität können sich davon unterscheiden, was im Dynamics-Client angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="bca7c-133">The **Date and Time** data in the exported DMF entity can be different then what is displayed in the Dynamics client.</span></span> 
 
<span data-ttu-id="bca7c-134">Wenn externe Quellen wie DMF verwendet werden, um Daten anzuzeigen oder zu erstellen, ist es wichtig, daran zu denken, dass **Datum und Uhrzeit**-Werte standardmäßig in UTC berücksichtigt werden, unabhängig von der Zeitzone des Computers des Benutzers oder der aktuellen Benutzerzeitzoneneinstellung.</span><span class="sxs-lookup"><span data-stu-id="bca7c-134">When using external sources like DMF to view or author data, it is important to keep in mind that the **Date and Time** values are considered by default to be in UTC regardless of the time zone of the user's computer or their current user time zone settings.</span></span> 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a><span data-ttu-id="bca7c-135">Beispiele desselben Datensatzes, der in verschiedenen Produktbereichen angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="bca7c-135">Examples of the same record being displayed in different product areas</span></span> 

<span data-ttu-id="bca7c-136">**Talent mit Benutzerzeitzone ist auf UTC festgelegt**</span><span class="sxs-lookup"><span data-stu-id="bca7c-136">**Talent with user time zone set to UTC**</span></span>

<span data-ttu-id="bca7c-137">[![Formular Arbeitskraft](./media/worker-form3.png)](./media/worker-form3.png)</span><span class="sxs-lookup"><span data-stu-id="bca7c-137">[![Worker form](./media/worker-form3.png)](./media/worker-form3.png)</span></span>

<span data-ttu-id="bca7c-138">**Talent mit Benutzerzeitzone ist auf GMT + 12:00 festgelegt**</span><span class="sxs-lookup"><span data-stu-id="bca7c-138">**Talent with user time zone set to GMT +12:00**</span></span> 

<span data-ttu-id="bca7c-139">[![Formular Arbeitskraft](./media/worker-form4.png)](./media/worker-form4.png)</span><span class="sxs-lookup"><span data-stu-id="bca7c-139">[![Worker form](./media/worker-form4.png)](./media/worker-form4.png)</span></span>

<span data-ttu-id="bca7c-140">**Excel über ODaten**</span><span class="sxs-lookup"><span data-stu-id="bca7c-140">**Excel Via OData**</span></span>

<span data-ttu-id="bca7c-141">[![Excel über ODaten](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span><span class="sxs-lookup"><span data-stu-id="bca7c-141">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span></span>

<span data-ttu-id="bca7c-142">**D;F Staging:-**</span><span class="sxs-lookup"><span data-stu-id="bca7c-142">**DMF Staging**</span></span>

<span data-ttu-id="bca7c-143">[![DMF Staging:-](./media/DMFStaging.png)](./media/DMFStaging.png)</span><span class="sxs-lookup"><span data-stu-id="bca7c-143">[![DMF Staging](./media/DMFStaging.png)](./media/DMFStaging.png)</span></span>

<span data-ttu-id="bca7c-144">**DMF Export**</span><span class="sxs-lookup"><span data-stu-id="bca7c-144">**DMF Export**</span></span>

<span data-ttu-id="bca7c-145">[![DMF Staging:-](./media/DMFexport.png)](./media/DMFexport.png)</span><span class="sxs-lookup"><span data-stu-id="bca7c-145">[![DMF Staging](./media/DMFexport.png)](./media/DMFexport.png)</span></span>

<span data-ttu-id="bca7c-146">**Excel zu Common Data Service**</span><span class="sxs-lookup"><span data-stu-id="bca7c-146">**Excel via Common Data Service**</span></span>

<span data-ttu-id="bca7c-147">[![Excel zu Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span><span class="sxs-lookup"><span data-stu-id="bca7c-147">[![Excel via Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span></span>

### <a name="see-also"></a><span data-ttu-id="bca7c-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bca7c-148">See also</span></span>

[<span data-ttu-id="bca7c-149">Datum und Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="bca7c-149">Date and time data</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[<span data-ttu-id="bca7c-150">Bevorzugte Zeitzone des Benutzers</span><span class="sxs-lookup"><span data-stu-id="bca7c-150">User preferred time zones</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 
