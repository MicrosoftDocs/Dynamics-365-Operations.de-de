---
title: Datenfelder in Steuerkonfigurationen hinzufügen
description: In diesem Thema wird erläutert, wie Sie Steuerkonfigurationen durch Hinzufügen von Datenfeldern anpassen.
author: kailiang
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b9d9fce81151ad70d57c69e389e238a6f9137d56
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819423"
---
# <a name="add-data-fields-in-tax-configurations"></a><span data-ttu-id="d6d3e-103">Datenfelder in Steuerkonfigurationen hinzufügen</span><span class="sxs-lookup"><span data-stu-id="d6d3e-103">Add data fields in tax configurations</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="d6d3e-104">In diesem Thema wird erläutert, wie Sie Steuerkonfigurationen anpassen, indem Sie [Datenfelder, die in der Steuerintegration hinzugefügt werden](tax-service-add-data-fields-tax-integration-by-extension.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="d6d3e-104">This topic explains how to customize tax configurations by using [data fields that are added in the tax integration](tax-service-add-data-fields-tax-integration-by-extension.md).</span></span>

## <a name="customize-the-tax-data-model"></a><span data-ttu-id="d6d3e-105">Steuerdatenmodell anpassen</span><span class="sxs-lookup"><span data-stu-id="d6d3e-105">Customize the tax data model</span></span>

1. <span data-ttu-id="d6d3e-106">Wechseln Sie in Microsoft Dynamics 365 Finance zu **Elektronische Berichterstellung** \> **Steuerkonfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="d6d3e-106">In Microsoft Dynamics 365 Finance, go to **Electronic Reporting** \> **Tax configurations**.</span></span>
2. <span data-ttu-id="d6d3e-107">Wählen Sie im Konfigurationsbaum **Steuerdatenmodell – Europa** aus.</span><span class="sxs-lookup"><span data-stu-id="d6d3e-107">In the configuration tree, select **Tax Data Model - Europe**.</span></span> <span data-ttu-id="d6d3e-108">Wählen Sie dann im Aktivitätsbereich **Konfiguration erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="d6d3e-108">Then, on the Action Pane, select **Create configuration**.</span></span>
3. <span data-ttu-id="d6d3e-109">Wählen Sie im Dropdown-Dialogfeld die Option **Modell des steuerpflichtigen Dokuments abgeleitet von Name: Steuerdatenmodell – Europa, Microsoft**. Geben Sie bei dieser Option einen Namen für das neue Steuerdatenmodell ein und wählen Sie dann **Konfiguration erstellen**.</span><span class="sxs-lookup"><span data-stu-id="d6d3e-109">In the drop-down dialog box, select the **Taxable document model derived from Name: Tax Data Model -- Europe, Microsoft** option, enter a name for the new tax data model, and then select **Create configuration**.</span></span>
4. <span data-ttu-id="d6d3e-110">Wählen Sie das Steuerdatenmodell aus, das Sie gerade erstellt haben, und wählen Sie dann im Aktionsbereich **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="d6d3e-110">Select the tax data model that you just created, and then, on the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="d6d3e-111">Erweitern Sie den Datenmodellbaum und wählen Sie **Positionen** und dann **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="d6d3e-111">Expand the data model tree, select **Lines**, and then select **New**.</span></span>
6. <span data-ttu-id="d6d3e-112">Geben Sie im Dialogfeld **Knoten erstellen** einen Namen ein, geben Sie den Elementtyp an und wählen Sie dann **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="d6d3e-112">In the **Create node** dialog box, enter a name, specify the item type, and then select **Add**.</span></span>
7. <span data-ttu-id="d6d3e-113">Fügen Sie alle erforderlichen Spalten hinzu.</span><span class="sxs-lookup"><span data-stu-id="d6d3e-113">Add any required columns.</span></span>
8. <span data-ttu-id="d6d3e-114">Wählen Sie im Aktivitätsbereich **Speichern** und dann **Abschließen**.</span><span class="sxs-lookup"><span data-stu-id="d6d3e-114">On the Action Pane, select **Save**, and then select **Complete**.</span></span>
9. <span data-ttu-id="d6d3e-115">Schließen Sie die Seite und zeigen Sie die fertige Version Ihres Steuerdatenmodells an.</span><span class="sxs-lookup"><span data-stu-id="d6d3e-115">Close the page, and view the completed version of your tax data model.</span></span>

## <a name="customize-the-tax-configuration"></a><span data-ttu-id="d6d3e-116">Anpassen der Steuerkonfiguration</span><span class="sxs-lookup"><span data-stu-id="d6d3e-116">Customize the tax configuration</span></span>

