---
title: Online- und Offlineverkaufsstellen-(POS)-Vorgänge
description: Dieses Thema enthält Informationen zu den Verkaufsstelle (POS)-Arbeitsgängen in Dynamics 365 Commerce. Es gibt an, an welcher Position in der Anwendung die Arbeitsgänge aufgerufen werden können, und ob sie im Offline-Modus verfügbar sind.
author: jblucher
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-09-27
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 5e139b7b12b8f2e549fb9c2c8e39125e190c7396
ms.sourcegitcommit: 4d52c67f52ad0add63cd905df61367b344389069
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/16/2022
ms.locfileid: "8311978"
---
# <a name="online-and-offline-point-of-sale-pos-operations"></a>Online- und Offlineverkaufsstellen-(POS)-Vorgänge

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Die meisten Aktivitäten, die Benutzer in Verkaufsstelle (POS) vornehmen, gelten als Arbeitsgänge. Arbeitsgänge werden im Dynamics 365 Commerce-Backoffice konfiguriert und verwaltet. Viele Arbeitsgänge können den Schaltflächen im POS-Schaltflächenraster hinzugefügt werden. Benutzer können die Schaltflächen dann auswählen, um Vorgänge aufzurufen und die Funktion auszuführen. Andere Arbeitsgänge sind Teil der Haupt-POS-Anwendung und Schaltflächen werden entweder von Bildschirm-Schaltflächen oder als Bestandteil anderer Workflows oder Prozessen aufgerufen.

Die folgende Tabelle enthält Informationen zu den Arbeitsgängen, die in Modern POS und Cloud POS verfügbar sind. Die Tabelle gibt auch an, an welcher Position in der Anwendung die Arbeitsgänge aufgerufen werden können und ob POS im Offline-Modus verfügbar sind.

Einige Arbeitsgänge sind derzeit nicht in Modern POS oder Cloud POS für verfügbar. Einige dieser Arbeitsgänge sind gebietsschemaspezifische Arbeitsgänge, die weitere Konfiguration und Erweiterungen erfordern. Auch einige Funktionen von Microsoft Dynamics AX 2012 werden derzeit nicht unterstützt.

Die folgenden Spalten geben an, woher die Arbeitsgänge aufgerufen werden können:

- **Schaltflächenraster** – Der Arbeitsgang kann zu den Schaltflächen in POS-Schaltflächenrastern zugewiesen werden, die Teil eines POS-Bildschirmlayouts sind.
- **Buchungsbildschirm** – Der Arbeitsgang kann aus POS-Schaltflächenrastern aufgerufen werden, die im Feld POS-Buchungs-Bildschirm konfiguriert werden.
- **Willkommen-Bildschirm** – Der Arbeitsgang kann aus POS-Schaltflächenrastern aufgerufen werden, die im Feld POS-Buchungs-Bildschirm konfiguriert werden.

> [!NOTE]
> Die Arbeitsgänge unten gelten für die neueste Version von Commerce. Einige Vorgänge haben sich möglicherweise geändert oder sind möglicherweise in früheren Versionen nicht verfügbar.


