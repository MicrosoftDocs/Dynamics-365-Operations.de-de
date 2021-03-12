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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1d9482a45cb8f2ea52e7f58d55e30cfe56694d04
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985953"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a>Unterstützung für ein Content Delivery Network (CDN) hinzufügen


[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie ein Content Delivery Network (CDN) Ihrer Microsoft Dynamics 365 Commerce Umgebung hinzugefügt wird.

## <a name="overview"></a>Übersicht

Wenn Sie eine E-Commerce-Umgebung in Dynamics 365 Commerce einrichten, können Sie diese so konfigurieren, dass sie mit Ihrem CDN-Dienst arbeitet. 

Ihre benutzerdefinierte Domäne kann während des Bereitstellungsprozesses für Ihre E-Commerce-Umgebung aktiviert werden. Alternativ können Sie eine Serviceanforderung verwenden, um diese einzurichten, nachdem der Bereitstellungsprozess abgeschlossen ist. Der Bereitstellungsprozess für die E-Commerce-Umgebung generiert einen Hostnamen, der der Umgebung zugeordnet ist. Dieser Hostname hat das folgende Format, wobei \<*e-commerce-tenant-name*\> der Name Ihrer Umgebung ist:

&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com

Der Hostname oder der Endpunkt, die während des Bereitstellungsprozesses generiert wird, unterstützt eine Secure Sockets Layer (SSL)-Bescheinigung nur für \*.commerce.dynamics.com. Er unterstützt nicht SSL für benutzerdefinierte Domänen. Daher müssen Sie SSL für benutzerdefinierte Domänen in Ihrem CDN beenden und den Datenverkehr vom CDN zum Hostnamen Endpunkt weiterleiten, der Commerce generiert hat. 

Darüber hinaus kommt die *Statik* (JavaScript oder Cascading Style Sheets \[CSS\] Dateien) von Commerce vom Endpunkt, die Commerce generiert hat (\*.commerce.dynamics.com). Die Statik kann nur zwischengespeichert werden, wenn der Hostname oder der Endpunkt, der generiert wurde, hinter den CDN gestellt wird.

## <a name="set-up-ssl"></a>SSL einrichten

Um sicherzustellen, dass SSL eingerichtet ist und dass die Statik zwischengespeichert wird, müssen Sie Ihre CDN konfigurieren, damit sie dem Hostnamen zugeordnet wird, die Commerce für Ihre Umgebung generiert wurde. Sie müssen folgendes Muster nur für Statik zwischenspeichern: 

/\_msdyn365/\_scnr/\*

Nachdem Sie Ihre Commerce Umgebung mit der benutzerdefinierten Domäne bereitgestellt haben oder nachdem Sie die benutzerdefinierte Domäne für Ihre Umgebung mithilfe der Serviceanforderung bereitgestellt haben, zeigen Sie Ihre benutzerdefinierten Domäne zum Hostnamen oder Endpunkt, der Commerce generiert hat.

Wie zuvor erwähnt unterstützt der generierte Hostname oder der Endpunkt eine SSL-Zertifikat nur für \*.commerce.dynamics.com. Er unterstützt nicht SSL für benutzerdefinierte Domänen.

## <a name="cdn-services"></a>CDN-Services

Jeder CDN-Service kann mit einer Handelsumgebung verwendet werden. Nachfolgend finden Sie zwei Beispiele:

- **Microsoft Azure Front Door Service** – Die Azure CDN Lösung. Weitere Informationen über den Azure Front Door Service finden Sie unter [Azure Front Door Service Dokumentation](https://docs.microsoft.com/azure/frontdoor/).
- **Akamai Dynamic Site Accelerator** – Weitere Informationen finden Sie unter [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).

## <a name="cdn-setup"></a>CDN-Einstellungen

Der CDN-Einstellungsprozess besteht aus diesen allgemeinen Schritten:

1. Hinzufügen eines Front-End-Hosts.
1. Konfigurieren eines Back-End-Pools.
1. Richten Sie Regeln zum Weiterleiten und Zwischenspeichern ein.

### <a name="add-a-front-end-host"></a>Hinzufügen eines Front-End-Hosts.

Jeder CDN-Service kann verwendet werden, jedoch wird zum Beispiel in diesem Thema Azure Front Door Service verwendet. 

Informationen darüber, wie Azure Front Door Service eingerichtet wird, finden Sie unter [Schnellstart: Front Door für eine stark benutzte globale Webanwendung erstellen](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a>Konfigurieren eines Back-End-Pools in Azure Front Door Service

Um einen Back-End-Pool in Azure Front Door Service zu konfigurieren, folgen Sie diesen Schritten.

1. Fügen Sie **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** dem Back-End-Pool als benutzerdefinierten Host hinzu, der einen leeren Back-End-Host-Titel hat.
1. Lassen Sie unter **Lastenausgleich** die Standardwerte.

Die folgende Abbildung zeigt das Dialogfeld **Hinzufügen eines Back-End-Pools** in Azure Front Door Service mit dem eingegebenen Back-End-Hostnamen.

![Hinzufügen eines Back-End-Pool Dialogfelds](./media/CDN_BackendPool.png)

Die folgende Abbildung zeigt das Dialogfeld **Hinzufügen eines Back-End-Pools** in Azure Front Door Service mit den Standardwerten des Lastenausgleichs.

![Hinzufügen eines Back-End-Pool Dialogfelds – Fortsetzung](./media/CDN_BackendPool_2.png)

### <a name="set-up-rules-in-azure-front-door-service"></a>Richten Sie Regeln in Azure Front Door Service ein

Um eine Routingregel im Azure Front Door Service einzurichten, führen Sie die folgenden Schritte aus.

1. Eine Routingregel hinzufügen.
1. Geben Sie im Feld **Name** **Standard** ein.
1. Wählen Sie im Feld **Angenommenes Protokoll** **HTTP und HTTPS** aus.
1. Im Feld **Frontend-Hosts** geben Sie den Text **dynamics-ecom-tenant-name.azurefd.net** ein.
1. Unter **Muster zur Übereinstimmung** im oberen Feld geben Sie **/\** _ ein.
1. Unter **Arbeitsplandetails** legen Sie die Option **Arbeitsplantyp** auf **Vorwärts** fest.
1. Wählen Sie im Feld **Backend-Pool** **ecom-backend**.
1. In der Feldgruppe **Weiterleitungsprotokoll** wählen Sie die Option **Abgleichungsanforderung** aus. 
1. Hier können Sie die Option **URL neu schreiben** auf **Deaktiviert** festlegen.
1. Hier können Sie die Option **Zwischenspeichern** auf **Deaktiviert** festlegen.

Um eine Routingregel im Azure Front Door Service zwischenzuspeichern, führen Sie die folgenden Schritte aus.

1. Eine Zwischenspeicherregel hinzufügen.
1. Geben Sie im Feld **Name** **Statik** ein.
1. Wählen Sie im Feld **Angenommenes Protokoll** **HTTP und HTTPS** aus.
1. Im Feld **Frontend-Hosts** geben Sie den Text **dynamics-ecom-tenant-name.azurefd.net** ein.
1. Unter **Muster zur Übereinstimmung** im oberen Feld **/\_msdyn365/\_scnr/\** _.
1. Unter **Arbeitsplandetails** legen Sie die Option **Arbeitsplantyp** auf **Vorwärts** fest.
1. Wählen Sie im Feld **Backend-Pool** **ecom-backend**.
1. In der Feldgruppe **Weiterleitungsprotokoll** wählen Sie die Option **Abgleichungsanforderung** aus.
1. Hier können Sie die Option **URL neu schreiben** auf **Deaktiviert** festlegen.
1. Hier können Sie die Option **Zwischenspeichern** auf **Deaktiviert** festlegen.
1. Wählen Sie im Feld **Verhalten für Zwischenspeicherabfagezeichenfolge**, **Jede einzelne URL zwischenspeichern** aus.
1. In der Feldgruppe **Dynamische Kompression** wählen Sie die Option **Aktiviert** aus.

Die folgende Abbildung zeigt das Dialogfeld **Hinzufügen einer Regel** in Azure Front Door Service an.

![Fügen Sie ein Regeldialogfeld hinzu](./media/CDN_CachingRule.png)

> [!WARNING]
> Wenn die Domain, die Sie verwenden, bereits aktiv ist, erstellen Sie ein Supportticket aus der Kachel **Support** in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/), um Unterstützung für Ihre nächsten Schritte zu erhalten. Weitere Informationen finden Sie unter [Support für Finance and Operations Apps oder Lifecycle Services (LCS) anfordern](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

Wenn Ihre Domäne neu und keine bereits vorhandene aktive Domäne ist, können Sie Ihre benutzerdefinierte Domäne der Konfiguration für den Azure Front Door Service hinzufügen. So kann der Webdatenverkehr über die Azure-Front-Door-Instanz auf Ihre Site weitergeleitet werden. Um die benutzerdefinierte Domäne hinzuzufügen (beispielsweise `www.fabrikam.com`), müssen Sie einen kanonischen Namen (CNAME) für die Domäne konfigurieren.

Die folgende Abbildung zeigt das Dialogfeld **CNAME Konfiguration** in Azure Front Door Service an.

![CNAME Konfigurationsdialogfeld](./media/CNAME_Configuration.png)

Sie können Azure Front Door Service verwenden, um die Zertifikate zu verwalten, oder Sie können eine eigene Bescheinigung für die benutzerdefinierte Domäne verwenden.

Die folgende Abbildung zeigt das Dialogfeld **Benutzerdefinierte Domäne HTTPS** in Azure Front Door Service an.

![Benutzerdefiniertes Dialogfeld der Domäne HTTPS](./media/Custom_Domain_HTTPS.png)

Ausführliche Anweisungen zum Hinzufügen einer benutzerdefinierten Domäne zu Ihrer Azure Front Door finden Sie unter [Benutzerdefinierte Domäne zu Front Door hinzufügen](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).

Ihr CDN sollte jetzt ordnungsgemäß konfiguriert werden, so dass sie mit der Commerce Site verwendet werden kann.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Domänennamen konfigurieren](configure-your-domain-name.md)

[Neuen E-Commerce-Mandanten bereitstellen](deploy-ecommerce-site.md)

[E-Commerce-Website erstellen](create-ecommerce-site.md)

[Zuordnen einer Dynamics 365 Commerce-Website zu einem Onlinekanal](associate-site-online-store.md)

[Robots.txt-Dateien verwalten](manage-robots-txt-files.md)

[URL-Umleitungen in Massen hochladen](upload-bulk-redirects.md)

[Einrichten eines B2C-Mandanten in Commerce](set-up-B2C-tenant.md)

[Einrichten angepasster Seiten für die Benutzeranmeldungen](custom-pages-user-logins.md)

[Konfigurieren Sie mehrere B2C-Mandanten in einer Commerce-Umgebung](configure-multi-B2C-tenants.md)

[Standortbasierte Shop-Erkennung aktivieren](enable-store-detection.md)
