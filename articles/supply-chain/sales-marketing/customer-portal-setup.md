---
title: Installieren, einrichten und aktualisieren Sie das Kundenportal
description: Dieses Thema enthält Lizenzdetails und Installationsanweisungen für das Kundenportal.
author: dasani-madipalli
manager: tfehr
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: b9d1e742f78254d949dc49fda008d63b8bff4d65
ms.sourcegitcommit: 713b5dfc76a6875d0ba6d86c5cbd585ea502cf9d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/01/2020
ms.locfileid: "3413966"
---
# <a name="install-set-up-and-update-the-customer-portal"></a><span data-ttu-id="63fb1-103">Installieren, einrichten und aktualisieren Sie das Kundenportal</span><span class="sxs-lookup"><span data-stu-id="63fb1-103">Install, set up, and update the Customer portal</span></span>

## <a name="licensing-requirements"></a><span data-ttu-id="63fb1-104">Lizenzanforderungen</span><span class="sxs-lookup"><span data-stu-id="63fb1-104">Licensing requirements</span></span>

<span data-ttu-id="63fb1-105">Um das Kundenportal zu implementieren, müssen Sie über folgende Lizenzen verfügen:</span><span class="sxs-lookup"><span data-stu-id="63fb1-105">To implement the Customer portal, you must have the following licenses:</span></span>

- <span data-ttu-id="63fb1-106">**Power Apps Portale** – Diese Lizenz ist erforderlich, um das Kundenportal zu hosten.</span><span class="sxs-lookup"><span data-stu-id="63fb1-106">**Power Apps portals** – This license is required to host the Customer portal.</span></span> <span data-ttu-id="63fb1-107">Portale werden je nach Nutzung lizenziert.</span><span class="sxs-lookup"><span data-stu-id="63fb1-107">Portals are licensed based on usage.</span></span> <span data-ttu-id="63fb1-108">Weitere Informationen finden Sie in den [Power Apps Portal Lizenzanforderungen](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).</span><span class="sxs-lookup"><span data-stu-id="63fb1-108">For more information, see the [Power Apps portals licensing requirements](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).</span></span>
- <span data-ttu-id="63fb1-109">**Duales Schreiben** – Sie müssen über die erforderlichen Lizenzen verfügen, um duales Schreiben für Supply Chain Management-Entitäten zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="63fb1-109">**Dual-write** – You must have the necessary licenses to enable dual-write for Supply Chain Management entities.</span></span> <span data-ttu-id="63fb1-110">Weitere Informationen finden Sie unter [Systemanforderungen für duales Schreiben](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).</span><span class="sxs-lookup"><span data-stu-id="63fb1-110">For more information, see the [system requirements for dual-write](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).</span></span>

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a><span data-ttu-id="63fb1-111">Abhängigkeiten von dualem Schreiben und Power Apps Portalen</span><span class="sxs-lookup"><span data-stu-id="63fb1-111">Dependencies on dual-write and Power Apps portals</span></span>

<span data-ttu-id="63fb1-112">Das Kundenportal ist abhängig von Power Apps Portalen und dualem Schreiben, wie in der folgenden Abbildung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="63fb1-112">The Customer portal depends on Power Apps portals and dual-write, as shown in the following illustration.</span></span>

![![Kundenportalabhängigkeiten](media/customer-portal-elements.png "Kundenportalabhängigkeiten")](media/customer-portal-elements.png "Customer portal dependencies")

<span data-ttu-id="63fb1-114">Im Gegensatz zu anderen Funktionen von Supply Chain Management befindet sich die Kundenportalvorlage in Power Apps Portalen.</span><span class="sxs-lookup"><span data-stu-id="63fb1-114">Unlike other features from Supply Chain Management, the Customer portal template resides in Power Apps portals.</span></span> <span data-ttu-id="63fb1-115">Daher ist das Kundenportal durch die bereitgestellten Funktionen und Fähigkeiten eingeschränkt, die von Power Apps Portalen und die Entitäten in dualem Schreiben bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="63fb1-115">Therefore, the Customer portal is limited by the functionality and capabilities that are provided by Power Apps portals and the entities in dual-write.</span></span>

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a><span data-ttu-id="63fb1-116">Erfordert Installation zum Aktivieren des Kundenportals</span><span class="sxs-lookup"><span data-stu-id="63fb1-116">Required setup to enable the Customer portal</span></span>

