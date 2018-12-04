---
title: "Stücklisten und Formeln"
description: "Dieser Artikel enthält Informationen zu Stücklisten (BOMs) und Formeln, die ein zentraler Teil der Definition der Produkte und Produktvarianten sind."
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConsistOf, BOMDesigner, BOMTable, EcoResProductProcessManufacturingWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19331
ms.assetid: c19b437a-2de2-4728-9477-2bcb0c2b1f5e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 430e2ab0c4438222ceb9102c011940af803acfbc
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="bills-of-materials-and-formulas"></a>Stücklisten und Formeln

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Informationen zu Stücklisten (BOMs) und Formeln, die ein zentraler Teil der Definition der Produkte und Produktvarianten sind. Stücklisten und Formeln können die erforderlichen Inhaltsstoffe oder Materialien für ein bestimmtes Produkt angezeigt. Formeln definieren außerdem die Kuppel- und Nebenprodukten, die in einem bestimmten Produktionskontext eingehen. 

<a name="bills-of-materials"></a>Stücklisten
------------------

Eine Stückliste (BOM) definiert die Komponenten, die erforderlich sind, um ein Produkt zu erzeugen. Die Komponenten können Rohmaterialien, Halbfertigprodukte oder Inhaltsstoffe sein. In einigen Fällen kann eine Stückliste auf Dienstleistungen verweisen. Jedoch beschreiben Stücklisten in der Regel erforderliche *Materialressourcen*.  

Wenn sie mit dem Arbeitsplan oder einem Produktionsfluss kombiniert wird, die die Arbeitsgänge und Ressourcen beschreibt, die erforderlich sind, um ein Produkt zu erstellen, bildet die Stückliste die Grundlage für die Berechnung der vorkalkulierten Kosten des Produkts.  

Eine Stückliste ist eine einzelne Entität, die mit den folgenden Informationen beschrieben wird:

-   BOM-Kennung
-   Stücklistenname
-   Stücklistenpositionen, die die Komponenten und die Substanzen beschreiben
-   Stücklistenversionen, die das Produkt und den Zeitraum festlegen, für das oder den die Stückliste verwendet werden kann

Eine einzelne Stückliste beschreibt eine einzelne Ebene, die durch eine eindeutige Kennung identifiziert wird. Komponenten verfügen möglicherweise über eigene Stücklisten, auf die von Stücklistenversionen verwiesen wird. Sie können die vollständige Hierarchie von Stücklisten für ein bestimmtes Produkt im Stücklisten-Designer anzeigen und bearbeiten.

### <a name="formulas-co-products-and-by-products"></a>Formeln, Kuppel- und Nebenprodukte

Eine Formel ist ein Untertyp der Stückliste, die normalerweise für die Fertigungsverarbeitung verwendet wird. Zusätzlich zu Komponenten und Zutaten beschreibt eine Formel Kuppel- und Nebenprodukte. In der tatsächlichen Version erfordert die Definierung von Co- und Nebenprodukte für die Formel die Formelversion. Eine Formel wird normalerweise für ein bestimmtes Produkt definiert (Produktion einer Formel oder eines Planungsartikel) die in der Formelversion im Formular definiert ist.

### <a name="boms-in-the-product-lifecycle"></a>Stücklisten im Produktlebenszyklus

Im Produktlebenszyklus werden zahlreiche Arten von Stücklisten aus unterschiedlichen Gründen erstellt:

-   **Skizzieren/Entwurf Stückliste** - Diese Stückliste gibt eine Entwurfsschätzung der erforderlichen Materialien in einer frühen Designphase an und hilft, eine grobe Schätzung der Kosten und vorkalkulierter Produktattribute vorzunehmen. Diese Stückliste wird in der Regel nicht in der Enterprise Resource Planning (ERP) verwendet.
-   **Konstruktionsstückliste** - Diese Stückliste wird normalerweise verwendet, wenn Sie Produkte entwerfen, die auf vorhandenen Produktpaletten basieren. Kontstuktionsstücklisten werden strukturiert, um den Designprozess zu vereinfachen und komplexe Produkte in Konstruktionsmodulen zu gruppieren. Für einfache Produkte können Konstruktionsstücklisten für den tatsächlichen Produktionsprozess genutzt werden. Für andere Produkte, muss die Konstruktionsstückliste in eine tatsächliche Produktionsstückliste umgerechnet werden. Konstruktionsstücklisten werden in der Regel über Phantomstücklisten in der Stücklistenhierarchie dargestellt. Obwohl Konstruktionsstücklisten für die Planung und die Ausführung von Produktionsvorgängen verwendet werden können, kann dieser Ansatz unwirtschaftlich sein, insbesondere in sich wiederholenden Arbeitsgängen, in denen zahlreiche Aufträge erstellt werden.
-   **Planungsstückliste** - Diese Stückliste wird verwendet, um Materialbedarf zu planen. Der Bedarf von Komponenten und von Zutaten wird basierend auf dem Bedarf der Fertigprodukte berechnet. Wie Kalkulationsstücklisten stellen Planungsstücklisten möglicherweise eine bestimmte Mischung der Materialien dar, die in einer Periode verwendet werden.
-   **Produktionsstückliste** - Dies ist die tatsächliche Stückliste, die für eine bestimmte Produktion verwendet wird. Eine Produktionsstückliste muss die tatsächlichen Ressourcen berücksichtigen, die verwendet werden, um das Endprodukt zu produzieren. Wenn ein Produktionsauftrag, ein Chargenauftrag oder ein Kanban erstellt wird, werden die mehrere Ebenen von Stücklisten, die von Phantome dargestellt werden, auf eine Ebene verringert und zu den Arbeitsgängen für den Auftrag verteilt.
-   **Kalkulationsstückliste** Der Preis, der zum Berechnen der vorkalkulierten Kosten eines Produkts verwendet wird. So können Sie beispielsweise eine Kalkulationsstückliste nutzen, wenn Standardkosten verwendet werden, oder vorkalkulierte Kosten eines bestimmten Produkts berechnet werden. Kalkulationsstücklisten können auf eine bestimmte Mischung von Materialien und Ressourcen verweisen, die erwartungsgemäß verwendet werden. Daher können Sie die Kalkulationsstückliste verwenden, um repräsentativ vorkalkulierte Kosten für eine Periode zu erstellen und Abweichungen im Zeitverlauf zu vermeiden.

