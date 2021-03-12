---
title: Auto-Freigabelieferung für Crossdocking
description: In diesem Thema wird eine Crossdockingstrategie beschrieben, mit der Sie automatisch einen Bedarfsauftrag für den Lagerort freigeben können, wenn der Produktionsauftrag, der die Bedarfsmenge liefert, als fertig gemeldet wird, sodass die Menge direkt vom Produktions-Warenabgang zum ausgehenden Lagerplatz bewegt wird.
author: omulvad
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: bcae977ede91dcaf4e455353f023e9eee4fcb2b1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977487"
---
# <a name="auto-release-shipment-for-cross-docking"></a>Auto-Freigabelieferung für Crossdocking

[!include [banner](../includes/banner.md)]

In diesem Thema wird eine Crossdockingstrategie beschrieben, mit der Sie automatisch einen Bedarfsauftrag für den Lagerort freigeben können, wenn der Produktionsauftrag, der die Bedarfsmenge liefert, als fertig gemeldet wird. Auf diese Weise wird die Menge, die für die Erfüllung des Bedarfsauftrags erforderlich ist, direkt vom Produktions-Warenabgang zum ausgehenden Lagerplatz bewegt.

Crossdocking ist ein Lagerortverarbeitungsfluss, wobei die Menge, die erforderlich ist, um einen ausgehenden Auftrag zu erfüllen, an die Ausgangsrampe oder den Stagingbereich des Auftrags vom Lagerplatz weitergeleitet wird, wo der eingehende Auftrag empfangen wurde. (Der eingehende Auftrag kann eine Bestellung, ein Umlagerungsauftrag oder ein Produktionsauftrag sein.) Während die erweiterte Crossdockingfunktion alle Angebot- und Nachfrageaufträge unterstützt und erfordert, dass der ausgehende Bedarf freigegeben wird, bevor die Crossdockingchance identifiziert wird, weist die Auto-Freigabelieferungsfunktion diese Eigenschaften auf:

- Sie unterstützt nur Produktionsaufträge als Angebot und nur Bestellungen und Umlagerungsaufträge als Bedarf.
- Der Crossdockingvorgang kann auch dann gestartet werden, wenn der Bedarfsauftrag nicht für den Lagerort freigegeben wurde, bevor der Angebotszugang erfasst wurde (das heißt bevor die Produktion als fertig gemeldet wurde).

Diese Crossdockingfunktion hat zwei Vorteile:

- Die Lagerortarbeitsgänge können den Schritt des Einlagerns von Mengen von Fertigerzeugnissen im regulären Wareneingangsbereich überspringen, wenn diese Mengen einfach erneut entnommen werden, um den ausgehenden Auftrag zu erfüllen. Stattdessen können die Mengen einmalig umgelagert werden, vom ausgehenden Lagerplatz zu einem Verpackungs-/Lieferlagerplatz. Auf diese Weise kann mit der Funktion die Häufigkeit verringert werden, zu der der Bestand verarbeitet wird, und letztendlich maximal Zeit und Platz im Lagerortfertigungsbereich eingespart werden.
- Die Lagerortarbeitsgänge können die Freigabe von Aufträgen sowie Umlagerungsaufträgen für den Lagerort verschieben, bis die Ausgabe von Fertigerzeugnissen für den zugehörigen Produktionsauftrag als fertig gemeldet ist. Dieser Vorteil ist vor allem für Auftragsfertigungs-Produktionsumgebungen relevant, wo die Fertigungsdurchlaufzeit in der Regel länger ist als die Lieferzeiten in Bestandsumgebungen.

## <a name="prerequisites"></a>Voraussetzungen