<span data-ttu-id="63fb1-117">Nachdem Sie sichergestellt haben, dass Sie über die erforderlichen Lizenzen verfügen, können Sie duales Schreiben wie in der Beschreibung beschrieben einrichten [Anweisungen für die anfängliche Synchronisierung mit zwei Schreibvorgängen](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).</span><span class="sxs-lookup"><span data-stu-id="63fb1-117">After you've made sure that you have the required licenses, you can set up dual-write as described in the [dual-write initial synchronization instructions](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).</span></span>

<span data-ttu-id="63fb1-118">Stellen Sie sicher, dass die folgenden Entitätszuordnungen in dualem Schreiben aktiviert sind:</span><span class="sxs-lookup"><span data-stu-id="63fb1-118">Be sure to enable the following entity mappings in dual-write:</span></span>

- <span data-ttu-id="63fb1-119">Auftragskopf</span><span class="sxs-lookup"><span data-stu-id="63fb1-119">Sales Order Header</span></span>
- <span data-ttu-id="63fb1-120">Auftragsdetails</span><span class="sxs-lookup"><span data-stu-id="63fb1-120">Sales Order Details</span></span>
- <span data-ttu-id="63fb1-121">Konten</span><span class="sxs-lookup"><span data-stu-id="63fb1-121">Accounts</span></span>
- <span data-ttu-id="63fb1-122">Kontakte</span><span class="sxs-lookup"><span data-stu-id="63fb1-122">Contacts</span></span>
- <span data-ttu-id="63fb1-123">Produkte</span><span class="sxs-lookup"><span data-stu-id="63fb1-123">Products</span></span>

<span data-ttu-id="63fb1-124">Nach Abschluss dieser Einrichtung können Sie die Vorlage für das Kundenportal bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="63fb1-124">After this setup is completed, you can provision the Customer portal template.</span></span>

## <a name="provision-the-customer-portal"></a><span data-ttu-id="63fb1-125">Stellen Sie das Kundenportal bereit</span><span class="sxs-lookup"><span data-stu-id="63fb1-125">Provision the Customer portal</span></span>

