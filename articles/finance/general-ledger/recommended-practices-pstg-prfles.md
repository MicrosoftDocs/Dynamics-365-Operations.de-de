---
title: Empfohlene Verfahren für Buchungsprofile
description: In diesem Thema werden empfohlene Verfahren zum Konfigurieren von Buchungsprofilen beschrieben.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemSetup, CustPosting, VendPosting, InventPosting, AssetPosting, ProjPosting, AssetLeasePostingAccounts, ProjCategory, ITMCostTypeTable, ProdGroup, WrkCtrTable, WrkCtrResourceGroup, MainAccount, SysDatabaseLogSetup, CustGroup, VendGroup, InventItemGroup
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 211dc42b80089eb1f59a435f09d6e9d9f956736b
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734274"
---
# <a name="recommended-practices-for-posting-profiles"></a>Empfohlene Verfahren für Buchungsprofile

Es gibt mehrere empfohlene Vorgehensweisen, die Sie befolgen sollten, wenn Sie Buchungsprofile im gesamten System konfigurieren. In diesem Thema werden verschiedene Szenarien und die entsprechenden empfohlenen Vorgehensweisen beschrieben.

## <a name="setting-the-do-not-allow-manual-entry-flag"></a>Festlegen des Kennzeichens „Keine manuellen Eingaben zulassen“

Auf der **Hauptkonten**-Seite, die sollte das **Keine manuellen Eingaben zulassen**-Kontrollkästchen für jedes Hauptkonto ausgewählt werden, das für ein Buchungsprofil verwendet wird. Diese Einstellung verhindert, dass Benutzer eine Journalbuchung manuell auf das Hauptkonto buchen. Daher trägt sie dazu bei, dass das untergeordnete Sachkonto im Saldo mit dem Hauptbuch bleibt, und erleichtert den Abstimmungsprozess.

Wenn Anpassungen an einem Konto erforderlich sind, das vom System gesteuert und automatisch gebucht wird, können Sie einen der folgenden Ansätze verwenden:

- Erstellen Sie ein sekundäres Hauptkonto, auf dem die Anpassungen gebucht werden können. Verwenden Sie dann ein Gesamtkonto oder eine spezielle Zeile in Ihren Finanzberichten, um die Konten zu gruppieren und zu summieren.
- Stornieren Sie die ursprünglichen Transaktionen im entsprechenden untergeordneten Sachkonto, nehmen Sie alle erforderlichen Korrekturen vor und buchen Sie die Transaktion dann über dasselbe untergeordnete Sachkonto neu.

## <a name="changing-posting-profiles-after-transactions-exist"></a>Buchungsprofile ändern, nachdem Transaktionen vorhanden sind

Wenn Sie ein Buchungsprofil ändern, nachdem Transaktionen vorhanden sind, kann die Abstimmung fehlschlagen und Ihr untergeordnetes Sachkonto und Sachkonto können aus dem Saldo geraten. Generell empfehlen wir Ihnen das Buchungsprofil **nicht** zu ändern, nachdem Transaktionen vorhanden sind.

Wenn Änderungen erforderlich sind, verwenden Sie die folgenden Richtlinien, um die Integrität des Systems sicherzustellen:

- Nehmen Sie die Änderungen während eines Zeitraumabschlusses vor.
- Nehmen Sie die Änderungen vor, wenn keine anderen Transaktionen im System stattfinden.
- Validieren Sie das Hauptbuch und gleichen Sie es mit dem untergeordneten Sachkonto ab, bevor und nachdem Sie die Änderungen vornehmen.
- Gebuchte Transaktionen werden nicht aktualisiert, wenn Sie das Buchungsprofil ändern. Überlegen Sie genau, ob für Ihre Änderung Anpassungsbuchungen erforderlich sind.
- Wenn Sie Bestandsbuchungsprofile ändern, bedenken Sie, wie sich die Änderungen auf Ihre Lagerbestands- und Hauptbuchsalden auswirken. Einige Änderungen erfordern möglicherweise, dass Sie den Bestand auf 0 (Null) bringen, den Bestand schließen und den Bestand dann wieder einspielen, nachdem die Änderungen vorgenommen wurden.
- Testen Sie Ihre Änderungen immer in einer Nicht-Produktionsumgebung, bevor Sie sie in der Produktion vornehmen.

