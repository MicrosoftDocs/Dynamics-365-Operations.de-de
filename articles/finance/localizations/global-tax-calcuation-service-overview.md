---
title: Übersicht über die Steuerberechnung
description: In diesem Artikel werden der Gesamtumfang und die Funktionen der Steuerberechnung erläutert.
author: EricWangChen
ms.date: 03/02/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.search.form: TaxIntegrationTaxServiceParameters
ms.openlocfilehash: c6dabb9d2aae6f1fc759c40f870c66304d7f7c8d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270664"
---
# <a name="tax-calculation-overview"></a>Übersicht über die Steuerberechnung

[!include [banner](../includes/banner.md)]

Die Steuerberechnung ist ein hyperskalierbarer mandantenfähiger Dienst, mit dem die Global Tax Engine den Steuerermittlungs- und -berechnungsprozess automatisieren und vereinfachen kann. Das Steuermodul ist vollständig konfigurierbar. Zu den Elementen, die konfiguriert werden können, gehören unter anderem das steuerpflichtige Datenmodell, der Steuercode, die Steueranwendbarkeitsmatrix und die Steuerberechnungsformel. Das Steuermodul läuft auf der Microsoft Azure-Hauptserviceplattform und bietet moderne Technologie und exponenzielle Skalierbarkeit.

Die Steuerberechnung ist in Dynamics 365 Finance und Dynamics 365 Supply Chain Management integriert. Schließlich wird er auch in Dynamics 365 Project Operations, Dynamics 365 Commerce und andere Anwendungen von Erstanbietern und Drittanbietern integriert.