<span data-ttu-id="63fb1-126">Bevor Sie beginnen, stellen Sie sicher, dass Sie die [erforderliche Einrichtung](#required-setup) bereits abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="63fb1-126">Before you begin, make sure that you've already completed the [required setup](#required-setup).</span></span> <span data-ttu-id="63fb1-127">Führen Sie dann die folgenden Schritte aus, um das Kundenportal bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="63fb1-127">Then follow these steps to provision the Customer portal.</span></span>

1. <span data-ttu-id="63fb1-128">Gehen Sie zu [make.powerapps.com](https://make.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="63fb1-128">Go to [make.powerapps.com](https://make.powerapps.com/).</span></span>
2. <span data-ttu-id="63fb1-129">Stellen Sie sicher, dass Sie die Umgebung verwenden, in der Sie duales Schreiben aktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="63fb1-129">Make sure that you're using the environment where you enabled dual-write.</span></span>
3. <span data-ttu-id="63fb1-130">Auf der Registerkarte **Erstellen** scrollen Sie nach unten zum Abschnitt **Beginnen Sie mit der Vorlage** und wählen Sie die Vorlage aus, die benannt ist **Supply Chain Management Kunde**.</span><span class="sxs-lookup"><span data-stu-id="63fb1-130">On the **Create** tab, scroll down to the **Start from template** section, and select the template that is named **Supply Chain Management Customer**.</span></span>
4. <span data-ttu-id="63fb1-131">Befolgen Sie die Anweisungen auf dem Bildschirm.</span><span class="sxs-lookup"><span data-stu-id="63fb1-131">Follow the on-screen instructions.</span></span>

<span data-ttu-id="63fb1-132">Nach Abschluss der Bereitstellung können Sie auf das Kundenportal im Internet zugreifen im Abschnitt **Ihre Apps** auf der Seite **Startseite**.</span><span class="sxs-lookup"><span data-stu-id="63fb1-132">After provisioning is completed, you can access the Customer portal in the **Your apps** section of the **Home** page.</span></span>

> [!NOTE]
> <span data-ttu-id="63fb1-133">Wenn die Lösung duales Schreiben nicht in der Umgebung installiert ist, in der Sie arbeiten, wird eine Fehlermeldung angezeigt und das Kundenportal wird nicht bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="63fb1-133">If the dual-write solution isn't installed in the environment that you're working in, you will receive an error message, and the Customer portal won't be provisioned.</span></span>

## <a name="update-the-customer-portal"></a><span data-ttu-id="63fb1-134">Aktualisieren Sie das Kundenportal</span><span class="sxs-lookup"><span data-stu-id="63fb1-134">Update the Customer portal</span></span>

<span data-ttu-id="63fb1-135">Weitere Funktionen werden möglicherweise später zum Kundenportal hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="63fb1-135">More functionality might be added to the Customer portal later.</span></span> <span data-ttu-id="63fb1-136">Alle Änderungen, die Microsoft an den zugrunde liegenden Lösungskomponenten vornimmt, werden automatisch in Ihrer Umgebung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="63fb1-136">Any changes that Microsoft makes to the underlying solution components will automatically appear in your environment.</span></span> <span data-ttu-id="63fb1-137">Die in Ihrer Umgebung bereitgestellte Website spiegelt jedoch nicht automatisch Änderungen wider, die an den Konfigurationsdaten vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="63fb1-137">However, the website that is provisioned in your environment won't automatically reflect changes that are made to the configuration data.</span></span> <span data-ttu-id="63fb1-138">Sie müssen diese Änderungen manuell anwenden, indem Sie den Code aus der neuen Vorlage abrufen und mit der bereitgestellten Website zusammenführen.</span><span class="sxs-lookup"><span data-stu-id="63fb1-138">You will have to manually apply those changes by getting the code from the new template and merging it with the provisioned website.</span></span>

## <a name="resources"></a><span data-ttu-id="63fb1-139">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="63fb1-139">Resources</span></span>

<span data-ttu-id="63fb1-140">Um zu erfahren, wie Sie das Kundenportal einrichten und anpassen können, lesen Sie zunächst die folgende Dokumentation zu den zugrunde liegenden Technologien:</span><span class="sxs-lookup"><span data-stu-id="63fb1-140">To learn how you can set up and customize the Customer portal, you should start by reviewing the following documentation for the underlying technologies:</span></span>

- [<span data-ttu-id="63fb1-141">Power Apps Portaldokumentation</span><span class="sxs-lookup"><span data-stu-id="63fb1-141">Power Apps portals documentation</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [<span data-ttu-id="63fb1-142">Dokumentation Duales Schreiben</span><span class="sxs-lookup"><span data-stu-id="63fb1-142">Dual-write documentation</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

<span data-ttu-id="63fb1-143">Um Ihre Portale effektiv verwalten zu können, müssen Sie die Power Apps Portale und Common Data Service Lifecycle verstehen.</span><span class="sxs-lookup"><span data-stu-id="63fb1-143">To effectively manage your portals, you must understand the Power Apps portals and Common Data Service lifecycle.</span></span> <span data-ttu-id="63fb1-144">Weitere Informationen finden Sie in den folgenden Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="63fb1-144">For more information, see the following resources:</span></span>

- [<span data-ttu-id="63fb1-145">Informationen zum Portallebenszyklus</span><span class="sxs-lookup"><span data-stu-id="63fb1-145">About portal lifecycle</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [<span data-ttu-id="63fb1-146">Aktualisieren Sie ein Portal</span><span class="sxs-lookup"><span data-stu-id="63fb1-146">Upgrade a portal</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [<span data-ttu-id="63fb1-147">Portalkonfiguration migrieren</span><span class="sxs-lookup"><span data-stu-id="63fb1-147">Migrate portal configuration</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [<span data-ttu-id="63fb1-148">Solution Lifecycle Management: Dynamics 365 for Customer Engagement Apps</span><span class="sxs-lookup"><span data-stu-id="63fb1-148">Solution Lifecycle Management: Dynamics 365 for Customer Engagement apps</span></span>](https://www.microsoft.com/download/details.aspx?id=57777)
