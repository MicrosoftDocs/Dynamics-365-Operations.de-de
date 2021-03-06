---
title: Was ist neu oder geändert in der Warehouse Management Mobile-App
description: Dieses Thema listet die neuen und geänderten Funktionen für jede freigegebene Version der Warehouse Management Mobile-App für Microsoft Dynamics 365 Supply Chain Management auf.
author: ivanv-microsoft
ms.date: 06/07/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-07
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 61124728942c0b8162de9f687ae752773c47d07e
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261778"
---
# <a name="whats-new-or-changed-in-the-warehouse-management-mobile-app"></a>Was ist neu oder geändert in der Warehouse Management Mobile-App

[!include [banner](../includes/banner.md)]

Dieses Thema listet neue Funktionen, Korrekturen, Verbesserungen und bekannte Probleme für jede freigegebene Version der Warehouse Management Mobile-App für Microsoft Dynamics 365 Supply Chain Management auf.

## <a name="version-2060"></a>Version 2.0.6.0

### <a name="new-features-fixes-and-improvements-in-version-2060"></a>Neue Funktionen, Fehlerbehebungen und Verbesserungen in Version 2.0.6.0

Diese Version führt die folgenden neuen Funktionen, Korrekturen und Verbesserungen ein:

- Im Demomodus werden jetzt alle Labels in der Gerätesprache angezeigt.
- Die Wahrscheinlichkeit, dass Sie die folgende Fehlermeldung erhalten, ist geringer: „Es konnte keine passende Ansicht für die angegebene Größe gefunden werden.“
- Die Mindesthöhe für Arbeitskarten wurde erhöht (für Fälle, in denen drei oder weniger Felder konfiguriert sind, die in der Arbeitsliste erscheinen sollen).
- Die Ränder (Ausblendung) am unteren Rand von Detailkarten wurden verbessert.
- Ungültige Symbole in XML-Dateien, die mit dem Server ausgetauscht werden, werden nun korrekt behandelt. (Zum Beispiel werden nicht druckbare Zeichen jetzt korrekt behandelt und führen nicht mehr dazu, dass die App nicht mehr reagiert).
- HTTP-Fehler (z. B. „Fehler 503“) beim Senden einer Serveranforderung werden jetzt korrekt behandelt.
- Während ein Fehler angezeigt wird, wird die Optionsliste für Steuerelemente in Kombinationsfeldern nicht mehr automatisch angezeigt.
- Die App reagiert nicht mehr aufgrund der Anzeigeausrichtung, die in den Benutzereinstellungen festgelegt ist.
- Produktbilder werden jetzt in Self-Service-Umgebungen angezeigt. (Diese Änderung gilt nur für Versionen mit niedriger Auflösung. Der Dateiverwaltungsdienst unterstützt keine Bilder in voller Größe in Self-Service-Umgebungen.)
- Ein Problem, das das Kommissionieren von Null-Mengen betraf, wurde behoben.
- Die App reagiert nicht mehr, wenn eine Detailkarte mehrere identische Felder anzeigt.

### <a name="known-issues-in-version-2060"></a>Bekannte Probleme in Version 2.0.6.0

Die folgenden bekannten Probleme sind in dieser Version vorhanden:

- Die App (insbesondere die Arbeitsliste) wird mit der Zeit langsamer.
- **Windows-Version:** Wenn eine USB-Pistole zum Scannen unter Windows verwendet wird, werden durch inkonsistente Ergebnisse gescannte Symbole vertauscht.

## <a name="version-2050"></a>Version 2.0.5.0

Diese Version führt die folgenden neuen Funktionen, Korrekturen und Verbesserungen ein:

