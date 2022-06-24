---
title: Automatische Zuteilung von Gebühren
description: Die Gebührenfunktion in Microsoft Dynamics 365 Supply Chain Management hilft Ihnen dabei, Bestellungen oder Aufträgen automatisch Gebühren zuzuweisen.
author: GalynaFedorova
ms.date: 09/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2020-10-01
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a0dd10ba7ce0f6eca2549edb227eb9116edea2d7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857487"
---
# <a name="automatic-allocation-of-charges"></a>Automatische Zuteilung von Gebühren

[!include [banner](../includes/banner.md)]

Abhängig vom Kunden, mit dem Sie arbeiten, oder dem Artikel, den Sie verkaufen, möchten Sie möglicherweise bestimmte zusätzliche Gebühren erheben. Die *Gebühren*-Funktion in Microsoft Dynamics 365 Supply Chain Management hilft Ihnen dabei, Bestellungen oder Aufträgen automatisch Gebühren zuzuweisen.

Automatische Belastungen werden automatisch angewendet, wenn Sie einen Auftrag oder eine Bestellung erstellen. Sie können automatische Zuschläge für bestimmte Kreditoren, Debitoren oder Artikel oder für Gruppen von Kreditoren, Debitoren oder Artikel definieren. Sie können auch automatische Zuschläge festlegen, die für alle Kreditoren, Debitoren oder Artikel gültig sind.

## <a name="set-up-parameters"></a>Parameter einrichten

Die Seite **Beschaffungs- und Bezugsquellenparameter** enthält einige Einstellungen, die besonders relevant sind, wenn Sie Belastungen automatisch zuweisen möchten. Gehen Sie wie folgt vor, um diese Einrichtung abzuschließen.

1. Gehen Sie zu **Beschaffung und Ursproung\> Einstellungen \> Beschaffungs- und Ursprungsparameter**.
1. Öffnen Sie die Registerkarte **Preise**.
1. Nehmen Sie im Inforegister **Preise** die folgenden Einstellungen vor:
    - **Auto-Belastungen für Kopfzeile finden** – Gibt an, ob für Bestellköpfe automatisch Belastungen verrechnet werden sollen. Legen Sie diese Einstellung auf *Ja* fest, um die automatische Zuweisung von Belastungen zu verwenden.
    - **Auto-Belastungen für Position finden** – Gibt an, ob für Bestellpositionen automatisch Belastungen verrechnet werden sollen. Legen Sie diese Einstellung auf *Ja* fest, um die automatische Zuweisung von Belastungen zu verwenden.

## <a name="set-up-charges-codes"></a>Richten Sie einen Belastungscode ein

Um Gebühren zuzuweisen, müssen Sie zuerst Gebührencodes definieren.

1. Führen Sie einen dieser Schritte aus:

    - Für Bestellungen: Gehen Sie zu **Kreditorenkonten \> Gebühren einrichten \> Gebührencode**.
    - Für Aufträge: Gehen Sie zu **Debitoren \> Gebühren einrichten \> Gebührencode**.

1. Wählen Sie im Aktivitätsbereich **Neu** aus, um einen Code für Belastungen zu erstellen.
1. Legen Sie in der Kopfzeile des neuen Datensatzes die folgenden Felder fest:

    - **Gebührencode** – Geben Sie einen Code für die Gebühren ein.
    - **Beschreibung** - Geben Sie eine Beschreibung für die Gebühren ein.
    - **Artikel Umsatzsteuergruppe** – Wählen Sie gegebenenfalls eine Artikelumsatzsteuergruppe aus.
    - **Anteilige Verrechnung** – Setzen Sie diese Option auf *Ja*, wenn Sie Ihre Gebühren anteilig aufteilen möchten. Diese Option ist nur für Aufträge verfügbar.
    - **Maximaler Betrag** - Geben Sie den maximalen Abschreibungsbetrag ein, der für den Gebührencodes zulässig ist. Dieses Feld wird verwendet, um Belastungen für Kreditorenrechnungen zu überprüfen. Es ist nur für Bestellungen verfügbar.

        > [!NOTE]
        > Um die Funktion zum Überprüfen von Gebühren für Bestellungen zu aktivieren, gehen Sie zu **Kreditorenkonten \> Konfiguration \> Kreditorenkontenparameter**. Auf dem Inforegister **Rechnungsvalidierung** im Abschnitt **Rechnungsvalidierung** stellen Sie die Option **Aktivieren Sie die Validierung des Rechnungsabgleichs** auf *Ja* ein.