Die Typen der Stückliste, die tatsächlich in einer Implementierung verwendet werden, hängen von der Implementierung und ebenso von den Geschäftsszenarien und Anforderungen ab. In den einfachen Implementierungen können eine Planung Stückliste, eine Produktionsstückliste und eine Kalkulationsstückliste als eine Stückliste modelliert werden. In der Umgebung, in der allgemeine Konstruktionsänderungen und mehrere alternative Arbeitspläne vorhanden sind, ist wahrscheinlich ein größerer Satz Stücklistentypen erforderlich.

### <a name="approval-of-boms-and-formulas"></a>Genehmigung von Stücklisten und von Formeln

Jede Stückliste und Formel kann separat genehmigt oder widerrufen werden. In der Regel erfolgt die Genehmigung einer Stückliste oder Formel, wenn die erste entsprechende Stücklistenversion genehmigt wurde. In einigen Geschäftsszenarien, sind diese Genehmigungen möglicherweise unterschiedliche Schritte in der Fertigung und beziehen verschiedene Prozessbesitzer mit ein.  

Beachten Sie, dass, wenn eine Stückliste widerrufen ist, alle zugehörigen Stücklistenversionen auch widerrufen sind.

## <a name="bom-and-formula-versions"></a>Stücklisten- und Formelversionen
Wenn Sie eine bestimmte Stückliste oder eine Formel einer Produktvariante zuzuordnen, die produziert werden kann, müssen Sie eine Stücklistenversion oder Formelversion erstellen. Die Gültigkeit von Stücklistenversionen und von Formelversionen kann durch Periode, Menge, Standort, bestimmte Produktdimensionen und andere Kriterien eingeschränkt werden. Formelversionen haben zusätzlich wichtige Attribute, wie Ertrag, Kuppel- und Nebenproduktdefinitionen und die Kostenverteilungsanweisungen für die Formel.

### <a name="approval-of-bom-and-formula-versions"></a>Genehmigung der Stücklisten- und Formelversionen

Bevor eine Stücklistenversion in der Planung oder im Produktionsprozess verwendet werden kann, muss sie genehmigt werden. Wenn eine Stücklistenversion genehmigt wird, kann die zugehörige Stückliste, je nach den Auswahl- und Authentifizierungsrechten des Benutzers, auch genehmigt werden. Beachten Sie, dass eine Stücklistenversion nur genehmigt werden kann, wenn die zugehörige Stückliste selbst genehmigt wird.

### <a name="activation-of-the-default-bom-or-formula-version"></a>Aktivierung der standardmäßigen Stücklisten- oder Formelversion

Wenn Sie eine bestimmte Stückliste oder eine Formel als standardmäßige Stücklisten- oder Formelversion festlegen wollen, die von der Produktprogrammplanung verwendet wird oder verwendet wird, um Produktionsaufträge zu erstellen, müssen Sie die Version aktivieren. Wenn die Version aktiviert ist, wird die Eindeutigkeit der Version für die angegebenen Einschränkungen (beispielsweise Gesamtlayout, Periode, Standort oder Menge) geprüft. Sie erhalten eine Fehlermeldung, wenn die Version, die Sie aktivieren möchten,  einen Konflikt mit einer Version ergibt, die bereits aktiv ist. Sie müssen dann entweder die Konflikt verursachende Version deaktivieren oder die Versionseinschränkungen (meist die Periode) ändern, um eine mehrdeutige Aktivierung zu verhindern.

### <a name="product-change-with-case-management"></a>Produktänderung mit Anfrageverwaltung

