---
title: Erstellen Sie ein Datenintegratorprojekt (Vorschau)
description: In diesem Thema wird erläutert, wie Sie ein Datenintegratorprojekt erstellen.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 59f85c64ea7b1f539a245e08b76bd6a34797b0ca
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186467"
---
# <a name="create-a-data-integrator-project-preview"></a><span data-ttu-id="a6802-103">Erstellen Sie ein Datenintegratorprojekt (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="a6802-103">Create a data integrator project (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="a6802-104">In diesem Thema wird erläutert, wie Sie ein Datenintegratorprojekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="a6802-104">This topic explains how to create a data integrator project.</span></span>

1. <span data-ttu-id="a6802-105">Melden Sie sich bei Microsoft Dynamics 365 Finance an.</span><span class="sxs-lookup"><span data-stu-id="a6802-105">Sign in to Microsoft Dynamics 365 Finance.</span></span>
2. <span data-ttu-id="a6802-106">Wechseln Sie zu **Arbeitsbereiche \> Datenverwaltung** und wählen Sie **Datenentitäten**.</span><span class="sxs-lookup"><span data-stu-id="a6802-106">Go to **Workspaces \> Data management**, and select **Data entities**.</span></span> <span data-ttu-id="a6802-107">Warten Sie, bis alle Datenentitäten aktualisiert wurden, bevor Sie mit dem nächsten Schritt fortfahren.</span><span class="sxs-lookup"><span data-stu-id="a6802-107">Wait until all the data entities have been refreshed before you move on to the next step.</span></span>
3. <span data-ttu-id="a6802-108">Öffnen Sie das [Power Apps-Portal](https://make.powerapps.com/) und befolgen Sie diese Schritte:</span><span class="sxs-lookup"><span data-stu-id="a6802-108">Open the [Power Apps portal](https://make.powerapps.com/), and follow these steps:</span></span>

    1. <span data-ttu-id="a6802-109">Wählen Sie die entsprechende Umgebung aus.</span><span class="sxs-lookup"><span data-stu-id="a6802-109">Select the appropriate environment.</span></span>
    2. <span data-ttu-id="a6802-110">Wählen Sie im linken Navigationsbereich **Daten \> Verbindungen** aus.</span><span class="sxs-lookup"><span data-stu-id="a6802-110">In the left navigation pane, select **Data \> Connections**.</span></span>
    3. <span data-ttu-id="a6802-111">Stellen Sie eine Verbindung zu geeigneten Instanzen der folgenden Elemente her:</span><span class="sxs-lookup"><span data-stu-id="a6802-111">Connect to appropriate instances of the following items:</span></span>

        - <span data-ttu-id="a6802-112">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="a6802-112">Dynamics 365</span></span>
        - <span data-ttu-id="a6802-113">Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a6802-113">Dynamics 365 for Fin & Ops</span></span>

4. <span data-ttu-id="a6802-114">Öffnen Sie die [Power Apps-Umgebungen](https://admin.powerapps.com/environments) und befolgen Sie diese Schritte:</span><span class="sxs-lookup"><span data-stu-id="a6802-114">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>

    1. <span data-ttu-id="a6802-115">Wählen Sie **Datenintegrator**.</span><span class="sxs-lookup"><span data-stu-id="a6802-115">Select **Data Integrator**.</span></span>
    2. <span data-ttu-id="a6802-116">Wählen Sie **Verbindungssätze**.</span><span class="sxs-lookup"><span data-stu-id="a6802-116">Select **Connection sets**.</span></span>
    3. <span data-ttu-id="a6802-117">Wählen Sie **Neuer Verbindungssatz**.</span><span class="sxs-lookup"><span data-stu-id="a6802-117">Select **New connection set**.</span></span>
    4. <span data-ttu-id="a6802-118">Geben Sie einen Namens für die Verbindung ein.</span><span class="sxs-lookup"><span data-stu-id="a6802-118">Enter a name for the connection.</span></span>
    5. <span data-ttu-id="a6802-119">Wählen Sie die entsprechenden Verbindungen für die folgenden Elemente aus:</span><span class="sxs-lookup"><span data-stu-id="a6802-119">Select the appropriate connections for the following items:</span></span>

        - <span data-ttu-id="a6802-120">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="a6802-120">Dynamics 365</span></span>
        - <span data-ttu-id="a6802-121">Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a6802-121">Dynamics 365 for Fin & Ops</span></span>

    6. <span data-ttu-id="a6802-122">Wählen Sie die entsprechende Organisationszuordnung aus.</span><span class="sxs-lookup"><span data-stu-id="a6802-122">Select the appropriate organization mapping.</span></span>
    7. <span data-ttu-id="a6802-123">Wählen Sie **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="a6802-123">Select **Create**.</span></span>

5. <span data-ttu-id="a6802-124">Öffnen Sie die [Power Apps-Umgebungen](https://admin.powerapps.com/environments) und befolgen Sie diese Schritte:</span><span class="sxs-lookup"><span data-stu-id="a6802-124">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>  

    1. <span data-ttu-id="a6802-125">Erstellen Sie Datenintegrationsprojekte für die folgenden Vorlagen mit dem soeben erstellten Verbindungssatz:</span><span class="sxs-lookup"><span data-stu-id="a6802-125">Create data integration projects for the following templates by using the connection set that you just created:</span></span>

        - <span data-ttu-id="a6802-126">Ergebnisse der Debitorenzahlungserkenntnisse (CDS an Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="a6802-126">Customer payment insights results (CDS to Fin and Ops)</span></span>
            - <span data-ttu-id="a6802-127">Wenn Sie Version 10.0.17 oder höher verwenden, müssen Sie die Vorlage mit dem Namen „Ergebnisse der Debitorenzahlungserkenntnisse (CDS an Finance and Operations 10.0.17+)“ verwenden.</span><span class="sxs-lookup"><span data-stu-id="a6802-127">If you are using version 10.0.17 or later, you need to use the template named, Customer payment insights result (CDS to Fin and Ops 10.0.17+).</span></span>
        - <span data-ttu-id="a6802-128">Ergebnisse der Cashflow-Zeitreihen (CDS an Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="a6802-128">Cash flow time series results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="a6802-129">Ergebnisse der Budget-Zeitreihen (CDS an Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="a6802-129">Budget time series results (CDS to Fin and Ops)</span></span>

    2. <span data-ttu-id="a6802-130">Legen Sie für jedes Projekt die entsprechende Zeitplanung fest.</span><span class="sxs-lookup"><span data-stu-id="a6802-130">Set the appropriate scheduling for each project.</span></span>

> [!NOTE]
> <span data-ttu-id="a6802-131">Wenn Sie die erforderlichen Entitäten in CDS nicht sehen, gehen Sie bitte zu **Guthaben und Inkasso > Einrichtung > Finance Insights > Parameter für Finance Insights**, aktivieren Sie die Funktion „Debitorenzahlungsvorhersagen“ und klicken Sie auf die Schaltfläche **Vorhersagemodell erstellen**.</span><span class="sxs-lookup"><span data-stu-id="a6802-131">If you do not see the required entities in CDS, please go to **Credit and collections > Setup > Finance Insights > Finance insights parameters**, enable Customer payment predictions feature and click on **Create prediction model** button.</span></span> <span data-ttu-id="a6802-132">Wenn die Bereitstellung des KI-Modells abgeschlossen ist (erfolgreich oder fehlgeschlagen), werden die zum Erstellen der Integration erforderlichen CDS-Entitäten in CDS bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="a6802-132">When the deployment of AI model is completed (successful or failed), the CDS entities needed to create integration will be deployed in CDS.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
