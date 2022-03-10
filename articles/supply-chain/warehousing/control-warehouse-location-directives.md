---
title: Steuern von Lagerarbeit, indem Sie Arbeitsvorlagen und Lagerplatzrichtlinien verwenden
description: In diesem Thema wird beschrieben, wie Arbeitsvorlagen und Lagerplatzrichtlinien verwendet werden, um festzustellen wie und wo Arbeit am Lagerort ausgeführt wird.
author: perlynne
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocDirFailure, WHSLocDirHint, WHSLocDirTable, WHSLocDirTableUOM, WHSRFMenuItem, WHSWork, WHSWorkClass, WHSWorkPool, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72921
ms.assetid: 377ab8af-5b0c-4b5e-a387-06ac1e1820c0
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7e955fba12e963a443c0304f0a8a0e395c46909dd34de12cd51fa9788491786
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770143"
---
# <a name="control-warehouse-work-by-using-work-templates-and-location-directives"></a>Steuern von Lagerarbeit, indem Sie Arbeitsvorlagen und Lagerplatzrichtlinien verwenden

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Arbeitsvorlagen und Lagerplatzrichtlinien verwendet werden, um festzustellen wie und wo Arbeit am Lagerort ausgeführt wird.

Die Anweisungen, die Lagerarbeiter auf einem mobilen Gerät erhalten, werden durch die Arbeitsvorlagen bestimmt, die Sie in Dynamics 365 Supply Chain Management-Arbeitsvorlagen einrichten, um die verschiedenen Lagerortprozesse und -aufgaben zu definieren. Arbeitsvorlagen bestimmen, wie die Arbeit für jeden Lagerortprozess ausgeführt wird. Wenn Sie eine Lagerplatzrichtlinie mit Arbeitsvorlagen verknüpfen, können Sie sicherstellen, dass Arbeit in bestimmten physischen Bereichen der Lagerorte erfolgt.

## <a name="work-templates"></a>Arbeitsvorlagen

Auf der Seite **Arbeitsvorlagen** können Sie die Arbeitsvorgänge definieren, die am Lagerort ausgeführt werden müssen. In der Regel bestehen Lagerortarbeitsvorgänge aus folgenden Aktivitäten: Ein Lagerarbeiter entnimmt verfügbaren Lagerbestand an einem Lagerplatz und legt anschließend den entnommenen Bestand an einem anderen Lagerplatz ab. 

Arbeitsvorlagen bestehen aus einem Kopf und aus zugeordneten Positionen. Jede Arbeitsvorlage ist für einen bestimmten *Arbeitsauftragstyp* bestimmt. Viele Arbeitsauftragstypen werden Quelldokumenten, wie Bestellungen oder Aufträgen, zugeordnet. Jedoch stellen andere Arbeitsauftragstypen separate Lagerortprozesse, wie Zykluszählung, dar. Mithilfe der *Arbeitspool-IDs* können Sie die Arbeit in Gruppen organisieren. 

Verwenden Sie die Einstellungen in der Arbeitskopfdefinition, um festzulegen, wann ein neues Stück Arbeit erstellt werden soll. So können Sie beispielsweise eine maximale Anzahl Entnahmepositionen und maximale erwartete Entnahmezeit festlegen. Überscheitet die Arbeit für einen Auftragskommissionierungsprozess einen dieser Werte, wird diese Arbeit in zwei Arbeiten geteilt.

Verwenden Sie die Schaltfläche **Arbeitskopfpausen**, um festzulegen, wann das System neue Arbeitsköpfe erstellen soll. Um z.B. für jede _Auftragsnummer_ einen Arbeitskopf zu erstellen, wählen Sie **Abfrage bearbeiten** im Aktivitätsbereich und fügen dann das Feld **Auftragsnummer** auf der Registerkarte **Sortierung** des Abfrage-Editors hinzu. Felder, die der Registerkarte **Sortierung** hinzugefügt werden, stehen als *Gruppierungsfelder* zur Auswahl. Um Ihre Gruppierungsfelder festzulegen, wählen Sie **Arbeitszeilenunterbrechungen** im Aktivitätsbereich und aktivieren dann für jedes Feld, das Sie als Gruppierungsfeld verwenden wollen, das Kontrollkästchen in der Spalte **Gruppieren nach diesem Feld**.

