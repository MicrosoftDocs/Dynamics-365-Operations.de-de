---
title: Projektplanungen und -budgets
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 9577a7058986d200073d66a5824fbba29efa5125
ms.lasthandoff: 03/31/2017


---

# <a name="project-forecasts-and-budgets"></a>Projektplanungen und -budgets



Microsoft Dynamics 365 für Arbeitsgänge bietet zwei Möglichkeiten, die zum Verwalten und Steuern Ihrer Projekte: Projektplanungen und Projektbudgets. 

Sie können die Projektplanung verwenden, wenn die Organisation operativ ausgerichtet ist und der Schwerpunkt auf Umsatzerlösen und Kosten liegt, die aus speziellen Transaktionen stammen. Verwenden Sie die Projektbudgetierung, wenn sich die Organisation eher auf Finanzbeträge konzentriert. 

Sowohl für Projektplanungen als auch für Projektbudgets werden Planzahlenmodelle verwendet, die die voraussichtlichen Buchungsbeträge enthalten. 

Jede Methode hat ihre Vorteile. Bevor Sie sich für eine Methode entscheiden, sollten Sie die folgenden Aspekte berücksichtigen.

|                           |                                                                                                                                                                                                                                                         |                                                                                                                                                                         |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                           | **Projektplanung **                                                                                                                                                                                                                                 | **Projektbudgetierung **                                                                                                                                                   |
| **Zeitraumzuteilung **     | Sie können nicht explizit Transaktion über einen Finanzzeitraum zuweisen. Stattdessen basieren die Planung und Planungssteuerung auf der Lebensdauer des Projekts. Da Planungen auf einem bestimmten Datum basieren, müssen Sie die Periode vom Datum ableiten. | Sie können Buchungen über das gesamte Projekt oder einen Finanzzeitraum verteilen. Beim Verteilen von Planzahlen über einen Zeitraum, können nicht verbrauchte Beträge auf das nächste Geschäftsjahr vorgetragen werden. |
| **Anzeigen von Buchungen**  | In den Planungsformularen können Transaktionen angezeigt werden, in denen die Planungen des gesamten Unternehmens und für alle Projekte unabhängig von der Hierarchie dargestellt werden. Zum Anzeigen eines bestimmten Projekts müssen die Daten gefiltert werden.                                       | Sie können Budgetbuchungen für eine einzelne Projekthierarchie anzeigen. Sie sehen somit die Buchungsdetails für ein übergeordnetes Projekt oder dessen untergeordnete Projekte.                 |
| **Buchungsvariablen ** | Planungsbuchungen können unter Verwendung aller Attribute eingegeben werden, die für eine tatsächliche Buchung vorhanden sind. Planungen können dadurch mehr Details enthalten. So können z. B. Details für Mengen, Arbeitskräfte, Artikel oder Positionseigenschaften eingegeben werden.         | Budgetdetails können nur mit Beträgen, Kategorien und Aktivitäten eingegeben werden.                                                                                    |
| **Sicherheit **              | Die Planung basiert auf der Eingabe von Buchungen in Planungsformulare und umfasst keine prozessgesteuerten Mechanismen. Jede Arbeitskraft mit Berechtigungen für ein Planungsformular kann ohne Genehmigung Informationen überarbeiten.                                        | Für die Budgetierung wird ein Workflowsystem verwendet, das die Änderungsverwaltung und das Aufzeichnen einer Überarbeitungshistorie ermöglicht.                                                       |
| **Eintragstypen **           | Die Einträge von Planungsbuchungen basieren auf der Anzahl von Einheiten, dem Einstandspreis und dem Preis pro Verkaufseinheit.                                                                                                                                                       | Budgetdetails basieren auf Beträgen, die zwischen Kosten und Umsatzerlösen aufgeteilt werden.                                                                                        |
| **Forecast models**       | Da jede Planung einem Modell zugeordnet werden muss, können mehrere Planzahlenmodelle erstellt und auch Teilmodelle eingerichtet werden.                                                                                                                               | Bei der Projektbudgetierung sind die Planzahlenmodelle begrenzt, die für die Budgetierung verwendet werden. Weniger Planzahlenmodelle können zu einheitlicheren Prognosen beitragen.                           |
| **Kostenüberschreitungen **         | Die Eingabe von Buchungen, die eine Kostenüberschreitung verursachen würden, kann lediglich zugelassen oder nicht zugelassen werden.                                                                                                                                                                | Die Projektbudgetierung bietet den Benutzern zusätzliche Steueroptionen. Warnungen und Überschreitungen können zugelassen werden.                                                                   |
| **Control**               | Die Steuerung der Planung erfolgt mithilfe der Planungsverringerung. Tatsächliche Beträge werden ohne Audit-Trail von den Planungsbuchungssalden abgezogen. Dadurch kann schwer nachverfolgt werden, wo die tatsächlichen Buchungen stattgefunden haben.                   | Bei der Projektbudgetsteuerung werden die tatsächlichen Beträge von den Beträgen im Restbudget abgezogen. Das ermöglicht einen übersichtlicheren Audit-Trail.                                   |

## <a name="project-forecasts"></a>Projektplanungen
Bei Verwendung der Projektplanung können Sie für jede Buchungsart Planungsbuchungen in Planungsformulare eingeben. Alle für tätsächliche Buchungen verfügbaren Attribute können auch für eine Planungsbuchung verwendet werden—wie z. B. Positionsrentabilität, Positionsattribute, Arbeitskräfte oder Beschreibungen. Sie können auch berechnen, wann angefallene Kosten dem Debitor in Rechnung gestellt werden sollen. 

