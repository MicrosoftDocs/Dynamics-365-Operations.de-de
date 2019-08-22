---
title: Überblick über die Funktionsverwaltung
description: In diesem Thema werden die Funktionsverwaltungsfunktion und deren Verwendung beschrieben.
author: mikefalkner
manager: AnnBe
ms.date: 07/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: IT Pro, Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: 21eaf2fdcadf8fe9f91438a97a88cc3bddab8286
ms.sourcegitcommit: d0fa8d0140fa81029527edb317623c1a7737c593
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2019
ms.locfileid: "1862937"
---
# <a name="feature-management-overview"></a>Überblick über die Funktionsverwaltung

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

Funktionen werden in jeder Version von Microsoft Dynamics 365 for Finance and Operations hinzugefügt und aktualisiert. Die Funktionsverwaltungserfahrung bietet einen Arbeitsbereich, in dem Sie eine Liste mit Funktionen anzeigen können, die in jede Version geliefert wurden. Standardmäßig sind neue Funktionen ausgeschaltet. Sie können den Arbeitsbereich verwenden, um sie zu aktivieren und die Dokumentation für sie anzuzeigen.

## <a name="the-feature-management-workspace"></a>Der Arbeitsbereich für die Funktionsverwaltung

Sie können den Arbeitsbereich **Funktionsverwaltung** öffnen, indem Sie die entsprechende Kachel im Dashboard auswählen. Sie sehen eine Seite, die eine Liste mit Funktionen für alle Versionen anzeigt, die von der Funktionsverwaltungserfahrung unterstützt werden. Im Laufe der Zeit wird Microsoft die Funktionsverwaltungserfahrung verbessern, so dass sie zusätzliche Funktionen enthält, um Ihnen dabei zu helfen, Funktionen zu verwalten.

Die Funktionsliste für Positionsdetails enthält die folgenden Informationen:

- **Funktionsname** – Eine Beschreibung der Funktion, die hinzugefügt wurde.
- **Aktivierter Status** – Ein Symbol gibt an, ob eine Funktion aktiviert wurde (Häkchen), nicht aktiviert ist (leer), zur Aktivierung geplant ist (Uhr), obligatorisch aktiviert ist (Schloss), Aufmerksamkeit erfordert, bevor Sie sie aktivieren (Warnung), oder nicht aktiviert werden kann (X). Die Einstellung, die angezeigt wird, wird für alle juristischen Personen verwendet. Beachten Sie, dass auch bei Aktivierung einer Funktion diese nach wie vor über die Sicherheit gesteuert wird. Daher ist die Funktion nur für Benutzer verfügbar, die auf der Grundlage ihrer Sicherheitsrolle Zugriff darauf haben. Sie ist ebenfalls nur in juristischen Personen verfügbar, auf die der Benutzer Zugriff hat.
- **Aktivieren des Datums** – Das Datum, an dem die Funktion aktiviert wurde für das die Aktivierung geplant ist.
- **Funktion hinzugefügt** – Das Datum, an dem die Funktion für Ihre Umgebung hinzugefügt wurde. Dieses Datum wird automatisch eingegeben, wenn Sie Ihre Umgebung beim monatlichen Versionszyklus aktualisieren.
- **Modul** – Das Modul, das von der neuen Funktion betroffen ist.

Wenn Sie eine Funktion auswählen, werden zusätzliche Informationen im Detailbereich rechts neben der Funktionsliste angezeigt. Oben im Bereich finden Sie den Funktionsnamen, das Datum, an dem die Funktion hinzugefügt wurde, das Modul, das von der Funktion betroffen ist, und einen **Mehr erfahren**-Link. Wählen Sie diesen Link aus, um die Dokumentation für die Funktion anzuzeigen. Wenn keine Dokumentation verfügbar ist, gelangen Sie zu einer temporären Seite. Der Detailbereich beinhaltet auch ein **Kommentare**-Feld, in dem Sie Ihre eigenen Kommentare zur Funktion hinzufügen können.

