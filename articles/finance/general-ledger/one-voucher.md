---
title: Ein Beleg
description: Ein Beleg für Finanzerfassungen (allgemeine Erfassung, Anlagenerfassung, Kreditorenzahlungserfassung usw.) ermöglicht es Ihnen, mehrere untergeordnete Sachkontotransaktionen im Kontext eines einzelnen Belegs einzugeben.
author: kweekley
ms.date: 11/05/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerParameters, AssetProposalDepreciation
audience: Application User
ms.reviewer: roschlom
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: 8.0.2
ms.openlocfilehash: 978d0dc28f86860335a782bd2ddaa141ed639fe5
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344057"
---
# <a name="one-voucher"></a>Ein Beleg

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


## <a name="what-is-one-voucher"></a>Was ist ein Beleg?

Die vorhandene Funktion für Finanzerfassungen (allgemeine Erfassung, Anlagenerfassung, Kreditorenzahlungserfassung usw.) ermöglicht es Ihnen, mehrere untergeordnete Sachkontotransaktionen im Kontext eines einzelnen Belegs einzugeben (Kunden, Lieferant, Anlage, Projekt und Ban). Microsoft bezeichnet diese Funktionalität als *Ein Beleg*. Sie können einen einzelnen Beleg erstellen, indem Sie eine der folgenden Methoden verwenden:

- Richten Sie den Erfassungsnamen (**Hauptbuch** \> **Erfassungseinstellungen** \> **Erfassungsnamen**) ein, damit das Feld **Neuer Beleg** auf **Nur eine Belegnummer** festgelegt ist. Jede Position, die Sie der Erfassung hinzufügen, ist nun im selben Beleg einbezogen. Da jede Position demselben Beleg hinzugefügt wird, kann der Beleg als Beleg, Sammelrabatt als Konto/Gegenkonto der gleichen Position oder einer Kombination eingegeben werden.

    [![Einzelposition.](./media/same-line.png)](./media/same-line.png)

    > [!IMPORTANT]
    > Beachten Sie, dass die Definition von „Ein Beleg” **nicht** Fälle abdeckt, bei denen der Erfassungsname als **Nur eine Beleg-Nummer** eingerichtet ist, aber der Benutzer dann einen Beleg eingibt, der nur Sachkontentypen umfasst. In diesem Dokument bedeutet „Ein Beleg”, dass es einen Beleg gibt, der mehr als einen Lieferanten, Debitor, Bank, Anlage oder Projekt enthält.

- Geben Sie einen mehrzeiligen Beleg ein, wo es kein Gegenkonto gibt.

    [![Sammelrabatt-Beleg.](./media/Multi-line.png)](./media/Multi-line.png)

- Geben Sie einen Beleg ein, bei dem das Konto und das Gegenkonto eine Kontenart für untergeordnete Sachkonten enthält, beispielsweise **Lieferant**/**Lieferant**, **Debitor**/**Debitor**, **Lieferant**/**Debitor** oder **Bank**/**Bank**.

    [![Beleg für untergeordnetes Sachkonto.](./media/subledger.png)](./media/subledger.png)

## <a name="issues-with-one-voucher"></a>Abgänge mit einem Beleg

Die Funktion „Ein Beleg” verursacht Probleme beim Ausgleich bei der Steuerberechnung, Stornierungs-Transaktion, Abstimmung eines untergeordneten Sachkontos mit dem Hauptbuch, der Finanzberichterstellung usw. (Weitere Informationen zu Problemen, die während des Ausgleichs auftreten können, finden Sie unter [Einzelne Belege mit mehreren Debitoren oder Kreditoren](../accounts-payable/single-voucher-multiple-customer-vendor-records.md).) Um ordnungsgemäß zu funktionieren und zu berichten, erfordern diese Verfahren und Berichte Transaktionsdetails. Obwohl mehrere Szenarios unter Umständen weiterhin korrekt sind, abhängig von den Einstellungen Ihrer Organisation, gibt es oftmals Abgänge, wenn mehrere Buchungen in einen Beleg eingegeben werden.

Angenommen, Sie haben die folgenden mehrzeiligen Beleginformationen.

[![Beispiel eines mehrzeiligen Belegs.](./media/example.png)](./media/example.png)

