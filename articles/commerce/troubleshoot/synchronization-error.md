---
title: Probleme mit der asynchronen Auftragssynchronisierung
description: In diesem Artikel werden häufige Gründe für Fehler bei der asynchronen Auftragserstellung in Microsoft Dynamics 365 Commerce und Schritte zur Fehlerbehebung beschrieben, damit Systembenutzer und Partner wissen, was schief gelaufen ist.
author: Shajain
ms.date: 11/30/2022
ms.topic: Troubleshooting
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.openlocfilehash: 27bccced3c07149fe1842524660447a49f86f3fc
ms.sourcegitcommit: 2804b05214c87f76457608b5db072582ff339852
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/01/2022
ms.locfileid: "9815755"
---
# <a name="asynchronous-order-synchronization-issues"></a>Probleme mit der asynchronen Auftragssynchronisierung

[!include [banner](../../includes/banner.md)]

In diesem Artikel werden häufige Gründe für Fehler bei der asynchronen Auftragserstellung in Microsoft Dynamics 365 Commerce und Schritte zur Fehlerbehebung beschrieben, damit Systembenutzer und Partner wissen, was schief gelaufen ist.

## <a name="symptom"></a>Symptom

Asynchrone Aufträge, die aus Dynamics 365 Commerce E-Commerce oder der Verkaufsstelle (POS) erstellt werden, werden nicht in Commerce headquarters widergespiegelt.

## <a name="troubleshooting"></a>Problembehandlung

Die Auftragserstellung kann in Headquarters aus verschiedenen Gründen fehlschlagen, je nachdem, in welcher Phase der Auftragserstellungsprozess fehlschlägt. Die folgenden Schritte zur Fehlerbehebung gehen die möglichen Ursachen durch.

### <a name="validate-that-the-transaction-related-to-the-asynchronous-order-has-reached-headquarters"></a>Bestätigen Sie, dass die mit dem asynchronen Auftrag verbundene Transaktion in Headquarters erreicht hat

Gehen Sie bei E-Commerce-Aufträgen in Headquarters zu **Einzelhandel und Handel \> Anfragen und Berichte \> Onlineshopbuchungen**. Wenn Sie eine Bestätigungsnummer für den Auftrag haben, filtern Sie die Transaktionen, indem Sie die Bestätigungsnummer in das Feld **Kanalreferenz-ID** eingeben. Wenn Sie keine Bestätigungsnummer haben, filtern Sie die Transaktionen, indem Sie die Kundenkontonummer eingeben.

Öffnen Sie für POS-Aufträge die Seite **Geschäftstransaktionen** und filtern Sie die Datensätze nach Belegnummer oder Kundenkontonummer. Wenn die Transaktion nicht gefunden wird, führen Sie den Kanaltransaktionseinzelvorgang **P-0001** aus, der Transaktionen von den Kanälen mit Headquarters synchronisiert. Wenn der Einzelvorgang **P-0001** fehlschlägt, öffnen Sie ein Supportticket für den fehlgeschlagenen Auftrag. Wenn der Einzelvorgang **P-0001** erfolgreich ist, die Transaktionen jedoch immer noch nicht in Headquarters angezeigt werden, öffnen Sie ein Supportticket mit den relevanten Informationen.
 
### <a name="check-the-synchronization-status-if-the-transaction-is-present-in-headquarters-but-isnt-linked-with-a-sales-order"></a>Überprüfen Sie den Synchronisierungsstatus, wenn die Transaktion in Headquarters vorhanden, aber nicht mit einem Auftrag verknüpft ist

Wenn die Transaktion in Headquarters vorhanden ist, der Auftrag jedoch nicht erstellt wurde, öffnen Sie die Seite **Onlineshoptransaktionen** und wählen Sie das Inforegister **Synchronisierungsstatus**. Wenn der Einzelvorgang **Sychronisierungsstatus** versucht, diese Transaktion zu synchronisieren, sollte das Feld **Status des ausstehenden Auftrags** den Status **Erfolgreich** oder **Fehlgeschlagen**. Wenn der Status **Erfolgreich** lautet, muss das Auftragsfeld für diese Transaktion vorhanden sein. Wenn der Status **Fehlgeschlagen** lautet, können Sie die Fehlerdetails im Feld **Auftragsfehlerdetails** im Inforegister **Synchronisationsstatus** anzeigen lassen. Wenn keiner dieser Status angezeigt wird, wurde kein Versuch unternommen, die Transaktion zu verarbeiten. In diesem Fall können Sie oben auf der Seite **Auftrag synchronisieren** auswählen, um den Einzelvorgang für die Synchronisierung auszuführen.

