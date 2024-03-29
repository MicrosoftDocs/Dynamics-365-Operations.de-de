---
title: Produktionsausführungsschnittstelle konfigurieren
description: In diesem Artikel wird beschrieben, wie Sie eine oder mehrere Konfigurationen für die Produktionsoberflächen-Ausführungsschnittstelle erstellen. Wenn Sie die Produktionsausführungsoberfläche öffnen, wird automatisch eine ausgewählte Konfiguration und ein Auftragsfilter geladen, die für den Browser und das Gerät spezifisch sind. In der Konfiguration legen Sie die Richtlinien fest, die für eine bestimmte Verwendung gelten müssen.
author: johanhoffmann
ms.date: 11/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecutionConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 641b293617df608bc07b97c077dbcd05664f8e2a
ms.sourcegitcommit: 4abf9b375fed6885ea11a425c524958fea29c3b9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2022
ms.locfileid: "9748685"
---
# <a name="configure-the-production-floor-execution-interface"></a>Produktionsausführungsschnittstelle konfigurieren

[!include [banner](../includes/banner.md)]

Werkstattmitarbeiter nutzen die Produktionsausführungsschnittstelle, um ihre tägliche Arbeit zu registrieren, z. B. wenn Einzelvorgänge gestartet werden, Feedback zu Einzelvorgängen gemeldet, indirekte Aktivitäten registriert und Abwesenheit gemeldet werden. Diese Registrierungen sind die Grundlage für die Verfolgung von Fortschritt und Kosten bei Produktionsaufträgen und für die Berechnung der Grundlage für die Bezahlung von Arbeitnehmer.

Wenn Sie die Produktionsausführungsoberfläche öffnen, wird automatisch eine ausgewählte Konfiguration und ein Auftragsfilter geladen, die für den Browser und das Gerät spezifisch sind. In der Konfiguration legen Sie die Richtlinien fest, die für eine bestimmte Verwendung gelten müssen. Im Folgenden finden Sie einige Verbrauchsbeispiele hierfür:

- Auf einem Gerät in der Firmenhalle stempeln Mitarbeiter ein, wenn sie ins Büro kommen, und sie stempeln aus, wenn sie nach Hause gehen.
- Auf einem Gerät in der Werkstatt registrieren sich Maschinenbediener, wenn sie Aufträge starten und abschließen. Sie erfassen auch Pausen und indirekte Aktivitäten.

In diesem Artikel werden die verschiedenen Optionen zum Konfigurieren einer Produktionsausführungsschnittstelle für jedes Gerät beschrieben, das an Ihrem Standort verwendet wird.

## <a name="turn-on-the-production-floor-execution-interface-and-its-related-optional-features"></a>Aktivieren Sie die Produktionsausführungsoberfläche und die zugehörigen optionalen Funktionen

Die Produktionsausführungsoberfläche selbst sowie mehrere der optionalen Einstellungen, die in diesem Artikel beschrieben werden, müssen für Ihr System aktiviert werden, bevor Sie sie verwenden können. Verwenden Sie die Seite [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), um eine oder alle der in den folgenden Unterabschnitten beschriebenen Funktionen je nach Bedarf zu aktivieren.

### <a name="the-production-floor-execution-interface"></a>Die Produktionsausführungsoberfläche

Dies ist die primäre in diesem Artikel beschriebene Funktion und eine Voraussetzung für alle anderen in diesem Abschnitt erwähnten Funktionen. Ab Supply Chain Management 10.0.25 ist es obligatorisch und kann nicht deaktiviert werden. Wenn Sie eine ältere Version als 10.0.25 ausführen, können Administratoren diese Funktionalität ein- oder ausschalten, indem sie nach der Funktion *Produktionsausführung* im Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="generate-license-plates"></a>Generieren von Ladungsträgern

