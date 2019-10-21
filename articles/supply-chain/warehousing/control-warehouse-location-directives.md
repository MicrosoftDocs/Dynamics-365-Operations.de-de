---
title: Steuern von Lagerarbeit, indem Sie Arbeitsvorlagen und Lagerplatzrichtlinien verwenden
description: In diesem Thema wird beschrieben, wie Arbeitsvorlagen und Lagerplatzrichtlinien verwendet werden, um festzustellen wie und wo Arbeit am Lagerort ausgeführt wird.
author: perlynne
manager: AnnBe
ms.date: 09/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirFailure, WHSLocDirHint, WHSLocDirTable, WHSLocDirTableUOM, WHSRFMenuItem, WHSWork, WHSWorkClass, WHSWorkPool, WHSWorkTemplateTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72921
ms.assetid: 377ab8af-5b0c-4b5e-a387-06ac1e1820c0
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9a5292e88fe022482ab9c6c5a8f016745946988
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2026928"
---
# <a name="control-warehouse-work-by-using-work-templates-and-location-directives"></a>Steuern von Lagerarbeit, indem Sie Arbeitsvorlagen und Lagerplatzrichtlinien verwenden

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Arbeitsvorlagen und Lagerplatzrichtlinien verwendet werden, um festzustellen wie und wo Arbeit am Lagerort ausgeführt wird.

Die Anweisungen, die Lagerarbeiter auf einem mobilen Gerät erhalten, werden durch die Arbeitsvorlagen bestimmt, die Sie in Dynamics 365 Supply Chain Management-Arbeitsvorlagen einrichten, um die verschiedenen Lagerortprozesse und -aufgaben zu definieren. Arbeitsvorlagen bestimmen, wie die Arbeit für jeden Lagerortprozess ausgeführt wird. Wenn Sie eine Lagerplatzrichtlinie mit Arbeitsvorlagen verknüpfen, können Sie sicherstellen, dass Arbeit in bestimmten physischen Bereichen der Lagerorte erfolgt.

## <a name="work-templates"></a>Arbeitsvorlagen
Auf der Seite **Arbeitsvorlagen** können Sie die Arbeitsvorgänge definieren, die am Lagerort ausgeführt werden müssen. In der Regel bestehen Lagerortarbeitsvorgänge aus folgenden Aktivitäten: Ein Lagerarbeiter entnimmt verfügbaren Lagerbestand an einem Lagerplatz und legt anschließend den entnommenen Bestand an einem anderen Lagerplatz ab. 

Arbeitsvorlagen bestehen aus einem Kopf und aus zugeordneten Positionen. Jede Arbeitsvorlage ist für einen bestimmten *Arbeitsauftragstyp* bestimmt. Viele Arbeitsauftragstypen werden Quelldokumenten, wie Bestellungen oder Aufträgen, zugeordnet. Jedoch stellen andere Arbeitsauftragstypen separate Lagerortprozesse, wie Zykluszählung, dar. Mithilfe der *Arbeitspool-IDs* können Sie die Arbeit in Gruppen organisieren. 

Die Einstellungen in der Arbeitskopfdefinition können verwendet werden, um festzustellen, wann eine neue Arbeit erstellt werden soll. So können Sie beispielsweise eine maximale Anzahl Entnahmepositionen und maximale erwartete Entnahmezeit festlegen. Überscheitet die Arbeit für einen Auftragskommissionierungsprozess einen dieser Werte, wird diese Arbeit in zwei Arbeiten geteilt. 

Die Arbeitspositionen stellen die physischen Aufgaben dar, die erforderlich sind, um die Arbeit zu verarbeiten. Für einen ausgehenden Lagerortprozess gibt es möglicherweise eine Arbeitsposition für die Artikelentnahme im Lagerort und eine andere Position für das Liefern dieser Artikel an einen Stagingbereich. Es kann als Teil des Ladevorgangs eine weitere Position für die Entnahme der Artikel vom Stagingbereich geben und eine andere Position für das Verladen der Artikel auf einen LKW. Sie können einen *Richtliniencode* für Arbeitsvorlagenpositionen festlegen. Ein Richtliniencode wird mit einer Lagerplatzrichtlinie verknüpft und stellt daher sicher, dass die Lagerortarbeit am richtigen Lagerplatz am Lagerort verarbeitet wird. 

