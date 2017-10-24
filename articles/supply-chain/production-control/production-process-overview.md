---
title: "Überblick über den Produktionsprozess"
description: "Dieser Artikel enthält eine Übersicht des Produktionsprozesse. Er beschreibt die verschiedenen Produktionsaufträge, Chargenaufträgen und Kanbans, von der Auftragserstellung bis zum Schließen der Finanzperiode."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgProdStatusListPage, JmgShopSupervisorWorkspace, Kanban, ProdTable, ProdTableOverview
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19832
ms.assetid: 0e83c7ea-feba-4ed6-8717-8b48a3b8804a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e50e64057d19d0e1fbf5645c2abc31fbd19ea43a
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="production-process-overview"></a>Überblick über den Produktionsprozess

[!include[banner](../includes/banner.md)]


Dieser Artikel enthält eine Übersicht des Produktionsprozesse. Er beschreibt die verschiedenen Produktionsaufträge, Chargenaufträgen und Kanbans, von der Auftragserstellung bis zum Schließen der Finanzperiode. 

Die Produktion von Produkten, ein Prozess, der auch als Produktionslebenszyklus bezeichnet wird, folgt bestimmten Schritten, die erforderlich sind, um die Herstellung eines Artikels abzuschließen. Der Lebenszyklus beginnt mit der Erstellung des Produktionsauftrags, des Chargenauftrags oder des Kanbans. Dies endet mit dem fertigen, hergestellten Artikel, der entweder für einen Kunden oder eine weitere Produktionsphase bereit ist. Für jeden Schritt des Lebenszyklus sind bestimmte Arten von Informationen erforderlich, damit der entsprechende Vorgang abgeschlossen werden kann. Mit dem Abschluss jedes Schritts wird im Produktionsauftrag, im Chargenauftrag oder Kanban eine Änderung im Produktionsstatus angezeigt. Unterschiedliche Arten von Produkten erfordern verschiedene Fertigungsprozesse.  

Das Modul **Produktionssteuerung** wird mit anderen Modulen, wie **Produktinformationsverwaltung**, **Lagerverwaltung**, **Hauptbuch**, **Lagerortverwaltung**, **Projektverrechnung** und **Organisationsverwaltung** verknüpft. Diese Integration ermöglicht die reibungslose Weiterleitung von Informationen, die zum Fertigstellen der Artikelfertigung erforderlich sind.  

Der Produktionsprozess wird in der Regel von den Kostenrechnungs- und Lagerbewertungsmethoden beeinflusst, die für einen bestimmten Produktionsprozess ausgewählt werden. Finance and Operations unterstützt sowohl die Methode für tatsächliche Kosten (First in, First out \[FIFO\]; Last in, First out \[LIFO\]; sich verschiebender Durchschnitt; sowie periodisch gewichteter Durchschnitt) als auch die Methode für Standardkosten. Lean Manufacturing wird auf der Grundlage des Prinzips der Nachkalkulation für Produktionskosten implementiert.  

Die Auswahl der Kostenmessungsmethoden definiert auch die Anforderungen für die Berichterstellung zum Material- und Ressourcenverbrauch während des Produktionsprozesses. Normalerweise erfordern Methoden zu tatsächlichen Kosten eine genaue Berichterstellung auf Einzelvorgangsebene. Periodische Nachkalkulationsmethoden lassen hingegen eine weniger präzise Berichterstellung zum Material- und Ressourcenverbrauch zu.

## <a name="mixed-mode-manufacturing"></a>Fertigung im Mischbetrieb
Verschiedene Produkte und Produktionstopologien erfordern die Anwendung von unterschiedlichen Auftragstypen. Finance and Operations kann die verschiedenen Auftragstypen in einem gemischten Modus übernehmen. In anderen Worten können alle anderen Auftragstypen während des Ende-zu-Ende-Prozesses der Herstellung eines fertigen Produkts auftreten.

-   **Produktionsauftrag** – Dies ist der klassische Auftragstyp, um ein bestimmtes Produkt oder Produktvariante in einer bestimmten Menge an einem bestimmten Datum zu produzieren. Produktionsaufträge basieren auf Stücklisten und Arbeitsplänen.
-   **Chargenauftrag** – Dieser Auftragstyp wird für verarbeitende Industrien und diskrete Prozesse verwendet, bei denen die Herstellungsumwandlung auf einer Formel basiert, oder wobei die Co-Produkte und Nebenprodukte Endprodukte sein können, entweder zusätzlich zum oder statt des Hauptprodukts. Chargenauftrage verwenden Stücklisten und Arbeitspläne vom Typ **Formel**.
-   **Kanban** – Kanbans werden verwendet, um wiederkehrenden Lean Manufacturing-Prozesse zu signalisieren, die auf Produktionsflüssen, Kanban-Regeln und Stücklisten basieren.
-   **Projekt** – Ein Fertigungsprojekt kombiniert Produkte und Dienstleistungen mit einem vorgegebenen Zeitplan und Budget. Der Herstellungsteil eines Projekts kann durch irgendeinen der anderen Auftragstypen geliefert werden.

