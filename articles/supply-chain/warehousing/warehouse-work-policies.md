---
title: Arbeitsrichtlinien
description: In diesem Thema wird erläutert, wie Sie Arbeitsrichtlinien einrichten.
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 39a9ba00763fac220eff16bdd42aa07cc8e35ba4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838129"
---
# <a name="work-policies"></a>Arbeitsrichtlinien

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie das System und die Warehouse Management Mobile App so einrichten, dass sie Arbeitsrichtlinien unterstützen. Mit dieser Funktion können Sie schnell Bestand registrieren, ohne Einlagerungsarbeiten zu erstellen, wenn Sie Kauf- oder Umlagerungsaufträge erhalten oder wenn Sie Fertigungsprozesse abschließen. Dieses Thema enthält allgemeine Informationen. Ausführliche Informationen zum Kennzeichenempfang finden Sie unter [Kennzeichenempfang über die Warehouse Management Mobile App](warehousing-mobile-device-app-license-plate-receiving.md).

Eine Arbeitsrichtlinie steuert, ob Lagerortarbeit erstellt wird, wenn ein hergestellter Artikel als fertig gemeldet wird oder wenn Waren über die Warehouse Management Mobile App empfangen werden. Sie richten jede Arbeitsrichtlinie ein, indem Sie die Bedingungen definieren, unter denen sie gilt: die Arbeitsauftragstypen und -prozesse, den Lagerort und (optional) die Produkte. Zum Beispiel muss eine Bestellung für Produkt *A0001* am Lagerplatz *RECV* im Lagerort *24* empfangen werden. Später wird das Produkt in einem anderen Prozess am Lagerplatz *RECV* verbraucht. In diesem Fall können Sie eine Arbeitsrichtlinie einrichten, um zu verhindern, dass Einlagerungsarbeiten erstellt werden, wenn ein Mitarbeiter Produkt *A0001* am Lagerplatz *RECV* als erhalten meldet.

> [!NOTE]
> - Damit eine Arbeitsrichtlinie aktiv ist, müssen Sie mindestens einen Lagerplatz für die Arbeitsrichtlinie im Inforegister **Lagerorte** der Seite **Arbeitsrichtlinien** definieren. 
> - Sie können nicht denselben Speicherort für mehrere Arbeitsrichtlinien angeben.
> - Die Option **Etikett drucken** für Menüpunkte für mobile Geräte druckt kein Kennzeichenetikett ohne Arbeitserstellung.

## <a name="activate-the-features-in-your-system"></a>Funktionen im System aktivieren

Aktivieren Sie die folgenden beiden Funktionen in [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), um alle in diesem Thema beschriebenen Funktionen in Ihrem System verfügbar zu machen.

- Kennzeichenempfang und Verbesserungen
- Arbeitsrichtlinienverbesserungen für eingehende Arbeit

## <a name="the-work-policies-page"></a>Seite „Arbeitsrichtlinien“

Um Arbeitsrichtlinien einzurichten, gehen Sie zu **Lagerortverwaltung \> Einrichtung \> Arbeit \> Arbeitsrichtlinien**. Legen Sie dann auf jedem Inforegister die Felder wie in den folgenden Unterabschnitten beschrieben fest.

### <a name="the-work-order-types-fasttab"></a>Inforegister „Arbeitsauftragstypen“

Fügen Sie auf dem Inforegister **Arbeitsauftragstypen** alle Arbeitsauftragstypen und die zugehörigen Arbeitsprozesse hinzu, für die die Arbeitsrichtlinie gilt. Die folgenden Arbeitsauftragstypen und zugehörigen Arbeitsprozesse werden für Arbeitsrichtlinien unterstützt.

| Arbeitsauftragstyp | Arbeitsprozess |
|---|---|
| Rohmaterialentnahme| Alle damit verbundenen Prozesse |
| Einlagerung von Co- und Nebenprodukten | Alle damit verbundenen Prozesse |
| Einlagerung von Fertigerzeugnissen | Alle damit verbundenen Prozesse |
| Umlagerungseingang | Kennzeichenempfang (und -einlagerung) |
| Bestellungen | <ul><li>Kennzeichenempfang (und -einlagerung)</li><li>Artikelempfang (und -einlagerung) aus Ladung</li><li>Bestellpositionsempfang (und -einlagerung)</li><li>Bestellungsartikelempfang (und -einlagerung)</li></ul> |

