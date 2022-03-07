---
title: Nachkalkulation für Produktionskosten
description: Dieses Thema enthält das Konzepts der Nachkalkulation für Produktionskosten, die für Lean Manufacturing verwendet werden.
author: AndersGirke
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeanCosting, LeanCostingTimeBucket
audience: Application User
ms.reviewer: kamaybac
ms.custom: 272063
ms.assetid: 62a2a7da-ff79-49bf-a6e8-29460ba5252f
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: d158908182a35b7b4cbf0ad8a5d1fc7df37815d3
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579831"
---
# <a name="backflush-costing"></a>Nachkalkulation für Produktionskosten

[!include [banner](../includes/banner.md)]

Dieses Thema enthält das Konzepts der Nachkalkulation für Produktionskosten, die für Lean Manufacturing verwendet werden. 

Die Nachkalkulation für Lean Manufacturing verwendet den Produktionsfluss, um die Kostenkumulierungsmethode zu definieren, die als für Nachkalkulationen für Produktionskosten bezeichnet wird. In der Nachkalkulation für Produktionskosten-Methode werden die direkte Materialien, die verbraucht werden, im Produktionsflusses des Kontos der laufenden Arbeitskosten (VIP) kumuliert. Die Standardkosten-Modellgruppe wird verwendet. Die Produkte, die vom Produktionsfluss empfanen werden, werden vom RIF zu den Standardkosten abgezogen. Der Hauptunterschied zwischen Nachkalkulation für Produktionskosten und Standardkosten ist der, dass bei der Nachkalkulation für Produktionskosten Abweichungen pro Kanban oder abgeschlossenem Produkt nicht berechnet werden. Stattdessen werden Abweichungen pro Produktionsfluss über einen Zeitraum berechnet. Diese Methode bietet ein tatsächlich Lean-Konzept für das Melden der Materialentnahme. Dedizierte werden entnommene Stoffmengen keinem Kanban oder Produktionsauftrag gemeldet. Stattdessen werden vollständige Chargen oder Handhabungseinheiten dem Produktionsfluss bereitgestellt. Nachdem Chargen oder Handhabungseinheiten als leer erfasst werden, werden sie als verbraucht deklariert. Erweiterter Verbrauch wird verwendet, abhängig von der [Konfiguration des Produktionsflusses](../production-control/lean-manufacturing-modeling-lean-organization.md). Bevor der erweiterte Verbrauch verwendet werden kann, müssen Sie Organisationen es ermöglichen, dass Material im RIF-Konto des Produktionsflusses verschwindet. Die Nachkalkulation für regelmäßige Produktionskosten bestimmt den RIF-Wert am Ende der Periode. Diese Bestimmung basiert auf den Kanbanhandhabungseinheiten und dem Kanban-Einzelvorgangsstatus. Abweichungen zwischen den Ist-Werten und den tatsächlichen RIF-Werten pro Kostengruppe und Artikel werden als Abweichungen berechnet und angezeigt.

## <a name="configuring-backflush-costing"></a>Konfiguration der Nachkalkulation für Produktionskosten
Um die Nachkalkulation zu ermöglichen, müssen Sie folgende Einstellungen vornehmen:

