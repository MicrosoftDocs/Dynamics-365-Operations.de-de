---
title: Unterstützung für ein Content Delivery Network (CDN) hinzufügen
description: In diesem Thema wird beschrieben, wie ein Content Delivery Network (CDN) Ihrer Microsoft Dynamics 365 Commerce-Umgebung hinzugefügt wird.
author: brianshook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 59277323e0995f59d3a451395a038fa3708274eb
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936829"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="08442-103">Hinzufügen von Unterstützung für ein Content Delivery Network (CDN)</span><span class="sxs-lookup"><span data-stu-id="08442-103">Add support for a content delivery network (CDN)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="08442-104">In diesem Thema wird beschrieben, wie ein Content Delivery Network (CDN) Ihrer Microsoft Dynamics 365 Commerce-Umgebung hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="08442-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="08442-105">Wenn Sie eine E-Commerce-Umgebung in Dynamics 365 Commerce einrichten, können Sie diese so konfigurieren, dass sie mit Ihrem CDN-Dienst arbeitet.</span><span class="sxs-lookup"><span data-stu-id="08442-105">When you set up an e-commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="08442-106">Ihre benutzerdefinierte Domäne kann während des Bereitstellungsprozesses für Ihre E-Commerce-Umgebung aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="08442-106">Your custom domain can be enabled during the provisioning process for your e-commerce environment.</span></span> <span data-ttu-id="08442-107">Alternativ können Sie eine Serviceanforderung verwenden, um diese einzurichten, nachdem der Bereitstellungsprozess abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="08442-107">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="08442-108">Der Bereitstellungsprozess für die E-Commerce-Umgebung generiert einen Hostnamen, der der Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="08442-108">The provisioning process for the e-commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="08442-109">Dieser Hostname hat das folgende Format, wobei \<*e-commerce-tenant-name*\> der Name Ihrer Umgebung ist:</span><span class="sxs-lookup"><span data-stu-id="08442-109">This host name has the following format, where \<*e-commerce-tenant-name*\> is the name of your environment:</span></span>