Diese Funktionen machen die Funktionalität der Ladungsträger für die Produktionsausführungsoberfläche verfügbar. Wenn Sie sie nutzen möchten, schalten Sie die folgenden Funktionen in [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ein (in dieser Reihenfolge):

1. *Das Kennzeichen für Fertigmeldung wurde zum Einzelvorgangslistengerät hinzugefügt.*<br>(Ab Supply Chain Management Version 10.0.21 ist diese Funktion standardmäßig aktiviert. Ab Supply Chain Management Version 10.0.25 ist diese Funktion obligatorisch.)
1. *Aktivieren Sie die automatische Generierung der Kennzeichennummer, wenn die Berichtserstellung im Einzelvorgangskartengerät abgeschlossen wurde*<br>(Ab Supply Chain Management Version 10.0.25 ist diese Funktion obligatorisch.)

### <a name="print-labels"></a>Beschriftungen drucken

Diese Funktionen machen die Funktionalität des Etikettendrucks für die Produktionsausführungsoberfläche verfügbar. Wenn Sie sie nutzen möchten, schalten Sie die folgenden Funktionen in [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ein (in dieser Reihenfolge):

1. *Das Kennzeichen für Fertigmeldung wurde zum Einzelvorgangslistengerät hinzugefügt.*<br>(Ab Supply Chain Management Version 10.0.21 ist diese Funktion standardmäßig aktiviert. Ab Supply Chain Management Version 10.0.25 ist diese Funktion obligatorisch.)
1. *Beschriftung vom Einzelvorgangs-Kartengerät aus drucken*<br>(Ab Supply Chain Management Version 10.0.25 ist diese Funktion obligatorisch.)

### <a name="allow-locking-the-touch-screen"></a>Sperren des Touchscreens erlauben

Diese Funktion ermöglicht es Mitarbeitern, den Touchscreen zu sperren, damit sie ihn desinfizieren können.

Ab Supply Chain Management Version 10.0.21 ist diese Funktion standardmäßig aktiviert. Ab Supply Chain Management 10.0.25 ist diese Funktion obligatorisch und kann nicht deaktiviert werden. Wenn Sie eine ältere Version als 10.0.25 ausführen, können Administratoren diese Funktionalität ein- oder ausschalten, indem sie nach der Funktion *Funktion zum Sperren des Einzelvorgangs-Kartengeräts und des Einzelvorgangs-Kartenterminals zur Desinfektion* im Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) suchen.

### <a name="asset-management-functionality-for-the-production-floor-execution-interface"></a>Anlagenverwaltungsfunktion für die Produktionsumgebungs-Ausführungsschnittstelle

Diese Funktion fügt der Produktionsausführungsoberfläche eine Registerkarte für die Anlagenverwaltung hinzu. Auf dieser Registerkarte können Arbeitskräfte eine Anlage auswählen, die mit einer Maschinenressource verbunden ist, die sich im ausgewählten Filter der Auftragsliste befindet. Für die ausgewählte Maschinenanlage kann die Arbeitskraft den Status und den Zustand der Anlage anhand von Zählerwerten für bis zu vier ausgewählte Zähler anzeigen.

Ab Supply Chain Management Version 10.0.25 ist diese Funktion standardmäßig aktiviert. Ab Supply Chain Management Version 10.0.29 ist diese Funktion obligatorisch und kann nicht deaktiviert werden. Wenn Sie eine ältere Version als 10.0.29 ausführen, können Administratoren diese Funktionalität ein- oder ausschalten, indem sie nach der Funktion *Anlagenverwaltungsfunktion für die Produktionsumgebungs-Ausführungsschnittstelle* im Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) suchen.

### <a name="job-search"></a>Einzelvorgangssuche

Diese Funktion ermöglicht das Hinzufügen eines Suchfelds zur Einzelvorgangsliste. Mitarbeiter können einen bestimmten Einzelvorgang finden, indem sie die Job-ID eingeben, oder alle Jobs für einen bestimmten Auftrag finden, indem sie die Auftrags-ID eingeben. Arbeitskräfte können die ID über eine Tastatur oder durch Scannen eines Barcodes eingeben.

Ab Supply Chain Management Version 10.0.25 ist diese Funktion standardmäßig aktiviert. Ab Supply Chain Management Version 10.0.29 ist diese Funktion obligatorisch und kann nicht deaktiviert werden. Wenn Sie eine ältere Version als 10.0.29 ausführen, können Administratoren diese Funktionalität ein- oder ausschalten, indem sie nach der Funktion *Einzelvorgangssuche für die Produktionsausführungsoberfläche* im Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) suchen.

### <a name="report-on-co-products-and-by-products"></a>Berichte zu Kuppel- und Nebenprodukten

Mit dieser Funktion können Mitarbeiter die Ausführungsschnittstelle der Produktionshalle verwenden, um den Fortschritt von Batchaufträgen zu melden. Diese Berichte umfassen Kuppel- und Nebenprodukten.