-   **RIF-Konten für das Produktionsbuchungsprofil und den Produktionsfluss einrichten.** Die RIF-Konten für den Produktionsfluss werden in Produktionsgruppen definiert. Der Produktionsfluss der Nachkalkulation für Produktionskosten berechnet Abweichungen als Differenz im RIF-Wert vor und nach der Nachkalkulation für Produktionskosten wird für jeden Produktionsfluss ausgeführt. Daher wird empfohlen, dass Sie für jeden Produktionsfluss ein RIF-Konto erstellen.
-   **Aktuelle Ressource einer Ressourcengruppe zuweisen** Sie müssen eine Kostenkategorie der gewünschten Kategorie einer Arbeitsgruppe zuweisen. Wenn Sie Abweichungen nach Aktivität festzulegen, sollten Sie eine Kostenkategorie für jede Fertigungszelle erstellen. Die Kostenkategorien für Einrichtung und Menge werden nicht bei der Nachkalkulation für Produktion berücksichtigt. Die RIF-Konten pro Ressourcengruppe werden bei der Nachkalkulation für Produktionskosten ignoriert. Für Fremdarbeitsaktivitäten ist eine Kostenkategorie erforderlich. Die Kostengruppe, die dem aktiven Service zugewiesen wird, wird stattdessen verwendet.
-   **Kostengruppen zuweisen** Um Segmentierung des Kostenbeitrags in einem Produktionsfluss zu ermöglichen, müssen Sie die Kostengruppen über Kostengruppentypen zuweisen.:
    -   **Direkte Materialkostengruppe** Direktes Material erfordert eine Kostengruppe, die die Materialkategorie für die Kosten bestimmt. Diese Kostengruppen ermöglicht eine aggregierte Ansicht von Kosten, RIF und Abweichungen nach Direktmaterial.
    -   **Direkte Herstellungskostengruppe** - Die Kostengruppe Direkte Herstellungskosten erfasst den direkten Kostenbeitrag der betrieblichen Ressourcen für den Produktionsfluss. Diese Kostengruppen ermöglicht eine aggregierte Ansicht von Kosten, RIF und Abweichungen nach Direktmaterial.
    -   **Gruppe für indirekte Kostenkomponenten** - Die Gruppe der indirekten Kosten erforderlich, um den Deckungsbetrag indirekter Kosten den Produktionsfluss zu berechnen. Diese Kostengruppen ermöglicht eine aggregierte Ansicht von Kosten, RIF und Abweichungen nach indirekten Kosten.
    -   **Direkte Auslagerungskostengruppe** - Die Kostengruppe für die Dienstleistungen aktiviert aggregierte Ansichten von zugeordneten Kosten und RIF und bestimmt die Kostenabweichungen der weitervergebenen Dienstleistungen.
    -   **Kostengruppe für ein fertiges Produkt** - Fertige Produkte benötigen eine Kostengruppe, die die Produktkategorie für die Kosten bestimmt. Diese Kostengruppen ermöglicht eine aggregierte Ansicht von Kosten, RIF und Produktabweichungen nach Kategorie. Die Standardkosten für Produkte werden berechnet, indem die Kostenberechnung, die auf der Stückliste (BOM) ist, und entweder der Produktionsfluss und die Kanban-Regeln oder der Arbeitsplan verwendet wird.

### <a name="costing-sheet"></a>Nachkalkulationsbogen

Die Nachkalkulationsbogenmodelle der Kostenstruktur für das Unternehmen und wird von Kostengruppen erstellt, um die Kosten zu klassifizieren. Das Nachkalkulationsblatt hat unterschiedliche Formulare. Es zeigt Kosteninformationen entsprechend der Struktur, die darin enthaltenen sind. Im Nachkalkulationsblatt definieren Sie auch die Formel, die verwendet wird, um indirekte Kosten zu berechnen. Die Berechnungsformel kann auf Mengen, Gewicht, Volumen oder Wert basieren.

-   **Verwaltung der Nachkalkulationsversion** In der Nachkalkulationsversion definiert das Unternehmen, wie die Kosten verwaltet werden sollen. Eine Nachkalkulationsversion kann eine Gruppe von Standardkostendatensätzen oder eine Gruppe von Datensätzen mit geplanten Kosten enthalten, die vom Kostentyp, die der Nachkalkulationsversion zugewiesenen sind, abhängen. Die Nachkalkulationsversion, die zur Nachkalkulation für Produktion verwendet wird, muss auf den Standardkosten basieren.
-   **Weisen Sie den freigegebenen Artikeln eine Lagersteuerungsgruppe zu.** Alle Produkte, die dem Produktionsfluss zugeordnet werden, müssen einer Lagersteuerungsgruppe zugeordnet werden, die die **Standardkosten** Lagersteuerungsgruppe verwendet. Standardkosten werden pro Standort und Aktivierungsdatum verwaltet. Für Produktmaster kann die Lagersteuerungsgruppe aktiviert werden, wenn die Kosten pro Variante oder Produktmaster verwaltet werden.
-   **Definitionsgemäß sind Dienstleistungszeiten nicht-inventarisierte Services.** Weitervergebene Aktivitäten enthalten keine Lagersteuerungsgruppe. Um eine Fremdarbeitsaktivität korrekt zu kalkulieren, müssen Sie überprüfen ob die Serviceaktivität zu einer Lagersteuerungsgruppe gehört, in der die Bestandsrichtlinie auf **Gelagertes Produkt = False** festgelegt ist.

