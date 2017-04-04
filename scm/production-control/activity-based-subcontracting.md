---
title: "Aktivitätsbasierte Zulieferung"
description: "In diesem Thema wird beschrieben wie detailliert Fremdarbeitsaktivitäten in einem Produktionsfluss für die Produktion verwendet."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 267034
ms.assetid: 15c76a51-fa6d-42d2-994a-c67df6bae6a9
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 8e57c53ca894aa44b71e15c1f66bd7c722ea8a81
ms.lasthandoff: 03/31/2017


---

# <a name="activity-based-subcontracting"></a>Aktivitätsbasierte Zulieferung

In diesem Thema wird beschrieben wie detailliert Fremdarbeitsaktivitäten in einem Produktionsfluss für die Produktion verwendet.

In Microsoft Dynamics 365 für Arbeitsgänge, gibt es zwei Arten für das Nebenvertraglich Folgendes gesteuert wird: Produktionsaufträge und Produktion. Im Produktionsansatz wird die Lohnarbeit als Dienst modelliert, der einer Aktivität eines Produktionsflusses verknüpft ist. Ein spezieller Typ Kostengruppentyp, der Bezeichnung ** direktes Outsourcing ** ist und die Fremdarbeitsdienstleistungen sind nicht mehr zu einer Stückliste (BOM) eingegeben. Die Kostenrechnung der von gesetzlichen Bestimmungen unterliegenden Arbeit ist vollständig in die Nachkalkulationslösung für "Produktion" - integriert.

## <a name="production-flows-that-involve-subcontractors"></a>Produktionsflüsse, die Zulieferer ausgeführt werden
Das Dies eines Produktionsflusses nicht geändert, wenn Aktivitäten von reguliert sind. Material fließt noch zwischen Lagerplätzen, Produkten, Prozeßaktivitätsbekehrtmaterial und Umlagerungsaktivitäten verschieben Material oder Produkte aus einem Lagerplatz auf einen anderen. Sie können Lagerplätze und Fertigungszellen modellieren, wie Kreditor-verwaltet, indem Sie das Kreditorenkonto an einen Lagerort oder eine Ressource einer Ressourcengruppe zuweisen.  

Basierend auf diesen Funktionen erforderlich Produktion keine speziellen Funktionen, um den Material- und Produktfluss zu unterstützen. Alle Szenarien möglichen, die Lieferanten als privater der Produktion oder der Transportdienste umfassen, können auf Geschäftsjahren die Architektur des Produktionsflusses und der Aktivitäten modelliert werden.  

Beispielsweise arbeitet ein Zulieferer in einem Supermarkt aus, der am Zulieferer befindet. Wenn Zulieferer Handhabungseinheiten am geleert werden, werden durch die Kanban-Karten der Assemblyzelle zusammen mit der Kanban-Regel der nächsten Lieferung zurückgegeben. Der am Supermarkt Zulieferer wird aufgefüllt. Für Übertragungen auf und von dem als Zulieferer können keine expliziten Umlagerungsaktivitäten modelliert werden, um einen Lieferungs eine Entnahme und prozess zu unterstützen. Wenn eine explizite Erfassung nicht erforderlich ist, um den physischen Transport zu unterstützen, können mit Buchungsprofilen die Umlagerungsaktivitäten werden ausgelassen.  

Ein Zulieferer kann zum Lastenausgleich verwendet werden der Gesamtkapazität des Produktionsflusses. Beispielsweise wird ein Produktionsfluss modelliert, indem geplante Kanban-Regeln verwendet. Der Planer die verwendet Kanbanplanungskarte, um bei Bedarf zu planen und Niveauregulierung beide Fertigungszellen. Der überwacht Planer auch den konsolidierten Lieferungszeitplan für den auf der Lieferungszeitplan Supermarkt ** ** Seite. Mehrere Zulieferer können in einem oder mehreren Produktionsflüssen modelliert werden, und es werden möglicherweise mehrere Kanban-Regeln, die verwendet werden können, die dem gleichen Produkt an denselben Lagerplatz durch unterschiedliche Aktivitäten zu liefern. Der kann Planer Kanbans zu eine alternative Kanban-Regel konvertieren, ein Kanban neu einzuplanen, der ursprünglich für interne Produktion mit einem alternativen Prozess erstellt wurde. Genau genommen hat die von Dienstleistungszeiten Art der Fertigungszelle keine Auswirkungen im Produktionsfluss. Dasselbe Funktionsprinzip gilt für parallele zwei Fertigungszellen interne oder zwei von Dienstleistungszeiten Zellen.   