Dann generieren Sie den Bericht **Ausgaben nach Kreditor** im Arbeitsbereich **Finanzinformationen**. Auf diesem Bericht sind Ausgabenkontosalden nach Lieferantengruppe und dann nach LIeferant gruppiert. Wenn der Bericht generiert wird, kann das System nicht bestimmen, bei welchen Kreditorengruppen/Kreditoren die Ausgabe von 250,00 anfiel. Da Buchungsdetails fehlen, geht das System davon aus, dass die gesamte Ausgabe von 250,00 vom ersten Lieferant angefallen ist, der im Beleg gefunden wurden. Deshalb wird die Ausgabe von 250,00, die im Saldo für das Hauptkonto 600120 enthalten ist, unter dieser Lieferantengruppe/diesem Lieferanten angezeigt. Es ist aber außerordentlich wahrscheinlich, dass der erste Lieferant im Beleg nicht der korrekte Lieferant ist. Deshalb ist der Bericht wahrscheinlich falsch.

[![Ausgaben nach Lieferantenbericht.](./media/expenses.png)](./media/expenses.png)

## <a name="the-future-of-one-voucher"></a>Die Zukunft von „Ein Beleg”

Aufgrund der Probleme, die bei der Verwendung eines Belegs auftreten können, wird diese Funktionalität möglicherweise nicht mehr unterstützt. Da jedoch funktionale Lücken vorhanden sind, die von diesen Funktionen abhängen, wird die Einstellung nicht auf einmal auftreten. Stattdessen können Sie den folgenden Zeitplan nutzen:

- **Freigabe Frühling 2018** – diese Funktionalität wurde standardmäßig durch den Parameter **Mehrere Transaktionen innerhalb eines Belegs zulassen** auf der Registerkarte **Allgemeines** der Seite **Hauptbuchparameter** deaktiviert. Allerdings können Sei sie wieder aktivieren, wenn in Ihrer Organisation ein Szenario besteht, das in eine der funktionalen Lücken fällt, die weiter unten in diesem Thema aufgeführt sind.

    - Wenn für Ihr Geschäftsszenario „Ein Beleg“ nicht erforderlich ist, empfehlen wir, die Funktionalität deaktiviert zu lassen. Wenn Sie diese Funktion verwenden, obwohl eine andere Lösung vorhanden ist, wird Microsoft keine „Fehler” in den Bereichen beheben, die später in diesem Thema identifiziert wurden.
    - Wir empfehlen, dass Sie die Verwendung von „Ein Beleg” für Integrationen einstellen, sofern Sie die Funktionalität nicht für die dokumentierten Funktionslücken benötigen.

- **Spätere Versionen** – einige dieser Geschäftsanforderungen können nur mithilfe von „Ein Beleg” erfüllt werden. Microsoft muss sicherstellen, dass alle identifizierten Geschäftsanforderungen im System noch erfüllt werden können, nachdem die Funktionalität eingestellt ist. Daher müssen wahrscheinlich neue Funktionen hinzugefügt werden, um funktionalen Lücken zu schließen. Microsoft kann keine spezifische Lösung bereitstellen, da jede Funktionslücke unterschiedlich ist und basierend auf den Geschäftsanforderungen bewertet werden muss. Einige Funktionslücken werden wahrscheinlich durch Funktionen ersetzt, die dazu beitragen, bestimmte Geschäftsanforderungen zu erfüllen. Andere Lücken können jedoch geschlossen werden, indem weiterhin der Eintrag in eine Erfassung ermöglicht wird, wie bei Verwendung eines Belegs, aber das System erweitert wird, um bei Bedarf detailliertere Informationen zu erhalten.

Nachdem alle Funktionslücken geschlossen wurden, teilt Microsoft mit, dass die Funktion nicht mehr unterstützt wird. Die Einstellung wird jedoch erst ein Jahr nach dieser Mitteilung wirksam. Obwohl Microsoft keine Schätzung darüber abgeben kann, wann die Funktionalität „Ein Beleg“ eingestellt werden wird, wird es wahrscheinlich mindestens zwei Jahre dauern, bis die Einstellung eintritt. Die Microsoft-Richtlinie sieht vor, dass zwischen der Ankündigung veralteter Funktionen und der tatsächlichen Ablehnung mindestens 12 Monate verbleiben, damit Kunden und unabhängige Softwareanbieter (ISVs) Zeit haben, auf die Änderung zu reagieren. So muss eine Organisation möglicherweise ihre Geschäftsprozesse, Entitäten und Integrationen aktualisieren.

