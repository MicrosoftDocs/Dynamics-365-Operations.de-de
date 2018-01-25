---
title: "Stücklisten- und Formelpositionen für den Lagerort freigeben"
description: "In diesem Thema wird der Prozess für die Freigabe von Rohmaterial für Stücklistenpositionen und Formelpositionen zum Lagerort beschrieben."
author: johanhoffmann
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: johanho
ms.search.validfrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 0ca19ab9ed7a52328c5dd5252c418bb9343bdc2b
ms.openlocfilehash: 6aec3532a36a2c1e67ee0c189e45a352ad7670f6
ms.contentlocale: de-de
ms.lasthandoff: 12/14/2017

---

# <a name="release-bom-and-formula-lines-to-the-warehouse"></a>Stücklisten- und Formelpositionen für den Lagerort freigeben

In diesem Thema wird der Prozess für die Freigabe von Rohmaterial für Stücklisten-(BOM)-Positionen und Formelpositionen zum Lagerort beschrieben. Wenn Sie eine Stücklisten- oder eine Formelposition dem Lagerort freigeben, bestimmt das System zuerst, ob das Material am Produktionseingangslagerplatz im Fertigungsbereich bereits vorhanden ist, wo das Material für den Produktionsprozess verbraucht wird.

- Wenn das Material am Produktionseingangslagerplatz verfügbar ist, wird es sofort von diesem Standort entnommen, nachdem das Signal für die Freigabe von Material an den Lagerort gegeben wird.
- Wenn das Material am Produktionseingangslagerplatz nicht verfügbar ist, gibt die Materialfreigabe an, dass Material von Lagerplätzen im Lagerort zum Produktionseingangslagerplatz verschoben werden muss. Das Material wird über Lagerortarbeit für Rohmaterialentnahme verschoben. Daher müssen Lagerortprozesse für Rohmaterialentnahme konfiguriert werden. Weitere Informationen finden Sie unter [Wiederbeschaffung](../warehousing/replenishment.md) und [Steuern von Lagerarbeit mithilfe von Arbeitsvorlagen und Lagerplatzrichtlinien](../warehousing/control-warehouse-location-directives.md).

## <a name="methods-for-releasing-bom-and-formula-lines"></a>Methoden für die Freigabe von Stücklisten- und Formelpositionen

Sie können die Freigabe von Stücklisten- und Formelpositionen konfigurieren, sodass sie als Teil der Freigabe eines Produktionsauftrags oder Chargenauftrags erolgt. Alternativ kann die Freigabe über einen Batchauftrag gesteuert werden oder als manuelle Interaktion ausgeführt werden.

Die Methode, die verwendet wird, um Stücklisten- und Formelpositionen freizugeben, wird vom Parameter **Produktionspositionsfreigabe** gesteuert. Sie können diesen Parameter unter **Produktionssteuerung** \> **Einstellungen** \> **Produktionsparameter** finden.

- **Freigeben von Stücklisten- und Formelpositionen als Teil der Produktions- oder Chargenauftragsfreigabe** – Bei dieser Methode werden Stücklisten- und Formelpostionen für einen Produktions- oder einen Chargenauftrag als Teil des Prozesses der Freigabe des Auftrags freigegeben. Normalerweise werden während der Freigabe eines Produktions- oder Chargenauftrags Produktionseinzelvorgänge für die Fertigungsbereichsmitarbeiter freigegeben, und die Produktionspapiere werden gedruckt. Bei diesem Prozess wird auch der Status des Auftrags zu **Freigegeben** geändert.
- **Freigeben von Stücklisten- und Formelpositionen über einen Batchauftrag oder eine manuelle Interaktion** – In dieser Methode können Stücklisten- und Formelpositionen nur durch den Batchauftrag **Automatische Freigabe von Stücklisten- und Formelpositionen** freigegeben werden oder als manuelle Interaktion. Um Stücklisten- und Formelpositionen manuell freizugeben, wählen Sie auf der Produktionsauftrags-Listenseite oder der Produktionsauftrags-Detailseite im Aktivitätsbereich die Option **Für Lagerort freigeben** aus.

## <a name="releasing-the-bom-and-formula-lines-by-using-a-batch-job"></a>Freigabe der Stücklisten- und Formelpositionen mithilfe eines Bachauftrags

Der Batchauftrag **Automatische Freigabe von Stücklisten- und Formelpositionen** durchläuft die ausgewählten Stücklisten- und Formelpositionen, bei denen eine Restmenge freigegeben werden muss. Der Einzelvorgang berücksichtigt nur Aufträge, die einen Status **Freigegeben**, **Gestartet** oder **Als fertig gemeldet** besitzen. Wenn eine Stücklisten- oder Formelposition eine freizugebende Restmenge hat, wird durch den Einzelvorgang bis zur Menge freigegeben, die von der Menge abgedeckt werden kann, die bereits physisch reserviert wurde und die Menge, die physisch verfügbar ist.

### <a name="example-of-a-batch-job-release"></a>Beispiel einer Batchauftragsfreigabe

| Szenario | Für die Freigabe verbleibende Restmenge | Physisch reservierte Menge | Physisch verfügbare Menge | Vom Batchauftrag freigegebene Menge |
|----------|-------------------------------|------------------------------|-------------------------------|------------------------------------|
| 1        | 100                           | 20                           | 90                            | 100                                |
| 2        | 100                           | 20                           | 70                            | 90                                 |
| 3        | 100                           | 0                            | 90                            | 90                                 |
| 4        | 100                           | 0                            | 110                           | 100                                |
| 5        | 100                           | 20                           | 0                             | 20                                 |

