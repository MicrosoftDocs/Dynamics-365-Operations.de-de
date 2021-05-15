---
title: Ermöglicht Qualitäts- und Qualitätsmangel-Management
description: Dieses Thema bietet einen Überblick über den Prozess zum Einrichten und Konfigurieren der Funktionen zum Management von Qualitätsmängeln und Abweichungen in Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome, InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 67d5da648e31d07d054246f5d308a6c6cdeb506c
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956253"
---
# <a name="enable-quality-and-nonconformance-management"></a><span data-ttu-id="dbf8e-103">Ermöglicht Qualitäts- und Qualitätsmangel-Management</span><span class="sxs-lookup"><span data-stu-id="dbf8e-103">Enable quality and nonconformance management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dbf8e-104">Dieses Thema bietet einen Überblick über den Prozess zum Einrichten und Konfigurieren der Funktionen zum Management von Qualitätsmängeln und Abweichungen in Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="dbf8e-104">This topic provides an overview of the process for setting up and configuring quality and nonconformance management features in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="enable-quality-and-nonconformance-management"></a><a name="enable-qm"></a><span data-ttu-id="dbf8e-105">Qualitäts- und Qualitätsmangel-Management aktivieren</span><span class="sxs-lookup"><span data-stu-id="dbf8e-105">Enable quality and nonconformance management</span></span>

<span data-ttu-id="dbf8e-106">Führen Sie diese Schritte aus, um das Qualitätsmanagement auf Ihrem System zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="dbf8e-106">Follow these steps to enable quality management on your system.</span></span>

1. <span data-ttu-id="dbf8e-107">Gehen Sie zu **Bestandsverwaltung \> Einrichtung \> Bestands- und Lagerverwaltungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="dbf8e-107">Go to **Inventory management \> Setup \> Inventory and warehouse management parameters**.</span></span>
1. <span data-ttu-id="dbf8e-108">Legen Sie auf der Registerkarte **Qualitätsmanagement** die Option **Qualitätsmanagement verwenden** auf *Ja* fest.</span><span class="sxs-lookup"><span data-stu-id="dbf8e-108">On the **Quality management** tab, set the **Use quality management** option to *Yes*.</span></span>
1. <span data-ttu-id="dbf8e-109">Geben Sie im Feld **Stundensatz** einen Arbeitsstundensatz in lokaler Währung ein.</span><span class="sxs-lookup"><span data-stu-id="dbf8e-109">In the **Hourly rate** field, enter an hourly labor rate in the local currency.</span></span> <span data-ttu-id="dbf8e-110">Der Stundensatz wird zur Berechnung der Kosten für Arbeitsgänge verwendet, die sich auf einen Qualitätsmangel beziehen.</span><span class="sxs-lookup"><span data-stu-id="dbf8e-110">The hourly rate is used to calculate costs for operations that are related to a nonconformance.</span></span> <span data-ttu-id="dbf8e-111">Der Stundensatz sowie die berechneten Kosten fungieren als Referenzinformationen für einen Qualitätsmangel.</span><span class="sxs-lookup"><span data-stu-id="dbf8e-111">The hourly rate and calculated costs provide reference information for a nonconformance.</span></span> <span data-ttu-id="dbf8e-112">Sie interagieren nicht mit anderen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="dbf8e-112">They don't interact with other functionality.</span></span>
1. <span data-ttu-id="dbf8e-113">Wählen Sie **Bericht einrichten**.</span><span class="sxs-lookup"><span data-stu-id="dbf8e-113">Select **Report setup**.</span></span>
1. <span data-ttu-id="dbf8e-114">Fügen Sie neue Zeilen für die verschiedenen Berichtstypen hinzu und wählen Sie die Art des Dokuments, das für jeden Bericht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="dbf8e-114">Add new lines for the various report types, and select the type of document to use for each report.</span></span>
1. <span data-ttu-id="dbf8e-115">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="dbf8e-115">Close the page.</span></span>
1. <span data-ttu-id="dbf8e-116">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="dbf8e-116">Close the page.</span></span>

