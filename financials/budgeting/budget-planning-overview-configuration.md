---
title: "Budgetplanung (Überblick)"
description: "Dieser Artikel umfasst die Budgetplanung und enthält Informationen, die Ihnen die dabei helfen, die Budgetplanung zu konfigurieren und Budgetplanungsprozesse einzurichten."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17251
ms.assetid: a2e06633-a800-4840-a962-88fed8462104
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: d5073958f8ffe90e47dc10cde67e081420e559a1
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning-overview"></a>Budgetplanung (Überblick)

[!include[banner](../includes/banner.md)]


Dieser Artikel umfasst die Budgetplanung und enthält Informationen, die Ihnen die dabei helfen, die Budgetplanung zu konfigurieren und Budgetplanungsprozesse einzurichten.

<a name="overview-of-budget-planning"></a>Über blick zur Budgetplanung
---------------------------

Sie führen Budgetplanung durch, wenn Sie die Budgets vorbereiten, die von einer Organisation implementiert werden. Eine Organisation kann Budgetplanung konfigurieren und anschließend Budgetplanungsprozesse einrichten, um die Richtlinien, die Verfahren und Bedingungen ihrer Organisation für Budgetausarbeitung zu erfüllen. 

Wenn Sie die Konzepte und die Terminologie verstehen, die in Microsoft Dynamics 365 for Operations verwendet werden, erleichtert dies die Budgetplanung in Ihrer Organisation.

### <a name="key-terms"></a>Schlüsselbegriffe

-   **Budgetplanungsprozesse** - Budgetplanungsprozess bestimmen, wie Budgetpläne in der Budgetplanungs-Organisationshierarchie aktualisiert, weitergeleitet, geprüft und genehmigt werden können. Ein Budgetplanungsprozess wird mit einem Budgetzyklus und mit einer Organisation über eine juristischen Person verknüpft.
-   **Budgetpläne** - Budgetpläne enthalten die Budgetdaten für einen Budgetzyklus. Sie benötigen mehrere Budgetpläne für verschiedene Zwecke. So können Budgetpläne z. B. verwenden, um Budgetbeträge für verschiedene Organisationseinheiten zu erstellen, oder sie können helfen, Vergleiche zu erstellen und fundierte Entscheidungen zu treffen.
-   **Budgetplanszenarien** - Budgetplanszenarien definieren Kategorien von Daten für die Budgetpläne. Sie definieren Budgetplanszenarien, um monetäre und anderen Maßeinheitsklassen, wie Menge zu unterstützen. Beispiele für Währungsbudgetplanszenarien umfassen das vorige Abteilungsjahr und Abteilungsanforderungen. Beispiele für Budgetplanszenarios, die Mengen verwenden, schließen Support-Aufrufe des Vorjahres und die Vollzeitäquivalent (FTE)-Anzahl ein.
-   **Budgetplanungsphasen** - Budgetplanungsphasen definieren die Schritte, denen ein Budgetplan von Start zur endgültigen Zustimmung folgt. Budgetplanungsphasen werden in Budgetplanungsworkflows angeordnet.
-   **Budgetplanungsworkflows** - Budgetplanungsworkflows bestehen aus Budgetplanungsphasen und legen diese fest. Budgetplanungsworkflows werden Budgetierungsworkflows zugeordnet. Budgetierungsworkflows sind die automatisierten und manuelle Prozesse, die Budgetpläne durch die Budgetplanungsphasen verschieben.

[![Budgetplanungsterminologie](./media/budgetplanning-terms-1024x504.png)](./media/budgetplanning-terms.png)

### <a name="common-tasks"></a>Allgemeine Aufgaben

Die folgenden Aufgaben können mit Budgetplanung ausgeführt werden:

-   Erstellen Sie Budgetpläne, um die erwarteten Umsatzerlöse und Aufwendungen für einen Budgetzyklus zu definieren.
-   Analysieren und aktualisieren Sie Budgetpläne für mehrere Szenarios.
-   Leiten Sie die Budgetpläne automatisch zusammen mit Arbeitsblättern, Begründungsdokumenten und weiteren Anlagen zur Prüfung und Genehmigung weiter.
-   Konsolidieren Sie mehrere Budgetpläne von einer untergeordneten Ebene der Organisation in einen einzigen Haushaltsplan auf einer höheren Ebene der Organisation. Sie können auch einen einzelnen Budgetplan auf einer höheren Ebene der Organisation entwickeln und das Budget den untergeordneten Ebenen der Organisation zuordnen.

