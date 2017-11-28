---
title: Veraltete Funktionen
description: In diesem Thema werden die Funktionen beschrieben, die entfernt wurden oder entfernt werden sollen.
author: sericks007
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 21821
ms.assetid: 31019808-4cbf-47d7-b1ba-d791db4281ae
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 6
ms.translationtype: HT
ms.sourcegitcommit: 9ee81bbdd22fed4ef6ea97080fe1f6b3d82bcaf5
ms.openlocfilehash: ee051bbf50a6124fe1700a244b36b5f9c599e714
ms.contentlocale: de-de
ms.lasthandoff: 11/06/2017

---

# <a name="deprecated-features"></a>Veraltete Funktionen

[!include[banner](../includes/banner.md)]

Dieses Thema beschreibt Funktionen, die aus Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, entfernt wurden, oder für die vorgesehen ist, sie zu entfernen.

## <a name="features-that-have-been-deprecated-in-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-with-platform-update-8"></a>Funktionen, die in Dynamics 365 for Finance and Operations, Enterprise Edition (Juli 2017) mit Plattform Update 8 veraltet wurden

### <a name="warehouse-mobile-devices-portal"></a>Portal für mobile Geräte für das Lager

Portal für mobile Geräte für das Lager (Warehouse Mobile Devices Portal – WMDP) war eine eigenständige Komponente, die für lokale Selbstbereitstellung vorgesehen war. Diese Komponente wird von Microsoft Dynamics 365 for Finance and Operations, Enterprise edition nicht mehr unterstützt. Eine systemeigener App, die die Benutzererfahrung verbessert, hat die Funktionalität von WMDP ersetzt. 

|                                  |                                                 |
|----------------------------------|-------------------------------------------------|
| **Grund für Abschreibung**       | Doppelte Funktionen.                        |
| **Ersetzt durch eine andere Funktion?** | Ja. Diese Funktion wurde von Finance and Operations - Warehousing ersetzt. Weitere Informationen zu Einrichtung und Voraussetzungen finden Sie unter [Microsoft Dynamics 365 for Finance and Operations - Warehousing einrichten und konfigurieren](../../supply-chain/warehousing/install-configure-warehousing-app.md). |
| **Betroffene Module**             | Lagerortverwaltung und Transportverwaltung |

### <a name="advanced-bank-reconciliation-matching-rule-for-manual-matching"></a>Erweiterte Abgleichsregel für Bankabstimmung für den manuelle Abgleich

Eine Abgleichsregel, die verwendet wurde, um ein Bankdokument beim manuellen Abgleich von Dokumenten der Auszugsposition im Abstimmungsarbeitsblatt auszuwählen und zu markieren

|                                  |                                                                                        |
|----------------------------------|----------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Begrenzte Verwendung.                                                                         |
| **Ersetzt durch eine andere Funktion?** | Nr. Funktionen zur Spaltenfilterung sollten verwendet werden, um nach Dokumente für die Abstimmung zu suchen. |
| **Betroffene Module**             | Bargeld- und Bankverwaltung                                                               |

### <a name="windows-8-tablet-app"></a>Windows 8-Tablet-App

Die bereitgestellte Funktionen der Windows 8-Tablet-App für Speseneintrag und Genehmigung.

|                                  |                                                                                          |
|----------------------------------|------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Finance and Operations ist mit Tablets kompatibel. Die Tablet-App wird nicht mehr benötigt. |
| **Ersetzt durch eine andere Funktion?** | Nr.                                                                                      |
| **Betroffene Module**             | Spesenverwaltung                                                                       |


## <a name="features-that-have-been-deprecated-in-dynamics-365-for-operations-1611-with-platform-update-3"></a>Funktionen, die in Dynamics 365 for Operations 1611 mit Plattformaktualisierung 3 veraltet sind

### <a name="aeb-payment-formats-for-spain"></a>AEB-Zahlungsformate für Spanien

Die überlegenen Bancario Zahlungsformate vom werden verwendet, um Rimessedateien für Debitoren- und Kreditorenzahlungen zu senden. Der Inhalt dieser Formate wird von der Asociación Española de Banca bestimmt. Er deckt Cuaderno 19, 32, 58, 34 aus.

|                              |                                                                          |
|------------------------------|--------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Die Zahlungsformate werden nicht mehr verwendet.                                  |
| **Ersetzt durch eine andere Funktion?** | Ja, ISO20022 Banküberweisung und Lastschriftverfahren für Spanien |
| **Betroffene Module**             | Kreditorenkonten, Debitoren                                    |

### <a name="bank-payments-transfer-for-lithuania"></a>Zahlung per Banküberweisung für Litauen

Zahlungsüberweisungen werden mithilfe von des Exportformats der Zahlungsüberweisung (LT) für Litauen erstellt und gedruckt. Der litauische Markt verwendet LITAS, das einheitliche Electronic Banking-System seit dem Jahre 2005.

|                              |                                                            |
|------------------------------|------------------------------------------------------------|
| **Grund für Abschreibung**       | Die Zahlungsformate werden nicht mehr verwendet.                    |
| **Ersetzt durch eine andere Funktion?** | Ja, Kredittransferzahlungsformat ISO20022 für Litauen |
| **Betroffene Module**             | Kreditorenkonten                                           |

### <a name="bbs-direkte-remittering-payment-formats-for-norway"></a>Zahlungsformate BBS Direkte Remittering für Norwegen

Zahlungsformate BBS Direkte Remittering enthalten Debitorenzahlungsinkassoexport (Direktbelastung) und Rückholnachrichtenimport.

|                              |                                                                                                                                                                |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Die Zahlungsformate werden nicht mehr verwendet.                                                                                                                        |
| **Ersetzt durch eine andere Funktion?** | Das AvtaleGiro-Debitorenzahlungsformat für Norwegen kann verwendet werden, um Direktbelastungsnachrichten zu generieren. Rückholnachrichtenimport wird in künftigen Versionen implementiert. |
| **Betroffene Module**             | Kreditorenkonten, Debitoren                                                                                                                          |

### <a name="chart-of-accounts-tool-for-spain"></a>Kontenplan-Tool für Spanien

Dieses Tool wird verwendet, wenn ein Kontenplan in Spanien größere Änderungen erfordert. Benutzer können einen neuen Kontenplan in Microsoft Excel oder Textformat importieren und können auch Finanzaufstellungen importieren.

|                              |                |
|------------------------------|----------------|
| **Grund für Abschreibung**       | Begrenzte Verwendung  |
| **Ersetzt durch eine andere Funktion?** | Nr.             |
| **Betroffene Module**             | Hauptbuch |

### <a name="dom80-payment-format-for-belgium"></a>Dom80 Zahlungsformat für Belgien

Ältere Zahlungsformat Belgeien für Zahlungsinkasso (Direktbelastung).

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| **Grund für Abschreibung**      | Das Zahlungsformat wird nicht mehr verwendet.                  |
| **Ersetzt durch eine andere Funktion?** | Ja; ISO 20022, Lastschriftzahlungsformat für Belgien |
| **Betroffene Module**            | Debitorenkonten                                    |

### <a name="dtaezag-payment-formats-for-switzerland"></a>DTA/EZAG Zahlungsformate für die Schweiz

DTA-/EZAG-Formate sind im ESR-System integriert, da sie eine Referenznummer führen können. Da die Referenznummern nicht obligatorisch ist, können diese Formate für die Verarbeitung alle beliebigen Kreditorenzahlungen verwendet werden. Diese Formate werden von Unternehmen verwendet, die ein Bankkonto außerhalb von "Postfinance" haben.

