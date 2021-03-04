---
title: Put-to-Wall - Put-to-Store
description: Dieses Thema enthält Informationen zu den Funktionen „Put-to-Wall - Put-to-Store“. Mit dieser Funktion können Sie Szenarien behandeln, in denen Sie ein Produkt basierend auf konfigurierbaren Kriterien in einem Prepack-Staging-Bereich konsolidieren müssen. Dies verkürzt die Kommissionierzeit, da es die Kommissionierung auf ein einzelnes Zielkennzeichen ermöglicht und mehr Put-Positionen als die Cluster-Kommissionierung verwenden kann.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationType, WHSLocationProfile, WHSLocation, WHSPackProfile, WHSWaveStepCode, WHSOutboundSortTemplate, WHSPostMethod, WHSWaveTemplateTable, WHSLocDirTable, WHSWorkClass, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 12501b90e4b31ec11e3c59784ace9fd9a8b7d934
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4429038"
---
# <a name="put-to-wall---put-to-store"></a>Put-to-Wall - Put-to-Store

[!include [banner](../includes/banner.md)]

Mit der Funktion *Put-to-Wall - Put-to-Store* können Sie Szenarien behandeln, in denen Sie ein Produkt basierend auf konfigurierbaren Kriterien in einem Prepack-Staging-Bereich konsolidieren müssen. Da diese Funktion die Kommissionierung auf einem einzelnen Zielkennzeichen ermöglicht und mehr Put-Positionen als die Cluster-Kommissionierung verwenden kann, profitieren Unternehmen, die an Geschäfte liefern oder kleine Artikel bearbeiten, von einer kürzeren Kommissionierzeit.

Der Workflow für diese Funktionalität leitet das ausgewählte Produkt an einen Sortierort zur Verteilung in verschiedene Arten von Containern. Im Allgemeinen enthält jeder Sortierort mehrere Sortierpositionen. Jede Sortierposition wird gemäß den vom Geschäftsprozess festgelegten Kriterien zugewiesen. Typische Kriterien sind das endgültige Ziel, die Lieferung oder die Auslastung. Nachdem ein Produkt angekommen ist, wird es basierend auf der Menge, die der Bestellung, dem Bestimmungsort, der Sendung oder der Ladung zugeordnet ist, an jede Sortierposition verteilt. Wenn ein Container voll oder vollständig ist, wird er je nach Geschäftsprozess zur weiteren Bearbeitung an einen Bereitstellungsort oder einen Versandort verschoben.

Auf diese Warehousing-Funktion wird auch mit anderen Namen verwiesen, z. B. Aufleuchten und Öffnen.

## <a name="turn-on-the-outbound-sorting-feature"></a>Aktivieren der Funktion „Ausgangssortierung“

