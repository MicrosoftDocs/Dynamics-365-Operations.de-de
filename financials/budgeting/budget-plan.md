---
title: Budgetplanung
description: "Das Ziel dieser Übungseinheit ist, eine geführte Ansicht von Microsoft Dynamics 365 für Arbeitsgangsfunktionensaktualisierungen im Budget planungsbereich bereitzustellen. Ziel dieser Übungseinheit ist es, ein schnelles Konfigurationsbeispiel für das Budgetplanungsmodul zu illustrieren und zu zeigen, wie die Budgetplanung mithilfe dieser Konfiguration erstellt werden kann.  Diese Übungseinheit bezieht sich speziell auf die folgenden Geschäftsprozesse und Aufgaben - - Organisationshierarchie für Budgetplanung der Informationen der Benutzer - sicherheit Budgetplanszenarien, Budgetplanspalten Layouts Excel-Vorlagen von definierend - und - Budgetplandokument durch Übernehmen in Wirklichkeiten im Hauptbuch beim - mithilfe der Zuweisungen Erstellen und Konfigurieren aktivierenden Budgetplanungsprozess, um Budgetplandokumentdaten anzupassen - Bearbeitungsbudgetplan-Dokumentdaten in Excel"
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 81b44aa7af3a05ebc28963f406fab98bfbbb340d
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning"></a>Budgetplanung

Das Ziel dieser Übungseinheit ist, eine geführte Ansicht von Microsoft Dynamics 365 für Arbeitsgangsfunktionensaktualisierungen im Budget planungsbereich bereitzustellen. Ziel dieser Übungseinheit ist es, ein schnelles Konfigurationsbeispiel für das Budgetplanungsmodul zu illustrieren und zu zeigen, wie die Budgetplanung mithilfe dieser Konfiguration erstellt werden kann.  Diese Übungseinheit bezieht sich speziell auf die folgenden Geschäftsprozesse und Aufgaben - - Organisationshierarchie für Budgetplanung der Informationen der Benutzer - sicherheit Budgetplanszenarien, Budgetplanspalten Layouts Excel-Vorlagen von definierend - und - Budgetplandokument durch Übernehmen in Wirklichkeiten im Hauptbuch beim - mithilfe der Zuweisungen Erstellen und Konfigurieren aktivierenden Budgetplanungsprozess, um Budgetplandokumentdaten anzupassen - Bearbeitungsbudgetplan-Dokumentdaten in Excel 

<a name="prerequisites"></a>Voraussetzungen 
------------------

Dazu Lernprogramm muss das Dynamics 365 für Arbeitsgangsumgebung mit Contoso-Demodaten zugreifen und als Administrator für die Instanz bereitgestellt. Verwenden Sie nicht im Browsermodus privaten für diese - Übungseinheit signieren zum Auschecken aus ein beliebiges anderes Konto im Browser nach Bedarf und unterzeichnet Sie in den Dynamics 365 für Arbeitsgangsadministrator-anmeldeinformationen. Beim Signieren in Dynamics 365 für Arbeitsgänge, überprüfen Sie MÜSSEN ** Sie ** beibehalten "Warnen signiert" im Kontrollkästchen. Dadurch wird ein persistentes Cookie erstellt, das die Excel-App derzeit benötigt. Wenn Sie in das Dynamics 365 für Arbeitsgänge mithilfe eines Browsers anderen als IE signieren, werden Sie aufgefordert, in der Excel-App in zu signieren. Beim Sie auf "Anmelden" in der Excel-App klicken, wird im IE ein Popup- Fenster geöffnet und Sie **MÜSSEN** das Kontrollkästchen "Angemeldet bleiben" aktivieren. Wenn Sie in der Excel-App auf "Anmelden" klicken, und nichts passiert, leeren Sie den Cookie-Zwischenspeicher des IE.

## <a name="scenario-overview"></a>**Scenario overview**
Julia arbeitet als Finanzmanager in Contoso Entertainment Systems in Deutschland (DEMF). Mit dem sich nähernden GJ 2016 muss sie an der Einrichtung des Unternehmensbudgets für das kommende jahr arbeiten. Budgetvorbereitung sieht wie folgt aus:

