---
title: ISO20022-Dateien importieren
description: Dieser Artikel beschreibt den Import von Zahlungsdateien in den Formaten ISO 20022 camt.054 und pain.002 in Microsoft Dynamics 365 Finance.
author: AdamTrukawka
ms.date: 07/27/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Italy, Latvia, Lithuania, Norway, Poland, Spain, Sweden, Switzerland, United Kingdom
ms.author: atrukawk
ms.search.validFrom: 2017-06-01
ms.dyn365.ops.version: July 2017 update
ms.search.form: CustPaymMode, CustBankAccounts, VendPaymMode, VendBankAccounts
ms.openlocfilehash: 3c3dc260d7f2b4d4aee966007941f5c626f0a4c6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273829"
---
# <a name="import-iso20022-files"></a>ISO20022-Dateien importieren

[!include [banner](../includes/banner.md)]

Sie können Zahlungsdateien in den folgenden Formaten importieren:

 - **ISO20022 camt.054 Gutschriftanzeige** – Import eingehender Zahlungen aus einer Datei in diesem Format in das Kundenzahlungsjournal.
 - **ISO20022 pain.002 Statusrückgabe** und **ISO20022 camt.054 Lastschriftanzeige** – Import von Rückgabedateien in diesen Formaten in das AP-Zahlungstransferjournal.

## <a name="prerequisites-for-importing-the-camt054-credit-advice-file"></a>Voraussetzungen für den Import der camt.054-Gutschriftanzeigedatei
Sie müssen die folgenden Voraussetzungen erfüllen, um Bankbenachrichtigungsmeldungen im Format camt.054.001.002 in das Kundenzahlungsjournal zu importieren.

1. Import der Konfiguration für die elektronische Berichterstellung (EB) **ISO20022 camt.054** aus Microsoft Dynamics Lifecycle Services (LCS). Anschließend wählen Sie auf der Seite **Kundenzahlungsmethode** im Feld **Importformatkonfiguration** diese Konfiguration aus. Weitere Informationen finden Sie [Dateiformate für Zahlungsmethoden](emea-select-file-formats-for-the-method-of-payments.md).
2. Geben Sie auf der Seite **Alle Kunden** einen Namen und eine Unternehmensnummer für jeden Kunden ein.
3. Richten Sie auf der Seite **Kundenbankkonto** einen Kundenbankkontendatensatz ein, indem Sie die folgenden Informationen eingeben: IBAN oder Bankkontonummer und SWIFT-Code oder Bankleitzahl.
4. Richten Sie auf der Seite **Bankkonto** Bankkonten für die juristische Entität ein, indem Sie die folgenden Informationen eingeben: IBAN oder Bankkontonummer und SWIFT-Code oder Bankleitzahl, Währung und Adresse.

   > [!NOTE]
   > Wenn Sie vorhaben, eine erweiterte Bankabstimmung auf dem FastTab **Abstimmung** zu verwenden, setzen Sie die Option **Erweiterte Bankabstimmung** auf **Ja**. Wenn Sie vorhaben, nicht gebuchte importierte Zahlungen abzugleichen, setzen Sie die Option **Bankauszüge als Bestätigung elektronischer Zahlungen verwenden** auf **Ja**.

5. Optional: Richten Sie auf der Seite **Transaktionscodezuordnung** die Zuordnung zwischen Banktransaktionscodes in der Datei und Banktransaktionstypen ein.
6. Wenn die Datei Transaktionsgebühren enthält, die Sie zusammen mit der Eingangszahlung buchen wollen, erstellen Sie eine Zahlungsgebühr auf der Seite **Kundenzahlungsgebühr**. Anschließend ordnen Sie die Zahlungsgebühr auf der Seite **Zahlungsmethoden** dem Bankkonto zu, das in den Einstellungen für die Zahlungsgebühr angegeben ist.
7. Wenn ESR-Zahlungen importiert werden und ISR-Referenzen enthalten (anwendbar für juristische Entitäten in der Schweiz), gehen Sie bei der Einrichtung wie folgt vor:

    - Geben Sie in das Feld **Kundenzahlungen, Kontolängen** die Länge des Kundencodes ein, der in den ISR-Referenzen verwendet wird, oder für die automatische Identifizierung des Kunden.
    - Stellen Sie sicher, dass die Kundennummer und die Rechnungsnummer (Zahlenfolgen) nur Ziffern enthalten. Sie dürfen keine anderen Zeichen enthalten. Die Rechnungsnummer darf keine führenden Nullen haben.
    - Geben Sie ESR, BESR und Bankleitzahl für das Bankkonto der juristischen Entität ein. Weitere Informationen finden Sie unter [ESR-Debitorenzahlungen für Importe](emea-che-esr-customer-payments-import.md), weil hier ähnliche Einstellungen erforderlich sind.
    
