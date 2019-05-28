---
title: Überblick über die Funktionsverwaltung
description: In diesem Thema werden die Funktionsverwaltungsfunktion und deren Verwendung beschrieben.
author: mikefalkner
manager: AnnBe
ms.date: 04/18/2019
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
ms.openlocfilehash: e75e42926db22d4fccda86c755b12d9d121a9c0e
ms.sourcegitcommit: be447fc81bc874982bc0185fcb4d87d99bd742c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538689"
---
# <a name="feature-management-overview"></a>Überblick über die Funktionsverwaltung

[!include[banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

Funktionen werden in jeder Version von Microsoft Dynamics 365 for Finance and Operations hinzugefügt und aktualisiert. Die Funktionsverwaltungserfahrung bietet einen Arbeitsbereich, in dem Sie eine Liste mit Funktionen anzeigen können, die in jede Version geliefert wurden. Standardmäßig sind neue Funktionen ausgeschaltet. Sie können den Arbeitsbereich verwenden, um sie zu aktivieren und die Dokumentation für sie anzuzeigen.

## <a name="the-feature-management-workspace"></a>Der Arbeitsbereich für die Funktionsverwaltung

Sie können den Arbeitsbereich **Funktionsverwaltung** öffnen, indem Sie die entsprechende Kachel im Dashboard auswählen. Sie sehen eine Seite, die eine Liste mit Funktionen für alle Versionen anzeigt, die von der Funktionsverwaltungserfahrung unterstützt werden. Im Laufe der Zeit wird Microsoft die Funktionsverwaltungserfahrung verbessern, so dass sie zusätzliche Funktionen enthält, um Ihnen dabei zu helfen, Funktionen zu verwalten.

Die Funktionsliste für Positionsdetails enthält die folgenden Informationen:

- **Funktionsname** – Eine Beschreibung der Funktion, die hinzugefügt wurde.
- **Aktivierter Status** – Ein Symbol gibt an, ob eine Funktion aktiviert wurde (Häkchen), nicht aktiviert ist (leer), zur Aktivierung geplant wurde (Uhr) oder obligatorisch aktiviert ist (Schloss). Die Einstellung, die hier angezeigt wird, wird für alle juristischen Personen verwendet. Beachten Sie, dass auch bei Aktivierung einer Funktion diese nach wie vor über die Sicherheit gesteuert wird. Daher ist die Funktion nur für Benutzer verfügbar, die auf der Grundlage ihrer Sicherheitsrolle Zugriff darauf haben. Sie ist ebenfalls nur für juristische Personen verfügbar, auf die der Benutzer Zugriff hat.
- **Aktivierungsdatum** – Das Datum, an dem die Funktion aktiviert wurde oder aktiviert wird, wenn das Datum in der Zukunft liegt.
- **Funktion hinzugefügt** – Das Datum, an dem die Funktion für Ihre Umgebung hinzugefügt wurde. Dieses Datum wird automatisch eingegeben, wenn Sie Ihre Umgebung beim monatlichen Versionszyklus aktualisieren.
- **Modul** – Das Modul, das von der neuen Funktion betroffen ist.

Wenn Sie eine Funktion auswählen, werden zusätzliche Informationen im Detailbereich rechts neben der Funktionsliste angezeigt. Oben im Bereich finden Sie den Funktionsnamen, das Datum, an dem die Funktion hinzugefügt wurde, das Modul, das von der Funktion betroffen ist, und einen **Mehr erfahren**-Link. Wählen Sie diesen Link aus, um die Dokumentation für die Funktion anzuzeigen. Wenn keine Dokumentation verfügbar ist, gelangen Sie zu einer temporären Seite. Der Detailbereich beinhaltet auch ein **Kommentare**-Feld, in dem Sie Ihre eigenen Kommentare zur Funktion hinzufügen können.

Der Arbeitsbereich **Funktionsverwaltung** enthält auch einige Registerkarten mit einer Liste der Funktionen darin. 
- **Neu** - Zeigt alle Funktionen, die seit der letzten monatlichen Aktualisierung hinzugefügt wurden. Wenn Sie monatliche Aktualisierungen übersprungen haben, dann werden alle neuen Funktionen seit Ihrer letzten Ausführung angezeigt. Die neuesten Funktionen werden ganz oben in der Liste angezeigt. Die Gesamtanzahl der neuen Funktionen wird in einer Kachel am oberen Seitenrand angezeigt.
- **Nicht aktiviert** - Zeigt alle Funktionen an, die noch nicht aktiviert wurden. Die neuesten Funktionen werden ganz oben in der Liste angezeigt. Die Gesamtanzahl der neuen Funktionen wird in einer Kachel am oberen Seitenrand angezeigt.
- **Geplant** - Zeigt alle Funktionen an, die für zukünftige Aktualisierung geplant sind. Die Funktionen mit dem frühesten geplanten Datum werden oben in der Liste angezeigt. Die Gesamtanzahl der neuen Funktionen wird in einer Kachel am oberen Seitenrand angezeigt.
- **Alle** - Zeigt alle Funktionen an. Die neuesten Funktionen werden ganz oben in der Liste angezeigt.


## <a name="enable-a-feature"></a>Aktivieren einer Funktion

Wenn eine Funktion nicht aktiviert wurde, wird eine **Aktivieren**-Schaltfläche im Detailbereich angezeigt. Sie können diese Schaltfläche verwenden, um die Funktion zu aktivieren.

1. Wählen Sie die Funktion aus, die Sie aktivieren möchten, und wählen Sie dann im Detailbereich **Aktivieren** aus.
2. Ein Schieberegler wird angezeigt, mit dem Sie das Datum angeben können, zu dem die Funktion ausgeführt werden soll. Standardmäßig wird dafür das aktuelle Datum festgelegt.
3. Wählen Sie **Aktivieren** aus, um die Funktion zu aktivieren.

Einige Funktionen können nicht deaktiviert werden, nachdem Sie aktiviert wurden. Wenn die Funktion, die Sie zu aktivieren versuchen, nicht deaktiviert werden kann, erhalten Sie eine Warnung. An diesem Punkt können Sie **Abbrechen** auswählen, um den Vorgang abzubrechen und die Funktion deaktiviert zu lassen. Wenn Sie allerdings **Aktivieren** auswählen und die Funktion aktivieren, können Sie sie später nicht mehr deaktivieren.

Nach der Aktivierung der Funktion wird eine Meldung unterhalb des Links **Mehr erfahren** im Detailbereich angezeigt. Diese Nachricht gibt entweder an, dass die Funktion aktiviert ist oder gibt an, wann die Funktion zukünftig aktiviert wird. Wenn Sie ein in der Zukunft liegendes Datum werden, wird die Funktion in der Liste **Geplant** angezeigt. Diese Nachricht wird jedes Mal angezeigt, wenn Sie die Funktion in der Funktionsliste auswählen. Funktionen, die in der Zukunft geplant sind, werden durch eine Stapelverarbeitung um Mitternacht in der vom Systemdatum angegebenen Zeitzone aktiviert. 

## <a name="reschedule-a-feature"></a>Neuplanen einer Funktion

Wenn eine Funktion in der Zukunft aktiviert wurde, wird eine **Neuplanen**-Schaltfläche im Detailbereich angezeigt. Sie können diese Schaltfläche verwenden, um das **Aktivierungsdatum** auf ein anderes Datum zu ändern.

1. Wählen Sie eine geplante Funktion aus, die Sie neu planen möchten, und wählen Sie dann im Detailbereich **Neu planen** aus.
2. Ein Schieberegler wird angezeigt, mit dem Sie das Datum angeben können, zu dem die Funktion ausgeführt werden soll. 
3. Wählen Sie **Aktivieren** aus, um die Funktion neu zu planen oder **Deaktivieren**, um die Planung abzubrechen.

## <a name="disable-a-feature"></a>Deaktivieren einer Funktion

Wenn eine Funktion bereits aktiviert wurde, wird eine **Deaktivieren**-Schaltfläche im Detailbereich angezeigt. Sie können diese Schaltfläche verwenden, um die Funktion zu deaktivieren. Die Schaltfläche **Deaktivieren** ist nicht verfügbar, wenn die Funktion nicht deaktiviert werden kann, nachdem sie aktiviert wurde.

- Wählen Sie die Funktion aus, die Sie ausschalten möchten, und wählen Sie dann im Detailbereich **Deaktivieren** aus.

- Die Funktion ist deaktiviert und das Datum wird gelöscht.

Nach der Deaktivierung der Funktion wird eine Meldung unterhalb des Links **Mehr erfahren** im Detailbereich angezeigt. Diese Meldung gibt an, dass die Funktion noch nicht aktiviert wurde und sie wird in der Liste **Nicht aktiviert** angezeigt. Die Meldung wird jedes Mal angezeigt, wenn Sie die Funktion in der Funktionsliste auswählen.

## <a name="features-that-must-be-enabled"></a>Funktionen, die aktiviert werden müssen

Eine wichtige Funktion wird möglicherweise geliefert, die automatisch aktiviert werden muss, wenn Sie eine Aktualisierung ausführen. Sie wird automatisch in **Aktivierungsdatum** aktiviert. Eine Meldung wird unter dem Link **Mehr erfahren** im Detailbereich angezeigt. Diese Meldung gibt an, dass die Funktion aktiviert wurde oder automatisch am **Aktivierungsdatum** aktiviert wird. Sie wird jedes Mal angezeigt, wenn Sie die Funktion in der Funktionsliste auswählen.

## <a name="assigning-roles"></a>Zuweisen von Rollen

Der Arbeitsbereich **Funktionsverwaltung** kann von Systemadministratoren und von Benutzern geöffnet werden, die den Funktionsmanager- oder Funktions-Viewer-Rollen zugewiesen werden, die zur Unterstützung der Funktionsverwaltungserfahrung erstellt wurden. Benutzer in der Funktionsmanagerrolle können jede Funktion aktivieren oder deaktivieren. Sie können auch den Kommentarabschnitt für die Funktion aktualisieren. Benutzer in der Funktions-Viewer-Rolle können nur den Arbeitsbereich **Funktionsverwaltung** anzeigen. Sie können keine Funktionen aktivieren oder deaktivieren.

Die Funktionsmanagerrolle und die Funktions-Viewer-Rolle setzen die vorhandene Sicherheit eines Benutzers nicht außer Kraft. Die Rollen steuern nur den Zugriff auf aktivierende Funktionen. Sie stellt keinen Zugriff auf die Funktionen selbst zur Verfügung.

## <a name="using-feature-management-to-enable-isv-features-or-custom-features"></a>Verwenden der Funktionsverwaltung zum Aktivieren von ISV-Funktionen oder benutzerdefinierten Funktionen

Der Funktionsverwaltungsprozess ist aktuell für ISV-Funktionen oder benutzerdefinierte Funktionen nicht verfügbar. Es fügen zusätzliche Funktion hinzu, um die Funktionsverwaltung zu verbessern, und wenn diese Erweiterungen abgeschlossen sind, wird die Funktionsverwaltung auf alle Funktionen erweitert und stellt bestimmte Anweisungen zur Aktualisierung Ihrer Funktionen zur Verwendung bereit.

## <a name="feature-management-and-flighting"></a>Funktionsverwaltung und Flight

Mit der Funktionsverwaltung können Sie Funktionen steuern, die in jeder Version geliefert werden. Flight ermöglicht es den Microsoft Teams Funktionen für eine begrenzte Anzahl von Kunden zu veröffentlichen, sodass die Funktionen getestet und überprüft werden können, ohne sich auf alle Kunden auszuwirken. Die Funktionsverwaltung kontrolliert nicht das Flight der Funktionen.
