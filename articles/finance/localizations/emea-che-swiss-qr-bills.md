---
title: Schweizer QR-Rechnungen
description: Dieses Thema enthält Informationen zum Generieren von QR-Rechnungen (QR-Slips) und zum Verarbeiten eingehender QR-Rechnungen.
author: neserovleo
manager: AnnBe
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Switzerland
ms.author: v-lenest
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 1c58aa35dacb719eeef3a9b8d5f4904beefc73a0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4407758"
---
# <a name="swiss-qr-bills"></a>Schweizer QR-Rechnungen

[!include [banner](../includes/banner.md)]


Ab Juli 2020 müssen zusätzlich zu den Rechnungen QR-Rechnungen (QR-Belege) bearbeitet und ausgestellt werden. In diesem Thema wird erläutert, wie Sie QR-Rechnungen generieren und eingehende QR-Rechnungen in Microsoft Dynamics 365 Finance verarbeiten.

Um die QR-Rechnungsfunktion verfügbar zu machen, müssen Sie die folgenden Funktionen im Modul **Funktionsverwaltung** aktivieren:

- Konfigurierbare Zahlungskennung
- QR-Rechnungen (Schweiz)

> [!NOTE]
> Wenn Sie die Schweizer QR-Rechnungsfunktion aktivieren, steht sie auch anderen Ländern zur Verfügung. Zu diesen Ländern gehören je nach Anschrift der juristischen Person die Schweiz (CH), Deutschland (DE), Österreich (AT), Frankreich (FR) und Italien (IT).

## <a name="electronic-reporting-configurations"></a>Elektronische Berichtskonfigurationen

Die neuesten Versionen der folgenden EB-Konfigurationen (Electronic Reporting) sollten aus Microsoft Dynamics Lifecycle Services (LCS) importiert werden:

- Schweizer QR-Rechnungstext
- Strukturierte Informationen für Schweizer QR-Rechnung
- Kreditübertragung ISO20022 (CH)
- ISO20022 pain.002
- ISO20022 Camt.054

Die erforderlichen EB-Datenmodell- und EB-Modellzuordnungskonfigurationen werden automatisch importiert.

## <a name="setup-of-company-bank-accounts"></a>Einrichtung von Firmenbankkonten

Auf der **Bankkonto** Seite (**Bargeld- und Bankmanagement** \> **Bankkonten** \> **Bankkonten**), in dem **QR-IBAN**, geben Sie im Feld die QR-IBAN an. Diese Nummer kann gleichzeitig mit der normalen internationalen Bankkontonummer (IBAN) verwendet werden und hat ähnliche Validierungen im System.

### <a name="cash-discount-and-tax-code-descriptions"></a>Beschreibungen von Skonto und Steuerkennzeichen

Das Feld für die Beschreibung der QR-Rechnung sollte für alle Skonti und Steuerkennzeichen ausgefüllt werden. Diese Beschreibung wird verwendet, wenn QR-Rechnungen gedruckt werden.

## <a name="setup-of-the-legal-entity-registration-ids"></a>Einrichtung der Registrierungs-IDs für juristische Personen

Damit die eindeutige Kennung (UID) korrekt in die generierte QR-Rechnung eingetragen wird, sollte der UID-Wert in das Feld **Registrierungs-ID** im Setup der juristischen Person eingegeben werden. Zusätzlich sollte der Wert im Feld **Registrierungskategorie** dem Wert **Umsatzsteuer-ID** entsprechen.

## <a name="accounts-receivable-setup"></a>Einrichten der Debitoren

### <a name="payment-id"></a>Zahlungskennung

Auf der Seite **Zahlungs-ID** können Sie die Zahlungs-ID-Struktur konfigurieren, die angewendet wird, wenn ausgehende QR-Rechnungen aus dem Modul **Debitoren** erstellt werden. Die Länge der Zahlungs-ID sollte auf 27 Stellen eingestellt sein, und die Prüfziffer sollte mithilfe des Algorithmus **Modulo11** generiert werden. Nichtstellige Symbole werden bei Ausführung des Algorithmus von den Zahlungs-IDs ausgeschlossen. Daher sollten die Nummernfolgen, die für Kundenkonten und Rechnungen verwendet werden, nur Ziffern haben.

