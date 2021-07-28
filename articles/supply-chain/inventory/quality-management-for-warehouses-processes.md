---
title: Qualitätsmanagement für Lagerortprozesse
description: Dieses Thema enthält Informationen zur Funktion „Qualitätsmanagement für Lagerortprozesse“. Diese Funktion erweitert die Funktionen des Qualitätsmanagements und ermöglicht Benutzern, mithilfe der erweiterten Lagerverwaltung Steuerelemente für die Probenahme von Artikeln in den Wareneingangsprozess zu integrieren.
author: Henrikan
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-02
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 79eb7d750869ef365ad117ecc024afc8db2edbf7
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6348828"
---
# <a name="quality-management-for-warehouse-processes"></a>Qualitätsmanagement für Lagerortprozesse

Die Funktion _Qualitätsmanagement für Lagerortprozesse_ erweitert die Funktionen des Qualitätsmanagements und ermöglicht Ihnen, mithilfe der erweiterten Lagerverwaltung Steuerelemente für die Probenahme von Artikeln in den Wareneingangsprozess zu integrieren. Lagerortarbeit kann automatisch generiert werden, um Bestand an den Ort für die Qualitätskontrolle zu verschieben, und zwar basierend auf einem Prozentsatz oder einer festen Menge oder basierend auf jedem *n*-ten Kennzeichen. Nach Abschluss eines Qualitätsprüfungsauftrags kann abhängig von den Ergebnissen der Qualitätsprüfung automatisch Arbeit generiert werden, um Bestand an den nächsten Ort im Prozess zu verschieben.

Die Funktion _Qualitätsmanagement für Lagerortprozesse_ erweitert die Möglichkeiten des grundlegenden Qualitätsmanagements. Sie bietet die Möglichkeit, Qualitätsprüfungsaufträge für den Bestand zu erstellen, der an den Ort für die Qualitätskontrolle gesendet wird, obwohl Qualitätsprüfungsaufträge nicht immer erforderlich sind. Daher ermöglicht sie einen einfachen Qualitätskontrollenprozess, der auf Lagerortarbeit basiert.