| Voraussetzung | Beschreibung |
|---|---|
| Element | Der Artikel muss für Lagerortverwaltungsprozesse aktiviert werden.<p>**Hinweis:** Artikel mit Artikelgewicht können nicht in den Crossdockingprozessen einbezogen werden.</p> |
| Lagerort | Der Lagerort muss für Lagerortverwaltungsprozesse aktiviert werden. |
| Crossdockingvorlagen | Es muss mindestens eine Crossdockingvorlage, die die **Bei Angebotszugang**-Bedarfsfreigaberichtlinie verwendet, für einen bestimmten Lagerort eingerichtet werden. |
| Arbeitsklasse | Eine Crossdockingarbeitsklassen-ID muss für den Arbeitsauftragstyp **Crossdocking** erstellt werden. |
| Arbeitsvorlagen | Arbeitsvorlagen des **Crossdocking**-Arbeitsauftragstyps sind erforderlich, um Crossdocking-Entnahme- und Einlagerungsarbeit zu erstellen. |
| Lagerplatzrichtlinien | Lagerplatzrichtlinien des **Crossdocking**-Arbeitsauftragstyps sind erforderlich, um Einlagerungsarbeit an den Lagerplätzen, an denen Auftragsmengen verpackt und versendet werden, zu unterstützen. |
| Markierung zwischen einem Bedarfsauftrag und einem Produktionsauftrag | Das Lagerortverwaltungssystem kann nur dann die automatische Freigabe der ausgehenden Auftragslieferung auslösen und Crossdockingarbeit vom Ausgangslagerplatz bei der Fertigmeldung-Aktivität starten, wenn Aufträge und Umlagerungsaufträge für einen Produktionsauftrag reserviert und markiert werden. |

## <a name="example-cross-docking-flow"></a>Beispiel Crossdockingfluss

Ein typischer Crossdockingfluss besteht aus den folgenden Hauptschritten.

1. Ein Auftragnehmer erstellt einen Auftrag für ein Auftragsfertigungsprodukt. In der Regel ist die angeforderte Menge nicht verfügbar und muss zuerst produziert werden.
2. Der Auftragnehmer erstellt einen Produktionsauftrag direkt aus der Auftragsposition. Auf diese Weise reserviert und markiert der Auftragnehmer die Auftragsmenge für Produktionsauftragsmenge. 

    Alternativ gibt ein Produktionsplaner an, dass die Markierung aktualisiert werden muss, wenn Bestellvorschläge umgewandelt werden.

3. Der Produktionsauftrag durchläuft die folgenden Schritte:

    1. Ein Produktionsplaner schätzt den Produktionsauftrag und gibt ihn frei. (Die Vorkalkulation enthält die Rohmaterialreservierung, und die Freigabe enthält die Freigabe für einen Lagerort.)
    2. Ein Lagerarbeiter startet und finalisiert die Rohmaterialentnahme vom Lagerplatz für einen Produktionseingangslagerplatz, gemäß der Produktionsentnahmearbeit.
    3. Ein Bediener im Fertigungsbereich startet den Produktionsauftrag.
    4. Im letzten Arbeitsgang verwendet ein Maschinenbediener das mobile Gerät, um den Produktionsauftrag als fertig zu melden.

4. Das System verwendet die Einstellung, um das Crossdockingereignis für die beiden verknüpften Aufträge zu identifizieren und schließt dann diese Aufgaben ab:

    1. Automatische Freigabe des zugeordneten Auftrags für einen Lagerort, um eine Lieferung zu erstellen.
    2. Automatisches Erstellen einer Crossdockingarbeit mit den Anweisungen, die Fertigerzeugnisse vom Ausgangslagerplatz zu entnehmen und sie zum Ausgangslagerplatz zu bewegen, den die Crossdockinglagerplatzrichtlinien zum Auftrag zugewiesen haben.
    3. Auffordern eines Maschinenbedieners, die Crossdockingarbeit umgehend auszuführen, nachdem der Produktionsauftrag als fertig gemeldet wurde.

5. Nachdem die Crossdockingarbeit abgeschlossen ist und die Mengen auf das Fahrzeug geladen wurden, bestätigt ein Ausgangslagerortplaner die Auftragslieferung.

## <a name="example-scenario"></a>Beispielszenario

