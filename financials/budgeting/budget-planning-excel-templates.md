---
title: "Budgetplanungsvorlagen für Excel"
description: "In diesem Thema wird beschrieben, wie Microsoft Excel-Vorlagen erstellt, die mit Budgetplänen verwendet werden können."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 0e2eb6e7c130f03edbf60a185d397d94b5d61d7d
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning-templates-for-excel"></a>Budgetplanungsvorlagen für Excel

In diesem Thema wird beschrieben, wie Microsoft Excel-Vorlagen erstellt, die mit Budgetplänen verwendet werden können.

Dieses Thema zeigt, wie Excel-Vorlagen von erstellt, die mit Budgetplänen mithilfe des Standarddemodatsatzes und der Benutzer Admin-Anmeldung verwendet werden. Weitere Informationen zu Budgetplanung, finden Sie Budgetplanungsüberblick [] () budget-planning-overview-configuration.md. Sie können auch auf das das Budget, [101] plant das Lernprogramm "budget-plan.md,), um die Grundeinstellungsmodulkonfigurations- und -Verwendungsprinzipien zu ermitteln.

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a>Generieren eines Arbeitsblatts mithilfe des Budgetplan dokumentlayouts
Budgetplandokumente können mithilfe einer oder mehrerer Layouts angezeigt und bearbeitet werden. Jedes Layout kann eine zugeordnete Budgetplandokumentvorlage, haben, um die Budgetplandaten in einer Excel-Kalkulationstabelle anzuzeigen und zu bearbeiten. In diesem Thema wird eine Budgetplandokumentvorlage mit einer vorhandenen Layoutkonfiguration generiert. Öffnen Sie Budgetplanliste ** ** **( Planung ** **&gt; Budgetpläne ** ). ** Auf neu ** um einen neuen Budgetplandokuments zu erstellen. ![bpt1 ([]. /media/bpt11-1024x552.png)]". /media/bpt11.png) 

Mithilfe die ** Hinzufügen ** Positionsoption, Positionen hinzuzufügen. ** Auf Layouts ** um die Budgetplandokument-Layoutkonfiguration anzuzeigen. 
![bpt2 ([]. /media/bpt2-1024x274.png)]". /media/bpt2.png) 

Sie können die Layoutkonfiguration wiederholen und nach Bedarf anpassen. Wechseln Sie ** Vorlage ** &gt; ** generieren ** eine Excel-Datei für dieses Layout erstellen. Nachdem die Vorlage generiert wurde, fahren ** Vorlage ** &gt; ** Ansicht ** die Budgetplandokumentvorlage öffnen und wiederholen. Auf der Excel-Datei zu Ihrem lokalen Laufwerk speichern. ![bpt3 ([]. /media/bpt3-1024x545.png)]". /media/bpt3.png) 

> [!NOTE] 
> Das Budgetplandokumentlayout kann nicht geändert werden, nachdem eine ihr Tabelle zugeordnet ist. Zum Ändern des Layouts, löschen Sie die zugeordnete Excel-Vorlagendatei und Schaltfläche können Sie sie. Dies ist erforderlich, um die Felder im synchronisierten Layout und im Arbeitsblatt zu halten. 

Die übertreffungs-Vorlage enthält alle Elemente aus dem Budgetplandokumentlayout, in dem die im Arbeitsblatt ** verfügbar ** Spalte auf Wahr festgelegt wird. Überlappende Elemente werden in der Tabelle " nicht zulässig. Falls aus dem Layout Spalten der Anforderung M1, der Anforderung M2, der Anforderung Q3 und der Anforderung Q4 enthält, und Anforderungsspalte eine gesamte, die eine Summe aller Spalten 4 vierteljährlichen darstellt, die nur Spalten oder vierteljährlichen die gesamte Spalte verfügbar ist, der Tabelle in verwendet werden. Die überlappende Spalten Excel-Datei kann nicht für die Aktualisierung zu aktualisieren, da Daten in der Tabelle veraltet und ungenau werden können.

![bpt4 ([]. /media/bpt4-1024x615.png)]". /media/bpt4.png)

