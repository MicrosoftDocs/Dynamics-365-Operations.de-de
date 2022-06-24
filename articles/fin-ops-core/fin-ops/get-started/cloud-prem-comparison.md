---
title: Vergleich von Cloud- und On-Premises-Funktionen
description: Der Artikel zeigt Funktionen, die in der Cloud und lokal unterstützt werden.
author: sericks007
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 89563
ms.assetid: ''
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2017-11-29
ms.dyn365.ops.version: Platform update 9
ms.openlocfilehash: 4096089978032f150bf6d711711a948cf1d3232f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879774"
---
# <a name="comparison-of-cloud-and-on-premises-features"></a>Vergleich von Cloud- und On-Premises-Funktionen

[!include [banner](../includes/banner.md)]

In diesem Artikel wird ein Vergleich der Funktionen in der Cloud und lokal für die folgenden Anwendungen gezeigt:

- [Dynamics 365 Finance](cloud-prem-comparison.md#dynamics-365-finance)
- [Dynamics 365 Supply Chain Management](cloud-prem-comparison.md#dynamics-365-supply-chain-management)
- [Dynamics 365 Commerce](cloud-prem-comparison.md#dynamics-365-commerce)
- [Dynamics 365 Human Resources](cloud-prem-comparison.md#dynamics-365-human-resources)

Informationen zu [Entwicklungs- und Verwaltungsfunktionen](cloud-prem-comparison.md#development-and-administration-features) sind ebenfalls enthalten.

Die folgenden Tabellen führen die Anwendungsbereiche auf. Cloud und lokaler Support wird für die Funktion als Ganzes aufgeführt. Wo bestimmte Funktionen im Bereich gesamthaft unterschieden werden, werden die Funktionen in einer separaten Position in der Funktionsspalte aufgeführt.

## <a name="dynamics-365-finance"></a>Dynamics 365 Finance

| **Bereich**             | **Funktion**                | **Cloud** | **Lokal** |
|---------------------|-----------------------------|-----------|-----------------|
| Compliance und Bescheinigungen        |                                                                                           | Ja       | Ja             |
|                                      | SOC 1 Type 1 Zertifizierung                                                                | Ja       | Nein              |
| Datenverwaltung und -integration      |                                                                                           | Ja       | Ja             |
|                                      | Exportieren von Daten in Ihrem eigenen Data Warehouse                                                    | Ja       | Ja             |
|                                      | Aktivieren des Exports von stufenweisen Aktualisierungen an einer Datenentität                                 | Ja       | Ja             |
|                                      | Datenintegrationen                                                                         | Ja       | Ja             |
| Dokumentverwaltung                  |                                                                                           | Ja       | Ja             |
| Finanzverwaltung                 |                                                                                           | Ja       | Ja             |
| Hilfe                                 |                                                                                           | Ja       | Nein              |
| Personalverwaltung                      |                                                                                           | Ja       | Ja             |
| Intelligence                         |                                                                                           | Ja       | Ja             |
|                                      | Elektronische Berichterstellung (ER, Elektronic Reporting)                                                                 | Ja       | Ja             |
|                                      | EB: Integration in LCS                                                                  | Ja       | Nein              |
|                                      | EB: Integration in SharePoint                                                           | Ja       | Nein              |
|                                      | EB: Integration in Regulatory Configuration Services (RCS)                              | Ja       | Nein              |
|                                      | EB: Verwendet lokales Dateisystem als Speicherung von EB-Konfigurationen, auf die über EB-Repositorys zugegriffen werden kann | Nein        | Ja             |
|                                      | Integration mit PowerBI.com                                                              | Ja       | Nein              |
|                                      | Integration mit PowerBI Desktop                                                          | Nein        | Ja             |
|                                      | Analytische Arbeitsbereiche                                                                     | Ja       | Nein              |
|                                      | Intelligente Geschäftsprozesse: Empfehlungen                                             | Ja       | Nein              |
|                                      | Power BI-Berichte mit OData mithilfe des Power BI-Desktops oder des Excel PowerQuery-Tools genehmigen    | Ja       | Nein              |
|                                      | SQL Server Reporting Services unterstützt die Skalierung nach Außen                                 | Ja       | Ja             |
|                                      | Telemetrie wird in die Cloud übertragen                                                   | Ja       | Nein              |
| Lifecycle Services                   |                                                                                           | Ja       | Ja             |
|                                      | Konfigurierbare Geschäftsprozesse                                                           | Ja       | Nein              |
| Lokalisierungen                        |                                                                                           | Ja       | Ja             |
| Mobile App Arbeitsbereiche und Plattform |                                                                                           | Ja       | Ja             |
| Office-Integration                   |                                                                                           | Ja       | Ja             |
| Organisationsverwaltung          |                                                                                           | Ja       | Ja             |
| Lohnabrechnung                              |                                                                                           | Ja       | Ja             |
|                                      | Direktüberweisung                                                                            | Ja       | Nein              |
| Projektverwaltung und Buchhaltung    |                                                                                           | Ja       | Ja             |
| Sicherheit                             |                                                                                           | Ja       | Ja             |
| Serviceverwaltung                   |                                                                                           | Ja       | Ja             |
| Webclient                           |                                                                                           | Ja       | Ja             |
|                                      | Aufgabenaufzeichnung - Aufgabenaufzeichnung aus der BPM-Bibliothek speichern oder laden                         | Ja       | Nein              |
| Support                              |                                                                                           | Ja       | Ja             |
|                                      | Zugriff auf Support über das Menü Hilfe und Support                                             | Ja       | Nein              |
|                                      | Geschäftsereignisse                                                                           | Ja       | Ja (entweder ist eine Internetverbindung erforderlich, oder es müssen benutzerdefinierte Endpunkte implementiert werden, um Geschäftsereignisse innerhalb des Intranets zu senden/zu empfangen)              |

## <a name="dynamics-365-supply-chain-management"></a>Dynamics 365 Supply Chain Management 

| **Bereich**                | **Funktion**             | **Cloud** | **Lokal** |
|-------------------------|-------------------|-----------|-----------------|
| Anlagenverwaltung                     |                                                                                           | Ja       | Ja             |
| Compliance und Bescheinigungen        |                                                                                           | Ja       | Ja             |
|                                      | SOC 1 Type 1 Zertifizierung                                                                | Ja       | Nein              |
| Kostenrechnung                      |                                                                                           | Ja       | Ja             |
|                                      | Kostenrechnungs-Inhaltspaket für Power BI                                                 | Ja       | Nein              |
|                                      | Kostenrechnungsarbeitsbereich für mobile App                                                  | Ja       | Nein              |
| Kostenverwaltung                      |                                                                                           | Ja       | Ja             |
|                                      | Kostenrechnungs-Inhaltspaket für Power BI                                                 | Ja       | Nein              |
| Datenverwaltung und -integration      |                                                                                           | Ja       | Ja             |
|                                      | Konfigurations-getriebene Erweiterung                                                            | Ja       | Nein              |
|                                      | Exportieren von Daten in Ihrem eigenen Data Warehouse                                                    | Ja       | Ja             |
|                                      | Aktivieren des Exports von stufenweisen Aktualisierungen an einer Datenentität                                 | Ja       | Ja             |
|                                      | Datenintegrationen                                                                         | Ja       | Ja             |
| Dokumentverwaltung                  |                                                                                           | Ja       | Ja             |
| Hilfe                                 |                                                                                           | Ja       | Nein              |
| Intelligence                         |                                                                                           | Ja       | Ja             |
|                                      | Elektronische Berichterstellung (ER, Elektronic Reporting)                                                                 | Ja       | Ja             |
|                                      | EB: Integration in LCS                                                                  | Ja       | Nein              |
|                                      | EB: Integration in SharePoint                                                           | Ja       | Nein              |
|                                      | EB: Integration in Regulatory Configuration Services (RCS)                              | Ja       | Nein              |
|                                      | EB: Verwendet lokales Dateisystem als Speicherung von EB-Konfigurationen, auf die über EB-Repositorys zugegriffen werden kann | Nein        | Ja             |
|                                      | Integration mit PowerBI.com                                                              | Ja       | Nein              |
|                                      | Integration mit PowerBI Desktop                                                          | Nein        | Ja             |
|                                      | Analytische Arbeitsbereiche                                                                     | Ja       | Nein              |
|                                      | Intelligente Geschäftsprozesse: Empfehlungen                                             | Ja       | Nein              |
|                                      | Power BI-Berichte mit OData mithilfe des Power BI-Desktops oder des Excel PowerQuery-Tools genehmigen    | Ja       | Nein              |
|                                      | SQL Server Reporting Services unterstützt die Skalierung nach Außen                                 | Ja       | Ja             |
|                                      | Telemetrie wird in die Cloud übertragen                                                   | Ja       | Nein              |
| Lagerverwaltung                 |                                                                                           | Ja       | Ja             |
| Lifecycle Services                   |                                                                                           | Ja       | Ja             |
|                                      | Konfigurierbare Geschäftsprozesse                                                           | Ja       | Nein              |
| Lokalisierungen                        |                                                                                           | Ja       | Ja             |
| Fertigung                        |                                                                                           | Ja       | Ja             |
| Produktprogrammplanung und Bedarfsplanung      |                                                                                           | Ja       | Ja             |
| Planungsoptimierung                |                                                                                           | Ja       | Nein              |
| Mobile App Arbeitsbereiche und Plattform |                                                                                           | Ja       | Ja             |
| Office-Integration                   |                                                                                           | Ja       | Ja             |
| Organisationsverwaltung          |                                                                                           | Ja       | Ja             |
| Beschaffung             |                                                                                           | Ja       | Ja             |
|                                      | Angebot für die Bestellanforderungsposition aus dem externen Katalog                                   | Ja       | Nein              |
|                                      | Power BI-Berichte zur Einkaufs- und Ausgabenanalyse                                                  | Ja       | Nein              |
| Produktinformationsverwaltung       |                                                                                           | Ja       | Ja             |
| Produktmasterdaten                  |                                                                                           | Ja       | Ja             |
| Produktion                           |                                                                                           | Ja       | Ja             |
|                                      | Power BI-Berichte zur Produktionsleistung                                                   | Ja       | Nein              |
| Projektverwaltung und -verrechnung    |                                                                                           | Ja       | Ja             |
| Verk.                                |                                                                                           | Ja       | Ja             |
|                                      | Power BI-Berichte zur Umsatz- und Rentabilitätsleistung                                      | Ja       | Nein              |
| Sicherheit                             |                                                                                           | Ja       | Ja             |
| Serviceverwaltung                   |                                                                                           | Ja       | Ja             |
| Lieferkettenverwaltung              |                                                                                           | Ja       | Ja             |
| Transportverwaltung            |                                                                                           | Ja       | Ja             |
| Kreditor-Kooperation                 |                                                                                           | Ja       | Nein              |
| Lagerortverwaltung                 |                                                                                           | Ja       | Ja             |
|                                      | Mobile App am Lagerort                                                                      | Ja       | Ja             |
|                                      | Power BI-Berichte zur Lagerung                                                              | Ja       | Nein              |
| Webclient                           |                                                                                           | Ja       | Ja             |
|                                      | Aufgabenaufzeichnung - Aufgabenaufzeichnung aus der BPM-Bibliothek speichern oder laden                         | Ja       | Nein              |
| Unterstützung                              |                                                                                           | Ja       | Ja             |
|                                      | Zugriff auf Support über das Menü Hilfe und Support                                             | Ja       | Nein              |

## <a name="dynamics-365-commerce"></a>Dynamics 365 Commerce 

Eine Liste der Funktionen, die in lokalen Implementierungen verfügbar sind, finden Sie unter [Commerce-Funktionen, die in lokalen Implementierungen verfügbar sind](../../../commerce/retail-onprem.md).

## <a name="dynamics-365-human-resources"></a>Dynamics 365 Human Resources 

| **Bereich**         | **Funktion**         | **Cloud** | **Lokal** |
|------------------|---------------------|-----------|-----------------|
| Alle Personalverwaltungsbereiche | Alle Personalverwaltungsfunktionen | Ja       | Nein              |

## <a name="development-and-administration-features"></a>Entwicklungs- und Verwaltungsfunktionen

| **Bereich**                   | **Funktion**                               | **Cloud** | **Lokal** |
|----------------------------|-------------------------------------------|-----------|-----------------|
| Produzieren und testen             |                                           | Ja       | Ja             |
| Erweiterbarkeit              |                                           | Ja       | Ja             |
| Überwachung und Telemetrie   |                                           | Ja       | Ja             |
| Plattformkompatibilität     |                                           | Ja       | Ja             |
| Wartung                  |                                           | Ja       | Ja             |
|                            | Wartungsumgebungen                    | Ja       | Nein              |
| Ablaufverfolgungs-Parser               |                                           | Ja       | Ja             |
| PerfTimer                  |                                           | Ja       | Ja\*           |
| Upgrade durchführen                    |                                           | Ja       | Ja             |
|                            | Upgrade durchführen                                   | Ja       | Nein              |
|                            | Aktualisierung und Support für frühere Versionen | Ja       | Nein              |
| Visual Studio-Entwicklung  |                                           | Ja       | Ja             |

\* In lokalen Umgebungen zeigt PerfTimer nur Ergebnisse für den Client an.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
