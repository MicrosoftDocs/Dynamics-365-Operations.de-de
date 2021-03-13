---
title: Verwaltungskomponenten im Add-On zur elektronischen Rechnungsstellung
description: Dieses Thema enthält Informationen zu den Komponenten, die sich auf die Verwaltung des Add-Ons für die elektronische Rechnungsstellung beziehen.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 6f630ebb694217c3bd52378a649933a670c090f2
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104385"
---
# <a name="electronic-invoicing-add-on-administration-components"></a><span data-ttu-id="6225a-103">Verwaltungskomponenten im Add-On zur elektronischen Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="6225a-103">Electronic invoicing add-on administration components</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="6225a-104">Dieses Thema enthält Informationen zu den Komponenten, die sich auf die Verwaltung des Add-Ons für die elektronische Rechnungsstellung beziehen.</span><span class="sxs-lookup"><span data-stu-id="6225a-104">This topic provides information about the components that are related to administration of the Electronic invoicing add-on.</span></span> <span data-ttu-id="6225a-105">Außerdem finden Sie Informationen zum Konfigurieren des Add-On-Diensts für die elektronische Rechnungsstellung.</span><span class="sxs-lookup"><span data-stu-id="6225a-105">It also provides information about how to configure the Electronic invoicing add-on service.</span></span>

## <a name="azure"></a><span data-ttu-id="6225a-106">Azure</span><span class="sxs-lookup"><span data-stu-id="6225a-106">Azure</span></span>

<span data-ttu-id="6225a-107">Verwenden Sie Microsoft Azure, um die Geheimnisse für den Schlüsseltresor und das Speicherkonto zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6225a-107">Use Microsoft Azure to create the secrets for the key vault and storage account.</span></span> <span data-ttu-id="6225a-108">Verwenden Sie dann die Geheimnisse in der Konfiguration des Add-Ons für die elektronische Rechnungsstellung.</span><span class="sxs-lookup"><span data-stu-id="6225a-108">Then use the secrets in the configuration of the Electronic invoicing add-on.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="6225a-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="6225a-109">Lifecycle Services</span></span>

<span data-ttu-id="6225a-110">Verwenden Sie Microsoft Dynamics Lifecycle Services (LCS), um das Add-On für die Microservices für Ihr LCS-Bereitstellungsprojekt zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="6225a-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the add-on for the microservices for your LCS deployment project.</span></span>

<span data-ttu-id="6225a-111">Wählen Sie in LCS die Kachel **Verwaltung von Vorschaufunktionen** aus, und aktivieren Sie anschließend die **E-Invoicing-Dienst**-Funktion.</span><span class="sxs-lookup"><span data-stu-id="6225a-111">In LCS, select the **Preview feature management** tile, and then turn on the **e-Invoicing Service** feature.</span></span>

## <a name="regulatory-configuration-services"></a><span data-ttu-id="6225a-112">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="6225a-112">Regulatory Configuration Services</span></span>

<span data-ttu-id="6225a-113">Dynamics 365 Regulatory Configuration Services (RCS) ist die Schnittstelle für die Konfiguration des Add-Ons für die elektronische Rechnungsstellung.</span><span class="sxs-lookup"><span data-stu-id="6225a-113">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure the Electronic invoicing add-on.</span></span> <span data-ttu-id="6225a-114">Ressourcen wie Umgebungen und Funktionen für die elektronische Rechnungsstellung werden in RCS erstellt, verwaltet und gehostet.</span><span class="sxs-lookup"><span data-stu-id="6225a-114">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="6225a-115">Wenn die Ressourcen bereit sind, werden sie im Add-On-Service für die elektronische Rechnungsstellung veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="6225a-115">When the resources are ready, they are published to the Electronic invoicing add-on service.</span></span>