Um diese Funktion nutzen zu können, muss sie für Ihr System aktiviert werden. Ab Supply Chain Management Version 10.0.29 ist die Funktion standardmäßig aktiviert. Admins können diese Funktion ein- oder ausschalten, indem sie nach der Funktion *Bericht zu Kuppel- und Nebenprodukten von der Produktionsausführungsoberfläche* im Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) suchen.

### <a name="display-full-serial-batch-and-license-plate-numbers"></a>Vollständige Serien-, Batch- und Kennzeichennummern

Diese Funktion bietet eine verbesserte Erfahrung beim Anzeigen von Listen von Serien-, Chargen- und Kennzeichennummern in der Produktionsausführungsoberfläche. Die Anzeige wechselt von einer Kartenansicht, die eine begrenzte Anzahl von Zeichen anzeigt, zu einer Listenansicht, die genügend Platz für die Anzeige der vollständigen Werte bietet. Die Liste bietet auch die Möglichkeit, nach bestimmten Nummern zu suchen.

Um diese Funktion nutzen zu können, muss sie für Ihr System aktiviert werden. Ab Supply Chain Management Version 10.0.25 ist die Funktion standardmäßig aktiviert. Ab Supply Chain Management Version 10.0.29 ist die Funktion obligatorisch und kann nicht deaktiviert werden. Wenn Sie eine ältere Version als 10.0.29 verwenden, können Administratoren diese Funktion ein- oder ausschalten, indem sie im Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) nach der Funktion *Vollständige Serien-, Batch- und Kennzeichennummern in der Produktionsausführungsoberfläche anzeigen* suchen.

Ab Supply Chain Management Version 10.0.25 ist diese Funktion standardmäßig aktiviert. Admins können diese Funktion ein- oder ausschalten, indem sie im Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) nach der Funktion *Vollständige Serien-, Batch- und Ladungsträger-Nummern in der Produktionsausführungsoberfläche anzeigen* suchen.

### <a name="register-material-consumption"></a>Materialverbrauch registrieren

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until further notice -->

Diese Funktion ermöglicht es Arbeitern, die Produktionsausführungsoberfläche zu verwenden, um Materialverbrauch, Chargennummern und Seriennummern zu registrieren. Einige Hersteller, insbesondere in der Prozessindustrie, müssen explizit die Materialmenge registrieren, die für jede Batch oder jeden Produktionsauftrag verbraucht wird. Arbeitskräfte könnten zum Beispiel eine Waage verwenden, um die Menge des Materials zu wiegen, das sie bei ihrer Arbeit verbrauchen. Um eine vollständige Rückverfolgbarkeit der Materialien zu gewährleisten, müssen diese Organisationen auch die Batch-Nummern registrieren, die zur Herstellung der einzelnen Produkte verbraucht wurden.