Der Produktänderungsfall zur Genehmigung und Aktivierung von neuen oder geänderten Stücklisten und Stücklistenversionen enthält eine einfache Möglichkeit, einen Überblick über die Stücklistenversionseinschränkungen anzuzeigen. Sie können alle Stücklisten und Formeln auch genehmigen und aktivieren, die einer bestimmten Änderung an einem Aktivierungsdatum zugeordnet sind.

### <a name="alternative-bom-versions"></a>Alternative Stücklistenversionen

Manchmal sollen die aktive Stücklistenversion oder die Formelversion nicht in Planungen, im Aufträgen bzw. in einem übergeordneten Produkt verwendet werden. In diesem Fall können Sie eine bestimmte genehmigte Stückliste als Teil des Bedarfs (Planungsposition, Verkaufsposition oder Stücklistenposition) auswählen, wenn eine genehmigte Stücklistenversion oder Formelversion für die alternative Stückliste oder Formel vorhanden ist.  

Wenn Bestellvorschläge, Produktionsaufträge oder Kanbans erstellt werden, kann der Planer oder Fertigungsbereichsvorgesetzte jede genehmigte Stücklistenversion verwenden, die am angeforderten geplanten Produktionsdatum gültig ist, um ein bestimmtes Produkt zu planen oder zu erzeugen. Die Stücklistenversion, die verwendet wird, muss nicht als standardmäßige Stücklistenversion aktiviert werden.

## <a name="bom-and-formula-lines"></a>Stürcklisten- und Formelpositionen
Eine Stücklistenposition wird für jedes Material, Service oder Bestandteil erstellt. Die Position definiert den geplanten Verbrauch der angegebenen Produktvariante und definiert auch die verschiedenen Attribute, die dem geplanten Verbrauch zugeordnet sind.  

Stücklistenpositionen können die folgenden Positionstypen haben: **Artikel**, **Phantom**, **Lieferung mit Bedarfsverursachung**, **Kreditor**.

### <a name="item"></a>Artikel

Wählen Sie den Positionstyp **Artikel** für Material oder Dienstleistungen aus, die direkt verbraucht werden und die keine weiteren Auflösung oder Lieferungen mit Bedarfsverursachung erfordern.

### <a name="phantom"></a>Phantom

Der Positionstyp **Phantom** wird zum Auflösen von Stücklistenartikeln einer niedrigeren Ebene verwendet, die in der Stücklistenposition enthalten sind. Beim Produktprogrammplanungslauf, der Berechnung der geplanten Kosten oder bei der Vorkalkulation eines Produktionsauftrags, die die Stücklistenpositionen des Typs **Phantom** verwendet, wird die übergeordnete Stücklistenposition mit der Produktvariante "Phantomstückliste" durch die Komponentenartikel, die als Stücklistenpositionen in dieser Stückliste aufgeführt sind, ersetzt, wie von der vorhandenen aktiven Stücklistenversion dieser Produktvariante bestimmt. Wenn die Produktvariante über einen vorhandenen aktiven Arbeitsplan verfügt, werden die Operationen dieses Arbeitsplans im übergeordneten Arbeitsplan zusammengeführt.  

Beachten Sie, dass Phantome in der Regel verwendet werden, um den Verfahrensprozess zu vereinfachen. Die umfangreiche Verwendung von Phantomstücklisten in vielen Ebenen hat Auswirkungen auf die Leistung, insbesondere in den hochgradig wiederkehrenden Fertigungsszenarien. Zur Verbesserung der Leistung, sollten Sie tiefgreifende Hierarchien von Phantomen vermeiden. Stattdessen verwenden Sie voraufgelöste Produktionsstücklisten und Arbeitspläne.

### <a name="pegged-supply"></a>Lieferung mit Bedarfsverursachung

Wählen Sie den**Lieferung mit Bedarfsverursachung** Positionstyp aus, wenn Sie eine Unterproduktion, einen Stücklistenpositions-Ereignis-Kanban oder eine direkte Bestellung für jede Produktvariante erstellen möchten auf die die Stücklistenposition verweist. Die Unterproduktion, der Ereignis-Kanban oder die Bestellung wird erstellt, wenn der Produktionsauftrag vorkalkuliert wurde. Die erforderlichen Artikelmengen werden automatisch für den Auftrag der Verbrauchsproduktion reserviert.

### <a name="vendor"></a>Händler

Wählen Sie den Positionstyp **Händler** wenn für den Produktionsprozess ein Zulieferer zum Einsatz kommt und für diesen automatisch eine Unterproduktion oder eine Bestellung erstellt werden soll.  

**Hinweis zu Fremdarbeitsdiensten in einer Stückliste:** Die Dienstleistung oder Arbeit, die der Zulieferer ausführt wird, muss als Dienstleistungsartikel erstellt werden, der im Bestand nachverfolgt wird. Sie müssen den Dienstleistungsartikel dem übergeordneten Artikel als Stücklistenposition zuordnen. Der Arbeitsplan muss einen Arbeitsgang enthalten, der der betrieblichen Ressource des Zulieferers zugewiesen ist.