## <a name="using-database-logging-to-audit-changes-to-posting-profiles"></a>Verwenden der Datenbankprotokollierung zum Überwachen von Änderungen an Buchungsprofilen

Erwägen Sie die Einrichtung einer Datenbankprotokollierung für jedes Buchungsprofil und jede Parametertabelle, die die Buchung steuern. Wenn ein Parameter oder Profil geändert wird, haben Sie dann einen vollständigen Prüfbericht darüber, welcher Wert geändert wurde, wer ihn geändert hat, wann er geändert wurde und was der vorherige Wert war. Diese Informationen können während Ihres Abstimmungsprozesses von entscheidender Bedeutung sein, und Ihr Prüfer benötigt möglicherweise die unterstützende Dokumentation.

Weitere Informationen finden Sie unter [Konfigurieren der Datenbankprotokollierung](../../fin-ops-core/dev-itpro/sysadmin/configure-manage-database-log.md).

Verwenden Sie die folgende Tabelle als Referenz für allgemeine Tabellennamen, die sich auf Buchungsprofile und zugehörige Buchungsparameter beziehen.

| Seitenname | Navigationspfad | Name der Tabelle |
|-----------|-----------------|------------|
| Kreditorenkontenparameter | Kreditorenkonten &gt; Einstellen &gt; Kreditorenkontenparameter | VendParm |
| Kreditoren-Buchungsprofil | Kreditorenkonten &gt;Einstellen&gt; Kreditorenbuchungsprofil | VendPosting |
| Belastungscode | Kreditorenkonten &gt; Belastungseinstellungen &gt; Belastungscode oder Kreditorenkonten &gt; Belastungseinstellung &gt; Belastungscode | MarkupTable |
| Zahlungsmethoden | Kreditorenkonten &gt; Zahlungseinstellungen &gt; Zahlungsmethode | VendPaymMode |
| Skonti | Kreditorenkonten &gt; Zahlungseinstellungen &gt; Skonti oder Forderungen oder Kreditorenkonten &gt; Zahlungseinstellungen &gt; Skonti | CashDisc |
| Zahlungsgebühr (Kreditor) | Kreditorenkonten &gt; Zahlungseinstellungen &gt; Zahlungsgebühr | VendPaymFee |
| Debitorenkontenparameter | Kreditorenkonten &gt; Einstellen &gt; Kreditorenkontenparameter | CustParm |
| Debitoren-Buchungsprofile | Debitoren &gt; Einstellen &gt; Debitorenbuchungsprofil | CustPosting |
| Zahlungsmethoden | Debitoren &gt; Zahlungseinstellungen &gt; Zahlungsmethoden | CustPaymMode |
| Zahlungsgebühr (Debitor) | Debitoren &gt; Zahlungseinstellungen &gt; Zahlungsmethoden | CustPaymFee |
| Anlagen-Leasingparameter | Anlagenleasing &gt; Einstellen &gt; Anlagenleasing-Parameter | AssetLeasePostingAccounts<br>AssetLeaseJournalParameters<br>AssetLeaseExecutoryCostPostingAccounts |
| Bankkonten | Bargeld- und Bankverwaltung &gt; Bankkonten &gt; Bankkonten | BankAccountsTable |
| Bankbuchungsarten | Bargeld- und Bankverwaltung &gt; Einstellen &gt; Banktransaktionstypen | BankTransType |
| Löschungsregeln | Konsolidierungen &gt; Einstellen &gt; Löschungsregel | LedgerEliminationRule<br>LedgerEliminationRuleLines |
| Spesenkategorien | Spesenverwaltung &gt; Einstellen &gt; Allgemein &gt; Spesenkategorien | ProjCategories |
| Anlagenparameter | Anlagen &gt; Einstellen &gt; Anlagenparameter | AssetParameters |
| Anlagenbuchungsprofile | Anlagen &gt; Einstellen &gt; Anlagenbuchungsprofile | AssetLedgerAccounts<br>AssetDisposalParameters |
| Konten für Währungsneubewertung | Hauptbuch &gt; Währungen &gt; Währungsneubewertungskonten | CurrencyLedgerGainLossAccount |
| Konten für automatische Buchungen | Hauptbuch &gt; Buchungseinstellungen &gt; Konten für automatische Buchungen | LedgerSystemAccounts |
| Verrechnung | Hauptbuch &gt; Buchungseinstellungen &gt; Intercompany-Konten | LedgerIntercompany |
| Buchung - Definitionen | Hauptbuch &gt; Buchungseinstellungen &gt; Transaktionsbuchungsdefinitionen | JournalizingDefinitionTrans |
| Buchung (Definitionen) | Hauptbuch &gt; Buchungseinstellungen &gt; Buchungsdefinitionen | JournalizingDefintion |
| Buchung (Bestand) | Bestandsverwaltung &gt; Einstellen &gt; Buchung &gt; Buchung | InventPosting |
| Kostentypcodes | Gesamttransportkosten &gt; Kalkulationseinstellungen &gt; Kostenartencodes | ITMCostTypeTable |
| Ressourcen | Produktionssteuerung &gt; Einstellen &gt; Ressourcen &gt; Ressourcen | WrkCtrTable |
| Ressourcengruppen  | Produktionssteuerung &gt; Einstellen &gt; Ressourcen &gt; Ressourcengruppen | WrkCtrResourceGroup |
| Produktionsbuchungsprofile | Produktionssteuerung &gt; Einstellen &gt; Produktion &gt; Produktionsgruppe | ProdGroup |
| Kostenarten | Produktionskontrolle &gt; Einstellen &gt; Routen &gt; Kostenkategorien | ProjCategory |
| Projektgruppen | Projektverwaltung und -buchhaltung &gt; Einstellen &gt; Buchung &gt; Projektgruppen | ProjGroup |
| Sachkontobuchungseinstellungen (Projekte) | Projektverwaltung und -buchhaltung &gt; Einstellen &gt; Buchung &gt; Sachkontobuchungseinstellungen | ProjPosting |
| Standardgegenkonten für Ausgaben | Projektverwaltung und -buchhaltung &gt; Einstellen &gt; Buchung &gt; Standardverrechnungskonten für Ausgaben | ProjDefaultOffsetSetup |
| Profile von Rückvergütungsverwaltungsbuchungen | Rabattverwaltung &gt; Einstellen der Rabattverwaltungsbuchung &gt; Buchungsprofile der Rabattverwaltung | TAMRebatePosting |
| Sachkontobuchungsgruppe (Steuer) | Steuer &gt; Einstellen &gt; Mehrwertsteuer &gt; Sachkontenbuchungsgruppe | TaxAccountGroup |