Der Arbeitsbereich **Funktionsverwaltung** enthält auch einige Registerkarten, die jede die Funktionen auflistet.

- **Neu** - Diese Registerkarte zeigt alle Funktionen, die seit der letzten monatlichen Aktualisierung hinzugefügt wurden. Wenn Sie einen Monatsaktualisierungen übersprungen haben, werden auf der Registerkarte alle neuen Funktionen aufgezeigt, die seit Ihrer letzten Aktualisierung hinzugefügt wurden. Die neuesten Funktionen werden ganz oben in der Liste angezeigt. Die Gesamtanzahl der neuen Funktionen wird auf einer Kachel am oberen Seitenrand angezeigt.
- **Nicht aktiviert** – Auf dieser Registerkarte werden alle Funktionen angezeigt, die noch nicht aktiviert wurden. Die neuesten Funktionen werden ganz oben in der Liste angezeigt. Die Gesamtanzahl der neuen Funktionen, die noch nicht aktiviert wurden, werden auch auf einer Kachel am oberen Seitenrand angezeigt.
- **Geplant** - Diese Registerkarte zeigt alle Funktionen an, die zur Aktivierung geplant sind. Die Funktionen mit dem frühesten geplanten Datum werden oben in der Liste angezeigt. Die Gesamtanzahl der geplanten neuen Funktionen wird auf einer Kachel am oberen Seitenrand angezeigt.
- **Alle** – Auf dieser Registerkarte werden alle Funktionen angezeigt. Die neuesten Funktionen werden ganz oben in der Liste angezeigt.

## <a name="turn-on-a-feature"></a>Eine Funktion aktivieren

Wenn eine Funktion nicht aktiviert wurde, wird eine **Jetzt Aktivieren**-Schaltfläche im Detailbereich angezeigt. Sie können diese Schaltfläche verwenden, um die Funktion zu aktivieren.

- Wählen Sie die Funktion aus, die Sie aktivieren möchten, und wählen Sie dann im Detailbereich **Jetzt Aktivieren** aus. Die Funktion ist aktiviert.

Einige Funktionen können nicht deaktiviert werden, nachdem Sie diese aktiviert haben. Wenn die Funktion, die Sie zu aktivieren versuchen, nicht deaktiviert werden kann, erhalten Sie eine Warnung. An diesem Punkt können Sie **Abbrechen** auswählen, um den Vorgang abzubrechen und die Funktion deaktiviert lassen. Wenn Sie allerdings **Aktivieren** auswählen und die Funktion aktivieren, können Sie sie später nicht mehr deaktivieren.

Bei einigen Funktionen wird eine Meldung angezeigt, die weitere Informationen bereitstellt, bevor Sie die Funktion aktivieren. Diese Funktionen sind mit einem gelben Warnsymbol gekennzeichnet. Sie sollten die zusätzlichen Information sorgfältig lesen, um besser zu verstehen, was geschieht, wenn die Funktion aktiviert ist. Allerdings können Sie immer noch **Aktivieren** auswählen, um die Funktion zu aktivieren.

Bei einigen Funktionen wird eine Meldung angezeigt, dass die Funktion erst aktiviert werden kann, wenn eine Aktion unternommen wird. Diese Funktionen sind mit einem roten X-Symbol gekennzeichnet. Sie müssen erst die in der Beschreibung erläuterten Aktionen ausführen, bevor die Funktion aktiviert werden kann. Wenn Sie zum Beispiel eine Funktion erst verwenden können, wenn ein Konfigurationsschlüssel deaktiviert wurde, müssen Sie zuerst den Konfigurationsschlüssel deaktivieren und dann zur Funktionsverwaltung zurückkehren, um die Funktion zu aktivieren.

Nach der Aktivierung einer Funktion wird eine Meldung unterhalb des Links **Mehr erfahren** im Detailbereich angezeigt. Diese Nachricht gibt entweder an, dass die Funktion aktiviert ist oder gibt das Datum an, wann die Funktion zur Aktivierung geplant ist. Sie wird jedes Mal angezeigt, wenn Sie die Funktion in der Funktionsliste auswählen.

