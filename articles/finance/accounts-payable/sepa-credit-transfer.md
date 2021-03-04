---
title: Überblick zur SEPA-Kreditübertragung
description: Dieser Artikel stellt allgemeine Informationen zu ISO 20022-Banküberweisungen bereit, die SEPA (Single Euro Payments Area) Banküberweisungen und alle sonstigen elektronische Zahlungen für Kreditoren umfassen. Eine SEPA-Überweisung ist eine Zahlung (in Euro) von einem Unternehmen oder von Einzelperson zu einem anderen Unternehmen oder einer Einzelperson. Der Artikel beschreibt zudem, wie eine SEPA-Überweisung-Zahlungsdatei eingerichtet und übermittelt wird.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, VendPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 11124
ms.assetid: 36b0f870-16d4-4bbb-8da5-e747e69b970d
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f0fc01508bd206f750a4101521cd9dff7b647656
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443524"
---
# <a name="sepa-credit-transfer-overview"></a>Überblick zur SEPA-Kreditübertragung

[!include [banner](../includes/banner.md)]

Dieser Artikel stellt allgemeine Informationen zu ISO 20022-Banküberweisungen bereit, die SEPA (Single Euro Payments Area) Banküberweisungen und alle sonstigen elektronische Zahlungen für Kreditoren umfassen. Eine SEPA-Überweisung ist eine Zahlung (in Euro) von einem Unternehmen oder von Einzelperson zu einem anderen Unternehmen oder einer Einzelperson. Der Artikel beschreibt zudem, wie eine SEPA-Überweisung-Zahlungsdatei eingerichtet und übermittelt wird.

## <a name="what-is-a-credit-transfer-message"></a>Was ist eine SEPA-Mitteilung?
Die Banküberweisungsnachricht ist eine Anforderung, die eine initiierende Partei (Ihr Unternehmen) zum Verschieben von einem separaten Konto zu einem Kreditgeber sendet. Es gibt viele länder-/regionsspezifische und bankspezifisch Implementierungen von Banküberweisungsnachrichten. Viele hiervon werden innerhalb eines Landes/Regionen verwendet, und werden Standards. Ein Standard ist globaler ISO 20022 und seine Startnachrichten, z.B. Banküberweisung. Die folgende Abbildung zeigt die Beziehungen und Disposition für die ausgewählte Banküberweisungsnachrichten angezeigt. 
![Credit tansfer](./media/credit-transfer.jpg) Kreditübertragungsnachrichten 

## <a name="what-are-iso-20022-and-sepa-payments"></a>Was sind ISO 20022 SEPA-Zahlungen?
Single Euro Payments Area (SEPA) wurde von der Europäischen Kommission eingerichtet und schreibt vor, dass alle elektronischen Zahlungen als Inlandszahlungen gelten, unabhängig vom Land/von der Region in der sich die Person, das Unternehmen oder die Organisation und die Bank befindet. Es gibt keine Differenz zwischen nationalen und grenzüberschreitenden Zahlungen. Zu SEPA zählen die 28 Mitgliedsstaaten der Europäischen Union (EU) sowie Island, Liechtenstein, Norwegen, die Schweiz, Monaco und San Marino. SEPA hilft dabei, einen gemeinsamen Markt für Zahlungsbuchungen innerhalb des europäischen Wirtschaftsraums (EEA) zu bilden. Letztlich wird von SEPA erwartet, die Anzahl von Zahlungsformaten zu reduzieren, mit denen Banken, Unternehmen und Personen arbeiten müssen. Die Europäische Kommission hat die Rechtsgrundlage für SEPA-Zahlungen über die Payment Services-Direktive (PSD) definiert. Der European Payments Council (EPC) unterstützt SEPA durch die folgenden Aktivitäten:

-   Er legt die Standards für elektronische SEPA-Zahlungen über das XML-Format ISO 20022 Universal-Nachrichtenschema für die Finanzindustrie fest.
-   Er richtet Regeln und Richtlinien zur die Behandlung von Eurozahlungen ein.

Der EPC besteht aus europäischen Banken und entwickelt das Handels- und das technische Framework für SEPA-Zahlungsmittel. Es werden drei Typen SEPA-Zahlungen verwendet:

-   Überweisungen
-   Bankeinzug
-   Karten

