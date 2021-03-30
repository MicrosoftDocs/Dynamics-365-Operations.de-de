---
title: Schwellenwert für Zonenwiederbeschaffung
description: Die zonenbasierte Wiederbeschaffung verwendet eine minimale/maximale (min/max) Wiederbeschaffungsstrategie, bewertet jedoch ganze Lagerortzonen anstelle nur einzelner Lagerplätze. Daher können Lagerverwalter schneller erkennen, wann in einer Kommissionierzone zusätzlicher Bestand erforderlich ist.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocDirHint, WHSLocDirTable, WHSRequestType
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6aaa139fb206c035b25b7056e681d086fde6447f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245057"
---
# <a name="zone-threshold-replenishment"></a>Schwellenwert für Zonenwiederbeschaffung

[!include [banner](../includes/banner.md)]

Die zonenbasierte Wiederbeschaffung verwendet eine minimale/maximale (min/max) Strategie zur [Wiederbeschaffung](replenishment.md), bewertet jedoch ganze Lagerortzonen anstelle nur einzelner Lagerplätze. Daher können Lagerverwalter schneller erkennen, wann in einer Kommissionierzone zusätzlicher Bestand erforderlich ist.

Das Setup für diese Funktion ähnelt dem Setup für die lagerplatzbasierte Wiederbeschaffung. Wenn Sie jedoch eine Vorlage für die minimale/maximale Wiederbeschaffung einrichten, können Sie auch angeben, ob der Schwellenwert pro Lagerplatz oder pro Zone ausgewertet werden soll. Wenn Sie eine Bewertung einrichten, die auf Zonen basiert, müssen Sie der Zonenauswahlabfrage bestimmte Zonen hinzufügen.

Wie bei der lagerplatzbasierten Min./Max.-Wiederbeschaffung basiert die zonenbasierte Min./Max.-Wiederbeschaffung auf dem Setup eines Mindestbestandsschwellenwerts, der die Erstellung von Wiederbeschaffungsarbeiten für ausgewählte Artikel auslöst. Durch diese Wiederbeschaffungsarbeiten wird der Lagerbestand auf den angegebenen Höchstschwellenwert für die Zone erhöht.

> [!NOTE]
> Zonenwiederbeschaffungsprozesse für Produktvarianten werden in der aktuellen Version nicht unterstützt.


Im Gegensatz zur lagerplatzbasierten Min./Max.-Wiederbeschaffung sind für die zonenbasierte Min./Max.-Wiederbeschaffung keine festen Lagerplätze erforderlich, um zu bewerten, ob Lagerplätze einen bestimmten Artikel speichern sollen. Daher können Sie bei zonenbasierter Wiederbeschaffung die Min./Max.-Wiederbeschaffung verwenden, auch wenn Sie nicht für jeden Artikel oder jede Artikelvariante im Lagerort feste Lagerplätze haben. Wenn eine Menge in der Zone den angegebenen Mindestschwellenwert unterschreitet, werden Wiederbeschaffungsarbeiten erstellt. Lagerplatzrichtlinien bestimmen, an welchem bestimmten Lagerplatz der Bestand eingelagert werden soll.

## <a name="turn-on-the-zone-threshold-replenishment-feature"></a>Funktion für Schwellenwert für Zonenwiederbeschaffung aktivieren