Für dieses Szenario müssen Demodaten eingerichtet werden, und Sie müssen das **USMF**-Demodatunternehmen verwenden.

### <a name="set-up-cross-docking-that-uses-the-auto-release-shipment-feature"></a>Einrichten von Crossdocking mit Auto-Freigabelieferungsfunktion

#### <a name="cross-docking-template"></a>Crossdockingvorlage

1. Wechseln Sie zu **Lagerortverwaltung** \> **Einstellungen** \> **Arbeit** \> **Crossdocking-Vorlagen**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Laufende Nummer** den Wert **1** ein.
4. Geben Sie im Feld **Crossdockingvorlagen-ID** einen Namen ein, wie **XDock\_RAF**.
5. Wählen Sie im Feld **Bedarfsfreigaberichtlinie** **Bei Angebotszugang** aus.
6. Geben Sie im Feld **Lagerort** die Nummer des Lagerorts ein, für den Sie den Crossdockingprozess einrichten möchten. Wählen Sie für dieses Beispiel **51** aus.

    > [!NOTE]
    > Wenn Sie **Bei Angebotszugang** als Bedarfsfreigabenrichtlinie für die Vorlage ausgewählt haben, sind alle anderen Felder auf der Seite nicht mehr verfügbar. Ebenso können Sie keine Lieferungsquellen definieren. Dieses Verhalten tritt auf, da Crossdocking, das die Auto-Freigabelieferungsfunktion verwendet, nur Produktionsaufträge als Lieferungsquellen unterstützt und es erfordert, dass eine Markierung zwischen Aufträgen und Produktionsaufträgen vorhanden ist. Wenn Sie **Vor Angebotszugang** als Bedarfsfreigabenrichtlinie auswählen, sind die Felder auf den Registerkarten **Planung** und **Lieferungsquellen** verfügbar und können bearbeitet werden.

#### <a name="work-classes"></a>Arbeitsklassen

1. Wechseln Sie zu **Lagerortverwaltung** \> **Einstellungen** \> **Arbeit** \> **Arbeitsklassen**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Arbeitsklassen-ID** einen Namen ein, wie **CrossDock**.
4. Wählen Sie im Feld **Arbeitsauftragstyp** **Crossdocking** aus.

Um die Typen der Lagerplätze, an denen Crossdock-Fertigerzeugnisse eingelagert werden können, einzuschränken, können Sie mindestens einen gültigen Lagerplatztypen angeben.

#### <a name="work-templates"></a>Arbeitsvorlagen

1. Wechseln Sie zu **Lagerortverwaltung** \> **Einstellungen** \> **Arbeit** \> **Arbeitsvorlagen**.
2. Wählen Sie im Feld **Arbeitsauftragstyp** **Crossdocking** aus.
3. Wählen Sie **Neu** aus.
4. Geben Sie im Feld **Laufende Nummer** den Wert **1** ein.
5. Geben Sie im Feld **Arbeitsvorlage** einen Namen ein, wie **CrossDock\_51**.
6. Wählen Sie **Speichern**.
7. Im Abschnitt **Arbeitsvorlagendetails** wählen Sie **Neu** aus.
8. Wählen Sie für die neue Position im Feld **Arbeitstyp** **Entnahme** aus. Wählen Sie im Feld **Arbeitsklassen-ID** **CrossDock** aus.
9. Wählen Sie **Neu** aus.
10. Wählen Sie für die neue Position im Feld **Arbeitstyp** **Einlagerung** aus. Wählen Sie im Feld **Arbeitsklassen-ID** **CrossDock** aus.

#### <a name="location-directives"></a>Lagerplatzrichtlinien

Ein Standard-Einlagerungsprozess für Fertigerzeugnisse erfordert eine **Einlagerung**-Lagerplatzrichtlinie, um die Bewegung von entnommenen Produktionsmengen zu einem regulären Lagerbereich zu unterstützen. Ebenso müssen Sie eine **Einlagerung**-Lagerplatzrichtlinie einrichten, um die Arbeit anzuweisen, die fertige Menge in einen ausgewählten ausgehenden Lagerplatz einzulagern, der die Lieferung des zugehörigen Auftrags bereitstellt.