Wie jede andere Aktivität in einem Produktionsfluss, können Fremdarbeitsaktivitäten verbrauchen und angeben inventarisiertes, nicht-inventarisiertes (Ressource in Fertigung) und RIF \[\]halb fertige nach Material und Produkte. In allen Argumenten werden die Prozesse für die Planung und die Ausführung von der geregelten Aktivitäten identisch. Darüber hinaus verarbeiten die denjenigen Prozesse für interne Arbeit.

## <a name="purchase-process-for-subcontracted-activities-services"></a>Einkaufprozess für Fremdarbeitsaktivitäten (Dienstleistungen )
Der Einkaufprozess für Fremdarbeitsaktivitäten basiert auf dem physischen Materialfluss, der durch Kanban-Einzelvorgangs-Fortschritt beispielsweise Start erfasst wird oder dem Lagerabschluss aus. Der Finanzstrom beispielsweise Kosten der von gesetzlichen Bestimmungen unterliegenden Arbeit ist, um einen sekundären, der Fluss der physischen Ablauf folgt. Gleichzeitig ist der Einkaufprozess ein unabhängiger Prozess, der manuelle Regulierung der Bestellungen bei jedem Schritt zulässt. Das hier der Einkaufprozess für Fremdarbeitsaktivitäten:

1.  Erstellen einer Rahmenbestellung. Die wird Rahmenbestellung für den Service erstellt und verbunden an die Aktivität des Produktionsflusses.
2.  Erstellen einer Bestellung. Eine Freigabenbestellung kann für den Dienst, auf der Grundlage der geplanten Kanban-Einzelvorgänge erstellt werden. Einzelvorgänge für den gleichen Service können Bestellpositionen nach Tag, Woche oder Monat gruppiert werden. Die Bestellpositionen können jederzeit erstellt werden, nachdem die Kanban-Einzelvorgänge erstellt wurden. Bestellpositionen können nach der Tatsache auch erstellt werden. Diese Option wird normalerweise ausgewählt, wenn ein Zulieferer Dienstleistungen zusätzliche Hinweis, ohne auf Grundlage die Kanbans oder die Kanban-Karten bereitstellt, die der Zulieferer erhält. In diesem Fall kann Abweichungen zwischen Bestellung und der Rechnung minimiert werden.
3.  Generieren von Kanban-Karten, Material sowie eine Kommissionierliste, um Zulieferer zu übermitteln, um sich für das Verarbeiten vorbereiten. Basierend auf detaillierte Modell- des Produktionsflusses, ist die Vorbereitung in der Kanban-Übersicht für Prozessaktivitäten ausgeführt, indem die Kommissionierliste und die Vorbereitungsfunktion verwendet. Alternativ ist die Vorbereitung in der Kanban-Übersicht für Umlagerungseinzelvorgänge ausgeführt, indem die Kommissionierliste und Start oder beim Abschluss verwendet. Für inventarisiertes Material können beide Prozesse durch einen WMS-Entnahme- Lieferprozess und unterstützt werden. Ein Frachtbrief kann bei Bedarf erstellt werden.
4.  Generieren Sie Kanbanhandhabungseinheiten und -Kanban-Karten. Nachdem von verarbeitet hat Karten werden vom Zulieferer zurückgegeben. Normalerweise schließt die Karten eines Lieferscheins ein, der angibt dem physischen Material, die geliefert wurde. Eine Referenz auf den erbrachten Dienstleistungen ist nicht erforderlich. Der Eingang des Materials und Fertigprodukten am Debitor wird in der Kanban-Übersicht, abhängig von Kanban-Karten erfasst. Entweder (die Kanban-Übersicht für Prozessaktivitäten oder die Kanban-Übersicht für Umlagerungseinzelvorgänge wird, hängt von den geformten Aktivitäten. verwendet).
5.  Erstellen Sie eine Zugangsempfehlung. Die Zugangsempfehlung kann verwendet werden, um ein Lieferscheindokuments für die eingegangenen Dienste zu ersetzen. Zugangsempfehlungen können basierend auf den abgeschlossenen für Kanban-Einzelvorgänge die Fremdarbeitsaktivität für einen ausgewählten Zeitraum generiert werden. Für jeden Einzelvorgangszugang werden verwandte Empfehlungen für die Bestellposition erstellt. Die Zugangsempfehlung kann z als Zulieferer Eingangsbestätigung gedruckt und gesendet werden.
6.  Generieren Sie eine Rechnung.

Der Prozess als fertig gemeldet, wenn für den Zulieferer in einer Periode fakturiert wird. Die Rechnungsabgleichung ist für die Zugangsempfehlungen ausgeführt, die erstellt werden. Da die Zugangsempfehlungen den genauen physischen Zugang des Materials darstellen, wird der dreiseitige Abgleich vereinfacht.

