---
title: Planungszeiträume
description: In diesem Thema wird beschrieben, wie Sie Planungszeiträume einrichten, wenn Sie die Planungsoptimierung verwenden. Ein Planungszeitraum gibt Ihren Planungshorizont und Ihr Limit an.
author: ChristianRytt
ms.date: 01/18/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2021-01-18
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 32bf890d1ff74155a75862afd6b0e861fbfc10e2
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567318"
---
# <a name="coverage-time-fences"></a>Planungszeiträume

[!include [banner](../../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie *Planungszeiträume* einrichten, wenn Sie die Planungsoptimierung verwenden. Planer können den Planungshorizont (den Planungszeitraum in Tagen) definieren und Angebot und Nachfrage ausschließen, die über diesen Horizont hinausgehen. Daher helfen Planungszeiträume dabei, „Rauschen“ zu vermeiden, das durch Liefervorschläge verursacht wird, auf die Sie monatelang nicht reagieren müssen. Beispiele hierfür sind Prognosen für das nächste Jahr und Kundenaufträge, die weit über die normale Vorlaufzeit hinausgehen.

Ein Planungszeitraum ist die Anzahl der Tage nach dem heutigen Datum (oder genauer gesagt dem Datum, an dem Sie den Planungslauf durchführen), für die Angebot und Nachfrage ausgeschlossen sind. Um Verzögerungen zu vermeiden, müssen Sie sicherstellen, dass der Planungszeitraum länger als die Gesamtvorlaufzeit ist. Der Standardsystemwert sind 100 Tage.

Sie können auf jeder der folgenden Ebenen einen Planungszeitraum festlegen:

- **Dispositionssteuerungsgruppe** – Sie können für jede Dispositionssteuerungsgruppe einen Planungszeitraum festlegen.
- **Artikeldeckung** – Sie können den Planungszeitraum überschreiben, der von der Dispositionssteuerungsgruppe geerbt wird, die einem Artikel zugewiesen ist.
- **Produktprogrammplan** – Sie können die Planungszeiträume überschreiben, der von der Dispositionssteuerungsgruppe und den Artikeldeckungseinstellungen geerbt wird.

In den folgenden Abschnitten wird erläutert, wie Sie auf jeder Ebene eine Dispositionssteuerungsgruppe angeben.

## <a name="set-a-coverage-time-fence-for-a-coverage-group"></a>Einen Planungszeitraum für eine Dispositionssteuerungsgruppe festlegen

Wenn Sie einen Planungszeitraum für eine Dispositionssteuerungsgruppe angeben, gilt die Einstellung für alle Artikel (Produkte), die zu dieser Gruppe gehören. Sie können jedoch die Einstellung für bestimmte Artikel oder bestimmte Produktprogrammpläne überschreiben.

Führen Sie die folgenden Schritte aus, um einen Planungszeitraum für eine Dispositionssteuerungsgruppe festzulegen.

1. Gehen Sie zu **Produktprogrammplanung \> Einstellungen \> Planungshorizont \> Dispositionssteuerungsgruppen**
1. Wählen Sie eine vorhandene Dispositionssteuerungsgruppe in der Liste aus oder erstellen Sie eine neue Dispositionssteuerungsgruppe.
1. Auf dem Inforegister **Allgemein** stellen Sie das Feld **Planungszeitraum (Tage)** auf die Anzahl der Tage ein, die Sie als Planungszeitraum für die Dispositionssteuerungsgruppe verwenden möchten.

## <a name="set-a-coverage-time-fence-for-a-specific-item"></a>Einen Planungszeitraum für einen bestimmten Artikel festlegen

Jeder Artikel (Produkt) gehört zu einer Dispositionssteuerungsgruppe. Wenn einem Artikel keine Dispositionssteuerungsgruppe explizit zugeordnet ist, gilt eine Standard-Dispositionssteuerungsgruppe. Jede Artkel erbt einen Planungszeitraum von seiner Dispositionssteuerungsgruppe. Sie können diesen Zeitraum jedoch für bestimmte Artikel nach Bedarf überschreiben.

Führen Sie die folgenden Schritte aus, um einen Planungszeitraum für einen bestimmten Artikel festzulegen.

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Wählen Sie im Raster ein Produkt aus.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Plan** in der Gruppe **Planungshorizont** die Option **Artikeldeckung** aus.
1. Auf der Seite **Artikeldeckung** auf der Registerkarte **Überblick** wählen Sie eine Zeile für den Standort aus, für den Sie einen Planungszeitraum festlegen möchten, oder erstellen Sie eine.
1. Wählen Sie die Registerkarte **Allgemein** aus, um die Einstellungen für den ausgewählten Standort zu öffnen.
1. Aktivieren Sie das Kontrollkästchen **Deckungsgruppeneinstellungen überschreiben**.
1. Stellen Sie das Feld **Planungszeitraum (Tage)** auf die Anzahl der Tage ein, die Sie als Planungszeitraum für den Artikel verwenden möchten.

## <a name="set-a-coverage-time-fence-for-a-specific-master-plan"></a>Einen Planungszeitraum für einen bestimmten Produktprogrammplan festlegen

Sie können auf Ebene des Produktprogrammplans einen Planungszeitraum festlegen. Auf diese Weise definieren Sie die Anzahl der Tage, die die Produktprogrammplan-Berechnung für einen Produktprogrammplan abdeckt. Diese Einstellung überschreibt alle Einstellungen für den Planungszeitraum, die für jeden relevanten Artikel und jede relevante Dispositionssteuerungsgruppe definiert wurden.

Führen Sie die folgenden Schritte aus, um einen Planungszeitraum für einen bestimmten Produktprogrammplan festzulegen.

1. Wechseln Sie zu **Produktprogrammplanung \> Einrichtung \> Pläne \> Produktprogrammpläne**.
1. Wählen Sie einen vorhandenen Produktprogrammplan in der Liste aus, oder erstellen Sie einen neuen Produktprogrammplan.
1. Setzen Sie auf dem Inforegister **Planungszeitraum in Tagen** die Option **Planungshorizont** auf *Ja*. Geben Sie dann in dem Feld unter der Option die Anzahl der Tage ein, die Sie als Planungszeitraum für den Produktprogrammplan verwenden möchten.

## <a name="considerations-for-coverage-time-fences"></a>Überlegungen zu Planungszeiträumen

Berücksichtigen Sie beim Einrichten von Planungszeiträumen die folgenden Punkte:

- Planungszeiträume wirken sich nur auf Eingabedaten für den Produktprogrammplan aus. Wenn Verzögerungen auftreten, haben die resultierenden Planaufträge möglicherweise ein Datum, das nach dem heutigen Datum liegt, zuzüglich des Planungszeitraums.
- Planungszeiträume werden in Kalendertagen angegeben. Kalender, die Arbeitstage verwenden, wirken sich nicht auf die Planungszeitraumberechnung aus. Beispielsweise wird eine Woche immer als sieben Tage betrachtet, selbst wenn Wochenenden im Arbeitszeitkalender als geschlossene Tage eingerichtet sind.
- Anforderungstransaktionen werden nicht für Angebot und Nachfrage generiert, die außerhalb des Planungszeitraums liegen.
- Wenn ein genehmigtes Angebot und eine genehmigte Nachfrage außerhalb des Planungszeitraums liegen, wird es nicht in das Modul geladen. Daher wird keine Wiederbeschaffung ausgelöst, und Verzögerungen werden nicht berechnet. Trotzdem sollten Angebot und Nachfrage nicht aus dem System gelöscht werden.
- Abweichungen in den Sicherheitsbestandsmengen (von den Mindestbestandsfaktoren) werden ignoriert, wenn sie außerhalb des Planungszeitraums liegen.
- Der Intercompany-Bedarf wird ignoriert, wenn das angeforderte Lieferdatum, das berechnet wird, nicht innerhalb des Planungszeitraums liegt. Beachten Sie, dass bei der integrierten Produktprogrammplanung der Intercompany-Bedarf nicht durch den Planungszeitraum begrenzt ist.
- Bedarfsplanungen werden ignoriert, wenn das Budgetdatum nicht innerhalb des Planungszeitraums liegt. Beachten Sie, dass bei der integrierten Produktprogrammplanung Bedarfsplanungen nicht durch den Planungszeitraum begrenzt sind.
- Die Planungsoptimierung ist zeitzonenabhängig. Dabei werden die Zeitzone an den Angebots- und Nachfragestellen sowie der Zeitpunkt des Planungslaufs berücksichtigt. Beispielsweise wird die Produktprogrammplanung am 15. Oktober um 11:00 Uhr von einem Standort in Dänemark (Zeitzone GMT + 1) aus ausgelöst, und es wird ein Planungszeitraum von zehn Tagen verwendet. In diesem Fall werden Angebot und Nachfrage von einem Standort in Seattle (GMT-8-Zeitzone) bis 2 Uhr morgens am 25. Oktober berücksichtigt (= zehn 24-Stunden-Tage nach Auslösung der Produktprogrammplanung abzüglich der Zeitzonendifferenz von neun Stunden). Beachten Sie, dass die integrierte Produktprogrammplanung nur das Datum des Zeitrahmens berücksichtigt. Daher kann das Ergebnis abweichen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]