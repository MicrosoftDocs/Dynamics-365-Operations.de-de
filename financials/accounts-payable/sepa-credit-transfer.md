---
title: "Überblick zur SEPA-Kreditübertragung"
description: "Dieser Artikel wird allgemeine Informationen zu 20022-Banküberweisungen fest, ISO die einheitlicher Euro-Zahlungsverkehrsraum (SEPA)- Banküberweisungen und alle sonstigen elektronische Zahlungen für Kreditoren enthalten. Eine SEPA-Überweisungen ist ein bestimmter Typ Zahlung in Britischen von einem Unternehmen oder Person aus einem anderen Unternehmen oder Person zu. Das Thema werden auch, wie eine und sendet der Zahlungsdatei eingerichtet."
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, VendPaymMode
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 11124
ms.assetid: 36b0f870-16d4-4bbb-8da5-e747e69b970d
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 848df5e3898f37284d7746c59bff8b38d35ac883
ms.lasthandoff: 03/31/2017


---

# <a name="sepa-credit-transfer-overview"></a>Überblick zur SEPA-Kreditübertragung

Dieser Artikel wird allgemeine Informationen zu 20022-Banküberweisungen fest, ISO die einheitlicher Euro-Zahlungsverkehrsraum (SEPA)- Banküberweisungen und alle sonstigen elektronische Zahlungen für Kreditoren enthalten. Eine SEPA-Überweisungen ist ein bestimmter Typ Zahlung in Britischen von einem Unternehmen oder Person aus einem anderen Unternehmen oder Person zu. Das Thema werden auch, wie eine und sendet der Zahlungsdatei eingerichtet.

## <a name="what-is-a-credit-transfer-message"></a>Was ist eine Banküberweisungsnachricht?
Die Banküberweisungsnachricht ist eine Anforderung, die eine Partei initiierende (Ihr Unternehmen) den Verschiebungsmitteln von einem separaten Konto zu einem Kreditgeber sendet. Es gibt viele länder-/regionsspezifische und Bankbesondereimplementierungen von Banküberweisungsnachrichten. Viele hiervon werden innerhalb eines Landes/Regionen verwendet, und sind mehrere werdene Standards. Ein Standardwert ist korrekt eingerichteter globaler ISO 20022 und die Startnachrichten, z Banküberweisung. Die folgende Abbildung zeigt die Beziehungen und Disposition für die ausgewählte Banküberweisungsnachrichten angezeigt. 
Haben tansfer ![](./media/credit-transfer.jpg) Banküberweisungsnachrichten\[/caption\] 

## <a name="what-are-iso-20022-and-sepa-payments"></a>Welcher ISO 20022 - und SEPA-Zahlungen?
Single Euro Payments Area (SEPA) wurde von der Europäischen Kommission eingerichtet und schreibt vor, dass alle elektronischen Zahlungen als Inlandszahlungen gelten, unabhängig vom Land/von der Region in der sich die Person, das Unternehmen oder die Organisation und die Bank befindet. Es gibt keine Differenz zwischen nationalen Zahlungen grenzüberschreitenden und Zahlungen. Das enthält SEPA die 28 köpfigen Bundesländer der Europäischen Union (EU) sowie Island, Liechtenstein, Norwegen, die Schweiz, Monaco und San Marino. SEPA hilft dabei, einen gemeinsamen Markt für Zahlungsbuchungen innerhalb des europäischen Wirtschaftsraums (EEA) zu bilden. Letztlich wird von SEPA erwartet, die Anzahl von Zahlungsformaten zu reduzieren, mit denen Banken, Unternehmen und Personen arbeiten müssen. Die Europäische Kommission hat die Rechtsgrundlage für SEPA-Zahlungen über die Payment Services-Direktive (PSD) definiert. Der European Payments Council (EPC) unterstützt SEPA durch die folgenden Aktivitäten:

-   Er legt die Standards für elektronische SEPA-Zahlungen über das XML-Format ISO 20022 Universal-Nachrichtenschema für die Finanzindustrie fest.
-   Er richtet Regeln und Richtlinien zur die Behandlung von Eurozahlungen ein.

Der EPC besteht aus europäischen Banken und entwickelt das Handels- und das technische Framework für SEPA-Zahlungsmittel. Es werden drei Typen SEPA-Zahlungen verwendet:

-   Überweisungen
-   Bankeinzug
-   Karten

