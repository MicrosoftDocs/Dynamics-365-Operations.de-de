---
title: Steuern von Lagerarbeit, indem Sie Arbeitsvorlagen und Lagerplatzrichtlinien verwenden
description: "In diesem Artikel wird beschrieben, wie Arbeitsvorlagen und Lagerplatzrichtlinien verwendet werden, um festzustellen wie und wo Arbeit am Lagerort ausgeführt wird."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLocDirFailure, WHSLocDirHint, WHSLocDirTable, WHSLocDirTableUOM, WHSRFMenuItem, WHSWork, WHSWorkClass, WHSWorkPool, WHSWorkTemplateTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 72921
ms.assetid: 377ab8af-5b0c-4b5e-a387-06ac1e1820c0
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 269631124e9cab89a85bf4ff6936f3cd5d1dab2a
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="control-warehouse-work-by-using-work-templates-and-location-directives"></a>Steuern von Lagerarbeit, indem Sie Arbeitsvorlagen und Lagerplatzrichtlinien verwenden

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie Arbeitsvorlagen und Lagerplatzrichtlinien verwendet werden, um festzustellen wie und wo Arbeit am Lagerort ausgeführt wird.

Die Anweisungen, die Lagerarbeiter auf einem mobilen Gerät erhalten, werden durch die Arbeitsvorlagen bestimmt, die Sie in Microsoft Dynamics 365 for Finance and Operations einrichten, um die verschiedenen Lagerortprozesse und -aufgaben zu definieren. Arbeitsvorlagen bestimmen, wie die Arbeit für jeden Lagerortprozess ausgeführt wird. Wenn Sie eine Lagerplatzrichtlinie mit Arbeitsvorlagen verknüpfen, können Sie sicherstellen, dass Arbeit in bestimmten physischen Bereichen der Lagerorte erfolgt.

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

### <a name="example-of-the-use-of-location-directives"></a>Beispiel für die Verwendung von Lagerplatzrichtlinien

In vorliegenden Beispiel berücksichtigen wir einen Bestellprozess, in dem die Lagerplatzrichtlinie die freie Kapazität innerhalb eines Lagerorts für Lagerartikel finden muss, die gerade an der empfangenden Rampe erfasst wurden. Zuerst möchten wir versuchen, die freie Kapazität im Lagerort zu finden, indem wir mit vorhandenem verfügbaren Lagerbestand konsolidieren. Wenn die Konsolidierung nicht möglich ist, wird ein leerer Lagerplatz gesucht. 

Für dieses Szenario müssen wir zwei Lagerplatzrichtlinien-Aktivitäten definieren. Die erste Aktivität in der Folge muss die Strategie **Konsolidieren** verwenden, die zweite sollte die Strategie **Leerer Lagerplatz ohne eingehende Arbeit** verwenden. Wenn wir keine dritte Aktivität definieren, um ein Überlaufszenario zu behandeln, sind zwei Ergebnisse möglich, wenn es keine mehr Kapazität am Lagerort gibt: Arbeit kann erstellt werden, auch wenn keine Lagerplätze definiert sind, oder der Arbeitserstellungsprozess kann fehlschlagen. Das Ergebnis wird durch die Einstellung auf der Seite **Lagerplatzrichtlinienfehler** bestimmt, auf der Sie entscheiden, ob die Option **Arbeit bei Lagerplatzrichtlinienfehler anhalten** für jeden Arbeitsauftragstyp auswählt wird.




