---
title: Arbeitskräfte ohne Beschäftigung
description: Arbeitskräfte, die nicht in der Zukunft, aktiv oder in der Vergangenheit bei Ihrer Organisation beschäftigt waren, erscheinen im Formular Arbeitskräfte ohne Beschäftigung.
author: andreabichsel
ms.date: 04/06/2021
ms.topic: ''
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkerV2, HRMMassHireProject, HRMMassHireLine, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-04-06
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1a137de25924f4c4ec6f6b1fe70f9d21af591c0
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924570"
---
# <a name="workers-without-employment"></a><span data-ttu-id="f42ab-103">Arbeitskräfte ohne Beschäftigung</span><span class="sxs-lookup"><span data-stu-id="f42ab-103">Workers without employment</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f42ab-104">Arbeitskräfte, die keine zukünftige, aktive oder historische Beschäftigung bei Ihrer Organisation haben, erscheinen im Formular **Arbeiter ohne Beschäftigung**.</span><span class="sxs-lookup"><span data-stu-id="f42ab-104">Workers with no future, active, or historical employment with your organization appear in the **Workers without employment** form.</span></span> <span data-ttu-id="f42ab-105">Arbeitskräfte mit diesem Status können erscheinen, wenn Sie Arbeitskräfte ohne Datensatz importieren, oder wenn Sie die Beschäftigung einer Arbeitskraft über **Arbeiter > Beschäftigungshistorie** löschen.</span><span class="sxs-lookup"><span data-stu-id="f42ab-105">Workers with this status can appear when you import workers without an employment record, or when you delete a worker's employment via **Workers > Employment history**.</span></span>

<span data-ttu-id="f42ab-106">Standardmäßig ist das Formular **Worker ohne Beschäftigung** für die folgenden Rollen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="f42ab-106">By default, the **Workers without employment** form is available to the following roles:</span></span>

- <span data-ttu-id="f42ab-107">Personalassistent</span><span class="sxs-lookup"><span data-stu-id="f42ab-107">Human Resources Assistant</span></span>
- <span data-ttu-id="f42ab-108">Personalmanager</span><span class="sxs-lookup"><span data-stu-id="f42ab-108">Human Resources Manager</span></span>
- <span data-ttu-id="f42ab-109">Personalbeschaffungsmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="f42ab-109">Recruiter</span></span>
- <span data-ttu-id="f42ab-110">Manager für Vergütung und Leistungen</span><span class="sxs-lookup"><span data-stu-id="f42ab-110">Comp and Benefits Manager</span></span>
- <span data-ttu-id="f42ab-111">Gehaltsabrechnung Administrator</span><span class="sxs-lookup"><span data-stu-id="f42ab-111">Payroll Administrator</span></span>
- <span data-ttu-id="f42ab-112">Gehaltsabrechnung Manager</span><span class="sxs-lookup"><span data-stu-id="f42ab-112">Payroll Manager</span></span>
- <span data-ttu-id="f42ab-113">Ausbildung Manager</span><span class="sxs-lookup"><span data-stu-id="f42ab-113">Training Manager</span></span>

<span data-ttu-id="f42ab-114">In der Liste **Arbeiter ohne Beschäftigung** können Sie die aufgeführten Personen löschen.</span><span class="sxs-lookup"><span data-stu-id="f42ab-114">In the **Workers without employment** list, you can delete the individuals listed.</span></span> <span data-ttu-id="f42ab-115">Standardmäßig ist diese Berechtigung der Rolle Human Resources Assistant zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="f42ab-115">By default, this privilege is given to the Human Resources Assistant role.</span></span> <span data-ttu-id="f42ab-116">Sie können dieses Recht mit den folgenden Schritten an andere Rollen weitergeben:</span><span class="sxs-lookup"><span data-stu-id="f42ab-116">You can give this privilege to other roles with the following steps:</span></span>

1. <span data-ttu-id="f42ab-117">Wählen Sie **Systemverwaltung** und dann **Sicherheitskonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="f42ab-117">Select **System administration**, and then select **Security configuration**.</span></span>

2. <span data-ttu-id="f42ab-118">Filtern Sie in der Registerkarte **Privilegien** die Liste der **Privilegien** nach **Arbeitskräfte pflegen**.</span><span class="sxs-lookup"><span data-stu-id="f42ab-118">In the **Privileges** tab, filter the **Privileges** list to **Maintain workers**.</span></span>

   <span data-ttu-id="f42ab-119">[![Liste der Filterprivilegien](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)</span><span class="sxs-lookup"><span data-stu-id="f42ab-119">[![Filter Privileges list](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)</span></span>

3. <span data-ttu-id="f42ab-120">Wählen Sie in der Spalte **Verweise** **Menüpunkte anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="f42ab-120">In the **References** column, select **Display menu items**.</span></span>

4. <span data-ttu-id="f42ab-121">In **Menüelemente anzeigen** wählen Sie **HcmWorkersWithoutEmployment**.</span><span class="sxs-lookup"><span data-stu-id="f42ab-121">In **Display menu items**, select **HcmWorkersWithoutEmployment**.</span></span>

   <span data-ttu-id="f42ab-122">[![Formular auswählen](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)</span><span class="sxs-lookup"><span data-stu-id="f42ab-122">[![Select form](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)</span></span>

5. <span data-ttu-id="f42ab-123">Legen Sie die Berechtigung **Löschen** auf **Gewähren** fest.</span><span class="sxs-lookup"><span data-stu-id="f42ab-123">Set the **Delete** permission to **Grant**.</span></span>

6. <span data-ttu-id="f42ab-124">Wählen Sie die Registerkarte **Unveröffentlichte Objekte** aus.</span><span class="sxs-lookup"><span data-stu-id="f42ab-124">Select the **Unpublished objects** tab.</span></span>

7. <span data-ttu-id="f42ab-125">Wählen Sie **Alle veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="f42ab-125">Select **Publish all**.</span></span>

   <span data-ttu-id="f42ab-126">[![Änderungen veröffentlichen](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)</span><span class="sxs-lookup"><span data-stu-id="f42ab-126">[![Publish changes](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]