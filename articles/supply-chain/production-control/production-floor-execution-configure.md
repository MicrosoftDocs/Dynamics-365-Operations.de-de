---
title: Produktionsausführungsschnittstelle konfigurieren
description: In diesem Thema wird beschrieben, wie Sie eine oder mehrere Konfigurationen für die Produktionsoberflächen-Ausführungsschnittstelle erstellen. Wenn Sie die Produktionsausführungsoberfläche öffnen, wird automatisch eine ausgewählte Konfiguration und ein Auftragsfilter geladen, die für den Browser und das Gerät spezifisch sind. In der Konfiguration legen Sie die Richtlinien fest, die für eine bestimmte Verwendung gelten müssen.
author: johanhoffmann
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: ff68761ce1cf2174be8ebb9732b9348439a53a32
ms.sourcegitcommit: d24ebce50421f8656d23bb1e47cd636ad2e2ca0a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/02/2020
ms.locfileid: "4664295"
---
# <a name="configure-the-production-floor-execution-interface"></a>Produktionsausführungsschnittstelle konfigurieren

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Werkstattmitarbeiter nutzen die Produktionsausführungsschnittstelle, um ihre tägliche Arbeit zu registrieren, z. B. wenn Einzelvorgänge gestartet werden, Feedback zu Einzelvorgängen gemeldet, indirekte Aktivitäten registriert und Abwesenheit gemeldet werden. Diese Registrierungen sind die Grundlage für die Verfolgung von Fortschritt und Kosten bei Produktionsaufträgen und für die Berechnung der Grundlage für die Bezahlung von Arbeitnehmer.

Wenn Sie die Produktionsausführungsoberfläche öffnen, wird automatisch eine ausgewählte Konfiguration und ein Auftragsfilter geladen, die für den Browser und das Gerät spezifisch sind. In der Konfiguration legen Sie die Richtlinien fest, die für eine bestimmte Verwendung gelten müssen. Im Folgenden finden Sie einige Verbrauchsbeispiele hierfür:

- Auf einem Gerät in der Firmenhalle stempeln Mitarbeiter ein, wenn sie ins Büro kommen, und sie stempeln aus, wenn sie nach Hause gehen.
- Auf einem Gerät in der Werkstatt registrieren sich Maschinenbediener, wenn sie Aufträge starten und abschließen. Sie erfassen auch Pausen und indirekte Aktivitäten.

In diesem Thema werden die verschiedenen Optionen zum Konfigurieren der Einzelvorgangskartengeräte beschrieben.

## <a name="turn-on-the-production-floor-execution-interface-and-its-related-optional-features"></a>Aktivieren Sie die Produktionsausführungsoberfläche und die zugehörigen optionalen Funktionen

Die Produktionsausführungsoberfläche selbst sowie mehrere der optionalen Einstellungen, die in diesem Thema beschrieben werden, müssen in Ihrem System aktiviert werden, bevor Sie sie verwenden können. Verwenden Sie die Seite [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), um eine oder alle der in den folgenden Unterabschnitten beschriebenen Funktionen je nach Bedarf zu aktivieren.

### <a name="the-production-floor-execution-interface"></a>Die Produktionsausführungsoberfläche