1.  Julia verwendet Istwerte des Vorjahres als Ausgangspunkt, um das Budget zu erstellen.
2.  Auf Grundlage der Istwerte des Vorjahres erstellt sie Vorkalkulationen für 12 Monate im kommenden Jahr
3.  Julia überprüft das Budget mit dem Leiter der Finanzabteilung. Sobald sie fertig ist, nimmt sie die erforderlichen Regulierungen für den Budgetplan vor und schließt die Budgetausarbeitung ab.

Budgetplanungs-Konfigurationsschema für das Szenario suchen, wie folgt:

![Screenshot 1](./media/screenshot1-300x152.png)

Julia wird folgende Tabelle erstellen, um das Budget:

[![](./media/screenshot2-1024x352.png)](./media/screenshot2.png)

<a name="exercise-1-configuration"></a>Übung 1: Konfiguration
=========================

## <a name="task-1-create-organizational-hierarchy"></a>** Aufgabe: 1 Erstellen Sie Organisationshierarchie **
Da der ganze Budgetierungsprozess in der Finanzabteilung geschieht, muss Julia eine sehr einfache Organisationshierarchie erstellen, die nur aus der Finanzabteilung besteht. 1.1. Navigieren Sie zu den Organisations-Organisationshierarchien &gt; " &gt; Organisationshierarchien " Organisationsverwaltung und klicken Sie auf Neue Schaltfläche

![Screenshot 3](./media/screenshot3.png) 

1.2. Geben Sie den Namen für die Organisationshierarchie ein und Schaltfläche weisen Zweck zu

![Screenshot4 ([]. -/media/screenschuß 4.png)]". -/media/screenschuß 4.png) 

1.3. Wählen Sie aus, Budgetplanungszweck fügen Schaltfläche hinzufügen und weisen neu erstellte Organisationshierarchie zu: 

![Screenshot5 ([]. -/media/screenschuß 5.png)]". -/media/screenschuß 5.png)

1.4. Wiederholen Sie den obigen Schritt für den Zweck der Organisationssicherheit. Schließen Sie das Formular, wenn Sie fertig sind.

![Screenshot6 ([]. -/media/screenschuß 6.png)]". -/media/screenschuß 6.png)

1.5. In der Organisationshierarchieformularklicken-Schaltfläche Ansicht. Klicken Sie im Hierarchie-Designer auf "Bearbeiten", und erstellen Sie eine Hierarchie, indem Sie auf die Schaltfläche "Einfügen" klicken.

![Screenshot7 ([]. -/media/screenschuß 7.png)]". -/media/screenschuß 7.png) 

1.6. Wählen Sie die Finanzabteilung für die Budgethierarchie aus. 

![Screenshot8 ([]. -/media/screenschuß 8.png)]". -/media/screenschuß 8.png)

1.7. Wenn Sie fertig sind, klicken Sie auf die Schaltfläche "Veröffentlichen und schließen". Wählen Sie 1/1/2015 als Gültigkeitsdatum für die Hierarchieveröffentlichung aus.

![Screenshot9 ([]. -/media/screenschuß 9.png)]". -/media/screenschuß 9.png)

