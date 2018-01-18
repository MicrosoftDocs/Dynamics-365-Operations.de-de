---
title: Formeln und Formelversionen
description: "Dieses Thema enthält Informationen zu Formeln und Formelversionen. Eine Formel definiert die Materialien, die Substanz und die Ergebnisse eines bestimmten Prozesses in einem der Fertigungsverarbeitung. Formeln werden verwendet, um in der Fertigungsverarbeitung Produkte zu planen und zu erzeugen."
author: cvocph
manager: AnnBe
ms.date: 09/12/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4475695b1a00213ab7e3b5060fd38cc71883d2bd
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="formulas-and-formula-versions"></a>Formeln und Formelversionen

[!include[banner](../includes/banner.md)]

Eine Formel definiert die Materialien, die Substanz und die Ergebnisse eines bestimmten Prozesses in einem der Fertigungsverarbeitung. Zusammen mit dem entsprechenden Arbeitsplan definiert die Formel in der Fertigungsverarbeitung den Gesamtprozess. Formeln werden verwendet, um in der Fertigungsverarbeitung Produkte zu planen und zu erzeugen.

Eine Formel besteht aus der Substanz und den Mengen, die erforderlich sind, um eine bestimmte Menge eines Formelartikels zu erzeugen. Abhängig von der Aufgabe, die Sie ausführen, können Sie Formelfunktionen  über " Lager- und Lagerortverwaltung oder aus dem Produkt informationsmanagement zugreifen.

## <a name="formulas-and-formula-lines"></a>Formeln und Formelpositionen 
Eine Formel besteht aus einer oder mehrerer Formelposition, die die Substanz oder Artikel identifizieren,  die die Formel ausmachen. Eine Formelposition kann Artikel, Stückliste (BOM), Formelartikel, Catch Weight-Artikel, gekaufte Artikel, Kuppel- oder Nebenprodukte enthalten. Da viele Artikel in mehreren Produkten verwendet werden, können Sie einen Artikel in mehreren Formeln verwenden.

Ein Beispiel einer Formel ist die Formel für Schokoladensplittercookie. Die Substanz dieser Formel verwendet mehrere Positionen, wie Mehl, Zucker, Eier, Butter und Schokoladensplitter. Die Formel für Kekse mit Schokoladensplittern werden Zutaten beschrieben, die mit ziemlicher Sicherheit auch in anderen rezeptbezogenen Formeln verwendet werden. Wenn Sie die Schokoladensplittercookien machen, haben Sie möglicherweise Restmengen wie Krumen, oder mehrere Kekse sind zu stark oder zu wenig stark gebacken. Diese Artikel können als Kuppel- oder Nebenprodukte eingerichtet werden, je nach Produktionsbetrieb.

Wenn Sie eine Formelposition erstellen, verwenden Sie den Positionstyp, um anzugeben, wie das System die Position behandeln solle,  wenn Sie die Produktprogrammplanung ausführen und Chargenaufträge produzieren. Jeder Positionstyp liefert ein anderes Ergebnis. In der folgenden Tabelle werden die Workflowtypen beschrieben, die Sie wählen können. 