Fügen Sie dem Raster eine separate Position für jeden Arbeitsprozess hinzu, um eine Arbeitsrichtlinie so einzurichten, dass sie für mehrere Arbeitsprozesse desselben Arbeitsauftragstyps gilt.

Legen Sie für jede Position im Raster das Feld **Arbeitserstellungsmethode** auf einen der folgenden Werte fest:

- **Nie** – Die Arbeitsrichtlinie verhindert, dass Lagerortarbeit für den ausgewählten Arbeitsauftragstyp und zugehörigen Arbeitsprozess erstellt wird.
- **Crossdocking** – Die Arbeitsrichtlinie erstellt Crossdocking-Arbeit unter Verwendung der Richtlinie, die Sie im Feld **Name der Crossdocking-Richtlinie** auswählen.

### <a name="the-inventory-locations-fasttab"></a>Inforegister „Lagerorte“

Fügen Sie auf dem Inforegister **Lagerorte** alle Lagerplätze hinzu, an denen diese Arbeitsrichtlinie angewendet werden soll. Ist keinem Lagerplatz eine Arbeitsrichtlinie zugeordnet, wird die Arbeitsrichtlinie auf keinen Prozess angewendet.

Sie können nicht denselben Speicherort für mehrere Arbeitsrichtlinien angeben.

Sie können einen Lagerortplatz verwenden, der einem Lagerplatzprofil zugewiesen ist, an dem die Option **Kennzeichenverfolgung verwenden** deaktiviert ist. In diesem Fall registrieren die Mitarbeiter den Lagerbestand direkt.

### <a name="the-products-fasttab"></a>Inforegister „Produkte“

Stellen Sie auf der Registerkarte **Produkte** das Feld **Produktauswahl** so ein, um zu steuern, für welche Produkte die Richtlinie gelten soll:

- **Alle** – Die Richtlinie soll für alle Produkte gelten.
- **Ausgewählt** – Die Richtlinie soll nur für Produkte gelten, die im Raster aufgeführt sind. Verwenden Sie die Symbolleiste auf dem Inforegister **Produkte**, um Produkte zum Raster hinzuzufügen oder aus dem Raster zu entfernen.

## <a name="default-and-custom-to-locations"></a>Standard- und benutzerdefinierte „Nach“-Lagerplätze