## <a name="manufacturing-principles"></a>Fertigungsprinzipien
Um das Fertigungsprinzip auszuwählen, das am besten zu einem bestimmten Produkt und dem dazugehörigen Markt passt, müssen Sie die Anforderungen der Produktion und Logistik berücksichtigen sowie Kundenerwartungen zu Liefervorlaufzeiten.

-   **Auf Lager fertigen** – Dies ist das klassische Fertigungsprinzip, bei dem Produkte für den Lagerbestand produziert werden, auf Grundlage von Prognosen oder einer Mindest-Lagerauffüllmenge (letztere wird normalerweise auf Grundlage einer Prognose oder dem Verbrauch in der Vergangenheit berechnet).
-   **Auf Auftrag fertigen** – Standardprodukte werden auf Auftrag hergestellt werden oder fertiggestellt. Obwohl die Vorproduktion möglicherweise mithilfe des Prinzips "Auf Lager fertigen" erfolgt, werden teure Schritte der Wertschöpfungskette oder Schritte, bei denen Varianten erstellt werden, durch einen Auftrag oder einen Umlagerungsauftrag ausgelöst.
-   **Auf Auftrag konfigurieren** – Wie beim Prinzip "Auf Auftrag fertigen", werden die abschließenden Arbeitsgänge der Wertschöpfungskette auf Auftrag ausgeführt. Die tatsächliche Produktvariante, die produziert wird, ist nicht vordefiniert, sondern wird zum Zeitpunkt der Auftragserfassung erstellt, basierend auf dem Konfigurationsmodell des Verkaufsprodukts. Das Prinzip "Auf Auftrag konfigurieren" erfordert ein bestimmtes Maß der Prozessvereinheitlichung für eine bestimmte Produktposition.
-   **Auf Auftrag entwickeln** – Prozesse mit Entwicklung auf Auftrag werden normalerweise von einem Projekt angesprochen und beginnen gewöhnlich mit der Entwicklungsphase. Während der Entwicklungsphase werden die tatsächlichen Produkte, die zur Erfüllung des Auftrags erforderlich sind, entworfen und beschrieben. Produktionsaufträge, Chargenaufträge oder Kanbans können dann erstellt werden, um die Produkte herzustellen.

## <a name="overview-of-the-production-life-cycle"></a>Übersicht über den Produktionslebenszyklus
Die folgenden Schritte im Produktionslebenszyklus können bei allen Auftragstypen mit einer Herstellung im Mischbetrieb erfolgen. Allerdings werden nicht alle von ihnen als expliziter Auftragsstatus dargestellt.

1.  **Erstellt** – Sie können einen Produktionsauftrag, einen Chargenauftrag oder Kanban manuell erstellen, oder Sie können das System so konfigurieren, dass sie auf der Grundlage verschiedener Bedarfssignale generiert werden. Durch den Produktprogrammplan werden Produktionsaufträge, Chargenaufträge oder Kanbans erstellt, indem geplante Aufträge umgewandelt werden. Andere Bedarfssignale sind Aufträge oder Signale für Lieferung mit Bedarfsverursachung aus anderen Produktionsaufträgen oder Kanbans. Für Kanbans für feste Menge werden Bedarfssignale generiert, wenn Kanbans als leer erfasst werden.
2.  **Vorkalkuliert** – Sie können Vorkalkulationen für den Material- und Ressourcenverbrauch vornehmen. Die Vorkalkulation generiert Lagerbuchungen für Rohmaterialen, die den Status **In Auftrag** besitzen. Die Zugänge, für Hauptprodukte Kuppel- und Nebenprodukte werden generiert, wenn Produktionsaufträge vorkalkuliert oder Chargenaufträge werden. Wenn die Stückliste umfasst, geben Positionen des Typs **Lieferung mit Bedarfsverursachung** Bestellungen für Materialien oder von Dienstleistungszeiten Arbeitsgangsdienstleistungen Den werden generiert und dem Produktionsauftrag oder dem Chargenauftrag ein. Artikel oder Aufträge werden entsprechend der Reservierungsstrategie des Produktionsauftrags reserviert, und der Preis der Fertigartikel wird auf Grundlage der Parametereinstellungen berechnet.
3.  **Geplant** – Sie können die Produktion auf Grundlage von Arbeitsgängen, bestimmten Einzelvorgängen oder beidem planen.
    -   **Grobterminierung** – Diese Planungsmethode dient zum Erstellen eines groben, langfristig ausgelegten Plans. Mithilfe dieser Methode können Produktionsaufträge mit einem Start- und Enddatum versehen werden. Produktionsaufträge, die Arbeitsplanarbeitsgängen zugeordnet sind, können auch Ressourcengruppen zugeordnet werden.
    -   **Feinterminierung** – Diese Planungsmethode dient zum Erstellen eines detaillierten Plans. Jeder Arbeitsgang wird in individuelle Einzelvorgänge mit bestimmten Daten, Uhrzeiten und zugewiesenen betrieblichen Ressourcen aufgeteilt. Bei Verwendung begrenzter Kapazitäten erfolgt die Zuordnung der Einzelvorgänge zu betrieblichen Ressourcen nach Verfügbarkeit. Änderungen am Plan können in einem Gantt-Diagramm vorgenommen werden.
    -   **Kanban-Zeitplan** – Kanban-Einzelvorgänge werden auf der Kanban-Zeitplanübersicht geplant oder automatisch auf Grundlage der automatischen Planungskonfiguration der Kanban-Regeln geplant.

