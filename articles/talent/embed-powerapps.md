---
title: Einbetten von PowerApps-Apps in Core HR
description: "In diesem Thema wird erläutert, wie das Problem gelöst wird, bei dem das PowerApps-Menü aus dem Systemverwaltungsmodul verschwunden ist."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 197b553f0b202ee29ad42274e2c0e03446ec782c
ms.contentlocale: de-de
ms.lasthandoff: 12/04/2018

---

# <a name="embed-powerapps-apps-in-core-hr"></a><span data-ttu-id="ea447-103">Einbetten von PowerApps-Apps in Core HR</span><span class="sxs-lookup"><span data-stu-id="ea447-103">Embed PowerApps apps in Core HR</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ea447-104">**Abgang**</span><span class="sxs-lookup"><span data-stu-id="ea447-104">**Issue**</span></span>

<span data-ttu-id="ea447-105">Die Menüoption **PowerApps** ist aus dem Modul **Systemverwaltung** verschwunden.</span><span class="sxs-lookup"><span data-stu-id="ea447-105">The **PowerApps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="ea447-106">**Ursache**</span><span class="sxs-lookup"><span data-stu-id="ea447-106">**Cause**</span></span>

<span data-ttu-id="ea447-107">Das Design der Benutzeroberfläche (UI) ist verändert worden, und Microsoft PowerApps ist jetzt im standardmäßigen Personalisierungsmodell enthalten.</span><span class="sxs-lookup"><span data-stu-id="ea447-107">The user interface (UI) design has been changed, and Microsoft PowerApps is now included in the standard personalization model.</span></span>

<span data-ttu-id="ea447-108">**Auflösung**</span><span class="sxs-lookup"><span data-stu-id="ea447-108">**Resolution**</span></span>

<span data-ttu-id="ea447-109">Die Art und Weise, wie PowerApps-Apps jetzt eingebettet sind, hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="ea447-109">The way that PowerApps apps are embedded has been changed.</span></span> <span data-ttu-id="ea447-110">PowerApps-Apps werden jetzt durch das Personalisierungsmodell hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ea447-110">PowerApps apps are now added through the personalization model.</span></span> <span data-ttu-id="ea447-111">Sie können PowerApps-Apps fast allen Seiten in Microsoft Dynamics 365 for Talent hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ea447-111">You can add PowerApps apps to almost all pages in Microsoft Dynamics 365 for Talent.</span></span>

<span data-ttu-id="ea447-112">Ausführliche Informationen dazu, wie PowerApps-Apps in Talent eingebettet werden, finden Sie unter [PowerApps-Apps einbetten](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="ea447-112">For information about how to embed PowerApps apps in Talent, see [Embed PowerApps apps](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="ea447-113">Jeder PowerApps-Kunde, der Apps vor der Änderung eingebettet hat, sollte auf das neue Modell aktualisiert worden sein.</span><span class="sxs-lookup"><span data-stu-id="ea447-113">Any PowerApps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="ea447-114">Die Schaltfläche **PowerApps** befindet sich in der oberen rechten Ecke beinahe jeder Seite in Talent.</span><span class="sxs-lookup"><span data-stu-id="ea447-114">The **PowerApps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="ea447-115">Sie können diese Schaltfläche verwenden, um eine PowerApps-App einzufügen.</span><span class="sxs-lookup"><span data-stu-id="ea447-115">You can use this button to insert a PowerApps app.</span></span>

<span data-ttu-id="ea447-116">Hier ist ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="ea447-116">Here is an example.</span></span>

1. <span data-ttu-id="ea447-117">Wechseln Sie zu **Personalverwaltung \> Links \> Arbeitskräfte \> Mitarbeiter**.</span><span class="sxs-lookup"><span data-stu-id="ea447-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="ea447-118">Wählen Sie die Schaltfläche **PowerApps** aus, und wählen Sie dann **Eine PowerApp einfügen** aus.</span><span class="sxs-lookup"><span data-stu-id="ea447-118">Select the **PowerApps** button, and then select **Insert a PowerApp**.</span></span>

    ![PowerApps-Schaltfläche](media/png.png)

3. <span data-ttu-id="ea447-120">Füllen Sie die Felder im Dialogfeld **Eine PowerApp einfügen** aus.</span><span class="sxs-lookup"><span data-stu-id="ea447-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![Ein PowerApp-Dialogfeld einfügen](media/insert-powerapp.png)

<span data-ttu-id="ea447-122">Gehen Sie alternativ folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="ea447-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="ea447-123">Wählen Sie im Aktivitätsbereich der Seite in der Registerkarte **Optionen** in der Gruppe **Personalisieren** die Option **Dieses Formular personalisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="ea447-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![Gruppe „Personalisieren” in der Registerkarte „Optionen”](media/options.png)

    <span data-ttu-id="ea447-125">Die Personalisierungssymbolleiste wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ea447-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="ea447-126">Wählen Sie auf der Symbolleiste die Option **Einfügen \> PowerApp** aus.</span><span class="sxs-lookup"><span data-stu-id="ea447-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![Eine PowerApps-App mithilfe der Personalisierungssymbolleiste einfügen](media/powerapp-bar.png)
