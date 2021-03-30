---
title: Budgetplanung – Übersicht
description: Dieses Thema beschreibt die Budgetplanung. Es enthält Informationen, die Ihnen bei der Konfiguration der Budgetplanung und der Einrichtung von Budgetplanungsprozessen helfen können.
author: panolte
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: roschlom
ms.custom: 17251
ms.assetid: a2e06633-a800-4840-a962-88fed8462104
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f45def44a285dbc937a2a602aa873f8a04486902
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210288"
---
# <a name="budget-planning-overview"></a>Budgetplanung – Übersicht

[!include [banner](../includes/banner.md)]

Dieses Thema beschreibt die Budgetplanung. Es enthält Informationen, die Ihnen bei der Konfiguration der Budgetplanung und der Einrichtung von Budgetplanungsprozessen helfen können.

## <a name="overview-of-budget-planning"></a>Über blick zur Budgetplanung

Eine Organisation kann Budgetplanung konfigurieren und anschließend Budgetplanungsprozesse einrichten, um die Richtlinien, die Verfahren und Bedingungen ihrer Organisation für Budgetausarbeitung zu erfüllen. Wenn Sie die Konzepte und die Terminologie verstehen, die in Microsoft Dynamics 365 Finance verwendet werden, können Sie die Budgetplanung in Ihrer Organisation leichter und effektiver umsetzen.

### <a name="key-terms"></a>Schlüsselbegriffe

- **Budgetplanungsprozesse** - Budgetplanungsprozess bestimmen, wie Budgetpläne in der Budgetplanungs-Organisationshierarchie aktualisiert, weitergeleitet, geprüft und genehmigt werden können. Ein Budgetplanungsprozess ist mit einem Budgetzyklus und einer Organisation durch eine juristische Person verbunden.
- **Budgetpläne** - Budgetpläne enthalten die Budgetdaten für einen Budgetzyklus. Sie benötigen mehrere Budgetpläne für verschiedene Zwecke. Beispielsweise können Sie mit Hilfe von Budgetplänen Budgetbeträge für verschiedene Organisationseinheiten anlegen. Sie können sie auch verwenden, um Vergleiche anzustellen und fundierte Entscheidungen zu treffen.
- **Budgetplanszenarien** - Budgetplanszenarien definieren Kategorien von Daten für die Budgetpläne. Sie definieren Budgetplanszenarien, um Geldklassen und andere Mengeneinheitenklassen, wie z.B. Mengen, zu unterstützen. Beispiele für monetäre Budgetplanszenarien sind „Abteilung Vorjahr“ und „Anträge der Abteilung“. Beispiele für Budgetplan-Szenarien, die Mengen verwenden, sind „Supportanrufe des Vorjahres“ und „Zählung der Vollzeitäquivalente“.
- **Budgetplanungsphasen** - Die Budgetplanungsphasen definieren die Schritte, denen ein Budgetplan von seinem Beginn bis zur endgültigen Genehmigung folgt. Budgetplanungsphasen werden in Budgetplanungsworkflows angeordnet.
- **Budgetplanungsworkflows** - Budgetplanungsworkflows bestehen aus Budgetplanungsphasen und legen diese fest. Die Workflows der Budgetplanung sind mit den Budgetierungs-Workflows verbunden. Budgetierungsworkflows sind die automatisierten und manuelle Prozesse, die Budgetpläne durch die Budgetplanungsphasen verschieben.

[![Budgetplanungsterminologie](./media/budgetplanning-terms-1024x504.png)](./media/budgetplanning-terms.png)

### <a name="typical-tasks"></a>Typische Aufgaben

Die folgenden Aufgaben können mit Budgetplanung ausgeführt werden:

