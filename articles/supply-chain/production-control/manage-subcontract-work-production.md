---
title: Verwalten Sie Lohnarbeit in der Produktion
description: In diesem Thema wird erläutert, wie Fremdarbeitsdienste in Dynamics 365 Supply Chain Management verwaltet werden. Das bedeutet, wird dies, wie Produktions-Einzelvorgänge, die einer Ressource zugewiesen, von einem Kreditor verwaltet werden.
author: johanhoffmann
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeanDocumentServiceCreation, PlanActivity, ProdBOMVendorListPage, ProdRoute, ProdTable, ProdTableListPage, PurchAgreementSubcontractorLookup, RouteTable, WrkCtrResourceGroup, ProdBOMVendorListPagePreviewPane, ProdBOMVendor
audience: Application User
ms.reviewer: kamaybac
ms.custom: 268174
ms.assetid: fe47c498-4f48-42a2-a0cf-5436c19ab3ea
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e80efc751ccf9243163d23ed48fd17923326f89
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579378"
---
# <a name="manage-subcontracting-work-in-production"></a>Verwalten Sie Lohnarbeit in der Produktion

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Fremdarbeitsdienste in Dynamics 365 Supply Chain Management verwaltet werden. Das bedeutet, wird dies, wie Produktions-Einzelvorgänge, die einer Ressource zugewiesen, von einem Kreditor verwaltet werden.

In [Produktionsprozesse](production-process-overview.md) kann Arbeit nach Ressourcen ausgeführt werden, die von den Kreditoren zugeordnet oder verwaltet werden. Normalerweise werden Kreditorenbetriebsmittel der Ebene der periodischen Übernachfrage verwendet, die die verfügbare Kapazität der eigenen Ressourcen eines Unternehmens hinausreicht. Der Kreditor kann z auch in der Lage, Angaben [Ressourcenfunktionen](resource-capabilities.md) oder Ressourcen mit einem geringeren Preis anzubieten.  

Abhängig von den Kreditorenbetriebsmitteln, die in einen Produktionsprozess verwendet werden, kann ein [Arbeitsplan](routes-operations.md) häufig zusätzliche logistische Anforderungen, da das Material und die Halbfertigprodukte dem Standort des Kreditors zuerst transportiert werden müssen. Anschließend muss dem Ergebnis der von gesetzlichen Bestimmungen unterliegenden Arbeitsgangs transportiert werden entweder auf, der zum nächsten Arbeitsgang oder einem Endproduktelagerort zugewiesen wird.  

Wenn Sie Arbeitsgänge oder Aktivitäten von unterliegt, sind jedoch betreffen alle Phasen der Arbeitsgänge, von der Definition der Arbeitsgänge, die in der Produktion, für die Nachkalkulation, in der Planung, bei der Kapazitätsplanung und im Planen, zur Verwaltung von Logistik für Materialien, Halbfertigprodukte erforderlich sind, und Erstellen der verwendet. Schließlich erfordern diese Ressourcen eigene Prozesse für die Berechnung und Kostenkontrolle.  

Bei internen Ressourcen wird ein Fixkostensatz normalerweise für eine Periode aufgeteilt. Durch Kontrast sind die Kosten der geregelten von Ressourcen auf dem Einkaufspreis des zugehörigen Service. Der als Service wird ein weiteres Produkt definiert und wird verwendet, um die Einkaufprozesse Beschaffungs- und für einen angegebenen Artikel von Arbeitsgang zu treiben.  

Derzeit gibt es kein explizites Konzept für Halbfertigprodukte in Supply Chain Management. Für einen Produktionsauftrag, der mehr als einen Arbeitsgang erforderlich, um Rohmaterial in ein Fertigprodukt umzuwandeln, wird das Endprodukt wieder dem Lager nur im letzten Arbeitsgang gebucht. Die, die Halbfertigprodukte das vorherige Arbeitsgangserzeugnis im in Fertigung (WIP) verwendet werden, doch sie werden nicht im Bestand gebucht oder nachverfolgt. Obgleich die Arbeitspläne und die Stücklisten (BOMs) in mehrere kleinere Einheiten, in Erhöhungen dieses Ansatzes Anzahl von Produkten, die in Stücklisten und Arbeitsplänen in aufteilbare, die verwaltet werden müssen.  

Es gibt zwei Methoden der Modellierung von Lohnarbeit für Produktionsarbeitsgänge. Methoden Diese unterscheiden sich auf die Methode, mit der der Fremdarbeitsprozess modelliert werden kann, die Halbfertigprodukte, wie die im Prozess angezeigt werden, und die Art, dass Kostenkontrolle verwaltet wird.