|                              |                                                              |
|------------------------------|--------------------------------------------------------------|
| **Grund für Abschreibung**       | Die Zahlungsformate werden nicht mehr verwendet.                      |
| **Ersetzt durch eine andere Funktion?** | Ja, ISO20022 Kredittransferzahlungsformat für die Schweiz |
| **Betroffene Module**             | Kreditorenkonten                                             |

### <a name="edifact-dirdeb-payment-format-for-austria"></a>EDIFACT-DIRDEB Zahlungsformat für Österreich

EDIFACT-DIRDEB Zahlungsformat für Zahlungsinkasso (Direktbelastung).

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| **Grund für Abschreibung**       | Das Zahlungsformat wird nicht mehr verwendet.                  |
| **Ersetzt durch eine andere Funktion?** | Ja; ISO 20022, Lastschriftzahlungsformat für Österreich |
| **Betroffene Module**             | Debitorenkonten                                    |

### <a name="edivat-for-belgium"></a>EDIVAT für Belgien

EDIVAT ist ein veralteter belgischer Standard für elektronische Meldungen über sicheren Mailverkehr. Microsoft Dynamics AX 2012 bewahrt die schreibgeschützte Lösung, um auf die historische Daten zuzugreifen.

|                              |                                      |
|------------------------------|--------------------------------------|
| **Grund für Abschreibung**       | Die Funktionalität wird nicht mehr verwendet. |
| **Ersetzt durch eine andere Funktion?** | Nr.                                   |
| **Betroffene Module**             | Hauptbuch                       |

### <a name="egiro-edifact-cremul-payment-import-format-for-norway"></a>eGiro EDIFACT CREMUL Zahlungsimportformat für Norwegen

eGiro basiert auf den internationalen UN EDIFACT CREMUL (Mehrere Gutschriftsanzeigen) Standard, der zum automatischen Buchen von Debitorenzahlungen verwendet wird. In Microsoft Dynamics AX wird eGiro als Debitorenzahlungsimportformat implementiert.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Das Zahlungsformat wird nicht mehr verwendet.                                                     |
| **Ersetzt durch eine andere Funktion?** | Nr. Das Format wird durch ISO 20022 Auszugsimportformate in künftigen Versionen ersetzt. |
| **Betroffene Module**             | Debitorenkonten                                                                       |

### <a name="external-inventory-for-poland"></a>Externer Bestand für Polen

Nachweis von Waren, die von einem Kreditor für Verkäufe ohne Einkauf verwendet werden. Waren, die im externen Bestand verwaltet werden, haben keinen Einfluss auf den Standardbestand und können verkauft und automatisch gekauft werden. Dieser Prozess erstellt echte Bestandumlagerungen.

|                              |                                                 |
|------------------------------|-------------------------------------------------|
| **Grund für Abschreibung**       | Ersetzt durch eine andere Funktion                     |
| **Ersetzt durch eine andere Funktion?** | Ja, die zentrale eingehende Lieferungsfunktionalität |
| **Betroffene Module**             | Kreditorenkonto, Bestandverwaltung          |

### <a name="financial-reports-generator-for-eastern-europe"></a>Finanzberichtsgenerator für Osteuropa

Ein Tool, um die Datenerfassung für die Berechnung und die Steuererklärungen einzurichten und Daten in XLS- und DOC-Berichtsvorlagen zu exportieren

|                              |                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Begrenzte Verwendung                                                                            |
| **Ersetzt durch eine andere Funktion?** | Nr. Das Tool wird durch die elektronische Berichterstellungskonfigurationen in künftigen Versionen ersetzt. |
| **Betroffene Module**             | Hauptbuch                                                                           |

### <a name="import-of-customer-payment-transactions-for-finland"></a>Import von Buchungen für Debitorenzahlungen für Finnland

Sie können ein Importformat für finnische Zahlungen auswählen, das Debitorenzahlungsbuchungen aus einer externen Datei importiert, die von der Bank bereitgestellten wird.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Das Zahlungsformat wird nicht mehr verwendet.                                                     |
| **Ersetzt durch eine andere Funktion?** | Nr. Das Format wird durch ISO 20022 Auszugsimportformate in künftigen Versionen ersetzt. |
| **Betroffene Module**             | Debitorenkonten                                                                       |

### <a name="import-of-payment-transactions-into-a-general-ledger-journal-for-finland"></a>Import von Zahlungsbuchungen in eine Hauptbucherfassung für Finnland

Ein Sonderformat für Finnland zum Import von Buchhaltungsbuchungen in das Hauptbuch.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Das Zahlungsformat wird nicht mehr verwendet.                                                     |
| **Ersetzt durch eine andere Funktion?** | Nr. Das Format wird durch ISO 20022 Auszugsimportformate in künftigen Versionen ersetzt. |
| **Betroffene Module**             | Debitorenkonten                                                                       |

### <a name="integration-with-isabel-synchronized-cis-for-belgium"></a>Integration mit Isabel synchronisiert (CIS) für Belgien

Isabel ist das Framework für Electronic Banking in Europa und kein tatsächlicher Standard in Belgien.

|                              |                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Integration mit Isabel-Kunden ist eingestellt.                                                                |
| **Ersetzt durch eine andere Funktion?** | Nr. Die Zahlungsformate, die nicht mehr verwendet werden, werden durch Transferzahlungsformat des Kredits ISO20022 für Belgien ersetzt. |
| **Betroffene Module**             | Kreditorenkonten                                                                                                     |

### <a name="modifications-in-the-chart-of-accounts-and-accounting-rules-for-spain"></a>Änderungen im Kontenplan und bei den Buchhaltungsvorschriften für Spanien

Diese Funktion wurde für Änderungen im Kontenplan und bei den Buchhaltungsvorschriften in Spanien verwendet. Führt Konten zusammen, um alte Kontenpläne in die neuen Kontenpläne zu transformieren und das vorherige Geschäftsjahr mit dem neuen Geschäftsjahr zu vergleichen, selbst wenn sie an verschiedene Kontonummern gebucht wurden.

|                              |                |
|------------------------------|----------------|
| **Grund für Abschreibung**       | Begrenzte Verwendung  |
| **Ersetzt durch eine andere Funktion?** | Nr.             |
| **Betroffene Module**             | Hauptbuch |

### <a name="pagamento-fornittori-vendor-payment-format"></a>Kreditorenzahlungsformat Pagamento Fornittori

Veraltetes italienisches Zahlungsformat für Kreditübertragungen.

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| **Grund für Abschreibung**       | Das Zahlungsformat wird nicht mehr verwendet.                  |
| **Ersetzt durch eine andere Funktion?** | Ja, ISO20022 Kredittransferzahlungsformat für Italien |
| **Betroffene Module**             | Kreditorenkonten                                       |

### <a name="payment-export-formats-for-estonia"></a>Zahlungsexportforamte für Estland

Die Formate Telehansa und Teleservide werden für den Bankzahlungsexport verwendet.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| **Grund für Abschreibung**      | Die Zahlungsformate werden nicht mehr verwendet.                  |
| **Ersetzt durch eine andere Funktion?** | Ja, ISO20022 Kredittransferzahlungsformat für Estland |
| **Betroffene Module**             | Kreditorenkonten                                         |

### <a name="payment-file-archive-for-norway"></a>Zahlungsdateiarchiv für Norwegen

Wenn Zahlungsdateien generiert werden archiviert das Dateiarchiv automatisch alle Dateien, die erstellt werden, auch Dateien, die zuvor gelesen oder geschrieben wurden.

