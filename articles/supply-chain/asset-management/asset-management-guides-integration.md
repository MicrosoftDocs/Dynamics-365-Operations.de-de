---
title: Integrieren von Dynamics 365 Supply Chain Management (Anlagenverwaltung) in Dynamics 365 Guides
description: In diesem Thema wird erläutert, wie Sie das Anlagenverwaltungsmodul in Microsoft Dynamics 365 Supply Chain Management in Dynamics 365 Guides integrieren, um die Mixed-Reality-Anleitungen in Ihren täglichen Service- und Wartungsworkflows zu nutzen.
author: kamaybac
ms.date: 04/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-28
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 4af14a66c839ccee02008057ad1de8ef5b9d291b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813916"
---
# <a name="integrate-dynamics-365-supply-chain-management-asset-management-with-dynamics-365-guides"></a><span data-ttu-id="e05fa-103">Integrieren von Dynamics 365 Supply Chain Management (Anlagenverwaltung) in Dynamics 365 Guides</span><span class="sxs-lookup"><span data-stu-id="e05fa-103">Integrate Dynamics 365 Supply Chain Management (Asset management) with Dynamics 365 Guides</span></span>

<span data-ttu-id="e05fa-104">Sie können das Modul **Anlageverwaltung** in Microsoft Dynamics 365 Supply Chain Management in Dynamics 365 Guides integrieren, um die Mixed-Reality-Anleitungen in Ihren täglichen Service- und Wartungsworkflows zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="e05fa-104">You can integrate the **Asset management** module in Microsoft Dynamics 365 Supply Chain Management with Dynamics 365 Guides to take advantage of mixed-reality guides in your day-to-day service and maintenance workflows.</span></span> <span data-ttu-id="e05fa-105">Wenn eine Anleitung einem Anlagenverwaltungs-Arbeitsauftrag zugeordnet ist, sieht ein Mitarbeiter, der die Wartungsprüfliste des Arbeitsauftrags in der mobilen Supply Chain Management (Dynamics 365)-App öffnet, dass eine Anleitung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="e05fa-105">If a guide is associated with an Asset Management work order, a worker who opens the work order's maintenance checklist in the Supply Chain Management (Dynamics 365) mobile app sees that a guide is available.</span></span> <span data-ttu-id="e05fa-106">Die Arbeitskraft kann dann die Anleitung in der Dynamics 365 Guides HoloLens-App finden und öffnen.</span><span class="sxs-lookup"><span data-stu-id="e05fa-106">The worker can then find and open the guide in the Dynamics 365 Guides HoloLens app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e05fa-107">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="e05fa-107">Prerequisites</span></span>

<span data-ttu-id="e05fa-108">Bevor Sie Anleitungen an Anlagenverwaltungs-Arbeitsaufträge anhängen können, müssen Sie die folgenden Voraussetzungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="e05fa-108">Before you can attach guides to Asset management work orders, you must complete these prerequisites:</span></span>