Die Einstellung von „Ein Beleg“ ist eine wesentliche Änderung, die in großem Umfang kommuniziert wird. Im Rahmen dieser Kommunikation wird Microsoft dieses Thema aktualisieren und einen Blog-Beitrag im Microsoft Dynamics 365 Finance-Blog veröffentlichen, das Thema „Entfernte oder veraltete Funktionen“ aktualisieren, die Änderung auf entsprechenden Microsoft-Konferenzen mitteilen usw.

## <a name="why-use-one-voucher"></a>Warum „Ein Beleg” verwenden?

Auf Grundlage von Unterhaltungen mit Debitoren, hat Microsoft die folgende Liste von Szenarien kompiliert, in der Debitoren eine Belegfunktionen oder Gründe verwenden, warum sie diese verwenden. Einige dieser Geschäftsanforderungen können nur mithilfe von „Ein Beleg” erfüllt werden. Für viele Szenarien, können Alternativen die selben geschäftlichen Anforderungen erfüllen.

### <a name="scenarios-that-require-one-voucher"></a>Szenarien, die nicht „Ein Beleg” erfordern

Die folgenden Szenarien können nur mithilfe der Funktionalität „Ein Beleg” ausgeführt werden. Wenn Ihre Organisation eines dieser Szenarien hat, müssen Sie mehrere Transaktionen aktivieren, um sie in einen Beleg einzugeben, indem sie die Einstellungen **Mehrere Transaktionen in einem Beleg zulassen** auf der Seite **Hauptbuchparameter** ändern. Diese Funktionslücken werden in späteren Versionen durch andere Funktionen ausgefüllt.

> [!NOTE]
> [Für jedes der folgenden Szenarien muss das Feld **Mehrere Transaktionen innerhalb eines Belegs zulassen** im Feld **Allgemein** Inforegister auf der Seite **Hauptbuchparameter** auf Ja gesetzt sein.]

### <a name="post-vendor-or-customer-payments-in-summary-form-to-a-bank-account"></a>Formular Beitragsdebitorenzahlungszusammenfassung vom Bankkonto

**Szenario** Eine Organisation übermittelt eine Liste mit Kreditoren und Beträgen auf ihre Bank, und die Bank verwendet diese Liste, um Kreditoren im Auftrag der Organisation darzustellen. Die Bank bucht die Summe der Zahlungen als einzelne Entnahme beim Bankkonto.

Zusammenfassung von Kreditorenzahlungen wird nur durch „Ein Beleg” unterstützt. Jeder Kreditor wird als separate Position eingegeben, um Details im dem Kreditor untergeordneten Sachkonto zu verwalten. Allerdings wird der zusammengefassten Betrag für alle Zahlungen für eine einzelne Zeile für das Bankkonto gebucht. Daher ist die Entnahme in einem einzelnen zusammengefassten Betrag im untergeordneten Banksachkonto angezeigt.

**Szenario** Eine Organisation macht Debitorenzahlungen oder Bankguthabendebitorenzahlungen im Auftrag der Organisation und die Einzahlung wird als Pauschalbetrag für das Bankkonto angezeigt.

Zusammenfassung von Debitorenzahlungen wird in der Regel über die Einzahlungsfunktionalität unterstützt. Wenn Sie "Bridging" als Zahlungsmethode verwenden, wird dieses Szenarios nur über einen Beleg unterstützt. Die Debitorenzahlungen werden in derselben Weise eingegeben, die für die Kreditorenzahlungszusammenfassung beschrieben wird.

### <a name="mechanism-to-group-transactions-from-a-business-event"></a>Mechanismus, um Buchungen über ein Geschäftsereignis zu gruppieren

**Szenario** Eine Organisation hat ein einzelnes Geschäftsereignis, das mehrere Transaktionen auslöst. Allerdings möchte die Buchhaltungs die Buchhaltungseinträge zur besseren Überprüfung zusammen angezeigt.

Wenn eine Organisation der Buchhaltungseinträge eines Geschäftsereignisses zusammen anzeigt, muss diese einen Beleg verwenden. 

### <a name="country-specific-features"></a>Landesspezifische Funktionen

