---
title: Online- und Offlineverkaufsstellen-(POS)-Vorgänge
description: Dieses Thema enthält Informationen zu den Verkaufsstelle (POS)-Arbeitsgängen in Microsoft Dynamics 365 for Retail. Es gibt an, an welcher Position in der Anwendung die Arbeitsgänge aufgerufen werden können, und ob sie im Offline-Modus verfügbar sind.
author: jblucher
manager: AnnBe
ms.date: 10/12/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-09-27
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 85708c7197a71e6ad9b814e2e63d62122c8890f6
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/14/2019
ms.locfileid: "842721"
---
# <a name="online-and-offline-point-of-sale-pos-operations"></a>Online- und Offlineverkaufsstellen-(POS)-Vorgänge

[!include [banner](includes/banner.md)]

Die meisten Aktivitäten, die Benutzer in Verkaufsstelle (POS) vornehmen, gelten als Arbeitsgänge. Arbeitsgänge werden im Microsoft Dynamics 365 for Retail-Backoffice konfiguriert und verwaltet. Viele Arbeitsgänge können den Schaltflächen im POS-Schaltflächenraster hinzugefügt werden. Benutzer können die Schaltflächen dann auswählen, um Vorgänge aufzurufen und die Funktion auszuführen. Andere Arbeitsgänge sind Teil der Haupt-POS-Anwendung und Schaltflächen werden entweder von Bildschirm-Schaltflächen oder als Bestandteil anderer Workflows oder Prozessen aufgerufen.

Die folgende Tabelle enthält Informationen zu den Arbeitsgängen, die in Retail Modern POS und Cloud POS für Dynamics 365 for Retail verfügbar sind. Die Tabelle gibt auch an, an welcher Position in der Anwendung die Arbeitsgänge aufgerufen werden können, und ob POS im Offline-Modus verfügbar sind.

Einige Arbeitsgänge sind derzeit nicht in Retail Modern POS oder Cloud POS für Dynamics 365 for Retail verfügbar. Einige dieser Arbeitsgänge sind jeder gebietsschemaspezifische Arbeitsgänge, die weitere Konfiguration und Erweiterungen erfordern. Auch einige Funktionen von Microsoft Dynamics AX 2012 werden derzeit nicht unterstützt.

Die folgenden Spalten geben an, woher die Arbeitsgänge aufgerufen werden können:

- **Schaltflächenraster** – Der Arbeitsgang kann zu den Schaltflächen in POS-Schaltflächenrastern zugewiesen werden, die Teil eines POS-Bildschirmlayouts sind.
- **Buchungsbildschirm** – Der Arbeitsgang kann aus POS-Schaltflächenrastern aufgerufen werden, die im Feld POS-Buchungs-Bildschirm konfiguriert werden.
- **Willkommen-Bildschirm** – Der Arbeitsgang kann aus POS-Schaltflächenrastern aufgerufen werden, die im Feld POS-Buchungs-Bildschirm konfiguriert werden.

> [!NOTE]
> Die Arbeitsgänge unten gelten für die neueste Version von Dynamics 365 for Retail. Einige Vorgänge haben sich möglicherweise geändert oder sind möglicherweise in früheren Versionen nicht verfügbar.

