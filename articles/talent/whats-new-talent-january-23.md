---
title: Neuerungen oder Änderungen in Dynamics 365 for Talent Core HR (23. Januar 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 for Talent Core HR entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 01/23/2019
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
ms.search.validFrom: 2019-01-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 4e492095d5269ec81c0c22145b7af356937c256b
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742515"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-january-23-2019"></a><span data-ttu-id="758df-103">Neuerungen oder Änderungen in Dynamics 365 for Talent Core HR (23. Januar 2019)</span><span class="sxs-lookup"><span data-stu-id="758df-103">What's new or changed in Dynamics 365 for Talent Core HR (January 23, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="758df-104">**Build 8.1.2121**</span><span class="sxs-lookup"><span data-stu-id="758df-104">**Build 8.1.2121**</span></span>

<span data-ttu-id="758df-105">In diesem Thema werden die Funktionen beschrieben, die in Core HR entweder neu oder geändert sind.</span><span class="sxs-lookup"><span data-stu-id="758df-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="758df-106">Änderungen</span><span class="sxs-lookup"><span data-stu-id="758df-106">Changes</span></span>

### <a name="import-of-employee-fixed-compensation-not-working-when-creating-new-fixed-compensation-records"></a><span data-ttu-id="758df-107">Import von nicht funktionierenden Mitarbeiter-Festvergütungen beim Anlegen neuer Festvergütungssätze</span><span class="sxs-lookup"><span data-stu-id="758df-107">Import of employee fixed compensation not working when creating new fixed compensation records</span></span>
<span data-ttu-id="758df-108">Es wurde eine Änderung an der festen Vergütungseinheit vorgenommen, um die Vergütungshöhe beim Import abzurufen.</span><span class="sxs-lookup"><span data-stu-id="758df-108">A change has been made to the employee fixed compensation entity to retrieve the compensation level upon import.</span></span> <span data-ttu-id="758df-109">Vor dieser Freigabe wurde eine Meldung angezeigt, die angab, dass der Level erforderlich war.</span><span class="sxs-lookup"><span data-stu-id="758df-109">Prior to this release, a message was displayed indicating that the level was required.</span></span>

### <a name="remove-the-minimum-balance-field-from-the-time-off-request-dialog-box"></a><span data-ttu-id="758df-110">Entfernen Sie das Feld Mindestguthaben aus dem Dialogfenster Urlaubsantrag.</span><span class="sxs-lookup"><span data-stu-id="758df-110">Remove the minimum balance field from the time off request dialog box</span></span>
<span data-ttu-id="758df-111">Das Feld **Mindestguthaben** wurde aus dem Dialogfenster **Urlaubsantrag** entfernt.</span><span class="sxs-lookup"><span data-stu-id="758df-111">The **Minimum balance** field has been removed from the **Time off request** dialog box.</span></span> <span data-ttu-id="758df-112">Diese Änderung betrifft alle Bereiche, in denen eine Freistellung beantragt werden kann.</span><span class="sxs-lookup"><span data-stu-id="758df-112">This change affects all areas where time off can be requested.</span></span>

### <a name="data-upgrade-for-compensation-levels-not-updating-in-all-scenarios"></a><span data-ttu-id="758df-113">Datenaktualisierung für Vergütungsstufen, die nicht in allen Szenarien aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="758df-113">Data upgrade for compensation levels not updating in all scenarios</span></span>
<span data-ttu-id="758df-114">Es wurde eine Änderung vorgenommen, um die Vergütungshöhe bei festen Vergütungsplänen zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="758df-114">A change has been made to update the compensation level on fixed compensation plans.</span></span> <span data-ttu-id="758df-115">Diese Änderung füllt die Vergütungsstufe bei festen Plänen für die dem Mitarbeiter zugeordnete Stelle.</span><span class="sxs-lookup"><span data-stu-id="758df-115">This change will populate the compensation level on fixed plans for the job assigned to the employee.</span></span>

### <a name="payroll-information-in-the-manage-changes-page-is-only-available-when-logged-in-as-system-administrator"></a><span data-ttu-id="758df-116">Abrechnungsinformationen auf der Seite Änderungen verwalten sind nur verfügbar, wenn Sie als Systemadministrator angemeldet sind</span><span class="sxs-lookup"><span data-stu-id="758df-116">Payroll information in the Manage changes page is only available when logged in as System Administrator</span></span>
<span data-ttu-id="758df-117">Diese Änderung ermöglicht Mitarbeitern mit der Rolle Sachbearbeiter Abrechnung den Zugriff auf die Abrechnungsinformationen auf der Seite **Änderungszeitachse > Änderungen verwalten** für die Planstelle.</span><span class="sxs-lookup"><span data-stu-id="758df-117">This change allows employees with the Payroll Administrator role access to the payroll information on the **Changes timeline > Manage changes** page for the position.</span></span>

### <a name="job-fields-default-to-positions"></a><span data-ttu-id="758df-118">Stellenfelder standardmäßig auf Planstellen voreingestellt</span><span class="sxs-lookup"><span data-stu-id="758df-118">Job fields default to positions</span></span>
<span data-ttu-id="758df-119">Wenn Sie die Stelle an einer Stelle ändern, werden die Stellenfelder standardmäßig auf die Stelle gesetzt.</span><span class="sxs-lookup"><span data-stu-id="758df-119">When changing the job on a position, job fields will default to the position.</span></span> <span data-ttu-id="758df-120">Es erscheint eine Warnmeldung, die die Möglichkeit bietet, die Standardwerte zu übernehmen oder die vorhandenen Werte für diese Felder beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="758df-120">An alert message will appear giving an option to accept the default values or keep the existing values for those fields.</span></span>

### <a name="probation-period-and-calendar-are-not-displayed-for-future-hired-employees"></a><span data-ttu-id="758df-121">Probezeit und Kalender werden für zukünftige eingestellte Mitarbeiter nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="758df-121">Probation period and calendar are not displayed for future hired employees.</span></span>
<span data-ttu-id="758df-122">Mit dieser Änderung wurden die Felder **Probezeit** und **Kalender** auf der Seite **Änderungen verwalten** hinzugefügt, um die Dateneingabe für zukünftige und ehemalige Mitarbeiter zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="758df-122">With this change, **Probation period** and **Calendar** fields have been added to the **Manage changes** page to allow for data entry for future and past employees.</span></span>

### <a name="platform-update-23"></a><span data-ttu-id="758df-123">Plattformupdate 23</span><span class="sxs-lookup"><span data-stu-id="758df-123">Platform update 23</span></span>
<span data-ttu-id="758df-124">Kleinere Bugfixes wurden im Rahmen des Plattform-Updates 23 aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="758df-124">Minor bug fixes have been included as part of Platform update 23.</span></span> <span data-ttu-id="758df-125">Weitere Informationen finden Sie unter [Was ist neu oder geändert in Dynamics 365 for Finance and Operations Plattform-Update 23 (Januar 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23).</span><span class="sxs-lookup"><span data-stu-id="758df-125">For more information, see [What's new or changed in Dynamics 365 for Finance and Operations platform update 23 (January 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23).</span></span> 
