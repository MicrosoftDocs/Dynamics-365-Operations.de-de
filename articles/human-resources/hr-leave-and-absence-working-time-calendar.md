---
title: Erstellen eines Arbeitszeitkalenders
description: Definieren Sie einen Arbeitszeitkalender, Feiertage und arbeitsfreie Zeiten in Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8ea55ad7f86e0c7d5ccc6e6de0af475299b05639
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052432"
---
# <a name="create-a-working-time-calendar"></a><span data-ttu-id="f7668-103">Erstellen eines Arbeitszeitkalenders</span><span class="sxs-lookup"><span data-stu-id="f7668-103">Create a working time calendar</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f7668-104">Ein Arbeitszeitkalender in Dynamics 365 Human Resources zeigt die Tage und Stunden an, an denen Mitarbeiter in Ihrer Organisation arbeiten.</span><span class="sxs-lookup"><span data-stu-id="f7668-104">A working time calendar in Dynamics 365 Human Resources shows the days and hours that employees work in your organization.</span></span> <span data-ttu-id="f7668-105">Wenn ein Mitarbeiter eine Freistellung beantragt, muss er sich keine Gedanken über Feiertage und Schließungen machen.</span><span class="sxs-lookup"><span data-stu-id="f7668-105">When an employee submits a time-off request, they don't have to worry about holidays and closures.</span></span>

<span data-ttu-id="f7668-106">Konfigurieren Sie die folgenden Elemente für Ihre Organisation, um Anfragen nach Freizeit zu optimieren:</span><span class="sxs-lookup"><span data-stu-id="f7668-106">To streamline time-off requests, configure these items for your organization:</span></span>

- <span data-ttu-id="f7668-107">Arbeitszeitkalender</span><span class="sxs-lookup"><span data-stu-id="f7668-107">Working time calendar</span></span>
- <span data-ttu-id="f7668-108">Feiertage und Schließungen</span><span class="sxs-lookup"><span data-stu-id="f7668-108">Holidays and closures</span></span>
- <span data-ttu-id="f7668-109">Arbeitsfreie Zeit</span><span class="sxs-lookup"><span data-stu-id="f7668-109">Non-work time</span></span>

<span data-ttu-id="f7668-110">Sie können die letzten beiden Elemente hinzufügen, während Sie einen Arbeitszeitkalender einrichten.</span><span class="sxs-lookup"><span data-stu-id="f7668-110">You can add the last two items while you're setting up a working time calendar.</span></span> <span data-ttu-id="f7668-111">Sie können sie auch separat konfigurieren oder aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f7668-111">You can also configure or update them separately.</span></span>

## <a name="set-up-a-working-time-calendar"></a><span data-ttu-id="f7668-112">Einen Arbeitszeitkalender einrichten</span><span class="sxs-lookup"><span data-stu-id="f7668-112">Set up a working time calendar</span></span>

<span data-ttu-id="f7668-113">Richten Sie mindestens einen Arbeitszeitkalender ein, der Ihre Tage und Betriebsstunden anzeigt.</span><span class="sxs-lookup"><span data-stu-id="f7668-113">Set up at least one working time calendar that shows your days and hours of operation.</span></span> <span data-ttu-id="f7668-114">Wenn Sie Standorte in mehreren Ländern und Regionen haben, möchten Sie möglicherweise einen Arbeitszeitkalender für jeden Bereich einrichten.</span><span class="sxs-lookup"><span data-stu-id="f7668-114">If you have locations in multiple countries and regions, you might want to set up a working time calendar for each area.</span></span>

1. <span data-ttu-id="f7668-115">Klicken Sie auf der Seite **Organisationsadministration** auf **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="f7668-115">On the **Organization administration** page, select **Calendars**.</span></span>

2. <span data-ttu-id="f7668-116">Geben Sie unter **Neu** einen Namen und eine Beschreibung für Ihren Kalender ein.</span><span class="sxs-lookup"><span data-stu-id="f7668-116">Select **New** and enter a name and description for your calendar.</span></span>