| ID | Arbeitsgang | Beschreibung | Schaltflächenraster | Transaktionsbildschirm | Willkommensbildschirm | Verfügbar offline | Gebietsschemaspezifisch |
|----|-----------|-------------|-------------|--------------------|----------------|-------------------|-----------------|
| 707 | Gerät aktivieren | Aktiviert das aktuelle Gerät, indem Sie einen authentifizierten Benutzer ermöglichen, Verbindungsinformationen verfügbar zu machen und eine Gerät und Register Kennung zuzuweisen | Nr. | Nr. | Nr. | Nr. | Nr. |
| 134 | Zugehörigkeit hinzufügen | Hinzufügen einer vorausgewählten Zugehörigkeit zu einer Transaktion. Wählen Sie die Zugehörigkeit auf der Seite **-Schaltflächeneigenschaften**. | Ja | Ja | Nr. | Ja | Nr. |
| 135 | Zugehörigkeit aus Liste hinzufügen | Hinzufügen einer Zugehörigkeit durch Auswahl aus einer Liste. | Ja | Ja | Ja | Ja | Nr. |
| 137 | Hinzufügen einer Zugehörigkeit zu einem Debitor | Hinzufügen einer Zugehörigkeit einem Debitor auf der Seite **Debitorendetails**. | Nr. | Nr. | Nr. | Ja | Nr. |
| 138 | Zugehörigkeit von Debitor entfernen | Zugehörigkeit eines Debitor auf der Seite **Debitorendetails** entfernen. | Nr. | Nr. | Nr. | Ja | Nr. |
| 643 | Couponcode hinzufügen | Einen Coupon hinzufügen durch Eingabe seines Codes in POS. | Ja | Ja | Nr. | Ja | Nr. |
| 117 | Treuekarte hinzufügen | Fordern Sie den Benutzer auf, eine Treuekartennummer einzugeben, die der aktuellen Buchung hinzugefügt wird. | Ja | Ja | Nr. | Ja | Nr. |
| 136 | Seriennummer hinzufügen | Dieser Arbeitsgang erlaubt dem Benutzer, eine Seriennummer für das derzeit ausgewählte Produkt anzugeben. | Ja | Ja | Nr. | Ja | Nr. |
| 1214 | Versandadresse hinzufügen | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nr. |
| 519 | Zu Geschenkkarte hinzufügen | Fügt der angegebenen Geschenkkarte einen Geldbetrag hinzu. | Ja | Ja | Nr. | Nr. | Nr. |
| 6000 | Überspringen der Steuerregistrierung zulassen | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Ja |
| 1212 | Bankeinzahlung | Erfasst den bei der Bank eingezahlten Geldbetrag und andere Informationen, z. B. die Nummer der Banktasche. | Ja | Ja | Ja | Ja | Nr. |
| 923 | Überprüfung der Banksummen | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Ja |
| 915 | Leerer Vorgang | Dieser Vorgang stellt eine anpassbare Schaltfläche dar, die vom Softwareentwickler programmgesteuert geändert werden kann, falls das Unternehmen einen speziellen Vorgang benötigt. | Ja | Ja | Ja | Ja | Nr. |
| 1053 | Schicht blind schließen | Festlegen der aktuellen Schicht, um Einträge blind vorzunehmen, und unterzeichnet Sie den Benutzer aus. Eine blind-geschlossene Schicht wird abgeschlossen, als Lieferant zu weiteren Buchungen jedoch zu den Kassenladearbeitsgängen, wie Zahlungsmittel entfernen und Kassensturz weiterhin geöffnet. | Ja | Ja | Ja | Nr. | Nr. |
| 310 | Summe berechnen | Wenn Rabattberechnung verzögert wird, initiiert dieser Arbeitsgang die Berechnung für die aktuelle Buchung. | Ja | Ja | Nr. | Ja | Nr. |
| 642 | Alle Produkte ausführen | Legen Sie die Lieferart für alle Positionen auf **Takeaway** fest. | Ja | Ja | Nr. | Ja\* | Nr. |
| 641 | Ausgewählte Produkte ausführen | Legen Sie die Lieferart für die ausgewählten Positionen auf **Takeaway** fest. | Ja | Ja | Nr. | Ja\* | Nr. |
| 1215 | Kennwort ändern | Dieser Arbeitsgang ermöglicht dem POS-Benutzer, sein Kennwort zu ändern. | Ja | Ja | Ja | Nr. | Nr. |
| 123 | Maßeinheit ändern | Ändern der Maßeinheit für den ausgewählten Positionsartikel. | Ja | Ja | Nr. | Ja | Nr. |
| 639 | Standardverkäufer für Buchung löschen | Entfernt die Provisionsverkaufsgruppe (Verkäufer) aus der Buchung. | Ja | Ja | Nr. | Ja | Nr. |
| 106 | Menge löschen | Setzt die Menge auf der momentan ausgewählten Position auf **1** zurück. | Ja | Ja | Nr. | Ja | Nr. |
| 640 | Verkäufer für Position löschen | Entfernt die Provisionsverkaufsgruppe (Verkaufsrepräsentanten) von der derzeit ausgewählten Position. | Ja | Ja | Nr. | Ja | Nr. |
| 121 | Verkäufer löschen | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nr. |
| 1055 | Schicht schließen | Schließt die aktuelle Schicht, Drucken eines Z-Berichts und meldet den Benutzer aus dem System ab. | Ja | Ja | Ja | Nr. | Nr. |
| 925 | Bankscheck kopieren | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Ja |
| 620 | Debitorenauftrag erstellen | POS-Buchung in einen Debitor-Auftrag umwandeln | Ja | Ja | Nr. | Ja\* | Nr. |
| 621 | Angebot erstellen | POS-Buchung in ein Vertriebsangebot umwandeln | Ja | Ja | Nr. | Ja\* | Nr. |
| 636 | Einzelhandelstransaktion erstellen | Dieser Arbeitsgang ermöglicht dem Benutzer, eine Standardverkaufsbuchung zu erstellen, wenn das Standardverhalten des POS ist, Kundenaufträge zu erstellen. | Ja | Ja | Nr. | Ja | Nr. |
| 600 | Kunde | Fügen Sie den angegeben Debitor der Buchung hinzu. | Nr. | Nr. | Nr. | Ja | Nr. |
| 1100 | Einzahlung auf Debitorenkonto | Nimmt eine Einzahlung auf dem Konto eines Debitors vor. | Ja | Ja | Ja | Ja | Ja |
| 612 | Debitor hinzufügen | Dieser Arbeitsgang ermöglicht dem Benutzer, einen neuen Debitorendatensatz zu erstellten. | Ja | Ja | Ja | Ja† | Nr. |
| 603 | Debitor löschen | Den Debitor aus der aktuellen Buchung entfernten. | Ja | Ja | Nr. | Ja | Nr. |
| 602 | Debitorensuche | Dieser Arbeitsgang erlaubt dem Benutzer die Suche nach einem Debitorendatensatz, indem er zur Debitorensuchseite am Point-of-Sale wechselt. | Ja | Ja | Ja | Ja | Nr. |
| 609 | Debitorenbuchungen | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nr. |
| 917 | Datenbankverbindungsstatus | Mit diesem Arbeitsgang können die Benutzer aktuelle Verbindungseinstellungen anzeigen und zwischen online oder offline Modi wechseln. | Ja | Ja | Ja | Ja | Nr. |
| 1200 | Ausgangsbetrag deklarieren | Deklariert den Betrag, der zu Tages- oder Schichtbeginn in der Kassenlade vorhanden ist. | Ja | Ja | Ja | Ja | Nr. |
| 132 | Einzahlung überschreiben | Überschreibt die standardmäßige Einzahlung für Kundenaufträge. | Ja | Ja | Nr. | Ja\* | Nr. |
| 913 | Entwurfsmodus deaktivieren | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nr. |
| 912 | Entwurfsmodus aktivieren | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nr. |
| 1217 | Sets zerlegen | Zerlegen eines Kits in seine Produktkomponenten. | Ja | Ja | Ja | Ja | Nr. |
| 624 | Rückerstattungsbeträge anzeigen | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Ja |
| 513 | Summe anzeigen | Zeigt den Saldo der Buchung auf der Debitorenanzeige an. | Ja | Ja | Ja | Ja | Nr. |
| 623 | Debitordaten bearbeiten | Dient zum Bearbeiten der aktuellen Details des Debitors. | Ja | Ja | Nr. | Nr. | Nr. |
| 614 | Debitorenauftrag bearbeiten | Rufen Sie den ausgewählten Auftrag zurück, damit er am Point-of-Sale geändert werden kann. | Nr. | Nr. | Nr. | Nr. | Nr. |
| 615 | Angebot bearbeiten | Rufen Sie das ausgewählte Angebot zurück, damit es am Point-of-Sale geändert werden kann. | Nr. | Nr. | Nr. | Nr. | Nr. |
| 518 | Aufwandskonten | Dient zum Erfassen des Geldes, das der Geldlade für gelegentliche Ausgaben entnommen wird. | Ja | Ja | Ja | Ja | Nr. |
| 919 | Erweiterte Anmeldung | Weisen Sie Berechtigungen zum Anmelden hinzu oder entfernen Sie sie, indem Sie einen Strichcode scannen oder indem Sie eine Karte durch ein Lesegerät ziehen. | Ja | Ja | Ja | Ja | Nein |
| 1201 | Mittelzugang | Dieser Arbeitsgang ermöglicht dem Benutzer, zusätzliches Geld der aktuellen Schicht oder Kassenlade hinzufügen. | Ja | Ja | Ja | Ja | Nr. |
| 1218 | Entsperren von Peripheriegerät erzwingen | Das System verwendet diesen Arbeitsgang intern, um die Sperrung der POS-Peripheriegeräte aufzuheben. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nr. |
| 520 | Geschenkkartensaldo | Zeigt den Saldo einer Geschenkkarte an. | Ja | Ja | Nr. | Nr. | Nr. |
| 708 | Gerät deaktivieren | Deaktivieren Sie das aktuelle Gerät, damit es nicht als POS-Register verwendet werden kann. | Nr. | Nr. | Nr. | Nr. | Nr. |
| 517 | Ertragskonten | Dient zum Erfassen des Geldes, das der Geldlade hinzugefügt wird, aber nicht aus einem Verkauf stammt. | Ja | Ja | Ja | Ja | Nr. |
| 801 | Bestandssuche | Suchen Sie verfügbare, bestellte oder für Zusage verfügbare (ATP) Mengen für den aktuellen Shop und an anderen verfügbaren Lagerplätzen. | Ja | Ja | Ja | Nr. | Nr. |
| 122 | Rechnungskommentar | Dieser Arbeitsgang ermöglicht dem Benutzer, einen Kommentar zur aktuellen Buchung einzugeben. | Ja | Ja | Nr. | Ja | Nr. |
| 511 | Gutschrift ausstellen | Geben Sie eine Gutschrift aus, um einen Beleg anstelle einer Rückerstattung bereitzustellen. | Ja | Ja | Nr. | Nr. | Nr. |
| 512 | Geschenkkarte ausstellen | Geben Sie eine neuen Geschenkkarte für den angegebenen Betrag aus. | Ja | Ja | Nr. | Nr. | Nr. |
| 625 | Treuekarte ausstellen | Geben Sie eine Treuekarte an den Debitor aus, damit dieser am Treueprogramm des Geschäfts teilnehmen kann. | Ja | Ja | Ja | Nr. | Nr. |
| 300 | Positionsrabattbetrag | Dient zum Eingeben eines Rabattbetrags für einen Positionsartikel in der Buchung. Dieser Vorgang kann ausschließlich für rabattfähige Artikel verwendet und nur innerhalb der angegebenen Rabattgrenzen angegeben werden. | Ja | Ja | Nr. | Ja | Nr. |
| 301 | Positionsrabatt (in Prozent) | Dient zum Eingeben eines Rabattprozentsatzes für einen Positionsartikel in der Buchung. Dieser Vorgang kann ausschließlich für rabattfähige Artikel verwendet und nur innerhalb der angegebenen Rabattgrenzen angegeben werden. | Ja | Ja | Nr. | Ja | Nr. |
| 703 | Register sperren | Sperren Sie das aktuelle Register, damit es nicht verwendet werden kann, aber melden Sie nicht den aktuellen Benutzer ab. | Nr. | Nr. | Nr. | Ja | Nr. |
| 701 | Abmelden | Melden Sie den aktuellen Benutzer aus dem Register ab. | Ja | Ja | Ja | Ja | Nr. |
| 521 | Treuekarten-Punktestand | Anzeigen des Saldos von Punkten für die angegebene Treuekarte. | Ja | Ja | Nr. | Nr. | Nr. |
| 918 | Schichten verwalten | Zeigen Sie eine Liste aktiver, unterbrochener und blinder, geschlossener Schichten an. | Ja | Ja | Ja | Nr. | Nr. |
| 914 | POS-Fenster minimieren | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nr. |
| 1.000 | Kassenlade öffnen | Führen Sie einen Arbeitsgangs "Verkauf" aus, und öffnen Sie die derzeit ausgewählte Geldlade. | Ja | Ja | Ja | Ja | Nr. |
| 928 | Auftragserfüllung | Dieser Arbeitsgang ermöglicht es Benutzern, Aufträge für die Filialabholung zu entnehmen, zu verpacken, zu versenden oder zurückzurufen. | Ja | Ja | Ja | Nr. | Nr. |
| 129 | Steuer für Positionsprodukt überschreiben | Überschreibt die Steuer für den ausgewählten Positionsartikel mit einer anderen angegebenen Steuer. | Ja | Ja | Nr. | Ja | Nr. |
| 130 | Steuer für Positionsprodukt aus Liste überschreiben | Überschreibt die Steuer für den ausgewählten Positionsartikel mit einer Steuer, die der Benutzer in einer Liste auswählt. | Ja | Ja | Nr. | Ja | Nr. |
| 127 | Transaktionssteuer überschreiben | Dient zum Überschreiben der Steuer für die Buchung, um eine andere angegebene Steuer zu verwenden. | Ja | Ja | Nr. | Ja | Nr. |
| 128 | Transaktionssteuer aus Liste überschreiben | Dient zum Überschreiben der Steuer für die Buchung mit einer Steuer, die der Benutzer in einer Liste auswählt. | Ja | Ja | Nr. | Ja | Nr. |
| 131 | Lieferschein | Erstellen eines Lieferscheins für den ausgewählten Auftrag. | Nr. | Nr. | Nr. | Nr. | Nr. |
| 710 | Hardwarestation koppeln | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nr. |
| 201 | Zahlung - Karte | Akzeptiert eine Kreditkarte, wie Kreditkarte oder Debitkarte als Zahlungsmittel. | Ja | Ja | Nr. | Ja | Nr. |
| 200 | Zahlung - Bar | Akzeptiert Bargeld als Zahlungsmittel. | Ja | Ja | Nr. | Ja | Nr. |
| 206 | Zahlung - Bar (schnell) | Schließt die Buchung in einem Schritt ab, und nimmt den Betrag an, der in bar fällig ist (genaue Änderung). | Ja | Ja | Nr. | Ja | Nr. |
| 204 | Zahlung - Scheck | Akzeptiert einen Scheck als Zahlungsmittel. | Ja | Ja | Nr. | Ja | Nr. |
| 213 | Zahlung - Gutschrift | Dient zum Akzeptieren einer vom Shop ausgestellten Gutschrift (Beleg). | Ja | Ja | Nr. | Nr. | Nr. |
| 203 | Zahlung - Währung | Akzeptiert Zahlungen in verschiedenen Währungen. | Ja | Ja | Nr. | Ja | Nr. |
| 202 | Zahlung - Debitorenkonto | Dient zum Belasten eines Debitorenkontos mit der Buchung. Diese Zahlungsmethode ist nicht für Debitorenauftragseinzahlungen gültig. | Ja | Ja | Nr. | Nr. | Nr. |
| 214 | Zahlung - Geschenkkarte | Annehmen einer Geschenkkarte, die der Shop ausgestellt hat. | Ja | Ja | Nr. | Nr. | Nr. |
| 207 | Treuekarte bezahlen | Annehmen einer Treuekarte für Zahlung, und Einlösen von Punkten für qualifizierte Produkte. | Ja | Ja | Nr. | Nr. | Nr. |
| 634 | Zahlungsverlauf | Dient zum Anzeigen der Zahlungshistorie des Debitors für den aktuellen Kundenauftrag. | Ja | Ja | Nr. | Nr. | Nr. |
| 803 | Entnahme und Empfang | Öffnen Sie die Seite **Entnahme und Empfang**, auf der Sie Bestellungen auswählen können, im Shop zu entnehmen oder zu erhalten. | Ja | Ja | Ja | Nr. | Nr. |
| 632 | Alle Produkte abholen | Legen Sie die Erfüllungsmethode alle Positionen auf **Abholung im Shop** fest. | Ja | Ja | Nr. | Ja\* | Nr. |
| 631 | Ausgewählte Produkte abholen | Legen Sie die Erfüllungsmethode für die ausgewählten Positionen auf **Abholung im Shop** fest. | Ja | Ja | Nr. | Ja\* | Nr. |
| 400 | Popupmenü | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nr. |
| 101 | Preisüberprüfung | Dieser Arbeitsgang ermöglicht dem Benutzer, den Preis eines angegebenen Produkts suchen. | Ja | Ja | Ja | Ja | Nr. |
| 104 | Preisüberschreibung | Überschreibt den Preis eines Produkts, wenn die Konfiguration des Produkts Preisüberschreibungen zulässt. | Ja | Ja | Nr. | Ja | Nr. |
| 1058 | Steuer X drucken | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Ja |
| 1059 | Steuer Z drucken | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Ja |
| 927 | Artikelbeschriftung drucken | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nr. |
| 926 | Regalbeschriftung drucken | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nr. |
| 1056 | X drucken | X-Bericht für die aktuelle Schicht drucken | Ja | Ja | Ja | Nr. | Nr. |
| 103 | Produktkommentar | Fügt dem in der Buchung ausgewählten Positionsartikel einen Kommentar hinzu. | Ja | Ja | Nr. | Ja | Nr. |
| 100 | Produktverkauf | Fügt der Buchung ein angegebenes Produkt hinzu. | Ja | Ja | Ja | Ja | Nr. |
| 108 | Produktsuche | Dieser Arbeitsgang erlaubt dem Benutzer die Suche nach einem Produkt, indem er zur Produktsuchseite am Point-of-Sale wechselt. | Ja | Ja | Ja | Ja | Nr. |
| 633 | Ablaufdatum für Angebot | Dieser Arbeitsgang erlaubt dem Benutzer, das Ablaufdatum auf einem Verkaufsangebot anzuzeigen oder zu ändern. | Ja | Ja | Nr. | Ja\* | Nr. |
| 627 | Neu berechnen | Berechnen Sie alle Debitoren-Auftragspositionen und Steuern auf Basis der aktuellen Konfiguration. | Ja | Ja | Nr. | Ja\* | Nr. |
| 515 | Auftrag zurückrufen | Dieser Arbeitsgang erlaubt Benutzern die Suche nach und das Zurückrufen von Debitorenaufträgen und Verkaufsangeboten. | Ja | Ja | Ja | Nr. | Nr. |
| 504 | Buchung zurückrufen | Dieser Arbeitsgang ermöglicht dem Benutzer, eine zuvor unterbrochene Buchung vom aktuellen Shops zurückzurufen. | Ja | Ja | Nr. | Ja‡ | Nr. |
| 305 | Treuepunkte einlösen | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Ja |
| 635 | Rückerstattung der Versandgebühren | Dieser Arbeitsgang ermöglicht dem Benutzer, Versandkosten auf einem stornierten Auftrag zu erstatten. | Nr. | Nr. | Nr. | Nr. | Nr. |
| 644 | Couponcode entfernen | Fordern Sie den Benutzer auf, Coupons zu entfernen, indem Sie diese in einer Liste auswählen Coupons, die momentan mit der Buchung zusammenhängen. | Ja | Ja | Nr. | Ja | Nr. |
| 1057 | Z erneut drucken | Druckt den Z-Bericht für die vorherige Schicht oder einer ausgewählten Schicht aus. | Ja | Ja | Ja | Nr. | Nr. |
| 1216 | Ein neues Kennwort eingeben | Diesen Vorgang kann ein Benutzer, der über die Kennwortrücksetzungsberechtigung verfügt, verwenden kann, um das Kennwort eines Mitarbeiters zurückzusetzen, indem er ein temporäres Kennwort verwendet. | Ja | Ja | Ja | Nr. | Nr. |
| 1219 | URL in POS öffnen | Mithilfe dieses Arbeitsgangs kann ein Benutzer eine von einem Administrator konfigurierte URL in POS öffnen. | Ja | Ja | Ja | Ja | Nr. | 
| 109 | Produkt zurückgeben | Dient zum Ausführen einer Retoure für einzelne Produkte. Das nächste gescannte Produkt wird als zurückgegebenes Produkt mit einer negativen Menge und einem negativen Preis angezeigt. | Ja | Ja | Nr. | Ja | Nr. |
| 114 | Retourenbuchung | Zurückrufen einer vorherigen Buchung anhand der Bonnummer, um einige oder alle Produkte zurückzugeben. | Ja | Ja | Ja | Ja§ | Nr. |
| 1211 | Ablage in Tresor | Führt eine Ablage im Tresor durch, um Geld aus dem Register in einen Tresor einzuschließen. | Ja | Ja | Ja | Ja | Nr. |
| 516 | Verkaufsrechnung | Dieser Arbeitsgang ermöglicht dem Debitor, Zahlungen für die ausgewählte Rechnung vorzunehmen. | Ja | Ja | Nr. | Nr. | Nr. |
| 502 | Verkäufer | Dieser Arbeitsgang ermöglicht dem Benutzer, den **Sales Erfasser**-Wert in einem Auftrag für Kundenaufträge am Point-of-Sale festzulegen. | Ja | Ja | Nr. | Ja\* | Nr. |
| 2000 | Zeitplanverwaltung | Dieser Arbeitsgang erlaubt Benutzern, Mitarbeiterzeitpläne zu erstellen, zu ändern oder anzuzeigen. | Ja | Ja | Ja | Nr. | Nr. |
| 2001 | Zeitplananforderungen | Dieser Arbeitsgang erlaubt Benutzern das Anfordern von Freizeit, das Austauschen von Schichten oder das Anbieten von Schichten an andere Mitarbeiter. | Ja | Ja | Ja | Nr. | Nr. |
| 622 | Aufträge durchsuchen | Dieser Arbeitsgang erlaubt Benutzern, POS-Schaltflächen vorzukonfigurieren, um Suchen nach Kategorie oder Artikel, Debitor auszuführen. | Ja | Ja | Ja | Ja | Nr. |
| 1213 | Versandadresse suchen | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nr. |
| 709 | Hardwarestation auswählen | Dieser Arbeitsgang ermöglicht dem Benutzer, eine Hardwarestation in einer Liste der verfügbaren Hardwarestationen auszuwählen. | Ja | Ja | Ja | Ja | Nr. |
| 637 | Standardverkäufer für Buchung festlegen | Dieser Arbeitsgang ermöglicht dem Benutzer, eine der freigegebenen Provisionsverkaufsgruppen (Verkaufsripse) als der Standardvertriebsmitarbeiter für Positionen auszuwählen, die zu einem späteren Zeitpunkt hinzugefügt werden. | Ja | Ja | Nr. | Ja | Nr. |
| 105 | Menge festlegen | Dient zum Ändern der Menge eines Positionsartikels in der Buchung. | Ja | Ja | Nr. | Ja | Nr. |
| 638 | Verkäufer für Position festlegen | Dieser Arbeitsgang ermöglicht dem Benutzer, eine der freigegebenen Provisionsverkaufsgruppen (Verkaufsrepräsentanten) als für die aktuell ausgewählte Position auszuwählen. | Ja | Ja | Nr. | Ja | Nr. |
| 630 | Alle Produkte versenden | Legen Sie den Erfüllungsmodus auf **Versand** für alle Positionsartikel fest. | Ja | Ja | Nr. | Ja\* | Nr. |
| 629 | Ausgewählte Produkte versenden | Legen Sie den Erfüllungsmodus für die ausgewählten Positionen auf **Versenden** fest. | Ja | Ja | Nr. | Ja\* | Nr. |
| 115 | Erfassung anzeigen | Anzeigen der Erfassung der Filiale. Sie können Buchungen, Neuauflagenzugänge und Geschenkzugänge anzeigen und Rückruf für Rücklieferung. | Ja | Ja | Ja | Ja\*\* | Nr. |
| 802 | Bestandsmenge | Dieser Arbeitsgang erlaubt Benutzer, Inventurerfassungen vordefinierten physischen Bestand oder Gangzählungen zu erstellen oder zu ändern. | Ja | Ja | Ja | Nr. | Nr. |
| 401 | Untermenü | Dieser Arbeitsgang leitet den Benutzer zu einem anderen verknüpften Schaltflächenraster. | Ja | Ja | Ja | Ja | Nr. |
| 1054 | Schicht aussetzen | Aktuelle Schicht aussetzen, sodass eine neue oder eine andere Schicht im aktuellen Schichtregister aktiviert werden kann. | Ja | Ja | Ja | Nr. | Nr. |
| 503 | Buchung aussetzen | Aktuelle Verkaufsbuchung aussetzen, sodass sie im Shop später zurückgerufen werden kann. | Ja | Ja | Nr. | Ja‡ | Nr. |
| 1004 | Aufgabenaufzeichnung | Öffnen der Aufgabenaufzeichnung, um Schritte im POS zu erfassen. | Nr. | Nr. | Nr. | Ja | Nr. |
| 1052 | Kassensturz | Dieser Arbeitsgang ermöglicht dem Benutzer, den Geldbetrag in der Kassenlade für jede Zahlungsmethode anzugeben. | Ja | Ja | Ja | Ja | Nr. |
| 1210 | Zahlungsmittel entfernen | Dieser Arbeitsgang ermöglicht dem Benutzer, Geld aus der aktuellen Schicht oder Kassenlade zu entfernen. | Ja | Ja | Ja | Ja | Nr. |
| 920 | Zeituhr | Dieser Arbeitsgang erlaubt Benutzern, aus Arbeitsschichten und Pausen ein- und auszustempeln. | Ja | Ja | Ja | Nr. | Nr. |
| 302 | Betrag für Rechnungsrabatt | Einen Rabattbetrag für die Buchung eingeben. Dieser Vorgang kann ausschließlich für rabattfähige Artikel verwendet und nur innerhalb der angegebenen Rabattgrenzen angegeben werden. | Ja | Ja | Nr. | Ja | Nr. |
| 303 | Rechnungsrabatt gesamt (in Prozent) | Einen Rabattprozentsatz für die Buchung eingeben. Dieser Vorgang kann ausschließlich für rabattfähige Artikel verwendet und nur innerhalb der angegebenen Rabattgrenzen angegeben werden. | Ja | Ja | Nr. | Ja | Nr. |
| 501 | Buchungskommentar | Fügt der aktuellen Buchung einen Kommentar hinzu. | Ja | Ja | Nr. | Ja | Nr. |
| 922 | Produktdetails anzeigen | Öffnen Sie die Produktdetailseite für den derzeit ausgewählten Positionsartikel. | Ja | Ja | Nr. | Ja | Nr. |
| 1003 | Berichte anzeigen | Anzeigen der Berichte, die für den aktuellen Benutzer konfiguriert wurden. | Ja | Ja | Ja | Nr. | Nr. |
| 921 | Zeituhreinträge anzeigen | Hier werden die Stempeluhreinträge für alle Arbeitskräfte im Shop angezeigt. | Ja | Ja | Ja | Nr. | Nr. |
| 211 | Zahlung stornieren | Stornieren der derzeit ausgewählten Zahlungsposition aus der Buchung. | Ja | Ja | Nr. | Ja | Nr. |
| 102 | Produkt stornieren | Stornieren des derzeit ausgewählten Positionsartikels aus der Buchung. | Ja | Ja | Nr. | Ja | Nr. |
| 500 | Buchung stornieren | Aktuellen Buchung leeren. | Ja | Ja | Nr. | Ja | Nr. |
| 916 | Windows Workflow Foundation | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nr. |
| 924 | X-Bericht für Bankkarten | Der Vorgang wird nicht unterstützt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Ja |

\* Der Arbeitsgang ist nur im Offlinemodus verfügbar, wenn ein Kundenauftrag oder Verkaufsangebot erstellt wird, und nur bei Erstellung offline Debitorenbestellungen sowie von Verkaufsangeboten im POS-Funktionsprofil konfiguriert wird. Der Vorgang kann nicht ausgeführt werden, wenn Aufträge erstellt werden, indem Echtzeit-Service verwendet wird, wenn Aufträge erneut aufgerufen oder bearbeitet werden.

† Der Arbeitsgang kann im Offlinemodus ausgeführt werden, wenn der Betrag vom POS konfiguriert ist, um offline Erstellung von Debitoren im POS-Funktionsprofil zuzulassen.

‡, Wenn der POS offline ist, können unterbrochene Buchungen nur aus der aktuellen offline Datenbank des Registers erneut aufgerufen werden. Benutzer können Buchungen in Registern nicht aussetzen und erneut aufrufen.

§ Wenn der POS offline ist, können nur Buchungen in der aktuellen offline Datenbank für Rückgabe erneut aufgerufen werden.

\*\* Wenn der POS offline ist, werden nur Buchungen in der aktuellen offline Kanal-Datenbank in der Erfassung angezeigt.