## <a name="configuring-activities-for-subcontracting"></a>Konfigurieren der Aktivitäten für das Nebenvertraglich regeln
In den folgenden Abschnitten wird, wie die Aktivitäten für das Nebenvertraglich regeln konfiguriert.

### <a name="subcontracted-services"></a>Nebenvertraglich mit Dienstleistungen

Der Zahlungsartikel, der in der aktivitätsbasierten Zulieferung verwendet wird, muss eines Produkts werden, das die folgenden Eigenschaften auf:

-   ** Produkttyp: ** Dienst
-   ** Lagersteuerungsgruppe: ** Nicht gelagert

Diese Anforderung erzwingt die Nutzung von First in, First out (FIFO)- Lagermodell. ** Hinweis: ** Kostenberechnung der Produkte erforderlich, dass die Standardkosten des Dienstes definiert werden. Eine Rahmenbestellung den Kreditor erforderlich. Andernfalls kann der Dienstleistung nicht für aktivitätsbasierte Zulieferung verwendet werden.

### <a name="subcontracted-process-activities"></a>Nebenvertraglich verschiedene Prozessaktivitäten

Um eine Verarbeitungsaktivität als Fremdarbeitsaktivität zu konfigurieren, die folgenden Schritte aus.

1.  Konfigurieren einer von Dienstleistungszeiten Fertigungszelle. Wählen Sie eine Fertigungszelle zu konfigurieren wie von gesetzlichen Bestimmungen, müssen Sie eine Ressource aus Kreditor erstellen ** ** eingeben und ihr zugeordnet (Fertigungszelle mit der Ressourcengruppe). Eine Ablaufkostenkategorie ** direktes Outsourcing ** Kostengruppentyp der Fertigungszelle zugewiesen werden soll. Die Kostenkategorien für Einrichtung und Menge sind nicht erforderlich.
2.  Nachdem eine Verarbeitungsaktivität einer von gesetzlichen Bestimmungen unterliegenden Fertigungszelle erstellt und zugeordnet ist, müssen Sie einen Service für die Aktivität konfigurieren, bevor die Produktionsflussversion aktiviert werden kann. Schließen Sie diesen Schritt für den ** Aktivität ** ** Details ab ** Seite. Bei Aktivitäten, die einer von gesetzlichen Bestimmungen unterliegenden Fertigungszelle zugeordnet sind, wird das Service-Bedingungen ** ** Inforegister angezeigt. Auf diesem Inforegister können Sie einen Standard-Service hinzu, der für alle Ausgabeartikel gültig ist. Wenn Besondereausgabeartikel verschiedene Dienstleistungen oder unterschiedliche Service-Berechnungsparameter (beispielsweise Gesamtlayout, ein anderes Service-Verhältnis) erforderlich ist, können Sie andere Dienstleistungen der Aktivität hinzufügen.

## <a name="subcontracted-transfer-activities"></a>Nebenvertraglich verschiedene Umlagerungsaktivitäten
Durch eine Umlagerungsaktivität wird als Fremdarbeitsaktivität, abhängig von den Einstellungen von ** befördert ** Umlagerungsaktivität der konfiguriert. Die folgenden Optionen sind verfügbar:

-   ** Verlader ** – Die Aktivität wird von gesetzlichen Bestimmungen, wenn der Übertrag der Von-Lagerort von einem Kreditor verwaltet wird (hierfür eine Eigenschaft des Lagerorts) definiert. Alle ausgewählten Rahmenbestellungen für Leistungen muss dieselbe Kreditor Kennung wie der Lagerort verfügen.
-   ** Empfänger ** – Die Aktivität wird von gesetzlichen Bestimmungen, wenn der Übertrag der An-Lagerort von einem Kreditor verwaltet wird (hierfür eine Eigenschaft des Lagerorts) definiert. Alle ausgewählten Rahmenbestellungen für Leistungen muss dieselbe Kreditor Kennung wie der Lagerort verfügen.
-   ** Spediteur ** – Die Aktivität ist für einen beliebigen Kreditor von gesetzlichen Bestimmungen, der den Service durchführt. Um gültig ist, muss ein Spediteur für Lagerortverwaltung erstellt werden und muss zugewiesenes Kreditorenkonto aufweisen.

Neuheiten Prozessaktivitäten, wird für Sie müssen einen Standard-Service für von Dienstleistungszeiten Umlagerungsaktivitäten auf dem Inforegister " Service-Bedingungen ** ** ** Aktivität ** ** Details konfigurieren ** Seite.

