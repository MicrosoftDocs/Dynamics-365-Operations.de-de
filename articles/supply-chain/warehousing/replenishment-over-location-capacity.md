---
title: Wiederbeschaffung über Lagerplatzkapazität
description: Dieses Thema enthält Informationen zur Funktion „Wiederbeschaffung über Lagerplatzkapazität“. Mit dieser Funktion können alle für den Tag erforderlichen Wiederbeschaffungsarbeiten erstellt und die Verfügbarkeit dieser Wiederbeschaffungsarbeiten verwaltet werden, um sicherzustellen, dass am Kommissionierort weder der Lagerbestand ausgeht noch die Kapazität überschritten wird.
author: mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 309df56671bf258e1669ae6d5393de01e2b500f0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823238"
---
# <a name="replenishment-over-location-capacity"></a>Wiederbeschaffung über Lagerplatzkapazität

[!include [banner](../includes/banner.md)]

Einige Lagerorte mit hohem Volumen oder Platzmangel müssen an einem Tag mehr Mengen eines Artikels versenden, als in den Kommissionierort passen. Mit der Funktion *Wiederbeschaffung über Lagerplatzkapazität* können alle für den Tag erforderlichen Wiederbeschaffungsarbeiten erstellt und die Verfügbarkeit dieser Wiederbeschaffungsarbeiten verwaltet werden, um sicherzustellen, dass am Kommissionierort weder der Lagerbestand ausgeht noch die Kapazität überschritten wird.

Mit dieser Funktion können mehr Wiederbeschaffungsarbeiten erstellt werden, als in einen Lagerplatz passen, und es wird verhindert, dass Wiederbeschaffungsarbeiten abgeschlossen werden, wenn der Standort voll ist. Wenn der Lagerbestand am Kommissionierort unter einen konfigurierbaren Schwellenwert fällt, werden mehr Wiederbeschaffungsarbeiten zur Verfügung gestellt.

## <a name="turn-on-the-replenishment-over-location-capacity-feature"></a>Aktivieren der Funktion „Wiederbeschaffung über Lagerplatzkapazität“

