---
title: Einbetten von PowerApps-Apps in Dynamics 365 – Core HR
description: In diesem Thema wird erläutert, wie das Problem des aus dem Systemverwaltungsmodul verschwundenen PowerApps-Menüs gelöst wird.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b510c10ebfcf4939eb2e1297972d27aa1812ae5a
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551002"
---
# <a name="embed-powerapps-apps-in-dynamics-365---core-hr"></a><span data-ttu-id="ed33a-103">Einbetten von PowerApps-Apps in Dynamics 365 – Core HR</span><span class="sxs-lookup"><span data-stu-id="ed33a-103">Embed PowerApps apps in Dynamics 365 - Core HR</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ed33a-104">**Abgang**</span><span class="sxs-lookup"><span data-stu-id="ed33a-104">**Issue**</span></span>

<span data-ttu-id="ed33a-105">Die Menüoption **PowerApps** ist aus dem Modul **Systemverwaltung** verschwunden.</span><span class="sxs-lookup"><span data-stu-id="ed33a-105">The **PowerApps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="ed33a-106">**Ursache**</span><span class="sxs-lookup"><span data-stu-id="ed33a-106">**Cause**</span></span>

<span data-ttu-id="ed33a-107">Das Design der Benutzeroberfläche (UI) wurde verändert, und Microsoft PowerApps ist jetzt im standardmäßigen Personalisierungsmodell enthalten.</span><span class="sxs-lookup"><span data-stu-id="ed33a-107">The user interface (UI) design has been changed, and Microsoft PowerApps is now included in the standard personalization model.</span></span>

<span data-ttu-id="ed33a-108">**Lösung**</span><span class="sxs-lookup"><span data-stu-id="ed33a-108">**Resolution**</span></span>

<span data-ttu-id="ed33a-109">Die Art und Weise, wie PowerApps jetzt eingebettet sind, hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="ed33a-109">The way that PowerApps apps are embedded has been changed.</span></span> <span data-ttu-id="ed33a-110">PowerApps werden jetzt durch das Personalisierungsmodell hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ed33a-110">PowerApps apps are now added through the personalization model.</span></span> <span data-ttu-id="ed33a-111">Sie können PowerApps fast allen Seiten in Microsoft Dynamics 365 Talent hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ed33a-111">You can add PowerApps apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="ed33a-112">Ausführliche Informationen zum Einbetten von PowerApps in Talent finden Sie unter [Einbetten von PowerApps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps)</span><span class="sxs-lookup"><span data-stu-id="ed33a-112">For information about how to embed PowerApps apps in Talent, see [Embed PowerApps apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="ed33a-113">Jeder PowerApps-Kunde, der Apps vor der Änderung eingebettet hat, sollte auf das neue Modell aktualisiert worden sein.</span><span class="sxs-lookup"><span data-stu-id="ed33a-113">Any PowerApps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="ed33a-114">Die Schaltfläche **PowerApps** befindet sich in der oberen rechten Ecke beinahe jeder Seite in Talent.</span><span class="sxs-lookup"><span data-stu-id="ed33a-114">The **PowerApps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="ed33a-115">Sie können diese Schaltfläche verwenden, um eine PowerApps-App einzufügen.</span><span class="sxs-lookup"><span data-stu-id="ed33a-115">You can use this button to insert a PowerApps app.</span></span>

<span data-ttu-id="ed33a-116">Hier ist ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="ed33a-116">Here is an example.</span></span>

1. <span data-ttu-id="ed33a-117">Wechseln Sie zu **Personalverwaltung \> Links \> Arbeitskräfte \> Mitarbeiter**.</span><span class="sxs-lookup"><span data-stu-id="ed33a-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="ed33a-118">Wählen Sie die Schaltfläche **PowerApps** und dann **PowerApp einfügen** aus.</span><span class="sxs-lookup"><span data-stu-id="ed33a-118">Select the **PowerApps** button, and then select **Insert a PowerApp**.</span></span>

    ![PowerApps-Schaltfläche](media/png.png)

3. <span data-ttu-id="ed33a-120">Füllen Sie die Felder im Dialogfeld **Eine PowerApp einfügen** aus.</span><span class="sxs-lookup"><span data-stu-id="ed33a-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![Ein PowerApp-Dialogfeld einfügen](media/insert-powerapp.png)

<span data-ttu-id="ed33a-122">Gehen Sie alternativ folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="ed33a-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="ed33a-123">Wählen Sie im Aktivitätsbereich der Seite in der Registerkarte **Optionen** in der Gruppe **Personalisieren** die Option **Dieses Formular personalisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="ed33a-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![Gruppe „Personalisieren” in der Registerkarte „Optionen”](media/options.png)

    <span data-ttu-id="ed33a-125">Die Personalisierungssymbolleiste wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ed33a-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="ed33a-126">Wählen Sie auf der Symbolleiste die Option **Einfügen \> PowerApp** aus.</span><span class="sxs-lookup"><span data-stu-id="ed33a-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![Einfügen einer PowerApps-App mithilfe der Personalisierungssymbolleiste](media/powerapp-bar.png)