Es gibt zwei Versionen dieser Funktion. Man unterstützt Artikel, die *nicht* für die Verwendung von Lagerverwaltungsprozessen (WMS) aktiviert sind. Die anderen unterstützen Elemente, die *für die Verwendung von WMS aktiviert sind*. Um diese Funktionalität zu nutzen, aktivieren Sie eine oder beide der folgenden Funktionen in [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (in dieser Reihenfolge), je nachdem, ob Sie Artikel haben, die für WMS aktiviert sind:

- *Materialverbrauch in der Produktionsausführungsoberfläche (nicht WMS) registrieren*
- *(Vorschauversion) Materialverbrauch in der Produktionsausführungsoberfläche registrieren (WMS-fähig)*

> [!IMPORTANT]
> Sie können die Nicht-WMS-Funktion allein verwenden. Wenn Sie jedoch WMS verwenden, müssen Sie beide Funktionen aktivieren.

### <a name="report-on-catch-weight-items"></a>Bericht zu Artikelgewichtsartikel

Arbeitskräfte können die Produktionsausführungsoberfläche verwenden, um den Fortschritt bei Batch-Aufträgen für Artikel mit Artikelgewicht zu melden. Batch-Aufträge werden aus Formeln erstellt, die so definiert werden können, dass Artikelgewichte als Formelpositionen, Kuppelprodukte und Nebenprodukte enthalten sind. Eine Formel kann auch so definiert werden, dass sie Formelzeilen für Zutaten enthält, die für das Artikelgewicht definiert sind. Artikel mit Artikelgewicht verwenden zwei Maßeinheiten, um den Bestand zu verfolgen: die Menge des Artikelgewichts und die Menge des Bestands. In der Lebensmittelbranche kann z.B. verpacktes Fleisch als Element mit Artikelgewicht definiert werden, wobei die Menge des Artikelgewichts zur Erfassung der Anzahl der Kartons und die Bestandsmenge zur Erfassung des Gewichts der Kartons verwendet wird.

Um diese Funktion zu nutzen, schalten Sie die folgende Funktion in [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ein:

- *Bericht über Artikel mit Artikelgewicht über die Produktionsausführungsoberfläche*

### <a name="the-my-day-dialog"></a>Dialogfeld „Mein Tag“ anzeigen

Das **Mein Tag**-Dialogfeld bietet den Mitarbeitern einen Überblick über ihre täglichen Erfassungen und aktuellen Salden für bezahlte Zeit, bezahlte Überstunden, Abwesenheit und bezahlte Abwesenheit.

Um diese Funktion nutzen zu können, muss sie für Ihr System aktiviert werden. Ab Supply Chain Management Version 10.0.29 ist die Funktion standardmäßig aktiviert. Admins können diese Funktion ein- oder ausschalten, indem sie nach der Funktion *Ansicht „Mein Tag“ für die Produktionsausführungsoberfläche* im Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) suchen.

### <a name="teams"></a>Teams

Wenn mehrere Arbeitskräfte demselben Produktions-Einzelvorgang zugewiesen werden, können sie ein Team bilden. Das Team kann einen Mitarbeiter als Pilot ernennen. Die verbleibenden Arbeitskräfte werden dann automatisch zu Assistenten dieses Piloten. Für das resultierende Team muss nur der Pilot den Einzelvorgangstatus registrieren. Zeiterfassungen gelten für alle Teammitglieder.

Um diese Funktion zu nutzen, schalten Sie die folgende Funktion in [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ein:

- *Produktionsteams in der Produktionsausführungsoberfläche*

### <a name="additional-configuration-in-the-production-floor-execution-interface"></a>Zusätzliche Konfiguration auf der Produktionsausführungsoberfläche

Diese Funktion fügt der Seite **Produktionsausführung konfigurieren** Einstellungen für die folgende Funktionalität hinzu:

- Öffnen Sie automatisch das **Einzelvorgang starten**-Dialogfeld, wenn eine Suche abgeschlossen ist.
- Öffnen Sie automatisch das **Fortschritt melden**-Dialogfeld, wenn eine Suche abgeschlossen ist.
- Füllen Sie die Restmenge vorab in das **Fortschritt melden**-Dialogfeld.
- Aktivieren Sie Anpassungen des Materialverbrauchs über das Dialogfeld **Fortschritt melden**. (Diese Funktionalität erfordert auch die Funktion *Materialverbrauch in der Produktionsausführungsoberfläche (nicht WMS) registrieren*.)
- Aktivieren Sie Suchen nach Projektkennung.

Informationen zum Verwenden der Einstellungen finden Sie weiter unten in diesem Artikel.

Um diese Funktion zu nutzen, schalten Sie die folgende Funktion in [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ein:

- *Zusätzliche Konfiguration auf der Produktionsausführungsoberfläche*

### <a name="enable-the-my-jobs-tab"></a>Aktivieren Sie die Registerkarte Meine Jobs

Auf der Registerkarte **Meine Aufträge** können Arbeitskräfte ganz einfach alle nicht gestarteten und nicht beendeten Aufträge einsehen, die ihnen speziell zugewiesen sind. Es ist nützlich in Unternehmen, in denen Aufträge manchmal oder immer bestimmten Arbeitskräften (Human Resources) statt anderen Arten von Ressourcen (z.B. Maschinen) zugewiesen werden.

Um diese Funktion zu nutzen, schalten Sie die folgende Funktion in [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ein:

- *Registerkarte Meine Einzelvorgänge auf der Produktionsausführungsoberfläche*

### <a name="enable-use-of-a-numpad-on-the-sign-in-page"></a>Verwendung eines Ziffernblocks auf der Anmeldeseite aktivieren

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until 10.0.31 GA -->

Über diese Funktion können Administratoren ein Ziffernblock-Steuerelement zut Anmeldeseite für die Produktionsausführungsoberfläche hinzufügen. Die Mitarbeiter können sich dann anmelden, indem sie über den Ziffernblock ihre Ausweis-ID oder persönliche Nummer eingeben.

Um diese Funktion zu nutzen, schalten Sie die folgende Funktion in [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ein:

- *Verwendung eines Ziffernblocks auf der Anmeldeseite aktivieren*

## <a name="work-with-production-floor-execution-configurations"></a>Arbeiten mit Produktionsausführungsoberflächen-Konfigurationen

Um Produktionsausführungskonfigurationen zu erstellen und zu verwalten, gehen Sie zu **Produktionskontrolle \> Einrichtung \> Fertigungsausführung \> Produktionsausführung konfigurieren**. Die Seite **Konfigurieren Sie die Ausführung der Produktionsfläche** zeigt eine Liste der vorhandenen Konfigurationen. Auf dieser Seite können folgende Aktivitäten ausgeführt werden:

- Wählen Sie eine Produktionsausführungskonfiguration aus, die in der linken Spalte aufgeführt ist, um sie anzuzeigen und zu bearbeiten.
- Wählen Sie im Aktivitätsbereich **Neu** aus , um der Liste eine neue Konfiguration hinzuzufügen. Dann geben Sie im Feld **Konfiguration** einen Namen ein, um die neue Konfiguration identifizieren zu können. Der Name, den Sie eingeben, muss für alle Konfigurationen eindeutig sein und kann später nicht mehr bearbeitet werden. Sie können im Feld **Beschreibung** optional eine Beschreibung der Konfiguration eingeben.

Konfigurieren Sie als Nächstes die verschiedenen Einstellungen für die ausgewählte Konfiguration, wie in den folgenden Unterabschnitten beschrieben.

### <a name="the-general-fasttab"></a>Inforegister „Allgemein“

Die folgenden Einstellungen sind auf dem Inforegister **Allgemein** verfügbar:

- **Nur Ein- und Ausstempeln** – Legen Sie diese Option auf *Ja* fest, um eine vereinfachte Oberfläche zu erstellen, die nur die Ein- und Ausstempelfunktionalität bietet. Durch diese Einstellung werden die meisten anderen Optionen auf dieser Seite deaktiviert. Sie müssen alle Zeilen aus dem Inforegister **Tab-Auswahl** entfernen, bevor Sie diese Option aktivieren können.
- **Suche aktivieren** – Setzen Sie diese Option auf *Ja*, um ein Suchfeld in die Einzelvorgangsliste aufzunehmen. Mitarbeiter können einen bestimmten Einzelvorgang finden, indem sie die Einzelvorgangskennung eingeben, oder alle Einzelvorgänge für einen bestimmten Auftrag finden, indem sie die Auftragskennung eingeben. Arbeitskräfte können die ID über eine Tastatur oder durch Scannen eines Barcodes eingeben.
- **Suche nach Projektkennung aktivieren** – Legen Sie diese Option auf *Ja* fest, um Mitarbeitern zu ermöglichen, nach Projektkennung (zusätzlich zu Einzelvorgangskennung und Auftragskennung) im Suchfeld der Schnittstelle zur Produktionsausführung zu suchen. Sie können diese Option nur dann auf *Ja* festlegen, wenn die Option **Suche aktivieren** ebenfalls auf *Ja* festgelegt ist.
- **Startdialogfeld automatisch öffnen** – Wenn diese Option auf *Ja* festgelegt ist, wird das Dialogfeld **Einzelvorgang starten** automatisch geöffnet, wenn Arbeitskräfte die Suchleiste zur Suche nach einem Einzelvorgang verwenden.
- **Dialogfeld für Berichtsfortschritt automatisch öffnen** – Wenn diese Option auf *Ja* festgelegt ist, wird das Dialogfeld **Fortschritt melden** automatisch geöffnet, wenn Arbeitskräfte die Suchleiste zur Suche nach einem Einzelvorgang verwenden.
- **Anpassen von Material aktivieren** – Legen Sie diese Option auf *Ja* fest, um die Schaltfläche **Material anpassen** im Dialogfeld **Fortschritt melden** zu aktivieren. Arbeitskräfte können diese Schaltfläche auswählen, um den Materialverbrauch für den Einzelvorgang anzupassen.
- **Menge beim Ausstempeln melden** – Stellen Sie diese Option auf *Ja* ein, um die Mitarbeiter aufzufordern, beim Ausstempeln Feedback zu laufenden Vorgängen zu melden. Wird diese Option auf *Nein* eingestellt, werden Arbeiter nicht dazu aufgefordert.
- **Mitarbeiter sperren** – Wenn diese Option auf *Nein* eingestellt ist, werden die Arbeitnehmer sofort nach der Registrierung abgemeldet (z. B. bei einem neuen Einzelvorgang). Die Schnittstelle kehrt dann zur Anmeldeseite zurück. Wenn diese Option auf *Ja* festgelegt ist, bleibt jeder Mitarbeiter in der Produktionsausführungsschnittstelle angemeldet. Ein Mitarbeiter kann sich jedoch manuell abmelden, damit sich ein anderer Mitarbeiter anmelden kann, während die Produktionsausführungsschnittstelle weiterhin unter demselben Systembenutzerkonto ausgeführt wird. Weitere Informationen zu diesen Arten von Konten finden Sie unter [Zugewiesene Benutzer](config-job-card-device.md#assigned-users).
- **Verwenden Sie den tatsächlichen Zeitpunkt der Registrierung** – Stellen Sie diese Option auf *Ja* ein, um die Zeit für jede neue Registrierung so festzulegen, dass sie genau der Zeit entspricht, zu der die Registrierung von einem Arbeitnehmer eingereicht wurde. Wenn diese Option auf *Nein* eingestellt wird, wird stattdessen die Anmeldezeit verwendet. Normalerweise möchten Sie diese auf *Ja* einstellen, wenn Sie die Optionen **Mitarbeiter sperren** und/oder **Einzelner Arbeiter** auf *Ja* festgelegt haben, falls Mitarbeiter häufig länger angemeldet bleiben.
- **Einzelne Arbeitskraft** – Setzen Sie diese Option auf *Ja*, wenn nur ein Mitarbeiter jedes Produktionsausführungsschnittstelle verwendet, auf dem diese Konfiguration aktiv ist. Wenn diese Option auf *Ja* festgelegt ist, wird die Option **Mitarbeiter sperren** automatisch auf *Ja* festgelegt. Darüber hinaus entfällt mit dieser Einstellung die Anforderung (und Fähigkeit), dass sich der Mitarbeiter mit einer Ausweis-ID (oder ähnlichem) anmelden muss. Stattdessen meldet sich der Mitarbeiter bei Microsoft Dynamics 365 Supply Chain Management mit einem Systembenutzerkonto an, das mit einer *Zeit registrierten Arbeitskraft* (von der *Arbeitskräfte* Tabelle) verknüpft ist und gleichzeitig als diese Arbeitskraft in der Produktionsausführungsschnittstelle angemeldet wird.
- **Nummernblock aktivieren** – Stellen Sie diese Option auf *Ja* ein um dem Anmeldebildschirm einen Nummernblock hinzuzufügen, der es den Mitarbeitern ermöglicht, ihre Ausweis-ID oder persönliche Nummer über einen Touchscreen-Nummernblock einzugeben. Legen Sie diese Option auf *Nein* fest, um den Ziffernblock zu entfernen.
- **Erlauben Sie das Sperren des Touchscreens** – Setzen Sie diese Option auf *Ja*, damit Mitarbeiter den Touchscreen der Produktionsausführungsschnittstelle sperren können, damit sie ihn bereinigen können. Wenn diese Option auf *Ja* eingestellt ist, wird eine Schaltfläche **Sperrbildschirm zum Desinfizieren** der Anmeldeseite hinzugefügt. Wenn ein Mitarbeiter diese Schaltfläche auswählt, wird der Touchscreen vorübergehend gesperrt, um unbeabsichtigte Eingaben zu verhindern. Ein Countdown-Timer wird ebenfalls angezeigt. Die Arbeitskraft kann dann das Gerät und den Bildschirm sicher reinigen. Nach Abschluss des Countdowns wird der Touchscreen automatisch wieder entsperrt.
- **Dauer der Bildschirmsperre** – Wenn die Option **Sperren des Touchscreens zulassen** auf *Ja* festgelegt ist, verwenden Sie diese Option, um anzugeben, wieviele Sekunden der Touchscreen für die Bereinigung gesperrt werden soll. Die Dauer muss eine Zahl zwischen 5 und 120 Sekunden sein.
- **Kennzeichen erstellen** – Setzen Sie diese Option auf *Ja*, um jedes Mal eine neue Kennzeichnung zu erstellen, wenn ein Mitarbeiter die Produktionsausführungsschnittstelle verwendet, um den Vorgang als beendet zu melden. Das Kennzeichen wird aus einer Nummernfolge generiert, die auf der Seite **Lagerverwaltungsparameter** erstellt wird. Wenn diese Option auf *Nein* festgelegt ist, muss die Arbeitskraft eine bestehende Kennzeichnung definieren, wenn er den Vorgang als beendet meldet.
- **Etikett drucken** – Setzen Sie diese Option auf *Ja*, um ein Kennzeichenetikett zu drucken, wenn eine Arbeitskraft die Produktionsausführungsschnittstelle verwendet, um dann den Vorgang als beendet zu melden. Die Konfiguration des Labels wird im Document Routing festgelegt, wie in [Document Routing Etikettenlayouts](../warehousing/document-routing-layout-for-license-plates.md) beschrieben.

### <a name="the-tab-selection-fasttab"></a>Inforegister „Registerkartenauswahl“

Verwenden Sie die Einstellungen auf dem Inforegister **Registerkartenauswahl**, um auszuwählen, welche Registerkarten von der Produktionsausführungsoberfläche angezeigt werden sollen, wenn die aktuelle Konfiguration aktiv ist. Sie können beliebig viele Registerkarten entwerfen und diese dann mithilfe der Schaltflächen auf der Inforegister-Symbolleiste nach Bedarf hinzufügen und anordnen. Informationen zum Gestalten von Registerkarten und zum Arbeiten mit den Einstellungen hier finden Sie unter [Produktionsausführungsoberfläche entwerfen](production-floor-execution-tabs.md).

### <a name="the-report-progress-fasttab"></a>Inforegister „Fortschritt melden“

Die folgenden Einstellungen sind auf dem Inforegister **Fortschritt melden** verfügbar:

- **Anpassen von Material aktivieren** – Legen Sie diese Option auf *Ja* fest, um die Schaltfläche **Material anpassen** ins Dialogfeld **Fortschritt melden** einzubeziehen. Arbeitskräfte können diese Schaltfläche auswählen, um den Materialverbrauch für den Einzelvorgang anzupassen.
- **Standardmäßig verbleibende Menge** – Legen Sie diese Option auf *Ja* fest, um die erwartete Restmenge für einen Produktions-Einzelvorgang im Dialogfeld **Fortschritt melden** im Voraus zu füllen.

## <a name="clean-up-job-configurations"></a>Bereinigen Sie die Einzelvorgangskonfigurationen

Wenn der Fertigungsleiter die Produktionsausführungsschnittstelle einrichtet, wählt er eine Konfiguration und einen Auftragsfilter aus. Diese Auswahlen werden in einer Referenztabelle in Supply Chain Management gespeichert und der Browser verwendet eine ID, die in einem lokalen Cookie gespeichert ist, um die richtige Zeile in dieser Tabelle zu finden. In der Tabelle werden auch Datum und Uhrzeit protokolliert, zu denen sich ein Mitarbeiter zuletzt bei jedem Gerät angemeldet hat.

Ein Chargen-Einzelvorgang bereinigt regelmäßig Einträge in der Referenztabelle für Geräte, die in den letzten 60 Tagen keine Aktivität protokolliert haben. Sie können die Einträge auch jederzeit manuell bereinigen, indem Sie die folgenden Schritte ausführen.

1. Gehen Sie zu **Produktionskontrolle \> Einrichtung \> Fertigungsausführung \> Ausführung in der Produktion**.
1. Wählen Sie im Aktionsbereich die Option **Bereinigen Sie Client-Konfigurationen** aus.
1. In dem Dialogfeld **Bereinigen Sie die Client-Konfiguration** stellen Sie das Feld **Anzahl der Tage** auf die Anzahl der Tage der Inaktivität (vor heute) ein, die zu berücksichtigen sind. Sie entfernen alle Konfigurationen und Anmeldedatensätze für Geräte, die während dieser Zeit nicht aktiv waren.
1. Wählen Sie **OK**, um die relevanten Konfigurationen zu bereinigen, basierend auf der Eisntellung **Anzahl der Tage**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