Um diese Funktion verfügbar zu machen, aktivieren Sie die folgenden Funktionen in [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (in dieser Reihenfolge):

1. Organisationsweite Arbeitssperrung
1. Wiederbeschaffung über Lagerplatzkapazität

## <a name="set-up-the-feature-for-the-example-scenario"></a>Funktion für das Beispielszenario einrichten

Dieser Abschnitt enthält Richtlinien und ein Beispiel, das zeigt, wie Sie diese Funktion einrichten und Beispieldaten für das Beispielszenario vorbereiten, das später in diesem Thema bereitgestellt wird.

### <a name="enable-sample-data"></a>Beispieldaten aktivieren

Um das [Beispielszenario](#example-scenario) mithilfe der Beispieldatensätze und -werte, die hier angegeben sind, zu verarbeiten, müssen Sie ein System verwenden, auf dem die standardmäßigen [Demodaten](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) installiert sind. Außerdem müssen Sie die **USMF** juristische Person auswählen, bevor Sie beginnen.

### <a name="location-profile"></a>Lagerortprofil

Aktivieren Sie die Funktion „Wiederbeschaffung über Lagerplatzkapazität“ im Lagerplatzprofil.

1. Wechseln Sie zu **Lagerortverwaltung \> Einrichtung \> Lagerort \> Lagerplatzprofile**.
1. Wählen Sie im linken Bereich **PICK-06** aus.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Legen Sie im Inforegister **Wiederbeschaffung** die folgenden Werte fest:

    - **Lagerplatzkapazität überschreiten:** *Ja*

        Bei Aktivierung wird zugelassen, dass die Maximalkapazität des Lagerplatzes durch Wiederbeschaffungsarbeit überschritten wird. Dies aktiviert auch andere Felder im Inforegister **Wiederbeschaffung**.

    - **Schwellenwerttyp für Arbeitsverfügbarkeit:** *Menge*

        Dieses Feld definiert die Methode, mit der festgelegt wird, wann mehr Arbeit freigegeben werden soll. Sie können die Freigabe entweder nach Menge oder nach Prozentsatz festlegen:

        - *Prozent* – Wählen Sie diese Option aus, um die Kapazität in Prozent zu verwenden, die auf Bestandsgrenzen oder Volumenmaßen basiert. Durch Auswahl dieser Option wird das Feld **Überlaufprozentsatz** aktiviert und die beiden mengenbezogenen Felder **Überlaufmenge** und **Überlaufeinheit** deaktiviert.

            Sie können diese Option verwenden, wenn die Kommissionierorte Volumenmaße verwenden.

            Wenn diese Option ausgewählt ist, legen Sie das Feld **Überlaufprozentsatz** auf den Prozentsatz fest, zu dem mehr Wiederbeschaffungsarbeiten zur Verfügung gestellt werden.

        - *Menge* – Wählen Sie diese Option aus, um einen bestimmten Mengenwert zu verwenden. Durch Auswahl dieser Option wird das Feld **Überlaufprozentsatz** deaktiviert und die Felder **Überlaufmenge** und **Überlaufeinheit** aktiviert.

            Verwenden Sie diese Option, wenn Sie für die Lagerplätze, die aufgefüllt werden, keine Volumenmaße verwenden oder wenn Sie über konsistente Mengen verfügen, bei denen mehr Bestand an den Lagerplatz gebracht werden soll.

           Wenn diese Option ausgewählt ist, legen Sie die Felder **Überlaufmenge** und **Überlaufeinheit** auf die Menge und Einheit fest, ab der weitere Wiederbeschaffungsarbeiten zur Verfügung gestellt werden.

    - **Überlaufmenge:** *0,65*

        Dieses Feld definiert die Menge, bei der der Lagerplatz überquillt.

        Arbeit ist immer dann verfügbar, wenn die Summe der Bestandsmenge am Lagerplatz und der Arbeitsmenge unterhalb dieses Werts liegt. Jede Wiederbeschaffungsarbeit über diesem Wert wird gesperrt und muss manuell entsperrt werden.

        Lagerplatzbestandsgrenzen werden bei der Berechnung der Arbeitsmenge berücksichtigt.

    - **Überlaufeinheit:** *PL*

        Dieses Feld definiert die Einheit, die der Überlaufmenge zugeordnet ist.

        In diesem Fall werden mehr Wiederbeschaffungsarbeiten zur Verfügung gestellt, wenn der Lagerplatz auf 0,65 Paletten (PL) gesunken ist.

    - **Überlaufprozentsatz**

        Dieses Feld definiert den Prozentsatz, bei dem der Lagerplatz überquillt.

        Arbeit ist immer dann verfügbar, wenn die Summe der Bestandsmenge am Lagerplatz und der Arbeitsmenge unterhalb dieses Prozentsatzes liegt. Jeder Prozentsatz der Wiederbeschaffungsarbeitsmenge über diesem Wert wird gesperrt und muss manuell entsperrt werden.

        Lagerplatzbestandsgrenzen werden bei der Berechnung des Prozentsatzes der Arbeitsmenge berücksichtigt. Wenn keine Lagerplatzbestandsgrenzen definiert wurden, wird der Prozentsatz der Arbeitsmenge nach Volumen berechnet, wenn für das Lagerplatzprofil Volumenbeschränkungen definiert sind.

> [!IMPORTANT]
> Wenn Sie die Demodaten für die juristische Person **USMF** verwenden und zuvor die Funktion *Lagerplatzkennzeichenpositionierung* aktiviert haben, müssen Sie die Einstellung **Kennzeichenpositionierung aktivieren** für das Lagerplatzprofil **BULK-06** deaktivieren, um die mobilen Schritte im Beispielszenario abzuschließen.

### <a name="wave-step-code"></a>Wellenschrittcode

> [!NOTE]
> Um einen Wellenschrittcode wie hier beschrieben einzurichten, müssen Sie möglicherweise zuerst die [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) verwenden, um die Funktion namens *Organisationsweiter Wellenschrittcode* zu aktivieren.

1. Wechseln Sie zu **Lagerortverwaltung \> Einrichtung \> Wellen \> Wellenschrittcodes**.
1. Wählen Sie **Neu** aus, und legen Sie die folgenden Werte fest:

    - **Wellenschrittcode:** *Auffüllen*
    - **Wellenschrittbeschreibung:** *Wiederbeschaffung*
    - **Wellenschritttyp:** *Wiederbeschaffung*

1. Wählen Sie **Speichern** aus.

### <a name="replenishment-template"></a>Wiederbeschaffungsvorlage

Wiederbeschaffungsvorlagen sind eine Reihe von Regeln, die steuern, wann und wie ein Lagerplatz aufgefüllt wird.

1. Wechseln Sie zu **Lagerortverwaltung \> Setup \> Wiederbeschaffung \> Wiederbeschaffungsvorlagen**.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Wählen Sie im Abschnitt **Übersicht** die Position aus, in der das Feld **Wiederbeschaffungsvorlage** auf *Bedarfswiederbeschaffung* festgelegt ist.
1. Legen Sie die folgenden Werte fest:

    - **Wellenschrittcode:** *Auffüllen*
    - **Wellenbedarf die Nutzung nicht reservierter Mengen gestatten:** *Ja*

1. Wählen Sie **Speichern** aus.

### <a name="wave-template"></a>Wellenvorlage

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenvorlagen**.
1. Legen Sie im linken Bereich im Feld **Wellenvorlagentyp** *Versand* fest.
1. Wählen Sie die Vorlage **61 Shipping** in der Liste aus.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Legen Sie im Inforegister **Allgemein** die Option **Freigabe der Wiederbeschaffungsarbeit automatisieren** auf *Ja* fest.

    Legen Sie diese Option auf *Ja* fest, um bedarfsbasierte Wiederbeschaffungsarbeit zu erstellen und diese automatisch freizugeben. Sie müssen die Wiederbeschaffungswellenmethode der Wellenvorlage hinzufügen und eine Wiederbeschaffungsvorlage vom Typ **Wellenbedarf** erstellen. Richten Sie eine Wiederbeschaffungsvorlage auf der Seite **Wiederbeschaffungsvorlagen** ein. Um eine Wiederbeschaffungsvorlage einzurichten, müssen Sie der Wellenvorlage die Wiederbeschaffungsmethode hinzufügen.

1. Suchen Sie im Inforegister **Methoden** in der Spalte **Ausgewählte Methoden** die folgende Position:

    - **Methodenname:** *Auffüllen*
    - **Name:** *Wiederbeschaffung*

1. Legen Sie das Feld **Wellenschrittcode** für diese Position auf *Auffüllen* fest.
1. Wählen Sie **Speichern** aus.

## <a name="example-scenario"></a>Beispielszenario

Nachdem Sie alle zuvor beschriebenen Beispieldaten verfügbar gemacht und eingerichtet haben, können Sie dieses Szenario durcharbeiten, um die Funktion *Wiederbeschaffung über Lagerplatzkapazität* zu testen. Bei den in diesem Szenario angezeigten Werten wird davon ausgegangen, dass Sie mit den Standarddemodaten arbeiten, die juristische Person **USMF** ausgewählt und die Beispieldatensätze vorbereitet haben, die weiter oben in diesem Thema beschrieben wurden. Dieses Szenario dient auch als Beispiel, das zeigt, wie die Funktion in einer Produktionseinstellung verwendet werden kann.

### <a name="create-replenishment-work"></a>Wiederbeschaffungsarbeit erstellen

#### <a name="create-sales-order-1"></a>Auftrag 1 erstellen

1. Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um ein Dialogfeld zum Erstellen eines neuen Auftrags zu öffnen.
1. Legen Sie im Dialogfeld die folgenden Werte fest:

    - **Debitorenkonto:** *US-007*
    - **Lagerort:** *61*

1. Wählen Sie **OK** aus, um den Auftrag zu erstellen und das Dialogfeld zu schließen.
1. Der neue Auftrag wird geöffnet. Er enthält eine neue leere Position im Inforegister **Auftragspositionen**. Legen Sie die folgenden Werte für diese Position fest:

    - **Artikelnummer:** *T0100*
    - **Menge** *40*

1. Wählen Sie im Inforegister **Auftragspositionen** die Option **Bestand \> Reservierung** aus.
1. Wählen Sie auf der Seite **Reservierung** die Option **Los reservieren** aus.
1. Schließen Sie die Seite.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** auf **Lagerortfreigabe**.

    Sie erhalten Informationsnachrichten mit den Wellen- und Lieferungs-IDs, die erstellt wurden. Eine Wiederbeschaffungswelle wird ebenfalls erstellt.

    Sie erhalten außerdem eine Warnmeldung mit dem Titel „Die Arbeits-ID XXXX kann nicht entsperrt werden, da Wiederbeschaffungsarbeiten noch nicht abgeschlossen wurden.“.

#### <a name="create-sales-order-2"></a>Auftrag 2 erstellen

1. Wählen Sie auf der Seite **Alle Aufträge** im Aktivitätsbereich **Neu** aus, um ein Dialogfeld zum Erstellen eines neuen Auftrags zu öffnen.
1. Legen Sie im Dialogfeld den folgenden Wert fest:

    - **Debitorenkonto:** *US-001*
    - **Lagerort:** *61*

1. Wählen Sie **OK** aus, um den Auftrag zu erstellen und das Dialogfeld zu schließen.
1. Der neue Auftrag wird geöffnet. Er enthält eine neue leere Position im Inforegister **Auftragspositionen**. Legen Sie die folgenden Werte für diese Position fest:

    - **Artikelnummer:** *T0100*
    - **Menge** *60*

1. Wählen Sie im Inforegister **Auftragspositionen** die Option **Bestand \> Reservierung** aus.
1. Wählen Sie auf der Seite **Reservierung** die Option **Los reservieren** aus.
1. Schließen Sie die Seite.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** auf **Lagerortfreigabe**.

    Sie erhalten Informationsnachrichten mit den Wellen- und Lieferungs-IDs, die erstellt wurden. Eine Wiederbeschaffungswelle wird ebenfalls erstellt.

    Sie erhalten außerdem eine Warnmeldung mit dem Titel „Die Arbeits-ID XXXX kann nicht entsperrt werden, da Wiederbeschaffungsarbeiten noch nicht abgeschlossen wurden.“.

#### <a name="create-sales-order-3"></a>Auftrag 3 erstellen

1. Wählen Sie auf der Seite **Alle Aufträge** im Aktivitätsbereich **Neu** aus, um ein Dialogfeld zum Erstellen eines neuen Auftrags zu öffnen.
1. Legen Sie im Dialogfeld die folgenden Werte fest:

    - **Debitorenkonto:** *US-004*
    - **Lagerort:** *61*

1. Wählen Sie **OK** aus, um den Auftrag zu erstellen und das Dialogfeld zu schließen.
1. Der neue Auftrag wird geöffnet. Er enthält eine neue leere Position im Inforegister **Auftragspositionen**. Legen Sie die folgenden Werte für diese Position fest:

    - **Artikelnummer:** *T0100*
    - **Menge** *30*

1. Wählen Sie im Inforegister **Auftragspositionen** die Option **Bestand \> Reservierung** aus.
1. Wählen Sie auf der Seite **Reservierung** die Option **Los reservieren** aus.
1. Schließen Sie die Seite.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** auf **Lagerortfreigabe**.

    Sie erhalten Informationsnachrichten mit den Wellen- und Lieferungs-IDs, die erstellt wurden. Eine Wiederbeschaffungswelle wird ebenfalls erstellt.

    Sie erhalten außerdem eine Warnmeldung mit dem Titel „Die Arbeits-ID XXXX kann nicht entsperrt werden, da Wiederbeschaffungsarbeiten noch nicht abgeschlossen wurden.“.

#### <a name="view-work-details"></a>Arbeitsdetails anzeigen

1. Wechseln Sie zu **Lagerortverwaltung \> Arbeit \> Arbeitsdetails**.
1. Filtern Sie im Abschnitt **Übersicht** die Spalte **Lagerort** nach dem Lagerort *61*.
1. Es sollten sieben Arbeits-IDs für die drei Bedarfsaufträge erstellt werden.

    - Drei der sieben Arbeits-IDs haben einen **Arbeitsauftragstyp**-Wert von *Wiederbeschaffung* und vier haben einen **Arbeitsauftragstyp**-Wert von *Aufträge*.
    - Alle drei Arbeits-IDs mit einem **Arbeitsauftragstyp**-Wert von *Wiederbeschaffung* weisen dieselben *Entnehmen*- und *Einlagern*-Lagerplätze im Abschnitt **Positionen** auf:

        - **Entnehmen:** *02A01R5S1B*
        - **Einlagern:** *06A01R2S1B*

    - Für Auftrag 1 wurden zwei Arbeits-IDs erstellt.

1. Notieren Sie sich die Arbeits-IDs für die Aufträge.

Abhängig von Ihren Bestandsmengen können die erstellten Arbeitsmengen geringfügig variieren. Insgesamt sollten die erstellten Arbeitskopfzeilen jedoch mit diesem Szenariobeispiel übereinstimmen.

#### <a name="on-hand-inventory-license-plate-id"></a>Bestandskennzeichen-ID

Später in diesem Szenario verwenden Sie die Warehouse Management Mobile App (oder einen Emulator), in der Sie das Kennzeichen identifizieren müssen, um die Kommissionier- und Wiederbeschaffungsszenarien abzuschließen.

Führen Sie die folgenden Schritte aus, um die Kennzeichen-IDs zu finden, die Sie später benötigen.

1. Wechseln Sie zu **Bestandsverwaltung \> Anfragen und Berichte \> Bestandsliste**.
1. Wählen Sie die Schaltfläche **Filter anzeigen** aus, um den Filterbereich zu öffnen.
1. Geben Sie die folgenden Filterkriterien ein, um die Kennzeichen für das Szenario zu erhalten. Verwenden Sie den Filter *beginnt mit*.

    - **Artikelnummer:** *T0100*
    - **Lagerort:** *61*

1. Wählen Sie **Anwenden** aus.
1. Wählen Sie im Aktionsbereich **Dimensionen** aus.
1. Wählen Sie im Dialogfeld **Dimensionsanzeige** im Abschnitt **Lagerdimensionen** alle Werte aus.
1. Wählen Sie im Abschnitt **Buchungen** **Artikelnummer** und **Menge \<\> 0** aus.
1. Wenn Sie fertig sind, wählen Sie **OK** aus, um das Dialogfeld zu schließen.
1. Das Raster **Bestand** zeigt die Kennzeichennummern für den Artikel *T0100* an jedem Lagerplatz an. Notieren Sie sich das Kennzeichen eines jeden Lagerplatzes, da Sie diese Informationen später benötigen.
1. Schließen Sie die Seite.

### <a name="process-steps"></a>Prozessschritte

Sie führen die Lagerplatzwiederbeschaffung für die ersten beiden Arbeits-IDs durch. Die Arbeiten an der dritten Wiederbeschaffungsarbeit werden blockiert, bis der Lagerbestand am Kommissionierort den Schwellenwert unterschreitet.

#### <a name="replenishment"></a>Wiederbeschaffung

1. Melden Sie sich bei der Warehouse Management Mobile App als ein Benutzer im Lagerort *61* an. (Geben Sie *61* als Benutzer-ID und *1* als Passwort ein.)
1. Gehen Sie zu **Lager \> Wiederbeschaffung**.

    Sie werden aufgefordert, die erste Wiederbeschaffungsarbeit abzuschließen. Artikelnummer, -menge und -lagerplatz zur Entnahme werden angezeigt.

1. Geben Sie im Feld **LP** die Kennzeichennummer für den Artikel am angezeigten Lagerplatz ein.
1. Wählen Sie die Schaltfläche **OK** (Häkchensymbol) aus.

    Das System generiert eine Zielkennzeichennummer für das neue Kennzeichen des entnommenen Artikels.

1. Wählen Sie **OK**, um den Wert zu bestätigen.

    Es wird eine Einlagerungsarbeit angezeigt, die den Benutzer anweist, das Zielkennzeichen in den Wiederbeschaffungslagerplatz einzulagern. Der *Einlagern*-Lagerplatz sollte **06A01R2S1B** lauten.

1. Bestätigen Sie die Einlagerungsdetails, und wählen Sie **OK**.

    Sie erhalten die Meldung „Arbeit erledigt“ und die Details der nächsten Wiederbeschaffungsentnahmeaufgabe werden angezeigt: Artikelnummer, -menge und -lagerplatz zur Entnahme. Der Kommissionierort ist derselbe wie der erste Wiederbeschaffungslagerplatz. Daher hat das Kennzeichen dieselbe Kennzeichen-ID, die für die erste Wiederbeschaffungsarbeitsaufgabe verwendet wurde.

1. Wiederholen Sie die vorhergehenden Schritte, um die Wiederbeschaffungsarbeit für die zweite Arbeitsaufgabe abzuschließen. Die Menge und das Zielkennzeichen unterscheiden sich von der Menge und dem Zielkennzeichen für die erste Arbeitsaufgabe.

Nach Abschluss der zweiten Wiederbeschaffungsarbeit erhalten Sie die Meldung „Arbeit abgeschlossen“. Das mobile Gerät informiert Sie auch darüber, dass keine Arbeit verfügbar ist, obwohl noch einige Wiederbeschaffungsarbeiten vorhanden sind. Dieses Verhalten tritt auf, weil die Wiederbeschaffungsarbeit den Verfügbarkeitsstatus *Gehalten* aufweist und daher als **Gesperrt** markiert ist.

Der Status *Gehalten* wurde ausgelöst, weil das Lagerplatzprofil für den Kommissionierstandort, dem die Arbeit zugewiesen ist, einen **Überlaufmenge**-Wert von *0,65 PL* aufweist. Die beiden vorherigen Wiederbeschaffungsarbeitsaufgaben füllten den Lagerplatz fast bis zu seiner Überlaufgrenze für Artikel *T0100*. (Die Einheitenumrechnung für den Artikel ist *1 PL = 100 EA*.) Daher würde die verbleibende Wiederbeschaffungsarbeit dazu führen, dass der Lagerplatz seine Überlaufgrenze überschreitet.

Solange nicht genügend Bestand vom Lagerplatz entnommen wurde, um es unter den Schwellenwert für die Arbeitsfreigabe im Menüelement für mobile Geräte zu bringen, bleibt diese Wiederbeschaffungsarbeit gesperrt.

#### <a name="sales-order-pick"></a>Auftragsentnahme

Bevor die verbleibende Wiederbeschaffungsarbeitsaufgabe abgeschlossen werden kann, muss der Kommissionierort so weit vom Bestand geleert sein, dass die verbleibende Wiederbeschaffungsarbeit entsperrt werden kann. Mit anderen Worten, die Summe aus der Menge des Lagerbestands am Lagerplatz und der Wiederbeschaffungsmenge darf den **Überlaufmenge**-Wert nicht überschreiten. Wenn diese Summe geringer ist als die Überlaufmenge, wird die verbleibende Wiederbeschaffungsarbeit entsperrt.

1. Melden Sie sich bei der Warehouse Management Mobile App als ein Benutzer im Lagerort *61* an. (Geben Sie *61* als Benutzer-ID und *1* als Passwort ein.)
1. Gehen Sie zu **Ausgehend \> Verkaufskommissionierung**.
1. Geben Sie die erste Arbeits-ID für Auftrag 1 ein.

    Auf der Seite **Arbeitsdetails** finden Sie in den Arbeits-IDs, die Sie zuvor notiert haben, Informationen zu Aufträgen. Die hier eingegebene Arbeits-ID generiert eine Kommissionierarbeit für eine Menge von 10 EA an zwei verschiedenen Lagerplätzen.

1. Wählen Sie **OK**.

    Auf der Aufgabenseite **Aufträge: Entnehmen** werden Artikelnummer, -menge und -lagerplatz zur Entnahme für den ersten Lagerplatz angezeigt.

1. Geben Sie im Feld **LP** die Kennzeichennummer für den Artikel am angezeigten Lagerplatz ein.
1. Wählen Sie die Schaltfläche **OK** (Häkchensymbol) aus.

    Auf der Aufgabenseite **Aufträge: Entnehmen** werden Artikelnummer, -menge und -lagerplatz zur Entnahme für den nächsten Lagerplatz angezeigt.

1. Geben Sie im Feld **LP** die Kennzeichennummer für den Artikel am angezeigten Lagerplatz ein.
1. Wählen Sie die Schaltfläche **OK** (Häkchensymbol) aus.

    Die Seite **Aufträge: Einlagern** weist Sie an, beide abgeschlossenen Kommissionierarbeiten an den ausgehenden Bereitstellungslagerplatz zu verschieben.

1. Wählen Sie **OK**.

    Sie erhalten die Nachricht „Arbeit abgeschlossen“.

1. Geben Sie die zweite Arbeits-ID für Auftrag 1 ein.

    Für diese Arbeits-ID gibt es nur eine Entnahmeaufgabe.

1. Wählen Sie **OK**.

    Auf der Aufgabenseite **Aufträge: Entnehmen** werden Artikelnummer, -menge und -lagerplatz zur Entnahme angezeigt.

1. Geben Sie im Feld **LP** die Kennzeichennummer für den Artikel am angezeigten Lagerplatz ein.

    Das von Ihnen angegebene Kennzeichen ist eines der vom System generierten Kennzeichen aus den Wiederbeschaffungsarbeitsaufgaben. Um sicherzustellen, dass Sie die richtige Kennzeichen-ID erfassen, überprüfen Sie auf der Seite **Bestandsliste** den Bestand für Artikel, Lagerplatz und Menge.

1. Wählen Sie die Schaltfläche **OK** (Häkchensymbol) aus.
1. Bestätigen Sie die Anweisungen für die Einlagerungsaufgabe am ausgehenden Bereitstellungslagerplatz.
1. Wählen Sie **OK**.

    Sie erhalten die Nachricht „Arbeit abgeschlossen“.

Auftrag 2 kann nicht kommissioniert werden, da die Wiederbeschaffungsaufgabe, mit der er verknüpft ist, nicht abgeschlossen ist. Derzeit befindet sich am Kommissionierort noch eine Menge von 30 EA, und die Wiederbeschaffungsmenge für Auftrag 2 beträgt 60 EA. Die Summe aus Lagerbestand und Wiederbeschaffungsbestand (90 EA) überschreitet die Überlaufmenge von 0,65 PL (oder 65 EA). Bevor die Wiederbeschaffungsarbeit abgeschlossen werden kann, muss Auftrag 3 kommissioniert werden.

1. Geben Sie die Arbeits-ID für Auftrag 3 ein.

    Für diese Arbeits-ID gibt es nur eine Entnahmeaufgabe.

1. Wählen Sie **OK**.

    Auf der Aufgabenseite **Aufträge: Entnehmen** werden Artikelnummer, -menge und -lagerplatz zur Entnahme angezeigt.

1. Geben Sie im Feld **LP** die Kennzeichennummer für den Artikel am angezeigten Lagerplatz ein.

    Das von Ihnen angegebene Kennzeichen ist eines der vom System generierten Kennzeichen aus den Wiederbeschaffungsarbeitsaufgaben. Um sicherzustellen, dass Sie die richtige Kennzeichen-ID erfassen, überprüfen Sie auf der Seite **Bestandsliste** den Bestand für Artikel, Lagerplatz und Menge.

1. Wählen Sie die Schaltfläche **OK** (Häkchensymbol) aus.
1. Bestätigen Sie die Anweisungen für die Einlagerungsaufgabe am ausgehenden Bereitstellungslagerplatz.
1. Wählen Sie **OK**.

    Sie erhalten die Nachricht „Arbeit abgeschlossen“.

Sobald die Summe der Bestandsmenge am Kommissionierort und der Wiederbeschaffungsmenge unter dem Schwellenwert liegt, können Sie die verbleibenden Wiederbeschaffungsarbeiten bearbeiten.

Gehen Sie zur Seite **Arbeitsdetails** zurück, und beachten Sie, dass die Verfügbarkeit der Wiederbeschaffungsarbeit für den letzten Wiederbeschaffungsteil (für Auftrag 2) *Offen* lautet, weil jetzt genügend Platz am Lagerplatz vorhanden ist, um die Wiederbeschaffung zu akzeptieren.

Sie können diese Wiederbeschaffungsarbeit jetzt über das mobile Gerät bearbeiten.

1. Gehen Sie zu **Lager \> Wiederbeschaffung**.

    Sie werden aufgefordert, die verbleibende Wiederbeschaffungsarbeit abzuschließen. Artikelnummer, -menge und -lagerplatz zur Entnahme werden angezeigt.

1. Geben Sie im Feld **LP** die Kennzeichennummer für den Artikel am angezeigten Lagerplatz ein.
1. Wählen Sie die Schaltfläche **OK** (Häkchensymbol) aus.

    Das System generiert eine Zielkennzeichennummer für das neue Kennzeichen des entnommenen Artikels.

1. Wählen Sie **OK**, um den Wert zu bestätigen.

    Es wird eine Einlagerungsarbeit angezeigt, die den Benutzer anweist, das Zielkennzeichen in den Wiederbeschaffungslagerplatz einzulagern. Der *Einlagern*-Lagerplatz sollte **06A01R2S1B** lauten.

1. Bestätigen Sie die Einlagerungsdetails, und wählen Sie **OK**.

    Sie erhalten die Meldungen „Arbeit erledigt“ und „Keine Arbeit verfügbar“.

Sie können nun Auftrag 2 kommissionieren. Er wurde entsperrt, als die mit dem Auftrag verknüpfte Wiederbeschaffungsarbeit abgeschlossen wurde.

1. Geben Sie die Arbeits-ID für Auftrag 2 ein.

    Für diese Arbeits-ID gibt es nur eine Entnahmeaufgabe.

1. Wählen Sie **OK**.

    Auf der Aufgabenseite **Aufträge: Entnehmen** werden Artikelnummer, -menge und -lagerplatz zur Entnahme angezeigt.

1. Geben Sie im Feld **LP** die Kennzeichennummer für den Artikel am angezeigten Lagerplatz ein.

    Das von Ihnen angegebene Kennzeichen ist das vom System generierte Kennzeichen aus der Wiederbeschaffungsarbeitsaufgabe. Um sicherzustellen, dass Sie die richtige Kennzeichen-ID erfassen, überprüfen Sie auf der Seite **Bestandsliste** den Bestand für Artikel, Lagerplatz und Menge.

1. Wählen Sie die Schaltfläche **OK** (Häkchensymbol) aus.
1. Bestätigen Sie die Anweisungen für die Einlagerungsaufgabe am ausgehenden Bereitstellungslagerplatz.
1. Wählen Sie **OK**.

    Sie erhalten die Nachricht „Arbeit abgeschlossen“.

## <a name="notes-and-tips"></a>Hinweise und Tipps

- Diese Funktionalität funktioniert mit allen Typen der Wiederbeschaffung: Wellenbedarf, Min./Max., Ladungsbedarf und Zuteilung von Zeitfenstern.
- Sie können die Verfügbarkeit der Wiederbeschaffungsarbeit für jede Arbeitskopfzeile aus der Seite **Arbeitsdetails** manuell überschreiben, wenn Sie wollen.
- Wenn das System die Verfügbarkeit der Wiederbeschaffungsarbeiten festlegt, berücksichtigt es alle Bestände, die sich bereits am Lagerplatz befinden, bevor Arbeiten abgeschlossen werden.
- Jeder Teil der Auftragsarbeit ist mit einer bestimmten Wiederbeschaffungsarbeit verknüpft. Es gibt keine entsprechende Verfügbarkeitsfunktion für Verkaufsarbeiten.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]