---
title: Entfernte oder veraltete Funktionen in Dynamics 365 Supply Chain Management
description: In diesem Artikel werden die Funktionen beschrieben, die entfernt wurden oder entfernt werden sollen in Dynamics 365 Supply Chain Management.
author: kamaybac
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 722b34e89a54715db39259549c11a78d69d2b4d3
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739869"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Entfernte oder veraltete Funktionen in Dynamics 365 Supply Chain Management

[!include [banner](../includes/banner.md)]

Dieser Artikel wird aktualisiert, sobald neue entfernte oder veraltete Funktionen dokumentiert werden Dynamics 365 Supply Chain Management.

- Eine Funktion *entfernt* ist nicht mehr im Produkt verfügbar.
- Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.

Diese Liste soll ihnen dabei helfen, diese entfernten und veralteten Funktionen bei Ihrer eigenen Planung zu berücksichtigen.

> [!NOTE]
> Ausführliche Informationen über Objekte in Apps für Finanzen und Betrieb finden Sie in den [Technischen Referenzberichten](/dynamics/s-e/). Sie können die verschiedenen Versionen dieser Berichte vergleichen, um sich über Objekte zu informieren, die in den einzelnen Versionen der Apps für Finanzen und Betrieb geändert oder entfernt wurden.

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10029-release"></a>Entfernte oder veraltete Funktionen in Supply Chain Management 10.0.29

### <a name="stock-transfer-orders-that-have-tax-on-the-transfer-price"></a>Umlagerungsaufträge mit Steuer auf den Verrechnungspreis

| &nbsp;  | &nbsp;  |
|---|---|
| **Grund für veralteten Zustand/Entfernung** | Die Funktion [Umlagerungsaufträge mit Steuer auf den Verrechnungspreis](../../finance/localizations/apac-ind-gst-stock-transfer-transactions.md) wird durch [Umlagerungsaufträge für Indien](../../finance/localizations/apac-ind-stock-transfer.md) ersetzt. |
| **Ersetzt durch eine andere Funktion?**   | Ja, die Funktion [Umlagerungsaufträge mit Steuer auf den Verrechnungspreis](../../finance/localizations/apac-ind-gst-stock-transfer-transactions.md) wird durch [Umlagerungsaufträge für Indien](../../finance/localizations/apac-ind-stock-transfer.md) ersetzt. |
| **Betroffene Produktbereiche** | Supply Chain Management - Bestand |
| **Bereitstellungsoption** | Cloud und lokal |
| **Status** | <p>Ist veraltet.  Die Funktion: *Umlagerungsaufträge, die Steuern auf den Transferpreis enthalten* wird nicht mehr mit Fehlerkorrekturen und Sicherheitskorrekturen unterstützt.</p><p>Ab April 2023 werden Kunden gebeten, die verbesserte Funktionalität *Umlagerungsaufträge für Indien* zu nutzen. Nach Oktober 2023 wird die Funktion *Umlagerungsaufträge, die Steuern auf den Transferpreis enthalten* nicht mehr verfügbar sein, und die Kunden werden gebeten, auf die verbesserte Funktionalität *Umlagerungsaufträge für Indien* umzusteigen.</p><p>Weitere Informationen finden Sie unter [Umlagerungsaufträge für Indien ](../../finance/localizations/apac-ind-stock-transfer.md).</p> |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10019-release"></a>Entfernte oder veraltete Funktionen in Supply Chain Management 10.0.19

### <a name="job-card-device"></a>Einzelvorgangslistengerät

