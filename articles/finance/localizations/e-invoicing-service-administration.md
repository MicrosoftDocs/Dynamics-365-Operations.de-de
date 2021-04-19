---
title: Verwaltungskomponenten der elektronischen Rechnungsstellung
description: Dieses Thema enthält Informationen zu den Komponenten, die sich auf die Verwaltung der elektronischen Rechnungsstellung beziehen.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 2e859875e124796e49000cd5ea94cfb75ecd768a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840027"
---
# <a name="electronic-invoicing-administration-components"></a><span data-ttu-id="9be35-103">Verwaltungskomponenten der elektronischen Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="9be35-103">Electronic invoicing administration components</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="9be35-104">Dieses Thema enthält Informationen zu den Komponenten, die sich auf die Verwaltung der elektronischen Rechnungsstellung beziehen.</span><span class="sxs-lookup"><span data-stu-id="9be35-104">This topic provides information about the components that are related to administration of Electronic invoicing.</span></span> <span data-ttu-id="9be35-105">Außerdem finden Sie Informationen zum Konfigurieren der elektronischen Rechnungsstellung.</span><span class="sxs-lookup"><span data-stu-id="9be35-105">It also provides information about how to configure the Electronic invoicing service.</span></span>

## <a name="azure"></a><span data-ttu-id="9be35-106">Azure</span><span class="sxs-lookup"><span data-stu-id="9be35-106">Azure</span></span>

<span data-ttu-id="9be35-107">Verwenden Sie Microsoft Azure, um die Geheimnisse für den Schlüsseltresor und das Speicherkonto zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9be35-107">Use Microsoft Azure to create the secrets for the key vault and storage account.</span></span> <span data-ttu-id="9be35-108">Verwenden Sie dann die Geheimnisse in der Konfiguration der elektronischen Rechnungsstellung.</span><span class="sxs-lookup"><span data-stu-id="9be35-108">Then use the secrets in the configuration of Electronic invoicing.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="9be35-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="9be35-109">Lifecycle Services</span></span>

<span data-ttu-id="9be35-110">Verwenden Sie Microsoft Dynamics Lifecycle Services (LCS), um die Microservices für Ihr LCS-Bereitstellungsprojekt zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="9be35-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the microservices for your LCS deployment project.</span></span>

> [!NOTE]
> <span data-ttu-id="9be35-111">Für die Installation des Microservices in LCS ist mindestens ein virtueller Tier 2-Computer erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9be35-111">The installation of the microservice in LCS requires at least a Tier 2 virtual machine.</span></span> <span data-ttu-id="9be35-112">Weitere Informationen zur Umgebungsplanung finden Sie unter [Umgebungsplanung](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="9be35-112">For more information about environment planning, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
 

## <a name="regulatory-configuration-services"></a><span data-ttu-id="9be35-113">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="9be35-113">Regulatory Configuration Services</span></span>

<span data-ttu-id="9be35-114">Dynamics 365 Regulatory Configuration Services (RCS) ist die Schnittstelle für die Konfiguration der elektronischen Rechnungsstellung.</span><span class="sxs-lookup"><span data-stu-id="9be35-114">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure Electronic invoicing.</span></span> <span data-ttu-id="9be35-115">Ressourcen wie Umgebungen und Funktionen für die elektronische Rechnungsstellung werden in RCS erstellt, verwaltet und gehostet.</span><span class="sxs-lookup"><span data-stu-id="9be35-115">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="9be35-116">Wenn die Ressourcen bereit sind, werden sie in der elektronischen Rechnungsstellung veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="9be35-116">When the resources are ready, they are published to Electronic invoicing service.</span></span>

