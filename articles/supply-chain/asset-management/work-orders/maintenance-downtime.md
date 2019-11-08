---
title: Wartungsausfallzeit
description: In diesem Thema wird Wartungsausfallzeit in Asset Management beschrieben.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
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
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ad9f1b2a0e63b4fb0d6daceb451c3a1dc1ec7de7
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626152"
---
# <a name="maintenance-downtime"></a><span data-ttu-id="47eb2-103">Wartungsausfallzeit</span><span class="sxs-lookup"><span data-stu-id="47eb2-103">Maintenance downtime</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="47eb2-104">Sie können Wartungsausfallzeiterfassungen für die auf einem Arbeitsauftrag ausgewählte Anlage anlegen.</span><span class="sxs-lookup"><span data-stu-id="47eb2-104">You can create maintenance downtime registrations on the asset that is selected on a work order.</span></span> <span data-ttu-id="47eb2-105">Dies ist hilfreich, wenn Sie Wartungsausfallzeit auf einem oder mehreren Computern im Produktionsbereich erfassen möchten.</span><span class="sxs-lookup"><span data-stu-id="47eb2-105">This capability is useful if you want to register maintenance downtime on one or more machines in the production area.</span></span> <span data-ttu-id="47eb2-106">Zunächst erstellen Sie die Ursachencodes für Wartungsausfallzeit, die Sie verwenden möchten, z. B. **Ausfall** und **Geplanter Stopp**.</span><span class="sxs-lookup"><span data-stu-id="47eb2-106">You first create the maintenance downtime reason codes that you want to use, such as **Breakdown** and **Planned stop**.</span></span> <span data-ttu-id="47eb2-107">Dies geschieht auf der Seite **Ursachencodes für Wartungsausfallzeit**.</span><span class="sxs-lookup"><span data-stu-id="47eb2-107">This step is done on the **Maintenance downtime reason codes** page.</span></span> <span data-ttu-id="47eb2-108">Als Nächstes können Sie auf der Seite **Wartungsausfallzeit** Wartungsausfallzeiterfassungen anlegen und die entsprechenden Ursachencodes für Wartungsausfallzeit hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="47eb2-108">You can then create maintenance downtime registrations on the **Maintenance downtime** page and add the relevant maintenance downtime reason codes.</span></span>

## <a name="create-maintenance-downtime-reason-codes"></a><span data-ttu-id="47eb2-109">Erstellen von Ursachencodes für Wartungsausfallzeit</span><span class="sxs-lookup"><span data-stu-id="47eb2-109">Create maintenance downtime reason codes</span></span>

1. <span data-ttu-id="47eb2-110">Wählen Sie **Anlagenmanagement** > **Einstellungen** > **Arbeitsaufträge** > **Ursachencodes für Wartungsausfallzeit** aus.</span><span class="sxs-lookup"><span data-stu-id="47eb2-110">Select **Asset management** > **Setup** > **Work orders** > **Maintenance downtime reason codes**.</span></span>

2. <span data-ttu-id="47eb2-111">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="47eb2-111">Select **New**.</span></span>

3. <span data-ttu-id="47eb2-112">Geben Sie im Feld **Ursachencode für Wartungsausfallzeit** eine Kennung für den Ursachencode für Wartungsausfallzeit ein.</span><span class="sxs-lookup"><span data-stu-id="47eb2-112">In the **Maintenance downtime reason code** field, enter an ID for the maintenance downtime reason code.</span></span>

4. <span data-ttu-id="47eb2-113">Geben Sie im Feld **Name** einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="47eb2-113">In the **Name** field, enter a name.</span></span>

5. <span data-ttu-id="47eb2-114">Aktivieren Sie das Kontrollkästchen **KPI enthalten**, wenn der Ursachencode in Berechnungen von Leistungskennzahlen (KPIs) für die Anlage enthalten sein soll.</span><span class="sxs-lookup"><span data-stu-id="47eb2-114">Select the **KPI include** check box if the reason code should be included in calculations of key performance indicators (KPIs) for the asset.</span></span> <span data-ttu-id="47eb2-115">Im Allgemeinen sollten geplante Produktionsstopps nicht in die KPI-Berechnungen einbezogen werden, da sie die erwartete Leistung nicht beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="47eb2-115">In general, planned production stops should not be included in KPI calculations, because they don't affect expected performance.</span></span>

6. <span data-ttu-id="47eb2-116">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="47eb2-116">Select **Save**.</span></span>

<span data-ttu-id="47eb2-117">Die folgende Abbildung zeigt ein Beispiel der Seite **Ursachencodes für Wartungsausfallzeit**.</span><span class="sxs-lookup"><span data-stu-id="47eb2-117">The illustration below shows an example of the **Maintenance downtime reason codes** page.</span></span>

![Abbildung 1](media/15-work-orders.png)

<span data-ttu-id="47eb2-119">Wenn Sie die von Ihnen gewünschten Ursachencodes für Wartungsausfallzeit angelegt haben, können Sie Wartungsausfallzeiterfassungen für Arbeitsaufträge und Anlagen anlegen.</span><span class="sxs-lookup"><span data-stu-id="47eb2-119">After you've created the maintenance downtime reason codes that you want to use, you can create maintenance downtime registrations for work orders and assets.</span></span>


