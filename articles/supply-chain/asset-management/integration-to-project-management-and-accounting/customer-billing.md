---
title: Rechnung für die Wartung von kundeneigenen Anlagen
description: In diesem Thema wird erläutert, wie Sie Wartungsarbeiten erstellen, verarbeiten und abrechnen, die an Anlagen durchgeführt werden, die Ihren Kunden gehören.
author: johanhoffmann
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjInvoiceTable, ProjProjectsListPage, ProjTable, EntAssetWorkOrderType, EntAssetWorkOrderProjectSetup, EntAssetObjectTable, EntAssetWorkOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: a48e681da1801ef3c0d1c9c03cebaa5eecd37d76349a7b1c3cfe53e892fae489
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6774944"
---
# <a name="bill-for-maintenance-on-customer-owned-assets"></a>Rechnung für die Wartung von kundeneigenen Anlagen

[!include [banner](../../includes/banner.md)]

Mit der Funktion *Abrechnung von Arbeitsaufträgen* können Sie Wartungsarbeiten erstellen, verarbeiten und abrechnen, die an Anlagen durchgeführt werden, die Ihren Kunden gehören. Mit dieser Funktion können folgende Aufgaben ausgeführt werden:

- Verbinden Sie Kunden mit den Anlagen, die sie besitzen.
- Wählen Sie einen Kunden aus, und zeigen Sie die Anlagen an, die der Kunde besitzt, wenn Sie einen Arbeitsauftrag erstellen.
- Richten Sie für jeden Kunden ein übergeordnetes Projekt ein.
- Registrieren Sie Stunden, Artikel, Ausgaben und Gebühren für den Arbeitsauftrag und erstellen Sie später einen Rechnungsvorschlag für den Kunden.

Darüber hinaus bietet die Funktion die folgenden Möglichkeiten:

- Der Projektvertrag aus dem übergeordneten Projekt eines Kunden wird automatisch in das entsprechende Arbeitsauftragsprojekt kopiert.
- Die Anlagenverwaltung kann jetzt die Projekttransaktionsart *Gebühr* sowohl für Arbeitsauftragsprognosen als auch für Arbeitsauftragserfassungen verwenden.

