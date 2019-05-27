---
title: Aktivitätsbasierte Fremdarbeit
description: In diesem Thema wird beschrieben wie Fremdarbeitsaktivitäten in einem Produktionsfluss für die Lean Manufacturing verwendet wird.
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 267034
ms.assetid: 15c76a51-fa6d-42d2-994a-c67df6bae6a9
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c219208c7ba5dd3686473d094658ab7f4c1b2b59
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549312"
---
# <a name="activity-based-subcontracting"></a>Aktivitätsbasierte Fremdarbeit

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben wie Fremdarbeitsaktivitäten in einem Produktionsfluss für die Lean Manufacturing verwendet wird.

In Microsoft Dynamics 365 for Finance and Operations gibt es zwei Ansätze für Fremdarbeit: Produktionsaufträge und Lean Manufacturing. Im Lean Manufacturing-Ansatz wird die Fremdarbeit als Dienst modelliert, der mit einer Aktivität eines Produktionsflusses verknüpft ist. Ein spezieller Kostengruppentyp mit der Bezeichnung **Direktes Outsourcing** wurde eingeführt und die Fremdarbeitsdienstleistungen sind nicht mehr Teil einer Stückliste (BOM). Die Kostenbuchhaltung der Fremdarbeit wird vollständig in die Kostenlösung für Lean Manufacturing integriert.

## <a name="production-flows-that-involve-subcontractors"></a>Produktionsflüsse, die durch Fremdarbeit ausgeführt werden
Das Grundprinzip eines Produktionsflusses ändert nicht, wenn Aktivitäten weitergegeben werden. Material fließt noch zwischen Lagerplätzen, Prozeßaktivitäten konvertieren Material in Produkte und verschieben Aktivitäten, Material oder Produkte von einem Lagerplatz zu einem anderen. Sie können Lagerplätze und Fertigungszellen vom Kreditor verwalten lassen, indem Sie das Kreditorenkonto einem Lagerort oder einer Ressource einer Ressourcengruppe zuweisen.  

Basierend auf diesen Funktionen erfordert das Lean Management keine speziellen Funktionen, um den Material- und Produktfluss zu unterstützen. Alle möglichen Szenarien, die Lieferanten als Anbieter von Produktions- oder Transportdiensten umfasst, können auf der Architektur des Produktionsflusses und der Aktivitäten basiert werden.  

Beispielsweise hilft ein Zulieferer in einem Supermarkt aus, der sich am Standort des Zulieferers befindet. Wenn Handhabungseinheiten beim Zulieferer geleert werden, werden die Kanban-Karten der Assemblyzelle zusammen mit der nächsten Lieferung zurückgegeben. Der Supermarkt beim Zulieferer wird dann aufgefüllt. Für Übertragungen auf und zum Zulieferer können keine expliziten Umlagerungsaktivitäten modelliert werden, um einen Lieferungs- und Entnahmeprozess zu unterstützen. Wenn eine explizite Erfassung nicht erforderlich ist, um den physischen Transport zu unterstützen, können mit Buchungsprofilen die Umlagerungsaktivitäten ausgelassen werden.  

Ein Zulieferer kann zum Lastenausgleich verwendet werden, um die Gesamtkapazität des Produktionsflusses auszugleichen. Beispielsweise wird ein Produktionsfluss modelliert, indem geplante Kanban-Regeln verwendet werden. Der Planer verwendet die Kanbanplanungskarte, um Arbeitsgruppen zu planen und auszulasten. Der Planer überwacht auch den konsolidierten Lieferungszeitplan für den Supermakrt auf der Seite **Zeitplan bereitstellen**. Mehrere Zulieferer können in einem oder mehreren Produktionsflüssen modelliert werden, und es gibt möglicherweise mehrere Kanban-Regeln, die verwendet werden können, um das gleiche Produkt an denselben Lagerplatz durch unterschiedliche Aktivitäten zu liefern. Der Planer kann Kanbans zu einer alternativen Kanban-Regel konvertieren, ein Kanban neu einzuplanen, der ursprünglich für  die interne Produktion mit einem alternativen Prozess erstellt wurde. Genau genommen hat die Art der Fertigungszelle keine Auswirkungen auf den Produktionsfluss. Dasselbe Funktionsprinzip gilt für zwei parallele interne Fertigungszellen oder zwei untergeordnete Dienstleistungszellen.   