- Erstellen Sie Budgetpläne, um die erwarteten Einnahmen und Ausgaben für einen Budgetzyklus zu definieren.
- Analysieren und aktualisieren Sie Budgetpläne für mehrere Szenarios.
- Leiten Sie die Budgetpläne automatisch zusammen mit Arbeitsblättern, Begründungsdokumenten und weiteren Anlagen zur Prüfung und Genehmigung weiter.
- Konsolidieren Sie mehrere Budgetpläne von einer niedrigeren Ebene der Organisation in einen einzigen übergeordneten Budgetplan auf einer höheren Ebene. Sie können auch einen einzigen Budgetplan auf einer höheren Ebene der Organisation entwickeln und das Budget auf niedrigeren Ebenen zuweisen.

Budgetplanung ist in anderen Modulen integriert. Daher können Sie Informationen aus früheren Budgets, Ist-Ausgaben, Anlagen und Personalressourcen einbeziehen. Da die Budgetplanung auch mit Microsoft Excel und Microsoft Word integriert ist, können Sie mit diesen Programmen mit den Daten der Budgetplanung arbeiten. So kann ein Budgetverantwortlicher beispielsweise die Budgetanforderung einer Abteilung aus einem Budgetplan-Szenario in ein Excel-Arbeitsblatt exportieren. Die Daten können dann analysiert, aktualisiert und im Arbeitsblatt dargestellt werden und dann wieder in den Budgetplanzeilen veröffentlicht werden.

## <a name="configuring-budget-planning"></a>Budgetplanung konfigurieren

Die Funktionalität, die in Dynamics 365 Finance Version 10.0.9 (April 2020) eingeführt wurde, umfasst eine Funktion, die zur Verbesserung der Leistung beiträgt, wenn Sie die Schaltfläche **Veröffentlichen** verwenden, um vorhandene Datensätze in Excel zu aktualisieren und dann zurück an den Kunden zu veröffentlichen. Diese Funktion beschleunigt den Aktualisierungsprozess und hilft auch, die Wahrscheinlichkeit zu verringern, dass eine Aktualisierung blockiert wird, wenn Sie viele Datensätze gleichzeitig aktualisieren. Um diese Funktionalität verfügbar zu machen, gehen Sie zum Arbeitsbereich **Funktionsverwaltung** Arbeitsbereich und schalten Sie die Funktion **Budgetplanungsabfrageoptimierung für Leistung** unter **Budgetierung** ein. Wir empfehlen Ihnen, diese Funktion zu aktivieren.

Die Seite **Budgetplanungskonfiguration** enthält die meisten Einstellungen, die für die Einrichtung der Budgetplanung erforderlich sind. In den folgenden Abschnitten werden einige der Faktoren beschrieben, die Sie bei der Konfiguration der Budgetplanung berücksichtigen sollten. Nachdem Sie die Konfiguration abgeschlossen haben, können Sie Budgetplanungsprozesse einrichten.

### <a name="budget-planning-schema-optional"></a>Budgetplanungsschema (optional)

Ein optionaler, aber empfohlener erster Schritt ist die Erstellung eines Schemas, das das Verfahren Ihrer Organisation zur Aufstellung eines Budgets zeigt. Sie können jede Methode verwenden, um dieses Schema zu erstellen.

Die folgende Abbildung zeigt ein generisches Beispiel, in dem separate Budgetplanungsworkflows für verschiedene Ebenen der Organisation erstellt werden. In jedem Workflow werden Stufen definiert, und jeder Stufe werden spezifische Szenarien zugeordnet, um die Budgetdaten zu halten. Die Aufgaben werden abgeschlossen, um die Daten von einer Stufe zur nächsten zu verschieben. So können Beträge z. B. auf verschiedenen Konten, Genehmigungen oder anderen Überprüfungen zugewiesen oder zusammengefasst werden. In dieser Abbildung weist kursiver Text auf ein Szenario hin, das während der Phase nicht bearbeitet werden kann, oder auf Daten, die historisch sind oder in einer früheren Phase genehmigt wurden und daher nicht geändert werden sollten.