## <a name="task-2-configure-user-security"></a>Aufgabe 2: Benutzersicherheit konfigurieren
Budgetplanung verwendet spezielle Sicherheitsrichtlinien, um den Zugriff auf die Budgetpläne zu konfigurieren. Julia muss den Zugriff auf die Finanzbudgetpläne selbst erteilen. 2.1. Wechseln Sie zum DEMF-juristischerPerson Kontext:![Screenshot10 ([]. -/media/screenschuß 10.png)]". -/media/screenschuß 10.png) 2,2. Navigieren Sie zu Haushaltsplanungs &gt; einstellungs- &gt; Budgetplanung &gt; Budget-Planungskonfiguration. In der Parameterregisterkarte legen Sie den Sicherheitsmodellwert auf Basis Sicherheitsorganisationen fest []![Screenshot11![. -/media/screenschuß 11.png)]". -/media/screenschuß 11.png) 2,3. Navigieren Sie zu den Systemverwaltungs- &gt; Benutzer- &gt; Benutzern. Geben Sie dem Benutzer Admin (Julia Funderburk) die Budget-Manager-Rolle. ![Screenshot12 ([]. -/media/screenschuß 12.png)]". -/media/screenschuß 12.png) 2,4. Klicken Entnahmebenutzerrolle und weisen Organisationen zu ![Screenshot13 ([![. -/media/screenschuß 13.png)]". -/media/screenschuß 13.png) 2,5. Wählen Sie "Zugriff individuell auf spezifische Organisationen erteilen" aus. Wählen Sie die im ersten Schritt erstellte Organisationshierarchie aus. Entnehmen Sie Finanzknoten und klicken Sie auf wichtigem Zuschuss mit *** Schaltfläche der Kinder! *** * – Stellen Sie sicher, dass Sie im Zusammenhang DEMF-juristischerPerson sind, sofern diese Aufgabe, als organisatorische Sicherheit ist empfangener gültiges entity* [] (![ausgeführt wird . -/media/screenschuß 14.png)]". -/media/screenschuß 14.png)

## <a name="task-3-create-scenarios"></a>Abgabe 3: Szenarien erstellen
3.1. Navigieren Sie zur BudgetingSetup-&gt;&gt; Budgetplanung &gt; Budget-Planungskonfiguration. Beachten Sie auf der Szenarioseite die Szenarien, die wir später in dieser Übungseinheit verwenden werden: Vorjahres-Istwerte und Budgetiert. *Hinweis: Sie können neue Szenarien für diese Übung erstellen, wenn sie wünschen, und stattdessen diese verwenden.* ![Screenshot15 ([]. -/media/screenschuß 15.png)]". -/media/screenschuß 15.png) *Note: da Julia formalen Genehmigungsprozess nicht für Budgetausarbeitung verwendet, wird Workflow- überspringen, Phasen- und Workflowphaseneinstellung in dieser Übungseinheit und verwenden vorhandenen Einstellungen für automatischen Vorkalkulationserstellung - Genehmigen Workflow. Siehe Anhang für diesen Workflow configuration.*

## <a name="task-4-create-budget-plan-columns"></a>Abgabe 4: Budgetplanspalten erstellen
Budgetplanspalten sind entweder monitär- oder mengenbasierte Spalten, die im Budgetplan-Dokumentenlayout verwendet werden können. In unserem Beispiel müssen wir eine Spalte für Vorjahres-Istwerte und 12 Spalten für jeden Monat in einem budgetierten Jahr erstellen. Spalten können entweder erstellt werden, indem Sie einfach auf die Schaltfläche "Hinzufügen" klicken und die Werte eintragen, oder mithilfe der "Datenentität". In dieser Übungseinheit verwenden wir "Datenentität", um die Werte einzutragen. 4.1. BudgetingSetup-Budgetplanung &gt;&gt; in der Budgetplanungskonfiguration &gt; Seite " Offen Spalten. Klicken Sie auf Office- auf der oberen rechten Ecke der Formulars und Entnahmen Spalten (ungefiltert) [] (Screenshot16![. -/media/screenschuß 16.png)]". -/media/screenschuß 16.png) 4,2. Das System öffnet die Excel-Arbeitsmappe, die zum Ausfüllen der Werten verwendet wird. Wenn er aufgefordert wird, aktivieren und auf Bearbeitung vertrauen der Zeit-App [] (Screenshot18![. -/media/screenschuß 18.png)]". - /media/screenschuß 18.png)[](![. -/media/screenschuß 17.png)]". -/media/screenschuß 17.png) 4,3. Es müssen mehrere Spalten, um die Werte ein. Klicken Sie auf Entwurf im rechten Bereich, um die Spalten im Raster hinzuzufügen:![Screenshot19 ([]. -/media/screenschuß 19.png)]". -/media/screenschuß 19.png) 4,4. Klicken Sie nach Stiftsschaltfläche neben PlanColumns, um der verfügbaren Spalten zu finden, um dem Raster [] (![hinzuzufügen . -/media/screenschuß 20.png)]". -/media/screenschuß 20.png) 4,5. Doppelklicken Sie für jeden verfügbaren Feld, auf die ausgewählten Felder und auf Aktualisieren [] (Screenshot21![hinzuzufügen. -/media/screenschuß 21.png)]". -/media/screenschuß 21.png) 4,6. Fügen Sie in der Excel-Tabelle alle Spalten hinzu, die erstellt werden müssen. Verwenden Sie die AutoFill-Funktion in Excel, um die Positionen schnell hinzuzufügen. Stellen Sie sicher, dass die Positionen als Teil der Tabelle hinzugefügt werden (sofern von vertikalen Bildlauf verwenden, sollten Sie in der Lage sein, Spaltenüberschriften auf die Oberseite des Rasters"![Screenshot22 [] (zu finden. -/media/screenschuß 22.png)]". -/media/screenschuß 22.png) 4,7. Zurückkehren zu Dynamics 365 für Arbeitsgänge zurück und aktualisieren Sie die Seite. Veröffentlichte Werte werden in Dynamics 365 für Arbeitsgänge. ![Screenshot23 ([]. -/media/screenschuß 23.png)]". -/media/screenschuß 23.png)

