---
title: Wartungsausfallzeit
description: In diesem Thema wird Wartungsausfallzeit in Asset Management beschrieben.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cc79dc1b5911679586fa560142ada5add1a881d2
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918243"
---
# <a name="maintenance-downtime"></a><span data-ttu-id="bdd4f-103">Wartungsausfallzeit</span><span class="sxs-lookup"><span data-stu-id="bdd4f-103">Maintenance downtime</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="bdd4f-104">Sie können Wartungsausfallzeiterfassungen für die auf einem Arbeitsauftrag ausgewählte Anlage anlegen.</span><span class="sxs-lookup"><span data-stu-id="bdd4f-104">You can create maintenance downtime registrations on the asset selected on a work order.</span></span> <span data-ttu-id="bdd4f-105">Dies ist hilfreich, wenn Sie Wartungsausfallzeit auf einem oder mehreren Computern im Produktionsbereich erfassen möchten.</span><span class="sxs-lookup"><span data-stu-id="bdd4f-105">This is useful if you want to register maintenance downtime on one or more machines in the production area.</span></span> <span data-ttu-id="bdd4f-106">Zunächst erstellen Sie die Ursachencodes für Wartungsausfallzeit, die Sie verwenden möchten, z.B. Ausfall und geplanter Stopp.</span><span class="sxs-lookup"><span data-stu-id="bdd4f-106">First, you create the maintenance downtime reason codes that you want to use, for example, breakdown and planned stop.</span></span> <span data-ttu-id="bdd4f-107">Dies geschieht in den **Ursachencodes für Wartungsausfallzeit**.</span><span class="sxs-lookup"><span data-stu-id="bdd4f-107">This is done in **Maintenance downtime reason codes**.</span></span> <span data-ttu-id="bdd4f-108">Als nächstes können Sie unter **Wartungsausfallzeit** Wartungsausfallzeiterfassungen anlegen und die entsprechenden Ursachencodes hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="bdd4f-108">Next, you can create maintenance downtime registrations in **Maintenance downtime** and add the relevant reason codes.</span></span>

## <a name="create-maintenance-downtime-reason-codes"></a><span data-ttu-id="bdd4f-109">Erstellen von Ursachencodes für Wartungsausfallzeit</span><span class="sxs-lookup"><span data-stu-id="bdd4f-109">Create maintenance downtime reason codes</span></span>

1. <span data-ttu-id="bdd4f-110">Klicken Sie auf **Anlagenverwaltungsparameter** > **Einstellungen** > **Arbeitsaufträge** > **Ursachencodes für Wartungsausfallzeit**.</span><span class="sxs-lookup"><span data-stu-id="bdd4f-110">Click **Asset management** > **Setup** > **Work orders** > **Maintenance downtime reason codes**.</span></span>

2. <span data-ttu-id="bdd4f-111">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="bdd4f-111">Click **New**.</span></span>

3. <span data-ttu-id="bdd4f-112">Geben Sie eine Kennung im Feld **Ursachencodes für Wartungsausfallzeit** ein.</span><span class="sxs-lookup"><span data-stu-id="bdd4f-112">Insert an ID in the **Maintenance downtime reason code** field.</span></span>

4. <span data-ttu-id="bdd4f-113">Geben Sie im Feld **Name** einen Namen für den Ursachencode ein.</span><span class="sxs-lookup"><span data-stu-id="bdd4f-113">Insert a name for the reason code in the **Name** field.</span></span>

5. <span data-ttu-id="bdd4f-114">Aktivieren Sie das Kontrollkästchen **KPI enthalten**, wenn der Ursachencode in den Berechnungen der Anlage-KPI-Berechnung enthalten sein soll.</span><span class="sxs-lookup"><span data-stu-id="bdd4f-114">Select the **KPI include** check box if the reason code should be included in asset KPI calculations.</span></span> <span data-ttu-id="bdd4f-115">Im Allgemeinen sollten geplante Produktionsstopps nicht in die KPI-Berechnungen einbezogen werden, da sie die erwartete Leistung nicht beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="bdd4f-115">Generally, planned production stops should not be included in KPI calculations as they do not impact expected performance.</span></span>

6. <span data-ttu-id="bdd4f-116">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="bdd4f-116">Click **Save**.</span></span>

![Abbildung 1](media/15-work-orders.png)


<span data-ttu-id="bdd4f-118">Wenn Sie die von Ihnen gewünschten Ursachencodes für Wartungsausfallzeit angelegt haben, können Sie Wartungsausfallzeiterfassungen für Arbeitsaufträge und Anlagen anlegen.</span><span class="sxs-lookup"><span data-stu-id="bdd4f-118">When you have created the maintenance downtime reason codes you want to use, you can create maintenance downtime registrations for work orders and assets.</span></span>


