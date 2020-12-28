---
title: Attract-Benutzer können sich nicht mit dem Karriereportal auf Stellen bewerben
description: In diesem Thema wird erläutert, wie Sie ein Problem behandeln können, wenn sich Attract-Benutzer nicht über das Karriereportal auf Stellen bewerben können.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: e1d72bef6d8bbe15e27326f66341915ba44a09b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461247"
---
# <a name="attract-users-cant-apply-for-jobs-from-career-portal"></a><span data-ttu-id="e1893-103">Attract-Benutzer können sich nicht mit dem Karriereportal auf Stellen bewerben</span><span class="sxs-lookup"><span data-stu-id="e1893-103">Attract users can't apply for jobs from career portal</span></span>

[!include [banner](includes/banner.md)]

## <a name="issue"></a><span data-ttu-id="e1893-104">Abgang</span><span class="sxs-lookup"><span data-stu-id="e1893-104">Issue</span></span>

<span data-ttu-id="e1893-105">Attract-Benutzer können sich nicht mit dem Karriereportal auf Stellen bewerben.</span><span class="sxs-lookup"><span data-stu-id="e1893-105">Attract users can't apply for jobs from the career portal.</span></span> <span data-ttu-id="e1893-106">Wenn sie versuchen, sich auf eine Stelle zu bewerben, die in Dynamics 365 Talent: Attract erstellt wurde, lädt der Browser die Seite kontinuierlich und schließt die Aktivität nicht ab.</span><span class="sxs-lookup"><span data-stu-id="e1893-106">When they try to apply for a job that was created in Dynamics 365 Talent: Attract, the browser loads the page continuously and doesn't complete the action.</span></span>

## <a name="cause"></a><span data-ttu-id="e1893-107">Ursache</span><span class="sxs-lookup"><span data-stu-id="e1893-107">Cause</span></span>

<span data-ttu-id="e1893-108">Dieses Problem tritt auf, wenn das Talent Relationship Team nicht über die Talent-Benutzerrolle verfügt.</span><span class="sxs-lookup"><span data-stu-id="e1893-108">This problem occurs when the Talent Relationship Team doesn't have the Talent user role.</span></span>

## <a name="resolution"></a><span data-ttu-id="e1893-109">Lösung</span><span class="sxs-lookup"><span data-stu-id="e1893-109">Resolution</span></span>

<span data-ttu-id="e1893-110">Weisen Sie dem Talent Relationship Team die Talent-Benutzerrolle zu.</span><span class="sxs-lookup"><span data-stu-id="e1893-110">Assign the Talent user role to the Talent Relationship Team.</span></span>

1. <span data-ttu-id="e1893-111">Melden Sie sich im [Power Platform Admin Center](https://admin.powerplatform.microsoft.com) mit einem der folgenden Administratoranmeldeinformationen an:</span><span class="sxs-lookup"><span data-stu-id="e1893-111">Sign in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com) with any of the following admin credentials:</span></span>

   - <span data-ttu-id="e1893-112">Dynamics 365-Administrator</span><span class="sxs-lookup"><span data-stu-id="e1893-112">Dynamics 365 admin</span></span>
   - <span data-ttu-id="e1893-113">Globaler Administrator</span><span class="sxs-lookup"><span data-stu-id="e1893-113">Global admin</span></span>
   - <span data-ttu-id="e1893-114">Power Platform-Administrator</span><span class="sxs-lookup"><span data-stu-id="e1893-114">Power Platform admin</span></span>

2. <span data-ttu-id="e1893-115">Wählen Sie im Navigationsbereich **Umgebungen** und dann die Umgebung aus, in der die Talent-Benutzerrolle dem Talent Relationship Team zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e1893-115">In the navigation pane, select **Environments**, and then select the environment in which to assign the Talent user role to the Talent Relationship Team.</span></span>

   ![Umgebung auswählen](./media/attract-troubleshoot-career-portal-select-environment.png)

3. <span data-ttu-id="e1893-117">Wählen Sie im Bereich **Umgebungen** die **Umgebungs-URL** aus und melden Sie sich beim Admininistratorportal der Umgebung an (z. B. https:<orgname>.crm.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="e1893-117">In the **Environments** pane, select the **Environment URL** and sign in to the environment's admin portal (for example, https:<orgname>.crm.dynamics.com).</span></span>

4. <span data-ttu-id="e1893-118">Wählen Sie **Einstellungen**, **System** und dann **Sicherheit**.</span><span class="sxs-lookup"><span data-stu-id="e1893-118">Select **Settings**, select **System**, and then select **Security**.</span></span>

   ![Zu Sicherheit navigieren](./media/attract-troubleshoot-career-portal-security.png)

5. <span data-ttu-id="e1893-120">Wählen Sie **Teams** aus.</span><span class="sxs-lookup"><span data-stu-id="e1893-120">Select **Teams**.</span></span>

   ![Teams auswählen](./media/attract-troubleshoot-career-portal-security-teams.png)

6. <span data-ttu-id="e1893-122">Suchen Sie im Suchfeld nach dem **Talent Relationship Team** und wählen Sie dann aus den Suchergebnissen das Team aus.</span><span class="sxs-lookup"><span data-stu-id="e1893-122">Search for **Talent Relationship Team** in the search box, and then select the team from the search results.</span></span>

7. <span data-ttu-id="e1893-123">Wählen Sie im Menüband **ROLLEN VERWALTEN** aus.</span><span class="sxs-lookup"><span data-stu-id="e1893-123">Select **MANAGE ROLES** from the ribbon.</span></span>

8. <span data-ttu-id="e1893-124">Wählen Sie im Dialogfeld **Teamrollen verwalten** und dann **Talent-Benutzer** aus der Liste der verfügbaren Rollen aus. Übernehmen Sie die Rolle dann mit **OK**.</span><span class="sxs-lookup"><span data-stu-id="e1893-124">In the **Manage Team Roles** dialog, select **Talent user** from the list of available roles, and then select **OK** to apply the role.</span></span>

   ![Rolle übernehmen](./media/attract-troubleshoot-career-portal-apply-role.png)

9. <span data-ttu-id="e1893-126">Testen Sie Ihre Änderungen:</span><span class="sxs-lookup"><span data-stu-id="e1893-126">Test your changes:</span></span>

   1. <span data-ttu-id="e1893-127">Melden Sie sich über ein neues Browserfenster im Karriereportal an.</span><span class="sxs-lookup"><span data-stu-id="e1893-127">Sign in to the career portal from a new browser window.</span></span>
   2. <span data-ttu-id="e1893-128">Bewerben Sie sich über das Karriereportal auf die Stelle.</span><span class="sxs-lookup"><span data-stu-id="e1893-128">Apply for the job from the career portal.</span></span> 