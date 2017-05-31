---
title: "Budgetplanungsvorlage für Excel"
description: "In diesem Thema wird beschrieben, wie Microsoft Excel-Vorlagen erstellt werden, die mit Budgetplänen verwendet werden können."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 93aa0aeffad0411542f36e27745f63198c4438b2
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="budget-planning-templates-for-excel"></a>Budgetplanungsvorlage für Excel

[!include[banner](../includes/banner.md)]


In diesem Thema wird beschrieben, wie Microsoft Excel-Vorlagen erstellt werden, die mit Budgetplänen verwendet werden können.

Dieses Thema zeigt, wie Excel-Vorlagen erstellt werden, die mit Budgetplänen mithilfe des Standarddemodatsatzes und der Benutzer Admin-Anmeldung verwendet werden. Weitere Informationen zu Budgetplanung, finden Sie unter [Budgetplanungsüberblick](budget-planning-overview-configuration.md) Sie können auch auf das Lernprogramm [Budgetplanung 101](budget-plan.md) zugreifen, um die Grundeinstellungsmodulkonfigurations- und -Verwendungsprinzipien zu ermitteln.

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a>Erstellt ein Arbeitsblatt mithilfe der Budgetplandokumentvorlage.
Budgetplandokumente können mithilfe einer oder mehrerer Layouts angezeigt und bearbeitet werden. Jedes Layout kann eine zugeordnete Budgetplandokumentvorlage haben, um die Budgetplandaten in einer Excel-Kalkulationstabelle anzuzeigen und zu bearbeiten. In diesem Thema wird eine Budgetplandokumentvorlage mit einer vorhandenen Layoutkonfiguration generiert. Öffnen Sie**Budgetplanliste** (**Planung**&gt; **Budgetplan**). Klicken Sie auf **Neu**, um einen neuen Budgetplan zu erstellen. [![bpt1](./media/bpt11-1024x552.png)](./media/bpt11.png) 

Mithilfe der Zeilenoption **Hinzufügen** fügen Sie Zeilen hinzu. **Layouts** klicken, um die Budgetplandokument-Layoutkonfiguration anzuzeigen. 
[![bpt2](./media/bpt2-1024x274.png)](./media/bpt2.png) 

Sie können die Layoutkonfiguration anschauen und nach Bedarf anpassen. Wechseln Sie zu **Vorlage** &gt; **Erstellen**, um eine Excel-Datei für dieses Layout zu erstellen. Nachdem die Vorlage generiert wurde, gehen Sie zu **Vorlage** &gt; **Ansicht**, um die Budgetplandokumentvorlage zu öffnen und zu wiederholen. Sie können die Excel-Datei auf Ihrem lokalen Laufwerk speichern. [![bpt3](./media/bpt3-1024x545.png)](./media/bpt3.png) 

> [!NOTE] 
> Das Budgetplandokumentlayout kann nicht geändert werden, nachdem ihr eine Excel-Tabelle zugeordnet wurde. Um das Layout zu ändern, löschen Sie die zugeordnete Excel-Vorlagendatei und erstellen Sie diese neu. Dies ist erforderlich, um die Felder im synchronisierten Layout und im Arbeitsblatt zu halten. 

Die Excel-Vorlage enthält alle Elemente aus dem Budgetplandokumentlayout, in dem die Spalte **Verfügbar im Arbeitsblatt** auf "True" festgelegt ist. Überlappende Elemente sind in der Excel-Tabelle nicht zulässig. Wenn beispielsweise das Layout Spalten der Anforderung Q1, der Anforderung Q2, der Anforderung Q3 und der Anforderung Q4 enthält, und Anforderungsspalte eine gesamte, die eine Summe aller Spalten 4 vierteljährlichen darstellt, die eine Summe aller 4 Quartalsspalten enthält oder wenn die Totalspalte zur Verwendung in der Excel-Vorlage bereit steht. Die Excel-Datei kann keine überlappenden Spalten während der Aktualisierung aktualisieren, da Daten in der Tabelle veraltet und ungenau werden könnte.

[![bpt4](./media/bpt4-1024x615.png)](./media/bpt4.png)

> [!NOTE] 
> Um mögliche Probleme beim Anzeigen und Bearbeiten von Budgetplandaten mithilfe von Excel zu vermeiden, sollte der Benutzer in Dynamics 365 for Operations und in Microsoft Dynamics Office Add-in Data Connector.angemeldet sein.

## <a name="add-a-header-to-budget-plan-document-template"></a>Der Budgetplandokumentvorlage eine Kopfzeile hinzufügen
Um weitere Kopfzeilen hinzuzufügen, wählen Sie die oberste Zele in der Excel-Datei und fügen Sie die leere Zeile hinzu. Klicken Sie im **Datenkonnektor** auf **Design**, um Kopfzeilenfelder dem Excel hinzuzufügen.

[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png) 

Klicken Sie in der Registerkarte **Design** auf Felder **hinzufügen** und wählen Sie dann  **BudgetPlanHeader** als Entitätsdatenquelle aus.

[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)

Gehen Sie mit dem Cursor auf den gewünschten Ort in der Excel-Datei. Klicken Sie auf  **Beschriftung hinzufügen**, um die Feldbezeichnung dem ausgewählten Ort hinzuzufügen. Wählen Sie **Wert hinzufügen**, um die Wertefelder am ausgewählten Ort hinzuzufügen. Klicken Sie anschließend auf **Fertig**, um den Designer zu beenden.

## <a name="bpt7mediabpt7pngmediabpt7png"></a>[![bpt7](./media/bpt7.png)](./media/bpt7.png)

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a>Der Budgetplandokumentvorlagentabelle eine berechnete Spalte hinzufügen
--------------------------------------------------------------

