---
title: Ursachencodes einrichten
description: Dynamics 365 Human Resources erläutert anhand von Ursachencodes, warum sich die Vorteile eines Mitarbeiters ändern.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ee74cb8b11c9b72940448077ee485ade4c0b7a39
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801046"
---
# <a name="set-up-reason-codes"></a><span data-ttu-id="f936c-103">Ursachencodes einrichten</span><span class="sxs-lookup"><span data-stu-id="f936c-103">Set up reason codes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f936c-104">Dynamics 365 Human Resources erläutert anhand von Ursachencodes, warum sich die Vorteile eines Mitarbeiters ändern.</span><span class="sxs-lookup"><span data-stu-id="f936c-104">Dynamics 365 Human Resources uses reason codes to explain why an employee’s benefits are changing.</span></span>

> [!NOTE]
> <span data-ttu-id="f936c-105">Ab Januar 2021 werden Ursachencodes zum **Personalverwaltung**-Arbeitsbereich statt zum **Vorteilsverwaltung**-Arbeitsbereich migriert.</span><span class="sxs-lookup"><span data-stu-id="f936c-105">As of January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="f936c-106">Weitere Informationen finden Sie unter [Ursachencodes manuell in die Personalverwaltung migrieren](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).</span><span class="sxs-lookup"><span data-stu-id="f936c-106">For more information, see [Manually migrate reason codes to Personnel management](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).</span></span>

## <a name="create-reason-codes"></a><span data-ttu-id="f936c-107">Erstellen von Ursachencodes</span><span class="sxs-lookup"><span data-stu-id="f936c-107">Create reason codes</span></span>

