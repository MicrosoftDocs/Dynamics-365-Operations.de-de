---
title: "Budgetierungsüberblick"
description: "Fast jedes Unternehmen, das Financials-Funktionalität in Microsoft Dynamics 365 for Finance and Operations verwendet, muss Berichte erstellen können, die das Budget und den Ist-Status aufzeigen. In diesem Artikel wird beschrieben , wie die Mindstkonfiguration sein muss, um Budgets in Dynamics 365 for Finance and Operations zu erstellen oder diese aus einem Programm einer Drittpartei hochzuladen."
author: twheeloc
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 60113
ms.assetid: 28a9793e-d376-47af-a345-69046bad17df
ms.search.region: global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 1d768ee6d2244a237972f7183f27a60b93eea819
ms.contentlocale: de-de
ms.lasthandoff: 03/26/2018

---

# <a name="budgeting-overview"></a>Budgetierungsüberblick 

[!include[banner](../includes/banner.md)]


Fast jedes Unternehmen, das Financials-Funktionalität in Microsoft Dynamics 365 for Finance and Operations verwendet, muss Berichte erstellen können, die das Budget und den Ist-Status aufzeigen. In diesem Artikel wird beschrieben , wie die Mindstkonfiguration sein muss, um Budgets in Dynamics 365 for Finance and Operations zu erstellen oder diese aus einem Programm einer Drittpartei hochzuladen.

<a name="overview"></a>Überblick
--------

Das genehmigte Budget für eine juristische Person wird in einem Dokument verwaltet, das als *Budgetregistereintrag* bekannt ist. Die Positionen in einem Budgetregistereintragsdokument wird als *Budgetkonto*bezeichnet und enthält Finanzdimensionsinformationen, Datumsangaben und Beträge der genehmigten Budgets. Das Budgetregistereintragsdokument wird mit grundlegenden Finanzberichten und Abfragenseiten ergänzt, in dem die tatsächlichen Beträge des Sachkontos mit den Budgetbeträgen verglichen werden. 

Es gibt mehrere Möglichkeiten zum Erstellen von Budgetregistereinträgen in Finance and Operations:

-   Geben Sie die Dokumentinformationen auf der Seite **Budgeterfassungseinträge** manuell ein.
-   Verwenden Sie die Microsoft- Excelvorlage, die geöffnet können, indem Sie auf der Seite **in Excel öffnen** auf die Schaltfläche **Budgetregistereinträge** klicken.
-   Verwenden Sie die **Budgetkontoeinträge** Datenentität in der Datenverwaltung, um Budgetregistereinträge zu importieren. Sie sollten in Betracht ziehen, diese Methode anzuwenden und den **Prozessparameter** **Set-basiert** setzen,  wenn viele Budgetkontoeinträge in das System importiert werden müssen.
-   Wenn das Unternehmen Planungsfunktionen plant, um Budgetdaten vorzubereiten, können Sie den periodischen Prozess **Budgetregistereintrag erstellen** verwenden.

Der Budgetregistereintrag wird als abgeschlossen betrachtet, wenn die Budgetsalden aktualisiert wurden. Auf der Seite **Budgeterfassungseinträge** klicken Sie auf **Budgetsalden aktualisieren**, um ausgewählte Budgeteinträge oder Mehrfacheinträge zu machen. Nachdem Sie die Budgetsalden aktualisiert haben, wird der Status des Budgetregistereintrags auf **Abgeschlossen** gesetzt. Ein abgeschlossener Budgetregistereintrag kann nicht erneut zum Bearbeiten geöffnet werden. Wenn die Budgetdaten angepasst werden müssen, müssen Sie einen neuen Budgetregistereintrag erstellen, anstatt die Daten im abgeschlossenen Budgetregistereintrag zu korrigieren.

## <a name="configuration"></a>Konfiguration
Wenn Sie die Budgetierung konfigurieren, beginnen Sie auf der Seite **Budgetierungsparameter**. Auf dieser Seite müssen Sie die Budgeterfassung, die Zahlenfolge für die Budgetregistereinträge und das Standardverhalten in den Arbeitsbereichen definieren.

Wenn es Richtlinien gibt, die die Genehmigung von Budgetregistereinträgen basierend auf dem Budgettyp regeln (beispielsweise Übertragungen oder Überarbeitungen), müssen Sie Budgetregistereintrags-Workflows auf der Seite **Budgetierungs-Workflows** erstellen. Sind Szenarien vorhanden, bei denen Übertragungen ohne Workflowgenehmigung zulässig sind, können Sie Budgetübertragungsregeln definieren, die diese Szenarien unterstützen. 

Wählen Sie auf der Seite **Budgetierungsdimensionen** Finanzdimensionen, die für die Budgetierung basierend auf den im Kontenplan verwendeten Dimensionen verwendet werden. Sie können für die Budgetierung alle Finanzdimensionen oder eine Auswahl davon auswählen.

