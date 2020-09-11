---
title: Beurlaubungs- und Abwesenheitsparameter konfigurieren
description: Definieren Sie Personalparameter für Urlaub und Abwesenheit in Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2020
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
ms.openlocfilehash: 196c3901b5bc19f73b882bac7d3361e5bcc37e07
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712375"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="d70be-103">Beurlaubungs- und Abwesenheitsparameter konfigurieren</span><span class="sxs-lookup"><span data-stu-id="d70be-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="d70be-104">Bevor Sie Urlaubs- und Abwesenheitspläne einrichten in Dynamics 365 Human Resourcesi st es eine gute Idee, die Einstellungen für alle zugehörigen Personalparameter zu überprüfen, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="d70be-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="d70be-105">Nummernfolge für Urlaubsanträge</span><span class="sxs-lookup"><span data-stu-id="d70be-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="d70be-106">Family and Medical Leave Act (FMLA) Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d70be-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="d70be-107">Self-Service-Einstellungen für Mitarbeiter für Urlaubs- und Abwesenheitsanträge</span><span class="sxs-lookup"><span data-stu-id="d70be-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="d70be-108">Urlaubs- und Abwesenheitsparameter</span><span class="sxs-lookup"><span data-stu-id="d70be-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="d70be-109">Personalverwaltungsparameter anzeigen und ändern</span><span class="sxs-lookup"><span data-stu-id="d70be-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="d70be-110">Auf der Seite **Urlaub- und Abwesenheit** klicken Sie auf die Registerkarte **Links**.</span><span class="sxs-lookup"><span data-stu-id="d70be-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="d70be-111">Unter **Einrichtung** wählen Sie **Personalverwaltungsparameter einrichten**.</span><span class="sxs-lookup"><span data-stu-id="d70be-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="d70be-112">Auf der **Zahlenfolgen** Registerkarte, überprüfen Sie die **Zahlenfolgecode** für **Urlaubsanfragen-ID** und ändern Sie nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="d70be-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="d70be-113">Diese Einstellung legt die Reihenfolge fest, in der IDs zum automatischen Zuweisen von IDs für Urlaubsanforderungen.</span><span class="sxs-lookup"><span data-stu-id="d70be-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="d70be-114">Auf der **FMLA** Registerkarte, überprüfen Sie die FMLA-Einstellungen und ändern Sie sie nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="d70be-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="d70be-115">Auf der Registerkarte **Mitarbeiter-Selbstservice** geben Sie an, ob Manager Urlaubs- und Abwesenheitsanträge für ihre Mitarbeiter eingeben können.</span><span class="sxs-lookup"><span data-stu-id="d70be-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

7. <span data-ttu-id="d70be-116">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="d70be-116">Select **Save**.</span></span>

## <a name="view-and-change-leave-and-absence-parameters"></a><span data-ttu-id="d70be-117">Urlaub- und Abwesenheitsparameter anzeigen und ändern</span><span class="sxs-lookup"><span data-stu-id="d70be-117">View and change leave and absence parameters</span></span>

