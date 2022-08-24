---
title: Zuteilung von Zeitfenstern für Lagerort
description: Dieser Artikel enthält Informationen zur Zuteilung von Zeitfenstern für den Lagerort. Mit der Zuteilung von Zeitfenstern für den Lagerort können Sie die Nachfrage nach Artikeln und Maßeinheiten aus Bestellungen mit dem Status „Bestellt“, „Reserviert“ oder „Freigegeben“ konsolidieren. Es hilft Lagerverwaltern, Entnahmeorte intelligent zu planen, bevor sie Aufträge für den Lagerort freigeben und Kommissionierarbeiten erstellen.
author: Mirzaab
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventFixedLocation, WHSSlotDemandLocated, WHSSlotDemand, WHSSlotUOMTier, WHSSlotTemplate, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: d319a1130facbc2988cc074960e6cdfbe053a2d6
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218943"
---
# <a name="warehouse-slotting"></a>Zuteilung von Zeitfenstern für Lagerort

[!include [banner](../includes/banner.md)]

Es stehen mehrere Funktionen für Lagerorte zur Verfügung, um Lagerleiter bei der intelligenten Planung von Lagerplätzen zu unterstützen, bevor sie Aufträge an das Lager freigeben und Entnahmearbeiten erstellen.

Mit der Funktion *Lagerorteinteilung* können Sie die Nachfrage nach Elementen und Maßeinheiten von Aufträgen konsolidieren, die den Status *Bestellt*, *Reserviert* oder *Freigegeben* haben. Der generierte Bedarf kann dann auf Lagerplätze angewendet werden, die für die Kommissionierung verwendet werden, basierend auf Menge, Einheit, physischen Dimensionen, festen Lagerplätzen und mehr. Nachdem der Plan für die Zuteilung von Zeitfenstern erstellt wurde, können Wiederbeschaffungsarbeiten erstellt werden, um die entsprechende Menge an Bestand an jeden Lagerplatz zu bringen.

Mit der Funktion *Lagerplätze für Transportaufträge* können Lagerort-Verwalter Wiederbeschaffung betreiben, basierend auf der Nachfrage von Transportaufträgen, die noch nicht für das Lager freigegeben sind. Sie stellt sicher, dass die Lagerorte alle Elemente enthalten, die für die Transportaufträge benötigt werden, nachdem sie für das Lager freigegeben wurden. Diese Funktion setzt voraus, dass Sie auch die Funktion *Lagerorte einlagern* einschalten.

Die Funktion *Erweiterung der Lagerort-Zuweisung* fügt eine Option für die Vorlagenzeilen hinzu, die von der Funktion *Lagerort-Zuweisung* verwendet werden. Die Option ermöglicht es dem System, den vorhandenen Bestand an einem Lagerplatz zu berücksichtigen. Daher werden möglicherweise weniger Wiederbeschaffungen für die Platzierung erzeugt. Die Funktion *Erweiterung der Lagerort-Zuweisung* erfordert, dass Sie auch die Funktion *Lagerort-Zuweisung* einschalten. Sie kann optional zusammen mit der Funktion *Lagerort-Zuteilung für Transportaufträge* verwendet werden.

## <a name="turn-on-the-warehouse-slotting-features"></a>Einschalten der Funktionen für den Lagerort