3. <span data-ttu-id="f7668-117">Unter **Generierungsoptionen** wählen Sie die Arbeitstage für Ihre Organisation aus und geben Sie die Arbeitszeiten ein.</span><span class="sxs-lookup"><span data-stu-id="f7668-117">Under **Generation options**, select the work days for your organization and enter work times.</span></span> 
   - <span data-ttu-id="f7668-118">Um einen Feiertag oder eine Schließung hinzuzufügen, wählen Sie die Schaltfläche **Hinzufügen** neben **Feiertage und Schließungen**.</span><span class="sxs-lookup"><span data-stu-id="f7668-118">To add a holiday or closure, select the **Add** button next to **Holidays and closures**.</span></span>
   - <span data-ttu-id="f7668-119">Wählen Sie, um arbeitsfreie Zeiten wie Mittagessen oder Pausen hinzuzufügen, wählen Sie **Hinzufügen** unter **Arbeitsfreie Zeit** und geben Sie den Namen und den Zeitraum ein.</span><span class="sxs-lookup"><span data-stu-id="f7668-119">To add non-work time, like lunches or breaks, select **Add** under **NON-WORK TIME** and enter the name and time range.</span></span>

4. <span data-ttu-id="f7668-120">Unter **Tage** wählen Sie **Generieren**, um die Tage in dem Kalender zu generieren.</span><span class="sxs-lookup"><span data-stu-id="f7668-120">Under **Days**, select **Generate** to generate the days in your calendar.</span></span> <span data-ttu-id="f7668-121">Geben Sie den Datumsbereich für Ihren Kalender ein und wählen Sie dann **Tage generieren**.</span><span class="sxs-lookup"><span data-stu-id="f7668-121">Enter the date range for your calendar and then select **Generate days**.</span></span>

5. <span data-ttu-id="f7668-122">Um Arbeitszeitpläne hinzuzufügen, gehen Sie zu **Arbeitsplan** und wählen **Hinzufügen** und geben Sie dann die Zeiten für jeden Arbeitszeitplan ein.</span><span class="sxs-lookup"><span data-stu-id="f7668-122">To add work schedules, under **Work schedule**, select **Add** and then enter the times for each work schedule.</span></span>

## <a name="configure-holidays-and-closures"></a><span data-ttu-id="f7668-123">Feiertage und Schließungen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="f7668-123">Configure holidays and closures</span></span>

<span data-ttu-id="f7668-124">Sie können Feiertage und Schließungen separat von einem Arbeitszeitkalender hinzufügen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="f7668-124">You can add or change holidays and closures separately from a working time calendar.</span></span>

1. <span data-ttu-id="f7668-125">Klicken Sie auf der Seite **Organisationsadministration** auf **Feiertage und Schließungen**.</span><span class="sxs-lookup"><span data-stu-id="f7668-125">On the **Organization administration** page, select **Holidays and closures**.</span></span>

2. <span data-ttu-id="f7668-126">Geben Sie unter **Neu** einen neuen Namen und ein Datum für die Daten und Schließungen ein.</span><span class="sxs-lookup"><span data-stu-id="f7668-126">Select **New** and enter a name and date for the holiday or closure.</span></span>

## <a name="configure-non-work-time"></a><span data-ttu-id="f7668-127">Arbeitsfreie Zeit konfigurieren</span><span class="sxs-lookup"><span data-stu-id="f7668-127">Configure non-work time</span></span>

<span data-ttu-id="f7668-128">Sie können Feiertage und Schließungen separat von einem Arbeitszeitkalender hinzufügen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="f7668-128">You can add or change non-work times separately from a working time calendar.</span></span>

1. <span data-ttu-id="f7668-129">Klicken Sie auf der Seite **Organisationsadministration** auf **Arbeitsfreie Zeit**.</span><span class="sxs-lookup"><span data-stu-id="f7668-129">On the **Organization administration** page, select **Non-work time**.</span></span>

2. <span data-ttu-id="f7668-130">Wählen Sie **Neu** und geben Sie einen Namen und den Zeitraum für die arbeitsfreie Zeit ein.</span><span class="sxs-lookup"><span data-stu-id="f7668-130">Select **New** and enter a name and time range for the non-work time.</span></span>

<span data-ttu-id="f7668-131">Wenn Sie die Vorschau für Urlaubs- und Abwesenheitskorrekturen für Feiertage aktiviert haben, verwendet die Personalabteilung Feiertage und Schließungsdaten, um die Anzahl der Tage zu bestimmen, die für die im Kalender registrierten Mitarbeiter angepasst werden müssen.</span><span class="sxs-lookup"><span data-stu-id="f7668-131">If you've enabled the Leave and absence bank holiday corrections preview feature, Human Resources uses holidays and closure dates to determine the number of days to adjust for employees enrolled in the calendar.</span></span>

## <a name="see-also"></a><span data-ttu-id="f7668-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7668-132">See also</span></span>

- [<span data-ttu-id="f7668-133">Urlaubs- und Abwesenheitsübersicht</span><span class="sxs-lookup"><span data-stu-id="f7668-133">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="f7668-134">Urlaubs- und Abwesenheitstypen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="f7668-134">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]