Sie können eine Abfrage einrichten, um zu steuern, wann eine bestimmte Arbeitsvorlage verwendet wird. So können Sie eine Einschränkung festlegen, damit eine bestimmte Vorlage für Arbeit nur in einem bestimmten Lagerort verwendet werden kann. Alternativ haben Sie möglicherweise einige Vorlagen, die verwendet werden, um Arbeit für den ausgehenden Auftrag zu erstellen, abhängig von der Auftragsgrundlage. Das System verwendet das Feld **Laufende Nummer**, um den Auftrag zu bestimmen, in der die verfügbaren Lagerplatzdirektiven anfallen. Wenn Sie daher eine einzelne Frage für eine bestimmte Arbeitsvorlage haben, müssen Sie ihnen eine niedrige laufende Nummer eingeben. Diese Abfrage wird dann vor den anderen allgemeineren Abfragen ausgewertet. 

Um einen Arbeitsprozess zu beenden oder anzuhalten, können Sie die Einstellung **Arbeit anhalten** für die Arbeitsposition verwenden. In diesem Fall wird die Arbeitskraft, die die Arbeit ausführt, aufgefordert, den folgenden Arbeitspositionsschritt nicht auszuführen. Um mit dem nächsten Schritt fortzufahren, muss diese Arbeitskraft oder eine andere Arbeitskraft für die Arbeit wieder ausgewählt werden. Sie können die Aufgaben innerhalb einer Arbeit auch trennen, indem Sie ein andere *Arbeitsklassen-ID* für die Arbeitsvorlagenpositionen verwenden.

## <a name="location-directives"></a>Lagerplatzrichtlinien
Lagerplatzrichtlinien sind Regeln, die dabei helfen, Entnahme- und Einlagerungslagerorte für die Lagerumlagerung zu identifizieren. In einer Auftragsbuchung bestimmt eine Lagerplatzrichtlinie z. B., wo die Artikel entnommen und wo die entnommenen Artikel eingelagert werden. Lagerplatzrichtlinien bestehen aus einem Kopf und aus zugeordneten Positionen, und Sie erstellen sie auf der Seite **Lagerplatzrichtlinien**. 

Im Kopf muss jede Lagerplatzrichtlinie einem *Arbeitsauftragstyp* zugeordnet werden, der den Typ der Lagerbuchung angibt, für den die Richtlinie verwendet wird, wie Aufträge, Auffüllung oder Rohmaterialentnahme. Der *Arbeitstyp* gibt an, ob die Lagerplatzrichtlinie für die Entnahme oder die Lagerung der Arbeit verwendet wird oder für einen anderen Lagerortprozess, wie Inventur oder Bestandsstatusänderungen. Sie müssen auch einen *Standort* und einen *Lagerort* angeben. Ein *Richtliniencode*, den Sie im Kopf angeben, kann verwendet werden, um die Lagerplatzrichtlinie an eine oder mehrere Arbeitsvorlagen zu knüpfen. 

Was Arbeitsvorlagen angeht, können Sie eine Abfrage einrichten, um festzustellen, wann eine bestimmte Lagerplatzrichtlinie verwendet wird. Beispielsweise können Sie angeben, dass, wenn E-Commerce der Ursprung eines Auftrags ist, der Bestand aus einem dediziertem Bereich des Lagerorts abgeholt werden muss. Das System verwendet das Feld **Laufende Nummer**, um den Auftrag zu bestimmen, in der die verfügbaren Lagerplatzdirektiven anfallen. 