Budgetplanung ist in anderen Microsoft Dynamics 365 for Operations-Modulen integriert. Daher können Sie Informationen aus früheren Budgets, tatsächlichen Aufwendungen, Anlagen und der Personalverwaltung einbringen. Da die Budgetplanung ebenfalls in Microsoft Excel und Microsoft Word integriert ist, können Sie diese Programme verwenden, um mit den Budgetplanungsdaten zu arbeiten. So kann ein Budget-Manager Budgetanforderung einer Abteilung aus einem Budgetplanszenario in ein Excel-Arbeitsblatt exportieren. Die Daten können im Arbeitsblatt analysiert, aktualisiert und entworfen werden, und dann wieder in den Budgetplanpositionen veröffentlicht werden.

## <a name="configuring-budget-planning"></a>Budgetplanung konfigurieren
Die Seite **Budgetplanungskonfiguration** enthält die meisten Einstellungen, die Sie benötigen, um eine Budgetplanung einzurichten. In folgenden Abschnitte beschreiben wesentliche Faktoren, die Sie bei der Konfiguration der Budgetplanung berücksichtigen sollten. Nachdem die Konfiguration abgeschlossen ist, richten Sie Budgetplanungsprozesse ein.

### <a name="create-a-budget-planning-schema"></a>Budgetplanungsschema erstellen

Ein optionaler jedoch empfohlener erster Schritt ist die Erstellung eines Schemas, das die Prozedur Ihrer Organisation für die Formulierung eines Budgets anzeigt. Sie können jede Methode verwenden, um dieses Schema zu erstellen. Die folgende Abbildung zeigt ein generisches Beispiel, in dem separate Budgetplanungsworkflows für verschiedene Ebenen der Organisation erstellt werden. Innerhalb jedes Workflows werden Phasen definiert, und bestimmte Szenarien, die die Budgetdaten enthalten, werden jeder Phase zugeordnet. Aufgaben werden durchgeführt, um die Daten von einer Phase zur nächsten zu verschieben. So können Beträge z. B. auf verschiedenen Konten, Genehmigungen oder anderen Überprüfungen zugewiesen oder zusammengefasst werden. In diesem Beispiel zeigt kursiver Text ein Szenario an, das innerhalb der Phase nicht bearbeitbar ist, oder historische in einer vorherigen Phase genehmigte Daten, die daher nicht geändert werden sollten. 

[![Beispiel eines Budgetplanungsschemas](./media/budgetplanninggenericschema-300x145.png)](./media/budgetplanninggenericschema.png) 

Im folgenden Beispiel schätzt der Unternehmenshauptsitz die ersten Budgetbasisbeträge und verteilt diese auf die Verkaufsabteilungen. Die Verkaufsabteilungen schätzen dann ihre Planung und senden sie an die Zentralverwaltung zurück, wo der Budget-Manager die Planung zusammenfasst und reguliert. Schließlich sendet der Budget-Manager die angepassten Budgetbeträge zur Prüfung, endgültigen Regulierung und Genehmigung zum CFO. 

[![Beispiel eines Budgetplanungsschemas](./media/budgetplanningexampleschema-300x145.png)](./media/budgetplanningexampleschema.png)

###  <a name="organization-hierarchy-for-budget-planning"></a>Organisationshierarchie für Budgetplanung

Auf der **Organisationshierarchie**-Seite können Sie für jeden Budgetplanungsprozess eine Organisationshierarchie als Budgetplanungshierarchie auswählen. Die Budgetplanungshierarchie muss mit der Standardorganisationshierarchie nicht übereinstimmen, die für andere Zwecke verwendet wird. Da diese Hierarchie verwendet wird, um Daten zu aggregieren und zu verteilen, sollten sie eine andere Struktur haben. Im Beispielsschema sind befinden sich die Verkaufsabteilungen unter der Ebene der Zentralverwaltung, die Budget- und Finanzabteilungen enthält. Diese Struktur unterscheidet sich wahrscheinlich von der Struktur, die verwendet wird, um Arbeitsgänge für die Verkaufsabteilungen zu verwalten. Nur eine Organisationshierarchie kann einem Budgetplanungsprozess zugewiesen werden. 