Dies ist die wichtigste Funktion, die in diesem Thema beschrieben wird. Sie fügt die Produktionsausführungsoberfläche zu Ihrem System hinzu. Um sie zu aktivieren, schalten Sie die folgende Funktion in der [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ein:  
- Produktionsbereich-Ausführung

### <a name="generate-license-plates"></a>Generieren von Ladungsträgern

Diese Funktionen machen die Funktionalität der Ladungsträger für die Produktionsausführungsoberfläche verfügbar. Wenn Sie sie nutzen möchten, schalten Sie die folgenden Funktionen in [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ein (in dieser Reihenfolge):

1. Das Kennzeichen für Fertigmeldung wurde zum Einzelvorgangslistengerät hinzugefügt.
1. Aktivieren Sie die automatische Generierung der Kennzeichennummer, wenn die Berichtserstellung im Einzelvorgangskartengerät abgeschlossen wurde

### <a name="print-labels"></a>Beschriftungen drucken

Diese Funktionen machen die Funktionalität des Etikettendrucks für die Produktionsausführungsoberfläche verfügbar. Wenn Sie sie nutzen möchten, schalten Sie die folgenden Funktionen in [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ein (in dieser Reihenfolge):

1. Das Kennzeichen für Fertigmeldung wurde zum Einzelvorgangslistengerät hinzugefügt.
1. Beschriftung vom Einzelvorgangs-Kartengerät aus drucken

### <a name="allow-locking-the-touch-screen"></a>Sperren des Touchscreens erlauben

Diese Funktion fügt der Produktionsausführungsoberfläche eine Schaltfläche hinzu, die es den Arbeitskräften ermöglicht, den Touchscreen zu desinfizieren. Wenn Sie diese Funktion nutzen möchten, aktivieren Sie die folgende Funktion in [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- Funktion zum Sperren von Jobkartengerät und Jobkartenterminal, damit sie saniert werden können

## <a name="work-with-production-floor-execution-configurations"></a>Arbeiten mit Produktionsausführungsoberflächen-Konfigurationen

Um Gerätekonfigurationen zu erstellen und zu verwalten, gehen Sie zu **Produktionskontrolle \> Einrichtung \> Fertigungsausführung \> Konfigurieren Sie die Ausführung der Produktionsfläche**. Die Seite **Konfigurieren Sie die Ausführung der Produktionsfläche** zeigt eine Liste der vorhandenen Konfigurationen. Auf dieser Seite können folgende Aktivitäten ausgeführt werden:

- Wählen Sie eine Produktionsausführungskonfiguration aus, die in der linken Spalte aufgeführt ist, um sie anzuzeigen und zu bearbeiten.
- Wählen **Neu** im Aktivitätsbereich, um der Liste eine neue Gerätekonfiguration hinzuzufügen. Dann geben Sie im Feld **Konfiguration** einen Namen ein, um die neue Konfiguration identifizieren zu können. Der Name, den Sie eingeben, muss für alle Gerätekonfigurationen eindeutig sein und kann später nicht mehr bearbeitet werden.

Konfigurieren Sie als Nächstes die verschiedenen Einstellungen für die ausgewählte Gerätekonfiguration. Folgende Felder sind verfügbar:

- **Menge beim Ausstempeln melden** – Stellen Sie diese Option auf *Ja* ein, um die Mitarbeiter aufzufordern, beim Ausstempeln Feedback zu laufenden Vorgängen zu melden. Wird diese Option auf *Nein* eingestellt, werden Arbeiter nicht dazu aufgefordert.
- **Mitarbeiter sperren** – Wenn diese Option auf *Nein* eingestellt ist, werden die Arbeitnehmer sofort nach der Registrierung abgemeldet (z. B. bei einem neuen Einzelvorgang). Das Gerät kehrt dann zur Anmeldeseite zurück. Wenn diese Option auf *Ja* festgelegt ist, bleibt jeder Mitarbeiter am Einzelvorgangsgerät angemeldet. Ein Mitarbeiter kann sich jedoch manuell abmelden, damit sich ein anderer Mitarbeiter anmelden kann, während das Einzelvorgangsgerät weiterhin unter demselben Systembenutzerkonto ausgeführt wird. Weitere Informationen zu diesen Arten von Konten finden Sie unter [Zugewiesene Benutzer](config-job-card-device.md#assigned-users).
- **Verwenden Sie den tatsächlichen Zeitpunkt der Registrierung** – Stellen Sie diese Option auf *Ja* ein, um die Zeit für jede neue Registrierung so festzulegen, dass sie genau der Zeit entspricht, zu der die Registrierung von einem Arbeitnehmer eingereicht wurde. Wenn diese Option auf *Nein* eingestellt wird, wird stattdessen die Anmeldezeit verwendet. Normalerweise möchten Sie diese auf *Ja* einstellen, wenn Sie die Optionen **Mitarbeiter sperren** und/oder **Einzelner Arbeiter** auf *Ja* festgelegt haben, falls Mitarbeiter häufig länger angemeldet bleiben.
- **Einzelne Arbeitskraft** – Setzen Sie diese Option auf *Ja*, wenn nur ein Mitarbeiter jedes Einzelvorgangsgerät verwendet, auf dem diese Konfiguration aktiv ist. Wenn diese Option auf *Ja* festgelegt ist, wird die Option **Mitarbeiter sperren** automatisch auf *Ja* festgelegt. Darüber hinaus entfällt mit dieser Einstellung die Anforderung (und Fähigkeit), dass sich der Mitarbeiter mit einer Ausweis-ID (oder ähnlichem) anmelden muss. Stattdessen meldet sich der Mitarbeiter bei Microsoft Dynamics 365 Supply Chain Management mit einem Systembenutzerkonto an, das mit einer *Zeit registrierten Arbeitskraft* (von der *Arbeitskräfte* Tabelle) verknüpft ist und gleichzeitig als diese Arbeitskraft am Einzelvorgangsgerät angemeldet wird.
- **Erlauben Sie das Sperren des Touchscreens** – Setzen Sie diese Option auf *Ja*, damit Mitarbeiter den Touchscreen vom Einzelvorganggerät sperren können, damit sie ihn bereinigen können. Wenn diese Option auf *Ja* eingestellt ist, wird eine Schaltfläche **Sperrbildschirm zum Desinfizieren** der Anmeldeseite des Geräts hinzugefügt. Wenn ein Mitarbeiter diese Schaltfläche auswählt, wird der Touchscreen vorübergehend gesperrt, um unbeabsichtigte Eingaben zu verhindern. Ein Countdown-Timer wird ebenfalls angezeigt. Die Arbeitskraft kann dann das Gerät und den Bildschirm sicher reinigen. Nach Abschluss des Countdowns wird der Touchscreen automatisch wieder entsperrt.
- **Dauer der Bildschirmsperre** – Wenn die Option **Sperren des Touchscreens zulassen** auf *Ja* festgelegt ist, verwenden Sie diese Option, um anzugeben, wieviele Sekunden der Touchscreen für die Bereinigung gesperrt werden soll. Die Dauer muss eine Zahl zwischen 5 und 120 Sekunden sein.
- **Kennzeichen erstellen** – Setzen Sie diese Option auf *Ja*, um jedes Mal eine neue Kennzeichnung zu erstellen, wenn ein Mitarbeiter das Einzelvorgangsgerät verwendet, um den Vorgang als beendet zu melden. Das Kennzeichen wird aus einer Nummernfolge generiert, die auf der Seite **Lagerverwaltungsparameter** erstellt wird. Wenn diese Option auf *Nein* festgelegt ist, muss die Arbeitskraft eine bestehende Kennzeichnung definieren, wenn er den Vorgang als beendet meldet.
- **Etikett drucken** – Setzen Sie diese Option auf *Ja*, um ein Kennzeichenetikett zu drucken, wenn eine Arbeitskraft das Einzelvorgangskartengerät verwendet, um dann den Vorgang als beendet zu melden. Die Konfiguration des Etiketts wird im Dokumentrouting eingerichtet, wie beschrieben in [Dokumenten-Routing-Layout für Kennzeichenetiketten](../warehousing/document-routing-layout-for-license-plates.md).
- **Registerkartenauswahl** - Verwenden Sie die Einstellungen in diesem Abschnitt, um festzulegen, welche Registerkarten von der Produktionsausführungsoberfläche angezeigt werden sollen, wenn die aktuelle Konfiguration aktiv ist. Sie können so viele Registerkarten entwerfen, wie Sie benötigen, und diese dann hier nach Bedarf hinzufügen und anordnen. Details zum Gestalten von Registerkarten und zum Arbeiten mit den Einstellungen hier finden Sie unter [Gestalten der Produktionsausführungsoberfläche](production-floor-execution-tabs.md).

## <a name="clean-up-job-configurations"></a>Bereinigen Sie die Einzelvorgangskonfigurationen

Wenn der Fertigungsleiter die Produktionsausführungsschnittstelle einrichtet, wählt er eine Konfiguration und einen Auftragsfilter aus. Diese Auswahlen werden in einer Referenztabelle in Supply Chain Management gespeichert und der Browser verwendet eine ID, die in einem lokalen Cookie gespeichert ist, um die richtige Zeile in dieser Tabelle zu finden. In der Tabelle werden auch Datum und Uhrzeit protokolliert, zu denen sich ein Mitarbeiter zuletzt bei jedem Gerät angemeldet hat.

Ein Chargen-Einzelvorgang bereinigt regelmäßig Einträge in der Referenztabelle für Geräte, die in den letzten 60 Tagen keine Aktivität protokolliert haben. Sie können die Einträge auch jederzeit manuell bereinigen, indem Sie die folgenden Schritte ausführen.

1. Gehen Sie zu **Produktionskontrolle \> Einrichtung \> Fertigungsausführung \> Ausführung in der Produktion**.
1. Wählen Sie im Aktionsbereich die Option **Bereinigen Sie Client-Konfigurationen** aus.
1. In dem Dialogfeld **Bereinigen Sie die Client-Konfiguration** stellen Sie das Feld **Anzahl der Tage** auf die Anzahl der Tage der Inaktivität (vor heute) ein, die zu berücksichtigen sind. Sie entfernen alle Konfigurationen und Anmeldedatensätze für Geräte, die während dieser Zeit nicht aktiv waren.
1. Wählen Sie **OK**, um die relevanten Konfigurationen zu bereinigen, basierend auf der Eisntellung **Anzahl der Tage**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]