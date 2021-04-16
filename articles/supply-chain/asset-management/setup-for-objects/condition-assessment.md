---
title: Bedingungsbewertung
description: In diesem Thema wird erläutert, wie Sie eine Bedingungsbewertungsvorlage und -erfassung für eine Anlage in der Anlagenverwaltung erstellen.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectCondition, EntAssetConditionTemplate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 082a2bfd8818e511095e9ab2dcc22de59eb98d31
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808423"
---
# <a name="condition-assessment"></a><span data-ttu-id="16277-103">Bedingungsbewertung</span><span class="sxs-lookup"><span data-stu-id="16277-103">Condition assessment</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="16277-104">In diesem Thema wird erläutert, wie Sie eine Bedingungsbewertungsvorlage und -erfassung für eine Anlage in der Anlagenverwaltung erstellen.</span><span class="sxs-lookup"><span data-stu-id="16277-104">This topic explains how to create a condition assessment template and registration on an asset in Asset Management.</span></span> <span data-ttu-id="16277-105">Eine Bedingungsbewertung wird in regelmäßigen Intervallen durchgeführt. Das vorrangige Ziel einer solchen Bewertung ist, Zustandsdaten für Anlagen zu erstellen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="16277-105">Condition assessment is performed at regular intervals, and the primary objective is to create and maintain condition data on assets.</span></span> <span data-ttu-id="16277-106">Gesehen aus einer Perspektive der vorbeugenden Wartung ist es wichtig, zentrale Informationen zu überwachen, wie z. B. den aktuellen Zustand und die verbleibende Nutzungsdauer.</span><span class="sxs-lookup"><span data-stu-id="16277-106">Seen from a preventive maintenance perspective, it is important to monitor key information such as current condition, and remaining life span.</span></span> <span data-ttu-id="16277-107">Wenn Sie außerdem eine Bedingungsbewertung in regelmäßigen Intervallen ausführen, sind Sie in der Lage, die Bedingungen des Maschinenparks in Ihrer Fabrik zu überwachen und zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="16277-107">Furthermore, if you carry out condition assessment at regular intervals, you will be able to monitor and compare conditions on the machinery in your factory.</span></span>

<span data-ttu-id="16277-108">Die Bedingungsbewertung kann verwendet werden, um mehrere Bedingungen Ihrer Ausrüstung zu messen und zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="16277-108">Condition assessment can be used to measure and monitor many conditions on your equipment.</span></span> <span data-ttu-id="16277-109">Beispiel: Sie können Erschütterungen auf Maschinen messen.</span><span class="sxs-lookup"><span data-stu-id="16277-109">Example: You could measure vibrations on your machinery.</span></span> <span data-ttu-id="16277-110">Nachdem Sie Erschütterungsmessungen in der Anlagenverwaltung für verschiedene Arten von Ausrüstung erfasst haben, können Sie nach den aktuellen Bewertungen suchen und die Erschütterungsmessungen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="16277-110">After you have registered vibration measurements in Asset Management on various types of equipment, you can search for the latest registered assessment and view vibration measurements.</span></span>

<span data-ttu-id="16277-111">Die Bedingungsbewertung wird für Anlagen erstellt.</span><span class="sxs-lookup"><span data-stu-id="16277-111">Condition assessment is created on assets.</span></span> <span data-ttu-id="16277-112">Sie richten eine Bedingungsbewertungsvorlage für einen Anlagentyp ein, bevor Sie die Bedingungsbewertung durchführen.</span><span class="sxs-lookup"><span data-stu-id="16277-112">You set up a condition assessment template on an asset type before you carry out the condition assessment procedure.</span></span> <span data-ttu-id="16277-113">Der Grund für die Verwendung von Vorlagen für die Bedingungsbewertung ist, Abweichungen bei den Bedingungsdaten auf ähnlichen Anlagen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="16277-113">The reason for using templates for condition assessment is to avoid variation of condition data on similar assets.</span></span> <span data-ttu-id="16277-114">Die Reihenfolge für das Einrichten und Verwenden der Bedingungsbewertung in der Anlagenverwaltung ist folgende: Zuerst richten Sie die erforderlichen Bedingungsbewertungsvorlagen ein.</span><span class="sxs-lookup"><span data-stu-id="16277-114">The sequence for setting up and using condition assessment in Asset Management is: First you set up the required condition assessment templates.</span></span> <span data-ttu-id="16277-115">Dann ordnen Sie Vorlagen den Anlagentypen im Formular **Anlagentypen** zu.</span><span class="sxs-lookup"><span data-stu-id="16277-115">Next, you associate templates with asset types in the **Asset types** form.</span></span> <span data-ttu-id="16277-116">Schließlich können Sie Bedingungsbewertungserfassungen für eine Anlage im Formular **Anlagen** erstellen.</span><span class="sxs-lookup"><span data-stu-id="16277-116">Finally, you can create condition assessment registrations on an asset in the **Asset** form.</span></span>