Weitere Informationen zu den finden Sie unter [Organisationen und Organisationshierarchien](/dynamics365/operations/organization-administration/organizations-organizational-hierarchies).

### <a name="user-security"></a>Benutzersicherheit

Budgetplanung kann einem von zwei Sicherheitsmodellen folgen, um Benutzerrechte zu definieren. Um das Sicherheitsmodell anzugeben, legen Sie auf der Seite **Budgetplanungskonfiguration** einem Budgetplanungsparameter fest.

### <a name="budget-planning-workflows-stages"></a>Budgetplanungsworkflowphasen

Budgetplanungsworkflows werden zusammen mit Budgetierungsworkflows verwendet, um die Erstellung und Entwicklung von Budgetplänen zu verwalten.

Ein Budgetplanungsworkflow besteht aus einer geordneten Menge von Phasen, die ein Budgetplan durchläuft. Jeder Budgetplanungsworkflow wird einem Budgetierungsworkflow zugeordnet. Budgetierungsworkflows sind einer der Workflowtypen, die in Microsoft Dynamics 365 for Operations verwendet werden. Der Budgetierungsworkflow leitet können Sie den Budgetplan, zusammen mit Arbeitsblättern, Begründungen und Anlagen, automatisch durch die Organisation zur Prüfung und Genehmigung weiterleiten. 

Sie erstellen den Budgetplanungsworkflow im Abschnitt **Workflowphasen** auf der Seite **Budgetplanungskonfiguration**. Dort können Sie die Phasen und den Budgetierungsworkflow auswählen, der verwendet wird, und auch zusätzliche Einstellungen konfigurieren. 

Eine bewährte Methode ist das Erstellen eines Budgetplanungsworkflows für jedes Ebene einer Budgetplanungshierarchie. Sie weisen dann einen Budgetierungsworkflow zu, der Elemente enthält, die den Phasen im Budgetplanungsworkflow entsprechen. Im Beispielschema früher im Artikel wird ein Budgetplanungsworkflow für die Verkaufsabteilung erstellt, und ein anderes für den Hauptsitz. Ein Budgetierungsworkflow verschiebt die Budgetpläne durch die Phasen. 

Sie erstellen den Budgetierungsworkflow für die Budgetplanung auf der Seite **Budgetierungsworkflows**. Der Vorgang ähnelt dem Vorgang zum Erstellen anderer Workflows in Microsoft Dynamics 365 for Operations. Die folgende Abbildung zeigt das Beispiel eines Hauptsitzworkflows. 

[![Budgetierungsworkflow für Budgetplanung](./media/budgetingworkflowforbudgetplanning-300x300.png)](./media/budgetingworkflowforbudgetplanning.png) 

Der Workflow umfasst Elemente für die Zuordnung zu den Verkaufsabteilungen und zur Aggregation ihrer Unterordnungen, Prüfung durch den Budget-Manager, Genehmigung durch den Leiter der Finanzabteilung und Phasenübergänge zwischen jeder Phase. 

Sie weisen den Budgetierungsworkflow jedem Budgetplan im Abschnitt **Workflowphasen** auf der Seite **Budgetplanungskonfiguration** zu.

### <a name="parameters-scenarios-and-stages"></a>Parameter, Szenarien und Phasen

Mit den ersten Einstellungen auf der Seite **Budgetplanungskonfiguration** können Sie mehrere Bausteine für spätere Konfigurationsschritte erstellen:

-   **Parameter** - Parameter definieren die Sicherheitsregeln, die Sie auf Budgetpläne anwenden möchten, und die Standardfinanzdimensionen, die verwendet werden sollen, wenn Benutzer die Budgetplanszenariobeträge detailiert anzeigen.
-   **Szenarien** - Szenarien umfassen die Kategorien von Daten, die Sie für die Budgetpläne möchten. Sie definieren Budgetplanszenarien, um monetäre und anderen Maßeinheitsklassen, wie Menge zu unterstützen. In einem Budgetplan stellen Szenarien eine Version der Budgetplanungsdaten dar. Beispiele für Währungsbudgetplanszenarien umfassen das Verkäufe des Vorjahres und unterzeichneten Verträge. Beispiele von Szenarien, die Mengen verwenden, umfassen die Anzahl von Auftragsanrufen und die Vollzeitäquivalent (FTE)-Anzahl.
-   **Phasen** - Phasen definieren die Schritte, denen ein Budgetplan von seinem Beginn bis zur abschließenden Genehmigung folgt. Beispiele für Budgetplanungsphasen enthalten HQ-Rollup, Überprüfung durch den Leiter der Finanzabteilung und Abschluss.