## <a name="what-is-a-sepa-credit-transfer"></a>Was ist eine SEPA-Überweisung?
Eine SEPA-Überweisung ist eine Zahlung von einem Unternehmen oder von Einzelperson zu einem anderen Unternehmen oder einer Einzelperson. Zahlungen müssen in Euro durchgeführt werden und sie müssen die internationale Bankkontonummer (IBAN) und Bank Identifier Code (BIC) für beide Parteien enthalten. (Die BIC ist auch als Society for Worldwide Interbank Financial Telecommunication \[SWIFT\] Code bekannt.) Darüber hinaus müssen Buchungskosten zwischen beiden Parteien freigegeben werden. Banküberweisungen zwischen Parteien sollten XML-Dateien verwenden, die den ISO 20022-Standards zu Zahlungsverarbeitung entsprechen und das durch das EPC festgelegt XML-Format verwenden.

## <a name="how-is-a-credit-transfer-implemented"></a>Wie wird eine Überweisung implementiert?
Das SEPA-Überweisungsformat wird über die generische elektronische Berichterstellung und die Methoden von Zahlungsfunktionen in Microsoft Dynamics 365 Finance implementiert. Einige Banküberweisungsformate, die in anderen Regionen noch verwendet werden, verwenden Sie das vorhandene Zahlungsframework. Unter vielen anderen Formaten gibt es zwölf ISO 20022-Banküberweisungsdateiformate, die verfügbar sind. Diese Exportformate entsprechen dem XML-Standard SEPA ISO 20022. Sie werden verwendet, um Nicht-Euro-Zahlungsüberweisungen für Land/Region zu generieren, in denen sie Eurozahlungen und verwendet werden, z.B. in der Version 8,2 der SEPA-Kredit-Übertragungssystem-Regelung der EPC. Bevor Sie die Überweisungen implementieren können, müssen Sie von Ihrer Bank die Software erhalten, die erforderlich ist, um elektronisch Bankdateien hochzuladen. Sie verwenden diese Software, um XML-Dateien zu übertragen, die Zahlungen an die Bank enthalten.

## <a name="what-credit-transfer-formats-are-currently-supported"></a>Welche Kreditübertragungsformate werden derzeit unterstützt?
Sie sollten für die Bibliothek der freigegebenen Anlage auf Microsoft Dynamics Lifecycle Services (LCS) nutzen und die neuesten Liste der verfügbaren Dateien mit dem Anlagentyp **GER-Konfiguration** sehen. Im nächsten Abschnitt "Was muss ich einrichten?" wird ein Link zum Thema bereitgestellt, der erläutert, wie ein LCS-Repository herstellt, um verfügbare Konfigurationen und Importieren ausgewählter Konfigurationen zu prüfen.

## <a name="what-do-i-have-to-set-up"></a>Was muss ich einrichten?
-   Bevor Sie Überweisungsdateien erstellen können, muss mindestens eine aktive Banküberweisungskonfiguration in die generischen elektronischen Berichterstellungskonfigurationen importiert werden. Weitere Informationen finden Sie unter [Elektronische Berichtskonfigurationen aus Lifecycle Services herunterladen](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).
-   Wenn Sie Kreditorenkonten-Zahlungsmethoden konfigurieren, wählen Sie die **Elektronische Berichterstellung**-Kontrollkästchen und wählen das passende Banküberweisungsformat (z. B. **ISO 20022 Credit transfer (AT)**)
-   Sie müssen die juristische Person und die Bankkontoinformationen einrichten.
-   Kontonummern, IBAN und manchmal SWIFT-Codes (BICs) oder andere Nummern werden benötigt, um spezifische Kredittransferzahlungen zu erstellen. Daher müssen diese für das Bankkonto des Kreditors einrichten und das Bankkonto der Organisation, die die Übertragung angefordert werden.
-   Zusätzliche Informationen kann, beispielsweise die Mehrwertsteuer (VAT)- Nummern für die Parteien erforderlich, die in der Banküberweisungsnachricht gemeldet werden. Diese Anpassung muss für Kreditoren und für die juristische Person eingerichtet werden, wenn sie angefordert hat.
-   Einige Kreditorzahlungsmethoden (größtenteils ISO 20022 - basierend Zahlungsmethoden), erfordern ggf. zusätzliche Einstellungen für **Zahlungsformat-Codesätze** wie **Dienstleistungstypen** = **SLEV**. Diese Codes verwendet werden,als zusätzliche Markierung für Zahlungsbuchungen während des Zahlungs verarbeitens. Standardwerte aus Zahlungscodes, wie **Kategoriezweck**, **Zuschlagsträger**, **Lokales Instrument** und **Servicelevel** können in zwei Orte festgelegt werden. Der erste Ort ist **Kreditorenzahlungserfassungskopf** und der zweite ist **Kreditorenkontenmethoden für Zahlungen**. Nach Erstellung Zahlungserfassungspositionen, werden die Zahlungscodewerte, die auf Zahlungserfassungskopf festgelegt werden, in eine Erfassungsposition, wenn sie, nicht die Werte von den Zahlungsmethoden festgelegt werden, übertragen werden verwendet.