## <a name="turn-on-the-quality-management-for-warehouse-processes-feature"></a>Aktivieren der Funktion „Qualitätsmanagement für Lagerortprozesse“

Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden. Administratoren können mit den Einstellungen [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Module:** *Lagerortverwaltung*
- **Funktionsname:** *Qualitätsmanagement für Lagerortprozesse*

## <a name="key-benefits"></a>Die wichtigsten Vorteile

Die Funktion _Qualitätsmanagement für Lagerortprozesse_ generiert automatisch Arbeit als Teil des Empfangsprozesses, um die für die Qualitätskontrolle erforderliche Bestandsmenge an einen Ort für die Qualitätskontrolle zu verschieben. Wenn die empfangene Menge die zur Qualitätskontrolle erforderliche Menge überschreitet (gemäß den Einstellungen für die Artikelmusteraufnahme), wird die überschüssige Menge an einen eingehenden Lagerplatz verschoben, der in den Einstellungen der Lagerplatzdirektive definiert ist. Nachdem der Qualitätsprüfungsauftrag validiert wurde, wird automatisch Arbeit generiert, um die Menge für den Qualitätsprüfungsauftrag basierend auf dem Prüfergebnis und den Einstellungen der Lagerplatzdirektive an einen neuen Eingangs- oder Rückgabeort zu verschieben. Die automatische Generierung von Arbeit, die nur die Menge enthält, die zur und von der Qualitätskontrolle bewegt werden muss, bietet eine integrierte Prozesserfahrung.

> [!NOTE]
> Wenn die Funktion _Qualitätsmanagement für Lagerortprozesse_ aktiviert ist, können Sie den manuellen Prozess dennoch weiterhin nutzen. Im manuellen Prozess werden Bestandsbewegungen und Verlagerungen nach Vorlage verwendet, damit eine Lagerarbeitskraft die Erstellung von Lagerarbeiten auslöst, um Bestände von einem Ort für die Qualitätskontrolle an einen neuen Ort zu verschieben. Sie können auch weiterhin eine Richtlinie für eingehende Lagerorte einrichten, mit der der gesamte Bestand von einem Empfangsort an einen Ort für die Qualitätskontrolle verschoben wird, ohne die Einstellungen für die Artikelmusteraufnahme zu berücksichtigen.

## <a name="quality-management-and-the-quality-management-for-warehouse-processes-feature"></a>Qualitätsmanagement und die Funktion „Qualitätsmanagement für Lagerortprozesse“

Wenn die Funktion _Qualitätsmanagement für Lagerortprozesse_ aktiviert ist, ändert sich die Einrichtung der wichtigsten Entitäten für das Lagermanagement und das Qualitätsmanagement. Die folgende Abbildung gibt einen Überblick über die Entitäten, die Qualitätsprüfungsaufträge für Lagerortprozesse ermöglichen. Der Text in Klammern zeigt die vorgeschlagenen Maßnahmen an, wenn das Qualitätsmanagement angewendet wurde, bevor die Funktion _Qualitätsmanagement für Lagerortprozesse_ aktiviert wurde.

![Entitäten für das Qualitätsmanagement.](media/quality-management-entity-diagram.png "Entitäten für das Qualitätsmanagement")

## <a name="enablers-the-quality-item-sampling-and-quality-order-work-order-types"></a>Enabler: Die Arbeitsauftragstypen „Qualitätsartikelmuster“ und „Qualitätsprüfungsauftrag“

Die Funktion _Qualitätsmanagement für Lagerortprozesse_ führt zwei Arbeitsauftragstypen ein, die den Arbeitserstellungsprozess ermöglichen:

- **Qualitätsartikelmuster** – Dieser Arbeitsauftragstyp wird verwendet, um Arbeit zu erstellen, mit der registrierter Bestand zur Qualitätskontrolle verschoben wird.
- **Qualitätsprüfungsauftrag** – Dieser Arbeitsauftragstyp wird verwendet, um Arbeit zu erstellen, mit der Bestand basierend auf den Einstellungen der Lagerplatzdirektive von der Qualitätskontrolle an einen neuen Lagerplatz verschoben wird.

### <a name="work-classes-location-directives-and-work-templates"></a>Arbeitsklassen, Lagerplatzrichtlinien und Arbeitsvorlagen

Die Arbeitsauftragstypen _Qualitätsartikelmuster_ und _Qualitätsprüfungsauftrag_ werden von Lagerplatzrichtlinien, Arbeitsklassen und Arbeitsvorlagen verwendet.

Bevor Lagerarbeiten automatisch generiert werden können, um den Bestand zur Qualitätskontrolle zu verschieben, müssen Sie diese Schritte ausführen, um Ihr System einzurichten.

1. Erstellen Sie separate Arbeitsklassen für die Arbeitsauftragstypen _Qualitätsartikelmuster_ und _Qualitätsprüfungsauftrag_. Auf diese Weise stellen Sie sicher, dass basierend auf den beiden Arbeitsauftragstypen automatisch entsprechende Arbeit generiert werden kann und diese Arbeit dann mithilfe der Warehouse Management Mobile App ausgeführt werden kann.
1. Einrichten einer Arbeitsvorlage für jeden Arbeitsauftragstyp:

    - Richten Sie eine Arbeitsvorlage ein, die den Arbeitsauftragstyp _Qualitätsartikelmuster_ verwendet, um registrierten Bestand automatisch an einen Ort für die Qualitätskontrolle zu verschieben.
    - Richten Sie eine Arbeitsvorlage ein, die den Arbeitsauftragstyp _Qualitätsprüfungsauftrag_ verwendet, um Bestand von einem Ort für die Qualitätskontrolle zu verschieben, nachdem die Qualitätskontrolle abgeschlossen wurde.

1. Richten Sie für jeden Arbeitsauftragstyp Lagerplatzrichtlinien ein, die den Bestand an die richtigen Orte für die Qualitätskontrolle verschieben. Nach Abschluss der Qualitätskontrolle stellt die Lagerplatzrichtlinie für den Arbeitsauftragstyp _Qualitätsprüfungsauftrag_ sicher, dass ein neuer Zielort ausgewählt wird, damit der Bestand vom Ort für die Qualitätskontrolle verschoben werden kann.
1. Richten Sie die entsprechenden Menüoptionen für mobile Geräte ein, um die Verschiebung des empfangenen Bestands zum Ort für die Qualitätskontrolle und die Verschiebung des Bestands, der die Qualitätskontrolle besteht oder nicht besteht, vom Ort für die Qualitätskontrolle an einen neuen Ort zu unterstützen.

Ein Schritt-fürSchritt-Beispiel für die Durchführung dieser Einrichtung finden Sie im [Beispielszenario](#example-scenario) am Ende dieses Themas.

## <a name="enable-a-warehouse-for-quality-management"></a>Vorbereiten eines Lagerortes für das Qualitätsmanagement

Bevor die Funktion _Qualitätsmanagement für Lagerortprozesse_ für einen bestimmten Lagerort angewendet werden kann, müssen Sie die folgenden Schritte ausführen, um die Funktion für diesen Lagerort verfügbar zu machen.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerort \> Lagerorte**.
1. Wählen Sie den Lagerort aus, der für das Qualitätsmanagement vorbereitet werden soll.
1. Legen Sie im Inforegister **Lagerort** die Option **Qualitätsprüfungsaufträge für Lagerortprozesse aktivieren** auf _Ja_ fest. (Beachten Sie, dass diese Option nur für Lagerorte, die Lagerortverwaltungsprozesse verwenden, auf _Ja_ eingestellt werden kann.)

Wenn die Option **Qualitätsprüfungsaufträge für Lagerortprozesse aktivieren** auf _Ja_ festgelegt ist, steuern die Einstellungen für die Qualitätszuordnung, ob die Funktion _Qualitätsmanagement für Lagerortprozesse_ für den ausgewählten Lagerort auch wirklich angewendet wird. Sie können die Einstellung der Option jederzeit zu _Nein_ ändern. In diesem Fall gilt die Funktion unabhängig von den Einstellungen für die Qualitätszuordnung für den Lagerort nicht mehr.

## <a name="quality-control"></a>Qualitätskontrolle

Die Funktion _Qualitätsmanagement für Lagerortprozesse_ steuert mehrere wichtige Einstellungen für Qualitätszuordnungen und Artikelmuster.

### <a name="quality-associations"></a>Qualitätszuordnungen

Jeder [Qualitätszuordnungsdatensatz](enable-quality-management.md) definiert die Tests, das akzeptable Qualitätsniveau (AQL) und den Musteraufnahmeplan, die für die generierten Qualitätsprüfungsaufträge gelten. Gehen Sie folgendermaßen vor, um einen Qualitätszuordnungsdatensatz einzurichten.

1. Wechseln Sie zu **Bestandsverwaltung \> Einstellungen \> Qualitätskontrolle \> Qualitätszuordnungen**.
1. Erstellen Sie für den Artikel oder die Gruppe, mit der Sie arbeiten, oder für alle Artikel den Qualitätszuordnungseintrag oder wählen Sie einen aus.
1. Wählen Sie im Inforegister **Bedingungen** für das Feld **Zutreffender Lagerorttyp** einen der folgenden Werte aus:

    - **Qualitätsmanagement nur für Lagerortprozesse** – Aktivieren Sie die Funktion _Qualitätsmanagement für Lagerortprozesse_. Sie können diesen Wert nur auswählen, wenn der Referenztyp entweder *Kauf* oder *Produktion* ist.
    - **Alle** – Deaktivieren Sie die Funktion _Qualitätsmanagement für Lagerortprozesse_. Wählen Sie diesen Wert für alle Referenztypen außer *Kauf* und *Produktion* aus.

> [!NOTE]
> Die Funktion _Qualitätsmanagement für Lagerortprozesse_ wird nur wirksam, wenn der Artikel in der Quelldokumentzeile erweiterte Lagerortverwaltungsprozesse verwendet und wenn die Option **Qualitätsprüfungsaufträge für Lagerortprozesse aktivieren** für den Lagerort in der Quelldokumentzeile auf _Ja_ festgelegt ist.

Da jeder Artikel registriert (oder als fertig gemeldet) wird, bestimmt das System, welche Qualitätszuordnungen für ihn gelten.

Wenn die Funktion _Qualitätsmanagement für Lagerortprozesse_ aktiviert ist, wird der entsprechende Lagerorttyp logisch in die vierte Suchgruppe der Suchhierarchie für Qualitätszuordnungen eingefügt. Die folgende Tabelle zeigt eine logische Darstellung der Suchhierarchie.

| Suchgruppe | Beschreibung |
|---|---|
| Gruppe 1 | Prüfen Sie für jede Qualitätszuordnung die Werte **Referenztyp**, **Ereignistyp** und **Ausführungsübereinstimmung** gegen den Artikel. Wenn eine Übereinstimmung mit der Quelldokumentzeile besteht, fahren Sie mit Gruppe 2 fort. |
| Gruppe 2 | Prüfen Sie für jede Qualitätszuordnung den Wert **Artikelcode** (_Tabelle_, _Gruppe_ oder _Alle_) gegen den Artikel. _Tabelle_ ist spezifischer als _Gruppe_ und _Gruppe_ ist wiederum spezifischer als _Alle_. Wenn es eine Übereinstimmung für _Tabelle_ (einen bestimmten Artikel) gibt, fahren Sie mit Gruppe 3 fort. Wenn es keine Übereinstimmung für _Tabelle_ gibt, suchen Sie nach einer Übereinstimmung für _Gruppe_. Wenn es keine Übereinstimmung für _Gruppe_ gibt, trifft _Alle_ zu. Wenn es eine Übereinstimmung gibt, fahren Sie mit Gruppe 3 fort. |
| Gruppe 3 | Prüfen Sie für jede Qualitätszuordnung die Werte **Kontocode** und **Ressourcencode** gegen den Artikel. Die angewendete Logik ähnelt der Logik, die für den Wert **Artikelcode** angewendet wird. |
| Gruppe 4 | Prüfen Sie für jede Qualitätszuordnung den Wert **Zutreffender Lagerorttyp** (_Qualitätsmanagement nur für Lagerortprozesse_ oder _Alle_) gegen den Artikel. Wenn die Option **Qualitätsprüfungsaufträge für Lagerortprozesse aktivieren** für den Lagerort im Quelldokument auf _Ja_ festgelegt ist und der Artikel in der Quelldokumentzeile auf _Benutzerfehlerprotokoll für Lagerortverwaltungsprozesse verwenden_, treffen beide Zuordnungen mit einer Übereinstimmung für _Qualitätsmanagement nur für Lagerortprozesse_ und Zuordnungen mit einer Übereinstimmung für _Alle_ gleichzeitig zu, sofern beide existieren. Wenn die Option **Qualitätsprüfungsaufträge für Lagerortprozesse aktivieren** für den Lagerort in der Quelldokumentzeile auf _Nein_ festgelegt ist und der Artikel in der Quelldokumentzeile auf _Benutzerfehlerprotokoll für Lagerortverwaltungsprozesse verwenden_, trifft nur das Qualitätsmanagement zu. |

Beispiel: Sie haben einen Lagerort definiert, für den die Option **Qualitätsprüfungsaufträge für Lagerortprozesse aktivieren** auf _Ja_ festgelegt ist und es gibt zwei Qualitätszuordnungen, die für den Referenztyp *Kauf* definiert sind, eine davon für alle Artikel und eine für den Ereignistyp *Registrierung*. Der einzige Unterschied zwischen den beiden Qualitätszuordnungen ist der Wert **Zutreffender Lagerorttyp**, der für eine Qualitätszuordnung auf _Alle_ festgelegt und für die andere auf _Qualitätsmanagement nur für Lagerortprozesse_. In diesem Fall sind beide Qualitätszuordnungen gleich spezifisch und beide sind zutreffend.

Der Wert im Feld **Testgruppe** für die Qualitätszuordnungen ist ebenfalls ein Faktor. Dieses Feld definiert das Prüfverfahren, das angewendet werden muss. Falls der Wert **Testgruppe** für beide Zuordnungen identisch ist, wird nur ein Qualitätsprüfungsauftrag erstellt, und zwar für die Qualitätszuordnung, für die der Wert **Zutreffender Lagerorttyp** auf _Qualitätsmanagement nur für Lagerortprozesse_ festgelegt ist. Ist der Wert **Testgruppe** nicht für beide Zuordnungen identisch, werden zwei Qualitätsprüfungsaufträge erstellt. Der erste Qualitätsprüfungsauftrag wird für diejenige Qualitätszuordnung erstellt, für die der Wert **Zutreffender Lagerorttyp** auf _Qualitätsmanagement nur für Lagerortprozesse_ festgelegt ist. Der zweite Qualitätsprüfungsauftrag wird für diejenige Qualitätszuordnung erstellt, für die der Wert **Zutreffender Lagerorttyp** auf _Alle_ festgelegt ist.

> [!NOTE]
> Der Wert _Qualitätsmanagement nur für Lagerortprozesse_ wird als spezifischer angesehen als _Alle_, wenn die Kriterien für die Qualitätszuordnungen für die Gruppen 1 und 2 identsich sind und wenn die Testgruppe dieselbe ist. Zwei Qualitätsprüfungsaufträge werden nur dann erstellt, wenn sich die Testgruppen unterscheiden.

#### <a name="reference-types"></a>Referenztypen

Wenn der Wert **Referenztyp** auf _Kauf_ und der Wert **Zutreffender Lagerorttyp** auf _Qualitätsmanagement nur für Lagerortprozesse_ festgelegt sind , muss für das Feld **Ereignistyp** im Inforegister **Prozess** der Wert _Registrierung_ ausgewählt werden. _Registrierung_ ist der einzige unterstützte Ereignistyp für den Referenztyp _Kauf_, wenn Sie die Funktion _Qualitätsmanagement für Lagerortprozesse_ verwenden.

#### <a name="quality-processing-policy"></a>Qualitätsverarbeitungsrichtlinie

Die Funktion _Qualitätsmanagement für Lagerortprozesse_ ermöglicht das Erstellen von Arbeit nur auf der Grundlage der Artikelmusteraufnahme. Daher ermöglicht sie einen einfachen Prozess. Der Bestand, für den die Arbeit erstellt wird, hängt von der Artikelmusteraufnahme ab, die der Qualitätszuordnung zugeordnet ist. Wenn der einfache Prozess verwendet wird, kann die Qualitätsabteilung, nachdem eine Arbeitskraft die Menge am Ort für die Qualitätskontrolle abgelegt hat, manuell einen Qualitätsauftrag erstellen, falls ein Qualitätsauftrag erforderlich ist.

Das Feld **Qualitätsverarbeitungsrichtlinie** im Inforegister **Qualitätsauftragsprozess** steuert, ob beim Erstellen von Arbeit zum Verschieben eines Artikels an den Ort für die Qualitätskontrolle auch ein Qualitätsprüfungsauftrag erstellt wird. Dieses Feld kann auf _Qualitätsprüfungsauftrag erstellen_ oder _Nur Arbeit erstellen_ festgelegt werden. Das Standardwert ist _Qualitätsprüfungsauftrag erstellen_.

> [!NOTE]
> Unabhängig davon, ob Sie Qualitätsprüfungsaufträge manuell oder automatisch erstellen, generiert das System automatisch Arbeit zum Verschieben von Artikeln vom Ort für die Qualitätskontrolle, wenn der Qualitätsprüfungsauftrag als geprüft markiert wird.

Die Erstellung von Arbeit im Zusammenhang mit Qualitätsprüfungsaufträgen hängt nicht mit den Einstellungen für die Qualitätszuordnung zusammen. Wenn eine Arbeitsvorlage vorhanden ist, für die der Wert **Arbeitsauftragsart** auf *Qualitätsprüfungsauftrag* festgelegt ist, und wenn die Abfragekriterien für diese Arbeitsvorlage eingehalten werden, löst die Prüfung eines Qualitätsprüfungsauftrags die Erstellung von Arbeit aus.

#### <a name="referenced-item-sampling"></a>Referenzierte Artikelmusteraufnahme

Jede Qualitätszuordnung muss eine Artikelmusteraufnahme referenzieren. Eine Artikelmusteraufnahme definiert die Menge, die zur Qualitätskontrolle gesendet wird. Sie kann so eingerichtet werden, dass sie nur für Qualitätszuordnungen zutrifft, für die der Wert **Zutreffender Lagerorttyp** auf _Qualitätsmanagement nur für Lagerortprozesse_ festgelegt ist. Wenn der Wert **Musterumfang** für eine Artikelmusteraufnahme auf _Ladung_ oder _Lieferung_ festgelegt ist oder der Wert **Mengenspezifikation** auf _Vollständiges Kennzeichen_, kann die Artikelmusteraufnahme nur durch Qualitätszuordnungen referenziert werden, für die der Wert **Zutreffender Lagerorttyp** auf _Qualitätsmanagement nur für Lagerortprozesse_ festgelegt ist.

Wenn Sie eine Artikelmusteraufnahme definieren, die den für _Qualitätsmanagement nur für Lagerortprozesse_ zutreffenden Lagerorttyp verwendet, erhalten Sie eine Fehlermeldung, falls Sie versuchen, sie über eine Qualitätszuordnung zu referenzieren, die nicht die Funktion _Qualitätsmanagement für Lagerortprozesse_ verwendet.

> [!NOTE]
> Eine Artikelmusteraufnahme, die die vollständige Sperrung verwendet, wird für Qualitätszuordnungen nicht unterstützt, bei denen für das Feld **Zutreffender Lagerorttyp** der Wert _Qualitätsmanagement nur für Lagerortprozesse_ ausgewählt ist.

### <a name="item-sampling"></a>Artikelmusteraufnahme

Die Artikelmusteraufnahme steuert, wie oft Artikel zur Qualitätskontrolle gesendet werden. Die Funktion _Qualitätsmanagement für Lagerortprozesse_ führt das Konzept des _Umfangs der Artikelmusteraufnahme_ ein. Das System verwendet den Umfang der Artikelmusteraufnahme, wenn es bewertet, ob und wie Qualitätsprüfungsaufträge und/oder Arbeit für Qualitätsartikelmuster und Qualitätsaufträge erstellt werden sollen.

Um die Artikelmusteraufnahme einzurichten, wechseln Sie zu **Bestandsverwaltung \> Einstellungen \> Qualitätskontrolle \> Artikelmusteraufnahme** und wählen für das Feld **Musterumfang** einen der folgenden Werte aus:

- **Auftrag** – Die Quelldokumentzeile dient als Grundlage für die Bewertung, ob und wie Qualitätsprüfungsaufträge und/oder Arbeit für Qualitätsartikelmuster und Qualitätsaufträge erstellt werden. Dieser Wert ist der Standardwert und wenn er ausgewählt ist, funktioniert das System auf dieselbe Weise, wie bei nicht aktivierter Funktion _Qualitätsmanagement für Lagerortprozesse_.
- **Ladung** – Ladungen dienen als Grundlage zur Bewertung, ob und wie ein Qualitätsprüfungsauftrag und/oder Arbeit erstellt wird. Dieser Wert ist nur dann verfügbar, wenn die Funktion _Qualitätsmanagement für Lagerortprozesse_ aktiviert ist.
- **Lieferung** – Lieferungen dienen als Grundlage zur Bewertung, ob und wie ein Qualitätsprüfungsauftrag und/oder Arbeit erstellt wird. Dieser Wert ist nur dann verfügbar, wenn die Funktion _Qualitätsmanagement für Lagerortprozesse_ aktiviert ist.

> [!NOTE]
> Wenn für das Feld **Musterumfang** entweder *Ladung* oder *Lieferung* ausgewählt ist, werden die Ladungsentität und die Lieferungsentitäten verwendet, sofern sie verfügbar sind. Sind Sie nicht verfügbar, wird die Auftragsentität verwendet.

Die Funktion _Qualitätsmanagement für Lagerortprozesse_ führt außerdem den Wert *Vollständiges Kennzeichen* für das Feld **Mengenspezifikation** ein. Dieser Wert unterstützt die Erstellung von Arbeit für Qualitätsprüfungsaufträge und Qualitätsartikelmuster auf der Grundlage von Kennzeichen. Wenn Sie diesen Wert auswählen, kommt es zu folgenden Änderungen:

- Die Option **Anzahl nach Artikel aufteilen** und das Feld **Pro n-tem Kennzeichen** im Inforegister **Prozess** stehen zur Verfügung.
- Das Feld **Wert** im Inforegister **Menge der Artikelmusteraufnahme** steht nicht mehr zur Verfügung.
- Die Optionen **Pro aktualisierter Menge**, **Lagerort** und **Kennzeichen** werden alle auf *Ja* festgelegt und die Einstellungen können nicht geändert werden.

Die Option **Anzahl nach Artikel aufteilen** steuert, ob die Kennzeichenanzahl pro Artikel oder für alle Artikel im Umfang der Artikelmusteraufnahme bewertet wird. Produktvarianten werden als gleicher Artikel behandelt. Diese Option steuert auch, ob die Kennzeichenanzahl für jeden Artikel zurückgesetzt wird.

Der Wert für das Feld **Pro n-tem Kennzeichen** steuert, wie oft Qualitätsprüfungsaufträge in Bezug auf die Anzahl der registrierten Artikel erstellt werden. Beispiel: Für einen Wert von *3* wird jeder dritte Artikel an die Qualitätskontrolle gesendet, beginnend mit dem ersten Artikel. Der Wert muss größer als 0 (null) sein.

Während Arbeitskräfte mithilfe der Warehouse Management Mobile App Artikel erhalten, überprüft das System, ob für jeden eingehenden Artikel eine Qualitätszuordnung eingerichtet wurde. Wenn eine Qualitätszuordnung eingerichtet ist, verwendet das System den für diese Qualitätszuordnung konfigurierten Artikelmusteraufnahme-Datensatz, um zu bestimmen, wie Qualitätsprüfungsaufträge, Arbeit für Qualitätsartikelmuster und Arbeit für Bestellungen erstellt werden.

> [!NOTE]
> Wenn die Eingangsregistrierung im Webclient erfolgt (über die kleine Registrierungsseite oder die Wareneingangserfassung für Bestellpositionen), wird unabhängig von der Einrichtung keine Arbeit für Qualitätsartikelmuster oder Arbeit für Bestellungen erstellt. Stattdessen wird für Artikel, die einer Qualitätszuordnung entsprechen, die referenzierte Artikelmusteraufnahme verwendet, um nur die Erstellung von Qualitätsprüfungsaufträgen zu steuern.

## <a name="examples-of-automatic-generation-of-quality-orders"></a>Beispiele zur automatischen Generierung von Qualitätsprüfungsaufträgen

Die folgenden Beispiele zeigen, wie sich die Einrichtung einer Qualitätszuordnung und einer zugehörigen Artikelmusteraufnahme auf die Generierung von Qualitätsprüfungsaufträgen auswirkt, wenn für das Feld **Zutreffender Lagerorttyp** die Option _Qualitätsmanagement nur für Lagerortprozesse_ ausgewählt ist.

Wenn der Wert **Mengenspezifikation** auf _Vollständiges Kennzeichen_ festgelegt ist, steuert das Feld **Pro n-tem Kennzeichen**, für welche Kennzeichen Arbeit für Qualitätsartikelmuster erstellt wird. Das erste Kennzeichen wird immer einer Qualitätskontrolle unterzogen. Der Wert dieses Feldes gibt dann an, dass jedes *n*-te Kennzeichen nach diesem Kennzeichen ebenfalls einer Qualitätskontrolle unterzogen werden sollte.

Der Wert **Referenztyp** für die folgenden Beispiele lautet _Kauf_ und der Wert **Ereignistyp** ist *Registrierung*.

| Musterumfang | Mengespezifikation | Pro aktualisierter Menge | Pro Lagerdimension | Zählung nach Artikel | Alle x Ladungsträger | Ergebnis |
|---|---|---|---|---|---|---|
| Auftrag | Vollständiger Ladungsträger | Ja _(gesperrt/nicht bearbeitbar)_ | <p>Lagerort: Ja</p><p>Kennzeichen: Ja _(gesperrt/nicht bearbeitbar)_</p> | Nr. | 3 | <p>**Auftragspositionsmenge: 100 EA**</p><ol><li>Registrieren des Empfangs in der Warehouse Management Mobile App für 20 EA, LP1<p>Qualitätsartikelmuster-Arbeit für 20 EA</p><p>Qualitätsprüfungsauftrag 1 für 20 EA</p></li><li>Registrieren des Empfangs in der Warehouse Management Mobile App für 20 EA, LP2<p>Bestellungsarbeit für 20 EA (Einlagerung)</p></li><li>Registrieren des Empfangs in der Warehouse Management Mobile App für 20 EA, LP3<p>Bestellungsarbeit für 20 EA (Einlagerung)</p></li><li>Registrieren des Empfangs in der Warehouse Management Mobile App für 20 EA, LP4<p>Qualitätsartikelmuster-Arbeit für 20 EA</p></li><li>Registrieren des Empfangs in der Warehouse Management Mobile App für 20 EA, LP5<p>Bestellungsarbeit für 20 EA (Einlagerung)</p></li></ol> |
| Auftrag | Feste Menge = 1 | Ja | <p>Lagerort: Ja</p><p>Kennzeichen: Ja</p> | Nr. | Nicht zutreffend | <p>**Auftragspositionsmenge: 100**</p><ol><li>Registrieren des Empfangs in der Warehouse Management Mobile App für 20 EA, LP1<p>Qualitätsartikelmuster-Arbeit für 1 EA</p><p>Qualitätsprüfungsauftrag 1 für 1 EA</p><p>Bestellungsarbeit für 19 EA (Einlagerung)</p></li><li>Registrieren des Empfangs in der Warehouse Management Mobile App für 20 EA, LP2<p>Qualitätsartikelmuster-Arbeit für 1 EA</p><p>Qualitätsprüfungsauftrag 1 für 1 EA</p><p>Bestellungsarbeit für 19 (Einlagerung)</p></li><li>Registrieren des Empfangs in der Warehouse Management Mobile App für 20 EA, LP3<p>Qualitätsartikelmuster-Arbeit für 1 EA</p><p>Qualitätsprüfungsauftrag 1 für 1 EA</p><p>Bestellungsarbeit für 19 EA (Einlagerung)</p></li><li>Registrieren des Empfangs in der Warehouse Management Mobile App für 20 EA, LP4<p>Qualitätsartikelmuster-Arbeit für 1 EA</p><p>Qualitätsprüfungsauftrag 1 für 1 EA</p><p>Bestellungsarbeit für 19 EA (Einlagerung)</p></li><li>Registrieren des Empfangs in der Warehouse Management Mobile App für 20 EA, LP5<p>Qualitätsartikelmuster-Arbeit für 1 EA</p><p>Qualitätsprüfungsauftrag 1 für 1 EA</p><p>Bestellungsarbeit für 19 EA (Einlagerung)</p></li></ol> |
| Auftrag | Prozent = 10 | Nr. | <p>Lagerort: Nein</p><p>Kennzeichen: Nein</p> | Nr. | Nicht zutreffend | <p>**Auftragspositionsmenge: 100 EA**</p><ol><li>Registrieren des Empfangs in der Warehouse Management Mobile App für 50 EA, LP1<p>Qualitätsartikelmuster-Arbeit für 10 EA</p><p>Qualitätsprüfungsauftrag 1 für 10 EA</p><p>Bestellungsarbeit für 40 EA (Einlagerung)</p></li><li>Registrieren des Empfangs in der Warehouse Management Mobile App für 50 EA, LP2<p>Bestellungsarbeit für 50 EA (Einlagerung)</p></li></ol> |
| Einlesen | Prozent = 5 | Ja _(gesperrt/nicht bearbeitbar)_ | <p>Lagerort: Nein</p><p>Kennzeichen: Nein</p> | Nr. | Nicht zutreffend | <p>**Auftragspositionsmenge: 500 EA**</p><p>**Zwei Ladungen: erste Ladung 200 EA, zweite Ladung 300 EA**</p><ol><li>Registrieren des Empfangs in der Warehouse Management Mobile App für die erste Ladung für 100 EA<p>Qualitätsartikelmuster-Arbeit für 5 EA</p><p>Qualitätsprüfungsauftrag 1 für 5 EA</p><p>Bestellungsarbeit für 95 EA (Einlagerung)</p></li><li>Registrieren des Empfangs in der Warehouse Management Mobile App für die erste Ladung für 100 EA<p>Qualitätsartikelmuster-Arbeit für 5 EA</p><p>Qualitätsprüfungsauftrag 1 für 5 EA</p><p>Bestellungsarbeit für 95 EA (Einlagerung)</p></li><li>Registrieren des Empfangs in der Warehouse Management Mobile App für die zweite Ladung für 300 EA<p>Qualitätsartikelmuster-Arbeit für 15 EA</p><p>Qualitätsprüfungsauftrag 1 für 15 EA</p><p>Bestellungsarbeit für 285 EA (Einlagerung)</p></li></ol> |
| Reihenfolge | Prozent = 10 | Ja | <p>Lagerort: Ja</p><p>Kennzeichen: Ja</p> | Nr. | Nicht zutreffend | <p>**Auftragspositionsmenge: 100**</p><ol><li>Registrieren des Empfangs in der Warehouse Management Mobile App für 50 EA, LP1<p>Qualitätsartikelmuster-Arbeit für 5 EA</p><p>Qualitätsprüfungsauftrag 1 für 5 EA</p><p>Bestellungsarbeit für 45 EA (Einlagerung)</p></li><li>Registrieren des Empfangs in der Warehouse Management Mobile App für 50 EA, LP2<p>Qualitätsartikelmuster-Arbeit für 5 EA</p><p>Qualitätsprüfungsauftrag 1 für 5 EA</p><p>Bestellungsarbeit für 45 (Einlagerung)</p></li></ol> |
| Last | Vollständiger Ladungsträger | Ja _(gesperrt/nicht bearbeitbar)_ | <p>Lagerort: Ja</p><p>Kennzeichen: Ja _(gesperrt/nicht bearbeitbar)_</p> | Nr. | 3 | <p>**Zwei Artikel:**</p><ul><li>**Auftragspositionsmenge für Artikel A: 120 EA (4 Paletten)**</li><li>**Auftragspositionsmenge für Artikel B: 90 EA (3 Paletten)**</li></ul><p>**Eine Ladung, zwei Ladungspositionen für jede Auftragsposition**</p><ol><li>Registrieren des Empfangs in der Warehouse Management Mobile App für Artikel A, 30 EA, LP1<p>Qualitätsartikelmuster-Arbeit für 30 EA</p><p>Qualitätsprüfungsauftrag 1 für 30 EA</p></li><li>Registrieren des Empfangs in der Warehouse Management Mobile App für Artikel A, 30 EA, LP2<p>Bestellungsarbeit für 30 EA (Einlagerung)</p></li><li>Registrieren des Empfangs in der Warehouse Management Mobile App für Artikel A, 30 EA, LP3<p>Bestellungsarbeit für 30 EA (Einlagerung)</p></li><li>Registrieren des Empfangs in der Warehouse Management Mobile App für Artikel A, 30 EA, LP4<p>Qualitätsartikelmuster-Arbeit für 30 EA</p><p>Qualitätsprüfungsauftrag 1 für 30 EA</p></li><li>Registrieren des Empfangs in der Warehouse Management Mobile App für Artikel B, 30 EA, LP5<p>Bestellungsarbeit für 30 EA (Einlagerung)</p></li><li>Registrieren des Empfangs in der Warehouse Management Mobile App für Artikel B, 30 EA, LP6<p>Bestellungsarbeit für 30 EA (Einlagerung)</p></li><li>Registrieren des Empfangs in der Warehouse Management Mobile App für Artikel A, 30 EA, LP7<p>Qualitätsartikelmuster-Arbeit für 30 EA</p><p>Qualitätsprüfungsauftrag 1 für 30 EA</p></li></ol> |
| Last | Vollständiger Ladungsträger | Ja _(gesperrt/nicht bearbeitbar)_ | <p>Lagerort: Ja</p><p>Kennzeichen: Ja _(gesperrt/nicht bearbeitbar)_</p> | Ja | 3 | <p>**Zwei Artikel:**</p><ul><li>**Auftragspositionsmenge für Artikel A: 120 EA (4 Paletten)**</li><li>**Auftragspositionsmenge für Artikel B: 90 EA (3 Paletten)**</li></ul><p>**Eine Ladung, zwei Ladungspositionen für jede Auftragsposition**</p><ol><li>Registrieren des Empfangs in der Warehouse Management Mobile App für Artikel A, 30 EA, LP1<p>Qualitätsartikelmuster-Arbeit für 30 EA</p><p>Qualitätsprüfungsauftrag 1 für 30 EA</p></li><li>Registrieren des Empfangs in der Warehouse Management Mobile App für Artikel A, 30 EA, LP2<p>Bestellungsarbeit für 30 EA (Einlagerung)</p></li><li>Registrieren des Empfangs in der Warehouse Management Mobile App für Artikel A, 30 EA, LP3<p>Bestellungsarbeit für 30 EA (Einlagerung)</p></li><li>Registrieren des Empfangs in der Warehouse Management Mobile App für Artikel A, 30 EA, LP4<p>Qualitätsartikelmuster-Arbeit für 30 EA</p><p>Qualitätsprüfungsauftrag 1 für 30 EA</p></li><li>Registrieren des Empfangs in der Warehouse Management Mobile App für Artikel B, 30 EA, LP5<p>Qualitätsartikelmuster-Arbeit für 30 EA</p><p>Qualitätsprüfungsauftrag 1 für 30 EA</p></li><li>Registrieren des Empfangs in der Warehouse Management Mobile App für Artikel B, 30 EA, LP6<p>Bestellungsarbeit für 30 EA (Einlagerung)</p></li><li>Registrieren des Empfangs in der Warehouse Management Mobile App für Artikel A, 30 EA, LP7<p>Bestellungsarbeit für 30 EA (Einlagerung)</p></li></ol> |
| Last | Prozent = 10 | Ja _(gesperrt/nicht bearbeitbar)_ | <p>Lagerort: Nein</p><p>Kennzeichen: Nein</p> | Nr. | Nicht zutreffend | <p>**Auftragspositionsmenge: 100 EA**</p><p>**Es werden keine Ladungen erstellt. Der Auftragsumfang wird angewendet.**</p><ol><li>Registrieren des Empfangs in der Warehouse Management Mobile App für 50 EA, LP1<p>Qualitätsartikelmuster-Arbeit für 5 EA</p><p>Qualitätsprüfungsauftrag 1 für 5 EA</p><p>Bestellungsarbeit für 45 EA (Einlagerung)</p></li><li>Registrieren des Empfangs in der Warehouse Management Mobile App für 50 EA, LP2<p>Qualitätsartikelmuster-Arbeit für 5 EA</p><p>Qualitätsprüfungsauftrag 1 für 5 EA</p><p>Bestellungsarbeit für 45 EA (Einlagerung)</p></li></ol> |

Wenn eine Arbeitskraft eine der in der vorherigen Tabelle aufgeführten Qualitätszuordnungen prüft, generiert das System automatisch Arbeit für Qualitätsprüfungsaufträge, um Bestand vom Ort für die Qualitätskontrolle an den Ort zu verschieben, der in der Lagerplatzrichtlinie für den Arbeitsauftragstyp _Qualitätsprüfungsauftrag_ definiert ist. Abhängig vom Testergebnis für den Qualitätsprüfungsauftrag können Sie zu diesem Zweck einen beliebigen Ort einrichten, z. B. einen Rückgabe- oder Lagerort. Ein Beispiel für diese Einrichtung finden Sie im [Beispielszenario](#example-scenario) am Ende dieses Themas.

Sie können einen bereits validierten Qualitätsprüfungsauftrag erneut öffnen, falls die Arbeit für den Qualitätsprüfungsauftrag, die mit dem Verschieben des Bestands vom Ort für die Qualitätskontrolle zusammenhängt, nicht über einen Wert **Arbeitsstatus** von *Geschlossen* oder *In Bearbeitung* verfügt.

## <a name="process-insights-when-multiple-quality-associations-coexist"></a>Prozesseinblicke, wenn mehrere Qualitätszuordnungen gleichzeitig existieren

Es können mehrere Qualitätszuordnungen für dieselbe Quelldokumentzeile definiert und auf diese angewendet werden und für das Feld **Zutreffender Lagerorttyp** kann für manche dieser Qualitätszuordnungen _Qualitätsmanagement nur für Lagerortprozesse_ ausgewählt werden und _Alle_ für andere.

Im folgenden Beispiel ist der Wert **Referenztyp** auf _Kauf_ festgelegt.

1. Die erste Qualitätszuordnung wird folgendermaßen eingerichtet:

    - **Zutreffender Lagerorttyp:** *Qualitätsmanagement nur für Lagerortprozesse*
    - **Artikelcode:** *A0001*
    - **Kontocode:** *Alle*
    - **Testgruppe:** *Anlage*
    - **Artikelmusteraufnahme:** *5 Stk.*

1. Die zweite Qualitätszuordnung wird folgendermaßen eingerichtet:

    - **Zutreffender Lagerorttyp:** *Alle*
    - **Artikelcode:** *Alle*
    - **Kontocode:** *Alle*
    - **Testgruppe:** *Anlage*
    - **Artikelmusteraufnahme:** *1 Stk.*

1. Die dritte Qualitätszuordnung wird folgendermaßen eingerichtet:

    - **Zutreffender Lagerorttyp:** *Qualitätsmanagement nur für Lagerortprozesse*
    - **Artikelcode:** *Alle*
    - **Kontocode:** *104*
    - **Testgruppe:** *Widerstand*
    - **Artikelmusteraufnahme:** *Jedes zweite Kennzeichen* (Diese Einstellung bedeutet, dass das erste, das dritte, das fünfte Kennzeichen usw., das empfangen wird, einen Qualitätsprüfungsauftrag erstellt.)

1. Die vierte Qualitätszuordnung wird folgendermaßen eingerichtet:

    - **Zutreffender Lagerorttyp:** *Alle*
    - **Artikelcode:** *Alle*
    - **Kontocode:** *Alle*
    - **Testgruppe:** *Widerstand*
    - **Artikelmusteraufnahme:** *5 Stk.*

1. Die fünfte Qualitätszuordnung wird folgendermaßen eingerichtet:

    - **Zutreffender Lagerorttyp:** *Alle*
    - **Artikelcode:** *Alle*
    - **Kontocode:** *Alle*
    - **Testgruppe:** *Kegel*
    - **Artikelmusteraufnahme:** *10 %*

Für den Lieferanten 104 wird nun eine Bestellung für eine Menge von 10 Stück des Artikels A0001 erstellt. Anschließend wird eine Bestellposition mit einer Menge von 10 mithilfe der Warehouse Management Mobile App auf einem Ladungsträger als empfangen registriert. Hier ist das Ergebnis:

- Es gibt einen Qualitätsprüfungsauftrag von der ersten Qualitätszuordnung für die Testgruppe *Anlage*. Die Menge beträgt 5. Es gibt keinen Qualitätsprüfungsauftrag von der zweiten Qualitätszuordnung, da die Kriterien für die erste Qualitätszuordnung in Bezug auf die Testgruppe *Anlage* spezifischer sind.
- Es gibt einen Qualitätsprüfungsauftrag für die dritte Qualitätszuordnung für die Testgruppe *Widerstand*. Die Menge beträgt 10. Es gibt keinen Qualitätsprüfungsauftrag von der vierten Qualitätszuordnung, da die Kriterien für die erste Qualitätszuordnung in Bezug auf die Testgruppe *Widerstand* spezifischer sind.
- Es gibt einen Qualitätsprüfungsauftrag für die fünfte Qualitätszuordnung für die Testgruppe *Kegel*. Die Menge beträgt 1.

Im Zusammenhang mit der Erstellung eines Qualitätsprüfungsauftrags für jede der drei Qualitätszuordnungen wird auch Arbeit für Qualitätsartikelmuster erstellt. Die registrierte Menge beträgt nur 10. Aufgrund der Einstellungen für die Artikelmusteraufnahme beläuft sich jedoch die Summe der Mengen der Qualitätsprüfungsaufträge, die für den zutreffenden Lagerorttyp *Qualitätsmanagement nur für Lagerortprozesse* erstellt werden, auf 16, was die physisch registrierte Menge von 10 überschreitet. Daher wird keine Arbeit für alle die gesamte Menge der Qualitätsprüfungsaufträge (16) erstellt, da für den Transport zum Ort für die Qualitätskontrolle nur 10 physisch verfügbar sind. Die Priorität beim Erstellen von Arbeit für Qualitätsartikelmuster folgt der Reihenfolge der Erstellung von Qualitätsprüfungsaufträgen:

- **Erster Qualitätsprüfungsauftrag (Menge = 5):** Qualitätsartikelmuster-Arbeit für 5 wird erstellt. Es verbleibt nun eine Menge von 5 (10 abzüglich 5) für die spätere Erstellung von Qualitätsartikelmuster-Arbeit.
- **Zweiter Qualitätsprüfungsauftrag (Menge = 10):** Qualitätsartikelmuster-Arbeit für 5 wird erstellt. Es verbleibt nun eine Menge von 0 (null) für die spätere Erstellung von Qualitätsartikelmuster-Arbeit.
- **Dritter Qualitätsprüfungsauftrag (Menge = 1):** Keine Qualitätsartikelmuster-Arbeit wird erstellt.

Im Rahmen der Erstellung der Qualitätsprüfungsaufträge wird eine Sperrung von Lagerbestand für 10 Stück erstellt. Diese Sperrung von Lagerbestand wird für jeden der drei Qualitätsprüfungsaufträge referenziert. Die Summe der Mengen der Qualitätsprüfungsaufträge beträgt 16.

Wenn die Qualitätsprüfungsaufträge geprüft werden, versucht das System, für jeden geprüften Qualitätsprüfungsauftrag Arbeit zu erstellen. Da die Summe der Mengen der Qualitätsprüfungsaufträge die Menge überschreitet, die tatsächlich gesperrt und daher für die Arbeitserstellung verfügbar ist, kann nicht für die gesamte Menge der Qualitätsprüfungsaufträge Arbeit für Qualitätsprüfungsaufträge erstellt werden, wie hier gezeigt. (Bei diesem Beispiel wird das vorherige Bespiel fortgesetzt.)

1. **Prüfen Sie den zweiten erstellten Qualitätsprüfungsauftrag (Menge = 10). Die Arbeit für Qualitätsprüfungsaufträge wird für eine Menge von 4 erstellt.**

    Die Erstellung von Arbeit für Qualitätsprüfungsaufträge wird durch eine Änderung der Menge für die Sperrung von Lagerbestand ausgelöst. Da die Summe der Mengen der Qualitätsprüfungsaufträge 16 betrug, führt die Prüfung einer Menge von 10 dazu, dass 6 Mengen der Qualitätsprüfungsaufträge zur Prüfung verbleiben. Die Menge für die Sperrung von Lagerbestand wird von 10 auf 6 reduziert. Die reduzierte Menge von 4 wird der Erstellung von Arbeit für Qualitätsprüfungsaufträge zugeteilt.

2. **Prüfen Sie den ersten erstellten Qualitätsprüfungsauftrag (Menge = 5). Die Arbeit für Qualitätsprüfungsaufträge wird für eine Menge von 5 erstellt.**

    Die Erstellung von Arbeit für Qualitätsprüfungsaufträge wird durch eine Änderung der Menge für die Sperrung von Lagerbestand ausgelöst. Da die Summe der Mengen der Qualitätsprüfungsaufträge 6 betrug, führt die Prüfung einer Menge von 5 dazu, dass 1 Mengen der Qualitätsprüfungsaufträge zur Prüfung verbleiben. Die Menge für die Sperrung von Lagerbestand wird von 6 auf 1 reduziert. Die reduzierte Menge von 5 wird der Erstellung von Arbeit für Qualitätsprüfungsaufträge zugeteilt.

3. **Prüfen Sie den dritten erstellten Qualitätsprüfungsauftrag (Menge = 1). Die Arbeit für Qualitätsprüfungsaufträge wird für eine Menge von 1 erstellt.**

    Die Erstellung von Arbeit für Qualitätsprüfungsaufträge wird durch eine Änderung der Menge für die Sperrung von Lagerbestand ausgelöst. Da die Summe der Mengen der Qualitätsprüfungsaufträge 1 betrug, führt die Prüfung einer Menge von 1 dazu, dass 0 (null) Mengen der Qualitätsprüfungsaufträge zur Prüfung verbleiben. Die Sperrung von Lagerbestand wird entfernt (d. h. die Menge für die Sperrung von Lagerbestand wird von 1 auf 0 reduziert). Die reduzierte Menge von 1 wird der Erstellung von Arbeit für Qualitätsprüfungsaufträge zugeteilt.

> [!NOTE]
> Die Erstellung von Arbeit für Qualitätsprüfungsaufträge hängt von der Menge für die Sperrung von Lagerbestand ab, die gegen einen oder mehrere Qualitätsprüfungsaufträge referenziert wird. Wenn die Summe der Mengen der Qualitätsprüfungsaufträge die referenzierte Menge für die Sperrung von Lagerbestand überschreitet, bestimmt die Reihenfolge, in der die Qualitätsprüfungsaufträge geprüft werden, die Erstellung von Arbeit für Qualitätsprüfungsaufträge.

## <a name="canceling-quality-item-sampling-work"></a>Abbrechen von Qualitätsartikelmuster-Arbeit

Sie können die Arbeit abbrechen, die für Qualitätsartikelmuster erstellt wurde. Gehen Sie folgendermaßen vor, um zu steuern, was beim Abbrechen dieser Arbeit geschieht.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerortverwaltungsparameter**.
1. Legen Sie auf der Registerkarte **Allgemein** im Inforegister **Arbeit** die Option **Registrierung bei Arbeitsabbruch aufheben** auf einen der folgenden Werte fest:

    - **Ja** – Wenn die Qualitätsartikelmuster-Arbeit abgebrochen wird, wird der zugehörige Qualitätsprüfungsauftrag gelöscht und die Registrierung für den Bestand wird aufgehoben.
    - **Nein** – Wenn die Qualitätsartikelmuster-Arbeit abgebrochen wird, wird der zugehörige Qualitätsprüfungsauftrag nicht gelöscht und die Registrierung für den Bestand wird nicht aufgehoben.

## <a name="cross-docking"></a>Crossdocking

Sie können Einstellungen für die Qualitätszuordnung verwenden, mit denen Qualitätsartikelmuster-Arbeit erstellt werden. Wenn jedoch neben einer Qualitätszuordnung, die Qualitätsartikelmuster-Arbeit erstellt, Crossdocking vorhanden ist, wird nur Qualitätsartikelmuster-Arbeit erstellt, wenn nur eine ausreichende Menge für Crossdocking vorhanden ist. In Fällen, in denen die Option **Qualitätsprüfungsaufträge für Lagerortprozesse aktivieren** für den empfangenden Lagerort auf _Ja_ festgelegt ist und für das Feld **Zutreffender Lagerorttyp** die Option _Qualitätsmanagement nur für Lagerortprozesse_ für eine Qualitätszuordnung ausgewählt ist, hat die Erstellung von Qualitätsartikelmuster-Arbeit Vorrang für der Erstellung von Arbeit für Crossdocking. Falls die Menge die Anforderungen für Crossdocking überschreitet, erstellt das System weiterhin nur Qualitätsartikelmuster-Arbeit.

## <a name="destructive-testing"></a>Zerstörungstests

Sie können eine Testgruppe definieren, die zerstörende Prüfungen durchführt. Bei einer zerstörenden Prüfung wird davon ausgegangen, dass unabhängig vom Ergebnis die Menge des geprüften Artikels im Rahmen der Prüfung zerstört wird. Die Funktion _Qualitätsmanagement für Lagerortprozesse_ unterstützt zerstörende Prüfungen auf dieselbe Weise wie das Qualitätsmanagement, wenn die Funktion nicht aktiviert ist. Bevor der Qualitätsprüfungsauftrag geprüft werden kann, muss der Qualitätskontrolleur den Entnahmeort für die zerstörte Menge angeben. Sie können die Entnahme auf der Seite mit den Qualitätsprüfungsaufträgen registrieren, indem Sie im Aktionsbereich **Bestand \> Entnahme** auswählen. Nachdem die Entnahme für die Menge für den Qualitätsprüfungsauftrag registriert wurde, kann die Prüfung abgeschlossen werden.

## <a name="example-scenario"></a>Beispielszenario

### <a name="prepare-the-scenario"></a>Vorbereiten des Szenarios

Um dieses Szenario zu bearbeiten, müssen Sie Ihr System folgendermaßen vorbereiten:

- Stellen Sie sicher, dass Demodaten auf dem System installiert sind, und wählen Sie die juristische Person **USMF** aus.
- Aktivieren Sie die Funktion _Qualitätsmanagement für Lagerortprozesse_ in der [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Konfigurieren Sie Lagerort 51 für die Verwendung der Funktion _Qualitätsmanagement für Lagerortprozesse_, indem Sie folgendermaßen vorgehen:

    1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerort \> Lagerorte**.
    1. Wählen Sie Lagerort 51.
    1. Legen Sie im Inforegister **Lagerort** die Option **Qualitätsprüfungsaufträge für Lagerortprozesse aktivieren** auf *Ja* fest.

### <a name="quality-in-setup--move-to-the-quality-control-location"></a>Einrichtung Qualitätseingang – Verschieben zum Ort für die Qualitätskontrolle

Sie müssen jetzt eine Grundeinrichtung vorbereiten, die es Ihrem System ermöglicht, die Funktion _Qualitätsmanagement für Lagerortprozesse_ für den Lagerort 51 zu unterstützen. (Die Demodaten definieren einen Ort für das Qualitätsmanagement mit dem Namen *QMS*. Dieser Ort wird in diesem Szenario mehrmals referenziert.) Sie bereiten die folgenden Elemente vor, wie in den Unterabschnitten dieses Abschnitts beschrieben:

- Arbeitsklasse
- Arbeitsvorlage
- Lagerplatzrichtlinie
- Artikelmusteraufnahme
- Qualitätszuordnung
- Menüelemente des mobilen Geräts

#### <a name="work-class-for-quality-in"></a>Arbeitsklasse für Qualitätseingang

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsklassen**.
1. Erstellen Sie eine Arbeitsklasse und legen Sie die folgenden Werte fest:

    - **Arbeitsklassenkennung:** _Qualitätseingang_
    - **Beschreibung:** _Qualitätsartikelmuster_
    - **Arbeitsauftragstyp:** _Qualitätsartikelmuster_

#### <a name="work-template"></a>Arbeitsvorlage

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsvorlagen**.
1. Legen Sie das Feld **Arbeitsauftragstyp** auf _Qualitätsartikelmuster_ fest.
1. Erstellen Sie eine Arbeitsvorlage und legen Sie die folgenden Werte fest:

    - **Arbeitsvorlage:** _51 Qualität_
    - **Arbeitsvorlagenbeschreibung:** _51 Qualität_

1. Fügen Sie eine Position zur Arbeitsvorlage hinzu und legen Sie die folgenden Werte fest:

    - **Arbeitstyp:** _Entnahme_
    - **Arbeitsklassenkennung:** _Qualitätseingang_

1. Fügen Sie eine zweite Position zur Arbeitsvorlage hinzu und legen Sie die folgenden Werte fest:

    - **Arbeitstyp:** _Einlagern_
    - **Arbeitsklassenkennung:** _Qualitätseingang_

#### <a name="location-directive"></a>Lagerplatzrichtlinie

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerplatzrichtlinien**.
1. Legen Sie das Feld **Arbeitsauftragstyp** auf _Qualitätsartikelmuster_ fest.
1. Erstellen Sie eine Lagerplatzrichtlinie und legen Sie die folgenden Werte fest:

    - **Name:** _51 zu Qualität_
    - **Arbeitstyp:** _Einlagern_
    - **Standort:** 5
    - **Lagerort:** _51_

1. Fügen Sie eine Position für die Lagerplatzrichtlinie hinzu und legen Sie die folgenden Werte fest:

    - **Von Menge:** _1_
    - **Bis Menge:** _1000000_

1. Erstellen Sie eine Lagerplatzrichtlinienaktivität und legen Sie den folgenden Wert fest:

    - **Name:** _Qualität_

1. Wählen Sie für die neue Lagerplatzrichtlinienaktivität die Option **Abfrage bearbeiten** aus und geben Sie einen Datensatz **Bereich** mit folgenden Werten an:

    - **Tabelle:** *Lagerorte*
    - **Feld:** _Lagerortprofilkennung_
    - **Kriterien:** *QMS*

1. Wählen Sie **OK** aus, um die Abfrage und die neue Lagerplatzrichtlinie zu speichern.

Als Nächstes müssen Sie die Reihenfolge der vorhandenen Bestellungs-Lagerplatzrichtlinien für Lagerort 51 ändern. Die Demodaten enthalten zwei Lagerplatzrichtlinien mit einem Wert **Arbeitsauftragstyp** von _Kauf_ : Der eine trägt den Namen _51 QMS_ und der andere den Namen _51 Bestellung direkt_. Um sicherzustellen, dass die Funktion *Qualitätsmanagement für Lagerortprozesse* für Lagerort 51 angewendet wird, müssen Sie sicherstellen, dass die Lagerplatzrichtlinie _51 QMS_ nicht angewendet wird. Anstatt diese Lagerplatzrichtlinie jedoch zu löschen (weil Sie sie möglicherweise zu einem späteren Zeitpunkt verwenden möchten), können Sie einfach die Reihenfolge ändern.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerplatzrichtlinien**.
1. Wählen Sie für das Feld **Arbeitsauftragstyp** die Option _Bestellung_ aus.
1. Wählen Sie in der Sequenzliste die Sequenznummer 5 für die Lagerplatzrichtlinie _51 Bestellung direkt_ aus.
1. Verschieben Sie die ausgewählte Sequenz auf Sequenznummer 4.
1. Überprüfen Sie, ob die Sequenznummer der Lagerplatzrichtlinie _51 QMS_ jetzt mindestens 5 ist.

#### <a name="item-sampling"></a>Artikelmusteraufnahme

Die Funktion _Qualitätsmanagement für Lagerortprozesse_ fügt einige neue Funktionen für die Artikelmusteraufnahme hinzu. Der Wert **Musterumfang** kann jetzt _Auftrag_, _Lieferung_ oder _Ladung_ sein und der Wert **Menge der Artikelmusteraufnahme** kann _Vollständiges Kennzeichen_ sein.

1. Wechseln Sie zu **Lagerverwaltung \> Einstellungen \> Qualitätskontrolle \> Artikelmusteraufnahme**.
1. Erstellen Sie einen Artikelmusteraufnahme-Datensatz und legen Sie die folgenden Werte fest:

    - **Artikelmusteraufnahme:** _3. LP_
    - **Beschreibung:** _Jedes dritte Kennzeichen_
    - **Musterumfang:** _Auftrag_

1. Wählen Sie im Inforegister **Menge der Artikelmusteraufnahme** für das Feld **Mengenspezifikation** die Option _Vollständiges Kennzeichen_ aus.
1. Wählen Sie im Inforegister **Prozess** für das Feld **Pro n-tem Kennzeichen** die Option _3_ aus.
1. Aktivieren Sie im Abschnitt **Nach Lagerdimension** die Optionen **Lagerort** und **Bestandsstatus**.

#### <a name="quality-associations"></a>Qualitätszuordnungen

Erstellen Sie eine Qualitätszuordnung, die die neue Artikelmusteraufnahme verwendet.

1. Wechseln Sie zu **Bestandsverwaltung \> Einstellungen \> Qualitätskontrolle \> Qualitätszuordnungen**.
1. Erstellen Sie einen Qualitätszuordnungsdatensatz und legen Sie die folgenden Werte fest:

    - **Referenztyp:** _Kauf_
    - **Artikelcode:** _Tabelle_
    - **Artikel:** _M9201_
    - **Standort:** _5_

1. Wählen Sie im Inforegister **Prozess** für das Feld **Ereignistyp** die Option *Registrierung* aus.
1. Wählen Sie im Inforegister **Bedingungen** für das Feld **Zutreffender Lagerorttyp** die Option *Qualitätsmanagement nur für Lagerortprozesse*.
1. Wählen Sie im Inforegister **Qualitätsauftragsprozess** für das Feld **Qualitätsverarbeitungsrichtlinie** die Option _Qualitätsprüfungsauftrag erstellen_ aus.
1. Klicken Sie im Inforegister **Spezifikationen** mit der rechten Maustaste in das Feld **Testgruppe** und wählen Sie **Details anzeigen** aus, um die Seite **Testgruppen** zu öffnen.
1. Erstellen Sie auf der Seite **Testgruppen** auf der Registerkarte **Übersicht** des oberen Rasters eine Testgruppe und legen Sie die folgenden Werte fest:

    - **Testgruppe:** _QMS_
    - **Beschreibung:** _QMS Test_
    - **Akzeptable Menge:** _100_
    - **Artikelmusteraufnahme:** _3. LP_ (Auswählen)

1. Fügen Sie auf der Registerkarte **Übersicht** des unteren Rasters einen Datensatz für einen Test hinzu und legen Sie die folgenden Werte fest:

    - **Sequenz:** *1*
    - **Prüfung:** *Anlagenmessung*

1. Legen Sie auf der Registerkarte **Test** des unteren Rasters die folgenden Werte fest:

    - **Testvariablen:** *Bestanden/Fehler*
    - **Standardergebnis:** *Bestanden*

1. Speichern Sie die neue Testgruppe und schließen Sie die Seite **Testgruppen**.
1. Wählen Sie auf der Seite **Qualitätszuordnungen** für das Feld **Testgruppe** die Option **QMS** aus.
1. Speichern Sie den Datensatz.

#### <a name="mobile-device-menu-items-for-quality-in"></a>Menüpunkte für mobile Geräte für Qualitätseingang

Um die Einrichtung zum Verschieben von Waren an den Ort für die Qualitätskontrolle abzuschließen, müssen Sie die Qualitätsartikelmuster-Arbeit über einen Menüpunkt für mobile Geräte verfügbar machen.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.
1. Wählen Sie den Menüpunkt **Kaufeinlagerung** aus.
1. Fügen Sie im Inforegister **Arbeitsklassen** die Arbeitsklassenkennung *Qualitätseingang* hinzu.

#### <a name="summary-your-setup-to-move-goods-to-quality-control"></a>Zusammenfassung: Ihre Einrichtung, um Waren zur Qualitätskontrolle zu verschieben

Sie haben jetzt eine Qualitätszuordnung definiert, die die Funktion *Qualitätsmanagement für Lagerortprozesse* verwendet, um die Erstellung eines Qualitätsprüfungsauftrags auszulösen. Sie haben die Arbeits- und Ortsdaten für Lagerort 51 eingerichtet, um sicherzustellen, dass bei der Kaufregistrierung für Artikel M9201 bestimmte Arbeiten erstellt werden. Diese Einrichtung stellt sicher, dass jede dritte Kennung, die registriert ist, an einen Qualitätslagerort (_QMS_) verschoben wird, und dass ein Qualitätsprüfungsauftrag für die Kennzeichenmenge erstellt wird. Alles andere wird zum Einlagern anstatt zum Ort für die Qualitätskontrolle verschoben.

### <a name="process-quality-management-work"></a>Arbeit für die Prozessqualitätverwaltung

1. Wechseln Sie zu **Beschaffung \> Bestellungen \> Alle Bestellungen**.
1. Erstellen Sie eine Bestellung und legen Sie die folgenden Werte fest:

    - **Lieferantenkonto angeben:** *104*
    - **Lagerort:** *51*

1. Fügen Sie eine Bestellposition hinzu und legen Sie die folgenden Werte fest:

    - **Artikel:** *M9201*
    - **Menge** *20*
    - **UoM:** *ea*
    - **Lagerort:** *51*

1. Notieren Sie sich die Bestellnummer, damit Sie sie später verwenden können.
1. Wechseln Sie zu einem mobilen Gerät oder Emulator, auf dem die Warehouse Management Mobile App ausgeführt wird, und melden Sie sich mit der Benutzer-ID *51* und dem Kennwort *1* am Lagerort 51 an.
1. Wechseln Sie zu **Eingehend \> Kaufempfang** und geben Sie die folgenden Werte ein:

    - **Best.nr.:** Die Nummer der soeben erstellten Bestellung.
    - **Menge:** *5*
    - **Einheit:** *ea*

1. Fahren Sie mit dem Empfang für die Position mit jeweils *5 ea* fort, bis die Position vollständig empfangen ist. (Insgesamt werden vier Kennzeichen erstellt.)
1. Melden Sie sich von der Warehouse Management Mobile App ab.
1. Wechseln Sie im Webclient zu **Beschaffung \> Bestellungen \> Alle Bestellungen**.
1. Suchen und öffnen Sie Ihre Bestellung.
1. Wählen Sie im Bereich **Bestellpositionen** die Position für Artikelnummer *M9201* aus und wechseln Sie dann zu **Bestellpositionen \> Arbeitsdetails**.
1. Beachten Sie, dass es sich bei der zweiten und dritten Arbeitskopfzeile, die erstellt wurden, um reguläre Einlagerungsarbeit handelt, wohingegen es sich bei der ersten und vierten Arbeitskopfzeile um Qualitätsartikelmuster-Arbeit handelt. Dieses Ergebnis steht im Einklang mit den Einstellungen für die Artikelmusteraufnahme, die so konfiguriert ist, dass jedes dritte Kennzeichen gemustert wird.

#### <a name="move-to-the-quality-control-location"></a>Verschieben zum Ort für die Qualitätskontrolle

Sie verschieben nun die Kennzeichen an die entsprechenden Orte. Das erste und vierte Kennzeichen werden an den Ort für die Qualitätskontrolle verschoben, während das zweite und dritte Kennzeichen direkt eingelagert werden.

1. Wechseln Sie zu einem mobilen Gerät oder Emulator, auf dem die Warehouse Management Mobile App ausgeführt wird, und melden Sie sich mit der Benutzer-ID *51* und dem Kennwort *1* am Lagerort 51 an.
1. Wechseln Sie zu **Eingehend \> Kaufeinlagerung** und lagern Sie jedes Kennzeichen aus der vorherigen Prozedur ein, bis alle Arbeiten abgeschlossen sind.

#### <a name="summary-process-quality-management-work"></a>Zusammenfassung: Arbeit für die Prozessqualitätverwaltung

Sie haben nun die Qualitätsartikelmuster-Arbeit für das erste und vierte Kennzeichen ausgeführt, indem Sie sie an den Ort für die Qualitätskontrolle verschoben haben. Sie haben außerdem das zweite und dritte Kennzeichen eingelagert. Der nächste Schritt ist die Prüfung und Kontrolle des Qualitätsprüfungsauftrags.

### <a name="quality-out-setup-move-from-the-quality-control-location-to-storage-or-return"></a>Einrichtung Qualitätsausgang: Verschieben vom Ort für die Qualitätskontrolle zur Einlagerung oder Rückgabe

Wenn Arbeitskräfte Ergebnisse von Qualitätsprüfungsaufträgen melden, generiert das System automatisch Arbeit.

Sie fahren nun mit der erforderlichen grundlegenden Einrichtung von Arbeitsklasse, Arbeitsvorlage und Lagerplatzrichtlinie fort, um das Qualitätsmanagement für Lagerortprozesse zu aktivieren, sodass die erforderliche Arbeit erstellt werden kann, um die Menge für den Qualitätsprüfungsauftrag vom Ort für die Qualitätskontrolle an einen bestimmten Lagerort-Lagerplatz zu verschieben.

#### <a name="work-class-for-quality-out"></a>Arbeitsklasse für Qualitätsausgang

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsklassen**.
1. Erstellen Sie eine Arbeitsklasse und legen Sie die folgenden Werte fest:

    - **Arbeitsklassenkennung:** *Qualitätsausgang*
    - **Beschreibung:** *Qualitätsausgang*
    - **Arbeitsauftragstyp:** *Qualitätsprüfungsauftrag*

#### <a name="work-templates"></a>Arbeitsvorlagen

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsvorlagen**.
1. Ändern Sie den Wert **Arbeitsauftragstyp** zu *Qualitätsprüfungsauftrag*.
1. Erstellen Sie eine Arbeitsvorlage und legen Sie die folgenden Werte fest:

    - **Arbeitsvorlage:** *51 Qualitätsausgang*
    - **Arbeitsvorlagenbeschreibung:** *51 Qualitätsausgang*

1. Fügen Sie eine Position hinzu und legen Sie die folgenden Werte fest:

    - **Arbeitstyp:** *Entnahme*
    - **Arbeitsklassenkennung:** **Qualitätsausgang**

1. Fügen Sie eine zweite Position hinzu und legen Sie die folgenden Werte fest:

    - **Arbeitstyp:** *Einlagern*
    - **Arbeitsklassenkennung:** *Qualitätsausgang*

#### <a name="location-directives"></a>Lagerplatzrichtlinien

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerplatzrichtlinien**.
1. Ändern Sie den Wert **Arbeitsauftragstyp** zu *Qualitätsprüfungsauftrag*.
1. Erstellen Sie eine Lagerplatzrichtlinie und legen Sie die folgenden Werte fest:

    - **Name:** *51 Bestanden*
    - **Arbeitstyp:** *Einlagern*
    - **Standort:** *5*
    - **Lagerort:** *51*

1. Wählen Sie im Aktivitätsbereich **Abfrage bearbeiten** aus, um den Abfrageeditor zu öffnen.
1. Legen Sie auf der Registerkarte **Bereich** die folgenden Werte fest:

    - **Tabelle:** *Qualitätsprüfungsaufträge*
    - **Feld:** *Status*
    - **Kriterien:** *Bestanden*

1. Wählen Sie **OK** aus, um die Abfrage zu speichern und das Dialogfeld zu schließen.
1. Fügen Sie im Inforegister **Positionen** eine Position hinzu und legen Sie die folgenden Werte fest:

    - **Von Menge:** *1*
    - **Bis Menge:** *1000000*

1. Fügen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** eine Zeile hinzu und legen Sie den folgenden Wert fest:

    - **Name:** *Bestanden*

1. Wählen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** die Option **Abfrage bearbeiten** aus, um den Abfrageeditor zu öffnen.
1. Legen Sie auf der Registerkarte **Bereich** die folgenden Werte fest:

    - **Tabelle:** *Lagerorte*
    - **Feld:** *Zonen-ID*
    - **Kriterien:** *Bulk*

1. Wählen Sie **OK** aus, um die Abfrage zu speichern und das Dialogfeld zu schließen.
1. Wählen Sie im Aktivitätsbereich **Speichern** aus, um die neue Lagerplatzrichtlinie zu speichern.
1. Erstellen Sie eine zweite Lagerplatzrichtlinie und legen Sie die folgenden Werte fest:

    - **Name:** *51 Fehler*
    - **Arbeitstyp:** *Einlagern*
    - **Standort:** *5*
    - **Lagerort:** *51*

1. Wählen Sie im Aktivitätsbereich **Abfrage bearbeiten** aus, um den Abfrageeditor zu öffnen.
1. Legen Sie auf der Registerkarte **Bereich** die folgenden Werte fest:

    - **Tabelle:** *Qualitätsprüfungsaufträge*
    - **Feld:** *Status*
    - **Kriterien:** *Fehler*

1. Wählen Sie **OK** aus, um die Abfrage zu speichern und das Dialogfeld zu schließen.
1. Fügen Sie im Inforegister **Positionen** eine Position hinzu und legen Sie die folgenden Werte fest:

    - **Von Menge:** *1*
    - **Bis Menge:** *1000000*

1. Fügen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** eine Zeile hinzu und legen Sie den folgenden Wert fest:

    - **Name:** *Fehler*

1. Wählen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** die Option **Abfrage bearbeiten** aus, um den Abfrageeditor zu öffnen.
1. Legen Sie auf der Registerkarte **Bereich** die folgenden Werte fest:

    - **Tabelle:** *Lagerorte*
    - **Feld:** *Zonen-ID*
    - **Kriterien:** *Zurück*

1. Wählen Sie **OK** aus, um die Abfrage zu speichern und das Dialogfeld zu schließen.
1. Wählen Sie im Aktivitätsbereich **Speichern** aus, um die neue Lagerplatzrichtlinie zu speichern.

#### <a name="mobile-device-menu-items-for-quality-out"></a>Menüpunkte für mobile Geräte für Qualitätsausgang

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.
1. Wählen Sie den Menüpunkt **QMS Einlagerung** aus.
1. Fügen Sie im Inforegister **Arbeitsklassen** die Arbeitsklassenkennung *Qualitätseinlagerung* hinzu.

Lagerarbeiter können jetzt mithilfe des Menüpunkts **QMS Einlagerung** Arbeit für Qualitätsprüfungsaufträge auswählen. Waren, die durch die Qualitätskontrolle gefallen sind, können an einem Rückgabeort abgelegt werden. Waren mit bestandener Qualitätskontrolle können an den Lagerort „Bulk-001“ gebracht werden.

#### <a name="summary-your-setup-to-move-goods-from-quality-control"></a>Zusammenfassung: Ihre Einrichtung, um Waren von der Qualitätskontrolle zu verschieben

Sie haben die Arbeits- und Ortsdaten für Lagerort 51 eingerichtet, um sicherzustellen, dass beim Abschluss von Qualitätsprüfungsaufträgen Arbeiten automatisch erstellt werden. Diese Einrichtung stellt sicher, dass jedes Kennzeichen nach der Qualitätskontrolle entweder an einen Sammellagerort oder an einen Rückgabeort verschoben wird.

### <a name="process-quality-management-work"></a>Arbeit für die Prozessqualitätverwaltung

1. Wechseln Sie zu **Bestandsverwaltung \> Periodische Aufgaben \> Qualitätsmanagement \> Qualitätsprüfungsaufträge**.
1. Wählen Sie den ersten Qualitätsprüfungsauftrag für die registrierten Mengen aus.
1. Wählen Sie **Überprüfen** aus. Der Status des Tests wird auf *Fehler* aktualisiert.
1. Wechseln Sie zu **Lagerortverwaltung \> Alle Arbeit**.
1. Öffnen Sie die soeben erstellte Arbeit und beachten Sie, dass der Wert **Arbeitsauftragstyp** auf *Qualitätsprüfungsauftrag* festgelegt ist. Die Arbeit enthält eine Position, für die der Einlieferungslagerplatz *Zurück* und der Status *Fehler* lauten. (Wenn der Status des Qualitätsprüfungsauftrags *Bestanden* lauten würde, wäre der Einlieferungslagerplatz stattdessen *Bulk*.)
1. Wechseln Sie zurück zu **Bestandsverwaltung \> Periodische Aufgaben \> Qualitätsmanagement \> Qualitätsprüfungsaufträge**.
1. Wählen Sie den zweiten Qualitätsprüfungsauftrag für die registrierten Artikel aus.
1. Wählen Sie **Ergebnisse** oberhalb dem unteren Raster aus. Aktualisieren Sie den Wert **Ergebnismenge** zu *5* und prüfen Sie, ob der Wert **Testergebnis** in ein Häkchen geändert wurde.
1. Wählen Sie **Prüfen** aus und schließen Sie die Seite.
1. Wählen Sie auf der Seite **Qualitätsprüfungsaufträge** die Option **Prüfen** aus und führen Sie die Prüfung durch. Der Status wird zu *Bestanden* aktualisiert.

    > [!NOTE]
    > Das Prüfereignis löst die Erstellung der Arbeit für Qualitätsprüfungsaufträge aus, um die Menge vom Ort für die Qualitätskontrolle an einen neuen Lagerort zu verschieben.

1. Wechseln Sie zu **Lagerortverwaltung \> Alle Arbeit**.
1. Wählen Sie die gerade erstellte Arbeit aus und beachten Sie, dass ein zweiter Arbeitskopf für den Qualitätsprüfungsauftrag erstellt wurde, in dem der Einlieferungslagerplatz *BULK-001* ist.
1. Wechseln Sie zu einem mobilen Gerät oder Emulator, auf dem die Warehouse Management Mobile App ausgeführt wird, und melden Sie sich mit der Benutzer-ID *51* und dem Kennwort *1* am Lagerort 51 an.
1. Wechseln Sie zu **Qualität \> Aus QMS einlagern** und verarbeiten Sie jedes der zwei Kennzeichen, die mit beiden Arbeiten in Zusammenhang stehen, sodass alle Arbeiten abgeschlossen werden.

> [!NOTE]
> Ziehen Sie es in Betracht, den Eintrag für den Qualitätsausgang zu einem Menüpunkt für mobile Geräte hinzuzufügen, für den der Aktivitätscode *Offene Arbeitsliste anzeigen* lautet. Ein Beispiel stellt der Menüpunkt für mobile Geräte mit dem Namen **Arbeitsliste** in den Demodaten dar. Fügen Sie zuerst die Arbeitsklasse *Qualitätsprüfungsauftrag* zu einem benutzergesteuerten Menüpunkt hinzu, da diese Arbeitsklasse erforderlich ist, damit die Arbeit in der Arbeitsliste angezeigt wird. Fügen Sie die Arbeitsklasse *Qualitätsprüfungsauftrag* anschließend dem Menüpunkt **Arbeitsliste** hinzu. Benutzer, die Zugriff auf die Arbeitsliste haben, können dann die Arbeit auswählen und verarbeiten, die durch die Prüfung des Qualitätsprüfungsauftrags automatisch generiert wird.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Überblick über Qualitätsmanagement und Qualitätsmangel](quality-management-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]