1. <span data-ttu-id="f936c-108">In dem **Personalverwaltung**-Arbeitsbereich (oder, wenn Ihre Ursachencodes noch nicht migriert wurden, im **Vorteilsverwaltung**-Arbeitsbereich) wählen Sie **Links** und dann **Ursachencodes** aus.</span><span class="sxs-lookup"><span data-stu-id="f936c-108">In the **Personnel management** workspace (or **Benefits management** workspace if your reason codes haven't yet migrated), select **Links**, and then select **Reason codes**.</span></span>

2. <span data-ttu-id="f936c-109">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="f936c-109">Select **New**.</span></span>

3. <span data-ttu-id="f936c-110">Geben Sie Werte für die folgenden Felder an:</span><span class="sxs-lookup"><span data-stu-id="f936c-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="f936c-111">Feld</span><span class="sxs-lookup"><span data-stu-id="f936c-111">Field</span></span> | <span data-ttu-id="f936c-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f936c-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f936c-113">**Ursachencode**</span><span class="sxs-lookup"><span data-stu-id="f936c-113">**Reason code**</span></span> | <span data-ttu-id="f936c-114">Ein eindeutiger Name, der den Grund angibt, aus dem ein Mitarbeiter die Registrierung eines Vergütungsplans ändern würde.</span><span class="sxs-lookup"><span data-stu-id="f936c-114">A unique name to identify the reason an employee would change a benefit plan enrollment.</span></span> |
   | <span data-ttu-id="f936c-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f936c-115">**Description**</span></span> | <span data-ttu-id="f936c-116">Eine Beschreibung des Ursachencodes.</span><span class="sxs-lookup"><span data-stu-id="f936c-116">A description of the reason code.</span></span> |

4. <span data-ttu-id="f936c-117">Legen Sie unter **Zutreffende Szenarios** die Option **Vorteilsverwaltung** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="f936c-117">Under **Applicable scenarios**, set **Benefits management** to **Yes**.</span></span> <span data-ttu-id="f936c-118">(Gilt nicht, wenn Ihre Ursachencodes noch nicht auf den **Personalverwaltung**-Arbeitsbereich migriert wurden.)</span><span class="sxs-lookup"><span data-stu-id="f936c-118">(Not applicable if your reason codes haven't yet migrated to the **Personnel management** workspace.)</span></span>

5. <span data-ttu-id="f936c-119">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="f936c-119">Select **Save**.</span></span>

## <a name="manually-migrate-reason-codes-to-personnel-management"></a><span data-ttu-id="f936c-120">Ursachencodes manuell in die Personalverwaltung migrieren</span><span class="sxs-lookup"><span data-stu-id="f936c-120">Manually migrate reason codes to Personnel management</span></span>

<span data-ttu-id="f936c-121">Im Januar 2021 werden Ursachencodes zum **Personalverwaltung**-Arbeitsbereich statt zum **Vorteilsverwaltung**-Arbeitsbereich migriert.</span><span class="sxs-lookup"><span data-stu-id="f936c-121">In January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="f936c-122">Die meisten Ursachencodedaten werden automatisch in Ihre Umgebung migriert.</span><span class="sxs-lookup"><span data-stu-id="f936c-122">Most reason code data will automatically migrate in your environment.</span></span> <span data-ttu-id="f936c-123">Einige Ursachencodedaten werden möglicherweise nicht migriert.</span><span class="sxs-lookup"><span data-stu-id="f936c-123">Some reason code data might not migrate.</span></span> <span data-ttu-id="f936c-124">Beispielsweise haben Ursachencodes jetzt ein Maximum von 15 Zeichen, sodass Ursachencodes, die länger als 15 Zeichen sind, nicht automatisch migriert werden.</span><span class="sxs-lookup"><span data-stu-id="f936c-124">For example, reason codes now have a 15-character maximum, so any reason codes longer than 15 characters won't migrate automatically.</span></span>

<span data-ttu-id="f936c-125">Sie sehen ein Banner auf der **Links**-Seite des **Vorteilsverwaltung**-Arbeitsbereichs, das Sie über die Migration informiert und darüber, ob Ursachencodes nicht migriert wurden.</span><span class="sxs-lookup"><span data-stu-id="f936c-125">You'll see a banner on the **Links** page of the **Benefits management** workspace informing you about the migration and whether any reason codes didn't migrate.</span></span>

1. <span data-ttu-id="f936c-126">Wählen Sie **Ursachencodes** aus, um Einzelheiten zum Migrationsstatus zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f936c-126">Select **Reason codes** for details about migration status.</span></span>

   <span data-ttu-id="f936c-127">[![Ursachencodes](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span><span class="sxs-lookup"><span data-stu-id="f936c-127">[![Reason codes](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span></span>

2. <span data-ttu-id="f936c-128">Wählen Sie einen Ursachencode aus, der nicht migriert werden konnte.</span><span class="sxs-lookup"><span data-stu-id="f936c-128">Select a reason code that failed to migrate.</span></span>

   <span data-ttu-id="f936c-129">[![Migrationsstatus des Ursachencodes](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span><span class="sxs-lookup"><span data-stu-id="f936c-129">[![Reason code migration status](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span></span>

3. <span data-ttu-id="f936c-130">Wählen Sie **Ursachencode migrieren**.</span><span class="sxs-lookup"><span data-stu-id="f936c-130">Select **Migrate reason code**.</span></span>

   <span data-ttu-id="f936c-131">[![Ursachencode für Migration](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span><span class="sxs-lookup"><span data-stu-id="f936c-131">[![Migrate reason code](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span></span>

4. <span data-ttu-id="f936c-132">In dem **Migration von Vorteilsursachencodes**-Bereich haben Sie zwei Optionen für die Zuordnung zu einem Ursachencode der Personalverwaltung:</span><span class="sxs-lookup"><span data-stu-id="f936c-132">In the **Benefit reason code migration** pane, you have two options for mapping to a Personnel management reason code:</span></span>

   - <span data-ttu-id="f936c-133">Um einen vorhandenen Ursachencode in der Personalverwaltung zu verwenden, wählen Sie einen aus der **Vorhandenen Ursachencode verwenden**-Dropdown-Liste.</span><span class="sxs-lookup"><span data-stu-id="f936c-133">To use an existing reason code in Personnel management, choose one from the **Use existing reason code** dropdown.</span></span>
     > [!NOTE]
     > <span data-ttu-id="f936c-134">Sie können nur dann einen vorhandenen Ursachencode in der Personalverwaltung verwenden, wenn noch kein anderer Ursachencode für die Vorteilsverwaltung dorthin migriert wurde.</span><span class="sxs-lookup"><span data-stu-id="f936c-134">You can only use an existing reason code in Personnel management if another Benefits management reason code hasn't already migrated to it.</span></span>
   - <span data-ttu-id="f936c-135">Geben Sie einen neuen Ursachencode in **Neuer Ursachencode** ein, und geben Sie dann eine Beschreibung in ein **Neue Beschreibung** ein, um einen neuen Ursachencode in der Personalverwaltung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f936c-135">To create a new reason code in Personnel management, enter a new one in **New reason code**, and then enter a description in **New description**.</span></span>

   <span data-ttu-id="f936c-136">[![Zuordnung zu einem Ursachencode für die Personalverwaltung](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span><span class="sxs-lookup"><span data-stu-id="f936c-136">[![Map to a Personnel management reason code](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span></span>

<span data-ttu-id="f936c-137">Nachdem Ursachencodes in die Personalverwaltung migriert wurden, wird die Option für deren Verwendung in der Vorteilsverwaltung automatisch auf **Ja** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f936c-137">After reason codes migrate to Personnel management, the option for using them in Benefits management is automatically set to **Yes**.</span></span>

<span data-ttu-id="f936c-138">[![Ursachencodes in der Vorteilsverwaltung verwenden](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span><span class="sxs-lookup"><span data-stu-id="f936c-138">[![Use reason code in Benefits management](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]