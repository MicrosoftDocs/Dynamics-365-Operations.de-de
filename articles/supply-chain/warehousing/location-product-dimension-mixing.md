---
title: Lagerplatz-Produktdimensionsmischung
description: Dieses Thema enthält Informationen zur Lagerplatz-Produktdimensionsmischung. Diese Lagerplatzprofilfunktion hilft bei der Verbesserung der Standortverwaltung, wenn Produktvarianten oder Produkte mit Dimensionen verwendet werden, z. B. in der Modebranche. Hier können Sie entscheiden, ob Konfigurationen, Farben, Stile und Größen für ein bestimmtes Lagerplatzprofil gemischt werden können oder ob nur eine dieser Dimensionen oder eine Kombination davon an demselben Lagerplatz platziert werden kann.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: c4e42864bfde9ed0650a88961b5a71b33b34c89d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004601"
---
# <a name="location-product-dimension-mixing"></a>Lagerplatz-Produktdimensionsmischung

[!include [banner](../includes/banner.md)]

Die Lagerplatz-Produktdimensionsmischung ist eine Lagerplatzprofilfunktion, die bei der Verbesserung der Standortverwaltung hilft, wenn Produktvarianten oder Produkte mit Dimensionen verwendet werden, z. B. in der Modebranche. Hier können Sie entscheiden, ob Konfigurationen, Farben, Stile und Größen für ein bestimmtes Lagerplatzprofil gemischt werden können oder ob nur eine dieser Dimensionen oder eine Kombination davon an demselben Lagerplatz platziert werden kann.

## <a name="turn-on-the-location-product-dimension-mixing-feature"></a>Funktion für Lagerplatz-Produktdimensionsmischung aktivieren