Die richtungweisenden Positionen des Lagerplatzes setzen zusätzliche Einschränkungen für die Anwendung für die Regel für das Auffinden des Lagerplatzes fest. Sie können eine minimale Menge und eine maximale Menge angeben, für die die Richtlinie gelten soll, und Sie können angeben, dass die Richtlinie für eine bestimmte Lagereinheit sein soll. Wenn beispielsweise die Maßeinheit Paletten ist, können Artikel auf Paletten an einem bestimmten Lagerplatz eingelagert werden. Sie können auch angeben, ob die Menge über mehrere Lagerplätze verteilt werden kann. Wie der richtungweisende Kopf des Lagerplatzes hat jede richtungweisende Position des Lagerplatzes eine laufende Nummer, die die Reihenfolge bestimmt, in der die Positionen bewertet werden. 

Lagerplatzdirektive haben eine zusätzliche Genauigkeitsebene: *Lagerplatzdirektivenaktivitäten*. Sie können Lagerplatzrichtlinien-Aktivitäten für jede Position definieren. Erläuternd, eine laufende Nummer wird verwendet, um die Reihenfolge festzulegen, in der die Aktivitäten anfallen. Auf dieser Ebene können Sie eine Abfrage einrichten, um festzulegen, wo sich der optimale Lagerplatz am Lagerort befindet. Sie können auch vordefinierte **Strategieeinstellungen** verwenden, um einen optimalen Lagerplatz zu finden.

## <a name="location-directives-configuration-details"></a>Lagerplatzdirektiven-Konfigurationsdetails 

 ### <a name="sequence-number"></a>Laufende Nummer
 
Diese Zahl zeigt die Reihenfolge ein, in der die Lagerplatzrichtlinie für den ausgewählten Arbeitstyp verarbeitet werden soll. Sie kann mit **Nach oben** und **Nach unten** im Menü geändert werden.
 
 ### <a name="work-type"></a>Arbeitstyp
 
Wählen Sie die Art der auszuführenden Arbeit aus. Der verfügbare Arbeitstyp basiert auf dem Typ der Lagerbuchungstransaktion, die Sie im Feld **Arbeitsauftragstyp** ausgewählt haben.
-   **Gesetzt** Arbeitstyp ist gleich **Gesetzt** bedeutet, dass die Lagerplatzdirektive den besten Lagerplatz suchen wird, um den Bestand zu platzieren oder zu suchen, der im System entweder von Eingang, Produktion oder Lagerregulierungen stammt. Er kann auch verwendet werden, um einen Put für einen vorübergehenden Lagerplatz oder einen endgültigen Versandort zu definieren.
-   **Entnahme** Arbeitstyp -ist gleich **Entnahme** bedeutet, dass der Lagerort den idealsten den Speicherort finden wird, um physischen Lagerbestand zu reservieren (Arbeit erstellen). Die Entnahme kann abgeschlossen werden (Entnahmearbeitsposition kann geschlossen werden), selbst wenn die Arbeit nicht abgeschlossen ist. Der Benutzer kann physische Entnahme beenden, was ein Entnahmeschritt ist. Der Benutzer kann dann die Arbeit auf einem mobilen Gerät abbrechen und später abschließen. Allerdings wird der Arbeitskopf geschlossen, wenn die letzte Einlagerung geschlossen wurde. 
-    **Inventur, Regulierungen, benutzerdefiniert, Bestandsstatusänderung, Kfz-Kennzeichen-Gebäude, Drucken, Statusänderung, zu geschachtelten Kfz-Kennzeichen packen** - Das sind keine verwendbaren  Lagerplatzdirektiveneinstellungen. Dies ist eine Enumeration, deshalb sind keine Filter mit dem Arbeitsauftragstyp verbunden. 

### <a name="directive-code"></a>Richtliniencode

Wählen Sie den Richtliniencode aus, der einer Arbeitsvorlage oder der Auffüllungsvorlage zuzuordnen ist. Im Formular **Richtungweisender Code** können Sie neue Codes erstellen, die für eine Verbindung zwischen einer Arbeitsvorlage-Wiederbeschaffungsvorlage und einer Lagerplatzdirektiven verwendet werden können. Dies kann auch verwendet werden, um die Verknüpfung zwischen sämtlicher Arbeitsvorlagenpositionen und Lagerplatzdirektiven zu erstellen (wie Ladebereichtstor oder Phasenlagerplatz).