[![Beispiel eines Budgetplanungsschemas](./media/budgetplanninggenericschema-300x145.png)](./media/budgetplanninggenericschema.png) 

Die folgende Abbildung zeigt ein Beispiel, bei dem die Unternehmenszentrale die Basisbeträge für das Anfangsbudget schätzt und an die Vertriebsabteilungen verteilt. Die Vertriebsabteilungen schätzen dann ihre Prognose und übermitteln sie an den Hauptsitz zurück, wo der Budgetverantwortliche die Prognose aggregiert und anpasst. Schließlich sendet der Budgetverantwortliche die angepassten Budgetbeträge an den Chief Financial Officer (CFO) zur Überprüfung, abschließenden Anpassung und Genehmigung.

[![Beispiel eines Budgetplanungsschemas](./media/budgetplanningexampleschema-300x145.png)](./media/budgetplanningexampleschema.png)

### <a name="organization-hierarchy-for-budget-planning"></a>Organisationshierarchie für Budgetplanung

Auf der Seite **Organisationshierarchie** können Sie für jeden Budgetplanungsprozess eine Organisationshierarchie als Budgetplanungshierarchie festlegen. Die Budgetplanungshierarchie muss mit der Standardorganisationshierarchie nicht übereinstimmen, die für andere Zwecke verwendet wird. Da diese Hierarchie verwendet wird, um Daten zu aggregieren und zu verteilen, sollten sie eine andere Struktur haben. In dem Beispielschema befinden sich die Vertriebsabteilungen unter einer Hauptsitz-Ebene, die die Budget- und Finanzabteilungen umfasst. Diese Struktur unterscheidet sich wahrscheinlich von der Struktur, die für die Verwaltung der Vorgänge für die Vertriebsabteilungen verwendet wird. Nur eine Organisationshierarchie kann einem Budgetplanungsprozess zugewiesen werden.

Weitere Informationen zu den finden Sie unter [Organisationen und Organisationshierarchien](../../fin-and-ops/organization-administration/organizations-organizational-hierarchies.md).

### <a name="user-security"></a>Benutzersicherheit

Budgetplanung kann einem von zwei Sicherheitsmodellen folgen, um Benutzerrechte zu definieren. Um das Sicherheitsmodell anzugeben, legen Sie auf der Seite **Budgetplanungskonfiguration** einem Budgetplanungsparameter fest.

### <a name="budget-planning-workflows-stages"></a>Budgetplanungsworkflowphasen

Budgetplanungs-Workflows werden zusammen mit den Budgetierungs-Workflows verwendet, um die Erstellung und Entwicklung von Budgetplänen zu verwalten.

Ein Budgetplanungsworkflow besteht aus einer geordneten Menge von Phasen, die ein Budgetplan durchläuft. Jeder Budgetplanungs-Workflow ist mit einem Budgetierungs-Workflow verbunden. Budgetierungs-Workflows sind eine der Arten von Workflows, die durchgehend in Dynamics 365 Finance verwendet werden. Sie leiten die Budgetpläne zusammen mit Arbeitsblättern, Begründungen und Anhängen zur Überprüfung und Genehmigung durch die Organisation.

Sie erstellen einen Budgetplanungs-Workflow im Abschnitt **Workflow-Stufen** der Seite **Budgetplanungskonfiguration**. Dort können Sie die Phasen und den zu verwendenden Budgetierungs-Workflow auswählen und zusätzliche Einstellungen konfigurieren.

Eine bewährte Methode ist das Erstellen eines Budgetplanungsworkflows für jedes Ebene einer Budgetplanungshierarchie. Anschließend ordnen Sie einen Budgetierungs-Workflow zu, der Elemente enthält, die den Stufen im Workflow der Budgetplanung entsprechen. In dem Beispielschema, das weiter oben in diesem Thema erscheint, wird ein Budgetplanungs-Workflow für die Vertriebsabteilungen und ein weiterer für die Zentrale erstellt. Ein Budgetierungs-Workflow bewegt die Budgetpläne durch die verschiedenen Phasen.