Bevor Sie die Funktion *Put-to-Wall - Put-to-Store* verwenden können, muss die *Ausgangssortierung* in Ihrem System aktiviert sein. Administratoren können mit der Einstellung [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und ggf. aktivieren. Dort wird die Funktion folgendermaßen aufgelistet:

- **Module:** *Lagerortverwaltung*
- **Funktionsname:** *Ausgangssortierung*

Die Funktion *Ausgangssortierung* kann in Verbindung mit der Funktion *Organisationsweiter Wellenschrittcode* verwendet werden, wenn sie eingeschaltet ist. Sie müssen diese Funktion auch aktivieren, wenn Sie vordefinierte Codes verwenden, die in Wellenschrittcodes eingerichtet sind. Im Arbeitsbereich **Funktionsverwaltung** ist diese Funktion wie folgt aufgeführt:

- **Module:** *Lagerortverwaltung*
- **Funktionsname:** *Organisationsweiter Wellenschrittcode*

## <a name="setup"></a>Einstellung

Für diese Demo werden Standard-Contoso-Daten und Lagerotz *62* verwendet. Einige Ergänzungen, die später erwähnt werden, werden ebenfalls verwendet.

### <a name="location-type"></a>Lagerplatztyp

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerort \> Lagerplatztypen**.
1. Wählen Sie im Aktivitätsbereich die Option **Neu** aus, um einen Lagerplatztyp zum Sortieren zu erstellen.
1. Legen Sie die folgenden Werte fest:

    - **Lagerplatztyp:** *SORT*
    - **Beschreibung:** *Sortieren*

1. Wählen Sie **Speichern** aus.

### <a name="warehouse-management-parameters"></a>Parameter für Lagerortverwaltung

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerortverwaltungsparameter**.
1. Geben Sie im Registerkarte **Allgemein** im Inforegister **Lagerplatztypen** das Feld **Lagerplatztyp für Sortierung** *SORT* ein.
1. Wählen Sie **Speichern** aus.

### <a name="location-profile"></a>Lagerortprofil

1. Wechseln Sie zu **Lagerortverwaltung \> Einrichtung \> Lagerort \> Lagerplatzprofile**.
1. Wählen Sie im Aktivitätsbereich die Option **Neu** aus, um ein Lagerplatzprofil für den Sortierort zu erstellen.
1. Legen Sie im Header die folgenden Werte fest:

    - **Lagerortprofilkennung:** *Sortieren*
    - **Name:** *Sortieren*

1. Legen Sie im Inforegister **Allgemein** die folgenden Werte fest:

    - **Lagerplatzformat:** *PACK*
    - **Lagerplatztyp:** *SORT*
    - **Kennzeichenverfolgung verwenden:** *Ja*
    - **Gemischte Artikel zulassen:** *Ja*
    - **Gemischte Bestandstatus zulassen:** *Ja*

1. Wählen Sie **Speichern** aus.

### <a name="locations"></a>Lagerplätze

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerort \> Lagerplätze**.
1. Löschen Sie das Kontrollkästchen **Prüfziffern für den Lagerplatz erstellen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, und legen Sie dann die folgenden Werte fest:

    - **Lagerort:** *62*
    - **Lagerplatz:** *Sortieren*
    - **Lagerortprofilkennung:** *Sortieren*

1. Wählen Sie **Speichern** aus.

### <a name="packing-profiles"></a>Verpackungsprofile

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Verpackung \> Verpackungsprofile**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, und legen Sie dann die folgenden Werte fest:

    - **Verpackungsprofilkennung:** *Sortieren*
    - **Beschreibung:** *Sortieren*
    - **Containerverpackungsrichtlinien:** Lassen Sie dieses Feld leer.
    - **Containerkennungsmodus:** *Auto*
    - **Containertyp:** *PALETTE 48X48*
    - **Container beim Schließen des Containers automatisch erstellen:** Lassen Sie dieses Feld leer.

1. Wählen Sie **Speichern** aus.

### <a name="wave-step-codes"></a>Wellenschrittcodes

Wenn Sie die Funktion *Organisationsweiter Wellenschrittcode* eingeschaltet haben, richten Sie den folgenden Code ein.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenschrittcodes**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, und legen Sie dann die folgenden Werte fest:

    - **Wellenschrittcode:** *Sortieren*
    - **Wellenschrittbeschreibung:** *Sortieren*
    - **Wellenschritttyp:** *Vorlage sortieren*

1. Wählen Sie **Speichern** aus.

### <a name="outbound-sorting-template"></a>Vorlage für ausgehende Sortierung

Die Sortiervorlage steuert, ob Sortierpositionen erstellt werden, welche Kriterien verwendet werden und andere Attribute des Sortierprozesses.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Verpackung \> Vorlage für die Ausgangssortierung**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Sortiervorlage zu erstellen.
1. Legen Sie in der Kopfzeile der neuen Vorlage die folgenden Werte fest:

    - **ID der Vorlage für die Ausgangssortierung:** *Wellensortierung*
    - **Beschreibung:** *Wellensortierung*
    - **Sortiervorlagentyp:** *Wellenbedarf*

        Dieses Feld definiert den Prozess, für den die Sortiervorlage verwendet wird. Folgende Werte sind verfügbar:

        - **Wellenbedarf** – Die Sortiervorlage wird für den Prozess *Put-to-Wall* verwendet. Dieser Vorlagentyp wird zur Umgehung der Verpackungsstation und Verarbeitung des Bestands direkt aus der Welle verwendet. Sie können diesen Typ nur verwenden, wenn die Wellenprozessmethode **Sortieren** in der Wellenvorlage enthalten ist.
        - **Container** – Die Sortiervorlage wird für den Prozess *Palettenerstellung nach dem Verpacken* verwendet. Dieser Vorlagentyp wird zur Verarbeitung von Containern verwendet, die an dieser Packstation geschlossen werden und auf Paletten sortiert werden müssen.

    - **Lagerort:** *62*
    - **Lagerplatz:** *Sortieren*

1. Legen Sie im Inforegister **Allgemein** die folgenden Werte fest:

    - **Sortierbestätigung:** *Positionsscan*

        Dieses Feld definiert die Überprüfung, die während des Sortierens erforderlich ist. Folgende Werte sind verfügbar:

        - Keiner
        - Ladungsträgerscan
        - Positionsscan

    - **Arbeit bei Schließen der Position erstellen:** *Ja*

        Wenn diese Option auf *Ja* eingestellt ist, wird Arbeit erstellt, wenn die Position geschlossen wird, um den Bestand zum endgültigen Versandlagerplatz umzulagern. Ist sie auf *Nein* festgelegt, wird Lagerbestand sofort für den Auftrag entnommen, wenn die Position geschlossen wird.

    - **Positionszuweisung:** *Manuell*

        Dieses Feld definiert die Art der Positionszuweisung. Folgende Werte sind verfügbar:

        - **Manuell** – Der Benutzer muss immer angeben, in welche Position der Bestand sortiert werden soll.
        - **Automatisch** – Das System automatisch den Bestand an eine Position, sofern möglich, basierend auf den Sortiervorlagenunterbrechungen.

    - **Sortierpositionskriterien zuweisen:** *Nur die leere Position verwenden*

        Dieses Feld steuert, ob der Bestand, der auf Sortierungspositionen bereits vorhanden ist, berücksichtigt wird, wenn eine Position für den Bedarf zugewiesen wird. Folgende Werte sind verfügbar:

        - **Nur die leere Position verwenden** – Positionen, denen bereits Bestand zugeordnet ist, werden berücksichtigt
        - **Position als leer annehmen** – Jeder Bestand, der sich bereits auf der Position befindet, wird bei der Zuordnung nicht berücksichtigt. Alle verfügbaren Positionen werden verwendet.

    - **Wellenschrittcode:** *Sortieren*

        Wenn die Funktion *Organisationsweiter Wellenschrittcode* eingeschaltet ist, muss der Wellenschrittcode *Sortieren* auch in Wellenschrittcodes eingerichtet werden.

    - **Sortierposition automatisch schließen:** *Ja*

        Wenn diese Option auf *Ja* eingestellt ist, wird die Sortierungsposition automatisch geschlossen, wenn alle Arbeiten in der Position abgeschlossen sind.

    - **Anzahl der Sortierpositionen:** *3*

        Dieses Feld definiert die maximale Anzahl von Sortierpositionen, die das System erstellen wird.

    - **Sortierpositionspräfix:** *SP-*

        Dieses Feld definiert das Präfix, das das System vor der Positionsnummer zuweist.

    - **Sortierposition automatisch packen:** *Ja*

        Wenn diese Option auf *Ja* eingestellt ist, wird der Bestand für die Sortierungsposition in einen Container verpackt, wenn die Position geschlossen ist.

    - **Verpackungsprofilkennung:** *Sortieren*

        Dieses Feld definiert das Verpackungsprofil, das verwendet wird, wenn die Sortierungsposition in einen Container verpackt wird.

1. Wählen Sie im Aktivitätsbereich **Abfrage bearbeiten** aus, um die Kriterien anzugeben, die für diese Sortiervorlage verwendet werden.
1. Wählen Sie im Abfragedialogfeld auf der Registerkarte **Sortieren** die Option **Neu** aus, um eine Position hinzuzufügen und legen Sie die folgenden Werte fest:

    - **Tabelle:** *Ladungsdetails*
    - **Abgeleitete Tabelle:** *Ladungsdetails*
    - **Feld:** *Lieferungs-ID*
    - **Suchrichtigung:** *Aufsteigend*

1. Wählen Sie **OK**.
1. Möglicherweise erhalten Sie die folgende Meldung: „Gruppierung wird zurückgesetzt, fortfahren?“ Wählen Sie **Ja** aus.

    Die Schaltfläche **Vorlagenunterbrechungen für Ausgangssortierung** im Aktivitätsbereich wird verfügbar.

1. Wählen Sie im Aktivitätsbereich **Vorlagenunterbrechungen für Ausgangssortierung**.
1. Aktivieren Sie das Kontrollkästchen **Gruppieren nach Feld**, um nach Lieferungs-ID zu gruppieren.

    Diese Einstellung erstellt eine Sortierposition pro Sendung, die ein Container in der Welle ist.

1. Wählen Sie **OK**.

### <a name="wave-process-methods"></a>Wellenverarbeitungsmethoden

1. Wechseln Sie zu **Lagerortverwaltung \> Setup \> Wellen \> Wellenverarbeitungsmethoden**.
1. Wählen Sie im Aktivitätsbereich **Methoden erneut generieren** aus.

    Die Methode **Sortieren** wird der Liste der verfügbaren Methoden hinzugefügt, und der Wellenvorlagentyp *Lieferung* ist dafür ausgewählt.

### <a name="wave-templates"></a>Wellenvorlagen

Bearbeiten Sie die Wellenvorlage, die für die Sortierung der Wellenanforderungen verwendet wird.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenvorlagen**.
1. Wählen Sie im Feld **Wellenvorlagentyp** *Versand* aus.
1. Wählen Sie die vorhandene Vorlage **Standard-62-Lieferung** aus.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Nehmen Sie im Inforegister **Allgemein** die folgenden Änderungen vor:

    - Legen Sie die Option **Welle bei Freigabe für Lagerort verarbeiten** auf *Nein* fest.
    - Legen Sie die Option **Offenen Wellen zuweisen** auf *Ja* fest.

1. Richten Sie im Inforegister **Methoden** die Methode **Sortieren** ein:

    1. Wählen Sie im Raster **Verbleibende Methoden** **Sortieren** aus.
    2. Wählen Sie die Schaltfläche mit dem Pfeil nach rechts aus, um **Sortieren** in das Raster **Ausgewählte Methoden** zu verschieben.
    3. Wählen Sie im Raster **Ausgewählte Methoden** **Sortieren** aus.
    4. Legen Sie das Feld **Wellenschrittcode** auf *Sortieren* fest.

1. Wählen Sie **Speichern** aus.

### <a name="mobile-device-menu-items"></a>Menüelemente des mobilen Geräts

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie im Header die folgenden Werte fest:

    - **Menüelementname:** *Sortieren*
    - **Titel:** *Sortieren*
    - **Modus:** *Indirekt*
    - **Vorhandene Arbeit verwenden:** *Nein*

1. Legen Sie im Inforegister **Allgemein** die folgenden Werte fest:

    - **Aktivitätscode:** *Ausgangssortierung*
    - **Prozessleitfaden verwenden:** *Ja* (Standardwert)
    - **ID der Vorlage für die Ausgangssortierung:** *Wellensortierung*

1. Wählen Sie **Speichern** aus.

### <a name="mobile-device-menu"></a>Menü für mobiles Gerät

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menü für mobiles Gerät**.
1. Wählen Sie in der Liste der Menüs **Ausgehend** aus.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Suchen und wählen Sie inm Raster **Verfügbare Menüs und Menüpunkte** den Menüpunkt **Sortieren** aus, den Sie gerade erstellt haben.
1. Wählen Sie die rechte Pfeiltaste, um **Sortieren** zum Raster **Menüstruktur** zu verschieben. Auf diese Weise fügen Sie dem ausgewählten Menü den Menüpunkt **Ausgehend** hinzu.
1. Wählen Sie **Speichern** aus.

### <a name="location-directives"></a>Lagerplatzrichtlinien

Sie müssen Standortanweisungen erstellen, um die Arbeit zu steuern, die nach Abschluss der Sortierung erstellt wird.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerplatzrichtlinien**.
1. Wählen Sie im Feld **Arbeitsauftragsart** *Sortierte Bestandsentnahme*.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie im Header die folgenden Werte fest:

    - **Sequenz:** *1*
    - **Name:** *Zu Frachttür bringen*

1. Legen Sie im Inforegister **Lagerplatzrichtlinien** die folgenden Werte fest:

    - **Arbeitstyp:** *Einlagern*
    - **Standort:** *6*
    - **Lagerort:** *62*
    - **Richtliniencode:** Lassen Sie dieses Feld leer.
    - **Mehrfach-SKU:** *Nein*

1. Wählen Sie **Speichern** aus, um das Inforegister **Positionen** verfügbar zu machen.
1. Legen Sie im Inforegister **Positionen** die Option **Neu** aus und stellen Sie dann die folgenden Werte ein. Übernehmen Sie für alle anderen Felder die Standardwerte.

    - **Sequenznummer:** *1*
    - **Von Menge:** *0*
    - **Bis Menge:** *1000000*

1. Wählen Sie **Speichern** aus, um das Inforegister **Lagerplatzrichtlinienaktivitäten** verfügbar zu machen.
1. Legen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** die Option **Neu** aus und stellen Sie dann die folgenden Werte ein. Übernehmen Sie für alle anderen Felder die Standardwerte.

    - **Sequenznummer:** *1*
    - **Name:** *Ladebereichstor*

1. Wählen Sie **Speichern** aus, um die Schaltfläche **Abfrage bearbeiten** im Inforegister **Lagerplatzrichtlinienaktivitäten** verfügbar zu machen.
1. Wählen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** **Abfrage bearbeiten** aus.
1. Suchen Sie im Abfragedialogfeld auf der Registerkarte **Bereich** die Zeile, in der das Feld **Feld** auf *Lagerplatz* festgelegt ist. Legen Sie das Feld **Kriterien** für diese Zeile auf *Baydoor* fest.
1. Wählen Sie **OK**, um die Bearbeitung zu bestätigen.

### <a name="work-classes"></a>Arbeitsklassen

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsklassen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie im Header die folgenden Werte fest:

    - **Arbeitsklassen-ID:** *Sortieren*
    - **Beschreibung:** *Sortieren*
    - **Arbeitsauftragstyp:** *Sortierte Bestandsentnahme*

1. Wählen Sie **Speichern** aus.

### <a name="work-templates"></a>Arbeitsvorlagen

1. Wechseln Sie zu **Lagerortverwaltung \> Arbeit \> Arbeitsvorlagen**.
1. Wählen Sie im Feld **Arbeitsauftragsart** *Arbeitsaufträge* aus.
1. Wählen Sie im Raster die Arbeitsvorlage **62 entnehmen für Paket** aus.
1. Wählen Sie im Aktivitätsbereich **Arbeitskopfzeilenumbrüche** aus.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Löschen Sie in der Position, in der das Feld **Feldname** auf *Lieferungs-ID* gesetzt ist, das Kontrollkästchen **Nach diesem Feld gruppieren**.
1. Wählen Sie **Speichern** und schließen Sie dann das Dialogfeld **Arbeitskopfzeilenumbrüche**.
1. Wählen Sie im Feld **Arbeitsauftragsart** *Sortierte Bestandsentnahme*.
1. Wählen Sie **Neu** aus, um eine Arbeitsvorlage zu erstellen.
1. Legen Sie im Abschnitt **Übersicht** die folgenden Werte fest. Übernehmen Sie für alle anderen Felder die Standardwerte.

    - **Arbeitsvorlage:** *Sortierte Kommissionierung*
    - **Arbeitsvorlagenbeschreibung:** *Sortierte Kommissionierung*

1. Wählen Sie **Speichern** aus, um den Abschnitt **Arbeitsvorlagendetails** verfügbar zu machen.
1. Im Abschnitt **Arbeitsvorlagendetails** erstellen Sie zwei Zeilen. Wählen Sie **Neu** aus, und legen Sie dann die folgenden Werte für Position 1 fest:

    - **Arbeitstyp:** *Entnahme*
    - **Obligatorisch:** Ausgewählt (= *Ja*)
    - **Arbeitsklassen-ID:** *Sortieren*

1. Wählen Sie erneut **Neu** aus, und legen Sie dann die folgenden Werte für Position 2 fest:

    - **Arbeitstyp:** *Einlagern*
    - **Obligatorisch:** Ausgewählt (= *Ja*)
    - **Arbeitsklassen-ID:** *Sortieren*

1. Wählen Sie **Speichern** aus.

## <a name="example-scenario"></a>Beispielszenario

Dieses Szenario simuliert eine Situation, in der das Lager kleine Artikel an Standorten lagert und diese vor dem Versand in Kartons verpacken muss und in denen die Funktionalität der Packstation nicht wirklich geeignet ist. Mitarbeiter kommissionieren gleichzeitig Bestellungen für mehrere Kunden und unterschiedliche Adressen, um die Kommissioniergeschwindigkeit zu erhöhen. Nach Abschluss der Kommissionierung erreichen die Mitarbeiter den Sortierort, an dem die kommissionierten Artikel anhand der erforderlichen Kriterien in die richtige Box sortiert werden können. In diesem Beispiel wird die Lieferungs-ID verwendet, um das richtige Feld zu bestimmen, da jede Lieferung eine andere Adresse hat. Nachdem alle Artikel aus der Ladung verpackt und nach Versand sortiert wurden, werden die Kartons in den Bereitstellungsbereich gebracht und schließlich auf einen LKW verladen.

Stellen Sie vor dem Starten des Szenarios sicher, dass alle Standard-Warehouse-Funktionen für Ihren Lagerort korrekt eingerichtet sind. Standard-Contoso-Lagerort *62* wird zu diesem Zweck verwendet. Die Standardkonfigurationen wurden außer den in den Einstellungen beschriebenen nicht geändert.

### <a name="create-demand"></a>Bedarf erstellen

Bevor die Funktionalität demonstriert werden kann, müssen Sie eine Nachfrage erstellen. In diesem Szenario erstellen Sie drei Kundenaufträge für drei verschiedene Kunden, um verschiedene Lieferadressen zu simulieren. Auf diese Weise erstellen Sie drei separate Sendungen.

Bevor Sie Aufträge und Lieferungen erstellen, müssen Sie sicherstellen, dass die Entnahmeorte über genügend Bestand für alle Artikel in den Aufträgen verfügen. Überprüfen Sie die Einstellungen der Standortrichtlinie, um die Kommissionierorte zu bestätigen, die für die Kundenauftragskommissionierung verwendet werden. Wenn Sie den Lagerbestand anpassen müssen, können Sie manuelle Bewegungen erstellen, Wiederbeschaffung verwenden oder einen anderen Flow verwenden. Reservieren Sie dann den Bestand.

1. Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
1. Wählen Sie **Neu** aus, um einen Auftrag für Auftrag 1 zu erstellen.
1. Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:

    - **Kunde:** *US-001*
    - **Lagerort:** *62*

1. Wählen Sie **OK**.
1. Im Inforegister **Auftragspositionen** wird eine neue Position hinzugefügt. Legen Sie die folgenden Werte fest:

    - **Artikelnummer** *A001*
    - **Menge** *5*

1. Wählen Sie **Position hinzufügen** aus, um eine zweite Position hinzuzufügen, und legen Sie die folgenden Werte fest:

    - **Artikelnummer:** *A0002*
    - **Menge** *10*

1. Wiederholen Sie die folgenden Schritte für jede Verkaufsposition in der Bestellung, um Bestand dafür zu reservieren:

    1. Wählen Sie im Inforegister **Auftragspositionen** im Menü **Bestand** die Option **Reservierung** aus.
    1. Wählen Sie auf der Seite **Reservierung** die Option **Los reservieren** aus, und schließen Sie dann die Seite.
    1. Wählen Sie **Speichern** aus.

1. Wählen Sie **Neu** aus, um einen Auftrag für Auftrag 2 zu erstellen.
1. Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:

    - **Kunde:** *US-004*
    - **Lagerort:** *62*

1. Wählen Sie **OK**.
1. Im Inforegister **Auftragspositionen** wird eine neue Position hinzugefügt. Legen Sie die folgenden Werte fest:

    - **Artikelnummer** *A001*
    - **Menge** *7*

1. Wählen Sie **Position hinzufügen** aus, um eine zweite Position hinzuzufügen, und legen Sie die folgenden Werte fest:

    - **Artikelnummer:** *A0002*
    - **Menge** *3*

1. Wiederholen Sie die folgenden Schritte für jede Verkaufsposition in der Bestellung, um Bestand dafür zu reservieren:

    1. Wählen Sie im Inforegister **Auftragspositionen** im Menü **Bestand** die Option **Reservierung** aus.
    1. Wählen Sie auf der Seite **Reservierung** die Option **Los reservieren** aus, und schließen Sie dann die Seite.
    1. Wählen Sie **Speichern** aus.

1. Wählen Sie **Neu** aus, um einen Auftrag für Auftrag 3 zu erstellen.
1. Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:

    - **Kunde:** *US-007*
    - **Lagerort:** *62*

1. Wählen Sie **OK**.
1. Im Inforegister **Auftragspositionen** wird eine neue Position hinzugefügt. Legen Sie die folgenden Werte fest:

    - **Artikelnummer** *A001*
    - **Menge** *8*

1. Um Bestand für die Verkaufsposition zu reservieren, führen Sie diese Schritte aus.

    1. Wählen Sie im Inforegister **Auftragspositionen** im Menü **Bestand** die Option **Reservierung** aus.
    1. Wählen Sie auf der Seite **Reservierung** die Option **Los reservieren** aus, und schließen Sie dann die Seite.
    1. Wählen Sie **Speichern** aus.

Führen Sie die folgenden Schritte aus, um jeden Kundenauftrag an das Lager freizugeben. Es werden drei verschiedene Sendungen erstellt. Sie werden dann alle drei Sendungen zu einer neuen Welle hinzufügen.

1. Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
1. Wählen Sie im Raster den ersten Kundenauftrag aus, den Sie erstellt haben.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** auf **Lagerortfreigabe**.

    Sie erhalten eine Informationsnachricht mit der Wellen-ID und der Lieferungs-ID, die erstellt wurden.

1. Wiederholen Sie die vorherigen Schritte, um die Kundenaufträge 2 und 3 für das Lager freizugeben. Beachten Sie, dass die Informationsnachricht, die Sie erhalten, darauf hinweist, dass der Welle, die bei der Freigabe des Kundenauftrags 1 erstellt wurde, eine Sendung hinzugefügt wurde.
1. Wechseln Sie zu **Lagerortverwaltung \> Ausgehende Wellen \> Lieferungswellen \> Alle Wellen**.
1. Wählen Sie die Wellen-ID, die von der Freigabe des Auftrags erstellt wurde, um die Seite **Wellen** zu öffnen. Diese Seite zeigt die Wellendetails. Das Inforegister **Wellenpositionen** zeigt die Sendungen an, die erstellt wurden.

    Sie müssen jetzt Arbeit erstellen, um Artikel von den Kommissionierorten zum Sortierort zu bringen.

1. Klicken Sie im Aktivitätsbereich auf **Verarbeiten**.

    Während der Wellenverarbeitung verwendet die Sortiermethode die Sortiervorlage, um den Bestand den Sortierpositionen zuzuweisen. Nach Abschluss der Wellenverarbeitung erhalten Sie eine Informationsmeldung, die angibt, dass die Welle gebucht und Arbeit erstellt wurde.

1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Welle** in der Gruppe **Zugehörige Informationen** auf **Arbeit**, um die Arbeit anzuzeigen, die für diese Welle erstellt wurde. Notieren Sie die Arbeits-ID.
1. Gehen Sie zu **Lagerortverwaltung \> Verpackung und Containerisierung \> Zuweisungen von Ausgangssortierpositionen**.
1. In der linken Spalte können Sie die ausgehende Sortierposition anzeigen, die für jede Sendung erstellt wurde.
1. Im Inforegister **Sortierpositionskriterien** können Sie die Lieferungs-ID für diese Position anzeigen.

Es wurde eine Arbeits-ID erstellt, um Bestand von den Kommissionierorten zum Sortierort zu bringen. Um die Arbeit abzuschließen, benötigen Sie die Arbeits-ID, die während der Wellenverarbeitung erstellt wurde.

### <a name="sales-order-picking-to-the-sorting-location"></a>Kommissionierung von Kundenaufträgen zum Sortierort

1. Melden Sie sich bei der mobilen App als eine Arbeitskraft im Lagerort *62* an.
1. Auf dem Hauptmenü wählen Sie **Ausgehend**.
1. Auf dem Menü **Ausgehend** wählen Sie **Verkaufsauswahl**.
1. Wählen Sie das Feld **ID** aus, und geben Sie dann die Arbeits-ID aus der Wellenverarbeitung ein.
1. Bestätigen Sie Ihre Eingabe.

    Als Nächstes werden Sie aufgefordert, ein Zielkennzeichen (LP) einzugeben. Beachten Sie, dass Position 1 aus Kundenauftrag 1 ausgewählt und dem Zielkennzeichen hinzugefügt werden muss. Die Artikelnummer, Menge, Artikelbeschreibung und der Kommissionierort werden angezeigt.

1. Geben Sie in das Feld **Ziel-LP** eine Kennzeichennummer ein.

    Sie wählen alle Positionen, die aus der verarbeiteten Welle erstellt wurden, auf demselben Zielkennzeichen aus.

1. Bestätigen Sie Ihre Eingabe.

    Die mobile App präsentiert nun eine Reihe von **Entnehmen**-Seiten, die Sie auf den Kommissionierort sowie auf den Artikel und die Menge verweisen, die kommissioniert werden müssen. Nachdem der kommissionierte Artikel dem Kennzeichen hinzugefügt wurde, bestätigen Sie die Kommissionierarbeiten. Die letzte Seite ist die Arbeit, um die ausgewählten Artikel an den Sortierort zu bringen.

1. Bestätigen Sie die erste Entnahmearbeit.
1. Die nächste Entnahmearbeit wird angezeigt. Bestätigen Sie die Entnahme.
1. Bestätigen Sie dann die verbleibenden Kommissionierarbeiten.
1. Der letzte Schritt besteht darin, die Put-Arbeit abzuschließen. Bestätigen Sie die Einlagerung an den Sortierort.

    Sie erhalten die Nachricht „Arbeit abgeschlossen“.

1. Verlassen Sie **Verkaufsauswahl** auf der mobilen App.

### <a name="sortingput-to-wall"></a>Sortieren/Put-to-Wall

Nachdem der gesamte Bestand an den Sortierort gebracht wurde, muss es an der richtigen Sortierposition sortiert werden.

1. Melden Sie sich bei der mobilen App an.
1. Auf dem Hauptmenü wählen Sie **Ausgehend**.
1. Wählen Sie im Menü **Ausgehend** **Sortieren** aus, um die Artikel zu sortieren.
1. Geben Sie im Feld **LP/CON** das Zielkennzeichen der ausgewählten Kundenauftragsarbeit ein.
1. Bestätigen Sie Ihre Eingabe.
1. Geben Sie zuerst die zu sortierende Artikelnummer ein.
1. Das System bestimmt die erste Sortierposition, die angezeigt werden soll. Bestätigen Sie die Sortierposition.
1. Sie werden aufgefordert, der Sortierposition ein Kennzeichen zuzuweisen. Wählen Sie das Feld **LP** aus, geben Sie ein Kennzeichen ein und bestätigen Sie Ihre Eingabe.

    Da sich die Sortierposition auf die Lieferungs-ID bezieht, sortieren Sie die kommissionierten Artikel in ein Kennzeichen, das für die ausgehende Lieferung und den Kundenauftrag spezifisch ist.

    Auf der nächsten Seite werden die Artikel-ID, die Menge, die Sortierpositions-ID sowie die Kennzeichen-IDs „von“ (Kommissionierung) und „bis“ (Sortierung) angezeigt. Die Informationen auf dieser Seite weisen Sie an, den angegebenen Artikel und die angegebenen Mengen vom Kommissionierkennzeichen in das Sortierkennzeichen zu sortieren.

1. Bestätigen Sie die Sortierposition.
1. Sortieren Sie die Artikel an der ersten Sortierposition. Wenn Sie fertig sind, leitet Sie das System zur nächsten Sortierposition.
1. Wiederholen Sie diesen Vorgang für alle ausgewählten Positionen im Arbeitsauftrag. Sie sollten diesen Prozess auch verwenden, wenn mehrere Kommissionierzeilen dieselbe Artikelnummer haben.

    Wenn Sie diesen Vorgang für alle Artikel wiederholen, wertet das System die Kriterien des nächsten gescannten Artikel (Arbeitsposition) aus und bestimmt, an welche Sortierposition es verschoben werden soll. Sie werden automatisch angewiesen, den Artikel an die richtige Sortierposition zu bringen. Abhängig von der Bestätigungskonfiguration werden Sie auch angewiesen, diese Aktion durch Eingabe der Positionsnummer oder des Kennzeichens zu bestätigen.

    > [!NOTE]
    > Wenn die automatische Sortierung aktiviert ist, ist kein manuelles Überschreiben verfügbar.

1. Wenn Sie fertig sind, öffnen Sie in Microsoft Dynamics 365 Supply Chain Management die Seite **Ausgehende Sortierungspositionszuweisungen**, um den Status der Positionen zu überprüfen.

    - Wenn Positionen automatisch geschlossen werden, wählen Sie **Geschlossene anzeigen**, um die geschlossenen Positionen anzuzeigen.
    - Beachten Sie, dass Sortierpositionstransaktionen angezeigt werden. Der Artikel und die Menge, die über die Position verarbeitet wurden, werden angezeigt.

    Wenn Sie die ausgehende Sortiervorlage einrichten, legen Sie die Option **Sortierposition automatisch schließen** auf *Ja* fest. Daher wird die Position automatisch geschlossen, nachdem der letzte erwartete Bestand darauf gelegt wurde. Die Sortierpositionen sind im Status **Geschlossen** und Arbeit wurde erstellt, um den sortierten Bestand zum Lagerplatz *Frachttür* zu verschieben.

1. Schließen Sie die Kommissionierarbeiten für sortierten Bestand ab, um den Bestand an den Versandort zu verschieben. Wenn der Bestand fertig ist, bestätigen Sie es für die Lieferung.

> [!NOTE]
> Damit die sortierte Bestandsauswahl korrekt verarbeitet werden kann, sollte ein Menüelement für mobile Geräte mit einer Arbeitsklassen-ID, in der das Feld **Arbeitsauftragstyp** auf *Sortierte Bestandsentnahme* festgelegt ist, für den Bewegungs- und Ladevorgang verwendet werden.

### <a name="manually-close-a-position-optional"></a>Manuelles Schließen einer Position (optional)

Wenn Sortierpositionen manuell geschlossen werden sollen, muss die Option **Sortierposition automatisch schließen** für die Vorlage für die Ausgangssortierung auf *Nein* gesetzt sein und das Schließen muss erfolgen, bevor der Bestand in den Bereich der Frachttür gebracht werden kann. Positionen können auf verschiedene Arten geschlossen werden:

- Über die Warehouse-App:

    - Der Benutzer kann einen der Artikel scannen, die sich bereits an der Position befinden, und dann **Schließen** auswählen, um die Position zu schließen.
    - Wenn der Benutzer einen Container sortiert, der bereits sortiert wurde, wird eine Fehlermeldung angezeigt. Der Benutzer kann die Position jedoch weiterhin schließen.

- Über die Seite Microsoft Dynamics 365 Supply Chain Management **Ausgehende Sortierungspositionszuweisungen**:

    - Der Benutzer kann den ausgehenden Sortierpositionsdatensatz auswählen und dann im Aktionsbereich **Position schließen** auswählen.

## <a name="tips"></a>Tipps

- Artikel können nicht zwischen Positionen verschoben werden, nachdem sie einer zugewiesen wurden. Das System bewertet, wie viele von jedem Artikel an eine bestimmte Position gehen sollen.
- Die Sortiervorlage kann so konfiguriert werden, dass beim Schließen von Positionen automatisch Container erstellt werden. Dieser Ansatz erstellt eine Standard-Container-ID-Struktur, die auf dem angegebenen Verpackungsprofil basiert.

> [!IMPORTANT]
> Nachdem die Umlagerungsarbeit vom Sortierort aus erstellt wurde, dürfen Sie die Arbeit nicht abbrechen. Andernfalls werden die Position und die darin enthaltenen Container aus dem System gelöscht und stehen nicht zur weiteren Verarbeitung zur Verfügung. Der Bestand wird ebenfalls entfernt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]