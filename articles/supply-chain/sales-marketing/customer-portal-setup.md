---
title: Installieren, einrichten und aktualisieren Sie das Kundenportal
description: Dieses Thema enthält Lizenzdetails und Installationsanweisungen für das Kundenportal.
author: dasani-madipalli
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 5c4cad305e3d130b3283ca3424c84f60e2d13307
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907814"
---
# <a name="install-set-up-and-update-the-customer-portal"></a><span data-ttu-id="3bc15-103">Installieren, einrichten und aktualisieren Sie das Kundenportal</span><span class="sxs-lookup"><span data-stu-id="3bc15-103">Install, set up, and update the Customer portal</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="licensing-requirements"></a><span data-ttu-id="3bc15-104">Lizenzanforderungen</span><span class="sxs-lookup"><span data-stu-id="3bc15-104">Licensing requirements</span></span>

<span data-ttu-id="3bc15-105">Um das Kundenportal zu implementieren, müssen Sie über folgende Lizenzen verfügen:</span><span class="sxs-lookup"><span data-stu-id="3bc15-105">To implement the Customer portal, you must have the following licenses:</span></span>

- <span data-ttu-id="3bc15-106">**Power Apps Portale** – Diese Lizenz ist erforderlich, um das Kundenportal zu hosten.</span><span class="sxs-lookup"><span data-stu-id="3bc15-106">**Power Apps portals** – This license is required to host the Customer portal.</span></span> <span data-ttu-id="3bc15-107">Portale werden je nach Nutzung lizenziert.</span><span class="sxs-lookup"><span data-stu-id="3bc15-107">Portals are licensed based on usage.</span></span> <span data-ttu-id="3bc15-108">Weitere Informationen finden Sie in den [Power Apps Portal Lizenzanforderungen](/power-platform/admin/powerapps-flow-licensing-faq#portals).</span><span class="sxs-lookup"><span data-stu-id="3bc15-108">For more information, see the [Power Apps portals licensing requirements](/power-platform/admin/powerapps-flow-licensing-faq#portals).</span></span>
- <span data-ttu-id="3bc15-109">**Duales Schreiben** – Sie müssen über die erforderlichen Lizenzen verfügen, um duales Schreiben für Supply Chain Management-Tabellen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3bc15-109">**Dual-write** – You must have the necessary licenses to enable dual-write for Supply Chain Management tables.</span></span> <span data-ttu-id="3bc15-110">Weitere Informationen finden Sie unter [Systemanforderungen für duales Schreiben](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).</span><span class="sxs-lookup"><span data-stu-id="3bc15-110">For more information, see the [system requirements for dual-write](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).</span></span>

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a><span data-ttu-id="3bc15-111">Abhängigkeiten von dualem Schreiben und Power Apps Portalen</span><span class="sxs-lookup"><span data-stu-id="3bc15-111">Dependencies on dual-write and Power Apps portals</span></span>

<span data-ttu-id="3bc15-112">Das Kundenportal ist abhängig von Power Apps Portalen und dualem Schreiben, wie in der folgenden Abbildung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="3bc15-112">The Customer portal depends on Power Apps portals and dual-write, as shown in the following illustration.</span></span>

<span data-ttu-id="3bc15-113">![Kundenportalabhängigkeiten](media/customer-portal-elements.png "Kundenportalabhängigkeiten")</span><span class="sxs-lookup"><span data-stu-id="3bc15-113">![Customer portal dependencies](media/customer-portal-elements.png "Customer portal dependencies")</span></span>

<span data-ttu-id="3bc15-114">Im Gegensatz zu anderen Funktionen von Supply Chain Management befindet sich die Kundenportalvorlage in Power Apps Portalen.</span><span class="sxs-lookup"><span data-stu-id="3bc15-114">Unlike other features from Supply Chain Management, the Customer portal template resides in Power Apps portals.</span></span> <span data-ttu-id="3bc15-115">Daher ist das Kundenportal durch die bereitgestellten Funktionen und Fähigkeiten eingeschränkt, die von Power Apps Portalen und Tabellen in dualem Schreiben bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="3bc15-115">Therefore, the Customer portal is limited by the functionality and capabilities that are provided by Power Apps portals and the tables in dual-write.</span></span>

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a><span data-ttu-id="3bc15-116">Erfordert Installation zum Aktivieren des Kundenportals</span><span class="sxs-lookup"><span data-stu-id="3bc15-116">Required setup to enable the Customer portal</span></span>

<span data-ttu-id="3bc15-117">Nachdem Sie sichergestellt haben, dass Sie über die erforderlichen Lizenzen verfügen, können Sie duales Schreiben wie in der Beschreibung beschrieben einrichten [Anweisungen für die anfängliche Synchronisierung mit zwei Schreibvorgängen](/dynamics365/supply-chain/sales-marketing/enable-entity-map).</span><span class="sxs-lookup"><span data-stu-id="3bc15-117">After you've made sure that you have the required licenses, you can set up dual-write as described in the [dual-write initial synchronization instructions](/dynamics365/supply-chain/sales-marketing/enable-entity-map).</span></span>

<span data-ttu-id="3bc15-118">Stellen Sie sicher, dass die folgenden Tabellenzuordnungen in dualem Schreiben aktiviert sind:</span><span class="sxs-lookup"><span data-stu-id="3bc15-118">Be sure to enable the following table mappings in dual-write:</span></span>

- <span data-ttu-id="3bc15-119">Auftragskopf</span><span class="sxs-lookup"><span data-stu-id="3bc15-119">Sales Order Header</span></span>
- <span data-ttu-id="3bc15-120">Auftragsdetails</span><span class="sxs-lookup"><span data-stu-id="3bc15-120">Sales Order Details</span></span>
- <span data-ttu-id="3bc15-121">Konten</span><span class="sxs-lookup"><span data-stu-id="3bc15-121">Accounts</span></span>
- <span data-ttu-id="3bc15-122">Kontakte</span><span class="sxs-lookup"><span data-stu-id="3bc15-122">Contacts</span></span>
- <span data-ttu-id="3bc15-123">Produkte</span><span class="sxs-lookup"><span data-stu-id="3bc15-123">Products</span></span>

<span data-ttu-id="3bc15-124">Nach Abschluss dieser Einrichtung können Sie die Vorlage für das Kundenportal bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="3bc15-124">After this setup is completed, you can provision the Customer portal template.</span></span>

## <a name="provision-the-customer-portal"></a><span data-ttu-id="3bc15-125">Stellen Sie das Kundenportal bereit</span><span class="sxs-lookup"><span data-stu-id="3bc15-125">Provision the Customer portal</span></span>

<span data-ttu-id="3bc15-126">Bevor Sie beginnen, stellen Sie sicher, dass Sie die [erforderliche Einrichtung](#required-setup) bereits abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="3bc15-126">Before you begin, make sure that you've already completed the [required setup](#required-setup).</span></span> <span data-ttu-id="3bc15-127">Führen Sie dann die folgenden Schritte aus, um das Kundenportal bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="3bc15-127">Then follow these steps to provision the Customer portal.</span></span>

1. <span data-ttu-id="3bc15-128">Gehen Sie zu [make.powerapps.com](https://make.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="3bc15-128">Go to [make.powerapps.com](https://make.powerapps.com/).</span></span>
2. <span data-ttu-id="3bc15-129">Stellen Sie sicher, dass Sie die Umgebung verwenden, in der Sie duales Schreiben aktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="3bc15-129">Make sure that you're using the environment where you enabled dual-write.</span></span>
3. <span data-ttu-id="3bc15-130">Auf der Registerkarte **Erstellen** scrollen Sie nach unten zum Abschnitt **Beginnen Sie mit der Vorlage** und wählen Sie die Vorlage aus, die benannt ist **Debitorenportal**.</span><span class="sxs-lookup"><span data-stu-id="3bc15-130">On the **Create** tab, scroll down to the **Start from template** section, and select the template that is named **Customer Portal**.</span></span>
4. <span data-ttu-id="3bc15-131">Befolgen Sie die Anweisungen auf dem Bildschirm.</span><span class="sxs-lookup"><span data-stu-id="3bc15-131">Follow the on-screen instructions.</span></span>

<span data-ttu-id="3bc15-132">Nach Abschluss der Bereitstellung können Sie auf das Kundenportal im Internet zugreifen im Abschnitt **Ihre Apps** auf der Seite **Startseite**.</span><span class="sxs-lookup"><span data-stu-id="3bc15-132">After provisioning is completed, you can access the Customer portal in the **Your apps** section of the **Home** page.</span></span>

> [!NOTE]
> <span data-ttu-id="3bc15-133">Wenn die Lösung duales Schreiben nicht in der Umgebung installiert ist, in der Sie arbeiten, wird eine Fehlermeldung angezeigt und das Kundenportal wird nicht bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="3bc15-133">If the dual-write solution isn't installed in the environment that you're working in, you will receive an error message, and the Customer portal won't be provisioned.</span></span>

## <a name="update-the-customer-portal"></a><span data-ttu-id="3bc15-134">Aktualisieren Sie das Kundenportal</span><span class="sxs-lookup"><span data-stu-id="3bc15-134">Update the Customer portal</span></span>

<span data-ttu-id="3bc15-135">Weitere Funktionen werden möglicherweise später zum Kundenportal hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3bc15-135">More functionality might be added to the Customer portal later.</span></span> <span data-ttu-id="3bc15-136">Alle Änderungen, die Microsoft an den zugrunde liegenden Lösungskomponenten vornimmt, werden automatisch in Ihrer Umgebung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3bc15-136">Any changes that Microsoft makes to the underlying solution components will automatically appear in your environment.</span></span> <span data-ttu-id="3bc15-137">Die in Ihrer Umgebung bereitgestellte Website spiegelt jedoch nicht automatisch Änderungen wider, die an den Konfigurationsdaten vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="3bc15-137">However, the website that is provisioned in your environment won't automatically reflect changes that are made to the configuration data.</span></span> <span data-ttu-id="3bc15-138">Sie müssen diese Änderungen manuell anwenden, indem Sie den Code aus der neuen Vorlage abrufen und mit der bereitgestellten Website zusammenführen.</span><span class="sxs-lookup"><span data-stu-id="3bc15-138">You will have to manually apply those changes by getting the code from the new template and merging it with the provisioned website.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3bc15-139">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3bc15-139">Additional resources</span></span>

<span data-ttu-id="3bc15-140">Um zu erfahren, wie Sie das Kundenportal einrichten und anpassen können, lesen Sie zunächst die folgende Dokumentation zu den zugrunde liegenden Technologien:</span><span class="sxs-lookup"><span data-stu-id="3bc15-140">To learn how you can set up and customize the Customer portal, you should start by reviewing the following documentation for the underlying technologies:</span></span>

- [<span data-ttu-id="3bc15-141">Power Apps Portaldokumentation</span><span class="sxs-lookup"><span data-stu-id="3bc15-141">Power Apps portals documentation</span></span>](/powerapps/maker/portals/overview)
- [<span data-ttu-id="3bc15-142">Dokumentation Duales Schreiben</span><span class="sxs-lookup"><span data-stu-id="3bc15-142">Dual-write documentation</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

<span data-ttu-id="3bc15-143">Um Ihre Portale effektiv verwalten zu können, müssen Sie die Power Apps Portale und Microsoft Dataverse Lifecycle verstehen.</span><span class="sxs-lookup"><span data-stu-id="3bc15-143">To effectively manage your portals, you must understand the Power Apps portals and Microsoft Dataverse lifecycle.</span></span> <span data-ttu-id="3bc15-144">Weitere Informationen finden Sie in den folgenden Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="3bc15-144">For more information, see the following resources:</span></span>

- [<span data-ttu-id="3bc15-145">Informationen zum Portallebenszyklus</span><span class="sxs-lookup"><span data-stu-id="3bc15-145">About portal lifecycle</span></span>](/powerapps/maker/portals/admin/portal-lifecycle)
- [<span data-ttu-id="3bc15-146">Aktualisieren Sie ein Portal</span><span class="sxs-lookup"><span data-stu-id="3bc15-146">Upgrade a portal</span></span>](/powerapps/maker/portals/admin/upgrade-portal)
- [<span data-ttu-id="3bc15-147">Portalkonfiguration migrieren</span><span class="sxs-lookup"><span data-stu-id="3bc15-147">Migrate portal configuration</span></span>](/powerapps/maker/portals/admin/migrate-portal-configuration)
- [<span data-ttu-id="3bc15-148">Solution Lifecycle Management: Dynamics 365 for Customer Engagement Apps</span><span class="sxs-lookup"><span data-stu-id="3bc15-148">Solution Lifecycle Management: Dynamics 365 for Customer Engagement apps</span></span>](https://www.microsoft.com/download/details.aspx?id=57777)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]