## <a name="changing-groups-after-transactions-exist"></a>Ändern von Gruppen, nachdem Transaktionen vorhanden sind

Lassen Sie Vorsicht walten, wenn Sie Gruppen in Stammdaten ändern. Wenn Sie Gruppen verwenden, um Ihre Buchungsprofile zu definieren, kann jede Änderung an einer Gruppe in einem Stammsatz negative Auswirkungen auf die Fähigkeit haben, das Sachkonto mit dem untergeordneten Sachkonto abzugleichen. Beispielsweise können Sie das Bestandsbuchungsprofil für Auftragserlöse so konfigurieren, dass für jede Artikelgruppe ein anderes Erlöskonto verwendet wird. Wenn Sie die einem Artikel zugewiesene Artikelgruppe ändern, nachdem Transaktionen vorhanden sind, werden die Einnahmen aus neuen Transaktionen auf das aktualisierte Konto gebucht. Alle Einnahmen, die vor der Änderung gebucht wurden, verbleiben jedoch auf dem ursprünglichen Konto.

## <a name="testing-posting-profiles"></a>Testen von Buchungsprofilen

Vor der Tatsächlichen Aktivierung und nachdem Sie Änderungen oder Ergänzungen an Ihren Buchungsprofilen oder verwandten Parametern vorgenommen haben, sollten Sie jedes Szenario testen. Sie sollten zumindest jeden Buchungstyp testen, um sicherzustellen, dass die Buchung korrekt funktioniert. Es wird jedoch empfohlen, jede Buchungsprofiltransaktion und -kombination zu testen.