## <a name="import-the-camt054-credit-advice-file-into-the-customer-payment-journal"></a>Importieren der camt.054-Gutschriftanzeigedatei in das Kundenzahlungsjournal.
1. Klicken Sie auf der Seite **Kundenzahlungserfassungspositionen** auf **Funktionen** > **Zahlungen importieren**.
2. Wählen Sie die Zahlungsmethode aus, die die erforderlichen Einstellungen für das ISO20022 camt.054-Format besitzt.
3. Geben Sie die erforderlichen Parameter und den Dateipfad an und klicken Sie anschließend auf **OK**. Die Datei wird importiert.

## <a name="prerequisites-for-importing-files-in-the-pain002-status-return-and-camt054-debit-advice-formats-into-the-ap-payment-transfer-journal"></a>Voraussetzungen für das Importieren von Dateien in pain.002 Statusrückgabe- und camt.054 Lastschriftanzeigeformaten in das AP-Zahlungstransferjournal
Sie müssen die folgenden Voraussetzungen erfüllen, um Bankbenachrichtigungsmeldungen in den folgenden ISO20022-Formaten auf die Seite **Zuliefererzahlungstransfer** zu importieren: pain.002.001.003-Statusrückgabenachrichten und camt.054.001.002-Lastschriftanzeige.

1. Import der **ISO20022 camt.054** und **ISO20022 pain.002** ER-Konfigurationen aus LCS.
2. Wählen Sie auf der Seite **Zuliefererzahlungsmethode** in den Feldern **Rückgabeformatkonfiguration** und **Sekundäre Rückgabeformatkonfiguration** die importierten ER-Konfigurationen aus. Sie müssen für die ausgewählte Zahlungsmethode das generische elektronische Rückgabeformat aktivieren.
3. Richten Sie auf der Seite **Zuordnung Rückgabeformatstatus** die Zuordnung von Statuscodes zwischen pain.002-Status und Zuliefererzahlungsjournalstatus ein.

    Im Folgenden finden Sie ein Beispiel für eine Statuseinrichtung.

    Rückgabestatus | Zahlungsstatus
    --------------|---------------
    RJCT          | Verweigert
    ACCP          | Angenommen
    ACSP          | Eingegangen

4. Richten Sie auf der Seite **Rückgabeformatfehlercodes** pain.002-Fehlercodes und Beschreibung in Übereinstimmung mit externen ISO20022-Statusbegründungscodes ein.

    Im Folgenden finden Sie ein Beispiel für einen Teil einer Fehlercodeeinrichtung.

    Code | Name
    -----|-----
    AC01 | IncorrectAccountNumber
    AC02 | InvalidDebtorAccountNumber
    AC03 | InvalidCreditorAccountNumber
    AC04 | ClosedAccountNumber
    AC05 | ClosedDebtorAccountNumber
    AC06 | BlockedAccount

5. Wenn die camt.054-Datei Transaktionsgebühren enthält, die Sie zusammen mit der Eingangszahlung buchen wollen, erstellen Sie eine Zahlungsgebühr auf der Seite **Kundenzahlungsgebühr**. Anschließend ordnen Sie die Zahlungsgebühr auf der Seite **Zahlungsmethoden** dem Bankkonto zu, das in den Einstellungen für die Zahlungsgebühr angegeben ist.

## <a name="import-the-pain002-status-return-or-camt054-debit-advice-files-into-the-vendor-payment-journal"></a>Importieren der pain.002 Statusrückgabe- oder camt.054 Lastschriftanzeigedateien in das Zahlungstransferjournal
1. Öffnen Sie im Menü Kreditoren die Seite **Zahlungstransfers**.
2. Klicken Sie auf der Seite **Zahlungstransfers** auf **Rückgabedatei – Zulieferer**
3. Wählen Sie die Zahlungsmethode aus, die die erforderlichen Einstellungen für ISO20022-Dateien besitzt, und klicken Sie dann auf **OK**.
4. Wählen Sie das Dateiformat, das Sie importieren wollen, und klicken Sie dann auf **OK**.
5. Geben Sie die erforderlichen Parameter und den Dateipfad an und klicken Sie anschließend auf **OK**.

Wenn Sie die pain.002-Datei importieren, wird der Status der Zuliefererzahlungspositionen aktualisiert, basierend auf den Informationen in der importieren Datei.

Wenn Sie die camt.054-Datei importieren, sollten Sie die folgenden zusätzlichen Parameter spezifizieren:

- **Gebühren-ID** – Geben Sie die Gebühren-ID ein, die neue Zahlungsgebührpositionen definiert, die in der Zuliefererzahlungserfassungsposition erstellt werden, wenn in der camt.054-Datei ein Gebührenbetrag enthalten ist.
- **Neuer Journalname** und **Neue Journalbeschreibung** – Geben Sie den Namen und die Beschreibung des Journals ein, in das die verarbeiteten Transaktionen übertragen werden. Nach der Übertragung müssen dem neuen Journal neue Belegnummern zugewiesen werden.
- **Import von Direktlastschrifttransaktionen** – Setzen Sie diese Option auf **Ja**, wenn ausgehende Direktlastschriften in das Zuliefererzahlungsjournal importiert werden müssen.
- **Journalname** – Definieren Sie einen neuen Journalnamen für die importierten Direktlastschrifttransaktionen.
- **Abgleichstransaktionen** – Setzen Sie diese Option auf **Ja**, wenn importierte Zuliefererzahlungen mit Rechnungen im System abgeglichen werden müssen.

