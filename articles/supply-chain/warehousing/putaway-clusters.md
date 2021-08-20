---
title: Clustereinlagerung
description: Einlagerungs-Cluster bieten eine Möglichkeit, mehrere Ladungsträger gleichzeitig zu entnehmen und diese dann an verschiedenen Lagerplätzen einzulagern. Sie können sehr nützlich für Einzelhandelsgeschäfte sein, bei denen Ladungsträger in der Regel keine vollen Paletten mit Bestand darstellen.
author: Mirzaab
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: c2b12798a6ef9c2d4aa022e0c270d8191b2cf4e7fc844042ed88c4eb9f5b98a5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741907"
---
# <a name="putaway-clusters"></a>Clustereinlagerung

[!include [banner](../includes/banner.md)]

Einlagerungs-Cluster bieten eine Möglichkeit, mehrere Ladungsträger gleichzeitig zu entnehmen und diese dann an verschiedenen Lagerplätzen einzulagern. Dieser Prozess wird oft als *Milchlauf* bezeichnet. Clustereinlagerungen können sehr nützlich für Einzelhandelsgeschäfte sein, bei denen die Ladungsträger in der Regel keine vollen Paletten mit Bestand sind. 

## <a name="turn-on-the-cluster-putaway-feature"></a>Schalten Sie die Funktion Clustereinlagerung ein

Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden. Administratoren können mit der Einstellung [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und ggf. aktivieren. Dort wird die Funktion folgendermaßen aufgelistet:

- **Module:** *Lagerortverwaltung*
- **Funktionsname:** *Funktion Clustereinlagerung*

## <a name="setup-for-the-example-scenario"></a>Einrichten für das Beispielszenario

### <a name="cluster-profiles"></a>Clusterprofile

Das Clustereinlagerungs-Profil bestimmt, wohin ein Element geht, basierend auf dem Lagerplatz, der dem Element zum Zeitpunkt des Eingangs zugewiesen ist. Wenn verschiedene Cluster benötigt werden, sollten verschiedene Clustereinlagerungen erstellt werden, eine für jeden Menüpunkt des mobilen Geräts.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Clusterprofile**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie in der Ansicht **Kopfzeile** die folgenden Werte fest:

    - **Clustereinlagerungsprofil-ID:** *Clustereinlagerung*
    - **Name der Clustereinlagerungs-Profil-ID:** *Clustereinlagerung*
    - **Typ der Clustereinlagerung:** *Einlagerung*
    - **Sequenznummer:** Akzeptieren Sie den Standardwert.

1. Wählen Sie **Speichern**, um die erforderlichen Felder auf dem Inforegister **Allgemein** verfügbar zu machen.
1. Legen Sie im Inforegister **Allgemein** die folgenden Werte fest:

    - **Zeitpunkt der Cluster-Zuweisung:** *Beim Empfang*

        Dieses Feld legt fest, ob der eingelagerte Cluster sofort bei Eingang des Bestandes zugewiesen werden soll, oder ob er später sortiert werden soll.

    - **Regel für Cluster-Zuweisung:** *Manuell*

        Dieses Feld legt fest, ob die Clusterzuordnung automatisch vom System oder manuell vom Benutzer bestimmt werden soll.

    - **Richtliniencode:** Lassen Sie dieses Feld leer.
    - **Clustereinlagerung lokalisieren:** *Empfang*

        Folgende Werte sind verfügbar:

        - **Empfang** - Ein Lagerplatz wird sofort beim Empfang gefunden.
        - **Cluster schließen** - Ein Lagerplatz wird gefunden, wenn der Cluster geschlossen wird.
        - **Benutzergesteuert** - Ein Lagerplatz wird gefunden, wenn der Ladungsträger zum Einlagern aus dem Cluster entnommen wird. In diesem Fall wird kein Lagerplatz angegeben, wenn das Einlagerungswerk erstellt wird. Beim Einlagern selbst muss der Benutzer den Ladungsträger oder die Arbeits-ID scannen, um den Einlagerungsschritt zu initiieren. Das System findet dann den Lagerplatz wieder und sagt dem Benutzer, wo er die entnommene Menge einlagern soll.

    - **Clustereinlagerung pro Benutzer:** *Nein*

        Dieses Feld legt fest, ob jeder Cluster pro Benutzer eindeutig sein soll, wenn Cluster automatisch zugewiesen werden. Es ist nur verfügbar, wenn das Feld **Cluster-Zuweisungsregel** auf *Automatisch* festgelegt ist.

    - **Einheitsbeschränkung:** Lassen Sie dieses Feld leer.

        Dieses Feld definiert die Einheit, die empfangen werden muss, damit das Profil gültig ist. Wenn es leer gelassen wird, sind alle Einheiten gültig.

    - **Unterbrechung der Einheit:** *Einzelperson*

        Dieses Feld legt fest, ob beim Schließen eines Clusters der gesamte Bestand (unter Verwendung der Cluster-ID und des Kennzeichens) auf einen Ladungsträger konsolidiert werden soll und ob er als einzelner Ladungsträger oder getrennt auf den empfangenen Ladungsträgern eingelagert werden soll. Dieses Feld ist nicht verfügbar, wenn das Feld **Clustereinlagerung einlagern** auf *Empfang* festgelegt ist.

    - **Cluster bleibt als übergeordneter Ladungsträger bestehen:** *Nein*

        Wenn diese Option auf *Ja* festgelegt ist, wird die Cluster-ID nach dem Einlagern zu einem übergeordneten Ladungsträger, und alle Elemente auf der Cluster-ID werden mit diesem übergeordneten Ladungsträger verknüpft.

1. Auf der Inforegister-Registerkarte **Clustereinlagerung** können Sie Kriterien für die Einlagerungssortierung definieren. Wählen Sie **Neu** in der Symbolleiste, um eine Zeile hinzuzufügen, und legen Sie dann die folgenden Werte fest:

    - **Sequenznummer:** Akzeptieren Sie den Standardwert.
    - **Feldname:** *WMSLocationId*

        Dieses Feld definiert das Feld, das diese Zeile als Sortierkriterium verwenden soll.

    - **Sortierung:** *Aufsteigend*

        Dieses Feld legt fest, ob die Sortierung in aufsteigender oder absteigender Reihenfolge erfolgen soll.

1. Wählen Sie auf dem Inforegister **Cluster-Arbeitsvorlage** die Option **Neu** in der Symbolleiste, um eine Zeile hinzuzufügen, und legen Sie dann die folgenden Werte fest:

    - **Arbeitsauftragstyp:** *Bestellungen*
    - **Arbeitsvorlage:** *61 PO Direct*

1. Wählen Sie im Aktivitätsbereich **Speichern** und wählen Sie dann **Abfrage bearbeiten**.
1. Wählen Sie im Dialogfeld **Clustereinlagerung** auf der Registerkarte **Bereich** die Option **Hinzufügen**, um der Abfrage eine zweite Zeile hinzuzufügen. Aktualisieren Sie dann die Zeilen der Abfrage wie in der folgenden Tabelle gezeigt.

    | Tabelle | Abgeleitete Tabelle | Feld | Kriterien |
    |---|---|---|---|
    | Arbeit | Arbeit | Lagerort | *61* |
    | Arbeit | Arbeit | Arbeitskennung | Lassen Sie dieses Feld leer. |

1. Wählen Sie **OK** aus, um die Abfrage zu speichern und das Dialogfeld zu schließen.
1. Wählen Sie im Aktivitätsbereich **Speichern**, und schließen Sie die Seite.

> [!IMPORTANT]
> Felder im Clusterprofil, die abgeblendet erscheinen, wenn **Cluster-ID generieren** auf *Ja* festgelegt ist, sind nicht verfügbar und werden nicht berücksichtigt, wenn diese Funktion verwendet wird.

### <a name="mobile-device-menu-items"></a>Menüelemente des mobilen Geräts

Für diese Funktion sind zwei neue Menüelemente für mobile Geräte verfügbar. Der Menüpunkt **Cluster empfangen und sortieren** wird verwendet, um den empfangenen Bestand beim Empfang in ein Cluster für die Einlagerung zu sortieren. Der Menüpunkt **Clustereinlagerung** dient zum Einlagern des Clusters, nachdem er zugewiesen worden ist.

#### <a name="receive-and-sort-cluster"></a>Cluster empfangen und sortieren

Erstellen Sie einen neuen Menüpunkt für mobile Geräte, um Bestände zu empfangen und in einen Cluster zu sortieren. Dieses Element erstellt einen Eingang nach dem Empfang von Bestand, was bedeutet, dass der Menüpunkt Empfangen für das Einlagern von Clustern verwendet wird.

> [!NOTE]
> Der Menüpunkt **Cluster empfangen und sortieren** kann mit den folgenden Empfangsmenüpunkten verwendet werden:
>
> - Bestellposition – Empfang
> - Bestellungsartikel – Empfang
> - Artikelempfang aus Ladung

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie in der Ansicht **Kopfzeile** die folgenden Werte fest:

    - **Name des Menüelements:** *Cluster empfangen und sortieren*
    - **Titel:** *Clusters empfangen und sortieren*
    - **Modus:** *Arbeit*
    - **Vorhandene Arbeit verwenden:** *Nein*

1. Legen Sie im Inforegister **Allgemein** die folgenden Werte fest:

    - **Arbeitserstellungsprozess:** *Empfang von Elementen der Einkaufsbestellung*
    - **Kennzeichen generieren:** *Ja*
    - **Clustereinlagerung zuweisen:** *Ja*

        > [!NOTE]
        > Die Option **Clustereinlagerung zuweisen** ist nur für die einstufige Aktivität *Arbeitserstellungsprozess* für den Empfang verfügbar.

    Übernehmen Sie für alle verbleibenden Felder die Standardwerte.

1. Wählen Sie im Aktionsbereich **Speichern** aus.

#### <a name="cluster-putaway"></a>Clustereinlagerung

Erstellen Sie ein neues Menüelement für das Einlagern des Clusters, nachdem es zugewiesen wurde.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie in der Ansicht **Kopfzeile** die folgenden Werte fest:

    - **Name des Menüelements:** *Clustereinlagerung*
    - **Titel:** *Clustereinlagerung*
    - **Modus:** *Arbeit*
    - **Vorhandene Arbeit verwenden:** *Ja*

1. Legen Sie im Inforegister **Allgemein** das Feld **Gerichtet durch** auf *Clustereinlagerung* fest. Übernehmen Sie für alle verbleibenden Felder die Standardwerte.
1. Legen Sie auf dem Inforegister **Arbeitsklassen** die gültige Arbeitsklasse für diesen Menüpunkt für mobile Geräte fest:

    - **Arbeitsklassen-ID:** *Kauf*
    - **Arbeitsauftragstyp:** *Bestellungen*

1. Wählen Sie im Aktionsbereich **Speichern** aus.

### <a name="mobile-device-menu"></a>Menü für mobiles Gerät

Fügen Sie die soeben erstellten Menüelemente in das Eingangsmenü der mobilen App ein.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menü für mobiles Gerät**.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Wählen Sie in der Menüliste **Eingang**.
1. Suchen Sie in der Liste **Verfügbare Menüs und Menüpunkte** den Eintrag **Cluster empfangen und sortieren** und wählen Sie ihn aus.
1. Wählen Sie die rechte Pfeil-Schaltfläche, um das ausgewählte Element in die Liste **Menüstruktur** zu verschieben.
1. Verwenden Sie die Pfeil-nach-oben- oder Pfeil-nach-unten-Schaltfläche, um das Element an die gewünschte Position im Menü zu verschieben.
1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Wiederholen Sie die Schritte 4 bis 7, um die restlichen Menüelemente hinzuzufügen:

    - Cluster zuweisen
    - Clustereinlagerung

## <a name="example-scenario"></a>Beispielszenario

Dieses Szenario simuliert die Clustereinlagerungs-Verarbeitung.

### <a name="create-a-purchase-order"></a>Eine Bestellung erstellen

1. Wechseln Sie zu **Kreditorenkonten \> Bestellungen \> Alle Bestellungen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie im Dialogfeld **Bestellung erstellen** die folgenden Werte fest:

    - **Kreditorenkonto:** *1001*
    - **Lagerort:** *61*

1. Wählen Sie **OK**.

    Die Seite **Alle Einkaufsbestellungen** wird angezeigt.

1. Fügen Sie auf der Seite **Alle Bestellungen** auf dem Inforegister **Bestellzeilen** mit der Schaltfläche **Zeile hinzufügen** die folgenden Zeilen hinzu:

    - Einkaufsbestellung Zeile 1:

        - **Artikelnummer** *A001*
        - **Menge** *10*

    - Einkaufsbestellung Zeile 2:

        - **Artikelnummer:** *A0002*
        - **Menge** *20*

    - Einkaufsbestellung Zeile 3:

        - **Artikelnummer:** *M9215*
        - **Menge** *30*

1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Notieren Sie sich die Bestellnummer.

### <a name="receive-inventory-and-put-it-away-from-the-mobile-device"></a>Bestand empfangen und auf dem mobilen Gerät einlagern

#### <a name="receive-and-sort-the-inventory-into-a-cluster"></a>Bestand empfangen und in ein Cluster einsortieren

1. Melden Sie sich bei der Warehouse Management Mobile App als Benutzer an, der auf den Lagerort *61* eingestellt ist.
1. Wählen Sie im Hauptmenü **Eingang**.
1. Wählen Sie im Menü **Eingang** die Option **Cluster empfangen und sortieren**.
1. Geben Sie im Feld **Ponum** die Nummer der Einkaufsbestellung ein.
1. Wählen Sie **OK** (die Schaltfläche mit dem Häkchen).
1. Wählen Sie das Feld **Element**, geben Sie die Positionsnummer *A0001* ein und wählen Sie dann **OK**.
1. Wählen Sie das Feld **Anzahl**, geben Sie *10* mit Hilfe des Nummernblocks ein und wählen Sie dann die Schaltfläche mit dem Häkchen.
1. Auf der Aufgabenseite **Anzahl** wählen Sie **OK** (die Schaltfläche mit dem Häkchen), um die eingegebene Menge zu bestätigen.
1. Wählen Sie auf der Aufgabenseite **Element** **OK**, um zu bestätigen, dass das Element *A0001* eingegeben wurde.
1. Wählen Sie das Feld **Cluster-ID** und geben Sie einen Wert ein, um eine ID für den Cluster zu vergeben, den Sie erstellen.

    Die ID, die Sie hier eingeben, wird verwendet, wenn die beiden restlichen Elemente der Einkaufsbestellung eingehen.

1. Wählen Sie **OK**.

    Die Aufgabenseite **Ponum** erscheint und zeigt die Meldung „Arbeit abgeschlossen“.

    Element *A0001* ist nun auf dem Lagerplatz *RECV* eingegangen und der Cluster-ID zugeordnet, die Sie in Schritt 10 eingegeben haben.

1. Wiederholen Sie die Schritte 4 bis 11, um die restlichen zwei Elemente aus der Einkaufsbestellung zu empfangen und der Cluster-ID zuzuordnen:

    - Eine Menge von *20* für Element *A0002*
    - Eine Menge von *30* für das Element *M9215*

#### <a name="close-the-cluster"></a>Schließen des Clusters

Bevor die Elemente des Clusters eingelagert werden können, muss der Cluster geschlossen werden.

1. Gehen Sie im Supply Chain Management auf **Lagerortverwaltung \> Arbeit \> Ausgang \> Arbeits-Cluster**.
1. Suchen Sie auf der Seite **Arbeitscluster** im Abschnitt **Arbeitscluster** im Feld **Cluster-ID** nach der Cluster-ID, die Sie zuvor eingegeben haben.
1. Wenn der Cluster nicht angezeigt wird, wurde er möglicherweise bereits geschlossen. Um festzustellen, ob der Cluster geschlossen wurde, aktivieren Sie das Kontrollkästchen **Geschlossene Arbeiten anzeigen** und suchen Sie nach der Cluster-ID, die Sie zuvor eingegeben haben. Folgen Sie dann diesen Schritten:

    - Wenn der Cluster geschlossen wurde, überspringen Sie die restlichen Schritte dieser Prozedur und fahren Sie mit der nächsten Prozedur fort, [Den Cluster einlagern](#put-the-cluster-away).
    - Wenn der Cluster nicht geschlossen wurde, folgen Sie den verbleibenden Schritten dieser Prozedur, um den Cluster manuell zu schließen. Fahren Sie dann mit der nächsten Prozedur fort.

1. Wählen Sie im Bereich **Arbeitscluster** die Cluster-ID, die Sie zuvor eingegeben haben.
1. Wählen Sie im Aktivitätsbereich **Cluster schließen**.

    Nachdem der Cluster geschlossen wurde, wird er nicht mehr im Bereich **Arbeitscluster** angezeigt (es sei denn, das Kontrollkästchen **Geschlossene Arbeit anzeigen** ist aktiviert).

#### <a name="put-the-cluster-away"></a>Einlagern des Clusters

1. Melden Sie sich bei der Warehouse Management Mobile App als Benutzer an, der auf den Lagerort *61* eingestellt ist.
1. Wählen Sie im Hauptmenü **Eingang**.
1. Wählen Sie im Menü **Eingang** die Option **Clustereinlagerung**.
1. Wählen Sie **Cluster-ID**, und geben Sie die Cluster-ID ein, die Sie zuvor für den geschlossenen Cluster eingegeben haben.
1. Wählen Sie **OK**.

    Die Seite **Clustereinlagerung: Entnehmen** erscheint. Sie zeigt die Cluster-ID, den Lagerplatz, die Elemente (es wird der Wert *Mehrfach* angezeigt) und die Gesamtmenge im Cluster, die entnommen werden muss.

1. Wählen Sie **OK**.

    Die Seite **Clustereinlagerung: Einlagern** erscheint. Die Anweisungen **Einlagern** identifizieren die Cluster-ID, den Lagerplatz, die Elemente, die Gesamtmenge und die Ladungsträger-IDs für die Elemente, die auf dem Cluster eingegangen sind.

    Sie haben die Standardoptionen, um diesen Schritt zu überschreiben oder zu übergehen.

    ![Clustereinlagerung: Seite einlagern.](media/Cluster_putaway-Put.png "Clustereinlagerung: Seite einlagern")

1. Wählen Sie **OK**, um die Clustereinlagerung zu bestätigen.

    Es wird eine Meldung „Cluster abgeschlossen“ angezeigt.

## <a name="notes-and-tips"></a>Hinweise und Tipps

In Fällen, in denen die Cluster-ID zum übergeordneten Ladungsträger für eine verschachtelte Palette wird, wird die Einlagerungsposition automatisch angegeben, wenn die Cluster-ID gescannt wird. Es muss kein weiteres Ladungsträger-Kennzeichen gescannt werden, auch wenn die Kennzeichenerstellung auf manuell festgelegt ist.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]