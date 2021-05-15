---
title: Verwaltungskomponenten der elektronischen Rechnungsstellung
description: Dieses Thema enthält Informationen zu den Komponenten, die sich auf die Verwaltung der elektronischen Rechnungsstellung beziehen.
author: gionoder
ms.date: 04/29/2021
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
ms.openlocfilehash: 3ac4a03d75898680b5655421f3024dc6f666464c
ms.sourcegitcommit: 54d3ec0c006bfa9d2b849590205be08551c4e0f0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2021
ms.locfileid: "5963190"
---
# <a name="electronic-invoicing-administration-components"></a><span data-ttu-id="a6130-103">Verwaltungskomponenten der elektronischen Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="a6130-103">Electronic invoicing administration components</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a6130-104">Dieses Thema enthält Informationen zu den Komponenten, die sich auf die Verwaltung der elektronischen Rechnungsstellung beziehen.</span><span class="sxs-lookup"><span data-stu-id="a6130-104">This topic provides information about the components that are related to administration of Electronic invoicing.</span></span> <span data-ttu-id="a6130-105">Außerdem finden Sie Informationen zum Konfigurieren der elektronischen Rechnungsstellung.</span><span class="sxs-lookup"><span data-stu-id="a6130-105">It also provides information about how to configure the Electronic invoicing service.</span></span>

## <a name="azure"></a><span data-ttu-id="a6130-106">Azure</span><span class="sxs-lookup"><span data-stu-id="a6130-106">Azure</span></span>

<span data-ttu-id="a6130-107">Verwenden Sie Microsoft Azure, um die Geheimnisse für den Key Vault und das Speicherkonto zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a6130-107">Use Microsoft Azure to create the secrets for the Key Vault and storage account.</span></span> <span data-ttu-id="a6130-108">Verwenden Sie dann die Geheimnisse in der Konfiguration der elektronischen Rechnungsstellung.</span><span class="sxs-lookup"><span data-stu-id="a6130-108">Then use the secrets in the configuration of Electronic invoicing.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="a6130-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="a6130-109">Lifecycle Services</span></span>

<span data-ttu-id="a6130-110">Verwenden Sie Microsoft Dynamics Lifecycle Services (LCS), um die Microservices für Ihr LCS-Bereitstellungsprojekt zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a6130-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the microservices for your LCS deployment project.</span></span>

> [!NOTE]
> <span data-ttu-id="a6130-111">Für die Installation des Microservices in LCS ist mindestens ein virtueller Tier 2-Computer erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a6130-111">The installation of the microservice in LCS requires at least a Tier 2 virtual machine.</span></span> <span data-ttu-id="a6130-112">Weitere Informationen zur Umgebungsplanung finden Sie unter [Umgebungsplanung](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="a6130-112">For more information about environment planning, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
 

## <a name="regulatory-configuration-services"></a><span data-ttu-id="a6130-113">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="a6130-113">Regulatory Configuration Services</span></span>

<span data-ttu-id="a6130-114">Dynamics 365 Regulatory Configuration Services (RCS) ist die Schnittstelle für die Konfiguration der elektronischen Rechnungsstellung.</span><span class="sxs-lookup"><span data-stu-id="a6130-114">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure Electronic invoicing.</span></span> <span data-ttu-id="a6130-115">Ressourcen wie Umgebungen und Funktionen für die elektronische Rechnungsstellung werden in RCS erstellt, verwaltet und gehostet.</span><span class="sxs-lookup"><span data-stu-id="a6130-115">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="a6130-116">Wenn die Ressourcen bereit sind, werden sie in der elektronischen Rechnungsstellung veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="a6130-116">When the resources are ready, they are published to Electronic invoicing service.</span></span>

