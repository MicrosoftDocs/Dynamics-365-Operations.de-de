---
title: SEPA-Direktbelastungsüberblick
description: Der einheitliche Euro-Zahlungsverkehrsraum (SEPA) wird von der Europäischen Kommission eingerichtet und schreibt vor, dass alle elektronischen Zahlungen als Inland gelten, unabhängig vom Land/Region, wo die Person, Geschäfte, oder Organisation und die Bank sich befinden. Es gibt keine Differenz zwischen nationalen und grenzüberschreitenden Zahlungen. Zu SEPA zählen die 28 Mitgliedsstaaten der Europäischen Union (EU) sowie Island, Liechtenstein, Norwegen, die Schweiz, Monaco und San Marino. SEPA hilft dabei, einen gemeinsamen Markt für Zahlungsbuchungen innerhalb des europäischen Wirtschaftsraums (EEA) zu bilden. Letztlich wird von SEPA erwartet, die Anzahl von Zahlungsformaten zu reduzieren, mit denen Banken, Unternehmen und Personen arbeiten müssen.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, CustBankAccounts, CustParameters, CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 11144
ms.assetid: 3277c9b6-e46e-40c9-aa76-9b0449467842
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fcb7585d344988e00093231f785c1a746226e4e0
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836642"
---
# <a name="sepa-direct-debit-overview"></a>SEPA-Direktbelastungsüberblick

[!include [banner](../includes/banner.md)]

Der einheitliche Euro-Zahlungsverkehrsraum (SEPA) wird von der Europäischen Kommission eingerichtet und schreibt vor, dass alle elektronischen Zahlungen als Inland gelten, unabhängig vom Land/Region, wo die Person, Geschäfte, oder Organisation und die Bank sich befinden. Es gibt keine Differenz zwischen nationalen und grenzüberschreitenden Zahlungen. Zu SEPA zählen die 28 Mitgliedsstaaten der Europäischen Union (EU) sowie Island, Liechtenstein, Norwegen, die Schweiz, Monaco und San Marino. SEPA hilft dabei, einen gemeinsamen Markt für Zahlungsbuchungen innerhalb des europäischen Wirtschaftsraums (EEA) zu bilden. Letztlich wird von SEPA erwartet, die Anzahl von Zahlungsformaten zu reduzieren, mit denen Banken, Unternehmen und Personen arbeiten müssen.   

<a name="what-is-the-goal-of-sepa-direct-debits"></a>Was ist das Ziel der SEPA-Direktbelastungen?
---------------------------------------

Eine SEPA-Direktbelastung erlaubt einem Kreditgeber Mittel vom Bankkonto eines Debitors einzuziehen, vorausgesetzt, dass eine signierte Einzugsermächtigung dem Kreditor vom Debitor gewährt wurde. Der Debitor signiert eine Einzugsermächtigung, die den Lieferanten autorisiert, eine Zahlung einzuziehen und die Bank des Debitors anweist, die Sammlung zu bezahlen. 

SEPA-Direktbelastungen erstellen zum ersten Mal ein Zahlungsmittel, das für nationale und grenzüberschreitenden Eurodirektbelastungen in den 32 SEPA-Ländern/Regionen verwendet werden kann. 

Es gibt zwei verfügbare Schemata: das SEPA-Kern-Direktbelastungs-Schema und das SEPA Business-to-Business (B2B)-Direktbelastungsschema. Beide Schemata verwenden das gleiche Dateiformat.

## <a name="what-is-the-core-direct-debit-scheme"></a>Was ist das Kern-Direktbelastungsschema?
Das SEPA-Kern-Direktbelastungs-Schema ist das grundlegende Schema. Es weist die folgenden Attribute auf:
-   Die Übertragung von Geldbeträgen erfolgt in Euro (obwohl die Bankkonten möglicherweise auf andere Währungen lauten).
-   Der Debitor und der Kreditgeber müssen ein Konto bei einem Kreditinstitut im SEPA-Raum besitzen.
-   Der Debitor muss dem Kreditgeber eine signierte Einzugsermächtigung gewähren.
-   Einzugsermächtigungen laufen 36 Monate nach dem letzten initiierten Inkasso ab.
-   Der Kreditgeber muss Einzugsermächtigungen so lange speichern, wie die Einzugsermächtigung gültig ist, und für mindestens 14 Monate nach dem letzten Inkasso.
-   Das Schema wird für die einzelnen (einmalig) oder sich wiederholenden Direktbelastungsinkassos verwendet werden.
-   Debitoren haben ein "keine Fragen stellen"-Recht um eine Rückerstattung für bis zu acht Wochen nach dem Soll ihres Kontos zu erhalten.

## <a name="what-is-the-sepa-business-to-business-b2b-direct-debit-scheme"></a>Was ist das SEPA Business-to-Business (B2B) Direktbelastungschema?
Das Direktbelastungs-Schema SEPA B2B gilt den Business-to-Business-Transaktionen und basiert auf dem SEPA-Kern-Direktbelastungs-Schema. Die Hauptunterschiede sind:
-   Das Direktbelastungs-Schema SEPA B2B ist nicht zulässig, wenn der Debitor eine Privatperson (Kunden) ist.
-   Der Debitor ist nicht bevollmächtigt, eine Rückerstattung einer autorisierten Transaktion zu erhalten.
-   Debitorenbanken müssen sicher stellen, ob das Inkasso autorisiert ist, indem sie das Inkasso mit den Einzugsermächtigungsinformationen gegen prüfen. Debitorenbanken und Debitoren werden benötigt, der Prüfung zuzustimmen, die für jede Direktbelastung ausgeführt wird.
-   Das Schema bietet eine kürzere Zeitachse für das Anzeigen von Direktbelastungen und reduziert die Wiederkehrperiode.