|                              |                                                                    |
|------------------------------|--------------------------------------------------------------------|
| **Grund für Abschreibung**       | Ersetzt durch eine andere Funktion                                        |
| **Ersetzt durch eine andere Funktion?** | Ja, archivierte Einzelvorgänge für elektronische Berichterstellung                            |
| **Betroffene Module**             | Kreditorenkonten, Debitoren, Organisationsverwaltung |

### <a name="payment-import-formats-for-estonia"></a>Zahlungsimportformate für Estland

Die Formate Telehansa und TeleTeenus werden für den Bankzahlungimport verwendet.

|                              |                                                                                            |
|------------------------------|--------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Die Zahlungsformate werden nicht mehr verwendet.                                                    |
| **Ersetzt durch eine andere Funktion?** | Nr. Die Formate werden durch ISO 20022 Auszugsimportformate in künftigen Versionen ersetzt. |
| **Betroffene Module**             | Debitorenkonten                                                                        |

### <a name="performance-management-goal-workflow"></a>Leistungsverwaltungsziel-Workflow

Leistungsverwaltung enthält Zielverwaltung und Integration mit Leistungsbeurteilungen.

|                              |                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Leistungsverwaltung wurde neu gestaltet und die Anzahl von Zielseiten wurde verringert, um den Prozess zu vereinfachen.                 |
| **Ersetzt durch eine andere Funktion?** | Nr. Ziele sind für Manager über das Manager-Self-Service-Portal sichtbar und können vom Manager angezeigt und geändert werden. |
| **Betroffene Module**             | Human Capital Management                                                                                                 |

### <a name="postgirot-and-postgirot-utland-payment-formats-for-sweden"></a>Zahlungsformate Postgirot und Postgirot Utland für Schweden

Zahlungsformate Postgirot und Postgirot Utland für Schweden.

|                              |                                                         |
|------------------------------|---------------------------------------------------------|
| **Grund für Abschreibung**       | Die Zahlungsformate werden nicht mehr verwendet.                 |
| **Ersetzt durch eine andere Funktion?** | Ja, ISO20022 Kredittransferzahlungsformat für Schweden |
| **Betroffene Module**             | Kreditorenkonten                                        |

### <a name="radio-frequency-identifier"></a>Kennung für Funkübertragung

RFID (Radiofrequenz-Identifikation) ist eine Technologie zum Sammeln von Daten. Bei dieser Technologie werden Daten mithilfe elektronischer Markierungen zum Speichern von Identifizierungsdaten sowie mittels eines Lesegeräts erfasst, das ohne direkte Sichtverbindung funktioniert.

|                              |                                               |
|------------------------------|-----------------------------------------------|
| **Grund für Abschreibung**       | Geringe Kundennutzung und ein begrenzter Funktionsumfang. |
| **Ersetzt durch eine andere Funktion?** | Nr.                                            |
| **Betroffene Module**             | Lagerverwaltung                          |

### <a name="report-about-state-invoices-numbering-for-latvia"></a>Bericht zu Bundeslandrechnungsnummerierung für Lettland

Lettische Gesetzgebung schafft bestimmte Regeln dazu, wie Verkaufsrechnungen nummeriert werden sollen. Mit der Funktionalität können Sie bestimmte Nummern Verkaufsrechnungen zuweisen, basierend auf dem Benutzer oder den Benutzergruppen. Sie können einen Bericht oder eine XML-Datei generieren. Sie können auch einen Bericht zu Rechnungsnummern drucken, die verwendet werden.

|                              |                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Die Bundeslandrechnungsnummerierung muss nicht mehr verwaltet werden. Der Bericht zu verwendeten Rechnungsnummern wird nicht mehr benötigt. |
| **Ersetzt durch eine andere Funktion?** | Nr.                                                                                                                       |
| **Betroffene Module**             | Debitorenkonten                                                                                                      |

### <a name="set-up-the-names-of-the-manager-and-general-accountant-of-a-company-for-lithuania"></a>Richten Sie die Namen vom Manager und dem allgemeinen Buchhalter eines Unternehmens für Litauen ein

Die Namen vom Manager und dem allgemeinen Buchhalter eines Unternehmens können auf den Unternehmensinformationen angegeben werden und in verschiedenen lokalen Berichtsausdrücken verwendet werden.

|                              |                                                                 |
|------------------------------|-----------------------------------------------------------------|
| **Grund für Abschreibung**       | Ersetzt durch eine andere Funktion                                     |
| **Ersetzt durch eine andere Funktion?** | Ja, das Einrichten von Beamten kann für den selben Zweck verwendet werden.   |
| **Betroffene Module**             | Debitorenkonten, Kreditorenkonten, Bargeld- und Bankverwaltung |

### <a name="telepay-payment-formats-for-norway"></a>Telepay-Zahlungsformate für Norwegen

Telepay-Zahlungsformate enthalten Kreditorenzahlungsexport (Banküberweisung) und Debitorenzahlungsinkasso (Direktbelastung).

|                              |                                                                                                |
|------------------------------|------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Die Zahlungsformate werden nicht mehr verwendet.                                                        |
| **Ersetzt durch eine andere Funktion?** | Ja, ISO20022 Kredittransferzahlungsformat und AvtaleGiro-Debitorenzahlungsformat für Norwegen |
| **Betroffene Module**            | Kreditorenkonten, Debitoren                                                          |

### <a name="vendor-payment-export-formats-for-finland"></a>Exportformate für Kreditorenzahlungen für Finnland

Zwei Formate für den Export von Zahlungen werden für Finnland verfügbar. LM02 (FI) wird für Inlandszahlungen und LUM2 (FI) wird für Auslandszahlungen verwendet.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| **Grund für Abschreibung**       | Die Zahlungsformate werden nicht mehr verwendet.                  |
| **Ersetzt durch eine andere Funktion?** | Ja, ISO20022 Kredittransferzahlungsformat für Finnland |
| **Betroffene Module**            | Kreditorenkonten                                         |

### <a name="workflow-for-creating-goals"></a>Workflow zum Erstellen der Zielsetzungen

Ein Workflow für das Verwalten der Erstellung der Mitarbeiterziele ist einer von mehreren Workflows, die verfügbar sind, um den Leistungsverwaltungsprozes zu koordinieren.

|                              |                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Die Leistungsverwaltung wurde in Microsoft Dynamics 365 for Finance and Operations vollständig neu gestaltet.                                                                                                                                                                                                                                        |
| **Ersetzt durch eine andere Funktion?** | Die neu entworfene Leistungsverwaltungsfunktion gibt mehr Kontrolle über den Inhalt der Ziele, die Messungen, die verwendet werden, um den Fortschritt zu verfolgen, und die Zuordnung der Begleitunterlagen. Ziele können als Vorlagen gespeichert werden und anschließend wieder verwendet werden. Diese Funktion kann Ihnen helfen, zusätzliche Ziele für Ihre Mitarbeiter schneller einzurichten. |
| **Betroffene Module**            | Human Capital Management                                                                                                                                                                                                                                                                                                               |

## <a name="features-that-have-been-deprecated-in-dynamics-ax-70-releases"></a>Funktionen, die in der Ausgabe Dynamics AX 7.0 veraltet sind

### <a name="ability-to-cancel-changes-to-a-vendor-invoice"></a>Möglichkeit zum Abbrechen von Änderungen an einer Kreditorenrechnung

|                              |                         |
|------------------------------|-------------------------|
| **Grund für Abschreibung**       | Leistungsverbesserung |
| **Ersetzt durch eine andere Funktion?** | Nein                      |
| **Betroffene Module**            | Kreditorenkonten        |

### <a name="aif-axd-and-axbc-integrations"></a>Integration mit AIF, AxD und AxBC