> [!NOTE]
> Um die in diesem Abschnitt beschriebenen Funktionen in Ihrem System verfügbar zu machen, müssen Sie die Funktionen *Verbesserungen beim Kennzeichenempfang* und *Verbesserungen der Arbeitsrichtlinien für eingehende Arbeiten* in [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aktivieren.

Bisher unterstützte das System den Empfang nur am Standardort, der für jedes Lager definiert ist. Menüpunkte für mobile Geräte, die die folgenden Arbeitserstellungsprozesse verwenden, bieten jetzt jedoch die Option **Standarddaten verwenden**. Mit dieser Option können Sie einem oder mehreren Menüpunkten einen benutzerdefinierten „Nach“-Lagerplatz zuweisen. (Diese Option war bereits für einige andere Arten von Menüelementen verfügbar.)

- Kennzeichenempfang (und -einlagerung)
- Artikelempfang (und -einlagerung) aus Ladung
- Bestellpositionsempfang (und -einlagerung)
- Bestellungsartikelempfang (und -einlagerung)

Die Einstellung **Nach Lagerplatz** für einen Menüpunkt überschreibt mit diesem Menüpunkt den Standardempfangslagerplatz für den Lagerort für alle Bestellungen, die verarbeitet werden.

Führen Sie die folgenden Schritte aus, um einen Menüpunkt für mobile Geräte einzurichten, der den Empfang an einem benutzerdefinierten Lagerplatz unterstützt.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.
1. Wählen Sie einen Menüpunkt aus oder erstellen Sie ihn, der einen der zuvor in diesem Abschnitt aufgeführten Arbeitserstellungsprozesse verwendet.
1. Legen Sie auf dem Inforegister **Allgemein** die Option **Standarddaten verwenden** auf **Ja** fest.
1. Wählen Sie **Standarddaten** im Aktivitätsbereich aus.
1. Legen Sie auf der Seite **Standarddaten** die folgenden Werte fest:

    - **Standarddatenfeld:** Stellen Sie das Feld auf *Nach Lagerplatz* ein.
    - **Lagerort:** Wählen Sie den Ziellagerort aus, der mit diesem Menüpunkt verwendet werden soll.
    - **Lagerplatz:** In diesem Feld werden alle Lagerplatz-IDs aufgelistet, die für den ausgewählten Lagerort verfügbar sind. Die Einstellung dieses Feldes hat jedoch keine Auswirkung. Sie können es daher leer lassen. Trotzdem können Sie die Liste verwenden, um die ID zu bestätigen, die Sie in das Feld **Fest codierter Wert** eingeben müssen.
    - **Fest codierter Wert:** Geben Sie die Lagerplatz-ID für den Empfangslagerplatz ein, der für diesen Menüpunkt gilt.

> [!TIP]
> Eine Arbeitsrichtlinie kann nur angewendet werden, wenn alle Empfangslagerplätze in der entsprechenden Arbeitsrichtlinieneinrichtung aufgeführt sind. Diese Anforderung gilt unabhängig davon, ob Sie den Standardempfangslagerplatz für den Lagerort oder einen benutzerdefinierten „Nach“-Lagerplatz verwenden.

## <a name="example-scenario-warehouse-receiving"></a>Beispielszenario: Lagerortempfang

Alle Produkte, die vom Prozess *Bestellungsartikelempfang (und -einlagerung)* erhalten wurden, müssen am Lagerplatz *FL-001* registriert werden und im Lagerort *24* verfügbar sein. Arbeit sollte jedoch nicht erstellt werden. Produkte, die von einem anderen Prozess empfangen werden (d. h. mithilfe anderer Menüpunkte für mobile Geräte), sollten am Standardempfangslagerplatz für den Lagerort (*RECV*) registriert werden, und die Arbeit sollte wie gewohnt erstellt werden. (In diesem Szenario wird nicht die Standardempfangseinrichtung angezeigt.)

Dieses Szenario erfordert die folgenden Elemente:

- Eine Arbeitsrichtlinie für den Prozess *Bestellungsartikelempfang (und -einlagerung)* am Lagerplatz *FL-001* für alle Produkte
- Einen Menüpunkt für Mobilgeräte, der Standarddaten enthält und das Feld **Nach Lagerplatz** auf *FL-001* festlegt

### <a name="prerequisites"></a>Voraussetzungen

Um die in diesem Szenario beschriebenen Funktionen in Ihrem System verfügbar zu machen, müssen Sie die Funktionen *Verbesserungen beim Kennzeichenempfang* und *Verbesserungen der Arbeitsrichtlinien für eingehende Arbeiten* in [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aktivieren.

In diesem Szenario werden die Standarddemodaten verwendet. Wenn Sie es also mithilfe der in diesem Thema bereitgestellten Werte bearbeiten möchten, müssen Sie auf einem System arbeiten, auf dem die Demodaten installiert sind. Außerdem müssen Sie die **USMF** juristische Person auswählen.

### <a name="set-up-a-work-policy"></a>Eine Arbeitsrichtlinie einrichten

1. Wechseln Sie zu **Lagerortverwaltung \> Einrichtung \> Arbeit \> Arbeitsrichtlinien**.
1. Wählen Sie **Neu** aus.
1. Geben Sie im Feld **Name der Arbeitsrichtlinie** *Keine Einlagerungsarbeiten für Kaufartikel* ein.
1. Wählen Sie **Speichern** aus.
1. Wählen Sie auf dem Inforegister **Arbeitsauftragstypen** **Hinzufügen** aus, um dem Raster eine Zeile hinzuzufügen, und legen Sie dann die folgenden Werte für die neue Zeile fest:

    - **Arbeitsauftragstyp:** *Bestellungen*
    - **Arbeitsprozess:** *Bestellungsartikelempfang (und -einlagerung)*
    - **Arbeitserstellungsmethode:** *Nie*
    - **Name der Crossdocking-Richtlinie:** Lassen Sie dieses Feld leer.

1. Wählen Sie auf dem Inforegister **Lagerorte** **Hinzufügen** aus, um dem Raster eine Zeile hinzuzufügen, und legen Sie dann die folgenden Werte für die neue Zeile fest:

    - **Lagerort:** *24*
    - **Lagerplatz:** *FL-001*

1. Legen Sie auf dem Inforegister **Produkte** das Feld **Produktauswahl** auf *Alle* fest.
1. Wählen Sie **Speichern** aus.

### <a name="set-up-a-mobile-device-menu-item-to-change-the-receiving-location"></a>Einen Menüpunkt für das mobile Gerät einrichten, um den Empfangslagerplatz zu ändern

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.
1. Wählen Sie im linken Bereich den vorhandenen Menüpunkt **Kaufempfang** aus.
1. Legen Sie auf dem Inforegister **Allgemein** die Option **Standarddaten verwenden** auf *Ja* fest.
1. Wählen Sie **Speichern** aus.
1. Wählen Sie **Standarddaten** im Aktivitätsbereich aus.
1. Wählen Sie auf der Seite **Standarddaten** im Aktivitätsbereich **Neu** aus, um dem Raster eine Zeile hinzuzufügen, und legen Sie dann die folgenden Werte für die neue Zeile fest:

    - **Standarddatenfeld:** *Nach Lagerplatz*
    - **Lagerort:** *24*
    - **Lagerplatz:** Lassen Sie dieses Feld leer.
    - **Fest codierter Wert:** *FL-001*

1. Wählen Sie **Speichern** aus.

### <a name="receive-a-purchase-order-without-creating-work"></a>Eine Bestellung erhalten, ohne Arbeit zu erstellen

Das Beispiel in diesem Abschnitt zeigt, wie Sie einen Bestellungsartikel, ohne Arbeit zu erstellen, an einen Lagerplatz erhalten, der sich vom Standardempfangslagerplatz unterscheidet, der für den Lagerort eingerichtet ist. In diesem Beispiel werden die Arbeitsrichtlinie und der Mobilgerätepunkt verwendet, die Sie zuvor in diesem Szenario erstellt haben.

#### <a name="create-a-purchase-order"></a>Eine Bestellung erstellen

1. Wechseln Sie zu **Beschaffung \> Bestellungen \> Alle Bestellungen**.
1. Wählen Sie **Neu** aus.
1. Legen Sie im Dialogfeld **Bestellung erstellen** die folgenden Werte fest:

    - **Kreditorenkonto:** *US-101*
    - **Standort:** *2*
    - **Lagerort:** *24*

1. Wählen Sie **OK** aus, um das Dialogfeld zu schließen und die neue Bestellung zu öffnen.
1. Legen Sie auf dem Inforegister **Bestellpositionen** die folgenden Werte für die leere Zeile fest:

    - **Artikelnummer** *A001*
    - **Menge** *1*

1. Wählen Sie **Speichern** aus.
1. Notieren Sie sich die Bestellnummer.

#### <a name="receive-a-purchase-order"></a>Eine Bestellung erhalten

1. Melden Sie sich auf dem Mobilgerät beim Lagerort *24* an, indem Sie *24* als die Benutzer-ID und *1* als das Kennwort verwenden.
1. Wählen Sie **Eingehend** aus.
1. Wählen Sie **Kaufempfang** aus. Das Feld **Lagerplatz** sollte auf *FL-001* festgelegt sein.
1. Geben Sie die Bestellnummer für die Bestellung ein, die Sie im vorherigen Verfahren erstellt haben.
1. Geben Sie im Feld **Artikelnummer** den Wert *A0001* ein.
1. Wählen Sie **OK**.
1. Geben Sie im Feld **Menge** den Wert *1* ein.
1. Wählen Sie **OK**.

Die Bestellung ist jetzt eingegangen, aber es sind keine Arbeiten damit verbunden. Der Lagerbestand wurde aktualisiert, und eine Menge von *1* des Artikels *A0001* ist jetzt an Lagerplatz *FL-001* verfügbar.

## <a name="example-scenario-manufacturing"></a>Beispielszenario: Fertigung

Im folgenden Beispiel gibt es zwei Produktionsaufträge, *PRD-001* und *PRD-002*. Produktionsauftrag *PRD-001* hat einen Arbeitsgang, der als *Montage* bezeichnet wird, wo Produkt *SC1* an Lagerplatz *001* als fertig gestellt gemeldet ist. Produktionsauftrag *PRD-002* hat einen Arbeitsgang, der als *Anstrich* bezeichnet wird und bei dem Produkt *SC1* von Lagerplatz *001* verbraucht wird. Produktionsauftrag *PRD-002* verbraucht auch Rohmaterial *RM1* von Lagerplatz *001*. Rohmaterial *RM1* wird an Lagerortplatz *BULK-001* gelagert und für Lagerplatz *001* durch Lagerortarbeit für Rohmaterialentnahme entnommen. Die Entnahmearbeit wird generiert, wenn die Produktion *PRD-002* freigegeben wird.

[![Lagerortarbeitsrichtlinien](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)

Wenn Sie planen, eine Lagerortarbeitsrichtlinie dieses Szenarios zu konfigurieren, sollten Sie die folgenden Punkte berücksichtigen:

- Lagerortarbeit für die Einlagerung von Fertigerzeugnissen ist nicht erforderlich, wenn Sie Produkt *SC1* aus Produktionsauftrag *PRD-001* zum Lagerplatz *001* als fertig gestellt melden. Dies liegt daran, dass beim Arbeitsgang *Anstrich* für Produktionsauftrag *PRD-002* das Produkt *SC1* am selben Lagerplatz verbraucht wird.
- Lagerortarbeit für Rohmaterialentnahme ist erforderlich, um Rohmaterial *RM1* vom Lagerortplatz *BULK-001* zum Lagerplatz *001* zu verschieben.

Hier ist ein Beispiel einer Arbeitsrichtlinie, die Sie einrichten können, basierend auf diesen Überlegungen:

- **Name der Arbeitsrichtlinie:** *Keine Einlagerungsarbeiten*
- **Arbeitsauftragstypen:** *Einlagerung von Fertigerzeugnissen* und *Einlagerung von Kuppel- und Nebenprodukten*
- **Lagerorte:** Lagerort *51* und Lagerplatz *001*
- **Produkte:** *SC1*

Das folgende Beispielszenario enthält schrittweise Anweisungen zum Einrichten der Lagerortarbeitsrichtlinie für dieses Szenario.

## <a name="example-scenario-report-as-finished-to-a-location-that-isnt-license-platecontrolled"></a>Beispielszenario: An einen Lagerplatz, der nicht kennzeichengesteuert ist, als fertig gestellt melden

Dieses Szenario zeigt ein Beispiel, in dem ein Produktionsauftrag an einen Lagerplatz als fertig gestellt gemeldet wird, der nicht kennzeichengesteuert ist.

In diesem Szenario werden die Standarddemodaten verwendet. Wenn Sie es also mithilfe der in diesem Thema bereitgestellten Werte bearbeiten möchten, müssen Sie auf einem System arbeiten, auf dem die Demodaten installiert sind. Außerdem müssen Sie die **USMF** juristische Person auswählen.

### <a name="set-up-a-warehouse-work-policy"></a>Eine Lagerort-Arbeitsrichtlinie einrichten

Lagerortprozesse enthalten nicht immer Lagerortarbeit. Wenn Sie eine Arbeitsrichtlinie definieren, können Sie die Erstellung von Arbeit für Rohmaterialentnahme sowie die Einlagerung von Fertigerzeugnissen für einen Satz von Produkten an bestimmten Lagerplätzen verhindern.

1. Wechseln Sie zu **Lagerortverwaltung \> Einrichtung \> Arbeit \> Arbeitsrichtlinien**.
1. Wählen Sie **Neu** aus.
1. Geben Sie im Feld **Name der Arbeitsrichtlinie** *Keine Einlagerungsarbeiten* ein.
1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Wählen Sie auf dem Inforegister **Arbeitsauftragstypen** **Hinzufügen** aus, um dem Raster eine Zeile hinzuzufügen, und legen Sie dann die folgenden Werte für die neue Zeile fest:

    - **Arbeitsauftragstyp:** *Einlagerung von Fertigerzeugnissen*
    - **Arbeitsprozess:** *Alle damit verbundenen Arbeitsprozesse*
    - **Arbeitserstellungsmethode:** *Nie*
    - **Name der Crossdocking-Richtlinie:** Lassen Sie dieses Feld leer.

1. Wählen Sie erneut **Hinzufügen** aus, um dem Raster eine zweite Zeile hinzuzufügen, und legen Sie dann die folgenden Werte für die neue Zeile fest:

    - **Arbeitsauftragstyp:** *Einlagerung von Kuppel- und Nebenprodukten*
    - **Arbeitsprozess:** *Alle damit verbundenen Arbeitsprozesse*
    - **Arbeitserstellungsmethode:** *Nie*
    - **Name der Crossdocking-Richtlinie:** Lassen Sie dieses Feld leer.

1. Wählen Sie auf dem Inforegister **Lagerorte** **Hinzufügen** aus, um dem Raster eine Zeile hinzuzufügen, und legen Sie dann die folgenden Werte für die neue Zeile fest:

    - **Lagerort:** *51*
    - **Lagerplatz:** *001*

1. Legen Sie auf dem Inforegister **Produkte** das Feld **Produktauswahl** auf *Ausgewählt* fest.
1. Wählen Sie auf dem Inforegister **Produkte** die Option **Hinzufügen** aus, um dem Raster eine Zeile hinzuzufügen.
1. Stellen Sie in der neuen Zeile das Feld **Artikelnummer** auf *L0101* ein.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

### <a name="set-up-an-output-location"></a>Richten Sie einen Ausgabelagerplatz ein

1. Wechseln Sie zu **Organisationsverwaltung \> Ressourcen \> Ressourcengruppen**.
1. Wählen Sie im linken Bereich die Ressourcengruppe **5102** aus.
1. Legen Sie im Inforegister **Allgemein** die folgenden Werte fest:

    - **Ausgabelagerort:** *51*
    - **Ausgabelagerplatz:** *001*

1. Wählen Sie im Aktionsbereich **Speichern** aus.

> [!NOTE]
> Lagerplatz *001* ist kein kennzeichengesteuerter Lagerplatz. Sie können einen Ausgabelagerplatz, der nicht kennzeichengesteuert ist, nur dann einrichten, wenn eine anwendbare Arbeitsrichtlinie für den Lagerplatz vorhanden ist.

### <a name="create-a-production-order-and-report-it-as-finished"></a>Erstellen Sie einen Produktionsauftrag und melden Sie ihn als abgeschlossen

1. Wechseln Sie zu **Produktionssteuerung \> Produktionsaufträge \> Alle Produktionsaufträge**.
1. Wählen Sie im Aktivitätsbereich **Neuer Produktionsauftrag** aus.
1. Stellen Sie im Dialogfeld **Produktionsauftrag erstellen** das Feld **Artikelnummer** auf *L0101* ein.
1. Wählen Sie **Erstellen** aus, um den Auftrag zu erstellen und das Dialogfeld zu schließen.

    Ein neuer Produktionsauftrag wird dem Raster auf der Seite **Alle Produktionsaufträge** hinzugefügt.

    Lassen Sie den neuen Produktionsauftrag ausgewählt.

1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Produktionsauftrag** in der Gruppe **Prozess** auf **Kalkulieren**.
1. Lesen Sie im Dialogfeld **Kalkulieren** die Schätzung, und wählen Sie dann **OK** aus, um das Dialogfeld zu schließen.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Produktionsauftrag** in der Gruppe **Prozess** auf **Starten**.
1. Stellen Sie im Dialogfeld **Starten** auf der Registerkarte **Allgemein** das Feld **Automatischer Stücklistenverbrauch** auf *Nie* ein.
1. Wählen Sie **OK**, um Ihre Einstellung zu speichern und das Dialogfeld zu schließen.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Produktionsauftrag** in der Gruppe **Prozess** auf **Als erledigt melden**.
1. Legen Sie im Dialogfeld **Als erledigt melden** auf der Registerkarte **Allgemein** die Option **Fehler akzeptieren** auf *Ja* fest.
1. Wählen Sie **OK**, um Ihre Einstellung zu speichern und das Dialogfeld zu schließen.
1. Wählen Sie im Aktivitätsbereich, auf der Registerkarte **Lagerort** in der Gruppe **Allgemein** die Option **Arbeitsdetails** aus.

Wenn der Produktionsauftrag als fertig gemeldet ist, wird keine Arbeit für die Einlagerung generiert. Dieses Verhalten tritt auf, weil eine Arbeitsrichtlinie definiert ist, die verhindert, dass Arbeit generiert wird, wenn Produkt *L0101* an Lagerplatz *001* als fertig gestellt gemeldet wird.

## <a name="more-information"></a>Weitere Informationen

Weitere Informationen zu Menüelementen für Mobilgeräte finden Sie unter [Richten Sie mobile Geräte für die Lagerarbeit ein](configure-mobile-devices-warehouse.md).

Weitere Informationen zum Kennzeichenempfang und Arbeitsrichtlinien finden Sie unter [Kennzeichenempfang über die Warehouse Management Mobile App](warehousing-mobile-device-app-license-plate-receiving.md).

Weitere Informationen über eingehende Auslastungverwaltung finden Sie unter [Lagerortverwaltung von eingehender Auslastung für Bestellungen](inbound-load-handling.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]