## <a name="create-maintenance-downtime-registrations"></a><span data-ttu-id="bdd4f-119">Erstellen von Wartungsausfallzeiterfassungen</span><span class="sxs-lookup"><span data-stu-id="bdd4f-119">Create maintenance downtime registrations</span></span>

1. <span data-ttu-id="bdd4f-120">Klicken Sie auf **Anlagenmanagement** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge**.</span><span class="sxs-lookup"><span data-stu-id="bdd4f-120">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="bdd4f-121">Wählen Sie den Arbeitsauftrag aus und klicken Sie auf **Wartungsausfallzeit**.</span><span class="sxs-lookup"><span data-stu-id="bdd4f-121">Select the work order and click **Maintenance downtime**.</span></span>

3. <span data-ttu-id="bdd4f-122">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="bdd4f-122">Click **New**.</span></span>

4. <span data-ttu-id="bdd4f-123">Fügen Sie das Datums- und Uhrzeitintervall für die Wartungsausfallzeitregistrierung in den Feldern **Von** und **Bis** ein.</span><span class="sxs-lookup"><span data-stu-id="bdd4f-123">Insert date and time interval for the maintenance downtime registration in the **From** and **To** fields.</span></span>

5. <span data-ttu-id="bdd4f-124">Wenn Sie das Feld **Bis** leer lassen, ist die Dauer in Stunden automatisch im Feld **Dauer** eingefügt.</span><span class="sxs-lookup"><span data-stu-id="bdd4f-124">When you leave the **To** field, the duration in hours is automatically inserted in the **Duration** field.</span></span>

6. <span data-ttu-id="bdd4f-125">Wählen Sie im Feld **Ursachencodes für Wartungsausfallzeit** einen Ursachencode ein.</span><span class="sxs-lookup"><span data-stu-id="bdd4f-125">Select a reason code in the **maintenance downtime reason code** field.</span></span>

7. <span data-ttu-id="bdd4f-126">Wiederholen Sie die Schritte 3-6, wenn mehrere Erfassungen hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="bdd4f-126">Repeat steps 3-6 if you want to add more registrations.</span></span>

8. <span data-ttu-id="bdd4f-127">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="bdd4f-127">Click **Save**.</span></span>


![Abbildung 2](media/16-work-orders.png)


<span data-ttu-id="bdd4f-129">Der Kalender, der für die Berechnung einer Wartungsausfallzeiterfassung verwendet wird, hängt von Ihrer Auswahl bei der Einrichtung von Anlagen und Parametern ab.</span><span class="sxs-lookup"><span data-stu-id="bdd4f-129">The calendar used to calculate a maintenance downtime registration depends on your selection in the setup of assets and parameters.</span></span> <span data-ttu-id="bdd4f-130">Wenn eine Ressource auf einer Anlage im Feld **Alle Anlagen** > **Anlage** Inforegister > **Ressource** ausgewählt wird, wird der für die zugehörige Ressourcengruppe eingerichtete Kalender verwendet, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="bdd4f-130">If a resource is selected on an asset in **All assets** > **Fixed asset** FastTab > **Resource** field, the calendar set up for the associated resource group is used, as shown in the following figure.</span></span>

![Abbildung 3](media/17-work-orders.png)


<span data-ttu-id="bdd4f-132">Wenn keine Ressource auf der Anlage ausgewählt ist, wird der in den **Anlagenverwaltungsparameter** ausgewählte Standardkalender verwendet, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="bdd4f-132">If no resource is selected on the asset, the standard calendar selected in **Asset management parameters** is used, as shown in the following figure.</span></span>

![Abbildung 4](media/18-work-orders.png)


<span data-ttu-id="bdd4f-134">Klicken Sie **Unternehmensanlagenverwaltung** > **Abfragen** > **Wartungsausfallzeit**, um eine Übersicht über alle Wartungsausfallzeiterfassungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="bdd4f-134">Click **Enterprise asset management** > **Inquiries** > **Maintenance downtime** to see an overview of all maintenance downtime registrations.</span></span>

>[!NOTE]
><span data-ttu-id="bdd4f-135">Alle Kalender, die im Modul **Anlagenverwaltung** verwendet werden, werden in **Organisationsverwaltung** > **Einstellungen** > **Kalender** > **Kalender** eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="bdd4f-135">All calendars used in the **Asset Management** module are set up in **Organization administration** > **Setup** > **Calendars** > **Calendars**.</span></span>