Beispiel: Sie haben zwei Kundenbuchungsprofile, von denen jedes drei Datensätze enthält, die für Kundengruppen spezifisch sind. In diesem Fall sollten Sie jeden Transaktionstyp testen.

**Buchungsprofile:**

- **GEN** – das allgemeine Buchungsprofil mit einer Gruppe für Mitarbeiter, einer für Kunden und einer für Intercompany. Jede Gruppe zeigt auf ein anderes Debitorenhandelskonto.
- **PRE** – das Vorauszahlungsbuchungsprofil mit einem Datensatz für alle Vorauszahlungen, der auf die Vorauszahlungskonten des Kunden verweist.

### <a name="testing-scenarios"></a>Testszenarien

- Freitextrechnung für einen Kunden in der **Mitarbeiter**-Gruppe, die das **GEN**-Buchungsprofil verwendet
- Freitextrechnung für einen Kunden in der **Mitarbeiter**-Gruppe, die das **PRE**-Buchungsprofil verwendet
- Auftragsrechnung für einen Kunden in der **Mitarbeiter**-Gruppe, die das **GEN**-Buchungsprofil verwendet
- Auftragsrechnung für einen Kunden in der **Mitarbeiter**-Gruppe, die das **PRE**-Buchungsprofil verwendet
- Debitorzahlungserfassung für einen Kunden in der **Mitarbeiter**-Gruppe, die das **GEN**-Buchungsprofil verwendet
- Debitorzahlungserfassung für einen Kunden in der **Mitarbeiter**-Gruppe, die das **PRE**-Buchungsprofil verwendet

Wiederholen Sie für das vorherige Beispiel ein Testszenario für jede Kundengruppe und wiederholen Sie jede Gruppe von Testszenarien für jeden zusätzlichen Transaktionstyp (z. B. Projektrechnungen und Servicemanagement).

## <a name="reconciling-the-ledger-to-the-subledger"></a>Abstimmen des Sachkontos mit dem untergeordneten Sachkonto

Das Sachkonto sollte in jeder Periode mit dem untergeordneten Sachkonto abgestimmt werden. Viele Module enthalten vorkonfigurierte Berichte, die für diesen Abgleich verwendet werden können. Abhängig von Ihren lokalen Anforderungen müssen Sie jedoch möglicherweise benutzerdefinierte Berichte entwickeln oder die vorhandenen Berichte erweitern, um Ihre Berichtsanforderungen zu erfüllen.

Wir empfehlen, dass Sie vor der tatsächlichen Aktivierung jedes Ihrer untergeordneten Sachkonten mit dem Sachkonto abgleichen. Wir empfehlen außerdem, dass Sie vor der ersten tatsächlichen Aktivierung eine Scheinumstellung aller offenen Salden und offenen Transaktionen durchführen. Als Teil dieses Prozesses sollten Sie eine vollständige Abstimmung durchführen, um sicherzustellen, dass die Migration von Salden und offenen Transaktionen mit den Altsystemen saldiert wird und dass alle untergeordneten Sachkonten mit dem Sachkonto saldieren, bevor neue Transaktionen erstellt werden.