### <a name="allocation-schedules"></a>Zuteilungszeitpläne

In der Budgetplanung können Sie die Beträge zuweisen oder Mengen auf den Budgetplanpositionen von einem Szenario zum anderen oder sogar dem gleichen Szenario verschieben. Beispielsweise wiesen Sie möglicherweise zum gleichen Szenario zu, wenn Sie Änderungen an den Finanzdimensionen oder Datumsangaben der Beträge in diesem Szenario anwenden möchten. Eine Zuteilung kann innerhalb eines Budgetplans oder von einem Budgetplan zum anderen durchgeführt werden. 

Zuteilungszeitpläne weisen Budgetplanpositionen während der Workflowverarbeitung automatisch zu. Sie können Zuteilungen ausführen, indem Sie eine folgenden Methoden in der Liste **Zuordnungsmethode** werden:

-   **Auf Perioden verteilen** - Sie verwenden den Planzahlenverteilungsschlüssel, um Budgetplanpositionen von den Quellbudgetplanszenarioperioden im Zielszenario zuzuteilen. **Hinweis:** Bevor Sie auf Perioden verteilen können, müssen Sie Planzahlenverteilungsschlüssel auf der Seite ****Planzahlenverteilungskategorien**** einrichten.
-   **Zu Dimensionen zuordnen** - Die Budgetplanpositionen werden vom Quellbudgetplanszenario in den Finanzdimensionen im Zielszenario zugewiesen. **Hinweis:** Bevor Sie auf die Dimensionen zuteilen können, müssen Sie Budgetzuweisungsbedingungen auf der Seite ****Budgetzuweisungsbedingungen**** einrichten.
-   **Zusammenführen** - Die Budgetplanpositionen werden aus dem Quellbudgetplanszenario in zugeordneten Budgetplänen auf das Zielszenario in den übergeordneten Budgetplan verteilt.
-   **Verteilen** - Die Budgetplanpositionen werden aus dem Quellbudgetplanszenario im übergeordneten Budgetplan auf das Zielszenario in den zugehörigen Budgetplänen verteilt.
-   **Sachkonto-Zuordnungsregeln verwenden** - Die Budgetplanpositionen werden vom Quellbudgetplanszenario auf Grundlage der ausgewählten Sachkonto-Zuordnungsregel auf das Zielbudgetplanszenario verteilt.
-   **Aus Budgetplan kopieren** - Sie können einen anderen Budgetplan auswählen, den Sie als Quelle der Zuordnung verwenden.

### <a name="stage-allocations"></a>Phasenzuteilungen

Phasenzuteilungen werden verwendet, um Budgetplanpositionen während des Workflowverarbeitens zuzuordnen. Wenn Phasenzuteilungen verwendet werden, können Budgetplanpositionen im Zielszenario ohne Eingreifen des Budgetplanantragstellers oder -Überprüfers erstellt und geändert werden, um die Positionen zu erstellen.

Wenn Sie eine Phasenzuteilung einrichten, ordnen Sie den Budgetplanungsworkflow zu und stellen ihn mit dem Zuteilungszeitplan bereit. Der Budgetplanungsworkflow muss einem Budgetierungsworkflow zugeordnet sein, der die automatisierte Workflowaufgabe ****Zuteilung für Budgetplanungsphase**** verwendet. Wenn der Workflow die angegebene Phase erreicht, tritt die Zuweisung automatisch auf. Diese automatisierte Aufgabe kann verwendet werden, um Budgetplanpositionen in einem neuen Szenario zu erstellen. 

Im Beispielsschema früher im Artikel, wird eine Zuordnung ausgeführt, um Beträgen von einem Budgetplan und von Szenarien in der Basislinienphase der Zentralverwaltung zu einem anderen Budgetplan und Szenarien in der Vorkalkulationsphase der Verkaufsabteilung zu übertragen. Die folgende Abbildung zeigt den relevanten Abschnitt des Beispielsschemas.

[![Phasenzuteilungen](./media/stageallocation-204x300.png)](./media/stageallocation.png) 

