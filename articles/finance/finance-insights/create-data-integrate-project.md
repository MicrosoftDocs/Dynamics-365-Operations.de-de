---
title: Erstellen Sie ein Datenintegratorprojekt (Vorschau)
description: In diesem Thema wird erläutert, wie Sie ein Datenintegratorprojekt erstellen.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 050c4f0fe1aea07c3866e2e9d7a6db6c758205ca
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208508"
---
# <a name="create-a-data-integrator-project-preview"></a><span data-ttu-id="e7705-103">Erstellen Sie ein Datenintegratorprojekt (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="e7705-103">Create a data integrator project (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="e7705-104">In diesem Thema wird erläutert, wie Sie ein Datenintegratorprojekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="e7705-104">This topic explains how to create a data integrator project.</span></span>

1. <span data-ttu-id="e7705-105">Melden Sie sich bei Microsoft Dynamics 365 Finance an.</span><span class="sxs-lookup"><span data-stu-id="e7705-105">Sign in to Microsoft Dynamics 365 Finance.</span></span>
2. <span data-ttu-id="e7705-106">Wechseln Sie zu **Arbeitsbereiche \> Datenverwaltung** und wählen Sie **Datenentitäten**.</span><span class="sxs-lookup"><span data-stu-id="e7705-106">Go to **Workspaces \> Data management**, and select **Data entities**.</span></span> <span data-ttu-id="e7705-107">Warten Sie, bis alle Datenentitäten aktualisiert wurden, bevor Sie mit dem nächsten Schritt fortfahren.</span><span class="sxs-lookup"><span data-stu-id="e7705-107">Wait until all the data entities have been refreshed before you move on to the next step.</span></span>
3. <span data-ttu-id="e7705-108">Öffnen Sie das [Power Apps-Portal](https://make.powerapps.com/) und befolgen Sie diese Schritte:</span><span class="sxs-lookup"><span data-stu-id="e7705-108">Open the [Power Apps portal](https://make.powerapps.com/), and follow these steps:</span></span>

    1. <span data-ttu-id="e7705-109">Wählen Sie die entsprechende Umgebung aus.</span><span class="sxs-lookup"><span data-stu-id="e7705-109">Select the appropriate environment.</span></span>
    2. <span data-ttu-id="e7705-110">Wählen Sie im linken Navigationsbereich **Daten \> Verbindungen** aus.</span><span class="sxs-lookup"><span data-stu-id="e7705-110">In the left navigation pane, select **Data \> Connections**.</span></span>
    3. <span data-ttu-id="e7705-111">Stellen Sie eine Verbindung zu geeigneten Instanzen der folgenden Elemente her:</span><span class="sxs-lookup"><span data-stu-id="e7705-111">Connect to appropriate instances of the following items:</span></span>

        - <span data-ttu-id="e7705-112">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="e7705-112">Dynamics 365</span></span>
        - <span data-ttu-id="e7705-113">Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e7705-113">Dynamics 365 for Fin & Ops</span></span>

4. <span data-ttu-id="e7705-114">Öffnen Sie die [Power Apps-Umgebungen](https://admin.powerapps.com/environments) und befolgen Sie diese Schritte:</span><span class="sxs-lookup"><span data-stu-id="e7705-114">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>

    1. <span data-ttu-id="e7705-115">Wählen Sie **Datenintegrator**.</span><span class="sxs-lookup"><span data-stu-id="e7705-115">Select **Data Integrator**.</span></span>
    2. <span data-ttu-id="e7705-116">Wählen Sie **Verbindungssätze**.</span><span class="sxs-lookup"><span data-stu-id="e7705-116">Select **Connection sets**.</span></span>
    3. <span data-ttu-id="e7705-117">Wählen Sie **Neuer Verbindungssatz**.</span><span class="sxs-lookup"><span data-stu-id="e7705-117">Select **New connection set**.</span></span>
    4. <span data-ttu-id="e7705-118">Geben Sie einen Namens für die Verbindung ein.</span><span class="sxs-lookup"><span data-stu-id="e7705-118">Enter a name for the connection.</span></span>
    5. <span data-ttu-id="e7705-119">Wählen Sie die entsprechenden Verbindungen für die folgenden Elemente aus:</span><span class="sxs-lookup"><span data-stu-id="e7705-119">Select the appropriate connections for the following items:</span></span>

        - <span data-ttu-id="e7705-120">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="e7705-120">Dynamics 365</span></span>
        - <span data-ttu-id="e7705-121">Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e7705-121">Dynamics 365 for Fin & Ops</span></span>

    6. <span data-ttu-id="e7705-122">Wählen Sie die entsprechende Organisationszuordnung aus.</span><span class="sxs-lookup"><span data-stu-id="e7705-122">Select the appropriate organization mapping.</span></span>
    7. <span data-ttu-id="e7705-123">Wählen Sie **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="e7705-123">Select **Create**.</span></span>

5. <span data-ttu-id="e7705-124">Öffnen Sie die [Power Apps-Umgebungen](https://admin.powerapps.com/environments) und befolgen Sie diese Schritte:</span><span class="sxs-lookup"><span data-stu-id="e7705-124">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>  

    1. <span data-ttu-id="e7705-125">Erstellen Sie Datenintegrationsprojekte für die folgenden Vorlagen mit dem soeben erstellten Verbindungssatz:</span><span class="sxs-lookup"><span data-stu-id="e7705-125">Create data integration projects for the following templates by using the connection set that you just created:</span></span>

        - <span data-ttu-id="e7705-126">Ergebnisse der Debitorenzahlungserkenntnisse (CDS an Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="e7705-126">Customer payment insights results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="e7705-127">Ergebnisse der Cashflow-Zeitreihen (CDS an Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="e7705-127">Cash flow time series results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="e7705-128">Ergebnisse der Budget-Zeitreihen (CDS an Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="e7705-128">Budget time series results (CDS to Fin and Ops)</span></span>

    2. <span data-ttu-id="e7705-129">Legen Sie für jedes Projekt die entsprechende Zeitplanung fest.</span><span class="sxs-lookup"><span data-stu-id="e7705-129">Set the appropriate scheduling for each project.</span></span>

> [!NOTE]
> <span data-ttu-id="e7705-130">Wenn Sie die erforderlichen Entitäten in CDS nicht sehen, gehen Sie bitte zu **Guthaben und Inkasso > Einrichtung > Finance Insights > Parameter für Finance Insights**, aktivieren Sie die Funktion „Debitorenzahlungsvorhersagen“ und klicken Sie auf die Schaltfläche **Vorhersagemodell erstellen**.</span><span class="sxs-lookup"><span data-stu-id="e7705-130">If you do not see the required entities in CDS, please go to **Credit and collections > Setup > Finance Insights > Finance insights parameters**, enable Customer payment predictions feature and click on **Create prediction model** button.</span></span> <span data-ttu-id="e7705-131">Wenn die Bereitstellung des KI-Modells abgeschlossen ist (erfolgreich oder fehlgeschlagen), werden die zum Erstellen der Integration erforderlichen CDS-Entitäten in CDS bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="e7705-131">When the deployment of AI model is completed (successful or failed), the CDS entities needed to create integration will be deployed in CDS.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="e7705-132">Datenschutzhinweis</span><span class="sxs-lookup"><span data-stu-id="e7705-132">Privacy notice</span></span>

<span data-ttu-id="e7705-133">Vorschauen (1) wenden möglicherweise weniger Datenschutz- und Sicherheitsmaßnahmen an als der Dynamics 365 Finance and Operations-Dienst, (2) sind nicht in der Service Level Agreement (SLA) für diesen Dienst enthalten, (3) sollten nicht zur Verarbeitung personenbezogener Daten oder anderer Daten verwendet werden, die gesetzlichen oder behördlichen Compliance-Anforderungen unterliegen, und (4) hat begrenzten Support.</span><span class="sxs-lookup"><span data-stu-id="e7705-133">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]