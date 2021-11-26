---
title: Einzelvorgangsliste für Geräte konfigurieren
description: In diesem Thema werden die verschiedenen Optionen zum Konfigurieren der Einzelvorgangskartengeräts beschrieben.
author: johanhoffmann
ms.date: 05/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch, JmgRegistrationTouchUserConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 0382e34664f20389c43e8dec4437f0078fa1f60a
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/09/2021
ms.locfileid: "7777739"
---
# <a name="configure-job-card-for-devices"></a>Einzelvorgangsliste für Geräte konfigurieren

[!include [banner](../includes/banner.md)]

Das Einzelvorgangsgerät wird von den Mitarbeitern in der Werkstatt verwendet, um ihre tägliche Arbeit zu registrieren, z. B. wenn Vorgänge gestartet werden, Feedback zu Jobs gemeldet, indirekte Aktivitäten registriert und Abwesenheit gemeldet werden. Diese Registrierungen sind die Grundlage für die Verfolgung von Fortschritt und Kosten bei Produktionsaufträgen und für die Berechnung der Grundlage für die Bezahlung der Arbeitnehmer. In diesem Thema werden die verschiedenen Optionen zum Konfigurieren der Einzelvorgangskartengeräte beschrieben.

## <a name="enable-new-features-in-feature-management"></a>Aktivieren neuer Funktionen in der Funktionsverwaltung

Einige der in diesem Thema beschriebenen Einstellungen müssen auf Ihrem System aktiviert sein, bevor sie Ihnen zur Verfügung stehen. Verwenden Sie die Seite [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), um einige oder alle der folgenden Funktionen nach Bedarf zu aktivieren.

### <a name="generate-license-plate"></a>Ladungsträger generieren

