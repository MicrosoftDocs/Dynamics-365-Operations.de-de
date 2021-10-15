---
title: Operations-Ressourcen
description: Betriebliche Ressourcen führen die Aktivitäten eines Projekts oder eines Produktionsprozesses aus. Sie können unterschiedlicher Art sein und verschiedene Funktionen haben.
author: johanhoffmann
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifecycleManagementWorkspace, WrkCtrCapability, WrkCtrResourceGroup, WrkCtrResourceAbilityMap, OpResCapacityPlanningWorkspace, WrkCtrCapResGraph, WrkCtrResourceRequirementPart, WrkCtrCapResGraphDialog, WrkCtrResourceCopy, WrkCtrCapResStatistic
audience: Application User
ms.reviewer: kamaybac
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9296ea874acece9af6be58ccfe777f8713a4d279
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566718"
---
# <a name="operations-resources"></a>Operations-Ressourcen

[!include [banner](../includes/banner.md)]

Betriebliche Ressourcen führen die Aktivitäten eines Projekts oder eines Produktionsprozesses aus. Sie können unterschiedlicher Art sein und verschiedene Funktionen haben. 

## <a name="operations-resources"></a>Operations-Ressourcen

Als betriebliche Ressourcen werden die Maschinen, Werkzeuge, Arbeitskräfte, Einrichtungen, physische Bereiche oder Kreditoren bezeichnet, die die Aktivitäten des Projekts oder des Produktionsprozesses ausführen. Sie können unterschiedlicher Arten sein und verschiedene Funktionen haben.

-   **Anbieter** – Eine externe Ressource, die die Projektaktivitäten oder Produktionsarbeitsgänge ausführt. Beispiel: Ein Zulieferer. Sie können Bestellungen für Zulieferer auf Grundlage von Stücklistenpositionen oder Produktionspositionen generiert, indem sie die Kreditorenressourcen mit einem Kreditorenkonto verknüpfen.
-   **Personalverwaltung** - Eine Projekt- oder Produktionsarbeitskraft, die eine Aktivität, entweder allein oder als Operator eines Tools oder einer Maschine ausführt. Wenn Sie die Personalfunktionen verwenden, können Sie die Personalverwaltung mit einer Arbeitskraft verknüpfen. Das Planungsmodul kann dann die Ressourcen, basierend auf den Kompetenzen, die für die entsprechende Arbeitskraft definiert werden, zuweisen.
-   **Maschine** - Eine Maschine oder anderes Produktionsarbeitsgerät, das für die Produktion benötigt wird.
-   **Werkzeug** - Ein Instrument oder Gerät, das üblicherweise zusammen mit einer anderen Ressource benötigt wird, um eine Aktivität in einem Projekt oder in der Produktion auszuführen.
-   **Lagerplatz** - Ein physischer Standort einer bestimmten Größe, der erforderlich ist, um eine Aktivität auszuführen. Beispiel: Ein Montagebereich.
-   **Einrichtung** - Ein Gebäude oder eine feste Struktur, die erforderlich ist, um eine Aktivität auszuführen.

## <a name="calendars"></a>Kalender
Ein Kalender kann einer betrieblichen Ressource zugewiesen werden und beschreibt die Kapazität dieser Ressource (in Stunden). Die Arbeitszeiten der betrieblichen Ressource werden anhand des Kalenders bestimmt, der der Ressourcengruppe zugewiesen ist, der die betriebliche Ressource angehört. Sie können ein Gültigkeits- und ein Ablaufdatum für den zugewiesenen Kalender festlegen. Danach können Sie mehrere Kalender einer betrieblichen Ressource zuweisen. Allerdings dürfen sich die Datumsangaben der zugewiesenen Kalender nicht überschneiden, und die betriebliche Ressource kann nur jeweils einem Kalender zugewiesen werden. **Hinweis:** Wenn für eine Ressourcengruppe keine gültigen Arbeitszeitkalender vorliegen (z. B., wenn der zuletzt zugewiesene Kalender oder der einzige zugewiesene Kalender abgelaufen ist), können Sie für die Produktionsplanung und die Grobterminierung nicht mehr auf die Ressourcen zugreifen, die der Ressourcengruppe zugewiesen sind. Sie können ebenfalls einen Kalender einer Ressourcengruppe zuweisen, um die Arbeitszeiten für die Ressourcengruppe und alle betrieblichen Ressourcen anzugeben, die der Ressourcengruppe zugewiesen sind. Die Kapazität der Ressourcengruppe ist die Summe der Kapazitäten jeder betrieblichen Ressource, die dieser Ressourcengruppe zugewiesen ist. Der Kalender, der einer Ressourcengruppe zugewiesen ist, kann im Laufe der Zeit geändert werden.

