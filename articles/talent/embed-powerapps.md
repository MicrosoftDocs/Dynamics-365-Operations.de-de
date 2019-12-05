---
title: Einbetten von Power Apps-Apps in Dynamics 365 – Core HR
description: In diesem Thema wird erläutert, wie das Problem des aus dem Systemverwaltungsmodul verschwundenen Microsoft Power Apps-Menüs gelöst wird.
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
ms.openlocfilehash: 6d1b7f1dd71e6bcbf10c4d91fe33e9494b041a2c
ms.sourcegitcommit: ae0efac749ab34d423fac44d00a597801c143fbb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/22/2019
ms.locfileid: "2830208"
---
# <a name="embed-power-apps-apps-in-dynamics-365---core-hr"></a><span data-ttu-id="6b3f6-103">Einbetten von Power Apps-Apps in Dynamics 365 – Core HR</span><span class="sxs-lookup"><span data-stu-id="6b3f6-103">Embed Power Apps apps in Dynamics 365 - Core HR</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6b3f6-104">**Abgang**</span><span class="sxs-lookup"><span data-stu-id="6b3f6-104">**Issue**</span></span>

<span data-ttu-id="6b3f6-105">Die Menüoption **Power Apps** ist aus dem Modul **Systemverwaltung** verschwunden.</span><span class="sxs-lookup"><span data-stu-id="6b3f6-105">The **Power Apps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="6b3f6-106">**Ursache**</span><span class="sxs-lookup"><span data-stu-id="6b3f6-106">**Cause**</span></span>

<span data-ttu-id="6b3f6-107">Das Design der Benutzeroberfläche (UI) wurde verändert, und Microsoft Power Apps ist jetzt im standardmäßigen Personalisierungsmodell enthalten.</span><span class="sxs-lookup"><span data-stu-id="6b3f6-107">The user interface (UI) design has been changed, and Microsoft Power Apps is now included in the standard personalization model.</span></span>

<span data-ttu-id="6b3f6-108">**Lösung**</span><span class="sxs-lookup"><span data-stu-id="6b3f6-108">**Resolution**</span></span>

<span data-ttu-id="6b3f6-109">Die Art und Weise, wie Power Apps jetzt eingebettet ist, hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="6b3f6-109">The way that Power Apps are embedded has been changed.</span></span> <span data-ttu-id="6b3f6-110">Power Apps wird jetzt über das Personalisierungsmodell hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6b3f6-110">Power Apps are now added through the personalization model.</span></span> <span data-ttu-id="6b3f6-111">Sie können Power Apps fast allen Seiten in Microsoft Dynamics 365 Talent hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6b3f6-111">You can add Power Apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="6b3f6-112">Informationen zum Einbetten von Power Apps in Talent finden Sie unter [Einbetten von Microsoft Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="6b3f6-112">For information about how to embed Power Apps in Talent, see [Embed Microsoft Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="6b3f6-113">Jeder Power Apps-Kunde, der Apps vor der Änderung eingebettet hat, sollte auf das neue Modell aktualisiert worden sein.</span><span class="sxs-lookup"><span data-stu-id="6b3f6-113">Any Power Apps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="6b3f6-114">Die Schaltfläche **Power Apps** befindet sich in der oberen rechten Ecke beinahe jeder Seite in Talent.</span><span class="sxs-lookup"><span data-stu-id="6b3f6-114">The **Power Apps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="6b3f6-115">Sie können diese Schaltfläche verwenden, um Power Apps einzufügen.</span><span class="sxs-lookup"><span data-stu-id="6b3f6-115">You can use this button to insert Power Apps.</span></span>

<span data-ttu-id="6b3f6-116">Hier ist ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="6b3f6-116">Here is an example.</span></span>

1. <span data-ttu-id="6b3f6-117">Wechseln Sie zu **Personalverwaltung \> Links \> Arbeitskräfte \> Mitarbeiter**.</span><span class="sxs-lookup"><span data-stu-id="6b3f6-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="6b3f6-118">Wählen Sie die Schaltfläche **Power Apps** und dann **PowerApp einfügen** aus.</span><span class="sxs-lookup"><span data-stu-id="6b3f6-118">Select the **Power Apps** button, and then select **Insert a PowerApp**.</span></span>

    ![Power Apps-Schaltfläche](media/png.png)

3. <span data-ttu-id="6b3f6-120">Füllen Sie die Felder im Dialogfeld **Eine PowerApp einfügen** aus.</span><span class="sxs-lookup"><span data-stu-id="6b3f6-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![Ein PowerApp-Dialogfeld einfügen](media/insert-powerapp.png)

<span data-ttu-id="6b3f6-122">Gehen Sie alternativ folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="6b3f6-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="6b3f6-123">Wählen Sie im Aktivitätsbereich der Seite in der Registerkarte **Optionen** in der Gruppe **Personalisieren** die Option **Dieses Formular personalisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="6b3f6-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![Gruppe „Personalisieren” in der Registerkarte „Optionen”](media/options.png)

    <span data-ttu-id="6b3f6-125">Die Personalisierungssymbolleiste wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6b3f6-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="6b3f6-126">Wählen Sie auf der Symbolleiste die Option **Einfügen \> PowerApp** aus.</span><span class="sxs-lookup"><span data-stu-id="6b3f6-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![Einfügen einer Power Apps-App mithilfe der Personalisierungssymbolleiste](media/powerapp-bar.png)
