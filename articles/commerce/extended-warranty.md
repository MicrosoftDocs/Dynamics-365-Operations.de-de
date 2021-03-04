---
title: Erstellen und konfigurieren Sie erweiterte Garantien
description: In diesem Thema werden erweiterte Garantien behandelt und deren Erstellung und Konfiguration in Microsoft Dynamics 365 Commerce beschrieben.
author: sijoshi
manager: annbe
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: sijoshi
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: a875343d9b93f5ebf2c2992fba8b2f182310461e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412456"
---
# <a name="create-and-configure-extended-warranties"></a>Erstellen und konfigurieren Sie erweiterte Garantien

[!include [banner](includes/banner.md)]

In diesem Thema werden erweiterte Garantien behandelt und deren Erstellung und Konfiguration in Microsoft Dynamics 365 Commerce beschrieben.

## <a name="overview"></a>Übersicht

Kunden entscheiden sich zunehmend für erweiterten Support und Service, wenn sie Produkte kaufen, insbesondere Konsumgüter, die zu einem Premium-Preis verkauft werden, wie z. B. Telefone und Computer. Durch die Bereitstellung erweiterter Kaufgarantien können Einzelhändler zur Kundenbindung beitragen. Erweiterte Garantien informieren Kunden darüber, wo sie Service und Support erhalten können. Daher können sie darauf vertrauen, dass ihre Probleme effektiv behandelt werden.

Erweiterte Garantien können beim ersten Produktkauf an Kunden in einem Einzelhandelskanal verkauft werden. Sie können auch nach dem ersten Kauf für eine begrenzte Zeit verkauft werden.

### <a name="warranty-item-setup"></a>Einrichtung des Garantieartikels

Dynamics 365 Commerce bietet Funktionen, mit denen Sie ein Garantieelement erstellen und Attribute dafür festlegen können. Diese Attribute umfassen die Zuordnung zwischen einem Produkt und einem Garantieartikel, den Preis der Garantie und die Dauer der Garantie. Nachdem ein Garantieartikel konfiguriert und an die Organisationseinheit freigegeben wurde, kann ein Einzelhändler Garantien über MPOS (Modern Point of Sale), Online-Shops und andere Einzelhandelskanäle verkaufen.

### <a name="warranty-item-sales"></a>Einrichtung des Garantieartikelverkaufs

Erweiterte Garantien können beim ersten Produktkauf an Kunden in einem Einzelhandelskanal verkauft werden. Sie können auch nach dem ersten Kauf für eine begrenzte Zeit verkauft werden.

An der Verkaufsstelle (POS) werden Vertriebsmitarbeiter aufgefordert, eine erweiterte Garantie hinzuzufügen, wenn ein verwandtes Produkt in den Warenkorb eines Kunden gelegt wird. Daher wird Vertriebsmitarbeitern im Rahmen der Verkaufschance eine Upsell- oder Cross-Selling-Gelegenheit angeboten.

Kunden können auch später zurückkehren und eine erweiterte Garantie für ein zuvor erworbenes Produkt erwerben. In diesen Fällen kann ein Vertriebsmitarbeiter die ursprüngliche Transaktion nachschlagen und dem Kunden den entsprechenden Artikel mit erweiterter Garantie verkaufen.

### <a name="warranty-terminology"></a>Garantieterminologie

In der folgenden Tabelle sind einige Garantiebedingungen definiert.