In Application Integration Framework (AIF), können Daten mit externen Systemen über Geschäftslogik ausgetauscht werden, die als Dienst verfügbar gemacht wird. Dynamics AX verfügt über Dienste, die auf Dokumenten und .NET Business Connector (AxBC) basieren. Ein Dokument wird über XML erstellt. Das XML umfasst Kopfinformationen, die hinzugefügt werden, um eine *Meldung* zu erstellen, die zu oder aus Dynamics AX übertragen werden kann. Beispiele zu Dokumenten sind Aufträge und Bestellungen. Fast jede Entität, z. B. ein Debitor, kann über Dokument dargestellt werden. Dienste, die auf Dokumente basieren verwenden**Axd &lt;*Dokument*&gt;** Klassen.

|                              |                                                                                                                                                                                                          |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Die Architektur von AIF und AxDs konnte nicht zu einem Clouddienst skaliert werden. Es gab Leistungsprobleme beim Massenimport.                                                                               |
| **Ersetzt durch eine andere Funktion?** | In der aktuellen Version von Dynamics AX wird diese Funktion durch das Datenimport-/Exportframework ersetzt, das den wiederholten Massenimport/-export unterstützt. Für AxBC wird empfohlen, dass Sie die tatsächlichen Tabellen verwenden. |
| **Betroffene Module**             | AxDs, AxBCs und AIF                                                                                                                                                                                     |

### <a name="boms-without-bom-versions"></a>Stücklisten ohne Stücklistenversionen

Wurde der **Stücklistenversionen**-Konfigurationsschlüssel deaktiviert, so wurden Stücklisteversionen in allen Formularen ausgeblendet, und das System erzwang eine 1:1-Beziehung zwischen freigegebenen Produkten und Stücklisten. Der **Stücklistenversionen**-Konfigurationsschlüssel kann in der aktuellen Version von Dynamics AX nicht deaktiviert werden.

|                              |                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------|
| **Grund für Abschreibung**      | Verwenden eines Konfigurationsschlüssels, um die Skalierung von Stücklistenversionen in einer Cloudumgebung zu verhindern. |
| **Ersetzt durch eine andere Funktion?** | Nein                                                                                      |
| **Betroffene Module**            | Produktinformationsverwaltung, Lagerverwaltung                                    |

### <a name="brazilian-bordero"></a>Brasilianer Bordero

Bestimmte Zahlungsmethode für brasilianische Unternehmen

|                              |                                                                                                       |
|------------------------------|-------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Unterstützung für die brasilianische Bordero-Zahlungsmethode wurde in der brasilianischen Version eingestellt. |
| **Ersetzt durch eine andere Funktion?** | Nr.                                                                                                    |
| **Betroffene Module**             | Kreditorenkonten                                                                                      |

### <a name="brazilian-sintegra-statement"></a>Brasilianischer Sintegra-Auszug

Bundessteuerauszug für ICMS-Steuer

|                              |                                                                                                                       |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Dieser Auszug gilt nicht mehr für einige brasilianische Bundesländer.                                                     |
| **Ersetzt durch eine andere Funktion?** | Nr. Benutzer können das generische elektronische Berichtstool verwenden, um sofern erforderlich den Auszug für bestimmten Situationen zu konfigurieren. |
| **Betroffene Module**             | Steuerbücher                                                                                                          |

### <a name="brazilian-scan-contingency-mode-for-nf-e"></a>Brasilianischer SCAN Notfallmodus für NF-e

(SCAN) Notfallumgebung wird verwendet, um den Status einer Nota Fiscal eletrônica (NF-e) zu generieren, zu exportieren und zu importieren, wenn die Umgebung von Secretaria da Fazenda (SEFAZ) nicht verfügbar ist.

|                              |                                                                             |
|------------------------------|-----------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Diese Notfallmethode gilt nicht mehr in allen brasilianischen Bundesländern |
| **Ersetzt durch eine andere Funktion?** | Nr.                                                                          |
| **Betroffene Module**             | Debitorenkonten                                                         |

### <a name="business-analyzer"></a>Business Analyzer

Diese mobile Anwendung ermöglicht dem Benutzer die Prüfung von wichtigen Geschäftsmetriken.

|                              |                                                                                                                                                               |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Die Funktion wurde durch eine andere Funktion ersetzt.                                                                                                      |
| **Ersetzt durch eine andere Funktion?** | Das Inhaltspack "Finanzielle Leistung überwachen" für Microsoft Power BI umfasst entscheidende Finanzmetriken, die zuvor im Business Analyzer verfügbar waren. |
| **Betroffene Module**             | Hauptbuch                                                                                                                                                |

### <a name="business-statistics"></a>Geschäftsstatistik

Die Einrichtung von Geschäftsstatistikabfragen kann das Analysieren der Leistung der Organisation unterstützen

|                              |                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Ein veralteter Ansatz für Business Intelligence (BI), geringe Kundennutzung und ein begrenzter Funktionsumfang |
| **Ersetzt durch eine andere Funktion?** | Neue BI-Lösung für die aktuelle Version von Dynamics AX                                      |
| **Betroffene Module**             | Beschaffung, Kreditorenkonten, Vertrieb und Marketing, Debitorenkonten         |

### <a name="change-document-date-function-in-invoice-approval-journal"></a>Funktion zum Ändern des Dokumentdatum in der Rechnungsgenehmigungserfassung

|                              |                                                                         |
|------------------------------|-------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Geringe Verwendung                                                               |
| **Ersetzt durch eine andere Funktion?** | Ja. Das Dokumentdatum auf der gebuchten Kreditorenbuchung kann geändert werden. |
| **Betroffene Module**             | Kreditorenkonten                                                        |

### <a name="clieop03-payment-format-for-the-netherlands"></a>ClieOp03-Zahlungsformat für die Niederlande

|                              |                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Das Format ist nicht mehr in den Niederlanden anwendbar, da es durch die SEPA-Funktionen ersetzt wurde. |
| **Ersetzt durch eine andere Funktion?** | SEPA-Zahlungsexport                                                                                       |
| **Betroffene Module**             | Alle                                                                                                        |

### <a name="compliance-center"></a>Compliance Center

Das Compliance Center war eine Enterprise Portal-Website für die Verwaltung der Dokumentationsanforderungen für Kompatibilitätsinitiativen, die dem Sarbanes-Oxley-Gesetz zugeordnet sind.

|                              |                                                                                                                        |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Fehlender Einsatz durch die Kunden. Microsoft SharePoint umfasst die gleiche Fähigkeit, die im Compliance Center verfügbar war. |
| **Ersetzt durch eine andere Funktion?** | Nein                                                                                                                     |
| **Betroffene Module**             | Konformität und interne Kontrollen                                                                                       |

### <a name="connector-for-microsoft-dynamics"></a>Connector für Microsoft Dynamics

Dieses Tool wurde verwendet, um Schlüsseldaten von Microsoft Dynamics CRM mit Microsoft Dynamics ERP-Anwendungen zu integrieren.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| **Grund für Abschreibung**       | Die Funktion wurde durch eine andere Funktion ersetzt. |
| **Ersetzt durch eine andere Funktion?** | Dynamics-Integrator                                      |
| **Betroffene Module**             | Connector für Microsoft Dynamics                         |

### <a name="container-unit-and-multi-dimension-on-hand"></a>Container-Einheit und mehrere Dimensionen am Lager

