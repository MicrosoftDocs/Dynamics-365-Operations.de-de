---
title: Kundenportal für Dynamics 365 Supply Chain Management Übersicht (enthält Video)
description: In diesem Artikel wird das Kundenportal vorgestellt und erläutert, wer es verwenden soll und wie es funktioniert.
author: Henrikan
ms.date: 06/16/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: ff074e62489fe74f0c2de6dae0e02d1da7e7f6ae
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901907"
---
# <a name="customer-portal-for-dynamics-365-supply-chain-management-overview"></a>Kundenportal für Dynamics 365 Supply Chain Management Überblick

[!include [banner](../includes/banner.md)]


## <a name="what-is-the-customer-portal"></a>Was ist das Kundenportal?

Moderne Supply-Chain-Systeme setzen auf Integration. Sie erfordern, dass Inventar, Kundennachfrage und Verkaufsabteilungen integriert werden, anstatt sich in separaten Silos zu befinden. Das Kundenportal hilft Organisationen, die Microsoft Dynamics 365 Supply Chain Management ausführen, diese Integration zu verbessern und die Kunden effektiver auf dem Laufenden zu halten.

Das Kundenportal ist eine [Power Apps Portale](/powerapps/maker/portals/overview) Vorlage, mit der Unternehmen eine extern ausgerichtete B2B-Website (Business-to-Business) für Szenarien erstellen können, die sich auf die Auftragsabwicklung beziehen. Die Vorlage verwendet [Duales Schreiben](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md), Supply Chain Management und Power Apps Portale, mit denen externe Unternehmenskunden Daten aus der Dynamics 365-Umgebung des Unternehmens anzeigen und erstellen können.

Die Kundenportalvorlage hat Anpassungsfunktionen, über die die Portale von Power Apps verfügen. Die Vorlage kann einfach geändert werden, um die Marke des Unternehmens darzustellen, die Funktionalität zu erweitern und die Benutzererfahrung zu ändern. Alle Funktionen, die die Vorlage sofort bietet, können nach Bedarf geändert werden.

> [!IMPORTANT]
> An sich wird nicht erwartet, dass die Vorlage vollständig funktionsfähig ist. Es dient lediglich als Enabler für Kunden, die eine nach außen gerichtete Website erstellen möchten, damit Unternehmenskunden mit Daten aus dem Supply Chain Management interagieren können.

> [!NOTE]
> Die Dokumentation zum Kundenportal richtet sich an Administratoren, Anpasser und Systemintegratoren, die das Kundenportal für eine Supply Chain Management-Installation einrichten. Es verwendet die Begriffe _Kunde_ und _Benutzer_, um Personen zu beschreiben, die Kunden der Organisation sind, die Supply Chain Management ausführt, und die das endgültige Portal selbst verwenden.

## <a name="video"></a>-Video

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4ylwW]

Das [Übersicht über die Debitorenportalvorlage in Dynamics 365 Supply Chain Management](https://youtu.be/nPrqoLuHfV8)-Video (siehe oben) ist enthalten in der [Wiedergabeliste von Finanzen und Betrieb](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) verfügbar auf YouTube.

## <a name="who-should-use-it"></a>Wer sollte es benutzen?

Das Kundenportal richtet sich an Unternehmen, die Supply Chain Management betreiben und folgende Merkmale aufweisen:

- Sie möchten eine nach außen gerichtete Website erstellen, die Informationen zur Auftragsabwicklung (z. B. Auftragsstatus oder Kontoinformationen) direkt von ihrem Supply Chain Management-System an ihre Unternehmenskunden übermittelt.
- Sie wechseln von Dynamics AX 2012 zu Supply Chain Management und verwendet zuvor das [AX 2012 Kunden-Self-Service-Portal](/dynamicsax-2012/appuser-itpro/about-the-customer-self-service-portal).

Die folgenden Arten von Organisationen sind **keine** guten Kandidaten für die Implementierung des Kundenportals:

- Unternehmen, die eine Website für Nicht-Unternehmenskunden erstellen möchten. Diese Unternehmen sollten in Betracht ziehen, eine [Dynamics 365 Commerce E-Commerce-Website](../../commerce/create-ecommerce-site.md).
- Unternehmen, die bereits eine bestehende nutzen Power Apps Portale Website für einen ähnlichen Zweck. Diese Unternehmen erhalten keine zusätzlichen Vorteile aus dem Kundenportal. Das Kundenportal wird als Vorlage geliefert, die als Leitfaden und Ausgangspunkt für Kunden dient, die die Punkte zwischen Dualen Schreiben, Supply Chain Management und Power Apps Portal verbinden möchte. Wenn Sie bereits eine Website eingerichtet haben, die diesem Zweck dient, können Sie durch die Verwendung der Kundenportalvorlage zur erneuten Bereitstellung dieser Website möglicherweise nicht viel Wert gewinnen.

## <a name="how-does-it-work"></a>Wie funktioniert das?

Das Kundenportal wird als Power Apps Portal Vorlage bereitgestellt. Es hängt von dualem Schreiben und Power Apps Portalen ab.

[Power Apps Portal](/powerapps/maker/portals/overview) ist eine Funktion, mit der eine nach außen gerichtete Website erstellen können, bei der sich Personen außerhalb des Unternehmens anmelden können. Für die Erstellung von Portalen ist nur wenig bis gar keine Codierung erforderlich. Das Kundenportal ist eine von vielen [Dynamics 365-Portalvorlagen](/powerapps/maker/portals/portal-templates#environment-with-model-driven-apps-in-dynamics-365), die von Microsoft erhältlich sind.

[Duales Schreiben](/powerapps/maker/portals/overview) ist ein vordefiniertes Infrastrukturprodukt, das eine Interaktion zwischen Kundenbindungs-Apps und Apps für Finanzen und Betrieb in Quasi-Echtzeit ermöglicht. Duales Schreiben bietet eine eng gekoppelte, bidirektionale Integration zwischen Apps für Finanzen und Betrieb und Microsoft Dataverse. Deshalb bietet dieser automatisierte Datenfluss eine integrierte Benutzererfahrung über die Anwendungen hinweg. Das Kundenportal hängt von Tabellen ab, die mit dualem Schreiben synchronisiert sind. Bevor Daten aus dem Supply Chain Management im Kundenportal angezeigt werden können, muss duales Schreiben für alle entsprechenden Tabellen aktiviert sein.

![Kundenportalabhängigkeiten.](media/customer-portal-elements.png "Kundenportalabhängigkeiten")

Das Kundenportal dient als Ausgangspunkt für Organisationen, die Power Apps Portal zum Erstellen einer nach außen gerichteten Website verwenden möchten, die Daten aus ihrer Supply Chain Management-Installation verwendet. Es hilft Unternehmen dabei, duales Schreibe, Supply Chain Management und Power Apps Portal zu organisieren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]