- Das Client-Geheimnis wird beim Einrichten der Verbindungseinstellungen nicht mehr versteckt.
- Sie können jetzt lange auf einen beliebigen Text drücken, um ihn vollständig zu sehen.
- Die Fehlermeldung beim Fehlen von Speicherberechtigungen wurde verbessert.
- Es wurden neue Steuerelemente für einige Flows hinzugefügt.
- Die Schaltfläche „Senden“ wird nicht mehr fälschlicherweise aufgrund der Fenstergröße verfügbar.
- Schieberegler können jetzt auf kleineren Bildschirmen weiterlaufen, wenn größere Schaltflächen verwendet werden.
- Das Overlay mit vier Schaltflächen wird nicht mehr abgeschnitten.
- Die Tastatur unterstützt jetzt die DELETE-Schaltfläche.
- Ein Problem mit der Helligkeit, das beim Drücken der Tastatur auftreten konnte, wurde behoben.
- Verschiedene Probleme mit Demo-Daten wurden behoben.
- Ein Problem, das numerische Felder auf der Detailseite betraf, wurde behoben.
- Die Bildschirmtastatur wird nicht mehr gelegentlich auf einigen Geräten ausgeblendet.
- Verschiedene Fehler in der Benutzeroberfläche (UI) wurden behoben, z. B. Fehler, die die Hintergrundfarbe und -positionierung betrafen.
- Die russischsprachige Benutzeroberfläche wurde verbessert.
- Verschiedene Probleme, die dazu führten, dass das System nicht mehr reagierte, wurden behoben.
- Ein Problem, das mit dem erneuten Öffnen des Taschenrechners zusammenhing, wurde behoben.
- **Android Version:** Ein Problem, das dazu führte, dass Android 4.4 beim Starten nicht mehr reagierte, wurde behoben.
- **Android Version:** Die minimale Skalierung wurde auf 50 Prozent reduziert.

## <a name="version-2040"></a>Version 2.0.4.0

Version 2.0.4.0 war die erste allgemein verfügbare Version der Warehouse Management Mobile-App.

### <a name="new-features-fixes-and-improvements-in-version-2040"></a>Neue Funktionen, Korrekturen und Verbesserungen in Version 2.0.4.0

Diese Version führt die folgenden neuen Funktionen, Korrekturen und Verbesserungen ein, die in der Vorschau-Version nicht verfügbar waren:

- Wenn eine Detailkarte zwei Labels enthält, die identische Daten haben, wird eines der Labels ausgeblendet.
- Sonderzeichen werden jetzt standardmäßig angezeigt, und die Option, sie auszublenden, wurde aus den Benutzereinstellungen entfernt.
- Deaktivierte Schaltflächen zum Senden werden jetzt in der kompakten Armansicht als nicht verfügbar angezeigt.
- Eine Änderung der Sequenz-Logik für Steuerelemente sorgt für eine reibungslosere Skalierung über Geräte hinweg. Daher ist es weniger notwendig, die Skalierung von Schriftarten oder Schaltflächen anzupassen.
- Das Standard-Farbdesign wurde auf *Dunkel* geändert.
- Das fehlende Symbol für die deaktivierte Schaltfläche „Senden“ wurde in der Menüband-Ansicht hinzugefügt.
- Timeout-Ausnahmen führen nun zur Verbindungsseite, anstatt einen Inline-Fehler anzuzeigen.
- Wenn keine Sendeaktion verfügbar ist (wie **OK**, **Ja**, **Akzeptieren**, **Erledigt** oder **Fertig**), wird die Schaltfläche Senden deaktiviert.
- Die Stabilität der Apps wurde verbessert.
- Es gibt einen Fix für die Sicherheitslücke [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).
- **Windows-Version:** Ein Problem unter Windows, bei dem die Menüs nach der Größenänderung des Fensters nicht mehr reagierten, wurde behoben.

### <a name="known-issue-in-version-2040"></a>Bekanntes Problem in Version 2.0.4.0

Das folgende bekannte Problem ist in dieser Version vorhanden:

- Diese Version hat ein Problem mit Geräten, die Android 4.4 verwenden. Es kann zu Problemen kommen, wenn Sie die App auf dieser Android-Version verwenden.