Die Arbeitszeilen stellen die physischen Aufgaben dar, die zur Bearbeitung der Arbeit erforderlich sind. Zum Beispiel könnte es für einen Ausgangslagerprozess eine Zeile für das Entnehmen der Elemente im Lagerort und eine weitere Zeile für das Einlagern dieser Elemente in einen Bereitstellungsbereich geben. Dann kann es eine weitere Zeile geben, um die Elemente aus der Bereitstellungszone zu entnehmen, und eine weitere Zeile, um die Elemente als Teil des Ladevorgangs in einen LKW einzulagern. Sie können einen *Richtliniencode* für Arbeitsvorlagenpositionen festlegen. Ein Richtliniencode ist mit einer Lagerplatzrichtlinie verknüpft und trägt somit dazu bei, dass die Lagerarbeit am richtigen Lagerplatz im Lager bearbeitet wird.

Sie können eine Abfrage einrichten, um zu steuern, wann eine bestimmte Arbeitsvorlage verwendet wird. So können Sie eine Einschränkung festlegen, damit eine bestimmte Vorlage für Arbeit nur in einem bestimmten Lagerort verwendet werden kann. Alternativ können Sie mehrere Vorlagen haben, die je nach Vertriebsherkunft Arbeit für die Verarbeitung ausgehender Aufträge erstellen. Das System verwendet das Feld **Laufende Nummer**, um den Auftrag zu bestimmen, in der die verfügbaren Lagerplatzdirektiven anfallen. Wenn Sie daher eine einzelne Frage für eine bestimmte Arbeitsvorlage haben, müssen Sie ihnen eine niedrige laufende Nummer eingeben. Diese Abfrage wird dann vor den anderen, allgemeineren Abfragen ausgewertet.