Für hergestellte Produkte braucht die Kostenberechnung, die auf dem Produktionsfluss basiert, die Standardkosten für Dienstleistungen, die mit den weitervergebenen Aktivitäten zusammenhängen. Die Kostengruppe, die den Services zugeordnet ist, wird verwendet, um die Kostenabweichungen der weitervergebenen Aktivitäten zu bestimmen.

## <a name="cost-calculation-for-lean-manufacturing"></a>Kostenberechnung für Lean Manufacturing
Klicken Sie für Produkte, die aus einem Produktionsfluss nicht angegeben werden muss, die Herstellkostenkalkulation auf einer Arbeitsplanversion einen Produktionsfluss oder lauten. Die Herstellkostenkalkulation berechnet die Kosten eines Produkts und die Aufschlüsselung der zugehörigen Ressourcen, die erforderlich sind, um das Produkt zu erstellen. Der Abzug vom RIF für den Produktionsfluss erfolgt, indem er die Aufschlüsselung eines Produkts nach Artikel und Kostengruppe verwendet.

### <a name="calculation-that-is-based-on-the-production-flow"></a>Berechnung, die auf dem Produktionsfluss basiert.

Lean Manufacturing für Dynamics 365 Supply Chain Management ist unabhängig von Arbeitsplänen. Die Kostenkalkulation für Produkte, die aus einem Produktionsfluss erfolgen, kann auf dem Produktionsfluss selber basieren. Bevor die Berechnung ausgeführt werden kann, muss eine Kanban-Regel erstellt werden, die das Produkt aus dem Produktionsfluss bereitstellt. Wenn ein Produkt aus mehreren Produktionsflüssen am gleichen Standort im Berechnungsdatum beschafft werden kann, können Sie den Produktionsfluss für die Herstellkostenkalkulation auswählen. Auf der Seite **Standardproduktionsfluss** können Sie einen Standardproduktionsfluss für jeden Artikel konfigurieren. Wenn mehrere Kanban-Regeln für die gleiche Produktdimensionsgruppe im gleichen Produktionsfluss vorhanden sind, der auf dem Berechnungsdatum aktiv ist, wird die Berechnung die erste Kanban-Regel ausführen, die für die Berechnung aktiviert ist.

### <a name="calculation-that-is-based-on-the-route"></a>Berechung, die auf dem Arbeitsplan basiert

Berechnung, die auf einem Arbeitsplan basiert, ist ebenso gültig wie ein wenn sie auf einem Produktionsfluss basiert. Allerdings verwendet die Berechnung auf de Basis eines Arbeitsplans nicht die Nachkalkulation für Lean Manufacturing-Funktionalitäten. Der Arbeitsplan sollte Ressourcenanforderungen für Ressourcengruppen verwenden. Um Systemabweichungen zu vermeiden, sollte er die gleichen Arbeitsgruppen verwenden oder mintestens die gleichen Kostenkategorien. Wieder sollten Sie Kostenkategorien für Einrichtung und Menge vermeiden. Sie unterstützen nicht bei der Berechnung von Kosten in eine genauere Aufschlüsselung als die Nachkalkulation beim Lean Manufacturing. Um zu bestimmen, welche Option (Produktionsfluss oder Arbeitsplan) Sie verwenden sollten, um die Kosten zu berechnen, nehmen Sie die Ergebnisse der Kostenaufschlüsselung. Die Version, die der Realität mehr entspricht und weniger Abweichungen gesamthaft produziert, ist die bessere Option In einer Produktionsumgebung, in der ein Produkt über einen einzelnen Produktionsfluss und eine einzige Kanban-Regel beschafft wird, basiert die Berechnung auf Grundlage des Produktionsflusses und ist wahrscheinlich genauer. Für ein Produkt, das durch Lean Manufacturing und Produktionsaufträge für den gleichen Standort beschafft werden kann oder das mehrere Produktionsflüsse oder mehrere Kanban-Regeln im selben Fluss haben kann, ist eine Berechnung möglicherweise genauer, wenn sie auf einer Arbeitsplanversion basiert, die speziell für die Kostenberechnung erstellt wird und nicht für die Produktion. Die Produktionsflussberechnung muss verwendet werden, um Produkte zu berechnen, die Fremdarbeit umfassen. Die Kostenmodelle für Fremdarbeit über Produktionsaufträge und Fremdarbeit in Lean Manufacturing verwenden zwei unterschiedliche Ansätze. Lean Manufacturing führt einen neuen Kostengruppentyp, **Direktes Outsourcing** ein, Fremdarbeits-Services zu berechnen.