## <a name="what-is-a-sepa-credit-transfer"></a>Was ist eine SEPA-Überweisung?
Eine SEPA-Überweisung ist eine Zahlung von einem Unternehmen oder von Einzelperson zu einem anderen Unternehmen oder einer Einzelperson. Zahlungen müssen in Euro durchgeführt werden und sie müssen die internationale Bankkontonummer (IBAN) und Bank Identifier Code (BIC) für beide Parteien enthalten. (Der ist auch als BIC (Society for Code \[SWIFT\] Der SWIFT-Code auch.) Darüber hinaus müssen Buchungskosten zwischen beiden Parteien freigegeben werden. Banküberweisungen zwischen Parteien sollten XML-Dateien verwenden, die den ISO 20022-Standards zu Zahlungsverarbeitung entsprechen und das durch das EPC festgelegt XML-Format verwenden.

## <a name="how-is-a-credit-transfer-implemented"></a>Wie wird eine Banküberweisung implementiert?
Das für Kredittransferzahlungsformat europäische Länder so implementiert, indem elektronische meldende (ER) und die Zahlungsmethode funktionen in Dynamics 365 für Arbeitsgänge verwendet. Einige Banküberweisungsformate, die in anderen Regionen noch verwendet werden, verwenden Sie das vorhandene Zahlungsframework. Unter vielen anderen Formaten gibt es 20022-Banküberweisungsdateiformate zwölf ISO, die verfügbar sind. Diese Exportformate SEPA entsprechen dem Standard XML ISO 20022. Sie werden verwendet, um NichtEuro-Zahlungsüberweisungen für Land/Region zu generieren, in denen sie Eurozahlungen und verwendet werden, z in der Version 8,2 SEPA-Kredit-Übertragungssystem-Regelung angegeben, die Freigabe das EPC. Bevor Sie Banküberweisungen zu implementieren, müssen Sie mit Ihrer Bank in Verbindung setzen, um die US 1099-Software verschaffen, die erforderlich ist, um Bankings-Dateien Electronic hochzuladen. Sie verwenden diese Software, um XML-Dateien zu übertragen, die Auszahlungsanordnungen an Ihre Bank enthalten.

## <a name="what-credit-transfer-formats-are-currently-supported-in-dynamics-365-for-operations"></a>Welche Banküberweisungsformate werden derzeit in Dynamics 365 für Arbeitsgänge unterstützt?
Sie sollten für die Bibliothek der freigegebenen Anlage auf Microsoft Dynamics-Lebenszyklusdienstleistungen (LCS) immer wechseln und die neuesten Liste der verfügbaren Dateien sehen, haben Sie den Anlagentyp ** GER-Konfiguration **. Im nächsten Abschnitt ", was muss ich werden? ", wird ein Link zum Thema bereit, die erläutert, wie ein LCS-Repository herstellt, um verfügbare Konfigurationen und Importieren ausgewählter Konfigurationen zu prüfen.

## <a name="what-do-i-have-to-set-up"></a>Was muss ich einrichten?
-   Bevor Sie Banküberweisungsdateien erstellen können, muss mindestens eine aktive Banküberweisungskonfiguration in die ER-Konfigurationen importiert werden. Anweisungen finden Sie Berichterstellungskonfigurationen [elektronische des Downloads von den Lebenszyklus-Dienstleistungen]( https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).
-   Wenn Sie Kreditorzahlungsmethoden konfigurieren, wählen Sie das generische elektronische ** Berichterstellung ** Kontrollkästchen, und aktivieren Sie das entsprechende Banküberweisungsformat (beispielsweise aus, 20022-Banküberweisung ** ISO (** AT ") als Exportformatkonfiguration.
-   Sie muss die juristische Person und die Bankkontoinformationen Dynamics 365 für Arbeitsgänge einrichten.
-   Validieren, IBAN und manchmal SWIFT-Codes (BICs) oder andere Nummern werden benötigt, um spezifische Kredittransferzahlungen zu erstellen. Daher müssen diese für das Bankkonto des Kreditors einrichten und das Bankkonto der Organisation, die die Übertragung angefordert werden.
-   Zusätzliche Informationen kann, beispielsweise Mehrwertsteuer (VAT)- Nummern für die Parteien erforderlich, die in der Banküberweisungsnachricht gemeldet werden. Diese Anpassung muss für Kreditoren und für die juristische Person eingerichtet werden, wenn sie angefordert hat.
-   Einige Kreditorzahlungsmethoden größtenteils, ISO 20022 - basierend Zahlungsmethoden, erfordern ggf. zusätzliche Einstellungen für ZahlungsformatCodesätz ** **, z ** Dienstleistungstyp ** = ** = **. Diese Codes verwendet werden, z das zusätzliche Markierung für Zahlungsbuchungen während des Zahlungs verarbeitens. Standardwerte aus Zahlungscodes, wie Kategoriezweck ** **, Zuschlagsträger ** ** **, lokales Instrument ** und ** Servicelevel ** können in zwei Orte festgelegt werden. Der erste Platz ist Kreditorenzahlungserfassungskopf ** ** und als zweites ausgewählt wurde Kreditormethoden ** ** für Zahlungen. Nach Erstellung Zahlungserfassungspositionen, werden die Zahlungs codewerte, die auf Zahlungserfassungskopf festgelegt werden, in eine Erfassungsposition, wenn sie, nicht die Werte von den Zahlungsmethoden festgelegt werden, übertragen werden verwendet.

## <a name="what-parameters-are-available-for-generating-credit-transfer-payments"></a>Die Parameter sind für das Generieren von Kredittransferzahlungen verfügbar?
Die Liste bestimmter Parameter hängt vom Banküberweisungsformat ab. In der folgenden Tabelle werden die Parameter angezeigt, die verfügbar sind, wenn Sie eine 20022-Kredittransferzahlungsdatei ISO für Deutschland in eine Kreditorzahlungserfassung generieren. Mithilfe der Optionen verwenden, die im Formular verfügbar sind ** laufen Sie in den Hintergrund ** Registerkarte, können Sie Zahlungsgenerierung im Stapelverarbeitungsmodus ausgeführt werden.

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
<li><strong>Strd</strong> – Wählen Sie diese Option aus, um das Format strukturierte zu verwenden ist, ob eine Zahlungsposition mit einer Rechnung ausgeglichen wird. Diese Option ist nicht für das länder-/regionsspezifischen Exportformate, Deutschland oder Frankreich für die Niederlande verfügbar.</li>
<li><strong>Ustrt</strong> - Wählen Sie diese Option, um das unstrukturierte Format zu verwendet, wenn die Zahlung mehrere Rechnungen ausgleicht. Die Rechnungsnummern für die ausgeglichenen Rechnungen werden als die Rimesseinformationen verkettet und verwendet. Gemäß ISO 20022-Richtlinien werden unstrukturierte Rimesseinformationen maximal 140 Zeichen umfassen.</li>
</ul></td>
</tr>
<tr class="even">
<td>Anzahl der Rechnungen</td>
<td>Geben Sie die Anzahl der Rechnungen, aus denen der <strong>Zahlungsavis</strong> Bericht gedruckt wird.</td>
</tr>
<tr class="odd">
<td>Laufende Nummer</td>
<td>Geben Sie eine Sequenznummer ein, um die Datei zu identifizieren. Die laufende Nummer wird <strong>Begleitzettel</strong> im Bericht.</td>
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
Die International Bank Account Number (IBAN) und die Bankleitzahl (BIC) werden verwendet, um ein beliebiges Konto in vielen Ländern/Regionen weltweit zu identifizieren. Diese enthalten die 34 SEPA-Land/Region. Geben Sie den " im ** SWIFT-Code ** Feld und der IBAN im ** IBAN ** Feld ein. Für das Bankkonto des Kreditors sowie das Bankkonto des Debitors sind diese Felder auf dem Inforegister ** zusätzliche Kennung ** ** ** Bankkonto auf der Registerkarte der Bankkonten ** ** Seite. Die Verwendung von als BIC für SEPA-Zahlungen wird nicht mehr erzwungen.

## <a name="how-do-i-transmit-a-payment-file-to-the-bank"></a>Wie übertrage ich eine Zahlungsdatei an die Bank?
Gehen Zahlungen generieren, wird die Zahlungsdatei generiert, und Sie werden aufgefordert, diese in Ihrem Webbrowser für jeden verfügbaren Ort zu speichern. Im nächsten Schritt werden, die XML-Datei an Ihre Bank senden. Dieser Prozess variiert von Bank zu Bank. Befolgen Sie die Anweisungen der Bank, um die Dateien an die Bank zur senden.