> [!NOTE]
> Um zu verhindern, dass das System nach dem Löschen einer Vorlage automatisch *Sequenznummern* der Arbeitsvorlage überschreibt, schalten Sie die Funktion *Sequenznummern der Arbeitsvorlage beim Löschen beibehalten* in [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ein.

Um einen Arbeitsprozess zu beenden oder anzuhalten, können Sie die Einstellung **Arbeit anhalten** für die Arbeitsposition verwenden. In diesem Fall wird die Arbeitskraft, die die Arbeit ausführt, aufgefordert, den folgenden Arbeitspositionsschritt nicht auszuführen. Um mit dem nächsten Schritt fortzufahren, muss diese Arbeitskraft oder eine andere Arbeitskraft für die Arbeit wieder ausgewählt werden. Sie können die Aufgaben innerhalb einer Arbeit auch trennen, indem Sie ein andere *Arbeitsklassen-ID* für die Arbeitsvorlagenpositionen verwenden.

## <a name="location-directives"></a>Lagerplatzrichtlinien

Lagerplatzrichtlinien sind Regeln, die dabei helfen, Entnahme- und Einlagerungslagerorte für die Lagerumlagerung zu identifizieren. In einer Auftragsbuchung bestimmt eine Lagerplatzrichtlinie z. B., wo die Artikel entnommen und wo die entnommenen Artikel eingelagert werden. Lagerplatzrichtlinien bestehen aus einem Kopf und aus zugeordneten Positionen, und Sie erstellen sie auf der Seite **Lagerplatzrichtlinien**.

Im Kopf muss jede Lagerplatzrichtlinie einem *Arbeitsauftragstyp* zugeordnet werden, der den Typ der Lagerbuchung angibt, für den die Richtlinie verwendet wird, wie Aufträge, Auffüllung oder Rohmaterialentnahme. Der *Arbeitstyp* gibt an, ob die Lagerplatzrichtlinie für die Entnahme oder die Lagerung der Arbeit verwendet wird oder für einen anderen Lagerortprozess, wie Inventur oder Bestandsstatusänderungen. Sie müssen auch einen *Standort* und einen *Lagerort* angeben. Ein *Richtliniencode*, den Sie im Kopf angeben, kann verwendet werden, um die Lagerplatzrichtlinie an eine oder mehrere Arbeitsvorlagen zu knüpfen. 

Was Arbeitsvorlagen angeht, können Sie eine Abfrage einrichten, um festzustellen, wann eine bestimmte Lagerplatzrichtlinie verwendet wird. Beispielsweise können Sie angeben, dass, wenn E-Commerce der Ursprung eines Auftrags ist, der Bestand aus einem dediziertem Bereich des Lagerorts abgeholt werden muss. Das System verwendet das Feld **Laufende Nummer**, um den Auftrag zu bestimmen, in der die verfügbaren Lagerplatzdirektiven anfallen.

Die richtungweisenden Positionen des Lagerplatzes setzen zusätzliche Einschränkungen für die Anwendung für die Regel für das Auffinden des Lagerplatzes fest. Sie können eine minimale Menge und eine maximale Menge angeben, für die die Richtlinie gelten soll, und Sie können angeben, dass die Richtlinie für eine bestimmte Lagereinheit sein soll. Wenn beispielsweise die Maßeinheit Paletten ist, können Artikel auf Paletten an einem bestimmten Lagerplatz eingelagert werden. Sie können auch angeben, ob die Menge über mehrere Lagerplätze verteilt werden kann. Wie der richtungweisende Kopf des Lagerplatzes hat jede richtungweisende Position des Lagerplatzes eine laufende Nummer, die die Reihenfolge bestimmt, in der die Positionen bewertet werden.

Lagerplatzdirektive haben eine zusätzliche Genauigkeitsebene: *Lagerplatzdirektivenaktivitäten*. Sie können Lagerplatzrichtlinien-Aktivitäten für jede Position definieren. Erläuternd, eine laufende Nummer wird verwendet, um die Reihenfolge festzulegen, in der die Aktivitäten anfallen. Auf dieser Ebene können Sie eine Abfrage einrichten, um festzulegen, wo sich der optimale Lagerplatz am Lagerort befindet. Sie können auch vordefinierte **Strategieeinstellungen** verwenden, um einen optimalen Lagerplatz zu finden.

Weitere Informationen zum Erstellen und Konfigurieren von Lagerplatzanweisungen finden Sie unter [Erstellen einer Lagerplatzrichtlinie](create-location-directive.md).

### <a name="how-location-directives-work"></a>Wie Lagerplatzrichtlinien funktionieren

Lagerplatzrichtlinien bestimmen, *wo* Elemente entnommen und *wo* sie eingelagert werden sollen. Das System wertet eine Lagerplatzrichtlinie gegen jede Zeile aus und wählt dann einen Lagerplatz aus, basierend auf den Details der Zeile. Das System findet zunächst alle Lagerplatzrichtlinien, die zu einer bestimmten Arbeitszeile passen (z.B. für das richtige Lagerort und passend zur Abfrage). Anschließend wertet es die gefundenen Richtlinien sequentiell aus.

> [!NOTE]
> Es gibt Sonderfälle, in denen der entnommene Lagerplatz oder der eingelagerte Lagerplatz vorausgewählt ist. Zum Beispiel wird bei _Kaufregistrierung_ immer von dem Lagerplatz entnommen, an dem die Registrierung stattfindet. Ein anderes Beispiel ist die *Bestandsbewegung nach Vorlage*, bei der die Arbeitskraft im Lager den Lagerort auswählt und nur die Einlagerungsplätze durch Lagerplatzrichtlinien gefunden werden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- Video: [Tiefe Einblicke in die Konfiguration der Lagerortverwaltung](https://community.dynamics.com/365/b/techtalks/posts/warehouse-management-configuration-deep-dive-october-14-2020)
- Hilfethema: [Mit Lagerplatzrichtlinien arbeiten](create-location-directive.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]