Beachten Sie, dass bei festgelegtem Code das System die Lagerplatzdirektive nicht nach Nummernkreis suchen wird, wenn Arbeit erstellt wird, die Suche erfolgt nach Direktivencode. Das bedeutet, dass Sie spezifischer sein können in Bezug auf die Verwendung der Lagerplatzvorlage für einen bestimmten Schritt in einer Arbeitsvorlage, wie die  Bereitstellung von Material. 

### <a name="site"></a>Standort

Standort ist ein Pflichtfeld, da die Lagerplatzdirektive den Standort und der Lagerort ist, das für diese gültig ist. 

### <a name="warehouse"></a>Lagerort

Lagerhaus ist ein Pflichtfeld, da die Lagerplatzdirektive den Standort und der Lagerort ist, das für diese gültig ist.

### <a name="multiple-sku"></a>Mehrfach-SKU

Dies ermöglicht mehrere Lagermengeneinheiten (SKU) an einem Ort, z. B. Ladebereichstor. Wenn Sie **Mehrere SKU** auswählen, wird der Lagerplatz wieder in Arbeit angegeben (die voraussichtliche Arbeit) aber es ist nur möglich, mehrere gesetzten Artikel zu bearbeiten (wenn die Arbeit verschiedenen SKUS umfasst, die entnommen und eingelagert werden, nicht eine einzelne SKU-Einlagerung). Wenn Sie **Mehrere SKU** nicht aktivieren, wird der Einlagerungslagerort nur festgelegt, wenn die Einlagerung nur eine Art SKU hat. Um beide Aktivitäten zu verwenden, müssen Sie zwei Positionen definieren, eine mit mehreren SKUs aktiviert und eine mit mehreren SKUs deaktiviert. Diese müssen die selbe Struktur aufweisen und gleich eingerichtet sein. Für gesetzte Arbeitsgänge müssen Sie Lagerplatzdirektive haben, die übereinstimmen, wenn Sie nicht zwischen den einzelnen und mehreren SKUs in der Arbeits-Kennung unterscheiden Sie müssen außerdem die Entnahme einrichten, wenn Sie einen Auftrag mit mehr als einem Artikel haben.

### <a name="sequence-number"></a>Laufende Nummer

Geben Sie die Reihenfolge ein, in der die Lagerplatzrichtlinie für den ausgewählten Arbeitstyp verarbeitet werden soll. Sie können die Reihenfolge bei Bedarf mithilfe von **Nach oben** und **Nach unten** auch ändern.

### <a name="fromto-quantity"></a>Von/zu Menge

Dies bietet die Möglichkeit, einen Mengenbereich für Zuschläge anzugeben, wenn der mittlere Rasternummernkreis ausgewählt werden soll. Sie können den von/zu Bereich der Menge in der jeweiligen Einheit angeben.

### <a name="unit"></a>Einheit

Sie können eine minimale Menge und eine maximale Menge angeben, für die die Richtlinie gelten soll, und Sie können angeben, dass die Richtlinie für eine bestimmte Lagereinheit sein soll. Das Einheitsfeld für die Position wird nur für Mengenbewertung verwendet.

Beim Prüfen, ob die richtungweisende Position des Lagerplatzes gilt, basiert dies auf der Menge in der betreffenden Einheit in der Lagerplatzdirektivenposition. Beim Buchen einer richtungweisende Position des Lagerplatzes versucht das System, die Bedarfseinheit auf eine Einheit zu konvertieren, die auf der Position angegeben wird. Wenn die UOM-Umrechnung nicht vorhanden ist, wird sie zur nächsten Position springen. 

### <a name="locate-quantity"></a>Menge suchen

Diese Option wird nur verwendet, für eingelagerte/platzierte Mengen am Lagerort. Sie ist nur für den Arbeitstyp gesetzt. Folgende Werte sind gültig:

