---
title: Talent wird nicht in den Microsoft Dynamics 365-Anwendungen angezeigt (CDS1.0)
description: In diesem Thema wird erklärt, was zu tun ist, wenn der Kunde die Microsoft Dynamics 365 for Talent-App nicht unter den Microsoft Dynamics 365-Apps sieht.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 32ae0ab807e953bd811a557e6878b9bee79d293c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "304559"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-cds10"></a><span data-ttu-id="19ef3-103">Talent wird nicht in den Microsoft Dynamics 365-Anwendungen angezeigt (CDS1.0)</span><span class="sxs-lookup"><span data-stu-id="19ef3-103">Talent doesn't appear among the Microsoft Dynamics 365 apps (CDS1.0)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="19ef3-104">**Abgang**</span><span class="sxs-lookup"><span data-stu-id="19ef3-104">**Issue**</span></span>

<span data-ttu-id="19ef3-105">Der Debitor wird nicht der Zeit-App Microsoft unter Dynamics 365 for Talent Apps Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="19ef3-105">The customer doesn't see the Microsoft Dynamics 365 for Talent app among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="19ef3-106">**Auflösung**</span><span class="sxs-lookup"><span data-stu-id="19ef3-106">**Resolution**</span></span>

<span data-ttu-id="19ef3-107">Der Benutzer muss der Umgebungsersteller-Rolle für die Umgebung in Microsoft PowerApps hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="19ef3-107">The user must be added to the Environment Maker role for the environment in Microsoft PowerApps.</span></span>

1. <span data-ttu-id="19ef3-108">Der Administratorbenutzer, der eine PowerApps Plan 2-Lizenz hat, muss das [PowerApps-Administratorportal](https://preview.admin.powerapps.com/) öffnen.</span><span class="sxs-lookup"><span data-stu-id="19ef3-108">The admin user who has a PowerApps Plan 2 license must open the [PowerApps Admin portal](https://preview.admin.powerapps.com/).</span></span>
2. <span data-ttu-id="19ef3-109">Wählen Sie **Umgebungen** aus, und wählen Sie die richtige Umgebung für Talent aus.</span><span class="sxs-lookup"><span data-stu-id="19ef3-109">Select **Environments**, and select the correct environment for Talent.</span></span>
3. <span data-ttu-id="19ef3-110">Wählen Sie auf der Registerkarte **Sicherheit** auf der Registerkarte **Umgebungsrollen** die Option **Umgebungsersteller** aus.</span><span class="sxs-lookup"><span data-stu-id="19ef3-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Registerkarte „Umgebungsrollen”](media/environment-roles.png)

4. <span data-ttu-id="19ef3-112">Fügen Sie auf der Registerkarte **Benutzer** den Benutzer oder Ihre Organisation hinzu.</span><span class="sxs-lookup"><span data-stu-id="19ef3-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Registerkarte „Benutzer”](media/environment-maker.png)

5. <span data-ttu-id="19ef3-114">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="19ef3-114">Select **Save**.</span></span>
6. <span data-ttu-id="19ef3-115">Der Benutzer muss sich jetzt bei [Microsoft Dynamics 365](https://home.dynamics.com/) anmelden.</span><span class="sxs-lookup"><span data-stu-id="19ef3-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>
7. <span data-ttu-id="19ef3-116">Wählen Sie **Synchronisieren** aus, m die Benutzer-Apps zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="19ef3-116">Select **Sync** to update the user apps.</span></span>

    ![Schaltfläche „Synchronisieren”](media/get-more.png)

    <span data-ttu-id="19ef3-118">Nachdem die Synchronisierung abgeschlossen ist, wird Talent auf der Startseite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="19ef3-118">After synchronization is completed, Talent will appear on the home page.</span></span>
