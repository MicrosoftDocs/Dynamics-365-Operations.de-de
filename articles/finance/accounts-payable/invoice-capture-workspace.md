---
title: Invoice Capture-Lösung Arbeitsbereich
description: Dieser Artikel enthält Informationen zum Arbeitsbereich zur Invoice Capture-Lösung.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4f3af7abf94542437be6132344d6bb7ffaf33d07
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691151"
---
# <a name="invoice-capture-solution-workspace"></a>Invoice Capture-Lösung Arbeitsbereich

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="side-by-side-viewer-for-the-invoice-capture-solution"></a>Side-by-Side-Viewer für die Invoice Capture-Lösung

Die Eingabe von Rechnungen in das System war in der Regel ein zeitaufwendiger und fehleranfälliger Prozess, da die Sachbearbeiter durch mehrere Anhangsdateien und Fenster navigieren müssen, um die richtigen Informationen zu sammeln. Der Side-by-Side-Dokumenten-Viewer trägt dazu bei, Ihre Erfahrung bei der Arbeit an Rechnungen zu verbessern, indem der Prozess einfacher, effizienter und genauer wird.

Mit dem Side-by-Side-Dokumenten-Viewer können Benutzer das Originaldokument und die Rechnung nebeneinander im selben Fenster öffnen. Die Rechnungsseite wird mit Informationen gefüllt, die aus dem ursprünglichen Rechnungsdokument stammen. Der Viewer stellt die Verbindung zwischen den Rechnungsseitenfeldern und dem Originalrechnungsdokument her. Der Viewer hilft Benutzern auch dabei, alle Fehler zu finden, die auf der Rechnungsseite vorhanden sind.

### <a name="open-the-side-by-side-viewer"></a>Seite-bei-Seite-Viewer öffnen

In Microsoft Dynamics 365 Finance können Sie den Side-by-Side-Viewer über die Liste auf der Zusammenfassungsseite oder über die Rechnungslistenseite öffnen. Sie können es auch öffnen, indem Sie auf einen Datensatz doppeltippen (oder doppelklicken) oder indem Sie die Rechnungsnummer auswählen.

### <a name="using-the-side-by-side-viewer"></a>Seite-bei-Seite-Viewer verwenden

#### <a name="manually-review-an-invoice"></a>Eine Rechnung manuell überprüfen

Ein importiertes Rechnungsdokument muss möglicherweise aufgrund von Fehlern oder Warnungen manuell überprüft werden. Im Side-by-Side-Viewer zeigt die Kopfzeile des Dokuments den Status **Importiert** an, und die aktuelle Version wird **Originalversion** sein.

Wählen Sie **Überprüfung starten** aus, um mit der Überprüfung der Rechnung zu beginnen. Alle Felder werden editierbar. Das Feld **Status** wird aktualisiert auf **Wird überprüft**, und das Feld **Aktuelle Version** wird aktualisiert auf **Modifizierte Version**.

#### <a name="view-and-work-with-messages"></a>Anzeigen und Arbeiten mit Nachrichten

Benutzer sollten den Überprüfungsprozess vom Nachrichtenbereich aus starten. Fehlermeldungen sind durch ein rotes X, Warnmeldungen durch ein Dreieck und Informationsmeldungen durch einen Kreis gekennzeichnet. Meldungen im Zusammenhang mit der Vertrauensbewertung können je nach Schwellenwert, der von der Konfigurationsgruppe festgelegt wird, entweder als Warnungen oder als Fehler klassifiziert werden. Weitere Informationen finden Sie unter [Konfigurationsgruppen der Invoice Capture-Lösung](invoice-capture-config-group.md).

Warn- und Fehlermeldungen können im Meldungsbereich, im Rechnungskopf oder in den Rechnungszeilen ignoriert werden. Nachdem eine Nachricht ignoriert wurde, wird sie nicht mehr als Fehler oder Warnung angezeigt und die Rechnung wird die Überprüfung nicht bestehen.

- Um Nachrichten aus dem Nachrichtenbereich zu ignorieren, wählen Sie **Ignorieren** aus. Um eine ignorierte Nachricht zurückzusetzen, wählen Sie wieder **Ignorieren** aus. Sein Typ wird dann von Fehler oder Warnung auf Information geändert.
- Um Meldungen aus dem Rechnungskopf oder der Rechnungszeile zu ignorieren, wählen Sie **Ignorieren** auf dem Feld. Das Nachrichtensymbol verschwindet. Es wird jedoch erneut angezeigt, wenn die Nachricht aus dem Nachrichtenbereich zurückgesetzt wird.

Bei Nachrichten, die sich auf Rechnungskopffelder beziehen, wird der Cursor bei Auswahl der Nachricht im Nachrichtenbereich in das entsprechende Feld im Kopfbereich bewegt.

#### <a name="proofread-and-edit-fields"></a>Felder korrigieren und bearbeiten

Wird der Wert eines Feldes per optischer Zeichenerkennung (OCR) aus der Originalrechnung ausgelesen, erscheint auf dem Feld ein Symbol. Wenn Sie das Symbol auswählen, zoomt der Dokumentenbetrachter hinein und hebt die Stelle hervor, an der der Feldwert gelesen wird, um Ihnen bei der Überprüfung von Rechnungsdaten zu helfen.

Führen Sie einen der folgenden Schritte aus, um den Dokumentbetrachter auf seine ursprüngliche Vergrößerung zurückzusetzen:

- Wählen Sie dasselbe Symbol aus, das Sie zuvor ausgewählt haben.
- Wählen Sie in der rechten oberen Ecke des Dokumenten-Viewers die Schaltfläche aus.

