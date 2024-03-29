---
title: Bezugsprinzipien
description: Dieser Artikel beschreibt die vier Bezugsprinzipien für den Rohmaterialverbrauch.
author: johanhoffmann
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgShopSupervisorReleaseOrders
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 89fd38ea6d2c1635e9d8974ab99c2e4cdae4d6be
ms.sourcegitcommit: 8d072505f66f507aafbaae65bedf3b530eb6cb7b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9266427"
---
# <a name="flushing-principles"></a>Bezugsprinzipien

[!include [banner](../includes/banner.md)]

Die Bezugsprinzipien reflektieren verschiedene Verbrauchsstrategien für Rohmaterialen, die in Produktionsprozessen verwendet werden. Verbrauch ist der Prozess, bei dem Material aus dem Bestand vor Ort abgezogen wird und der Wert der verbrauchten Materialien für Produktionsaufträge und Chargenaufträge auf **Ressource in Fertigung** (RIF) gesetzt wird. Rohmaterialien werden normalerweise von einem Standort aus verbraucht, der für den Prozess konfiguriert ist, der das Material verbraucht. Dieser Standort wird als Produktionseingangsstandort bezeichnet.

Vor dem Materialverbrauch werden die Materialien an den Eingangsstandort transportiert. Die folgende Abbildung zeigt den Zykluszählprozess.

[![scenario4a.](./media/scenario4a.png)](./media/scenario4a.png)

1. Materiallagerort
2. Rohmaterialentnahme
3. Lagerplatz für Produktions-Wareneingang
4. Rohmaterialverbrauch
5. Produktionsprozess

Der Materialverbrauch wird durch die folgenden die vier Bezugsprinzipien geregelt:

- Manuell
- Starten
- Fertig stellen
- Am Lagerplatz verfügbar

Die Bezugsprinzipien sind in einer Hierarchie mit Standardwerten konfiguriert. Die Hierarchie beginnt mit dem freigegebenen Produkt, wo das Bezugsprinzip den Wert **Start** hat. Auf der Stückliste (BOM) oder Formelposition kann das Bezugsprinzip vom Produkt überschrieben werden. Das Standardbezugsprinzip der BOM-Positionen aus der Produktion oder der Formelpositionen bei Batchaufträgen stammt vom Produkt oder von dem überschriebenen Wert von der BOM oder den Formeln.

## <a name="description-of-the-flushing-principles"></a>Beschreibung der Bezugsprinzipien

### <a name="manual"></a>Manuell
Das manuelle Bezugsprinzip zeigt an, dass die Registrierung des Materialverbrauchs eine manuelle Tätigkeit ist. Dieses Prinzip ist beispielsweise relevant, wenn Sie die Zeit nachverfolgen wollen, und wenn die Menge der verbrauchten Chargennummern oder Seriennummern für Nachverfolgungszwecke berücksichtigt werden muss. Ein manueller Verbrauch wird in einem Produktionspicklistenjournal aufgezeichnet. Für Artikel, die für Lagerverwaltungsprozesse (WMS) aktiviert sind, kann ein Handheld Flow angewendet werden.

### <a name="start"></a>Start
Das Bezugsprinzip Start zeigt an, dass Material automatisch verbraucht wird, wenn der Produktionsauftrag gestartet wird. Die Menge des verbrauchten Materials ist proportional zu der gestarteten Menge. Wenn das Bezugsprinzip Start zusammen mit dem Herstellungsausführungssystem verwendet wird, kann es auch für einen Bezug von Materialien verwendet werden, wenn eine Operation oder ein Verarbeitungsauftrag gestartet werden. Dieses Prinzip ist beispielsweise relevant, wenn eine geringe Verbrauchsvarianz vorliegt, wenn die Materialien einen geringen Wert haben, wenn keine Nachverfolgung erforderlich ist, oder wenn die Operationen eine kurze Laufzeit aufweisen. 

### <a name="finish"></a>Fertig stellen
Das Bezugsprinzip Fertigstellung zeigt an, dass Material automatisch verbraucht wird, wenn der Produktionsauftrag als fertiggestellt gemeldet wird, oder wenn eine Operation, die für den Verbrauch der Materialien eingerichtet ist, als abgeschlossen registriert wird. Die Menge des verbrauchten Materials ist proportional zu der als fertiggestellt gemeldeten Menge. Wenn das Bezugsprinzip Fertigstellung zusammen mit dem Herstellungsausführungssystem verwendet wird, kann es auch für einen Bezug von Materialien verwendet werden, wenn eine Operation oder ein Verarbeitungsauftrag abgeschlossen werden. Dieses Prinzip ist in denselben Situationen relevant wie das Prinzip Start. Das Prinzip Fertigstellung ist jedoch für Operationen vorgesehen, die eine längere Laufzeit haben, und die Materialien nicht auf RIF gesetzt werden sollen, bevor die Operation abgeschlossen ist.

> [!NOTE]
> Sie können „Prinzip für automatischen Artikelverbrauch beenden“ nicht zusammen mit Planungsartikeln verwenden. Stattdessen sollten Sie „Prinzip für automatischen Artikelverbrauch starten“ verwenden. Geplante Artikel haben den Produktionstyp *Planungsartikel* und nur Co-Produkte und Nebenprodukte für Chargenaufträge, die für geplante Artikel erstellt wurden, als beendet gekennzeichnet werden.

### <a name="available-at-location"></a>Am Lagerplatz verfügbar
Das Bezugsprinzip Am Lagerplatz verfügbar zeigt an, dass das Material automatisch verbraucht wird, wenn es als für die Produktion entnommen registriert wird. Das Material wird als vom Standort entnommen registriert, wenn die Arbeit für die Rohmaterialentnahme abgeschlossen ist, oder wenn das Material am Produktionseingangsstandort zur Verfügung steht und die Materialposition für das Lager freigegeben wird. Die Entnahmeliste, die während des Prozesses erzeugt wird, wird in einem Chargenauftrag gebucht. Dieses Prinzip ist beispielsweise relevant, wenn Sie sehr viele Entnahmeaktivitäten für einen Produktionsauftrag haben. In diesem Fall müssen Sie die Entnahmeliste nicht manuell aktualisieren, und Sie können eine aktuelle Ansicht des RIF-Saldos erhalten.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