| Zeitdauer | Beschreibung |
|------------------------------|--------------|
| Erweiterte Garantie/Garantie | Eine *erweiterte Garantie* bezieht sich auf einen Servicevertrag oder Vertrag, der Kunden eine verlängerte Garantie bietet. Die erweiterte Garantie umfasst den zusätzlichen Service des Austauschs oder Reparierens von Waren während der Garantiezeit. |
| Herstellergarantie | Eine *Herstellergarantie* (oft als bezeichnet als *eingeschränkte Garantie*) ist die Garantie, die Kunden beim Kauf eines Produkts erhalten. Hier sind einige Merkmale einer Herstellergarantie:<ul><li>Die Garantiekosten sind in den Produktkosten enthalten. Kunden müssen keinen zusätzlichen Betrag für die Herstellergarantie bezahlen.</li><li>Je nach Produktkategorie beträgt die Herstellergarantie in der Regel 30 Tage, sechs Monate oder ein Jahr. (Für die meisten Unterhaltungselektronikprodukte beträgt die Garantie ein Jahr).</li><li>Die Garantie deckt alle Mängel ab, die durch mechanische oder elektrische Ausfälle verursacht werden. Der Versicherungsschutz ist begrenzt und beinhaltet keine versehentlichen Schäden am gekauften Produkt. Kunden, die die von ihnen gekauften Produkte vor alltäglichen Schäden schützen möchten, sollten in eine erweiterte Garantie investieren. Die Garantieverlängerung beträgt je nach Produktkategorie zwei bis zehn Jahre. Sie haben auch eine breitere Abdeckung und decken alltägliche Pannen wie Tropfen, Verschüttungen und Flecken ab.</li></ul> |
| Garantieartikel | Ein *Garantieartikel* ist ein Artikel mit erweiterter Garantie, der für einen Artikel mit Garantie verkauft wird. Ein Beispiel ist ein zweijähriger Unfallschutzplan für Laptops. |
| Garantierter Artikel | Ein *garantierter Artikel* ist ein serialisiertes Produkt, für das eine Garantie verkauft wird. Zum Beispiel ist ein Laptop ein garantierter Artikel, für den zwei Jahre und drei Jahre erweiterte Garantie verkauft werden. |
| Garantiegruppe | Eine *Garantiegruppe* ist eine Beziehung zwischen Garantieartikeln und garantierten Artikeln. Der POS verwendet Garantiegruppen, um zu bestimmen, welche Garantieartikel Vertriebsmitarbeiter zum Hinzufügen aufgefordert werden sollten, wenn ein garantierter Artikel zum Warenkorb eines Kunden hinzugefügt wird. |
| Garantierichtlinie | Eine *Garantiebestimmung* ist eine Entität, die in Commerce erstellt wird, wenn eine Garantierichtlinie verkauft wird. Eine Garantierichtlinie enthält Informationen wie das Start- und Enddatum des gekauften Garantieartikels, die allgemeinen Geschäftsbedingungen und die Seriennummer des garantierten Produkts. Garantierichtlinien können an Kunden weitergegeben werden, sodass diese eine Referenz für den von ihnen gekauften erweiterten Garantiegegenstand haben. |

## <a name="create-a-warranty-item"></a>Anlegen eines Garantieartikels

Führen Sie die folgenden Schritte aus, um ein Garantieelement in Commerce zu erstellen.

1. Navigieren Sie zu **Einzelhandel und Handel \> Produkte und Kategorien \> Produkte**.
1. Wählen Sie **Neu** aus, um einen neuen Garantieartikel zu erstellen.
1. In dem Dialogfeld **Neues Produkt** im Feld **Produktart** wählen Sie **Dienstleistung**.
1. Wählen Sie im Feld **Produktuntertyp** den Eintrag **Produktmaster**.
1. Wählen Sie im Feld **Produktservicetyp** den Eintrag **Dienstleistung** aus.
1. Geben Sie in das Feld **Produktname** den Produktnamen ein.
1. In dem Feld **Einzelhandelskategorie** wählen Sie im Dropdown-Dialogfeld einen Wert aus und wählen Sie dann **OK**.
1. Geben Sie im Feld **Produktnummer** die Nummer des neuen Produkts ein.
1. Wählen Sie **OK**.
1. Auf der Seite **Produktdetails** im Inforegister **Garantie** legen Sie die Felder **Zeiteinheit** und **Länge der Zeit** ein.

    | Feldname | Wert | Beschreibung |
    |------------|-------|-------------|
    | Zeiteinheit | **Tage**, **Wochen**, **Monate**, oder **Jahre** | Dieses Feld gibt die Zeiteinheit an, die für die Garantie verwendet wird. |
    | Zeitdauer | Ein positiver ganzzahliger Wert | Dieses Feld gibt die Dauer der Garantie in der ausgewählten Zeiteinheit an. |

    Stellen Sie beispielsweise für eine zweijährige Garantie das Feld **Zeiteinheit** auf **Jahre** und das Feld **Länge der Zeit** auf **2**. Alternativ können Sie das Feld **Zeiteinheit** auf **Monate** und das Feld **Länge der Zeit** auf **24** festlegen, wie in der folgenden Abbildung gezeigt.

    ![Produktdetailseite für einen Garantieartikel](./media/ew-time-properties.png)

