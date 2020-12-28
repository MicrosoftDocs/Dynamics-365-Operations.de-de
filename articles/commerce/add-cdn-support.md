---
title: Unterstützung für ein Content Delivery Network (CDN) hinzufügen
description: In diesem Thema wird beschrieben, wie ein Content Delivery Network (CDN) Ihrer Microsoft Dynamics 365 Commerce Umgebung hinzugefügt wird.
author: brianshook
manager: annbe
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0e888fca4a5401f1df6e61b10358489846ad4b0e
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517207"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="ea113-103">Unterstützung für ein Content Delivery Network (CDN) hinzufügen</span><span class="sxs-lookup"><span data-stu-id="ea113-103">Add support for a content delivery network (CDN)</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ea113-104">In diesem Thema wird beschrieben, wie ein Content Delivery Network (CDN) Ihrer Microsoft Dynamics 365 Commerce Umgebung hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="ea113-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

## <a name="overview"></a><span data-ttu-id="ea113-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="ea113-105">Overview</span></span>

<span data-ttu-id="ea113-106">Wenn Sie eine E-Commerce-Umgebung in Dynamics 365 Commerce einrichten, können Sie diese so konfigurieren, dass sie mit Ihrem CDN-Dienst arbeitet.</span><span class="sxs-lookup"><span data-stu-id="ea113-106">When you set up an e-commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="ea113-107">Ihre benutzerdefinierte Domäne kann während des Bereitstellungsprozesses für Ihre E-Commerce-Umgebung aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="ea113-107">Your custom domain can be enabled during the provisioning process for your e-commerce environment.</span></span> <span data-ttu-id="ea113-108">Alternativ können Sie eine Serviceanforderung verwenden, um diese einzurichten, nachdem der Bereitstellungsprozess abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="ea113-108">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="ea113-109">Der Bereitstellungsprozess für die E-Commerce-Umgebung generiert einen Hostnamen, der der Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ea113-109">The provisioning process for the e-commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="ea113-110">Dieser Hostname hat das folgende Format, wobei \<*e-commerce-tenant-name*\> der Name Ihrer Umgebung ist:</span><span class="sxs-lookup"><span data-stu-id="ea113-110">This host name has the following format, where \<*e-commerce-tenant-name*\> is the name of your environment:</span></span>