## <a name="turn-on-the-customer-billing-feature"></a>Debitorenabrechnungsfunktion aktivieren

Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden. Administratoren können mit den Einstellungen [Funktionsverwaltung](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Modul:** *Projektverwaltung und Buchhaltung*
- **Funktionsname:** *Abrechnung von Arbeitsaufträgen*

## <a name="example-scenario"></a>Beispielszenario

Um zu erfahren, wie diese Funktion funktioniert, arbeiten Sie das folgende Beispielszenario durch.

Um dieses Szenario mithilfe der Beispieldatensätze und -werte, die hier angegeben sind, zu verarbeiten, müssen Sie ein System verwenden, auf dem die standardmäßigen [Demodaten](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) installiert sind. Sie müssen die juristische Person **USMF** auswählen, bevor Sie beginnen.

Sie können dieses Szenario auch als Anleitung zur Verwendung dieser Funktion nutzen, wenn Sie an einem Produktionssystem arbeiten. In diesem Fall müssen Sie jedoch Ihre eigenen Werte ersetzen, und es fehlen möglicherweise einige Typen von erforderlichen Datensätzen, die in den Standarddemodaten enthalten sind.

### <a name="step-1-create-a-new-project-contract-for-the-customer"></a>Schritt 1: Erstellen Sie einen neuen Projektvertrag für den Kunden

1. Wechseln Sie zu **Projektverwaltung und Buchhaltung \> Projekte \> Projektverträge**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie im Dialogfeld **Neuer Projektvertrag** die folgenden Werte fest:

    - **Name:** *Pelican Wholesales*
    - **Finanzierungsart:** *Kunde*
    - **Finanzierungsquelle:** *US-013* (*Pelican Wholesales*)

1. Wählen Sie **OK**.

### <a name="step-2-create-a-new-parent-project-for-the-customer"></a>Schritt 2: Erstellen Sie einen übergeordneten Projektvertrag für den Kunden

Das übergeordnete Projekt, das Sie hier erstellen, wird verwendet, wenn Arbeitsaufträge für den Kunden erstellt werden.

1. Wechseln Sie zu **Projektverwaltung und -verrechnung \> Projekte \> Alle Projekte**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie im Dialogfeld **Neues Projekt** die folgenden Werte fest:

    - **Projekttyp:** *Nach Aufwand*
    - **Projektname:** *Arbeitsaufträge von Pelican Wholesales*
    - **Projektgruppe:** *TM*
    - **Projektvertrags-ID:** *Pelikan Wholesales* (der Vertrag, den Sie zuvor erstellt haben)
    - **Startdatum:** Wählen Sie das heutige Datum aus.

1. Wählen Sie **Projekt erstellen** aus.
1. Das neue Projekt wird geöffnet. Notieren Sie den Wert **Projekt-ID**. Sie müssen ihn später eingeben.

### <a name="step-3-create-a-new-work-order-type-in-asset-management"></a>Schritt 3: Erstellen Sie einen neuen Arbeitsauftragstyp in der Anlagenverwaltung

1. Gehen Sie zu **Anlagenverwaltung \> Einstellungen \> Arbeitsauftrag \> Arbeitsauftragsarten**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Der Liste wird ein neuer Datensatz hinzugefügt. Stellen Sie dafür die folgenden Werte ein:

    - **Arbeitsauftragstyp:** *Service*
    - **Name:** *Servicearbeitsaufträge*
    - **Lebenszyklusstatus von Arbeitsaufträgen:** *Standard*

### <a name="step-4-link-the-customer-account-to-the-parent-project"></a>Schritt 4: Verknüpfen Sie das Kundenkonto mit dem übergeordneten Projekt

Sie müssen jetzt das Kundenkonto mit dem übergeordneten Projekt in den Projekteinstellungen in der Anlagenverwaltung verknüpfen.

1. Gehen Sie zu **Anlagenverwaltung \> Einstellungen \> Arbeitsaufträge \> Projekteinstellungen**.
1. Wählen Sie auf der Registerkarte **Übergeordnetes Projekt** die Option **Hinzufügen** aus, um eine Position hinzuzufügen.
1. Legen Sie die folgenden Werte für die neue Position fest:

    - **Kundenkonto:** *US-013* (*Pelican Wholesales*)
    - **Projekt-ID:** Geben Sie die Projekt-ID ein, die Sie zuvor notiert haben.

### <a name="step-5-link-the-project-group-and-type-to-the-work-order-project"></a>Schritt 5: Verknüpfen Sie die Projektgruppe und geben Sie sie in das Arbeitsauftragsprojekt ein

Sie sollten sich immer noch auf der Seite **Projekteinstellungen** befinden (**Anlagenverwaltung \> Einstellungen \> Arbeitsaufträge \> Projekteinstellungen**).

1. Wählen Sie auf der Registerkarte **Projektgruppe** die Option **Hinzufügen** aus, um eine Position hinzuzufügen.
1. Legen Sie die folgenden Werte für die neue Position fest:

    - **Arbeitsauftragstyp:** *Service* (der Arbeitsauftragstyp, den Sie zuvor erstellt haben)
    - **Projektgruppe:** *TM*

> [!NOTE]
> Der Projektvertrag für das Arbeitsauftragsprojekt wird immer vom übergeordneten Projekt geerbt.

### <a name="step-6-link-an-asset-to-the-customer-id"></a>Schritt 6: Verknüpfen Sie eine Anlage mit der Kunden-ID

1. Wechseln Sie zu **Anlagenverwaltung \> Anlagen \> Aktive Anlagen**.
1. Geben Sie im Feld **Filter** *VE-102* ein, und wählen Sie Filtern nach **Anlage** aus.
1. Wählen Sie die Anlage aus, um ihre Einstellungen zu öffnen.
1. Legen Sie im Inforegister **Kunde** das Feld **Kundenkonto** auf *US-013* (*Pelican Wholesales*) fest.

    Das Feld **Name** wird automatisch in *Pelikan Wholesales* aktualisiert.

### <a name="step-7-create-a-new-work-order-on-the-asset"></a>Schritt 7: Erstellen Sie einen neuen Arbeitsauftrag für die Anlage

1. Gehen Sie zu **Anlagenverwaltung \> Arbeitsaufträge \> Aktive Arbeitsaufträge**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie im Dialogfeld **Arbeitsauftrag erstellen** die folgenden Werte fest:

    - **Arbeitsauftragstyp:** *Service*
    - **Beschreibung:** *LKW reparieren*
    - **Kundenkonto:** *US-013* (*Pelican Wholesales*)
    - **Anlage:** *VE-102*

        > [!NOTE]
        > Die Suche zeigt nur Anlagen an, die mit dem ausgewählten Kundenkonto verknüpft sind.

    - **Wartungsjobtyp:** *Reparatur*
    - **Art:** *Mechaniker*
    - **Servicelevel:** *4*

1. Wählen Sie **OK**.

### <a name="step-8-review-the-work-order-and-start-to-work-on-it"></a>Schritt 8: Überprüfen Sie den Arbeitsauftrag, und beginnen Sie mit der Arbeit

In diesem Abschnitt arbeiten Sie an dem Arbeitsauftrag, den Sie im vorherigen Abschnitt erstellt haben.

1. Befolgen Sie diese Schritte, um zu überprüfen, ob das übergeordnete Projekt das Projekt *Arbeitsaufträge von Pelican Wholesales* ist:

    1. Wählen Sie im Abschnitt **Wartungsaufträge für Arbeitsaufträge** eine Position aus.
    1. Überprüfen Sie auf dem Inforegister **Positionsdetails** den Wert **Projekt-ID**. Es sollte eine Zahl mit Bindestrich im Format *\<Parent-Project-ID\>-\<Project-ID\>* sein. Dieser Wert ist ein Link.
    1. Wählen Sie den Projekt-ID-Link aus, um eine Seite zu öffnen, auf der Sie die Namen des übergeordneten Projekts und des Projekts anzeigen können.

1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Arbeitsauftrag** in der Gruppe **Lebenszyklusstatus** die Option **Arbeitsauftragsstatus aktualisieren**.
1. Wählen Sie im Dialogfeld **Arbeitsauftragsstatus aktualisieren** in der Spalte **Auswählen** das Kontrollkästchen für die Zeile, in der das Feld **Lebenszyklusstatus** auf *In Bearbeitung* gesetzt ist.
1. Wählen Sie **OK**.
1. Wählen Sie im Dialogfeld **Lebenszyklusstatus: In Bearbeitung** **OK** aus.

### <a name="step-9-post-the-hours-that-were-spent-on-the-work-order-and-create-a-new-invoice-proposal"></a>Schritt 9: Buchen Sie die Stunden, die für den Arbeitsauftrag aufgewendet wurden, und erstellen Sie einen neuen Rechnungsvorschlag

In diesem Abschnitt arbeiten Sie an dem Arbeitsauftrag, an dem Sie im vorherigen Abschnitt gearbeitet haben.

1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Arbeitsauftrag** in der Gruppe **Projekt** auf **Erfassungen**.

    Die Seite **Arbeitsauftragserfassungen** wird angezeigt. Hier können Sie die Zeit registrieren, die Sie für den Arbeitsauftrag aufgewendet haben.

1. Wählen Sie auf dem Inforegister **Stunden** die Option **Position hinzufügen** aus.
1. Stellen Sie in der neuen Zeile das Feld **Stunden** auf *4* ein.
1. Wählen Sie im Aktionsbereich **Erfassungen buchen** aus.
1. Schließen Sie die Seite **Arbeitsauftragserfassungen**, um zum Arbeitsauftrag zurückzukehren.
1. Klicken Sie im Aktivitätsbereich auf die Registerkarte **Rechnungsstellung**, und wählen Sie **Neuer Rechnungsvorschlag** aus.
1. Aktivieren Sie im Dialogfeld **Rechnungsvorschlag erstellen** im Abschnitt **Projektbuchungen** das Kontrollkästchen **Auswählen** für jede Zeile, die Sie in Rechnung stellen möchten.
1. Wählen Sie **OK** aus, um das Dialogfeld zu schließen und den neuen Rechnungsvorschlag anzuzeigen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]