1. Wählen Sie **Speichern**, um den Garantieartikel zu speichern.
1. Geben Sie das Garantieprodukt an das Unternehmen weiter, damit es verkauft werden kann. Weitere Informationen zum Einrichten von Einzelhandelsprodukten finden Sie unter [Einrichten von Einzelhandelsprodukten](set-up-retail-products.md).
1. Auf der Seite **Freigegebene Produktdetails** im Inforgister **Garantie** stellen Sie die Felder **Preisspannenbasis**, **Untere Grenze**, und **Höchstgrenze** fest.

    | Feldname | Wert | Beschreibung |
    |------------|-------|-------------|
    | Preisspannenbasis | **Keiner**, **Grundpreis**, oder **Verkaufspreis** | <ul><li>**Keiner** – Die Werte **Untere Grenze** und **Höchstgrenze** von Preisklassen gelten nicht.</li><li>**Grundpreis** – Eine gegebene Garantie gilt, wenn der Grundpreis (d.h der Preis ohne Rabatte) des garantierten Artikels zwischen den Werten **Untere Grenze** und **Höchstgrenze**, die hier angegeben sind, basierend auf dem Preis des garantierten Artikels liegen.</li><li>**Verkaufspreis** – Dieser Wert ist für die zukünftige Verwendung reserviert.</li></ul> |
    | Untergrenze, Obergrenze | Ein positiver ganzzahliger Wert | Diese Felder definieren die oberen und unteren Preisgrenzen des garantierten Artikels und wie der aktuelle Garantieartikel auf den garantierten Artikel anwendbar ist. Diese Grenzwerte können auf dem Grundpreis des garantierten Artikels basieren (auch als vom Hersteller empfohlener Verkaufspreis bezeichnet \[UVP\]). Wenn das Feld **Preisspanne Basis** auf **Grundpreis** festgelegt ist, wird nur ein Garantieartikel (Produkt), dessen Grundpreis zwischen den Werten **Untere Grenze** und **Höchstgrenze** liegt, eine Aufforderung auslösen, das Garantieelement dem POS hinzuzufügen. |

    Die folgende Abbildung zeigt beispielsweise die **Preisspanne Basis**, das Feld ist auf den **Grundpreis** festgelegt, das Feld **Untere Grenze** ist auf $500 gesetzt, und das Feld **Höchstgrenze** auf $1000.
    
    ![Freigegebene Produktdetailseite für einen Garantieartikel](./media/ew-release-product-details.png)

1. Sortieren Sie den Garantieartikel auf den Kanal, auf dem er verkauft wird. Weitere Informationen finden Sie unter [Einrichten von Sortimenten](set-up-assortments.md).

### <a name="example"></a>Beispiel

Ein Artikel (Produkt) mit Garantie für einen Laptop hat einen Grundpreis $999, und es gibt zwei Artikel mit Garantie für einen Laptop:

- Garantie\_1 hat eine Untergrenze von $500 und eine Obergrenze von $1,000 und das Feld **Preisspanne Basis** ist auf **Grundpreis** festgesetzt.
- Garantie\_2 hat eine Untergrenze von $1,001 und eine Obergrenze von $2,000 und das Feld **Preisspanne Basis** ist auf **Grundpreis** festgesetzt.

In diesem Fall werden Sie aufgefordert, die Garantie hinzuzufügen, wenn der Artikel mit der Garantie für den Laptop in den Warenkorb eines Kunden gelegt wird\_1 wird am POS angezeigt, da der Preis des Laptops zwischen der unteren und oberen Garantiegrenze liegt\_1.

> [!NOTE]
> In diesem Beispiel, wenn Sie möchten, dass Eingabeaufforderungen für beide Garantien angezeigt werden\_1 und Garantie\_2, unabhängig vom Preis des garantierten Artikels, stellen Sie das **Preisspanne Basis** Feld auf **Keiner**.

## <a name="configure-channel-specific-settings"></a>Konfigurieren Sie kanalspezifische Einstellungen

Mit kanalspezifischen Einstellungen können Sie festlegen, ob am POS eine Aufforderung zum Hinzufügen eines Garantieartikels angezeigt werden soll, wenn ein Warenkorbartikel in den Warenkorb eines Kunden gelegt wird.

