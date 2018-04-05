---
title: Ein Beleg
description: "Ein Beleg für Finanzerfassungen (allgemeine Erfassung, Anlagenerfassung, Kreditorenzahlungserfassung usw.) ermöglicht es Ihnen, mehrere untergeordnete Sachkontotransaktionen im Kontext eines einzelnen Belegs einzugeben."
author: kweekley
manager: AnnBe
ms.date: 03/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 3831a6b5ec458495134b4b490d33a9acd76b6d2e
ms.openlocfilehash: 76ea8470786bd50896400a65564d698d96119d6f
ms.contentlocale: de-de
ms.lasthandoff: 03/20/2018

---

# <a name="one-voucher"></a>Ein Beleg

[!include[banner](../includes/banner.md)]

> [!NOTE]
>  Diese Funktionalität wird in Dynamics 365 for Finance and Operations Version 8.0 verfügbar sein, welche in der Version von Frühjahr 18 verfügbar sein wird.   

<a name="what-is-one-voucher"></a>Was ist „Ein Beleg”?
======================

Die vorhandene Funktion für Finanzerfassungen (allgemeine Erfassung, Anlagenerfassung, Kreditorenzahlungserfassung usw.) ermöglicht es Ihnen, mehrere untergeordnete Sachkontotransaktionen im Kontext eines einzelnen Belegs einzugeben. Diese Funktionalität wird als „Ein Beleg” bezeichnet. Sie können „Ein Beleg” erstellen, indem Sie eine der folgenden Methoden verwenden:

-   Richten Sie den Erfassungsnamen (**Hauptbuch** \> **Erfassungseinstellungen** \>**Erfassungsnamen**) ein, damit das Feld **Neuer Beleg** auf **Nur eine Belegnummer** festgelegt ist. Jede Position, die Sie der Erfassung hinzufügen, ist nun im selben Beleg einbezogen. Da jede Position demselben Beleg hinzugefügt wird, kann der Beleg als Beleg, Sammelrabatt als Konto/Gegenkonto der gleichen Position oder einer Kombination eingegeben werden.

[![Einzelposition](./media/same-line.png)](./media/same-line.png)

-   Geben Sie einen mehrzeiligen Beleg ein, wo es kein Gegenkonto gibt.