## <a name="create-a-condition-assessment-template"></a><span data-ttu-id="16277-117">Bedingungsbewertungsvorlage erstellen</span><span class="sxs-lookup"><span data-stu-id="16277-117">Create a condition assessment template</span></span>

1. <span data-ttu-id="16277-118">Wählen Sie **Anlagenverwaltung** > **Einstellungen** > **Anlagentypen** > **Bedingungsbewertung** aus.</span><span class="sxs-lookup"><span data-stu-id="16277-118">Select **Asset management** > **Setup** > **Asset types** > **Condition assessment**.</span></span>
2. <span data-ttu-id="16277-119">Wählen Sie **Neu** aus, um eine neue Vorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="16277-119">Select **New** to create a new template.</span></span>
3. <span data-ttu-id="16277-120">Geben Sie eine ID für die Vorlage im Feld **Vorlage** ein.</span><span class="sxs-lookup"><span data-stu-id="16277-120">Insert and ID for the template in the **Template** field.</span></span>
4. <span data-ttu-id="16277-121">Geben Sie im Feld **Name** einen Namen für die Vorlage ein.</span><span class="sxs-lookup"><span data-stu-id="16277-121">Insert a name for the template in the **Name** field.</span></span>
5. <span data-ttu-id="16277-122">Fügen Sie auf dem Inforegister **Bedingungsbewertungspositionen** die für die Bedingungsbewertung benötigten Positionen hinzu. Hierbei wählen Sie auch den relevanten Bedingungstyp und die Maßeinheit aus.</span><span class="sxs-lookup"><span data-stu-id="16277-122">On the **Condition assessment lines** FastFab, add the lines required for the condition assessment, including selection of the appropriate condition type and measurement unit.</span></span>
6. <span data-ttu-id="16277-123">Fügen Sie auf dem Inforegister **Anlagentypen** die Anlagentypen hinzu, die die Bedingungsbewertungsvorlage verwenden sollen.</span><span class="sxs-lookup"><span data-stu-id="16277-123">On the **Asset types** FastTab, add the asset types that should use the condition assessment template.</span></span>
7. <span data-ttu-id="16277-124">In den Feldern **Positionen** und **Anlagentypen** in der Gruppe **Details** am oberen Rand des Bildschirms sehen Sie die Anzahl der Bewertungspositionen und Anlagentypen zur ausgewählten Bedingungsbewertungsvorlage.</span><span class="sxs-lookup"><span data-stu-id="16277-124">In the **Lines** and **Asset types** fields in the **Details** group at the top of the screen, you will see the number of assessment lines and asset types related to the selected condition assessment template.</span></span>


## <a name="create-condition-assessment-registration-on-an-asset"></a><span data-ttu-id="16277-125">Bedingungsbewertungserfassung für eine Anlage erstellen</span><span class="sxs-lookup"><span data-stu-id="16277-125">Create condition assessment registration on an asset</span></span>