Definieren Sie ein *Budgetmodell*, das allen oder einigen Budgets entspricht. Sie können ein einziges Budgetmodell für alle Budgetregistereinträge verwenden. Alternativ können Sie separate Modelle erstellen, die auf dem Budgettyp, dem geografischen Standort oder einen beliebigen anderen Methode, mit der ein Budget klassifiziert werden kann, basiert. 

> [!NOTE] 
> Wenn die Budgetsteuerung verwendet wird, können Sie nur ein Budgetmodell einer bestimmten Zeitspanne für den Budgetzyklus zuordnen. 

Erstellen Sie *Budgetcodes*, die den Typ der zu erfassenden Budgettransaktionen und die damit im Zusammenhang stehende Workflows identifizieren. Budgetcodes können die folgende Budgettypen unterstützen:

-   Ursprüngliches Budget
-   Umlagerung
-   Überarbeitung
-   Belastung
-   Vorabbelastung
-   Vortragsbudget

Budgetcodes geben Ihnen einen Audit-Trail mit den im Verlauf des Budgetzyklus genehmigten Budgetänderungen. Wenn ein Workflow einem Budgetcode zugeordnet ist, wird der Workflow aktiviert für alle Budgetregistereinträge, die diesen Budgetcode verwenden, und Workflowschritte müssen ausgeführt werden, bevor dem Budgetregistereintrag Phase **Abgeschlossen** eingeben kann.  

Sie können optional auch *Budgetübertragungsregeln* festlegen. Wenn Sie  Budgetübertragungsregeln verwenden, wählen Sie **Regeln für Budgetübertragungen** auf der Seite **Budgetparameter** aus. Wenn Budgetübertragungsregeln verwendet werden, wenn ein Benutzer ein Dokument mithilfe des Budgetcodes vom Typ **Übertragen** erstellt, werden Budgetsalden nicht aktualisiert, wenn die Budgetübertragungsregeln verletzt werden. Sie können beispielsweise Budgetübertragungsdokumente zulassen, wenn das Ausgabenbudget zwischen den Hauptkonten für die Vertriebs- und Marketingabteilung übertragen werden, kann jedoch verhindern, dass Budget von dieser Abteilung oder zu dieser übertragen wird, sofern keine Workflowgenehmigung für diesen Typ von Budgetkontoeinträgen gewährt wurde.

## <a name="using-workspaces-and-inquiry-pages-to-track-budget-vs-actuals"></a>Verwenden der Arbeitsbereiche und Anfragenseiten, um des Budgets im Vergleich zum Istwert zu verfolgen
Der Budget-Manager kann den aktuellen Status eines Budgets im Arbeitsbereich **Sachkontobudgets und Planungen** überprüfen. Die Registerkarten **Ausgaben über Budget** und **Umsatzerlös unter Budget** geben einen raschen Überblick über die Finanzdimensionskombinationen, wenn Budgetziele nicht erfüllt werden oder sich dem Schwellenwert nähern. Sie können den Budgetschwellenwertprozentsatz und die Finanzdimensionssätze, die in diesen Registerkarten verwendet werden, personalisieren, indem Sie den **Meinen Arbeitsbereich konfigurieren** anklicken. Sie können auf **Einheiten-Manager** klicken, um die Arbeitskräfte anzuzeigen, die für bestimmte Finanzdimensionskombinationen, die auf diesen Registerkarten ausgewählt werden, verantwortlich sind. Wenn Sie beispielsweise sehen, dass das Ausgabenbudget der Betriebsabteilung den Budgetschwellenwert überschreitet, können Sie den Betriebsabteilungsmanager einfach auffinden, um das Problem zu diskutieren. 

> [!NOTE] 
> Das Feld **Abteilungsleiter** auf der Seite **Organisationseinheiten** bestimmt, welche Manager bestimmte Finanzdimensionskombinationen unterstützen. Klicken Sie **Mehr** am unteren Rand der Registerkarte, um die Abfrageseite **Budget im Vergleich zum Istwert** zu öffnen, um weitere Details zu Budgetbeträge im Vergleich zu den aktuellen Beträgen zu erhalten. 

Auf der Abfrageseite **Istwert verglichen mit Budget** können Sie zu den Details des Budgets im Vergleich zu den Istwerten blättern. Wählen Sie eine Position auf der Abfrageseite aus und klicken Sie dann **Periodensaldi** an, um das Budget und die Istwerte im Finanzzeitraum anzusehen. Die Seite **Budgetkontoeinträge** enthält Drillthroughs zu den Details des Budgetbetrags im Budgetregistereintrag. Die Seite **Allgemeine Erfassungseinträge** öffnet die Sachkontobuchungen, die im berechneten Betrag **Istwerte** enthalten sind. 

Ein Unternehmen, das Budgetplanungsfunktionen verwendet, kann im Arbeitsbereich unter *Sachkontenbudget und Planung*. **Budgetplanung** verwenden.