## <a name="quality-management-configuration-process"></a><span data-ttu-id="dbf8e-117">Qualitätsmanagement Konfigurationsprozess</span><span class="sxs-lookup"><span data-stu-id="dbf8e-117">Quality management configuration process</span></span>

<span data-ttu-id="dbf8e-118">Bevor Sie beginnen können, die Funktionen des Qualitätsmanagements zu verwenden und Qualitätsprüfungsaufträge zu generieren, müssen Sie das System und die Voraussetzungen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="dbf8e-118">Before you can start to use the quality management features and generate quality orders, you must configure the system and prerequisites.</span></span> <span data-ttu-id="dbf8e-119">Hier finden Sie eine Liste der Schritte, die für die Konfiguration des Qualitätsmanagements erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="dbf8e-119">Here is a list of the steps that are required to configure quality management.</span></span>

1. <span data-ttu-id="dbf8e-120">[Qualitäts- und Qualitätsmangel-Management aktivieren](#enable-qm).</span><span class="sxs-lookup"><span data-stu-id="dbf8e-120">[Enable quality and nonconformance management](#enable-qm).</span></span>
1. <span data-ttu-id="dbf8e-121">Optional: [Konfigurieren Sie Prüfgeräte](quality-test-instruments.md).</span><span class="sxs-lookup"><span data-stu-id="dbf8e-121">Optional: [Configure test instruments](quality-test-instruments.md).</span></span>
1. <span data-ttu-id="dbf8e-122">[Konfigurieren Sie Tests](quality-tests.md).</span><span class="sxs-lookup"><span data-stu-id="dbf8e-122">[Configure tests](quality-tests.md).</span></span>
1. <span data-ttu-id="dbf8e-123">[Konfigurieren Sie Test-Variablen und -Ergebnisse](quality-test-variables.md).</span><span class="sxs-lookup"><span data-stu-id="dbf8e-123">[Configure test variables and outcomes](quality-test-variables.md).</span></span>
1. <span data-ttu-id="dbf8e-124">[Konfigurieren Sie Testgruppen](quality-test-groups.md).</span><span class="sxs-lookup"><span data-stu-id="dbf8e-124">[Configure test groups](quality-test-groups.md).</span></span>
1. <span data-ttu-id="dbf8e-125">Optional: [Konfigurieren Sie Qualitätsgruppen, und verknüpfen Sie sie mit Produkten](quality-groups.md).</span><span class="sxs-lookup"><span data-stu-id="dbf8e-125">Optional: [Configure quality groups, and link to products](quality-groups.md).</span></span>
1. <span data-ttu-id="dbf8e-126">Optional: [Qualitätszuordnungen konfigurieren](quality-associations.md).</span><span class="sxs-lookup"><span data-stu-id="dbf8e-126">Optional: [Configure quality associations](quality-associations.md).</span></span>

<span data-ttu-id="dbf8e-127">Nachdem die Konfiguration abgeschlossen ist, können Sie damit beginnen, Qualitätsprüfungsaufträge zu erstellen und zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="dbf8e-127">After the configuration is completed, you can start to create and process quality orders.</span></span> <span data-ttu-id="dbf8e-128">Weitere Informationen zum Erstellen und Arbeiten mit Qualitätsprüfungsaufträgen finden Sie unter [Qualitätsprüfungsaufträge](quality-orders.md).</span><span class="sxs-lookup"><span data-stu-id="dbf8e-128">For more information about how to create and work with quality orders, see [Quality orders](quality-orders.md).</span></span>

## <a name="nonconformance-management-configuration-process"></a><span data-ttu-id="dbf8e-129">Konfigurationsprozess für das Qualitätsmangel-Management</span><span class="sxs-lookup"><span data-stu-id="dbf8e-129">Nonconformance management configuration process</span></span>

<span data-ttu-id="dbf8e-130">Bevor Sie beginnen können, die Funktionen zur Verwaltung von Qualitätsmängeln zu verwenden und Qualitätsmängel zu erzeugen, müssen Sie das System und die Voraussetzungen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="dbf8e-130">Before you can start to use the nonconformance management features and generate nonconformances, you must configure the system and prerequisites.</span></span> <span data-ttu-id="dbf8e-131">Hier ist eine Liste der Schritte, die zur Konfiguration des Qualitätsmangels erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="dbf8e-131">Here is a list of the steps that are required to configure nonconformance management.</span></span>

1. <span data-ttu-id="dbf8e-132">[Qualitäts- und Qualitätsmangel-Management aktivieren](#enable-qm).</span><span class="sxs-lookup"><span data-stu-id="dbf8e-132">[Enable quality and nonconformance management](#enable-qm).</span></span>
1. <span data-ttu-id="dbf8e-133">[Konfigurieren Sie Worker, die für die Genehmigung von Qualitätsmängeln zuständig sind](quality-responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="dbf8e-133">[Configure workers who are responsible for approving nonconformances](quality-responsible-workers.md).</span></span>
1. <span data-ttu-id="dbf8e-134">[Konfigurieren Sie Problemtypen](quality-problem-types.md).</span><span class="sxs-lookup"><span data-stu-id="dbf8e-134">[Configure problem types](quality-problem-types.md).</span></span>
1. <span data-ttu-id="dbf8e-135">[Konfigurieren Sie Quarantänezonen](quality-quarantine-zones.md).</span><span class="sxs-lookup"><span data-stu-id="dbf8e-135">[Configure quarantine zones](quality-quarantine-zones.md).</span></span>
1. <span data-ttu-id="dbf8e-136">[Konfigurieren Sie Diagnosetypen](quality-diagnostic-types.md).</span><span class="sxs-lookup"><span data-stu-id="dbf8e-136">[Configure diagnostic types](quality-diagnostic-types.md).</span></span>
1. <span data-ttu-id="dbf8e-137">[Vorgänge konfigurieren](quality-operations.md).</span><span class="sxs-lookup"><span data-stu-id="dbf8e-137">[Configure operations](quality-operations.md).</span></span>
1. <span data-ttu-id="dbf8e-138">Optional: [Konfigurieren Sie Qualitätsbelastungen](quality-charges.md).</span><span class="sxs-lookup"><span data-stu-id="dbf8e-138">Optional: [Configure quality charges](quality-charges.md).</span></span>

<span data-ttu-id="dbf8e-139">Nachdem die Konfiguration abgeschlossen ist, können Sie beginnen, Qualitätsmängel zu erstellen und zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="dbf8e-139">After the configuration is completed, you can start to create and process nonconformances.</span></span> <span data-ttu-id="dbf8e-140">Weitere Informationen über das Erstellen und Verarbeiten von Qualitätsmängeln finden Sie unter [Erstellen und Verarbeiten von Qualitätsmängeln](tasks/create-process-non-conformance.md).</span><span class="sxs-lookup"><span data-stu-id="dbf8e-140">For more information about how to create and work with nonconformances, see [Create and process nonconformances](tasks/create-process-non-conformance.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dbf8e-141">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="dbf8e-141">Additional resources</span></span>

- [<span data-ttu-id="dbf8e-142">Qualitätsmanagement – Übersicht</span><span class="sxs-lookup"><span data-stu-id="dbf8e-142">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="dbf8e-143">Qualitäts- und Qualitätsmangel-Management aktivieren</span><span class="sxs-lookup"><span data-stu-id="dbf8e-143">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="dbf8e-144">Qualitätsmanagement für Lagerortprozesse</span><span class="sxs-lookup"><span data-stu-id="dbf8e-144">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