**Szenario** Bei der Funktion „Einheitspapier der Versandanmeldung” (SAD) für Polen ist es derzeit erforderlich, dass ein einziger Beleg verwendet wird. Bis eine Gruppierungsoption für diese Funktion verfügbar ist, müssen Sie weiterhin die Funktionalität „Ein Beleg” verwenden. Es gibt möglicherweise zusätzliche länderspezifische Funktionen, die die „Ein Beleg”-Funktionalität benötigen.

### <a name="customer-prepayment-payment-journal-that-has-taxes-on-multiple-lines"></a>Debitorenvorauszahlungszahlungserfassung, die Steuern auf mehreren " Positionen" anzeigen

In diesem Szenario sind die Debitoren im einzelnen Voucher derselbe Debitor, da die Buchung die Positionen eines Debitorenauftrags simuliert. Die Vorauszahlung muss in einem einzelnes Beleg eingegeben werden, da die Steuerberechnung für die „Positionen” der Einzelzahlung vorgenommen werden muss, die der Debitor leistete.

### <a name="customer-reimbursement"></a>Debitor-Rückerstattung

**Szenario** Ein Debitor erstellt eine Vorauszahlung für einen Auftrag, und die Positionen des Auftrags sind verschiedene Steuern, die für die Vorauszahlung erfasst werden müssen. Die Vorauszahlungsdebitorenzahlung ist eine Buchung, bei der die Positionen des Auftrags simuliert werden, sodass die entsprechende Steuer für den Beitrag auf jeder Position erfasst werden kann.

Wenn die periodische Aufgabe die Preiserstattung vom Debitorenmodul ausgeführt wird, erstellt sie eine Buchung, um den Saldo von einem Debitor zu einem Kreditor zu verschieben. Für dieses Szenario muss ein Beleg verwendet werden, um dem Debitor die Rückerstattung zu geben.

### <a name="fixed-asset-maintenance-catch-up-depreciation-split-asset-calculate-depreciation-on-disposal"></a>Erhaltung des Anlagenbestandes: Ausgleichsabschreibung, geteilte Anlage, berechnen der Abschreibung für Abgang
Ab Version 10.0.21 werden Transaktionen für Anlagen zum Nachholen der Abschreibung, zum Splitten einer Anlage und zum Berechnen der Abschreibung für den Abgang einer Anlage mit unterschiedlichen Belegnummern erstellt.

### <a name="bills-of-exchange-and-promissory-notes"></a>Wechsel und Solawechsel
Wechsel und Solawechsel verlangen, dass ein Beleg verwendet wird, da die Transaktion den Debitoren- bzw. Kreditorensaldo von einem Debitoren-/Kreditorsachkonto auf ein anderes verschiebt, basierend auf dem Status der Zahlung.

## <a name="scenarios-that-dont-require-one-voucher"></a>Szenarien, die nicht „Ein Beleg” erfordern

Die folgenden Szenarien können mit anderen Mitteln ausgeführt werden, udie nd sollten nicht „Ein Beleg” Funktionalität verwenden.

### <a name="post-customer-payments-in-summary-form-to-the-bank-account"></a>Formular Beitragsdebitorenzahlungszusammenfassung vom Bankkonto

Eine Organisation macht Debitorenzahlungen oder Bankguthabendebitorenzahlungen im Auftrag der Organisation und die Einzahlung wird als Pauschalbetrag für das Bankkonto angezeigt.

Zusammenfassung von Debitorenzahlungen wird durch die Einzahlungsfunktionalität unterstützt, wenn Transfer bei der Zahlungsmethode nicht verwendet wird.

### <a name="netting"></a>Saldierung

Die Salden für einen Kreditor und einen Debitor werden miteinander verrechnet, da der Kreditor und der Debitor von der gleichen Partei sind. Durch diesen Ansatz wird der Geldwechsel zwischen einer Organisation und der Debitoren-/Kreditorenpartei minimiert.

Netting kann abgewickelt werden, indem die Erhöhung und die Verringerung in separaten Belegen eingegeben wird und das Gegenkonto ein Sachkonto ist.

### <a name="post-in-summary-to-the-general-ledger"></a>Buchungszusammenfassung im Hauptbuch

Organisationen möchten häufig im Hauptbuch als Zusammenfassung buchen, um die angezeigte Datenmenge zu verringern. Allerdings verlangen die Organisationen in der Regel, dass die Buchungsdetails beibehalten werden. Wenn das Buchen zusammenfassend mit einem einzelnen Beleg erfolgt, sind die Buchungsdetails nicht bekannt und können nicht verwaltet werden.