## <a name="task-5-create-budget-plan-document-layouts-and-templates"></a>Abgabe 5:Budgetplan-Dokumentenlayouts und - vorlagen erstellen
Layout definiert, wie das Raster der Budgetsplan-Dokumentenpositionen aussieht, wenn ein Benutzer das Budgetplandokument öffnet. Es ist auch möglich, das Layout des Budgetplandokuments zu wechseln, um dieselben Daten aus verschiedenen Winkeln anzuzeigen. Jetzt, da sie die Spalten definiert hat, die in unserem Budgetplandokument verwendet werden, muss Julia ein Budgetsplan-Dokumentenlayout erstellen, das der Excel-Tabelle ähnlich sieht, das sie verwendet, um Budgetdaten zu erstellen (weitere Informationen finden Sie im Abschnitt "Szenarioüberblick" in dieser Übungseinheit) 5.1. In der BudgetingSetup-&gt;&gt; Budgetplanung &gt; Budget-Planungskonfiguration öffnen Sie Layoutseite. Erstellen Sie ein neues Layout für den Monatsbudgeteintrag:

-   Wählen Sie den MA+BU-Dimensionssatz, um dem Layout Hauptkonten und Unternehmenseinheiten hinzuzufügen.
-   Führen Sie alle Budgetplanspalten auf, die im vorherigen Schritt im Elementabschnitt erstellt wurden. Machen Sie alle Istwerte aus denen des Vorjahres bearbeitbar.
-   Klicken Sie auf die Schaltfläche "Beschreibungen", um auszuwählen, welche Finanzdimensionen Beschreibungen im Raster anzeigen sollten.

![Screenshot24 ([]. -/media/screenschuß 24.png)]". /media/screen schoss 24.png) auf Basis der Budgetplanlayoutdefinition, die Sie als alternative Methode zu verwendende Tabelle, auf Budgetdaten erstellen, zu bearbeiten. Da die Excel-Vorlage mit der Budgetplan-Layoutdefinition übereinstimmen muss, sind keine Änderungen am Budgetplanlayout mehr möglich, nachdem Sie die Excel-Vorlage generiert haben. Daher sollte diese Aufgabe erfolgen, nachdem alle Layoutkomponenten definiert sind. 5.2. Für das Layout erstellt in dem Betrag 5,1. Schritt, Schaltfläche Vorlage &gt; generiert werden. Bestätigen Sie die Warnmeldung. Soll die Vorlage angezeigt werden, klicken Sie auf Vorlagen-. *Note: Stellen Sie sicher, wie "Speichern" auswählen und den Ort auszuwählen, in der Vorlage gespeichert werden soll, um diese zu bearbeiten. Wenn Benutzer "Öffnen" im Dialogfeld auswählen, ohne Speichern, werden die Änderungen, die in die Datei geleisteten, nicht beibehalten, wenn die Datei closed.* ist ![Screenshot25 ([]. -/media/screenschuß 25.png)]". -/media/screenschuß 25.png) 5,3. &lt; Optionaler Tabelle " Schritt&gt; ändern, um sie benutzerfreundlicher suchen werden sollen – Fügen gesamte Sie Formeln, Überschriftenfelder, Formatierung, usw. die Änderungen speichern hinzu und laden Sie die Datei zum Budgetplan layout hohe, indem Sie im Layout -![Upload [ &gt; ] (klicken . -/media/screenschuß 26.png)]". -/media/screenschuß 26.png)

