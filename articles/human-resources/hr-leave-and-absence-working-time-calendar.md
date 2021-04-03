---
title: Erstellen eines Arbeitszeitkalenders
description: Definieren Sie einen Arbeitszeitkalender, Feiertage und arbeitsfreie Zeiten in Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ecabac54134629074ac01944963a037c2cdc63c9
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467168"
---
# <a name="create-a-working-time-calendar"></a><span data-ttu-id="eda67-103">Erstellen eines Arbeitszeitkalenders</span><span class="sxs-lookup"><span data-stu-id="eda67-103">Create a working time calendar</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="eda67-104">Ein Arbeitszeitkalender in Dynamics 365 Human Resources zeigt die Tage und Stunden an, an denen Mitarbeiter in Ihrer Organisation arbeiten.</span><span class="sxs-lookup"><span data-stu-id="eda67-104">A working time calendar in Dynamics 365 Human Resources shows the days and hours that employees work in your organization.</span></span> <span data-ttu-id="eda67-105">Wenn ein Mitarbeiter eine Freistellung beantragt, muss er sich keine Gedanken über Feiertage und Schließungen machen.</span><span class="sxs-lookup"><span data-stu-id="eda67-105">When an employee submits a time-off request, they don't have to worry about holidays and closures.</span></span>

<span data-ttu-id="eda67-106">Konfigurieren Sie die folgenden Elemente für Ihre Organisation, um Anfragen nach Freizeit zu optimieren:</span><span class="sxs-lookup"><span data-stu-id="eda67-106">To streamline time-off requests, configure these items for your organization:</span></span>

- <span data-ttu-id="eda67-107">Arbeitszeitkalender</span><span class="sxs-lookup"><span data-stu-id="eda67-107">Working time calendar</span></span>
- <span data-ttu-id="eda67-108">Feiertage und Schließungen</span><span class="sxs-lookup"><span data-stu-id="eda67-108">Holidays and closures</span></span>
- <span data-ttu-id="eda67-109">Arbeitsfreie Zeit</span><span class="sxs-lookup"><span data-stu-id="eda67-109">Non-work time</span></span>

<span data-ttu-id="eda67-110">Sie können die letzten beiden Elemente hinzufügen, während Sie einen Arbeitszeitkalender einrichten.</span><span class="sxs-lookup"><span data-stu-id="eda67-110">You can add the last two items while you're setting up a working time calendar.</span></span> <span data-ttu-id="eda67-111">Sie können sie auch separat konfigurieren oder aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="eda67-111">You can also configure or update them separately.</span></span>

## <a name="set-up-a-working-time-calendar"></a><span data-ttu-id="eda67-112">Einen Arbeitszeitkalender einrichten</span><span class="sxs-lookup"><span data-stu-id="eda67-112">Set up a working time calendar</span></span>

<span data-ttu-id="eda67-113">Richten Sie mindestens einen Arbeitszeitkalender ein, der Ihre Tage und Betriebsstunden anzeigt.</span><span class="sxs-lookup"><span data-stu-id="eda67-113">Set up at least one working time calendar that shows your days and hours of operation.</span></span> <span data-ttu-id="eda67-114">Wenn Sie Standorte in mehreren Ländern und Regionen haben, möchten Sie möglicherweise einen Arbeitszeitkalender für jeden Bereich einrichten.</span><span class="sxs-lookup"><span data-stu-id="eda67-114">If you have locations in multiple countries and regions, you might want to set up a working time calendar for each area.</span></span>

1. <span data-ttu-id="eda67-115">Klicken Sie auf der Seite **Organisationsadministration** auf **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="eda67-115">On the **Organization administration** page, select **Calendars**.</span></span>

2. <span data-ttu-id="eda67-116">Geben Sie unter **Neu** einen Namen und eine Beschreibung für Ihren Kalender ein.</span><span class="sxs-lookup"><span data-stu-id="eda67-116">Select **New** and enter a name and description for your calendar.</span></span>

3. <span data-ttu-id="eda67-117">Unter **Generierungsoptionen** wählen Sie die Arbeitstage für Ihre Organisation aus und geben Sie die Arbeitszeiten ein.</span><span class="sxs-lookup"><span data-stu-id="eda67-117">Under **Generation options**, select the work days for your organization and enter work times.</span></span> 
   - <span data-ttu-id="eda67-118">Um einen Feiertag oder eine Schließung hinzuzufügen, wählen Sie die Schaltfläche **Hinzufügen** neben **Feiertage und Schließungen**.</span><span class="sxs-lookup"><span data-stu-id="eda67-118">To add a holiday or closure, select the **Add** button next to **Holidays and closures**.</span></span>
   - <span data-ttu-id="eda67-119">Wählen Sie, um arbeitsfreie Zeiten wie Mittagessen oder Pausen hinzuzufügen, wählen Sie **Hinzufügen** unter **Arbeitsfreie Zeit** und geben Sie den Namen und den Zeitraum ein.</span><span class="sxs-lookup"><span data-stu-id="eda67-119">To add non-work time, like lunches or breaks, select **Add** under **NON-WORK TIME** and enter the name and time range.</span></span>