1. <span data-ttu-id="d6d3e-117">Wechseln Sie in Finance zu **Elektronische Berichterstellung** \> **Steuerkonfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="d6d3e-117">In Finance, go to **Electronic reporting** \> **Tax configurations**.</span></span>
2. <span data-ttu-id="d6d3e-118">Wählen Sie im Konfigurationsbaum **Steuerkonfiguration – Europa** aus.</span><span class="sxs-lookup"><span data-stu-id="d6d3e-118">In the configuration tree, select **Tax Configuration -- Europe**.</span></span> <span data-ttu-id="d6d3e-119">Wählen Sie dann im Aktivitätsbereich **Konfiguration erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="d6d3e-119">Then, on the Action Pane, select **Create configuration**.</span></span>
3. <span data-ttu-id="d6d3e-120">Wählen Sie im Dropdown-Dialogfeld die Option **Steuerdienstkonfiguration abgeleitet von Name: Steuerkonfiguration – Europa, Microsoft**. Geben Sie bei dieser Option einen Namen für die neue Steuerkonfiguration ein und wählen Sie dann **Konfiguration erstellen**.</span><span class="sxs-lookup"><span data-stu-id="d6d3e-120">In the drop-down dialog box, select the **Tax service configuration derived from Name: Tax Configuration -- Europe, Microsoft** option, enter a name for the new tax configuration, and then select **Create configuration**.</span></span>
4. <span data-ttu-id="d6d3e-121">Wählen Sie die Steuerkonfiguration aus, das Sie gerade erstellt haben, und wählen Sie dann im Aktionsbereich **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="d6d3e-121">Select the tax configuration that you just created, and then, on the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="d6d3e-122">Wählen Sie im Abschnitt **Eigenschaften** im Feld **Datenmodell** das zuvor erstellte benutzerdefinierte Steuerdatenmodell aus.</span><span class="sxs-lookup"><span data-stu-id="d6d3e-122">In the **Properties** section, in the **Data model** field, select the customized tax data model that you created earlier.</span></span>
6. <span data-ttu-id="d6d3e-123">Wählen Sie im Feld **Datenmodellversion** die fertige Version des Steuerdatenmodells aus.</span><span class="sxs-lookup"><span data-stu-id="d6d3e-123">In the **Data model version** field, select the completed version of the tax data model.</span></span>
7. <span data-ttu-id="d6d3e-124">Wählen Sie **Hinzufügen** und fügen Sie die erforderlichen Steuermaßnahmen hinzu.</span><span class="sxs-lookup"><span data-stu-id="d6d3e-124">Select **Add**, and add the required tax measures.</span></span>
8. <span data-ttu-id="d6d3e-125">Wählen Sie im Aktivitätsbereich **Speichern** und dann **Abschließen**.</span><span class="sxs-lookup"><span data-stu-id="d6d3e-125">On the Action Pane, select **Save**, and then select **Complete**.</span></span>
9. <span data-ttu-id="d6d3e-126">Schließen Sie die Seite und zeigen Sie die fertige Version Ihrer Steuerkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="d6d3e-126">Close page, and view the completed version of your tax configuration.</span></span>

## <a name="implement-tax-features-in-the-customized-tax-configuration"></a><span data-ttu-id="d6d3e-127">Implementieren von Steuerfunktionen in der benutzerdefinierten Steuerkonfiguration</span><span class="sxs-lookup"><span data-stu-id="d6d3e-127">Implement tax features in the customized tax configuration</span></span>

1. <span data-ttu-id="d6d3e-128">Wechseln Sie in Regulatory Configuration Services (RCS) zu **Globalisierungsfunktionen** \> **Steuern**.</span><span class="sxs-lookup"><span data-stu-id="d6d3e-128">In Regulatory Configuration Service (RCS), go to **Globalization Features** \> **Tax**.</span></span>
2. <span data-ttu-id="d6d3e-129">Wählen Sie **Hinzufügen**, geben Sie Informationen zur neuen Funktion ein und wählen Sie dann **Funktion erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="d6d3e-129">Select **Add**, enter information about the new feature, and then select **Create feature**.</span></span>
3. <span data-ttu-id="d6d3e-130">Wählen Sie auf der Registerkarte **Versionen** die Funktion aus und wählen Sie dann **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="d6d3e-130">On the **Versions** tab, select the feature, and then select **Edit**.</span></span>
4. <span data-ttu-id="d6d3e-131">Wählen Sie auf der Registerkarte **Allgemein** im Feld **Konfigurationsversion** die angepasste Steuerkonfiguration und -version aus.</span><span class="sxs-lookup"><span data-stu-id="d6d3e-131">On the **General** tab, in the **Configuration version** field, select the customized tax configuration and version.</span></span>
5. <span data-ttu-id="d6d3e-132">Wählen Sie im Dialogfeld **Spalten verwalten** die Kopf- und Positionsspalten aus, die Sie in Ihre benutzerdefinierte Steuermaßnahme aufnehmen möchten, und klicken Sie dann auf die Schaltfläche mit dem Rechtspfeil, um sie der **Ausgewählte Spalten**-Liste hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="d6d3e-132">In the **Manage columns** dialog box, select the header and line columns that you want to include in your customized tax measure, and then select the right arrow button to add them to the **Selected columns** list.</span></span>