Bevor Sie die Lagerplatz-Produktdimensionsmischung verwenden können, muss die Funktion in Ihrem System aktiviert sein. Administratoren können mit der Einstellung [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und ggf. aktivieren. Dort wird die Funktion folgendermaßen aufgelistet:

- **Module:** *Lagerortverwaltung*
- **Funktionsname:** *Lagerplatz-Produktdimensionsmischung*

## <a name="setup"></a>Einstellung

Jedem Standort im Lagerort muss ein Lagerplatzprofil zugeordnet sein, das die Eigenschaften des Lagerplatzes beschreibt. Daher können alle Standorte, die dasselbe Lagerplatzprofil verwenden, die Produktdimensionsmischung nach dem Einrichten ermöglichen.

### <a name="configure-location-profiles-to-allow-product-dimension-mixing"></a>Lagerplatzprofile konfigurieren, um Produktdimensionsmischung zu ermöglichen

1. Wechseln Sie zu **Lagerortverwaltung \> Einrichtung \> Lagerort \> Lagerplatzprofile**.
1. Wählen Sie in der Liste der Lagerplatzprofile **BULK** aus.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Legen Sie im Inforegister **Allgemein** die Option **Spezifische Lagerplatz-Produktdimensionsmischung aktivieren** auf *Ja* fest.

    > [!NOTE]
    > Sie können diese Option nur dann auf *Ja* festlegen, wenn die Option **Gemischte Artikel zulassen** auf *Nein* festgelegt ist.

1. Legen Sie im Inforegister **Produktdimensionsmischung zulässig** die Option **Größe** auf *Ja* fest. In dem in diesem Thema beschriebenen Szenario kann das Mischen nur für Produkte mit unterschiedlichen Dimensionen der **Größe** durchgeführt werden. Es stehen jedoch auch andere Optionen zur Verfügung.
1. Wählen Sie **Speichern** aus.

### <a name="create-a-new-product-master-and-product-variants"></a>Einen neuen Produktmaster und Produktvarianten erstellen

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Produktmaster**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um einen Produktmaster zu erstellen.
1. Legen Sie im Dialogfeld **Neues Produkt** die folgenden Werte fest:

    - **Produkttyp:** *Artikel*
    - **Produktuntertyp:** *Produktmaster*
    - **Produktnummer:** *B0001*
    - **Produktname:** *B0001 Größe*
    - **Produktdimensionsgruppe:** *Größe*
    - **Konfigurationstechnologie:** *Vordefinierte Variante*

1. Wählen Sie **OK**.
1. Legen Sie auf der Seite **Produktdetails** im Inforegister **Allgemein** die folgenden Werte fest:

    - **Varianten automatisch generieren:** *Ja*
    - **Größengruppe:** *CASUALDHIR*

1. Um die vordefinierten Varianten anzuzeigen, wählen Sie im Aktivitätsbereich die Option **Produktvarianten** aus.

    Die Seite **Produktvarianten** erscheint und zeigt eine Liste von Varianten aus der Konfiguration der Größengruppe.

### <a name="release-products-to-the-usmf-company"></a>Produkte für USMF-Unternehmen freigeben

1. Wählen Sie im Aktivitätsbereich **Produkte freigeben** aus.
1. Bestätigen Sie auf der Seite **Produkte zum Freigeben auswählen**, dass die Produktnummer *B0001* in der Liste ist, und wählen Sie dann **Weiter** aus.
1. Wählen Sie **Weiter** aus, um die freizugebenden Produktvarianten zu bestätigen.
1. Wählen Sie auf der Seite **Unternehmen für die Freigabe auswählen** die Option *USMF* und dann **Weiter** aus, um die Auswahl zu bestätigen.
1. Wählen Sie auf der Seite **Auswahl bestätigen** die Option **Fertig** aus, um die Veröffentlichung abzuschließen.

    Sie erhalten die Nachricht „Vorgang abgeschlossen“.

### <a name="update-a-released-product-in-the-usmf-company"></a>Freigegebenes Produkt in USMF-Unternehmen aktualisieren

1. Stellen Sie sicher, dass Sie beim **USMF**-Unternehmen angemeldet sind.
1. Gehen Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**, um die Erstellung des freigegebenen Produkts abzuschließen.
1. Suchen und wählen Sie die Artikelnummer *B0001* aus, um die Seite **Details für freigegebene Produkte** zu öffnen.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Stellen Sie im Inforegister **Allgemein** sicher, dass das Feld **Artikelmodellgruppe** auf *FIFO* festgelegt ist.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Produkt** in der Gruppe **Einrichten** auf **Dimensionsgruppen**.
1. Legen Sie die folgenden Werte fest:

    - **Lagerdimensionsgruppe:** *Lagerort*
    - **Rückverfolgungsangabengruppe:** *Keine*

1. Wählen Sie **OK**.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Produkt** in der Gruppe **Einrichten** auf **Reservierungshierarchie**.
1. Legen Sie das Feld **Reservierungshierarchie** auf *Standard* fest, und wählen Sie dann **OK** aus.
1. Im Inforegister **Allgemein** im Abschnitt **Verwaltung** sehen Sie, dass Ihre Auswahl aktualisiert wurde.
1. Geben Sie im Inforegister **Kauf** im Feld **Preis** den Wert *10* ein.
1. Geben Sie im Inforegister **Kosten verwalten** im Feld **Artikelgruppe** die Zeichenfolge *Audio* ein.
1. Geben Sie im Inforegister **Kauf** im Feld **Preis** den Wert *10* ein.
1. Geben Sie im Inforegister **Lagerort** im Feld **Einheitensequenzgruppen-ID** die Zeichenfolge *ea* ein.
1. Wählen Sie **Speichern** aus.

### <a name="create-a-location-directive"></a>Erstellen einer Lagerplatzrichtlinie

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerplatzrichtlinien**.
1. Wählen Sie im linken Bereich im Feld **Arbeitsauftragstyp** *Bestellungen* aus.
1. Wählen Sie in der Liste die Lagerplatzrichtlinie namens *24 PO Direkt* aus.
1. Wählen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** die Option **Neu** aus, um dem Raster eine Position hinzuzufügen.
1. Legen Sie die folgenden Werte für die neue Position fest:

    - **Sequenznummer:** *1*

        Die neue Position sollte sich vor der zuvor vorhandenen Position befinden. Um die Änderung vorzunehmen, verwenden Sie die Schaltflächen **Nach oben** und **Nach unten** in der Symbolleiste, oder ändern Sie den Wert der **Sequenznummer** der vorhandenen Position zu *2*.

    - **Name:** *In BULK-Lagerplatzprofil einlagern*
    - **Feste Standortnutzung:** *Feste und nicht feste Lagerplätze*
    - **Negativen Lagerbestand zulassen:** *Kontrollkästchen deaktivieren (=Nein)*
    - **Charge aktiviert:** *Kontrollkästchen deaktivieren (=Nein)*
    - **Strategie:** *Keine*

1. Wählen Sie **Abfrage bearbeiten** über dem Gitter aus, während die neue Position noch ausgewählt ist.
1. Wählen Sie im Abfragedialogfeld auf der Registerkarte **Bereich** die Option **Hinzufügen** aus, um dem Raster eine Position hinzuzufügen.
1. Legen Sie die folgenden Werte für die neue Position fest:

    - **Tabelle:** *Lagerorte*
    - **Abgeleitete Tabelle:** *Lagerorte*
    - **Feld:** *Lagerortprofilkennung*
    - **Kriterien:** *BULK*

1. Wählen Sie **OK**.
1. Wählen Sie auf der Seite **Lagerplatzrichtlinien** im Aktivitätsbereich **Speichern** aus.

> [!NOTE]
> Wenn Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** im Feld **Strategie** die Standortstrategie *Konsolidieren* verwenden, wird die Einrichtung des Inforegisters **Produktdimensionsmischung zulässig** in den **Lagerplatzprofilen** überschrieben, und Artikel werden an denselben Lagerplatz verschoben, auch wenn dieses Verhalten von der Einrichtung nicht zugelassen wird.

### <a name="create-a-mobile-device-menu-item"></a>Erstellen eines Menüelements für ein mobiles Geräts

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.
1. Wählen Sie im Aktivitätsbereich die Option **Neu** aus, um einen Menüpunkt zum Sortieren zu erstellen.
1. Legen Sie im Header die folgenden Werte fest:

    - **Name des Menüpunkts:** *PO-Positionsempfang*
    - **Titel:** *PO-Positionsempfang*
    - **Modus:** *Arbeit*
    - **Vorhandene Arbeit verwenden:** *Nein*

1. Legen Sie im Inforegister **Allgemein** die folgenden Werte fest:

    - **Arbeitserstellungsprozess:** *Bestellungspositionsempfang und Einlagerung*
    - **Kennzeichen generieren:** *Ja*

1. Wählen Sie **Speichern** aus.

### <a name="configure-the-mobile-device-menu"></a>Menü des mobilen Geräts konfigurieren

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menü für mobiles Gerät**.
1. Wählen Sie in der Liste der Menüs **Eingehend** aus.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Suchen und wählen Sie in der Liste **Verfügbare Menüs und Menüpunkte** den Menüpunkt **PO-Positionsempfang** aus.
1. Wählen Sie die Schaltfläche mit dem Pfeil nach Rechts aus, um den Menüpunkt **PO-Positionsempfang** in die Liste **Menüstruktur** zu verschieben. Auf diese Weise fügen Sie dem ausgewählten Menü Ihren neuen Menüpunkt hinzu.
1. Wählen Sie **Speichern** aus.

## <a name="scenario"></a>Szenario

Dieses Demoszenario zeigt, wie zwei verschiedene Produktvarianten an denselben Lagerplatz platziert werden können, wenn das Lagerplatzprofil keine gemischten Artikel zulässt, aber die Funktion *Lagerplatz-Produktdimensionsmischung* aktiviert ist. In diesem Fall verwenden Sie die Variante **Größe** als Kriterium.

Bevor Sie beginnen, stellen Sie sicher, dass sich im Lagerort *24* leere Lagerplätze befinden, die das *BULK*-Lagerplatzprofil verwenden.

### <a name="create-a-purchase-order"></a>Eine Bestellung erstellen

Sie erstellen eine Bestellung mit drei Positionen: zwei Positionen für dieselbe Produktnummer, jedoch unterschiedliche **Größe**-Varianten und eine dritte Position für ein anderes Produkt ohne Varianten.

1. Wechseln Sie zu **Kreditorenkonten \> Bestellungen \> Alle Bestellungen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie im Dialogfeld **Bestellung erstellen** die folgenden Werte fest:

    - **Kreditorenkonto:** *1001*
    - **Lagerort:** *24*

1. Wählen Sie **OK**.
1. Die Bestellung wird erstellt und im Inforegister **Bestellpositionen** wird eine neue Position hinzugefügt. Notieren Sie sich die Bestellnummer.
1. Legen Sie die folgenden Werte für die neue Position fest:

    - **Artikelnummer:** *B0001*
    - **Größe** *L*
    - **Menge** *2*

1. Wählen Sie **Position hinzufügen** über dem Raster aus, um eine zweite Bestellposition hinzuzufügen, und legen Sie die folgenden Werte fest:

    - **Artikelnummer:** *B0001*
    - **Größe** *XL*
    - **Menge** *2*

1. Wählen Sie **Position hinzufügen** aus, um eine dritte Bestellposition hinzuzufügen, und legen Sie die folgenden Werte fest:

    - **Artikelnummer** *A001*
    - **Menge** *1*

1. Wählen Sie **Speichern** aus.

### <a name="receive-purchase-order-lines-in-the-warehouse-app"></a>Bestellpositionen in der Warehouse-App erhalten

1. Melden Sie sich bei der Warehouse-App als Benutzer an, der für den Lagerort *24* aktiviert ist.
1. Wählen Sie das Menü **Eingehend**.
1. Wählen Sie **PO-Positionsempfang**.
1. Wählen Sie das Feld **PONUM**, und geben Sie dann die Bestellnummer ein.
1. Bestätigen Sie Ihre Eingabe, indem Sie auf die Schaltfläche zum Bestätigen (✔) unten auf der Seite klicken.
1. Geben Sie die Positionsnummer aus der Bestellung ein, die eingeht. Wählen Sie das Feld **LINENUM**, und verwenden Sie dann das Nummernpad, um *1* einzugeben.
1. Bestätigen Sie Ihre Eingabe.
1. Geben Sie die zu empfangende Menge ein. Wählen Sie zweimal das Pluszeichen (**+**) aus, um den Wert im Feld **Menge** auf *2* zu erhöhen.
1. Registrieren Sie Ihren Eintrag, indem Sie auf die Schaltfläche (✔) unten auf der Seite klicken, und bestätigen Sie Ihre Eingabe, indem Sie erneut auf die Schaltfläche (✔) klicken.
1. Zeigen Sie die Informationen auf der Seite **Bestellungen: Einlagern** an. Diese Seite zeigt die Arbeit, die für die Einlagerung erstellt wurde (Arbeit 1).

    Der Lagerplatz, an dem der empfangene Artikel weggelegt wird, das Kennzeichen, der Artikel, die Größe und die Menge der gerade erledigten Aufgabe **PO-Positionsempfang** werden angezeigt.

1. Bestätigen Sie die Einlagerungsarbeiten.
1. Wiederholen Sie die Schritte 4 bis 11 für die Bestellposition 2. Geben Sie in Schritt 8 jedoch eine Menge von *1* an.

    Neue Einlagerungsarbeiten (Arbeit 2) werden an demselben Lagerplatz wie Arbeit 1 erstellt.

1. Wiederholen Sie erneut die Schritte 4 bis 11 für die Bestellposition 2. Geben Sie in Schritt 8 die verbleibende Menge von *1* an.

    Neue Einlagerungsarbeiten (Arbeit 3) werden an demselben Lagerplatz wie Arbeit 1 und Arbeit 2 erstellt. Dieses Verhalten tritt auf, weil die Lagerplatzrichtlinienstrategie *Konsolidieren* verwendet wird, und die Einrichtung im Inforegister **Produktdimensionsmischung zulässig** in den **Lagerplatzprofilen** *Bulk* ermöglicht die **Größe**-Variante, die an einem Lagerplatzprofil gemischt werden soll.

1. Wiederholen Sie die Schritte 4 bis 11 für die Bestellposition 3. Geben Sie in Schritt 8 eine Menge von *1* für Artikelnummer *A0001* an.

    Neue Einlagerungsarbeiten (Arbeit 4) werden für einen anderen Lagerplatz als den erstellt, der für die Bestellpositionen 1 und 2 verwendet wird. Dieses Verhalten tritt auf, weil das Lagerplatzprofil keine gemischten Produkte zulässt, jedoch gemischte Dimensionen desselben Produktmasters.

1. Wählen Sie die Menüschaltfläche oben auf der Seite (manchmal auch als Hamburger oder Hamburgerschaltfläche bezeichnet) und dann **Abbrechen** aus, um **PO-Positionsempfang** zu beenden.

> [!TIP]
> Sie können dieses Szenario wiederholen, diesmal jedoch **Größe** - *Nein* im Inforegister **Produktdimensionsmischung zulassen** in den **Lagerplatzprofilen** *BULK* festlegen, sodass keine der Produktdimensionen gemischt werden kann. In diesem Fall wird bei Erhalt der Bestellung jede Produktvariante an einen neuen Lagerplatz verschoben.