## <a name="create-maintenance-downtime-registrations"></a><span data-ttu-id="47eb2-120">Erstellen von Wartungsausfallzeiterfassungen</span><span class="sxs-lookup"><span data-stu-id="47eb2-120">Create maintenance downtime registrations</span></span>

1. <span data-ttu-id="47eb2-121">Klicken Sie auf **Anlagenmanagement** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge**.</span><span class="sxs-lookup"><span data-stu-id="47eb2-121">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="47eb2-122">Wählen Sie den Arbeitsauftrag aus, und wählen Sie dann auf der Registerkarte **Arbeitsauftrag** in der Gruppe **Anlage** **Wartungsausfallzeit** aus.</span><span class="sxs-lookup"><span data-stu-id="47eb2-122">Select the work order, and then, on the **Work order** tab, in the **Asset** group, select **Maintenance downtime**.</span></span>

3. <span data-ttu-id="47eb2-123">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="47eb2-123">Select **New**.</span></span>

4. <span data-ttu-id="47eb2-124">Definieren Sie das Datums- und Uhrzeitintervall für die Wartungsausfallzeitregistrierung in den Feldern **Von** und **Bis**.</span><span class="sxs-lookup"><span data-stu-id="47eb2-124">In the **From** and **To** fields, define the date and time interval for the maintenance downtime registration.</span></span>

>[!NOTE]
><span data-ttu-id="47eb2-125">Wenn Sie das Feld **Bis** leer lassen, ist die Dauer in Stunden automatisch im Feld **Dauer** eingefügt.</span><span class="sxs-lookup"><span data-stu-id="47eb2-125">When you leave the **To** field, the duration in hours is automatically inserted in the **Duration** field.</span></span>

5. <span data-ttu-id="47eb2-126">Wählen Sie im Feld **Ursachencodes für Wartungsausfallzeit** einen Ursachencode aus.</span><span class="sxs-lookup"><span data-stu-id="47eb2-126">In the **maintenance downtime reason code** field, select a reason code.</span></span>

6. <span data-ttu-id="47eb2-127">Wiederholen Sie die Schritte 3 bis 5, um weitere Erfassungen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="47eb2-127">Repeat steps 3 through 5 to add more registrations.</span></span>

7. <span data-ttu-id="47eb2-128">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="47eb2-128">Select **Save**.</span></span>

<span data-ttu-id="47eb2-129">Die folgende Abbildung zeigt das Beispiel einer Registrierung für Wartungsausfallzeit.</span><span class="sxs-lookup"><span data-stu-id="47eb2-129">The illustration below shows an example of maintenance downtime registration.</span></span>

![Abbildung 2](media/16-work-orders.png)

<span data-ttu-id="47eb2-131">Der Kalender, der für die Berechnung einer Wartungsausfallzeiterfassung verwendet wird, hängt von Ihrer Auswahl bei der Einrichtung von Anlagen und Parametern ab.</span><span class="sxs-lookup"><span data-stu-id="47eb2-131">The calendar that is used to calculate a maintenance downtime registration depends on your selection in the setup of assets and parameters.</span></span> <span data-ttu-id="47eb2-132">Wenn eine Ressource auf einer Anlage im Feld **Ressource** im Inforegister **Anlage** auf der Seite **Alle Anlagen** ausgewählt wird, wird der für die zugehörige Ressourcengruppe eingerichtete Kalender verwendet, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="47eb2-132">If a resource is selected on an asset in the **Resource** field on the **Fixed asset** FastTab of the **All assets** page, the calendar that is set up for the associated resource group is used, as shown in the following illustration.</span></span>

![Abbildung 3](media/17-work-orders.png)

<span data-ttu-id="47eb2-134">Wenn keine Ressource auf der Anlage ausgewählt ist, wird der auf der Seite **Anlagenverwaltungsparameter** ausgewählte Standardkalender verwendet, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="47eb2-134">If no resource is selected on the asset, the standard calendar that is selected on the **Asset management parameters** page is used, as shown in the following illustration.</span></span>

![Abbildung 4](media/18-work-orders.png)

<span data-ttu-id="47eb2-136">Klicken Sie **Anlagenverwaltung** > **Abfragen** > **Wartungsausfallzeit**, um eine Übersicht über alle Wartungsausfallzeiterfassungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="47eb2-136">To see an overview of all maintenance downtime registrations, click **Asset management** > **Inquiries** > **Maintenance downtime**.</span></span>

>[!NOTE]
><span data-ttu-id="47eb2-137">Alle Kalender, die im Modul **Anlagenverwaltung** verwendet werden, werden in **Organisationsverwaltung** > **Einstellungen** > **Kalender** > **Kalender** eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="47eb2-137">All calendars that are used in the **Asset Management** module are set up in **Organization administration** > **Setup** > **Calendars** > **Calendars**.</span></span>

