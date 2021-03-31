---
title: Kundenaufträge in Point of Sale (POS)
description: Dieses Thema enthält Informationen zu Kundenaufträgen in Point of Sale (POS). Debitorenaufträge sind auch Sonderauftrag. Das Thema enthält eine Diskussion zu zugehörigen Parametern und Buchungsflüssen.
author: josaw1
manager: AnnBe
ms.date: 01/06/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: f60e07c1faae9bc3cb6d3c843e72e6000cff7591
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220509"
---
# <a name="customer-orders-in-point-of-sale-pos"></a>Kundenaufträge in Point of Sale (POS)

[!include [banner](includes/banner.md)]

Dieses Thema enthält Informationen zur Erstellung und Verwaltung von Kundenaufträgen in Point of Sale (POS). Kundenaufträge können verwendet werden, um dort Verkäufe zu erfassen, wo Käufer Produkte zu einem späteren Zeitpunkt oder von einem anderen Standort abholen oder Artikel gesendet bekommen möchten. 

In einer Omni-Channel-Commerce-Welt stellen viele Einzelhändler von Debitorenaufträgen als Option oder Sonderaufträge, um die verschiedenen Produkt- und Erfüllungsbedingungen zu erfüllen. Nachfolgend sind einige typische Szenarios:

- Ein Debitor fordert, dass Produkte für eine bestimmten Adresse an einem bestimmten Datum geliefert werden.
- Ein Debitor möchte Produkte von einem Shop oder einem Lagerplatz aufheben, der aus Filiale oder vom Lagerplatz abweicht, an dem der Debitor die Produkte gekauft hat.
- Ein Kunde in einem Laden möchte Produkte heute bestellen und zu einem späteren Zeitpunkt im gleichen Laden abholen.

Einzelhändler können auch Debitorenaufträge verwenden, um verlorenen Verkäufe zu minimieren, den vordefinierten Ausfälle möglicherweise nicht anzeigen, da die Waren zu unterschiedlichen Zeiten oder an einem Ort geliefert oder verarbeitet werden kann.

## <a name="set-up-customer-orders"></a>Debitorenbestellungen einrichten
Bevor Sie versuchen, die Kundenbestellfunktion in POS zu verwenden, stellen Sie sicher, dass Sie alle erforderlichen Konfigurationen in der Commerce-Zentrale abgeschlossen haben.

### <a name="configure-modes-of-delivery"></a>Konfigurieren von Lieferarten