-   **Ladungsträgermenge** – Beim Auswerten, ob die Menge innerhalb der "von" und "zu" Menge liegt, nutzen Sie die Menge auf dem empfangenen Ladungsträger.
-   **Vereinheitlichte Menge** – Beim Auswerten, ob die Menge innerhalb der "von" und "zu" Menge liegt, nutzen Sie die Menge, die während der bestimmten Transaktion vereinheitlicht wird.
-   **Restliches Menge** – Beim Auswerten, ob die Menge innerhalb des "von" und "zu" Bereichs liegt, nutzen Sie die verbleibende Menge, die von der Bestellposition empfangen wird, die gerade geprüft wird.
-   **Erwartete Menge** – Beim Auswerten, ob die Menge innerhalb des "von" und "zu" Bereichs liegt, nutzen Sie die Gesamtmenge der Bestellposition, unabhängig davon, was Sie empfangen haben.

### <a name="restrict-by-unit"></a>Nach Einheit einschränken

So kann eine Lagerplatzdirektivenposition spezifisch auf eine Maßeinheit oder mehrere Maßeinheiten erstellt werden. Wenn Sie Menge reservieren und Sie nur betimmte Paletten von einer Reihe von Standorten reservieren möchten, dann würde der mittlere Rasternummernkreis diese bestimmte Sequenz zu" PL "einschränken,  sodass eine Menge kleiner als eine Palette nicht den Nummernkreis auswählt. Wählen Sie **Beschränken nach Einheit**, um die Einheiten einzurichten. Sie können die Position für mehr als eine Einheit begrenzen. Dies funktioniert nur mit Lagerplatzdirektiven des Typs Entnahme. 

### <a name="round-up-to-unit"></a>Aufrunden zur Einheit

Dieses Feld arbeitet in Verbindung mit dem Feld **Nach Einheit einschränken** Wenn die Position **Beschränken nach Einheit ein** auf "Feld" festgelegt ist, wählen Sie **Einheit ergänzen** um anzuzeigen, dass die erstellte Arbeit, die ausserhalb der Direktive für Rohmaterialentnahmen liegt, ergänzt werden soll für ein Vielfaches von eine Handhabungseinheit (definiert durch **Beschränken nach Einheit**). Beachten Sie, dass dieses nur für Rohmaterialentnahmen und nur mit Lagerplatzdirektiven der Typentnahme geht.

### <a name="locate-packing-qty"></a>Verpackungsmenge suchen

Wenn eine Verpackungsmenge für einen Auftrag, einen Umlagerungsauftrag oder für einen Produktionsauftrag angegeben ist, kann das System nur Lagerplätze mit einer packenden Menge am Standort auswählen. Dies funktioniert nur mit Lagerplatzdirektiven des Typs Entnahme.

### <a name="allow-split"></a>Aufteilung zulassen

Dies definiert, ob eine Lagerplatzdirektive die eingehende Menge oder die reservierte Menge auf mehrere Lagerortlagerplätzen aufteilen darf oder ob die gesamte Menge an einem einzelnen Ort zugewiesen werden muss oder von einem einzelnen Standort reserviert werden muss, um Arbeit zu erstellen. 

### <a name="sequence-number"></a>Laufende Nummer

Diese Nummer ist die Reihenfolge, in der die Lagerplatzrichtlinie für den ausgewählten Arbeitstyp verarbeitet werden soll. Sie können die Reihenfolge bei Bedarf ändern. Allerdings müssen Sie anhand der laufenden Nummern vorsichtig sein, da die Verarbeitung immer nacheinander ausgeführt wird. 

### <a name="name"></a>Name

Geben Sie einen Namen für die Lagerplatzrichtlinienaktion ein. Stellen Sie sicher, genau zu sein, falls Sie einen Namen angeben.

### <a name="fixed-location-usage"></a>Verwendung fester Lagerplätze 

-   **Feste und nicht feste Lagerplätze** - Die Lagerplatzdirektive berücksichtigt alle Lagerplätze.
-   **Nur feste Lagerplätze für das Produkt** - Die feste Lagerplatzdirektive betrachtet nur Lagerplätze für Produkte.
-   **Nur feste Lagerplätze für die Produktvariante** - Die feste Lagerplatzdirektive betrachtet nur Lagerplätze für Produktvarianten.

### <a name="allow-negative-inventory"></a>Negativen Bestand zulassen

