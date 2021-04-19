---
title: Dienst für Steuerberechnungen (Vorschau)
description: In diesem Thema werden der Gesamtumfang und die Funktionen des Steuerberechnungsdienstes erläutert.
author: wangchen
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 518d3fda7b97e55d23beea6a1ba0e50b44a7aa0e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818223"
---
# <a name="tax-calculation-service-preview"></a>Dienst für Steuerberechnungen (Vorschau)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Der Steuerberechnungsdienst ist ein hyperskalierbarer mandantenfähiger Dienst, mit dem die Global Tax Engine den Steuerermittlungs- und -berechnungsprozess automatisieren und vereinfachen kann. Das Steuermodul ist vollständig konfigurierbar. Zu den Elementen, die konfiguriert werden können, gehören unter anderem das steuerpflichtige Datenmodell, der Steuercode, die Steueranwendbarkeitsmatrix und die Steuerberechnungsformel. Das Steuermodul läuft auf der Microsoft Azure-Hauptserviceplattform und bietet moderne Technologie und exponenzielle Skalierbarkeit.

Der Steuerberechnungsdienst ist in Dynamics 365 Finance und Dynamics 365 Supply Chain Management integriert. Schließlich wird er auch in Dynamics 365 Project Operations, Dynamics 365 Commerce und andere Anwendungen von Erstanbietern und Drittanbietern integriert.

Der Steuerberechnungsdienst ist ein Microsoft-basiertes Steuermodul, das exponenzielle Skalierbarkeit bietet. Er kann bei der Ausführung folgender Aufgaben helfen:

- Konfigurieren Sie den Steuerberechnungsdienst über den Regulatory Configuration Service (RCS). RCS ist eine erweiterte Version des Designers für elektronische Berichterstellung (ER) und als eigenständiger Dienst verfügbar.
- Konfigurieren Sie die Steuermatrix so, dass Steuercodes und Steuersätze automatisch ermittelt werden.
- Konfigurieren Sie die Steuermatrix so, dass die Steuerregistrierungsnummer automatisch ermittelt wird.
- Konfigurieren Sie den Steuerberechnungsdesigner so, dass Formeln und Bedingungen definiert werden.
- Teilen Sie die Steuerermittlungs- und -berechnungslösung für verschiedene juristische Personen.

Um den Steuerberechnungsdienst zu verwenden, installieren Sie das Steuerberechnungsdienst-Add-In aus Ihrem Projekt in Microsoft Dynamics Lifecycle Services (LCS). Schließen Sie dann die Einrichtung in RCS ab und aktivieren Sie den Steuerberechnungsdienst in Finance und Supply Chain Management. Weitere Informationen finden Sie unter [Erste Schritte mit dem Steuerdienst](https://go.microsoft.com/fwlink/?linkid=2138482).

## <a name="availability"></a>Verfügbarkeit

Der Steuerberechnungsdienst ist nur in Sandbox-Umgebungen und für ausgewählte Kunden über ein öffentliches Vorschauprogramm verfügbar. Schließlich wird es für alle Kunden und in Produktionsumgebungen allgemein verfügbar sein.

Neue Funktionen werden weiterhin im Steuerberechnungsdienst bereitgestellt. Lesen Sie daher regelmäßig die aktuellste Dokumentation, um mehr über die Abdeckung und den Umfang der unterstützten Funktionen zu erfahren.

Der Steuerberechnungsdienst wird in den folgenden Azure-Regionen bereitgestellt. Er wird auch in weiteren Azure-Regionen bereitgestellt, je nach Kundenanforderungen:

- Vereinigte Staaten
- Europa
- Frankreich
- Vereinigtes Königreich

> [!NOTE]
> Der Steuerberechnungsdienst unterstützt keine lokalen Bereitstellungen von Dynamics 365. Frühere Versionen wie Dynamics AX 2012 werden ebenfalls nicht unterstützt.

## <a name="feature-highlights"></a>Besondere Funktionen

- Eine konfigurierbare Steuermatrix für die automatische Ermittlung und Berechnung der Steuer
- Unterstützung für mehrere Mehrwertsteuer (MwSt.)-Erfassungsnummern
- Umlagerungsauftragsunterstützung für Steuerermittlung und -berechnung
- Umlagerungsauftragsunterstützung zur Ermittlung mehrerer Mehrwertsteuererfassungsnummern

## <a name="supported-transactions"></a>Unterstützte Transaktionen

Der Steuerberechnungsdienst kann nach juristischer Person und Transaktion aktiviert werden. Folgende Transaktionen werden unterstützt:

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

[Erste Schritte mit dem Steuerdienst](https://go.microsoft.com/fwlink/?linkid=2138482)

[Mehrere Mehrwertsteuererfassungsnummern](https://go.microsoft.com/fwlink/?linkid=2153387)

[Unterstützung für Steuerfunktionen für Umlagerungsaufträge](https://go.microsoft.com/fwlink/?linkid=2153388)

[So erstellen Sie eine Erweiterung im Steuerdienst](https://go.microsoft.com/fwlink/?linkid=2138483)