Für Crossdocking, in Bezug auf die reguläre Einlagerung von Fertigerzeugnissen, müssen Sie keine Lagerplatzrichtlinie für die Entnahmearbeitsaktivität erstellen, da der ausgehende Lagerplatz angegeben ist. Darüber hinaus wird bei diesem ausgehenden Lagerplatz erwartet, dass er entweder als der Standardausgabelagerplatz in einem der ressourcenbezogenen Datensätze (das heißt die Ressource, Ressourcengruppenrelation oder Ressourcengruppe) oder als Standardproduktions-Fertigerzeugnislagerplatz für einen Lagerort eingerichtet ist.

1. Wechseln Sie zu **Lagerortverwaltung** \> **Einstellungen** \> **Lagerplatzrichtlinien**.
2. Wählen Sie im Feld **Arbeitsauftragstyp** **Crossdocking** aus.
3. Wählen Sie **Neu** aus.
4. Geben Sie im Feld **Laufende Nummer** den Wert **1** ein.
5. Geben Sie im Feld **Name** einen Namen ein, wie **Baydoor**.
6. Wählen Sie im Feld **Arbeitsart** **Eingabe**.
7. Im Feld **Standort** wählen Sei **5** aus.
8. Im Feld **Lagerort** wählen Sie **51** aus.
9. Auf dem Inforegister **Positionen** wählen Sie **Neu** aus.
10. Geben Sie im Feld **Bis Menge** die maximale Menge des Bereichs ein, wie **1000000**.
11. Wählen Sie **Speichern**.
12. Auf dem Inforegister **Lagerplatzrichtlinien-Aktivitäten** wählen Sie **Neu** aus.
13. Geben Sie im Feld **Name** einen Namen ein, wie **Baydoor**.
14. Wählen Sie **Speichern**.
15. Sie können die Standardabfrageneinrichtung verwenden, um Lagerplätze auf einen oder mehrere bestimmte Lagerplätze zu beschränken. Wählen Sie **Abfrage bearbeiten** und **51** als Kriterium für das Feld **Lagerort** in der Tabelle **Lagerplätze** aus.

### <a name="cross-dock-finished-goods-to-the-outbound-location"></a>Crossdock-Fertigerzeugnisse für den ausgehenden Lagerplatz

Für ein Crossdocking der Menge von Fertigerzeugnissen für den ausgehenden Lagerplatz des zugehörigen Auftrags gehen Sie folgendermaßen vor.

1. Wechseln Sie zu **Vertrieb und Marketing** \> **Aufträge** \> **Alle Aufträge**.
2. Wählen Sie **Neu** aus.
3. Für den Auftragskopf wählen Sie das Debitorenkonto **US-001** und einen Lagerort aus, der für das Crossdocking eingerichtet ist, das die Auto-Freigabenlieferungsfunktion verwendet.
4. Fügen Sie eine Position für ein Fertigerzeugnis hinzu, und geben Sie **10** als Menge ein.
5. Wählen Sie im Abschnitt **Auftragspositionen** **Produkt und Beschaffung** \> **Produktionsauftrag** aus.
6. Im Dialogfeld **Produktionsauftrag erstellen** überprüfen Sie die Standardwerte und wählen Sie dann **Erstellen** aus. Ein neuer Produktionsauftrag wird erstellt und mit dem Auftrag verknüpft (das heißt reserviert und markiert).
7. Optional: Ändern Sie den Wert im Feld **Menge**, sodass er mehr ist als der Wert, der erforderlich ist, um den Auftrag zu erfüllen. Wenn die Produktionsmenge als fertig gemeldet wurde, erstellt das System Crossdockingarbeit für die markierte Menge und Einlagerungsarbeit für die Restmenge, entsprechend der regulären Vorgehensweise für die Verarbeitung der Einlagerung von Fertigerzeugnissen.

    Wie oben genannt muss eine Markierung zwischen dem Auftrag und dem Produktionsauftrag vorhanden sein. Andernfalls funktioniert das Crossdocking nicht. Eine Markierung kann auf denen mehrere Arten erstellt werden:

    - Das System kann die Markierung in den folgenden Situationen automatisch erstellen:

        - Der Produktionsauftrag wird direkt aus der Auftragsposition manuell erstellt (siehe Schritt 6).
        - Geplante Produktionsaufträge werden umgewandelt und das Feld **Markierung aktualisieren** wird auf **Standard** festgelegt.

    - Der Benutzer kann die Markierung manuell erstellen, indem er die Seite **Markierung** von der Bedarfsauftragsposition öffnet.

    > [!NOTE]
    > Eine Markierung kann für Artikel, die so eingerichtet wurden, dass Standardwerte und gewichteter Durchschnitt als Bestandsmodelle verwendet werden, nicht manuell erstellt werden.