|                              |                                                                                                                                                                 |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Doppelte Funktionen                                                                                                                                         |
| **Ersetzt durch eine andere Funktion?** | Ja. Seit AX 2012 ist diese Funktion durch die konsolidierte Chargenauftragsfunktion ersetzt worden. Dieser Funktionsumfang umfasst die konsolidierte verfügbare Ansicht. |
| **Betroffene Module**             | Produktinformationsverwaltung, -Produktionssteuerung, Lagerverwaltung, Vertrieb und Marketing                                                                   |

### <a name="cue-group-metadata"></a>Cue-Group-Metadaten

|                              |                                                                                                                                                                                                                               |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Cue-Gruppen wurden verwendet, um eine oder mehrere Cues im Infoboxbereich anzuzeigen. Der Nutzen war beschränkt. Es gab außerdem Leistungsbedenken, da eine Datensatzändern in einem übergeordneten Formular eine Abfrage pro Cue aus der Cue-Gruppe verursacht hat. |
| **Ersetzt durch eine andere Funktion?** | Nein                                                                                                                                                                                                                            |
| **Betroffene Module**             | Alle                                                                                                                                                                                                                           |

### <a name="cue-metadata"></a>Cue-Metadaten

|                              |                                                                                                                                                                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Cue-Metadaten wurden auf das Zählen oder Summieren von Informationen beschränkt.                                                                                                                                                                                   |
| **Ersetzt durch eine andere Funktion?** | Tile-Metadaten wurden für mehr Flexibilität bei der Modellierung eingeführt. So können z. B. aktuelle Nummern, Navigation und Key Performance Indicators (KPIs) modellieren. Count-Tile-Metadaten sind ein direkter Ersatz für Cue-Metadaten. |
| **Betroffene Module**             | Alle                                                                                                                                                                                                                                     |

### <a name="danish-check-format"></a>Scheckformat Dänemark

|                              |                                                                                                                         |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Die Unterstützung für das dänische Scheckformatlayout ist eingestellt wurden, und der Bericht ist aus der DK-Lokalisierung entfernt worden. |
| **Ersetzt durch eine andere Funktion?** | Nein                                                                                                                      |
| **Betroffene Module**             | Alle                                                                                                                     |

### <a name="data-partitions"></a>Datenpartitionen

Datenpartitionen enthalten eine logische Trennung von Daten in der Microsoft Dynamics AX-Datenbank.

|   |   |
|---|---|
| **Grund für Abschreibung**       | Datenpartitionen wurden in Microsoft Dynamics AX 2012 R2 eingeführt, um Datenisolation zu ermöglichen. In einem häufigen Szenario verfügt ein Unternehmen über Tochtergesellschaften und die Daten einer Tochtergesellschaft sollen einer anderen nicht angezeigt werden, obwohl beide Tochterunternehmen von derselben IT-Abteilung verwaltet werden. Zusätzliche Skripts und Verwaltungsaufwand im gesamten Programm sind jedoch erforderlich, um neue Partitionen zu erstellen und mit Daten zu füllen und Partitionsdaten sichern. In der Cloud, in der wir über Platform-as-a-Service(PaaS) Datenbankdienste (Microsoft Azure SQL-Datenbank) verfügen, ist es sehr viel effizienter, eine Datenbank als Isolationscontainer zu verwenden, als Isolationen im Programm durchzuführen. Egal, ob eine Datenpartitionierung für Tochterunternehmen, mehrere Mandanten oder nur zur Skalierung benötigt wird, glauben wir, dass die Szenarien besser über mehrere Datenbanken oder mehrere Instanzen von Dynamics AX behandelt werden können. |
| **Ersetzt durch eine andere Funktion?** | Datenpartitionen werden durch die Unterstützung mehrerer Datenbanken oder Instanzen von Dynamics AX in einer zukünftigen Version ersetzt.    |
| **Betroffene Module**             | Alle  |

### <a name="database-and-file-share-storage-for-attachments"></a>Datenbank- und Dateifreigabespeicher für Anhänge
Microsoft Dynamics AX 2012 ließ die Speicherung von Anhängen in der Datenbank und in Dateifreigaben zu. Beide Optionen werden nicht mehr unterstützt.

|                              |                                        |
|------------------------------|----------------------------------------|
| **Grund für Abschreibung**       | Der Dateifreigabespeicher wird nicht mehr unterstützt, weil in der Cloud gehostete Umgebungen nicht mit lokalen Dateifreigaben kommunizieren können. Der Datenbankspeicher wurde zugunsten von Azure Blob-Speicher eingestellt. Azure Blob-Speicher ist äquivalent zur Speicherung in der Datenbank, weil der Zugriff nur über Client-Formulare von Dynamics 365 for Finance and Operations möglich ist. Auf diese Weise entsteht der zusätzliche Vorteil, dass Speicher bereitgestellt wird, der sich nicht negativ auf die Leistung der Datenbank auswirkt. Blob-Speicher ist der Standardspeichermechanismus für die Dokumentenverwaltung und funktioniert unmittelbar. |
| **Ersetzt durch eine andere Funktion?** | Der Datenbankspeicher wurde zugunsten von Azure Blob-Speicher eingestellt.       |
| **Betroffene Module**             | Alle                   |

### <a name="delimitation"></a>Trennung

|                              |                                        |
|------------------------------|----------------------------------------|
| **Grund für Abschreibung**       | Kein Verwendung der Funktionen gefunden. |
| **Ersetzt durch eine andere Funktion?** | Nein                                     |
| **Betroffene Module**             | Zeit und Anwesenheit                    |

### <a name="desktop-client"></a>Desktopclient

|                              |                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Der Dynamics AX-Client wurde neu gestaltet, um die Benutzererfahrung über mehrere Plattformen und Geräten zu verbessern.                      |
| **Ersetzt durch eine andere Funktion?** | Der neue Webclient basiert auf den Desktop-Formularmetadaten und -Programmiermodell, die geändert wurden, um eine umfangreiche Internet-Plattform bereitzustellen. |
| **Betroffene Module**             | Alle                                                                                                                                    |

### <a name="direct-database-connection"></a>Direkte Datenbankverbindung

In Dynamics AX 2012 R3, konnte sich Retail Modern POS direkt mit dem Kanal DB in ähnlicher Weise mit dem Enterprise POS verbinden. Dies war zusätzlich zur Standardkommunikationsmethode von Retail Modern POS über den Retail Server.  

|                              |                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Direkte Datenbankkonnektivität erforderte ein geringeres Sicherheitsprotokolle und wurde hauptsächlich verwendet, um den höchsten Leistungsstandard zu erreichen. Aufgrund der Leistung und der Sicherheitserweiterungen, die in Finance and Operations aufgetreten sind, führen diese Funktionen nun zu mehr Problemen, als sie lösen. |
| **Ersetzt durch eine andere Funktion?** | Nr. Nur Standard Retail Server Kommunikation wird nun unterstützt.    |
| **Betroffene Module**             | Kanal DB/Retail Modern POS                                    |

### <a name="dutch-swift-mt940"></a>Niederländisches SWIFT MT940

|                              |                                                                                                                                                                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Anstelle der lokalisierten Funktionalität wird nun eine generische Funktion verwendet.                                                                                                                                                                 |
| **Ersetzt durch eine andere Funktion?** | Ja, diese Funktion wurde durch erweiterte Bankabstimmungsfunktionen ersetzt. |
| **Betroffene Module**             | Alle                                                                                                                                                                                                                                   |

### <a name="ebilanz-xbrl-for-germany"></a>eBilanz (XBRL für Deutschland)

Diese Funktionen stellten die eXtensible Business Reporting Language (XBRL)-Ausgabe speziell für die deutsche eBilanz Taxonomie bereit.