Wie jede andere Aktivität in einem Produktionsfluss, können in Fremdarbeit ausgeführte Aktivitäten inventarisiertes, nicht-inventarisiertes (Ressource in Fertigung) und \[RIF\] und halbfertige Materialien und Produkte verbrauchen. In allen Argumenten sind die Prozesse für die Planung und die Ausführung mit denen der geregelten Aktivitäten identisch. Darüber hinaus verarbeiten denjenigen Prozesse das gleiche wie interne Arbeit.

## <a name="purchase-process-for-subcontracted-activities-services"></a>Bestellanforderungen für Fremdarbeitsaktivitäten (Services)
Der Einkaufprozess für Fremdarbeitsaktivitäten basiert auf dem physischen Materialfluss, der durch Kanban-Einzelvorgangs-Fortschritt beispielsweise Start oder Beenden erfasst wird. Der Finanzstrom beispielsweise Kosten von Fremdarbeit ist ein sekundärer Fluss, der dem physischen Ablauf folgt. Gleichzeitig ist der Einkaufprozess ein unabhängiger Prozess, der manuelle Regulierung der Bestellungen bei jedem Schritt zulässt. Bestellanforderungen für Fremdarbeitsaktivitäten (Services):

1.  Kaufvertrag erstellen. Der Kaufvertrag wird für den Service erstellt und mit der Aktivität des Produktionsflusses verbunden.
2.  Erstellen einer Bestellung. Eine Freigabebestellung kann für den Dienst auf der Grundlage der geplanten Kanban-Einzelvorgänge erstellt werden. Einzelvorgänge für den gleichen Service können in Bestellpositionen nach Tag, Woche oder Monat gruppiert werden. Die Bestellpositionen können jederzeit erstellt werden, nachdem die Kanban-Einzelvorgänge erstellt wurden. Bestellpositionen können selbst nach der Tatsache erstellt werden. Diese Option wird normalerweise ausgewählt, wenn ein Zulieferer Dienstleistungen ohne zusätzliche Hinweis basierend auf dne Kanbans oder den Kanban-Karten bereitstellt, die der Zulieferer erhält. In diesem Fall können Abweichungen zwischen Bestellung und der Rechnung minimiert werden.
3.  Generieren von Kanban-Karten, Material sowie eine Kommissionierliste, um Zulieferer zu übermitteln, um sich für das Verarbeiten vorzubereiten. Basierend auf detaillierte Modell- des Produktionsflusses, ist die Vorbereitung in der Kanban-Übersicht für Prozessaktivitäten ausgeführt, indem die Kommissionierliste und die Vorbereitungsfunktion verwendet wird. Alternativ ist die Vorbereitung in der Kanban-Übersicht für Umlagerungseinzelvorgänge ausgeführt, indem die Kommissionierliste und Start oder Abschluss verwendet wird. Für inventarisiertes Material können beide Prozesse durch einen WMS-Entnahme- und Lieferprozess unterstützt werden. Ein Frachtbrief kann bei Bedarf erstellt werden.
4.  Generieren Sie Kanbanhandhabungseinheiten und -Kanban-Karten. Nachdem der Verarbeitung werden Karten vom Zulieferer zurückgegeben. Normalerweise schließen die Karten einen Lieferschein ein, der das physische Material angibt, das geliefert wurde. Eine Referenz auf den erbrachten Dienstleistungen ist nicht erforderlich. Der Eingang des Materials und der Fertigprodukte am Debitor wird in der Kanban-Übersicht, abhängig von den Kanban-Karten erfasst. (Entweder die Kanban-Übersicht für Prozessaktivitäten oder die Kanban-Übersicht für Umlagerungseinzelvorgänge werden verwendet, abhängig von der geformten Aktivität.)
5.  Erstellen Sie eine Zugangsempfehlung. Die Zugangsempfehlung kann verwendet werden, um ein Lieferscheindokuments für die eingegangenen Dienste zu ersetzen. Zugangsempfehlungen können basierend auf den abgeschlossenen Kanban-Einzelvorgänge die Fremdarbeitsaktivität für einen ausgewählten Zeitraum generiert werden. Für jeden Einzelvorgangszugang werden verwandte Empfehlungen für die Bestellposition erstellt. Die Zugangsempfehlung kann gedruckt und dem Zulieferer als Eingangsbestätigung gesendet werden.
6.  Rechnung generieren.

Der Prozess endet, wenn für den Zulieferer in einer Periode fakturiert wird. Die Rechnungsabgleichung ist für die Zugangsempfehlungen ausgeführt, die erstellt werden. Da die Zugangsempfehlungen den genauen physischen Zugang des Materials darstellen, wird der dreiseitige Abgleich vereinfacht.