- <span data-ttu-id="e05fa-109">[Einrichten von Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) Version 10.0.9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="e05fa-109">[Set up Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) version 10.0.9 or later.</span></span>
- <span data-ttu-id="e05fa-110">[Aktivieren Sie duales Schreiben für Supply Chain Management-Apps](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="e05fa-110">[Turn on dual-write for Supply Chain Management apps](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).</span></span>
- <span data-ttu-id="e05fa-111">[Schalten Sie Flight ein](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) für die Funktion **MRGuidesFeature**.</span><span class="sxs-lookup"><span data-stu-id="e05fa-111">[Turn on flight](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) for the **MRGuidesFeature** feature.</span></span> <span data-ttu-id="e05fa-112">(Für Produktionsumgebungen müssen Sie zuerst ein Support-Ticket übermitteln, damit Ihr Mandant zur Flighting-Gruppe hinzugefügt wird.)</span><span class="sxs-lookup"><span data-stu-id="e05fa-112">(For production environments, you must first submit a support ticket to have your tenant added to the flighting group.)</span></span>
- <span data-ttu-id="e05fa-113">[Aktivieren Sie die folgenden Konfigurationsschlüssel](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) auf der Seite **Lizenzkonfiguration**:</span><span class="sxs-lookup"><span data-stu-id="e05fa-113">[Turn on the following configuration keys](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) on the **License configuration** page:</span></span>

    - <span data-ttu-id="e05fa-114">Anlagenverwaltung \> Anlagenverwaltung – Mixed Reality</span><span class="sxs-lookup"><span data-stu-id="e05fa-114">Asset management \> Asset management mixed reality</span></span>
    - <span data-ttu-id="e05fa-115">Mixed Reality \> Mixed Reality-Anleitung</span><span class="sxs-lookup"><span data-stu-id="e05fa-115">Mixed reality \> Mixed reality guide</span></span>

- <span data-ttu-id="e05fa-116">[Einrichten von Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) Version 200.0.0.96 oder höher.</span><span class="sxs-lookup"><span data-stu-id="e05fa-116">[Set up Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 200.0.0.96 or later.</span></span>

## <a name="use-dynamics-365-guides-with-asset-management"></a><span data-ttu-id="e05fa-117">Verwenden von Dynamics 365 Guides mit Anlagenverwaltung</span><span class="sxs-lookup"><span data-stu-id="e05fa-117">Use Dynamics 365 Guides with Asset management</span></span>

<span data-ttu-id="e05fa-118">Um eine Anleitung zuzuordnen, verwenden Sie eine Wartungsprüflistenposition in der Anlagenverwaltung.</span><span class="sxs-lookup"><span data-stu-id="e05fa-118">To associate a guide, you use a maintenance checklist line in Asset management.</span></span> <span data-ttu-id="e05fa-119">Sie können die Zuordnung über eine Wartungsprüflistenvorlage, einen Wartungsauftragstyp oder einen Arbeitsauftrag erstellen, da alle drei Wartungsprüflistenpositionen enthalten.</span><span class="sxs-lookup"><span data-stu-id="e05fa-119">You can create the association through a maintenance checklist template, a maintenance job type, or a work order, because all three contain maintenance checklist lines.</span></span> <span data-ttu-id="e05fa-120">Sie können Zeit sparen, indem Sie eine Vorlage verwenden, da eine Vorlage allen Wartungsauftragstypen zugeordnet werden kann, die sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="e05fa-120">You can save time by using a template, because a template can be associated with all the maintenance job types that use it.</span></span> <span data-ttu-id="e05fa-121">Beispielsweise wird eine Anleitung, die einem Wartungsauftragstyp zugeordnet ist, automatisch allen Arbeitsaufträgen zugeordnet, die diesen Auftragstyp angeben.</span><span class="sxs-lookup"><span data-stu-id="e05fa-121">For example, a guide that is associated with a maintenance job type is automatically associated with all work orders that specify that job type.</span></span> <span data-ttu-id="e05fa-122">Andererseits existiert eine Anleitung, die direkt einem Arbeitsauftrag zugeordnet ist, nur für diesen Arbeitsauftrag.</span><span class="sxs-lookup"><span data-stu-id="e05fa-122">On the other hand, a guide that is associated directly with a work order exists only for that work order.</span></span>

### <a name="associate-a-guide-with-a-maintenance-checklist-template"></a><span data-ttu-id="e05fa-123">Eine Anleitung einer Wartungsprüflistenvorlage zuordnen</span><span class="sxs-lookup"><span data-stu-id="e05fa-123">Associate a guide with a maintenance checklist template</span></span>

<span data-ttu-id="e05fa-124">Um eine Anleitung einer Wartungsprüflistenvorlage zuzuordnen, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="e05fa-124">To associate a guide with a maintenance checklist template, follow these steps.</span></span>

1. <span data-ttu-id="e05fa-125">Erstellen Sie eine Anleitung mit dem Dynamics 365 Guides-PC und HoloLens-Apps.</span><span class="sxs-lookup"><span data-stu-id="e05fa-125">Create a guide by using the Dynamics 365 Guides PC and HoloLens apps.</span></span> <span data-ttu-id="e05fa-126">Informationen darüber, wie eine Anleitung erstellt wird, finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="e05fa-126">For information about how to create a guide, see the following topics:</span></span>

    - [<span data-ttu-id="e05fa-127">Verwenden der PC-App, um eine Anleitung zu erstellen</span><span class="sxs-lookup"><span data-stu-id="e05fa-127">Use the PC app to create a guide</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/pc-app-overview)
    - [<span data-ttu-id="e05fa-128">Verwenden der HoloLens-App, um Ihre Hologramme zu platzieren</span><span class="sxs-lookup"><span data-stu-id="e05fa-128">Use the HoloLens app to place your holograms</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/hololens-app-overview)

1. <span data-ttu-id="e05fa-129">In Supply Chain Management [erstellen Sie eine Wartungsprüflistenvorlage](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).</span><span class="sxs-lookup"><span data-stu-id="e05fa-129">In Supply Chain Management, [create a maintenance checklist template](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).</span></span>
1. <span data-ttu-id="e05fa-130">Ordnen Sie die Anleitung zu, die Sie mit einer Wartungsprüflistenposition in der neuen Wartungsprüflistenvorlage erstellt haben:</span><span class="sxs-lookup"><span data-stu-id="e05fa-130">Associate the guide that you created with a maintenance checklist line in the new maintenance checklist template:</span></span>

    1. <span data-ttu-id="e05fa-131">Im Inforegister **Wartungsprüflistenpositionen** wählen Sie die Position aus, der Sie die Anleitung zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="e05fa-131">On the **Maintenance checklist lines** FastTab, select the line that you want to associate the guide with.</span></span>
    1. <span data-ttu-id="e05fa-132">Wählen Sie im Inforegister **Zugeordnete Anleitungen** die Option **Anleitung hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="e05fa-132">On the **Associated guides** FastTab, select **Add Guide**.</span></span>

        <span data-ttu-id="e05fa-133">![Eine Anleitung einer Wartungsprüflistenposition zuordnen](media/am-guides-integration-add-guide.png "Eine Anleitung einer Wartungsprüflistenposition zuordnen")</span><span class="sxs-lookup"><span data-stu-id="e05fa-133">![Associate a guide with a maintenance checklist line](media/am-guides-integration-add-guide.png "Associate a guide with a maintenance checklist line")</span></span>

    1. <span data-ttu-id="e05fa-134">Wählen Sie im Feld **Name** eine Anleitung aus, und wählen Sie dann **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="e05fa-134">In the **Name** field, select a guide, and then select **Save**.</span></span>

        <span data-ttu-id="e05fa-135">![Eine Anleitung im Feld „Name“ auswählen](media/am-guides-integration-select-guide.png "Eine Anleitung im Feld „Name“ auswählen")</span><span class="sxs-lookup"><span data-stu-id="e05fa-135">![Select a guide in the Name field](media/am-guides-integration-select-guide.png "Select a guide in the Name field")</span></span>

1. <span data-ttu-id="e05fa-136">Ordnen Sie die Wartungsprüflistenvorlage einem Auftragstyp zu:</span><span class="sxs-lookup"><span data-stu-id="e05fa-136">Associate the maintenance checklist template with a job type:</span></span>

    1. <span data-ttu-id="e05fa-137">[Erstellen Sie einen Wartungsauftragstyp](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type), oder wählen Sie einen vorhandenen Wartungsauftragstyp aus.</span><span class="sxs-lookup"><span data-stu-id="e05fa-137">[Create a maintenance job type](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type), or select an existing maintenance job type.</span></span>
    1. <span data-ttu-id="e05fa-138">Wählen Sie im Aktionsbereich **Standardeinstellungen für den Wartungsauftragstyp** aus.</span><span class="sxs-lookup"><span data-stu-id="e05fa-138">On the Action Pane, select **Maintenance job type defaults**.</span></span>

        <span data-ttu-id="e05fa-139">![Schaltfläche für Wartungsauftragstyp-Standardwerte](media/am-guides-integration-job-defaults.png "Schaltfläche für Wartungsauftragstyp-Standardwerte")</span><span class="sxs-lookup"><span data-stu-id="e05fa-139">![Maintenance job type defaults button](media/am-guides-integration-job-defaults.png "Maintenance job type defaults button")</span></span>

    1. <span data-ttu-id="e05fa-140">Erstellen Sie eine Position, und wählen Sie dann **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="e05fa-140">Create a line, and then select **Save**.</span></span>

        <span data-ttu-id="e05fa-141">![Eine Position erstellen](media/am-guides-integration-add-line.png "Eine Position erstellen")</span><span class="sxs-lookup"><span data-stu-id="e05fa-141">![Create a line](media/am-guides-integration-add-line.png "Create a line")</span></span>

    1. <span data-ttu-id="e05fa-142">Wählen Sie im Aktionsbereich **Wartungsprüfliste** aus.</span><span class="sxs-lookup"><span data-stu-id="e05fa-142">On the Action Pane, select **Maintenance checklist**.</span></span>

        <span data-ttu-id="e05fa-143">![Schaltfläche „Wartungsprüfliste“](media/am-guides-integration-maintenance-checklist.png "Schaltfläche „Wartungsprüfliste“")</span><span class="sxs-lookup"><span data-stu-id="e05fa-143">![Maintenance checklist button](media/am-guides-integration-maintenance-checklist.png "Maintenance checklist button")</span></span>

    1. <span data-ttu-id="e05fa-144">In der Registerkarte **Wartungsprüflistenpositionen** fügen Sie eine Position hinzu, und ändern Sie dann den Wert des Felds **Typ** zu **Vorlage**.</span><span class="sxs-lookup"><span data-stu-id="e05fa-144">On the **Maintenance checklist lines** FastTab, add a line, and then change the value of the **Type** field to **Template**.</span></span>

        <span data-ttu-id="e05fa-145">![Den Wert „Typ“ ändern](media/am-guides-integration-checklist-lines.png "Den Wert „Typ“ ändern")</span><span class="sxs-lookup"><span data-stu-id="e05fa-145">![Change the Type value](media/am-guides-integration-checklist-lines.png "Change the Type value")</span></span>

    1. <span data-ttu-id="e05fa-146">In der Registerkarte **Positionsdetails** im Feld **Vorlage** wählen Sie die Vorlage aus, der Sie die Anleitung zugeordnet haben, und wählen Sie dann **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="e05fa-146">On the **Line details** FastTab, in the **Template** field, select the template that you associated the guide with, and then select **Save**.</span></span>

        <span data-ttu-id="e05fa-147">![Die Vorlage auswählen](media/am-guides-integration-checklist-line-details.png "Die Vorlage auswählen")</span><span class="sxs-lookup"><span data-stu-id="e05fa-147">![Select the template](media/am-guides-integration-checklist-line-details.png "Select the template")</span></span>

1. <span data-ttu-id="e05fa-148">[Erstellen Sie einen Arbeitsauftrag](work-orders/manually-created-workorders.md#create-work-order), und wählen Sie dann den Wartungsauftragstyp aus, der die Wartungsprüflistenvorlage verwendet, der Sie die Anleitung zugeordnet haben.</span><span class="sxs-lookup"><span data-stu-id="e05fa-148">[Create a work order](work-orders/manually-created-workorders.md#create-work-order), and then select the maintenance job type that uses the maintenance checklist template that you associated the guide with.</span></span> <span data-ttu-id="e05fa-149">Die Anleitung wird automatisch dem Arbeitsauftrag zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="e05fa-149">The guide is automatically associated with the work order.</span></span>

    <span data-ttu-id="e05fa-150">![Einen Wartungsauftragstyp auswählen](media/am-guides-integration-create-work-order.png "Einen Wartungsauftragstyp auswählen")</span><span class="sxs-lookup"><span data-stu-id="e05fa-150">![Select a maintenance job type](media/am-guides-integration-create-work-order.png "Select a maintenance job type")</span></span>

1. <span data-ttu-id="e05fa-151">Zeigen Sie die Anleitung an, die dem Arbeitsauftrag und den Arbeitskräften zugeordnet ist:</span><span class="sxs-lookup"><span data-stu-id="e05fa-151">View the guide that is associated with the work order and workers:</span></span>

    1. <span data-ttu-id="e05fa-152">Öffnen Sie den [mobilen Arbeitsbereich „Anlagenverwaltung“](asset-management-mobile-workspace.md), um auf den Arbeitsauftrag zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="e05fa-152">Open the [Asset management mobile workspace](asset-management-mobile-workspace.md) to access the work order.</span></span>
    1. <span data-ttu-id="e05fa-153">[Öffnen Sie die Wartungsprüfliste](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) für den Arbeitsauftrag.</span><span class="sxs-lookup"><span data-stu-id="e05fa-153">[Open the maintenance checklist](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) for the work order.</span></span>
    1. <span data-ttu-id="e05fa-154">Wählen Sie eine Prüflistenposition aus, um die zugeordnete Anleitung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e05fa-154">Select a checklist line to see the associated guide.</span></span>

        <span data-ttu-id="e05fa-155">![Einer Prüflistenposition zugeordnete Anleitung](media/am-guides-integration-show-guide.png "Einer Prüflistenposition zugeordnete Anleitung")</span><span class="sxs-lookup"><span data-stu-id="e05fa-155">![Guide associated with a checklist line](media/am-guides-integration-show-guide.png "Guide associated with a checklist line")</span></span>

    1. <span data-ttu-id="e05fa-156">Öffnen Sie die Anleitung in HoloLens.</span><span class="sxs-lookup"><span data-stu-id="e05fa-156">Open the guide on HoloLens.</span></span>

        <span data-ttu-id="e05fa-157">![Öffnen Sie die Anleitung in HoloLens](media/am-guides-integration-hololens-select.png "Die Anleitung in HoloLens öffnen")</span><span class="sxs-lookup"><span data-stu-id="e05fa-157">![Open the guide on HoloLens](media/am-guides-integration-hololens-select.png "Open the guide on HoloLens")</span></span>

> [!NOTE]
> <span data-ttu-id="e05fa-158">Sie können einen Leitfaden auch direkt in der Wartungsprüfliste eines Arbeitsauftrags oder eines Auftragstyps zuordnen.</span><span class="sxs-lookup"><span data-stu-id="e05fa-158">You can also associate a guide directly in the maintenance checklist of a work order or a job type.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e05fa-159">Es gibt ein bekanntes Problem, bei dem, wenn Sie eine Wartungsprüflistenvorlage einem Standard-Wartungsauftragstyp zuordnen, die Anleitung, die mit der Vorlage verknüpft ist, nicht im Inforegister **Zugeordnete Anleitungen** der Seite **Wartungsauftragstyp-Standardwerte** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e05fa-159">There is a known issue where, when you associate a maintenance checklist template with a default maintenance job type, the guide that is linked to the template doesn't appear on the **Associated guides** FastTab of the **Maintenance job type defaults** page.</span></span> <span data-ttu-id="e05fa-160">Die Anleitung wird jedoch angezeigt, nachdem dieser Auftragstyp auf einen Arbeitsauftrag im Inforegister **Zugehörige Anleitungen** angewendet ist.</span><span class="sxs-lookup"><span data-stu-id="e05fa-160">However, the guide will appear after that job type is applied to a work order on the **Associated guides** FastTab.</span></span>

## <a name="see-also"></a><span data-ttu-id="e05fa-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e05fa-161">See also</span></span>

- [<span data-ttu-id="e05fa-162">Duales Schreiben – Übersicht</span><span class="sxs-lookup"><span data-stu-id="e05fa-162">Dual-write overview</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview.md)
- [<span data-ttu-id="e05fa-163">Überblick über die Anlagenverwaltung</span><span class="sxs-lookup"><span data-stu-id="e05fa-163">Asset management overview</span></span>](index.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]