|                              |                                                                                                                                                                        |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Fehlender Einsatz durch die Kunden.                                                                                                                                                 |
| **Ersetzt durch eine andere Funktion?** | Nicht durch eine andere Funktion ersetzt. Es gibt aber mehrere spezielle XBRL-Pakete, die umfangreiche XBRL-Funktionen für den deutschen Markt bereitstellen. |
| **Betroffene Module**             | Management Reporter                                                                                                                                                    |

### <a name="enterprise-portal-client"></a>Enterprise Portal-Kunde

|                              |                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Eine einzelne Clientplattform ist bereitgestellt worden.                                                                                            |
| **Ersetzt durch eine andere Funktion?** | Der neue Webclient basiert auf den Desktop-Formularmetadaten und -Programmiermodell, die geändert wurden, um eine umfangreiche Internet-Plattform bereitzustellen. |
| **Betroffene Module**             | Alle                                                                                                                                    |

### <a name="environmental-sustainability"></a>Umweltverträglichkeit

|                              |                                                    |
|------------------------------|----------------------------------------------------|
| **Grund für Abschreibung**       | Geringe Kundennutzung und ein begrenzter Funktionsumfang.       |
| **Ersetzt durch eine andere Funktion?** | Nein                                                 |
| **Betroffene Module**             | Konformität und interne Kontrollen, Kreditorenkonten |

### <a name="form-activex-and-managed-host-controls"></a>ActiveX- und Managed Host-Steuerelemente in Formularen

|                              |                                                                                                                                                                                               |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | ActiveX und die Managed Host-Steuerelemente basieren auf dem veralteten Desktopclient.                                                                                                             |
| **Ersetzt durch eine andere Funktion?** | Das Framework für erweiterbare Steuerelemente basiert auf HTML, CSS und JavaScript und dient als Steuerelement in der Microsoft Visual Studio-Umgebung. |
| **Betroffene Module**             | Alle                                                                                                                                                                                           |

### <a name="generate-prenotes-by-using-a-batch"></a>Generieren von Testtransaktionen als Stapelverarbeitung

Testtransaktionsgenerierung kann nicht mithilfe einer Charge verwendet werden. Sie kann jedoch immer noch von einem Benutzer erstellt werden.

|                              |                                                                                                        |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Es ist kein Formular vorhanden, um die resultierende Testtransaktionsdatei zu verwalten und anzuzeigen, wenn sie mithilfe einer Charge generiert wurde. |
| **Ersetzt durch eine andere Funktion?** | Testtransaktionen können weiterhin generiert werden, und der Benutzer hat die Kontrolle über den Speicherort der Datei.   |
| **Betroffene Module**             | Debitorenkonten, Kreditorenkonten, Bargeld- und Bankverwaltung                                        |

### <a name="german-dtaus-payment-export-and-account-statement-import-totals-and-transactions"></a>Deutscher DTAUS-Zahlungsexport und Kontoauszugsimport (Summen und Buchungen)

|                              |                                                                                                                                                                                                                                                                                                |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Das Format ist nicht mehr in Deutschland anwendbar, da es durch die SEPA-Funktionen ersetzt wurde.                                                                                                                                                                 |
| **Ersetzt durch eine andere Funktion?** | Ja, diese Funktionalität wurde durch SEPA-Zahlungsexport und erweiterte Bankabstimmungsfunktionen zum Importieren von Kontoauszügen ersetzt. |
| **Betroffene Module**             | Alle                                                                                                                                                                                                                                                                                            |

### <a name="german-dtazv-payment-format"></a>Deutsches DTAZV-Zahlungsformat

|                              |                                                                                                    |
|------------------------------|----------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Das Format ist nicht mehr in Deutschland anwendbar, da es durch die SEPA-Funktionen ersetzt wurde. |
| **Ersetzt durch eine andere Funktion?** | SEPA-Zahlungsexport                                                                               |
| **Betroffene Module**             | Alle                                                                                                |

### <a name="german-mt940-import"></a>MT940 Import, deutsch

|                              |                                                                                                                                                                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Anstelle der lokalisierten Funktionalität wird nun eine generische Funktion verwendet.                                                                                                                                                                 |
| **Ersetzt durch eine andere Funktion?** | Ja, diese Funktion wurde durch erweiterte Bankabstimmungsfunktionen ersetzt. |
| **Betroffene Module**             | Alle                                                                                                                                                                                                                                   |

### <a name="german-xml-eu-sales-list"></a>Deutsche XML EU Sales-Liste

|                              |                                                                                                                                                                                    |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Das XML-Format für EU-Umsatzliste für Deutschland wird nicht mehr unterstützt. Nur das Format der Textdatei ELMA5 kann verwendet werden, um den Bericht zur EU-Umsatzliste der deutschen Steuerbehörde zu senden. |
| **Ersetzt durch eine andere Funktion?** | Nein                                                                                                                                                                                 |
| **Betroffene Module**             | USt.                                                                                                                                                                                |

### <a name="gl-ssrs-reports"></a>GL SSRS Berichte

Berichte mit den folgenden Menüoptionen wurden entfernt: **Zusammengefasste Zwischenbilanz**, **Ausführliche Zwischenbilanz**, **Kontenplan**, **Audit-Trail**, **Saldenliste** und **Summen- und Saldenliste**.

|                              |                                                                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Microsoft SQL Server Reporting Services (SSRS)-Finanzberichte wurden durch nach Management Reporter-Funktionen und -Standardberichte ersetzt. |
| **Ersetzt durch eine andere Funktion?** | Management Reporter (**Finanzberichterstellung** in der aktuellen Version von Dynamics AX)                                                  |
| **Betroffene Module**            | Hauptbuch                                                                                                                               |

### <a name="infopart-and-formpart-metadata"></a>InfoPart- und FormPart-Metadaten

|                              |                                                                                                                                                                                                                                |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | InfoPart- und FormPart-Metadaten ermöglichen die Erstellung von Infoboxen für zwei verschiedene Clients.                                                                                                                                    |
| **Ersetzt durch eine andere Funktion?** | InfoPart-Metadaten, die einen vereinfachten Formulardefinition darstellen, werden über ein Upgrade zu einem Formular konvertiert. FormPart-Metadaten, die ein Formular referenzieren, wird durch eine direktere Referenz ersetzt, die über ein Upgrade erstellt wird. |
| **Betroffene Module**             | Alle                                                                                                                                                                                                                            |

### <a name="main-account-list-page"></a>Listenseite "Hauptkonten"

Eine Liste der Konten für die juristische Person und die zugeordneten Saldoinformationen

|                              |                                                                                                                                                                                    |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Saldoinformationen sind auf der Listenseite **Zwischenbilanz** nach Konto und Dimension verfügbar.                                                                                      |
| **Ersetzt durch eine andere Funktion?** | **Hauptkonten** enthält die gleiche Liste aus Konten, die die **Hauptkonto** Listenseite enthielt. Die Rasteransicht in **Hauptkonten** zeigt auch eine kleinere, rasterähnliche Ansicht. |
| **Betroffene Module**             | Hauptbuch                                                                                                                                                                     |

### <a name="malaysia-and-singapore-bank-cash-flow-report"></a>Malaysia- und Singapur-Bankcashflowbericht

Drucken eines Cashflowberichts mit Buchungen und Details des Zu- und Abflusses flüssiger Mittel für einen bestimmten Datumsbereich für die ausgewählten Bankkonten.

|                              |                                                                         |
|------------------------------|-------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Die gleichen Informationen können aus der Anfragenbankbuchung eingeholt werden. |
| **Ersetzt durch eine andere Funktion?** | Die Anfragenbanktransaktion.                                            |
| **Betroffene Module**             | Bargeld- und Bankverwaltung                                                |