<span data-ttu-id="a6130-117">Informationen zur RCS-Anmeldung finden Sie unter [Regulatory services](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="a6130-117">For RCS sign-up, see [Regulatory services](https://marketing.configure.global.dynamics.com/).</span></span>

<span data-ttu-id="a6130-118">Weitere Informationen zu RCS finden Sie unter [Regulatory Configuration Services (RCS) – Globalisierungsfunktionen](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="a6130-118">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="a6130-119">Integration in die elektronische Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="a6130-119">Integration with Electronic invoicing</span></span> 

<span data-ttu-id="a6130-120">Bevor Sie RCS zum Konfigurieren elektronischer Rechnungen verwenden können, müssen Sie RCS konfigurieren, um die Kommunikation mit der elektronischen Rechnungsstellung zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="a6130-120">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with Electronic invoicing.</span></span> <span data-ttu-id="a6130-121">Diese Konfiguration führen Sie auf der Registerkarte **Elektronische Rechnungsstellung** der Seite **Parameter für elektronische Berichterstellung** durch.</span><span class="sxs-lookup"><span data-stu-id="a6130-121">You complete this configuration on the **Electronic invoicing** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="a6130-122">Dienstendpunkt</span><span class="sxs-lookup"><span data-stu-id="a6130-122">Service endpoint</span></span>

<span data-ttu-id="a6130-123">Die elektronische Rechnungsstellung ist in mehreren Azure-Rechenzentrumsregionen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a6130-123">Electronic invoicing is available in several Azure datacenter geographies.</span></span> <span data-ttu-id="a6130-124">In der folgenden Tabelle ist die Verfügbarkeit pro Region aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="a6130-124">The following table lists the availability per region.</span></span>

| <span data-ttu-id="a6130-125">Azure-Rechenzentrumgeografie</span><span class="sxs-lookup"><span data-stu-id="a6130-125">Azure datacenter geography</span></span> |
|----------------------------|
| <span data-ttu-id="a6130-126">USA, Osten</span><span class="sxs-lookup"><span data-stu-id="a6130-126">East US</span></span>                    |
| <span data-ttu-id="a6130-127">USA, Westen</span><span class="sxs-lookup"><span data-stu-id="a6130-127">West US</span></span>                    |
| <span data-ttu-id="a6130-128">Norden, Europa</span><span class="sxs-lookup"><span data-stu-id="a6130-128">North EU</span></span>                   |
| <span data-ttu-id="a6130-129">Westen, Europa</span><span class="sxs-lookup"><span data-stu-id="a6130-129">West EU</span></span>                    |

### <a name="service-environments"></a><span data-ttu-id="a6130-130">Dienstumgebungen</span><span class="sxs-lookup"><span data-stu-id="a6130-130">Service environments</span></span>

<span data-ttu-id="a6130-131">Service-Umgebungen sind logische Partitionen, die erstellt werden, um die Ausführung der Funktionen für die elektronische Rechnungsstellung in der elektronischen Rechnungsstellung zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a6130-131">Service environments are logical partitions that are created to support execution of the electronic invoicing features in Electronic invoicing.</span></span> <span data-ttu-id="a6130-132">Die Sicherheitsgeheimnisse und digitalen Zertifikate sowie die Governance (d. h. Zugriffsberechtigungen) müssen auf der Ebene der Service-Umgebung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="a6130-132">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="a6130-133">Kunden können beliebig viele Service-Umgebungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="a6130-133">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="a6130-134">Alle von einem Kunden erstellten Service-Umgebungen sind voneinander unabhängig.</span><span class="sxs-lookup"><span data-stu-id="a6130-134">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="a6130-135">Service-Umgebungen müssen in RCS erstellt und verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="a6130-135">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="a6130-136">Wenn die Service-Umgebungen bereit sind, müssen sie in der elektronischen Rechnungsstellung veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="a6130-136">When the service environments are ready, they must be published to Electronic invoicing.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="a6130-137">Status der Service-Umgebung</span><span class="sxs-lookup"><span data-stu-id="a6130-137">Service environment status</span></span>

<span data-ttu-id="a6130-138">Service-Umgebungen können über den Status verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="a6130-138">Service environments can be managed through status.</span></span> <span data-ttu-id="a6130-139">Mögliche Optionen sind:</span><span class="sxs-lookup"><span data-stu-id="a6130-139">The possible options are:</span></span>

- <span data-ttu-id="a6130-140">**Nicht veröffentlicht** – Die Umgebung wurde erstellt, aber noch nicht veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="a6130-140">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="a6130-141">**Veröffentlicht** – Die Umgebung wurde in der elektronischen Rechnungsstellung veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="a6130-141">**Published** – The environment has been published to Electronic invoicing .</span></span>
- <span data-ttu-id="a6130-142">**Geändert** – Die Attribute einer veröffentlichten Umgebung wurden geändert, die Änderungen wurden jedoch noch nicht veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="a6130-142">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="a6130-143">Kundengeheimnisse</span><span class="sxs-lookup"><span data-stu-id="a6130-143">Customer secrets</span></span>

<span data-ttu-id="a6130-144">Der Dienst für die elektronische Rechnungsstellung ist verantwortlich für die Speicherung aller Ihrer Geschäftsdaten in den Azure-Ressourcen, die Ihrem Unternehmen gehören.</span><span class="sxs-lookup"><span data-stu-id="a6130-144">The Electronic invoicing service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="a6130-145">Um sicherzustellen, dass der Service ordnungsgemäß funktioniert und auf alle Geschäftsdaten, die für die elektronische Rechnungsstellung erforderlich sind und von ihr generiert werden, ordnungsgemäß zugegriffen wird, müssen Sie zwei Azure-Hauptressourcen erstellen:</span><span class="sxs-lookup"><span data-stu-id="a6130-145">To ensure that the service works correctly, and that all the business data that is required for and generated by Electronic invoicing is accessed appropriately, you must create two main Azure resources:</span></span>

- <span data-ttu-id="a6130-146">ein Azure-Speicherkonto (Blob-Speicher) zum Speichern elektronischer Rechnungen</span><span class="sxs-lookup"><span data-stu-id="a6130-146">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="a6130-147">Ein Azure Key Vault, der Zertifikate und den Uniform Resource Identifier (URI) des Speicherkontos speichert</span><span class="sxs-lookup"><span data-stu-id="a6130-147">An Azure Key Vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>


<span data-ttu-id="a6130-148">Ein dediziertes Key Vault- und Kunden-Speicherkonto muss speziell für die Elektronische Rechnungsstellung zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="a6130-148">A dedicated Key Vault and customer storage account must be allocated specifically for use with Electronic Invoicing.</span></span> <span data-ttu-id="a6130-149">Weitere Informationen finden Sie unter [Erstellen eines Azure-Speicherkontos und eines Key Vaults](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="a6130-149">For more information, see [Create an Azure storage account and a Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

<span data-ttu-id="a6130-150">Um den Zustand Ihres Key Vault zu überwachen und Warnungen zu erhalten, konfigurieren Sie den Azure Monitor für Key Vault.</span><span class="sxs-lookup"><span data-stu-id="a6130-150">To monitor the health of your Key Vault and receive alerts, configure the Azure Monitor for key Vault.</span></span> <span data-ttu-id="a6130-151">Indem Sie die Protokollierung von Schlüsseltresoren aktivieren, können Sie überwachen, wie, wann und von wem auf Ihre Schlüsseltresore zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="a6130-151">By enabling Key Vault logging, you can monitor how, when, and by whom your Key Vaults are accessed.</span></span> <span data-ttu-id="a6130-152">Weitere Informationen finden Sie unter [Überwachung und Alarmierung für Azure Key Vault](/azure/key-vault/general/alert) und [Wie Sie die Key Vault-Protokollierung aktivieren](/azure/key-vault/general/howto-logging?tabs=azure-cli).</span><span class="sxs-lookup"><span data-stu-id="a6130-152">For more information, see [Monitoring and alerting for Azure Key Vault](/azure/key-vault/general/alert) and [How to enable Key Vault logging](/azure/key-vault/general/howto-logging?tabs=azure-cli).</span></span>

<span data-ttu-id="a6130-153">Als bewährtes Verfahren sollten Sie die Geheimnisse periodisch austauschen.</span><span class="sxs-lookup"><span data-stu-id="a6130-153">As a best practice, periodically rotate the secrets.</span></span> <span data-ttu-id="a6130-154">Weitere Informationen finden Sie unter [Geheimnisvolle Dokumentation](/azure/key-vault/secrets/).</span><span class="sxs-lookup"><span data-stu-id="a6130-154">For more information, see [Secrets documentation](/azure/key-vault/secrets/).</span></span>

#### <a name="users"></a><span data-ttu-id="a6130-155">Benutzer</span><span class="sxs-lookup"><span data-stu-id="a6130-155">Users</span></span>

<span data-ttu-id="a6130-156">Jede Service-Umgebung muss die Benutzer auflisten, die aus Dynamics 365 Finance und Dynamics 365 Supply Chain Management in der elektronischen Rechnungsstellung eine Verbindung herstellen können.</span><span class="sxs-lookup"><span data-stu-id="a6130-156">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in Electronic invoicing.</span></span>

#### <a name="publication"></a><span data-ttu-id="a6130-157">Veröffentlichung</span><span class="sxs-lookup"><span data-stu-id="a6130-157">Publication</span></span>

<span data-ttu-id="a6130-158">Service-Umgebungen müssen in der elektronischen Rechnungsstellung veröffentlicht werden, bevor sie genutzt werden können.</span><span class="sxs-lookup"><span data-stu-id="a6130-158">Service environments must be published to Electronic invoicing before they can be used.</span></span> <span data-ttu-id="a6130-159">Finance und Supply Chain Management können nur auf veröffentlichte Umgebungen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="a6130-159">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="a6130-160">Darüber hinaus muss eine Service-Umgebung veröffentlicht werden, bevor Aktualisierungen ihrer Attribute für den elektronischen Rechnungsstellungsdienst in Kraft treten.</span><span class="sxs-lookup"><span data-stu-id="a6130-160">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="a6130-161">Verbundene Anwendungen</span><span class="sxs-lookup"><span data-stu-id="a6130-161">Connected applications</span></span>

<span data-ttu-id="a6130-162">Verbundene Anwendungen sind die Instanzen von Finance und Supply Chain Management, die Sie möglicherweise über RCS erreichen möchten.</span><span class="sxs-lookup"><span data-stu-id="a6130-162">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="a6130-163">Neben der Anwendungs-URL und ihrem Mandanten enthält eine verbundene Anwendung die Anmeldeinformationen, mit denen RCS eine Verbindung zur Umgebung herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="a6130-163">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="a6130-164">Über die verbundenen Anwendungen können Sie einen Teil der Funktion für die elektronische Rechnungsstellung in Finance und Supply Chain Management so konfigurieren, dass die gesamte Funktion für die elektronische Rechnungsstellung funktioniert.</span><span class="sxs-lookup"><span data-stu-id="a6130-164">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="a6130-165">Finance und Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="a6130-165">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="a6130-166">Integration in die elektronische Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="a6130-166">Integration with Electronic invoicing</span></span>

<span data-ttu-id="a6130-167">Bevor Sie mit Finance und Supply Chain Management elektronische Rechnungen über die elektronische Rechnungsstellung ausstellen können, muss sie so konfiguriert sein, dass die Kommunikation mit dem Dienst möglich ist.</span><span class="sxs-lookup"><span data-stu-id="a6130-167">Before you can use Finance and Supply Chain Management to issue electronic invoices through Electronic invoicing, it must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-integration-feature"></a><span data-ttu-id="a6130-168">Integrationsfunktion für die elektronische Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="a6130-168">Electronic invoicing integration feature</span></span>

<span data-ttu-id="a6130-169">Um die Kommunikation zwischen Finance und Supply Chain Management sowie der elektronischen Rechnungsstellung zu ermöglichen, müssen Sie die Funktion **Integration für die elektronische Rechnungsstellung** im Arbeitsbereich **Funktionsverwaltung** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a6130-169">To enable communication between Finance and Supply Chain Management and Electronic invoicing, you must turn on the **Electronic Invoicing integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="a6130-170">Dienstendpunkt</span><span class="sxs-lookup"><span data-stu-id="a6130-170">Service endpoint</span></span>

<span data-ttu-id="a6130-171">Der Dienstendpunkt ist die URL, unter der sich die elektronische Rechnungsstellung befindet.</span><span class="sxs-lookup"><span data-stu-id="a6130-171">The service endpoint is the URL where Electronic invoicing is located.</span></span> <span data-ttu-id="a6130-172">Bevor elektronische Rechnungen ausgestellt werden können, muss der Dienstendpunkt in Finance und Supply Chain Management konfiguriert werden, um die Kommunikation mit dem Dienst zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="a6130-172">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="a6130-173">Rufen Sie **Organisationsverwaltung \> Einrichtung \> Parameter elektronischer Dokumente** auf, um den Dienstendpunkt zu konfigurieren. Geben Sie anschließend auf der Registerkarte **Übermittlungsdienste** im Feld **URL für die elektronische Rechnungsstellung** die URL ein – wie in der Tabelle im Abschnitt **Dienstendpunkt** beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a6130-173">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="a6130-174">Umgebungen</span><span class="sxs-lookup"><span data-stu-id="a6130-174">Environments</span></span>

<span data-ttu-id="a6130-175">Der Umgebungsname, der in Finance und Supply Chain Management eingegeben wird, bezieht sich auf den Namen der Umgebung, die in RCS erstellt und in der elektronischen Rechnungsstellung veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="a6130-175">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to Electronic invoicing.</span></span>

<span data-ttu-id="a6130-176">Die Umgebung muss auf der Registerkarte **Übermittlungsdienste** der Seite **Parameter elektronischer Dokumente** konfiguriert werden, sodass jede Anfrage zur Ausstellung elektronischer Rechnungen die Umgebung enthält, in der die elektronische Rechnungsstellung bestimmen kann, welche elektronische Rechnungsfunktion die Anfrage verarbeiten muss.</span><span class="sxs-lookup"><span data-stu-id="a6130-176">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where Electronic invoicing can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a6130-177">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a6130-177">Additional resources</span></span>

- [<span data-ttu-id="a6130-178">Elektronische Rechnungen in RCS konfigurieren</span><span class="sxs-lookup"><span data-stu-id="a6130-178">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="a6130-179">Elektronische Rechnungen in Finance und Supply Chain Management ausstellen</span><span class="sxs-lookup"><span data-stu-id="a6130-179">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