Wählen Sie diese Option, um einen negativen Bestand am angegebenen Lagerort in der Lagerplatzdirektive zu ermöglichen. 

### <a name="batch-enabled"></a>Charge aktiviert 

Aktivieren Sie dieses Kontrollkästchen, um Chargenstrategien für die Artikel zu verwenden, für die Chargen aktiviert sind. Wenn eine Position erreicht wird, bei der **Stapelverarbeitung aktiviert** mit einem Nicht-Chargenartikel festgelegt ist, wird der Prozess auf der nächsten Aktivitätsposition fortgesetzt. 

### <a name="strategy"></a>Strategie

-   **Konsolieriung** . Diese Strategie wird verwendet, um Artikel an einem bestimmten Lagerplatz zu konsolidieren, wenn ähnliche Artikel bereits verfügbar sind. Dies funktioniert nur für den Einlagerungstyp mit der Lagerplatzdirektive. Allgemeine Einstellungen für Einlagerungen ist es, in der ersten Aktivitätsposition zu konsolidieren und dann im zweiten Versuch die Einlagerung ohne Konsolidierung vorzunehmen. Durch Konsolidieren von Waren ist das Buchen effizienter.
-   **Packmenge anpassen** - Diese Strategie wird verwendet, um sicherzustellen, dass ein Entnahmeort die angegebene Verpackungsmenge hat. Dies funktioniert nur für Lagerplatzdirektiven des Typs Entnahme. 
-   **FEFO-Chargenreservierung** - Diese Strategie wird verwendet, wenn Bestand mithilfe eines Chargenablaufdatums zur Chargenreservierung zugeordnet wird. Sie können diese Strategie nur für stapelverarbeitungsfähige Artikel verwenden. Dies geht nur für eine Lagerplatzdirektive des Typs Entnahme. 
-   **Auffüllen für eine vollständige LP** - Diese Strategie wird verwendet, um die Bestandsmenge zu runden, sodass sie der Ladungsträgermenge entspricht, die den zu entnehmenden Artikeln zugewiesen ist. Sie können diese Strategie für den Wiederbeschaffungstyp von Lagerplatzdirektiven des Typs Entnahme verwenden. 
-   **Leerer Lagerplatz ohne eingehende Arbeit** -  Diese Strategie wird verwendet, um leere Lagerplätze zu suchen. Der Lagerplatz wird als leer angesehen, wenn dieser keinen physischen Bestand und keine erwartete eingehende Arbeit hat. Diese Strategie wird nur für einen Einlagerungsty der Lagerplatzdirektive verwendet. 

### <a name="example-of-the-use-of-location-directives"></a>Beispiel für die Verwendung von Lagerplatzrichtlinien

Im vorliegenden Beispiel berücksichtigen wir einen Bestellprozess, in dem die Lagerplatzrichtlinie die freie Kapazität innerhalb eines Lagerorts für Lagerartikel finden muss, die gerade an der empfangenden Rampe erfasst wurden. Zuerst müssen Sie die freie Kapazität am Lagerort finden, indem der vorhandene verfügbare Lagerbestand konsolidiert wird. Falls die Konsolidierung nicht möglich ist, wird ein leerer Lagerplatz gesucht. 

Für dieses Szenario müssen zwei Lagerplatzrichtlinien-Aktivitäten definiert werden. Die erste Aktivität in der Folge muss die Strategie **Konsolidieren** verwenden, die zweite sollte die Strategie **Leerer Lagerplatz ohne eingehende Arbeit** verwenden. Wenn Sie keine dritte Aktivität definieren, um ein Überlaufszenario zu behandeln, sind zwei Ergebnisse möglich, wenn es keine Kapazität mehr am Lagerort gibt: Arbeit kann erstellt werden, auch wenn keine Lagerplätze definiert sind, oder der Arbeitserstellungsprozess kann fehlschlagen. Das Ergebnis wird durch die Einstellung auf der Seite **Lagerplatzrichtlinienfehler** bestimmt, auf der Sie entscheiden, ob die Option **Arbeit bei Lagerplatzrichtlinienfehler anhalten** für jeden Arbeitsauftragstyp auswählt wird.