| &nbsp;  | &nbsp;  |
|---|---|
| **Grund für veralteten Zustand/Entfernung** | Das [Jobkartengerät](../production-control/config-job-card-device.md) wird durch die neue [Produktionsausführungsoberfläche](../production-control/production-floor-execution-configure.md) ersetzt. |
| **Ersetzt durch eine andere Funktion?**   | Ja, das [Jobkartengerät](../production-control/config-job-card-device.md) soll durch die neue [Produktionsausführungsoberfläche](../production-control/production-floor-execution-configure.md) ersetzt werden. |
| **Betroffene Produktbereiche** | Supply Chain Management – Steuerelement für die Produktion |
| **Bereitstellungsoption** | Cloud und lokal |
| **Status** | Veraltet. Das Jobkartengerät wird mit Fehler- und Sicherheitskorrekturen unterstützt, aber Funktionserweiterungen werden nicht mehr zur Verfügung gestellt. Nach April 2022 wird das Jobkarten-Gerät nicht mehr unterstützt und die Kunden werden aufgefordert, auf die neue Produktionsausführungsoberfläche umzusteigen. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10018-release"></a>Entfernte oder veraltete Funktionen in Supply Chain Management 10.0.18

### <a name="supply-chain-management--warehousing-the-warehouse-app"></a><a name="wma"></a>Supply Chain Management- Lagerverwaltung (die Lager App)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Ab April 2021 ist *Supply Chain Management – Warehousing* (die Warehouse App) veraltet und wird ab April 2022 nicht mehr unterstützt. Es wird jetzt durch die *Warehouse Management Mobile App* ersetzt, die mit Version 10.0.17 von Supply Chain Management veröffentlicht wurde. Die neue App ist ein vollständiger Ersatz, verwendet jedoch dasselbe zugrunde liegende Framework, was die Migration vereinfacht. Bei Bedarf können die beiden Apps nebeneinander verwendet werden, damit Benutzer sich schrittweise anpassen können, während sie lernen, die neue App zu verwenden.<br><br>Weitere Informationen über die neue Warehouse Management Mobile App finden Sie unter [Mobile Warehouse Management-Anwendung](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-application) und unter [Warehouse Management Mobile App installieren und Verbindung herstellen](../warehousing/install-configure-warehouse-management-app.md). |
| **Ersetzt durch eine andere Funktion?**   | Ja, wird durch die neue Warehouse Management Mobile App ersetzt. |
| **Betroffene Produktbereiche**         | Supply Chain Management – Lagerort-App |
| **Bereitstellungsoption**              | Cloud und lokal |
| **Status**                         | Veraltet. Die Lagerort-App wird mit Fehler- und Sicherheitskorrekturen unterstützt, es werden jedoch keine Funktionserweiterungen mehr bereitgestellt. Nach April 2022 wird die alte Lagerort-App nicht mehr unterstützt und Kunden werden aufgefordert, auf die neue Warehouse Management Mobile App umzusteigen. Die alte Lagerort-App wird dann aus dem Microsoft Store und dem Google Play Store entfernt.  |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10015-release"></a>Entfernte oder veraltete Funktionen in Supply Chain Management 10.0.15

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11 Unterstützung für Dynamics 365 wird außer Betrieb genommen

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Ab Dezember 2020 wird die Unterstützung von Microsoft Internet Explorer 11 für alle Dynamics 365-Produkte veraltet sein und Internet Explorer 11 wird nach August 2021 nicht mehr unterstützt werden.<br><br>Dies wirkt sich auf Kunden aus, die Dynamics 365-Produkte verwenden, die für die Verwendung über eine Internet Explorer 11-Schnittstelle entworfen wurden. Nach August 2021 wird Internet Explorer 11 für solche Dynamics 365-Produkte nicht mehr unterstützt. |
| **Ersetzt durch eine andere Funktion?**   | Wir empfehlen den Kunden den Übergang zu Microsoft Edge.|
| **Betroffene Produktbereiche**         | Alle Dynamics 365-Produkte |
| **Bereitstellungsoption**              | Alle|
| **Status**                         | Veraltet. Internet Explorer 11 wird nach August 2021 nicht mehr unterstützt.|

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-manufacturing-scenarios"></a>Verwendung der integrierten Supply Chain Management-Masterprogrammplanung für Fertigungsszenarien

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Um die Leistung zu verbessern und die SQL-Datenbanklast während der Ausführung der Masterplanung zu minimieren, wird das integrierte Supply Chain Management-Masterplanungsmodul durch die Planungsoptimierung ersetzt. Die Planungsoptimierung ermöglicht schnelle Planungsausführungen, die auch während der Geschäftszeiten durchgeführt werden können. Dadurch können Planer sofort auf Änderungen in der Nachfrage oder bei den Planungsparametern reagieren. |
| **Ersetzt durch eine andere Funktion?**   | Ja, die Planungsoptimierung wird das bestehende integrierte Supply Chain Management-Masterplanungsmodul ersetzen. |
| **Betroffene Produktbereiche**         | Supply Chain Management – Masterplanung |
| **Bereitstellungsoption**              | Nur Cloud. Planungsoptimierung wird bei lokalen Bereitstellungen nicht unterstützt. |
| **Status**                         | Veraltet. Ab dem 1. April 2022 werden Fertigungsszenarien nicht mehr für die integrierte Produktprogrammplanungsmodul von Supply Chain Management unterstützt. Ab diesem Datum wird Microsoft die gesamte aktive Entwicklung von Fertigungsszenarien für das integrierte Planungsmodul einstellen, keine neuen Funktionen veröffentlichen und nur kritische Fehlerbehebungen veröffentlichen. Nach diesem Datum müssen alle Unternehmen, die Unterstützung für Fertigungsszenarien benötigen, die Planungsoptimierung für ihre Hauptplanungsberechnungen verwenden. Die Planungsoptimierung wird Fertigungsszenarien voraussichtlich bis Oktober 2022 vollständig unterstützen. (Weitere Informationen finden Sie unter [Übersicht über veraltete Masterplanung](../master-planning/deprecated-master-planning-overview.md) .)<br><br>Unternehmen, die Supply Chain Management lokal bereitstellen, können nach April 2022 weiterhin das integrierte Produktprogrammplanungsmodul für Fertigungsszenarien verwenden. Es werden jedoch keine weiteren Funktionserweiterungen bereitgestellt. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Entfernte oder veraltete Funktionen in Supply Chain Management 10.0.11

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>Verwenden des integrierten Supply Chain Management-Masterplanungsmoduls für Verteilungszenarien

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Um die Leistung zu verbessern und die SQL-Datenbanklast während der Ausführung der Masterplanung zu minimieren, wird das integrierte Supply Chain Management-Masterplanungsmodul durch die Planungsoptimierung ersetzt. Die Planungsoptimierung ermöglicht schnelle Planungsausführungen, die auch während der Geschäftszeiten durchgeführt werden können. Dadurch können Planer sofort auf Änderungen in der Nachfrage oder bei den Planungsparametern reagieren. |
| **Ersetzt durch eine andere Funktion?**   | Ja, die Planungsoptimierung wird das bestehende integrierte Supply Chain Management-Masterplanungsmodul ersetzen. |
| **Betroffene Produktbereiche**         | Supply Chain Management – Masterplanung |
| **Bereitstellungsoption**              | Nur Cloud. Planungsoptimierung wird bei lokalen Bereitstellungen nicht unterstützt. |
| **Status**                         | Veraltet. Ab dem 1. April 2021 werden Vertriebsszenarien nicht mehr mit der eingebauten Dynamics 365 Supply Chain Management-Masterprogrammplanung unterstützt. Für Verteilungsszenarien müssen Kunden die Planungsoptimierung für Masterplanungsberechnungen verwenden. (Weitere Informationen finden Sie unter [Übersicht über veraltete Masterplanung](../master-planning/deprecated-master-planning-overview.md) .) Kunden mit lokalen Bereitstellungen von Dynamics 365 Supply Chain Management verwenden möglicherweise weiterhin das Supply Chain Management-Masterplanungsmodul für Verteilungsszenarien nach April 2021. Es werden jedoch keine weiteren Funktionserweiterungen bereitgestellt. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Frühere Ankündigungen über entfernte oder veraltete Funktionen

Um mehr über Funktionen zu erfahren, die in früheren Versionen entfernt oder veraltet sind, siehe [Entfernte oder veraltete Funktionen in früheren Versionen](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