Außerdem wird im Beispielsschema eine Aggregation von Budgetplänen und Szenarios in der Phase "Übermittelt" der Verkaufsabteilung zu einem übergeordneten Plan in der Rollupphase der Zentralverwaltung ausgeführt. Die folgende Abbildung zeigt den relevanten Abschnitt des Beispielsschemas.

[![Aggregation](./media/aggregation-109x300.png)](./media/aggregation.png)

### <a name="priorities"></a>Prioritäten

Sie können optional Budgetplanprioritäten verwenden, um Kategorien und Ziele für die Budgetpläne zu definieren, die Sie eingerichtet haben. Sie können Prioritäten auch verwenden, um mehrere Budgetpläne zu organisieren, zu klassifizieren und zu bewerten. So können Sie beispielsweise eine Budgetplanungspriorität für Status und Sicherheit erstellen und dann Budgetpläne überprüfen, die dieser Priorität zugewiesen werden. Sie können auch eine Zahl zuweisen, um Budgetpläne alle Budgetpläne übergreifend einzustufen.

### <a name="columns-and-layouts"></a>Spalten und Layouts

Budgetzahlen werden in einem Budgetplan in den Zeilen und Spalten angezeigt. Sie müssen erst die Spalten definieren, anschließend können Sie ein Layout erstellen, um die Darstellung der Spalten zu definieren. 

Wenn Sie eine Spalte definieren, wählen Sie ein Budgetplanszenario aus. Die Positionsbeträge von diesem Szenario werden im Budgetplan angezeigt. Sie können eine Periode auswählen, um den Betrag zu filtern, und Sie können auch Filter anwenden, die auf dem Sachkonto basieren. 

Wenn Sie ein Layout definieren, wählen Sie eine Sachkontodimension aus, die, um die Budgetplanzeilen zu erstellen, die Sie anzeigen möchten, und wählen Sie die Spalten als Layoutelemente aus. Sie können mehrere Layouts erstellen, damit ein Budgetplan die gewünschten Daten in unterschiedlichen Phasen des Budgetplanungsprozesses anzeigt. 

Zusätzlich zu den Spalten für Budgetbeträge können Sie Spalten für die Felder "Projekt", "Vorgeschlagene Projekt", "Anlage" und "Vorgeschlagene Anlage" vom Budgetplan definieren. Sie können eine Spalte für Budgetpositionen definieren. Diese Option ist überaus nützlich, wenn Sie Mitarbeiterbudgets analysieren müssen. 

Für das Beispielschema sollten Sie Spalten für die Vertriebs-, -Vertrags- und Prognoseszenarien des Vorjahres erstellen (die folgende Abbildung zeigt die relevanten Abschnitt des Schemas). Sie können eins oder alle dieser Szenarien in separate Spalten für jedes Quartal des Geschäftsjahrs aufteilen, sodass der Leiter der Verkaufsabteilung genaue Planungsbeträge für jede Periode eingeben kann.

[![Spalten](./media/columns.png)](./media/columns.png) 

Sie legen auch fest, ob jedes Layoutelement (Spalte) bearbeitbar ist und ob es in einer beliebigen Arbeitsblattvorlage verfügbar ist, die für dieses Layout erstellt wird. Im Layout, das im Beispielschema für die Vorkalkulationsphase verwendet wird, sind die Planungsspalten bearbeitbar, während die Spalten für Verkauf und Vertrag des Vorjahres schreibgeschützt sind.

### <a name="templates"></a>Vorlagen

Im **Layouts**-Bereich der Seite **Budgetplanungskonfiguration**, können Sie auch Excel-Vorlagen generieren, anzeigen oder hochladen. Diese Vorlagen sind die Arbeitsmappen, die mit jedem Budgetplan verknüpft werden, um zusätzliche Analyse-, Diagrammerstellung- und Dateneingabefunktionen bereitzustellen. 

Sie können eine Vorlage für jedes Layout generieren, anzeigen oder hochladen. Wenn eine Vorlage generiert wird, wird das Layout gesperrt und kann nicht bearbeitet werden. Diese Sperre stellt sicher, dass das Vorlagenformat mit dem Layout des Budgetplans übereinstimmt und dieselben Daten umfasst. Nachdem eine Vorlage generiert wurde, kann sie angezeigt und bearbeitet werden. Sie können der Vorlage z. B. Diagramme hinzufügen oder die Darstellung weiter anpassen.