1. Das Inforegiser **Erfassung** enthält die Abschnitte **astschrift** und **Gutschrift**. Legen Sie die folgenden Felder fest, abhängig vom Hauptbuch, in das Sie die Gebühren buchen möchten:

    - **Art** – Wählen Sie den Kontotyp aus, auf den Sie buchen (*Sachbuch*, *Kunde*, oder *Artikel*).
    - **Buchung** – Wählen Sie die Art der zu erstellenden Buchungen aus (z.B. *Brokergebühr* oder *Kundenabrechnung*).
    - **Konto** – Wählen Sie das Konto aus, für das die Gebühr gebucht werden soll.

1. Wählen Sie im Aktionsbereich **Speichern** aus.

## <a name="create-charge-groups"></a>Erstellen Sie Gebührengruppen

Gebührengruppen weisen einer Gruppe von Kunden oder Lieferanten automatisch bestimmte Gebühren zu. In den folgenden Unterabschnitten wird beschrieben, wie Sie diese Gebührengruppen erstellen und zuweisen.

### <a name="charge-groups-for-purchase-orders"></a>Belastungsgruppen für Bestellungen

Führen Sie die folgenden Schritte aus, um Gebührengruppen für Bestellungen zu erstellen.

1. Gehen Sie zu **Kreditorenkonten \> Gebühren einrichten \> Lieferantengebührengruppe**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um dem Raster im Bereich Übersicht eine Zeile hinzuzufügen:

    - **Gebührengruppe** – Geben Sie den Namen der Gebührengruppe ein.
    - **Beschreibung** - Geben Sie eine Beschreibung für die Gebührengruppe ein.

1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Gehen Sie zu **Kreditorenkonten \> Lieferant \> Alle Anbieter** und öffnen Sie entweder einen vorhandenen Anbieter oder erstellen Sie einen neuen Anbieter.
1. Auf dem Inforegister **Standards für Bestellungen** im Abschnitt **Bestellung** legen Sie das Feld **Gebührengruppe** auf die Gebührengruppe fest, die Sie gerade erstellt haben.

### <a name="charge-groups-for-sales-orders"></a>Belastungsgruppen für Bestellungen

Führen Sie die folgenden Schritte aus, um Gebührengruppen für Bestellungen zu erstellen.

1. Wechseln Sie zu **Debitoren \> Belastungen einrichten \> Kunden-Belastungsgruppen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um dem Raster im Bereich Übersicht eine Zeile hinzuzufügen:

    - **Gebührengruppe** – Geben Sie den Namen der Gebührengruppe ein.
    - **Beschreibung** - Geben Sie eine Beschreibung für die Gebührengruppe ein.

1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Gehen Sie zu **Debitoren \> Kunden \> Alle Kunden** und öffnen Sie entweder einen bestehenden Kunden oder erstellen Sie einen neuen Kunden.
1. Auf dem Inforegister **Standards für Bestellungen** in dem Abschnitt **Bestellung** legen Sie das Feld **Gebührengruppe** auf die Gebührengruppe fest, die Sie gerade erstellt haben.

## <a name="define-auto-charges"></a>Automatische Zuschläge definieren

Führen Sie nach dem Einrichten Ihrer Gebührencodes die folgenden Schritte aus, um die automatischen Gebühren zu definieren.

1. Führen Sie einen dieser Schritte aus:

    - Für Bestellungen: Gehen Sie zu **Beschaffung \> Konfiguration \> Gebühren \> Automatische Ladevorgänge**.
    - Für Aufträge: Gehen Sie zu **Debitoren \> Konfiguration \> Gebühren einrichten \> Automatische Belastungen**.

1. Im Listenbereich im Feld **Ebene** wählen Sie im Feld die Stufe aus, für die Ihre automatische Aufladung gilt:

    - *Haupttabelle* – Übernimmt Zuschläge in den Auftragskopf.
    - *Zeile* – Übernimmt Zuschläge in die Auftragspositionen.

1. Wählen Sie eine vorhandene automatische Aufladung aus, um sie zu bearbeiten, oder wählen Sie **Neu**, um eine neue automatische Aufladung zu definieren.
1. In der Liste **Konto Code** wählen Sie in der Liste einen der folgenden Werte aus, um den Umfang der betroffenen Konten anzugeben:

    - *Tabelle* – Weist einem bestimmten Debitor oder Kreditor Zuschläge zu.
    - *Gruppe* – Weist einer Gruppe für sonstige Zuschläge bestimmte Zuschläge zu.
    - *Alle* – Weist allen Debitoren oder Kreditoren Zuschläge zu.