## <a name="material-consumption"></a>Materialverbrauch
Wenn Material von Bestand in RIF verbraucht wird, werden die Kosten des Materials in RIF den tatsächlichen Standardkosten für eine Kostengruppe hinzugefügt. Dieser Vorgang erfolgt unter den folgenden Bedingungen:

-   Kanbanaprobleme werden für Kanbanentnahmepositionen gebucht, die den Bestand aktualisieren.
-   Umlagerungseinzelvorgänge wurden abgeschlossen, die den Bestand bei Entnahme aktualisieren, aber nicht den Empfang (Übertrg von Material aus dem Bestand zu RiF).

## <a name="receiving-products-from-the-production-flow"></a>Eingang von Produkten im Produktionsfluss
Produkte werden aus dem Produktionsfluss unter den folgenden Bedingungen erhalten:

-   Verarbeitete Jobs sind abgeschlossen, wenn **Bestand bei Eingang Aktualisieren** auf **Ja** festgelegt ist.
-   Umlagerungseinzelvorgänge wurden abgeschlossen, die den Bestand bei Eingang aktualisieren, aber **Bestand bei Abholung aktualisieren** auf **Nein** gesetzt haben (Übertrag von RiF zum Bestand) Mit dieser Option können Sie beliebige Produkte aus einem Produktionsfluss empfangen, unabhängig von der Stücklisten- und Arbeitsplankonfiguration. Der Prozess folgt derzeit dem physischen Fluss. Diese Option ist besonders geeignet für den Erhalt von Nebenprodukten, Co-Produkten oder Teilen aus dem Produktionsfluss und für das korrigieren von Kostensalden im entsprechenden RIF-Produktionsfluss.

Produkte, die vom Produktionsfluss empfangen werden, werden vom RIF zu den Standardkosten abgezogen.

## <a name="products-in-wip"></a>Produkte in RIF
Mit dem RIF-Modell von Lean Manufacturing können Sie den Kanbanstatus der Handhabungseinheit verwenden, um das Material, die Halbfertigprodukte und Produkte, die Teil von RIF sind, zu verwalten.

-   **Zugewiesen** - Der Kanban kann Material verbraucht haben, das in RIF berechnet wird.
-   **Eingegangen** -, Wenn das Kanban sich auf eine letzte Aktivität bezieht, in der **Aktualisierungsbestand bei Empfang** auf **Nein** festgelegt ist, stellt er eine volle Handhabungseinheit eines Produkts oder des Halbfertig-Produdukts dar, das nicht dem Lager erfasst wird.

Beachten Sie, dass Material in RIF nicht in den Lagerbestandsüberblicken sichtbar ist. Es wird allerdings in den Kanban-Mengenübersichten angezeigt.

## <a name="consuming-products-in-wip"></a>Verbrauch von Produkten in RIF
Produkte in RIF werden verbraucht, wenn die entsprechenden Kanbanhandhabungseinheiten geleert werden. Ein leeres Kanban-Signal produziert keine aktive Nachkalkulationsbuchung, hat aber Wirkung, wenn die nächste Nachkalkulation für Produktionskosten ausgeführt wird. Geleerte Kanbanhandhabungseinheiten werden nicht als an Lager berechnet und werden daher in der Periode als verbraucht berechnet.

### <a name="automatic-empty-registration"></a>Automatische Leererfassung

Geplante Kanban-Regeln oder Ereignis-Kanbans können auf automatische leere Erfassung in der Kanban-Regel festgelegt werden:

-   **Wenn Handhabungseinheiten empfangen werden** - Standardmäßig, für geplante Kanbans, wird das Material als verbraucht deklariert, wenn der letzte Einzelvorgang des Kanbans abgeschlossen ist. Für feste Kanban-Mengen wird diese Option nur für Einzel-Lagerfachkanbane empfohlen, da sie die Karte mit der Bedarfsquelle zurückgibt, wenn ein Kanban am endgültigen Bestimmungsort eingeht.
-   **Wenn Quellanforderung erfasst wird** - Diese Option ist nur verfügbar für Ereignis-Kanbans und ist die Standardeinstellung. In Verbindung mit RIF ist diese Option zum Führen von RIF gut, da Kanbans für Komponenten in RIF automatisch geleert werden und daher von RIF verbraucht werden, wenn der übergeordnete Kanban vorbereitet wird.