> [!NOTE] 
> Die Vorlage soll in einem Speicherort gespeichert werden, auf den der Benutzer Zugriff hat, damit sie zum Layout hochgeladen werden kann, nachdem die Bearbeitung abgeschlossen ist. Auf diese Weise wird die Vorlage mit Budgetplänen verwendet, die das Layout verwenden.

### <a name="descriptions"></a>Beschreibungen

Die Beschreibungen, die Sie im Bereich **Layouts** zugewiesen können, werden verwendet, um den Namen einer Finanzdimension anzuzeigen, die in einem Layout enthalten ist. Eine Organisation möchte z. B. den Namen des Hauptkontos in einem Budgetplan neben der Hauptkontonummer anzeigen, aber die Namen anderer Finanzdimensionen auslassen, um die Anzeige nicht zu überfüllen.

## <a name="setting-up-budget-planning-processes"></a>Einrichten von Budgetplanungsprozessen

Nachdem Sie die Konfiguration der Budgetplanung abgeschlossen haben, können Sie Budgetplanungsprozesse auf der Seite **Budgetplanungsprozess** einrichten. Budgetplanungsprozesse sind ein Satz Regeln, die bestimmen, wie Budgetpläne in der Budgetplanungs-Organisationshierarchie aktualisiert, weitergeleitet, geprüft und genehmigt werden können. 

Für jeden Budgetplanungsprozess wählen Sie zunächst einen Budgetzyklus und ein Sachkonto aus. Jeder Budgetplanungsprozess bezieht sich nur auf einen Budgetzyklus und ein Sachkonto. Dann wählen Sie die Budgetorganisationshierarchie im Inforegister **Budgetplanungsprozess-Verwaltung** und, weisen allen Zuständigkeitseinheiten in der Organisation, die im Raster angezeigt werden, einen Budgetplanungsworkflow zu. 

Um Sie den Budgetplanungsworkflow für ähnliche Zuständigkeitseinheiten zuzuweisen oder zu ändern, klicken Sie auf **Workflow zuweisen**, und wählen Sie dann den zu verwendenden Organisationstyp und den Budgetplanungsworkflow aus. Die Budgetierungsworkflow-Kennung, die jedem Budgetplanungsworkflow zugeordnet ist, wird dem Raster automatisch hinzugefügt. 

Wenn Sie die Phasenregeln und Vorlagen im Inforegister **Regeln und Layouts für die Budgetplanungsphase** definieren, können Sie eine andere Gruppe von Regeln und Standardlayouts für jede Budgetplanungsphase definieren. Beispielsweise kann die Vorkalkulationsphase der Verkaufsabteilung Benutzer die Positionen in einem Budgetplan ändern lassen, aber Benutzer am Hinzufügen von Positionen hindern. In der Phase "Übermittelt" können Benutzer Positionen anzeigen lassen, diese aber nicht hinzufügen oder bearbeiten, da die Arbeit zu diesem Zeitpunkt abgeschlossen wurde und Änderungen an den Budgetplänen vermieden werden müssen. Um die Layouts auswählen, die für Budgetpläne verfügbar sind, klicken Sie auf **Alternative Layouts**. 

Sie können Budgetplanungsprioritäten optional auf dem Inforegister **Budgetplanprioritäts-Einschränkungen** auswählen. Prioritäten können dann auf Budgetplänen ausgewählt werden. 

Der letzte Schritt ist die Aktivierung des Budgetplanungsprozesses über das Menüs **Aktivitäten** Ein Budgetplanungsprozess kann nicht verwendet werden, bis er aktiviert wurde. 

Im Menü **Aktivitäten** können Sie auch einen neuen Prozess erstellen, indem Sie einen vorhandenen Prozess kopieren. Diese Funktion ist hilfreich für Organisationen, die bei jedem Budgetzyklus dem gleichen Prozessfluss folgen und nur wenigste oder gar keine Änderungen vornehmen. 

Ein anderer nützlicher Befehl im Menü **Aktivitäten** ist **Budgetprozessstatus anzeigen**. Dieser Befehl stellt die Budgetpläne innerhalb eines Prozesses zusammen mit relevanten Daten, wie den Workflowstatus der Pläne, Zusammenfassungen nach Betrag und nach Einheit sowie Navigation zu den Budgetplänen grafisch dar.

[![Status des Budgetplanungsprozesses](./media/budgetplanningprocessstatus-300x171.png)](./media/budgetplanningprocessstatus.png)