### <a name="mexican-cfd-electronic-invoice"></a>Mexikanische CFD (elektronische Rechnung).

Diese Funktion aktivierte die Generierung der mexikanischen elektronischen Rechnungen, indem die Methode Comprobante Fiscal Digital (CFD) angewendet wird, bei der das Unternehmen die Rechnung signiert, indem es die zugehörige Autorisierung von der Behörde anfordert. Diese Funktion umfasst auch einen monatlichen Bericht, der alle elektronischen Rechnungen umfasst, die in der Periode ausgestellt wurden.

|                              |                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Die Methode ist nicht mehr verfügbar. Die Generierung elektronischer Rechnungen über die CFD-Methode wurde von den Steuerbehörden als veraltet definiert und durch die Comprobante Fiscal Digital a través de Internet (CFDI)-Methode ersetzt, bei der die Signierung an einen Drittanbieter (PAC) delegiert wird. Der monatliche Bericht ist entfernt wurden. Eine Abfragemöglichkeit ermöglicht Benutzern die Abfrage von historischen Transaktionen. |
| **Ersetzt durch eine andere Funktion?** | Nein                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Betroffene Module**             | Debitoren, Projekt                                                                                                                                                                                                                                                                                                                                                                              |

### <a name="mexico-realized-and-unrealized-vat"></a>Realisierte und nicht realisierter Mehrwertsteuer in Mexiko

Microsoft Dynamics AX 2012 verwaltete die nicht realisierte Mehrwertsteuer (VAT), indem es verwendete Mexiko-spezifische Funktionen für "nicht realisierte Steuer" nutzt.

|                              |                                                                                                                     |
|------------------------------|---------------------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Doppelte Funktionen                                                                                             |
| **Ersetzt durch eine andere Funktion?** | Ja, diese Funktion wurde durch eine Standardmehrwertsteuerfunktion ersetzt, die von Core bereitgestellt wird. |
| **Betroffene Module**             | USt.                                                                                                                 |

### <a name="microsoft-outlook-integration"></a>Microsoft Outlook-Integration

|                              |                                                                                |
|------------------------------|--------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Diese Funktion wurde von der Microsoft Exchange Server-Integration ersetzt. |
| **Ersetzt durch eine andere Funktion?** | Ja                                                                            |
| **Betroffene Module**             | Vertrieb und Marketing                                                            |

### <a name="payroll-information-in-human-resources"></a>Lohndaten in der Personalverwaltung

Personalverwaltung-Lohndaten

|                              |                                                                                                                                                                                                                                                                                                                              |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Diese Funktion wurde durch zentrale Lohn- und Personalverwaltungsseiten ersetzt.                                                                                                                                                                                                                                              |
| **Ersetzt durch eine andere Funktion?** | **Vergütungen**, **Einnahmen** und zugehörige Seiten, die zuvor in US-Lohn waren, sind umkonfiguriert worden und sind jetzt Teil der zentralen Personalverwaltungskonfiguration, um die externe Lohnverarbeitung besser zu unterstützen.. Diese Funktionen steht über den Konfigurationsschlüssel **Personalverwaltung 1** &gt; **Lohnabrechnung** bereit. |
| **Betroffene Module**             | Personalverwaltung, Lohnabrechnung                                                                                                                                                                                                                                                                                                     |

### <a name="private-blocking-of-inventory-and-warehouse-management-journals"></a>Private Sperrung von Lager- und Lagerortverwaltungserfassungen

Die Bestands- und Lagerorterfassungen unterstützen nicht mehr die Möglichkeit, eine Erfassung als privat für einen ausgewählten Benutzer zu markieren. Nur der Prozess der Sperrung von Erfassungen als privat für Benutzergruppen und der Sperrung während der Bearbeitung wird unterstützt.

|                              |                                        |
|------------------------------|----------------------------------------|
| **Grund für Abschreibung**       | Kein Verwendung der Funktionen gefunden. |
| **Ersetzt durch eine andere Funktion?** | Nein                                     |
| **Betroffene Module**             | Bestandsverwaltung                   |

### <a name="product-builder"></a>Produktgenerator

Der Produktgenerator wurde zur dynamischen Konfiguration von Artikel aus einem Auftrag, Verkaufsangebot, Produktionsauftrag, Projektangebot oder einem Artikelbedarf verwendet. Basierend auf einem Produktmodell mit Modellvariablen kann der Benutzer Werte auswählen, um die Kundenanforderungen zu erfüllen und eine eindeutige Produktvariante mit einer Stückliste und einem Arbeitsplan zu erhalten.

|                              |                                                                                                                                                                                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Der Produktgenerator zeigte X++-Code für die Endbenutzern an und wird in der aktuelle Version von Dynamics AX nicht unterstützt. Es ist entfernt wurden, um doppelten Wartungsaufwand durch Überschneidung einer beträchtlichen Codebases zu vermeiden. |
| **Ersetzt durch eine andere Funktion?** | Produktkonfiguration                                                                                                                                                                                   |
| **Betroffene Module**             | Produktinformationsverwaltung, Vertrieb und Marketing                                                                                                                                                     |

### <a name="rename-product-dimension"></a>Produktdimension umbenennen

Mit dieser Funktion können Sie den Namen einer der drei Standardproduktdimensionen (Größe, Farbe oder Stil) auf einen passenderen Namen ändern, der Ihren Geschäftsanforderungen besser entspricht. Das Umbenennen umfasste alle Beschriftungen, in denen der Produktdimensionsname verwendet wurde.

|                              |                                                                               |
|------------------------------|-------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Die aktuelle Version von Dynamics AX unterstützt Beschriftungsänderungen zur Laufzeit nicht. |
| **Ersetzt durch eine andere Funktion?** | Nr.                                                                            |
| **Betroffene Module**             | Produktinformationsverwaltung                                                |

### <a name="retail-server-connectivity-using-http"></a>Retail Serververbindung mithilfe von HTTP

In Dynamics AX 2012 R3, könnte der Retail Server mithilfe der HTTP-Kommunikation arbeiten (nicht-gesichert). Dies war zusätzlich zur Standardkommunikation mithilfe HTTPS.

|                              |                                                                               |
|------------------------------|-------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Aufgrund der neuen Sicherheitsanforderungen wird nur noch die gesicherte Kommunikation mit TLS 1.2 (oder höher, wenn verfügbar) unterstützt. Der Self-Service-Installer konfiguriert automatisch den Computer für die Kommunikation. |
| **Ersetzt durch eine andere Funktion?** | Nr. Nur Standard HTTPS-Kommunikation wird nun unterstützt.                                                                           |
| **Betroffene Module**             | Retail Server                                                |

### <a name="role-center-pages"></a>Rollencenterseiten

|                              |                                                                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Die Rollencenter-Seiten basierten auf der veralteten Enterprise Portal-Plattform, die durch die neue Webclient-Plattform in der aktuellen Version von Dynamics AX ersetzt wurde. |
| **Ersetzt durch eine andere Funktion?** | Das neue Arbeitsbereichs-Formularmuster bietet Benutzer ein prozesszentriertes Design, das den einfachen Zugriff auf häufig verwendete Aufgaben innerhalb dieses Prozesses bietet.                       |
| **Betroffene Module**             | Alle                                                                                                                                                                      |

### <a name="sales-tax-jurisdictions"></a>Umsatzsteuerzuständigkeiten

|                              |                                              |
|------------------------------|----------------------------------------------|
| **Grund für Abschreibung**       | Geringe Kundennutzung und ein begrenzter Funktionsumfang. |
| **Ersetzt durch eine andere Funktion?** | Nein                                           |
| **Betroffene Module**             | US-Mehrwertsteuer                                 |