| Positionstyp     | Beschreibung  |
|---------------|--------------|
| Artikel          | Wählen Sie **Artikel**, wenn es sich um Artikel aus Rohmaterialien oder halbfertigen Artikel handelt. Sie wird auch verwendet, wenn es sich bei dem Artikel um einen Service handelt. |
| Phantom       | Der Positionstyp **Phantom** wird zum Auflösen von Stücklistenartikeln einer niedrigeren Ebene verwendet, die in der Stücklistenposition enthalten sind. Wen Sie den Chargenauftrag schätzen und die Formelartikel aufgelöst sind, werden die Komponentenartikel als Formelpositionen für den Chargenauftrag angezeigt. Darüber hinaus werden die entsprechenden Arbeitspläne dem Produktionsarbeitsplan hinzugefügt. Formelartikel werden aufgelöst, indem die aktuelle Konfiguration verwendet wird. Bei Verwendung des Positionstyps **Phantom** können Sie die Produktions- und Verbrauchsrechnungskonfigurationen behandeln, die auf den verschiedenen Stücklistenebenen anfallen. Wenn Sie **Phantom** für ein Produkt auf dem Inforegister **Entwickler** der Seite **Details für freigegebene Produkte** auswählen und dann dieses Produkt in einer Formel verwenden, wird der Positionstyp der Formelposition zu **Phantom** geändert. Sie können **Phantom** für einen Catch Weight-Artikel oder für Artikel nicht auswählen, in denen der Produktionstyp von **Kuppelprodukt**, **Nebenprodukt** oder ist **Planungsartikel** |
| Lieferung mit Bedarfsverursachung | Wählen Sie **Lieferung mit Bedarfsverursachung**, um einen Chargenauftrag, einen Produktionsauftrag, ein Kanban, einen Umlagerungsauftrag oder eine Bestellung für den dienen zu erstellen, die in der Formelposition enthalten ist. Der zugehörige Auftrag wird basierend die Standardauftragseinstellungen und der Produktionstyp der Substanz bestimmt und erstellt, wenn Sie den Chargenauftrag schätzen. Die erforderlichen Substanzmengen werden automatisch für den Chargenauftrag reserviert. |
| Lieferant        | Die Option **Lieferant** wird verwendet, wenn für den Produktionsprozess ein Zulieferer zum Einsatz kommt und für diesen automatisch eine Unterproduktion oder eine Bestellung erstellt werden soll. Die Dienstleistung oder die Arbeit, die durch den Zulieferer ausgeführt wird, müssen als mithilfe des Formelartikels oder des Serviceelements  im Formular  erstellt werden. Sie können den Dienstleistungsartikel dem übergeordneten Artikel als Stücklistenposition zuordnen. Der Arbeitsplan muss einen Arbeitsgang enthalten, der der betrieblichen Ressource des Zulieferers zugewiesen ist. Dieser Arbeitsgang muss der Stücklistenposition mithilfe des Felds **Arbeitsgangnummer** zugeordnet werden. enthält. |

## <a name="formula-versions"></a>Formelversionen
Wenn Sie eine neue Formel erstellen, müssen Sie zuerst die Formelversion erstellen, bevor Sie Formelpositionsartikel mit deren bestimmten Merkmalen hinzufügen. Für jede Formel ist mindestens eine Version erforderlich. Die Schaltfläche **Genehmigt** in einer Formelversion wird verfügbar, nachdem ein Versionsdatensatz erfolgreich gespeichert wurde. Jeder Formelversionsdatensatz wird mit einem oder vielen Kuppel- und Nebenprodukten verknüpft, die Sie produziert werden können, wenn Sie das fertige Produkt erstellen. Viele Produkte können aus den gleichen Zutaten auch in verschiedenen Batchgrößen, in Vielfachen oder durch Erstellen verschiedener Erträge verwendet werden. Sie können beliebig viele zusätzliche Formularversionen erstellen.

Verwenden Sie zur einfacheren Verwaltung von mehreren aktiven Formelversionen gültige Datumsbereiche oder die Mengen-Felder. Allerdings können nur dann mehrere aktive Formelversionen vorhanden sein, wenn sich die Datumsangaben und Mengen nicht überschneiden.

Anders als Stücklisten, in denen eine Stückliste häufig zahlreichen Stücklistenversionen zugeordnet wird, existiert in der Regel nur eine Formelversion pro Formel. Bedenken Sie, dass nur eine Formelversion für die Deckungsdimensionen und die Menge für ein bestimmtes Produkt aktiviert werden kann. Jedoch können viele Formelversionen für andere Ursachen bestehen und Sie können manuell auswählen, wenn Sie einen Chargenauftrag erstellen.