Funktionen, die zur Aktivierung geplant sind, werden auf der Registerkarte **Eingeplant** angezeigt. Ein Stapelverarbeitungsvorgang schaltet sie am angegebenen Datum um Mitternacht basierend auf derZeitzone, die auf dem Systemdatum dargestellt wird, ein.

## <a name="reschedule-a-feature"></a>Neuplanen einer Funktion

Wenn eine Funktion zur Aktivierung in der Zukunft geplant ist, wird eine Schaltfläche **Zeitplan** im Detailbereich angezeigt. Sie können diese Schaltfläche verwenden, um den Wert **Aktivierungsdatum** auf ein anderes Datum zu ändern.

1. Wählen Sie die geplante Funktion aus, die Sie neu planen möchten, und wählen Sie dann im Detailbereich **Zeitplan** aus.
2. Im Dialogfeld, das im Feld **Aktivierungsdatum** angezeigt wird, geben Sie das neue Datum ein, an dem die Funktion aktiviert werden soll.
3. Wählen Sie **Aktivieren** aus, um die Funktion neu zu planen oder **Deaktivieren**, um die Planung abzubrechen.

## <a name="turn-off-a-feature"></a>Eine Funktion deaktivieren

Wenn eine Funktion bereits aktiviert ist, wird eine **Deaktivieren**-Schaltfläche im Detailbereich angezeigt. Sie können diese Schaltfläche verwenden, um die Funktion zu deaktivieren. Die Schaltfläche **Deaktivieren** ist nicht verfügbar, wenn die Funktion nicht mehr deaktiviert werden kann, nachdem sie aktiviert wurde.

- Wählen Sie die Funktion aus, die Sie deaktivieren möchten, und wählen Sie dann im Detailbereich **Deaktivieren** aus. Die Funktion wird deaktiviert, und das Feld **Aktivierungsdatum** wird deaktiviert.

Nach der Deaktivierung einer Funktion wird eine Meldung unterhalb des Links **Mehr erfahren** im Detailbereich angezeigt. Diese Nachricht zeigt an, dass die Funktion noch nicht aktiviert wurde. Sie wird jedes Mal angezeigt, wenn Sie die Funktion in der Funktionsliste auswählen. Funktionenen, die noch nicht aktiviert wurden, weren auf der Registerkarte als **Nicht aktiviert** angezeigt.

## <a name="features-that-must-be-turned-on"></a>Funktionen, die aktiviert werden müssen

Manchmal wird eine wichtige Funktion bereitgestellt, die automatisch aktiviert werden muss, wenn Sie eine Aktualisierung ausführen. Diese Funktionalität wird automatisch am Datum aktiviert, das im Feld **Aktivierungsdatum** angegeben ist. Für diese Funktionen wird eine Meldung unterhalb des Links **Mehr erfahren** im Detailbereich angezeigt. Diese Nachricht gibt entweder an, dass die Funktion aktiviert ist oder gibt das Datum an, wann die Funktion aktiviert wird. Sie wird jedes Mal angezeigt, wenn Sie die Funktion in der Funktionsliste auswählen.

## <a name="enable-all-features"></a>Alle Funktionen aktivieren

Standardmäßig sind alle Funktionen, die Ihrer Umgebung hinzugefügt werden deaktiviert. Sie können alle Funktionen aktivieren, indem Sie die Schaltfläche **Alle aktivieren** auswählen. 

Wenn Sie **Alle aktivieren** auswählen, wird eine Option angezeigt, bei der Sie die folgenden Informationen angeben müssen:
- Eine Liste aller Funktionen, die eine Bestätigung erfordern, bevor sie aktiviert werden können. Wenn Sie die Funktionen in der Liste aktivieren möchten, wählen Sie **Ja** für die Schaltfläche **Funktionen aktivieren, die eine Bestätigung erfordern** aus.
- Eine Liste aller Funktionen wird angezeigt, die nicht aktiviert werden können. Diese Funktionen werden nicht aktiviert.