Sie erstellen einen Budgetierungs-Workflow für die Budgetplanung auf der Seite **Budgetierungs-Workflows**. Der Vorgang ähnelt dem Vorgang zum Erstellen anderer Workflows. Die folgende Abbildung zeigt ein Beispiel für einen Workflow für die Zentrale.

[![Budgetierungsworkflow für Budgetplanung](./media/budgetingworkflowforbudgetplanning-300x300.png)](./media/budgetingworkflowforbudgetplanning.png) 

Der Workflow umfasst die folgenden Elemente:

- Zuweisung an die Vertriebsabteilungen und Aggregation ihrer Eingaben
- Überprüfung der Budgetverantwortlichen
- CFO-Freigabe
- Schrittweise Übergänge zwischen den einzelnen Phasen des Budgetplanungs-Workflows einrichten

Sie ordnen den Budgetierungs-Workflow jedem Budgetplanungs-Workflow im Abschnitt **Workflow-Stufen** der Seite **Budgetplanungskonfiguration** zu.

### <a name="parameters-scenarios-and-stages"></a>Parameter, Szenarien und Phasen

Mit den ersten Einstellungen auf der Seite **Budgetplanungskonfiguration** können Sie mehrere Bausteine für spätere Konfigurationsschritte erstellen:

- **Parameter** - Parameter definieren die Sicherheitsregeln, die Sie auf die Budgetpläne anwenden möchten, und die standardmäßigen finanziellen Dimensionen, die verwendet werden sollen, wenn die Benutzer die Beträge in den Budgetplan-Szenarien aufschlüsseln.
- **Szenarien** - Szenarien umfassen die Kategorien von Daten, die Sie für die Budgetpläne möchten. Sie definieren Budgetplanszenarien zur Unterstützung von Geldklassen und anderen Mengeneinheitsklassen, wie z.B. der Menge. In einem Budgetplan stellen Szenarien eine Version der Budgetplanungsdaten dar. Beispiele für monetäre Budgetplanszenarien sind „Verkäufe des Vorjahres“ und „Unterzeichnete Verträge“. Beispiele für Szenarien, die Mengen verwenden, sind „Anzahl der Verkaufsanrufe“ und „Anzahl der Vollzeitäquivalente“.
- **Stufen** - Stufen definieren die Schritte, denen ein Budgetplan von seinem Beginn bis zur endgültigen Genehmigung folgt. Beispiele für Budgetplanungsphasen sind „HQ-Rollup“, „CFO-Prüfung“ und „Endgültig“.

### <a name="allocation-schedules"></a>Zuteilungszeitpläne

In der Budgetplanung können Sie die Beträge zuweisen oder Mengen auf den Budgetplanpositionen von einem Szenario zum anderen oder sogar dem gleichen Szenario verschieben. Sie können beispielsweise Beträge oder Mengen demselben Szenario zuweisen, wenn Sie Änderungen an den finanziellen Dimensionen oder den Daten der Beträge in diesem Szenario vornehmen möchten. Eine Zuteilung kann innerhalb eines Budgetplans oder von einem Budgetplan zum anderen durchgeführt werden.

Zuteilungszeitpläne weisen Budgetplanpositionen während der Workflowverarbeitung automatisch zu. Sie können Zuordnungen vornehmen, indem Sie eine der folgenden Methoden in der Liste **Zuordnungsmethode** verwenden:

- **Auf Perioden verteilen** - Sie verwenden den Planzahlenverteilungsschlüssel, um Budgetplanpositionen von den Quellbudgetplanszenarioperioden im Zielszenario zuzuteilen.

    > [!NOTE]
    > Bevor Sie eine periodenübergreifende Zuordnung durchführen können, müssen Sie Periodenaufteilungsschlüssel auf der Seite **Periodenaufteilungskategorien** einrichten.

