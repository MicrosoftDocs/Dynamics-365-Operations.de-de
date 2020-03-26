---
title: Unterstützung für ein Content Delivery Network (CDN) hinzufügen
description: In diesem Thema wird beschrieben, wie ein Content Delivery Network (CDN) Ihrer Microsoft Dynamics 365 Commerce Umgebung hinzugefügt wird.
author: brianshook
manager: annbe
ms.date: 03/02/2020
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
ms.openlocfilehash: 23ac9d8844c2a8ae20bd316c40078319601a3a4d
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096724"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a>Unterstützung für ein Content Delivery Network (CDN) hinzufügen


[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie ein Content Delivery Network (CDN) Ihrer Microsoft Dynamics 365 Commerce Umgebung hinzugefügt wird.

## <a name="overview"></a>Übersicht

Wenn Sie eine E-Commerce-Umgebung in Dynamics 365 Commerce einrichten, können Sie diese so konfigurieren, dass sie mit dem CDN-Service arbeitet. 

Ihre benutzerdefinierte Domäne kann während des Bereitstellungsprozesses für die E-Commerce-Umgebung aktiviert werden. Alternativ können Sie eine Serviceanforderung verwenden, um diese einzurichten, nachdem der Bereitstellungsprozess abgeschlossen ist. Der Bereitstellungsprozess für die E-Commerce-Umgebung generiert einen Hostnamen, der der Umgebung zugeordnet ist. Dieser Hostname hat das folgende Format *E-Commerce-Mandantname*, was der Name Ihrer Umgebung ist:

&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com

Der Hostname oder der Endpunkt, die während des Bereitstellungsprozesses generiert wird, unterstützt eine Secure Sockets Layer (SSL)-Bescheinigung nur für \*.commerce.dynamics.com. Er unterstützt nicht SSL für benutzerdefinierte Domänen. Daher müssen Sie SSL für benutzerdefinierte Domänen in Ihrem CDN beenden und den Datenverkehr vom CDN  zum Hostnamen Endpunkt weiterleiten, der Commerce generiert hat. 

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
1. Konfigurieren eines Back-End-Pools
1. Richten Sie Regeln zum Weiterleiten und Zwischenspeichern ein.

### <a name="add-a-front-end-host"></a>Hinzufügen eines Front-End-Hosts.

Jeder CDN-Service kann verwendet werden, jedoch wird zum Beispiel in diesem Thema Azure Front Door Service verwendet. 

Informationen darüber, wie Azure Front Door Service eingerichtet wird, finden Sie unter [Schnellstart: Front Door für eine stark benutzte globale Webanwendung erstellen](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).

### <a name="configure-a-back-end-pool-in-azure-front-door-service"></a>Konfigurieren eines Back-End-Pool in Azure Front Door Service

Um einen Back-End-Pool in Azure Front Door Service zu konfigurieren, folgen Sie diesen Schritten.

1. Fügen Sie **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** dem Back-End-Pool einem benutzerdefinierten Host hinzu, der einen leeren Back-End-Host-Titel hat.
1. Unter **Statusüberprüfungen** im Feld **Pfad**, geben Sie **/keepalive** ein.
1. Geben Sie im Feld **Intervalle (Sekunden)** den Text **255** ein.
1. Lassen Sie unter **Lastenausgleich** die Standardwerte.

Die folgende Abbildung zeigt das Dialogfeld **Hinzufügen eines Backend-Pools** in Azure Front Door Service an.

![Hinzufügen eines Back-End-Pool Dialogfelds](./media/CDN_BackendPool.png)

### <a name="set-up-rules-in-azure-front-door-service"></a>Richten Sie Regeln in Azure Front Door Service ein

Um eine Routingregel im Azure Front Door Service einzurichten, führen Sie die folgenden Schritte aus.

1. Eine Routingregel hinzufügen.
1. Geben Sie im Feld **Name** **Standard** ein.
1. Wählen Sie im Feld **Angenommenes Protokoll** **HTTP und HTTPS** aus.
1. Im Feld **Frontend-Hosts** geben Sie den Text **dynamics-ecom-tenant-name.azurefd.net** ein.
1. Unter **Muster der Übereinstimmung** im oberen Feld, geben Sie **/\*** ein.
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
1. Unter **Muster zur Übereinstimmung** im oberen Feld **/\_msdyn365/\_scnr/\***.
1. Unter **Arbeitsplandetails** legen Sie die Option **Arbeitsplantyp** auf **Vorwärts** fest.
1. Wählen Sie im Feld **Backend-Pool** **ecom-backend**.
1. In der Feldgruppe **Weiterleitungsprotokoll** wählen Sie die Option **Abgleichungsanforderung** aus.
1. Hier können Sie die Option **URL neu schreiben** auf **Deaktiviert** festlegen.
1. Hier können Sie die Option **Zwischenspeichern** auf **Deaktiviert** festlegen.
1. Wählen Sie im Feld **Verhalten für Zwischenspeicherabfagezeichenfolge**, **Jede einzelne URL zwischenspeichern** aus.
1. In der Feldgruppe **Dynamische Kompression** wählen Sie die Option **Aktiviert** aus.

Die folgende Abbildung zeigt das Dialogfeld **Hinzufügen einer Regel** in Azure Front Door Service an.

![Fügen Sie ein Regeldialogfeld hinzu](./media/CDN_CachingRule.png)

Nachdem diese Erstkonfiguration bereitgestellt wurde, müssen Sie Ihre benutzerdefinierten Domäne der Konfiguration für Azure Front Door Service hinzufügen. Um die benutzerdefinierte Domäne hinzuzufügen (beispielsweise `www.fabrikam.com`), müssen Sie einen kanonischen Namen (CNAME) für die Domäne konfigurieren.

Die folgende Abbildung zeigt das Dialogfeld **CNAME Konfiguration** in Azure Front Door Service an.

![CNAME Konfigurationsdialogfeld](./media/CNAME_Configuration.png)

> [!NOTE]
> Wenn die Domänen, die Sie verwenden möchten, bereits aktiv ist, unterstützt Kontakt die Aktivierung dieser Domäne mit Azure Front Door Service, um einen Test einzurichten.

Sie können Azure Front Door Service verwenden, um die Zertifikate zu verwalten, oder Sie können eine eigene Bescheinigung für die benutzerdefinierte Domäne verwenden.

Die folgende Abbildung zeigt das Dialogfeld **Benutzerdefinierte Domäne HTTPS** in Azure Front Door Service an.

![Benutzerdefiniertes Dialogfeld der Domäne HTTPS](./media/Custom_Domain_HTTPS.png)

Ihr CDN sollte jetzt ordnungsgemäß konfiguriert werden, so dass sie mit der Commerce Site verwendet werden kann.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Ihren Domänennamen konfigurieren](configure-your-domain-name.md)

[Bereitstellen einer neuen E-Commerce-Webseite](deploy-ecommerce-site.md)

[Onlineshopkanal einrichten](online-stores.md)

[E-Commerce-Site erstellen](create-ecommerce-site.md)

[Zuordnen einer Onlinewebseite zu einem Kanal](associate-site-online-store.md)

[Verwalten von robots.txt-Dateien](manage-robots-txt-files.md)

[URL-Weiterleitungen in großen Mengen hochladen](upload-bulk-redirects.md)

[Einrichten eines B2C-Mandanten in Commerce](set-up-B2C-tenant.md)

[Einrichten angepasster Seiten für die Benutzeranmeldungen](custom-pages-user-logins.md)

[Konfigurieren Sie mehrere B2C-Mandanten in einer Commerce-Umgebung](configure-multi-B2C-tenants.md)

[Standortbasierte Shop-Erkennung aktivieren](enable-store-detection.md)
