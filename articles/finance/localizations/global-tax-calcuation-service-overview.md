---
title: Steuerberechnung (Vorschau)
description: In diesem Thema werden der Gesamtumfang und die Funktionen der Steuerberechnung erläutert.
author: wangchen
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 9daa6e001200d03a2639974fb6de618d77ddf09d
ms.sourcegitcommit: cb282e8d2306ab71adf80a84346a6863d2d019e8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2021
ms.locfileid: "6184100"
---
# <a name="tax-calculation-preview"></a>Steuerberechnung (Vorschau)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Die Steuerberechnung ist ein hyperskalierbarer mandantenfähiger Dienst, mit dem die Global Tax Engine den Steuerermittlungs- und -berechnungsprozess automatisieren und vereinfachen kann. Das Steuermodul ist vollständig konfigurierbar. Zu den Elementen, die konfiguriert werden können, gehören unter anderem das steuerpflichtige Datenmodell, der Steuercode, die Steueranwendbarkeitsmatrix und die Steuerberechnungsformel. Das Steuermodul läuft auf der Microsoft Azure-Hauptserviceplattform und bietet moderne Technologie und exponenzielle Skalierbarkeit.

Die Steuerberechnung ist in Dynamics 365 Finance und Dynamics 365 Supply Chain Management integriert. Schließlich wird er auch in Dynamics 365 Project Operations, Dynamics 365 Commerce und andere Anwendungen von Erstanbietern und Drittanbietern integriert.

> [!IMPORTANT]
> Wenn Sie den Steuerberechnungsdienst aktivieren, werden einige Vorgänge an verwandten Daten möglicherweise in einem anderen Rechenzentrum als dem Rechenzentrum ausgeführt, das Ihre Dienstdaten verwaltet. Überprüfen Sie die [Geschäftsbedingungen](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md), bevor Sie den Steuerberechnungsdienst aktivieren. Datenschutz ist uns sehr wichtig. Weiteres erfahren Sie in unserer [Datenschutzerklärung](https://go.microsoft.com/fwlink/?LinkId=521839).

Die Steuerberechnung ist ein Microsoft-basiertes Steuermodul, das exponenzielle Skalierbarkeit bietet. Er kann bei der Ausführung folgender Aufgaben helfen:

- Konfigurieren Sie die Steuerberechnung über den Regulatory Configuration Service (RCS). RCS ist eine erweiterte Version des Designers für elektronische Berichterstellung (ER) und als eigenständiger Dienst verfügbar.
- Konfigurieren Sie die Steuermatrix so, dass Steuercodes und Steuersätze automatisch ermittelt werden.
- Konfigurieren Sie die Steuermatrix so, dass die Steuerregistrierungsnummer automatisch ermittelt wird.
- Konfigurieren Sie den Steuerberechnungsdesigner so, dass Formeln und Bedingungen definiert werden.
- Teilen Sie die Steuerermittlungs- und -berechnungslösung für verschiedene juristische Personen.

Um den Steuerberechnungsdienst zu verwenden, installieren Sie das Steuerberechnungsdienst-Add-In aus Ihrem Projekt in Microsoft Dynamics Lifecycle Services (LCS). Schließen Sie dann die Einrichtung in RCS ab und aktivieren Sie den Steuerberechnungsdienst in Finance und Supply Chain Management. Weitere Informationen finden Sie unter [Erste Schritte mit dem Steuerdienst](./global-get-started-with-tax-calculation-service.md).

## <a name="availability"></a>Verfügbarkeit

Die Steuerberechnung ist nur in Sandbox-Umgebungen und für ausgewählte Kunden über ein öffentliches Vorschauprogramm verfügbar. Schließlich wird es für alle Kunden und in Produktionsumgebungen allgemein verfügbar sein.

Da laufend neue Funktionen bereitgestellt werden, lesen Sie regelmäßig die aktuellste Dokumentation, um mehr über die Abdeckung und den Umfang der unterstützten Funktionen zu erfahren.

Die Steuerberechnung wird in den folgenden Azure-Regionen bereitgestellt. Er wird auch in weiteren Azure-Regionen bereitgestellt, je nach Kundenanforderungen:

- Vereinigte Staaten
- Europa

> [!NOTE]
> Die Steuerberechnung unterstützt keine lokalen Bereitstellungen von Dynamics 365. Frühere Versionen wie Dynamics AX 2012 werden ebenfalls nicht unterstützt.

## <a name="feature-highlights"></a>Besondere Funktionen

- Eine konfigurierbare Steuermatrix für die automatische Ermittlung und Berechnung der Steuer
- Unterstützung für mehrere Steuernummern
- Umlagerungsauftragsunterstützung für Steuerermittlung und -berechnung
- Umlagerungsauftragsunterstützung zur Ermittlung mehrerer Steuernummern

## <a name="supported-transactions"></a>Unterstützte Transaktionen

Die Steuerberechnung kann nach juristischer Person und Transaktion aktiviert werden. Folgende Transaktionen werden unterstützt:

- Verkaufsprozess

    - Verkaufsangebot
    - Auftrag
    - Bestätigung
    - Kommissionierliste
    - Lieferschein
    - Verkaufsrechnung
    - Gutschrift
    - Rücklieferung
    - Sonstige Kopfgebühren
    - Sonstige Positionsbelastungen

- Kaufprozess

    - Bestellung
    - Bestätigung
    - Zugangsliste
    - Produktzugang
    - Einkaufsrechnung
    - Sonstige Kopfgebühren
    - Sonstige Positionsbelastungen
    - Gutschrift
    - Rücklieferung
    - Bestellanforderung
    - Sonstige Belastung pro Bestellanforderungsposition
    - Angebotsanforderung
    - Sonstige Kopfgebühr für Angebotsanforderung
    - Sonstige Belastung pro Angebotsanforderungsposition

- Bestandsprozess

    - Umlagerungsauftrag – versenden
    - Umlagerungsauftrag – empfangen

## <a name="related-resources"></a>Zugehörige Ressourcen

[Erste Schritte mit dem Steuerdienst](./global-get-started-with-tax-calculation-service.md)

[Mehrere Mehrwertsteuererfassungsnummern](./emea-multiple-vat-registration-numbers.md)

[Unterstützung für Steuerfunktionen für Umlagerungsaufträge](./tasks/tax-feature-support-for-transfer-order.md)

[So erstellen Sie eine Erweiterung im Steuerdienst](./tax-service-add-data-fields-tax-integration-by-extension.md)