Die importierten Informationen können auf der Seite **Zahlungstransfers** angezeigt werden. 

## <a name="additional-details"></a>Zusätzliche Details

Wenn Sie eine Formatkonfiguration in LCS importieren, importieren Sie die gesamte Konfigurationsstruktur, was bedeutet, dass Varianten«» der Modell- und Modellzuordnung enthalten sind. Im Zahlungsmodell ab Version 8 werden die Zuordnungen in separaten ER-Konfigurationen in der Lösungsstruktur (Zahlungsmodellzuordnung 1611, Zahlungsmodell zum Ziel ISO20022, usw.). Es gibt viele verschiedene Zahlungsformate unter einem Modell (Zahlungsmodell) und getrennte Zuordnungshandhabung ist zentral für eine einfache Lösungsverwaltung. Hierzu nehmen Sie beispielsweise dieses Szenarios: Sie nutzen ISO20022 Zahlungen, um Banküberweisungsdateien zu generieren und dann importieren Sie die Rückgabemeldungen von der Bank. In diesem Szenario sollten Sie die folgenden Einstellungen nutzen:

 - **Zahlungsmodell**
 - **Zahlungsmodellzuordnung 1611** – Diese Zuordnung wird verwendet, um die Exportdatei zu generieren
 - **Zahlungsmodellzuordnung an das Ziel ISO20022** – Diese Konfiguration enthält alle Zuordnungen, die verwendet werden, um die Daten ("zum Ziel" Zuordnungsrichtung) zu importieren
 - **ISO20022 Überweisung** – Diese Konfiguration enthält eine Formatkomponente, die zuständig ist für die Exportdateierstellung (pain.001) basierend auf der Zahlungsmodellzuordnung 1611, sowie als Format um Zuordnungskomponenten zu modellieren, die zusammen mit dem Zahlungsmodell verwendet werden zum Ziel ISO20022, um exportierte Zahlungen im System für Importzwecke zu erfassen (Import in technische Tabelle CustVendProcessedPayments)
 - **ISO20022 Banküberweisung (CER)**, wenn CER der Landerweiterung entspricht - abgeleitetes Format in ISO20022 Banküberweisung mit derselben Struktur und mit bestimmten landesspezifischen Unterschieden
 - **Pain.002** – Dieses Format wird zusammen mit dem Zahlungsmodell verwendet, das sich auf das ISO20022 Ziel bezieht, um die Datei pain.002 in Kreditorenzahlungsübergangserfassung zu importieren
 - **Camo.054** – Dieses Format wird zusammen mit dem Zahlungsmodell verwendet, das sich auf das ISO20022 Ziel bezieht, um die Datei camt.054 in Kreditorenzahlungsübergangserfassung zu importieren Dieselbe Formatkonfiguration wird in den Debitorenzahlungsimportfunktionen verwendet, aber unterschiedliche Zuordnung wird im Zahlungsmodell verwendet, das zur Konfiguration des Ziels ISO20022 bezieht.

Weitere Informationen über die elektronische Berichterstattung finden Sie unter [Elektronischer Berichterstellungsüberblick](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen
- [Kreditorenzahlungen mithilfe eines ISO20022-Zahlungsformats erstellen und exportieren](./tasks/create-export-vendor-payments-iso20022-payment-format.md)
- [ISO20022-Banküberweisungskonfiguration importieren](./tasks/import-iso20022-credit-transfer-configuration.md)
- [ISO20022-Direktbelastungskonfiguration importieren](./tasks/import-iso20022-direct-debit-configuration.md)
- [Unternehmens-Bankkonten für ISO20022-Überweisungen einrichten](./tasks/set-up-company-bank-accounts-iso20022-credit-transfers.md)
- [Unternehmens-Bankkonten für ISO20022-Lastschriften einrichten](./tasks/set-up-company-bank-accounts-iso20022-direct-debits.md)
- [Debitoren und Debitoren-Bankkonten für ISO20022-Lastschriften einrichten](./tasks/set-up-bank-accounts-iso20022-direct-debits.md)
- [Zahlungsmethode für ISO20022-Kreditübertragung einrichten](./tasks/set-up-method-payment-iso20022-credit-transfer.md)
- [Zahlungsmethode für ISO20022-Direktbelastungen einrichten](./tasks/setup-method-payment-iso20022-direct-debit.md)
- [Kreditoren und Kreditorenbankkonten für ISO20022-Überweisungen einrichten](./tasks/set-up-vendor-iso20022-credit-transfers.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
