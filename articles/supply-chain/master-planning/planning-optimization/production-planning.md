---
title: Produktionsplanung
description: In diesem Thema wird die Planung für die Produktion beschrieben und erläutert, wie Sie geplante Produktionsaufträge mithilfe der Planungsoptimierung ändern können.
author: ChristianRytt
ms.date: 06/01/2021
ms.topic: article
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 85167e3de5f586c341143a43412501377a6c689e
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570896"
---
# <a name="production-planning"></a>Produktionsplanung

[!include [banner](../../includes/banner.md)]

Die Planungsoptimierung unterstützt mehrere Produktionsszenarien. Wenn Sie vom bestehenden integrierten Masterplanungsmodul migrieren, ist es wichtig, dass Sie einige geänderte Verhaltensweisen beachten.

Das folgende Video gibt eine kurze Einführung in einige der in diesem Thema besprochenen Konzepte: [Dynamics 365 Supply Chain Management: Erweiterungen der Planungsoptimierung](https://youtu.be/u1pcmZuZBTw).

## <a name="turn-on-this-feature-for-your-system"></a>Schalten Sie diese Funktion für Ihr System ein

Wenn Ihr System noch nicht über die in diesem Thema beschriebenen Funktionen verfügt, gehen Sie zu [Funktionsverwaltung](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) und schalten Sie die Funktion *Geplante Produktionsaufträge zur Planungsoptimierung* ein.

## <a name="planned-production-orders"></a>Geplante Produktionsaufträge

Wenn die Masterplanung geplante Aufträge erstellt, um Anforderungen zu erfüllen, wird der Auftragstyp durch den Wert des Felds **Geplante Auftragsart** bestimmt. Wenn das Feld **Geplante Auftragsart** auf *Produktion* festgelegt ist, werden geplante Produktionsaufträge erstellt. Diese geplanten Produktionsaufträge enthalten Informationen zur aktiven Stückliste und zur Routenkennung aus dem zugehörigen Produktionsaufbau.

## <a name="requirements-from-boms"></a>Anforderungen aus Stücklisten

Stücklisteninformationen werden bei der Masterplanung berücksichtigt. Die Planausgabe umfasst die Materialversorgung zur Deckung des damit verbundenen Materialbedarfs für die Produktion.

Während der Masterplanung wird anhand der aktuellen aktiven Stückliste ermittelt, welche Materialien für die Produktion benötigt werden. Dieser Schritt wird auf allen Ebenen der Stücklistenstruktur ausgeführt, die sich auf den erforderlichen Produktionsauftrag beziehen. Der Materialbedarf wird durch die Verwendung des verfügbaren Bestands, der laufenden Vorratsbestellungen und der genehmigten geplanten Aufträge erfüllt. Wenn zusätzliches Material benötigt wird, wird ein geplanter Auftrag erstellt, um den Bedarf zu decken.

## <a name="scheduling-during-firming"></a>Planung während der Umwandlung

Geplante Produktionsaufträge enthalten die Routenkennung, die zur Produktionsplanung erforderlich ist. Der Planungssupport während des Planungslaufs für geplante Aufträge steht jedoch noch aus. Die Routenkennung wird verwendet, um geplante Produktionsaufträge während der Umwandlung zu planen. Daher kann die Vorlaufzeit für geplante Produktionsaufträge von der Vorlaufzeit für zugehörige geplante, umgewandelte Produktionsaufträge abweichen, die aus ihnen generiert werden, wie hier beschrieben:

- **Geplanter Produktionsauftrag** – Die Vorlaufzeit basiert auf der statischen Vorlaufzeit des freigegebenen Produkts.
- **Umgewandelter Produktionsauftrag** – Die Vorlaufzeit basiert auf einer Zeitplanung, die Routeninformationen und zugehörige Ressourcenbeschränkungen verwendet.

Weitere Informationen zur erwarteten Verfügbarkeit von Funktionen finden Sie unter [Passanalyse zu Planungsoptimierung](planning-optimization-fit-analysis.md).

Wenn Sie auf Produktionsfunktionen angewiesen sind, die zur Planungsoptimierung noch nicht verfügbar sind, können Sie weiterhin das integrierte Masterplanungsmodul verwenden. Eine Ausnahme ist nicht erforderlich.

## <a name="delays"></a>Verzögerungen

Wenn die Vorlaufzeit für das erforderliche Material länger ist als der Zeitraum zwischen dem heutigen Datum und dem Materialbedarfsdatum, wird der geplante Auftrag für das erforderliche Material und den zugehörigen Produktionsauftrag verzögert. Bei geplanten Aufträgen wird die Verzögerung (in Tagen) anhand der Vorlaufzeit des freigegebenen Produkts berechnet. Die Verzögerungsinformationen werden dann über alle Ebenen der Stücklistenstruktur weitergegeben. Daher können Sie die Auswirkungen von Verzögerungen beim Rohmaterial bis zum Kundenauftrag verfolgen.

## <a name="modifying-planned-orders"></a>Ändern von geplanten Aufträgen

Wenn Sie Informationen zu einem geplanten Auftrag ändern, wird folgende Meldung angezeigt: „Beachten Sie, dass die Auswirkungen manueller Änderungen auf geplante Aufträge für die restliche Planung erst im nächsten Masterplanungslauf berücksichtigt werden.“

Wenn Sie Informationen zu einem geplanten Auftrag ändern und die Auswirkungen auf die zugehörigen Materialanforderungen sehen möchten, führen Sie die folgenden Schritte aus.

1. Aktualisieren Sie den geplanten Auftrag.
2. Genehmigen Sie den geplanten Auftrag.
3. Führen Sie die Masterplanung aus.

Wenn Sie die Masterplanung ausführen, sollten Sie keine Filter verwenden, wenn geplante Produktionsaufträge enthalten sind. Weitere Informationen finden Sie im Abschnitt [Filter](#filters) weiter unten in diesem Thema.

> [!NOTE]
> Wenn das Lieferdatum für den geplanten Auftrag auf einen späteren Zeitpunkt verschoben wird, kann die Nachfrage an einen neuen geplanten Auftrag gebunden sein. Dieses Verhalten tritt auf, wenn der neue Liefertermin eine Verzögerung für die gebundene Nachfrage verursacht, die Verzögerung jedoch gemäß den Einstellungen für die Vorlaufzeit vermieden werden kann.

## <a name="explosion-page"></a>Die Seite „Auflösung“

Sie können die Seite **Auflösung** verwenden, um den erforderlichen Bedarf für einen bestimmten oder geplanten Produktionsauftrag, die zugehörige Abdeckung und die Informationen zum Bedarfsverursacher zu analysieren. Die Informationen auf der Seite **Auflösung** werden während der Masterplanung aktualisiert. Sie können die Informationen nicht direkt über die Seite **Auflösung** aktualisieren.

## <a name="filters"></a><a name="filters"></a>Filter

Um sicherzustellen, dass die Planungsoptimierung über die erforderlichen Informationen zur Berechnung des korrekten Ergebnisses verfügt, müssen Sie alle Produkte berücksichtigen, die in irgendeiner Beziehung zu Produkten in der gesamten Stücklistenstruktur des geplanten Auftrags stehen. Für Planungsszenarien inklusive Produktion empfehlen wir deshalb, gefilterte Masterplanungsläufe zu vermeiden.

Obwohl abhängige untergeordnete Artikel automatisch erkannt und in Masterplanungsläufe einbezogen werden, wenn das integrierte Masterplanungsmodul verwendet wird, führt die Planungsoptimierung diese Aktion aktuell nicht aus.

Wenn beispielsweise eine einzelne Schraube aus der Stücklistenstruktur von Produkt A auch zur Herstellung von Produkt B verwendet wird, müssen alle Produkte in der Stücklistenstruktur der Produkte A und B in den Filter aufgenommen werden. Da es komplex sein kann, sicherzustellen, dass alle Produkte Teil des Filters sind, empfehlen wir, gefilterte Masterplanungsläufe zu vermeiden, wenn Produktionsaufträge betroffen sind. Andernfalls führt die Masterplanung zu unerwünschten Ergebnissen.

### <a name="reasons-to-avoid-filtered-master-planning-runs"></a>Gründe, gefilterte Masterplanungsläufe zu vermeiden

Wenn Sie eine gefilterte Gesamtplanung für ein Produkt ausführen, erkennt die Planungsoptimierung (im Gegensatz zur integrierten Masterplanungs-Engine) nicht alle Unterprodukte und Rohstoffe in der Stücklistenstruktur dieses Produkts und nimmt sie daher nicht in den Master auf Planungslauf. Obwohl die Planungsoptimierung die erste Ebene in der Stücklistenstruktur des Produkts identifiziert, werden keine Produkteinstellungen (wie die Standardauftragsart oder die Artikelabdeckung) aus der Datenbank geladen.

In der Planungsoptimierung werden die Daten für den Lauf zuvor geladen und wenden die Filter an. Dies bedeutet, dass, wenn ein Unterprodukt oder ein Rohmaterial, das in einem bestimmten Produkt enthalten ist, nicht Teil des Filters ist, keine Informationen darüber für den Lauf erfasst werden. Wenn das Unterprodukt oder der Rohstoff auch in einem anderen Produkt enthalten ist, würde ein gefilterter Lauf, der nur das Originalprodukt und seine Komponenten enthält, den bestehenden Planbedarf entfernen, der für dieses andere Produkt erstellt wurde.

Diese Logik kann dazu führen, dass gefilterte Masterplanungsläufe unerwartete Ergebnisse liefern. Die folgenden Abschnitte enthalten Beispiele, die die unerwarteten Ergebnisse veranschaulichen, die auftreten können.

### <a name="example-1"></a>Beispiel 1

Fertigerzeugnisse *FG* bestehen aus folgenden Komponenten:

- Rohmaterial *R*
- Unterprodukt *S1*, das aus Unterprodukt *S2* besteht

Es gibt Lagerbestände für das Rohmaterial *R*, während Unterprodukt *S1* nicht im Bestand vorhanden ist.

Wenn Sie einen gefilterten Masterplanungslauf für Fertigerzeugnisse *FG* durchführen, erhalten Sie einen geplanten Produktionsauftrag für das Fertigerzeugnis *FG*, eine geplante Einkaufsbestellung für den Rohstoff *R* und eine geplante Einkaufsbestellung für das Unterprodukt *S1*. Dies ist ein unerwünschtes Ergebnis, da die Planungsoptimierung die vorhandene Rohstoffversorgung *R* ignoriert hat und Unterprodukt *S1* mit *S2* hergestellt werden muss, anstatt es direkt zu bestellen. Dies geschah, weil Planning Optimization nur die Liste der Komponenten für das Fertigerzeugnis *FG* ohne diesbezügliche Informationen hat, wie zum Beispiel die vorhandene Lieferung seiner Komponenten oder deren Standardbestelleinstellungen.

### <a name="example-2"></a>Beispiel 2

Aufbauend auf dem vorherigen Beispiel nutzt ein zusätzliches Fertigerzeugnis *FG2* auch Unterprodukt *S1*. Für das Fertigerzeugnis *FG2* liegt ein geplanter Auftrag vor und es besteht ein geplanter Bedarf für alle seine Komponenten, einschließlich *S1*.

Sie beschließen, die unerwünschten Ergebnisse des gefilterten Gesamtplanungslaufs aus dem vorherigen Beispiel zu überwinden, indem Sie alle Unterprodukte und Rohstoffe aus der Stücklistenstruktur des Fertigerzeugnisses *FG* zum Filter hinzufügen und dann eine vollständige Regeneration durchführen.

Wenn Sie die vollständige Regenerierung ausführen, löscht das System alle vorhandenen Ergebnisse für alle enthaltenen Produkte und erstellt dann die Ergebnisse basierend auf den neuen Berechnungen neu. Dies bedeutet, dass der bestehende geplante Bedarf für Produkt *S1* gelöscht wird und dann unter Berücksichtigung nur der Anforderungen des Fertigerzeugnisses *FG* neu erstellt wird, während die Anforderungen für Fertigerzeugnis *FG2* nicht beachtet werden. Dies liegt daran, dass beim Ausführen der Planungsoptimierung der geplante Bedarf anderer geplanter Produktionsaufträge nicht berücksichtigt wird&mdash;nur der während des Laufs erzeugte Planbedarf wird verwendet.

> [!NOTE]
> Wenn der bestehende geplante Auftrag für Fertigerzeugnis *FG2* sich im Status *Genehmigt* befindet, dann wird der genehmigte geplante Bedarf eingeschlossen, auch wenn das übergeordnete Produkt dem Filter nicht hinzugefügt wird.

Daher stellt die gefilterte Masterplanung, sofern Sie nicht alle Komponenten des Fertigerzeugnisses *FG*, Fertigerzeugnis *FG2*, und alle anderen Produkte, zu denen diese Komponenten (zusammen mit ihren Komponenten) gehören ,hinzufügen, unerwünschte Ergebnisse bereit.

Da es komplex sein kann, sicherzustellen, dass alle Produkte Teil des Filters sind, empfehlen wir, gefilterte Masterplanungsläufe zu vermeiden, wenn Produktionsaufträge betroffen sind.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
