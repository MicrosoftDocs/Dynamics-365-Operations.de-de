---
title: Human Resources wird nicht in Microsoft Dynamics 365-Apps angezeigt
description: In diesem Artikel wird erklärt, was zu tun ist, wenn der Kunde die Microsoft Dynamics 365 Human Resources-App nicht unter den Microsoft Dynamics 365-Apps sieht.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cbf47b4673e1c97965bba7728e5669b7639c4d56
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418654"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a><span data-ttu-id="4b278-103">Human Resources wird nicht in Microsoft Dynamics 365-Apps angezeigt</span><span class="sxs-lookup"><span data-stu-id="4b278-103">Human Resources doesn't appear in Microsoft Dynamics 365 apps</span></span>

<span data-ttu-id="4b278-104">**Abgang**</span><span class="sxs-lookup"><span data-stu-id="4b278-104">**Issue**</span></span>

<span data-ttu-id="4b278-105">Der Kunde sieht Dynamics 365 Human Resources nicht bei den Microsoft Dynamics 365-Apps.</span><span class="sxs-lookup"><span data-stu-id="4b278-105">The customer doesn't see Dynamics 365 Human Resources among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="4b278-106">**Lösung**</span><span class="sxs-lookup"><span data-stu-id="4b278-106">**Resolution**</span></span>

<span data-ttu-id="4b278-107">Der Benutzer muss der Umgebungsersteller-Rolle für die Umgebung in Microsoft Power Apps hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="4b278-107">The user must be added to the Environment Maker role for the environment in Microsoft Power Apps.</span></span>

1. <span data-ttu-id="4b278-108">Der Administratorbenutzer, der eine Power Apps Plan 2-Lizenz hat, muss das [Power Apps-Administratorportal](https://preview.admin.powerapps.com/) öffnen.</span><span class="sxs-lookup"><span data-stu-id="4b278-108">The admin user who has a Power Apps Plan 2 license must open the [Power Apps Admin portal](https://preview.admin.powerapps.com/).</span></span>

2. <span data-ttu-id="4b278-109">Wählen Sie **Umgebungen** aus, und wählen Sie die richtige Umgebung für Human Resources aus.</span><span class="sxs-lookup"><span data-stu-id="4b278-109">Select **Environments**, and select the correct environment for Human Resources.</span></span>

3. <span data-ttu-id="4b278-110">Wählen Sie auf der Registerkarte **Sicherheit** auf der Registerkarte **Umgebungsrollen** die Option **Umgebungsersteller** aus.</span><span class="sxs-lookup"><span data-stu-id="4b278-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Registerkarte „Umgebungsrollen”](media/environment-roles.png)

4. <span data-ttu-id="4b278-112">Fügen Sie auf der Registerkarte **Benutzer** den Benutzer oder Ihre Organisation hinzu.</span><span class="sxs-lookup"><span data-stu-id="4b278-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Registerkarte „Benutzer”](media/environment-maker.png)

5. <span data-ttu-id="4b278-114">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="4b278-114">Select **Save**.</span></span>

6. <span data-ttu-id="4b278-115">Der Benutzer muss sich jetzt bei [Microsoft Dynamics 365](https://home.dynamics.com/) anmelden.</span><span class="sxs-lookup"><span data-stu-id="4b278-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>

7. <span data-ttu-id="4b278-116">Wählen Sie **Synchronisieren** aus, m die Benutzer-Apps zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="4b278-116">Select **Sync** to update the user apps.</span></span>

    ![Schaltfläche „Synchronisieren”](media/get-more.png)

    <span data-ttu-id="4b278-118">Nachdem die Synchronisierung abgeschlossen ist, wird Human Resources auf der Startseite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4b278-118">After synchronization is completed, Human Resources will appear on the home page.</span></span>