<span data-ttu-id="ea113-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="ea113-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="ea113-112">Der Hostname oder der Endpunkt, die während des Bereitstellungsprozesses generiert wird, unterstützt eine Secure Sockets Layer (SSL)-Bescheinigung nur für \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="ea113-112">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="ea113-113">Er unterstützt nicht SSL für benutzerdefinierte Domänen.</span><span class="sxs-lookup"><span data-stu-id="ea113-113">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="ea113-114">Daher müssen Sie SSL für benutzerdefinierte Domänen in Ihrem CDN beenden und den Datenverkehr vom CDN zum Hostnamen Endpunkt weiterleiten, der Commerce generiert hat.</span><span class="sxs-lookup"><span data-stu-id="ea113-114">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="ea113-115">Darüber hinaus kommt die *Statik* (JavaScript oder Cascading Style Sheets \[CSS\] Dateien) von Commerce vom Endpunkt, die Commerce generiert hat (\*.commerce.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="ea113-115">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="ea113-116">Die Statik kann nur zwischengespeichert werden, wenn der Hostname oder der Endpunkt, der generiert wurde, hinter den CDN gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="ea113-116">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="ea113-117">SSL einrichten</span><span class="sxs-lookup"><span data-stu-id="ea113-117">Set up SSL</span></span>

<span data-ttu-id="ea113-118">Um sicherzustellen, dass SSL eingerichtet ist und dass die Statik zwischengespeichert wird, müssen Sie Ihre CDN konfigurieren, damit sie dem Hostnamen zugeordnet wird, die Commerce für Ihre Umgebung generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ea113-118">To help guarantee that SSL is set up, and that statics are cached, you must configure your CDN so that it is associated with the host name that Commerce generated for your environment.</span></span> <span data-ttu-id="ea113-119">Sie müssen folgendes Muster nur für Statik zwischenspeichern:</span><span class="sxs-lookup"><span data-stu-id="ea113-119">You must also cache the following pattern for statics only:</span></span> 

<span data-ttu-id="ea113-120">/\_msdyn365/\_scnr/\*</span><span class="sxs-lookup"><span data-stu-id="ea113-120">/\_msdyn365/\_scnr/\*</span></span>

<span data-ttu-id="ea113-121">Nachdem Sie Ihre Commerce Umgebung mit der benutzerdefinierten Domäne bereitgestellt haben oder nachdem Sie die benutzerdefinierte Domäne für Ihre Umgebung mithilfe der Serviceanforderung bereitgestellt haben, zeigen Sie Ihre benutzerdefinierten Domäne zum Hostnamen oder Endpunkt, der Commerce generiert hat.</span><span class="sxs-lookup"><span data-stu-id="ea113-121">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, point your custom domain to the host name or endpoint that Commerce generated.</span></span>

<span data-ttu-id="ea113-122">Wie zuvor erwähnt unterstützt der generierte Hostname oder der Endpunkt eine SSL-Zertifikat nur für \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="ea113-122">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="ea113-123">Er unterstützt nicht SSL für benutzerdefinierte Domänen.</span><span class="sxs-lookup"><span data-stu-id="ea113-123">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="ea113-124">CDN-Services</span><span class="sxs-lookup"><span data-stu-id="ea113-124">CDN services</span></span>

<span data-ttu-id="ea113-125">Jeder CDN-Service kann mit einer Handelsumgebung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea113-125">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="ea113-126">Nachfolgend finden Sie zwei Beispiele:</span><span class="sxs-lookup"><span data-stu-id="ea113-126">Here are two examples:</span></span>

- <span data-ttu-id="ea113-127">**Microsoft Azure Front Door Service** – Die Azure CDN Lösung.</span><span class="sxs-lookup"><span data-stu-id="ea113-127">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="ea113-128">Weitere Informationen über den Azure Front Door Service finden Sie unter [Azure Front Door Service Dokumentation](https://docs.microsoft.com/azure/frontdoor/).</span><span class="sxs-lookup"><span data-stu-id="ea113-128">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="ea113-129">**Akamai Dynamic Site Accelerator** – Weitere Informationen finden Sie unter [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="ea113-129">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="ea113-130">CDN-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="ea113-130">CDN setup</span></span>

<span data-ttu-id="ea113-131">Der CDN-Einstellungsprozess besteht aus diesen allgemeinen Schritten:</span><span class="sxs-lookup"><span data-stu-id="ea113-131">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="ea113-132">Hinzufügen eines Front-End-Hosts.</span><span class="sxs-lookup"><span data-stu-id="ea113-132">Add a front-end host.</span></span>
1. <span data-ttu-id="ea113-133">Konfigurieren eines Back-End-Pools.</span><span class="sxs-lookup"><span data-stu-id="ea113-133">Configure a backend pool.</span></span>
1. <span data-ttu-id="ea113-134">Richten Sie Regeln zum Weiterleiten und Zwischenspeichern ein.</span><span class="sxs-lookup"><span data-stu-id="ea113-134">Set up rules for routing and caching.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="ea113-135">Hinzufügen eines Front-End-Hosts.</span><span class="sxs-lookup"><span data-stu-id="ea113-135">Add a front-end host</span></span>

<span data-ttu-id="ea113-136">Jeder CDN-Service kann verwendet werden, jedoch wird zum Beispiel in diesem Thema Azure Front Door Service verwendet.</span><span class="sxs-lookup"><span data-stu-id="ea113-136">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="ea113-137">Informationen darüber, wie Azure Front Door Service eingerichtet wird, finden Sie unter [Schnellstart: Front Door für eine stark benutzte globale Webanwendung erstellen](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span><span class="sxs-lookup"><span data-stu-id="ea113-137">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a><span data-ttu-id="ea113-138">Konfigurieren eines Back-End-Pools in Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="ea113-138">Configure a backend pool in Azure Front Door Service</span></span>

<span data-ttu-id="ea113-139">Um einen Back-End-Pool in Azure Front Door Service zu konfigurieren, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="ea113-139">To configure a backend pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="ea113-140">Fügen Sie **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** dem Back-End-Pool als benutzerdefinierten Host hinzu, der einen leeren Back-End-Host-Titel hat.</span><span class="sxs-lookup"><span data-stu-id="ea113-140">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a backend pool as a custom host that has an empty backend host header.</span></span>
1. <span data-ttu-id="ea113-141">Lassen Sie unter **Lastenausgleich** die Standardwerte.</span><span class="sxs-lookup"><span data-stu-id="ea113-141">Under **Load balancing**, leave the default values.</span></span>

<span data-ttu-id="ea113-142">Die folgende Abbildung zeigt das Dialogfeld **Hinzufügen eines Back-End-Pools** in Azure Front Door Service mit dem eingegebenen Back-End-Hostnamen.</span><span class="sxs-lookup"><span data-stu-id="ea113-142">The following illustration shows the **Add a backend** dialog box in Azure Front Door Service with the backend host name entered.</span></span>

![Hinzufügen eines Back-End-Pool Dialogfelds](./media/CDN_BackendPool.png)

<span data-ttu-id="ea113-144">Die folgende Abbildung zeigt das Dialogfeld **Hinzufügen eines Back-End-Pools** in Azure Front Door Service mit den Standardwerten des Lastenausgleichs.</span><span class="sxs-lookup"><span data-stu-id="ea113-144">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service with the default load balancing values.</span></span>

![Hinzufügen eines Back-End-Pool Dialogfelds – Fortsetzung](./media/CDN_BackendPool_2.png)

### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="ea113-146">Richten Sie Regeln in Azure Front Door Service ein</span><span class="sxs-lookup"><span data-stu-id="ea113-146">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="ea113-147">Um eine Routingregel im Azure Front Door Service einzurichten, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="ea113-147">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="ea113-148">Eine Routingregel hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ea113-148">Add a routing rule.</span></span>
1. <span data-ttu-id="ea113-149">Geben Sie im Feld **Name** **Standard** ein.</span><span class="sxs-lookup"><span data-stu-id="ea113-149">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="ea113-150">Wählen Sie im Feld **Angenommenes Protokoll** **HTTP und HTTPS** aus.</span><span class="sxs-lookup"><span data-stu-id="ea113-150">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="ea113-151">Im Feld **Frontend-Hosts** geben Sie den Text **dynamics-ecom-tenant-name.azurefd.net** ein.</span><span class="sxs-lookup"><span data-stu-id="ea113-151">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="ea113-152">Unter **Muster zur Übereinstimmung** im oberen Feld geben Sie \**/\** _ ein.</span><span class="sxs-lookup"><span data-stu-id="ea113-152">Under **Patterns to match**, in the upper field, enter \**/\** _.</span></span>
1. <span data-ttu-id="ea113-153">Unter **Arbeitsplandetails** legen Sie die Option **Arbeitsplantyp** auf **Vorwärts** fest.</span><span class="sxs-lookup"><span data-stu-id="ea113-153">Under _\*Route Details\*\*, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="ea113-154">Wählen Sie im Feld **Backend-Pool** **ecom-backend**.</span><span class="sxs-lookup"><span data-stu-id="ea113-154">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="ea113-155">In der Feldgruppe **Weiterleitungsprotokoll** wählen Sie die Option **Abgleichungsanforderung** aus.</span><span class="sxs-lookup"><span data-stu-id="ea113-155">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="ea113-156">Hier können Sie die Option **URL neu schreiben** auf **Deaktiviert** festlegen.</span><span class="sxs-lookup"><span data-stu-id="ea113-156">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="ea113-157">Hier können Sie die Option **Zwischenspeichern** auf **Deaktiviert** festlegen.</span><span class="sxs-lookup"><span data-stu-id="ea113-157">Set the **Caching** option to **Disabled**.</span></span>

<span data-ttu-id="ea113-158">Um eine Routingregel im Azure Front Door Service zwischenzuspeichern, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="ea113-158">To set up a caching rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="ea113-159">Eine Zwischenspeicherregel hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ea113-159">Add a caching rule.</span></span>
1. <span data-ttu-id="ea113-160">Geben Sie im Feld **Name** **Statik** ein.</span><span class="sxs-lookup"><span data-stu-id="ea113-160">In the **Name** field, enter **statics**.</span></span>
1. <span data-ttu-id="ea113-161">Wählen Sie im Feld **Angenommenes Protokoll** **HTTP und HTTPS** aus.</span><span class="sxs-lookup"><span data-stu-id="ea113-161">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="ea113-162">Im Feld **Frontend-Hosts** geben Sie den Text **dynamics-ecom-tenant-name.azurefd.net** ein.</span><span class="sxs-lookup"><span data-stu-id="ea113-162">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="ea113-163">Unter **Muster zur Übereinstimmung** im oberen Feld \**/\_msdyn365/\_scnr/\** _.</span><span class="sxs-lookup"><span data-stu-id="ea113-163">Under **Patterns to match**, in the upper field, \**/\_msdyn365/\_scnr/\** _.</span></span>
1. <span data-ttu-id="ea113-164">Unter **Arbeitsplandetails** legen Sie die Option **Arbeitsplantyp** auf **Vorwärts** fest.</span><span class="sxs-lookup"><span data-stu-id="ea113-164">Under _\*Route Details\*\*, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="ea113-165">Wählen Sie im Feld **Backend-Pool** **ecom-backend**.</span><span class="sxs-lookup"><span data-stu-id="ea113-165">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="ea113-166">In der Feldgruppe **Weiterleitungsprotokoll** wählen Sie die Option **Abgleichungsanforderung** aus.</span><span class="sxs-lookup"><span data-stu-id="ea113-166">In the **Forwarding protocol** field group, select the **Match request** option.</span></span>
1. <span data-ttu-id="ea113-167">Hier können Sie die Option **URL neu schreiben** auf **Deaktiviert** festlegen.</span><span class="sxs-lookup"><span data-stu-id="ea113-167">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="ea113-168">Hier können Sie die Option **Zwischenspeichern** auf **Deaktiviert** festlegen.</span><span class="sxs-lookup"><span data-stu-id="ea113-168">Set the **Caching** option to **Disabled**.</span></span>
1. <span data-ttu-id="ea113-169">Wählen Sie im Feld **Verhalten für Zwischenspeicherabfagezeichenfolge**, **Jede einzelne URL zwischenspeichern** aus.</span><span class="sxs-lookup"><span data-stu-id="ea113-169">In the **Query string caching behavior** field, select **Cache every unique URL**.</span></span>
1. <span data-ttu-id="ea113-170">In der Feldgruppe **Dynamische Kompression** wählen Sie die Option **Aktiviert** aus.</span><span class="sxs-lookup"><span data-stu-id="ea113-170">In the **Dynamic compression** field group, select the **Enabled** option.</span></span>

<span data-ttu-id="ea113-171">Die folgende Abbildung zeigt das Dialogfeld **Hinzufügen einer Regel** in Azure Front Door Service an.</span><span class="sxs-lookup"><span data-stu-id="ea113-171">The following illustration shows the **Add a rule** dialog box in Azure Front Door Service.</span></span>

![Fügen Sie ein Regeldialogfeld hinzu](./media/CDN_CachingRule.png)

> [!WARNING]
> <span data-ttu-id="ea113-173">Wenn die Domain, die Sie verwenden, bereits aktiv ist, erstellen Sie ein Supportticket aus der Kachel **Support** in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/), um Unterstützung für Ihre nächsten Schritte zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ea113-173">If the domain that you will use is already active and live, create a support ticket from the **Support** tile in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) to get assistance for your next steps.</span></span> <span data-ttu-id="ea113-174">Weitere Informationen finden Sie unter [Support für Finance and Operations Apps oder Lifecycle Services (LCS) anfordern](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="ea113-174">For more information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

<span data-ttu-id="ea113-175">Wenn Ihre Domäne neu und keine bereits vorhandene aktive Domäne ist, können Sie Ihre benutzerdefinierte Domäne der Konfiguration für den Azure Front Door Service hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ea113-175">If your domain is new and is not a pre-existing live domain, you can add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="ea113-176">So kann der Webdatenverkehr über die Azure-Front-Door-Instanz auf Ihre Site weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="ea113-176">This will enable web traffic to direct to your site via the Azure Front Door instance.</span></span> <span data-ttu-id="ea113-177">Um die benutzerdefinierte Domäne hinzuzufügen (beispielsweise `www.fabrikam.com`), müssen Sie einen kanonischen Namen (CNAME) für die Domäne konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ea113-177">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="ea113-178">Die folgende Abbildung zeigt das Dialogfeld **CNAME Konfiguration** in Azure Front Door Service an.</span><span class="sxs-lookup"><span data-stu-id="ea113-178">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![CNAME Konfigurationsdialogfeld](./media/CNAME_Configuration.png)

<span data-ttu-id="ea113-180">Sie können Azure Front Door Service verwenden, um die Zertifikate zu verwalten, oder Sie können eine eigene Bescheinigung für die benutzerdefinierte Domäne verwenden.</span><span class="sxs-lookup"><span data-stu-id="ea113-180">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="ea113-181">Die folgende Abbildung zeigt das Dialogfeld **Benutzerdefinierte Domäne HTTPS** in Azure Front Door Service an.</span><span class="sxs-lookup"><span data-stu-id="ea113-181">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![Benutzerdefiniertes Dialogfeld der Domäne HTTPS](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="ea113-183">Ausführliche Anweisungen zum Hinzufügen einer benutzerdefinierten Domäne zu Ihrer Azure Front Door finden Sie unter [Benutzerdefinierte Domäne zu Front Door hinzufügen](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span><span class="sxs-lookup"><span data-stu-id="ea113-183">For detailed instructions on adding a custom domain to your Azure Front Door, see [Add a custom domain to your Front Door](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span></span>

<span data-ttu-id="ea113-184">Ihr CDN sollte jetzt ordnungsgemäß konfiguriert werden, so dass sie mit der Commerce Site verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ea113-184">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ea113-185">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ea113-185">Additional resources</span></span>

[<span data-ttu-id="ea113-186">Domänennamen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="ea113-186">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="ea113-187">Neuen E-Commerce-Mandanten bereitstellen</span><span class="sxs-lookup"><span data-stu-id="ea113-187">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="ea113-188">E-Commerce-Website erstellen</span><span class="sxs-lookup"><span data-stu-id="ea113-188">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="ea113-189">Zuordnen einer Dynamics 365 Commerce-Website zu einem Onlinekanal</span><span class="sxs-lookup"><span data-stu-id="ea113-189">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="ea113-190">Robots.txt-Dateien verwalten</span><span class="sxs-lookup"><span data-stu-id="ea113-190">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="ea113-191">URL-Umleitungen in Massen hochladen</span><span class="sxs-lookup"><span data-stu-id="ea113-191">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="ea113-192">Einrichten eines B2C-Mandanten in Commerce</span><span class="sxs-lookup"><span data-stu-id="ea113-192">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="ea113-193">Einrichten angepasster Seiten für die Benutzeranmeldungen</span><span class="sxs-lookup"><span data-stu-id="ea113-193">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="ea113-194">Konfigurieren Sie mehrere B2C-Mandanten in einer Commerce-Umgebung</span><span class="sxs-lookup"><span data-stu-id="ea113-194">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="ea113-195">Standortbasierte Shop-Erkennung aktivieren</span><span class="sxs-lookup"><span data-stu-id="ea113-195">Enable location-based store detection</span></span>](enable-store-detection.md)