Bevor Sie diese Funktionen verwenden können, müssen sie in Ihrem System eingeschaltet werden. Administratoren können mit den Einstellungen in der [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktionen überprüfen und sie gegebenenfalls aktivieren. Schalten Sie die folgenden Funktionen je nach Bedarf ein:

- Lagerortzeitrahmen-Funktion
- Lagerort Einlagerung für Transportaufträge

    > [!IMPORTANT]
    > Die Funktion *Lagerort-Zuteilung* muss vor dieser Funktion eingeschaltet werden.

- Erweiterungen für die Lagerort-Zuweisung (Zuteilung von Zeitfenstern )

    > [!IMPORTANT]
    > Die Funktion *Lagerort-Zuteilung* muss vor dieser Funktion eingeschaltet werden.

## <a name="set-up-warehouse-slotting"></a>Zuteilung von Zeitfenstern für den Lagerort einrichten

Um die Lagerort-Zuteilung zu verwenden, müssen Sie die folgenden Elemente in Ihrem System festlegen:

- Maßeinheitsebenen für die Zuteilung von Zeitfenstern
- Richtliniencodes
- Vorlagen für die Zuteilung von Zeitfenstern
- Lagerplatzrichtlinien

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a>Maßeinheitsstufen für Zuteilung von Zeitfenstern erstellen

Mithilfe von Maßeinheitsstufen können mehrere Maßeinheiten zum Zwecke der Zuteilung von Zeitfenstern zusammengefasst werden. Wenn beispielsweise mehrere Kistengrößen aus demselben Kistenauswahlbereich ausgewählt werden, kann für alle Größen eine Stufe erstellt werden. **Für jede Maßeinheit, die Teil der Stufe sein soll, muss eine Position erstellt werden.**

1. Gehen Sie zu **Lagerortverwaltung \> Setup \> Wiederbeschaffung \> Maßeinheitsstufen für Zuteilung von Zeitfenstern**.
1. Wählen Sie **Neu** aus.
1. Legen Sie im Header die folgenden Werte fest:

    - **Maßeinheitsstufe:** *EaBoxPl*
    - **Beschreibung:** *Jede Kistenpalette*

1. Wählen Sie **Speichern** aus.
1. Wählen Sie im Inforegister **Maßeinheiten** die Option **Neu** aus, um dem Raster eine Position hinzuzufügen.
1. Legen Sie die folgenden Werte für die neue Position fest:

    - **Einheit:** *Kiste*
    - **Beschreibung:** Lassen Sie dieses Feld leer. Es wird automatisch ausgefüllt, wenn Sie Ihre Änderungen speichern.
    - **Einheitenklasse:** *Menge*

1. Wählen Sie **Neu** aus, um dem Raster eine zweite Position hinzuzufügen.
1. Legen Sie die folgenden Werte für die neue Position fest:

    - **Einheit:** *ea*
    - **Beschreibung:** Lassen Sie dieses Feld leer. Es wird automatisch ausgefüllt, wenn Sie Ihre Änderungen speichern.
    - **Einheitenklasse:** *Menge*

1. Wählen Sie **Neu** aus, um dem Raster eine dritte Position hinzuzufügen.
1. Legen Sie die folgenden Werte für die neue Position fest:

    - **Einheit:** *PL*
    - **Beschreibung:** Lassen Sie dieses Feld leer. Es wird automatisch ausgefüllt, wenn Sie Ihre Änderungen speichern.
    - **Einheitenklasse:** *Menge*

1. Wählen Sie **Speichern** aus, um die Stufe zu speichern.

### <a name="create-a-directive-code-for-slotting"></a>Richtliniencode für Zuteilung von Zeitfenstern erstellen

Sie müssen den Richtliniencode auswählen, der einer Vorlage zugeordnet werden soll.

1. Wechseln Sie zu **Lagerortverwaltung \> Setup \> Richtliniencodes**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Geben Sie im Feld **Richtliniencode** *Zuteilung von Zeitfenstern* ein.
1. Geben Sie im Feld **Richtlinienbeschreibung** *Zuteilung von Zeitfenstern* ein.

### <a name="set-up-slotting-templates"></a>Vorlagen für Zuteilung von Zeitfenstern einrichten

Jede Vorlage für die Zuteilung von Zeitfenstern steuert, wie der Bestand den Lagerplätzen für einen bestimmten Lagerort zugewiesen wird. Jede Vorlage muss eine Position für jede Spezifikation für die Zuteilung von Zeitfenstern enthalten. Verwenden Sie die in diesem Abschnitt beschriebenen Verfahren, um Vorlagen für die Zuteilung von Zeitfenstern einzurichten.

1. Gehen Sie zu **Lagerortverwaltung \> Setup \> Wiederbeschaffung \> Vorlagen für Zuteilung von Zeitfenstern**.
1. Wählen Sie **Neu** aus, um eine Vorlage zu erstellen.

Als Nächstes müssen Sie den Vorlagenkopf, die Spezifikationen für die Zuteilung von Zeitfenstern und die Lagerplatzrichtlinien einrichten, wie in den folgenden Unterabschnitten erläutert. Das Einrichten der Lageraufteilung für Transportaufträge ähnelt dem Einrichten der Lageraufteilung für Verkaufsaufträge, aber das Feld **Auftragsart** ist auf *Transportaufträge* anstelle von *Verkaufsauftrag* festgelegt.

#### <a name="set-up-the-header-for-a-sales-order-slotting-template"></a>Festlegen der Kopfzeile für eine Vorlage für die Zuteilung von Zeitfenstern von Verkaufsaufträgen

1. Legen Sie in der Kopfzeile der Vorlage die folgenden Werte fest:

    - **Vorlage für die Zuteilung von Zeitfenstern:** _61_
    - **Beschreibung:** _61_
    - **Bedarfstyp:** *Auftrag*

        > [!NOTE]
        > Derzeit sind *Verkaufsaufträge* und *Transferaufträge* die einzigen Bedarfsarten, die unterstützt werden. Sie können *Transportaufträge* nur auswählen, wenn die Funktion *Lagerort Zuteilung von Zeitfenstern für Transportaufträge* eingeschaltet ist.

    - **Bedarfsstrategie:** _Bestellt_

        In diesem Feld stehen folgende Werte zur Verfügung:

        - **Bestellt** – Die volle Bestellmenge auf dem Auftrag sollte als Bedarf betrachtet werden.
        - **Reserviert** – Nur die reservierten (physischen und bestellten) Auftragspositionsmengen sollten als Bedarf betrachtet werden.
        - **Freigegeben** - Die freigegebene Menge soll als Bedarf betrachtet werden.

    - **Lagerort:** _61_
    - **Wellenbedarf die Nutzung nicht reservierter Mengen gestatten:** _Ja_

Sie können auch eine Abfrage angeben, um den Umfang des ausgewerteten Bedarfs einzugrenzen.

#### <a name="set-up-slotting-specifications-for-each-template"></a>Spezifikationen für Zuteilung von Zeitfenstern für jede Vorlage einrichten

Führen Sie für jede Verkaufsauftragsvorlage, die Sie erstellen, die folgenden Schritte aus, um eine Zeile für jede Zuteilung von Zeitfenstern-Spezifikation hinzuzufügen.

1. Wählen Sie im Inforegister **Vorlagendetails für Zuteilung von Zeitfenstern** die Option **Neu** aus, um eine Vorlagenposition zu erstellen.
1. Legen Sie die folgenden Werte für die neue Position fest:

    - **Sequenz:** _1_
    - **Beschreibung:** _Fester Lagerplatz_
    - **Mindestmenge:** _1_

        Dieses Feld definiert die Mindestbedarfsmenge, die für die Position erforderlich ist.

    - **Höchstmenge:** _1000000_

        Dieses Feld definiert die Höchstbedarfsmenge, die für die Position gültig ist.

    - **Einheit:** Lassen Sie dieses Feld leer.

        Dieses Feld definiert die Maßeinheit, auf die sich die minimalen und maximalen Mengen beziehen.

    - **Maßeinheitsstufe:** _EaBoxPl_

        Dieses Feld definiert die Bedarfsmaßeinheiten, die für die Position gültig sind. (Weitere Informationen erhalten Sie im Abschnitt [Maßeinheitsstufen für Zuteilung von Zeitfenstern einrichten](#unit-tiers) weiter oben in diesem Artikel.)

    - **Kriterien für Zuteilung von Zeitfenstern zuweisen:** _Menge betrachten_

        In diesem Feld stehen folgende Werte zur Verfügung:

        - **Angenommen leer** – Dieses System sollte davon ausgehen, dass alle Lagerplätze im Kommissionierbereich leer sind, und diese Lagerplätze nicht auf Bestand prüfen.
        - **Menge betrachten** – Das System sollte die Lagerplätze im Kommissionierbereich auf Bestand überprüfen und alle Lagerplätze überspringen, die nicht leer sind.
        - **Bestandsmäßig berücksichtigen** - Das System sollte prüfen, ob irgendein Ziellagerplatz nicht reservierte Mengen für das Element in der Bedarfszeile enthält. Wenn die Menge groß genug ist, um mindestens eine Einheit der Bedarfszeile zu befriedigen, wird der generierte Zuteilung von Zeitfenstern-Plan-Datensatz um die verfügbare Menge reduziert. Wenn der Bedarf z. B. 10 Kisten beträgt und eine Kiste vorrätig ist, beträgt der lokalisierte Bedarf neun Kisten. Wenn der Bedarf 10 Fälle beträgt und jeweils ein Fall vorhanden ist, beträgt der geortete Bedarf 10 Fälle. Dieser Wert ist nur verfügbar, wenn die Funktion *Erweiterungen für die Lagerort-Zuweisung* eingeschaltet ist.

    - **Richtliniencode:** _Zuteilung von Zeitfenstern_

        Dieses Feld definiert die Lagerplatzrichtlinie, mit der der Kommissionierort der Wiederbeschaffungsarbeiten ermittelt wird.

    - **Überlauflagerplatz:** Lassen Sie dieses Feld leer.

        Dieses Feld definiert den Lagerplatz, an den der Bestand eingelagert wird, wenn bei der Verarbeitung der Position kein Lagerplatz für die Menge gefunden werden kann.

    - **Pause zulassen:** _Ja_

        Wenn diese Option auf *Ja* festgelegt ist, wenn die Zuteilung von Zeitfenstern für Bedarf nicht möglich ist, werden Bewegungsarbeiten erstellt, um Bestand von Lagerplätzen zu entfernen, an denen Bestand vorhanden ist, an denen jedoch keine Zuteilung von Zeitfenstern durchgeführt wurde. Die Vorlage wird dann erneut ausgeführt. Dieses Mal wird der Bestand an den Lagerplätzen ignoriert. Diese Funktionalität funktioniert am besten, wenn das Feld **Kriterien für Zuteilung von Zeitfenstern zuweisen** auf _Menge betrachten_ festgelegt ist.

    - **Feste Lagerplatznutzung:** _Nur feste Lagerplätze für das Produkt_

        In diesem Feld stehen folgende Werte zur Verfügung:

        - **Feste und nicht feste Lagerplätze** – Das System sollte nicht darauf beschränkt sein, nur feste Lagerplätze zu verwenden.
        - **Nur feste Lagerplätze für das Produkt** – Das System sollte nur an Lagerplätze eingesetzt werden, die feste Lagerplätze für das Produkt sind.
        - **Nur feste Lagerplätze für die Produktvariante** – Das System sollte nur an Lagerplätze eingesetzt werden, die feste Lagerplätze für die Produktvariante sind.

> [!NOTE]
> Wenn die Slot-Vorlage mindestens eine Zeile enthält, in der das Feld **Slot-Zuordnungskriterien** auf *Vorhandenes berücksichtigen* festgelegt ist, sind für keine Zeile in der Vorlage mehr Aufschläge erlaubt.

1. Wählen Sie **Speichern** aus.
1. Wählen Sie **Neu** aus, um eine zweite Vorlagenposition zu erstellen.
1. Legen Sie die folgenden Werte für die neue Position fest:

    - **Sequenz:** _2_
    - **Beschreibung:** _Sonstige_
    - **Mindestmenge:** _1_
    - **Höchstmenge:** _1000000_
    - **Einheit:** Lassen Sie dieses Feld leer.
    - **Maßeinheitsstufe:** _EaBoxPl_
    - **Kriterien für Zuteilung von Zeitfenstern zuweisen:** _Menge betrachten_
    - **Richtliniencode:** _Zuteilung von Zeitfenstern_
    - **Überlauflagerplatz:** Lassen Sie dieses Feld leer.
    - **Pause zulassen:** _Ja_
    - **Feste Lagerplätze nutzen:** _Feste und nicht feste Lagerplätze_

    In der Abfrage für die zweite Position geben Sie nun die Kriterien an, anhand derer bestimmt wird, an welchen Lagerplätzen die Zuteilung von Zeitfenstern für den Bestand für diese Position möglich ist.

1. Wählen Sie die Position aus, in der das Feld **Sequenz** auf *2* festgelegt ist.
1. Wählen Sie **Abfrage bearbeiten**.
1. Wählen Sie auf der Registerkarte **Bereich** die Option **Hinzufügen** aus, um dem Raster eine Position hinzuzufügen.
1. Legen Sie die folgenden Werte für die neue Position fest:

    - **Tabelle:** *Lagerorte*
    - **Abgeleitete Tabelle:** *Lagerorte*
    - **Feld:** *Lagerortprofilkennung*
    - **Kriterien:** *Pick-06* (Wählen Sie das doppelte Pluszeichen \[**++**\] im Feld, um die Liste zu erweitern, und wählen Sie dann *Pick-06* - *Kommissionierstelle 6*.)

1. Wählen Sie **OK**.

#### <a name="set-up-location-directives"></a>Lagerplatzrichtlinien einrichten

Es muss mindestens eine Lagerplatzrichtlinie eingerichtet werden, um die Zuteilung von Zeitfenstern für Entnahmen zu unterstützen. Verwenden Sie die Verfahren in diesem Abschnitt, um eine neue *Wiederbeschaffungslagerplatzrichtlinie* für die Zuteilung von Zeitfenstern für Entnahmen einzurichten.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerplatzrichtlinien**.
1. Wählen Sie im linken Bereich im Feld **Arbeitsauftragstyp** *Wiederbeschaffung* aus.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Geben Sie in der Kopfzeile für die neue Lagerplatzrichtlinie im Feld **Name** *61 Zuteilung von Zeitfenstern für Entnahmen* ein.
1. Übernehmen Sie im Feld **Sequenznummer** den Standardwert.

##### <a name="configure-the-location-directives-fasttab"></a>Inforegister „Lagerplatzrichtlinien“ konfigurieren

1. Legen Sie im Inforegister **Lagerplatzrichtlinien** die folgenden Werte fest. Akzeptieren Sie die Standardwerte für alle anderen Felder.

    - **Arbeitstyp:** _Entnahme_
    - **Standort:** _6_
    - **Lagerort:** _61_
    - **Richtliniencode:** _Zuteilung von Zeitfenstern_

1. Wählen Sie **Speichern** aus, um das Inforegister **Positionen** verfügbar zu machen.

##### <a name="configure-the-lines-fasttab"></a>Inforegister „Positionen“ konfigurieren

1. Klicken Sie im Inforegister **Positionen** auf **Neu**, um eine Position zu erstellen.
1. Legen Sie die folgenden Werte für die neue Position fest.

    - **Von Menge:** _0_
    - **Bis Menge:** _1000000_

1. Übernehmen Sie für alle verbleibenden Felder die Standardwerte.
1. Wählen Sie **Speichern** aus, um das Inforegister **Lagerplatzrichtlinienaktivitäten** verfügbar zu machen.

##### <a name="configure-the-location-directive-actions-fasttab"></a>Inforegister „Lagerplatzrichtlinienaktivitäten“ konfigurieren

1. Wählen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** die Option **Neu** aus, um eine Position zu erstellen.
1. Legen Sie die folgenden Werte für die neue Position fest. Akzeptieren Sie die Standardwerte für alle anderen Felder.

    - **Sequenznummer:** Akzeptieren Sie den Standardwert.
    - **Name:** _Bulk_
    - **Strategie:** _Keine_

1. Übernehmen Sie für alle verbleibenden Felder die Standardwerte.
1. Wählen Sie **Speichern** aus, um die Schaltfläche **Abfrage bearbeiten** verfügbar zu machen.

##### <a name="edit-the-query"></a>Abfrage bearbeiten

1. Wählen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** **Abfrage bearbeiten** aus.
1. Wählen Sie auf der Registerkarte **Bereich** die Option **Hinzufügen** aus, um dem Raster eine Position hinzuzufügen.
1. Legen Sie die folgenden Werte für die neue Position fest:

    - **Tabelle:** *Lagerorte*
    - **Abgeleitete Tabelle:** *Lagerorte*
    - **Feld:** *Zonen-ID*
    - **Kriterien:** *Bulk* (Wählen Sie das doppelte Pluszeichen \[**++**\] im Feld, um die Liste zu erweitern, und wählen Sie dann *Bulk*.)

1. Wählen Sie **OK**.

## <a name="scenario"></a>Szenario

### <a name="set-up-the-scenario"></a>Szenario einrichten

Verwenden Sie für dieses Szenario die integrierten Beispieldaten und erstellen Sie die in diesem Abschnitt beschriebenen Datensätze.

#### <a name="use-the-usmf-sample-data"></a>USMF-Beispieldaten verwenden

Um dieses Szenario mithilfe der Beispieldatensätze und -werte, die hier angegeben sind, zu verarbeiten, müssen Sie ein System verwenden, auf dem die standardmäßigen [Demodaten](../../fin-ops-core/fin-ops/get-started/demo-data.md) installiert sind. Außerdem müssen Sie die **USMF** juristische Person auswählen, bevor Sie beginnen.

#### <a name="create-demand"></a>Bedarf erstellen

Befolgen Sie diese Schritte, um den Bedarf zu erstellen, auf den Sie die Zuteilung von Zeitfenstern anwenden.

1. Gehen Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
1. Wählen Sie **Neu** aus, um einen Auftrag zu erstellen.
1. Wählen Sie im Dialogfeld **Auftrag erstellen** im Feld **Debitorenkonto** _US-007_ aus.
1. Im Feld **Lagerort** wählen Sie _61_ aus.
1. Wählen Sie **OK**.
1. Der neue Auftrag wird geöffnet. Er enthält eine leere Position im Inforegister **Auftragspositionen**. Legen Sie die folgenden Werte für diese Position fest:

    - **Artikel:** _L0101_
    - **Menge** _20_

1. Wählen Sie **Position hinzufügen** aus, um eine neue Position hinzuzufügen, und legen Sie die folgenden Werte fest:

    - **Artikel:** _T0100_
    - **Menge** _8_

1. Wählen Sie **Speichern** aus.
1. Wählen Sie **Neu** aus, um einen zweiten Auftrag zu erstellen.
1. Wählen Sie im Dialogfeld **Auftrag erstellen** im Feld **Debitorenkonto** _US-008_ aus.
1. Im Feld **Lagerort** wählen Sie _61_ aus.
1. Der neue Auftrag wird geöffnet. Er enthält eine leere Position im Inforegister **Auftragspositionen**. Legen Sie die folgenden Werte für diese Position fest:

    - **Artikel:** _T0100_
    - **Menge** _1_

1. Wählen Sie **Speichern** aus.

### <a name="walk-through-a-typical-slotting-scenario"></a>Typisches Szenario für Zuteilung von Zeitfenstern durchgehen

Nachdem alle erforderlichen Elemente vorhanden sind, wie im vorherigen Abschnitt beschrieben, können Sie die Funktion ausprobieren, indem Sie jede Übung in diesem Abschnitt durcharbeiten.

#### <a name="generate-demand"></a>Bedarf generieren

1. Navigieren Sie zu **Lagerortverwaltung \> Setup \> Wiederbeschaffung \> Vorlagen für Zuteilung von Zeitfenstern**, und wählen Sie die Vorlage für die Zuteilung von Zeitfenstern aus, die Sie zuvor erstellt haben.
1. Wählen Sie im Aktivitätsbereich **Bedarf generieren** aus. Dieser Befehl wertet den gesamten Bedarf aus, der sich im System befindet und mit der Vorlagenabfrage für die Zuteilung von Zeitfenstern übereinstimmt. Der Gesamtbedarf aller Bestellungen wird dann in einer Position pro Menge/Maßeinheit zusammengefasst. Nach Abschluss des Vorgangs wird eine Informationsmeldung angezeigt.

#### <a name="slotting-demand"></a>Bedarf an der Zuteilung von Zeitfenstern

Die *Zuteilung von Zeitfenstern für den Bedarf* zeigt die Ergebnisse der Bedarfsgenerierung basierend auf dem Setup der Vorlage für die Zuteilung von Zeitfenstern.

- Wählen Sie im Aktivitätsbereich **Zuteilung von Zeitfenstern für den Bedarf** aus, um die Ergebnisse aus dem Befehl **Bedarf generieren** zu sehen. Die Positionen in der Zuteilung von Zeitfenstern für den Bedarf können bearbeitet werden. Sie können eine Position löschen, eine neue Position hinzufügen oder die Positionsdetails bearbeiten.

> [!NOTE]
> Sie können den Bedarf manuell bearbeiten oder mithilfe der Datenverwaltung von einem externen System importieren. Was auch immer in der Zuteilung von Zeitfenstern für den Bedarf enthalten ist, wird im nächsten Schritt verwendet, unabhängig davon, woher es stammt.

#### <a name="locate-demand"></a>Bedarf ermitteln

Nachdem der Bedarf generiert wurde, müssen Sie den Befehl **Bedarf ermitteln** verwenden, um den *Plan für die Zuteilung von Zeitfenstern* zu generieren.

- Wählen Sie im Aktivitätsbereich **Bedarf ermitteln** aus. Der Vorgang für die Zuteilung von Zeitfenstern läuft. Nach Abschluss des Vorgangs wird eine Informationsmeldung angezeigt.

#### <a name="slotting-plan"></a>Plan für die Zuteilung von Zeitfenstern

Der Plan für die Zuteilung von Zeitfenstern zeigt den Lagerplatz, dem jeder Artikel/jede Menge zugewiesen wurde, ob ein Überlauf verwendet wurde, ob Pausenarbeiten erstellt wurden und welche Vorlagenposition verwendet wurde. *Jeder Bedarf, für den keine Zuteilung von Zeitfenstern möglich ist, wird rot hervorgehoben.*

- Wählen Sie im Aktivitätsbereich **Plan für die Zuteilung von Zeitfenstern** aus, um die Ergebnisse anzuzeigen.

> [!NOTE]
> - Die Prozesse **Bedarf generieren**, **Bedarf lokalisieren** und **Wiederbeschaffung ausführen** werden jetzt in einer Sandbox ausgeführt. (Diese Prozesse sind im Aktivitätsbereich auf der Seite **Nachschubvorlagen** verfügbar).
> - Die Prozesse **Bedarf generieren**, **Bedarf lokalisieren** und **Nachschub ausführen** haben eine Sperre, um sicherzustellen, dass sie nicht gleichzeitig ausgelöst werden können. Andernfalls könnten die verwendeten Daten gelöscht werden.
> - Die Prozesse **Nachschub generieren** und **Nachschub lokalisieren** zeigen eine Warnung an, wenn der Lauf keine Datensätze generiert hat oder wenn in den Datensätzen Informationen fehlen.
> - Wenn Sie **Bedarfsplan** wählen, hat die Seite keine Schaltflächen **Neu**, **Bearbeiten** oder **Löschen** im Aktivitätsbereich, weil die Datenquelle nicht bearbeitet werden kann.
> - Wenn Sie **Wiederbeschaffung ausführen** wählen, validiert das System die ausgewählte Slot-Vorlage und die Prozesse.

#### <a name="create-replenishment"></a>Wiederbeschaffung erstellen

Nachdem der Plan für die Zuteilung von Zeitfenstern erstellt wurde, müssen Sie *Wiederbeschaffungsarbeiten* basierend auf dem Plan erstellen.

- Wählen Sie im Aktivitätsbereich **Wiederbeschaffung ausführen** aus. Nach Abschluss des Vorgangs wird eine Informationsmeldung angezeigt. Diese Nachricht gibt die Anzahl der Header an, die für die Arbeits-Build-ID erstellt wurden.

Zu verwendende Lagerplatzrichtlinien werden anhand des Richtliniencodes identifiziert, der in jeder Vorlagenposition angegeben ist.

## <a name="tips"></a>Tipps

### <a name="set-up-automatic-slotting"></a>Automatische Zuteilung von Zeitfenstern einrichten

Nachdem alle erforderlichen Elemente vorhanden sind, können Sie die Zuteilung von Zeitfenstern so einrichten, dass sie automatisch ausgeführt wird, indem Sie die folgenden Schritte ausführen.

1. Wechseln Sie zu **Lagerortverwaltung \> Wiederbeschaffung \> Zuteilung von Zeitfenstern ausführen**.
1. Geben Sie die auszuführenden Schritte für die Zuteilung von Zeitfenstern an. Wählen Sie einen oder mehrere der folgenden Schritte für die Zuteilung von Zeitfenstern aus:

    - Bedarf generieren
    - Bedarf ermitteln
    - Wiederbeschaffungsarbeit erstellen

    > [!NOTE]
    > Die Schritte für die Zuteilung von Zeitfenstern sind progressiv. Wenn Sie *Bedarf ermitteln* auswählen möchten, müssen Sie zuerst *Bedarf generieren* auswählen.

1. Geben Sie die zu verwendende Vorlage für die Zuteilung von Zeitfenstern an.
1. Stellen Sie die Serie so ein, dass sie automatisch ausgeführt wird, wenn Sie möchten.

Richten Sie für die Übungen im Szenario **nicht** die automatische Zuteilung von Zeitfenstern ein.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]