8. Auf der Seite **Produktionsauftrag** im Aktivitätsbereich auf der **Produktionsauftrag**-Registerkarte in der Gruppe **Prozess** wählen Sie **Vorkalkulation** und dann **OK** aus. Der Auftrag wird vorkalkuliert und die Rohmaterialmenge wird für die Produktion reserviert.
9. Im Aktivitätsbereich auf der **Produktionsauftrag**-Registerkarte in der Gruppe **Prozess** wählen Sie **Freigabe** und dann **OK** aus. Die Lagerortentnahmearbeit wird für die Rohmaterialien erstellt.
10. Öffnen und überprüfen Sie die Arbeit. Wählen Sie im Aktivitätsbereich, auf der Registerkarte **Lagerort** in der Gruppe **Allgemein** die Option **Arbeitsdetails** aus. Notieren Sie die Arbeits-ID.
11. Melden Sie sich bei der Warehouse-App an, um die Arbeit an Lagerort 51 auszuführen.
12. Gehen Sie zu **Produktion** \> **Produktionsentnahme**.
13. Geben Sie die Arbeits-ID ein, um schließen Sie die Rohmaterialentnahme ab. 

    Nachdem die Arbeit als fertig gemeldet ist, ist die Menge von Rohmaterial in einen Produktionseingangslagerplatz (**005** in USMF-Demodaten) verfügbar, und die Ausführung des Produktionsauftrags kann gestartet werden.

14. Auf der Seite **Produktionsauftrag** im Aktivitätsbereich auf der **Produktionsauftrag**-Registerkarte in der Gruppe **Prozess** wählen Sie **Start** und dann **OK** aus.
15. Gehen Sie in der App zu **Produktion** \> **Fertigmeldung und Einlagerung**
16. Geben Sie im Feld **Produktkennung** die Nummer des Produktionsauftrags und weitere Pflichtdetails ein, und wählen Sie dann **OK** aus.

Beachten Sie, dass die folgenden Ereignisse auftreten:

- Die Freigabe für einen Lagerort wird für den verknüpften Auftrag ausgelöst.
- Auf Grundlage der Freigabe wird die Lieferungs- und Crossdockingarbeit erstellt. Diese Arbeit weist den Lagerortoperator an, die Mengen zu entnehmen, die erforderlich sind, um die Auftragsposition zu erfüllen, und im ausgehenden Lagerplatz einzulagern, der in den Crossdockinglagerplatzrichtlinien angegeben ist.
- Wenn die Produktionsauftragsmenge mehr ist als die Menge, die für den Auftrag erforderlich ist, wird reguläre Einlagerungsarbeit erstellt. Diese Arbeit weist den Lagerortoperator an, die Menge von Fertigerzeugnissen zu entnehmen, die nach dem Crossdocking verbleibt, und zum regulären Lagerplatz zu bewegen, gemäß den Lagerplatzrichtlinie.