Standardmäßig kann der Zahlungs-ID-Typ, der auf die Rechnung angewendet wird, die folgende Hierarchieebene verwenden:

- **Debitorenparameter** Seite \> **Hauptbuch und Umsatzsteuer** Registerkarte
- Seite **Debitorengruppen**
- Seite **Kundenkonto** \> **Zahlungsausfälle** Registerkarte
- Seite **Zahlungsart** \> Registerkarte **Zahlungskontrolle**

### <a name="methods-of-payment--customers"></a>Zahlungsmethode - Debitoren

Die Zahlungsmethode sollte auf den Kundenkonten eingerichtet werden, die QR-Rechnungen verwenden, um die Details des Firmenbankkontos zu definieren, auf das eine QR-Rechnung ausgestellt wird. Um eingehende Zahlungen im Format camt.054 zu verarbeiten, sollten Sie die ER-Importkonfiguration einrichten.

### <a name="customer-account"></a>Debitorenkonto

Die Standardzahlungsmethode muss ausgewählt und der Zahlungs-ID-Typ muss ausgefüllt werden, wenn er nicht bereits in der Standardeinstellung für Kundengruppen auf der Seite **Debitorenparameter** angegeben ist.

In der Feldgruppe **Zugehöriger Zahlungsanhang** wird der neue Typ, **QR-Rechnung** hinzugefügt. Wenn diese Option ausgewählt ist, wird die QR-Rechnung gedruckt, wenn das Dokument des entsprechenden Typs gedruckt wird.

### <a name="giro-report-processing-group"></a>Berichtsverarbeitungsgruppe für Girokonto

Die Einstellungsinformationen, die in den Giro-Berichtsverarbeitungsgruppen bereitgestellt werden, bestimmen, wie die Abschnitte **Abrechnungsdaten** auf einer QR-Rechnung ausgefüllt wird. Bei Bedarf können Sie verschiedene Teile dieses Abschnitts auf der QR-Rechnung in ER konfigurieren und verwenden. Im Folgenden finden Sie einige Beispiele hierfür:

- **Konto Code** – Das spezifische Format, das dem spezifischen Kundenkonto zugeordnet ist.
- **Debitorenrelation** – Der Wert des jeweiligen Kundenkontos oder Kundengruppe.
- **QR-Bill-Informationen** – Die EB-Formatkonfiguration, die für das Ausfüllen der Rechnungsinformationen verantwortlich ist.
- **Scherensymbol drucken** – Die Aufnahme des Scherensymbols in den gedruckten Bericht. Die Aufnahme dieses Symbols kann wichtig sein, wenn Sie auswählen, ob Sie eine gedruckte Version der QR-Rechnung oder eine elektronische Version senden möchten.

## <a name="accounts-payable-setup"></a>Kreditoren einrichten

### <a name="methods-of-payment--vendors"></a>Zahlungsmethoden – Lieferanten

Für Zahlungsmethoden des Anbieters müssen Sie das zugehörige Bankkonto angeben, die erforderlichen EB-Konfigurationen für den Export und Import für die Verarbeitung von Zahlungsdateien auswählen und die Zahlungsspezifikation einrichten. Ein neuer Parameterwert für die Zahlungsspezifikation, **Tp3.QR** ist für Zahlungen verfügbar, die den eingehenden QR-Rechnungen entsprechen. Zusätzlich kann eine Option, die auf dem Bankkonto des Anbieters verfügbar ist, verwendet werden, um die Parameter **Spezifikation** neu zu definieren.

Die Zahlungs-ID sollte auf der Registerkarte **Zahlungsattribute** aktiviert werden, damit die Zahlungs-ID während des Zahlungsvorschlags für Zahlungen im Zusammenhang mit QR-Rechnungen vererbt werden kann.