## <a name="task-6-create-a-budget-planning-process"></a>Aufgabe 6: Budgetplanungsprozess erstellen
Julia muss einen neuen Budgetplanungsprozess erstellen und aktivieren, der sämtliche oben genannten Einstellungen kombiniert, um mit der Eingabe von Budgetplänen zu beginnen. Der Budgetplanungsprozess definiert, welche Budgetplanungsorganisationen, Workflows, Layouts und Vorlagen zum Erstellen von Budgetplänen verwendet werden. 6.1. Navigieren Sie zu Haushaltsplanungseinstellungs-Budgetplanung &gt; Budgetplanungsprozess &gt; und &gt; erstellen Sie einen neuen Datensatz.

-   Budgetplanungsprozess – DEMF-Budgetierung GJ2016
-   Budgetzyklus – GJ2016
-   Sachkonto – DEMF
-   Standardkontostruktur – Herstellungs-GuV
-   Organisationshierarchie – wählen Sie die Hierarchie, die am Anfang der Übungseinheit erstellt wurde aus
-   Budgetplanungsworkflow – weisen Sie den Workflow für automatische Zuweisung für die Finanzabteilung aus
-   Wählen Sie in den hasenregeln und - vorlagen für die Budgetplanung für jede Workflow-Budgetplanungsphase aus, ob das Hinzufügen und das Ändern von Positionen zulässig ist und welches Layout standardmäßig verwendet werden soll

*Hinweis: Sie können zusätzliche Dokumentlayouts erstellen, und sie zuzuordnen, damit sie in der Budgetplanungs-Workflowphase zur Verfügung stehen, indem Sie auf die Schaltfläche "Alternative Layouts" klicken.* ![Screenshot27 ([]. -/media/screenschuß 27.png)]". -/media/screenschuß 27.png) 6,2. Wählen Sie Aktivitäten &gt; aktivieren, um diesen Budgetplanungsworkflow [aus![Screenshot28![" zu aktivieren. -/media/screenschuß 28.png)]". -/media/screenschuß 28.png)

<a name="exercise-2-process-simulation"></a>Übung 2: Prozesssimulation
==============================

## <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a>Aufgabe 7: Anfängliche Daten für den Budgetplan aus dem Hauptbuch generieren
7.1. Navigieren Sie zur regelmäßigen &gt; Budgetierung &gt; generieren Budgetplan aus dem Hauptbuch. Füllen Sie die periodischen Prozessparameter aus, klicken Sie auf die Schaltfläche "Generieren". ![Screenshot29 ([]. -/media/screenschuß 29.png)]". -/media/screenschuß 29.png) 7,2. Navigieren Sie zu &gt; Budgetplänen, einen Budgetplan zu finden, der durch Generate Prozess erstellt wird. ![Screenshot30 ([]. -/media/screenschuß 30.png)]". -/media/screenschuß 30.png) 7,3. Öffnen Sie Dokumentdetails, indem Sie den Dokumentnummerhyperlink klicken. Budgetplan wird angezeigt, wie im Layout definiert, das während dieser Übungseinheit [![Screenshot31] "erstellt wird. -/media/screenschuß 31.png)]". -/media/screenschuß 31.png)