1. <span data-ttu-id="d70be-118">Auf der Seite **Urlaub- und Abwesenheit** klicken Sie auf die Registerkarte **Links**.</span><span class="sxs-lookup"><span data-stu-id="d70be-118">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="d70be-119">Unter **Installieren**, wählen Sie **Urlaubs- und Abwesenheitsparameter**.</span><span class="sxs-lookup"><span data-stu-id="d70be-119">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="d70be-120">Legen Sie auf der Registerkarte **Allgemein** die folgenden Parameter fest:</span><span class="sxs-lookup"><span data-stu-id="d70be-120">On the **General** tab, set the following parameters:</span></span>
 
    - <span data-ttu-id="d70be-121">**Einheit für Urlaub und Abwesenheit** auf Stunden oder Tage festlegen.</span><span class="sxs-lookup"><span data-stu-id="d70be-121">Set **Unit for leave and absence** to either hours or days.</span></span> <span data-ttu-id="d70be-122">Wenn Tage, können Sie **Aktivieren Sie die Halbtagesdefinition** auswählen, damit die Mitarbeiter in ihren Freistellungsanträgen entweder die erste oder die zweite Tageshälfte auswählen können.</span><span class="sxs-lookup"><span data-stu-id="d70be-122">If days, you can select **Enable half day definition** to allow employees to choose either first or second half of day in their time-off requests.</span></span> 

    - <span data-ttu-id="d70be-123">Wählen Sie **Datum des Inkrafttretens der Dienstmonate**, um festzulegen, wann die Abgrenzungssätze für Urlaubspläne mit monatelanger Dienstzeit wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="d70be-123">Select **Months of service effective date** to set when the accrual rates take effect for leave plans using months of service.</span></span>

    - <span data-ttu-id="d70be-124">Wählen Sie **Bilanzberechnung** aus, um Salden anzuzeigen, die ab heute oder ab dem Abgrenzungszeitraum angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d70be-124">Select **Balance calculation** to display balances as of today or as of the accrual period.</span></span> <span data-ttu-id="d70be-125">Wenn Sie **Saldo ab heute** in der Bilanz auswählen, wird die Summe aller Rückstellungen, Anpassungen und Anforderungen bis heute angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d70be-125">If you select **Balance as of today**, the balance displays the total of all accruals, adjustments, and requests as of today.</span></span> <span data-ttu-id="d70be-126">Wenn Sie **Saldo zum Abgrenzungszeitraum** auswählen, zeigt der Saldo die Summe aller Rückstellungen, Anpassungen und Anforderungen ab dem Abgrenzungszeitraum an, der durch die Häufigkeit im Urlaubsplan definiert ist.</span><span class="sxs-lookup"><span data-stu-id="d70be-126">If you select **Balance as of accrual period**, the balance displays the total of all accruals, adjustments, and requests as of the accrual period defined by the frequency in the leave plan.</span></span> 

    - <span data-ttu-id="d70be-127">Legen Sie die Startzeit für den Vortragsablaufuhrzeit-Batchauftrag fest.</span><span class="sxs-lookup"><span data-stu-id="d70be-127">Set the start time for the carry forward expiration batch job.</span></span>  
    
    - <span data-ttu-id="d70be-128">Wählen Sie **Ja** für **Mitarbeitern erlauben, Urlaub zu kaufen** und **Mitarbeitern erlauben, Urlaub zu verkaufen** aus.</span><span class="sxs-lookup"><span data-stu-id="d70be-128">Select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span> <span data-ttu-id="d70be-129">Wenn Sie für diese Optionen **Ja** auswählen, können Sie Richtlinien zum Kauf und Verkauf von Urlaub erstellen und es Mitarbeitern ermöglichen, Anforderungen zum Kaufen und Verkaufen von Urlaubsanforderungen einzureichen.</span><span class="sxs-lookup"><span data-stu-id="d70be-129">If you select **Yes** for these options, you can create buy and sell leave policies and enable employees to submit buy and sell leave requests.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="d70be-130">Konfigurieren Sie die Kalenderparameter</span><span class="sxs-lookup"><span data-stu-id="d70be-130">Configure calendar parameters</span></span>

1. <span data-ttu-id="d70be-131">Auf der Seite **Urlaub- und Abwesenheit** klicken Sie auf die Registerkarte **Links**.</span><span class="sxs-lookup"><span data-stu-id="d70be-131">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="d70be-132">Unter **Installieren**, wählen Sie **Urlaubs- und Abwesenheitsparameter**.</span><span class="sxs-lookup"><span data-stu-id="d70be-132">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="d70be-133">Auf der **Kalender** Registerkarte, überprüfen Sie die Einstellungen und ändern Sie sie nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="d70be-133">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="d70be-134">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="d70be-134">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="d70be-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d70be-135">See also</span></span>

- [<span data-ttu-id="d70be-136">Urlaubs- und Abwesenheitsübersicht</span><span class="sxs-lookup"><span data-stu-id="d70be-136">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