### <a name="return-format-error-codes-and-return-format-status-mapping"></a>Rückgabeformat-Fehlercodes und Rückgabeformat-Statuszuordnung

Wenn pain.002 als Rückgabedateiformat verwendet wird, müssen die Fehlercodes für das Rückgabeformat und die Statuszuordnung für das Rückgabeformat eingerichtet werden. Weitere Informationen finden Sie unter [Importieren von ISO20022 Dateien](emea-iso20022-file-formats.md).

### <a name="vendor-account"></a>Kreditorenkonto

Die Standardeinstellung des Anbieterkontos für ISO20022-Zahlungen wird erwartet. Weitere Informationen finden Sie unter [Lieferanten und Lieferantenbankkonten für ISO20022-Überweisungen einrichten](tasks/set-up-vendor-iso20022-credit-transfers.md).

### <a name="vendor-bank-account"></a>Kreditoren-Bankkonto

Eine QR-IBAN muss den Bankkonten des Anbieters zugewiesen werden. Es wird erwartet, dass andere Felder gemäß dem typischen Zahlungsverfahren für Zahlungsart 3 in der Schweiz festgelegt werden.

Darüber hinaus besteht die Möglichkeit, einen Zahlungsspezifikationsparameter direkt auf dem Bankkonto des Anbieters auszuwählen. Wenn eine Zahlungsspezifikation vorgenommen wurde, erhält der Wert eine höhere Priorität als die Zahlungsspezifikationsmethode, wenn eine Überweisungsdatei generiert wird.

## <a name="accounts-receivable-process"></a>Debitorenprozess

### <a name="generate-the-qr-bills"></a>Generieren Sie die QR-Rechnungen

Drucken Sie das Dokument aus, um die QR-Rechnung für ein Dokument, z. B. eine Debitorenrechnung zu erstellen. Die QR-Rechnung wird automatisch als zusätzlicher Bericht generiert. Sie können die QR-Rechnung dann als PDF-Datei exportieren und dann ausdrucken oder elektronisch senden.

Nachfolgend finden Sie einige Dokumente, die diese Funktionen unterstützen:

- Auftragrechnungen
- Freitextrechnungen
- Projektrechnungen
- Zinsrechnungen
- Mahnschreiben
- Kontoauszug

### <a name="import-payments-in-camt054-format"></a>Importieren Sie Zahlungen im Format camt.054

Um einen Kontoauszug im Format camt.054 von der Bank zu importieren, öffnen Sie die Zeile für das Kundenzahlungsjournal und führen Sie die Funktion **Zahlung importieren** aus. Die 27-stellige Referenz wird in der Datei **Ref** im Abschnitt **RmtInf** der Datei erwartet. Nach dem Import werden die Zahlungsvorgänge erstellt und mit Kundentransaktionen basierend auf der Zahlungs-ID abgerechnet. Weitere Informationen finden Sie unter [Importieren von ISO20022 Dateien](emea-iso20022-file-formats.md).

## <a name="accounts-payable-process"></a>Kreditorenkontenprozess

Der Umfang der unterstützten Funktionen umfasst den Prozess des manuellen Importierens der QR-Code-Werte in das Eingabedialogfeld. Dieser Import kann mithilfe von Scangeräten erfolgen, die den Textwert des QR-Codes übertragen. Die Struktur der Informationen im QR-Code sollte den Standards entsprechen, die zum Zeitpunkt der Funktionsfreigabe auf der Website der SIX-Gruppe verfügbar sind. Jede Ableitung von der Struktur der im QR-Code verschlüsselten Informationen oder alle Formatänderungen, die erforderlich sind, um dem gerätespezifischen Verhalten zu folgen, können mithilfe vom Modul **Elektronische Berichterstattung** (EB) konfiguriert werden. Es sind keine Codeänderungen erforderlich.

### <a name="import-qr-bills"></a>Importieren von QR-Rechnungen