Als Schlußfolgerung können Kanbanhandhabungseinheiten zugewiesen (=in Bearbeitung), eingegangene (=voll) oder geleert werden. Es gilt keine teilweise Leerung. Um eine genaue Erfassung des Verbrauchs zu aktivieren, ist es wichtig, dass Sie die Produktmengen eines Kanbans begrenzen, damit diese kleiner sind als der Verbrauch pro Periode. Produkte, die im Fertigungsbereich in großen Chargen verschoben werden, die Tagen oder Wochen des Bedarfs abdecken, dürfen nicht für RIF verbraucht werden. Stattdessen sollten diese Produkte im Lager aufbewahrt werden.

## <a name="backflush-costing"></a>Nachkalkulation für Produktionskosten
Sie sollten Nachkalkulationen in regelmäßigen Abständen ausführten, um den Wert des RIF zu überprüfen und einen Periodenstatus produzieren, der die Abweichungen des Material, Personal und der indirekten Kosten berechnet. Die berechneten Abweichungen werden in den Abweichungskonten gebucht. Im Nachkalkulations-Proezss werden alle Produktionsflüsse der juristischen Person in derselben Batchausführung verwendet. Wenn eine Nachkalkulation als Charge ausgeführt wird, kann die Verarbeitung mehrfädig nach Produktionsfluss sein. Die Nachkalkulationsperiode wird von einem Enddatum definiert. Sie können neue Buchungen nicht auf ein Datum buchen, wenn eine Nachkalkulation ausgeführt wurde. Sie sollten nie eine Nachkalkulationen für Produktionskosten für das aktuelle Datum ausführen, bevor der tag vorüber ist. Nachkalkulation für Produktionskosten führt die folgenden Schritte aus.

1.  Ermittelt die nicht verwendeten Mengen im Produktionsfluss vor dem Enddatum der Periode. Nachdem die Nachkalkulation für Produktionskosten ausgeführt ist, können Sie die nicht verwendeten Mengen bei der Vergabe der Nachkalkulation anzeigen, die im Dialogfeld **Ungenutzte Mengen** ausgeführt wird.
2.  Berechnet die realisierte Verwendung des Produktionsfluss-Netzwerk zu den Zeitraum.
3.  Deaktivieren Sie den RIF vom realisierten Ressourcenverbrauch und von den Produkten.
4.  Berechnen Sie die Produktionsabweichungen zu den Standardkosten für die Periode. **Für verbrauchte Komponenten während der Periode:**
    -   Aktualisieren Sie eine wertmäßige Aktualisierung der realisierten Materialmenge, die der Produktionsfluss für den Zeitraum benötigte. Das System verarbeitet den First-In, First-Out (FIFO) Auftrag, in den individuellen Bestandtransaktionen, um die  physisch aktualisierten Buchungen für den Produktionsfluss, bis die realisierten Netto-Mengen für die Periode erreicht sind.
    -   Buchungen werden wertmäßig aufgeteilt, um die genaue verbrauchte Mengen zuzuordnen.
    -   Ungenutzte Mengen im Produktionsfluss RIF verbleiben im physisch aktualisierten Status.

    **Beim Produktionserfassungstyp abgeschlossene Periode der Mengen:**
    -   Aktualisieren Sie Lagerbuchungen die wertmäßig für die abgeschlossenen Mengen für die Periode.

    **Für die Verarbeitungskosten:**
    -   Die angewendeten Verarbeitungskosten (Arbeitsplanbuchungen), die während der Periode erfasst wurden, werden wertmäßig aktualisiert.
    -   Alle direkten Herstellkosten werden wertmäßig aktualisiert. Alle Kanbanbearbeitungs-Einzelvorgänge, die für die Periode abgeschlossen sind, werden kumuliert.
    -   Alle indirekten Kosten, die für das verbrauchte Material innerhalb der Periode berechnet werden, sind von RIF kalkuliert und abgezogen. Die verbleibenden indirekten Kosten werden als Abweichung gebucht.

5.  Berechnen Sie die Produktionsabweichungen zu den Standardkosten. Die Abweichung wird basierend pro Kostengruppe berechnet.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]