## <a name="configuring-activities-for-subcontracting"></a>Konfigurieren der Aktivitäten für die Fremdarbeit
In den folgenden Abschnitten wird beschrieben, wie die Aktivitäten für das Nebenvertragliche konfiguriert wird.

### <a name="subcontracted-services"></a>Fremdarbeitsservices

Der Zahlungsartikel, der in der aktivitätsbasierten Zulieferung verwendet wird, muss ein Produkt sein, das die folgenden Eigenschaften aufweist:

-   **Produkttyp:** Dienstleistung
-   **Bestandmodellgruppe:** nicht gelagert

Diese Anforderung erzwingt die Nutzung des First in, First out (FIFO)- Lagermodells. **Hinweis:** Kostenberechnung der Produkte erfordert, dass die Standardkosten des Dienstes definiert werden. Eine Rahmenbestellung mit dem Kreditor ist erforderlich. Andernfalls kann die Dienstleistung nicht für die aktivitätsbasierte Zulieferung verwendet werden.

### <a name="subcontracted-process-activities"></a>Weiter gegebene Prozessaktivitäten

Um eine Verarbeitungsaktivität als Fremdarbeitsaktivität zu konfigurieren, führen Sie die folgenden Schritte aus.

1.  Konfigurieren einer von weitergegebenen Arbeitsgruppe. Um eine Arbeitsgruppe als Fremdarbeit zu konfigurieren, müssen Sie eine Ressource des **Lieferanten** tpys erstellen und sie der Arbeitsgruppe (Ressourcengruppe) zuweisen. Eine Ablaufkostenkategorie des **direkten Outsourcing** kostengruppentyps sollt der Arbeitsgruppe zugewiesen werden. Die Kostenkategorien für Einrichtung und Menge sind nicht erforderlich.
2.  Nachdem eine Verarbeitungsaktivität einer von gesetzlichen Bestimmungen unterliegenden Fertigungszelle erstellt und zugeordnet ist, müssen Sie einen Service für die Aktivität konfigurieren, bevor die Produktionsflussversion aktiviert werden kann. Schließen Sie diesen Schritt auf der Seite **Aktivität** **Detail** ab. Bei Aktivitäten, die einer von gesetzlichen Bestimmungen unterliegenden Fertigungszelle zugeordnet sind, wird das **Service-Bedingungen** Inforegister angezeigt. Auf diesem Inforegister können Sie einen Standard-Service hinzufügen, der für alle Ausgabeartikel gültig ist. Wenn besondere  Ausgabeartikel verschiedene Dienstleistungen oder unterschiedliche Service-Berechnungsparameter (beispielsweise Gesamtlayout, ein anderes Service-Verhältnis) erfordern, können Sie andere Dienstleistungen der Aktivität hinzufügen.

## <a name="subcontracted-transfer-activities"></a>Weitergegebene Umlagerungsaktivitäten
Eine Umlagerungsaktivität wird als Fremdarbeitsaktivität konfiguriert, abhängig von den Einstellungen von  **befördert durch** der Umlagerungsaktivität. Die folgenden Optionen sind verfügbar:

-   **Verlader** – Die Aktivität wird weitergegeben, wenn der Übertrag des Von-Lagerort von einem Kreditor /(entsprechend einer Eigenschaft des Lagerorts) ausgeführt wird. Alle ausgewählten Rahmenbestellungen für Leistungen müssen über dieselbe Kreditor-Kennung wie der Lagerort verfügen.
-   **Empfänger** – Die Aktivität wird weitergegeben, wenn der Übertrag des Von-Lagerort von einem Kreditor (entsprechend einer Eigenschaft des Lagerorts) ausgeführt wird. Alle ausgewählten Rahmenbestellungen für Leistungen müssen über dieselbe Kreditor-Kennung wie der Lagerort verfügen.
-   **Spediteur** – Die Aktivität wird an einen beliebigen Kreditor weitergegeben, der den Dienst bereitstellt. Um gültig zu sein, muss ein Spediteur für Lagerortverwaltung erstellt werden und muss ein zugewiesenes Kreditorenkonto aufweisen.

Wie für Prozessaktivitäten müssen Sie einen Standard-Service für weitervergebene  Umlagerungsaktivitäten auf dem Inforegister **Dienstleistungsbedingunges** der Seite **Aktivität** **Details** erstellen.

