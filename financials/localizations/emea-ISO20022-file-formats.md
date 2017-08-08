---
title: Import von ISO20022-Dateien
description: Dieses Thema beschreibt den Import von Zahlungsdateien in den Formaten ISO 20022 camt.054 und pain.002 in Microsoft Dynamics 365 for Finance and Operations, Enterprise-Edition.
author: neserovleo
manager: AnnBe
ms.date: 05/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Italy, Latvia, Lithuania, Norway, Poland, Spain, Sweden, Switzerland, United Kingdom
ms.author: v-lenest
ms.search.validFrom: 2017-06-01T00:00:00.000Z
ms.dyn365.ops.version: Enterprise edition, July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 48e280bf0a6c5db237bd389fe448c9d698d3ae12
ms.openlocfilehash: acf6ed5f503d77f372d802a51a71cec062c2b24b
ms.contentlocale: de-de
ms.lasthandoff: 07/25/2017

---

# <a name="import-iso20022-files"></a>ISO20022-Dateien importieren

## <a name="overview"></a>Überblick
Sie können Zahlungsdateien in den folgenden Formaten importieren:

 - **ISO20022 camt.054 Gutschriftanzeige** – Import eingehender Zahlungen aus einer Datei in diesem Format in das Kundenzahlungsjournal.
 - **ISO20022 pain.002 Statusrückgabe** und **ISO20022 camt.054 Lastschriftanzeige** – Import von Rückgabedateien in diesen Formaten in das AP-Zahlungstransferjournal.

## <a name="prerequisites-for-importing-the-camt054-credit-advice-file"></a>Voraussetzungen für den Import der camt.054-Gutschriftanzeigedatei
Sie müssen die folgenden Voraussetzungen erfüllen, um Bankbenachrichtigungsmeldungen im Format camt.054.001.002 in das Kundenzahlungsjournal zu importieren.

1. Import der **ISO20022 camt.054** Electronic Reporting (ER)-Konfiguration aus Microsoft Dynamics Lifecycle Services (LCS). Anschließend wählen Sie auf der Seite **Kundenzahlungsmethode** im Feld **Importformatkonfiguration** diese Konfiguration aus. Weitere Informationen finden Sie [Dateiformate für Zahlungsmethoden](emea-select-file-formats-for-the-method-of-payments.md).
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
    - Geben Sie ESR, BESR und Bankleitzahl für das Bankkonto der juristischen Entität ein. Weitere Informationen finden Sie unter [ESR-Funktion der Vorversion](emea-che-esr-customer-payments-import.md), weil hier ähnliche Einstellungen erforderlich sind.
    
## <a name="import-the-camt054-credit-advice-file-into-the-customer-payment-journal"></a>Importieren der camt.054-Gutschriftanzeigedatei in das Kundenzahlungsjournal.
1. Klicken Sie auf der Seite **Kundenzahlungserfassungspositionen** auf **Funktionen** > **Zahlungen importieren**.
2. Wählen Sie die Zahlungsmethode aus, die die erforderlichen Einstellungen für das ISO20022 camt.054-Format besitzt.
3. Geben Sie die erforderlichen Parameter und den Dateipfad an und klicken Sie anschließend auf **OK**.

Die Datei wird importiert.

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