## <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a>Aufgabe 8: Budget des aktuellen Jahres auf Grundlage der Vorjahres-Istwerte erstellen
Zuordnungsmethoden können im Budegetplan verwendet werden, um Informationen für Budgetpläne einfach von einem Szenario zu einem anderen zu kopieren/sie über Perioden zu verteilen/Dimensionen zuweisen. Wir verwenden Zuweisungen, um das Budget des aktuellen Jahres aus den Vorjahres-Istwerten zu erstellen. 8.1. Entnehmen Sie alle Positionen im Budgetplandokumentraster und Schaltfläche weisen Budget zu ![Screenshot32![[]. -/media/screenschuß 32.png)]". -/media/screenschuß 32.png) 8,2. Wählen Sie, Zuordnungsmethode Periodenschlüssel, Quelle aus und Zielszenarien und weisen Eintrag zu 

![Screenshot33 ([]. -/media/screenschuß 33.png)]". -/media/screenschuß 33.png)

Die tatsächlichen Beträge das vorherige Jahr werden in das Budget des aktuellen Jahres sowie diese periodenübergreifend mithilfe von zuzuweisen kurvenperiodenschlüssels kopiert. 

![Screenshot34 ([]. -/media/screenschuß 34.png)]". -/media/screenschuß 34.png)

## <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a>Abgabe 9: Das Budgetplandokument mithilfe von Excel anpassen und das Dokument fertig stellen
9.1. Klicken Sie auf die Schaltflächen arbeitsblatt mit dem Inhalt offener Dokuments in Excel

![Screenshot35 ([]. -/media/screenschuß 35.png)]". -/media/screenschuß 35.png)

9.2. Wenn die Excel-Arbeitsmappe geöffnet wird, passen Sie die Nummern im Budgetplandokument an, und klicken Sie auf die Schaltfläche "Veröffentlichen".

![Screenshot36 ([]. -/media/screenschuß 36.png)]". -/media/screenschuß 36.png)

9.3. Kehren Sie zum Budgetplandokument in Dynamics 365 für Arbeitsgänge zurück. Klick-Workflow übermitteln, um das Dokument Auto-zugenehmigen

![Screenshot37 ([]. -/media/screenschuß 37.png)]". -/media/screenschuß 37.png) 

Sobald Workflow abschließt, wird Budgetplandokumentphase zu genehmigtem. ![Screenshot38 ([]. -/media/screenschuß 38.png)]". -/media/screenschuß 38.png)

<a name="appendix"></a>Anhang
========

### <a name="auto-approve-workflow-configuration"></a>Workflowkonfiguration für automatische Genehmigung

A. Haushaltsplanungshaushaltsplanungsworkflow &gt; der &gt; Einstellungs- planung Erstellen &gt; eines neuen Workflows mithilfe der Vorlage Budget-Planungsworkflow:

![Screenshot39 ([]. -/media/screenschuß 39.png)]". -/media/screenschuß 39.png)

Dieser Workflow enthält nur eine Aufgabe – Phasenübergangsbudgetplan 

![Screenshot40 ([]. -/media/screenschuß 40.png)]". -/media/screenschuß 40.png) 

Speichern und Aktivieren des Workflows. 

B. Navigieren Sie zu Haushaltsplanungs &gt; einstellungs- &gt; Budgetplanung &gt; Budget-Planungskonfiguration. In der Phasenregisterkarte erstellen Sie 2 erste und Sendedaten Phasen - 

![Screenshot41 ([]. -/media/screenschuß 41.png)]". -/media/screenschuß 41.png)

C. Navigieren Sie zu Haushaltsplanungs &gt; einstellungs- &gt; Budgetplanung &gt; Budget-Planungskonfiguration. In der Workflow-Phasenregisterkarte Ordnet das Auto Workflow zu – Genehmigt Sie in den ersten a-Schritt mit Phasen und gesendet 

![Screenshot42 ([]. -/media/screenschuß 42.png)]". -/media/screenschuß 42.png)  