> [!IMPORTANT]
> Wenn Sie die Steuerberechnung aktivieren, werden einige Vorgänge an zugehörigen Daten möglicherweise in einem anderen Rechenzentrum durchgeführt als dem, das Ihre Servicedaten verwaltet. Lesen Sie die [Bedingungen und Konditionen](https://go.microsoft.com/fwlink/?linkid=2156043), bevor Sie die Steuerberechnung aktivieren. Datenschutz ist uns sehr wichtig. Weiteres erfahren Sie in unserer [Datenschutzerklärung](https://go.microsoft.com/fwlink/?LinkId=521839).

Tax Calculation ist eine Microservice-basierte Steuer-Engine, die exponentielle Skalierbarkeit bietet und Sie bei den folgenden Aufgaben unterstützen kann:

- Automatische Ermittlung der korrekten Mehrwertsteuergruppe, der Mehrwertsteuergruppe für Elemente und der Steuerkennzeichen durch einen erweiterten Ermittlungsmechanismus.
- Unterstützung mehrerer Steuerregistrierungsnummern in einer juristischen Entität und automatische Bestimmung der korrekten Steuerregistrierungsnummer bei steuerpflichtigen Transaktionen.
- Unterstützung der Steuerermittlung, -berechnung, -buchung und -abrechnung für Umlagerungsaufträge.
- Definieren Sie konfigurierbare Steuerberechnungsformeln und -bedingungen für Ihre spezifischen Geschäftsanforderungen.
- Nutzen Sie die Lösung zur Steuerermittlung und -berechnung über juristische Entitäten hinweg, um Wartungsaufwand zu sparen und Fehler zu vermeiden.
- Unterstützen Sie die Ermittlung von Debitor- und Kreditor-Steuernummern.
- Unterstützt die Ermittlung von Listencodes.
- Unterstützen Sie Steuerberechnungsparameter auf der Ebene der Steuerjurisdiktion.

Um Tax Calculation zu verwenden, installieren Sie das Add-In Tax Calculation aus Ihrem Projekt in Microsoft Dynamics Lifecycle Services. Vervollständigen Sie dann die Einrichtung in [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/), und aktivieren Sie Tax Calculation in Finance und Supply Chain Management. Weitere Informationen finden Sie unter [Erste Schritte mit dem Steuerdienst](global-get-started-with-tax-calculation-service.md).

## <a name="availability"></a>Verfügbarkeit

Tax Calculation ist allgemein in produktiven Umgebungen für alle Kunden ab der Version 10.0.21 verfügbar.

Es werden weiterhin neue Funktionen ausgeliefert. Prüfen Sie regelmäßig den aktuellen Release-Plan, um sich über die Abdeckung und den Umfang der unterstützten Funktionen zu informieren.

Die Steuerberechnung wird in den folgenden Azure-Regionen bereitgestellt. Weitere Azure-Geografien werden auf Basis der Kundenanforderungen hinzugefügt.

- Asien-Pazifik
- Australien
- Brasilien
- Kanada
- Europa
- Frankreich
- Indien
- Japan
- Südafrika
- Schweiz
- Vereinigte Arabische Emirate
- Vereinigtes Königreich
- USA

> [!NOTE]
> Steuerberechnung unterstützt keine früheren Versionen von Dynamics 365, wie z.B. Dynamics AX 2012, oder Lokal-Bereitstellungen von Dynamics 365.

## <a name="versions"></a>Versionen
Wir empfehlen Ihnen, Ihre Steuerberechnungskonfiguration mit der Version zu importieren und einzurichten, die Ihrer Finance- oder Supply Chain Management-Version entspricht.

| Finance‑ oder Supply Chain Management-Version | Steuerkonfigurationsversion               |
| --------------- | --------------------------------------- |
| 10.0.18         | Steuerkonfiguration - Europa 30.12.82     |
| 10.0.19         | Steuerberechnungs-Konfiguration 36.38.193 |
| 10.0.20         | Steuerberechnungs-Konfiguration 40.43.208 |
| 10.0.21         | Steuerberechnungs-Konfiguration 40.48.215 |
| 10.0.22         | Steuerberechnungs-Konfiguration 40.48.215 |
| 10.0.23         | Steuerberechnungs-Konfiguration 40.50.221 |
| 10.0.24         | Steuerberechnungs-Konfiguration 40.50.225 |
| 10.0.25         | Steuerberechnungs-Konfiguration 40.50.225 |
| 10.0.26         | Steuerberechnungs-Konfiguration 40.54.234 |
| 10.0.27         | Steuerberechnungs-Konfiguration 40.54.234 |
| 10.0.28         | Steuerberechnungs-Konfiguration 40.54.234 |


## <a name="data-flow"></a>Datenfluss

Hier ist ein Überblick über den Datenflussprozess für die Steuerberechnung. 

1. Zeigen Sie in RCS die Konfigurationen für das Modell des steuerpflichtigen Belegs und die Konfigurationen für die Modellzuordnung an und importieren Sie sie. Wenn Sie Konfigurationen für ein erweitertes Szenario erweitern müssen, lesen Sie [Datenfelder in Steuerkonfigurationen hinzufügen](tax-service-add-data-fields-tax-configurations.md).
2. In RCS erstellen oder pflegen Sie steuerliche Funktionen. Sie können Steuerfunktionen verwenden, um Steuersätze und Regeln für die Anwendbarkeit von Steuern zu pflegen.
3. Nachdem die Einrichtung der Steuerfunktionen abgeschlossen ist, veröffentlichen Sie die Steuerkonfigurationen und Steuerfunktionen aus RCS in das globale Repository.
4. Wählen Sie in Finance, welche Version der Einrichtung von Steuerfunktionen für eine bestimmte juristische Entität verwendet werden soll.
5. Führen Sie in Finance und Supply Chain Management Transaktionen wie gewohnt durch. Wenn eine Steuerberechnung benötigt wird, sammelt der Client Informationen aus der Transaktion, wie z.B. dem Verkaufsauftrag oder der Bestellung, und verpackt die Informationen als Payload. Dann wird eine Anfrage zur Berechnung der Steuer gesendet.
6. Die Anforderung zur Steuerberechnung wird vom Client empfangen und die Berechnung wird abgeschlossen. Das Steuerergebnis wird dann an den Client zurückgesendet.
7. Der Dynamics 365 Client empfängt das Steuerergebnis und stellt das Ergebnis der Steuerberechnung auf einer Umsatzsteuerseite dar.

## <a name="supported-transactions"></a>Unterstützte Transaktionen

Die Steuerberechnung kann durch Transaktionen aktiviert werden. 

Die folgenden Transaktionen werden in Version 10.0.21 unterstützt: 

- Verk.

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

- Kaufen

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

- Bestand

    - Umlagerungsauftrag – versenden
    - Umlagerungsauftrag – empfangen

Die folgenden Transaktionen werden in Version 10.0.23 unterstützt: 

- Freitextrechnung

Die folgenden Transaktionen werden in Version 10.0.26 unterstützt: 

- Allgemeine Erfassungen
- Kreditorenrechnungserfassung

Die folgenden Transaktionen werden in Version 10.0.28 unterstützt: 

- Kreditorzahlungserfassung
- Debitorzahlungserfassung

Die folgenden Transaktionen werden in Version 10.0.29 unterstützt: 

- Periodische Erfassung

## <a name="supported-countriesregions"></a>Unterstützte Länder/Regionen

Die Steuerberechnung kann mit den unterstützten Lokalisierungsfunktionen in den folgenden Ländern/Regionen für die Hauptadresse einer juristischen Person ausgeführt werden: 

In Version 10.0.21 unterstützt:

- Österreich
- Belgien
- Dänemark
- Estland
- Finnland
- Frankreich
- Deutschland
- Ungarn
- Island
- Irland
- Italien
- Lettland
- Litauen
- Niederlande
- Norwegen
- Polen
- Schweden
- Schweiz
- Vereinigtes Königreich
- USA

In Version 10.0.22 unterstützt:

- Australien
- Bahrain
- Kanada
- Ägypten
- Hongkong (SAR)
- Kuwait
- Neuseeland
- Oman
- Katar
- Saudi-Arabisch
- Südafrika
- Vereinigte Arabische Emirate

In Version 10.0.23 unterstützt:

- Thailand
- Japan
- Malaysia
- Singapur

In Version 10.0.24 unterstützt:

- Mexiko

In Version 10.0.26 unterstützt:

- China
- Tschechische Republik
- Spanien

Für alle Länder/Regionen, die nicht von Microsoft lokalisiert wurden, kann die Steuerberechnung auch aktiviert und mit anderen globalen Funktionen ausgeführt werden.

## <a name="related-resources"></a>Zugehörige Ressourcen

[Erste Schritte mit dem Steuerdienst](./global-get-started-with-tax-calculation-service.md)

[Mehrere Mehrwertsteuererfassungsnummern](./emea-multiple-vat-registration-numbers.md)

[Unterstützung für Steuerfunktionen für Umlagerungsaufträge](./tasks/tax-feature-support-for-transfer-order.md)

[So erstellen Sie eine Erweiterung im Steuerdienst](./tax-service-add-data-fields-tax-integration-by-extension.md)
