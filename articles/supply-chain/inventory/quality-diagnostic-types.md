---
title: Diagnosetypen für Qualitätsmängel
description: Dieses Thema beschreibt, wie Sie Diagnosetypen verwenden und erstellen, die mit Qualitätsmängeln verwendet werden können.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestDiagnosticType, InventTestCorrection
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 19fcd57e28efabd6ca32c444ab961b876bde424d
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956663"
---
# <a name="diagnostic-types-for-nonconformances"></a><span data-ttu-id="bbdfe-103">Diagnosetypen für Qualitätsmängel</span><span class="sxs-lookup"><span data-stu-id="bbdfe-103">Diagnostic types for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bbdfe-104">Dieses Thema beschreibt, wie Sie Diagnosetypen verwenden und erstellen, die mit Qualitätsmängeln verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="bbdfe-104">This topic describes how to use and create diagnostic types that can be used with nonconformances.</span></span>

<span data-ttu-id="bbdfe-105">Sie verwenden die Seite **Diagnosetypen**, um eine Klassifizierung von Diagnoseaktionen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="bbdfe-105">You use the **Diagnostic types** page to define a classification of diagnostic actions.</span></span> <span data-ttu-id="bbdfe-106">Wenn Sie dann eine Korrektur für einen Qualitätsmangel erstellen, wählen Sie eine Diagnose aus.</span><span class="sxs-lookup"><span data-stu-id="bbdfe-106">Then, when you create a correction for a nonconformance, you select a diagnostic.</span></span> <span data-ttu-id="bbdfe-107">Durch eine Korrektur werden die Diagnoseaktivität für eine genehmigte Nichtübereinstimmung sowie die ausführende Person angegeben.</span><span class="sxs-lookup"><span data-stu-id="bbdfe-107">A correction specifies what type of diagnostic action should be taken for an approved nonconformance, and who should take that action.</span></span> <span data-ttu-id="bbdfe-108">Außerdem werden das angeforderte und das geplante Abschlussdatum angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bbdfe-108">It also specifies the requested completion date and the planned completion date.</span></span>

## <a name="examples-of-diagnostic-types"></a><span data-ttu-id="bbdfe-109">Beispiele für Diagnosetypen</span><span class="sxs-lookup"><span data-stu-id="bbdfe-109">Examples of diagnostic types</span></span>

<span data-ttu-id="bbdfe-110">Sie arbeiten für eine produzierende Firma, und mehrere Elemente haben Qualitätstests nicht bestanden.</span><span class="sxs-lookup"><span data-stu-id="bbdfe-110">You work for a manufacturing company, and several items have failed quality tests.</span></span> <span data-ttu-id="bbdfe-111">Diese Elemente werden in einen Quarantänebereich verschoben und als Qualitätsmangel gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bbdfe-111">Those items are moved into a quarantine area and marked as nonconforming products.</span></span> <span data-ttu-id="bbdfe-112">Ein Datensatz für Qualitätsmängel wird in Microsoft Dynamics 365 Supply Chain Management erstellt, um die Details bis zur Problemlösung zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="bbdfe-112">A nonconformance record is created in Microsoft Dynamics 365 Supply Chain Management to track the details through issue resolution.</span></span>

<span data-ttu-id="bbdfe-113">In diesem Fall treten die Qualitätsprobleme auf, weil Lager in der Maschine, die die Elemente verpackt, schlecht geworden sind und sich überhitzen.</span><span class="sxs-lookup"><span data-stu-id="bbdfe-113">In this case, the quality issues are occurring because bearings in the machine that packages the items have gone bad and are overheating.</span></span> <span data-ttu-id="bbdfe-114">Die Korrektur für dieses Problem ist der Austausch der Teile in der Maschine.</span><span class="sxs-lookup"><span data-stu-id="bbdfe-114">The correction for this problem is to replace the parts in the machine.</span></span>

<span data-ttu-id="bbdfe-115">Wenn Sie die Diagnosetypen konfigurieren, können Sie mehrere Datensätze erstellen, von denen jeder eine andere Art von Problem darstellt, das die Maschine haben könnte.</span><span class="sxs-lookup"><span data-stu-id="bbdfe-115">When you configure the diagnostic types, you can create multiple records, each of which represents a different type of problem that the machine might have.</span></span> <span data-ttu-id="bbdfe-116">Alternativ können Sie einen generischen Diagnosetyp erstellen, der eine Maschinenreparatur darstellt.</span><span class="sxs-lookup"><span data-stu-id="bbdfe-116">Alternatively, you can create one generic diagnostic type that represents machine repair.</span></span>

## <a name="create-a-diagnostic-type"></a><span data-ttu-id="bbdfe-117">Erstellen Sie einen Diagnosetyp</span><span class="sxs-lookup"><span data-stu-id="bbdfe-117">Create a diagnostic type</span></span>

1. <span data-ttu-id="bbdfe-118">Gehen Sie zu **Bestandsverwaltung \> Einrichten \> Qualitätsmanagement \> Diagnosetypen**.</span><span class="sxs-lookup"><span data-stu-id="bbdfe-118">Go to **Inventory management \> Setup \> Quality management \> Diagnostic types**.</span></span>
1. <span data-ttu-id="bbdfe-119">Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Zeile zum Raster hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="bbdfe-119">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="bbdfe-120">Legen Sie für die neue Zeile die folgenden Felder fest:</span><span class="sxs-lookup"><span data-stu-id="bbdfe-120">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="bbdfe-121">**Diagnose** – Geben Sie eine eindeutige ID oder einen Namen für den Diagnosetyp ein.</span><span class="sxs-lookup"><span data-stu-id="bbdfe-121">**Diagnostic** – Enter a unique ID or name for the diagnostic type.</span></span>
    - <span data-ttu-id="bbdfe-122">**Beschreibung** – Geben Sie eine detaillierte Beschreibung der Diagnoseart ein.</span><span class="sxs-lookup"><span data-stu-id="bbdfe-122">**Description** – Enter a detailed description of the diagnostic type.</span></span>

1. <span data-ttu-id="bbdfe-123">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="bbdfe-123">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bbdfe-124">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bbdfe-124">Additional resources</span></span>

- [<span data-ttu-id="bbdfe-125">Qualitätsmanagement – Übersicht</span><span class="sxs-lookup"><span data-stu-id="bbdfe-125">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="bbdfe-126">Qualitäts- und Qualitätsmangel-Management aktivieren</span><span class="sxs-lookup"><span data-stu-id="bbdfe-126">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="bbdfe-127">Mitarbeiter, der für die Genehmigung von Qualitätsmängeln verantwortlich ist</span><span class="sxs-lookup"><span data-stu-id="bbdfe-127">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="bbdfe-128">Quarantänezonen für Qualitätsmängel</span><span class="sxs-lookup"><span data-stu-id="bbdfe-128">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="bbdfe-129">Problemtypen für Qualitätsmängel</span><span class="sxs-lookup"><span data-stu-id="bbdfe-129">Problem types for nonconformances</span></span>](quality-problem-types.md)
- [<span data-ttu-id="bbdfe-130">Qualitätsbelastungen für Qualitätsmängel</span><span class="sxs-lookup"><span data-stu-id="bbdfe-130">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="bbdfe-131">Vorgänge für Qualitätsmängel</span><span class="sxs-lookup"><span data-stu-id="bbdfe-131">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="bbdfe-132">Qualitätsmanagement für Lagerortprozesse</span><span class="sxs-lookup"><span data-stu-id="bbdfe-132">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