### <a name="batch-job-setup"></a>Batchauftragssetup

In der Abfrage für den Batchauftrag **Automatische Freigabe der Stücklisten- und Formelpositionen** können Sie ein Filterkriterium einrichten, um anzugeben, wie viele Tage im Voraus der Einzelvorgang nach Positionen suchen soll, die nicht freigegebene Mengen haben. In der Abfrage für den Einzelvorgang, im Feld **Rohmaterialdatum**, verwenden Sie die Funktion **(LessThanDate())** als Filterkriterium.

Die folgende Abbildung zeigt einen Produktionsauftrag, der zwei Einzelvorgänge hat, 10 und 20, die die Zusammenstellung und Verpackung für den Produktionsauftrag abdecken. Jeder Einzelvorgang ist so eingerichtet, dass er eine Menge von Material verbraucht. In dieser Abbildung entspricht der Freigabezeitraum, der durch den grünen Pfeil unter der Zeitposition angezeigt wird der Anzahl der Tage, die im Kriterium **(LessThanDate())** festgelegt wurde. Beispielsweise gibt **(LessThanDate (2))** an, dass der Einzelvorgang nur innerhalb eines Zeitraums von zwei Tagen nach nicht freigegebenen Mengen suchen soll.

![Beispiel eines Produktionsauftrags, der zwei Batchaufträge hat](media/bach-job-setup.PNG)

## <a name="releasing-material-per-operation-number-or-in-proportion-to-the-amount-of-finished-goods"></a>Freigabe von Material pro Arbeitsgangnummer oder im Verhältnis zur Menge der Fertigartikel

Wenn Sie Materialien mithilfe der Parametereinstellung **Bei Freigabe des Produktionsauftrags** freigeben, wenn Sie eine manuelle Freigabe durchführen, haben Sie zwei Optionen zur Steuerung der Materialfreigabe:

- Geben Sie Material pro Arbeitsgangnummer frei.
- Geben Sie Material im Verhältnis zur Menge der Fertigartikel frei.

### <a name="release-material-per-operation-number"></a>Freigeben von Material pro Arbeitsgangnummer

Um die Arbeitsgänge zu steuern, zu denen Material freigegeben werden soll, verwenden Sie die Seite **Für Lagerort freigeben**.

- Wählen Sie **Produktionssteuerung** \> **Produktionsaufträge** \> **Alle Produktionsaufträge** aus, wählen Sie einen Produktionsauftrag aus, und klicken Sie auf der Registerkarte **Lagerort** dann auf **Für Lagerort freigeben**. Verwenden Sie dann die Felder **Von Arbeitsgang-Nr.** und **Bis Arbeitsgang-Nr.**, um den Bereich der Arbeitsgangnummern anzugeben.

Die folgende Abbildung zeigt einen Produktionsauftrag, der zwei Arbeitsgänge hat, 10 und 20. Wenn Sie in diesem Beispiel die Freigabe auf Arbeitsgang 10 einschränken, wird nur Material M9203 freigegeben.

![Beispiel der Freigabe von Material pro Arbeitsgangnummer](media/two-operations.PNG)

### <a name="release-material-in-proportion-to-the-amount-of-finished-goods"></a>Freigeben von Material im Verhältnis zur Menge der Fertigartikel

Sie können Rohmaterial für eine Teilmenge der Fertigartikel oder in einer bestimmte Einheit freigeben.

- Um Rohmaterial für eine Teilmenge von Fertigartikeln freizugeben, wählen Sie **Produktionssteuerung** \> **Produktionsaufträge** \> **Alle Produktionsaufträge** aus, wählen Sie einen Produktionsauftrag aus, und klicken Sie auf der Registerkarte **Lagerort** dann auf **Für Lagerort freigeben**. Geben Sie dann eine Menge im Feld **Menge** ein.

    Beispielsweise wird ein Produktionsauftrag für 1.000 Stück (Stk.) erstellt und geplant. Der Abteilungsleiter des Fertigungsbereichs plant die Produktion von 100 Stk. für die nächste Schicht und möchte nur für diese Schicht Materialien freigeben. In diesem Fall kann der Abteilungsleiter das Feld **Menge** verwenden, um Materialien für die 100 Stk. freizugeben, die für die nächste Schicht geplant sind.

- Um Rohmaterial in einer bestimmten Einheit freizugeben, wählen Sie **Produktionssteuerung** \> **Produktionsaufträge** \> **Alle Produktionsaufträge** aus, wählen Sie einen Produktionsauftrag aus, und klicken Sie auf der Registerkarte **Lagerort** dann auf **Für Lagerort freigeben**. Wählen Sie dann mithilfe des Felds **Einheit** die Einheit von Fertigartikeln, in der Material freigegeben werden soll.

    Die Einheiten, die zur Verfügung stehen, werden in der Einheitsnummernkreisgruppen-ID der Fertigartikel definiert.

    Ein Fertigartikel weist beispielsweise die folgende Einheitskonvertierung zwischen Kilogramm (kg) und Palette (PL) auf: 1 PL = 50 kg. Um einen Produktionsauftrag für 5.000 kg von Fertigkartikeln zu erstellen, können Sie Rohmaterialen für die Anzahl der Paletten freigeben, für die Sie die Fertigung planen. Wählen Sie **PL** als Einheit aus, und wählen Sie dann eine entsprechende Zahl im Feld **Menge** aus.