Nächste berechnete Spalten werden der zu generierenden Budgetplandokumentvorlage hinzugefügt. Eine Spalte **Gesamte Anforderung**, die die Anforderung Q1 zusammenfasst: Anforderung Q4 Spalten und eine Spalte **Anpassung**, die die Spalte **Total Anforderung** durch einen vordefinierten Faktor berechnet.

Klicken Sie im **Datenkonnektor** auf **Design**, um Spalten dem Excel hinzuzufügen. Klicken Sie neben dem **BudgetPlanWorksheet** auf **Bearbeiten**, um Spalten hinzuzufügen.

[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png) 

Die ausgewählte Feldgruppe zeigt die Spalten an, die in der Vorlage verfügbar sind. Klicken Sie auf **Formular**, um einen neuen Code manuell hinzuzufügen. Geben Sie der neuen Spalte einen Namen und fügen dann die Formel in das Feld **Formel** ein. Klicken Sie auf **Aktualisieren**, um die Spalte einzufügen.

[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)

> [!NOTE] 
> Um die Formel zu definieren, erstellen Sie die Formel im Arbeitsblatt und kopieren sie dann in das Fenster**Design**. Eine an Dynamics 365 for Operations gebundene Tabelle ist in der Regel ein "AXTable1". Um beispielsweise die Anforderung Q1 zusammenfassen: Fordern Sie die Spalten Q4 in der Tabelle an, die Formel  = AxTable1\[Request Q1\]+AxTable1\[Request Q2\]+AxTable1\[Request Q3\]+AxTable1\[Request Q4\].

Wiederholen Sie diese Schritte, um die Spalte**Regulierung** hinzuzufügen. Mithilfe der Formel = AxTable1\[Total request\]\*$I$1 für diese Spalte. Dadurch wird der Wert in Zelle I1 multipliziert und die Werte in der Spalte **Anforderung gesamt**, um die Regulierungsbeträge zu berechnen.

Speichern und schließen Sie die Excel-Datei. Kehren Sie zu Dynamics 365 for Operations zurück. Klicken Sie unter **Layouts** auf **Template &gt; hochladen**, um die gespeicherte Excelvorlage für den Budgetplan zu verwenden. 

[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png) 

Schließen -Sie den **Layouts**-Schieberegler. Im Dokument **Budgetplan** klicken Sie auf **Arbeitsblatt**, um das Dokument in Excel anzeigen und bearbeiten. Beachten Sie, dass die angepasste Excel-Tabelle verwendet wurde, um dieses Budgetplanarbeitsblatt erstellen und die berechneten Spalten mithilfe der Produktion aktualisiert werden, die in den vorherigen Schritten definiert wurden. 

[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)

## <a name="tips--tricks-for-creating-budget-plan-templates"></a>Tipps und Tricks für das Erstellen von Budgetplanvorlagen
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a>Kann ich zusätzliche Datenquellen in eine Budgetplanvorlage hinzufügen und verwendet?

Ja, Sie können das Menü **Design**verwenden, um weitere Entitäten dem gleichen oder anderen Arbeitsblättern der Excel-Tabelle hinzuzufügen. So können Sie die Datenquelle **BudgetPlanProposedProject** hinzufügen, um eine Liste mit vorgeschlagenen Projekten gleichzeitig zu erstellen und zu verwalten, wenn Sie mit Budgetplandaten in Excel arbeiten. Beachten Sie, das große Datenquellenmengen die Leistung der Excel-Arbeitsmappe beeinträchtigen können. 

Sie können die Option **Filter** im **Datenkonnektor** hinzufügen, um den Datenquellen die gewünschten Filter hinzuzufügen.

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a>Kann ich die Designoption im Datenkonnektor für andere Benutzer ausblenden?

Ja öffnen, die Optionen  **Datenkonnektor**, um die Option **Design** für andere Benutzer auszublenden.

[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)

Erweitern Sie die **Datenkonnektoroptionen** und deaktivieren das Kontrollkästchen **Design aktivieren**. Dies blendet die Option **Design** vom**Datenkonnektor** aus.

[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a>Kann ich Benutzer daran hindern, den Datenkonnektor bei der Arbeit versehentlich zu schließen?

Es wird empfohlen, die Vorlage zu sperren, um Benutzer am Schließen zu hindern. Um die Sperre zu aktivieren, klicken Sie auf den **Datenkonnektor** in der oberen rechten Ecke. Ein erscheint ein Pfeil. 

[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png) 

Klicken auf den Pfeil für ein weiteres Menü. Wählen Sie **Sperren**.

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a>[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a>Kann ich andere Excel-Funktionen, wie Zellenformatierung, Farben, bedingte Formatierung und Diagramme mit Budgetplanvorlagen verwenden?

Ja, die meisten Standard-Excel-Funktionen arbeiten in den Budgetplanvorlagen. Es wird empfohlen, Farbkennung zu verwenden damit Benutzer zwischen Lesezugriff und bearbeitbaren Spalten unterscheiden können. Bedingte Formatierung kann verwendet werden, um problematischer Bereiche des Budgets hervorzuheben. Spaltensummen können leicht dargestellt werden, indem Standard-Excel-Formeln über der Tabelle verwendet. werden.

Sie können zusätzliche Pivottabellen und Diagramme für Gruppierungen und Visualisierungen von Budgetdaten erstellen und verwenden. Klicken Sie in der Registerkarte **Daten** auf der Gruppe **Verbindungen** auf **Alle Aktualisieren** und klicken Sie dann auf **Eigenschaften verbinden**. Klicken Sie auf die Registerkarte **Nutzung**. Unter **Aktualisieren** wählen Sie das Kontrollkästchen **Daten beim Öffnen der Datei aktualisieren** aus. 

[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)