<span data-ttu-id="9be35-117">Informationen zur RCS-Anmeldung finden Sie unter [Regulatory services](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="9be35-117">For RCS sign-up, see [Regulatory services](https://marketing.configure.global.dynamics.com/).</span></span>

<span data-ttu-id="9be35-118">Weitere Informationen zu RCS finden Sie unter [Regulatory Configuration Services (RCS) – Globalisierungsfunktionen](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="9be35-118">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="9be35-119">Integration in die elektronische Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="9be35-119">Integration with Electronic invoicing</span></span> 

<span data-ttu-id="9be35-120">Bevor Sie RCS zum Konfigurieren elektronischer Rechnungen verwenden können, müssen Sie RCS konfigurieren, um die Kommunikation mit der elektronischen Rechnungsstellung zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="9be35-120">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with Electronic invoicing.</span></span> <span data-ttu-id="9be35-121">Diese Konfiguration führen Sie auf der Registerkarte **Elektronische Rechnungsstellung** der Seite **Parameter für elektronische Berichterstellung** durch.</span><span class="sxs-lookup"><span data-stu-id="9be35-121">You complete this configuration on the **Electronic invoicing** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="9be35-122">Dienstendpunkt</span><span class="sxs-lookup"><span data-stu-id="9be35-122">Service endpoint</span></span>

<span data-ttu-id="9be35-123">Die elektronische Rechnungsstellung ist in mehreren Azure-Rechenzentrumsregionen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9be35-123">Electronic invoicing is available in several Azure datacenter geographies.</span></span> <span data-ttu-id="9be35-124">In der folgenden Tabelle ist die Verfügbarkeit pro Region aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="9be35-124">The following table lists the availability per region.</span></span>

| <span data-ttu-id="9be35-125">Azure-Rechenzentrumgeografie</span><span class="sxs-lookup"><span data-stu-id="9be35-125">Azure datacenter geography</span></span> |
|----------------------------|
| <span data-ttu-id="9be35-126">USA, Osten</span><span class="sxs-lookup"><span data-stu-id="9be35-126">East US</span></span>                    |
| <span data-ttu-id="9be35-127">USA, Westen</span><span class="sxs-lookup"><span data-stu-id="9be35-127">West US</span></span>                    |
| <span data-ttu-id="9be35-128">Norden, Europa</span><span class="sxs-lookup"><span data-stu-id="9be35-128">North EU</span></span>                   |
| <span data-ttu-id="9be35-129">Westen, Europa</span><span class="sxs-lookup"><span data-stu-id="9be35-129">West EU</span></span>                    |

### <a name="service-environments"></a><span data-ttu-id="9be35-130">Dienstumgebungen</span><span class="sxs-lookup"><span data-stu-id="9be35-130">Service environments</span></span>

<span data-ttu-id="9be35-131">Service-Umgebungen sind logische Partitionen, die erstellt werden, um die Ausführung der Funktionen für die elektronische Rechnungsstellung in der elektronischen Rechnungsstellung zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9be35-131">Service environments are logical partitions that are created to support execution of the electronic invoicing features in Electronic invoicing.</span></span> <span data-ttu-id="9be35-132">Die Sicherheitsgeheimnisse und digitalen Zertifikate sowie die Governance (d. h. Zugriffsberechtigungen) müssen auf der Ebene der Service-Umgebung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="9be35-132">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="9be35-133">Kunden können beliebig viele Service-Umgebungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="9be35-133">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="9be35-134">Alle von einem Kunden erstellten Service-Umgebungen sind voneinander unabhängig.</span><span class="sxs-lookup"><span data-stu-id="9be35-134">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="9be35-135">Service-Umgebungen müssen in RCS erstellt und verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="9be35-135">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="9be35-136">Wenn die Service-Umgebungen bereit sind, müssen sie in der elektronischen Rechnungsstellung veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="9be35-136">When the service environments are ready, they must be published to Electronic invoicing.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="9be35-137">Status der Service-Umgebung</span><span class="sxs-lookup"><span data-stu-id="9be35-137">Service environment status</span></span>

<span data-ttu-id="9be35-138">Service-Umgebungen können über den Status verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="9be35-138">Service environments can be managed through status.</span></span> <span data-ttu-id="9be35-139">Mögliche Optionen sind:</span><span class="sxs-lookup"><span data-stu-id="9be35-139">The possible options are:</span></span>

- <span data-ttu-id="9be35-140">**Nicht veröffentlicht** – Die Umgebung wurde erstellt, aber noch nicht veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="9be35-140">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="9be35-141">**Veröffentlicht** – Die Umgebung wurde in der elektronischen Rechnungsstellung veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="9be35-141">**Published** – The environment has been published to Electronic invoicing .</span></span>
- <span data-ttu-id="9be35-142">**Geändert** – Die Attribute einer veröffentlichten Umgebung wurden geändert, die Änderungen wurden jedoch noch nicht veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="9be35-142">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="9be35-143">Kundengeheimnisse</span><span class="sxs-lookup"><span data-stu-id="9be35-143">Customer secrets</span></span>

<span data-ttu-id="9be35-144">Der Dienst für die elektronische Rechnungsstellung ist verantwortlich für die Speicherung aller Ihrer Geschäftsdaten in den Azure-Ressourcen, die Ihrem Unternehmen gehören.</span><span class="sxs-lookup"><span data-stu-id="9be35-144">The Electronic invoicing service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="9be35-145">Um sicherzustellen, dass der Service ordnungsgemäß funktioniert und auf alle Geschäftsdaten, die für die elektronische Rechnungsstellung erforderlich sind und von ihr generiert werden, ordnungsgemäß zugegriffen wird, müssen Sie zwei Azure-Hauptressourcen erstellen:</span><span class="sxs-lookup"><span data-stu-id="9be35-145">To ensure that the service works correctly, and that all the business data that is required for and generated by Electronic invoicing is accessed appropriately, you must create two main Azure resources:</span></span>

- <span data-ttu-id="9be35-146">ein Azure-Speicherkonto (Blob-Speicher) zum Speichern elektronischer Rechnungen</span><span class="sxs-lookup"><span data-stu-id="9be35-146">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="9be35-147">einen Azure-Schlüsseltresor zum Speichern von Zertifikaten und des URI (Uniform Resource Identifier) des Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="9be35-147">An Azure key vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>

> [!NOTE]
> <span data-ttu-id="9be35-148">Ein dedizierter Schlüsseltresor und ein Speicherkonto für den Kunden müssen speziell für die Verwendung mit der elektronischen Rechnungsstellung zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="9be35-148">A dedicated key vault and customer storage account must be allocated specifically for use with the Electronic invoicing .</span></span>

<span data-ttu-id="9be35-149">Weitere Informationen finden Sie unter [Ein Azure-Speicherkonto und einen Schlüsseltresor erstellen](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="9be35-149">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

#### <a name="users"></a><span data-ttu-id="9be35-150">Benutzer</span><span class="sxs-lookup"><span data-stu-id="9be35-150">Users</span></span>

<span data-ttu-id="9be35-151">Jede Service-Umgebung muss die Benutzer auflisten, die aus Dynamics 365 Finance und Dynamics 365 Supply Chain Management in der elektronischen Rechnungsstellung eine Verbindung herstellen können.</span><span class="sxs-lookup"><span data-stu-id="9be35-151">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in Electronic invoicing.</span></span>

#### <a name="publication"></a><span data-ttu-id="9be35-152">Veröffentlichung</span><span class="sxs-lookup"><span data-stu-id="9be35-152">Publication</span></span>

<span data-ttu-id="9be35-153">Service-Umgebungen müssen in der elektronischen Rechnungsstellung veröffentlicht werden, bevor sie genutzt werden können.</span><span class="sxs-lookup"><span data-stu-id="9be35-153">Service environments must be published to Electronic invoicing before they can be used.</span></span> <span data-ttu-id="9be35-154">Finance und Supply Chain Management können nur auf veröffentlichte Umgebungen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="9be35-154">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="9be35-155">Darüber hinaus muss eine Service-Umgebung veröffentlicht werden, bevor Aktualisierungen ihrer Attribute für den elektronischen Rechnungsstellungsdienst in Kraft treten.</span><span class="sxs-lookup"><span data-stu-id="9be35-155">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="9be35-156">Verbundene Anwendungen</span><span class="sxs-lookup"><span data-stu-id="9be35-156">Connected applications</span></span>

<span data-ttu-id="9be35-157">Verbundene Anwendungen sind die Instanzen von Finance und Supply Chain Management, die Sie möglicherweise über RCS erreichen möchten.</span><span class="sxs-lookup"><span data-stu-id="9be35-157">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="9be35-158">Neben der Anwendungs-URL und ihrem Mandanten enthält eine verbundene Anwendung die Anmeldeinformationen, mit denen RCS eine Verbindung zur Umgebung herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="9be35-158">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="9be35-159">Über die verbundenen Anwendungen können Sie einen Teil der Funktion für die elektronische Rechnungsstellung in Finance und Supply Chain Management so konfigurieren, dass die gesamte Funktion für die elektronische Rechnungsstellung funktioniert.</span><span class="sxs-lookup"><span data-stu-id="9be35-159">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="9be35-160">Finance und Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="9be35-160">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="9be35-161">Integration in die elektronische Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="9be35-161">Integration with Electronic invoicing</span></span>

<span data-ttu-id="9be35-162">Bevor Sie mit Finance und Supply Chain Management elektronische Rechnungen über die elektronische Rechnungsstellung ausstellen können, muss sie so konfiguriert sein, dass die Kommunikation mit dem Dienst möglich ist.</span><span class="sxs-lookup"><span data-stu-id="9be35-162">Before you can use Finance and Supply Chain Management to issue electronic invoices through Electronic invoicing, it must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-integration-feature"></a><span data-ttu-id="9be35-163">Integrationsfunktion für die elektronische Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="9be35-163">Electronic invoicing integration feature</span></span>

<span data-ttu-id="9be35-164">Um die Kommunikation zwischen Finance und Supply Chain Management sowie der elektronischen Rechnungsstellung zu ermöglichen, müssen Sie die Funktion **Integration für die elektronische Rechnungsstellung** im Arbeitsbereich **Funktionsverwaltung** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="9be35-164">To enable communication between Finance and Supply Chain Management and Electronic invoicing, you must turn on the **Electronic Invoicing integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="9be35-165">Dienstendpunkt</span><span class="sxs-lookup"><span data-stu-id="9be35-165">Service endpoint</span></span>

<span data-ttu-id="9be35-166">Der Dienstendpunkt ist die URL, unter der sich die elektronische Rechnungsstellung befindet.</span><span class="sxs-lookup"><span data-stu-id="9be35-166">The service endpoint is the URL where Electronic invoicing is located.</span></span> <span data-ttu-id="9be35-167">Bevor elektronische Rechnungen ausgestellt werden können, muss der Dienstendpunkt in Finance und Supply Chain Management konfiguriert werden, um die Kommunikation mit dem Dienst zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="9be35-167">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="9be35-168">Rufen Sie **Organisationsverwaltung \> Einrichtung \> Parameter elektronischer Dokumente** auf, um den Dienstendpunkt zu konfigurieren. Geben Sie anschließend auf der Registerkarte **Übermittlungsdienste** im Feld **URL für die elektronische Rechnungsstellung** die URL ein – wie in der Tabelle im Abschnitt **Dienstendpunkt** beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9be35-168">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="9be35-169">Umgebungen</span><span class="sxs-lookup"><span data-stu-id="9be35-169">Environments</span></span>

<span data-ttu-id="9be35-170">Der Umgebungsname, der in Finance und Supply Chain Management eingegeben wird, bezieht sich auf den Namen der Umgebung, die in RCS erstellt und in der elektronischen Rechnungsstellung veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="9be35-170">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to Electronic invoicing.</span></span>

<span data-ttu-id="9be35-171">Die Umgebung muss auf der Registerkarte **Übermittlungsdienste** der Seite **Parameter elektronischer Dokumente** konfiguriert werden, sodass jede Anfrage zur Ausstellung elektronischer Rechnungen die Umgebung enthält, in der die elektronische Rechnungsstellung bestimmen kann, welche elektronische Rechnungsfunktion die Anfrage verarbeiten muss.</span><span class="sxs-lookup"><span data-stu-id="9be35-171">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where Electronic invoicing can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9be35-172">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9be35-172">Additional resources</span></span>

- [<span data-ttu-id="9be35-173">Elektronische Rechnungen in RCS konfigurieren</span><span class="sxs-lookup"><span data-stu-id="9be35-173">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="9be35-174">Elektronische Rechnungen in Finance und Supply Chain Management ausstellen</span><span class="sxs-lookup"><span data-stu-id="9be35-174">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