4.  **Freigegeben** – Sie können den Produktionsauftrag oder Chargenauftrag freigeben, wenn die Planung beendet wird und das Material verfügbar ist, um entnommen oder vorbereitet zu werden. Die Materialverfügbarkeitsprüfung unterstützt den Fertigungsbereichsvorgesetzten dabei, die Verfügbarkeit von Material für Produktionsaufträge oder Chargenaufträge zu bewerten. Darüber hinaus können die Dokumente für den Produktionsauftrag, wie die Auswahllisten, Einzelvorgangsliste, Arbeitsplanliste oder Arbeitsplan-Einzelvorgang, gedruckt werden. Nach Freigabe des Produktionsauftrags wird der Status des Auftrags geändert, sodass ersichtlich ist, dass mit der Produktion begonnen werden kann. Wenn die Lagerortverwaltung verwendet wird, werden durch die Freigabe des Produktionsauftrags oder Chargenauftrags die Produktionsstücklisten-Positionen für die Lagerortverwaltung freigegeben. Lagerortwellen und Lagerortarbeit werden dann entsprechend der Einstellungen des Lagerorts generiert.
5.  **Vorbereitet**/**Entnommen** – Wenn alle Materialien und Ressourcen am Produktionslagerplatz bereitgestellt wurden, werden die Produktionsstücklisten-Positionen oder die Kanban-Positionen auf den Status **Entnommen** aktualisiert. Aufträge mit Lieferung mit Bedarfsverursachung und zugehörige Lagerortarbeit werden normalerweise in dieser Phase abgeschlossen. Die Kanban-Karten oder Einzelvorgangslisten, die erforderlich sind, um den Produktionsfortschritt zu melden, sollten zugewiesen und gedruckt werden.
6.  **Gestartet** – Wenn ein Produktionsauftrag, ein Chargenauftrag oder ein Kanban gestartet wird, können Sie Material- und Ressourcenverbrauch für den Auftrag melden. Das System kann so konfiguriert werden, dass Material- und Ressourcenverbrauch, die dem Auftrag zugewiesen sind, automatisch gebucht werden, wenn der Auftrag gestartet wird. Diese Zuteilung wird als Preflushing oder vorwärts gerichteter Verbrauch oder Selbstverbrauch bezeichnet. Sie können Materialien manuell Produktionsaufträgen oder Chargenaufträgen zuweisen, indem Sie zusätzliche Kommissionierlistenerfassungen erstellen. Sie können auch Arbeitskosten und andere Arbeitsplankosten dem Auftrag manuell zuweisen. Wenn die Grobterminierung verwendet wird, können Sie diese Kosten zuweisen, indem Sie eine Arbeitsplanlistenerfassung erstellen. Wenn die Feinterminierung verwendet wird, können Sie die Kosten zuweisen, indem Sie eine Einzelvorgangsliste erstellen. Produktionsaufträge oder Chargenaufträge können in Chargen der angeforderten endgültigen Menge gestartet werden. Innerhalb eines Produktionsauftrags, eines Chargenauftrags oder eines Kanbans können die Einzelvorgänge, die erstellt werden, über Erfassungen, das Fertigungssteuerungsterminal (MES-Terminal) oder die Kanban-Übersichten separat gestartet und gemeldet werden.
7.  Fortschritt melden/**Abschließen** von Einzelvorgängen – Verwenden Sie das MES-Terminal, Produktionserfassungen, Kanban-Übersichten oder mobile Scanfunktionen, um den Produktionsfortschritt nach Einzelvorgang und Ressource zu melden. Material- und Ressourcenverbrauch werden gebucht und der Status der zugehörigen Kanbans, der Produktionsaufträge und der Chargenaufträge werden möglicherweise auf **Eingegangen** oder **Als fertig gemeldet** aktualisiert. Einlagerungsarbeit für den Lagerort kann, abhängig von der Lagerortkonfiguration, erstellt werden.
8.  **Als fertig gemeldet** (der Produktzugang) – Wenn ein Produktionsauftrag oder ein Chargenauftrag als fertig gemeldet wird, wird die Menge der fertigen Güter, die fertig gestellt wurden, im Lagerbestand aktualisiert. Diese Menge umfasst die Menge relevanter Co-Produkte und Nebenprodukte. Bei Verwendung der "Ressource in Fertigung"-(RIF)-Buchführung, wird eine Sachkontenerfassung generiert, um die RIF-Konten zu verringern und den Bestand der fertigen Waren zu erhöhen. Wenn die Kosten eines Produktionsauftrags berechnet werden, werden die tatsächlichen Kosten der Produktion gebucht. Wenn die Material- und Arbeitskosten, die der Produktion zugeordnet sind, nicht bereits in einer Erfassung oder durch automatischen Preflushing (Vorverbrauch) zugewiesen wurden, können sie per Rückfluss automatisch zugewiesen werden. Zuteilung durch Rückfluss beinhaltet den nachträglichen Abzug von Lagerbuchungsprozessen. Wenn der Produktionsauftrag abgeschlossen ist, aktivieren Sie das Kontrollkästchen **Abschluss-Einzelvorgang**, um den verbleibenden Status zu **Abgeschlossen** zu ändern. Andernfalls lassen Sie das Feld leer, um die Berichterstellung über zusätzlich produzierte Mengen zu aktivieren.
9.  **Qualitätsbewertung** – Ein Produktzugang kann das Erstellen von Testbestellungen auslösen, abhängig von der Konfiguration der Testverfahren und der Qualitätsregeln, die für bestimmte Produkte eingerichtet sind. Da durch eine Testbestellung der Bestandsstatus oder die Stapelverarbeitungsattribute der getesteten Produkte aktualisiert werden können, ist die Qualitätsbewertung ein obligatorischer Prozess in vielen Branchen.
10. **Einlagern** und **Auf Auftrag liefern** – Nach dem Produktzugang und der Qualitätsbewertung leitet die Einlagerungsarbeit die empfangenen Produkte an den nächsten Punkt des Verbrauchs weiter, einem Lagerort für Fertigwaren oder einer Lieferungszone, wenn es Anforderungen fürs Liefern auf Auftrag gibt.
11. **Abgeschlossen** – Vor dem Beenden der Produktion werden die tatsächlichen Kosten für die produzierte Menge berechnet. Alle vorkalkulierten Material-, Arbeits- und Gemeinkosten werden storniert und durch die Istkosten ersetzt. Wenn Sie beim ausführen der Kostenberechnung das Kontrollkästchen **Abschluss-Einzelvorgang** auswählen, ändert sich der Produktionsauftragsstatus zu **Abgeschlossen**. Mit diesem Status wird sichergestellt, dass für einen abgeschlossenen Produktionsauftrag keine weiteren Kosten mehr gebucht werden können.
12. **Periodenabschluss** – Einige Kostenrechnungsprinzipien, wie regelmäßiger Durchschnitt, Nachkalkulation mit rückwärtiger Leerung, FIFO oder LIFO, erfordern, dass Periodenaktivitäten den Bestand oder die Finanzperiode abschließen. In der Regel versucht das System, den gesamten Material- und Ressourcenverbrauch zu melden sowie auch Korrekturen bei Bestand und Ausschuss, bevor die Periode abgeschlossen wird. Diese Berichterstellung erfolgt normalerweise mithilfe von Lagerumlagerungserfassungen oder Regulierungserfassungen. Die Zielsetzung besteht darin, die wirtschaftliche Leistung von Organisationseinheiten pro Periode zu bewerten. In einigen Fällen, wenn Produktionsaufträge mit langer Laufzeit verwendet werden, die sich über die Finanzberichterstellungsperioden erstrecken, werden Produktionserfassungen verwendet, um den Produktionsfortschritt und den Ressourcenverbrauch am Ende der Periode zu melden.


<a name="see-also"></a>Siehe auch
--------

[Produktionsrückmeldung](production-feedback.md)

[Produktkonfigurationsmodelle](../pim/product-configuration-models.md)

[Lean Manufacturing](lean-manufacturing-overview.md)