- Da die Buchungsdetails aktuell nicht beibehalten werden können, wird empfohlen, dass die Organisation **One-Beleg nicht zum Buchen der Zusammenfassung verwendet**.
- Nachdem Support für einen Beleg entfernt wurde, können das Quelldokument und das Buchhaltungsframeworks in die Erfassungen der Organisation implementiert werden. Durch diese Frameworks werden dann die Transaktionsdetails und die Supportzusammenfassung im Hauptbuch verwaltet.


### <a name="settle-multiple-unposted-payments-to-the-same-invoice"></a>Gleichen Sie nicht gebuchte Zahlungen mit der gleichen Rechnung aus

Dieses Szenario findet sich in der Regel in Organisationen, in denen Kunden mehrere Zahlungsmethoden zur Bezahlung von Einkäufen verwenden können. In diesem Szenario muss die Organisation in der Lage sein, mehrere nicht gebuchte Zahlungen zu erfassen und mit der Debitorenrechnung auszugleichen.

Eine neue Fähigkeit, die in Microsoft Dynamics 365 for Operations Version 1611 (November 2016) ermöglicht es, dass mehrfach nicht gebuchte Zahlungen nicht mit einzelnen Rechnungen ausgeglichen werden. Mehrere Debitorenzahlungen müssen in einem einzelnen Dokument nicht mehr erfasst werden.

### <a name="import-bank-statement-transactions"></a>Bankauszugbuchungen importieren

Banken machen und erhalten häufig Zahlung einer Organisation, und diese Transaktionen werden in Finance durch eine Datei erfasst, die von der Bank empfangen wird. Organisationen möchten diese Transaktionen gruppieren, indem die Bankauszugsnummer in der Datei verwendet wird. Da jede Buchung im Detail auf dem Bankauszug angezeigt wird, ist keine bankuntergeordnete Zusammenfassung im Sachkonto erforderlich.

Buchungen können gruppiert werden, indem andere Felder in der Erfassung verwendet werden, wie beispielsweise die Erfassungschargennummer selbst oder die Dokumentnummer.


### <a name="transfer-balances"></a>Salden übertragen

Eine Organisation muss ggf. eine Bilanz von einem Kreditor an einem anderen Kreditor übertragen, entweder aufgrund eines Fehlers oder weil ein anderer Kreditor die Verbindlichkeiten übernommen hat. Übertragungen dieses Typs treten auch bei Kontentypen auf, wie beispielsweise **Debitoren** und **Bank**.

Saldo-Übertragungen von einem Konto (Kreditor, Debitor, Bankkonto, usw.) in ein anderes Konto können von separaten Belegen ausgeführt werden, und das Gegenkonto kann auf ein Sachkonto gebucht werden.

### <a name="enter-beginning-balances"></a>Anfangssalden eingeben

Organisationen geben häufig die Anfangssalden für Konten für untergeordnete Sachkonten (Debitoren, Kreditoren, Anlagen, usw.) als eine Belegbuchung ein. Anfangssalden der einzelnen Konten für untergeordnete Sachkonten können als separate Belege eingegeben werden, und das Gegenkonto kann gebucht werden auf ein Sachkonto.

### <a name="correct-the-accounting-entry-of-a-posted-customer-or-vendor-document"></a>Korrigieren Sie den Buchhaltungseintrag eines gebuchten Debitoren- oder Kreditorendokuments

Eine Organisation muss möglicherweise den Debitor oder ein Kreditorsachkonto für einen Buchhaltungseintrags einer gebuchten Rechnung korrigieren, aber diese Rechnung kann nicht durch einen anderen Mechanismus storniert werden oder korrigiert werden.

Wenn eine Korrektur des Debitor- oder Kreditorsachkonto vorgenommen wird, muss eine Regulierung auf das Sachkonto vorgenommen werden. Die Regulierung kann nicht vorgenommen werden, indem über den Kreditor oder Debitor gebucht wird. Dieser Ansatz erfordert, dass die Regulierung während einer „Ausfallzeit” vorgenommen wird, damit das Sachkonto vorübergehend die manuelle Eingabe zulassen kann.

### <a name="the-system-allows-it"></a>"Das System erlaubt es"

Organisationen verwenden häufig nur eine Belegfunktionen, da sie das System verwenden können, ohne die Auswirkungen zu veranschaulichen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