- **Zu Dimensionen zuordnen** - Die Budgetplanpositionen werden vom Quellbudgetplanszenario in den Finanzdimensionen im Zielszenario zugewiesen.

    > [!NOTE]
    > Bevor Sie auf Dimensionen verrechnen können, müssen Sie auf der Seite **Budgetvergabebedingungen** Budgetvergabebedingungen einrichten.

- **Zusammenführen** - Die Budgetplanpositionen werden aus dem Quellbudgetplanszenario in zugeordneten Budgetplänen auf das Zielszenario in den übergeordneten Budgetplan verteilt.
- **Verteilen** - Die Budgetplanpositionen werden aus dem Quellbudgetplanszenario im übergeordneten Budgetplan auf das Zielszenario in den zugehörigen Budgetplänen verteilt.
- **Sachkonto-Zuordnungsregeln verwenden** - Die Budgetplanpositionen werden vom Quellbudgetplanszenario auf Grundlage der ausgewählten Sachkonto-Zuordnungsregel auf das Zielbudgetplanszenario verteilt.
- **Aus Budgetplan kopieren** - Sie können einen anderen Budgetplan auswählen, den Sie als Quelle der Zuordnung verwenden.

### <a name="stage-allocations"></a>Phasenzuteilungen

Phasenzuteilungen werden verwendet, um Budgetplanpositionen während des Workflowverarbeitens zuzuordnen. Bei der Verwendung von Stufenverteilungen können Budgetplanzeilen im Zielszenario ohne die Intervention des Erstellers des Budgetplans oder des Revisors angelegt und geändert werden.

Wenn Sie eine Phasenzuteilung einrichten, ordnen Sie den Budgetplanungsworkflow zu und stellen ihn mit dem Zuteilungszeitplan bereit. Der Budgetplanungs-Workflow muss mit einem Budgetierungs-Workflow verbunden sein, der die **Budgetplanungsstufenzuweisung** automatisierte Workflow-Aufgabe verwendet. Wenn der Workflow die angegebene Phase erreicht, tritt die Zuweisung automatisch auf. Diese automatisierte Aufgabe kann verwendet werden, um Budgetplanpositionen in einem neuen Szenario zu erstellen.

In dem Beispielschema, das weiter oben in diesem Thema erscheint, wird eine Zuweisung vorgenommen, um Beträge von einem Budgetplan und Szenarien in der Phase „Baseline“ für die Zentrale auf einen anderen Budgetplan und Szenarien in der Phase „Schätzung“ für die Vertriebsabteilungen zu übertragen. Die folgende Abbildung zeigt den relevanten Abschnitt des Beispielsschemas.

[![Phasenzuteilungen](./media/stageallocation-204x300.png)](./media/stageallocation.png) 

Zusätzlich wird im Beispielschema eine Aggregation von Budgetplänen und Szenarien in der Phase „Eingereicht“ für die Vertriebsabteilungen auf einen übergeordneten Plan in der Phase „Rollup“ für den Hauptsitz vorgenommen. Die folgende Abbildung zeigt den relevanten Abschnitt des Beispielsschemas.

[![Aggregation](./media/aggregation-109x300.png)](./media/aggregation.png)

### <a name="priorities"></a>Prioritäten

Sie können optional die Prioritäten des Budgetplans verwenden, um Kategorien und Ziele für die von Ihnen eingerichteten Budgetpläne zu definieren. Sie können Prioritäten auch verwenden, um mehrere Budgetpläne zu organisieren, zu klassifizieren und zu bewerten. So können Sie beispielsweise eine Budgetplanungspriorität für Status und Sicherheit erstellen und dann Budgetpläne überprüfen, die dieser Priorität zugewiesen werden. Sie können Ihren Budgetplänen auch eine Nummer zuweisen, um eine Rangfolge anzugeben.

### <a name="columns-and-layouts"></a>Spalten und Layouts

