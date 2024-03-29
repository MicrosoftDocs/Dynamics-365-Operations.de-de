---
title: Implementierungsoptionen für das Content Delivery Network
description: In diesem Artikel werden die verschiedenen Optionen für die Implementierung des Content Delivery Network (CDN) zur Verwendung mit Microsoft Dynamics 365 Commerce-Umgebungen beschrieben. Diese Optionen umfassen native, von Commerce bereitgestellte Instanzen von Azure Front Door und kundeneigene Instanzen von Azure Front Door.
author: BrianShook
ms.date: 07/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.14
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: de2ecab86809af3ace64ba06956f00137d254ab7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275146"
---
# <a name="content-delivery-network-implementation-options"></a>Implementierungsoptionen für das Content Delivery Network

[!include [banner](includes/banner.md)]

In diesem Artikel werden die verschiedenen Optionen für die Implementierung des Content Delivery Network (CDN) zur Verwendung mit Microsoft Dynamics 365 Commerce-Umgebungen beschrieben. Diese Optionen umfassen native, von Commerce bereitgestellte Instanzen von Azure Front Door und kundeneigene Instanzen von Azure Front Door.

Commerce-Kunden haben mehrere Möglichkeiten, wenn sie überlegen, welchen CDN-Dienst sie in ihrer Commerce-Umgebung verwenden möchten. Commerce wird mit grundlegender Azure Front Door-Unterstützung veröffentlicht, die grundlegende Hosting- und benutzerdefinierte Domänenanforderungen abdeckt. Für Unternehmen, die mehr Kontrolle und spezifischere Sicherheitsfunktionen wünschen, wie z. B. eine Web Application Firewall (WAF), besteht die beste Option darin, entweder eine kundeneigene Instanz von Azure Front Door oder einen externen CDN-Dienst zu verwenden.

Die folgenden drei CDN-Implementierungsoptionen können in Commerce-Umgebungen verwendet werden:

- Die von Commerce bereitgestellte Azure Front Door-Instanz
- Eine kundeneigene Instanz von Azure Front Door (für mehr Kontrolle und zusätzliche Sicherheitsfunktionen)
- Ein externer CDN-Dienst

Alle drei CDN-Implementierungsoptionen liefern nur dynamischen HTML-Inhalt aus benutzerdefinierten Domänen. Commerce verarbeitet automatisch alle JavaScripts, Cascading Style Sheets (CSS), Bilder, Videos und andere statische Inhalte über von Microsoft verwaltete CDNs. Die von Ihnen ausgewählte Option bestimmt die Betriebsfunktionen, Steuerungsfunktionen und zusätzlichen Sicherheitsfunktionen, die verfügbar sind.

Die folgende Abbildung zeigt eine Übersicht über die Commerce-Architektur.

![Commerce – Architekturübersicht.](media/Commerce_CDN-Option_ComparisonModels.png)

Weitere Informationen zum Einrichten einer Instanz von Azure Front Door für Ihre Commerce-Site finden Sie unter [CDN-Unterstützung hinzufügen](add-cdn-support.md).

## <a name="use-the-commerce-provided-azure-front-door-instance"></a>Die von Commerce bereitgestellte Azure Front Door-Instanz verwenden

In der folgenden Tabelle sind die Vor- und Nachteile der Verwendung der von Commerce bereitgestellten Instanz von Azure Front Door zum Verwalten von Inhaltsendpunkten aufgeführt.

| Vorteile | Nachteile |
|------|------|
| <ul><li>Die Instanz ist in den Commerce-Kosten enthalten.</li><li>Da die Instanz vom Commerce-Team verwaltet wird, ist weniger Wartung erforderlich und es gibt gemeinsame Einrichtungsschritte.</li><li>Die von Azure gehostete Infrastruktur ist skalierbar, sicher und zuverlässig.</li><li>Das SSL-Zertifikat (Secure Sockets Layer) erfordert eine einmalige Einrichtung und wird automatisch erneuert.</li><li>Die Instanz wird vom Commerce-Team auf Fehler und Anomalien überwacht.</li></ul> | <ul><li>Ein WAF wird nicht unterstützt.</li><li>Es gibt keine spezifischen Anpassungen oder Einstellungsregulierungen.</li><li>Die Instanz hängt vom Commerce-Team für Aktualisierungen oder Änderungen ab.</li><li>Für Apex-Domänen ist eine separate Azure Front Door-Instanz erforderlich, und für die Integration von Apex-Domänen in Azure DNS ist zusätzliche Arbeit erforderlich.</li><li>Dem Kunden wird keine Telemetrie über Antworten pro Sekunde (RPS) oder die Fehlerrate zur Verfügung gestellt.</li></ul> |