Führen Sie die folgenden Schritte aus, um Kanal spezifische Einstellungen in Commerce zu aktivieren.

1. Gehen Sie zu **Retail and Commerce \> Produkte und Kategorien \> Garantien \> Garanieeinstellungen**.
1. Auf der Registerkarte **Kanalspezifisch** in der **Aufforderung zur Gewährleistung** führen Sie einen der folgenden Schritte aus, um die Spalte für Ihren Kanal anzuzeigen:

    - Aktivieren Sie das Kontrollkästchen, wenn am POS eine Eingabeaufforderung für den Garantieartikel angezeigt werden soll, wenn der Garantieartikel in den Warenkorb gelegt wird.
    - Deaktivieren Sie das Kontrollkästchen, wenn am POS keine Eingabeaufforderung für den Garantieartikel angezeigt werden soll, wenn der Garantieartikel in den Warenkorb gelegt wird.

1. Führen Sie den Einzelvorgang **1070** zum Synchronisieren der Daten mit dem Kanal aus.

## <a name="configure-a-number-sequence-for-warranty-policies"></a>Konfigurieren Sie eine Nummernfolge für Garantierichtlinien

Jede Garantierichtlinie wird durch eine Garantierichtliniennummer eindeutig identifiziert, die durch eine Nummernfolge generiert wird. Weitere Informationen zu Nummernsquenzen finden Sie unter [Überblick über Nummernsequenzen](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).

Führen Sie die folgenden Schritte aus, um eine Nummernfolge für Garantierichtlinien in Commerce zu konfigurieren.

1. Gehen Sie zu **Retail and Commerce \> Produkte und Kategorien \> Garantien \> Garanieeinstellungen**.
1. Auf der **Zahlenfolgen** Registerkarte in der Zeile für die **Garantiebestimmungen** Referenz geben Sie einen Wert ein oder wählen Sie ihn aus dem Feld **Nummernfolgecode** aus.

## <a name="set-up-a-warranty-group"></a>Eine Garantiegruppe einrichten

Eine Garantiegruppe ist eine Beziehung zwischen Garantieartikeln und garantierten Artikeln. Der POS verwendet Garantiegruppen, um zu bestimmen, welche Garantieartikel Vertriebsmitarbeiter zum Hinzufügen aufgefordert werden sollten, wenn ein garantierter Artikel zum Warenkorb eines Kunden hinzugefügt wird.

Gehen Sie zum Einrichten einer Garantiegruppe in Commerce folgendermaßen vor:

1. Gehen Sie zu **Retail and Commerce \> Produkte und Kategorien \> Garantien \> Garaniegruppen**.
1. Wählen Sie **Neu** aus, um einen neuen Garantiegruppe zu erstellen.
1. Geben Sie im Feld **Name** einen Namen für die neue Gruppe ein.
1. Geben Sie auf dem Inforegister  im Feld **Allgemein** eine **Beschreibung** der Gruppe ein.
1. Auf dem Inforegister **Garantieprodukte** wählen Sie **Zeile hinzufügen**, um einen Garantieartikel hinzuzufügen.
1. In dem Feld **Bestellung anzeigen** geben Sie eine Nummer ein, um die Garantiegruppe am POS zu bewerten. Der POS zeigt Garantieartikel in aufsteigender Reihenfolge in der Garantieaufforderung an.
1. Auf dem Inforegister **Garantieprodukte** wählen Sie **Zeile hinzufügen**, um ein Garantieprodukt hinzuzufügen.
1. Wenn der Garantiegegenstand für eine ganze Kategorie von Garantiegegenständen (Produkten) gilt, wählen Sie die Kategorie im Feld **Kategorie** aus. Wenn der Garantiegegenstand auf einen bestimmten Garantiegegenstand (Produkt) anwendbar ist, wählen Sie das Produkt im Feld **Produkt** aus.
1. Auf dem Inforegister **Anwendbare Kanäle** wählen Sie **Zeile hinzufügen**, um den Kanal hinzuzufügen, in dem Sie den Garantieartikel verkaufen möchten.
1. Wählen Sie **Speichern**, um die Konfiguration zu speichern.
1. Wählen Sie **Veröffentlichen**, um die Garantiegruppe zu veröffentlichen.
1. Führen Sie den Einzelvorgang **1040** zum Synchronisieren von Daten mit dem Kanal aus.