Alle Funktionen, die aktiviert werden können, werden aktiviert. Wenn bereits geplant ist, dass eine Funktion in der Zukunft aktiviert wird, ändert sich der Zeitplan nicht. 

## <a name="turn-on-all-features-automatically"></a>Alle Funktionen automatisch aktivieren

Standardmäßig sind alle Funktionen, die Ihrer Umgebung hinzugefügt werden deaktiviert, es sei denn, es handelt sich um erforderliche Funktionen. Wenn Sie jedoch automatisch alle neuen Funktionen aktivieren möchten, können Sie die Dropdownliste unter dem Arbeitsbereichtitel verwenden, um zu ändern, was geschieht, wenn neue Fähigkeiten hinzugefügt werden.

- Wählen Sie **Alle neuen Funktionen sind standardmäßig aktiviert**, um automatisch alle neuen Funktionen zu aktivieren, die Ihrer Umgebung hinzugefügt werden.
- Wählen Sie **Alle neuen Funktionen sind standardmäßig deaktiviert**, um automatisch alle neuen Funktionen zu deaktivieren, die Ihrer Umgebung hinzugefügt werden.

Wenn Sie alle Funktionen automatisch aktivieren, werden dadurch alle Features aktiviert, die aktiviert würden, wenn Sie auf die Schaltfläche **Alle aktivieren** klicken. Die Funktionen, die eine Bestätigung erfordern, oder die Features, die erst nach einer Aktion aktiviert werden können, werden nicht aktiviert.

## <a name="check-for-updates"></a>Nach Updates suchen

Funktionen werden nach jeder Aktualisierung zu Ihrer Umgebung hinzugefügt. Sie können jedoch auch manuell auf Updates prüfen, indem Sie auf die Schaltfläche **Nach Updates suchen** klicken. Alle Funktionen, die dem System nach dem Update hinzugefügt wurden, werden der Liste mit Funktionen hinzugefügt. Wenn beispielsweise eine Flight-Funktion nach einer Veröffentlichung aktiviert wird, können Sie nach Updates suchen, und die Funktion wird dann Ihrer Liste hinzugefügt.

## <a name="assigning-roles"></a>Zuweisen von Rollen

Der Arbeitsbereich **Funktionsverwaltung** kann von Systemadministratoren und auch von Benutzern geöffnet werden, die den Funktionsmanager- oder Funktions-Viewer-Rollen zugewiesen werden, die zur Unterstützung der Funktionsverwaltungserfahrung erstellt wurden. Diese beiden Rollen wurden erstellt, um die Funktionsverwaltungserfahrung zu unterstützen. Benutzer in der Funktionsmanagerrolle können jede Funktion aktivieren oder deaktivieren. Sie können auch das Feld **Kommentar** für die Funktion aktualisieren. Benutzer in der Funktions-Viewer-Rolle können nur den Arbeitsbereich **Funktionsverwaltung** anzeigen. Sie können keine Funktionen aktivieren oder deaktivieren.

Die Funktionsmanagerrolle und die Funktions-Viewer-Rolle setzen die vorhandene Sicherheit eines Benutzers nicht außer Kraft. Sie steuern lediglich, ob Benutzer derzeit Funktionen anzeigen und deaktivieren können. Sie stellen keinen Zugriff auf die Funktionen selbst zur Verfügung.

## <a name="features-that-use-configuration-keys"></a>Funktionen, die Konfigurationsschlüssel verwenden

Wenn eine Funktion einen Konfigurationsschlüssel verwendet, aber der Konfigurationsschlüssel nicht aktiviert ist, wird im Arbeitsbereich **Funktionsverwaltung** die Funktion nicht in der Liste der verfügbaren Funktionen angezeigt. Nachdem Sie die Konfigurationsschlüssel aktiviert haben, müssen Sie die Funktionsliste aktualiseren, indem Sie das Menüelement **Auf Aktualisierung prüfen** verwenden. Die Funktion wird dann in der Funktionsliste angezeigt.