-   Zulieferung von Arbeitsplan-Arbeitsgängen in Produktionsaufträgen oder in den Chargenaufträgen
    -   Das Service-Produkt muss ein gelagertes Produkt werden, und es muss Teil der Stückliste sein.
    -   Diese Methode unterstützt, First out (FIFO) oder Standardkosten.
    -   Halbfertigprodukte werden im Service-Produkt im Prozess angezeigt.
    -   Kostenkontrolle weist die Kosten an, die mit von geregelter Arbeit den Materialkosten zugeordnet sind.
-   Zulieferung der Produktionsflussaktivitäten in einem der Fluss Produktion basiert
    -   Der ist ein Dienst nicht-gelagertes Service-Produkt, und nicht Teil der Stückliste.
    -   Diese Methode verwendet Rahmenbestellungen als Servicevereinbarungen.
    -   Diese Methode verwendet Nachkalkulation für Produktionskosten.
    -   Diese Methode ermöglicht aggregierte und asynchrone Beschaffung zu. (Materialfluss ist unabhängig von der Beschaffungsprozesses.)
    -   Kostenkontrolle weist Fremdarbeit im eigenen Kostenaufschlüsselungsblock zu.

## <a name="subcontracting-of-route-operations"></a>Zulieferung von Arbeitsplan-Arbeitsgängen
Um Zulieferung von Arbeitsplan-Arbeitsgängen für Produktions- und Chargenaufträge verwendet werden können, muss das Service-Produkt das für die Beschaffung des Service verwendet wird als Produkt vom Typ **Service** definiert werden. Außerdem muss es eine Artikelmodellgruppe besitzen, die die **Gelagertes Produkt** Option der Gruppe **Bestandsrichtlinie** **Ja** hat. Mit dieser Option wird definiert, ob ein Produkt als Bestand auf Produktzugangs berechnet wird (**Gelagertes Produkt** = **Ja**) oder ob das Produkt in Gewinn- und Verlustkonto (**Gelagertes Produkt** = **Nein**). Obwohl dieses Verhalten kann widersprüchlich schiene, verfügt diese auf Basis der Tatsache, dass nur Produkte, die dieser Richtlinie haben, erstellen, die Lagerbuchungen in der Kostensteuerung verwendet werden können, um geplante Kosten zu berechnen und den Istkosten ermittelt, wenn ein Produktionsauftrag abgeschlossen ist.  

Weitere hinzugefügt werden bei der Kapazitätsplanung und der Kostenkalkulation berücksichtigt zu werden, muss der Dienstleistung in der Stückliste. Die der Stücklistenposition muss vom Typ **Kreditor** sein, und es muss dem Arbeitsplan-Arbeitsgang zugeordnet sind, der der Service zugewiesen ist. Dieser muss eine Arbeitsplan-Arbeitsgang Nachkalkulationsressource haben und Ressourcenanforderung, die für eine Ressource des Typs **Kreditor** sein, das den und den zugehörigen Arbeitsgang der Dienstleistung an das entsprechende Kreditorenkonto herstellt.  

Wenn diese Konfiguration verwendet wird, wird einer Bestellung für das zugehörige Service-Produkt, basierend Vorkalkulation eines Produktionsauftrags erstellt. Die Bestellung der Dienstleistung wird als Anker die für von gesetzlichen Bestimmungen unterliegenden Arbeitsgänge verwendet. Die Fremdarbeit kann durch die **Fremdarbeit** Listenseite in der Produktionssteuerung verwaltet werden. Die Fremdarbeit wird verwendet, wenn ein Rohmaterial und schließlich Halbfertigprodukt dem Kreditor in der Pipelinespezifikation auf den Arbeitsgang zu versenden. Sie wird auch verwendet, um die sich ergebende Produkt des geregelten von Arbeitsgangs im Wareneingang zu erhalten, in dem das Service-Produkt verwendet wird, um den Eingang des Halbzeugs zu identifizieren. Wenn die Bestellposition ein, wird der Produktionsarbeitsgang aktualisiert, die als abgeschlossen.  

Ein Produktionsauftrag kann zahlreiche Arbeitsgänge haben, und jeder Arbeitsgang kann zu einem anderen Lieferanten zugewiesen werden. Daher kann ausgelöst hat ein aufeinander folgender Produktionsauftrag mehrere Bestellungen.