Die folgende Abbildung zeigt die Architektur der von Commerce bereitgestellten Azure Front Door-Instanz.

![Von Commerce bereitgestellte Azure Front Door-Instanz.](media/Commerce_CDN-Option_CommerceFrontDoor.png)

## <a name="use-a-customer-owned-azure-front-door-instance"></a>Kundeneigene Azure Front Door-Instanz verwenden

In der folgenden Tabelle sind die Vor- und Nachteile der Verwendung der kundeneigenen Instanz von Azure Front Door zum Verwalten von Inhaltsendpunkten aufgeführt.

| Vorteile | Nachteile |
|------|------|
| <ul><li>Die Einrichtung ist sicher und einfach zu verwalten.</li><li>Die von Azure gehostete Infrastruktur ist skalierbar, sicher und zuverlässig.</li><li>Die Instanz ermöglicht die WAF-Integration und detaillierte Regelsteuerungen für eine genauere Sicherheit, die speziell für Ihre Site optimiert wurde.</li><li>Die Instanz ermöglicht eine genauere Steuerung von SSL-Zertifikaten (sowohl im Kundenbesitz als auch von Azure Front Door verwaltet) und der Domänenverknüpfung.</li><li>Die Instanz bietet eine Apex-Domänenlösung, wenn sie direkt mit Azure DNS gekoppelt ist.</li><li>Telemetrie und Alarmierung sind vorhanden.</li><li>Das SSL-Zertifikat erfordert eine einmalige Einrichtung und wird automatisch erneuert.</li></ul> | <ul><li>Die Instanz ist selbstverwaltet.</li><li>Ein erster Wissensaufbau ist erforderlich.</li></ul> |

Die folgende Abbildung zeigt eine Commerce-Infrastruktur, die eine kundeneigene Azure Front Door-Instanz enthält.

![Commerce-Infrastruktur, die eine kundeneigene Azure Front Door-Instanz enthält.](media/Commerce_CDN-Option_CustomerOwnedAzureFrontDoor.png)

## <a name="use-an-external-cdn-service"></a>Externen CDN-Dienst verwenden

In der folgenden Tabelle sind die Vor- und Nachteile der Verwendung eines externen CDN-Dienstes zum Verwalten von Inhaltsendpunkten aufgeführt.

| Vorteile | Nachteile |
|------|------|
| <ul><li>Diese Option ist nützlich, wenn die vorhandene Domäne bereits auf einem externen CDN gehostet ist.</li><li>WAF: Abhängig vom externen Anbieter.</li></ul> | <ul><li>Ein separater Vertrag und zusätzliche Kosten sind erforderlich.</li><li>SSL kann zusätzliche Kosten verursachen.</li><li>Da der Dienst von der Azure-Cloud-Struktur getrennt ist, muss zusätzliche Infrastruktur verwaltet werden.</li><li>Der Dienst erfordert möglicherweise längere Zeitinvestitionen in Endpunkt- und Sicherheitseinstellungen.</li><li>Der Dienst ist selbstverwaltet.</li><li>Der Dienst ist selbstüberwacht.</li></ul> |

Die folgende Abbildung zeigt eine Commerce-Infrastruktur, die einen externen CDN-Dienst enthält.

![Commerce-Infrastruktur mit einem externen CDN-Dienst.](media/Commerce_CDN-Option_ExternalFrontDoor.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Hinzufügen von Unterstützung für ein Content Delivery Network (CDN)](add-cdn-support.md)