4. <span data-ttu-id="eda67-120">Unter **Tage** wählen Sie **Generieren**, um die Tage in dem Kalender zu generieren.</span><span class="sxs-lookup"><span data-stu-id="eda67-120">Under **Days**, select **Generate** to generate the days in your calendar.</span></span> <span data-ttu-id="eda67-121">Geben Sie den Datumsbereich für Ihren Kalender ein und wählen Sie dann **Tage generieren**.</span><span class="sxs-lookup"><span data-stu-id="eda67-121">Enter the date range for your calendar and then select **Generate days**.</span></span>

5. <span data-ttu-id="eda67-122">Um Arbeitszeitpläne hinzuzufügen, gehen Sie zu **Arbeitsplan** und wählen **Hinzufügen** und geben Sie dann die Zeiten für jeden Arbeitszeitplan ein.</span><span class="sxs-lookup"><span data-stu-id="eda67-122">To add work schedules, under **Work schedule**, select **Add** and then enter the times for each work schedule.</span></span>

## <a name="configure-holidays-and-closures"></a><span data-ttu-id="eda67-123">Feiertage und Schließungen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="eda67-123">Configure holidays and closures</span></span>

<span data-ttu-id="eda67-124">Sie können Feiertage und Schließungen separat von einem Arbeitszeitkalender hinzufügen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="eda67-124">You can add or change holidays and closures separately from a working time calendar.</span></span>

1. <span data-ttu-id="eda67-125">Klicken Sie auf der Seite **Organisationsadministration** auf **Feiertage und Schließungen**.</span><span class="sxs-lookup"><span data-stu-id="eda67-125">On the **Organization administration** page, select **Holidays and closures**.</span></span>

2. <span data-ttu-id="eda67-126">Geben Sie unter **Neu** einen neuen Namen und ein Datum für die Daten und Schließungen ein.</span><span class="sxs-lookup"><span data-stu-id="eda67-126">Select **New** and enter a name and date for the holiday or closure.</span></span>

## <a name="configure-non-work-time"></a><span data-ttu-id="eda67-127">Arbeitsfreie Zeit konfigurieren</span><span class="sxs-lookup"><span data-stu-id="eda67-127">Configure non-work time</span></span>

<span data-ttu-id="eda67-128">Sie können Feiertage und Schließungen separat von einem Arbeitszeitkalender hinzufügen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="eda67-128">You can add or change non-work times separately from a working time calendar.</span></span>

1. <span data-ttu-id="eda67-129">Klicken Sie auf der Seite **Organisationsadministration** auf **Arbeitsfreie Zeit**.</span><span class="sxs-lookup"><span data-stu-id="eda67-129">On the **Organization administration** page, select **Non-work time**.</span></span>

2. <span data-ttu-id="eda67-130">Wählen Sie **Neu** und geben Sie einen Namen und den Zeitraum für die arbeitsfreie Zeit ein.</span><span class="sxs-lookup"><span data-stu-id="eda67-130">Select **New** and enter a name and time range for the non-work time.</span></span>

<span data-ttu-id="eda67-131">Wenn Sie die Vorschau für Urlaubs- und Abwesenheitskorrekturen für Feiertage aktiviert haben, verwendet die Personalabteilung Feiertage und Schließungsdaten, um die Anzahl der Tage zu bestimmen, die für die im Kalender registrierten Mitarbeiter angepasst werden müssen.</span><span class="sxs-lookup"><span data-stu-id="eda67-131">If you've enabled the Leave and absence bank holiday corrections preview feature, Human Resources uses holidays and closure dates to determine the number of days to adjust for employees enrolled in the calendar.</span></span>

## <a name="see-also"></a><span data-ttu-id="eda67-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eda67-132">See also</span></span>

- [<span data-ttu-id="eda67-133">Urlaubs- und Abwesenheitsübersicht</span><span class="sxs-lookup"><span data-stu-id="eda67-133">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="eda67-134">Urlaubs- und Abwesenheitstypen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="eda67-134">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]