## <a name="subcontracting-of-production-flow-activities"></a>Zulieferung der Produktionsflussaktivitäten
Die [Lean Manufacturing](lean-manufacturing-overview.md)-Lösungsmodelle wird die Fremdarbeit als Dienst modelliert, der mit einer Aktivität eines [Produktionsflusses](tasks/create-production-flow-version.md) (Aufgabeleitfaden) verknüpft ist. Daher wird dieser Typ Zulieferung der auch als [aktivitätsbasierte Fremdarbeit](activity-based-subcontracting.md). Ein spezieller Kostengruppentyp mit der Bezeichnung **Direktes Outsourcing** wurde eingeführt und die Fremdarbeitsdienstleistungen sind nicht mehr Teil einer Stückliste (BOM). Wenn Sie Produktion verwenden, werden alle nach Kanbans Aktivitäten definiert, die in einem oder mehreren zu Produktionsflussaktivitäten zugeordnet werden können. Bis hierher klingt diese Erklärung wie die zu Produktionsaufträgen. Allerdings für Produktionsaufträge mit einem Produkt, müssen immer beenden können Sie Kanbans erstellen, um ein Halbfertigprodukt zu liefern. Sie müssen ein neues Produkt und einer Stücklistenebene nicht vorstellen.  

Da Kanban-Regeln sehr dynamisch werden können, können diesem verschiedene Varianten der Lieferung für dasselbe Produkt in einem Produktionsfluss modellieren. Wenn Sie schlanke Zulieferung verwenden, werden der Materialfluss und der Finanzstrom ausschließlich getrennt. Der gesamte Materialfluss wird durch Kanbanaktivitäten dargestellt. Die Bestellungen für die Service-Produkte und Zugangsbuchung für diese Leistungen können, auf dem Status von Kanban-Einzelvorgängen im Produktionsfluss automatisiert werden. Kanban-Einzelvorgänge können gestartet und abgeschlossen werden, auch vor die Bestellungen erstellt werden. Die Fremdarbeitsdokumente (Bestellung und Empfang von Bestellungen des Service) können von der Periode und des Diensts zusammengefasst werden. Daher kann die Anzahl von Einkaufsbelegen und Positionen, die auch in ausdrücklich wiederholenden Arbeitsgängen klein aufbewahrt werden, in denen Kreditoren von Dienstleistungszeiten Dienstleistungen in einem Einzelstückfluss erbringen.

### <a name="modeling-subcontracting-in-a-production-flow"></a>Modellierungsfremdarbeit in einem Produktionsfluss

In einem [Lean-Produktionsfluss](lean-manufacturing-modeling-lean-organization.md) kann eine Verarbeitungsaktivität definiert werden, wie von geregelt wurde, die einer Fertigungszelle (Ressourcengruppe) zugewiesen hat die einzelne eine Kreditorenressource hat. Wenn eine Fertigungszelle von bestimmten Regularien, müssen die zugehörige Prozessaktivitäten zu einer aktiven Rahmenbestellungsposition verknüpft werden, die das Dienstleistungsartikel und Preis des Service angegeben werden. Die Servicevereinbarung der Aktivität definiert auch das Berechnungs-Verhältnis zwischen der Produktmenge des Kanban-Einzelvorgangs und die sich ergebenden Service-Menge. Sie können auswählen, ob die Service-Menge auf der Anzahl von Einzelvorgängen, guter Produktmenge, die in diesen Einzelvorgängen gemeldet ist, oder von vollständigen Produktmenge berechnet wird (diese Gesamtmenge enthält ausrangierte Produkte).  

Umlagerungsaktivitäten können auch festgelegt werden, z von reguliert wurde. Die Definition erfolgt implizit auf, wenn Sie die zuständige Partei für den Versand Umlagerungsaktivität im Formular auswählen. Wenn Sie **Verlader** oder **Empfänger** wenn der entsprechende Quell- Ziellagerort oder ein Kreditor-verwalteter Lagerort ist, die von gesetzlichen Bestimmungen gelten als Aktivität auswählen. Wenn Sie auswählen **Spediteur** wird die Aktivität immer von reguliert. Gleiche von Dienstleistungszeiten Prozessaktivitäten, einer von Dienstleistungszeiten Umlagerungsaktivität müssen mit einem Servicevertrag herstellen, vor der Verwendung aktiviert werden kann.

### <a name="backflush-costing"></a>Nachkalkulation für Produktionskosten