Stellen Sie sicher, dass der Einzelvorgang **Aufträge synchronisieren** regelmäßig ausgeführt wird, damit asynchrone Transaktionen als Aufträge in Headquarters erstellt werden können.

Die folgenden Abschnitte enthalten Informationen zu einigen häufigen Fehlern und zu Korrekturvorschlägen.

#### <a name="the-order-error-details-field-shows-the-following-error-message-number-sequence-has-been-exceeded"></a>Das Feld „Auftragsfehlerdetails“ zeigt die folgende Fehlermeldung: „Nummernkreis wurde überschritten“

Nummernkreise werden verwendet, um Aufträge in Headquarters zu erstellen. Wenn alle für einen Nummernkreis zulässigen Nummern ausgeschöpft sind, generiert das System diese Fehlermeldung. Den Nummernkreis, der zum Erstellen von Aufträgen verwendet wird, finden Sie unter **Debitorenparameter \> Nummernkreise \> Auftrag**. Um diesen Fehler zu beheben, korrigieren Sie den vorhandenen Nummernkreis oder ersetzen Sie ihn durch einen neuen Nummernkreis.

#### <a name="the-order-error-details-field-shows-the-following-error-message-there-must-be-a-default-payment-service-to-process-credit-card-transactions"></a>Das Feld „Auftragsfehlerdetails“ zeigt die folgende Fehlermeldung an: „Für die Verarbeitung von Kreditkartentransaktionen muss ein Standardzahlungsservice vorhanden sein“

Um diesen Fehler zu beheben, bestätigen Sie, dass in Headquarters eine Standardzahlung definiert ist. Wenn keine Standardzahlung festgelegt ist, müssen Sie dies tun. Gehen Sie zu **Debitoren \> Zahlungseinstellungen \> Zahlungsdienste** und stellen Sie sicher, dass die Option **Standardprozessor für neue Kreditkarten** für einen Zahlungsdienst auf **Ja** gesetzt ist.
    
#### <a name="the-order-error-details-field-shows-an-account-structure-error-message"></a>Das Feld „Auftragsfehlerdetails“ zeigt eine Fehlermeldung zur Kontostruktur

Der Text der Fehlermeldung zur Kontostruktur kann variieren, wie die folgenden Beispiele zeigen. Die Fehler haben jedoch eine gemeinsame Ursache, die mit der Konfiguration der Kontostruktur zusammenhängt.

- „Buchungsergebnisse für Stapelverarbeitungsnummer 0009656328 Beleg ARP-000959899 1.00 für Beleg ARP-000959899 in Unternehmen usrt werden als Überzahlung oder Unterzahlung gebucht“
- „Buchungsergebnisse für Stapelverarbeitungsnummer 0009656328 Beleg ARP-000959899 Beleg ARP-000959901 Kontostruktur für die Kombination 618160 ist nicht gültig für Sachkonto gemeinsames Hauptkonto“
- „Buchungsergebnisse für Stapelverarbeitungsnummer 0009656328 Beleg ARP-000959899 Beleg ARP-000959901 gemeldet von Unternehmenkonten usrt“
- „Buchungsergebnisse für Stapelverarbeitungsnummer 0009656328 Beleg ARP-000959899 Buchung wurde abgebrochen“
    
Um diese Fehler zu beheben, überprüfen Sie, ob die Kontostrukturen richtig sind. Weitere Informationen finden Sie unter [Kontostrukturen konfigurieren](/dynamics365/finance/general-ledger/configure-account-structures).
    
Nachdem der Fehler behoben wurde, wählen Sie die fehlgeschlagene Transaktion und dann oben auf der Seite **Auftrag synchronisieren** aus, um den Synchronisierungsauftrag auszuführen.
    
#### <a name="other-types-of-errors-that-might-require-the-transaction-data-to-be-fixed"></a>Andere Arten von Fehlern, die möglicherweise eine Korrektur der Transaktionsdaten erfordern

Um andere Arten von Fehlern zu beheben, die möglicherweise eine Korrektur der Transaktionsdaten erfordern, können Sie die Funktion „Transaktionen bearbeiten und prüfen“ verwenden. Weitere Informationen finden Sie unter [Transaktionen bearbeiten und prüfen](../edit-order-trans.md).