## <a name="resource-capabilities"></a>Ressourcenfähigkeiten
Eine Funktion ist die Fähigkeit einer betrieblichen Ressource, eine bestimmte Aktivität auszuführen. Sie können eine oder mehrere Funktionen einer betrieblichen Ressource zuweisen. Das Planungsmodul weist dann Ressourcen zu, indem die Ressourcenanforderungen jeder Aktivität mit den Funktionen der verfügbaren betrieblichen Ressourcen abgeglichen werden. Funktionen können allen Typen von betriebliche Ressourcen zugewiesen werden(**Werkzeug**, **Anbieter**, **Maschine**, **Personalverwaltung**, **Lagerplatz** oder **Einrichtung**). Um Funktionen den betrieblichen Ressourcen für einen begrenzten Zeitraum zuzuweisen, definieren Sie in der Funktionszuweisung ein Startdatum und Enddatum. Weitere Informationen finden Sie unter [Ressourcenfunktionen](resource-capabilities.md).

## <a name="resource-groups"></a>Ressourcengruppen
Eine Ressourcengruppe ist ein Satz betrieblicher Ressourcen, der die Granularität darstellt, an der Sie Ressourcen planen möchten, wenn Sie die Grobterminierungsmethode verwenden. Aus diesem Grund entsprechen Ressourcengruppen in der Regel der physischen Organisation von Arbeitsgruppen, die durch gelbe Positionen in der Zeiterfassung definiert sind. Die Ressourcengruppe definiert den Standort-, Produktionseinheits- und Lagerortkontext für betriebliche Ressourcen, die der Gruppe zugewiesen sind. Wenn Sie eine betriebliche Ressource einer Ressourcengruppe zuweisen, kann die Ressource an dem Standort eingeplant werden, an dem sich die Ressourcengruppe befindet. Die betriebliche Ressource, die Sie in einer Ressourcengruppe erstellt haben, müssen keiner Ressourcengruppe mehr zugewiesen werden. Eine betriebliche Ressource muss jedoch einer Ressourcengruppe zugewiesen sein, bevor sie zur Ausführung von Arbeit eingeplant werden kann. Eine betriebliche Ressource kann einer Ressourcengruppe für eine begrenzte Zeit zugewiesen werden. Sie können eine betriebliche Ressource auch mehreren Ressourcengruppen zuweisen, damit die Ressource standortübergreifend verwendet werden kann. Allerdings dürfen sich die Gültigkeits- und Ablaufdaten nicht überschneiden. Das bedeutet, Sie können eine betriebliche Ressource nicht gleichzeitig zwei verschiedenen Ressourcengruppen zuweisen. Änderungen in den Gruppenzuweisungen für betriebliche Ressourcen sind nur für neue Ressourcenzuordnungen effektiv. Kapazitätsreservierungen für Einzelvorgänge, Arbeitsgänge und Projektstundenplanungen, die bereits geplant wurden, sind nicht betroffen. **Hinweis:** Wenn Sie einer betrieblichen Ressource vom Typ **Anbieter** eine Ressourcengruppe zuweisen, müssen alle betrieblichen Ressourcen, die dieser Ressourcengruppe zugewiesen werden, vom Typ **Anbieter** sein und mit dem gleichen Kreditorenkonto verknüpft werden.

## <a name="production-units"></a>Produktionseinheiten
Bei einer Produktionseinheit handelt es sich um eine Verwaltungseinheit – genauer gesagt um eine Sammlung von Ressourcengruppen. Eine Produktionseinheit kann zwar mehrere Ressourcengruppen enthalten, eine Ressourcengruppe kann jedoch immer nur jeweils einer Produktionseinheit zugewiesen sein. Produktionseinheiten stehen für das physische Layout von Produktionsressourcen und haben keinerlei Auswirkungen auf Transaktionen oder deren Verarbeitung. Eine Produktionseinheit muss einem Standort zugeordnet werden. Außerdem können einer Produktionseinheit ein Lagerort für die Entnahme sowie ein Lagerort für die Lagerung zugewiesen werden. Mithilfe einer Produktionseinheit lassen sich produktionsbezogene Daten konsolidieren und filtern. So steht beispielsweise einem Manager für "Zeiterfassung/BDE" eine praktische Übersicht über die Arbeitsauslastung und die verfügbare Kapazität einer bestimmten Produktionseinheit zur Verfügung. Die Produktionseinheit, die einer Ressource zugewiesen ist, kann geändert werden. Des Weiteren besteht die Möglichkeit zum Löschen einer Produktionseinheit. Diese Änderungen an der Produktionseinheit gelten jedoch nur für neue Aufträge, die nach der Ausführung der Produktprogrammplanung erstellt werden. Soll die Änderung der Produktionseinheit auf bereits vorhandene Aufträge angewendet werden, muss die Änderung manuell erfolgen.