<span data-ttu-id="6225a-116">Weitere Informationen zu RCS finden Sie unter [Regulatory Configuration Services (RCS) – Globalisierungsfunktionen](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="6225a-116">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="6225a-117">Integration mit dem Add-On für die elektronische Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="6225a-117">Integration with the Electronic invoicing add-on</span></span>

<span data-ttu-id="6225a-118">Bevor Sie RCS zum Konfigurieren elektronischer Rechnungen verwenden können, müssen Sie RCS konfigurieren, um die Kommunikation mit dem Add-On für die elektronische Rechnungsstellung zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="6225a-118">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with the Electronic invoicing add-on.</span></span> <span data-ttu-id="6225a-119">Diese Konfiguration führen Sie auf der Registerkarte **Add-On für die elektronische Rechnungsstellung** der Seite **Parameter für elektronische Berichterstellung** durch.</span><span class="sxs-lookup"><span data-stu-id="6225a-119">You complete this configuration on the **Electronic invoicing add-on** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="6225a-120">Dienstendpunkt</span><span class="sxs-lookup"><span data-stu-id="6225a-120">Service endpoint</span></span>

<span data-ttu-id="6225a-121">Die URL des Add-On-Endpunkts für die elektronische Rechnungsstellung kann je nach Geografie des Azure-Rechenzentrums variieren.</span><span class="sxs-lookup"><span data-stu-id="6225a-121">The URL of the Electronic invoicing add-on endpoint can vary according to the Azure datacenter geography.</span></span> <span data-ttu-id="6225a-122">In der folgenden Tabelle ist die Verfügbarkeit pro Region aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="6225a-122">The following table lists the availability per region:</span></span>

| <span data-ttu-id="6225a-123">Azure-Rechenzentrumgeografie</span><span class="sxs-lookup"><span data-stu-id="6225a-123">Azure datacenter geography</span></span> | <span data-ttu-id="6225a-124">Dienstendpunkt-URL</span><span class="sxs-lookup"><span data-stu-id="6225a-124">Service endpoint URL</span></span>                                                       |
|----------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="6225a-125">USA, Osten</span><span class="sxs-lookup"><span data-stu-id="6225a-125">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="6225a-126">USA, Westen</span><span class="sxs-lookup"><span data-stu-id="6225a-126">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="6225a-127">Norden, Europa</span><span class="sxs-lookup"><span data-stu-id="6225a-127">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="6225a-128">Westen, Europa</span><span class="sxs-lookup"><span data-stu-id="6225a-128">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

#### <a name="application-id"></a><span data-ttu-id="6225a-129">Anwendungs-ID</span><span class="sxs-lookup"><span data-stu-id="6225a-129">Application ID</span></span>

<span data-ttu-id="6225a-130">Die Anwendungs-ID ist die ID der Add-On-Anwendung für die elektronische Rechnungsstellung.</span><span class="sxs-lookup"><span data-stu-id="6225a-130">The application ID is the ID of the Electronic invoicing add-on application.</span></span> <span data-ttu-id="6225a-131">In diesem Fall ist der Wert festgelegt: **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="6225a-131">In this case, the value is fixed: **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

#### <a name="lcs-environment-id"></a><span data-ttu-id="6225a-132">LCS-Umgebungs-ID</span><span class="sxs-lookup"><span data-stu-id="6225a-132">LCS environment ID</span></span>

<span data-ttu-id="6225a-133">Die LCS-Umgebungs-ID ist die ID des LCS-Abonnements Ihrer Organisation.</span><span class="sxs-lookup"><span data-stu-id="6225a-133">The LCS environment ID is the ID of your organization's LCS subscription.</span></span>

### <a name="service-environments"></a><span data-ttu-id="6225a-134">Dienstumgebungen</span><span class="sxs-lookup"><span data-stu-id="6225a-134">Service environments</span></span>

<span data-ttu-id="6225a-135">Service-Umgebungen sind logische Partitionen, die erstellt werden, um die Ausführung der Funktionen für die elektronische Rechnungsstellung im zugehörigen Add-On zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6225a-135">Service environments are logical partitions that are created to support execution of the electronic invoicing features in the Electronic invoicing add-on.</span></span> <span data-ttu-id="6225a-136">Die Sicherheitsgeheimnisse und digitalen Zertifikate sowie die Governance (d. h. Zugriffsberechtigungen) müssen auf der Ebene der Service-Umgebung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="6225a-136">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="6225a-137">Kunden können beliebig viele Service-Umgebungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="6225a-137">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="6225a-138">Alle von einem Kunden erstellten Service-Umgebungen sind voneinander unabhängig.</span><span class="sxs-lookup"><span data-stu-id="6225a-138">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="6225a-139">Service-Umgebungen müssen in RCS erstellt und verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="6225a-139">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="6225a-140">Wenn die Service-Umgebungen bereit sind, müssen sie im Add-On für die elektronische Rechnungsstellung veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="6225a-140">When the service environments are ready, they must be published to the Electronic invoicing add-on.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="6225a-141">Status der Service-Umgebung</span><span class="sxs-lookup"><span data-stu-id="6225a-141">Service environment status</span></span>

<span data-ttu-id="6225a-142">Service-Umgebungen können über den Status verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="6225a-142">Service environments can be managed through status.</span></span> <span data-ttu-id="6225a-143">Mögliche Optionen sind:</span><span class="sxs-lookup"><span data-stu-id="6225a-143">The possible options are:</span></span>

- <span data-ttu-id="6225a-144">**Nicht veröffentlicht** – Die Umgebung wurde erstellt, aber noch nicht veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="6225a-144">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="6225a-145">**Veröffentlicht** – Die Umgebung wurde im Add-On für die elektronische Rechnungsstellung veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="6225a-145">**Published** – The environment has been published to the Electronic invoicing add-on.</span></span>
- <span data-ttu-id="6225a-146">**Geändert** – Die Attribute einer veröffentlichten Umgebung wurden geändert, die Änderungen wurden jedoch noch nicht veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="6225a-146">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="6225a-147">Kundengeheimnisse</span><span class="sxs-lookup"><span data-stu-id="6225a-147">Customer secrets</span></span>

<span data-ttu-id="6225a-148">Der Add-On-Dienst für die elektronische Rechnungsstellung ist verantwortlich für die Speicherung aller Ihrer Geschäftsdaten in den Azure-Ressourcen, die Ihrem Unternehmen gehören.</span><span class="sxs-lookup"><span data-stu-id="6225a-148">The Electronic invoicing add-on service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="6225a-149">Um sicherzustellen, dass der Dienst ordnungsgemäß funktioniert und auf alle Geschäftsdaten, die für das Add-On für die elektronische Rechnungsstellung erforderlich sind und von ihm generiert werden, nur über das Add-On zugegriffen wird, müssen Sie zwei Azure-Hauptressourcen erstellen:</span><span class="sxs-lookup"><span data-stu-id="6225a-149">To ensure that the service works correctly, and that all the business data that is required for and generated by the Electronic invoicing add-on is accessed only by the add-on, you must create two main Azure resources:</span></span>

- <span data-ttu-id="6225a-150">ein Azure-Speicherkonto (Blob-Speicher) zum Speichern elektronischer Rechnungen</span><span class="sxs-lookup"><span data-stu-id="6225a-150">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="6225a-151">einen Azure-Schlüsseltresor zum Speichern von Zertifikaten und des URI (Uniform Resource Identifier) des Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="6225a-151">An Azure key vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>

> [!NOTE]
> <span data-ttu-id="6225a-152">Ein dedizierter Schlüsseltresor und ein Speicherkonto für den Kunden müssen speziell für die Verwendung mit dem Add-On für die elektronische Rechnungsstellung zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="6225a-152">A dedicated key vault and customer storage account must be allocated specifically for use with the Electronic invoicing add-on.</span></span>

<span data-ttu-id="6225a-153">Weitere Informationen finden Sie unter [Ein Azure-Speicherkonto und einen Schlüsseltresor erstellen](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="6225a-153">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

#### <a name="users"></a><span data-ttu-id="6225a-154">Benutzer</span><span class="sxs-lookup"><span data-stu-id="6225a-154">Users</span></span>

<span data-ttu-id="6225a-155">Jede Service-Umgebung muss die Benutzer auflisten, die aus Dynamics 365 Finance und Dynamics 365 Supply Chain Management im Add-On für die elektronische Rechnungsstellung eine Verbindung herstellen können.</span><span class="sxs-lookup"><span data-stu-id="6225a-155">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in the Electronic invoicing add-on.</span></span>

#### <a name="publication"></a><span data-ttu-id="6225a-156">Veröffentlichung</span><span class="sxs-lookup"><span data-stu-id="6225a-156">Publication</span></span>

<span data-ttu-id="6225a-157">Service-Umgebungen müssen im Add-On für die elektronische Rechnungsstellung veröffentlicht werden, bevor sie genutzt werden können.</span><span class="sxs-lookup"><span data-stu-id="6225a-157">Service environments must be published to the Electronic invoicing add-on before they can be used.</span></span> <span data-ttu-id="6225a-158">Finance und Supply Chain Management können nur auf veröffentlichte Umgebungen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="6225a-158">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="6225a-159">Darüber hinaus muss eine Service-Umgebung veröffentlicht werden, bevor Aktualisierungen ihrer Attribute für den elektronischen Rechnungsstellungsdienst in Kraft treten.</span><span class="sxs-lookup"><span data-stu-id="6225a-159">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="6225a-160">Verbundene Anwendungen</span><span class="sxs-lookup"><span data-stu-id="6225a-160">Connected applications</span></span>

<span data-ttu-id="6225a-161">Verbundene Anwendungen sind die Instanzen von Finance und Supply Chain Management, die Sie möglicherweise über RCS erreichen möchten.</span><span class="sxs-lookup"><span data-stu-id="6225a-161">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="6225a-162">Neben der Anwendungs-URL und ihrem Mandanten enthält eine verbundene Anwendung die Anmeldeinformationen, mit denen RCS eine Verbindung zur Umgebung herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="6225a-162">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="6225a-163">Über die verbundenen Anwendungen können Sie einen Teil der Funktion für die elektronische Rechnungsstellung in Finance und Supply Chain Management so konfigurieren, dass die gesamte Funktion für die elektronische Rechnungsstellung funktioniert.</span><span class="sxs-lookup"><span data-stu-id="6225a-163">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="6225a-164">Finance und Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="6225a-164">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing-add-on"></a><span data-ttu-id="6225a-165">Integration mit dem Add-On für die elektronische Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="6225a-165">Integration with Electronic invoicing add-on</span></span>

<span data-ttu-id="6225a-166">Bevor Sie mit Finance und Supply Chain Management elektronische Rechnungen über das Add-On für die elektronische Rechnungsstellung ausstellen können, muss das Add-On so konfiguriert sein, dass die Kommunikation mit dem Dienst möglich ist.</span><span class="sxs-lookup"><span data-stu-id="6225a-166">Before you can use Finance and Supply Chain Management to issue electronic invoices through the Electronic invoicing add-on, the add-on must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="6225a-167">Add-On-Integrationsfunktion für die elektronische Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="6225a-167">Electronic invoicing add-on integration feature</span></span>

<span data-ttu-id="6225a-168">Um die Kommunikation zwischen Finance und Supply Chain Management sowie dem Add-On für die elektronische Rechnungsstellung zu ermöglichen, müssen Sie die Funktion **Add-On-Integration für die elektronische Rechnungsstellung** im Arbeitsbereich **Funktionsverwaltung** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="6225a-168">To enable communication between Finance and Supply Chain Management and the Electronic invoicing add-on, you must turn on the **Electronic Invoicing add-on integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="6225a-169">Dienstendpunkt</span><span class="sxs-lookup"><span data-stu-id="6225a-169">Service endpoint</span></span>

<span data-ttu-id="6225a-170">Der Service-Endpunkt ist die URL, unter der sich das Add-On für die elektronische Rechnungsstellung befindet.</span><span class="sxs-lookup"><span data-stu-id="6225a-170">The service endpoint is the URL where the Electronic invoicing add-on is located.</span></span> <span data-ttu-id="6225a-171">Bevor elektronische Rechnungen ausgestellt werden können, muss der Dienstendpunkt in Finance und Supply Chain Management konfiguriert werden, um die Kommunikation mit dem Dienst zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="6225a-171">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="6225a-172">Rufen Sie **Organisationsverwaltung \> Einrichtung \> Parameter elektronischer Dokumente** auf, um den Dienstendpunkt zu konfigurieren. Geben Sie anschließend auf der Registerkarte **Übermittlungsdienste** im Feld **Add-On-URL für die elektronische Rechnungsstellung** die URL ein – wie in der Tabelle im Abschnitt **Dienstendpunkt** beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6225a-172">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing add-on URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="6225a-173">Umgebungen</span><span class="sxs-lookup"><span data-stu-id="6225a-173">Environments</span></span>

<span data-ttu-id="6225a-174">Der Umgebungsname, der in Finance und Supply Chain Management eingegeben wird, bezieht sich auf den Namen der Umgebung, die in RCS erstellt und im Add-On für die elektronische Rechnungsstellung veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="6225a-174">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to the Electronic invoicing add-on.</span></span>

<span data-ttu-id="6225a-175">Die Umgebung muss auf der Registerkarte **Übermittlungsdienste** der Seite **Parameter elektronischer Dokumente** konfiguriert werden, sodass jede Anfrage zur Ausstellung elektronischer Rechnungen die Umgebung enthält, in der das Add-On für die elektronische Rechnungsstellung bestimmen kann, welche elektronische Rechnungsfunktion die Anfrage verarbeiten muss.</span><span class="sxs-lookup"><span data-stu-id="6225a-175">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where the Electronic invoicing add-on can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6225a-176">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6225a-176">Additional resources</span></span>

- [<span data-ttu-id="6225a-177">Elektronische Rechnungen in RCS konfigurieren</span><span class="sxs-lookup"><span data-stu-id="6225a-177">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="6225a-178">Elektronische Rechnungen in Finance und Supply Chain Management ausstellen</span><span class="sxs-lookup"><span data-stu-id="6225a-178">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)
