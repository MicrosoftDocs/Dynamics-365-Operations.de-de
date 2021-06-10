---
title: Human Resources wird nicht in Microsoft Dynamics 365-Apps angezeigt
description: In diesem Artikel wird erklärt, was zu tun ist, wenn der Kunde die Microsoft Dynamics 365 Human Resources-App nicht unter den Microsoft Dynamics 365-Apps sieht.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 17a454cd32a08db105a13577c32368ad819bed1c
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053375"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a><span data-ttu-id="d0fe4-103">Human Resources wird nicht in Microsoft Dynamics 365-Apps angezeigt</span><span class="sxs-lookup"><span data-stu-id="d0fe4-103">Human Resources doesn't appear in Microsoft Dynamics 365 apps</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d0fe4-104">**Abgang**</span><span class="sxs-lookup"><span data-stu-id="d0fe4-104">**Issue**</span></span>

<span data-ttu-id="d0fe4-105">Der Kunde sieht Dynamics 365 Human Resources nicht bei den Microsoft Dynamics 365-Apps.</span><span class="sxs-lookup"><span data-stu-id="d0fe4-105">The customer doesn't see Dynamics 365 Human Resources among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="d0fe4-106">**Lösung**</span><span class="sxs-lookup"><span data-stu-id="d0fe4-106">**Resolution**</span></span>

<span data-ttu-id="d0fe4-107">Der Benutzer muss der Umgebungsersteller-Rolle für die Umgebung in Microsoft Power Apps hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d0fe4-107">The user must be added to the Environment Maker role for the environment in Microsoft Power Apps.</span></span>

1. <span data-ttu-id="d0fe4-108">Der Administratorbenutzer, der eine Power Apps Plan 2-Lizenz hat, muss das [Power Apps-Administratorportal](https://preview.admin.powerapps.com/) öffnen.</span><span class="sxs-lookup"><span data-stu-id="d0fe4-108">The admin user who has a Power Apps Plan 2 license must open the [Power Apps Admin portal](https://preview.admin.powerapps.com/).</span></span>

2. <span data-ttu-id="d0fe4-109">Wählen Sie **Umgebungen** aus, und wählen Sie die richtige Umgebung für Human Resources aus.</span><span class="sxs-lookup"><span data-stu-id="d0fe4-109">Select **Environments**, and select the correct environment for Human Resources.</span></span>

3. <span data-ttu-id="d0fe4-110">Wählen Sie auf der Registerkarte **Sicherheit** auf der Registerkarte **Umgebungsrollen** die Option **Umgebungsersteller** aus.</span><span class="sxs-lookup"><span data-stu-id="d0fe4-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Registerkarte „Umgebungsrollen”](media/environment-roles.png)

4. <span data-ttu-id="d0fe4-112">Fügen Sie auf der Registerkarte **Benutzer** den Benutzer oder Ihre Organisation hinzu.</span><span class="sxs-lookup"><span data-stu-id="d0fe4-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Registerkarte „Benutzer”](media/environment-maker.png)

5. <span data-ttu-id="d0fe4-114">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="d0fe4-114">Select **Save**.</span></span>

6. <span data-ttu-id="d0fe4-115">Der Benutzer muss sich jetzt bei [Microsoft Dynamics 365](https://home.dynamics.com/) anmelden.</span><span class="sxs-lookup"><span data-stu-id="d0fe4-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>

7. <span data-ttu-id="d0fe4-116">Wählen Sie **Synchronisieren** aus, m die Benutzer-Apps zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d0fe4-116">Select **Sync** to update the user apps.</span></span>

    ![Schaltfläche „Synchronisieren”](media/get-more.png)

    <span data-ttu-id="d0fe4-118">Nachdem die Synchronisierung abgeschlossen ist, wird Human Resources auf der Startseite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d0fe4-118">After synchronization is completed, Human Resources will appear on the home page.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]