1. Im Feld **Kundenbeziehung** oder **Lieferantenbeziehung** wählen Sie einen bestimmten Kunden oder Lieferanten aus, wenn Sie das Feld **Kontocode** auf *Tabelle* setzen. Wenn Sie im Feld **Kontocode** die Option *Gruppe* ausgewählt haben, wählen Sie eine LIeferantengebührengruppe aus.
1. In dem Feld **Elementcode** wählen Sie einen der folgenden Werte aus, um den Umfang der betroffenen Konten anzugeben: Sie können einen Artikelcode nur auswählen, wenn Sie automatische Zuschläge auf der Zeilenebene definieren.

    - *Tabelle* – Weist einem bestimmten Artikel Zuschläge zu.
    - *Gruppe* – Weist einer Artikelzuschlagsgruppe Zuschläge zu.
    - *Alle* – Weist allen Artikeln Zuschläge zu.

1. Im Feld **Artikelcode** wählen Sie einen bestimmten Artikel, wenn Sie das Feld **Artikelcod** auf *Tabelle* festlegen. Wenn Sie im Feld **Artikelcode** die Option *Gruppe* ausgewählt haben, wählen Sie eine Artikelgebührengruppe aus.
1. **Nur für Kundenaufträge:** In dem Feld **Art des Lieferungscodes** wählen Sie im Feld einen der folgenden Werte aus, um den Umfang der betroffenen Zustellungsmodi anzugeben:

    - *Tabelle* – Einer bestimmten Lieferart Zuschläge zuweisen.
    - *Gruppe* – Einer bestimmten Lieferartgruppe Zuschläge zuweisen.
    - *Alle* - Allen Lieferarten Zuschläge zuweisen.

1. **Nur für Bestellungen:** Im Feld **Lieferungsbeziehungsmodus** wählen Sie einen bestimmten Lieferungsmodus, wenn Sie das Feld **Lieferungscodemodus** auf *Tabelle* festlegen. Wenn Sie das Feld **Lieferungscodemodus** auf *Gruppe* festlegen, wählen Sie einen Modus für die Lieferungsgruppe aus.
1. Auf dem Inforegister **Zeilen** definieren Sie die Belastungen und die Belastungssätze, die verwendet werden, wenn die aktuelle automatische Belastung angewendet wird. Sie können die Symbolleiste auf diesem Inforegister verwenden, um so viele Zeilen hinzuzufügen, wie Sie benötigen. Legen Sie für jede Zeile die folgenden Felder fest:

    - **Währung** – Wählen Sie die Währung aus, die zur Berechnung der Gebühr verwendet werden soll.
    - **Gebührencode** – Wählen Sie einen Code für die Gebühr aus.
    - **Kategorie** - Wählen Sie einen der folgenden Werte aus:

        - *Fest* – Die Belastung wird als fester Betrag in der Position eingegeben. Feste Zuschläge können sowohl für Zuschläge im Auftragskopf und in den Auftragspositionen verwendet werden.
        - *Stück* – Der Zuschlag basiert auf der Einheit. Diese Zuschläge können nur in Auftragspositionen verwendet werden. Sie werden angezeigt, wenn Sie die Gesamtsumme der Bestellung berechnen.
        - *Prozent* – Die Belastung wird als Prozentsatz in der Position eingegeben. Prozentzuschläge können sowohl für Zuschläge im Auftragskopf und in den Auftragspositionen verwendet werden.
        - *Intercompany-Prozent* – Der Zuschlag wird als Prozentsatz der Position für Intercompany-Aufträge eingegeben. Intercompany-Prozentsatz-Zuschläge können nur in Auftragspositionen verwendet werden.
        - *Extern* – Der Zuschlag wird durch einen Drittanbieterdienst berechnet, der mindestens einem Spediteur zugeordnet ist.

    - **Gebührenwert** – Geben Sie den Gebührenwert basierend auf der von Ihnen ausgewählten Kategorie ein.
    - **Gebühren Währungscode** – Geben Sie eine Währung für die Gebühr an, wenn Sie eine andere Währung als die im Feld **Währung** angegebene verwenden möchten. Sie können nur eine andere Währung eingeben, wenn der **Solltyp** oder der **Haben-Typ** entweder *Sachkontocode* oder *Artikel* lautet.
    - **Von Betrag** - Geben Sie einen Anfangsbetrag an, um den automatische Zuschlag anzuwenden. In diesem Zusammenhang bezieht sich der Betrag auf die Gesamtsumme der Bestellung.
    - **Zu Betrag** - Geben Sie einen Endbetrag an, um den automatische Zuschlag anzuwenden. In diesem Zusammenhang bezieht sich der Betrag auf die Gesamtsumme der Bestellung.
    - **Umsatzsteuergruppe** – Geben Sie eine Umsatzsteuergruppe an.
    - **Site** und **Lager** – Geben Sie einen Standort und ein Lager an, wenn Gebühren nur für einen bestimmten Standort und ein bestimmtes Lager erhoben werden sollen.
    - **Beibehalten** - Aktivieren Sie dieses Kontrollkästchen , um die Zuschlagsbuchungen nach der Fakturierung beizubehalten, damit der Zuschlag immer angewendet wird, wenn Sie eine neue Rechnung für das ausgewählte Debitorenkonto erstellen.