## <a name="what-parameters-are-available-for-generating-credit-transfer-payments"></a>Die Parameter sind für das Generieren von Überweisungen verfügbar?
Die Liste bestimmter Parameter hängt vom Banküberweisungsformat ab. In der folgenden Tabelle werden die Parameter aufgeführt, die Sie verwenden können, wenn Sie eine ISO 20022-Überweisung in einer Kreditorenzahlungserfassung für Deutschland generieren. Wenn Sie die Optionen verwenden, die auf der Registerkarte **Ausführung im Hintergrund** verfügbar sind, können Sie Zahlungsgenerierung im Stapelverarbeitungsmodus ausführen.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Feld</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Stapelbuchung</td>
<td>Aktivieren Sie dieses Kontrollkästchen, um den Stapelbuchung-Tag in der XML-Datei einzufügen.</td>
</tr>
<tr class="even">
<td>Bearbeitungsdatum</td>
<td>Geben Sie das Datum ein, an dem die Bank die Zahlungen verarbeitet soll.</td>
</tr>
<tr class="odd">
<td>Format</td>
<td>Wählen Sie das Format für Rimesseinformationen entsprechend der Anforderungen Ihres Land/Region oder Bank aus:
<ul>
<li><strong>Strt</strong> – Wählen Sie diese Option, um das strukturierte Format zu verwendet, wenn eine Zahlungsposition eine Rechnung ausgleicht. Diese Option ist nicht für die länder-/regionsspezifischen Exportformate für Frankreich, Deutschland oder die Niederlande verfügbar.</li>
<li><strong>Ustrt</strong> - Wählen Sie diese Option, um das unstrukturierte Format zu verwendet, wenn die Zahlung mehrere Rechnungen ausgleicht. Die Rechnungsnummern für die ausgeglichenen Rechnungen werden als die Rimesseinformationen verkettet und verwendet. Gemäß ISO 20022-Richtlinien dürfen unstrukturierte Rimesseinformationen maximal 140 Zeichen umfassen.</li>
</ul></td>
</tr>
<tr class="even">
<td>Anzahl der Rechnungen</td>
<td>Geben Sie die Anzahl von Rechnungen ein, über die das <strong>Zahlungsbegleitschreiben</strong> gedruckt wird.</td>
</tr>
<tr class="odd">
<td>Laufende Nummer</td>
<td>Geben Sie eine Sequenznummer ein, um die Datei zu identifizieren. Die Sequenznummer wird im <strong>Begleitzettel</strong>-Bericht angezeigt.</td>
</tr>
<tr class="even">
<td>Begleitzettel drucken</td>
<td>Aktivieren Sie dieses Kontrollkästchen, um den <strong>Begleitzettel</strong>-Bericht auszudrucken.</td>
</tr>
<tr class="odd">
<td>Kontrollbericht drucken</td>
<td>Aktivieren Sie dieses Kontrollkästchen, um die Berichts mit den Zahlungsinformationen auszudrucken.</td>
</tr>
<tr class="even">
<td>Begleitschreiben drucken</td>
<td>Aktivieren Sie dieses Kontrollkästchen, um einen <strong>Zahlungsavisbericht</strong> zu drucken.</td>
</tr>
</tbody>
</table>

## <a name="what-are-ibans-and-bics"></a>Was sind IBAN und BICs?
Die International Bank Account Number (IBAN) und Bank Identifier Code (BIC) werden verwendet, um den entsprechenden Konto in vielen Ländern/Regionen zu identifizieren. Diese enthalten die 34 SEPA-Land/Region. In **SWIFT-Code** geben Sie den BIC und im Feld **IBAN** die IBAN ein. Für das Bankkonto des Kreditors und das Bankkonto des Debitors befinden sich diese Felder auf dem **Zusätzliche Kennung**-Inforegister auf der **Bankkonto**-Registerkarte auf der Seite **Bankkonten**. Die Verwendung von als BIC für SEPA-Zahlungen wird nicht mehr erzwungen.

## <a name="how-do-i-transmit-a-payment-file-to-the-bank"></a>Wie übertrage ich eine Zahlungsdatei an die Bank?
Wenn Sie Zahlungen generieren, wird die Zahlungsdatei generiert, und Sie werden aufgefordert, diesen von Ihrem Webbrowser aus in einem verfügbaren Speicherort zu speichern. Im nächsten Schritt senden Sie die XML-Datei an die Bank. Dieser Prozess variiert von Bank zu Bank. Befolgen Sie die Anweisungen der Bank, um die Dateien an die Bank zur senden.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]