[![" Sammelrabatt-Beleg](./media/Multi-line.png)](./media/Multi-line.png)

-   Geben Sie einen Beleg ein, in der das Konto und das Gegenkonto eine Kontenart für untergeordnete Sachkonten ist, beispielsweise Kreditor, Debitor/Kreditor/Debitor, Kreditor/Debitor oder Bank/Bank.

[![Beleg für untergeordnetes Sachkonto](./media/subledger.png)](./media/subledger.png)

<a name="issues-with-one-voucher"></a>Abgänge mit einem Beleg
=======================

Die Funktion „Ein Beleg” verursacht Probleme bei Ausgleich, Steuerberechnung, Abstimmung eines untergeordneten Sachkontos mit dem Hauptbuch, der Finanzberichterstellung usw. (Für weitere Informationen zu Problemen, die während des Ausgleichs auftreten können, finden Sie unter[Einzelne Belege mit mehreren Debitoren oder Kreditoren](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/accounts-payable/single-voucher-multiple-customer-vendor-records).) Um ordnungsgemäß zu funktionieren und zu berichten, erfordern diese Verfahren und Berichte Buchungsdetails. Obwohl mehrere Szenarios unter Umständen weiterhin korrekt sind, basierend auf den Einstellungen Ihrer Organisation, gibt es oftmals Abgänge, wenn mehrere Buchungen in einen Beleg eingegeben werden.

Angenommen, Sie haben die folgenden mehrzeiligen Beleginformationen.

[![Beispiel](./media/example.png)](./media/example.png)

Dann generieren Sie den Bericht **Ausgaben nach Kreditor** im Arbeitsbereich **Finanzinformationen**. Das Berichtsgruppen-Ausgabenkonto gleicht unter Kreditorengruppe und dann Kreditor aus. Wenn der Bericht generiert wird, kann das System nicht bestimmen, bei welchen Kreditorengruppen/Kreditoren die Ausgabe von 250,00 anfiel. Da Buchungsdetails fehlen, geht das System davon aus, dass die gesamte 250,00 vom ersten Kreditor angefallen sind, die im Beleg gefunden wurden. Die 250,00, die im Saldo für das Hauptkonto 600120 enthalten sind, werden dann unter dieser Kreditorengruppe/Kreditor angezeigt. Es ist außerordentlich wahrscheinlich, dass der Beleg im ersten Kreditor nicht der korrekte Kreditor ist, sodass der Bericht falsch.

[![Ausgaben](./media/expenses.png)](./media/expenses.png)

<a name="the-future-of-one-voucher"></a>Die Zukunft von „Ein Beleg”
=========================

Aufgrund der Abgänge, die früher angegeben wurden, werden die Belegfunktionen als veraltet vorgenommen. Da jedoch funktionale Lücken vorhanden sind, die von diesen Funktionen abhängen, werden die Funktionen nicht auf einmal verworfen. Stattdessen können Sie den folgenden Zeitplan nutzen: 

-   **Version Frühlinges 2018** – Die Funktionen werden standardmäßig durch einen Hauptbuchparameter deaktiviert. Allerdings kann diese Funktion aktiviert werden, wenn in Ihrer Organisation ein Szenario besteht, das in die Geschäftsszenariolücken sinkt, die weiter unten in diesem Thema aufgeführt sind.

    -   Wenn ein Debitor ein Geschäftsszenario hat, das keinen Beleg erfordert, wechseln Sie nicht die Funktionen. Es werden keine „Fehler” in den Bereichen behoben, die später in diesem Thema identifiziert wurden, wenn diese Funktion verwendet wird, obwohl eine andere Lösung vorhanden ist.

    -   Beenden Sie die Verwendung von „Ein Beleg” für Integrationen in Microsoft Dynamics 365 Finance and Operations, sofern die Funktionalität nicht für eine der Funktionslücken erforderlich ist.

-   **Herbst 2018 und später Versionen** – Die funktionalen Lücken werden ausgefüllt. Nachdem die funktionalen Lücken ausgefüllt sind, wird die Belegfunktionen dauerhaft deaktiviert.

<a name="why-use-one-voucher"></a>Warum „Ein Beleg” verwenden?
====================

Auf Grundlage von Unterhaltungen mit Debitoren, haben wir die folgende Liste von Szenarien kompiliert, in der Debitoren eine Belegfunktionen oder -Gründe verwenden, warum sie diese verwenden. Einige dieser Geschäftsanforderungen können nur mithilfe von „Ein Beleg” erfüllt werden. Für viele Szenarien, können Alternativen die selben geschäftlichen Anforderungen erfüllen.

<a name="scenarios-that-require-one-voucher"></a>Szenarien, die nicht „Ein Beleg” erfordern
----------------------------------

Die folgenden Szenarien können nur mithilfe der Funktionalität „Ein Beleg” ausgeführt werden. Diese Funktionslücken werden in der Version von Herbst 2018 und späteren Versionen durch andere Funktionen ausgefüllt.

-   **Formular Beitragsdebitorenzahlungszusammenfassung vom Bankkonto**

    -   Eine Organisation übermittelt eine Liste mit Kreditoren und Beträgen auf ihre Bank, und die Bank verwendet diese Liste, um Kreditoren im Auftrag der Organisation darzustellen. Die Bank bucht die Summe der Zahlungen als einzelne Entnahme beim Bankkonto.

>   Zusammenfassung von Kreditorenzahlungen wird nur durch „Ein Beleg” unterstützt. Jeder Kreditor wird als separate Zeile eingegeben, um die Details im Kreditorenkonto zu behalten, aber der zusammengefasste Betrag für alle Zahlungen für eine einzelne Zeile für das Bankko.gebucht wird. Daher ist die Entnahme in einem einzelnen zusammengefassten Betrag im untergeordneten Banksachkonto angezeigt.

-   Eine Organisation macht Debitorenzahlungen oder Bankguthabendebitorenzahlungen im Auftrag der Organisation und die Einzahlung wird als Pauschalbetrag für das Bankkonto angezeigt.

>   Zusammenfassung von Debitorenzahlungen wird in der Regel über die Einzahlungsfunktionalität unterstützt. Wenn Sie "Bridging" als Zahlungsmethode verwenden, wird dieses Szenarios nur über einen Beleg unterstützt. Die Debitorenzahlungen werden in derselben Weise eingegeben, die für die Kreditorenzahlungszusammenfassung beschrieben wird.

-   **Mechanismus, um Buchungen über ein Geschäftsereignis zu gruppieren**

    -   Eine Organisation hat ein einzelnes Geschäftsereignis, das mehrere Buchungen auslöst. Allerdings möchte die Buchhaltungs die Buchhaltungseinträge zur besseren Überprüfung zusammen angezeigt.

>   Wenn eine Organisation der Buchhaltungseinträge eines Geschäftsereignisses zusammen anzeigt, muss diese einen Beleg verwenden. 

-   **Landesspezifische Funktionen**

 -   Bei der Funktion „Einheitspapier der Versandanmeldung” (SAD) für Polen ist es derzeit erforderlich, dass ein einziger Beleg verwendet wird. Bis eine Gruppierungsoption für diese Funktion verfügbar ist, müssen Sie weiterhin die Funktionalität „Ein Beleg” verwenden. Es gibt möglicherweise zusätzliche länderspezifische Funktionen, die die „Ein Beleg”-Funktionalität benötigen.

-   **Debitorenvorauszahlungszahlungserfassung, die Steuern auf mehreren " Positionen" anzeigen**

 -   Ein Debitor erstellt eine Vorauszahlung für einen Auftrag, und die Positionen des Auftrags sind verschiedene Steuern, die für die Vorauszahlung erfasst werden müssen. Die Vorauszahlungsdebitorenzahlung ist eine Buchung, bei der die Positionen des Auftrags simuliert werden, sodass die entsprechende Steuer für den Beitrag auf jeder Position erfasst werden kann.

In diesem Szenario sind die Debitoren im einzelnen Voucher derselbe Debitor, da die Buchung die Positionen eines Debitorenauftrags simuliert. Die Vorauszahlung muss in einem einzelnes Beleg eingegeben werden, da die Steuerberechnung für die „Positionen” der Einzelzahlung vorgenommen werden muss, die der Debitor leistete.

-   **Erhaltung des Anlagenbestandes: Ausgleichsabschreibung, geteilte Anlage, berechnen der Abschreibung für Abgang**

Mit den folgenden Anlagenbuchungen werden auch mehrere Transaktionen innerhalb eines Einzelbelegs erstellt:
-   Eine zusätzliche Anschaffung wird in einer Anlage vorgenommen und die "Ausgleichs" Abschreibung wird berechnet.
-   Eine Anlage wird aufgeteilt.
-   Ein Parameter, um die Abschreibung nach Verwendung zu berechnen wird aktiviert und anschließend wird die Anlage abgeschafft.

<a name="scenarios-that-dont-require-one-voucher"></a>Szenarien, die nicht „Ein Beleg” erfordern
----------------------------------------

Die folgenden Szenarien können mit anderen Mitteln ausgeführt werden, und es sollte nicht „Ein Beleg” verwendet werden.

-   **Formular Beitragsdebitorenzahlungszusammenfassung vom Bankkonto**

Eine Organisation macht Debitorenzahlungen oder Bankguthabendebitorenzahlungen im Auftrag der Organisation und die Einzahlung wird als Pauschalbetrag für das Bankkonto angezeigt.

Zusammenfassung von Debitorenzahlungen wird durch die Einzahlungsfunktionalität unterstützt, wenn Transfer bei der Zahlungsmethode nicht verwendet wird.

-   **Saldierung**

Die Salden für einen Kreditor und einen Debitor werden miteinander verrechnet, da der Kreditor und der Debitor von der gleichen Partei sind. Durch diesen Ansatz wird der Geldwechsel zwischen einer Organisation und der Debitoren-/Kreditorenpartei minimiert.

Netting kann abgewickelt werden, indem die Erhöhung und die Verringerung in separaten Belegen eingegeben wird und das Gegenkonto ein Sachkonto ist.

-   **Buchungszusammenfassung im Hauptbuch**

Organisationen möchten häufig im Hauptbuch als Zusammenfassung buchen, um die angezeigte Datenmenge zu verringern. Allerdings verlangen die Organisationen in der Regel, dass die Buchungsdetails beibehalten werden. Wenn das Buchen zusammenfassend mit einem einzelnen Beleg erfolgt, sind die Buchungsdetails nicht bekannt und können nicht verwaltet werden.

   -   Da die Buchungsdetails aktuell nicht beibehalten werden können, wird empfohlen One-Beleg nicht zu verwenden, der zum Buchen der Zusammenfassung verwendet wird.
   -   Nachdem Support für einen Beleg entfernt wurde, können wir die Quelldokument und Buchhaltungsframeworks in die Erfassungen der Organisation implementieren. Durch diese Frameworks werden dann die Buchungsdetails und die Supportzusammenfassung in das Hauptbuch verwaltet.

-   **Gleichen Sie nicht gebuchte Zahlungen mit der gleichen Rechnung aus**

Dieses Szenario ist normalerweise bei Einzelhandelsorganisationen anzutreffen, wo Debitoren mehrere Zahlungsmethoden verwenden können, um für Einkäufe zu bezahlen. In diesem Szenario muss die Organisation in der Lage sein, mehrere nicht gebuchte Zahlungen zu erfassen und mit der Debitorenrechnung auszugleichen.

Eine neue Fähigkeit, die in Microsoft Dynamics 365 for Operations Version 1611 (November 2016) ermöglicht es, dass mehrfach nicht gebuchte Zahlungen nicht mit einzelnen Rechnungen ausgeglichen werden. Mehrere Debitorenzahlungen müssen in einem einzelnen Dokument nicht mehr erfasst werden.

-   **Bankauszugbuchungen importieren**

Banken machen und erhalten häufig Zahlung einer Organisation, und die Buchungen werden im Bereich Finance and Operations durch eine Datei erfasst, die von der Bank eingeht. Organisationen möchten diese Transaktionen gruppieren, indem die Bankauszugsnummer in der Datei verwendet wird. Da jede Buchung im Detail auf dem Bankauszug angezeigt wird, ist keine bankuntergeordnete Zusammenfassung im Sachkonto erforderlich.

Buchungen können gruppiert werden, indem andere Felder in der Erfassung verwendet werden, wie beispielsweise die Erfassungschargennummer selbst oder die Dokumentnummer.

-   **Salden übertragen**

Eine Organisation muss ggf. eine Bilanz von einem Kreditor an einem anderen Kreditor übertragen, entweder aufgrund eines Fehlers oder weil ein anderer Kreditor die Verbindlichkeiten übernommen hat. Übertragungen dieses Typs treten auch bei Kontentypen auf, wie beispielsweise Debitoren- und Bankkonten.

Saldo-Übertragungen von einem Konto (Kreditor, Debitor, Bankkonto, usw.) mit einem anderen Konto können von separaten Belegen ausgeführt werden, und das Gegenkonto kann gebucht werden auf ein Sachkonto.

-   **Anfangssalden eingeben**

Organisationen geben häufig die Anfangssalden für Konten für untergeordnete Sachkonten (Debitoren, Kreditoren, Anlagen, usw.) als eine Belegbuchung ein. Anfangssalden der einzelnen Konten für untergeordnete Sachkonten können als separate Belege eingegeben werden, und das Gegenkonto kann gebucht werden auf ein Sachkonto.

-   **Korrigieren Sie den Buchhaltungseintrag eines gebuchten Debitoren- oder Kreditorendokuments**

Eine Organisation muss möglicherweise den Debitor oder ein Kreditorsachkonto für einen Buchhaltungseintrags einer gebuchten Rechnung korrigieren, aber diese Rechnung kann nicht durch einen anderen Mechanismus storniert werden oder korrigiert werden.

Wenn eine Korrektur des Debitor- oder Kreditorsachkonto vorgenommen wird, muss eine Regulierung auf das Sachkonto vorgenommen werden. Die Regulierung kann nicht vorgenommen werden, indem über den Kreditor oder Debitor gebucht wird. Dieser Ansatz erfordert, dass die Regulierung während einer „Ausfallzeit” vorgenommen wird, damit das Sachkonto vorübergehend die manuelle Eingabe zulassen kann.

-   **"Das System erlaubt es"**

Organisationen verwenden häufig nur eine Belegfunktionen, da sie das System verwenden können, ohne die Auswirkungen zu veranschaulichen.