1. **Nur für Kundenaufträge:** Wenn Sie gestaffelte Gebühren berechnen möchten, lesen Sie [Staffelgebühren für Kundenaufträge](/dynamicsax-2012/appuser-itpro/about-tiered-charges-on-sales-orders) für weitere Information.

## <a name="allocate-charges-from-the-header-to-a-line"></a>Ordnen Sie einer Zeile Gebühren aus dem Header zu

Das folgende Verfahren zeigt, wie einer Zeile Gebühren auf Kopfebene zugewiesen werden. Bevor Sie mit diesem Verfahren beginnen, sollten Sie bereits eine Gebühr auf Kopfzeilen-Ebene für den Typ *fester Betrag* und eine Bestellung haben, in der diese Gebühr erhoben wird. Darüber hinaus sollte die Bestellung bereits mindestens einen Zeilenartikel enthalten.

1. Öffnen Sie die Bestellung oder den Belastungsauftrag.
1. Führen Sie im Aktivitätenbereich einen der folgenden Schritte aus:

    - Für Bestellungen: Auf der Registerkarte **Kauf** in der Gruppe **Gebühren** wählen Sie **Gebühren zuweisen**.
    - Für Aufträge: Auf der Registerkarte **Verkauf** in der Gruppe **Gebühren** wählen Sie **Gebühren zuweisen**.

1. In dem Dialogfeld **Ordnen Sie den Bestellpositionen Gebühren zu** legen Sie die folgenden Felder fest:

    - **Gebührenverteilung** – Wählen Sie einen der folgenden Werte aus, um festzulegen, wie die Gebühren zugewiesen werden sollen:

        - *Netto-Betrag* – Verteilen Sie die Gebühren nach jedem Zeilenbetrag im Verhältnis zum Gesamtnettobetrag.
        - *Menge* – Ordnen Sie die Gebühren entsprechend der Anzahl der Einheiten für jede Zeile im Verhältnis zur Gesamtzahl der Einheiten zu.
        - *Pro Zeile* – Die Zuschläge werden gleichmäßig gemäß der Gesamtanzahl der Positionen zugeordnet.

    - **Ordnen Sie den Zeilen Gebühren zu** – Wählen Sie einen Wert aus, um anzugeben, ob Gebühren allen Zeilen, nur positiven Zeilen oder nur negativen Zeilen zugeordnet werden sollen.
    - **Alle zuweisen** - Aktivieren Sie dieses Kontrollkästchen, um Zuschläge auch dann Bestellpositionen zuzuweisen, wenn der Code für sonstige Zuschläge einen anderen Solltyp als *Artikel* aufweist.
    - **Empfangen** - Aktivieren Sie dieses Kontrollkästchen, um Zuschläge nur eingegangenen Bestellpositionen zuzuordnen.
    - **Gelagert** - Aktivieren Sie dieses Kontrollkästchen, um Zuschläge nur gelagerten Bestellpositionen zuzuordnen.
    - **Auswahl anzeigen und bestimmte Zeilen löschen** – Aktivieren Sie dieses Kontrollkästchen, um bestimmte Zeilen von dieser Zuordnung auszuschließen. Wenn Sie dieses Kontrollkästchen aktivieren, wird der Raster **Wählen Sie Zeilen aus, die von der Zuordnung ausgeschlossen werden sollen** geöffnet. Dieses Raster umfasst nur die Positionen, die den Kriterien in den Feldern **Belastungen den Positionen zuteilen** und **Gelagert** entsprechen. Wenn Sie zum Beispiel **Positive Positionen** im Feld *Belastungen den Positionen zuteilen* und die Option **Gelagert** auswählen, werden nur positive, gelagerte Positionen im Raster angezeigt. Darüber hinaus filtert das Raster automatisch alle Zeilen heraus, für die bereits die volle Menge empfangen wurde. Deaktivieren Sie das Kontrollkästchen **Einschließen** für jede Zeile, die von der Zuordnung ausgeschlossen werden soll, während das Raster geöffnet ist. 

        > [!IMPORTANT]
        > Wenn Sie mit dem Raster **Wählen Sie Zeilen aus, die von der Zuordnung ausgeschlossen werden sollen** arbeiten, lassen Sie das Raster offen, bis Sie **Zuweisen** auswählen. Wenn Sie das Raster schließen, bevor Sie **Zuweisen** auswählen, gehen Ihre Einstellungen im Raster verloren. Daher werden Gebühren basierend auf den zuvor definierten Kriterien zugewiesen.

1. Wählen Sie **Zuordnen**, um Ihre Einstellungen zu übernehmen und das Abfragedialogfeld zu schließen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