## <a name="sell-warranty-items-at-the-pos"></a>Verkaufen Sie Garantieartikel am POS

Mit zwei POS-Vorgängen können Vertriebsmitarbeiter während des Workflows Garantieartikel für Kundenkäufe verkaufen:

- **Garantie hinzufügen** – Dieser Vorgang löst eine Eingabeaufforderung aus, in der die geltenden Garantien für einen im Warenkorb ausgewählten garantierten Artikel angezeigt werden.
- **Fügen Sie der bestehenden Transaktion eine Garantie hinzu** – Mit dieser Operation können Vertriebsmitarbeiter Garantien für garantierte Artikel verkaufen, die zuvor verkauft wurden. Vertriebsmitarbeiter können die ursprüngliche Transaktion für einen garantierten Artikel finden, indem sie die Belegnummer der Transaktion eingeben.

Die folgende Abbildung zeigt ein Beispiel einer POS-Terminalseite mit der Aufforderung, einen Garantieartikel für den aktuellen Kauf eines Garantieartikels hinzuzufügen.

![Beispiel für eine Aufforderung zum Hinzufügen eines Garantieartikels für den aktuellen Kauf](./media/ew-sell-warranty.png)

Die folgende Abbildung zeigt ein Beispiel für die Funktion zum Hinzufügen eines Garantieartikels für einen zuvor verkauften Garantieartikel.

![Beispiel für die Funktion zum Hinzufügen eines Garantieartikels für einen zuvor verkauften Garantieartikel](./media/ew-add-warranty-existing.png)

## <a name="process-warranty-transactions"></a>Garantiebuchungen verarbeiten

Wenn Garantien in Cash-and-Carry-Transaktionen verkauft werden, können Commerce-Benutzer die Transaktionen ausführen, nachdem die Transaktionen in der Commerce-Zentrale als Einzelauftrag **Garantietransaktionen verarbeiten** ausgeführt wurden, um die Garantietransaktionen zu verarbeiten und Garantierichtlinien zu erstellen.

Um Garantietransaktionen in Commerce Headquarters zu verarbeiten, folgen Sie diesen Schritten.

1. Gehen Sie zu **Retail and Commerce \> Produkte und Kategorien \> Garantien \> Garantietransaktionen verarbeiten**.
1. In dem **Wählen Sie Organisationsknoten** Dialogfeld im Feld **Organisationshierarchie** wählen Sie einen Wert.
1. In der Liste **Verfügbare Organisationsknoten** wählen Sie entweder ein einzelnes Geschäft oder, wenn Sie den Stapeljob für eine Gruppe von Geschäften erstellen möchten, einen Knoten aus.
1. Wählen Sie die Schaltfläche mit dem Pfeil nach Rechts, um das Feld in die Liste Ausgewählte Felder zu verschieben und wählen Sie **Ausgewählten Organisationsknoten**.
1. Wählen Sie **Im Hintergrund ausführen**.
1. Stellen Sie die Option **Stapelverarbeitung** auf **Ja** und wählen dann **Wiederholung**.
1. In dem **Wiederholung definieren** Dialogfeld im Feld **Anfangsdatum** wählen Sie in diesem Feld ein Startdatum für die Wiederholung aus oder geben Sie es ein.
1. In dem Feld **Startzeit** wählen Sie im Feld eine Startzeit für die Wiederholung aus oder geben Sie sie ein.
1. Führen Sie einen dieser Schritte aus:

    - Wählen Sie die Option **Kein Enddatum**, wenn die Wiederholung niemals enden sollte.
    - Wählen Sie die Option **Ende danach**,  wenn die Wiederholung nach einer bestimmten Anzahl von Läufen enden soll. Wenn Sie diese Option wählen, geben Sie nach der Auswahl dieser Option die Anzahl von Perioden ein.
    - Wählen Sie die Option **Enddatum**, wenn die Wiederholung an einem bestimmten Datum enden soll. Wenn Sie diese Option wählen, geben Sie nach der Auswahl dieser Option das Datum ein.

1. Wählen Sie **OK**.
1. Wählen Sie **OK**.