### <a name="shipping-carrier-interface"></a>Versandspediteurschnittstelle

|                              |                                                                                                                                                 |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Doppelte Funktionen                                                                                                                         |
| **Ersetzt durch eine andere Funktion?** | Ja, diese Funktion wurde teilweise ersetzt durch die Transportverwaltung, wurde aber noch nicht durch die grundlegende Lagerortverwaltung (WMS I) ersetzt. |
| **Betroffene Module**             | Vertrieb und Marketing, Bestandsverwaltung                                                                                                       |

### <a name="sites-services"></a>Sites Services

Sites Services lassen Sie Websites erstellen, die Ihre Geschäftsprozesse mit dem Internet ohne IT-Support erweitern.

|                              |                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Die Microsoft Azure-Infrastruktur, die durch Dynamics AX verwendet wird, hat neue Funktionen, die stattdessen verwendet werden können (beispielsweise Azure-Sites). |
| **Ersetzt durch eine andere Funktion?** | Nein                                                                                                                                       |
| **Betroffene Module**             | Personalrekrutierung, Fallverwaltung, Angebotsanforderungen, Kreditorenregistrierung                                                                  |

### <a name="ssas-demand-forecasting-strategy"></a>SSAS Bedarfsplanungsdienste

|                              |                                                                              |
|------------------------------|------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Das Design der Funktion kann nicht von der neuen Cloudarchitektur unterstützt werden. |
| **Ersetzt durch eine andere Funktion?** | Azure Machine Learning Bedarfsplanungsstrategie                           |
| **Betroffene Module**             | Planung                                                                     |

### <a name="travel-requisitions"></a>Reiseanforderungen

|                              |                                                                 |
|------------------------------|-----------------------------------------------------------------|
| **Grund für Abschreibung**       | Geringe Verwendung und die meisten Funktionen waren im Enterprise Portal vorhanden. |
| **Ersetzt durch eine andere Funktion?** | Nein                                                              |
| **Betroffene Module**             | Spesenverwaltung                                              |

### <a name="vendor-invoice-pool-excluding-posting-details"></a>Kreditorenrechnungspool ohne Buchungsdetails

|                              |                                                                                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Geringe Verwendung. Diese Funktion wurde durch die Rechnungserfassung ersetzt, die Workflowfunktionen hat. |
| **Ersetzt durch eine andere Funktion?** | Workflowfunktionalitäten der Rechnungserfassung                                                           |
| **Betroffene Module**             | Kreditorenkonten                                                                                        |

### <a name="virtual-company-accounts"></a>Virtuelle Unternehmenskonten

Die virtuelle Unternehmensfunktion wird nicht mehr in Dynamics AX unterstützt. Die virtuelle Unternehmensfunktion ermöglicht es Benutzern, Tabellen einzurichten, die für eine Gruppe von Unternehmen freigegeben werden könnten. Eine Beschreibung der Funktion finden Sie unter [Unternehmenskonten und virtuelle Unternehmenskonten](https://msdn.microsoft.com/en-us/library/aa834382(v=ax.10).aspx). Die Funktion arbeitet, indem sie Tabellen in Sammlungen gruppiert die virtuellen Unternehmen zugewiesen werden (Gruppen von "tatsächlichen" Unternehmen). Abfragen werden erstellt, sodass alle Unternehmen im virtuellen Unternehmen auf die Daten in Tabellen der zugeordneten Tabellensammlungen zugreifen können.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><b>Grund für Abschreibung</b></td>
<td><ul>
<li>Virtuelle Unternehmen müssen eingerichtet werden, bevor Daten in Tabellen gespeichert werden. Das nachträgliche Einpassen von virtuellen Unternehmen in eine vorhandene Implementierung ist sehr schwierig.</li>
<li>Da in der aktuellen Version von Microsoft Dynamics AX eine starke Datennormalisierung vorgenommen wurde, ist es sehr schwierig zu wissen, was zu den Tabellensammlungen hinzugefügt werden muss. Beispielsweise ist es schwierig, zu wissen, welche Tabellen freigegeben werden sollen. Alle Tabellen die auf Tabellen verweisen, die in einem virtuellen Unternehmen sind, müssen ebenfalls hinzugefügt werden. Die Tabellennormalisierung bedeutet, dass auch einfache Masterdaten, die auf eine Vielzahl von Tabellen verteilt sind, Teil des virtuellen Unternehmens sein müssen. Jeder Fehler, der hier auftritt, verursacht funktionale Probleme.</li>
<li>Wenn eine Tabelle Teil eines virtuellen Unternehmens ist, verliert sie Informationen über den Ursprung der Daten. Nur das virtuelle Unternehmen wird erfasst.</li>
</ul></td>
</tr>
<tr class="even">
<td><b>Ersetzt durch eine andere Funktion?</b></td>
<td>Globale Tabellen können verwendet werden, um Tabellen für alle Unternehmen verfügbar zu machen. Zurzeit besteht kein Ersatz.</td>
</tr>
<tr class="odd">
<td><b>Betroffene Module</b></td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

### <a name="warehouse-management-ii"></a>Lagerortverwaltung II

|                              |                                                                                                                                                                                                                                                                                                             |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Die Lösung Lagerortverwaltung II (WMS II), die im Modul **Inventurverwaltung** verfügbar war, dupliziert die Funktionalität, die im Modul **Lagerortverwaltung** enthalten ist, die in Microsoft Dynamics AX 2012 R3 enthalten war.                                                                         |
| **Ersetzt durch eine andere Funktion?** | Das **Lagerortverwaltungsmodul**, das in AX 2012 R3, Microsoft Dynamics AX 2012 R3 CU8 und Microsoft Dynamics AX 2012 R3 CU9 freigegeben wurde, ersetzt die Funktionen der Lagerortverwaltung II. Das neue Modul hat fortschrittlichere Funktionen sowie flexiblere Lagerortverwaltungsprozesse als jene, die in den Funktionen der Lagerortverwaltung II angeboten werden. |
| **Betroffene Module**             | Bestandsverwaltung, Verkauf und Marketing, Beschaffung                                                                                                                                                                                                                                         |

### <a name="worker-reminders-in-human-resources"></a>Erinnerungen für Arbeitskräfte in der Personalverwaltung

Personalverwaltung-Lohndaten

|                              |                 |
|------------------------------|-----------------|
| **Grund für Abschreibung**       | Geringe Verwendung       |
| **Ersetzt durch eine andere Funktion?** | Nein              |
| **Betroffene Module**             | Personalverwaltung |

### <a name="workplanner"></a>Arbeitsplanung

|                              |                                                                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Geringe Verwendung                                                                                                                                                            |
| **Ersetzt durch eine andere Funktion?** | Nein, aber die Seite **Profilbeziehung**, die von der Seite **Profilgruppen** geöffnet wird, unterstützt das gleiche Geschäftsszenario wie die veraltete Seite **Arbeitsplanung**. |
| **Betroffene Module**             | Zeit und Anwesenheit                                                                                                                                                  |

### <a name="x-financial-statements"></a>X++ Finanzaufstellungen

|                              |                                                                                             |
|------------------------------|---------------------------------------------------------------------------------------------|
| **Grund für Abschreibung**       | Die Funktion wurde durch eine andere Funktion ersetzt.                                    |
| **Ersetzt durch eine andere Funktion?** | Management Reporter (**Finanzberichterstellung** in der aktuellen Version von Dynamics AX) |
| **Betroffene Module**             | Hauptbuch                                                                              |


