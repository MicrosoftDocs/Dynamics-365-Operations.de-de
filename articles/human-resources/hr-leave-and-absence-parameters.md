---
title: Beurlaubungs- und Abwesenheitsparameter konfigurieren
description: Definieren Sie Personalparameter für Urlaub und Abwesenheit in Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 11/02/2020
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
ms.openlocfilehash: c3a3f4a8a1fa0b5dbc4869f81f091cc66437e978
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056851"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="2e9af-103">Beurlaubungs- und Abwesenheitsparameter konfigurieren</span><span class="sxs-lookup"><span data-stu-id="2e9af-103">Configure leave and absence parameters</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="2e9af-104">Bevor Sie Urlaubs- und Abwesenheitspläne einrichten in Dynamics 365 Human Resourcesi st es eine gute Idee, die Einstellungen für alle zugehörigen Personalparameter zu überprüfen, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="2e9af-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="2e9af-105">Nummernfolge für Urlaubsanträge</span><span class="sxs-lookup"><span data-stu-id="2e9af-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="2e9af-106">Family and Medical Leave Act (FMLA) Einstellungen</span><span class="sxs-lookup"><span data-stu-id="2e9af-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="2e9af-107">Self-Service-Einstellungen für Mitarbeiter für Urlaubs- und Abwesenheitsanträge</span><span class="sxs-lookup"><span data-stu-id="2e9af-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="2e9af-108">Urlaubs- und Abwesenheitsparameter</span><span class="sxs-lookup"><span data-stu-id="2e9af-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="2e9af-109">Personalverwaltungsparameter anzeigen und ändern</span><span class="sxs-lookup"><span data-stu-id="2e9af-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="2e9af-110">Auf der Seite **Urlaub- und Abwesenheit** klicken Sie auf die Registerkarte **Links**.</span><span class="sxs-lookup"><span data-stu-id="2e9af-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="2e9af-111">Unter **Einrichtung** wählen Sie **Personalverwaltungsparameter einrichten**.</span><span class="sxs-lookup"><span data-stu-id="2e9af-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="2e9af-112">Auf der **Zahlenfolgen** Registerkarte, überprüfen Sie die **Zahlenfolgecode** für **Urlaubsanfragen-ID** und ändern Sie nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="2e9af-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="2e9af-113">Diese Einstellung legt die Reihenfolge fest, in der IDs zum automatischen Zuweisen von IDs für Urlaubsanforderungen.</span><span class="sxs-lookup"><span data-stu-id="2e9af-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="2e9af-114">Auf der **FMLA** Registerkarte, überprüfen Sie die FMLA-Einstellungen und ändern Sie sie nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="2e9af-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="2e9af-115">Auf der Registerkarte **Mitarbeiter-Selbstservice** geben Sie an, ob Manager Urlaubs- und Abwesenheitsanträge für ihre Mitarbeiter eingeben können.</span><span class="sxs-lookup"><span data-stu-id="2e9af-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

7. <span data-ttu-id="2e9af-116">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="2e9af-116">Select **Save**.</span></span>

>[!IMPORTANT]
><span data-ttu-id="2e9af-117">Urlaub und Abwesenheit wird in verschiedenen Unternehmen derzeit in der Vorschau angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2e9af-117">Viewing leave and absence across companies is currently in preview.</span></span> <span data-ttu-id="2e9af-118">Um die Urlaubs- und Abwesenheitsoption anzuzeigen, müssen Sie sie in Ihrer **Sandbox**-Umgebung aktivieren.</span><span class="sxs-lookup"><span data-stu-id="2e9af-118">You'll need to enable it in your **Sandbox** environment to display the option for leave and absence.</span></span> <span data-ttu-id="2e9af-119">Weitere Informationen zum Aktivieren der Vorschaufunktionen finden Sie unter [Funktonen verwalten](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="2e9af-119">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="view-and-change-human-resources-shared-parameters"></a><span data-ttu-id="2e9af-120">Freigegebenen Human Resources-Parameter anzeigen und ändern</span><span class="sxs-lookup"><span data-stu-id="2e9af-120">View and change Human resources shared parameters</span></span>

1. <span data-ttu-id="2e9af-121">Wählen Sie auf der Seite **Personalverwaltung** die Registerkarte **Links** aus.</span><span class="sxs-lookup"><span data-stu-id="2e9af-121">On the **Personnel management** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="2e9af-122">Unter **Einrichtung** wählen Sie **Freigegebene Human Resources-Parameter** aus.</span><span class="sxs-lookup"><span data-stu-id="2e9af-122">Under **Setup**, select **Human resources shared parameters**.</span></span>

3. <span data-ttu-id="2e9af-123">Wählen Sie in der Registerkarte **Vorabzugang** **Ja** bei **Unternehmensübergreifende Urlaubsansicht aktivieren**, damit der Urlaub unternehmensweit angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="2e9af-123">On the **Advance access** tab, select **Yes** for **Enable cross company leave view** to allow leave to be viewed across company.</span></span>

4. <span data-ttu-id="2e9af-124">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="2e9af-124">Select **Save**.</span></span>