Projektplanungsbuchungen basieren auf Einheiten und Beträgen. 

Jede Projektplanung muss einem Planzahlenmodell zugeordnet sein. Wenn Sie eine Planungsbuchung eingeben, wird automatisch ein Planzahlenmodell vorgeschlagen. Das Planzahlenmodell fungiert als Container für die Planungsbuchungen. 

Sie können Planzahlenmodelle als Teilmodelle für ein Modell festlegen. Dadurch können Sie nach Regionen, Zeitperiode oder Abteilung planen. Sie können die Planungsbuchungen zum Erstellen eines neuen Modells kopieren und die Transaktionen auch in das Hauptbuch übertragen. Zwischen einer Planung und einem Modell besteht eine 1:1-Beziehung. Deshalb stellt jedes Planzahlenmodell ein gesondertes Budget für ein Projekt dar. 

In Planzahlenmodellen kann eine Planungsverringerung als Kontrollmechanismus für Projekte verwendet werden. Bei einer Planungsverringerung werden Planungsbuchungssalden durch Istbuchungen verringert. Da eine Planungsverringerung jedoch auf das oberste Projekt in der Hierarchie angewendet wird, ist der Einblick in Planungsänderungen eingeschränkt. Ist beispielsweise eine Arbeitskraft einem Unterprojekt zugeordnet, werden die tatsächlichen Buchungen für die Arbeitskraft im übergeordneten Projekt gebucht. Deshalb können Änderungen möglicherweise nur schwer nachverfolgt werden. Denn es ist nicht leicht zu bestimmen, welche Buchung in welchem Unterprojekt eine Verringerung des Planungsbetrags verursacht hat. Daher wird empfohlen, eine Kopie des Planzahlenmodells zu erstellen, das von der Planungsverringerung verwendet wird. Sie können dann Berichte verwenden, um anzuzeigen, welches die ursprüngliche Planung war. 

Sie können Projektplanungen überarbeiten, kopieren, löschen oder in ein Hauptbuchbudget übertragen. Jedoch gibt es keine Prozesssteuerung. Jede Arbeitskraft mit der Berechtigung für ein Planungsformular kann ohne Überprüfung Bearbeitungen vornehmen.

-   ** Überarbeiten Sie ** – kann eine Planungsbuchung in denselben Formularen überarbeiten, in denen die Originaleinträge vorgenommen wurden.
-   **Kopieren oder löschen** – Beim Kopieren von Planungsbuchungen werden die Buchungspositionen eines Planzahlenmodells in ein anderes Planzahlenmodell kopiert. Beim Löschen einer Planung werden die Planungsbuchungen aus einem Planzahlenmodell gelöscht. Wählen Sie bestimmte Buchungsarten und Datumsangaben aus, um die zu kopierenden oder zu löschenden Planungsbuchungen einzuschränken. Auf diese Weise können Sie nur bestimmte Teile einer Planung kopieren oder löschen.
-   **Übertragen** – Beim Übertragen einer Projektplanung in ein Hauptbuchbudget werden die Planungsbuchungen eines Planzahlenmodells in ein Hauptbuchbudget übertragen. Sie können jede zuvor übertragene Buchungen in dem Hauptbuchbudget überschreiben, in das Sie die Projektplanung übertragen haben.

## <a name="project-budgets"></a>Projektbudgets
Die Projektbudgetierung ist trotz der Integration in Planzahlenmodelle eine einfachere Methode als die Planung. Für die Details des ursprünglichen Budgets und für Überarbeitungen wird nur ein Eingabeformular verwendet. Zudem können Projektionen allein anhand des Betrags, der Kategorie oder der Aktivität vorgenommen werden. 

Bei der Projektbudgetierung müssen alle ursprünglichen Budgets und Überarbeitungen an den Projektworkflow zur Genehmigung gesendet werden. Der Workflow ermöglicht eine bessere Steuerung des Prozesses und erstellt einen Änderungshistoriendatensatz. 

Die Projektbudgetierung ist mit der Budgetfunktion des Hauptbuchs vergleichbar, kann jedoch schneller und einfacher eingerichtet werden. Viele der Optionen im Hauptbuchbudget, wie Nummernkreise oder Währung, müssen für Projekte nicht separat eingerichtet werden.

Projektbudgets werden automatisch zwei Planzahlenmodellen zugeordnet, eines für das ursprüngliche Budget und eines für das Restbudget. Dies ermöglicht die Verwendung von Budgetdaten für Berichte, die auf Planzahlenmodellen basieren. Wenn ein Projektbudget zugesagt wird, werden anhand der zugeordneten Modelle Planungsbuchungen erstellt, die für Berichterstellungs- und Steuerungszwecke verwendet werden.

## <a name="forecast-models"></a>Planzahlenmodelle
Planzahlenmodelle bestehen aus einer Einzelebenen-Hierarchie. Daher muss jede Projektplanung muss einem Planzahlenmodell zugeordnet sein.

Wenn Sie die Projektplanung verwenden, können Sie Modelle als Teilmodelle festlegen und damit. Sie können Planungen nach Abteilung, Zeitperiode oder Region erstellt werden. Es ist z. B. möglich, ein Planzahlenmodell für ein Jahr und anschließend Teilmodelle für die Regionalplanungen "Nordosten", "Südosten", "Nordwesten" und "Südwesten" zu erstellen, die von den Regionsleitern übermittelt werden. Wenn Sie verschiedene Optionen in den verfügbaren Berichten auswählen, sodass Informationen nach Aggregatplanung oder nach Teilmodellen angezeigt werden können.