Bearbeiten Sie das Feld wie gewünscht. Änderungen werden automatisch gespeichert, wenn der Cursor ein Feld verlässt. Ein Symbol rechts neben einem Feld zeigt an, dass das Feld manuell aktualisiert wurde. Wenn die Seite aktualisiert wird, wird das Symbol entfernt.

#### <a name="check-an-invoice-to-get-up-to-date-messages"></a>Überprüfen Sie eine Rechnung, um aktuelle Nachrichten zu erhalten

Wenn Sie ein Feld bearbeiten, wird der Feldwert aktualisiert, aber es werden keine neuen Validierungsmeldungen generiert. Um aktuelle Prüfungen zu erhalten, wählen Sie **Prüfen**. Die Meldungen im Meldungsbereich, im Rechnungskopf und in den Rechnungspositionen werden aktualisiert.

#### <a name="complete-the-review"></a>Überprüfung abschließen

Um die Überprüfung abzuschließen, wählen Sie **Vollständige Überprüfung** aus. Die Rechnungen werden validiert. Wenn Fehler gefunden werden, bleibt der Dokumentstatus **Wird überprüft** bestehen, und eine Meldungsleiste wird angezeigt. Alle Nachrichten im Nachrichtenbereich und im Rechnungskopf und in den Zeilen werden automatisch aktualisiert, um Informationen über die Ursachen der fehlgeschlagenen Validierung bereitzustellen.

Nachdem alle Blockierungsfehler behoben wurden, kann die Überprüfung abgeschlossen werden. Der Dokumentstatus wird aktualisiert auf **Überprüft**, und die Felder können nicht mehr bearbeitet werden. Sie können die Überprüfung neu starten, indem Sie **Überprüfung starten** wieder auswählen.

#### <a name="generate-a-pending-vendor-invoice-in-finance"></a>Ausstehende Kreditorenrechnung in Finance generieren

Um das Rechnungsdokument an die angeschlossene Finanzumgebung zu senden, wählen Sie **Generieren**. Schlägt die Rechnungserstellung fehl, erscheint eine Fehlermeldung in einer Meldungsleiste.

#### <a name="void-an-invoice"></a>Rechnung stornieren

Um eine Rechnung zu stornieren, wählen Sie **Stornieren** aus. Stornierte Rechnungen können nicht überprüft werden und werden nicht in der Liste **Rechnungen müssen manuell überprüft werden** angezeigt.

### <a name="validation-logic"></a>Prüfungslogik

Einige Schlüsselfelder im Side-by-Side-Viewer sind in den Rechnungsbereitstellungsdaten nicht vorhanden, aber erforderlich, um ausstehende Rechnungen in Finance zu generieren. Diese Felder werden aus einer Kombination der aktuellen Rechnungsbereitstellungsdaten und Stammdaten aus der Finance abgeleitet.

Die Felder, die abgeleitet werden müssen, sind **Juristische Person**, **Anbieterkonto**, und **Artikelnummer**. Sie müssen in der folgenden Reihenfolge abgeleitet werden. Wenn die Ableitung eines Felds fehlschlägt, stoppt der Prozess.

1. **Juristische Person** – Die juristische Person wird zuerst abgeleitet. Wenn für die juristische Person eine aktive Zuordnungsregel gefunden wird, wird die juristische Person anhand des Firmennamens und der Firmenadresse abgeleitet.
2. **Lieferantenkonto** – Als Nächstes wird das Kreditorenkonto basierend auf einer aktiven Zuordnungsregel und einer Kombination aus der abgeleiteten juristischen Person und dem Namen und der Kreditorenadresse des Kreditors abgeleitet.
3. **Artikelnummer** – Schließlich wird der Artikelname aus der Bereitstellung abgeleitet, basierend auf den folgenden drei Arten von Informationen:

    - Eine konfigurierte Zuordnungsregel
    - Die abgeleitete Juristische Person
    - Die abgeleitete Kreditorenkontonummer

Um eine Validierung durchzuführen, wählen Sie **Prüfen** im Side-by-Side-Viewer aus. Derzeit führt die Validierung die folgenden Prüfungen durch:

- **Obligatorische Prüfung** – Diese Prüfung validiert die Pflichtfelder für den Side-by-Side-Viewer. Benutzer können auswählen, welche Felder auf der Seite **Konfigurationseinstellung** Pflichtfelder sein müssen.
- **Konfidenzbewertung** – Benutzer können den Warnschwellenwert und den Fehlerschwellenwert für die Vertrauensbewertung festlegen. Diese Prüfung konzentriert sich auf den Konfidenzwert von OCR, der unter diesen Schwellenwerten liegt. Fehler- oder Warnmeldungen werden basierend auf dem Validierungsergebnis angezeigt.
- **Juristische Person** – Diese Prüfung bestätigt, dass sich eine juristische Person in Finance befindet. Wenn die juristische Person in der Finance-Umgebung nicht vorhanden ist, schlägt die Validierung fehl.

Wenn der Side-by-Side-Viewer zum ersten Mal verwendet wird und der Benutzer **Prüfen** auswählt, werden die Ableitungs- und Validierungsprozesse ausgeführt. Wenn die Rechnungen korrekt sind, wird der Validierungsprozess ausgeführt, wenn der Benutzer **Vollständige Überprüfung** auswählt. Es wird auch ausgeführt, wenn der Benutzer **Lieferantenrechnung erstellen** auswählt.

Der Ableitungsprozess findet vor dem Validierungsprozess statt, und alle Warnungen oder Fehler stammen aus dem Validierungsprozess. Die Warnungen und Fehler werden in Finance protokolliert.