| ID | Arbeitsgang | Beschreibung | Schaltflächenraster | Transaktionsbildschirm | Willkommensbildschirm | Verfügbar offline | Gebietsschemaspezifisch |
|----|-----------|-------------|-------------|--------------------|----------------|-------------------|-----------------|
| 707 | Gerät aktivieren | Aktiviert das aktuelle Gerät, indem Sie einen authentifizierten Benutzer ermöglichen, Verbindungsinformationen verfügbar zu machen und eine Gerät und Register Kennung zuzuweisen | Nein | Nein | Nein | Nein | Nein |
| 134 | Zugehörigkeit hinzufügen | Hinzufügen einer vorausgewählten Zugehörigkeit zu einer Transaktion. Wählen Sie die Zugehörigkeit auf der Seite **-Schaltflächeneigenschaften**. | Ja | Ja | Nein | Ja | Nein |
| 135 | Zugehörigkeit aus Liste hinzufügen | Hinzufügen einer Zugehörigkeit durch Auswahl aus einer Liste. | Ja | Ja | Ja | Ja | Nein |
| 137 | Hinzufügen einer Zugehörigkeit zu einem Debitor | Hinzufügen einer Zugehörigkeit einem Debitor auf der Seite **Debitorendetails**. | Nein | Nein | Nein | Ja | Nein |
| 138 | Zugehörigkeit von Debitor entfernen | Zugehörigkeit eines Debitor auf der Seite **Debitorendetails** entfernen. | Nein | Nein | Nein | Ja | Nein |
| 643 | Couponcode hinzufügen | Einen Coupon hinzufügen durch Eingabe seines Codes in POS. | Ja | Ja | Nein | Ja | Nein |
| 141 | Kopfzuschläge hinzufügen | Fügen Sie dem Auftragskopf eine Gebühr für eine Fehlbestellung hinzu. | Ja | Ja | Nein | Nein| Nein |
| 141 | Belastungen pro Position hinzufügen | Fügen Sie einer ausgewählten Verkaufszeile Gebühr für eine Fehlbestellung hinzu. | Ja | Ja | Nein | Nein| Nein |
| 117 | Treuekarte hinzufügen | Fordern Sie den Benutzer auf, eine Treuekartennummer einzugeben, die der aktuellen Buchung hinzugefügt wird. | Ja | Ja | Nein | Ja | Nein |
| 136 | Seriennummer hinzufügen | Dieser Arbeitsgang erlaubt dem Benutzer, eine Seriennummer für das derzeit ausgewählte Produkt anzugeben. | Ja | Ja | Nein | Ja | Nein |
| 1214 | Versandadresse hinzufügen | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nein |
| 519 | Zu Geschenkkarte hinzufügen | Fügt der angegebenen Geschenkkarte einen Geldbetrag hinzu. | Ja | Ja | Nein | Nein | Nein |
| 6000 | Überspringen der Steuerregistrierung zulassen | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Ja |
| 1212 | Bankeinzahlung | Erfasst den bei der Bank eingezahlten Geldbetrag und andere Informationen, z. B. die Nummer der Banktasche. | Ja | Ja | Ja | Ja | Nein |
| 923 | Überprüfung der Banksummen | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Ja |
| 915 | Leerer Vorgang | Dieser Vorgang stellt eine anpassbare Schaltfläche dar, die vom Softwareentwickler programmgesteuert geändert werden kann, falls das Unternehmen einen speziellen Vorgang benötigt. | Ja | Ja | Ja | Ja | Nein |
| 1053 | Schicht blind schließen | Festlegen der aktuellen Schicht, um Einträge blind vorzunehmen, und unterzeichnet Sie den Benutzer aus. Eine blind-geschlossene Schicht wird abgeschlossen, als Lieferant zu weiteren Buchungen jedoch zu den Kassenladearbeitsgängen, wie Zahlungsmittel entfernen und Kassensturz weiterhin geöffnet. | Ja | Ja | Ja | Nein | Nein |
| 310 | Summe berechnen | Wenn Rabattberechnung verzögert wird, initiiert dieser Arbeitsgang die Berechnung für die aktuelle Buchung. | Ja | Ja | Nein | Ja | Nein |
| 642 | Alle Produkte ausführen | Legen Sie die Lieferart für alle Positionen auf **Takeaway** fest. | Ja | Ja | Nein | Ja\* | Nein |
| 641 | Ausgewählte Produkte ausführen | Legen Sie die Lieferart für die ausgewählten Positionen auf **Takeaway** fest. | Ja | Ja | Nein | Ja\* | Nein |
| 647 | Lieferart ändern | Ändern Sie die Lieferart für vorkonfigurierte Versandverkaufszeilen. | Ja | Ja | Nein | Nein| Nein |
| 1215 | Kennwort ändern | Dieser Arbeitsgang ermöglicht POS-Benutzern, ihr Kennwort zu ändern. | Ja | Ja | Ja | Nein | Nein |
| 123 | Maßeinheit ändern | Ändern der Maßeinheit für den ausgewählten Positionsartikel. | Ja | Ja | Nein | Ja | Nein |
| 639 | Standardverkäufer für Buchung löschen | Entfernt die Provisionsverkaufsgruppe (Verkäufer) aus der Buchung. | Ja | Ja | Nein | Ja | Nein |
| 106 | Menge löschen | Setzt die Menge auf der momentan ausgewählten Position auf **1** zurück. | Ja | Ja | Nein | Ja | Nein |
| 640 | Verkäufer für Position löschen | Entfernt die Provisionsverkaufsgruppe (Verkaufsrepräsentanten) von der derzeit ausgewählten Position. | Ja | Ja | Nein | Ja | Nein |
| 121 | Verkäufer löschen | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nein |
| 1055 | Schicht schließen | Schließt die aktuelle Schicht, Drucken eines Z-Berichts und meldet den Benutzer aus dem System ab. | Ja | Ja | Ja | Nein | Nein |
| 139 | Transaktion einbeziehen | Fordert Benutzer dazu auf, eine Zahlungsmethode auswählen | Ja | Ja | Nein | Ja | Nein |
| 925 | Bankscheck kopieren | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Ja |
| 620 | Debitorenauftrag erstellen | POS-Buchung in einen Debitor-Auftrag umwandeln | Ja | Ja | Nein | Ja\* | Nein |
| 621 | Angebot erstellen | POS-Buchung in ein Vertriebsangebot umwandeln | Ja | Ja | Nein | Ja\* | Nein |
| 636 | Einzelhandelstransaktion erstellen | Erstellt eine Standardverkaufsbuchung, wenn das Standardverhalten des POS ist, Kundenaufträge zu erstellen. | Ja | Ja | Nein | Ja | Nein |
| 600 | Kunde | Fügen Sie den angegeben Debitor der Buchung hinzu. | Nein | Nein | Nein | Ja | Nein |
| 1100 | Einzahlung auf Debitorenkonto | Nimmt eine Einzahlung auf dem Konto eines Debitors vor. | Ja | Ja | Ja | Ja | Ja |
| 612 | Debitor hinzufügen | Dient zum Erstellen eines neuen Debitorendatensatzes. | Ja | Ja | Ja | Ja† | Nein |
| 603 | Debitor löschen | Den Debitor aus der aktuellen Buchung entfernten. | Ja | Ja | Nein | Ja | Nein |
| 602 | Debitorensuche | Sucht nach einem Debitorendatensatz, indem er zur Debitorensuchseite am Point-of-Sale wechselt. | Ja | Ja | Ja | Ja | Nein |
| 609 | Debitorenbuchungen | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nein |
| 917 | Datenbankverbindungsstatus | Zeigt aktuelle Verbindungseinstellungen an und wechselt zwischen online oder offline Modi. | Ja | Ja | Ja | Ja | Nein |
| 1200 | Ausgangsbetrag deklarieren | Deklariert den Betrag, der zu Tages- oder Schichtbeginn in der Kassenlade vorhanden ist. | Ja | Ja | Ja | Ja | Nein |
| 132 | Einzahlung überschreiben | Überschreibt die standardmäßige Einzahlung für Kundenaufträge. | Ja | Ja | Nein | Ja\* | Nein |
| 913 | Entwurfsmodus deaktivieren | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nein |
| 912 | Entwurfsmodus aktivieren | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nein |
| 1217 | Sets zerlegen | Zerlegen eines Kits in seine Produktkomponenten. | Ja | Ja | Ja | Ja | Nein |
| 624 | Rückerstattungsbeträge anzeigen | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Ja |
| 513 | Summe anzeigen | Zeigt den Saldo der Buchung auf der Debitorenanzeige an. | Ja | Ja | Ja | Ja | Nein |
| 623 | Debitordaten bearbeiten | Dient zum Bearbeiten der aktuellen Details des Debitors. | Ja | Ja | Nein | Nein | Nein |
| 614 | Debitorenauftrag bearbeiten | Rufen Sie den ausgewählten Auftrag zurück, damit er am Point-of-Sale geändert werden kann. | Nein | Nein | Nein | Nein | Nein |
| 615 | Angebot bearbeiten | Rufen Sie das ausgewählte Angebot zurück, damit es am Point-of-Sale geändert werden kann. | Nein | Nein | Nein | Nein | Nein |
| 518 | Aufwandskonten | Dient zum Erfassen des Geldes, das der Geldlade für gelegentliche Ausgaben entnommen wird. | Ja | Ja | Ja | Ja | Nein |
| 919 | Erweiterte Anmeldung | Weisen Sie Berechtigungen zum Anmelden hinzu oder entfernen Sie sie, indem Sie einen Strichcode scannen oder indem Sie eine Karte durch ein Lesegerät ziehen. | Ja | Ja | Ja | Ja | Nein |
| 1201 | Mittelzugang | Fügt zusätzliches Geld zur aktuellen Schicht oder Kassenlade hinzu. | Ja | Ja | Ja | Ja | Nein |
| 1218 | Entsperren von Peripheriegerät erzwingen | Das System verwendet diesen Arbeitsgang intern, um die Sperrung der POS-Peripheriegeräte aufzuheben. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nein |
| 520 | Geschenkkartensaldo | Zeigt den Saldo einer Geschenkkarte an. | Ja | Ja | Nein | Nein | Nein |
| 708 | Gerät deaktivieren | Deaktivieren Sie das aktuelle Gerät, damit es nicht als POS-Register verwendet werden kann. | Nein | Nein | Nein | Nein | Nein |
| 804 | Eingangsvorgang | Greifen Sie auf die Funktionen der Bestandsverwaltung eingehender Filialen zu. | Ja | Nein | Ja | Nein| Nein |
| 517 | Ertragskonten | Dient zum Erfassen des Geldes, das der Geldlade hinzugefügt wird, aber nicht aus einem Verkauf stammt. | Ja | Ja | Ja | Ja | Nein |
| 801 | Bestandssuche | Suchen Sie verfügbare, bestellte oder für Zusage verfügbare (ATP) Mengen für den aktuellen Shop und an anderen verfügbaren Lagerplätzen. | Ja | Ja | Ja | Nein | Nein |
| 806 | Lagerregulierung | Passen Sie den Bestand innerhalb oder außerhalb des Lagers mithilfe der Regulierungs- oder Umlagerungserfassung an. | Ja | Ja | Ja | Nein | Nein |
| 807 | Lagerbestandsumlagerung | Lagern Sie Artikel von einem Lagerplatz an einen anderen im Lager um. | Ja | Ja | Ja | Nein | Nein |
| 122 | Rechnungskommentar | Dient zum Eingeben eines Kommentars zur aktuellen Buchung. | Ja | Ja | Nein | Ja | Nein |
| 511 | Gutschrift ausstellen | Geben Sie eine Gutschrift aus, um einen Beleg anstelle einer Rückerstattung bereitzustellen. | Ja | Ja | Nein | Nein | Nein |
| 512 | Geschenkkarte ausstellen | Geben Sie eine neuen Geschenkkarte für den angegebenen Betrag aus. | Ja | Ja | Nein | Nein | Nein |
| 625 | Treuekarte ausstellen | Geben Sie eine Treuekarte an den Debitor aus, damit dieser am Treueprogramm des Geschäfts teilnehmen kann. | Ja | Ja | Ja | Nein | Nein |
| 300 | Positionsrabattbetrag | Dient zum Eingeben eines Rabattbetrags für einen Positionsartikel in der Buchung. Dieser Vorgang kann ausschließlich für rabattfähige Artikel verwendet und nur innerhalb der angegebenen Rabattgrenzen angegeben werden. | Ja | Ja | Nein | Ja | Nein |
| 301 | Positionsrabatt (in Prozent) | Dient zum Eingeben eines Rabattprozentsatzes für einen Positionsartikel in der Buchung. Dieser Vorgang kann ausschließlich für rabattfähige Artikel verwendet und nur innerhalb der angegebenen Rabattgrenzen angegeben werden. | Ja | Ja | Nein | Ja | Nein |
| 703 | Register sperren | Sperren Sie das aktuelle Register, damit es nicht verwendet werden kann, aber melden Sie nicht den aktuellen Benutzer ab. | Nein | Nein | Nein | Ja | Nein |
| 701 | Abmelden | Melden Sie den aktuellen Benutzer aus dem Register ab. | Ja | Ja | Ja | Ja | Nein |
| 521 | Treuekarten-Punktestand | Anzeigen des Saldos von Punkten für die angegebene Treuekarte. | Ja | Ja | Nein | Nein | Nein |
| 142 | Belastungen verwalten | Anzeigen und Verwalten der auf die Transaktion angewendeten Gebühren. | Ja | Ja | Nein | Nein| Nein |
| 918 | Schichten verwalten | Zeigen Sie eine Liste aktiver, unterbrochener und blinder, geschlossener Schichten an. | Ja | Ja | Ja | Nein | Nein |
| 914 | POS-Fenster minimieren | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nein |
| 1.000 | Kassenlade öffnen | Führen Sie einen Arbeitsgangs "Verkauf" aus, und öffnen Sie die derzeit ausgewählte Geldlade. | Ja | Ja | Ja | Ja | Nein |
| 928 | Auftragserfüllung | Dieser Arbeitsgang ermöglicht es Benutzern, Aufträge für die Filialabholung zu entnehmen, zu verpacken, zu versenden oder zurückzurufen. | Ja | Ja | Ja | Nein | Nein |
| 805 | Ausgangsvorgang | Zugriffsfunktionen für die Verwaltung von Sendungen ausgehender Transportaufträge. | Ja | Nein | Ja | Nein| Nein |
| 129 | Steuer für Positionsprodukt überschreiben | Überschreibt die Steuer für den ausgewählten Positionsartikel mit einer anderen angegebenen Steuer. | Ja | Ja | Nein | Ja | Nein |
| 130 | Steuer für Positionsprodukt aus Liste überschreiben | Überschreibt die Steuer für den ausgewählten Positionsartikel mit einer Steuer, die der Benutzer in einer Liste auswählt. | Ja | Ja | Nein | Ja | Nein |
| 127 | Transaktionssteuer überschreiben | Dient zum Überschreiben der Steuer für die Buchung, um eine andere angegebene Steuer zu verwenden. | Ja | Ja | Nein | Ja | Nein |
| 128 | Transaktionssteuer aus Liste überschreiben | Dient zum Überschreiben der Steuer für die Buchung mit einer Steuer, die der Benutzer in einer Liste auswählt. | Ja | Ja | Nein | Ja | Nein |
| 131 | Lieferschein | Erstellen eines Lieferscheins für den ausgewählten Auftrag. | Nein | Nein | Nein | Nein | Nein |
| 710 | Hardwarestation koppeln | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nein |
| 201 | Zahlung - Karte | Akzeptiert eine Kreditkarte, wie Kreditkarte oder Debitkarte als Zahlungsmittel. | Ja | Ja | Nein | Ja | Nein |
| 200 | Zahlung - Bar | Akzeptiert Bargeld als Zahlungsmittel. | Ja | Ja | Nein | Ja | Nein |
| 206 | Zahlung - Bar (schnell) | Schließt die Buchung in einem Schritt ab, und nimmt den Betrag an, der in bar fällig ist (genaue Änderung). | Ja | Ja | Nein | Ja | Nein |
| 204 | Zahlung - Scheck | Akzeptiert einen Scheck als Zahlungsmittel. | Ja | Ja | Nein | Ja | Nein |
| 213 | Zahlung - Gutschrift | Dient zum Akzeptieren einer vom Shop ausgestellten Gutschrift (Beleg). | Ja | Ja | Nein | Nein | Nein |
| 203 | Zahlung - Währung | Akzeptiert Zahlungen in verschiedenen Währungen. | Ja | Ja | Nein | Ja | Nein |
| 202 | Zahlung - Debitorenkonto | Dient zum Belasten eines Debitorenkontos mit der Buchung. Diese Zahlungsmethode ist nicht für Debitorenauftragseinzahlungen gültig. | Ja | Ja | Nein | Nein | Nein |
| 214 | Zahlung - Geschenkkarte | Annehmen einer Geschenkkarte, die der Shop ausgestellt hat. | Ja | Ja | Nein | Nein | Nein |
| 207 | Treuekarte bezahlen | Annehmen einer Treuekarte für Zahlung, und Einlösen von Punkten für qualifizierte Produkte. | Ja | Ja | Nein | Nein | Nein |
| 634 | Zahlungsverlauf | Dient zum Anzeigen der Zahlungshistorie des Debitors für den aktuellen Kundenauftrag. | Ja | Ja | Nein | Nein | Nein |
| 803 | Entnahme und Empfang | Öffnen Sie die Seite **Entnahme und Empfang**, auf der Sie Bestellungen auswählen können, im Shop zu entnehmen oder zu erhalten. | Ja | Ja | Ja | Nein | Nein |
| 632 | Alle Produkte abholen | Legen Sie die Erfüllungsmethode alle Positionen auf **Abholung im Shop** fest. | Ja | Ja | Nein | Ja\* | Nein |
| 631 | Ausgewählte Produkte abholen | Legen Sie die Erfüllungsmethode für die ausgewählten Positionen auf **Abholung im Shop** fest. | Ja | Ja | Nein | Ja\* | Nein |
| 400 | Popupmenü | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nein |
| 101 | Preisüberprüfung | Dieser Arbeitsgang ermöglicht dem Benutzer, den Preis eines angegebenen Produkts suchen. | Ja | Ja | Ja | Ja | Nein |
| 104 | Preisüberschreibung | Überschreibt den Preis eines Produkts, wenn die Konfiguration des Produkts Preisüberschreibungen zulässt. | Ja | Ja | Nein | Ja | Nein |
| 1058 | Steuer X drucken | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Ja |
| 1059 | Steuer Z drucken | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Ja |
| 927 | Artikelbeschriftung drucken | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nein |
| 926 | Regalbeschriftung drucken | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nein |
| 1056 | X drucken | X-Bericht für die aktuelle Schicht drucken | Ja | Ja | Ja | Nein | Nein |
| 103 | Produktkommentar | Fügt dem in der Buchung ausgewählten Positionsartikel einen Kommentar hinzu. | Ja | Ja | Nein | Ja | Nein |
| 100 | Produktverkauf | Fügt der Buchung ein angegebenes Produkt hinzu. | Ja | Ja | Ja | Ja | Nein |
| 108 | Produktsuche | Sucht nach einem Produkt, indem er zur Produktsuchseite am Point-of-Sale wechselt. | Ja | Ja | Ja | Ja | Nein |
| 633 | Ablaufdatum für Angebot | Dient zur Anzeige oder Änderung des Ablaufdatums auf einem Verkaufsangebot. | Ja | Ja | Nein | Ja\* | Nein |
| 627 | Neu berechnen | Berechnen Sie alle Debitoren-Auftragspositionen und Steuern auf Basis der aktuellen Konfiguration. | Ja | Ja | Nein | Ja\* | Nein |
| 143 | Belastung neu berechnen | Neuberechnung der auf den Auftrag angewendeten automatischen Gebühren. | Ja | Ja | Nein | Nein| Nein |
| 515 | Auftrag zurückrufen | Ermöglicht die Suche nach und das Zurückrufen von Debitorenaufträgen und Verkaufsangeboten. | Ja | Ja | Ja | Nein | Nein |
| 504 | Buchung zurückrufen | Dient zum Zurückrufen einer zuvor unterbrochenen Buchung vom aktuellen Shop. | Ja | Ja | Nein | Ja‡ | Nein |
| 305 | Treuepunkte einlösen | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Ja |
| 635 | Rückerstattung der Versandgebühren | Erstattet die Versandkosten für eine stornierte Bestellung. | Nein | Nein | Nein | Nein | Nein |
| 644 | Couponcode entfernen | Fordern Sie den Benutzer auf, Coupons zu entfernen, indem Sie diese in einer Liste auswählen Coupons, die momentan mit der Buchung zusammenhängen. | Ja | Ja | Nein | Ja | Nein |
| 1057 | Z erneut drucken | Druckt den Z-Bericht für die vorherige Schicht oder einer ausgewählten Schicht aus. | Ja | Ja | Ja | Nein | Nein |
| 1216 | Ein neues Kennwort eingeben | Diesen Vorgang kann ein Benutzer, der über die Kennwortrücksetzungsberechtigung verfügt, verwenden kann, um das Kennwort eines Mitarbeiters zurückzusetzen, indem er ein temporäres Kennwort verwendet. | Ja | Ja | Ja | Nein | Nein |
| 1219 | URL in POS öffnen | Öffnet eine vom Administrator konfigurierte URL in POS. | Ja | Ja | Ja | Ja | Nein |
| 109 | Produkt zurückgeben | Dient zum Ausführen einer Retoure für einzelne Produkte. Das nächste gescannte Produkt wird als zurückgegebenes Produkt mit einer negativen Menge und einem negativen Preis angezeigt. | Ja | Ja | Nein | Ja | Nein |
| 114 | Retourenbuchung | Zurückrufen einer vorherigen Buchung anhand der Bonnummer, um einige oder alle Produkte zurückzugeben. | Ja | Ja | Ja | Ja§ | Nein |
| 1211 | Ablage in Tresor | Führt eine Ablage im Tresor durch, um Geld aus dem Register in einen Tresor einzuschließen. | Ja | Ja | Ja | Ja | Nein |
| 516 | Verkaufsrechnung | Dieser Arbeitsgang ermöglicht dem Debitor, Zahlungen für die ausgewählte Rechnung vorzunehmen. | Ja | Ja | Nein | Nein | Nein |
| 502 | Verkäufer | Legt den **Sales Erfasser**-Wert in einem Auftrag für Kundenaufträge am Point-of-Sale fest. | Ja | Ja | Nein | Ja\* | Nein |
| 2000 | Zeitplanverwaltung | Dieser Vorgang wird noch nicht unterstützt. | Ja | Ja | Ja | Nein | Nein |
| 2001 | Zeitplananforderungen | Dieser Vorgang wird noch nicht unterstützt. | Ja | Ja | Ja | Nein | Nein |
| 622 | Durchsuchen | Dieser Arbeitsgang erlaubt Benutzern, POS-Schaltflächen vorzukonfigurieren, um Suchen nach Kategorie oder Artikel, Debitor auszuführen. | Ja | Ja | Ja | Ja | Nein |
| 1213 | Versandadresse suchen | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nein |
| 709 | Hardware Station auswählen | Wählt eine Hardwarestation aus einer Liste der verfügbaren Hardwarestationen aus. | Ja | Ja | Ja | Ja | Nein |
| 637 | Standardverkäufer für Buchung festlegen | Wählt eine der freigegebenen Provisionsverkaufsgruppen (Verkaufsrepräsentanten) als der Standardvertriebsmitarbeiter für Positionen aus, die zu einem späteren Zeitpunkt hinzugefügt werden. | Ja | Ja | Nein | Ja | Nein |
| 105 | Menge festlegen | Dient zum Ändern der Menge eines Positionsartikels in der Buchung. | Ja | Ja | Nein | Ja | Nein |
| 638 | Verkäufer für Position festlegen | Wählt eine der freigegebenen Provisionsverkaufsgruppen (Verkaufsrepräsentanten) als für die aktuell ausgewählte Position aus. | Ja | Ja | Nein | Ja | Nein |
| 630 | Alle Produkte versenden | Legen Sie den Erfüllungsmodus auf **Versand** für alle Positionsartikel fest. | Ja | Ja | Nein | Ja\* | Nein |
| 629 | Ausgewählte Produkte versenden | Legen Sie den Erfüllungsmodus für die ausgewählten Positionen auf **Versenden** fest. | Ja | Ja | Nein | Ja\* | Nein |
| 115 | Erfassung anzeigen | Anzeigen der Erfassung der Filiale. Sie können Buchungen, Neuauflagenzugänge und Geschenkzugänge anzeigen und Rückruf für Rücklieferung. | Ja | Ja | Ja | Ja\*\* | Nein |
| 802 | Bestandsmenge | Dient zum Erstellen und Ändern von Inventurerfassungen von physischem Bestand oder Zykluszählungen. | Ja | Ja | Ja | Nein | Nein |
| 401 | Untermenü | Dieser Arbeitsgang leitet den Benutzer zu einem anderen verknüpften Schaltflächenraster. | Ja | Ja | Ja | Ja | Nein |
| 1054 | Schicht aussetzen | Aktuelle Schicht aussetzen, sodass eine neue oder eine andere Schicht im aktuellen Schichtregister aktiviert werden kann. | Ja | Ja | Ja | Nein | Nein |
| 503 | Buchung aussetzen | Aktuelle Verkaufsbuchung aussetzen, sodass sie im Shop später zurückgerufen werden kann. | Ja | Ja | Nein | Ja‡ | Nein |
| 1004 | Aufgabenaufzeichnung | Öffnen der Aufgabenaufzeichnung, um Schritte im POS zu erfassen. | Nein | Nein | Nein | Ja | Nein |
| 1052 | Zahlungsmitteldeklaration | Dient zur Angabe des Geldbetrags in der Kassenlade für jede Zahlungsmethode. | Ja | Ja | Ja | Ja | Nein |
| 1210 | Zahlungsmittel entfernen | Entnimmt Geld aus der aktuellen Kassenlade oder Schicht. | Ja | Ja | Ja | Ja | Nein |
| 920 | Zeituhr | Ermöglicht Ein‑ und Ausstempeln aus Arbeitsschichten und Pausen. | Ja | Ja | Ja | Nein | Nein |
| 302 | Betrag für Rechnungsrabatt | Einen Rabattbetrag für die Buchung eingeben. Dieser Vorgang kann ausschließlich für rabattfähige Artikel verwendet und nur innerhalb der angegebenen Rabattgrenzen angegeben werden. | Ja | Ja | Nein | Ja | Nein |
| 303 | Rechnungsrabatt gesamt (in Prozent) | Einen Rabattprozentsatz für die Buchung eingeben. Dieser Vorgang kann ausschließlich für rabattfähige Artikel verwendet und nur innerhalb der angegebenen Rabattgrenzen angegeben werden. | Ja | Ja | Nein | Ja | Nein |
| 501 | Buchungskommentar | Fügt der aktuellen Buchung einen Kommentar hinzu. | Ja | Ja | Nein | Ja | Nein |
| 922 | Produktdetails anzeigen | Öffnen Sie die Produktdetailseite für den derzeit ausgewählten Positionsartikel. | Ja | Ja | Nein | Ja | Nein |
| 1003 | Berichte anzeigen | Anzeigen der Berichte, die für den aktuellen Benutzer konfiguriert wurden. | Ja | Ja | Ja | Nein | Nein |
| 921 | Zeituhreinträge anzeigen | Hier werden die Stempeluhreinträge für alle Arbeitskräfte im Shop angezeigt. | Ja | Ja | Ja | Nein | Nein |
| 211 | Zahlung stornieren | Stornieren der derzeit ausgewählten Zahlungsposition aus der Buchung. | Ja | Ja | Nein | Ja | Nein |
| 102 | Produkt stornieren | Stornieren des derzeit ausgewählten Positionsartikels aus der Buchung. | Ja | Ja | Nein | Ja | Nein |
| 500 | Buchung stornieren | Aktuellen Buchung leeren. | Ja | Ja | Nein | Ja | Nein |
| 916 | Windows Workflow Foundation | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nein |
| 924 | X-Bericht für Bankkarten | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Ja |
| 311 | Systemrabatte von Transaktionen entfernen | Entfernen Sie alle vom System angewendeten Rabatte, einschließlich Coupon-basierter Rabatte, aus der Transaktion. Manuelle Rabatte werden dadurch nicht entfernt. | Ja | Ja | Ja | Ja | Nein |
| 312 | Systemrabatte erneut anwenden | Wenden Sie Systemrabatte erneut auf die Transaktion an, wenn diese mithilfe des Vorgangs **Systemrabatte von Transaktion entfernen** entfernt wurden. | Ja | Ja | Ja | Ja | Nein |

\* Der Arbeitsgang ist nur im Offlinemodus verfügbar, wenn ein Kundenauftrag oder Verkaufsangebot erstellt wird, und nur bei Erstellung offline Debitorenbestellungen sowie von Verkaufsangeboten im POS-Funktionsprofil konfiguriert wird. Der Vorgang kann nicht ausgeführt werden, wenn Aufträge erstellt werden, indem Echtzeit-Service verwendet wird, wenn Aufträge erneut aufgerufen oder bearbeitet werden.

† Der Arbeitsgang kann im Offlinemodus ausgeführt werden, wenn der Betrag vom POS konfiguriert ist, um offline Erstellung von Debitoren im POS-Funktionsprofil zuzulassen.

‡, Wenn der POS offline ist, können unterbrochene Buchungen nur aus der aktuellen offline Datenbank des Registers erneut aufgerufen werden. Benutzer können Buchungen in Registern nicht aussetzen und erneut aufrufen.

§ Wenn der POS offline ist, können nur Buchungen in der aktuellen offline Datenbank für Rückgabe erneut aufgerufen werden.

\*\* Wenn der POS offline ist, werden nur Buchungen in der aktuellen offline Kanal-Datenbank in der Erfassung angezeigt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