> [!NOTE] 
> Um mit Potentialabgänge Anzeigen und Bearbeitungsbudgetplandaten mithilfe Excel zu vermeiden, sollte der Benutzer in Dynamics 365 für Arbeitsgänge und die Add-In-Datenkonnektor Microsoft Dynamics Public-Vorlage Office protokolliert werden.

## <a name="add-a-header-to-budget-plan-document-template"></a>Hinzufügen eines Budgetplandokumentvorlage Kopf hinzu
Weitere Kopfdaten hinzufügen, die obere Reihe der leere Zeilen in der Excel-Datei und der Sie auswählen. ** Auf Entwurf ** in Datenkonnektor ** ** um die Kopffeldern der Excel-Datei hinzuzufügen.

![bpt5 ([]. /media/bpt5-1024x615.png)]". /media/bpt5.png) 

Klicken Sie im Formular Entwurf ** ** Registerkarte ** ** auf ** Hinzufügen ** Felder und wählen dann BudgetPlanHeader ** ** als die Entitätsdatenquelle aus.

![bpt6 ([]. /media/bpt6-1024x615.png)]". /media/bpt6.png)

Hier dem Cursor auf den gewünschten Lagerplatz in der Excel-Datei. ** Auf fügen Sie Beschriftung hinzu ** um die Feldbezeichnung dem ausgewählten Ort hinzuzufügen. Wählen Sie Hinzufügen ** Sie Werte aus ** um den Wertfeld dem ausgewählten Ort hinzuzufügen. ** ** Auf erfolgt auf Designer zu schließen.

## <a name="bpt7mediabpt7pngmediabpt7png"></a>![bpt7 ([]. /media/bpt7.png)]". /media/bpt7.png)

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a>Hinzufügen einer Spalte Budgetplandokumentvorlagentabelle berechneten hinzu
--------------------------------------------------------------

Nächste berechnete, Spalten sind zu generierten Budgetplandokumentvorlage hinzugefügt. A ** gesamte Anforderung ** Spalte, die Notwendigkeit M1 zusammengefasst: Angebotsanforderung Sie Spalten Q4 und eine Regulierung ** ** Spalte, die die gesamte Spalte ** ** Anforderung von einem vordefinierten Faktor neu berechnen soll.

** Auf Entwurf ** in Datenkonnektor ** ** dem von Spalten zum Tabelle hinzuzufügen. ** Auf Bearbeiten ** neben ** BudgetPlanWorksheet ** der Datenquelle, zum Hinzufügen von Spalten zu starten.

![bpt8 ([]. /media/bpt8-1024x301.png)]". /media/bpt8.png) 

Die Feldgruppe wird die ausgewählte Spalten an, die in die Vorlage verfügbar sind. ** Auf Formel ** um eine neue Spalte hinzuzufügen. Name der neuen Spalte und fügen dann die Formel ** ** Formel in das Feld ein. ** Aktualisierung auf ** um die Spalte eingefügt.

![bpt12 ([]. /media/bpt12-1024x565.png)]". /media/bpt12.png)

> [!NOTE] 
> Soll die Formel festzulegen, erstellen die Formel in Arbeitsblatt und kopieren sie an den Entwurf ** ** Fenster. Dynamics 365 für Arbeitsgänge gebundene Tabelle ist in der Regel "AXTable1". Beispielsweise Anforderung M1 zusammenfassen: Angebotsanforderung Q4 Sie Spalten im Arbeitsblatt, die Anforderung Q4 Formel =\]AxTable1\[der Anforderungs-\]+AxTable1\[Anforderungs-Q2\]+AxTable1\[der Anforderungs-\]+AxTable1\[.

Wiederholen Sie diese Schritte, um die Regulierung ** ** Spalte eingefügt. Mithilfe Sie Formel = Gesamte Anforderung \]\*$I$1 AxTable1\[für diese Spalte. Dieses wird der Wert in Zelle I1 multipliziert und die Werte in der Anforderung ** ** gesamte Spalte Ausgleichsbeträge, um zu berechnen.

Speichern und schließen Sie die Excel-Datei. Zurückkehren zu Dynamics 365 für Arbeitsgänge und in ** Layouts **, auf Vorlagen-Upload &gt; ** zurück ** um die gespeicherte für den Budgetplan verwendet werden) hochzuladen Tabelle. 