## <a name="view-and-change-leave-and-absence-parameters"></a><span data-ttu-id="2e9af-125">Urlaub- und Abwesenheitsparameter anzeigen und ändern</span><span class="sxs-lookup"><span data-stu-id="2e9af-125">View and change leave and absence parameters</span></span>

1. <span data-ttu-id="2e9af-126">Auf der Seite **Urlaub- und Abwesenheit** klicken Sie auf die Registerkarte **Links**.</span><span class="sxs-lookup"><span data-stu-id="2e9af-126">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="2e9af-127">Unter **Installieren**, wählen Sie **Urlaubs- und Abwesenheitsparameter**.</span><span class="sxs-lookup"><span data-stu-id="2e9af-127">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="2e9af-128">Legen Sie auf der Registerkarte **Allgemein** die folgenden Parameter fest:</span><span class="sxs-lookup"><span data-stu-id="2e9af-128">On the **General** tab, set the following parameters:</span></span>
 
    - <span data-ttu-id="2e9af-129">**Einheit für Urlaub und Abwesenheit** auf Stunden oder Tage festlegen.</span><span class="sxs-lookup"><span data-stu-id="2e9af-129">Set **Unit for leave and absence** to either hours or days.</span></span> <span data-ttu-id="2e9af-130">Wenn Tage, können Sie **Aktivieren Sie die Halbtagesdefinition** auswählen, damit die Mitarbeiter in ihren Freistellungsanträgen entweder die erste oder die zweite Tageshälfte auswählen können.</span><span class="sxs-lookup"><span data-stu-id="2e9af-130">If days, you can select **Enable half day definition** to allow employees to choose either first or second half of day in their time-off requests.</span></span> 

    - <span data-ttu-id="2e9af-131">Wählen Sie **Datum des Inkrafttretens der Dienstmonate**, um festzulegen, wann die Abgrenzungssätze für Urlaubspläne mit monatelanger Dienstzeit wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="2e9af-131">Select **Months of service effective date** to set when the accrual rates take effect for leave plans using months of service.</span></span>

    - <span data-ttu-id="2e9af-132">Wählen Sie **Bilanzberechnung** aus, um Salden anzuzeigen, die ab heute oder ab dem Abgrenzungszeitraum angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2e9af-132">Select **Balance calculation** to display balances as of today or as of the accrual period.</span></span> <span data-ttu-id="2e9af-133">Wenn Sie **Saldo ab heute** in der Bilanz auswählen, wird die Summe aller Rückstellungen, Anpassungen und Anforderungen bis heute angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2e9af-133">If you select **Balance as of today**, the balance displays the total of all accruals, adjustments, and requests as of today.</span></span> <span data-ttu-id="2e9af-134">Wenn Sie **Saldo zum Abgrenzungszeitraum** auswählen, zeigt der Saldo die Summe aller Rückstellungen, Anpassungen und Anforderungen ab dem Abgrenzungszeitraum an, der durch die Häufigkeit im Urlaubsplan definiert ist.</span><span class="sxs-lookup"><span data-stu-id="2e9af-134">If you select **Balance as of accrual period**, the balance displays the total of all accruals, adjustments, and requests as of the accrual period defined by the frequency in the leave plan.</span></span> 

    - <span data-ttu-id="2e9af-135">Legen Sie die Startzeit für den Vortragsablaufuhrzeit-Batchauftrag fest.</span><span class="sxs-lookup"><span data-stu-id="2e9af-135">Set the start time for the carry forward expiration batch job.</span></span>  
    
    - <span data-ttu-id="2e9af-136">Wählen Sie **Ja** für **Mitarbeitern erlauben, Urlaub zu kaufen** und **Mitarbeitern erlauben, Urlaub zu verkaufen** aus.</span><span class="sxs-lookup"><span data-stu-id="2e9af-136">Select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span> <span data-ttu-id="2e9af-137">Wenn Sie für diese Optionen **Ja** auswählen, können Sie Richtlinien zum Kauf und Verkauf von Urlaub erstellen und es Mitarbeitern ermöglichen, Anforderungen zum Kaufen und Verkaufen von Urlaubsanforderungen einzureichen.</span><span class="sxs-lookup"><span data-stu-id="2e9af-137">If you select **Yes** for these options, you can create buy and sell leave policies and enable employees to submit buy and sell leave requests.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="2e9af-138">Konfigurieren Sie die Kalenderparameter</span><span class="sxs-lookup"><span data-stu-id="2e9af-138">Configure calendar parameters</span></span>

1. <span data-ttu-id="2e9af-139">Auf der Seite **Urlaub- und Abwesenheit** klicken Sie auf die Registerkarte **Links**.</span><span class="sxs-lookup"><span data-stu-id="2e9af-139">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="2e9af-140">Unter **Installieren**, wählen Sie **Urlaubs- und Abwesenheitsparameter**.</span><span class="sxs-lookup"><span data-stu-id="2e9af-140">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="2e9af-141">Auf der **Kalender** Registerkarte, überprüfen Sie die Einstellungen und ändern Sie sie nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="2e9af-141">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="2e9af-142">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="2e9af-142">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="2e9af-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e9af-143">See also</span></span>

- [<span data-ttu-id="2e9af-144">Urlaubs- und Abwesenheitsübersicht</span><span class="sxs-lookup"><span data-stu-id="2e9af-144">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]