## <a name="warranty-policies"></a>Garantiebestimmungen

Wenn eine erweiterte Garantie verkauft wird, wird automatisch eine Garantierichtlinie erstellt. Garantierichtlinien können an Kunden weitergegeben werden, damit diese eine Referenz für den von ihnen gekauften erweiterten Garantiegegenstand haben. Zu den Eigenschaften der Garantierichtlinien gehören das effektive Start- und Ablaufdatum der Garantie, die allgemeinen Geschäftsbedingungen sowie die Seriennummer des Garantiegegenstandes, für den die Garantie verkauft wurde.

> [!NOTE]
> Garantierichtlinieneigenschaften werden automatisch generiert, wenn Garantierichtlinienentitäten erstellt werden. Derzeit können sie nicht manuell konfiguriert oder bearbeitet werden.

In der folgenden Tabelle werden die Eigenschaften der Garantierichtlinien und ihre Werte beschrieben. In der Commerce-Zentrale heißt die Datenbanktabelle WARRANTYPOLICY.

| Eigenschaftenname | Wert | Beschreibung |
|---------------|-------|-------------|
| Versicherungsnummer | Eine Zeichenkette (maximal 20 Zeichen) | Die Garantiebedingungen |
| WarrantiedItemId | Eine Zeichenkette (maximal 20 Zeichen) | Die Kennung des Garantieelements |
| WarrantiedInventoryLotId | Eine Zeichenkette (maximal 20 Zeichen) | Die Bestandlos-Kennung des Garantieelements |
| WarrantiedSerialNumber | Eine Zeichenkette (maximal 20 Zeichen) | Die Seriennummer des Garantieartikels |
| WarrantiedFulfilledDate | Ein Datum | Das Erfüllungsdatum des Garantieelements |
| WarrantyItemId | Eine Zeichenkette (maximal 20 Zeichen) | Die Kennung des Garantieartikels |
| WarrantyInventoryLotId | Eine Zeichenkette (maximal 20 Zeichen) | Die Bestandlos-Kennung des Garantieartikels |
| WarrantySalesDate | Ein Datum | Das Verkaufsdatum des Garantieartikels |
| WarrantyEffectiveDate | Ein Datum | Das effektive Datum der Garantierichtlinie |
| Garantieablaufdatum | Ein Datum | Das Ablaufdatum der Garantierichtlinie |
| CustAccount | Eine Zeichenkette (maximal 20 Zeichen) | Die Nummer des Debitorenkontos. |
| Status | **Erstellt**, **Nichtig**, **Wirksam**, oder **Abgelaufen** | Der Status der Garantierichtlinie |
| Notizen | Eine Zeichenkette (ein Maxium von 255 Zeichen) | Hinweise zur Garantiepolitik, wie z. B. Geschäftsbedingungen |

## <a name="frequently-asked-questions-faq"></a>Häufig gestellte Fragen (FAQ)

**Warum wird am POS keine Garantieaufforderung angezeigt?**

Stellen Sie sicher, dass der Garantieartikel dem Kanal zugeordnet ist. Stellen Sie außerdem sicher, dass die Garantiegruppe so konfiguriert ist, dass sie den entsprechenden Kanal enthält.

**Wenn ich versuche, einer vorhandenen Transaktion eine Garantie hinzuzufügen und die Bestellnummer des Kundenauftrags einzugeben, werden dann keine Transaktionsposten angezeigt?**

Belege können nur gefunden werden, wenn ein Pull-Job (P-Job) ausgeführt wird, um die Belege in die Commerce-Zentrale hochzuladen. Um den P-Job auszuführen, gehen Sie zu **Retail and Commerce \> Retail and Commerce IT \> Verteilungsplan**, wählen Sie den Einzelauftrag **P-0001** und wählen Sie dann **Jetzt ausführen**.

**Warum gilt die Garantiefunktion nur für serialisierte Produkte?**

Eine Garantie ist eine Dienstleistung, die für ein bestimmtes, einzigartiges Produkt erbracht wird. In Dynamics 365 kann ein Produkt nur durch eine Seriennummer eindeutig identifiziert werden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Einzelhandelsprodukte einrichten](set-up-retail-products.md)

[Sortimente einrichten](set-up-assortments.md)

[Nummernkreise – Übersicht](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]