Um Kundenbestellungen verwenden zu können, müssen Sie die Lieferarten konfigurieren, die der Ladenkanal verwenden kann. Sie müssen mindestens eine Lieferart definieren, die verwendet werden kann, wenn Bestellpositionen aus einem Laden an einen Kunden versendet werden. Sie müssen zudem mindestens eine Abholart definieren, die verwendet werden kann, wenn Bestellpositionen im Laden abgeholt werden. Lieferarten sind auf Seite **Versandarten** in der Commerce-Zentralverwaltung definiert. Einzelheiten zum Einrichten der Lieferarten für Commerce-Kanäle finden Sie unter [Lieferarten definieren](https://docs.microsoft.com/dynamics365/commerce/configure-call-center-delivery#define-delivery-modes).

![Seite „Lieferarten“](media/customer-order-modes-of-delivery.png)


### <a name="set-up-fulfillment-groups"></a>Erfüllungsgruppen einrichten

Einige Läden oder Lagerorte sind möglicherweise nicht in der Lage, Kundenaufträge zu erfüllen. Durch die Konfiguration von Erfüllungsgruppen kann eine Organisation angeben, welche Filialen und Lagerorte als Optionen für Benutzer angezeigt werden, die Kundenaufträge am POS erstellen. Erfüllungsgruppen werden auf der Seite **Erfüllungsgruppen** konfiguriert. Organisationen können beliebig viele Erfüllungsgruppen erstellen. Verknüpfen Sie die Erfüllungsgruppe – sobald sie definiert ist – mit einem Shop, indem Sie **Erfüllungsgruppenzuweisung** auf der Registerkarte im Aktivitätsbereich **Einrichten** der Seite **Shops** auswählen.

In Commerce Version 10.0.12 und höher können Organisationen definieren, ob die in Erfüllungsgruppen definierten Lagerort- oder Lagerort und Shop-Kombinationen für den Versand, die Abholung oder sowohl für den Versand als auch für die Abholung verwendet werden können. Dies ermöglicht dem Unternehmen zusätzliche Flexibilität bei der Bestimmung, welche Lagerorte beim Erstellen eines Debitorenauftrags für zu versendende Artikel und welche Shops beim Erstellen eines Debitorenauftrags für die Abholung von Artikeln ausgewählt werden können. Aktivieren Sie zur Nutzung dieser Konfigurationsoptionen die Funktion **Möglichkeit, die in der Erfüllungsgruppe aktivierten Standorte als „Versand“ oder „Abholung“ anzugeben** aktivieren. Wenn ein Lagerort, der mit einer Erfüllungsgruppe verknüpft ist, kein Geschäft ist, kann es nur als Versandort konfiguriert werden. Es kann nicht verwendet werden, wenn Bestellungen für die Abholung am POS konfiguriert sind.

![Seite „Erfüllungsgruppen“](media/customer-order-fulfillment-group.png)

### <a name="configure-channel-settings"></a>Kanaleinstellungen konfigurieren

Wenn Sie mit Kundenbestellungen am POS arbeiten, müssen Sie einige Einstellungen des Geschäftskanals berücksichtigen. Diese Einstellungen finden Sie auf der Seite **Shops** in der Commerce-Zentralverwaltung.

- **Lagerort** – Dieses Feld gibt den Lagerort an, in dem Bestellungen ausgeführt werden, die für den Versand aus dem Geschäft konfiguriert sind.
- **Zuordnung von Erfüllungsgruppen** – Wählen Sie diese Schaltfläche (auf der **Einrichten**-Registerkarte im Aktionsbereich) aus, um die Erfüllungsgruppen zu verknüpfen, auf die verwiesen wird, um Optionen für Abholorte oder Sendungsursprünge anzuzeigen, wenn Kundenaufträge am POS erstellt werden.
- **Zielbasierte Steuer verwenden** – Diese Option gibt an, ob die Lieferadresse verwendet wird, um die Steuergruppe zu bestimmen, die auf Bestellpositionen angewendet wird, die an die Adresse des Kunden versendet werden.
- **Debitorenbasierte Steuer verwenden** – Diese Option gibt an, ob die Steuergruppe, die für die Lieferadresse des Kunden definiert ist, zur Besteuerung von Kundenbestellungen verwendet wird, die am POS für den Versand zum Kunden nach Hause erstellt wurden.

![Shopkanal auf der Seite „Shops“ einrichten](media/customer-order-all-stores.png)

### <a name="set-up-customer-order-parameters"></a>Einrichten von Parametern für Kundenaufträge

Bevor Sie versuchen, Kundenaufträge am POS zu erstellen, müssen Sie die entsprechenden Parameter in der Commerce-Zentralverwaltung konfigurieren. Diese Parameter finden Sie auf der **Kundenbestellungen**-Registerkarte der **Handelsparameter**-Seite.

- **Standardauftragstyp** – Sie können den Auftragstyp angeben, der Kundenaufträgen, die am POS erstellt werden, standardmäßig zugewiesen wird. Diese Kundenaufträge können entweder Aufträge oder Angebotsaufträge sein. Unabhängig vom Standardauftragstyp können Benutzer weiterhin sowohl Aufträge als auch Kundenaufträge am POS erstellen.
- **Standardanzahlung in Prozent** – Geben Sie den Prozentsatz des Auftragsgesamtbetrags an, den der Debitor als eine Anzahlung bezahlen muss, bevor ein Auftrag bestätigt werden kann. Abhängig von ihren Berechtigungen können Filialmitarbeiter den Betrag möglicherweise mithilfe der Operation **Einzahlung überschreiben** am POS überschreiben, wenn diese Operation für das Transaktionsbildschirmlayout konfiguriert ist.
- **Abholtyp der Lieferung** – Geben Sie die Lieferart an, der auf Kundenauftragspositionen angewendet werden soll, die für die Abholung am POS konfiguriert sind.
- **Takeaway-Lieferart** – Geben Sie die Lieferart an, der auf Auftragspositionen angewendet werden soll, die als Takeaway-Auftragspositionen gelten, wenn ein gemischter Warenkorb erstellt wird, in dem einige Positionen abgeholt oder versendet werden und andere sofort vom Kunden mitgenommen werden.
- **Annullierungsgebührprozentsatz** – Wenn ein Zuschlag angewendet soll, wenn ein Kundenauftrag zurückgezogen wurde, geben Sie den Betrag dieses Zuschlages an.
- **Code für Stornogebühr** – Geben Sie den Debitorenbelastungscode an, der verwendet werden soll, wenn eine Stornogebühr auf über den POS stornierte Kundenbestellungen erhoben wird. Der Gebührencode definiert die Logik der Finanzbuchung für die Stornogebühr.
- **Versandkostencode** – Wenn die Option **Erweiterte automatische Gebühren verwenden** auf gesetzt **Ja** festgelegt ist, hat diese Parametereinstellung keine Auswirkung. Wenn diese Option auf **Nein** festgelegt ist, werden Benutzer aufgefordert, manuell eine Versandkostenpauschale einzugeben, wenn sie Kundenbestellungen am POS erstellen. Verwenden Sie diesen Parameter, um einen Debitorengebührencode zuzuordnen, der auf Bestellungen angewendet wird, wenn Benutzer eine Versandgebühr eingeben. Der Gebührencode definiert die Logik der Finanzbuchung für die Versandgebühr.
- **Erweiterte automatische Gebühren verwenden** – Legen Sie diese Option auf **Ja** fest, um vom System berechnete automatische Gebühren zu verwenden, wenn Kundenaufträge am POS erstellt werden. Diese automatischen Gebühren können zur Berechnung von Versandkosten oder anderen bestell- oder artikelspezifischen Gebühren verwendet werden. Weitere Informationen zum Einrichten und Verwenden der erweiterten automatischen Gebühren finden Sie unter [Erweiterte automatische Omni-Channel-Gebühren](https://docs.microsoft.com/dynamics365/commerce/omni-auto-charges).

![Registerkarte „Kundenbestellungen“ auf der Seite „Commerce-Parameter“](media/customer-order-parameters.png)

### <a name="update-transaction-screen-layouts-in-pos"></a>Aktualisieren der Layouts des Transaktionsbildschirms am POS

Stellen Sie sicher, dass der POS [Bildschirmlayout](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts) so konfiguriert ist, dass die Erstellung und Verwaltung von Kundenaufträgen unterstützt wird und alle erforderlichen POS-Vorgänge konfiguriert sind. Im Folgenden sind einige der POS-Vorgänge aufgeführt, die empfohlen werden, um die Erstellung und Verwaltung von Kundenaufträgen korrekt zu unterstützen:
- **Alle Produkte versenden** – Mit diesem Vorgang wird festgelegt, dass alle Positionen im Einkaufskorb der Transaktion an ein Ziel gesendet werden.
- **Ausgewählte Produkte versenden** – Mit diesem Vorgang wird festgelegt, dass ausgewählte Positionen im Einkaufskorb der Transaktion an ein Ziel gesendet werden.
- **Alle Produkte abholen** – Mit diesem Vorgang wird festgelegt, dass alle Positionen im Einkaufskorb der Transaktion von einem ausgewählten Shopstandort abgeholt werden.
- **Ausgewählte Produkte abholen** – Mit diesem Vorgang wird festgelegt, dass ausgewählte Positionen im Einkaufskorb der Transaktion von einem ausgewählten Shopstandort abgeholt werden.
- **Alle Produkte für Takeaway** – Mit diesem Vorgang wird festgelegt, dass alle Zeilen im Einkaufskorb der Transaktion mitgenommen werden. Wenn dieser Vorgang im POS verwendet wird, wird die Kundenbestellung in eine Cash-and-Carry-Transaktion umgewandelt.
- **Ausgewählte Produkte als Takeaway** – Mit diesem Vorgang wird festgelegt, dass ausgewählte Positionen im Einkaufskorb der Transaktion zum Zeitpunkt des Kaufs vom Kunden mitgenommen werden. Diese Operation ist nur in einem [Hybridbestellung](https://docs.microsoft.com/dynamics365/commerce/hybrid-customer-orders)-Szenario nützlich.
- **Bestellung zurückrufen** – Dieser Vorgang wird zum Suchen und Abrufen von Kundenaufträgen verwendet, damit POS-Benutzer sie nach Bedarf bearbeiten, stornieren oder erfüllungsbezogene Vorgänge ausführen können.
- **Lieferart ändern** – Mit diesem Vorgang können Sie die Lieferart für Positionen, die bereits für den Versand konfiguriert sind, schnell ändern, ohne dass Benutzer erneut den Flow „Alle Produkte versenden“ oder „Ausgewählte Produkte versenden“ erneut durchlaufen müssen.
- **Einzahlung überschreiben** – Mit diesem Vorgang können Sie den Einzahlungsbetrag ändern, den der Kunde für die ausgewählte Kundenbestellung bezahlt.

![Vorgänge auf dem POS-Transaktionsbildschirm](media/customer-order-screen-layout.png)

## <a name="work-with-customer-orders-in-pos"></a>Mit Kundenaufträgen in POS arbeiten

> [!NOTE]
> Die Funktionen zur Umsatzerkennung wird derzeit nicht für die Verwendung in Commerce-Kanälen (E-Commerce, POS, Callcenter) unterstützt. Mithilfe der Umsatzerkennung konfigurierte Artikel sollten nicht Aufträgen hinzugefügt werden, die in Commerce-Kanälen erstellt wurden. 

### <a name="create-a-customer-order-for-products-that-will-be-shipped-to-the-customer"></a>Einen Kundenauftrag für Produkte erstellen, die an den Kunden versendet werden

1. Fügen Sie auf dem POS-Transaktionsbildschirm der Transaktion einen Kunden hinzu.
2. Produkte zum Warenkorb hinzufügen
3. Wählen Sie **Ausgewählte versenden** oder **Alle versenden** aus, um die Produkte an eine Adresse im Kundenkonto zu versenden.
4. Wählen Sie die Option, um einen Kundenauftrag zu erstellen.
5. Bestätigen oder ändern Sie den Ort für „Versand von“, bestätigen oder ändern Sie die Versandadresse und wählen Sie eine Versandart aus.
6. Geben Sie das gewünschte Versanddatum der Bestellung des Kunden ein.
7. Verwenden Sie die Zahlungsfunktionen, um alle berechneten Beträge zu bezahlen, die fällig sind, oder verwenden Sie die **Einzahlung überschreiben**-Operation, um die fälligen Beträge zu ändern und dann die Zahlung anzuwenden.
8. Wenn der Gesamtbetrag der Bestellung nicht bezahlt wurde, geben Sie eine Kreditkarte ein, die für den Restbetrag erfasst wird, der bei Rechnungsstellung auf der Bestellung fällig ist.

### <a name="create-a-customer-order-for-products-that-the-customer-will-pick-up"></a>Einen Kundenauftrag für Produkte erstellen, die der Kunden abholt

1. Fügen Sie auf dem POS-Transaktionsbildschirm der Transaktion einen Kunden hinzu.
2. Produkte zum Warenkorb hinzufügen
3. Wählen Sie **Ausgewählte abholen** oder **Alle abholen** aus, um die Konfiguration der Auftragsabholung zu starten.
4. Wählen Sie den Shopstandort aus, in dem der Kunde die ausgewählten Artikel abholen möchte.
5. Wählen Sie ein Datum aus, an dem der Artikel abgeholt wird.
6. Verwenden Sie die Zahlungsfunktionen, um alle berechneten Beträge zu bezahlen, die fällig sind, oder verwenden Sie die **Einzahlung überschreiben**-Operation, um die fälligen Beträge zu ändern und dann die Zahlung anzuwenden.
7. Wenn die vollständige Bestellsumme nicht bezahlt wurde, wählen Sie aus, ob der Kunde die Zahlung später (bei der Abholung) vornehmen wird oder ob eine Kreditkarte jetzt mit einem Token versehen und zum Zeitpunkt der Abholung verwendet und erfasst wird.

### <a name="edit-an-existing-customer-order"></a>Bearbeiten eines bestehenden Kundenauftrags.

Einzelhandelsaufträge, die entweder im Online- oder im Shop-Kanal erstellt wurden, können bei Bedarf über den POS abgerufen und bearbeitet werden.

> [!IMPORTANT]
> Nicht alle Einzelhandelsaufträge können über die POS-Anwendung bearbeitet werden. Aufträge, die in einem Call Center-Kanal erstellt werden, können nicht über POS bearbeitet werden, wenn die Einstellung [Auftragsabschluss aktivieren](https://docs.microsoft.com/dynamics365/commerce/set-up-order-processing-options#enable-order-completion) für den Call Center-Kanal aktiviert ist. Um eine korrekte Zahlungsabwicklung sicherzustellen, müssen Aufträge, die aus einem Callcenter-Kanal stammen und die Funktion „Auftragsabschluss aktivieren“ verwenden, über die Callcenter-Anwendung in der Commerce-Zentrale bearbeitet werden.

In Version 10.0.17 und höher können Benutzer berechtigte Aufträge über die POS-Anwendung bearbeiten, auch wenn die Bestellung teilweise erfüllt ist. Bestellungen, die vollständig in Rechnung gestellt werden, können jedoch immer noch nicht über den POS bearbeitet werden. Aktivieren Sie die Funktion **Teilweise erfüllte Aufträge in der Verkaufsstelle bearbeiten** im Arbeitsbereich **Funktionsverwaltung**, um diese Funktionalität zu aktivieren. Wenn diese Funktion nicht aktiviert ist oder wenn Sie Version 10.0.16 oder früher verwenden, können Benutzer Debitorenaufträge nur in POS bearbeiten, wenn der Auftrag noch vollständig offen ist. Außerdem können Sie, wenn die Funktion aktiviert ist, einschränken, in welchen Shops teilweise erfüllte Aufträge bearbeitet werden können. Die Option zum Deaktivieren dieser Funktion für bestimmte Shops kann über das **Funktionsprofil** im Inforegister **Allgemein** konfiguriert werden.


1. Wählen Sie **Auftrag zurückrufen**.
2. Verwenden Sie **Suche**, um Filter einzugeben, um den Auftrag zu finden, und wählen Sie dann **Anwenden** aus.
3. Wählen Sie den Auftrag in der Ergebnisliste aus und wählen Sie dann **Bearbeiten**. Wenn die **Bearbeiten**-Schaltfläche nicht verfügbar ist, befindet sich der Auftrag in einem Zustand, in dem er nicht bearbeitet werden kann.
4. Nehmen Sie im Einkaufskorb der Transaktion alle erforderlichen Änderungen am Kundenauftrag vor. Einige Änderungen sind möglicherweise während der Bearbeitung nicht zulässig.
5. Schließen Sie den Bearbeitungsvorgang ab, indem Sie einen Zahlungsvorgang auswählen.
6. Um den Bearbeitungsprozess zu beenden, ohne Änderungen zu speichern, können Sie die Operation **Transaktion stornieren** verwenden.



### <a name="cancel-a-customer-order"></a>Stornieren eines Debitorenauftrags

1. Wählen Sie **Auftrag zurückrufen**.
2. Verwenden Sie **Suche**, um Filter einzugeben, um den Auftrag zu finden, und wählen Sie dann **Anwenden** aus.
3. Wählen Sie den Auftrag in der Ergebnisliste aus und wählen Sie dann **Stornieren**. Wenn die **Stornieren**-Schaltfläche nicht verfügbar ist, befindet sich der Auftrag in einem Zustand, in dem er nicht mehr storniert werden kann.
4. Wenn Stornogebühren konfiguriert sind, bestätigen Sie diese. Sie können die Stornogebühren nach Bedarf anpassen, bevor Sie sie bestätigen. 
5. Schließen Sie den Stornierungsvorgang im Einkaufskorb der Transaktion ab, indem Sie einen Zahlungsvorgang auswählen. Wenn die gezahlten Einzahlungen die Stornogebühr überschreiten, können Rückerstattungszahlungen fällig werden.
6. Um den Stornierungsprozess zu beenden, ohne Änderungen zu speichern, können Sie die Operation **Transaktion stornieren** verwenden.

## <a name="finalizing-the-customer-order-shipment-or-pickup-from-pos"></a>Abschluss der Kundenauftragslieferung oder der Abholung am POS

Nachdem ein Auftrag erstellt wurde, werden die Artikel vom Kunden je nach Konfiguration der Bestellung von einem Geschäft abgeholt oder versendet. Weitere Informationen zu diesem Vorgang finden Sie in der [Shopauftragserfüllung](https://docs.microsoft.com/dynamics365/commerce/order-fulfillment-overview)-Dokumentation.

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Asynchroner Transaktionsfluss für Kundenbestellungen

Kundenaufträge können im POS entweder im synchronen Modus oder im asynchronen Modus erstellt werden. Wenn Sie beim Erstellen von Kundenaufträgen am POS Leistungsprobleme oder Benutzerverzögerungen feststellen, sollten Sie die asynchrone Auftragserstellung aktivieren.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Aktivieren Sie Kundenaufträge, um diese im asynchronen Modus zu erstellen

1. Wählen Sie in der Commerce-Zentralverwaltung auf der Seite **Funktionsprofile** das Funktionsprofil aus, das dem Shop entspricht, den Sie konfigurieren möchten.
2. Wählen Sie im Inforegister **Allgemein** unter **Kundenauftrag in asynchronem Modus erstellen** die Option **Ja** aus.

Wenn die Option **Kundenauftrag in asynchronem Modus** auf **Ja** festgelegt wurde, werden Debitorenaufträge immer in asynchronen Modus erstellt, selbst wenn Retail Transaction Service (RTS) verfügbar ist. Wenn Sie diesen Option auf **Nein** setzen, werden Debitorenaufträge immer im Modus synchronen mithilfe von RTS erstellt. Wenn Kundenaufträge im asynchronen Modus erstellt werden, werden sie aus aus den Comerce Pull (P)-Jobs abgerufen und als Einzelhandelstransaktionen in der Commerce-Zentrale erstellt. Die entsprechenden Aufträge für die Einzelhandelstransaktionen werden erstellt, wenn **Aufträge synchronisieren** entweder manuell oder mithilfe von Chargenaufträgen ausgeführt wird.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Hybriddebitorenaufträge](hybrid-customer-orders.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]