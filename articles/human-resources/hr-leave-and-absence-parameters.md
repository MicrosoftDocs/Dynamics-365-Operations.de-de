---
title: Beurlaubungs- und Abwesenheitsparameter konfigurieren
description: Definieren Sie Personalparameter für Urlaub und Abwesenheit in Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2acb8502ebcab122a0a1ff21e9f5e23931026327
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009129"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="dd6d6-103">Beurlaubungs- und Abwesenheitsparameter konfigurieren</span><span class="sxs-lookup"><span data-stu-id="dd6d6-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="dd6d6-104">Bevor Sie Urlaubs- und Abwesenheitspläne einrichten in Dynamics 365 Human Resourcesi st es eine gute Idee, die Einstellungen für alle zugehörigen Personalparameter zu überprüfen, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="dd6d6-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="dd6d6-105">Nummernfolge für Urlaubsanträge</span><span class="sxs-lookup"><span data-stu-id="dd6d6-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="dd6d6-106">Family and Medical Leave Act (FMLA) Einstellungen</span><span class="sxs-lookup"><span data-stu-id="dd6d6-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="dd6d6-107">Self-Service-Einstellungen für Mitarbeiter für Urlaubs- und Abwesenheitsanträge</span><span class="sxs-lookup"><span data-stu-id="dd6d6-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="dd6d6-108">Urlaubs- und Abwesenheitsparameter</span><span class="sxs-lookup"><span data-stu-id="dd6d6-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="dd6d6-109">Personalverwaltungsparameter anzeigen und ändern</span><span class="sxs-lookup"><span data-stu-id="dd6d6-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="dd6d6-110">Auf der Seite **Urlaub- und Abwesenheit** klicken Sie auf die Registerkarte **Links**.</span><span class="sxs-lookup"><span data-stu-id="dd6d6-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="dd6d6-111">Unter **Einrichtung** wählen Sie **Personalverwaltungsparameter einrichten**.</span><span class="sxs-lookup"><span data-stu-id="dd6d6-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="dd6d6-112">Auf der **Zahlenfolgen** Registerkarte, überprüfen Sie die **Zahlenfolgecode** für **Urlaubsanfragen-ID** und ändern Sie nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="dd6d6-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="dd6d6-113">Diese Einstellung legt die Reihenfolge fest, in der IDs zum automatischen Zuweisen von IDs für Urlaubsanforderungen.</span><span class="sxs-lookup"><span data-stu-id="dd6d6-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="dd6d6-114">Auf der **FMLA** Registerkarte, überprüfen Sie die FMLA-Einstellungen und ändern Sie sie nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="dd6d6-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="dd6d6-115">Auf der Registerkarte **Mitarbeiter-Selbstservice** geben Sie an, ob Manager Urlaubs- und Abwesenheitsanträge für ihre Mitarbeiter eingeben können.</span><span class="sxs-lookup"><span data-stu-id="dd6d6-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

6. <span data-ttu-id="dd6d6-116">Auf der **Urlaub und Abwesenheit** Registerkarte, überprüfen Sie die Einstellungen und ändern Sie sie nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="dd6d6-116">On the **Leave and absence** tab, verify the settings and change as necessary.</span></span>

7. <span data-ttu-id="dd6d6-117">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="dd6d6-117">Select **Save**.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="dd6d6-118">Konfigurieren Sie die Kalenderparameter</span><span class="sxs-lookup"><span data-stu-id="dd6d6-118">Configure calendar parameters</span></span>

<span data-ttu-id="dd6d6-119">Wenn Sie die Vorschau für Urlaubs- und Abwesenheitskalender aktiviert haben, müssen Sie zusätzliche Parameter konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="dd6d6-119">If you have enabled the Leave and absence calendar preview feature, you need to configure additional parameters.</span></span> 

[!include [banner](includes/preview-feature-leave-absence.md)]

> [!NOTE]
> <span data-ttu-id="dd6d6-120">Für den Vorschau-Release am 3. Februar 2020 sind nur **Ausstehende Urlaubsanträge** aktiviert.</span><span class="sxs-lookup"><span data-stu-id="dd6d6-120">For the preview release on February 3, 2020, only **Pending leave requests** are enabled.</span></span>

1. <span data-ttu-id="dd6d6-121">Auf der Seite **Urlaub- und Abwesenheit** klicken Sie auf die Registerkarte **Links**.</span><span class="sxs-lookup"><span data-stu-id="dd6d6-121">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="dd6d6-122">Unter **Einrichtung** wählen Sie **Personalverwaltungsparameter einrichten**.</span><span class="sxs-lookup"><span data-stu-id="dd6d6-122">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="dd6d6-123">Auf der **Kalender** Registerkarte, überprüfen Sie die Einstellungen und ändern Sie sie nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="dd6d6-123">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="dd6d6-124">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="dd6d6-124">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="dd6d6-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd6d6-125">See also</span></span>

- [<span data-ttu-id="dd6d6-126">Urlaubs- und Abwesenheitsübersicht</span><span class="sxs-lookup"><span data-stu-id="dd6d6-126">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