In einem Budgetplan erscheinen die Budgetzahlen in Zeilen und Spalten. Sie definieren zunächst die Spalten und können dann ein Layout erstellen, um die Darstellung dieser Spalten zu definieren.

Wenn Sie eine Spalte definieren, wählen Sie ein Budgetplanszenario aus. Die Zeilenbeträge aus diesem Szenario werden im Budgetplan angezeigt. Sie können eine Periode auswählen, um den Betrag zu filtern, und Sie können auch Filter anwenden, die auf dem Sachkonto basieren.

Wenn Sie ein Layout definieren, wählen Sie ein Ledger-Dimensionsset aus, um die Budgetplanzeilen anzulegen, die Sie einblenden wollen, und wählen Sie die Spalten als Layoutelemente aus. Sie können mehrere Layouts anlegen, sodass ein Budgetplan die gewünschten Daten in verschiedenen Phasen des Budgetplanungsprozesses anzeigt.

Zusätzlich zu den Spalten für Budgetbeträge können Sie Spalten für die Felder "Projekt", "Vorgeschlagene Projekt", "Anlage" und "Vorgeschlagene Anlage" vom Budgetplan definieren. Sie können eine Spalte für Budgetpositionen definieren. Diese Option ist nützlich, wenn Sie Personalbudgets analysieren müssen.

Für das Beispielschema könnten Sie Spalten für die Szenarien „Jahresumsatz“, „Verträge“ und „Prognose“ anlegen. (Die folgende Abbildung zeigt den entsprechenden Abschnitt des Schemas.) Sie können dann eines oder alle diese Szenarien in separate Spalten für jedes Quartal des Geschäftsjahres aufgliedern, sodass der Leiter der Vertriebsabteilung die Prognosebeträge für jede Periode genau eingeben kann.

[![Spalten](./media/columns.png)](./media/columns.png)

Sie geben auch an, ob jedes Layoutelement (Spalte) bearbeitbar ist und ob es in jeder Arbeitsblattvorlage, die für dieses Layout erstellt wird, verfügbar ist. Für das Beispielschema sind in dem Layout, das für die Phase „Schätzung“ verwendet wird, die Spalten „Prognose“ editierbar, die Spalten „PY Verkauf“ und „Verträge“ sind jedoch schreibgeschützt.

> [!NOTE]
> Standardmäßig sind Sie auf 36 Spalten beschränkt, es sei denn, Sie erweitern die Budgetplanung, indem Sie die Schritte unter [Budgetplanungslayout erweitern](./extending-budget-planning-layout.md) befolgen.

### <a name="templates"></a>Vorlagen

Im Abschnitt **Layouts** der Seite **Budgetplanungskonfiguration** können Sie für jedes Layout eine Excel-Vorlage generieren, anzeigen oder hochladen. Diese Vorlagen sind die Arbeitsmappen, die mit jedem Budgetplan verknüpft werden, um zusätzliche Analyse-, Diagrammerstellung- und Dateneingabefunktionen bereitzustellen.

Wenn eine Vorlage generiert wird, wird das Layout gesperrt und kann nicht bearbeitet werden. Diese Sperre hilft sicherzustellen, dass das Format der Vorlage mit dem Layout des Budgetplans übereinstimmt und dieselben Daten enthält. Nachdem eine Vorlage generiert wurde, kann sie angezeigt und bearbeitet werden. Sie können der Vorlage z. B. Diagramme hinzufügen oder die Darstellung weiter anpassen.

> [!NOTE]
> Eine Vorlage sollte an einem Ort gespeichert werden, auf den der Benutzer Zugriff hat, sodass sie nach Abschluss der Bearbeitung in das Layout hochgeladen werden kann. Auf diese Weise wird die Vorlage bei Budgetplänen verwendet, die das Layout verwenden.

### <a name="descriptions"></a>Beschreibungen