## <a name="service-quantity-calculation"></a>Servicemengenberechnung
Der Ganzeinkaufprozess basiert auf einer Artikelreferenz für einen Service. Diese Artikelreferenz wird in eine Maßeinheit eines Dienstes gemessen. Services werden üblicherweise entweder in Anzahl Dienstleistungen (Einheiten) oder in Zeit gemessen. Um die Service-Menge, basierend auf den erfassten Abschluss von Kanban-Einzelvorgängen zu berechnen, können die folgenden Methoden zur Verfügung:

-   ** Berechnung, die auf der Anzahl von Einzelvorgängen ** – ein Kanban-Einzelvorgang ist, entspricht *n* Einheiten Service, unabhängig davon, die die Fertigproduktmenge beschafft wird. Im Produktion entspricht ein Einzelvorgang einer Handhabungseinheit. Für diese Berechnungsmethode betrifft alle Services, die einen Festpreis pro Handhabungseinheit haben. Daher entspricht diese Methode normalerweise auf Umlagerungsaktivitäten zu. Allerdings kann außerdem gelten, Aktivitäten zu verarbeiten, die gesamte Handhabungseinheiten verarbeiten.
-   ** Berechnung, die auf Grundlage die Produktmenge ** – Die Service-Menge ist, ist relativ zu der Produktmenge, die geplant wird,/beschafft. Wenn die Produktmenge beschaffte berechnet wird, können Ausschussmengen entweder einbezogen oder nicht berücksichtigt werden. Für diese Berechnungsmethode gilt für alle Anfragen zu, in denen der Service-Preis pro Einheit des verarbeiteten Produkts ausgeglichen wird.
-   ** Berechnung, die auf der die Aktivitätszeit ** ist - die theoretischen Aktivitätszeiten werden, basierend die Laufzeit der Aktivität, verarbeiteten Summe der Menge und des Durchsatz-Verhältnisses des verarbeiteten Produkts berechnet. Für diese Berechnungsmethode gilt für Dienste, die bezahlt stundenweise und Abweichungen in Zeit pro verarbeitetes Produkt zu werden.

## <a name="cost-accounting-of-subcontracted-services"></a>Kostenrechnung der geregelten von Services
Wenn die Zugangsempfehlung oder ein Lieferschein des Kreditors auf eine Bestellung, die für einen Produktionsfluss erstellt wurde (das heißt, eine Bestellung, die anhand Kanban-Einzelvorgänge für Fremdarbeitsaktivitäten generiert wurde), gebucht wird, wird der Wert des Bons auf WIP-Konten des Produktionsflusses berechnet. Abweichungen von Rechnungen werden auch dem Produktionsfluss berechnet. Eine Kostenkategorie für ist Fremdarbeit eingegeben. Diese Kostenkategorien aktivieren transparente Nachverfolgung des Werts der von gesetzlichen Bestimmungen unterliegenden Arbeit, die in " RIF zugewiesen und pro Periode verbraucht.  

Die Nachkalkulation für Produktionskosten für Produktion am Ende einer Nachkalkulationsperiode berechnet die eigentlichen Abweichungen der Produkte, die dem Produktionsfluss während der Nachkalkulationsperiode produziert werden.

## <a name="modeling-transfers-as-subcontracted-activities"></a>Modellvariablen der Überträge als Fremdarbeitsaktivitäten
Person berücksichtigt häufig als unproduktiv Transport und denkt, dass er keinen Wert unter. Wenn die Kosten der Zulieferung zu den Kosten der internen Produktion verglichen werden, müssen die Kosten der zusätzlichen Transporttätigkeit berücksichtigt werden. Ein Produktionsfluss, der mehrere Lagerplätze umfasst und Transportdienste erforderlich, muss der Transportkosten als Teil der Kosten zur Festlegung der Produkte an den Debitor entwerfen. 

Aktivitätsbasierte Zulieferung in Produktion können Sie Spediteure Integration von und Datentransportkreditoren, der Material und Produkten zwischen die Lagerplätze eines Produktionsflusses verschieben. Durch eine Umlagerungsaktivität Sie modellieren, können Sie einen Spediteur oder Kreditor zuweisen. Die Stelle Umlagerungsaktivitäten/basiert auf einem Service und eine Rahmenbestellung, und Sie können Bestellungen und Zugangsempfehlungen, auf Basis der tatsächlichen Umlagerungseinzelvorgänge erstellen. Diese Funktionen sind identisch, die den Funktionsumfang für von Dienstleistungszeiten Prozessaktivitäten.  

Daher unterstützt Dynamics 365 nun Herstellkostenkalkulation für Arbeitsgänge, die Transportdienste, die Erstellung von Bestellungen Zugangserfassung integrierte zugehörigen, und die Datentransportdienstleistungskosten Integration von in die Produktionsflussnachkalkulation enthält.