<span data-ttu-id="08442-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="08442-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="08442-111">Der Hostname oder der Endpunkt, die während des Bereitstellungsprozesses generiert wird, unterstützt eine Secure Sockets Layer (SSL)-Bescheinigung nur für \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="08442-111">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="08442-112">Er unterstützt nicht SSL für benutzerdefinierte Domänen.</span><span class="sxs-lookup"><span data-stu-id="08442-112">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="08442-113">Daher müssen Sie SSL für benutzerdefinierte Domänen in Ihrem CDN beenden und den Datenverkehr vom CDN zum Hostnamen Endpunkt weiterleiten, der Commerce generiert hat.</span><span class="sxs-lookup"><span data-stu-id="08442-113">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="08442-114">Darüber hinaus kommt die *Statik* (JavaScript oder Cascading Style Sheets \[CSS\] Dateien) von Commerce vom Endpunkt, die Commerce generiert hat (\*.commerce.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="08442-114">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="08442-115">Die Statik kann nur zwischengespeichert werden, wenn der Hostname oder der Endpunkt, der generiert wurde, hinter den CDN gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="08442-115">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="08442-116">SSL einrichten</span><span class="sxs-lookup"><span data-stu-id="08442-116">Set up SSL</span></span>

<span data-ttu-id="08442-117">Nachdem Sie Ihre Commerce Umgebung mit der benutzerdefinierten Domäne bereitgestellt haben oder nachdem Sie die benutzerdefinierte Domäne für Ihre Umgebung mithilfe der Serviceanforderung bereitgestellt haben, müssen Sie Ihre DNS-Änderungen gemeinsam mit dem Commerce-Onboarding-Team planen.</span><span class="sxs-lookup"><span data-stu-id="08442-117">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, you need to work with the Commerce onboarding team to plan the DNS changes.</span></span>

<span data-ttu-id="08442-118">Wie zuvor erwähnt unterstützt der generierte Hostname oder der Endpunkt eine SSL-Zertifikat nur für \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="08442-118">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="08442-119">Er unterstützt nicht SSL für benutzerdefinierte Domänen.</span><span class="sxs-lookup"><span data-stu-id="08442-119">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="08442-120">CDN-Services</span><span class="sxs-lookup"><span data-stu-id="08442-120">CDN services</span></span>

<span data-ttu-id="08442-121">Jeder CDN-Service kann mit einer Handelsumgebung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08442-121">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="08442-122">Nachfolgend finden Sie zwei Beispiele:</span><span class="sxs-lookup"><span data-stu-id="08442-122">Here are two examples:</span></span>

- <span data-ttu-id="08442-123">**Microsoft Azure Front Door Service** – Die Azure CDN Lösung.</span><span class="sxs-lookup"><span data-stu-id="08442-123">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="08442-124">Weitere Informationen über den Azure Front Door Service finden Sie unter [Azure Front Door Service Dokumentation](/azure/frontdoor/).</span><span class="sxs-lookup"><span data-stu-id="08442-124">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](/azure/frontdoor/).</span></span>
- <span data-ttu-id="08442-125">**Akamai Dynamic Site Accelerator** – Weitere Informationen finden Sie unter [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="08442-125">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="08442-126">CDN-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="08442-126">CDN setup</span></span>

<span data-ttu-id="08442-127">Der CDN-Einstellungsprozess besteht aus diesen allgemeinen Schritten:</span><span class="sxs-lookup"><span data-stu-id="08442-127">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="08442-128">Hinzufügen eines Front-End-Hosts.</span><span class="sxs-lookup"><span data-stu-id="08442-128">Add a front-end host.</span></span>
1. <span data-ttu-id="08442-129">Konfigurieren eines Back-End-Pools.</span><span class="sxs-lookup"><span data-stu-id="08442-129">Configure a backend pool.</span></span>
1. <span data-ttu-id="08442-130">Richten Sie Routingregeln ein.</span><span class="sxs-lookup"><span data-stu-id="08442-130">Set up rules for routing.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="08442-131">Hinzufügen eines Front-End-Hosts.</span><span class="sxs-lookup"><span data-stu-id="08442-131">Add a front-end host</span></span>

<span data-ttu-id="08442-132">Jeder CDN-Service kann verwendet werden, jedoch wird zum Beispiel in diesem Thema Azure Front Door Service verwendet.</span><span class="sxs-lookup"><span data-stu-id="08442-132">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="08442-133">Informationen darüber, wie Azure Front Door Service eingerichtet wird, finden Sie unter [Schnellstart: Front Door für eine stark benutzte globale Webanwendung erstellen](/azure/frontdoor/quickstart-create-front-door).</span><span class="sxs-lookup"><span data-stu-id="08442-133">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a><span data-ttu-id="08442-134">Konfigurieren eines Back-End-Pools in Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="08442-134">Configure a backend pool in Azure Front Door Service</span></span>

<span data-ttu-id="08442-135">Um einen Back-End-Pool in Azure Front Door Service zu konfigurieren, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="08442-135">To configure a backend pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="08442-136">Fügen Sie **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** einen Back-End-Pool als benutzerdefinierten Host hinzu, der eine Back-End-Host-Kopfzeile hat, die **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** entspricht.</span><span class="sxs-lookup"><span data-stu-id="08442-136">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a backend pool as a custom host that has a backend host header that is the same as **&lt;ecom-tenant-name&gt;.commerce.dynamics.com**.</span></span>
1. <span data-ttu-id="08442-137">Lassen Sie unter **Lastenausgleich** die Standardwerte.</span><span class="sxs-lookup"><span data-stu-id="08442-137">Under **Load balancing**, leave the default values.</span></span>
1. <span data-ttu-id="08442-138">Deaktivieren Sie Integritätsprüfungen für den Back-End-Pool.</span><span class="sxs-lookup"><span data-stu-id="08442-138">Disable health checks for the backend pool.</span></span>

<span data-ttu-id="08442-139">Die folgende Abbildung zeigt das Dialogfeld **Hinzufügen eines Back-End-Pools** in Azure Front Door Service mit dem eingegebenen Back-End-Hostnamen.</span><span class="sxs-lookup"><span data-stu-id="08442-139">The following illustration shows the **Add a backend** dialog box in Azure Front Door Service with the backend host name entered.</span></span>

![Hinzufügen eines Back-End-Pool Dialogfelds](./media/CDN_BackendPool.png)

<span data-ttu-id="08442-141">Die folgende Abbildung zeigt das Dialogfeld **Hinzufügen eines Back-End-Pools** in Azure Front Door Service mit den Standardwerten des Lastenausgleichs.</span><span class="sxs-lookup"><span data-stu-id="08442-141">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service with the default load balancing values.</span></span>

![Hinzufügen eines Back-End-Pool Dialogfelds – Fortsetzung](./media/CDN_BackendPool_2.png)

> [!NOTE]
> <span data-ttu-id="08442-143">Stellen Sie sicher, dass Sie **Integritätstests** beim Einrichten Ihres eigenen Azure Front Door Service für Commerce deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="08442-143">Be sure to disable **Health Probes** when setting up your own Azure Front Door service for Commerce.</span></span>


### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="08442-144">Richten Sie Regeln in Azure Front Door Service ein</span><span class="sxs-lookup"><span data-stu-id="08442-144">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="08442-145">Um eine Routingregel im Azure Front Door Service einzurichten, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="08442-145">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="08442-146">Eine Routingregel hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="08442-146">Add a routing rule.</span></span>
1. <span data-ttu-id="08442-147">Geben Sie im Feld **Name** **Standard** ein.</span><span class="sxs-lookup"><span data-stu-id="08442-147">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="08442-148">Wählen Sie im Feld **Angenommenes Protokoll** **HTTP und HTTPS** aus.</span><span class="sxs-lookup"><span data-stu-id="08442-148">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="08442-149">Im Feld **Frontend-Hosts** geben Sie den Text **dynamics-ecom-tenant-name.azurefd.net** ein.</span><span class="sxs-lookup"><span data-stu-id="08442-149">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="08442-150">Unter **Muster der Übereinstimmung** im oberen Feld, geben Sie **/\*** ein.</span><span class="sxs-lookup"><span data-stu-id="08442-150">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="08442-151">Unter **Arbeitsplandetails** legen Sie die Option **Arbeitsplantyp** auf **Vorwärts** fest.</span><span class="sxs-lookup"><span data-stu-id="08442-151">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="08442-152">Wählen Sie im Feld **Backend-Pool** **ecom-backend**.</span><span class="sxs-lookup"><span data-stu-id="08442-152">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="08442-153">In der Feldgruppe **Weiterleitungsprotokoll** wählen Sie die Option **Abgleichungsanforderung** aus.</span><span class="sxs-lookup"><span data-stu-id="08442-153">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="08442-154">Hier können Sie die Option **URL neu schreiben** auf **Deaktiviert** festlegen.</span><span class="sxs-lookup"><span data-stu-id="08442-154">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="08442-155">Hier können Sie die Option **Zwischenspeichern** auf **Deaktiviert** festlegen.</span><span class="sxs-lookup"><span data-stu-id="08442-155">Set the **Caching** option to **Disabled**.</span></span>


> [!WARNING]
> <span data-ttu-id="08442-156">Wenn die Domain, die Sie verwenden, bereits aktiv ist, erstellen Sie ein Supportticket aus der Kachel **Support** in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/), um Unterstützung für Ihre nächsten Schritte zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="08442-156">If the domain that you will use is already active and live, create a support ticket from the **Support** tile in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) to get assistance for your next steps.</span></span> <span data-ttu-id="08442-157">Weitere Informationen finden Sie unter [Support für Finance and Operations Apps oder Lifecycle Services (LCS) anfordern](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="08442-157">For more information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

<span data-ttu-id="08442-158">Wenn Ihre Domäne neu und keine bereits vorhandene aktive Domäne ist, können Sie Ihre benutzerdefinierte Domäne der Konfiguration für den Azure Front Door Service hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="08442-158">If your domain is new and is not a pre-existing live domain, you can add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="08442-159">So kann der Webdatenverkehr über die Azure-Front-Door-Instanz auf Ihre Site weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="08442-159">This will enable web traffic to direct to your site via the Azure Front Door instance.</span></span> <span data-ttu-id="08442-160">Um die benutzerdefinierte Domäne hinzuzufügen (beispielsweise `www.fabrikam.com`), müssen Sie einen kanonischen Namen (CNAME) für die Domäne konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="08442-160">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="08442-161">Die folgende Abbildung zeigt das Dialogfeld **CNAME Konfiguration** in Azure Front Door Service an.</span><span class="sxs-lookup"><span data-stu-id="08442-161">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![CNAME Konfigurationsdialogfeld](./media/CNAME_Configuration.png)

<span data-ttu-id="08442-163">Sie können Azure Front Door Service verwenden, um die Zertifikate zu verwalten, oder Sie können eine eigene Bescheinigung für die benutzerdefinierte Domäne verwenden.</span><span class="sxs-lookup"><span data-stu-id="08442-163">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="08442-164">Die folgende Abbildung zeigt das Dialogfeld **Benutzerdefinierte Domäne HTTPS** in Azure Front Door Service an.</span><span class="sxs-lookup"><span data-stu-id="08442-164">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![Benutzerdefiniertes Dialogfeld der Domäne HTTPS](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="08442-166">Ausführliche Anweisungen zum Hinzufügen einer benutzerdefinierten Domäne zu Ihrer Azure Front Door finden Sie unter [Benutzerdefinierte Domäne zu Front Door hinzufügen](/azure/frontdoor/front-door-custom-domain).</span><span class="sxs-lookup"><span data-stu-id="08442-166">For detailed instructions on adding a custom domain to your Azure Front Door, see [Add a custom domain to your Front Door](/azure/frontdoor/front-door-custom-domain).</span></span>

<span data-ttu-id="08442-167">Ihr CDN sollte jetzt ordnungsgemäß konfiguriert werden, so dass sie mit der Commerce Site verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="08442-167">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="08442-168">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="08442-168">Additional resources</span></span>

[<span data-ttu-id="08442-169">Implementierungsoptionen für das Content Delivery Network</span><span class="sxs-lookup"><span data-stu-id="08442-169">Content delivery network implementation options</span></span>](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]