Im Abschnitt **Layouts** können Sie Beschreibungen zuordnen, um den Namen einer finanziellen Dimension anzuzeigen, die in einem Layout enthalten ist. Eine Organisation möchte z.B. in einem Budgetplan den Namen des Hauptkontos neben der Nummer des Hauptkontos anzeigen. Sie könnte jedoch die Namen anderer finanzieller Dimensionen weglassen wollen, um die Anzeige nicht zu überladen.

## <a name="setting-up-budget-planning-processes"></a>Einrichten von Budgetplanungsprozessen

Nachdem Sie die Konfiguration der Budgetplanung abgeschlossen haben, können Sie Budgetplanungsprozesse auf der Seite **Budgetplanungsprozess** einrichten. Budgetplanungsprozesse sind ein Satz Regeln, die bestimmen, wie Budgetpläne in der Budgetplanungs-Organisationshierarchie aktualisiert, weitergeleitet, geprüft und genehmigt werden können.

Für jeden Budgetplanungsprozess wählen Sie zunächst einen Budgetzyklus und ein Sachkonto aus. Jeder Budgetplanungsprozess bezieht sich nur auf einen Budgetzyklus und ein Sachkonto. Sie wählen dann die Hierarchie der Budgetorganisation auf der Registerkarte **Verwaltung des Budgetplanungsprozesses** und ordnen allen in der Tabelle angezeigten Verantwortungszentren in der Organisation einen Budgetplanungs-Workflow zu.

Um den Budgetplanungs-Workflow für ähnliche Verantwortungszentren zuzuordnen oder zu ändern, wählen Sie **Workflow zuweisen** und wählen dann die zu verwendende Organisationsart und den zu verwendenden Budgetplanungs-Workflow aus. Die Budgetierungs-Workflow-ID, die mit jedem Budgetplanungs-Workflow verknüpft ist, wird automatisch der Tabelle hinzugefügt.

Wenn Sie die Phasenregeln und Vorlagen im Inforegister **Regeln und Layouts für die Budgetplanungsphase** definieren, können Sie eine andere Gruppe von Regeln und Standardlayouts für jede Budgetplanungsphase definieren. Beispielsweise kann die Phase „Schätzung“ für die Vertriebsabteilungen den Benutzern erlauben, die Zeilen in einem Budgetplan zu ändern, aber das Hinzufügen von Zeilen verbieten. In der Phase „Eingereicht“ können Benutzer Zeilen anzeigen, aber nicht hinzufügen oder ändern, da die Arbeit in dieser Phase abgeschlossen ist und Änderungen an den Budgetplänen verhindert werden müssen. Um die Layouts auszuwählen, die für Budgetpläne zur Verfügung stehen, wählen Sie **Alternative Layouts**.

Sie können Budgetplanungsprioritäten optional auf dem Inforegister **Budgetplanprioritäts-Einschränkungen** auswählen. Prioritäten können dann auf Budgetplänen ausgewählt werden.

Der letzte Schritt ist die Aktivierung des Budgetplanungsprozesses über das Menü **Aktionen**. Ein Budgetplanungsprozess kann erst nach seiner Aktivierung verwendet werden.

Sie können auch das Menü **Aktionen** verwenden, um einen neuen Prozess anzulegen, indem Sie einen bestehenden Prozess kopieren. Diese Funktion ist hilfreich für Organisationen, die bei jedem Budgetzyklus dem gleichen Prozessfluss folgen und nur wenigste oder gar keine Änderungen vornehmen.

Ein anderer nützlicher Befehl im Menü **Aktivitäten** ist **Budgetprozessstatus anzeigen**. Dieser Befehl zeigt die Budgetpläne in einem Prozess grafisch an, zusammen mit relevanten Daten, wie z.B. dem Workflow-Status der Pläne, Zusammenfassungen nach Betrag und Einheit und die Navigation zu den Budgetplänen selbst mit einem Klick.

[![Status des Budgetplanungsprozesses](./media/budgetplanningprocessstatus-300x171.png)](./media/budgetplanningprocessstatus.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]