![bpt10 ([]. /media/bpt10-1024x352.png)]". /media/bpt10.png) 

** Schließen des Layouts ** Schieberegler. ** Budgetplan ** im Dokument klicken Sie ** Arbeitsblatt ** um das Dokument in Excel anzeigen und bearbeiten. Beachten Sie, dass die angepasste Tabelle wurde verwendet, um dieses Budgetplanarbeitsblatt erstellen und berechneten Spalten mithilfe der Produktion aktualisiert werden, die in den vorherigen Schritten definiert wurden. 

![bpt11 ([]. /media/bpt111-1024x431.png)]". /media/bpt111.png)

## <a name="tips--tricks-for-creating-budget-plan-templates"></a>Tipps). Tricks für das Erstellen von Budgetplanvorlagen
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a>Kann ich zusätzliche Datenquellen in eine Budgetplanvorlage hinzufügen und verwendet?

Ja, können Sie das verwenden ** Entwurf ** Menü, um weitere Entitäten dem gleichen oder andere der Tabelle in Bilanzen hinzuzufügen. So können Sie die BudgetPlanProposedProject ** ** Datenquelle hinzufügen, um eine Liste mit vorgeschlagenen Projekte gleichzeitig erstellen und verwalten wenn mit Budgetplandaten in Excel. Notieren Sie das Großseriendatenquellen einschließlich könnte der Excel-Arbeitsmappe Leistung auswirken. 

Sie können die Filter ** ** Option in verwenden Datenkonnektor ** ** gewünschten Filter zusätzlichen Datenquellen hinzuzufügen.

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a>Kann ich die Designoption im Datenkonnektor für andere Benutzer ausblenden?

Ja öffnen, die Datenkonnektor ** ** Optionen, die ** Entwurf ** Option von anderen Benutzern auszublenden.

![bpt13 ([]. /media/bpt13-1024x565.png)]". /media/bpt13.png)

Erweitern ** Datenkonnektoroptionen ** und deaktivieren das ** Entwurf ** Kontrollkästchen aktivieren. Dies blendet die ** Entwurf ** Option aus Datenkonnektor ** **.

![bpt14 ([]. /media/bpt14-1024x592.png)]". /media/bpt14.png)

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a>Kann ein Benutzer an den Datenkonnektor bei Arbeit versehentlich schließen verhindern mit Daten?

Es wird empfohlen, die Vorlage zu sperren, um Benutzer an Abschließen der zu verhindern. Um die Sperre zu aktivieren, klicken Sie auf Datenkonnektor ** **, in der oberen rechten Ecke, mit einem Pfeil wird. 

![bpt15 ([]. /media/bpt15-1024x285.png)]". /media/bpt15.png) 

Klicken auf den Pfeil für ein weiteres Menü. Wählen Sie aus ** Sperre **.

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a>![bpt16 ([]. /media/bpt16-1024x614.png)]". /media/bpt16.png)

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a>Kann ich andere Excel-Funktionen, z Zellenformatierung, Farben, bedingte Formatierung und Diagramme mit Budgetplanvorlagen Auftrag verwendet?

Ja, die meisten Standard-Excel-Funktionen arbeitet in den Budgetplanvorlagen. Es wird empfohlen mithilfe der Farbkennung, damit Benutzer unter den Lesezugriff bearbeitbaren unterscheiden und Spalten. Bedingte Formatierung kann verwendet werden, die beim Identifizieren problematischer Bereiche des Budgets hervorzuheben. Spaltensummen können leicht dargestellt werden, indem Standard-Excel-Formeln über der Tabelle verwendet.

Sie können zusätzliche für Pivottabellen und Diagramme Gruppierungen und Visualisierungen von Budgetdaten auch erstellen und verwenden. ** ** Daten auf der Registerkarte in der ** Verbindungen ** Gruppe, klicken auf ** Aktualisieren aller ** und dann Verbindungs-Eigenschaften ** **. Klicken Sie auf die Registerkarte. ** ** Verwendung ** Aktualisierung unter **, aktivieren Sie das ** Aktualisieren von Daten, wenn Sie die Datei öffnen ** Kontrollkästchen. 

![bpt17 ([]. /media/bpt17-1024x614.png)]". /media/bpt17.png)