Bevor Sie die Funktion *Schwellenwert für Zonenwiederbeschaffung* verwenden können, muss sie in Ihrem System aktiviert sein. Administratoren können mit den Einstellungen in der [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie gegebenenfalls aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Module:** *Lagerortverwaltung*
- **Funktionsname:** *Schwellenwert für Zonenwiederbeschaffung*

## <a name="set-up-zone-based-replenishment"></a><a name="setup"></a>Zonenbasierte Wiederbeschaffung einrichten

Um die zonenbasierte Wiederbeschaffung einzurichten, müssen Sie mehrere Teile des Systems konfigurieren. In diesem Abschnitt werden die verschiedenen Einstellungen vorgestellt und Demodatenwerte bereitgestellt, die Sie eingeben können, wenn Sie das Szenario am Ende dieses Themas durcharbeiten möchten.

### <a name="set-up-directive-codes"></a>Richtliniencodes einrichten

Mit [Richtliniencodes](control-warehouse-location-directives.md) können Sie genauer sein, wenn Sie die Lagerplatzvorlage definieren, die in einer Arbeitsvorlage verwendet wird. Jeder Code legt einen gemeinsamen Wert fest, auf den Sie sich bei der Konfiguration der einzelnen Vorlagentypen beziehen können.

#### <a name="view-and-edit-directive-codes"></a>Richtliniencodes anzeigen und bearbeiten

Um Ihre Richtliniencodes anzuzeigen oder zu bearbeiten, gehen Sie zu **Lagerortverwaltung \> Setup \> Richtliniencodes**.

#### <a name="prepare-demo-data-directive-codes"></a>Demodaten-Richtliniencodes vorbereiten

Dieses Beispiel zeigt, wie ein Richtliniencode vorbereitet wird. Wenn Sie das Szenario am Ende dieses Themas durcharbeiten möchten, verwenden Sie die hier angegebenen Demodatenwerte. Verwenden Sie andernfalls Ihre eigenen Werte.

1. Wählen Sie **USMF** juristische Person aus, um mit den Demodaten zu arbeiten.
1. Wechseln Sie zu **Lagerortverwaltung \> Setup \> Richtliniencodes**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Zeile zum Raster hinzuzufügen.
1. Legen Sie in der neuen Zeile die folgenden Werte fest:

    - **Richtliniencode:** _Zonenwiederb._
    - **Richtlinienbeschreibung:** _Zonenwiederbeschaffung_

1. Wählen Sie **Speichern** aus, um den neuen Code zu speichern.

### <a name="set-up-replenishment-templates"></a>Wiederbeschaffungsvorlagen einrichten

[Min./Max.-Wiederbeschaffungsvorlagen](tasks/set-up-min-max-replenishment-process.md) sind der Hauptmechanismus zur Verwaltung optimaler Level in Entnahmeorten. In diesen Vorlagen müssen Sie die Regeln festlegen, nach denen der Bestand im Lagerort aufgefüllt wird. Die Wiederbeschaffung, für die die Vorlagen verwendet werden können, umfasst die zonenbasierte Wiederbeschaffung.

#### <a name="view-and-edit-replenishment-templates"></a>Wiederbeschaffungsvorlagen anzeigen und bearbeiten

Eine Wiederbeschaffungsvorlage ist eine Reihe von Regeln, die steuern, wann und wie ein Lagerplatz aufgefüllt wird. Sie wählen eine Vorlage aus, um zu steuern, wann und wie die Wiederbeschaffung erfolgt. Um Wiederbeschaffungsvorlagen anzuzeigen und zu bearbeiten, gehen Sie zu **Lagerortverwaltung \> Setup \> Wiederbeschaffung \> Wiederbeschaffungsvorlagen**.

#### <a name="prepare-a-demo-data-replenishment-template"></a>Demodaten-Wiederbeschaffungsvorlage vorbereiten

Dieses Beispiel zeigt, wie eine Wiederbeschaffungsvorlage vorbereitet wird. Wenn Sie das Szenario am Ende dieses Themas durcharbeiten möchten, verwenden Sie die hier angegebenen Demodatenwerte. Verwenden Sie andernfalls Ihre eigenen Werte.

1. Wählen Sie **USMF** juristische Person aus, um mit den Demodaten zu arbeiten.
1. Wechseln Sie zu **Lagerortverwaltung \> Setup \> Wiederbeschaffung \> Wiederbeschaffungsvorlagen**.
1. Klicken Sie auf **Bearbeiten**, um die Seite in den Bearbeitungsmodus zu versetzen.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um dem Raster **Übersicht** eine Zeile hinzuzufügen.
1. Legen Sie in der neuen Zeile die folgenden Werte fest. Akzeptieren Sie die Standardwerte für alle anderen Felder.

    - **Wiederbeschaffungsvorlage:** _Min./Max.-Zonenwiederb._
    - **Beschreibung:** _Min./Max.-Zonenwiederbeschaffung_
    - **Wiederbeschaffungstyp:** _Minimum oder Maximum_

1. Wählen Sie **Speichern** aus.
1. Während die neue Zeile noch im Raster **Übersicht** ausgewählt ist, wählen Sie **Neu** über dem Raster **Wiederbeschaffungsvorlagendetails** aus, um eine Zeile hinzuzufügen, die der Wiederbeschaffungsvorlage *Min./Max.-Zonenwiederb.* zugeordnet ist, die Sie gerade erstellt haben.
1. Legen Sie in der neuen Zeile die folgenden Werte fest:

    - **Sequenznummer:** Geben Sie _1_ ein.
    - **Beschreibung:** Geben Sie _Entnahmezonenwiederbeschaffung_ ein.
    - **Wiederbeschaffungseinheit:** Wählen Sie _EA_ aus.
    - **Anforderungstyp:** Lassen Sie dieses Feld leer.
    - **Richtliniencode:** Dieses Feld verknüpft die Wiederbeschaffungsvorlage mit einer Lagerplatzrichtlinie. Wählen Sie den zuvor erstellten Demodaten-Richtliniencode (_Zonenwiederb._) aus.
    - **Arbeitsvorlage:** Lassen Sie dieses Feld leer.
    - **Mindestmenge:** In diesem Feld wird die Menge festgelegt, bei der die Wiederbeschaffung ausgelöst wird. Geben Sie _50_ ein.
    - **Höchstmenge:** In diesem Feld wird die maximale Menge eines Artikels festgelegt, die in einer Zone vorhanden sein kann. Durch generierte Wiederbeschaffungsarbeiten wird der Lagerbestand auf diese Menge erhöht. Geben Sie _150_ ein.
    - **Einheit:** In diesem Feld wird die Einheit für die Mindest- und Höchstwerte festgelegt. Wählen Sie _EA_ aus.
    - **Bedarfserhöhung:** Wählen Sie _Aufrunden_ aus.
    - **Leere feste Lagerplätze auffüllen:** Aktivieren Sie dieses Kontrollkästchen.
    - **Nur feste Lagerplätze auffüllen:** Deaktivieren Sie dieses Kontrollkästchen.
    - **Produktabfragemodus:** Wählen Sie _Produktabfrage_ aus.
    - **Wiederbeschaffungsschwellenbereich:** In diesem Feld wird festgelegt, ob die Vorlage nach Zone oder nach bestimmtem Lagerplatz ausgewertet werden soll. Wählen Sie _Zone_ aus.
    - **Lagerort:** Wählen Sie _61_ aus.

1. Wählen Sie **Produkte auswählen** über dem Raster **Wiederbeschaffungsvorlagendetails** aus.
1. Wählen Sie im Dialogfeld **Produktabfrage** auf der Registerkarte **Bereich** die Option **Hinzufügen** aus, um dem Raster eine Zeile hinzuzufügen.
1. Legen Sie in der neuen Zeile die folgenden Werte fest:

    - **Tabelle:** _Artikel_
    - **Abgeleitete Tabelle:** _Artikel_
    - **Feld:** _Artikelnummer_
    - **Kriterien:** _A0001_

1. Wählen Sie **OK** aus, um die Abfrage zu speichern und das Dialogfeld zu schließen.
1. Wählen Sie **Zonen zum Auffüllen auswählen** über dem Raster **Wiederbeschaffungsvorlagendetails** aus.
1. Fügen Sie im Dialogfeld **Zonenabfrage** auf der Registerkarte **Bereich** eine Zeile zum Raster hinzu.
1. Legen Sie in der neuen Zeile die folgenden Werte fest:

    - **Tabelle:** _Lagerortzone_
    - **Abgeleitete Tabelle:** _Lagerortzone_
    - **Feld:** _Zonen-ID_
    - **Kriterien:** _BODEN_

1. Wählen Sie **OK** aus, um die Abfrage zu speichern und das Dialogfeld zu schließen.

### <a name="set-up-location-directives"></a>Lagerplatzrichtlinien einrichten

Im Gegensatz zur standortbasierten Min./Max.-Wiederbeschaffung müssen Sie bei der zonenbasierten Min./Max.-Wiederbeschaffung sowohl Entnahmelagerplatzrichtlinien als auch Einlagerungslagerplatzrichtlinien einrichten, da das System die gesamte Zone und nicht nur den Entnahmelagerplatz für ausgehende Arbeiten auswertet.

#### <a name="view-and-edit-location-directives"></a>Lagerplatzrichtlinien anzeigen und bearbeiten

Um Ihre Lagerplatzrichtlinien anzuzeigen oder zu bearbeiten, gehen Sie zu **Lagerortverwaltung \> Setup \> Lagerplatzrichtlinien**.

Beispiele, die zeigen, wie Sie die Einstellungen zum Erstellen der erforderlichen Entnahmelagerplatzrichtlinien und Einlagerungslagerplatzrichtlinien verwenden, finden Sie im nächsten Abschnitt.

#### <a name="prepare-demo-data-location-directives"></a>Demodaten-Lagerplatzrichtlinien vorbereiten

Um Demodaten so vorzubereiten, dass sie im Szenario am Ende dieses Themas verwendet werden können, müssen Sie zwei Lagerplatzrichtlinien erstellen: eine für die Entnahme und eine für die Einlagerung.

##### <a name="create-a-replenishment-pick-directive"></a>Wiederbeschaffungsentnahmerichtlinie erstellen

1. Wählen Sie **USMF** juristische Person aus, um mit den Demodaten zu arbeiten.
1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerplatzrichtlinien**.
1. Legen Sie im linken Bereich im Feld **Arbeitsauftragstyp** _Wiederbeschaffung_ fest.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine neue Richtlinie zu erstellen.
1. Legen Sie die folgenden Werte fest:

    - **Sequenznummer:** Akzeptieren Sie den Standardwert.
    - **Name:** Geben Sie _Zonenentnahme_ ein.
    - **Arbeitstyp:** Wählen Sie _Entnahme_ aus.
    - **Standort:** Wählen Sie _6_ aus.
    - **Lagerort:** Wählen Sie _61_ aus.
    - **Richtliniencode:** Lassen Sie dieses Feld leer.
    - **Multi-SKU:** Setzen Sie diese Option auf _Nein_.

1. Wählen Sie **Speichern** aus, um eine Richtlinie zu erstellen, die die Einstellungen enthält, die Sie bisher konfiguriert haben.
1. Wählen Sie im Inforegister **Positionen** die Option **Neu** aus, um dem Raster eine Position hinzuzufügen.
1. Legen Sie die folgenden Werte für die neue Position fest:

    - **Sequenznummer:** Geben Sie _1_ ein.
    - **Von Menge:** Geben Sie _0_ ein.
    - **Zu Menge:** Geben Sie _10000000_ ein.
    - **Einheit:** Lassen Sie dieses Feld leer.
    - **Menge ermitteln:** Wählen Sie _Keine_ aus.
    - **Nach Einheit einschränken:** Deaktivieren Sie dieses Kontrollkästchen.
    - **Auf Einheit aufrunden:** Deaktivieren Sie dieses Kontrollkästchen.
    - **Verpackungsmenge ermitteln:** Deaktivieren Sie dieses Kontrollkästchen.
    - **Teilen zulassen:** Aktivieren Sie dieses Kontrollkästchen.

1. Wählen Sie **Speichern** aus, um die neue Position zu speichern.
1. Während Ihre neue Position noch im Raster **Positionen** ausgewählt ist, wählen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** **Neu** aus, um dem Raster eine Zeile hinzuzufügen.
1. Legen Sie in der neuen Zeile die folgenden Werte fest:

    - **Sequenznummer:** Geben Sie _1_ ein.
    - **Name:** Geben Sie _Entnahme aus Bulk_ ein.
    - **Feste Standortnutzung:** Wählen Sie _Feste und nicht feste Lagerplätze_ aus.
    - **Negativen Lagerbestand zulassen:** Deaktivieren Sie dieses Kontrollkästchen.
    - **Charge aktiviert:** Deaktivieren Sie dieses Kontrollkästchen.
    - **Strategie:** Wählen Sie _Keine_ aus.

1. Wählen Sie **Speichern** aus, um die neue Aktivität zu speichern.
1. Während Ihre neue Aktivität noch ausgewählt ist, wählen Sie **Abfrage bearbeiten** über dem Raster **Lagerplatzrichtlinienaktivitäten** aus.
1. Ein Abfragedialogfeld wird angezeigt, in dem Sie die Lagerplätze auswählen können, aus denen nachgefüllt werden soll. Wählen Sie auf der Registerkarte **Bereich** die Option **Hinzufügen** aus, um dem Raster eine Zeile hinzuzufügen.
1. Legen Sie in der neuen Zeile die folgenden Werte fest:

    - **Tabelle:** _Lagerorte_
    - **Abgeleitete Tabelle:** _Lagerorte_
    - **Feld:** _Zonen-ID_
    - **Kriterien:** _BULK_

1. Wählen Sie **OK** aus, um die Abfrage zu speichern und das Dialogfeld zu schließen.
1. Wählen Sie **Speichern** aus, um Ihre Lagerplatzrichtlinie zu speichern.

##### <a name="create-a-replenishment-put-directive"></a>Wiederbeschaffungseinlagerungsrichtlinie erstellen

1. Stellen Sie im linken Bereich auf der Seite **Lagerplatzrichtlinien** sicher, dass das Feld **Arbeitsauftragstyp** immer noch auf _Wiederbeschaffung_ festgelegt ist.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine weitere neue Richtlinie zu erstellen.
1. Legen Sie die folgenden Werte fest:

    - **Sequenznummer:** Akzeptieren Sie den Standardwert.
    - **Name:** Geben Sie _Zoneneinlagerung_ ein.
    - **Arbeitsauftragstyp:** Wählen Sie _Einlagern_ aus.
    - **Standort:** Wählen Sie _6_ aus.
    - **Lagerort:** Wählen Sie _61_ aus.
    - **Richtliniencode:** Wählen Sie _Zonenwiederb._ aus, um diese Lagerplatzrichtlinie mit der zuvor erstellten Wiederbeschaffungsvorlage zu verknüpfen, indem Sie den zuvor erstellten Code verwenden.
    - **Multi-SKU:** Setzen Sie diese Option auf _Nein_.

1. Wählen Sie **Speichern** aus, um eine Richtlinie zu erstellen, die die Einstellungen enthält, die Sie bisher konfiguriert haben.
1. Wählen Sie im Inforegister **Positionen** die Option **Neu** aus, um dem Raster eine Position hinzuzufügen.
1. Legen Sie die folgenden Werte für die neue Position fest:

    - **Sequenznummer:** Geben Sie _1_ ein.
    - **Von Menge:** Geben Sie _0_ ein.
    - **Zu Menge:** Geben Sie _10000000_ ein.
    - **Einheit:** Lassen Sie dieses Feld leer.
    - **Menge ermitteln:** Wählen Sie _Keine_ aus.
    - **Nach Einheit einschränken:** Deaktivieren Sie dieses Kontrollkästchen.
    - **Auf Einheit aufrunden:** Deaktivieren Sie dieses Kontrollkästchen.
    - **Verpackungsmenge ermitteln:** Deaktivieren Sie dieses Kontrollkästchen.
    - **Teilen zulassen:** Aktivieren Sie dieses Kontrollkästchen.

1. Wählen Sie **Speichern** aus, um die neue Position zu speichern.
1. Während Ihre neue Position noch im Raster **Positionen** ausgewählt ist, wählen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** **Neu** aus, um dem Raster eine Zeile hinzuzufügen.
1. Legen Sie in der neuen Zeile die folgenden Werte fest:

    - **Sequenznummer:** Geben Sie _1_ ein.
    - **Name:** Geben Sie _Zoneneinlagerung_ ein.
    - **Feste Standortnutzung:** Wählen Sie _Feste und nicht feste Lagerplätze_ aus.
    - **Negativen Lagerbestand zulassen:** Deaktivieren Sie dieses Kontrollkästchen.
    - **Charge aktiviert:** Deaktivieren Sie dieses Kontrollkästchen.
    - **Strategie:** Wählen Sie _Konsolidieren_ aus.

1. Wählen Sie **Speichern** aus, um die neue Aktivität zu speichern.
1. Während Ihre neue Aktivität noch ausgewählt ist, wählen Sie **Abfrage bearbeiten** über dem Raster **Lagerplatzrichtlinienaktivitäten** aus.
1. Ein Abfragedialogfeld wird angezeigt, in dem Sie die Zone auswählen können, an denen nachgefüllt werden soll. Diese Zone sollte dieselbe Zone sein, die in der Wiederbeschaffungsvorlage angegeben ist. Wählen Sie auf der Registerkarte **Bereich** die Option **Hinzufügen** aus, um dem Raster eine Zeile hinzuzufügen.
1. Legen Sie in der neuen Zeile die folgenden Werte fest:

    - **Tabelle:** _Lagerorte_
    - **Abgeleitete Tabelle:** _Lagerorte_
    - **Feld:** _Zonen-ID_
    - **Kriterien:** _BODEN_

1. Wählen Sie **OK** aus, um die Abfrage zu speichern und das Dialogfeld zu schließen.
1. Wählen Sie **Speichern** aus, um Ihre Lagerplatzrichtlinie zu speichern.

## <a name="scenario"></a>Szenario

Dieser Abschnitt enthält ein Beispielszenario, das zeigt, wie Sie mit der Funktion arbeiten.

### <a name="prepare-the-sample-data-that-is-required-for-the-sample-scenario"></a>Beispieldaten vorbereiten, die für das Beispielszenario erforderlich sind

Bevor Sie mit der Bearbeitung des Szenarios beginnen, müssen Sie Beispieldaten aktivieren und die Funktion wie in diesem Abschnitt und in den vorherigen Abschnitten dieses Themas beschrieben einrichten.

#### <a name="use-the-usmf-legal-entity"></a>USMF juristische Person verwenden

Um das Szenario mithilfe der Beispieldatensätze und -werte, die hier angegeben sind, zu verarbeiten, müssen Sie ein System verwenden, auf dem die standardmäßigen [Demodaten](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) installiert sind. Außerdem müssen Sie die **USMF** juristische Person auswählen, bevor Sie beginnen.

#### <a name="prepare-additional-sample-data"></a>Zusätzliche Beispieldaten vorbereiten

Nachdem Sie die **USMF** juristische Person ausgewählt haben, fügen Sie die zusätzlichen Beispieldaten hinzu, die erforderlich sind, wie im Abschnitt [Zonenbasierte Wiederbeschaffung einrichten](#setup) weiter oben in diesem Thema beschrieben.

#### <a name="check-your-on-hand-inventory"></a>Verfügbaren Lagerbestand prüfen

Befolgen Sie diese Schritte, um sicherzustellen, dass Ihr System genügend Bestand enthält, um das Beispielszenario zu unterstützen.

1. Stellen Sie sicher, dass Bestand für den Artikel *A0001* an zwei verschiedenen Lagerplätzen in der Kommissionierzone (*BODEN*) vorhanden ist, wie in der Wiederbeschaffungsvorlage angegeben ist. Der Gesamtbestand sollte jedoch unter der erforderlichen Mindestmenge liegen (*50*), wie in der Wiederbeschaffungsvorlage angegeben ist. Auf diese Weise können Sie simulieren, wie die Berechnung für die gesamte Zone und nicht nur für einen einzelnen Lagerplatz erfolgt. **Verwenden Sie einen der Lagerortprozesse, um den Lagerbestand nach Bedarf anzupassen.**
1. Stellen Sie sicher, dass genügend Bestand für den Artikel *A0001* an einem Bulk-Lagerplatz vorhanden ist, der in der Zonenentnahmelagerplatzrichtlinie angegeben ist, an dem die Wiederbeschaffungsarbeiten die Artikel aus der Zonen-ID *BULK* entnehmen sollen. Der Gesamtbestand muss über der erforderlichen Höchstmenge liegen (*150*), wie in der Wiederbeschaffungsvorlage angegeben ist.
1. Optional, aber empfohlen: Führen Sie die folgenden Schritte aus, um eine Bestandsanpassungserfassung zu erstellen:

    1. Wechseln Sie zu **Bestandsverwaltung \> Erfassungseinträge \> Artikel \> Bestandsanpassung**.
    1. Wählen Sie **Neu** aus.
    1. Wählen Sie im Dialogfeld **Bestandserfassung erstellen** im Feld **Lagerort** *61* aus.
    1. Wählen Sie **OK**.
    1. Verwenden Sie im Inforegister **Erfassungspositionen** die Schaltfläche **Neu**, um dem Raster drei Positionen hinzuzufügen, und legen Sie die folgenden Werte fest. Nachdem Sie jede Position eingerichtet haben, wählen Sie **Speichern** aus.

        - **Position 1:**

            - **Artikelnummer** *A001*
            - **Standort:** *6*
            - **Lagerort:** *61*
            - **Lagerplatz:** *02A01R1S1B*
            - **Kennzeichen:** Wählen Sie ein vorhandenes Kennzeichen in der Liste aus, oder erstellen Sie ein neues Kennzeichen.
            - **Menge** *1000*

        - **Position 2:**

            - **Artikelnummer** *A001*
            - **Standort:** *6*
            - **Lagerort:** *61*
            - **Lagerplatz:** *07A01R2S1B*
            - **Kennzeichen:** Wählen Sie ein vorhandenes Kennzeichen in der Liste aus, oder erstellen Sie ein neues Kennzeichen.
            - **Menge** *15*

        - **Position 3:**

            - **Artikelnummer** *A001*
            - **Standort:** *6*
            - **Lagerort:** *61*
            - **Lagerplatz:** *07A01R1S1B*
            - **Kennzeichen:** Wählen Sie ein vorhandenes Kennzeichen in der Liste aus, oder erstellen Sie ein neues Kennzeichen.
            - **Menge** *10*

    1. Wählen Sie im Aktivitätsbereich **Überprüfen** aus. Beheben Sie alle gefundenen Fehler, bevor Sie mit dem nächsten Schritt fortfahren.
    1. Wählen Sie im Aktivitätsbereich **Buchen** aus, um den Bestand in den Lagerort zu buchen.

### <a name="sample-scenario-run-zone-based-minmax-replenishment"></a>Beispielszenario: Zonenbasierte minimale/maximale Wiederbeschaffung ausführen

Nachdem alle erforderlichen Beispieldaten vorhanden sind, können Sie die Wiederbeschaffung auslösen, indem Sie die folgenden Schritte ausführen.

1. Wechseln Sie zu **Lagerortverwaltung \> Wiederbeschaffung \> Wiederbeschaffungen**.
1. Wählen Sie im Dialogfeld **Wiederbeschaffung** im Inforegister **Einzuschließende Datensätze** **Filter** aus.
1. Bearbeiten Sie im Dialogfeld **Anfrage** auf der Registerkarte **Bereich** die Standardtabellenzeile folgendermaßen:

    - **Tabelle:** Wählen Sie _Wiederbeschaffungsvorlagen_ aus.
    - **Abgeleitete Tabelle:** Wählen Sie _Wiederbeschaffungsvorlagen_ aus.
    - **Feld:** Wählen Sie _Wiederbeschaffungsvorlage_ aus.
    - **Kriterien:** Wählen Sie _Min./Max.-Zonenwiederb._ aus. Diese Wiederbeschaffungsvorlage ist die Wiederbeschaffungsvorlage, die Sie erstellt haben, als Sie die Demodaten für dieses Szenario vorbereitet haben.

1. Wählen Sie **OK** aus, um die Abfrage zu speichern und zurück zum Dialogfeld **Wiederbeschaffung** zu gelangen.
1. Wählen Sie **OK** aus, um die Wiederbeschaffungsvorlage auszuführen.

Wiederbeschaffungsarbeiten werden jetzt erstellt, um Bestand aus der *BULK*-Zone zu entnehmen und ihn in die *BODEN*-Zone aufzufüllen.

## <a name="notes-and-tips"></a>Hinweise und Tipps

Hier sind einige Hinweise und Tipps zum Arbeiten mit der Funktion:

- Um Wiederbeschaffungsarbeiten einzurichten, die in die gewünschte Zone gehen, können Sie die Wiederbeschaffungsvorlagenpositionen und Lagerplatzrichtlinien auf eine der folgenden Arten verknüpfen:

    - Bearbeiten Sie die Header-Abfrage der Lagerplatzrichtlinie, und filtern Sie die ausgewählten Wiederbeschaffungsvorlagenpositionen.
    - Verwenden Sie einen Richtliniencode in der Wiederbeschaffungsvorlagenposition, und gleichen Sie ihn mit der Einlagerungslagerplatzrichtlinie ab.

- Wenn Sie dynamische Lagerplätze verwenden, werden Wiederbeschaffungsarbeiten entweder für den ersten verfügbaren Lagerplatz oder für einen Lagerplatz erstellt, der bereits Bestand enthält, wenn die Lagerplatzrichtlinienaktivität für die Verwendung der Strategie **Konsolidieren** eingerichtet ist.
- Wenn Sie feste Lagerplätze anstelle von Zonen verwenden, sollten Sie die [Min./Max.-Standardwiederbeschaffung](tasks/set-up-min-max-replenishment-process.md) verwenden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]