## <a name="approve-and-activate-formulas-and-formula-versions"></a>Hiermit genehmigen und aktivieren Sie Formeln und Formelversionen
Formeln und Formelversionen müssen genehmigt werden, bevor Sie für die Planung und Produktion gestartet werden können. Formeln werden normalerweise aktiviert, bevor sie verwendet werden. Allerdings können Sie während der Produktion eine Formelversion auswählen, die genehmigt, aber nicht aktiviert ist.

Um eine Formel oder Formelversion zu unterstützen, können Sie die **Bearbeitung sperren** und **Entfernung der Genehmigung**-Parameter auf der Seite **Produktionssteuerungsparameter** festlegen.

Wenn Sie **Bearbeitung sperren** auswählen und die Formel genehmigt ist, können keine Felder in den Formelpositionen gelöscht oder bearbeitet werden. Wenn Sie die Genehmigung der Formel entfernen, können Sie Formelpositionen löschen und ändern. Sie können neue Formeln und Formelversionen auch neue erstellen.

Wenn Sie **Entfernung der Genehmigung sperren** auswählen, können Sie die Genehmigung einer genehmigten Formel oder Formelversion nicht mehr entfernen. Allerdings können Sie neue Formeln und neue Formelversionen erstellen, und Sie können die Aktivierung der Formelversion entfernen.

Sie können mehr Steuerungsdimensionen le hinzufügen, indem Sie die Funktion für elektronische Signaturen verwendet werden. Wenn ein Benutzer eingerichtet wird, dass eine elektronische Signatur zum Zeitpunkt der genehmigung Formel erforderlich ist, wird die Seite **Unterschrift** angezeigt, wenn die Formel aktiviert ist. Der Benutzer muss autorisiert sind, um elektronisch zu signieren, und die Bescheinigung muss erfolgreich validiert werden, damit die Änderung übernommen wird. Wenn die Signatur nicht authentifiziert werden kann, wird die Genehmigung bzw. das Aufheben der Genehmigung verweigert, und die Änderung, durch die dieser Vorgang initiiert wird, wird in den ursprünglichen Zustand zurückversetzt.

## <a name="use-the-scalable-feature"></a>Verwenden Sie die Funktion Skalierbar
Die Funktion Skalierbar ist nur verfügbar, wenn nur alle Artikelkomponenten in der Formel auf **Variabler Verbrauch** werden. Die Funktion ist nicht verfügbar, wenn Artikelkomponenten auf **Fester Verbrauch** oder **Verbrauch pro Schritt** festgelegt werden. Wenn die Funktion Skalierbar verwendet wird, wenn Sie eine Substanz in einer Formel ändern, wird die Menge der anderen Substanz, die Sie ausgewählt haben, angepasst. Die Größe der Formel wird auch angepasst. Ebenso wenn Sie die Formelgröße ändern, wird die Menge aller skalierbare Substanzen geändert. Diese Funktion dient speziell für die Formelerstellung und Verwaltung. Sie gibt nicht an, ob die Menge des Inhaltsstoffs nach oben oder unten in einem Chargenauftrag skaliert wird.

## <a name="use-step-consumption"></a>Verbrauch pro Serie
Schrittverbrauch beseitigt die Menge auf der **Formelposition**,den Sie für eine Substanz eingeben müssen. Stattdessen wird der  Schrittverbrauch konfiguriert, sodass dieser den **Von Serie**Wert und eine **Menge** besitzt. Auf Basis der Chargenauftragsmenge werden die Informationen aus dem Schritt pro Serie, der die Menge befriedigt, ausgewählt Schrittverbrauch ist hilfreich, wenn der Verbrauchssatz nicht linear in Bezug auf die Chargenauftraggröße ist und die Anforderung nur erhöht, wenn ein bestimmter Mengenschwellenwert erfüllt wird. Um diese Funktion für eine neue Formel, unter der Gruppe **Verbrauchsberechnung** zu aktivieren,ändern Sie die Formeleinstellung für den betreffenden Inhaltsstoff von **Standard** auf **Schritt** Sie können dieser Verbrauchsmethode auf der Registerkarte**Einstellungen** auf der Seite **Formelposition** anzeigen.