## <a name="resource-scheduling"></a>Ressourcenplanung
Betriebliche Ressourcen werden den Aktivitäten zugeordnet, wenn ein Projekt oder eine Produktion geplant wird. Zwei Planungsmethoden sind verfügbar: Grobterminierung und Feinterminierung. Wenn die Grobterminierung verwendet wird, wird jeder Arbeitsgang oder Projektaktivität in der Ressourcengruppe geplant, die die betrieblichen Ressourcen enthält, die mit den, für den Arbeitsgang angegebenen, Ressourcenanforderungen übereinstimmen. Wenn eine bestimmte betriebliche Ressource für den Arbeitsgang erforderlich ist, reserviert die Planung Kapazitäten nur für die bestimmte betriebliche Ressource in der Gruppe. Die Feinterminierung ist eine ausführlichere Form der Planung als die Grobterminierung. Jeder Arbeitsgang wird dabei in einzelne Aufgaben oder Einzelvorgänge aufgelöst. Diese Einzelvorgänge werden dann den betrieblichen Ressourcen zugewiesen, die sie ausführen. Die Terminierung reserviert Kapazität für die Ressourcengruppen anhand der Arbeitszeit, die im Produktionsarbeitsplan oder den Projektaktivitäten definiert ist. Wenn Sie mit begrenzter Kapazität arbeiten, hängt der Zeitplan von der Verfügbarkeit der betrieblichen Ressourcen ab, die zum Abschluss der Produktion erforderlich sind. Bei der Grobterminierung ist die Kapazität der Ressourcengruppe die Summe der verfügbaren Kapazitäten der betrieblichen Ressourcen, die Teil dieser Gruppe sind. Kapazitätsreservierungen, die bereits für die betrieblichen Ressourcen vorhanden sind, werden als nicht verfügbare Kapazität betrachtet. Falls die verfügbare Kapazität für die Produktion nicht ausreichend ist, können die Produktionsaufträge verzögert oder auch angehalten werden. Auf der **Ressourcen** Seite können Sie mehrere Eigenschaften definieren, mit denen gesteuert wird, wie Kapazitätsreservierungen vorgenommen werden:

-   **Kapazität** - Geben Sie die Kapazität der betrieblichen Ressource pro Stunde in Bezug auf die Kapazitätsmaßeinheit an.
-   **Stapelverarbeitungskapazität** – Geben Sie die maximale Stückzahl an, die von der betrieblichen Ressource pro Ausführung bearbeitet werden kann.
-   **Effizienzgrad** – Geben Sie die Effizienz an, die Sie von der betrieblichen Ressource erwarten. Mit dem Effizienzgrad wird der Durchsatz einer betrieblichen Ressource angepasst und er wirkt sich somit auch auf die für die Ressource reservierte Zeit aus. Die Lieferzeiten für die Arbeitsgänge, die die betriebliche Ressource verwenden, werden ebenfalls entsprechend angepasst. Dies ist die Formel, die für die Berechnung verwendet wird: Planungszeit = Zeit × 100 ÷ Effizienzgrad. *Zeit* beinhaltet sowohl die Ausführungszeit als auch die Rüstzeit.
-   **Grobterminierungsprozentsatz** – Geben Sie den maximalen Prozentsatz der Kapazität der betrieblichen Ressource an, die sie für die Grobterminierung verwenden möchten. Damit die Kapazität in der Feinterminierung flexibel geplant werden kann, sollte dieser Wert weniger als 100 Prozent betragen.
-   **Begrenzte Kapazität** – Legen Sie diese Option auf **Ja** fest, wenn die betriebliche Ressource auf Basis der tatsächlich verfügbaren Kapazität geplant und wenn vorhandene Kapazitätsreservierungen berücksichtigt werden sollen. Wenn die Option auf **Nein** festgelegt ist, wird angenommen, dass die betriebliche Ressource unbegrenzte Kapazität hat, und die Ressource kann möglicherweise überbucht werden.
-   **Begrenzte Eigenschaft** - Legen Sie diese Option auf Kapazität **Ja** fest, wenn die betriebliche Ressource basierend auf der aktuellen Kapazität geplant werden soll, die in Bezug auf die erforderlichen Arbeitszeitplanungseigenschaften verfügbar ist.
-   **Exklusiv** – Aktivieren Sie das Kontrollkästchen **Ja**, wenn die Ressource erst dann für einen anderen Einzelvorgang oder Arbeitsgang eingesetzt werden soll, wenn die aktuelle Produktion abgeschlossen ist. In diesem Fall bedeutet es, dass die Ressource auch dann nicht anderweitig eingesetzt werden kann, wenn hierdurch Lücken in der Laufzeit der Ressource entstehen.
-   **Engpassressource** - Definieren Sie die betriebliche Ressource als Engpassressource. Eine Engpassressource wird mit begrenzter Kapazität geplant, wenn die Felder **Begrenzte Kapazität** und **Engpassplanung** auf der Seite **Produktprogrammpläne** ausgewählt sind.