1. <span data-ttu-id="16277-126">Wählen Sie **Anlagenverwaltung** > **Allgemeines** > **Anlagen** > **Alle Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="16277-126">Select **Asset management** > **Common** > **Assets** > **All Assets**.</span></span>
2. <span data-ttu-id="16277-127">Wählen Sie in der Liste eine Anlage aus, für die Sie eine Bedingungsbewertungserfassung erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="16277-127">In the list, select the asset for which you want to create a condition assessment registration.</span></span>
3. <span data-ttu-id="16277-128">Klicken Sie auf der Registerkarte **Allgemein** auf **Bedingungsbewertung**.</span><span class="sxs-lookup"><span data-stu-id="16277-128">On the **General** tab, click **Condition assessment**.</span></span>
4. <span data-ttu-id="16277-129">Klicken Sie auf **Neu**, um eine neue Erfassung zu tätigen.</span><span class="sxs-lookup"><span data-stu-id="16277-129">Click **New** to make a new registration.</span></span>
5. <span data-ttu-id="16277-130">Wählen Sie das Datum für die Bedingungsbewertung im Feld **Datum** aus.</span><span class="sxs-lookup"><span data-stu-id="16277-130">Select the date for the condition assessment in the **Date** field.</span></span>
6. <span data-ttu-id="16277-131">Wählen Sie im Feld **Arbeitskraft** den Namen der Arbeitskraft aus, die die Bewertungserfassung durchgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="16277-131">Select the name of the worker who carried out the assessment registration in the **Worker** field.</span></span>
7. <span data-ttu-id="16277-132">Im Feld **Positionen** sehen Sie die Anzahl der Bewertungspositionen, die in der Bedingungsbewertung eingerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="16277-132">In the **Lines** field, you see the number of assessment lines set up on the condition assessment.</span></span>
8. <span data-ttu-id="16277-133">Wählen eine Vorlage für die Bedingungsbewertung im Feld **Vorlage** aus.</span><span class="sxs-lookup"><span data-stu-id="16277-133">Select a template for the condition assessment in the **Template** field.</span></span> <span data-ttu-id="16277-134">Der Name der Vorlage wird automatisch im Feld **Name** eingefügt, und die zugehörigen Erfassungspositionen werden auf dem Inforegister **Bedingungsbewertungspositionen** eingefügt.</span><span class="sxs-lookup"><span data-stu-id="16277-134">The name of the template is automatically inserted in the **Name** field, and the related registration lines are inserted on the **Condition assessment lines** FastTab.</span></span>
9. <span data-ttu-id="16277-135">Sie können Notizen in Bezug auf die ausgewählte Bedingungsbewertung auf dem Inforegister **Hinweise** einfügen.</span><span class="sxs-lookup"><span data-stu-id="16277-135">You can insert notes relating to the selected condition assessment on the **Notes** FastTab.</span></span>
10. <span data-ttu-id="16277-136">Geben Sie für jede Bedingungsbewertungsposition Messungsdaten im Feld **Wert** ein.</span><span class="sxs-lookup"><span data-stu-id="16277-136">For each condition assessment line, insert measurement data in the **Value** field.</span></span>
11. <span data-ttu-id="16277-137">Sie können einen Kommentar zur ausgewählten Erfassungsposition auf dem Inforegister **Bedingungsbewertungspositionen** im Feld **Kommentare** eingeben.</span><span class="sxs-lookup"><span data-stu-id="16277-137">You can insert a comment relating to the selected registration line on the **Condition assessment lines** FastTab > **Comments** field.</span></span> <span data-ttu-id="16277-138">Wenn Sie einen Kommentar für eine Position hinzufügen, wird das Kontrollkästchen **Kommentar** automatisch aktiviert.</span><span class="sxs-lookup"><span data-stu-id="16277-138">If you add a comment on a line, the **Comment** check box is automatically selected.</span></span>

<span data-ttu-id="16277-139">Nachdem Sie eine Bedingungsbewertungserfassung für eine Anlage vorgenommen haben, können Sie einen Bedingungsbewertungsbericht drucken.</span><span class="sxs-lookup"><span data-stu-id="16277-139">After you have made a condition assessment registration on an asset, you can print a condition assessment report.</span></span>

>[!NOTE]
><span data-ttu-id="16277-140">Sie können Bedingungsbewertungen auch in einem Arbeitsauftrag erfassen (**Anlagenverwaltung** > **Allgemeines** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** > **Bedingungsbewertung**).</span><span class="sxs-lookup"><span data-stu-id="16277-140">You can also register condition assessment on a work order (**Asset management** > **Common** > **Work orders** > **All Work orders** > **Condition assessment** button.)</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]