## <a name="can-i-use-the-cor1-scheme-for-direct-debit-mandates"></a>Kann ich das Schema COR1 für Direkteinzugsmandate verwenden?
Ja. Sie können das Schema COR1 für SEPA-Direktbelastungseinzugsermächtigungen in Österreich, in Belgien, Deutschland, Frankreich, in Italien, Spanien und in den Niederlanden verwenden. Das Schema bietet einen kürzeren Vorbenachrichtigungszeitraum für den Direktbelastungsinkasso für den Kreditor.

## <a name="what-are-international-bank-account-numbers-iban-and-bank-identifier-codes-bic"></a>Was sind internationale Bankkontonummern (IBAN) und Bankleitzahlen (BIC)?
Die International Bank Account Number (IBAN) und Bank Identifier Code (BIC) werden verwendet, um den entsprechenden Konto in den 32 SEPA-Ländern/Regionen zu identifizieren. In SWIFT-Code geben Sie den BIC und im Feld IBAN die IBAN ein. Beide Felder befinden sich im Inforegister Zusätzliche Kennung auf der Registerkarte Bankkonto in der Seite Bankkonten. Dies gilt für das Bankkonto des Kreditors und das Bankkonto des Debitors.

## <a name="where-do-i-enter-creditor-identifiers-direct-debit-ids"></a>Wo gebe ich Gläubigerkennungen ein (Direktbelastungs-ID)?
Im SEPA wird jeder Kreditgeber durch eine eindeutige Gläubigerkennung identifiziert. Diese Kennung ermöglicht dem Debitor und dem Debitor-Bankfilter jede Direktbelastung und dann verarbeitet oder lehnt sie die Abbuchung gemäß Debitorenanweisungen zurück. Kreditgeber müssen diese Kennung durch ihre Bank anfordern. Geben Sie diese Kennung in das Feld Bankeinzugskennung für das Bankkonto für die juristische Person ein.

## <a name="what-are-mandates"></a>Was sind Einzugsermächtigungen?
Der Debitor signiert eine Einzugsermächtigung, die den Lieferanten autorisiert, eine Zahlung einzuziehen und die Bank des Debitors anweist, die Sammlung zu bezahlen. Der Debitor kann die Einzugsermächtigung in der Papierform ausstellen oder auf elektronischem Wege. Standardmäßig läuft die Einzugsermächtigung nach 36 Monaten ab, nachdem die Abbuchung zuletzt ausgelöst wurde.

## <a name="where-do-i-specify-the-sepa-direct-debit-file-format-iso-20022"></a>Wo gebe ich das SEPA-Direktbelastungsdateiformat an (ISO 20022)?
Die SEPA-Datenformate basieren auf den Standards der Nachricht ISO 20022. Sie aktivieren das Generische elektronische Berichterstellung-Kontrollkästchen und wählen das SEPA-Banküberweisungsformat als Exportformatkonfiguration aus, wenn Sie die Zahlungsmethoden für Kreditoren konfigurieren. Sie verwenden diese Zahlungsmethode, wenn Sie eine Zahlungsdatei in einer Debitoren-Zahlungserfassung generieren.

## <a name="in-what-file-formats-can-i-generate-sepa-direct-debit-payment-files"></a>In welchen Dateiformaten kann ich SEPA-Direktbelastungsdateien generieren?
Sie können Dateien für elektronische Zahlung für SEPA-Direktbelastungen in den folgenden Formaten generieren:
-   Sie können SEPA-Direktbelastungsdateien im XML-Dateiformat PAIN.008.001.02 für Belgien, Deutschland, Finnland, Frankreich, Italien und die Niederlande generieren.
-   SEPA-Direktbelastungszahlung archiviert im Format der XML-Datei PAIN.008.001.02 für Österreich und im Format der XML-Datei PAIN.008.003.02 für Deutschland.

## <a name="how-do-refunds-and-returns-work-with-sepa-direct-debits"></a>Wie arbeiten Rückerstattungen und Rücklieferungen mit der SEPA-Direktbelastung?
Unter beiden SEPA-Direktbelastungsschemen besitzen Debitoren bestimmte Rechte für Rückerstattungen. Der Debitor darf, ohne einen Grund dafür geben zu müssen, alle autorisierten Transaktionen während einer achtwöchigen Periode nach dem Fälligkeitsdatum zurückrufen. Im Falle der nicht autorisierten Transaktionen wird die Periode zu 13 Monate nach dem Fälligkeitsdatum erweitert. Rückbuchungen sämtlicher Zahlungen, die gemacht wurden, werden manuell vorgenommen, indem die Schaltfläche „Zahlung stornieren“ auf der Seite „Debitorenbuchungen“ verwendet wird.