Sie können die QR-Rechnungen in das Rechnungsjournal oder in ausstehende Kreditorenrechnungsziele importieren.

Um QR-Rechnungen in das Rechnungsjournal zu importieren führen Sie die Funktion **QR-Rechnung importieren** aus, die auf der Seite **Rechnungsjournalzeilen** verfügbar ist.

In dem Dialogfeld **Importieren** zeigt das Feld **QR-Rechnung** den Namen der EB-Formatkonfiguration an, die verwendet werden soll. Sie können ein anderes EB-Format angeben. Im leeren Textfeld der **QR-Rechnung** geben Sie im Feld den QR-Code ein. Wählen Sie dann **OK** aus.

Auf der nächsten Seite zeigt die Registerkarte **QR-Rechnung** den analysierten Werte der QR-Rechnung. Auf der Registerkarte **Allgemeines** können Sie die Werte des erkannten Lieferanten, des Bankkontos, des Betrags und anderer Details anzeigen, die in das System importiert werden. Nachdem Sie **OK** ausgewählt haben, werden die Rechnungsjournalzeilen erstellt. Wenn diese QR-Rechnung zuvor importiert wurde, werden Sie durch eine Warnmeldung benachrichtigt. Die Informationen der importierten QR-Rechnung werden gespeichert und können auf der Seite **Importierte QR-Rechnungen** zur Überprüfung angezeigt werden.

Für Rechnungen, die Bestellungen zugeordnet sind, können Sie ausstehende Lieferantenrechnungsköpfe erstellen, die auf QR-Rechnungsinformationen basieren. Um die QR-Rechnung zu importieren, klicken Sie auf die Seite **Ausstehende Lieferantenrechnungen** auf der Registerkarte **Prozess** und wählen Sie **QR-Rechnung importieren**. Das Verfahren zum Hinzufügen, Überprüfen und Importieren des QR-Codes ähnelt dem im vorherigen Absatz beschriebenen Verfahren.

Sie können die QR-Rechnung auch importieren, wenn die Lieferantenrechnung aus der Seite **Bestellung** geöffnet wird. Das Importverfahren entspricht dem Verfahren für ausstehende Lieferantenrechnungen. Wenn die Rechnung einer Bestellung zugeordnet ist, erfolgt der Import automatisch.

Um die QR-Rechnung zu verarbeiten, wenn kein vordefiniertes Ziel vorhanden ist, oder um ein benutzerdefiniertes Ziel zu verwenden, können Sie eine spezielle Option verwenden, die unter **Periodische Aufgaben** im Modul **Abrechnungsverbindlichkeiten** definiert ist. In diesem Fall müssen Sie das Ziel manuell anpassen.

Wenn der Klartext der QR-Rechnung leer bleibt, können Sie den Import aus der Textdatei ausführen, die sich im Ordner SharePoint befindet, basierend auf dem Setup der ER-Quelle.

Nachdem die Rechnung gebucht wurde, steht die Lieferantentransaktion mit der importierten Zahlungs-ID zur Abrechnung im Zahlungsjournal zur Verfügung.

## <a name="payment-file-processing"></a>Zahlungsdateiverarbeitung

Erstellen Sie Lieferantenzahlungsjournalzeilen mithilfe der Zahlungsvorschlagsfunktion. Weitere Informationen finden Sie unter [Lieferantenzahlungen mithilfe eines ISO20022-Zahlungsformats erstellen und exportieren](tasks/create-export-vendor-payments-iso20022-payment-format.md).

Für Zahlungen, die sich auf QR-Rechnungen beziehen, wird die Überweisungsdatei basierend auf dem Zahlungs-ID-Wert generiert. Dieser Wert wird aus dem QR-Code abgerufen.

Sie können die Dateien pain.002 und camt.054 aus der Seite **Zahlungsüberweisungen** importieren. Weitere Informationen finden Sie unter [Importieren von ISO20022 Dateien](emea-iso20022-file-formats.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]