## <a name="service-quantity-calculation"></a>Servicemengenberechnung
Der ganze Einkaufsprozess basiert auf einer Artikelreferenz für einen Service. Diese Artikelreferenz wird in eine Maßeinheit eines Dienstes gemessen. Services werden üblicherweise entweder in Anzahl Dienstleistungen (Einheiten) oder in Zeit gemessen. Um die Service-Menge, basierend auf den erfassten Abschluss von Kanban-Einzelvorgängen zu berechnen, können die folgenden Methoden zur Verfügung gestellt werden:

-   **Berechnung, die auf der Anzahl von Einzelvorgängen basiert** – Ein Kanban-Einzelvorgang entspricht *n* Service-Einheiten, unabhängig davon, wie die Fertigproduktmenge beschafft wird. Im Lean Manufacturing, ein Einzelvorgang entspricht einer Handhabungseinheit. Diese Berechnungsmethode betrifft alle Services, die einen Festpreis pro Handhabungseinheit haben. Daher gilt diese Methode normalerweise für Umlagerungsaktivitäten. Allerdings kann dies auch für Prozessaktivitäten gelten, die gesamte Handhabungseinheiten verarbeiten.
-   **Berechnung, die auf Grundlage der Produktmenge basiert** – Die Service-Menge ist relativ zu der Produktmenge, die geplant/beschafft wird. Wenn die beschaffte Produktmenge berechnet wird, können Ausschussmengen entweder einbezogen oder nicht berücksichtigt werden. Diese Berechnungsmethode gilt für alle Anfragen, in denen der Service-Preis pro Einheit des verarbeiteten Produkts ausgeglichen wird.
-   **Berechnung, die auf der Aktivitätszeit basiert** – Die theoretischen Aktivitätszeiten werden, basierend auf der Laufzeit der Aktivität, der verarbeiteten Summe der Menge und des Durchsatz-Verhältnisses des verarbeiteten Produkts berechnet. Diese Berechnungsmethode gilt für Dienste, die stundenweise bezahlt werden und Abweichungen in Zeit pro verarbeitetes Produkt aufweisen.

## <a name="cost-accounting-of-subcontracted-services"></a>Kostenbuchhaltung von Fremdarbeitservices
Wenn die Zugangsempfehlung oder ein Lieferschein des Kreditors auf eine Bestellung, die für einen Produktionsfluss erstellt wurde (das heißt, eine Bestellung, die anhand Kanban-Einzelvorgänge für Fremdarbeitsaktivitäten generiert wurde), gebucht wird, wird der Wert des Bons auf RIF-Konten des Produktionsflusses berechnet. Abweichungen von Rechnungen werden auch dem Produktionsfluss zugewiesen. Eine Kostenkategorie für Fremdarbeit wurde eingeführt. Diese Kostenkategorien aktiviert eine transparente Nachverfolgung des Werts der Fremdarbeit, die im RIF zugewiesen und pro Periode verbraucht wird.  

Die Nachkalkulation für Produktionskosten für Produktion am Ende einer Nachkalkulationsperiode berechnet die eigentlichen Abweichungen der Produkte, die dem Produktionsfluss während der Nachkalkulationsperiode produziert werden.

## <a name="modeling-transfers-as-subcontracted-activities"></a>Modellvariablen der Überträge als Fremdarbeitsaktivitäten
Menschen betrachten den Transport oft als unproduktive und denken, er habe keinen Wert. Wenn die Kosten der Zulieferung mit den Kosten der internen Produktion verglichen werden, müssen die Kosten der zusätzlichen Transporttätigkeit berücksichtigt werden. Ein Produktionsfluss, der mehrere Lagerplätze umfasst und Transportdienste erfordert, muss den Transportkosten als Teil der Kosten zur Festlegung der Produkte an den Debitor entsprechen. 

Mit der aktivitätsbasierten Fremdarbeit im Lean Manufacturing können Sie Spediteure integrieren und Kreditoren bewegen, die Material und Produkte zwischen Lagerplätzen eines Produktionsflusses verschieben. Durch die Modellierung einer Umlagerungsaktivität können Sie einen Spediteur oder Kreditor zuweisen. Die Umlagerungsaktivitäten/der Einzelvorgang basiert auf einem Service und einer Rahmenbereinbarung, und Sie können Bestellungen und Zugangsempfehlungen auf Basis der tatsächlichen Umlagerungseinzelvorgänge erstellen. Diese Funktionen sind identisch wie die Funktionalität für die Weitervergabe von Prozessaktivitäten.  

Daher unterstützt Finance and Operations jetzt BOM-Berechnungen, die Transportdienste, die Erstellung von Bestellungen, integrierte Zugangserfassung und die Integration von Transportdienstleistungskosten in die Produktionsflussnachkalkulation enthalten.