Wenn Sie den Konfigurationsschlüssel deaktivieren, wird die Funktion nicht aus der Funktionsliste entfernt.

## <a name="data-entities"></a>Datenentitäten

Eine Datenentität mit der Bezeichnung **Funktionsverwaltung** ermöglicht es,  die Funktionsverwaltungseinstellungen einer Umgebung zu exportieren und in einer anderen Umgebung dann zu importieren. Diese Entität aktualisiert nur vorhandene Funktionen. Die zugehörige Geschäftslogik in der Entität stellt außerdem sicher, dass dieselben Regeln, die im Arbeitsbereich **Funktionsverwaltung** verwendet werden, übernommen werden, wenn der Import ausgeführt wird. So können Sie beispielsweise eine erforderliche Funktionseinstellung nicht überschreiben, indem Sie das Datum für den Import entfernen.

Das folgende Beispiel beschreibt, was geschieht, wenn Sie die Entität **Funktionsverwaltung** verwenden, um Daten zu importieren.

- Wenn Sie den Wert des Felds **Aktiviert** auf **Ja** ändern, wird die Funktion aktiviert, und das Feld **Datum aktivieren**  wird auf das aktuelle Datum festgelegt.
- Wenn Sie den Wert des Felds **Aktiviert** auf **Nein** ändern oder es leer lassen, wird die Funktion **Datum aktivieren** deaktiviert, und das Feld **Datum aktivieren** wird gelöscht. Sie können eine erforderliche Funktion oder eine Funktion, die nicht deaktiviert werden kann nicht deaktivieren, nachdem sie aktiviert wurde.
- Wird der Wert des Felds **Datum aktivieren** zu einem künftigen Zeitpunkt geändert, wird die Funktion für dieses Datum geplant.
- Wenn Sie den Wert des Felds **Aktiviert** auf **Ja** ändern und den Wert des Felds **Datum aktivieren**  auf ein künftiges Datum ändern, wird die Funktion für dieses Datum geplant. 
- Wenn Sie den Wert des Felds **Aktiviert** auf **Nein** ändern und den Wert des Felds **Datum aktivieren**  auf ein künftiges Datum ändern, wird die Funktion für dieses Datum geplant.
- Wenn eine Funktion aktiviert ist und Sie das Feld **Datum aktivieren**hinzufügen, das auf ein zukünftiges Datum festgelegt ist, bleibt die Funktion aktiviert. Um die Funktiont neu zu planen, müssen Sie das Feld **Aktiviert** auf **Nein** ändern.

## <a name="feature-management-and-flighting"></a>Funktionsverwaltung und Flight

Mit der Funktionsverwaltung können Sie die Funktionen steuern, die in jeder Version geliefert werden. Flight ermöglicht es den Microsoft Teams Funktionen für eine begrenzte Anzahl von Kunden zu veröffentlichen, sodass diese Funktionen getestet und überprüft werden können, ohne sich auf alle Kunden auszuwirken. Die Funktionsverwaltung kontrolliert nicht das Flight der Funktionen.

## <a name="using-feature-management-to-turn-on-isv-features-or-custom-features"></a>Verwenden der Funktionsverwaltung zum Aktivieren von ISV-Funktionen oder benutzerdefinierten Funktionen

Funktionsverwaltung ist derzeit für Funktionen von unabhängigen Softwareherstellern (ISVs) und benutzerdefinierten Funktionen nicht verfügbar. Microsoft fügt aber mehr Funktionen hinzu, um die Funktionsverwaltung zu verbessern. Nachdem diese Erweiterungen abgeschlossen sind, ist die Microsoft Funktionsverwaltung für alle Funktionen verfügbar und stellt Anweisungen zum Aktualisieren Ihrer Funktionen zur Verwendung bereit.