Um die Ausführung mehrerer betrieblicher Ressourcen gleichzeitig zur planen, z. B. einen Arbeitsgang in der Produktion, müssen Sie die Anforderungen für die verschiedenen Ressourcen angeben, indem Sie primäre und sekundäre Arbeitsgänge verwenden. Sie können dann auch mehrere betriebliche Ressourcen mit unterschiedlichen Kapazitäten reservieren. Die betriebliche Ressource, die für den primären Arbeitsgang geplant wurde, bestimmt die Dauer der Aktivität.

## <a name="lean-work-cells"></a>Lean-Arbeitsgruppe
Sie können eine Ressourcengruppe als Lean-Arbeitsgruppe angeben. Die Ressourcengruppe kann dann Teil eines Produktionsflusses sein. Wenn Sie eine Ressourcengruppe als Lean-Arbeitsgruppe angeben, verhindern Sie auch, dass die Ressourcengruppe und die zugewiesenen betrieblichen Ressourcen den Arbeitsgängen eines Produktionsauftrags oder der Projektstundenplanung zugeordnet werden. Für jede Ressourcengruppe, die als Lean-Arbeitsgruppe handelt, müssen Sie die folgenden Informationen angeben:

-   **Kalender** - Der Arbeitskalender der Arbeitsgruppe, der die Eigenschaft eines Standardarbeitstags besitzen muss.
-   **Eingangslagerort und -lagerplatz** - Der Standardspeicherort, der verwendet wird, um Material für eine Aktivität zu entnehmen.
-   **Ausgangslagerort und - lagerplatz** - Der Standardspeicherort, der als Ausgangslager der Arbeitsgruppe dient.
-   **Laufzeitkostenkategorie** - Diese Kategorie muss für die Arbeitsgruppe definiert werden, wenn direkte Arbeitskosten in der Nachkalkulation verfolgt werden.

Wenn eine Ressourcengruppe als Lean-Arbeitsgruppe verwendet wird, wird die Kapazität der Arbeitsgruppe direkt in der Ressourcengruppe angegeben. Aus diesem Grund dürfen Sie die betrieblichen Ressourcen nicht einer Ressourcengruppe zuweisen. Nur wenn die Arbeitsgruppe von einem Zulieferer verwaltet wird, muss eine betriebliche Ressource vom Typ **Anbieter** der Arbeitsgruppe zugewiesen werden. Wenn Sie eine betriebliche Ressource einer Ressourcengruppe zuweisen, die als Arbeitsgruppe markiert wurde, ist die Kapazität der Arbeitsgruppe nicht betroffen.

## <a name="costing-resources"></a>Nachkalkulationsressourcen
Wenn Sie eine Aktivität wie einen Arbeitsplan-Arbeitsgang oder eine Projektstundenplanung definieren, können Sie die Anforderung für eine bestimmte betriebliche Ressourcen oder -Ressourcengruppe angeben. Sie können jedoch auch die Anforderung für eine betriebliche Ressource eines bestimmten Typs oder einer betrieblichen Ressource mit einer bestimmten Funktion oder Kompetenz angeben. Aus diesem Grund wird die tatsächliche Ressourcenzuweisung nicht getätigt, bis die Aktivität geplant ist und die Kapazität reserviert ist. Daher können Sie auf einem Arbeitsplan-Arbeitsgang angeben, dass Vorkalkulation und Herstellkostenkalkulation auf Basis einer Einzelgeschäftressource erfolgen müssen. Diese betriebliche Ressource wird als Nachkalkulationsressource bezeichnet. Sie können Kostenkategorien und Arbeitsgangzeiten aus der Nachkalkulationsressource zur Aktivität übertragen. Wenn der Arbeitsgang geplant wird, werden Vorkalkulation und Stücklistenberechnung unter Verwendung der tatsächlich geplanten betrieblichen Ressource erstellt.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]