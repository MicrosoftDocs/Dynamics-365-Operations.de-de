---
title: Bestandsmarkierung mit Planungsoptimierung
description: Dieser Artikel enthält Informationen über die Optionen, die für die Markierung von Beständen in umgewandelten Aufträgen zur Verfügung stehen, wenn Sie die Planungsoptimierung verwenden.
author: t-benebo
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 55c83cdbc144f194fe80e8281a35ec7ff43d551e
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219936"
---
# <a name="inventory-marking-with-planning-optimization"></a>Bestandsmarkierung mit Planungsoptimierung

[!include [banner](../../includes/banner.md)]

Dieser Artikel enthält Informationen über die Optionen, die für die Markierung von Beständen in umgewandelten Aufträgen zur Verfügung stehen, wenn Sie die Planungsoptimierung verwenden.

*Markierung* wird verwendet, um Angebot und Nachfrage zu verknüpfen. Sie ähnelt dem *Bedarfsverursacher*, der angibt, wie die Produktprogrammplanung die Nachfrage zu decken gedenkt. Aus Sicht der Planung besteht der Hauptunterschied darin, dass die Markierung dauerhafter ist als der Bedarfsverursacher.

Die Markierung wurde eingeführt, um spezielle Kalkulationsszenarien für First In, First Out (FIFO) und Last In, First Out (LIFO) zu unterstützen. Sie wird jetzt aber auch für einige Nicht-Kalkulationsszenarien verwendet. Die Markierung zwischen Angebot und Nachfrage ist optional und fast permanent. Die Markierung kann manuell von einem Benutzer entfernt werden, oder sie kann durch die Ausführung einer Verkaufsauftragszeilenauflösung entfernt werden, bei der die Option **Markierung entfernen** ausgewählt ist.

Die Bedarfsverursacher werden von der Produktprogrammplanung während der Deckung gesteuert, um die Nachfrage mit dem benötigten Angebot zu verknüpfen. Die Bedarfsverursacher können für jeden Planungslauf aktualisiert werden, um das Angebot zu optimieren, das zur Deckung der Nachfrage erforderlich ist. Wenn die Produktprogrammplanung Bedarfsverursacher-Informationen aktualisiert, berücksichtigt sie alle vorhandenen Markierungen.

Der Bedarfsverursacher beginnt mit der Einbeziehung relevanter Markierungen, Bestandsreservierungen und Bestellreservierungen in der folgenden Sequenz:

1. Markierung zwischen Bedarf und Angebot
1. Bestandsreservierungen
1. Reservierungen auf Bestellung

Wenn Sie einen Planauftrag umwandeln, bietet die Dialogbox **Umwandlung** ein Feld **Bestandsmarkierung aktualisieren**, mit dem Sie Markierungsoptionen für die Aufträge festlegen können, die während der Umwandlung erstellt werden. Wählen Sie einen der folgenden Werte aus:

- *Nein* - Es wird keine Bestandsmarkierung angewendet.
- *Standard* - Die Bestandsmarkierung wird entsprechend dem Bedarfsverursacher aktualisiert. Ein Bedarfsauftrag (Nachfrage) wird gegen einen Erfüllungsauftrag (Lieferung) markiert. Wenn eine bestimmte Menge auf dem Erfüllungsauftrag verbleibt, wird sie nicht markiert und die Referenzinformationen bleiben leer. Wenn z. B. ein Verkaufsauftrag über 100 ea gegen eine Einkaufsbestellung über 150 ea verrechnet wird, werden die Referenzinformationen nur dem Verkaufsauftrag zugewiesen.
- *Erweitert* - Sowohl der Bedarfsauftrag (Nachfrage) als auch der Erfüllungsauftrag (Lieferung) werden markiert, unabhängig von der Menge, die auf dem Erfüllungsauftrag verbleibt. Wenn z. B. ein Verkaufsauftrag über 100 ea mit einer Einkaufsbestellung über 150 ea verrechnet wird, werden die Referenzinformationen sowohl dem Verkaufsauftrag als auch der Einkaufsbestellung zugewiesen.
- *Einstufiger Standard* – Es wird eine einstufige Markierung verwendet. Die Markierung auf einer Ebene markiert nur den Hauptartikel, nicht seine Komponenten der Stückliste (BOM). Daher können Sie die Komponentenzuordnung für Fertigungsaufträge nach der Fixierung flexibel halten. Die einstufige Markierung ermöglicht es dem System, Last-Minute-Bedarfsänderungen zu optimieren. Bei der einstufigen *Standard*-Markierung werden Bedarfsaufträge mit ihren Auftragserfüllung-Aufträgen markiert, aber Auftragserfüllungs-Aufträge werden nicht markiert, wenn sie eine Restmenge haben.
- *Einzelne Ebene erweitert* – Es wird eine einstufige Markierung verwendet. Bei der erweiterten *Einzelebenen*-Markierung werden Bedarfsaufträge mit ihren Auftragserfüllung-Aufträgen markiert, und Auftragserfüllungs-Aufträge werden immer markiert, egal ob sie eine Restmenge haben oder nicht.

Um die Standardmarkierungsoption für Ihr System festzulegen, gehen Sie zu **Masterplanung \> Konfiguration \> Masterplanungsparameter**. Dann auf der **Standard-Update** Registerkarte, legen Sie das Feld **Kennzeichnung aktualisieren** auf die bevorzugte Option fest.

> [!NOTE]
> Die Optionen *Einzelebenenstandard* und *Einzelne Ebene erweitert* sind nur verfügbar, wenn die *Automatisierung der Lieferungen zur Auftragsfertigung* Funktion auf Ihrem System aktiviert ist. Weitere Informationen zu dieser Funktion und ihrer Aktivierung finden Sie unter [Automatisierung der Lieferungen zur Auftragsfertigung](../make-to-order-supply-automation.md).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