Um diese Funktion verfügbar zu machen, aktivieren Sie die folgenden Funktionen in [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (um):

1. Kennzeichen für die Meldung als fertig zum Einzelvorgangslistengerät hinzugefügt (Ab Supply Chain Management Version 10.0.21 ist diese Funktion standardmäßig aktiviert.)
1. Aktivieren Sie die automatische Generierung der Kennzeichennummer, wenn die Berichtserstellung im Einzelvorgangskartengerät abgeschlossen wurde

### <a name="print-label"></a>Etikett drucken

Um diese Funktion verfügbar zu machen, aktivieren Sie die folgenden Funktionen in [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (um):

1. Kennzeichen für die Meldung als fertig zum Einzelvorgangslistengerät hinzugefügt (Ab Supply Chain Management Version 10.0.21 ist diese Funktion standardmäßig aktiviert.)
1. Beschriftung vom Einzelvorgangs-Kartengerät aus drucken

### <a name="allow-locking-of-touch-screen"></a>Sperren des Touchscreens zulassen

Ab Supply Chain Management Version 10.0.21 ist diese Funktion standardmäßig aktiviert. Wenn Sie es nutzen möchten, überprüfen Sie, ob die folgende Funktion in der [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aktiviert ist:

- Funktion zum Sperren von Jobkartengerät und Jobkartenterminal, damit sie saniert werden können

## <a name="manage-your-device-configurations"></a>Ihre Gerätekonfigurationen verwalten

Um die Gerätekonfigurationen aufzusetzen, wechseln Sie zu **Produktionssteuerung > Einstellungen > Fertigungssteuerung > Einzelvorgangskarte für Geräte konfigurieren**. Die Seite **Konfigurieren Sie die Einzelvorgangskarte für Geräte** wird geöffnet, auf der eine Liste der vorhandenen Konfigurationen angezeigt wird. Von hier aus können Sie folgendermaßen vorgehen: 

- Wählen Sie eine in der linken Spalte aufgeführte Gerätekonfiguration aus, um sie anzuzeigen und zu bearbeiten.
- Wählen **Neu** im Aktivitätsbereich, um der Liste eine neue Gerätekonfiguration hinzuzufügen. Dann geben Sie im Feld **Konfiguration** einen Namen ein, um die neue Konfiguration identifizieren zu können. Der hier eingegebene Wert muss für alle Gerätekonfigurationen eindeutig sein und kann später nicht mehr bearbeitet werden.

In den folgenden Abschnitten finden Sie Details zu den einzelnen Einstellungen zum Konfigurieren von Einzelvorgangsgeräten.

## <a name="general-settings"></a>Allgemeine Einstellungen

Mit dem Inforegister **Allgemein** können Sie die verschiedenen Optionen konfigurieren, die für die ausgewählte Gerätekonfiguration verfügbar sind. Folgende Einstellungen sind verfügbar:

- **Menge beim Ausstempeln melden** – Stellen Sie dies auf **Ja** ein, um die Mitarbeiter aufzufordern, beim Ausstempeln Feedback zu laufenden Vorgängen zu melden. Wird **Nein** eingestellt, werden Arbeiter nicht dazu aufgefordert.
- **Mitarbeiter sperren** – Wenn diese Option auf **Nein** eingestellt ist, wird jeder Mitarbeiter sofort nach der Registrierung abgemeldet (z. B. ein neuer Auftrag), und das Gerät kehrt zur Anmeldeseite zurück. Wenn diese Option auf **Ja** eingestellt ist, bleibt jeder Mitarbeiter am Einzelvorgangsgerät angemeldet. Der Mitarbeiter kann sich jedoch weiterhin manuell abmelden, damit sich ein anderer Mitarbeiter anmelden kann, während das Einzelvorgangsgerät weiterhin unter demselben Systembenutzerkonto ausgeführt wird. Weitere Informationen zu diesen Arten von Konten finden Sie unter [Zugewiesene Benutzer](#assigned-users).
- **Barcode-Scanner** - Legen Sie dies auf **Ja** fest, um eine Option auf dem Jobkartengerät bereitzustellen, die es den Arbeitskräften erlaubt, den Beginn eines neuen Auftrags durch Scannen eines Barcodes zu registrieren.
- **Verwenden Sie den tatsächlichen Zeitpunkt der Registrierung** – Stellen Sie dies auf **Ja** ein, um die Zeit für jede neue Registrierung so festzulegen, dass sie genau der Zeit entspricht, zu der die Registrierung von einem Arbeitnehmer eingereicht wurde. Auf **Nein** einstellen, um stattdessen die Anmeldezeit zu verwenden. Normalerweise möchten Sie diese auf **Ja** einstellen, wenn Sie die Optionen **Mitarbeiter sperren** und/oder **Einzelner Arbeiter** aktiviert haben, bei denen Mitarbeiter häufig länger angemeldet bleiben.
- **Einzelne Arbeitskraft** – Setzen Sie diese Option auf **Ja**, wenn nur ein Mitarbeiter jedes Einzelvorgangsgerät verwendet, auf dem diese Konfiguration aktiv ist. Wenn diese Option ausgewählt ist, wird die Option **Mitarbeiter sperren** automatisch auf **Ja** festgelegt. Darüber hinaus entfällt mit dieser Option die Anforderung (und Fähigkeit), dass sich der Mitarbeiter mit einer Ausweis-ID (oder ähnlichem) anmelden muss. Stattdessen meldet sich der Mitarbeiter bei Supply Chain Management mit einem Systembenutzerkonto an, das mit einer *Zeit registrierten Arbeitskraft* (von der *Arbeitskräfte* Tabelle) verknüpft ist und gleichzeitig als diese Arbeitskraft am Einzelvorgangsgerät angemeldet wird.  Weitere Informationen zu diesen Arten von Konten finden Sie unter [Zugewiesene Benutzer](#assigned-users).
- **Ermöglichen Sie den Mitarbeitern, persönliche Filter festzulegen** – Setzen Sie diese Option auf **Ja** damit Mitarbeiter die Vorgänge filtern können, die ihnen auf dem Gerät angezeigt werden. Die Arbeitskraft kann Werte für eines der drei Filterkriterien ändern: **Produktionseinheit**, **Ressourcengruppe** und **Ressource**. Auf dem Gerät werden nur Vorgänge angezeigt, die für Ressourcen geplant sind, die den ausgewählten Filterkriterien entsprechen. Sie können auch Standardwerte für eines oder alle dieser Kriterien zuweisen. Diese gelten auch dann, wenn diese Option nicht ausgewählt ist.
- **Erlauben Sie das Sperren des Touchscreens** – Setzen Sie diese Option auf **Ja**, damit Mitarbeiter den Touchscreen des Einzelvorganggeräts sperren können, damit sie ihn bereinigen können. Wenn aktiviert, wird eine Schaltfläche **Sperrbildschirm zum Desinfizieren gepserrt** der Anmeldeseite des Geräts hinzugefügt. Wenn ein Mitarbeiter diese Schaltfläche auswählt, wird der Touchscreen vorübergehend gesperrt, um unbeabsichtigte Eingaben zu verhindern, und ein Countdown-Timer wird angezeigt. Die Arbeitskraft kann jetzt das Gerät und den Bildschirm sicher reinigen. Nach Ablauf des Countdowns wird der Touchscreen automatisch wieder entsperrt.
- **Dauer der Bildschirmsperre** – Wenn die Option **Sperren des Touchscreens zulassen** aktiviert ist, verwenden Sie diese Option, um anzugeben, wieviele Sekunden der Touchscreen für die Bereinigung gesperrt werden soll. Die Dauer muss eine Zahl zwischen 5 und 120 Sekunden sein.
- **Produktionseinheit** – Wählen Sie eine Produktionseinheit aus, die als Standardfilterkriterium für die Liste der Vorgänge angewendet werden soll, die jedem Mitarbeiter angezeigt werden. Das Gerät zeigt zunächst nur Vorgänge an, die für Ressourcen geplant sind, die unter der ausgewählten Produktionseinheit gruppiert sind. Wenn die Option **Ermöglichen Sie den Mitarbeitern, persönliche Filter festzulegen** aktiviert ist, können Arbeitskräfte diesen Wert bearbeiten. Andernfalls wird dieser Filter immer angewendet, wenn diese Gerätekonfiguration aktiv ist.
- **Ressourcengruppe** – Wählen Sie eine Ressourcengruppe aus, die als Standardfilterkriterium für die Liste der Vorgänge angewendet werden soll, die jedem Mitarbeiter angezeigt werden. Das Gerät zeigt zunächst nur Vorgänge an, die für Ressourcen geplant sind, die unter der ausgewählten Ressourcengruppe gruppiert sind. Wenn die Option **Ermöglichen Sie den Mitarbeitern, persönliche Filter festzulegen** aktiviert ist, können Arbeitskräfte diesen Wert bearbeiten. Andernfalls wird dieser Filter immer angewendet, wenn diese Gerätekonfiguration aktiv ist.
- **Ressource** – Wählen Sie eine Ressourcengruppe aus, die als Standardfilterkriterium für die Liste der Vorgänge angewendet werden soll, die jedem Mitarbeiter angezeigt werden. Das Gerät zeigt zunächst nur Vorgänge an, die für Ressourcen geplant sind, die unter der ausgewählten Ressourcengruppe gruppiert sind. Wenn die Option **Ermöglichen Sie den Mitarbeitern, persönliche Filter festzulegen** aktiviert ist, können Arbeitskräfte diesen Wert bearbeiten. Andernfalls wird dieser Filter immer angewendet, wenn diese Gerätekonfiguration aktiv ist.
- **Kennzeichen erstellen** – Setzen Sie diese Option auf **Ja**, um jedes Mal eine neue Kennzeichnung zu erstellen,wenn ein Mitarbeiter das Einzelvorgangsgerät verwendet, um den Vorgang als beendet zu melden. Das Kennzeichen wird aus einer Nummernfolge generiert, die auf der Seite **Lagerverwaltungsparameter** erstellt wird. Bei Einstellung auf **Nein** muss die Arbeitskraft eine bestehende Kennzeichnung definieren, wenn er er den Vorgang als beendet meldet.
- **Etikett drucken** – Setzen Sie diese Option auf **Ja**, um ein Kennzeichenetikett zu drucken, wenn eine Arbeitskraft das Einzelvorgangskartengerät verwendet, um den Vorgang als beendet zu melden. Die Konfiguration des Etiketts wird im Dokumentrouting eingerichtet, wie beschrieben in [Dokumenten-Routing-Layout für Kennzeichenetiketten](../warehousing/document-routing-layout-for-license-plates.md).

<a name="assigned-users"></a>

## <a name="assigned-users"></a>Zugewiesene Benutzer

Verwenden Sie das Inforegister **Zugewiesene Benutzer**, um einen oder mehrere Systembenutzer mit der aktuellen Gerätekonfiguration zu verknüpfen. Jedem Systembenutzer kann nur eine Einzelvorgangskonfiguration zugewiesen werden.

Beim Einrichten eines Geräts meldet sich ein IT-Mitarbeiter normalerweise mit einem Systembenutzerkonto beim Supply Chain Management an. Danach gilt die diesem Systembenutzer zugeordnete Einzelvorgangsgerätekonfiguration so lange, wie dieser Systembenutzer angemeldet bleibt. Diese Systembenutzerkonten sind normalerweise so beschränkt, dass nur der Zugriff auf die Einzelvorgangs-Geräteseite und sosnt auf keinen anderen Teil des Supply Chain Managements möglich ist.

Nachdem der Systembenutzer angemeldet und die Konfiguration des Einzelvorgangsgeräts geladen wurde, können sich die Mitarbeiter mit ihrem Einzelvorgangsgerätkonto *Zeit registrierte Arbeitskraft* (z. B. durch Scannen eines Barcodes auf dem Ausweis) anmelden, damit sie neue Vorgänge starten und andere Arten von Registrierungen vornehmen können. Verschiedene Mitarbeiter können sich tagsüber an- und abmelden, während auf diesem Computer dieselbe Gerätekonfiguration wirksam bleibt, da der Systembenutzer für diesen Tag bei Supply Chain Management angemeldet bleibt.

Wie bereits erwähnt, wenn Sie eine Gerätekonfiguration mit der Option **Einzelne Arbeitskraft** verwenden, melden sich Arbeitskräfte in der Regel selbst bei Supply Chain Management mithilfe einem Systembenutzer an, der mit dem Konto *Zeit registrierten Arbeitskraft* verknüpft ist, sodass sie die Gerätekonfiguration laden und sich gleichzeitig als Arbeitskraft auf dem Einzelvorgangskartengerät anmelden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Vom Einzelvorgangskartengerät als erledigt melden](report-finished-job-device.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]