Die Kostenbuchhaltung der Fremdarbeit wird vollständig in die Kostenlösung für Lean Manufacturing integriert. Wenn der Bestellungseingang des Service gebucht ist oder die Rechnungsstellung übereinstimmen, werden die Kosten des Service dem Produktionsfluss zugewiesen. Die Nachkalkulation für Produktionskosten wird die Abweichung von Dienstleistungen geregelten berechnet, indem die Fremdarbeitsblock der Standardkosten der empfangenen Produkte anhand die tatsächlich eingegangen und fakturierten ausgleicht Leistungsmengen.

## <a name="material-supply-for-subcontracted-operations"></a>Materialbereitstellung für Arbeitsgänge von Dienstleistungszeiten
Halbfertigprodukte und zugehöriger Materialien müssen dem Ort übertragen werden, in der die Arbeit tatsächlich ausgeführt wird. Wenn Sie von Dienstleistungszeiten Arbeitsgänge und Aktivitäten verwendet, wird diese Übertragung erfolgen häufig zur weiteren Transport zu einem Kreditor-Betriebsstandort zugeordnet. Durch Festlegen Material in der Stückliste von dem geregelten Arbeitsgang zuweisen, melden Sie, dass das Material am Lagerplatz für den Wareneingang der Ressourcengruppe für die zugewiesene Ressource angegeben werden muss. Produktprogrammplanungs- oder Lean-Wiederbeschaffung stellt dann das Material an diesen Lagerplatz bereit.  

Um den Bestand zu modellieren der an einem Kreditorenstandort befindet, ist es eine Verfahren in der Industrie einen Kreditor-verwalteten Lagerort definieren. Sie können einen Lagerort Kreditor-verwalteten leicht festlegen, indem Sie einen neuen Lagerort erstellen und das Kreditorenkonto zuweisen. Zum Dokument, dass Material zum Kreditor übertragen werden muss, bevor ein Arbeitsgang ausgeführt werden, können Sie ggf. den Kreditor-verwalteten Lagerort zum Eingangslagerort der Ressourcengruppe zuordnen, die die Ressource an.  

Wenn Material an diesem Lagerort zu ergänzen, können Sie mehrere Strategien verwenden:

-   Umlagerungsaufträge
-   Umlagerungserfassungen
-   Entnahme-Kanban
-   Direkter Kauf dem Standort des Kreditors

Halbfertigprodukte sind die Ausnahme von dieser Regel. Um Halbfertigprodukte zu übertragen, werden Sie zu diesen Optionen beschränkt:

-   Beim Produktionserfassungstyp und Chargenaufträge Halbfertigprodukte logisch können nur übertragen werden, indem Sie die Kommissionierlistenerfassung aus der **Fremdarbeit** Listenseite verwendet. Diese Erfassung erstellt Lieferscheindokuments ein, das verwendet werden kann, um fertig halb fertige Rohmaterial und an den Kreditor zu übertragen.
-   Für von Dienstleistungszeiten Arbeitsgänge in Produktionsflüssen, wird die Übertragung von Halbzeugen durch Lagerzugänge von Zurücknahme- oder Produktionskanbanen am Standort des Kreditors angegeben. Um eine explizite Umlagerungsaktivität zu modellieren, können Sie einen Produktionskanban mit einer zusätzlichen Umlagerungsaktivität beenden.

**Hinweis:** Ein Produktionsarbeitsplan für einen einzelnen Produktionsauftrag kann mehrere Standorte nicht verteilen. Diese Regel gilt auch für gleichzeitig die Fremdarbeit zu. Daher müssen die Lagerorte, die Kreditor-verwalteten die Schaltfläche Positionen darstellen, im gleichen Standort wie interne die Ressourcen definiert sind, die im Arbeitsplan verwendet werden. Obwohl Produktionsflüsse Standorte verteilen können, können sie nicht Datentransporthalbzeuge von einem Standort an anderen, da der Arbeitsgang eine Änderung des Kontexts Kosten vorgesehen.  

In der Regel werden der Ausgangslagerort und der Speicherort einer von Ressourcengruppe Artikel direkt zum Lagerort und Speicherort des nächsten Schritt des Arbeitsgangs im Arbeitsplan oder im Produktionsfluss zugewiesen. Diese Einstellung ermöglicht, den Betrag der berichterstellung Einzelvorgangs, die oder fungiert, der zusätzliche Arbeitsgänge der Nummer zu reduzieren Übergangs, die modelliert werden müssen.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]